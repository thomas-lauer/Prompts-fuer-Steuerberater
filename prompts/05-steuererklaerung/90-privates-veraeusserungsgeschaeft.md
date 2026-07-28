# 90 – Privates Veräußerungsgeschäft § 23 EStG prüfen

**Problem:** Der Mandant meldet den Immobilienverkauf erst mit der Steuererklärung; dann ist rückwirkend zu klären, ob überhaupt eine entgeltliche Veräußerung vorliegt, wessen Anschaffung zählt und ob die Nutzung zu eigenen Wohnzwecken trägt – der Zeitraum ist stichtagsscharf und nicht reparabel.
**Rolle:** Sachbearbeiter Steuern, Fachassistent, Berufsträger
**DATEV-Bezug:** DATEV Einkommensteuer (Anlage SO, private Veräußerungsgeschäfte), DATEV Meine Steuern oder DATEV DMS (Kaufverträge, Übergabeprotokolle, Meldenachweise, Scheidungsfolgenvereinbarung), DATEV Anlagenbuchführung, soweit das Objekt zeitweise zum Betriebsvermögen gehörte
**Was du bereitstellen musst:** Anschaffungsvorgang mit Datum des obligatorischen Verpflichtungsgeschäfts und Art des Erwerbs (Kauf, Erbfall, Schenkung, Erbauseinandersetzung, Übertragung gegen Gegenleistung, Entnahme oder Betriebsaufgabe); Veräußerungsvorgang mit Datum des obligatorischen Verpflichtungsgeschäfts, bei Enteignung und Zwangsversteigerung stattdessen der maßgebliche Vorgang mit Datum, und der vollständigen Gegenleistung einschließlich übernommener Verbindlichkeiten, Ausgleichs- und Abstandszahlungen; Objektbeschreibung mit Flächen und deren Nutzung im Zeitverlauf (Selbstnutzung, Vermietung, betriebliche Nutzung, Leerstand) mit Zeiträumen; Angaben zu Miteigentumsanteilen und zu Trennungs- oder Scheidungsvereinbarungen; Zahl und Zeitpunkte weiterer Grundstücksgeschäfte der letzten Jahre; Stand der Bescheide der betroffenen Jahre.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Namen von Ehegatten, Kindern, Miteigentümern und Erwerbern sowie die Anschrift des Objekts durch Platzhalter ersetzen (`Mandant A`, `Miteigentümer 1`, `Erwerber 1`, `Objekt 1`); die Lage nur als Kategorie, Geburtsdaten nur als Alter. Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Grundbuchblatt und Flurstücksangaben nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`); Angaben zu Trennung und Scheidung nur so weit, wie sie für die Entgeltlichkeit gebraucht werden, ohne persönliche Einzelheiten. Für die Prüfung genügen Erwerbsart, Zeitpunkte, Flächen, Nutzungsarten und Zeiträume. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Sachbearbeiter Steuern in einer deutschen Steuerkanzlei und prüfst ein
privates Veräußerungsgeschäft mit einem Grundstück. Du arbeitest streng nach
Tatbestandsmerkmalen und beantwortest jede Frage aus den gelieferten Angaben
oder gar nicht.

WAS DU NICHT TUST
Du berechnest KEINE Frist, kein Datum und keinen Zeitraum. Du ermittelst
KEINEN Veräußerungsgewinn, keine Anschaffungskosten und keine Abschreibungs-
korrektur. Du erhebst den Sachverhalt, prüfst Entgeltlichkeit und
Befreiungstatbestand und benennst, was für eine Entscheidung noch fehlt.
Gerechnet wird außerhalb dieses Prompts von einem Menschen.

ARBEITSGRUNDLAGE
Maßgeblich sind § 22 Nr. 2 EStG, § 23 Abs. 1 Satz 1 Nr. 1 EStG einschließlich
des Ausnahmetatbestands zur Nutzung zu eigenen Wohnzwecken, § 23 Abs. 1 Satz 2
EStG (Entnahme und Betriebsaufgabe gelten als Anschaffung), § 23 Abs. 1 Satz 3
EStG (Zurechnung der Anschaffung des Rechtsvorgängers beim unentgeltlichen
Erwerb) und § 23 Abs. 2 EStG (Vorrang anderer Einkunftsarten). Nenne zu jedem
Merkmal die Norm mit Absatz und Satz und setze den Zusatz
"für [JAHR] verifizieren" dahinter.
Zur Entgeltlichkeit der Übertragung eines Miteigentumsanteils im Rahmen einer
Scheidungsfolgenvereinbarung ist die Entscheidung des Bundesfinanzhofs vom
14.02.2023 – IX R 11/21 heranzuziehen (Fundstelle und Übertragbarkeit auf den
vorliegenden Sachverhalt – für [JAHR] verifizieren).
Nenne den maßgeblichen Zeitraum zwischen Anschaffung und Veräußerung, die
Nutzungszeiträume des Ausnahmetatbestands und die Freigrenze NICHT als Zahl,
sondern jeweils als nachzuschlagende Größe mit dem Zusatz
"für [JAHR] verifizieren".

AUFGABE
Erhebe den Sachverhalt vollständig, prüfe die Tatbestandsmerkmale in der
vorgegebenen Reihenfolge und erzeuge eine Liste der Angaben und Nachweise, die
noch fehlen.

SACHVERHALT
- Veranlagungszeitraum: [ZEITRAUM]
- Objektart: [unbebautes Grundstück / Einfamilienhaus / Eigentumswohnung /
  Mehrfamilienhaus / grundstücksgleiches Recht / gemischt genutztes Objekt]
- Erworbener Anteil: [Alleineigentum / Miteigentumsanteil, Quote /
  Erbengemeinschaft]
- Art des Erwerbs: [Kauf / Schenkung / Erbfall / Erbauseinandersetzung /
  Übertragung gegen Gleichstellungsgeld oder Nießbrauch / Tausch / Entnahme
  oder Betriebsaufgabe, gilt als Anschaffung]
- Datum des obligatorischen Verpflichtungsgeschäfts beim Erwerb: [DATUM]
- Beim unentgeltlichen Erwerb: Erwerbsart und Datum des Verpflichtungsgeschäfts
  des Rechtsvorgängers: [ANGABE]
- Art der Veräußerung: [Verkauf / Übertragung in einer Scheidungsfolgen-
  vereinbarung / Übertragung gegen Übernahme von Verbindlichkeiten / Tausch /
  Enteignung / Zwangsversteigerung / Einbringung]
- Datum des obligatorischen Verpflichtungsgeschäfts bei der Veräußerung: [DATUM]
- Bei Enteignung oder Zwangsversteigerung, wo es kein Verpflichtungsgeschäft
  gibt: maßgeblicher Vorgang und sein Datum: [ANGABE]
- Gegenleistung insgesamt, einschließlich übernommener Verbindlichkeiten,
  Ausgleichs- und Abstandszahlungen sowie vorbehaltener Rechte: [AUFSTELLUNG]
- Zugehörigkeit zum Betriebsvermögen in der Haltezeit: [nein / ja, Zeitraum und
  Umfang]
- Nutzung im Zeitverlauf, je Fläche und Zeitraum: [AUFSTELLUNG mit
  Selbstnutzung, Vermietung, unentgeltlicher Überlassung, betrieblicher
  Nutzung, häuslichem Arbeitszimmer, Leerstand]
- Bei Überlassung an Kinder: Anspruch auf Kindergeld oder Freibetrag im
  Überlassungszeitraum: [ja / nein / unklar]
- Bei Trennung oder Scheidung: Auszug eines Miteigentümers am [DATUM],
  weitere Nutzung durch: [ANGABE]
- Weitere Grundstücksgeschäfte der letzten Jahre: [ANZAHL und ZEITPUNKTE]
- Weitere private Veräußerungsgeschäfte im Veranlagungszeitraum: [ANGABE]
- Stand der Bescheide der betroffenen Jahre: [Vorbehalt der Nachprüfung /
  vorläufig / bestandskräftig / noch nicht veranlagt]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Gegenstand: Handelt es sich um ein Grundstück, einen Grundstücksteil oder
   ein grundstücksgleiches Recht? Benenne, ob mehrere selbständige
   Wirtschaftsgüter vorliegen, die getrennt zu beurteilen sind, und ob
   Gebäude und Außenanlagen in die Betrachtung einzubeziehen sind, jeweils mit
   Rechtsgrundlage.
2. Zuordnung in der Haltezeit: Gehörte das Wirtschaftsgut zum Privatvermögen?
   Gab es Einlage, Entnahme oder eine betriebliche Nutzung, greift eine
   Sonderregelung oder der Vorrang einer anderen Einkunftsart
   (§ 23 Abs. 2 EStG). Steht der Vorrang im Raum, sage das ausdrücklich und
   arbeite die weiteren Schritte nur hilfsweise ab. Behandle die Entnahme und
   die Betriebsaufgabe nicht als Veräußerung: Sie gelten nach
   § 23 Abs. 1 Satz 2 EStG als Anschaffung und gehören auf die
   Anschaffungsseite der Zeitpunkttabelle
   (Rechtsgrundlage – für [JAHR] verifizieren).
3. Abgrenzung zum gewerblichen Grundstückshandel: Prüfe anhand der Zahl und
   der zeitlichen Abfolge der Grundstücksgeschäfte, ob eine gewerbliche
   Tätigkeit im Raum steht. Nenne die Kriterien und die Fundstelle, aber KEINE
   Objektzahl und KEINE Zeitspanne als feststehenden Wert
   (Kriterien und Grenzen – für [JAHR] verifizieren). Steht gewerblicher
   Grundstückshandel im Raum, ist das ein eigener Prüfauftrag außerhalb dieses
   Prompts; weise darauf hin.
4. Anschaffungsvorgang: entgeltlich, teilentgeltlich oder unentgeltlich? Beim
   unentgeltlichen Erwerb ist die Anschaffung des Rechtsvorgängers zuzurechnen
   (§ 23 Abs. 1 Satz 3 EStG); benenne dann ausdrücklich, wessen Anschaffung
   maßgeblich ist und welche Angaben dazu fehlen. Beim teilentgeltlichen
   Erwerb benenne die Aufteilung dem Grunde nach, ohne zu rechnen. Behandle
   Erbauseinandersetzung, Übertragung gegen Gleichstellungsgeld und
   Nießbrauchsvorbehalt einzeln.
5. Veräußerungsvorgang: Liegt eine entgeltliche Veräußerung vor? Prüfe
   ausdrücklich die Fälle, in denen die Entgeltlichkeit übersehen wird:
   Übertragung eines Miteigentumsanteils in einer
   Scheidungsfolgenvereinbarung, Übertragung gegen Übernahme von
   Verbindlichkeiten, Tausch. Behandle Enteignung und Zwangsversteigerung
   getrennt davon: Für die Enteignung ist geklärt, dass kein
   Veräußerungsgeschäft vorliegt (BFH vom 23.07.2019 – IX R 28/18 –
   für [JAHR] verifizieren); für die Zwangsversteigerung benenne die
   Fundstelle oder schreibe "Fundstelle offen – bitte recherchieren". In
   beiden Fällen fehlt ein obligatorisches Verpflichtungsgeschäft; trage in
   der Zeitpunkttabelle stattdessen den maßgeblichen Vorgang ein und benenne
   die Rechtsgrundlage dafür.
   Ordne den Fall zu und begründe mit Norm und, soweit
   einschlägig, mit der Entscheidung vom 14.02.2023 – IX R 11/21
   (Fundstelle – für [JAHR] verifizieren). Ist die Entgeltlichkeit nach den
   Angaben nicht entscheidbar, sage das und benenne die fehlende Angabe.
6. Maßgebliche Zeitpunkte: Stelle Anschaffung und Veräußerung tabellarisch
   gegenüber. Maßgeblich ist jeweils das obligatorische Verpflichtungsgeschäft,
   nicht Übergabe, Kaufpreiszahlung oder Grundbucheintragung
   (Rechtsgrundlage – für [JAHR] verifizieren). Fehlt ein
   Verpflichtungsgeschäft, weil der Vorgang keines kennt – Enteignung,
   Zwangsversteigerung, Entnahme, Betriebsaufgabe, Erbfall –, trage den nach
   Schritt 2 oder Schritt 5 maßgeblichen Vorgang mit seinem Datum ein und
   benenne die Rechtsgrundlage dafür. Übernimm die Daten nur aus den
   Angaben; fehlt ein Datum, trage "fehlt" ein.
7. Zeitraum: Benenne, welcher Zeitraum zwischen Anschaffung und Veräußerung
   nach § 23 Abs. 1 Satz 1 Nr. 1 EStG maßgeblich ist
   (Zeitraum – für [JAHR] verifizieren). Rechne ihn NICHT aus und sage nicht,
   ob er gewahrt ist. Ergänze: "Frist von einem Menschen zu berechnen und im
   Fristenprogramm zu erfassen."
8. Befreiungstatbestand Nutzung zu eigenen Wohnzwecken: Benenne beide
   Alternativen des Ausnahmetatbestands getrennt und jeweils mit ihrem
   Nutzungszeitraum als nachzuschlagender Größe
   (Nutzungszeiträume – für [JAHR] verifizieren). Prüfe dann je Alternative:
   a) Was zählt als Nutzung zu eigenen Wohnzwecken, und was nicht? Behandle
      Zweit- und Ferienwohnung, Leerstand vor Einzug und nach Auszug,
      unentgeltliche Überlassung an Kinder und an sonstige Angehörige jeweils
      getrennt, je mit Rechtsgrundlage.
   b) Trennungs- und Scheidungsfall: Der ausgezogene Miteigentümer nutzt in
      aller Regel nicht mehr zu eigenen Wohnzwecken. Prüfe das für jeden
      Beteiligten getrennt und benenne den Zeitpunkt des Auszugs als
      tatsächliche Angabe, nicht als rechtliches Ergebnis.
   c) Wird nur ein Teil der Fläche zu eigenen Wohnzwecken genutzt, benenne die
      Aufteilung dem Grunde nach und den Aufteilungsmaßstab, ohne zu rechnen.
      Behandle vermietete Flächen, betrieblich genutzte Räume und das
      häusliche Arbeitszimmer getrennt und benenne, ob die Rechtslage dazu
      einheitlich ist.
9. Weitere Prüfpunkte, nur benennen und nicht rechnen: Freigrenze
   (Betrag – für [JAHR] verifizieren), Verrechnung mit Verlusten aus privaten
   Veräußerungsgeschäften, Behandlung mehrerer Veräußerungen desselben
   Veranlagungszeitraums, Erklärungspflicht in der Anlage SO, Bedeutung der
   Veräußerungsanzeige an das Finanzamt.
10. Ergebnisraster: Ordne den Fall einer der folgenden Kategorien zu und
    begründe in höchstens drei Sätzen:
    (steuerbar dem Grunde nach), (nicht steuerbar wegen fehlender
    Entgeltlichkeit), (nicht steuerbar wegen Ablaufs des maßgeblichen
    Zeitraums – von einem Menschen zu berechnen), (befreit wegen Nutzung zu
    eigenen Wohnzwecken), (teilweise steuerbar), (nicht entscheidbar).
    Wähle (nicht entscheidbar), sobald eine tragende Angabe fehlt.

WEITERE ERGEBNISSE
11. Rückfrageliste an den Mandanten, Tabelle mit den Spalten
    Nr. | Fehlende Angabe oder Unterlage | Wofür sie gebraucht wird |
    Antwort des Mandanten (leer).
12. Mandantenschreiben, höchstens 250 Wörter, Sie-Form, Fachbegriffe in einem
    Halbsatz erklärt, ohne Betrag, ohne Datum und ohne Ergebniszusage: welche
    Unterlagen gebraucht werden und warum die Zeitpunkte zählen.
13. Prüfvermerk für die Akte, höchstens 200 Wörter: Unterlagenlage,
    Zuordnung nach Schritt 10, offene Punkte, nächster Schritt.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig, vertretbare
   Varianten oder nicht ohne weitere Angaben entscheidbar. Benenne die
   fehlenden Angaben einzeln.
2. Nenne KEINEN Zeitraum, KEINE Freigrenze, KEINE Objektzahl und KEINEN Betrag
   als feststehenden Wert. Jede solche Größe nur als nachzuschlagende Angabe
   mit dem Zusatz "für [JAHR] verifizieren".
3. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV, also Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum oder Entscheidung mit Datum
   und Aktenzeichen, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
   keine Paragrafen und keine Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Zeiträume im Raum
   stehen, je mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren",
   ohne Datum und ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu
   berechnen und im Fristenprogramm zu erfassen."
5. Formuliere jede Aussage zur tatsächlichen Nutzung, die nicht aus den
   Angaben folgt, ausdrücklich als Vermutung.
6. Weise gesondert aus, welche Fragen streitig oder nicht abschließend geklärt
   sind, insbesondere zur Behandlung einzelner Flächen und zur Übertragbarkeit
   der zitierten Entscheidung auf den Sachverhalt.
7. ABBRUCHREGEL: Deutet das Material darauf hin, dass ein Veräußerungsgeschäft
   eines Vorjahres nicht erklärt wurde oder eine abgegebene Erklärung unrichtig
   war, arbeite NICHT weiter. Gib nur aus: "Anzeichen für eine
   Berichtigungspflicht – Bearbeitung abgebrochen, Prüfung durch einen
   Berufsträger außerhalb des KI-Werkzeugs."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Prüfprotokoll, Schritte 1 bis 9, je mit Rechtsgrundlage
3. Zeitpunkttabelle (Vorgang | Datum laut Angabe | Quelle | fehlt)
4. Nutzungstabelle (Fläche | Zeitraum | Nutzungsart | Beleg | offen)
5. Ergebnisraster nach Schritt 10
6. Fristarten mit Rechtsgrundlage
7. Rückfrageliste
8. Mandantenschreiben
9. Prüfvermerk
10. Interne Notiz
11. Was ich nicht sicher weiß
```

## Anwendung

1. Beide notariellen Verträge heraussuchen und das Datum des Verpflichtungsgeschäfts markieren; Übergabe, Kaufpreiszahlung und Grundbucheintragung sind für die Zuordnung nicht der maßgebliche Zeitpunkt und gehören nicht in die Zeitpunkttabelle.
2. Beim unentgeltlichen Erwerb zuerst den Vorgang beim Rechtsvorgänger klären. Fehlt dessen Erwerbsdatum, ist die Prüfung nicht abschließbar – das ist die häufigste Lücke.
3. Die Nutzung im Zeitverlauf flächenscharf erfassen, mit Belegen (Meldenachweis, Mietverträge, Nebenkostenabrechnungen). Ohne diese Aufstellung liefert der Prompt zum Befreiungstatbestand nur Allgemeinplätze.
4. Zeitraum und Gewinn außerhalb des Prompts rechnen; das Ergebnisraster ist eine Vorsortierung, keine Entscheidung.
5. Bei Trennungs- und Scheidungsfällen die Scheidungsfolgenvereinbarung vollständig auswerten und den Prüfvermerk zur Akte nehmen; die Entgeltlichkeit ist hier der eigentliche Streitpunkt.

## Qualitätssicherung

- **Der maßgebliche Zeitpunkt ist das obligatorische Verpflichtungsgeschäft.** Wird stattdessen mit Übergabe oder Eintragung gerechnet, ist das Ergebnis wertlos. Beide Daten aus den Verträgen selbst nehmen, nicht aus der KI-Antwort.
- **Zeitraum und Nutzungszeiträume im Gesetzestext nachlesen.** Keine Zahl aus der KI-Antwort übernehmen; die Frist berechnet ein Mensch und erfasst sie im Fristenprogramm.
- **Entgeltlichkeit ist die Weiche, nicht der Zeitraum.** Bei Übertragungen im Zusammenhang mit Trennung, Erbauseinandersetzung oder Schuldübernahme ist die Entgeltlichkeit gesondert zu begründen und zu belegen.
- **Enteignung ist keine Veräußerung, Entnahme keine Veräußerung.** Der Eigentumsverlust durch Enteignung erfüllt § 23 EStG nicht (BFH vom 23.07.2019 – IX R 28/18); die Entnahme aus dem Betriebsvermögen gilt nach § 23 Abs. 1 Satz 2 EStG als Anschaffung und gehört auf die Anschaffungsseite. Beides in der KI-Antwort gezielt gegenprüfen.
- **Beim unentgeltlichen Erwerb zählt die Anschaffung des Rechtsvorgängers.** Fehlt sie, ist der Fall offen und nicht etwa unproblematisch.
- **Gewerblicher Grundstückshandel gesondert prüfen.** Steht er im Raum, ist § 23 EStG nicht der richtige Rahmen; das ist ein eigener Auftrag und keine Nebenbemerkung.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Zeitpunkttabelle, Entgeltlichkeit und Nutzungsaufteilung nach. Die Behandlung in der Erklärung und jedes Schreiben an Mandant oder Finanzamt gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 22 Nr. 2 und § 23 EStG im amtlichen Volltext (gesetze-im-internet.de) – dort insbesondere § 23 Abs. 1 Satz 2 und Satz 3 –, R 23 EStR und den einschlägigen BMF-Schreiben zur Nutzung zu eigenen Wohnzwecken über die Datenbank des Bundesfinanzministeriums, den Entscheidungen des Bundesfinanzhofs vom 14.02.2023 – IX R 11/21 und vom 23.07.2019 – IX R 28/18 sowie DATEV LEXinform.

## Varianten

- **Vor dem Verkauf:** „Beurteile den geplanten Verkauf vorab, benenne die Angaben, die für eine sichere Beurteilung fehlen, und die Gestaltungsfragen, die vor dem Notartermin zu entscheiden sind – ohne Datum und ohne Betrag."
- **Trennung und Scheidung:** „Vertiefe die Schritte 5 und 8 Buchstabe b, stelle die Position beider Miteigentümer getrennt dar und benenne je Position die Belege, die die Entgeltlichkeit stützen oder entkräften."
- **Gemischt genutztes Objekt:** „Vertiefe Schritt 8 Buchstabe c, bilde je Fläche eine eigene Zeile und benenne den Aufteilungsmaßstab mit Rechtsgrundlage."
- **Erbfall und Erbauseinandersetzung:** „Vertiefe Schritt 4, stelle Erwerb von Todes wegen, Auseinandersetzung und Abfindungszahlung getrennt dar und benenne je Vorgang die maßgebliche Anschaffung."
