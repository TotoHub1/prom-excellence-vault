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
Beschrijven wanneer een afwijking door een gebruiker een compliance breach wordt, en hoe de [[Property Manager]] een breach classificeert, logt, communiceert, opvolgt en afsluit, met de juiste verantwoordelijke per ernst. Centrale log- en escalatiestap binnen AM-PROM-300 ([[Property Operations Compliance Control]]) voor afwijkingen die worden vastgesteld in [[Monitoren Verplichtingen]] (AM-PROM-3Y0), [[Periodieke Rondgang]] (AM-PROM-330) en andere bronnen. ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

## Scope
Van toepassing op afwijkingen en compliance breaches door **gebruikers** — Maatschappijen en interne BAC-gebruikers (ook BAC in de rol van gebruiker) — van lokalen en gebouwen beheerd door Property Management (single user en multi user via [[E&C]]), van de vaststelling tot de afsluiting. Ook breaches waarvan het herstel volgens de [[Demarcatielijst]] bij de Eigenaar ligt.

**Buiten scope:** de uitvoering van herstellingen (AM RUN/BUILD); overtredingen door BAC-medewerkers of contractors buiten hun rol als gebruiker. ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

## Definities ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

| Term | Definitie |
|------|-----------|
| Afwijking | Vaststelling dat de gebruiker een verplichting of regel niet (volledig) naleeft — contract, demarcatielijst, site rules, huishoudelijk reglement of wetgeving — die nog geen compliance breach is. Gebruiker krijgt één herinnering met termijn. **Niet gelogd.** |
| Compliance breach | Afwijking waarvoor de gebruiker verantwoordelijk is en die (a) niet opgelost na één herinnering, (b) veiligheidsrisico inhoudt (onmiddellijk), of (c) herhaling is van dezelfde afwijking door dezelfde gebruiker binnen 12 maanden (voorstel, te valideren). **Enkel breaches worden gelogd.** |
| Gebruiker | Maatschappij (contractpartij) of interne BAC-gebruiker (zonder contract/demarcatielijst; verplichtingen onderhoud/keuring bij Eigenaar, gebruik volgt site rules/huishoudelijk reglement) |
| Maatschappij | Enige partij aan wie het gebouw ter beschikking wordt gesteld, met contractuele afspraken over onderhoud en investeringen (definitie AM-PROM-411). Wie via de Maatschappij het gebouw gebruikt (personeel, onderaannemers, onderhuurders) valt onder haar verantwoordelijkheid (te bevestigen). |
| Herinnering | Één schriftelijke vraag aan de gebruiker om een afwijking binnen een termijn op te lossen. Bij een periodieke rondgang geldt het verslag met actiepunten en termijn als herinnering. |
| Kennisgeving | Schriftelijke mededeling aan de gebruiker dat de afwijking een compliance breach is, met de ernst, de gevraagde actie en de hersteltermijn. |
| Controlemoment | Het volgende periodieke moment waarop de naleving opnieuw wordt gecontroleerd: de volgende periodieke rondgang van het gebouw, of de volgende controle volgens de periodiciteit in het compliance-register. |
| Breach log | Register van alle compliance breaches door gebruikers van één Business Department. Tussentijds Excel (AM-PROM-3X2); definitieve tool n.t.b. — zie [[60_OpenItems/OI-006 Definitieve tool breach log]]. |
| Compliance-register | Overzicht per gebouw/rentable unit van alle verplichtingen van gebruiker en Eigenaar (AM-PROM-3Y2); documentafwijkingen worden daar opgevolgd tot ze een compliance breach worden. |

## Trigger ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])
1. Vaststelling tijdens [[Periodieke Rondgang]] (AM-PROM-330) die niet ter plaatse is opgelost en na het verslag (de herinnering) niet binnen de termijn is opgelost
2. Overdracht vanuit [[Monitoren Verplichtingen]] (AM-PROM-3Y0): verplicht document blijft na één herinnering uit of blijft niet-conform (status 'Niet in orde', herinneringstermijn verstreken)
3. Melding door BAC-stakeholder (AMCC, AM RUN, H&S, [[Commercial Lead]]), externe inspecteur of [[E&C]], of eigen vaststelling [[Property Manager]] buiten periodieke rondgang — die na één herinnering niet opgelost is
4. Elke afwijking door de gebruiker **met veiligheidsrisico**, ongeacht de bron (onmiddellijk, zonder herinnering)
5. **Herhaling** van dezelfde afwijking door dezelfde gebruiker binnen 12 maanden (voorstel, te valideren)

## Input
- Vastgestelde afwijking (uit [[Periodieke Rondgang]], eigen vaststelling [[Property Manager]], melding stakeholder, of overdracht vanuit [[Monitoren Verplichtingen]])
- Referentie rondgangverslag of mail
- [[Compliance-register]] per gebouw (AM-PROM-3Y2)
- Contract, [[Demarcatielijst]] (AM-PROM-411) en site rules van het gebouw
([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

## Stappen (WI AM-PROM-3X1)

| # | Stap | Actor | Tool |
|---|------|-------|------|
| 1 | **Afwijking opvolgen en breach vaststellen:** Ontvang vaststelling (rondgang, melding, overdracht 3Y0). Is afwijking ter plaatse opgelost of geen afwijking? → niet loggen, terugkoppelen. Stuur anders één schriftelijke herinnering met vaststelling, regel, gevraagde actie en termijn (bij rondgang = het verslag). Opgelost → stopt hier. Wordt breach? → stap 2. | [[Property Manager]] / Melder / [[E&C]] | [[Breach Log]], Outlook |
| 2 | **Classificeren:** Kies categorie (zie Categorieën). Bepaal ernst (Limited/Significant/Major/Critical) per classificatietabel. Veiligheidsrisico = minstens Major. Bepaal wie het herstel uitvoert (gebruiker of Eigenaar via demarcatielijst). **Critical: neem eerst maatregel die gevaar wegneemt, bel onmiddellijk [[APM]]**. Gebruik in strijd met classificatie of geen contract → controleer en corrigeer in [[Airport View]] (zie [[Patrimonium Data Beheer]], WI AM-PROM-130). | [[Property Manager]] | [[Breach Log]], [[Airport View]] |
| 3 | **Loggen:** Open [[Breach Log]] BD, eerste lege regel (ID automatisch). Vul verplichte velden ★ in: datum breach, bron, gebouw, gebruiker, omschrijving met verwijzing verslag/mail, reden, ernst, status 'Open'. Eén regel per breach. Controleer berekende kolommen 'Verantwoordelijk' en 'Te informeren'. **Herstel door Eigenaar?** → HIF-ticket (defect) of AM Request (Request Type 'Andere', prioriteit per ernst — zie Eigenaar-acties tabel); noteer referentie in [[Breach Log]]. **Documentbreach?** → noteer ID in [[Breach Log]] en 'Overgedragen aan Breach Logging' in [[Compliance-register]]. | [[Property Manager]] | [[Breach Log]], HIF (Maximo), [[AM Request]], [[Compliance-register]] |
| 4 | **Communiceren:** Stuur gebruiker kennisgeving met: vaststelling, eerdere herinnering, ernst, gevraagde actie en hersteltermijn. **Maatschappij:** informeer [[Commercial Lead]] (bv. in cc). **BAC als gebruiker (Limited/Significant):** informeer [[APM]]. **Multi user:** stem met [[E&C]] af wie Maatschappij aanspreekt (mandaat E&C n.t.b.). Noteer locatie correspondentie en bewijs in [[Breach Log]]. | [[Property Manager]] | [[Breach Log]], Outlook |
| 5 | **Opvolgen per controlemoment:** Vul volgend controlemoment in (zie tabel Opvolging over tijd). Filter [[Breach Log]] wekelijks op 'Actie nodig' en handel af. Werk status bij ('In herstel' / 'Hersteld – te verifiëren'). Termijn verstreken vóór controlemoment → standaard opvolging, ernst blijft gelijk. Controlemoment voorbij en niet opgelost → ernst +1, ernsthistoriek invullen (datum – wijziging – reden), nieuw controlemoment, informeer 'Te informeren'; vanaf Major → stap 6. Verifieer herstel met bewijs (foto, verslag, keuring) of ter plaatse. | [[Property Manager]] / Gebruiker | [[Breach Log]] |
| 6 | **Overdragen aan [[APM]]:** Major (bij registratie of na ernst +1) → overdragen aan [[APM]] met overzicht regels van die gebruiker; vul datum overdracht in. Critical → overdracht telefonisch (stap 2). [[APM]] beslist over risk register. Interne BAC-gebruiker vanaf Major: [[APM]] spreekt verantwoordelijke afdeling aan. Bij schade/verhaalbare kosten/weigering: [[APM]] beslist over contractuele escalatie, [[Commercial Lead]] voert uit. **Periodieke review PM + [[APM]]** (frequentie n.t.b.): tabblad Rapportage bespreken. | [[Property Manager]] + [[APM]] | [[Breach Log]] |
| 7 | **Afsluiten:** Verifieer herstel (en bij Eigenaar-herstel: wacht op afsluiting HIF-ticket of AM Request). Zet status 'Afgesloten', datum afsluiting = datum herstel. Noteer uitkomst en leerpunten. Geef feedback aan gebruiker, Melder, [[Commercial Lead]]; vanaf Major ook [[APM]]. Documentbreach: werk [[Compliance-register]] bij (nieuwe gegevens + status 'Afgesloten'). Archiveer bewijs en correspondentie (Bricsys). **Contract loopt af met open breach met schade?** → bezorg aan [[Commercial Lead]] voor uitgaande [[PLB]] (WI AM-PROM-311, stap 4.7) (te bevestigen). | [[Property Manager]] | [[Breach Log]], [[Compliance-register]], Bricsys |

([[00_Sources/AM-PROM-3X1 WI Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

## Output
- Afgesloten breach in [[Breach Log]] met datum afsluiting, uitkomst en leerpunten
- Bijgewerkt [[Compliance-register]]
- Input voor periodieke review met [[APM]] en voor PRM.1.1

## RACI

| Ernst | Responsible | Accountable | Consulted | Informed |
|-------|-------------|-------------|-----------|---------|
| Limited / Significant | [[Property Manager]] | [[Property Manager]] | [[Commercial Lead]] (twijfel classificatie) | [[Commercial Lead]] (Maatschappij) of [[APM]] (BAC intern) |
| Major / Critical | [[APM]] | [[APM]] | [[Property Manager]] | [[Commercial Lead]] of stakeholders |
| Critical | [[APM]] | [[APM]] | | Beslist over risk register; eerst telefonisch |

([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

## Rollen ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

| Rol | Omschrijving |
|-----|-------------|
| [[Property Manager]] | Eigenaar van de activiteit en van de [[Breach Log]] van het eigen BD: volgt afwijking op met één herinnering; classificeert, logt, communiceert en volgt breach op. Verantwoordelijk bij Limited en Significant. |
| Melder | Meldt een mogelijke afwijking aan de [[Property Manager]] (bv. [[AMCC]], AM RUN, H&S, [[Commercial Lead]], [[E&C]], externe inspecteur). |
| Gebruiker | Maatschappij of interne BAC-gebruiker; lost de afwijking of breach op binnen de termijn. |
| Uitvoerder | Voert herstellingen uit waarvoor de Eigenaar verantwoordelijk is (AM RUN/BUILD, via HIF-ticket of AM Request). |
| [[Commercial Lead]] | Contractverantwoordelijke voor de Maatschappij: geraadpleegd bij classificatie, geïnformeerd bij elke breach van een Maatschappij; voert contractuele escalatie uit na beslissing APM. |
| [[APM]] | Geïnformeerd bij Limited/Significant van BAC als gebruiker; verantwoordelijk vanaf Major; beslist bij Critical over risk register; periodieke review breach log. |
| [[E&C]] (multi user) | Externe gebouwbeheerder; meldt afwijkingen in multi user-gebouwen; rol in communicatie met Maatschappij n.t.b. |

## Ernst en escalatielogica ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

| Ernst | Verantwoordelijk | Hersteltermijn | Wie geïnformeerd | Voorbeelden |
|-------|-----------------|----------------|-----------------|-------------|
| Limited | [[Property Manager]] | **30 dagen** | CL (klant) of APM (BAC intern) | Afval/opslag in gangen na herinnering; niet-kritisch onderhoudsattest na herinnering |
| Significant | [[Property Manager]] | **15 dagen** | CL (klant) of APM (BAC intern) | Hinder naburige gebruikers; lokaal buiten bestemming; fit-out zonder toelating (zonder schade) |
| Major | [[APM]] | **5 dagen** | CL (klant) | Vervallen keuring veiligheidsinstallatie; schade gebouw door gebruiker; opslag in technische ruimte |
| Critical | [[APM]] | **Onmiddellijk** | CL (klant); APM beslist over risk register | Geblokkeerde nooduitgang; uitgeschakelde branddetectie |

> Hersteltermijnen vastgelegd in [[50_Decisions/DEC-005 Hersteltermijnen breach per ernst vastgelegd]]

**Ernststijging:** de ernst stijgt per **gemist controlemoment**, niet per dag. Noteren in ernsthistoriek (datum – wijziging – reden). Ernst daalt enkel om een classificatiefout recht te zetten. Een breach wordt nooit opnieuw een afwijking. ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

### Categorieën ([[00_Sources/AM-PROM-3X1 WI Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

| Categorie | Omschrijving |
|-----------|-------------|
| Veiligheid | Inbreuken die veiligheidsrisico inhouden |
| Documenten / keuringen | Ontbrekende of niet-conforme keurings- en onderhoudsverslagen |
| Netheid / gebruik | Gebruik niet conform contract/site rules; netheid |
| Gedrag / overlast | Hinder voor naburige gebruikers of derden |
| Contractuele inbreuk | Schending van contractuele verplichtingen zonder directe schade |
| Andere | Inbreuken buiten bovenstaande categorieën |

### Opvolging over tijd — controlemoment per bron ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

| Bron van de breach | Volgend controlemoment | Ernst +1 wanneer |
|--------------------|----------------------|-----------------|
| Periodieke rondgang | Volgende periodieke rondgang van het gebouw | Breach bij die rondgang nog niet opgelost |
| Keuringsverslag of onderhoudsrapport | Volgende controle volgens periodiciteit in [[Compliance-register]] | Document dan nog niet aangeleverd of niet conform |
| Melding of eigen vaststelling | Eerstvolgende periodieke rondgang of controle | Breach dan nog niet opgelost |

### Eigenaar-acties: AM Request prioriteit (voorstel) ([[00_Sources/AM-PROM-3X1 WI Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

| Ernst breach | AM Request Priority |
|-------------|-------------------|
| Limited | (3) Low |
| Significant | (2) Normal |
| Major | (1) High + Priority Motivation |
| Critical | (1) High + Priority Motivation |

## Tools
- [[Breach Log]] (AM-PROM-3X2) — tussentijdse Excel-template per Business Department
- [[Compliance-register]] (AM-PROM-3Y2) — bijwerken na overdracht en na afsluiting
- HIF (Maximo) + [[AM Request]] (AMR SharePoint) — enkel voor herstel door de Eigenaar
- [[Airport View]] — controle Occupant/Classificatie bij gebruik in strijd met classificatie (stap 2)
- Bricsys — archivering bewijs en correspondentie
- Outlook en telefoon — kennisgeving, herinnering

## KPI's
- **% Overdue compliance actions** — open breaches waarvan hersteltermijn verstreken (streefwaarde: TBD)
- **% Compliance findings closed on time** — afgesloten breaches binnen hersteltermijn (streefwaarde: TBD)
- **Number of open (critical) compliance issues** — open breaches / waarvan Critical (streefwaarde: TBD)
([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])

## Kwaliteitsborging ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]])
- Elk BD houdt **één breach log** bij als enige registratie van compliance breaches
- **Wekelijks:** [[Property Manager]] filtert op 'Actie nodig' en handelt elke regel af
- **Periodieke review** PM + [[APM]] (frequentie n.t.b.): tabblad Rapportage bespreken (open breaches, verstreken termijnen, breaches ≥ Major, gedrag per gebruiker, KPI's) → kerncijfers plakken in historiek
- Breach met **Eigenaar-herstel**: pas afsluiten na afsluiting gekoppeld HIF-ticket of AM Request
- Input PRM.1.1 voorlopig ondergebracht in [[Monitoren Verplichtingen]] (AM-PROM-3Y0); op termijn mogelijk aparte activiteit in AM-PROM-300

## Raakvlakken
- [[Periodieke Rondgang]] — voornaamste bron van breaches
- [[Monitoren Verplichtingen]] — documentbreaches worden overgedragen
- [[AMR Handling]] — herstelacties via HIF-ticket of [[AM Request]]; Eigenaar-herstel volgt WI AM-PROM-101 vanaf stap 2
- [[Patrimonium Data Beheer]] — gebruik in strijd met classificatie → corrigeren in Airport View (stap 2)
- [[Plaatsbeschrijving]] — open breach met schade bij contractafloop → bezorgen aan CL voor uitgaande PLB (stap 7, te bevestigen)
- PRM.1.1 — compliance-score gebruiker als input evaluatie

## Open punten
- Hersteltermijnen vastgelegd — zie [[50_Decisions/DEC-005 Hersteltermijnen breach per ernst vastgelegd]]
- Zie [[60_OpenItems/OI-006 Definitieve tool breach log]]
- Periode herhaling (12 maanden) — voorstel, nog te valideren
- Herinneringstermijn n.t.b. in AM-PROM-3X0
- AM Request prioriteitsmapping per ernst — voorstel, te valideren
- Rol [[E&C]] in communicatie met Maatschappij — n.t.b.
- Verantwoordelijkheid personeel/onderaannemers/onderhuurders via Maatschappij — te bevestigen
- Frequentie periodieke review PM + [[APM]] — n.t.b.
- Nieuwe kennisgeving aan gebruiker bij ernst +1 — n.t.b. in WI AM-PROM-3X1
- Activering risk register bij Critical — n.t.b.
- Kanaal APM → verantwoordelijke afdeling bij interne BAC-gebruiker vanaf Major — n.t.b.

## Bronnen
- ([[00_Sources/AM-PROM-3X0 SOP Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]]) — SOP, versie 24/04/2026, Toan Pauwels
- ([[00_Sources/AM-PROM-3X1 WI Registreren en opvolgen van afwijkingen en compliance breaches door gebruikers.pdf]]) — WI, versie 31/03/2026, Toan Pauwels
- ([[00_Sources/AM-PROM-3X2 Breach Log Template.xlsx]]) — template breach log, eigenaar: Toan Pauwels
- ([[00_Sources/Compliance breaches - PROM Atelier (5).pptx]]) — PROM Atelier Compliance Breaches, 20/10
