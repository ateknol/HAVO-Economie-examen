# 🎯 Logica-Dashboard · Hoofdstuk 1 — Samenwerken is een spel

> Visueel dashboard per paragraaf. Focus op **causale ketens** (Mermaid) en **score-termen** (exact de woorden uit de correctievoorschriften 2023-2025). Onderaan: welke examenvragen je oefent per paragraaf.

---

## § 1.1 · Speltheorie · Nash & Gevangenendilemma

### Causale keten — van dominante strategie naar gevangenendilemma

```mermaid
flowchart TD
    A["Simultaan spel<br/>(tegelijk beslissen, geen overleg)"] --> B["Per speler: kijk per kolom/rij naar<br/>beste uitkomst → best response"]
    B --> C{"Ongeacht wat ander kiest<br/>ALTIJD dezelfde keuze beste?"}
    C -- "Ja" --> D["DOMINANTE STRATEGIE"]
    C -- "Nee" --> E["Geen dominante strategie<br/>(kijk alleen naar Nash)"]
    D --> F["Nash-evenwicht<br/>= kruising van beider best response"]
    F --> G{"Is Nash optimaal<br/>voor beide spelers?"}
    G -- "Nee, beide zouden beter af zijn<br/>bij andere combinatie" --> H["⚠ GEVANGENENDILEMMA<br/>Uitkomst is SUBOPTIMAAL"]
    G -- "Ja" --> I["Géén gevangenendilemma<br/>(evenwicht = optimaal)"]
```

### 🔑 Dikgedrukte score-termen

- **Simultaan spel** · beide spelers beslissen tegelijk, geen overleg.
- **Dominante strategie** · "de keuze die een partij maakt, **ongeacht** de keuze die de ander maakt".
- **Best response-methode** · per kolom het beste voor rijspeler arceren; per rij het beste voor kolomspeler.
- **Nash-evenwicht** · combinatie van strategieën waarbij **geen van de spelers een reden heeft om van strategie te veranderen**.
- **Gevangenendilemma** · situatie waarin een evenwicht ontstaat waarbij de uitkomst **voor beiden niet optimaal** is.

### ✍️ Examen-formulering (letterlijk goed gerekend in CV)

> "De dominante strategie voor X is Y, want **ongeacht wat** de tegenpartij kiest, de uitkomst is het **minst negatief / het meest positief** als X kiest voor Y."
>
> "Het resultaat (Y, Y) is **suboptimaal voor beide**, want **beider individuele resultaten zouden beter zijn** als beide kiezen voor Z (en dus er is sprake van een **gevangenendilemma**)."

### ⚠️ Check: géén gevangenendilemma

Als beide partijen een dominante strategie hebben, maar de uitkomst is al **optimaal voor beiden tegelijk** → géén gevangenendilemma (zie 2025 v16).

---

## § 1.2 · Prijzenoorlog & Oligopolie

### Causale keten — prijzenoorlog als gevangenendilemma

```mermaid
flowchart LR
    M["Oligopolie<br/>(weinig aanbieders, marktmacht)"] --> P1["Bedrijf A verlaagt prijs<br/>= dominante strategie"]
    P1 --> P2["Bedrijf B verlaagt ook<br/>= dominante strategie"]
    P2 --> PW["PRIJZENOORLOG<br/>beide winstmarges dalen"]
    PW --> OPT["Collectief optimum<br/>= beide prijs handhaven"]
    OPT -. "niet bereikbaar zonder overleg<br/>= gevangenendilemma" .-> P1
    PW --> UIT["Zwakste valt om →<br/>winnaar verhoogt prijs weer"]
```

### 🔑 Kenmerken oligopolie (score-termen CV 2023 v21)

| Kenmerk | Examenzin |
|---|---|
| Beperkt aantal aanbieders | "Er is sprake van een **beperkt aantal aanbieders**." |
| Toetredingsbarrières | "Er zijn **toetredingsbarrières** (beschikking over [specifieke input] is voorwaardelijk voor toetreding)." |
| Marktmacht | "Er is sprake van **marktmacht** (dit blijkt uit het gegeven dat er concurrentiestrijd is om marktaandeel)." |

### ⚠️ Let op — prijsafspraken vs. prijzenoorlog

- **Prijzenoorlog** = toegestaan.
- **Prijsafspraken** tussen concurrenten = **verboden** (Mededingingswet / kartelverbod).

### Olie-voorbeeld (2023): prijsinelastische vraag

```mermaid
flowchart LR
    A["Beide landen verlagen aanbod"] --> B["Prijs olie ↑"]
    B --> C{"Omzet verandert"}
    C -- "Omzet ↑ ondanks prijsstijging" --> D["Vraag is PRIJSINELASTISCH<br/>(|Ev| < 1)"]
```

> Economische logica: bij **prijsinelastische vraag** → prijsstijging leidt tot omzetstijging; bij **prijselastische vraag** → prijsstijging leidt tot omzetdaling.

---

## § 1.3 · Onderhandelen, Ultimatumspel & Sociale normen

### Causale keten — minimum-acceptatie in een eenmalig spel

```mermaid
flowchart TD
    S["Eenmalig ultimatumspel<br/>Speler 1 doet voorstel<br/>Speler 2 accepteert/weigert"] --> S2["Speler 2 heeft startkosten €X"]
    S2 --> MIN["Minimaal acceptabel:<br/>voorstel ≥ startkosten"]
    MIN --> TIP["✔ Minimum = €X of €X+1<br/>(eigenbelang korte termijn)"]
    S --> HERH{"Herhaald spel?"}
    HERH -- "Ja, toekomstige samenwerking" --> V["Vertrouwen speelt mee →<br/>speler 1 biedt HOGER"]
    HERH -- "Sociale norm aanwezig" --> SN["Eerlijke verdeling / geen gezichtsverlies →<br/>speler 1 biedt HOGER<br/>speler 2 weigert te lage voorstellen"]
```

### 🔑 Score-termen (CV 2024 v25-27)

- **Ultimatumspel-minimum** · "De aannemer zal een verdeling accepteren waarmee de **eigen startkosten worden terugverdiend**." → antwoord: `€ 25.000 / € 25.001`.
- **Herhaald spel** · "**Vertrouwen (in een gunstige toekomstige samenwerking)** speelt een rol" → speler 1 stelt **hoger bedrag** voor.
- **Sociale norm** · voorbeeld: "**gelijke verdeling bij gelijke prestatie**" of "**eerlijke verdeling**".
- Effect sociale norm op gedrag: speler 2 **weigert een (te laag) bedrag dat niet voldoet aan de sociale norm**; speler 1 biedt hoger **om gezichtsverlies in de sociale omgeving te voorkomen**.

### Verzonken kosten · dubbele rol

```mermaid
flowchart LR
    VK["Verzonken kosten<br/>= specifieke al gemaakte kosten,<br/>niet terug te verdienen bij stoppen"]
    VK --> R1["Rationele les:<br/>speelt géén rol in keuze vooruit"]
    VK --> R2["Praktisch effect in CO2-casus:<br/>bedrijven ZOEKEN nieuwe markten<br/>om investering terug te verdienen<br/>→ productie ↑ → CO2 ↑"]
```

### Zelfbinding vs. contract vs. sociale norm

| Instrument | Werking | Geloofwaardigheidsbron |
|---|---|---|
| **Contract** | Juridisch bindend, boete bij verbreken | Wet / rechter |
| **Sociale norm** | Reputatie, gezichtsverlies | Sociale omgeving |
| **Zelfbinding** | Eenzijdig onomkeerbaar maken | Zichtbaarheid + onomkeerbaarheid |

---

## § 1.4 · Externe effecten & Internalisatie

### Causale keten — van negatief extern effect naar internalisering

```mermaid
flowchart TD
    A["Productie/consumptie<br/>(bv. autorijden, CO2-uitstoot)"] --> B["BIJKOMSTIG gevolg voor derden<br/>(luchtvervuiling, klimaatschade)"]
    B --> C["Gevolg komt NIET tot uitdrukking<br/>in de prijs → MAATSCHAPPELIJKE KOSTEN"]
    C --> D["MARKTFALEN<br/>(markt houdt er geen rekening mee)"]
    D --> E{"Overheidsingrijpen"}
    E --> F["Belasting / heffing<br/>(bv. CO2-afhankelijke bijtelling)"]
    E --> G["Verhandelbare emissierechten<br/>met prijs = maatschappelijke kosten"]
    E --> H["Subsidie / collectieve dwang"]
    F --> I["Vervuiler gaat meer betalen →<br/>prikkel om minder/schoner te produceren"]
    G --> I
    I --> J["✅ GEÏNTERNALISEERD<br/>geen (minder) negatieve externe effecten"]
```

### 🔑 Score-termen — negatief extern effect (CV 2023 v13 + 2025 v15/v20)

- **Negatief extern effect** · "de vervuiling **komt niet tot uitdrukking in de prijs** van [het product]".
- **Maatschappelijke kosten** · "dit leidt tot **maatschappelijke kosten**".
- **Prijsmechanisme als prikkel** · "de vervuiler gaat **meer betalen voor meer CO₂-uitstoot** → consument wordt **gestimuleerd** om [minder vervuilend alternatief] te kiezen".
- **Internalisatie** · "Hierdoor wordt de vervuiling **geïnternaliseerd** en is er sprake van **minder negatieve externe effecten**" / "de **vervuiler gaat er zelf voor betalen**. Er zijn dan **geen negatieve externe effecten meer**."
- **Emissierechten** · kopen → kosten ↑ → prikkel om **duurzamer / schoner / minder te produceren**; verkopen → opbrengst ↑ → duurzaam produceren **aantrekkelijker**.

### Groen bbp — twee tegengestelde effecten bij minder emissierechten (CV 2025 v19)

```mermaid
flowchart LR
    M["Minder emissierechten"] --> P["Productie ↓"]
    P --> BBP1["BBP ↓ → groen bbp ↓"]
    P --> U["Uitstoot ↓"]
    U --> MS["Milieuschade ↓"]
    MS --> BBP2["groen bbp ↑"]
```

---

## § 1.5 · Arbeidsmarkt · CAO · EU · MVO

*In de examens 2023-2025 is géén directe vraag gesteld over CAO / vakbond / EU-structuur / MVO. Kerntheorie voor SE en eventuele examenvraagstukken staat in de volledige samenvatting. Onderstaand dashboard blijft relevant voor begrippen.*

### Causale keten — CAO als oplossing voor gevangenendilemma op arbeidsmarkt

```mermaid
flowchart LR
    WN["Individuele werknemer<br/>(zwakke positie)"] --> VB["Vakbond<br/>(collectieve onderhandelingsmacht)"]
    WG["Individuele werkgever"] --> WO["Werkgeversorganisatie"]
    VB <--> WO
    VB --> CAO["CAO<br/>(primaire + secundaire voorwaarden)"]
    WO --> CAO
    CAO --> AVV["Minister SZW:<br/>Algemeen Verbindend Verklaren"]
    AVV --> BT["Alle werkgevers in bedrijfstak"]
```

### Kernbegrippen

- **Primaire arbeidsvoorwaarden** · loon + werktijden.
- **Secundaire arbeidsvoorwaarden** · vakantie, pensioen, ziekteuitkering, opleiding.
- **CAO** · collectieve afspraken per bedrijfstak tussen vakbonden en werkgeversorganisaties.
- **EU / EMU** · 27 landen; gezamenlijk monetair beleid & euro.
- **MVO / 3 P's** · People, Planet, Profit.
- **Circulaire economie** · producten en materialen behouden waarde door hergebruik.

---

## 📝 Geselecteerde examenvragen per paragraaf

| § | Thema | Jaar · Opg. · Vraag | Punten |
|---|---|---|---|
| **1.1** | Dominante strategie & gevangenendilemma | **2023 · Opg. 5 · v22** | 2p |
| **1.1** | Dominante strategie & géén gevangenendilemma | **2025 · Opg. 3 · v16** | 2p |
| **1.2** | Marktvraag verandering → prijs | **2023 · Opg. 5 · v20** | 1p |
| **1.2** | Oligopolie + 2 kenmerken | **2023 · Opg. 5 · v21** | 2p |
| **1.3** | Ultimatumspel — minimale acceptatie | **2024 · Opg. 6 · v25** | 2p |
| **1.3** | Herhaald spel & vertrouwen | **2024 · Opg. 6 · v26** | 2p |
| **1.3** | Sociale norm beïnvloedt gedrag | **2024 · Opg. 6 · v27** | 2p |
| **1.3** | Verzonken kosten → zoektocht nieuwe markten | **2025 · Opg. 3 · v17** | 2p |
| **1.4** | Fiscale bijtelling → negatief extern effect terugdringen | **2023 · Opg. 3 · v13** | 2p |
| **1.4** | Emissierechten prikkelen tot minder CO₂ | **2025 · Opg. 3 · v15** | 1p |
| **1.4** | Internalisering: prijs = maatschappelijke kosten | **2025 · Opg. 3 · v20** | 1p |

**Totaal: 11 vragen · 20 punten**

---

> 📂 Voor de interactieve oefening: open `Examen_Engine_H1.html` in je browser. Vraag + volledig antwoordmodel (puntenverdeling 1-op-1 uit het officiële correctievoorschrift) staan daar inklapbaar.
