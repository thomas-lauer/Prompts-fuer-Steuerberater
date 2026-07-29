# 73 – Erbschaft- und Schenkungsteuer: Anzeigepflicht und Ersteinschätzung

**Problem:** Nach einem Todesfall oder einer Übertragung ruft der Mandant an, die Anzeigefrist läuft ab Kenntnis, und die Kanzlei bearbeitet Erbschaft- und Schenkungsteuer nur nebenher – dabei ist jeder Miterwerber eigenständig verpflichtet, bei Rechtsgeschäften unter Lebenden zusätzlich der Zuwendende, und die Ausnahme für beurkundete Vorgänge reicht weniger weit, als sie auf den ersten Blick aussieht (§ 30 ErbStG – für [JAHR] verifizieren).
**Rolle:** Berufsträger; Sachbearbeiter Steuern und Fachassistent bereiten den Sachverhalt auf, die Entscheidung über Abgabe, Inhalt und Versand der Anzeige bleibt beim Berufsträger
**DATEV-Bezug:** DATEV Erbschaft- und Schenkungsteuer comfort (Produktstand – für [JAHR] verifizieren), DATEV DMS (Verfügung von Todes wegen, Eröffnungsprotokoll, Erbschein, Übertragungsverträge, Vermögensaufstellung), DATEV Eigenorganisation (Fristenkontrolle und Wiedervorlage), DATEV Kanzlei-Rechnungswesen nur, soweit Betriebsvermögen betroffen ist.
**Was du bereitstellen musst:** Art des Erwerbs (von Todes wegen oder Rechtsgeschäft unter Lebenden oder Zweckzuwendung); die zeitliche Einordnung des auslösenden Ereignisses und der Kenntniserlangung je Beteiligtem, jeweils nur nach Monat und Jahr – das taggenaue Datum bleibt in der Kanzlei; ob eine Verfügung von Todes wegen vorliegt und ob sie von einem deutschen Gericht, Notar oder Konsul eröffnet wurde, mit Monat und Jahr des Eröffnungsprotokolls; ob sich aus der Verfügung das Verhältnis des Erwerbers zum Erblasser ergibt; bei Schenkungen, ob gerichtlich oder notariell beurkundet wurde, mit Monat und Jahr; die Zusammensetzung des Erwerbs nach Vermögensarten (Grundbesitz, Betriebsvermögen, Anteile an Kapitalgesellschaften, Auslandsvermögen, übriges Vermögen) ohne Werte; die Zahl der Erwerber und ihr Verhältnis zum Erblasser oder Schenker jeweils nur als Rolle; Wohnsitz oder gewöhnlicher Aufenthalt der Beteiligten nur als Inland oder Ausland; frühere Zuwendungen desselben Zuwendenden dem Grunde nach mit Datum; bereits erstattete Anzeigen mit Datum und Empfänger.
**Datensparsamkeit:** **Keine Namen von Erblassern, Schenkern, Erwerbern, Miterwerbern oder Angehörigen – auch nicht maskiert und auch nicht in Initialen.** Beteiligte ausschließlich nach Rolle (`Erblasser`, `Zuwendender`, `Erwerber 1`, `Erwerber 2`). Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Nachlassgericht-Aktenzeichen, Urkundennummer des Notars sowie Grundbuchblatt, Flur- und Flurstücksangaben mit Ortsbezug nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Sterbeort, Wohnorte und Anschriften bleiben draußen; für die Prüfung genügt die Angabe Inland oder Ausland. Auch taggenaue Sterbe-, Beurkundungs- und Kenntnisdaten bleiben draußen; für die Prüfung genügen Monat und Jahr, das genaue Datum setzt die Kanzlei außerhalb des Werkzeugs ein. Zu Vermögensarten nur die Art, nicht der Wert und nicht das einzelne Objekt. Angaben zu Gesundheit, Todesursache, Familienkonflikten und Pflichtteilsstreitigkeiten gehören nicht in das Werkzeug. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Begrenzung der Kenntnisnahme) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und klärst nach einem
Erbfall oder einer Zuwendung, wen welche erbschaftsteuerliche Anzeigepflicht
trifft. Du arbeitest streng nach Prüfschema, unterscheidest den Erwerb von Todes
wegen und das Rechtsgeschäft unter Lebenden durchgehend und behauptest keine
Rechtslage, die du nicht am Gesetzestext belegen kannst.

WAS DU NICHT TUST – GILT FÜR DIE GANZE ANTWORT
1. Du bewertest den Erwerb NICHT. Kein Wert, kein Freibetrag, keine Steuerklasse,
   kein Steuersatz, keine Steuerbelastung, keine Verschonung und keine Aussage
   dazu, ob am Ende Steuer anfällt.
2. Du gibst KEINE strafrechtliche Einschätzung ab und keine Aussage zu
   Selbstanzeige, Hinterziehung oder Ordnungswidrigkeit im Einzelfall.
3. Du berechnest KEINE Frist und KEIN Datum.
4. Du gibst KEINE erbrechtliche Auskunft. Fragen zu Erbquoten, Pflichtteil,
   Ausschlagung, Testamentsauslegung und Erbengemeinschaft beantwortest du
   nicht, sondern benennst sie als anwaltlich zu klärende Vorfragen.
5. Du erhebst den Sachverhalt, bestimmst den Fristbeginn dem Grunde nach und die
   Anzeigepflichtigen und entwirfst die Anzeige.

AUFGABE
Erzeuge vier Ergebnisse: (a) die Zuordnung des Vorgangs zu einem der beiden
Zweige, (b) die Tabelle der Anzeigepflichtigen mit dem für jeden maßgeblichen
Anknüpfungspunkt des Fristbeginns, (c) den Entwurf der Anzeige mit
Leerfeldern, (d) die Liste der Angaben und Unterlagen, die noch fehlen.

SACHVERHALT
- Art des Vorgangs: [Erwerb von Todes wegen / Schenkung unter Lebenden /
  Zweckzuwendung / unklar]
- Zeitliche Einordnung des auslösenden Ereignisses: [MONAT UND JAHR]; das
  taggenaue Datum bleibt in der Kanzlei
- Kenntniserlangung, je Beteiligtem getrennt: [ROLLE], zeitliche Einordnung:
  [MONAT UND JAHR], liegt sie vor oder nach dem Ereignis: [ANGABE]
- Verfügung von Todes wegen vorhanden: [nein / ja, Testament / ja, Erbvertrag /
  unbekannt]
- Eröffnung durch ein deutsches Gericht, einen deutschen Notar oder einen
  deutschen Konsul: [nein / ja / unbekannt], zeitliche Einordnung:
  [MONAT UND JAHR]
- Verhältnis des Erwerbers zum Erblasser ergibt sich aus der Verfügung:
  [ja / nein / nicht eindeutig]
- Bei Schenkung oder Zweckzuwendung: gerichtlich oder notariell beurkundet:
  [nein / ja / teilweise], zeitliche Einordnung: [MONAT UND JAHR]
- Zahl der Erwerber: [ANZAHL], je Erwerber das Verhältnis nur als Rolle:
  [ANGABEN]
- Zusammensetzung des Erwerbs nach Vermögensarten, ohne Werte:
  Grundbesitz [nein / ja], Betriebsvermögen [nein / ja],
  Anteile an Kapitalgesellschaften [nein / ja], Auslandsvermögen [nein / ja],
  übriges Vermögen [nein / ja]
- Wohnsitz oder gewöhnlicher Aufenthalt der Beteiligten:
  [Inland / Ausland / gemischt]
- Frühere Zuwendungen desselben Zuwendenden dem Grunde nach:
  [keine / vorhanden], zeitliche Einordnung je Zuwendung: [MONAT UND JAHR]
- Bereits erstattete Anzeigen: [keine / vorhanden], zeitliche Einordnung und
  Empfänger: [ANGABEN]
- Mandat umfasst die Erbschaft- und Schenkungsteuer: [ja / nein / noch offen]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Zweig bestimmen – dieser Schritt trägt alle weiteren, weil sich
   Anzeigepflichtige, Ausnahmetatbestand und Anknüpfungspunkt des Fristbeginns
   je Zweig unterscheiden. Ordne den Vorgang zu:
   ZWEIG A – Erwerb von Todes wegen.
   ZWEIG B – Rechtsgeschäft unter Lebenden oder Zweckzuwendung.
   Ist der Vorgang mit "unklar" angegeben oder liegen mehrere Vorgänge vor,
   behandle jeden Vorgang einzeln und ordne ihn gesondert zu. Vermische die
   Zweige in keinem folgenden Schritt.
2. Grundpflicht. Halte fest, dass der Erwerb vom Erwerber dem zuständigen
   Finanzamt schriftlich anzuzeigen ist und dass die Frist an die Kenntnis vom
   Anfall des Erwerbs anknüpft (§ 30 Abs. 1 ErbStG – für [JAHR] verifizieren).
   Nenne die Fristlänge NICHT als Zahl und kein Datum, sondern führe sie als
   nachzuschlagende Größe (Anzeigefrist – für [JAHR] verifizieren) und ergänze:
   "Frist von einem Menschen zu berechnen und im Fristenprogramm zu erfassen."
3. Anzeigepflichtige bestimmen, je Vorgang und je Person einzeln:
   a) Jeder Erwerber ist eigenständig verpflichtet. Bei mehreren Erwerbern legst
      du je Erwerber eine eigene Zeile an; die Anzeige eines Miterwerbers
      entlastet die übrigen nicht. Sage das ausdrücklich.
   b) Nur im ZWEIG B: Zur Anzeige ist auch derjenige verpflichtet, aus dessen
      Vermögen der Erwerb stammt (§ 30 Abs. 2 ErbStG – für [JAHR] verifizieren).
      Übertrage diese Pflicht NICHT auf den Zweig A.
   Benenne je Person, ob die Kanzlei sie überhaupt vertritt, und trenne die
   Beauftragung von der Pflicht.
4. Ausnahmetatbestand – hier verlaufen die beiden Zweige unterschiedlich. Prüfe
   getrennt und übertrage kein Ergebnis vom einen auf den anderen Zweig:
   ZWEIG A (§ 30 Abs. 3 Satz 1 ErbStG – für [JAHR] verifizieren). Die Anzeige
   entfällt nur, wenn ALLE drei Voraussetzungen zusammentreffen:
     (i) der Erwerb beruht auf einer Verfügung von Todes wegen,
    (ii) diese Verfügung wurde von einem deutschen Gericht, einem deutschen
         Notar oder einem deutschen Konsul eröffnet,
   (iii) das Verhältnis des Erwerbers zum Erblasser ergibt sich daraus
         unzweifelhaft.
   Zusätzlich gilt im Zweig A ein Vorbehalt nach Vermögensarten: Gehört zum
   Erwerb Grundbesitz, Betriebsvermögen, ein Anteil an einer Kapitalgesellschaft
   oder Auslandsvermögen, bleibt die Anzeigepflicht bestehen, auch wenn die drei
   Voraussetzungen erfüllt sind. Prüfe die vier Vermögensarten einzeln und
   benenne die für Anteile an Kapitalgesellschaften geltende Einschränkung am
   Gesetzeswortlaut (Wortlaut des Vorbehalts – für [JAHR] verifizieren).
   Bei gesetzlicher Erbfolge ohne Verfügung von Todes wegen ist die Ausnahme
   von vornherein nicht einschlägig; sage das ausdrücklich.
   ZWEIG B (§ 30 Abs. 3 Satz 2 ErbStG – für [JAHR] verifizieren). Die Anzeige
   entfällt, wenn die Schenkung unter Lebenden oder die Zweckzuwendung
   gerichtlich oder notariell beurkundet ist. **Der Vorbehalt nach Vermögensarten
   des Satzes 1 gilt hier NICHT.** Übernimm ihn nicht und behaupte nicht, dass
   die Anzeigepflicht bei beurkundeter Schenkung wegen Grundbesitzes,
   Betriebsvermögens, Anteilen an Kapitalgesellschaften oder Auslandsvermögen
   fortbestehe. Prüfe stattdessen, ob die Beurkundung den gesamten Vorgang
   erfasst oder nur einen Teil, und behandle nicht beurkundete Teile gesondert.
   Ergebnis je Person und Vorgang: (Anzeige erforderlich),
   (Anzeige nach dem Ausnahmetatbestand entbehrlich) oder (nicht entscheidbar).
   Wähle (nicht entscheidbar), sobald eine der Voraussetzungen unbekannt ist,
   und fordere die fehlende Angabe an.
5. Anknüpfungspunkt des Fristbeginns, je anzeigepflichtiger Person einzeln.
   Benenne, an welches Ereignis und an wessen Kenntnis die Frist anknüpft, und
   sage, welche Angabe dafür im Sachverhalt fehlt. Berechne nichts und nenne
   kein Datum. Weise ausdrücklich darauf hin, dass mehrere Erwerber
   unterschiedliche Anknüpfungspunkte haben können.
6. Zuständiges Finanzamt. Benenne, welches Finanzamt die Anzeige entgegennimmt
   und aus welcher Norm sich die Zuständigkeit ergibt. Bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren" und fordere die Klärung als
   Punkt der Rückfrageliste an. Behandle die Frage der persönlichen
   Steuerpflicht bei Auslandsbezug ausschließlich als Vorfrage, die den
   Zuständigkeits- und Umfangsrahmen betrifft, und beurteile sie nicht.
7. Inhalt der Anzeige. Der Inhalt ergibt sich aus § 30 Abs. 4 ErbStG und ist
   dort in sechs Nummern geregelt (Wortlaut und Reihenfolge der sechs Nummern –
   für [JAHR] verifizieren). Lies die sechs Nummern am Gesetzestext ab, übernimm
   sie als Gliederung der Anzeige und markiere jede Angabe, die du nicht sicher
   zuordnen kannst. Halte fest, dass die Anzeige schriftlich zu erstatten ist.
8. Verhältnis zur Steuererklärung. Sage ausdrücklich, dass die Anzeige die
   Erbschaft- oder Schenkungsteuererklärung nicht ersetzt und dass die Erklärung
   gesondert und regelmäßig erst auf Anforderung des Finanzamts abzugeben ist
   (§ 31 ErbStG – für [JAHR] verifizieren).
9. Anzeigen Dritter. Halte fest, dass Anzeigen und Mitteilungen Dritter –
   insbesondere von Gerichten, Notaren, Kreditinstituten und
   Versicherungsunternehmen – die eigene Anzeigepflicht nur in den gesetzlich
   geregelten Fällen entfallen lassen. Benenne die Norm; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
10. Anschließende Pflichten, nur benennen und nicht ausfüllen: frühere
    Zuwendungen desselben Zuwendenden innerhalb eines maßgeblichen Zeitraums
    (Zusammenrechnungszeitraum – für [JAHR] verifizieren), Anzeigepflichten nach
    einem Verstoß gegen Behaltens- und Lohnsummenregelungen bei begünstigtem
    Vermögen sowie laufende Erklärungspflichten des Nachlasses. Nenne dazu keine
    Zahl, keinen Zeitraum als Wert und keine Rechtsfolge als feststehend.

WEITERE ERGEBNISSE
11. Entwurf der Anzeige als strukturierter Text, gegliedert nach den sechs
    Nummern des § 30 Abs. 4 ErbStG, in Sie-Form und sachlich. Setze für jede
    fehlende Angabe "(fehlt – vor Absendung ergänzen)" ein. Übernimm KEINE
    Namen, KEINE Identifikationsnummer, KEINE Steuernummer, KEINE Anschrift,
    KEINEN Sterbeort, KEIN taggenaues Datum und KEINE Grundbuchangabe; setze
    dafür ausnahmslos
    "(von der Kanzlei außerhalb des Werkzeugs einzusetzen)". Trage in das Feld
    für den Wert des Erwerbs nichts ein, sondern "(Wert von der Kanzlei
    einzusetzen; in diesem Prompt wird nicht bewertet)".
12. Rückfrageliste als Tabelle: Nr. | Fehlende Angabe oder Unterlage | Wofür sie
    gebraucht wird | Von wem sie zu beschaffen ist | Antwort (leer).
13. Mandantenanschreiben, Sie-Form, höchstens 250 Wörter: welche Unterlagen
    benötigt werden, dass jeder Erwerber eigenständig verpflichtet ist, dass die
    Anzeige unabhängig davon zu erstatten ist, ob am Ende Steuer anfällt, und
    dass die Bewertung des Erwerbs ein gesonderter Schritt ist. Keine Zusage
    einer Steuerhöhe, keine Beruhigung, kein Freibetrag.
14. Interner Vermerk für die Akte, höchstens 250 Wörter: Zweig, Ergebnis je
    Person, offene Vorfragen, welche Fristen im Raum stehen und wer sie erfasst.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Benenne fehlende Angaben
   je Person einzeln und arbeite mit ausdrücklich benannten Annahmen.
2. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV, also Norm mit Absatz und
   Satz, Erlass mit Datum oder Entscheidung mit Datum und Aktenzeichen, jeweils
   mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine Absätze, keine
   Richtlinien und keine Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Nenne KEINE Frist, KEINEN Freibetrag, KEINE Steuerklasse, KEINEN Steuersatz
   und KEINEN Betrag als feststehenden Wert. Jede solche Größe nur als
   nachzuschlagende Angabe mit dem Zusatz "für [JAHR] verifizieren".
4. Behandle die Anzeigepflicht als eigenständige Pflicht, die unabhängig davon
   besteht, ob der Erwerb am Ende zu einer Steuer führt. Sage das ausdrücklich.
5. Halte die beiden Zweige in jeder Ausgabe getrennt und weise am Ende
   ausdrücklich aus, dass der Vorbehalt nach Vermögensarten nur im Zweig A gilt.
6. ABBRUCHREGEL: Deuten die Angaben zu einem einzelnen Vorgang oder zu einer
   einzelnen Person darauf hin, dass eine abgegebene Erklärung unrichtig war,
   dass eine Selbstanzeige erwogen wird oder dass ein Steuerstrafverfahren
   läuft, arbeite DIESEN Vorgang beziehungsweise DIESE Person nicht weiter ab.
   Gib dafür nur aus: "Ausgesteuert – Prüfung durch einen Berufsträger außerhalb
   des KI-Werkzeugs." Ob eine Anzeigefrist abgelaufen ist, beurteilst du NICHT;
   ein zurückliegendes Ereignisdatum ist kein Abbruchgrund. Liegt das Ereignis
   oder die Kenntniserlangung erkennbar länger zurück, bearbeite den Vorgang
   vollständig und ergänze im Prüfprotokoll: "Fristablauf und eine etwaige
   Berichtigungspflicht nach § 153 AO prüft der Berufsträger; die Anzeige ist
   auch verspätet zu erstatten." Beende die Bearbeitung NICHT; die übrigen
   Vorgänge und Personen bearbeitest du normal weiter und weist die
   ausgesteuerten gesondert aus.

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit"
2. "Zuordnung der Vorgänge": Nr. | Vorgang | Zweig A oder B | zeitliche
   Einordnung des Ereignisses
3. "Prüfprotokoll je Vorgang", Schritte 3 bis 6
4. "Anzeigepflichtige": Person nach Rolle | Vorgang | Ergebnis |
   Anknüpfungspunkt des Fristbeginns | fehlende Angabe
5. "Fristarten mit Rechtsgrundlage"
6. "Inhalt der Anzeige nach den sechs Nummern"
7. "Verhältnis zur Steuererklärung und Anzeigen Dritter": Abgrenzung der Anzeige
   von der Erbschaft- oder Schenkungsteuererklärung nach § 31 ErbStG sowie
   Reichweite der Anzeigen und Mitteilungen Dritter, je mit Norm und dem Zusatz
   "für [JAHR] verifizieren"
8. "Entwurf der Anzeige"
9. "Rückfrageliste"
10. "Mandantenanschreiben (Entwurf)"
11. "Interner Vermerk"
12. "Ausgesteuerte Vorgänge und Personen"
13. "Anschließende Pflichten, die zu terminieren sind"
14. "Was ich nicht sicher weiß"
```

## Anwendung

1. Beim ersten Anruf nur den Sachverhalt aufnehmen und die Fristfrage sofort an den Berufsträger geben. Der Prompt ersetzt diesen Schritt nicht; er strukturiert ihn.
2. Vor dem Prompt klären, ob eine Verfügung von Todes wegen vorliegt und ob sie eröffnet wurde. Das Eröffnungsprotokoll ist die Unterlage, an der der Zweig A entschieden wird – nicht die Erinnerung des Mandanten. In den Prompt gehen nur Monat und Jahr; das taggenaue Datum bleibt in der Akte und wird erst beim Ausfüllen der Anzeige eingesetzt.
3. Bei mehreren Erwerbern je Person eine eigene Zeile führen. Jeder ist eigenständig verpflichtet, und der Anknüpfungspunkt des Fristbeginns kann je Person unterschiedlich sein.
4. Bei Schenkungen den Beurkundungsumfang prüfen. Erfasst die Urkunde nur einen Teil des Vorgangs, bleibt für den nicht beurkundeten Teil die Anzeigepflicht zu prüfen.
5. Fristen im Fristenprogramm erfassen und die Erfassung von einer zweiten Person nachprüfen lassen. Kein Datum aus der KI-Antwort übernehmen.
6. Die Anzeige vervollständigen, Namen und Nummern außerhalb des Werkzeugs einsetzen, vom Berufsträger freigeben lassen und den Absendenachweis zur Akte nehmen. Die Anzeige ist auch dann zu erstatten, wenn die Kanzlei erwartet, dass keine Steuer anfällt.
7. Bewertung des Erwerbs, Verschonung und Erklärung sind gesonderte Arbeitsschritte und werden erst nach der Anzeige aufgesetzt (Fristen und Voraussetzungen – für [JAHR] verifizieren).

## Qualitätssicherung

- **Der Vorbehalt nach Vermögensarten gilt nur im Zweig A.** Grundbesitz, Betriebsvermögen, Anteile an Kapitalgesellschaften und Auslandsvermögen halten die Anzeigepflicht nur beim Erwerb von Todes wegen aufrecht, dem eine eröffnete Verfügung zugrunde liegt (§ 30 Abs. 3 Satz 1 ErbStG). **Für die notariell beurkundete Schenkung nach Satz 2 gilt er nicht** – ein Entwurf, der ihn dort anwendet, ist zu korrigieren (Wortlaut – für [JAHR] verifizieren).
- **Gesetzliche Erbfolge ohne Verfügung ist immer anzuzeigen.** Der Ausnahmetatbestand des Zweigs A setzt eine eröffnete Verfügung von Todes wegen voraus; ohne sie greift er von vornherein nicht.
- **Jeder Miterwerber ist eigenständig verpflichtet**, und bei Rechtsgeschäften unter Lebenden trifft die Pflicht zusätzlich den Zuwendenden (§ 30 Abs. 2 ErbStG). Die Anzeige einer Person entlastet die anderen nicht.
- **Der Prompt bewertet nicht und beurteilt nicht strafrechtlich.** Jede Angabe zu Wert, Freibetrag, Steuerklasse oder Steuerhöhe in der Antwort wird gelöscht; ebenso jede Aussage zu Selbstanzeige oder Hinterziehung.
- **Namen und Identifikationsnummern kommen nicht in das Werkzeug.** Der Vordruck verlangt sie, der Entwurf lässt sie leer; eingesetzt werden sie außerhalb des KI-Werkzeugs (Zone Rot in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch**, hier ausnahmslos mit Nachprüfung durch eine zweite Person. Der Fristbeginn knüpft an die Kenntnis an und ist je Person gesondert festzustellen.
- **Ausgesteuerte Vorgänge sind nicht erledigt.** Eine unrichtige abgegebene Erklärung, eine erwogene Selbstanzeige oder ein Steuerstrafverfahren gehören unverzüglich zum Berufsträger und werden außerhalb des KI-Werkzeugs bearbeitet.
- **Den Fristablauf stellt der Mensch fest, nicht der Prompt.** Ein zurückliegender Erbfall wird bewusst nicht ausgesteuert – der Prompt rechnet keine Fristen und dürfte den Ablauf deshalb gar nicht beurteilen. Ob die Frist des § 30 Abs. 1 ErbStG abgelaufen ist und ob daneben § 153 AO zu prüfen ist, entscheidet der Berufsträger; die Anzeige ist auch verspätet zu erstatten.
- **Taggenaue Daten bleiben in der Kanzlei.** In den Prompt gehen nur Monat und Jahr. Sterbedatum, Beurkundungs- und Kenntnisdatum sind personenbezogene Einzelangaben und machen den Fall in einem kleinen Mandantenbestand identifizierbar; für die Prüfung werden sie nicht gebraucht, weil der Prompt keine Frist berechnet.
- **Erbrechtliche Vorfragen sind nicht Sache der Kanzlei.** Erbquote, Pflichtteil, Ausschlagung und Testamentsauslegung werden anwaltlich geklärt; der Prompt benennt sie nur.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Zweigzuordnung, Personenliste und Fristerfassung nach. Die Anzeige an das Finanzamt und jede Auskunft an den Mandanten gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 30 ErbStG im amtlichen Volltext (gesetze-im-internet.de), insbesondere Abs. 1 (Anzeige durch den Erwerber, drei Monate ab Kenntnis, schriftlich), Abs. 2 (Zuwendender bei Rechtsgeschäften unter Lebenden), Abs. 3 Satz 1 und Satz 2 (Ausnahmen mit dem Vorbehalt nach Vermögensarten allein in Satz 1) und Abs. 4 (Inhalt in sechs Nummern); daneben § 31 ErbStG, die Zuständigkeitsvorschrift des Erbschaftsteuergesetzes, die Anzeigepflichten Dritter sowie DATEV LEXinform. Alle Fristen und Wortlaute am Original nachlesen (Stand – für [JAHR] verifizieren).

## Varianten

- **Nur Schenkung:** „Beschränke dich auf den Zweig B, prüfe den Beurkundungsumfang und stelle Zuwendendem und Erwerber getrennt gegenüber, was jeder anzuzeigen hat."
- **Nur Erbfall mit eröffnetem Testament:** „Beschränke dich auf den Zweig A und arbeite die drei Voraussetzungen sowie die vier Vermögensarten einzeln ab, je mit der Unterlage, aus der sich die Antwort ergibt."
- **Erstkontakt:** „Erzeuge ausschließlich eine Aufnahmeliste für das erste Gespräch mit höchstens zwölf Fragen, ohne rechtliche Einordnung und ohne Fristaussage."
- **Unterlagenanforderung:** „Erzeuge ausschließlich das Anforderungsschreiben an den Mandanten mit den Unterlagen, gegliedert nach Vermögensarten, ohne Wertangaben."
- **Anschluss:** Übertragung von Betriebsvermögen Prompt 92, Grundbesitz in Gesellschaften Prompt 93, Fristenkonzept Prompt 35, Mandantenkommunikation Prompt 11.
