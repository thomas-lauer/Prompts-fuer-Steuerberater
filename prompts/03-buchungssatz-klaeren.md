# 03 – Buchungssatz klären und begründen (SKR03 / SKR04)

**Problem:** Bei Sonderfällen ist unklar, welches Konto und welcher Steuerschlüssel richtig ist; die Frage landet beim erfahrenen Kollegen, der sie zum fünften Mal beantwortet.
**Rolle:** Buchhaltung, Steuerfachangestellte, Berufseinsteiger
**DATEV-Bezug:** Kanzlei-Rechnungswesen, Kontenrahmen SKR03/SKR04, DATEV-Steuerschlüssel
**Was du bereitstellen musst:** Sachverhalt, Belegangaben, Kontenrahmen, Rechtsform und Besteuerungsart des Mandanten.
**Datensparsamkeit:** Mandantenname, Steuernummer und den Namen des Rechnungsausstellers durch Platzhalter ersetzen (`Mandant A`, `Lieferant 1`). Für die Kontierungsfrage genügen Rechtsform, Kontenrahmen, Sachverhalt und Beträge.

## Prompt

```text
Du bist Bilanzbuchhalter mit langjähriger Erfahrung in einer deutschen
Steuerkanzlei und arbeitest mit DATEV Kanzlei-Rechnungswesen.

AUFGABE
Bestimme für den folgenden Sachverhalt den korrekten Buchungssatz und
begründe ihn nachvollziehbar.

MANDANTENRAHMEN
- Kontenrahmen: [SKR03 / SKR04]
- Rechtsform: [z. B. Einzelunternehmen / GmbH / Freiberufler-GbR]
- Gewinnermittlung: [Bilanz / EÜR]
- Umsatzsteuer: [Regelbesteuerung / Kleinunternehmer § 19 / teilweise steuerfrei]
- Besonderheiten: [z. B. Ist-Versteuerung, Vorsteuerabzug eingeschränkt]

SACHVERHALT
[SACHVERHALT AUSFÜHRLICH]

BELEGANGABEN
- Rechnungsdatum / Leistungsdatum: [DATUM]
- Netto / USt / Brutto: [BETRÄGE]
- Rechnungsaussteller, Sitz: [LAND, USt-ID vorhanden ja/nein]
- Rechnungshinweise: [z. B. "Steuerschuldnerschaft des Leistungsempfängers"]
- Zahlungsweg: [Bank / Kasse / Kreditkarte / privat verauslagt]

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab:
   eindeutig / vertretbare Varianten / nicht ohne weitere Angaben entscheidbar.
   Wenn Angaben fehlen, liste sie auf und arbeite mit klar benannten Annahmen.
2. Nenne den Buchungssatz in der Form
   Soll-Konto (Nummer + Bezeichnung) an Haben-Konto (Nummer + Bezeichnung), Betrag,
   plus DATEV-Steuerschlüssel oder Automatikkonto-Hinweis.
3. Begründe in maximal 6 Sätzen, warum diese Konten und dieser
   Steuerschlüssel richtig sind. Nenne die einschlägige Norm
   (z. B. § 13b UStG, § 4 Abs. 5 EStG, R 4.10 EStR).
4. Nenne bis zu zwei plausible ALTERNATIVE Buchungen mit dem Kriterium,
   an dem sich die Entscheidung dreht.
5. Nenne die AUSWIRKUNG auf die UStVA (welche Kennzahl, Kz, betroffen ist)
   und – falls relevant – auf die Gewinnermittlung.
6. Nenne typische FEHLERQUELLEN bei diesem Sachverhalt.
7. Kennzeichne ausdrücklich jede Aussage, bei der du dir nicht sicher bist
   oder bei der sich die Rechtslage geändert haben könnte. Rate nicht.
   Prüfe insbesondere, ob Kontonummern im genannten Kontenrahmen wirklich
   so belegt sind; wenn du unsicher bist, sag es.

AUSGABEFORMAT
1. Eindeutigkeit  2. Buchungssatz  3. Begründung  4. Alternativen
5. Auswirkung UStVA/Gewinn  6. Fehlerquellen  7. Was ich nicht sicher weiß
```

## Anwendung

1. Sachverhalt möglichst vollständig beschreiben – die Qualität der Antwort hängt fast vollständig an den Belegangaben.
2. Ergebnis gegen den DATEV-Kontenrahmen (Hilfe-Center-Dokument SKR03/SKR04) und die Steuerschlüsseltabelle abgleichen.
3. Wiederkehrende Fälle mit der geprüften Antwort in die Kanzlei-Wissensdatenbank aufnehmen.

## Qualitätssicherung

- **Kontonummern immer selbst verifizieren.** Sprachmodelle geben Kontonummern häufig plausibel, aber falsch an. Die Nummer ist der am wenigsten verlässliche Teil der Antwort, die Begründung der verlässlichste.
- Steuerschlüssel im DATEV-Programm gegenprüfen, nicht aus der KI-Antwort übernehmen.
- Bei Fällen mit steuerlicher Auswirkung oberhalb der von der Kanzlei festgelegten Wesentlichkeitsgrenze: Freigabe durch einen Berufsträger. Ist keine Grenze festgelegt, gilt jeder Sonderfall als freigabepflichtig.
- Rechtsstand prüfen: Das Modell kennt möglicherweise nicht die aktuellste Rechtsprechung oder BMF-Schreiben.

## Varianten

- **Schulung:** Zusatz "Formuliere die Antwort als Lernfall für einen Auszubildenden im 2. Lehrjahr, mit einer Kontrollfrage am Ende."
- **Massenprüfung:** "Prüfe die folgenden 10 gebuchten Sachverhalte und markiere nur die, bei denen die Kontierung fraglich erscheint."
- **Mandatsübernahme:** "Vergleiche die bisherige Kontierung des Vorberaters mit deiner Empfehlung und benenne Abweichungen."
