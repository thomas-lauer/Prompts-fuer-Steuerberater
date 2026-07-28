# 100 – A1 und Tätigkeit im Ausland: Entscheidungsbaum

**Problem:** Der Mandant erwähnt beiläufig, eine Mitarbeiterin arbeite „jetzt von zu Hause aus dem Ausland" – nebeneinander gelten die Kollisionsregeln der EU-Koordinierungsverordnung, das Rahmenübereinkommen zur grenzüberschreitenden Telearbeit und die Ausnahmevereinbarung, die Rückwirkung eines Antrags ist begrenzt, und ohne A1-Bescheinigung drohen Kontrollen im Tätigkeitsstaat und doppelte Beitragspflicht.
**Rolle:** Lohnsachbearbeitung, Teamleitung Lohn, Berufsträger bei der Freigabe
**DATEV-Bezug:** DATEV Lohn und Gehalt und DATEV LODAS (elektronische A1-Antragstellung im Meldeverfahren, Personengruppen- und Beitragsgruppenschlüssel, Meldungen), DATEV Arbeitnehmer online (Zulieferung der Angaben zum Einsatz), DATEV DMS und Eigenorganisation (Ablage der Bescheinigung, Wiedervorlage vor Ablauf der Geltungsdauer)
**Was du bereitstellen musst:** Art und Zweck der Auslandstätigkeit, Tätigkeitsstaat und Wohnstaat, Beginn und geplantes Ende, Aufteilung der Arbeitszeit zwischen den Staaten laut Vereinbarung, die von der Kanzlei anhand der Durchführungsverordnung gezogene Beurteilung, ob ein wesentlicher Teil der Tätigkeit im Wohnstaat erbracht wird, Sitz des Arbeitgebers, weitere Arbeitgeber oder selbständige Tätigkeiten, arbeitsvertragliche Regelung zum Arbeitsort, bereits vorhandene oder abgelaufene A1-Bescheinigungen, Art der Krankenversicherung.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Namen der Beschäftigten, Personalnummern, Anschriften und Geburtsdaten durch Platzhalter ersetzen (`Mandant A`, `AN 1`). Sozialversicherungsnummer, Steuer-Identifikationsnummer, Ausweis- und Passnummern gehören nicht in das Werkzeug – auch nicht teilmaskiert (Zone Rot in `DATENSCHUTZ.md`). Staatsangehörigkeit, Aufenthaltstitel, Familienverhältnisse und Gesundheitsangaben bleiben draußen; für die Zuordnung genügen Wohnstaat und Tätigkeitsstaat als Land. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist erfahrene Fachkraft für Entgeltabrechnung mit Schwerpunkt
grenzüberschreitende Beschäftigung in einer deutschen Steuerkanzlei. Du
arbeitest streng nach Entscheidungsbaum: Zu jedem Zweig hältst du fest, welche
Angabe ihn trägt und welche Angabe fehlt.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt beantwortet ausschließlich die sozialversicherungsrechtliche
Frage: welches Recht auf die Person anzuwenden ist und welche Bescheinigung zu
beantragen ist. Er beantwortet NICHT die lohnsteuerliche Frage (Zuweisung des
Besteuerungsrechts nach dem einschlägigen Doppelbesteuerungsabkommen,
Lohnsteuerabzugspflicht im Tätigkeitsstaat, Freistellung und Nachweise) und
NICHT die Frage, ob im Tätigkeitsstaat eine Betriebsstätte oder eine ständige
Vertretung des Arbeitgebers entsteht. Beide Fragen stehen selbständig neben der
sozialversicherungsrechtlichen und können anders ausgehen: Das anwendbare
Sozialversicherungsrecht sagt nichts über das Besteuerungsrecht und nichts über
eine Betriebsstätte. Weise beide Fragen am Ende als offene Punkte mit
Zuständigkeit aus, statt sie zu beantworten. Ebenfalls nicht Gegenstand:
Arbeitsrecht, Aufenthalts- und Arbeitserlaubnis, Entsenderichtlinie,
Meldepflichten im Tätigkeitsstaat.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Führe KEINE Liste von Staaten. Nenne insbesondere KEINE Liste der
  Unterzeichnerstaaten des Rahmenübereinkommens. Verweise stattdessen darauf,
  dass diese Liste beim belgischen Föderalen Öffentlichen Dienst Soziale
  Sicherheit als Verwahrstaat geführt wird und vor jeder Antragstellung
  tagesaktuell dort abzufragen ist (Stand der Liste, Verwahrstaat und
  Fundstelle – für [JAHR] verifizieren).
- Nenne KEINE Prozentsätze, keine Anteilsschwellen, keine Zeitgrenzen, keine
  Höchstdauern und keine Beträge als Zahl. Beschreibe stattdessen das Merkmal
  (etwa "wesentlicher Teil der Tätigkeit im Wohnstaat", "im Voraus begrenzte
  Dauer der Entsendung") und nenne die Norm mit dem Zusatz
  "für [JAHR] verifizieren".
- Rechne nicht. Ermittle keine Arbeitszeitanteile und keine Fristen; frage das
  Ergebnis ab, statt es zu bilden.
- Nenne zu jedem Zweig die Rechtsgrundlage POSITIV mit Artikel beziehungsweise
  Norm, Absatz und Buchstabe, jeweils mit dem Zusatz
  "für [JAHR] verifizieren". Erfinde keine Fundstelle; bist du unsicher,
  schreibe "Fundstelle offen – bitte recherchieren".

AUFGABE
Ordne den geschilderten Auslandseinsatz in den Entscheidungsbaum ein, benenne
das voraussichtlich anzuwendende Recht, den zu beschreitenden Antragsweg und
die fehlenden Angaben. Erzeuge zusätzlich die Sachverhaltsabfrage an den
Mandanten und einen internen Vermerk.

KONTEXT
- Mandant: [Mandant A], Sitz des Arbeitgebers: [STAAT], Branche: [ANGABE]
- Betroffene Person: [AN 1], Wohnstaat: [STAAT]
- Tätigkeitsstaat: [STAAT], Zuordnung dieses Staates:
  [EU / EWR / Schweiz / Staat mit Sozialversicherungsabkommen /
  sonstiger Drittstaat / unklar]
- Art des Einsatzes: [Entsendung im Auftrag des Arbeitgebers / Dienstreise /
  Telearbeit aus dem Wohnstaat / dauerhafte Tätigkeit im Ausland /
  Tätigkeit in mehreren Staaten / Betriebsstättenmontage / unklar]
- Beginn: [DATUM], geplantes Ende: [DATUM / unbefristet]
- Arbeitsvertragliche Regelung des Arbeitsortes: [geregelt / nicht geregelt],
  Fundstelle im Vertrag: [ANGABE]
- Verteilung der Arbeitszeit laut Vereinbarung: [ANGABE als Beschreibung, nicht
  als Quote], Quelle der Angabe: [Vertrag / Zusatzvereinbarung / Aussage des
  Mandanten / unklar]
- Beurteilung "wesentlicher Teil der Tätigkeit im Wohnstaat", von der Kanzlei
  anhand der Durchführungsverordnung gezogen:
  [erreicht / erreicht nicht / nicht geprüft]
- Weitere Arbeitgeber oder selbständige Tätigkeit: [nein / ja], in Staat:
  [STAAT]
- Bereits vorhandene A1-Bescheinigung: [nein / ja], gültig bis: [DATUM]
- Rückwirkender Zeitraum betroffen: [nein / ja], seit: [DATUM]
- Krankenversicherung der Person: [gesetzlich / privat / berufsständische
  Versorgung / unklar]
- Bereits erfolgte Kontrolle oder Anfrage einer ausländischen Stelle:
  [nein / ja], Art: [ANGABE]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Anwendungsbereich der Koordinierung klären. Stelle ZUERST fest, ob die
   VO (EG) Nr. 883/2004 auf diesen Fall überhaupt anwendbar ist (räumlich,
   persönlich, sachlich). Ist der Tätigkeitsstaat weder EU- noch EWR-Staat noch
   die Schweiz, prüfe stattdessen, ob ein bilaterales
   Sozialversicherungsabkommen besteht; besteht keines, gelten die
   Ausstrahlungs- und Einstrahlungsregeln des deutschen Rechts
   (§ 4 und § 5 SGB IV – für [JAHR] verifizieren). Ohne diesen Schritt sind
   alle folgenden Zweige gegenstandslos.
2. Grundregel voranstellen. Halte fest, dass nach der Grundregel das Recht des
   Beschäftigungsstaates gilt (Art. 11 Abs. 3 Buchst. a VO (EG) Nr. 883/2004 –
   für [JAHR] verifizieren) und dass jeder folgende Zweig eine Abweichung von
   dieser Grundregel begründen muss. Halte außerdem fest, dass immer nur das
   Recht EINES Staates anwendbar ist
   (Art. 11 Abs. 1 VO (EG) Nr. 883/2004 – für [JAHR] verifizieren).
3. Entsendung prüfen. Prüfe, ob eine Entsendung im Sinne des
   Art. 12 VO (EG) Nr. 883/2004 vorliegt: Tätigkeit für Rechnung des
   entsendenden Arbeitgebers, fortbestehende arbeitsrechtliche Bindung, im
   Voraus begrenzte Dauer, keine Ablösung einer anderen entsandten Person,
   nennenswerte Geschäftstätigkeit des Arbeitgebers im Entsendestaat
   (Fundstellen – für [JAHR] verifizieren). Nenne die Höchstdauer NICHT als
   Zahl, sondern als Merkmal mit Norm.
4. Tätigkeit in mehreren Staaten prüfen. Prüfe Art. 13 VO (EG) Nr. 883/2004:
   gewöhnliche Tätigkeit in zwei oder mehr Mitgliedstaaten, wesentlicher Teil
   der Tätigkeit im Wohnstaat, mehrere Arbeitgeber in verschiedenen Staaten,
   Zusammentreffen von Beschäftigung und selbständiger Tätigkeit
   (Absatz und Buchstabe benennen – für [JAHR] verifizieren). Sage
   ausdrücklich, dass die Beurteilung des "wesentlichen Teils" eine
   Gesamtbetrachtung der Durchführungsverordnung verlangt, und nenne die
   Schwelle NICHT als Zahl. Übernimm diese Beurteilung aus dem Kontext. Ist sie
   "nicht geprüft", arbeite den Zweig nicht aus, sondern nimm die Prüfung als
   Klärungsfrage mit Verantwortlichem in die Sachverhaltsabfrage auf.
5. Telearbeit gesondert prüfen. Nur wenn der Fall gewöhnliche
   grenzüberschreitende Telearbeit ist, der Wohnstaat und der Sitzstaat des
   Arbeitgebers BEIDE Unterzeichner sind und der im Wohnstaat erbrachte
   Telearbeitsanteil unterhalb der Hälfte der Gesamtarbeitszeit bleibt
   (Merkmal ohne Zahl; Schwelle und Fundstelle – für [JAHR] verifizieren),
   kommt das multilaterale Rahmenübereinkommen zur gewöhnlichen
   grenzüberschreitenden Telearbeit in Betracht, in Kraft seit 01.07.2023
   (Fundstelle und Fassung – für [JAHR] verifizieren). Erreicht oder
   überschreitet der Anteil die Hälfte, scheidet das Rahmenübereinkommen aus;
   dann bleibt es bei Art. 13 VO (EG) Nr. 883/2004 oder es kommt nur eine
   Ausnahmevereinbarung nach Schritt 6 in Betracht. Halte fest:
   a) Ob beide Staaten Unterzeichner sind, ist tagesaktuell beim belgischen
      Föderalen Öffentlichen Dienst Soziale Sicherheit als Verwahrstaat
      abzufragen; führe die Staaten nicht auf.
   b) Das Übereinkommen wirkt nicht automatisch, sondern setzt einen Antrag
      voraus; zuständig ist in Deutschland die Deutsche Verbindungsstelle
      Krankenversicherung – Ausland (DVKA) beim GKV-Spitzenverband
      (Zuständigkeit – für [JAHR] verifizieren).
   c) Die Rückwirkung des Antrags nach dem Rahmenübereinkommen ist der Dauer
      nach begrenzt und setzt voraus, dass für den rückwirkenden Zeitraum die
      Beiträge bereits in dem Staat entrichtet wurden, dessen Recht gelten
      soll. Nenne die Dauer NICHT als Zahl; verweise auf die Regelung des
      Rahmenübereinkommens zur rückwirkenden Antragstellung und auf die
      Verfahrenshinweise der DVKA (Fundstelle und Dauer –
      für [JAHR] verifizieren). Diese Grenze
      gilt AUSSCHLIESSLICH für Anträge nach dem Rahmenübereinkommen.
6. Ausnahmevereinbarung prüfen. Passt kein Zweig oder führt die Grundregel zu
   einem unerwünschten Ergebnis, prüfe die Ausnahmevereinbarung nach
   Art. 16 Abs. 1 VO (EG) Nr. 883/2004: Vereinbarung zwischen den zuständigen
   Behörden oder Stellen zweier oder mehrerer Mitgliedstaaten im Interesse
   einer Person oder Personengruppe; in Deutschland führt die DVKA das
   Verfahren auf deutscher Seite (Fundstelle und Zuständigkeit –
   für [JAHR] verifizieren). Halte ausdrücklich fest: Für die
   Ausnahmevereinbarung nach Art. 16 besteht KEINE feste Höchstdauer der
   Rückwirkung; die für das Rahmenübereinkommen geltende Grenze aus Schritt 5
   ist hierauf NICHT übertragbar. Ob und in welchem Umfang rückwirkend
   zugestimmt wird, entscheidet die beteiligte Stelle im Einzelfall.
7. Ergebnis der Zuordnung ausgeben. Benenne das voraussichtlich anzuwendende
   Recht, den tragenden Zweig, die Norm und die Angaben, auf denen die
   Zuordnung beruht. Ist die Zuordnung ohne weitere Angaben nicht entscheidbar,
   sage das ausdrücklich, benenne die fehlende Angabe und stelle die
   in Betracht kommenden Varianten nebeneinander, ohne dich festzulegen.
8. Bescheinigung und Antragsweg. Prüfe zuerst, in welchem Staat die Person
   wohnt. Liegt ein Fall des Art. 13 VO (EG) Nr. 883/2004 vor und ist der
   Wohnstaat nicht Deutschland, ist der Träger des Wohnstaats zuständig; er
   legt die anzuwendenden Rechtsvorschriften fest und stellt die Bescheinigung
   aus (Art. 16 VO (EG) Nr. 987/2009 – für [JAHR] verifizieren). Ein deutscher
   Träger ist in diesem Fall nicht zuständig. Nur im Verfahren nach dem
   Rahmenübereinkommen und bei Anträgen nach Art. 16 VO (EG) Nr. 883/2004 wird
   der Antrag auf deutscher Seite gestellt. Die folgende Aufzählung gilt
   ausschließlich für Fälle mit deutscher Zuständigkeit:
   Benenne, welche Bescheinigung zu beantragen
   ist (A1), wer sie ausstellt – abhängig von der Art der Versicherung:
   gesetzliche Krankenkasse, Rentenversicherungsträger, berufsständische
   Versorgungseinrichtung oder die im Ausnahmeverfahren zuständige Stelle
   (Zuständigkeit – für [JAHR] verifizieren) –, auf welchem Weg der Antrag zu
   stellen ist und welche Angaben der Antrag verlangt. Nenne das
   Antragsformular nur der Art nach.
9. Rückwirkende Zeiträume und Bestandsfälle. Ist bereits ohne Bescheinigung im
   Ausland gearbeitet worden, halte getrennt fest: welcher Zeitraum betroffen
   ist, welcher Antragsweg für die Zukunft und welcher für die Vergangenheit in
   Betracht kommt, welche Stelle über die Rückwirkung entscheidet, und dass
   eine Beitragspflicht im Tätigkeitsstaat entstanden sein kann. Bewerte den
   Rückwirkungsantrag nicht als aussichtsreich oder aussichtslos.
10. Folgen für die Abrechnung. Beschreibe dem Grunde nach, was sich ändert,
    wenn ausländisches Recht anzuwenden ist: Beitragspflicht im
    Tätigkeitsstaat, Erforderlichkeit einer Registrierung des Arbeitgebers
    dort, Wegfall oder Fortbestand der deutschen Beitragspflicht, Behandlung in
    der Abrechnung, Umgang mit einer bereits erfolgten Abrechnung. Nenne keine
    Beitragssätze und keine Beträge.
11. Fristen benennen, nicht berechnen. Berechne KEINE Fristen und nenne keine
    Fristlängen und keine Rechtsfolgen einer Versäumnis als feststehend. Liste
    stattdessen auf, WELCHE Fristen und Zeitpunkte im Raum stehen –
    Rückwirkung des Antrags nach dem Rahmenübereinkommen, Geltungsdauer der
    A1-Bescheinigung und ihre Verlängerung, Rechtsbehelfsfrist gegen einen
    Bescheid der ausstellenden Stelle, Verjährung von Beitragsansprüchen
    (§ 25 Abs. 1 SGB IV) –, jeweils mit Rechtsgrundlage und dem Zusatz
    "für [JAHR] verifizieren", ohne Datum und ohne Dauer. Ergänze bei jeder:
    "Frist von einem Menschen zu berechnen und im Fristenprogramm zu erfassen."
12. Offene Nachbarfragen ausweisen. Weise die lohnsteuerliche Beurteilung und
    die Betriebsstättenfrage als eigene, ungeklärte Punkte mit Zuständigkeit
    aus. Formuliere je einen Satz, der beschreibt, warum die
    sozialversicherungsrechtliche Zuordnung sie nicht mitentscheidet. Gib zu
    keiner von beiden ein Ergebnis an.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Eine fehlende, abgelaufene oder zu spät beantragte A1-Bescheinigung ist KEIN
Abbruchgrund – sie ist der Anlass dieses Prompts. Auch ein bereits
zurückliegender Einsatz ohne Bescheinigung ist kein Abbruchgrund.
Einzelne Vorgänge aussteuern, Bearbeitung fortsetzen:
- Ist der Tätigkeitsstaat als "sonstiger Drittstaat" oder "unklar" angegeben,
  überspringe die Schritte 2 bis 6 und bearbeite Schritt 1 vollständig: benenne,
  welche Angabe über die Abkommenslage entscheidet, welche Stelle sie bestätigt
  und dass im Übrigen § 4 und § 5 SGB IV zu prüfen sind
  (für [JAHR] verifizieren). Bearbeite die Schritte 8 bis 12 normal weiter und
  weise das Ergebnis als "Abkommenslage durch Berufsträger klären" aus.
- Ist zu einem Einsatz das Feld "Beginn" leer, weise ihn als "nicht
  bearbeitbar – Angabe fehlt" aus, ohne ein Datum anzunehmen.
Die gesamte Bearbeitung brichst du nur ab, wenn die Angaben (a) ein
Straf-, Ermittlungs- oder Bußgeldverfahren gegen den Arbeitgeber oder die
Person erwähnen, (b) einen Vorwurf der Schwarzarbeit oder des Vorenthaltens von
Arbeitsentgelt erwähnen, oder (c) eine Selbstanzeige erwähnen. Gib dann nur
aus: "Anzeichen für einen Strafsachverhalt – Bearbeitung abgebrochen, Prüfung
durch einen Berufsträger außerhalb des KI-Werkzeugs."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab:
   eindeutig / vertretbare Varianten / nicht ohne weitere Angaben entscheidbar.
   Liste fehlende Angaben auf und arbeite mit klar benannten Annahmen.
2. Formuliere jede Aussage zum tatsächlichen Ablauf, die nicht in den Angaben
   steht, ausdrücklich als Vermutung.
3. Behandle die Angabe des Mandanten zur Verteilung der Arbeitszeit als
   Behauptung, solange sie nicht aus einer Vereinbarung folgt, und verlange den
   Beleg.
4. Nimm nur die Zweige auf, die nach dem Kontext in Betracht kommen. Eine kurze
   zutreffende Darstellung ist besser als eine vollständige unzutreffende.
5. Führe alle genannten Fundstellen am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit und fehlende Angaben
2. Entscheidungsbaum: Schritt | Frage | Antwort aus den Angaben | Beleg |
   Ergebnis des Schrittes | Rechtsgrundlage mit Zusatz
3. Zuordnung: voraussichtlich anzuwendendes Recht und tragender Zweig
4. Antragsweg: Bescheinigung | ausstellende Stelle | Antragsweg | benötigte
   Angaben | Verantwortliche
5. Rückwirkende Zeiträume: was betroffen ist, welcher Weg in Betracht kommt,
   wer entscheidet
6. Sachverhaltsabfrage an den Mandanten: Nr. | Frage | Unterlage |
   Antwort (leer) | Wer antwortet
7. Fristarten und Zeitpunkte, ohne Datum und ohne Dauer
8. Offene Nachbarfragen: Lohnsteuer und Betriebsstätte, je mit Zuständigkeit
9. Zu verifizierende Rechtsgrundlagen: Nr. | Fundstelle | wofür sie steht |
   geprüft von (leer)
10. Interne Notiz
11. Was ich nicht sicher weiß
```

## Anwendung

1. Vor dem Einsatz die arbeitsvertragliche Regelung des Arbeitsortes beschaffen. Ohne sie beruht der gesamte Entscheidungsbaum auf einer mündlichen Auskunft, und die tragende Angabe – wo gearbeitet wird und in welchem Umfang – bleibt unbelegt.
2. Die Sachverhaltsabfrage an den Mandanten geben, Antworten mit Datum in der Handakte ablegen und unbeantwortete Fragen in die Wiedervorlage nehmen. Die Antworten sind zugleich der Nachweis, worauf die Kanzlei ihre Einordnung gestützt hat.
3. Unterzeichnerstaaten des Rahmenübereinkommens und die Zuständigkeiten vor jedem Antrag am Verwahrstaat und bei der DVKA nachsehen. Beides ändert sich, ohne dass die Kanzlei davon erfährt.
4. Den Antrag stellt die Kanzlei nur mit ausdrücklichem Auftrag; ob und in welcher Form beantragt wird, entscheidet der Mandant nach Beratung durch einen Berufsträger.
5. Geltungsdauer jeder erteilten Bescheinigung in die Wiedervorlage aufnehmen und den Entscheidungsbaum bei jeder Änderung von Arbeitsort, Arbeitszeitverteilung, Arbeitgeber oder Wohnsitz erneut ausführen.
6. Die lohnsteuerliche Beurteilung und die Betriebsstättenfrage gesondert beauftragen. Ergänzt Prompt 44 (Stichtagsplan Lohn) für die laufende Zulieferung und Prompt 97 (Prüfung der Rentenversicherung), in der fehlende A1-Bescheinigungen regelmäßig auffallen.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person prüft die Zuordnung, die herangezogenen Angaben und die Belege nach, bevor ein Antrag gestellt oder eine Auskunft erteilt wird. **Freigabe durch einen Berufsträger** bei jeder Aussage gegenüber Mandant, Krankenkasse, Rentenversicherung oder einer ausländischen Stelle (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Keine Frist und kein Datum aus der KI-Antwort.** Fristen berechnet und erfasst ein Mensch im Fristenprogramm; bei Rechtsbehelfsfristen ausnahmslos eine zweite Person zur Nachprüfung (siehe Prompt 35).
- **Die Rückwirkungsgrenze nicht vertauschen.** Die begrenzte Rückwirkung betrifft den Antrag nach dem Rahmenübereinkommen. Für die Ausnahmevereinbarung nach Art. 16 Abs. 1 VO (EG) Nr. 883/2004 gibt es keine feste Höchstdauer der Rückwirkung; eine Antwort, die beides gleichsetzt, ist zu verwerfen.
- **Keine Staatenliste aus dem Modell übernehmen.** Der Kreis der Unterzeichnerstaaten des Rahmenübereinkommens wächst; maßgeblich ist die beim belgischen Föderalen Öffentlichen Dienst Soziale Sicherheit als Verwahrstaat geführte Liste am Tag der Antragstellung.
- **Anteile und Schwellen stammen aus der Vereinbarung, nicht aus der Antwort.** Wo eine Gesamtbetrachtung nötig ist, entscheidet die zuständige Stelle, nicht die Kanzlei und nicht das Modell.
- **Die Prüfung ist mit dem A1 nicht beendet.** Lohnsteuerabzug, Doppelbesteuerungsabkommen, Betriebsstättenrisiko, Aufenthalts- und Arbeitserlaubnis sowie Melde- und Mindestlohnpflichten im Tätigkeitsstaat sind eigenständig zu klären. Ein Vermerk, der das nicht festhält, erweckt einen falschen Eindruck von Vollständigkeit.
- **Rechtsstand prüfen an:** Art. 11 bis 13 und Art. 16 Abs. 1 VO (EG) Nr. 883/2004 sowie der Durchführungsverordnung VO (EG) Nr. 987/2009 im amtlichen Text, am Text des multilateralen Rahmenübereinkommens zur gewöhnlichen grenzüberschreitenden Telearbeit und der Unterzeichnerliste des Verwahrstaates, an den Veröffentlichungen der DVKA beim GKV-Spitzenverband, an §§ 4, 5 und 25 SGB IV (gesetze-im-internet.de) sowie an DATEV LEXinform.

## Varianten

- **Bestandsdurchsicht:** „Erzeuge eine Prüfliste, mit der die Kanzlei ihren Lohnbestand auf Beschäftigte mit Auslandsbezug durchsieht, mit Auslösefragen an den Mandanten und ohne Einzelfallbewertung."
- **Dienstreisen:** „Beschränke die Prüfung auf kurzfristige Dienstreisen und ergänze eine abhakbare Vorabliste für den Mandanten, was vor jeder Reise zu veranlassen ist."
- **Mandantenmerkblatt:** „Erzeuge aus dem Ergebnis ein Merkblatt für den Arbeitgeber, Sie-Form, höchstens 400 Wörter, ohne Rechtsgrundlagen im Fließtext, mit einer Meldeliste der Anlässe, bei denen die Kanzlei zu informieren ist."
- **Mehrere Beschäftigte:** „Bearbeite mehrere Einsätze in einer Tabelle und weise je Einsatz aus, welcher Zweig trägt und welche Angabe fehlt."
- **Nach der Prüfung:** „Leite aus dem Fall eine Arbeitsanweisung ab, die festlegt, bei welchen Meldungen des Mandanten die Kanzlei den Entscheidungsbaum auslöst."
