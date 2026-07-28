# Prompts für Steuerberater

Praxistaugliche KI-Prompts für Steuerkanzleien, die mit DATEV arbeiten.
Zum Kopieren, Ausfüllen, Einsetzen.

---

## Für wen

Für alle, die in einer deutschen Steuerkanzlei arbeiten:

- **Buchhaltung und Steuerfachangestellte** – Kontierung, Belegklärung, Rückfragen an Mandanten
- **Lohnsachbearbeitung** – Sonderfälle einordnen, Abrechnungen erklären, Zulieferungen einfordern
- **Steuerberaterinnen und Steuerberater** – Auswertungen kommentieren, Sachverhalte prüfen, Mandanten verständlich informieren
- **Sekretariat und Kanzleiorganisation** – Fristen, Nachforderungen, wiederkehrende Korrespondenz
- **Kanzleileitung** – Arbeitsanweisungen, Einarbeitung, Prozessdokumentation

Vorkenntnisse in KI-Werkzeugen sind nicht nötig. Wer einen Text in ein
Chatfenster einfügen kann, kann diese Prompts benutzen.

## Wofür

Jeder Prompt löst ein Problem, das im Kanzleialltag regelmäßig wiederkehrt und
jedes Mal von Hand erledigt wird. Die Themen sind nicht erfunden, sondern aus
Foren, Fachdiensten und Kanzleiblogs recherchiert – unter anderem aus der
DATEV-Community.

**68 Prompts.** Die vollständige Übersicht nach Rolle, Anlass und Prompt-Ketten
steht in [INDEX.md](INDEX.md).

| Bereich | Was die Prompts leisten |
|---------|-------------------------|
| **Belege und Mandantenzulieferung** | Fehlende Unterlagen in Eskalationsstufen nachfordern; unklare Bankumsätze gebündelt statt einzeln klären; Belegkanäle und Scan-Regeln festlegen |
| **Buchführung** | Buchungssätze in SKR03/SKR04 begründen; Umsatzsteuer-Sonderfälle nach Prüfschema einordnen; UStVA-Abweichungen eingrenzen; Kontenrahmen bei Mandatsübernahme überleiten |
| **Analyse exportierter Daten** | Offene Posten nach Alter und Risiko, Dubletten in Buchungen und Stammdaten, Summen- und Saldenliste, EÜR-Plausibilität vor Abgabe |
| **Lohn** | Sonderfälle lohnsteuerlich und sozialversicherungsrechtlich prüfen; Abrechnungen erklären; SV-Fehlerprotokolle entschlüsseln; Stichtagspläne und Behördenanschreiben |
| **Steuererklärung, Bescheide, Prüfung** | Unterlagen-Checklisten je Mandantentyp; Bescheid gegen Erklärung abgleichen; Einspruch begründen; Fristverlängerung; Betriebsprüfung vorbereiten |
| **GoBD, Kasse, Dokumentation** | Verfahrensdokumentation entwerfen; Kassenführung prüfen; Kontierungsrichtlinie und Sachbezugs-Merkblatt für den Mandanten |
| **Auswertung und Kommunikation** | BWA in Mandantensprache kommentieren; Fachtexte übersetzen; E-Rechnungspflicht erklären; lange Mandantenmails zu Aufgaben und Fristen verdichten |
| **Honorar** | Leistungsnachweis zur Rechnung; Honorarbeschwerde und -anpassung; Mahnstufen mit berufsrechtlichen Grenzen |
| **Kanzleiorganisation** | Arbeitsanweisungen, Vertretungsleitfäden, Fristenkonzept, Onboarding, Übungsfälle, Erreichbarkeit, Change-Kommunikation, Mandantenbindung |

## Wofür nicht

Diese Prompts sind **kein Ersatz für steuerliche Beratung** und **keine
verbindliche Auskunft**. Sie erzeugen Entwürfe, Prüfschemata und Textvorlagen.
Die fachliche Verantwortung bleibt vollständig bei der Kanzlei.

Sie können außerdem nicht:

- auf DATEV-Daten zugreifen oder in DATEV buchen
- technische Probleme lösen (Installation, Updates, Bankabruf, Lizenzen)
- Rechtsstände garantieren – Pauschbeträge, Freigrenzen und Beitragsbemessungsgrenzen ändern sich jährlich

## So benutzt du sie

1. Passenden Prompt über [INDEX.md](INDEX.md) suchen und in `prompts/<kategorie>/` öffnen.
2. Den Block unter **## Prompt** vollständig kopieren.
3. Alle Platzhalter in eckigen Klammern ersetzen – `[MANDANT]`, `[ZEITRAUM]`, `[BETRAG]`.
4. In dein KI-Werkzeug einfügen und ausführen.
5. Den Abschnitt **## Qualitätssicherung** durchgehen, bevor das Ergebnis die Kanzlei verlässt.

Jede Datei hat denselben Aufbau: Problem, Rolle, DATEV-Bezug, benötigte Daten,
Datensparsamkeitshinweis, der eigentliche Prompt, Anwendung, Qualitätssicherung,
Varianten.

## Datenschutz und Berufsrecht

**Vor dem Einfügen anonymisieren.** Mandantenname, Anschrift, Steuernummer,
Personalnummern, IBAN und Namen Dritter durch Platzhalter ersetzen
(`Mandant A`, `AN 1`, `Konto ****1234`). Für die fachliche Arbeit genügen
Sachverhalt, Beträge, Konten und Daten.

Der Einsatz von KI-Werkzeugen mit Mandantenbezug berührt die berufsrechtliche
Verschwiegenheitspflicht (§ 57 StBerG, § 203 StGB), die Einbindung von
Dienstleistern (§ 62a StBerG), die DSGVO und die KI-Kompetenzpflicht des
Art. 4 KI-VO. Ob und mit welchen Daten ein bestimmtes Werkzeug befüllt werden
darf, muss die Kanzlei entscheiden und dokumentieren. Jeder Prompt enthält dazu
einen eigenen Hinweis.

**Einzelheiten, die drei Datenzonen, die Freigabestufen und die Checkliste vor
dem ersten Einsatz: [DATENSCHUTZ.md](DATENSCHUTZ.md).**

## Zwei Grundregeln, die den Unterschied machen

**Zahlen prüfen, Struktur nutzen.** Die Stärke dieser Prompts liegt in der
Vollständigkeit der Prüfschritte, nicht in den Zahlen. Sprachmodelle geben
Kontonummern, Pauschbeträge und Freigrenzen plausibel, aber häufig falsch an.
Deshalb fordert jeder Prompt das Modell auf, solche Werte als
"für [JAHR] verifizieren" zu markieren – dieser Markierung folgen, immer.

**Vier Augen.** Kein Ergebnis geht ungeprüft an einen Mandanten oder in eine
Buchung. Der Abschnitt Qualitätssicherung sagt in jeder Datei konkret, worauf
zu achten ist.

## Eigene Prompts schreiben

Der [BAUKASTEN.md](BAUKASTEN.md) enthält die wiederverwendbaren Bausteine, aus
denen diese Sammlung gebaut ist: Rollen- und Arbeitsweisenformeln, den
Unsicherheitsbaustein, Ausgabeformate, das Freigabe-Bauteil und die Anti-Muster,
die in Kanzleiprompts regelmäßig schiefgehen.

## Beitragen

Fehler gefunden, Formulierung verbessert, neuen Anwendungsfall? Issue oder
Pull Request. Besonders wertvoll sind Rückmeldungen aus dem echten
Kanzleieinsatz: Was hat funktioniert, was musste umgeschrieben werden.

## Lizenz

Nutzung, Anpassung und Weitergabe innerhalb und außerhalb von Kanzleien
ausdrücklich erwünscht. Ohne Gewähr, ohne Haftung.

---

## Änderungsprotokoll

Änderungen werden hier chronologisch festgehalten, neueste zuerst – ein Eintrag
je abgeschlossener Runde.

### 2026-07-28 – Runde 12b: Lohn, Verfahrensrecht, KI-Compliance (95–104)

- Zehn neue Prompts: Lohn-Jahreswechsel, Aktivrente, Betriebsprüfung der
  Rentenversicherung, Phantomlohn-Screening, Statusfeststellung nach § 7a SGB IV,
  A1 und Tätigkeit im Ausland, Lohnpfändung, elektronische Bekanntgabe nach
  § 122a AO, Dienstleisterprüfung nach § 62a StBerG, KI-Richtlinie und
  KI-Kompetenz nach Art. 4 KI-VO.
- Adversarische Fachprüfung in zwei Domänen: 45 Mängel, alle behoben. Die
  schwersten: Die Soll-Regelung des § 122a Abs. 1 Satz 2 AO ist durch das
  Mindeststeueranpassungsgesetz auf 2027 verschoben worden – der Prompt hätte
  sonst auf einem Rechtsstand aufgesetzt, der noch nicht gilt; die Abgabenordnung
  kennt an dieser Stelle keinen „Widerspruch", sondern einen Antrag auf
  postalische Bekanntgabe; § 62a StBerG hat acht Absätze, die Prüfung endete bei
  fünf und ließ damit die Ausnahme für gesetzlich bereits verschwiegenheits-
  verpflichtete Dienstleister aus; ein Aktenzeichen des Bundessozialgerichts trug
  die ihm zugeschriebene Aussage nicht; bei Tätigkeit in mehreren Mitgliedstaaten
  ist der Träger des Wohnstaats zuständig, nicht eine deutsche Stelle; § 850f
  Abs. 2, § 845 und § 833 Abs. 2 ZPO fehlten in der Lohnpfändung.
- Vier Abbruchregeln feuerten erneut im eigenen Hauptanwendungsfall. Sie hängen
  jetzt an objektiven Angaben und steuern einzelne Vorgänge aus, statt die
  Bearbeitung zu beenden.
- `DATENSCHUTZ.md` nachgezogen: § 203 Abs. 3 Satz 2 StGB als Erlaubnistatbestand
  ergänzt, § 62a Abs. 8 StBerG als Fundstelle dafür, dass das Datenschutzrecht
  neben dem Berufsrecht steht, und eine Formulierung korrigiert, die eine
  zeitliche Vorgabe fälschlich dem § 62a Abs. 3 StBerG zuschrieb.
- Prompt 07 nachgezogen: Die Lohnpfändung ist dort aus dem Problemsatz genommen
  und verweist auf Prompt 101.
- Strukturprüfung über alle 88 Dateien: 0 Befunde.

### 2026-07-28 – Runde 12a: Umsatzsteuer, Immobilien, Nachfolge (85–94)

- Zehn neue Prompts: E-Rechnungs-Umstellungsradar, fehlerhafte E-Rechnung,
  § 14c UStG, Kleinunternehmer-Grenzen, Erhaltungsaufwand gegen anschaffungsnahe
  Herstellungskosten, privates Veräußerungsgeschäft § 23 EStG,
  Betriebsaufspaltungs-Monitoring, Sonderbetriebsvermögen bei der Übertragung,
  Grunderwerbsteuer bei Anteilsbewegungen, verdeckte Gewinnausschüttung.
- Vor dem Bau wurden die offenen Fundstellen an der Primärquelle gegengelesen.
  Dabei fiel auf: Das BMF-Schreiben vom 26.01.2026 enthält weder eine
  Vereinfachungsregelung mit Betragsgrenze je Baumaßnahme noch eine angeordnete
  Prüfungsreihenfolge, und vier der fünf für die sachliche Verflechtung bei der
  Betriebsaufspaltung genannten BFH-Entscheidungen betreffen tatsächlich die
  personelle Verflechtung oder ein anderes Thema. Diese Angaben stehen deshalb
  in keinem Prompt.
- Adversarische Fachprüfung in zwei Domänen: 39 Mängel, alle behoben. Die
  schwersten: ein Prüfschritt, der EU-ansässige Kleinunternehmer entgegen § 19
  Abs. 4 UStG von der Prüfung ausschloss; ein Hinweis, der den Anlagenverkauf in
  den Gesamtumsatz einbezog, obwohl § 19 Abs. 2 UStG ihn ausnimmt; die falsche
  Zuordnung von Satz 1 und Satz 2 des § 6 Abs. 3 EStG; die falschen Nummern des
  § 13 GrEStG und damit der falsche Anzeigepflichtige; die Abschaltung des
  § 6 Abs. 1 Nr. 1a EStG beim unentgeltlichen Erwerb; eine fehlende Grenze der
  Befugnis gegenüber Vertragsgestaltung und Beurkundung.
- Drei Abbruchregeln feuerten in ihrem eigenen Hauptanwendungsfall und mussten
  auf den einzelnen Vorgang statt auf den Gesamtfall umgestellt werden – dieselbe
  Fehlerart wie in Runde 10.
- Prompt 52 nachgezogen: Er verweist jetzt für Erwerbe im maßgeblichen Zeitraum
  auf Prompt 89, und umgekehrt.
- Strukturprüfung über alle 78 Dateien: 0 Befunde.

### 2026-07-28 – Recherche: 20 neue Prompt-Kandidaten

- Vier unabhängige Recherchen (Umsatzsteuer und E-Rechnung; Lohn und
  Sozialversicherung; Ertragsteuer, Immobilien und Nachfolge; Kanzleiführung,
  Berufsrecht und KI) mit rund 55 Suchen und 60 Quellenabrufen. Ergebnis: 56
  belegte Kandidaten.
- Daraus 20 ausgewählt und als Runde 12 (85–104) in den Backlog aufgenommen,
  12 als Reserve dokumentiert, der Rest mit Begründung verworfen.
- Ausschlussregeln, die am meisten aussortiert haben: bereits abgedeckt durch
  den Bestand oder die Runde 11; Kern ist eine Berechnung, ein Systemzugriff
  oder eine Wertetabelle; Entscheidungsgrundlagen liegen in der Kanzlei nicht
  vor; Rechtslage nicht gefestigt.
- Neue Recherchedatei `recherche/2026-07-28-kandidaten.md` mit Problem,
  zwingenden Normen, Haftungsrisiko und offenen Fundstellen je Kandidat – sowie
  einer Liste der Punkte, die vor dem Bau am Primärtext zu belegen sind.
- Noch kein Prompt erstellt: Diese Runde war die Suche.

### 2026-07-28 – Verzeichnisstruktur nach Kategorien

- Die Prompts liegen jetzt in zwölf Kategorieordnern unter `prompts/`
  (`01-finanzbuchhaltung` bis `12-krise-liquiditaet-bank`) statt flach in einem
  Verzeichnis. Die Ordner sind durchnummeriert, damit die Reihenfolge auf GitHub
  der des Index entspricht.
- Jeder Kategorieordner enthält eine `README.md` mit den Prompts der Kategorie –
  GitHub zeigt sie beim Öffnen des Ordners an.
- Alle 68 Links in `INDEX.md` auf die neuen Pfade umgestellt und maschinell
  geprüft, dass jedes Ziel existiert.
- Die Strukturprüfung durchsucht `prompts/` jetzt rekursiv und überspringt die
  Ordner-READMEs: 68 Dateien geprüft, 0 Befunde.
- **Hinweis für alle, die das Repository schon geklont oder verlinkt haben:
  Die Dateipfade haben sich geändert, die Dateinamen nicht.**

### 2026-07-28 – Kategorien im Index

- `INDEX.md` um eine Gliederung **nach Kategorie** erweitert, vorangestellt vor
  den bisherigen Gliederungen nach Rolle und nach Anlass. Zwölf Kategorien:
  Finanzbuchhaltung, Umsatzsteuer, Jahresabschluss und Bilanzierung, Lohn und
  Gehalt, Steuererklärung und Einzelsteuerfälle, Finanzamt/Fristen/Rechtsbehelf,
  GoBD/Kasse/Verfahrensdokumentation, Mandantenkommunikation, Honorar und
  Forderungen, Kanzleiorganisation und Team, Mandatsbeginn und Mandatswechsel,
  Krise/Liquidität/Bank.
- Jeder der 68 Prompts steht in genau einer Kategorie – anders als bei Rolle und
  Anlass, wo Mehrfachnennungen gewollt sind. Die Vollständigkeit und
  Überschneidungsfreiheit der Zuordnung wird beim Erzeugen maschinell geprüft.
- Urheberzeile am Ende dieser Datei ergänzt.

### 2026-07-27 – Runde 10: Mandantenthemen, Krise, Neumandat (60–69)

Zehn neue Prompts. Damit umfasst die Sammlung 68 Prompts.

- **Mandantenthemen 2026:** Photovoltaik (Steuerbefreiung, Entnahme von
  Bestandsanlagen, Nullsteuersatz) · Kryptowerte (Nachweise anfordern und einen
  Steuerreport prüfen) · verbilligte Vermietung · Elektro-Dienstwagen ·
  Minijob und Übergangsbereich.
- **Krise und Beratung:** Krisenindikatoren erkennen und ein Hinweisschreiben
  entwerfen (ausschließlich Berufsträger) · rollierende 13-Wochen-Liquiditäts-
  planung · Bankgespräch und Rating.
- **Neumandat:** Fragebogen zur steuerlichen Erfassung mit seinen bindenden
  Weichenstellungen · Mandatswechsel und Datenübernahme vom Vorberater.

**Qualitätssicherung.** Eine adversarische Fachprüfung fand 21 Mängel, davon
8 schwer; alle behoben. Die wichtigsten:

- Die Abbruchregel des Krisen-Prompts blockierte ihren eigenen Normalfall: Sie
  löste bei jedem Sozialversicherungsrückstand aus, den das Indikatorenraster
  zugleich abfragt – und ihr Tatbestand verlangte genau die insolvenzrechtliche
  Beurteilung, die der Prompt verbietet. Jetzt an objektiven Angaben verankert.
- Der Mandatswechsel-Prompt verlangte ein Anschreiben an den Vorberater, ohne
  dessen Entbindung von der Verschwiegenheit – das Schreiben wäre zu Recht
  zurückgewiesen worden, während laufende Fristen ablaufen.
- Die Liquiditätsplanung ermittelt den Punkt der ersten Unterdeckung und hatte
  dafür keine Weiterleitungsregel; sie bricht jetzt ab und verweist auf den
  Krisen-Prompt, dessen Rolle ausschließlich der Berufsträger ist.
- Der Vergleich von Kalt- und Warmmiete bei der verbilligten Vermietung war im
  Eingabeteil angelegt: Für die ortsübliche Seite fehlte das Feld für die
  umlagefähigen Kosten.
- Zwei Prompts versprachen in der Rollenbeschreibung eine Prüfung, die im
  Schema fehlte (Lohnsteuer beim Minijob, Sozialversicherung beim Dienstwagen).
- Photovoltaik: Kleinunternehmerregelung und Vorsteuerabzug standen unverbunden
  nebeneinander; die umsatzsteuerliche Entnahme der Altanlage und die
  gewerbesteuerliche Befreiung mit ihrer eigenen Grenze fehlten.
- Der Satz "bei Zweifeln ist die vorsichtigere Bewertung der sichere Weg" ist
  beim Dienstwagen keine sichere Anleitung, sondern führt zu einem zu hohen
  Sachbezug – ersetzt durch die Anrufungsauskunft.

### 2026-07-27 – Runde 9: Jahresabschluss und selten geübte Steuerarten (50–59)

Zehn neue Prompts, Grundlage ist eine Lückenanalyse gegen die vorhandenen 48
Prompts mit 30 belegten Kandidaten.

- **Jahresabschluss:** Rückstellungs-Prüfschema mit getrennter handelsrechtlicher
  und steuerlicher Beurteilung · Cut-off- und Nachlaufcheck zum Stichtag ·
  Anlagevermögen und AfA-Wahlrechte · Investitionsabzugsbetrag überwachen ·
  E-Bilanz-Kontennachweise vorbereiten · Anhang kleine Kapitalgesellschaft ·
  Offenlegung und Ordnungsgeldabwehr.
- **Selten geübte Steuerarten:** Bauabzugsteuer · Zusammenfassende Meldung und
  innergemeinschaftliche Lieferung · Kapitalertragsteuer bei Ausschüttung.

**Qualitätssicherung.** Eine adversarische Fachprüfung fand 28 Mängel, davon
7 schwer; alle behoben. Die wichtigsten:

- Der Bauleistungsbegriff des § 48 EStG ist **nicht** identisch mit dem des
  § 13b UStG. Gerüstbau ist bei der Bauabzugsteuer Bauleistung, bei der
  Umsatzsteuer nicht – die Verwechslung hätte zum Unterlassen des Einbehalts und
  damit zur Haftung geführt.
- Steuerliche Ansatzverbote bei Rückstellungen werden jetzt einzeln eingefordert,
  damit kein handelsrechtlicher Ansatz unbesehen in die Steuerspalte wandert.
- Kleinstkapitalgesellschaften brauchen unter Voraussetzungen keinen Anhang – der
  Prompt bricht dort jetzt ab, statt einen Anhang zu erzeugen, der mehr offenlegt
  als geschuldet.
- Rechnungsabgrenzungsposten setzen "eine bestimmte Zeit" voraus; ohne dieses
  Merkmal wurde jede Vorauszahlung zum Abgrenzungsposten.
- Teilwertabschreibung wird nicht mehr für Mandanten mit
  Einnahmenüberschussrechnung geprüft.
- Veraltete Fundstellen korrigiert: § 328a HGB existiert nicht; die
  Umsatzsteuer-Durchführungsverordnung wurde zum 1.1.2020 umnummeriert, die
  Gelangensbestätigung ist § 17b, der Buchnachweis § 17d.
- Ein Ampelstatus verlangte implizit die Fristberechnung, die derselbe Prompt
  verbietet – ersetzt durch einen Status, der sich allein aus der Datenlage ergibt.
- Teilmaskierte Steuernummern aus zwei Dateien entfernt; sie sind nach dem
  Datenschutzleitfaden auch in Ausschnitten unzulässig.

**Querschnitt:** Der Marker für prüfbedürftige Werte war in 15 älteren Dateien
über Zeilenumbrüche getrennt und damit maschinell nicht auffindbar – 18 Stellen
zusammengezogen, und die Strukturprüfung erkennt diesen Fehler ab jetzt selbst.

### 2026-07-27 – Veröffentlichungsrhythmus umgestellt

Ab sofort wird nach jeder abgeschlossenen Runde veröffentlicht statt am Ende
eines Arbeitslaufs. Jede Runde erhält damit einen eigenen Eintrag in diesem
Protokoll und einen eigenen Commit – die Historie wird nachvollziehbar, und
Arbeit ist gesichert, sobald sie geprüft ist.

### 2026-07-27 – Läufe 2 bis 8: von 10 auf 48 Prompts

**Neu: 38 Prompts (11–49, ohne 45).**

- Kommunikation und Mandantenführung (11–17): Fachtext übersetzen,
  E-Rechnungs-Rundschreiben, Mandantenmail verdichten, Leistungsnachweis zur
  Honorarrechnung, Honorarbeschwerde und -anpassung, Mahnstufen, Zulieferkalender.
- Analyse exportierter Daten (18–22): Offene Posten, Dubletten, Summen- und
  Saldenliste, EÜR-Plausibilität, Kontenrahmen-Vergleich.
- Kanzleiorganisation und Qualitätssicherung (23–30): Arbeitsanweisung,
  Vertretungsleitfaden, Stammdatenkonvention, Belegkanäle, Scan-Anleitung,
  OCR-Prüfroutine, Onboarding, Übungsfälle.
- Fristen, Bescheide, Prüfung (31–36): Fristverlängerung, Bescheidabgleich,
  Einspruchsbegründung, Betriebsprüfung, Fristenkonzept, Sachverhaltsdarstellung.
- GoBD, Kasse, Dokumentation (37–40): Verfahrensdokumentation, GoBD-Kasse,
  Kontierungsrichtlinie, Sachbezüge.
- Lohn vertieft (41–44): SV-Fehlerprotokoll, Behördenanschreiben, FAQ Lohn,
  Stichtagsplan.
- Kanzleiführung (46–49): Mandatsprofitabilität, Erreichbarkeitskonzept,
  Change-Kommunikation, Mandantenkontakt.

**Neu: drei Querschnittsdateien.**

- [DATENSCHUTZ.md](DATENSCHUTZ.md) – Datenschutz- und Freigabe-Leitfaden mit
  drei Datenzonen, vier Freigabestufen, Werkzeugauswahl nach § 62a StBerG,
  KI-Kompetenz nach Art. 4 KI-VO und Checkliste vor dem ersten Einsatz.
- [BAUKASTEN.md](BAUKASTEN.md) – 15 wiederverwendbare Prompt-Bausteine und die
  Anti-Muster, die in Kanzleiprompts schiefgehen.
- [INDEX.md](INDEX.md) – Übersicht nach Rolle, Anlass und Prompt-Ketten.

**Qualitätssicherung.** Vier unabhängige adversarische Fachprüfungen fanden
**86 Mängel**, davon 15 schwer; alle behoben. Die wichtigsten Korrekturen:

- § 62a StBerG (Einbindung von Dienstleistern) und Art. 4 KI-VO (KI-Kompetenz)
  fehlten in allen Dateien und sind jetzt durchgehend berücksichtigt.
- Bei versäumter Erklärungsfrist ist die rückwirkende Fristverlängerung nach
  § 109 Abs. 1 Satz 2 AO das Mittel, nicht die Wiedereinsetzung.
- Bekanntgabefiktion auf vier Tage aktualisiert (seit 1.1.2025);
  § 200a AO (qualifiziertes Mitwirkungsverlangen) ergänzt; § 147 Abs. 6 AO
  in der Fassung ab 1.1.2025.
- Gestufte Ausgangskontrolle mit Sendenachweis im Fristenkonzept ergänzt.
- Sachbezugs-Merkblatt: Vorteile mit eigener Bewertungsregel gehören nicht in
  die monatliche Freigrenze.
- Offene-Posten-Analyse: Zweifelhaftigkeit und Uneinbringlichkeit nach
  § 17 UStG getrennt; Wertberichtigung bei EÜR ausgeschlossen.
- E-Rechnung in Belegkanal-, Scan- und Kontierungsprompts berücksichtigt –
  aufbewahrungspflichtig ist der strukturierte Datensatz, nicht der Ausdruck.
- GoBD-Fundstelle auf die zweite Änderung vom 14.7.2025 aktualisiert.
- Keine Beschäftigtenbeurteilungen, keine Gesundheitsdaten über Mitarbeitende.
- Markertext für prüfbedürftige Werte auf eine kanonische Form vereinheitlicht
  und Rechtsgrundlagen werden jetzt positiv eingefordert, nicht nur ihre
  Erfindung verboten.

Strukturprüfung über alle 48 Dateien: 0 Befunde.

### 2026-07-27 – Veröffentlichung auf GitHub

- Projekt auf zwei Repositorys aufgeteilt: ein privates Entwicklungs-Repository
  mit Charter, Backlog, Recherche und Projektdokumentation, und dieses
  öffentliche Repository mit den Prompts und dieser Beschreibung.
- `README.md` neu geschrieben: von einer internen Konventionsdatei zu einer
  Beschreibung für Anwender – für wen, wofür, wofür ausdrücklich nicht,
  Anwendung, Datenschutz und Berufsrecht.
- Die bisherigen Konventionen für Prompt-Dateien sind in die Projekt-
  dokumentation des privaten Repositorys gewandert.

### 2026-07-27 – Lauf 1: Erstveröffentlichung

- Recherchebasis aufgebaut: 60+ Alltagsprobleme aus DATEV-Community, Circula-Blog,
  IWW, DATEV-Magazin, DStV, Haufe und Kanzleiblogs; gefiltert auf die Fälle, bei
  denen KI ohne DATEV-Systemzugriff tatsächlich hilft.
- Die ersten zehn Prompts erstellt (01–10): Belegnachforderung, Bankumsatz-Rückfragen,
  Buchungssatz SKR03/04, Umsatzsteuer-Sonderfälle, UStVA-Abweichung, BWA-Kommentar,
  Lohn-Sonderfälle, Lohnabrechnung erklären, ESt-Unterlagencheckliste,
  Reisekosten- und Bewirtungsprüfung.
- Zwei Prüfdurchgänge: Strukturprüfung bestanden; adversarische Fachprüfung
  fand 24 Mängel, alle behoben. Unter anderem: zirkuläres Umsatzsteuer-Prüfschema
  neu geordnet, falscher Rechnungsadressat beim Bewirtungsbeleg korrigiert,
  Fahrtkostenzuschuss und bAV in der Lohnabrechnung richtig einsortiert,
  abgekündigtes DATEV-Produkt ersetzt, Datensparsamkeitshinweis in allen Dateien ergänzt.
- Backlog mit 52 Punkten angelegt.

---

Erstellt von Thomas Lauer (Thomas@Lauer.io) – mehr unter https://www.Lauer.io
