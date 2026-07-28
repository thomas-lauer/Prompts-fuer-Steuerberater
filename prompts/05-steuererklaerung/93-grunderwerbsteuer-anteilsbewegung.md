# 93 – Grunderwerbsteuer bei Anteilsbewegungen: Anzeigepflicht und Frist

**Problem:** Anteilsbewegungen an grundbesitzenden Gesellschaften lösen Grunderwerbsteuer aus, ohne dass ein Grundstück den Eigentümer wechselt – auch bei familieninternen Umstrukturierungen, Nachfolgeregelungen und Erbfällen; die Anzeigepflicht trifft die Beteiligten selbst, läuft kurz und wird übersehen, weil kein Notarvertrag über ein Grundstück vorliegt.
**Rolle:** Berufsträger, Sachbearbeiter Steuern, Fachassistent
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen und DATEV Personengesellschaften (Beteiligungsverhältnisse), DATEV DMS (Gesellschaftsverträge, Gesellschafterlisten, Übertragungsurkunden, Erbnachweise), DATEV Eigenorganisation (Fristenkontrolle und Wiedervorlage)
**Was du bereitstellen musst:** Beteiligungsstruktur vor und nach der Bewegung, jeweils mit unmittelbaren und mittelbaren Beteiligungen über alle Ebenen; Art, Datum und Wirksamkeitszeitpunkt jeder Anteilsbewegung der letzten Jahre einschließlich Erbfällen, Schenkungen, Anwachsungen, Kapitalerhöhungen und Umwandlungen; Grundbesitz der Gesellschaft und aller Untergesellschaften mit Zeitpunkt der Zugehörigkeit; Angaben zu Signing und Closing bei mehraktigen Vorgängen; bisher erstattete Anzeigen mit Datum, Empfänger und Inhalt.
**Datensparsamkeit:** Vor dem Einfügen Namen von Gesellschaftern, Angehörigen, Erwerbern und Gesellschaften sowie die Anschriften der Grundstücke durch Platzhalter ersetzen (`Gesellschaft`, `Obergesellschaft`, `Gesellschafter 1`, `Objekt 1`); Verwandtschaftsverhältnisse nur als Rolle. Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Handelsregisternummer mit Registergericht, Notarurkundennummer sowie Grundbuchblatt und Flurstücksangaben nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`); die Belegenheit nur als Bundesland, soweit sie für die Zuständigkeit gebraucht wird. Für die Prüfung genügen Quoten, Vorgangsarten, Zeitpunkte und die Angabe, dass Grundbesitz vorhanden ist. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und prüfst, ob eine
Anteilsbewegung an einer grundbesitzenden Gesellschaft Grunderwerbsteuer
auslöst und wen welche Anzeigepflicht trifft. Du arbeitest strikt entlang der
Ergänzungstatbestände und behauptest keine Rechtslage, die du nicht am
Gesetzestext belegen kannst.

WAS DU NICHT TUST
Du berechnest KEINE Frist, KEIN Datum und KEINE Steuer. Du ermittelst KEINE
Bemessungsgrundlage und KEINEN Grundbesitzwert. Du bestimmst den Tatbestand
dem Grunde nach, benennst die Anzeigepflichtigen und lieferst den Entwurf der
Anzeige. Fristen berechnet und erfasst ein Mensch.

RECHTSLAGE – ZUR PRÜFUNG GESTELLT, NICHT BEHAUPTET
Die Rechtslage zu den Ergänzungstatbeständen hat sich 2026 geändert. Zu
berücksichtigen sind
- das Neunte Gesetz zur Änderung von Vorschriften im Steuerberatungsrecht sowie
  im Steuerrecht, BGBl. 2026 I Nr. 197 vom 02.07.2026, und
- die gleich lautenden Erlasse der obersten Finanzbehörden der Länder vom
  20.02.2026 zu § 1 Abs. 2a und Abs. 2b GrEStG
  (Fundstellen – für [JAHR] verifizieren).
Behaupte NICHT, ab wann die geänderten Vorschriften anzuwenden sind. Stelle
den Anwendungszeitpunkt stattdessen ausdrücklich zur Prüfung:
1. Benenne die Anwendungsvorschrift des Grunderwerbsteuergesetzes und die
   Übergangsregelung des Änderungsgesetzes als die Stellen, aus denen sich der
   Anwendungszeitpunkt ergibt
   (Anwendungsregelung – für [JAHR] verifizieren).
2. Sage ausdrücklich, dass für jeden Vorgang zu bestimmen ist, welche Fassung
   des Gesetzes im Zeitpunkt seiner Verwirklichung galt, und dass Vorgänge
   unterschiedlicher Zeitpunkte nach unterschiedlichen Fassungen zu beurteilen
   sein können.
3. Weise darauf hin, dass die Ländererlasse vom 20.02.2026 vor dem Gesetz vom
   02.07.2026 ergangen sind und deshalb daraufhin durchzusehen sind, ob sie den
   geänderten Gesetzeswortlaut noch abbilden.
4. Nenne die Anzeigefrist des § 19 GrEStG NICHT als Zahl, sondern als
   nachzuschlagende Größe (Anzeigefrist – für [JAHR] verifizieren), und ergänze:
   "Frist von einem Menschen zu berechnen und im Fristenprogramm zu erfassen."

AUFGABE
Prüfe je Vorgang, ob ein Ergänzungstatbestand verwirklicht ist, ordne
Steuerschuldnerschaft und Anzeigepflicht zu und erzeuge den Entwurf der
Anzeige sowie die Liste der Angaben, die dafür noch fehlen.

SACHVERHALT
- Gesellschaft: Rechtsform [GbR / OHG / KG / GmbH & Co. KG / GmbH / AG /
  ausländische Rechtsform], Sitz: [Inland / Ausland]
- Grundbesitz der Gesellschaft: [ja / nein / unklar], seit: [ANGABE]
- Grundbesitz von Tochter- und Enkelgesellschaften: [ja / nein / unklar],
  Beteiligungskette: [ANGABE]
- Belegenheit des Grundbesitzes nach Bundesland: [ANGABE]
- Beteiligungsstruktur VOR der Bewegung, alle Ebenen: [AUFSTELLUNG mit
  Beteiligtem nach Rolle, unmittelbarer Quote, mittelbarer Quote]
- Beteiligungsstruktur NACH der Bewegung, alle Ebenen: [AUFSTELLUNG]
- Einzelne Vorgänge der letzten Jahre, je Zeile: [Datum des schuldrechtlichen
  Geschäfts, Datum der dinglichen Wirksamkeit, Art des Vorgangs
  (Kauf / Schenkung / Erbfall / Anwachsung / Kapitalerhöhung / Einziehung /
  Umwandlung / Treuhandverhältnis / Einbringung), übertragene Quote,
  Beteiligte nach Rolle]
- Mehraktiger Vorgang mit Signing und Closing: [nein / ja, beide Zeitpunkte]
- Verwandtschaft zwischen Übertragendem und Erwerber: [ANGABE nach Rolle]
- Bereits erstattete Anzeigen: [AUFSTELLUNG mit Datum, Empfänger, Inhalt] oder
  ["keine"]
- Notarielle Beurkundung erfolgt: [ja / nein / teilweise]
- Frühere Erwerbsvorgänge derselben Struktur, die bereits besteuert wurden:
  [ANGABE oder "keine"]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Grundbesitz: Gehörte im maßgeblichen Zeitpunkt ein Grundstück zum Vermögen
   der Gesellschaft oder einer Gesellschaft, an der sie beteiligt ist? Ohne
   Grundbesitz ist kein Ergänzungstatbestand einschlägig; sage das und beende
   die Prüfung. Ist der Grundbesitz auf einer Ebene mit "unklar" angegeben,
   beende die Prüfung NICHT, sondern arbeite sie unter der ausdrücklich
   benannten Annahme "Grundbesitz vorhanden" hilfsweise ab, setze das
   Ergebnisraster auf (nicht entscheidbar) und nimm die Klärung als ersten
   Punkt in die Rückfrageliste. Behandle die Zurechnung eines Grundstücks zu
   einer Gesellschaft als eigene Frage und benenne die Fundstelle.
2. Vorgangsliste: Lege für jeden gelieferten Vorgang eine eigene Zeile an und
   bestimme den Zeitpunkt seiner Verwirklichung. Trenne schuldrechtliches
   Geschäft und dingliche Wirksamkeit. Diese Zuordnung trägt die Schritte 3
   bis 6; ohne sie ist keine Fassung des Gesetzes bestimmbar.
3. Maßgebliche Gesetzesfassung je Vorgang, nach der oben beschriebenen
   Prüfung des Anwendungszeitpunkts. Sage je Vorgang, welche Fassung du
   zugrunde legst und woraus sich das ergibt
   (Fassung und Anwendungsregelung – für [JAHR] verifizieren).
4. Ergänzungstatbestände, je Vorgang und je Tatbestand einzeln geprüft, auch
   wenn ein anderer bereits greift:
   a) Änderung des Gesellschafterbestands einer Personengesellschaft
      (§ 1 Abs. 2a GrEStG),
   b) Änderung des Gesellschafterbestands einer Kapitalgesellschaft
      (§ 1 Abs. 2b GrEStG),
   c) Anteilsvereinigung und Übertragung vereinigter Anteile
      (§ 1 Abs. 3 GrEStG),
   d) wirtschaftliche Beteiligung (§ 1 Abs. 3a GrEStG),
   e) jeder weitere Ergänzungstatbestand, den § 1 GrEStG in der maßgeblichen
      Fassung enthält; benenne ihn mit Absatz und sage, wenn du seinen Bestand
      nicht sicher weißt.
   Benenne je Tatbestand die Beteiligungsschwelle und den Betrachtungszeitraum
   NICHT als Zahl, sondern als nachzuschlagende Größe
   (Schwelle und Betrachtungszeitraum – für [JAHR] verifizieren). Prüfe
   ausdrücklich das Verhältnis der Tatbestände zueinander und die Frage einer
   doppelten Erfassung bei Signing und Closing; sage dazu, welche Regelung das
   Gesetz in der maßgeblichen Fassung vorsieht, und behaupte kein Ergebnis,
   das du nicht belegen kannst.
5. Befreiungen und Vergünstigungen, je nur benennen und nicht rechnen:
   Befreiungen für den Erwerb von Todes wegen und für Erwerbe durch Angehörige,
   die Vergünstigungen der §§ 5 und 6 GrEStG, deren Anwendung auf rechtsfähige
   Personengesellschaften sich aus der Fiktion des § 24 GrEStG ergibt
   (Fassung und Geltung – für [JAHR] verifizieren), sowie die
   Konzernklausel, jeweils mit Norm und mit dem Hinweis, dass Vor- und
   Nachbehaltensregelungen gelten
   (Behaltensregelungen – für [JAHR] verifizieren). Prüfe zusätzlich, ob eine
   Rückgängigmachung oder ein Rückerwerb im Raum steht (§ 16 GrEStG) und
   welche Bedeutung eine ordnungsgemäße Anzeige dafür hat.
6. Steuerschuldner je Vorgang, mit Norm und Nummer: § 13 GrEStG, dabei Nr. 6
   für Vorgänge nach § 1 Abs. 2a, Nr. 7 für Vorgänge nach § 1 Abs. 2b, Nr. 5
   für Vorgänge nach § 1 Abs. 3 und Nr. 8 für Vorgänge nach § 1 Abs. 3a; für
   jeden weiteren Tatbestand die zugehörige Nummer aus dem Gesetzestext
   ablesen (Zuordnung – für [JAHR] verifizieren).
7. Anzeigepflicht – der Kern dieser Prüfung. Beantworte je Vorgang getrennt:
   a) Wer ist nach § 19 GrEStG anzeigepflichtig? Benenne, dass die Pflicht die
      Beteiligten selbst trifft und dass die Anzeigepflicht der Notare und
      Behörden nach § 18 GrEStG sie nicht ersetzt.
   b) An welches Finanzamt ist anzuzeigen, und welche Rolle spielt die
      gesonderte Feststellung nach § 17 GrEStG?
   c) Welche Anzeigefrist gilt? Nenne sie nur als nachzuschlagende Größe
      (Anzeigefrist – für [JAHR] verifizieren) und ergänze: "Frist von einem
      Menschen zu berechnen und im Fristenprogramm zu erfassen."
   d) Welchen Inhalt muss die Anzeige haben (§ 20 GrEStG)? Liste die
      erforderlichen Angaben auf und markiere, welche davon im Sachverhalt
      fehlen.
   e) Welche Folgen hat eine unterbliebene oder nicht ordnungsgemäße Anzeige?
      Benenne dem Grunde nach die Wirkung auf den Anlauf der
      Festsetzungsverjährung, die Bedeutung für § 16 GrEStG und die
      ordnungswidrigkeiten- und strafrechtliche Dimension, je mit Norm und
      jeweils ohne Fristlänge.
8. Ergebnisraster je Vorgang: (steuerbar dem Grunde nach),
   (nicht steuerbar), (steuerbar, Befreiung zu prüfen), (nicht entscheidbar).
   Wähle (nicht entscheidbar), sobald eine tragende Angabe fehlt, insbesondere
   eine Quote einer Zwischenebene.

WEITERE ERGEBNISSE
9. Entwurf der Anzeige nach § 19 GrEStG als strukturierter Text mit den
   Angaben aus Schritt 7 Buchstabe d. Setze für jede fehlende Angabe
   ausdrücklich "(fehlt – vor Absendung ergänzen)" ein und erfinde nichts.
10. Rückfrageliste, Tabelle mit den Spalten Nr. | Fehlende Angabe oder
    Unterlage | Wofür sie gebraucht wird | Antwort (leer).
11. Prüfvermerk für die Akte, höchstens 250 Wörter: Vorgänge, Ergebnisraster,
    Anzeigepflichtige, offene Punkte, ausdrücklicher Hinweis darauf, dass der
    Anwendungszeitpunkt der geänderten Vorschriften geprüft werden muss.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben je Vorgang einzeln. Fehlt eine Quote auf einer Zwischenebene,
   entscheide NICHT, sondern fordere sie an.
2. Nenne KEINE Beteiligungsschwelle, KEINEN Betrachtungszeitraum, KEINE
   Anzeigefrist, KEINEN Steuersatz und KEINEN Betrag als feststehenden Wert.
   Jede solche Größe nur als nachzuschlagende Angabe mit dem Zusatz
   "für [JAHR] verifizieren".
3. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV, also Norm mit Absatz und
   Satz, Erlass mit Datum oder Entscheidung mit Datum und Aktenzeichen, jeweils
   mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine Absätze, keine
   Erlasse und keine Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE Fristen im Raum stehen, je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu berechnen und
   im Fristenprogramm zu erfassen."
5. Behandle die Anzeigepflicht als eigenständige Pflicht, die unabhängig davon
   besteht, ob am Ende Steuer festgesetzt wird. Sage das ausdrücklich.
6. Weise gesondert aus, welche Fragen durch die Gesetzesänderung 2026 berührt
   sind und deshalb nicht nach älteren Merkblättern beantwortet werden dürfen.
7. ABBRUCHREGEL: Bearbeite Vorgänge, deren Anzeigefrist erkennbar bereits
   abgelaufen ist, NICHT weiter. Gib für diese Vorgänge nur aus: "Anzeichen
   für eine unterbliebene Anzeige – Bearbeitung für diesen Vorgang
   abgebrochen, Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs." Für die übrigen Vorgänge arbeite normal weiter und weise
   die abgebrochenen im Prüfvermerk gesondert aus. Deutet das Material
   zusätzlich auf eine unrichtige abgegebene Erklärung oder ein
   Steuerstrafverfahren hin, brich die gesamte Bearbeitung ab.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Vorgangstabelle (Nr. | Art | Zeitpunkt schuldrechtlich | Zeitpunkt dinglich |
   Quote | maßgebliche Fassung)
3. Prüfprotokoll je Vorgang, Schritte 4 bis 6
4. Ergebnisraster nach Schritt 8
5. Anzeigepflichten (Vorgang | Anzeigepflichtiger | Empfänger | Inhalt |
   fehlende Angaben)
6. Fristarten mit Rechtsgrundlage
7. Entwurf der Anzeige
8. Rückfrageliste
9. Prüfvermerk
10. Interne Notiz
11. Was ich nicht sicher weiß
```

## Anwendung

1. Vor dem Prompt klären, ob überhaupt Grundbesitz vorhanden ist – auch mittelbar über Tochtergesellschaften. Ohne diese Angabe läuft die gesamte Prüfung ins Leere.
2. Die Beteiligungsstruktur über alle Ebenen aufnehmen, vor und nach der Bewegung. Mittelbare Quoten sind der Punkt, an dem die Prüfung in der Praxis scheitert; eine fehlende Zwischenebene macht das Ergebnis wertlos.
3. Alle Bewegungen der letzten Jahre erfassen, nicht nur den aktuellen Vorgang. Die Ergänzungstatbestände betrachten Zeiträume, und Erbfälle, Anwachsungen und Kapitalerhöhungen zählen mit.
4. Anzeigefrist und Anwendungszeitpunkt am Gesetzestext nachschlagen, die Frist im Fristenprogramm erfassen und die Erfassung von einer zweiten Person nachprüfen lassen.
5. Den Entwurf der Anzeige vervollständigen, vom Berufsträger freigeben lassen und den Absendenachweis zur Akte nehmen. Die Anzeige ist auch dann zu erstatten, wenn die Kanzlei die Steuerbarkeit für zweifelhaft hält.

## Qualitätssicherung

- **Der Anwendungszeitpunkt wird nachgeschlagen, nicht angenommen.** Für jeden Vorgang ist die im Zeitpunkt seiner Verwirklichung geltende Fassung maßgeblich; Vorgänge aus verschiedenen Jahren können unterschiedlich zu beurteilen sein.
- **Die Ländererlasse vom 20.02.2026 sind vor dem Gesetz vom 02.07.2026 ergangen.** Sie sind daraufhin durchzusehen, ob sie den geänderten Wortlaut noch abbilden; ältere Merkblätter und Kanzleivorlagen sind auszusortieren.
- **Die Anzeigefrist berechnet und erfasst ein Mensch**, bei dieser Frist ausnahmslos mit Nachprüfung durch eine zweite Person. Kein Datum und keine Fristlänge aus der KI-Antwort übernehmen.
- **Die Anzeigepflicht trifft die Beteiligten.** Die Anzeige des Notars nach § 18 GrEStG entlastet nicht, und die Pflicht besteht unabhängig davon, ob am Ende Steuer festgesetzt wird.
- **Steuerschuldner nach der richtigen Nummer des § 13 GrEStG.** Bei § 1 Abs. 2a ist es die Personengesellschaft (Nr. 6), bei § 1 Abs. 2b die Kapitalgesellschaft (Nr. 7) – nicht der Erwerber. Wer hier Nr. 5 ansetzt, zeigt über die falsche Person an.
- **Abgebrochene Vorgänge sind nicht erledigt.** Bricht der Prompt einen Altvorgang wegen abgelaufener Anzeigefrist ab, gehört er unverzüglich zum Berufsträger; die übrigen Vorgänge laufen im Prompt weiter.
- **Mittelbare Beteiligungen vollständig aufnehmen.** Eine nicht erfasste Zwischenebene ist kein Detail, sondern der häufigste Grund für ein falsches Ergebnis.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Vorgangstabelle, Quoten und Fristerfassung nach. Die Anzeige an das Finanzamt und jede Auskunft an den Mandanten gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** dem Grunderwerbsteuergesetz im amtlichen Volltext (gesetze-im-internet.de), insbesondere § 1, §§ 3, 5, 6, 6a, § 13, § 16, § 17, §§ 18 bis 20 und § 24 GrEStG einschließlich der Anwendungsvorschriften, dem Neunten Gesetz zur Änderung von Vorschriften im Steuerberatungsrecht sowie im Steuerrecht (BGBl. 2026 I Nr. 197 vom 02.07.2026), den gleich lautenden Ländererlassen vom 20.02.2026 zu § 1 Abs. 2a und Abs. 2b GrEStG sowie DATEV LEXinform.

## Varianten

- **Nur Anzeigepflicht:** „Beschränke dich auf Schritt 7 und den Entwurf der Anzeige und behandle die Steuerbarkeit ausdrücklich als offen."
- **Vor der Umstrukturierung:** „Beurteile die geplante Struktur vorab, benenne je Zwischenschritt den in Betracht kommenden Ergänzungstatbestand und die Angaben, die für eine sichere Beurteilung fehlen – ohne Frist und ohne Betrag."
- **Erbfall und vorweggenommene Erbfolge:** „Vertiefe Schritt 5, stelle die in Betracht kommenden Befreiungen für Erwerbe von Todes wegen und durch Angehörige gegenüber und benenne je Befreiung die Behaltensregelungen als nachzuschlagende Größen."
- **Bestandsaufnahme im Mandat:** „Erstelle ohne konkreten Vorgang eine Aufstellung aller grundbesitzenden Gesellschaften des Mandats mit den Beteiligungsquoten über alle Ebenen und benenne, welche Bewegungen künftig anzeigepflichtig sein können." Ergänzt Prompt 35.
