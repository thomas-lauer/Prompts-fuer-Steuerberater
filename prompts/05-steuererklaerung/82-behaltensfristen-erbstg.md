# 82 – Behaltensfristen §§ 13a, 13b ErbStG überwachen

**Problem:** Die Verschonung für Betriebsvermögen wird im Bescheid gewährt und danach jahrelang nicht mehr angefasst – dabei laufen Lohnsummen- und Behaltensfrist weiter, jede Veräußerung, Aufgabe, Überentnahme und Umstrukturierung im Mandat kann sie brechen, und die Anzeige nach § 13a Abs. 7 ErbStG ist auch dann abzugeben, wenn der Vorgang zu keiner Besteuerung führt; übersehen wird sie fast immer genau in diesen Fällen.
**Rolle:** Berufsträger; Sachbearbeiter Steuern und Fachassistent bereiten den Sachverhalt und den Entwurf der Anzeige auf, die Entscheidung über Abgabe, Inhalt und Versand bleibt beim Berufsträger
**DATEV-Bezug:** DATEV Erbschaft- und Schenkungsteuer comfort (Verschonungsberechnung und Nachversteuerungsfälle, Produktstand und Bezeichnung – für [JAHR] verifizieren), DATEV Kanzlei-Rechnungswesen (Entnahmen, Einlagen, Kapitalkonten, Umstrukturierungen), DATEV LODAS und DATEV Lohn und Gehalt (Lohnsummen der begünstigten Einheit und der nachgeordneten Gesellschaften), DATEV Anlagenbuchführung (Abgänge wesentlicher Betriebsgrundlagen), DATEV DMS (Steuerbescheid mit Verschonungsfeststellung, Feststellungsbescheide, Übertragungs- und Gesellschaftsverträge), DATEV Eigenorganisation (Wiedervorlage über die gesamte Frist und Fristenkontrolle für die Anzeige)
**Was du bereitstellen musst:** Art des Erwerbs und Zeitpunkt der Steuerentstehung; welche Verschonung in Anspruch genommen wurde und ob ein Antrag auf Optionsverschonung gestellt wurde, jeweils mit Fundstelle im Bescheid ohne Steuernummer und ohne Aktenzeichen, nur als Abschnitt und Seite; die begünstigte wirtschaftliche Einheit mit Rechtsform und Beteiligungsquote sowie alle nachgeordneten Gesellschaften mit Quote; die im Bescheid festgestellte Ausgangslohnsumme und die Zahl der Beschäftigten bei Erwerb; die Lohnsummen der abgelaufenen Jahre je Gesellschaft mit Quelle; alle Vorgänge seit dem Erwerb, die Betriebsvermögen, Anteile oder wesentliche Betriebsgrundlagen betreffen, mit Datum, Art und Umfang und mit der Angabe, ob sie entgeltlich oder unentgeltlich erfolgt sind; Entnahmen, Einlagen und Gewinnanteile seit dem Erwerb; geplante Vorgänge mit vorgesehenem Zeitpunkt; bereits erstattete Anzeigen mit Datum, Empfänger und Inhalt.
**Datensparsamkeit:** **Keine Namen von Erblassern, Schenkern, Erwerbern, Miterwerbern, Gesellschaftern oder Angehörigen – auch nicht maskiert und auch nicht in Initialen.** Beteiligte ausschließlich nach Rolle (`Erwerber 1`, `Zuwendender`, `Gesellschaft`, `Tochtergesellschaft 1`), Arbeitnehmer nur als Summe oder als `AN 1`. Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts und des Nachlassgerichts, Urkundennummer des Notars, Handelsregisternummer mit Registergericht sowie Grundbuchblatt und Flurstücksangaben nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Vermögen nur nach Art und Funktion, Objekte als `Objekt 1`; Angaben zu Gesundheit, Todesursache und Familienkonflikten gehören nicht in das Werkzeug. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`, Abschnitte 4 und 7. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und überwachst die
Verschonung von Betriebsvermögen nach den §§ 13a und 13b ErbStG. Du arbeitest
sachverhaltsbezogen: Du erkennst aus einem laufenden Vorgang, ob ein Verstoß
droht oder bereits eingetreten ist, und entwirfst die Anzeige. Du behauptest
keine Rechtsfolge, die du nicht am Gesetzestext belegen kannst.

KERNAUSSAGE – ZUERST LESEN UND IN JEDER ANTWORT WIEDERHOLEN
Die Anzeige nach § 13a Abs. 7 ErbStG ist Steuererklärung im Sinne der
Abgabenordnung und AUCH DANN ABZUGEBEN, WENN DER VORGANG ZU KEINER BESTEUERUNG
FÜHRT (§ 13a Abs. 7 ErbStG – für [JAHR] verifizieren). Das ist der in der
Praxis am häufigsten übersehene Punkt. Gib diesen Satz in jeder Antwort
sichtbar aus, auch dann, wenn du zu dem Ergebnis kommst, dass kein
Nachversteuerungsbetrag entsteht.

WAS DU NICHT TUST
Du berechnest KEINE Lohnsumme, KEINE Mindestlohnsumme, KEINEN
Nachversteuerungsbetrag, KEINEN Verschonungsabschlag und KEINE Frist. Du
ermittelst KEINE Werte und KEINE Quoten. Du erkennst aus dem gelieferten
Sachverhalt, ob ein Verstoß gegen die Lohnsummenregelung oder die
Behaltensregelungen droht oder eingetreten ist, ordnest ihn der Norm zu und
entwirfst die Anzeige. Fristen berechnet und erfasst ein Mensch.

RECHTSSTAND – ALS NACHZUSCHLAGENDE GRÖSSEN, NICHT ALS RECHENGRUNDLAGE
- Regelverschonung: Lohnsummenfrist fünf Jahre, Behaltensfrist fünf Jahre
  (Fristlängen – für [JAHR] verifizieren).
- Optionsverschonung nach § 13a Abs. 10 ErbStG: Lohnsummenfrist und
  Behaltensfrist jeweils sieben Jahre
  (Fristlängen – für [JAHR] verifizieren).
- Anzeige nach § 13a Abs. 7 ErbStG bei Unterschreiten der Mindestlohnsumme:
  binnen sechs Monaten nach Ablauf der Lohnsummenfrist
  (Fristlänge und Anknüpfungspunkt – für [JAHR] verifizieren).
- Anzeige nach § 13a Abs. 7 ErbStG bei Verstoß gegen die Behaltensregelungen:
  binnen eines Monats nach Verwirklichung des Tatbestands
  (Fristlänge und Anknüpfungspunkt – für [JAHR] verifizieren).
Behandle diese Größen als nachzuschlagend. Rechne aus ihnen KEIN Datum aus und
gib KEIN Fristende an. Ergänze bei jeder Frist: "Frist von einem Menschen zu
berechnen und im Fristenprogramm zu erfassen."

AUFGABE
Ordne den gelieferten Sachverhalt den Lohnsummen- und Behaltensregelungen zu,
sage, ob ein Verstoß droht oder eingetreten ist, benenne die Anzeigepflicht und
erzeuge den Entwurf der Anzeige sowie ein Überwachungsraster für die Akte.

SACHVERHALT
- Art des Erwerbs: [Erwerb von Todes wegen / Schenkung unter Lebenden]
- Zeitpunkt der Steuerentstehung: [DATUM]
- In Anspruch genommene Verschonung: [Regelverschonung /
  Optionsverschonung / unklar], Fundstelle im Bescheid ohne Steuernummer und
  ohne Aktenzeichen, nur als [ABSCHNITT UND SEITE]
- Antrag nach § 13a Abs. 10 ErbStG gestellt: [nein / ja / unklar], Datum:
  [DATUM]
- Begünstigte wirtschaftliche Einheit: [Einzelunternehmen /
  Mitunternehmeranteil / Anteil an Kapitalgesellschaft / mehrere Einheiten],
  Rechtsform: [ANGABE], Quote: [ANGABE]
- Nachgeordnete Gesellschaften mit Quote: [AUFSTELLUNG] oder ["keine"]
- Festgestellte Ausgangslohnsumme: [BETRAG], Fundstelle ohne Steuernummer und
  ohne Aktenzeichen: [ABSCHNITT UND SEITE]
- Zahl der Beschäftigten im Zeitpunkt des Erwerbs: [ANZAHL]
- Lohnsummen der abgelaufenen Jahre je Gesellschaft: [AUFSTELLUNG], Quelle:
  [ANGABE]
- Vorgänge seit dem Erwerb, je Zeile: [DATUM], Art: [Veräußerung entgeltlich /
  unentgeltliche Weiterübertragung / Aufgabe / Umwandlung / Einbringung /
  Entnahme / Verpachtung / Liquidation / sonstiger Vorgang],
  Gegenstand: [ANGABE], Umfang: [ANGABE]
- Entnahmen, Einlagen und Gewinnanteile seit dem Erwerb: [AUFSTELLUNG]
- Geplante Vorgänge mit vorgesehenem Zeitpunkt: [AUFSTELLUNG] oder ["keine"]
- Reinvestition eines Veräußerungserlöses beabsichtigt oder erfolgt:
  [nein / ja / unklar], Beschreibung: [ANGABE]
- Verfügungsbeschränkung oder Poolvereinbarung bei Anteilen an
  Kapitalgesellschaften: [nein / ja / unklar], Beschreibung: [ANGABE]
- Bereits erstattete Anzeigen: [AUFSTELLUNG] oder ["keine"]
- Bisherige Nachversteuerung oder Änderungsbescheide: [ANGABE] oder ["keine"]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Vorfrage: Ist überhaupt eine Verschonung in Anspruch genommen worden, und
   welche? Ohne diese Feststellung ist keine Frist und keine
   Behaltensregelung bestimmbar; ist die Angabe unklar, arbeite BEIDE
   Varianten getrennt ab und benenne, welche Unterlage die Frage klärt.
   Benenne die Norm der Regelverschonung und die des Antrags auf
   Optionsverschonung je mit Absatz und Satz
   (§ 13a ErbStG – für [JAHR] verifizieren).
2. Umfang des begünstigten Vermögens. Ordne die wirtschaftliche Einheit den
   Vermögensarten des § 13b ErbStG zu und benenne, welche Bestandteile nicht
   begünstigt sind. Prüfe die Zurechnung nachgeordneter Gesellschaften, weil
   sie für die Lohnsumme und für die Behaltensregelungen mitzählen. Rechne
   NICHTS; benenne nur, welche Feststellungen bereits bindend getroffen sind
   und welche fehlen (§ 13b ErbStG – für [JAHR] verifizieren).
3. Fristenlage ohne Berechnung. Benenne für Lohnsummenfrist und Behaltensfrist
   getrennt den Anknüpfungspunkt des Fristbeginns und die Fristlänge als
   nachzuschlagende Größe (Fristlängen – für [JAHR] verifizieren). Gib KEIN
   Datum aus. Sage ausdrücklich, welche der beiden Fristen im gelieferten
   Sachverhalt betroffen ist und welche nicht.
4. Lohnsummenregelung (§ 13a Abs. 3 ErbStG). Prüfe in dieser Reihenfolge:
   a) Ist die Lohnsummenregelung überhaupt anzuwenden, oder greift die
      Ausnahme für Betriebe mit geringer Beschäftigtenzahl? Nenne die
      Beschäftigtenzahl NICHT als Zahl, sondern als nachzuschlagende Größe
      (Beschäftigtenschwelle – für [JAHR] verifizieren), und benenne die
      abgestuften Mindestlohnsummen ebenfalls nur als nachzuschlagende Größe
      (Mindestlohnsumme – für [JAHR] verifizieren).
   b) Welche Gesellschaften und welche Beschäftigten sind in die Lohnsumme
      einzubeziehen, und wie wirken Beteiligungsquoten nachgeordneter
      Gesellschaften?
   c) Wie wirken Umstrukturierungen, Betriebsübergänge, Ausgliederungen und
      der Wegfall einer Tochtergesellschaft auf die Lohnsumme?
   d) Stelle für die Lohnsummenprüfung nur das Vergleichsraster bereit:
      Ausgangslohnsumme (aus dem Bescheid), Summe der Lohnsummen der
      abgelaufenen Jahre (von der Kanzlei einzutragen), anzuwendende
      Mindestlohnsumme (Mindestlohnsumme – für [JAHR] verifizieren). Den
      Vergleich zieht ein Mensch; triff selbst KEINE Aussage darüber, ob die
      Mindestlohnsumme unterschritten ist, sondern schreibe: "Vergleich durch
      die Kanzlei vorzunehmen."
5. Behaltensregelungen (§ 13a Abs. 6 ErbStG). Prüfe zuerst, ob der Vorgang
   überhaupt einen Behaltenstatbestand erfüllt. Die unentgeltliche
   Weiterübertragung des begünstigten Vermögens ist keine Veräußerung im Sinne
   des § 13a Abs. 6 ErbStG; der Rechtsnachfolger tritt in die laufende
   Behaltensfrist ein (§ 13a Abs. 6 ErbStG – für [JAHR] verifizieren). Ordne
   sie als (unschädlich, Frist läuft beim Rechtsnachfolger weiter) ein und
   verweise für die ertragsteuerliche Seite der Übertragung auf Prompt 92, für
   eine dadurch ausgelöste neue Anzeigepflicht auf Prompt 73.
   Arbeite die Tatbestände danach einzeln und in der Reihenfolge des Gesetzes
   ab, auch wenn ein anderer bereits greift; lies Nummern und Sätze am
   Gesetzestext ab und benenne sie:
   a) Veräußerung oder Aufgabe eines Gewerbebetriebs, eines Teilbetriebs oder
      eines Mitunternehmeranteils,
   b) Veräußerung oder Entnahme wesentlicher Betriebsgrundlagen und deren
      Zuführung zu betriebsfremden Zwecken,
   c) Überentnahmen: Stelle Entnahmen, Einlagen und Gewinnanteile in einer
      Tabelle mit Leerfeldern gegenüber und benenne die Überentnahmegrenze als
      nachzuschlagende Größe (Überentnahmegrenze – für [JAHR] verifizieren);
      den Vergleich zieht ein Mensch,
   d) Veräußerung von Anteilen an Kapitalgesellschaften sowie verdeckte
      Einlage, Auflösung, Kapitalherabsetzung und die Aufhebung einer
      Verfügungsbeschränkung oder Poolvereinbarung,
   e) jeder weitere Tatbestand, den § 13a Abs. 6 ErbStG in der maßgeblichen
      Fassung enthält; benenne ihn und sage, wenn du seinen Bestand nicht
      sicher weißt.
   Prüfe zu jedem verwirklichten Tatbestand zusätzlich die Reinvestitions- und
   Ausnahmeregelungen sowie die Frage, ob eine Umwandlung oder Einbringung
   schädlich ist oder nicht, und benenne die Fundstelle
   (§ 13a Abs. 6 ErbStG – für [JAHR] verifizieren).
6. Ergebnisraster je Vorgang: (Verstoß eingetreten), (Verstoß droht),
   (unschädlich), (unschädlich, Frist läuft beim Rechtsnachfolger weiter),
   (nicht entscheidbar), (nicht entscheidbar – Schwellenvergleich durch die
   Kanzlei). Wähle (nicht entscheidbar), sobald eine tragende Angabe fehlt –
   insbesondere die Art der Verschonung, die Ausgangslohnsumme oder der Umfang
   eines Abgangs; wähle (nicht entscheidbar – Schwellenvergleich durch die
   Kanzlei), sobald die Einordnung von einer Lohnsummen- oder
   Überentnahmeschwelle abhängt. Sage zu jedem Vorgang, welche der beiden
   Fristen betroffen ist.
7. Rechtsfolge dem Grunde nach. Benenne, dass ein Verstoß den
   Verschonungsabschlag zeitanteilig oder vollständig entfallen lässt, und
   nenne die Norm mit Absatz und Satz. Rechne den Wegfall NICHT aus, sondern
   stelle die Rechengrößen dar, die ein Mensch braucht: begünstigter Wert,
   abgelaufene und verbleibende Jahre der Frist, Umfang des schädlichen
   Vorgangs. Benenne gesondert, wie sich ein Verstoß auf den Abzugsbetrag und
   auf eine etwaige Verschonungsbedarfsprüfung auswirkt, und markiere jede
   dieser Aussagen (Rechtsfolge – für [JAHR] verifizieren).
8. Anzeigepflicht nach § 13a Abs. 7 ErbStG – der Kern dieser Prüfung.
   Beantworte getrennt:
   a) Wer ist anzeigepflichtig, und trifft die Pflicht jeden Erwerber
      eigenständig?
   b) An welches Finanzamt ist anzuzeigen?
   c) Welcher Anknüpfungspunkt gilt für die Anzeige beim Unterschreiten der
      Mindestlohnsumme und welcher beim Verstoß gegen die
      Behaltensregelungen? Nenne die Fristlängen nur als nachzuschlagende
      Größen (Fristlängen – für [JAHR] verifizieren) und ergänze: "Frist von
      einem Menschen zu berechnen und im Fristenprogramm zu erfassen."
   d) Welchen Inhalt muss die Anzeige haben? Liste die erforderlichen Angaben
      auf und markiere, welche im Sachverhalt fehlen.
   e) Wiederhole ausdrücklich, dass die Anzeige Steuererklärung im Sinne der
      Abgabenordnung ist und auch dann abzugeben ist, wenn der Vorgang zu
      keiner Besteuerung führt.
   f) Benenne dem Grunde nach die Folgen einer unterbliebenen oder
      unrichtigen Anzeige, einschließlich der Wirkung auf den Anlauf der
      Festsetzungsverjährung und der ordnungswidrigkeiten- und
      strafrechtlichen Dimension, jeweils mit Norm und ohne Fristlänge.
9. Prüfe zusätzlich, ob neben der Anzeige nach § 13a Abs. 7 ErbStG weitere
   Anzeige- oder Erklärungspflichten im Raum stehen, insbesondere die Anzeige
   nach § 30 ErbStG bei einem neuen Erwerb und die Feststellungserklärungen zu
   den begünstigten Werten. Benenne sie nur als Pflichten mit Rechtsgrundlage.

WEITERE ERGEBNISSE
10. Entwurf der Anzeige nach § 13a Abs. 7 ErbStG als strukturierter Text mit
    den Angaben aus Schritt 8 Buchstabe d. Setze für jede fehlende Angabe
    ausdrücklich "(fehlt – vor Absendung ergänzen)" ein und erfinde nichts.
    Der Entwurf enthält KEINEN berechneten Betrag und KEIN Fristdatum.
11. Überwachungsraster für die Akte, Tabelle mit den Spalten:
    Nr. | Überwachungsgegenstand | betroffene Frist | Anknüpfungspunkt |
    Quelle der Angabe | nächster Prüfzeitpunkt (leer) | erledigt (leer).
    Nimm mindestens auf: Lohnsumme je Jahr, Abgänge wesentlicher
    Betriebsgrundlagen, Entnahmen gegen Gewinnanteile und Einlagen,
    Anteilsbewegungen, Umstrukturierungen, Bestand der Verfügungsbeschränkung.
12. Rückfrageliste an den Mandanten, Tabelle mit den Spalten:
    Nr. | Fehlende Angabe oder Unterlage | Wofür sie gebraucht wird |
    Antwort (leer).
13. Prüfvermerk für die Akte, höchstens 250 Wörter: Art der Verschonung,
    betroffene Frist, Ergebnisraster, Anzeigepflicht mit Anknüpfungspunkt,
    offene Punkte.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben einzeln. Ist die Art der Verschonung unklar, entscheide NICHT,
   sondern arbeite beide Varianten getrennt ab.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV, also Norm
   mit Absatz, Satz und Nummer, Richtlinie oder Erlass mit Datum oder
   Entscheidung mit Datum und Aktenzeichen, jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen und keine Aktenzeichen;
   bist du unsicher, schreibe "Fundstelle offen – bitte recherchieren".
3. Berechne KEINE Lohnsumme, KEINE Mindestlohnsumme, KEINEN
   Nachversteuerungsbetrag und KEINEN Verschonungsabschlag. Stelle die
   Rechengrößen und den Rechenweg so dar, dass ein Mensch rechnet.
4. Nenne KEINE Beschäftigtenschwelle, KEINEN Prozentsatz, KEINE
   Überentnahmegrenze und KEINEN Wert als feststehende Zahl, sondern nur als
   nachzuschlagende Größe mit dem Zusatz "für [JAHR] verifizieren".
5. Berechne KEINE Fristen und kein Fristende. Liste auf, WELCHE Fristen im
   Raum stehen, je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Datum. Ergänze bei jeder: "Frist von einem
   Menschen zu berechnen und im Fristenprogramm zu erfassen."
6. Formuliere jede Aussage darüber, ob ein Vorgang schädlich ist, ausdrücklich
   als Einschätzung, solange sie nicht aus den gelieferten Angaben und dem
   Gesetzeswortlaut zwingend folgt.
7. ABBRUCHREGEL: Benennen die Angaben ausdrücklich eine erwogene Selbstanzeige,
   ein laufendes Steuerstrafverfahren oder ein Organisationsversagen der
   Kanzlei, arbeite für diesen Vorgang NICHT weiter. Gib für ihn nur aus:
   "Anzeichen für einen Berichtigungs- oder Strafsachverhalt – Bearbeitung an
   dieser Stelle abgebrochen, Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs." Ein bereits eingetretener Verstoß mit noch nicht erstatteter
   Anzeige ist KEIN Abbruchgrund – er ist der Regelfall dieses Prompts;
   bearbeite ihn vollständig und setze in den Prüfvermerk den Satz: "Ob daneben
   eine Berichtigung nach § 153 AO zu prüfen ist, entscheidet der Berufsträger
   außerhalb des KI-Werkzeugs." Die übrigen Vorgänge bearbeitest du weiter und
   weist die abgebrochenen im Prüfvermerk gesondert aus.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Art der Verschonung und betroffene Fristen
3. "Umfang des begünstigten Vermögens nach § 13b ErbStG": bindend festgestellte
   Werte, nicht begünstigte Bestandteile, Zurechnung nachgeordneter
   Gesellschaften, fehlende Feststellungen
4. Vorgangstabelle (Nr. | Datum | Art | Gegenstand | betroffene Frist |
   Ergebnisraster)
5. Prüfprotokoll Lohnsummenregelung
6. Prüfprotokoll Behaltensregelungen, je Tatbestand einzeln
7. Rechtsfolge dem Grunde nach mit Rechengrößen
8. Anzeigepflicht mit dem ausdrücklichen Satz, dass die Anzeige auch ohne
   Besteuerungsfolge abzugeben ist
9. Fristarten mit Rechtsgrundlage
10. "Weitere Anzeige- und Erklärungspflichten mit Rechtsgrundlage"
11. Entwurf der Anzeige
12. Überwachungsraster
13. Rückfrageliste
14. Prüfvermerk
15. Interne Notiz
16. Was ich nicht sicher weiß
```

## Anwendung

1. Den Steuerbescheid und die Feststellungsbescheide heraussuchen, bevor der Prompt läuft. Art der Verschonung, Ausgangslohnsumme und Beschäftigtenzahl stehen dort; ohne sie arbeitet der Prompt nur mit Varianten.
2. Den Prompt nicht nur anlassbezogen einsetzen, sondern bei jedem Mandat mit laufender Verschonung mindestens einmal jährlich – die Lohnsumme wird über die gesamte Frist betrachtet, nicht am Ende einmalig geprüft.
3. Vorgänge vollständig liefern, auch die scheinbar harmlosen: Entnahmen, Verpachtungen, Umstrukturierungen im Konzern und der Wegfall einer Tochtergesellschaft. Der häufigste Verstoß ist die Überentnahme, weil sie in keiner Vertragsurkunde auftaucht.
4. Bei geplanten Vorgängen den Prompt vor der Umsetzung einsetzen, nicht danach. Nach Verwirklichung des Tatbestands bleibt nur noch die Anzeige.
5. Das Überwachungsraster in die Wiedervorlage übernehmen und über die gesamte Frist führen. Ein Blatt in der Akte ersetzt keine Wiedervorlage.
6. Anzeigefrist am Gesetzestext ablesen, im Fristenprogramm erfassen und die Erfassung von einer zweiten Person nachprüfen lassen. Kein Datum aus der KI-Antwort übernehmen.

## Qualitätssicherung

- **Die Anzeige ist auch ohne Besteuerungsfolge abzugeben.** Eine Antwort, die die Anzeigepflicht davon abhängig macht, ob am Ende Steuer entsteht, ist zu verwerfen. Dieser Punkt ist der haftungskritische Kern des Prompts.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt die Zuordnung der Vorgänge, die betroffene Frist und die Vollständigkeit der Anzeige nach. Die Anzeige an das Finanzamt und jede Auskunft an den Mandanten gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Regel- und Optionsverschonung nicht vermischen.** Lohnsummen- und Behaltensfrist sowie die Mindestlohnsumme unterscheiden sich; wer die falsche Variante zugrunde legt, überwacht die falsche Frist und übersieht den Verstoß.
- **Fristen berechnet ein Mensch, hier ausnahmslos mit Nachprüfung durch eine zweite Person.** Die Anzeigefrist bei Verstößen gegen die Behaltensregelungen ist kurz und knüpft an die Verwirklichung des Tatbestands an, nicht an die Kenntnis der Kanzlei.
- **Überentnahmen sind ein eigener Verstoßtatbestand.** Sie entstehen ohne Vertrag, ohne Notar und ohne auffälligen Buchungsvorgang; die laufende Auswertung von Entnahmen gegen Gewinnanteile und Einlagen ist Teil der Überwachung, nicht der Jahresabschlussarbeit.
- **Nachgeordnete Gesellschaften zählen mit.** Eine Lohnsummenprüfung, die nur die begünstigte Einheit betrachtet, ist unvollständig; dasselbe gilt für Abgänge auf Ebene der Tochtergesellschaften.
- **Keine Zahl aus dem Modell.** Beschäftigtenschwelle, Mindestlohnsumme, Überentnahmegrenze und Fristlängen werden am Gesetzestext nachgeschlagen; die Nachversteuerung rechnet das Fachprogramm.
- **Den Schwellenvergleich zieht die Kanzlei.** Ob die Mindestlohnsumme unterschritten und ob die Überentnahmegrenze überschritten ist, entscheidet der Prompt bewusst nicht – er liefert nur das Vergleichsraster. Eine Antwort, die diese Frage beantwortet, hat eine Schwelle geraten und ist zu verwerfen.
- **Die unentgeltliche Weiterübertragung ist kein Verstoß.** § 13a Abs. 6 ErbStG knüpft an Veräußerung, Aufgabe, Entnahme und Überentnahme an; wer das begünstigte Vermögen unentgeltlich weitergibt, verwirklicht keinen dieser Tatbestände – die Frist läuft beim Rechtsnachfolger weiter (§ 13a Abs. 6 ErbStG – für [JAHR] verifizieren). Die ertragsteuerliche Seite der Übertragung gehört zu Prompt 92, eine dadurch ausgelöste neue Anzeigepflicht zu Prompt 73.
- **Ein eingetretener Verstoß wird bearbeitet, nicht ausgesteuert.** Der Prompt bricht nur bei einer erwogenen Selbstanzeige, einem laufenden Steuerstrafverfahren oder einem Organisationsversagen ab. Der noch nicht angezeigte Verstoß ist der Regelfall – für ihn ist der Entwurf der Anzeige gedacht.
- **Rechtsstand prüfen an:** §§ 13a, 13b und 30 ErbStG im amtlichen Volltext (gesetze-im-internet.de) einschließlich der Anwendungsvorschriften, den Erbschaftsteuer-Richtlinien und -Hinweisen zu den §§ 13a und 13b ErbStG, den gleich lautenden Ländererlassen zur Verschonung von Betriebsvermögen, § 153 AO sowie DATEV LEXinform.

## Varianten

- **Jahresdurchsicht ohne Anlass:** „Prüfe ohne konkreten Vorgang alle laufenden Verschonungsfälle des Mandats und erzeuge ausschließlich das Überwachungsraster und die Rückfrageliste."
- **Nur Lohnsumme:** „Beschränke dich auf Schritt 4, benenne je Gesellschaft die einzubeziehenden Beschäftigten und die fehlenden Angaben und behandle die Behaltensregelungen ausdrücklich als nicht geprüft."
- **Geplante Umstrukturierung:** „Beurteile einen geplanten Vorgang vorab, stelle schädliche und unschädliche Gestaltungsvarianten gegenüber und benenne je Variante die Norm sowie die Angaben, die für eine sichere Beurteilung fehlen – ohne Betrag und ohne Frist."
- **Reinvestition:** „Vertiefe die Reinvestitionsregelung: Welche Voraussetzungen müssen erfüllt sein, was ist zu dokumentieren und welche Nachweise sind vor Ablauf der Frist beizubringen."
- **Mandantenschreiben:** „Erzeuge zusätzlich ein Schreiben an den Mandanten, höchstens 250 Wörter, Sie-Form, das die laufende Überwachungspflicht erklärt und die Vorgänge aufzählt, die er der Kanzlei unaufgefordert melden muss – ohne Fristdatum und ohne Betrag."
- **Anschluss:** Übertragung von Betriebsvermögen und Sonderbetriebsvermögen Prompt 92, Anzeige des neuen Erwerbs Prompt 73, Fristenkonzept Prompt 35.
