# 28 – Vier-Augen-Prüfroutine für OCR-erfasste Belege

**Problem:** Die Belegerkennung schlägt falsche Kreditoren, Beträge oder Daten vor; die Fehler werden übersehen, weil der Buchungsvorschlag plausibel aussieht und nur noch bestätigt wird.
**Rolle:** Buchhaltung, Teamleitung Finanzbuchhaltung, Qualitätsmanagement
**DATEV-Bezug:** DATEV Unternehmen online (Belegerkennung), Belegwesen online, DATEV Kanzlei-Rechnungswesen, Buchungsstapel-Export im DATEV-Format (CSV) – Bezeichnung im eingesetzten Programmstand verifizieren
**Was du bereitstellen musst:** Belegkreis und Mandantenstruktur, eingesetzter Erfassungsweg, bisher aufgefallene Fehlerbilder; für Teil 2 ein Buchungsstapel-Export ohne Klarnamen.
**Datensparsamkeit:** Kreditorennamen durch `Lieferant 1` ersetzen, Bankverbindungen auf `Konto ****1234` kürzen, Mandantenname und Steuernummer entfernen. Für die Auffälligkeitsprüfung genügen Konto, Betrag, Steuerschlüssel, Datum und Belegnummer. Personenbezogene Verwendungszwecke (Löhne, Unterhalt) vorher aussortieren. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

### Teil 1 – Prüfroutine erzeugen

```text
Du bist Teamleiter Finanzbuchhaltung in einer deutschen Steuerkanzlei.
Du entwirfst Kontrollen so, dass sie im Tagesgeschäft tatsächlich
durchgehalten werden: wenige Pflichtfelder, klare Stichprobenregel.

AUFGABE
Erstelle eine Vier-Augen-Prüfroutine für Belege, die über die
Belegerkennung erfasst und als Buchungsvorschlag übernommen werden.

RAHMEN
- Mandant / Belegkreis: [MANDANT], [EINGANGSRECHNUNGEN / KASSE / AUSGANGSRECHNUNGEN]
- Belege pro Monat: [ZAHL]
- Erfassungsweg: [DATEV Unternehmen online / Belegtransfer / Scanner Kanzlei]
- Kontenrahmen: [SKR03 / SKR04]
- Besonderheiten: [z. B. viele gemischte Steuersätze, Skonto, Auslandsrechnungen]
- Bisher aufgefallene Fehler: [FEHLERBILDER]

ANFORDERUNGEN
1. Trenne die Felder in drei Gruppen:
   (IMMER PRÜFEN) – bei jedem Beleg, ohne Ausnahme:
   Rechnungsbetrag, ausgewiesener Steuerbetrag, Steuersatz/Steuerschlüssel,
   Leistungs- bzw. Lieferdatum, Kreditor, Rechnungsnummer.
   (STICHPROBE) – mit ausdrücklicher Regel, z. B. jeder n-te Beleg oder alle
   Belege über [BETRAGSGRENZE].
   (SYSTEMSEITIG) – was das Programm selbst absichert.
2. Nenne je Feld in einem Halbsatz, WORAN der Fehler erkennbar ist.
3. Beschreibe die typischen Fehlermuster der Belegerkennung, mindestens:
   Zahlendreher im Betrag; Rechnungsdatum als Leistungsdatum übernommen;
   falscher Kreditor bei ähnlich lautenden Namen oder Doppelanlagen;
   Bruttobetrag im Nettofeld; falscher Steuersatz bei gemischten Belegen
   (zwei Steuersätze auf einem Bon); Skontoabzug fehlt oder doppelt.
   Ergänze weitere, die zum genannten Rahmen passen.
4. Lege Freigabestufen fest: Wer erfasst, wer prüft, wer gibt frei, ab
   welcher Fallgruppe ist ein Berufsträger einzubinden. Das
   Vier-Augen-Prinzip muss ausdrücklich benannt sein.
5. Nenne KEINE Betragsgrenzen, Steuersätze oder Fristen als feststehend.
   Kennzeichne sie als "Wert – für [JAHR] verifizieren" oder als
   kanzleiseitig festzulegen. Erfinde keine Paragrafen; unsichere
   Fundstellen kennzeichnest du mit "Fundstelle – für [JAHR] verifizieren".

AUSGABEFORMAT
1. Prüfroutine als abhakbare Checkliste (Kästchen ☐), gegliedert nach
   (IMMER PRÜFEN) / (STICHPROBE) / (SYSTEMSEITIG)
2. Tabelle "Typische Fehlermuster": Fehlermuster | Woran erkennbar | Sofortmaßnahme
3. Freigabestufen als Tabelle: Fallgruppe | Erfassung | Prüfung | Freigabe
4. Interne Notiz: was die Kanzlei festlegen muss, bevor die Routine gilt
5. Was ich nicht sicher weiß
```

### Teil 2 – Buchungsstapel auf Auffälligkeiten prüfen

```text
Du bist Bilanzbuchhalter und prüfst einen maschinell erzeugten
Buchungsstapel auf Auffälligkeiten. Du behauptest keine Fehler, sondern
benennst Verdachtsmomente mit dem Kriterium, an dem sie sich klären.

DATEN (anonymisiert, Spalten: Belegdatum, Leistungsdatum, Belegnummer,
Kreditor, Sollkonto, Habenkonto, Betrag, Steuerschlüssel, Buchungstext)
[STAPEL EINFÜGEN]

RAHMEN
- Kontenrahmen: [SKR03 / SKR04], Zeitraum: [ZEITRAUM]
- Branche des Mandanten: [BRANCHE]

ANFORDERUNGEN
1. Prüfe auf: doppelte Belegnummern; identische Beträge desselben Kreditors
   im Zeitraum; Betrag und Steuerbetrag rechnerisch unstimmig;
   Steuerschlüssel unpassend zum Konto; Leistungsdatum fehlt oder gleicht
   dem Belegdatum bei Jahreswechselbelegen; auffällig runde Beträge;
   Ausreißer beim selben Kreditor; ähnlich lautende Kreditoren.
2. Nenne HÖCHSTENS 15 Auffälligkeiten. Sortiere nach Risiko, nicht nach
   Zeile. Ignoriere den Rest bewusst.
3. Formuliere jede Aussage als Verdacht, solange sie nicht rechnerisch aus
   den Daten folgt. Rechnerische Unstimmigkeiten kennzeichnest du als solche.
4. Rechne nichts hoch und ergänze keine Werte, die nicht in den Daten stehen.

AUSGABEFORMAT
Tabelle: Zeile | Auffälligkeit | Verdacht oder rechnerisch belegt |
Was zu prüfen ist | Erledigt (leer)
Darunter: "Interne Notiz" und "Was ich nicht sicher weiß".
```

## Anwendung

1. Teil 1 einmal je Belegkreis erzeugen, kürzen und als Kanzleivorgabe verabschieden – eine Checkliste mit mehr als 12 Pflichtpunkten wird nicht angewandt.
2. Stichprobenregel und Betragsgrenzen selbst festlegen; das Modell kennt die Risikolage nicht.
3. Teil 2 vor der Festschreibung anwenden, nicht danach.
4. Wiederholte Fehler an derselben Belegart sind ein Erfassungsproblem, kein Prüfproblem – dann greift Prompt 27.

## Qualitätssicherung

- **Beide Teile liefern Entwürfe.** Die Prüfroutine gilt erst, wenn eine zweite Person sie gegengelesen hat und die Kanzleileitung sie verabschiedet; Fallgruppen, in denen ein Berufsträger freigeben muss, legt ein Berufsträger fest, nicht das Modell (Freigabestufe 3 in `DATENSCHUTZ.md`).
- Die Auffälligkeitenliste ist eine Vorauswahl, kein Prüfergebnis. Jede Zeile wird am Originalbeleg geklärt.
- Ein unauffälliger Stapel ist nicht geprüft, sondern nur unauffällig. Die Pflichtfelder aus Teil 1 bleiben unabhängig davon zu prüfen.
- Der Vorsteuerabzug hängt an der formellen Rechnung, nicht am erkannten Datensatz. Bei Beanstandungen den Beleg selbst gegen die Pflichtangaben prüfen.
- Vor dem Einfügen prüfen, ob der Export tatsächlich anonymisiert ist – Buchungstexte enthalten häufig Klarnamen.

## Varianten

- **Kassenbelege:** Zusatz "Ergänze Prüfpunkte für Barbelege: Kassensturzfähigkeit, negative Kassenbestände, Bewirtungsangaben."
- **Jahreswechsel:** "Prüfe zusätzlich auf periodenfremde Buchungen und fehlende Abgrenzung."
- **Neuer Mandant:** "Liste die 10 Kreditoren mit dem höchsten Volumen und markiere mögliche Doppelanlagen."
