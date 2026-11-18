---
type: activity
code: 350
proces: Property Operations Compliance Control
status: draft
sop: AM-PROM-350
wi: AM-PROM-351
eigenaar: "[[Property Manager]]"
laatst_bijgewerkt: 2026-11-18
---

# Evacuatie Oefening — Organisatie evacuatieoefening

## Doel
Het correct organiseren en uitvoeren van de jaarlijkse verplichte evacuatieoefening in gebouwen eigendom van BAC, waarbij elke betrokken partij weet wat zijn/haar verantwoordelijkheid is en wanneer welke stappen ondernomen moeten worden. ([[00_Sources/AM-PROM-350 PRO Organisatie evacuatieoefening .pdf]])

## Scope
Van toepassing op gebouwen:
- Eigendom van Brussels Airport Company
- Geen eigen BAC-personeel aanwezig
- Meer dan één externe klant aanwezig (multi-user)

Indien het gebouw extern beheerd wordt, kan AM Property Management de taak delegeren aan de externe gebouwbeheerder, maar blijft verantwoordelijk voor de opvolging. ([[00_Sources/AM-PROM-351 WI Organisatie evacuatieoefening .pdf]])

## Wettelijke basis
- Codex, Boek III, Titel 3, art. III.3-26: elke werkgever verplicht tot jaarlijkse evacuatieoefening
- Gezamenlijk brandpreventiedossier: verantwoordelijkheid bij de beheerder van het gebouw
- BAC als beheerder: intern noodplan + interventiedossier voor de volledige entiteit
([[00_Sources/AM-PROM-350 PRO Organisatie evacuatieoefening .pdf]])

## Trigger
Periodieke verplichting vanuit het [[Compliance-register]] (CR-073 Verslag evacuatieoefening — minstens jaarlijks). ([[00_Sources/AM-PROM-3Y2 Template Compliance-register.xlsx]])

## Input
- [[Compliance-register]] per gebouw (verplichting CR-073)
- Evacuatieplannen ([[00_Sources/AM-ADC-201 PRO Beheren van evacuatieplannen (2).pdf]])
- ISO45001-instructies: Richtlijnen organiseren evacuatieoefeningen op Brussels Airport
- Contactgegevens klanten en preventieadviseurs
- AVL-site: Arbeidsveiligheid Luchthavengebruikers

## Stappen (WI AM-PROM-351)

| # | Stap | Actor | Tool |
|---|------|-------|------|
| 1 | Datum van de evacuatieoefening indienen via AVL-site, ten minste **3 weken** op voorhand ter goedkeuring | [[Property Manager]] of externe gebouwbeheerder | AVL-site |
| 2 | Aanvraag indienen conform ISO45001-instructies organiseren evacuatieoefeningen op Brussels Airport | [[Property Manager]] of externe gebouwbeheerder | ISO45001-richtlijn |
| 3 | Indien extern beheerd gebouw: datum bepalen in overleg met AM/BP&WC | [[Property Manager]] | Outlook |
| 4 | Datum ten minste **1 maand** op voorhand communiceren aan klanten; notificaties sturen naar: Federale Politie, BAC Security, BAC Airside Inspection | [[Property Manager]] of externe gebouwbeheerder | Outlook |
| 5 | Wachten op goedkeuring/afwijzing (binnen **14 dagen** na aanvraag) | [[Property Manager]] | AVL-site |
| 6 | Bij afwijzing: alle betrokken partijen verwittigen en nieuwe datum bepalen | [[Property Manager]] | Outlook |
| 7 | Na goedkeuring door alle goedkeurende partijen: notificaties sturen naar informatieve partijen | [[Property Manager]] | Outlook |
| 8a | **Dag van de oefening — aanvang:** telefonisch informeren: Noodcentrale (112), Airside Inspection (indien airside gebouw of evacuatie richting airside: 02/753.69.00), HIF (02/753.60.00), ERC (02/753.33.33), Plantondienst (02/753.70.00) | [[Property Manager]] of externe gebouwbeheerder | Telefoon |
| 8b | **Dag van de oefening — uitvoering:** beheerder + technieker brandmeldcentrale aanwezig; 1 verantwoordelijke per klant (bij voorkeur preventieadviseur) meldt zich aan bij beheerder; coördinatie door beheerder; oefening gestart door technieker brandmeldcentrale. Organisatie conform ISO45001. | [[Property Manager]], technicus onderhoudsfirma brandmeldcentrale, preventieadviseurs klanten | |
| 8c | **Dag van de oefening — afsluiting:** telefonisch informeren: zelfde diensten als aanvang | [[Property Manager]] of externe gebouwbeheerder | Telefoon |
| 9 | Na de oefening: feedbackformulier invullen op ASK (**binnen 1 week**); verslag opmaken met aanbevelingen en basis voor aanpassingen intern noodplan/technische interventies (**binnen 1 maand**) | [[Property Manager]] of externe gebouwbeheerder | ASK |
| 10 | Verslag delen met preventieadviseurs van betrokken klanten | [[Property Manager]] | Outlook |
| 11 | Indien verslag door klant opgesteld: kopie bezorgen aan [[Property Manager]] via AMproperty@brusselsairport.be; eventuele schade/vaststellingen bezorgen aan verantwoordelijke partij | Klant | AMproperty@brusselsairport.be |
| 12 | Schade/vaststellingen binnen AM opnemen via HIF (defect) of [[AM Request]] (planbare actie); [[Compliance-register]] bijwerken (CR-073 → Geldig) | [[Property Manager]] | HIF (Maximo), [[AM Request]], [[Compliance-register]] |

([[00_Sources/AM-PROM-351 WI Organisatie evacuatieoefening .pdf]])

## Output
- Uitgevoerde evacuatieoefening conform wettelijke verplichting
- Feedbackformulier ingevuld op ASK
- Verslag evacuatieoefening (met aanbevelingen)
- Bijgewerkt [[Compliance-register]] (CR-073 status = Geldig)
- Eventuele actiepunten via HIF of [[AM Request]]

## RACI

| Stap | Responsible | Accountable | Consulted | Informed |
|------|-------------|-------------|-----------|---------|
| 1–12 | [[Property Manager]] (of externe gebouwbeheerder) | [[Property Manager]] | H&S, Fire & Emergency Services, preventieadviseurs klanten | Federale Politie, BAC Security, BAC Airside Inspection, Noodcentrale, ERC, Plantondienst, HIF |

## Termijnen

| Termijn | Wat |
|---------|-----|
| ≥ 3 weken voor oefening | Datum indienen via AVL-site |
| ≥ 1 maand voor oefening | Datum communiceren aan klanten en goedkeurende partijen |
| 14 dagen na aanvraag | Goedkeuring/afwijzing via AVL-site |
| Binnen 1 week na oefening | Feedbackformulier invullen op ASK |
| Binnen 1 maand na oefening | Verslag opmaken |

## Tools
- AVL-site (Arbeidsveiligheid Luchthavengebruikers) — indienen en goedkeuren datum
- ISO45001-instructies — richtlijnen organiseren evacuatieoefeningen
- ASK — feedbackformulier en verslag
- [[AM Request]] (ASK SharePoint) — actiepunten binnen AM
- HIF (Maximo) — defecten na oefening
- [[Compliance-register]] (AM-PROM-3Y2) — CR-073 bijwerken
- Evacuatieplannen (AM-ADC-201)

## KPI's
- **Jaarlijkse uitvoering per gebouw** — % gebouwen (MU, geen BAC-personeel) met uitgevoerde evacuatieoefening per kalenderjaar (streefwaarde: 100%)
- **Tijdige rapportering** — % verslagen ingediend binnen 1 maand na oefening (streefwaarde: TBD)

## Raakvlakken
- [[Monitoren Verplichtingen]] — compliance-register, CR-073; oefening is een periodieke verplichting
- [[Periodieke Rondgang]] — verificatie naleving (B6, B11)
- [[AMR Handling]] — actiepunten na oefening via HIF of AM Request

## Open punten
- KPI-streefwaarden n.t.b.
- Procedure voor single-user gebouwen n.t.b. (AM-PROM-350/351 enkel voor MU zonder BAC-personeel)
- Rol externe gebouwbeheerder en rapporteringsvorm aan PM n.t.b.

## Bronnen
- ([[00_Sources/AM-PROM-350 PRO Organisatie evacuatieoefening .pdf]]) — SOP/PRO, versie V0.2, 23/12/2023, Ines Devos en Shelly Onsea
- ([[00_Sources/AM-PROM-351 WI Organisatie evacuatieoefening .pdf]]) — WI, versie V0.2, 22/12/2023, Ines Devos en Shelly Onsea
- ([[00_Sources/AM-ADC-201 PRO Beheren van evacuatieplannen (2).pdf]]) — PRO beheer evacuatieplannen, BIM Office Manager, 15/12/2022
- ([[00_Sources/AM-PROM-3Y2 Template Compliance-register.xlsx]]) — CR-073
