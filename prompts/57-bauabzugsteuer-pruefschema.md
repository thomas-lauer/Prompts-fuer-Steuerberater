# 57 – Bauabzugsteuer § 48 EStG: Prüf- und Einbehaltsschema

**Problem:** Der Mandant zahlt eine Handwerkerrechnung ohne gültige Freistellungsbescheinigung voll aus – der Haftungsbescheid kommt später an ihn, der Vorwurf an die Kanzlei.
**Rolle:** Buchhaltung, Berufsträger
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Zahlungslauf), DATEV Unternehmen online (Belegprüfung), DATEV DMS (Ablage der Freistellungsbescheinigungen)
**Was du bereitstellen musst:** Rechnung mit Leistungsbeschreibung und Beträgen; Sitz des Leistenden; Status des Leistungsempfängers und Art seiner Umsätze; Freistellungsbescheinigung mit Geltungszeitraum samt Abfrageergebnis des Bundeszentralamts für Steuern; geplantes Zahlungsdatum; Jahressumme je Leistendem.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Steuernummer, Name des Handwerksbetriebs und Bescheinigungsnummer durch Platzhalter ersetzen (`Mandant A`, `Leistender 1`, `Bescheinigung ****12`). Für die Prüfung genügen Leistungsbeschreibung, Beträge, Zeitpunkte und Status der Beteiligten. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Bilanzbuchhalter in einer deutschen Steuerkanzlei und prüfst die
Bauabzugsteuer vor dem Zahlungslauf. Du arbeitest streng nach Prüfschema und entscheidest
nichts, was die Angaben nicht hergeben.

AUFGABE
Prüfe, ob ein Steuerabzug einzubehalten ist, und leite die Folgehandlungen ab.

SACHVERHALT
- Leistender: [ROLLE, anonymisiert], Sitz: [LAND], Rechtsform: [ANGABE]
- Leistungsbeschreibung der Rechnung: [WORTLAUT]
- Beträge: Netto [NETTO], Umsatzsteuer [UMSATZSTEUER], Brutto [BRUTTO]
- Gegenleistungen an denselben Leistenden im Kalenderjahr: [BETRAG]
- Leistungsempfänger: [Unternehmer / juristische Person des öffentlichen Rechts
  / Privatperson / Vermieter]
- Umsätze des Empfängers: [nur steuerfreie Vermietung / gemischt / andere]
- Freistellungsbescheinigung: [liegt vor / liegt nicht vor / abgelaufen]
- Geltungszeitraum der Bescheinigung: [VON BIS]
- Abfrage beim Bundeszentralamt für Steuern: [erfolgt am DATUM / nicht erfolgt]
- Geplantes Zahlungsdatum: [DATUM]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Liegt eine Bauleistung im Sinne des § 48 Abs. 1 Satz 3 EStG vor? Prüfe
   POSITIV: Dient die Leistung der Herstellung, Instandsetzung, Instandhaltung,
   Änderung oder Beseitigung eines Bauwerks? Der Bauwerksbegriff ist weit
   auszulegen. Der Bauleistungsbegriff des § 48 EStG ist NICHT identisch mit dem
   des § 13b UStG – übertrage keine Abgrenzung von dort und sage ausdrücklich,
   wenn eine Einordnung nur für die Umsatzsteuer gilt. Ordne anhand der
   Baubetriebe-Verordnung und des einschlägigen BMF-Schreibens zu
   (Fundstelle – für [JAHR] verifizieren). Behandle als Zweifelsfälle mit eigener
   Begründung und eigener Fundstelle: Gerüstbau, Wartungsarbeiten an Bauwerken,
   Vermietung von Baugeräten mit und ohne Bedienpersonal, planerische Leistungen,
   Reinigung, reine Materiallieferung, Arbeitnehmerüberlassung. Nenne den jeweils
   maßgeblichen Grenzwert, soweit einer besteht
   (Grenzwert – für [JAHR] verifizieren). Bei gemischten Leistungen: Welcher Teil
   überwiegt, ist die Rechnung aufteilbar?
2. Ist der Leistungsempfänger Unternehmer oder juristische Person des
   öffentlichen Rechts? Behandle den Sonderfall des Vermieters gesondert, auch
   zur Frage, ob die Vermietung ein Unternehmen begründet.
3. Greift eine Ausnahme vom Abzug? Prüfe getrennt:
   a) die Bagatellgrenzen. Es gibt ZWEI; die höhere gilt, wenn der
      Leistungsempfänger ausschließlich steuerfreie Vermietungsumsätze erbringt.
      Bezugsgröße ist die voraussichtliche Jahressumme je Leistendem.
   b) die gesonderte Ausnahme für Leistungsempfänger, die nur eine geringe Zahl
      von Wohnungen vermieten, und ihre Voraussetzung, dass die Bauleistung
      diese Wohnungen betrifft.
   Nenne alle Grenzen nur als nachzuschlagende Größen
   (Bagatellgrenzen und maßgebliche Wohnungszahl – für [JAHR] verifizieren)
   und je Ausnahme die Rechtsgrundlage.
4. Liegt eine im Zeitpunkt der Gegenleistung gültige Freistellungsbescheinigung
   vor, und wurde sie beim Bundeszentralamt für Steuern abgefragt? Maßgeblich ist
   der Zahlungszeitpunkt, nicht das Rechnungsdatum. Fehlt die Abfrage, behandle
   die Bescheinigung als ungeprüft.
5. Wenn kein Abzugsverzicht greift: Benenne den einzubehaltenden Anteil der
   Gegenleistung (Prozentsatz – für [JAHR] verifizieren), die Bemessungsgrundlage
   (Brutto oder Netto ausdrücklich klären), Anmeldung beim Finanzamt des
   Leistenden, Abführung und Abrechnung gegenüber dem Leistenden mit
   Pflichtangaben.
6. Anrechnung beim Leistenden: In welcher Reihenfolge wird angerechnet oder
   erstattet, welche Unterlagen braucht er?

HAFTUNG
Halte fest: Der Leistungsempfänger haftet für einen nicht oder zu niedrig
abgeführten Abzugsbetrag. Das Vertrauen auf die Freistellungsbescheinigung
schützt nur unter den Voraussetzungen der Vorschrift – nenne sie mit
Rechtsgrundlage.

WEITERE ERGEBNISSE
7. Merkblatt für den Mandanten, höchstens 250 Wörter, Sie-Form, Fachbegriffe in
   einem Halbsatz erklärt, ohne Beträge und Fristen.
8. Anforderungsschreiben für die Freistellungsbescheinigung.
9. Prüfliste für den Zahlungslauf, abhakbar mit ☐, in der Reihenfolge der
   Schritte 1 bis 4 aufgebaut.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Entscheide bei unklarer Leistungsbeschreibung nicht, frage nach.
2. Berechne KEINE Fristen und nenne keine Fristlängen und keine Rechtsfolgen
   einer Versäumnis als feststehend. Liste auf, WELCHE Fristen im Raum stehen
   (Anmeldung, Abführung), je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und ohne Dauer. Ergänze bei jeder:
   "Frist von einem Menschen zu berechnen und im Fristenprogramm zu erfassen."
3. Nenne Prozentsatz, Bagatellgrenzen und maßgebliche Wohnungszahl nur als
   nachzuschlagende Größen mit dem Zusatz "für [JAHR] verifizieren".
4. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz oder BMF-Schreiben mit Datum) mit dem Zusatz "für [JAHR] verifizieren".
   Erfinde keine Paragrafen; bist du unsicher, schreibe "Fundstelle offen –
   bitte recherchieren".
5. Gib ein klares Ergebnis: [Abzug erforderlich / Abzug entfällt / nicht ohne
   weitere Angaben entscheidbar]. Bei der dritten Variante stelle beide Fälle mit
   ihren Folgen für den Zahlungslauf nebeneinander dar, ohne einen Betrag zu
   berechnen, und benenne die eine Angabe, die die Entscheidung herbeiführt.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Prüfprotokoll, Schritte 1 bis 6, mit Rechtsgrundlage
3. Ergebnis und Handlungsfolge für den Zahlungslauf
4. Fristarten mit Rechtsgrundlage
5. Merkblatt für den Mandanten
6. Anforderungsschreiben
7. Prüfliste Zahlungslauf mit ☐
8. Interne Notiz
9. Was ich nicht sicher weiß
```

## Anwendung

1. Vor jedem Zahlungslauf Handwerkerrechnungen aussteuern und je Leistendem die Bescheinigungslage klären.
2. Freistellungsbescheinigung selbst beim Bundeszentralamt für Steuern abfragen und das Ergebnis mit Datum in DATEV DMS ablegen – die KI kann das nicht.
3. Prompt je unklarem Fall ausführen, das Ergebnis als Dauervermerk zum Kreditor hinterlegen, Geltungszeitraum überwachen.
4. Bei Abzug den Zahlungsbetrag in DATEV Kanzlei-Rechnungswesen kürzen, Anmeldung und Abrechnung anstoßen, Belege zur Akte.
5. Merkblatt und Prüfliste an Mandanten geben, die selbst zahlen.

## Qualitätssicherung

- **Der Leistungsempfänger haftet.** Bei Zweifeln ist der Einbehalt der sichere Weg; die Entscheidung dagegen trifft ein Berufsträger und begründet sie zur Akte.
- **Das Ergebnis ist ein Entwurf.** Vor der Zahlung prüfen: Leistungsbeschreibung, Geltungszeitraum zum Zahlungszeitpunkt, Bemessungsgrundlage, Jahressumme je Leistendem.
- **Fristen berechnet und erfasst ein Mensch**, bei Anmeldung und Abführung mit zweiter Person zur Nachprüfung. Kein Datum aus der KI-Antwort.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person zeichnet Abzug und Anmeldung ab; jedes Schreiben nach außen gibt ein Berufsträger frei, die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** §§ 48 bis 48d EStG und § 1 Abs. 3 Baubetriebe-Verordnung im amtlichen Volltext (gesetze-im-internet.de), den BMF-Schreiben zum Steuerabzug bei Bauleistungen – der Bauleistungsbegriff des § 48 EStG deckt sich nicht mit dem des § 13b UStG –, den Hinweisen des Bundeszentralamts für Steuern sowie DATEV LEXinform.

## Varianten

- **Vermieter:** Zusatz "Prüfe nur Schritt 2 und 3, stelle beide Bagatellgrenzen und die gesonderte Ausnahme für Leistungsempfänger mit wenigen vermieteten Wohnungen gegenüber."
- **Dauerkreditor:** Zusatz "Leite eine Überwachungsroutine für Geltungszeiträume ab." Ergänzt Prompt 35.
- **Leistender im Ausland:** Zusatz "Prüfe, ob abkommensrechtliche Besonderheiten den Abzug berühren, mit Rechtsgrundlage."
