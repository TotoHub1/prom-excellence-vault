---
type: activity
code: 3Y0
proces: Property Operations Compliance Control
status: draft
sop: AM-PROM-3Y0
wi: AM-PROM-3Y1
eigenaar: "[[Property Manager]]"
laatst_bijgewerkt: 2026-11-18
---

# Monitoren Verplichtingen — Monitoren van contractuele en regelgevende verplichtingen

## Doel
Per gebouw een actueel overzicht bijhouden van alle verplichtingen van de gebruiker en van BAC als Eigenaar, en opvolgen dat ze worden nagekomen. Afwijkingen opvolgen tot ze opgelost of overgedragen zijn aan [[Compliance Breach Logging]]. Input leveren voor de evaluatie van gebruikers (PRM.1.1). ([[00_Sources/AM-PROM-3Y0 SOP Monitoren van contractuele en regelgevende verplichtingen.docx]])

De [[Periodieke Rondgang]] (AM-PROM-330) is een procesvariant van deze activiteit: dezelfde regels (register, controlepunten, beslisregels, herinnering, overdracht, rapportering) gelden ook tijdens de rondgang.

## Scope
- **Single user (SU):** [[Property Manager]] voert alle stappen zelf uit.
- **Multi user (MU):** [[E&C]] voert stap 1–4 uit voor de Maatschappijen en rapporteert aan de [[Property Manager]], die monitort via E&C.

## Trigger
1. **Tijdsgebonden:** vervaldatum van een verplichting nadert of verstreken
2. **Document ontvangen:** keurings-/onderhoudsverslag van gebruiker, rapportering E&C, of afgesloten HIF-ticket/AM Request
3. **Contractgebeurtenis:** start of einde contract (met PLB, AM-PROM-310), fit-out door gebruiker
4. **Periodieke rondgang:** documentaire afwijking uit voorbereiding of fysieke vaststellingen (AM-PROM-330)
5. **Signaal:** HIF-ticket, AM Request of compliance breach die wijst op ontbrekend/vervallen document

## Input
- [[Compliance-register]] per gebouw (AM-PROM-3Y2)
- Contract en [[Demarcatielijst]] (AM-PROM-411)
- Keurings- en onderhoudsverslagen van gebruiker en Eigenaar
- HIF-tickets (Maximo) en AM Requests (AMR SharePoint)

## Stappen (WI AM-PROM-3Y1)

| # | Stap | Actor | Tool |
|---|------|-------|------|
| 1 | Compliance-register bijhouden: verplichtingen vastleggen per gebouw (document-type, verantwoordelijke, periodiciteit, vervaldatum, status); bijwerken bij contractwijziging, fit-out of nieuwe wetgeving | [[Property Manager]] (E&C bij MU) | [[Compliance-register]] |
| 2 | Documenten opvolgen en opvragen: register periodiek nakijken op vervaldata; ontvangen documenten registreren; verplichting gebruiker → schriftelijk opvragen met termijn (= herinnering); verplichting Eigenaar → status HIF/AMR controleren of nieuw aanmaken | [[Property Manager]] (E&C bij MU) | [[Compliance-register]], Outlook, Maximo, AMR SharePoint |
| 3 | Documenten reviewen: elk ontvangen document toetsen aan 6 controlepunten; status in register invullen (conform / conform met opmerkingen / niet conform); twijfel → advies H&S | [[Property Manager]] (E&C bij MU) | [[Compliance-register]] |
| 4 | Afwijkingen opvolgen: gebruiker verantwoordelijk → schriftelijk herstel + bewijs vragen (één herinnering); Eigenaar verantwoordelijk → HIF-ticket (defect) of AM Request (planbare actie); bij veiligheidsrisico: onmiddellijk actie | [[Property Manager]] (E&C bij MU) | [[Compliance-register]], HIF, AMR SharePoint |
| 5 | Overdragen aan Breach Logging: gebruikersafwijking na termijn niet opgelost, of veiligheidsrisico → overdragen aan AM-PROM-3X1 stap 1 (gebouw, gebruiker, document/vaststelling, datum herinnering, bewijs); referentie in register noteren | [[Property Manager]] | [[Breach Log]], [[Compliance-register]] |
| 6 | Archiveren en rapporteren: gereviewde documenten archiveren in Bricsys/Forma; register bijwerken; periodiek compliance-status per gebouw rapporteren aan [[APM]] en [[Commercial Lead]] (input PRM.1.1) | [[Property Manager]] | Bricsys/Forma, [[Compliance-register]] |

## Controlepunten bij documentreview (stap 3, en documentaire voorbereiding rondgang)

| Punt | Vraag |
|------|-------|
| A — Aanwezig en tijdig | Ontvangen vóór de vervaldatum in het register? |
| B — Juist onderwerp | Juiste gebouw en gebouwonderdeel uit de demarcatielijst? |
| C — Bevoegde uitvoerder | Erkend keuringsorganisme (keuringsverslag) of bevoegde firma/technicus (onderhoudsverslag)? |
| D — Geldigheid | Datum volgende keuring/onderhoud vermeld en binnen termijn? |
| E — Conformiteitsoordeel | Conform, conform met opmerkingen of niet conform? |
| F — Opmerkingen | Herstelpunten aanwezig, en met welke hersteltermijn? |

**Na de review:**
- Conform → status in register, document archiveren (stap 6)
- Conform met opmerkingen → herstelpunten opvolgen met termijn (stap 4)
- Niet conform → afwijking opvolgen beslisregels (stap 4)

## Beslisregels bij afwijkingen (stap 4–5)

| Situatie | Actie |
|----------|-------|
| Document/herstel ontbreekt — gebruiker | Eén herinnering met termijn. Blijft het uit → overdragen aan AM-PROM-3X0 (stap 5). |
| Niet-conformiteit ter plaatse — gebruiker | Herstel en bewijs vragen (één herinnering). Geen herstel binnen termijn → overdragen. |
| Afwijking met veiligheidsrisico — gebruiker | Onmiddellijk overdragen aan AM-PROM-3X0, zonder herinnering. |
| Afwijking — Eigenaar (BAC) | Geen breach: HIF-ticket (defect) of AM Request (planbare actie), opvolgen; AM Request vastgelopen → escalatiemodel AM-PROM-100. |
| Afwijking met veiligheidsrisico — Eigenaar | Geen breach: onmiddellijk HIF-ticket hoge prioriteit + APM telefonisch informeren. |
| Multi user: E&C lost afwijking niet op in termijn, of rapportering E&C ontbreekt | Property Manager draagt over aan AM-PROM-3X0. |

## Document-types (Bijlage A, SOP AM-PROM-3Y0)

| Document-type | Aard | Frequentie |
|--------------|------|-----------|
| Keuringsverslag | Wettelijk | Per installatie (AREI, liften, brandmelding…) |
| Onderhoudsverslag en -attest | Wettelijk of contractueel | Wetgeving / fabrieksvoorschriften |
| Verslag evacuatieoefening | Wettelijk | Minstens jaarlijks |
| Onderhoudsplan | Contractueel | Volgens contract |
| Vergunningen en dossiers | Wettelijk | Eenmalig of bij wijziging |
| Andere wettelijke verplichtingen | Wettelijk | Volgens verplichting |
| Contractuele verplichtingen | Contractueel | Volgens contract |

Totaal: 120+ standaardregels in het [[Compliance-register]] (CR-001 t/m CR-120+), uitbreidbaar per gebouw.

## Status-waarden in het compliance-register

| Status | Betekenis |
|--------|----------|
| Te bepalen | n.t.b. |
| Ontbrekend | Geen datum of document ontvangen |
| Vervallen | Vervaldatum vóór rapportdatum |
| Vervalt binnenkort | Binnen signaaltermijn (aanname 60 dagen) |
| Geldig | Geldig document aanwezig |
| Aanwezig | Eenmalig document zonder vervaldatum |

**Status verplichting:**
- Niet in orde = ontbrekend, vervallen of niet-conform
- In orde met aandachtspunten = vervalt binnenkort of conform met opmerkingen
- In orde = geldig/aanwezig en conform

## Output
- Actueel [[Compliance-register]] per gebouw
- Periodieke rapportage (compliance-status per rentable unit, KPI's)
- Gearchiveerde documenten in Bricsys/Forma
- Afwijkingen opgelost of overgedragen aan [[Compliance Breach Logging]]
- Input voor PRM.1.1 (evaluatie tenants)

## RACI

| Stap | Responsible | Accountable | Consulted | Informed |
|------|-------------|-------------|-----------|---------|
| 1–6 | [[Property Manager]] | [[Property Manager]] | [[APM]], [[Commercial Lead]], H&S | |
| Multi user | [[E&C]] (stap 1–4) | [[Property Manager]] | | |

## Tools
- [[Compliance-register]] (AM-PROM-3Y2) — per gebouw, eigenaar: [[Property Manager]]
- [[Bricsys]] / [[Forma]] — archivering keurings- en onderhoudsverslagen
- HIF (Maximo) + AM Request (AMR SharePoint) — Eigenaar-verplichtingen
- Outlook — e-mail per BD (AMproperty@brusselsairport.be)

## KPI's
- **% Overdue keuringsverslagen en onderhoudsrapporten** (gebruiker en Eigenaar) — target TBD
- **% afwijkingen van de gebruiker opgelost na herinnering** (zonder overdracht aan Breach Logging) — target TBD
- **PRM.1.1 — Evaluation of Tenants with Good Score** (gepland) — target TBD

Rapportage: 3-maandelijks door [[Property Manager]] aan [[APM]] en [[Commercial Lead]].

## Raakvlakken
- [[Compliance Breach Logging]] — bij uitblijvende respons of veiligheidsrisico (AM-PROM-3X0)
- [[Periodieke Rondgang]] — gedeeld register; rondgang = procesvariant
- [[Demarcatielijst]] — bepaalt verantwoordelijkheid per onderdeel
- [[AMR Handling]] — Eigenaar-acties via HIF/AMR, escalatiemodel AM-PROM-100
- PRM.1.1 — compliance-score gebruiker als input evaluatie

## Open punten
- Zie [[60_OpenItems/OI-007 Herinneringstermijn compliance-register]]
- Rol van [[E&C]] in het bijhouden van het register (multi user) n.t.b. — zie [[70_Conflicts/CONF-004 Rol EC in compliance-register]]
- Definitie PRM.1.1 en drempel voor 'goede score' n.t.b. — zie [[60_OpenItems/OI-012 PRM11 definitie compliance-score]]
- Herinneringstermijn: n.t.b. in AM-PROM-3Y0

## Bronnen
- ([[00_Sources/AM-PROM-3Y0 SOP Monitoren van contractuele en regelgevende verplichtingen.docx]]) — SOP, versie 09/10/2026, Toan Pauwels
- ([[00_Sources/AM-PROM-3Y1 WI Monitoren van contractuele en regelgevende verplichtingen.docx]]) — WI, versie 13/10/2026, Toan Pauwels
- ([[00_Sources/AM-PROM-3Y2 Template Compliance-register.xlsx]]) — template compliance-register, eigenaar: Toan Pauwels
- ([[00_Sources/PROM Atelier — Monitoren van contractuele en regelgevende verplichtingen (8).pptx]]) — PROM Atelier 17/11/2026
