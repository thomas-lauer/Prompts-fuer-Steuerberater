# 04 – Umsatzsteuer-Sonderfall prüfen (§ 13b, i.g. Erwerb, Differenzbesteuerung, Kleinunternehmer)

**Problem:** Reverse-Charge, innergemeinschaftliche Vorgänge und Sonderformen werden falsch eingeordnet; der Fehler zeigt sich erst in der Voranmeldung oder in der Prüfung.
**Rolle:** Buchhaltung, Steuerberater
**DATEV-Bezug:** Kanzlei-Rechnungswesen, UStVA, Zusammenfassende Meldung
**Was du bereitstellen musst:** Sachverhalt, beide Beteiligte mit Sitz und USt-ID-Status, Leistungsart, Rechnungswortlaut.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Steuernummer, Personalnummern und Namen Dritter durch Platzhalter ersetzen (`Mandant A`, `Lieferant EU 1`, `Konto ****1234`). Für die fachliche Prüfung genügen Rolle, Sitzland, USt-ID-Status, Beträge und Daten.

## Prompt

```text
Du bist Umsatzsteuer-Spezialist in einer deutschen Steuerkanzlei. Du arbeitest
streng nach Prüfschema und behauptest nichts, was du nicht begründen kannst.

AUFGABE
Ordne den folgenden Vorgang umsatzsteuerlich ein und leite daraus die
Behandlung in Buchführung, UStVA und ggf. Zusammenfassender Meldung ab.

SACHVERHALT
- Leistender Unternehmer: [ROLLE, anonymisiert – z. B. "Lieferant EU 1"],
  Sitz: [LAND], USt-ID: [vorhanden/nicht],
  Kleinunternehmer § 19 UStG: [ja/nein/unbekannt]
- Leistungsempfänger: [ROLLE, anonymisiert], Sitz: [LAND], USt-ID: [vorhanden/nicht],
  Unternehmer: [ja/nein], Verwendung: [unternehmerisch/privat/gemischt]
- Art der Leistung: [Warenlieferung / sonstige Leistung / Werklieferung /
  Bauleistung / Grundstücksleistung / digitale Leistung / …]
- Beschreibung: [SACHVERHALT]
- Ort der Leistungserbringung / Warenweg: [VON → NACH]
- Beträge: [NETTO / AUSGEWIESENE USt / BRUTTO]
- Rechnungswortlaut / Hinweise auf der Rechnung: [WORTLAUT]
- Zeitpunkt: [LEISTUNGSDATUM / RECHNUNGSDATUM / ZAHLUNG]
- Besonderheiten: [z. B. Kleinunternehmer, Differenzbesteuerung angewendet,
  Reihengeschäft, Anzahlung]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Ist der Leistende Unternehmer und handelt er im Rahmen seines
   Unternehmens? (§ 2 UStG) Ist er Kleinunternehmer (§ 19 UStG)?
   Wenn ja: Folgen für Steuerausweis, Vorsteuerabzug des Empfängers
   und die Anwendbarkeit des § 13b UStG.
2. Was ist der Umsatz? Lieferung, sonstige Leistung, Werklieferung?
   (§ 3 Abs. 1 / Abs. 9 UStG)
3. Wo liegt der Leistungsort? Nenne die Ortsvorschrift (§ 3 Abs. 5a–8,
   § 3a, § 3b, § 3c, § 3e, § 3g UStG). Erst daraus folgt, ob der Umsatz
   im Inland steuerbar ist (§ 1 Abs. 1 Nr. 1 UStG).
4. Greift eine Steuerbefreiung? Wenn ja: welche, und welche Nachweise sind nötig?
5. Wie hoch ist die Bemessungsgrundlage (§ 10 UStG)? Prüfe, ob eine
   Sonderform greift, insbesondere Differenzbesteuerung (§ 25a UStG)
   mit ihren Voraussetzungen und Aufzeichnungspflichten.
6. Wer schuldet die Steuer? Prüfe insbesondere § 13b UStG mit seinen
   Tatbestandsvoraussetzungen einzeln.
7. Welcher Steuersatz gilt?
8. Wann entsteht die Steuer? (Soll-/Ist-Versteuerung, Anzahlungen)
9. Ist der Vorsteuerabzug gegeben? Nenne Voraussetzungen und Hindernisse.
10. Welche Meldepflichten entstehen? (UStVA-Kennzahlen, Zusammenfassende
    Meldung, Intrastat)
11. Ist die vorliegende Rechnung formell korrekt? Nenne fehlende Pflichtangaben
    nach § 14 Abs. 4 / § 14a UStG und den nötigen Hinweistext.

ANFORDERUNGEN
- Nenne zu jedem Schritt die Rechtsgrundlage.
- Wenn ein Schritt ohne weitere Angaben nicht entscheidbar ist: sag das
  ausdrücklich, benenne die fehlende Angabe und rechne beide Varianten durch.
- Schließe mit einer Kurzfassung in fünf Sätzen, die ein Mandant versteht.
- Kennzeichne am Ende gesondert: "Rechtsstand unsicher / bitte prüfen bei: …"
  für alle Punkte, bei denen sich die Rechtslage geändert haben könnte.
- Erfinde keine Paragrafen und keine BMF-Schreiben. Wenn du eine Fundstelle
  nicht sicher kennst, schreibe "Fundstelle bitte verifizieren".

AUSGABEFORMAT
Prüfschritte 1–11 als nummerierte Abschnitte, dann
"Buchungs- und Meldefolge", dann "Kurzfassung für den Mandanten",
dann "Rechtsstand unsicher".
```

## Anwendung

1. Beide Beteiligte vollständig beschreiben – die häufigste Fehlerursache ist eine unvollständige Angabe zum Leistungsempfänger.
2. Ergebnis für die UStVA-Kennzahlen im DATEV-Programm gegenprüfen.
3. Bei wiederkehrenden Konstellationen (z. B. ein Dienstleister aus dem EU-Ausland) die geprüfte Einordnung als Dauervermerk zum Kreditor hinterlegen.

## Qualitätssicherung

- **Fundstellen einzeln nachschlagen.** Sprachmodelle zitieren Paragrafen häufig richtig, BMF-Schreiben und Aktenzeichen jedoch häufig falsch.
- Prüfschema ist ein Denkgerüst, keine verbindliche Auskunft. Bei Zweifelsfällen Rücksprache mit dem Berufsträger, ggf. verbindliche Auskunft beim Finanzamt.
- USt-ID des Geschäftspartners immer über das qualifizierte Bestätigungsverfahren des BZSt prüfen – das kann die KI nicht.
- Rechtsstandsangaben (Steuersätze, Schwellenwerte, Meldepflichten) an der aktuellen Fassung verifizieren.

## Varianten

- **Rechnungsprüfung isoliert:** Nur Schritt 11 verwenden, mit Zusatz "Erzeuge den korrekten Hinweistext in Deutsch und Englisch."
- **Mandantenschulung:** "Erkläre den Fall als Entscheidungsbaum mit Ja/Nein-Fragen, den ein Mitarbeiter des Mandanten selbst durchlaufen kann."
- **Bauleistungen:** Schritt 6 mit dem Zusatz "Prüfe die Bauleistereigenschaft nach § 13b Abs. 5 Satz 2 UStG und die Bedeutung der Freistellungsbescheinigung USt 1 TG."
