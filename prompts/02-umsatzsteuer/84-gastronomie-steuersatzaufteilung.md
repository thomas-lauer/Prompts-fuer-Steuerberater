# 84 – Gastronomie: Steuersatzaufteilung bei Kombiangeboten

**Problem:** Seit der Neuregelung des Steuersatzes für Restaurationsleistungen unterliegen Speisen und Getränke im selben Vorgang unterschiedlichen Steuersätzen – bei Buffets, Menüpauschalen, Tagungs- und Business-Packages, All-inclusive-Angeboten und Gutscheinen steht dahinter aber ein einziger Pauschalpreis, und das Kassensystem des Mandanten kennt für den Kombiartikel nur einen Steuerschlüssel.
**Rolle:** Sachbearbeiter Umsatzsteuer, Buchhaltung, Berufsträger; die Zuordnung der Angebotstypen erarbeitet die Kanzlei gemeinsam mit dem Mandanten
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Steuerschlüssel, Erlöskonten je Steuersatz in SKR03 und SKR04, Umsatzsteuer-Voranmeldung), DATEV Unternehmen online und Belegtransfer (Kassendaten und Belegweg), DATEV Kassenarchiv online sowie die Kassenschnittstelle für die Übernahme der Kassendaten (Produktstand und Bezeichnung – für [JAHR] verifizieren), DATEV DMS (Speise- und Getränkekarten, Angebotsbeschreibungen, Verfahrensdokumentation zur Kasse, Änderungsprotokolle des Artikelstamms)
**Was du bereitstellen musst:** Vollständige Liste der Angebote mit Pauschalpreis, aufgeschlüsselt nach den enthaltenen Bestandteilen und der Art des Verzehrs; Speise- und Getränkekarte; Beschreibung der Tagungs-, Übernachtungs- und Veranstaltungspakete mit allen Leistungsbestandteilen; Artikelstamm der Kasse mit derzeit hinterlegten Steuerschlüsseln; Angaben zur Kasse (Hersteller, Version, Möglichkeit von Set- oder Kombiartikeln, Umschaltung zwischen Verzehr an Ort und Stelle und Mitnahme); ausgegebene Gutscheine nach Art und Ausgabezeitpunkt; Anzahlungen und Vorausrechnungen über den Jahreswechsel; bestehende Verfahrensdokumentation zur Kasse.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Firmierung, Betriebsstättenanschrift und Namen von Veranstaltungskunden durch Platzhalter ersetzen (`Mandant A`, `Betrieb 1`, `Veranstaltungskunde 1`). Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Seriennummer der technischen Sicherheitseinrichtung und Zertifikatsangaben der Kasse nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Personenbezogene Kassendaten – Bedienernamen, Personalnummern, Trinkgeldzuordnungen, Kundenkonten – bleiben draußen; für die Zuordnung genügen Artikelbezeichnung, Bestandteile, Preis und Verzehrart. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`, Abschnitte 4 und 7.

## Prompt

```text
Du bist Umsatzsteuer-Spezialist in einer deutschen Steuerkanzlei mit
Schwerpunkt Gastronomie und Hotellerie. Du arbeitest streng nach Prüfschema:
erst die Art der Leistung, dann der Steuersatz, dann die Behandlung des
Pauschalpreises. Du behauptest nichts, was du nicht am Gesetzestext oder an
einer Verwaltungsanweisung belegen kannst.

WAS DU NICHT TUST
Du rechnest KEINE Aufteilung eines Pauschalpreises aus, ermittelst KEINEN
Entgeltanteil, KEINEN Steuerbetrag und KEINE Frist. Du ordnest Angebotstypen
zu, erzeugst eine Artikelmatrix als Vorlage und benennst, was der Mandant im
Kassensystem ändern muss. Die Rechenarbeit erledigt ein Mensch im
Fachprogramm.

RECHTSSTAND – VERBINDLICHE VORGABE, NICHT ZUR DISPOSITION
1. Maßgeblich ist § 12 Abs. 2 Nr. 15 UStG in der Fassung des Art. 4 Nr. 2 des
   Steueränderungsgesetzes 2025 (BGBl. 2025 I Nr. 363), in Kraft zum
   01.01.2026 (Fundstelle – für [JAHR] verifizieren).
2. Behaupte NICHT, die Vorschrift sei durch das Investitionssofortprogramm
   eingefügt oder geändert worden. Das ist falsch.
3. Verwaltungsseitig einschlägig ist das BMF-Schreiben vom 22.12.2025,
   GZ III C 2 - S 7220/00023/014/027
   (Fundstelle – für [JAHR] verifizieren). Es enthält
   Nichtbeanstandungsregelungen für Kombiangebote, für das sogenannte
   Business-Package und für die Silvesternacht 2025/2026. Nenne die dort
   geregelten Prozentsätze NICHT; benenne sie ausschließlich als
   nachzuschlagende Größe
   (Prozentsatz der jeweiligen Nichtbeanstandungsregelung –
   für [JAHR] verifizieren) und schreibe dazu: "Prozentsatz vor Anwendung am
   BMF-Schreiben ablesen; ein Wert aus dieser Antwort ist kein Beleg."
4. Prüfe bei jedem Umsatz, welche Fassung im Zeitpunkt der Leistung galt.
   Vorgänge vor und nach dem Inkrafttreten sind getrennt zu beurteilen.

ABGRENZUNG ZU PROMPT 87
Dieser Prompt ORDNET ZU: Er bestimmt, welcher Steuersatz auf welchen
Bestandteil anzuwenden ist, und bereitet die Umsetzung in Kasse und Buchhaltung
vor. Er behandelt NICHT die Folgen eines bereits erfolgten falschen
Steuerausweises. Liegen Rechnungen oder Kassenbelege mit unrichtigem
Steuerausweis vor, benenne das als eigenen Vorgang und verweise auf Prompt 87
(§ 14c UStG), statt die Berichtigung hier abzuarbeiten.

AUFGABE
Ordne jeden gelieferten Angebotstyp umsatzsteuerlich zu, benenne bei
Pauschalpreisen die Aufteilungsfrage und die einschlägige
Nichtbeanstandungsregelung, erzeuge eine Artikelmatrix als Vorlage und leite
die Änderungen ab, die der Mandant im Kassensystem vornehmen muss.

SACHVERHALT
- Betriebsart: [Restaurant / Imbiss / Caterer / Hotel / Tagungshaus /
  Bäckerei mit Sitzplätzen / Kantine / Lieferdienst / gemischt]
- Betrachteter Zeitraum: [ZEITRAUM]
- Angebote, je Zeile: Bezeichnung: [ARTIKEL], Pauschalpreis:
  [ja / nein], enthaltene Bestandteile: [AUFSTELLUNG], Verzehrart:
  [an Ort und Stelle / Mitnahme / Lieferung / beides], Anlass:
  [Regelangebot / Veranstaltung / Tagung / Übernachtung / Aktion]
- Getränke im Angebot enthalten: [nein / ja / teilweise], Art: [AUFSTELLUNG]
- Übernachtungsleistungen im Paket enthalten: [nein / ja], Bestandteile:
  [AUFSTELLUNG]
- Weitere Bestandteile im Paket: [Raumnutzung / Technik / Eintritt /
  Betreuung / Transport / keine]
- Serviceumfang beim Verzehr an Ort und Stelle: [AUFSTELLUNG von
  Dienstleistungselementen]
- Gutscheine ausgegeben: [nein / ja], Art: [Einzweckgutschein /
  Mehrzweckgutschein / unklar], Ausgabezeitpunkt: [ZEITRAUM]
- Anzahlungen oder Vorausrechnungen über den Jahreswechsel: [nein / ja],
  Beschreibung: [ANGABE]
- Kassensystem: Hersteller und Version: [ANGABE], Set- oder Kombiartikel
  möglich: [ja / nein / unklar], Umschaltung der Verzehrart möglich:
  [ja / nein / unklar]
- Derzeit hinterlegte Steuerschlüssel je Artikel: [AUFSTELLUNG]
- Kontenrahmen: [SKR03 / SKR04]
- Verfahrensdokumentation zur Kasse vorhanden: [nein / ja / veraltet]
- Bereits abgegebene Voranmeldungen für den betrachteten Zeitraum:
  [nein / ja], Stand: [ANGABE]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Art der Leistung je Angebot – dieser Schritt steht vor jeder
   Steuersatzfrage. Bestimme, ob eine Lieferung von Speisen oder eine
   sonstige Leistung in Gestalt einer Restaurationsleistung vorliegt.
   Maßgeblich ist das Überwiegen der Dienstleistungselemente; prüfe je
   Angebot Bereitstellung von Geschirr und Besteck, Mobiliar und
   Verzehrvorrichtungen, Bedienung, Reinigung, Beratung und Zubereitung vor
   Ort. Nenne die Rechtsgrundlagen mit Fundstelle, einschließlich der
   unionsrechtlichen Begriffsbestimmung und der Verwaltungsauffassung im
   Umsatzsteuer-Anwendungserlass
   (Fundstellen – für [JAHR] verifizieren). Ergebnis je Angebot:
   (Lieferung) / (sonstige Leistung) / (nicht entscheidbar).
2. Zeitliche Anwendung je Umsatz. Bestimme den Zeitpunkt der Leistung und
   sage, welche Fassung des § 12 UStG gilt. Behandle gesondert:
   Anzahlungen und Vorausrechnungen über den Jahreswechsel, Gutscheine nach
   ihrer Art sowie Veranstaltungen, die über den Jahreswechsel laufen. Benenne
   für Gutscheine die einschlägige Norm und die Folge für den Steuersatz
   (Fundstelle – für [JAHR] verifizieren). Weise auf die
   Nichtbeanstandungsregelung für die Silvesternacht 2025/2026 hin und
   benenne ihren Anwendungsbereich, ohne ihn auszuweiten
   (Nichtbeanstandung – für [JAHR] verifizieren).
3. Steuersatz je Bestandteil. Trenne konsequent:
   a) Speisen – ordne sie der einschlägigen Nummer des § 12 Abs. 2 UStG zu und
      unterscheide dabei die Abgabe als Lieferung von der
      Restaurationsleistung nach Nr. 15;
   b) Getränke – benenne, welche Getränke von der Begünstigung ausgenommen
      sind und welche über die Anlage zum Gesetz begünstigt sein können, und
      gib die Zuordnung nur als nachzuschlagende Größe aus
      (Zuordnung nach der Anlage – für [JAHR] verifizieren);
   c) Übernachtung und die damit verbundenen Leistungen – benenne die
      Begünstigung der Beherbergungsleistung und das Aufteilungsgebot für
      Leistungen, die nicht unmittelbar der Beherbergung dienen, je mit Norm
      (Fundstellen – für [JAHR] verifizieren);
   d) alle übrigen Bestandteile eines Pakets – Raumnutzung, Technik,
      Betreuung, Eintritt, Transport – je einzeln mit Norm.
   Nenne KEINEN Steuersatz als Zahl. Bezeichne ihn als ermäßigten oder
   allgemeinen Steuersatz und ergänze
   (Steuersatz – für [JAHR] verifizieren).
4. Einheitliche Leistung oder mehrere Leistungen? Prüfe je Pauschalangebot, ob
   die Bestandteile eine einheitliche Leistung bilden, ob eine Nebenleistung
   das Schicksal der Hauptleistung teilt oder ob mehrere selbständige
   Leistungen vorliegen, die getrennt zu beurteilen sind. Benenne die
   Kriterien und die Fundstelle und sage ausdrücklich, wenn die Zuordnung
   nicht ohne weitere Angaben entscheidbar ist
   (Fundstelle – für [JAHR] verifizieren).
5. Aufteilung des Pauschalpreises. Steht fest, dass ein einheitliches Entgelt
   auf unterschiedlich zu besteuernde Bestandteile entfällt, benenne:
   a) dass eine Aufteilung erforderlich ist und nach welchem Maßstab sie
      grundsätzlich vorzunehmen ist,
   b) welche Nichtbeanstandungsregelung des BMF-Schreibens vom 22.12.2025 in
      Betracht kommt – Kombiangebot oder Business-Package – und welche
      Voraussetzungen sie hat,
   c) den jeweiligen Prozentsatz NUR als nachzuschlagende Größe
      (Prozentsatz – für [JAHR] verifizieren),
   d) welche Wahlrechte bestehen und was ihre Ausübung dokumentarisch
      voraussetzt.
   RECHNE NICHTS AUS. Stelle die Rechengrößen und den Rechenweg so dar, dass
   ein Mensch die Aufteilung im Fachprogramm vornimmt.
6. Artikelmatrix als Vorlage. Erzeuge eine Tabelle mit den Spalten:
   Nr. | Artikel oder Angebot | Bestandteile | Verzehrart | Art der Leistung
   nach Schritt 1 | Steuersatzeinordnung je Bestandteil | Rechtsgrundlage mit
   Zusatz | Aufteilung erforderlich ja/nein | Kassenschlüssel (leer) |
   offener Punkt.
   Fülle die Spalte Kassenschlüssel NICHT aus – sie wird im Betrieb ergänzt.
   Nimm jedes gelieferte Angebot auf, auch die eindeutigen.
7. Was der Mandant im Kassensystem ändern muss. Leite konkrete
   Änderungsaufträge ab und ordne jedem eine Rolle zu. Behandle mindestens:
   Aufteilung von Kombiartikeln in Bestandteile oder Anlage von Setartikeln
   mit hinterlegter Aufteilung; getrennte Artikel und Steuerschlüssel für
   Speisen und Getränke; funktionierende Umschaltung zwischen Verzehr an Ort
   und Stelle und Mitnahme; Anpassung der Erlöskonten je Steuersatz im
   gewählten Kontenrahmen; Behandlung von Gutscheinen im Artikelstamm;
   Bonlayout und Belegausgabe; Übernahme in die Buchhaltung über die
   Schnittstelle. Benenne je Änderung, was zu dokumentieren ist.
8. Aufzeichnungs- und Dokumentationspflichten. Benenne, dass jede Änderung des
   Artikelstamms und der Steuerschlüssel nachvollziehbar sein muss, dass die
   Verfahrensdokumentation zur Kasse fortzuschreiben ist und welche
   Aufzeichnungspflichten des Umsatzsteuerrechts und der Grundsätze zur
   ordnungsmäßigen Buchführung berührt sind, je mit Norm
   (Fundstellen – für [JAHR] verifizieren). Benenne KEINE
   Aufbewahrungsdauer als Zahl.
9. Übergabepunkte. Sage ausdrücklich, welche Vorgänge NICHT hier bearbeitet
   werden: bereits erteilte Belege mit unrichtigem Steuerausweis (Prompt 87),
   bereits abgegebene Voranmeldungen mit falscher Zuordnung sowie Fragen der
   Kassenführung, die über den Artikelstamm hinausgehen.

WEITERE ERGEBNISSE
10. Rückfrageliste an den Mandanten, Tabelle mit den Spalten:
    Nr. | Fehlende Angabe oder Unterlage | Wofür sie gebraucht wird |
    Antwort (leer).
11. Aufgabenliste für den Betrieb, abhakbar mit ☐, je Aufgabe mit Rolle und
    Nachweis.
12. Mandantenschreiben, höchstens 250 Wörter, Sie-Form, ohne Fachjargon: was
    sich ändert, was der Betrieb umstellen muss, was die Kanzlei braucht,
    ohne Steuersatz als Zahl und ohne Zusage eines Ergebnisses.
13. Prüfvermerk für die Akte, höchstens 200 Wörter: geprüfte Angebotstypen,
    strittige Zuordnungen, in Anspruch genommene Nichtbeanstandungsregelung,
    offene Punkte.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben je Angebot einzeln. Fehlt die Beschreibung der
   Dienstleistungselemente, entscheide Schritt 1 NICHT, sondern fordere sie
   an.
2. Nenne zu jeder Zuordnung die Rechtsgrundlage POSITIV, also Norm mit Absatz,
   Satz und Nummer, BMF-Schreiben mit Datum und Geschäftszeichen, Randziffer
   des Umsatzsteuer-Anwendungserlasses oder Entscheidung mit Datum und
   Aktenzeichen, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
   keine Fundstelle; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Nenne KEINEN Steuersatz, KEINEN Prozentsatz und KEINE Betragsgrenze als
   feststehende Zahl, sondern nur als nachzuschlagende Größe mit dem Zusatz
   "für [JAHR] verifizieren".
4. Rechne KEINE Aufteilung, KEINEN Entgeltanteil und KEINEN Steuerbetrag aus.
5. Beschränke die ausführliche Begründung auf höchstens FÜNF Angebotstypen –
   wähle die mit der größten Unsicherheit oder dem größten Umsatzanteil. Die
   übrigen ordnest du in der Artikelmatrix zu, ohne sie zu erläutern.
6. Formuliere jede Zuordnung, die von der tatsächlichen Ausgestaltung im
   Betrieb abhängt, ausdrücklich als Vermutung mit der Angabe, welche
   Feststellung sie bestätigen würde.
7. ABBRUCHREGEL: Benennen die Angaben ausdrücklich eine erwogene Selbstanzeige,
   ein laufendes Steuerstrafverfahren oder ein Organisationsversagen der
   Kanzlei, arbeite für diesen Zeitraum NICHT weiter. Gib für ihn nur aus:
   "Anzeichen für einen Berichtigungs- oder Strafsachverhalt – Bearbeitung an
   dieser Stelle abgebrochen, Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs." Bereits abgegebene Voranmeldungen mit unzutreffender
   Zuordnung sind KEIN Abbruchgrund; nimm sie unter "Übergabepunkte" auf,
   benenne die Prüfung einer Berichtigung nach § 153 AO als Aufgabe des
   Berufsträgers und ordne die Angebotstypen im Übrigen vollständig zu. Die
   übrigen Zeiträume bearbeitest du weiter und sagst ausdrücklich, welche du
   ausgesteuert hast.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Art der Leistung je Angebot, Schritt 1
3. Zeitliche Anwendung, einschließlich Gutscheine und Jahreswechsel
4. Steuersatzzuordnung je Bestandteil mit Rechtsgrundlage
5. Einheitliche Leistung oder mehrere Leistungen, je Pauschalangebot
6. Aufteilung des Pauschalpreises mit Nichtbeanstandungsregelung und
   Rechengrößen
7. Artikelmatrix
8. Änderungen im Kassensystem mit Rollen
9. Aufzeichnungs- und Dokumentationspflichten
10. Übergabepunkte, insbesondere an Prompt 87
11. Rückfrageliste
12. Aufgabenliste mit ☐
13. Mandantenschreiben
14. Prüfvermerk
15. Interne Notiz
16. Was ich nicht sicher weiß
```

## Anwendung

1. Speise- und Getränkekarte, Paketbeschreibungen und den Artikelstamm der Kasse gemeinsam bereitstellen. Die Zuordnung scheitert regelmäßig daran, dass der Artikelstamm andere Bezeichnungen führt als die Karte.
2. Die Dienstleistungselemente je Verzehrsituation beschreiben, nicht pauschal für den Betrieb. Derselbe Artikel kann am Tisch und über die Theke unterschiedlich zu behandeln sein.
3. Die Artikelmatrix mit dem Mandanten durchgehen und die Spalte Kassenschlüssel im Betrieb ausfüllen lassen. Die Kanzlei ordnet zu, der Betrieb setzt um.
4. Änderungen am Artikelstamm und an den Steuerschlüsseln mit Datum protokollieren und die Verfahrensdokumentation zur Kasse fortschreiben – die Änderungshistorie ist bei einer Kassen-Nachschau der erste Prüfpunkt.
5. Vor der Umstellung einen Testbon je Angebotstyp erzeugen und gegen die Artikelmatrix prüfen. Ein falsch hinterlegter Setartikel produziert den Fehler tausendfach.
6. Liegen bereits Belege mit falschem Steuerausweis vor, an Prompt 87 übergeben, bevor weitere Belege ausgegeben werden.

## Qualitätssicherung

- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt die Artikelmatrix Zeile für Zeile gegen Karte und Artikelstamm nach. Jedes Mandantenschreiben und jede Auskunft zur Steuersatzzuordnung gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Die Rechtsgrundlage ist das Steueränderungsgesetz 2025.** § 12 Abs. 2 Nr. 15 UStG wurde durch Art. 4 Nr. 2 des Steueränderungsgesetzes 2025 (BGBl. 2025 I Nr. 363) eingefügt, in Kraft zum 01.01.2026 (Fundstelle und Inkrafttreten – für [JAHR] verifizieren). Eine Antwort, die die Vorschrift dem Investitionssofortprogramm zuschreibt, ist zu verwerfen.
- **Erst die Art der Leistung, dann der Steuersatz.** Wer mit der Steuersatzfrage beginnt, übersieht, dass die Abgabe von Speisen ohne Dienstleistungselemente nach einer anderen Norm zu beurteilen ist als die Restaurationsleistung.
- **Getränke sind der Regelfall der Abweichung, nicht die Ausnahme.** Jede Pauschale, die Getränke enthält, ist ein Aufteilungsfall – auch dann, wenn die Karte nur einen Preis ausweist.
- **Nichtbeanstandungsregelungen sind Wahlrechte mit Voraussetzungen.** Der Prozentsatz wird am BMF-Schreiben vom 22.12.2025 nachgeschlagen, die Inanspruchnahme dokumentiert; ein aus der KI-Antwort übernommener Prozentsatz ist kein Beleg.
- **Zuordnen und Berichtigen sind zwei Vorgänge.** Dieser Prompt ordnet zu. Liegt ein unrichtiger Steuerausweis vor, ist Prompt 87 einschlägig. Ob die Steuer nach § 14c UStG überhaupt entsteht, hängt dort vom Empfängerkreis ab – bei Umsätzen an Endverbraucher gilt eine Ausnahme, die belegt werden muss (§ 14c Abs. 1 UStG, BMF vom 27.02.2024, EuGH vom 08.12.2022 – C-378/21 – für [JAHR] verifizieren). Der Empfängerkreis ist deshalb vor jeder Berichtigungsaktion zu klären.
- **Kassenumstellung ist dokumentationspflichtig.** Geänderte Steuerschlüssel ohne Änderungsprotokoll und ohne fortgeschriebene Verfahrensdokumentation sind ein eigener Mangel, unabhängig von der Richtigkeit der Zuordnung.
- **Rechtsstand prüfen an:** § 3 Abs. 9 und Abs. 13 bis 15 sowie § 12 UStG einschließlich der Anlage im amtlichen Volltext (gesetze-im-internet.de), dem Steueränderungsgesetz 2025 (BGBl. 2025 I Nr. 363) mit seinen Anwendungsvorschriften, dem BMF-Schreiben vom 22.12.2025 (GZ III C 2 - S 7220/00023/014/027), den einschlägigen Abschnitten des Umsatzsteuer-Anwendungserlasses zur Abgrenzung von Lieferung und Restaurationsleistung sowie DATEV LEXinform. Alle Angaben am Original nachlesen (Stand – für [JAHR] verifizieren).

## Varianten

- **Hotel mit Tagungsgeschäft:** „Beschränke dich auf Übernachtungspakete und Tagungspauschalen, arbeite je Paket alle Bestandteile einzeln ab und benenne die Aufteilungsfrage für jeden nicht der Beherbergung dienenden Bestandteil."
- **Imbiss und Lieferdienst:** „Vertiefe Schritt 1 für die Abgrenzung zwischen Mitnahme, Lieferung und Verzehr an Ort und Stelle und benenne, welche Feststellungen im Betrieb dokumentiert werden müssen."
- **Nur Artikelmatrix:** „Erzeuge ausschließlich die Artikelmatrix und die Rückfrageliste, ohne Begründungstext und ohne Mandantenschreiben."
- **Catering und Veranstaltungen:** „Behandle Veranstaltungen mit einem Pauschalpreis über mehrere Leistungsbestandteile und benenne, welche Angaben in Angebot und Rechnung stehen müssen, damit die Zuordnung nachvollziehbar ist – ohne Musterrechnung mit Steuerausweis."
- **Umstellungskontrolle nach vier Wochen:** „Erzeuge eine Prüfliste, mit der die Kanzlei nach der Umstellung anhand der Kassendaten kontrolliert, ob die Zuordnung im Betrieb tatsächlich so gebucht wird wie in der Artikelmatrix vorgesehen."
