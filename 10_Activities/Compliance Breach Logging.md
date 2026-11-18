---
type: activity
code: 3X0
proces: Property Operations Compliance Control
status: draft
sop: AM-PROM-3X0
wi: AM-PROM-3X1
eigenaar: "[[Property Manager]]"
laatst_bijgewerkt: 2026-11-18
---

# Compliance Breach Logging — Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers

## Doel
Registreren, opvolgen en afsluiten van compliance breaches door gebruikers (Maatschappijen en interne BAC-gebruikers) per Business Department, met escalatie op basis van ernst en herhaling. ([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]])

## Trigger
Een afwijking wordt een compliance breach indien:
1. Na herinnering niet opgelost
2. Veiligheidsrisico inhoudt (dan onmiddellijk, zonder herinnering)
3. Herhaling is binnen 12 maanden (voorstel, te valideren)
4. Als documentbreach overgedragen vanuit [[Monitoren Verplichtingen]] (AM-PROM-3Y0)

Een gewone afwijking (zonder bovenstaande kenmerken) wordt **niet** gelogd — standaard opvolging volstaat (één herinnering). ([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]])

## Input
- Vastgestelde afwijking uit [[Periodieke Rondgang]], eigen vaststelling [[Property Manager]], melding stakeholder, of overdracht van [[Monitoren Verplichtingen]]
- Referentie rondgangverslag of mail
([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]])

## Stappen

| # | Stap | Wie | Tool |
|---|------|-----|------|
| 1 | Registratie breach in [[Breach Log]] (datum, bron, gebouw, gebruiker, omschrijving, reden) | [[Property Manager]] | [[Breach Log]] |
| 2 | Ernst bepalen (Limited / Significant / Major / Critical) | [[Property Manager]] | [[Breach Log]] |
| 3 | Hersteltermijn + volgend controlemoment invullen | [[Property Manager]] | [[Breach Log]] |
| 4 | Kennisgeving sturen aan verantwoordelijke | [[Property Manager]] | [[Breach Log]] |
| 5 | Informeren [[Commercial Lead]] (Maatschappij) of [[APM]] (interne BAC-gebruiker) | [[Property Manager]] | [[Breach Log]] |
| 6 | Bij Major/Critical: overdragen aan [[APM]] | [[Property Manager]] / [[APM]] | [[Breach Log]] |
| 7 | Herstel verifiëren op volgend controlemoment | [[Property Manager]] / [[APM]] | [[Breach Log]] |
| 8 | Ernst bijwerken indien niet opgelost (ernst +1, ernsthistoriek invullen) | [[Property Manager]] / [[APM]] | [[Breach Log]] |
| 9 | Afsluiten breach (datum afsluiting = datum herstel) | [[Property Manager]] / [[APM]] | [[Breach Log]] |
| 10 | Compliance-register bijwerken | [[Property Manager]] | [[Compliance-register]] |

([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]])

## Output
- Afgesloten breach in [[Breach Log]] met datum afsluiting en uitkomst
- Bijgewerkt [[Compliance-register]]
- Input voor periodieke review met [[APM]] en voor PRM.1.1

## RACI

| Ernst | Responsible | Accountable | Consulted | Informed |
|-------|-------------|-------------|-----------|---------|
| Limited / Significant | [[Property Manager]] | [[Property Manager]] | | [[Commercial Lead]] (Maatschappij) of [[APM]] (BAC intern) |
| Major / Critical | [[APM]] | [[APM]] | [[Property Manager]] | [[Commercial Lead]] of stakeholders |
| Critical | [[APM]] | [[APM]] | | Beslist over risk register; eerst telefonisch |

([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]])

## Ernst en escalatielogica

| Ernst | Verantwoordelijk | Hersteltermijn | Wie geïnformeerd | Opvolging |
|-------|-----------------|----------------|-----------------|----------|
| Limited | [[Property Manager]] | **30 dagen** | CL (klant) of APM (BAC intern) | Standaard opvolging PROM |
| Significant | [[Property Manager]] | **15 dagen** | CL (klant) of APM (BAC intern) | Standaard opvolging PROM |
| Major | [[APM]] | **5 dagen** | CL (klant) | [[Property Manager]] volgt op |
| Critical | [[APM]] | **Onmiddellijk** | CL (klant); APM beslist over risk register | Eerst maatregel die gevaar wegneemt; telefonisch naar APM |

> Zie [[50_Decisions/DEC-005 Hersteltermijnen breach per ernst vastgelegd]]

**Ernststijging:** bij elk gemist controlemoment stijgt de ernst met 1 niveau. Noteren in ernsthistoriek (datum – wijziging – reden). ([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]])

## Tools
- [[Breach Log]] (AM-PROM-3X2) — tussentijdse Excel-template per Business Department
- [[Compliance-register]] (AM-PROM-3Y2) — bijwerken na afsluiting

## KPI's
- **% Overdue compliance actions** — open breaches waarvan hersteltermijn verstreken (streefwaarde: TBD)
- **% Compliance findings closed on time** — afgesloten breaches binnen hersteltermijn (streefwaarde: TBD)
- **Number of open (critical) compliance issues** — open breaches / waarvan Critical
([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]])

## Raakvlakken
- [[Periodieke Rondgang]] — voornaamste bron van breaches
- [[Monitoren Verplichtingen]] — documentbreaches worden overgedragen
- [[AMR Handling]] — herstelacties via HIF-ticket of [[AM Request]]
- PRM.1.1 — evaluatie tenants op basis van breach-data

## Open punten
- Hersteltermijnen vastgelegd — zie [[50_Decisions/DEC-005 Hersteltermijnen breach per ernst vastgelegd]] ([[60_OpenItems/OI-005 Hersteltermijnen per ernst]] gesloten)
- Zie [[60_OpenItems/OI-006 Definitieve tool breach log]]
- Periode herhaling (12 maanden — voorstel, nog te valideren)

## Bronnen
- ([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]]) — template breach log, eigenaar: Toan Pauwels
- ([[00_Sources/Compliance breaches - PROM Atelier (5).pptx]]) — PROM Atelier Compliance Breaches, 20/10
