---
name: unrichtiger-steuerausweis-14c
description: Arbeitet eine Liste betroffener Ausgangsrechnungen ab: Sie steuert
  zuerst die Zeiträume mit bereits abgegebener Erklärung aus, bildet aus den
  verbliebenen Belegen Gruppen nach Rechnungstyp, Wortlaut des Steuerausweises
  und Empfängerkategorie, ordnet je Gruppe den Tatbestand zu und leitet
  Berichtigungsweg, Nachweisbedarf und eine abhakbare Arbeitsliste ab. Sie
  rechnet dabei keinen Steuerbetrag, keinen Mehrbetrag und keinen Anteil aus.
  Use when a Steuerkanzlei has to clean up many outgoing invoices with a wrong
  Steuerausweis – after a Steuersatzwechsel, a wrong Steuerbefreiung or a
  Steuerausweis by a Kleinunternehmer – and has to decide between Einzel- und
  Sammelberichtigung.
---

# 87 – § 14c UStG: unrichtiger Steuerausweis erkennen und berichtigen

## Zweck

Die Skill führt den Massenfall: Nach einem Steuersatzwechsel oder einer falsch
angenommenen Befreiung liegen nicht ein Beleg, sondern hunderte gleichartige
Rechnungen vor, verteilt über mehrere Voranmeldungszeiträume mit
unterschiedlichem Erklärungsstand. Sie trennt diese Menge in zwei Schritten,
die der Prompt beschreibt, aber nicht selbst vollzieht: erst nach dem
Erklärungsstand je Zeitraum – wobei die Zeiträume mit dem heiklen Stand
ausgesteuert und nicht weiterbearbeitet werden –, dann nach Rechnungstyp,
Wortlaut des Ausweises und Empfängerkategorie zu Gruppen, die sich gleich
verhalten. Erst danach läuft das Prüfschema, und zwar je Gruppe einmal statt je
Beleg einmal. Das Ergebnis ist eine Arbeitsliste, an der die Kanzlei die
Berichtigung abarbeiten kann, nicht ein Gutachten über einen Einzelfall.

## Wann einsetzen – und wann nicht

**Einsetzen** aus Sicht des **Ausstellers**: Der Mandant hat Rechnungen,
Kleinbetragsrechnungen oder Kassenbelege mit einem Steuerausweis herausgegeben,
der so nicht geschuldet ist, oder er hat als Kleinunternehmer beziehungsweise
ohne zugrunde liegende Leistung Steuer ausgewiesen; ebenso, wenn er einer
Gutschrift des Leistungsempfängers mit gesondertem Steuerausweis nicht
widersprochen hat. Der Zuschnitt der Skill ist die Menge: viele Belege, mehrere
Zeiträume, ein gemischter Empfängerkreis.

**Nicht einsetzen für die Eingangsseite.** Ist der Mandant
Leistungsempfänger und will er eine berichtigte Rechnung anfordern, trägt diese
Skill den Fall nicht; sie fragt durchgehend Angaben des Ausstellers ab –
Wortlaut des eigenen Ausweises, Zusammensetzung des eigenen Empfängerkreises,
Stand der eigenen Voranmeldungen. Prompt 86 ist dafür **kein** Ersatz: Sein
Sachverhaltsbogen verlangt Validierungswerkzeug, Wortlaut der Fehlermeldung,
Regelkennung und Schweregrad, also eine beanstandete E-Rechnung; eine
Papierrechnung mit falschem Steuersatz erzeugt keine solche Meldung. Für die
Eingangsseite gilt die entsprechende Variante am Ende der Prompt-Datei, im
Dialog geführt und ohne diese Skill.

**Nicht einsetzen, um die zutreffende Behandlung zu bestimmen.** Welcher
Steuersatz oder welche Befreiung richtig gewesen wäre, ist Vorfrage und kommt
aus der Kanzlei – für den Einzelfall über Prompt 04, dessen Bogen Beteiligte,
Leistungsart, Leistungsort und Rechnungswortlaut abfragt, für die Zuordnung von
Kombiangeboten in der Gastronomie über Prompt 84. Beide hören auf, bevor ein
Beleg falsch ausgewiesen ist; diese Skill setzt dort an. Ob der Mandant im
fraglichen Zeitraum überhaupt Kleinunternehmer war und wann die Befreiung
weggefallen ist, klärt Prompt 88 – er allein fragt Vorjahresumsatz,
aufgelaufenen Umsatz und den Grenzenvergleich der Kanzlei ab; diese Skill
übernimmt das Ergebnis als Angabe und ermittelt es nicht.

**Nicht einsetzen bei Berichtigungs- oder Strafsachverhalt.** Für Zeiträume, in
denen eine bereits abgegebene Erklärung die geschuldete Steuer nicht enthält,
oder bei Anzeichen für § 153 AO, eine Selbstanzeige, ein Steuerstrafverfahren
oder ein Organisationsversagen der Kanzlei endet die Bearbeitung – siehe
Abbruchregel der Prompt-Datei und Schritt 1 unten.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

**Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts
kommen nicht in das Werkzeug** – auch nicht maskiert, auch nicht in
Ausschnitten, auch nicht als erfundenes Beispiel (Zone Rot in
`DATENSCHUTZ.md`). Die Prompt-Datei nimmt die
Umsatzsteuer-Identifikationsnummer hinzu; auch sie wird vollständig entfernt und
nicht teilmaskiert. Für die Prüfung genügen Rechnungstyp, Wortlaut des
Ausweises, Empfängerkategorie, Zeitraum und Beträge.

Vor der ersten Zeile fordert die Skill die Bestätigung an, dass diese Spalten
aus der Belegliste gelöscht sind und dass Mandant, Firmierungen und Empfänger
nur als Kürzel erscheinen (`Mandant A`, `Kunde Unternehmer 1`,
`Kunde Endverbraucher 1`). Fehlt die Bestätigung oder lautet sie anders als
`bestätigt`, wird keine Zeile bearbeitet.

**Taucht eine solche Angabe während der Bearbeitung auf, wird abgebrochen, nicht
überlesen und nicht stillschweigend bereinigt.** Die Rückmeldung nennt Zeile und
Spalte, erklärt den begonnenen Durchlauf für verworfen und verlangt die Liste
ohne diese Spalte neu; ein Weiterarbeiten „ohne die Nummer" gibt es nicht, denn
die Angabe ist dann bereits im Werkzeug. Dasselbe gilt für Angaben zu
Selbstanzeigen und laufenden Steuerstrafverfahren: Sie sind Zone Rot und gehören
nicht in den Sachverhalt, sondern lösen die Abbruchregel aus.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche
Einbindung des Anbieters nach § 62a StBerG (sorgfältige Auswahl, Vertrag in
Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt
sein – siehe `DATENSCHUTZ.md`.

## Ablauf

1. **Zeiträume nach Erklärungsstand trennen und aussteuern.** Zuerst wird für
   jeden betroffenen Voranmeldungs- und Veranlagungszeitraum der Stand
   abgefragt: keine Erklärung abgegeben / Erklärung abgegeben, die geschuldete
   Steuer enthalten / Erklärung abgegeben, ohne die geschuldete Steuer. Die
   Zeiträume der dritten Gruppe und alle Zeiträume mit Anzeichen nach der
   Abbruchregel der Prompt-Datei werden **namentlich benannt und nicht
   bearbeitet**; für sie gibt die Skill ausschließlich die dort vorgeschriebene
   Rückmeldung aus und trägt weder Tatbestand noch Berichtigungsweg noch
   Anschreiben ein. Die übrigen Zeiträume laufen normal weiter. Fehlt der Stand
   für einen Zeitraum, wird er nachgefordert und nicht unterstellt; ein
   Zeitraum ohne Angabe wird bis zur Klärung wie ausgesteuert behandelt.
2. **Zutreffende Behandlung entgegennehmen.** Die Kanzlei liefert Steuersatz
   oder Befreiung mit Begründung. Die Skill übernimmt diese Angabe, prüft sie
   nur auf Schlüssigkeit und sagt ausdrücklich, wenn sie nicht schlüssig ist.
   Sie ermittelt die zutreffende Behandlung **nicht selbst neu** – fehlt sie,
   hält die Bearbeitung an dieser Stelle an und die Skill benennt die
   Vorfrage.
3. **Belegliste formal prüfen und gruppieren.** Erwartet wird eine Zeile je
   Beleg oder je Belegbündel mit den Feldern des Sachverhaltsbogens der
   Prompt-Datei: Zeitraum, Rechnungstyp, Wortlaut des Steuerausweises,
   ausgewiesener Steuersatz, Steuerbetrag nur dem Grunde nach,
   Empfängerkategorie, Nachweisquelle, Berichtigungsstand, Stand der
   Rückzahlung. Eine fehlende Spalte wird nachgefordert und nicht ergänzt; eine
   Spalte mit Zone-Rot-Inhalt führt zur Zurückweisung. Anschließend bildet die
   Skill Gruppen aus Zeitraum × Rechnungstyp × Wortlaut des Ausweises ×
   Empfängerkategorie und meldet, wie viele Zeilen auf jede Gruppe entfallen.
   Belege ohne gesonderten Steuerausweis scheiden nach dem ersten Prüfschritt
   der Prompt-Datei aus und werden als eigene Gruppe sichtbar geführt, nicht
   weggelassen. Bei sehr großen Beständen mit einem Ausschnitt beginnen – etwa
   einem Zeitraum – und die Gruppenbildung daran erproben.
4. **Je Gruppe den Tatbestand zuordnen.** Jede Gruppe durchläuft die
   Prüfschritte der Prompt-Datei in deren Reihenfolge; Rechtsgrundlagen stehen
   dort und werden hier nicht wiederholt. Absatz 1 und Absatz 2 werden getrennt
   geführt, weil sich die Berichtigungswege unterscheiden; die Varianten des
   unberechtigten Ausweises werden einzeln geprüft, und beim Rechnungstyp
   Gutschrift des Leistungsempfängers ausdrücklich auch der unterbliebene
   Widerspruch. **Keine Zuordnung ohne Feldbezug:** Zu jeder Einstufung wird
   das Feld genannt, aus dem sie folgt. Widersprechen sich die Felder, läuft
   die Gruppe als „Zuordnung offen" weiter und wird nicht weggelassen.
5. **Empfängerkreis als Nachweisfrage führen.** Je Gruppe wird die
   Nachweisquelle festgehalten. Steht dort `Schätzung` oder `keine Quelle`,
   trifft die Skill **keine** Entscheidung über die Entlastung für
   Endverbraucherumsätze, sondern benennt die Nachweismittel, die der Mandant
   beibringen muss, und führt die Gruppe unter „Nachweis offen". Sie rechnet
   keine Anteile aus, bildet keine Summen über Beträge und leitet aus der Zahl
   der Zeilen keinen Anteil am Empfängerkreis ab; die Anteile stammen
   ausschließlich aus der benannten Quelle. Gemischte Empfängerkreise bleiben
   gemischt, bis die Quelle etwas anderes hergibt.
6. **Berichtigungsweg je Gruppe ableiten.** Nach dem Schema der Prompt-Datei:
   Berichtigung gegenüber dem Empfänger, Form und Bezugnahme auf die
   Ursprungsrechnung, Rückzahlung des Mehrbetrags, in den Fällen des Absatzes 2
   die zusätzlichen Schritte, sowie der Zeitraum, in dem die Berichtigung
   wirkt. Jede Voraussetzung wird als offener Punkt mit Nachweisbedarf geführt,
   nicht als erledigt vermerkt: Was nicht belegt ist, ist nicht erfüllt.
   Anschließend die Folge für den Empfänger nach Schritt 8 der Prompt-Datei:
   für den zu hoch ausgewiesenen Mehrbetrag kein Vorsteuerabzug. Sie wird je
   Gruppe festgehalten und ist der Grund, warum unternehmerische Kunden ein
   Anschreiben bekommen – bei Gruppen mit reinem Endverbraucherkreis entfällt
   es, und das wird ausdrücklich vermerkt.
7. **Weichenstellung Einzel- oder Sammelberichtigung stellen.** Je Gruppe
   werden beide Wege mit Voraussetzungen, Aufwand, Nachweisbedarf und Risiko
   gegenübergestellt und ein Weg empfohlen, passend zu Rechnungstyp und
   Empfängerkategorie, mit Begründung. Unterschiedliche Gruppen dürfen
   unterschiedliche Wege bekommen; das ist der eigentliche Ertrag der
   Gruppenbildung.
8. **Ergebnisse erzeugen und ablegen.** Anschreiben an unternehmerische Kunden
   (höchstens 180 Wörter, Sie-Form, ein klarer nächster Schritt), Prüfvermerk
   für die Akte (höchstens 200 Wörter), Prüfliste mit ☐ je Gruppe und Beleg.
   Das Anschreiben wird als versandgesperrt gekennzeichnet, bis die
   Tatbestandszuordnung freigegeben ist. Fristen werden nur dem Grunde nach
   aufgezählt, mit Rechtsgrundlage und dem Zusatz `für [JAHR] verifizieren`,
   ohne Datum und ohne Dauer.

## Ergebnis

Eine Markdown-Datei, Vorschlag:
`<Mandatskürzel>-14c-berichtigung-<JJJJ-MM-TT>.md`.

Inhalt in der Reihenfolge des Ausgabeformats der Prompt-Datei: Einschätzung der
Eindeutigkeit und Datenlage, die Liste der ausgesteuerten Zeiträume mit
Begründung, Prüfprotokoll je Gruppe mit Rechtsgrundlage und Feldbezug, Ergebnis
zur Entstehung der Steuer, Berichtigungsweg mit Voraussetzungen als offenen
Punkten, Weichenstellung Massenfall mit Empfehlung je Gruppe, Fristarten,
Anschreiben, Prüfvermerk, Prüfliste, interne Notiz und der Abschnitt zu dem, was
unsicher geblieben ist. Die Arbeitsliste trägt je Zeile mindestens
`Gruppe | Zeitraum | Rechnungstyp | Empfängerkategorie | Tatbestand |
Berichtigungsweg | Nachweis offen | erledigt`. Nur das Anschreiben verlässt nach
Freigabe die Kanzlei; alles Übrige bleibt in der Akte.

## Qualitätssicherung

Das Ergebnis ist ein Entwurf und kennt nur, was in der Liste stand.

- **Prüfen, ob die ausgesteuerten Zeiträume unbearbeitet geblieben sind.** Für
  sie darf weder eine Tatbestandszuordnung noch ein Berichtigungsweg noch ein
  Anschreiben im Ergebnis stehen. Ihre Bearbeitung gehört zu einem Berufsträger
  außerhalb des KI-Werkzeugs.
- **Die Steuer entsteht kraft Rechnungsausweis.** Solange nicht belegt ist, dass
  der Umsatz an Endverbraucher erbracht wurde, bleibt es bei der Entstehung. Ein
  Ergebnis, das die Entlastung auf einen geschätzten Anteil stützt, ist an
  dieser Stelle falsch.
- **Absatz 1 und Absatz 2 nachlesen, nicht übernehmen.** Eine zweite fachkundige
  Person prüft die Zuordnung stichprobenweise gegen die Belege, insbesondere den
  Gutschriftfall und den Ausweis durch einen Kleinunternehmer.
- **Keine Rückwirkung.** Die Berichtigung wirkt im Besteuerungszeitraum ihrer
  Vornahme; ein rückwirkend geänderter Voranmeldungszeitraum ist ein Fehler.
  Welche Norm den Berichtigungszeitraum trägt, steht in der Prompt-Datei und
  wird dort nachgelesen, nicht aus der Ausgabe übernommen. Zwei Behauptungen
  sind am Ergebnis nachzuprüfen und tragen nicht: dass das Jahressteuergesetz
  2024 den § 14c Abs. 1 UStG geändert habe – neu gefasst wurde Abs. 2 Satz 2 –,
  und dass die Berichtigung einer Rechnung ein rückwirkendes Ereignis im Sinne
  der Abgabenordnung sei; das schließt § 14 Abs. 4 Satz 4 UStG aus, der aber
  eine andere Frage regelt als den Besteuerungszeitraum nach § 14c UStG.
- **Rückzahlung des Mehrbetrags an den Empfänger** ist in den einschlägigen
  Fällen Voraussetzung, nicht Höflichkeit; im Ergebnis muss sie als
  nachzuweisender Punkt stehen, nicht als erledigt.
- **Die Skill rechnet nichts.** Kein Steuerbetrag, kein Mehrbetrag, kein Anteil
  am Empfängerkreis, keine Summe über die Belegliste. Sie **berechnet auch keine
  Frist**: Berichtigungszeitraum, Voranmeldung und Erklärungsabgabe werden nur
  dem Grunde nach mit Rechtsgrundlage benannt; berechnet und im Fristenprogramm
  erfasst werden sie von einem Menschen. Findet sich im Ergebnis eine gerechnete
  Größe, ist sie zu streichen und der Rechenweg an einen Menschen zu geben.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person nimmt
  Tatbestandszuordnung, Empfängernachweis und Berichtigungszeitraum nach. Jedes
  Anschreiben an Kunden und jede Berichtigung gegenüber dem Finanzamt gibt ein
  Berufsträger frei; die Freigabe wird dokumentiert (Freigabestufe 3 in
  `DATENSCHUTZ.md`).
- **Vollständigkeit vor Buchung.** Eine Teilberichtigung erzeugt zwei
  Rechtsstände in derselben Akte: Vor der Umsetzung ist zu prüfen, ob jede Zeile
  der Liste einer Gruppe zugeordnet wurde, einschließlich der Gruppe ohne
  gesonderten Steuerausweis und der Gruppen „Zuordnung offen" und „Nachweis
  offen".
- **Rechtsstand:** Die Skill führt keine eigene Fundstellensammlung; geprüft wird
  an den in der Prompt-Datei genannten Fundstellen. In der Ausgabe steht
  gleichwohl zu jeder rechtlichen Aussage die Rechtsgrundlage mit Absatz und
  Satz und dem Zusatz `für [JAHR] verifizieren`; ist eine Fundstelle unsicher,
  steht dort „Fundstelle offen – bitte recherchieren".

## Grundlage

Rechtsrahmen, Prüfreihenfolge und Ausgabeformat stehen in der Prompt-Datei
[prompts/02-umsatzsteuer/87-14c-unrichtiger-steuerausweis.md](../../../prompts/02-umsatzsteuer/87-14c-unrichtiger-steuerausweis.md);
die Skill folgt ihr und schreibt sie nicht ab.
