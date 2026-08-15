---
name: ustva-abweichung-eingrenzen
description: Stellt die Werte der Umsatzsteuer-Voranmeldung je Kennzahl neben die
  Salden der Umsatzsteuer-, Vorsteuer- und Erlöskonten, rechnet die Verprobung je
  Steuersatz mit sichtbarem Rechenweg, beziffert den unerklärten Rest und leitet daraus
  eine nach Wahrscheinlichkeit sortierte Ursachenliste mit Zehn-Minuten-Prüfschritten
  ab. Hält den Abweichungsbetrag zusätzlich gegen jeden Kontensaldo und gegen typische
  Betragsmuster. Use when a VAT return does not match the bookkeeping and the cause has
  to be narrowed down, monthly or after a correction.
---

# 05 – UStVA-Abweichung zur Buchhaltung systematisch eingrenzen

## Zweck

Der Prompt beschreibt das hypothesengeleitete Vorgehen. Diese Skill führt es aus:
Sie rechnet die Verprobung selbst – erwartete Umsatzsteuer aus den Erlöskonten je
Steuersatz gegen die gemeldeten Kennzahlen –, beziffert den Rest, der damit noch
nicht erklärt ist, und hält den Abweichungsbetrag maschinell gegen jeden
eingefügten Kontensaldo und gegen die typischen Betragsmuster. Der Mengenvorteil
liegt in dieser Kombinatorik: Kennzahlen mal Konten mal Steuersätze sind von Hand
mühsam, und derselbe Lauf wiederholt sich jeden Voranmeldungszeitraum mit neuen
Zahlen. Am Ende steht ein aufklärender Prüfweg, keine Verfahrensbeschreibung.

## Wann einsetzen – und wann nicht

Einsetzen, wenn eine Differenz zwischen Voranmeldung und Buchhaltung bekannt ist
oder aus Kennzahlen und Salden ermittelt werden soll – im laufenden Monat, nach
einer Rückfrage des Finanzamts oder wenn eine Abweichung seit mehreren Perioden
mitläuft.

Nicht einsetzen, wenn noch gar keine Abweichung im Raum steht und die
Buchhaltung nur allgemein durchgesehen werden soll: Dafür ist Prompt 20 gemacht,
der Verkehrszahlen, Vorjahreswerte und Kontenrahmen verlangt und die Konten über
das gesamte Prüfraster laufen lässt. Steht die umsatzsteuerliche Einordnung eines
einzelnen Sachverhalts in Frage – Reverse-Charge, innergemeinschaftlicher Erwerb,
Differenzbesteuerung –, ist Prompt 04 der richtige Einstieg; er fragt Sitz und
USt-ID-Status beider Beteiligten und den Rechnungswortlaut ab, Angaben, die in
einer Kennzahlen-Salden-Liste gar nicht vorkommen. Betrifft die Abweichung
steuerfreie innergemeinschaftliche Lieferungen, gehört der belegweise Abgleich
gegen die übermittelten Meldungen und die Nachweise zu Prompt 58. Geht es um
Rechnungen mit unrichtigem Steuerausweis und deren Berichtigung, führt Prompt 87
über Ausweiswortlaut und Empfängerkreis – aber nur für **eigene
Ausgangsrechnungen** des Mandanten: Sein Bogen fragt durchgehend Angaben des
Ausstellers ab, und eine Abweichung, die aus einer Eingangsrechnung stammt,
trägt er nicht. Um den unterjährigen Statuswechsel eines Kleinunternehmers geht
es in Prompt 88. Diese Skill klärt die Ursache – sie entscheidet
nicht über eine Berichtigung und erstellt keine Korrekturmeldung.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Vor dem Einlesen der Zahlen bestätigen lassen:

- dass Steuer-Identifikationsnummer, Steuernummer und Aktenzeichen des
  Finanzamts entfernt sind – auch nicht maskiert, auch nicht als Kopfzeile eines
  UStVA-Ausdrucks oder eines Verprobungsprotokolls;
- dass der Mandant nur als Mandatskürzel geführt wird und Geschäftspartner, die
  in einer Kontobezeichnung oder in einer Belegliste auftauchen, konsistent
  maskiert sind (`Lieferant 1`, `Kunde EU 1`);
- dass vollständige Umsatzsteuer-Identifikationsnummern nicht mitgeschickt
  werden – für die Eingrenzung genügt das Länderkennzeichen.

Für die Verprobung genügen Branche, Zeitraum, Besteuerungsart, Kennzahlen mit
Beträgen und die Kontensalden mit Bezeichnung. Erscheint Zone-Rot-Material – eine
Steuernummer im Kopf des UStVA-Ausdrucks, ein Aktenzeichen in einer
Rückfrage des Finanzamts, eine vollständige IBAN in einer Kontobezeichnung, ein
Hinweis auf eine Selbstanzeige oder ein Steuerstrafverfahren –, sofort abbrechen,
den Fundort mit Zeile und Spalte nennen und den Anwender bitten, die Zahlen ohne
Kopfzeile und ohne diese Angabe neu einzufügen. Nicht selbst entfernen und
weiterarbeiten. Das gilt besonders, wenn die Abweichung aus einer bereits
übermittelten Voranmeldung stammt und der Vorgang in Richtung Selbstanzeige
laufen könnte: Dann endet die Arbeit im Werkzeug, und der Berufsträger übernimmt
außerhalb.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung
des Anbieters nach § 62a StBerG müssen vor dem Einsatz geklärt sein; § 62a StBerG
geht der DSGVO-Prüfung vor. Maßstab ist `DATENSCHUTZ.md`, Zone Rot.

## Ablauf

1. **Abweichung fassen – vor jeder Hypothese.** Betrag, betroffene Kennzahl oder
   betroffenes Konto, Richtung und Zeitraum festhalten. Ist nur bekannt, dass
   "etwas nicht stimmt", wird die Differenz zuerst aus den eingefügten Kennzahlen
   und Salden selbst ermittelt und dem Anwender zur Bestätigung vorgelegt, bevor
   Ursachen gesammelt werden. Ohne bezifferte Abweichung keine Ursachenliste –
   sonst entsteht eine Sammlung allgemeiner Fehlerquellen ohne Bezug zum Fall.

2. **Rahmen abfragen.** Besteuerungsart (Soll oder Ist), Kontenrahmen,
   Dauerfristverlängerung, Branche und die Besonderheiten des Zeitraums:
   § 13b-Fälle, innergemeinschaftliche Vorgänge, steuerfreie Umsätze,
   Vorsteueraufteilung, Umstellungen im Zeitraum. Die Besteuerungsart ist das
   Feld, ohne das die gesamte Kategorie der zeitlichen Abgrenzung nicht bewertbar
   ist – fehlt sie, anhalten und nachfragen, nicht aus dem Kontenbild
   rückschließen. Fehlen die Besonderheiten, wird ausdrücklich gefragt, statt aus
   dem Fehlen auf ihr Nichtvorliegen zu schließen.

3. **Vorperioden klären.** Trat die Abweichung erstmals auf oder besteht sie seit
   mehreren Zeiträumen, und ist der Betrag konstant oder wachsend? Die Antwort
   steuert die Sortierung der Ursachenliste in Schritt 6; sie wird erfragt, nicht
   aus einem einzelnen Zeitraum geraten. Liegen mehrere Zeiträume vor, wird die
   Abweichung je Zeitraum in einer Zeile geführt, damit der Verlauf sichtbar
   wird.

4. **Verprobung rechnen und Rechenweg zeigen.** Erwartete Umsatzsteuer aus den
   Erlöskonten je Steuersatz getrennt gegen die gemeldeten Kennzahlen, dazu
   Vorsteuer und die Kennzahlen der § 13b-Fälle, soweit die Zahlen es hergeben:
   Ausgangswert, Rechenschritt, Ergebnis. Der unerklärte Rest wird ausdrücklich
   beziffert, auch wenn er groß ist. Reichen die eingefügten Zahlen für eine
   Teilrechnung nicht aus, wird das benannt und die fehlende Auswertung genannt –
   es wird kein Wert geschätzt und kein Rest auf null gerechnet.

5. **Betragsmuster abgleichen.** Den Abweichungsbetrag gegen jeden eingefügten
   Kontensaldo halten, gegen den Steueranteil eines Bruttobetrags beim jeweils
   anwendbaren Steuersatz (Satz: für [JAHR] verifizieren) und gegen die Summe
   einzelner Kennzahlen. Ist die Differenz ohne Rest durch neun teilbar, ist das
   ein Hinweis auf eine Ziffernvertauschung – ein Hinweis, kein Beweis, und als
   solcher gekennzeichnet. Dieser Schritt ist reine Rechenarbeit über alle
   Zeilen und wird vollständig ausgeführt, nicht stichprobenweise; ein Treffer
   wird in Schritt 6 nach oben sortiert.

6. **Ursachenliste bilden.** Nach den Kategorien und der Mindestzahl aus
   Anforderung 1 der Prompt-Datei, sortiert nach Wahrscheinlichkeit für genau
   diese Konstellation. Keine Kategorie wird weggelassen: Passt eine für diesen
   Fall erkennbar nicht, steht sie mit der Begründung als unwahrscheinlich in der
   Liste, damit die Kanzlei sieht, dass sie bedacht wurde. Je Ursache der
   Prüfschritt, der sie in zehn Minuten bestätigt oder ausschließt – mit
   Auswertung, Filter und Vergleichsgröße, nicht als allgemeiner Hinweis.

7. **Prüfreihenfolge festlegen.** Die drei Schritte benennen, die den größten
   Teil der Abweichung am schnellsten aufklären, in der Reihenfolge der
   Ausführung und mit der erwarteten Wirkung je Schritt.

8. **Vermerk schreiben.** Interner Vermerk im Umfang der Prompt-Datei: Stand der
   Klärung, was geprüft wurde, was offen ist. Er ist so angelegt, dass er nach
   Abarbeitung der Prüfschritte ergänzt wird und den Klärungsstand über mehrere
   Sitzungen trägt. Jede rechtliche Aussage trägt ihre Fundstelle mit dem Zusatz
   "für [JAHR] verifizieren"; ist sie unsicher, "Fundstelle offen – bitte
   recherchieren". Jeder genannte Steuersatz und Grenzwert erhält den Zusatz
   "Wert für [JAHR] verifizieren", auch innerhalb der Verprobungsrechnung.

## Ergebnis

Eine Markdown-Datei `<Mandatskürzel>-ustva-abweichung-<JJJJ-MM>.md` im
Arbeitsordner des Mandats, benannt nach dem Voranmeldungszeitraum, aufgebaut nach
dem Ausgabeformat der Prompt-Datei: Verprobungsrechnung mit Rechenweg,
Ursachenliste als Tabelle mit Wahrscheinlichkeit und Prüfschritt, empfohlene
Prüfreihenfolge und interner Vermerk. Im Kopf stehen Zeitraum, Besteuerungsart,
Kontenrahmen, Dauerfristverlängerung, die bezifferte Abweichung mit Richtung und
der unerklärte Rest nach der Verprobung.

Jede Zeile der Ursachenliste bekommt eine Spalte für Erledigungsvermerk und
Handzeichen. Wird die Datei je Voranmeldungszeitraum neu angelegt, ergibt sich
aus den gleichnamigen Dateien eine Reihe: Eine Ursache, die drei Monate in Folge
oben steht und nie erledigt wird, ist selbst ein Befund und gehört in den
Vermerk.

## Qualitätssicherung

Kein Ergebnis verlässt die Kanzlei ohne menschliche Prüfung. Vor der Freigabe:

- Die Verprobungsrechnung vollständig nachrechnen, Gegenprobe in der Tabelle.
  Mehrstufige Beträge sind die bekannte Schwachstelle maschinellen Rechnens.
- Jede Kontonummer im Kontenplan des Mandanten nachschlagen, keine aus der
  Auswertung übernehmen; SKR03 und SKR04 werden hier regelmäßig verwechselt.
- Die gefundene Ursache im Programm belegen, bevor sie als geklärt gilt – die
  Liste nennt Hypothesen, der Nachweis kommt aus der Auswertung.
- Betrifft die Abweichung eine bereits übermittelte Voranmeldung, sind
  Korrekturpflicht und Anzeigepflicht gesondert und ausdrücklich zu prüfen. Eine
  Berichtigung nach § 153 AO entscheidet allein der Berufsträger; die Skill
  bereitet sie nicht vor und schlägt sie nicht vor.
- Vier-Augen-Prinzip: Eine zweite fachkundige Person zeichnet nach, dass
  Verprobung und Ursache nachvollziehbar sind. Die Freigabe für eine
  Korrekturmeldung oder eine Mitteilung an den Mandanten erteilt ein
  Berufsträger; sie ist zu dokumentieren.
- Alle Steuersätze, Grenzwerte und Fundstellen gegen eine Primärquelle prüfen.

Die Skill berechnet keine Fristen: weder Abgabetermine noch die Wirkung einer
Dauerfristverlängerung noch eine Berichtigungsfrist. Die Dauerfristverlängerung
ist für sie eine Rahmenangabe, die die Zuordnung eines Belegs zum Zeitraum
erklären kann – kein Terminrechner.

## Grundlage

Ursachenkategorien, Sachverhaltsbogen und Ausgabeformat stehen allein in der
Prompt-Datei:
[prompts/02-umsatzsteuer/05-ustva-abweichung-eingrenzen.md](../../../prompts/02-umsatzsteuer/05-ustva-abweichung-eingrenzen.md).
