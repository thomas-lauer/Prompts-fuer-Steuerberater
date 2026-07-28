# 63 – Elektro-Dienstwagen: Bewertungsschema und Lohnabrechnungsfolgen

**Problem:** Der Mandant fragt nach dem Elektroauto; die Kanzlei muss zwischen mehreren Bewertungsansätzen, Bruttolistenpreisgrenzen je Anschaffungszeitraum, Ladestrom und Wallbox sauber unterscheiden.
**Rolle:** Lohnsachbearbeitung, Steuerberater
**DATEV-Bezug:** DATEV Lohn und Gehalt, DATEV LODAS, DATEV Arbeitnehmer online, DATEV Anlagenbuchführung
**Was du bereitstellen musst:** Antriebsart, Bruttolistenpreis zur Erstzulassung samt Sonderausstattung, Datum von Anschaffung, Erstzulassung und Überlassung, Nutzungsvereinbarung, Entfernung zur ersten Tätigkeitsstätte, Regelung zu Ladestrom und Ladeeinrichtung.
**Datensparsamkeit:** Vor dem Einfügen Name, Personalnummer, Anschrift und Kennzeichen ersetzen (`AN 1`, `Mandant A`, `Fahrzeug 1`). Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Fahrtenbuchauszüge nur ohne Ziel- und Kundennamen einfügen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachkraft für Entgeltabrechnung in einer deutschen Steuerkanzlei. Du
arbeitest streng nach Entscheidungsbaum und entscheidest keinen Schritt vor dem
vorhergehenden.

AUFGABE
Beurteile die Überlassung eines Elektro- oder Hybridfahrzeugs und leite
Abrechnung und Unternehmensfolgen ab.

KONTEXT
- Arbeitnehmer: [AN 1], Beschäftigung: [Vollzeit / Teilzeit / Minijob /
  Geschäftsführer]
- Antriebsart: [rein elektrisch / extern aufladbarer Hybrid / Brennstoffzelle /
  Verbrenner]
- Reichweite und Emissionswert laut Fahrzeugpapieren: [ANGABEN]
- Bruttolistenpreis samt Sonderausstattung: [BETRAG]
- Anschaffung: [Kauf / Leasing / Miete], Zeitpunkt: [ZEITPUNKT]
- Erstzulassung: [ZEITPUNKT], Überlassung ab: [ZEITPUNKT]
- Fahrzeug: [neu / gebraucht / Wechsel], Privatnutzung: [vereinbart / untersagt]
- Entfernung zur ersten Tätigkeitsstätte: [KILOMETER], Tage im Monat: [ANZAHL]
- Zuzahlung: [nein / einmalig / laufend], Höhe: [BETRAG]
- Ladestrom: [beim Arbeitgeber / Erstattung nach Nachweis / pauschal /
  Ladekarte / keiner]
- Ladeeinrichtung: [keine / übereignet / überlassen / Zuschuss]
- Bisherige Abrechnung: [ANGABEN]

ENTSCHEIDUNGSBAUM – REIHENFOLGE EINHALTEN, JEDEN SCHRITT FESTHALTEN
1. Fahrzeugart: Voraussetzungen der Kategorie einzeln prüfen. Beim extern
   aufladbaren Hybrid gelten zusätzliche Anforderungen an Reichweite oder
   Emissionswert – nenne sie und prüfe sie
   (Reichweiten- und Emissionsanforderung – für [JAHR] verifizieren).
2. Zeitpunkte von Anschaffung, Erstzulassung und Überlassung: Leite ab, WELCHES
   Regime gilt, welcher Zeitpunkt maßgeblich ist und dass bei Fahrzeugwechsel neu
   zu prüfen ist (Regimewechsel – für [JAHR] verifizieren).
3. Bruttolistenpreis: Bezugsgröße, Sonderausstattung, Rabatte,
   Gebrauchtfahrzeuge; dazu die maßgebliche Grenze DIESES Zeitraums
   (Bruttolistenpreisgrenze – für [JAHR] verifizieren) und die Folge eines
   Überschreitens.
4. Bewertungsmethode pauschal oder Fahrtenbuch, gegenübergestellt; Sätze nur als
   nachzuschlagend (Bewertungssatz je Fahrzeugart – für [JAHR] verifizieren).
   Führe die Anforderungen an ein ordnungsgemäßes Fahrtenbuch vollständig auf
   (zeitnah, in geschlossener Form, vollständig und fortlaufend, unveränderbar
   oder mit protokollierten Änderungen, Angaben je Fahrt, Anforderungen an
   elektronische Aufzeichnungen) und sage, wann ein Methodenwechsel zulässig ist.
4a. Zuzahlungen des Arbeitnehmers: Trenne einmalige Zuschüsse zu den
    Anschaffungskosten von laufenden Nutzungsentgelten und von
    kilometerbezogenen Entgelten. Je Fall: Anrechnung auf den Sachbezug,
    Behandlung eines übersteigenden Betrags, Verteilung über die Nutzungsdauer,
    Wirkung bei Fahrzeugwechsel und bei Beendigung des Arbeitsverhältnisses,
    Anforderungen an die schriftliche Vereinbarung, jeweils mit Rechtsgrundlage
    (Behandlung und Verteilungszeitraum – für [JAHR] verifizieren). Rechne nicht,
    stelle den Rechenweg dar.
5. Fahrten zur ersten Tätigkeitsstätte gesondert: monatliche gegenüber
   tagesbezogener Bewertung mit Voraussetzung, Aufzeichnung,
   Entfernungspauschale und Pauschalversteuerung
   (Bewertungssatz und Tageshöchstzahl – für [JAHR] verifizieren).
6. Ladestrom getrennt: Laden beim Arbeitgeber, Erstattung nach Nachweis oder
   Pauschale, Ladekarte – je mit Steuerfolge, Rechtsgrundlage und Nachweis
   (Ladestrompauschalen – für [JAHR] verifizieren). Befreiungen können befristet
   sein.
7. Ladeeinrichtung: Übereignung, Überlassung und Zuschuss getrennt nach
   Steuerpflicht, Pauschalierung und Nachweis; Eigentum nach Ende des
   Arbeitsverhältnisses.
8. Unternehmensseite: Abschreibung, Sonderabschreibung mit Voraussetzungen,
   Vorsteuerabzug, unentgeltliche Wertabgabe und Bemessungsgrundlage – die nicht
   zwingend dem lohnsteuerlichen Sachbezug entspricht.
8a. Sozialversicherung: Der Sachbezug ist Arbeitsentgelt. Prüfe die
    Beitragspflicht, ob eine lohnsteuerliche Befreiung oder Pauschalierung in die
    Beitragspflicht durchschlägt, und – bei geringfügiger Beschäftigung – ob die
    Geringfügigkeitsgrenze durch den Sachbezug überschritten wird; dann Prompt 64
    anwenden und hier abbrechen (Rechtsgrundlagen für [JAHR] verifizieren).

HAFTUNG
Halte fest: Der Arbeitgeber haftet für die Lohnsteuer; ein Bewertungsfehler
trifft rückwirkend alle Monate bis zur Lohnsteuer-Außenprüfung. Benenne die
Haftungsnorm.

WEITERE ERGEBNISSE
9. Berechnungsbeispiel mit PLATZHALTERN: Rechenweg als Formel, ohne eine
   einzige Zahl.
10. Mitarbeiterinformation, höchstens 250 Wörter, Sie-Form, ohne Betrag, mit den
    beizubringenden Nachweisen.
11. Antwortschreiben an den Mandanten, höchstens 300 Wörter, mit den vor der
    Beschaffung zu treffenden Entscheidungen.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Fehlt ein Zeitpunkt, entscheide Schritt 2 nicht.
2. Nenne KEINEN Prozentsatz, keine Bruttolistenpreisgrenze, Pauschale,
   Höchstzahl und keinen Anwendungszeitraum als feststehend – nur als
   nachzuschlagend mit dem Zusatz "für [JAHR] verifizieren".
3. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV (Norm, Richtlinie oder
   BMF-Schreiben mit Datum) mit dem Zusatz "für [JAHR] verifizieren"; bist du
   unsicher, schreibe "Fundstelle offen – bitte recherchieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE im Raum stehen, je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum, und
   ergänze: "Frist von einem Menschen zu berechnen und im Fristenprogramm zu
   erfassen."
5. Nenne die typischen Fehlerquellen dieses Falls.

AUSGABEFORMAT
1. Eindeutigkeit 2. Entscheidungsbaum 1 bis 8 einschließlich 4a und 8a mit
Rechtsgrundlagen 3. Haftung
4. Berechnungsbeispiel 5. Fristarten 6. Handlungsanweisung
7. Mitarbeiterinformation 8. Antwortschreiben 9. Interne Notiz 10. Was ich nicht
sicher weiß
```

## Anwendung

1. Fahrzeugpapiere, Preisnachweis und Nutzungsvereinbarung vorher beschaffen; Mandantenerinnerung genügt nicht.
2. Je Fahrzeug und Überlassungszeitraum ausführen, bei Wechsel neu.
3. Ergebnis in LODAS bzw. Lohn und Gehalt als Sachbezug erfassen, Fahrten getrennt schlüsseln.
4. Nachweise zu Ladestrom und Ladeeinrichtung zum Lohnkonto, sonst trägt die Befreiung nicht.
5. Berechnungsbeispiel in die Kanzleivorlage übernehmen, selbst mit Zahlen füllen.

## Qualitätssicherung

- **Der Arbeitgeber haftet.** Ein Bewertungsfehler trifft rückwirkend alle Monate und wird von der Lohnsteuer-Außenprüfung im Block aufgedeckt. **Bei Zweifeln nicht „vorsichtig" abrechnen, sondern klären.** Ein zu hoher Sachbezug ist ebenso fehlerhaft wie ein zu niedriger und wirkt in die Sozialversicherung durch. Bei offenem Bewertungsansatz vor der ersten Abrechnung eine Anrufungsauskunft nach § 42e EStG erwägen (für [JAHR] verifizieren).
- **Sätze, Grenzen und Pauschalen nie aus der KI-Antwort übernehmen** – sie hängen am Anschaffungszeitpunkt.
- **Maßgeblichen Zeitpunkt selbst nachschlagen** – Anschaffung, Erstzulassung und Überlassung fallen auseinander; der falsche Zeitpunkt ergibt den falschen Satz.
- **Fahrtenbuch vor der Methodenwahl bewerten** – ein fehlerhaftes führt rückwirkend zur pauschalen Bewertung.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Fahrzeugart, Zeitpunkt, Bruttolistenpreis, Bewertungssatz und die Fahrtenbewertung nach; beide Schreiben gibt ein Berufsträger frei (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 6 Abs. 1 Nr. 4, § 8 Abs. 2, § 3 Nr. 46 i.V.m. § 52 Abs. 4, § 7 Abs. 2a, § 42d und § 42e EStG sowie § 14 SGB IV und § 1 Sozialversicherungsentgeltverordnung (gesetze-im-internet.de), R 8.1 LStR, den BMF-Schreiben zur Kfz-Überlassung und zum Laden sowie DATEV LEXinform.

## Varianten

- **Vor der Beschaffung:** „Beurteile nur die Schritte 1 bis 4 und stelle zwei Varianten gegenüber."
- **Gesellschafter-Geschäftsführer:** „Prüfe eine verdeckte Gewinnausschüttung bei Nutzung ohne Vereinbarung, mit Rechtsgrundlage."
- **Nur Ladeinfrastruktur:** „Beurteile nur die Schritte 6 und 7 und erstelle eine Nachweisliste für das Lohnkonto."
- **Fahrtenbuch:** „Erstelle eine Anleitung mit den Mindestangaben je Fahrt."
- **Minijob:** Prompt 64.
