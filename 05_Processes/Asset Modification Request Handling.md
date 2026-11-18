---
type: process
niveau: L2
naam: Asset Modification Request Handling
status: draft
process_owner: n.t.b.
process_lead: n.t.b.
turtle_bron: "[[00_Sources/Asset Modification Request Handling Turtle.pptx]]"
turtle_versie: 13/05/2026
eigenaar: n.t.b.
laatst_bijgewerkt: 2026-11-18
---

# Asset Modification Request Handling

## Doel
Alle Modification-gerelateerde vragen van (interne) klanten centraliseren op één plaats, correct routeren naar de bevoegde uitvoerende partij, en de uitvoering en klantfeedback consistent opvolgen. ([[00_Sources/Asset Modification Request Handling Turtle.pptx]])

## Scope: drie klantstromen

| Stroom | Drempel | Kanaal |
|--------|---------|--------|
| **Modification** (AMR) | < €100.000 | AM Request (ASK) |
| **Project** | > €100.000 | Project Portfolio Review |
| **Complaint** | Storing/defect | HIF-ticket |

([[00_Sources/Asset Modification Request Handling Turtle.pptx]])

## Trigger
Binnenkomende businessnood rond assets, infrastructuur of diensten van een (interne) klant. ([[00_Sources/Asset Modification Request Handling Turtle.pptx]])

## Input
- Klantaanvraag via AM Request (Modification-stroom), Project Portfolio Review (Project-stroom) of HIF-ticket (Complaint-stroom)
- Klant- en contractgegevens
- Asset- en locatiegegevens
([[00_Sources/Asset Modification Request Handling Turtle.pptx]])

## Activiteiten

| Activiteit | Van toepassing op stroom | Referentie |
|-----------|--------------------------|-----------|
| [[AMR Handling]] (AM-PROM-100/101) | Modification | SOP + WI |
| Project Portfolio Review | Project | n.t.b. |
| [[Plaatsbeschrijving]] (AM-PROM-310/311) | Modification (PLB-trigger) | SOP + WI |
| [[Patrimonium Data Beheer]] (AM-PROM-130) | Modification (na uitvoering) | SOP + WI |

([[00_Sources/Asset Modification Request Handling Turtle.pptx]])

## Output
- AM Request in status 'Closed' met geregistreerde klantfeedback (Modification-stroom)
- Klantaanvraag gerouteerd naar bevoegde partij (Project- of Complaint-stroom)
- Bijgewerkte [[Patrimonium Data Beheer|patrimoniumdata]] in [[Airport View]] na ruimtewijziging
([[00_Sources/Asset Modification Request Handling Turtle.pptx]])

## RACI

| Stroom | Responsible | Accountable | Consulted | Informed |
|--------|-------------|-------------|-----------|---------|
| Modification | [[PROM]] | [[PROM]] | [[AMCC]], [[APM]], Uitvoerder | Requestor |
| Dispatching | [[HIF Back Office]] | | | |
| Project | n.t.b. | | | |
| Complaint | n.t.b. | | | |

## Controls
n.t.b. ([[00_Sources/Asset Modification Request Handling Turtle.pptx]])

## Tools
- [[AM Request]] (ASK SharePoint) — Modification-stroom
- [[AM Cockpit]] (Tableau) — maandelijkse KPI-rapportage
- [[Airport View]] — patrimoniumdata na uitvoering
- [[ServiceNow]] — BIM Office ticket
([[00_Sources/Asset Modification Request Handling Turtle.pptx]])

## KPI's

| KPI | Definitie | Target |
|-----|-----------|--------|
| IRM.1.1 | Service Request Performance: AM Requests + HIF Tickets binnen SLA | **90%** |
| IRM.2.1 | Change Requests (AMR): AM Requests binnen 60 dagen | **75%** |
| C&L-3 | Cargo & Logistics: AM Requests binnen 60 dagen | **75%** |
| CRE-3 | Commercial Real Estate: AM Requests binnen 60 dagen | **75%** |
| PAV-7 | Passenger Aviation: AM Requests binnen 60 dagen | **75%** |

Maandelijks gerapporteerd via SLA-AMR dashboard en [[AM Cockpit]]. ([[00_Sources/Asset Modification Request Handling Turtle.pptx]])

## Raakvlakken
- [[Space Use Change]] — ruimtegerelateerde AMR's
- [[Space Planning Terminal]]
- [[Periodieke Rondgang]] — Eigenaar-acties via HIF/AMR
- [[Monitoren Verplichtingen]] — Eigenaar-verplichtingen opvolgen via AMR

## Open punten
- Process Owner en Process Lead n.t.b. — zie [[00_Sources/Asset Modification Request Handling Turtle.pptx]]
- Zie [[70_Conflicts/CONF-005 Request Types SOP vs SharePoint-doc]] — 5 vs. 6 request types

## Bronnen
- ([[00_Sources/Asset Modification Request Handling Turtle.pptx]]) — procesturtle, versie 13/05/2026
- ([[00_Sources/AM-PROM-100 SOP Asset Modification Request Handling.docx]]) — SOP activiteitsniveau
- ([[00_Sources/AMR PROM Atelier (4).pptx]]) — PROM Atelier AMR
