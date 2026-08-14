# 115 – EDI-Strecke prüfen: Übergangsfrist, Extraktion und Interoperabilität

**Problem:** Der Mandant rechnet seit Jahren über EDI ab, die Übergangsregelung für EDI läuft aus, und niemand hat geprüft, ob sich die nach dem Umsatzsteuergesetz erforderlichen Angaben aus dem eingesetzten Format richtig und vollständig extrahieren lassen.
**Rolle:** Steuerberater, Sachbearbeiter Umsatzsteuer, Ansprechpartner für die IT des Mandanten
**DATEV-Bezug:** DATEV SmartTransfer (Formatumwandlung und Rechnungsversand), DATEV Auftragswesen next (Rechnungsausgang), DATEV Unternehmen online (Belegweg), DATEV DMS (Ablage von EDI-Vereinbarung, Zustimmungsnachweis und Prüfprotokoll); Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Bezeichnung der Strecke und Geschäftspartner als Kürzel; den von der Kanzlei bestimmten Ort der abgerechneten Umsätze; Anzahl der Belege im Jahr; eingesetztes Format mit Versionsstand und Nachrichtentyp; EDI-Dienstleister; bestehende EDI-Vereinbarung mit Datum; Nachweis der Zustimmung des Empfängers; Ausführungszeitpunkte der über die Strecke abgerechneten Umsätze; Angabe, ob der Gesamtumsatz des Vorjahres über oder unter 800.000 € liegt; Ergebnis eines etwaigen Extraktionstests; Archivierung des strukturierten Datensatzes.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname und Firmierung der EDI-Partner durch Platzhalter ersetzen (`Mandant A`, `Partner 1`, `Partner 2`) und konsistent durchhalten. Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer, IBAN und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen und nur als im Datensatz vorhanden oder fehlend kennzeichnen (Zone Rot in `DATENSCHUTZ.md`). Es werden keine Echtnachrichten und keine Mappings mit Echtdaten eingefügt, sondern nur Feld- und Segmentbezeichnungen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug für ein konkretes Mandat und nicht nur als allgemeine Kanzlei-IT eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und prüfst eine
bestehende EDI-Abrechnungsstrecke auf ihre umsatzsteuerliche Tragfähigkeit.
Du unterscheidest strikt zwischen der befristeten Übergangsregelung und dem
dauerhaften Weg und behauptest keine Anforderung, die du nicht an einer Norm
oder an einer Verwaltungsanweisung festmachen kannst.

WAS DU NICHT TUST
Du liest keine Nachricht und validierst keinen Datensatz. Dir liegen nur
Format- und Segmentbezeichnungen sowie die Angaben zur Strecke vor. Alles,
was du über den Inhalt des Formats sagst, ist eine Ableitung aus diesen
Angaben – kennzeichne sie als solche. Du berechnest keine Fristen und keine
Umsatzgrenzen und vergleichst keinen Betrag mit der Grenze von 800.000 €;
diese Einordnung liefert der Sachverhaltsbogen.

AUSSTEUERUNGSREGEL – kein Abbruch, an einer objektiven Angabe.
Steht im Feld "Rechnungen für Umsätze mit Ausführungszeitpunkt nach dem
31.12.2027 bereits über diese Strecke ausgestellt" ein "ja", steuere die
Beurteilung dieser bereits abgerechneten Umsätze aus. Gib dafür nur aus:
"Ausgesteuert – Prüfung durch einen Berufsträger außerhalb des KI-Werkzeugs."
Beende die Bearbeitung NICHT; arbeite alle übrigen Schritte weiter ab, führe
den ausgesteuerten Punkt gesondert auf und prüfe die Strecke im Übrigen
vollständig.

AUFGABE
Erzeuge die Prüfung der EDI-Strecke, eine Fragenliste an den EDI-Dienstleister
und einen Maßnahmenplan mit Verantwortlichen.

EDI-STRECKE
- Bezeichnung der Strecke: [KENNUNG]
- Geschäftspartner (Kürzel, konsistent): [PARTNER 1], [PARTNER 2]
- Anzahl Belege im Jahr je Partner: [ANZAHL]
- Eingesetztes Format, Nachrichtentyp und Version: [ANGABE]
- EDI-Dienstleister oder Konverter: [extern / im eigenen Haus],
  Bezeichnung: [ANGABE]
- Bestehende EDI-Vereinbarung: [keine / ja], Datum: [DATUM]
- Zustimmung des Empfängers dokumentiert: [nein / ja], Form: [ANGABE]
- Ausführungszeitpunkte der über die Strecke abgerechneten Umsätze:
  [ZEITRAUM]
- Rechnungen für Umsätze mit Ausführungszeitpunkt nach dem 31.12.2027
  bereits über diese Strecke ausgestellt: [nein / ja]
- Gesamtumsatz des Vorjahres: [nicht mehr als 800.000 € / mehr als
  800.000 € / nicht ermittelt]
- Ort der über die Strecke abgerechneten Umsätze, von der Kanzlei bestimmt:
  [Inland / überwiegend Inland, Ausnahmen angeben / nicht im Inland /
  nicht bestimmt]
- Ansässigkeit von Leistendem und Leistungsempfänger: [beide im Inland /
  abweichend, bitte angeben]
- Extraktion der Rechnungsangaben je getestet: [nein / ja], Ergebnis:
  [ANGABE]
- Im Format vorhandene Segmente und Felder (Bezeichnungen, keine Inhalte):
  [FELDLISTE]
- Strukturierter Datensatz wird archiviert: [nein / ja], System: [ANGABE]

NORMENRAHMEN, MIT DEM DU ARBEITEST
Prüfe jeden Wortlaut am amtlichen Gesetzes- bzw. Erlasstext nach; für jede der
folgenden Angaben gilt der Zusatz: Fundstelle – für [JAHR] verifizieren.
- § 14 Abs. 2 Satz 1 UStG setzt für die Rechnungspflicht eine im Inland
  ausgeführte Lieferung oder sonstige Leistung voraus; § 1 Abs. 1 Nr. 1 UStG
  für die Steuerbarkeit, § 3 und § 3a UStG für den Ort.
- § 14 Abs. 2 Satz 2 Nr. 1 Halbsatz 2 UStG (Pflicht zur E-Rechnung) und
  Satz 3 (Inlandsansässigkeit) für die Frage, ob überhaupt eine Pflicht
  besteht.
- § 14 Abs. 1 Satz 6 UStG bestimmt das Format: Nr. 1 Entsprechung mit der
  europäischen Norm für die elektronische Rechnungsstellung und der
  Syntaxliste gemäß der Richtlinie 2014/55/EU; Nr. 2 ein zwischen
  Rechnungsaussteller und Rechnungsempfänger vereinbartes Format, wenn die
  richtige und vollständige Extraktion der nach diesem Gesetz erforderlichen
  Angaben in ein Format möglich ist, das der Norm entspricht oder mit dieser
  interoperabel ist. Nummer 2 ist der DAUERHAFTE Weg für EDI nach Ablauf der
  Übergangsregelung – arbeite diesen Punkt in jedem Fall aus.
- § 27 Abs. 38 Satz 1 UStG, drei Nummern, die sauber auseinanderzuhalten
  sind:
  Nr. 1 – bis 31.12.2026 darf für einen nach dem 31.12.2024 und vor dem
  01.01.2027 ausgeführten Umsatz eine Rechnung auf Papier oder, mit
  Zustimmung des Empfängers, in einem nicht normkonformen elektronischen
  Format ÜBERMITTELT werden.
  Nr. 2 – bis 31.12.2027 für einen nach dem 31.12.2026 und vor dem
  01.01.2028 ausgeführten Umsatz, wenn der Gesamtumsatz (§ 19 Abs. 2 UStG)
  des ausstellenden Unternehmers im vorangegangenen Kalenderjahr nicht mehr
  als 800.000 € betragen hat.
  Nr. 3 – bis 31.12.2027 für einen nach dem 31.12.2026 und vor dem
  01.01.2028 ausgeführten Umsatz darf die Rechnung mit Zustimmung des
  Empfängers in einem nicht normkonformen elektronischen Format AUSGESTELLT
  werden, wenn sie mittels elektronischem Datenaustausch (EDI) nach Artikel 2
  der Empfehlung 94/820/EG der Kommission vom 19.10.1994 übermittelt wird.
  Nr. 3 gilt OHNE Umsatzgrenze. Die Grenze von 800.000 € steht in Nr. 2 und
  hat mit EDI nichts zu tun. Nr. 1 spricht vom Übermitteln, Nr. 3 vom
  Ausstellen. Für Umsätze der Jahre 2025 und 2026 folgt die Zulässigkeit des
  EDI-Verfahrens bereits aus Nr. 1.
- § 14 Abs. 4 UStG ist der Katalog der Angaben, die aus dem Format
  extrahierbar sein müssen.
- OFFENZULEGEN: Die Bezeichnung "EN 16931" steht NICHT im Umsatzsteuer-
  gesetz. Das Gesetz verweist nur auf die Richtlinie 2014/55/EU. Die
  ausdrückliche Bezugnahme auf die Normenreihe findet sich erst in UStAE
  Abschnitt 14.1 Abs. 11 Satz 1 Nr. 1 und Abs. 12 ff. Eine Rechtsverordnung
  nach § 14 Abs. 6 Satz 2 UStG existiert nicht. Sage das ausdrücklich und
  täusche kein Gesetzeszitat vor.
- § 14b Abs. 1 UStG für die Aufbewahrung der Rechnungen und der Doppel der
  selbst ausgestellten Rechnungen (Satz 2: die Rechnungen müssen für den
  gesamten Zeitraum die Anforderungen des § 14 Abs. 3 Satz 1 UStG erfüllen;
  Satz 3: Fristbeginn mit dem Schluss des Kalenderjahres der Ausstellung,
  § 147 Abs. 3 AO bleibt unberührt) sowie § 147 Abs. 1 und 3 AO. Nenne keine
  Dauer, die du nicht im amtlichen Volltext gelesen hast.
- BMF-Schreiben vom 15.10.2024, BStBl I 2024, 1320, geändert und ergänzt
  durch BMF-Schreiben vom 15.10.2025, GZ III C 2 - S 7287-a/00019/007/243.
  Das Schreiben von 2024 ist nicht aufgehoben und gilt in der geänderten
  Fassung fort. Nenne für das Schreiben von 2025 KEINE Fundstelle im
  Bundessteuerblatt.

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. PFLICHT UND ZUORDNUNG. Kläre zuerst anhand des Feldes "Ort der über die
   Strecke abgerechneten Umsätze", ob die Umsätze im Inland ausgeführt werden
   (§ 14 Abs. 2 Satz 1, § 1 Abs. 1 Nr. 1 UStG); übernimm die Angabe und
   bestimme den Ort nicht selbst. Steht dort "nicht bestimmt", behandle die
   Pflichtfrage als offen; liegt der Ort nicht im Inland, sage das
   ausdrücklich und weise darauf hin, dass sich die Rechnungserteilung dann
   nicht nach § 14 Abs. 2 Satz 2 UStG richtet. Kläre danach anhand der
   Ansässigkeit von Leistendem und Leistungsempfänger, ob für die über diese
   Strecke abgerechneten Umsätze überhaupt eine Pflicht zur E-Rechnung
   besteht (§ 14 Abs. 2 Satz 2 Nr. 1 Halbsatz 2 und Satz 3 UStG). Ordne
   danach jedem angegebenen Ausführungszeitraum die anwendbare Nummer des
   § 27 Abs. 38 Satz 1 UStG zu.
   Berechne dabei nichts und leite keine Fristen ab; ordne nur zu. Sage zu
   jedem Zeitraum, welche Voraussetzung die jeweilige Nummer verlangt
   (Zustimmung, Umsatzgrenze, Übermittlungsweg) und ob sie nach dem
   Sachverhaltsbogen erfüllt ist. Steht dort "nicht ermittelt", behandle die
   Zuordnung als offen. Für Umsätze, die nach dem 31.12.2027 ausgeführt
   werden, greift KEINE der drei Nummern mehr; schreibe in die Zeitachse
   "keine Übergangsregelung – § 14 Abs. 1 Satz 6 UStG maßgeblich" und
   verweise auf Schritt 2.
2. DAUERHAFTER WEG. Prüfe, ob die Strecke über § 14 Abs. 1 Satz 6 Nr. 2 UStG
   dauerhaft gangbar ist: Liegt ein zwischen Aussteller und Empfänger
   vereinbartes Format vor, und ist die richtige und vollständige Extraktion
   der erforderlichen Angaben in ein normkonformes oder mit der Norm
   interoperables Format möglich? Benenne, wer diesen Nachweis führt und
   woraus er besteht.
3. EXTRAKTIONSPRÜFUNG. Gehe den Katalog des § 14 Abs. 4 UStG durch und ordne
   jeder Angabe zu, ob sie nach der Feldliste im Format vorhanden und ob sie
   extrahierbar ist. Ist eine Angabe nicht belegt, schreibe "nicht belegt"
   und keine Vermutung ins Ergebnis. Steht im Feld "Extraktion je getestet"
   ein "nein", weise das als zentrale offene Maßnahme aus.
4. ZUSTIMMUNG UND VEREINBARUNG. Ist die Zustimmung des Empfängers
   dokumentiert, in welcher Form, und deckt die bestehende EDI-Vereinbarung
   sie ab? Ordne die Anforderung der einschlägigen Nummer des § 27 Abs. 38
   Satz 1 UStG zu.
5. ARCHIVIERUNG. Wird der strukturierte Datensatz selbst aufbewahrt oder nur
   eine Bilddatei? Benenne die Aufbewahrungspflicht mit den Fundstellen aus
   dem Normenrahmen (§ 14b Abs. 1 UStG, § 147 Abs. 1 und 3 AO) und nenne
   keine Dauer ohne Beleg; bist du unsicher, schreibe "Fundstelle offen –
   bitte recherchieren".

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben, statt sie zu erfinden.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV, also Norm
   mit Absatz, Satz und Nummer oder Erlass mit Fundstelle, jeweils mit dem
   Zusatz "für [JAHR] verifizieren", und führe sie am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" auf. Bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Berechne KEINE Fristen und keine Restlaufzeiten. Nenne die Stichtage nur
   so, wie sie im Gesetzeswortlaut stehen, je mit dem Zusatz
   "für [JAHR] verifizieren", und ergänze: "Fristen berechnet und erfasst
   ein Mensch."
4. Formuliere jede Aussage über den Inhalt des Formats als Vermutung,
   solange sie nicht aus der Feldliste oder aus einem Testergebnis folgt.
5. Höchstens ZWÖLF Fragen an den Dienstleister und höchstens ZEHN Maßnahmen.
   Sortiere die Maßnahmen nach der Zahl der betroffenen Belege je Partner,
   die im Sachverhaltsbogen steht. Lasse weg, was auf diese Strecke nicht
   passt.

AUSGABEFORMAT
1. (Einordnung) – Eindeutigkeit, Datenlage, fehlende Angaben.
2. (Zeitachse) – Tabelle ohne Datumsberechnung:
   Ausführungszeitraum | anwendbare Nummer des § 27 Abs. 38 Satz 1 UStG oder
   "keine" | Voraussetzung dieser Nummer | im Sachverhalt erfüllt
   (ja/nein/offen)
3. (Dauerhafter Weg) – Beurteilung nach § 14 Abs. 1 Satz 6 Nr. 2 UStG mit
   Begründung, ausdrücklich getrennt von der Übergangsregelung.
4. (Extraktionsprüfung) – Tabelle:
   Angabe nach § 14 Abs. 4 UStG | im Format vorhanden | extrahierbar | Beleg
5. (Archivierung) – was aufbewahrt wird (strukturierter Datensatz oder
   Bilddatei), in welchem System, mit welcher Rechtsgrundlage, welche Punkte
   offen sind.
6. (Fragen an den EDI-Dienstleister) – nummeriert, jede Frage so gestellt,
   dass sie mit ja, nein oder einer Fundstelle beantwortbar ist.
7. (Maßnahmen) – Tabelle:
   Nr. | Maßnahme | Verantwortlicher (Kanzlei / Mandant / Dienstleister) |
   Voraussetzung | erledigt (leer)
8. (Offene Punkte) – darunter ausdrücklich der Hinweis, dass "EN 16931" nicht
   im Gesetz steht, sondern erst in UStAE Abschnitt 14.1 Abs. 11 Satz 1 Nr. 1
   und Abs. 12 ff., dass eine Rechtsverordnung nach § 14 Abs. 6 Satz 2 UStG
   nicht existiert, sowie alle ausgesteuerten Punkte.
9. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
10. (Interne Notiz) – was die Kanzlei mit dem Mandanten vor dem Gespräch mit
   dem Dienstleister klären muss.
```

## Anwendung

1. **Vorschaltfrage durch den Berufsträger, vor dem Werkzeugeinsatz und außerhalb des Werkzeugs:** Gibt es Anhaltspunkte für eine Berichtigungspflicht nach § 153 AO, eine Selbstanzeige oder ein Steuerstrafverfahren? Wenn ja, wird dieser Prompt nicht eingesetzt; die Antwort wird in der Handakte vermerkt (Zone Rot in `DATENSCHUTZ.md`).
2. Je Strecke ein Lauf, nicht je Mandant. Zwei Partner mit unterschiedlichen Formaten sind zwei Strecken und zwei Prüfungen.
3. Die Feldliste beim Dienstleister anfordern, bevor der Prompt läuft. Ohne sie liefert die Extraktionsprüfung nur Fragen und keine Aussagen – das ist ein zulässiges Zwischenergebnis, aber kein Prüfergebnis.
4. Die Angabe zum Gesamtumsatz des Vorjahres wird in der Kanzlei aus der Umsatzsteuer-Auswertung hergeleitet und als Einordnung eingetragen; der Prompt vergleicht keinen Betrag mit der Grenze. Ebenso wird der Ort der über die Strecke abgerechneten Umsätze vor dem Lauf in der Kanzlei bestimmt und eingetragen – der Prompt übernimmt die Einordnung, er ermittelt sie nicht.
5. Fragenliste unverändert an den Dienstleister geben und die Antworten in der Maßnahmentabelle nachtragen. Antworten ohne Fundstelle gelten als unbeantwortet.
6. **Abgrenzung zu den Nachbarprompts:** Prompt 85 ist das Umstellungsradar über den Mandantenbestand, dieser Prompt die Einzelfallprüfung einer EDI-Strecke. Prompt 12 erzeugt das Mandantenrundschreiben.

## Qualitätssicherung

- **Die drei Nummern des § 27 Abs. 38 Satz 1 UStG werden getrennt gelesen.** Nr. 3 erfasst nur Umsätze, die nach dem 31.12.2026 und vor dem 01.01.2028 ausgeführt werden, gilt ohne Umsatzgrenze, verlangt die Zustimmung des Empfängers, betrifft das Ausstellen und verweist auf Artikel 2 der Empfehlung 94/820/EG der Kommission vom 19.10.1994. Für Umsätze der Jahre 2025 und 2026 folgt die Zulässigkeit bereits aus Nr. 1, die vom Übermitteln spricht. Die Grenze von 800.000 € steht in Nr. 2 und betrifft EDI nicht (für [JAHR] verifizieren).
- **Ohne Inlandsumsatz keine Pflicht nach § 14 Abs. 2 Satz 2 UStG.** Der Ort der über die Strecke abgerechneten Umsätze wird in der Kanzlei bestimmt und in den Sachverhaltsbogen eingetragen; die Ansässigkeit der Beteiligten beantwortet die Ortsfrage nicht (§ 14 Abs. 2 Satz 1, § 1 Abs. 1 Nr. 1, §§ 3 und 3a UStG – für [JAHR] verifizieren).
- **Nach dem 31.12.2027 trägt keine der drei Nummern mehr.** Für später ausgeführte Umsätze bleibt allein § 14 Abs. 1 Satz 6 UStG; eine Zeitachse, die auch für diese Zeiträume eine Nummer des § 27 Abs. 38 Satz 1 UStG ausweist, ist falsch (für [JAHR] verifizieren).
- **Die Übergangsregelung ist nicht der Dauerzustand.** Der dauerhafte Weg für ein vereinbartes EDI-Format ist § 14 Abs. 1 Satz 6 Nr. 2 UStG und hängt daran, dass die richtige und vollständige Extraktion der nach dem Gesetz erforderlichen Angaben in ein normkonformes oder interoperables Format möglich ist. Wer diesen Nachweis nicht führt, hat nach Ablauf der Übergangsregelung keine Grundlage mehr.
- **Kein vorgetäuschtes Gesetzeszitat.** "EN 16931" steht nicht im Umsatzsteuergesetz; das Gesetz verweist auf die Richtlinie 2014/55/EU. Die ausdrückliche Bezugnahme steht in UStAE Abschnitt 14.1 Abs. 11 Satz 1 Nr. 1 und Abs. 12 ff. Eine Rechtsverordnung nach § 14 Abs. 6 Satz 2 UStG existiert nicht (für [JAHR] verifizieren).
- **Extraktion ist eine Tatsachenfrage, keine Rechtsfrage.** Ob ein Feld vorhanden und extrahierbar ist, belegt ein Test oder eine schriftliche Auskunft des Dienstleisters – nicht die KI-Antwort. Jede Zeile der Extraktionstabelle ohne Beleg gilt als offen.
- **Aufbewahrung getrennt vom Format prüfen.** Aufzubewahren ist der strukturierte Datensatz selbst; Rechtsgrundlagen sind § 14b Abs. 1 UStG und § 147 Abs. 1 und 3 AO. Dauer und Fassung im amtlichen Volltext nachlesen und keine Jahreszahl aus der KI-Antwort übernehmen (für [JAHR] verifizieren).
- **Zustimmung des Empfängers dokumentieren.** Sie ist Tatbestandsmerkmal, nicht Formalie; die Ablage gehört in `DATENSCHUTZ.md`-konforme Systeme der Kanzlei oder des Mandanten und wird mit Datum geführt.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person prüft die Zuordnung der Ausführungszeiträume zu den Nummern des § 27 Abs. 38 Satz 1 UStG und die Beurteilung nach § 14 Abs. 1 Satz 6 Nr. 2 UStG nach. Jede Auskunft an den Mandanten, an den Dienstleister oder an den EDI-Partner gibt ein Berufsträger frei; die Freigabe wird dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch.** Kein Umstellungstermin und keine Restlaufzeit aus der KI-Antwort übernehmen.
- **Rechtsstand prüfen an:** § 1 Abs. 1 Nr. 1, §§ 3 und 3a, § 14, § 14b und § 27 Abs. 38 UStG sowie § 147 AO im amtlichen Volltext (gesetze-im-internet.de), UStAE Abschnitt 14.1, Richtlinie 2014/55/EU und Empfehlung 94/820/EG (EUR-Lex), BMF-Schreiben vom 15.10.2024 (BStBl I 2024, 1320) in der durch das BMF-Schreiben vom 15.10.2025 (GZ III C 2 - S 7287-a/00019/007/243) geänderten und ergänzten Fassung. Für das Schreiben von 2025 wird keine Fundstelle im Bundessteuerblatt zitiert.

## Varianten

- **Mehrere Strecken vergleichen:** „Fasse die Ergebnisse mehrerer Läufe zu einer Übersicht zusammen: Strecke, anwendbare Nummer je Zeitraum, Extraktionsnachweis vorhanden, nächste Maßnahme."
- **Nur Fragenliste:** „Bearbeite ausschließlich Schritt 2 und Schritt 3 und erzeuge daraus ein Anschreiben an den EDI-Dienstleister mit Rückantwortfrist, die die Kanzlei einträgt."
- **Empfängerseite:** „Prüfe die Strecke aus Sicht des Rechnungsempfängers und benenne, welche Nachweise er für den Vorsteuerabzug vorhalten sollte."
- **Vertragsanpassung:** „Leite aus dem Ergebnis eine Liste der Punkte ab, die in der EDI-Vereinbarung ergänzt werden sollten, ohne Vertragsformulierung."
