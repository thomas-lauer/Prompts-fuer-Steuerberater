# 14 – Leistungsnachweis als Anlage zur Honorarrechnung

**Problem:** Der Mandant sieht eine Summe und eine Paragrafenkette. Er versteht nicht, wofür er zahlt, fragt nach oder zahlt spät. Die Bundessteuerberaterkammer benennt das Kernproblem selbst: Die Leistung ist für den Mandanten nicht greifbar.
**Rolle:** Kanzleileitung, Sekretariat, Berufsträger
**DATEV-Bezug:** DATEV Eigenorganisation comfort (Leistungserfassung, Rechnungsschreibung)
**Was du bereitstellen musst:** Die abgerechneten Positionen mit Vorschrift, Gegenstandswert und Satz, dazu die tatsächlich erbrachten Tätigkeiten.
**Datensparsamkeit:** Mandantenname und Steuernummer erst beim Ausdruck aus der Kanzleisoftware einsetzen. Für den Entwurf genügen Leistungsart, Gegenstandswerte und Beträge. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du erstellst für eine deutsche Steuerkanzlei die erläuternde Anlage zu einer
Honorarrechnung nach der Steuerberatervergütungsverordnung. Ziel ist, dass der
Mandant nachvollziehen kann, wofür er zahlt – nicht, dass die Rechnung
gerechtfertigt wird.

AUFGABE
Erzeuge einen Leistungsnachweis als Anlage zur Rechnung.

ABGERECHNETE POSITIONEN
[JE POSITION: Tätigkeit | angewandte Vorschrift | Gegenstandswert |
 Zehntelsatz oder Zeitgebühr | Betrag]

TATSÄCHLICH ERBRACHTE TÄTIGKEITEN
[STICHWORTARTIG, so konkret wie möglich – z. B.
 - Prüfung und Kontierung 340 Belege
 - Abstimmung Verrechnungskonto mit dem Mandanten, zwei Telefonate
 - Anlagenspiegel erstellt, drei Zugänge, ein Abgang
 - Rückfrage Finanzamt zur Vorsteueraufteilung beantwortet
 - Jahresabschluss besprochen, 45 Minuten]

RAHMEN
- Leistungszeitraum: [ZEITRAUM]
- Auftrag: [z. B. Jahresabschluss 2025 und Steuererklärungen]
- Besonderheiten, die Mehraufwand verursacht haben: [ANGABE oder "keine"]
- Was im Vorjahr abgerechnet wurde: [BETRAG oder "unbekannt"]
- Gibt es eine Vergütungsvereinbarung: [ja, Inhalt … / nein, gesetzliche Gebühren]

ANFORDERUNGEN
1. Erzeuge eine Tabelle mit den Spalten:
   Tätigkeit | Was dahintersteckt | Rechtsgrundlage | Betrag
   Spalte "Was dahintersteckt": ein bis zwei Sätze in Alltagssprache, was in
   diesem Posten konkret an Arbeit steckt. Diese Spalte ist der eigentliche
   Zweck der Anlage.
2. Vermeide Sammelbezeichnungen wie "Jahresabschlussarbeiten", "Buchführung"
   oder "diverse Tätigkeiten". Beschreibe die Tätigkeit so konkret, wie es
   die Angaben zulassen. Wo die Angaben zu dünn sind, schreibe in die Spalte
   "Angaben ergänzen" statt einer erfundenen Beschreibung.
3. Bei Zeitgebühren: Tätigkeiten einzeln aufführen und den Zeitaufwand je
   Tätigkeit nennen. Fasse nur zusammen, was denselben Stundensatz hat.
   Runde die Zeitangaben auf den Abrechnungstakt der Kanzlei (Zeitgebühr nach
   § 13 StBVV, Takt für [JAHR] verifizieren), damit Anlage und Rechnung
   zusammenpassen.
4. Nenne bei Wertgebühren Gegenstandswert und Zehntelsatz. Der
   Gegenstandswert ist in der Berechnung selbst zwingend anzugeben
   (§ 9 Abs. 2 Nr. 6 StBVV – für [JAHR] verifizieren); in der Anlage
   wiederholt macht er sie für den Mandanten nachvollziehbar.
5. Schreibe ein Anschreiben von höchstens 100 Wörtern: welcher Zeitraum,
   welcher Auftrag, ein Satz zum Nutzen für den Mandanten, Angebot, Rückfragen
   zu besprechen.
6. Wenn der Betrag deutlich über dem Vorjahr liegt, ergänze einen Abschnitt
   "Warum die Rechnung höher ausfällt als im Vorjahr" mit den konkreten
   Gründen aus den Angaben. Erfinde keine Gründe. Wenn die Angaben keine
   Erklärung hergeben, sag das in der internen Notiz.
7. Erzeuge eine INTERNE NOTIZ mit:
   - Positionen, deren Beschreibung im Streitfall zu dünn wäre
   - Tätigkeiten aus der Liste, die keiner abgerechneten Position zugeordnet
     werden konnten (möglicherweise nicht abgerechnet)
   - Positionen, bei denen der Ermessensspielraum begründet werden sollte
8. Rechne nichts nach und ändere keine Beträge. Wenn eine Summe nicht
   aufgeht, weise darauf hin, statt zu korrigieren.
9. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage, jeweils mit dem
   Zusatz "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du
   unsicher, schreibe "Fundstelle offen – bitte recherchieren".

AUSGABEFORMAT
Anschreiben – Leistungsübersicht (Tabelle) – ggf. Warum höher als im Vorjahr –
Interne Notiz.
```

## Anwendung

1. Tätigkeitsliste möglichst aus der Zeiterfassung oder den Aktennotizen ziehen – je konkreter, desto brauchbarer die Anlage.
2. Anlage der Rechnung unmittelbar beifügen, nicht auf Nachfrage nachreichen.
3. Bei komplexen Rechnungen die Anlage im Gespräch durchgehen statt sie nur zu versenden.
4. Bei Zeitgebühren die Aufstellung ohnehin aufbewahren – sie ist im Streitfall die Grundlage.

## Qualitätssicherung

- **Beträge und Vorschriften nicht aus der KI-Antwort übernehmen**, sondern aus der Rechnung. Das Modell darf beschreiben, nicht rechnen.
- Prüfen, ob die Beschreibung mit der tatsächlich erbrachten Leistung übereinstimmt – eine geschönte Anlage ist im Streitfall schlechter als keine.
- Die Rechnung selbst muss § 9 StBVV genügen: mitgeteilte Berechnung in Textform (Abs. 1), darin Beträge der einzelnen Gebühren und Auslagen, Vorschüsse, kurze Bezeichnung des Gebührentatbestands, Bezeichnung der Auslagen, angewandte Vorschriften und bei Wertgebühren der Gegenstandswert (Abs. 2). Ohne mitgeteilte Berechnung ist die Vergütung nicht einforderbar. Die Anlage ersetzt die Berechnung nicht. Fundstellen für [JAHR] verifizieren.
- **Freigabe durch einen Berufsträger vor dem Versand, ausnahmslos** (Freigabestufe 3 in `DATENSCHUTZ.md`). Die Anlage begleitet eine Vergütungsforderung; sie berührt Vergütungs- und Berufsrecht. Vier-Augen-Prinzip: Eine zweite Person gleicht Anlage und Rechnung Position für Position ab.

## Varianten

- **Standardanlage:** "Erzeuge eine Vorlage für Jahresabschluss und Einkommensteuererklärung, in der nur noch Zahlen und Zeiten einzusetzen sind."
- **Vorab-Transparenz:** "Erzeuge aus dem Auftragsumfang eine Übersicht, die der Mandant VOR Beginn erhält: welche Leistungen enthalten sind und welche gesondert berechnet werden."
- **Leistungspakete:** "Formuliere aus dem Leistungsumfang drei Pakete – Basis, Standard, Umfassend – mit klarer Abgrenzung, was jeweils nicht enthalten ist."
- **Zeiterfassung auswerten:** "Fasse die folgende Zeiterfassung zu abrechenbaren Tätigkeiten zusammen und markiere Zeiten, die keiner Position zuzuordnen sind."
