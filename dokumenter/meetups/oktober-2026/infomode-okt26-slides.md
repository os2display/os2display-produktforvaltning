---
marp: true
paginate: true
header: '![OS2](../../OS2_logo_SVG.svg)'
---
<!-- _class: cover -->
<img class="power-mark" src="../../OS2-on-symbol-green.svg" alt="" aria-hidden="true" />

# OS2display webinar
### Produktdemonstration og planlagt M365 integration
22. oktober 2026 kl. 14 - 15:30

<!-- Note: Velkommen til OS2Display informationsmøde. Det koordinationsgruppen pg produktforvaltning der er værter i dag. Vi har sammensat et bredt program hvor der både er noget for nysgerrige der bare vil se hvad OS2Display er for noget og så er der også programpunkter for garvede brugere fra medlemskommunerne, leverandører og udviklrere. Jeg har sat tider på dagsordenen så man evt kan koble lidt fra de dele af mødet man er mindst interesseret i. Jeg vil som mødeleder holde styr på tiden.

  -->

---

# OS2display produktfællesskabet
<div class="columns membership">
<div>


- Aarhus Kommune
- Ballerup Kommune
- København Kommune
- Køge Kommune
- Næstved Kommune
- Sønderborg Kommune
- Vejle Kommune



</div>

<blockquote>

“Fælles og solidarisk finansiering af vedligeholdelse, sikkerhed og videreudvikling af produktet”

</blockquote>

</div>

<!-- Note: 

NHvad betyder det at en myndighed er tilsluttet produktfællesskabet?

- Fælles og solidarisk finansiering af vedligeholdelse, sikkerhed og videreudvikling af produktet.

- Indflydelse på produktets fremtid gennem fælles prioritering af udviklingsønsker og deltagelse i produktets styring.

- Rådgivning og videndeling gennem produktforvaltningen og samarbejdet med andre kommuner.

--->

---

# Organisering i OS2display

### Koordinationsgruppe

- Mads Lykke, Aarhus Kommune
- Michael Wolf, Københavns Kommune
- Lars Kjær Lauridsen, Næstved Kommune
- Michael Walbum, Ballerup Kommune
- Mads Agerbo Knude, Aarhus Kommune


### Produktforvalter 
Agnete Moos, Sønderborg Kommune (siden 1. januar 2026)

<!-- Note:
Ansat i Sønderborg Kommune ansvar for 60 infoskærme. 

Udlånt 8 timer om ugen til at varetage opgaven som OS2display produktkoordinator.

 I Sønderborg Kommune er OS2display startet på biblioteket, kører nu også ude i nogle sportshaller hvor der vises banebooking via en integration til BRND. Næste skridt i Sønderborg bliver at brede systemet ud til folkeskoler og daginstitioner.

Historien om dette arrangement.  -->

---





# OS2display version 3

### Oprydning og teknisk kvalitetssikring - tre komponenter samles i en

### Installetion

- Installtionspakke vedligeholdt af fællesskabet
- interaktiv installationswizard til hurtigt demosite eller seriøs driftsinstalletion
- Menubaseret ystemadministration
- Grundig dokumentation vedr. drift og opdatering

### Udvikling:
- Nemmere at tilføje skabeloner og dataintegrationer 
- Enkel etablering af et udviklingsmiljø
- Omfattende teknisk udvikler dokumentation 



<!-- Note:
Der er en ny Større udgave  af OS2display meget tæt på udgivelse. Den kører allerede på flere skrme i Aarhus og udrulles i drift i Sønderborg. Der er mindre mangler, men de er småtingsafdelingen. 

Version 3 er et tigerspring fremad i teknisk modenhed

Vi sidder i Næstved og tænker at det kan vi ikke bruge til så meget. 
Nedbringe omkostninger og gøre systemet tilgængeligt for flere leverandører. 

Det er også grunden til at det nu giver mening at tale om M365 integration, arrangementsplakater fra Folkebibliotekernes CMS, TopDesk integration og hvad der ellers tales om. Nu er det faktisk muligt. Version 3 er den trædesten der bringer os derhen hvor vi kan gå i gang med alt det sjove.
-->

---

# Økonomi i en kommune

# Bellcom produktleverandør

Starter optagelse

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700;800&display=swap');
:root {
  --os2-green: #3a7f3b;
  --os2-green-dark: #1b3c1c;
  --os2-gray: #727272;
  --os2-light-gray: #e3e3e3;
}
section {
  background: #fff;
  border-left: 10px solid var(--os2-green);
  color: #231f20;
  font-family: "Open Sans", "Noto Sans", sans-serif;
  justify-content: flex-start;
  padding: 80px 70px 48px 78px;
}
section > header {
  left: auto;
  position: absolute;
  right: 70px;
  top: 24px;
  z-index: 2;
}
section > header img {
  display: block;
  height: auto;
  width: 120px;
}
h1, h2, h3 {
  color: #231f20;
  font-weight: 700;
}
h2, h3 {
  color: var(--os2-green);
}
section > h1,
section > h2:first-of-type {
  border: 0;
  color: #000;
  font-size: 1.5em;
  font-weight: 800;
  line-height: 1.15;
  margin: 0 0 0.6em;
  padding: 0;
}
section > h1::after,
section > h2:first-of-type::after {
  background: var(--os2-green);
  content: "";
  display: block;
  height: 4px;
  margin-top: 0.55em;
  width: 200px;
}
p, li {
  line-height: 1.3;
}
li::marker {
  color: var(--os2-green);
}
section::after {
  color: var(--os2-gray);
  font-size: 0.45em;
}
section.cover {
  align-items: flex-start;
  border: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 80px;
}
section.cover .power-mark {
  height: 600px;
  max-width: none;
  opacity: 1;
  position: absolute;
  right: -200px;
  top: 90px;
  width: auto;
}
section.cover h1 {
  border: 0;
  color: #000;
  font-size: 1.8em;
  margin: 0 0 0.3em;
  max-width: 74%;
  position: relative;
  z-index: 1;
}
section.cover h1::after {
  display: none;
}
section.cover h3 {
  color: var(--os2-green);
  font-size: 0.7em;
  font-weight: 600;
  line-height: 1.3;
  margin: 0 0 1.8em;
  max-width: 74%;
  position: relative;
  z-index: 1;
}
section.cover > p {
  color: var(--os2-gray);
  font-size: 0.55em;
  margin: 0;
  max-width: 74%;
}
.columns {
  display: block;
}
.columns > div:first-child {
  background-color: var(--os2-green);
  color: #fff;
  padding: 1em;
}
.columns > div:first-child li::marker {
  color: #fff;
}
.membership {
  align-items: center;
  display: grid;
  gap: 1em;
  grid-template-columns: 1fr 1.2fr;
}
.membership > blockquote {
  background: var(--os2-light-gray);
  border-left: 8px solid var(--os2-green);
  color: #000;
  font-size: 1.1em;
  font-weight: 800;
  margin: 0;
  padding: 1em;
}
.membership > blockquote p {
  margin: 0;
}
</style>