# 17 – Jahres-Terminplan und Zulieferkalender für den Mandanten

**Problem:** Belege, Stundenzettel und Unterlagen kommen jedes Mal zu spät, und jedes Mal wird einzeln erinnert. Der Mandant weiß nicht, wann die Kanzlei was braucht – niemand hat es ihm je im Zusammenhang gesagt.
**Rolle:** Sekretariat, Buchhaltung, Lohnsachbearbeitung, Kanzleileitung
**DATEV-Bezug:** DATEV Unternehmen online, LODAS/Lohn und Gehalt, Eigenorganisation (Fristen und Wiedervorlage)
**Was du bereitstellen musst:** Welche Leistungen die Kanzlei für den Mandanten erbringt, in welchem Rhythmus, mit welchen internen Bearbeitungszeiten.
**Datensparsamkeit:** Mandantenname und Steuernummer erst beim Ausdruck einsetzen. Für den Entwurf genügen Leistungsumfang und Rhythmus. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du organisierst die Zusammenarbeit zwischen einer deutschen Steuerkanzlei und
ihren Mandanten. Du erstellst Terminpläne, die Mandanten tatsächlich befolgen –
das heißt: wenige Termine, klare Stichtage, jeder Termin mit dem Grund, warum
er gilt.

AUFGABE
Erstelle einen Zulieferkalender für ein Kalenderjahr.

LEISTUNGEN DER KANZLEI
- Finanzbuchführung: [monatlich / quartalsweise / jährlich / nein]
- Umsatzsteuer-Voranmeldung: [monatlich / quartalsweise / nein],
  Dauerfristverlängerung: [ja / nein]
- Lohnabrechnung: [ja / nein], Anzahl Arbeitnehmer: [ZAHL],
  Abrechnungsschluss am [TAG] des Monats
- Jahresabschluss: [ja / nein], Art: [Bilanz / EÜR]
- Steuererklärungen: [WELCHE]
- Sonstiges: [z. B. Kassenbuch, Anlagenbuchhaltung, betriebswirtschaftliche
  Auswertungen, Zahlungsverkehr]

RAHMEN
- Kalenderjahr: [JAHR]
- Wirtschaftsjahr weicht ab: [nein / ja, von … bis …]
- Interne Bearbeitungszeit der Kanzlei: [z. B. FiBu 5 Arbeitstage,
  Lohn 2 Arbeitstage]
- Übermittlungsweg: [DATEV Unternehmen online / Meine Steuern / Mail / Papier]
- Bekannte Schwachstellen bei diesem Mandanten: [z. B. Kontoauszüge fehlen
  regelmäßig, Stundenzettel kommen zu spät, Kassenbericht unvollständig]
- Betriebsferien oder Saisonspitzen des Mandanten: [ANGABE]

ANFORDERUNGEN
1. Erzeuge eine Jahresübersicht als Tabelle:
   Termin | Was Sie liefern | Wofür wir es brauchen | Was passiert, wenn es fehlt
   Sortiert nach Datum. Wiederkehrende Termine einmal als Regel beschreiben
   ("jeweils bis zum 5. des Folgemonats"), nicht zwölfmal auflisten.
2. Rechne von den gesetzlichen Fristen und vom Abrechnungsschluss RÜCKWÄRTS:
   Zulieferfrist = Frist minus interne Bearbeitungszeit minus zwei
   Arbeitstage Puffer. Nenne die Rechnung offen, damit der Mandant den Sinn
   des Termins versteht.
3. Nenne KEINE konkreten gesetzlichen Abgabefristen als feststehend, ohne sie
   als "für [JAHR] verifizieren" zu kennzeichnen. Fristen verschieben sich
   (Wochenenden, Feiertage, Fristverlängerungen, gesetzliche Änderungen).
   Nenne zu jeder gesetzlichen Frist die Rechtsgrundlage, aus der sie folgt,
   jeweils mit dem Zusatz "für [JAHR] verifizieren"; prüfe und vermerke, ob
   das Fristende auf einen Samstag, Sonntag oder Feiertag fällt (§ 108 Abs. 3
   AO – für [JAHR] verifizieren). Ergänze bei jeder gesetzlichen Frist:
   "Frist von einem Menschen zu berechnen und im Fristenprogramm zu erfassen."
4. Gruppiere nach Rhythmus: monatlich / quartalsweise / jährlich / einmalig.
5. Erzeuge je Zulieferung eine kurze Liste, WAS genau gemeint ist – so
   konkret, dass der Mandant es abhaken kann. Nicht "Buchhaltungsunterlagen",
   sondern die einzelnen Positionen.
6. Gehe auf die genannten Schwachstellen gesondert ein: Für jede eine
   konkrete Regel, die sie abstellt.
7. Erzeuge ein Anschreiben von höchstens 120 Wörtern: warum es den Plan gibt,
   was der Mandant davon hat (nicht: was die Kanzlei davon hat), und wer
   Ansprechpartner ist.
8. Erzeuge zusätzlich eine EINSEITIGE KURZFASSUNG zum Aufhängen: nur die
   wiederkehrenden Termine, groß und knapp, ohne Erläuterung.
9. Erzeuge eine INTERNE VERSION mit einer zusätzlichen Spalte "Wiedervorlage
   Kanzlei": wann die Kanzlei erinnert, wenn nichts eingegangen ist –
   üblicherweise zwei Arbeitstage nach dem Zuliefertermin.
10. Erfinde keine Fristen und keine Bearbeitungszeiten. Was nicht angegeben
    ist, kennzeichnest du als "von der Kanzlei zu ergänzen".
11. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage, jeweils mit dem
    Zusatz "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du
    unsicher, schreibe "Fundstelle offen – bitte recherchieren".

AUSGABEFORMAT
Anschreiben – Jahresübersicht – Kurzfassung zum Aufhängen –
Interne Version mit Wiedervorlagen – Was noch zu ergänzen ist.
```

## Anwendung

1. Einmal je Mandantentyp erzeugen (nur FiBu, FiBu plus Lohn, Jahresabschluss plus Erklärungen) und als Vorlage ablegen.
2. Interne Bearbeitungszeiten realistisch angeben – zu knappe Puffer machen den Plan unglaubwürdig, sobald er einmal nicht hält.
3. Kurzfassung dem Mandanten ausgedruckt geben, nicht nur als PDF ins Portal.
4. Interne Version in die Wiedervorlage übertragen. Der Plan wirkt erst, wenn die Kanzlei die Erinnerung automatisiert.
5. Kombinierbar mit Prompt 01: Bleibt eine Zulieferung aus, greift die Eskalationsstrecke.

## Qualitätssicherung

- **Der Plan ist ein Entwurf, kein Fristenkalender.** Vor dem Versand von einem Berufsträger freigeben lassen: Der Mandant wird die genannten Termine als verbindliche Zusage der Kanzlei verstehen.
- **Alle gesetzlichen Fristen selbst prüfen und eintragen.** Der Prompt liefert die Struktur und die Rückwärtsrechnung, nicht den Fristenkalender. Fristen berechnet und erfasst ein Mensch; kein Datum aus der KI-Antwort übernehmen.
- Prüfen, ob Wochenenden und Feiertage die Termine verschieben.
- Prüfen, ob eine Dauerfristverlängerung besteht – sie verändert die gesamte Monatslogik.
- Bei abweichendem Wirtschaftsjahr die Jahrestermine gesondert kontrollieren.
- Vor dem Versand mit den tatsächlichen Kapazitäten der Kanzlei abgleichen: Ein Plan, den die Kanzlei selbst nicht hält, ist schlechter als keiner.

## Varianten

- **Fristenkonzept der Kanzlei:** "Erzeuge aus dem Plan eine interne Fristenübersicht über alle Mandate: welcher Termin betrifft wie viele Mandanten, wo entstehen Lastspitzen."
- **Onboarding:** "Erzeuge eine Erstversion für ein neues Mandat, ergänzt um die einmalig benötigten Unterlagen zum Mandatsbeginn."
- **Lohn separat:** "Erzeuge nur den Lohnteil als eigenen Stichtagsplan für den Personalverantwortlichen des Mandanten."
- **Erinnerungstexte:** "Erzeuge zu jedem wiederkehrenden Termin einen kurzen Erinnerungstext von höchstens 40 Wörtern, der drei Tage vorher automatisch versendet werden kann."
