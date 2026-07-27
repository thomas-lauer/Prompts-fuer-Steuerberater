# 29 – Onboarding-Fahrplan für neue Kanzleimitarbeiter

**Problem:** Fachkräftemangel trifft auf fehlende Zeit zum Anlernen; neue Mitarbeitende arbeiten sich unstrukturiert ein, und jede Rückfrage landet bei denselben erfahrenen Kolleginnen.
**Rolle:** Kanzleileitung, Teamleitung, Ausbildungsbeauftragte
**DATEV-Bezug:** DATEV Arbeitsplatz, Kanzlei-Rechnungswesen, LODAS / Lohn und Gehalt, Einkommensteuer, DMS / Dokumentenablage, DATEV Unternehmen online
**Was du bereitstellen musst:** Rolle und Vorerfahrung der neuen Person, Mandantenstruktur des Teams, eingesetzte DATEV-Module, verfügbare Ansprechpartner mit Zeitbudget, kanzleieigene Freigaberegeln.
**Datensparsamkeit:** Keine Namen, keine Personalnummern, keine Angaben zu Gehalt, Gesundheit oder Bewerbungsunterlagen in den Prompt. Es genügen Rolle, Vorerfahrung in Jahren und die Module (`neue Kraft FiBu, Quereinstieg, 0 Jahre DATEV`). Ansprechpartner als `Kollegin FiBu`, `Teamleitung Lohn` benennen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Kanzleileiterin einer deutschen Steuerkanzlei und planst
Einarbeitungen. Du planst nach überprüfbaren Fertigkeiten, nicht nach
Themenlisten: Am Ende jedes Abschnitts steht etwas, das die neue Person
nachweislich allein kann.

AUFGABE
Erstelle einen Einarbeitungsplan für die ersten 90 Tage.

RAHMEN
- Rolle: [FIBU / LOHN / ERKLÄRUNGEN / SEKRETARIAT]
- Vorerfahrung: [BERUFSEINSTEIGER / QUEREINSTEIGER OHNE STEUERPRAXIS /
  ERFAHREN AUS ANDERER KANZLEI]
- Vorhandene DATEV-Erfahrung: [KEINE / GRUNDKENNTNISSE / ROUTINIERT,
  welche Module]
- Wochenarbeitszeit und Präsenz: [ZEIT], [BÜRO / HYBRID / REMOTE]
- Mandantenstruktur des Teams: [z. B. 60 kleine Gewerbe, 10 GmbH, 5 Lohnmandate]
- Eingesetzte Module: [MODULE]
- Ansprechpartner mit Zeitbudget: [z. B. Kollegin FiBu, 3 h/Woche;
  Teamleitung, 1 h/Woche]
- Kanzleiregeln zu Freigaben: [REGELN ODER "noch festzulegen"]

ANFORDERUNGEN
1. Gliedere in vier Abschnitte: Woche 1, Woche 2–4, Monat 2, Monat 3.
   Gib je Abschnitt an: Lernziel, konkrete Aufgaben am echten Mandat,
   Ansprechpartner, und eine ÜBERPRÜFBARE FERTIGKEIT am Ende
   ("kann einen Kontoauszug eines Standardmandats vollständig vorkontieren
   und die offenen Punkte benennen").
2. Passe Tiefe und Tempo an die Vorerfahrung an. Für Quereinsteiger gehören
   Grundlagen (Belegarten, Kontenlogik, Umsatzsteuer im Überblick) in
   Woche 1–4; für Erfahrene aus anderer Kanzlei gehört dorthin stattdessen
   das kanzleispezifische Vorgehen: Ablage, Namenskonventionen,
   Mandantenkommunikation, Fristenkalender.
3. Mache VIER-AUGEN-PRINZIP UND FREIGABESTUFEN ausdrücklich:
   Erzeuge eine eigene Tabelle, welche Aufgaben ab welchem Zeitpunkt ohne
   Rücksprache erledigt werden dürfen, welche weiter gegengelesen werden und
   welche dauerhaft einem Berufsträger vorbehalten bleiben. Ordne jede
   Aufgabe genau einer dieser drei Stufen zu.
4. Plane höchstens DREI Lernziele je Abschnitt. Lasse alles weg, was in
   den ersten 90 Tagen nicht gebraucht wird, und benenne es getrennt unter
   "Später".
5. Nenne je Abschnitt die wahrscheinlichste Überforderungsstelle und wie
   sie abgefedert wird.
6. Nenne KEINE Fristen, Betragsgrenzen oder Rechtsstände als feststehend;
   kennzeichne sie als "für [JAHR] verifizieren". Kanzleispezifische
   Regelungen, die du nicht kennst, markierst du als
   (VON DER KANZLEI FESTZULEGEN) statt sie zu erfinden.
7. BEWERTE KEINE PERSONEN. Der Plan beschreibt Aufgaben, Lernziele und
   Freigabestufen – nie Eignung, Auffassungsgabe, Motivation, Alter oder
   Belastbarkeit einer Person. Gib KEINE Empfehlung zur Probezeit, zur
   Verlängerung oder zur Beendigung des Arbeitsverhältnisses ab; die
   "Entscheidung" im Feedbackgespräch ist ausschließlich eine Entscheidung über
   den weiteren Plan (nächste Lernziele, nächste Freigabestufe). Weise darauf
   hin, dass ein kanzleiweit verwendetes Fertigkeits- oder Beurteilungsraster
   mitbestimmungs- und beschäftigtendatenschutzrechtlich prüfbedürftig ist
   (§ 94 BetrVG, Art. 88 DSGVO, § 26 BDSG – Fundstellen für [JAHR] verifizieren)
   und dass Zweck, Zugriff und Löschfrist der Gesprächsnotizen von der Kanzlei
   festzulegen sind – markiere das als (VON DER KANZLEI FESTZULEGEN).

AUSGABEFORMAT
1. Einarbeitungsplan als Tabelle:
   Abschnitt | Lernziel | Aufgaben | Ansprechpartner | Überprüfbare Fertigkeit
2. Tabelle Freigabestufen:
   Aufgabe | ab wann selbständig | Gegenlesen durch | dauerhaft Berufsträger
3. "Später" – was bewusst nicht in die ersten 90 Tage gehört
4. Gesprächsleitfaden für die Feedbackgespräche nach 30, 60 und 90 Tagen:
   je Termin maximal 6 Fragen, davon mindestens 2 an die Kanzlei gerichtete
   ("Was hat Ihnen gefehlt?"), plus eine Entscheidung, die am Ende
   festzuhalten ist – ausschließlich über den weiteren Plan, siehe
   Anforderung 7
5. Interne Notiz: was die Kanzlei VOR Tag 1 erledigt haben muss –
   Verschwiegenheitsverpflichtung in Textform mit Hinweis auf die Strafbarkeit
   (§ 62 StBerG – für [JAHR] verifizieren), dokumentierte Einweisung in den
   Datenschutz- und KI-Leitfaden der Kanzlei einschließlich KI-Kompetenz nach
   Art. 4 KI-VO, Zugänge und Rechte, Arbeitsplatz, Mandatszuordnung.
   Vor Vorliegen der Verschwiegenheitsverpflichtung darf keine Aufgabe an einem
   echten Mandat eingeplant werden.
6. Was ich nicht sicher weiß
```

## Anwendung

1. Vor dem ersten Tag erzeugen, nicht am ersten Tag – Zugänge und Rechte brauchen Vorlauf.
2. Zeitbudget der Ansprechpartner realistisch angeben. Ein Plan, der 8 Stunden Betreuung pro Woche unterstellt, scheitert in Woche 2.
3. Plan mit der neuen Person gemeinsam durchgehen und die überprüfbaren Fertigkeiten als gemeinsame Erwartung festhalten.
4. Nach jedem Feedbackgespräch den Plan anpassen und die Freigabestufen-Tabelle fortschreiben; sie ist das eigentliche Arbeitsergebnis.
5. Für die Übungsphasen die Fälle aus Prompt 30 nutzen, damit nicht am Echtmandat gelernt wird.

## Qualitätssicherung

- Die Freigabestufen sind eine berufsrechtliche Frage, keine Organisationsfrage. Vorbehaltsaufgaben und Zeichnungsrechte legt ein Berufsträger fest, nicht das Modell.
- Prüfen, ob die "überprüfbaren Fertigkeiten" wirklich beobachtbar sind. Formulierungen wie "versteht die Umsatzsteuer" sind nicht überprüfbar und gehören umgeschrieben.
- Datenschutz und Verschwiegenheit gehören **vor** Tag 1; in Woche 1 folgt nur die Anwendung. Die Verpflichtung nach § 62 StBerG in Textform und die dokumentierte Einweisung einschließlich KI-Kompetenz nach Art. 4 KI-VO liegen vor dem ersten Zugriff auf Mandantendaten vor – wenn das Modell sie weglässt, ergänzen.
- **Kein Beurteilungsinstrument.** Prüfen, dass der Plan und die Gesprächsnotizen keine Aussage zu Eignung, Motivation oder Probezeit enthalten. Ein kanzleiweit verwendetes Fertigkeitsraster ist mitbestimmungs- und beschäftigtendatenschutzrechtlich prüfbedürftig; Zweck, Zugriff und Löschfrist der Notizen vor dem Einsatz festlegen.
- **Der Plan ist ein Entwurf.** Vier-Augen-Prinzip: Teamleitung und ein Berufsträger geben den Plan und die Freigabestufen-Tabelle gemeinsam frei, bevor Aufgaben an echten Mandaten eingeplant werden.
- Plan gegen die tatsächliche Mandatslast prüfen: Wer ab Monat 2 volle Fälle übernimmt, braucht ab Monat 2 auch weniger Betreuungstermine, nicht mehr.
- Bei Auszubildenden zusätzlich Berufsschulzeiten, Ausbildungsrahmenplan und Ausbildungsnachweis einplanen.

## Varianten

- **Rückkehr nach Abwesenheit:** "Erstelle einen 30-Tage-Plan für die Rückkehr nach Elternzeit; Schwerpunkt auf Änderungen seit [ZEITRAUM]."
- **Werkstudenten und Aushilfen:** "Begrenze auf abgegrenzte, wiederkehrende Aufgaben ohne Mandantenkontakt."
- **Führungsrolle:** "Ergänze einen Abschnitt zur Übernahme der Teamverantwortung ab Monat 3."
- **Standardplan:** Je Rolle einmal erzeugen und als Vorlage ablegen; pro Person nur noch Vorerfahrung und Mandate anpassen.
