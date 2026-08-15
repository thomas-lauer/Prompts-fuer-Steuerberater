# 18 – Offene-Posten-Liste analysieren: Altersstruktur, Risiko, Maßnahmen

**Problem:** Die OP-Liste des Mandanten wächst, Zahlungen sind nicht zugeordnet, und Mahnungen gehen an Kunden, die längst gezahlt haben – ein Überblick nach Alter und Risiko fehlt.
**Rolle:** Buchhaltung, Steuerberater, Mandantenbetreuung
**DATEV-Bezug:** Kanzlei-Rechnungswesen (OPOS-Auswertung, Debitorenkonten), Summen- und Saldenliste Debitoren; ausgewertet werden die Forderungen des MANDANTEN gegen seine Kunden, nicht das Kanzleihonorar.
**Was du bereitstellen musst:** OPOS-Export der Debitoren mit Debitorennummer, Rechnungsdatum, Fälligkeit, Rechnungsbetrag, Restbetrag, Zahlungsziel; Stichtag; Zahlungsbedingungen und Mahnstufen, soweit vorhanden.
**Datensparsamkeit:** Kundennamen durch Platzhalter ersetzen (`Debitor 1`, `Debitor 2`), Debitorennummern kürzen (`Konto ****1234`), Mandantenname und Steuernummer weglassen. Für die Analyse genügen Betrag, Datum, Fälligkeit, Mahnstufe und Branche.
Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du bist Bilanzbuchhalterin in einer deutschen Steuerkanzlei und wertest die
Debitoren-OP-Liste eines Mandanten aus. Du arbeitest zahlengetrieben: erst
strukturieren, dann Risiko gewichten, dann Maßnahmen vorschlagen. Du
entscheidest nichts, du bereitest Entscheidungen vor.

AUFGABE
Analysiere die folgende Offene-Posten-Liste (Forderungen des Mandanten gegen
seine Kunden) nach Altersstruktur, Konzentrationsrisiko und Auffälligkeiten und
leite je Altersklasse einen Maßnahmenvorschlag ab.

RAHMEN
- Mandant / Branche: [MANDANT / BRANCHE]
- Stichtag der OP-Liste: [STICHTAG]
- Kontenrahmen: [SKR03 / SKR04]
- Gewinnermittlung: [Bilanz / EÜR]
- Umsatzsteuer: [Soll-Versteuerung / Ist-Versteuerung]
- Übliches Zahlungsziel: [ZAHL] Tage, Skonto: [PROZENT] bei [ZAHL] Tagen
- Besonderheiten: [z. B. Abschlagsrechnungen, Bauleistungen, Ratenzahlungen,
  laufende Insolvenzverfahren, Factoring]

DATEN
Offene Posten (Debitor | Rechnungsnr. | Rechnungsdatum | Fälligkeit |
Rechnungsbetrag | Restbetrag | Mahnstufe):
[LISTE EINFÜGEN]

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER DATENQUALITÄT ab: Welche Felder fehlen,
   welche Posten sind nicht auswertbar? Rechne nicht mit geratenen Werten.
2. Bilde eine Altersstrukturanalyse in den Klassen: nicht fällig / 1–30 Tage
   überfällig / 31–60 / 61–90 / 91–180 / über 180 Tage. Weise je Klasse aus:
   Anzahl Posten, Summe, Anteil an der Gesamtforderung in Prozent.
3. Ermittle das Konzentrationsrisiko: Anteil der drei und der zehn größten
   Debitoren an der Gesamtforderung. Benenne ausdrücklich jedes Klumpenrisiko
   (ein einzelner Debitor mit auffällig hohem Anteil) und was sein Ausfall
   bedeuten würde.
4. Liste AUFFÄLLIGKEITEN, höchstens zehn, sortiert nach Betrag:
   - Teilzahlungen ohne erkennbare Zuordnung (Restbetrag ≠ Rechnungsbetrag)
   - Skontoabzug trotz überschrittener Skontofrist oder ohne Vereinbarung
   - Dauerbrenner: derselbe Debitor mit mehreren Posten über 90 Tage
   - Kleinstbeträge, deren Beitreibung teurer ist als der Betrag
   - Gutschriften/Minusposten ohne Zuordnung zu einem offenen Posten
5. Schlage je Altersklasse eine Maßnahme vor (z. B. keine Maßnahme,
   Zahlungserinnerung, Mahnung mit Frist, telefonische Klärung, Lieferstopp,
   Übergabe an Inkasso/Rechtsanwalt). Nenne je Maßnahme den Adressaten in der
   Kanzlei oder beim Mandanten.
6. Prüfe zuerst, ob eine Wertberichtigung überhaupt in Betracht kommt: Nur bei
   Gewinnermittlung durch Betriebsvermögensvergleich (Bilanz). Ist EÜR angegeben,
   schreibe ausdrücklich "Wertberichtigung bei Gewinnermittlung nach § 4 Abs. 3
   EStG nicht anwendbar" und beschränke dich auf den umsatzsteuerlichen Prüfpfad.
   Nur bei Bilanz: Erstelle einen PRÜFVORSCHLAG zum Wertberichtigungsbedarf:
   Welche Posten sind auf Einzelwertberichtigung zu PRÜFEN und warum (Alter,
   Mahnstufe, Bestreiten, Insolvenz)? Ausdrücklich als Prüfvorschlag formulieren,
   nicht als Entscheidung und nicht als Buchungssatz. Nenne keinen Pauschalsatz
   als gesichert; kennzeichne Erfahrungssätze als "Satz für [JAHR] verifizieren –
   auch für diesen Mandanten".
7. Trenne STRIKT drei Ebenen und ordne jeden Posten aus Nr. 6 genau einer zu:
   a) ZWEIFELHAFT (Bilanz): Anhaltspunkte für eine Wertminderung. Folge:
      Prüfung einer Wertberichtigung auf den NETTOBETRAG. Unterscheide
      handelsrechtlichen Wertansatz (§ 253 HGB) und steuerliche
      Teilwertabschreibung (§ 6 Abs. 1 Nr. 2 EStG, zusätzlich voraussichtlich
      dauernde Wertminderung) und sage, dass beide auseinanderfallen können.
   b) UNEINBRINGLICH (Umsatzsteuer): erst wenn die Forderung auf absehbare Zeit
      rechtlich oder tatsächlich nicht durchsetzbar ist. Bloße Zweifelhaftigkeit,
      Bestreiten oder eine gebildete Wertberichtigung genügen NICHT. Nur dann
      kommt eine Berichtigung nach § 17 Abs. 2 Nr. 1 UStG in Betracht.
   c) WEDER NOCH.
   Weise darauf hin, dass der Zeitpunkt der Uneinbringlichkeit gesondert
   festzustellen ist und den Voranmeldungszeitraum bestimmt, und dass bei
   Ist-Versteuerung nach § 20 UStG die Steuer erst mit Vereinnahmung entsteht,
   eine Berichtigung wegen Uneinbringlichkeit also regelmäßig ausscheidet.
   Behandle Entgeltminderungen getrennt: Für Skonti, Boni und Gutschriften weise
   auf eine Änderung der Bemessungsgrundlage nach § 17 Abs. 1 UStG hin und nenne
   den Voranmeldungszeitraum als gesondert festzustellend; prüfe, ob ein bereits
   übermittelter Zeitraum betroffen ist. Behaupte keine Fristen, Quoten oder
   Buchungssätze. Alle Fundstellen mit "für [JAHR] verifizieren".
8. Formuliere jede Ursachenaussage als Vermutung, solange sie nicht aus den
   Daten folgt. Erfinde keine Beträge.
9. Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Kannst du sie nicht angeben, kennzeichne die Aussage
   als "ohne Fundstelle – vor Verwendung belegen". Erfinde keine Paragrafen,
   BMF-Schreiben oder Dokumentnummern; unsichere: "Fundstelle offen – bitte
   recherchieren".

AUSGABEFORMAT (alles als Tabellen, kein Fließtext)
1. Datenqualität
2. Altersstruktur (Klasse | Anzahl | Summe | Anteil %)
3. Konzentrationsrisiko (Debitor | Summe | Anteil % | Bemerkung)
4. Auffälligkeiten (Nr. | Debitor | Betrag | Auffälligkeit | Prüfschritt)
5. Maßnahmen je Altersklasse (Klasse | Maßnahme | Verantwortlich | Frist)
6. Prüfvorschlag Wertberichtigung (Posten | Betrag | Grund | zu klären)
7. Interne Notiz (was die Kanzlei noch prüfen muss, geht nicht an den Mandanten)
8. Was ich nicht sicher weiß
```

## Anwendung

1. OPOS-Liste zum Stichtag aus dem Rechnungswesen exportieren (CSV genügt), Kundennamen maskieren.
2. Prompt ausführen. Die Altersstruktursummen gegen die Debitorensumme der Summen- und Saldenliste abgleichen – stimmen sie nicht überein, ist der Export unvollständig.
3. Auffälligkeiten und Maßnahmen mit dem Mandanten durchgehen; die Tabelle "Maßnahmen" eignet sich als Besprechungsgrundlage.
4. Prüfvorschlag zur Wertberichtigung in die Abschlussakte legen, nicht direkt buchen.

## Qualitätssicherung

- Altersklassen-Summen und Prozentanteile selbst nachrechnen; Summenbildung über viele Zeilen ist eine bekannte Fehlerquelle von Sprachmodellen. Gegenprobe in Excel.
- Vor jeder Mahnung prüfen, ob zwischenzeitliche Zahlungseingänge verbucht sind. Eine Mahnung an einen bereits zahlenden Kunden ist der teuerste Fehler dieser Auswertung.
- Wertberichtigung, Ausbuchung und § 17 UStG entscheidet ausschließlich der Berufsträger.
- Vier-Augen-Prinzip und Freigabe: Vor Weitergabe an den Mandanten muss eine zweite Person die Konzentrationsanalyse und mindestens drei Einzelposten nachvollziehen und abzeichnen. Die Freigabe zur Weitergabe erteilt ein Berufsträger; über Wertberichtigung, Ausbuchung und § 17 UStG entscheidet er ausschließlich selbst. Die Freigabe ist zu dokumentieren.
- Alle genannten Wertberichtigungssätze, Fristen und Fundstellen gegen eine Primärquelle verifizieren.

## Varianten

- **Kreditorenseite:** Gleiche Struktur auf offene Verbindlichkeiten anwenden, Zusatz "Bewerte Skontovorteile und Fälligkeiten für die Liquiditätsplanung."
- **Monatliche Serie:** Zusatz "Vergleiche mit der Auswertung des Vormonats und benenne nur die Veränderungen."
- **Liquiditätsblick:** Zusatz "Leite aus den Fälligkeiten eine Zahlungseingangsprognose für 30/60/90 Tage ab und kennzeichne sie als Schätzung."

## Als Skill

Für die wiederkehrende Auswertung gibt es diesen Prompt auch als ausführende
Skill: [skills/01-finanzbuchhaltung/18-op-liste-analysieren/](../../skills/01-finanzbuchhaltung/18-op-liste-analysieren/).
Sie führt die Altersklassen-Zuordnung und die Risikoklassifizierung über alle
Zeilen des OPOS-Exports selbst aus, statt sie dem Leser zu überlassen.
