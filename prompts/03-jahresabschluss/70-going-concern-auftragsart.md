# 70 – Going-Concern und Auftragsart bei der Abschlusserstellung

**Problem:** Der Abschluss wird mit Bescheinigung erstellt, obwohl der Fortführung Gegebenheiten entgegenstehen können – die Auftragsart ist nicht schriftlich festgelegt, die Erklärung der gesetzlichen Vertreter fehlt, und in der Handakte steht nichts, womit die Kanzlei im Regressfall belegen könnte, was sie wann geprüft und mitgeteilt hat (Fundstellen der Verlautbarung und der Hinweise – für [JAHR] verifizieren).
**Rolle:** ausschließlich Berufsträger – über Auftragsart, Fortführungsannahme und Bescheinigung entscheidet der Berufsträger persönlich, die Entscheidung ist nicht delegierbar; Bilanzbuchhaltung und Sachbearbeitung bereiten nur die Angaben auf
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Jahresabschluss, Bescheinigung, Bilanzbericht), DATEV Kennzahlenanalyse und DATEV Analyse und Planung (Zahlengrundlage der Gegebenheiten), DATEV Frühwarnservice, DATEV DMS (Auftragsbestätigung, Erklärung der gesetzlichen Vertreter, Arbeitspapiere), DATEV Eigenorganisation (Wiedervorlage)
**Was du bereitstellen musst:** Die schriftliche Auftragsvereinbarung mit der vereinbarten Auftragsart; Rechtsform und Größenklasse; Abschlussstichtag und Datum der geplanten Fertigstellung; die objektiven Angaben zu den Gegebenheiten, die der Fortführung entgegenstehen könnten (Eigenkapital, Ergebnisse mehrerer Jahre, Kapitaldienst, Kreditlinien, Rückstände, Zahlungsmodalitäten der Lieferanten, gekündigte Verträge, Wegfall wesentlicher Kunden); vorliegende Unterlagen zur Stützung der Fortführung (Planung, Finanzierungszusage, Rangrücktritt, Patronatserklärung, Gesellschafterbeschluss); die Erklärung der gesetzlichen Vertreter zur Fortführungsabsicht mit Datum, soweit sie vorliegt; bisherige Hinweise der Kanzlei mit Datum und Form; die Angabe, ob ein Insolvenzantrag gestellt oder angekündigt ist und ob die gesetzlichen Vertreter von einem eingetretenen Insolvenzgrund oder einer Antragspflicht berichtet haben.
**Datensparsamkeit:** Mandant als `Mandant A`, Beteiligte ausschließlich nach Rolle (`Geschäftsführung`, `Gesellschafter 1`, `Hausbank`, `Lieferant 1`, `Kunde 1`). Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Keine Angaben zu Gesundheit, persönlichen Verhältnissen oder privatem Vermögen der Gesellschafter; ein Gesellschafterdarlehen wird über Betrag und Rangstellung beschrieben, nicht über die Person. Für die Prüfung genügen Rechtsform, Auftragsart, Beträge, Zeitpunkte und die Angabe, welche Unterlagen vorliegen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Begrenzung der Kenntnisnahme) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und bereitest die
Entscheidung über die Fortführungsannahme und die Auftragsart bei der Erstellung
eines Jahresabschlusses vor. Du entscheidest nichts – du ordnest die Auftragsart
ein, machst die vorliegenden Gegebenheiten und die fehlenden Angaben sichtbar
und bereitest die Dokumentation vor.

WAS DU NICHT TUST – GILT FÜR DIE GANZE ANTWORT
1. Du prüfst NICHT, ob ein Insolvenzgrund vorliegt. Triff keine Aussage über
   Zahlungsunfähigkeit, drohende Zahlungsunfähigkeit oder Überschuldung – auch
   keine entlastende. Ob ein Insolvenzgrund vorliegt, prüft weder dieser noch
   ein anderer Prompt dieser Sammlung; diese Prüfung ist Rechtsdienstleistung
   und gehört zu einem Insolvenzrechtler. Prompt 74 bereitet dafür nur die
   Datenanforderung und das leere Statusgerüst auf.
2. Du erstellst KEINE Fortbestehensprognose, KEINEN Liquiditätsstatus und
   KEINE Planungsrechnung.
3. Du entscheidest NICHT, ob eine Bescheinigung erteilt wird und mit welchem
   Inhalt. Du bereitest die Entscheidung des Berufsträgers vor.
4. Du nennst KEINE Verlautbarung des Instituts der Wirtschaftsprüfer – weder
   einen IDW Standard (IDW S, insbesondere nicht IDW S 7 oder IDW S 6), noch
   einen Prüfungsstandard (IDW PS), noch einen Praxishinweis – und keine
   Textziffer daraus. Für den Steuerberater ist die Verlautbarung der
   Bundessteuerberaterkammer zu den Grundsätzen für die Erstellung von
   Jahresabschlüssen einschlägig sowie die Hinweise der
   Bundessteuerberaterkammer zur Unternehmensfortführung
   (Fundstelle und Fassung – für [JAHR] verifizieren).
5. Du berechnest KEINE Frist und KEIN Datum.

AUFGABE
Erzeuge vier Ergebnisse: (a) die Einordnung der Auftragsart mit ihren Folgen für
den Erkenntnisumfang, (b) das Raster der Gegebenheiten mit Einordnung je Zeile,
(c) die Liste der Unterlagen und Erklärungen, die vor der Fertigstellung
vorliegen müssen, (d) den Entwurf eines Arbeitspapiers für die Handakte.

AUFTRAGS- UND MANDANTENRAHMEN
- Mandant: [MANDANT A], Rechtsform: [ANGABE]
- Größenklasse nach Handelsrecht: [kleinst / klein / mittelgroß / groß]
- Abschlussstichtag: [STICHTAG], Wirtschaftsjahr: [ZEITRAUM]
- Vereinbarte Auftragsart: [ohne Beurteilungen / mit Plausibilitätsbeurteilungen
  / mit umfassenden Beurteilungen / nicht schriftlich vereinbart]
- Auftragsvereinbarung liegt schriftlich vor: [ja / nein], Datum: [DATUM]
- Auftragsart des Vorjahres: [ANGABE]
- Erklärung der gesetzlichen Vertreter zur Fortführungsabsicht:
  [liegt vor / liegt nicht vor / mündlich], Datum: [DATUM]
- Bisherige Hinweise der Kanzlei: [dokumentiert / mündlich / keine],
  Datum: [DATUM]

GEGEBENHEITEN – jede Zeile ausfüllen oder "unbekannt" eintragen. Trage nur
objektive Angaben ein, keine Wertungen.
- Nicht durch Eigenkapital gedeckter Fehlbetrag: [BETRAG] zum [STICHTAG]
- Jahresergebnisse der letzten drei Jahre: [BETRÄGE]
- Eigenkapital und Gesellschafterdarlehen: [BETRÄGE],
  Rangrücktritt: [vorhanden / nicht vorhanden / unbekannt]
- Kapitaldienst gegenüber erwirtschaftetem Überschuss: [BETRÄGE]
- Kreditlinien: [unverändert / reduziert / gekündigt], Datum: [DATUM]
- Zahlungsmodalitäten der Lieferanten: [unverändert / Vorkasse / Lieferstopp /
  Mahnbescheide]
- Rückstände bei Steuern: [nein / ja], Betrag: [BETRAG], seit: [DATUM]
- Rückstände bei Sozialversicherungsbeiträgen insgesamt: [nein / ja / unbekannt],
  seit: [DATUM]. Der Beitrag wird als Gesamtsozialversicherungsbeitrag
  geschuldet; eine Aufteilung wird hier nicht abgefragt. Ob Arbeitnehmeranteile
  nicht abgeführt wurden, klärt der Berufsträger vor dem Werkzeugeinsatz
  außerhalb des Werkzeugs und vermerkt das Ergebnis in der Handakte.
- Insolvenzantrag gestellt oder angekündigt: [nein / ja / unbekannt]
- Bericht der gesetzlichen Vertreter über einen eingetretenen Insolvenzgrund
  oder eine Antragspflicht: [nein / ja / unbekannt]
- Wegfall wesentlicher Kunden, Aufträge oder Lieferanten: [nein / ja], [ANGABE]
- Gekündigte oder auslaufende Verträge von wesentlicher Bedeutung
  (Miete, Pacht, Lizenz, Finanzierung): [nein / ja], [ANGABE]
- Rechtliche Gegebenheiten (Gesellschafterstreit, Kündigung eines
  Beherrschungs- oder Ergebnisabführungsvertrags, behördliche Untersagung,
  Wegfall einer Erlaubnis): [nein / ja], [ANGABE]
- Ereignisse nach dem Stichtag bis heute: [ANGABE]
- Stützende Unterlagen, die vorliegen: [Planungsrechnung / Finanzierungszusage /
  Rangrücktritt / Patronatserklärung / Gesellschafterbeschluss / keine],
  jeweils Datum: [DATUM]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Auftragsart. Bestimme sie zuerst – sie trägt alle weiteren Schritte, weil sie
   festlegt, welche Erkenntnisquellen der Auftrag umfasst und welchen Inhalt
   eine Bescheinigung haben kann. Ordne den Auftrag einer der drei Auftragsarten
   der Verlautbarung der Bundessteuerberaterkammer zu:
   a) Erstellung ohne Beurteilungen,
   b) Erstellung mit Plausibilitätsbeurteilungen,
   c) Erstellung mit umfassenden Beurteilungen.
   Sage je Auftragsart in zwei Sätzen, welche Erkenntnisse sie verlangt und
   welche Erwartung der Mandant an das Ergebnis haben darf. Ist die Auftragsart
   nicht schriftlich vereinbart, sage ausdrücklich: "Auftragsart vor der
   Fertigstellung schriftlich zu vereinbaren" und arbeite hilfsweise mit der
   Auftragsart des Vorjahres unter ausdrücklich benannter Annahme weiter.
   (Auftragsarten und ihre Anforderungen – für [JAHR] verifizieren.)
2. Verantwortungsverteilung. Halte fest, dass die Aufstellung des Abschlusses
   und die Einschätzung der Fortführung Sache der gesetzlichen Vertreter sind
   und dass der Steuerberater diese Einschätzung entgegennimmt und würdigt.
   Benenne die Erklärung der gesetzlichen Vertreter als eigenständige Unterlage
   und sage, was fehlt, wenn sie nicht vorliegt.
3. Fortführungsannahme dem Grunde nach. Benenne, dass bei der Bewertung von der
   Fortführung der Unternehmenstätigkeit auszugehen ist, sofern dem nicht
   tatsächliche oder rechtliche Gegebenheiten entgegenstehen, und dass die
   Fortführungsbewertung aufzugeben ist, sobald solche Gegebenheiten
   entgegenstehen – das ist kein Wahlrecht
   (§ 252 Abs. 1 Nr. 2 HGB – für [JAHR] verifizieren). Benenne ergänzend, dass
   von den Bewertungsgrundsätzen des Absatzes 1 nur in begründeten
   Ausnahmefällen abgewichen werden darf
   (§ 252 Abs. 2 HGB – für [JAHR] verifizieren). Ob Gegebenheiten
   entgegenstehen, beurteilst du nicht.
4. Gegebenheiten einzeln einordnen. Lege je gelieferter Zeile eine eigene Zeile
   an mit: Angabe, Zeitpunkt, Einordnung als (Gegebenheit liegt nach den Angaben
   vor), (Angabe liegt vor, Gegebenheit nach den Angaben nicht erkennbar) oder
   (Angabe fehlt). Bewerte nicht, ob eine Angabe auffällig ist. Keine
   Gesamtnote, keine Ampel, keine Rangfolge, keine Wahrscheinlichkeitsaussage.
   Formuliere jede Ursachenaussage ausdrücklich als Vermutung, solange sie nicht
   aus den Angaben folgt.
5. Stützende Gegebenheiten und ihre Belastbarkeit. Ordne je stützender Unterlage
   zu: Art, Datum, wer sie abgegeben hat, bis wann sie trägt und welche
   Nachweise dafür fehlen. Behandle eine mündliche Zusage ausdrücklich als
   fehlenden Nachweis. Bewerte NICHT, ob die Fortführung damit gesichert ist.
6. Auswirkung auf den Abschluss, nur dem Grunde nach dargestellt. Sage, welche
   Folgen es für Ansatz und Bewertung hätte, wenn nicht mehr von der Fortführung
   auszugehen wäre, und welche Angabepflichten dann in Betracht kommen
   (Fundstellen – für [JAHR] verifizieren). Rechne keinen Wert um und schlage
   keine Umbewertung vor.
7. Folge für die Bescheinigung, als Entscheidungsvorlage und nicht als
   Entscheidung. Stelle die dreistufige Folge der Hinweise der
   Bundessteuerberaterkammer dar:
   a) Bescheinigung mit Ergänzung,
   b) Bescheinigung mit Einwendung,
   c) keine Bescheinigung und Niederlegung des Auftrags.
   Stelle je Stufe dar, welche Angabe oder Unterlage sie voraussetzt und ob
   diese nach den gelieferten Angaben vorliegt, fehlt oder unbekannt ist. Sage
   NICHT, ob eine Voraussetzung erfüllt ist – das ist die Entscheidung selbst.
   Schließe mit dem Satz: "Ob eine Voraussetzung erfüllt ist und welche Stufe
   gewählt wird, entscheidet der Berufsträger."
   (Stufenfolge und Fundstelle – für [JAHR] verifizieren.)
8. Hinweis- und Warnpflicht. Benenne die eigene Hinweis- und Warnpflicht des
   Beraters bei der Erstellung eines Jahresabschlusses: Sie besteht, wenn
   Anhaltspunkte für einen Insolvenzgrund nach den §§ 17 bis 19 InsO offenkundig
   sind und anzunehmen ist, dass dem Mandanten die mögliche Insolvenzreife nicht
   bewusst ist (§ 102 StaRUG – für [JAHR] verifizieren). Ob diese
   Voraussetzungen vorliegen, beurteilst du nicht. Erzeuge KEINEN Hinweistext;
   verweise auf den dafür vorgesehenen Arbeitsschritt und halte fest, ob ein
   Hinweis nach den Angaben bereits dokumentiert ist.
9. Dokumentation. Liste auf, was vor der Fertigstellung in der Handakte liegen
   muss: schriftliche Auftragsvereinbarung mit Auftragsart, Erklärung der
   gesetzlichen Vertreter, stützende Unterlagen, Vermerk über die gewürdigten
   Gegebenheiten, Datum und Form jedes Hinweises. Markiere je Position
   (liegt vor) oder (fehlt).

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Benenne fehlende Angaben
   einzeln, arbeite mit ausdrücklich benannten Annahmen und erfinde keine Zahlen.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV, also Norm mit
   Absatz und Satz, Verlautbarung oder Hinweise mit Bezeichnung und Fassung oder
   Entscheidung mit Datum und Aktenzeichen, jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen, keine Beschlüsse und
   keine Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Nenne KEINE Betragsgrenze, KEINE Kennzahlenschwelle und KEINEN Zeitraum als
   feststehenden Wert. Jede solche Größe nur als nachzuschlagende Angabe mit dem
   Zusatz "für [JAHR] verifizieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE Fristen im Raum stehen, je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und ohne
   Dauer. Ergänze bei jeder: "Frist von einem Menschen zu berechnen und im
   Fristenprogramm zu erfassen."
5. Trenne durchgehend zwischen dem, was aus den Angaben folgt, und dem, was eine
   Beurteilung wäre. Eine Beurteilung gibst du nicht ab.
6. AUSSTEUERUNGSREGEL – kein Abbruch, an objektiven Angaben. Steuere einen
   Einzelpunkt aus, wenn die dafür vorgesehene Zeile des Sachverhaltsbogens es
   sagt:
   (a) im Feld "Insolvenzantrag gestellt oder angekündigt" steht "ja",
   (b) im Feld "Bericht der gesetzlichen Vertreter über einen eingetretenen
       Insolvenzgrund oder eine Antragspflicht" steht "ja".
   Gib für den ausgesteuerten Einzelpunkt nur aus: "Ausgesteuert – Prüfung durch
   einen Berufsträger außerhalb des KI-Werkzeugs." Beende die Bearbeitung
   NICHT; arbeite die übrigen Schritte weiter und führe die ausgesteuerten
   Punkte im Arbeitspapier gesondert auf.

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit"
2. "Auftragsart und ihre Folgen"
3. "Verantwortungsverteilung und Erklärung der gesetzlichen Vertreter"
4. "Fortführungsannahme dem Grunde nach" mit Rechtsgrundlage
5. "Raster der Gegebenheiten": Angabe | Zeitpunkt | Einordnung | Bemerkung
6. "Stützende Gegebenheiten": Unterlage | Datum | Reichweite | fehlender Nachweis
7. "Auswirkung auf Ansatz und Bewertung, nur dem Grunde nach"
8. "Entscheidungsvorlage Bescheinigung" nach Schritt 7
9. "Hinweis- und Warnpflicht: Stand der Dokumentation"
10. "Fristarten, die im Raum stehen"
11. "Unterlagen- und Dokumentationsliste" mit (liegt vor) oder (fehlt)
12. "Arbeitspapier für die Handakte (Entwurf)", höchstens 300 Wörter
13. "Ausgesteuerte Punkte"
14. "Interne Notiz"
15. "Was ich nicht sicher weiß"
```

## Anwendung

1. Vor dem Prompt die Auftragsvereinbarung heraussuchen und die Auftragsart feststellen. Ist sie nicht schriftlich vereinbart, ist das der erste Befund und vor der Fertigstellung des Abschlusses zu heilen – nicht danach.
2. Die Gegebenheiten aus Bilanz, betriebswirtschaftlicher Auswertung, Kennzahlenanalyse und Frühwarnservice als objektive Angaben aufnehmen und auf Kürzel umstellen. Wertungen gehören nicht in den Eingabeblock.
3. Die Erklärung der gesetzlichen Vertreter zur Fortführungsabsicht schriftlich anfordern, mit Datum zur Akte nehmen und im Prompt als vorliegend oder fehlend führen. Sie ersetzt die eigene Würdigung nicht, aber ohne sie fehlt die Grundlage.
4. Das Ergebnis als Entscheidungsvorlage behandeln: Die Wahl zwischen Bescheinigung mit Ergänzung, Bescheinigung mit Einwendung und Niederlegung des Auftrags trifft der Berufsträger und begründet sie im Arbeitspapier.
5. Steht ein Insolvenzgrund im Raum: Ob er vorliegt, prüft weder dieser noch ein anderer Prompt dieser Sammlung; diese Prüfung ist Rechtsdienstleistung und gehört zu einem Insolvenzrechtler. Prompt 74 bereitet dafür nur die Datenanforderung und das leere Statusgerüst auf, Prompt 65 den Hinweis an den Mandanten samt Handaktenvermerk. Dieser Prompt ersetzt beides nicht.
6. Auftragsart, Gegebenheitenraster und Arbeitspapier im Dokumentenmanagement ablegen und mit Wiedervorlage versehen; Fundstellen der Verlautbarung und der Hinweise vor der Verwendung am Original prüfen (Fassung – für [JAHR] verifizieren).

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf und eine Entscheidungsvorlage.** Vor der Verwendung prüfen: Auftragsart, Vollständigkeit des Gegebenheitenrasters, Belastbarkeit der stützenden Unterlagen, Datum jeder Erklärung.
- **Jede Beurteilung streichen.** Aussagen zu Zahlungsunfähigkeit, Überschuldung, Insolvenzreife oder Antragspflicht – auch entlastende – ersatzlos entfernen. Diese Prüfung nimmt ein Insolvenzrechtler vor, nicht die Kanzlei und kein Prompt dieser Sammlung.
- **Keine IDW-Verlautbarung im Text.** Für den Steuerberater ist die Verlautbarung der Bundessteuerberaterkammer zu den Grundsätzen für die Erstellung von Jahresabschlüssen einschlägig; jede Bezugnahme auf eine IDW-Verlautbarung (IDW S, IDW PS, Praxishinweis) und jede Textziffer daraus ist zu löschen.
- **Auftragsart schriftlich.** Ohne schriftlich vereinbarte Auftragsart lässt sich im Regressfall nicht belegen, welchen Erkenntnisumfang der Auftrag hatte. Die Vereinbarung wird vor der Fertigstellung nachgeholt, nicht rückdatiert.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person nimmt das Gegebenheitenraster gegen die Auswertungen nach. Über Fortführungsannahme, Auftragsart und Inhalt der Bescheinigung entscheidet ausnahmslos ein Berufsträger; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`). Fristen berechnet und erfasst ein Mensch.
- **Rückstände bei Arbeitnehmeranteilen berühren die Zone Rot in `DATENSCHUTZ.md`** (Strafsachverhalt) und gehören nicht in ein KI-Werkzeug. Der Sachverhaltsbogen fragt deshalb nur den Beitragsrückstand insgesamt ab; der Beitrag wird nach § 28e Abs. 1 SGB IV als Gesamtsozialversicherungsbeitrag geschuldet, eine Aufteilung in Arbeitgeber- und Arbeitnehmeranteil gibt es weder in der Zahlung noch in diesem Prompt (Fundstelle – für [JAHR] verifizieren).
- **Rechtsstand prüfen an:** § 252 Abs. 1 Nr. 2 und Abs. 2 HGB sowie § 102 StaRUG im amtlichen Volltext (gesetze-im-internet.de); der Verlautbarung der Bundessteuerberaterkammer zu den Grundsätzen für die Erstellung von Jahresabschlüssen in der Fassung des Beschlusses der Bundeskammerversammlung vom 28./29.03.2022; den Hinweisen der Bundessteuerberaterkammer zur Unternehmensfortführung (Präsidiumsbeschluss vom 07.09.2021) mit der Stufenfolge Bescheinigung mit Ergänzung, Bescheinigung mit Einwendung sowie keine Bescheinigung und Niederlegung des Auftrags; sowie DATEV LEXinform. Fassung und Fundstelle jeweils am Original nachlesen (Stand – für [JAHR] verifizieren).

## Varianten

- **Nur Auftragsartklärung:** „Beschränke dich auf Schritt 1 und 2 und erzeuge zusätzlich den Entwurf einer Ergänzung zur Auftragsvereinbarung, in der die Auftragsart schriftlich festgelegt wird."
- **Erklärung der gesetzlichen Vertreter:** „Erzeuge ausschließlich den Entwurf einer Erklärung der gesetzlichen Vertreter zur Fortführungsabsicht mit Leerfeldern für Datum, Unterschrift und die zugrunde gelegten Unterlagen – ohne eigene Würdigung."
- **Folgejahr:** „Vergleiche die Angaben mit denen des Vorjahres, benenne jede Veränderung und sage, welche Gegebenheit erstmals vorliegt und welche entfallen ist."
- **Abschlussgespräch:** „Leite aus dem Raster höchstens acht Fragen für das Abschlussgespräch mit der Geschäftsführung ab, je mit der Unterlage, die zur Beantwortung vorzulegen ist."
- **Anschluss:** Datenaufbereitung für den Insolvenzrechtler Prompt 74, Hinweisschreiben und Handaktenvermerk Prompt 65, Zahlengrundlage Prompt 66.
