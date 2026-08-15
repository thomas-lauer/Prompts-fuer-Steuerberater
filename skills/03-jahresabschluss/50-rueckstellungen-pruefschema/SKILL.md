---
name: rueckstellungen-pruefschema
description: Arbeitet einen Rückstellungsspiegel zum Bilanzstichtag Position für Position durch,
  hält je Position die Trennung von Handels- und Steuerbilanz durch und fordert fehlende
  Sachverhalts- und Datumsangaben aktiv nach. Sie bewertet keine Rückstellung der Höhe nach.
  Use when a Rückstellungsspiegel has to be reviewed before closing the books, when Ansatz,
  Bewertung oder Auflösungszeitpunkt je Position begründet werden müssen, or when
  Begründungstexte für die Handakte fehlen.
---

# 50 – Rückstellungen zum Bilanzstichtag prüfen

## Zweck

Die Skill nimmt den Mandantenrahmen einmal auf, bildet aus dem Spiegel eine Arbeitsliste und
wendet auf jede Zeile dasselbe Sechs-Schritte-Raster der Prompt-Datei an. Darin liegt der
Mengenvorteil: Mit dem Textblock allein müsste ein Mensch den Prompt je Position neu ausfüllen
und den Rahmen jedes Mal wiederholen; die Skill fragt je Position nur noch nach, was tatsächlich
fehlt, und führt die offenen Punkte gebündelt zurück. Sie erzwingt zudem, was in der Handarbeit
untergeht: Ansatz handelsrechtlich und Ansatz steuerlich werden je Position getrennt beantwortet
und einzeln protokolliert. Die Skill **bewertet nicht**: Sie ermittelt keine Rückstellung der Höhe
nach und rechnet außer der Konsistenzprobe je Spiegelzeile nichts.

## Wann einsetzen – und wann nicht

Einsetzen, wenn ein Rückstellungsspiegel mit mehreren Positionen zum Stichtag vorliegt und je
Position Ansatz, Bewertungsvergleich, Auflösungszeitpunkt und ein Begründungstext für die
Handakte entstehen sollen – bei der Abschlusserstellung, vor dem Abschlussgespräch oder wenn die
Begründungen der Vorjahre nur fortgeschrieben wurden. Nicht einsetzen für:

- **Periodenabgrenzung und Nachlauf** – nach dem Stichtag eingegangene Rechnungen,
  Abgrenzungsposten, nicht abgerechnete Leistungen: Prompt 51. Er arbeitet mit der Buchungsliste
  des Nachlaufzeitraums und der OPOS-Liste, nicht mit dem Rückstellungsspiegel.
- **Investitionsabzugsbeträge und ihre Fristen:** Prompt 53. Er verlangt die Übersicht der
  Abzugsbeträge mit Jahr, Betrag, geplantem Wirtschaftsgut und verwendetem Teilbetrag – Angaben,
  die im Spiegel nicht stehen.
- **Vorbereitung einer Betriebsprüfung:** Prompt 34. Er setzt die Prüfungsanordnung mit
  Steuerarten, Zeitraum, Schwerpunkten, Beginn und Prüfungsort voraus; ohne sie ist er nicht
  bedienbar.
- **Übernommene Bestände beim Mandatswechsel:** Prompt 22, sobald die Frage die Kontenzuordnung
  des Vorberaters betrifft – er verlangt dessen Kontenplan oder Summen- und Saldenliste.

Ebenso wenig einsetzen, um eine Rückstellung der Höhe nach zu ermitteln, eine Abzinsung zu
rechnen oder einen Erfüllungsbetrag zu schätzen.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Vor der ersten Position ist zu bestätigen, dass **Steuer-Identifikationsnummer, Steuernummer und
Aktenzeichen des Finanzamts entfernt** sind – nicht maskiert, sondern entfernt, auch in
Ausschnitten und in Kopfzeilen exportierter Auswertungen. Sie sind Zone Rot nach
`DATENSCHUTZ.md` und werden für die Prüfung nicht gebraucht.

Gearbeitet wird ausschließlich mit Mandatskürzeln und Rollenbezeichnungen: `Mandant A`, `AN 1`,
`Gegenseite 1`, `Lieferant 1`. Prozessgegner, Behörden und Vertragspartner werden nur nach ihrer
Rolle bezeichnet; für die Prüfung genügen Sachverhalt, Beträge, Zeitpunkte und Restlaufzeiten.
Zwei Positionsarten verlangen besondere Aufmerksamkeit: Bei **Prozesskostenrückstellungen** darf
der Sachverhalt nichts zu einem laufenden Straf- oder Steuerstrafverfahren oder zu einer
Selbstanzeige enthalten, bei **Personalrückstellungen** nichts zu Gesundheit, Religions-,
Gewerkschafts- oder Parteizugehörigkeit einzelner Arbeitnehmer. Beides ist Zone Rot.

Taucht Zone-Rot-Material auf, wird abgebrochen und konkret zurückgemeldet, was stattdessen
einzureichen ist – etwa: Spalte mit der Steuernummer aus dem Export löschen; den Sachverhalt der
Prozessrückstellung auf Zeitpunkt, Streitwert und die Angabe "zivilrechtliche Streitigkeit" oder
"verwaltungsrechtliche Streitigkeit" reduzieren; Arbeitnehmernamen durch `AN 1`, `AN 2` ersetzen.
Danach den Spiegel erneut einreichen. Betrifft die Rückstellung ein Straf- oder
Steuerstrafverfahren oder eine Selbstanzeige, wird die Position gar nicht eingereicht – auch nicht
in reduzierter Form, weil schon die Art des Streitgegenstands das Verfahren offenbart: Sie wird
außerhalb des Werkzeugs vom Berufsträger beurteilt und im Ergebnis nur als "Position außerhalb des
Werkzeugs bearbeitet" geführt.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters
nach § 62a StBerG (sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung)
müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Ablauf

0. **Abbruchregel – gilt vor jedem Schritt und nach jeder neuen Angabe.** Deutet das Material
   darauf hin, dass eine bereits abgegebene Erklärung unrichtig war, endet die Bearbeitung sofort;
   ausgegeben wird nur der Abbruchsatz der Prompt-Datei (Anforderung 7). Kein Prüfprotokoll, keine
   Teilausgabe, keine Rückfrageliste. Die Prüfung führt ein Berufsträger außerhalb des Werkzeugs.
1. **Mandantenrahmen einmal aufnehmen:** Rechtsform, Gewinnermittlung (Bilanz oder Bilanz mit
   Überleitungsrechnung – wird EÜR angegeben, endet die Bearbeitung mit dem Hinweis, dass
   Rückstellungen bei Gewinnermittlung nach § 4 Abs. 3 EStG nicht in Betracht kommen und die
   Positionen anders zu qualifizieren sind), Kontenrahmen, handelsrechtliche Größenklasse,
   Einordnung durch die Finanzverwaltung, Stichtag, Branche und Besonderheiten. Fehlt die
   Einordnung des Betriebs, wird sie als unbekannt geführt und nicht geraten – sie wirkt auf die
   Position "Kosten einer Betriebsprüfung".
2. **Eindeutigkeit festhalten, bevor die erste Position beurteilt wird:** Was ist aus dem Spiegel
   entscheidbar, was nicht, welche Angabe fehlt je Position. Dieser Abschnitt wird nicht
   nachträglich aus dem Ergebnis abgeleitet, sondern vorab geschrieben und danach nur ergänzt.
3. **Spiegel in eine Arbeitsliste überführen:** je Zeile Konto, Bezeichnung, Vorjahressaldo,
   Zuführung, Verbrauch, Auflösung, Stand am Stichtag, Sachverhalt, Restlaufzeit. Beträge werden
   unverändert übernommen. Ermittelt wird kein Erfüllungsbetrag, keine Abzinsung und kein
   Auflösungsbetrag; geprüft wird lediglich, ob Vorjahressaldo, Zuführung, Verbrauch, Auflösung und
   Stand am Stichtag je Zeile zusammenpassen. Eine Abweichung ist ein Befund und wird als Rückfrage
   geführt, nicht korrigiert.
4. **Vollständigkeit je Zeile prüfen, bevor gearbeitet wird.** Eine Zeile ohne Sachverhalt in
   zwei bis drei Sätzen oder ohne Datum des auslösenden Ereignisses wird markiert; die Schritte zur
   Verursachung und zur Wahrscheinlichkeit bleiben für sie ausdrücklich "nicht entscheidbar –
   Angabe fehlt". Die übrigen Schritte werden auch für diese Zeilen durchgeführt, soweit die
   Bezeichnung sie trägt, und die fehlende Angabe geht in die Rückfrageliste. Ein Ansatz wird auf
   dieser Grundlage nie bestätigt.
5. **Jede Position einzeln durch die sechs Prüfschritte** der Prompt-Datei führen (Abschnitt
   "PRÜFE JEDE RÜCKSTELLUNG IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST"), in deren
   Reihenfolge und mit deren Kriterien. Jedes Schrittergebnis wird festgehalten, auch wenn es
   "nicht entscheidbar" lautet. Jede Ursachen- und Wahrscheinlichkeitsaussage, die nicht aus den
   eingereichten Angaben folgt, wird ausdrücklich als Vermutung gekennzeichnet – auch im
   Begründungstext für die Handakte.
6. **Prüfschritt 4 wird nie zusammengezogen.** Je Position zuerst der handelsrechtliche Ansatz,
   danach getrennt der steuerliche. Die unter Prüfschritt 4 Buchstabe b der Prompt-Datei
   aufgeführten steuerlichen Ansatz- und Bewertungsverbote werden **einzeln** und in der dortigen
   Reihenfolge
   durchgegangen und je Fall mit "greift / greift nicht / nachzuschlagen" und Fundstelle
   protokolliert; der Katalog wird aus der Prompt-Datei gelesen, nicht aus dieser Skill. Ein
   handelsrechtlicher Wert wird **nie** stillschweigend in die Steuerspalte übernommen: Fehlt das
   protokollierte Ergebnis, bleibt die Steuerspalte offen und die Position kommt auf die
   Rückfrageliste. "Wie handelsrechtlich" ist kein zulässiges Ergebnis.
7. **Sonderfälle an der Bezeichnung erkennen** und die zusätzlichen Voraussetzungen aus dem
   Abschnitt "SONDERFÄLLE, SOWEIT IM SPIEGEL VORHANDEN" der Prompt-Datei anwenden; der Katalog der
   Sonderfälle steht dort und wird von dort gelesen. Ist die maßgebliche Einordnung des Betriebs unbekannt, wird das als
   offener Punkt geführt.
8. **Begründungslage je Position einstufen** als tragfähig, dünn oder nicht tragfähig, mit einem
   Satz dazu, was fehlt (Anforderung 6 der Prompt-Datei). Die Einstufung steht je Position im
   Prüfprotokoll, nicht nur in der Sammelliste.
9. **Fehlende Angaben gebündelt nachfordern:** eine Rückfrage über alle markierten Zeilen, je
   Zeile mit der genau fehlenden Angabe. Bleibt sie unbeantwortet, gilt die Position als nicht
   entscheidbar und ihre Begründungslage als nicht tragfähig – es wird nicht geschätzt und nicht
   aus dem Vorjahr fortgeschrieben.
10. **Ergebnisdatei schreiben** in der Gliederung des Ausgabeformats der Prompt-Datei.

## Ergebnis

Eine Datei `<Mandatskürzel>-rueckstellungen-<JJJJ-MM-TT>.md` mit dem Stichtag im Namen. Inhalt und
Reihenfolge richten sich nach dem Ausgabeformat der Prompt-Datei: Eindeutigkeit und Datenlage;
Prüfprotokoll je Position mit den sechs Schritten, der Einstufung der Begründungslage und dem
Begründungstext für die Handakte; Tabelle Bewertungsvergleich mit den dort genannten Spalten;
Liste der dünn und der nicht tragfähig begründeten Positionen mit dem, was nachzudokumentieren
ist; aufzulösende Rückstellungen mit Zeitpunkt; interne Notiz; "Was ich nicht sicher weiß".

Jede rechtliche Aussage trägt Norm, Absatz und Satz mit dem wörtlichen Zusatz "für [JAHR]
verifizieren"; unsichere Fundstellen: "Fundstelle offen – bitte recherchieren". Kein Prozentsatz,
Zinssatz, kein Betragsgrenzwert und keine Fristlänge wird als feststehend genannt – jeder solche
Wert erscheint als nachzuschlagende Größe mit demselben Zusatz. Offene Positionen bleiben sichtbar
offen statt gefüllt.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Eine zweite fachkundige Person zeichnet den Spiegel Position
  für Position ab; über Ansatz und Bewertung entscheidet ein Berufsträger und dokumentiert die
  Freigabe (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Die Skill bewertet nicht.** Sie ermittelt keinen Erfüllungsbetrag, keine Abzinsung und keinen
  Auflösungsbetrag; jeder Betrag ist außerhalb zu ermitteln und nachzurechnen. Die einzige
  Rechnung, die sie ausführt, ist die Konsistenzprobe je Zeile (Vorjahressaldo plus Zuführung
  abzüglich Verbrauch und Auflösung gegen den Stand am Stichtag); auch sie ist gegenzurechnen.
- Vor der Verwendung ist je Position zu prüfen: Verursachungszeitpunkt, Ergebnis zum steuerlichen
  Ansatz, Abzinsung, Trennung von Handels- und Steuerbilanz. Eine Steuerspalte, die den
  Handelsbilanzwert wiederholt, ist ein Befund und kein Ergebnis.
- Der Rechtsstand ist an den Quellen zu prüfen, die der Abschnitt `## Qualitätssicherung` der
  Prompt-Datei nennt; keine Norm, kein Zinssatz und keine Frist wird aus der Ausgabe übernommen.
- Fehlt zu einer Rückstellung ein Beleg, ist das ein Befund: nicht dokumentierte Rückstellungen
  fallen in der Prüfung zuerst.

## Grundlage

Prüfschema, Sachverhaltsbogen und Ausgabeformat stehen in der Prompt-Datei; die Skill folgt ihr
und schreibt sie nicht ab:
[prompts/03-jahresabschluss/50-rueckstellungen-pruefschema.md](../../../prompts/03-jahresabschluss/50-rueckstellungen-pruefschema.md).
