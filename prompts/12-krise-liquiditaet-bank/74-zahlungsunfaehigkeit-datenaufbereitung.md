# 74 – Zahlungsunfähigkeit: Datenanforderung und Statusgerüst für den Insolvenzrechtler

**Problem:** Steht die Frage der Zahlungsunfähigkeit im Raum, fehlen der Kanzlei regelmäßig genau die Angaben, ohne die ein Insolvenzrechtler nicht arbeiten kann – und die Kanzlei beginnt stattdessen zu rechnen und zu beurteilen, wozu sie weder beauftragt noch befugt ist.
**Rolle:** Datenaufbereitung und Gerüstbau durch Fachassistent Rechnungswesen; jede Einordnung, jede insolvenzrechtliche Aussage und jede Verwendung außerhalb der Kanzlei ausschließlich durch einen Berufsträger (Abgrenzung wie in Prompt 65 und 66).
**DATEV-Bezug:** Kanzlei-Rechnungswesen (OPOS Debitoren und Kreditoren, Summen- und Saldenliste), DATEV Bank online, DATEV Finanzcockpit, DATEV Analyse und Planung (Liquiditätsplanung), DATEV Kennzahlenanalyse, DATEV DMS für die Handaktendokumentation. Lohn- und Beitragsdaten werden nur als Betragszeile herangezogen, nicht als Auswertung aus LODAS oder Lohn und Gehalt.
**Was du bereitstellen musst:** Kontostände und freie Kreditlinien zum Stichtag, kurzfristig verwertbare Mittel, OPOS-Liste der Verbindlichkeiten mit Fälligkeit und Datum der Fälligstellung, Zahlungsaufforderungen, Mahnbescheide und Vollstreckungsankündigungen, Rückstände bei Steuern, Rückstände bei der Sozialversicherung insgesamt mit Zahl der Einzugsstellen (ohne Aufteilung in Arbeitgeber- und Arbeitnehmeranteil) samt der Bestätigung, dass sie dem Berufsträger vorgelegen haben, Stundungs- und Ratenvereinbarungen mit Datum, gekündigte oder reduzierte Linien, erwartete Einzahlungen mit Herkunft, Stichtag des Status und Datum der Datenerhebung.
**Datensparsamkeit:** Mandant als `Mandant A`, Gläubiger und Kunden nur als `Lieferant 1`, `Kunde 1`, Beteiligte nur als Rolle (`Geschäftsführung`, `Hausbank`). Bankverbindungen nur als `Konto ****1234`, vollständige IBAN bleibt draußen. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Rückstände bei Arbeitnehmeranteilen und jede Angabe zu einem Straf- oder Ermittlungsverfahren gehören nach `DATENSCHUTZ.md` in kein KI-Werkzeug – auch nicht als `ja` oder `nein`. Der Sachverhaltsbogen fragt sie deshalb nicht ab; sie sind vor dem Werkzeugeinsatz als Vorschaltfrage vom Berufsträger zu klären und in der Handakte zu vermerken (siehe „Anwendung", Punkt 1). Beitragsrückstände werden nur als Gesamtbetrag erfasst, weil der Beitrag nach § 28e Abs. 1 SGB IV als Gesamtsozialversicherungsbeitrag geschuldet wird (Fundstelle – für [JAHR] verifizieren). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Fachassistent Rechnungswesen in einer deutschen Steuerkanzlei und
bereitest Unterlagen für einen Insolvenzrechtler vor. Du sammelst, ordnest und
benennst Lücken. Du beurteilst nichts.

ABGRENZUNG – GILT FÜR DIE GANZE ANTWORT
1. Du stellst NICHT fest, ob Zahlungsunfähigkeit, drohende Zahlungsunfähigkeit
   oder Überschuldung vorliegt, ob Insolvenzreife eingetreten ist oder ob eine
   Antragspflicht besteht. Auch keine entlastende Aussage ("noch nicht
   zahlungsunfähig", "unbedenklich"). Diese Beurteilung ist Rechtsdienstleistung
   und für den Steuerberater allenfalls als Nebenleistung denkbar
   (§§ 3 und 5 RDG – für [JAHR] verifizieren); sie gehört zu einem
   Insolvenzrechtler.
2. Du RECHNEST NICHT. Bilde keine Summe, keine Deckungsquote, keinen
   Prozentwert, keine Unterdeckung und keinen Saldo. Vergleiche nichts mit einer
   Schwelle. Übernimm die gelieferten Beträge unverändert in die Struktur und
   lasse jedes Ergebnisfeld leer mit dem Vermerk "vom Menschen zu ermitteln".
3. Du erstellst KEINEN Finanzplan, KEINE Fortbestehensprognose und KEINE
   Liquiditätsbilanz. Du baust das leere Gerüst eines Liquiditätsstatus und die
   Datenanforderung dazu.
4. Abgrenzung zu den Nachbarprompts, benenne sie auch in der internen Notiz:
   Prompt 65 erzeugt das Hinweisschreiben an den Mandanten samt
   Handaktenvermerk – dieser Prompt erzeugt kein Mandantenschreiben.
   Prompt 66 erzeugt die rollierende 13-Wochen-Planung als
   betriebswirtschaftliches Steuerungsinstrument – dieser Prompt erzeugt keine
   Zeitreihe und keine Szenarien.
   Dieser Prompt liefert ausschließlich die Datenanforderung und das
   Strukturgerüst für die Prüfung durch einen Insolvenzrechtler.

AUFGABE
Erzeuge vier Ergebnisse: (a) eine Datenanforderungsliste an den Mandanten,
(b) das leere Strukturgerüst eines Liquiditätsstatus zum Stichtag, (c) eine
Lückenliste der fehlenden Angaben, (d) eine Liste der Fundstellen, die der
Berufsträger nachzuschlagen hat.

RAHMEN
- Mandant: [MANDANT A], Rechtsform: [ANGABE], Branche: [ANGABE]
- Stichtag des Status: [STICHTAG], Datum der Datenerhebung: [ZEITPUNKT]
- Anlass der Anfrage: [Mandant fragt / Bank fragt / Kanzlei hat Indikatoren
  gesehen / Abschlusserstellung / sonstiger]
- Bisheriger Hinweis der Kanzlei nach Prompt 65: [erteilt / nicht erteilt /
  unbekannt]
- Insolvenzrechtler eingeschaltet: [ja / nein / in Anbahnung]

ANGABEN – jede Zeile ausfüllen oder "fehlt" eintragen, nichts ergänzen
- Kontostände zum Stichtag: [BETRÄGE je Konto als Kürzel]
- Kreditlinien: [BETRAG Limit], ausgenutzt: [BETRAG], Status:
  [unverändert / reduziert / gekündigt], Datum: [ZEITPUNKT]
- Kurzfristig verwertbare Mittel: [POSITIONEN mit Betrag und Verfügbarkeit]
- Fällige Verbindlichkeiten: [OPOS-LISTE mit Betrag, Fälligkeit,
  Gläubiger als Kürzel, Datum der Fälligstellung]
- Bestrittene oder gestundete Positionen: [POSITIONEN mit Betrag,
  Vereinbarung und Datum]
- Rückstände Steuern: [BETRAG] seit [ZEITPUNKT], Stundung: [ja / nein]
- Rückstände bei der Sozialversicherung insgesamt: [BETRAG] seit [ZEITPUNKT],
  Einzugsstellen: [ANZAHL] (der Beitrag wird nach § 28e Abs. 1 SGB IV als
  Gesamtsozialversicherungsbeitrag geschuldet; eine Aufteilung in Arbeitgeber-
  und Arbeitnehmeranteil wird hier nicht abgefragt)
- Beitragsrückstände wurden dem Berufsträger vor Einsatz dieses Prompts
  vorgelegt: [ja] (Pflichtangabe; ohne diese Bestätigung wird der Prompt nicht
  eingesetzt)
- Vollstreckung, Mahnbescheide, Titel: [keine / vorhanden], Anzahl: [ZAHL]
- Erwartete Einzahlungen im Anschlusszeitraum: [POSITIONEN mit Betrag,
  Herkunft und Verlässlichkeit]
- Insolvenzantrag gestellt oder angekündigt: [ja / nein / unbekannt]

VORGEHEN – IN DIESER REIHENFOLGE, JEDEN SCHRITT AUSWEISEN
1. Vollständigkeitsprüfung. Gehe die Angaben Zeile für Zeile durch und ordne
   jede ein: (vorhanden), (unvollständig) oder (fehlt). Ergänze nichts und
   schätze nichts. Nenne zu jeder unvollständigen Zeile, welche Einzelangabe
   fehlt – Betrag, Datum, Fälligkeit, Gläubiger oder Nachweis.
2. Datenanforderungsliste. Formuliere je fehlender Angabe genau eine Anforderung
   an den Mandanten: was genau, aus welcher Quelle, in welcher Form, bis wann
   (Datum als Leerfeld). Führe JEDE fehlende Angabe auf und lasse keine weg.
   Ordne die Liste in der Reihenfolge des Sachverhaltsbogens, nicht nach eigener
   Gewichtung; eine Rangfolge nach Bedeutung für die Prüfung bildest du nicht.
   Ergänze je Position in einem Satz, wofür die Angabe im Statusgerüst
   gebraucht wird.
3. Strukturgerüst des Liquiditätsstatus zum Stichtag. Baue eine Tabelle mit den
   Abschnitten: verfügbare Mittel, fällige Verbindlichkeiten, streitige oder
   gestundete Positionen (gesondert und nicht eingerechnet). Trage die
   gelieferten Beträge unverändert ein. Lasse alle Summen-, Saldo- und
   Ergebniszeilen LEER und beschrifte sie mit "vom Menschen zu ermitteln".
   Halte fest, dass der Status allein keine Aussage trägt und dass die
   Rechtsprechung des Bundesgerichtshofs den Status um einen Finanzplan für den
   Anschlusszeitraum ergänzt (BGH 28.06.2022 – II ZR 112/21 –
   für [JAHR] verifizieren). Zitiere keinen Leitsatz und keinen Entscheidungstext
   wörtlich; benenne nur Gericht, Datum, Aktenzeichen und den Gegenstand in einem
   Satz.
4. Streitige und gestundete Positionen. Weise sie in einer eigenen Rubrik aus,
   je mit der Angabe, worauf die Stundung oder das Bestreiten beruht und ob ein
   Nachweis vorliegt. Entscheide NICHT, ob eine Position einzurechnen ist – das
   ist eine rechtliche Wertung.
5. Anschlusszeitraum. Lege eine leere Spalte für den Anschlusszeitraum an und
   beschrifte sie mit "Zeitraum vom Berufsträger festzulegen". Bestimme den
   Zeitraum NICHT selbst und nenne keine Wochen- oder Monatszahl.
6. Nachzuschlagende Größen. Die von der Rechtsprechung verwendete
   Erheblichkeitsschwelle, der maßgebliche Betrachtungszeitraum und der
   Prognosezeitraum des § 19 Abs. 2 InsO sind NICHT zu nennen. Führe sie als
   Zeilen einer Tabelle "Vom Berufsträger nachzuschlagen" mit leerem Wertfeld,
   je mit Fundstelle und dem Zusatz "für [JAHR] verifizieren".
7. Fundstellen. Nenne POSITIV und je mit dem Zusatz "für [JAHR] verifizieren",
   nur in der internen Notiz und ohne Fristdauer, ohne Prozentwert und ohne
   Zeitraumangabe: § 17 Abs. 2 InsO, § 19 Abs. 2 InsO, § 15a Abs. 1 Satz 2 InsO,
   § 15b InsO einschließlich der Privilegierung steuerrechtlicher
   Zahlungspflichten in Absatz 8, § 252 Abs. 1 Nr. 2 HGB, § 102 StaRUG,
   BGH 24.05.2005 – IX ZR 123/04, BGH 19.12.2017 – II ZR 88/16,
   BGH 28.06.2022 – II ZR 112/21. Erfinde keine weitere Entscheidung und kein
   weiteres Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
8. Übergabemappe. Liste auf, welche Unterlagen ein Insolvenzrechtler zusätzlich
   benötigt, ohne die Prüfung vorwegzunehmen.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER VOLLSTÄNDIGKEIT ab: vollständig /
   in Teilen vollständig / nicht ausreichend für eine Prüfung. Diese Einschätzung
   bezieht sich auf die Datenlage, NICHT auf die wirtschaftliche Lage.
2. Nenne keinen Betrag, der nicht geliefert wurde. Was fehlt, bleibt Lücke.
3. Formuliere jede Ursachenaussage als Vermutung und kennzeichne sie als solche.
4. Berechne KEINE Fristen und nenne keine Fristlänge und keine Rechtsfolge einer
   Versäumnis als feststehend. Liste nur auf, WELCHE Fristen im Raum stehen, je
   mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   ohne Dauer, und ergänze: "Frist von einem Menschen zu berechnen und im
   Fristenprogramm zu erfassen." Die Bestimmung der Antragsfrist obliegt dem
   Insolvenzrechtler, nicht der Kanzlei.
5. Erzeuge KEINEN Text an den Mandanten außer der Datenanforderungsliste, und
   auch diese ohne jede Einordnung der Lage.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Kein Abbruchgrund sind: ein Krisenverdacht, hohe Rückstände, gekündigte Linien,
eine erkennbar angespannte Lage, fehlende Angaben oder eine Anfrage der Bank.
In diesen Fällen arbeitest du normal weiter – das ist der Regelfall dieses
Prompts.
Brich die Bearbeitung nur ab, wenn diese objektive Angabe vorliegt:
(a) im Feld "Insolvenzantrag gestellt oder angekündigt" steht "ja".
Gib dann nur aus: "Abbruchgrund liegt vor (Buchstabe angeben) – Bearbeitung an
dieser Stelle abgebrochen, Prüfung durch einen Berufsträger außerhalb des
KI-Werkzeugs."
Nicht abgeführte Arbeitnehmeranteile und Straf- oder Ermittlungsverfahren sind
hier bewusst kein Abbruchgrund: Sie werden nach `DATENSCHUTZ.md` gar nicht erst
in das Werkzeug eingegeben, sondern vor dem Einsatz vom Berufsträger geklärt.

AUSGABEFORMAT
1. "Einschätzung der Vollständigkeit der Datenlage"
2. "Vollständigkeitsprüfung und Lückenliste": Zeile des Sachverhaltsbogens |
   Einordnung (vorhanden) / (unvollständig) / (fehlt) | welche Einzelangabe fehlt
3. "Datenanforderung": Nr. | Angabe | Quelle | Form | warum gebraucht |
   bis wann (leer) | erledigt (leer)
4. "Liquiditätsstatus – Gerüst": Abschnitt | Position | Betrag | Datum |
   Nachweis | Anmerkung; Summen- und Saldozeilen leer
5. "Streitige und gestundete Positionen" – gesondert, nicht eingerechnet
6. "Vom Berufsträger nachzuschlagen": Größe | Fundstelle mit Zusatz |
   Wert (leer) | geprüft von (leer)
7. "Fristarten, die im Raum stehen" – ohne Datum und ohne Dauer
8. "Unterlagen für die Übergabe an den Insolvenzrechtler"
9. "Interne Notiz": Abgrenzung zu Prompt 65 und Prompt 66, Fundstellen,
   was nicht hinausgeht
10. "Was ich nicht sicher weiß"
```

## Anwendung

1. **Vorschaltfrage vor dem Werkzeugeinsatz, außerhalb des Werkzeugs zu beantworten:** Ist ein Insolvenzantrag gestellt oder angekündigt, ein Straf-, Ermittlungs- oder Steuerstrafverfahren anhängig oder sind Arbeitnehmeranteile zur Sozialversicherung nicht abgeführt? Bei einem Ja wird dieser Prompt nicht eingesetzt; der Berufsträger übernimmt außerhalb des KI-Werkzeugs, bei nicht abgeführten Arbeitnehmeranteilen zusätzlich ein Strafverteidiger. Die Antwort wird in der Handakte vermerkt, nicht im Werkzeug.
2. Klären, wer den Auftrag hat: Die Vorbereitung von Unterlagen ist Kanzleiarbeit, die Prüfung der Insolvenzreife nicht. Fehlt ein Insolvenzrechtler, ist zuerst Prompt 65 abzuarbeiten.
3. OPOS-Kreditoren mit Fälligkeit und Datum der Fälligstellung exportieren, Kontostände und freie Linien zum Stichtag festhalten, alles auf Kürzel umstellen. Ein Status ohne Stichtag ist wertlos.
4. Stundungs- und Ratenvereinbarungen mit Datum belegen. Eine mündlich behauptete Stundung ist kein Nachweis und bleibt in der Rubrik der streitigen Positionen.
5. Die Datenanforderungsliste unverändert an den Mandanten geben, Rücklauf mit Datum zur Akte nehmen. Der Rücklauf ist der eigentliche Ertrag dieses Prompts.
6. Ergebnis und Datum der Datenerhebung im DMS ablegen. Der Status altert vom Tag der Erhebung an; jede spätere Verwendung braucht einen neuen Stichtag.
7. Ergebnis nicht an die Bank geben – dafür gilt Prompt 67 samt der dort geforderten dokumentierten Einwilligung.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Das Ergebnis ist ein Entwurf. Eine zweite Person gleicht jede Betragszeile und jedes Datum gegen den Export ab; Positionen ohne Quelle werden gestrichen. **Die Freigabe erteilt ausnahmslos ein Berufsträger**, dokumentiert mit Datum (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Jede Beurteilung streichen.** Aussagen zu Zahlungsunfähigkeit, drohender Zahlungsunfähigkeit, Überschuldung, Insolvenzreife oder Antragspflicht – auch entlastende – ersatzlos entfernen. Eine Antwort, die eine Quote bildet oder mit einer Schwelle vergleicht, ist zu verwerfen.
- **Leere Summenzeilen bleiben leer.** Hat das Modell gerechnet, ist das Ergebnis unbrauchbar: Die Summenbildung entscheidet über die Einordnung und ist damit selbst Teil der rechtlichen Wertung.
- **Keine Prozentwerte, keine Zeiträume aus der Rechtsprechung im Text.** Sie stehen ausschließlich in der Tabelle „Vom Berufsträger nachzuschlagen" mit leerem Wertfeld.
- **Keine wörtlichen Leitsatzzitate.** Zu den genannten Entscheidungen sind Gericht, Datum und Aktenzeichen gesichert, der Wortlaut der Leitsätze ist es nicht. Jedes wörtliche Zitat aus der KI-Antwort ist zu löschen und bei Bedarf an der Primärquelle zu belegen.
- **Fristen berechnet ein Mensch.** Kein Datum und keine Dauer aus der KI-Antwort übernehmen; die Antragsfrist bestimmt der Insolvenzrechtler.
- **Zone Rot beachten.** Nicht abgeführte Arbeitnehmeranteile und Angaben zu Straf- oder Ermittlungsverfahren gehören nach `DATENSCHUTZ.md` in kein KI-Werkzeug – auch nicht als Betragszeile und auch nicht als bloßes „ja" oder „nein". Der Sachverhaltsbogen fragt sie deshalb nicht ab; sie werden über die Vorschaltfrage in „Anwendung", Punkt 1, geklärt. Steht in einer KI-Antwort trotzdem eine solche Angabe, ist die Antwort zu verwerfen und der Vorfall nach `DATENSCHUTZ.md`, Abschnitt 8, zu behandeln.
- **Rechtsstand prüfen an:** § 17 Abs. 2, § 19 Abs. 2, § 15a Abs. 1 Satz 2 und § 15b InsO einschließlich Absatz 8, § 252 Abs. 1 Nr. 2 HGB, § 102 StaRUG, § 28e Abs. 1 SGB IV sowie §§ 3 und 5 RDG im amtlichen Volltext (gesetze-im-internet.de); die Entscheidungen BGH 24.05.2005 – IX ZR 123/04, BGH 19.12.2017 – II ZR 88/16 und BGH 28.06.2022 – II ZR 112/21 an der Entscheidungsdatenbank des Bundesgerichtshofs; ergänzend DATEV LEXinform und die Hinweise der Bundessteuerberaterkammer zur Unternehmensfortführung. Datum, Aktenzeichen und Fortgeltung jeder Entscheidung am Original nachlesen (Stand – für [JAHR] verifizieren).

## Varianten

- **Nur Anforderung:** „Erzeuge ausschließlich die Datenanforderungsliste als abhakbares Formular mit Kästchen ☐, ohne Statusgerüst."
- **Zweiter Stichtag:** „Erzeuge dasselbe Gerüst für einen zweiten Stichtag und stelle die Positionen nebeneinander, ohne Veränderungen zu bewerten."
- **Übergabemappe:** „Erzeuge ausschließlich das Verzeichnis der Unterlagen für die Übergabe an einen Insolvenzrechtler, mit Spalte ‚liegt vor (leer)'."
- **Gläubigerübersicht:** „Erzeuge eine Gläubigerübersicht nach Kürzeln mit Betrag, Fälligkeit und Nachweis, ohne Rangfolge und ohne Bewertung."
- **Hinweisschreiben:** Prompt 65. **13-Wochen-Planung:** Prompt 66. **Bankgespräch:** Prompt 67. **Krisenfrüherkennung:** Prompt 75.
