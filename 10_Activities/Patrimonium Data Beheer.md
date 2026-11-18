---
type: activity
code: 130
proces: Space Use Change
status: draft
sop: AM-PROM-130
wi: AM-PROM-130
eigenaar: "[[Property Manager]]"
laatst_bijgewerkt: 2026-11-18
---

# Patrimonium Data Beheer — Beheren van Patrimonium Datavelden

## Doel
De vier PROM-eigen datavelden (Occupant, Name, Classificatie, Observation) van ruimtes in [[Airport View]] actueel, correct en conform bijhouden, zodat ze de werkelijke situatie weerspiegelen en als basis dienen voor tijdige en accurate ruimtetoewijzing (verhuurbaarheid, facturatie). ([[00_Sources/AM-PROM-130 SOP Patrimonium Data Beheer.docx]])

## Scope
Van toepassing op alle PROM-eigen datavelden van ruimtes in eigendom van BAC, op premiseniveau in Airport View (GIS-tool, geen PM- of commerciële tool). De [[Property Manager]] is eigenaar en uitvoerder binnen zijn/haar Business Domain.

## De 4 PROM-datavelden

| Veld | Definitie | Geldige waarden / bron |
|------|-----------|------------------------|
| **Occupant** | Huidige gebruiker van een ruimte; bepaalt de verhuurbaarheid. | Glossary Occupant: Brussels Airport Company · Leeg Zonder Contract · Leeg Verhuurbaar · Leeg Niet Verhuurbaar · Leeg Nooit Verhuurbaar. Normaal automatisch gevuld vanuit commercieel contract in AX. |
| **Name** | Specifieke naam van een ruimte (bv. 'MRC 2.03'). | Vrije tekst (conform naamconventie) |
| **Classificatie** | Fysieke classificatie van de ruimte op basis van brandveiligheid (4 subvelden: Code, Grp, Classification, Detail). | AM-PROM-REF Legende Classificatie; conform wettelijk kader brandveiligheid (AM-PROM-120) |
| **Observation** | Verwachte/gereserveerde toekomstige gebruiker vóór contractondertekening. | Naam van de kandidaat-gebruiker; leegmaken bij contractondertekening |

## Triggers per situatie

### Situatie 1 — Premise ontstaat uit een project (Gate 4B Start-to-operate)

| Veld | Trigger | Actor | Systeem |
|------|---------|-------|---------|
| Classificatie | Gate 4B | [[BIM Office]] / Project Manager | Airport View |
| Observation | Plaatsbeschrijving (flow B) | [[Property Manager]] | Airport View |
| Occupant | Plaatsbeschrijving (flow B) | [[Property Manager]] | Airport View |
| Visuele tekening | Gate 4B | Project Manager | ServiceNow + Airport View |

### Situatie 2 — Premise bestaat reeds of ontstaat/wordt gerenoveerd via AM Request

| Veld | Trigger | Actie | Actor |
|------|---------|-------|-------|
| Observation | Ruimteaanvraag klant (vóór contract) | Veld invullen | [[Property Manager]] |
| Observation | Contractondertekening | Veld leegmaken | [[Property Manager]] |
| Occupant | Uitgaande plaatsbeschrijving (flow A, stap 8) | Veld invullen | [[Property Manager]] |
| Occupant | Sluiten AM Request (AMR-stap 10) | Veld invullen | [[Property Manager]] |
| Classificatie | Sluiten AM Request (AMR-stap 10) | Veld invullen | [[Property Manager]] |
| Name | Sluiten AM Request (AMR-stap 10) | Veld invullen | [[Property Manager]] |

## Stappen WI per veld (AM-PROM-130 WI)

### Veld 1 — Occupant (Actor: Property Manager)
1. Ga in Airport View naar 'Choose location' of 'Find known asset' voor het juiste lokaal.
2. Ga naar 'Add Assets' → 'Building Activities' → 'Maintenance'; vink laag 'Premises for Editor' aan.
3. Controleer het onderliggende veld voor Occupant ('tenant'): normaal automatisch gevuld vanuit AX-contract.
4. Geen actieve huurder of manuele aanpassing nodig? Vul één geldige waarde in (Glossary Occupant).
5. Sla op.

### Veld 2 — Name (Actor: Property Manager)
1. Ga in Airport View naar het juiste lokaal.
2. Ga naar 'Add Assets' → 'Building Activities' → 'Maintenance'; vink laag 'Premises for Editor' aan.
3. Vul het veld 'name' in de pop-up in met de specifieke naam van het lokaal (bv. 'MRC 2.03').
4. Sla op.

### Veld 3 — Classificatie (Code, Grp, Classification, Detail) (Actor: Property Manager)
1. Ga in Airport View naar het juiste lokaal/gebouw.
2. Vink 'Architecture' aan in de 'Contents of view'.
3. Ga naar 'Add Assets' → 'Building Activities' → 'Maintenance'.
4. Vink 'Premises physical classification' aan om huidige classificatie te raadplegen; gebruik 'Classify By' > 'Code' voor de kleurenlegende.
5. Voor effectief invullen/wijzigen: gebruik de editeerbare laag 'Premises physical classification for Editor' via de Collector App.
6. Vul Grp, Classification en Detail in volgens AM-PROM-REF Legende Classificatie.
7. Sla op.
8. Let op: de classificatie moet stroken met het gebouw-specifieke wettelijk kader brandveiligheid (AM-PROM-120).

### Veld 4 — Observation (Actor: Property Manager)
1. Ga in Airport View naar het juiste lokaal.
2. Ga naar 'Add Assets' → 'Building Activities' → 'Maintenance'; vink laag 'Premises for Editor' aan.
3. Bij ruimteaanvraag van een klant (optie/reservatie): vul, in samenspraak met de [[Commercial Lead]], het veld in met naam verwachte toekomstige gebruiker (via Terminal Space Management in Airport View) vóór contractondertekening.
4. Sla op.
5. Bij contractondertekening: maak het veld Observation **leeg** (reservatie/optie vervalt).
6. Sla op.

### Visuele tekening (Actor: Property Manager aanvraag; BIM Office uitvoering)
1. Ga naar ServiceNow, maak een nieuw ticket gericht aan BIM Office voor het bijwerken van de tekening.
2. Vermeld de premise-referentie en een korte beschrijving van de wijziging (nieuwe/gerenoveerde ruimte), met verwijzing naar het AM Request-nummer.
3. Dien het ticket in.
4. BIM Office ontvangt het ticket en werkt de tekening bij in Airport View.

## Output
- Correcte, actuele en conforme PROM-datavelden in Airport View

## RACI

| Stap | Responsible | Accountable | Consulted | Informed |
|------|-------------|-------------|-----------|---------|
| Veld 1–4 | [[Property Manager]] (+ [[Data Clerk]] ondersteuning) | [[APM]] | [[Commercial Lead]], [[BIM Office]] | |

## Tools
- [[Airport View]] (Collector App) — primair systeem PROM-datavelden
- AX — commercieel contract (Occupant normaal automatisch gevuld)
- [[ServiceNow]] — BIM Office ticket voor visuele tekening
- AM-PROM-REF Legende Classificatie — geldige waarden Classificatie
- Glossary Occupant — geldige waarden Occupant

## KPI's

| KPI | Definitie | Target |
|-----|-----------|--------|
| Tijdigheid | % triggermomenten waarbij PROM-datavelden binnen 5 werkdagen bijgewerkt zijn | n.t.b. (voorstel ≥80%) |
| Volledigheid | % actieve ruimtes met alle 4 velden correct ingevuld | n.t.b. (voorstel 80%) |
| Correctiegraad | % ruimtes bij follow-up waarbij ≥1 veld gecorrigeerd moest worden | n.t.b. (doel: dalende trend) |

## Raakvlakken
- [[AMR Handling]] — stap 10: sluiten AM Request triggert Occupant/Classificatie/Name (Situatie 2)
- [[Plaatsbeschrijving]] — flow A stap 8: uitgaande PLB triggert Occupant; flow B stap 6: Gate 4B triggert Occupant/Observation (Situatie 1)
- [[Periodieke Rondgang]] — controle patrimoniumdata ter plaatse (checklist C8), correctie via AM-PROM-130
- [[Space Use Change]] — ruimtewijziging als trigger

## Open punten
- Zie [[60_OpenItems/OI-004 Premises niet in contract zichtbaar]]
- Zie [[60_OpenItems/OI-003 Toegangsrechten Airport View]]
- Zie [[60_OpenItems/OI-002 Platformtransitie Planon-Maximo-AV]]
- Exacte laagnaam in Airport View voor Occupant/Name te bevestigen met PROM's (vermoedelijk 'Premises for Editor')
- Of Observation-leegmaken bij contractondertekening automatisch kan via AX-koppeling: n.t.b.

## Bronnen
- ([[00_Sources/AM-PROM-130 SOP Patrimonium Data Beheer.docx]]) — SOP, versie 22/07/2026, Toan Pauwels
- ([[00_Sources/AM-PROM-130 WI Patrimonium Databeheer.docx]]) — WI, versie 22/07/2026, Toan Pauwels
- ([[00_Sources/PROM Atelier — Patrimonium data beheer (4).pptx]]) — PROM Atelier 06/10
