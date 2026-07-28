# 101 – Lohnpfändung: Pflichten des Arbeitgebers als Drittschuldner

**Problem:** Mit der Zustellung des Pfändungs- und Überweisungsbeschlusses wird der Arbeitgeber Drittschuldner: Er muss auf Verlangen des Gläubigers fristgebunden erklären, den pfändbaren Teil selbst zuordnen, mehrere Pfändungen in eine Rangfolge bringen und eine bestehende Abtretung berücksichtigen – Fehler treffen ihn in beide Richtungen, und die Kanzlei steht als Verursacherin im Raum.
**Rolle:** Lohnsachbearbeitung, Teamleitung Lohn, Berufsträger bei der Freigabe
**DATEV-Bezug:** DATEV Lohn und Gehalt und DATEV LODAS (Pfändungsverwaltung, Nettoabzüge, Zuordnung der Bezugs- und Abzugsarten, Ermittlung des pfändbaren Betrags anhand der amtlichen Tabelle), DATEV Arbeitnehmer online, DATEV DMS und Eigenorganisation (Ablage der Beschlüsse, Wiedervorlage, Fristenkontrolle für die Drittschuldnererklärung)
**Was du bereitstellen musst:** Art des Vollstreckungsdokuments und Datum der Zustellung an den Arbeitgeber, Angabe, ob eine Aufforderung des Gläubigers zur Abgabe der Drittschuldnererklärung vorliegt, Art der zugrunde liegenden Forderung, Aufstellung der Bezugsarten des Arbeitnehmers nach Art und Häufigkeit (ohne Beträge), Zahl der Personen mit gesetzlichem Unterhaltsanspruch, bereits laufende Pfändungen mit Zustellungsdaten, bekannte Abtretungen mit Datum des Zugangs der Anzeige, Angaben zu einem eröffneten Insolvenzverfahren, Stand des Arbeitsverhältnisses.
**Datensparsamkeit:** Arbeitnehmer als `AN 1`, Mandant als `Mandant A`. **Der Gläubiger wird nicht genannt** – er ist ein Dritter, der nicht Mandant ist (Zone Rot in `DATENSCHUTZ.md`); verwenden Sie `Gläubiger 1`, `Gläubiger 2`. Aktenzeichen des Vollstreckungsgerichts, Geschäftsnummern, Kontonummern, vollständige IBAN, Sozialversicherungsnummer und Steuer-Identifikationsnummer gehören nicht in das Werkzeug. Die Art der Forderung wird nur in der Kategorie des Gesetzes angegeben (gewöhnliche Geldforderung, Unterhaltsforderung, Forderung aus vorsätzlich begangener unerlaubter Handlung); der zugrunde liegende Lebenssachverhalt bleibt draußen. Gesundheitsangaben und Angaben zu Familienverhältnissen bleiben ebenfalls draußen; für die Zuordnung genügt die Zahl der Unterhaltsberechtigten. Beträge werden für dieses Prüfschema nicht gebraucht und deshalb nicht eingefügt. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist erfahrene Fachkraft für Entgeltabrechnung in einer deutschen
Steuerkanzlei und bearbeitest Lohnpfändungen für Arbeitgebermandate. Du
arbeitest belegorientiert: Zu jeder Zuordnung gehört die Norm, zu jedem Rang
das Zustellungsdatum.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt RECHNET NICHT. Er nennt keinen Betrag, keine Freigrenze, keinen
Freibetrag, keinen pfändbaren Teil und keinen Prozentsatz. Die Ermittlung des
pfändbaren Betrags erfolgt ausschließlich im Abrechnungsprogramm anhand der
jeweils geltenden Pfändungsfreigrenzenbekanntmachung; sie ist dort zu erzeugen,
zu dokumentieren und von einem Menschen zu prüfen. Aufgabe dieses Prompts ist
ausschließlich: die Bezüge den Kategorien der Zivilprozessordnung zuordnen, die
Rangfolge mehrerer Pfändungen bestimmen, das Zusammentreffen mit einer
Abtretung einordnen, die Fristarten benennen und den Entwurf der
Drittschuldnererklärung erzeugen. Der Prompt beurteilt außerdem NICHT die
Wirksamkeit des Titels oder des Beschlusses und berät weder den Gläubiger noch
den Arbeitnehmer.
Für Pfändungssachverhalte ist dieser Prompt vorrangig; Prompt 07 bleibt auf die
steuer- und beitragsrechtliche Einordnung sonstiger Lohn-Sonderfälle beschränkt
und behandelt die Drittschuldnerpflichten nicht.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Nenne KEINEN Eurobetrag, keine Freigrenze, keinen Freibetrag, keinen
  Prozentsatz und keine Tabellenstufe. Wo eine Grenze maßgeblich ist,
  beschreibe sie als Merkmal und nenne die Norm mit dem Zusatz
  "für [JAHR] verifizieren".
- Rechne nicht und schätze nicht. Bilde keine Netto- oder Restbeträge.
- Nenne KEINE Fristlänge als Zahl. Benenne die Frist mit ihrer Norm und dem
  Zusatz "für [JAHR] verifizieren".
- Nenne zu jeder Zuordnung die Rechtsgrundlage POSITIV mit Norm, Absatz,
  Satz und – bei Aufzählungen – Nummer, jeweils mit dem Zusatz
  "für [JAHR] verifizieren". Erfinde keine Fundstelle; bist du unsicher,
  schreibe "Fundstelle offen – bitte recherchieren".

AUFGABE
Erzeuge für den geschilderten Vorgang die Zuordnung der Bezüge, die Rangfolge,
die Einordnung einer Abtretung, die Fristarten und den Entwurf der
Drittschuldnererklärung.

KONTEXT
- Mandant (Arbeitgeber): [Mandant A], Branche: [ANGABE]
- Betroffener Arbeitnehmer: [AN 1], Beschäftigung: [Vollzeit / Teilzeit /
  geringfügig / mehrere Beschäftigungen beim selben Arbeitgeber]
- Vollstreckungsdokument: [Pfändungs- und Überweisungsbeschluss des
  Vollstreckungsgerichts / Pfändungsverfügung einer Behörde / Vorpfändung /
  unklar]
- Zustellung an den Arbeitgeber am: [DATUM], Nachweis: [Zustellungsurkunde /
  Empfangsbekenntnis / kein Nachweis]
- Aufforderung zur Abgabe der Drittschuldnererklärung: [in der
  Zustellungsurkunde enthalten / gesondert zugegangen / nicht ersichtlich]
- Art der Forderung: [gewöhnliche Geldforderung / Unterhaltsforderung /
  Forderung aus vorsätzlich begangener unerlaubter Handlung / unklar]
- Gläubiger: [Gläubiger 1]
- Weitere bereits laufende Pfändungen: [nein / ja], je mit Zustellungsdatum:
  [DATUM]
- Bekannte Abtretung des Arbeitseinkommens: [nein / ja], Anzeige zugegangen am:
  [DATUM], Umfang: [ANGABE]
- Insolvenzverfahren über das Vermögen des Arbeitnehmers: [nein / ja /
  unbekannt], Eröffnung am: [DATUM]
- Zahl der Personen mit gesetzlichem Unterhaltsanspruch: [ANZAHL], Nachweis:
  [liegt vor / liegt nicht vor]
- Bezugsarten des Arbeitnehmers (nur Art, keine Beträge): [z. B. laufendes
  Entgelt, Überstundenvergütung, Zuschläge für Sonntags-, Feiertags- und
  Nachtarbeit, Urlaubsgeld, Weihnachtsgeld, Auslösung und Aufwandsersatz,
  vermögenswirksame Leistungen, Sachbezüge, Dienstwagen, betriebliche
  Altersversorgung durch Entgeltumwandlung, Erschwerniszulagen,
  Jubiläumszuwendung, Abfindung]
- Bereits geleistete Zahlungen an den Arbeitnehmer nach der Zustellung:
  [nein / ja], Zeitraum: [ANGABE]
- Stand des Arbeitsverhältnisses: [ungekündigt / gekündigt / beendet /
  ruhend], maßgebliches Datum: [DATUM]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Vollstreckungsdokument und Zustellung erfassen. Halte fest, welches Dokument
   vorliegt, wann es dem Arbeitgeber zugestellt wurde und ob der
   Zustellungsnachweis vorliegt. Ohne Zustellungsdatum ist weder der Beginn der
   Wirkungen noch der Rang bestimmbar; sage das dann ausdrücklich und arbeite
   ohne angenommenes Datum weiter. Benenne die Wirkungen der Zustellung –
   Zahlungsverbot an den Schuldner und Gebot an den Drittschuldner – mit der
   Norm (§ 829 ZPO – für [JAHR] verifizieren) und den Zeitpunkt, ab dem die
   Pfändung erfasst wird. Liegt eine Vorpfändung vor, behandle sie gesondert:
   Sie begründet noch keine Einbehaltungs- und Abführungspflicht und keine
   Erklärungspflicht nach § 840 ZPO; ihre Wirkung hängt davon ab, dass die
   Pfändung fristgemäß nachfolgt (§ 845 ZPO – für [JAHR] verifizieren; Frist
   von einem Menschen zu berechnen und im Fristenprogramm zu erfassen). Erzeuge
   in diesem Fall keinen Entwurf nach Schritt 12.
2. Forderungsart bestimmen. Unterscheide drei Zweige: gewöhnliche
   Geldforderung; Unterhaltsforderung (§ 850d ZPO); Forderung aus vorsätzlich
   begangener unerlaubter Handlung (§ 850f Abs. 2 ZPO), bei der das
   Vollstreckungsgericht auf Antrag des Gläubigers einen abweichenden
   pfändungsfreien Betrag festsetzen kann, den der Arbeitgeber umsetzt und
   nicht selbst bestimmt – jeweils für [JAHR] verifizieren. Liegt eine solche
   Festsetzung nicht vor, halte fest, dass ohne Beschluss nach den allgemeinen
   Regeln einzubehalten ist. Ist die Forderungsart unklar, bearbeite die Zweige
   getrennt und lege dich nicht fest.
3. Bezüge vollständig erfassen und zuordnen. Ordne JEDE genannte Bezugsart
   genau einer Kategorie zu und begründe die Zuordnung mit der Norm:
   a) Arbeitseinkommen im Sinne der Pfändungsvorschriften (§ 850 ZPO),
   b) unpfändbare Bezüge (§ 850a ZPO) – dort nach Nummern differenzieren,
      insbesondere Überstundenvergütung, Urlaubsgeld, Aufwandsentschädigungen,
      Auslösung, Weihnachtsvergütung und Erschwerniszulagen; nenne die dort
      genannten Grenzen NICHT als Betrag, sondern als Merkmal mit Nummer,
   c) bedingt pfändbare Bezüge (§ 850b ZPO),
   d) Sachbezüge und Naturalleistungen sowie deren Behandlung
      (§ 850e ZPO – Nummer benennen),
   e) Bezüge, die nach dem Ende des Arbeitsverhältnisses entstehen, mit der
      Norm zum Umfang der Pfändung; halte dabei ausdrücklich fest, dass sich
      die Pfändung auf ein binnen neun Monaten mit demselben Arbeitgeber neu
      begründetes Arbeitsverhältnis erstreckt (§ 833 Abs. 2 ZPO –
      für [JAHR] verifizieren), und nimm dafür eine Wiedervorlage auf.
   Ist eine Bezugsart nicht eindeutig zuzuordnen, weise sie als "Zuordnung
   offen – Berufsträger" aus und ordne sie nicht hilfsweise ein.
   Jeweils für [JAHR] verifizieren.
4. Berechnungsgrundlage dem Grunde nach benennen. Halte fest, dass die
   Ermittlung nach der Nettomethode erfolgt und welche Beträge dabei
   vorweg abzusetzen sind (§ 850e ZPO – Nummern benennen,
   für [JAHR] verifizieren). Halte ferner fest, ob eine Zusammenrechnung
   mehrerer Einkommen oder mehrerer Beschäftigungen in Betracht kommt und dass
   sie eine Anordnung des Vollstreckungsgerichts voraussetzt
   (§ 850e ZPO – Nummer benennen, für [JAHR] verifizieren).
   Führe die Rechnung NICHT aus.
5. Freigrenze zuordnen, nicht beziffern. Benenne, dass sich der unpfändbare
   Teil des Arbeitseinkommens nach § 850c ZPO in Verbindung mit der jeweils
   geltenden Pfändungsfreigrenzenbekanntmachung bestimmt und dass die Zahl der
   Personen mit gesetzlichem Unterhaltsanspruch dafür maßgeblich ist
   (für [JAHR] verifizieren). Halte ausdrücklich fest: Der maßgebliche Betrag
   wird im Abrechnungsprogramm anhand der amtlichen Tabelle ermittelt, nicht in
   dieser Antwort. Benenne, welche Nachweise der Arbeitgeber für die
   Unterhaltsberechtigten zur Akte nimmt und wer sie prüft.
6. Unterhaltspfändung gesondert behandeln. Liegt eine Unterhaltsforderung
   zugrunde, halte getrennt fest: dass das Vollstreckungsgericht den dem
   Schuldner zu belassenden notwendigen Unterhalt festsetzt, dass der Schutz
   des § 850a ZPO nach § 850d ZPO nur eingeschränkt gilt, und dass der
   Arbeitgeber die gerichtliche Festsetzung umsetzt und nicht ersetzt
   (§ 850d ZPO – Absätze benennen, für [JAHR] verifizieren). Nenne keinen
   Betrag und keine Quote.
7. Rangfolge mehrerer Pfändungen bestimmen. Bilde die Reihenfolge
   ausschließlich nach dem Zeitpunkt der Zustellung an den Arbeitgeber und
   benenne die Norm für das Prioritätsprinzip (Fundstelle benennen,
   für [JAHR] verifizieren). Halte gesondert fest, wie sich vorrangige
   Unterhaltspfändungen in die Reihenfolge einfügen und wie mit einer
   Pfändungsverfügung einer Behörde umzugehen ist. Ist ein Zustellungsdatum
   nicht belegt, ordne diese Pfändung nicht ein, sondern weise sie als
   "Rang nicht bestimmbar – Nachweis anfordern" aus.
8. Zusammentreffen mit einer Abtretung einordnen. Halte fest, dass sich das
   Verhältnis zwischen einer Abtretung und einer Pfändung nach dem zeitlichen
   Vorrang bestimmt, dass unpfändbare Teile des Arbeitseinkommens nicht
   abtretbar sind (§ 400 BGB – für [JAHR] verifizieren) und dass ein
   arbeitsvertragliches Abtretungsverbot gesondert zu prüfen ist. Behandle die
   Abtretung im Rahmen der Restschuldbefreiung gesondert und weise darauf hin,
   dass mit der Eröffnung eines Insolvenzverfahrens über das Vermögen des
   Arbeitnehmers besondere Regeln für Vollstreckungsmaßnahmen und für die
   Auszahlung gelten (§§ 89 und 287 InsO – für [JAHR] verifizieren). Triff in
   diesem Schritt keine Entscheidung über die Wirksamkeit; benenne die
   Weichenstellung und wer sie entscheidet.
9. Pflichten des Arbeitgebers als Drittschuldner zusammenstellen. Prüfe
   zuerst, ob eine Aufforderung des Gläubigers vorliegt; ohne sie besteht keine
   Erklärungspflicht (§ 840 Abs. 1 und Abs. 2 ZPO – für [JAHR] verifizieren).
   Ist keine Aufforderung ersichtlich, erzeuge den Entwurf nach Schritt 12
   nicht, sondern weise das als Klärungspunkt aus. Benenne
   getrennt: die Erklärungspflicht nach § 840 ZPO mit ihrem Inhalt nach den
   dortigen Nummern, die Pflicht zur Einbehaltung und Abführung ab dem
   maßgeblichen Zeitpunkt, die Pflicht zur laufenden Anpassung bei Änderung der
   Bezüge oder der Unterhaltspflichten, die Mitteilung bei Beendigung des
   Arbeitsverhältnisses und die Aufbewahrung der Unterlagen. Benenne ferner die
   Folge einer unterbliebenen oder unrichtigen Erklärung dem Grunde nach
   (§ 840 ZPO – Absatz und Satz benennen, für [JAHR] verifizieren), ohne
   Haftungsumfang oder Betrag zu beziffern.
10. Grenzen der Arbeitgeberpflichten benennen. Halte fest, was der Arbeitgeber
    NICHT tut: Auskünfte über den Arbeitnehmer, die über den Inhalt der
    Erklärung hinausgehen; Weitergabe von Daten Dritter; Beratung des
    Arbeitnehmers zu Vollstreckungsschutz, Pfändungsschutzkonto oder
    Insolvenzverfahren; Beurteilung der Wirksamkeit des Titels; Kündigung wegen
    der Pfändung. Weise darauf hin, dass Rechtsberatung des Arbeitnehmers dem
    Arbeitgeber und der Kanzlei nicht zusteht.
11. Fristen benennen, nicht berechnen. Berechne KEINE Fristen und nenne keine
    Fristlängen und keine Rechtsfolgen einer Versäumnis als feststehend. Liste
    stattdessen auf, WELCHE Fristen im Raum stehen – Abgabe der
    Drittschuldnererklärung nach § 840 ZPO, Beginn der Einbehaltung, Wirkung
    einer Vorpfändung, Rechtsbehelfe des Arbeitnehmers gegen den Beschluss –,
    jeweils mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne
    Datum und ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu
    berechnen und im Fristenprogramm zu erfassen."
12. Entwurf der Drittschuldnererklärung erzeugen. Erstelle den Entwurf
    strukturiert nach den Nummern des § 840 ZPO, in der Sie-Form, sachlich,
    ohne Wertung und ohne Rechtsansicht. Setze für jede Angabe, die aus der
    Abrechnung stammt, einen Platzhalter und KEINEN Betrag. Nimm eine Zeile für
    Ort, Datum und Unterschrift des Arbeitgebers auf sowie einen Hinweis, dass
    der Entwurf vor Absendung zu prüfen ist.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Eine Pfändung ist der Anlass dieses Prompts und KEIN Abbruchgrund. Auch
mehrere Pfändungen, eine Abtretung, eine Unterhaltspfändung oder eine hohe Zahl
von Gläubigern sind kein Abbruchgrund.
Einzelne Vorgänge aussteuern, Bearbeitung fortsetzen:
- Fehlt zu einer Pfändung das Zustellungsdatum oder der Zustellungsnachweis,
  weise sie als "Rang nicht bestimmbar – Nachweis anfordern" aus und bearbeite
  die übrigen weiter.
- Ist im Feld zum Insolvenzverfahren "ja" angegeben, weise diesen Vorgang als
  "Insolvenzbeschlag – Berufsträger vor Umsetzung" aus und setze die übrige
  Bearbeitung fort.
- Ist im Feld "Bereits geleistete Zahlungen an den Arbeitnehmer nach der
  Zustellung" der Wert "ja" angegeben, weise diesen Punkt als "möglicher
  Haftungssachverhalt – unverzüglich dem Berufsträger vorzulegen" gesondert aus
  und bearbeite die Zuordnung der Bezüge weiter.
Die gesamte Bearbeitung brichst du nur ab, wenn (a) die Angaben einen Klarnamen
einer natürlichen Person, eine Anschrift, eine Konto- oder IBAN-Angabe, ein
gerichtliches Aktenzeichen oder eine Beschreibung des Lebenssachverhalts
enthalten, aus dem die Forderung stammt (etwa Schilderung einer Straftat, einer
Erkrankung oder familiärer Umstände) – gib dann nur aus: "Angaben nicht
datensparsam – Bearbeitung abgebrochen, bitte maskierte Fassung nachreichen" –, oder (b) die Angaben ein
Straf-, Ermittlungs- oder Bußgeldverfahren gegen den Arbeitgeber wegen des
Vorenthaltens von Arbeitsentgelt erwähnen – gib dann nur aus: "Anzeichen für
einen Strafsachverhalt – Bearbeitung abgebrochen, Prüfung durch einen
Berufsträger außerhalb des KI-Werkzeugs."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab:
   eindeutig / vertretbare Varianten / nicht ohne weitere Angaben entscheidbar.
   Liste fehlende Angaben auf.
2. Ordne jede genannte Bezugsart zu. Eine nicht zugeordnete Bezugsart ist ein
   Mangel und wird am Ende gesondert ausgewiesen.
3. Formuliere jede Aussage zum Sachverhalt, die nicht in den Angaben steht,
   ausdrücklich als Vermutung.
4. Wiederhole am Ende in einem eigenen Satz, dass kein Betrag ermittelt wurde
   und die Berechnung im Abrechnungsprogramm erfolgt.
5. Führe alle genannten Fundstellen am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit und fehlende Angaben
2. Vorgangsübersicht: Dokument | Zustellung | Forderungsart | Gläubigerkürzel |
   Rang | Status
3. ZUORDNUNGSTABELLE der Bezüge: Nr. | Bezugsart | Kategorie |
   Rechtsgrundlage mit Zusatz | Bemerkung | offen (ja/nein)
4. Rangfolge mehrerer Pfändungen und Einordnung der Abtretung
5. Pflichten des Arbeitgebers, abhakbar mit ☐, mit Verantwortlichen
6. Grenzen: was der Arbeitgeber nicht tut
7. Fristarten, ohne Datum und ohne Dauer
8. (Entwurf Drittschuldnererklärung) – gegliedert nach den Nummern des
   § 840 ZPO, mit Platzhaltern statt Beträgen
9. Zu verifizierende Rechtsgrundlagen: Nr. | Fundstelle | wofür sie steht |
   geprüft von (leer)
10. Interne Notiz: was vor der Umsetzung zu klären ist
11. Was ich nicht sicher weiß
```

## Anwendung

1. Beschluss und Zustellungsnachweis zuerst beschaffen und das Zustellungsdatum aktenkundig machen. Rang, Beginn der Einbehaltung und Erklärungsfrist hängen an diesem einen Datum; alles andere ist nachrangig.
2. Prüfen, ob der Gläubiger die Drittschuldnererklärung verlangt hat; liegt die Aufforderung vor, die Frist sofort nach Eingang im Fristenprogramm erfassen – vor der fachlichen Bearbeitung, nicht danach.
3. Zuordnungstabelle mit den tatsächlich in der Abrechnung angelegten Lohnarten abgleichen und die Zuordnung im Abrechnungsprogramm hinterlegen. Die Tabelle ist die Brücke zwischen Norm und Lohnart; hier entsteht der Fehler oder er entsteht nicht.
4. Den pfändbaren Betrag im Abrechnungsprogramm ermitteln lassen, das Ergebnis ausdrucken und zur Akte nehmen. Kein Betrag aus der KI-Antwort und keine überschlägige Handrechnung.
5. Entwurf der Drittschuldnererklärung mit den Werten aus der Abrechnung vervollständigen, prüfen lassen und über den Arbeitgeber versenden; die Erklärung gibt der Arbeitgeber ab, nicht die Kanzlei aus eigenem Recht.
6. Wiedervorlage setzen für: Änderung der Bezüge, Änderung der Zahl der Unterhaltsberechtigten, Eingang weiterer Pfändungen, Beendigung des Arbeitsverhältnisses. Ergänzt Prompt 44 (Stichtagsplan Lohn) um den Zulieferweg für Pfändungsunterlagen.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person prüft die Zuordnung jeder Bezugsart, die Rangfolge und die Vollständigkeit der Drittschuldnererklärung anhand des Beschlusses nach. **Freigabe durch einen Berufsträger** vor jeder Erklärung gegenüber dem Vollstreckungsgericht, einer Behörde oder dem Gläubiger und vor jeder Auskunft an den Arbeitnehmer (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch.** Die Frist zur Abgabe der Drittschuldnererklärung wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Zustellungsnachweises nachgeprüft und abgezeichnet. Kein Datum aus der KI-Antwort (siehe Prompt 35).
- **Kein Betrag aus dem Modell.** Enthält die Antwort einen Betrag, eine Freigrenze, einen Prozentsatz oder eine Tabellenstufe, ist sie zu verwerfen. Der pfändbare Teil wird ausschließlich im Abrechnungsprogramm anhand der jeweils geltenden Pfändungsfreigrenzenbekanntmachung ermittelt und dort dokumentiert.
- **Zuordnung an der Lohnart prüfen, nicht am Namen.** Ob ein Bezug unter § 850a ZPO fällt, entscheidet sich nach seinem Charakter, nicht nach der Bezeichnung im Abrechnungsprogramm. Umbenannte oder gemischte Lohnarten sind die häufigste Fehlerquelle.
- **Rang nur nach belegter Zustellung.** Eine Rangfolge, die auf einem angenommenen oder aus dem Beschlussdatum abgeleiteten Zustellungsdatum beruht, ist unbrauchbar; fehlende Nachweise werden angefordert, nicht ersetzt.
- **Insolvenz und Abtretung nicht nebenbei erledigen.** Eröffnetes Insolvenzverfahren, laufende Abtretung an einen Treuhänder und arbeitsvertragliche Abtretungsverbote gehören vor der Umsetzung auf den Tisch des Berufsträgers.
- **Keine Rechtsberatung des Arbeitnehmers.** Fragen zu Vollstreckungsschutz, Pfändungsschutzkonto oder Restschuldbefreiung werden an eine Schuldnerberatung oder einen Rechtsanwalt verwiesen; die Kanzlei berät den Arbeitgeber.
- **Rechtsstand prüfen an:** §§ 829, 833, 840, 845, 850, 850a, 850b, 850c, 850d, 850e und 850f ZPO sowie § 400 BGB und §§ 89, 287 InsO im amtlichen Volltext (gesetze-im-internet.de), an der jeweils geltenden Pfändungsfreigrenzenbekanntmachung im Bundesgesetzblatt und an DATEV LEXinform.

## Varianten

- **Mehrere Pfändungen:** „Bearbeite mehrere Pfändungen desselben Arbeitnehmers in einer Tabelle und weise je Pfändung Rang, tragendes Zustellungsdatum und Status aus."
- **Behördliche Pfändung:** „Beschränke die Prüfung auf eine Pfändungsverfügung einer Behörde und weise die Unterschiede im Verfahrensweg gegenüber dem Beschluss des Vollstreckungsgerichts gesondert aus."
- **Arbeitgebermerkblatt:** „Erzeuge ein Merkblatt für den Arbeitgeber, Sie-Form, höchstens 400 Wörter: was er nach Zustellung sofort tut, was er unterlässt und wann er die Kanzlei einschaltet."
- **Beendigung des Arbeitsverhältnisses:** „Erzeuge eine Checkliste für den Fall, dass das Arbeitsverhältnis während einer laufenden Pfändung endet, einschließlich der Mitteilungen und der Behandlung noch offener Bezüge."
- **Arbeitsanweisung:** „Leite aus dem Vorgang eine Arbeitsanweisung für die Lohnbuchhaltung ab: Posteingang, Fristerfassung, Zuordnung, Freigabe, Wiedervorlage."
