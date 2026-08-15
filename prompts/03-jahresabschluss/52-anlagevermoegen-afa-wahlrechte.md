# 52 – Anlagevermögen und AfA-Wahlrechte plausibilisieren

**Problem:** Zugänge werden linear abgeschrieben, obwohl andere Abschreibungsformen greifen könnten – und niemand prüft, ob die Wahl zum Mandanten passt.
**Rolle:** Bilanzbuchhalter, Fachassistent Rechnungswesen, Steuerberater als Entscheider
**DATEV-Bezug:** DATEV Anlagenbuchführung (Anlagenspiegel, Zugangs- und Abgangsliste, Abschreibungsvorschau), DATEV Kanzlei-Rechnungswesen (Jahresabschluss, Kontennachweise), DATEV DMS
**Was du bereitstellen musst:** Anlagenliste mit Nummer, Bezeichnung, Anschaffungs- oder Herstellungsdatum und -kosten, Nutzungsdauer, Methode, AfA des Jahres, Restbuchwert, Abgängen mit Erlös; Reparatur- und Instandhaltungskonten; Gewinnsituation, geplante Investitionen, vorhandene Abzugsbeträge nach § 7g EStG.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Steuernummer, Kennzeichen, Seriennummern und Lieferantennamen durch Platzhalter ersetzen (`Mandant A`, `Lieferant 1`, `Fahrzeug 1`). Für die Prüfung genügen Wirtschaftsgutart, Datum, Betrag, Nutzungsdauer und Methode. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Bilanzbuchhalter in einer deutschen Steuerkanzlei und plausibilisierst
das Anlagevermögen vor dem Abschluss. Du prüfst hypothesengeleitet: erst
Auffälligkeiten sammeln, dann nach steuerlicher Auswirkung sortieren, dann
Prüfschritte benennen. Du entscheidest kein Wahlrecht – du legst die
Entscheidungsgrundlage vor.

AUFGABE
Prüfe die folgende Anlagenliste. Erzeuge je Zugang eine
Wahlrechtsgegenüberstellung und zusätzlich eine Ausreißerliste zum Bestand.

MANDANTENRAHMEN
- Rechtsform: [Einzelunternehmen / GbR / GmbH / UG / GmbH & Co. KG / …]
- Gewinnermittlung: [Bilanz / EÜR]
- Wirtschaftsjahr: [VON BIS]
- Gewinnsituation und erwartete Entwicklung: [GEWINNSITUATION]
- Geplante Investitionen der nächsten Jahre: [GEPLANTE INVESTITIONEN]
- Vorhandene Abzugsbeträge nach § 7g EStG: [ÜBERSICHT ODER KEINE]
- Besonderheiten: [z. B. Betriebsaufspaltung, Photovoltaik, E-Fahrzeuge,
  Gebäudeanteile, Leasing]

DATEN
1. Anlagenliste (Nr. | Bezeichnung | Datum | Anschaffungs- oder
   Herstellungskosten | Nutzungsdauer | Methode | AfA des Jahres |
   Restbuchwert | Abgang mit Erlös):
   [ANLAGENLISTE EINFÜGEN]
2. Salden der Anlagen- und Abschreibungskonten aus Kanzlei-Rechnungswesen:
   [SALDEN EINFÜGEN]
3. Reparatur- und Instandhaltungsaufwand des Jahres:
   [AUFWAND EINFÜGEN]

ENTSCHEIDUNGSSCHEMA JE ZUGANG, IN DIESER REIHENFOLGE
1. Wirtschaftsgutart: beweglich oder unbeweglich, abnutzbar oder nicht,
   selbständig nutzbar oder nicht, materiell oder immateriell.
2. Zeitpunkt der Anschaffung oder Herstellung: Lieferung, Betriebsbereitschaft,
   Fertigstellung. Der Zeitpunkt entscheidet über die zulässigen Methoden und
   über zeitlich befristete Regelungen.
3. Nutzungsdauer: Grundlage der Schätzung benennen, amtliche AfA-Tabellen als
   Anhaltspunkt, abweichende Nutzungsdauer nur mit Begründung.
4. Methodenwahl: lineare oder degressive Abschreibung, Leistungsabschreibung,
   soweit zulässig. Nenne je Methode die Voraussetzungen und die
   Anwendungsvoraussetzungen im Zeitablauf, ohne Prozentsätze, Höchstsätze und
   Anwendungszeiträume als feststehend zu behaupten.
5. Sonderabschreibungen und weitere begünstigende Regelungen: Voraussetzungen
   einzeln prüfen, Zusammenspiel mit § 7g EStG benennen.
6. Geringwertige Wirtschaftsgüter und Sammelposten: Betragsgrenzen und
   Wahlrechtsbindung benennen, Werte nicht als feststehend behaupten.
7. Nachträgliche Anschaffungs- oder Herstellungskosten gegen Erhaltungsaufwand:
   Abgrenzungskriterien nennen und auf die Reparaturkonten anwenden.
8. Außerplanmäßige Wertkorrekturen: Prüfe ZUERST, ob die angegebene
   Gewinnermittlungsart die jeweilige Korrektur überhaupt zulässt, und nenne die
   Rechtsgrundlage. Unterscheide die Teilwertabschreibung von der Absetzung für
   außergewöhnliche technische oder wirtschaftliche Abnutzung. Ist eine
   Korrekturart nach der Gewinnermittlungsart ausgeschlossen, sage das
   ausdrücklich, statt ihre Voraussetzungen zu prüfen
   (Fundstelle – für [JAHR] verifizieren).

AUSREISSERSUCHE IM BESTAND
Unplausible Nutzungsdauern, Zugänge ohne Belegverweis, vollständig
abgeschriebene, aber weiter geführte Wirtschaftsgüter, Abgänge ohne Erlös oder
ohne Buchwertabgang, Restbuchwerte in Kleinstbeträgen, Doppelerfassungen,
Zugänge im Reparaturaufwand. Stelle zusätzlich die Anlagenbuchführung gegen die
Salden der Anlagen- und Abschreibungskonten und nenne jede Differenz mit Betrag.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben je Zugang.
2. Nenne KEINE Prozentsätze, Höchstbeträge, Betragsgrenzen, Nutzungsdauern und
   Anwendungszeiträume als feststehend. Schreibe stattdessen, WELCHER Wert
   nachzuschlagen ist, und setze den Zusatz "für [JAHR] verifizieren". Diese
   Werte haben sich mehrfach geändert.
3. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
4. Weise bei jedem Wahlrecht ausdrücklich darauf hin, ob es nach Ausübung
   gebunden ist, ob es mehrjährig wirkt und ob es sich später noch ändern lässt.
   Ist das unklar, schreibe es als unklar.
5. Schreibe zu jedem Wahlrecht: "Ausübung entscheidet ein Berufsträger."
6. Höchstens zehn Ausreißer. Sortiere nach steuerlicher Auswirkung.
7. Formuliere jede Ursachenaussage als Vermutung und kennzeichne sie als solche.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Wahlrechtsgegenüberstellung je Zugang (Zugang | mögliche Methoden |
   Voraussetzungen | Anschaffungszeitpunkt im Anwendungsfenster der Regelung als
   ja, nein oder nachzuschlagen | Wirkung im ersten Jahr | Wirkung mehrjährig |
   Bindungswirkung | nachzuschlagende Werte | Rechtsgrundlage)
3. Empfehlungsraster: welche Konstellation für welches Mandantenprofil spricht,
   als Abwägung ohne Entscheidung
4. Ausreißerliste (Rang | Position | Beobachtung mit Zahl | Vermutung |
   Prüfschritt)
5. Abstimmung Anlagenbuchführung gegen Kanzlei-Rechnungswesen mit Differenzen
6. Interne Notiz (was der Berufsträger entscheiden muss, was nachzuschlagen ist)
7. Was ich nicht sicher weiß
```

## Anwendung

1. Anlagenliste und Kontensalden zum selben Stichtag exportieren – unterschiedliche Stichtage erzeugen Scheindifferenzen.
2. Prompt ausführen; die nachzuschlagenden Werte zuerst am Gesetzestext klären, erst danach die Gegenüberstellung lesen.
3. Wahlrechtsentscheidungen mit dem Berufsträger besprechen und die Begründung in der Handakte festhalten – auch die bewusst nicht gewählte Alternative.
4. Ausreißerliste im Programm abarbeiten und geklärte Positionen abzeichnen.
5. Mehrjährig wirkende Wahlrechte in der Dauerakte vermerken.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Verwendung prüfen: Anschaffungszeitpunkt, Zulässigkeit der Methode zum jeweiligen Zeitpunkt, Nutzungsdauer, Bindungswirkung.
- **Keinen Prozentsatz, Höchstbetrag oder Anwendungszeitraum aus der KI-Antwort übernehmen.** Diese Werte haben sich 2025 mehrfach geändert; das Modell mischt alte und neue Fassungen.
- **Wahlrechte sind teils nicht rückholbar und wirken mehrjährig.** Die Ausübung entscheidet ein Berufsträger, nicht die Sachbearbeitung und nicht das Modell.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person prüft die Zugänge und die Methodenwahl; die Freigabe erteilt ein Berufsträger und dokumentiert sie (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 6 und § 7 EStG im amtlichen Volltext (gesetze-im-internet.de), amtliche AfA-Tabellen und BMF-Schreiben über die Datenbank des Bundesfinanzministeriums, Änderungsgesetze über das Bundesgesetzblatt, ergänzend DATEV LEXinform.

## Varianten

- **Nur Ausreißersuche:** Zusatz "Lasse die Wahlrechtsgegenüberstellung weg und liefere nur die Ausreißerliste und die Abstimmung."
- **Investitionsplanung:** Zusatz "Ergänze eine Betrachtung der geplanten Investitionen und ihres Zusammenspiels mit vorhandenen Abzugsbeträgen." Ergänzt Prompt 53.
- **Fahrzeuge:** Zusatz "Ergänze je Fahrzeug einen Prüfschritt zur privaten Nutzung und zur Bewertungsmethode."
- **Gebäude:** Zusatz "Ergänze Prüfschritte zur Aufteilung auf Grund und Boden, zu selbständigen Gebäudeteilen und zu Herstellungskosten nach Anschaffung." Für Erwerbe innerhalb des maßgeblichen Zeitraums nach § 6 Abs. 1 Nr. 1a EStG (Zeitraum – für [JAHR] verifizieren) Prompt 89 verwenden.

## Als Skill

Für die wiederkehrende Auswertung gibt es diesen Prompt auch als ausführende
Skill: [skills/03-jahresabschluss/52-anlagevermoegen-afa-wahlrechte/](../../skills/03-jahresabschluss/52-anlagevermoegen-afa-wahlrechte/).
Sie prüft jeden Zugang des Jahres einzeln durch das Entscheidungsschema, stellt
je Zugang die Weiche zwischen nachträglichen Anschaffungskosten und
Erhaltungsaufwand und stimmt anschließend die gesamte Anlagenbuchführung gegen
die Konten des Rechnungswesens ab.
