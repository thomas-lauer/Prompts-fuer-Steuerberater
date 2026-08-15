# 50 – Rückstellungs-Prüfschema zum Bilanzstichtag

**Problem:** Rückstellungen werden aus dem Vorjahr fortgeschrieben statt neu begründet; in der Betriebsprüfung fallen Ansatz, Bewertung und Auflösungszeitpunkt reihenweise weg.
**Rolle:** Bilanzbuchhalter, Fachassistent Rechnungswesen
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Jahresabschluss, Kontennachweise), DATEV Bilanzbericht, DATEV DMS für die Begründungen in der Handakte
**Was du bereitstellen musst:** Rückstellungsspiegel mit Bezeichnung, Vorjahressaldo, Zuführung, Verbrauch, Auflösung und Stand zum Stichtag; je Rückstellung den Sachverhalt in zwei bis drei Sätzen mit Datum des auslösenden Ereignisses; Rechtsform, Kontenrahmen, Restlaufzeitschätzung; vorhandene Berechnungsgrundlagen (Urlaubslisten, Angebote, Schriftwechsel).
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Steuernummer, Personalnummern und Namen Dritter durch Platzhalter ersetzen (`Mandant A`, `AN 1`, `Gegenseite 1`); Prozessgegner, Behörden und Vertragspartner nur nach Rolle bezeichnen. Für die fachliche Prüfung genügen Sachverhalt, Beträge, Zeitpunkte und Restlaufzeiten. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Bilanzbuchhalter in einer deutschen Steuerkanzlei und prüfst
Rückstellungen zum Bilanzstichtag. Du begründest jede Rückstellung neu aus dem
Sachverhalt und übernimmst keinen Ansatz allein deshalb, weil er im Vorjahr
gebildet wurde.

AUFGABE
Prüfe jede der unten aufgeführten Rückstellungen einzeln nach dem Prüfschema und
erzeuge je Rückstellung einen Begründungstext, der in der Handakte Bestand hat.

MANDANTENRAHMEN
- Rechtsform: [Einzelunternehmen / GbR / GmbH / UG / GmbH & Co. KG / …]
- Gewinnermittlung: [Bilanz / Bilanz mit Überleitungsrechnung]
- Kontenrahmen: [SKR03 / SKR04]
- Größenklasse nach Handelsrecht: [kleinst / klein / mittelgroß / groß]
- Einordnung durch die Finanzverwaltung für Prüfungszwecke:
  [Kleinstbetrieb / Kleinbetrieb / Mittelbetrieb / Großbetrieb / unbekannt]
  (Merkmale der Einordnung – für [JAHR] verifizieren)
- Stichtag: [STICHTAG]
- Branche und Besonderheiten: [BRANCHE UND BESONDERHEITEN]

DATEN
Rückstellungsspiegel (Konto | Bezeichnung | Vorjahr | Zuführung | Verbrauch |
Auflösung | Stand am Stichtag | Sachverhalt | geschätzte Restlaufzeit):
[SPIEGEL EINFÜGEN]

PRÜFE JEDE RÜCKSTELLUNG IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Verpflichtungsart: Außenverpflichtung gegenüber einem Dritten oder
   Innenverpflichtung? Bei Innenverpflichtungen prüfe gesondert, ob ein Ansatz
   überhaupt zulässig ist.
2. Wirtschaftliche Verursachung: Welches Ereignis hat die Verpflichtung
   verursacht, und lag es vor dem Stichtag? Nenne das Datum.
3. Wahrscheinlichkeit der Inanspruchnahme: Woraus folgt sie? Unterscheide
   konkrete Anhaltspunkte von allgemeiner Erwartung.
4. Ansatz handelsrechtlich und Ansatz steuerlich, getrennt beantworten:
   a) handelsrechtlich: Passivierungspflicht, Passivierungsverbot oder keines von
      beiden? Prüfe jede behauptete Wahlrechtsregel darauf, ob sie noch gilt –
      für Aufwandsrückstellungen bestand früher ein Wahlrecht, das aufgehoben
      wurde (Fundstelle und Fassung – für [JAHR] verifizieren).
   b) steuerlich: Greift ein eigenes steuerliches Ansatz- oder Bewertungsverbot?
      Prüfe einzeln und ausdrücklich, ob eine Sonderregel für drohende Verluste
      aus schwebenden Geschäften, für Jubiläumszuwendungen, für Verpflichtungen,
      die nur aus künftigen Einnahmen zu erfüllen sind, oder für die Bewertung
      entgegensteht. Nenne je Fall die Norm mit Absatz und Satz, jeweils mit dem
      Zusatz "für [JAHR] verifizieren".
   Führe KEINEN handelsrechtlichen Ansatz in die Steuerspalte über, ohne b)
   geprüft und das Ergebnis festgehalten zu haben.
5. Bewertung, getrennt in zwei Spalten:
   a) handelsrechtlich: Erfüllungsbetrag, künftige Preis- und
      Kostensteigerungen, Abzinsung bei Restlaufzeit über einem Jahr
      (Schwelle und Zinssatz – für [JAHR] verifizieren)
   b) steuerlich: Bewertungsvorbehalt und Bewertungsgrenzen
      (Wertansatz und Abzinsungsregel – für [JAHR] verifizieren)
   Weichen a) und b) ab, benenne Abweichung, Höhe und Folge für die
   Überleitungsrechnung oder die latenten Steuern.
6. Auflösung: Ist der Grund entfallen, teilweise entfallen oder fortbestehend?
   Nenne den Zeitpunkt, zu dem aufzulösen ist, und die Begründung.

SONDERFÄLLE, SOWEIT IM SPIEGEL VORHANDEN, JE MIT DEN ZUSÄTZLICHEN
VORAUSSETZUNGEN UND DER TYPISCHEN ANGRIFFSFLÄCHE IN DER PRÜFUNG
Instandhaltung mit Nachholfrist (Frist – für [JAHR] verifizieren), Kosten einer
Betriebsprüfung, Aufbewahrung von Geschäftsunterlagen, Urlaub, Jubiläum,
drohende Verluste aus schwebenden Geschäften, Gewährleistung, Prozesskosten.
Bei den Kosten einer Betriebsprüfung benenne, WELCHE Einordnung des Betriebs für
den Ansatz maßgeblich ist, woraus sie folgt und was gilt, wenn sie unbekannt ist
(Fundstelle – für [JAHR] verifizieren).

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: Was ist aus dem Spiegel
   entscheidbar, was nicht, welche Angaben fehlen je Rückstellung?
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
3. Nenne keine Prozentsätze, Zinssätze, Betragsgrenzen und Fristlängen als
   feststehend. Jeder solche Wert erhält den Zusatz "für [JAHR] verifizieren".
4. Rechne keinen Betrag vor, den die Daten nicht hergeben. Fehlt eine
   Bewertungsgrundlage, benenne sie als fehlend statt zu schätzen.
5. Formuliere jede Ursachen- oder Wahrscheinlichkeitsaussage als Vermutung,
   solange sie nicht aus den Angaben folgt.
6. Bewerte die Begründungslage je Rückstellung als [tragfähig / dünn /
   nicht tragfähig] und sage in einem Satz, was fehlt.
7. ABBRUCHREGEL: Deutet das Material darauf hin, dass eine bereits abgegebene
   Erklärung unrichtig war, arbeite NICHT weiter. Gib nur aus: "Anzeichen für
   eine Berichtigungspflicht – Bearbeitung abgebrochen, Prüfung durch einen
   Berufsträger außerhalb des KI-Werkzeugs."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Prüfprotokoll je Rückstellung (Schritte 1 bis 6, danach der
   Begründungstext für die Handakte in höchstens acht Sätzen)
3. Tabelle Bewertungsvergleich (Rückstellung | handelsrechtlich |
   steuerlich | Abweichung | Folge)
4. Liste "Begründung im Prüfungsfall zu dünn" mit dem, was je Position
   nachzudokumentieren ist
5. Aufzulösende Rückstellungen mit Zeitpunkt
6. Interne Notiz (was vor der Abschlussfreigabe geklärt sein muss)
7. Was ich nicht sicher weiß
```

## Anwendung

1. Rückstellungsspiegel aus Kanzlei-Rechnungswesen ziehen und je Position den Sachverhalt in zwei Sätzen ergänzen – ohne Sachverhalt liefert der Prompt nur Allgemeinplätze.
2. Prompt ausführen, das Prüfprotokoll in die Handakte übernehmen und dort ergänzen, wo Belege fehlen.
3. Die Liste der dünn begründeten Rückstellungen vor dem Abschlussgespräch abarbeiten; offene Punkte in die Mandantenrückfrage übernehmen.
4. Bewertungsvergleich gegen die Überleitungsrechnung stellen und Abweichungen nachziehen.
5. Begründungstexte als Vorlage sichern, aber jedes Jahr neu gegen den Sachverhalt prüfen.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Verwendung prüfen: Verursachungszeitpunkt je Rückstellung, Ansatzverbote, Abzinsung und die Trennung handelsrechtlich/steuerlich.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person zeichnet den Rückstellungsspiegel Position für Position ab. Über Ansatz und Bewertung entscheidet ein Berufsträger; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- Jeden Betrag selbst nachrechnen; Abzinsungsrechnungen des Modells sind nicht belastbar.
- **Rechtsstand prüfen an:** § 249, § 253 HGB und § 5 – insbesondere § 5 Abs. 2a, 4, 4a EStG – sowie § 6 Abs. 1 Nr. 3a EStG im amtlichen Volltext (gesetze-im-internet.de), einschlägige BMF-Schreiben über die Datenbank des Bundesfinanzministeriums, Abzinsungssätze über die Bekanntmachungen der Deutschen Bundesbank sowie DATEV LEXinform.
- Fehlt zu einer Rückstellung ein Beleg, ist das ein Befund: nicht dokumentierte Rückstellungen fallen in der Prüfung zuerst.

## Varianten

- **Nur Personalrückstellungen:** Zusatz "Beschränke dich auf Urlaub, Jubiläum, Tantieme und Altersvorsorge und nenne je Position die Berechnungsgrundlage, die die Kanzlei anfordern muss."
- **Vorbereitung Betriebsprüfung:** Zusatz "Formuliere je Position die Frage, die ein Prüfer stellen würde." Ergänzt Prompt 34.
- **Erstjahr eines Mandats:** Zusatz "Behandle jede Rückstellung als neu und kennzeichne, was vom Vorberater anzufordern ist." Ergänzt Prompt 22.

## Als Skill

Für die wiederkehrende Auswertung gibt es diesen Prompt auch als ausführende
Skill: [skills/03-jahresabschluss/50-rueckstellungen-pruefschema/](../../skills/03-jahresabschluss/50-rueckstellungen-pruefschema/).
Sie führt den Rückstellungsspiegel Position für Position durch dasselbe
Sechs-Schritte-Raster, fragt je Position nur die fehlenden Sachverhalts- und
Datumsangaben nach und protokolliert den steuerlichen Ansatz getrennt vom
handelsrechtlichen, statt den Handelsbilanzwert zu übernehmen.
