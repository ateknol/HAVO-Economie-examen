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
    subgraph Methode["📖 Leerproces — 4 Lagen"]
        direction LR
        D1{{"1️⃣ Definitie"}} ==> D2(["2️⃣ Logica 🧠"]) ==> D3[/"3️⃣ Valkuil ⚠️"/] ==> D4[["4️⃣ Examen 🎯"]]
    end
    classDef stap1 fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef stap2 fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef stap3 fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef stap4 fill:#fef9c3,stroke:#eab308,stroke-width:2px,color:#713f12
    class D1 stap1
    class D2 stap2
    class D3 stap3
    class D4 stap4
```

> [!IMPORTANT]
> **Examen-Focus — Leeswijzer:** De dikke pijl `==>` toont de **vaste leesvolgorde**. Sla stap 2 (Logica) nooit over — examenvragen testen de keten, niet de definitie.

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
    subgraph Dim1["⏱️ Dimensie 1 — Tijd"]
        direction LR
        T{{"Wanneer?"}} -->|"tegelijk"| Sim(["Simultaan"]) ==> Mat["📊 Matrix + Nash"]
        T -->|"om beurt"| Seq(["Sequentieel"]) ==> Boom["🌳 Spelboom + BI"]
    end
    subgraph Dim2["🔁 Dimensie 2 — Herhaling"]
        direction LR
        H{{"Hoe vaak?"}} -->|"1×"| Een(["Eenmalig"]) ==> GDC["💼 GD klassiek"]
        H -->|"vaker"| Rep(["Herhaald"]) ==> Soc["🤝 Reputatie"]
    end
    subgraph Dim3["🤝 Dimensie 3 — Overleg"]
        direction LR
        S{{"Overleg?"}} -->|"ja"| Coop(["Coöperatief"]) ==> Con["📜 Contract"]
        S -->|"nee"| Niet(["Niet-coöp."]) ==> Kar["⚖️ Ieder voor zich"]
    end
    classDef besluit fill:#fef9c3,stroke:#eab308,stroke-width:2px,color:#713f12
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef grijs fill:#f1f5f9,stroke:#64748b,stroke-width:1px,color:#334155
    class T,H,S besluit
    class Sim,Een,Coop markt
    class Seq,Rep,Niet succes
    class Mat,Boom,GDC,Soc,Con,Kar grijs
```

> [!IMPORTANT]
> **Examen-Focus — 3 Dimensies:** Elke subgraph is één dimensie. De **gele hexagons** zijn de sleutelvragen — op het examen stel je deze 3 vragen bij iedere casus. De **blauwe stadium-nodes** zijn type A, de **groene** type B. De grijze rechthoeken tonen het bijbehorende analysemodel.

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
    subgraph Nash_Check["🔍 Nash-Evenwicht Check"]
        direction TB
        N_Start(["Kies strategieën"]) ==> N_Vraag{{"Eenzijdig<br/>verbeteren?"}}
        N_Vraag ==>|"✅ Nee"| N_Uitk[["🏆 Nash-evenwicht"]]
        N_Vraag -->|"❌ Ja"| N_Wissel[/"Andere strategie"/]
        N_Wissel -.->|"iteratie"| N_Start
    end
    classDef besluit fill:#fef9c3,stroke:#eab308,stroke-width:2px,color:#713f12
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    class N_Vraag besluit
    class N_Uitk succes
    class N_Wissel falen
    class N_Start markt
```

> [!IMPORTANT]
> **Examen-Focus — Nash-check:** De **gestippelde terugpijl** (`-.->`) is de feedbackloop — de iteratie stopt pas bij het **groene [[Nash-evenwicht]]**. De rode parallelogram toont dat een niet-Nash uitkomst onstabiel is: iemand wil altijd wisselen.

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
    GD_Kern{{"🔒 Gevangenen-<br/>dilemma"}}
    subgraph GD_Ind["👤 Individueel belang"]
        direction LR
        GD_Dom(["Bekennen = dominant"]) ==> GD_Slecht[/"😢 Nash: 3+3 jaar"/]
    end
    subgraph GD_Col["🤝 Collectief belang"]
        direction LR
        GD_Opt(["Niet bekennen = optimaal"]) ==> GD_Goed[["😊 1+1 jaar"]]
    end
    GD_Kern ==> GD_Dom
    GD_Kern ==> GD_Opt
    GD_Slecht -.->|"❌ paradox"| GD_Goed
    classDef risico fill:#ffedd5,stroke:#f97316,stroke-width:3px,color:#7c2d12
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    class GD_Kern risico
    class GD_Dom,GD_Slecht falen
    class GD_Opt,GD_Goed succes
```

> [!IMPORTANT]
> **Examen-Focus — GD:** Twee subgraphs staan naast elkaar: **rood** = wat rationeel gebeurt, **groen** = wat collectief beter is. De gestippelde pijl `-.->` markeert de paradox — de uitkomst wijst van de slechte Nash-uitkomst naar het collectieve optimum dat *niet* bereikt wordt. Op het examen: leg altijd uit waarom de rode uitkomst ondanks de groene optie het Nash-evenwicht is.

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
    subgraph PO_Trig["⚡ Trigger"]
        direction LR
        PO_Ol{{"🏪 Oligopolie"}} ==> PO_A(["Bedrijf A ↓ prijs"])
    end
    subgraph PO_Spiral["🔄 Neerwaartse Spiraal"]
        direction TB
        PO_B(["Marktaandeel A ↑"]) ==> PO_C(["Bedrijf B reageert ↓"])
        PO_C ==> PO_D[/"📉 Prijsspiraal"/]
    end
    subgraph PO_Uit["📊 Uitkomst"]
        direction LR
        PO_Q{{"Wie overleeft?"}}
        PO_Q -->|"zwakste weg"| PO_Win[["🏆 Winnaar"]]
        PO_Q -->|"beide overleven"| PO_GD[/"💸 GD-verlies"/]
    end
    PO_A ==> PO_B
    PO_D ==> PO_Q
    classDef risico fill:#ffedd5,stroke:#f97316,stroke-width:2px,color:#7c2d12
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef besluit fill:#fef9c3,stroke:#eab308,stroke-width:2px,color:#713f12
    class PO_Ol risico
    class PO_A,PO_B,PO_C markt
    class PO_D,PO_GD falen
    class PO_Win succes
    class PO_Q besluit
```

> [!IMPORTANT]
> **Examen-Focus — Prijzenoorlog cascade:** Drie subgraphs tonen de drie fases: oranje = **startconditie** (oligopolie), blauw = **actie** (de spiraal), geel = **beslissingsmoment** (wie overleeft?). De dikke pijl `==>` doorloopt de hoofdlijn; voor het examen: herken in welke fase de casustekst zich bevindt.

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
    subgraph OL_Cond["🏭 Vereiste Condities"]
        direction LR
        OL_K{{"Oligopolie<br/>+ homogeen"}} --> OL_Z(["👁️ Zichtbare prijzen"])
        OL_K --> OL_S(["🔄 Snelle substitutie"])
    end
    subgraph OL_Eff["📉 Gevolg"]
        direction LR
        OL_Sp[/"Iedereen verlaagt"/] ==> OL_V[["💸 Nash = GD-uitkomst"]]
    end
    OL_Z ==> OL_Sp
    OL_S ==> OL_Sp
    classDef risico fill:#ffedd5,stroke:#f97316,stroke-width:2px,color:#7c2d12
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    class OL_K risico
    class OL_Z,OL_S markt
    class OL_Sp,OL_V falen
```

> [!IMPORTANT]
> **Examen-Focus — Oligopolie mechanisme:** De twee blauwe stadium-nodes zijn de **condities** die tegelijk aanwezig moeten zijn. Beide pijlen `==>` stromen samen naar de rode parallelogram (spiraal). Ontbreekt één conditie (bv. product is heterogeen) → geen prijzenoorlog.

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
    subgraph Sp_U["🏢 Unilever — 1e zet"]
        U(((U)))
    end
    subgraph Sp_N["🏢 Nestlé — reageert"]
        N1(((N₁)))
        N2(((N₂)))
    end
    subgraph Sp_R["📊 Uitkomsten (Unilever ; Nestlé)"]
        R1["4,5 ; 4,5"]
        R2[["⭐ 6 ; 5,5"]]
        R3[["⭐ 5,5 ; 6"]]
        R4["5 ; 5"]
    end
    U -->|"ja"| N1
    U -->|"nee"| N2
    N1 -->|"ja"| R1
    N1 ==>|"nee ✓"| R2
    N2 ==>|"ja ✓"| R3
    N2 -->|"nee"| R4
    classDef s1 fill:#dbeafe,stroke:#3b82f6,stroke-width:3px,color:#1e3a8a
    classDef s2 fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef gekozen fill:#fef9c3,stroke:#eab308,stroke-width:3px,color:#713f12
    classDef niet fill:#f1f5f9,stroke:#64748b,stroke-width:1px,color:#334155
    class U s1
    class N1,N2 s2
    class R2,R3 gekozen
    class R1,R4 niet
```

> [!IMPORTANT]
> **Examen-Focus — Spelboom:** De **dikke pijlen** `==>` tonen het backwards-induction-pad (de gekozen takken). De gele [[dubbele rechthoeken]] zijn de ⭐-uitkomsten. Op het examen: werk altijd van rechts naar links — begin bij de gele vakjes, trek de dikke pijlen terug naar de blauwe cirkel.

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
    subgraph ZB_Zon["❌ Zonder zelfbinding"]
        direction LR
        ZB_Bel(["Belofte"]) --x ZB_NGB[/"Niet geloofwaardig"/]
    end
    subgraph ZB_Met["✅ Met zelfbinding"]
        direction LR
        ZB_Cert(["Belofte +<br/>🔒 Onomkeerbaar"]) ==> ZB_Gel(["Geloofwaardig"]) ==> ZB_Win[["🤝 Win-win"]]
    end
    ZB_Bel -.->|"+ certificaat<br/>+ boete"| ZB_Cert
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef oploss fill:#f3e8ff,stroke:#a855f7,stroke-width:2px,color:#581c87
    class ZB_Bel markt
    class ZB_NGB falen
    class ZB_Cert oploss
    class ZB_Gel,ZB_Win succes
```

> [!IMPORTANT]
> **Examen-Focus — Zelfbinding:** Let op de `--x` (kruis-pijl) in het rode blok — dit symboliseert een **blokkade**: de belofte zonder bewijs komt niet aan. De gestippelde pijl `-.->` verbindt de twee werelden: met de juiste toevoeging (certificaat/boete) wordt de belofte wél geloofwaardig. Paarse node = oplossingsmechanisme.

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
    subgraph EX_Markt["🏪 Markt (privaat)"]
        direction LR
        EX_PR(["💰 Private prijs"]) ==> EX_Bes(["Beslissing"])
    end
    EX_Ext{{"🌍 Extern effect"}} --x|"genegeerd"| EX_Bes
    EX_Falen[/"⚠️ Suboptimaal<br/>te veel / te weinig"/]
    subgraph EX_Cor["🏛️ Overheid corrigeert"]
        direction LR
        EX_OV{{"Beleid"}} -->|"belasting"| EX_Bel(["Internaliseren −"])
        EX_OV -->|"subsidie"| EX_Sub2(["Internaliseren +"])
    end
    EX_Opt[["✅ Maatschappelijk optimum"]]
    EX_Bes ==> EX_Falen
    EX_Falen ==> EX_OV
    EX_Bel ==> EX_Opt
    EX_Sub2 ==> EX_Opt
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef risico fill:#ffedd5,stroke:#f97316,stroke-width:2px,color:#7c2d12
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef oploss fill:#f3e8ff,stroke:#a855f7,stroke-width:2px,color:#581c87
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    class EX_PR,EX_Bes markt
    class EX_Ext risico
    class EX_Falen falen
    class EX_OV,EX_Bel,EX_Sub2 oploss
    class EX_Opt succes
```

> [!IMPORTANT]
> **Examen-Focus — Extern effect:** De `--x` kruis-pijl toont dat het oranje hexagon (extern effect) door de markt **geblokkeerd/genegeerd** wordt. Volg dan de rode parallelogram (suboptimaal) → paarse subgraph (overheidsbeleid) → groen resultaat. Dit is de standaard examenketen: **marktfalen → overheid ingrijpen → optimum**.

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
    subgraph CAO_Part["🤝 Sociale Partners"]
        direction LR
        CAO_V{{"👥 Vakbond"}} <-->|"onderhandelen"| CAO_WG{{"🏭 Werkgevers"}}
    end
    subgraph CAO_Proc["📜 CAO Proces"]
        direction LR
        CAO_C(["CAO bedrijfstak"]) ==> CAO_AVV[/"🏛️ AVV Minister SZW"/]
    end
    CAO_V ==> CAO_C
    CAO_WG ==> CAO_C
    CAO_Res[["✅ Geldt voor ALLE werknemers<br/>bedrijfstak"]]
    CAO_AVV ==> CAO_Res
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef proces fill:#e0e7ff,stroke:#4338ca,stroke-width:2px,color:#1e1b4b
    classDef oploss fill:#f3e8ff,stroke:#a855f7,stroke-width:2px,color:#581c87
    class CAO_V markt
    class CAO_WG succes
    class CAO_C proces
    class CAO_AVV oploss
    class CAO_Res succes
```

> [!IMPORTANT]
> **Examen-Focus — CAO:** De dubbele pijl `<-->` toont de *onderhandeling* tussen blauw (werknemers) en groen (werkgevers). Beide stromen via `==>` naar de blauwe stadium-node (CAO). De paarse parallelogram (AVV) is de **overheids-stempel** die de CAO voor de hele bedrijfstak geldig maakt. Eindresultaat: het groene [[uitkomst-blok]].

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
    subgraph EU_Zon["❌ Zonder EU — GD scenario"]
        direction LR
        EU_27{{"27 landen<br/>eigen belang"}} ==> EU_GD[/"Handelsoorlogen<br/>Valuta-race<br/>Subsidie-wedloop"/]
    end
    subgraph EU_Met["✅ Met EU — Coöperatief spel"]
        direction LR
        EU_Verd(["Verdragen + Regels"]) ==> EU_Inst(["🏛️ ECB · Hof · EMU"])
        EU_Inst ==> EU_Win[["💶 Lagere kosten<br/>grotere markt · vrede"]]
    end
    EU_27 -.->|"verdragen sluiten"| EU_Verd
    classDef risico fill:#ffedd5,stroke:#f97316,stroke-width:2px,color:#7c2d12
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef oploss fill:#f3e8ff,stroke:#a855f7,stroke-width:2px,color:#581c87
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    class EU_27 risico
    class EU_GD falen
    class EU_Verd,EU_Inst oploss
    class EU_Win succes
```

> [!IMPORTANT]
> **Examen-Focus — EU als coöperatief spel:** Twee subgraphs: rood = het GD-scenario **zonder** EU, groen = de oplossing **met** EU. De gestippelde pijl `-.->` toont de transitie: de 27 landen kiezen ervoor verdragen te sluiten. Paarse nodes = de EU-instituten die het GD doorbreken. Dit diagram is de EU-samenvatting in één oogopslag.

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
    subgraph VZ_Calc["🧮 Stap 1 — Bereken"]
        direction LR
        VZ_R{{"R = kans × schade"}} ==> VZ_P{{"P = jaarpremie"}}
    end
    subgraph VZ_Bes["💡 Stap 2 — Beslisregel"]
        direction TB
        VZ_Comp{{"P vs R?"}} -->|"P < R"| VZ_GoA[["✅ VERZEKEREN<br/>wiskundig voordelig"]]
        VZ_Comp -->|"P > R"| VZ_Vr{{"Schade<br/>draagbaar?"}}
        VZ_Vr -->|"Nee"| VZ_GoB[["✅ VERZEKEREN<br/>risicoaversie"]]
        VZ_Vr -->|"Ja"| VZ_Niet[/"❌ Zelf-verzekeren"/]
    end
    VZ_P ==> VZ_Comp
    classDef besluit fill:#fef9c3,stroke:#eab308,stroke-width:2px,color:#713f12
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    class VZ_R,VZ_P,VZ_Comp,VZ_Vr besluit
    class VZ_GoA,VZ_GoB succes
    class VZ_Niet falen
```

> [!IMPORTANT]
> **Examen-Focus — Beslisregel verzekeren:** Twee subgraphs = twee stappen. Begin altijd in de **gele subgraph** (berekenen). Daarna stroomt de pijl naar de beslisregel. De dikke pijl `==>` verbindt de twee stappen; het examen verwacht dat je beiden uitvoert — niet alleen "P > R dus niet verzekeren".

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
    subgraph Sol_Vrij["❌ Vrijwillig"]
        direction TB
        S_V(["Alleen zieken<br/>melden zich"]) ==> S_VH[/"Hoog risico<br/>€ 1.350"/]
    end
    subgraph Sol_Vpl["✅ Verplicht (solidariteit)"]
        direction TB
        S_P(["Iedereen verplicht<br/>ook gezonden"]) ==> S_PL[["Laag risico<br/>€ 1.080"]]
    end
    S_VH -.->|"solidariteit<br/>doorbreekt spiraal"| S_PL
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef oploss fill:#f3e8ff,stroke:#a855f7,stroke-width:2px,color:#581c87
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    class S_V markt
    class S_VH falen
    class S_P oploss
    class S_PL succes
```

> [!IMPORTANT]
> **Examen-Focus — Solidariteit:** Twee subgraphs naast elkaar: rood = vrijwillig (slechte uitkomst), groen = verplicht (goede uitkomst). De gestippelde pijl `-.->` loopt van de slechte uitkomst naar de goede — dit is de **doorbreking** van de spiraal door verplichting. Op het examen: leg altijd uit *waarom* de premie daalt (grotere noemer + lager gemiddeld risico).

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
    subgraph AS_Start["❓ Asymmetrische info"]
        direction LR
        AS_Info{{"🔍 Verzekeraar<br/>weet risico NIET"}} ==> AS_Gem(["Één gemiddelde premie"])
    end
    subgraph AS_Sel["🔄 Zelfselectie"]
        direction LR
        AS_Goed[/"🟢 Goede risico's<br/>haken af"/]
        AS_Slecht(["🔴 Slechte risico's<br/>stromen in"])
    end
    subgraph AS_Spiral["📈 Opwaartse spiraal"]
        direction LR
        AS_Hoog[/"Gemiddeld risico ↑"/] ==> AS_Prem[/"Premie ↑"/]
    end
    AS_Gem -->|"te duur"| AS_Goed
    AS_Gem -->|"koopje!"| AS_Slecht
    AS_Goed ==> AS_Hoog
    AS_Prem -.->|"feedback:<br/>meer uitstroom"| AS_Goed
    classDef risico fill:#ffedd5,stroke:#f97316,stroke-width:2px,color:#7c2d12
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    class AS_Info risico
    class AS_Gem markt
    class AS_Goed,AS_Slecht,AS_Hoog,AS_Prem falen
```

> [!IMPORTANT]
> **Examen-Focus — Averechtse selectie spiraal:** Drie subgraphs tonen de drie fases: oranje hexagon = **oorzaak** (informatiekloof), rood parallelogram = **zelfselectie** (goede risico's weg), rood spiraal = **escalatie** (premie omhoog). De `-.->` feedbackpijl sluit de lus — dit is de **doodsspiraal**. Op het examen: benoem alle drie fases bij naam.

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
    subgraph MH_Voor["✅ Vóór verzekering"]
        direction TB
        MH_V(["Kosten = 100% bij jou"]) ==> MH_VG[["Voorzichtig gedrag"]]
    end
    subgraph MH_Na["⚠️ Ná verzekering"]
        direction TB
        MH_N(["Kosten = 0% bij jou<br/>prikkel weg"]) ==> MH_NG[/"Risicovol gedrag"/]
        MH_NG ==> MH_NK[/"Premies ↑ voor iedereen"/]
    end
    MH_V -.->|"tekenen polis →<br/>prikkel verdwijnt"| MH_N
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    class MH_V markt
    class MH_VG succes
    class MH_N,MH_NG,MH_NK falen
```

> [!IMPORTANT]
> **Examen-Focus — Moral hazard:** De gestippelde pijl `-.->` toont het **omslagpunt**: het tekenen van de polis. Links = groen (vóór), rechts = rood (ná). Dit is het kernprincipe: hetzelfde individu verandert van gedrag door de polis. Op het examen: moral hazard = **ná afsluiten**, averechtse selectie = **vóór afsluiten**.

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
    subgraph I_Probl["⚠️ Probleem"]
        I_Ainfo{{"Asymm. info<br/>→ AS + MH"}}
    end
    subgraph I_1["1️⃣ Eigen risico"]
        direction LR
        I_ER(["Skin in the game"]) ==> I_ER2[["Anti-MH + Signalling AS"]]
    end
    subgraph I_2["2️⃣ Premiedifferentiatie"]
        direction LR
        I_PD(["Premie per risicogroep"]) ==> I_PD2[["Goede risico's blijven<br/>+ gedrag beloond"]]
    end
    subgraph I_3["3️⃣ Informatie inwinnen"]
        direction LR
        I_INF(["Vragenlijst + CIS<br/>+ schadevrije jaren"]) ==> I_INF2[["AS verkleind<br/>fraude opgespoord"]]
    end
    I_Ainfo ==> I_ER
    I_Ainfo ==> I_PD
    I_Ainfo ==> I_INF
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    class I_Ainfo falen
    class I_ER,I_PD,I_INF markt
    class I_ER2,I_PD2,I_INF2 succes
```

> [!IMPORTANT]
> **Examen-Focus — 3 Instrumenten:** De rode hexagon is het **probleem** dat drie dikke pijlen `==>` uitzendt naar de drie blauwe oplossingen. Elk blauw stadium-node stroomt naar een groen resultaat. Op het examen: voor elke maatregel moet je kunnen benoemen *welk* probleem (AS, MH of beide) het aanpakt.

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
    subgraph ER_Base["💶 Eigen risico"]
        direction TB
        ER_V{{"€ 385 verplicht<br/>+ vrijwillig deel"}}
    end
    subgraph ER_Eff1["⚠️ Effect: Moral Hazard"]
        direction LR
        ER_MH(["Skin in the game"]) ==> ER_MH2[["✅ Voorzichtiger gedrag"]]
    end
    subgraph ER_Eff2["🔍 Effect: Averechtse Selectie"]
        direction LR
        ER_Sig(["Hoog ER kiezen<br/>= signaal laag risico"]) ==> ER_AS[["✅ Verzekeraar leert<br/>risicotype"]]
    end
    ER_V ==> ER_MH
    ER_V ==> ER_Sig
    classDef besluit fill:#fef9c3,stroke:#eab308,stroke-width:2px,color:#713f12
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    class ER_V besluit
    class ER_MH,ER_Sig markt
    class ER_MH2,ER_AS succes
```

> [!IMPORTANT]
> **Examen-Focus — Eigen risico:** De gele hexagon (eigen risico) zendt twee dikke pijlen `==>` uit naar twee verschillende effecten. Subgraph links = anti-MH, rechts = anti-AS via signalling. Op het examen: onderscheid altijd het **verplichte** deel (anti-MH) van het **vrijwillige** deel (signalling → anti-AS).

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
    subgraph BM_Ladder["🎯 Bonus-malus ladder"]
        direction TB
        BM_S{{"Starttrede 2"}} -->|"🟢 Jaar zonder schade"| BM_Up(["⬆️ Trede +1 bonus"])
        BM_S -->|"🔴 Schade gemeld"| BM_Dn(["⬇️ Treden omlaag malus"])
    end
    BM_Up ==> BM_WR[["Voorzichtig rijden<br/>→ anti-MH"]]
    BM_Dn -.->|"prikkel tot<br/>voorzichtigheid"| BM_Up
    classDef besluit fill:#fef9c3,stroke:#eab308,stroke-width:2px,color:#713f12
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    class BM_S besluit
    class BM_Up,BM_WR succes
    class BM_Dn falen
```

| Effect | Uitleg |
|---|---|
| Tegen **moral hazard** | Claimen kost je korting → je rijdt voorzichtiger / claimt alleen echte schade |
| Tegen **averechtse selectie** | Goede rijders betalen lagere premie → stoppen niet → blijven in de groep |

**Aandachtspunt:** bij zorgverzekering heeft bonus-malus voor de basisverzekering beperkt effect, want gezondheid is niet altijd beïnvloedbaar.

```mermaid
flowchart TD
    subgraph PD_Zon["❌ Zonder differentiatie"]
        direction LR
        PD_ZD(["Iedereen € 1.000"]) ==> PD_AF[/"Goede risico's<br/>haken af = AS"/]
    end
    subgraph PD_Met["✅ Mét differentiatie + bonus-malus"]
        direction TB
        PD_MD(["Premie per risicogroep"]) ==> PD_ST(["Goede risico's blijven<br/>€ 600"])
        PD_ST ==> PD_ST2[["✅ Stabiele pool"]]
        PD_BM(["Claim → ↑ premie<br/>geen claim → ↓ premie"]) ==> PD_RG[["Voorzichtiger gedrag<br/>anti-MH"]]
    end
    PD_AF -.->|"oplossing"| PD_MD
    PD_AF -.->|"oplossing"| PD_BM
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    class PD_ZD,PD_AF falen
    class PD_MD,PD_ST,PD_BM markt
    class PD_ST2,PD_RG succes
```

> [!IMPORTANT]
> **Examen-Focus — Premiedifferentiatie:** Twee subgraphs: rood = probleem (zonder diff.), groen = oplossing. De twee gestippelde `-.->` pijlen vanuit de rode parallelogram tonen dat dezelfde oorzaak (AS) **twee** oplossingen triggert. Op het examen: premiedifferentiatie pakt AS aan, bonus-malus pakt MH aan — maar ze kunnen tegelijk ingezet worden.

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
    subgraph AP_Bas["🏥 Basiszorgverzekering"]
        direction TB
        AP_B{{"Maatschappelijk vitaal"}} ==> AP_AP(["✅ Acceptatieplicht<br/>+ verbod risicoselectie"])
        AP_AP ==> AP_SOL[["🤝 Hoge solidariteit"]]
    end
    subgraph AP_Vrij["🚗 Aanvullend / Auto / Reis"]
        direction TB
        AP_V{{"Vrije markt"}} ==> AP_RS(["⚖️ Selectie + differentiatie<br/>toegestaan"])
        AP_RS ==> AP_EFF[["⚡ Hoge efficiëntie"]]
    end
    AP_SOL -.->|"spanning"| AP_EFF
    classDef oploss fill:#f3e8ff,stroke:#a855f7,stroke-width:2px,color:#581c87
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef markt fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef besluit fill:#fef9c3,stroke:#eab308,stroke-width:2px,color:#713f12
    class AP_B oploss
    class AP_AP,AP_SOL succes
    class AP_V,AP_RS markt
    class AP_EFF besluit
```

> [!IMPORTANT]
> **Examen-Focus — Acceptatieplicht:** Twee subgraphs staan naast elkaar: paars-groen = **basiszorg** (solidariteit wins), blauw-geel = **aanvullend** (efficiëntie wins). De gestippelde `-.->` pijl tussen de twee uitkomsten toont de **spanningsverhouding** — dit is een classic examenthema: solidariteit vs. efficiëntie.

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

### Infographic — verbanden tussen alle hoofdthema's

```mermaid
flowchart TD
    KERN{{"🎯 MARKTFALEN<br/>+ OPLOSSINGEN"}}
    subgraph ST["🎲 Speltheorie H1.1–1.3"]
        direction LR
        ST1(["Simultaan"]) --> ST1a["Matrix · Nash · GD"]
        ST2(["Sequentieel"]) --> ST2a["Spelboom · BI · Ultimatum"]
        ST3(["GD Doorbrekers"]) --> ST3a["Contract · Zelfbinding · Herhaling"]
    end
    subgraph EX["🌍 Externe Effecten H1.4"]
        direction LR
        EX1(["Negatief"]) --> EX1a["Belasting · Verbod"]
        EX2(["Positief"]) --> EX2a["Subsidie"]
        EX3(["Collectief goed"]) --> EX3a["Free-rider · Collectieve dwang"]
    end
    subgraph SAM["🤝 Samenwerking H1.5"]
        direction LR
        SAM1(["Arbeidsmarkt"]) --> SAM1a["CAO · AVV"]
        SAM2(["EU"]) --> SAM2a["EMU · Euro · Brexit"]
        SAM3(["MVO"]) --> SAM3a["People · Planet · Profit"]
    end
    subgraph RISICO_G["🛡️ Risico H2.1"]
        direction LR
        R1(["R = kans × schade"]) --> R1a["Solidariteit · Omslag/Kapitaal"]
    end
    subgraph INFO_G["❓ Asymm. Info H2.2"]
        direction LR
        I1(["Averechtse selectie"]) --> I1a["vóór contract · spiraal"]
        I2(["Moral hazard"]) --> I2a["ná contract · gedrag"]
    end
    subgraph OPL["🔧 Oplossingen H2.3"]
        direction LR
        O1(["Eigen risico"]) --> O1a["anti-MH + signalling"]
        O2(["Premiediff."]) --> O2a["anti-AS + anti-MH"]
        O3(["Informatie + CIS"]) --> O3a["acceptatieplicht"]
    end
    KERN ==> ST
    KERN ==> EX
    KERN ==> SAM
    KERN ==> RISICO_G
    KERN ==> INFO_G
    INFO_G ==> OPL
    classDef kern fill:#ffedd5,stroke:#f97316,stroke-width:3px,color:#7c2d12
    classDef blauw fill:#dbeafe,stroke:#3b82f6,stroke-width:2px,color:#1e3a8a
    classDef groen fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    classDef paars fill:#f3e8ff,stroke:#a855f7,stroke-width:2px,color:#581c87
    classDef grijs fill:#f1f5f9,stroke:#64748b,stroke-width:1px,color:#334155
    class KERN kern
    class ST1,ST2,ST3 blauw
    class EX1,EX2,EX3 blauw
    class SAM1,SAM2,SAM3 groen
    class R1 groen
    class I1,I2 paars
    class O1,O2,O3 paars
    class ST1a,ST2a,ST3a,EX1a,EX2a,EX3a,SAM1a,SAM2a,SAM3a,R1a,I1a,I2a,O1a,O2a,O3a grijs
```

> [!IMPORTANT]
> **Examen-Focus — Infographic:** Het oranje hexagon (`KERN`) is het centrale concept: marktfalen. Alle dikke pijlen `==>` tonen de 6 hoofd-deelgebieden als subgraphs. Blauw = speltheorie/externe effecten, groen = samenwerking/risico, paars = informatieproblemen + oplossingen. Grijze rechthoeken = de examenbegrippen. Gebruik dit overzicht als checklijst bij een open casusvraag: in welke subgraph valt de casus?

### Het terugkerende patroon: probleem → keten → oplossing

```mermaid
flowchart LR
    subgraph TP_P["⚠️ Marktfalen"]
        direction TB
        TP_Prob{{"PROBLEEM"}}
        TP_Prob --> TP_P1["• GD"]
        TP_Prob --> TP_P2["• Extern effect"]
        TP_Prob --> TP_P3["• Asymm. info"]
    end
    subgraph TP_K["🔄 Negatieve Keten"]
        TP_Ket[/"SPIRAAL<br/>te veel · te weinig<br/>race to bottom"/]
    end
    subgraph TP_I["🏛️ Institutionele Oplossing"]
        direction TB
        TP_Inst(["Wet"])
        TP_Inst2(["Contract / CAO"])
        TP_Inst3(["Verzekering"])
        TP_Inst4(["Verdrag / Belasting"])
    end
    TP_Opt[["✅ Maatschappelijk optimum"]]
    TP_Prob ==> TP_Ket
    TP_Ket ==> TP_Inst
    TP_Ket ==> TP_Inst2
    TP_Ket ==> TP_Inst3
    TP_Ket ==> TP_Inst4
    TP_Inst ==> TP_Opt
    TP_Inst2 ==> TP_Opt
    TP_Inst3 ==> TP_Opt
    TP_Inst4 ==> TP_Opt
    TP_Opt -.->|"kan opnieuw falen<br/>(techniek · vergrijzing · AI)"| TP_Prob
    classDef falen fill:#fee2e2,stroke:#ef4444,stroke-width:2px,color:#7f1d1d
    classDef risico fill:#ffedd5,stroke:#f97316,stroke-width:2px,color:#7c2d12
    classDef oploss fill:#f3e8ff,stroke:#a855f7,stroke-width:2px,color:#581c87
    classDef succes fill:#dcfce7,stroke:#22c55e,stroke-width:2px,color:#14532d
    class TP_Prob,TP_P1,TP_P2,TP_P3 falen
    class TP_Ket risico
    class TP_Inst,TP_Inst2,TP_Inst3,TP_Inst4 oploss
    class TP_Opt succes
```

> [!IMPORTANT]
> **Examen-Focus — Terugkerend patroon:** De rode subgraph (marktfalen) voedt de oranje spiraal via `==>`. Vier paarse nodes (oplossingen) convergeren allemaal naar het groene [[optimum]]. De `-.->` feedbackpijl sluit de cirkel — dit is het cruciale inzicht voor open vragen: markten kunnen **opnieuw** falen als omstandigheden veranderen. Gebruik dit schema als kapstok bij *elke* casusanalyse.

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
