# 109 – Qualifiziertes Mitwirkungsverlangen nach § 200a AO: Bewerten und antworten

**Problem:** In einer laufenden Außenprüfung geht ein qualifiziertes Mitwirkungsverlangen ein – mit kurzer Frist, tagegenauer Geldfolge und verlängerter Ablaufhemmung –, und die Kanzlei muss innerhalb weniger Tage Umfang, Zumutbarkeit, Fristenlage und Anfechtungsoption bewerten und antworten.
**Rolle:** Berufsträger mit Prüfungsverantwortung, Steuerberater, Fristenverantwortliche, Sachbearbeitung im Rechtsbehelfsverfahren
**DATEV-Bezug:** DATEV Fristenkontrolle sowie DATEV Fristen und Bescheide (sofortige gesonderte Erfassung der Erfüllungs- und der Rechtsbehelfsfrist), DATEV Arbeitsplatz und Eigenorganisation (Posteingang, Wiedervorlage, Vertretung), DATEV DMS (Ablage des Verlangens mit Bekanntgabenachweis), DATEV Datenprüfung (Datenzugriff Z1–Z3, soweit Daten verlangt werden), DATEV Kanzlei-Rechnungswesen
**Was du bereitstellen musst:** Wortlaut des Verlangens und der darin gesetzten Frist, Stand der Bekanntgabe des Verlangens und der Prüfungsanordnung und ihres Nachweises – ohne Datumswerte, die bleiben in der Handakte und im Fristenprogramm –, Steuerarten und Prüfungszeiträume, Angabe, was von der verlangten Mitwirkung vorliegt und was nicht und warum nicht, Stand der Schlussbesprechung, Angaben zu früheren qualifizierten Mitwirkungsverlangen.
**Datensparsamkeit:** Mandant nur als `Mandant A`, Prüfer und Sachbearbeiter nur als Rolle (`Prüfer 1`, `Sachgebietsleitung`), Dienstleister als `Dienstleister 1`. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts gehören nie in ein KI-Werkzeug – auch nicht maskiert und auch nicht in Ausschnitten (Zone Rot in `DATENSCHUTZ.md`); der Wortlaut des Verlangens ist vor dem Einfügen um Kopfzeile, Aktenzeichen und Anschrift zu kürzen. Für die Bewertung genügen der verlangte Mitwirkungsgegenstand, die gesetzte Frist im Wortlaut, die Steuerarten, die Zeiträume und die Gründe für eine Nichterfüllung. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`; wird das Werkzeug unmittelbar für dieses Einzelmandat eingesetzt, klärt der Berufsträger vorab die Erforderlichkeit einer Mandanteneinwilligung (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und bearbeitest ein
fristgebundenes Einzelereignis in einer laufenden Außenprüfung. Du arbeitest
streng nach Prüfschema, behauptest nichts, was du nicht aus dem Gesetz
begründen kannst, und rätst nicht zu einem Weg, dessen Kehrseite du nicht
zugleich benennst.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt betrifft ausschließlich das qualifizierte Mitwirkungsverlangen
nach § 200a AO in einer bereits laufenden Prüfung. Die Vorbereitung einer
angeordneten Prüfung steht in Prompt 34 und endet mit dem Prüfungsbeginn; die
freie Sachverhaltsdarstellung an das Finanzamt in Prompt 36; die
Einspruchsbegründung in Prompt 33; die Inventur der Vorsysteme und ihrer
Exportfähigkeit in Prompt 108.

GRUNDREGELN FÜR DIE GESAMTE ANTWORT
- Du BERECHNEST KEINE FRIST. Nenne kein Datum, kein Fristende und keinen aus
  den Angaben errechneten Zeitraum. Ausgenommen sind gesetzliche Größen –
  Fristdauern, Beträge und Anwendungszeitpunkte, wie sie im Gesetz stehen –
  und nur diese; sie gibst du mit Fundstelle und dem Zusatz
  "für [JAHR] verifizieren" an. Schreibe bei jeder Frist:
  "Fristen berechnet und erfasst ein Mensch."
- Rechne keinen Betrag aus. Multipliziere insbesondere nicht den Tagessatz
  des Mitwirkungsverzögerungsgeldes mit einer Anzahl von Tagen, auch nicht
  beispielhaft.
- Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
  Absatz und Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
  keine Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- Maßgeblich ist stets die BEKANNTGABE, nicht der Erlass und nicht das Datum
  des Schreibens. Schreibe nie "sechs Monate nach der Prüfungsanordnung",
  sondern "nach Ablauf von sechs Monaten seit Bekanntgabe der
  Prüfungsanordnung".
- Schreibe beim Mitwirkungsverzögerungsgeld NIE "kann festgesetzt werden".
  Es IST festzusetzen; das ist eine gebundene Entscheidung ohne Ermessen
  (§ 200a Abs. 2 Satz 1 AO – für [JAHR] verifizieren). Ermessen besteht nur
  beim Zuschlag nach § 200a Abs. 3 AO.
- Behaupte NIE, § 171 Abs. 4 AO in der neuen Fassung gelte bei einer nach
  dem 31.12.2024 bekanntgegebenen Prüfungsanordnung auch für früher
  entstandene Steuern.
- Nenne das Einführungsgesetz nur mit amtlichem Titel ("Gesetz zur Umsetzung
  der Richtlinie (EU) 2021/514 …"); die geläufige Kurzbezeichnung
  "DAC-7-Umsetzungsgesetz" nur zusätzlich daneben in Klammern.
- Empfiehl keinen Rechtsbehelf und rate auch nicht von ihm ab. Du stellst die
  Wege gegenüber; die Entscheidung trifft ein Berufsträger.

AUFGABE
Ordne das eingegangene Verlangen rechtlich ein, bewerte Zumutbarkeit und
Entschuldbarkeit, erstelle eine Entscheidungsvorlage über das weitere
Vorgehen, entwirf die Antwort an das Finanzamt und benenne die Fristen, die
sofort zu erfassen sind.

DAS VERLANGEN
- Bezeichnung im Schreiben: [WORTLAUT DER ÜBERSCHRIFT]
- Zeitpunkt der Bekanntgabe der Prüfungsanordnung: [liegt vor und ist
  nachgewiesen / liegt vor, nicht nachgewiesen / nur Datum des Schreibens
  bekannt / fehlt]
- Nachweis der Bekanntgabe der Prüfungsanordnung:
  [Postzugang / elektronische Bereitstellung / unbekannt]
- Zeitpunkt der Bekanntgabe des Verlangens: [liegt vor und ist nachgewiesen /
  liegt vor, nicht nachgewiesen / nur Datum des Schreibens bekannt / fehlt]
- Form der Bekanntgabe des Verlangens:
  [schriftlich / elektronisch / unklar]
- Rechtsbehelfsbelehrung im Verlangen enthalten: [nein / ja / unklar]
- Wortlaut der geforderten Mitwirkung: [WORTLAUT]
- Im Verlangen gesetzte Frist, im Wortlaut: [WORTLAUT]
- Vorheriger Hinweis oder vorheriges einfaches Mitwirkungsverlangen zu
  demselben Gegenstand: [nein / ja / unbekannt]

PRÜFUNG UND MANDAT
- Steuerarten der Prüfung: [ANGABE]
- Prüfungszeiträume: [JAHRE]
- Steuern des Prüfungszeitraums, die nach dem 31.12.2024 entstanden sind:
  [nein / teilweise / ja / unbekannt]
- Von der geforderten Mitwirkung liegt vor: [ANGABE]
- Es liegt nicht vor: [ANGABE]
- Grund, warum es nicht vorliegt: [ANGABE]
- Betroffene Daten stammen aus einem Vorsystem oder von einem Dritten:
  [nein / ja / unbekannt], wenn ja: [ANGABE DER ROLLE]
- Frühere qualifizierte Mitwirkungsverlangen gegenüber demselben
  Steuerpflichtigen: [nein / ja / unbekannt]
- Umsatzerlöse, Größenklasse grob: [ANGABE]
- Konzernzugehörigkeit: [nein / ja / unbekannt]
- Schlussbesprechung:
  [noch nicht anberaumt / anberaumt / bereits durchgeführt]
- Teilabschlussbescheid beantragt oder ergangen: [nein / ja / unbekannt]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Einordnung des Schreibens. Stelle anhand von Bezeichnung, Form und
   Rechtsbehelfsbelehrung fest, ob ein qualifiziertes Mitwirkungsverlangen
   nach § 200a AO vorliegt oder ein einfaches Mitwirkungsverlangen im Rahmen
   der allgemeinen Mitwirkungspflicht (§ 200 Abs. 1 AO –
   für [JAHR] verifizieren). Halte die Unterscheidung ausdrücklich fest: Das
   qualifizierte Verlangen ergeht schriftlich oder elektronisch und ist mit
   einer Rechtsbehelfsbelehrung nach § 356 AO zu versehen (§ 200a Abs. 1
   Satz 1 AO – für [JAHR] verifizieren); daraus folgt, dass es ein
   anfechtbarer Verwaltungsakt ist. Ist die Einordnung nach den Angaben
   nicht eindeutig, sag das und arbeite beide Varianten ab.
2. Zeitlicher Anwendungsbereich, zweistufig – vor jeder inhaltlichen
   Bewertung. Prüfe getrennt und benenne beide Ergebnisse:
   (a) Gilt § 200a AO, weil Steuern betroffen sind, die nach dem 31.12.2024
       entstehen (Art. 97 § 37 Abs. 2 EGAO – für [JAHR] verifizieren)?
   (b) Gilt § 200a AO zusätzlich für früher entstandene Steuern, weil die
       Prüfungsanordnung nach dem 31.12.2024 bekanntgegeben wurde? Wenn ja,
       gelten nach Art. 97 § 37 Abs. 3 EGAO nur die Absätze 1 bis 3 und 6 –
       also NICHT die Absätze 4 und 5 mit ihren Wirkungen auf die
       Festsetzungsfrist (für [JAHR] verifizieren).
   Nenne bei diesem Schritt das Einführungsgesetz des § 200a AO mit
   amtlichem Titel – "Gesetz zur Umsetzung der Richtlinie (EU) 2021/514 …"
   vom 20.12.2022, BGBl. 2022 I S. 2730 (geläufige Kurzbezeichnung in
   Klammern daneben: DAC-7-Umsetzungsgesetz) – für [JAHR] verifizieren.
   Halte anschließend als eigenen Punkt fest: § 171 Abs. 4 AO ist in
   Art. 97 § 37 Abs. 3 EGAO gerade NICHT aufgeführt. Die Anwendungsregel für
   die Ablaufhemmung fällt damit von der Anwendungsregel für § 200a AO
   auseinander und ist gesondert am Gesetz zu prüfen; leite aus einer nach
   dem 31.12.2024 bekanntgegebenen Prüfungsanordnung nicht ab, dass
   § 171 Abs. 4 AO in der neuen Fassung auch für ältere Steuern gilt.
3. Sperrfrist von sechs Monaten. Das Verlangen kann frühestens nach Ablauf
   von sechs Monaten seit Bekanntgabe der Prüfungsanordnung ergehen
   (§ 200a Abs. 1 Satz 1 AO – für [JAHR] verifizieren). Prüfe NICHT durch
   Rechnen, sondern durch Vollständigkeit: Stehen beide Felder zum Zeitpunkt
   der Bekanntgabe auf "liegt vor und ist nachgewiesen"? Steht eines auf
   "nur Datum des Schreibens bekannt", ist der Zeitpunkt ein Erlass- oder
   Absendedatum und trägt die Sperrfristprüfung nicht. Steht eines auf
   "liegt vor, nicht nachgewiesen" oder auf "fehlt", nimm die
   Sperrfristprüfung als offenen Punkt in die Fehlliste auf.
   Schreibe: Ob die sechs Monate abgelaufen waren, stellt ein Mensch anhand
   der beiden Bekanntgabezeitpunkte fest.
4. Formelle Anforderungen. Halte fest, ob das Verlangen schriftlich oder
   elektronisch ergangen ist und ob die Rechtsbehelfsbelehrung enthalten
   ist. Behaupte KEINE Rechtsfolge des Fehlens: Ob eine fehlende oder
   unrichtige Belehrung das Verlangen unwirksam macht oder allein die
   Rechtsbehelfsfrist berührt, ist am Gesetz zu prüfen (§ 356 AO –
   für [JAHR] verifizieren). Behaupte insbesondere keine Nichtigkeit.
   Benenne die Rechtsbehelfsfrist positiv, ohne sie zu berechnen:
   Einspruchsfrist nach § 355 Abs. 1 AO; ist die Rechtsbehelfsbelehrung
   nicht oder unrichtig erteilt, richtet sich die Frist nach § 356 Abs. 2 AO
   (jeweils für [JAHR] verifizieren). Dasselbe gilt später für einen
   Einspruch gegen die Festsetzung des Mitwirkungsverzögerungsgeldes.
5. Inhalt und Umfang. Gib den verlangten Mitwirkungsgegenstand in eigenen
   Worten wieder und ordne ihn zu: Auskunft, Vorlage von Unterlagen,
   Überlassung von Daten, Erläuterung von Aufzeichnungen. Prüfe, ob er sich
   im Rahmen der Mitwirkungspflicht nach § 200 Abs. 1 AO hält
   (für [JAHR] verifizieren), ob er die Steuerarten und Zeiträume der
   Prüfung betrifft und ob er hinreichend bestimmt ist – also erkennen
   lässt, was genau bis wann in welcher Form vorzulegen ist; prüfe die im
   Verlangen gesetzte Frist dabei allein auf ihren Wortlaut, nicht auf ihr
   Ende. Halte außerdem fest, ob dem Verlangen ein Hinweis oder ein
   einfaches Mitwirkungsverlangen zu demselben Gegenstand vorausging: Das
   ist für die Verhältnismäßigkeit und für die Entschuldbarkeit nach
   Schritt 7 erheblich, und ein bereits erfüllter Vorgang kann den Umfang
   des Verlangens begrenzen. Behaupte NICHT, ein vorheriger Hinweis sei
   Wirksamkeitsvoraussetzung; ob das Gesetz ihn verlangt, ist am Wortlaut
   zu prüfen (§ 200a AO – für [JAHR] verifizieren). Benenne jede
   Unbestimmtheit einzeln; sie ist der Ansatz für eine Rückfrage und
   zugleich für die Entschuldbarkeit nach Schritt 7.
6. Erfüllbarkeit gegenüberstellen. Stelle in einer Zeile je verlangtem
   Einzelpunkt gegenüber: verlangt / liegt vor / liegt nicht vor / Grund /
   wer könnte es beschaffen / in welcher Form. Trenne dabei ausdrücklich
   nach Ursachen: nicht vorhanden, nicht exportierbar, bei einem Dritten,
   in einem Altsystem, tatsächlich unmöglich, oder nur mit unverhältnis-
   mäßigem Aufwand zu beschaffen. Stammt der Punkt aus einem Vorsystem oder
   von einem Dritten, verweise für die Systemklärung auf Prompt 108, ohne
   die Bewertung dorthin abzugeben.
7. Entschuldbarkeit – eigener Prüfschritt, nicht als Nebensatz. Von der
   Festsetzung des Mitwirkungsverzögerungsgeldes ist abzusehen, soweit die
   Verzögerung entschuldbar erscheint und dies glaubhaft gemacht wird
   (§ 200a Abs. 2 Satz 6 AO – für [JAHR] verifizieren). Das ist der
   wichtigste Verteidigungsansatz. Arbeite je Einzelpunkt ab: Welcher Grund
   wird geltend gemacht, ist er dem Steuerpflichtigen zuzurechnen, was
   könnte ihn glaubhaft machen (Bestätigung des Dienstleisters, Nachweis
   des Systemwechsels, Ausfallnachweis, Schriftverkehr über den Umfang),
   wer kann ihn glaubhaft machen, und was ist dafür zu beschaffen. Ordne
   jedem Grund die Stärke der Glaubhaftmachung zu
   [nicht belegt / belegbar / belegt] und benenne die Lücke.
8. Rechtsfolgen bei Nichterfüllung, vollständig und in dieser Reihenfolge.
   (a) Erfüllungsfrist: ein Monat nach Bekanntgabe des Verlangens, in
       begründeten Einzelfällen verlängerbar (§ 200a Abs. 1 Satz 4 AO –
       für [JAHR] verifizieren).
   (b) Mitwirkungsverzögerungsgeld: IST festzusetzen, gebundene Entscheidung
       ohne Ermessen (§ 200a Abs. 2 Satz 1 AO – für [JAHR] verifizieren);
       75 € je vollem Kalendertag der Verzögerung, höchstens
       150 Kalendertage (§ 200a Abs. 2 AO – Satzangabe und Betrag am
       amtlichen Volltext prüfen, für [JAHR] verifizieren). Ende
       spätestens mit Ablauf des Tages der Schlussbesprechung
       (§ 200a Abs. 2 Satz 5 AO – für [JAHR] verifizieren); ordne den
       angegebenen Stand der Schlussbesprechung hier ein. Rechne nicht.
   (c) Zuschlag zum Mitwirkungsverzögerungsgeld: steht im Ermessen und setzt
       einen Wiederholungsfall innerhalb von fünf Jahren
       (§ 200a Abs. 3 Nr. 1 AO) oder die wirtschaftliche Leistungsfähigkeit
       voraus, für die das Gesetz Umsatzerlöse ab 12 Mio. € und im Konzern
       ab 120 Mio. € als Regelbeispiel nennt (§ 200a Abs. 3 Nr. 2 AO);
       höchstens 25.000 € je vollem Kalendertag, höchstens 150
       Kalendertage (§ 200a Abs. 3 AO – Satzangabe und Betrag am amtlichen
       Volltext prüfen, für [JAHR] verifizieren). Ordne die Angaben zu früheren
       Verlangen, zur Größenklasse und zur Konzernzugehörigkeit hier ein und
       kennzeichne jede Einordnung, die nicht aus den Angaben folgt, als
       Vermutung.
   (d) Ablaufhemmung: § 200a Abs. 4 AO verlängert die in § 171 Abs. 4 Satz 3
       Halbsatz 1 AO bestimmte Frist um die Dauer der Verzögerung, mindestens
       um ein Jahr; im Wiederholungsfall entfällt dieser Halbsatz ganz
       (für [JAHR] verifizieren). Ordne ein, worauf sich das bezieht: Die
       Ablaufhemmung endet spätestens fünf Jahre nach Ablauf des
       Kalenderjahres, in dem die Prüfungsanordnung BEKANNTGEGEBEN wurde
       (§ 171 Abs. 4 Satz 3 AO – für [JAHR] verifizieren); § 200a Abs. 4 und
       5 AO bleibt davon unberührt (§ 171 Abs. 4 Satz 8 AO –
       für [JAHR] verifizieren). Berechne nichts und nenne kein Jahr.
9. Der Zielkonflikt bei der Anfechtung – ausdrücklich herausarbeiten, nicht
   nur erwähnen. Wird gegen das Verlangen oder gegen die Festsetzung
   Einspruch eingelegt oder Klage erhoben, endet die Festsetzungsfrist nicht
   vor Ablauf eines Jahres nach Unanfechtbarkeit der Entscheidung
   (§ 200a Abs. 5 AO – für [JAHR] verifizieren). Halte in einem eigenen,
   sichtbaren Absatz fest: Wer anficht, verlängert die Festsetzungsfrist und
   hält damit den Prüfungszeitraum länger offen. Stelle das dem möglichen
   Erfolg der Anfechtung gegenüber, ohne zu einem Weg zu raten, und weise
   darauf hin, dass diese Wirkung von der Anwendungsprüfung in Schritt 2
   abhängt.
10. Folgepflicht nach der Prüfung als Merkposten, nicht als gegenwärtige
    Pflicht. Eine Berichtigungspflicht nach § 153 Abs. 4 AO entsteht erst,
    wenn Prüfungsfeststellungen UNANFECHTBAR in einem Steuerbescheid, einem
    Feststellungsbescheid nach § 180 Abs. 1 Satz 1 Nr. 2 AO oder einem
    Teilabschlussbescheid nach § 180 Abs. 1a AO umgesetzt sind und derselbe
    Sachverhalt in einer anderen, nicht geprüften Erklärung zu einer
    Änderung führt (für [JAHR] verifizieren). Ordne die Angabe zum
    Teilabschlussbescheid hier ein. Schreibe ausdrücklich, dass daraus jetzt
    keine Handlungspflicht folgt, und leite aus dem Verlangen selbst keine
    Berichtigungspflicht ab.
11. Entscheidungsvorlage. Stelle vier Wege gegenüber – vollständig erfüllen,
    teilweise erfüllen und den Rest begründen, Verlängerung der
    Erfüllungsfrist beantragen (§ 200a Abs. 1 Satz 4 AO), anfechten – jeweils
    mit Voraussetzung, Vorteilen, Nachteilen und der Wirkung auf die
    Festsetzungsfrist. Die Wege schließen einander nicht aus; benenne die
    Kombinationen. Sprich keine Empfehlung aus.
12. Antwortentwurf. Formuliere ein Schreiben an das Finanzamt: sachlich,
    ohne Vorwurf, ohne Rechtsausführungen im Streitton, mit Bezug auf das
    Verlangen ohne Wiedergabe des Aktenzeichens, mit einer Aufstellung, was
    beigefügt ist, was nachgereicht wird und was aus welchem Grund nicht
    vorgelegt werden kann, und mit einer Bitte um Klarstellung bei jedem in
    Schritt 5 gefundenen unbestimmten Punkt. Höchstens 400 Wörter. Setze
    kein Datum ein, sondern schreibe an jeder Stelle, an der ein Datum
    stehen müsste, "(Datum von der Kanzlei einzusetzen)".

KEIN ABBRUCHGRUND – ausdrücklich
Fehlende, verlorene, nicht exportierbare oder bei einem Dritten liegende
Unterlagen sind KEIN Abbruchgrund – sie sind der Anlass dieses Prompts. Auch
eine bereits abgelaufene oder knappe Frist ist kein Abbruchgrund; sie ist
vielmehr sofort in der Fristenliste auszuweisen.

SPERRE GEGEN UNZULÄSSIGE EINGABEN
Diese Sperre ist keine fachliche Abbruchregel, sondern eine Notbremse für
Angaben, die nach `DATENSCHUTZ.md` (Zone Rot) gar nicht erst eingegeben
werden dürfen. Brich die gesamte Bearbeitung nur ab, wenn die Angaben eine
Steuernummer, eine Steuer-Identifikationsnummer oder ein Aktenzeichen des
Finanzamts enthalten. Gib dann nur aus:
"Abbruchgrund liegt vor – Bearbeitung an dieser Stelle abgebrochen, Prüfung
durch einen Berufsträger außerhalb des KI-Werkzeugs."
Ein Steuerstraf- oder Bußgeldverfahren, eine Selbstanzeige, eine
Durchsuchung sowie ein Haftungs-, Regress- oder Deckungsverfahren gegen die
Kanzlei klärt der Berufsträger vor dem Werkzeugeinsatz (siehe Abschnitt
Anwendung); die Antwort wird in der Handakte vermerkt und nicht in die
Eingabe geschrieben.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig /
   vertretbare Varianten / nicht ohne weitere Angaben entscheidbar. Liste
   fehlende Angaben auf, statt sie zu ergänzen.
2. Formuliere jede Aussage, die nicht aus den Angaben oder aus dem Gesetz
   folgt, ausdrücklich als Vermutung.
3. Behaupte nichts darüber, wie das Finanzamt im konkreten Fall entscheiden
   wird.
4. Jede Zuständigkeit als ROLLE, nie als Personenname.
5. Führe alle genannten Fundstellen am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit
2. (Einordnung) – Ergebnis der Schritte 1 bis 5, je Schritt höchstens fünf
   Sätze, mit Fundstelle
3. (Anwendungsprüfung) – Tabelle:
   Steuerart und Zeitraum | nach dem 31.12.2024 entstanden? |
   Prüfungsanordnung nach dem 31.12.2024 bekanntgegeben? | anwendbare
   Absätze des § 200a AO | offener Punkt
4. (Erfüllbarkeit) – Tabelle:
   Nr. | verlangter Einzelpunkt | liegt vor | liegt nicht vor | Grund |
   wer beschafft | Form
5. (Zumutbarkeits- und Entschuldbarkeitsraster) – Tabelle:
   Nr. | Einzelpunkt | Grund der Verzögerung | zurechenbar? | Mittel der
   Glaubhaftmachung | Stärke [nicht belegt / belegbar / belegt] | Lücke
6. (Rechtsfolgen) – Ergebnis von Schritt 8, ohne Rechnung, ohne Datum
7. (Zielkonflikt bei der Anfechtung) – eigener Absatz nach Schritt 9
8. (Entscheidungsvorlage) – Tabelle:
   Weg | Voraussetzung | Vorteile | Nachteile | Wirkung auf die
   Festsetzungsfrist | entscheidet
9. (Antwortentwurf an das Finanzamt) – höchstens 400 Wörter, ohne Datum
10. (Fristen und Zeitpunkte) – ohne Datum und ohne Berechnung, je mit
    Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren": Erfüllungsfrist
    des Verlangens, Antrag auf Verlängerung, Rechtsbehelfsfrist gegen das
    Verlangen, Rechtsbehelfsfrist gegen eine Festsetzung, Ende der
    Verzögerung mit der Schlussbesprechung, Wirkungen auf die
    Ablaufhemmung. Stelle voran: Die Frist des Verlangens und die
    Rechtsbehelfsfrist sind SOFORT und GESONDERT im Fristenprogramm zu
    erfassen. Ergänze in jedem Fall den Satz:
    "Fristen berechnet und erfasst ein Mensch."
11. (Merkposten nach der Prüfung) – § 153 Abs. 4 AO nach Schritt 10, mit dem
    ausdrücklichen Hinweis, dass daraus jetzt keine Handlungspflicht folgt
12. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
13. (Interne Notiz) – was die Kanzlei sofort veranlassen muss, wer welchen
    Nachweis beschafft, was gegenüber dem Mandanten anzusprechen ist; nicht
    an den Mandanten und nicht an das Finanzamt
14. Was ich nicht sicher weiß
```

## Anwendung

1. **Zuerst die Frist, dann der Prompt.** Das Verlangen geht an dem Tag des Eingangs an den Berufsträger; die Erfüllungsfrist und die Rechtsbehelfsfrist werden sofort und gesondert im Fristenprogramm erfasst, bevor irgendetwas bewertet wird. Der Prompt ersetzt diesen Schritt nicht und leistet ihn nicht.
2. **Vorschaltfrage vor dem Werkzeugeinsatz, vom Berufsträger zu beantworten und in der Handakte zu vermerken:** Berührt der verlangte Mitwirkungsgegenstand eine Berichtigungspflicht nach § 153 AO, eine Selbstanzeige, ein Steuerstraf- oder Bußgeldverfahren oder eine Durchsuchung – oder steht ein Haftungs-, Regress- oder Deckungsverfahren gegen die Kanzlei im Raum? Wenn ja, wird der Sachverhalt außerhalb des KI-Werkzeugs bearbeitet; die Fragen werden nicht in der Eingabe beantwortet (Zone Rot in `DATENSCHUTZ.md`).
3. Wortlaut des Verlangens vor dem Einfügen kürzen: Kopfzeile, Aktenzeichen, Anschrift und Namen entfernen, den Mitwirkungsgegenstand und die Fristsetzung wörtlich stehen lassen. Gerade an der Formulierung entscheidet sich die Bestimmtheit.
4. Die Gründe für eine Nichterfüllung ehrlich und getrennt eintragen. Wer „liegt nicht vor" ohne Ursache angibt, bekommt kein Entschuldbarkeitsraster, sondern eine Aufzählung.
5. Nachweise für die Glaubhaftmachung parallel beschaffen, nicht erst nach der Entscheidung über den Weg – die Bestätigung eines Dienstleisters braucht länger als die Frist.
6. Das Ergebnis mit dem laufenden Prüfungsvorgang zusammenführen (Prompt 34) und für die Systemfragen auf die Inventur der Vorsysteme zurückgreifen (Prompt 108). Wird aus dem Verlangen ein Rechtsbehelf, geht die Begründung an Prompt 33; eine freie Darstellung des Sachverhalts an das Finanzamt an Prompt 36.

## Qualitätssicherung

- **Vier-Augen-Prinzip, ausnahmslos:** Die Erfüllungsfrist des Verlangens und die Rechtsbehelfsfrist werden von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Verlangens und des Bekanntgabenachweises nachgeprüft und abgezeichnet – unabhängig davon, ob ein Rechtsbehelf geplant ist. Beide Fristen werden gesondert erfasst, nicht als ein Eintrag.
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum, kein Fristende und kein Betrag aus der KI-Antwort übernehmen. Erscheint in der Antwort ein errechneter Betrag des Mitwirkungsverzögerungsgeldes, ist die Antwort an dieser Stelle regelwidrig und zu streichen.
- **Bekanntgabe gegenprüfen, nicht das Datum des Schreibens.** Sowohl die Sechs-Monats-Sperre als auch die Erfüllungsfrist knüpfen an die Bekanntgabe an; der Nachweis der Bekanntgabe ist zu den Akten zu nehmen. Bei elektronischer Bekanntgabe den Bereitstellungs- und Abrufnachweis zur Akte nehmen; das Verfahren, mit dem die Kanzlei solche Nachweise erzeugt und überwacht, regelt Prompt 102 – die Bekanntgabe im Einzelfall stellt der Berufsträger anhand des Nachweises fest, nicht Prompt 102.
- **Formulierung zum Mitwirkungsverzögerungsgeld prüfen.** Es ist festzusetzen; ein „kann festgesetzt werden" im Entwurf ist falsch und führt in der Beratung zu einer falschen Risikoeinschätzung. Ermessen besteht nur beim Zuschlag.
- **Die beiden Anwendungsregeln getrennt prüfen.** Art. 97 § 37 Abs. 2 und Abs. 3 EGAO für § 200a AO einerseits, die Anwendungsregel für § 171 Abs. 4 AO andererseits – § 171 Abs. 4 AO ist in Art. 97 § 37 Abs. 3 EGAO nicht aufgeführt (für [JAHR] verifizieren). Jede Antwort, die beides gleichsetzt, ist zu korrigieren.
- **Den Zielkonflikt dem Mandanten offenlegen.** Die Anfechtung kann die Festsetzungsfrist verlängern (§ 200a Abs. 5 AO – für [JAHR] verifizieren). Diese Kehrseite gehört in die Beratung und in die Handakte, nicht nur in die interne Notiz.
- **Freigabe durch einen Berufsträger** für den Antwortentwurf, für jede Aussage gegenüber der Prüfungsstelle und für die Entscheidung über den Weg (Freigabestufe 3 in `DATENSCHUTZ.md`). Die Entscheidung über einen Rechtsbehelf trifft der Mandant nach Beratung.
- **Umfang der Herausgabe gesondert freigeben.** Was tatsächlich vorgelegt oder überlassen wird, entscheidet der Berufsträger; das Modell schlägt nichts vor, was über den Wortlaut des Verlangens hinausgeht.
- **Rechtsstand prüfen an:** § 200a AO, § 200 AO, § 171 Abs. 4 AO, § 153 Abs. 4 AO, § 180 Abs. 1 Satz 1 Nr. 2 und Abs. 1a AO, § 202 AO, § 356 AO, § 355 AO und Art. 97 § 37 EGAO im amtlichen Volltext (gesetze-im-internet.de), am Anwendungserlass zur Abgabenordnung sowie am amtlichen Titel des Einführungsgesetzes (Gesetz zur Umsetzung der Richtlinie (EU) 2021/514, BGBl. 2022 I S. 2730 – für [JAHR] verifizieren).

## Varianten

- **Nur Fristenblatt:** „Gib ausschließlich die Fristenliste ohne Datum und ohne Berechnung aus, mit Rechtsgrundlage, Zuständigkeit und Erfassungsvermerk."
- **Nur Entschuldbarkeit:** „Beschränke die Antwort auf das Entschuldbarkeitsraster nach § 200a Abs. 2 Satz 6 AO und auf die Liste der zu beschaffenden Nachweise, je mit Rolle und Beschaffungsweg."
- **Fristverlängerung:** „Erzeuge nur den Antrag auf Verlängerung der Erfüllungsfrist nach § 200a Abs. 1 Satz 4 AO mit Begründung des Einzelfalls, ohne Datum, höchstens 200 Wörter."
- **Festsetzung eingegangen:** „Das Mitwirkungsverzögerungsgeld ist festgesetzt. Erzeuge die Prüfung der Festsetzung nach Grund, Dauer, Höchstdauer und Entschuldbarkeit sowie die Entscheidungsvorlage über einen Rechtsbehelf einschließlich der Wirkung des § 200a Abs. 5 AO."
- **Mandanteninformation:** „Erkläre dem Mandanten in Sie-Form, höchstens 250 Wörter, was das Verlangen ist, was jetzt zu tun ist, welche Folgen eine Verzögerung hat und warum die Entscheidung über eine Anfechtung nicht selbstverständlich ist – ohne Datum, ohne Betragsberechnung."
