---
name: summen-salden-pruefen
description: Liest eine exportierte Summen- und Saldenliste, rechnet Summenkontrolle,
  Vorjahresvergleich und Verhältniskennzahlen selbst und legt daraus eine nach Risiko
  sortierte Auffälligkeitenliste mit Prüfschritten an. Klärt vorab die Vollständigkeit
  der Liste und fordert Rechtsform, Gewinnermittlung und Besteuerungsart nach, weil
  einzelne Prüfschritte erst dadurch anwendbar werden. Use when a trial balance (SuSa)
  export has to be screened before a year-end close, a VAT return or as monthly control.
---

# 20 – Summen- und Saldenliste auf Auffälligkeiten prüfen

## Zweck

Der Prompt beschreibt das Prüfraster. Diese Skill wendet es auf den Export an:
Sie geht die Kontenzeilen durch, prüft je Zeile Vorzeichen und Kontenart, rechnet
Vorjahresabweichungen, bildet die Verhältniskennzahlen mit sichtbarem Rechenweg
und führt – sofern zulässig – die Summenkontrolle über Soll und Haben aus. Am
Ende steht eine Arbeitsliste, keine Vorgehensbeschreibung. Der Mengenvorteil
liegt in der Kontenzahl, und viele Befunde entstehen erst aus dem Vergleich
mehrerer Zeilen miteinander.

## Wann einsetzen – und wann nicht

Einsetzen, wenn ein SuSa-Export zu einem Stichtag vorliegt – vor dem Abschluss,
vor Übermittlung der Umsatzsteuer-Voranmeldung oder als Monatskontrolle.

Nicht einsetzen, wenn die Abweichung zwischen Voranmeldung und Buchhaltung schon
bekannt ist und nur noch eingegrenzt werden soll: Dafür ist Prompt 05 gemacht,
der die UStVA-Werte je Kennzahl neben die Salden der Umsatzsteuer-, Vorsteuer-
und Erlöskonten stellt. Für die Plausibilität der EÜR-Positionen mit
Anlagenverzeichnis, Kfz und Privatanteilen ist Prompt 21 der Einstieg; für die
Überführung eines Vorberater-Kontenplans in den eigenen Kontenrahmen Prompt 22,
der Zielkontenrahmen und Überleitungsliste abfragt. Altersstruktur und
Ausfallrisiko einzelner Forderungen gehören zu Prompt 18, doppelt erfasste
Buchungen und doppelt angelegte Personenkonten zu Prompt 19. Diese Skill ersetzt
keine Abschlussprüfung und keine Kontenklärung.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Vor dem Einlesen des Exports bestätigen lassen:

- dass Steuer-Identifikationsnummer, Steuernummer und Aktenzeichen des Finanzamts
  entfernt sind – auch nicht maskiert, auch nicht in Kopfzeilen oder Ausschnitten;
- dass Mandantenname und Beraternummer entfernt sind und der Mandant nur als
  Mandatskürzel geführt wird;
- dass Personenkonten maskiert, aber zeilenweise enthalten sind (`Debitor 1`,
  `Kreditor 1`), konsistent über alle Zeilen hinweg. Nur so bleibt die
  Summenkontrolle möglich; eine auf einen Sammelsaldo verdichtete
  Personenkontenspalte macht die Liste unvollständig im Sinne von Schritt 1 des
  Ablaufs und sperrt die Summenkontrolle. Wer verdichten muss, wird darauf vor
  dem Einlesen hingewiesen.

Für die Prüfung genügen Kontonummer, Bezeichnung, Verkehrszahlen, Saldo und
Vorjahreswert. Erscheint Zone-Rot-Material – eine Steuernummer in der
Exportkopfzeile, ein Aktenzeichen in einer Bemerkungsspalte, ein Hinweis auf ein
Steuerstrafverfahren oder eine Selbstanzeige –, sofort abbrechen, den Fundort mit
Zeile und Spalte nennen und den Anwender bitten, den Export ohne Kopfzeile und
ohne diese Spalte neu zu ziehen. Nicht selbst entfernen und weiterarbeiten.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung
des Anbieters nach § 62a StBerG müssen vor dem Einsatz geklärt sein; § 62a StBerG
geht der DSGVO-Prüfung vor. Maßstab ist `DATENSCHUTZ.md`, Zone Rot.

## Ablauf

1. **Vollständigkeit der Liste klären – vor jeder Rechnung.** Ausdrücklich
   fragen: Enthält der Export alle Sach- und Personenkonten einschließlich der
   Vortragswerte, oder ist er ausschnittweise, verdichtet oder ohne
   Personenkonten eingefügt? Die Frage steht am Anfang und wird nicht aus der
   Zeilenzahl geraten. Ist die Liste unvollständig, unterbleibt die
   Summenkontrolle, aus einer Soll-Haben-Differenz wird kein Befund abgeleitet,
   und es gilt der Vermerk des Prompts (Anforderung 6), dass sie im Programm an
   der vollständigen Liste zu erfolgen hat. Gesperrt ist damit nur die
   Summenkontrolle, nicht die Prüfung: Die übrigen Schritte des Prüfrasters
   werden auf dem Ausschnitt normal abgearbeitet, jeder Befund erhält aber den
   Zusatz "auf Ausschnitt festgestellt – an der vollständigen Liste im Programm
   zu bestätigen", und aus dem Fehlen eines Kontos wird kein Befund abgeleitet.

2. **Rahmen abfragen.** Branche, Rechtsform, Gewinnermittlung (Bilanz oder EÜR),
   Kontenrahmen, Umsatzsteuerstatus und Besteuerungsart (Soll oder Ist), Stichtag
   und Zeitraum, Prüfanlass, Besonderheiten wie Betriebsaufspaltung,
   Gesellschafterdarlehen oder Kontenrahmenwechsel. Rechtsform, Gewinnermittlung
   und Besteuerungsart schalten Prüfschritte frei: Ohne sie ist nicht
   entscheidbar, ob ein Privatkonto rechtsformwidrig ist, welche Konten geführt
   werden dürfen und welche Umsatzsteuerkonten erwartbar bebucht sind. Fehlt eine
   der drei, anhalten und nachfragen – nicht aus dem Kontenbild rückschließen.

3. **Eindeutigkeit einschätzen.** Vor dem ersten Befund festhalten, was aus der
   Liste entscheidbar ist und was fehlt. Ohne Vorjahresspalte entfällt der
   Vorjahresvergleich – vermerken, nicht durch Schätzwerte ersetzen.

4. **Zeilenweise durch das Prüfraster.** Die Prüfschritte 1 bis 8 der
   Prompt-Datei (Abschnitt "PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT
   FEST") in deren Reihenfolge abarbeiten und jeden Schritt mit seinem Ergebnis
   festhalten, auch wenn es "ohne Befund" lautet. Die Schritte werden aus der
   Prompt-Datei gelesen, nicht aus dieser Skill. Prozentsatz und Betragsgrenze
   des Vorjahresvergleichs beim Anwender erfragen, nicht setzen.

5. **Rechnen und Rechenweg zeigen.** Verhältniskennzahlen und die Verprobung der
   Umsatzsteuerkonten je Steuersatz werden ausgerechnet, nicht beschrieben:
   Zähler, Nenner, Ergebnis. Bei der Summenkontrolle – nur bei vollständiger
   Liste – Soll- und Habensumme gegenüberstellen; eine Abweichung ist der erste
   und wichtigste Befund.

6. **Auffälligkeiten sortieren und begrenzen.** Nach Risiko ordnen, nicht nach
   Kontonummer, auf die im Prompt genannte Höchstzahl kürzen, rein Formales
   weglassen. Je Position: Beobachtung mit Zahl, gekennzeichnete Vermutung,
   Prüfschritt samt Auswertung und Zeitbedarf. Konten über ihre Bezeichnung
   ansprechen, Kontonummern nur mit dem Nachschlagevermerk des Prompts.

7. **Ergebnis schreiben.** Fragen an den Mandanten und interne Notiz getrennt
   halten. Jede rechtliche Aussage trägt Norm (Absatz und Satz), Richtlinie oder
   BMF-Schreiben mit Datum und den wörtlichen Zusatz "für [JAHR] verifizieren";
   ist die Fundstelle unsicher, "Fundstelle offen – bitte recherchieren", ist sie
   nicht angebbar, "ohne Fundstelle – vor Verwendung belegen". Jeder genannte
   Steuersatz, Grenzwert und Schwellenbetrag erhält zusätzlich den Zusatz "Wert –
   für [JAHR] verifizieren", auch in den Verprobungsrechnungen.

## Ergebnis

Eine Markdown-Datei `<Mandatskürzel>-susa-auffaelligkeiten-<JJJJ-MM>.md` im
Arbeitsordner des Mandats, aufgebaut nach dem Ausgabeformat der Prompt-Datei:
Eindeutigkeit und Datenlage, nach Rang sortierte Auffälligkeitenliste,
Verprobungsrechnungen mit Rechenweg, Fragen an den Mandanten, interne Notiz und
unsichere Punkte. Im Kopf stehen Stichtag, Rechtsform, Gewinnermittlung,
Besteuerungsart, Kontenrahmen und die beantwortete Vollständigkeitsfrage samt
Angabe, ob die Summenkontrolle durchgeführt wurde. Jede Zeile der
Auffälligkeitenliste bekommt eine Spalte für Erledigungsvermerk und Handzeichen,
damit sie über mehrere Sitzungen fortgeschrieben werden kann.

## Qualitätssicherung

Kein Ergebnis verlässt die Kanzlei ohne menschliche Prüfung. Vor der Freigabe:

- Jede Kontonummer im Kontenplan des Mandanten nachschlagen, keine aus der
  Auswertung übernehmen; die Verwechslung von SKR03 und SKR04 ist die häufigste
  Fehlerart dieser Prüfung.
- Jede Verprobungsrechnung selbst nachrechnen, Gegenprobe in der Tabelle.
- Ein nicht genannter Fehler ist nicht ausgeschlossen; die Liste ersetzt weder
  Abschlussprüfung noch Kontenklärung.
- Eine zweite Person prüft vor der Abschlussfreigabe die Auffälligkeitenliste und
  zeichnet ab, dass jede Position geklärt oder bewusst verworfen wurde. Die
  Freigabe erteilt ein Berufsträger, bei Bilanzansätzen entscheidet er selbst;
  sie ist zu dokumentieren.
- Alle Grenzwerte, Steuersätze und Fundstellen gegen eine Primärquelle prüfen.

Die Skill berechnet keine Fristen: weder Abgabe- noch Berichtigungsfristen, und
keine Aussage dazu, bis wann ein Befund korrigiert sein muss. Sie benennt den
Prüfschritt, nicht den Termin.

## Grundlage

Prüfraster, Sachverhaltsbogen und Ausgabeformat stehen allein in der Prompt-Datei:
[prompts/01-finanzbuchhaltung/20-summen-salden-pruefen.md](../../../prompts/01-finanzbuchhaltung/20-summen-salden-pruefen.md).
