---
name: kleinunternehmer-grenzen
description: Führt die Kleinunternehmer-Mandate als fortschreibbare
  Überwachungsliste: Sie geht den Bestand mandatsweise durch, übernimmt je Zeile
  den von der Kanzlei gelieferten Grenzenvergleich, ordnet den Status zu, leitet
  die Folgen des Statuswechsels ab und vergleicht das Ergebnis mit dem
  vorangegangenen Durchlauf. Sie summiert keine Umsätze und vergleicht keinen
  Betrag mit einer Grenze. Use when a Steuerkanzlei has to check after the
  Jahresabschluss or at mid-year which Kleinunternehmer are approaching or have
  exceeded the Grenzen des § 19 UStG and which Mandate have to switch.
---

# 88 – Kleinunternehmer: Grenzen überwachen und Statuswechsel begleiten

## Zweck

Die Skill macht aus einer einmaligen Statusprüfung eine gepflegte
Überwachungsliste. Sie arbeitet den Kleinunternehmer-Bestand Zeile für Zeile
nach dem Prüfschema der Prompt-Datei ab, hält je Mandat fest, aus welcher Angabe
der Status folgt und welche eine Angabe noch fehlt, und stellt den Durchlauf
neben den vorangegangenen: Wer ist seit dem letzten Mal in die Nähe der oberen
Grenze gerückt, wo hat sich der Status gedreht, wo steht die Umstellung noch
offen. Genau darin liegt der Vorteil gegenüber dem Textblock – die Statusfrage
ist je Mandat schnell beantwortet, ihre halbjährliche Wiederholung über
zwanzig oder hundert Mandate hinweg ist es nicht. Die Zahlenarbeit bleibt dabei
außerhalb: Summiert und mit den Grenzen verglichen wird in der Kanzlei, die
Skill übernimmt das Ergebnis dieses Vergleichs als Angabe.

## Wann einsetzen – und wann nicht

**Einsetzen** für den Bestandsdurchlauf nach Abschluss des Vorjahres und zur
Jahresmitte, für die Prognose auf das Folgejahr und für die Begleitung eines
Statuswechsels in beide Richtungen – einschließlich Verzicht und Widerruf,
Umstellung der Rechnungen und Stammdaten und der Frage, ob die unionsweite
Regelung berührt ist.

**Nicht einsetzen für die Umsatzüberwachung selbst.** Die laufenden Umsätze
überwacht die Buchhaltung an einer Auswertung; die Skill bekommt einen
Stichtagsstand und erzeugt den Überwachungsauftrag, sie ersetzt ihn nicht.

**Nicht einsetzen für Rechnungen mit unrichtigem Steuerausweis.** Weist ein
Mandant nach dem Wechsel zur Kleinunternehmerregelung weiterhin Steuer aus, ist
das ein eigener Vorgang; er gehört zu Prompt 87 und der zugehörigen Skill, deren
Bogen Wortlaut des Ausweises, Rechnungstyp, Empfängerkreis und Stand der
Berichtigung abfragt. Diese Skill benennt den Übergabepunkt und arbeitet ihn
nicht aus.

**Nicht einsetzen zur Einordnung eines einzelnen Umsatzes.** Ob ein Vorgang
steuerbar, steuerfrei oder ein Fall des § 13b UStG ist, klärt Prompt 04. Sein
Sachverhaltsbogen nimmt den Kleinunternehmerstatus als gegebene Angabe
(`ja / nein / unbekannt`) entgegen und kennt keine Felder für Vorjahresumsatz,
aufgelaufenen Umsatz oder den Grenzenvergleich – er kann den Status also nicht
bestimmen. Umgekehrt beurteilt diese Skill keinen einzelnen Umsatz.

**Nicht einsetzen für die Wahl bei Gründung.** Der Fragebogen zur steuerlichen
Erfassung mit Tätigkeit, Beginn, Rechtsform, geschätzten Umsätzen der ersten
beiden Jahre und Vollmachten ist Prompt 68; er arbeitet mit Schätzungen vor der
ersten Rechnung und hat kein Feld für einen aufgelaufenen Jahresumsatz. Diese
Skill setzt später an: Sie behandelt das Beurteilungsjahr, auch das der Aufnahme
der Tätigkeit, mit den dann vorliegenden Zahlen.

**Nicht einsetzen bei Berichtigungs- oder Strafsachverhalt.** Wurde die
Kleinunternehmerregelung für einen bereits erklärten Zeitraum zu Unrecht
angewendet oder deuten die Angaben auf § 153 AO, eine Selbstanzeige oder ein
Steuerstrafverfahren hin, endet die Bearbeitung – siehe Abbruchregel der
Prompt-Datei und Schritt 3 unten.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

**Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts
kommen nicht in das Werkzeug** – auch nicht maskiert, auch nicht in
Ausschnitten, auch nicht als erfundenes Beispiel (Zone Rot in
`DATENSCHUTZ.md`). Die Prompt-Datei nimmt die
Umsatzsteuer-Identifikationsnummer und die Kleinunternehmer-Identifikationsnummer
hinzu; beide werden vollständig entfernt und nicht teilmaskiert. Für die Prüfung
genügen Beträge, Zeiträume, Umsatzarten und Status; ob eine
Kleinunternehmer-Identifikationsnummer vorliegt, wird ausschließlich als
`vorhanden ja / nein / unbekannt` geführt.

Mandate erscheinen nur als fortlaufende Kürzel (`M-01`), Kunden nur als
Kategorie. Vor der ersten Zeile fordert die Skill die Bestätigung an, dass alle
Nummernspalten vor dem Einfügen gelöscht wurden; steht dort etwas anderes als
`bestätigt` – auch wenn das Feld leer geblieben ist –, wird keine Zeile
bearbeitet.

**Taucht eine solche Nummer während der Bearbeitung dennoch auf, wird
abgebrochen, nicht überlesen und nicht stillschweigend bereinigt.** Die
Rückmeldung nennt Zeile und Spalte, erklärt den begonnenen Durchlauf für
verworfen und verlangt den Bestand ohne diese Spalte neu. Angaben zu
Selbstanzeigen und laufenden Steuerstrafverfahren sind ebenfalls Zone Rot: Sie
gehören nicht in den Sachverhalt, sondern lösen die Abbruchregel aus. Ein
lückenhafter Bestand ist dagegen **kein** Abbruchgrund – fehlende Angaben sind
der Anlass dieser Auswertung und landen in der Nachforderungsliste.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche
Einbindung des Anbieters nach § 62a StBerG (sorgfältige Auswahl, Vertrag in
Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt
sein – siehe `DATENSCHUTZ.md`.

## Ablauf

1. **Rahmen des Durchlaufs aufnehmen.** Beurteilungsjahr, Stichtag des
   Umsatzstands, Auswertung, aus der die Beträge stammen, verantwortliche Rolle
   in der Kanzlei und – falls vorhanden – die Datei des vorangegangenen
   Durchlaufs. Was fehlt, wird nachgefordert und nicht unterstellt.
2. **Bestandsliste formal prüfen.** Erwartet wird eine Zeile je Mandat mit den
   Feldern des Sachverhaltsbogens der Prompt-Datei: Jahr der Aufnahme der
   Tätigkeit, bisheriger Status, Verzicht und Widerruf mit Datum,
   Vorjahresumsatz mit Herleitung, aufgelaufener Umsatz zum Stichtag, der von
   der Kanzlei bereits summierte voraussichtliche Gesamtumsatz, das Ergebnis
   ihres Grenzenvergleichs, Zusammensetzung der Umsätze, Bezugsgröße,
   Ansässigkeit, Umsätze in anderen Mitgliedstaaten, bisher gestellte
   Rechnungen, Investitionen und Berichtigungsobjekte, Kundenkreis. Eine
   fehlende Spalte wird nachgefordert und nicht ergänzt; eine Spalte mit
   Zone-Rot-Inhalt führt zur Zurückweisung.
3. **Zeilenweise aussteuern.** Zeigt eine Zeile die Anzeichen der Abbruchregel,
   wird sie **nicht bearbeitet**: keine Statuseinschätzung, kein
   Wechselzeitpunkt, kein Mandantentext, nur die dort vorgeschriebene
   Rückmeldung und die Übergabe an einen Berufsträger außerhalb des Werkzeugs.
   Die Aussteuerung wirkt je Mandat; die übrigen Zeilen laufen weiter. Betrifft
   sie mehrere Mandate, steht dieser Befund an erster Stelle der Ergebnisdatei –
   dann ist nicht ein Mandat auffällig, sondern die Überwachung.
4. **Bezugsgröße je Zeile klären.** Steht dort `unklar` oder weicht die
   Bezugsgröße der gelieferten Beträge von der maßgeblichen ab, wird **nicht
   umgerechnet**: Die Zeile läuft als „nicht entscheidbar" weiter, und die Skill
   fordert die Beträge in der richtigen Bezugsgröße an. Welche Bezugsgröße
   maßgeblich ist, steht in der Prompt-Datei als nachzuschlagende Größe und wird
   hier nicht festgelegt.
5. **Den Grenzenvergleich entgegennehmen, nicht anstellen.** Die Skill summiert
   keine Umsätze, rechnet keinen Umsatz hoch und vergleicht keinen Betrag mit
   einer Grenze. Fehlt das Vergleichsergebnis der Kanzlei, entscheidet sie
   nicht, sondern führt die Zeile unter „Vergleich nachzuliefern" und benennt
   die eine Angabe, die die Entscheidung herbeiführt. Das ist der Punkt, an dem
   ein Bestandsdurchlauf erfahrungsgemäß kippt: Ein aus der Liste
   zusammengerechneter Umsatz sieht aus wie ein Ergebnis und ist keines.
6. **Zeile für Zeile durch das Prüfschema.** Jede verbliebene Zeile durchläuft
   die Schritte der Prompt-Datei in deren Reihenfolge – Ansässigkeit und
   Prüfstrang, Bemessungsgröße, untere und obere Grenze, Aufnahme der Tätigkeit
   im Beurteilungsjahr, Verzicht und Widerruf, unionsweite Regelung.
   Rechtsgrundlagen stehen dort und werden hier nicht wiederholt. **Keine
   Statuszuordnung ohne Feldbezug:** Zu jedem Ergebnis wird das Feld genannt,
   aus dem es folgt. Nach der letzten Zeile meldet die Skill, wie viele sie
   bearbeitet, wie viele sie ausgesteuert und wie viele sie als nicht
   entscheidbar geführt hat.
7. **Folgen des Statuswechsels je Richtung ableiten.** Für jede Zeile mit
   Wechsel: was ab dem Wechselzeitpunkt für Rechnungen, Vorsteuerabzug,
   Voranmeldung und Steuerschlüssel gilt, und ob eine Vorsteuerberichtigung
   ausgelöst wird. Die Skill **benennt den Auslöser und rechnet die Berichtigung
   nicht**. Zwei gegenläufige Rechnungsfälle werden dabei je Zeile getrennt
   ausgewiesen und nach Schritt 8 der Prompt-Datei behandelt: Rechnungen, die
   nach dem Wegfall der Befreiung noch ohne Steuerausweis gestellt wurden – kein
   Fall des unrichtigen Steuerausweises, der Umsatz aber steuerpflichtig, mit
   der Folgefrage, ob die Steuer aus dem vereinnahmten Betrag herauszurechnen
   ist; ob die Nachforderung beim Kunden durchsetzbar ist, entscheidet die Skill
   nicht, sondern gibt sie als zivilrechtliche Frage an den Berufsträger, und
   gerechnet wird auch hier nichts. Umgekehrt weiterhin ausgewiesene Steuer nach
   dem Wechsel zur Kleinunternehmerregelung wird als Übergabepunkt an Prompt 87
   vermerkt.
8. **Gegen den vorangegangenen Durchlauf stellen.** Liegt die Vorlaufdatei vor,
   trägt die Skill je Mandat ein, was sich seit dem letzten Durchlauf geändert
   hat: Status, Nähe zur oberen Grenze nach dem gelieferten Vergleich, erledigte
   und offen gebliebene Umstellungspunkte, neu hinzugekommene und weggefallene
   Mandate. Ohne Vorlauf wird der Durchlauf als Erstaufnahme gekennzeichnet.
   Der Vorlauf wird nicht überschrieben; jede Fassung bleibt mit ihrem Datum
   erhalten.
9. **Ergebnisse erzeugen und ablegen.** Mandantenschreiben nur für die Mandate
   mit Wechsel oder absehbarer Überschreitung (höchstens 250 Wörter, Sie-Form,
   ohne Betrag und ohne Frist), Überwachungsauftrag an die Buchhaltung mit
   Bezugsgrößen statt Beträgen, Umstellungsliste mit ☐ je wechselndem Mandat.
   Fristen – Verzicht, Widerruf, Mitteilung bei Überschreitung, Meldung im
   besonderen Verfahren – werden nur dem Grunde nach mit Rechtsgrundlage und dem
   Zusatz `für [JAHR] verifizieren` aufgezählt, ohne Datum und ohne Dauer.

## Ergebnis

Zwei Markdown-Dateien. Für den Bestandsdurchlauf:
`kleinunternehmer-ueberwachung-<JJJJ-MM-TT>.md` – Einschätzung der Datenlage,
ausgesteuerte Zeilen an erster Stelle, Statusliste je Mandat mit Feldbezug und
Gruppe (`Befreiung bleibt` / `Befreiung entfällt ab dem mitgeteilten Zeitpunkt` /
`Befreiung entfällt zum Jahreswechsel` / `nicht entscheidbar`), Spalte
`Änderung seit dem letzten Durchlauf`, Nachforderungsliste je Mandat,
Umstellungsliste mit ☐, Überwachungsauftrag, Fristarten, interne Notiz und der
Abschnitt zu dem, was unsicher geblieben ist.

Für ein einzelnes Mandat mit Wechsel:
`<Mandatskürzel>-kleinunternehmer-status-<JJJJ-MM-TT>.md` mit Prüfprotokoll,
Folgen des Wechsels, Umstellungsliste und dem Mandantenschreiben. Nur das
Mandantenschreiben wird nach Freigabe entnommen; alles Übrige bleibt in der
Kanzlei.

## Qualitätssicherung

Das Ergebnis ist ein Entwurf und kennt nur, was in der Liste stand.

- **Beide Grenzen des § 19 Abs. 1 UStG im Gesetzestext nachlesen**, jedes Jahr
  neu, und ebenso, ob sie netto oder brutto zu verstehen sind. Kein Grenzbetrag,
  kein Schwellenwert und keine Fristdauer aus der Ausgabe übernehmen.
- **Prüfen, dass die Skill nicht gerechnet hat.** Jede Statusaussage muss auf dem
  gelieferten Grenzenvergleich beruhen und das Feld nennen, aus dem sie folgt.
  Eine Zeile, in der eine Summe oder ein Vergleich aus der Liste selbst
  entstanden ist, wird gestrichen und der Kanzlei zur Berechnung zurückgegeben.
- **Die obere Grenze wirkt sofort.** Der Umsatz, der zur Überschreitung führt,
  ist bereits betroffen. Ein Ergebnis, das die Umstellung erst zum Jahreswechsel
  ansetzt, obwohl der Vergleich die Überschreitung im laufenden Jahr ausweist,
  ist falsch.
- **Gesamtumsatz ist nicht gleich Erlöskonto.** Hilfsumsätze, Verkäufe von
  Anlagevermögen und steuerfreie Umsätze beurteilt ein Mensch an der Auswertung;
  die Skill übernimmt die Zusammensetzung, wie sie geliefert wurde.
- **Jahr der Aufnahme der Tätigkeit gesondert nachlesen.** Ob die im
  Beurteilungsjahr geltende Fassung eine Umrechnung des Umsatzes auf einen
  Jahresbetrag vorsieht, entscheidet die Fassung, nicht das Modell; steht im
  Ergebnis eine Hochrechnung, ist sie gegen die Fassung zu prüfen, bevor
  irgendetwas umgestellt wird.
- **§ 15a UStG immer mitprüfen.** Der Statuswechsel ist der klassische Auslöser
  in beide Richtungen; die Berichtigung selbst wird außerhalb gerechnet, und
  ihre Höhe darf im Ergebnis nicht stehen.
- **Die unionsweite Regelung ist ein eigenes Verfahren** mit eigener
  Registrierung, eigener Zuständigkeit und eigenen Meldepflichten; sie wird
  nicht nebenbei miterledigt und nicht mit dem Prüfstrang für im übrigen
  Gemeinschaftsgebiet ansässige Unternehmer vermengt.
- **Die Skill berechnet keine Frist.** Verzicht, Widerruf, Mitteilung bei
  Überschreitung und die Meldungen im besonderen Verfahren stehen nur dem Grunde
  nach mit Rechtsgrundlage; berechnet und im Fristenprogramm erfasst werden sie
  von einem Menschen.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person nimmt
  Bemessungsgröße, Grenzenvergleich und Wechselzeitpunkt stichprobenweise nach.
  Mandantenschreiben, Verzicht und Widerruf gibt ein Berufsträger frei; die
  Freigabe wird dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fortschreibung prüfen.** Vor dem nächsten Durchlauf ist zu prüfen, ob die
  offenen Punkte des letzten übernommen wurden; eine Überwachungsliste, die bei
  jedem Lauf bei null beginnt, überwacht nichts.
- **Rechtsstand:** Die Skill führt keine eigene Fundstellensammlung; geprüft wird
  an den in der Prompt-Datei genannten Fundstellen. In der Ausgabe steht
  gleichwohl zu jeder rechtlichen Aussage die Rechtsgrundlage mit Absatz und
  Satz und dem Zusatz `für [JAHR] verifizieren`; ist eine Fundstelle unsicher,
  steht dort „Fundstelle offen – bitte recherchieren".

## Grundlage

Rechtsrahmen, Prüfreihenfolge und Ausgabeformat stehen in der Prompt-Datei
[prompts/02-umsatzsteuer/88-kleinunternehmer-grenzen.md](../../../prompts/02-umsatzsteuer/88-kleinunternehmer-grenzen.md);
die Skill folgt ihr und schreibt sie nicht ab.
