---
type: decision
datum: 2026-11-18
bron: "[[00_Sources/Aanpassingen aan de AMR SharePoint.docx]]"
status: bevestigd
eigenaar: PROM Excellence Team
laatst_bijgewerkt: 2026-11-18
---

# Beslissing: AMR escalatiemethode — geel signaal op 45 dagen, rood signaal op 60 dagen

## Beschrijving
De opvolgings- en escalatiemethode voor [[AMR Handling]] is vastgelegd en gevalideerd door het PROM Excellence-team. AMR's die te lang openstaan krijgen een kleurcode en automatische alerts.

## Context
Voortvloeiend uit de herziening van de AM Request-activiteit met het PROM Excellence-team. Onderdeel van de nieuwe SOP (AM-PROM-100) en WI (AM-PROM-101).

## Beslissing
- **Geel signaal**: Days Open ≥ 45 dagen (status ≠ Closed) → alert naar Handled By en Assigned To
- **Rood signaal**: Days Open ≥ 60 dagen (status ≠ Closed) → alert naar Handled By en Assigned To; Handled By escaleert naar [[APM]]
- Implementatie via dagelijkse Power Automate-flow (te bevestigen met SharePoint-team)

## Gevolgen
- Nieuw veld 'Days Open' toe te voegen aan [[AM Request]] SharePoint
- Kleurcodering in de AMR-lijst (geel/rood)
- Impact op [[AM Cockpit]]: afstemmen met Business Analyst (buiten scope SharePoint-aanpassingen)

## Bronnen
- ([[00_Sources/Aanpassingen aan de AMR SharePoint.docx]])
