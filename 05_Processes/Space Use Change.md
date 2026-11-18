---
type: process
niveau: L2
naam: Space Use Change
status: draft
process_owner: "[[Sr Process Manager AMCC]]"
process_lead: BD/ED PROM
turtle_bron: "[[00_Sources/Space Use Change Turtle New.pptx]]"
turtle_versie: 15/06/2026
eigenaar: "[[Sr Process Manager AMCC]]"
laatst_bijgewerkt: 2026-11-18
---

# Space Use Change

## Doel
Tijdige, accurate en conforme ruimtetoewijzing aan gebruiker, afgestemd op bedrijfsbehoeften, met behoud van data-integriteit in alle systemen. ([[00_Sources/Space Use Change Turtle New.pptx]])

## Trigger
Ruimteaanvraag of ruimtewijziging van: externe klant, BLO Tender, AM Klant, IT Klant of PM. ([[00_Sources/Space Use Change Turtle New.pptx]])

## Input
- Klant- en contractgegevens
- Ruimtegegevens
- Architecturale plannen van Build & Project
- Technische ruimtegegevens van [[BIM Office]] (bv. ID, m²)
- Beleids- en classificatieregels
([[00_Sources/Space Use Change Turtle New.pptx]])

## Activiteiten

| # | Activiteit | Wie | Tool |
|---|-----------|-----|------|
| 1 | [[Terminal Space Management]] | [[PROM]] | [[Airport View]] |
| 2 | [[Plaatsbeschrijving]] (ingaande of uitgaande [[PLB]] & sleuteloverdracht) | [[PROM]] | [[AM Request]] |
| 3 | [[Patrimonium Data Beheer]] | [[PROM]], [[Data Clerk]], [[BIM Office]] | [[Airport View]] |

([[00_Sources/Space Use Change Turtle New.pptx]])

## Output
1. Ondertekend contract in [[AX]] / [[Planon]]
2. Data & systemen:
   - 2D-plattegronden op gebouw-, verdiepings- en premiseniveau met bijhorende kenmerken in [[Airport View]] (bv. ID, m², deurnummer, kamernummer, naam, contractreferentie, observatie, classificatie)
   - [[Airport View]] is momenteel het primair referentiepunt voor ruimtelijke consultatie
   - Gevalideerde ruimte- en contractclassificatie
3. Operationeel:
   - Ruimte operationeel beschikbaar of ingenomen
   - Overdracht (sleutels, [[PLB]])
([[00_Sources/Space Use Change Turtle New.pptx]])

## RACI

| Activiteit | Responsible | Accountable | Consulted | Informed |
|-----------|-------------|-------------|-----------|---------|
| 1–3 | [[PROM]] | n.t.b. | [[Commercial Lead]], [[APM]] | |
| 3 | [[PROM]], [[Data Clerk]], [[BIM Office]] | n.t.b. | | |

## Controls
n.t.b. ([[00_Sources/Space Use Change Turtle New.pptx]])

## Tools
- [[Airport View]] — primair systeem ruimtelijke data
- [[Planon]] — contractbeheer (transitie lopend)
- [[AX]] — contractbeheer (huidig)
- [[AM Request]] — aanvraagregistratie
- [[ServiceNow]] — gegevenscorrectie aanvragen
- CAD Tools ([[BIM Office]])
- GIS Tools (GIS Team)
([[00_Sources/Space Use Change Turtle New.pptx]])

## KPI's
Alle KPI's beschreven maar **niet actief**. ([[00_Sources/Space Use Change Turtle New.pptx]])
- [[Patrimonium Data Beheer]]: Tijdigheid, Volledigheid, Correctiegraad bij follow-up-controles
- [[PLB]]: Overall Lead Time, Volume, Workload Distribution

## Raakvlakken
- [[Space Planning Terminal]]
- [[Asset Modification Request Handling]]
- BIM Office (geometrie & feature checks)
- GIS Team

## Open punten
- Zie [[60_OpenItems/OI-001 KPIs Space Use Change niet actief]]
- Zie [[60_OpenItems/OI-002 Platformtransitie Planon-Maximo-AV]]
- Zie [[60_OpenItems/OI-003 Toegangsrechten Airport View]]
- Zie [[60_OpenItems/OI-004 Premises niet in contract zichtbaar]]
- Zie [[70_Conflicts/CONF-001 Rolafbakening Commercial Lead vs Property Manager]]
- Zie [[70_Conflicts/CONF-002 Premise vs Rentable Unit definitie]]

## Bronnen
- ([[00_Sources/Space Use Change Turtle New.pptx]]) — versie 15/06/2026, Process Owner: Sr Process Manager AMCC, Process Lead: BD/ED PROM
