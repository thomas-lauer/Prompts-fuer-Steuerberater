# 117 – Einzweck- oder Mehrzweckgutschein: Einordnung und Folgen

**Problem:** Der Mandant gibt Gutscheine aus, und ob die Umsatzsteuer schon bei der Ausgabe oder erst bei der Einlösung entsteht, hängt an einer Einordnung, die meist erst gestellt wird, wenn die Buchung längst läuft.
**Rolle:** Sachbearbeiter Umsatzsteuer, Buchhaltung, Berufsträger
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Steuerschlüssel, Erlös- und Verbindlichkeitskonten in SKR03 und SKR04, Umsatzsteuer-Voranmeldung), DATEV Unternehmen online (Belegweg und Kassendaten bei ausgegebenen Gutscheinen), DATEV DMS (Gutscheinbedingungen, Muster des Gutscheins, Vertriebsvereinbarungen); Produktstand und Bezeichnung – für [JAHR] verifizieren
**Was du bereitstellen musst:** Muster oder Wortlaut des Gutscheins und der zugehörigen Bedingungen; Beschreibung des Sortiments, das damit bezogen werden kann; Angaben zu Einlösestellen, Einlöseraum, Ausgabe im eigenen oder fremden Namen, Übertragbarkeit, Restwert- und Verfallregelung, Ausstellungszeitpunkt und Vertriebsweg; die heutige Buchungspraxis für Ausgabe, Einlösung und Nichteinlösung.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Firmierung, Anschriften sowie die Namen von Vertriebspartnern und Einlösestellen durch Platzhalter ersetzen (`Mandant A`, `Vertriebspartner 1`, `Einlösestelle 1`). Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Gutscheincodes, Kartennummern und Kundenkonten bleiben draußen; für die Einordnung genügen Leistungsumfang, Einlösestellen, Einlöseraum, Namensverhältnis und Zeitpunkt. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug für ein konkretes Mandat und nicht nur als allgemeine Kanzlei-IT eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Umsatzsteuer-Spezialist in einer deutschen Steuerkanzlei. Du arbeitest
streng nach Prüfschema, in der vorgegebenen Reihenfolge, und behauptest nichts,
was du nicht aus den Angaben begründen kannst. Steht ein Merkmal nicht fest,
sagst du das, statt es zu unterstellen.

AUFGABE
Ordne den beschriebenen Gutschein als Einzweckgutschein oder als
Mehrzweckgutschein ein, begründe die Einordnung je Merkmal und leite die Folgen
für Steuerentstehung, Buchung, Nichteinlösung und Rechnungsstellung ab.

ABGRENZUNG – hier NICHT behandeln, sondern auf den genannten Prompt verweisen
- Andere Umsatzsteuer-Sonderfälle (Reverse-Charge, innergemeinschaftlicher
  Erwerb, Differenzbesteuerung, Kleinunternehmer): Prompt 04.
- Aufteilung eines Pauschalpreises auf unterschiedliche Steuersätze bei
  Kombiangeboten in der Gastronomie: Prompt 84.
- Unrichtiger Steuerausweis und seine Berichtigung: Prompt 87.

GUTSCHEIN
- Bezeichnung / interne Kennung: [BEZEICHNUNG]
- Was kann damit bezogen werden: [ANGABE]
- Berechtigt das Instrument nur zu einem Preisnachlass auf einen späteren
  Umsatz, ohne selbst Gegenleistung zu sein: [nein / ja / nicht bekannt]
- Verpflichtung, das Instrument als vollständige oder teilweise Gegenleistung
  anzunehmen: [ja / nein / nicht bekannt]
- Auf dem Instrument oder in den zusammenhängenden Unterlagen angegeben:
  [Liefergegenstand / sonstige Leistung / Identität des leistenden
  Unternehmers / keine dieser Angaben]
- Sortiment: [einheitlicher Steuersatz / unterschiedliche Steuersätze /
  nicht bekannt]
- Auch steuerfreie oder nicht steuerbare Leistungen beziehbar:
  [nein / ja / nicht bekannt]
- Einlösbar: [nur beim Aussteller / auch bei Dritten], bei welchen: [ANGABE]
- Einlösbar: [nur im Inland / auch im Ausland / nicht bekannt]
- Ausgabe erfolgt im: [eigenen Namen / fremden Namen], für: [ANGABE]
- Leistung wird erbracht durch: [den Aussteller / einen anderen Unternehmer]
- Übertragbar auf Dritte: [nein / ja]
- Wird der Gutschein weiterverkauft (Vertriebskette): [nein / ja],
  Stufen: [ANGABE]
- Restwert bei Teileinlösung: [verfällt / bleibt bestehen / wird ausgezahlt]
- Verfallregelung: [kein Verfall / Verfall nach ANGABE]
- Zeitpunkt der Ausstellung: [DATUM]

ABRECHNUNG UND BUCHUNG
- Über die Ausgabe wurde mit gesondertem Steuerausweis abgerechnet: [nein / ja]
- Heutige Buchungspraxis bei Ausgabe und bei Einlösung: [ANGABE]
- Heutige Behandlung nicht eingelöster Gutscheine: [ANGABE]

AUSSTEUERUNGSREGEL – kein Abbruch, an einer objektiven Angabe
Steht im Feld "Über die Ausgabe wurde mit gesondertem Steuerausweis
abgerechnet" ein "ja", gib zum Punkt Berichtigung bereits erteilter
Abrechnungen nur aus: "Ausgesteuert – Prüfung durch einen Berufsträger
außerhalb des KI-Werkzeugs; Vorgehen nach Prompt 87." Beende die Bearbeitung
NICHT, arbeite alle übrigen Schritte weiter und führe den ausgesteuerten Punkt
gesondert auf.

PRÜFSCHEMA – in dieser Reihenfolge, keinen Schritt überspringen
1. GUTSCHEIN ODER PREISNACHLASSINSTRUMENT (§ 3 Abs. 13 UStG). Prüfe zuerst
   anhand des Ausstellungszeitpunkts, ob die Regelung überhaupt anwendbar ist
   (§ 27 Abs. 23 UStG: Gutscheine, die nach dem 31.12.2018 ausgestellt werden).
   Prüfe dann § 3 Abs. 13 Satz 1 UStG: Nr. 1 die Verpflichtung, das Instrument
   als vollständige oder teilweise Gegenleistung anzunehmen, und Nr. 2 die
   Angabe des Liefergegenstands, der sonstigen Leistung oder der Identität des
   leistenden Unternehmers auf dem Instrument selbst oder in damit
   zusammenhängenden Unterlagen. Prüfe zuletzt § 3 Abs. 13 Satz 2 UStG:
   Instrumente, die lediglich zu einem Preisnachlass berechtigen, sind KEINE
   Gutscheine. Dieser Schritt wird in der Praxis übersprungen – überspringe ihn
   nicht. Ergibt er, dass kein Gutschein vorliegt, gib das als Ergebnis aus und
   arbeite die Schritte 2 bis 7 nicht weiter ab; die Schritte 8 und 9
   bleiben.
2. ORT der Lieferung oder der sonstigen Leistung. Steht er zum Zeitpunkt der
   Ausstellung für ALLE mit dem Gutschein beziehbaren Leistungen fest? Werte
   die Angaben zu Einlösestellen und Einlöseraum aus.
3. GESCHULDETE STEUER. Steht sie zum Zeitpunkt der Ausstellung für ALLE
   beziehbaren Leistungen fest? Werte die Angaben zum Sortiment und zu
   steuerfreien oder nicht steuerbaren Leistungen aus. Nenne keinen Steuersatz
   als Zahl; schreibe stattdessen "Steuersatz – für [JAHR] verifizieren".
4. EINORDNUNG. Einzweckgutschein nach § 3 Abs. 14 Satz 1 UStG, wenn Ort der
   Lieferung oder der sonstigen Leistung UND die für diese Umsätze geschuldete
   Steuer zum Zeitpunkt der Ausstellung feststehen. Mehrzweckgutschein nach
   § 3 Abs. 15 Satz 1 UStG ist jeder Gutschein im Sinne des Abs. 13, der kein
   Einzweckgutschein ist. Maßgeblich sind die Verhältnisse zum Zeitpunkt der
   Ausstellung. Die Angaben zu Übertragbarkeit und Vertriebskette sprechen
   daher WEDER für noch gegen die Einordnung: Es kommt nicht darauf an, ob der
   Gutschein nach seiner Ausgabe zwischen Steuerpflichtigen übertragen werden
   kann, die im eigenen Namen handeln und in anderen Mitgliedstaaten ansässig
   sind als demjenigen, in dem der Leistungsort liegt (BFH, BESCHLUSS vom
   25.06.2025 – XI R 14/24 (XI R 21/21),
   ECLI:DE:BFH:2025:B.250625.XIR14.24.0; Vorabentscheidung EuGH
   vom 18.04.2024 – C-68/23 "Finanzamt O", EU:C:2024:342). Zitiere die
   BFH-Entscheidung als Beschluss, NICHT als Urteil, und bezeichne die
   EuGH-Rechtssache als "Finanzamt O".
5. ZEITPUNKT DER STEUERENTSTEHUNG. Beim Einzweckgutschein gilt die Übertragung
   als die Lieferung oder sonstige Leistung selbst, auf die sich der Gutschein
   bezieht (§ 3 Abs. 14 Satz 2 UStG); die spätere tatsächliche Leistung gilt
   nicht als unabhängiger Umsatz (§ 3 Abs. 14 Satz 5 UStG). Beim
   Mehrzweckgutschein unterliegt nur die tatsächliche Leistung bei Einlösung
   der Umsatzsteuer, jede vorangegangene Übertragung nicht (§ 3 Abs. 15 Satz 2
   UStG). Nenne für den Zeitpunkt der Steuerentstehung zusätzlich § 13 Abs. 1
   Nr. 1 UStG – Buchst. a bei der Berechnung nach vereinbarten Entgelten,
   Buchst. b bei der Berechnung nach vereinnahmten Entgelten (§ 20 UStG) –
   und
   grenze ihn ausdrücklich ab: § 3 Abs. 14 und 15 UStG bestimmen, welcher
   Vorgang als Leistung gilt, § 13 UStG, wann die Steuer daraus entsteht.
6. HANDELN IM EIGENEN ODER FREMDEN NAMEN. Werte die Angaben zu Namensverhältnis,
   leistendem Unternehmer und Vertriebskette aus und ordne sie § 3 Abs. 14
   Sätze 2 bis 4 UStG zu (Übertragung im eigenen Namen; Übertragung im fremden
   Namen; Leistungserbringung durch einen anderen Unternehmer als denjenigen,
   der den Gutschein ausgestellt hat). Gib je Vertriebsstufe aus, wer welchen
   Umsatz ausführt.
7. NICHTEINLÖSUNG. Behandle den Fall gesondert, auch wenn im Sachverhalt nicht
   danach gefragt wird: Beim Einzweckgutschein ist die Steuer bereits mit der
   Übertragung entstanden und bleibt es, wenn der Gutschein nicht eingelöst
   wird. Beim Mehrzweckgutschein entsteht mangels tatsächlicher Leistung keine
   Steuer. Werte dazu die Verfall- und Restwertregelung aus. Ob ein
   einbehaltener Betrag darüber hinaus zu einer Entgeltminderung führt, ist
   nicht Gegenstand dieses Prompts – gib die Frage als offenen Punkt aus.
8. ABGLEICH MIT DER HEUTIGEN PRAXIS. Stelle die Angaben "Heutige
   Buchungspraxis bei Ausgabe und bei Einlösung" und "Heutige Behandlung nicht
   eingelöster Gutscheine" dem Ergebnis der Schritte 5 und 7 gegenüber.
   Benenne jede Abweichung und ihre Richtung (zu früh oder zu spät versteuert)
   sowie die Zeiträume, die betroffen sein können – ohne Betrag, ohne Frist
   und ohne eigene Berichtigungsempfehlung. Steht dort keine Angabe, schreibe
   "keine Buchungspraxis mitgeteilt".
9. RECHNUNGSSTELLUNG. Leite ab, was auf der Abrechnung über Ausgabe und
   Einlösung stehen darf. Weise ausdrücklich darauf hin, dass ein Steuerausweis
   über einen Mehrzweckgutschein, der wie ein Einzweckgutschein abgerechnet
   wurde, ein Fall des § 14c UStG sein kann, und verweise für Prüfung und
   Berichtigung auf Prompt 87.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben, statt sie zu erfinden.
2. Unterscheide zwei Fälle und sage ausdrücklich, welcher vorliegt.
   (a) DATENLÜCKE: Fehlt eine Angabe des Sachverhaltsbogens oder lautet sie
   "nicht bekannt", gib für dieses Merkmal einen UNSICHERHEITSVERMERK aus,
   benenne, welche Auskunft fehlt und wer sie beschaffen kann, und leite aus
   der Datenlücke KEINE Einordnung ab.
   (b) TATBESTANDSMERKMAL: Ergibt der Sachverhalt dagegen, dass der Ort der
   Leistung oder die geschuldete Steuer zum Zeitpunkt der Ausstellung objektiv
   nicht feststehen, ist das keine Unsicherheit, sondern die Voraussetzung des
   § 3 Abs. 15 Satz 1 UStG: Der Gutschein ist dann Mehrzweckgutschein, und du
   sagst das als Ergebnis.
3. Rechne nicht. Berechne keine Steuerbeträge, keine Entgelte und keine
   Fristen. Nenne keinen Steuersatz und keinen Betragswert als Zahl ohne den
   Zusatz "für [JAHR] verifizieren".
4. Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Entscheidung mit Datum und Aktenzeichen), jeweils mit dem Zusatz
   "für [JAHR] verifizieren", und führe sie am Ende in der Tabelle "Zu
   verifizierende Rechtsgrundlagen" auf. Erfinde keine Paragrafen,
   BMF-Schreiben oder Aktenzeichen; bist du dir nicht sicher, schreibe
   "Fundstelle offen – bitte recherchieren".
5. Formuliere jede Aussage über die künftige Verwendung des Gutscheins als
   Vermutung und kennzeichne sie als solche.

AUSGABEFORMAT
1. (Einschätzung der Eindeutigkeit)
2. (Einordnung je Merkmal) – Tabelle:
   Merkmal | Angabe aus dem Sachverhalt | steht zum Zeitpunkt der Ausstellung
   fest (ja / nein / unklar) | Folge für die Einordnung | Fundstelle
3. (Ergebnis) – Einzweckgutschein, Mehrzweckgutschein oder kein Gutschein im
   Sinne des § 3 Abs. 13 UStG, in einem Satz, mit Begründung in höchstens fünf
   Sätzen.
4. (Unsicherheitsvermerk) – nur für Merkmale, zu denen eine Angabe FEHLT:
   was fehlt, wer es beschafft, wie sich das Ergebnis bei beiden Auslegungen
   ändern würde. Merkmale, die nach dem Sachverhalt objektiv nicht feststehen,
   gehören nicht hierher, sondern in das Ergebnis.
5. (Folgen für Steuerentstehung und Buchung) – Zeitpunkt der Entstehung,
   betroffener Vorgang je Vertriebsstufe, Hinweis auf die zu prüfenden Konten
   und Steuerschlüssel in [SKR03 / SKR04] ohne Kontonummern zu erfinden.
6. (Behandlung bei Nichteinlösung)
7. (Abweichung von der heutigen Praxis) – je Vorgang: heutige Buchung,
   Ergebnis nach diesem Schema, Abweichung, betroffene Zeiträume.
8. (Hinweise zur Rechnung) – einschließlich des § 14c-Risikos und des
   Verweises auf Prompt 87.
9. (Offene Punkte und ausgesteuerte Punkte)
10. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. **Vorschaltfrage außerhalb des Werkzeugs:** Der Berufsträger klärt vorab, ob der Vorgang bereits in eine Berichtigungsanzeige, eine Selbstanzeige oder ein Steuerstrafverfahren mündet. Solche Angaben gehören nach `DATENSCHUTZ.md` (Zone Rot) in kein KI-Werkzeug; die Antwort wird in der Handakte vermerkt, und der Prompt wird in diesem Fall nicht eingesetzt.
2. Den Gutschein und die zugehörigen Bedingungen im Wortlaut auswerten, nicht die Beschreibung des Mandanten. Was ein Gutschein leisten darf, steht in den Bedingungen; was der Mandant erzählt, ist oft die Vertriebsabsicht.
3. Das Feld zum Preisnachlass ernst nehmen: Rabattkarten, Bonuspunkte und Nachlassaktionen sind keine Gutscheine im Sinne des § 3 Abs. 13 UStG und laufen sonst durch das ganze Schema.
4. Bei mehreren Gutscheinarten je Art einen eigenen Lauf machen. Eine Sammelbetrachtung erzeugt eine Einordnung, die für keine der Arten stimmt.
5. Das Ergebnis in der Akte festhalten, mit dem Ausstellungszeitpunkt als Bezugsgröße – ändert der Mandant später das Sortiment oder die Einlösestellen, ist die Einordnung für neu ausgegebene Gutscheine erneut zu prüfen.

## Qualitätssicherung

- **Der Zeitpunkt der Ausstellung ist der Beurteilungszeitpunkt.** Prüfen, ob die Einordnung tatsächlich auf die Verhältnisse bei Ausstellung gestützt ist und nicht auf das, was der Mandant später beobachtet hat (BFH, Beschluss vom 25.06.2025 – XI R 14/24 (XI R 21/21), Streitjahr 2019, Vorinstanz Schleswig-Holsteinisches FG 10.03.2021 – 4 K 62/19 – für [JAHR] verifizieren). Der zugrunde liegende Sachverhalt wird vor jeder Übertragung auf den eigenen Fall im Volltext der Entscheidung nachgelesen; aus dem Leitsatz allein folgt keine Aussage über die Vergleichbarkeit.
- **Zitierweise kontrollieren:** Die BFH-Entscheidung ist ein **Beschluss**, kein Urteil. Die EuGH-Rechtssache C-68/23 wird amtlich als **"Finanzamt O"** bezeichnet. Beide Angaben in der Ausgabe nachlesen und falsche Bezeichnungen korrigieren, bevor der Text weiterverwendet wird.
- **Nicht feststehen ist ein Ergebnis, kein Zweifel.** Steht die geschuldete Steuer oder der Ort zum Ausstellungszeitpunkt objektiv nicht fest, ist der Gutschein Mehrzweckgutschein (§ 3 Abs. 15 Satz 1 UStG – für [JAHR] verifizieren). Eine Antwort, die deshalb gar keine Einordnung trifft, ist unbrauchbar; nur eine fehlende Auskunft rechtfertigt den Unsicherheitsvermerk.
- **Kein Steuersatz und kein Betrag ohne Marker.** Der Prompt rechnet nicht; jede Zahl, die dennoch in der Ausgabe steht, wird gestrichen oder gegen den Rechtsstand geprüft.
- **Das Sortiment ist das Einfallstor.** Ein Gutschein, mit dem auch nur eine Leistung mit abweichendem Steuersatz oder eine steuerfreie Leistung bezogen werden kann, verändert das Ergebnis. Die Prüfung erfolgt anhand des tatsächlichen Angebots, nicht anhand der Absicht.
- **Nichteinlösung gesondert entscheiden lassen.** Die Behandlung nicht eingelöster Gutscheine wirkt sich auf jeden Jahresabschluss aus; die Buchung wird vom Berufsträger festgelegt und nicht aus der Modellantwort übernommen.
- **Vier-Augen-Prinzip:** Die Einordnung wird von einer zweiten Person gegen den Wortlaut der Gutscheinbedingungen nachvollzogen; die Freigabe erteilt ein Berufsträger (Freigabestufe 3 in `DATENSCHUTZ.md`), bevor die Buchungspraxis geändert oder der Mandant informiert wird.
- **Fristen berechnet und erfasst ein Mensch.** Ergibt sich aus der Einordnung Handlungsbedarf für bereits übermittelte Voranmeldungen oder Erklärungen, werden die Fristen außerhalb des Werkzeugs berechnet und im Fristenprogramm erfasst.

## Varianten

- **Sortimentsprüfung:** "Prüfe nur, ob mit dem beschriebenen Sortiment die geschuldete Steuer zum Zeitpunkt der Ausstellung feststeht, und gib eine Liste der Leistungen aus, die dem entgegenstehen könnten."
- **Gutscheinbedingungen entwerfen:** "Formuliere aus der gewünschten Einordnung heraus die Punkte, die in den Gutscheinbedingungen geregelt sein müssen – als Entwurfshinweise für den Berufsträger, nicht als fertige Bedingungen."
- **Vertriebskette:** "Stelle für eine Kette aus Aussteller, Vertriebspartner und Einlösestelle je Stufe dar, wer welchen Umsatz ausführt und wer welche Abrechnung erteilt."
- **Mandantenschreiben:** "Erzeuge aus dem Ergebnis ein Mandantenschreiben in Sie-Form, höchstens 300 Wörter, ohne Paragrafenketten, mit einem konkreten nächsten Schritt."
- **Bestandsaufnahme:** "Erzeuge einen Fragebogen, mit dem der Mandant alle heute ausgegebenen Gutscheinarten erfasst – je Art die Merkmale des Prüfschemas, in Alltagssprache."
