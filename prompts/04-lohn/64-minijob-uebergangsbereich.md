# 64 – Minijob und Übergangsbereich: Grenzen überwachen und Überschreitungen beurteilen

**Problem:** Die Geringfügigkeitsgrenze ist dynamisch an den Mindestlohn gekoppelt; Mandanten rechnen mit alten Zahlen weiter, und beim gelegentlichen Überschreiten weiß niemand, wie oft und wie hoch es zulässig ist.
**Rolle:** Lohnsachbearbeitung
**DATEV-Bezug:** DATEV Lohn und Gehalt, DATEV LODAS, DATEV Arbeitnehmer online
**Was du bereitstellen musst:** Arbeitsvertrag mit Arbeitszeit und Stundenlohn, Entgeltnachweise der letzten zwölf Monate, Angaben zu Einmalzahlungen, Sachbezügen, weiteren Beschäftigungen und Rentenbezug.
**Datensparsamkeit:** Vor dem Einfügen Name, Personalnummer, Geburtsdatum und Anschrift ersetzen (`AN 1`, `Mandant A`); die Sozialversicherungsnummer bleibt draußen. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Angaben zu Krankheit nur, soweit zwingend. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachkraft für Entgeltabrechnung in einer deutschen Steuerkanzlei. Du
behandelst alle Grenzwerte als jährlich veränderliche, nachzuschlagende Größen
und prüfst Sozialversicherung und Lohnsteuer getrennt.

AUFGABE
Beurteile die Beschäftigung, überwache die Grenzen und leite die Folgen einer
Überschreitung ab.

KONTEXT
- Arbeitnehmer: [AN 1], beschäftigt seit: [ZEITPUNKT]
- Regelmäßige Arbeitszeit: [STUNDEN JE WOCHE], Stundenlohn: [BETRAG]
- Monatsentgelt regelmäßig: [BETRAG]
- Weitere Entgeltbestandteile: [Urlaubsgeld / Weihnachtsgeld / Prämie /
  Sachbezug / keine], Vereinbarung: [zugesagt / freiwillig / betriebliche Übung]
- Entgelte der letzten zwölf Monate: [AUFSTELLUNG JE MONAT]
- Überschreitungen bisher: [nein / ja, Monate]
- Grund: [Vertretung / Auftragsspitze / Mehrarbeit / Entgelterhöhung]
- Weitere Beschäftigungen: [keine / Minijob / Hauptjob / Selbständigkeit]
- Geplante Art: [geringfügig entlohnt / kurzfristig / Übergangsbereich /
  versicherungspflichtig]
- Befreiungsantrag: [liegt vor / liegt nicht vor], Rentenbezug: [nein / ja]
- Bisherige Beurteilung: [ANGABEN]

PRÜFSCHEMA – REIHENFOLGE EINHALTEN, JEDEN SCHRITT FESTHALTEN
1. Jahresbetrachtung: Bestimme die Bezugsgröße der Geringfügigkeitsgrenze und
   erläutere ihre Kopplung an den Mindestlohn. Rechne vorausschauend mit dem
   regelmäßigen Jahresentgelt, nicht mit einem Monat. Halte fest, WELCHE
   Entgeltbestandteile mitzählen: laufendes Entgelt, Einmalzahlungen, Urlaubs- und
   Weihnachtsgeld, Sachbezüge, Zuschläge; unterscheide zugesagte von freiwilligen
   Leistungen. Grenzbetrag, Mindestlohn und Stundenzahl nur nachzuschlagend
   (Grenzwerte – für [JAHR] verifizieren).
2. Unvorhersehbares Überschreiten: Voraussetzungen einzeln nennen und prüfen
   (Unvorhersehbarkeit zum Prognosezeitpunkt, Anlass, Dokumentation). Häufigkeit
   und Höchstgrenze nur nachzuschlagend
   (Häufigkeit und Höchstgrenze – für [JAHR] verifizieren). Eine Entgelterhöhung
   ist nicht unvorhersehbar.
3. Vorhersehbares Überschreiten: Übergang in Übergangsbereich und
   Versicherungspflicht, Zeitpunkt des Statuswechsels, Beitragsberechnung als
   Rechenweg ohne Zahlen, Lastenverteilung und Meldungen
   (Unter- und Obergrenze – für [JAHR] verifizieren).
4. Mehrere Beschäftigungen: Was ist zusammenzurechnen, wie wirkt eine
   Hauptbeschäftigung, was gilt bei zwei Minijobs, ab wann entsteht
   Versicherungspflicht? Benenne Auskunfts- und Nachweispflicht.
5. Kurzfristige Beschäftigung: Voraussetzungen, eigene Zeitgrenzen,
   Berufsmäßigkeit und Folge ihres Verfehlens
   (Zeitgrenzen – für [JAHR] verifizieren). Geringfügigkeit und Kurzfristigkeit
   schließen einander aus.
6. Rentenversicherung: Beitragspflicht, Aufstockung, Voraussetzungen und Wirkung
   des Befreiungsantrags, Form und Verbleib, Bindung an weitere Minijobs.
6a. Lohnsteuer getrennt von der Sozialversicherung: Pauschalierung bei
    geringfügiger und bei kurzfristiger Beschäftigung mit den je eigenen
    Voraussetzungen, Alternative der Besteuerung nach den Merkmalen des
    Arbeitnehmers, Wahlrecht und wer die Pauschsteuer trägt, Verhältnis zur
    sozialversicherungsrechtlichen Einordnung (Pauschalierungssätze und
    Voraussetzungen – für [JAHR] verifizieren). Sage ausdrücklich, wenn die
    lohnsteuerliche und die sozialversicherungsrechtliche Einordnung
    auseinanderfallen.
7. Folgen einer Fehlbeurteilung: Nachverbeitragung, wer den
   Gesamtsozialversicherungsbeitrag trägt, Grenzen des Rückgriffs, Verjährung
   samt Verlängerung bei Vorsatz, Säumniszuschläge dem Grunde nach,
   Meldekorrekturen. Nenne keinen Zins- und Zuschlagssatz.

WEITERE ERGEBNISSE
8. Mandanten-Merkblatt, höchstens 300 Wörter, Sie-Form, Fachbegriffe in einem
   Halbsatz erklärt, ohne Betrag, mit Hinweis auf die jährliche Änderung der
   Grenzwerte.
9. Anschreiben zur Vertragsanpassung bei Mindestlohnerhöhung: warum die
   Stundenzahl zu prüfen ist, welche Angaben die Kanzlei braucht, welcher Schritt
   folgt.
10. Interne Überwachungsliste als Tabelle: AN | Stunden | Stundenlohn |
    Monatsentgelt | Prognose Jahr | Überschreitungen | Prüfung | Erledigt (leer)

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Fehlen die Entgelte der Vormonate, beurteile Schritt 2 nicht.
2. Nenne KEINEN Grenzbetrag, keine Mindestlohnhöhe, Stundenzahl,
   Häufigkeitsgrenze und Zeitgrenze als feststehend – nur als nachzuschlagend mit
   dem Zusatz "für [JAHR] verifizieren". Betone, dass diese Werte sich jährlich
   ändern und dass eine Fehlbeurteilung rückwirkend zur Nachverbeitragung
   führt.
3. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV (Norm mit Absatz und Satz,
   Geringfügigkeits-Richtlinien mit Fassungsdatum) mit dem Zusatz
   "für [JAHR] verifizieren"; bist du unsicher:
   "Fundstelle offen – bitte recherchieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE im Raum stehen (Meldungen,
   Befreiungsantrag, Verjährung), je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", und ergänze: "Frist von einem Menschen zu berechnen
   und im Fristenprogramm zu erfassen."
5. Gib ein klares Ergebnis: [geringfügig entlohnt / kurzfristig /
   Übergangsbereich / versicherungspflichtig / nicht entscheidbar]; bei der
   letzten Variante die entscheidende Angabe.

AUSGABEFORMAT
1. Eindeutigkeit 2. Prüfprotokoll 1 bis 7 einschließlich 6a mit
Rechtsgrundlagen 3. Status
4. Fristarten 5. Handlungsanweisung 6. Merkblatt 7. Anschreiben
8. Überwachungsliste 9. Interne Notiz 10. Was ich nicht sicher weiß
```

## Anwendung

1. Arbeitsvertrag und Entgelte der letzten zwölf Monate zusammenstellen; ohne Vormonate ist die Prognose nicht belegbar.
2. Bei jeder Neueinstellung, Entgeltänderung und Mindestlohnerhöhung ausführen.
3. Ergebnis über SV-Schlüssel und Übergangsbereichskennzeichnung umsetzen, Statuswechsel richtig melden.
4. Überwachungsliste als Kanzleivorlage führen, mit Wiedervorlage verbinden;
   Befreiungsantrag zum Lohnkonto nehmen und den Eingang datieren.

## Qualitätssicherung

- **Grenzbetrag, Mindestlohn und Stundenzahl nie aus der KI-Antwort übernehmen** – jede Vorlage mit festen Zahlen veraltet binnen eines Jahres.
- **Eine Fehlbeurteilung wirkt rückwirkend.** Die Betriebsprüfung verbeitragt nach; den Gesamtbeitrag trägt der Arbeitgeber, der Rückgriff ist begrenzt.
- **Prognose dokumentieren** – ohne Vermerk ist Unvorhersehbarkeit später nicht belegbar.
- **Bei Zweifeln:** Anfrage bei der Minijob-Zentrale; die KI-Antwort ersetzt keine verbindliche Auskunft.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite Person nimmt Prognose, Zusammenrechnung, Status und Jahreswerte nach; Merkblatt und Anschreiben gibt ein Berufsträger frei (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 8 Abs. 1 Nr. 1 und Nr. 2, Abs. 1a, Abs. 1b und Abs. 2 SGB IV, § 20 Abs. 2, §§ 25, 28e, 28g SGB IV, § 6 Abs. 1b SGB VI, § 40a EStG und § 1 Abs. 2 MiLoG (gesetze-im-internet.de), den geltenden Geringfügigkeits-Richtlinien, der Minijob-Zentrale, der Deutschen Rentenversicherung und DATEV LEXinform.

## Varianten

- **Nur Überschreitung:** „Beurteile nur die Schritte 2 und 3 und stelle beide Varianten nebeneinander."
- **Saisonkräfte:** „Vertiefe Schritt 5 mit einer Prüfliste zur Berufsmäßigkeit."
- **Rentner:** „Prüfe die Auswirkung auf Rentenbezug und Beitragspflicht, mit Rechtsgrundlage."
- **Selbstauskunft:** „Erzeuge einen Fragebogen zu Nebenbeschäftigungen."
