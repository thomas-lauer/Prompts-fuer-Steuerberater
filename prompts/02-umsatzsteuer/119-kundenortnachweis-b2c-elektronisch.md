# 119 – Elektronische Leistungen an Privatkunden: Ort des Kunden nachweisen

**Problem:** Wer digitale Inhalte, Software, Online-Kurse oder Downloads an Privatkunden im EU-Ausland verkauft, schuldet die Steuer am Wohnsitz des Kunden – und muss belegen können, wo dieser liegt.
**Rolle:** Sachbearbeiter Umsatzsteuer, Steuerberater, Berufsträger; in der Vorbereitung der Mandant selbst
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Erlöskonten je Bestimmungsland und Steuersatz, Umsatzsteuer-Voranmeldung), DATEV Unternehmen online (Belegweg aus Shop- und Zahlungssystemen), DATEV DMS (Ablage der Nachweisdokumentation und der Verzichtserklärung); Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Geschäftsmodell und Art der Leistung; ob automatisiert erbracht wird; Vertriebsweg und Rolle einer Plattform; Zahlungsdienstleister; welche Arten von Beweismitteln heute erhoben werden, wo sie gespeichert sind und ob sie von einem Dritten stammen; die von der Kanzlei bereits ermittelte Lage zu den beiden Schwellenwerten für das laufende und das vorangegangene Kalenderjahr; ob ein Verzicht erklärt wurde und seit wann; ob für zurückliegende Zeiträume bereits Erklärungen abgegeben wurden.
**Datensparsamkeit:** In diesen Prompt kommt **kein einziges Beweismittel**, sondern nur seine Art und die Angabe ja oder nein. Keine IP-Adresse, kein Standortdatensatz, keine Bankverbindung, keine Mobilfunkkennung, keine Kundenanschrift, kein Kundenname – IP-Adresse und Geolokalisierung sind personenbezogene Daten und gehören auch nicht als Beispiel in die Eingabe. Mandantenname und Firmierung durch Platzhalter ersetzen (`Mandant A`, `Kunde EU 1`). Steuernummer, Steuer-Identifikationsnummer und Umsatzsteuer-Identifikationsnummer nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Umsatzsteuer-Spezialist in einer deutschen Steuerkanzlei. Du prüfst den
Leistungsort, BEVOR du irgendetwas anderes prüfst, und du unterscheidest streng
zwischen der Ortsregel und dem Nachweis, mit dem der Ort belegt wird.

WAS DIESER PROMPT NICHT TUT
- Er behandelt NICHT das besondere Besteuerungsverfahren und nicht die Meldung
  selbst. Das ist Portalbedienung und wird von einem Menschen erledigt. Triff
  dazu keine Aussage und gib keine Ausfüllhinweise.
- Er RECHNET NICHT. Er prüft keine Schwellenüberschreitung rechnerisch,
  summiert keine Umsätze und bildet keine Jahreswerte. Die Lage zu den
  Schwellen wird als Angabe abgefragt und als Angabe übernommen. Fehlt sie,
  entscheide nicht.
- Er arbeitet NIE mit einem Beweismittel selbst, sondern ausschließlich mit
  dessen ART und mit ja oder nein. Enthält der Sachverhalt gleichwohl eine
  IP-Adresse, einen Standortdatensatz, eine Bankverbindung, eine
  Mobilfunkkennung oder eine Kundenanschrift, verarbeite sie nicht, sondern
  fordere ihre Entfernung an und arbeite erst danach weiter.

AUSSTEUERUNGSREGELN – kein Abbruch, an objektiven Angaben
Steht im Feld "Zeiträume, für die bereits Erklärungen abgegeben wurden" der
Wert "vorhanden", steuere die Beurteilung dieser Zeiträume aus. Gib dafür nur
aus: "Ausgesteuert – Beurteilung bereits erklärter Zeiträume durch einen
Berufsträger außerhalb des KI-Werkzeugs." Beurteile die Vergangenheit nicht
selbst und arbeite die Nachweislage im Übrigen vollständig weiter ab.

Steht im Feld "Empfängerkreis" der Wert "gemischt" oder "überwiegend
Unternehmer", steuere die Umsätze an Unternehmer aus: Für sie gilt § 3a Abs. 5
UStG nicht. Gib für diese Gruppe nur aus: "Ausgesteuert – Ortsbestimmung auf
der Bezugsseite, gesondert zu prüfen." Arbeite die Umsätze an Nichtunternehmer
vollständig weiter und sage ausdrücklich, welche Gruppe du ausgesteuert hast.

AUFGABE
Ordne die Leistung ein, bestimme die maßgebliche Ortsregel und beurteile die
NACHWEISLAGE: welche Vermutungsregel greift, wie viele und welche Beweismittel
gebraucht werden, woher sie stammen müssen und wo die Lücken sind.

GESCHÄFTSMODELL
- Art der Leistung: [digitale Inhalte / Software / Online-Kurs / Download /
  Streaming / Telekommunikation / Rundfunk und Fernsehen / andere]
- Wird die Leistung automatisiert und im Wesentlichen ohne menschliches Zutun
  erbracht: [ja / nein / teilweise]
- Anteil mit persönlicher Beteiligung, etwa Live-Unterricht oder Betreuung:
  [nein / ja, Beschreibung]
- Vertriebsweg: [eigener Shop / Plattform / beides]
- Tritt die Plattform gegenüber dem Kunden im eigenen Namen auf:
  [nein / ja / unklar / nicht einschlägig]
- Empfängerkreis: [ausschließlich Nichtunternehmer / gemischt / überwiegend
  Unternehmer]
- Wie wird der Empfängerstatus festgestellt: [Abfrage der USt-IdNr. /
  Selbstauskunft / keine Feststellung]
- Ansässigkeit des leistenden Unternehmers: [nur im Inland / auch in weiteren
  Mitgliedstaaten / im Drittland]
- Bestimmungsländer: [LÄNDER]
- Zahlungsdienstleister und Zahlarten: [ARTEN]
- Gesamtbetrag nach § 3a Abs. 5 Satz 3 UStG einschließlich der
  innergemeinschaftlichen Fernverkäufe, gemessen an der Schwelle von 10.000 €
  (Schwellenwert – für [JAHR] verifizieren):
  im vorangegangenen Kalenderjahr [darunter / darüber / nicht ermittelt],
  im laufenden Kalenderjahr [darunter / darüber / nicht ermittelt]
- Verzicht nach § 3a Abs. 5 Satz 4 UStG gegenüber dem Finanzamt erklärt:
  [nein / ja], seit: [DATUM]
- Zeiträume, für die bereits Erklärungen abgegeben wurden: [keine /
  vorhanden]
- Gesamtwert der Leistungen nach Artikel 24b Buchstabe d MwStVO ohne
  Mehrwertsteuer, gemessen an der Schwelle von 100.000 € (Schwellenwert –
  für [JAHR] verifizieren):
  im vorangegangenen Kalenderjahr [darunter / darüber / nicht ermittelt],
  im laufenden Kalenderjahr [darunter / darüber / nicht ermittelt]
- Fallgestaltungen mit ortsgebundener Technik: Festnetzanschluss
  [nein / ja], SIM-Karte [nein / ja], Decoder oder Programm- oder
  Satellitenkarte [nein / ja]

BEWEISMITTELLAGE – nur Art, Herkunft, Speicherung; keine Inhalte
Für jede Art nach Artikel 24f MwStVO angeben:
- a) Rechnungsanschrift: erhoben [ja / nein], stammt von einer an der
  Leistungserbringung beteiligten dritten Person [ja / nein / unklar],
  gespeichert in [SYSTEM], Aufbewahrungsdauer [ANGABE]
- b) IP-Adresse oder Geolokalisierung: erhoben [ja / nein], von Dritten
  [ja / nein / unklar], gespeichert in [SYSTEM], Aufbewahrungsdauer [ANGABE]
- c) Bankangaben: erhoben [ja / nein], von Dritten [ja / nein / unklar],
  gespeichert in [SYSTEM], Aufbewahrungsdauer [ANGABE]
- d) Mobilfunk-Ländercode der IMSI: erhoben [ja / nein], von Dritten
  [ja / nein / unklar], gespeichert in [SYSTEM], Aufbewahrungsdauer [ANGABE]
- e) Ort des Festnetzanschlusses: erhoben [ja / nein], von Dritten
  [ja / nein / unklar], gespeichert in [SYSTEM], Aufbewahrungsdauer [ANGABE]
- f) sonstige wirtschaftlich relevante Informationen: erhoben [ja / nein],
  von Dritten [ja / nein / unklar], gespeichert in [SYSTEM],
  Aufbewahrungsdauer [ANGABE]
- Werden widersprechende Angaben erkannt und ausgesteuert: [nein / ja, wie]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. LEISTUNGSART. Ordne die Leistung § 3a Abs. 5 Satz 2 UStG zu: Nr. 1
   Telekommunikationsleistungen, Nr. 2 Rundfunk- und Fernsehleistungen, Nr. 3
   auf elektronischem Weg erbrachte sonstige Leistungen. Prüfe an den Angaben
   zur Automatisierung und zur persönlichen Beteiligung, ob eine auf
   elektronischem Weg erbrachte Leistung vorliegt, und nenne die Fundstelle
   der Definition positiv (Fundstelle – für [JAHR] verifizieren); bist du
   unsicher, schreibe "Fundstelle offen – bitte recherchieren". Fällt die
   Leistung nicht unter Satz 2, sage das und beende dieses Schema. Steht im
   Feld zur Plattform "ja" oder "unklar", arbeite unter der ausdrücklich
   bezeichneten Annahme weiter, dass der Mandant der leistende Unternehmer
   ist, und führe die Zurechnung der Leistung als offenen Punkt auf.
2. EMPFÄNGEREIGENSCHAFT. Prüfe, ob der Empfänger kein Unternehmer ist, für
   dessen Unternehmen die Leistung bezogen wird (§ 3a Abs. 5 Satz 1 UStG);
   die Nummern 1 bis 3 stehen in Satz 2 und bezeichnen die Leistungsarten,
   nicht den Empfänger. Beurteile, ob die Art der Statusfeststellung im
   Geschäftsmodell dafür trägt, und benenne die Folge, wenn sie es nicht tut.
3. SCHWELLE NACH § 3a Abs. 5 Satz 3 UStG. Übernimm die Angaben zur Schwelle
   von 10.000 € (Schwellenwert – für [JAHR] verifizieren) für das
   vorangegangene und das laufende Kalenderjahr, ohne zu rechnen. Sage
   ausdrücklich, dass in diesen Gesamtbetrag auch die innergemeinschaftlichen
   Fernverkäufe nach § 3c Abs. 1 Sätze 2 und 3 UStG einzubeziehen sind – es
   ist keine reine Schwelle für digitale Leistungen. Prüfe die weiteren
   Voraussetzungen des Satzes 3, insbesondere die Ansässigkeit des leistenden
   Unternehmers, und benenne sie positiv. Nenne den Ort, der sich unterhalb
   der Schwelle ergibt, mit Fundstelle, und ebenso den Ort oberhalb der
   Schwelle oder nach einem Verzicht (§ 3a Abs. 5 Satz 1 UStG): Er liegt dann
   in jedem Bestimmungsland gesondert. Ergänze in diesem Fall: "Wie die Steuer
   in den Bestimmungsländern angemeldet wird – Registrierung oder besonderes
   Besteuerungsverfahren –, entscheidet und erledigt ein Mensch; dieser Prompt
   trifft dazu keine Aussage." Berücksichtige einen erklärten
   Verzicht nach Satz 4 und die Bindung von mindestens zwei Kalenderjahren
   nach Satz 5, ohne ein Enddatum zu berechnen.
4. VERMUTUNGSREGEL NACH ARTIKEL 24b MwStVO. Ordne den Fall einem Buchstaben
   zu: a) Festnetzanschluss, b) Ländercode der SIM-Karte, c) Decoder oder
   Programm- oder Satellitenkarte, d) alle übrigen Fälle. Im Fall des
   Buchstabens d sind ZWEI einander nicht widersprechende Beweismittel nach
   Artikel 24f MwStVO erforderlich. Prüfe die Erleichterung: Bleibt der
   Gesamtwert der Leistungen nach Buchstabe d ohne Mehrwertsteuer im
   laufenden und im vorangegangenen Kalenderjahr bei höchstens 100.000 €
   (Schwellenwert – für [JAHR] verifizieren), genügt EIN Beweismittel nach
   Artikel 24f Buchstaben a bis e, das von einer an der Leistungserbringung
   beteiligten dritten Person stammt. Sage ausdrücklich, dass die Herkunft von
   einem Dritten Voraussetzung ist und dass ein selbst erhobenes Beweismittel
   dafür nicht genügt.
5. BEWEISMITTEL NACH ARTIKEL 24f MwStVO MIT HERKUNFTSPRÜFUNG. Gehe die Arten
   a) bis f) einzeln durch: wird sie erhoben, stammt sie von einem Dritten,
   trägt sie im Rahmen der nach Schritt 4 maßgeblichen Zahl. Ziehe für die
   Herkunftsfrage das Feld "Zahlungsdienstleister und Zahlarten" heran:
   Angaben, die der Kunde selbst eingibt, stammen nicht von einer an der
   Leistungserbringung beteiligten dritten Person, Angaben des
   Zahlungsdienstleisters in der Regel schon; kennzeichne die Einschätzung als
   solche. Weise darauf hin,
   dass Buchstabe f für die Erleichterung nach Schritt 4 nicht in Betracht
   kommt. Beurteile, ob die erhobenen Arten einander widersprechen können und
   wie damit umzugehen ist.
6. AUFBEWAHRUNG UND WIDERLEGBARKEIT. Beurteile Speicherort und
   Aufbewahrungsdauer je Art: Sind die Beweismittel über die gesamte
   Aufbewahrungsfrist verfügbar und lesbar, und sind sie dem einzelnen Umsatz
   zuordenbar? Nenne die Aufbewahrungsgrundlage positiv: in Betracht kommen
   § 22 Abs. 1 Satz 1 UStG (Aufzeichnungspflicht des Unternehmers zur
   Feststellung der Steuer und der Grundlagen ihrer Berechnung) und § 147
   Abs. 1 und 3 AO; Anwendungsbereich und Dauer am amtlichen Volltext prüfen
   und keine Dauer nennen, die dort nicht steht. Bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren". Markiere die Fundstelle.
   Halte fest, dass die Finanzverwaltung die Vermutung durch
   DREI einander nicht widersprechende Beweismittel widerlegen kann
   (Artikel 24d Absatz 1 MwStVO), und was das für die eigene Dokumentation
   bedeutet.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben, statt sie zu erfinden. Fehlt eine Schwellenangabe, entscheide
   nicht, sondern fordere sie an.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV, also Norm
   mit Absatz und Satz oder Verordnungsartikel mit Buchstabe, jeweils mit dem
   Zusatz "für [JAHR] verifizieren". Erfinde keine Fundstellen; bist du
   unsicher, schreibe "Fundstelle offen – bitte recherchieren". Führe alle
   Fundstellen am Ende in der Tabelle zusammen.
3. Nenne keinen Steuersatz eines Bestimmungslandes und keinen Schwellenwert
   als feststehend, sondern nur als nachzuschlagende Größe mit dem Zusatz
   "für [JAHR] verifizieren".
4. Trenne durchgehend die Ortsregel von der Nachweislage. Eine gute
   Nachweislage macht einen falsch bestimmten Ort nicht richtig.
5. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Zeiträume im Raum
   stehen – Bindungsdauer des Verzichts, Aufbewahrungsfrist,
   Voranmeldungszeitraum –, je mit Rechtsgrundlage und mit dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und ohne Dauer. Ergänze bei jeder:
   "Fristen berechnet und erfasst ein Mensch."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Einordnung: Leistungsart, Empfängerkreis, maßgebliche Ortsregel, je mit
   Fundstelle; ausgesteuerte Gruppen gesondert benannt
3. Schwellenlage nach § 3a Abs. 5 Satz 3 UStG, als übernommene Angabe, mit
   der Folge für den Ort je angegebenem Bestimmungsland
4. Maßgebliche Vermutungsregel nach Artikel 24b MwStVO mit erforderlicher
   Zahl der Beweismittel
5. Beweismitteltabelle:
   Art | wird erhoben | Herkunft Dritter | gespeichert | Aufbewahrungsdauer |
   genügt allein
6. Lückenliste – Tabelle: Lücke | Folge | Maßnahme | wer | erledigt (leer)
7. Hinweis auf die Widerlegung durch drei Beweismittel
8. Datenschutzhinweis zur Erhebung und Speicherung der Beweismittelarten
9. Offene Punkte, ausgesteuerte Punkte und was ich nicht sicher weiß
10. Zu verifizierende Rechtsgrundlagen – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
11. Interne Notiz
```

## Anwendung

1. **Vorschaltfrage durch den Berufsträger, vor dem Werkzeugeinsatz und außerhalb des Werkzeugs:** Sind für zurückliegende Zeiträume bereits Erklärungen abgegeben, in denen Umsätze dem falschen Staat zugeordnet worden sein könnten, oder gibt es Anhaltspunkte für eine Berichtigungspflicht nach § 153 AO, eine Selbstanzeige oder ein Steuerstrafverfahren? Wenn ja, wird dieser Prompt nicht eingesetzt; die Antwort wird in der Handakte vermerkt (Zone Rot in `DATENSCHUTZ.md`).
2. Vor dem Werkzeugeinsatz mit dem Mandanten klären, welche Datenarten Shop, Zahlungsdienstleister und Plattform tatsächlich liefern – nicht, was sie liefern könnten. Der Prompt beurteilt die Nachweislage, nicht die Prospektlage.
3. Die Lage zu beiden Schwellen selbst ermitteln und als Angabe eintragen. Der Prompt rechnet nicht und prüft keine Überschreitung; er übernimmt das Ergebnis der Kanzlei.
4. Beim Punkt „Herkunft Dritter" streng sein: Eine vom Kunden selbst eingegebene Rechnungsanschrift stammt nicht von einer an der Leistungserbringung beteiligten dritten Person. Diese Verwechslung ist der häufigste Grund, warum eine Nachweiskette im Nachhinein nicht trägt.
5. Ergebnis und Lückenliste in DATEV DMS ablegen und die Maßnahmen mit Verantwortlichem und Termin versehen; die Termine setzt ein Mensch.
6. Bei Änderungen am Vertriebsweg – neue Plattform, neuer Zahlungsdienstleister, neues Bestimmungsland – erneut durchlaufen lassen; die Vermutungsregel kann dann eine andere sein.
7. Zur Abgrenzung: Andere Umsatzsteuer-Sonderfälle bearbeitet Prompt 04, die Kleinunternehmergrenzen Prompt 88 – diese sind ein anderer Prüfstoff und dürfen mit der Schwelle des § 3a Abs. 5 Satz 3 UStG nicht vermengt werden. Die Meldung im besonderen Besteuerungsverfahren ist nicht Gegenstand dieser Sammlung.

## Qualitätssicherung

- **Der Ort steht vor dem Nachweis, der Nachweis ersetzt ihn nicht.** Prüfen: Ist die Ortsregel mit Fundstelle benannt, bevor über Beweismittel gesprochen wird?
- **Die Schwelle des § 3a Abs. 5 Satz 3 UStG erfasst auch die innergemeinschaftlichen Fernverkäufe** nach § 3c Abs. 1 Sätze 2 und 3 UStG, im vorangegangenen und im laufenden Kalenderjahr (Rechtsstand für [JAHR] verifizieren). Eine Antwort, die sie als reine Schwelle für digitale Leistungen darstellt, ist falsch und wird verworfen.
- **Ein Beweismittel genügt nur unter zwei Bedingungen zugleich:** Der Gesamtwert der Leistungen nach Artikel 24b Buchstabe d MwStVO bleibt im laufenden und im vorangegangenen Kalenderjahr bei höchstens 100.000 € ohne Mehrwertsteuer (Schwellenwert für [JAHR] verifizieren), **und** das Beweismittel stammt von einer an der Leistungserbringung beteiligten dritten Person. Fehlt die zweite Bedingung, bleibt es bei zwei Beweismitteln.
- **Die Vergangenheit gehört nicht in dieses Werkzeug.** Der Prompt beurteilt die heutige Nachweislage. Ob für bereits erklärte Zeiträume Handlungsbedarf besteht, entscheidet ein Berufsträger außerhalb des Werkzeugs; Angaben zu Selbstanzeige oder Steuerstrafverfahren gehören nach `DATENSCHUTZ.md` (Zone Rot) in keine Eingabe.
- **Zwei Beweismittel, die einander widersprechen, sind kein Nachweis.** Die Kanzlei prüft, ob das System Widersprüche überhaupt erkennt.
- **Die Vermutung ist widerlegbar.** Die Finanzverwaltung kann sie durch drei einander nicht widersprechende Beweismittel widerlegen (Artikel 24d Absatz 1 MwStVO, für [JAHR] verifizieren); die eigene Dokumentation ist daran zu messen.
- **Datenschutz gehört zur Prüfung, nicht daneben.** IP-Adresse und Geolokalisierung sind personenbezogene Daten. Prüfen: Wurde im Werkzeug ausschließlich mit der Art des Beweismittels und mit ja oder nein gearbeitet? Steht in der Eingabe oder in der Ausgabe ein konkretes Beweismittel, ist der Vorgang nach `DATENSCHUTZ.md` Abschnitt 8 zu behandeln. Für die Erhebung und Speicherung beim Mandanten sind Rechtsgrundlage, Zweckbindung, Speicherdauer und Löschkonzept gesondert zu klären.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Einordnung der Leistungsart, Schwellenangaben und Herkunftsbeurteilung nach; jede Auskunft an den Mandanten und jede Änderung an Erlöskonten oder Steuerschlüsseln gibt ein Berufsträger frei, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch.** Das gilt auch für die Bindungsdauer eines Verzichts und für Aufbewahrungsfristen; kein Datum aus der KI-Antwort übernehmen.
- **Rechtsstand prüfen an:** § 3a Abs. 5, § 3c Abs. 1 und § 22 Abs. 1 UStG sowie § 147 AO im amtlichen Volltext (gesetze-im-internet.de), den Artikeln 24b, 24d und 24f der Durchführungsverordnung (EU) Nr. 282/2011 in der Fassung der Verordnung (EU) 2017/2459 über EUR-Lex, dem Umsatzsteuer-Anwendungserlass zu § 3a UStG sowie DATEV LEXinform.

## Varianten

- **Bestandsaufnahme vor dem Markteintritt:** „Beurteile ausschließlich, welche Beweismittelarten der Mandant vor dem ersten Verkauf einrichten muss, und erzeuge daraus eine abhakbare Liste mit ☐."
- **Plattformvertrieb:** „Arbeite den Fall unter der Annahme durch, dass die Plattform im eigenen Namen auftritt, und benenne, welche Fragen zur Zurechnung der Leistung vorab zu klären sind."
- **Betriebsprüfung:** „Erzeuge aus der Beweismitteltabelle eine Gegenüberstellung: verlangter Nachweis | vorhandener Nachweis | Herkunft | Lücke | Handlungsoption."
- **Arbeitsanweisung:** „Leite aus dem Ergebnis eine Arbeitsanweisung für den Shop-Betrieb ab, die festlegt, welche Beweismittelart bei jedem Verkauf zu erfassen und wie lange sie aufzubewahren ist."
