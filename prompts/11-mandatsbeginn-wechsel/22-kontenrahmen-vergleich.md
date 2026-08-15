# 22 – Kontenrahmen-Vergleich SKR03 ↔ SKR04 bei Mandatsübernahme

**Problem:** Bei Mandatsübernahme oder Kontenrahmenwechsel müssen Salden und Kontierungsgewohnheiten des Vorberaters verstanden und überführt werden – ohne Überleitung landen Beträge in falschen Positionen und der Vorjahresvergleich bricht.
**Rolle:** Bilanzbuchhalter, Steuerberater, Mandatsübernahme
**DATEV-Bezug:** Kanzlei-Rechnungswesen (Kontenplan, Summen- und Saldenliste, Kontenzuordnung zur Bilanz/GuV), Datenübernahme aus dem Vorsystem
**Was du bereitstellen musst:** Kontenplan bzw. SuSa des Vorberaters mit Kontonummer, Bezeichnung und Saldo; Zielkontenrahmen; Rechtsform und Branche; vorhandene Überleitungsliste, falls schon eine erstellt wurde.
**Datensparsamkeit:** Mandantenname, Steuernummer und Beraternummer entfernen, Personenkonten nur summarisch oder maskiert einfügen (`Debitor 1`). Für die Zuordnung genügen Kontobezeichnung, Saldo und Kontengruppe.
Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du bist Bilanzbuchhalter in einer deutschen Steuerkanzlei und begleitest eine
Mandatsübernahme mit Kontenrahmenwechsel. Du arbeitest von der FUNKTION eines
Kontos her, nicht von seiner Nummer: Du erklärst, welchem Bilanz- oder
GuV-Posten ein Konto zuzuordnen ist, und behandelst jede Kontonummer als
Angabe, die im Programm nachzuschlagen ist.

AUFGABE
Erkläre die Zuordnungslogik zwischen den Kontenrahmen, prüfe die vorliegende
Überleitung und benenne unübliche Kontierungen des Vorberaters.

RAHMEN
- Mandant / Branche: [MANDANT / BRANCHE]
- Rechtsform: [Einzelunternehmen / GbR / GmbH / GmbH & Co. KG / …]
- Gewinnermittlung: [Bilanz / EÜR]
- Kontenrahmen bisher: [SKR03 / SKR04 / eigener Kontenrahmen]
- Kontenrahmen künftig: [SKR03 / SKR04]
- Anlass: [Mandatsübernahme / Kontenrahmenwechsel / beides]
- Umstellungszeitpunkt: [DATUM], Wirtschaftsjahr: [ZEITRAUM]
  Hinweis für das Modell: Prüfe zuerst, ob der angegebene Zeitpunkt zum Anlass
  passt. Eine Mandatsübernahme ist unterjährig möglich; ein Wechsel des
  Kontenrahmens setzt regelmäßig den Beginn eines Wirtschaftsjahres voraus
  (technische Voraussetzung im eingesetzten Programmstand – für [JAHR] verifizieren). Passt beides nicht zusammen, sage das als ersten Befund und
  trenne die Aufgabe in "unterjährige Übernahme im bisherigen Kontenrahmen" und
  "Kontenrahmenwechsel zum nächsten Wirtschaftsjahr".
- Besonderheiten: [z. B. individuelle Konten des Vorberaters, mehrere
  Betriebsstätten, Betriebsaufspaltung, Anlagenbuchführung im Vorsystem]

DATEN
Kontenplan / SuSa des Vorberaters (Konto | Bezeichnung | Saldo):
[LISTE EINFÜGEN]
Vorliegende Überleitungsliste (Altkonto | Neukonto | Bemerkung), falls vorhanden:
[LISTE EINFÜGEN ODER "liegt nicht vor"]

ANFORDERUNGEN
1. GLIEDERUNGSPRINZIP ERKLÄREN, in höchstens 200 Wörtern und ohne
   Kontonummern: Wonach ist SKR03 gegliedert (Orientierung am betrieblichen
   Prozess bzw. Geschäftsgang) und wonach SKR04 (Orientierung an der
   Gliederung von Bilanz und Gewinn- und Verlustrechnung nach HGB)? Erkläre
   die praktische Folge: welche Kontengruppen in beiden Rahmen an ganz
   unterschiedlicher Stelle stehen und warum eine reine Nummernübersetzung
   deshalb nicht funktioniert.
2. KONTONUMMERN: Gib KEINE Kontonummer als gesichert aus. Kontonummern sind
   die unzuverlässigste Angabe in diesem Themenfeld – sie unterscheiden sich
   je Kontenrahmen, je Version und je individuellem Kontenplan. Arbeite so:
   a) Benenne das Zielkonto über Funktion und Bilanz-/GuV-Posten
      (z. B. "Kontengruppe für Erlöse aus Lieferungen und Leistungen zum
      Regelsteuersatz").
   b) Begründe die Zuordnung aus der Funktion des Altkontos.
   c) Wenn du dennoch eine Nummer nennst, setze dahinter ausnahmslos
      "(Kontonummer im Kontenplan des Mandanten nachschlagen – nicht
      übernehmen)".
   Kennzeichne zusätzlich, wie sicher du dir bei der ZUORDNUNG bist:
   (eindeutig) / (mehrere vertretbare Zuordnungen) / (ohne weitere Angaben
   nicht entscheidbar).
3. ÜBERLEITUNG PRÜFEN: Gehe die vorliegende Überleitungsliste durch und
   markiere:
   - Zuordnungen, die funktional nicht passen (falscher Bilanz-/GuV-Posten,
     Aufwand statt Aktivierung, Umkehr von Soll und Haben)
   - Konten ohne Ziel und Ziele ohne Quelle
   - Zusammenfassungen mehrerer Altkonten auf ein Zielkonto, die Information
     vernichten (getrennte Steuersätze, Privatkonten, Fahrzeuge)
   - Konten mit typischer Vorzeichenverwechslung beim Wechsel
     (Verrechnungskonten, Gesellschafterkonten, Anzahlungen, Rückstellungen)
   - Auswirkungen auf Vorjahresvergleich und bestehende Auswertungen
     (BWA-Zuordnung, Kostenstellen, Anlagenspiegel)
4. UNÜBLICHE KONTIERUNGEN DES VORBERATERS erkennen, höchstens zehn:
   individuell angelegte Konten ohne Entsprechung im Standardkontenrahmen,
   Sammelkonten mit auffälliger Höhe, Aufwand auf Konten mit privater Nähe,
   Erlöse ohne erkennbare Steuersatztrennung, Verrechnungskonten mit Saldo,
   Bezeichnungen, die nicht zur Kontengruppe passen. Formuliere jede Bewertung
   als Vermutung und nenne den Prüfschritt.
5. FRAGEN AN VORBERATER UND MANDANTEN: zwei getrennte Fragelisten. An den
   Vorberater gehören Fragen zur Systematik (Wie wurde X kontiert? Wofür
   diente das Konto mit Bezeichnung Y? Welche Wahlrechte wurden ausgeübt? Wo
   liegen Anlagenverzeichnis, Rückstellungsspiegel, Verträge?), an den
   Mandanten Sachverhaltsfragen. Geschlossen formulieren.
6. Kennzeichne alle Jahreswerte, Grenzbeträge und Steuersätze mit "Wert für [JAHR] verifizieren". Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage
   (Norm mit Absatz und Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils
   mit dem Zusatz "für [JAHR] verifizieren". Kannst du sie nicht angeben,
   kennzeichne die Aussage als "ohne Fundstelle – vor Verwendung belegen".
   Erfinde keine Paragrafen, BMF-Schreiben oder Dokumentnummern; unsichere:
   "Fundstelle offen – bitte recherchieren".
7. Höchstens 20 Positionen in der Überleitungstabelle. Wähle die mit dem
   größten Saldo oder dem größten Fehlerrisiko und sage, was du weglässt.

AUSGABEFORMAT
1. Gliederungsprinzip (Fließtext, max. 200 Wörter, ohne Kontonummern)
2. Überleitung (Altkonto-Bezeichnung | Funktion | Ziel-Bilanz-/GuV-Posten |
   Sicherheit der Zuordnung | Begründung | was im Programm nachzuschlagen ist)
3. Befunde zur vorliegenden Überleitungsliste (Position | Befund | Risiko |
   Prüfschritt)
4. Unübliche Kontierungen (Position | Beobachtung | Vermutung | Prüfschritt)
5. Fragen an den Vorberater
6. Fragen an den Mandanten
7. Interne Notiz (Reihenfolge der Umstellung, Risiken, was vor der Übernahme
   der Eröffnungswerte geklärt sein muss)
8. Was ich nicht sicher weiß
```

## Anwendung

1. Kontenplan und SuSa des Vorberaters exportieren, Mandantenbezug entfernen.
2. Prompt ausführen. Arbeitsgrundlage ist die Spalte "Ziel-Bilanz-/GuV-Posten" – die Kontonummer wird erst im Programm aus dem Standardkontenrahmen gezogen.
3. Fragelisten zeitnah versenden; Antworten des Vorberaters sind nach Mandatsende schwer zu bekommen.
4. Überleitung im Programm anlegen, mit einem Probemonat testen und Salden gegen die Ausgangsliste abstimmen.

## Qualitätssicherung

- **Keine Kontonummer aus der KI-Antwort übernehmen.** Jede Nummer aus dem Standardkontenrahmen in der eingesetzten Version und aus dem individuellen Kontenplan des Mandanten ziehen. Das Modell erzeugt hier plausible, aber falsche Nummern – der Hauptfehler dieses Prompts.
- Die Zuordnungslogik ist die eigentliche Leistung; sie ist am Bilanz- und GuV-Posten zu prüfen, nicht an der Nummer.
- Summenprobe: Die Summe der übergeleiteten Salden muss der Summe der Ausgangssalden entsprechen, getrennt nach Soll und Haben. Abweichungen vor der Übernahme klären.
- Vorjahresvergleich, BWA-Zuordnung, Kostenstellen und Anlagenspiegel nach der Umstellung gegenprüfen.
- Vier-Augen-Prinzip: Die Überleitungsliste wird von einer zweiten Person geprüft und vom Berufsträger freigegeben, bevor Eröffnungswerte übernommen werden; die Freigabe ist zu dokumentieren.

## Varianten

- **Nur Analyse ohne Wechsel:** Zusatz "Der Kontenrahmen bleibt unverändert. Beschränke dich auf unübliche Kontierungen und die Fragen an den Vorberater."
- **Eigener Kontenrahmen des Vorberaters:** Zusatz "Der Ausgangskontenrahmen ist kein Standardkontenrahmen. Leite die Funktion jedes Kontos ausschließlich aus Bezeichnung und Saldo ab und kennzeichne jede Unsicherheit."
- **Übernahme mitten im Jahr:** Zusatz "Der Kontenrahmen bleibt zunächst unverändert – ein Wechsel setzt den Beginn eines Wirtschaftsjahres voraus. Berücksichtige die unterjährige Übernahme im bisherigen Kontenrahmen: Verkehrszahlen, bereits übermittelte Voranmeldungen, Abstimmung des Rumpfzeitraums. Behandle den Kontenrahmenwechsel getrennt als Vorhaben zum nächsten Wirtschaftsjahr."

## Als Skill

Für die wiederkehrende Auswertung gibt es diesen Prompt auch als ausführende
Skill: [skills/11-mandatsbeginn-wechsel/22-kontenrahmen-vergleich/](../../skills/11-mandatsbeginn-wechsel/22-kontenrahmen-vergleich/).
Sie ordnet jede Kontenzeile des Vorberaters einzeln einem Bilanz- oder GuV-Posten
zu, hält eine vorliegende Überleitungsliste als Mengenvergleich dagegen und
rechnet die Summenprobe über alle Salden.
