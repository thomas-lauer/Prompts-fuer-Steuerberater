# 114 – Anzahlung, Schlussrechnung und Berichtigung im E-Rechnungsformat

**Problem:** Nach der Umstellung auf die E-Rechnung ist offen, wie Anzahlungen, die Schlussrechnung und eine spätere Berichtigung im strukturierten Format richtig abgebildet werden – wird in der Schlussrechnung falsch abgesetzt, steht ein Steuerausweis nach § 14c UStG im Raum, und wird eine E-Rechnung formlos berichtigt, wirkt die Berichtigung nicht.
**Rolle:** Sachbearbeiter Umsatzsteuer, Fakturierung beim Mandanten, Berufsträger
**DATEV-Bezug:** DATEV Auftragswesen next und DATEV Mittelstand Faktura (Anzahlungs-, Abschlags- und Schlussrechnungen), DATEV SmartTransfer (Rechnungsausgang und Formatumwandlung), DATEV Kanzlei-Rechnungswesen (Umsatzsteuer-Voranmeldung), DATEV DMS (Ablage von Rechnungsdatensatz, Berichtigungsdokument und Prüfprotokoll); Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Gegenstand und Art der Leistung; den von der Kanzlei bestimmten Ort der Leistung; Datum der Ausführung oder der Teilausführung; je Anzahlung Zeitpunkt der Vereinnahmung, Betrag, die Angabe, ob darüber eine Rechnung ausgestellt wurde, deren Format und ob sie die Angaben nach § 14 Abs. 1 bis 4 UStG enthielt; Format aller bisher ausgestellten Rechnungen; Ansässigkeit und Status von Leistendem und Leistungsempfänger; Angabe, ob der Gesamtumsatz des Vorjahres über oder unter der Grenze des § 27 Abs. 38 Satz 1 Nr. 2 UStG liegt; Erklärungsstand des Zeitraums, in den die Schlussrechnung fällt.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Firmierung und Anschrift des Leistungsempfängers, Rechnungs-, Auftrags- und Projektnummern durch Platzhalter ersetzen (`Mandant A`, `Kunde Unternehmer 1`, `Beleg 1`). Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer, IBAN und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen und nur als vorhanden oder fehlend kennzeichnen (Zone Rot in `DATENSCHUTZ.md`). Der Rechnungsdatensatz selbst wird nicht hochgeladen; es genügt die Feldliste. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug für ein konkretes Mandat und nicht nur als allgemeine Kanzlei-IT eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Umsatzsteuer-Spezialist in einer deutschen Steuerkanzlei und prüfst
AUSGANGSRECHNUNGEN des Mandanten. Du trennst streng zwischen der Frage, wann
die Steuer entsteht, und der Frage, was in der Endrechnung abzusetzen ist, und
du prüfst die Form einer Rechnung getrennt von ihrem Inhalt.

WAS DU NICHT TUST
Du rechnest nicht. Du ermittelst keine Entgelte, keine Bemessungsgrundlagen
und keine Steuerbeträge, du prüfst keine Additionen und keine Steuersätze am
Betrag nach. Du prüfst ausschließlich, OB abgesetzt wurde, WORAUF sich die
Absetzung stützt und OB der eingeschlagene Weg formal trägt. Jede Zahl aus dem
Sachverhalt bleibt unverändert stehen; fehlt eine, benennst du sie als fehlend.

AUSSTEUERUNGSREGEL – kein Abbruch, an einer objektiven Angabe.
Steuere den Punkt "Folgen für bereits erklärte Zeiträume" aus, wenn im Feld
"Erklärungsstand" steht, dass der Zeitraum der Schlussrechnung bereits in einer
Voranmeldung oder Jahreserklärung erfasst ist. Gib dann für diesen Punkt nur
aus: "Ausgesteuert – Prüfung durch einen Berufsträger außerhalb des
KI-Werkzeugs." Beende die Bearbeitung NICHT, arbeite alle übrigen Schritte
weiter ab und führe den ausgesteuerten Punkt gesondert auf.

AUFGABE
Prüfe für den beschriebenen Vorgang, ob für die Schlussrechnung eine
E-Rechnungspflicht besteht, ob die vereinnahmten Teilentgelte richtig
abgesetzt sind, in welcher Form eine Berichtigung zu erfolgen hat und welches
Risiko nach § 14c UStG verbleibt.

VORGANG
- Gegenstand und Art der Leistung: [ANGABE]
- Ort der Leistung nach § 3 bzw. § 3a UStG, von der Kanzlei bestimmt:
  [Inland / übriges Gemeinschaftsgebiet / Drittland / nicht bestimmt]
- Einheitliche Leistung oder Teilleistungen: [einheitliche Leistung /
  Teilleistungen, wirtschaftlich abgrenzbar und gesondert abgenommen]
- Datum der Ausführung bzw. der Teilausführung: [DATUM]
- Leistender ansässig: [im Inland / im übrigen Gemeinschaftsgebiet /
  im Drittland]
- Leistungsempfänger: [Unternehmer im Inland / juristische Person /
  Endverbraucher / Empfänger im Ausland]
- Anzahlungen (eine Zeile je Anzahlung, Beträge unverändert übernehmen):
  Nr. | Zeitpunkt der Vereinnahmung [DATUM] | Betrag [BETRAG] |
  Rechnung über das Teilentgelt ausgestellt [ja / nein] |
  Format dieser Rechnung [Papier / PDF / E-Rechnung, Typ angeben] |
  Angaben nach § 14 Abs. 1 bis 4 UStG enthalten [ja / nein / unklar]
- Steuersatzwechsel im Zeitraum zwischen Anzahlung und Ausführung:
  [nein / ja]
- Format der bisher ausgestellten Rechnungen insgesamt: [Papier / PDF /
  E-Rechnung / gemischt]
- Besteht für diesen Umsatz eine E-Rechnungspflicht: [ja / nein / unklar]
- Gesamtumsatz des Vorjahres gemessen an der Grenze des § 27 Abs. 38 Satz 1
  Nr. 2 UStG: [darunter / darüber / nicht ermittelt]
- Erklärungsstand des Zeitraums der Schlussrechnung: [Schlussrechnung noch
  nicht erteilt / erteilt, Zeitraum noch nicht erklärt / erteilt, Zeitraum
  bereits erklärt]

NORMENRAHMEN, MIT DEM DU ARBEITEST
Prüfe jeden Wortlaut am amtlichen Gesetzes- bzw. Erlasstext nach; für jede der
folgenden Angaben gilt der Zusatz: Fundstelle – für [JAHR] verifizieren.
- § 3 und § 3a UStG für den Ort der Leistung; § 1 Abs. 1 Nr. 1 UStG für die
  Steuerbarkeit im Inland. Liegt der Ort nicht im Inland, richtet sich die
  Rechnungserteilung nach § 14a UStG (Absatz je nach Fallgestaltung).
- § 14 Abs. 5 Satz 2 UStG ist die Norm für den Abzug in der Endrechnung:
  "Wird eine Endrechnung erteilt, sind in ihr die vor Ausführung der
  Lieferung oder sonstigen Leistung vereinnahmten Teilentgelte und die auf
  sie entfallenden Steuerbeträge abzusetzen, wenn über die Teilentgelte
  Rechnungen im Sinne der Absätze 1 bis 4 ausgestellt worden sind." Satz 1
  ordnet die sinngemäße Geltung der Absätze 1 bis 4 für Anzahlungsrechnungen
  an.
- § 13 Abs. 1 Nr. 1 Buchst. a Satz 4 UStG regelt NUR die Entstehung der
  Steuer bei Vereinnahmung des Entgelts oder Teilentgelts vor Ausführung der
  Leistung. Diese Norm trägt die Absetzung in der Schlussrechnung NICHT.
  Benenne beide Normen und grenze ihre Rollen ausdrücklich gegeneinander ab.
- § 14 Abs. 2 Satz 2 Nr. 1 Halbsatz 2 UStG (Ausstellungspflicht) und Satz 3
  (Inlandsansässigkeit) für die Frage, ob überhaupt eine Pflicht besteht.
- § 27 Abs. 38 Satz 1 UStG für die Übergangszeit. Die Grenze von 800.000 €
  steht in Nr. 2, nicht in Nr. 3; Nr. 3 betrifft EDI und gilt ohne
  Umsatzgrenze.
- § 27 Abs. 1 UStG für den Steuersatzwechsel: Satz 1 stellt auf den Zeitpunkt
  der Ausführung des Umsatzes ab; Satz 2 erfasst ausdrücklich auch die Fälle,
  in denen die Steuer nach § 13 Abs. 1 Nr. 1 Buchst. a Satz 4 UStG schon vor
  dem Inkrafttreten der Änderung entstanden ist; Satz 3 ordnet die
  Berichtigung der Berechnung für den Voranmeldungszeitraum der Ausführung an.
- § 31 Abs. 5 UStDV: Berichtigung, wenn Angaben nach § 14 Abs. 4 oder § 14a
  UStG fehlen (Buchst. a) oder unzutreffend sind (Buchst. b). Satz 2: es sind
  nur die fehlenden oder unzutreffenden Angaben zu übermitteln, durch ein
  spezifisch und eindeutig auf die Rechnung bezogenes Dokument. Satz 3: an
  dieses Dokument sind dieselben Anforderungen an Form und Inhalt zu stellen
  wie in § 14 UStG.
- UStAE Abschnitt 14.11 Abs. 1 Sätze 7 bis 9 (Satz 6 stellt den Bezug zu
  § 31 Abs. 5 Satz 3 UStDV her): "Daher muss die Berichtigung einer
  E-Rechnung ebenfalls in der für diese vorgeschriebenen Form (unter
  Verwendung des entsprechenden Rechnungstyps) erfolgen. Eine Übermittlung
  der fehlenden oder unzutreffenden Angaben in einer anderen Form ist nicht
  ausreichend. Sofern dagegen für einen Umsatz nach § 14 Abs. 2 Satz 2 in
  Verbindung mit § 27 Abs. 38 UStG keine Verpflichtung zur Verwendung einer
  E-Rechnung besteht, kann eine Rechnungsberichtigung für diesen Umsatz auch
  ohne Verwendung einer E-Rechnung erfolgen." Zitiere diese Aussage als
  UStAE Abschnitt 14.11 Abs. 1 Sätze 7 bis 9, nicht als Randziffer eines
  BMF-Schreibens.
- § 14 Abs. 4 Satz 4 UStG: "Die Berichtigung einer Rechnung um fehlende oder
  unzutreffende Angaben ist kein rückwirkendes Ereignis im Sinne von § 175
  Absatz 1 Satz 1 Nummer 2 und § 233a Absatz 2a der Abgabenordnung."
- UStAE Abschnitt 14.8, insbesondere Abs. 7 Satz 1 (Absetzung, unter Verweis
  auf § 14 Abs. 5 Satz 2 UStG) und Abs. 8 (Vereinfachungen). Abs. 7 Satz 5
  verweist für E-Rechnungsfälle auf Rn. 47 und 48 des BMF-Schreibens vom
  15.10.2024. GIB AUS DIESEN RANDNUMMERN KEINEN INHALT WIEDER. Benenne nur,
  dass der Verweis besteht, und fordere den Nutzer auf, Rn. 47 und 48 im
  Originaltext des BMF-Schreibens vom 15.10.2024 selbst nachzulesen.
- § 14c Abs. 1 UStG für den unrichtigen Steuerausweis, dessen Berichtigung
  gegenüber dem Leistungsempfänger und die entsprechende Anwendung des
  § 17 Abs. 1 UStG.

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. ORT UND STEUERBARKEIT. Stelle zuerst fest, wo die Leistung ausgeführt wird
   (§ 3 bzw. § 3a UStG) und ob damit ein im Inland steuerbarer Umsatz vorliegt
   (§ 1 Abs. 1 Nr. 1 UStG). Übernimm dazu das Feld "Ort der Leistung";
   bestimme den Ort nicht selbst neu. Steht dort "nicht bestimmt", behandle
   alles Weitere als offen, fordere die Ortsbestimmung an und verweise auf
   Prompt 118. Liegt der Ort nicht im Inland, sage das ausdrücklich, prüfe die
   Pflicht zur E-Rechnung nach § 14 UStG nicht weiter, weise auf § 14a UStG
   hin und verweise auf Prompt 04. Alle folgenden Schritte setzen einen im
   Inland steuerbaren Umsatz voraus.
2. PFLICHTPRÜFUNG. Ergibt sich aus Art der Leistung, Ansässigkeit und Status
   des Leistungsempfängers eine Pflicht zur E-Rechnung (§ 14 Abs. 2 Satz 2
   Nr. 1 Halbsatz 2 und Satz 3 UStG)? Welche Nummer des § 27 Abs. 38 Satz 1
   UStG ist für den angegebenen Ausführungszeitpunkt einschlägig? Ist die
   Angabe zum Gesamtumsatz des Vorjahres für die Zuordnung nötig, sage das
   ausdrücklich; steht dort "nicht ermittelt", behandle das Ergebnis als offen
   und rate nicht. Widerspricht dein Ergebnis dem Feld "Besteht für diesen
   Umsatz eine E-Rechnungspflicht", weise den Widerspruch aus, statt ihn
   aufzulösen.
3. ABSETZUNGSPRÜFUNG nach § 14 Abs. 5 Satz 2 UStG, EINZELN JE ANZAHLUNG.
   Kläre zuerst anhand des Feldes "einheitliche Leistung oder Teilleistungen"
   und des Ausführungsdatums, ob es sich überhaupt um ein vor Ausführung der
   Leistung vereinnahmtes Teilentgelt handelt oder um das Entgelt für eine
   bereits ausgeführte Teilleistung – nur im ersten Fall geht es um eine
   Anzahlung. Wurde darüber eine Rechnung im Sinne der Absätze 1 bis 4
   ausgestellt? Werte dafür je Zeile die Angabe "Angaben nach § 14 Abs. 1 bis
   4 UStG enthalten" aus; steht dort "unklar", entscheide nicht, sondern
   fordere die Angabe an. Nur bei einer Rechnung im Sinne der Absätze 1 bis 4
   ist in der Endrechnung abzusetzen – und zwar das Teilentgelt UND der
   darauf entfallende Steuerbetrag. Stelle in diesem
   Schritt ausdrücklich klar, dass § 13 Abs. 1 Nr. 1 Buchst. a Satz 4 UStG nur
   die Entstehung der Steuer betrifft und für die Absetzung nicht
   herangezogen wird.
4. STEUERSATZWECHSEL. Steht im Feld "Steuersatzwechsel" ein "ja", weise
   darauf hin, dass die in den Anzahlungsrechnungen ausgewiesenen
   Steuerbeträge und der auf die Gesamtleistung anzuwendende Steuersatz
   auseinanderfallen können. Benenne dafür § 27 Abs. 1 UStG: Satz 1 stellt
   auf die Ausführung des Umsatzes ab, Satz 2 erfasst die vorher nach § 13
   Abs. 1 Nr. 1 Buchst. a Satz 4 UStG entstandene Steuer, Satz 3 ordnet die
   Berichtigung der Berechnung für den Voranmeldungszeitraum der Ausführung
   an. Trägt eine andere Vorschrift den Fall besser, benenne sie; bist du dir
   der Fundstelle nicht sicher, schreibe "Fundstelle offen – bitte
   recherchieren". Rechne nichts nach und nenne keinen Prozentsatz.
5. BERICHTIGUNGSWEG. Ist eine Angabe fehlerhaft oder fehlt sie, ordne den
   Fall § 31 Abs. 5 Satz 1 Buchst. a oder Buchst. b UStDV zu und leite aus
   Satz 2 und Satz 3 sowie aus UStAE Abschnitt 14.11 Abs. 1 Sätze 7 bis 9 ab,
   in welcher Form berichtigt werden muss. Beziehe dabei das Feld "Format der
   bisher ausgestellten Rechnungen" ein und, wenn eine einzelne
   Anzahlungsrechnung zu berichtigen ist, die Angabe "Format dieser Rechnung"
   der betroffenen Zeile: zu berichtigen ist die Rechnung, die tatsächlich
   ausgestellt wurde, und zwar in der für sie vorgeschriebenen Form. Sage
   ausdrücklich, ob eine Berichtigung ohne E-Rechnung ausreicht, und woran das
   hängt.
6. § 14c-RISIKO. Ergibt sich aus Schritt 3 oder Schritt 5, dass in der
   Schlussrechnung zu wenig abgesetzt oder ein zu hoher Steuerbetrag
   ausgewiesen ist, benenne den unrichtigen Steuerausweis nach § 14c Abs. 1
   UStG, den Weg über die Berichtigung gegenüber dem Leistungsempfänger und
   die entsprechende Anwendung des § 17 Abs. 1 UStG – ohne Betrag. Die Folgen
   für bereits erklärte Zeiträume richten sich nach dem Feld
   "Erklärungsstand"; beachte dafür die Aussteuerungsregel.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben, statt sie zu erfinden.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV, also Norm
   mit Absatz und Satz oder Erlass mit Fundstelle, jeweils mit dem Zusatz
   "für [JAHR] verifizieren", und führe sie am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" auf. Bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren" statt einer Angabe.
3. Berechne KEINE Fristen und keine Zeiträume. Liste auf, WELCHE Fristen und
   Stichtage im Raum stehen, je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und ohne Dauer. Ergänze bei jeder:
   "Fristen berechnet und erfasst ein Mensch."
4. Formuliere jede Aussage über den Inhalt eines Rechnungsdatensatzes, der
   dir nicht als Feldliste vorliegt, als Vermutung und kennzeichne sie so.
5. Der Formulierungsvorschlag enthält KEINE Zahlen. Setze für Beträge,
   Nummern und Daten Auslassungen ein, die die Kanzlei füllt.

AUSGABEFORMAT
1. (Einordnung) – Eindeutigkeit, Datenlage, fehlende Angaben.
2. (Ort und Steuerbarkeit) – übernommener Ort, Ergebnis zur Steuerbarkeit im
   Inland, Rechtsgrundlage; bei einem Ort außerhalb des Inlands der Hinweis
   auf § 14a UStG und der Abbruch der weiteren Prüfung nach diesem Schema.
3. (Prüfprotokoll je Anzahlung) – Tabelle:
   Nr. | vor Ausführung vereinnahmt (ja/nein) | Rechnung nach § 14 Abs. 1
   bis 4 UStG ausgestellt (ja/nein/unklar) | in der Endrechnung abzusetzen
   (ja/nein) | Rechtsgrundlage | offene Frage
4. (Steuersatzwechsel) – nur wenn das Feld "Steuersatzwechsel" ein "ja" sagt:
   welche Anzahlungsrechnungen betroffen sind, welche Norm den anzuwendenden
   Steuersatz bestimmt, was daraus für die Absetzung folgt – ohne Prozentsatz
   und ohne Betrag. Sonst: "Kein Steuersatzwechsel angegeben."
5. (Formatentscheidung) – in welchem Format Schlussrechnung und
   Berichtigungsdokument zu erstellen sind, mit Begründung aus § 14 Abs. 2
   Satz 2 und § 27 Abs. 38 Satz 1 UStG sowie § 31 Abs. 5 Satz 3 UStDV und
   UStAE Abschnitt 14.11 Abs. 1 Sätze 7 bis 9.
6. (Formulierungsvorschlag Absetzungsteil) – Textbaustein für den Teil der
   Schlussrechnung, in dem die vereinnahmten Teilentgelte und die auf sie
   entfallenden Steuerbeträge abgesetzt werden, ohne Zahlen.
7. (Risikoliste § 14c UStG) – Tabelle:
   Nr. | Risiko | woran es hängt | was zu prüfen ist | erledigt (leer)
8. (Offene Punkte) – darunter ausdrücklich der Verweis in UStAE Abschnitt
   14.8 Abs. 7 Satz 5 auf Rn. 47 und 48 des BMF-Schreibens vom 15.10.2024,
   deren Inhalt im Originaltext nachzulesen ist, sowie alle ausgesteuerten
   Punkte.
9. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
10. (Interne Notiz) – was die Kanzlei vor dem Versand der Schlussrechnung
    klären muss.
```

## Anwendung

1. **Vorschaltfrage durch den Berufsträger, vor dem Werkzeugeinsatz und außerhalb des Werkzeugs:** Gibt es Anhaltspunkte für eine Berichtigungspflicht nach § 153 AO, eine Selbstanzeige oder ein Steuerstrafverfahren? Wenn ja, wird dieser Prompt nicht eingesetzt; die Antwort wird in der Handakte vermerkt (Zone Rot in `DATENSCHUTZ.md`).
2. Den Ort der Leistung vor dem Lauf in der Kanzlei bestimmen und eintragen; der Prompt übernimmt die Einordnung, er ermittelt sie nicht. Für Bezüge über Betriebsstätte und Stammhaus ist Prompt 118 der richtige Ort, für Reverse-Charge und die übrigen Sonderfälle Prompt 04.
3. Anzahlungstabelle aus der Fakturierung übernehmen, nicht aus dem Gedächtnis. Entscheidend ist je Zeile die Angabe, ob über das Teilentgelt tatsächlich eine Rechnung ausgestellt wurde und ob sie die Angaben nach § 14 Abs. 1 bis 4 UStG enthielt – daran hängt die Absetzung, nicht am Zahlungseingang.
4. Bei bereits erstellter Schlussrechnung zusätzlich die Feldliste des strukturierten Teils beifügen; ohne sie bleibt jede Aussage über den Datensatz Vermutung.
5. Das Ergebnis der Formatentscheidung mit dem Fakturaprogramm abgleichen: Welcher Rechnungstyp steht dort für Schlussrechnung und für Berichtigung zur Verfügung, und wird der strukturierte Datensatz revisionssicher abgelegt?
6. Ergibt Schritt 6 ein § 14c-Risiko und ist der Zeitraum noch nicht erklärt, mit Prompt 87 weiterarbeiten. Ist der Zeitraum bereits erklärt, bleibt dieser Prompt anwendbar – der Punkt „Folgen für bereits erklärte Zeiträume" ist dann nach der Aussteuerungsregel ausgesteuert und wird ausschließlich vom Berufsträger außerhalb des KI-Werkzeugs bearbeitet; Prompt 87 wird dafür nicht eingesetzt.
7. **Abgrenzung zu den Nachbarprompts:** Prompt 85 bestimmt den Umstellungsstichtag über den Mandantenbestand hinweg, dieser Prompt prüft einen einzelnen Vorgang. Prompt 86 bestimmt die Fehlerklasse einer **eingegangenen** Rechnung, dieser Prompt betrifft die eigene **Ausgangs**rechnung. Prompt 87 behandelt § 14c UStG allgemein und die Berichtigung des Steuerausweises; hier endet die Prüfung mit der Feststellung des Risikos.

## Qualitätssicherung

- **Der Ort steht vor allem anderen.** Die Pflicht zur E-Rechnung, der Steuersatz und § 14c UStG setzen einen im Inland steuerbaren Umsatz voraus (§ 1 Abs. 1 Nr. 1 UStG). Prüfen: Steht die Ortsangabe im Ergebnis vor der Pflichtprüfung, und stammt sie aus der Kanzlei und nicht aus dem Modell? Liegt der Ort nicht im Inland, ist § 14a UStG die richtige Spur, nicht § 14 Abs. 2 Satz 2 UStG (für [JAHR] verifizieren).
- **Die Normen nicht vertauschen.** Der Abzug in der Endrechnung folgt aus § 14 Abs. 5 Satz 2 UStG. § 13 Abs. 1 Nr. 1 Buchst. a Satz 4 UStG regelt allein die Entstehung der Steuer bei Vereinnahmung; wer ihn für die Absetzung zitiert, begründet das Ergebnis falsch. Beide Fundstellen im amtlichen Volltext nachlesen (für [JAHR] verifizieren).
- **Absetzung hängt an der ausgestellten Rechnung, nicht an der Zahlung.** § 14 Abs. 5 Satz 2 UStG verlangt Rechnungen im Sinne der Absätze 1 bis 4 über die Teilentgelte. Diese Voraussetzung wird je Anzahlung geprüft und dokumentiert.
- **Formfrage der Berichtigung getrennt prüfen.** § 31 Abs. 5 Satz 3 UStDV stellt an das Berichtigungsdokument dieselben Anforderungen an Form und Inhalt wie § 14 UStG; UStAE Abschnitt 14.11 Abs. 1 Sätze 7 bis 9 zieht daraus die Folge für die E-Rechnung. Eine formlose Korrektur per E-Mail oder Papier trägt nur, wenn für den Umsatz nach § 14 Abs. 2 Satz 2 i. V. m. § 27 Abs. 38 UStG keine E-Rechnungspflicht besteht (für [JAHR] verifizieren).
- **Keine falsche Beruhigung zur Rückwirkung.** § 14 Abs. 4 Satz 4 UStG bestimmt, dass die Berichtigung einer Rechnung kein rückwirkendes Ereignis i. S. d. § 175 Abs. 1 Satz 1 Nr. 2 und § 233a Abs. 2a AO ist. Fassung, Anwendungszeitpunkt und Entstehungsgeschichte am amtlichen Text prüfen und die Vorschrift nicht mit § 14c UStG vermengen (für [JAHR] verifizieren).
- **§ 14c UStG nicht falsch datieren.** Keine Aussage, das Jahressteuergesetz 2024 habe § 14c Abs. 1 UStG geändert – geändert wurde Abs. 2 Satz 2 (für [JAHR] verifizieren).
- **Rn. 47 und 48 des BMF-Schreibens vom 15.10.2024 werden gelesen, nicht wiedergegeben.** Der Verweis in UStAE Abschnitt 14.8 Abs. 7 Satz 5 belegt nur, dass es diese Randnummern gibt. Jeder Inhalt, den ein Modell dazu ausgibt, ist ungeprüft und wird verworfen.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person prüft Absetzungsentscheidung, Formatentscheidung und Berichtigungsweg anhand der Rechnungsdatensätze nach. Schlussrechnung, Berichtigungsdokument und jede Mitteilung an den Leistungsempfänger gibt ein Berufsträger frei; die Freigabe wird dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum und keine Zeitraumangabe aus der KI-Antwort übernehmen.
- **Rechtsstand prüfen an:** § 1 Abs. 1 Nr. 1, § 3, § 3a, § 13, § 14, § 14a, § 14c, § 27 Abs. 1 und § 27 Abs. 38 UStG sowie § 31 Abs. 5 UStDV im amtlichen Volltext (gesetze-im-internet.de), UStAE Abschnitte 14.8 und 14.11, BMF-Schreiben zur obligatorischen E-Rechnung vom 15.10.2024 (BStBl I 2024, 1320) in der durch das BMF-Schreiben vom 15.10.2025 geänderten und ergänzten Fassung – das Schreiben von 2024 ist nicht aufgehoben.

## Varianten

- **Nur Formatfrage:** „Bearbeite ausschließlich Schritt 2 und Schritt 5 und erzeuge daraus eine einseitige Arbeitsanweisung für die Fakturierung."
- **Bauleistung mit Teilabnahmen:** „Prüfe zusätzlich je Teilleistung, ob sie wirtschaftlich abgrenzbar und gesondert abgenommen ist, und weise die Prüfung in einer eigenen Spalte aus."
- **Dauerhafte Vorlage:** „Leite aus dem Ergebnis eine Prüfliste für alle künftigen Schlussrechnungen dieses Mandanten ab, abhakbar mit ☐."
- **Empfängerseite:** „Formuliere aus dem Ergebnis eine Reklamation an einen Lieferanten, dessen Schlussrechnung die Teilentgelte nicht absetzt, ohne Betragsangaben."
