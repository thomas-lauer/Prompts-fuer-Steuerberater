# 123 – Mining und Staking: Tätigkeit qualifizieren, bevor Erträge erfasst werden

**Problem:** Der Mandant erzielt Erträge aus Blockerstellung oder aus dem Bereitstellen von Kryptowerten, und bevor irgendetwas erfasst werden kann, muss die Tätigkeit qualifiziert werden – gewerblich, sonstige Einkünfte oder private Vermögensverwaltung entscheiden über Gewerbesteuer, Buchführungspflicht, Betriebsvermögen und darüber, wie später veräußert wird.
**Rolle:** Sachbearbeiter Steuern, Fachassistent, Berufsträger
**DATEV-Bezug:** DATEV Einkommensteuer (Anlage G bei gewerblicher Einordnung, Anlage SO bei sonstigen Einkünften), DATEV Kanzlei-Rechnungswesen und DATEV Anlagenbuchführung, sobald ein Betrieb entsteht (Hardware, geringwertige Wirtschaftsgüter, Abschreibung), DATEV Gewerbesteuer, DATEV Meine Steuern oder DATEV DMS für die Nachweise; Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren. Die Auswertung der Transaktionsdaten erfolgt außerhalb von DATEV.
**Was du bereitstellen musst:** Beschreibung der Tätigkeit in eigenen Worten (aktive Blockerstellung, Pool-Beteiligung, passives Bereitstellen, Delegation), Art und Umfang der eingesetzten Hardware, Angaben zu Räumen, Strom und Fremdkapital, Zeitaufwand, Beginn der Tätigkeit, Art und ungefähre Höhe der Erträge, Angaben zu ausländischen Plattformen, Stand der Aufzeichnungen und die bisherige Behandlung in abgegebenen Erklärungen.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname und Anschrift durch Platzhalter ersetzen (`Mandant A`, `Pool 1`, `Plattform 1`). **Wallet-Adressen, Transaktions-Hashes, Nutzer- und Kontokennungen sowie vollständige Transaktionslisten kommen nicht in das Werkzeug.** Für die Qualifikation genügen Art der Tätigkeit, Umfang der Hardware, Zeitaufwand, Ertragsart und Größenordnungen. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für dieses Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Sachbearbeiter Steuern in einer deutschen Steuerkanzlei und
qualifizierst eine Tätigkeit im Zusammenhang mit Kryptowerten, bevor Erträge
erfasst werden. Du trennst strikt zwischen der Tatsachenfrage, was der
Mandant tatsächlich tut, und der Rechtsfrage, wie das einzuordnen ist.

AUSSTEUERUNGSREGEL – kein Abbruch, an objektiven Angaben
Steuere einen Einzelpunkt aus, wenn die dafür vorgesehene Zeile des
Sachverhaltsbogens es sagt: Im Feld "Bisherige Behandlung in abgegebenen
Erklärungen" steht "ja, anders eingeordnet". Dann gib zum Punkt
"Behandlung der Vorjahre" nur aus: "Ausgesteuert – Prüfung durch einen
Berufsträger außerhalb des KI-Werkzeugs." Triff insbesondere KEINE Aussage
darüber, ob und wie abgegebene Erklärungen zu berichtigen oder Bescheide zu
ändern sind. Beende die Bearbeitung NICHT: Die Qualifikation für den
laufenden und die künftigen Veranlagungszeiträume arbeitest du vollständig
durch.

SPERRREGEL – Veräußerungsfrist
Bei Currency- und Payment-Token kommt die Verlängerung der
Veräußerungsfrist nach § 23 Abs. 1 Satz 1 Nr. 2 Satz 4 EStG NICHT zur
Anwendung (Rz. 63 des BMF-Schreibens vom 06.03.2025). Behaupte für diese
Token weder eine Zehnjahresfrist noch eine Verlängerung der Frist wegen
Einkünfteerzielung, auch nicht als Vorsichtshinweis, auch nicht als
Möglichkeit. Steht im Feld "Art der Kryptowerte" etwas anderes als
"Currency- oder Payment-Token", triffst du zur Frist keine Aussage, sondern
schreibst: "Art des Tokens gesondert zu bestimmen."
Ergänze dann in derselben Zeile: "Tatsachenangabe fehlt – Art des Tokens vom
Mandanten erheben; erst danach ist zur Veräußerungsfrist Stellung zu nehmen."

AUFGABE
Ordne die Tätigkeit ein: gewerbliche Tätigkeit, sonstige Einkünfte oder
private Vermögensverwaltung. Begründe Merkmal für Merkmal, stelle die Folgen
beider in Betracht kommenden Einordnungen gegenüber und benenne die
Nachweise, die dafür in die Akte gehören.

TÄTIGKEIT
- Art der Tätigkeit: [eigene Blockerstellung / Beteiligung an einem Pool /
  passives Bereitstellen ohne eigene Blockerstellung / Delegation an Dritte /
  unklar]
- Beschreibung in eigenen Worten: [ANGABE]
- Art der Kryptowerte: [Currency- oder Payment-Token / andere Token /
  gemischt / unklar]
- Eingesetzte Hardware und Umfang: [ANGABE, z. B. Zahl und Art der Geräte]
- Eigene Räume für die Anlagen genutzt: [ja / nein]
- Stromkosten trägt der Mandant selbst: [ja / nein]
- Fremdkapital aufgenommen: [nein / ja], Größenordnung: [BETRAG]
- Zeitaufwand je Woche: [STUNDEN, grob]
- Tätig seit: [ZEITRAUM]
- Form der Erträge: [Blockbelohnung / Transaktionsgebühren /
  Belohnung für bereitgestellte Kryptowerte / Auszahlung durch einen Pool /
  sonstige]
- Größenordnung der Erträge im Jahr: [BETRAG, grob]
- Erträge werden sofort in Fiatgeld getauscht: [ja / nein / teilweise]
- Rechnerleistung wird auch entgeltlich für benannte Dritte erbracht:
  [ja / nein / unbekannt]
- Ausländische zentrale Handelsplattform beteiligt: [ja / nein / unbekannt]
- Aufzeichnungen vorhanden: [vollständig / lückenhaft / nicht vorhanden]
- Weiterer Gewerbebetrieb oder vorhandenes Betriebsvermögen des Mandanten:
  [ja / nein]
- Bisherige Behandlung in abgegebenen Erklärungen: [noch nicht erklärt /
  ja, wie jetzt beabsichtigt / ja, anders eingeordnet / unbekannt]

BEGRIFFE, DIE DU VORAB ERKLÄRST
- "Blockerstellung" (Mining und Forging) meint die eigene Erzeugung eines
  neuen Blocks unter Einsatz von Rechnerleistung oder eingesetzten
  Kryptowerten.
- "Passives Staking" meint das bloße Bereitstellen eines Stakes, ohne selbst
  Blöcke zu erstellen. Der Alltagsbegriff "Staking" umfasst beides; er ist
  für die Einordnung unbrauchbar und deshalb aufzulösen.
- "Private Vermögensverwaltung" ist kein Synonym für "privat veranlasst",
  sondern das ungeschriebene Abgrenzungsmerkmal zur gewerblichen Tätigkeit.

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. TATSACHENFRAGE ZUERST: aktive Blockerstellung oder passives
   Bereitstellen? Werte dazu die Felder "Art der Tätigkeit", "Beschreibung",
   "Eingesetzte Hardware", "Form der Erträge" und "Zeitaufwand" aus. Nach
   Rz. 34 des BMF-Schreibens vom 06.03.2025 können Mining und Forging nach
   den Umständen des Einzelfalls private oder gewerbliche Tätigkeit sein;
   nach Rz. 48 unterfällt passives Staking – die Bereitstellung eines Stakes
   ohne eigene Blockerstellung – "in der Regel als der privaten
   Vermögensverwaltung unterfallende Fruchtziehung" dem § 22 Nr. 3 EStG.
   Steht im Feld "Art der Tätigkeit" "unklar", entscheide nicht, sondern
   benenne die drei Angaben, die zur Klärung fehlen, und arbeite beide
   Varianten getrennt durch, ohne zu rechnen.
2. § 15 Abs. 2 Satz 1 EStG MERKMAL FÜR MERKMAL. Prüfe getrennt und
   nacheinander: Selbständigkeit, Nachhaltigkeit, Gewinnerzielungsabsicht,
   Beteiligung am allgemeinen wirtschaftlichen Verkehr. Ziehe zu jedem
   Merkmal die Angaben heran, die es tragen: Fremdkapital, Räume,
   Stromkosten und Hardwareumfang für Selbständigkeit und
   Gewinnerzielungsabsicht, Dauer und Zeitaufwand für die Nachhaltigkeit.
   Zur Beteiligung am allgemeinen wirtschaftlichen Verkehr gilt Rz. 38 des
   BMF-Schreibens vom 06.03.2025 im Wortlaut: "Die Blockerstellenden nehmen
   bereits dadurch am allgemeinen wirtschaftlichen Verkehr teil, indem sie
   den Netzwerkteilnehmenden ihre Rechnerleistung für die Verifikation der
   Transaktionsdaten und deren Aufnahme in einen neu zu erstellenden Block
   der Blockchain zur Verfügung stellen. Dass das Entgelt von der
   erfolgreichen Erstellung des Blocks abhängt, steht einer Teilnahme am
   allgemeinen wirtschaftlichen Verkehr nicht entgegen."
3. UNGESCHRIEBENES MERKMAL. Prüfe gesondert, ob die Grenze zur privaten
   Vermögensverwaltung überschritten ist. Kennzeichne ausdrücklich, dass
   dieses Merkmal NICHT im Wortlaut des § 15 Abs. 2 Satz 1 EStG steht,
   sondern ungeschrieben ist. Nach Rz. 39 des BMF-Schreibens vom 06.03.2025
   geht die Verwaltung bei der Blockerstellung davon aus, dass die Grenze zur
   privaten Vermögensverwaltung überschritten ist. Das ist eine
   Verwaltungsauffassung und ersetzt die Einzelfallbetrachtung nach Rz. 34
   nicht; benenne die Angaben des Sachverhalts, die dafür und die dagegen
   sprechen, und kennzeichne das Ergebnis als Verwaltungsauffassung
   (Rz. 34 und Rz. 39 – für [JAHR] verifizieren).
4. ZUORDNUNG. Führe die Schritte 1 bis 3 zusammen: § 15 EStG oder
   § 22 Nr. 3 EStG. Nach Rz. 45 des BMF-Schreibens vom 06.03.2025 liegen
   andernfalls sonstige Einkünfte nach § 22 Nr. 3 EStG vor; die dortige
   Freigrenze beträgt 256 € (Betrag – für [JAHR] verifizieren). Nenne dazu
   neben Rz. 45 die gesetzliche Fundstelle in § 22 Nr. 3 EStG mit Satzangabe
   (Fundstelle – für [JAHR] verifizieren).
   Halte fest, dass die Freigrenze zu prüfen ist und dass der Abgleich mit
   den tatsächlichen Erträgen ein Arbeitsschritt der Kanzlei ist; führe ihn
   NICHT aus und triff keine Aussage darüber, ob sie über- oder
   unterschritten ist. Ist die Zuordnung nicht ohne weitere Angaben entscheidbar,
   sag das ausdrücklich und arbeite mit klar benannten Annahmen.
5. FOLGEN DER EINORDNUNG. Behandle nacheinander: Gewerbesteuerpflicht dem
   Grunde nach, Freibetrag für natürliche Personen (Norm nennen, Betrag
   nicht nennen), Buchführungs- und Aufzeichnungspflichten einschließlich
   der Frage, ob eine Einnahmenüberschussrechnung genügt, Anzeige der
   Erwerbstätigkeit gegenüber Gemeinde und Finanzamt, Zuordnung der Hardware
   zum Betriebsvermögen und deren Abschreibung. Werte dabei das Feld
   "Weiterer Gewerbebetrieb oder vorhandenes Betriebsvermögen" aus und
   benenne, ob ein eigener Betrieb entsteht oder eine bestehende Tätigkeit
   berührt ist. Nenne zu jedem Punkt die Norm mit dem Zusatz
   "für [JAHR] verifizieren"; nenne keine betragsmäßige Grenze ohne diesen
   Zusatz.
6. VERÄUSSERUNGSFOLGEN. Stelle dar, was aus der Einordnung für die spätere
   Veräußerung der Kryptowerte folgt: Bei Zuordnung zum Betriebsvermögen
   findet § 23 EStG nach § 23 Abs. 2 EStG keine Anwendung
   (für [JAHR] verifizieren); die Veräußerung wirkt im Betrieb.
   Bleibt es beim Privatvermögen, gilt die Jahresfrist des § 23 Abs. 1
   Satz 1 Nr. 2 Satz 1 EStG; die Freigrenze steht in § 23 Abs. 3 Satz 5 EStG
   und beträgt 1.000 € ab dem Veranlagungszeitraum 2024
   (für [JAHR] verifizieren) – NICHT in § 23 Abs. 1 Nr. 2 EStG. Beachte
   zwingend die SPERRREGEL zur Veräußerungsfrist.
7. AUFZEICHNUNGS- UND MITWIRKUNGSPFLICHTEN. Werte die Felder
   "Aufzeichnungen vorhanden" und "Ausländische zentrale Handelsplattform
   beteiligt" aus. Grundlage sind Rz. 87 ff. des BMF-Schreibens vom
   06.03.2025. Steht bei der ausländischen Plattform "ja", gilt nach Rz. 89
   die erweiterte Mitwirkungspflicht nach § 90 Abs. 2 AO; dort heißt es
   wörtlich: "Fehlende Aufzeichnungen und Datenverluste (z. B. wegen
   Insolvenz der Handelsplattform oder aufgrund eines Hacker-Angriffs) gehen
   zu Lasten der Steuerpflichtigen." Nach Rz. 92 kommt eine Schätzung nach
   § 162 AO in Betracht; dort heißt es: "Eine Schätzung darf nicht dazu
   dienen, Steuerpflichtige zu sanktionieren." Führt die Einordnung zu einem
   Betrieb, treten die Pflichten der §§ 145 bis 147 AO, die GoBD, die
   Verfahrensdokumentation und der Datenzugriff nach § 147 Abs. 6 AO hinzu
   (Rz. 96 bis 99). Zitiere KEINE Randziffer der GoBD.
8. OFFENE UMSATZSTEUERLICHE FRAGE. Entscheide sie NICHT. Halte fest, dass zu
   prüfen ist, ob ein Leistungsaustausch im Sinne des § 1 Abs. 1 Nr. 1 UStG
   vorliegt, dass die umsatzsteuerliche Behandlung von Vergütungen für die
   Blockerstellung umstritten ist und dass die Entscheidung dem Berufsträger
   obliegt. Werte dabei das Feld "Rechnerleistung wird auch entgeltlich für
   benannte Dritte erbracht" aus, weil ein benannter Leistungsempfänger die
   Frage anders stellt als eine Belohnung aus dem Netzwerk. Kannst du zu
   einer Teilfrage keine gesicherte Aussage treffen, schreibe "Fundstelle
   offen – bitte recherchieren".
9. NACHWEISE. Leite aus den Schritten 1 bis 8 ab, welche Unterlagen die
   getroffene Einordnung tragen müssen. Werte dazu die Felder "Erträge
   werden sofort in Fiatgeld getauscht" und "Tätig seit" aus.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab:
   eindeutig / vertretbare Varianten / nicht ohne weitere Angaben
   entscheidbar. Fehlende Angaben auflisten, nicht erfinden.
2. Kennzeichne jede Aussage, bei der du dir nicht sicher bist oder bei der
   sich die Rechtslage geändert haben könnte. Rate nicht.
3. Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage mit Absatz und
   Satz oder das BMF-Schreiben mit Datum und Randziffer, jeweils mit dem
   Zusatz "für [JAHR] verifizieren", und führe sie am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" auf. Kennst du eine Fundstelle nicht
   sicher, schreibe "Fundstelle offen – bitte recherchieren".
4. Nenne KEINEN Jahreswert (Freigrenze, Freibetrag, Buchführungsgrenze,
   Abschreibungsbetrag) ohne den Zusatz "für [JAHR] verifizieren".
5. Berechne keine Steuer und keinen Gewinn. Der Prompt qualifiziert die
   Tätigkeit; die Erfassung der Erträge ist ein eigener Arbeitsschritt.
6. Berechne KEINE Fristen und nenne keine Fristlängen als feststehend.
   Liste stattdessen auf, WELCHE Fristen im Raum stehen, jeweils mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   ohne Dauer. Ergänze bei jeder: "Fristen berechnet und erfasst ein
   Mensch."
7. Trenne durchgehend Feststellung und Vermutung. Kennzeichne jede Vermutung
   als solche.

AUSGABEFORMAT
1. (Einschätzung der Eindeutigkeit)
2. (Einordnung) – Ergebnis in einem Satz, danach die Begründung Merkmal für
   Merkmal als Tabelle:
   Merkmal | Angaben aus dem Sachverhalt | Bewertung | Fundstelle (mit
   Zusatz) | Feststellung oder Vermutung
   Am Ende ein ausdrücklicher Vorbehalt, dass die Einordnung eine Beurteilung
   des Einzelfalls ist und vom Berufsträger zu verantworten bleibt.
3. (Gegenüberstellung der Folgen) – Tabelle:
   Folge | bei gewerblicher Einordnung | bei sonstigen Einkünften nach
   § 22 Nr. 3 EStG | was das für diesen Fall bedeutet
   Mindestens: Gewerbesteuer, Buchführung und Gewinnermittlung, Anzeige der
   Tätigkeit, Betriebsvermögen und Hardware, Behandlung späterer
   Veräußerungen, Aufzeichnungspflichten.
4. (Nachweisliste) – abhakbar, Kästchen ☐ vor jeder Position, getrennt nach:
   Tätigkeitsnachweise | Hardware und Kosten | Ertragsnachweise |
   Plattform- und Poolunterlagen | Aufzeichnungen und
   Verfahrensdokumentation.
5. (Offene umsatzsteuerliche Frage) – was zu prüfen ist, welche Angaben
   dafür fehlen, wer entscheidet.
6. (Ausgesteuerte Punkte) – nur, wenn die Aussteuerungsregel gegriffen hat.
7. (Was ich nicht sicher weiß) – offene Punkte und fehlende Angaben.
8. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. Vor dem Werkzeugeinsatz klärt der Berufsträger außerhalb des Werkzeugs und vermerkt in der Handakte: Gibt es Anhaltspunkte für eine unrichtige abgegebene Erklärung, eine Berichtigungspflicht, eine Selbstanzeige oder ein Steuerstrafverfahren? Solche Sachverhalte gehören nach `DATENSCHUTZ.md` in die Zone Rot und damit nicht in das Werkzeug – auch nicht als Ja-Nein-Angabe.
2. Die Tätigkeit vom Mandanten in eigenen Worten beschreiben lassen und erst danach das Feld „Art der Tätigkeit" ausfüllen. Viele Mandanten nennen jede Ertragsform „Staking"; die Unterscheidung zwischen aktiver Blockerstellung und passivem Bereitstellen ist der Punkt, an dem sich die gesamte Einordnung entscheidet.
3. Hardware, Stromkosten, Räume und Fremdkapital ehrlich eintragen. Wer sie weglässt, bekommt eine Einordnung, die auf Vermutungen beruht.
4. Das Ergebnis ist die Grundlage für die Erfassung, nicht die Erfassung selbst. Die Aufbereitung der Nachweise und die Prüfung eines Steuerreports laufen über Prompt 61. Für die spätere Veräußerung der Kryptowerte gibt es keinen eigenen Prompt: Prompt 90 behandelt ausschließlich Grundstücke nach § 23 Abs. 1 Satz 1 Nr. 1 EStG und trägt den Fall nicht. Die Veräußerung nach § 23 Abs. 1 Satz 1 Nr. 2 EStG bearbeitet ein Berufsträger gesondert.
5. Die Gegenüberstellung der Folgen mit dem Mandanten durchgehen, bevor eine Einordnung nach außen vertreten wird – sie macht sichtbar, was an Gewerbeanmeldung, Buchführung und Betriebsvermögen daran hängt.
6. Fällt die Entscheidung für die gewerbliche Einordnung, die Folgeschritte terminieren und im Fristenprogramm erfassen.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Verwendung prüfen: Trifft die Tatsachenannahme in Schritt 1 zu, sind alle vier Merkmale des § 15 Abs. 2 Satz 1 EStG einzeln geprüft, und ist das ungeschriebene Merkmal als ungeschrieben gekennzeichnet?
- **Freigabe durch einen Berufsträger** für die Einordnung und für jede daraus folgende Erklärung oder Anzeige (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Vier-Augen-Prinzip: Die Einordnung wird von einer Person begründet und von einer zweiten Person Merkmal für Merkmal gegen den Sachverhalt und gegen das BMF-Schreiben vom 06.03.2025 nachgeprüft und abgezeichnet** – sie wirkt auf Gewerbesteuer, Buchführungspflicht, Betriebsvermögen und alle späteren Veräußerungen fort.
- **Prüfen, dass die Ausgabe für Currency- und Payment-Token keine Zehnjahresfrist nennt.** Nach Rz. 63 des BMF-Schreibens vom 06.03.2025 kommt § 23 Abs. 1 Satz 1 Nr. 2 Satz 4 EStG dort nicht zur Anwendung. Dieser Fehler steht in vielen Vorlagen und ist der häufigste in diesem Themenfeld.
- **Prüfen, dass die Freigrenze des § 23 EStG nicht in Abs. 1 Nr. 2 verortet wird.** Sie steht in § 23 Abs. 3 Satz 5 EStG, 1.000 € ab dem Veranlagungszeitraum 2024 (für [JAHR] verifizieren).
- Fundstelle des maßgeblichen Schreibens gegenprüfen: BMF vom 06.03.2025, „Einzelfragen zur ertragsteuerrechtlichen Behandlung bestimmter Kryptowerte", GZ IV C 1 - S 2256/00042/064/043, BStBl I 2025, 658; es fasst das Schreiben vom 10.05.2022 (BStBl I S. 668) neu (für [JAHR] verifizieren).
- Die Freigrenze von 256 € bei § 22 Nr. 3 EStG (Rz. 45; gesetzliche Fundstelle mit Satzangabe in § 22 Nr. 3 EStG gegenprüfen) und jede Buchführungsgrenze am aktuellen Rechtsstand nachschlagen, bevor sie gegenüber dem Mandanten genannt werden (für [JAHR] verifizieren). Der Abgleich der Erträge mit der Freigrenze ist Sache der Kanzlei; steht in der Ausgabe die Aussage, sie sei über- oder unterschritten, ist das ein Mangel.
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum aus der KI-Antwort übernehmen.
- Keine umsatzsteuerliche Aussage aus der Antwort übernehmen: Der Prompt hat die Frage bewusst offen zu lassen. Steht in der Ausgabe eine Entscheidung, ist das ein Mangel und kein Ergebnis.
- Wurde die Tätigkeit in einer abgegebenen Erklärung bereits anders eingeordnet, bleibt die Behandlung der Vorjahre ausgesteuert und wird ausschließlich vom Berufsträger außerhalb des Werkzeugs bearbeitet.

## Varianten

- **Pool-Beteiligung:** „Ergänze einen Schritt, in dem du prüfst, welche Angaben zur vertraglichen Ausgestaltung der Pool-Beteiligung fehlen, um zwischen eigener Blockerstellung und bloßer Beteiligung an fremder Blockerstellung zu unterscheiden."
- **Mandantenfassung:** „Erzeuge zusätzlich eine Kurzfassung für den Mandanten in Sie-Form, höchstens 300 Wörter, ohne interne Bewertungen, die nur erklärt, wovon die Einordnung abhängt und welche Unterlagen gebraucht werden."
- **Nur Nachweisliste:** „Beschränke dich auf Ausgabepunkt 4 und gliedere die Nachweisliste zusätzlich nach ‚liegt vor / fehlt / beim Mandanten angefordert'."
- **Wechsel der Einordnung:** „Stelle dar, welche Angaben nötig wären, um einen Wechsel der Einordnung ab einem bestimmten Zeitpunkt zu begründen; triff keine Aussage zu abgegebenen Erklärungen."
