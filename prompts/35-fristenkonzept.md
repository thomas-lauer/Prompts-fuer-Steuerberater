# 35 – Wiedervorlage- und Fristenkonzept für die Kanzlei

**Problem:** Fristen werden in Köpfen, Outlook-Terminen und Notizzetteln geführt; bei Urlaub oder Krankheit weiß niemand, was offen ist. Fristversäumnis ist der häufigste Haftungsfall in Steuerkanzleien.
**Rolle:** Kanzleileitung, Berufsträger, Fristenverantwortliche
**DATEV-Bezug:** DATEV Fristenkontrolle, DATEV Fristen und Bescheide, DATEV Arbeitsplatz / Eigenorganisation, DMS
**Was du bereitstellen musst:** Kanzleigröße und Rollen, verwendete Programme, bisherige Praxis der Fristenerfassung, bekannte Schwachstellen, heutige Zuständigkeiten.
**Datensparsamkeit:** Keine Mandantendaten einfügen. Mitarbeiter nur als Rollen benennen (`Sachbearbeitung 1`, `Sekretariat`, `Berufsträger A`). Für das Konzept genügen Strukturangaben. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Organisationsberater für deutsche Steuerkanzleien und schreibst
verbindliche Kanzleiregelungen. Du schreibst so, dass eine neue Mitarbeiterin
danach arbeiten kann, ohne nachzufragen: kurze Sätze, klare Zuständigkeit,
kein Konjunktiv.

AUFGABE
Erzeuge ein Wiedervorlage- und Fristenkonzept für unsere Kanzlei. Das Konzept
ist eine Organisationsregelung, kein Einzelfallgutachten.

KANZLEIRAHMEN
- Größe: [ZAHL BERUFSTRÄGER / ZAHL MITARBEITER / ZAHL STANDORTE]
- Rollen: [z. B. Berufsträger, Sachbearbeitung, Sekretariat,
  Fristenverantwortliche, Auszubildende]
- Programme: [z. B. DATEV Fristenkontrolle, DATEV Fristen und Bescheide,
  DMS, Outlook, Excel-Liste]
- Bisherige Praxis: [WIE FRISTEN HEUTE ERFASST UND ÜBERWACHT WERDEN]
- Bekannte Schwachstellen: [z. B. Urlaubsvertretung, digitaler Posteingang,
  Fristen aus Telefonaten, mehrere Standorte]
- Bereits schriftlich geregelt: [ANGABE / nichts]

ANFORDERUNGEN
1. Gliedere die Fristarten in vier Gruppen und behandle jede getrennt:
   a) gesetzliche Abgabefristen,
   b) Rechtsbehelfs- und Rechtsmittelfristen,
   c) mandantenbezogene Zulieferfristen,
   d) interne Bearbeitungs- und Wiedervorlagefristen.
   Beschreibe je Gruppe: Auslöser, wer erfasst, wo, wer überwacht,
   wie quittiert wird, wann eskaliert wird.
2. Nenne KEINE konkreten Fristlängen, keine Stichtage und keine gesetzlichen
   Termine als feststehend. Das Konzept regelt das VERFAHREN, nicht die
   Fristdauer. Wo eine Fristdauer erwähnt werden müsste, schreibe stattdessen
   "Dauer im Einzelfall durch den Berufsträger festzustellen".
3. Schreibe ausdrücklich und an sichtbarer Stelle: Fristberechnung wird
   niemals einer KI überlassen. Ein Sprachmodell darf Fristen weder berechnen
   noch bestätigen noch überwachen; es erzeugt allenfalls Entwürfe von
   Schriftsätzen. Begründe das kurz. Regle außerdem, dass jede Person, die
   KI-Werkzeuge in der Kanzlei einsetzt, vorher nachweislich eingewiesen wird
   (KI-Kompetenz nach Art. 4 KI-VO, seit 2.2.2025 – für [JAHR] verifizieren),
   und dass diese Einweisung mit Datum dokumentiert wird.
3a. Bestimme GENAU EIN führendes Fristensystem. Jede Frist ist dort und nur dort
    maßgeblich erfasst. Kalender, Aufgabenlisten und Tabellenblätter dürfen
    Erinnerungen enthalten, sind aber niemals Fristennachweis; regle
    ausdrücklich, dass eine nur dort notierte Frist als nicht erfasst gilt.
    Nenne in der Entscheidungsliste, welches System die Kanzlei als führend
    festlegt.
4. Regle das VIER-AUGEN-PRINZIP für Rechtsbehelfsfristen: wer erfasst, wer
   prüft nach, wie das dokumentiert wird, was gilt, wenn die zweite Person
   nicht verfügbar ist.
4a. Regle die AUSGANGSKONTROLLE gesondert und gestuft:
    - Eine Frist wird im Fristenprogramm erst gestrichen, nachdem anhand der
      Akte festgestellt ist, dass der fristwahrende Schriftsatz tatsächlich
      abgesandt wurde und nichts mehr zu veranlassen ist.
    - Nachweis des Abgangs ist Pflicht und wird zur Akte genommen (Sendeprotokoll,
      Übermittlungsprotokoll, Postausgangsvermerk). Ohne Nachweis bleibt die
      Frist offen.
    - Am Abend jedes Arbeitstages prüft eine benannte Person die an diesem Tag
      ablaufenden Fristen auf Erledigung.
    - Regle VORFRISTEN: zu jeder Rechtsbehelfsfrist wird zusätzlich eine
      Vorfrist notiert, deren Abstand die Kanzlei festlegt.
5. Regle die Vertretung: Urlaub, Krankheit, kurzfristiger Ausfall –
   auch der fristenverantwortlichen Person selbst.
6. Regle die Dokumentation: was festgehalten wird, wo, wie lange, und wie im
   Streitfall nachgewiesen wird, dass die Frist geführt war. Halte fest, dass zu
   jeder Frist ein Vermerk in der Handakte geführt wird (Auslöser,
   Berechnungsgrundlage, erfassende und nachprüfende Person, Abgangsnachweis) und
   wie lange dieser aufbewahrt wird.
7. Regle den Posteingang: Papier, elektronisch, Telefon, persönliche Übergabe.
   Jede Eingangsart braucht einen Weg in die Fristenerfassung.
8. Benenne zu jedem Abschnitt die berührte berufs- oder haftungsrechtliche
   Anforderung mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren",
   statt sie zu umschreiben – mindestens: allgemeine Berufspflicht zur
   gewissenhaften Berufsausübung (§ 57 Abs. 1 StBerG), Handakte und deren
   Aufbewahrung (§ 66 StBerG), Berufshaftpflichtversicherung (§ 67 StBerG),
   Zurechnung des Vertreterverschuldens bei versäumten Fristen
   (§ 110 Abs. 1 Satz 2 AO). Erfinde keine Fundstelle; unsichere: "Fundstelle
   offen – bitte recherchieren". Führe alle genannten Fundstellen am Ende in
   einer Tabelle "Zu verifizierende Rechtsgrundlagen" mit Spalte
   "geprüft von (leer)".
9. Alles, was die Kanzlei selbst entscheiden muss, gehört NICHT als Annahme
   in den Text, sondern in die Entscheidungsliste am Ende.
10. Höchstens 1.200 Wörter für das Konzept.

AUSGABEFORMAT
1. (Fristenkonzept) – nummerierte Abschnitte:
   1. Grundsätze (einschließlich des Satzes zur KI und des führenden
      Fristensystems)
   2. Fristarten a–d
   3. Erfassung
   4. Überwachung und Quittierung
   5. Ausgangskontrolle, Sendenachweis und Vorfristen
   6. Eskalation
   7. Vier-Augen-Prinzip bei Rechtsbehelfsfristen
   8. Vertretung
   9. Dokumentation und Nachweis
2. (Rollenmatrix) – Tabelle:
   Aufgabe | Rolle verantwortlich | Rolle prüft nach | Vertretung |
   Nachweis wo
3. (Von der Kanzlei festzulegen) – nummerierte Liste offener Punkte mit
   je einer Entscheidungsfrage.
4. (Einführungsschritte) – höchstens fünf Schritte, in Reihenfolge.
5. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | für welchen Abschnitt sie steht | geprüft von (leer)
6. (Interne Notiz) – Risiken der bisherigen Praxis, jeweils als Vermutung
   gekennzeichnet, soweit sie nicht aus meinen Angaben folgt.
```

## Anwendung

1. Bisherige Praxis ehrlich beschreiben, einschließlich der Umgehungen, die sich eingebürgert haben. Ein Konzept, das den Ist-Zustand beschönigt, wird nicht gelebt.
2. Entwurf mit den Berufsträgern durchgehen und die Entscheidungsliste Punkt für Punkt abarbeiten – erst danach ist es eine Regelung.
3. Rollenmatrix mit echten Namen hinterlegen, im Dokument aber bei Rollen bleiben, damit es Personalwechsel überlebt.
4. Konzept datieren, versionieren und im DMS ablegen. Nach Einführung einen Stichtag für die erste Kontrolle festlegen.

## Qualitätssicherung

- **Fristberechnung wird nie einer KI überlassen.** Das Modell schreibt das Konzept, nicht die Fristen. Kein Datum und keine Fristdauer aus einem Sprachmodell übernehmen.
- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Ausgangsdokuments nachgeprüft und abgezeichnet** – bei Rechtsbehelfsfristen ausnahmslos, unabhängig davon, ob ein Rechtsbehelf geplant ist. Kein Datum aus dem Modell übernehmen.
- **Freigabe durch einen Berufsträger**; das Konzept betrifft die Organisationspflichten und damit die Haftung.
- Prüfen, ob das Konzept irgendwo eine Frist als bekannt voraussetzt. Solche Stellen streichen und durch die Zuständigkeitsregel ersetzen.
- Prüfen, ob jeder Eingangsweg abgedeckt ist – der ungeregelte Weg ist der, über den die versäumte Frist kommt.
- Angaben zu berufsrechtlichen Anforderungen an der aktuellen Fassung verifizieren. Konzept jährlich überprüfen und die Prüfung dokumentieren.

## Varianten

- **Kurzfassung:** "Erzeuge eine einseitige Aushangfassung mit den fünf wichtigsten Regeln."
- **Einarbeitung:** "Leite eine abhakbare Einweisungscheckliste für neue Mitarbeiter ab, mit Unterschriftszeile."
- **Notfall:** „Erzeuge eine Regelung für den Fall einer versäumten Frist. Sie enthält in dieser Reihenfolge: (1) Sofortmaßnahmen zur Schadensminderung, (2) unverzügliche Information des zuständigen Berufsträgers, (3) unverzügliche Prüfung eines Wiedereinsetzungs- oder rückwirkenden Verlängerungsantrags durch den Berufsträger mit eigener Fristnotierung, (4) unverzügliche Anzeige an die Berufshaftpflichtversicherung mit dem ausdrücklichen Hinweis, dass gegenüber Mandant und Dritten **kein Anspruch anerkannt und keine Schuld eingeräumt** wird, (5) Information des Mandanten nur nach Abstimmung mit Berufsträger und Versicherer, (6) Dokumentation des Ablaufs, (7) Ursachenanalyse und Anpassung des Konzepts. Rechtliche Bewertung des Einzelfalls bleibt dem Berufsträger vorbehalten."
