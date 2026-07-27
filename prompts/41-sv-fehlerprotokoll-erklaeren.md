# 41 – SV-Fehlerprotokoll im Klartext erklären und Ursachen eingrenzen

**Problem:** Eine Meldung läuft auf Fehler – falsche Krankenkasse, unbekannte Betriebsnummer, Gefahrtarifstelle fehlt, digitaler Lohnnachweis nicht erstellbar –, die Fehlermeldung ist kryptisch, und niemand weiß, ob die Ursache in den Stammdaten, in der Abrechnung oder bei der Einzugsstelle liegt.
**Rolle:** Lohnsachbearbeitung, Teamleitung Lohn
**DATEV-Bezug:** LODAS, Lohn und Gehalt (SV-Meldezentrale, Protokolle aus dem Rückmeldedienst, digitaler Lohnnachweis UV-Meldeverfahren)
**Was du bereitstellen musst:** Fehlermeldung im Wortlaut, betroffene Meldeart, Meldezeitraum, was zuletzt an Stammdaten geändert wurde, bisherige Lösungsversuche.
**Datensparsamkeit:** Arbeitnehmer als `AN 1`, keine Personalnummer, keine Versicherungsnummer, kein Geburtsdatum, keine Anschrift. Mandant als `Mandant A`. Betriebs- und Krankenkassen-Betriebsnummern **vollständig weglassen** und als `BBNR 1`, `BBNR 2` durchnummerieren. Für die Ursachensuche genügt die Aussage, welche Nummer geändert wurde, nicht ihr Wert. Keine Angaben zu Krankheit, Arbeitsunfähigkeit oder Unfallhergang. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Fachkraft für Entgeltabrechnung in einer deutschen Steuerkanzlei und
arbeitest mit DATEV LODAS bzw. Lohn und Gehalt. Du prüfst hypothesengeleitet:
erst mögliche Ursachen sammeln, dann nach Wahrscheinlichkeit und Prüfaufwand
sortieren, dann konkrete Prüfschritte nennen. Du erfindest nichts.

AUFGABE
Erkläre die folgende Fehlermeldung aus dem Melde- oder Bescheinigungsverfahren
in Alltagssprache, grenze die Ursache ein und bereite die Klärung vor.

FEHLERMELDUNG IM WORTLAUT
[FEHLERTEXT VOLLSTÄNDIG EINFÜGEN, EINSCHLIESSLICH FEHLERNUMMER UND
 PRÜFKENNZEICHEN, OHNE PERSONENBEZUG]

KONTEXT
- Meldeart: [z. B. Anmeldung / Abmeldung / Jahresmeldung / Unterbrechung /
  Beitragsnachweis / digitaler Lohnnachweis UV / A1-Bescheinigung]
- Meldezeitraum: [ZEITRAUM]
- Empfänger: [Einzugsstelle / Minijob-Zentrale / Berufsgenossenschaft /
  Rentenversicherung]
- Betroffen: [ein AN / mehrere AN / gesamter Betrieb / gesamte Betriebsstätte]
- Zuletzt geändert: [z. B. Krankenkassenwechsel, neue Betriebsstätte,
  Gefahrtarifstelle geändert, Mandant neu angelegt, Beitragsgruppe geändert,
  Softwareupdate, Jahreswechsel]
- Bisherige Lösungsversuche: [WAS WURDE SCHON PROBIERT UND MIT WELCHEM ERGEBNIS]
- Wiederholung: [erstmals / schon früher aufgetreten]
- Wenn schon früher: Zeitraum: [ZEITRAUM]

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab:
   eindeutig / vertretbare Varianten / nicht ohne weitere Angaben entscheidbar.
   Liste die fehlenden Angaben auf.
2. Erkläre die Meldung in höchstens fünf Sätzen Alltagssprache: was das
   Verfahren beanstandet und wer den Fehler festgestellt hat (eigene Software,
   Datenannahmestelle, Empfänger).
3. WICHTIG: Erfinde KEINE Fehlerschlüssel, Prüfnummern, Meldegründe,
   Abgabegründe, Personengruppen- oder Beitragsgruppenschlüssel. Wenn du einen
   Code nicht sicher kennst, schreibe ausdrücklich "Bedeutung dieses Schlüssels
   nicht sicher – in der DATEV-Hilfe oder beim Empfänger nachschlagen" und
   erkläre stattdessen nur den Klartextanteil der Meldung.
4. Liste mögliche Ursachen nach Wahrscheinlichkeit sortiert. Höchstens sechs.
   Zu jeder Ursache genau EINEN konkreten Prüfschritt: wo nachzusehen ist und
   woran man erkennt, ob die Ursache zutrifft. Formuliere jede Ursachenaussage
   ausdrücklich als Vermutung, solange sie nicht aus den Angaben folgt.
   Nimm in die Ursachenliste auch die Kategorie "Zuordnung einer Einmalzahlung
   im ersten Quartal (§ 23a Abs. 4 SGB IV – für [JAHR] verifizieren)" auf,
   soweit der Meldezeitraum oder die Angaben darauf hindeuten.
5. Schlage eine Prüfreihenfolge vor, sortiert nach Aufwand: erst was in einer
   Minute geprüft ist, zuletzt was eine Rückfrage bei Dritten erfordert.
   Berücksichtige die Reihenfolge der Datenebenen: Betriebsstammdaten →
   Betriebsstätte/Betriebsnummer → Personenstammdaten → Abrechnungsdaten →
   Meldedatensatz. Bei Meldeart "digitaler Lohnnachweis UV" ergänze eine eigene
   Datenebene VOR den Betriebsstammdaten: erfolgreicher UV-Stammdatenabruf beim
   Unfallversicherungsträger (Mitgliedsnummer, PIN, Gefahrtarifstellen des
   Meldejahres). Nenne § 99 SGB IV als Rechtsgrundlage der Meldung und die
   Gemeinsamen Grundsätze nach § 103 SGB IV für die Datensatzbeschreibung,
   jeweils mit "für [JAHR] verifizieren", ohne Termin zu nennen.
6. Formuliere zwei Anfrageentwürfe: (a) an die Einzugsstelle bzw. den
   Meldeempfänger, (b) an den Softwaresupport. Jeweils mit Sachverhalt,
   bereits geprüften Punkten und konkreter Frage. Höchstens 150 Wörter je
   Entwurf, ohne personenbezogene Daten.
7. Nenne KEINE Jahreswerte (Beitragssätze, Beitragsbemessungsgrenzen,
   Geringfügigkeitsgrenze, Umlagesätze, Gefahrtarife), ohne sie als
   "Wert – für [JAHR] verifizieren" zu markieren.
7a. Nenne KEINE Meldefristen, Fälligkeitstermine und keine Rechtsfolgen einer
    verspäteten oder unterbliebenen Meldung als feststehend – auch nicht
    Säumniszuschläge, Schätzung, Bußgeld oder strafrechtliche Folgen. Gib
    stattdessen aus, WELCHE Frist im Raum steht und wo sie nachzuschlagen ist
    (Meldefristen: DEÜV; Beitragsnachweis und Fälligkeit: §§ 23, 28f SGB IV –
    für [JAHR] verifizieren), und den Satz "Frist und Folgen sind von einem
    Menschen zu prüfen und im Fristenprogramm zu erfassen".
8. Nenne zu jedem Prüfungsschritt die einschlägige Rechtsgrundlage, jeweils mit
   dem Zusatz "für [JAHR] verifizieren", und führe sie am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit Spalte "geprüft von (leer)".
   Mindestens zu nennen, soweit im Fall berührt: Meldeverfahren DEÜV,
   Fälligkeit § 23 SGB IV, Einmalzahlungen § 23a SGB IV, Meldepflichten
   § 28a SGB IV, Beitragsnachweis und Aufzeichnungspflichten § 28f SGB IV,
   digitaler Lohnnachweis § 99 SGB IV, Gemeinsame Grundsätze § 103 SGB IV.
   Bist du dir einer Fundstelle nicht sicher, schreibe "Fundstelle offen – bitte
   recherchieren" statt einer Angabe.

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit
2. Klartexterklärung
3. Ursachentabelle: Rang | Vermutete Ursache | Prüfschritt | Wo zu prüfen |
   Trifft zu (leer)
4. Prüfreihenfolge (nummeriert, abhakbar mit ☐)
5. Anfrageentwurf Einzugsstelle / Meldeempfänger
6. Anfrageentwurf Softwaresupport
7. Interne Notiz: welche Frist im Raum steht (ohne Datum, ohne Fristlänge), wo
   sie nachzuschlagen ist, wer sie einträgt
8. Zu verifizierende Rechtsgrundlagen: Nr. | Fundstelle | wofür sie steht |
   geprüft von (leer)
9. Was ich nicht sicher weiß
```

## Anwendung

1. Fehlertext aus dem Protokoll vollständig kopieren, dann Personalnummer, Versicherungsnummer und Betriebsnummern maskieren. Der Wortlaut trägt die Information, die Nummern nicht.
2. Prüfreihenfolge von oben nach unten abarbeiten und das Ergebnis in der Spalte "Trifft zu" festhalten – das ist zugleich die Dokumentation für die Rückfrage.
3. Erst nach den Punkten 1 bis 3 der Reihenfolge den Anfrageentwurf verwenden.
4. Gelöste Fälle mit Fehlertext und tatsächlicher Ursache in eine kanzleiinterne Fehlersammlung aufnehmen.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Ausgangsdokuments nachgeprüft und abgezeichnet** – bei Rechtsbehelfs- und Widerspruchsfristen ausnahmslos, unabhängig davon, ob ein Rechtsbehelf geplant ist. Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Jede Schlüsselbedeutung selbst nachschlagen.** Meldegründe, Abgabegründe, Personengruppen- und Beitragsgruppenschlüssel sind der Punkt, an dem das Modell strukturell falsch liegt. Maßgeblich sind die DATEV-Hilfe, die Gemeinsamen Grundsätze und die Auskunft des Empfängers – nicht die KI-Antwort.
- Prüfen, ob die Meldefrist noch läuft. Eine Ursachenanalyse ersetzt keine fristgerechte Abgabe; im Zweifel korrekt melden und danach klären.
- Vor Korrekturmeldungen (Stornierung und Neumeldung) prüfen, welche Folgemeldungen und Bescheinigungen betroffen sind, und die Freigabe durch die Teamleitung einholen.
- Anfrageentwurf vor Versand auf personenbezogene Daten durchsehen; Versicherungsnummern gehören in den Meldeweg, nicht in eine Support-E-Mail.
- Bei Betriebsnummern- und Betriebsstättenfehlern prüfen, ob frühere Meldungen denselben Fehler haben.

## Varianten

- **Sammelprotokoll:** "Es liegen mehrere Fehlermeldungen vor. Gruppiere sie nach vermuteter gemeinsamer Ursache und nenne je Gruppe einen Prüfschritt."
- **Digitaler Lohnnachweis:** Zusatz "Prüfe zusätzlich, ob Gefahrtarifstellen, Mitgliedsnummer der Berufsgenossenschaft und Zuordnung der Arbeitsstunden hinterlegt sind."
- **Arbeitsanweisung:** "Leite aus der Ursache eine Arbeitsanweisung ab, die den Fehler künftig verhindert."
- **Anschreiben:** siehe Prompt 42 für die Korrespondenz mit dem Meldeempfänger.
