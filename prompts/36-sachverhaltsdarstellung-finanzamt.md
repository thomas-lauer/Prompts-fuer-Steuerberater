# 36 – Sachverhaltsdarstellung für das Finanzamt ausformulieren

**Problem:** Aus Notizen, Mandantenerinnerungen und einem Belegstapel entsteht unter Zeitdruck ein Schreiben, in dem Vermutungen wie Tatsachen klingen – und das später gegen den Mandanten verwendet wird.
**Rolle:** Sachbearbeitung im Entwurf, Steuerberater (Freigabe)
**DATEV-Bezug:** DATEV DMS, DATEV Meine Steuern, Schriftverkehr aus der Eigenorganisation
**Was du bereitstellen musst:** Anlass des Schreibens, Notizen und Gesprächsvermerke, Belegliste mit Bezeichnung und Datum, Mandantenangaben mit Herkunft, offene Punkte.
**Datensparsamkeit:** Vor dem Einfügen Name, Anschrift, Steuernummer, Aktenzeichen und Namen Dritter durch Platzhalter ersetzen (`Mandant A`, `Vertragspartner 1`). Für die Darstellung genügen Rollen, Daten, Beträge und Belegbezeichnungen. **Abbruch bei Berichtigungs- oder Strafverdacht.** Sobald das Material auf einen Berichtigungsfall (§ 153 AO), eine Selbstanzeige oder ein Steuerstrafverfahren hindeutet, wird der Prompt nicht weiter verwendet – solche Sachverhalte gehören nach `DATENSCHUTZ.md` (Zone Rot) in kein KI-Werkzeug. Weiter nur durch einen Berufsträger, außerhalb des KI-Werkzeugs. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist erfahrener Sachbearbeiter in einer deutschen Steuerkanzlei und
formulierst Sachverhaltsdarstellungen für das Finanzamt. Du trennst
Tatsachen und Bewertung strikt und schreibst nichts, was nicht belegt ist.

AUFGABE
Erzeuge aus den folgenden Angaben eine geordnete Sachverhaltsdarstellung.

ANLASS
- Auslöser: [ANFRAGE DES FINANZAMTS / EINSPRUCHSBEGRÜNDUNG /
  BETRIEBSPRÜFUNG / ANTRAG / NACHREICHUNG]
- Wortlaut der Frage des Finanzamts, soweit vorhanden: [WORTLAUT]
- Klärungsbedürftige Position: [BEZEICHNUNG, BETRAG, ZEITRAUM]

MATERIAL
- Notizen und Gesprächsvermerke: [TEXT, mit Datum]
- Angaben des Mandanten: [TEXT] – Herkunft je Angabe:
  [schriftlich / telefonisch / Erinnerung / unklar]
- Belege: [NR | BEZEICHNUNG | DATUM | WAS DARAUS HERVORGEHT]
- Beteiligte: [ROLLE, anonymisiert, und Verhältnis zueinander]
- Bekannte Lücken: [WAS FEHLT ODER NICHT REKONSTRUIERBAR IST]

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab: Reicht das Material
   für eine tragfähige Darstellung? Benenne fehlende Angaben.
2. TRENNE SACHVERHALT UND WERTUNG STRIKT. Der Sachverhaltsteil enthält nur
   Tatsachen. Einordnung, Schlussfolgerungen und Absichtszuschreibungen
   stehen ausschließlich im Abschnitt "Rechtliche Einordnung".
3. Behaupte NICHTS, was nicht durch einen genannten Beleg oder eine
   ausdrückliche Angabe gedeckt ist. Ergänze keine plausiblen Zwischenschritte.
3a. ABBRUCHREGEL: Ergibt sich aus dem Material, dass eine abgegebene Erklärung
    unrichtig oder unvollständig sein könnte, formuliere KEINE Darstellung weiter.
    Gib stattdessen nur aus: "Anzeichen für einen Berichtigungsfall – Anzeige- und
    Berichtigungspflicht nach § 153 AO durch einen Berufsträger prüfen (für [JAHR]
    verifizieren). Bearbeitung an dieser Stelle abgebrochen."
4. Kennzeichne jede Lücke als Lücke, an der Stelle, an der sie auftritt –
   nicht nur am Ende: "hierzu liegt uns kein Nachweis vor".
5. Formuliere KEINE Vermutung als Tatsache. Angaben aus der Erinnerung
   kennzeichnest du mit "nach Angabe des Mandanten". Was du selbst
   erschließt, ist Schlussfolgerung und gehört in die rechtliche Einordnung.
6. Schreibe im Sachverhaltsteil keine Motive oder Absichten, es sei denn,
   sie sind ausdrücklich angegeben und belegt.
7. Ordne chronologisch. Jedes Ereignis mit Datum; fehlt es, schreibe
   "Datum nicht dokumentiert" statt eines geschätzten Datums.
8. Verweise auf Belege mit ihrer Nummer, z. B. "(Beleg 3)".
9. Nenne zu jeder rechtlichen Aussage der Einordnung die einschlägige
   Rechtsgrundlage, jeweils mit dem Zusatz "für [JAHR] verifizieren", und führe
   sie am Ende in einer Tabelle "Zu verifizierende Rechtsgrundlagen" mit Spalte
   "geprüft von (leer)". Zu nennen ist insbesondere § 153 AO, sobald eine
   Berichtigung im Raum steht. Jahresabhängige Werte kennzeichnest du als
   "für [JAHR] verifizieren". Bist du dir einer Fundstelle nicht sicher, schreibe
   "Fundstelle offen – bitte recherchieren" statt einer Angabe.
10. Berechne KEINE Fristen und nenne kein Fristende. Antwortet das Schreiben
    auf eine gesetzte Frist, weise nur darauf hin, dass die Frist von einem
    Menschen zu berechnen und im Fristenprogramm zu führen ist.
11. Ton: sachlich, ohne Rechtfertigung, ohne Verstärker ("selbstverständlich",
    "eindeutig"). Höchstens 600 Wörter.

AUSGABEFORMAT
1. (Sachverhaltsdarstellung) in dieser Gliederung:
   a) Beteiligte und ihr Verhältnis zueinander
   b) Zeitlicher Ablauf – chronologisch, mit Belegverweisen
   c) Wirtschaftlicher Hintergrund – was dem Vorgang zugrunde liegt
   d) Hinweis auf die Belegunterlagen
2. (Rechtliche Einordnung) – getrennter Abschnitt, als Wertung
   überschrieben, jede Fundstelle mit "(für [JAHR] verifizieren)".
3. (Belegverzeichnis) – Tabelle:
   Nr. | Bezeichnung | Datum | belegt welche Aussage | liegt vor (ja/nein)
4. (Lücken) – Tabelle:
   Nr. | Lücke | betroffene Aussage | wie schließbar
5. (Als Wertung aus dem Sachverhalt entfernte Sätze) – Liste.
6. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | wofür sie im Text steht | geprüft von (leer)
7. (Interne Notiz) – nicht ans Finanzamt: Risiken, erwartbare Nachfragen,
   Wiedervorlage.
```

## Anwendung

1. Belege vorher nummerieren – die Nummern trägt der Entwurf wörtlich.
2. Herkunft jeder Mandantenangabe eintragen. "Telefonisch, aus der Erinnerung" führt zu einer anderen Formulierung als "schriftlich, mit Vertrag belegt".
3. Liste der entfernten Wertungen durchgehen: Steht dort Wesentliches, gehört es in die rechtliche Einordnung, nicht zurück in den Sachverhalt.
4. Lückenliste mit dem Mandanten abarbeiten, bevor das Schreiben rausgeht.
5. Darstellung nach Freigabe im DMS ablegen; sie wird in Folgeverfahren gebraucht.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Ausgangsdokuments nachgeprüft und abgezeichnet** – bei Rechtsbehelfsfristen ausnahmslos, unabhängig davon, ob ein Rechtsbehelf geplant ist. Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Freigabe durch einen Berufsträger** ist zwingend. Eine Sachverhaltsdarstellung bindet den Mandanten faktisch für das weitere Verfahren.
- **Fristen werden von einem Menschen berechnet, geprüft und im Fristenprogramm geführt** – auch die vom Finanzamt gesetzte Antwortfrist. Kein Datum aus dem Modell.
- Satz für Satz prüfen: Steht dahinter ein Beleg, eine ausdrückliche Angabe oder eine Annahme? Annahmen streichen oder kennzeichnen.
- Prüfen, ob Formulierungen eine Absicht unterstellen ("um … zu erreichen", "wollte damit"). Das ist Wertung.
- Belegverzeichnis gegen die beigefügten Unterlagen abgleichen. Ein zitierter, aber nicht beigefügter Beleg schadet mehr als keiner.
- Prüfen, ob die Darstellung mehr offenbart als die Frage verlangt – der Umfang ist Entscheidung des Berufsträgers.

## Varianten

- **Kurzfassung:** "Erzeuge eine Fassung mit höchstens 150 Wörtern für ein einfaches Antwortschreiben."
- **Gegenprobe:** "Lies die Darstellung als Betriebsprüfer und nenne die fünf Rückfragen, die du stellen würdest."
- **Zeitstrahl:** "Erzeuge eine Chronologie als Tabelle: Datum | Ereignis | Beleg | Quelle."
