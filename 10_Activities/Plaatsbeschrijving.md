---
type: activity
code: 310
proces: Space Use Change
status: draft
sop: AM-PROM-310
wi: AM-PROM-311
eigenaar: "[[Property Manager]]"
laatst_bijgewerkt: 2026-11-18
---

# Plaatsbeschrijving

## Doel
Twee types PLB, elk met een eigen doel:
1. **PLB bij terbeschikkingstelling (Flow A):** staat van een ruimte/gebouw formeel vastleggen bij in-/uitgang van een externe klant; alle partijen beschermen tegen niet-waarheidsgetrouwe schadeclaims.
2. **PLB bij oplevering van een project (Flow B):** nagaan of het project effectief is opgeleverd zoals initieel verwacht/gepland (Gate 4B – Start-to-operate). Altijd door externe firma.

([[00_Sources/AM-PROM-310 SOP Plaatsbeschrijving.docx]])

## Trigger
- **Flow A:** AM Request van het type 'Plaatsbeschrijving', ingediend door de [[Commercial Lead]].
- **Flow B:** Start-to-operate Nota bij Gate 4B (C&S Gate), aangevraagd door de Technical Lead. Geen AM Request.

## Beslissingen
- [[50_Decisions/DEC-003 PLB standaard extern uitbesteed]] — terbeschikkingstelling PLB standaard extern uitbesteed
- [[50_Decisions/DEC-004 PLB budgettaire verantwoordelijkheid CL]] — [[Commercial Lead]] is budgetverantwoordelijk

---

## Flow A — PLB bij terbeschikkingstelling aan een klant

**Trigger:** AM Request type 'Plaatsbeschrijving' door [[Commercial Lead]].
**Uitvoerder:** [[Property Officer]] (intern) of externe landmeter (standaard, zie DEC-003).

### Stappen (WI AM-PROM-311, Flow A)

| # | Stap | Actor | Tool |
|---|------|-------|------|
| 1 | Aanvraag ontvangen (AM Request type 'PLB' van CL) | [[Property Officer]] | AM Request |
| 2 | Intern of extern bepalen (standaard extern; intern enkel bij kleine PLB, contractueel anders bepaald of uitzondering) | [[Property Officer]] | — |
| 3 | Afspraak en voorbereiding (bij intern): klant uitnodigen, badge regelen, sleutels via Keyservices, eventueel voorbereidend bezoek | [[Property Officer]] | — |
| 4 | Plaatsbeschrijving uitvoeren (per ruimte: plafond/wanden/deuren/vloer; foto's, staat, schade; uitrustingen; meterstanden; sleutels; kostenraming bij uitgaande PLB via BAC-catalogus) | [[Property Officer]] of externe landmeter | PLB-template AM-PROM-311a |
| 5 | Ondertekening: finale versie via ondertekeningstool naar klant; na klantondertekening ondertekent CL; volledig ondertekend verslag naar PROO | [[Commercial Lead]] | Ondertekeningstool |
| 6 | Administratieve opvolging: CL stelt AM Request(en) op voor werkpunten; CL voegt ondertekend verslag als bijlage toe aan contract in Icertis (via contract management); PROO slaat kopie op in Bricsys | [[Commercial Lead]] + [[Property Officer]] | Icertis, [[Bricsys]] |
| 7 | Externe uitbesteding (indien van toepassing): PROO registreert PLB-aanvragen en mailt door naar externe landmeter; landmeter plant afspraak, voert PLB uit en levert digitaal ondertekend verslag; BAC verzorgt archivering (stap 6) | [[Property Officer]] + externe landmeter | — |
| 8 | PROM-datavelden aanvullen: bij uitgaande PLB Occupant bijwerken in Airport View (verhuurbaarheid) | [[Property Manager]] | [[Airport View]] |

### Rolverschuiving t.o.v. vorige werkwijze

| Taak | Vorig | Nieuw |
|------|-------|-------|
| Budget voorzien | Onduidelijk | [[Commercial Lead]] |
| Uitvoering | Per dossier intern/extern | Standaard extern |
| Ondertekening | Manueel door PROM | Via ondertekeningstool door CL |
| Archivering contract | — | CL in Icertis |
| Archivering PROM | PROM in Bricsys | PROM in Bricsys (ongewijzigd) |
| AM Request werkpunten | PROM | [[Commercial Lead]] |

---

## Flow B — PLB bij oplevering van een project (Gate 4B)

**Trigger:** Start-to-operate Nota bij Gate 4B, aangevraagd door Technical Lead.
**Uitvoerder:** altijd externe firma (nooit intern door PROO).
**Verschil met Flow A:** geen kostenraming, geen ondertekening door klant, toegevoegd aan Start-to-operate Nota.

### Stappen (WI AM-PROM-311, Flow B)

| # | Stap | Actor | Tool |
|---|------|-------|------|
| 1 | Aanvraag: Technical Lead identificeert nood aan PLB bij Gate 4B; neemt rechtstreeks contact op met externe firma | Technical Lead | Start-to-operate Nota |
| 2 | Afspraak en voorbereiding: externe firma plant afspraak met TL en betrokken partijen; verzamelt projectdocumentatie (programma van eisen, opleveringsvereisten) | Externe firma | — |
| 3 | PLB uitvoeren: per ruimte/onderdeel vastleggen of conform opgeleverd; afwijkingen fotograferen; **geen kostenraming** | Externe firma | PLB-template |
| 4 | Afronding: PLB ondertekenen; bezorgen aan Technical Lead die ondertekent en toevoegt aan Start-to-operate Nota (Gate 4B) | Externe firma / Technical Lead | Start-to-operate Nota |
| 5 | Archivering: TL uploadt Start-to-operate Nota met PLB in Bricsys/Forma | Technical Lead | [[Bricsys]] / [[Forma]] |
| 6 | PROM-datavelden aanvullen: PM vult Occupant en eventueel Observation in Airport View in (Situatie 1, AM-PROM-130) | [[Property Manager]] + [[Data Clerk]] | [[Airport View]] |

---

## Output
- **Flow A:** ondertekende PLB, gearchiveerd in Bricsys (PROM) en Icertis (CL via contract management); AM Requests voor werkpunten opgesteld door CL
- **Flow B:** PLB toegevoegd aan Start-to-operate Nota, gearchiveerd in Bricsys/Forma

## RACI

| Stap | Responsible | Accountable |
|------|-------------|-------------|
| Flow A — organisatie/uitvoering | [[Property Officer]] of externe landmeter | [[Commercial Lead]] (opdrachtgever, budget) |
| Flow A — ondertekening/admin | [[Commercial Lead]] | [[Commercial Lead]] |
| Flow B — uitvoering | Externe firma | Technical Lead (opdrachtgever) |
| Beide flows — PROM-datavelden | [[Property Manager]] | [[APM]] |

## Tools
- PLB-template AM-PROM-311a (Word)
- [[Airport View]] — plan toevoegen, PROM-datavelden bijwerken (stap 8/6)
- Ondertekeningstool — digitale ondertekening (Flow A, stap 5)
- Icertis — contractarchivering PLB (CL, Flow A)
- [[Bricsys]] / [[Forma]] — archivering PROM (Flow A) en projectoplevering (Flow B)
- Start-to-operate Nota — Gate 4B (Flow B)

## KPI's (Flow A, via AM Request)
- **Overall Lead Time** — gemiddeld aantal kalenderdagen Request type 'PLB' van 'New' naar 'Closed' (target TBD)
- **Volume** — aantal PLB-requests per maand (target TBD)
- **Workload Distribution** — aantal PLB-requests per PROM per maand (target TBD)

## Raakvlakken
- [[AMR Handling]] — Request Type 'Plaatsbeschrijving' triggert Flow A
- [[Patrimonium Data Beheer]] — stap 8 (Flow A) en stap 6 (Flow B) triggeren datavelden
- [[Space Use Change]] — PLB is onderdeel van stap 2
- [[Monitoren Verplichtingen]] — vorige PLB als brondocument voor compliance-register

## Open punten
n.t.b.

## Bronnen
- ([[00_Sources/AM-PROM-310 SOP Plaatsbeschrijving.docx]]) — SOP, versies 07/07/2026 en 27/07/2026, Toan Pauwels
- ([[00_Sources/AM-PROM-311 WI Plaatsbeschrijving.docx]]) — WI, versies 07/07/2026, 27/07/2026 en 28/09/2026, Toan Pauwels
- ([[00_Sources/AM-PROM-311a TEMP Plaatsbeschrijving  (1).docx]]) — PLB-template
- ([[00_Sources/PROM Atelier PLB (8).pptx]]) — PROM Atelier PLB, 11/08
