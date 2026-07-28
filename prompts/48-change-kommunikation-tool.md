# 48 – Change-Kommunikation bei Tool-Einführung im Team

**Problem:** Widerstand gegen ein neues Werkzeug kommt selten aus der Technik, sondern aus Versagensangst, Kontrollverlust und Sorge um die eigene Rolle – daran scheitern Tool-Einführungen, nicht an der Software.
**Rolle:** Kanzleileitung, Projektverantwortliche
**DATEV-Bezug:** Einführung von DATEV-Anwendungen, z. B. DATEV Unternehmen online, Belegtransfer, DATEV Meine Steuern
**Was du bereitstellen musst:** Werkzeug und Zweck, betroffene Rollen, was sich je Rolle ändert, Zeitrahmen, bereits geäußerte Bedenken (sinngemäß, ohne Personenbezug).
**Datensparsamkeit:** Keine Namen von Mitarbeitenden, keine Zuordnung von Aussagen zu Personen, keine Leistungsbeurteilungen, keine Angaben zu Alter, Gesundheit oder persönlichen Umständen. Betroffene nur als Rolle (`Fachkraft FiBu`), Mandanten als `Mandant A`. Bedenken nur als Aussage, nie als "Kollegin X sagt". Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du berätst die Leitung einer deutschen Steuerkanzlei bei der Einführung
eines neuen Werkzeugs. Widerstand ist meist ein Hinweis auf ein
ungelöstes Problem, nicht auf mangelnden Willen. Du bewertest keine
Personen, triffst keine Personalentscheidung und empfiehlst keine
Maßnahme gegen Mitarbeitende – du lieferst einen Kommunikationsplan
zur Entscheidung durch die Kanzleileitung.

AUFGABE
Erstelle einen Kommunikationsplan für die Einführung einschließlich
Einwandbehandlung und Ankündigungstext an das Team.

VORHABEN
- Werkzeug / Modul: [BEZEICHNUNG]
- Zweck aus Sicht der Kanzlei: [ANGABE]
- Was das Werkzeug NICHT leisten soll: [ANGABE]
- Betroffene Rollen: [ANGABE, nur Rollen]
- Was sich je Rolle ändert: [ROLLE: Änderung im Arbeitsalltag]
- Was bleibt wie bisher: [ANGABE]
- Zeitrahmen: [START – VOLLBETRIEB]
- Unterstützung: [z. B. Schulung, Testphase, Pate, Sprechstunde]
- Geäußerte Bedenken (sinngemäß, ohne Personenbezug): [ANGABE]
- Frühere Einführungen: [gut / gemischt / schlecht]

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab und benenne fehlende
   Angaben. Rate nicht, was das Team denkt.
2. Baue den Kommunikationsplan entlang dieser fünf Fragen:
   (1) Was wird geändert und warum – der Grund muss ein Kanzleiproblem
       benennen, nicht "Digitalisierung" als Selbstzweck.
   (2) Was ändert sich für wen – je Rolle in einfachen Sätzen, am
       Arbeitstag entlang, nicht am Funktionsumfang entlang.
   (3) Was bleibt – ausdrücklich benennen; Sicherheit entsteht durch das,
       was nicht angetastet wird.
   (4) Welche Unterstützung es gibt – Angebot, Zeitpunkt, ansprechbare
       Rolle, und die Zusage, dass Fehler in der Einführungsphase keine
       arbeitsrechtlichen Folgen und keine Auswirkung auf Beurteilung oder
       Zuständigkeit haben. Sag im selben Satz, dass die fachliche
       Vier-Augen-Kontrolle in der Einführungsphase nicht entfällt, sondern
       verstärkt wird, und benenne, wer in dieser Phase gegenliest.
   (5) Wie Bedenken aufgenommen werden – Weg, Frist, wer antwortet und
       was mit einer Rückmeldung geschieht.
3. BEHANDLE BEDENKEN ALS SACHLICH. Zu jedem Einwand erst der berechtigte
   Kern, dann die Antwort. Relativierende Antworten ("das ist doch ganz
   einfach", "das wird schon") sind unzulässig. Was nicht ausgeräumt
   werden kann, sag offen – und benenne, womit die Kanzlei lebt.
4. Benenne die NACHTEILE ehrlich: was länger dauert, was schlechter wird,
   welcher Aufwand entsteht, wie lange die Umstellung dauert.
   Kennzeichne Zeitschätzungen als Schätzung.
5. BEWERTE KEINE MITARBEITENDEN. Keine Aussage über Lernfähigkeit,
   Haltung, Motivation, Alter oder Betriebszugehörigkeit. Keine
   Einteilung in Befürworter und Bremser. Keine Maßnahmen gegen einzelne
   Personen. Multiplikatoren nur als ROLLE mit Aufgabe und Zeitbudget,
   nicht als Person und nicht als Auszeichnung.
6. Nenne drei bis fünf Erfolgsmaße auf Kanzlei- oder Prozessebene, nicht
   auf Personenebene. Sag ausdrücklich, dass Nutzungsdaten Einzelner
   nicht zur Leistungskontrolle dienen und eine Auswertung
   mitbestimmungs- und datenschutzrechtlich prüfbedürftig sein kann.
   Erfinde dazu keine Fundstellen. Sag ausdrücklich, dass bereits die
   EINFÜHRUNG und Anwendung einer technischen Einrichtung, die zur Leistungs-
   oder Verhaltenskontrolle geeignet ist, mitbestimmungsrechtlich prüfbedürftig
   ist – nicht erst deren Auswertung (§ 87 Abs. 1 Nr. 6 BetrVG – für [JAHR] verifizieren).
7. Ankündigungstext: höchstens 250 Wörter, ruhig, konkret, ohne Werbeton.
   Erster Absatz: was, ab wann, warum. Letzter Absatz: wohin mit Fragen
   und Bedenken, bis wann.
8. VORAUSSETZUNGEN VOR DER ANKÜNDIGUNG: Nimm in die interne Notiz auf, was vor
   dem ersten Kommunikationsschritt geklärt sein muss – Auftragsverarbeitungs-
   vertrag, Verschwiegenheitsverpflichtung des Anbieters in Textform
   (§ 62a Abs. 3 StBerG), Ausschluss der Verwendung von Eingaben zum Training,
   Verarbeitungsort, Zugriffskontrolle, KI-Kompetenz des Personals
   (Art. 4 KI-VO), Eintrag in die Werkzeugliste der Kanzlei (Checkliste in
   DATENSCHUTZ.md). Ist einer dieser Punkte offen, schreibe ausdrücklich: noch
   nicht ankündigungsreif.
9. Nenne zu jedem als prüfbedürftig gekennzeichneten Punkt die voraussichtlich
   einschlägige Norm mit dem Zusatz "Fundstelle – für [JAHR] verifizieren".
   Erfinde keine Fundstelle; bist du unsicher, schreibe "Norm unbekannt, durch
   Berufsträger zu bestimmen".

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit"
2. "Kommunikationsplan" (Fragen 1–5)
3. "Einwandtabelle": Einwand | berechtigter Kern | Antwort | offen (j/n)
4. "Zeitplan": Schritt | Woche | Rolle | Ergebnis
5. "Rollen": Multiplikator, Ansprechstelle, Entscheidung – mit Aufgabe
   und Zeitbudget
6. "Erfolgsmessung": Maß | Erhebungsweg | Intervall
7. "Ankündigungstext an das Team"
8. "Interne Notiz": Entscheidungsbedarf der Kanzleileitung, zu deckende
   Zusagen, fehlende Angaben
9. "Was ich nicht sicher weiß"
```

## Anwendung

1. Vor dem Prompt die fünf Fragen selbst beantworten – besonders "was bleibt". Wer das nicht sagen kann, sollte noch nicht ankündigen.
2. Bedenken sinngemäß und ohne Personenbezug einfügen. Eine Einwandtabelle ohne echte Einwände ist wertlos.
3. Ankündigung mündlich machen, den Text danach nachreichen – nicht umgekehrt.
4. Zusagen zu Schulung, Testphase und Ansprechzeiten vorher terminlich absichern. Eine nicht gehaltene Zusage kostet mehr als keine.
5. Nach vier bis sechs Wochen die offenen Punkte der Einwandtabelle durchgehen und Rückmeldung geben.

## Qualitätssicherung

- **Jede Zusage auf Deckung prüfen** – Schulungstermine, Ansprechzeiten, Testphase. Die Zusage zur Folgenfreiheit von Fehlern gilt für arbeitsrechtliche Folgen, Beurteilung und Zuständigkeit; sie hebt die fachliche Vier-Augen-Kontrolle nicht auf. Steht im Text nicht, wer in der Einführungsphase gegenliest, ist die Zusage ungedeckt. Ungedeckte Zusagen streichen, nicht abschwächen.
- **Werkzeug vor Ankündigung freigeben.** Ohne Auftragsverarbeitungsvertrag, Verschwiegenheitsverpflichtung des Anbieters in Textform (§ 62a Abs. 3 StBerG), Trainingsausschluss, geklärten Verarbeitungsort, Zugriffskontrolle, KI-Kompetenzschulung (Art. 4 KI-VO) und Eintrag in die Werkzeugliste wird nicht angekündigt (Checkliste in `DATENSCHUTZ.md`). Fundstellen für [JAHR] verifizieren.
- **Einwandtabelle gegenlesen:** Wird jeder Einwand ernst genommen oder wegargumentiert? Antworten mit "eigentlich", "einfach", "kein Problem" überarbeiten.
- **Nachteile prüfen.** Stehen keine Nachteile im Ergebnis, ist der Text Werbung und wird nicht geglaubt.
- **Keine Personenbewertung.** Text auf Aussagen über einzelne Mitarbeitende oder Gruppen ("die Älteren", "die Skeptiker") durchsuchen und entfernen.
- **Mitbestimmung setzt bei der Einführung an, nicht erst bei der Auswertung.** Ist das Werkzeug zur Leistungs- oder Verhaltenskontrolle geeignet, ist schon die Einführung prüfbedürftig (§ 87 Abs. 1 Nr. 6 BetrVG – für [JAHR] verifizieren). Erfolgsmessung zusätzlich datenschutzrechtlich prüfen lassen; die Hinweise des Modells sind prüfbedürftig.
- **Freigabe durch die Kanzleileitung** vor jeder Kommunikation ans Team, im Vier-Augen-Prinzip mit der projektverantwortlichen Rolle; berührt die Einführung Mandantenkommunikation oder Mandantendaten, gibt ein Berufsträger frei (Freigabestufe 3 in `DATENSCHUTZ.md`).

## Varianten

- **Pflichtumstellung:** "Das Werkzeug ist nicht verhandelbar. Formuliere den Plan so, dass der Rahmen klar ist, die Ausgestaltung aber mitgestaltet werden kann."
- **Nach dem Fehlstart:** "Die Einführung ist gescheitert. Erzeuge einen Neustart-Plan, der den Fehlstart benennt, ohne Schuld zuzuweisen."
- **Mandantenseite:** "Erzeuge eine Information an betroffene Mandanten, was sich ändert und was bleibt." (Prompt 12 und 26)
- **Arbeitsanweisung:** Prompt 23. **Einarbeitung:** Prompt 29.
