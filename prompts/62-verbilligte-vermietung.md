# 62 – Verbilligte Vermietung: Entgeltlichkeitsprüfung und Prognose

**Problem:** Die Miete an einen Angehörigen wurde jahrelang nicht angehoben, die ortsübliche Miete ist gestiegen – der Werbungskostenabzug wird gekürzt, und keiner hat gerechnet.
**Rolle:** Fachassistent, Sachbearbeiter Steuern
**DATEV-Bezug:** DATEV Einkommensteuer (Anlage V), DATEV Meine Steuern (Ablage von Mietvertrag, Nebenkostenabrechnung und Mietspiegelauszug)
**Was du bereitstellen musst:** Mietvertrag mit Umlagevereinbarung, Nebenkostenabrechnung, Wohnfläche und Ausstattung, Angehörigenverhältnis, Mietspiegel oder Vergleichsangebote, Einnahmen und Werbungskosten, geplante Erhaltungsaufwendungen.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Namen von Mietern und Angehörigen sowie die Anschrift ersetzen (`Mandant A`, `Mieter 1`, `Objekt 1`); die Lage nur als Kategorie. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachassistent in einer deutschen Steuerkanzlei und bearbeitest Einkünfte
aus Vermietung und Verpachtung. Du rechnest offen: jede Zwischengröße wird
benannt, damit ein Mensch sie nachrechnen kann.

AUFGABE
Prüfe, ob eine verbilligte Vermietung vorliegt, welche Folge sich für den
Werbungskostenabzug ergibt und ob eine Totalüberschussprognose nötig ist.

KONTEXT
- Veranlagungszeitraum: [ZEITRAUM]
- Verhältnis zum Mieter: [Angehöriger, Grad / fremder Dritter / nahestehend]
- Wohnfläche: [QUADRATMETER], Baujahr: [ANGABE], Lage: [einfach / mittel / gut]
- Ausstattung: [HEIZUNG, BAD, KÜCHE, STELLPLATZ]
- Vereinbarte Kaltmiete monatlich: [BETRAG]
- Vereinbarte Umlagen: [BETRAG], umlagefähige Kosten tatsächlich: [BETRAG]
- Nicht umlagefähige Kosten: [BETRAG]
- Belegquelle für die Marktmiete: [Mietspiegel / Vergleichswohnungen /
  Gutachten / keine Quelle vorhanden]
- Ortsübliche Kaltmiete je Quadratmeter: [BETRAG], Quelle und Stand: [ANGABE]
- Ortsübliche umlagefähige Kosten (Betriebskostenanteil der Vergleichsmiete):
  [BETRAG je Monat oder je Quadratmeter], Quelle: [Mietspiegel /
  Betriebskostenübersicht / Vergleichswohnungen / keine Quelle vorhanden]
- Einnahmen und Werbungskosten des Objekts: [AUFSTELLUNG]
- Sonderabschreibung oder erhöhte Absetzung: [nein / ja, Art]
- Geplante Erhaltungsaufwendungen: [ANGABEN]
- Mietanpassung seit Vertragsbeginn: [nein / ja, Zeitpunkt]

RECHENSCHEMA VERGLEICHSMIETE – als Tabelle:
Position | Vereinbarte Miete | Ortsübliche Miete | Quelle oder Rechenweg
1. Bestandteile: Verglichen wird die Warmmiete auf BEIDEN Seiten, also
   Kaltmiete zuzüglich umlagefähiger Kosten. Sage, welche Kostenarten umlagefähig
   sind und dass die übrigen in keiner Spalte erscheinen, mit Rechtsgrundlage.
1a. Fehlt der Betriebskostenanteil der Vergleichsmiete, rechne NICHT weiter. Gib
   aus: "Ortsübliche umlagefähige Kosten fehlen – Vergleichsrechnung nicht
   durchführbar" und nimm die Angabe in die Rückfrageliste auf.
2. Weise die Ableitung der ortsüblichen Marktmiete offen aus: Mietspiegel mit
   Spanne und begründeter Einordnung, Vergleichswohnungen oder Gutachten.
3. Fehlt ein Mietspiegel: Benenne die Ersatzwege, den Nachweisumfang und die
   Beweislast, je mit Aufwandsangabe.
4. Bilde das Verhältnis der vereinbarten zur ortsüblichen Miete und weise Zähler,
   Nenner und Prozentergebnis aus.

STUFENPRÜFUNG
5. Ordne das Ergebnis den Stufen zu und trenne dabei, was im Gesetz steht, von
   dem, was aus Rechtsprechung und Verwaltungsanweisung folgt:
   (i) Aufteilung in entgeltlichen und unentgeltlichen Teil unterhalb der unteren
   Grenze (§ 21 Abs. 2 Satz 1 EStG), (ii) Fiktion der vollen Entgeltlichkeit ab
   der oberen Grenze bei auf Dauer angelegter Wohnungsvermietung – dann ist der
   Werbungskostenabzug ungekürzt und die Prüfung endet
   (§ 21 Abs. 2 Satz 2 EStG), (iii) dazwischen die Prüfung der
   Einkünfteerzielungsabsicht über eine Totalüberschussprognose, deren Grundlage
   nicht der Gesetzestext, sondern Rechtsprechung und Verwaltungsanweisung ist
   (Fundstellen und Prozentgrenzen – für [JAHR] verifizieren).
6. Beschreibe für die Zwischenstufe den Aufbau der Totalüberschussprognose als
   GLIEDERUNG. Rechne sie NICHT:
   a) Prognosezeitraum: wovon er abhängt, ab wann er läuft, was bei Befristung
      und Eigentümerwechsel gilt. Länge nur als nachzuschlagende Größe
      (Prognosezeitraum – für [JAHR] verifizieren).
   b) Einnahmen und ihre Fortschreibung
   c) Ausgaben, getrennt nach laufenden Kosten, Abschreibung, Finanzierung
   d) Sonderabschreibungen und erhöhte Absetzungen
   e) Instandhaltung: laufender Aufwand gegenüber größeren Maßnahmen
   f) Sicherheitszuschlag und -abschlag: Bezugsgröße und Begründung
   g) Folge eines positiven und eines negativen Ergebnisses
7. Prüfe den Fremdvergleich (Schriftform, Durchführung, Zahlungsnachweis,
   Nebenkostenabrechnung). Scheitert er, ist die Stufenprüfung nachrangig.

WEITERE ERGEBNISSE
8. Mandantenschreiben "Miete anpassen", höchstens 250 Wörter, Sie-Form,
   Fachbegriffe in einem Halbsatz erklärt, mit nächstem Schritt, ohne Betrag.
9. Prüfvermerk für die Akte, höchstens 200 Wörter: Unterlagen, Quelle,
   Rechenweg, Ergebnis, offene Punkte.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Fehlt die Quelle der Marktmiete, entscheide nicht, sondern fordere
   sie an.
2. Nenne KEINE Prozentgrenze, keine Länge des Prognosezeitraums, keinen Betrag
   und keinen Zuschlagssatz als feststehend – jede Größe nur als nachzuschlagend
   mit dem Zusatz "für [JAHR] verifizieren".
3. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV (Norm, Richtlinie oder
   BMF-Schreiben mit Datum) mit dem Zusatz "für [JAHR] verifizieren". Erfinde
   keine Paragrafen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
4. Rechne offen: keine Ergebniszahl ohne Rechenweg.
5. Berechne KEINE Fristen. Liste auf, WELCHE im Raum stehen, je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   Dauer, und ergänze: "Frist von einem Menschen zu berechnen und im
   Fristenprogramm zu erfassen."

AUSGABEFORMAT
1. Eindeutigkeit 2. Vergleichsrechnung 3. Stufenzuordnung und Folge
4. Prognosegliederung (nicht gerechnet) 5. Fremdvergleich 6. Fristarten
7. Mandantenschreiben 8. Prüfvermerk 9. Interne Notiz 10. Was ich nicht sicher
weiß
```

## Anwendung

1. Mietvertrag und Nebenkostenabrechnung vorher zusammentragen; ohne Abrechnung keine Warmmiete.
2. Marktmiete selbst belegen und in DATEV Meine Steuern ablegen; die KI darf keine nennen.
3. Vergleichsrechnung nachrechnen, Ergebnis in die Anlage V.
4. Prognose außerhalb des Prompts rechnen – er liefert die Struktur, nicht das Ergebnis.
5. Prüfvermerk zur Akte, Wiedervorlage setzen.

## Qualitätssicherung

- **Warmmiete auf beiden Seiten.** Häufigster Fehler ist der Vergleich von Kalt- und Warmmiete; haben die Spalten nicht denselben Umfang, ist die Antwort zu verwerfen.
- **Prozentgrenzen und Prognosezeitraum nie aus der KI-Antwort übernehmen** – sie sind gesetzlich bestimmt und haben sich geändert.
- **Die ortsübliche Miete ist eine Nachweisfrage.** Quelle mit Stand und Spanneneinordnung gehören zur Akte, sonst hält die Kürzung nicht.
- **Die Prognose rechnet ein Mensch.** Ein von der KI errechnetes Ergebnis wird nicht übernommen.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Vergleichsrechnung, Stufenzuordnung und Quellenbeleg nach; das Mandantenschreiben gibt ein Berufsträger frei (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 21 Abs. 2 und § 9 Abs. 1 EStG (gesetze-im-internet.de), R 21.3 EStR, dem BMF-Schreiben vom 08.10.2004 samt Nachfolgeschreiben, der BFH-Rechtsprechung zur ortsüblichen Marktmiete sowie DATEV LEXinform.

## Varianten

- **Vor Vertragsschluss:** „Beurteile nur die Schritte 1 bis 5 und benenne als Rechenweg, ab welcher Miete die günstigste Stufe greift."
- **Kein Mietspiegel:** „Vertiefe Schritt 3 und erstelle eine Anforderungsliste für Vergleichswohnungen."
- **Gewerbliche Vermietung:** „Prüfe die Anwendbarkeit der Stufenregelung und benenne den abweichenden Maßstab, mit Rechtsgrundlage."
- **Mehrjahresfall:** „Stelle je Zeitraum eine Tabellenzeile auf und benenne den Stufenwechsel."
