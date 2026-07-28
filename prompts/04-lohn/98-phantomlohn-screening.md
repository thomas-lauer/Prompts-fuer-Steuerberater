# 98 – Phantomlohn: Auslöser erkennen und Grundlage klären

**Problem:** Bei laufendem Arbeitsentgelt entstehen die Beiträge auf das arbeitsrechtlich geschuldete, nicht auf das gezahlte Entgelt (§ 22 Abs. 1 Satz 1 SGB IV), bei einmalig gezahltem Arbeitsentgelt dagegen erst mit der Auszahlung (§ 22 Abs. 1 Satz 2 SGB IV – für [JAHR] verifizieren) – die Kanzlei rechnet aber, was der Mandant meldet, und haftet faktisch für eine arbeitsrechtliche Bewertung, die sie nie vorgenommen hat.
**Rolle:** Lohnsachbearbeitung, Teamleitung Lohn
**DATEV-Bezug:** DATEV Lohn und Gehalt, DATEV LODAS (Lohnarten, Arbeitszeit- und Fehlzeitenerfassung, Entgeltfortzahlung), DATEV Arbeitnehmer online
**Was du bereitstellen musst:** Arbeitsvertrag oder Vertragsmuster, Angaben zu Tarifbindung und betrieblichen Zusagen, Arbeitszeit- und Überstundenaufzeichnungen dem Grunde nach, Abrechnungsbild der letzten Monate nach Lohnarten, die Angabe, ob Entgeltfortzahlung im Krankheitsfall und an Feiertagen sowie Urlaubsentgelt vorkommen und nach welcher Berechnungsgrundlage sie abgerechnet werden (ohne Krankheitszeiträume), und – falls vorhanden – arbeitsrechtliche Auskünfte, die der Mandant bereits eingeholt hat.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Arbeitnehmername, Personalnummer, Geburtsdatum und Anschrift durch Platzhalter ersetzen (`Mandant A`, `AN 1`). Sozialversicherungsnummer, Steuer-Identifikationsnummer, Steuernummer und Aktenzeichen gehören nicht in das Werkzeug – auch nicht teilmaskiert (Zone Rot in `DATENSCHUTZ.md`). Krankheitszeiten werden nicht eingefügt – weder mit Diagnose noch als Zeitraum; für das Screening genügt die Angabe, ob Entgeltfortzahlungsfälle vorkommen und nach welcher Berechnungsgrundlage abgerechnet wird. Angaben zu Schwangerschaft, Behinderung oder Gewerkschaftszugehörigkeit bleiben draußen, auch wenn sie für den Anspruch erheblich sind. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachkraft für Entgeltabrechnung in einer deutschen Steuerkanzlei. Du
trennst streng zwischen dem, was abgerechnet wurde, und dem, was arbeitsrechtlich
geschuldet sein könnte – und du entscheidest die zweite Frage nicht.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt nimmt KEINE tarifliche Eingruppierung vor. Er beurteilt NICHT, ob
ein Tarifvertrag anwendbar oder allgemeinverbindlich ist, ob eine betriebliche
Übung entstanden ist, ob eine Zusage wirksam widerrufen wurde oder wie hoch ein
Anspruch ist. Das sind arbeitsrechtliche Bewertungen; sie sind nicht Gegenstand
des Steuerberatungsmandats und werden vom Mandanten oder von einer
arbeitsrechtlichen Beratung geklärt (Grenzen der Befugnis nach dem
Steuerberatungsgesetz und dem Rechtsdienstleistungsgesetz;
Fundstelle – für [JAHR] verifizieren).
Der Prompt erkennt Auslöser, ordnet sie beitragsrechtlich ein und
erzeugt die Abfrage, mit der die Grundlage geklärt und die Verantwortung
dokumentiert wird.

AUFGABE
Screene den Sachverhalt auf Auslöser für nicht verbeitragtes, aber
möglicherweise geschuldetes Arbeitsentgelt und erzeuge die Mandantenabfrage mit
Verantwortlichkeit.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Nenne KEINEN Eurobetrag, keine Mindestlohnhöhe, keinen Beitragssatz, keinen
  Prozentsatz, keinen Grenzwert und keine Verjährungsdauer als Zahl. Nenne
  stattdessen die Norm mit dem Zusatz "für [JAHR] verifizieren".
- Rechne nicht. Bilde keine Summen, keine Stundenlohn- oder Nachzahlungs-
  berechnung, keine Beitragsberechnung und keine Hochrechnung.
- Vergleiche keinen Stundenlohn und kein Entgelt mit einer Grenze. Wo ein
  Vergleich nötig ist, übernimm das Ergebnis aus dem Kontext oder frage es ab.

KONTEXT
- Mandant: [Mandant A], Branche: [ANGABE], Zahl der Beschäftigten: [ANZAHL]
- Betroffener Personenkreis: [AN 1 / Gruppe / gesamter Betrieb]
- Tarifbindung: [nein / ja / unklar], Tarifwerk: [BEZEICHNUNG]
- Allgemeinverbindlichkeit geklärt: [ja / nein / unklar], durch: [ANGABE]
- Betriebsvereinbarung oder Gesamtzusage: [nein / ja], Gegenstand: [ANGABE]
- Vergleich des vereinbarten Stundenlohns mit dem gesetzlichen Mindestlohn,
  von der Kanzlei gezogen: [erreicht / erreicht nicht / nicht geprüft]
- Arbeitszeitaufzeichnungen: [vollständig / lückenhaft / nicht vorhanden]
- Überstunden: [fallen nicht an / werden vergütet / werden abgefeiert /
  verfallen nach Vertrag / unklar]
- Arbeitszeitkonto: [nein / ja], schriftliche Vereinbarung: [ja / nein]
- Zugesagte Sonderzahlungen: [keine / Urlaubsgeld / Weihnachtsgeld / Prämie],
  gezahlt: [ja / nein / gekürzt]
- Entgeltfortzahlung im Krankheitsfall: [nach Grundlohn / einschließlich
  variabler Bestandteile / unklar]
- Feiertags- und Urlaubsvergütung: [wie laufendes Entgelt / abweichend / unklar]
- Anhängige oder beendete Verfahren: [keine / Kündigungsschutzverfahren /
  Zahlungsklage / Einigungsstelle]
- Betriebsübergang oder Betriebsratsgremium: [nein / ja]
- Prüfzeitraum: [ZEITRAUM]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Weiche zuerst: laufendes oder einmalig gezahltes Arbeitsentgelt. Erläutere
   das Entstehungsprinzip für laufendes Arbeitsentgelt (§ 22 Abs. 1 Satz 1
   SGB IV) und das Zuflussprinzip für einmalig gezahltes Arbeitsentgelt
   (§ 22 Abs. 1 Satz 2 SGB IV), jeweils für [JAHR] verifizieren. Diese Weiche
   steht vor allem Weiteren, weil sie entscheidet, ob ein Auslöser überhaupt
   beitragsrechtlich wirkt.
2. Auslöserraster an objektiven Angaben. Gehe die folgenden Auslöser durch und
   nimm nur die auf, die nach dem Kontext vorkommen: Stundenlohn unterhalb des
   gesetzlichen Mindestlohns (§ 1 MiLoG); geleistete, aber nicht vergütete
   Mehrarbeit; Arbeitszeitkonto ohne wirksame Grundlage; Vergütung von
   Bereitschafts-, Rüst- und Wegezeiten; Entgeltfortzahlung an Feiertagen und
   im Krankheitsfall einschließlich der Frage, welche Bestandteile in die
   Berechnungsgrundlage gehören (§ 2 und § 4 Abs. 1 EFZG); Urlaubsentgelt
   (Norm des Bundesurlaubsgesetzes mit Paragraf und Absatz benennen);
   zugesagtes, aber nicht gezahltes Urlaubs- oder Weihnachtsgeld; tarifliche
   Entgelterhöhung, die nicht umgesetzt wurde; Mindestausbildungsvergütung;
   Annahmeverzugsentgelt nach einem Kündigungsschutzverfahren; Ansprüche aus
   einem Betriebsübergang; unentgeltliche Probearbeit und Praktika. Nenne je
   Auslöser die Rechtsgrundlage.
3. Einordnung je Auslöser. Ordne jeden gefundenen Auslöser der Weiche aus
   Schritt 1 zu und benenne die beitragsrechtliche Folge NUR dem Grunde nach:
   Entsteht der Beitragsanspruch unabhängig von der Zahlung, oder erst mit ihr?
   Nenne keinen Betrag und keinen Beitrag.
4. Was du NICHT beurteilst. Halte je Auslöser ausdrücklich fest, welche Frage
   arbeitsrechtlich zu klären ist, und dass du sie nicht beantwortest –
   insbesondere Anwendbarkeit und Allgemeinverbindlichkeit eines Tarifvertrags,
   Eingruppierung, Entstehen einer betrieblichen Übung, Wirksamkeit von
   Ausschluss-, Verfalls- und Widerrufsklauseln, Höhe des Anspruchs.
5. Mandantenabfrage erzeugen. Formuliere zu jedem Auslöser genau eine Frage, die
   der Mandant oder seine arbeitsrechtliche Beratung mit ja, nein oder einer
   Unterlage beantworten kann. Keine Suggestivfragen, keine Rechtsansicht in der
   Frage. Ergänze je Frage, welche Unterlage die Antwort belegt.
6. Verantwortung dokumentieren. Formuliere einen Vermerk für die Handakte und
   einen Absatz für das Anschreiben, die beide festhalten: Die Abrechnung folgt
   den Angaben des Arbeitgebers; die arbeitsrechtliche Beurteilung des
   geschuldeten Entgelts trifft der Arbeitgeber; ungeklärte Punkte bleiben
   ungeklärt, bis eine Antwort vorliegt. Ohne Vorwurf und ohne Drohung
   formulieren.
7. Folgen dem Grunde nach. Nachforderung des Gesamtsozialversicherungsbeitrags
   und wer ihn trägt (§ 28e SGB IV), die Grenze des Rückgriffs beim Arbeitnehmer
   (§ 28g SGB IV) und die Verjährung einschließlich der Verlängerung bei Vorsatz
   (§ 25 Abs. 1 SGB IV), jeweils für [JAHR] verifizieren. Nenne keine Dauer,
   keinen Satz und keinen Betrag. Berechne KEINE Fristen. Liste auf, WELCHE
   Fristen im Raum stehen (tarifliche und vertragliche Ausschlussfristen,
   Verjährung, Meldekorrekturen), je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", und ergänze bei jeder: "Frist von einem Menschen zu
   berechnen und im Fristenprogramm zu erfassen."
8. Ergebnis als Arbeitsstand, nicht als Beurteilung. Fasse zusammen, welche
   Auslöser gefunden wurden, welche Fragen offen sind und wer sie beantwortet.
   Gib KEIN Ergebnis zur Beitragspflicht aus.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Der Verdacht, dass auf geschuldetes, aber nicht gezahltes Entgelt keine Beiträge
abgeführt wurden, ist KEIN Abbruchgrund – er ist der Gegenstand dieses Prompts.
Auch eine drohende Beitragsnachforderung ist kein Abbruchgrund. Brich die
gesamte Bearbeitung nur ab, wenn die Angaben (a) angeben, dass einbehaltene
Arbeitnehmeranteile nicht abgeführt wurden, (b) ein Straf-, Ermittlungs- oder
Bußgeldverfahren, eine Durchsuchung oder eine Prüfung der Finanzkontrolle
Schwarzarbeit mit strafrechtlichem Einschlag erwähnen, oder (c) angeben, dass
Arbeitsentgelt bewusst ohne Abrechnung ausgezahlt wurde. Gib dann nur aus:
"Anzeichen für einen Strafsachverhalt – Bearbeitung abgebrochen, Prüfung durch
einen Berufsträger außerhalb des KI-Werkzeugs, zusätzlich Hinzuziehung eines
Strafverteidigers." Betrifft ein einzelner Auslöser einen Zeitraum, für den
bereits ein Beitragsbescheid ergangen ist, steuere nur diesen Auslöser aus,
weise ihn als "Rechtsbehelfssache – Berufsträger" gesondert aus und arbeite die
übrigen normal weiter.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben
   auf. Ist der Mindestlohnvergleich nicht gezogen, bearbeite den entsprechenden
   Auslöser nicht, sondern nimm ihn als offene Frage auf.
2. Nenne zu jedem Auslöser die Rechtsgrundlage POSITIV mit Norm, Absatz und
   Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine
   Paragrafen, keine Tarifverträge und keine Aktenzeichen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
3. Höchstens ZEHN Auslöser. Wähle die mit dem größten Nachforderungsrisiko und
   lasse alles weg, was nach dem Kontext nicht vorkommt.
4. Formuliere jede Aussage über den arbeitsrechtlichen Anspruch als Frage oder
   ausdrücklich als Vermutung. Keine erfundenen Ansprüche, keine erfundene
   Tarifbindung.
5. Erzeuge die Mandantenabfrage als Tabelle mit leerer Antwortspalte.

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit und fehlende Angaben
2. Weiche: laufendes oder einmalig gezahltes Arbeitsentgelt
3. AUSLÖSERTABELLE mit den Spalten:
   Nr. | Auslöser | Rechtsgrundlage mit Zusatz | Einordnung nach Schritt 1 |
   Arbeitsrechtlich offene Frage | Belegende Unterlage
4. MANDANTENABFRAGE mit den Spalten:
   Nr. | Frage | Unterlage | Antwort des Mandanten (leer) | Wer antwortet |
   Erledigt (leer)
5. Vermerk für die Handakte und Absatz für das Anschreiben
6. Folgen dem Grunde nach
7. Fristarten mit Rechtsgrundlage
8. Arbeitsstand: gefundene Auslöser, offene Fragen, Verantwortliche
9. Interne Notiz
10. Was ich nicht sicher weiß
```

## Anwendung

1. Prompt bei jedem Mandatsbeginn im Lohnbereich, bei Tarifbindung, bei Branchenmindestlöhnen und vor jeder Prüfung der Rentenversicherung ausführen.
2. Den Mindestlohnvergleich vor dem Einsatz selbst ziehen und das Ergebnis in den Kontext eintragen – der Prompt rechnet nicht.
3. Mandantenabfrage unverändert versenden, Antworten in der Handakte ablegen und den Eingang datieren; unbeantwortete Fragen bleiben in der Wiedervorlage.
4. Der Vermerk gehört in die Handakte, nicht in das Anschreiben – und er ersetzt keine Klärung, sondern hält den Stand fest.
5. Für die Vorbereitung der Prüfung der Rentenversicherung mit Prompt 97 weiterarbeiten, für Statusfragen mit Prompt 99.

## Qualitätssicherung

- **Der Prompt beantwortet die entscheidende Frage nicht – und das ist beabsichtigt.** Ob ein Anspruch besteht, ist arbeitsrechtlich zu klären. Eine Antwort, die eine Eingruppierung vornimmt oder eine Allgemeinverbindlichkeit bejaht, ist zu verwerfen.
- **Keine Beträge und keine Mindestlohnhöhe aus der KI-Antwort.** Der Mindestlohn ändert sich; der Vergleich wird in der Kanzlei gezogen und dokumentiert.
- **Das Entstehungsprinzip überrascht Mandanten regelmäßig.** Der Hinweis, dass Beiträge auch ohne Auszahlung entstehen können, gehört ausdrücklich in das Anschreiben – sonst wird die Abfrage als Formalie behandelt.
- **Unbeantwortete Fragen sind ein Ergebnis.** Wer sie nicht in der Wiedervorlage führt, hat die Verantwortung nicht dokumentiert, sondern nur verschoben.
- **Rückgriff beim Arbeitnehmer ist begrenzt.** Bei einer Nachforderung trägt der Arbeitgeber wirtschaftlich beide Anteile; das ist dem Mandanten vor der Abfrage zu sagen.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt die Auslöserliste, die Einordnung nach § 22 Abs. 1 SGB IV und die Vollständigkeit der Abfrage nach. Anschreiben, Vermerk und jede Aussage gegenüber dem Mandanten gibt ein Berufsträger frei, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 22 Abs. 1 Satz 1 und Satz 2, § 25 Abs. 1, § 28e und § 28g SGB IV, § 1 MiLoG, § 2 und § 4 Abs. 1 EFZG sowie den Vorschriften des Bundesurlaubsgesetzes zum Urlaubsentgelt im amtlichen Volltext (gesetze-im-internet.de), ergänzend an den Rundschreiben der Spitzenorganisationen der Sozialversicherung und an DATEV LEXinform.

## Varianten

- **Nur Abfrage:** „Erzeuge ausschließlich die Mandantenabfrage mit leerer Antwortspalte, ohne Prüfprotokoll."
- **Branchenmindestlohn:** „Ergänze die Frage, ob ein Branchenmindestlohn oder ein für allgemeinverbindlich erklärter Tarifvertrag einschlägig sein kann, und benenne, wer das klärt."
- **Entgeltfortzahlung:** „Vertiefe den Auslöser zur Berechnungsgrundlage der Entgeltfortzahlung und erzeuge eine Prüfliste der Entgeltbestandteile."
- **Bestandsdurchsicht:** „Erzeuge eine Prüfliste, mit der die Kanzlei ihre Lohnmandate auf die drei häufigsten Auslöser durchsieht."
- **Mandanteninformation:** „Erkläre dem Arbeitgeber in höchstens 300 Wörtern, Sie-Form, ohne Betrag, warum Beiträge auch auf nicht ausgezahltes Entgelt entstehen können."
