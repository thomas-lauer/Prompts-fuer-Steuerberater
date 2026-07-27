# 20 – Summen- und Saldenliste auf Auffälligkeiten prüfen

**Problem:** Kontierungsfehler fallen erst beim Jahresabschluss auf, obwohl sie in der Summen- und Saldenliste seit Monaten sichtbar waren.
**Rolle:** Buchhaltung, Bilanzbuchhalter, Steuerberater
**DATEV-Bezug:** Kanzlei-Rechnungswesen (Summen- und Saldenliste, Sachkontenübersicht), Auswertung vor Abschluss und vor Übermittlung der UStVA
**Was du bereitstellen musst:** SuSa-Export mit Konto, Kontenbezeichnung, Eröffnungsbilanzwert, Verkehrszahlen Soll/Haben, Saldo; Vorjahreswerte zum selben Stichtag, soweit vorhanden; Rechtsform und Kontenrahmen.
**Datensparsamkeit:** Mandantenname, Steuernummer und Beraternummer entfernen. Personenkonten nur als Summe oder maskiert einfügen (`Debitor 1`). Für die Prüfung genügen Kontonummer, Bezeichnung, Saldo und Vorjahreswert.
Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du bist Bilanzbuchhalter in einer deutschen Steuerkanzlei und prüfst eine
Summen- und Saldenliste vor dem Abschluss. Du arbeitest nach festem Prüfraster
und begründest jede Auffälligkeit aus der Liste selbst – du behauptest keinen
Fehler, den du nicht an einer Zahl festmachen kannst.

AUFGABE
Prüfe die folgende Summen- und Saldenliste auf Auffälligkeiten und gib zu jeder
Auffälligkeit einen konkreten Prüfschritt an.

RAHMEN
- Mandant / Branche: [MANDANT / BRANCHE]
- Rechtsform: [Einzelunternehmen / GbR / GmbH / UG / GmbH & Co. KG / …]
- Gewinnermittlung: [Bilanz / EÜR]
- Kontenrahmen: [SKR03 / SKR04]
- Umsatzsteuer: [Regelbesteuerung / Kleinunternehmer § 19 UStG /
  teilweise steuerfrei], Besteuerungsart: [Soll / Ist]
- Stichtag / Zeitraum: [ZEITRAUM]
- Prüfanlass: [vor Jahresabschluss / vor UStVA / laufende Kontrolle]
- Besonderheiten: [z. B. Betriebsaufspaltung, Gesellschafterdarlehen,
  Kontenrahmenwechsel zum Wirtschaftsjahresbeginn im Prüfzeitraum]

DATEN
Summen- und Saldenliste (Konto | Bezeichnung | Soll | Haben | Saldo |
Vorjahressaldo zum selben Stichtag):
[LISTE EINFÜGEN]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Vorzeichenprüfung: Konten mit einem Saldo, der ihrer Kontenart
   widerspricht (Aktivkonto im Haben, Erlöskonto im Soll, negativer
   Kassenbestand, Bankkonto mit unerwartetem Vorzeichen, Verbindlichkeit im
   Soll). Ein negativer Kassenbestand ist immer ein Befund, kein Rundungsthema.
2. Verrechnungs-, Interims- und Zwischenkonten mit Saldo ungleich null –
   einschließlich Geldtransit, unklarer Posten, Verrechnungskonto Lohn,
   Fragen-an-den-Mandanten-Konto.
3. Rechtsformwidrige Konten: Privatentnahmen, Privateinlagen und
   Privatsteuern bei einer Kapitalgesellschaft; Gesellschafterkonten bei einem
   Einzelunternehmen; Konten für Gewinnermittlungsarten, die hier nicht gelten.
4. Pflichtkonten ohne Bewegung: Konten, die bei dieser Rechtsform, Branche und
   Besteuerungsart erwartbar bebucht wären und keinen Umsatz zeigen
   (z. B. Abschreibungen, Umsatzsteuervorauszahlungen, Personalaufwand bei
   vorhandenen Arbeitnehmern). Formuliere als Frage, nicht als Feststellung.
5. Sammel- und Auffangkonten mit auffälliger Höhe: sonstige betriebliche
   Aufwendungen, sonstige Erträge, durchlaufende Posten, Konten ohne
   sprechende Bezeichnung. Auffällig ist ein Anteil, der im Verhältnis zur
   Kontengruppe aus dem Rahmen fällt – nenne das Verhältnis.
6. Vorjahresvergleich: Abweichung über [PROZENT] Prozent oder über [BETRAG]
   zum Vorjahresstichtag; Konten, die im Vorjahr bebucht waren und jetzt leer
   sind, und umgekehrt.
7. Verhältniskennzahlen, soweit die Liste sie hergibt: Wareneinsatz zu Erlösen,
   Personalaufwand zu Erlösen, Umsatzsteuerkonten zu den zugehörigen
   Erlöskonten (rechnerische Verprobung je Steuersatz), Vorsteuer zu
   Aufwandsvolumen. Nenne die Rechnung, nicht nur das Ergebnis.
8. Rundungsauffälligkeiten: auffällig viele glatte Beträge, sich wiederholende
   identische Salden, Salden exakt in Höhe eines anderen Kontos
   (Hinweis auf Doppelbuchung oder falsches Gegenkonto), Zahlendreher-Muster.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: Was ist aus der Liste
   entscheidbar, was nicht, welche Angaben fehlen?
2. Höchstens 15 Auffälligkeiten. Sortiere nach Risiko (Auswirkung auf Steuer,
   Bilanzansatz oder UStVA mal Wahrscheinlichkeit), nicht nach Kontonummer.
   Lasse alles weg, was nur formal auffällt und keine Folge hat.
3. Nenne zu jeder Auffälligkeit: betroffene Position, Beobachtung mit Zahl,
   Vermutung (ausdrücklich als Vermutung gekennzeichnet), Prüfschritt mit der
   Auswertung, in der man ihn durchführt, und geschätzten Zeitbedarf.
4. Sprich Konten über ihre BEZEICHNUNG und Funktion an. Wenn du eine
   Kontonummer nennst, kennzeichne sie mit "(Kontonummer im Kontenplan des
   Mandanten nachschlagen – nicht übernehmen)". Kontonummern unterscheiden sich
   je Kontenrahmen und je individuellem Kontenplan.
5. Kennzeichne jeden Steuersatz, Grenzwert und Schwellenbetrag mit "Wert – für
   [JAHR] verifizieren".
6. Prüfe die Summenkontrolle nur, wenn die eingefügte Liste vollständig ist
   (alle Sach- und Personenkonten, mit Vortragswerten). Frage zuerst danach. Ist
   die Liste ausschnittweise, verdichtet oder ohne Personenkonten eingefügt,
   schreibe "Summenkontrolle nicht durchführbar – in der vollständigen Liste im
   Programm prüfen" und leite daraus KEINEN Befund ab. Nur bei vollständiger
   Liste: Weichen Soll- und Habensumme voneinander ab, ist das der erste und
   wichtigste Befund.
7. Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Kannst du sie nicht angeben, kennzeichne die Aussage
   als "ohne Fundstelle – vor Verwendung belegen". Erfinde keine Paragrafen,
   BMF-Schreiben oder Dokumentnummern; unsichere: "Fundstelle offen – bitte
   recherchieren".

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Auffälligkeitenliste (Rang | Position | Beobachtung mit Zahl | Vermutung |
   Prüfschritt | Auswertung | Zeitbedarf)
3. Verprobungsrechnungen (Rechenweg sichtbar)
4. Fragen an den Mandanten
5. Interne Notiz (was vor Abschluss zwingend geklärt sein muss)
6. Was ich nicht sicher weiß
```

## Anwendung

1. SuSa zum Stichtag mit Vorjahresspalte exportieren, Mandantenbezug entfernen.
2. Prompt ausführen, die Auffälligkeitenliste als Arbeitsliste ausdrucken und abarbeiten.
3. Vor der UStVA nur die Ränge mit Umsatzsteuerbezug abarbeiten, den Rest zum Abschluss.
4. Geklärte Positionen mit Begründung in der Handakte dokumentieren.

## Qualitätssicherung

- **Kontonummern nicht aus der KI-Antwort übernehmen.** Jede Nummer im Kontenplan des Mandanten nachschlagen. Das Modell verwechselt SKR03 und SKR04 und erfindet plausible, aber falsche Nummern – das ist die häufigste Fehlerart bei dieser Auswertung.
- Jede Verprobungsrechnung selbst nachrechnen; mehrstufige Beträge sind eine bekannte Fehlerquelle. Gegenprobe in Excel.
- Ein vom Modell nicht genannter Fehler ist nicht ausgeschlossen: Die Liste ersetzt keine Abschlussprüfung und keine Kontenklärung.
- Vier-Augen-Prinzip und Freigabe: Vor der Abschlussfreigabe prüft eine zweite Person die Auffälligkeitenliste und zeichnet ab, dass jede Position geklärt oder bewusst verworfen wurde. Die Freigabe erteilt ein Berufsträger; bei Bilanzansätzen entscheidet er selbst. Die Freigabe ist zu dokumentieren.
- Alle genannten Grenzwerte, Steuersätze und Fundstellen gegen eine Primärquelle verifizieren.

## Varianten

- **Nur Umsatzsteuer:** Zusatz "Beschränke dich auf Konten mit Umsatzsteuerbezug und prüfe die Verprobung je Steuersatz." Ergänzt Prompt 05.
- **Monatsroutine:** Zusatz "Vergleiche mit dem Vormonat statt mit dem Vorjahr und nenne nur neue Auffälligkeiten."
- **Mandatsübernahme:** Zusatz "Kennzeichne Auffälligkeiten, die auf abweichende Kontierungsgewohnheiten des Vorberaters hindeuten." Ergänzt Prompt 22.
