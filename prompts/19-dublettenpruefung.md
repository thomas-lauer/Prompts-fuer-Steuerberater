# 19 – Dublettenprüfung auf Buchungs- und Stammdatenexporten

**Problem:** Belege werden doppelt eingereicht (einmal per Mail, einmal über das Portal) und Personenkonten doppelt angelegt, weil die Schreibweise abweicht – beides fällt erst im Abschluss oder beim Zahlungslauf auf.
**Rolle:** Buchhaltung, Stammdatenpflege
**DATEV-Bezug:** Kanzlei-Rechnungswesen (Buchungsstapel, Journal, Personenkonten/Debitoren-Kreditoren-Stammdaten), DATEV Unternehmen online (Belegeingang aus mehreren Kanälen)
**Was du bereitstellen musst:** Modus A: Buchungsexport mit Datum, Beleg-/Rechnungsnummer, Betrag, Konto, Gegenkonto, Buchungstext, Erfassungsdatum, Belegquelle. Modus B: Stammdatenexport mit Kontonummer, Name, Anschriftsort, IBAN, USt-IdNr., Anlagedatum.
**Datensparsamkeit:** Klarnamen durch Platzhalter ersetzen (`Kreditor 1`). IBAN und USt-IdNr. **nicht verkürzen, sondern durch Pseudonyme ersetzen**: identische Werte erhalten dasselbe Pseudonym (`IBAN-A`, `IBAN-B`, `USTID-A`), verschiedene Werte verschiedene. Die Zuordnungstabelle bleibt in der Kanzlei. Verkürzte Angaben (`****1234`) sind unbrauchbar, weil verschiedene Konten in den letzten Stellen übereinstimmen können. Steuernummern von Geschäftspartnern ebenso pseudonymisieren. Mandantenname und Steuernummer weglassen.
Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du bist Sachbearbeiterin für Datenqualität in einer deutschen Steuerkanzlei.
Du arbeitest regelbasiert: Du prüfst jeden Treffer gegen ein benanntes
Kriterium und gibst an, wie sicher der Treffer ist. Du behauptest keine
Dublette, die du nicht an einem Kriterium festmachen kannst.

AUFGABE
Finde Dubletten im folgenden Export und schlage je Fund eine Zusammenführung
oder Bereinigung vor.

MODUS
- Modus: [A = Buchungsdubletten / B = Stammdatendubletten]
  Bearbeite ausschließlich den gewählten Modus.

RAHMEN
- Mandant / Branche: [MANDANT / BRANCHE]
- Zeitraum bzw. Stand: [ZEITRAUM / STICHTAG]
- Kontenrahmen: [SKR03 / SKR04]
- Belegkanäle: [z. B. Mail, Portal, Papier, Scan-App]
- Besonderheiten: [z. B. Dauerbuchungen, Ratenzahlungen, wiederkehrende
  gleiche Beträge, mehrere Standorte mit gleichem Lieferanten]

DATEN
[EXPORT EINFÜGEN]

KRITERIEN MODUS A – BUCHUNGSDUBLETTEN
Prüfe in dieser Reihenfolge und halte je Treffer das erfüllte Kriterium fest:
1. Gleicher Betrag + gleiches Belegdatum + gleicher Kreditor/Debitor
2. Gleicher Betrag + gleiche Rechnungsnummer (auch bei abweichendem Datum)
3. Gleiche Rechnungsnummer bei abweichendem Betrag (Hinweis auf Teilerfassung
   oder Korrektur, nicht zwingend Dublette)
4. Betrag identisch bis auf Rundung (Abweichung bis [BETRAG]) innerhalb eines
   Zeitfensters von [ZAHL] Tagen beim selben Geschäftspartner
5. Gleicher Betrag + ähnlicher Buchungstext bei unterschiedlichem Erfassenden
   oder unterschiedlicher Belegquelle
Grenze ausdrücklich ab, was KEINE Dublette ist: wiederkehrende Zahlungen
(Miete, Leasing, Abschläge), Raten, Sammelrechnungen, Storno plus Neubuchung.

KRITERIEN MODUS B – STAMMDATENDUBLETTEN
Prüfe in dieser Reihenfolge:
1. Gleiche IBAN bei verschiedenen Kontonummern
2. Gleiche USt-IdNr. oder Steuernummer bei verschiedenen Kontonummern
3. Namensvarianten desselben Partners: Rechtsformzusatz weggelassen oder
   anders geschrieben (GmbH / G.m.b.H., & Co. KG / u. Co. KG, e.K. / eK);
   umschriebene Umlaute (Müller / Mueller / Muller); Abkürzungen und
   Kurzformen (Elektro / Elektr., Gebr.); abweichende Leerzeichen,
   Bindestriche, Punkte, Groß-/Kleinschreibung; Wortdreher und Zusätze
   (Filiale, Werk, Niederlassung, Standort)
4. Gleicher Name bei unterschiedlichem Ort – ausdrücklich als möglicher
   ECHTER Unterschied kennzeichnen (Filialen, Namensgleichheit)

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER DATENQUALITÄT ab und benenne fehlende
   Felder. Fehlt ein für ein Kriterium nötiges Feld, sage das, statt zu raten.
2. Vergib je Fund einen Sicherheitsgrad: (sicher) / (wahrscheinlich) / (prüfen).
   (sicher) nur, wenn mindestens ein eindeutiges Kriterium erfüllt ist
   (gleiche IBAN, gleiche Rechnungsnummer + gleicher Betrag). Alles, was nur
   auf Namensähnlichkeit beruht, ist höchstens (wahrscheinlich).
   Beruht ein Treffer auf pseudonymisierten Bank- oder Steuermerkmalen, setze
   den Sicherheitsgrad höchstens auf (wahrscheinlich) und nenne als Prüfschritt
   den Abgleich der vollständigen Werte in der Kanzlei.
3. Nenne je Fund ausdrücklich das Kriterium, aus dem der Verdacht folgt.
4. Schlage je Fund eine Zusammenführung vor: welcher Datensatz bleibt führend
   (Begründung: ältestes Anlagedatum, vollständigste Daten, bebucht), was mit
   dem anderen geschieht und was vor der Zusammenführung zu prüfen ist
   (offene Posten, Zahlungsläufe, Mahnstufen, Vorjahresbezug).
5. Höchstens 25 Funde, sortiert nach Sicherheitsgrad, dann nach Betrag.
   Lieber eine kurze belastbare Liste als eine lange vermutete.
6. Nenne KEINE Kontonummer als gesichert und keine Jahreswerte oder
   Betragsgrenzen ohne den Zusatz "für [JAHR] verifizieren".
7. Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Kannst du sie nicht angeben, kennzeichne die Aussage
   als "ohne Fundstelle – vor Verwendung belegen". Erfinde keine Paragrafen,
   BMF-Schreiben oder Dokumentnummern; unsichere: "Fundstelle offen – bitte
   recherchieren".

AUSGABEFORMAT
1. Datenqualität
2. Fundliste (Nr. | Sicherheitsgrad | betroffene Datensätze | erfülltes
   Kriterium | Betrag/Datum | Zusammenführungsvorschlag | vorher zu prüfen)
3. Ausdrücklich KEINE Dublette (Position | warum nicht)
4. Interne Notiz (Bereinigungsreihenfolge, Risiken, offene Punkte)
5. Was ich nicht sicher weiß
```

## Anwendung

1. Modus wählen und nur die dafür nötigen Felder exportieren – gemischte Exporte erzeugen Scheintreffer.
2. Namen und Bankdaten pseudonymisieren, nicht verkürzen: gleiche Werte erhalten dasselbe Pseudonym, verschiedene ein anderes – sonst findet die Prüfung nichts oder Falsches.
3. Prompt ausführen, Fundliste in eine Arbeitsdatei übernehmen und Spalte "geprüft von / am" ergänzen.
4. Erst nach Freigabe im Programm bereinigen: bei Buchungen storniert man, bei Stammdaten sperrt man das nicht führende Konto, statt es zu löschen.

## Qualitätssicherung

- **Niemals automatisch löschen.** Keine Buchung und kein Personenkonto wird auf Grundlage der KI-Ausgabe gelöscht. Buchungen werden storniert oder umgebucht, Konten gesperrt und erst nach Abschluss zusammengeführt – jeweils mit Beleg über den Vorgang.
- Jeden Fund mit Sicherheitsgrad (sicher) trotzdem am Originalbeleg prüfen. Gleicher Betrag am gleichen Tag ist bei Abschlägen, Filialen und Raten normal.
- Vor Zusammenführung von Personenkonten prüfen: offene Posten, laufende Mahnungen, Zahlungsläufe, Vorjahresbestände, Bezug in Anlagen- oder Vertragsverwaltung. Eine Zusammenführung im laufenden Jahr kann Vorjahresvergleiche zerstören.
- Vier-Augen-Prinzip: Die Bereinigung führt eine andere Person durch als die, die die Fundliste erstellt hat; die Freigabe zeichnet der Berufsträger ab.
- Aufbewahrungs- und Unveränderbarkeitspflichten (GoBD) beachten – ein festgeschriebener Stapel wird nicht nachträglich verändert.

## Varianten

- **Belegeingang statt Buchung:** Auf die Belegliste aus dem Portal anwenden, Zusatz "Prüfe zusätzlich gleiche Dateigröße und gleichen Dateinamen als Hinweis auf Doppeleinreichung."
- **Laufende Kontrolle:** Zusatz "Leite aus den Funden eine Arbeitsanweisung ab, die die häufigste Dublettenursache künftig verhindert (z. B. verbindlicher Belegkanal)."
- **Mandatsübernahme:** Zusatz "Berücksichtige, dass Stammdaten aus zwei Systemen stammen, und weise auf Konten hin, die nur in einem Bestand bebucht sind."
