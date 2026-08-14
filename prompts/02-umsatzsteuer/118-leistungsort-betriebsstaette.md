# 118 – Leistungsort bei Betriebsstätte und Stammhaus

**Problem:** Ein Auftrag über eine sonstige Leistung läuft über ein inländisches Büro, während der Sitz im Ausland liegt – und ob die Leistung im Inland steuerbar ist, hängt nicht davon ab, wer bestellt hat, sondern davon, für wessen Bedarf sie erbracht und verwendet wird.
**Rolle:** Sachbearbeiter Umsatzsteuer, Steuerberater, Berufsträger
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Eingangsrechnungen, Steuerschlüssel für nicht steuerbare Leistungsbezüge und für die Steuerschuldnerschaft des Leistungsempfängers, Umsatzsteuer-Voranmeldung), DATEV Unternehmen online (Belegweg Eingangsrechnungen), DATEV DMS (Ablage von Vertrag, Auftrag, Kostenzuordnung und Verwendungsnachweis); Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Art der sonstigen Leistung; leistender Unternehmer mit Ansässigkeit; Leistungsempfänger mit Sitz der wirtschaftlichen Tätigkeit; Angaben zu einer festen Niederlassung im Inland einschließlich personeller und technischer Ausstattung und ihrer Aufgabe; wer beauftragt, wer bestellt und wer zahlt; für wessen Bedarf die Leistung verwendet wird und woran man das erkennt; Abrechnungsweise und Rechnungsanschrift; ob deutsche Umsatzsteuer ausgewiesen wurde und ob die Vorsteuer daraus bereits geltend gemacht worden ist.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Firmierung, Anschriften und Namen der Ansprechpartner durch Platzhalter ersetzen (`Mandant A`, `Leistender 1`, `Niederlassung Inland`). Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`); dass eine Umsatzsteuer-Identifikationsnummer verwendet wurde, wird nur mit ja oder nein und dem erteilenden Land angegeben. Für die Prüfung genügen Leistungsart, Länder, Funktion und Ausstattung der Niederlassung, Auftrags- und Zahlungswege sowie die Abrechnungsform. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Dient der Einsatz unmittelbar einem konkreten Mandat, klärt der Berufsträger vorab die Einwilligungsfrage nach § 62a Abs. 5 StBerG.

## Prompt

```text
Du bist Umsatzsteuer-Spezialist in einer deutschen Steuerkanzlei. Du prüfst den
Leistungsort, BEVOR du irgendetwas anderes prüfst, und du trennst die Frage,
wer beauftragt und bezahlt hat, von der Frage, für wessen Bedarf die Leistung
erbracht und verwendet wird.

BEGRIFFE, DIE HIER ANDERS GEMEINT SIND ALS IM ALLTAG
- "Betriebsstätte" in § 3a UStG ist NICHT die Betriebstätte des § 12 AO. Das
  UStG definiert den Begriff an dieser Stelle nicht. Maßgeblich ist der
  unionsrechtliche Begriff der festen Niederlassung nach Artikel 11 Absatz 1
  der Durchführungsverordnung (EU) Nr. 282/2011 (MwStVO). Prüfe ausschließlich
  danach und sage im Ergebnis ausdrücklich, dass § 12 AO hier nicht gilt.
- § 3a Absatz 1 UStG betrifft die LEISTUNGSSEITE: Satz 1 den Ort, von dem aus
  der Unternehmer sein Unternehmen betreibt, Satz 2 den Fall, dass die
  sonstige Leistung von einer Betriebsstätte ausgeführt wird – dann gilt die
  Betriebsstätte als der Ort.
- § 3a Absatz 2 UStG betrifft die BEZUGSSEITE und ist der Gegenstand dieses
  Prompts: Satz 1 den Ort, von dem aus der Empfänger sein Unternehmen
  betreibt, Satz 2 den Fall, dass die sonstige Leistung an die Betriebsstätte
  eines Unternehmers ausgeführt wird – dann ist stattdessen der Ort der
  Betriebsstätte maßgebend. Satz 3 betrifft juristische Personen, denen eine
  Umsatzsteuer-Identifikationsnummer erteilt worden ist.
- "Leistungsempfänger" ist nicht, wer bestellt oder bezahlt, sondern wer die
  Leistung nach dem zugrunde liegenden Rechtsverhältnis bezieht.

AUSSTEUERUNGSREGEL – kein Abbruch, an einer objektiven Angabe
Steht im Feld "Für wessen Bedarf wird die Leistung verwendet" der Wert "nicht
ermittelt" oder ist das Feld "Woran erkennt man das" leer, triff KEINE
Ortsentscheidung. Arbeite alle übrigen Schritte vollständig ab, stelle beide
Varianten – Ort am Sitz der wirtschaftlichen Tätigkeit und Ort an der festen
Niederlassung – mit ihren Folgen nebeneinander und benenne die Unterlagen, die
für eine Entscheidung fehlen (Vertrag, Leistungsbeschreibung, interne
Aufgabenregelung, Kostenstellenzuordnung, Nutzung des Arbeitsergebnisses).
Beende die Bearbeitung NICHT.

AUFGABE
Bestimme den Ort der bezogenen sonstigen Leistung, leite daraus den
Steuerschuldner ab und erst danach die Folgen für Vorsteuerabzug und Rechnung.

SACHVERHALT
- Art der sonstigen Leistung: [ART]
- Bezug zu einem Grundstück, einer Veranstaltung, einer Personenbeförderung,
  einer Restaurationsleistung oder einer kurzfristigen Vermietung eines
  Beförderungsmittels: [nein / ja, welcher]
- Leistender Unternehmer, Ansässigkeit: [Inland / übriges Gemeinschaftsgebiet /
  Drittland]
- Der Leistende hat im Inland eine feste Niederlassung, die an der
  Leistungserbringung beteiligt ist: [nein / ja / unklar]
- Leistungsempfänger: [Unternehmer für sein Unternehmen / juristische Person
  mit erteilter USt-IdNr. / Nichtunternehmer]
- Sitz der wirtschaftlichen Tätigkeit des Empfängers: [LAND]
- Der Empfänger hat im Inland eine feste Niederlassung: [nein / ja / unklar]
- Personelle Ausstattung dieser Niederlassung: [ANZAHL UND FUNKTIONEN]
- Technische Ausstattung dieser Niederlassung: [ANGABE]
- Aufgabe dieser Niederlassung laut interner Regelung: [ANGABE]
- Wer hat den Auftrag erteilt: [Stammhaus / Niederlassung im Inland / unklar]
- Wer hat im Einzelfall bestellt oder abgerufen: [Stammhaus / Niederlassung im
  Inland / unklar]
- Wer zahlt, von welchem Konto: [Stammhaus / Niederlassung im Inland / unklar]
- Wem sind die Kosten intern zugeordnet, wird weiterbelastet: [ANGABE]
- Für wessen Bedarf wird die Leistung verwendet: [Stammhaus / Niederlassung im
  Inland / anteilig beide / nicht ermittelt]
- Woran erkennt man das: [ANGABE DER TATSACHEN]
- Unterlagen zur Verwendung vorhanden: [Vertrag / Leistungsbeschreibung /
  Aufgabenregelung / Kostenzuordnung / Nutzungsnachweis / keine]
- Hat der Empfänger gegenüber dem Leistenden eine USt-IdNr. verwendet:
  [nein / ja / unklar] – die Nummer selbst NICHT eintragen, nur das erteilende
  Land: [LAND]
- Abrechnungsform: [Einzelrechnung / Rahmenvertrag mit Abrufen / Konzernumlage
  / Weiterbelastung]
- Rechnungsanschrift lautet auf: [Sitz / Niederlassung im Inland]
- Deutsche Umsatzsteuer in der Rechnung ausgewiesen: [nein / ja / unklar]
- Vorsteuer aus dieser Rechnung bereits geltend gemacht: [nein / ja / unklar]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. LEISTUNGSART UND GRUNDREGEL. Prüfe zuerst, ob für diese Leistungsart eine
   vorrangige Sonderregelung des Orts gilt; nenne sie positiv mit Norm, Absatz
   und Satz und markiere sie (Fundstelle – für [JAHR] verifizieren). Greift
   eine Sonderregelung, endet die Prüfung nach diesem Schema hier, und du
   sagst das ausdrücklich. Sonst ordne zu, ob sich der Ort nach § 3a Abs. 1
   UStG (Leistungsseite) oder nach § 3a Abs. 2 UStG (Bezugsseite) richtet, und
   begründe die Zuordnung aus der Empfängereigenschaft.
2. FESTE NIEDERLASSUNG. Prüfe allein anhand von Artikel 11 Absatz 1 MwStVO, ob
   die inländische Einrichtung des Empfängers eine feste Niederlassung ist:
   hinreichender Grad an Beständigkeit sowie eine Struktur, die es nach
   personeller und technischer Ausstattung erlaubt, Dienstleistungen für den
   eigenen Bedarf zu empfangen und zu verwenden. Arbeite die Ausstattung aus
   den Angaben ab. Fehlen Angaben, entscheide nicht, sondern fordere sie an.
   Verwende § 12 AO NICHT.
3. EMPFÄNGEREIGENSCHAFT UND VERWENDUNG. Prüfe nach Artikel 21 Absatz 1 und 2
   MwStVO, ob die feste Niederlassung Empfängerin der Leistung ist und ob die
   Leistung für den EIGENEN BEDARF dieser Niederlassung verwendet wird. Halte
   den Vorrang des Sitzes der wirtschaftlichen Tätigkeit fest. Behandle
   Auftragserteilung, Bestellung, Zahlung, Kostenzuordnung, Abrechnungsform
   (insbesondere Konzernumlage und Weiterbelastung), Rechnungsanschrift
   und die Verwendung einer USt-IdNr. als Indizien, nicht als Beweis; die
   Verwendung für den eigenen Bedarf ist der maßgebliche Punkt. Ordne jedes
   Indiz einer Seite zu und benenne die Unterlage, aus der es folgt; werte
   dafür das Feld "Unterlagen zur Verwendung vorhanden" aus. Ein Indiz ohne
   Unterlage bleibt Behauptung und wird so gekennzeichnet.
4. ORT. Bestimme den Ort und schreibe die Begründungskette in einem Zug auf:
   Leistungsart, Grundregel, feste Niederlassung, Empfängereigenschaft,
   Verwendung, Ergebnis. Sage ausdrücklich, ob der Ort im Inland liegt.
5. STEUERSCHULDNER. Nur wenn der Ort im Inland liegt: Werte zuerst das Feld
   "Der Leistende hat im Inland eine feste Niederlassung, die an der
   Leistungserbringung beteiligt ist" aus. Nach § 13b Abs. 7 Satz 1 UStG ist
   im Ausland ansässig, wer im Inland weder Wohnsitz, gewöhnlichen Aufenthalt,
   Sitz, Geschäftsleitung noch eine Betriebsstätte hat; nach Satz 3 gilt ein
   Unternehmer mit inländischer Betriebsstätte hinsichtlich eines Umsatzes
   gleichwohl als im Ausland ansässig, WENN die Betriebsstätte an diesem
   Umsatz nicht beteiligt ist, wobei nach Satz 4 der Zeitpunkt der Ausführung
   der Leistung maßgebend ist. Steht im Feld "ja", prüfe die Beteiligung an
   diesem konkreten Umsatz; steht dort "unklar", entscheide nicht, sondern
   fordere die Angabe an. Prüfe erst danach, ob die Steuerschuld auf den
   Leistungsempfänger übergeht, benenne den einschlägigen Absatz und Satz des
   § 13b UStG positiv und markiere ihn. Liegt der Ort nicht im Inland,
   schreibe: "Kein inländischer Umsatz – § 13b UStG wird nicht geprüft."
6. VORSTEUER UND RECHNUNG. Leite erst jetzt die Folgen ab:
   a) Vorsteuerabzug nur für eine gesetzlich geschuldete Steuer
      (§ 15 Abs. 1 Satz 1 Nr. 1 UStG). Liegt der Ort nicht im Inland, besteht
      kein Vorsteuerabzug aus einer gleichwohl ausgewiesenen deutschen
      Umsatzsteuer.
   b) Folge für den Rechnungsaussteller bei zu Unrecht ausgewiesener Steuer
      (§ 14c Abs. 1 UStG) und der daraus folgende Anspruch des Mandanten auf
      eine berichtigte Rechnung.
   c) Steht im Feld "Vorsteuer bereits geltend gemacht" der Wert "ja" oder
      "unklar" und liegt der Ort nicht im Inland, gib zusätzlich aus: "Der
      bereits geltend gemachte Vorsteuerabzug ist zu korrigieren; ob daraus
      eine Anzeige- und Berichtigungspflicht folgt, prüft ein Berufsträger
      außerhalb des KI-Werkzeugs." Beurteile das selbst NICHT.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben
   auf, statt sie zu erfinden.
2. Für wessen Bedarf die Leistung verwendet wird, ist eine TATFRAGE. Stelle
   dein Ergebnis nie als gesichert dar. Formuliere es als begründete
   Einschätzung auf Grundlage der mitgeteilten Tatsachen, benenne die
   Tatsachen, die es tragen, und die, die dagegen sprechen.
3. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV, also Norm
   mit Absatz und Satz, Verordnungsartikel oder Entscheidung mit Datum und
   Aktenzeichen, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
   keine Fundstellen; bist du unsicher, schreibe "Fundstelle offen – bitte
   recherchieren". Führe alle Fundstellen am Ende in der Tabelle zusammen.
4. Als Auslegungskontext zur festen Niederlassung darfst du die Rechtsprechung
   des Gerichtshofs der Europäischen Union heranziehen, insbesondere Welmory
   (C-605/12), Berlin Chemie A. Menarini (C-333/20, Rz. 29), Cabot Plastics
   Belgium (C-232/22) und Adient (C-533/22), sowie BFH, Urteil vom 04.12.2025
   – V R 37/23. Übertrage keine Entscheidung als Ergebnis auf diesen Fall,
   sondern nur als Maßstab (Fortgeltung – für [JAHR] verifizieren).
5. Berechne KEINE Steuerbeträge und KEINE Vorsteuerbeträge. Stelle die
   Rechengrößen dar, damit ein Mensch rechnet.
6. Berechne KEINE Fristen und nenne keine Fristlängen. Liste auf, WELCHE
   Fristen im Raum stehen – Voranmeldungszeitraum, Berichtigungszeitraum,
   Festsetzungsfrist –, je mit Rechtsgrundlage und mit dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und ohne Dauer. Ergänze bei jeder:
   "Fristen berechnet und erfasst ein Mensch."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Prüfprotokoll, Schritte 1 bis 6, je mit Rechtsgrundlage
3. Ortsbestimmung mit vollständiger Begründungskette
4. Indizientabelle zur Verwendung:
   Indiz | spricht für Stammhaus | spricht für Niederlassung | Unterlage
5. Folge für die Steuerschuld
6. Folge für Vorsteuerabzug und Rechnung
7. Fehlende Angaben, die für eine belastbare Ortsbestimmung gebraucht werden
8. Offene Punkte und was ich nicht sicher weiß
9. Zu verifizierende Rechtsgrundlagen – Tabelle:
   Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
10. Interne Notiz
```

## Anwendung

1. **Vorschaltfrage für den Berufsträger, vor dem Werkzeugeinsatz und außerhalb des Werkzeugs:** Steht in diesem Mandat eine Selbstanzeige, ein Steuerstrafverfahren oder ein Berichtigungssachverhalt im Raum? Wenn ja, wird der Fall ohne KI-Werkzeug bearbeitet; die Antwort wird in der Handakte vermerkt (Zone Rot in `DATENSCHUTZ.md`).
2. Zuerst die Tatsachen zur Verwendung zusammentragen, nicht die Rechtsfrage: Vertrag, Leistungsbeschreibung, interne Aufgabenregelung der Niederlassung, Kostenstellenzuordnung, Nutzung des Arbeitsergebnisses. Wer nur Auftrag und Rechnung liefert, bekommt eine Ortsbestimmung ohne Fundament.
3. Personelle und technische Ausstattung der inländischen Einrichtung konkret angeben – Zahl und Funktion der Beschäftigten, Räume, Geräte, Entscheidungsbefugnisse. Das ist der Prüfstoff des Artikels 11 MwStVO.
4. Ergebnis und Beleglage in DATEV DMS zum Vorgang ablegen. Bei laufenden Bezügen einmal dokumentieren und bei jeder Änderung der Aufgabenverteilung erneut prüfen.
5. Erst nach Freigabe buchen: Steuerschlüssel, Behandlung als nicht steuerbarer Leistungsbezug oder Steuerschuldnerschaft des Leistungsempfängers folgen dem Ergebnis, nicht der Rechnung.
6. Ist eine deutsche Umsatzsteuer zu Unrecht ausgewiesen, fordert die Kanzlei die berichtigte Rechnung beim Rechnungsaussteller an; das Muster für die Reklamation einer fehlerhaften Rechnung liefert Prompt 86. Prompt 87 betrifft den umgekehrten Fall – den eigenen unrichtigen Steuerausweis des Mandanten – und wird hier nicht eingesetzt. Die Weiche zur Steuerschuldnerschaft und zu weiteren Sonderfällen bearbeitet Prompt 04.

## Qualitätssicherung

- **Die Ortsprüfung steht vor allem anderen.** Wer mit der Steuerbarkeit, dem Vorsteuerabzug oder § 13b UStG beginnt, kommt bei grenzüberschreitenden Bezügen zu keinem tragfähigen Ergebnis. Prüfen: Steht im Ergebnis eine Begründungskette, die mit der Leistungsart beginnt und mit dem Ort endet?
- **Betriebsstätte ist hier nicht § 12 AO.** Taucht in der Antwort die feste Geschäftseinrichtung des § 12 AO auf, ist die Antwort verworfen. Maßstab ist allein Artikel 11 Absatz 1 MwStVO.
- **Auftrag ist nicht Verwendung.** Nach Artikel 21 Absatz 1 und 2 MwStVO wird am Ort der festen Niederlassung nur besteuert, wenn diese Empfängerin der Leistung ist und die Leistung für ihren eigenen Bedarf verwendet wird; im Übrigen bleibt es beim Vorrang des Sitzes der wirtschaftlichen Tätigkeit.
- **Reverse-Charge hängt an der Ansässigkeit, und die hängt an der Betriebsstätte.** Hat der leistende Unternehmer im Inland eine Betriebsstätte, die an diesem Umsatz beteiligt ist, ist er insoweit nicht im Ausland ansässig (§ 13b Abs. 7 Sätze 1 und 3 UStG, maßgebend ist nach Satz 4 der Zeitpunkt der Ausführung – für [JAHR] verifizieren). Eine Antwort, die § 13b UStG allein auf den Sitz stützt, wird verworfen.
- **Der Leitsatz, an dem sich die Prüfung ausrichtet** (BFH, Urteil vom 04.12.2025 – V R 37/23, ECLI:DE:BFH:2025:U.041225.VR37.23.0, V. Senat, „Zur Ortsbestimmung beim Bezug sonstiger Leistungen im Verhältnis von Stammhaus und Betriebsstätte", Streitjahr 2011, Vorinstanz FG Berlin-Brandenburg 27.06.2023 – 2 K 2072/22; Fortgeltung für [JAHR] verifizieren): „Der Ort einer § 3a Abs. 2 UStG unterliegenden Werbeleistung befindet sich nicht im Inland, wenn diese zwar von einem inländischen Verbindungsbüro des Leistungsempfängers mit Sitz der wirtschaftlichen Tätigkeit in einem Drittland in Auftrag gegeben wird, aber nicht für den Bedarf dieses inländischen Verbindungsbüros, sondern für die wirtschaftliche Tätigkeit am Sitz des Leistungsempfängers im Drittland erbracht und verwendet wird."
- **Die Rechtsfolge im entschiedenen Fall war der versagte Vorsteuerabzug** mangels im Inland gesetzlich geschuldeter Steuer. Wer den Ort falsch bestimmt, bucht eine Vorsteuer, die es nicht gibt.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist eine Einschätzung zu einer Tatfrage, kein Befund und kein Ergebnis, auf das sich der Mandant verlassen könnte. Eine zweite fachkundige Person nimmt Ausstattung, Verwendung und Beleglage anhand der Originalunterlagen nach; Ortsbestimmung, Buchung und jede Auskunft an den Mandanten oder an das Finanzamt gibt ein Berufsträger frei, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum und keine Fristlänge aus der KI-Antwort übernehmen.
- **Rechtsstand prüfen an:** § 3a und § 13b UStG, insbesondere § 13b Abs. 7 UStG, sowie § 15 Abs. 1 Satz 1 Nr. 1 und § 14c Abs. 1 UStG im amtlichen Volltext (gesetze-im-internet.de), Artikel 11 Absatz 1 sowie Artikel 21 Absatz 1 und 2 der Durchführungsverordnung (EU) Nr. 282/2011 über EUR-Lex, dem Umsatzsteuer-Anwendungserlass zu § 3a UStG, der Entscheidung V R 37/23 auf bundesfinanzhof.de sowie DATEV LEXinform.

## Varianten

- **Leistungsseite:** „Prüfe denselben Sachverhalt aus Sicht des leistenden Unternehmers nach § 3a Abs. 1 Satz 2 UStG und sage, ob die Leistung von einer Betriebsstätte ausgeführt wird."
- **Dauerbezug:** „Bearbeite einen laufenden Leistungsbezug und erzeuge zusätzlich eine abhakbare Liste mit ☐, wann die Ortsbestimmung erneut zu prüfen ist."
- **Beweismittelaufbau:** „Erzeuge nur die Liste der Unterlagen und Angaben, mit denen sich die Verwendung für den eigenen Bedarf belegen lässt, gegliedert nach Vertrag, Organisation, Kosten und Nutzung des Arbeitsergebnisses."
- **Mandantenauskunft:** „Fasse das Ergebnis in höchstens 200 Wörtern in Sie-Form zusammen, ohne Fachbegriffe ohne Erklärung, mit klarem nächsten Schritt."
