# 59 – Kapitalertragsteuer bei Gewinnausschüttung: Ablauf- und Fristenschema

**Problem:** Der Gesellschafterbeschluss liegt vor, die Anmeldung erfolgt zu spät oder ohne Steuerbescheinigung – beim Gesellschafter fehlt später die Anrechnung.
**Rolle:** Fachassistent, Berufsträger
**DATEV-Bezug:** DATEV Körperschaftsteuer (einschließlich Kapitalertragsteuer-Anmeldung), DATEV DMS
**Was du bereitstellen musst:** Gesellschafterbeschluss mit Datum, Ausschüttungsbetrag und vereinbartem Auszahlungszeitpunkt; Gesellschafterliste mit Beteiligungsquote, Rechtsform, Wohnsitz- oder Sitzstaat und Angabe, wer beherrschender Gesellschafter ist; Bestand des steuerlichen Einlagekontos aus der letzten Feststellung; Art der Ausschüttung; vorliegende Freistellungs- oder Erstattungsbescheinigungen; bisherige Anmeldungen des Jahres.
**Datensparsamkeit:** Vor dem Einfügen Gesellschafts- und Gesellschafternamen sowie Anschriften durch Platzhalter ersetzen (`Gesellschaft A`, `Gesellschafter 1`). **Steuernummern und Steuer-Identifikationsnummern vollständig entfernen, nicht teilmaskieren** – sie gehören nach `DATENSCHUTZ.md` (Zone Rot) auch in Ausschnitten in kein KI-Werkzeug. Quoten, Beträge und Staaten dürfen bleiben. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachassistent für Kapitalgesellschaften in einer deutschen
Steuerkanzlei. Du arbeitest nach Ablaufplan und berechnest keine Fristen.

AUFGABE
Erstelle den Ablaufplan der Kapitalertragsteuer für die geplante Ausschüttung,
unterscheide nach Empfänger, prüfe die Sonderfälle und erzeuge die
Arbeitsergebnisse.

SACHVERHALT
- Rechtsform der ausschüttenden Gesellschaft: [GmbH / UG / AG / …]
- Beschluss: [DATUM], Ausschüttungsbetrag: [BETRAG]
- Vereinbarter Auszahlungszeitpunkt: [DATUM ODER OFFEN]
- Art: [Gewinnausschüttung / Vorabausschüttung / Sachausschüttung /
  verdeckte Gewinnausschüttung / Einlagenrückgewähr]
- Gesellschafter mit Quote, Rechtsform und Staat: [LISTE]
- Beherrschender Gesellschafter: [ja bei GESELLSCHAFTER / nein]
- Steuerliches Einlagekonto, letzter festgestellter Bestand: [BETRAG]
- Organschaft: [ja / nein / unklar]
- Freistellungs- oder Erstattungsbescheinigungen: [LISTE ODER KEINE]

ABLAUFPLAN
Stelle die Schritte in dieser Reihenfolge dar, je mit Verantwortlichem,
erforderlichem Dokument und Rechtsgrundlage:
1. Beschlussfassung und ihre formalen Voraussetzungen
2. Zuflusszeitpunkt beim Gesellschafter und wodurch er bestimmt wird
3. Entstehung der Kapitalertragsteuer und der Einbehalt
4. Anmeldung beim Finanzamt der Gesellschaft
5. Abführung
6. Steuerbescheinigung an den Gesellschafter
7. Ablage und Nachweisführung
Nenne bei 4 bis 6 nur die Fristart, nicht Datum und nicht Dauer.

FALLUNTERSCHEIDUNG NACH EMPFÄNGER
Behandle getrennt und benenne je Fall Einbehalt, Höhe, Anrechnung oder
Erstattung sowie die erforderlichen Bescheinigungen:
a) natürliche Person im Inland
b) Kapitalgesellschaft im Inland
c) Empfänger im Ausland, einschließlich Entlastung nach Abkommen oder
   nationalem Recht und des dafür zuständigen Verfahrens
d) Organschaft

SONDERFÄLLE, JEDEN AUSDRÜCKLICH PRÜFEN
Vorabausschüttung; verdeckte Gewinnausschüttung; Einlagenrückgewähr aus dem
steuerlichen Einlagekonto einschließlich der Verwendungsreihenfolge, der Bindung
an die letzte Feststellung und der Folgen einer fehlenden, verspäteten oder zu
niedrigen Steuerbescheinigung – benenne ausdrücklich, ob und bis zu welchem
Zeitpunkt eine Berichtigung möglich ist und welche Rechtsfolge eintritt, wenn die
Bescheinigung nicht rechtzeitig erteilt wird
(Rechtsgrundlage – für [JAHR] verifizieren); Sachausschüttung mit Bewertung und
Bemessungsgrundlage; beherrschender Gesellschafter mit der Besonderheit des
Zuflusszeitpunkts. Sage je Sonderfall, was zusätzlich zu klären ist.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben.
2. Halte fest: Steuerschuldner ist der Gläubiger der Kapitalerträge; die
   Gesellschaft hat die Steuer für dessen Rechnung einzubehalten und abzuführen
   und haftet dafür. Nenne je Aussage die Norm mit Absatz und Satz und benenne,
   was gilt, wenn die Gesellschaft die Steuer wirtschaftlich übernimmt.
3. Berechne KEINE Fristen und nenne keine Fristlängen und keine Rechtsfolgen
   einer Versäumnis als feststehend. Liste auf, WELCHE Fristen im Raum stehen
   (Anmeldung, Abführung, Bescheinigung), je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und ohne Dauer. Ergänze bei jeder:
   "Frist von einem Menschen zu berechnen und im Fristenprogramm zu erfassen."
4. Nenne Steuersätze, Zuschläge, Freibeträge und Beträge nur als
   nachzuschlagende Größen mit dem Zusatz "für [JAHR] verifizieren".
5. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz oder BMF-Schreiben mit Datum) mit dem Zusatz "für [JAHR] verifizieren".
   Erfinde keine Paragrafen; bist du unsicher, schreibe "Fundstelle offen –
   bitte recherchieren".
6. Die Steuerbescheinigung gib nur als STRUKTUR mit den erforderlichen
   Angabefeldern aus, nicht als amtliches Muster und nicht als ausfüllbares
   Formular. Weise darauf hin, dass das amtliche Muster zu verwenden ist.
7. ABBRUCHREGEL: Deutet das Material auf eine verdeckte Gewinnausschüttung in
   abgeschlossenen Jahren oder auf eine unrichtige abgegebene Erklärung hin,
   arbeite NICHT weiter. Gib nur aus: "Anzeichen für eine Berichtigungspflicht –
   Bearbeitung abgebrochen, Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Ablaufplan als Tabelle (Schritt | Verantwortlich | Dokument | Fristart |
   Rechtsgrundlage)
3. Fallunterscheidung a bis d
4. Sonderfälle mit zusätzlichem Klärungsbedarf
5. Checkliste "Was muss vor der Ausschüttung geklärt sein", abhakbar mit ☐
6. Struktur der Steuerbescheinigung als Feldliste
7. Merkblatt für den Mandanten, höchstens 250 Wörter, Sie-Form, ohne Beträge
   und ohne Fristen
8. Interne Notiz
9. Was ich nicht sicher weiß
```

## Anwendung

1. Beschluss, Gesellschafterliste und den festgestellten Bestand des steuerlichen Einlagekontos bereitlegen – ohne diese Angaben ist die Verwendung nicht bestimmbar.
2. Prompt vor der Auszahlung ausführen, nicht danach; der Zuflusszeitpunkt steuert alles Weitere.
3. Fristarten in der Fristenkontrolle erfassen und von einem Menschen terminieren, Anmeldung im DATEV-Steuerprogrammverbund vorbereiten – DATEV Körperschaftsteuer (einschließlich Kapitalertragsteuer-Anmeldung).
4. Steuerbescheinigung im amtlichen Muster erstellen, die Feldliste des Prompts nur als Vollständigkeitskontrolle nutzen, Ausfertigung in DATEV DMS ablegen.
5. Merkblatt und Checkliste vor dem Beschluss an die Geschäftsführung geben.

## Qualitätssicherung

- **Steuerschuldner ist der Gesellschafter, haften muss die Gesellschaft.** Sie behält die Steuer für Rechnung des Gläubigers der Kapitalerträge ein, führt sie ab und haftet dafür. Einbehalt, Anmeldung und Abführung sind kein Ermessen; die Verantwortung trägt die Geschäftsführung, die Prüfung der Kanzlei ist zu dokumentieren.
- **Das Ergebnis ist ein Entwurf.** Vor der Auszahlung prüfen: Zuflusszeitpunkt, Empfängerstatus je Gesellschafter, Verwendung des steuerlichen Einlagekontos, Bemessungsgrundlage.
- **Fristen berechnet und erfasst ein Mensch**, bei Anmeldung und Abführung mit zweiter Person zur Nachprüfung. Kein Datum aus der KI-Antwort.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person prüft Anmeldung und Bescheinigung Feld für Feld; Anmeldung, Bescheinigung und Mandantenschreiben gibt ein Berufsträger frei, die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** §§ 43, 43a, 44, 45a EStG und § 27, insbesondere § 27 Abs. 5 KStG im amtlichen Volltext (gesetze-im-internet.de), dem amtlichen Muster der Steuerbescheinigung und den BMF-Schreiben dazu, den Hinweisen des Bundeszentralamts für Steuern zur Entlastung bei Auslandsfällen sowie DATEV LEXinform.

## Varianten

- **Auslandsgesellschafter:** Zusatz "Behandle nur Fall c und benenne das Entlastungsverfahren mit den erforderlichen Nachweisen."
- **Einlagenrückgewähr:** Zusatz "Stelle Verwendungsreihenfolge, Bindung an die letzte Feststellung und die Folgen einer fehlenden, verspäteten oder zu niedrigen Steuerbescheinigung als eigenen Prüfschritt dar."
- **Beschlussvorbereitung:** Zusatz "Erzeuge nur die Checkliste vor der Ausschüttung." Ergänzt Prompt 17.
