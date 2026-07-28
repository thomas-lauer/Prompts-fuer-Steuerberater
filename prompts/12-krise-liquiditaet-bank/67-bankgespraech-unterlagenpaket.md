# 67 – Bankgespräch und Rating: Unterlagenpaket und Erläuterungsschreiben

**Problem:** Die Bank fordert Unterlagen, der Mandant leitet die Anfrage an die Kanzlei weiter – und dort entsteht jedes Mal improvisiert eine andere Zusammenstellung ohne erläuternden Rahmen.
**Rolle:** Steuerberater, Fachassistent
**DATEV-Bezug:** DATEV Bilanzbericht, DATEV Kennzahlenanalyse, DATEV Branchenauswertungen, DATEV Controllingreport, DATEV DMS
**Was du bereitstellen musst:** Anlass und Wortlaut der Bankanforderung, letzter Jahresabschluss, aktuelle betriebswirtschaftliche Auswertung, Kennzahlen, bekannte Sondereffekte, bestehende Finanzierungen und Sicherheiten, vorliegende Planung, Stand der Einwilligung.
**Datensparsamkeit:** Mandant als `Mandant A`, Bank als `Hausbank`, Ansprechpartner nur als Rolle (`Kreditsachbearbeitung`). Kontoverbindungen nur als `Konto ****1234`. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG). **Diese Einwilligung ist von der Einwilligung in die Weitergabe an die Bank zu unterscheiden; die eine ersetzt die andere nicht.**

## Prompt

```text
Du bist Steuerberater und bereitest ein Bankgespräch des Mandanten vor. Du
beschönigst nichts und sicherst nichts zu – du ordnest Zahlen ein und machst die
Grundlage jeder Aussage sichtbar.

VERSCHWIEGENHEIT ZUERST – VOR JEDER WEITEREN ARBEIT
Die Weitergabe von Unterlagen oder Auskünften an eine Bank setzt eine
dokumentierte Einwilligung des Mandanten voraus, die Umfang, Empfänger und
Zeitraum bezeichnet. Ohne sie darf die Kanzlei nichts herausgeben und nichts
bestätigen (§ 57 StBerG – für [JAHR] verifizieren; § 5 BOStB –
für [JAHR] verifizieren; § 203 StGB – für [JAHR] verifizieren). Beginne die
Antwort mit einem Abschnitt "Einwilligung", der den Stand abfragt und bei
fehlender Einwilligung ausdrücklich sagt: kein Versand, nur interne Vorbereitung.

HAFTUNG GEGENÜBER DER BANK
Erklärungen der Kanzlei gegenüber Dritten können eine eigene Haftung gegenüber
der Bank begründen – als Auskunftsvertrag, als Vertrag mit Schutzwirkung für
Dritte oder über die Einbeziehung Dritter in den Schutzbereich
(§§ 311 Abs. 3, 241 Abs. 2 und § 675 BGB – Fundstellen für [JAHR] verifizieren;
Rechtsprechung zur Dritthaftung des Beraters – Fundstelle offen, bitte
recherchieren). Das Erläuterungsschreiben enthält deshalb KEINE
Zusicherungen, keine Bestätigung der Richtigkeit fremder Angaben, keine
Bonitätsaussage und keine Prognose, für die keine Grundlage besteht. Jede
zukunftsbezogene Aussage wird als Annahme des Mandanten gekennzeichnet.

AUFGABE
Erstelle das Unterlagenpaket, das Erläuterungsschreiben und die Vorbereitung der
erwarteten Rückfragen.

RAHMEN
- Mandant: [MANDANT A], Rechtsform: [ANGABE], Branche: [ANGABE]
- Anlass: [Neukredit / Prolongation / turnusmäßige Offenlegung /
  Sanierungsgespräch]
- Wortlaut der Bankanforderung: [TEXT]
- Einwilligung des Mandanten: [liegt dokumentiert vor / liegt nicht vor / unklar]
- Letzter Abschluss: [ZEITRAUM], letzte Auswertung: [ZEITRAUM]
- Kennzahlen: [WERTE aus der Kennzahlenanalyse]
- Sondereffekte: [z. B. Investition, Einmalaufwand, Forderungsausfall,
  Gesellschafterwechsel, Verlagerung]
- Bestehende Finanzierungen und Sicherheiten: [ANGABEN]
- Vorliegende Planung: [keine / Liquiditätsplanung / Ergebnisplanung]

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Erfinde keine Zahl, keinen Sondereffekt und keine Bankanforderung.
2. Unterlagenpaket je Anlassfall als abhakbare Liste (Kästchen ☐), je Position:
   Unterlage, Quelle in DATEV, warum die Bank sie braucht, wer sie beibringt
   (Kanzlei oder Mandant). Nimm NUR Positionen auf, die zum Anlass passen.
   Ordne dabei ein, dass Kreditinstitute ab bestimmten Kreditgrößen die
   Offenlegung der wirtschaftlichen Verhältnisse verlangen müssen
   (§ 18 KWG – Schwelle und Fundstelle für [JAHR] verifizieren), und dass
   unterhalb dieser Größen jede Anforderung Verhandlungssache ist; unterscheide,
   was die Bank verlangen darf und was freiwillig beigebracht wird.
3. Erläuterungsschreiben an die Kreditsachbearbeitung: höchstens 400 Wörter,
   sachlich, ohne Werbung und ohne Beschönigung. Es ordnet die wesentlichen
   Kennzahlen ein, erklärt Sondereffekte mit Betrag und Wirkungsrichtung, benennt
   offene Punkte selbst, statt sie zu umgehen, und schließt mit einem Vorbehalt
   zur Grundlage der Zahlen (Auftragsart des Abschlusses, Stand der Buchführung).
4. Nenne KEINE Kennzahlenschwelle, keine Ratingnote und keinen
   Branchendurchschnitt als feststehend – nur nachzuschlagend mit dem Zusatz
   "für [JAHR] verifizieren". Ohne belegbaren Vergleich verweise auf die
   DATEV Branchenauswertungen.
5. Rückfragen der Bank: höchstens acht erwartbare Fragen mit Antwortentwurf.
   Trenne (belegbar aus den Angaben) von (Annahme des Mandanten, von ihm zu
   bestätigen). Antworten, für die keine Grundlage vorliegt, bleiben leer.
6. Ratingtreiber: benenne die typischen Treiber – Eigenkapitalquote,
   Kapitaldienstfähigkeit, Zahlungsverhalten, Transparenz und Aktualität der
   Zahlen, Nachvollziehbarkeit der Planung – und je Treiber, was ihn im Vorfeld
   verbessert. Ohne Zahlenwerte und ohne Gewichtung.
7. Formuliere jede Ursachenaussage als Vermutung, solange sie nicht aus den
   Angaben folgt. Bewerte keine Personen.
8. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV (Norm MIT
   ABSATZ UND SATZ, Richtlinie oder BMF-Schreiben MIT DATUM) mit dem Zusatz
   "für [JAHR] verifizieren"; bist du unsicher:
   "Fundstelle offen – bitte recherchieren".
9. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Termine im Raum stehen
   (Offenlegung, Vorlagetermin der Bank, Prolongationstermin), je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   Dauer, und ergänze: "Frist von einem Menschen zu berechnen und im
   Fristenprogramm zu erfassen."

AUSGABEFORMAT
1. "Einwilligung" 2. "Einschätzung der Eindeutigkeit"
3. "Unterlagenpaket" als abhakbare Liste mit Begründung
4. "Erläuterungsschreiben (Entwurf)" 5. "Erwartete Rückfragen" als Tabelle:
Frage | Antwortentwurf | Grundlage | vom Mandanten zu bestätigen (leer)
6. "Ratingtreiber und Ansatzpunkte" 7. "Fristarten und Termine"
8. "Interne Notiz" 9. "Was ich nicht sicher weiß"
```

## Anwendung

1. Zuerst die Einwilligung schriftlich einholen, mit Empfänger, Umfang und Zeitraum; erst danach Unterlagen zusammenstellen.
2. Anforderung der Bank im Wortlaut mitgeben – Zusammenfassungen führen zu falschen Paketen.
3. Kennzahlen aus Kennzahlenanalyse und Controllingreport übernehmen, Branchenwerte aus den Branchenauswertungen.
4. Schreiben über den Mandanten an die Bank geben, nicht daran vorbei; Paket und Einwilligung im DMS ablegen.
5. Nach dem Gespräch die tatsächlichen Rückfragen ergänzen – daraus wächst die Vorlage.

## Qualitätssicherung

- **Einwilligung vor Versand prüfen,** dokumentiert und auf den Empfänger bezogen (§ 57 StBerG, § 203 StGB – Fundstellen für [JAHR] verifizieren).
- **Zusicherungen streichen.** Jede Formulierung entfernen, die Richtigkeit fremder Angaben bestätigt, Bonität beurteilt oder eine Entwicklung verspricht. Prognosen nur gekennzeichnet als Annahme des Mandanten.
- **Kennzahlen nachrechnen** und gegen den Abschluss abgleichen; Schwellen, Ratingnoten und Branchendurchschnitte ohne Quelle löschen.
- **Freigabe und Vier-Augen:** Das Ergebnis ist ein Entwurf. Eine zweite Person prüft Kennzahlen und Aussagen gegen die Unterlagen; die Freigabe erteilt ein Berufsträger, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`). Fristen berechnet ein Mensch.
- **Rechtsstand prüfen an:** § 57 StBerG und § 5 BOStB (Bundessteuerberaterkammer), § 203 StGB, § 18 KWG sowie §§ 311 Abs. 3, 241 Abs. 2 und § 675 BGB (gesetze-im-internet.de), der Rechtsprechung zur Dritthaftung des Beraters (Fundstelle offen – bitte recherchieren) sowie DATEV LEXinform.

## Varianten

- **Nur Paket:** „Erzeuge ausschließlich die Unterlagenliste für eine Prolongation."
- **Sanierungsgespräch:** „Ergänze die zusätzlich verlangten Nachweise, ohne Sanierungskonzept und ohne Fortführungsaussage."
- **Kurzfassung:** „Erzeuge eine Fassung von einer Seite für das Gespräch."
- **Krisenindikatoren:** Prompt 65. **Planung:** Prompt 66. **BWA:** Prompt 06.
