---
type: activity
code: 410
proces: Property Operations Compliance Control
status: draft
sop: AM-PROM-400
wi: AM-PROM-410
eigenaar: "[[Property Manager]]"
laatst_bijgewerkt: 2026-11-18
---

# Demarcatielijst — Toepassen demarcatie template

## Doel
Per gebouw vastleggen wie (Maatschappij of Eigenaar/BAC) verantwoordelijk is voor de uitvoering, betaling en eigendom van onderhoud, herstelling en vervanging van elk onderdeel van de infrastructuur. De demarcatielijst maakt onlosmakelijk deel uit van het contract en legt op gestructureerde wijze de verdeling van verantwoordelijkheden vast. ([[00_Sources/AM-PROM-400 POL Demarcatielijst.pdf]])

## Definities ([[00_Sources/AM-PROM-400 POL Demarcatielijst.pdf]])

| Term | Definitie |
|------|-----------|
| Maatschappij | De partij aan wie het gebouw ter beschikking wordt gesteld en met wie contractuele afspraken gemaakt worden over verantwoordelijkheden |
| Single user (SU) | Gebouw waarbij slechts 1 partij gebruik maakt van het gebouw |
| Multi user (MU) | Gebouw waarbij meer dan 1 partij gebruik maakt van het gebouw |
| Eigenaar | BAC (en legale entiteiten/verbonden vennootschappen) als eigenaar van de gebouwen |
| Onderhoud | Preventief uitvoeren van reinigingen en werkzaamheden op vooraf bepaalde tijd, conform wettelijke eisen, normering en leveranciersvoorschriften |
| Herstelling | Na vastgesteld disfunctioneren of schade: herstelwerkzaamheden uitvoeren ter voorkoming van vervanging |
| Vervanging | Indien onderhoud/herstelling niet meer volstaat, of levensduur bereikt, of installatie faalt binnen waarborgperiode |
| Eigendom | Aanduiding aan welke partij de bouwkundige en installatietechnische onderdelen toebehoren |
| Uitvoering | Aanduiding wie verantwoordelijk is voor de uitvoering van onderhoud, herstelling en vervanging |
| Betaling | Aanduiding welke partij het onderhoud, herstelling en vervanging betaalt |

## Trigger
- Nieuw contract of gebouw: demarcatielijst opstellen voor die Maatschappij
- Contractwijziging: demarcatielijst bijwerken
- Start compliance-register: demarcatielijst als basis voor verantwoordelijkheden

## Input
- Standaard demarcatielijst SU of MU (AM-PROM-411)
- Contractuele afspraken
- Inventaris aanwezige installaties
([[00_Sources/AM-PROM-411 Template demarcatielijst.xlsx]])

## Stappen

| # | Stap | Wie | Tool |
|---|------|-----|------|
| 1 | Juiste variant kiezen: SU (Single User) of MU (Multi User) | [[Commercial Lead]] / [[Property Manager]] | Demarcatielijst AM-PROM-411 |
| 2 | Gebouw, Business Department en Maatschappij invullen | [[Commercial Lead]] | AM-PROM-411 |
| 3 | Standaardlijst aanpassen waar het contract afwijkt van de standaard | [[Property Manager]] | AM-PROM-411 |
| 4 | Verplichte keurings- en onderhoudsverslagen per onderdeel vastleggen | [[Property Manager]] | AM-PROM-411 |
| 5 | Demarcatielijst opnemen in [[Compliance-register]] (tabblad Demarcatielijst) | [[Property Manager]] | [[Compliance-register]] |

([[00_Sources/AM-PROM-411 Template demarcatielijst.xlsx]])

## Output
- Ingevulde demarcatielijst per gebouw/contract
- Basis voor [[Compliance-register]] (verantwoordelijkheden per onderdeel)

## RACI

| Stap | Responsible | Accountable | Consulted | Informed |
|------|-------------|-------------|-----------|---------|
| 1–5 | [[Property Manager]] | [[Property Manager]] | [[Commercial Lead]] | [[APM]] |

## Varianten

| Variant | Omschrijving |
|---------|-------------|
| SU (Single User) | Eén partij gebruikt het volledige gebouw |
| MU (Multi User) | Meerdere partijen; gemeenschappelijke delen altijd bij Eigenaar |

**Gemeenschappelijke delen (MU):** beheer (onderhoud, herstelling, vervanging, eigendom) steeds bij de Eigenaar (BAC). Kosten worden doorgerekend via rechargemechanisme. ([[00_Sources/AM-PROM-411 Template demarcatielijst.xlsx]])

## Hoofdstukken standaard demarcatielijst (15)

| Nr | Hoofdstuk |
|----|-----------|
| 1 | Buitenaanleg |
| 2 | Structuur |
| 3 | Gevelsluitingen |
| 4 | Dock-equipment (warehouse) |
| 5 | Dak (met / zonder PV-installatie) |
| 6 | Binnenafwerking |
| 7 | Brandbeschermingsmiddelen |
| 8 | Elektrische installaties |
| 9 | Security Technics |
| 10 | Data |
| 11 | Telefonie & Communicatie |
| 12 | Sanitair |
| 13 | HVAC |
| 14 | Diverse installaties |
| 15 | Privatieve Apron (incl. ruimtes rondom) |

([[00_Sources/AM-PROM-411 Template demarcatielijst.xlsx]])

## Tools
- Demarcatielijst AM-PROM-411 (Excel)
- [[Compliance-register]] AM-PROM-3Y2 (tabblad Demarcatielijst)

## KPI's
n.t.b.

## Raakvlakken
- [[Monitoren Verplichtingen]] — demarcatielijst bepaalt verantwoordelijkheden in het compliance-register
- [[Compliance Breach Logging]] — bij contractuele inbreuk
- [[Space Use Change]] — bij contractwijziging

## Open punten
n.t.b.

## Bronnen
- ([[00_Sources/AM-PROM-411 Template demarcatielijst.xlsx]]) — template demarcatielijst, eigenaar: Senior Process Manager AM Customer Care
- ([[00_Sources/AM-PROM-400 POL Demarcatielijst.pdf]]) — Policy, eigenaar: Senior Process Manager AM Customer Care
- ([[00_Sources/AM-PROM-410 PRO Toepassen demarcatie template.pdf]]) — Process Flow toepassen demarcatielijst-template, versie 25/06/2025, Ben Mariën
