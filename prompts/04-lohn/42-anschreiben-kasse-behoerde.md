# 42 – Anschreiben an Krankenkasse, Behörde oder Amt zu Bescheinigungen

**Problem:** Eine Bescheinigung wird zurückgewiesen, ein Amt fragt nach, ein Arbeitnehmer braucht kurzfristig einen Nachweis – jedes Mal wird das Anschreiben neu formuliert, und die Hälfte der Rückfragen entsteht, weil eine Angabe fehlt.
**Rolle:** Lohnsachbearbeitung, Sekretariat
**DATEV-Bezug:** LODAS, Lohn und Gehalt (Bescheinigungswesen, SV-Meldungen), DATEV Eigenorganisation (Wiedervorlage)
**Was du bereitstellen musst:** Adressat und Anlass, Bezugszeichen des Vorgangs, der streitige oder ungeklärte Punkt, die eigene Rechtsauffassung, gewünschte Frist.
**Datensparsamkeit:** Besonders streng. Arbeitnehmer als `AN 1`, Arbeitgeber als `Mandant A`, keine Personalnummern, keine Versicherungsnummern, keine Anschriften. **Gesundheitsdaten und Angaben zum Grund einer Leistung gehören NICHT in den Prompt** – also keine Diagnosen, keine Angaben zu Arbeitsunfähigkeit, Schwangerschaft, Reha, Unfallhergang, Behinderung, ebenso keine Gläubiger- oder Unterhaltsdaten. Für den Entwurf genügt die neutrale Bezeichnung des Vorgangs ("Bescheinigung zu einem Entgeltersatzleistungsfall"). Konkrete Angaben erst beim Ausfüllen der Kanzleivorlage einsetzen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist erfahrene Kanzleimitarbeiterin in einer deutschen Steuerkanzlei und
schreibst Korrespondenz mit Krankenkassen, Ämtern und Behörden.
Dein Stil: höflich, sachlich, kurze Sätze, keine Floskeln, keine Vorwürfe,
immer mit konkretem nächsten Schritt und klarer Frist.

AUFGABE
Formuliere ein Anschreiben zum folgenden Vorgang.

ANLASS (genau einen wählen)
[Rückfrage einer Behörde beantworten / zurückgewiesene Bescheinigung
 korrigiert erneut einreichen / fehlende Angaben nachfordern /
 Auskunft oder Beurteilung anfordern / Widerspruch einlegen und begründen
 (nur nach Freigabe durch einen Berufsträger) / Sachstandsanfrage]

KONTEXT
- Adressat: [Krankenkasse / Minijob-Zentrale / Agentur für Arbeit /
  Familienkasse / Rentenversicherung / Berufsgenossenschaft / Jobcenter /
  Elterngeldstelle / Finanzamt]
- Wir schreiben: [im Auftrag des Arbeitgebers / als steuerlicher Berater
  des Arbeitgebers]
- Bezugszeichen: [AKTENZEICHEN / VORGANGSNUMMER / DATUM DES SCHREIBENS]
- Betroffene Bescheinigung oder Meldung: [BEZEICHNUNG, ZEITRAUM]
- Streitiger oder ungeklärter Punkt: [SACHLICH IN 1 BIS 3 SÄTZEN,
  OHNE GESUNDHEITSDATEN UND OHNE LEISTUNGSGRUND]
- Unsere Auffassung und ihre Begründung: [ANGABEN; falls keine eigene
  Rechtsauffassung besteht: "offen, wir bitten um Beurteilung"]
- Bereits vorgelegte Unterlagen: [ANGABEN]
- Gewünschte Frist: [DATUM ODER FRISTLÄNGE]
- Eilbedürftigkeit: [normal / eilig]
- Wenn eilig, sachlicher Grund: [GRUND]

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab. Wenn Angaben fehlen,
   die für ein versandfähiges Schreiben nötig sind, liste sie auf und
   markiere die Stelle im Entwurf mit (Angabe ergänzen).
2. Aufbau des Anschreibens: Betreff mit Bezugszeichen – Bezug auf das
   Schreiben, Datum aus dem Bezugszeichen übernehmen –
   Sachverhalt in höchstens sechs Sätzen –
   unsere Auffassung bzw. unsere Frage – konkrete Bitte mit Frist –
   Ansprechpartner und Rückrufmöglichkeit.
3. Formuliere die Bitte handlungsfähig: was der Adressat konkret tun soll
   (bestätigen, korrigieren, mitteilen, aussetzen), nicht nur "um Prüfung".
4. Trenne Tatsachen von Rechtsauffassung sichtbar. Kennzeichne jede
   Rechtsauffassung als solche ("Nach unserer Auffassung …"). Behaupte keine
   Tatsache, die nicht in den Angaben steht.
5. Nimm KEINE Gesundheitsdaten, Diagnosen, Angaben zum Grund einer Leistung,
   Gläubiger- oder Unterhaltsdaten in den Text auf, auch nicht sinngemäß.
   Bezeichne den Vorgang neutral. Wenn eine solche Angabe für die Klärung
   zwingend wäre, schreibe stattdessen: (Diese Angabe wird nicht per E-Mail
   übermittelt – bitte gesonderten Weg vereinbaren.)
6. Nenne KEINE Jahreswerte (Beitragsbemessungsgrenzen, Sachbezugswerte,
   Geringfügigkeitsgrenze, Pfändungsfreibeträge, Umlagesätze), ohne sie als
   "Wert – für [JAHR] verifizieren" zu markieren.
6a. Formuliere niemals eine bloße Ankündigung eines Widerspruchs. Ist Widerspruch
    gewollt, weise ausdrücklich aus: "Eine Ankündigung wahrt die
    Widerspruchsfrist nicht (§ 84 SGG – für [JAHR] verifizieren); der Widerspruch
    selbst ist fristgerecht einzulegen und die Frist von einem Menschen zu
    berechnen und einzutragen."
6b. Nenne zu jedem Prüfungsschritt die einschlägige Rechtsgrundlage, jeweils mit
    dem Zusatz "für [JAHR] verifizieren", und führe sie am Ende in einer Tabelle
    "Zu verifizierende Rechtsgrundlagen" mit Spalte "geprüft von (leer)".
    Mindestens zu nennen, soweit im Fall berührt: Vertretungsbefugnis § 73 SGG,
    Widerspruch § 84 SGG. Bist du dir einer Fundstelle nicht sicher, schreibe
    "Fundstelle offen – bitte recherchieren" statt einer Angabe. Erfinde keine
    Formularbezeichnungen.
7. Länge: höchstens 250 Wörter. Sie-Form. Keine Abkürzungen ohne Auflösung.

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit
2. Anschreiben (versandfertig, Platzhalter als (Angabe ergänzen))
3. Anlagenliste: Anlage | Bezeichnung | liegt vor (☐) | enthält geschützte
   Daten (ja/nein)
4. Interne Notiz: Fristenkontrolle, Wiedervorlage, wer freigibt, was noch
   zu klären ist
5. Zu verifizierende Rechtsgrundlagen: Nr. | Fundstelle | wofür sie steht |
   geprüft von (leer)
6. Was ich nicht sicher weiß
```

## Anwendung

1. Den streitigen Punkt neutral beschreiben, bevor der Prompt ausgefüllt wird – das ist der Arbeitsschritt, der die Datenschutzprobleme verhindert.
2. Entwurf in die Kanzleivorlage übernehmen; Namen, Anschriften, Personal- und Versicherungsnummern erst dort einsetzen.
3. Anlagenliste abarbeiten. Anlagen mit geschützten Daten nicht per einfacher E-Mail versenden, sondern über den vereinbarten Weg.
4. Frist und Wiedervorlage sofort eintragen, nicht erst nach Versand.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Ausgangsdokuments nachgeprüft und abgezeichnet** – bei Widerspruchs- und Rechtsbehelfsfristen ausnahmslos, unabhängig davon, ob ein Rechtsbehelf geplant ist. Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Vertretungsbefugnis vorab klären.** Steuerberater sind nach § 73 Abs. 2 Satz 2 Nr. 4 SGG in Angelegenheiten nach §§ 28h, 28p SGB IV vertretungsbefugt (Einzugsstelle, Betriebsprüfung). Statusfeststellungsverfahren nach § 7a SGB IV sind dort **nicht** genannt – solche Vorgänge nicht ohne Klärung durch den Berufsträger bearbeiten (für [JAHR] verifizieren).
- **Zuständigkeit und Vollmacht prüfen.** Mandant ist der Arbeitgeber. Schreiben an Behörden in Angelegenheiten des Arbeitnehmers nur mit ausdrücklicher Grundlage; sonst über den Arbeitgeber.
- Bezugszeichen, Zeitraum und Bescheinigungsart gegen den Originalvorgang abgleichen. Ein falsches Aktenzeichen kostet mehr Zeit als das ganze Schreiben.
- Den Text vor Versand gezielt nach Gesundheits- und Leistungsgrundangaben durchsehen, auch nach solchen, die sich aus dem Zusammenhang ergeben.
- Fristen niemals aus der KI-Antwort übernehmen: gesetzliche Fristen (Widerspruch, Meldung, Bescheinigung) selbst nachschlagen und im Fristenkalender führen.
- Ein Widerspruch oder eine Rechtsauffassung zu Statusfragen geht nur nach Freigabe durch den Berufsträger hinaus; eine bloße Ankündigung wahrt die Frist nicht und ersetzt den Widerspruch nicht. Grenzen des Rechtsdienstleistungsgesetzes beachten.

## Varianten

- **Erinnerung:** "Formuliere eine Erinnerung, weil auf unser Schreiben vom [DATUM] keine Antwort erfolgt ist – sachlich, ohne Vorwurf, mit neuer Frist."
- **Kurzfassung für den Mandanten:** "Fasse in vier Sätzen zusammen, was wir geschrieben haben und was der Arbeitgeber jetzt tun muss."
- **Antwort auf Zurückweisung:** siehe Prompt 41 für die Ursachenanalyse der zurückgewiesenen Meldung.
- **Telefonnotiz:** "Erzeuge stattdessen einen Gesprächsleitfaden für ein Telefonat mit fünf Fragen und Platz für Antworten."
