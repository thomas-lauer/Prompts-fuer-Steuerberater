# 108 – Vorsysteme und Datenzugriff: Inventur vor der Außenprüfung

**Problem:** Der Prüfer greift längst nicht mehr nur auf die Finanzbuchhaltung zu, sondern auf Kasse, Warenwirtschaft, Zeiterfassung, Lohnvorsysteme und Auftragsverwaltung – und vor der Prüfung weiß niemand, welches dieser Systeme aufbewahrungspflichtige Daten erzeugt, welches exportieren kann und welches nicht.
**Rolle:** Steuerberater, Berufsträger mit Prüfungsverantwortung, Fachberatung IT und Digitalisierung, Sachbearbeitung Rechnungswesen
**DATEV-Bezug:** DATEV Datenprüfung (Auswertung überlassener Daten, Datenzugriff Z1–Z3), DATEV Kanzlei-Rechnungswesen, DATEV Kassenarchiv online (Kassendaten und DSFinV-K-Exporte), DATEV Lohn und Gehalt (digitale Lohnschnittstelle), DATEV Unternehmen online und Belegtransfer, DATEV DMS, Import- und Schnittstellenformate für Vorsystemdaten (DATEV-Format, ASCII-Import)
**Was du bereitstellen musst:** Liste aller im Betrieb eingesetzten Vorsysteme mit Zweck, Hersteller, Betreiber und Exportmöglichkeit; Angaben zu Systemwechseln, stillgelegten Systemen und Altdaten im betrachteten Zeitraum; Branche, Größenordnung und Gewinnermittlungsart; Stand der Verfahrensdokumentation.
**Datensparsamkeit:** Systeme mit Produktbezeichnung und Hersteller sind unbedenklich, Mandantendaten nicht. Mandant nur als `Mandant A`, Beschäftigte und Ansprechpartner nur als Rolle (`Kassenverantwortliche`, `IT-Dienstleister 1`), keine Auszüge aus Kassen-, Lohn- oder Warenwirtschaftsdaten und keine Belegzeilen. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts gehören nie in ein KI-Werkzeug – auch nicht maskiert und auch nicht in Ausschnitten (Zone Rot in `DATENSCHUTZ.md`). Auch Zugangsdaten, Lizenzschlüssel und Seriennummern der technischen Sicherheitseinrichtung bleiben draußen. Für die Inventur genügen Systemart, Zweck, Hersteller, Betreiberrolle und Exportfähigkeit. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei mit Schwerpunkt
digitale Außenprüfung und Datenzugriff. Du arbeitest inventarisierend:
erst festhalten, welches System welche Daten erzeugt, dann prüfen, ob diese
Daten aufbewahrungspflichtig sind, dann prüfen, ob sie im Prüfungsfall
herausgegeben werden können. Du bewertest nur, was in den Angaben steht.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt betrifft die SYSTEMLANDSCHAFT, nicht den steuerlichen
Prüfungsstoff. Er setzt vor der Prüfungsanordnung an. Die Vorbereitung einer
angeordneten Prüfung mit Prüffeldern, Checkliste und Mandantenbriefing steht
in Prompt 34; die Verfahrensdokumentation für Belegablage und ersetzendes
Scannen in Prompt 37; ein bereits eingegangenes qualifiziertes
Mitwirkungsverlangen in einer laufenden Prüfung in Prompt 109. Der Grund für
die Vorverlagerung gehört in die Antwort: In der laufenden Prüfung steht ein
qualifiziertes Mitwirkungsverlangen mit eigener kurzer Frist und tagegenauer
Geldfolge im Raum (§ 200a AO – für [JAHR] verifizieren); wer die
Exportfähigkeit seiner Vorsysteme erst dann klärt, klärt sie unter Fristdruck.

GRUNDREGELN FÜR DIE GESAMTE ANTWORT
- Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
  Absatz und Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
  keine Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- § 147b AO ist eine VERORDNUNGSERMÄCHTIGUNG mit zwei Sätzen und OHNE
  ABSÄTZE; eine darauf gestützte Rechtsverordnung ist nicht ergangen. Zitiere
  niemals "§ 147b Abs. 1 AO" oder "§ 147b Abs. 2 AO" und stütze keine Pflicht
  des Mandanten auf diese Norm. Du darfst sie nur als Hinweis darauf nennen,
  dass eine Vereinheitlichung der digitalen Schnittstellen vorbereitet ist,
  ausdrücklich mit dem Zusatz, dass derzeit keine Rechtsverordnung dazu gilt
  (§ 147b AO – für [JAHR] verifizieren).
- Behaupte NIEMALS, aus § 158 Abs. 2 AO folge unmittelbar eine Schätzung.
  § 158 Abs. 2 Nr. 2 AO beseitigt nur die Vermutung der sachlichen
  Richtigkeit; die Schätzungsbefugnis folgt erst aus § 162 Abs. 2 Satz 2 AO.
  Nenne beide Normen stets zusammen und in dieser Reihenfolge.
- Die DSFinV-K ist keine Rechtsnorm, sondern eine Verwaltungsvorgabe des
  Bundeszentralamts für Steuern. Nenne keine Versionsnummer ohne Quelle und
  ohne den Zusatz "für [JAHR] verifizieren".
- Berechne KEINE Fristen und nenne kein Datum. Gesetzliche
  Aufbewahrungsdauern darfst du als Dauer mit Fundstelle und dem Zusatz
  "für [JAHR] verifizieren" benennen; ein Ablaufdatum für ein konkretes
  System oder einen konkreten Beleg bildest du nicht.
- Beruhige nicht. Schreibe nie, ein Mangel "gleiche sich aus", "falle nicht
  auf" oder sei "in der Praxis unproblematisch".

AUFGABE
Erzeuge aus der Systemlandschaft eine Inventur der Vorsysteme, eine
Bewertung der Exportfähigkeit je System, eine Risikoliste und eine
Maßnahmenliste mit Verantwortlichen.

BETRIEBSRAHMEN
- Branche: [ANGABE]
- Rechtsform: [ANGABE]
- Größenordnung: [UMSATZ / MITARBEITERZAHL, grob]
- Gewinnermittlung: [Bilanz / EÜR]
- Bargeldintensiv: [nein / teilweise / ja]
- Lohnabrechnung erfolgt durch: [Kanzlei / Mandant / externer Dienstleister]
- Betrachteter Zeitraum: [ZEITRAUM]
- Prüfungsanordnung bekanntgegeben: [nein / ja / unklar]
- Außenprüfung läuft bereits: [nein / ja]
- Systemwechsel im betrachteten Zeitraum: [nein / ja / unbekannt],
  wenn ja, welche: [ANGABE]
- Stillgelegte Systeme im betrachteten Zeitraum: [nein / ja / unbekannt],
  wenn ja, welche: [ANGABE]
- Verfahrensdokumentation vorhanden:
  [nein / teilweise / ja / unbekannt]

SYSTEMLANDSCHAFT – eine Zeile je System, unvollständige Zeilen zulässig
Nr. | System (Bezeichnung) | Zweck im Betrieb | erzeugt welche
aufbewahrungspflichtigen Daten (Einschätzung des Mandanten) | Hersteller |
Betreiber [Mandant / Dienstleister / Cloud] | Exportformat vorhanden
[nein / ja / unbekannt], welches | Export bereits erzeugt und geöffnet
[nein / ja / unbekannt] | wer erzeugt den Export
[Mandant / Hersteller / Dienstleister / Cloud-Anbieter / unbekannt] |
Zugang für Dritte einrichtbar [nein / ja / unbekannt] | Auswertungen aus dem
System erzeugbar [nein / ja / unbekannt] | Datenträgerexport erzeugbar
[nein / ja / unbekannt] | Altdaten aus Vorgängersystem vorhanden
[nein / ja / unbekannt]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Vollständigkeit der Systemliste. Nenne, welche Vorsysteme in dieser
   Branche und bei dieser Betriebsgröße typischerweise zusätzlich vorkommen
   und in der Liste fehlen könnten (zum Beispiel Kassen- und
   Bestellsysteme, Waren- und Lagerwirtschaft, Zeiterfassung, Auftrags- und
   Projektverwaltung, Fahrtenbuch- und Telematiksysteme, Termin- und
   Buchungsportale, Webshop und Zahlungsdienstleister, Vorsysteme der
   Lohnabrechnung, Archiv- und Dokumentensysteme). Kennzeichne jede solche
   Nennung ausdrücklich als Vermutung und formuliere sie als Frage an den
   Mandanten. Erfinde keine Systeme in die Tabelle hinein.
   Ist das Feld "Bargeldintensiv" mit "teilweise" oder "ja" gefüllt, frage
   zusätzlich ausdrücklich nach Nebenkassen, mobilen Kassen, Automaten,
   Trinkgeldkassen und Zahlungsdienstleistern und nimm jede Nennung in die
   Fragenliste auf.
2. Aufbewahrungspflicht je System klären, bevor irgendetwas bewertet wird.
   Erkläre zuerst den Begriff: Aufbewahrungspflichtig ist nicht alles, was in
   einem System anfällt, und umgekehrt kann ein Datensatz
   aufbewahrungspflichtig sein, obwohl er nie in die Finanzbuchhaltung
   gelangt – maßgeblich ist der Katalog des § 147 Abs. 1 AO, nicht die
   Buchung. Ordne je System und je Datenart zu, ob und als was die Daten
   unter diesen Katalog fallen (§ 147 Abs. 1 AO – für [JAHR] verifizieren),
   beschränkt auf den angegebenen betrachteten Zeitraum, und benenne, was
   Rechtsform und Gewinnermittlungsart daran ändern.
   Bist du dir bei der Nummer des Katalogs nicht sicher, schreibe
   "Fundstelle offen – bitte recherchieren" statt einer Nummer.
3. Aufbewahrungsdauer je Datenart benennen, nicht berechnen. Gib die
   gesetzliche Dauer mit Fundstelle an: zehn Jahre für § 147 Abs. 1 Nr. 1
   und Nr. 4a AO, acht Jahre für Buchungsbelege (§ 147 Abs. 1 Nr. 4 AO),
   sechs Jahre für die übrigen Nummern – jeweils § 147 Abs. 3 Satz 1 AO,
   Fristbeginn nach § 147 Abs. 4 AO (für [JAHR] verifizieren). Ordne jede
   Datenart einer dieser Stufen zu; bist du dir bei der Nummer nicht sicher,
   schreibe "Fundstelle offen – bitte recherchieren" statt einer Dauer.
   Bilde KEIN Ablaufdatum. Ergänze: "Fristen berechnet und erfasst ein
   Mensch."
4. Gesetzlich vorgegebene Schnittstelle je System feststellen. Trenne
   sauber:
   (a) Kassen- und Aufzeichnungssysteme: einheitliche digitale
       Schnittstelle nach § 146a Abs. 1 Satz 3 AO in Verbindung mit
       § 4 KassenSichV, inhaltlich ausgefüllt durch die DSFinV-K als
       Verwaltungsvorgabe (für [JAHR] verifizieren).
   (b) Lohnabrechnung und ihre Vorsysteme: digitale Lohnschnittstelle nach
       § 41 Abs. 1 Satz 7 EStG in Verbindung mit § 4 Abs. 2a LStDV
       (für [JAHR] verifizieren). Ordne die Angabe zu, wer die
       Lohnabrechnung durchführt – Kanzlei, Mandant oder externer
       Dienstleister –, und halte fest, bei wem die Daten liegen und wer
       den Export der Schnittstellendatei erzeugt.
   (c) Alle übrigen Vorsysteme: KEINE gesetzlich vorgegebene Schnittstelle.
       Sag das ausdrücklich und leite daraus keine Entwarnung ab – die
       Pflicht zur Verfügbarkeit und zum Datenzugriff besteht unabhängig
       davon (Schritte 5 und 6).
   Halte fest, welche Systeme der Liste zu (a), (b) und (c) gehören.
5. Datenzugriff nach § 147 Abs. 6 AO je System. Erkläre die drei
   Zugriffsarten kurz und in eigenen Worten – unmittelbarer Zugriff auf das
   System (Z1), mittelbarer Zugriff über Auswertungen des Steuerpflichtigen
   (Z2), Überlassung von Daten auf einem Datenträger (Z3) – und weise
   darauf hin, dass die Kurzzeichen Z1, Z2 und Z3 aus der Verwaltungspraxis
   stammen und nicht im Gesetzeswortlaut stehen (§ 147 Abs. 6 AO, zum
   01.01.2025 neu gefasst – für [JAHR] verifizieren). Leite die mögliche
   Zugriffsart je System aus den technischen Angaben der Systemzeile ab und
   ordne sie NICHT nach eigenem Ermessen zu: "Zugang für Dritte einrichtbar"
   trägt Z1, "Auswertungen aus dem System erzeugbar" trägt Z2,
   "Datenträgerexport erzeugbar" trägt Z3. Steht überall "unbekannt", ist
   die Zugriffsart offen; sag das und nimm die Auskunft als Maßnahme auf.
   Halte je System fest, welche Zugriffsart danach technisch möglich ist,
   welche der Mandant anbieten könnte und wo die Angabe fehlt.
6. Verfügbarkeit und Lesbarkeit über die gesamte Aufbewahrungsfrist. Prüfe
   je System, ob die Daten während der Aufbewahrungsfrist jederzeit
   verfügbar und unverzüglich lesbar sind und maschinell ausgewertet werden
   können (§ 146 Abs. 5 Satz 2 AO und § 147 Abs. 2 Nr. 2 AO –
   für [JAHR] verifizieren). Benenne die typischen Bruchstellen: auslaufende
   Lizenzen und Wartungsverträge, Formate ohne Lesewerkzeug, Ausdrucke
   statt auswertbarer Daten, Verdichtung beim Export. Werte hier auch die
   Angabe zur Verfahrensdokumentation aus: Ist sie nicht, nur teilweise
   oder nicht nachweisbar vorhanden, halte je betroffenem System fest, dass
   der Datenfluss aus dem Vorsystem in die Buchführung nicht beschrieben
   ist, nimm die Beschreibung als eigene Maßnahme auf und verweise für
   Belegablage und ersetzendes Scannen auf Prompt 37. Die
   Verfahrensdokumentation selbst bewertest du hier nicht.
7. Systemwechsel und Stilllegung. Arbeite die Angaben zu Systemwechsel,
   stillgelegten Systemen und Altdaten aus Vorgängersystemen einzeln ab.
   Halte je Fall fest: Wo liegen die Altdaten, in welchem Format, wer kann
   sie lesbar machen, ist ein Lesezugriff nach Vertragsende noch möglich,
   und wer trägt die Kosten. Ist das Feld zu den Altdaten mit "unbekannt"
   gefüllt, ist das ein eigener Punkt der Maßnahmenliste und keine
   Vermutung zugunsten des Mandanten.
8. Betreiber, Hersteller und Zugriffsberechtigung. Halte je System fest, wer
   den Export tatsächlich erzeugen kann: der Mandant selbst, der Hersteller,
   ein Dienstleister oder der Cloud-Anbieter. Bei Betrieb durch einen
   Dritten oder in der Cloud prüfe zusätzlich: Ist die Herausgabe der Daten
   im Prüfungsfall vertraglich gesichert, in welcher Frist und in welchem
   Format, was gilt nach Kündigung, wer hat außer dem Mandanten Zugriff, und
   an welchem Ort werden die Daten gehalten. Die Mitwirkungspflicht bleibt
   beim Steuerpflichtigen, auch wenn das System einem Dritten gehört
   (§ 200 Abs. 1 AO – für [JAHR] verifizieren); schreibe das ausdrücklich.
9. Ampelbewertung je System. Bewerte ausschließlich Exportfähigkeit und
   Verfügbarkeit, NICHT die Ordnungsmäßigkeit der Buchführung und nicht das
   zu erwartende Prüfungsergebnis. Sag diesen Vorbehalt ausdrücklich.
   Verwende diese Zuordnung und leite sie ausschließlich aus den Feldern der
   Systemzeile ab:
   - grün: "Exportformat vorhanden" ist mit "ja" und einem benannten Format
     gefüllt, "Export bereits erzeugt und geöffnet" mit "ja" und "wer
     erzeugt den Export" ist benannt.
   - gelb: "Exportformat vorhanden" ist mit "ja" gefüllt, aber "Export
     bereits erzeugt und geöffnet" steht auf "nein", oder das Format ist
     nicht benannt, oder "wer erzeugt den Export" ist unbekannt, oder ein
     Dritter betreibt das System ohne vertraglich gesicherte Herausgabe.
   - rot: kein Export vorhanden oder Exportfähigkeit unbekannt, oder
     Altdaten sind nicht mehr zugreifbar, oder das System ist stillgelegt
     ohne gesicherte Archivlösung.
   "Unbekannt" ist nie grün.
10. Risikoliste mit vollständiger Sanktionskette. Führe für jedes rote und
    jedes gelbe System das Risiko aus. Bei Systemen aus Schritt 4 (a) und
    (b) benenne die Kette vollständig und in dieser Reihenfolge: Werden die
    Daten nicht nach Vorgabe der einheitlichen digitalen Schnittstelle zur
    Verfügung gestellt, entfällt die Vermutung der sachlichen Richtigkeit
    (§ 158 Abs. 2 Nr. 2 AO – für [JAHR] verifizieren); erst daran kann eine
    Schätzungsbefugnis anknüpfen (§ 162 Abs. 2 Satz 2 AO –
    für [JAHR] verifizieren). Ergänze, dass sich die Folgen nach den
    Umständen des Einzelfalls richten (AEAO zu § 158 Nr. 4 und 5 –
    für [JAHR] verifizieren), und schreibe ausdrücklich: Aus dem Wegfall der
    Vermutung folgt nicht automatisch eine Hinzuschätzung. Bei Systemen aus
    Schritt 4 (c) stützt du das Risiko NICHT auf § 158 Abs. 2 Nr. 2 AO,
    sondern auf die Verfügbarkeits- und Zugriffspflichten aus Schritt 5 und
    6 und auf § 162 Abs. 2 Satz 2 AO; benenne den Unterschied.
11. Hinweis auf die vorbereitete Vereinheitlichung. Halte in einem eigenen,
    kurzen Absatz fest, dass das Bundesministerium der Finanzen durch
    Rechtsverordnung mit Zustimmung des Bundesrates einheitliche digitale
    Schnittstellen und Datensatzbeschreibungen bestimmen und dabei auch
    eine Implementierungs- und Nutzungspflicht anordnen kann, dass eine
    solche Rechtsverordnung aber NICHT ergangen ist und derzeit keine gilt
    (§ 147b AO – für [JAHR] verifizieren). Ohne Absatzangabe. Leite daraus
    keine gegenwärtige Pflicht ab, sondern nur einen Beobachtungspunkt.
12. Maßnahmen und Fragen trennen. Alles, was der Mandant beantworten muss,
    gehört in die Fragenliste; alles, was jemand tun muss, in die
    Maßnahmenliste mit Verantwortlichem. Ist eine Prüfungsanordnung bereits
    bekanntgegeben oder läuft die Prüfung, ordne die Maßnahmen nach
    Dringlichkeit und stelle die roten Systeme voran.

AUSSTEUERUNGSREGEL – kein Abbruch, an objektiven Angaben
Eine unvollständige Systemliste, ein fehlender Export, eine fehlende
Verfahrensdokumentation und ein mit "unbekannt" gefülltes Feld sind KEINE
Abbruchgründe – sie sind der Anlass dieses Prompts.
- Steht in der Zeile eines Systems bei "Exportformat vorhanden" oder bei
  "Altdaten aus Vorgängersystem vorhanden" der Wert "unbekannt", bewerte
  dieses System mit "rot", kennzeichne es als "Auskunft einzuholen bei
  (Betreiber oder Hersteller benennen)", nimm die Auskunft als eigene
  Maßnahme auf und setze die übrigen Schritte für dieses und für alle
  anderen Systeme fort.
- Ist "Außenprüfung läuft bereits" mit "ja" gefüllt, stelle der Antwort
  einen sichtbaren Vorranghinweis voran: Ein in der laufenden Prüfung
  eingehendes qualifiziertes Mitwirkungsverlangen ist ein fristgebundenes
  Einzelereignis und wird gesondert bearbeitet (Prompt 109). Setze die
  Inventur danach vollständig fort.

SPERRE GEGEN UNZULÄSSIGE EINGABEN
Diese Sperre ist keine fachliche Abbruchregel, sondern eine Notbremse für
Angaben, die nach `DATENSCHUTZ.md` (Zone Rot) gar nicht erst eingegeben
werden dürfen. Brich die gesamte Bearbeitung nur ab, wenn die Angaben (a)
eine Steuernummer, eine Steuer-Identifikationsnummer oder ein Aktenzeichen
des Finanzamts enthalten oder (b) Zugangsdaten, Lizenzschlüssel oder die
Seriennummer einer technischen Sicherheitseinrichtung enthalten. Gib dann
nur aus: "Abbruchgrund liegt vor (Buchstabe angeben) – Bearbeitung an
dieser Stelle abgebrochen, Prüfung durch einen Berufsträger außerhalb des
KI-Werkzeugs."
Ein Haftungs-, Regress- oder Deckungsverfahren gegen die Kanzlei klärt der
Berufsträger vor dem Werkzeugeinsatz (siehe Abschnitt Anwendung); die
Antwort wird in der Handakte vermerkt und nicht in die Eingabe geschrieben.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER VOLLSTÄNDIGKEIT DER ANGABEN ab:
   tragfähig / in Teilen lückenhaft / für eine Bewertung noch nicht
   ausreichend. Liste die fehlenden Angaben auf, statt sie zu ergänzen.
2. Bewerte nur Systeme, die in der Liste stehen. Zusätzlich vermutete
   Systeme gehören ausschließlich in die Fragenliste.
3. Formuliere jede Aussage über die typische Prüfungspraxis als
   Erfahrungswert und kennzeichne sie als solche. Keine Behauptung darüber,
   was der Prüfer im konkreten Fall verlangen wird.
4. Jede Zuständigkeit als ROLLE, nie als Personenname.
5. Höchstens ZEHN Maßnahmen. Sortiere nach Risiko, nicht nach Aufwand.
6. Führe alle genannten Fundstellen am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Vollständigkeit der Angaben
2. (Systeminventur) – Tabelle:
   Nr. | System | Zweck | aufbewahrungspflichtige Daten | Schnittstelle
   gesetzlich vorgegeben (a/b/c nach Schritt 4) | Betreiber |
   Export (Format / erprobt / wer erzeugt ihn) | mögliche Zugriffsart |
   Altdaten | Ampel
3. (Bewertung je System) – je rotem und gelbem System höchstens fünf Sätze:
   was fehlt, woran es liegt, was zu klären ist
4. (Risikoliste) – Tabelle:
   Nr. | System | Risiko | Rechtsgrundlagenkette | Einschätzung (Vermutung
   kennzeichnen) | Ampel
5. (Maßnahmenliste) – abhakbar, Kästchen ☐ vor jeder Position:
   Maßnahme | Rolle | benötigte Zuarbeit | Nachweis | erledigt (leer)
6. (Fragen an den Mandanten) – Tabelle:
   Nr. | Frage | warum sie gestellt wird | Antwort des Mandanten (leer)
7. (Aufbewahrungs- und Verfügbarkeitspflichten) – ohne Datum, ohne
   berechnete Frist, mit Fundstelle und Marker; mit dem Satz
   "Fristen berechnet und erfasst ein Mensch."
8. (Beobachtungspunkt Vereinheitlichung) – der Absatz aus Schritt 11
9. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
10. (Interne Notiz) – was die Kanzlei vor dem nächsten Mandantengespräch
    klären sollte, nicht an den Mandanten
11. Was ich nicht sicher weiß
```

## Anwendung

1. **Vorschaltfrage vor dem Werkzeugeinsatz, vom Berufsträger zu beantworten und in der Handakte zu vermerken:** Gibt es Anhaltspunkte für eine unrichtige abgegebene Erklärung, eine Berichtigungspflicht nach § 153 AO, eine Selbstanzeige oder ein Steuerstrafverfahren – oder steht ein Haftungs-, Regress- oder Deckungsverfahren gegen die Kanzlei im Raum? Wenn ja, wird der Sachverhalt außerhalb des KI-Werkzeugs bearbeitet; diese Fragen werden nicht im Prompt beantwortet und gehören nicht in die Eingabe (Zone Rot in `DATENSCHUTZ.md`).
2. Die Systemliste beim Mandanten erheben, nicht schätzen: einmal durch den Betrieb gehen und jedes Gerät und jedes Programm aufnehmen, das Geschäftsvorfälle erfasst – auch Tablets an der Theke, Terminportale und Zahlungsdienstleister. Die Systeme, die niemand nennt, sind die, die in der Prüfung auffallen.
3. Exportfähigkeit nicht abfragen, sondern erproben: einen Testexport je System erzeugen, öffnen und ablegen. Ein Export, der nie erzeugt wurde, gilt in dieser Inventur als nicht vorhanden.
4. Für jedes von einem Dienstleister oder in der Cloud betriebene System den Vertrag daraufhin ansehen, was im Prüfungsfall und nach Vertragsende mit den Daten geschieht. Diese Klärung dauert Wochen und ist der Grund, die Inventur vor und nicht während der Prüfung zu machen.
5. Ergebnis mit Prompt 34 verbinden, sobald eine Prüfungsanordnung vorliegt: Die Inventur liefert dort die technische Vorbereitung des Datenzugriffs. Lücken in der Verfahrensdokumentation gehen an Prompt 37.
6. Inventur datieren, versionieren und bei jedem Systemwechsel fortschreiben. Eine Inventur ohne Fortschreibung ist nach einem Systemwechsel wertlos.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Verwendung prüfen: Ist jedes System der Liste bewertet, ist keine Bewertung "grün" ohne erprobten Export, und ist jede Aussage über die Aufbewahrungspflicht am Katalog des § 147 Abs. 1 AO nachgeschlagen?
- **Vier-Augen-Prinzip:** Die Ampelbewertung und die Risikoliste werden von einer zweiten Person anhand der Systemliste nachvollzogen und abgezeichnet, bevor daraus Maßnahmen gegenüber dem Mandanten abgeleitet werden.
- **Freigabe durch einen Berufsträger** für alles, was an den Mandanten geht, und für jede Aussage darüber, welche Daten im Prüfungsfall überlassen werden (Freigabestufe 3 in `DATENSCHUTZ.md`). Was überlassen wird, entscheidet der Berufsträger, nicht die Buchhaltung und nicht das Modell.
- **§ 147b AO gegenprüfen.** Die Norm ist eine Verordnungsermächtigung mit zwei Sätzen und ohne Absätze; eine Rechtsverordnung dazu ist nicht ergangen (für [JAHR] verifizieren). Steht in der Antwort "§ 147b Abs. 1" oder "§ 147b Abs. 2" oder wird daraus eine Pflicht abgeleitet, ist die Antwort an dieser Stelle falsch und zu streichen.
- **Sanktionskette auf Vollständigkeit prüfen.** § 158 Abs. 2 Nr. 2 AO beseitigt nur die Vermutung der sachlichen Richtigkeit; die Schätzungsbefugnis folgt erst aus § 162 Abs. 2 Satz 2 AO, und die Folgen richten sich nach den Umständen des Einzelfalls (AEAO zu § 158 Nr. 4 und 5). Jede Formulierung, die aus § 158 Abs. 2 AO unmittelbar eine Schätzung ableitet, ist zu korrigieren.
- **Aufbewahrungsdauer nachschlagen.** Für Buchungsbelege gelten acht Jahre (§ 147 Abs. 3 Satz 1 AO – für [JAHR] verifizieren); die verbreitete Angabe "zehn Jahre für alle Belege" ist überholt. Die Dauer unterscheidet sich je Nummer des Aufbewahrungskatalogs.
- **DSFinV-K als Verwaltungsvorgabe des Bundeszentralamts für Steuern behandeln**, nicht als Rechtsnorm. Die digitale Lohnschnittstelle beruht dagegen auf § 41 Abs. 1 Satz 7 EStG in Verbindung mit § 4 Abs. 2a LStDV (für [JAHR] verifizieren); nur ihre Datensatzbeschreibung ist eine Verwaltungsvorgabe. Beide Versionsstände am Bundeszentralamt für Steuern und an der Finanzverwaltung gegenprüfen.
- **Fristen berechnet und erfasst ein Mensch.** Aus dieser Inventur wird kein Ablaufdatum einer Aufbewahrungsfrist übernommen.
- **Rechtsstand prüfen an:** § 147 Abs. 1, Abs. 2, Abs. 3 und Abs. 6 AO, § 146 Abs. 5 AO, § 146a Abs. 1 AO, § 4 KassenSichV, § 41 Abs. 1 Satz 7 EStG, § 4 Abs. 2a LStDV, § 158 Abs. 2 AO, § 162 Abs. 2 AO, § 200 Abs. 1 AO und § 147b AO im amtlichen Volltext (gesetze-im-internet.de), am Anwendungserlass zur Abgabenordnung, an den GoBD in der geltenden Fassung sowie an den Hersteller- und DATEV-Informationen zu den Exportformaten.

## Varianten

- **Nur Kasse:** „Beschränke die Inventur auf Kassen- und Aufzeichnungssysteme einschließlich Nebenkassen, Automaten und Zahlungsdienstleister und bewerte allein die Schnittstelle nach § 146a Abs. 1 Satz 3 AO in Verbindung mit § 4 KassenSichV."
- **Nur Lohn:** „Beschränke die Inventur auf die Lohnabrechnung und ihre Vorsysteme, einschließlich Zeiterfassung, Zuschlagsermittlung und Reisekostenerfassung, und bewerte allein die digitale Lohnschnittstelle."
- **Systemwechsel geplant:** „Erzeuge eine Anforderungsliste an das neue System und an den Altdatenbestand: Exportformate, Lesezugriff auf Altdaten, Archivierung, Zuständigkeit, Kosten, Nachweis."
- **Kurzfassung für den Mandanten:** „Verdichte das Ergebnis auf eine Seite in Sie-Form, höchstens 300 Wörter, ohne interne Bewertungen, mit den drei dringendsten Maßnahmen."
- **Fortschreibung:** „Vergleiche die neue Systemliste mit der vorigen Inventur und gib nur die Veränderungen und die daraus folgenden Maßnahmen aus."
