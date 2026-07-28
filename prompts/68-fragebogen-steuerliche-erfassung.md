# 68 – Fragebogen zur steuerlichen Erfassung: Interview-Leitfaden mit Weichenstellungen

**Problem:** Der Fragebogen wird „schnell ausgefüllt", und damit fallen unbemerkt Vorentscheidungen zu Kleinunternehmerregelung, Ist-Versteuerung, Voranmeldungszeitraum und Vorauszahlungen, die den Gründer jahrelang binden.
**Rolle:** Fachassistent (Interview), Steuerberater (Entscheidungen)
**DATEV-Bezug:** Übermittlung über DATEV bzw. Mein ELSTER, Stammdatenanlage in DATEV Arbeitsplatz und den zentralen Stammdaten, Kanzlei-Rechnungswesen, DATEV Vollmachtsdatenbank
**Was du bereitstellen musst:** Art der Tätigkeit, geplanter Beginn, Rechtsform, Orte der Tätigkeit, geschätzte Umsätze und Gewinne der ersten zwei Jahre, Kundenkreis, Auslandsbezug, geplante Investitionen, geplante Beschäftigung, erteilte Vollmachten.
**Datensparsamkeit:** Gründer als `Mandant A`, Beteiligte nur als Rolle. Bankverbindung nur als `Konto ****1234`, vollständige IBAN bleibt draußen. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachassistent in einer deutschen Steuerkanzlei und führst das
Aufnahmegespräch für den Fragebogen zur steuerlichen Erfassung. Du entscheidest
kein Wahlrecht – du machst jede Weichenstellung, ihre Folgen und ihre
Umkehrbarkeit sichtbar und legst sie dem Berufsträger vor.

AUFGABE
Erstelle einen Interviewleitfaden mit Entscheidungspunkten, eine
Plausibilitätsprüfung der geschätzten Zahlen und eine Unterlagenliste zum
Mandatsbeginn.

RAHMEN
- Mandant: [MANDANT A], Tätigkeit: [BESCHREIBUNG]
- Einordnung: [gewerblich / freiberuflich / land- und forstwirtschaftlich / unklar]
- Rechtsform: [Einzelunternehmen / GbR / UG / GmbH / sonstige]
- Geplanter Beginn: [ZEITPUNKT], Vorbereitungshandlungen: [ZEITPUNKT]
- Orte der Tätigkeit: [ANGABEN], weitere Betriebsstätten: [ja / nein / geplant]
- Geschätzter Umsatz Jahr 1 und 2: [BETRÄGE]
- Geschätzter Gewinn Jahr 1 und 2: [BETRÄGE]
- Kundenkreis: [Unternehmen / Privatpersonen / gemischt],
  Auslandsbezug: [nein / EU / Drittland]
- Investitionen und Vorsteuerbeträge geplant: [ANGABEN]
- Arbeitnehmer geplant: [nein / ja, ab ZEITPUNKT], Minijob: [ja / nein]
- Weitere Einkünfte: [ANGABEN]

WEICHENSTELLUNGEN – JE WEICHE IN DIESER GLIEDERUNG
(1) Frage an den Mandanten in Alltagssprache
(2) Folgen von Weg A und Weg B, je in Alltagssprache, ohne Betrag
(3) Kriterien, nach denen entschieden wird
(4) Umkehrbarkeit: (frei wählbar) / (praktisch schwer korrigierbar) /
    (für mehrere Jahre bindend) / (nicht korrigierbar)
(5) Wer entscheidet – Ausübung stets durch den Berufsträger

Behandle diese Weichen:
a) Kleinunternehmerregelung anwenden oder darauf verzichten, samt der Bindung
   eines Verzichts (§ 19 UStG – für [JAHR] verifizieren), wobei der maßgebliche
   Gesamtumsatz alle Umsätze des Unternehmers erfasst, also auch die aus weiteren
   Tätigkeiten (§ 19 Abs. 1 und Abs. 3 UStG – für [JAHR] verifizieren; Bindung
   eines Verzichts über mehrere Kalenderjahre, Widerrufsmöglichkeit gesondert)
b) Ist-Versteuerung: keine freie Wahl, sondern Gestattung durch das Finanzamt auf
   Antrag, mit eigenen Voraussetzungen, Widerrufsmöglichkeit und Übergangsfolgen
   beim Wechsel
   (§ 20 UStG – Voraussetzungen und Schwellen für [JAHR] verifizieren)
c) Zeitraum der Umsatzsteuer-Voranmeldung: Regelzeitraum, Sonderregel für die
   Aufnahme der Tätigkeit (§ 18 Abs. 2 Satz 4 UStG) und die Frage, ob und bis zu
   welchem Kalenderjahr diese Sonderregel ausgesetzt ist (§ 18 Abs. 2 Satz 6 UStG
   – Geltungszeitraum für [JAHR] verifizieren, die Aussetzung ist befristet);
   Wahlrecht zum Kalendermonat bei Vorsteuerüberschuss (§ 18 Abs. 2a UStG) und
   seine Bindung für das Kalenderjahr; Dauerfristverlängerung und
   Sondervorauszahlung
   (§ 18 UStG i.V.m. UStDV – Fundstelle für [JAHR] verifizieren).
   Schwellenbeträge nur als nachzuschlagend.
d) geschätzte Umsätze und Gewinne und ihre Folge für Vorauszahlungen,
   einschließlich der Wirkung weiterer Einkünfte auf die Vorauszahlungen
   (§ 37 EStG – für [JAHR] verifizieren)
e) Gewinnermittlungsart: Einnahmenüberschussrechnung oder Bilanz, samt der
   Frage, wodurch eine Buchführungspflicht entsteht
f) Beginn der Tätigkeit und Abgrenzung zu Vorbereitungshandlungen
g) Betriebsstätten und ihre Folgen für weitere Steuerarten
h) geplante Beschäftigung von Arbeitnehmern und was daraus folgt
i) Bankverbindung und Lastschriftmandat, Nutzen und Widerrufbarkeit

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Ist die Einordnung der Tätigkeit unklar, entscheide sie NICHT,
   sondern lege sie dem Berufsträger vor.
2. Nenne KEINEN Schwellenwert, keinen Betrag, keinen Steuersatz und keine Frist
   als feststehend – nur nachzuschlagend mit dem Zusatz
   "für [JAHR] verifizieren"; besonders bei Kleinunternehmergrenze und
   Buchführungspflicht.
3. Sage bei JEDER Weiche ausdrücklich, wie umkehrbar sie ist, und benenne die
   praktisch schwer oder nicht korrigierbaren Wahlrechte im eigenen Abschnitt
   "Bindende Entscheidungen". Die Ausübung entscheidet ein Berufsträger.
4. Plausibilitätsprüfung: Prüfe die Schätzzahlen auf innere Stimmigkeit (Umsatz,
   Gewinn, Kostenstruktur, Investitionen, Kundenkreis) und stelle dar, welche
   Folge eine zu hohe und eine zu niedrige Schätzung für die Vorauszahlungen hat
   – als Wirkungsrichtung, ohne Betrag. Erfinde keine Zahl.
5. Liquiditätshinweis: höchstens 150 Wörter, Sie-Form, erklärt, warum
   Vorauszahlungen und Umsatzsteuer zurückzulegen sind, ohne Quote.
6. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Anzeigepflichten im
   Raum stehen (Anzeige der Erwerbstätigkeit, Dauerfristverlängerung, Verzicht
   und Widerruf bei der Kleinunternehmerregelung, Anmeldezeiträume), je mit
   Rechtsgrundlage – § 138 AO, § 19 UStG, § 18 UStG (für [JAHR] verifizieren) –
   ohne Datum und Dauer, und ergänze: "Frist von einem Menschen zu berechnen und
   im Fristenprogramm zu erfassen."
7. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV (Norm MIT
   ABSATZ UND SATZ, Richtlinie oder BMF-Schreiben MIT DATUM) mit dem Zusatz
   "für [JAHR] verifizieren"; bist du unsicher:
   "Fundstelle offen – bitte recherchieren".
8. Unterlagen- und Vollmachtenliste zum Mandatsbeginn als abhakbare Liste
   (Kästchen ☐), getrennt nach Kanzlei und Mandant, mit den Angaben für
   Stammdaten und Vollmachtsdatenbank.

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit"
2. "Interviewleitfaden" – je Weiche die fünf Gliederungspunkte
3. "Entscheidungstabelle": Weiche | Empfehlungstendenz aus den Angaben |
   Kriterium | Umkehrbarkeit | Entscheidung des Berufsträgers (leer)
4. "Bindende Entscheidungen" 5. "Plausibilitätsprüfung der Schätzzahlen"
6. "Liquiditätshinweis für den Gründer" 7. "Fristarten und Anzeigepflichten"
8. "Unterlagen und Vollmachten" 9. "Interne Notiz"
10. "Was ich nicht sicher weiß"
```

## Anwendung

1. Leitfaden im Erstgespräch abarbeiten; den Fragebogen erst danach ausfüllen.
2. Entscheidungstabelle dem Berufsträger vorlegen – seine Spalte bleibt bis dahin leer.
3. Schätzzahlen belegen (Angebote, Auftragsbestand, Kalkulation), nicht schätzen lassen.
4. Nach der Entscheidung Stammdaten anlegen, Vollmacht erfassen, Kontenrahmen und Voranmeldungszeitraum eintragen.
5. Entscheidung und Begründung je Wahlrecht dokumentieren.

## Qualitätssicherung

- **Kein Wahlrecht aus dem Interview ausüben.** Kleinunternehmerregelung, Ist-Versteuerung und Gewinnermittlungsart entscheidet ein Berufsträger, mit Begründung dokumentiert.
- **Schwellenwerte, Beträge und Fristen aus der KI-Antwort nie übernehmen.**
- **Bindungswirkung gegenprüfen.** Ein Verzicht auf die Kleinunternehmerregelung wirkt über mehrere Jahre; die Angabe des Modells ist prüfbedürftig (§ 19 UStG – für [JAHR] verifizieren).
- **Schätzzahlen prüfen.** Zu hohe Schätzungen belasten die Startliquidität, zu niedrige führen zu Nachzahlungen.
- **Freigabe und Vier-Augen:** Das Ergebnis ist ein Entwurf. Eine zweite Person prüft Entscheidungstabelle und Plausibilität; Fragebogen und Übermittlung gibt ein Berufsträger frei (Freigabestufe 3 in `DATENSCHUTZ.md`). Fristen berechnet ein Mensch.
- **Rechtsstand prüfen an:** § 138 AO, § 18 Abs. 2 Satz 4 und 6, Abs. 2a UStG, §§ 46 bis 48 UStDV, §§ 19, 20 UStG, § 37 EStG, § 141 AO und § 241a HGB (gesetze-im-internet.de), dem amtlichen Fragebogen samt Ausfüllhinweisen sowie DATEV LEXinform.

## Varianten

- **Nur Weichen:** „Erzeuge ausschließlich die Entscheidungstabelle."
- **Kapitalgesellschaft:** „Ergänze die Weichen einer neu gegründeten Kapitalgesellschaft, ohne Gestaltungsempfehlung."
- **Nebentätigkeit:** „Passe den Leitfaden auf eine Gründung neben einer Anstellung an."
- **Mandatsbeginn:** Prompt 09. **Mandatswechsel:** Prompt 69.
