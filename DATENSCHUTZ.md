# Datenschutz- und Freigabe-Leitfaden für KI in der Kanzlei

Wer KI-Werkzeuge mit Mandantenbezug einsetzt, arbeitet an der empfindlichsten
Stelle des Berufsrechts. Dieser Leitfaden sagt, was ohne Weiteres geht, was nur
maskiert geht und was gar nicht geht.

> **Kein Rechtsrat.** Dieser Leitfaden ist eine Arbeitshilfe, keine
> Rechtsberatung und keine datenschutzrechtliche Prüfung. Die Entscheidung über
> den Einsatz eines konkreten Werkzeugs trifft die Kanzleileitung, im Zweifel
> nach Rücksprache mit der Steuerberaterkammer oder einem Datenschutzbeauftragten.

---

## 1. Worum es rechtlich geht

Drei Ebenen, die gleichzeitig gelten:

| Ebene | Kern | Folge bei Verstoß |
|-------|------|-------------------|
| **Berufsrecht** – § 57 StBerG, § 5 BOStB, **§ 62a StBerG** (Einbindung von Dienstleistern), § 62 StBerG (Verpflichtung der Beschäftigten) | Verschwiegenheit über alles, was in Ausübung des Berufs bekannt wird | Rüge durch den Kammervorstand (§ 81 StBerG); berufsgerichtlich nach § 90 StBerG Warnung, Verweis, Geldbuße bis 50.000 € (Berufsausübungsgesellschaften bis 500.000 €), Berufsverbot bis fünf Jahre, Ausschließung aus dem Beruf |
| **Strafrecht** – § 203 StGB | Offenbaren fremder Geheimnisse durch Berufsgeheimnisträger ist strafbar | Freiheits- oder Geldstrafe |
| **Datenschutz** – DSGVO | Verarbeitung personenbezogener Daten braucht Rechtsgrundlage, Auftragsverarbeitungsvertrag und technische Maßnahmen | Bußgeld, Schadensersatz, Meldepflicht |
| **KI-Verordnung** – Art. 4 VO (EU) 2024/1689 | Betreiber müssen für ausreichende KI-Kompetenz des eigenen Personals sorgen | Aufsichtsrechtliche Folgen; im Haftungsfall Organisationsverschulden |

**Die berufsrechtliche Prüfung geht der datenschutzrechtlichen vor.**
§ 62a StBerG ist die Spezialnorm für die Einbindung von Dienstleistern und
damit für den KI-Einsatz. Ein Auftragsverarbeitungsvertrag nach Art. 28 DSGVO
ersetzt sie nicht; umgekehrt bleiben die Vorschriften zum Schutz
personenbezogener Daten neben dem Berufsrecht unberührt
(§ 62a Abs. 8 StBerG). § 203 Abs. 3 Satz 2 StGB erlaubt die Einbeziehung
sonstiger mitwirkender Personen, soweit dies für die Inanspruchnahme ihrer
Tätigkeit erforderlich ist; wer die erforderliche Verpflichtung unterlässt,
macht sich nach § 203 Abs. 4 StGB strafbar. Ob ein KI-Dienst
als mitwirkende Person in diesem Sinne gilt, ist nicht abschließend geklärt.
**Solange das offen ist, ist Maskierung nicht Vorsicht, sondern der eigentliche
Schutzmechanismus.**

Der praktische Ausweg ist einfach: Was nie beim Anbieter ankommt, kann nicht
offenbart werden. Für fast alle Aufgaben in dieser Sammlung ist der
Mandantenname fachlich irrelevant.

## 1a. KI-Kompetenz ist Pflicht, nicht Kür

Art. 4 KI-VO gilt seit **2.2.2025** und verpflichtet jeden Betreiber eines
KI-Systems, für ausreichende KI-Kompetenz der eigenen Beschäftigten zu sorgen –
auch bei rein internem Einsatz. Für die Kanzlei heißt das: eine dokumentierte
Einweisung, die mindestens Funktionsweise und Grenzen von Sprachmodellen, das
Halluzinationsrisiko bei Zahlen und Fundstellen sowie die kanzleiinternen
Freigabestufen abdeckt. Ein gelesener Leitfaden genügt dafür nicht. Datum,
Inhalt und Teilnehmerkreis festhalten.
*(Geltungsbeginn und Anforderungen für [JAHR] verifizieren – die KI-VO wird
stufenweise anwendbar.)*

Getrennt davon und schon vor dem ersten Zugriff auf Mandantendaten: Beschäftigte
sind nach **§ 62 StBerG in Textform** zur Verschwiegenheit zu verpflichten und
über die Strafbarkeit zu belehren – auch Auszubildende und Hilfskräfte.

## 2. Die drei Zonen

### Zone Rot – kommt nie in ein KI-Werkzeug

Auch nicht maskiert, auch nicht in Ausschnitten:

- Steuer-Identifikationsnummer, Steuernummer, Aktenzeichen des Finanzamts
- vollständige Ausweis-, Pass- und Sozialversicherungsnummern
- vollständige IBAN und Kreditkartennummern
- Zugangsdaten, Vollmachtsdaten, Freischaltcodes, ELSTER-Zertifikate
- Gesundheitsdaten, Angaben zu Religionszugehörigkeit, Gewerkschafts- oder
  Parteizugehörigkeit, Herkunft, sexueller Orientierung – auch wenn sie
  steuerlich relevant sind (Kirchensteuer, Behindertenpauschbetrag,
  Krankheitskosten). Für die Bearbeitung genügt "Pauschbetrag nach § 33b EStG",
  nicht der Grund.
- Angaben zu laufenden Strafverfahren, Steuerstrafverfahren, Selbstanzeigen
- Inhalte, die einem Beschlagnahmeschutz unterliegen könnten
- alles, was Dritte betrifft, die nicht Mandant sind, soweit vermeidbar
  (Gläubiger bei Pfändungen, Namen bewirteter Gäste, Angehörige)

### Zone Gelb – nur maskiert

Alles, was fachlich gebraucht wird, aber identifizierend wirkt:

| Statt | Einsetzen |
|-------|-----------|
| Mandantenname, Firma | `Mandant A`, `Mandantin B` |
| Anschrift, Ort | weglassen; bei Bedarf `Ort im Inland`, `Ort in [LAND]` |
| Arbeitnehmername, Personalnummer | `AN 1`, `AN 2` |
| Ansprechpartner | `Frau M.`, `Herr S.` oder nur die Rolle |
| Lieferant, Kunde, Geschäftspartner | `Lieferant 1`, `Kunde EU 1` |
| Bankverbindung | `Konto ****1234` |
| Objekt, Grundstück, Fahrzeug | `Objekt 1`, `Fahrzeug 1` |
| Bewirtete Personen | `Teilnehmer 1–4` |
| Geburtsdatum | `Kind 1, 14 Jahre` – Alter statt Datum |

**Konsistent maskieren.** Wenn derselbe Lieferant in mehreren Positionen
vorkommt, immer dasselbe Kürzel – sonst wird die Analyse unbrauchbar.

**Rückübersetzung bleibt in der Kanzlei.** Die Zuordnungstabelle
(`Mandant A = tatsächlicher Name`) wird nie mit übertragen und nie im
KI-Werkzeug gespeichert.

### Zone Grün – unbedenklich

- Sachverhalte ohne Personenbezug
- Beträge, Konten, Buchungssätze, Kennzahlen
- Daten und Zeiträume
- Rechtsfragen, Prüfschemata, Formulierungshilfen
- eigene Texte der Kanzlei, die veröffentlicht werden sollen
- alles, was ohnehin öffentlich ist

## 3. Freigabestufen

Wer darf was, ohne zu fragen:

| Stufe | Wer | Was |
|-------|-----|-----|
| **1 – frei** | alle Mitarbeitenden | Zone Grün: Formulierungshilfen, Erklärungen, Schulungsfälle, allgemeine Rechtsfragen ohne Mandantenbezug |
| **2 – nach Einweisung** | Mitarbeitende, die den Leitfaden gelesen und bestätigt haben | Zone Gelb: maskierte Mandantensachverhalte, maskierte Exporte |
| **3 – Berufsträger** | nur Berufsträger, dokumentiert | alles, was an einen Mandanten geht und rechtlich verbindlich wirkt: Einspruchsbegründung, Sachverhaltsdarstellung ans Finanzamt, Honoraranpassung, Mandatsfragen |
| **verboten** | niemand | Zone Rot |

Kein KI-Ergebnis verlässt die Kanzlei ohne menschliche Prüfung. Der Abschnitt
**Qualitätssicherung** in jeder Prompt-Datei sagt, worauf konkret zu achten ist.

## 4. Werkzeugauswahl – was vor dem Ersteinsatz geklärt sein muss

Diese Fragen entscheiden, ob ein Werkzeug überhaupt in Frage kommt. **Punkt 1
kommt zuerst – er ist berufsrechtlich und geht der DSGVO-Prüfung vor.**

1. **Berufsrechtliche Einbindung nach § 62a StBerG** geklärt?
   - Abs. 1 und 2: dokumentierte sorgfältige Auswahl des Anbieters; Beendigung
     der Zusammenarbeit bei Zweifeln.
   - Abs. 3: **Vertrag in Textform**, der den Anbieter unter Belehrung über die
     strafrechtlichen Folgen zur Verschwiegenheit verpflichtet, die
     Kenntnisnahme auf das zur Vertragserfüllung Erforderliche begrenzt und
     festlegt, ob Unterauftragnehmer herangezogen werden dürfen und wie sie in
     Textform zu verpflichten sind. Der Vertrag muss geschlossen sein, **bevor**
     dem Anbieter der Zugang eröffnet wird – das folgt aus § 62a Abs. 1 StBerG,
     nicht aus dem Wortlaut des Absatzes 3.
   - Abs. 4: bei Leistungserbringung im Ausland ein dem inländischen
     Berufsgeheimnis **vergleichbares Schutzniveau** – bei Anbietern außerhalb
     der EU gesondert zu begründen.
   - Abs. 5: dient der Einsatz **unmittelbar einem konkreten Einzelmandat**, ist
     zusätzlich die **Einwilligung des Mandanten** erforderlich. Ob ein allgemein
     genutztes KI-Werkzeug als Kanzlei-IT davon ausgenommen ist, ist ungeklärt.
     Solange das offen ist: entweder Einwilligung einholen oder durchgehend
     maskieren.
   *(Fundstellen für [JAHR] verifizieren.)*
2. **Auftragsverarbeitungsvertrag (Art. 28 DSGVO)** vorhanden und
   unterschrieben? Ohne AVV kein Einsatz mit personenbezogenen Daten. Er
   ersetzt Punkt 1 nicht.
3. **Werden Eingaben zum Training verwendet?** Muss abschaltbar sein oder in
   der Geschäftsversion ausgeschlossen sein. Bei kostenlosen Privatzugängen ist
   das regelmäßig nicht der Fall – **private Accounts sind für Kanzleiarbeit
   ungeeignet.**
4. **Wo werden Daten verarbeitet und wie lange gespeichert?** Serverstandort,
   Aufbewahrungsdauer, Löschmöglichkeit.
5. **Subunternehmer** benannt und vertraglich eingebunden?
6. **Zugriffskontrolle:** eigene Kanzlei-Accounts je Person, keine
   Sammelzugänge, Zwei-Faktor-Authentifizierung.
7. **Protokollierung:** Lässt sich nachvollziehen, wer wann was eingegeben hat?
8. **KI-Kompetenz des Personals** nach Art. 4 KI-VO nachweisbar sichergestellt
   (siehe Abschnitt 1a).

## 5. Was zu dokumentieren ist

- **Verzeichnis von Verarbeitungstätigkeiten** (Art. 30 DSGVO) um den
  KI-Einsatz ergänzen: Zweck, Datenkategorien, Empfänger, Löschfristen.
- **Technische und organisatorische Maßnahmen** (Art. 32) um die
  Maskierungsregel und die Freigabestufen ergänzen.
- **Einweisung der Mitarbeitenden** mit Datum und Unterschrift.
- **Nachweis der KI-Kompetenz** nach Art. 4 KI-VO: Schulungsinhalt, Datum, Teilnehmer.
- **Verschwiegenheitsverpflichtung der Beschäftigten** nach § 62 StBerG in Textform,
  vor dem ersten Zugriff auf Mandantendaten.
- **Vertrag mit dem Anbieter** nach § 62a Abs. 3 StBerG, in Textform.
- **Werkzeugliste:** welches Werkzeug ist freigegeben, welches ausdrücklich nicht.
- Bei Bedarf **Datenschutz-Folgenabschätzung** (Art. 35) – jedenfalls dann,
  wenn unmaskierte personenbezogene Daten verarbeitet werden sollen.

## 6. Mandanteninformation

Bei durchgehender Maskierung werden keine unmittelbar identifizierenden Daten
übermittelt. Das ist **Pseudonymisierung** (Art. 4 Nr. 5 DSGVO), **nicht
Anonymisierung** – die Zuordnungstabelle bleibt in der Kanzlei, der Personenbezug
ist damit nicht endgültig beseitigt. Formulieren Sie die Mandanteninformation
entsprechend: "Mandantendaten werden vor der Verarbeitung durch Platzhalter
ersetzt", nicht "anonymisiert".

Prüfen Sie außerdem, ob die verbleibenden Angaben (Branche, Größenklasse,
Region, Besonderheiten) in Ihrem Mandantenstamm einen Rückschluss zulassen – bei
kleinen Beständen genügt die Kombination.

Unabhängig davon ist nach § 62a Abs. 5 StBerG zu prüfen, ob eine ausdrückliche
Mandanteneinwilligung erforderlich ist, wenn das Werkzeug unmittelbar für ein
einzelnes Mandat eingesetzt wird (siehe Abschnitt 4 Punkt 1).

Transparenz zahlt sich aus: Ein Absatz in der Mandanteninformation, dass die
Kanzlei KI-Werkzeuge zur Textvorbereitung und Analyse einsetzt, dass
Mandantendaten dabei durch Platzhalter ersetzt werden und dass jedes Ergebnis
fachlich geprüft wird, nimmt das Thema vorweg, bevor ein Mandant es aufbringt.

## 7. Checkliste vor dem ersten Einsatz

- [ ] Werkzeug ausgewählt, Auswahlentscheidung dokumentiert (§ 62a Abs. 1, 2 StBerG)
- [ ] Vertrag mit dem Anbieter in Textform, mit Verschwiegenheitsverpflichtung (§ 62a Abs. 3 StBerG)
- [ ] Bei Auslandsbezug: vergleichbares Schutzniveau begründet (§ 62a Abs. 4 StBerG)
- [ ] Geprüft, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG)
- [ ] AVV nach Art. 28 DSGVO geschlossen
- [ ] Training auf Eingaben ausgeschlossen
- [ ] Kanzlei-Accounts eingerichtet, keine Privatzugänge
- [ ] Beschäftigte nach § 62 StBerG in Textform verpflichtet und belehrt
- [ ] KI-Kompetenzschulung nach Art. 4 KI-VO durchgeführt und dokumentiert
- [ ] Freigabestufen festgelegt und den Rollen zugeordnet
- [ ] Wesentlichkeitsgrenze festgelegt, ab der ein Berufsträger freigibt
- [ ] Maskierungsregel schriftlich, alle Mitarbeitenden eingewiesen
- [ ] Verarbeitungsverzeichnis und TOM ergänzt
- [ ] Mandanteninformation angepasst
- [ ] Eine Person benannt, die Rückfragen entscheidet

## 8. Wenn doch etwas passiert ist

1. **Nicht löschen und schweigen.** Vorfall festhalten: was wurde wann von wem
   eingegeben, welches Werkzeug, welche Daten.
2. Beim Anbieter Löschung veranlassen, Bestätigung anfordern.
3. **Meldepflicht prüfen** (Art. 33 DSGVO, 72 Stunden an die Aufsichtsbehörde;
   Art. 34 an die Betroffenen bei hohem Risiko).
4. Berufsrechtliche Seite mit der Steuerberaterkammer klären.
5. Ursache abstellen, Einweisung nachholen, im TOM dokumentieren.

Ein Verstoß, der gemeldet und behoben wird, ist ein Vorfall. Ein Verstoß, der
verschwiegen wird, ist ein zweiter Verstoß.

---

## Kurzfassung für den Aushang

> **Drei Regeln.**
> 1. Keine Namen, keine Nummern, keine Adressen – maskieren mit `Mandant A`, `AN 1`, `Konto ****1234`.
> 2. Steuernummern, Gesundheitsdaten, Zugangsdaten und Strafsachen gehören nie in ein KI-Werkzeug.
> 3. Nichts geht ungeprüft raus. Im Zweifel fragen.
