# 54 – E-Bilanz: unverdichtete Kontennachweise vorbereiten

**Problem:** Kontennachweise sind mitzuübermitteln; beim Übermitteln zeigt sich, dass Kontenbezeichnungen und Salden nicht vorzeigefähig sind – Sammelkonten, interne Kürzel, Privatkonten, sprechende Mandantenbeschriftungen.
**Rolle:** Bilanzbuchhalter, Sachbearbeiter Jahresabschluss, Kanzleiorganisation
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (E-Bilanz, Kontennachweise, Kontenplan und Kontenbeschriftung in den Mandantenstammdaten), DATEV Bilanzbericht, DATEV DMS
**Was du bereitstellen musst:** Kontenliste des betroffenen Wirtschaftsjahres mit Kontonummer, Bezeichnung und Saldo; Kontenrahmen und etwaige individuelle Kontenbeschriftungen; Rechtsform und Größenklasse; Angabe, welche Konten Verrechnungs-, Interims- oder Privatkonten sind.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Steuernummer und Beraternummer entfernen. Kontenbezeichnungen mit Namen von Gesellschaftern, Arbeitnehmern oder Dritten durch Platzhalter ersetzen (`Gesellschafter 1`, `AN 1`) – genau diese Bezeichnungen sind der Prüfgegenstand, nicht die Personen. Für die Prüfung genügen Kontonummer, Bezeichnung und Saldo. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Sachbearbeiter Jahresabschluss in einer deutschen Steuerkanzlei und
bereitest die Kontennachweise für die E-Bilanz vor. Du beurteilst
Kontenbezeichnungen aus der Sicht eines Lesers in der Finanzverwaltung, der den
Betrieb nicht kennt, und du behauptest keine Kontonummer als gesichert.

AUFGABE
Prüfe die folgende Kontenliste daraufhin, welche Bezeichnungen und Salden bei
einer Mitübermittlung erklärungsbedürftig wirken, und schlage neutrale
Bezeichnungen vor.

MANDANTENRAHMEN
- Rechtsform: [Einzelunternehmen / GbR / GmbH / UG / GmbH & Co. KG / …]
- Kontenrahmen: [SKR03 / SKR04 / branchenspezifisch]
- Größenklasse: [kleinst / klein / mittelgroß / groß]
- Wirtschaftsjahr: [VON BIS]
- Individuelle Kontenbeschriftungen im Einsatz: [ja / nein / teilweise]
- Besonderheiten: [z. B. Betriebsaufspaltung, Gesellschafterdarlehen,
  mehrere Betriebsstätten]

DATEN
Kontenliste (Kontonummer | Bezeichnung | Saldo | Art als Sach-, Verrechnungs-,
Interims- oder Privatkonto):
[KONTENLISTE EINFÜGEN]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Umfang der Mitübermittlung: Benenne, welche Nachweise mitzuübermitteln sind
   und ab welchem Anwendungszeitpunkt, jeweils mit Rechtsgrundlage und dem
   Zusatz "für [JAHR] verifizieren". Behaupte weder Umfang noch Zeitpunkt als
   feststehend.
2. Bezeichnungen, die interne Annahmen verraten: Wertungen, Schätzvermerke,
   Arbeitsstände, Hinweise auf Streitpunkte, Personennamen, Hinweise auf eine
   noch nicht geklärte steuerliche Behandlung.
3. Bezeichnungen, die erklärungsbedürftig wirken: interne Kürzel, Nummern ohne
   Bedeutung, umgangssprachliche Bezeichnungen, Konten mit widersprüchlicher
   Funktion.
4. Sammel-, Auffang- und Interimskonten: Welche sollten vor der Übermittlung
   aufgelöst, umgebucht oder aufgeteilt werden, welche nur umbenannt? Begründe
   die Unterscheidung.
5. Privat- und Gesellschafterkonten: Prüfe, ob Ausweis und Bezeichnung zur
   Rechtsform passen und was durch die Bezeichnung mehr offengelegt wird als
   nötig.
6. Prüfungsangriffsfläche: Wo entsteht durch die Offenlegung eines Saldos oder
   einer Bezeichnung eine naheliegende Rückfrage? Formuliere je Position die
   Frage, die ein Prüfer stellen würde.
7. Umbenennungsvorschlag: sachlich, neutral, ohne Wertung, ohne Personennamen,
   aus der Bezeichnung heraus verständlich. Behalte die Kontenlogik des
   Kontenrahmens bei.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben.
2. Nenne KEINE Kontonummer als gesichert. Sprich Konten über ihre Bezeichnung
   und Funktion an. Nennst du eine Nummer, setze dahinter "Kontonummer im
   Kontenplan des Mandanten nachschlagen – nicht übernehmen".
3. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen, BMF-Schreiben oder
   Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
4. Kennzeichne Anwendungszeitpunkt, Umfang der Mitübermittlungspflicht,
   Größenklassenmerkmale und alle Betragsgrenzen mit dem Zusatz
   "für [JAHR] verifizieren".
5. Höchstens 20 Positionen. Sortiere nach dem Risiko einer Rückfrage, nicht nach
   Kontonummer, und lasse unauffällige Bezeichnungen weg.
6. Schlage keine Umbuchung vor, die den Bilanzansatz verändert, ohne das
   ausdrücklich als Ansatzfrage zu kennzeichnen. Umbenennen ist keine Umbuchung.
7. Kennzeichne jede Vermutung über den Hintergrund einer Bezeichnung als
   Vermutung.
8. Benenne je Maßnahme, ob sie eine Stammdatenänderung ist und welche
   Anforderungen an Historisierung und Protokollierung dann gelten
   (Fundstelle – für [JAHR] verifizieren).

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Befundtabelle (Rang | Konto nach Bezeichnung | Befund | erwartbare Rückfrage
   | Maßnahme als umbenennen, aufteilen, umbuchen oder klären |
   Umbenennungsvorschlag)
3. Konten mit Handlungsbedarf vor der Übermittlung, getrennt nach
   "vor Übermittlung erledigen" und "im nächsten Wirtschaftsjahr umstellen"
4. Textbaustein für eine Begründung, wenn die vollständige Mitübermittlung im
   Einzelfall nicht möglich ist – als Entwurf, mit Leerstellen für die
   Sachverhaltsangaben und mit Rechtsgrundlage
5. Merkblatt für die Kanzlei: Regeln für die künftige Kontenanlage und
   Kontenbeschriftung, höchstens zehn Punkte, abhakbar mit Kästchen ☐
6. Interne Notiz (was vor der Übermittlung zu entscheiden ist)
7. Was ich nicht sicher weiß
```

## Anwendung

1. Kontenliste exportieren und die Kontenart je Position ergänzen; personenbezogene Bestandteile der Bezeichnungen vorher maskieren.
2. Prompt ausführen; zuerst die Positionen mit Handlungsbedarf vor der Übermittlung abarbeiten.
3. Umbenennungen ausschließlich **mit Gültigkeitsangabe (Historisierung)** in den Stammdaten vornehmen, damit die Bedeutung der bereits gebuchten Bewegungsdaten eindeutig bleibt; Änderung, Zeitpunkt und Bearbeiter protokollieren, die Historie unveränderbar halten. Rückwirkende Änderungen an bereits übermittelten Jahren gesondert prüfen.
4. Merkblatt in die Kontierungs- und Stammdatenkonvention der Kanzlei übernehmen.
5. Übermittlungsprotokoll und Kontennachweise im DMS ablegen.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Übermittlung prüfen: Vollständigkeit der Nachweise, Übereinstimmung der Salden mit dem Abschluss, Wirkung jeder Umbenennung auf die Zuordnung zur Taxonomie.
- **Keine Kontonummer aus der KI-Antwort übernehmen.** Das Modell verwechselt SKR03 und SKR04 und erfindet plausible, aber falsche Nummern.
- Umbenennen ändert nichts am Ansatz. Wo das Modell eine Umbuchung vorschlägt, ist das eine Bilanzierungsfrage und gehört zum Berufsträger.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person liest die Kontennachweise vor der Übermittlung vollständig gegen; die Übermittlung gibt ein Berufsträger frei und dokumentiert die Freigabe (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 5b, § 52 EStG und § 150 AO im amtlichen Volltext (gesetze-im-internet.de), das BMF-Schreiben zur E-Bilanz über die Datenbank des Bundesfinanzministeriums, die gültige Taxonomie über das amtliche Veröffentlichungsportal, die GoBD in der geltenden Fassung, insbesondere die Randziffern zu Stammdatenänderungen und Historisierung, sowie das DATEV Hilfe-Center zur E-Bilanz.

## Varianten

- **Nur Merkblatt:** Zusatz "Beschränke dich auf das Merkblatt für die künftige Kontenanlage." Ergänzt Prompt 25.
- **Mehrere Mandate:** Zusatz "Benenne die Bezeichnungsmuster, die in der Kanzlei wiederkehren."
- **Vorbereitung Betriebsprüfung:** Zusatz "Formuliere je Position eine Antwort auf die erwartbare Rückfrage." Ergänzt Prompt 34.
- **Mandantenkommunikation:** Zusatz "Erzeuge ein kurzes Schreiben, das erklärt, warum Kontenbezeichnungen geändert werden."
