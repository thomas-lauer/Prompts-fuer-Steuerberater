# 53 – Investitionsabzugsbetrag § 7g EStG überwachen

**Problem:** Der Investitionsabzugsbetrag aus einem Vorjahr läuft aus, niemand hat die Frist geführt; die Rückgängigmachung kommt mit Verzinsung und als Mandantenkonflikt zurück.
**Rolle:** Bilanzbuchhalter, Sachbearbeiter Jahresabschluss, Steuerberater als Entscheider
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Jahresabschluss), DATEV Anlagenbuchführung für die Investitionen der Folgejahre, Fristenverwaltung in DATEV Eigenorganisation comfort, DATEV DMS
**Was du bereitstellen musst:** Übersicht der gebildeten Abzugsbeträge mit Jahr der Bildung, Betrag, geplantem Wirtschaftsgut, verwendetem Teilbetrag und Rest; Zugänge des laufenden Jahres samt Art der betrieblichen Nutzung; Gewinnkennzahl der betroffenen Jahre; Angaben zu Veräußerung, Umwandlung oder Betriebsaufgabe.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Steuernummer, Aktenzeichen und Lieferantennamen durch Platzhalter ersetzen (`Mandant A`, `Lieferant 1`). Für die Überwachung genügen Jahr, Betrag, Art des Wirtschaftsguts und Nutzungsangaben. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Sachbearbeiter Jahresabschluss in einer deutschen Steuerkanzlei und
baust einen Überwachungsplan für Investitionsabzugsbeträge nach § 7g EStG. Du
berechnest keine Fristen und behauptest keine Beträge – du machst sichtbar, was
ein Mensch entscheiden und rechnen muss.

AUFGABE
Erzeuge aus der folgenden Übersicht einen Überwachungsplan mit einem Status je
Abzugsbetrag und dazu ein Mandantenschreiben, das die Entscheidung einfordert.

MANDANTENRAHMEN
- Rechtsform: [Einzelunternehmen / GbR / GmbH & Co. KG / Freiberufler / …]
- Gewinnermittlung: [Bilanz / EÜR]
- Laufendes Wirtschaftsjahr: [VON BIS]
- Gewinnsituation: [GEWINNSITUATION]
- Geplante Investitionen: [GEPLANTE INVESTITIONEN]
- Veränderungen im Betrieb: [Veräußerung / Aufgabe / Umwandlung / keine]

DATEN
1. Gebildete Abzugsbeträge (Jahr der Bildung | Betrag | geplantes Wirtschaftsgut
   | bereits verwendet | Rest):
   [ÜBERSICHT EINFÜGEN]
2. Zugänge des laufenden Jahres (Bezeichnung | Datum | Kosten | Art der
   betrieblichen Nutzung):
   [ZUGÄNGE EINFÜGEN]
3. Gewinnkennzahl der betroffenen Jahre:
   [GEWINNKENNZAHLEN EINFÜGEN]

PRÜFE JE ABZUGSBETRAG IN DIESER REIHENFOLGE
1. Investitionsfrist: Benenne, welche Frist läuft und woraus sie folgt.
   Berechne sie NICHT.
2. Verwendungsvoraussetzungen: Art des Wirtschaftsguts, betriebliche Nutzung und
   Verbleib im Betrieb – ohne Prozentsätze und Zeiträume als feststehend
   auszugeben.
3. Zuordnung: Passt ein Zugang des laufenden Jahres zum geplanten
   Wirtschaftsgut? Begründe die Zuordnung oder benenne sie als offen.
4. Hinzurechnung bei Investition: Wann kommt sie in Betracht, welches Wahlrecht
   besteht daneben?
5. Rückgängigmachung bei Nichtinvestition: Welcher Vorgang wird ausgelöst,
   welche Bescheide sind betroffen, welche Nebenfolgen stehen im Raum
   (Verzinsung nur benennen, nicht berechnen)? Benenne ausdrücklich, welche
   Zinsvorschrift gilt und ob die Rückgängigmachung als rückwirkendes Ereignis
   behandelt wird oder ob das ausgeschlossen ist, mit Norm, Absatz und Satz
   (für [JAHR] verifizieren). Berechne weder Zinsen noch Zinsläufe.
6. Verhältnis zur Sonderabschreibung nach derselben Vorschrift: Halte
   ausdrücklich fest, dass Abzugsbetrag und Sonderabschreibung zwei getrennte
   Begünstigungen sind. Prüfe je Begünstigung eigenständig, ob sie die andere
   voraussetzt oder unabhängig von ihr in Betracht kommt, und nenne Reihenfolge
   und Bemessungsgrundlage mit Rechtsgrundlage
   (Fundstelle – für [JAHR] verifizieren).
7. Gewinngrenze: Welche Größe ist maßgeblich, für welches Jahr, und was folgt
   daraus für eine Neubildung? Nenne keinen Betrag als feststehend.
8. Schädliche Vorgänge: Veräußerung, Entnahme, Nutzungsänderung, Aufgabe,
   Umwandlung – welche Folge löst welcher Vorgang aus?

FRISTEN UND RECHTSFOLGEN
Berechne KEINE Fristen und nenne keine Fristlängen und keine Rechtsfolgen einer
Versäumnis als feststehend. Liste stattdessen auf, WELCHE Fristen im Raum
stehen, jeweils mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren",
ohne Datum und ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu
berechnen und im Fristenprogramm zu erfassen."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne die fehlenden
   Angaben.
2. Setze je Abzugsbetrag einen Status, der sich allein aus der Datenlage ergibt,
   nicht aus einer Fristberechnung: [zugeordnet und dokumentiert /
   Zuordnung offen / Angaben fehlen / Fristlage durch die Kanzlei zu prüfen].
   Begründe den Status nur mit den vorliegenden Angaben. Beurteile NICHT, ob eine
   Frist abgelaufen, überfällig oder noch offen ist. Setze bei jedem Abzugsbetrag
   den Vermerk "Fristlage von einem Menschen zu prüfen und im Fristenprogramm zu
   erfassen".
3. Nenne KEINE Beträge, Prozentsätze, Gewinngrenzen und Fristlängen als
   feststehend. Schreibe, WELCHER Wert nachzuschlagen ist, mit dem Zusatz
   "für [JAHR] verifizieren".
4. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
5. Das Mandantenschreiben trägt den Betreff "Investitionsentscheidung
   erforderlich", ist in der Sie-Form gehalten, erklärt jeden Fachbegriff in
   einem Halbsatz, umfasst höchstens 300 Wörter und stellt beide Wege mit ihren
   Folgen dar: investieren oder nicht investieren. Es enthält kein Datum und
   keine Frist, sondern den Satz, dass die Kanzlei den Termin gesondert mitteilt.
6. Formuliere jede Zuordnung, die nicht aus den Daten folgt, als Vermutung.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Überwachungsplan (Abzugsbetrag | Jahr der Bildung | Betrag | Rest |
   Status | Begründung | nächste Handlung | Verantwortlicher)
3. Fristenübersicht ohne Datum und ohne Dauer, je Frist mit Rechtsgrundlage und
   dem Hinweis auf die Berechnung durch einen Menschen
4. Folgenabschätzung je Weg (investieren / nicht investieren)
5. Mandantenschreiben "Investitionsentscheidung erforderlich"
6. Interne Notiz (was der Berufsträger entscheiden muss)
7. Was ich nicht sicher weiß
```

## Anwendung

1. Übersicht der Abzugsbeträge aus Handakte und Vorjahresabschluss zusammenstellen; ohne das Bildungsjahr je Betrag ist keine Überwachung möglich.
2. Prompt ausführen; die Fristenübersicht sofort an die Fristenverwaltung geben, damit ein Mensch die Termine rechnet und erfasst.
3. Überwachungsplan in der Dauerakte ablegen und bei jedem Abschluss fortführen.
4. Mandantenschreiben erst nach Freigabe des Berufsträgers versenden.
5. Entscheidung des Mandanten mit Begründung schriftlich festhalten – bei einer Nichtinvestition ist die Dokumentation der Beratung der Haftungsschutz.

## Qualitätssicherung

- **Kein Datum aus der KI-Antwort übernehmen.** Fristen berechnet und erfasst ein Mensch; bei auslaufenden Investitionsfristen prüft eine zweite Person nach.
- **Das Ergebnis ist ein Entwurf.** Vor dem Versand prüfen: Zuordnung der Zugänge, Status je Abzugsbetrag, Vollständigkeit, Darstellung beider Wege.
- **Vier-Augen-Prinzip und Freigabe:** Mandantenschreiben und Folgenabschätzung gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- Verzinsung und Rückgängigmachung nie überschlägig beziffern, sondern im Programm rechnen.
- **Rechtsstand prüfen an:** § 7g EStG – einschließlich der Regelung zum rückwirkenden Ereignis – und § 233a AO, insbesondere Abs. 2a, im amtlichen Volltext (gesetze-im-internet.de), BMF-Schreiben über die Datenbank des Bundesfinanzministeriums, Änderungsgesetze über das Bundesgesetzblatt, ergänzend DATEV LEXinform.

## Varianten

- **Kanzleiweite Auswertung:** Zusatz "Verarbeite mehrere Mandate und sortiere nach Status."
- **Neubildung prüfen:** Zusatz "Prüfe, ob eine Neubildung in Betracht kommt, und benenne die nachzuschlagenden Voraussetzungen."
- **Nach der Nichtinvestition:** Zusatz "Erzeuge ein Schreiben, das die Folgen der Rückgängigmachung erklärt, ohne Beträge zu nennen." Ergänzt Prompt 11.
- **Jahresplanung:** Zusatz "Übernimm den Überwachungsplan in den Jahresterminplan." Ergänzt Prompt 17.
