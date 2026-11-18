---
type: tool
naam: AM Request (SharePoint)
categorie: systeem
eigenaar: PROM — Asset Management Property
toegang: Alle BAC-medewerkers (requestor), PROM, HIF Back Office, Assigned To
laatst_bijgewerkt: 2026-11-18
---

# AM Request (SharePoint)

## Omschrijving
SharePoint-lijst voor het indienen en opvolgen van Asset Modification Requests (AMR's). Een AMR is een aanvraag van een interne klant aan Asset Management voor een kleine wijziging aan een asset, gebouw of ruimte (financiële drempel < €100.000). PROM behandelt en volgt op van indienen tot afsluiting. ([[00_Sources/Aanpassingen aan de AMR SharePoint.docx]])

## Velden (conform aanpassingen PROM Excellence)

| Veld | Type | Verplicht | Wie vult in | Opmerkingen |
|------|------|-----------|-------------|-------------|
| Issue ID | Autonummer | Auto | Systeem | Automatisch volgnummer |
| Title | Tekst (1 regel) | Ja | Requestor | |
| Description | Tekst (meerdere regels) | Ja | Requestor | Exacte locatie vermelden (gebouw, verdieping, ruimte) |
| Attachment | Ja/Nee | Nee | Requestor | |
| Client | Tekst (1 regel) | Nee | Requestor | Externe gebruiker of tenant |
| Priority | Keuzelijst | Nee | Requestor | (1) High / (2) Normal / (3) Low |
| Priority Motivation | Tekst | Nee | Requestor | Verplicht bij Priority = High |
| Request Type | Keuzelijst | **Ja** | Requestor | Offerte / Werkaanvraag – Uitvoering Offerte / Plaatsbeschrijving / Advies / Facility / Andere |
| Asset Cluster | Keuzelijst (meervoudig) | Nee | PROM + Requestor | Electricity / HVAC & Plumbing / Fire / Infrastructure & Mechanics / Baggage / Physical Security / Apron / Airfield |
| Requestor BAC | Persoon/Groep | Ja | Requestor | Primaire contactpersoon |
| BLO | Persoon/Groep | Nee | Requestor | Budgetverantwoordelijke; verplicht indien financiering vereist |
| **Budgetcode** *(nieuw)* | Tekst (1 regel) | **Ja** | Requestor | Budgetcode of 'NVT'; verplicht veld |
| Assigned To | Persoon/Groep | Nee | PROM | Uitvoerder; bij meerdere clusters: persoon van grootste werklast |
| Request Status | Keuzelijst | Nee | PROM | New / Ongoing / To be discussed / To be followed / Waiting feedback requestor / Closed |
| Comments / Feedback | Tekst (meerdere regels) | Nee | PROM | Communicatiekanaal PROM ↔ Requestor ↔ Uitvoerder |
| Due Date | Datum | Nee | PROM | |
| Related Issues | Lookup | Nee | PROM | Verwijzing naar andere AMR (bv. Offerte → Uitvoering Offerte) |
| Created | Datum | Auto | Systeem | |
| **Days Open** *(nieuw)* | Getal (auto, via flow) | Auto | Systeem | Vandaag − Created; bevriest bij status Closed; geel ≥45d, rood ≥60d |
| Handled By | Keuzelijst | Nee | HIF Back Office | Cargo & Logistics / Commercial Real Estate / Passenger Aviation / Technology & Infrastructure / Facility |
| Attachments | Bijlage | Nee | Requestor | |

([[00_Sources/Aanpassingen aan de AMR SharePoint.docx]])

## Escalatie- en alertlogica

| Trigger | Ontvanger | Bericht |
|---------|-----------|---------|
| Days Open = 45d (status ≠ Closed) | Handled By (business department) | Geel signaal: stem voortgang af met uitvoerder |
| Days Open = 45d (status ≠ Closed) | Assigned To | Geel signaal: stem af met Handled By |
| Days Open = 60d (status ≠ Closed) | Handled By | Rood signaal: escaleer naar [[APM]] |
| Days Open = 60d (status ≠ Closed) | Assigned To | Rood signaal: stem af met Handled By |
| Status → 'Waiting feedback requestor' | Requestor | PROM wacht op jouw feedback |
| Status = 'Waiting feedback requestor' + Comments ≥ 7d niet bijgewerkt | Handled By | Feedback 7 dagen onbeantwoord |
| Status = 'Waiting feedback requestor' + Comments ≥ 14d niet bijgewerkt | Handled By | Feedback 14 dagen onbeantwoord; escaleer naar [[APM]] |

Technisch: dagen-open triggers vereisen een dagelijkse Power Automate-flow (native SharePoint-alerts ondersteunen geen tijdvoorwaarden). ([[00_Sources/Aanpassingen aan de AMR SharePoint.docx]])

## Gebruik in activiteiten
- [[AMR Handling]] — hoofdtool voor registratie en opvolging
- [[Space Use Change]] — ruimtegerelateerde aanvragen
- [[Periodieke Rondgang]] — Eigenaar-actiepunten na rondgang
- [[Monitoren Verplichtingen]] — Eigenaar-acties

## Toegang & rechten
- Alle BAC-medewerkers als requestor
- PROM-leden als Member (Tiebe Anckaert, Sylviane Raveschot, Dimitri Van Eyck, Mark Meert, Erik Akbas, Isabelle Bos) ([[00_Sources/Aanpassingen aan de AMR SharePoint.docx]])
- [[HIF Back Office]]: vult 'Handled By' in

## Aandachtspunten
- Wijziging Request Type-waarden heeft impact op [[AM Cockpit]] — zie [[60_OpenItems/OI-013 Impact Request Type wijziging op AM Cockpit]]
- Dagelijkse Power Automate-flow vereist voor Days Open en geel/rood signaal — te bevestigen met SharePoint-team
- Bestaande records met oude Request Type-waarden: migratie afspreken met SharePoint-team

## Bronnen
- ([[00_Sources/Aanpassingen aan de AMR SharePoint.docx]]) — versie 2026-11-18
- ([[00_Sources/Communication AM Request changes.docx]])
- ([[00_Sources/Space Use Change Turtle New.pptx]])
