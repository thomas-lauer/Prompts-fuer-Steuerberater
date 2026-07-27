# 38 – GoBD-Checkliste Kassenführung für den Mandanten

**Problem:** Kassenmängel sind der häufigste Grund für Hinzuschätzungen bei bargeldintensiven Betrieben – meist, weil niemand dem Mandanten je gesagt hat, was täglich, was monatlich und was einmalig zu tun ist.
**Rolle:** Steuerberater, Buchhaltung, Kanzleileitung
**DATEV-Bezug:** Kanzlei-Rechnungswesen (Kassenbuch), DATEV Unternehmen online (Kassenbuch online), DATEV Datenprüfung / Kassenarchiv online (DSFinV-K-Export)
**Was du bereitstellen musst:** Kassenart und Anzahl der Kassen, eingesetztes System, Branche, ob eine TSE vorhanden ist, ob die Mitteilung an das Finanzamt erfolgt ist, wie das Kassenbuch geführt wird.
**Datensparsamkeit:** Keine Umsatzzahlen, keine Seriennummern von TSE oder Kasse, keine Steuernummer, keine Mitarbeiternamen. Bedienerkennungen als `Bediener 1–n`.
Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du bist Steuerberater und prüfst die Kassenführung bargeldintensiver
Betriebe. Eine Hinzuschätzung hängt selten an einem falschen Betrag,
sondern an fehlenden Aufzeichnungen. Du beschreibst Pflichten als
Handlungen mit Takt (täglich / monatlich / einmalig), nicht als Rechtsprosa.

AUFGABE
Erstelle eine Prüfliste zur Kassenführung, ein Mandantenmerkblatt und eine
interne Risikoeinschätzung.

BETRIEBSPROFIL
- Branche: [z. B. Gastronomie / Einzelhandel / Friseur / Taxi]
- Rechtsform, Gewinnermittlung: [ANGABE / Bilanz / EÜR]
- Kassenart: [offene Ladenkasse / elektronisches Aufzeichnungssystem mit
  TSE / beides parallel / mehrere Kassen an mehreren Standorten]
- System und Hersteller: [ANGABE oder "unbekannt"]
- TSE: [ja / nein / unbekannt], Art: [Hardware / Cloud]
- Mitteilung an das Finanzamt erfolgt: [ja / nein / unbekannt]
- Kassenbuch heute: [Papier / Excel / Kassenbuch online / Kassensystem]
- Auffälligkeiten: [z. B. Minusbestände, runde Beträge, fehlende
  Zählprotokolle oder Tagesabschlüsse]
- Gesetzgebungsvorhaben zur Verpflichtung, elektronische Aufzeichnungssysteme
  einzusetzen: Stand für [JAHR] verifizieren. Bei offener Ladenkasse als
  Prüfpunkt aufnehmen, ob der Betrieb von einer künftigen Verpflichtung erfasst
  wäre (Schwelle, Anwendungszeitpunkt und Verfahrensstand – für [JAHR]
  verifizieren – nicht als geltendes Recht darstellen).

ARBEITSWEISE
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab. "Unbekannt" bei TSE
   oder Mitteilung ist ein Prüfpunkt hoher Priorität, keine Nebensache.
2. Nimm NUR Prüfpunkte auf, die zu dieser Kassenart passen. Eine kurze
   zutreffende Liste ist besser als eine vollständige unzutreffende.
3. Erkläre jeden Fachbegriff in einem Halbsatz in Klammern.

BLOCK A – OFFENE LADENKASSE
1. Tägliche Zählung bei Geschäftsschluss.
2. Zählprotokoll (Aufstellung der gezählten Stückelung): Kennzeichne diesen Punkt
   ausdrücklich als EMPFEHLUNG, nicht als Pflicht – ein Zählprotokoll ist nach der
   Rechtsprechung nicht zwingend, erhöht aber die Beweiskraft der
   Kassenaufzeichnungen erheblich (Fundstelle – für [JAHR] verifizieren).
   Beschreibe Inhalt, Unterschrift und Aufbewahrung. Trenne im Ausgabeformat
   durchgängig "Pflicht" von "Empfehlung" und nenne bei jedem Pflichtpunkt die
   Rechtsgrundlage.
3. Kassenbericht, RÜCKWÄRTS gerechnet: ausgezählter Kassenendbestand
   ./. Kassenanfangsbestand des Tages ./. Einlagen + bar bezahlte Ausgaben
   + Entnahmen = Tageslosung. Gib die Rechnung als Formel mit allen fünf Größen
   aus. Ein Kassenbuch, in das die Losung vorwärts eingetragen wird, ist kein
   Kassenbericht.
4. Kassensturzfähigkeit: rechnerischer und gezählter Bestand stimmen
   jederzeit überein; Differenzen aufzeichnen, nicht glätten.
5. Keine Minusbestände – warum sie zwingend ein Fehler sind und wie sie
   entstehen (verspätete Einlagen, nachgetragene Ausgaben).
6. Privatentnahmen und -einlagen taggenau mit Beleg, keine Sammelbuchung.
7. Zeitnahe, vollständige Erfassung; keine Änderung ohne erkennbare Korrektur.
8. Einzelaufzeichnungspflicht und ihre Ausnahme beim Verkauf an eine Vielzahl
   nicht bekannter Personen gegen Barzahlung – Voraussetzungen als
   "für [JAHR] verifizieren" markieren.

BLOCK B – ELEKTRONISCHES AUFZEICHNUNGSSYSTEM
1. Zertifizierte technische Sicherheitseinrichtung (TSE): vorhanden, aktiv,
   Ablaufdatum überwacht, Ausfallverfahren dokumentiert.
2. Belegausgabepflicht: Beleg in unmittelbarem zeitlichen Zusammenhang mit
   dem Geschäftsvorfall erstellt und zur Entgegennahme angeboten;
   elektronische Ausgabe nur mit Zustimmung des Kunden; Befreiung auf Antrag
   als Prüfpunkt benennen, ohne Voraussetzungen zu behaupten.
3. Mitteilungspflicht über Art und Zahl der Systeme (§ 146a Abs. 4 AO):
   Verfahren (elektronische Übermittlung), Angaben, Fristen für Bestand,
   Neuanschaffung und Außerbetriebnahme; alle Systeme einer Betriebsstätte in
   einer Mitteilung. Markiere JEDE Frist als "Frist – für [JAHR] verifizieren".
   Ist die Mitteilung mit "nein" oder "unbekannt" angegeben, behandle das nicht
   als offenen Termin, sondern als möglicherweise BEREITS VERSÄUMTE Pflicht:
   nimm einen eigenen Prüfpunkt "Meldestand feststellen und Mitteilung nachholen"
   mit höchster Priorität auf und verweise die Frage nach Folgen einer
   verspäteten Mitteilung an den Berufsträger, ohne sie zu bewerten.
4. Verfahrensdokumentation zum Kassensystem samt Herstellerunterlagen,
   Bedienungsanleitung, Programmierprotokollen, Stammdatenänderungen.
5. Datenexport nach dem Standard für Kassendaten (DSFinV-K): vollständig und
   auswertbar; probeweise erzeugen und lesbar prüfen.
6. Bedienerverwaltung: eindeutige Kennung je Bediener, keine Sammelanmeldung,
   Rechte für Storno und Preisänderung eingeschränkt.
7. Stornos, Retouren, Rabatte, Nachbuchungen lückenlos aufgezeichnet und
   begründet, nicht gelöscht.
8. Trainings- und Schulungsbuchungen gekennzeichnet, vom Echtbetrieb
   getrennt, im Export erkennbar.
9. Tagesabschluss, lückenlose Nummernfolge, Aufbewahrung aller Einzeldaten –
   nicht nur der Tagessummen; bei mehreren Kassen je Kasse eigene
   Aufzeichnung und nachvollziehbare Zusammenführung.

BLOCK C – BEIDE KASSENARTEN
Aufbewahrung: welche Kassenunterlagen wie lange und in welcher Form
(digital, maschinell auswertbar, unveränderbar). Behandle Buchungsbelege und
übrige Unterlagen getrennt und markiere JEDE Fristangabe als "Frist und
Anwendungsbereich für [JAHR] verifizieren".

ANFORDERUNGEN
- Markiere ALLE Fristen, Stichtage, Betragsgrenzen und Prozentsätze als
  "für [JAHR] verifizieren". Lieber keinen Wert als einen unmarkierten.
- Kennzeichne jede unsichere Aussage. Rate nicht.
- Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
  Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
  "für [JAHR] verifizieren". Kannst du sie nicht angeben, kennzeichne die Aussage
  als "ohne Fundstelle – vor Verwendung belegen". Erfinde keine Paragrafen,
  BMF-Schreiben oder Dokumentnummern; unsichere: "Fundstelle offen – bitte
  recherchieren".
- Formuliere Ursachenaussagen zu den Auffälligkeiten als Vermutung.

AUSGABEFORMAT
1. Checkliste zum Abhaken: ☐ | Prüfpunkt | Pflicht oder Empfehlung |
   Rechtsgrundlage (bei Pflicht) | Takt | Nachweis | erledigt (leer)
2. Mandantenmerkblatt, eine Seite, Sie-Form, keine Paragrafen:
   "täglich" · "monatlich" · "einmalig" · "das nie"
3. Interne Risikoeinschätzung: drei größte Schätzungsrisiken mit Begründung
   und Sofortmaßnahme; was vor der nächsten Kassen-Nachschau vorliegen muss.
4. "Was ich nicht sicher weiß"
```

## Anwendung

1. Kassenart vorab klären. Eine Registrierkasse ohne TSE ist kein Ausstattungs-, sondern ein Sofortproblem – dann zuerst Block B Punkte 1 und 3.
2. Checkliste ausgedruckt vor Ort durchgehen. Die Antwort auf "haben Sie ein Zählprotokoll?" fällt je nach Kanal unterschiedlich aus.
3. Den DSFinV-K-Export einmal testweise anfordern und einlesen. Ein Export, der erst in der Nachschau erzeugt wird, funktioniert erfahrungsgemäß nicht.
4. Ergebnis in der Mandantenakte dokumentieren – gerade die Punkte, die der Mandant nicht umsetzen will.

## Qualitätssicherung

- **Rechtsstand prüfen an:** § 146a AO mit der Kassensicherungsverordnung (KassenSichV), dem Anwendungserlass zur AO zu §§ 146, 146a AO und am FAQ-Katalog des BMF zur Ordnungsmäßigkeit der Kassenführung (Fassung vom 15.10.2025 – prüfen, ob eine neuere Fassung vorliegt; Stand für [JAHR] verifizieren). Für die Aufzeichnungsgrundsätze zusätzlich: GoBD, BMF-Schreiben vom 28.11.2019, zuletzt geändert durch BMF-Schreiben vom 14.07.2025 (Fassung und Änderungsstand für [JAHR] verifizieren – die GoBD wurden bereits zweimal geändert).
- **Fristen der Mitteilungspflicht selbst nachschlagen.** Für Bestandssysteme, Neuanschaffungen und Außerbetriebnahmen gelten unterschiedliche Fristen; Modellangaben dazu sind unzuverlässig.
- Bei mehreren Betriebsstätten prüfen, ob je Standort gesondert zu melden ist.
- Prüfen, ob das Merkblatt Pflichten benennt, die der Mandant mit seinem System technisch nicht erfüllen kann – dann ist vorher die Systemfrage zu klären.
- Vier-Augen-Prinzip: Freigabe durch einen Berufsträger. Die Risikoeinschätzung bleibt intern.

## Varianten

- **Kassen-Nachschau:** "Erzeuge eine Liste der Unterlagen, die bei einer unangekündigten Kassen-Nachschau binnen einer Stunde vorliegen müssen."
- **Aushang am Kassenplatz:** "Erzeuge eine Kurzfassung mit höchstens zehn Punkten."
- **Einweisung:** "Erzeuge eine Einweisung für neue Kassenkräfte, höchstens 300 Wörter, mit fünf Beispielen für Fehlbedienung."
- **Mängelbericht:** "Erzeuge aus der ausgefüllten Checkliste einen Bericht: Mangel | Risiko | zu tun | bis wann."
