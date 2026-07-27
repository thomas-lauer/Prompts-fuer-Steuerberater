# 06 – BWA in Mandantensprache kommentieren

**Problem:** Die BWA geht unkommentiert ins Portal. Der Mandant versteht die Zahlen nicht, ruft an oder zieht falsche Schlüsse – und fühlt sich unbetreut.
**Rolle:** Steuerberater, Buchhaltung
**DATEV-Bezug:** Kanzlei-Rechnungswesen (BWA, kurzfristige Erfolgsrechnung), DATEV Analyse und Planung (Kennzahlen/Controllingreport), DATEV Unternehmen online
**Was du bereitstellen musst:** BWA-Werte des Zeitraums, Vergleichswerte (Vormonat, Vorjahr, kumuliert), Branche, bekannte Sondereffekte.
**Datensparsamkeit:** Mandantenname und Anschrift durch ein Kürzel ersetzen (`Mandant A`). Für den Kommentar genügen Branche, Größenordnung und die Zahlen.

## Prompt

```text
Du bist Steuerberater und erklärst einem Unternehmer seine Zahlen. Dein Stil:
klar, konkret, ohne Fachjargon, ohne Alarmismus, immer mit Handlungsbezug.
Du erfindest keine Ursachen – du benennst Auffälligkeiten und formulierst
Fragen dazu.

AUFGABE
Schreibe einen Kommentar zur beigefügten BWA für den Mandanten.

KONTEXT
- Mandant / Branche / Größe: [ANGABEN]
- Zeitraum: [MONAT/JAHR], kumuliert [ZEITRAUM]
- Gewinnermittlung: [Bilanz / EÜR]
- Bekannte Sondereffekte: [z. B. Großauftrag, Investition, Saisonalität,
  Personalaufbau, Einmalzahlung, Wechsel der Kontierung]
- Was den Mandanten aktuell beschäftigt: [z. B. Bankgespräch, Liquidität,
  geplante Investition, Personalentscheidung]

ZAHLEN
[BWA-WERTE EINFÜGEN: Position | laufender Monat | Vormonat | Vorjahresmonat |
kumuliert | Vorjahr kumuliert]

ANFORDERUNGEN
1. Beginne mit drei Sätzen "Das Wichtigste in Kürze" – Ergebnis, Tendenz,
   ein Punkt, auf den der Mandant achten sollte.
2. Erläutere danach höchstens FÜNF Positionen. Wähle die mit der größten
   Abweichung oder der größten Steuerungsrelevanz. Ignoriere den Rest bewusst.
   Je Position: Was hat sich verändert (Betrag und Prozent), was das praktisch
   bedeutet, und – falls die Ursache nicht aus den Angaben hervorgeht –
   EINE Rückfrage an den Mandanten.
3. Nenne zwei bis drei Kennzahlen, die für diese Branche aussagekräftig sind
   (z. B. Rohertragsquote, Personalkostenquote, Materialeinsatzquote),
   mit Wert, Vorjahresvergleich und einer Einordnung in einem Satz.
   Nenne KEINE angeblichen Branchendurchschnitte, wenn du sie nicht belegen
   kannst – schreibe stattdessen, dass ein Branchenvergleich sinnvoll wäre.
4. Schließe mit "Vorschlag für das nächste Gespräch": zwei bis drei konkrete
   Punkte, keine Allgemeinplätze.
5. Sprache: Sie-Form, keine Abkürzungen ohne Auflösung, keine Begriffe wie
   "periodenfremd", "Abgrenzung", "neutraler Aufwand" ohne kurze Erklärung
   in Klammern.
6. Länge: maximal 400 Wörter.
7. Formuliere jede Ursachenaussage als Vermutung oder Frage, solange sie
   nicht aus den gelieferten Angaben eindeutig folgt. Keine erfundenen Gründe.
8. Schließe mit einem Vorbehaltssatz: Die BWA ist eine unterjährige
   Auswertung auf Basis der gebuchten Belege; Abgrenzungen,
   Bestandsveränderungen, Abschreibungen und Rückstellungen sind noch
   nicht oder nur planmäßig berücksichtigt. Nenne die Positionen, die
   dadurch im konkreten Fall verzerrt sein können.

AUSGABEFORMAT
"Das Wichtigste in Kürze" – "Was sich verändert hat" (max. 5 Punkte) –
"Kennzahlen" – "Vorschlag für das nächste Gespräch" – "Zur Einordnung"
(Vorbehaltssatz) –
darunter separat: "Interne Notiz: offene Rückfragen an den Mandanten".
```

## Anwendung

1. BWA-Werte inklusive Vergleichsspalten aus DATEV exportieren (CSV oder Kopie der Tabelle).
2. Sondereffekte, die man in der Kanzlei kennt, unbedingt mitgeben – sonst rät das Modell.
3. Kommentar als PDF zur BWA ins Portal legen, interne Notiz behalten.
4. Bei monatlicher Wiederholung: Zusatz "Beziehe dich auf den Kommentar des Vormonats: [TEXT]" ergänzen, damit keine Wiederholungen entstehen.

## Qualitätssicherung

- Prozentwerte und Abweichungen stichprobenartig nachrechnen.
- Jede Ursachenbehauptung streichen, die nicht belegt ist. Der häufigste Fehler ist eine plausibel klingende, aber erfundene Erklärung.
- Keine Prognosen und keine Finanzierungsempfehlungen ohne Freigabe durch den Berufsträger.
- Vor dem Versand prüfen, ob der Ton zur Mandantenbeziehung passt.

## Varianten

- **Bankgespräch:** Zusatz "Ergänze eine Fassung von einer Seite, die für ein Gespräch mit der Hausbank geeignet ist – sachlich, mit Fokus auf Ertragskraft und Kapitaldienstfähigkeit."
- **Kurzfassung:** "Erzeuge zusätzlich eine Fassung mit maximal 90 Wörtern für eine E-Mail."
- **Quartalsgespräch:** "Fasse die letzten drei Monatskommentare zu einem Quartalsbericht zusammen und benenne die Entwicklungslinie."
