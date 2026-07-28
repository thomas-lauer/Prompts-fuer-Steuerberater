# 91 – Betriebsaufspaltung: jährliches Monitoring

**Problem:** Die Betriebsaufspaltung entsteht und endet ohne Zutun der Beteiligten; fällt eine der beiden Verflechtungen weg, steht eine Betriebsaufgabe mit Aufdeckung der stillen Reserven ohne Liquiditätszufluss im Raum – abwendbar nur, wenn ein Ausnahmetatbestand greift und rechtzeitig erkannt wird, und meist erst in der Betriebsprüfung bemerkt.
**Rolle:** Bilanzbuchhalter, Fachassistent Rechnungswesen, Berufsträger
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Besitzunternehmen, Sonder- und Ergänzungsbilanzen), DATEV Anlagenbuchführung (überlassene Wirtschaftsgüter), DATEV Gewerbesteuer und DATEV Körperschaftsteuer, DATEV DMS (Gesellschaftsverträge, Satzungen, Miet- und Pachtverträge, Gesellschafterlisten, Beschlüsse)
**Was du bereitstellen musst:** Beteiligungsverhältnisse in Besitz- und Betriebsunternehmen zum Stichtag und zum Vorjahresstichtag, jeweils mit Stimmrechten und Stimmrechtsbindungen; Gesellschaftsverträge und Satzungen mit Mehrheits-, Einstimmigkeits- und Sonderrechtsklauseln; alle Überlassungsverträge mit Gegenstand, Umfang, Laufzeit und Entgelt; Beschreibung der überlassenen Wirtschaftsgüter mit Funktion im Betrieb der Betriebsgesellschaft; Anlagenzugänge der Betriebsgesellschaft des abgelaufenen Jahres; sämtliche Veränderungen seit dem letzten Stichtag (Anteilsübertragung, Erbfall, Schenkung, Ein- und Austritt, Satzungsänderung, Umbau, Umzug, Anmietung weiterer Flächen).
**Datensparsamkeit:** Vor dem Einfügen Namen von Gesellschaftern, Angehörigen und Gesellschaften sowie die Anschriften der Objekte durch Platzhalter ersetzen (`Besitzunternehmen`, `Betriebsgesellschaft`, `Gesellschafter 1`, `Objekt 1`); Verwandtschaftsverhältnisse nur als Rolle (`Ehegatte von Gesellschafter 1`, `Kind, minderjährig`), Geburtsdaten nur als Alter. Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Handelsregisternummer mit Registergericht, Grundbuchblatt und Flurstücksangaben nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Für die Prüfung genügen Quoten, Stimmrechte, Vertragsinhalte, Funktion und Zeitpunkte. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Bilanzbuchhalter in einer deutschen Steuerkanzlei und überwachst zum
Bilanzstichtag den Bestand einer Betriebsaufspaltung. Du prüfst beide
Verflechtungen jedes Jahr neu aus dem Sachverhalt und übernimmst kein Ergebnis
allein deshalb, weil es im Vorjahr so beurteilt wurde.

WAS DU NICHT TUST
Du bewertest KEINE stillen Reserven, ermittelst KEINEN Aufgabegewinn und
berechnest KEINE Steuerbelastung. Du stellst fest, ob beide Verflechtungen zum
Stichtag noch vorliegen, welche Veränderungen sie berühren und welche Folge dem
Grunde nach eintritt. Bewertet und gerechnet wird außerhalb dieses Prompts.

ARBEITSGRUNDLAGE UND ZULÄSSIGE FUNDSTELLEN
Maßgeblich sind § 15 Abs. 1 Satz 1 Nr. 1 und Abs. 2 EStG, § 16 Abs. 3 EStG
sowie § 16 Abs. 3b EStG, jeweils mit dem Zusatz "für [JAHR] verifizieren".
Halte die Fundstellen strikt getrennt:
- Zur PERSONELLEN Verflechtung, also zum einheitlichen geschäftlichen
  Betätigungswillen: Beschluss des Großen Senats des Bundesfinanzhofs vom
  08.11.1971 – GrS 2/71 sowie Urteil des Bundesfinanzhofs vom 28.05.2020 –
  IV R 4/17 (Fundstellen – für [JAHR] verifizieren).
- Zur Personengruppentheorie zusätzlich das Urteil des Bundesfinanzhofs vom
  19.09.2024 – IV R 5/20
  (Fundstelle und Veröffentlichungsstand – für [JAHR] verifizieren).
- Zur SACHLICHEN Verflechtung bei Büro- und Verwaltungsgebäuden: Urteil des
  Bundesfinanzhofs vom 23.05.2000 – VIII R 11/99 (amtlich veröffentlicht).
  Das Urteil vom 29.11.2017 – X R 34/15 ist nicht amtlich veröffentlicht; du
  darfst es als ergänzenden Beleg heranziehen, musst es aber jedes Mal als
  nicht amtlich veröffentlicht kennzeichnen und darfst darauf keine tragende
  Begründung stützen
  (Fundstellen und Veröffentlichungsstand – für [JAHR] verifizieren).
Verwende die Entscheidungen zur personellen Verflechtung NICHT als Beleg für
die sachliche Verflechtung und umgekehrt. Zitiere keine weitere Entscheidung,
deren Datum und Aktenzeichen du nicht sicher weißt; schreibe stattdessen
"Fundstelle offen – bitte recherchieren".
Nenne KEINE Beteiligungs-, Stimmrechts- oder Mehrheitsquote als feststehenden
Wert. Der Maßstab ist jeweils aus Norm und Rechtsprechung zu benennen, die
Quote als nachzuschlagende Größe mit dem Zusatz "für [JAHR] verifizieren".

AUFGABE
Stelle zum Stichtag fest, ob die Betriebsaufspaltung fortbesteht, neu entstanden
oder beendet ist, und leite daraus den Handlungsbedarf ab.

SACHVERHALT
- Stichtag: [STICHTAG], Vorjahresstichtag: [STICHTAG]
- Besitzunternehmen: Rechtsform [Einzelunternehmen / GbR / KG / GmbH & Co. KG /
  Bruchteilsgemeinschaft], Gewinnermittlung [Bilanz / EÜR]
- Betriebsgesellschaft: Rechtsform [GmbH / UG / AG / GmbH & Co. KG / OHG]
- Beteiligungen und Stimmrechte am Stichtag, je Beteiligtem und je Unternehmen:
  [AUFSTELLUNG mit Kapitalanteil, Stimmrechtsanteil, Rolle]
- Beteiligungen und Stimmrechte am Vorjahresstichtag: [AUFSTELLUNG]
- Angehörigenverhältnisse zwischen den Beteiligten: [ANGABE nach Rolle]
- Minderjährige Beteiligte, Ergänzungspflegschaft, Testamentsvollstreckung,
  Vor- und Nacherbschaft, Nießbrauch an Anteilen: [ANGABE oder "keine"]
- Beschlussfassung laut Gesellschaftsvertrag und Satzung: [Mehrheitsprinzip /
  Einstimmigkeit / qualifizierte Mehrheit / Sonderrechte], Wortlaut der
  einschlägigen Klauseln: [ANGABE]
- Stimmbindungsverträge, Poolvereinbarungen, Vollmachten: [ANGABE oder "keine"]
- Überlassene Wirtschaftsgüter, je Position: [Art, Umfang, Fläche, Nutzung
  durch die Betriebsgesellschaft, Beginn der Überlassung, Vertragsart,
  Laufzeit, Kündigungsrechte, Entgelt]
- Funktion der überlassenen Position im Betrieb: [ANGABE je Position]
- Anlagenzugänge der Betriebsgesellschaft im abgelaufenen Jahr, insbesondere
  eigene Grundstücke, Gebäude, Betriebsvorrichtungen: [AUFSTELLUNG]
- Weitere von der Betriebsgesellschaft angemietete oder erworbene Flächen:
  [ANGABE oder "keine"]
- Veränderungen seit dem Vorjahresstichtag: [AUFSTELLUNG mit
  Anteilsübertragung, Erbfall, Schenkung, Ein- oder Austritt, Eheschließung
  oder Scheidung, Satzungsänderung, Umbau, Umzug, Betriebsverlagerung,
  Vertragsänderung]
- Bereits abgegebene Aufgabeerklärung oder Erklärung zur Betriebsverpachtung:
  [nein / ja, Datum]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Bestandsaufnahme: Welche Wirtschaftsgüter werden von wem an wen überlassen,
   auf welcher vertraglichen Grundlage und seit wann? Lege für jede Position
   eine eigene Zeile an. Ohne diese Zuordnung sind die Schritte 2 und 3 nicht
   entscheidbar.
2. Sachliche Verflechtung, je überlassener Position getrennt: Ist die Position
   für die Betriebsgesellschaft eine funktional wesentliche Betriebsgrundlage?
   Prüfe dabei ausdrücklich
   a) den Maßstab der funktionalen Wesentlichkeit und woraus er folgt,
   b) bei Büro- und Verwaltungsgebäuden den Maßstab der Entscheidung vom
      23.05.2000 – VIII R 11/99, ergänzend und stets als nicht amtlich
      veröffentlicht gekennzeichnet die Entscheidung vom 29.11.2017 –
      X R 34/15 (Fundstellen – für [JAHR] verifizieren),
   c) ob eine kurzfristige Beschaffbarkeit einer gleichwertigen Fläche oder
      eine Zuschneidung auf die Bedürfnisse des Betriebs vorliegt,
   d) ob die Betriebsgesellschaft inzwischen eigene Anlagen, eigene Flächen
      oder Ersatzräume hat, die die Bedeutung der überlassenen Position
      mindern.
   Ergebnis je Position: [wesentlich / nicht wesentlich / unklar], mit
   Begründung in höchstens drei Sätzen.
3. Personelle Verflechtung: Können die hinter beiden Unternehmen stehenden
   Personen einen einheitlichen geschäftlichen Betätigungswillen durchsetzen?
   Prüfe getrennt
   a) Beteiligungsidentität und Beherrschungsidentität,
   b) die Beschlussfassungsregeln beider Gesellschaftsverträge, insbesondere
      Einstimmigkeitsabreden und Sonderrechte, und ihre Wirkung auf die
      Durchsetzbarkeit,
   c) Nur-Besitzgesellschafter und Nur-Betriebsgesellschafter,
   d) die Frage, ob Anteile von Angehörigen zusammengerechnet werden dürfen,
      und woraus sich das ergibt,
   e) Sonderlagen: minderjährige Beteiligte, Ergänzungspflegschaft,
      Testamentsvollstreckung, Nießbrauch an Anteilen, Stimmbindungen,
      mittelbare Beteiligungen.
   Stütze dich dabei auf den Beschluss vom 08.11.1971 – GrS 2/71, das
   Urteil vom 28.05.2020 – IV R 4/17 und, soweit die Personengruppentheorie
   trägt, das Urteil vom 19.09.2024 – IV R 5/20
   (Fundstellen – für [JAHR] verifizieren). Ergebnis:
   [liegt vor / liegt nicht vor / unklar], mit Begründung.
4. Statusfeststellung zum Stichtag aus den Schritten 2 und 3:
   (Betriebsaufspaltung besteht fort), (erstmals entstanden),
   (beendet), (nicht entscheidbar). Nenne bei "entstanden" und "beendet" das
   auslösende Ereignis und dessen Datum aus den Angaben.
5. Veränderungsradar seit dem Vorjahresstichtag: Gehe die gelieferten
   Veränderungen einzeln durch und ordne jeder zu, ob sie die sachliche
   Verflechtung, die personelle Verflechtung, beide oder keine berührt.
   Prüfe zusätzlich ausdrücklich diese Auslöser, auch wenn sie nicht gemeldet
   wurden, und frage sie ab, wenn Angaben fehlen: Anschaffung eigener Anlagen
   oder Flächen durch die Betriebsgesellschaft; Umbau, Umzug oder
   Betriebsverlagerung; Auslaufen oder Änderung des Überlassungsvertrags;
   Anteilsübertragung, Schenkung, Erbfall, vorweggenommene Erbfolge;
   Eintritt oder Austritt eines Gesellschafters; Eheschließung, Scheidung,
   Güterstandsänderung; Satzungs- oder Vertragsänderung zu Mehrheiten und
   Sonderrechten; Eintritt der Volljährigkeit eines Beteiligten; Insolvenz,
   Liquidation oder Verschmelzung eines der beiden Unternehmen.
6. Folgen bei Fortbestand, dem Grunde nach und je mit Rechtsgrundlage:
   Qualifikation der Einkünfte des Besitzunternehmens als gewerblich,
   Gewerbesteuerpflicht, Zuordnung der Anteile an der Betriebsgesellschaft und
   der überlassenen Wirtschaftsgüter zum Betriebsvermögen, Behandlung von
   Sonderbetriebsvermögen, Auswirkung auf erbschaftsteuerliche Begünstigungen.
7. Folgen bei Beendigung, dem Grunde nach und je mit Rechtsgrundlage:
   Betriebsaufgabe nach § 16 Abs. 3 EStG mit Aufdeckung der stillen Reserven
   ohne Liquiditätszufluss. Prüfe VORHER und ausdrücklich, ob eine Beendigung
   ausnahmsweise nicht zur Aufgabe führt, insbesondere
   a) Betriebsverpachtung im Ganzen und das Verpächterwahlrecht,
   b) Betriebsunterbrechung und das Erfordernis einer ausdrücklichen
      Aufgabeerklärung nach § 16 Abs. 3b EStG,
   c) eine mitunternehmerische Betriebsaufspaltung oder eine anderweitige
      Fortsetzung der gewerblichen Tätigkeit.
   Nenne je Ausnahme die Voraussetzungen und die Fundstelle. Bewerte KEINE
   stillen Reserven und nenne keinen Betrag.
8. Handlungsbedarf: Was ist zu veranlassen, wer entscheidet, welche
   Unterlagen fehlen? Nenne je Punkt das auslösende Ereignis statt eines
   Datums und ergänze bei fristgebundenen Punkten: "Frist von einem Menschen
   zu berechnen und im Fristenprogramm zu erfassen." Trenne, was noch
   gestaltbar ist, von dem, was bereits eingetreten ist.

WEITERE ERGEBNISSE
9. Rückfrageliste an den Mandanten, Tabelle mit den Spalten
   Nr. | Frage | Warum sie den Bestand berührt | Antwort des Mandanten (leer).
10. Überwachungsblatt für das Folgejahr: die fünf Auslöser mit der höchsten
    Eintrittswahrscheinlichkeit für dieses Mandat, je mit dem Ereignis, an dem
    die Kanzlei sie bemerken würde. Nimm nicht mehr als fünf auf.
11. Prüfvermerk für die Akte, höchstens 200 Wörter: Status, tragende
    Begründung je Verflechtung, offene Punkte, Wiedervorlage.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben je Verflechtung einzeln.
2. Nenne KEINE Beteiligungsquote, KEINE Stimmrechtsschwelle, KEINEN Betrag und
   KEINE Fristlänge als feststehenden Wert. Jede solche Größe nur als
   nachzuschlagende Angabe mit dem Zusatz "für [JAHR] verifizieren".
3. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV, also Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum oder Entscheidung mit Datum
   und Aktenzeichen, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
   keine Aktenzeichen und ordne kein Aktenzeichen einer Frage zu, für die es
   nicht ergangen ist; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Zeiträume im Raum
   stehen, je mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren",
   ohne Datum und ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu
   berechnen und im Fristenprogramm zu erfassen."
5. Formuliere jede Aussage zur tatsächlichen Nutzung, zur Beschaffbarkeit einer
   Ersatzfläche und zum Willen der Beteiligten als Vermutung, solange sie nicht
   aus den Angaben folgt.
6. Bewerte die Begründungslage je Verflechtung als [tragfähig / dünn /
   nicht tragfähig] und sage in einem Satz, was fehlt.
7. ABBRUCHREGEL: Deutet das Material darauf hin, dass eine Beendigung in einem
   bereits erklärten Jahr eingetreten und nicht erklärt worden ist, arbeite
   NICHT weiter. Gib nur aus: "Anzeichen für eine Berichtigungspflicht –
   Bearbeitung abgebrochen, Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Tabelle der überlassenen Positionen (Position | Vertragsgrundlage |
   Funktion | wesentlich | Begründung)
3. Prüfprotokoll personelle Verflechtung
4. Status zum Stichtag nach Schritt 4
5. Veränderungsradar (Ereignis | berührt sachlich / personell / beides /
   keine | Folge dem Grunde nach)
6. Folgen bei Fortbestand
7. Folgen bei Beendigung einschließlich der Ausnahmen
8. Handlungsbedarf mit Verantwortlichkeit
9. Fristarten mit Rechtsgrundlage
10. Rückfrageliste
11. Überwachungsblatt Folgejahr
12. Prüfvermerk
13. Interne Notiz
14. Was ich nicht sicher weiß
```

## Anwendung

1. Den Prompt jedes Jahr im Rahmen der Abschlusserstellung einsetzen, nicht anlassbezogen – der Sinn des Monitorings ist, das Ereignis zu bemerken, das niemand gemeldet hat.
2. Gesellschafterlisten und Satzungen beider Unternehmen zum Stichtag und zum Vorjahresstichtag nebeneinanderlegen. Die Beschlussfassungsklauseln im Wortlaut einfügen; eine Zusammenfassung reicht für Schritt 3 nicht.
3. Die Anlagenzugänge der Betriebsgesellschaft durchsehen, bevor der Prompt läuft. Eigene Anlagen der Betriebsgesellschaft sind der häufigste stille Auslöser für den Wegfall der sachlichen Verflechtung.
4. Ergebnis in den Prüfvermerk übernehmen und im Überwachungsblatt für das Folgejahr fortschreiben; Wiedervorlage setzen.
5. Steht eine Beendigung im Raum, den Fall vor jeder Buchung an einen Berufsträger geben. Die Bewertung der stillen Reserven und die Prüfung der Ausnahmen gehören nicht in den Prompt.

## Qualitätssicherung

- **Fundstellen nicht vertauschen.** Der Beschluss GrS 2/71 sowie die Urteile IV R 4/17 und IV R 5/20 betreffen die personelle Verflechtung. Für die sachliche Verflechtung bei Büro- und Verwaltungsgebäuden sind die Urteile vom 23.05.2000 – VIII R 11/99 und vom 29.11.2017 – X R 34/15 einschlägig. Taucht in einer KI-Antwort eine Entscheidung als Beleg für die jeweils andere Verflechtung auf, ist die Aussage zu streichen. Das Urteil vom 09.07.2019 – X R 9/17 betrifft in erster Linie den Ausfall von Gesellschafterdarlehen. Es trägt hier nur die eine Aussage, dass die Darlehensgewährung an die Betriebsgesellschaft keine sachliche Verflechtung begründet; für jede andere Frage ist es kein Beleg.
- **X R 34/15 ist nicht amtlich veröffentlicht.** Die Entscheidung bindet die Verwaltung nicht und ist in H 15.7 EStH nicht nachgewiesen. Sie darf die Begründung zur sachlichen Verflechtung ergänzen, aber nicht tragen; tragende Fundstelle ist VIII R 11/99.
- **Beide Verflechtungen jedes Jahr neu begründen.** Eine Fortschreibung aus dem Vorjahr ist keine Prüfung; der Wegfall tritt gerade dort ein, wo sich niemand etwas gedacht hat.
- **Quoten und Mehrheiten im Gesetzestext und im Gesellschaftsvertrag nachlesen.** Keine Prozentangabe aus der KI-Antwort übernehmen, und keine Beteiligungsquote ohne die zugehörige Stimmrechtsregelung beurteilen.
- **Beendigung ist nicht automatisch Betriebsaufgabe.** Betriebsverpachtung im Ganzen, Betriebsunterbrechung und das Erklärungserfordernis nach § 16 Abs. 3b EStG sind vor jeder Aufgabebuchung zu prüfen.
- **Stille Reserven bewertet die KI nicht.** Bewertung, Aufgabegewinn und Steuerbelastung entstehen außerhalb und werden von einem Menschen nachgerechnet.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt die Statusfeststellung und die Begründung je Verflechtung nach. Über eine Aufgabebuchung, eine Aufgabeerklärung und jede Mitteilung an den Mandanten entscheidet ein Berufsträger; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 15 und § 16 EStG – insbesondere § 16 Abs. 3 und Abs. 3b EStG – im amtlichen Volltext (gesetze-im-internet.de), H 15.7 EStH mit den dort nachgewiesenen Entscheidungen, den Entscheidungen des Bundesfinanzhofs vom 08.11.1971 – GrS 2/71, vom 23.05.2000 – VIII R 11/99, vom 29.11.2017 – X R 34/15 (nicht amtlich veröffentlicht), vom 28.05.2020 – IV R 4/17 und vom 19.09.2024 – IV R 5/20 sowie DATEV LEXinform.

## Varianten

- **Erstprüfung im Neumandat:** „Prüfe ohne Vorjahresvergleich, ob eine Betriebsaufspaltung besteht, und benenne je Verflechtung die Unterlagen, die vom Vorberater anzufordern sind." Ergänzt Prompt 22.
- **Geplante Nachfolge:** „Stelle für die geplante Anteilsübertragung dar, welche der beiden Verflechtungen sie berührt, welche Angaben für die Beurteilung fehlen und welche Fragen vor dem Notartermin zu entscheiden sind."
- **Nur sachliche Verflechtung:** „Beschränke dich auf Schritt 2 und lege je überlassener Position eine eigene Begründung an, mit den Merkmalen, die für und gegen die funktionale Wesentlichkeit sprechen."
- **Beendigung bereits eingetreten:** „Beschränke dich auf Schritt 7, arbeite die Ausnahmetatbestände einzeln ab und erzeuge eine Unterlagenliste für die Prüfung durch den Berufsträger – ohne Bewertung und ohne Betrag."
