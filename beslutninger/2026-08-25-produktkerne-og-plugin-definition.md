# [SDR]Definition af OS2Display produktkernen og plugin-system

- **Dato**: 2026-08-25
- **Status**: Udkast
- **Beslutningstagere**: Styregruppen
- **Beslutningstype**: Strategisk

## Kontekst/ Årsag
Produktforvaltningen ønsker en afgrænsning af hvilke dele af kodebasen som fællesskabet har ansvaret for at vedligeholde og hvilke dele det påfalder anvenderkommunerne at vedligeholde.

Hidtil har grundreglen været, at al kode i main-branch på os2display-api-service er at betragte som systemkerne, som skal vedligeholdes  af fællesskabet. Dvs. at når først en feature er inde i produktet, overgår den automatisk til at være et fælles anliggende, som skal holdes fejlfri og sikkerhedsopdateret af fællesskabet.

Den grundregel har vi brug for at gradbøje. Der findes i OS2Display et plugin-system bestående af templates og datakilder. Plugins bruges ofte til at integrere med tredjepartssystemer, som kun er i brug hos én eller ganske få kommuner.

### Grunde til forvaltningsmæssigt at skelne mellem kerne og plugins: 

1. Plugin-systemet er stort og voksende. OS2Displays økonomi kan ikke følge med. Hvis plugins skal vedligeholdes af fællesskabet skal indtægterne til fællesskabet (produktvederlaget) hæves. 

2. Det er især de største kommuner der udvikler plugins til tredjepartssystemer. Det er ikke rimeligt, at de mindre kommuner skal betale for vedligeholdlse for de største kommuners sær-løsninger.

3. Systemintegrationer kan kun fejlsøges og vedligeholdes af en leverandør med adgang til det underliggende tredjepartssystem. Det betyder, at en vedligeholdelsesleverandør, som OS2 tegner kontrakt med ifht. vedligehold af produktkernen, ikke har adgang og viden til at kunne vedligeholde alle tredjepartsintegrationer.

Som eksempel på punkt 3 vil ITK ikke kunne fejlsøge og udvikle på Københavns plugins, da de ikke har de nødvendige adgange eller den nødvendige viden om Københavns systemer.

Omvendt vil Bellcom ikke kunne fejlsøge og udvikle på Aarhus' eventdatabase-integration, da det kræver adgang og viden om et internt Aarhus-system.

## Installations- og opgraderingspakke
I forbindelse med OS2Display version 3 er der udviklet en installationspakke som kan bruges af både driftsleverandører samt kommuner, der ønsker at hjemtage produktet til lokal drift. 

Installationspakken bør betragtes som en kernekomponent, da produktet ikke kan udbredes, hvis det ikke kan installeres. 

## Vurdering

Produktforvaltningen vurderer, at der er behov for en strategisk beslutning der afgrænser fællesskabets ansvarsområde ifht. kerneprodukt og plugins, for at produktets vedligeholdelsesomkostninger kan holdes inden den givne økonomiske ramme.

En klar definition af produktkernen vil i øvrigt lette forventningsafstemning mellem anvenderkommuner og produktforvaltning, og skabe klarhed omkring hvad der falder inden for en den kodevedligeholdelsesaftale, der på sigt skal inggås mellem en leverandør og OS2Display produktfællesskabet.

## Indstilling

Udforming af afgrænsningskriterier har været drøftet i koordinationsgruppen.
Koordinationsgruppen indstiller at følgende afgrænsninger af produktkernen vedtages af styregruppen.

1. Al kode og dokumentation i produkt-repo os2display-api-serveice er en del af kerneproduktet. Undtaget er komponenter nævnt i punkt 2.

2. Datakilder og templates vedligeholdes IKKE af produktfællessakbet. Det er de kommuner der bruger dem, der har ansvaret for at holde dem opdateret. Alle udgifter til udvikling, review og evt. sær-release betales af de kommuner, der anvender disse. Undtaget denne regel er komponenter nævnt i punkt 3.
    
3. Nogle templates uden afhængigheder til tredjepartssystemer og som de fleste kommuner bruger, holdes vedlige af produktfællesskabet. Det er i sidste instans koordinationsgruppen, der beslutter hvilke templates, der vedligeholdes af produktfællesskabet

4. Al kode og dokumentation i installationspakke-repo os2display-docker-server er en del af kerneproduktet.


## Implementering
En afgrænsning af kerneproduktet vil skulle følges op af ændrede processer i produktforvaltningen. 


- Sagsstyring på Github. Det skal fremgå tydeligt hvem der er bestiller og betaler på alle sager.

- Leverandørdialog og leverancestyring. Produktfoirvaltningen støtter kommuner der tager initiativ til plugin-udvikling. Kode uden for produlktkernen skal leve op til de samme kvaliteskrav som kode inde i karnen, da det indlejres i den fælles kodebase og kan kan true driftsstabilitet og sikkerhed for alle hvis kodekvaliteten er lav.

- Crowd-funding. Produktforvaltningen skal være behjælpelig med at facilitere crowd-funding når anvenderkommuner sammen skal udvikle og vedligeholde et plugin.

- OS2 fællesskabet skal i god tid varsle hvis der introduceres ændringer i  OS2Display-kernen, der påvirker plugin-laget. Det kan f.eks. være opdatering af React, Symfony eller lignende.

- Hvis der er plugins, som efterlades uden vedligeholdelse, bør fællesskabet finansiere en "nedrivningspulje" til fjernelse af disse.