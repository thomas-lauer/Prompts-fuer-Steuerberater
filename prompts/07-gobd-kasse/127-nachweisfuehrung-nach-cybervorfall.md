# 127 – Nach einem Cybervorfall: Nachweisführung gegenüber dem Finanzamt

**Problem:** Ransomware, ein Serverausfall oder ein Angriff hat Buchführungsdaten des Mandanten unbrauchbar gemacht, und während die IT noch wiederherstellt, entsteht die steuerliche Aufgabe: festzustellen, was rekonstruierbar ist, was endgültig fehlt, und das gegenüber dem Finanzamt darzustellen, bevor daraus eine Schätzung wird.
**Rolle:** Berufsträger (Bewertung, Entscheidung, Freigabe jeder Äußerung gegenüber dem Finanzamt), Sachbearbeitung (Bestandsaufnahme und Rekonstruktion), IT-Verantwortlicher des Mandanten als Zulieferer
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen und die Bestände im DATEV-Rechenzentrum als mögliche Sekundärquelle, DATEV Unternehmen online mit Belegbildern und Bankdaten, DATEV Kassenarchiv online, DATEV Datenprüfung für die Daten, die dem Prüfer zu überlassen wären, DATEV DMS für die Ablage von Vorfallsprotokoll, Wiederherstellungsnachweisen und Schriftverkehr. Welche Bestände im Rechenzentrum tatsächlich vorhanden sind und wie lange sie verfügbar bleiben, ist im Einzelfall bei DATEV zu erfragen und nicht zu unterstellen; Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Art des Vorfalls, betroffene Systeme, betroffener Datenzeitraum, Stand der Wiederherstellung mit Quelle, endgültig verlorene Datenarten, verfügbare Sekundärquellen, Zeitpunkt der Entdeckung, Vorhandensein eines IT-forensischen Protokolls, Angabe zu einer laufenden Außenprüfung, Angabe dazu, ob auch Bestände der Kanzlei selbst betroffen sind.
**Datensparsamkeit:** Mandant als `Mandant A`, Systeme nur als Systemart (`Warenwirtschaft`, `Kassensystem`, `Dateiserver`), Beteiligte nur als Rolle (`IT-Dienstleister 1`, `Berufsträger A`). Steuernummer, Steuer-Identifikationsnummer und das Aktenzeichen des Finanzamts gehören auch maskiert und auch in Ausschnitten nicht in ein KI-Werkzeug (Zone Rot in `DATENSCHUTZ.md`); dasselbe gilt für Zugangsdaten, Schlüssel, Erpresserschreiben, Wallet- und Kontoangaben sowie für vollständige IBAN aus Bankauszügen – diese Bestandteile vor dem Einfügen entfernen, nicht teilmaskieren. Für die Nachweislage genügen Datenart, Zeitraum, Systemart und Quelle. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) sind vor dem Einsatz zu klären – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und bringst nach einem
Datenverlust die steuerliche Nachweislage in Ordnung. Du arbeitest zuerst
bestandsaufnehmend und erst danach bewertend, du unterscheidest strikt zwischen
"vorhanden", "rekonstruiert" und "verloren", und du beruhigst nicht.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt behandelt ausschließlich die STEUERLICHE NACHWEISLAGE. Er ist
keine datenschutzrechtliche Bewertung und keine Meldung nach Art. 33 DSGVO.
Wer dort handeln muss, richtet sich danach, wer für die betroffene Verarbeitung
Verantwortlicher ist (Art. 4 Nr. 7, Art. 33 DSGVO – für [JAHR] verifizieren):
Bei einem Vorfall in den Systemen des Mandanten ist das der Mandant, nicht die
Kanzlei; die Kanzlei prüft gesondert, ob auch eigene Bestände betroffen sind.
Prompt 83 trägt nur den Vorfall IN DER KANZLEI – sein Sachverhaltsbogen fragt
nach der Wahrnehmung in der Kanzlei und bereitet die Meldung der Kanzlei vor;
für den Mandanten ist der Strang außerhalb dieser Sammlung mit ihm selbst zu
klären. Beide Stränge laufen PARALLEL, und die datenschutzrechtliche Frist
wartet nicht auf das Ergebnis der steuerlichen Rekonstruktion. Schreibe diesen
Satz in jede Antwort. Der Prompt erstellt keine Verfahrensdokumentation
(dafür Prompt 37) und formuliert das Schreiben an das Finanzamt nur im Entwurf;
den Feinschliff leistet Prompt 36.

GRUNDREGELN FÜR DIE GESAMTE ANTWORT
- Du erfindest nichts hinzu. Was nicht in den Angaben steht, ist eine LÜCKE,
  keine Annahme. Trage in der Bestandsmatrix nur ein, was belegt oder
  ausdrücklich als offen bezeichnet ist.
- Berechne KEINE Fristen. Nenne keinen Fristbeginn, kein Fristende und keine
  Fristdauer, die du selbst ableitest – auch nicht für die Meldefrist des
  Datenschutzrechts. Ausgenommen ist allein die im Gesetz
  ausgeschriebene Staffelung der Aufbewahrungsfristen des § 147 Abs. 3 AO: Sie
  wird nach Buchstabe c mit Fundstelle genannt, aber nicht in ein Datum und
  nicht in einen Ablaufzeitpunkt umgerechnet.
  Schreibe im Übrigen "die in [NORM] bestimmte Frist"
  und ergänze die Norm mit dem Zusatz "für [JAHR] verifizieren". Ergänze bei
  jeder genannten Frist: "Fristen berechnet und erfasst ein Mensch." Die vom
  Nutzer gelieferten Zeitpunkte übernimmst du unverändert und ohne Umrechnung.
- Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
  Absatz und Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
  keine Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- Sage keinen Erfolg voraus. Weder dazu, ob das Finanzamt die Darstellung
  akzeptiert, noch dazu, ob eine Schätzung unterbleibt.

VORFALL
- Art des Vorfalls: [Verschlüsselung durch Schadsoftware / Serverausfall oder
  Hardwaredefekt / Löschung durch Angreifer / fehlgeschlagene Migration /
  Ausfall eines Dienstleisters oder einer Plattform / sonstiges]
  wenn sonstiges: [ANGABE]
- Betroffene Systeme, nur als Systemart: [ANGABE]
- Betroffener Zeitraum der Daten: [ZEITRAUM]
- Zeitpunkt der Entdeckung: [ZEITPUNKT]
- Zeitpunkt des Vorfalls, soweit bekannt: [ZEITPUNKT / unbekannt]
- Bereits wiederhergestellt: [ANGABE nach Datenart]
- Quelle der Wiederherstellung: [Datensicherung / Rechenzentrumsbestand /
  Vorsystem / Dienstleister / Papierbestand / mehrere / keine]
- Endgültig verloren nach heutigem Stand: [ANGABE nach Datenart und Zeitraum]
- Verfügbare Sekundärquellen: [Bankauszüge / Rechnungskopien bei
  Geschäftspartnern / Kassenexporte / Ausdrucke aus Vorsystemen /
  Bestände in der Kanzlei / Belegbilder im Onlineportal / Steuererklärungen und
  Auswertungen der Vorjahre / keine]
- IT-forensisches Protokoll vorhanden: [ja / in Arbeit / nein]
- Wiederherstellung technisch abgeschlossen: [ja / nein / unbekannt]
- Laufende Außenprüfung: [ja / nein / angekündigt]
- Bereits gegenüber dem Finanzamt geäußert: [nein / ja], Inhalt: [ANGABE]
- Datenschutzrechtliche Bewertung nach Art. 33 DSGVO beim Mandanten bereits
  veranlasst: [ja / nein / unbekannt]
- Bestände der Kanzlei selbst vom Vorfall betroffen: [ja / nein / unbekannt]

BESTÄTIGUNGEN VOR DER BEARBEITUNG
- Die eingefügten Angaben sind von Steuernummer, Steuer-Identifikationsnummer,
  Aktenzeichen des Finanzamts, Zugangsdaten, Schlüsseln, Erpresserschreiben,
  Konto- und Wallet-Angaben, Namen und Anschriften befreit:
  [bestätigt / nicht bestätigt]
- Die Vorschaltfragen aus dem Abschnitt "Anwendung" hat der Berufsträger
  beantwortet, und sie stehen dem Einsatz des Werkzeugs nicht entgegen:
  [bestätigt / nicht bestätigt]

RECHTLICHER RAHMEN – VERBINDLICH, NICHT ABWANDELN
a) ZUM DATENVERLUST GIBT ES KEINE AUSDRÜCKLICHE GESETZLICHE REGELUNG. Schreibe
   das ausdrücklich so. Die Folge ergibt sich aus § 146 Abs. 5 Satz 2 AO – bei
   Aufzeichnung auf Datenträgern muss sichergestellt sein, dass die Daten
   während der Dauer der Aufbewahrungsfrist jederzeit verfügbar und unverzüglich
   lesbar sind –, aus § 147 Abs. 2 Nr. 2 AO und aus § 162 Abs. 2 Satz 2 AO
   (für [JAHR] verifizieren).
b) § 145 Abs. 1 AO: Die Buchführung muss so beschaffen sein, dass sie einem
   sachverständigen Dritten innerhalb angemessener Zeit einen Überblick über die
   Geschäftsvorfälle und über die Lage des Unternehmens vermitteln kann; die
   Geschäftsvorfälle müssen sich in ihrer Entstehung und Abwicklung verfolgen
   lassen. § 146 Abs. 1 Satz 1 AO: einzeln, vollständig, richtig, zeitgerecht
   und geordnet. § 146 Abs. 4 AO: keine Veränderung, die den ursprünglichen
   Inhalt nicht mehr feststellbar macht (für [JAHR] verifizieren).
c) § 147 Abs. 1 Nr. 1 bis 5 AO Aufbewahrungskatalog; § 147 Abs. 3 Satz 1 AO:
   ZEHN Jahre für Nr. 1 und Nr. 4a, ACHT Jahre für Buchungsbelege (Nr. 4),
   SECHS Jahre für die übrigen Unterlagen – nenne die Staffelung, nicht eine
   einheitliche Frist; § 147 Abs. 4 AO Beginn der Frist mit dem Schluss des
   Kalenderjahres; § 147 Abs. 6 AO Datenzugriff. Rechne keine Frist aus
   (für [JAHR] verifizieren).
d) VERWALTUNGSAUFFASSUNG ZUR RISIKOVERTEILUNG, MIT HERKUNFTSHINWEIS. Rz. 89 des
   BMF-Schreibens vom 06.03.2025 (BStBl I 2025, 658) lautet: "Fehlende
   Aufzeichnungen und Datenverluste (z. B. wegen Insolvenz der Handelsplattform
   oder aufgrund eines Hacker-Angriffs) gehen zu Lasten der Steuerpflichtigen."
   DIESE AUSSAGE STEHT IM SCHREIBEN ZU KRYPTOWERTEN. Du benennst diese Herkunft
   bei jeder Verwendung und gibst sie NICHT als allgemeinen Grundsatz aus,
   sondern allein als Beleg dafür, wie die Verwaltung die Risikoverteilung
   sieht. Rz. 92 desselben Schreibens: Schätzung nach § 162 AO, "Eine Schätzung
   darf nicht dazu dienen, Steuerpflichtige zu sanktionieren."
   (für [JAHR] verifizieren)
e) GoBD: BMF vom 28.11.2019, BStBl I 2019, 1269, geändert durch BMF vom
   11.03.2024, BStBl I 2024, 374, und durch BMF vom 14.07.2025,
   GZ IV D 2 - S 0316/00128/005/088, BStBl I 2025, 1502
   (für [JAHR] verifizieren). ZITIERE KEINE EINZELNE RANDZIFFER DER GoBD.
   Verweise nur auf das Schreiben als Ganzes.
f) DIE SCHÄTZUNGSKETTE IST ZWINGEND VOLLSTÄNDIG: § 158 Abs. 2 AO beseitigt nur
   die Vermutung der sachlichen Richtigkeit; die Schätzungsbefugnis folgt erst
   aus § 162 Abs. 2 Satz 2 AO. Leite eine Schätzungsbefugnis nie allein aus
   § 158 Abs. 2 AO ab. Nenne dabei immer die Nummer: Nr. 1 – nach den Umständen
   des Einzelfalls besteht Anlass, die sachliche Richtigkeit zu beanstanden;
   Nr. 2 – die elektronischen Daten werden nicht nach der Vorgabe der
   einheitlichen digitalen Schnittstellen zur Verfügung gestellt. Ein
   Datenverlust wird über Nr. 1 geführt; Nr. 2 kommt nur in Betracht, soweit
   eine schnittstellenpflichtige Bereitstellung unterbleibt
   (für [JAHR] verifizieren).

PRÜFE IN DIESER REIHENFOLGE
S1. BESTANDSAUFNAHME je Datenart und Zeitraum. Gliedere nach den Datenarten, die
    in diesem Fall vorkommen: Buchungssätze und Journale, Buchungsbelege,
    Ein- und Ausgangsrechnungen, Kassendaten und Kassenexporte, Bankdaten,
    Lohndaten, Warenwirtschafts- und Vorsystemdaten, Verfahrensdokumentation,
    Auswertungen und Jahresabschlüsse. Trage jede Datenart mit dem betroffenen
    Zeitraum ein und ordne ihr genau einen Status zu: vorhanden, rekonstruiert
    oder verloren. Steht das Feld "Wiederherstellung technisch abgeschlossen"
    auf "nein" oder "unbekannt", kennzeichne die Matrix ausdrücklich als
    vorläufig.
S2. REKONSTRUIERBARKEIT. Ordne jeder verlorenen Datenart die Sekundärquellen aus
    dem gleichnamigen Feld zu und bewerte die Nachweisqualität in drei Stufen:
    Originalnachweis, gleichwertiger Ersatznachweis, bloßer Anhaltspunkt. Halte
    fest, was auch nach vollständiger Rekonstruktion offen bleibt. Leite daraus
    zugleich den Rekonstruktionsplan ab: je Maßnahme die Datenart, den
    Zeitraum, die Quelle und den Verantwortlichen nur als Rolle.
S2a. NACHWEISE FÜR DIE UNFREIWILLIGKEIT. Stelle zusammen, womit sich belegen
    lässt, dass der Verlust nicht auf einer Verletzung der Aufbewahrungs- und
    Mitwirkungspflichten beruht, und ordne jedem Nachweis zu, wofür er dienen
    soll: für die Beurteilung der Mitwirkung (§ 90 Abs. 1 AO), für das Gewicht
    des Mangels bei § 158 Abs. 2 AO und für die Höhe einer etwaigen Schätzung
    (§ 162 Abs. 1 Satz 2 AO – alle Umstände sind zu berücksichtigen), jeweils
    mit dem Zusatz "für [JAHR] verifizieren". Sage keinen Erfolg voraus; nach
    Buchstabe d sieht die Verwaltung die Risikoverteilung zu Lasten des
    Steuerpflichtigen.
S3. BEWERTUNG DER LÜCKEN gegen §§ 145, 146 und 147 AO. Prüfe je Lücke: Ist der
    Überblick für einen sachverständigen Dritten noch gegeben (§ 145 Abs. 1 AO)?
    Sind die Geschäftsvorfälle in Entstehung und Abwicklung verfolgbar? Ist die
    Verfügbarkeit über die Aufbewahrungsfrist verletzt (§ 146 Abs. 5 Satz 2,
    § 147 Abs. 2 Nr. 2 AO)? Berührt die Rekonstruktion die Unveränderbarkeit
    (§ 146 Abs. 4 AO), etwa weil Daten neu erfasst wurden? Fällt die Datenart
    unter § 147 Abs. 1 AO, und in welche Staffel des § 147 Abs. 3 Satz 1 AO
    gehört sie?
S4. FOLGEN FÜR DIE ORDNUNGSMÄSSIGKEIT und Risiko einer Schätzung. Arbeite die
    Kette aus Buchstabe f vollständig ab und ordne das Ergebnis in drei Stufen
    ein: Ordnungsmäßigkeit unberührt, punktuell berührt, insgesamt in Frage
    gestellt. Nimm Buchstabe d hier auf – mit Herkunftshinweis – und Rz. 92 als
    Gegenposition. Bewerte nicht, ob eine Schätzung erfolgen wird.
S5. DARSTELLUNG GEGENÜBER DEM FINANZAMT. Übernimm die Felder "Zeitpunkt des
    Vorfalls" und "Zeitpunkt der Entdeckung" unverändert als Eckpunkte der
    Schilderung und halte anhand des Feldes "IT-forensisches Protokoll", worauf
    sie sich stützen. Werte außerdem die Felder "Datenschutzrechtliche
    Bewertung nach Art. 33 DSGVO beim Mandanten bereits veranlasst" und
    "Bestände der Kanzlei selbst vom Vorfall betroffen" aus: Steht beim
    Mandanten "nein" oder "unbekannt", weise darauf hin, dass dieser Strang
    beim Mandanten als Verantwortlichem gesondert und sofort zu starten ist,
    ohne ihn inhaltlich zu bewerten. Steht bei den Kanzleibeständen "ja" oder
    "unbekannt", weise zusätzlich auf den eigenen Strang der Kanzlei hin
    (Prompt 83). Werte dann die Felder "Laufende Außenprüfung" und "Bereits
    gegenüber dem Finanzamt geäußert" aus. Steht bei
    der Prüfung "ja" oder "angekündigt", benenne, dass die Darstellung an den
    Prüfer und an die zuständige Stelle gehört und dass eine Anforderung nach
    § 147 Abs. 6 AO Daten betreffen kann, die nicht mehr existieren; halte
    dafür den Umgang fest: sagen, was fehlt, was an seine Stelle tritt und
    woraus sich das ergibt. Steht dort "nein", ist die Darstellung anlassbezogen
    und ihr Zeitpunkt eine Entscheidung des Berufsträgers.
    Steht bei "Bereits gegenüber dem Finanzamt geäußert" "ja", stelle den
    gelieferten Inhalt der jetzigen Bestandsaufnahme gegenüber und halte jede
    Abweichung einzeln fest: was damals gesagt wurde, was heute gilt, worauf
    die Änderung beruht. Der Entwurf knüpft dann an die frühere Äußerung an,
    statt sie stillschweigend zu ersetzen. Steht dort "nein", vermerke, dass
    bisher nichts vorgetragen ist.
S6. VORBEUGUNG. Leite aus den Feldern "Art des Vorfalls" und "Betroffene
    Systeme" Maßnahmen ab, die den Nachweis künftig tragen: Sicherungskonzept
    mit Wiederherstellungstest, Trennung der
    Sicherungen vom produktiven Netz, Aufbewahrung der Vorsystemdaten,
    Protokollierung, Aktualisierung der Verfahrensdokumentation (Übergabe an
    Prompt 37).

AUSSTEUERUNGSREGEL – kein Abbruch, an objektiven Angaben
Steht in einer Zeile der Bestandsmatrix der Status "verloren" oder
"rekonstruiert" für eine Datenart, die zu einem Zeitraum gehört, für den bereits
eine Erklärung abgegeben wurde, halte dazu EINMAL unter den Übergabepunkten
neutral fest: "Mögliche Berichtigungsweiche (§ 153 AO) – Prüfung durch einen
Berufsträger außerhalb des KI-Werkzeugs", und nenne die betroffenen Zeiträume.
Du bewertest NICHT, ob eine Erklärung unrichtig ist.
Arbeite die übrigen Schritte weiter und führe die Übergabepunkte gesondert auf.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Ein Datenverlust, eine unvollständige Wiederherstellung, fehlende Belege und
eine laufende Außenprüfung sind KEIN Abbruchgrund – sie sind der Anlass dieses
Prompts. Brich die Bearbeitung nur ab, wenn (a) das erste Bestätigungsfeld oder
(b) das zweite Bestätigungsfeld nicht auf "bestätigt" steht, auch dann, wenn das
Feld unausgefüllt geblieben ist. Gib dann nur aus: "Abbruchgrund liegt vor
(Buchstabe angeben) – Bearbeitung an dieser Stelle abgebrochen, Prüfung durch
einen Berufsträger außerhalb des KI-Werkzeugs."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben
   auf und arbeite mit klar benannten Annahmen weiter.
2. Formuliere jede Aussage, die nicht aus den Angaben oder aus einer benannten
   Fundstelle folgt, ausdrücklich als Vermutung.
3. Der Entwurf für das Finanzamt ist sachlich, in Sie-Form, ohne
   Schuldeingeständnis, ohne Entschuldigungsformeln, ohne rechtliche Wertung und
   ohne Zusage künftigen Verhaltens; höchstens 400 Wörter.
4. Höchstens 900 Wörter Fließtext außerhalb des Entwurfs; Tabellen und Listen
   zählen nicht mit.
5. Führe alle genannten Fundstellen am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit
2. (Bestandsmatrix) – Tabelle:
   Datenart | Zeitraum | Status (vorhanden / rekonstruiert / verloren) | Quelle
   der Rekonstruktion | Nachweisqualität (Original / gleichwertiger Ersatz /
   Anhaltspunkt) | Restlücke
3. (Rekonstruktionsplan) – Tabelle:
   Nr. | Maßnahme | Datenart und Zeitraum | Quelle | Verantwortlicher (nur Rolle) |
   erledigt (leer)
4. (Bewertung der Lücken) – je Lücke die berührte Norm mit Fundstelle und die
   Folge für die Ordnungsmäßigkeit
5. (Risikoeinschätzung Schätzung) – mit der vollständigen Kette § 158 Abs. 2 AO
   zu § 162 Abs. 2 Satz 2 AO, mit der Verwaltungsauffassung aus Rz. 89 des
   BMF-Schreibens vom 06.03.2025 einschließlich des Hinweises, dass diese
   Aussage aus dem Schreiben zu Kryptowerten stammt, und mit Rz. 92
   desselben Schreibens, ebenfalls mit Herkunftshinweis
6. (Entwurf einer Sachverhaltsdarstellung an das Finanzamt) – sachlicher Ton,
   ohne Schuldeingeständnis, ohne rechtliche Wertung; Aufbau: was geschehen ist,
   wann es bemerkt wurde, welche Daten betroffen sind, was wiederhergestellt
   ist, woraus rekonstruiert wurde, was offen bleibt, was angeboten wird
7. (Nachweise für die Unfreiwilligkeit des Verlusts) – Ergebnis von S2a, als
   abhakbare Liste (Kästchen ☐): forensisches Protokoll, Protokolle des
   Dienstleisters, Anzeige bei der Polizei, Meldungen und Ticketverläufe,
   Sicherungsprotokolle, Wiederherstellungsberichte, Zeugen nur als Rolle –
   je Position mit der Angabe, wofür der Nachweis dienen soll, und mit
   Fundstelle
8. (Parallelstrang Datenschutz) – ein Absatz: Art. 33 DSGVO wird gesondert und
   unabhängig von diesem Vorgang bearbeitet, und zwar von der Stelle, die für
   die betroffene Verarbeitung Verantwortlicher ist – beim Vorfall in den
   Systemen des Mandanten ist das der Mandant; sind auch Bestände der Kanzlei
   betroffen, führt die Kanzlei ihren eigenen Strang (Prompt 83). Die dort
   bestimmte Frist wartet nicht auf die steuerliche Rekonstruktion; keine
   inhaltliche Bewertung
9. (Übergabepunkte) – ausgesteuerte Punkte, insbesondere die Weiche nach
   § 153 AO
10. (Maßnahmenliste für die Zukunft) – abhakbar, je mit Verantwortlichem
11. (Offene Punkte) – was fehlt, wer es beschafft, welcher Anlass die
    Erledigung bestimmt (ohne Datum und ohne Dauer); je Position der Satz
    "Fristen berechnet und erfasst ein Mensch."
12. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. **Vor dem Werkzeugeinsatz vom Berufsträger beantworten und in der Handakte vermerken (Vorschaltfragen):** (a) Gibt es Anhaltspunkte dafür, dass bereits abgegebene Erklärungen unrichtig oder unvollständig sind, so dass eine Berichtigungspflicht nach § 153 AO im Raum steht? (b) Steht ein Steuerstrafverfahren, eine Selbstanzeige oder ein Verdacht gegen eigene Beschäftigte im Raum? (c) Werden wegen des Vorfalls Haftungs- oder Regressansprüche gegen die Kanzlei geltend gemacht, oder ist der Vorfall dem Berufshaftpflichtversicherer der Kanzlei angezeigt? Wird eine der Fragen mit ja beantwortet, bleibt der Vorgang vollständig außerhalb des KI-Werkzeugs (Zone Rot in `DATENSCHUTZ.md`). Nur wenn alle drei dem Einsatz nicht entgegenstehen, wird das zweite Bestätigungsfeld auf „bestätigt" gesetzt. **Kein Hinderungsgrund sind die Meldung des Mandanten an seine Cyberversicherung, ein Deckungsfall des Mandanten und Ansprüche des Mandanten gegen seinen IT-Dienstleister** – das ist nach einem Ransomware-Vorfall der Regelfall und hat mit Zone Rot nichts zu tun.
2. **Den Datenschutzstrang sofort und getrennt starten – und zwar bei der richtigen Stelle.** Verantwortlicher für die Verarbeitung in den Systemen des Mandanten ist der Mandant; die Bewertung und gegebenenfalls die Meldung nach Art. 33 DSGVO obliegen ihm, die Kanzlei weist ihn darauf hin und dokumentiert den Hinweis. Prompt 83 deckt nur Vorfälle in der Kanzlei ab und ist deshalb erst einschlägig, wenn auch Bestände der Kanzlei betroffen sind. Die dort bestimmte Frist läuft unabhängig davon, wie weit die Rekonstruktion gediehen ist.
3. Bestandsaufnahme datenartweise führen, nicht systemweise. Das Finanzamt fragt nach Belegen und Aufzeichnungen, nicht nach Servern.
4. Sekundärquellen zuerst dort suchen, wo sie ohnehin liegen: Bankauszüge bei der Bank, Ausgangsrechnungen beim Empfänger, Belegbilder und Buchungsbestände im Rechenzentrum, Kassenexporte im Archiv, Auswertungen der Vorjahre in der Kanzlei.
5. Beweise für die Unfreiwilligkeit sofort sichern, solange sie entstehen: forensisches Protokoll, Ticketverläufe, Sicherungsprotokolle, Anzeige. Was nach der Wiederherstellung überschrieben ist, lässt sich später nicht mehr belegen.
6. Den Entwurf des Schreibens nicht so versenden. Feinschliff über Prompt 36; ergibt die Rekonstruktion einen Berichtigungsfall nach § 153 AO, bleibt der Vorgang außerhalb beider Prompts und geht an den Berufsträger.
7. Die Bestandsmatrix als lebendes Dokument führen und bei jeder weiteren Wiederherstellung fortschreiben; die erste Fassung ist immer vorläufig.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor jeder Verwendung prüfen: Steht in der Bestandsmatrix etwas als „rekonstruiert", das tatsächlich nur vermutet wird? Jede Zeile braucht eine benannte Quelle, sonst lautet der Status „verloren".
- **Prüfen, ob der Text eine ausdrückliche gesetzliche Regelung zum Datenverlust behauptet.** Es gibt keine; die Folge ergibt sich aus § 146 Abs. 5 Satz 2 AO, § 147 Abs. 2 Nr. 2 AO und § 162 Abs. 2 Satz 2 AO (für [JAHR] verifizieren).
- **Prüfen, ob Rz. 89 des BMF-Schreibens vom 06.03.2025 als allgemeiner Grundsatz erscheint.** Die Aussage stammt aus dem Schreiben zu Kryptowerten; sie belegt die Sicht der Verwaltung auf die Risikoverteilung und ist keine Norm. Fehlt der Herkunftshinweis, ist die Ausgabe an dieser Stelle zu berichtigen.
- **Prüfen, ob eine einzelne GoBD-Randziffer zitiert wird.** Randziffern zum Datenverlust sind in diesem Projekt nicht belegt und dürfen nicht zitiert werden; zulässig ist nur der Verweis auf das Schreiben vom 28.11.2019 in der Fassung der Änderungen vom 11.03.2024 und vom 14.07.2025 (für [JAHR] verifizieren).
- **Prüfen, ob die Aufbewahrungsfristen als einheitliche Zehnjahresfrist dargestellt sind.** § 147 Abs. 3 Satz 1 AO ist gestaffelt; für Buchungsbelege gelten acht Jahre (für [JAHR] verifizieren).
- **Prüfen, ob eine Schätzungsbefugnis allein aus § 158 Abs. 2 AO abgeleitet wird.** Die Kette ist erst mit § 162 Abs. 2 Satz 2 AO vollständig. Die Nummer gehört dazu: Ein Datenverlust wird über Nr. 1 geführt, Nr. 2 setzt einen Schnittstellenverstoß voraus (für [JAHR] verifizieren).
- **Prüfen, ob die Ausgabe der Kanzlei eine Meldepflicht nach Art. 33 DSGVO zuschreibt, die den Mandanten trifft.** Verantwortlicher für die Verarbeitung in den Systemen des Mandanten ist der Mandant; Prompt 83 deckt nur Vorfälle in der Kanzlei ab (für [JAHR] verifizieren).
- **Freigabe durch einen Berufsträger** für jede Äußerung gegenüber der Finanzbehörde und für den Zeitpunkt der Offenlegung (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch**, auch die Meldefrist des Datenschutzrechts und jede vom Prüfer gesetzte Vorlagefrist; kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Prüfen, ob der Entwurf für das Finanzamt eine Schuldzuweisung, ein Eingeständnis oder eine rechtliche Wertung enthält.** Der Text schildert, was war und was fehlt – die Bewertung nimmt die Behörde vor, und was hier steht, gilt später als eigene Angabe.
- **Rechtsstand prüfen an:** §§ 145, 146, 147, 158 und 162 AO im amtlichen Volltext (gesetze-im-internet.de), am BMF-Schreiben vom 06.03.2025 (BStBl I 2025, 658) im Volltext und an den GoBD in der Fassung des BMF-Schreibens vom 14.07.2025 (BStBl I 2025, 1502).

## Varianten

- **Erste Stunde:** „Erzeuge nur die Sofortliste: was heute zu sichern ist, damit die Unfreiwilligkeit später belegbar bleibt. Höchstens zehn Positionen, abhakbar."
- **Während einer laufenden Prüfung:** „Ergänze eine Gegenüberstellung: angeforderte Unterlage | Status | was an ihre Stelle tritt | woraus sich das ergibt – als Anlage für den Prüfer."
- **Nur Bestandsmatrix:** „Erzeuge allein die Bestandsmatrix, ohne Bewertung und ohne Entwurf, als Arbeitsgrundlage für die Sachbearbeitung."
- **Mandantenbriefing:** „Fasse Lage und nächste Schritte in Sie-Form zusammen, höchstens 300 Wörter, ohne interne Bewertungen, mit klarer Aufgabenliste für den Mandanten."
- **Nachbereitung:** „Erzeuge aus dem Vorfall eine Ergänzungsliste für die Verfahrensdokumentation, gegliedert nach Sicherung, Wiederherstellung, Zuständigkeit und Nachweis (Übergabe an Prompt 37)."
