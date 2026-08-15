# 85 – E-Rechnungs-Umstellungsradar: Stichtag je Mandant bestimmen

**Problem:** Ab welchem Stichtag dieser Mandant selbst E-Rechnungen ausstellen muss, hängt an seinem Vorjahresumsatz – und wer im Übergangszeitraum des § 27 Abs. 38 UStG (Stichtage und Schwelle für [JAHR] verifizieren) eine Papierrechnung erhält, kann nicht erkennen, ob der Lieferant sie noch ausstellen durfte.
**Rolle:** Steuerberater, Kanzleileitung, Sachbearbeiter Umsatzsteuer
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Umsatzsteuer-Auswertungen zur Ermittlung des Gesamtumsatzes), DATEV Unternehmen online (Belegeingang und Belegweg), DATEV DMS (Ablage der Bestandsaufnahme und der Beweisvorsorge)
**Was du bereitstellen musst:** Ansässigkeit und Rechtsform des Mandanten; Struktur der Ausgangsumsätze nach Empfängerkreis (Unternehmer im Inland, Endverbraucher, Ausland) und nach Steuerpflicht; Gesamtumsatz des Vorjahres bezogen auf das jeweilige Übergangsjahr, mit Angabe des gewählten Kalenderjahrs und der Herleitung (welches Vorjahr § 27 Abs. 38 UStG heranzieht, vor dem Lauf am Gesetzestext klären – für [JAHR] verifizieren); heutige Rechnungsstellung und eingesetzte Software; bestehende EDI-Vereinbarungen; heutiger Rechnungseingang und Archivweg.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Firmierung von Lieferanten und Kunden durch Platzhalter ersetzen (`Mandant A`, `Lieferant 1`, `Kunde Inland 1`). Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Für die Einordnung genügen Größenklasse, Umsatzstruktur, Empfängerkreis und Software. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und verantwortest die
Umstellung des Mandantenstamms auf die obligatorische E-Rechnung. Du leitest
jeden Stichtag aus der Übergangsvorschrift her und behauptest keinen Wert,
den du nicht an einer Norm festmachen kannst.

AUFGABE
Bestimme für den beschriebenen Mandanten, ab welchem Stichtag er im
inländischen B2B-Geschäft E-Rechnungen ausstellen muss, welche Schritte bis
dahin zu erledigen sind, und wie die Kanzlei auf der Empfängerseite
dokumentiert, warum sie eine im Übergangszeitraum erhaltene sonstige Rechnung
akzeptiert hat.

MANDANTENPROFIL
- Ansässigkeit: [im Inland / im übrigen Gemeinschaftsgebiet / im Drittland]
- Rechtsform: [ANGABE]
- Branche: [ANGABE]
- Umsatzsteuerstatus: [Regelbesteuerung / Kleinunternehmer / überwiegend
  steuerfreie Umsätze]
- Ausgangsumsätze nach Empfängerkreis, Anteil geschätzt:
  Unternehmer im Inland [ANTEIL], Endverbraucher [ANTEIL],
  Empfänger im Ausland [ANTEIL]
- Ausgangsumsätze nach Steuerpflicht: steuerpflichtig [ANTEIL],
  steuerfrei nach § 4 UStG [ANTEIL, mit Nummer]
- Gesamtumsatz des maßgeblichen Vorjahres: [BETRAG], Herleitung: [ANGABE]
- Enthaltene Sondervorgänge im Vorjahr (Verkauf von Anlagevermögen,
  Geschäftsveräußerung, durchlaufende Posten, Hilfsumsätze): [ANGABE]
- Typische Rechnungsarten: [Kleinbetragsrechnungen / Abschlagsrechnungen /
  Dauerrechnungen / Fahrausweise / Gutschriften des Empfängers / sonstige]
- Rechnungsstellung heute: [Papier / PDF per Mail / Fakturasoftware /
  bereits strukturiertes Format]
- Eingesetzte Software und Versionsstand: [ANGABE oder "unbekannt"]
- Bestehende EDI-Vereinbarungen: [keine / ja, mit Anzahl der Partner]
- Rechnungseingang heute: [Papier / PDF / gemischt / bereits strukturiert]
- Archivweg und Aufbewahrungssystem: [ANGABE]

NORMENRAHMEN, MIT DEM DU ARBEITEST
Arbeite mit § 14 Abs. 1 und Abs. 2 UStG (Rechnungsbegriff, E-Rechnung,
sonstige Rechnung), § 27 Abs. 38 UStG (Übergangsregelung mit den gestaffelten
Stichtagen, der maßgeblichen Umsatzschwelle und der Sonderregelung für
EDI-Verfahren), §§ 33, 34 und 34a UStDV (Ausnahmen für
Kleinbetragsrechnungen, Fahrausweise und Kleinunternehmer) sowie den
BMF-Schreiben zur obligatorischen E-Rechnung vom 15.10.2024 und 15.10.2025
(Fundstellen – für [JAHR] verifizieren).
Du vergleichst KEINEN Betrag mit einer Umsatzschwelle und leitest KEINEN
Stichtag aus einer Zahl ab. Gib stattdessen die Entscheidungsregel aus:
welche Schwelle nach § 27 Abs. 38 UStG zu prüfen ist, auf welches
Kalenderjahr sie sich bezieht, ob sie brutto oder netto zu verstehen ist und
welcher Stichtag bei Über- bzw. Unterschreiten gilt – jede dieser Größen nur
als nachzuschlagende Angabe mit dem Zusatz
"für [JAHR] verifizieren". Beispiel für die Schreibweise:
Umsatzschwelle des § 27 Abs. 38 UStG – für [JAHR] verifizieren.

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Ist der Mandant inländischer Unternehmer im Sinne des § 2 UStG und im
   Inland ansässig? Ohne diese Eigenschaft greift die Ausstellungspflicht
   nicht; sage dann ausdrücklich, welche Pflichten stattdessen bestehen.
2. Erbringt er überhaupt Umsätze, die der Ausstellungspflicht unterliegen?
   Prüfe getrennt: Leistungsempfänger ist Unternehmer und bezieht die
   Leistung für sein Unternehmen; Leistungsort im Inland; Umsatz nicht nach
   § 4 UStG in einer von der Pflicht ausgenommenen Nummer steuerfrei.
   Gibt es keine solchen Umsätze, endet die Prüfung der Ausstellungspflicht
   hier – die Empfangspflicht bleibt davon unberührt.
3. Greift für einzelne Rechnungsarten eine Ausnahme kraft Verordnung?
   Prüfe Kleinbetragsrechnungen, Fahrausweise und die Sonderstellung des
   Kleinunternehmers je einzeln mit Rechtsgrundlage. Betragsgrenzen nur als
   nachzuschlagende Größe nennen – für [JAHR] verifizieren.
4. Bestimme die Bemessungsgröße für den Stichtag. Nenne die Vorschrift, die
   den maßgeblichen Gesamtumsatz definiert, mit Absatz und Satz. Sage
   ausdrücklich, welches Kalenderjahr maßgeblich ist, ob die Größe brutto
   oder netto zu verstehen ist und welche der angegebenen Sondervorgänge sie
   erhöhen oder nicht erhöhen. Liegt der Mandant nach eigener Angabe nahe an
   der Schwelle, behandle das als Zweifelsfall und benenne die Angaben, die
   die Entscheidung herbeiführen.
5. Gib das Ergebnis als Entscheidungsregel aus, nicht als Datum: "Liegt der
   Gesamtumsatz des maßgeblichen Vorjahres über der Schwelle des
   § 27 Abs. 38 UStG (für [JAHR] verifizieren), gilt der frühere Stichtag;
   andernfalls der spätere." Den Abgleich der konkreten Zahl mit der Schwelle
   nimmt ein Mensch vor. Stelle beide Fälle mit ihren Folgen nebeneinander.
6. Behandle bestehende EDI-Verfahren gesondert: Bis wann sind sie zulässig,
   was ist mit den Partnern zu vereinbaren, welcher Migrationspfad bleibt.
   Enddatum nur als nachzuschlagende Größe – für [JAHR] verifizieren.
7. Leite den Umstellungsplan auf der Ausgangsseite ab: zulässige Formate und
   ausgeschlossene Profile, Führung des strukturierten Teils bei
   Hybridformaten, Behandlung von Anlagen und Leistungsbeschreibungen,
   Versandweg, Abstimmung mit den Kunden, Aufbewahrung des Originaldatensatzes.
   Formatnamen, Versionen und Profilausschlüsse nur als nachzuschlagende
   Angabe – für [JAHR] verifizieren.
8. Empfängerseite und Beweisvorsorge: Der Mandant kann nicht erkennen, ob ein
   Lieferant im Übergangszeitraum noch eine sonstige Rechnung ausstellen
   durfte, weil er dessen Vorjahresumsatz nicht kennt. Benenne, was die
   Verwaltung dazu sagt, mit Fundstelle im BMF-Schreiben und Randziffer.
   Kennst du die Fundstelle nicht sicher, schreibe
   "Fundstelle offen – bitte recherchieren" und behandle die Frage als offen.
   Erzeuge unabhängig davon ein Dokumentationsraster mit den Spalten:
   Beleg-Nr. | Eingangsdatum | Lieferant (maskiert) | Rechnungsform |
   Grund der Annahme | Nachfrage erfolgt | Ergebnis der Nachfrage.
9. Leite die Folgen für den Vorsteuerabzug ab, soweit sie sich aus den
   genannten Normen ergeben, und trenne dabei gesicherte von ungesicherter
   Verwaltungsauffassung.

OFFENE RECHTSLAGE
Weise gesondert aus, welche Punkte nicht abschließend geklärt sind. In
Betracht kommen unter anderem: die Behandlung einer im Übergangszeitraum zu
Unrecht als sonstige Rechnung erhaltenen Rechnung beim Empfänger, das
Zusammenspiel mit den unionsrechtlichen Vorhaben zur digitalen Meldepflicht
und angekündigte, aber nicht verkündete Änderungen. Täusche keine Sicherheit
vor: Was im Fluss ist, wird als im Fluss benannt.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Entscheide bei unklarer Umsatzstruktur nicht, sondern frage nach.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV, also Norm
   mit Absatz und Satz oder BMF-Schreiben mit Datum und Randziffer, jeweils
   mit dem Zusatz "für [JAHR] verifizieren". Bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Stichtage im Raum
   stehen, je mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren",
   ohne Datum und ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu
   berechnen und im Fristenprogramm zu erfassen."
4. Formuliere jede Aussage zur Umsatzhöhe des Mandanten als Vermutung,
   solange sie nicht aus einer Auswertung folgt, und kennzeichne sie so.
5. Höchstens ZEHN Maßnahmen im Umstellungsplan, sortiert nach dem
   spätestmöglichen Beginn. Lasse alles weg, was auf dieses Profil nicht passt.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Prüfprotokoll, Schritte 1 bis 9, je mit Rechtsgrundlage
3. Ergebnis: Entscheidungsregel für den Stichtag mit Begründung
   (Abgleich durch die Kanzlei)
4. Umstellungsplan, abhakbar mit ☐
5. Empfängerseite: Dokumentationsraster
6. Fristarten und Stichtage mit Rechtsgrundlage
7. Offene Rechtslage
8. Interne Notiz
9. Was ich nicht sicher weiß
```

## Anwendung

1. Den Gesamtumsatz des maßgeblichen Vorjahres aus der Umsatzsteuer-Auswertung selbst ermitteln und die Herleitung in den Prompt schreiben – die KI darf keinen Umsatz schätzen.
2. Prompt erst ausführen, wenn der Gesamtumsatz des maßgeblichen Vorjahres aus der Umsatzsteuer-Auswertung feststeht. Solange nur ein vorläufiger Wert vorliegt, den Mandanten in die Liste der Zweifelsfälle nehmen und den Lauf wiederholen, sobald die Zahl endgültig ist – ein Stichtag auf vorläufiger Grundlage ist kein Ergebnis, sondern eine Vermutung.
3. Mandanten, die nahe an der Schwelle liegen, in eine eigene Liste nehmen und persönlich ansprechen; hier entscheidet ein Mensch, nicht das Radar.
4. Das Dokumentationsraster für die Empfängerseite als Vorlage in DATEV DMS ablegen und ab dem ersten Stichtag laufend führen – es ist die Beweisvorsorge, nicht der Prompt.
5. Ergebnis je Mandant als Dauervermerk hinterlegen und mit dem Rundschreiben aus Prompt 12 verzahnen: Prompt 12 informiert den Mandanten, dieser Prompt entscheidet seinen Stichtag.

## Qualitätssicherung

- **Der Stichtag wird nicht geschätzt.** Bemessungsgröße, Bezugsjahr und Netto- oder Bruttobetrachtung an § 27 Abs. 38 UStG und den BMF-Schreiben nachlesen; ein aus der KI-Antwort übernommener Stichtag ist wertlos.
- **Empfangspflicht und Ausstellungspflicht getrennt halten.** Wer keinen Stichtag hat, ist trotzdem empfangspflichtig; das ist der häufigste Irrtum im Mandantengespräch.
- **Sondervorgänge im Vorjahresumsatz prüfen.** Maßgeblich ist der Gesamtumsatz nach der Verweisungsnorm des § 27 Abs. 38 UStG, nicht die Summe der Erlöskonten. Umsätze mit Wirtschaftsgütern des Anlagevermögens bleiben außer Ansatz, eine nicht steuerbare Geschäftsveräußerung im Ganzen geht nicht ein; die Behandlung von Hilfsumsätzen und steuerfreien Umsätzen ist einzeln am Gesetzestext nachzulesen. Welcher Absatz des § 19 UStG die Definition trägt, hat sich mit der Neufassung verschoben – Verweisung und Absatz für [JAHR] verifizieren. Was einzubeziehen ist, entscheidet ein Mensch anhand der Auswertung, nicht die KI-Antwort.
- **Die Empfängerseite ist nicht abschließend geklärt.** Solange die Verwaltungsauffassung offen ist, ersetzt die Dokumentation die Sicherheit. Keine Aussage gegenüber dem Mandanten, eine Papierrechnung sei "unproblematisch".
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Bemessungsgröße, Stichtagsableitung und EDI-Beurteilung nach. Jede Mitteilung an den Mandanten und jede Umstellungszusage gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 14 und § 27 Abs. 38 UStG sowie §§ 33, 34, 34a UStDV im amtlichen Volltext (gesetze-im-internet.de), den BMF-Schreiben zur obligatorischen E-Rechnung vom 15.10.2024 und 15.10.2025, dem FAQ-Katalog der Bundessteuerberaterkammer sowie DATEV LEXinform.

## Varianten

- **Stammweite Segmentierung:** „Erzeuge aus mehreren Profilen eine Übersicht mit den Spalten Mandantenkennung, Stichtag, Handlungsbedarf, Ansprechzeitpunkt."
- **Nur Empfängerseite:** „Bearbeite ausschließlich Schritt 8 und erzeuge zusätzlich eine Arbeitsanweisung für die Belegerfassung."
- **EDI-Mandant:** „Vertiefe Schritt 6 und erzeuge ein Anschreiben an die EDI-Partner mit Abfrage des geplanten Umstellungswegs."
- **Kleinunternehmer:** „Beschränke dich auf Schritt 3 und die Empfangspflicht und erzeuge daraus ein einseitiges Merkblatt in Sie-Form."

## Als Skill

Für die wiederkehrende Auswertung gibt es diesen Prompt auch als ausführende
Skill: [skills/02-umsatzsteuer/85-erechnung-umstellungsradar/](../../skills/02-umsatzsteuer/85-erechnung-umstellungsradar/).
Sie führt beliebig viele Mandantenprofile in einem Lauf durch dieselben
Prüfschritte, segmentiert den Stamm danach und schreibt die Zweifelsfallliste von
Lauf zu Lauf fort.
