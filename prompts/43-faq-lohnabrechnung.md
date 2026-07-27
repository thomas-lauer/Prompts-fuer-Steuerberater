# 43 – FAQ zur Lohnabrechnung für die Mitarbeiter des Mandanten

**Problem:** Dieselben Fragen der Arbeitnehmer – Schichtzuschläge, Firmenwagen, Sachbezug, bAV, Minijob – kommen jeden Monat neu, binden Zeit beim Arbeitgeber und landen am Ende doch in der Kanzlei.
**Rolle:** Lohnsachbearbeitung, Teamleitung Lohn
**DATEV-Bezug:** Lohn und Gehalt, LODAS, DATEV Arbeitnehmer online (dort kann die FAQ als Dokument bereitgestellt werden)
**Was du bereitstellen musst:** Besonderheiten der Entgeltbestandteile beim Mandanten, die tatsächlich gestellten Fragen der letzten Monate, wer welche Frage beantwortet.
**Datensparsamkeit:** Keine Einzelfälle in die FAQ. Arbeitnehmer als `AN 1`, Arbeitgeber als `Mandant A`, keine Personalnummern, keine Beträge einzelner Arbeitnehmer, keine Gesundheitsdaten, keine Gläubigerdaten. Die FAQ beschreibt Regeln, nicht Personen. Beispielrechnungen nur mit erkennbar erfundenen Rundbeträgen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Fachkraft für Entgeltabrechnung in einer deutschen Steuerkanzlei und
schreibst eine FAQ für die Belegschaft eines Arbeitgebers.
Dein Stil: Alltagssprache, kurze Sätze, keine Paragrafen, keine Fachbegriffe
ohne Erklärung. Du erklärst, ohne zu belehren.

AUFGABE
Erzeuge eine FAQ-Sammlung zur Lohnabrechnung für die Mitarbeiter des
Arbeitgebers, zugeschnitten auf dessen Besonderheiten.

BETRIEBSPROFIL
- Branche und Größe: [ANGABEN]
- Beschäftigungsarten: [Vollzeit / Teilzeit / Minijob / kurzfristig /
  Werkstudenten / Azubis / Aushilfen]
- Arbeitszeitmodell: [Festzeit / Schicht / Nacht- und Sonntagsarbeit /
  Gleitzeit / Arbeitszeitkonto]
- Entgeltbestandteile im Betrieb: [z. B. Schichtzuschläge, Sonn-, Feiertags-
  und Nachtzuschläge, Firmenwagen, Jobrad, Tankgutschein, Essenszuschuss,
  betriebliche Altersversorgung, vermögenswirksame Leistungen,
  Fahrtkostenzuschuss, Prämien, Urlaubs- und Weihnachtsgeld]
- Sonderthemen aktuell: [z. B. Kurzarbeit, Tarifwechsel, Betriebsübergang,
  Umstellung des Abrechnungssystems]
- Abrechnungstermin und Zahltag: [ANGABEN]
- Zuständigkeiten: [wer beantwortet was: Personalabteilung / Vorgesetzte /
  Kanzlei / Krankenkasse / Finanzamt]
- Häufigste Fragen der letzten Monate: [LISTE, WÖRTLICH]

ANFORDERUNGEN
1. Erzeuge 12 bis 18 Fragen. Nimm NUR Themen auf, die zum Betriebsprofil
   passen. Lasse alles weg, was nicht zutrifft – eine kurze zutreffende FAQ
   ist besser als eine vollständige unzutreffende.
2. Jede Antwort höchstens 80 Wörter. Alltagssprache, Sie-Form, keine
   Paragrafen, keine Verweise auf Gesetze oder Verordnungen. In der FAQ selbst
   keine Paragrafen. **Führe jedoch in der internen Notiz zu jeder Antwort die
   einschlägige Rechtsgrundlage mit dem Zusatz "für [JAHR] verifizieren" auf** –
   sie geht nicht an die Belegschaft, sondern dient der Freigabe. Bist du dir
   einer Fundstelle nicht sicher, schreibe "Fundstelle offen – bitte
   recherchieren" statt einer Angabe.
3. Formuliere die Fragen so, wie Arbeitnehmer sie stellen, nicht in
   Fachsprache ("Warum ist mein Netto im Januar niedriger?" statt
   "Auswirkung der Beitragsbemessungsgrenze zum Jahreswechsel").
4. KEINE individuelle Steuerberatung des Arbeitnehmers. Bei allem, was von
   der persönlichen Situation abhängt (Steuerklassenwahl, Erstattung,
   Veranlagung, Kirchensteuer, Nebeneinkünfte, Elterngeldhöhe, private
   Vorsorge, Pfändung), gib KEINE Empfehlung, sondern verweise auf
   Finanzamt, Krankenkasse oder eigene steuerliche Beratung.
   Schreibe in diesen Fällen ausdrücklich, dass die Antwort allgemein ist.
5. Nenne KEINE Beträge, Grenzen, Sätze oder Freibeträge (Geringfügigkeits-
   grenze, Sachbezugswerte, Beitragsbemessungsgrenzen, steuerfreie
   Zuschlagsgrenzen, Freigrenze für Sachbezüge, bAV-Höchstbeträge),
   ohne sie als "Wert für [JAHR] verifizieren" zu markieren. Setze diesen
   Marker direkt hinter den Wert. Rate keine Werte; wenn du unsicher bist,
   schreibe die Antwort ohne Zahl.
6. Ordne die Fragen in Rubriken (z. B. Abrechnung allgemein, Zuschläge,
   Sachbezüge und Firmenwagen, Altersversorgung, Sonderzahlungen, Fehlzeiten,
   Ein- und Austritt, Bescheinigungen). Führe die Rubrik "Sonderzahlungen"
   in jedem Fall und vermerke in der internen Notiz, dass Antworten zu
   Einmalzahlungen im ersten Quartal vor Freigabe fachlich zu prüfen sind.
7. Erzeuge zusätzlich eine Liste "Diese Fragen beantworten wir nicht
   schriftlich" mit je einem Satz, an wen die Frage stattdessen geht.
8. Schließe die FAQ mit einem Satz, dass die Angaben allgemein sind, keine
   Beratung im Einzelfall ersetzen und sich Werte jährlich ändern.

AUSGABEFORMAT
1. FAQ, nach Rubriken gegliedert, Frage fett, Antwort darunter
2. "Diese Fragen beantworten wir nicht schriftlich": Frage | Zuständig |
   Begründung in einem Halbsatz
3. Interne Notiz als Tabelle: Frage | Rechtsgrundlage (für [JAHR] verifizieren) |
   vor Freigabe fachlich zu prüfen | Wert nachzuschlagen | jährlich zu
   aktualisieren
4. Was ich nicht sicher weiß
```

## Anwendung

1. Vorher die tatsächlichen Fragen der letzten drei Monate sammeln. Ohne diese Liste entsteht eine allgemeine FAQ, die niemand liest.
2. Entwurf mit dem Personalverantwortlichen durchgehen; er streicht, was im Betrieb nicht vorkommt, und ergänzt betriebliche Regelungen.
3. Alle Stellen mit "Wert für [JAHR] verifizieren" abarbeiten: Marker ersetzen oder Zahl streichen. Kein Versand mit stehengebliebenen Markern.
4. Freigabe durch den Arbeitgeber einholen – die FAQ geht in seinem Namen heraus. Wiedervorlage zum Jahreswechsel setzen.

## Qualitätssicherung

- **Jede Zahl selbst prüfen.** Geringfügigkeitsgrenze, Sachbezugswerte, Beitragsbemessungsgrenzen und steuerfreie Zuschlagsgrenzen ändern sich jährlich; hier ist das Modell strukturell unzuverlässig.
- Prüfen, ob eine Antwort im Einzelfall zur Beratung des Arbeitnehmers wird. Alles, was von Steuerklasse, Familienstand oder Nebeneinkünften abhängt, gehört in die Verweisliste, nicht in die Antwort.
- Abgleich mit Arbeitsvertrag, Betriebsvereinbarung und Tarifvertrag des Mandanten: Die FAQ darf keine betriebliche Regelung behaupten, die es nicht gibt.
- **Vier-Augen-Prinzip:** fachliche Prüfung durch die Lohnsachbearbeitung, Nachprüfung jeder Zahl und jeder Rechtsgrundlage der internen Notiz durch eine zweite Person mit Abzeichnung, Freigabe durch den Berufsträger, danach schriftliche Freigabe des Arbeitgebers. Kein Wert und kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- Prüfen, dass keine Aussage zu Kurzarbeit, Pfändung oder Entgeltersatzleistungen Rückschlüsse auf einzelne Beschäftigte zulässt.

## Varianten

- **Aushang:** "Erzeuge zusätzlich eine Kurzfassung mit den fünf häufigsten Fragen, höchstens 200 Wörter, für den Aushang am schwarzen Brett."
- **Onboarding:** "Erzeuge eine FAQ nur für neu eingestellte Mitarbeiter zur ersten Abrechnung."
- **Jahreswechsel:** "Erzeuge eine FAQ nur zu den Veränderungen im Januar."
- **Einzelfall:** siehe Prompt 08 für die Erklärung einer konkreten Abrechnung.
- **Sachbezüge:** siehe Prompt 40 für das ausführliche Merkblatt an den Arbeitgeber.
