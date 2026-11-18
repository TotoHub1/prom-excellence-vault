---
type: activity
code: AMR
proces: Asset Modification Request Handling
status: draft
sop: AM-PROM-100
wi: AM-PROM-101
eigenaar: "[[Property Manager]]"
laatst_bijgewerkt: 2026-11-18
---

# AMR Handling — Asset Modification Request Handling

## Doel
Alle Modification-gerelateerde vragen van (interne) klanten centraliseren op één plaats, correct routeren naar de bevoegde uitvoerende partij, en de uitvoering en klantfeedback consistent opvolgen. ([[00_Sources/AM-PROM-100 SOP Asset Modification Request Handling.docx]])

## Scope: drie klantstromen
Elke klantaanvraag volgt één van drie stromen:

| Stroom | Drempel | Kanaal |
|--------|---------|--------|
| **Modification** (AMR) | < €100.000 | AM Request (ASK) |
| **Project** | > €100.000 | Project Portfolio Review |
| **Complaint** | Storing/defect | HIF-ticket |

Deze SOP/WI is enkel van toepassing op de **Modification-stroom**.

## Request Types (AM Request)
Elke AM Request verplicht geclassificeerd bij indienen via het veld **Request Type** (5 types):

| Type | Beschrijving |
|------|-------------|
| Offerte | Prijsraming/kostenvoorstel vóór uitvoering |
| Werkaanvraag / Uitvoering Offerte | Uitvoering werken (rechtstreeks of na goedgekeurde Offerte) |
| Plaatsbeschrijving | Trigger voor [[Plaatsbeschrijving]]-activiteit |
| Facility | Kleine leveringen/meubilair, behandeld door Facility-team |
| Andere | Vragen buiten bovenstaande types |

> Zie [[70_Conflicts/CONF-005 Request Types SOP vs SharePoint-doc]] voor discrepantie met SharePoint-aanpassingsdoc (6 types incl. Advies).

## Trigger
Binnenkomende businessnood rond assets/infrastructuur/diensten binnen de Modification-stroom. ([[00_Sources/AM-PROM-100 SOP Asset Modification Request Handling.docx]])

## Input
- AM Request ingevuld door Requestor (Title, Description, Requestor BAC, Request Type verplicht)
- Optioneel: Attachment, Client, Priority, BLO, Budgetcode, Related Issues

## Stappen (WI AM-PROM-101)

| # | Stap | Actor | Tool |
|---|------|-------|------|
| 1 | Request indienen (Title, Description, Requestor BAC, Request Type; BLO+Budgetcode indien budget vereist) | Requestor | AM Request (ASK) |
| 2 | Dispatching: Handled By bepalen en invullen per BD (uitzondering: Facility → Handled by 'Facility') | [[HIF Back Office]] | AM Request |
| 3 | Metadata toevoegen: Client, BLO, Budgetcode, Issue ID in Title aanvullen | [[PROM]] | AM Request |
| 4 | Pre-gatekeeping analyse: volledigheid, maturiteit, duidelijkheid controleren; bijkomende info opvragen indien nodig; status → 'Ongoing' | [[PROM]] | AM Request |
| 5 | Aard identificatie: Run/Property (< €100k) of Build (> €100k)?  Bij twijfel: status → 'To Be Discussed', advies via [[AMCC]]. Build? → doorsturen naar Project Portfolio Review, status 'Closed'. | [[PROM]] | AM Request |
| 6 | Toewijzen verantwoordelijke: Assigned To invullen (Maintenance Manager voor Run, PROO voor Property); Asset Cluster invullen bij meerdere AM RUN-clusters | [[PROM]] | AM Request |
| 7 | Prioriteit bepalen (overleg PROM + Requestor + Uitvoerder): workload, urgentie, business impact, budget | [[PROM]] + Uitvoerder | AM Request |
| 8 | Opvolging uitvoering: wekelijkse werklijst (filter Handled By); tweewekelijkse AMR-meeting via [[PROM T&I]]; PROM-forum voor 'To Be Discussed', geel signaal, workloadconflict; escalatie naar [[APM]] bij rood signaal of vastgelopen afstemming | [[PROM]] + [[PROM T&I]] + [[APM]] | AM Request |
| 9 | Closing & feedback: klantfeedback opvragen, registreren in Comments/Feedback, status → 'Closed' of 'To Be Followed' | [[PROM]] | AM Request |
| 10 | PROM-datavelden aanvullen indien AM Request een ruimte deed ontstaan of renoveren: ServiceNow-ticket voor [[BIM Office]], Occupant + Classificatie + Name bijwerken in [[Airport View]] (zie [[Patrimonium Data Beheer]], situatie 2) | [[PROM]] + [[Data Clerk]] | [[Airport View]], [[ServiceNow]] |

## Opvolgings- en escalatiemodel

**Wekelijkse opvolging:** elke PROM raadpleegt eigen werklijst (filter Handled By, gegroepeerd per Request Status).

**Tweewekelijkse AMR-meeting** (gecoördineerd door [[PROM T&I]]):
- Requests met status 'Waiting for feedback requestor'
- Requests met geel signaal (45 dagen open)
- Requests met rood signaal (60 dagen open)

**PROM-forum** (wekelijks, [[AMCC]] aanwezig):
- Status 'To Be Discussed' → bespreken met AMCC
- Geel signaal na AMR-meeting → aangeven of onder controle
- Workload-/prioriteitsconflict → eerst onderlinge bespreking

**Escalatie naar [[APM]]** (3 gevallen):
1. Rood signaal (60 dagen) nadat PROM en Uitvoerder reeds hebben afgestemd
2. AMR-meeting 2x na elkaar niet doorgegaan (28 dagen)
3. Workload-/prioriteitsconflict niet opgelost op PROM-forum

APM neemt geëscaleerde requests mee in maandelijkse AMR KPI-review.

## Output
- AM Request in status 'Closed' (of 'To Be Followed') met geregistreerde klantfeedback
- Volledige lifecycle trace in AM Request SharePoint

## RACI

| Stap | Responsible | Accountable | Consulted | Informed |
|------|-------------|-------------|-----------|---------|
| 1 | Requestor | | | |
| 2 | [[HIF Back Office]] | | | |
| 3–9 | [[PROM]] | [[PROM]] | [[AMCC]], [[APM]], Uitvoerder | Requestor |
| 8 (coördinatie) | [[PROM T&I]] | | [[PROM]] | [[APM]] |
| 8 (escalatie) | [[APM]] | | | |
| 10 | [[PROM]] + [[Data Clerk]] | | [[BIM Office]] | |

## Tools
- [[AM Request]] (ASK SharePoint) — registratie, opvolging, afsluiting
- [[AM Cockpit]] (Tableau) — maandelijkse KPI-rapportage
- [[Airport View]] — PROM-datavelden bijwerken (stap 10)
- [[ServiceNow]] — BIM Office ticket voor tekening bijwerken (stap 10)

## KPI's

| KPI | Definitie | Target |
|-----|-----------|--------|
| IRM.1.1 | Service Request Performance: AM Requests + HIF Tickets binnen SLA | **90%** |
| IRM.2.1 | Change Requests (AMR): AM Requests binnen 60 dagen | **75%** |
| C&L-3 | Cargo & Logistics: AM Requests binnen 60 dagen (gefilterd BD C&L) | **75%** |
| CRE-3 | Commercial Real Estate: AM Requests binnen 60 dagen (gefilterd BD CRE) | **75%** |
| PAV-7 | Passenger Aviation: AM Requests binnen 60 dagen (gefilterd BD PAV) | **75%** |

Maandelijks gerapporteerd via SLA-AMR dashboard en [[AM Cockpit]].

## Raakvlakken
- [[Plaatsbeschrijving]] — Request Type 'Plaatsbeschrijving' triggert PLB-activiteit
- [[Patrimonium Data Beheer]] — stap 10 koppeling (Situatie 2: sluiten AM Request)
- [[Space Use Change]] — ruimtegerelateerde AMR's
- [[Periodieke Rondgang]] — Eigenaar-acties via HIF/AMR
- [[Monitoren Verplichtingen]] — Eigenaar-verplichtingen opvolgen via AMR

## Open punten
n.t.b.

## Bronnen
- ([[00_Sources/AM-PROM-100 SOP Asset Modification Request Handling.docx]]) — SOP, versie 14/07/2026, Toan Pauwels
- ([[00_Sources/AM-PROM-101 WI Asset Modification Request Handling.docx]]) — WI, versie 14/07/2026, Toan Pauwels
- ([[00_Sources/Asset Modification Request Handling Turtle.pptx]]) — procesturtle, versie 13/05/2026
- ([[00_Sources/AMR PROM Atelier (4).pptx]]) — PROM Atelier AMR
