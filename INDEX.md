# 101 Prompts für Steuerberater – Index nach Kategorie, Rolle und Anlass

101 Prompts. Die Nummerierung folgt der Entstehung, nicht der Wichtigkeit.
Die Nummern laufen von 01 bis 105; es fehlen 45, 78, 79 und 81 – 45 ist
zurückgestellt, 78, 79 und 81 sind als Kandidaten dokumentiert, aber bewusst
nicht umgesetzt (beides unter „Nicht enthalten" am Ende).
Vor dem ersten Einsatz: [DATENSCHUTZ.md](DATENSCHUTZ.md).
Eigene Prompts schreiben: [BAUKASTEN.md](BAUKASTEN.md).

---

## Nach Kategorie

Jeder Prompt steht hier genau einmal. Die Gliederungen nach Rolle und
nach Anlass weiter unten nennen einzelne Prompts mehrfach – ein
Merkblatt für den Mandanten kann die Lohnsachbearbeitung genauso
brauchen wie die Kanzleileitung.

| Kategorie | Prompts |
|---|---|
| [Finanzbuchhaltung](#finanzbuchhaltung) | 8 |
| [Umsatzsteuer](#umsatzsteuer) | 8 |
| [Jahresabschluss und Bilanzierung](#jahresabschluss-und-bilanzierung) | 11 |
| [Lohn und Gehalt](#lohn-und-gehalt) | 16 |
| [Steuererklärung und Einzelsteuerfälle](#steuererklärung-und-einzelsteuerfälle) | 15 |
| [Finanzamt, Fristen und Rechtsbehelf](#finanzamt-fristen-und-rechtsbehelf) | 7 |
| [GoBD, Kasse und Verfahrensdokumentation](#gobd-kasse-und-verfahrensdokumentation) | 3 |
| [Mandantenkommunikation](#mandantenkommunikation) | 9 |
| [Honorar und Forderungen](#honorar-und-forderungen) | 4 |
| [Kanzleiorganisation und Team](#kanzleiorganisation-und-team) | 12 |
| [Mandatsbeginn und Mandatswechsel](#mandatsbeginn-und-mandatswechsel) | 3 |
| [Krise, Liquidität und Bank](#krise-liquidität-und-bank) | 5 |

### Finanzbuchhaltung

Laufende Buchführung, Kontierung, Prüfung von Buchungs- und Stammdaten.

| # | Prompt |
|---|--------|
| 02 | [Gebündelte Rückfrageliste zu unklaren Bankumsätzen](prompts/01-finanzbuchhaltung/02-rueckfrageliste-bankumsaetze.md) |
| 03 | [Buchungssatz klären und begründen (SKR03/SKR04)](prompts/01-finanzbuchhaltung/03-buchungssatz-klaeren.md) |
| 10 | [Reisekosten- und Bewirtungsbeleg prüfen](prompts/01-finanzbuchhaltung/10-reisekosten-bewirtung-pruefen.md) |
| 18 | [Offene-Posten-Liste analysieren](prompts/01-finanzbuchhaltung/18-op-liste-analysieren.md) |
| 19 | [Dublettenprüfung auf Buchungs- und Stammdatenexporten](prompts/01-finanzbuchhaltung/19-dublettenpruefung.md) |
| 20 | [Summen- und Saldenliste auf Auffälligkeiten prüfen](prompts/01-finanzbuchhaltung/20-summen-salden-pruefen.md) |
| 25 | [Namens- und Stammdatenkonvention für Personenkonten](prompts/01-finanzbuchhaltung/25-stammdatenkonvention.md) |
| 28 | [Vier-Augen-Prüfroutine für OCR-erfasste Belege](prompts/01-finanzbuchhaltung/28-ocr-pruefroutine.md) |

### Umsatzsteuer

Voranmeldung, Sonderfälle, grenzüberschreitende Umsätze.

| # | Prompt |
|---|--------|
| 04 | [Umsatzsteuer-Sonderfall prüfen (§ 13b, i.g. Erwerb, § 25a, § 19)](prompts/02-umsatzsteuer/04-umsatzsteuer-sonderfall.md) |
| 05 | [UStVA-Abweichung systematisch eingrenzen](prompts/02-umsatzsteuer/05-ustva-abweichung-eingrenzen.md) |
| 58 | [Zusammenfassende Meldung und i.g. Lieferung abgleichen](prompts/02-umsatzsteuer/58-zusammenfassende-meldung-abgleich.md) |
| 84 | [Gastronomie: Steuersatzaufteilung bei Kombiangeboten](prompts/02-umsatzsteuer/84-gastronomie-steuersatzaufteilung.md) |
| 85 | [E-Rechnungs-Umstellungsradar: Stichtag je Mandant](prompts/02-umsatzsteuer/85-erechnung-umstellungsradar.md) |
| 86 | [Fehlerhafte E-Rechnung: Fehlerklasse bestimmen und reklamieren](prompts/02-umsatzsteuer/86-erechnung-fehlerklasse.md) |
| 87 | [§ 14c UStG: unrichtiger Steuerausweis erkennen und berichtigen](prompts/02-umsatzsteuer/87-14c-unrichtiger-steuerausweis.md) |
| 88 | [Kleinunternehmer: Grenzen überwachen und Statuswechsel begleiten](prompts/02-umsatzsteuer/88-kleinunternehmer-grenzen.md) |

### Jahresabschluss und Bilanzierung

Alles, was zwischen Bilanzstichtag und Offenlegung anfällt.

| # | Prompt |
|---|--------|
| 21 | [Plausibilitätsprüfung EÜR-Zahlen vor Abgabe](prompts/03-jahresabschluss/21-euer-plausibilitaet.md) |
| 50 | [Rückstellungs-Prüfschema zum Bilanzstichtag](prompts/03-jahresabschluss/50-rueckstellungen-pruefschema.md) |
| 51 | [Cut-off- und Nachlaufcheck zum Bilanzstichtag](prompts/03-jahresabschluss/51-cutoff-nachlaufcheck.md) |
| 52 | [Anlagevermögen und AfA-Wahlrechte plausibilisieren](prompts/03-jahresabschluss/52-anlagevermoegen-afa-wahlrechte.md) |
| 53 | [Investitionsabzugsbetrag § 7g EStG überwachen](prompts/03-jahresabschluss/53-investitionsabzugsbetrag-monitor.md) |
| 54 | [E-Bilanz: unverdichtete Kontennachweise vorbereiten](prompts/03-jahresabschluss/54-ebilanz-kontennachweise.md) |
| 55 | [Anhang kleine Kapitalgesellschaft: Pflichtangaben](prompts/03-jahresabschluss/55-anhang-kleine-kapitalgesellschaft.md) |
| 56 | [Offenlegung und Ordnungsgeldabwehr](prompts/03-jahresabschluss/56-offenlegung-ordnungsgeld.md) |
| 70 | [Going-Concern und Auftragsart bei der Abschlusserstellung (nur Berufsträger)](prompts/03-jahresabschluss/70-going-concern-auftragsart.md) |
| 91 | [Betriebsaufspaltung: jährliches Monitoring](prompts/03-jahresabschluss/91-betriebsaufspaltung-monitoring.md) |
| 94 | [Verdeckte Gewinnausschüttung: Vertragsdurchsicht](prompts/03-jahresabschluss/94-vga-vertragsdurchsicht.md) |

### Lohn und Gehalt

Abrechnung, Sozialversicherung, geldwerte Vorteile, Zulieferung.

| # | Prompt |
|---|--------|
| 07 | [Lohn-Sonderfall einordnen: Steuer- und SV-Pflicht](prompts/04-lohn/07-lohn-sonderfall-einordnen.md) |
| 08 | [Lohnabrechnung für den Arbeitnehmer erklären](prompts/04-lohn/08-lohnabrechnung-erklaeren.md) |
| 40 | [Merkblatt Sachbezüge: Freigrenze und Aufmerksamkeiten](prompts/04-lohn/40-merkblatt-sachbezuege.md) |
| 41 | [SV-Fehlerprotokoll im Klartext erklären](prompts/04-lohn/41-sv-fehlerprotokoll-erklaeren.md) |
| 42 | [Anschreiben an Krankenkasse, Behörde oder Amt](prompts/04-lohn/42-anschreiben-kasse-behoerde.md) |
| 43 | [FAQ zur Lohnabrechnung für die Belegschaft des Mandanten](prompts/04-lohn/43-faq-lohnabrechnung.md) |
| 44 | [Stichtagsplan und Erinnerungstexte für Lohnzulieferungen](prompts/04-lohn/44-stichtagsplan-lohn.md) |
| 63 | [Elektro-Dienstwagen: Bewertung und Lohnabrechnungsfolgen](prompts/04-lohn/63-elektro-dienstwagen.md) |
| 64 | [Minijob und Übergangsbereich: Grenzen überwachen](prompts/04-lohn/64-minijob-uebergangsbereich.md) |
| 95 | [Lohn-Jahreswechsel: Stammdaten- und Umstellungsprüfung](prompts/04-lohn/95-lohn-jahreswechsel.md) |
| 96 | [Aktivrente: Voraussetzungen, Nachweise, Abrechnungsfolgen](prompts/04-lohn/96-aktivrente.md) |
| 97 | [Betriebsprüfung der Rentenversicherung vorbereiten](prompts/04-lohn/97-drv-betriebspruefung.md) |
| 98 | [Phantomlohn: Auslöser erkennen und Grundlage klären](prompts/04-lohn/98-phantomlohn-screening.md) |
| 99 | [Statusfeststellung: Indizienerhebung für § 7a SGB IV](prompts/04-lohn/99-statusfeststellung-indizien.md) |
| 100 | [A1 und Tätigkeit im Ausland: Entscheidungsbaum](prompts/04-lohn/100-a1-taetigkeit-ausland.md) |
| 101 | [Lohnpfändung: Pflichten des Arbeitgebers als Drittschuldner](prompts/04-lohn/101-lohnpfaendung-drittschuldner.md) |

### Steuererklärung und Einzelsteuerfälle

Deklaration und Fälle, die selten vorkommen und deshalb Zeit kosten.

| # | Prompt |
|---|--------|
| 09 | [Unterlagen-Checkliste Einkommensteuer](prompts/05-steuererklaerung/09-unterlagen-checkliste-est.md) |
| 57 | [Bauabzugsteuer § 48 EStG: Prüf- und Einbehaltsschema](prompts/05-steuererklaerung/57-bauabzugsteuer-pruefschema.md) |
| 59 | [Kapitalertragsteuer bei Gewinnausschüttung](prompts/05-steuererklaerung/59-kapitalertragsteuer-ausschuettung.md) |
| 60 | [Photovoltaik: Fallklärung Steuerbefreiung und Entnahme](prompts/05-steuererklaerung/60-photovoltaik-fallklaerung.md) |
| 61 | [Krypto: Nachweise anfordern und Steuerreport prüfen](prompts/05-steuererklaerung/61-krypto-nachweise.md) |
| 62 | [Verbilligte Vermietung: Entgeltlichkeitsprüfung](prompts/05-steuererklaerung/62-verbilligte-vermietung.md) |
| 71 | [Grundsteuer: Änderungsanzeigen erkennen und erstatten](prompts/05-steuererklaerung/71-grundsteuer-aenderungsanzeige.md) |
| 72 | [Grundsteuerwert: niedrigeren gemeinen Wert prüfen](prompts/05-steuererklaerung/72-grundsteuerwert-niedrigerer-wert.md) |
| 73 | [Erbschaft- und Schenkungsteuer: Anzeigepflicht und Ersteinschätzung](prompts/05-steuererklaerung/73-erbschaftsteuer-anzeigepflicht.md) |
| 80 | [Gewerbesteuer-Zerlegung prüfen](prompts/05-steuererklaerung/80-gewerbesteuer-zerlegung.md) |
| 82 | [Behaltensfristen §§ 13a, 13b ErbStG überwachen](prompts/05-steuererklaerung/82-behaltensfristen-erbstg.md) |
| 89 | [Erhaltungsaufwand oder anschaffungsnahe Herstellungskosten](prompts/05-steuererklaerung/89-erhaltungsaufwand-abgrenzung.md) |
| 90 | [Privates Veräußerungsgeschäft § 23 EStG prüfen](prompts/05-steuererklaerung/90-privates-veraeusserungsgeschaeft.md) |
| 92 | [Sonderbetriebsvermögen bei der unentgeltlichen Übertragung](prompts/05-steuererklaerung/92-sonderbetriebsvermoegen-nachfolge.md) |
| 93 | [Grunderwerbsteuer bei Anteilsbewegungen: Anzeigepflicht und Frist](prompts/05-steuererklaerung/93-grunderwerbsteuer-anteilsbewegung.md) |

### Finanzamt, Fristen und Rechtsbehelf

Anträge, Bescheide, Einspruch, Betriebsprüfung.

| # | Prompt |
|---|--------|
| 31 | [Fristverlängerungsantrag entwerfen](prompts/06-finanzamt-fristen/31-fristverlaengerungsantrag.md) |
| 32 | [Steuerbescheid gegen Erklärung abgleichen](prompts/06-finanzamt-fristen/32-bescheid-abgleichen.md) |
| 33 | [Einspruchsbegründung formulieren](prompts/06-finanzamt-fristen/33-einspruchsbegruendung.md) |
| 34 | [Betriebsprüfung vorbereiten](prompts/06-finanzamt-fristen/34-betriebspruefung-vorbereiten.md) |
| 35 | [Wiedervorlage- und Fristenkonzept](prompts/06-finanzamt-fristen/35-fristenkonzept.md) |
| 36 | [Sachverhaltsdarstellung für das Finanzamt](prompts/06-finanzamt-fristen/36-sachverhaltsdarstellung-finanzamt.md) |
| 102 | [Elektronische Bekanntgabe nach § 122a AO: Umstellung und Fristenkontrolle](prompts/06-finanzamt-fristen/102-bekanntgabe-122a-ao.md) |

### GoBD, Kasse und Verfahrensdokumentation

Ordnungsmäßigkeit der Buchführung beim Mandanten.

| # | Prompt |
|---|--------|
| 37 | [Verfahrensdokumentation entwerfen](prompts/07-gobd-kasse/37-verfahrensdokumentation.md) |
| 38 | [GoBD-Checkliste Kassenführung](prompts/07-gobd-kasse/38-gobd-checkliste-kasse.md) |
| 39 | [Kontierungsrichtlinie für den Mandanten](prompts/07-gobd-kasse/39-kontierungsrichtlinie-mandant.md) |

### Mandantenkommunikation

Alles, was die Kanzlei an den Mandanten schreibt oder ihm erklärt.

| # | Prompt |
|---|--------|
| 01 | [Belegnachforderung in drei Eskalationsstufen](prompts/08-mandantenkommunikation/01-belegnachforderung-eskalation.md) |
| 06 | [BWA in Mandantensprache kommentieren](prompts/08-mandantenkommunikation/06-bwa-kommentar.md) |
| 11 | [Fachtext in Mandantensprache übersetzen](prompts/08-mandantenkommunikation/11-fachtext-in-mandantensprache.md) |
| 12 | [Mandantenrundschreiben E-Rechnungspflicht](prompts/08-mandantenkommunikation/12-e-rechnung-rundschreiben.md) |
| 13 | [Lange Mandanten-Mail verdichten](prompts/08-mandantenkommunikation/13-mandantenmail-verdichten.md) |
| 17 | [Jahres-Terminplan und Zulieferkalender](prompts/08-mandantenkommunikation/17-jahresterminplan-zulieferung.md) |
| 26 | [Merkblatt Belegkanäle](prompts/08-mandantenkommunikation/26-merkblatt-belegkanaele.md) |
| 27 | [Kurzanleitung: So reichen Sie Belege richtig ein](prompts/08-mandantenkommunikation/27-anleitung-belege-scannen.md) |
| 49 | [Kontaktkonzept gegen stille Mandantenabwanderung](prompts/08-mandantenkommunikation/49-mandantenkontakt-konzept.md) |

### Honorar und Forderungen

Leistung sichtbar machen, Honorar begründen, Außenstände einholen.

| # | Prompt |
|---|--------|
| 14 | [Leistungsnachweis als Anlage zur Honorarrechnung](prompts/09-honorar-forderungen/14-leistungsnachweis-honorarrechnung.md) |
| 15 | [Honorarbeschwerde und Honoraranpassung](prompts/09-honorar-forderungen/15-honorarbeschwerde-und-anpassung.md) |
| 16 | [Mahnstufen: Erinnerung bis Rechtsverfolgung](prompts/09-honorar-forderungen/16-mahnstufen-texte.md) |
| 46 | [Mandatsprofitabilität bewerten](prompts/09-honorar-forderungen/46-mandatsprofitabilitaet.md) |

### Kanzleiorganisation und Team

Interne Abläufe, Einarbeitung, Vertretung, Veränderungen.

| # | Prompt |
|---|--------|
| 23 | [Arbeitsanweisung aus Stichworten ausformulieren](prompts/10-kanzleiorganisation/23-arbeitsanweisung-ausformulieren.md) |
| 24 | [Vertretungsleitfaden je Mandant](prompts/10-kanzleiorganisation/24-vertretungsleitfaden.md) |
| 29 | [Onboarding-Fahrplan für neue Mitarbeiter](prompts/10-kanzleiorganisation/29-onboarding-neue-mitarbeiter.md) |
| 30 | [Übungsfälle mit Musterlösung erzeugen](prompts/10-kanzleiorganisation/30-uebungsfaelle-erzeugen.md) |
| 47 | [Telefon- und Erreichbarkeitskonzept](prompts/10-kanzleiorganisation/47-erreichbarkeitskonzept.md) |
| 48 | [Change-Kommunikation bei Tool-Einführung](prompts/10-kanzleiorganisation/48-change-kommunikation-tool.md) |
| 76 | [Die AVV-Anfrage des Mandanten beantworten](prompts/10-kanzleiorganisation/76-avv-anfrage-beantworten.md) |
| 77 | [Auskunftsersuchen nach Art. 15 DSGVO beantworten](prompts/10-kanzleiorganisation/77-auskunftsersuchen-art-15-dsgvo.md) |
| 83 | [Datenschutzvorfall: Bewertung, Meldung, Dokumentation](prompts/10-kanzleiorganisation/83-datenschutzvorfall.md) |
| 103 | [§ 62a StBerG: Dienstleister- und Werkzeugprüfung vor der Einführung](prompts/10-kanzleiorganisation/103-62a-dienstleisterpruefung.md) |
| 104 | [KI-Richtlinie für Mitarbeitende und KI-Kompetenz nach Art. 4 KI-VO](prompts/10-kanzleiorganisation/104-ki-richtlinie-kompetenz.md) |
| 105 | [Geldwäsche: Verdachtsmeldung vorbereiten und dokumentieren](prompts/10-kanzleiorganisation/105-gwg-verdachtsmeldung.md) |

### Mandatsbeginn und Mandatswechsel

Neumandat, Übernahme, Datenübergabe.

| # | Prompt |
|---|--------|
| 22 | [Kontenrahmen-Vergleich SKR03 ↔ SKR04](prompts/11-mandatsbeginn-wechsel/22-kontenrahmen-vergleich.md) |
| 68 | [Fragebogen zur steuerlichen Erfassung](prompts/11-mandatsbeginn-wechsel/68-fragebogen-steuerliche-erfassung.md) |
| 69 | [Mandatswechsel: Datenübernahme vom Vorberater](prompts/11-mandatsbeginn-wechsel/69-mandatswechsel-datenuebernahme.md) |

### Krise, Liquidität und Bank

Wirtschaftlich schwierige Lagen – der haftungskritischste Bereich.

| # | Prompt |
|---|--------|
| 65 | [Krisenindikatoren und Hinweisschreiben (nur Berufsträger)](prompts/12-krise-liquiditaet-bank/65-insolvenzreife-hinweisschreiben.md) |
| 66 | [Rollierende 13-Wochen-Liquiditätsplanung](prompts/12-krise-liquiditaet-bank/66-liquiditaetsplanung-13-wochen.md) |
| 67 | [Bankgespräch und Rating: Unterlagenpaket](prompts/12-krise-liquiditaet-bank/67-bankgespraech-unterlagenpaket.md) |
| 74 | [Zahlungsunfähigkeit: Datenanforderung und Statusgerüst für den Insolvenzrechtler (nur Berufsträger)](prompts/12-krise-liquiditaet-bank/74-zahlungsunfaehigkeit-datenaufbereitung.md) |
| 75 | [Krisenfrüherkennung nach § 1 StaRUG: Merkblatt und Frühwarnraster (nur Berufsträger)](prompts/12-krise-liquiditaet-bank/75-krisenfrueherkennung-starug.md) |

## Nach Rolle

### Buchhaltung und Steuerfachangestellte

| # | Prompt |
|---|--------|
| 02 | [Gebündelte Rückfrageliste zu unklaren Bankumsätzen](prompts/01-finanzbuchhaltung/02-rueckfrageliste-bankumsaetze.md) |
| 03 | [Buchungssatz klären und begründen (SKR03/SKR04)](prompts/01-finanzbuchhaltung/03-buchungssatz-klaeren.md) |
| 04 | [Umsatzsteuer-Sonderfall prüfen (§ 13b, i.g. Erwerb, § 25a, § 19)](prompts/02-umsatzsteuer/04-umsatzsteuer-sonderfall.md) |
| 05 | [UStVA-Abweichung systematisch eingrenzen](prompts/02-umsatzsteuer/05-ustva-abweichung-eingrenzen.md) |
| 10 | [Reisekosten- und Bewirtungsbeleg prüfen](prompts/01-finanzbuchhaltung/10-reisekosten-bewirtung-pruefen.md) |
| 18 | [Offene-Posten-Liste analysieren](prompts/01-finanzbuchhaltung/18-op-liste-analysieren.md) |
| 19 | [Dublettenprüfung auf Buchungs- und Stammdatenexporten](prompts/01-finanzbuchhaltung/19-dublettenpruefung.md) |
| 20 | [Summen- und Saldenliste auf Auffälligkeiten prüfen](prompts/01-finanzbuchhaltung/20-summen-salden-pruefen.md) |
| 21 | [Plausibilitätsprüfung EÜR-Zahlen vor Abgabe](prompts/03-jahresabschluss/21-euer-plausibilitaet.md) |
| 22 | [Kontenrahmen-Vergleich SKR03 ↔ SKR04](prompts/11-mandatsbeginn-wechsel/22-kontenrahmen-vergleich.md) |
| 25 | [Namens- und Stammdatenkonvention für Personenkonten](prompts/01-finanzbuchhaltung/25-stammdatenkonvention.md) |
| 28 | [Vier-Augen-Prüfroutine für OCR-erfasste Belege](prompts/01-finanzbuchhaltung/28-ocr-pruefroutine.md) |
| 50 | [Rückstellungs-Prüfschema zum Bilanzstichtag](prompts/03-jahresabschluss/50-rueckstellungen-pruefschema.md) |
| 51 | [Cut-off- und Nachlaufcheck zum Bilanzstichtag](prompts/03-jahresabschluss/51-cutoff-nachlaufcheck.md) |
| 52 | [Anlagevermögen und AfA-Wahlrechte plausibilisieren](prompts/03-jahresabschluss/52-anlagevermoegen-afa-wahlrechte.md) |
| 53 | [Investitionsabzugsbetrag § 7g EStG überwachen](prompts/03-jahresabschluss/53-investitionsabzugsbetrag-monitor.md) |
| 54 | [E-Bilanz: unverdichtete Kontennachweise vorbereiten](prompts/03-jahresabschluss/54-ebilanz-kontennachweise.md) |
| 57 | [Bauabzugsteuer § 48 EStG: Prüf- und Einbehaltsschema](prompts/05-steuererklaerung/57-bauabzugsteuer-pruefschema.md) |
| 58 | [Zusammenfassende Meldung und i.g. Lieferung abgleichen](prompts/02-umsatzsteuer/58-zusammenfassende-meldung-abgleich.md) |
| 71 | [Grundsteuer: Änderungsanzeigen erkennen und erstatten](prompts/05-steuererklaerung/71-grundsteuer-aenderungsanzeige.md) |
| 72 | [Grundsteuerwert: niedrigeren gemeinen Wert prüfen](prompts/05-steuererklaerung/72-grundsteuerwert-niedrigerer-wert.md) |
| 73 | [Erbschaft- und Schenkungsteuer: Anzeigepflicht und Ersteinschätzung](prompts/05-steuererklaerung/73-erbschaftsteuer-anzeigepflicht.md) |
| 80 | [Gewerbesteuer-Zerlegung prüfen](prompts/05-steuererklaerung/80-gewerbesteuer-zerlegung.md) |
| 82 | [Behaltensfristen §§ 13a, 13b ErbStG überwachen](prompts/05-steuererklaerung/82-behaltensfristen-erbstg.md) |
| 84 | [Gastronomie: Steuersatzaufteilung bei Kombiangeboten](prompts/02-umsatzsteuer/84-gastronomie-steuersatzaufteilung.md) |
| 85 | [E-Rechnungs-Umstellungsradar: Stichtag je Mandant](prompts/02-umsatzsteuer/85-erechnung-umstellungsradar.md) |
| 86 | [Fehlerhafte E-Rechnung: Fehlerklasse bestimmen und reklamieren](prompts/02-umsatzsteuer/86-erechnung-fehlerklasse.md) |
| 87 | [§ 14c UStG: unrichtiger Steuerausweis erkennen und berichtigen](prompts/02-umsatzsteuer/87-14c-unrichtiger-steuerausweis.md) |
| 88 | [Kleinunternehmer: Grenzen überwachen und Statuswechsel begleiten](prompts/02-umsatzsteuer/88-kleinunternehmer-grenzen.md) |
| 89 | [Erhaltungsaufwand oder anschaffungsnahe Herstellungskosten](prompts/05-steuererklaerung/89-erhaltungsaufwand-abgrenzung.md) |
| 90 | [Privates Veräußerungsgeschäft § 23 EStG prüfen](prompts/05-steuererklaerung/90-privates-veraeusserungsgeschaeft.md) |
| 91 | [Betriebsaufspaltung: jährliches Monitoring](prompts/03-jahresabschluss/91-betriebsaufspaltung-monitoring.md) |
| 92 | [Sonderbetriebsvermögen bei der unentgeltlichen Übertragung](prompts/05-steuererklaerung/92-sonderbetriebsvermoegen-nachfolge.md) |
| 93 | [Grunderwerbsteuer bei Anteilsbewegungen: Anzeigepflicht und Frist](prompts/05-steuererklaerung/93-grunderwerbsteuer-anteilsbewegung.md) |
| 94 | [Verdeckte Gewinnausschüttung: Vertragsdurchsicht](prompts/03-jahresabschluss/94-vga-vertragsdurchsicht.md) |

### Lohnsachbearbeitung

| # | Prompt |
|---|--------|
| 07 | [Lohn-Sonderfall einordnen: Steuer- und SV-Pflicht](prompts/04-lohn/07-lohn-sonderfall-einordnen.md) |
| 08 | [Lohnabrechnung für den Arbeitnehmer erklären](prompts/04-lohn/08-lohnabrechnung-erklaeren.md) |
| 40 | [Merkblatt Sachbezüge: Freigrenze und Aufmerksamkeiten](prompts/04-lohn/40-merkblatt-sachbezuege.md) |
| 41 | [SV-Fehlerprotokoll im Klartext erklären](prompts/04-lohn/41-sv-fehlerprotokoll-erklaeren.md) |
| 42 | [Anschreiben an Krankenkasse, Behörde oder Amt](prompts/04-lohn/42-anschreiben-kasse-behoerde.md) |
| 43 | [FAQ zur Lohnabrechnung für die Belegschaft des Mandanten](prompts/04-lohn/43-faq-lohnabrechnung.md) |
| 44 | [Stichtagsplan und Erinnerungstexte für Lohnzulieferungen](prompts/04-lohn/44-stichtagsplan-lohn.md) |
| 63 | [Elektro-Dienstwagen: Bewertung und Lohnabrechnungsfolgen](prompts/04-lohn/63-elektro-dienstwagen.md) |
| 64 | [Minijob und Übergangsbereich: Grenzen überwachen](prompts/04-lohn/64-minijob-uebergangsbereich.md) |
| 95 | [Lohn-Jahreswechsel: Stammdaten- und Umstellungsprüfung](prompts/04-lohn/95-lohn-jahreswechsel.md) |
| 96 | [Aktivrente: Voraussetzungen, Nachweise, Abrechnungsfolgen](prompts/04-lohn/96-aktivrente.md) |
| 97 | [Betriebsprüfung der Rentenversicherung vorbereiten](prompts/04-lohn/97-drv-betriebspruefung.md) |
| 98 | [Phantomlohn: Auslöser erkennen und Grundlage klären](prompts/04-lohn/98-phantomlohn-screening.md) |
| 99 | [Statusfeststellung: Indizienerhebung für § 7a SGB IV](prompts/04-lohn/99-statusfeststellung-indizien.md) |
| 100 | [A1 und Tätigkeit im Ausland: Entscheidungsbaum](prompts/04-lohn/100-a1-taetigkeit-ausland.md) |
| 101 | [Lohnpfändung: Pflichten des Arbeitgebers als Drittschuldner](prompts/04-lohn/101-lohnpfaendung-drittschuldner.md) |

### Steuerberaterinnen und Steuerberater

| # | Prompt |
|---|--------|
| 06 | [BWA in Mandantensprache kommentieren](prompts/08-mandantenkommunikation/06-bwa-kommentar.md) |
| 12 | [Mandantenrundschreiben E-Rechnungspflicht](prompts/08-mandantenkommunikation/12-e-rechnung-rundschreiben.md) |
| 32 | [Steuerbescheid gegen Erklärung abgleichen](prompts/06-finanzamt-fristen/32-bescheid-abgleichen.md) |
| 33 | [Einspruchsbegründung formulieren](prompts/06-finanzamt-fristen/33-einspruchsbegruendung.md) |
| 34 | [Betriebsprüfung vorbereiten](prompts/06-finanzamt-fristen/34-betriebspruefung-vorbereiten.md) |
| 36 | [Sachverhaltsdarstellung für das Finanzamt](prompts/06-finanzamt-fristen/36-sachverhaltsdarstellung-finanzamt.md) |
| 37 | [Verfahrensdokumentation entwerfen](prompts/07-gobd-kasse/37-verfahrensdokumentation.md) |
| 38 | [GoBD-Checkliste Kassenführung](prompts/07-gobd-kasse/38-gobd-checkliste-kasse.md) |
| 39 | [Kontierungsrichtlinie für den Mandanten](prompts/07-gobd-kasse/39-kontierungsrichtlinie-mandant.md) |
| 55 | [Anhang kleine Kapitalgesellschaft: Pflichtangaben](prompts/03-jahresabschluss/55-anhang-kleine-kapitalgesellschaft.md) |
| 59 | [Kapitalertragsteuer bei Gewinnausschüttung](prompts/05-steuererklaerung/59-kapitalertragsteuer-ausschuettung.md) |
| 60 | [Photovoltaik: Fallklärung Steuerbefreiung und Entnahme](prompts/05-steuererklaerung/60-photovoltaik-fallklaerung.md) |
| 61 | [Krypto: Nachweise anfordern und Steuerreport prüfen](prompts/05-steuererklaerung/61-krypto-nachweise.md) |
| 62 | [Verbilligte Vermietung: Entgeltlichkeitsprüfung](prompts/05-steuererklaerung/62-verbilligte-vermietung.md) |
| 65 | [Krisenindikatoren und Hinweisschreiben (nur Berufsträger)](prompts/12-krise-liquiditaet-bank/65-insolvenzreife-hinweisschreiben.md) |
| 66 | [Rollierende 13-Wochen-Liquiditätsplanung](prompts/12-krise-liquiditaet-bank/66-liquiditaetsplanung-13-wochen.md) |
| 67 | [Bankgespräch und Rating: Unterlagenpaket](prompts/12-krise-liquiditaet-bank/67-bankgespraech-unterlagenpaket.md) |
| 68 | [Fragebogen zur steuerlichen Erfassung](prompts/11-mandatsbeginn-wechsel/68-fragebogen-steuerliche-erfassung.md) |
| 69 | [Mandatswechsel: Datenübernahme vom Vorberater](prompts/11-mandatsbeginn-wechsel/69-mandatswechsel-datenuebernahme.md) |
| 70 | [Going-Concern und Auftragsart bei der Abschlusserstellung (nur Berufsträger)](prompts/03-jahresabschluss/70-going-concern-auftragsart.md) |
| 71 | [Grundsteuer: Änderungsanzeigen erkennen und erstatten](prompts/05-steuererklaerung/71-grundsteuer-aenderungsanzeige.md) |
| 72 | [Grundsteuerwert: niedrigeren gemeinen Wert prüfen](prompts/05-steuererklaerung/72-grundsteuerwert-niedrigerer-wert.md) |
| 73 | [Erbschaft- und Schenkungsteuer: Anzeigepflicht und Ersteinschätzung](prompts/05-steuererklaerung/73-erbschaftsteuer-anzeigepflicht.md) |
| 74 | [Zahlungsunfähigkeit: Datenanforderung und Statusgerüst für den Insolvenzrechtler (nur Berufsträger)](prompts/12-krise-liquiditaet-bank/74-zahlungsunfaehigkeit-datenaufbereitung.md) |
| 75 | [Krisenfrüherkennung nach § 1 StaRUG: Merkblatt und Frühwarnraster (nur Berufsträger)](prompts/12-krise-liquiditaet-bank/75-krisenfrueherkennung-starug.md) |
| 80 | [Gewerbesteuer-Zerlegung prüfen](prompts/05-steuererklaerung/80-gewerbesteuer-zerlegung.md) |
| 82 | [Behaltensfristen §§ 13a, 13b ErbStG überwachen](prompts/05-steuererklaerung/82-behaltensfristen-erbstg.md) |
| 84 | [Gastronomie: Steuersatzaufteilung bei Kombiangeboten](prompts/02-umsatzsteuer/84-gastronomie-steuersatzaufteilung.md) |
| 85 | [E-Rechnungs-Umstellungsradar: Stichtag je Mandant](prompts/02-umsatzsteuer/85-erechnung-umstellungsradar.md) |
| 86 | [Fehlerhafte E-Rechnung: Fehlerklasse bestimmen und reklamieren](prompts/02-umsatzsteuer/86-erechnung-fehlerklasse.md) |
| 87 | [§ 14c UStG: unrichtiger Steuerausweis erkennen und berichtigen](prompts/02-umsatzsteuer/87-14c-unrichtiger-steuerausweis.md) |
| 88 | [Kleinunternehmer: Grenzen überwachen und Statuswechsel begleiten](prompts/02-umsatzsteuer/88-kleinunternehmer-grenzen.md) |
| 89 | [Erhaltungsaufwand oder anschaffungsnahe Herstellungskosten](prompts/05-steuererklaerung/89-erhaltungsaufwand-abgrenzung.md) |
| 90 | [Privates Veräußerungsgeschäft § 23 EStG prüfen](prompts/05-steuererklaerung/90-privates-veraeusserungsgeschaeft.md) |
| 91 | [Betriebsaufspaltung: jährliches Monitoring](prompts/03-jahresabschluss/91-betriebsaufspaltung-monitoring.md) |
| 92 | [Sonderbetriebsvermögen bei der unentgeltlichen Übertragung](prompts/05-steuererklaerung/92-sonderbetriebsvermoegen-nachfolge.md) |
| 93 | [Grunderwerbsteuer bei Anteilsbewegungen: Anzeigepflicht und Frist](prompts/05-steuererklaerung/93-grunderwerbsteuer-anteilsbewegung.md) |
| 94 | [Verdeckte Gewinnausschüttung: Vertragsdurchsicht](prompts/03-jahresabschluss/94-vga-vertragsdurchsicht.md) |
| 96 | [Aktivrente: Voraussetzungen, Nachweise, Abrechnungsfolgen](prompts/04-lohn/96-aktivrente.md) |
| 97 | [Betriebsprüfung der Rentenversicherung vorbereiten](prompts/04-lohn/97-drv-betriebspruefung.md) |
| 99 | [Statusfeststellung: Indizienerhebung für § 7a SGB IV](prompts/04-lohn/99-statusfeststellung-indizien.md) |
| 100 | [A1 und Tätigkeit im Ausland: Entscheidungsbaum](prompts/04-lohn/100-a1-taetigkeit-ausland.md) |
| 101 | [Lohnpfändung: Pflichten des Arbeitgebers als Drittschuldner](prompts/04-lohn/101-lohnpfaendung-drittschuldner.md) |
| 102 | [Elektronische Bekanntgabe nach § 122a AO: Umstellung und Fristenkontrolle](prompts/06-finanzamt-fristen/102-bekanntgabe-122a-ao.md) |

### Sekretariat und Büroorganisation

| # | Prompt |
|---|--------|
| 01 | [Belegnachforderung in drei Eskalationsstufen](prompts/08-mandantenkommunikation/01-belegnachforderung-eskalation.md) |
| 09 | [Unterlagen-Checkliste Einkommensteuer](prompts/05-steuererklaerung/09-unterlagen-checkliste-est.md) |
| 13 | [Lange Mandanten-Mail verdichten](prompts/08-mandantenkommunikation/13-mandantenmail-verdichten.md) |
| 16 | [Mahnstufen: Erinnerung bis Rechtsverfolgung](prompts/09-honorar-forderungen/16-mahnstufen-texte.md) |
| 17 | [Jahres-Terminplan und Zulieferkalender](prompts/08-mandantenkommunikation/17-jahresterminplan-zulieferung.md) |
| 27 | [Kurzanleitung: So reichen Sie Belege richtig ein](prompts/08-mandantenkommunikation/27-anleitung-belege-scannen.md) |
| 31 | [Fristverlängerungsantrag entwerfen](prompts/06-finanzamt-fristen/31-fristverlaengerungsantrag.md) |
| 47 | [Telefon- und Erreichbarkeitskonzept](prompts/10-kanzleiorganisation/47-erreichbarkeitskonzept.md) |
| 56 | [Offenlegung und Ordnungsgeldabwehr](prompts/03-jahresabschluss/56-offenlegung-ordnungsgeld.md) |

### Kanzleileitung

| # | Prompt |
|---|--------|
| 14 | [Leistungsnachweis als Anlage zur Honorarrechnung](prompts/09-honorar-forderungen/14-leistungsnachweis-honorarrechnung.md) |
| 15 | [Honorarbeschwerde und Honoraranpassung](prompts/09-honorar-forderungen/15-honorarbeschwerde-und-anpassung.md) |
| 23 | [Arbeitsanweisung aus Stichworten ausformulieren](prompts/10-kanzleiorganisation/23-arbeitsanweisung-ausformulieren.md) |
| 24 | [Vertretungsleitfaden je Mandant](prompts/10-kanzleiorganisation/24-vertretungsleitfaden.md) |
| 26 | [Merkblatt Belegkanäle](prompts/08-mandantenkommunikation/26-merkblatt-belegkanaele.md) |
| 29 | [Onboarding-Fahrplan für neue Mitarbeiter](prompts/10-kanzleiorganisation/29-onboarding-neue-mitarbeiter.md) |
| 30 | [Übungsfälle mit Musterlösung erzeugen](prompts/10-kanzleiorganisation/30-uebungsfaelle-erzeugen.md) |
| 35 | [Wiedervorlage- und Fristenkonzept](prompts/06-finanzamt-fristen/35-fristenkonzept.md) |
| 46 | [Mandatsprofitabilität bewerten](prompts/09-honorar-forderungen/46-mandatsprofitabilitaet.md) |
| 48 | [Change-Kommunikation bei Tool-Einführung](prompts/10-kanzleiorganisation/48-change-kommunikation-tool.md) |
| 49 | [Kontaktkonzept gegen stille Mandantenabwanderung](prompts/08-mandantenkommunikation/49-mandantenkontakt-konzept.md) |
| 76 | [Die AVV-Anfrage des Mandanten beantworten](prompts/10-kanzleiorganisation/76-avv-anfrage-beantworten.md) |
| 77 | [Auskunftsersuchen nach Art. 15 DSGVO beantworten](prompts/10-kanzleiorganisation/77-auskunftsersuchen-art-15-dsgvo.md) |
| 83 | [Datenschutzvorfall: Bewertung, Meldung, Dokumentation](prompts/10-kanzleiorganisation/83-datenschutzvorfall.md) |
| 85 | [E-Rechnungs-Umstellungsradar: Stichtag je Mandant](prompts/02-umsatzsteuer/85-erechnung-umstellungsradar.md) |
| 102 | [Elektronische Bekanntgabe nach § 122a AO: Umstellung und Fristenkontrolle](prompts/06-finanzamt-fristen/102-bekanntgabe-122a-ao.md) |
| 103 | [§ 62a StBerG: Dienstleister- und Werkzeugprüfung vor der Einführung](prompts/10-kanzleiorganisation/103-62a-dienstleisterpruefung.md) |
| 104 | [KI-Richtlinie für Mitarbeitende und KI-Kompetenz nach Art. 4 KI-VO](prompts/10-kanzleiorganisation/104-ki-richtlinie-kompetenz.md) |
| 105 | [Geldwäsche: Verdachtsmeldung vorbereiten und dokumentieren](prompts/10-kanzleiorganisation/105-gwg-verdachtsmeldung.md) |

### Alle

| # | Prompt |
|---|--------|
| 11 | [Fachtext in Mandantensprache übersetzen](prompts/08-mandantenkommunikation/11-fachtext-in-mandantensprache.md) |

---

## Nach Anlass

### Der Mandant liefert nicht

01 Belegnachforderung · 02 Bankumsatz-Rückfragen · 17 Jahres-Terminplan ·
26 Merkblatt Belegkanäle · 27 Anleitung Belege einreichen ·
44 Stichtagsplan Lohn

### Ich bin mir fachlich unsicher

03 Buchungssatz · 04 Umsatzsteuer-Sonderfall · 07 Lohn-Sonderfall ·
21 EÜR-Plausibilität · 22 Kontenrahmen-Vergleich · 30 Übungsfälle zum Lernen ·
50 Rückstellungen · 57 Bauabzugsteuer · 59 Kapitalertragsteuer ·
60 Photovoltaik · 62 Verbilligte Vermietung · 63 Elektro-Dienstwagen ·
64 Minijob und Übergangsbereich · 80 Gewerbesteuer-Zerlegung ·
84 Gastronomie: Steuersatzaufteilung · 85 E-Rechnungs-Stichtag je Mandant ·
87 § 14c unrichtiger Steuerausweis · 88 Kleinunternehmer-Grenzen ·
89 Erhaltungsaufwand oder Herstellungskosten ·
90 Privates Veräußerungsgeschäft · 92 Sonderbetriebsvermögen ·
93 Grunderwerbsteuer bei Anteilsbewegungen · 96 Aktivrente ·
98 Phantomlohn-Auslöser · 99 Statusfeststellung ·
100 A1 und Tätigkeit im Ausland · 101 Lohnpfändung

### Jahresabschluss steht an

50 Rückstellungen · 51 Cut-off und Nachlauf · 52 Anlagevermögen und AfA ·
53 Investitionsabzugsbetrag · 54 E-Bilanz-Kontennachweise · 55 Anhang ·
56 Offenlegung · 70 Going-Concern und Auftragsart (nur Berufsträger) ·
91 Betriebsaufspaltung-Monitoring · 94 Verdeckte Gewinnausschüttung

### Das Lohnjahr wechselt

44 Stichtagsplan Lohn · 64 Minijob und Übergangsbereich ·
95 Lohn-Jahreswechsel: Stammdaten und Umstellung · 96 Aktivrente

### Dem Mandanten geht es wirtschaftlich schlecht

65 Krisenindikatoren und Hinweisschreiben (nur Berufsträger) ·
66 13-Wochen-Liquiditätsplanung · 67 Bankgespräch und Rating ·
70 Going-Concern und Auftragsart (nur Berufsträger) ·
74 Zahlungsunfähigkeit: Datenanforderung und Statusgerüst (nur Berufsträger) ·
75 Krisenfrüherkennung nach § 1 StaRUG (nur Berufsträger) ·
18 Offene Posten

### Ein Mandat beginnt oder wechselt

68 Fragebogen zur steuerlichen Erfassung · 69 Mandatswechsel und Datenübernahme ·
22 Kontenrahmen-Vergleich · 09 Unterlagen-Checkliste · 17 Zulieferkalender

### Etwas stimmt nicht

05 UStVA-Abweichung · 18 Offene Posten · 19 Dubletten ·
20 Summen- und Saldenliste · 28 OCR-Prüfroutine · 41 SV-Fehlerprotokoll ·
86 Fehlerhafte E-Rechnung · 87 § 14c unrichtiger Steuerausweis

### Ich muss etwas erklären

06 BWA-Kommentar · 08 Lohnabrechnung erklären · 11 Fachtext übersetzen ·
12 E-Rechnung · 40 Merkblatt Sachbezüge · 43 FAQ Lohnabrechnung

### Post vom Finanzamt oder von einer Behörde

31 Fristverlängerung · 32 Bescheid abgleichen · 33 Einspruchsbegründung ·
34 Betriebsprüfung · 36 Sachverhaltsdarstellung · 42 Anschreiben an Kasse/Behörde ·
72 Grundsteuerwert: niedrigerer gemeiner Wert ·
101 Lohnpfändung: Drittschuldnerpflichten ·
102 Elektronische Bekanntgabe nach § 122a AO

### Es geht ums Geld

14 Leistungsnachweis · 15 Honorarbeschwerde und -anpassung ·
16 Mahnstufen · 18 Offene Posten · 46 Mandatsprofitabilität

### Die Kanzlei soll besser laufen

23 Arbeitsanweisung · 24 Vertretungsleitfaden · 25 Stammdatenkonvention ·
29 Onboarding · 35 Fristenkonzept · 47 Erreichbarkeitskonzept ·
48 Change-Kommunikation · 49 Mandantenkontakt ·
102 Elektronische Bekanntgabe und Fristenkontrolle ·
103 § 62a StBerG: Dienstleisterprüfung · 104 KI-Richtlinie und KI-Kompetenz

### Prüfungssicherheit herstellen

10 Reisekosten und Bewirtung · 28 OCR-Prüfroutine ·
34 Betriebsprüfung · 37 Verfahrensdokumentation · 38 GoBD Kasse ·
39 Kontierungsrichtlinie · 84 Gastronomie: Steuersatzaufteilung ·
89 Erhaltungsaufwand oder Herstellungskosten ·
91 Betriebsaufspaltung-Monitoring · 94 Verdeckte Gewinnausschüttung ·
97 Prüfung der Rentenversicherung

### Die Rentenversicherung prüft

64 Minijob und Übergangsbereich · 97 Prüfung der Rentenversicherung vorbereiten ·
98 Phantomlohn-Auslöser · 99 Statusfeststellung ·
100 A1 und Tätigkeit im Ausland

### Der Mandant hat eine Immobilie gekauft, verkauft oder saniert

57 Bauabzugsteuer · 62 Verbilligte Vermietung ·
71 Grundsteuer-Änderungsanzeigen · 72 Grundsteuerwert: niedrigerer gemeiner Wert ·
89 Erhaltungsaufwand oder Herstellungskosten ·
90 Privates Veräußerungsgeschäft

### Der Mandant übergibt sein Unternehmen oder überträgt Anteile

73 Erbschaft- und Schenkungsteuer: Anzeigepflicht ·
82 Behaltensfristen §§ 13a, 13b ErbStG ·
91 Betriebsaufspaltung-Monitoring · 92 Sonderbetriebsvermögen ·
93 Grunderwerbsteuer bei Anteilsbewegungen

### Etwas ist anzuzeigen, nicht zu erklären

71 Grundsteuer-Änderungsanzeigen · 73 Erbschaft- und Schenkungsteuer:
Anzeigepflicht · 82 Behaltensfristen §§ 13a, 13b ErbStG ·
93 Grunderwerbsteuer bei Anteilsbewegungen

### Die Kanzlei steht selbst in der Pflicht: Datenschutz und Geldwäsche

76 AVV-Anfrage des Mandanten · 77 Auskunftsersuchen nach Art. 15 DSGVO ·
83 Datenschutzvorfall · 103 § 62a StBerG: Dienstleisterprüfung ·
104 KI-Richtlinie und KI-Kompetenz · 105 Geldwäsche: Verdachtsmeldung

---

## Prompts, die zusammen arbeiten

- **17 → 01 → 44** – Terminplan aufstellen, bei Ausbleiben eskalieren, für den Lohn stichtagsgenau.
- **09 → 01** – Unterlagen anfordern, dann gezielt nachfassen.
- **19 → 25** – Dubletten finden, dann die Konvention festlegen, die sie verhindert.
- **32 → 33 → 36** – Bescheid prüfen, Einspruch begründen, Sachverhalt darstellen.
- **14 → 15 → 16** – Rechnung erklären, Einwand beantworten, notfalls mahnen.
- **05 → 23** – Fehlerursache finden, daraus eine Arbeitsanweisung machen.
- **37 ↔ 38 ↔ 39** – Verfahrensdokumentation, Kassenprüfung und Kontierungsregeln greifen ineinander.
- **35** ist die Grundsatzdatei für alles Fristbezogene (31, 32, 33, 34, 42, 44, 53,
  56, 93, 100, 101, 102).
- **65 → 66 → 67** – Krisenindikatoren erkennen, Liquidität planen, gegenüber der
  Bank erläutern. 66 und 06 brechen ab und verweisen auf 65, sobald
  Krisenindikatoren auftreten; jede Weitergabe an eine Bank läuft über 67.
- **69 → 22 → 68** – Mandat übernehmen, Kontenrahmen überleiten, bei Neugründung
  die Weichen stellen.
- **63 ↔ 64** – Der Sachbezug Fahrzeug kann die Geringfügigkeitsgrenze reißen;
  63 bricht dann ab und verweist auf 64.
- **12 → 85 → 86** – Den Mandantenstamm über die E-Rechnungspflicht informieren,
  je Mandant den eigenen Ausstellungsstichtag bestimmen, dann den Fehlerfall in
  der Eingangsrechnung einordnen. 85 verweist für die Information ausdrücklich
  auf 12 zurück.
- **04 → 87** – 87 setzt die zutreffende umsatzsteuerliche Behandlung des
  Umsatzes voraus und verweist dafür auf 04.
- **52 ↔ 89** – Die Gebäude-Variante in 52 verweist für Erwerbe innerhalb des
  maßgeblichen Zeitraums auf 89; 89 ergänzt 52 und verweist zurück.
- **91 → 22** – Die Erstprüfung im Neumandat benennt die Unterlagen, die vom
  Vorberater anzufordern sind, und ergänzt damit 22.
- **94 → 34** – Die Vereinbarungen mit dem Gesellschafter-Geschäftsführer
  durchsehen, bevor die Betriebsprüfung sie durchsieht; 94 ergänzt 34.
- **95 → 64 · 95 → 99** – Der Jahreswechsel stellt die Stammdaten um und legt die
  offenen Weichenstellungen offen: geringfügige Beschäftigung und
  Übergangsbereich laufen in 64 weiter, Statusfragen in 99. 95 stellt die Frage
  ausdrücklich, entscheidet sie aber nicht.
- **97 ↔ 98 ↔ 99** – Die Vorbereitung der Prüfung nach § 28p SGB IV verweist für
  Auslöser nicht verbeitragten Entgelts auf 98 und für offene Statusfragen auf
  99; 98 und 99 geben ihre Ergebnisse in 97 zurück. 97 nennt daneben 64 für
  geringfügige Beschäftigungen.
- **97 neben 34** – 97 grenzt sich ausdrücklich ab: Prüfung des Trägers der
  Rentenversicherung (§ 28p SGB IV) hier, steuerliche Außenprüfung (§§ 193 ff. AO)
  in 34. Getrennte Prüffelder, getrennte Verfahrensregeln, getrennte Prompts.
- **100 → 44 · 100 → 97** – Die Tätigkeit im Ausland ergänzt 44 um den Zulieferweg
  und 97 um ein Prüffeld: fehlende A1-Bescheinigungen fallen regelmäßig erst in
  der Prüfung der Rentenversicherung auf.
- **101 vor 07** – Für Pfändungssachverhalte ist 101 vorrangig; 07 bleibt auf die
  steuer- und beitragsrechtliche Einordnung sonstiger Lohn-Sonderfälle beschränkt
  und behandelt die Drittschuldnerpflichten nicht. 101 ergänzt 44 um den
  Zulieferweg für Pfändungsunterlagen.
- **102 → 35 → 32 → 33** – 102 regelt nur den Zugangsweg der elektronischen
  Bekanntgabe und hängt sich in das allgemeine Fristenkonzept 35 ein, statt es zu
  ersetzen; 32 und 33 bauen auf einem fristgerecht bemerkten Bescheid auf.
- **104 → 103** – Auf die Positivliste der KI-Richtlinie gehört nur ein nach
  § 62a StBerG geprüftes Werkzeug; 103 übergibt sein Prüfergebnis an 104, und
  ein Auftragsverarbeitungsvertrag allein trägt die Aufnahme nicht.
- **70 → 74 · 70 → 65 · 70 → 66** – 70 entscheidet über Auftragsart und
  Fortführungsannahme und verweist ausdrücklich weiter: die Datenanforderung für
  den Insolvenzrechtler an 74, das Hinweisschreiben samt Handaktenvermerk an 65,
  die Zahlengrundlage an 66. Ob ein Insolvenzgrund vorliegt, prüft keiner der
  vier Prompts – das ist Rechtsdienstleistung.
- **74 ↔ 75** – Beide grenzen sich gegenseitig ab: 74 bereitet den
  Liquiditätsstatus für den Insolvenzrechtler auf, 75 baut nur das Frühwarnraster
  nach § 1 StaRUG. 75 nennt 74 in der Abgrenzung, 74 nennt 75 im Anschluss;
  sobald Krisenindikatoren auftreten, beginnt in beiden Fällen 65.
- **71 ↔ 72** – Die Änderungsanzeige und der Nachweis eines niedrigeren gemeinen
  Werts verweisen wechselseitig aufeinander; 72 führt für den Rechtsbehelf
  weiter zu 32 und 33.
- **82 → 92 · 82 → 73** – Die unentgeltliche Weiterübertragung bricht die
  Behaltensfrist nicht; 82 verweist für die ertragsteuerliche Seite auf 92 und
  für die dadurch ausgelöste neue Anzeigepflicht auf 73.
- **84 → 87** – 84 ordnet Kombiangebote den Steuersätzen zu und hört dort auf;
  liegen bereits Belege mit unrichtigem Steuerausweis vor, übergibt es
  ausdrücklich an 87, bevor weitere Belege ausgegeben werden.
- **76 ↔ 77 → 103** – 76 klärt die Rolle der Kanzlei gegenüber dem Mandanten,
  77 die Auskunft an eine betroffene Person; beide verweisen für die eigenen
  Dienstleister der Kanzlei auf 103 und aufeinander.
- **83 → 103 · 83 → 104** – 83 bearbeitet den Vorfall; ergibt er eine Lücke bei
  einem Werkzeug oder in der Richtlinie, geht der Punkt an 103 (§ 62a StBerG)
  und an 104 (KI-Richtlinie) und wird dort abgearbeitet.

## Nicht enthalten

**45 Mandatsniederlegung** – zurückgestellt. Eine Mandatsbeendigung ist
berufsrechtlich voraussetzungsvoll (Kündigung zur Unzeit, Herausgabepflichten,
Zurückbehaltungsrecht) und für einen KI-Entwurf nur begrenzt geeignet.
Steht in `ENTSCHEIDUNGEN.md` zur Entscheidung.

**78 Ausbildungs- und Fortbildungsplan für die Kanzlei** – als Kandidat
dokumentiert, aber bewusst nicht umgesetzt, weil der Kern Personalplanung und
Nachweisführung ist und das Umfeld bereits von 29 und 30 abgedeckt wird.

**79 OSS-Quartalsmeldung und Lieferschwelle** – als Kandidat dokumentiert, aber
bewusst nicht umgesetzt, weil der Kern der Abgleich von Melde-, Retouren- und
Marktplatzdaten ist, also eine Auswertung im System und kein Prompt.

**81 Vorsteuervergütung im Ausland** – als Kandidat dokumentiert, aber bewusst
nicht umgesetzt, weil der Fall im Wesentlichen Fristenüberwachung und
Belegsammlung ist und dafür 35 trägt.
