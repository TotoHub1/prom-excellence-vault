# PROM Knowledge Vault — instructions for Claude

This is an Obsidian vault used by Toan Pauwels (Methis Consulting) as a personal analysis hub for the
PROM Excellence engagement at Brussels Airport Company (BAC), Asset Management — Property Management.
Goal: analyse many sources and produce aligned process documentation (L2 turtles, SOPs, WIs).

## Folder structure
- `00_Sources/` — raw input (meeting notes, atelier verslagen, mails, exports, existing SOP/WI). NEVER edit.
- `10_Activities/` — one note per activity (e.g. `3Y0 Monitoren verplichtingen.md`)
- `20_Roles/` — one note per role (PROM, APM, Property Officer, E&C, HIF Back Office, ...)
- `30_Tools/` — one note per system/template (Forma, Maximo, AMR SharePoint, compliance-register, ...)
- `40_Glossary/` — one note per term; the single source for wording
- `50_Decisions/` — one note per decision (date, source, status)
- `60_OpenItems/` — one note per open item (n.t.b.)
- `70_Conflicts/` — one note per contradiction between sources
- `80_Output/` — generated SOP/WI/turtle drafts
- `_templates/` — note templates

## Rules
1. Every factual statement in a knowledge note links its source: `([[00_Sources/<file>]])`.
2. Never invent content. If something is missing, create/link an open item in `60_OpenItems/` and write `n.t.b.`.
3. If sources disagree, do not pick one: create a note in `70_Conflicts/` listing both versions + sources.
4. Use `[[wikilinks]]` for every role, tool, term and activity mentioned. Create the note if it doesn't exist.
5. Use glossary terms exactly; flag synonyms found in sources in the glossary note under `aliases`.
6. Knowledge notes and all SOP/WI output are in **Dutch**. These instructions are in English.
7. WI step tables have no "Verwacht resultaat" column.
8. Before changing many files, show a short plan and wait for my go.

## Frontmatter (activity note)
```yaml
---
type: activity
code: 3Y0            # BAC document/activity code
proces: Property Operations Compliance Control
status: draft        # draft | atelier | gevalideerd
sop: AM-PROM-xxx
wi: AM-PROM-xxx
eigenaar: "[[Property Manager]]"
laatst_bijgewerkt: 2026-11-18
---
```
Sections: Doel · Trigger · Input · Stappen · Output · RACI · Tools · KPI's · Raakvlakken · Open punten · Bronnen

## Common commands I'll give
- "Verwerk bron X" → extract facts from a new source into the knowledge notes, report new/changed/conflicts.
- "Gap-analyse activiteit Y" → list missing sections, open items and conflicts for Y.
- "Genereer SOP/WI voor Y" → build from the knowledge notes only, into `80_Output/`.
