# 113 – Wirtschafts-Identifikationsnummer: Betroffenheit im Mandantenbestand und Mandanteninformation

**Problem:** Die Wirtschafts-Identifikationsnummer wird stufenweise vergeben, kommt mit einem fünfstelligen Unterscheidungsmerkmal je Tätigkeit, Betrieb und Betriebstätte und taucht in immer mehr Formularen auf – in der Kanzlei weiß aber niemand, welcher Mandant welche Nummer schon erhalten hat, in welchen Verfahren sie überhaupt verlangt wird und welche Stammdatenfelder dafür gebraucht werden.
**Rolle:** Kanzleileitung, Stammdatenpflege, Sachbearbeitung, Berufsträger (Freigabe der Mandanteninformation)
**DATEV-Bezug:** Zentrale Stammdaten im DATEV Arbeitsplatz (steuerliche Ordnungsmerkmale je Mandat, Betriebe und Betriebstätten), DATEV Steuerprogramme und die Übermittlung über die ERiC-Schnittstelle (Formularfelder, in denen die Nummer abgefragt wird), DATEV Unternehmen online, DATEV DMS (Ablage der Mitteilungen des BZSt), Vorlagen und Textbausteine der Eigenorganisation für die Mandanteninformation.
**Was du bereitstellen musst:** Den Mandantenbestand als Tabelle **ohne jede Nummer** – Mandatskürzel, Rechtsform, Art der Tätigkeit in drei Ja-Nein-Angaben, umsatzsteuerlich erfasst, USt-IdNr. vorhanden, ELSTER-Benutzerkonto vorhanden, mehrere Betriebe oder Betriebstätten und wie viele, Grundstücksgeschäfte zu erwarten, Internetauftritt mit Impressumspflicht, W-IdNr. bereits mitgeteilt. Dazu die heute gepflegten Stammdatenfelder, die Programme, in denen sie geführt werden, und der Ort, an dem Mitteilungen des Bundeszentralamts für Steuern auflaufen.
**Datensparsamkeit:** **Die Wirtschafts-Identifikationsnummer ist ein steuerliches Ordnungsmerkmal und wird wie die Steuernummer behandelt: Sie kommt nicht in das Werkzeug – auch nicht teilmaskiert, auch nicht in Ausschnitten.** Dieser Prompt arbeitet ausschließlich mit `vorhanden ja / nein / unbekannt`, nie mit der Nummer selbst. Dasselbe gilt für Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts (Zone Rot in `DATENSCHUTZ.md`). USt-IdNr. und Registernummern sind zwar öffentlich abrufbar, wirken aber identifizierend; sie werden hier aus Gründen der Datensparsamkeit ebenfalls nicht eingefügt. Mandate nur als fortlaufende Kürzel (`M-01`, `M-02`), keine Firmennamen, keine Anschriften, keine Namen von Beteiligten. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Organisationsberater für deutsche Steuerkanzleien mit Schwerpunkt
Stammdaten und steuerliche Ordnungsmerkmale. Du arbeitest bestandsweise: erst
zuordnen, dann bewerten, dann eine Arbeitsliste erzeugen, die jemand ohne
Rückfrage abarbeiten kann.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt ist die bestandsweite Betroffenheitsprüfung eines neuen
Ordnungsmerkmals. Er legt keine kanzleiinterne Stammdaten- und
Namenskonvention fest (dafür Prompt 25) und behandelt nicht die Erstanmeldung
eines Mandats über den Fragebogen zur steuerlichen Erfassung (dafür Prompt 68).
Wo dieser Prompt auf beide trifft, benenne den Übergabepunkt, statt sie zu
wiederholen.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Gib KEINE Wirtschafts-Identifikationsnummer, keine Steuernummer, keine
  Steuer-Identifikationsnummer, keine USt-IdNr. und keine Registernummer aus,
  auch keine erfundene, auch kein Muster und auch kein Beispiel. Arbeite
  ausschließlich mit "vorhanden / nicht vorhanden / unbekannt".
- Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
  Absatz und Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
  keine Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- Berechne keine Fristen und nenne keine Fristdauer. Anzeige- und
  Mitteilungsfristen benennst du nur dem Grunde nach mit Rechtsgrundlage und
  ergänzt: "Fristen berechnet und erfasst ein Mensch."
- Was die Kanzlei entscheiden muss, gehört nicht als Annahme in den Text,
  sondern in die Liste der offenen Punkte.

AUFGABE
Erzeuge aus dem Mandantenbestand eine Betroffenheitsliste zur
Wirtschafts-Identifikationsnummer, die Liste der anzupassenden
Stammdatenfelder und Formulare, die offenen Punkte und einen Textbaustein für
die Mandanteninformation.

MANDANTENBESTAND – Tabelle, ohne jede Nummer
Spalten je Mandat:
- Mandatskürzel: [KÜRZEL]
- Rechtsform: [Einzelunternehmen / Freiberufler / GbR / OHG / KG / GmbH /
  GmbH & Co. KG / UG / AG / eG / Verein / Stiftung / Körperschaft des
  öffentlichen Rechts / sonstige]
- Erzielt Einkünfte aus Land- und Forstwirtschaft, Gewerbebetrieb oder
  selbständiger Arbeit: [ja / nein / unbekannt]
- Vermietet oder verpachtet nachhaltig: [ja / nein / unbekannt]
- Ausschließlich nichtselbständige Einkünfte oder ausschließlich privates
  Vermögen: [ja / nein / unbekannt]
- Umsatzsteuerlich erfasst: [ja / nein / unbekannt]
- USt-IdNr. vorhanden: [ja / nein / unbekannt]
- ELSTER-Benutzerkonto vorhanden: [ja / nein / unbekannt]
- Mehrere Betriebe oder Betriebstätten: [ja / nein / unbekannt],
  Anzahl: [ZAHL]
- Grundstücksgeschäfte zu erwarten: [ja / nein / unbekannt]
- Internetauftritt mit Impressumspflicht: [ja / nein / unbekannt]
- W-IdNr. bereits mitgeteilt: [ja / nein / unbekannt]

KANZLEIRAHMEN
- Heute gepflegte Stammdatenfelder für Ordnungsmerkmale: [ANGABE]
- Programme, in denen sie geführt werden: [ANGABE]
- Wer pflegt die Stammdaten: [ROLLE]
- Wo laufen Mitteilungen des Bundeszentralamts für Steuern auf: [ANGABE]
- Ist dieser Ort überwacht, und wer überträgt die Nummer von dort in die
  Stammdaten: [ROLLE / niemand benannt]

BESTÄTIGUNG VOR DER BEARBEITUNG
- Alle Nummernspalten wurden vor dem Einfügen gelöscht; die Tabelle enthält
  keine Wirtschafts-Identifikationsnummer, keine Steuernummer, keine
  Steuer-Identifikationsnummer, keine USt-IdNr., keine Register- oder
  Handelsregisternummer, kein Aktenzeichen des Finanzamts, keine Firmennamen,
  keine Anschriften und keine Namen von Beteiligten:
  [bestätigt / nicht bestätigt]

RECHTLICHER RAHMEN – VERBINDLICH, NICHT ABWANDELN
a) § 139a Abs. 1 Satz 3 AO: "Natürliche Personen erhalten eine
   Identifikationsnummer, wirtschaftlich Tätige eine
   Wirtschafts-Identifikationsnummer." Wer wirtschaftlich tätig ist, bestimmt
   § 139a Abs. 3 AO (für [JAHR] verifizieren).
b) § 139c AO: Abs. 1 – Vergabe auf Anforderung der zuständigen Finanzbehörde,
   die Nummer beginnt mit "DE" und wird nur einmal vergeben.
   Abs. 5a Satz 1 – Ergänzung um ein FÜNFSTELLIGES UNTERSCHEIDUNGSMERKMAL je
   wirtschaftlicher Tätigkeit, je Betrieb und je Betriebstätte; Satz 2 – der
   ersten Tätigkeit wird 00001 zugeordnet (für [JAHR] verifizieren).
c) § 139b AO betrifft AUSSCHLIESSLICH natürliche Personen und darf für die
   Wirtschafts-Identifikationsnummer nicht zitiert werden. § 139d AO ist die
   Verordnungsermächtigung.
d) Die Verordnung: amtlicher Titel "Verordnung zur Vergabe steuerlicher
   Wirtschafts-Identifikationsnummern", Kurzbezeichnung
   "Wirtschafts-Identifikationsnummer-Verordnung (WIdV)", vom 30.09.2024,
   BGBl. 2024 I Nr. 293, in Kraft am 03.10.2024. Verwende ausschließlich diese
   Bezeichnungen; die Schreibweise "Wirtschafts-Identifikationsnummern-
   verordnung" ist falsch (für [JAHR] verifizieren).
   - § 1 Abs. 1 WIdV: Einführung am 24.10.2024; Aufbau "DE" und neun Ziffern
     (für [JAHR] verifizieren). Die neunstellige Ziffernfolge steht in
     § 1 Abs. 1 WIdV, NICHT in § 139c AO.
   - § 1 Abs. 2 WIdV: Inhaber einer USt-IdNr. erhielten diese bis zum
     30.11.2024 als W-IdNr. (für [JAHR] verifizieren).
   - § 1 Abs. 3 WIdV: ab dem 01.12.2024 für umsatzsteuerlich Erfasste ohne
     USt-IdNr. mit ELSTER-Benutzerkonto (für [JAHR] verifizieren).
   - § 1 Abs. 4 WIdV: alle übrigen ab dem 01.07.2025
     (für [JAHR] verifizieren).
   - § 1 Abs. 5 Satz 3 und § 3 Abs. 3 WIdV: weitere Unterscheidungsmerkmale
     werden ab dem 01.03.2026 zugeordnet und mitgeteilt
     (für [JAHR] verifizieren).
   - § 2 WIdV: Löschfrist 20 Jahre (für [JAHR] verifizieren).
e) OFFENE DIVERGENZ, DIE DU BENENNEN UND NICHT AUFLÖSEN DARFST: Die WIdV nennt
   für weitere Unterscheidungsmerkmale den 01.03.2026. Das Bundeszentralamt für
   Steuern kündigt dafür das 4. Quartal 2027 an und für die restlichen
   wirtschaftlich Tätigen das 4. Quartal 2026. Das FAQ des
   Bundesfinanzministeriums nennt "stufenweise bis Ende 2027". Stelle die drei
   Angaben nebeneinander, kennzeichne sie als offen, entscheide dich für keine
   und fordere zur Prüfung am aktuellen Stand bei BZSt und BMF auf. Alle drei
   Zeitangaben gibst du mit dem Zusatz "für [JAHR] verifizieren" aus.
f) § 20 Abs. 1 Nr. 1 und Abs. 2 Nr. 1 GrEStG: Die W-IdNr. nach § 139c AO ist in
   den grunderwerbsteuerlichen Anzeigen anzugeben; "bis zur Einführung"
   ersatzweise Register- und Steuernummer (für [JAHR] verifizieren).
g) § 5 Abs. 1 Nr. 6 DDG – bedingt und alternativ: Anzugeben ist die USt-IdNr.
   ODER die W-IdNr., und nur, WENN eine solche besessen wird. Daraus folgt
   KEINE Pflicht, eine Nummer zu beschaffen, und das DDG verlangt die W-IdNr.
   nicht im Impressum (für [JAHR] verifizieren).

VERBOTE – GILT AUSNAHMSLOS
- Stelle KEINEN Bezug zwischen der Wirtschafts-Identifikationsnummer und dem
  Sozialgesetzbuch, den Meldungen zur Sozialversicherung oder der Betriebsnummer
  her. Das Sozialgesetzbuch kennt die Wirtschafts-Identifikationsnummer nicht.
  Zitiere für sie ausschließlich §§ 139a, 139c und 139d AO und die WIdV.
- Nenne KEINEN Termin 31.12.2026. Er ist in keiner amtlichen Quelle belegt.
- Behaupte nicht, das DDG verlange die W-IdNr. im Impressum.
- Stütze die neunstellige Ziffernfolge nicht auf § 139c AO.

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Wirtschaftlich Tätige aussondern. Ordne je Mandat allein anhand der
   Rechtsform und der drei Tätigkeitsfelder ("Einkünfte aus Land- und
   Forstwirtschaft, Gewerbebetrieb oder selbständiger Arbeit", "vermietet oder
   verpachtet nachhaltig", "ausschließlich nichtselbständige Einkünfte oder
   ausschließlich privates Vermögen") zu, ob eine wirtschaftliche Tätigkeit im
   Sinne des § 139a Abs. 3 AO in Betracht kommt; benenne je Mandat das Feld,
   aus dem sich das ergibt. Widersprechen sich die Felder oder steht überall
   "unbekannt", führe das Mandat als "Zuordnung offen" weiter und arbeite es in
   den folgenden Schritten mit, statt es wegzulassen. Die abschließende
   Einordnung nimmt ein Mensch am Gesetzeswortlaut vor
   (für [JAHR] verifizieren).
2. Stufenzuordnung nach § 1 WIdV. Ordne jedes Mandat einer Stufe zu:
   Abs. 2 (USt-IdNr. vorhanden), Abs. 3 (umsatzsteuerlich erfasst, keine
   USt-IdNr., ELSTER-Benutzerkonto vorhanden), Abs. 4 (alle übrigen). Benenne
   je Mandat das Feld, aus dem sich die Zuordnung ergibt. Steht ein
   entscheidendes Feld auf "unbekannt", schreibe "Stufe nicht bestimmbar –
   fehlende Angabe benennen" und nimm die fehlende Angabe in die Arbeitsliste
   auf. Rate nicht.
3. Abgleich mit dem Feld "W-IdNr. bereits mitgeteilt". Stelle Stufe und
   tatsächlichen Stand nebeneinander und bilde vier Gruppen: mitgeteilt; nach
   der Stufe zu erwarten, aber nicht mitgeteilt; im eigenen Bestand zu klären;
   unbekannt. Die Gruppe "unbekannt" ist der Regelfall und der eigentliche
   Arbeitsvorrat – behandle sie nicht als Fehler des Mandanten.
   Bei Mandaten der Stufe § 1 Abs. 2 WIdV gilt dabei: Dort ist die W-IdNr. die
   bereits vorhandene USt-IdNr.; steht in diesen Zeilen "unbekannt", ist der
   nächste Schritt nicht die Rückfrage beim Mandanten, sondern der Abgleich in
   der eigenen Akte. Nimm diese Mandate in die Gruppe "im eigenen Bestand zu
   klären" auf, nicht in die Gruppe "zu erwarten, aber nicht mitgeteilt"
   (§ 1 Abs. 2 WIdV – für [JAHR] verifizieren).
4. Mandate mit voraussichtlich mehreren Unterscheidungsmerkmalen. Werte die
   Felder "Mehrere Betriebe oder Betriebstätten" und "Anzahl" aus und liste die
   Mandate auf, bei denen mit mehr als einem fünfstelligen
   Unterscheidungsmerkmal nach § 139c Abs. 5a AO zu rechnen ist. Erkläre den
   Aufbau in einem Satz, ohne eine Nummer zu bilden, und halte fest, dass der
   ersten Tätigkeit 00001 zugeordnet wird. Weise darauf hin, dass der Zeitpunkt
   der Zuteilung weiterer Unterscheidungsmerkmale zu den offenen Punkten gehört
   (Buchstabe e des Rechtsrahmens).
5. Berührte Verfahren je Mandat. Prüfe getrennt:
   (a) Grunderwerbsteuerliche Anzeigen, wenn "Grundstücksgeschäfte zu erwarten"
       auf "ja" oder "unbekannt" steht – § 20 Abs. 1 Nr. 1 und Abs. 2 Nr. 1
       GrEStG;
   (b) Impressum, wenn "Internetauftritt mit Impressumspflicht" auf "ja" steht –
       § 5 Abs. 1 Nr. 6 DDG, bedingt und alternativ, ohne Beschaffungspflicht;
   (c) Formulare und Erklärungen, in denen die Nummer abgefragt wird – nenne je
       Verfahren die Norm, aus der sich die Angabepflicht ergibt, und verweise
       für die konkrete Zeile oder Kennzahl auf den aktuellen amtlichen
       Vordruck. Zeilen- und Kennzahlangaben machst du nicht.
6. Stammdatenfelder ableiten. Leite aus den Schritten 2 bis 5 ab, welche Felder
   die Kanzlei braucht: Merkmal "wirtschaftlich tätig", Stufe nach § 1 WIdV,
   Status der Mitteilung, Anzahl der Betriebe und Betriebstätten, Zuordnung der
   Unterscheidungsmerkmale zu Tätigkeit, Betrieb oder Betriebstätte, Quelle und
   Datum der Mitteilung, zuständige Rolle. Werte dabei die Felder "Wo laufen
   Mitteilungen des Bundeszentralamts für Steuern auf" und "Ist dieser Ort
   überwacht" aus: Halte den Eingangsweg je Mitteilung fest und benenne es als
   Lücke, wenn dafür keine Rolle angegeben ist. Halte für jedes Feld fest, ob es die
   Nummer selbst enthält; für diese Felder gilt: Sie werden ausschließlich im
   Kanzleisystem geführt und nie in ein KI-Werkzeug übernommen. Für Benennung
   und Schreibweise der Felder verweise auf die Stammdatenkonvention der
   Kanzlei (Prompt 25).
7. Offene Punkte sammeln, einschließlich der Termindivergenz aus Buchstabe e
   und jeder fehlenden Angabe aus Schritt 2.
8. Mandanteninformation formulieren, Sie-Form, höchstens 200 Wörter: was die
   Nummer ist, dass sie von Amts wegen mitgeteilt wird und nicht beantragt
   werden muss, dass Mitteilungen des Bundeszentralamts für Steuern an die
   Kanzlei weiterzuleiten sind, und an wen der Mandant sich wendet. Ohne
   Rechtsgrundlagen im Fließtext, ohne Nummer, ohne Termine, die nach
   Buchstabe e offen sind.

ABBRUCHREGEL – an einer objektiven Angabe, nicht an einer Beurteilung
Ein unvollständig bekannter Bestand ist KEIN Abbruchgrund – er ist der Anlass
dieses Prompts. "unbekannt" in einer Zeile ist kein Abbruchgrund; das gilt
ausdrücklich auch für das Feld "W-IdNr. bereits mitgeteilt" und für Zeilen, in
denen mehrere oder alle Angaben "unbekannt" lauten.
Brich die gesamte Bearbeitung nur ab, wenn das Bestätigungsfeld nicht auf
"bestätigt" steht – auch dann, wenn es unausgefüllt geblieben ist. Gib dann nur
aus: "Abbruchgrund liegt vor – Bestätigung zur Zone Rot fehlt, Bearbeitung an
dieser Stelle abgebrochen, Bestand vor dem erneuten Einsatz bereinigen."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER VOLLSTÄNDIGKEIT DER ANGABEN ab:
   ausreichend / in Teilen lückenhaft / für eine Bestandsaussage noch nicht
   tragfähig. Liste die fehlenden Angaben auf.
2. Jede Zuordnung wird auf das Feld zurückgeführt, aus dem sie folgt. Keine
   Zuordnung ohne Feldbezug.
3. Formuliere jede Aussage, die nicht aus den Angaben oder aus einer benannten
   Fundstelle folgt, ausdrücklich als Vermutung.
4. Höchstens 800 Wörter Fließtext; Tabellen und Listen zählen nicht mit.
5. Führe alle genannten Fundstellen am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Vollständigkeit der Angaben
2. (Betroffenheitsliste) – Tabelle:
   Mandatskürzel | wirtschaftlich tätig (ja / nein / offen) | Feld, aus dem das
   folgt | Stufe nach § 1 WIdV | Feld, aus dem die Stufe folgt | Gruppe nach
   Schritt 3 | nächster Schritt
3. (Mandate mit voraussichtlich mehreren Unterscheidungsmerkmalen) – Tabelle:
   Mandatskürzel | Anzahl Betriebe und Betriebstätten | erwartete Zahl der
   Unterscheidungsmerkmale | wofür sie gebraucht werden
4. (Anzupassende Stammdatenfelder und Formulare) – Tabelle:
   Feld oder Formular | Programm | enthält die Nummer selbst (ja / nein) |
   Eingangsweg der Mitteilung | Rolle | erledigt (leer)
5. (Offene Punkte) – nummeriert, mit je einer Entscheidungs- oder Prüffrage;
   die Termindivergenz aus Buchstabe e steht an erster Stelle und bleibt offen
6. (Mandanteninformation) – höchstens 200 Wörter
7. (Fristen und Termine, die im Raum stehen) – nur dem Grunde nach, mit
   Rechtsgrundlage, ohne Dauer, je mit dem Satz "Fristen berechnet und erfasst
   ein Mensch."
8. (Interne Notiz) – was die Kanzlei prüfen muss, bevor die
   Mandanteninformation hinausgeht; nicht an den Mandanten
9. (Zu verifizierende Rechtsgrundlagen): Nr. | Fundstelle | wofür sie steht |
   geprüft von (leer)
10. Was ich nicht sicher weiß
```

## Anwendung

1. Bestandsliste aus dem Kanzleisystem ziehen und **vor dem Einfügen alle Nummernspalten löschen**, nicht ausblenden und nicht maskieren. Übrig bleiben Kürzel, Merkmale und Ja-Nein-Angaben.
2. Mit einem Ausschnitt beginnen – etwa den Mandaten mit Betriebstätten oder mit Grundstücksbezug. Der vollständige Bestand lohnt erst, wenn die Feldliste steht.
3. Die Liste der Stammdatenfelder zuerst gegen die vorhandene Stammdatenkonvention halten (Prompt 25) und erst dann anlegen; neue Felder ohne Benennungsregel erzeugen denselben Wildwuchs wie bei den Personenkonten.
4. Für jedes Mandat festlegen, wo die Mitteilung des Bundeszentralamts für Steuern auflaufen soll und wer sie in die Stammdaten überträgt. Die Nummer wandert dabei aus dem Postfach in das Kanzleisystem und in kein weiteres Werkzeug.
5. Mandanteninformation erst versenden, wenn die offenen Termine geprüft sind. Ein Anschreiben mit einem Datum, das sich als nicht belegt erweist, erzeugt mehr Rückfragen, als es beantwortet.
6. Bei Neuaufnahmen greift der Weg über den Fragebogen zur steuerlichen Erfassung (Prompt 68); dieser Prompt behandelt den Bestand.

## Qualitätssicherung

- **Prüfen, ob im Ergebnis irgendwo eine Nummer steht.** Wirtschafts-Identifikationsnummer, Steuernummer, Steuer-Identifikationsnummer und USt-IdNr. sind steuerliche Ordnungsmerkmale und gehören nicht in ein KI-Werkzeug – auch nicht als erfundenes Beispiel. Findet sich eine, ist der Durchlauf zu verwerfen und der Bestand vor dem nächsten Einsatz zu bereinigen.
- **Freigabe durch einen Berufsträger** für die Mandanteninformation und für jede Aussage gegenüber Mandanten zu Terminen und Pflichten (Freigabestufe 3 in `DATENSCHUTZ.md`). Vier-Augen-Prinzip auch für die Betroffenheitsliste: Eine zweite Person prüft die Stufenzuordnung stichprobenweise gegen die Stammdaten.
- **Prüfen, ob die Termindivergenz offen geblieben ist.** WIdV, BZSt und BMF-FAQ nennen unterschiedliche Zeitpunkte für die weiteren Unterscheidungsmerkmale. Ein Ergebnis, das sich für einen Termin entscheidet, ist an dieser Stelle falsch; der aktuelle Stand ist bei BZSt und BMF nachzulesen (für [JAHR] verifizieren).
- **Prüfen, ob ein Bezug zur Sozialversicherung auftaucht.** Das Sozialgesetzbuch kennt die Wirtschafts-Identifikationsnummer nicht; jede Aussage, eine Vorschrift des SGB IV sehe sie vor, und jede Gleichsetzung mit der Betriebsnummer ist zu streichen (Volltextprüfung des SGB IV: kein Treffer).
- **Prüfen, ob ein Termin 31.12.2026 genannt wird.** Er ist in keiner amtlichen Quelle belegt und gehört gestrichen.
- **Prüfen, ob § 139b AO für die W-IdNr. zitiert wird.** Diese Vorschrift betrifft ausschließlich natürliche Personen; einschlägig sind § 139a Abs. 1 Satz 3 und Abs. 3 AO sowie § 139c AO, die Verordnungsermächtigung steht in § 139d AO.
- **Prüfen, ob das DDG richtig wiedergegeben ist:** anzugeben ist die USt-IdNr. **oder** die W-IdNr., und nur, wenn eine solche besessen wird – keine Beschaffungspflicht, keine Impressumspflicht für die W-IdNr.
- **Fristen berechnet und erfasst ein Mensch.** Anzeigefristen im Grunderwerbsteuerrecht und Mitteilungspflichten werden nicht aus dem Modell übernommen.
- **Rechtsstand prüfen an:** §§ 139a, 139c und 139d AO sowie § 20 GrEStG und § 5 DDG im amtlichen Volltext (gesetze-im-internet.de), der WIdV in der Fassung des BGBl. 2024 I Nr. 293, den Informationen und dem Vergabestand des Bundeszentralamts für Steuern und dem FAQ des Bundesfinanzministeriums – die drei Quellen zum Zeitpunkt der weiteren Unterscheidungsmerkmale ausdrücklich gegeneinander.

## Varianten

- **Nur Grundstücksfälle:** „Beschränke die Auswertung auf Mandate mit erwarteten Grundstücksgeschäften und erzeuge daraus eine Prüfliste für die grunderwerbsteuerlichen Anzeigen."
- **Nur Betriebstätten:** „Erzeuge ausschließlich die Liste der Mandate mit mehreren Betrieben oder Betriebstätten, mit der erwarteten Zahl der Unterscheidungsmerkmale und der Frage, wer je Einheit zuständig ist."
- **Feldliste für die Stammdaten:** „Erzeuge nur die Liste der anzulegenden Stammdatenfelder mit Benennungsvorschlag, Datentyp und Pflegehinweis, abgestimmt auf die vorhandene Stammdatenkonvention."
- **Mandanteninformation je Gruppe:** „Erzeuge je Stufe nach § 1 WIdV ein eigenes Anschreiben, höchstens 150 Wörter, ohne Termine, die nicht belegt sind."
- **Nachfassliste:** „Erzeuge eine abhakbare Nachfassliste für die Mandate mit unbekanntem Stand, mit Vorschlag für die Rückfrage in einem Satz."
