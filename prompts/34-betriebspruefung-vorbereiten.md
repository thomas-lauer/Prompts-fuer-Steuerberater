# 34 – Betriebsprüfung vorbereiten: Checkliste und Mandantenbriefing

**Problem:** Die Prüfungsanordnung liegt vor, die Vorbereitung beginnt zu spät, und der Mandant redet beim ersten Termin frei über Dinge, die niemand gefragt hat.
**Rolle:** Steuerberater, Sachbearbeitung, Mandantenbetreuung
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen, Datenprüfung / Datenzugriff (Z1–Z3), DATEV Bilanzbericht, DMS, Lohnbuchführung bei Lohnsteuer-Außenprüfung
**Was du bereitstellen musst:** Prüfungsanordnung mit Steuerarten, Zeitraum, Schwerpunkten, Beginn und Prüfungsort; Kurzprofil des Betriebs; bekannte offene Punkte.
**Datensparsamkeit:** Vor dem Einfügen Name, Anschrift, Steuernummer, Prüfername und Aktenzeichen durch Platzhalter ersetzen (`Mandant A`, `Prüfer 1`). Für die Vorbereitung genügen Branche, Größenklasse, Rechtsform, Steuerarten, Zeitraum und Schwerpunkte. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und bereitest
Betriebsprüfungen vor. Du arbeitest hypothesengeleitet: erst mögliche
Prüffelder sammeln, dann nach Wahrscheinlichkeit und Aufwand sortieren,
dann konkrete Vorbereitungsschritte nennen.

AUFGABE
Erzeuge aus der Prüfungsanordnung eine Vorbereitungscheckliste für die
Kanzlei, ein Verhaltensbriefing für den Mandanten und eine interne Risikoliste.

PRÜFUNGSANORDNUNG
- Steuerart(en): [z. B. KÖRPERSCHAFTSTEUER / GEWERBESTEUER / UMSATZSTEUER /
  LOHNSTEUER-AUSSENPRÜFUNG / EINKOMMENSTEUER]
- Prüfungszeitraum: [JAHRE]
- Angekündigte Prüfungsschwerpunkte: [WORTLAUT / keine genannt]
- Prüfungsbeginn laut Anordnung: [DATUM]
- Prüfungsort: [Betrieb / Kanzlei / Amtsstelle / offen]
- Datenzugriff angekündigt: [Z1 / Z2 / Z3 / nicht genannt] –
  Rechtsgrundlage § 147 Abs. 6 AO

BETRIEBSPROFIL
- Branche: [ANGABE]
- Rechtsform: [ANGABE]
- Größenordnung: [UMSATZ / MITARBEITERZAHL, grob]
- Gewinnermittlung: [Bilanz / EÜR]
- Besonderheiten: [z. B. Bargeldbranche, Auslandsbezug, Gesellschafter-
  Geschäftsführer, Umstrukturierung im Zeitraum, Fahrzeuge, Subunternehmer]
- Bekannte offene Punkte aus der Buchführung: [ANGABE]
- Vorprüfung: [wann, Ergebnis, damalige Beanstandungen / keine]

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab und benenne fehlende
   Angaben, statt sie zu erfinden.
2. Leite die Prüffelder AUS DEN ANGABEN ab. Nimm nur auf, was zu diesem
   Profil passt. Eine kurze zutreffende Liste ist besser als eine
   vollständige unzutreffende.
3. Höchstens ZEHN Prüffelder. Sortiere nach erwarteter Prüfungsintensität.
4. Formuliere jede Aussage über typische Prüfungspraxis als Erfahrungswert
   und kennzeichne sie als solche. Keine Behauptung darüber, was das
   Finanzamt im konkreten Fall tun wird.
5. Nenne zu jedem Prüfungsschritt die einschlägige Rechtsgrundlage, jeweils mit
   dem Zusatz "für [JAHR] verifizieren", und führe sie am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit Spalte "geprüft von (leer)".
   Mindestens zu nennen, soweit im Fall berührt: Prüfungsanordnung § 196 AO,
   Prüfungsbeginn und Verschiebung § 197 AO, Mitwirkungspflichten § 200 AO,
   qualifiziertes Mitwirkungsverlangen § 200a AO, Schlussbesprechung § 201 AO,
   Prüfungsbericht § 202 AO, Datenzugriff § 147 Abs. 6 AO. Jeden
   jahresabhängigen Wert kennzeichnest du als "für [JAHR] verifizieren". Bist du
   dir einer Fundstelle nicht sicher, schreibe "Fundstelle offen – bitte
   recherchieren" statt einer Angabe.
6. Berechne KEINE Fristen. Liste stattdessen auf, welche Fristen in diesem
   Verfahren im Raum stehen, jeweils mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und ohne Fristlänge:
   - Verschiebung des Prüfungsbeginns (§ 197 Abs. 2 AO)
   - Vorlagefristen aus der Prüfungsanordnung (§ 200 AO)
   - QUALIFIZIERTES MITWIRKUNGSVERLANGEN (§ 200a AO): eigene, kurze Frist mit
     tagegenauer Geldfolge und Verlängerung der Ablaufhemmung nach
     § 171 Abs. 4 AO. Weise ausdrücklich darauf hin, dass dieses Verlangen ein
     anfechtbarer Verwaltungsakt ist und dass Frist und Anfechtungsfrist sofort
     gesondert im Fristenprogramm zu erfassen sind.
   - Schlussbesprechung (§ 201 AO) und Stellungnahme zum Prüfungsbericht
     (§ 202 AO)
   Ergänze in jedem Fall: "Fristen berechnet und erfasst ein Mensch."
7. Das Mandantenbriefing ist in Sie-Form, ohne Fachbegriffe ohne Erklärung,
   höchstens 400 Wörter, und enthält keine internen Bewertungen.

AUSGABEFORMAT
1. (Vorbereitungscheckliste Kanzlei) – abhakbar, Kästchen ☐ vor jeder Position,
   gegliedert nach: bereitzustellende Unterlagen | vorab intern zu klären |
   technische Vorbereitung Datenzugriff | Zuständigkeiten. Nimm in jedem Fall
   diese Position auf:
   ☐ Verfahren für den Fall eines qualifizierten Mitwirkungsverlangens
   (§ 200a AO) festgelegt: wer nimmt es an, wer notiert die Frist, wer
   entscheidet über Anfechtung
2. (Erwartete Prüffelder) – Tabelle:
   Prüffeld | warum in diesem Fall zu erwarten | was wir vorher klären |
   Aufwand (hoch/mittel/gering)
3. (Mandantenbriefing) – Verhaltensleitfaden mit den Punkten:
   wer spricht mit dem Prüfer und wer nicht; welche Fragen nicht spontan
   beantwortet werden, sondern über die Kanzlei laufen; wie Nachfragen und
   Auskünfte dokumentiert werden; Umgang mit dem Datenzugriff und mit
   Unterlagen, die nicht angefordert wurden; Verhalten bei Gesprächen
   zwischen Tür und Angel.
4. (Interne Risikoliste) – nicht an den Mandanten:
   Nr. | Risiko | Einschätzung (Vermutung kennzeichnen) | vorher zu klären |
   wer | erledigt (leer)
5. (Fehlende Angaben) – was für eine belastbare Vorbereitung noch fehlt.
6. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | für welchen Schritt sie steht | geprüft von (leer)
7. (Interne Notiz) – Vorschlag für Terminplanung, Rollenverteilung und
   Wiedervorlagen.
```

## Anwendung

1. Prüfungsanordnung wörtlich übernehmen, insbesondere die Formulierung der Schwerpunkte – daraus folgt der halbe Vorbereitungsaufwand.
2. Bekannte Schwachstellen ehrlich eintragen. Wer sie weglässt, bekommt eine Checkliste, die genau daran vorbeigeht.
3. Checkliste mit dem Mandanten durchgehen und Zuständigkeiten je Position eintragen, bevor die Unterlagen zusammengestellt werden.
4. Datenzugriff frühzeitig technisch vorbereiten; den Umfang der Überlassung vorher mit dem Berufsträger festlegen.
5. Mandantenbriefing rechtzeitig versenden, nicht am Vortag des Termins.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Ausgangsdokuments nachgeprüft und abgezeichnet** – bei Rechtsbehelfsfristen und bei der Frist eines qualifizierten Mitwirkungsverlangens ausnahmslos, unabhängig davon, ob ein Rechtsbehelf geplant ist. Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Alle Fristen der Prüfung – Prüfungsbeginn, Verschiebungsantrag, qualifiziertes Mitwirkungsverlangen, Stellungnahme zum Prüfungsbericht – werden von einem Menschen berechnet, geprüft und im Fristenprogramm erfasst.** Das Modell liefert keine Datumsangaben.
- **Freigabe durch einen Berufsträger** für Checkliste, Briefing und jede Kommunikation mit der Prüfungsstelle.
- Umfang des Datenzugriffs prüfen: Was überlassen wird, entscheidet der Berufsträger, nicht die Buchhaltung und nicht das Modell.
- § 147 Abs. 6 AO wurde zum 1.1.2025 neu gefasst (für [JAHR] verifizieren): geprüft wird, welche Zugriffsart verlangt wird, ob der Umfang auf aufbewahrungspflichtige Unterlagen des Prüfungszeitraums begrenzt ist und wer die Überlassung freigibt.
- Interne Risikoliste bleibt intern und wird getrennt abgelegt – sie darf nicht in die Unterlagen für den Prüfer geraten.
- Aussagen zu Aufbewahrungspflichten, Zugriffsarten und Verfahrensdokumentation am aktuellen Rechtsstand verifizieren.
- Der Mandant erfährt vor dem ersten Termin, dass er Fragen weiterleiten darf und nicht sofort antworten muss.

## Varianten

- **Lohnsteuer-Außenprüfung:** "Beschränke die Prüffelder auf Lohn und Sozialversicherung, ergänzt um Sachbezüge, Pauschalbesteuerung und Reisekosten."
- **Kassenführung:** "Ergänze ein Prüffeld zur Kassenführung und Verfahrensdokumentation mit abhakbarer Unterlagenliste."
- **Nach dem Prüfungsbericht:** "Erzeuge aus den Feststellungen eine Gegenüberstellung: Feststellung | unsere Auffassung | Beleglage | Handlungsoption."
