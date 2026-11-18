---
type: process
niveau: L2
naam: Property Operations Compliance Control
status: draft
process_owner: n.t.b.
process_lead: n.t.b.
turtle_bron: n.t.b.
turtle_versie: n.t.b.
eigenaar: "[[Property Manager]]"
laatst_bijgewerkt: 2026-11-18
---

# Property Operations Compliance Control

## Doel
Continu bewaken dat gebruikers en BAC als Eigenaar hun contractuele en wettelijke verplichtingen nakomen, afwijkingen tijdig opvolgen en escaleren, en compliance-status per gebouw rapporteren als input voor gebruikersevaluatie en investeringsplanning.

## Trigger
- Vervaldatum van een verplichting nadert of verstreken
- Vastgestelde afwijking bij [[Periodieke Rondgang]] of eigen vaststelling
- Contractgebeurtenis (start/einde contract, fit-out)
- Signaal via HIF-ticket, AM Request of melding stakeholder

## Input
- [[Compliance-register]] per gebouw (AM-PROM-3Y2)
- Contract en [[Demarcatielijst]] (AM-PROM-411)
- Keurings- en onderhoudsverslagen van gebruiker en Eigenaar
- HIF-tickets (Maximo) en AM Requests (AMR SharePoint)

## Activiteiten

| Activiteit | Code | Eigenaar | Referentie |
|-----------|------|----------|-----------|
| [[Monitoren Verplichtingen]] | 3Y0 | [[Property Manager]] | SOP AM-PROM-3Y0 + WI AM-PROM-3Y1 |
| [[Periodieke Rondgang]] | 330 | [[Property Manager]] | SOP AM-PROM-330 + WI AM-PROM-331 |
| [[Compliance Breach Logging]] | 3X0 | [[Property Manager]] | SOP AM-PROM-3X0 + WI AM-PROM-3X1 |

## Output
- Actueel [[Compliance-register]] per gebouw
- Periodieke rapportage (compliance-status per rentable unit, KPI's)
- Gearchiveerde documenten in Bricsys/Forma
- Afgesloten compliance breaches in [[Breach Log]]
- Input voor PRM.1.1 (evaluatie tenants)

## RACI

| Activiteit | Responsible | Accountable | Consulted | Informed |
|-----------|-------------|-------------|-----------|---------|
| Monitoren Verplichtingen | [[Property Manager]] (of [[E&C]] bij MU) | [[Property Manager]] | [[APM]], [[Commercial Lead]], H&S | |
| Periodieke Rondgang | [[Property Officer]] | [[Property Manager]] | [[Commercial Lead]] | Gebruiker, [[APM]] |
| Compliance Breach Logging (Limited/Significant) | [[Property Manager]] | [[Property Manager]] | | [[Commercial Lead]] of [[APM]] |
| Compliance Breach Logging (Major/Critical) | [[APM]] | [[APM]] | [[Property Manager]] | [[Commercial Lead]] |

## Controls
- Ernst-escalatie bij gemist controlemoment (+1 niveau per gemist moment)
- Overdracht aan [[Compliance Breach Logging]] bij uitblijvende respons of veiligheidsrisico (één herinnering)
- Rapportage 3-maandelijks door [[Property Manager]] aan [[APM]] en [[Commercial Lead]]

## Tools
- [[Compliance-register]] (AM-PROM-3Y2) — per gebouw
- [[Breach Log]] (AM-PROM-3X2)
- [[Bricsys]] / [[Forma]] — archivering keurings- en onderhoudsverslagen
- HIF (Maximo) + AM Request (AMR SharePoint) — Eigenaar-verplichtingen

## KPI's

| KPI | Definitie | Target |
|-----|-----------|--------|
| % Overdue compliance actions | Open breaches waarvan hersteltermijn verstreken | TBD |
| % Compliance findings closed on time | Afgesloten breaches binnen hersteltermijn | TBD |
| Number of open (critical) compliance issues | Open breaches / waarvan Critical | TBD |
| % Overdue keuringsverslagen en onderhoudsrapporten | Gebruiker en Eigenaar | TBD |
| % rondgangen uitgevoerd volgens de planning | Rondgangen uitgevoerd in geplande maand / gepland in het jaar | TBD |
| PRM.1.1 — Evaluation of Tenants with Good Score | Gepland | TBD |

## Raakvlakken
- [[Asset Modification Request Handling]] — Eigenaar-acties via HIF/AMR
- [[Space Use Change]] — contractgebeurtenis triggert compliance-register update
- [[Patrimonium Data Beheer]] — afwijkende patrimoniumdata (rondgang C8)
- PRM.1.1 — compliance-score gebruiker als input evaluatie

## Open punten
- Turtle / L2-procesdiagram n.t.b. — zie [[60_OpenItems/OI-014 Turtle Property Operations Compliance Control]]
- Process Owner en Process Lead n.t.b.
- Herinneringstermijn n.t.b. — zie [[60_OpenItems/OI-007 Herinneringstermijn compliance-register]]
- Zie [[60_OpenItems/OI-012 PRM11 definitie compliance-score]]
- Zie [[70_Conflicts/CONF-004 Rol EC in compliance-register]]

## Bronnen
- ([[00_Sources/AM-PROM-3Y0 SOP Monitoren van contractuele en regelgevende verplichtingen.docx]])
- ([[00_Sources/AM-PROM-330 SOP Periodieke Rondgang.docx]])
- ([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]])
