# 65 – Krisenindikatoren erkennen und Hinweisschreiben an den Mandanten entwerfen

**Problem:** Die Kanzlei sieht in Bilanz und betriebswirtschaftlicher Auswertung klare Krisenindikatoren, dokumentiert aber keinen Hinweis – genau darauf stützt der Insolvenzverwalter später den Regress.
**Rolle:** ausschließlich Berufsträger – der Hinweis ist nicht delegierbar; die Bilanzbuchhaltung unterstützt nur bei der Datenaufbereitung
**DATEV-Bezug:** Kanzlei-Rechnungswesen (Bilanz, BWA), DATEV Kennzahlenanalyse, DATEV Analyse und Planung, DATEV Frühwarnservice, DATEV DMS für die Handaktendokumentation
**Was du bereitstellen musst:** Exportierte Abschlusszahlen (Eigenkapital, Ergebnisse mehrerer Jahre, Gesellschafterdarlehen), BWA des laufenden Jahres, Kapitaldienst, Lieferantenlaufzeiten, Rückstände bei Steuern und Sozialversicherung, Kreditlinien, Zahlungsmodalitäten, Gesprächsdatum und -inhalt.
**Datensparsamkeit:** Mandant als `Mandant A`, Beteiligte nur als Rolle (`Geschäftsführung`, `Gesellschafter 1`, `Hausbank`, `Lieferant 1`). Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Keine Angaben zu Gesundheit, persönlichen Umständen oder privaten Vermögensverhältnissen der Gesellschafter über das für die Indikatoren Nötige hinaus; ein Gesellschafterdarlehen wird über Betrag und Rangstellung beschrieben, nicht über die Person. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und dokumentierst einen
Hinweis an den Mandanten. Du beurteilst nichts – du machst Indikatoren und ihre
Prüfbedürftigkeit sichtbar.

ABGRENZUNG – GILT FÜR DIE GANZE ANTWORT
Triff KEINE Aussage darüber, ob Zahlungsunfähigkeit oder Überschuldung vorliegt,
ob Insolvenzreife eingetreten ist oder ob eine Antragspflicht besteht – auch
keine entlastende ("noch nicht insolvenzreif"). Erstelle weder
Fortbestehensprognose noch Liquiditätsstatus. Diese Beurteilung unterliegt einem
Beratungsvorbehalt, ist Rechtsdienstleistung und für den Steuerberater
allenfalls als Nebenleistung nach § 5 RDG denkbar
(Rechtsgrundlage – für [JAHR] verifizieren); sie gehört zu einem
Insolvenzrechtler.

AUFGABE
Erzeuge drei getrennte Ergebnisse: (a) Einordnung der Indikatoren nach
Prüfbedürftigkeit, (b) ein zurückhaltend formuliertes Hinweisschreiben,
(c) einen Handaktenvermerk über das geführte Gespräch.

MANDANTENRAHMEN
- Mandant: [MANDANT A], Rechtsform: [ANGABE], Branche und Größe: [ANGABEN]
- Zeitraum: [ZEITRAUM], letzter festgestellter Abschluss: [ZEITPUNKT]
- Auftragsart des Abschlusses: [ohne Beurteilung / mit
  Plausibilitätsbeurteilung / mit umfassenden Beurteilungen]
- Bisherige Hinweise der Kanzlei: [dokumentiert / mündlich / keine]

GESPRÄCHSANGABEN – nur ausfüllen, wenn das Gespräch geführt wurde
- Datum und Form: [ZEITPUNKT], [persönlich / telefonisch / Videokonferenz]
- Beteiligte, nur als Rolle: [ANGABEN]
- Was mitgeteilt wurde: [ANGABEN]
- Reaktion des Mandanten: [ANGABEN]
- Übergebene Unterlagen: [ANGABEN]

INDIKATORENRASTER – jede Zeile ausfüllen oder "unbekannt" eintragen
- Nicht durch Eigenkapital gedeckter Verlust: [BETRAG] zum [STICHTAG]
- Jahresergebnisse der letzten drei Jahre: [BETRÄGE]
- Eigenkapital und Gesellschafterdarlehen: [BETRÄGE],
  Rangrücktritt: [vorhanden / nicht vorhanden / unbekannt]
- Kapitaldienst: [BETRAG je Jahr], erwirtschafteter Überschuss: [BETRAG]
- Lieferantenlaufzeiten: [TAGE aktuell] gegenüber [TAGE Vorjahr]
- Rückstände bei Steuern: [BETRAG] seit [ZEITPUNKT]
- Rückstände bei Sozialversicherungsbeiträgen: [nein / ja, nur Arbeitgeberanteile /
  ja, auch Arbeitnehmeranteile / unbekannt], Betrag: [BETRAG] seit [ZEITPUNKT]
- Kreditlinien: [unverändert / reduziert / gekündigt], Datum: [ZEITPUNKT]
- Zahlungsmodalitäten: [unverändert / Vorkasse / Lieferstopp / Mahnbescheide]
- Weiteres: [z. B. Stundungsantrag, Pfändung, Bankwechsel]

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht entscheidbar. Benenne fehlende Angaben, arbeite mit
   benannten Annahmen und erfinde keine Zahlen.
2. Ordne JEDEN Indikator ein: Wert, Bedeutung in einem Satz, Einordnung als
   (prüfbedürftig) oder (nicht auffällig nach den Angaben). Keine Gesamtnote,
   keine Ampel, keine Rangfolge eines Insolvenzrisikos. Ordne die Indikatoren im
   Licht der angegebenen Auftragsart des Abschlusses ein und halte fest, welche
   Erkennbarkeit sich daraus ergibt.
3. Formuliere jede Ursachenaussage als Vermutung, solange sie nicht aus den
   Angaben folgt, und kennzeichne sie als solche.
4. Hinweisschreiben – nur, wenn mindestens ein Indikator als (prüfbedürftig)
   eingeordnet ist; andernfalls gib statt des Schreibens den Satz aus: "Kein
   Indikator prüfbedürftig – kein Hinweisschreiben erzeugt; Einordnung bleibt
   intern." Ist ein Schreiben zu erzeugen: Sie-Form, höchstens 300 Wörter,
   sachlich, ohne Alarmierung und ohne Beschönigung. Es
   (a) benennt die Indikatoren mit Wert und Stichtag,
   (b) sagt, dass eine insolvenzrechtliche Prüfung veranlasst werden MUSS und
       dass diese Prüfung der Geschäftsleitung obliegt, nicht der Kanzlei,
   (c) sagt, dass die insolvenzrechtlichen Handlungs- und Antragsfristen kurz
       sind und von einem Insolvenzrechtler zu bestimmen sind – ohne Dauer, ohne
       Datum, ohne Rechtsfolge als feststehend,
   (d) empfiehlt ausdrücklich einen Insolvenzrechtler und stellt in einem Satz
       klar, dass die Kanzlei diese Prüfung nicht vornimmt,
   (e) enthält KEINE insolvenzrechtliche Beurteilung, auch keine entlastende,
   (f) bittet um schriftliche Rückmeldung bis zu einem von der Kanzlei
       einzusetzenden Datum ([DATUM]) und nennt einen Terminvorschlag als
       Leerfeld.
5. Handaktenvermerk: Datum und Form des Gesprächs, Beteiligte nur als Rolle,
   vorliegende Zahlen, Mitteilung, Empfehlung, Reaktion, übergebene Unterlagen,
   Wiedervorlage als Leerfeld. Erfinde keinen Gesprächsinhalt. Fehlen die
   Gesprächsangaben, erzeuge KEINEN Vermerk, sondern ein leeres Vermerkformular
   mit den Feldern und dem Satz "Gespräch noch nicht geführt oder nicht
   dokumentiert".
6. Nenne die einschlägigen Fundstellen POSITIV, je mit dem Zusatz
   "für [JAHR] verifizieren", und nur in der internen Notiz: Rechtsprechung des
   Bundesgerichtshofs zur Hinweispflicht des Steuerberaters bei erkennbarer
   Insolvenzreife, § 15a InsO, § 15b InsO, §§ 17 und 19 InsO,
   § 252 Abs. 1 Nr. 2 HGB, Vorenthalten von Arbeitnehmerbeiträgen
   (Fundstelle offen – bitte recherchieren), Hinweise der
   Bundessteuerberaterkammer zur Unternehmensfortführung. Bist du unsicher:
   "Fundstelle offen – bitte recherchieren".
7. Berechne KEINE Fristen, nenne keine Fristlängen und keine Rechtsfolgen einer
   Versäumnis als feststehend. Liste nur auf, WELCHE Fristen im Raum stehen, je
   mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   Dauer, und ergänze: "Frist von einem Menschen zu berechnen und im
   Fristenprogramm zu erfassen."

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung:
Brich ab, wenn (a) Arbeitnehmeranteile zur Sozialversicherung nicht abgeführt
wurden (Straftatbestand – Fundstelle für [JAHR] verifizieren), (b) ein
Insolvenzantrag gestellt oder angekündigt ist, (c) der Mandant von einem
eingetretenen Insolvenzgrund oder einer Antragspflicht berichtet, oder (d) ein
Straf- oder Ermittlungsverfahren erwähnt wird. Prüfe NICHT selbst, ob ein
Insolvenzgrund vorliegt. Gib bei Abbruch nur aus: "Anzeichen für einen
eskalierten Insolvenzsachverhalt – Bearbeitung abgebrochen, Prüfung durch einen
Berufsträger außerhalb des KI-Werkzeugs, Rückstände bei Arbeitnehmeranteilen
gehören zusätzlich zu einem Strafverteidiger."

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit"
2. "Indikatorentabelle": Indikator | Wert | Bedeutung | Einordnung
3. "Hinweisschreiben (Entwurf)" 4. "Handaktenvermerk (Entwurf)"
5. "Fristarten, die im Raum stehen" 6. "Interne Notiz": fehlende Angaben,
Fundstellen, was nicht hinausgeht 7. "Was ich nicht sicher weiß"
```

## Anwendung

1. Zahlen aus Bilanz, BWA und Kennzahlenanalyse exportieren, auf Kürzel umstellen; Frühwarnservice als zweite Quelle nutzen.
2. Erst nach dem Gespräch ausführen – der Vermerk dokumentiert es, er ersetzt es nicht.
3. Schreiben nachweisbar zustellen. Ein Hinweis ohne Nachweis wirkt im Regressfall wie kein Hinweis.
4. Vermerk und Schreiben im DMS ablegen, mit Wiedervorlage. Bleibt eine Reaktion aus, Hinweis wiederholen und das gesondert dokumentieren.

## Qualitätssicherung

- **Jede Beurteilung streichen.** Aussagen zu Zahlungsunfähigkeit, Überschuldung, Insolvenzreife oder Antragspflicht – auch entlastende – ersatzlos entfernen.
- **Zahlen gegen den Export prüfen.** Eigenkapital, Jahresergebnisse, Rückstände und Kapitaldienst nachrechnen; Werte ohne Quelle löschen.
- **Abgrenzung zur Rechtsdienstleistung.** Das Schreiben empfiehlt einen Insolvenzrechtler und wertet nicht (Beratungsvorbehalt, § 5 RDG – Rechtsgrundlage für [JAHR] verifizieren).
- **Freigabe und Vier-Augen:** Das Ergebnis ist ein Entwurf. Freigabe ausnahmslos durch einen Berufsträger, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`); Schreiben und Vermerk liest eine zweite Person gegen. Fristen berechnet ein Mensch.
- **Rückstände bei Arbeitnehmeranteilen berühren die Zone Rot in `DATENSCHUTZ.md` (Strafsachverhalt) und gehören nicht in ein KI-Werkzeug.**
- **Rechtsstand prüfen an:** § 15a, § 15b, §§ 17 und 19 InsO, § 252 Abs. 1 Nr. 2 HGB (gesetze-im-internet.de), der Straftatbestand des Vorenthaltens von Arbeitnehmerbeiträgen (Fundstelle offen – bitte recherchieren), der Rechtsprechung des Bundesgerichtshofs zur Hinweispflicht des Steuerberaters, den Hinweisen der Bundessteuerberaterkammer zur Unternehmensfortführung, DATEV LEXinform.

## Varianten

- **Nur Vermerk:** „Erzeuge ausschließlich den Handaktenvermerk."
- **Zweiter Hinweis:** „Entwirf ein zweites Schreiben mit Bezug auf den ersten Hinweis, ohne neue Wertung."
- **Übergabe:** „Liste die Unterlagen, die ein Insolvenzrechtler benötigt."
- **Planung:** Prompt 66. **Bankgespräch:** Prompt 67.
