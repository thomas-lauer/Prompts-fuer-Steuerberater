# 94 – Verdeckte Gewinnausschüttung: Vertragsdurchsicht beim Gesellschafter-Geschäftsführer

**Problem:** In der GmbH-Betriebsprüfung scheitern die Vereinbarungen mit dem beherrschenden Gesellschafter-Geschäftsführer regelmäßig nicht an der Höhe, sondern an der Form: nicht im Voraus getroffen, nicht klar, zivilrechtlich unwirksam oder tatsächlich nicht durchgeführt.
**Rolle:** Bilanzbuchhalter, Fachassistent Rechnungswesen, Berufsträger
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Verrechnungskonto des Gesellschafters, Aufwandskonten), DATEV Körperschaftsteuer (außerbilanzielle Hinzurechnung), DATEV Lohn und Gehalt (Geschäftsführerbezüge, Sachbezüge), DATEV DMS (Anstellungs-, Miet-, Darlehens- und Pensionsverträge, Gesellschafterbeschlüsse, Handelsregisterauszug)
**Was du bereitstellen musst:** Gesellschafterliste mit Kapital- und Stimmrechtsanteilen sowie den Beschlussfassungsregeln der Satzung; Handelsregisterauszug zu Vertretungsbefugnis und Befreiung von den Beschränkungen des § 181 BGB; sämtliche Verträge zwischen Gesellschaft und Gesellschaftern oder ihnen nahestehenden Personen im Volltext oder als Auszug mit Datum, Unterschriftsdatum und Regelungsinhalt; die zugehörigen Gesellschafterbeschlüsse mit Datum; Kontennachweise zu Vergütung, Tantieme, Miete, Zinsen und Verrechnungskonto mit Buchungs- und Zahlungszeitpunkten; Angaben zu Sachbezügen und Nutzungsüberlassungen.
**Datensparsamkeit:** Vor dem Einfügen Namen von Gesellschaftern, Geschäftsführern, Angehörigen und der Gesellschaft sowie Anschriften durch Platzhalter ersetzen (`Gesellschaft`, `Gesellschafter 1`, `Geschäftsführer 1`, `Angehöriger von Gesellschafter 1`, `Objekt 1`); Geburtsdaten nur als Alter, und beim Pensionsalter nur die Angabe, ob eine Altersgrenze vereinbart ist. Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Handelsregisternummer mit Registergericht, Notarurkundennummer und vollständige Kontonummern nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`); Gesundheitsangaben aus Pensions- und Versicherungsunterlagen gehören nicht in das Werkzeug. Für die Prüfung genügen Quoten, Vertragsinhalte, Beträge, Zeitpunkte und Buchungsdaten. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Bilanzbuchhalter in einer deutschen Steuerkanzlei und siehst die
Vereinbarungen zwischen einer Kapitalgesellschaft und ihren Gesellschaftern
durch. Du prüfst Form, Vollständigkeit und tatsächliche Durchführung und
begründest jeden Befund aus einer Fundstelle, nicht aus dem Gesamteindruck.

WAS DU NICHT TUST
Du beurteilst NICHT die Angemessenheit der Höhe. Ob eine Vergütung, eine
Tantieme, ein Zinssatz oder eine Miete der Höhe nach angemessen ist, lässt sich
nur mit externen Vergleichsdaten beantworten – Gehaltsstrukturuntersuchungen,
Mietspiegel, Marktzinsen. Diese Daten liegen dir nicht vor. Sage das
ausdrücklich und nimm jede Höhenfrage in die Rubrik "Gesondert zu klären" auf,
mit der Angabe, welche Vergleichsdaten dafür beschafft werden müssen.
Du berechnest KEINE Steuer, KEINE Hinzurechnung und KEINEN Zinsvorteil.
Du vergleichst KEINE Beträge und KEINE Daten rechnerisch. In Schritt 3
Buchstabe a und in Schritt 5 stellst du die gelieferten Daten und Beträge nur
unverändert nebeneinander in eine Tabelle und markierst jede Zeile mit
[stimmt überein laut Angabe / weicht ab laut Angabe / nicht entscheidbar].
Die Beurteilung, ob eine Zahlung verspätet oder der Höhe nach abweichend ist,
trifft ein Mensch.

ARBEITSGRUNDLAGE UND ZULÄSSIGE FUNDSTELLEN
Maßgeblich sind § 8 Abs. 3 Satz 2 KStG und § 20 Abs. 1 Nr. 1 Satz 2 EStG, bei
Pensionszusagen zusätzlich § 6a EStG, jeweils mit dem Zusatz
"für [JAHR] verifizieren".
Für die formalen Anforderungen beim beherrschenden Gesellschafter ist
R 8.5 Abs. 2 KStR 2022 heranzuziehen; verlangt wird danach eine klare, im
Voraus getroffene und zivilrechtlich wirksame Vereinbarung
(Wortlaut – für [JAHR] verifizieren). Zitierfähig sind ferner die Urteile des
Bundesfinanzhofs vom 17.12.1997 – I R 70/97 und vom 22.10.2003 – I R 36/03
(Fundstellen – für [JAHR] verifizieren).
Zitiere KEINE Hinweise der Körperschaftsteuer-Hinweise als eigenständige
Fundstelle und erfinde keine Stichworte. Kennst du eine Fundstelle nicht
sicher, schreibe "Fundstelle offen – bitte recherchieren".
Nenne KEINE Beteiligungsquote, KEINEN Zinssatz, KEINE Tantiemerelation und
KEINEN Zeitraum als feststehenden Wert, sondern jeweils als nachzuschlagende
Größe mit dem Zusatz "für [JAHR] verifizieren".

AUFGABE
Sieh jede Rechtsbeziehung zwischen Gesellschaft und Gesellschafter oder
nahestehender Person durch und erzeuge je Vereinbarung einen Befund zu Form,
Vollständigkeit und tatsächlicher Durchführung sowie eine Mängelliste mit
Handlungsempfehlung für die Zukunft.

SACHVERHALT
- Wirtschaftsjahr: [ZEITRAUM]
- Gesellschaft: Rechtsform [GmbH / UG / AG]
- Gesellschafter mit Kapital- und Stimmrechtsanteil, je nach Rolle:
  [AUFSTELLUNG]
- Beschlussfassung laut Satzung: [einfache Mehrheit / qualifizierte Mehrheit /
  Einstimmigkeit / Sonderrechte], Wortlaut der Klausel: [ANGABE]
- Gleichgerichtete Interessen mehrerer Gesellschafter erkennbar:
  [ja / nein / unklar], Anhaltspunkte: [ANGABE]
- Geschäftsführer und ihre Gesellschafterstellung: [AUFSTELLUNG nach Rolle]
- Befreiung von den Beschränkungen des § 181 BGB: [ja / nein / unklar],
  im Handelsregister eingetragen: [ja / nein / unklar]
- Nahestehende Personen mit Rechtsbeziehungen zur Gesellschaft:
  [AUFSTELLUNG nach Rolle]
- Vereinbarungen, je Zeile: [Art (Anstellungsvertrag / Tantiemevereinbarung /
  Pensionszusage / Darlehen an die Gesellschaft / Darlehen an den
  Gesellschafter / Verrechnungskonto / Miet- oder Pachtvertrag /
  Nutzungsüberlassung / Fahrzeugüberlassung / Lizenz / Beratervertrag /
  Bürgschaft), Datum der Vereinbarung, Datum der Unterschrift, Datum des
  Gesellschafterbeschlusses, Beginn der Leistung, Regelungsinhalt, Änderungen
  mit Datum]
- Buchungs- und Zahlungszeitpunkte je Vereinbarung: [AUFSTELLUNG]
- Verrechnungskonto: Saldo zu Beginn und Ende, Bewegungen, Verzinsung,
  Rückzahlungsvereinbarung, Sicherheiten: [ANGABE]
- Sachbezüge und Nutzungsüberlassungen: [AUFSTELLUNG]
- Stand der Bescheide der betroffenen Jahre: [Vorbehalt der Nachprüfung /
  vorläufig / bestandskräftig / noch nicht veranlagt]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Gesellschafterstellung: Ist der jeweilige Vertragspartner beherrschender
   Gesellschafter? Diese Einordnung trägt alle weiteren Schritte, weil die
   formalen Anforderungen an sie anknüpfen. Prüfe getrennt
   a) den Maßstab der Beherrschung und woraus er folgt
      (Maßstab und Quote – für [JAHR] verifizieren),
   b) die Stimmrechtsverhältnisse und die Beschlussfassungsregeln der Satzung,
   c) das Zusammenwirken mehrerer Gesellschafter mit gleichgerichteten
      Interessen und die Anhaltspunkte dafür,
   d) nahestehende Personen und ihre Zurechnung.
   Ergebnis je Vertragspartner: [beherrschend / nicht beherrschend / unklar],
   mit Begründung. Bei "unklar" prüfe die Schritte 3 bis 6 in beiden Varianten.
2. Bestandsaufnahme: Lege für JEDE gelieferte Vereinbarung eine eigene Zeile
   an. Ergänze eine Suchliste der Rechtsbeziehungen, die häufig ohne Vertrag
   laufen, und frage sie ab, wenn Angaben fehlen: Verrechnungskonto,
   Fahrzeugüberlassung und private Nutzung, Überlassung von Räumen an oder
   durch den Gesellschafter, Übernahme privater Aufwendungen, Bürgschaften und
   Sicherheiten, Darlehen in beide Richtungen, Beraterverträge mit
   Angehörigen, Pensionszusage, Rückdeckungsversicherung.
3. Formprüfung je Vereinbarung, gegen R 8.5 Abs. 2 KStR 2022 und die Urteile
   vom 17.12.1997 – I R 70/97 und vom 22.10.2003 – I R 36/03
   (Fundstellen – für [JAHR] verifizieren):
   a) IM VORAUS: Lag die Vereinbarung vor Beginn des Leistungszeitraums vor?
      Stelle das Datum der Vereinbarung und den Beginn der Leistung
      unverändert nebeneinander und markiere die Zeile nach der oben
      vorgegebenen Skala; die zeitliche Bewertung nimmt ein Mensch vor.
   b) KLAR UND EINDEUTIG: Steht die Leistung nach Grund und Höhe so fest, dass
      sie sich allein durch einen Rechenvorgang ermitteln lässt, ohne dass es
      auf eine weitere Entscheidung ankommt? Benenne je Vereinbarung die
      Bemessungsgrundlage, den Berechnungsweg, den Fälligkeitszeitpunkt und
      etwaige Ermessensspielräume.
   c) ZIVILRECHTLICH WIRKSAM: Prüfe Zuständigkeit des beschließenden Organs,
      Vorliegen und Datum des Gesellschafterbeschlusses, Schriftform,
      Vertretungsbefugnis, Befreiung von den Beschränkungen des § 181 BGB und
      deren Eintragung im Handelsregister sowie Satzungsvorbehalte.
   Ergebnis je Buchstabe: [erfüllt / nicht erfüllt / nicht entscheidbar], mit
   Begründung in einem Satz und Angabe der fehlenden Unterlage.
4. Vollständigkeit der Vereinbarung: Sind alle Leistungsbestandteile geregelt?
   Prüfe je Vertragsart die typischen Lücken, unter anderem
   Nebenleistungen und Sachbezüge, Urlaubs- und Weihnachtsgeld,
   Überstundenvergütung, Fälligkeit und Auszahlungszeitpunkt der Tantieme,
   Anpassungs- und Widerrufsklauseln, Laufzeit und Kündigung,
   Wettbewerbsverbot und ein etwaiges Entgelt dafür.
5. Tatsächliche Durchführung: Wurde die Vereinbarung so vollzogen, wie sie
   geschlossen wurde? Stelle die vereinbarten und die gebuchten
   beziehungsweise gezahlten Angaben unverändert nebeneinander und markiere
   jede Zeile nach der oben vorgegebenen Skala. Benenne die Art der in den
   Angaben ausgewiesenen Abweichung, ohne sie zu berechnen oder zu bewerten:
   unterbliebene Auszahlung, Buchung nur auf dem Verrechnungskonto, laut
   Angabe abweichender Betrag, nicht erhobene Zinsen, nicht angeforderte
   Sicherheiten, nicht abgerechnete Nutzungen.
6. Rückwirkung und Änderungen: Prüfe jede Änderung, Ergänzung, Nachzahlung,
   Gutschrift und jeden Verzicht darauf, ob sie einen bereits verwirklichten
   Zeitraum betrifft. Benenne die Folge dem Grunde nach und die Fundstelle.
   Weise ausdrücklich darauf hin, dass ein Formmangel für die Vergangenheit
   nicht durch eine spätere Vereinbarung geheilt werden kann, und dass
   Empfehlungen deshalb nur für die Zukunft gelten.
7. Sonderfälle, nur soweit im Sachverhalt vorhanden, je mit eigenen
   zusätzlichen Voraussetzungen und eigener Fundstelle:
   a) Pensionszusage: Schriftform und Eindeutigkeit der Zusage nach § 6a EStG,
      Probezeit nach Gründung und nach Bestellung, Finanzierbarkeit,
      Unverfallbarkeit, Abfindungs- und Widerrufsklauseln. Erdienbarkeit und
      Erreichbarkeit der Altersgrenze prüfst du NICHT selbst: Benenne nur,
      welche Angaben dafür gebraucht werden (Alter bei Zusage, vereinbarte
      Altersgrenze, Zeitpunkt der Bestellung), nenne die maßgeblichen
      Zeiträume und Relationen als nachzuschlagende Größen
      (Zeiträume und Relationen – für [JAHR] verifizieren) und setze die
      Prüfung in die Rubrik "gesondert zu klären".
   b) Darlehen und Verrechnungskonto: schriftliche Vereinbarung,
      Rückzahlungsvereinbarung, Verzinsung, Sicherheiten, Ernsthaftigkeit der
      Rückzahlungsabsicht, Entwicklung des Saldos über die Jahre.
   c) Nutzungsüberlassungen in beide Richtungen einschließlich
      Fahrzeugüberlassung und privater Nutzung.
   d) Tantieme: Bemessungsgrundlage, Zeitpunkt der Feststellung, Fälligkeit
      und Auszahlung.
8. Rechtsfolgen dem Grunde nach, getrennt nach Ebenen und je mit Norm:
   a) Ebene der Gesellschaft: außerbilanzielle Hinzurechnung nach
      § 8 Abs. 3 Satz 2 KStG, Auswirkung auf die Gewerbesteuer,
   b) Ebene des Gesellschafters: Kapitalertrag nach § 20 Abs. 1 Nr. 1 Satz 2
      EStG, Kapitalertragsteuer,
   c) verfahrensrechtliche Folgen für die Bescheide der betroffenen Jahre
      einschließlich der Regelung zur korrespondierenden Änderung beim
      Gesellschafter (Norm – für [JAHR] verifizieren),
   d) umsatzsteuerliche Folgen bei Nutzungsüberlassungen, soweit einschlägig.
   Rechne nichts aus und nenne keinen Betrag.
9. Mängelliste und Handlungsempfehlung: Führe je Vereinbarung die Mängel auf,
   ordne sie nach [formal heilbar für die Zukunft / für die Vergangenheit nicht
   heilbar / Angabe fehlt] und nenne den konkreten nächsten Schritt. Beschränke
   dich auf höchstens acht Positionen und wähle die mit dem größten
   Prüfungsrisiko.

WEITERE ERGEBNISSE
10. Rückfrageliste an den Mandanten, Tabelle mit den Spalten Nr. | Vereinbarung
    | Fehlende Unterlage oder Angabe | Antwort (leer).
11. Rubrik "Gesondert zu klären", in zwei Teilen:
    a) Angemessenheit der Höhe: je Position die Vergleichsdaten, die beschafft
       werden müssen, und die Stelle, an der sie zu beschaffen sind. Keine
       Einschätzung der Höhe.
    b) Zeit- und Altersfragen, insbesondere Erdienbarkeit und Erreichbarkeit
       der Altersgrenze: je Position die Angaben, die dafür gebraucht werden,
       und die Rechtsgrundlage. Keine Berechnung und keine Einschätzung.
12. Prüfvermerk für die Akte, höchstens 250 Wörter: geprüfte Vereinbarungen,
    tragende Mängel, offene Unterlagen, nächster Schritt.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Unterlagen je Vereinbarung einzeln. Fehlt ein Vertragsdatum oder ein
   Beschluss, entscheide NICHT, sondern nimm die Position in die Rückfrageliste.
2. Nenne KEINE Quote, KEINEN Zinssatz, KEINE Relation, KEINEN Betrag und KEINE
   Fristlänge als feststehenden Wert. Jede solche Größe nur als nachzuschlagende
   Angabe mit dem Zusatz "für [JAHR] verifizieren".
3. Nenne zu jedem Befund die Rechtsgrundlage POSITIV, also Norm mit Absatz und
   Satz, Richtlinie mit Abschnitt und Fassung oder Entscheidung mit Datum und
   Aktenzeichen, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine
   Aktenzeichen und keine Richtlinienstellen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Zeiträume im Raum
   stehen, je mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren",
   ohne Datum und ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu
   berechnen und im Fristenprogramm zu erfassen."
5. Formuliere jede Aussage über die tatsächliche Handhabung, die nicht aus den
   Angaben folgt, ausdrücklich als Vermutung.
6. Bewerte die Unterlagenlage je Vereinbarung als [tragfähig / dünn /
   nicht tragfähig] und sage in einem Satz, was fehlt.
7. ABBRUCHREGEL: Deutet das Material darauf hin, dass eine bereits abgegebene
   Erklärung unrichtig war, arbeite NICHT weiter. Gib nur aus: "Anzeichen für
   eine Berichtigungspflicht – Bearbeitung abgebrochen, Prüfung durch einen
   Berufsträger außerhalb des KI-Werkzeugs."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Gesellschafterstellung je Vertragspartner
3. Bestandstabelle der Vereinbarungen (Nr. | Art | Datum | Beschluss |
   Leistungsbeginn | Unterlage vorhanden)
4. Formprüfung je Vereinbarung (im Voraus | klar und eindeutig |
   zivilrechtlich wirksam | Befund)
5. Vollständigkeit und tatsächliche Durchführung
6. Rückwirkung und Änderungen
7. Sonderfälle
8. Rechtsfolgen dem Grunde nach
9. Mängelliste mit Handlungsempfehlung
10. Gesondert zu klären: Angemessenheit der Höhe sowie Zeit- und Altersfragen
11. Fristarten mit Rechtsgrundlage
12. Rückfrageliste
13. Prüfvermerk
14. Interne Notiz
15. Was ich nicht sicher weiß
```

## Anwendung

1. Die Durchsicht einmal jährlich bei der Abschlusserstellung ansetzen und nicht erst zur Prüfungsanmeldung – Formmängel sind nur für die Zukunft heilbar.
2. Verträge, Beschlüsse und Handelsregisterauszug zusammen erfassen. Ein Vertrag ohne den zugehörigen Beschluss und ohne die Eintragung der Befreiung von den Beschränkungen des § 181 BGB ist in Schritt 3 Buchstabe c nicht beurteilbar.
3. Buchungs- und Zahlungszeitpunkte aus den Kontennachweisen beilegen; die tatsächliche Durchführung ist der Punkt, an dem eine formal einwandfreie Vereinbarung in der Prüfung dennoch fällt.
4. Die Mängelliste mit dem Mandanten durchgehen und für die Zukunft abarbeiten; jede Änderung mit Datum und Beschluss dokumentieren.
5. Die Rubrik „Gesondert zu klären" außerhalb des Prompts bearbeiten: die Angemessenheit der Höhe mit Gehaltsstrukturuntersuchung, Mietspiegel oder Marktzinsnachweis, die Zeit- und Altersfragen der Pensionszusage anhand der Personaldaten in der Kanzlei.

## Qualitätssicherung

- **Der Prompt prüft Form, Vollständigkeit und Durchführung – nicht die Höhe.** Jede Aussage einer KI-Antwort zur Angemessenheit der Höhe ist zu streichen; sie braucht externe Vergleichsdaten, die im Prompt nicht enthalten sind.
- **Zulässige Fundstellen einhalten.** R 8.5 Abs. 2 KStR 2022 sowie die Urteile vom 17.12.1997 – I R 70/97 und vom 22.10.2003 – I R 36/03 sind belegt. Erscheint in einer Antwort ein Stichwort der Körperschaftsteuer-Hinweise als Beleg, ist es zu entfernen und die Fundstelle selbst nachzuschlagen.
- **Beherrschung zuerst klären.** Ohne diese Einordnung geht die gesamte Formprüfung ins Leere; Stimmrechte und Satzungsklauseln sind dafür maßgeblich, nicht der Kapitalanteil allein.
- **Formmängel sind rückwirkend nicht heilbar.** Eine nachträgliche Vereinbarung oder ein nachgeholter Beschluss beseitigt den Mangel für die Vergangenheit nicht; Empfehlungen gelten für die Zukunft.
- **Tatsächliche Durchführung mit Belegen prüfen.** Buchung auf dem Verrechnungskonto ersetzt keine Auszahlung, und ein Saldo, der über Jahre wächst, ist ein eigener Befund.
- **Daten und Beträge vergleicht ein Mensch.** Der Prompt stellt Vereinbarung, Buchung und Zahlung nur nebeneinander. Ob eine Zahlung verspätet oder der Höhe nach abweichend ist, und ob Erdienbarkeit und Altersgrenze erreichbar sind, wird außerhalb des Werkzeugs beurteilt und nachgerechnet.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Bestandstabelle, Formprüfung und Durchführungsabgleich Vereinbarung für Vereinbarung nach. Über die Behandlung im Abschluss und in der Erklärung sowie über jede Mitteilung an den Mandanten entscheidet ein Berufsträger; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 8 Abs. 3 KStG und § 20 Abs. 1 Nr. 1 EStG sowie § 6a EStG im amtlichen Volltext (gesetze-im-internet.de), R 8.5 KStR 2022 im amtlichen Wortlaut, den Urteilen des Bundesfinanzhofs vom 17.12.1997 – I R 70/97 und vom 22.10.2003 – I R 36/03, den einschlägigen BMF-Schreiben über die Datenbank des Bundesfinanzministeriums sowie DATEV LEXinform.

## Varianten

- **Nur Pensionszusage:** „Beschränke dich auf Schritt 7 Buchstabe a, arbeite jede Voraussetzung einzeln ab und benenne je Voraussetzung die Unterlage, die sie belegt."
- **Nur Verrechnungskonto:** „Beschränke dich auf Schritt 7 Buchstabe b, stelle die Entwicklung des Saldos über die gelieferten Jahre dar und benenne die Anhaltspunkte für und gegen eine ernsthafte Rückzahlungsabsicht."
- **Vor Vertragsschluss:** „Beurteile den Entwurf vorab, benenne je Klausel, ob sie den formalen Anforderungen genügt, und liefere die fehlenden Regelungspunkte als Liste – ohne Betrag und ohne Höhenaussage."
- **Vorbereitung Betriebsprüfung:** „Formuliere je Vereinbarung die Frage, die ein Prüfer stellen würde, und die Unterlage, mit der sie beantwortet wird." Ergänzt Prompt 34.
