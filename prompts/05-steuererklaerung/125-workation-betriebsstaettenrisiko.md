# 125 – Arbeiten im Ausland: Betriebsstättenrisiko vor der Zusage klären

**Problem:** Ein Mitarbeiter will für einige Wochen aus dem Ausland arbeiten, der Arbeitgeber sagt zu – und niemand hat vorher geprüft, ob dadurch eine Betriebstätte entsteht, ob im Tätigkeitsstaat eine Lohnsteuerpflicht ausgelöst wird und welche Punkte in der Vereinbarung stehen müssen.
**Rolle:** Steuerberater, Lohnsachbearbeitung, Mandantenbetreuung, Berufsträger bei der Freigabe
**DATEV-Bezug:** DATEV Lohn und Gehalt und DATEV LODAS (Lohnsteuerabzug bei Auslandstätigkeit, Bescheinigungswesen), DATEV Arbeitnehmer online (Zulieferung der Angaben zum Vorhaben), DATEV Kanzlei-Rechnungswesen (Folgen einer ausländischen Betriebstätte für Buchführung und Gewinnabgrenzung), DATEV DMS und DATEV Eigenorganisation (Ablage des Freigabebogens und der Nebenabrede, Wiedervorlage bei Verlängerung); Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Zielstaat, Dauer und Lage des Vorhabens in Wochen, Anzahl der betroffenen Mitarbeiter, Funktion und Weisungsbefugnis, Angabe zu Leitungsfunktion, Angabe zu Vertragsanbahnung oder Vertragsabschluss im Zielstaat, Angabe zu Kundenkontakt vor Ort, wer die Räume stellt, Kostenübernahme und Mietvertrag, Vorhandensein eines anderen Arbeitsplatzes im Inland, Anteil der Arbeitszeit im Zielstaat, einmalig oder wiederkehrend, Angabe zum Doppelbesteuerungsabkommen mit dem Zielstaat.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Name des Mitarbeiters, Personalnummer, Geburtsdatum und die Anschrift der Unterkunft im Ausland durch Platzhalter ersetzen (`Mandant A`, `AN 1`); für die Prüfung genügen Zielstaat als Land, Funktion, Dauer in Wochen und die Angaben zu den Räumen. Steuer-Identifikationsnummer, Sozialversicherungsnummer, Ausweis- und Passnummern sowie das Aktenzeichen des Finanzamts gehören nie in ein KI-Werkzeug – auch nicht maskiert und auch nicht in Ausschnitten (Zone Rot in `DATENSCHUTZ.md`). Staatsangehörigkeit, Aufenthaltstitel, Familienverhältnisse und Gesundheitsangaben bleiben draußen, auch wenn sie für Visum oder Sozialversicherung eine Rolle spielen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`; wird das Werkzeug unmittelbar für dieses Einzelmandat eingesetzt, klärt der Berufsträger vorab die Erforderlichkeit einer Mandanteneinwilligung (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und prüfst Vorhaben,
bei denen Beschäftigte vorübergehend aus dem Ausland arbeiten. Du arbeitest
streng nach Prüfschema, in fester Reihenfolge, und redest kein Risiko herbei,
wo die Verwaltung ausdrücklich Entwarnung gibt.

AUFGABE
Erzeuge einen Freigabebogen, der VOR der Zusage des Arbeitgebers ausgefüllt
wird: Ampel je Prüffeld mit Begründung, Liste der vorher zu klärenden Punkte,
Entwurf einer Nebenabrede-Checkliste, Hinweis auf die Felder außerhalb des
Steuerrechts.

BEGRIFF UND EBENEN
Zwei Ebenen sind zu trennen: die innerstaatliche Prüfung nach § 12 AO – dort
lautet die amtliche Schreibweise "Betriebstätte" – und die abkommensrechtliche
Prüfung nach dem Betriebsstättenartikel des konkreten Doppelbesteuerungs-
abkommens. Die Voraussetzungen unterscheiden sich; die Schreibweise sagt
darüber nichts. Benenne bei jeder Aussage, auf welcher Ebene du dich bewegst,
und verwende bei § 12 AO die amtliche Schreibweise.
Eine dritte Ebene prüfst du NICHT: das innerstaatliche Recht des Zielstaats.
§ 12 AO, der AEAO und die BMF-Schreiben binden allein die deutsche Seite.

SPERREN (gelten unabhängig von den Eingaben, kein Abbruch)
- Sozialversicherung: Du entscheidest sie NICHT. Dieser Prompt behandelt die
  steuerliche Seite. Verweise für A1-Bescheinigung, anwendbares Recht und
  Ausnahmevereinbarung auf Prompt 100 und übergib das Feld dorthin.
- Arbeitsrecht, Aufenthalts- und Visarecht und Datenschutz benennst du als zu
  klärende Felder, prüfst sie aber nicht und gibst dazu keine Einschätzung ab.
- Du zählst keine Tage, berechnest keine Frist und nennst kein Datum.

AUSSTEUERUNGSREGEL – kein Abbruch, an einer objektiven Angabe.
Steht im Feld "DBA mit dem Zielstaat" nicht "ja, benannt", steuerst du
Prüfschritt 4 aus und gibst dort nur aus: "Ausgesteuert – ohne benanntes
Abkommen keine abkommensrechtliche Aussage; Prüfung durch einen Berufsträger
am Wortlaut des konkreten Abkommens." Prüfschritt 4 wandert dann als erster
Punkt in die Liste der vor der Zusage zu klärenden Punkte. Die Schritte 1, 2,
3, 5, 6 und 7 arbeitest du normal weiter.

VORHABEN
- Zielstaat: [LAND]
- Dauer: [ANZAHL] Wochen, Lage im Jahr: [QUARTAL ODER MONATE, ohne Datum]
- Anzahl betroffener Mitarbeiter: [ANZAHL]
- Funktion im Unternehmen: [ANGABE]
- Weisungsbefugnis gegenüber anderen Beschäftigten: [ja / nein]
- Leitungsfunktion, also Entscheidungen der Geschäftsleitung oder eines
  abgegrenzten Leitungsbereichs: [ja / nein / unklar]
- Vertragsanbahnung oder Vertragsabschluss im Zielstaat: [nein / ja],
  Art: [ANGABE]
- Kundenkontakt vor Ort: [nein / ja], Art: [ANGABE]
- Wer stellt die Räume: [Wohnung des Mitarbeiters / vom Arbeitgeber
  angemieteter Raum oder Coworking / Räume eines verbundenen Unternehmens /
  Räume eines Kunden / wechselnd]
- Kostenübernahme durch den Arbeitgeber: [ja / nein]
- Mietvertrag über die Räume: [nein / ja], Vertragspartner: [ANGABE]
- Anderer Arbeitsplatz im Inland vorhanden: [ja / nein]
- Anteil der Arbeitszeit im Zielstaat, bezogen auf die vereinbarte
  Arbeitszeit des Mitarbeiters im Bezugszeitraum: [unter 50 % /
  50 % oder mehr / unbekannt], Bezugszeitraum: [ANGABE]
- Wiederkehrend oder einmalig: [einmalig / wiederkehrend / unbefristet]
- DBA mit dem Zielstaat: [ja, benannt / nein / unbekannt], welches: [ANGABE]

PRÜFSCHRITTE – in dieser Reihenfolge, keine Reihenfolge überspringen
1. Verfügungsmacht und feste Geschäftseinrichtung nach § 12 AO.
   Grundlage: § 12 Satz 1 AO – "Betriebstätte ist jede feste
   Geschäftseinrichtung oder Anlage, die der Tätigkeit eines Unternehmens
   dient"; Satz 2 Nr. 1 bis 8 Regelbeispiele.
   Verwaltungsauffassung, wörtlich zitierfähig, AEAO zu § 12 Nr. 4: "Die
   Tätigkeit eines Arbeitnehmers in dessen häuslichem Homeoffice begründet in
   der Regel keine Betriebstätte des Arbeitgebers. Auch abkommensrechtlich
   begründet ein häusliches Homeoffice nach deutscher Anwenderstaatsperspektive
   in der Regel keine Betriebstätte …"
   Halte ausdrücklich fest, dass dies AUCH gilt, wenn der Arbeitgeber die
   Kosten übernimmt, AUCH wenn ein Mietvertrag über die häuslichen Räume
   besteht und AUCH wenn kein anderer Arbeitsplatz gestellt wird. Grund:
   fehlende Verfügungsmacht des Arbeitgebers. Diese drei Angaben allein führen
   deshalb nicht zu Gelb oder Rot.
   Anders zu bewerten sind Räume, über die der Arbeitgeber selbst verfügt
   (angemieteter Raum, Coworking auf seinen Namen, Räume eines verbundenen
   Unternehmens) sowie dauerhaft und gleichbleibend genutzte Räume mehrerer
   Beschäftigter. Zieh dafür die Angaben zu "wer stellt die Räume", "Anzahl
   betroffener Mitarbeiter" und "wiederkehrend oder einmalig" heran.
   Rechtsprechung zur Verfügungsmacht, als Prüfmaterial zu benennen:
   BFH vom 23.05.2002 – III R 8/00, BStBl II S. 512; BFH vom 26.07.2017 –
   III R 4/16, BFH/NV 2018 S. 233; BFH vom 07.06.2023 – I R 47/20.
2. Leitungsfunktion. Der AEAO nimmt Leitungsfunktionen von der Entwarnung
   aus. Nach dem BMF-Schreiben vom 18.06.2026, GZ IV B 2 - S
   1301/01410/007/264, "Grundsätze der Verwaltung für den Betriebsstätten-
   begriff", Rz. 143 können Leitungsfunktionen im Homeoffice eine
   Geschäftsleitungsbetriebstätte nach § 12 Satz 2 Nr. 1 AO begründen.
   Zieh die Angaben zu Funktion, Weisungsbefugnis und Leitungsfunktion heran.
   Steht dort "unklar", ist das Feld Gelb und wandert in die Klärungsliste.
3. Vertreterbetriebsstätte. Prüfe eigenständig, ob der Mitarbeiter im
   Zielstaat Verträge anbahnt oder abschließt oder regelmäßig die
   entscheidende Rolle beim Abschluss spielt. Halte fest, dass dieser Punkt
   praktisch der häufigste echte Risikofall ist und über der Homeoffice-Frage
   regelmäßig übersehen wird. Zieh die Angaben zu Vertragsanbahnung,
   Vertragsabschluss und Kundenkontakt vor Ort heran.
4. Abkommensrechtliche Ebene – nur mit dem konkreten Abkommen.
   Benenne das Abkommen mit dem Zielstaat namentlich und verlange die Prüfung
   an seinem Wortlaut. Das OECD-Musterabkommen (Art. 5 Abs. 1 feste
   Geschäftseinrichtung, Abs. 4 Negativkatalog, Abs. 5 und 6
   Vertreterbetriebsstätte) ist kein unmittelbar geltendes Recht; anwendbar
   ist allein das jeweilige Abkommen (Art. 59 Abs. 2 Satz 1 GG, § 2 Abs. 1 AO),
   und der Musterkommentar ist Auslegungshilfe nur unter Beachtung der
   deutschen Vorbehalte. Arbeite deshalb NICHT ersatzweise mit dem
   Musterabkommen, wenn das Abkommen nicht benannt ist.
   Nach dem BMF-Schreiben vom 18.06.2026, Rz. 145, begründet abkommens-
   rechtlich eine Nutzung zu weniger als 50 % der Arbeitszeit grundsätzlich
   keine Betriebsstätte; zieh dafür die Felder "Anteil der Arbeitszeit im
   Zielstaat" und "Bezugszeitraum" heran und benenne den Bezugszeitraum
   ausdrücklich, statt ihn zu unterstellen.
5. Lohnsteuer. Ob im Zielstaat ein Besteuerungsrecht für den Arbeitslohn
   entsteht, richtet sich nach dem Artikel des konkreten Abkommens zu
   Einkünften aus unselbständiger Arbeit. Er enthält regelmäßig mehrere
   kumulative Voraussetzungen und eine Aufenthalts- oder Tätigkeitsdauerregel,
   die in vielen Abkommen als 183-Tage-Regel bezeichnet wird. Gib weder die
   Zahl noch den Bezugszeitraum als gesichert aus und zähle keine Tage –
   Bezugszeitraum und Zählweise weichen von Abkommen zu Abkommen ab. Verlange
   stattdessen die Prüfung am Wortlaut und benenne, welche Angaben dafür
   erhoben werden müssen. Zieh dafür die Felder "Dauer", "Lage im Jahr" und
   "wiederkehrend oder einmalig" heran und weise darauf hin, dass Aufenthalte
   bei "wiederkehrend" zusammenzurechnen sein können und dass die Lage im Jahr
   je nach Bezugszeitraum des Abkommens über zwei Zeiträume streuen kann.
   Halte zusätzlich die deutsche Seite fest: Der Lohnsteuerabzug durch den
   inländischen Arbeitgeber nach § 38 Abs. 1 Satz 1 Nr. 1 EStG läuft
   unverändert weiter, bis eine Freistellung vorliegt; als Lohnsteuerabzugs-
   merkmal ist nach § 39 Abs. 4 Nr. 5 EStG die Mitteilung vorgesehen, dass der
   Arbeitslohn nach einem Abkommen zur Vermeidung der Doppelbesteuerung von
   der Lohnsteuer freizustellen ist, wenn der Arbeitnehmer oder der
   Arbeitgeber dies beantragt (§ 38 Abs. 1 Satz 1 Nr. 1 und § 39 Abs. 4 Nr. 5
   EStG – für [JAHR] verifizieren). Nimm "Freistellung vom Lohnsteuerabzug und
   die dafür erforderlichen Nachweise klären" als eigenen Punkt in die Liste
   der vor der Zusage zu klärenden Punkte auf. Entscheide nichts davon und
   triff keine Aussage über ein Lohnsteuerverfahren des Zielstaats.
   Ergänze: "Fristen berechnet und erfasst ein Mensch."
6. Sozialversicherung. Gib nur aus: "Übergabe an Prompt 100 (A1 und Tätigkeit
   im Ausland) – in diesem Bogen nicht entschieden." Keine eigene Aussage.
7. Nicht geprüfte Felder. Benenne als offene Felder mit dem Vermerk, wer sie
   klärt: das innerstaatliche Recht des Zielstaats zur Betriebsstätte und zum
   Lohnsteuerverfahren – es entscheidet über das tatsächliche Risiko vor Ort
   und wird hier nicht beurteilt –, ferner Arbeitsrecht (Arbeitsort,
   anwendbares Arbeitsrecht, Arbeitszeit, Unfallversicherungsschutz),
   Aufenthalts- und Visarecht sowie Datenschutz und IT-Sicherheit.

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab und benenne fehlende
   Angaben, statt sie zu erfinden.
2. Ampel je Prüffeld nach diesen Regeln, andere verwendest du nicht:
   grün = nach den benannten Fundstellen und den Angaben des Bogens spricht
   AUS DEUTSCHER SICHT nichts für ein Risiko in diesem Feld; gelb = eine
   erforderliche Angabe fehlt oder steht auf "unklar" beziehungsweise
   "unbekannt"; rot = eine Angabe des Bogens trifft eine der benannten
   Ausnahmen.
   Sämtliche Ampeln beziehen sich ausschließlich auf die deutsche
   Beurteilung. Setze unter JEDE grüne Ampel den Satz: "Das innerstaatliche
   Recht des Zielstaats ist damit nicht geprüft; es kann abweichend
   beurteilen. Klärung im Zielstaat erforderlich."
   Jede Ampel bekommt eine Begründung mit Bezug auf das Feld des Bogens, aus
   dem sie folgt. Ohne Feldbezug keine Ampel.
3. Trenne Feststellung und Vermutung. Jede Vermutung kennzeichnest du als
   Vermutung. Behaupte nicht, wie der Zielstaat entscheiden wird.
4. Nenne zu jeder rechtlichen Aussage die Fundstelle positiv, jeweils mit dem
   Zusatz "für [JAHR] verifizieren", und führe sie am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen". Bist du dir einer Fundstelle nicht
   sicher, schreibe "Fundstelle offen – bitte recherchieren".
5. Kennzeichne Randziffern, Aktenzeichen und Datumsangaben von Verwaltungs-
   anweisungen ausdrücklich als prüfbedürftig; sie ändern sich mit jeder
   Neufassung.
6. Höchstens 700 Wörter für die Ausgabepunkte 3 bis 6 zusammen; die Tabellen
   der Ausgabepunkte 2 und 7 zählen nicht mit.

AUSGABEFORMAT
1. (Eindeutigkeit) – in drei Sätzen.
2. (Freigabebogen) – Tabelle:
   Prüffeld | Ampel | Begründung mit Feldbezug | Fundstelle |
   was daraus folgt
   Die Zeilen entsprechen den Prüfschritten 1 bis 5, in dieser Reihenfolge.
   Die Prüfschritte 6 und 7 bekommen KEINE Ampel; sie erscheinen ausschließlich
   unter Ausgabepunkt 5 als Klärungsbedarf mit Zuständigkeit.
3. (Vor der Zusage zu klären) – nummerierte Liste, je Punkt: was fehlt,
   wer es liefert, warum es vor der Zusage nötig ist.
4. (Nebenabrede-Checkliste für den Arbeitgeber) – Entwurf, abhakbar,
   Kästchen ☐ vor jeder Position, mindestens: Zielstaat und Zeitraum
   ausdrücklich begrenzt | Verlängerung nur nach erneuter Freigabe |
   keine Vertragsanbahnung und kein Vertragsabschluss im Zielstaat |
   kein Kundenbesuch im Namen des Unternehmens ohne vorherige Freigabe |
   keine Anmietung von Räumen auf Namen des Arbeitgebers |
   Meldepflicht des Mitarbeiters bei Änderung der Tätigkeit |
   Mitwirkung bei der A1-Beantragung nach Prompt 100 |
   Widerruf der Zusage bei Änderung der Umstände.
5. (Nicht geprüfte Felder) – innerstaatliches Recht des Zielstaats
   (Betriebsstätte und Lohnsteuerverfahren), Arbeitsrecht, Aufenthalts- und
   Visarecht, Datenschutz und IT-Sicherheit, Sozialversicherung mit Verweis
   auf Prompt 100; je Feld nur der Klärungsbedarf, keine Bewertung.
6. (Offene Punkte) – was für eine belastbare Freigabe noch fehlt.
7. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. **Vorschaltfrage vor dem Werkzeugeinsatz, außerhalb des Werkzeugs:** Der Berufsträger klärt und vermerkt in der Handakte, ob die Tätigkeit im Zielstaat bereits stattgefunden hat und ob deswegen abgegebene Lohnsteuer-Anmeldungen oder Erklärungen unrichtig sein könnten. Trifft das zu, ist der Fall eine Berichtigungssache, gehört nach `DATENSCHUTZ.md` in die Zone Rot und in kein KI-Werkzeug – auch nicht als Ja-Nein-Angabe. Der Bogen wird dann ohne Werkzeug geführt.
2. Den Bogen ausfüllen, bevor der Arbeitgeber zusagt. Nach der Zusage ist die Nebenabrede eine Verhandlung, vorher eine Bedingung.
3. Zielstaat immer als Land angeben und das Abkommen benennen, wenn es bekannt ist. Steht dort „unbekannt", liefert der Prompt bewusst keine abkommensrechtliche Aussage – dieser Punkt wird in der Kanzlei am Abkommenstext geklärt.
4. Die Felder zu den Räumen sorgfältig ausfüllen. Der Unterschied zwischen der Wohnung des Mitarbeiters und einem vom Arbeitgeber angemieteten Coworking-Platz trägt die halbe Prüfung.
5. Vertragsanbahnung und Vertragsabschluss ehrlich beantworten, auch wenn es nur „gelegentliche Gespräche mit Interessenten" sind. Das ist der Punkt, an dem Fälle tatsächlich kippen.
6. Sozialversicherung parallel über Prompt 100 starten; die A1-Beantragung braucht Vorlauf und wird nicht in diesem Bogen entschieden.
7. Freigabebogen und Nebenabrede in der Akte ablegen und mit Wiedervorlage versehen, falls verlängert wird. Eine Verlängerung ist ein neuer Fall, kein Nachtrag.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Den Freigabebogen erstellt eine Person, ein Berufsträger prüft ihn anhand der Angaben des Arbeitgebers und zeichnet ihn ab.** Ohne diese Freigabe geht keine Aussage an den Mandanten; KI-Ergebnisse sind Entwürfe.
- **Fristen und Aufenthaltsdauern berechnet und erfasst ein Mensch.** Das Modell liefert keine Tageszahl und kein Datum (siehe Prompt 35).
- Prüfen, dass die deutsche Lohnsteuerseite benannt ist: Der Abzug nach § 38 Abs. 1 Satz 1 Nr. 1 EStG läuft weiter, bis eine Freistellung vorliegt; das Lohnsteuerabzugsmerkmal nach § 39 Abs. 4 Nr. 5 EStG setzt einen Antrag des Arbeitnehmers oder des Arbeitgebers voraus (für [JAHR] verifizieren). Fehlt dieser Punkt in der Klärungsliste, ist der Bogen unvollständig.
- **Die Entwarnung gilt nur für die deutsche Seite.** § 12 AO, der AEAO und die BMF-Schreiben binden die deutsche Finanzverwaltung; ob der Zielstaat nach seinem innerstaatlichen Recht eine Betriebsstätte annimmt, ist damit nicht beantwortet. Eine Ausgabe, die aus den deutschen Fundstellen eine Entwarnung für den Zielstaat ableitet, ist zu verwerfen; unter jeder grünen Ampel muss der Vorbehalt zum Zielstaat stehen.
- Prüfen, dass die Ausgabe kein Risiko konstruiert, wo der AEAO zu § 12 Nr. 4 entwarnt: Kostenübernahme, Mietvertrag über die häuslichen Räume und ein fehlender anderer Arbeitsplatz führen für sich genommen nicht zu einer Betriebstätte.
- Prüfen, dass die Ausnahme trotzdem sauber herausgearbeitet ist: Leitungsfunktionen im Homeoffice können eine Geschäftsleitungsbetriebstätte nach § 12 Satz 2 Nr. 1 AO begründen (BMF vom 18.06.2026, Rz. 143 – für [JAHR] verifizieren).
- Prüfen, dass die Vertreterbetriebsstätte einen eigenen Abschnitt hat. Fehlt er, ist die Ausgabe unvollständig.
- Prüfen, dass die abkommensrechtliche Ebene nur mit dem konkret benannten Abkommen bearbeitet wurde. Eine Ausgabe, die stattdessen mit dem OECD-Musterabkommen entscheidet, ist zu verwerfen: Das Musterabkommen ist kein unmittelbar geltendes Recht (Art. 59 Abs. 2 Satz 1 GG, § 2 Abs. 1 AO – für [JAHR] verifizieren).
- Aktenzeichen, Datum und Randziffern des BMF-Schreibens vom 18.06.2026, GZ IV B 2 - S 1301/01410/007/264, Rz. 140 bis 146, sowie den Wortlaut des AEAO zu § 12 Nr. 4 vor der Verwendung nachschlagen (für [JAHR] verifizieren).
- Die Prozentangabe aus Rz. 145 – Nutzung zu weniger als 50 % der Arbeitszeit – nicht als eigenständige Freigrenze verwenden; sie betrifft die abkommensrechtliche Ebene und ersetzt Prüfschritt 1 nicht.
- Sozialversicherung nicht in diesem Bogen entscheiden. Zuständig ist Prompt 100 (A1 und Tätigkeit im Ausland).
- Abgrenzung im Bestand: Prompt 100 behandelt A1 und Sozialversicherung, Prompt 07 den Lohn-Sonderfall in der Abrechnung.

## Varianten

- **Mehrere Mitarbeiter im selben Zielstaat:** „Erweitere Prüfschritt 1 um die Frage, ob mehrere Beschäftigte dieselben oder gleichbleibende Räume nutzen, und behandle die Gesamtheit als eigenen Sachverhalt."
- **Verlängerungsantrag:** „Behandle die Verlängerung als neuen Fall, stelle die geänderten Angaben der Erstfreigabe gegenüber und benenne, welche Ampel sich dadurch ändert."
- **Geschäftsführer oder Gesellschafter-Geschäftsführer:** „Setze Leitungsfunktion auf ja, beginne mit Prüfschritt 2 und arbeite zusätzlich heraus, welche Angaben für die Frage des Orts der Geschäftsleitung erhoben werden müssen."
- **Merkblatt für den Arbeitgeber:** „Formuliere aus dem Freigabebogen ein Mandantenschreiben in Sie-Form, höchstens 400 Wörter, ohne Fachbegriffe ohne Erklärung und ohne interne Bewertungen."
