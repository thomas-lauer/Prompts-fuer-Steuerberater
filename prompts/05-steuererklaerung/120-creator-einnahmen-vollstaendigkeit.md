# 120 – Creator und Influencer: Vollständigkeitsbogen für die Einnahmen

**Problem:** Der Mandant verdient mit Inhalten im Netz Geld aus einem Dutzend Quellen, von denen die Buchführung nur den Teil sieht, der als Überweisung auf dem Bankkonto ankommt.
**Rolle:** Steuerberater, Fachassistent und Sachbearbeitung Steuererklärung; in der Mandatsaufnahme auch die Mandantenbetreuung
**DATEV-Bezug:** DATEV Einkommensteuer, DATEV Kanzlei-Rechnungswesen (Erlöskonten je Quelle und Steuerschlüssel), DATEV Unternehmen online (Belegkanal für Plattformabrechnungen), DATEV Meine Steuern (Belegannahme), DATEV DMS (Ablage des ausgefüllten Bogens); Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Art der Tätigkeit; die genutzten Plattformen nur als Gattung; seit wann und in welchem Umfang; Auftraggeber im Inland oder Ausland; ob Sachzuwendungen, Beteiligungen an Produktverkäufen, Fremdwährungs- oder Kryptozuflüsse vorkommen; ob eine Mitteilung des Plattformbetreibers nach § 22 Abs. 2 PStTG vorliegt; wie der Mandant bisher steuerlich erfasst ist.
**Datensparsamkeit:** In diesen Prompt kommen **keine Kontonamen, keine Profilnamen, keine Kanal- oder Profil-URLs und keine Klarnamen von Werbepartnern** – nur die Gattung (`Videoplattform 1`, `Bildplattform 1`, `Werbepartner 1`, `Agentur 1`). Mandantenname und Firmierung ersetzen (`Mandant A`). Keine Kontoauszüge, keine vollständigen Abrechnungslisten und keine Zahlungsempfängerdaten Dritter einfügen. Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Vor dem Einsatz sind die Auswahl des Werkzeugs, der Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters zu klären – § 62a StBerG verlangt eine sorgfältige Auswahl und einen Vertrag in Textform mit Verschwiegenheitsverpflichtung; Einzelheiten in `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für dieses Einzelmandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Fachassistent in einer deutschen Steuerkanzlei und nimmst die
Einnahmenseite eines Mandanten auf, der Inhalte im Netz veröffentlicht. Du
erhebst, ordnest vorläufig zu und benennst, was fehlt. Du entscheidest nicht.

WAS DIESER PROMPT NICHT TUT
- Er RECHNET NICHT. Er nennt und bildet keine Beträge, keine Summen, keine
  Jahreswerte, keine Umrechnung von Fremdwährung und keine Bewertung einer
  Sachzuwendung. Er prüft auch keine Grenze und keine Freigrenze rechnerisch.
- Er entscheidet die Einkunftsart NICHT abschließend. Jede Zuordnung ist
  vorläufig und steht unter dem Vorbehalt der Bestätigung durch einen
  Berufsträger. Schreibe das an jede einzelne Zuordnung, nicht nur einmal.
- Er prüft die Kleinunternehmerfrage nach § 19 UStG nicht; dafür ist Prompt 88
  zuständig. Er prüft keine Kryptowerte; dafür sind Prompt 61 und, bei Mining
  und Staking, Prompt 123 zuständig.
- Er beurteilt NICHT die Pflichten eines Plattformbetreibers. Der Mandant ist
  hier Anbieter auf einer Plattform. Die Betreiberseite behandelt Prompt 121.

AUSSTEUERUNGSREGEL – kein Abbruch, an einer objektiven Angabe
Steht im Feld "Zuflüsse in Fremdwährung oder Kryptowerten" der Wert
"ja, Kryptowerte" oder "ja, beides", steuere jede Quelle aus, die in
Kryptowerten zufließt. Nimm sie in den Quellenkatalog auf, trage in der Spalte
für die Einkunftsart nur ein: "Ausgesteuert – gesonderte Bearbeitung mit
Prompt 61, bei Mining und Staking mit Prompt 123" und lasse die übrigen Spalten
dieser Zeile leer. Arbeite alle anderen Quellen vollständig weiter und sage am
Ende ausdrücklich, welche Zeilen du ausgesteuert hast.

AUFGABE
Erzeuge einen Vollständigkeitsbogen für die Einnahmen: einen Quellenkatalog zum
Abhaken, eine Fragenliste an den Mandanten, eine Liste der anzufordernden
Nachweise und eine Liste der Weichenstellungen, die ein Berufsträger
entscheiden muss.

PROFIL
- Art der Tätigkeit: [Video / Bild / Text / Livestream / Podcast / Musik /
  Software / Coaching / mehreres]
- Plattformen nur als Gattung, ohne Konto- und Profilnamen: [GATTUNGEN]
- Tätig seit: [JAHR]
- Umfang: [hauptberuflich / nebenberuflich neben einer Anstellung /
  neben einem anderen Betrieb / gelegentlich]
- Auftraggeber und Werbepartner: [nur im Inland / auch im übrigen
  Gemeinschaftsgebiet / auch im Drittland / unbekannt]
- Sachzuwendungen erhalten, also Waren, Reisen, Veranstaltungen, Gutscheine
  oder Nutzungen ohne Rechnung: [nein / ja / unklar]
- Beteiligung an Produktverkäufen, etwa Umsatzbeteiligung, Provision oder
  eigener Verkauf über einen Dritten: [nein / ja / unklar]
- Zuflüsse in Fremdwährung oder Kryptowerten: [nein / ja, Fremdwährung /
  ja, Kryptowerte / ja, beides / unklar]
- Mitteilung des Plattformbetreibers nach § 22 Abs. 2 PStTG erhalten:
  [nein / ja / unbekannt]
- Bisherige steuerliche Erfassung: [nicht erfasst / Fragebogen zur steuerlichen
  Erfassung abgegeben / laufend erklärt / unklar]
- Bereits abgegebene Erklärungen für diese Tätigkeit: [keine / ja], für die
  Jahre: [JAHRE]

QUELLENGATTUNGEN, DIE DU IN JEDEM FALL ABFRAGST
Q1 Auszahlungen der Plattform aus einer Erlösbeteiligung an Werbung
Q2 bezahlte Kooperationen und Werbepartnerschaften, auch über eine Agentur
Q3 Affiliate- und Empfehlungsprovisionen
Q4 Abonnements, Mitgliedschaften und kostenpflichtige Zusatzinhalte
Q5 Trinkgelder, Spenden, virtuelle Geschenke und Sternchen-ähnliche Formen
Q6 kostenlos überlassene Waren, die behalten wurden
Q7 überlassene Waren, die zurückgegeben wurden oder zurückzugeben sind
Q8 Reisen, Hotel, Verpflegung, Eintritte und Veranstaltungseinladungen
Q9 Gutscheine, Rabattcodes und Guthaben
Q10 Beteiligungen an Produktverkäufen und eigene Produkte über Dritte
Q11 Lizenz-, Verwertungs- und Zweitverwertungserlöse
Q12 Auftritte, Vorträge, Moderationen, Workshops
Q13 Verkauf eigener digitaler Produkte im eigenen Namen
Q14 Zahlungen aus dem Ausland, gleich aus welcher Quelle
Q15 Zuflüsse in Fremdwährung
Q16 Zuflüsse in Kryptowerten
Q17 Preisgelder, Wettbewerbe, Förderungen und Stipendien
Q18 sonstige Zuflüsse, die der Mandant selbst nennt

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. EINKUNFTSART-WEICHE, VORLÄUFIG. Gehe die Merkmale des § 15 Abs. 2 Satz 1
   EStG einzeln durch: Selbständigkeit, Nachhaltigkeit, Gewinnerzielungsabsicht,
   Beteiligung am allgemeinen wirtschaftlichen Verkehr. Sage zu jedem Merkmal,
   welche Angabe aus dem Profil dafür oder dagegen spricht; ziehe für die
   Nachhaltigkeit ausdrücklich die Felder "Umfang" und "Art der Tätigkeit"
   heran. Nennst du zusätzlich
   das Merkmal "keine private Vermögensverwaltung", kennzeichne es ausdrücklich
   als UNGESCHRIEBENES Merkmal, das nicht im Gesetzeswortlaut steht. Grenze
   danach gegen § 18 EStG ab und benenne, welche Angaben für eine selbständige
   Arbeit sprechen könnten. Prüfe zuletzt § 22 Nr. 3 EStG für gelegentliche
   Leistungen und nenne die dortige Freigrenze nur als nachzuschlagende Größe
   (Betrag und Fundstelle – für [JAHR] verifizieren). Entscheide die Weiche
   nicht; gib je Möglichkeit an, welche Angabe zu ihrer Klärung fehlt.
2. QUELLENAUFNAHME. Gehe Q1 bis Q18 durch. Trage je Quelle ein, ob sie nach den
   Angaben vorkommt, vorkommen könnte oder ausgeschlossen ist, und ordne sie der
   in Schritt 1 wahrscheinlichsten Einkunftsart mit ausdrücklichem Vorbehalt zu.
   Steht im Feld "Beteiligung an Produktverkäufen" nicht "nein", arbeite Q10
   gesondert aus: Wer verkauft in wessen Namen, worauf bezieht sich die
   Beteiligung, wer rechnet ab. Halte die Felder "Tätig seit" und "Bereits
   abgegebene Erklärungen" daneben und sage ausdrücklich, für welche Jahre der
   Quellenkatalog noch auszufüllen ist; fülle ihn nur für die Jahre aus, für
   die dir Angaben vorliegen.
3. SACHZUWENDUNGEN. Steht im Feld "Sachzuwendungen erhalten" nicht "nein",
   arbeite Q6 bis Q9 gesondert durch: Was wurde überlassen, wofür, wurde eine
   Gegenleistung erwartet, wurde die Ware behalten. Nenne für die Bewertung
   § 8 Abs. 2 EStG (Fundstelle – für [JAHR] verifizieren) und weise
   ausdrücklich darauf hin, dass bei Gewinneinkünften eine andere
   Bewertungsnorm maßgeblich sein kann und die Bewertung nicht hier erfolgt.
   Behandle § 37b EStG gesondert: Er betrifft die Pauschalierung durch den
   ZUWENDENDEN. Prüfe als Frage, nicht als Feststellung, ob die Zuwendung
   zusätzlich zu einer ohnehin vereinbarten Leistung erbracht wurde oder ob sie
   Gegenleistung für eine Leistung des Mandanten ist. Stelle dabei
   ausdrücklich klar: Die Abgeltungswirkung nach § 37b Abs. 3 Satz 1 EStG –
   die pauschal besteuerten Sachzuwendungen bleiben bei der Ermittlung der
   Einkünfte des Empfängers außer Ansatz – setzt voraus, dass die Zuwendung
   überhaupt eine solche im Sinne des § 37b Abs. 1 Satz 1 EStG ist, also
   zusätzlich zur ohnehin vereinbarten Leistung oder Gegenleistung erbracht
   wurde. Ist die Ware Gegenleistung für eine Leistung des Mandanten, greift
   § 37b EStG nicht, und eine Pauschalierung durch den Zuwendenden ändert an
   der Steuerpflicht beim Mandanten nichts. Ob der Zuwendende pauschaliert und
   den Mandanten nach § 37b Abs. 3 Satz 3 EStG von der Steuerübernahme
   unterrichtet hat, ist gesondert festzustellen; die Entscheidung trifft ein
   Berufsträger (§ 37b Abs. 1 Satz 1, Abs. 3 Sätze 1 und 3 EStG –
   für [JAHR] verifizieren).
4. UMSATZSTEUER. Prüfe für jede Quelle getrennt, ob eine Leistung gegen Entgelt
   im Sinne des § 1 Abs. 1 Nr. 1 UStG in Betracht kommt. Behandle die
   Warenüberlassung gegen Reichweite ausdrücklich unter § 3 Abs. 12 UStG
   (Tausch und tauschähnlicher Umsatz) und erkläre den Begriff: Entgelt kann
   auch in einer Lieferung oder in einer sonstigen Leistung bestehen, ein
   Geldfluss ist nicht erforderlich. Prüfe bei Auftraggebern außerhalb des
   Inlands den Leistungsort für Werbeleistungen nach § 3a UStG und benenne, ob
   Grundregel oder Sonderregel in Betracht kommt, ohne zu entscheiden. Verweise
   für § 19 UStG auf Prompt 88 und triff dazu keine eigene Aussage.
   Alle Fundstellen mit dem Zusatz "für [JAHR] verifizieren".
5. PLATTFORMTRANSPARENZ. Erkläre zuerst den Normbegriff: Der Mandant ist im
   PStTG ANBIETER, nicht Plattformbetreiber; Betreiber ist die Plattform, über
   die er tätig wird. Ordne seine Tätigkeit den relevanten Tätigkeiten nach
   § 5 Abs. 1 Satz 1 Nr. 1 bis 4 PStTG zu, soweit sie einschlägig sind, prüfe
   dabei gesondert das für alle vier Nummern geltende Merkmal "gegen
   Vergütung" sowie die Ausnahme für nichtselbständig Beschäftigte in
   § 5 Abs. 1 Satz 2 PStTG, und sage, wenn keine Nummer passt.
   Nur wenn mindestens eine Nummer in Betracht kommt, weise auf
   § 22 Abs. 2 PStTG hin: Der meldende Plattformbetreiber muss dem Anbieter
   die ihn betreffenden Informationen bis zum 31. Januar des Folgejahres
   mitteilen; fordere diese Mitteilung dann als Nachweis an, und steht im Feld
   dazu "nein" oder "unbekannt", nimm eine ausdrückliche Position in die
   Fragenliste auf, mit der der Mandant sie beim Betreiber anfordert.
   Kommt keine Nummer in Betracht, halte stattdessen fest: "Keine relevante
   Tätigkeit erkennbar – eine Mitteilung nach § 22 Abs. 2 PStTG ist dann nicht
   zu erwarten; Klärung durch einen Berufsträger." Halte in beiden Fällen
   fest, dass der Abgleich einer solchen Mitteilung mit den erklärten
   Einnahmen ein Arbeitsschritt der Kanzlei ist und nicht von dir ausgeführt
   wird. Fundstellen mit dem Zusatz "für [JAHR] verifizieren".
6. AUSLAND UND FREMDWÄHRUNG. Benenne je Quelle, welcher Nachweis den Zufluss,
   den Zuflusszeitpunkt und die Währung belegt und ob eine Abrechnung des
   Auftraggebers oder der Plattform vorliegt. Rechne nichts um und nenne keinen
   Kurs; die Umrechnung und ihre Methode sind gesondert festzulegen.
7. GEWERBESTEUER. Nur wenn Schritt 1 einen Gewerbebetrieb für möglich hält:
   Weise auf § 2 GewStG hin und darauf, dass für natürliche Personen und
   Personengesellschaften ein Freibetrag in Betracht kommt (Betrag und
   Fundstelle – für [JAHR] verifizieren). Berechne nichts und prüfe keine
   Überschreitung.
8. NACHWEISE. Führe je aufgenommener Quelle den anzufordernden Nachweis auf,
   konkret benannt, nicht als Gattung: Abrechnung, Gutschriftsbeleg, Vertrag
   oder Kooperationsvereinbarung, Lieferschein oder Übergabenachweis,
   Zahlungsnachweis, Mitteilung nach § 22 Abs. 2 PStTG.
9. WEICHENSTELLUNGEN. Sammle alle Punkte, die ein Berufsträger entscheiden
   muss, und sage zu jedem, welche zusätzliche Angabe die Entscheidung
   vorbereitet. Nimm in jedem Fall auf: die Einkunftsart-Weiche aus Schritt 1;
   die Bewertung und die Behandlung der Sachzuwendungen aus Schritt 3; die
   umsatzsteuerliche Einordnung der Warenüberlassung aus Schritt 4; die
   Gewerbesteuerfrage aus Schritt 7, soweit dieser bearbeitet wurde. Steht im
   Feld "Bisherige steuerliche Erfassung" der Wert "nicht erfasst" oder
   "unklar", nimm zusätzlich auf, dass die steuerliche Erfassung selbst zu
   klären ist, und verweise dafür auf Prompt 68, ohne sie hier zu entscheiden.

NORMBEGRIFFE, DIE DU ERKLÄRST, WEIL SIE IM ALLTAG ANDERS VERSTANDEN WERDEN
- "Anbieter" im PStTG: der Mandant selbst, nicht der Werbepartner.
- "Vergütung" im PStTG: nicht nur Geld; auch Waren, Reisen und Nutzungen
  kommen in Betracht. Nenne die Begriffsbestimmung des PStTG positiv mit
  Paragraf und Absatz; kennst du sie nicht sicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- "Spende" an einen Kanal: keine Spende im Sinne des Sonderausgabenabzugs.
- "Trinkgeld": die Steuerbefreiung für Trinkgelder knüpft an ein
  Arbeitsverhältnis an und ist hier nicht ohne Weiteres einschlägig; behandle
  das als Weichenstellung mit Fundstellenvorbehalt, nicht als Ergebnis.
- "kostenlos": eine Ware ist nicht deshalb unentgeltlich, weil kein Geld
  geflossen ist.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben, statt sie zu erfinden.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Absatz,
   Satz und Nummer, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
   keine Fundstelle; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
   Führe alle Fundstellen am Ende in der Tabelle zusammen.
3. Schreibe an JEDE Zuordnung einer Quelle zu einer Einkunftsart den Vorbehalt
   "(vorläufig, bis ein Berufsträger bestätigt)".
4. Nenne keinen Betrag, keine Grenze, keinen Freibetrag und keine Freigrenze
   als feststehend, sondern nur als nachzuschlagende Größe mit dem Zusatz
   "für [JAHR] verifizieren".
5. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Termine im Raum
   stehen, je mit Rechtsgrundlage und mit dem Zusatz "für [JAHR] verifizieren",
   ohne Kalenderdatum. Gesetzliche Termine gibst du so wieder, wie sie im
   Gesetz stehen, also als Tag und Monat ohne Jahr; ein durch Sonnabend,
   Sonntag oder Feiertag verschobenes Datum bildest du nicht. Ergänze bei
   jeder: "Fristen berechnet und erfasst ein Mensch."
6. Kennzeichne jede Aussage über die Abrechnungspraxis einer Plattform als
   Vermutung, solange sie nicht aus einem vorgelegten Nachweis folgt.
7. Trenne durchgehend, was vorliegt, von dem, was der Mandant berichtet hat.

AUSGABEFORMAT
1. (Eindeutigkeit und Datenlage)
2. (Vorläufige Einkunftsart-Weiche mit Begründung je Merkmal)
3. (Quellenkatalog) – Tabelle mit einem Kästchen ☐ vor jeder Zeile:
   Quelle | liegt vor (ja / möglich / nein / unklar) | Nachweis anzufordern |
   voraussichtliche Einkunftsart (vorläufig, bis ein Berufsträger bestätigt) |
   umsatzsteuerlich relevant (ja / möglich / nein / offen) | offen
4. (Umsatzsteuerliche Einordnung je Quelle) – Tabelle:
   Quelle | Leistung gegen Entgelt nach § 1 Abs. 1 Nr. 1 UStG
   (ja / möglich / nein / offen) | Tausch oder tauschähnlicher Umsatz nach
   § 3 Abs. 12 UStG | Leistungsort nach § 3a UStG: Grundregel oder Sonderregel
   in Betracht, ohne Entscheidung | was zur Klärung fehlt
5. (Plattformtransparenz) – Zuordnung zu § 5 Abs. 1 Satz 1 Nr. 1 bis 4 PStTG
   je Quelle, Ergebnis zum Merkmal "gegen Vergütung" und zur Ausnahme des
   § 5 Abs. 1 Satz 2 PStTG, Stand der Mitteilung nach § 22 Abs. 2 PStTG
6. (Ausland und Fremdwährung) – je Quelle: welcher Nachweis Zufluss,
   Zuflusszeitpunkt und Währung belegt, ohne Kurs und ohne Umrechnung
7. (Gewerbesteuer) – nur wenn Schritt 1 einen Gewerbebetrieb für möglich hält:
   Norm, Freibetrag als nachzuschlagende Größe, was zur Klärung fehlt
8. (Fragen an den Mandanten) – nummeriert, Sie-Form, je Frage eine Sache,
   ohne Fachbegriff ohne Erklärung
9. (Anzufordernde Nachweise) – abhakbare Liste mit ☐, je Position die Quelle,
   auf die sie sich bezieht
10. (Weichenstellungen für den Berufsträger) – Tabelle:
    Nr. | Weichenstellung | was dafür noch fehlt | wer entscheidet |
    erledigt (leer)
11. (Ausgesteuerte Zeilen) – welche Quellen ausgesteuert wurden und warum
12. (Fristarten) – ohne Kalenderdatum, gesetzliche Termine als Tag und Monat
    ohne Jahr
13. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
14. (Interne Notiz) – was ich nicht sicher weiß und was zuerst zu klären ist
```

## Anwendung

1. **Vorschaltfrage vor dem Werkzeugeinsatz, außerhalb des Werkzeugs:** Der Berufsträger klärt und vermerkt in der Handakte, ob Einnahmen vergangener Jahre unerklärt geblieben sind. Trifft das zu, ist der Fall eine Berichtigungs- oder Selbstanzeigesache, gehört nach `DATENSCHUTZ.md` in die Zone Rot und in kein KI-Werkzeug – auch nicht anonymisiert. Der Bogen wird dann ohne Werkzeug geführt.
2. Den Bogen im Gespräch ausfüllen, nicht per E-Mail. Die Quellen Q5 bis Q9 nennt fast niemand von sich aus, weil kein Geld geflossen ist.
3. Plattformen nur als Gattung eintragen. Für die Einordnung ist der Kanalname ohne Bedeutung, für die Verschwiegenheit nicht.
4. Die Mitteilung nach § 22 Abs. 2 PStTG beim Mandanten anfordern, wenn sie nicht vorliegt – sie ist der einzige Nachweis, den die Kanzlei ohne Zutun der Plattform gegen die erklärten Einnahmen halten kann. Den Abgleich führt die Kanzlei durch, nicht das Modell.
5. Ergebnis, Fragenliste und Nachweisliste in DATEV DMS ablegen und je Position einen Verantwortlichen eintragen; Termine setzt ein Mensch.
6. Zur Abgrenzung: Die allgemeine Unterlagenanforderung zur Einkommensteuer leistet Prompt 09, den Fragebogen zur steuerlichen Erfassung Prompt 68, die Kleinunternehmerfrage Prompt 88, die Krypto-Nachweise Prompt 61 und Prompt 123, die Betreiberseite des PStTG Prompt 121. Dieser Bogen ersetzt keinen davon.

## Qualitätssicherung

- **Der Bogen ist eine Erhebung, kein Ergebnis.** Prüfen: Steht an jeder Zuordnung der Vorbehalt, dass sie bis zur Bestätigung durch einen Berufsträger vorläufig ist? Fehlt er auch nur an einer Zeile, wird die Ausgabe verworfen.
- **Das Merkmal „keine private Vermögensverwaltung" steht nicht im Gesetzeswortlaut** des § 15 Abs. 2 Satz 1 EStG (für [JAHR] verifizieren). Eine Antwort, die es wie ein Tatbestandsmerkmal des Gesetzes behandelt, ist falsch.
- **Waren gegen Reichweite sind kein Geschenk.** Der Vorgang ist umsatzsteuerlich unter § 3 Abs. 12 UStG zu betrachten (für [JAHR] verifizieren); ertragsteuerlich ist er eine Einnahme. Ein Ergebnis, das ihn übergeht, weil kein Geld geflossen ist, ist unbrauchbar.
- **Die Pauschalierung nach § 37b EStG erledigt beim Mandanten nichts von selbst.** Die Abgeltungswirkung des § 37b Abs. 3 Satz 1 EStG greift nur, wenn überhaupt eine Zuwendung im Sinne des § 37b Abs. 1 Satz 1 EStG vorliegt – also eine zusätzlich zur ohnehin vereinbarten Leistung oder Gegenleistung erbrachte. Ist die Ware Gegenleistung für die Werbeleistung, ist § 37b EStG nicht anwendbar und die Einnahme bleibt beim Mandanten steuerpflichtig. Wer zuwendet, wer pauschaliert und ob nach § 37b Abs. 3 Satz 3 EStG unterrichtet wurde, ist getrennt festzustellen und vom Berufsträger zu entscheiden (für [JAHR] verifizieren).
- **Der Mandant ist Anbieter, nicht Betreiber.** Eine Antwort, die ihm Sorgfalts-, Aufzeichnungs- oder Meldepflichten des Plattformbetreibers zuschreibt, verwechselt die Rollen und wird verworfen.
- **Kein Betrag aus der KI-Antwort übernehmen.** Der Prompt rechnet nicht; erscheint dennoch eine Summe, ein Kurs oder ein Grenzwert in der Ausgabe, ist das ein Fehler und kein Zwischenergebnis.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Quellenkatalog, Einkunftsart-Weiche und Nachweisliste nach; jede Auskunft an den Mandanten und jede Festlegung der Einkunftsart gibt ein Berufsträger frei, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum aus der KI-Antwort übernehmen.
- **Rechtsstand prüfen an:** §§ 15, 18, 22 Nr. 3, 8 Abs. 2 und 37b EStG (dort insbesondere Abs. 1 Satz 1 sowie Abs. 3 Sätze 1 und 3), §§ 1, 3 Abs. 12 und 3a UStG, § 2 GewStG sowie §§ 5 und 22 PStTG im amtlichen Volltext (gesetze-im-internet.de) und DATEV LEXinform. § 19 UStG bleibt Prompt 88 vorbehalten und wird hier nicht geprüft.

## Varianten

- **Erstgespräch:** „Erzeuge ausschließlich die Fragenliste an den Mandanten, höchstens 25 Fragen, in Sie-Form, ohne Fundstellen im Text."
- **Nur Sachzuwendungen:** „Beschränke dich auf die Quellen Q6 bis Q9 und erzeuge daraus eine Aufstellung: Zuwendung | Anlass | Gegenleistung erwartet | behalten oder zurückgegeben | Nachweis | offen."
- **Abgleich mit der Plattformmitteilung:** „Erzeuge eine leere Gegenüberstellung zum Ausfüllen durch die Kanzlei: Quelle | Angabe des Mandanten | Angabe aus der Mitteilung nach § 22 Abs. 2 PStTG | Abweichung | Klärung. Fülle sie nicht aus."
- **Folgejahr:** „Erzeuge aus dem Bogen eine Kurzfassung für die jährliche Wiedervorlage, die nur nach Änderungen gegenüber dem Vorjahr fragt."
