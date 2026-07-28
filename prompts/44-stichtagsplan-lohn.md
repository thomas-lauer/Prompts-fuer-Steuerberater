# 44 – Stichtagsplan und Erinnerungstexte für Lohnzulieferungen

**Problem:** Stundenzettel, Krankmeldungen sowie Ein- und Austritte kommen nach Abrechnungsschluss; die Abrechnung muss zurückgerechnet, die Meldung storniert und neu abgegeben werden – jeden Monat aufs Neue.
**Rolle:** Lohnsachbearbeitung, Teamleitung Lohn, Sekretariat
**DATEV-Bezug:** LODAS, Lohn und Gehalt (Abrechnungsschluss, Rückrechnung, SV-Meldungen), DATEV Unternehmen online / Arbeitnehmer online (Zulieferung), Eigenorganisation (Wiedervorlage)
**Was du bereitstellen musst:** Abrechnungstermin und Zahltag, interne Bearbeitungszeit der Kanzlei, Zulieferwege, wer beim Mandanten liefert, wiederkehrende Verspätungsursachen.
**Datensparsamkeit:** Mandantenname und Steuernummer erst beim Ausdruck einsetzen. Arbeitnehmer als `AN 1`, keine Personalnummern. Für den Plan genügen Mengengerüst und Rhythmus. Keine Gesundheitsdaten – Krankmeldungen erscheinen im Plan nur als Unterlagenart, nie mit Grund oder Diagnose. Keine Gläubigerdaten bei Pfändungen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Teamleitung Lohn in einer deutschen Steuerkanzlei und arbeitest mit
DATEV LODAS bzw. Lohn und Gehalt. Du planst rückwärts: vom Zahltag über den
Abrechnungsschluss zu den Lieferterminen des Mandanten.

AUFGABE
Erzeuge einen Stichtagsplan für den Personalverantwortlichen des Arbeitgebers
und die zugehörigen Erinnerungstexte.

RAHMEN
- Zahltag im Betrieb: [z. B. letzter Werktag / 15. des Folgemonats]
- Abrechnungsschluss in der Kanzlei: [DATUM ODER ARBEITSTAG IM MONAT]
- Interne Bearbeitungszeit der Kanzlei: [ANZAHL ARBEITSTAGE]
- Beitragsnachweis und Beitragsfälligkeit: [ANGABEN] – aus der Norm ermittelt
  und von einem Menschen geprüft (Fälligkeit § 23 Abs. 1 SGB IV,
  Beitragsnachweis § 28f Abs. 3 SGB IV, für [JAHR] verifizieren). Nicht
  schätzen, nicht frei vereinbaren.
- Zulieferweg: [DATEV Unternehmen online / Arbeitnehmer online /
  E-Mail / Portal / Papier]
- Wer liefert: [FUNKTION, z. B. Personalabteilung, Schichtleitung,
  Geschäftsführung]
- Mengengerüst: [ANZAHL ARBEITNEHMER, davon variable Bezüge: ANZAHL]
- Zu liefernde Unterlagen: [z. B. Stundenzettel, Zuschlagsnachweise,
  Krankmeldungen (nur Zeitraum), Urlaubsmeldungen, Ein- und Austritte
  mit Vertragsunterlagen, Änderungen der Stammdaten, Einmalzahlungen,
  Sachbezüge, Bescheinigungsanforderungen]
- Bekannte Verspätungsursachen: [ANGABEN]

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und liste fehlende
   Angaben auf. Rechne den Plan NICHT auf Basis geratener Termine.
2. Rechne rückwärts vom Abrechnungsschluss. Gib zu jedem Stichtag an:
   Unterlage – Liefertermin (als Arbeitstag oder Kalendertag) – Empfänger –
   Weg – warum dieser Vorlauf nötig ist. Rechne ausschließlich
   **kanzleiinterne** Termine rückwärts und kennzeichne jeden davon als
   Vorschlag, der gegen den Kanzleikalender zu prüfen ist. Gesetzliche Termine –
   Beitragsfälligkeit, Beitragsnachweis, An-, Ab- und Sofortmeldung,
   Jahresmeldung, digitaler Lohnnachweis – rechnest du NICHT und nennst du nicht
   mit Datum; du benennst nur die Unterlage, die Rechtsgrundlage und den Satz
   "Termin von einem Menschen zu bestimmen und einzutragen".
3. Unterscheide drei Stufen: (a) muss vor Abrechnungsschluss vorliegen,
   (b) kann bis zur Abrechnungsfreigabe nachgereicht werden,
   (c) wirkt erst im Folgemonat.
4. Beschreibe je Unterlagenart, was bei verspäteter Lieferung passiert:
   Korrekturabrechnung, Rückrechnung in DATEV, Auswirkung auf SV-Meldungen
   (Storno und Neumeldung), auf Beitragsnachweis und Beitragsfälligkeit,
   auf Bescheinigungen, auf das Nettoergebnis des Arbeitnehmers und auf den
   Aufwand. Formuliere sachlich, ohne Drohton, ohne Vorwurf.
5. Behandle Ein- und Austritte gesondert: Anmeldung und Abmeldung sind
   fristgebunden und hängen nicht am Abrechnungslauf.
5a. Behandle Einmalzahlungen im Zeitraum Januar bis März gesondert: weise darauf
    hin, dass die Zuordnung zum Vorjahr nach § 23a Abs. 4 SGB IV in Betracht
    kommt (Märzklausel – für [JAHR] verifizieren), dass die Prüfung vor der
    Abrechnung erfolgen muss und dass eine nachträgliche Zuordnung Rückrechnung
    sowie Storno und Neumeldung auslöst. Nenne keine Grenzwerte.
6. Erzeuge kurze Erinnerungstexte für den automatischen Versand:
   je Stichtag höchstens 40 Wörter, Sie-Form, mit Unterlage, Termin und
   Zulieferweg. Ohne personenbezogene Daten, ohne Krankheitsangaben.
7. Erzeuge einen Eskalationstext für den Fall, dass die Lieferung nach
   Abrechnungsschluss ausbleibt: höchstens 90 Wörter, sachlich, mit Folge
   (Abrechnung erfolgt auf Basis der vorliegenden Daten, Korrektur im
   Folgemonat) und mit Bitte um Bestätigung.
8. Nenne KEINE gesetzlichen Fristen, Fälligkeitstermine, Beitragsbemessungs-
   grenzen, Sachbezugswerte, Geringfügigkeitsgrenzen oder Pfändungsfreibeträge,
   ohne sie als "Wert – für [JAHR] verifizieren" bzw. "Frist – für [JAHR] verifizieren" zu markieren. Erfinde keine Fristen.
8a. Nenne zu jedem Prüfungsschritt die einschlägige Rechtsgrundlage, jeweils mit
    dem Zusatz "für [JAHR] verifizieren", und führe sie am Ende in einer Tabelle
    "Zu verifizierende Rechtsgrundlagen" mit Spalte "geprüft von (leer)".
    Mindestens zu nennen, soweit im Fall berührt: Meldeverfahren DEÜV,
    Fälligkeit § 23 SGB IV, Einmalzahlungen § 23a SGB IV, Meldepflichten
    § 28a SGB IV, Beitragsnachweis § 28f SGB IV, digitaler Lohnnachweis
    § 99 SGB IV, Gemeinsame Grundsätze § 103 SGB IV. Bist du dir einer
    Fundstelle nicht sicher, schreibe "Fundstelle offen – bitte recherchieren"
    statt einer Angabe.
9. Formuliere jede Aussage zu betrieblichen Abläufen, die nicht in den
   Angaben steht, ausdrücklich als Vermutung.

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit
2. Stichtagsplan: Stichtag | Unterlage | Stufe (a/b/c) | Liefert | Weg |
   Folge bei Verspätung
3. Was-wird-benötigt-Liste, abhakbar mit ☐, nach Unterlagenart
4. Erinnerungstexte, je Stichtag einer, höchstens 40 Wörter
5. Eskalationstext
6. Interne Version: Wiedervorlagen der Kanzlei, Puffer, Zuständigkeiten,
   was bei Nichtlieferung intern zu veranlassen ist
7. Zu verifizierende Rechtsgrundlagen: Nr. | Fundstelle | wofür sie steht |
   geprüft von (leer)
8. Was ich nicht sicher weiß
```

## Anwendung

1. Abrechnungsschluss und Zahltag vorher verbindlich mit dem Mandanten abstimmen. Der Plan ist nur so belastbar wie dieser eine Termin.
2. Entwurf mit dem Personalverantwortlichen durchsprechen und die Stufen (a), (b), (c) gemeinsam festlegen – dort entsteht die Verbindlichkeit, nicht im Text.
3. Erinnerungstexte in den Serienversand oder das Kanzleiportal übernehmen und mit den Stichtagen verknüpfen.
4. Interne Version in die Wiedervorlage einstellen; Puffer für Feiertage, Jahreswechsel und Urlaubszeit gesondert setzen.
5. Ergänzt Prompt 17 (Jahres-Terminplan) und Prompt 01 (Eskalation bei ausbleibender Zulieferung) als monatliche Feinplanung.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Ausgangsdokuments nachgeprüft und abgezeichnet** – bei Melde- und Rechtsbehelfsfristen ausnahmslos, unabhängig davon, ob ein Rechtsbehelf geplant ist. Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Alle Termine gegen den Kanzleikalender rechnen.** Arbeitstage, Feiertage in den betroffenen Bundesländern und Brückentage prüfen; das Modell kennt den Kalender des Mandanten nicht.
- Gesetzliche Fristen – Beitragsnachweis, Beitragsfälligkeit, An- und Abmeldung, Sofortmeldung in den betroffenen Branchen – selbst nachschlagen – Fälligkeit § 23 Abs. 1 SGB IV, Beitragsnachweis § 28f Abs. 3 SGB IV, An-/Abmeldung §§ 6, 8 DEÜV, Jahresmeldung § 10 DEÜV, Sofortmeldung § 28a Abs. 4 SGB IV, digitaler Lohnnachweis § 99 SGB IV (jeweils für [JAHR] verifizieren) – und nie aus der KI-Antwort übernehmen.
- Prüfen, ob die beschriebenen Folgen einer Verspätung zur tatsächlichen Kanzleipraxis passen (wird zurückgerechnet oder im Folgemonat korrigiert?). Falsche Ankündigungen erzeugen Streit über Mehraufwand.
- Vereinbarungen zu Mehraufwand nur aufnehmen, wenn sie vertraglich gedeckt sind; Freigabe durch den Berufsträger.
- Erinnerungs- und Eskalationstexte auf Ton prüfen und sicherstellen, dass keine Krankmeldungsgründe, Namen oder Personalnummern darin stehen.

## Varianten

- **Jahresübersicht:** "Erzeuge aus dem Monatsplan eine Jahresübersicht mit allen zwölf Abrechnungsschlüssen und den Sonderterminen zum Jahreswechsel."
- **Ein-Seiten-Aushang:** "Verdichte den Stichtagsplan auf eine Seite für den Aushang in der Personalabteilung."
- **Mehrere Betriebsstätten:** "Erzeuge je Betriebsstätte mit eigener Schichtleitung eine eigene Zuliefererliste."
- **Nach der Panne:** "Leite aus dem letzten Verspätungsfall eine Arbeitsanweisung ab."
