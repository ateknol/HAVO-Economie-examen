# Volledige Samenvatting · HAVO Economie

## Hoofdstuk 1 — *Samenwerken is een spel*  ·  Hoofdstuk 2 — *Risico & Informatie*

> [!NOTE]
> Deze samenvatting dekt alle paragrafen (1.1 t/m 1.5 en 2.1 t/m 2.3), plus de begrippenlijsten, formules en EU/MVO-theorie uit de overige bronnen. Print-klaar, B1-niveau, met invalshoeken, professionele Mermaid-diagrammen en LaTeX-formules.

---

## 📖 Leeswijzer — hoe gebruik je dit document?

Dit document werkt op **drie lagen** per onderwerp. Lees ze altijd in deze volgorde, dan beklijft de stof veel sneller:

| Laag | Markering | Wat staat er? | Waarom? |
|---|---|---|---|
| **1. Definitie & feiten** | gewone tekst, tabel | Begrip + voorbeeld + formule | Examen vraagt vaak letterlijke definitie |
| **2. Causale keten** | `> [!IMPORTANT]` | Stap-voor-stap *waarom* het werkt zoals het werkt | Het examen test of je het mechanisme begrijpt |
| **3. Examenvalkuil** | `> [!CAUTION]` | Veelgemaakte fout / nuance | 1-2 punten extra die anderen verliezen |
| **4. Examen-truc** | `> [!TIP]` | Slimme aanpak / herkennings-trick | Tijd winnen op de toets |

### Iconen & invalshoeken in dit document

| Icoon | Betekenis | Mermaid-kleur |
|---|---|---|
| 👤 | Invalshoek **Consument** | 🟦 Blauw |
| 🏭 | Invalshoek **Producent** | 🟩 Groen |
| 🏛️ | Invalshoek **Markt / Overheid** | 🟪 Paars |
| 🧠 | "Begrijp de Logica" — causale keten | — |
| ⚠️ | Examenvalkuil | — |
| 🧮 | Rekenformule of -voorbeeld | — |
| 🔁 | Verband met ander begrip elders in de samenvatting | — |

```mermaid
flowchart LR
    DEF{{"1️⃣ Definitie<br/>weet wat het is"}} --> LOG(["2️⃣ Begrijp de Logica 🧠<br/>weet WAAROM"])
    LOG --> VAL[/"3️⃣ Valkuil ⚠️<br/>vermijd punt-aftrek"/]
    VAL --> EX([4️⃣ Examen<br/>pas toe in casus])

    classDef stap1 fill:#e0e7ff,stroke:#4338ca,stroke-width:2px,color:#1e1b4b
    classDef stap2 fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    classDef stap3 fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef stap4 fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f

    class DEF stap1
    class LOG stap2
    class VAL stap3
    class EX stap4
```

---

# HOOFDSTUK 1 · SAMENWERKEN IS EEN SPEL

---

## 1.1 Speltheorie

### Wat is speltheorie?

**[Invalshoek: 🏛️ De Markt / Overheid]**

- **Speltheorie** = theorie over de manier waarop mensen beslissingen nemen, waarbij ze rekening houden met de mogelijke uitkomst van keuzes van anderen.
- Uitgangspunt: spelers (consumenten, bedrijven, overheid) beslissen **rationeel** (met verstand, zonder emotie).
- In de praktijk is menselijk gedrag vaak onvoorspelbaarder dan de theorie.

> [!IMPORTANT]
> **Begrijp de Logica — Waarom überhaupt "speltheorie"?**
>
> Bij een gewone vraag/aanbod-markt heb je **veel** anonieme spelers — niemand kan in z'n eentje de prijs beïnvloeden. Maar zodra er **weinig** spelers zijn (oligopolie, twee landen, twee aannemers), wordt jouw winst direct beïnvloed door de keuze van die ander. Dan moet je vooruit-denken:
>
> 1. *"Wat doet hij waarschijnlijk?"*
> 2. *"Wat is mijn beste antwoord daarop?"*
> 3. *"Wist hij dát ik dat zou denken?"*
>
> Speltheorie geeft een **systematische methode** (matrix → best response → Nash) om dit redeneerproces te ordenen, zodat je niet vastloopt in een "ja maar wat als…"-spiraal.

> [!CAUTION]
> **Examenvalkuil:** Speltheorie is **rationeel**, maar examenvragen testen vaak het **gat met de praktijk** (rechtvaardigheidsgevoel, vertrouwen, sociale norm). Zie je in de casus woorden als *"in de praktijk"*, *"echte mensen"*, *"sociale norm"* — wijk dan af van de pure rationele uitkomst.

---

### De 3 dimensies van een spel

| Dimensie | Type A | Type B |
|---|---|---|
| **Tijd** | **Simultaan** — spelers beslissen tegelijk | **Sequentieel** — speler 1 kiest eerst, speler 2 reageert |
| **Herhaling** | **Eenmalig** — één ronde | **Herhaald** — acties in vorige rondes beïnvloeden strategie |
| **Samenwerking** | **Coöperatief** — spelers stemmen strategieën af | **Niet-coöperatief** — iedereen kiest voor eigen belang |

> **Ezelsbruggetje:** *"Tegelijk of om de beurt?"* · *"Eén keer of vaker?"* · *"Samen of solo?"*

```mermaid
flowchart TD
    Tijd{{"⏱️ Tijd?"}}
    Tijd -->|"Tegelijk"| Sim(["Simultaan spel"])
    Tijd -->|"Om de beurt"| Seq(["Sequentieel spel"])
    Sim --> Mat["📊 Opbrengsten-MATRIX<br/>+ best response → Nash"]
    Seq --> Boom["🌳 SPEL-BOOM<br/>+ backwards induction"]

    Herh{{"🔁 Hoe vaak?"}}
    Herh -->|"Eén keer"| Een(["Eenmalig"])
    Herh -->|"Vaker"| Rep(["Herhaald"])
    Een --> Eig["💼 Eigen belang wint<br/>klassiek GD"]
    Rep --> Soc["🤝 Reputatie + sociale<br/>norm tellen mee"]

    Sam{{"🤝 Samen mogelijk?"}}
    Sam -->|"Ja"| Coop(["Coöperatief"])
    Sam -->|"Nee"| Niet(["Niet-coöperatief"])
    Coop --> Con["📜 Contract / CAO /<br/>EU-verdrag"]
    Niet --> Kar["⚖️ Kartelverbod<br/>→ ieder voor zich"]

    classDef vraag fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f
    classDef proces fill:#e0e7ff,stroke:#4338ca,stroke-width:2px,color:#1e1b4b
    classDef overheid fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87

    class Tijd,Herh,Sam vraag
    class Sim,Seq,Een,Rep,Coop,Niet proces
    class Mat,Boom,Eig,Soc,Con,Kar overheid
```

> [!IMPORTANT]
> **Begrijp de Logica — Waarom maakt elke dimensie uit?**
>
> Elke dimensie bepaalt **welk model je mag gebruiken** en **welke uitkomst rationeel is**.
>
> **Voorbeeldketens uit recente examens:**
> - *Twee aannemers met aanbesteding* (24-2-25) → **sequentieel + eenmalig** → ultimatumspel.
> - *Twee energiebedrijven over CO₂-rechten* (25-1-16) → **simultaan + eenmalig** → matrix + Nash.
> - *Twee aannemers vaker samen* (24-2-26) → **herhaald** → reputatie telt → bod gaat omhoog.

> [!CAUTION]
> **Examenvalkuil:** Bij **herhaald** spel is "altijd verraden" niet meer dominant — je verliest reputatie en wordt in toekomstige rondes gestraft. Lees dus altijd of het spel "nog vaker" plaatsvindt.

---

### Opbrengstenmatrix (pay-off matrix)

**[Invalshoek: 🏭 De Producent]**

- **Opbrengstenmatrix** = tabel met de uitkomsten van een spel per combinatie van strategieën.
- **Rijspeler** links (getal vóór de komma), **kolomspeler** boven (getal ná de komma).
- Notatie: $(\text{uitkomst speler 1}\,;\, \text{uitkomst speler 2})$.

**Voorbeeld — Bibi (rij) vs. Stefan (kolom) — wel/geen trouwfoto's** (€):

$$
\begin{array}{c|cc}
 & \textbf{Stefan: Wel} & \textbf{Stefan: Geen} \\
\hline
\textbf{Bibi: Wel}  & (-1.000\,;\, 0)     & (2.000\,;\, -500) \\
\textbf{Bibi: Geen} & (\phantom{-}1.000\,;\, 3.000) & (\phantom{-}0\,;\, 0) \\
\end{array}
$$

> [!IMPORTANT]
> **Begrijp de Logica — De matrix is gewoon "alle mogelijke werelden"**
>
> Elk vakje is één scenario "als ík X kies en hij Y, dan…". De matrix dwingt je om **eerst álle scenario's uit te schrijven**, zodat je niet één optie vergeet. Pas daarna ga je kiezen.
>
> **Lees-truc voor de notatie $(a\,;\,b)$:**
> - $a$ = winst voor de **rij**speler (links) — vinger op het rij-label, kijk in dezelfde rij.
> - $b$ = winst voor de **kolom**speler (boven) — vinger op het kolom-label, kijk in dezelfde kolom.

> [!CAUTION]
> **Examenvalkuil:** Studenten halen vóór en ná de komma door elkaar. Schrijf bovenaan je examenblad: *"vóór = rij, ná = kolom"*.

---

### Best response-methode → Nash-evenwicht

**Stappenplan (examenmethode):**

1. **Rijspeler** bekijkt per kolom wat zijn beste uitkomst is → arceer dat getal vóór de komma.
2. **Kolomspeler** bekijkt per rij zijn beste uitkomst → arceer dat getal na de komma.
3. Vakje met **beide** getallen gearceerd = **Nash-evenwicht**.

> **Nash-evenwicht** = een combinatie van strategieën waarbij geen enkele speler een reden heeft om van strategie te veranderen, gegeven de strategie van de ander.

Toegepast op het Bibi/Stefan-voorbeeld → Nash = $(\text{Bibi: Geen}\,;\, \text{Stefan: Wel}) = (1.000\,;\, 3.000)$.

```mermaid
flowchart TD
    Start(["Spelers kiezen<br/>strategie (X, Y)"])
    Vraag{{"Kan iemand ALLÉÉN<br/>verbeteren door te wisselen?"}}
    Wissel(["Wissel naar betere strategie"])
    Geen[/"❌ Geen Nash"/]
    Nash[["✅ NASH-EVENWICHT<br/>niemand wisselt eenzijdig"]]

    Start --> Vraag
    Vraag -->|"Ja"| Geen
    Geen --> Wissel
    Wissel --> Start
    Vraag -->|"Nee, beide vast"| Nash

    classDef proces fill:#e0e7ff,stroke:#4338ca,stroke-width:2px,color:#1e1b4b
    classDef vraag fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class Start,Wissel proces
    class Vraag vraag
    class Geen fout
    class Nash goed
```

> [!IMPORTANT]
> **Begrijp de Logica — Waarom is Nash een "evenwicht"?**
>
> Een evenwicht in de natuurkunde = een bal die in een dal ligt. Tikt iemand er tegen → hij rolt terug. Een Nash-evenwicht is hetzelfde, maar dan met strategieën:
>
> 1. Stel: jij weet wat de ander doet.
> 2. Kun jij door **eenzijdig** te wisselen méér winst halen? → **NEE** = Nash.
> 3. Kun jij wél méér halen door te wisselen? → **GEEN** Nash, je rolt door naar een betere strategie.
>
> **Belangrijk:** Nash zegt NIETS over of de uitkomst goed is voor de groep. Het kan een **slecht** evenwicht zijn (zie gevangenendilemma) — toch blijft niemand spontaan wisselen, want je verslechtert je eigen positie.

> [!CAUTION]
> **Examenvalkuil:**
> - Een matrix kan **0, 1 of meerdere** Nash-evenwichten hebben — niet automatisch één.
> - Nash ≠ "beste" uitkomst. Het is de **stabiele** uitkomst.
> - Heb je géén dominante strategie? Doe dan stug de best-response-methode — die werkt altijd.

---

### Gevangenendilemma (prisoners' dilemma)

**[Invalshoek: 🏛️ De Markt / Overheid]**

Een **gevangenendilemma** is een spel waarbij het evenwicht voor **beide spelers niet optimaal** is.

**De 7 voorwaarden (uit je hoofd kennen):**

1. Beslissen tegelijkertijd.
2. Beslissingen zijn onafhankelijk, maar uitkomst hangt af van elkaar.
3. Eenmalige beslissing.
4. Beide spelers hebben dezelfde informatie.
5. Iedereen kiest voor eigen belang.
6. Slechts twee alternatieven per speler.
7. Geen overleg mogelijk.

**Standaardmatrix — Jesse vs. Finn (jaren cel):**

$$
\begin{array}{c|cc}
 & \textbf{Finn: Bekennen} & \textbf{Finn: Niet bekennen} \\
\hline
\textbf{Jesse: Bekennen}      & (3\,;\, 3)        & (0\,;\, 5) \\
\textbf{Jesse: Niet bekennen} & (5\,;\, 0)        & (1\,;\, 1) \\
\end{array}
$$

*Toelichting:* "0" = vrijuit (geen cel), uitkomsten in **jaren cel** dus **lager is beter**.

```mermaid
flowchart TD
    GD{{"🔒 GEVANGENEN-<br/>DILEMMA"}}
    Ind(["Individueel belang<br/>= Bekennen<br/>dominante strategie"])
    Col(["Collectief belang<br/>= Beide NIET bekennen<br/>optimaal: 1 + 1 jaar"])
    Uit[/"Uitkomst Nash:<br/>Beide bekennen<br/>→ 3 + 3 jaar cel"/]
    Sam[/"Vereist samenwerking<br/>+ vertrouwen<br/>contract / herhaling"/]

    GD --> Ind --> Uit
    GD --> Col --> Sam
    Uit -. "niet-optimaal<br/>evenwicht" .-> Sam

    classDef term fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87
    classDef proces fill:#e0e7ff,stroke:#4338ca,stroke-width:2px,color:#1e1b4b
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class GD term
    class Ind,Col proces
    class Uit fout
    class Sam goed
```

> [!IMPORTANT]
> **Begrijp de Logica — Waarom is dit een "dilemma"?**
>
> Het is een dilemma omdat **rationeel goed voor jou** = **slecht voor jullie samen**. Loop het denkproces van Jesse stap-voor-stap mee:
>
> 1. *"Stel Finn bekent."* → Bekennen (3 jaar) is beter dan niet bekennen (5 jaar). Dus: **bekennen**.
> 2. *"Stel Finn bekent niet."* → Bekennen (vrij) is beter dan niet bekennen (1 jaar). Dus: **bekennen**.
> 3. **Conclusie:** Wat Finn ook doet, Jesse zit beter af met bekennen → **dominante strategie**.
> 4. Finn doet exact dezelfde redenering → ook bekennen.
> 5. Resultaat: $(3\,;\,3)$, terwijl ze samen $(1\,;\,1)$ hadden kunnen halen → **2 jaar verspild per persoon**.
>
> **Het mechanisme:** wantrouwen + onafhankelijke keuze + eigen belang = Pareto-slecht evenwicht. Daarom heeft de samenleving instituten **uitgevonden** om eruit te breken.

#### Hoe doorbreek je een gevangenendilemma? 🎯

| Mechanisme | Welke voorwaarde wordt opgeheven? | Voorbeeld |
|---|---|---|
| **Contract / kartel** | Voorwaarde 7 (geen overleg) → wel overleg + boete | OPEC-quota, prijsafspraken (in NL verboden) |
| **Herhaling** | Voorwaarde 3 (eenmalig) → reputatie ontstaat | Vaste leveranciers, langetermijn-CAO |
| **Wetgeving / overheid** | Voorwaarde 5 (eigen belang) → wettelijk verplicht het collectieve | Milieuwet, kartelverbod, belasting |
| **Sociale norm** | Voorwaarde 5 → schaamte/eer als straf | "Goede buur" zijn, eerlijk delen |
| **Zelfbinding** | Voorwaarde 2 → keuze onomkeerbaar maken | Groen-certificaat, openbaar beloven |

> [!CAUTION]
> **Examenvalkuil:** Studenten roepen te snel "gevangenendilemma!". Check **alle 7** voorwaarden. Mist er één (bv. herhaald spel, of overleg toegestaan) → géén GD, maar gewone Nash-analyse.

---

### Dominante strategie vs. individueel/collectief belang

| Begrip | Definitie | Voorbeeld |
|---|---|---|
| **Dominante strategie** | Speler kiest altijd dezelfde strategie, ongeacht de ander | "Bekennen" in gevangenendilemma |
| **Individueel belang** | Uitkomst die voor hém het gunstigst is | Supermarkt: prijs verlagen |
| **Collectief belang** | Hoogste gezamenlijke opbrengst | Beide: prijzen gelijk houden |

> [!IMPORTANT]
> **Begrijp de Logica — Dominante strategie ≠ Nash-evenwicht!**
>
> - **Dominante strategie** = persoonlijk; één speler heeft één keuze die altijd het beste is.
> - **Nash-evenwicht** = de hele matrix; combinatie van keuzes waarbij niemand wil wisselen.
>
> **Verband:**
> - Hebben **beide** spelers een dominante strategie → de combinatie is automatisch een Nash-evenwicht.
> - Heeft **niemand** een dominante strategie → er kan nog steeds Nash zijn, maar je moet best response gebruiken.

> [!TIP]
> 🔁 **Verbinding:** bij prijzenoorlog (§1.2) zie je vaak dat *"meedoen aan prijsoorlog"* voor beide bedrijven dominant is → klassiek GD.

---

## 1.2 Strategie in een prijzenoorlog

### Nul-som vs. niet-nul-som

| Type spel | Kenmerk | Voorbeeld |
|---|---|---|
| **Nul-som-spel** | Uitkomst heeft constante waarde; wat de één wint, verliest de ander | Schaken, poker |
| **Niet-nul-som-spel** | Beide kunnen winnen óf beide verliezen | Gevangenendilemma, prijzenoorlog |

> [!IMPORTANT]
> **Begrijp de Logica — Waarom is dit onderscheid zó belangrijk?**
>
> Bij een **nul-som-spel** is de taart vast: jouw plus = mijn min. Samenwerken heeft geen zin. → Pure concurrentie is logisch.
>
> Bij een **niet-nul-som-spel** kan de taart **groter of kleiner** worden afhankelijk van wat we samen doen. Daarom loont het om te onderhandelen, contracten te sluiten of normen te volgen — anders blijven we allebei in de "kleine taart"-uitkomst hangen.

> [!TIP]
> **Examen-trick:** Als de som van de uitkomsten in elk vakje **anders** is, is het géén nul-som. Het meeste in economie (oligopolie, milieu, EU) = niet-nul-som.

---

### Prijzenoorlog

**[Invalshoek: 🏭 De Producent]**

**Prijzenoorlog** = situatie waarin concurrenten elkaar bestrijden met prijsverlagingen om marktaandeel te vergroten of concurrenten uit de markt te drukken.

- **Redenen:** omzet vergroten, marktaandeel pakken, concurrent uitschakelen.
- **Risico's voor producenten:** lagere winstmarge, lange verliesperiode, kwaliteitsverlies.
- **Risico's voor consumenten:** op korte termijn goedkoop, op lange termijn prijsverhoging + kwaliteitsverlies.
- **Plaats:** vooral in **oligopolies** (telecom, supermarkten, tankstations, zorgverzekeraars).

```mermaid
flowchart TD
    A(["Bedrijf A verlaagt prijs"]) --> B(["Marktaandeel A groeit tijdelijk"])
    B --> C(["Bedrijf B reageert: óók verlagen"])
    C --> D[/"Neerwaartse prijsspiraal"/]
    D --> Q{{"Wie houdt vol?"}}
    Q -->|"Zwakste valt om"| F[["Overblijver = winnaar<br/>prijzen stijgen weer"]]
    Q -->|"Beide overleven"| G[["Verlies voor allen<br/>klassiek GD-resultaat"]]

    classDef proces fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    classDef vraag fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class A,B,C proces
    class D fout
    class Q vraag
    class F goed
    class G fout
```

**Voorbeeld — Restaurants T en S** (€ winst):

$$
\begin{array}{c|cc}
 & \textbf{S: Meedoen} & \textbf{S: Niet meedoen} \\
\hline
\textbf{T: Meedoen}      & (1.425\,;\, 1.920) & (1.995\,;\, 1.200) \\
\textbf{T: Niet meedoen} & (\phantom{1.}996\,;\, 2.400) & (1.660\,;\, 2.100) \\
\end{array}
$$

→ Dominante strategie voor beide = meedoen. Collectief optimum = beide niet meedoen → **gevangenendilemma in de praktijk**.

> [!IMPORTANT]
> **Begrijp de Logica — Waarom ontstaan prijzenoorlogen vooral in oligopolies?**
>
> Een oligopolie heeft **weinig** spelers met **homogene** producten (benzine, telecom, supermarkten). Drie effecten versterken elkaar:
>
> 1. **Zichtbaarheid:** je ziet de prijs van je concurrent dagelijks (bordje pomp, folder Albert Heijn).
> 2. **Snelle substitutie:** consumenten wisselen makkelijk → kleine prijsverschillen = grote verschuiving in marktaandeel.
> 3. **Wederkerigheid:** verlaag jij, dan verliest de buur klanten → die móét reageren → spiraal.
>
> Bij **heterogene producten** (kleding, restaurants, auto's) is dit veel minder, omdat klanten ook om kwaliteit/merk geven → prijsoorlog werkt slechter.

```mermaid
flowchart TD
    OL{{"Oligopolie<br/>+ homogeen product"}}
    OL --> Z(["Prijzen zichtbaar<br/>pomp, folder"])
    OL --> S(["Snelle substitutie<br/>klant wisselt 1×"])
    Z --> SP[/"Iedereen verlaagt"/]
    S --> SP
    SP --> V[["Lagere winst voor allemaal<br/>= Nash, maar GD-uitkomst"]]

    classDef term fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    classDef proces fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d

    class OL term
    class Z,S proces
    class SP,V fout
```

> [!CAUTION]
> **Examenvalkuil:** Prijzenoorlog (= concurreren via prijsverlaging) **mag** in Nederland; **prijsafspraken** (kartelvorming) zijn juist **verboden** door de Mededingingswet (ACM controleert). Verwar deze twee nooit.

> [!TIP]
> 🔁 **Verbinding:** dit is een levensecht voorbeeld van de gevangenendilemma-logica uit §1.1 — daarom werkt de overheid via wetgeving in plaats van te hopen op vrijwillige samenwerking.

---

## 1.3 Onderhandelen en samenwerken

### Sequentieel spel → andere uitkomst

**[Invalshoek: 👤 De Consument & 🏭 Producent]**

Bij een **sequentieel spel** volgen beslissingen elkaar op. De latere speler heeft meer informatie; de "beste" keuze kan daardoor veranderen.

> [!IMPORTANT]
> **Begrijp de Logica — Wie als eerste mag, kan het spel "sturen"**
>
> Bij simultaan beslissen weet je niet wat de ander doet → je kiest voorzichtig. Bij sequentieel weet **speler 2** wel wat speler 1 deed → speler 2 kiest perfect. Maar: speler 1 weet dat speler 2 dat gaat doen, en speelt dus de zet die speler 2 dwingt tot de uitkomst die ík (speler 1) wil.
>
> Dit heet **first-mover-voordeel**: door als eerste een onomkeerbare zet te doen, beperk je de keuzes van de tegenstander.

---

### Ultimatumspel

- **Ultimatumspel** = sequentieel spel met één beslisser (speler 1) die een voorstel doet, speler 2 accepteert of wijst af.
- Bij afwijzing: **beiden** krijgen niets.
- Puur rationeel: speler 2 accepteert elk voorstel $> 0$.
- In de praktijk: rechtvaardigheidsgevoel telt; bevredigende verdeling ligt rond **€ 30 / € 70**.

> [!IMPORTANT]
> **Begrijp de Logica — Theorie vs. praktijk in één spel**
>
> | Visie | Wat doet speler 2 bij voorstel "€ 1 voor jou, € 99 voor mij"? | Waarom? |
> |---|---|---|
> | **Pure rationaliteit** | Accepteren | € 1 > € 0 |
> | **Echte mensen** | Weigeren (vaak) | "Liever niets dan een onrechtvaardig voorstel" |
>
> Speler 1 weet dit en biedt daarom in de praktijk **€ 30–€ 50**, niet € 1. De *anticipatie op woede* dwingt een eerlijker verdeling af.

> [!CAUTION]
> **Examenvalkuil:** Veel studenten geven alleen de "puur rationele" uitkomst. Lees of de vraag vraagt om de *theoretische* uitkomst óf wat in *de praktijk* gebeurt — dat scheelt 1-2 punten.

---

### Spelboom & Backwards induction

- **Spelboom** = visualisatie van een sequentieel spel, uitkomst $(\text{speler 1}\,;\,\text{speler 2})$.
- **Backwards induction**: werk terug vanaf de laatste beslissing en kies per knoop de beste optie voor de betreffende speler.

**Voorbeeld — Unilever (eerst) vs. Nestlé (daarna) — wel/niet biologisch** (€ mld winst):

```mermaid
flowchart LR
    U(((Unilever)))
    N1(((Nestlé)))
    N2(((Nestlé)))
    R1["(4,5 ; 4,5)"]
    R2["(6 ; 5,5) ⭐"]
    R3["(5,5 ; 6) ⭐"]
    R4["(5 ; 5)"]

    U -->|"ja"| N1
    U -->|"nee"| N2
    N1 -->|"ja"| R1
    N1 -->|"nee"| R2
    N2 -->|"ja"| R3
    N2 -->|"nee"| R4

    classDef speler1 fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef speler2 fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    classDef gekozen fill:#fef3c7,stroke:#d97706,stroke-width:3px,color:#78350f
    classDef niet fill:#f1f5f9,stroke:#94a3b8,stroke-width:1px,color:#475569

    class U speler1
    class N1,N2 speler2
    class R2,R3 gekozen
    class R1,R4 niet
```

**Stappen:**

- Als Unilever "ja" → Nestlé kiest "nee" → $(6\,;\,5{,}5)$.
- Als Unilever "nee" → Nestlé kiest "ja" → $(5{,}5\,;\,6)$.
- Unilever kiest wat hém het meeste oplevert: $6 > 5{,}5$ → **"ja"** → evenwicht = $(6\,;\,5{,}5)$.

> [!IMPORTANT]
> **Begrijp de Logica — Backwards induction in 3 stappen**
>
> Werk **van rechts naar links** door de boom:
>
> 1. **Begin bij de eindknopen** (de laatste speler die kiest). Markeer per knoop welke tak híj zou kiezen → noteer het uitkomst-paar.
> 2. **Knip de niet-gekozen takken weg** (denkbeeldig). Nu is er per pad één voorspelbare uitkomst.
> 3. **Ga één stap terug** naar de vorige beslisser en kies daar de tak met de hoogste eigen uitkomst.
> 4. Herhaal tot je bij de eerste speler bent → dat pad = **deelspel-perfect Nash-evenwicht**.

> [!TIP]
> **Examen-trick:** maak op je examen **altijd** eerst de boom en zet ⭐ bij de takken die de speler kiest. Heel visueel scoort beter dan tekstueel beredeneren.

> [!CAUTION]
> **Examenvalkuil:** Studenten redeneren vaak "voorwaarts". De examenmethode is **achterwaarts**. Pas als je weet wat de **laatste** speler doet, kan de **eerste** speler rationeel kiezen.

---

### Onderhandelen, contracten, zelfbinding

**[Invalshoek: 🏛️ De Markt / Overheid]**

| Instrument | Definitie | Functie |
|---|---|---|
| **Onderhandelen** | Overleg tot een acceptabele afspraak | Collectief > eigen belang |
| **Contract** | Document met schriftelijke afspraken + handtekening | Doorbreekt gevangenendilemma; boete bij verbreken |
| **Sociale normen** | Ongeschreven regels; werkt via reputatie | Alternatief voor contract (vooral bij herhaald spel) |
| **Zelfbinding** | Eenzijdig een keuze **geloofwaardig onomkeerbaar** maken | Bewijs van betrouwbaarheid |

**Zelfbinding — voorbeelden:** milieucertificaat, groen energiecontract, publieke CO₂-belofte.

```mermaid
flowchart LR
    A(["Bedrijf belooft<br/>'wij doen X'"])
    B[/"❌ Niemand gelooft het"/]
    C{{"+ Zelfbinding<br/>certificaat, investering,<br/>contract met boete"}}
    D(["Onomkeerbaar"])
    E(["Geloofwaardig ✅"])
    F[["Klant/partner past<br/>gedrag aan → win-win"]]

    A -->|"geen bewijs"| B
    A --> C
    C --> D --> E --> F

    classDef proces fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    classDef term fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class A,D,E proces
    class C term
    class B fout
    class F goed
```

> [!IMPORTANT]
> **Begrijp de Logica — Waarom werkt zelfbinding?**
>
> Klinkt paradoxaal: je beperkt **vrijwillig** je eigen vrijheid. Toch is dit slim, omdat het je **geloofwaardig** maakt voor de tegenpartij.
>
> *Voorbeeld:* een bedrijf belooft "wij gaan groen produceren". Niemand gelooft het, want er is geen straf bij liegen. Maar als het bedrijf publiekelijk een **certificaat** koopt + boete-clausule tekent + investeert in zonnepanelen → die zet is onomkeerbaar. Nu is de belofte geloofwaardig.

> [!TIP]
> 🔁 **Verbinding:** zelfbinding doorbreekt de "geen overleg"-voorwaarde van het GD (§1.1) — je geeft eenzijdig signaal i.p.v. te onderhandelen.

---

### Verzonken kosten (sunk costs)

- **Verzonken kosten** = kosten die al gemaakt zijn voor een samenwerking en niet terugkeren wanneer de samenwerking niet doorgaat (bv. marktonderzoek, ontwikkelingskosten).
- **Economisch rationeel** = kijk vooruit, niet achteruit. Verzonken kosten horen **géén rol** te spelen in toekomstige beslissingen (sunk cost fallacy).

> [!IMPORTANT]
> **Begrijp de Logica — De "kapotte bioscoopkaartje"-test**
>
> Stel: je hebt € 12 betaald voor een filmkaartje. Halverwege merk je: de film is verschrikkelijk. Wat is rationeel?
>
> - **Fout:** *"Ik blijf zitten, anders is mijn € 12 weggegooid."* → Sunk cost fallacy. De € 12 ben je **sowieso** kwijt.
> - **Goed:** *"Vergeet de € 12. Levert nog 1 uur kijken meer plezier op dan iets anders gaan doen?"* → meestal: nee → **wegwezen**.
>
> **Toegepast op bedrijven:** een bedrijf heeft € 5 mln R&D in product gestopt. Markt blijkt te klein. → Beslissing baseren op **toekomstige** kosten en opbrengsten, NIET op die € 5 mln.

> [!CAUTION]
> **Examenvalkuil:** *"Maar ze hebben er al zoveel ingestoken!"* is een gevoels-argument, geen economisch argument. Markeer in casussen elke euro die al uitgegeven is als 🚫 → niet meenemen in toekomstige analyse.

---

## 1.4 Externe effecten & collectieve goederen

### Extern effect

**[Invalshoek: 🏛️ De Markt / Overheid]**

- **Extern effect** = effect dat **niet in de (kost)prijs** van een product zit. Een bijkomstig gevolg van productie of consumptie dat niet door de veroorzaker wordt betaald of aan de veroorzaker wordt vergoed.
- **Negatief extern effect**: schade voor derden (luchtvervuiling, geluidsoverlast, files).
- **Positief extern effect**: voordeel voor derden (imkers bij boomgaarden, onderwijs, vaccinatie).

```mermaid
flowchart TD
    PR(["Private prijs<br/>wat de markt rekent"])
    KEUS([Beslissing<br/>consument / producent])
    EX{{"Extern effect<br/>niet in de prijs"}}
    SUB[/"⚠️ Suboptimaal:<br/>te veel bij negatief<br/>te weinig bij positief"/]
    OV{{"🏛️ Overheid corrigeert"}}
    INT(["Internaliseren =<br/>extern effect IN de prijs"])
    OPT[["✅ Maatschappelijk optimum"]]

    PR --> KEUS --> SUB
    EX -. "wordt genegeerd" .-> KEUS

    OV -->|"belasting / subsidie / norm"| INT --> OPT
    SUB --> OV

    classDef proces fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef term fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b
    classDef overheid fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87

    class PR,KEUS,INT proces
    class EX term
    class SUB fout
    class OPT goed
    class OV overheid
```

> [!IMPORTANT]
> **Begrijp de Logica — Waarom faalt de markt hier?**
>
> De marktprijs is gebaseerd op **private kosten en opbrengsten**. Maar als productie ook **derden** raakt zonder dat die compensatie krijgt of betaalt, dan zit dat **niet** in de prijs.
>
> - **Negatief extern effect** → product is "te goedkoop" → **te veel** geproduceerd/geconsumeerd (bv. te veel diesel verkocht).
> - **Positief extern effect** → product is "te duur" → **te weinig** geproduceerd (bv. te weinig vaccinaties).

> [!CAUTION]
> **Examenvalkuil:** **Internaliseren** = het externe effect **in de prijs trekken** via belasting (negatief) of subsidie (positief). Veel vragen vragen letterlijk dit woord.

---

### Maatschappelijke kosten & opbrengsten

- **Maatschappelijke kosten** = private kosten + negatieve externe effecten.
- **Maatschappelijke opbrengsten** = private opbrengsten + positieve externe effecten.

| Begrip | Betekenis | Actie overheid |
|---|---|---|
| **Negatief extern effect** | Schade niet doorberekend | Belasting, boete, verbod, **collectieve dwang** |
| **Positief extern effect** | Voordeel niet beloond | Subsidie, voorlichting |

---

### Soorten goederen

| Goed | Rivaliserend? | Exclusief? (individueel afrekenbaar) | Voorbeeld |
|---|---|---|---|
| **Individueel goed** | Ja | Ja | Brood, kleding |
| **Collectief goed** | Nee | Nee | Dijken, defensie, openbare verlichting |
| **Quasi-collectief goed** | Gedeeltelijk | Gedeeltelijk (grotendeels overheid) | Onderwijs, zorg, openbaar vervoer |

- **Collectieve goederen** = goederen die de overheid voortbrengt omdat ze niet individueel afrekenbaar zijn en geen prijs bij de gebruiker in rekening kan worden gebracht.
- **Quasi-collectieve goederen** = lasten worden grotendeels door de overheid betaald, maar afname is wél individueel.

---

### Free-rider / meeliftgedrag

- **Meeliftgedrag (free-rider)** = mensen maken wél gebruik van iets, maar betalen er niet voor.
- Typerend voor collectieve goederen → daarom belasting als **collectieve dwang**.

> [!IMPORTANT]
> **Begrijp de Logica — Free-rider = gevangenendilemma met N spelers**
>
> Stel: een dorp wil een dijk bouwen. Iedereen heeft baat bij de dijk (niet-rivaliserend, niet-exclusief). Wat denkt elke inwoner?
>
> 1. *"Als ík niet meebetaal en de anderen wel, krijg ik de dijk gratis."* → Niet betalen.
> 2. *"Als ík wel meebetaal en de anderen niet, krijg ik niks en ben ik mijn geld kwijt."* → Niet betalen.
> 3. **Conclusie:** Voor elke inwoner is "niet betalen" dominant → **niemand** betaalt → **geen** dijk.
>
> Dit is de groepsversie van het gevangenendilemma. **Oplossing:** belasting = verplichte bijdrage = collectieve dwang.

> [!TIP]
> 🔁 **Verbinding:** dit is exact dezelfde logica als waarom **zorgverzekeringen verplicht zijn** (§2.1) — anders ontstaat averechtse selectie en valt het systeem om.

> [!CAUTION]
> **Examenvalkuil:** Een collectief goed herken je aan **twee** kenmerken samen: (1) niet-rivaliserend én (2) niet-exclusief. Mist één → géén collectief goed.

---

## 1.5 Samenwerking op de arbeidsmarkt & in de EU

### Arbeidsovereenkomst

**[Invalshoek: 🏭 De Producent / Werknemer]**

- **(Individuele) arbeidsovereenkomst** = overeenkomst tussen werkgever en werknemer waarin de arbeidsvoorwaarden worden vastgelegd.
- **Arbeidsvoorwaarden** = afspraken over de voorwaarden waaronder arbeid verricht wordt.

| Soort voorwaarden | Inhoud |
|---|---|
| **Primaire arbeidsvoorwaarden** | Loonhoogte & werktijden |
| **Secundaire arbeidsvoorwaarden** | Vakantiedagen, vakantietoeslag, pensioen, uitkering bij ziekte, opleiding |

---

### CAO & sociale partners

- **Vakbond** = vereniging die belangen van werknemers behartigt.
- **Werkgeversorganisatie** = vereniging die belangen van werkgevers behartigt.
- **CAO (collectieve arbeidsovereenkomst)** = afspraken over de arbeidsvoorwaarden in een bedrijfstak, gemaakt door vakbonden en werkgeversorganisaties.
- **Algemeen verbindend verklaren (AVV)** = cao-afspraken gelden voor alle werknemers in die bedrijfstak als de cao algemeen verbindend is verklaard door de minister van SZW.
- **Centraal Akkoord** = afspraken op landelijk niveau tussen vakcentrales, werkgeverscentrales en de regering.

```mermaid
flowchart TD
    V{{"👥 Vakbond<br/>werknemers"}}
    WG{{"🏭 Werkgevers-<br/>organisatie"}}
    CAO(["📜 CAO bedrijfstak<br/>geldt voor leden"])
    AVV[/"🏛️ Minister SZW:<br/>Algemeen Verbindend Verklaren"/]
    All[["✅ Geldt voor ALLE werknemers<br/>in de bedrijfstak<br/>(ook niet-aangesloten)"]]

    V <-->|"overleg"| WG
    V --> CAO
    WG --> CAO
    CAO --> AVV --> All

    classDef cons fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef prod fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    classDef proces fill:#e0e7ff,stroke:#4338ca,stroke-width:2px,color:#1e1b4b
    classDef overheid fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class V cons
    class WG prod
    class CAO proces
    class AVV overheid
    class All goed
```

> [!IMPORTANT]
> **Begrijp de Logica — Waarom een CAO en niet 1000 individuele contracten?**
>
> 1. **Onderhandelingsmacht (machtsbalans):** één werknemer tegenover een groot bedrijf staat zwak. Maar **alle** werknemers samen via een vakbond → bedrijf kan niet doordraaien zonder hun arbeid → onderhandeling is gelijker → betere voorwaarden.
> 2. **Transactiekosten:** 1000 keer dezelfde onderhandeling voeren is verspilling. Eén CAO voor de hele bedrijfstak = efficiënter.
>
> **Algemeen verbindend verklaren** breidt deze logica uit naar **alle** werknemers in de bedrijfstak. Dit voorkomt **prijzenoorlog op arbeidsvoorwaarden** ("ik betaal mijn personeel minder dan de buurman → ik kan goedkoper produceren") → race to the bottom.

> [!TIP]
> 🔁 **Verbinding:** dit is opnieuw een **GD-doorbreker** — zonder CAO zouden bedrijven elkaar onderbieden op loon.

---

### De Europese Unie (EU)

- **Europese Unie (EU)** = samenwerkingsverband van 27 landen in Europa (2021).
- Doel: vrede, stabiliteit, economische groei door samenwerking en vrij verkeer van goederen, diensten, personen en kapitaal.

**Kerngeschiedenis (tijdlijn):**

```mermaid
timeline
    title 🇪🇺 Oprichting & groei Europese samenwerking
    1951 : EGKS — Europese Gemeenschap voor Kolen en Staal
    1957 : Verdrag van Rome — EEG (gemeenschappelijke markt)
    1992 : Verdrag van Maastricht — EU & start EMU
    2002 : Invoering euro (€) als contant geld
    2007 : Verdrag van Lissabon — meer democratie, sterker EP
    2020 : Brexit — VK verlaat de EU
```

- **EGKS** = Europese Gemeenschap voor Kolen en Staal (1951): begin van de Europese samenwerking; landen controleren elkaars kolen- en staalindustrie om oorlog te voorkomen.
- **EMU (Economische en Monetaire Unie)** = samenwerking tussen EU-landen op economisch en monetair gebied; gezamenlijk gebruik van de euro en één monetair beleid (ECB).
- **Verdrag van Lissabon (2007)** = verdrag dat de werking van de EU hervormt.
- **Criteria van Kopenhagen** = voorwaarden waaraan een land moet voldoen om lid te mogen worden van de EU.
- **Brexit** = uittreden van het Verenigd Koninkrijk uit de EU (2020).

```mermaid
flowchart TD
    IL{{"27 individuele landen"}}
    GD[/"❌ GD: handelsoorlogen,<br/>devaluaties, subsidie-wedloop,<br/>race to the bottom"/]
    EU(["EU: gemeenschappelijke regels<br/>= contract met boete"])
    Inst[["🏛️ ECB · Hof van Justitie ·<br/>EMU + euro · vrije markt"]]
    WIN[["✅ Lagere transactiekosten,<br/>grotere markt, vrede"]]

    IL -->|"iedereen eigen belang"| GD
    IL -->|"verdragen"| EU
    EU --> Inst --> WIN

    classDef term fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87
    classDef proces fill:#e0e7ff,stroke:#4338ca,stroke-width:2px,color:#1e1b4b
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class IL term
    class EU,Inst proces
    class GD fout
    class WIN goed
```

> [!IMPORTANT]
> **Begrijp de Logica — De EU als gigantisch coöperatief spel**
>
> Stel je 27 landen voor die elk **eigen** beleid willen voeren (eigen valuta, eigen importheffingen, eigen subsidies). Wat gebeurt er rationeel?
>
> 1. Land A verlaagt belasting voor bedrijven → bedrijven verhuizen daarheen → land B voelt zich gedwongen óók te verlagen → **race to the bottom** (klassieke GD).
> 2. Land C zet importtarieven op buurland D → D doet hetzelfde terug → **handelsoorlog**.
>
> De EU is een **bundel verdragen** die deze prijsoorlogen verbieden:
> - **Vrij verkeer** → geen importheffingen tussen lidstaten.
> - **EMU + euro** → geen valuta-oorlogen meer.
> - **Mededingingsregels + staatssteunregels** → geen oneerlijke subsidiewedloop.
> - **Hof van Justitie** → onafhankelijke rechter handhaaft de regels.

> [!TIP]
> 🔁 **Verbinding:** precies dezelfde logica als CAO en kartelverbod — instituten zorgen dat het collectieve belang wint van het eigen belang.

> [!CAUTION]
> **Examenvalkuil:** "Brexit" wordt vaak gevraagd in context van de **kosten** van uittreden (verlies van vrije markt, douane-controles, hogere prijzen, juridische onzekerheid). Niet alleen "VK is uit EU".

---

## H1-OVERIG · Duurzaamheid & MVO

### Maatschappelijk Verantwoord Ondernemen (MVO)

- **MVO** = bedrijven streven ernaar naast winst (profit) ook rekening te houden met het effect van hun activiteiten op het gebied van milieu (planet) en menselijke aspecten (people) bij de besluitvorming.

### De 3 P's

| Pijler | Focus | Voorbeeld |
|---|---|---|
| **People** | Mens, arbeidsomstandigheden, mensenrechten | Eerlijke lonen, geen kinderarbeid |
| **Planet** | Milieu, klimaat | CO₂-reductie, biodiversiteit |
| **Profit** | Winst, continuïteit onderneming | Gezonde financiën |

### Lineaire vs. circulaire economie

| Model | Kenmerk |
|---|---|
| **Lineair** | Grondstof → product → afval ("take-make-waste") |
| **Circulair** | Producten en materialen worden hergebruikt; grondstoffen behouden zoveel mogelijk hun waarde |

> [!IMPORTANT]
> **Begrijp de Logica:** Een circulaire economie probeert negatieve externe effecten (uitputting, afval, CO₂) te internaliseren → betere uitkomst voor alle 3 P's samen.

---

# HOOFDSTUK 2 · RISICO & INFORMATIE

---

## 2.1 Risico nemen of vermijden

### Risico & verzekeren

**[Invalshoek: 👤 De Consument]**

| Begrip | Betekenis |
|---|---|
| **Vrijwillige risico's** | Risico's die je zelf kiest te nemen (bv. skiën, ondernemen) |
| **Onvrijwillige risico's** | Risico's waarvoor je niet zelf kiest (bv. brand, overstroming) |
| **Verzekeren** | Het tegen betaling van een premie overnemen van het financiële risico op schade van een verzekerde door een verzekeraar |
| **Premie** | Betaling van de verzekerde voor het verkrijgen van een verzekering |
| **Polis** | Contract dat dient als bewijs van een verzekering |
| **Risicoavers gedrag** | Het zo veel mogelijk vermijden van risico's |

---

### 🧮 Formule — Risico berekenen

$$
\boxed{\text{Risico} = \text{kans op een voorval} \times \text{gemiddeld schadebedrag}}
$$

**Voorbeeld (fiets):** kans op diefstal $\tfrac{1}{5}$ per jaar; fiets kost € 700.

$$
\text{Risico per jaar} = \tfrac{1}{5} \times € 700 = € 140
$$

Is een jaarpremie van bv. € 32,80 lager dan € 140? → rationeel om te verzekeren.

```mermaid
flowchart TD
    Start{{"Premie P  vs<br/>verwacht risico R = kans × schade"}}
    Lager(["P < R"])
    Hoger(["P > R"])
    Vraag{{"Kun je de schade zelf dragen?<br/>(eigen vermogen?)"}}
    GoA[["✅ VERZEKEREN<br/>wiskundig gunstig + zekerheid"]]
    GoB[["✅ VERZEKEREN<br/>risicoavers, betaalt voor zekerheid"]]
    Niet[/"❌ NIET verzekeren<br/>zelf-verzekeren"/]

    Start --> Lager --> GoA
    Start --> Hoger --> Vraag
    Vraag -->|"Nee, te groot"| GoB
    Vraag -->|"Ja, genoeg spaargeld"| Niet

    classDef vraag fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f
    classDef proces fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d

    class Start,Vraag vraag
    class Lager,Hoger proces
    class GoA,GoB goed
    class Niet fout
```

> [!IMPORTANT]
> **Begrijp de Logica — Wanneer is verzekeren rationeel?**
>
> Vergelijk altijd **drie** getallen:
>
> | Variabele | Wat? | Voorbeeld fiets |
> |---|---|---|
> | $R$ | Verwachte schade = kans × bedrag | € 140 |
> | $P$ | Jaarpremie | € 32,80 |
> | $EV$ | Eigen vermogen / draagkracht | € 200 spaargeld |
>
> **Beslisregel:**
> - $P < R$ → wiskundig gunstig om te verzekeren.
> - $P > R$ én schade > $EV$ → toch verzekeren (risicoaversie).
> - $P > R$ én schade $\leq EV$ → niet verzekeren (zelf-verzekeren).

> [!CAUTION]
> **Examenvalkuil:** $P > R$ betekent NIET automatisch "niet verzekeren". Een verzekeraar moet altijd $P > R$ rekenen, anders gaat hij failliet. Voor de **risico-averse** consument kan het toch rationeel zijn — die betaalt voor **zekerheid**.

---

### Verplichte verzekeringen & solidariteit

**[Invalshoek: 🏛️ De Markt / Overheid]**

| Verzekering | Waarom verplicht? |
|---|---|
| **Zorgverzekering (basispakket)** | Iedereen moet toegang hebben tot zorg; voorkomt averechtse selectie |
| **WA-autoverzekering** | Bescherming van derden bij schade door verkeersongeval |

- **Verplichte solidariteit** = zowel de goede als de slechte risico's moeten meebetalen aan de verzekering, waardoor de premie laag blijft.

---

### 🧮 Formule — Minimale gemiddelde premie

$$
\boxed{\text{minimale gemiddelde premie} = \dfrac{\text{totaal uitkeringsbedrag}}{\text{aantal verzekerden}}}
$$

**Voorbeeld — Zorgverzekering ZONDER verplichte solidariteit:**

- $500.000$ verzekerden, kans $\tfrac{1}{2}$, gemiddelde kosten € 2.700.
- Uitkering per jaar: $250.000 \times € 2.700 = € 675.000.000$.
- Minimale premie: $\dfrac{€ 675.000.000}{500.000} = € 1.350$.

**Voorbeeld — ZELFDE verzekeraar MET verplichte solidariteit:**

- Nu ook gezonden verplicht: $750.000$ verzekerden, kans $\tfrac{1}{2{,}5}$.
- Uitkering: $300.000 \times € 2.700 = € 810.000.000$.
- Minimale premie: $\dfrac{€ 810.000.000}{750.000} = € 1.080$.

→ Verplichte solidariteit drukt de gemiddelde premie met **€ 270**.

```mermaid
flowchart LR
    V(["VRIJWILLIG verzekeren:<br/>alleen zieken doen mee"])
    H[/"Hoog gemiddeld risico"/]
    HP[["❌ Hoge premie<br/>€ 1.350"]]
    P(["VERPLICHT verzekeren:<br/>iedereen doet mee"])
    L([Laag gemiddeld risico])
    LP[["✅ Lage premie<br/>€ 1.080"]]

    V --> H --> HP
    P --> L --> LP

    classDef proces fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef warn fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b
    classDef proc2 fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87

    class V proces
    class P proc2
    class H warn
    class L goed
    class HP warn
    class LP goed
```

> [!IMPORTANT]
> **Begrijp de Logica — Waarom werkt verplichte solidariteit?**
>
> 1. **Noemer groter** (meer verzekerden): vaste kosten worden over meer hoofden verdeeld.
> 2. **Kans daalt** (% mensen met schade): door gezonden mee te verplichten daalt het *gemiddelde* risico van de pool. Bij 500.000 mensen is 1 op 2 ziek (50%); bij 750.000 mensen is 1 op 2,5 ziek (40%).
> 3. **Effect:** zelfde verzekeraar, lagere premie voor iedereen — **omdat** de gezonden meebetalen.

> [!TIP]
> 🔁 **Verbinding:** dit is het exact tegenovergestelde mechanisme van **averechtse selectie** (§2.2). Zonder verplichting → spiraal omhoog. Met verplichting → spiraal doorbroken.

> [!CAUTION]
> **Examenvalkuil:** Veel studenten denken dat solidariteit "zielig" of "links" is. Economisch is het puur wiskunde: grotere pool met lager gemiddeld risico = lagere premie voor iedereen.

---

#### Omslagstelsel vs. kapitaaldekkingsstelsel

| Kenmerk | **Omslagstelsel** | **Kapitaaldekkingsstelsel** |
|---|---|---|
| **Wie betaalt?** | Werkenden NU betalen voor uitkeringen NU | Iedere verzekerde spaart voor zichzelf |
| **Voorbeeld** | AOW, WW, WIA, Zorgverzekeringswet | Aanvullend pensioen, levensverzekering |
| **Risico** | Vergrijzing → minder werkenden, meer ouderen | Beleggingsrisico (slechte beurs = minder pensioen) |
| **Solidariteit** | Hoog (intergenerationeel) | Laag (ieder z'n eigen pot) |

> [!IMPORTANT]
> **Begrijp de Logica:** een omslagstelsel = "doorgeefluik" — jouw premie verdwijnt direct naar iemand die nu een uitkering krijgt. Een kapitaaldekkingsstelsel = "spaarpot" — jouw premie wordt belegd en later aan jou uitgekeerd.

---

## 2.2 Verzekeren is niet eenvoudig

### Informatieasymmetrie

**[Invalshoek: 🏛️ De Markt]**

- **Asymmetrische informatie** = de verzekeraar en de verzekerde beschikken bij het afsluiten van een verzekering **niet over dezelfde informatie**. De verzekerde weet meer over zijn eigen risico dan de verzekeraar.

> [!IMPORTANT]
> **Begrijp de Logica — Wie weet meer en waarom is dat een probleem?**
>
> | Partij | Weet wél | Weet niet |
> |---|---|---|
> | **Verzekerde** | "Ik rook, fiets door rood, opa stierf jong aan hartaanval" | — |
> | **Verzekeraar** | Algemene statistieken (leeftijd, postcode) | Privé-gedrag, gezondheidsrisico, intentie |
>
> De verzekeraar moet één premie kiezen voor mensen waarvan hij het echte risico **niet ziet**. Die premie is per definitie een **gemiddelde**. Daaruit ontstaan **twee** klassieke marktproblemen: **averechtse selectie** (vóór contract) en **moral hazard** (ná contract).

---

### Averechtse selectie

- **Averechtse selectie** = het verschijnsel dat alleen mensen met een meer dan gemiddeld risico zich verzekeren.
- Gevolg: uitkeringen stijgen → premie omhoog → goede risico's haken af → premie stijgt verder → **spiraal** waarbij verzekering onbetaalbaar wordt.

```mermaid
flowchart TD
    A{{"❓ Verzekeraar kent risico niet<br/>asymmetrische info"}}
    B(["Eén gemiddelde premie"])
    C(["🔴 Slechte risico's:<br/>'lekker goedkoop!'<br/>→ verzekeren zich"])
    D(["🟢 Goede risico's:<br/>'te duur!'<br/>→ HAKEN AF"])
    E[/"Gemiddeld risico stijgt"/]
    F[/"Premie omhoog"/]

    A --> B
    B --> C
    B --> D
    D --> E
    E --> F
    F --> D

    classDef term fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87
    classDef proces fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class A term
    class B proces
    class C fout
    class D goed
    class E,F fout
```

> [!IMPORTANT]
> **Begrijp de Logica — De doodsspiraal in 5 stappen**
>
> 1. **Start:** verzekeraar zet één premie van € 1.000 voor "het gemiddelde risico".
> 2. **Zelfselectie:** wie weet dat hij hoog risico is, denkt: "lekker goedkoop!" → tekent. Wie weet dat hij laag risico is, denkt: "veel te duur!" → tekent NIET.
> 3. **Pool verschuift:** alleen hoge risico's blijven → uitkeringen stijgen.
> 4. **Premieverhoging:** verzekeraar moet wel naar € 1.300.
> 5. **Verdere uitstroom:** ook de "matige" risico's haken af → spiraal naar € 1.700, € 2.500, …
>
> **Eindresultaat:** de markt **stort in** — niemand wil nog verzekeren. Dit heet **marktfalen door asymmetrische informatie**.

> [!TIP]
> 🔁 **Verbinding:** precies daarom is de **basiszorgverzekering verplicht** (§2.1) en geldt **acceptatieplicht** (§2.3) — om de spiraal van tevoren te blokkeren.

> [!CAUTION]
> **Examenvalkuil:** Averechtse selectie ≠ "verzekeraar selecteert verkeerd". Het is de **verzekerde** die zichzelf selecteert. "Averechts" = tegen het belang van de verzekeraar in.

---

### Moral hazard (moreel wangedrag)

- **Moral hazard** = opzettelijk onvoorzichtig gedrag van een verzekerde, omdat de kosten van dit gedrag niet bij de verzekerde terechtkomen.
- *Voorbeelden:* fiets minder goed op slot, roekeloos rijden, onnodig naar dokter.

```mermaid
flowchart LR
    VZ(["VÓÓR verzekering<br/>kosten = 100% bij jou<br/>baten = 100% bij jou"])
    VG[["✅ Voorzichtig gedrag"]]
    NA(["NA verzekering<br/>kosten = 0% bij jou<br/>baten = 100% bij jou<br/>→ prikkel weg"])
    RG[/"⚠️ Risicovol gedrag<br/>= MORAL HAZARD"/]
    KOS[["Premies stijgen<br/>voor IEDEREEN"]]

    VZ --> VG
    NA --> RG --> KOS

    classDef proces fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d

    class VZ,NA proces
    class VG goed
    class RG fout
    class KOS fout
```

> [!IMPORTANT]
> **Begrijp de Logica — Waarom verandert gedrag NA het tekenen?**
>
> Vóór de verzekering: jij draagt 100% van de schade → je bent voorzichtig.
> Na de verzekering: verzekeraar draagt 100% → "de prikkel om voorzichtig te zijn" verdwijnt.
>
> Dit is geen kwade opzet, maar **rationeel** gedrag: de **marginale kosten** van risico-nemend gedrag zijn voor jou nul, terwijl de **marginale opbrengsten** (gemak, tijdwinst) bij jou blijven.

> [!TIP]
> **Verschil om te onthouden (examen-klassieker):**
>
> | Probleem | Wanneer? | Wat selecteert/verandert? |
> |---|---|---|
> | **Averechtse selectie** | **Vóór** contract | Wie sluit af (samenstelling pool) |
> | **Moral hazard** | **Ná** contract | Gedrag van de verzekerde |
>
> Truc: **A**S = **A**fsluiten (vóór), **M**H = **M**et name **na** afsluiten.

---

## 2.3 Financiële risico's beperken

Verzekeraars gebruiken **3 instrumenten** om averechtse selectie en moral hazard tegen te gaan:

```mermaid
flowchart TD
    Probl{{"⚠️ PROBLEEM<br/>asymmetrische info<br/>→ AS + MH"}}
    I1(["1️⃣ Eigen risico<br/>skin in the game<br/>→ tegen MH + signalling tegen AS"])
    I2(["2️⃣ Premiedifferentiatie<br/>+ bonus-malus<br/>→ tegen AS + MH"])
    I3(["3️⃣ Informatie inwinnen<br/>vragenlijst, CIS, schadevrije jaren<br/>→ uitzondering acceptatieplicht"])

    Probl --> I1
    Probl --> I2
    Probl --> I3

    classDef term fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef cons fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef prod fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    classDef overheid fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87

    class Probl term
    class I1 cons
    class I2 prod
    class I3 overheid
```

---

### 1. Eigen risico

**[Invalshoek: 👤 De Consument / Verzekeraar]**

- **Eigen risico** = het gedeelte van de schade dat door de verzekerde zelf moet worden betaald. De hoogte ligt vast in de polis.
- **Verplicht eigen risico** (zorgverzekering 2017): € 385 per jaar voor basiszorg ≥ 18 jaar.
- **Vrijwillig eigen risico**: kies je bovenop het verplichte deel in ruil voor lagere premie.

**Effecten:**

- Tegen **moral hazard**: je wordt voorzichtiger, want je betaalt zelf mee.
- Tegen **averechtse selectie**: keuze tussen hoog eigen risico + lage premie óf laag eigen risico + hoge premie → verzekeraar leert welk risicotype je bent (signalling).

```mermaid
flowchart LR
    ER{{"💶 Eigen risico € 385<br/>verplicht"}}
    MH[["✅ Tegen MORAL HAZARD<br/>denk 2× na bij claim"]]
    Vrij(["+ vrijwillig deel<br/>€ 885"])
    SIG(["SIGNALLING<br/>lage risico's kiezen<br/>hoog eigen risico"])
    AS[["✅ Tegen AVERECHTSE<br/>SELECTIE"]]

    ER --> MH
    ER --> Vrij --> SIG --> AS

    classDef cons fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class ER,Vrij,SIG cons
    class MH,AS goed
```

> [!IMPORTANT]
> **Begrijp de Logica — Eigen risico = "skin in the game"**
>
> Door een deel van de schade weer **bij de verzekerde** neer te leggen, herstel je de prikkel die door de verzekering was weggenomen:
>
> 1. **Moral hazard wordt geremd:** als jij € 385 zelf betaalt voor een bezoek, denk je twee keer na → minder onnodige zorg.
> 2. **Averechtse selectie wordt geremd via signalling:** kies jij vrijwillig € 885 eigen risico → jij geeft het signaal "ik denk dat ik weinig zorg nodig heb" → verzekeraar gelooft je → lagere premie.

> [!TIP]
> 🔁 **Verbinding:** solidariteit (§2.1) staat hier op gespannen voet met efficiëntie. Eigen risico = pijnlijk voor chronisch zieken die elk jaar het volle bedrag betalen.

> [!CAUTION]
> **Examenvalkuil:** Eigen risico werkt **alleen** preventief tegen moral hazard als de verzekerde **vooraf** weet dat hij gaat betalen én zijn gedrag kan aanpassen. Bij echt onverwachte schade (botsing, infarct) heeft eigen risico **geen** preventief effect — alleen kosten-besparend voor de verzekeraar.

---

### 2. Premiedifferentiatie & bonus-malus

- **Premiedifferentiatie** = een risicogroep met een meer dan gemiddeld risico moet daardoor een hogere premie betalen dan een risicogroep met een gemiddeld of laag risico.
- **Bonus-malusregeling** = verzekeringsvorm waarbij de premie afhankelijk is van het aantal schades dat je maakt.
- **No-claim korting** = korting op de premie als je een heel jaar geen schade claimt.

**Werking bonus-malusladder (auto):**

```mermaid
flowchart LR
    S{{"Start trede 2"}}
    Up(["⬆️ Trede +1<br/>meer korting<br/>(bonus)"])
    Dn(["⬇️ Treden omlaag<br/>minder korting<br/>(malus)"])

    S -->|"Jaar zonder schade"| Up
    S -->|"1 of meer schades"| Dn

    classDef start fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d

    class S start
    class Up goed
    class Dn fout
```

| Effect | Uitleg |
|---|---|
| Tegen **moral hazard** | Claimen kost je korting → je rijdt voorzichtiger / claimt alleen echte schade |
| Tegen **averechtse selectie** | Goede rijders betalen lagere premie → stoppen niet → blijven in de groep |

**Aandachtspunt:** bij zorgverzekering heeft bonus-malus voor de basisverzekering beperkt effect, want gezondheid is niet altijd beïnvloedbaar.

```mermaid
flowchart TD
    ZD(["❌ ZONDER differentiatie<br/>iedereen € 1.000"])
    AF[/"Goede risico's haken af<br/>= AVERECHTSE SELECTIE"/]
    MD(["✅ MÉT differentiatie<br/>premie per risicogroep"])
    ST([Goede risico's BLIJVEN<br/>betalen € 600])
    ST2[["✅ Pool stabiel"]]
    BO(["✅ BONUS-MALUS<br/>jaarlijks dynamisch"])
    CL(["Claim → premie ⬆<br/>geen claim → premie ⬇"])
    RG[["Verzekerde rijdt<br/>voorzichtiger (-MH)"]]

    ZD --> AF
    MD --> ST --> ST2
    BO --> CL --> RG

    classDef proces fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef fout fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class ZD fout
    class AF fout
    class MD,ST,BO,CL proces
    class ST2,RG goed
```

> [!IMPORTANT]
> **Begrijp de Logica — Premiedifferentiatie = informatie kopen via gedrag**
>
> De verzekeraar weet niet of jij een goed of slecht risico bent. Maar door de premie afhankelijk te maken van **observeerbare** kenmerken (leeftijd, postcode, schadeverleden) of **gedrag in de tijd** (claims), dwingt hij elke verzekerde om "zichzelf te identificeren":
>
> 1. **Tegen averechtse selectie:** goede risico's krijgen lagere premie → blijven in de pool.
> 2. **Tegen moral hazard:** elke claim verlaagt jouw bonus → jij claimt alleen écht nodig.

> [!CAUTION]
> **Examenvalkuil:** Premiedifferentiatie staat op spanning met **solidariteit**. Hoe specifieker je differentieert (bv. via DNA-test of AI), hoe minder solidariteit. De wetgever stelt daarom **grenzen** (geen DNA bij zorg, wel leeftijd bij autoverzekering).

---

### 3. Informatie inwinnen, acceptatieplicht & risicoselectie

- **Acceptatieplicht** = verzekeraars zijn wettelijk verplicht om iemand te accepteren voor een verzekering.
- **Risicoselectie** = verzekeraars weigeren slechte risico's of accepteren slechte risico's alleen tegen bepaalde voorwaarden zoals een hogere premie.

**Geldt wel / niet:**

- **Basiszorgverzekering**: acceptatieplicht geldt, risicoselectie **niet toegestaan**.
- **Aanvullende zorgverzekering** & **autoverzekering**: acceptatieplicht geldt **niet**, verzekeraar mag informatie vragen en risicoselectie toepassen.

**Informatiemiddelen verzekeraars:**

- Vragen naar schadevrije jaren van de vorige verzekeraar.
- Vragenlijsten (leeftijd, geslacht, gezondheid, justitieel verleden).
- **Stichting CIS**: centraal informatiesysteem waarin Nederlandse verzekeraars gegevens over misbruik en fraudegevallen delen.

```mermaid
flowchart LR
    BAS{{"🏥 BASISZORG<br/>maatschappelijk vitaal"}}
    AP(["✅ Acceptatieplicht +<br/>verbod op risicoselectie"])
    SOL[["HOGE solidariteit<br/>jong betaalt mee voor oud,<br/>gezond voor chronisch ziek"]]

    AAN{{"🚗 AANVULLEND / AUTO / REIS<br/>vrije markt"}}
    VRIJ(["⚖️ Verzekeraar MAG<br/>selecteren + differentiëren"])
    EFF[["HOGE efficiëntie,<br/>lagere solidariteit"]]

    BAS --> AP --> SOL
    AAN --> VRIJ --> EFF

    classDef overheid fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87
    classDef cons fill:#dbeafe,stroke:#2563eb,stroke-width:2px,color:#1e3a8a
    classDef prod fill:#dcfce7,stroke:#16a34a,stroke-width:2px,color:#14532d
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class BAS overheid
    class AP cons
    class SOL goed
    class AAN prod
    class VRIJ prod
    class EFF goed
```

> [!IMPORTANT]
> **Begrijp de Logica — Acceptatieplicht: solidariteit boven efficiëntie**
>
> Voor een **commerciële verzekeraar** is risicoselectie wiskundig optimaal: weiger de slechte risico's en je hebt een mooie pool. Maar maatschappelijk is dat onaanvaardbaar voor zorg — een chronisch zieke is dan onverzekerbaar.
>
> Daarom dwingt de overheid:
> - **Basiszorg:** acceptatieplicht → verzekeraar **moet** iedereen accepteren.
> - **Aanvullend / auto / reis:** vrije markt → verzekeraar mág selecteren en differentiëren.

> [!IMPORTANT]
> **Eindlogica H2 — De drie instrumenten samengevat**
>
> | Instrument | Pakt aan | Mechanisme |
> |---|---|---|
> | **Eigen risico** | Moral hazard (én iets AS) | Skin in the game; signalling |
> | **Premiedifferentiatie / bonus-malus** | AS én MH | Goede risico's blijven; gedrag wordt beloond |
> | **Informatie inwinnen / CIS** | AS én fraude | Verzekeraar verkleint informatieachterstand |
>
> Verzekeraars bestrijden informatieasymmetrie via deze drie. Tegelijk bewaakt de overheid een **ondergrens** (acceptatieplicht basiszorg, verplichte WA) zodat solidariteit niet wegvalt.

---

## H2-OVERIG · Rekenformules op een rij

| # | Formule | Betekenis |
|---|---|---|
| 1 | $\text{Risico} = \text{kans} \times \text{gemiddelde schade}$ | Verwachte schade per periode |
| 2 | $\text{minimale gemiddelde premie} = \dfrac{\text{totaal uitkeringsbedrag}}{\text{aantal verzekerden}}$ | Break-even premie verzekeraar |
| 3 | $\text{nieuw bedrag} = \text{oud bedrag} \times \dfrac{\text{nieuwe index}}{\text{oude index}}$ | Reële vergelijkingen via indexcijfer |

**Voorbeeld rekenvraag (havo-examen 2010)** — zorgpremie via indexcijfer:

Premie Delta Lloyd (index 106,5) = € 1.150. Gezocht: premie Unizorg (index 92,1).

$$
\text{Premie Unizorg} = € 1.150 \times \dfrac{92{,}1}{106{,}5} = € 994{,}51
$$

---

## Kernbegrippen — compleet overzicht

### H1 — Speltheorie & samenwerken

| Begrip | Korte definitie |
|---|---|
| **Speltheorie** | Studie van beslissingen waarbij je rekening houdt met de keuze van anderen |
| **Simultaan / Sequentieel spel** | Tegelijk vs. na elkaar beslissen |
| **Eenmalig / Herhaald spel** | Eén ronde vs. meerdere rondes |
| **Coöperatief / Niet-coöperatief spel** | Wel / geen afstemming van strategieën |
| **Opbrengstenmatrix** | Tabel met uitkomsten van een spel |
| **Best response-methode** | Arceringsmethode om Nash te vinden |
| **Nash-evenwicht** | Geen speler heeft reden om te veranderen |
| **Gevangenendilemma** | Evenwicht dat voor beiden niet optimaal is |
| **Dominante strategie** | Altijd dezelfde keuze, ongeacht ander |
| **Individueel / Collectief belang** | Eigen vs. gezamenlijk beste uitkomst |
| **Nul-som-spel** | Wat de één wint verliest de ander |
| **Niet-nul-som-spel** | Beide kunnen winnen of verliezen |
| **Prijzenoorlog** | Strijd tussen concurrenten via prijsverlagingen |
| **Oligopolie** | Markt met enkele grote aanbieders |
| **Ultimatumspel** | Sequentieel spel: voorstel – accepteren of afwijzen |
| **Spelboom** | Visualisatie sequentieel spel |
| **Backwards induction** | Terugredeneren vanaf laatste beslissing |
| **Contract** | Schriftelijke afspraak met boete bij breuk |
| **Sociale normen** | Ongeschreven gedragsregels |
| **Zelfbinding** | Eigen keuze geloofwaardig onomkeerbaar maken |
| **Verzonken kosten** | Kosten die bij niet-doorgaan niet terugkeren |

### H1 — Externe effecten, arbeid, EU, duurzaamheid

| Begrip | Korte definitie |
|---|---|
| **Extern effect** | Niet in prijs meeberekend gevolg van productie/consumptie |
| **Positief / negatief extern effect** | Voordeel / nadeel voor derden |
| **Maatschappelijke kosten / opbrengsten** | Private + externe effecten |
| **Collectieve goederen** | Niet-individueel afrekenbaar; door overheid geleverd |
| **Quasi-collectieve goederen** | Grotendeels overheid betaalt, wel individueel afneembaar |
| **Individuele / particuliere goederen** | Door markt geleverd, individueel verhandelbaar |
| **Meeliftgedrag (free-rider)** | Gebruiken zonder betalen |
| **Collectieve dwang** | Middelen (belasting, wet) om negatieve externe effecten te voorkomen |
| **(Individuele) arbeidsovereenkomst** | Afspraken werkgever – werknemer |
| **Arbeidsvoorwaarden** | Voorwaarden waaronder arbeid verricht wordt |
| **Primaire arbeidsvoorwaarden** | Loon & werktijden |
| **Secundaire arbeidsvoorwaarden** | Vakantie, pensioen, ziekte, opleiding |
| **CAO** | Afspraken per bedrijfstak door vakbonden & werkgeversorganisaties |
| **Algemeen verbindend verklaring** | Cao geldt voor alle werknemers in de bedrijfstak |
| **Centraal Akkoord** | Landelijke afspraken tussen centrales en regering |
| **Europese Unie (EU)** | Samenwerkingsverband 27 landen (2021) |
| **EGKS** | Europese Gemeenschap voor Kolen en Staal (1951) |
| **EMU** | Economische en Monetaire Unie – gezamenlijk monetair beleid & euro |
| **Verdrag van Lissabon** | Hervormingsverdrag EU (2007) |
| **Criteria van Kopenhagen** | Toetredingsvoorwaarden tot de EU |
| **Brexit** | Uittreden VK uit de EU |
| **MVO** | Winst + people + planet in beslissingen |
| **3 P's** | People, Planet, Profit |
| **Circulaire economie** | Producten en materialen worden hergebruikt en behouden waarde |

### H2 — Risico & informatie

| Begrip | Korte definitie |
|---|---|
| **Vrijwillige risico's** | Risico's die je zelf kiest te nemen |
| **Onvrijwillige risico's** | Risico's waarvoor je niet zelf kiest |
| **Verzekeren** | Tegen premie financieel risico overdragen aan verzekeraar |
| **Premie** | Betaling voor verkrijgen van verzekering |
| **Polis** | Contract als bewijs van verzekering |
| **Risicoavers gedrag** | Zo veel mogelijk vermijden van risico's |
| **Verplichte solidariteit** | Goede én slechte risico's samen → lagere premie |
| **Asymmetrische informatie** | Verzekeraar en verzekerde hebben niet dezelfde informatie |
| **Averechtse selectie** | Alleen mensen met meer dan gemiddeld risico verzekeren zich |
| **Moral hazard** | Onvoorzichtig gedrag omdat kosten niet bij verzekerde zelf liggen |
| **Eigen risico** | Deel van schade dat verzekerde zelf betaalt |
| **Premiedifferentiatie** | Verschillende premies per risicogroep |
| **Bonus-malusregeling** | Premie afhankelijk van aantal schadeclaims |
| **No-claim korting** | Korting bij een heel jaar zonder claim |
| **Acceptatieplicht** | Verzekeraar is wettelijk verplicht iemand te accepteren |
| **Risicoselectie** | Slechte risico's weigeren of alleen tegen strengere voorwaarden accepteren |

---

## Examentips — Checklist

1. **Best-response met arceringen** altijd expliciet uitvoeren op je examenblad.
2. **Check de 7 voorwaarden** voordat je iets een gevangenendilemma noemt.
3. **Sequentieel spel** → altijd spelboom + backwards induction.
4. **Verzonken kosten** spelen **geen** rol in toekomstige beslissingen (sunk cost fallacy).
5. **Extern effect** in een vraag? → controleer of het negatief/positief is en wie het betaalt (of juist niet).
6. **Collectief / quasi-collectief goed** herkennen aan: *niet rivaliserend* én *niet exclusief*.
7. **Risicoformule:** $R = \text{kans} \times \text{gem. schade}$ — pas altijd eerst toe voordat je verzekeren-advies geeft.
8. **Onderscheid averechtse selectie (vóór) vs. moral hazard (ná) afsluiten** – examenklassieker.
9. **Minimale premie-formule:** $\dfrac{\text{totale uitkering}}{\text{aantal verzekerden}}$.
10. **Eigen risico, premiedifferentiatie, informatie inwinnen** — weet per maatregel welk probleem (selectie of hazard) het aanpakt.
11. **Acceptatieplicht** geldt alleen bij **basis**zorgverzekering — aanvullend mag de verzekeraar selecteren.
12. **EU-samenwerking** snappen als herhaald coöperatief spel: verdragen = contracten die een gevangenendilemma tussen landen doorbreken.

---

## 🗺️ Visuele eindsamenvatting — De grote lijn van H1 + H2

### De rode draad in één zin

> [!IMPORTANT]
> **Markten falen** wanneer er **interactie** is tussen weinig spelers (speltheorie), wanneer effecten **buiten de prijs** vallen (externe effecten / collectieve goederen), of wanneer er **informatie ontbreekt** (asymmetrische info). De economie biedt **instituten** (contracten, wetten, CAO, verdragen, eigen risico, acceptatieplicht) om deze marktfalens te repareren.

### Mind map — verbanden tussen alle hoofdthema's

```mermaid
mindmap
  root(("🎯 Marktfalen<br/>+ oplossingen"))
    🎲 Speltheorie H1
      Simultaan
        Matrix + Nash
        Gevangenendilemma
        Dominante strategie
      Sequentieel
        Spelboom
        Backwards induction
        Ultimatumspel
      Doorbrekers GD
        Contract
        Sociale norm
        Zelfbinding
        Herhaling
    🌍 Externe effecten H1.4
      Negatief
        Belasting
        Verbod
      Positief
        Subsidie
      Collectieve goederen
        Free-rider
        Collectieve dwang
    🤝 Samenwerking H1.5
      Arbeidsmarkt
        CAO
        AVV
      EU
        EMU + euro
        Vrije markt
        Brexit
      MVO
        People Planet Profit
        Circulair
    🛡️ Risico H2.1
      Risico = kans × schade
      Solidariteit
      Omslag vs kapitaaldekking
    ❓ Asymmetrische info H2.2
      Averechtse selectie
      Moral hazard
    🔧 Oplossingen H2.3
      Eigen risico
      Premiedifferentiatie
      Bonus-malus
      Acceptatieplicht
      CIS
```

### Het terugkerende patroon: probleem → keten → oplossing

```mermaid
flowchart LR
    PROB{{"⚠️ MARKTFALEN<br/>• GD<br/>• extern effect<br/>• asymm. info"}}
    KET[/"🔄 NEGATIEVE KETEN<br/>• spiraal<br/>• race to bottom<br/>• te veel/te weinig"/]
    INST(["🏛️ INSTITUTIONELE OPLOSSING<br/>• wet<br/>• contract / CAO<br/>• verzekering<br/>• verdrag / belasting"])
    OPT[["✅ HERSTELD EVENWICHT<br/>maatschappelijk optimum"]]

    PROB --> KET --> INST --> OPT
    OPT -. "kan opnieuw falen<br/>bij verandering<br/>(techniek, vergrijzing, AI)" .-> PROB

    classDef warn fill:#fee2e2,stroke:#dc2626,stroke-width:2px,color:#7f1d1d
    classDef proces fill:#fef3c7,stroke:#d97706,stroke-width:2px,color:#78350f
    classDef overheid fill:#f3e8ff,stroke:#9333ea,stroke-width:2px,color:#581c87
    classDef goed fill:#d1fae5,stroke:#059669,stroke-width:2px,color:#064e3b

    class PROB warn
    class KET proces
    class INST overheid
    class OPT goed
```

### Welk probleem hoort bij welk hoofdstuk? (snel-zoek-tabel)

| Probleem in casus | Theoretische bril | Waar in samenvatting? |
|---|---|---|
| Twee bedrijven, simultaan, prijs- of productie-keuze | **Matrix + Nash + GD** | §1.1 |
| Bedrijven onderbieden elkaar, marges dalen | **Prijzenoorlog** | §1.2 |
| Eerst speler A, daarna speler B (overname-bod, aanbesteding) | **Spelboom + backwards induction** | §1.3 |
| Bedrijf belooft duurzaamheid, klant gelooft het niet | **Zelfbinding + contract** | §1.3 |
| *"We hebben er al zoveel ingestoken"* | **Verzonken kosten (negeer!)** | §1.3 |
| Vervuiling, geluidsoverlast, vaccinatie, onderwijs | **Extern effect → belasting/subsidie** | §1.4 |
| Dijken, defensie, openbare verlichting | **Collectief goed + free-rider** | §1.4 |
| Loonstrijd, vakbond, minimumloon | **CAO + AVV** | §1.5 |
| Importheffing, euro, Brexit | **EU + EMU** | §1.5 |
| Wel/niet verzekeren bij bekende kans + bedrag | **Risico = kans × schade** | §2.1 |
| Premie hoger als je in de hele groep kijkt | **Solidariteit + minimale premie** | §2.1 |
| AOW vs. aanvullend pensioen | **Omslag vs. kapitaaldekking** | §2.1 |
| Premie loopt op, gezonde mensen haken af | **Averechtse selectie** | §2.2 |
| Verzekerde wordt onvoorzichtiger | **Moral hazard** | §2.2 |
| Eigen risico € 385 | **Anti-moral-hazard + signalling** | §2.3 |
| No-claim, premie per leeftijdsgroep | **Premiedifferentiatie + bonus-malus** | §2.3 |
| *"Verzekeraar moet mij accepteren"* | **Acceptatieplicht (alleen basiszorg)** | §2.3 |

### Drie examen-truc-vragen om jezelf te trainen

1. **"Waarom?"** — Bij elk antwoord dat je geeft, dwing jezelf één stap door te vragen: *Waarom werkt dat zo?*
2. **"En als…?"** — Verander één voorwaarde in de casus (van eenmalig naar herhaald, van symmetrisch naar asymmetrisch, van privaat naar collectief). Verandert je antwoord? Dat bewijst dat je de logica snapt.
3. **"Welke partij wil dit?"** — Markeer in elke casus: 👤 consument · 🏭 producent · 🏛️ overheid. Hun belangen botsen vaak — dat is meestal de kern van de vraag.

> [!TIP]
> **🎯 Slotadvies:** Examenvragen testen zelden of je de definitie kunt opdreunen. Ze testen of je in een **nieuwe casus** het juiste mechanisme herkent en de **causale keten** kunt opschrijven. De *Begrijp de Logica*-blokken zijn je belangrijkste oefenmateriaal — sla deze samenvatting open naast elke oefenexamenvraag.
