# 51 – Cut-off- und Nachlaufcheck zum Bilanzstichtag

**Problem:** Nach dem Stichtag eingehende Rechnungen, Abgrenzungsposten und noch nicht abgerechnete Leistungen werden vergessen, weil niemand eine strukturierte Nachlaufliste führt.
**Rolle:** Bilanzbuchhalter, Buchhaltung, Fachassistent Rechnungswesen
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Buchungssatzliste des Nachlaufzeitraums, OPOS-Liste, Kontennachweise, Jahresabschluss), DATEV Unternehmen online für Belegbilder und Belegdaten, DATEV DMS
**Was du bereitstellen musst:** Buchungsliste des Nachlaufzeitraums mit Belegdatum, Buchungsdatum, Konto, Gegenkonto, Betrag und – soweit vorhanden – Leistungszeitraum; OPOS-Liste zum Stichtag; Kontennachweise der Abgrenzungs-, Anzahlungs- und sonstigen Forderungs- und Verbindlichkeitskonten; Liste der Dauerschuldverhältnisse; bekannte Ereignisse nach dem Stichtag.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Steuernummer und Namen von Geschäftspartnern durch Platzhalter ersetzen (`Mandant A`, `Kreditor 1`, `Debitor 1`, `Konto ****1234`). Für die Prüfung genügen Belegdatum, Leistungszeitraum, Konto, Betrag und Leistungsart. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Bilanzbuchhalter in einer deutschen Steuerkanzlei und führst den
Nachlaufcheck zum Bilanzstichtag. Du ordnest jeden Vorgang nach dem
Leistungszeitraum zu, nicht nach dem Belegdatum, und du erfindest keinen
Sachverhalt, den die Liste nicht hergibt.

AUFGABE
Prüfe die folgenden Nachlaufbuchungen und offenen Posten daraufhin, ob sie das
abgelaufene oder das neue Wirtschaftsjahr betreffen, und erzeuge daraus eine
Abgrenzungsliste mit einem Prüfvorschlag je Position.

MANDANTENRAHMEN
- Rechtsform: [Einzelunternehmen / GbR / GmbH / UG / GmbH & Co. KG / …]
- Kontenrahmen: [SKR03 / SKR04]
- Stichtag: [STICHTAG]
- Nachlaufzeitraum der eingefügten Liste: [VON BIS]
- Umsatzsteuer: [Regelbesteuerung / Kleinunternehmer § 19 UStG /
  teilweise steuerfrei], Besteuerungsart: [Soll / Ist]
- Branche und laufende Projekte: [BRANCHE UND PROJEKTE]

DATEN
1. Nachlaufbuchungen (Belegdatum | Buchungsdatum | Konto | Gegenkonto | Betrag |
   Leistungszeitraum | Leistungsart):
   [BUCHUNGSLISTE EINFÜGEN]
2. Offene Posten zum Stichtag:
   [OPOS-LISTE EINFÜGEN]
3. Dauerschuldverhältnisse (Art | Laufzeit | Zahlungsweise | Betrag):
   [DAUERSCHULDVERHÄLTNISSE EINFÜGEN]
4. Bekannte Ereignisse nach dem Stichtag:
   [EREIGNISSE EINFÜGEN]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Periodenzuordnung: Fällt die Leistung in das abgelaufene Wirtschaftsjahr?
   Maßgeblich ist der Leistungszeitraum. Fehlt er, benenne das als Lücke und
   ordne NICHT nach dem Belegdatum zu.
2. Aktive Rechnungsabgrenzung: Ausgabe vor dem Stichtag, die Aufwand für eine
   BESTIMMTE ZEIT nach dem Stichtag darstellt. Prüfe das Merkmal "bestimmte
   Zeit" ausdrücklich und begründe es; fehlt es, kommt kein
   Rechnungsabgrenzungsposten in Betracht – ordne dann nach Schritt 4 oder 5 ein.
3. Passive Rechnungsabgrenzung: Einnahme vor dem Stichtag, die Ertrag für eine
   BESTIMMTE ZEIT nach dem Stichtag darstellt, mit derselben ausdrücklichen
   Prüfung des Merkmals.
4. Sonstige Verbindlichkeiten für empfangene, noch nicht abgerechnete
   Leistungen – abzugrenzen von einer Rückstellung, wenn Grund und Höhe
   feststehen. Begründe die Einordnung.
5. Sonstige Forderungen für erbrachte, noch nicht abgerechnete Leistungen,
   einschließlich Boni, Rückvergütungen und Erstattungsansprüchen.
6. Wertaufhellung oder Wertbegründung: Ordne jedes Ereignis nach dem Stichtag
   ausdrücklich einer der beiden Kategorien zu und begründe die Zuordnung.
   Wertbegründende Ereignisse dürfen den Stichtagswert nicht verändern. Benenne
   den Zeitraum, innerhalb dessen eine Kenntnis noch wertaufhellend wirkt, sowie
   seinen Endpunkt, mit Rechtsgrundlage (für [JAHR] verifizieren).
7. Dauerschuldverhältnisse: Miete, Leasing, Versicherungen, Wartung, Lizenzen,
   Beiträge – prüfe Vorauszahlungen, nachschüssige Zahlungen und
   Abrechnungsperioden, die den Stichtag überschreiten.
8. Erhaltene und geleistete Anzahlungen: richtige Ausweisseite, Umsatzsteuer bei
   Anzahlungen, Abgrenzung zu Teilleistungen.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und liste je Position die
   fehlenden Angaben auf.
2. Jede Position ist ein PRÜFVORSCHLAG, keine Buchungsanweisung. Formuliere so:
   "Prüfvorschlag: … – zu entscheiden durch die Kanzlei." Nenne keine
   Buchungssätze und keine Kontonummern als gesichert; Kontonummern
   unterscheiden sich je Kontenrahmen und je individuellem Kontenplan.
3. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
4. Kennzeichne jede Betragsgrenze, jeden Steuersatz und jede Vereinfachungsregel
   mit dem Zusatz "für [JAHR] verifizieren".
5. Höchstens 20 Positionen in der Abgrenzungsliste. Sortiere nach
   Ergebniswirkung, nicht nach Datum, und lasse Kleinbeträge ohne Folge weg.
6. Formuliere jede Annahme über den Leistungszeitraum als Vermutung und
   kennzeichne sie als Vermutung.
7. ABBRUCHREGEL: Eine Periodenverschiebung im Nachlauf kann eine bereits
   abgegebene Umsatzsteuervoranmeldung berühren. Deutet eine Position darauf hin,
   dass eine bereits abgegebene Voranmeldung unrichtig ist oder berichtigt werden
   muss, arbeite an dieser Position NICHT weiter. Gib nur aus: "Anzeichen für eine
   Berichtigungspflicht bei einer bereits abgegebenen Umsatzsteuervoranmeldung –
   Bearbeitung an dieser Stelle abgebrochen, Prüfung durch einen Berufsträger
   außerhalb des KI-Werkzeugs."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Abgrenzungsliste (Nr. | Position | Betrag | Leistungszeitraum | Einordnung |
   Prüfvorschlag | Rechtsgrundlage | Sicherheit als hoch, mittel oder gering)
3. Wertaufhellung und Wertbegründung (Ereignis | Einordnung | Begründung)
4. Rückfrageliste an den Mandanten (Nr. | Position | Unsere Frage |
   Antwort des Mandanten, Spalte leer)
5. Interne Notiz (was vor der Abschlussfreigabe geklärt sein muss)
6. Was ich nicht sicher weiß
```

## Anwendung

1. Nachlaufzeitraum festlegen und in der Kanzlei einheitlich halten; die Buchungsliste um die Spalte Leistungszeitraum ergänzen, sonst arbeitet der Prompt blind.
2. Prompt ausführen; die Abgrenzungsliste als Arbeitsliste ausdrucken und Position für Position im Programm entscheiden.
3. Rückfrageliste ohne interne Vermerke an den Mandanten geben, Antworten in der Liste nachtragen.
4. Nach dem Abschluss die Liste als Muster für den nächsten Stichtag sichern und um die Positionen ergänzen, die diesmal gefehlt haben.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Verwendung prüfen: Periodenzuordnung je Position, Einordnung als Abgrenzung, Verbindlichkeit oder Rückstellung, Umsatzsteuerbehandlung bei Anzahlungen.
- Keine Buchung aus der KI-Antwort übernehmen. Kontonummern im Kontenplan des Mandanten nachschlagen.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person prüft die Abgrenzungsliste gegen die Belege; die Abschlussfreigabe erteilt ein Berufsträger und dokumentiert sie (Freigabestufe 3 in `DATENSCHUTZ.md`).
- Die Unterscheidung zwischen wertaufhellenden und wertbegründenden Ereignissen entscheidet über den Bilanzansatz und wird vom Modell regelmäßig zu weit gefasst – jede Zuordnung einzeln nachvollziehen.
- **Rechtsstand prüfen an:** § 250, § 252 HGB und § 5 Abs. 5 EStG im amtlichen Volltext (gesetze-im-internet.de), einschlägige BMF-Schreiben über die Datenbank des Bundesfinanzministeriums, ergänzend DATEV LEXinform.

## Varianten

- **Nur Umsatzsteuer:** Zusatz "Beschränke dich auf die umsatzsteuerlichen Folgen des Nachlaufs, insbesondere Anzahlungen, Teilleistungen und den Zeitpunkt des Vorsteuerabzugs." Ergänzt Prompt 04.
- **Quartalsabschluss:** Zusatz "Behandle den Stichtag als Quartalsstichtag und beschränke die Liste auf Positionen über einer Wesentlichkeitsgrenze, die ich vorgebe."
- **Projektgeschäft:** Zusatz "Ergänze einen Prüfschritt zu unfertigen Leistungen und zum Stand der Abrechnung je Projekt."
- **Erstellung durch den Mandanten:** Zusatz "Formuliere die Rückfrageliste so, dass ein Mitarbeiter des Mandanten sie ohne Fachkenntnis beantworten kann." Ergänzt Prompt 11.
