# 121 – Plattformen-Steuertransparenzgesetz: Betroffenheit und Sorgfaltspflichten des Betreibers

**Problem:** Der Mandant betreibt einen Marktplatz, eine Vermittlungs-App oder ein Buchungsportal und weiß nicht, ob ihn das PStTG trifft – und wenn ja, mit welchen Sorgfalts-, Informations-, Aufzeichnungs- und Meldepflichten.
**Rolle:** Steuerberater und Berufsträger; in der Vorbereitung die Mandantenbetreuung. Der Mandant liefert die Angaben zum Geschäftsmodell zu, bedient das Werkzeug aber nicht selbst.
**DATEV-Bezug:** Kein DATEV-Modul erfüllt die Pflichten des PStTG; sie liegen im Plattformsystem des Mandanten. Berührt sind DATEV DMS (Ablage der Sorgfaltspflichten-Dokumentation, der Prozessbeschreibung und der Anbieterinformation), DATEV Kanzlei-Rechnungswesen (Provisions- und Vermittlungserlöse) und DATEV Unternehmen online (Belegweg aus dem Plattformsystem); Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren.
**Was du bereitstellen musst:** Beschreibung des Geschäftsmodells; wer die Anbieter sind; wie die Vergütung fließt und ob sie dem Betreiber bekannt ist; Sitz des Betreibers; ob Anbieter im Ausland tätig sind; grobe Zahl der Anbieter; seit wann die Plattform betrieben wird; Registrierungs- und Dokumentationsstand.
**Datensparsamkeit:** In diesen Prompt kommen **keine Anbieterdaten** – keine Namen, Anschriften, Geburtsdaten, Steueridentifikationsmerkmale, Registernummern, Kontodaten oder Umsatzangaben einzelner Anbieter; sie sind gerade der Gegenstand der Meldung und haben im Werkzeug nichts zu suchen. Plattform und Mandant nur als Platzhalter (`Mandant A`, `Plattform 1`), Anbieter nur als Gruppe (`Anbieter im Inland`, `Anbieter im übrigen Gemeinschaftsgebiet`). Steuernummer, Steuer-Identifikationsnummer, Wirtschafts-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Die Auswahl des Werkzeugs, der Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters sind vorher zu klären; § 62a StBerG verlangt sorgfältige Auswahl und einen Vertrag in Textform mit Verschwiegenheitsverpflichtung – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für dieses Einzelmandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und prüfst, ob ein
Mandant vom Plattformen-Steuertransparenzgesetz erfasst wird und welche
Pflichten daraus folgen. Du prüfst die Merkmale in der vorgegebenen Reihenfolge
und überspringst keines, auch wenn das Ergebnis naheliegt.

WAS DIESER PROMPT NICHT TUT
- Er nennt für Termine und Fristen KEIN vollständiges Kalenderdatum. Die
  Termine des PStTG stehen als Tag und Monat im Gesetz; so und nicht anders
  gibst du sie wieder. Ob sich ein Termin verschiebt, weil er auf einen
  Sonnabend, einen Sonntag oder einen Feiertag fällt, richtet sich über
  § 1 Abs. 2 PStTG nach § 108 Abs. 3 AO; ein solches Verschiebungsdatum ist
  NICHT amtlich bekanntgegeben, sondern von einem Menschen zu bestimmen.
  Berechne es nicht und nenne es nicht. Ausgenommen von diesem Verbot ist
  allein die Rechtsstandsangabe am Ende, also Verkündungs- und
  Änderungsdaten des Gesetzes.
- Er meldet nicht und füllt keine Meldung aus. Die Übermittlung an das
  Bundeszentralamt für Steuern ist Portalbedienung und Sache eines Menschen.
- Er beurteilt NICHT die Steuerpflicht der Anbieter. Die Anbieterseite behandelt
  Prompt 120.
- Er verarbeitet keine Anbieterdaten. Enthält der Sachverhalt gleichwohl Namen,
  Anschriften, Steueridentifikationsmerkmale, Registernummern oder Kontodaten
  einzelner Anbieter, verarbeite sie nicht, fordere ihre Entfernung an und
  arbeite erst danach weiter.

AUSSTEUERUNGSREGEL – kein Abbruch, an einer objektiven Angabe
Steht im Feld "Kryptowerte-Dienstleistungen über die Plattform" der Wert "ja"
oder "unklar", steuere diesen Geschäftsbereich aus. Gib dafür nur aus:
"Ausgesteuert – gesondert am Kryptowerte-Steuertransparenzgesetz zu prüfen
(Prompt 122); hier keine Aussage." Prüfe alle übrigen Geschäftsbereiche
vollständig weiter und sage am Ende ausdrücklich, welchen Bereich du
ausgesteuert hast.

AUFGABE
Beurteile die Betroffenheit Merkmal für Merkmal, leite daraus die Pflichten mit
Fundstelle und Termin ab, benenne die Lücken und liefere die beiden Entwürfe,
die der Mandant sofort braucht.

GESCHÄFTSMODELL
- Was wird über die Plattform ermöglicht: [BESCHREIBUNG in eigenen Worten]
- Ermöglicht die Plattform, dass Anbieter und Nutzer in Kontakt treten und ein
  Rechtsgeschäft schließen: [ja / nein / teilweise / unklar]
- Wer sind die Anbieter: [Privatpersonen / Unternehmen / beides]
- Sind die Anbieter beim Mandanten nichtselbständig beschäftigt:
  [nein / ja, teilweise / ja, ausschließlich]
- Wird die Vergütung über die Plattform abgewickelt: [ja / nein / teilweise]
- Ist die Vergütung dem Betreiber bekannt oder für ihn feststellbar:
  [ja / nein / teilweise / unklar]
- Sitz und Ansässigkeit des Betreibers: [Inland / übriges Gemeinschaftsgebiet /
  Drittland / mehrere]
- Anbieter ansässig: [nur im Inland / auch im übrigen Gemeinschaftsgebiet /
  auch im Drittland / unbekannt]
- Zahl der Anbieter, grob: [unter 100 / 100 bis 1.000 / über 1.000 / unbekannt]
- Plattform betrieben seit: [JAHR]
- Kryptowerte-Dienstleistungen über die Plattform: [nein / ja / unklar]
- Als meldender Plattformbetreiber beim Bundeszentralamt für Steuern
  registriert: [nein / ja / unbekannt]
- Feststellung als freigestellter Plattformbetreiber beantragt oder erteilt:
  [nein / beantragt / erteilt / unbekannt]
- Sorgfaltspflichten dokumentiert: [nein / teilweise / ja]
- Prozessbeschreibung nach § 24 Abs. 1 Nr. 1 PStTG vorhanden:
  [nein / in Arbeit / ja]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. PLATTFORMBETREIBER. Prüfe § 3 Abs. 2 PStTG: Ist der Mandant
   Plattformbetreiber? Grenze ab gegen § 3 Abs. 3 PStTG (freigestellter
   Plattformbetreiber) und § 3 Abs. 4 PStTG (meldender Plattformbetreiber) und
   erkläre, dass diese drei Begriffe nicht dasselbe bedeuten. Stütze dich dabei
   nur auf die Angaben zum Geschäftsmodell, zur Kontaktaufnahme und zum Sitz.
   Fällt das Ergebnis negativ aus, sage es und arbeite die weiteren Schritte
   nur noch hilfsweise durch, ausdrücklich als Hilfsprüfung bezeichnet. Halte
   zum Schluss das Feld zur Registrierung als meldender Plattformbetreiber
   daneben und benenne ausdrücklich, wenn dein Ergebnis und der
   Registrierungsstand auseinanderfallen oder der Stand unbekannt ist.
2. RELEVANTE TÄTIGKEIT. Prüfe § 5 Abs. 1 Satz 1 PStTG einzeln:
   Nr. 1 Überlassung unbeweglichen Vermögens, Nr. 2 persönliche
   Dienstleistungen, Nr. 3 Verkauf von Waren, Nr. 4 Überlassung von
   Verkehrsmitteln. Sage je Nummer, ob sie einschlägig ist, und begründe es an
   der Beschreibung des Geschäftsmodells. Prüfe DANACH gesondert das Merkmal
   "gegen Vergütung", das für alle vier Nummern gilt, an den Feldern zur
   Abwicklung und zur Kenntnis der Vergütung; steht dort "nein" oder "unklar",
   sage ausdrücklich, dass die relevante Tätigkeit insoweit nicht bejaht werden
   kann, und nimm das als offenen Punkt auf. Weise auf § 5 Abs. 1 Satz 2 PStTG
   hin: Nichtselbständig Beschäftigte des Betreibers sind ausgenommen; verknüpfe
   das mit dem entsprechenden Feld.
3. FREISTELLUNG. Prüfe § 3 Abs. 3 PStTG und erkläre danach das Verfahren nach
   § 11 PStTG. Stelle ausdrücklich klar: § 11 PStTG ist KEINE Melde- oder
   Aufzeichnungsvorschrift, sondern das Verfahren zur Feststellung eines
   freigestellten Plattformbetreibers durch das Bundeszentralamt für Steuern
   auf Antrag. Die Feststellung ist zeitlich begrenzt und deshalb zu
   verlängern; benenne Geltungsdauer und Verlängerung positiv mit Absatz und
   Satz aus dem amtlichen Volltext (§ 11 PStTG – für [JAHR] verifizieren) und
   schreibe "Fundstelle offen – bitte recherchieren", wenn du sie nicht sicher
   kennst.
   Nenne die Antragsfrist 31. Oktober (§ 11 Abs. 3 Satz 2 PStTG) als Termin
   ohne Jahresangabe und die Gebühren nach § 11 Abs. 7 Satz 3 PStTG:
   5.000 € je Feststellungsantrag, 2.500 € je Verlängerungsantrag (Beträge –
   für [JAHR] verifizieren). Verknüpfe das Ergebnis mit dem Feld zur bereits
   beantragten oder erteilten Feststellung.
4. SORGFALTSPFLICHTEN, ABSCHNITT 3 DES PStTG. Gehe §§ 16 bis 21 PStTG mit ihren
   Überschriften durch: § 16 Anwendung, § 17 Erhebung, § 18 Überprüfung, § 19
   Identifizierung freigestellter Anbieter, § 20 Frist, § 21 Erfüllung durch
   Dritte. Sage je Vorschrift, was sie vom Mandanten verlangt und was im
   Plattformsystem dafür vorhanden sein muss. Hebe zwei Punkte hervor:
   - § 18 Abs. 1 Satz 1 PStTG verlangt eine PLAUSIBILITÄTSPRÜFUNG, keine
     Richtigkeitsgewähr; sie erfolgt anhand aller Informationen, die aus anderen
     Zusammenhängen zur Erfüllung vertraglicher oder fachgesetzlicher Vorgaben
     verfügbar sind. Erkläre den Begriff ausdrücklich: Der Betreiber schuldet
     nicht, dass die Angaben richtig sind, sondern dass er sie mit dem ihm
     verfügbaren Material abgleicht.
   - § 20 Abs. 1 Satz 1 PStTG: Abschluss bis 31. Dezember des Meldezeitraums;
     für bereits bestehende Anbieter bis 31. Dezember des zweiten
     Meldezeitraums. Verknüpfe das mit dem Feld "Plattform betrieben seit" und
     sage, welche Anbietergruppe danach in welche Variante fällt, ohne ein
     Datum zu bilden.
   Beziehe die Felder zur Ansässigkeit der Anbieter und zur Zahl der Anbieter
   auf den Umsetzungsaufwand und auf die Frage, ob § 21 PStTG in Betracht kommt.
   Beziehe das Feld "Wer sind die Anbieter" darauf, dass die zu erhebenden und
   zu überprüfenden Angaben bei natürlichen Personen und bei Rechtsträgern
   auseinandergehen können; nimm das als zu klärenden Punkt auf, ohne die
   Angaben aufzuzählen. Übernimm zuletzt das Feld "Sorgfaltspflichten
   dokumentiert" und sage, welche der §§ 16 bis 21 PStTG danach als
   undokumentiert gelten und damit in die Lückenliste gehören.
5. INFORMATION DER ANBIETER, § 22 PStTG. Trenne die beiden Absätze:
   - Abs. 1: Information vor der erstmaligen Meldung, in ALLGEMEINER Form,
     mit den Gegenständen der Nummern 1 und 2.
   - Abs. 2: die den einzelnen Anbieter BETREFFENDEN Informationen, bis zum
     31. Januar des Folgejahres.
   Sage ausdrücklich, dass Abs. 1 eine allgemeine und Abs. 2 eine individuelle
   Information ist und dass die eine die andere nicht ersetzt.
6. AUFZEICHNUNGEN, § 24 PStTG. Benenne Abs. 1 Nr. 1: Beschreibung der Prozesse
   einschließlich der automationstechnischen, operativen und organisatorischen
   Vorkehrungen. Benenne Abs. 2 Nr. 1: Erstellung bis zum Ablauf des
   Meldezeitraums. Benenne Abs. 3 Satz 1: Aufbewahrung zehn Jahre (Dauer –
   für [JAHR] verifizieren). Verknüpfe das mit dem Feld zur vorhandenen
   Prozessbeschreibung.
7. BUSSGELDRISIKO, § 25 PStTG. Die Bußgeldvorschrift ist § 25 PStTG und NICHT
   § 24 PStTG; § 24 PStTG regelt Aufzeichnungen und Aufbewahrung und ist kein
   Bußgeldtatbestand. Leite deshalb keine Bußgeldhöhe aus § 24 PStTG ab.
   Ordne die festgestellten Lücken NUR denjenigen Tatbeständen des
   § 25 Abs. 1 PStTG zu, deren Wortlaut dir sicher bekannt ist. Belegt ist:
   Der Verstoß gegen § 24 Abs. 1 PStTG ist von § 25 Abs. 1 Nr. 7 PStTG erfasst
   und fällt damit in den Rahmen bis 5.000 €. Für jede weitere Lücke schreibe
   "Tatbestand am amtlichen Volltext des § 25 Abs. 1 PStTG zuzuordnen –
   Fundstelle offen – bitte recherchieren" und nenne für sie KEINEN Rahmen.
   Den Rahmen des § 25 Abs. 2 PStTG gibst du nur zur Einordnung wieder:
   bis 50.000 € für § 25 Abs. 1 Nr. 1 bis 3 Buchst. a, bis 30.000 € für
   Nr. 4 bis 6, bis 5.000 € für die übrigen (Beträge und Zuordnung –
   für [JAHR] verifizieren).
8. MELDEFRIST. Nenne § 13 Abs. 1 Satz 1 PStTG: Meldung spätestens zum
   31. Januar des Folgejahres. Weise darauf hin, dass über § 1 Abs. 2 PStTG
   § 108 Abs. 3 AO gilt und sich der Termin dadurch verschieben kann. Nenne
   kein Datum, berechne keine Verschiebung und behaupte nicht, ein
   Verschiebungstermin sei bekanntgegeben worden. Ergänze: "Fristen berechnet
   und erfasst ein Mensch."

RECHTSSTAND, DEN DU IM ERGEBNIS AUSWEIST
PStTG, Artikel 1 des Gesetzes zur Umsetzung der Richtlinie (EU) 2021/514 vom
20.12.2022, BGBl. 2022 I S. 2730, in Kraft seit 01.01.2023, zuletzt geändert
durch Artikel 5 des Gesetzes vom 22.12.2025 (BGBl. 2025 I Nr. 352). Weise
diesen Stand aus und ergänze "Rechtsstand – für [JAHR] verifizieren".

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben, statt sie zu erfinden. Fehlt eine Angabe zum Vergütungsmerkmal,
   entscheide die Betroffenheit nicht, sondern fordere sie an.
2. Nenne zu jeder Aussage die Rechtsgrundlage POSITIV mit Absatz, Satz und
   Nummer, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine
   Fundstelle; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
   Führe alle Fundstellen am Ende in der Tabelle zusammen.
3. Nenne jeden Betrag und jede Aufbewahrungsdauer nur als nachzuschlagende
   Größe mit dem Zusatz "für [JAHR] verifizieren".
4. Berechne KEINE Fristen und kein Datum. Nenne Termine ausschließlich so, wie
   sie im Gesetz stehen, also als Tag und Monat ohne Jahr, je mit
   Rechtsgrundlage, und ergänze bei jedem: "Fristen berechnet und erfasst ein
   Mensch."
5. Trenne durchgehend Betroffenheit, Pflicht und Lücke. Eine erfüllte
   Dokumentation macht eine verneinte Betroffenheit nicht richtig und umgekehrt.
6. Kennzeichne jede Aussage über die technische Ausgestaltung des
   Plattformsystems als Vermutung, solange sie nicht aus den Angaben folgt.

AUSGABEFORMAT
1. (Eindeutigkeit und Datenlage)
2. (Betroffenheitsergebnis) – Tabelle:
   Merkmal | Fundstelle | Ergebnis (ja / nein / offen) | Begründung aus den
   Angaben | was zur Klärung fehlt
   Mindestens: Plattformbetreiber § 3 Abs. 2 | freigestellt § 3 Abs. 3 |
   meldend § 3 Abs. 4 | relevante Tätigkeit § 5 Abs. 1 Satz 1 Nr. 1 bis 4 |
   Merkmal "gegen Vergütung" | Ausnahme § 5 Abs. 1 Satz 2
3. (Pflichtenliste) – abhakbare Tabelle mit ☐:
   Pflicht | Fundstelle | Termin laut Gesetz, Tag und Monat ohne Jahr |
   wer erledigt | Stand | erledigt (leer)
4. (Lückenliste) – Tabelle:
   Nr. | Lücke | Folge | Maßnahme | wer | erledigt (leer)
5. (Entwurf der allgemeinen Information nach § 22 Abs. 1 PStTG) – Text in
   Sie-Form, an die Anbieter gerichtet, allgemein gehalten, gegliedert nach
   den Gegenständen der Nummern 1 und 2; setze unter den Entwurf den Hinweis,
   dass der Wortlaut der beiden Nummern am amtlichen Volltext abzugleichen ist
   und der Entwurf ohne diesen Abgleich nicht verwendet wird
6. (Gliederungsvorschlag für die Prozessbeschreibung nach § 24 Abs. 1 Nr. 1
   PStTG) – nummerierte Gliederung mit je einem Satz, was der Abschnitt
   enthält, getrennt nach automationstechnischen, operativen und
   organisatorischen Vorkehrungen
7. (Bußgeldrisiko) – Tabelle:
   Lücke | Tatbestand des § 25 Abs. 1 PStTG, soweit zuordenbar | Rahmen nach
   § 25 Abs. 2 PStTG | Einschätzung (Vermutung kennzeichnen)
8. (Ausgesteuerter Geschäftsbereich) – falls einer ausgesteuert wurde
9. (Rechtsstand und Fristarten) – der Rechtsstand mit Verkündungs- und
   Änderungsdatum wie im Abschnitt RECHTSSTAND vorgegeben; die Fristarten
   dagegen nur als Tag und Monat ohne Jahr und ohne verschobenes Datum
10. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
11. (Interne Notiz) – was ich nicht sicher weiß, was zuerst zu klären ist
```

## Anwendung

1. **Vorschaltfrage vor dem Werkzeugeinsatz, außerhalb des Werkzeugs:** Der Berufsträger klärt und vermerkt in der Handakte, ob gegen den Mandanten bereits ein Bußgeld- oder Steuerstrafverfahren im Zusammenhang mit dem PStTG läuft, ob eine abgegebene Meldung unrichtig ist oder eine Berichtigung im Raum steht. Trifft eines davon zu, gehört der Fall nach `DATENSCHUTZ.md` in die Zone Rot und in kein KI-Werkzeug – auch nicht anonymisiert und auch nicht als Ja-Nein-Angabe. Die Betroffenheitsprüfung wird dann ohne Werkzeug geführt.
2. Die Beschreibung des Geschäftsmodells vom Mandanten selbst formulieren lassen, bevor Rechtsbegriffe ins Spiel kommen. Wer die Plattform vorab als „nur Vermittlung" oder „nur Anzeigen" beschreibt, hat die Prüfung schon vorweggenommen.
3. Das Merkmal „gegen Vergütung" gesondert klären. Es entscheidet in der Praxis häufiger über die Betroffenheit als die Frage, welche der vier relevanten Tätigkeiten vorliegt.
4. Keine Anbieterdaten in das Werkzeug geben – auch keine Beispielzeile aus dem System. Die Prüfung braucht Gruppen, nicht Personen.
5. Pflichtenliste und Lückenliste mit Verantwortlichen versehen und in DATEV DMS ablegen. Die Termine trägt ein Mensch in das Fristenprogramm ein; das Modell liefert nur den gesetzlichen Tag und Monat.
6. Den Entwurf der Information nach § 22 Abs. 1 PStTG vor der Verwendung gegen den amtlichen Gesetzeswortlaut abgleichen und durch einen Berufsträger freigeben; er geht an sämtliche Anbieter und wirkt nach außen.
7. Zur Abgrenzung: Die Zusammenfassende Meldung behandelt Prompt 58 – sie hat mit dem PStTG nichts zu tun und darf damit nicht vermengt werden. Die Anbieterseite, also den Mandanten, der auf einer fremden Plattform verdient, behandelt Prompt 120. Für Kryptowerte-Dienstleister gilt die Parallelnorm; dafür ist Prompt 122 zuständig.

## Qualitätssicherung

- **§ 11 PStTG ist eine Verfahrensvorschrift, keine Meldevorschrift.** Eine Antwort, die § 11 PStTG als Aufzeichnungs- oder Meldepflicht darstellt, ist falsch und wird verworfen. Geprüft wird: Feststellung durch das Bundeszentralamt für Steuern auf Antrag, Geltung jeweils für einen Meldezeitraum, Antragsfrist 31. Oktober nach Abs. 3 Satz 2, Gebühren nach Abs. 7 Satz 3 (für [JAHR] verifizieren).
- **Die Bußgeldvorschrift ist § 25 PStTG.** § 24 Abs. 1 Nr. 1 PStTG ist kein Bußgeldtatbestand; aus § 24 PStTG lässt sich keine Bußgeldhöhe ableiten. Erscheint in der Ausgabe ein Bußgeld unter Berufung auf § 24 PStTG, ist das ein Fehler und kein Zwischenergebnis.
- **§ 18 Abs. 1 Satz 1 PStTG verlangt eine Plausibilitätsprüfung, keine Richtigkeitsgewähr** (für [JAHR] verifizieren). Prüfen: Wurde der Maßstab richtig beschrieben – Abgleich anhand der aus anderen Zusammenhängen zur Erfüllung vertraglicher oder fachgesetzlicher Vorgaben verfügbaren Informationen – oder wurde daraus eine Einstandspflicht für die Richtigkeit der Anbieterangaben gemacht?
- **Kein Kalenderdatum aus der KI-Antwort übernehmen.** Die Meldefrist ist der 31. Januar des Folgejahres (§ 13 Abs. 1 Satz 1 PStTG, für [JAHR] verifizieren); ob sie sich über § 1 Abs. 2 PStTG in Verbindung mit § 108 Abs. 3 AO verschiebt, bestimmt die Kanzlei. Ein verschobener Meldetermin ist nicht amtlich bekanntgegeben worden; eine Antwort, die das behauptet, wird verworfen. **Fristen berechnet und erfasst ein Mensch.**
- **Die drei Betreiberbegriffe auseinanderhalten:** Plattformbetreiber (§ 3 Abs. 2 PStTG), freigestellter Plattformbetreiber (§ 3 Abs. 3 PStTG) und meldender Plattformbetreiber (§ 3 Abs. 4 PStTG) sind nicht dasselbe. Eine Antwort, die sie gleichsetzt, trägt nicht.
- **§ 22 Abs. 1 und Abs. 2 PStTG sind zwei getrennte Pflichten.** Die allgemeine Information vor der erstmaligen Meldung ersetzt nicht die individuelle Mitteilung der den Anbieter betreffenden Informationen bis zum 31. Januar des Folgejahres – und umgekehrt.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Betroffenheitsergebnis, Pflichtenliste und Zuordnung der Bußgeldtatbestände nach; die Anbieterinformation, jede Auskunft an den Mandanten und jede Kommunikation mit dem Bundeszentralamt für Steuern gibt ein Berufsträger frei, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** dem PStTG im amtlichen Volltext (gesetze-im-internet.de), insbesondere §§ 1, 3, 5, 11, 13, 16 bis 22, 24 und 25, dem Verkündungstext BGBl. 2022 I S. 2730 und der Änderung durch Artikel 5 des Gesetzes vom 22.12.2025 (BGBl. 2025 I Nr. 352) über recht.bund.de, den Informationen des Bundeszentralamts für Steuern sowie DATEV LEXinform.

## Varianten

- **Erstbeurteilung:** „Beschränke dich auf die Schritte 1 bis 3 und gib nur das Betroffenheitsergebnis mit Begründung je Merkmal und die offenen Punkte aus."
- **Umsetzungsplan:** „Erzeuge aus der Pflichten- und der Lückenliste einen Umsetzungsplan mit Arbeitspaketen, Verantwortlichen und Reihenfolge, ohne Termine zu setzen."
- **Systemanforderungen:** „Leite aus den §§ 17 bis 20 PStTG eine Anforderungsliste an das Plattformsystem ab: welches Feld erhoben, welche Angabe plausibilisiert und welcher Vorgang protokolliert werden muss."
- **Nach einem Betreiberwechsel oder einer Modelländerung:** „Prüfe ausschließlich, welche der bisherigen Feststellungen durch die geänderten Angaben hinfällig werden, und benenne, was neu zu klären ist."
