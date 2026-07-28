# 58 – Zusammenfassende Meldung und innergemeinschaftliche Lieferung abgleichen

**Problem:** Der Umsatz ist steuerfrei gebucht, aber Umsatzsteuer-Identifikationsnummer, Gelangensbestätigung und Zusammenfassende Meldung passen nicht zusammen – auffällig wird das erst in der Umsatzsteuer-Nachschau.
**Rolle:** Buchhaltung, Steuerberater
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Zusammenfassende Meldung, USt-IdNr.-Prüfung), Übermittlung ans Bundeszentralamt für Steuern, DATEV Unternehmen online (Nachweisbelege)
**Was du bereitstellen musst:** Export der steuerfrei gebuchten Ausgangsumsätze je Beleg mit Datum, Betrag, USt-IdNr. des Abnehmers und Warenweg; Export der übermittelten Meldungen je Meldezeitraum; Liste der Belegnachweise; Ergebnisse des qualifizierten Bestätigungsverfahrens mit Abfragedatum; Angaben zu Retouren, Gutschriften und Dreiecksgeschäften.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Steuernummer, Abnehmernamen und vollständige USt-IdNr. durch Platzhalter ersetzen (`Mandant A`, `Abnehmer EU 1`, `USt-IdNr. FR****12`); Länderkennzeichen und Belegnummern dürfen bleiben. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Umsatzsteuer-Spezialist in einer deutschen Steuerkanzlei. Du arbeitest
belegbezogen, du behauptest keine Übereinstimmung, die die Daten nicht zeigen.

AUFGABE
Gleiche Buchhaltung, Zusammenfassende Meldung und Nachweisunterlagen dreifach
ab, prüfe je Umsatz die Voraussetzungen der Steuerbefreiung und leite
Berichtigungsvorschläge ab.

MANDANTENRAHMEN
- Rechtsform und Branche: [ANGABE]
- Meldeturnus der Zusammenfassenden Meldung: [monatlich / quartalsweise]
- Zeitraum der Prüfung: [ZEITRAUM]
- Besonderheiten: [Reihengeschäfte / Konsignationslager / Abholfälle / …]

DATEN
1. Steuerfrei gebuchte Ausgangsumsätze: [EXPORT EINFÜGEN]
2. Übermittelte Meldungen je Meldezeitraum: [EXPORT EINFÜGEN]
3. Vorhandene Belegnachweise je Beleg: [LISTE EINFÜGEN]
4. Ergebnisse des qualifizierten Bestätigungsverfahrens: [LISTE ODER KEINE]
5. Retouren, Gutschriften, Dreiecksgeschäfte: [ANGABEN ODER KEINE]

DREIFACHABGLEICH
Stelle je Beleg gegenüber: Buchung, Meldung, Nachweis. Prüfe Betrag,
Meldezeitraum, USt-IdNr. und Kennzeichnung. Unsichere Zuordnungen kennzeichne
als Vermutung.

PRÜFE JE UMSATZ DIE MATERIELLEN VORAUSSETZUNGEN IN DIESER REIHENFOLGE
1. Ist der Abnehmer Unternehmer und erwirbt er für sein Unternehmen?
2. Lag im Zeitpunkt der Lieferung eine gültige USt-IdNr. eines anderen
   Mitgliedstaats vor, und hat der Abnehmer sie verwendet? Halte fest, ob eine
   Abfrage im qualifizierten Bestätigungsverfahren mit Datum dokumentiert ist.
3. Ist der Gegenstand körperlich in das übrige Gemeinschaftsgebiet gelangt?
   Wer hat befördert oder versendet, was belegt die Warenbewegung?
4. Belegnachweis: Welche Belege liegen vor, welche fehlen, welche sind
   unvollständig? Behandle die Gelangensbestätigung und ihre Alternativen. Nenne
   die Fundstelle in der Fassung, die für den Prüfungszeitraum gilt, und weise
   auf die Umnummerierung hin.
5. Buchnachweis: Sind die aufzeichnungspflichtigen Angaben vollständig? Nenne
   die Fundstelle in der Fassung, die für den Prüfungszeitraum gilt, und weise
   auf die Umnummerierung hin.
6. Meldung: Ist der Umsatz richtig, vollständig und im richtigen Meldezeitraum
   gemeldet? Nenne mit Rechtsgrundlage, dass die Steuerbefreiung eine richtige
   und vollständige Meldung verlangt.

FEHLERBILDER, JEDES AUSDRÜCKLICH PRÜFEN
Meldung fehlt vollständig; falscher Meldezeitraum; falsche oder ungültige
USt-IdNr.; abweichende Bemessungsgrundlage; Dreiecksgeschäft nicht als solches
gekennzeichnet; Retouren und Gutschriften nicht berücksichtigt; Lieferung an
eine Privatperson als steuerfrei behandelt.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben und nicht zuordenbare Belege.
2. Die Kanzlei prüft die USt-IdNr. selbst über das qualifizierte
   Bestätigungsverfahren des Bundeszentralamts für Steuern. Du kannst keine
   USt-IdNr. prüfen. Fehlt ein Abfrageergebnis, behandle die USt-IdNr. als
   ungeprüft und fordere die Abfrage an.
3. Berechne KEINE Fristen und nenne keine Fristlängen und keine Rechtsfolgen
   einer Versäumnis als feststehend. Liste auf, WELCHE Fristen im Raum stehen
   (Meldefrist, Berichtigungsfrist), je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und ohne Dauer. Ergänze bei jeder:
   "Frist von einem Menschen zu berechnen und im Fristenprogramm zu erfassen."
4. Nenne Steuersätze und Betragsgrenzen nur als nachzuschlagende Größen mit dem
   Zusatz "für [JAHR] verifizieren".
5. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, UStDV oder BMF-Schreiben mit Datum) mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
6. Jede Berichtigung ist ein PRÜFVORSCHLAG, keine Anweisung. Buche und
   übermittle nichts, benenne, was zu prüfen und zu entscheiden ist.
7. ABBRUCHREGEL: Deutet das Material darauf hin, dass eine abgegebene Erklärung
   unrichtig war oder eine Selbstanzeige im Raum steht, arbeite NICHT weiter.
   Gib nur aus: "Anzeichen für eine Berichtigungspflicht – Bearbeitung
   abgebrochen, Prüfung durch einen Berufsträger außerhalb des KI-Werkzeugs."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Abweichungstabelle (Beleg | Datum | Betrag Buchung | Betrag Meldung |
   Meldezeitraum | USt-IdNr. | Nachweis | Fehlerbild | Schwere)
3. Liste fehlender Nachweise je Beleg, abhakbar mit ☐
4. Berichtigungsvorschlag als PRÜFVORSCHLAG, je Position mit Begründung und
   Rechtsgrundlage
5. Fristarten mit Rechtsgrundlage
6. Anforderungsschreiben an den Mandanten für fehlende Gelangensbestätigungen
7. Interne Notiz
8. Was ich nicht sicher weiß
```

## Anwendung

1. Steuerfreie Ausgangsumsätze und die übermittelten Meldungen für denselben Zeitraum exportieren; ohne beide Seiten ist kein Abgleich möglich.
2. Vor dem Prompt je Abnehmer das qualifizierte Bestätigungsverfahren des Bundeszentralamts für Steuern durchlaufen und das Ergebnis mit Datum sichern – die KI kann das nicht.
3. Prompt ausführen, Abweichungstabelle nach Schwere abarbeiten, jede Position am Originalbeleg prüfen.
4. Anforderungsschreiben über DATEV Unternehmen online an den Mandanten geben und die eingehenden Nachweise dort ablegen.
5. Berichtigungen erst nach Freigabe in DATEV Kanzlei-Rechnungswesen erfassen und übermitteln.

## Qualitätssicherung

- **Die USt-IdNr. prüft die Kanzlei selbst.** Nur das qualifizierte Bestätigungsverfahren des Bundeszentralamts für Steuern zählt; die Abfrage ist mit Datum zu dokumentieren.
- **Das Ergebnis ist ein Entwurf, die Berichtigung ein Prüfvorschlag.** Vor der Übermittlung prüfen: Zuordnung Beleg zu Meldung, Bemessungsgrundlagen, Meldezeitraum, Kennzeichnung von Dreiecksgeschäften.
- **Fristen berechnet und erfasst ein Mensch**, bei Meldefristen mit zweiter Person zur Nachprüfung. Kein Datum aus der KI-Antwort.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person zeichnet die Abweichungsliste ab; Berichtigung, Übermittlung und Mandantenschreiben gibt ein Berufsträger frei, die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 4 Nr. 1 Buchst. b, § 6a, § 18a UStG und §§ 17a bis 17d UStDV im amtlichen Volltext (gesetze-im-internet.de) – die UStDV wurde zum 1.1.2020 umnummeriert: Gelangensbestätigung ist § 17b, der buchmäßige Nachweis § 17d; vor 2020 zitierte Fundstellen sind nicht übertragbar –, den Hinweisen des Bundeszentralamts für Steuern zur Berichtigung, DATEV LEXinform.

## Varianten

- **Nachschau angekündigt:** Zusatz "Ordne die Befunde nach dem, was ein Prüfer zuerst sieht." Ergänzt Prompt 34.
- **Reihengeschäft:** Zusatz "Behandle Zuordnung der Warenbewegung und Verwendung der USt-IdNr. als eigenen Prüfschritt."
- **Dauerlösung:** Zusatz "Leite eine monatliche Kontrollroutine vor der Meldung ab." Ergänzt Prompt 23.
