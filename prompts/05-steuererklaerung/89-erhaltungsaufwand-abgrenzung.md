# 89 – Erhaltungsaufwand oder anschaffungsnahe Herstellungskosten

**Problem:** Der Mandant kauft eine Immobilie und saniert sofort, die Kanzlei bucht Erhaltungsaufwand, die Betriebsprüfung qualifiziert um – und die Umqualifizierung wirkt über die gesamte Abschreibungsdauer.
**Rolle:** Sachbearbeiter Steuern, Fachassistent, Berufsträger
**DATEV-Bezug:** DATEV Einkommensteuer (Anlage V), DATEV Anlagenbuchführung (Gebäude, Bemessungsgrundlage der Abschreibung), DATEV Kanzlei-Rechnungswesen (Aufwandskonten), DATEV DMS oder DATEV Meine Steuern (Kaufvertrag, Kaufpreisaufteilung, Handwerkerrechnungen)
**Was du bereitstellen musst:** Kaufvertrag mit Übergang von Besitz, Nutzen und Lasten; bei unentgeltlichem oder teilentgeltlichem Erwerb zusätzlich Erwerbsvorgang und Erwerbszeitpunkt des Rechtsvorgängers; Kaufpreisaufteilung auf Grund und Boden, Gebäude und bewegliche Wirtschaftsgüter mit Herleitung; Zustand des Gebäudes bei Erwerb und Nutzung vor und nach der Maßnahme; Zahl der Wohnungen im Gebäude und Angabe, ob der Standard nur einzelner Wohnungen gehoben wird; sämtliche Rechnungen der Maßnahmen mit Datum, Nettobetrag und Leistungsbeschreibung; Angaben zur Ausstattung in den Bereichen Heizung, Sanitär, Elektro und Fenster vor und nach der Maßnahme; Stand der Bescheide der betroffenen Jahre.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift des Objekts, Namen der Handwerksbetriebe und Voreigentümer durch Platzhalter ersetzen (`Mandant A`, `Objekt 1`, `Handwerker 1`); die Lage nur als Kategorie. Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts und Grundbuchangaben nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Für die Abgrenzung genügen Leistungsbeschreibung, Nettobeträge, Zeitpunkte und Zustandsangaben. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Sachbearbeiter Steuern in einer deutschen Steuerkanzlei und grenzt
Erhaltungsaufwand von Anschaffungs- und Herstellungskosten ab. Du ordnest
jede Rechnungsposition einzeln zu und begründest jede Zuordnung aus einer
Norm, nicht aus dem Gesamteindruck der Maßnahme.

WAS DU NICHT TUST
Du bildest KEINE Summen, berechnest KEINE Prozentgrenze und stellst KEIN
Verhältnis zu den Anschaffungskosten her. Du lieferst die Zuordnung je
Position und die Bezugsgrößen; gerechnet wird außerhalb dieses Prompts.

ARBEITSGRUNDLAGE
Maßgeblich sind § 255 Abs. 1 und Abs. 2 HGB, § 6 Abs. 1 Nr. 1a EStG und das
BMF-Schreiben vom 26.01.2026, GZ IV C 1 - S 2253/00082/001/064. Dieses
Schreiben ersetzt die Schreiben vom 18.07.2003 und 20.10.2017 und ist in
allen offenen Fällen anzuwenden (Fundstelle – für [JAHR] verifizieren).
Zwei Klarstellungen, an die du dich zu halten hast:
- Das Schreiben ordnet KEINE bestimmte Prüfungsreihenfolge an. Die
  Reihenfolge unten ist eine Arbeitsreihenfolge der Kanzlei. Behaupte nicht,
  sie sei vorgeschrieben.
- Das Schreiben enthält KEINE Vereinfachungsregelung mit einer Betragsgrenze
  je Baumaßnahme. Nenne keine solche Grenze, auch nicht als Faustregel.
Nenne die Prozentgrenze und die Frist des § 6 Abs. 1 Nr. 1a EStG nicht als
Zahl, sondern als nachzuschlagende Größe mit dem Zusatz
"für [JAHR] verifizieren".

AUFGABE
Ordne die einzelnen Aufwendungen zu, benenne die Bezugsgrößen für die
Prüfung des § 6 Abs. 1 Nr. 1a EStG und leite die verfahrensrechtlichen Folgen
ab.

SACHVERHALT
- Veranlagungszeitraum und betroffene Jahre: [ZEITRAUM]
- Erwerb: entgeltlich [ja / nein / teilweise], Übergang von Besitz, Nutzen
  und Lasten am [DATUM]
- Bei unentgeltlichem oder teilentgeltlichem Erwerb: Erwerbsart und Übergang
  von Besitz, Nutzen und Lasten beim Rechtsvorgänger: [ANGABE]
- Anschaffungskosten des Gebäudes: [BETRAG], Anschaffungskosten Grund und
  Boden: [BETRAG], Herleitung der Aufteilung: [ANGABE]
- Mitangeschaffte bewegliche Wirtschaftsgüter: [ANGABE oder "keine"]
- Nutzung: [Vermietung / Betriebsvermögen / teilweise selbst genutzt],
  Nutzungsanteil: [ANTEIL]
- Zustand bei Erwerb: [bezugsfertig und vermietet / leer stehend /
  unbewohnbar / teilweise funktionsuntüchtig], Beschreibung: [ANGABE]
- Funktionsuntüchtige Teile bei Erwerb: [ANGABE oder "keine"]
- Bei Erwerb erkennbare Mängel: [ANGABE], verdeckte Mängel: [ANGABE]
- Zweckbestimmung des Erwerbers, Nutzung vor und nach der Maßnahme:
  [ANGABE]
- Maßnahmen als Einzelpositionen, je mit Rechnungsdatum, Nettobetrag und
  Leistungsbeschreibung: [AUFSTELLUNG]
- Ausstattung vor und nach der Maßnahme in den Bereichen Heizung, Sanitär,
  Elektro, Fenster: [ANGABE je Bereich]
- Erweiterung der nutzbaren Fläche oder Substanzmehrung: [nein / ja,
  Beschreibung]
- Zahl der Wohnungen im Gebäude: [ANZAHL], Standardhebung nur bei einzelnen
  Wohnungen: [nein / ja, welche / unklar]
- Jährlich üblicherweise anfallende Erhaltungsarbeiten darunter: [ANGABE]
- Geplante weitere Maßnahmen und deren Zeitpunkt: [ANGABE]
- Stand der Bescheide der betroffenen Jahre: [ANGABE zu Vorbehalt der
  Nachprüfung, Vorläufigkeit, Bestandskraft]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Ist das Gebäude entgeltlich angeschafft worden, und wann ging es über?
   Bei unentgeltlichem Erwerb tritt der Rechtsnachfolger in den maßgeblichen
   Zeitraum des Rechtsvorgängers ein, bei teilentgeltlichem Erwerb nur im
   Verhältnis zum unentgeltlichen Teil; § 6 Abs. 1 Nr. 1a EStG ist dann
   anhand der Anschaffung des Rechtsvorgängers zu prüfen (Randziffer 59 und
   64 des BMF-Schreibens vom 26.01.2026 – für [JAHR] verifizieren). Benenne
   bei teilentgeltlichem Erwerb ausdrücklich, welcher Teil betroffen ist, und
   fordere die Angaben zum Erwerb des Rechtsvorgängers an, wenn sie fehlen.
2. Anschaffungskosten nach § 255 Abs. 1 HGB: Welche Aufwendungen dienen
   dazu, das Gebäude in einen betriebsbereiten Zustand zu versetzen? Prüfe
   einzeln: Betriebsbereitschaft nach der Zweckbestimmung des Erwerbers,
   Beseitigung der Funktionsuntüchtigkeit tragender Teile, Beseitigung bei
   Erwerb erkennbarer Mängel, Behandlung verdeckter Mängel, Anschaffungs-
   nebenkosten. Sage zu jeder Position, warum sie hierunter fällt oder nicht.
3. Herstellungskosten nach § 255 Abs. 2 HGB: Prüfe getrennt
   a) Erweiterung, insbesondere Substanzmehrung, Vergrößerung der nutzbaren
      Fläche und Ergänzung um bisher nicht vorhandene Bestandteile,
   b) Änderung der Funktion oder der Nutzung des Gebäudes,
   c) wesentliche Verbesserung über den ursprünglichen Zustand hinaus,
      insbesondere die Hebung des Standards in den Kernbereichen Heizung,
      Sanitär, Elektro und Fenster. Benenne, in wie vielen Bereichen eine
      Hebung vorliegen muss und woran sie sich bemisst, mit Fundstelle im
      BMF-Schreiben vom 26.01.2026 einschließlich Randziffer; nenne die Zahl
      der Bereiche nur als nachzuschlagende Größe
      (Zahl der Bereiche – für [JAHR] verifizieren),
   d) Sanierung in Raten: Sind die gelieferten und die geplanten Maßnahmen
      Teil einer planmäßigen Gesamtmaßnahme, die sich in zeitlichem
      Zusammenhang über mehrere Jahre erstreckt und insgesamt zu einer
      deutlichen Erhöhung des Gebrauchswerts führt? Benenne die Merkmale, den
      Betrachtungszeitraum als nachzuschlagende Größe
      (Zeitraum – für [JAHR] verifizieren) und die Fundstelle (Randziffern 51
      bis 53 des BMF-Schreibens vom 26.01.2026). Ergebnis:
      [liegt vor / liegt nicht vor / nicht entscheidbar].
   Prüfe die Standardhebung in Schritt 3 unabhängig von jeder Betragsgrenze.
   Ob die Vereinfachung der Randziffer 77 des BMF-Schreibens vom 26.01.2026
   eingreift, ist erst nach dem Verhältnisvergleich zu entscheiden, den ein
   Mensch außerhalb dieses Prompts bildet. Weise dazu nur aus:
   "Standardhebung geprüft; ob Randziffer 77 die Prüfung entbehrlich macht,
   hängt vom Verhältnisvergleich ab – von einem Menschen zu bilden"
   (Randziffer und Prozentgrenze – für [JAHR] verifizieren).
4. Erst wenn die Schritte 2 und 3 zu keiner Zuordnung führen, prüfe
   § 6 Abs. 1 Nr. 1a EStG als eigenständigen Tatbestand. Benenne dabei
   ausdrücklich und je mit Rechtsgrundlage:
   a) den maßgeblichen Zeitraum ab der Anschaffung
      (Frist – für [JAHR] verifizieren),
   b) die Bezugsgröße, nämlich die Anschaffungskosten des Gebäudes ohne
      Grund und Boden und ohne bewegliche Wirtschaftsgüter,
   c) die Prozentgrenze (Grenze – für [JAHR] verifizieren) sowie die
      Randziffern 66 bis 68 des BMF-Schreibens vom 26.01.2026 als Fundstelle,
   d) dass die Aufwendungen ohne Umsatzsteuer anzusetzen sind,
   e) die Ausnahmen des Satzes 2, nämlich Aufwendungen für Erweiterungen und
      Erhaltungsarbeiten, die jährlich üblicherweise anfallen, je mit
      Abgrenzungskriterium,
   f) die Behandlung von Aufwendungen, die bereits nach Schritt 2 oder 3
      zuzuordnen sind: Sie fallen nicht zusätzlich unter diese Vorschrift,
      sind aber für die Betragsgrenze zu beachten, soweit die Vorschrift das
      vorsieht. Sage ausdrücklich, wenn du das nicht sicher weißt.
   g) Ergänze die Regelung in Randziffer 77 des Schreibens vollständig,
      einschließlich ihres zweiten Satzes: Die Prüfung der Standardhebung
      unterbleibt für den maßgeblichen Zeitraum nach der Anschaffung nur,
      wenn die Aufwendungen ohne Umsatzsteuer die Prozentgrenze nicht
      übersteigen; sie unterbleibt NICHT, wenn sich bei einem Gebäude mit
      mehreren Wohnungen der Standard einzelner Wohnungen hebt oder die
      Maßnahme der Beginn einer Sanierung in Raten sein kann. Prüfe beide
      Rückausnahmen ausdrücklich und sage, wenn die dafür nötigen Angaben
      fehlen (Randziffer und Prozentgrenze – für [JAHR] verifizieren).
5. Sonderfragen, je mit eigener Begründung und eigener Fundstelle:
   Aufteilung einer einheitlichen Baumaßnahme über mehrere Jahre; mehrere
   selbständige Gebäudeteile und ihre gesonderte Betrachtung; teilweise
   selbst genutzte oder unentgeltlich überlassene Flächen; Miteigentum;
   Eigenleistungen; Zuschüsse und Versicherungsleistungen; Abbruch- und
   Entsorgungskosten. Lasse weg, was nach dem Sachverhalt nicht einschlägig
   ist.
6. Verfahrensrechtliche Folge: Stellt sich nachträglich heraus, dass die
   Grenze über- oder unterschritten wurde, ist das ein rückwirkendes Ereignis
   nach § 175 Abs. 1 Satz 1 Nr. 2 AO. Benenne, welche Bescheide der
   betroffenen Jahre davon berührt sind, welche Bedeutung Vorbehalt der
   Nachprüfung und Vorläufigkeit haben, und was das für die Behandlung im
   Erstjahr bedeutet, solange die Maßnahmen noch laufen.
   Benenne zusätzlich die Folge für die Abschreibung dem Grunde nach: Welche
   Aufwendungen erhöhen oder vermindern die Bemessungsgrundlage der
   Gebäudeabschreibung, und ab welchem Zeitpunkt des jeweiligen Jahres
   geschieht das (Randziffer 68 des BMF-Schreibens vom 26.01.2026 und
   R 7.4 Abs. 9 Satz 3 EStR – für [JAHR] verifizieren). Rechne keine
   Bemessungsgrundlage und keinen Abschreibungsbetrag aus.
7. Zuordnungstabelle: Ordne JEDE gelieferte Position zu. Spalten:
   Nr. | Datum | Nettobetrag | Zuordnung | tragendes Kriterium |
   Rechtsgrundlage | Sicherheit der Zuordnung.
   Zulässige Werte in der Spalte Zuordnung: Anschaffungskosten,
   Herstellungskosten, Erhaltungsaufwand, in die Prüfung nach
   § 6 Abs. 1 Nr. 1a EStG einzubeziehen, nicht zuordenbar.
   Zulässige Werte in der Spalte Sicherheit: [sicher / vertretbar / unklar].
   Bilde KEINE Summen.

WEITERE ERGEBNISSE
8. Rückfrageliste an den Mandanten für alle Positionen, deren
   Leistungsbeschreibung für die Zuordnung nicht ausreicht, als Tabelle mit
   den Spalten Nr. | Position | Unsere Frage | Antwort des Mandanten (leer).
9. Mandantenschreiben, höchstens 250 Wörter, Sie-Form, Fachbegriffe in einem
   Halbsatz erklärt, ohne Betrag und ohne Frist: warum die Zuordnung zählt,
   welche Unterlagen fehlen, was bis wann noch beeinflussbar ist.
10. Prüfvermerk für die Akte, höchstens 200 Wörter: Unterlagenlage,
    Zuordnungsergebnis, offene Punkte, Empfehlung für die Veranlagung.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Reicht eine Leistungsbeschreibung nicht aus, ordne NICHT zu,
   sondern nimm die Position in die Rückfrageliste.
2. Nenne KEINE Prozentgrenze, KEINE Fristlänge und KEINE Betragsgrenze als
   Zahl. Jede dieser Größen nur als nachzuschlagende Angabe mit dem Zusatz
   "für [JAHR] verifizieren".
3. Erfinde keine Vereinfachungsregelung und keine Bagatellgrenze je
   Baumaßnahme. Gibt es zu einer Frage keine Regelung, sage das.
4. Nenne zu jeder Zuordnung die Rechtsgrundlage POSITIV, also Norm mit
   Absatz und Satz, BMF-Schreiben mit Datum und Randziffer oder Entscheidung
   mit Datum und Aktenzeichen, jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Aktenzeichen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
5. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Zeiträume im Raum
   stehen, je mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren",
   ohne Datum und ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen
   zu berechnen und im Fristenprogramm zu erfassen."
6. Formuliere jede Aussage über den baulichen Zustand, die nicht aus den
   Angaben folgt, ausdrücklich als Vermutung.
7. Weise gesondert aus, welche Abgrenzungsfragen streitig sind oder von der
   Verwaltungsauffassung abweichend beurteilt werden könnten.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Prüfprotokoll, Schritte 1 bis 6, je mit Rechtsgrundlage
3. Zuordnungstabelle
4. Bezugsgrößen für die Prüfung nach § 6 Abs. 1 Nr. 1a EStG, nicht gerechnet
5. Verfahrensrechtliche Folgen
6. Folge für die Bemessungsgrundlage der Abschreibung, nicht gerechnet
7. Fristarten mit Rechtsgrundlage
8. Rückfrageliste
9. Mandantenschreiben
10. Prüfvermerk
11. Interne Notiz
12. Was ich nicht sicher weiß
```

## Anwendung

1. Vor dem Prompt die Kaufpreisaufteilung klären und belegen; ohne die Anschaffungskosten des Gebäudes fehlt die Bezugsgröße und die gesamte Prüfung hängt in der Luft.
2. Rechnungen einzeln mit Datum, Nettobetrag und Leistungsbeschreibung erfassen. Sammelpositionen wie „Sanierung Bad" reichen nicht; sie landen in der Rückfrageliste.
3. Den Prompt beim ERSTEN Sanierungsjahr einsetzen, nicht erst bei der Betriebsprüfung – solange Maßnahmen laufen, ist die Zuordnung noch beeinflussbar.
4. Ergebnis in DATEV Anlagenbuchführung umsetzen und die Zuordnung je Position im Prüfvermerk dokumentieren; die Betriebsprüfung fragt nach der Begründung, nicht nach dem Ergebnis.
5. Solange der maßgebliche Zeitraum läuft, Wiedervorlage setzen und den Bescheidstatus der betroffenen Jahre überwachen.

## Qualitätssicherung

- **Das BMF-Schreiben vom 26.01.2026 im Volltext lesen.** Es ersetzt die Schreiben vom 18.07.2003 und 20.10.2017 und ist in allen offenen Fällen anzuwenden; Vorlagen und Merkblätter mit dem alten Stand sind auszusortieren.
- **Keine Vereinfachungsregelung mit Betragsgrenze je Baumaßnahme.** Eine solche Regelung enthält das Schreiben nicht. Taucht sie in einer KI-Antwort oder in einer Sekundärquelle auf, ist die Aussage zu streichen.
- **Keine vorgeschriebene Prüfungsreihenfolge.** Die Reihenfolge im Prompt ist eine Arbeitsreihenfolge; sie ersetzt nicht die Prüfung jedes Tatbestands.
- **Prozentgrenze und maßgeblichen Zeitraum im Gesetzestext nachlesen** (Grenze und Zeitraum – für [JAHR] verifizieren), ebenso die Frage, welche Aufwendungen in die Bezugsgröße einzubeziehen sind. Kein Wert aus der KI-Antwort.
- **Randziffer 77 nur mit ihrem zweiten Satz anwenden.** Die Vereinfachung gilt nicht, wenn sich bei einem Gebäude mit mehreren Wohnungen der Standard einzelner Wohnungen hebt oder die Maßnahme der Beginn einer Sanierung in Raten sein kann. Fehlt einer der beiden Punkte in der KI-Antwort, ist die Aussage unvollständig.
- **Beim unentgeltlichen Erwerb zählt der Rechtsvorgänger.** Der Rechtsnachfolger tritt in den maßgeblichen Zeitraum des Rechtsvorgängers ein, beim teilentgeltlichen Erwerb nur anteilig; ohne dessen Erwerbsdatum ist die Prüfung nicht abschließbar.
- **Die Folge für die Bemessungsgrundlage der Abschreibung gehört in den Prüfvermerk.** Sie ist der eigentliche Dauerschaden einer Umqualifizierung und wird außerhalb des Prompts gerechnet.
- **Die Grenze rechnet ein Mensch.** Der Prompt liefert die Zuordnung je Position; Summe und Verhältnis werden außerhalb gebildet und nachgerechnet.
- **Rückwirkendes Ereignis mitdenken.** Über- oder Unterschreiten der Grenze wirkt nach § 175 Abs. 1 Satz 1 Nr. 2 AO auf die Bescheide der betroffenen Jahre zurück; die Verfahrenslage gehört in den Prüfvermerk.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Kaufpreisaufteilung, Zuordnung der Einzelpositionen und die Bezugsgröße nach. Mandantenschreiben und die Behandlung in der Erklärung gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 6 Abs. 1 Nr. 1a EStG, § 255 HGB und § 175 AO im amtlichen Volltext (gesetze-im-internet.de), dem BMF-Schreiben vom 26.01.2026 (GZ IV C 1 - S 2253/00082/001/064) im Volltext, der Entscheidung des Bundesfinanzhofs vom 14.06.2016 – IX R 22/15 sowie DATEV LEXinform.

## Varianten

- **Vor der Sanierung:** „Beurteile die geplanten Maßnahmen vorab, benenne je Maßnahme die voraussichtliche Zuordnung und die Angaben, die für eine sichere Zuordnung fehlen."
- **Standardhebung:** „Vertiefe Schritt 3 Buchstabe c und stelle die Ausstattung in den vier Kernbereichen vor und nach der Maßnahme gegenüber."
- **Betriebsprüfung:** „Stelle der Zuordnung der Kanzlei die abweichende Auffassung der Prüfung gegenüber und benenne je Position das tragende Argument beider Seiten."
- **Mehrere Objekte:** „Bearbeite jedes Objekt in einer eigenen Tabelle und benenne, welche Positionen objektübergreifend zugeordnet werden müssen."
- **Sanierung in Raten:** „Vertiefe Schritt 3 Buchstabe d, stelle die Maßnahmen der einzelnen Jahre und die geplanten Maßnahmen als eine Gesamtmaßnahme dar und benenne die Merkmale, die für und gegen einen planmäßigen Zusammenhang sprechen."
- **Aus dem Anlagenbestand heraus:** „Beschränke dich auf die Positionen der Reparatur- und Instandhaltungskonten und ordne sie einzeln zu." Ergänzt Prompt 52; die dortige Gebäude-Variante ersetzt diesen Prompt nicht, sondern verweist auf ihn.
