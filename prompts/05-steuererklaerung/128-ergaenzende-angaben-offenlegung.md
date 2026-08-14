# 128 – Ergänzende Angaben in der Steuererklärung: Offenlegen oder nicht

**Problem:** In einer Erklärung steckt ein nicht abschließend geklärter Sachverhalt oder eine bewusst von der Verwaltungsauffassung abweichende Rechtsauffassung, und ob das im dafür vorgesehenen Feld gekennzeichnet wird – mit der Folge, dass der Fall aus der vollautomatisierten Veranlagung ausgesteuert wird und die Bearbeitung länger dauert –, entscheidet in vielen Kanzleien niemand systematisch, sondern die Person, die die Erklärung fertigstellt.
**Rolle:** Berufsträger (Entscheidung und Freigabe), Sachbearbeitung (Vorbereitung und Entwurf der Anlage)
**DATEV-Bezug:** DATEV Einkommensteuer mit dem Hauptvordruck und dem Abschnitt „Ergänzende Angaben zur Steuererklärung", Übermittlung über die ERiC-Schnittstelle, DATEV DMS für Anlage und Aktennotiz, DATEV Eigenorganisation für die Wiedervorlage bei wiederkehrenden Sachverhalten. Ob und an welcher Stelle die übrigen Steuerprogramme diesen Abschnitt führen, ist im Programm zu prüfen; Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Steuerart und Veranlagungszeitraum, der Sachverhalt in einem Satz ohne identifizierende Angaben, Art des Problems, ob die abweichende Auffassung durch Rechtsprechung oder Literatur gestützt ist, Größenklasse der Auswirkung, Wiederholungscharakter, Handhabung in Vorjahren, Stand einer erwogenen verbindlichen Auskunft, geprüfte Zeilennummer des aktuellen Vordrucks.
**Datensparsamkeit:** Der Sachverhalt gehört nur als abstrakte Fallbeschreibung in das Werkzeug – Mandant als `Mandant A`, Beteiligte nur als Rolle, Beträge nur als Größenklasse. Steuernummer, Steuer-Identifikationsnummer und das Aktenzeichen des Finanzamts gehören auch maskiert und auch in Ausschnitten nicht in ein KI-Werkzeug (Zone Rot in `DATENSCHUTZ.md`); Bildschirmausdrucke aus dem Erklärungsprogramm enthalten diese Angaben regelmäßig und werden nicht eingefügt. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) sind vor dem Einsatz zu klären – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und entscheidest über die
Offenlegung ergänzender Angaben in der Steuererklärung. Du wägst ab, statt zu
empfehlen, was bequem ist, du benennst die Nachteile der Offenlegung ebenso wie
ihre Vorteile, und du kennzeichnest ungesicherte Argumente als ungesichert.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt entscheidet über die Kennzeichnung IN DER ERKLÄRUNG und über den
Inhalt der gesonderten Anlage. Er ist keine Sachverhaltsdarstellung an das
Finanzamt nach Abgabe (dafür Prompt 36), keine Einspruchsbegründung (dafür
Prompt 33) und kein Bescheidabgleich (dafür Prompt 32). Er beurteilt auch nicht
die materielle Rechtsfrage selbst; er ordnet sie ein und stellt die
Handlungsoptionen gegenüber.

GRUNDREGELN FÜR DIE GESAMTE ANTWORT
- Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
  Absatz und Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
  keine Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- Berechne KEINE Fristen und nenne keine Fristdauer. Schreibe "die in [NORM]
  bestimmte Frist" und ergänze bei jeder genannten Frist: "Fristen berechnet und
  erfasst ein Mensch."
- Jede Empfehlung steht unter dem ausdrücklichen Vorbehalt der Entscheidung
  durch einen Berufsträger. Sage keinen Erfolg voraus – weder, dass das
  Finanzamt der Auffassung folgt, noch, dass eine Prüfung unterbleibt.
- Kennzeichne ungesicherte Argumente ausdrücklich als ungesichert.

SACHVERHALT
- Steuerart: [Einkommensteuer / Körperschaftsteuer / Gewerbesteuer / gesonderte
  Feststellung / Umsatzsteuer / sonstige]
- Veranlagungszeitraum: [JAHR]
- Worum es geht, in einem Satz und ohne identifizierende Angaben: [ANGABE]
- Art des Problems: [steuererhebliche Sachverhalte konnten nicht erklärt werden /
  bewusst abweichende Rechtsauffassung / Wunsch nach personell vertiefter
  Prüfung / mehrere der genannten Gründe]
- Es werden lediglich Belege oder Aufstellungen übermittelt, ohne dass einer der
  vorstehenden Gründe vorliegt: [ja / nein]
- Abweichende Auffassung durch Rechtsprechung oder Literatur gestützt:
  [ja / nein / unklar], Fundstellen soweit bekannt: [ANGABE]
- Größenklasse der steuerlichen Auswirkung, gemessen an diesem Mandat:
  [gering / mittel / hoch / nicht bezifferbar]
- Sachverhalt: [einmalig / wiederkehrend]
- In Vorjahren bereits so verfahren: [ja / nein / unbekannt]
- Verbindliche Auskunft erwogen: [ja / nein / nicht geprüft]
- Zeile und Kennzahl am aktuellen amtlichen Vordruck geprüft:
  [nein / ja], geprüfte Zeile: [ZEILE]

BESTÄTIGUNGEN VOR DER BEARBEITUNG
- Die eingefügten Angaben sind von Steuernummer, Steuer-Identifikationsnummer,
  Aktenzeichen des Finanzamts, Namen, Anschriften und Beträgen befreit:
  [bestätigt / nicht bestätigt]
- Die Vorschaltfragen aus dem Abschnitt "Anwendung" hat der Berufsträger
  beantwortet, und sie stehen dem Einsatz des Werkzeugs nicht entgegen:
  [bestätigt / nicht bestätigt]

RECHTLICHER RAHMEN – VERBINDLICH, NICHT ABWANDELN
a) GRUNDLAGE DES FREITEXTFELDS IST § 150 Abs. 7 SATZ 1 AO: Können
   Steuererklärungen nach § 155 Abs. 4 Satz 1 AO zu einer ausschließlich
   automationsgestützten Steuerfestsetzung führen, "ist es dem Steuerpflichtigen
   zu ermöglichen, Angaben, die nach seiner Auffassung Anlass für eine
   Bearbeitung durch Amtsträger sind, in einem dafür vorgesehenen Abschnitt oder
   Datenfeld der Steuererklärung zu machen" (für [JAHR] verifizieren).
   ZITIERE FÜR DAS FREITEXTFELD NIEMALS § 150 Abs. 7 SATZ 2 AO. Satz 2 regelt
   etwas anderes, nämlich die Fiktion für Daten, die nach § 93c AO übermittelt
   wurden. Eine Ausgabe, die Satz 2 für das Freitextfeld heranzieht, ist falsch.
b) RECHTSFOLGENORM IST § 155 Abs. 4 SATZ 3 AO, wörtlich: "Ein Anlass zur
   Bearbeitung durch Amtsträger liegt insbesondere vor, soweit der
   Steuerpflichtige in einem dafür vorgesehenen Abschnitt oder Datenfeld der
   Steuererklärung Angaben im Sinne des § 150 Absatz 7 gemacht hat."
   § 155 Abs. 4 Satz 1 AO trägt die ausschließlich automationsgestützte
   Festsetzung (für [JAHR] verifizieren).
c) VORDRUCK. Für den Veranlagungszeitraum 2025 steht der Abschnitt "Ergänzende
   Angaben zur Steuererklärung" in ZEILE 37 des Hauptvordrucks ESt 1 A,
   KENNZAHL 500, mit der Auswahl:
   1 = konnten steuererhebliche Sachverhalte nicht erklärt werden;
   2 = wird bewusst eine von der Verwaltungsauffassung abweichende
       Rechtsauffassung vertreten;
   3 = sollen Sachverhalte personell vertieft geprüft werden;
   4 = liegen mehrere der vorgenannten Gründe vor.
   Der Vordruck verlangt eine gesonderte Anlage "Ergänzende Angaben zur
   Steuererklärung" zur Erläuterung und weist darauf hin, dass sich die
   Bearbeitungsdauer verlängern kann. BEI BLOSSER ÜBERMITTLUNG VON BELEGEN UND
   AUFSTELLUNGEN IST KEINE EINTRAGUNG VORZUNEHMEN.
   ZWEI EINSCHRÄNKUNGEN, die du in jeder Antwort ausschreibst:
   (1) Die Zeilennummer ist nur für den Veranlagungszeitraum 2025 belegt und
       ändert sich jährlich; sie ist am aktuellen amtlichen Vordruck zu prüfen
       (für [JAHR] verifizieren).
   (2) Der Vordruck zitiert § 150 Abs. 7 AO NICHT; der Bezug ist inhaltlich,
       nicht zitiert. Behaupte nichts anderes.
d) WORUM ES WIRTSCHAFTLICH GEHT: § 173 Abs. 1 Nr. 1 AO – Änderung zuungunsten
   bei nachträglich bekannt gewordenen Tatsachen; § 173 Abs. 1 Nr. 2 Satz 1 AO –
   Änderung zugunsten nur, wenn den Steuerpflichtigen kein grobes Verschulden
   am nachträglichen Bekanntwerden trifft, Satz 2 Unbeachtlichkeit des
   Verschuldens im Zusammenhang mit Tatsachen nach Nummer 1; § 173 Abs. 2 AO –
   Änderungssperre nach einer Außenprüfung; § 173a AO (ein Satz, keine Absätze) –
   Schreib- oder Rechenfehler bei Erstellung der Steuererklärung
   (für [JAHR] verifizieren).
   AUSDRÜCKLICH VERBOTEN ist die Aussage, eine Eintragung im Abschnitt
   "Ergänzende Angaben" schließe grobes Verschulden nach § 173 Abs. 1 Nr. 2 AO
   aus oder führe zu dessen Wegfall. Das steht nicht im Gesetz und ist nicht
   belegt. Du darfst die Offenlegung als ARGUMENT gegen ein grobes Verschulden
   benennen, musst es aber ausdrücklich als "ungesichert – nicht belegt"
   kennzeichnen.
e) ALTERNATIVE, die du immer gegenüberstellst: die verbindliche Auskunft über
   die steuerliche Beurteilung genau bestimmter, noch nicht verwirklichter
   Sachverhalte nach § 89 Abs. 2 Satz 1 AO, die ein besonderes Interesse im
   Hinblick auf die erheblichen steuerlichen Auswirkungen voraussetzt. Für die
   Bearbeitung des Antrags wird eine Gebühr erhoben (§ 89 Abs. 3 Satz 1 AO);
   die Reichweite der Bindungswirkung regelt nicht § 89 AO selbst, sondern die
   auf § 89 Abs. 2 Satz 5 AO gestützte Steuer-Auskunftsverordnung (StAuskV),
   dort § 2 (für [JAHR] verifizieren). Halte dabei fest,
   dass sie sich auf einen noch nicht verwirklichten Sachverhalt bezieht und
   damit für einen bereits abgelaufenen Veranlagungszeitraum in der Regel nicht
   mehr in Betracht kommt – für wiederkehrende Sachverhalte dagegen für die
   Zukunft sehr wohl.
f) GRENZE: Reicht der Sachverhalt in den Bereich der Steuerhinterziehung
   (§ 370 AO) oder besteht eine Berichtigungspflicht nach § 153 AO, ist die
   Eintragung KEINE Lösung. Benenne diese Grenze in einem Satz und verweise auf
   die Vorschaltfrage; prüfe sie nicht (für [JAHR] verifizieren).

PRÜFE IN DIESER REIHENFOLGE
E1. ABGRENZUNG ZUR BLOSSEN BELEGÜBERMITTLUNG – dieser Schritt kommt zuerst.
    Steht im Feld "Es werden lediglich Belege oder Aufstellungen übermittelt"
    "ja", lautet das Ergebnis: keine Eintragung. Sage das deutlich, begründe es
    mit Buchstabe c und arbeite von den folgenden Schritten nur noch E6 aus.
    Gib die Positionen 4, 5 und 6 des Ausgabeformats dann mit "entfällt – keine
    Eintragung" aus, ohne sie zu füllen; insbesondere entwirfst du in diesem
    Fall KEINE gesonderte Anlage. Steht dort "nein", arbeite alle Schritte aus.
    Dies ist der häufigste Fehlgebrauch des Feldes.
E2. ZUORDNUNG. Ordne den Fall genau einer der vier Ausprägungen aus Buchstabe c
    zu und begründe die Zuordnung aus dem Feld "Art des Problems". Passen
    mehrere, ist es Ausprägung 4. Passt keine, sage das, statt zu erzwingen.
    Werte anschließend die Felder "Steuerart", "Veranlagungszeitraum" und
    "Zeile und Kennzahl am aktuellen amtlichen Vordruck geprüft" aus: Weicht die
    Steuerart von der Einkommensteuer oder der Veranlagungszeitraum von 2025 ab
    oder steht bei der Prüfung "nein", kennzeichnest du die Angabe zu Zeile und
    Kennzahl als UNGEPRÜFT, führst sie als offenen Punkt und benennst, dass
    Abschnitt, Zeile und Kennzahl am amtlichen Vordruck dieser Steuerart und
    dieses Veranlagungszeitraums festzustellen sind.
E3. ABWÄGUNG DER FOLGEN, in beide Richtungen und ohne Beschönigung:
    – Aussteuerung aus der ausschließlich automationsgestützten Festsetzung
      (§ 155 Abs. 4 Satz 3 AO), damit personelle Bearbeitung;
    – längere Bearbeitungsdauer, wie der Vordruck selbst ankündigt;
    – erhöhte Aufmerksamkeit für den Fall, auch über den gekennzeichneten Punkt
      hinaus;
    – auf der anderen Seite die dokumentierte Offenlegung. Ihre Wirkung auf die
      Frage, ob eine Tatsache dem Finanzamt nachträglich bekannt wird
      (§ 173 Abs. 1 Nr. 1 AO), knüpfst du ausschließlich an die in der
      gesonderten Anlage tatsächlich mitgeteilte Tatsache, nicht an die
      Kennzeichnung als solche; das Ankreuzen allein teilt keine Tatsache mit.
      Diese Wirkung kennzeichnest du – ebenso wie die Verschuldensfrage nach
      Buchstabe d – als "ungesichert – nicht belegt" und ergänzt
      "Fundstelle offen – bitte recherchieren".
    Beziehe die Felder "Größenklasse", "einmalig oder wiederkehrend" und "In
    Vorjahren bereits so verfahren" ein: Eine abweichende Handhabung gegenüber
    den Vorjahren begründest du gesondert oder empfiehlst, die Vorjahre
    mitzubetrachten.
E4. ALTERNATIVEN. Stelle Eintragen, Nicht eintragen und die verbindliche
    Auskunft nach § 89 Abs. 2 AO nebeneinander. Werte dazu die Felder
    "Verbindliche Auskunft erwogen", "einmalig oder wiederkehrend" und "durch
    Rechtsprechung oder Literatur gestützt" aus: Ist die Auffassung nicht
    gestützt und der Sachverhalt wiederkehrend, gehört die Auskunft für die
    Zukunft in die Empfehlung. Benenne Gebührenpflicht (§ 89 Abs. 3 Satz 1 AO)
    und Bindungswirkung (§ 2 StAuskV auf Grundlage des § 89 Abs. 2 Satz 5 AO)
    dem Grunde nach, jeweils mit Fundstelle und ohne Beträge zu nennen.
E5. INHALT DER GESONDERTEN ANLAGE. Lege fest, was hineingehört: Bezeichnung des
    Sachverhalts, betroffener Veranlagungszeitraum und betroffene Position,
    kurze Darstellung des Sachverhalts, die vertretene Auffassung mit Fundstellen,
    die abweichende Verwaltungsauffassung mit Fundstelle, Angabe der Auswirkung
    dem Grunde nach, Bitte um personelle Bearbeitung. Keine Beweisangebote, keine
    Wertungen über die Verwaltung, keine Verhandlungsangebote.
E6. HANDHABUNGSREGEL FÜR DIE KANZLEI. Schlage vor, wer die Entscheidung trifft
    und wie sie dokumentiert wird. Nach der Konvention dieser Kanzlei ist das ein
    BERUFSTRÄGER; die Sachbearbeitung bereitet vor und entscheidet nicht. Leite
    aus den Feldern "wiederkehrend" und "In Vorjahren bereits so verfahren" ab,
    ob eine Wiedervorlage für die Folgejahre anzulegen ist.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Ein ungeklärter Sachverhalt, eine bewusst abweichende Rechtsauffassung und der
Wunsch nach personeller Prüfung sind KEIN Abbruchgrund – sie sind der Anlass
dieses Prompts. Brich die Bearbeitung nur ab, wenn (a) das erste
Bestätigungsfeld oder (b) das zweite Bestätigungsfeld nicht auf "bestätigt"
steht, auch dann, wenn das Feld unausgefüllt geblieben ist. Gib dann nur aus:
"Abbruchgrund liegt vor (Buchstabe angeben) – Bearbeitung an dieser Stelle
abgebrochen, Prüfung durch einen Berufsträger außerhalb des KI-Werkzeugs."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben
   auf und arbeite mit klar benannten Annahmen weiter.
2. Formuliere jede Aussage, die nicht aus den Angaben oder aus einer benannten
   Fundstelle folgt, ausdrücklich als Vermutung.
3. Die gesonderte Anlage ist sachlich, in Sie-Form, höchstens 300 Wörter, ohne
   Beträge, ohne Angriff auf die Verwaltungsauffassung.
4. Höchstens 800 Wörter Fließtext außerhalb der Entwürfe; Tabellen und Listen
   zählen nicht mit.
5. Führe alle genannten Fundstellen am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit
2. (Abgrenzung zur bloßen Belegübermittlung) – Ergebnis in einem Satz, mit
   Begründung
3. (Empfehlung) – eintragen mit welcher Ausprägung, oder nicht eintragen; mit
   Begründung und dem ausdrücklichen Vorbehalt: die Entscheidung trifft ein
   Berufsträger
4. (Gegenüberstellung) – Tabelle; entfällt bei bloßer Belegübermittlung:
   Option (Eintragen / Nicht eintragen / Verbindliche Auskunft nach § 89 Abs. 2
   AO) | Vorteile | Nachteile | Voraussetzungen | Fundstelle
5. (Ungesicherte Argumente) – eigener Abschnitt; hierher gehören die Frage des
   groben Verschuldens nach § 173 Abs. 1 Nr. 2 AO und die Wirkung der
   Offenlegung auf das nachträgliche Bekanntwerden nach § 173 Abs. 1 Nr. 1 AO,
   beide ausdrücklich gekennzeichnet als "ungesichert – nicht belegt"
6. (Entwurf der gesonderten Anlage "Ergänzende Angaben zur Steuererklärung") –
   entfällt bei bloßer Belegübermittlung und bei der Empfehlung, nicht
   einzutragen
7. (Interne Aktennotiz) – Entscheidung, Begründung, Entscheider als Rolle,
   Datum als Auslassung zum Ausfüllen, Wiedervorlage für die Folgejahre;
   nicht an den Mandanten
8. (Hinweis zur Zeilennummer) – die Angabe zu Zeile 37 und Kennzahl 500 ist für
   den Veranlagungszeitraum 2025 belegt, ändert sich jährlich und ist am
   aktuellen amtlichen Vordruck zu prüfen; der Vordruck zitiert § 150 Abs. 7 AO
   nicht
9. (Handhabungsregel für die Kanzlei) – wer entscheidet, wer vorbereitet, wie
   dokumentiert wird
10. (Offene Punkte) – was fehlt, wer es klärt
11. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. **Vor dem Werkzeugeinsatz vom Berufsträger beantworten und in der Handakte vermerken (Vorschaltfragen):** (a) Reicht der Sachverhalt in den Bereich einer Steuerhinterziehung (§ 370 AO) oder in ein bereits eingeleitetes Straf- oder Bußgeldverfahren? (b) Besteht für diesen oder einen früheren Veranlagungszeitraum eine Berichtigungspflicht nach § 153 AO oder wird eine Selbstanzeige erwogen? Ist eine der Fragen mit ja zu beantworten, ist die Eintragung im Erklärungsvordruck nicht das richtige Mittel, und der Vorgang bleibt vollständig außerhalb des KI-Werkzeugs (Zone Rot in `DATENSCHUTZ.md`). Nur wenn beide Fragen dem Einsatz nicht entgegenstehen, wird das zweite Bestätigungsfeld auf „bestätigt" gesetzt.
2. **Zeile und Kennzahl am aktuellen amtlichen Vordruck nachschlagen, bevor der Prompt ausgefüllt wird**, und im Feld „geprüfte Zeile" eintragen. Belegt ist Zeile 37 des Hauptvordrucks ESt 1 A allein für den Veranlagungszeitraum 2025; die Nummerierung ändert sich jährlich, und für andere Steuerarten steht der Abschnitt an anderer Stelle.
3. Die Entscheidung fällt **vor** der Freigabe der Erklärung, nicht beim Absenden. Wer erst im Übermittlungsdialog entscheidet, entscheidet unter Zeitdruck und dokumentiert nichts.
4. Die gesonderte Anlage ist Pflichtbestandteil, wenn eingetragen wird. Eine Kennzeichnung ohne Erläuterung erzeugt eine Rückfrage und verlängert die Bearbeitung zusätzlich.
5. Bei wiederkehrenden Sachverhalten die Folgejahre gleich mitentscheiden und eine Wiedervorlage anlegen. Eine Handhabung, die zwischen den Jahren wechselt, ist im Nachhinein schwer zu erklären.
6. Aktennotiz und Anlage in dieselbe Ablage wie die Erklärung; die Entscheidung muss auch in zwei Jahren noch nachvollziehbar sein.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Die Entscheidung über die Eintragung trifft ein Berufsträger und niemand sonst; Freigabestufe 3 in `DATENSCHUTZ.md` für die Anlage und für die Erklärung insgesamt.
- **Prüfen, ob der Text § 150 Abs. 7 Satz 2 AO für das Freitextfeld heranzieht.** Grundlage ist Satz 1; Satz 2 regelt die Fiktion für nach § 93c AO übermittelte Daten (für [JAHR] verifizieren). Das ist der häufigste Zitierfehler zu dieser Norm.
- **Prüfen, ob behauptet wird, die Eintragung schließe grobes Verschulden nach § 173 Abs. 1 Nr. 2 AO aus.** Diese Aussage steht nicht im Gesetz und ist nicht belegt; zulässig ist sie nur als ausdrücklich gekennzeichnetes, ungesichertes Argument.
- **Prüfen, ob die Zeilenangabe ohne Jahresbezug stehen geblieben ist.** Zeile 37 und Kennzahl 500 sind für den Veranlagungszeitraum 2025 belegt (für [JAHR] verifizieren); ohne Prüfung am aktuellen Vordruck wird die Angabe im Folgejahr falsch.
- **Prüfen, ob behauptet wird, der Vordruck nehme auf § 150 Abs. 7 AO Bezug.** Er zitiert die Norm nicht; der Zusammenhang ist inhaltlich.
- **Prüfen, ob bei bloßer Belegübermittlung eine Eintragung empfohlen wird.** Das ist falsch und der häufigste Fehlgebrauch des Feldes. In diesem Fall darf die Ausgabe auch keinen Entwurf der gesonderten Anlage und keine Gegenüberstellung enthalten; die Positionen 4 bis 6 lauten dann „entfällt – keine Eintragung".
- **Prüfen, ob der Ausgabe zufolge schon das Ankreuzen eine Tatsache offenlegt.** Bekannt wird dem Finanzamt nur, was die gesonderte Anlage tatsächlich mitteilt; die Wirkung auf § 173 Abs. 1 Nr. 1 AO ist außerdem als ungesichert zu kennzeichnen.
- **Prüfen, ob die Nachteile der Offenlegung im Text stehen** – Aussteuerung aus der automationsgestützten Festsetzung, längere Bearbeitungsdauer, erhöhte Aufmerksamkeit. Eine Ausgabe, die nur die Vorteile nennt, ist unvollständig.
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum und keine Fristdauer aus dem Modell übernehmen (siehe Prompt 35).
- **Rechtsstand prüfen an:** §§ 89, 150, 153, 155, 173, 173a und 370 AO sowie § 2 der Steuer-Auskunftsverordnung im amtlichen Volltext (gesetze-im-internet.de) und am amtlichen Vordruck des betroffenen Veranlagungszeitraums einschließlich der zugehörigen Anleitung.

## Varianten

- **Kurzentscheid:** „Erzeuge nur Abgrenzung, Empfehlung und Zuordnung zu einer der vier Ausprägungen, höchstens 150 Wörter."
- **Nur die Anlage:** „Erzeuge allein den Entwurf der gesonderten Anlage, ohne Abwägung und ohne Aktennotiz."
- **Kanzleiregel:** „Formuliere aus der Handhabungsregel eine allgemeine Arbeitsanweisung für die Kanzlei: wann vorgelegt wird, wer entscheidet, wie dokumentiert wird, wie die Folgejahre behandelt werden."
- **Andere Steuerart:** „Übertrage die Prüfung auf den Vordruck der angegebenen Steuerart und weise ausdrücklich darauf hin, dass Abschnitt, Zeile und Kennzahl dort gesondert am amtlichen Vordruck zu prüfen sind."
- **Bestandsdurchsicht:** „Erzeuge eine Arbeitsliste, mit der die Kanzlei prüft, in welchen laufenden Erklärungen ein solcher Sachverhalt steckt, gegliedert nach Ausprägung und Größenklasse, mit Spalte für die Vorlage an den Berufsträger."
