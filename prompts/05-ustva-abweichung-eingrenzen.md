# 05 – UStVA-Abweichung zur Buchhaltung systematisch eingrenzen

**Problem:** Die Umsatzsteuer-Voranmeldung stimmt nicht mit den Konten überein, oder ein Vorjahresfehler wirkt nach. Die Ursachensuche kostet regelmäßig Stunden.
**Rolle:** Buchhaltung, Steuerberater
**DATEV-Bezug:** Kanzlei-Rechnungswesen, UStVA, Umsatzsteuer-Verprobung, Summen- und Saldenliste
**Was du bereitstellen musst:** UStVA-Werte je Kennzahl, Kontensalden der USt-/VSt-Konten und Erlöskonten, Zeitraum, Besteuerungsart.
**Datensparsamkeit:** Mandantenname und Steuernummer durch ein Kürzel ersetzen (`Mandant A`). Für die Verprobung genügen Branche, Besteuerungsart, Kennzahlen und Salden. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Prüfer für Umsatzsteuer-Verprobungen in einer deutschen Steuerkanzlei.
Du arbeitest hypothesengeleitet: erst mögliche Ursachen sammeln, dann nach
Wahrscheinlichkeit und Prüfaufwand sortieren, dann konkrete Prüfschritte nennen.

AUFGABE
Grenze die Ursache der folgenden Abweichung zwischen Buchhaltung und
Umsatzsteuer-Voranmeldung ein.

RAHMEN
- Mandant / Branche: [MANDANT]
- Zeitraum: [MONAT/QUARTAL JAHR]
- Besteuerungsart: [Soll / Ist]
- Kontenrahmen: [SKR03 / SKR04]
- Dauerfristverlängerung: [ja/nein]
- Besonderheiten: [z. B. § 13b-Fälle, i.g. Lieferungen, steuerfreie Umsätze,
  Vorsteueraufteilung, Umstellung im Zeitraum]

ZAHLEN
- UStVA-Kennzahlen (Kz und Betrag):
  [z. B. Kz 81: … / Kz 86: … / Kz 66: … / Kz 46: … / Kz 89: …]
- Kontensalden laut Buchhaltung (Konto, Bezeichnung, Saldo):
  [LISTE]
- Konkrete Abweichung: [BETRAG] in [Kennzahl/Konto], Richtung [zu hoch/zu niedrig]
- Vorperioden: [Abweichung trat erstmals auf / besteht seit …]

ANFORDERUNGEN
1. Erstelle eine URSACHENLISTE mit mindestens 10 Kandidaten, sortiert nach
   Wahrscheinlichkeit für genau diese Konstellation. Beispiele für Kategorien,
   die du abdecken sollst:
   - Zeitliche Abgrenzung (Buchung im falschen Voranmeldungszeitraum,
     Ist-/Soll-Versteuerung, Anzahlungen)
   - Falscher Steuerschlüssel / manuelle Umsatzsteuerbuchung ohne Automatik
   - § 13b-Fälle nicht oder doppelt erfasst
   - Vorsteuer aus nicht ordnungsgemäßer Rechnung
   - Nicht steuerbare oder steuerfreie Umsätze auf falschem Erlöskonto
   - Korrekturen und Stornos über Periodengrenzen
   - Berichtigung nach § 17 UStG (Forderungsausfall, Skonto, Rabatt,
     Storno-/Korrekturrechnung – nicht "Gutschrift" i. S. d. § 14 Abs. 2 UStG)
   - Vorjahresfehler, der im laufenden Jahr wirkt
   - Umbuchungen nach Übermittlung der UStVA
   - Rundungs- und Aufteilungsdifferenzen bei Vorsteueraufteilung
2. Gib zu jeder Ursache an: WIE man sie in zehn Minuten prüft
   (welche Auswertung, welcher Filter, welcher Vergleich).
3. Nenne die drei Prüfschritte, mit denen man den größten Teil der
   Abweichung am schnellsten aufklärt – in der Reihenfolge, in der man sie
   durchführen soll.
4. Rechne, soweit die Zahlen es hergeben, eine Verprobung: erwartete
   Umsatzsteuer aus den Erlöskonten gegen gemeldete Umsatzsteuer, und
   benenne den unerklärten Rest.
5. Formuliere zum Schluss einen kurzen internen Vermerk (max. 8 Zeilen),
   der den Stand der Klärung dokumentiert.
6. Wenn der Betrag der Abweichung auf einen typischen Fehler hindeutet
   (z. B. exakt der Steueranteil eines Bruttobetrags beim jeweils
   anwendbaren Steuersatz – Satz: für [JAHR] verifizieren –,
   exakt der Saldo eines Kontos, Zahlendreher), weise ausdrücklich darauf hin.
7. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".

AUSGABEFORMAT
1. Verprobungsrechnung  2. Ursachenliste (Tabelle: Ursache | Wahrscheinlichkeit |
Prüfschritt)  3. Empfohlene Prüfreihenfolge  4. Interner Vermerk
```

## Anwendung

1. UStVA-Werte und Kontensalden aus DATEV exportieren, Mandantenbezug maskieren.
2. Prompt ausführen, die drei empfohlenen Prüfschritte im Programm abarbeiten.
3. Ergebnis in den vorgeschlagenen Vermerk eintragen und zur Akte nehmen.

## Qualitätssicherung

- Die Verprobungsrechnung selbst nachrechnen – Rechenfehler von Sprachmodellen sind bei mehrstufigen Beträgen möglich. Alternativ: Zahlen in Excel gegenrechnen.
- Keine Berichtigung nach § 153 AO ohne Entscheidung des Berufsträgers.
- Wenn die Abweichung eine bereits übermittelte Voranmeldung betrifft: Korrekturpflicht und Anzeigepflicht gesondert prüfen.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person muss die Verprobungsrechnung und die gefundene Ursache nachvollziehen. Die Freigabe für eine Korrekturmeldung oder eine Mitteilung an den Mandanten erteilt ein Berufsträger; die Freigabe ist zu dokumentieren.

## Varianten

- **Jahresverprobung:** Zeitraum auf das Wirtschaftsjahr ausdehnen, Zusatz "Berücksichtige Abweichungen zwischen UStVA-Summe und Jahreserklärung."
- **Vorjahresfehler:** Zusatz "Erstelle zusätzlich einen Vorschlag, in welchem Zeitraum die Korrektur zu erfassen ist und welche Meldungen betroffen sind – als Prüfvorschlag, nicht als Entscheidung."
- **Wiederkehrend:** "Leite aus der gefundenen Ursache eine Arbeitsanweisung ab, die den Fehler künftig verhindert."
