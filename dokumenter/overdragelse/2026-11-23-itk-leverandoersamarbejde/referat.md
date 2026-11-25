#  OS2display workshop den 23 november 2026

### Rammer for leverandørsamarbejde efter 1/1 2027

**DELTAGERE**
- ***Aarhus Kommune*** - Nuværende ejer af produktet
- ***OS2display produktforvaltningen*** - fremtidig ejere af produktet
- ***ITK-development v. Aarhus kommune*** - udviklings- og vedligeholdelsesleverandør

### Plan for dagen

- **10.00 - 10.15** : Introduktion og velkomst
- **10.15 - 11.30** : Session 1: Samarbejdsprincipper & Nøglebegreber
- **11.30 - 12.00** : ***Frokost på OS2's regning***
- **12.00 - 13.30** : Session 2 : Workflow & arbejdsprincipper
- **13.30 - 14.30** : Session 3 : Åben Teknisk workflow
- **14.30 - 15.30** : Session 4 : Forvaltningsmodel og leverandøraftaler
- **15.30 - 15:45** : ***Farvel og tak for i dag***

Til stede er: Anna, Ture, Troels, Lene, Anna-Lis, Agnete

## Session 1: Samarbejdsprincipper & Nøglebegreber

### Formål: 
ITKs nøglemedarbejdere får en forståelse af forløbet og hvad der forventes. OS2 får en forståelse af hvor der er diskrepans imellem leverandørens gældende praksis og den fremtidige samarbejdsmodel.

Mødet handlede om samarbejdsprincipper, nøglebegreber og den kommende forvaltningsmodel. Formålet var at forventningsafstemme og identificere forskelle mellem nuværende arbejdsform og modellen efter 1.1.2027.

### Status lige nu

Status er at backloggen er overdraget, mens den formelle overdragelse af kildekoden, ejerskab og IPR skal afklares efter nytår med Aarhus Kommune.

Styregruppe er til godkendelse på OS2 bestyrlesesmøde den 16.12. og mødes første gang i januar.

Ifht. til migration til version 3: Sønderborg er overflyttet. Vejle er i proces- PO har rykket for status. Bellcoms kunder overflytter 25/11.


### Rammer og hovedprincipper for samarbejde med OS2-fællesskabet 

Ny anvenderrolle blev drøftet: Issue Lead, der skal sikre ansvar for fremdrift, økonomi og test.
Vi blev enige om at Milestone Owner var en bedre titel, og at issues skal knyttes op på milestones.

Følgende principper blev gennegået på mødet:

- Alt starter med et issue
- Alle issues er fra starten assigned til PO'en. 
- Alle issues/bidrag vurderes af PO ift. compliance med produktstrategien. Product owner fungerer som gateway for aktiviteter.
- Det er styregruppe og koordinationsgruppe der beslutter produktstrategien på vegne af fællesskabet.
- Alle beslutninger dokumenteres i ADR / ODR / SDR
- ADR initieres i issue som alle andre bidrag, og skal reviewes og godkendes af produktforvaltning

- Ingen arbejder på opgaver der ikke har en Milestone Owner
- Sager uden Milestone Owner er i backlog / on hold
- Ingen starter på opgaver før de er assignet
- Alle bidragsydere behandles principielt ens
- Alle bidrag skal gennem code review
- Der er forskellige review-krav til kodebidrag i hhv. core-zoner / plugin-zoner jvf. ADR
- Kodestandarder er klart defineret og integreret i CI-pipeline

- PO assigner Milestone Owner når issue vurderes compliant og tilstrækkelig beskrevet
- Milestone Owner og deres leverandør aftaler det videre forløb
- Alt samarbejde foregår i GitHub for at opretholde transparens i samarbejdet
- Hele udviklingsforløbet samt review betales af Milestone Owner
- Release betales af OS2 fællesskabet


## Hvad skal der ske nu?

Der skulle arbejdes videre med:

- formel godkendelse af styregruppen på OS2’s bestyrelsesmøde den 16.12.
- afholdelse af første styregruppemøde i januar
- senere afklaring af den formelle overdragelse af kildekode og IPR fra Aarhus Kommune
- videreudvikling af milestone owner-rollen
- videre arbejde med release-proces og GitHub-organisering

Liste over opgaver:

1. Formel godkendelse af styregruppe
   - Ansvarlig: OS2’s bestyrelse
   - Deadline: 16.12.

2. Afholdelse af første styregruppemøde
   - Ansvarlig: OS2 / produktforvaltningen
   - Deadline: Januar

3. Afklaring af overdragelse af kildekode og IPR
   - Ansvarlig: Aarhus Kommune
   - Deadline: Efter 1. februar

4. Videreudvikling af model for milestone owner
   - Ansvarlig: Produktforvaltningen i dialog med deltagerne
   - Deadline: Ikke fastsat

# Session 2:Workflow & arbejdsprincipper

## Formål
Leverandørens nøglemedarbejdere får en forståelse af OS2displays tekniske forvaltningsmodel fremover.
OS2display får leverandørens input til hvordan man operationaliserer den tekniske forvaltningsmodel.

## Fokus
- Samarbejdsmodel og arbejdsflow
- Gitflow
- Releaseproces
- Contribution flow
- Brugerinvolvering og brugertest
- Kontrakt- og aftalestruktur

### Kodeoverdragelse og juridisk overdragelse
Den væsentligste resterende overdragelse er juridisk. Der mangler et formelt overdragelsesdokument og en formel aftale, selv om den tekniske overdragelse i praksis langt hen ad vejen er gennemført.


### Transitionsperiode og dobbelt samarbejde i første kvartal
Første kvartal blev beskrevet som en transitionsperiode med overlap og dobbelt samarbejde. Flere forhold skal afklares i praksis, fordi ikke alle regler er på plads fra start.


### Drift, first line-support og afgrænsning af ansvar
Kodevedligehold, driftvedligehold og udvikling skal holdes kontraktmæssigt adskilt.
Vedligeholdelsesleverandøren skal ikke være first line-support. GitHub-sager skal først afklares via PO i gatekeeperfunktionen. Driftssager skal skilles fra fejl i kildekoden og sendes til driftleverandøren, hvis problemet ligger i driften.


### Fallback-plan for Aarhus, fork og hotfixes
Fallback-planen er en fork, som kan bruges til hotfixes, hvis Aarhus skal prioriteres hurtigt. Samtidig blev det understreget, at ændringer fra en fork skal contributes tilbage til core for at undgå permanent opsplitning.


### Kontraktstruktur og roller
Agnete er frikøbt som “Product Owner Light”. Der blev peget på behov for en revideret aftale med Sønderborg og sandsynligvis flere timer. Der blev også drøftet behov for administrativ støtte, men det blev sagt direkte, at der ikke er penge til en egentlig produktkoordinator.


### Vedligeholdelsesleverandørens opgaver og månedlige releases
OS2display produktfællesskabet ønsker at indgå en vedligeholdelsesaftale med månedlige releases. OS2display produktfællesskabet  betaler for, at produktet holdes opdateret, og ITK kan derefter i en anden rolle som driftsleverandør for Aarhus Kommune rulle releases ud på kundens miljø. 

Der blev gennemgået en teknisk vedligeholdelsesprocedure med opdatering af direkte afhængigheder til nyeste minor/patch, håndtering af indirekte afhængigheder, brug af composer outdated og composer audit, vurdering af deprecations, opdatering af Docker images og releasearbejde. Major-versioner af frameworks og direkte afhængigheder ligger uden for den almindelige vedligeholdelsesaftale.

Ture sender ITKs interne arbejdsbeskrivelse for opdatering og release. Ud fra den vil Agnete skrive et produktspecifikt tillæg til en vedligeholdelseskontrakt.


### Releaseproces, test og release candidates
Der var enighed om at droppe et egentligt release-candidate-lag for de månedlige patch- og minor-releases. I stedet skal testkravet ligge tidligere i processen. Den part, der får udviklet funktionalitet, skal selv sikre, at funktionaliteten er testet og accepteret, inden code review går i gang. 

Muligheden for at bygge images som del af code review blev vurderet som relevant, men som en option. 

For majors blev det vurderet, at release candidates fortsat giver mening.

### Sikkerhedsissues og lukket håndtering
Sikkerhedsbrud skal indberettes, men ikke alle sikkerhedssager bør ligge åbent på GitHub. Ved alvorlige sikkerhedssager blev det foreslået at arbejde i et lukket rum eller en privat fork og først offentliggøre patch og dokumentation, når løsningen er klar. Processen er beskrevet i SECURITY.md.

### Code review, prisstruktur og afregning
Code review er en betalingsydelse og skal beskrives tydeligt. Code review skal foregå på GitHub for at sikre transparens, og merge til develop er en del af leverancen. Milestone owner betaler for code review. Der skal laves en aftaleskabelon eller et issue template for code review. Der bør indarbejdes svarfrister og tidsfrister i aftalen.


### Crowdfunding-model for udvikling
Der blev drøftet en model, hvor OS2-projektet finansierer grundlæggende vedligeholdelse, mens konkrete udviklingsprojekter finansieres direkte af de kommuner, der ønsker funktionaliteten. Kommunerne kan enten bidrage med finansiering eller udviklertimer. Som eksemple blev Sønderborg nævnt som mulig milestone owner i forbindelse med M365-sporet, mens Næstved og Ballerup kan være medfinansierende.


### Næste skridt
- Input fra mødet skal bruges til at operationalisere den tekniske forvaltningsmodel i dokumentation og aftaler.
- Der skal udarbejdes et formelt overdragelsesdokument og en formel aftale om den juridiske kodeoverdragelse.
- Der skal laves en midlertidig vedligeholdelsesaftale for den første periode.
- Der sættes en månedlig pris der kan reguleres kvartalsvis ifht. faktisk timeforbrug
- Den månedlige releaseproces skal beskrives mere konkret.
- Der skal udarbejdes en aftaleskabelon eller et issue template for code review.
- Produktforvaltningen skal afklare hvilke optioner vedligeholdelsesleverandøren skal kunne tilbyde.
- Der skal etableres mulighed for, at PO kan købe rådgivningstimer hos vedligeholdelsesleverandøren, eksempelvis op til 10 timer om måneden.




