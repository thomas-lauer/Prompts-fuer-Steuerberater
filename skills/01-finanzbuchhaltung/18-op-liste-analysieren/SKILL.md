---
name: op-liste-analysieren
description: Wertet einen OPOS-Export der Debitoren zeilenweise aus: Altersstruktur,
  Konzentrationsrisiko, Auffälligkeiten und je Altersklasse eine Maßnahme. Fordert
  Gewinnermittlungsart und Besteuerungsart aktiv nach, weil Wertberichtigung und
  § 17 UStG davon abhängen, und ordnet jeden Posten einer Risikoklasse zu.
  Use when a client's open-item list (accounts receivable export) needs an ageing
  analysis, a dunning proposal or a bad-debt review before a period end.
---

# 18 – Offene Posten auswerten

## Zweck

Der Prompt beschreibt, wie eine OP-Liste zu analysieren ist. Diese Skill wertet
den Export tatsächlich aus: Sie liest jede Zeile, ordnet sie einer Altersklasse
zu, summiert je Klasse, rechnet die Anteile, ermittelt die Konzentration der
größten Debitoren, leitet die Maßnahmenliste ab und hält je Posten die Zuordnung
zu zweifelhaft, uneinbringlich oder weder-noch fest. Der Mengenvorteil liegt in
der Zeilenzahl – mehrere hundert Posten sind mit dem Textblock allein nur von
Hand durchzuarbeiten.

## Wann einsetzen – und wann nicht

Einsetzen, wenn ein OPOS-Export der Debitoren zu einem Stichtag vorliegt und die
Forderungen des Mandanten gegen seine Kunden auszuwerten sind – vor einem
Mandantengespräch, vor dem Abschluss oder als monatliche Serie. In der Serie wird
die Datei des Vormonats mit eingelesen; ausgewiesen werden dann zusätzlich die
Veränderungen je Altersklasse und je Debitor sowie die Posten, die eine Klasse
gewechselt haben.

Nicht einsetzen für offene Kanzleihonorare: Für Zahlungserinnerung, Mahnung und
Ratenzahlung gegenüber dem eigenen Mandanten ist Prompt 16 einschlägig, der
Rechnungsdaten, Kontaktverlauf und die Frage nach einer Ratenzahlung abfragt und
Mahntexte erzeugt. Soll aus den Fälligkeiten eine Zahlungsprognose mit
Kontoständen, Fixkosten und Kreditlinien werden, ist Prompt 66 einschlägig
(13-Wochen-Planung; jede Einordnung und jede Verwendung außerhalb der Kanzlei
nur durch einen Berufsträger). Steht Zahlungsunfähigkeit im Raum, gehört der Fall
zu Prompt 74 (nur Berufsträger); diese Skill stellt sie nicht fest und rechnet
keine Deckungslücke. Doppelt angelegte Debitorenkonten und doppelt erfasste
Rechnungen prüft Prompt 19 auf dem Buchungs- oder Stammdatenexport.

Der Abgleich der Altersstruktursummen gegen die Debitorensumme der Summen- und
Saldenliste ist kein eigener Prompt, sondern der Kontrollschritt dieser Skill
(siehe Qualitätssicherung); er wird an der Summen- und Saldenliste im Programm
vorgenommen. Fällt dabei die Summen- und Saldenliste selbst als prüfbedürftig
auf, ist Prompt 20 einschlägig, der den SuSa-Export auf Auffälligkeiten prüft.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Vor dem ersten Blick in die Daten einholen und dokumentieren:

- die ausdrückliche Bestätigung, dass Steuer-Identifikationsnummer, Steuernummer
  und Aktenzeichen des Finanzamts aus dem Export entfernt sind – nicht maskiert,
  nicht gekürzt, nicht in einzelnen Ausschnitten stehengelassen;
- dass Kundennamen durch fortlaufende Platzhalter ersetzt sind (`Debitor 1`,
  `Debitor 2`) und derselbe Kunde durchgehend dasselbe Kürzel trägt, sonst wird
  die Konzentrationsanalyse unbrauchbar;
- dass auch die Debitorennummern durch dieselben Pseudonyme ersetzt sind –
  identische Konten erhalten dasselbe Pseudonym, verschiedene Konten
  verschiedene. Nicht verkürzen: Zwei Konten können in den letzten Stellen
  übereinstimmen und würden in der Konzentrationsanalyse fälschlich zu einem
  Debitor verschmelzen;
- dass vollständige IBAN nicht mitkommen und der Mandant nur als Mandatskürzel
  geführt wird. Die Zuordnungstabelle bleibt in der Kanzlei.

Taucht Zone-Rot-Material auf – eine Steuernummer in einer Kopfzeile, ein
Aktenzeichen in einer Bemerkungsspalte, ein Hinweis auf ein Steuerstrafverfahren
–, sofort abbrechen, den Fundort mit Zeile und Spalte benennen und den Anwender
bitten, den Export ohne diese Spalte neu zu ziehen und erneut einzufügen. Nicht
selbst überschreiben und mit dem Rest weiterrechnen.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung
des Anbieters nach § 62a StBerG müssen vor dem Einsatz geklärt sein; § 62a StBerG
geht der DSGVO-Prüfung vor. Maßstab ist `DATENSCHUTZ.md`, Zone Rot.

## Ablauf

1. **Vollständigkeit und Rahmen abfragen, bevor gerechnet wird.** Zuerst
   ausdrücklich fragen: Enthält der Export alle offenen Debitorenposten zum
   Stichtag oder ist er gefiltert (nach Mahnstufe, Betragsgrenze,
   Vertriebsbereich, einzelnen Konten)? Ist er gefiltert, werden keine Anteile an
   der Gesamtforderung und keine Konzentrationsquoten ausgewiesen, sondern nur
   absolute Werte je Klasse; der Filter wird im Kopf der Datei genannt. Danach:
   Mandatskürzel und Branche, Stichtag, Kontenrahmen, Zahlungsziel und
   Skontokondition, Besonderheiten wie Abschlagsrechnungen, Ratenzahlungen,
   laufende Insolvenzverfahren oder Factoring. Ohne Stichtag ist keine
   Altersklasse bestimmbar – nachfordern, nicht schätzen.

2. **Gewinnermittlungsart und Besteuerungsart ausdrücklich nachfordern.** Bilanz
   oder EÜR, Soll- oder Ist-Versteuerung. Beide sind Schalter: Von der ersten
   hängt ab, ob eine Wertberichtigung überhaupt in Betracht kommt, von der
   zweiten, ob eine Berichtigung wegen Uneinbringlichkeit in Frage kommt. Fehlt
   eine, hier anhalten und fragen – nicht "Bilanz" unterstellen, weil die Liste
   umfangreich aussieht. Bei EÜR keine Wertberichtigung bilden und die
   Nichtanwendbarkeit vermerken, wie der Prompt es in Anforderung 6 verlangt; der
   umsatzsteuerliche Prüfpfad läuft unverändert weiter.

3. **Datenqualität je Spalte prüfen.** Welche Felder fehlen, welche Zeilen sind
   nicht auswertbar (kein Fälligkeitsdatum, Restbetrag leer). Solche Zeilen
   gesondert ausweisen und aus den Summen heraushalten. Gutschriften und
   Minusposten ohne Zuordnung werden NICHT als Datenqualitätsproblem abgelegt,
   sondern nach dem Katalog des Prompts (Anforderung 4, letzter Spiegelstrich)
   als Auffälligkeit geführt und zusätzlich in den Entgeltminderungszweig
   gegeben.

4. **Zeilenweise klassifizieren.** Jeden Posten anhand von Fälligkeit und
   Stichtag genau einer Altersklasse nach dem Raster des Prompts (Anforderung 2)
   zuordnen, je Klasse Anzahl, Summe und Anteil rechnen und die Klassensummen
   gegen die Gesamtsumme aller auswertbaren Zeilen zurückrechnen. Weicht die
   Rückrechnung ab, ist die eigene Zuordnung fehlerhaft – nicht der Export.

5. **Konzentration und Auffälligkeiten.** Debitoren aggregieren, die Anteile nach
   Anforderung 3 des Prompts ermitteln, jedes Klumpenrisiko benennen und je
   Klumpenrisiko sagen, was der Ausfall dieses Debitors für die Gesamtforderung
   bedeuten würde. Auffälligkeiten nach dem Katalog des Prompts (Anforderung 4)
   sammeln, nach Betrag sortieren, auf dessen Höchstzahl begrenzen. Skonti, Boni
   und Gutschriften werden zusätzlich in den Entgeltminderungszweig des Prompts
   (Anforderung 7, letzter Absatz) gegeben: getrennt von der Uneinbringlichkeit,
   mit dem Vermerk, dass der Voranmeldungszeitraum gesondert festzustellen ist,
   und mit der ausdrücklichen Frage an den Anwender, ob ein bereits übermittelter
   Zeitraum betroffen ist.

6. **Risikoklasse je Posten.** Jeden Posten der Liste – nicht nur die des
   Prüfvorschlags – genau einer der drei Ebenen des Prompts zuordnen:
   zweifelhaft, uneinbringlich oder weder noch. Bei EÜR entfällt die Ebene
   "zweifelhaft" mangels Wertberichtigung; die Ebenen "uneinbringlich" und "weder
   noch" werden trotzdem über alle Posten geführt, weil der umsatzsteuerliche
   Prüfpfad von der Gewinnermittlungsart unabhängig ist. Die Kriterien der drei
   Ebenen stehen vollständig in Anforderung 7 der Prompt-Datei und werden von
   dort übernommen, nicht aus dem Gedächtnis: Netto- statt Bruttobezug bei der
   Wertberichtigung, getrennte Beantwortung handelsrechtlich und steuerlich, die
   zusätzlichen Anforderungen an die Uneinbringlichkeit und die Folge der
   Ist-Versteuerung. Jedes Ergebnis wird je Posten protokolliert; ohne
   Anhaltspunkt für rechtliche oder tatsächliche Undurchsetzbarkeit lautet die
   Zuordnung nie uneinbringlich, und der fehlende Anhaltspunkt wird offene Frage.

7. **Maßnahmen ableiten und schreiben.** Je Altersklasse eine Maßnahme mit
   Adressat in der Kanzlei oder beim Mandanten; vorher ausdrücklich fragen, ob
   die Zahlungseingänge bis zum Stichtag vollständig verbucht sind. Alles, was
   nicht aus den Daten folgt, als Vermutung kennzeichnen. Kein Pauschalsatz und
   kein Erfahrungssatz wird als gesichert genannt; jeder erhält den Zusatz "Satz
   für [JAHR] verifizieren – auch für diesen Mandanten", Sätze aus dem Gedächtnis
   werden nicht gebildet. Jede rechtliche Aussage trägt Norm (Absatz und Satz),
   Richtlinie oder BMF-Schreiben mit Datum und den wörtlichen Zusatz "für [JAHR]
   verifizieren"; ist die Fundstelle unsicher, "Fundstelle offen – bitte
   recherchieren", ist sie nicht angebbar, "ohne Fundstelle – vor Verwendung
   belegen".

## Ergebnis

Eine Markdown-Datei `<Mandatskürzel>-op-analyse-<JJJJ-MM>.md` im Arbeitsordner
des Mandats, aufgebaut nach dem Ausgabeformat der Prompt-Datei: Datenqualität,
Altersstruktur, Konzentrationsrisiko, Auffälligkeiten, Maßnahmen je Altersklasse,
Prüfvorschlag zur Wertberichtigung – ausdrücklich als Prüfvorschlag formuliert,
ohne Entscheidung, ohne Betragsvorgabe und ohne Buchungssatz; er geht in die
Abschlussakte und wird nicht gebucht –, interne Notiz und unsichere Punkte. Im
Kopf stehen Stichtag, Gewinnermittlungsart, Besteuerungsart, die beantwortete
Vollständigkeitsfrage samt Filterangabe und die Zahl der ausgewerteten wie der
nicht auswertbaren Posten – daran ist erkennbar, auf welcher Grundlage
klassifiziert wurde. Die interne Notiz geht nicht an den Mandanten; fürs Gespräch
wird die Maßnahmentabelle einzeln herausgezogen.

## Qualitätssicherung

Kein Ergebnis verlässt die Kanzlei ohne menschliche Prüfung. Vor der Weitergabe:

- Klassensummen und Prozentanteile in der Tabellenkalkulation gegenrechnen.
  Summenbildung über viele Zeilen bleibt die bekannteste Fehlerquelle.
- Die Altersstruktursummen gegen die Debitorensumme der Summen- und Saldenliste
  abgleichen. Stimmen sie nicht überein, ist der Export unvollständig.
- Vor jeder Mahnung prüfen, ob zwischenzeitliche Zahlungseingänge verbucht sind.
- Eine zweite Person zeichnet die Konzentrationsanalyse und mindestens drei
  Einzelposten nach. Die Freigabe zur Weitergabe erteilt ein Berufsträger; über
  Wertberichtigung, Ausbuchung und § 17 UStG entscheidet er ausschließlich selbst.
  Die Freigabe ist zu dokumentieren.
- Alle Erfahrungssätze, Fristen und Fundstellen gegen eine Primärquelle prüfen;
  kein Wert wird aus der Ausgabe übernommen.

Die Skill berechnet keine Fristen: Zeitpunkt der Uneinbringlichkeit,
Voranmeldungszeitraum und Verjährung benennt sie als gesondert festzustellen.

## Grundlage

Prüfschema, Sachverhaltsbogen und Ausgabeformat stehen allein in der Prompt-Datei:
[prompts/01-finanzbuchhaltung/18-op-liste-analysieren.md](../../../prompts/01-finanzbuchhaltung/18-op-liste-analysieren.md).
