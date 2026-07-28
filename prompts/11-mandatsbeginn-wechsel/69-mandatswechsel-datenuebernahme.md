# 69 – Mandatswechsel: Datenübernahme vom Vorberater und Herausgabepflichten

**Problem:** Der Vorberater rückt Daten nicht heraus oder liefert einen unbrauchbaren Export – und die Kanzlei streitet, statt zu wissen, was sie verlangen darf und was sie beim eigenen Mandatsende herausgeben muss.
**Rolle:** Steuerberater, Kanzleiorganisation
**DATEV-Bezug:** DATEV-Datenübernahme (Bestandsdaten Rechnungswesen und Lohn), DATEV DMS, DATEV Arbeitsplatz, bei Lohn Übernahme der Personalstammdaten nach DATEV Lohn und Gehalt bzw. LODAS
**Was du bereitstellen musst:** Übernahmezeitpunkt und letztes bearbeitetes Jahr, Rechtsform und Gewinnermittlungsart, betroffene Bereiche, bereits gelieferte Bestände, Stand der Vollmachten, bekannte offene Verfahren und Fristen, Stand der Honorarforderungen des Vorberaters.
**Datensparsamkeit:** Mandant als `Mandant A`, Vorberater als `Vorberater`, Beschäftigte als `AN 1`. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`); ein laufender Rechtsbehelf wird über Verfahrensart und Streitpunkt beschrieben, nicht über das Aktenzeichen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG). **Diese Einwilligung ist von der Entbindung des Vorberaters von der Verschwiegenheit zu unterscheiden; die eine ersetzt die andere nicht.**

## Prompt

```text
Du bist Steuerberater und organisierst die Übernahme eines Mandats. Du arbeitest
listenbasiert und trennst streng, was verlangt werden kann, von dem, was nur
erbeten werden kann.

ENTBINDUNG ZUERST – VOR DEM ANSCHREIBEN
Der Vorberater unterliegt gegenüber der übernehmenden Kanzlei der
Verschwiegenheit (§ 57 StBerG, § 203 StGB – für [JAHR] verifizieren). Er darf
ohne schriftliche Entbindung durch den Mandanten nichts herausgeben und nichts
bestätigen. Beginne die Antwort mit dem Abschnitt "Entbindung und Vollmachten"
und trenne dort drei Dinge: (a) Entbindung des Vorberaters von der
Verschwiegenheit gegenüber dieser Kanzlei, (b) Herausgabeverlangen des Mandanten
gegenüber dem Vorberater, (c) Vollmacht gegenüber dem Finanzamt und Widerruf der
Vollmacht des Vorberaters. Liegt (a) nicht vor, sage ausdrücklich: kein Versand,
zuerst Erklärung des Mandanten einholen; entwirf dafür einen kurzen Text zur
Unterschrift des Mandanten, der dem Anschreiben beizulegen ist.

FRISTEN UNMITTELBAR DANACH
Lasse auf "Entbindung und Vollmachten" sofort den Abschnitt "Sofort zu erfassen"
folgen, vor jeder weiteren Arbeit: alle erkennbaren laufenden Verfahren und
Fristen, jede in eigener Zeile. Eine übersehene Rechtsbehelfsfrist ist der
teuerste Fehler dieses Vorgangs. Berechne KEINE Frist, nenne keine Fristlänge und
keine Rechtsfolge einer Versäumnis als feststehend. Benenne nur, WELCHE Frist im
Raum steht, mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne
Datum und Dauer, und ergänze: "Frist von einem Menschen zu berechnen und im
Fristenprogramm zu erfassen."

AUFGABE
Erstelle Teil A (Anforderung beim Vorberater) und Teil B (Prüfliste
Vollständigkeit).

RAHMEN
- Mandant: [MANDANT A], Rechtsform: [ANGABE]
- Gewinnermittlung: [Bilanz / EÜR], Kontenrahmen: [SKR03 / SKR04 / anderer]
- Übernahme ab: [ZEITPUNKT], letztes bearbeitetes Jahr: [ZEITRAUM]
- Betroffene Bereiche: [Finanzbuchhaltung / Lohn / Abschluss / Erklärungen]
- Bereits gelieferte Bestände: [ANGABEN oder "keine"]
- Vollmachten: [erteilt / widerrufen / unklar]
- Entbindung von der Verschwiegenheit: [liegt schriftlich vor / liegt nicht vor / unklar]
- Bekannte offene Verfahren: [ANGABEN oder "unbekannt"]
- Honorarforderungen des Vorberaters: [offen / beglichen / unklar]

TEIL A – ANFORDERUNG BEIM VORBERATER
1. Datenliste als abhakbare Liste (Kästchen ☐), je Position: Bezeichnung,
   Format (DATEV-Bestandsdaten, Auswertung, Beleg, Papier), Zweck und die
   Einordnung (herausgabepflichtig – prüfbedürftig) oder
   (nur auf Bitte erhältlich). Nimm mindestens auf: Salden und Vortragswerte,
   Anlagenspiegel und Anlagenverzeichnis, Bestände an
   Investitionsabzugsbeträgen, Verlustvorträge, steuerliches Einlagekonto,
   Lohnkonten und Personalstammdaten, Vollmachten, laufende Rechtsbehelfe und
   Fristen, Prüfungsberichte, Verfahrensdokumentation.
2. Anschreiben an den Vorberater: sachlich, kollegial, ohne Vorwurf, mit
   Fristsetzung als Leerfeld, Bezeichnung der Unterlagen und Bitte um
   Bestätigung der Vollständigkeit. Das Anschreiben tritt als Bitte im Auftrag
   des Mandanten auf, nicht als Anspruchsdurchsetzung: keine Androhung von
   Maßnahmen, keine Rechtsfolgenbehauptung, keine Fristsetzung mit Rechtsfolge.
   Die Durchsetzung eines Herausgabeanspruchs ist Rechtsdienstleistung
   (§§ 3 und 5 RDG – für [JAHR] verifizieren) und gehört zum Berufsträger, im
   Streitfall zu einem Rechtsanwalt.
3. Rechtsgrundlagen des Herausgabeanspruchs POSITIV benennen, je mit dem Zusatz
   "für [JAHR] verifizieren": § 66 Abs. 1 bis 4 StBerG, §§ 667 und 675 BGB,
   § 147 AO, § 32 BOStB, § 57 StBerG und § 203 StGB zur Verschwiegenheit,
   §§ 3 und 5 RDG zur Grenze der Rechtsdienstleistung, die Hinweise der
   Bundessteuerberaterkammer zum Mandatswechsel.
   Bist du unsicher: "Fundstelle offen – bitte recherchieren".
4. Prüfschritt "Was darf zurückbehalten werden?": Trenne zwei Fragen.
   (a) Umfang: Der Rückgabeanspruch erfasst nur die Schriftstücke, die der
       Berater vom Mandanten oder für ihn erhalten hat. NICHT erfasst sind
       der Briefwechsel zwischen Berater und Mandant, die Schriftstücke, die der
       Mandant bereits in Urschrift oder Abschrift erhalten hat, und die zu
       internen Zwecken gefertigten Arbeitspapiere
       (§ 66 Abs. 2 StBerG – für [JAHR] verifizieren). Nenne alle drei Ausnahmen
       einzeln.
   (b) Zurückbehaltungsrecht wegen offener Vergütung: voraussetzungsvoll und
       durch eine Unangemessenheitsschranke begrenzt
       (§ 66 Abs. 3 StBerG – für [JAHR] verifizieren). Beurteile es NICHT
       abschließend, benenne die zu klärenden Punkte und lege sie dem
       Berufsträger vor. Gib keine Empfehlung zu Zahlung oder Verweigerung.
       Verweise auf Prompt 16 für die eigene Seite.
   (c) Aufbewahrungspflicht der Handakte und ihr Verhältnis zur Herausgabe
       (§ 66 Abs. 1 und Abs. 4 StBerG – Dauer für [JAHR] verifizieren): Vor
       Herausgabe von Originalen ist der eigene Aufbewahrungsbestand zu sichern.

TEIL B – PRÜFLISTE VOLLSTÄNDIGKEIT
5. Prüfliste der übernommenen Bestände als Tabelle: Position | erwartet |
   erhalten (leer) | geprüft von (leer) | Abweichung (leer). Nimm ausdrücklich
   die Positionen auf, deren Fehlen erst Jahre später auffällt: Verlustvorträge,
   Investitionsabzugsbeträge samt Investitionsjahr, steuerliches Einlagekonto,
   Anschaffungsdaten und Restnutzungsdauern, ausgeübte Bewertungswahlrechte,
   Rückstellungsherleitungen, Behaltensfristen, Lohnvortragswerte und Lohnkonten
   des laufenden Jahres, Verfahrensdokumentation, Aufbewahrungsstände.
6. Je Position: woran das Fehlen erkennbar ist und was dann zu tun ist.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Erfinde keine Position, keinen Bestand und keine Zahl.
2. Nenne KEINE Aufbewahrungsdauer, keine Frist und keine Betragsgrenze als
   feststehend – nur nachzuschlagend mit dem Zusatz "für [JAHR] verifizieren".
3. Trenne durchgehend (herausgabepflichtig – prüfbedürftig) von
   (nur auf Bitte erhältlich). Behaupte keinen Anspruch, der nicht belegt ist.
4. Bewerte niemanden – keine Aussage zur Arbeitsweise des Vorberaters, auch
   nicht mittelbar.
5. Leite eine wiederverwendbare Kanzleicheckliste ab und einen Spiegelabschnitt
   "Eigenes Mandatsende": was die Kanzlei selbst herausgeben muss. Halte fest,
   dass vor der Herausgabe von Originalen Kopien im eigenen Bestand zu sichern
   sind, weil die Aufbewahrungspflicht der Handakte durch die Herausgabe nicht
   endet.

AUSGABEFORMAT
1. "Entbindung und Vollmachten" samt Text zur Unterschrift des Mandanten
2. "Sofort zu erfassen" (Verfahren und Fristarten)
3. "Einschätzung der Eindeutigkeit" 4. "Teil A: Datenliste"
5. "Anschreiben an den Vorberater (Entwurf)" 6. "Rechtsgrundlagen"
7. "Was darf zurückbehalten werden?" 8. "Teil B: Prüfliste Vollständigkeit"
9. "Kanzleicheckliste und eigenes Mandatsende" 10. "Interne Notiz"
11. "Was ich nicht sicher weiß"
```

## Anwendung

1. Entbindung des Vorberaters von der Verschwiegenheit schriftlich einholen und Vollmachten klären und in der Vollmachtsdatenbank erfassen, bevor angefordert wird. Ohne Entbindung geht kein Anschreiben hinaus.
2. "Sofort zu erfassen" am Tag der Übernahme abarbeiten: Fristen in das Fristenprogramm, mit Nachprüfung.
3. Als DATEV-Bestandsdaten anfordern, nicht als Papier oder PDF – nur so lassen sich Salden, Anlagenverzeichnis und Lohnvortragswerte übernehmen.
4. Nach dem Import Teil B abarbeiten, Abweichungen sofort nachfassen.
5. Anforderung, Antwort und Prüfliste im DMS ablegen; Fehlendes als offen dokumentieren.

## Qualitätssicherung

- **Fristen zuerst, mit Vier-Augen-Nachprüfung.** Rechtsbehelfs- und Erklärungsfristen erfasst ein Mensch, eine zweite Person prüft nach. Kein Datum aus der KI-Antwort übernehmen.
- **Entbindung von der Verschwiegenheit vor dem Versand prüfen.** Ohne schriftliche Entbindung durch den Mandanten darf der Vorberater nichts herausgeben und nichts bestätigen (§ 57 StBerG, § 203 StGB – Fundstellen für [JAHR] verifizieren); dann geht statt des Anschreibens nur der Text zur Unterschrift des Mandanten hinaus.
- **Herausgabeanspruch nicht überdehnen.** Der Briefwechsel zwischen Berater und Mandant, bereits in Urschrift oder Abschrift erhaltene Schriftstücke und zu internen Zwecken gefertigte Arbeitspapiere sind nicht herausgabepflichtig; jede Anspruchsbehauptung des Modells ist prüfbedürftig (§ 66 Abs. 2 StBerG – für [JAHR] verifizieren).
- **Vor Herausgabe von Originalen Kopien sichern.** Die Aufbewahrungspflicht der Handakte endet nicht mit der Herausgabe (§ 66 Abs. 1 und Abs. 4 StBerG – Dauer für [JAHR] verifizieren).
- **Zurückbehaltungsrecht nicht selbst beurteilen.** Das prüft ein Berufsträger im Einzelfall; das Anschreiben enthält dazu keine Rechtsbehauptung.
- **Vollständigkeit belegen.** Salden, Verlustvorträge, Investitionsabzugsbeträge und Einlagekonto gegen die Bescheide abgleichen, nicht gegen die Angabe des Vorberaters.
- **Freigabe und Vier-Augen:** Das Ergebnis ist ein Entwurf. Das Anschreiben gibt ein Berufsträger frei, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`); Teil B zeichnet eine zweite Person ab.
- **Rechtsstand prüfen an:** § 66 Abs. 1 bis 4 StBerG, § 57 StBerG, §§ 667 und 675 BGB, § 147 AO, § 203 StGB, §§ 3 und 5 RDG (gesetze-im-internet.de), § 32 BOStB, den Hinweisen der Bundessteuerberaterkammer zum Mandatswechsel sowie der DATEV-Hilfe zur Datenübernahme.

## Varianten

- **Nur Lohn:** „Beschränke die Listen auf Lohnkonten, Personalstammdaten und Vortragswerte."
- **Keine Antwort:** „Entwirf ein zweites Schreiben mit Bezug auf das erste, ohne Rechtsbehauptung und ohne Drohung."
- **Eigenes Mandatsende:** „Erzeuge nur die Herausgabeliste für ein ausscheidendes Mandat."
- **Fristen:** Prompt 35. **Neumandat:** Prompt 68.
