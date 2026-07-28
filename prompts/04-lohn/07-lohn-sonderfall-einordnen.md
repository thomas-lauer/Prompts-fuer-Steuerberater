# 07 – Lohn-Sonderfall einordnen: Steuer- und SV-Pflicht prüfen

**Problem:** Firmenwagen in der Elternzeit, Sachbezug beim Minijob, Einmalzahlung im Austrittsmonat – Sonderfälle kosten jedes Mal Recherche, und ein Fehler wirkt rückwirkend über Monate. Für Lohnpfändungen ist Prompt 101 vorrangig; er behandelt Zuordnung der Bezüge, Rangfolge und Drittschuldnerpflichten.
**Rolle:** Lohnsachbearbeitung
**DATEV-Bezug:** LODAS, Lohn und Gehalt (jeweils inkl. SV-Meldungen und Bescheinigungswesen)
**Was du bereitstellen musst:** Sachverhalt, Vertragsdaten, Abrechnungszeitraum, bisherige Behandlung.
**Datensparsamkeit:** Name, Personalnummer, Geburtsdatum und Anschrift des Arbeitnehmers durch Platzhalter ersetzen (`AN 1`), ebenso den Mandantennamen (`Mandant A`). Für die Einordnung genügen Beschäftigungsart, Status, Beträge und Zeitraum. Angaben zu Gesundheit, Gläubigern oder familiären Umständen nur so weit einfügen, wie sie für die Prüfung zwingend sind. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachkraft für Entgeltabrechnung in einer deutschen Steuerkanzlei und
arbeitest mit DATEV LODAS bzw. Lohn und Gehalt. Du prüfst Lohnsteuer und
Sozialversicherung getrennt, weil sie unterschiedlichen Regeln folgen.

AUFGABE
Ordne den folgenden Sachverhalt lohnsteuerlich und sozialversicherungsrechtlich
ein und leite die Behandlung in der Abrechnung ab.

SACHVERHALT
[SACHVERHALT AUSFÜHRLICH BESCHREIBEN]

ANGABEN ZUM ARBEITNEHMER (anonymisiert, z. B. "AN 1")
- Beschäftigungsart: [Vollzeit / Teilzeit / Minijob / kurzfristig / Werkstudent /
  Aushilfe / Gesellschafter-Geschäftsführer]
- Steuerklasse / Faktor / Kinderfreibeträge: [ANGABEN]
- Krankenkasse / Status: [gesetzlich / privat / freiwillig]
- Besonderer Status im Zeitraum: [z. B. Elternzeit, Mutterschutz, Krankengeld,
  Kurzarbeit, unbezahlter Urlaub, Austritt zum …]
- Weitere Beschäftigungen: [ja/nein]

ANGABEN ZUM VORGANG
- Art der Leistung / des Bezugs: [z. B. Firmenwagen 1 %-Regelung,
  Sachbezug, Gutschein, Zuschuss, Abfindung, Prämie, Pfändung]
- Höhe / Bewertung: [BETRÄGE]
- Zeitraum / Stichtag: [ANGABEN]
- Arbeitsvertragliche Grundlage: [z. B. Zusatzvereinbarung, Betriebsvereinbarung]
- Bisherige Behandlung: [wie wurde bisher abgerechnet]

PRÜFE UND HALTE GETRENNT FEST
A. LOHNSTEUER
   1. Liegt Arbeitslohn vor? Rechtsgrundlage.
   2. Steuerfrei, pauschalierbar oder individuell zu versteuern?
      Nenne Voraussetzungen einzeln und prüfe sie am Sachverhalt.
   3. Bewertungsmaßstab und Zuflusszeitpunkt.
B. SOZIALVERSICHERUNG
   4. Beitragspflichtiges Arbeitsentgelt? Rechtsgrundlage.
   5. Welche Zweige, welche Besonderheit (z. B. Beitragsfreiheit,
      Übergangsbereich, beitragsfreie Zeiten)?
   6. Zuordnung zum richtigen Abrechnungsmonat. Bei einmalig gezahltem
      Arbeitsentgelt zusätzlich: § 23a SGB IV, Märzklausel, anteilige
      Jahres-Beitragsbemessungsgrenze, Besonderheiten im Austrittsmonat.
B2. NETTOEBENE (nur bei Pfändung, Abtretung, Arbeitgeberdarlehen)
   6a. Pfändbares Einkommen: was ist unpfändbar, was bleibt außer Betracht
       (§§ 850 ff. ZPO), welche Rangfolge gilt bei mehreren Titeln?
       Bearbeite diesen Punkt nur überblicksartig; Zuordnung der Bezugsarten,
       Rangfolge, Abtretung und Drittschuldnererklärung sind Gegenstand von
       Prompt 101 und dort vorrangig zu bearbeiten.
   6b. Nenne KEINE konkreten Pfändungsfreibeträge, ohne sie als
       "Tabellenwert – für [JAHR] verifizieren" zu markieren.
C. FOLGEN
   7. Auswirkung auf Meldungen und Bescheinigungen.
   8. Was ist bei rückwirkender Korrektur zu beachten (Verjährung,
      Rückrechnung, Meldekorrektur)?

ANFORDERUNGEN
- Gib zuerst eine Einschätzung: eindeutig / vertretbare Varianten /
  nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben auf.
- Nenne zu jedem Prüfschritt und zu jeder rechtlichen Aussage die
  Rechtsgrundlage (EStG, LStR/LStH, § 14 SGB IV, § 23a SGB IV, SvEV,
  Beitragsverfahrensverordnung, Geringfügigkeits-Richtlinien, bei
  Nettoabzügen §§ 850 ff. ZPO), jeweils mit dem Zusatz
  "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du unsicher,
  schreibe "Fundstelle offen – bitte recherchieren".
- Nenne die typischen Fehlerquellen genau dieses Falls.
- Schließe mit einer Handlungsanweisung in Stichpunkten für die Abrechnung.
- Kennzeichne gesondert alles, was du nicht sicher weißt oder wo sich
  Werte jährlich ändern (Beitragsbemessungsgrenzen, Sachbezugswerte,
  Freigrenzen). Nenne KEINE konkreten Jahreswerte, ohne sie ausdrücklich
  als "für [JAHR] verifizieren" zu markieren.

AUSGABEFORMAT
Einschätzung – A Lohnsteuer – B Sozialversicherung – B2 Nettoebene
(falls einschlägig) – C Folgen – Handlungsanweisung –
"Rechtsstand – für [JAHR] verifizieren".
```

## Anwendung

1. Sachverhalt anonymisiert eingeben (Personalnummer und Name durch "AN 1" ersetzen).
2. Ergebnis gegen die DATEV-Hilfe und die einschlägigen Rundschreiben der Spitzenverbände prüfen.
3. Geprüfte Fälle in eine kanzleiinterne Fallsammlung aufnehmen – die meisten Sonderfälle wiederholen sich.

## Qualitätssicherung

- **Jahreswerte niemals aus der KI-Antwort übernehmen.** Beitragsbemessungsgrenzen, Sachbezugswerte, Geringfügigkeitsgrenze und Freibeträge ändern sich jährlich; hier ist das Modell strukturell unzuverlässig.
- Bei SV-rechtlichen Zweifelsfällen: Statusfeststellung oder Anfrage bei der Einzugsstelle. Die KI-Antwort ersetzt keine verbindliche Auskunft.
- Rückwirkende Korrekturen immer vom Berufsträger freigeben lassen – sie berühren Meldungen und ggf. Haftung.
- Prüfschema nutzen, Ergebnis verifizieren: Die Stärke der Antwort liegt in der Vollständigkeit der Prüfpunkte, nicht in den Zahlen.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Vor der Abrechnung muss eine zweite fachkundige Person die getrennte lohnsteuerliche und sozialversicherungsrechtliche Einordnung sowie alle Jahreswerte nachvollziehen. Die Freigabe erteilt ein Berufsträger, bevor der Fall abgerechnet, gemeldet oder dem Mandanten mitgeteilt wird; die Freigabe ist zu dokumentieren.

## Varianten

- **Anfrage an die Krankenkasse:** Zusatz "Formuliere zusätzlich eine sachliche Anfrage an die Einzugsstelle mit allen für die Beurteilung nötigen Angaben."
- **Mandanteninfo:** "Erkläre das Ergebnis in fünf Sätzen für den Arbeitgeber, ohne Paragrafen."
- **Arbeitnehmerinfo:** siehe Prompt 08.
- **Checkliste:** "Leite aus dem Fall eine wiederverwendbare Prüfcheckliste für diesen Sachverhaltstyp ab."
