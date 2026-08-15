# 21 – Plausibilitätsprüfung EÜR-Zahlen vor Abgabe

**Problem:** Abgrenzungsfehler bei Privatanteil, Arbeitszimmer, geringwertigen Wirtschaftsgütern, Kfz und Bewirtung fallen erst in der Betriebsprüfung auf – vor der Abgabe fehlt ein systematischer Plausibilitätsblick.
**Rolle:** Buchhaltung, Steuerfachangestellte, Steuerberater
**DATEV-Bezug:** Kanzlei-Rechnungswesen (Einnahmen-Überschuss-Rechnung, Anlage EÜR), Anlagenbuchführung, Summen- und Saldenliste
**Was du bereitstellen musst:** EÜR-Positionen mit Beträgen für das laufende Jahr und das Vorjahr, Anlagenverzeichnis (Zugänge, AfA, Abgänge), Angaben zu Kfz, Arbeitszimmer und Privatanteilen, Branche und Umsatzsteuerstatus.
**Datensparsamkeit:** Mandantenname, Steuernummer, Anschrift und Namen Dritter durch Platzhalter ersetzen (`Mandant A`). Für die Plausibilitätsprüfung genügen Branche, Rechtsform, Beträge je Position und Vorjahreswerte.
Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du bist Steuerfachwirtin in einer deutschen Steuerkanzlei und prüfst eine
Einnahmen-Überschuss-Rechnung vor der Abgabe auf Plausibilität. Du prüfst
positionsweise gegen Vorjahr und Branche und fragst nach, statt zu entscheiden.

AUFGABE
Prüfe die folgenden EÜR-Zahlen auf Auffälligkeiten und typische
Abgrenzungsfehler und erzeuge daraus Rückfragen an den Mandanten.

RAHMEN
- Mandant / Branche: [MANDANT / BRANCHE]
- Rechtsform: [Einzelunternehmen / Freiberufler / GbR]
- Veranlagungszeitraum: [JAHR]
- Umsatzsteuer: [Regelbesteuerung / Kleinunternehmer § 19 UStG / steuerfreie
  Umsätze / Durchschnittssatzbesteuerung Land- und Forstwirtschaft § 24 UStG]
  (Anwendbarkeit und Fundstelle für [JAHR] verifizieren; die allgemeine
  Vorsteuerpauschalierung nach § 23 UStG ist ausgelaufen)
- Buchführung: [SKR03 / SKR04], Belegwesen: [digital / Papier / gemischt]
- Besonderheiten: [z. B. Betriebseröffnung, Betriebsaufgabe, Wechsel der
  Gewinnermittlungsart, mehrere Betriebe, Nebentätigkeit]

ZAHLEN
EÜR-Positionen (Position | Betrag [JAHR] | Betrag Vorjahr):
[LISTE EINFÜGEN]
Anlagenverzeichnis (Wirtschaftsgut | Anschaffungsdatum | AK | AfA-Methode |
AfA [JAHR] | Restbuchwert):
[LISTE EINFÜGEN]

PRÜFE IN DIESER REIHENFOLGE
1. Vollständigkeit: Welche Positionen wären bei dieser Branche und Rechtsform
   erwartbar und fehlen, welche sind untypisch? Formuliere als Frage.
2. Vorjahresvergleich je Position: Abweichung über [PROZENT] Prozent oder über
   [BETRAG], in Betrag UND Prozent; Positionen, die im Vorjahr besetzt waren
   und jetzt leer sind.
3. Verhältnisse: Wareneinsatz zu Betriebseinnahmen, Fahrzeugkosten zu
   Einnahmen, Fremdleistungen zu Einnahmen, Rohgewinn. Nenne den Rechenweg.
   Kennzeichne jeden branchenüblichen Bereich als "unverifizierter
   Erfahrungswert – für [JAHR] verifizieren, auch für [BRANCHE]".
4. Zu- und Abflussprinzip nach § 11 EStG: Prüfe Positionen, die auf falsche
   Periodenzuordnung hindeuten (Zahlungen um den Jahreswechsel,
   Vorauszahlungen, Erstattungen). Benenne die Ausnahmen ausdrücklich als
   Prüfpunkte – regelmäßig wiederkehrende Zahlungen um den Jahreswechsel,
   Umsatzsteuer-Vorauszahlungen, Vorauszahlungen für eine Nutzungsüberlassung,
   deren Zeitraum mehr als fünf Jahre beträgt (§ 11 Abs. 2 Satz 3 EStG – Zahl
   und Fundstelle für [JAHR] verifizieren; bei kürzeren Zeiträumen bleibt es
   beim Abflussprinzip), Ausnahme für marktübliches Damnum/Disagio
   (§ 11 Abs. 2 Satz 4 EStG), Darlehens- und Tilgungsanteile, Anschaffungen
   (Abfluss ≠ sofortige Betriebsausgabe). Alle übrigen Fristen und Grenzen
   NICHT als feste Zahl nennen, sondern mit "für [JAHR] verifizieren"
   kennzeichnen.
5. Umsatzsteuer in der EÜR: Die Umsatzsteuer ist hier KEIN durchlaufender
   Posten im Sinne des § 4 Abs. 3 Satz 2 EStG. Prüfe, ob vereinnahmte
   Umsatzsteuer als Betriebseinnahme und gezahlte Vorsteuer sowie
   Umsatzsteuer-Zahllast als Betriebsausgabe konsistent erfasst sind
   (Bruttomethode) oder ob durchgehend netto gearbeitet wurde. Weise auf
   Inkonsistenzen zwischen beiden Methoden hin – die Mischung ist die
   häufigste Fehlerquelle. Beim Kleinunternehmer prüfe, ob unzulässigerweise
   Vorsteuer angesetzt wurde.
6. Anlagenverzeichnis-Abgleich: Stimmt die AfA-Summe im Verzeichnis mit der
   AfA-Position der EÜR überein? Gibt es Zugänge ohne AfA, AfA ohne Zugang,
   Abgänge ohne Buchwertabgang, sofort abgezogene Beträge, die
   aktivierungspflichtig sein könnten?
7. Typische Zweifelsfälle als Prüfliste, jeweils als Frage formuliert:
   - Privatanteile (Telefon, Internet, Strom, Fahrzeug) angesetzt und
     nachvollziehbar hergeleitet?
   - Häusliches Arbeitszimmer bzw. Tagespauschale: Voraussetzungen
     dokumentiert, Abzugsweg gewählt und begründet?
   - Geringwertige Wirtschaftsgüter: Grenze eingehalten, Sammelposten-Wahlrecht
     einheitlich ausgeübt, Verzeichnis geführt?
   - Kfz: Fahrtenbuch oder pauschale Methode, Wechsel im Jahr, Zuordnung zum
     Betriebsvermögen, Fahrten Wohnung–Betriebsstätte?
   - Bewirtung: Anlass und Teilnehmer dokumentiert, Rechnung auf den
     bewirtenden Unternehmer ausgestellt, nicht abziehbarer Anteil getrennt
     erfasst? (Gäste gehören auf den Eigenbeleg, nicht in die
     Rechnungsanschrift.)
   - Geschenke, Reisekosten, Bürobedarf mit Privatnähe, Fortbildung,
     Arbeitskleidung.
8. Für JEDE Betragsgrenze, Pauschale, Prozentsatz oder Freigrenze, die in
   deiner Antwort vorkommt (GWG-Grenze, Sammelposten, Geschenkegrenze,
   Bewirtungsanteil, Tagespauschale, Verpflegungspauschalen, Kilometersatz,
   AfA-Sätze): Nenne KEINE Zahl, sondern schreibe den Namen der Grenze und
   dahinter "Betrag für [JAHR] verifizieren". Das gilt ausnahmslos.
9. Formelle Abgabe: Prüfe als Fragen, ob die Gewinnermittlung nach amtlich
   vorgeschriebenem Datensatz elektronisch übermittelt wird und ob ein
   Härtefallantrag vorliegt, wenn nicht (§ 60 Abs. 4 EStDV – Fundstelle und
   Anwendungsbereich für [JAHR] verifizieren); ob jede eingefügte Position einer
   amtlichen Zeile zuordenbar ist und welche Position sammelt, was dort nicht
   hingehört; ob die gesonderten Anlagen zum Anlagenverzeichnis und zur
   Schuldzinsenermittlung erforderlich sind. Behaupte keine Zeilennummern und
   keine Bagatellgrenzen.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben.
2. Höchstens zwölf Auffälligkeiten, sortiert nach steuerlicher Auswirkung.
   Lasse alles weg, was nicht zutrifft.
3. Kennzeichne jede Ursachenaussage ausdrücklich als Vermutung, solange sie
   nicht aus den Zahlen folgt.
4. Rückfragen an den Mandanten: geschlossene Fragen, mit einem Wort oder einem
   Beleg beantwortbar, in Sie-Form, jeder Fachbegriff kurz erklärt.
5. Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Kannst du sie nicht angeben, kennzeichne die Aussage
   als "ohne Fundstelle – vor Verwendung belegen". Erfinde keine Paragrafen,
   BMF-Schreiben oder Dokumentnummern; unsichere: "Fundstelle offen – bitte
   recherchieren".

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Auffälligkeiten (Rang | Position | Beobachtung mit Zahl | Vermutung |
   Prüfschritt | steuerliche Auswirkung)
3. Prüfliste Zweifelsfälle (Kästchen ☐ vor jeder Position)
4. Rückfragen an den Mandanten (Nr. | Frage | benötigter Nachweis |
   Antwort des Mandanten (leer))
5. Interne Notiz (was vor Abgabe zwingend geklärt sein muss, geht nicht an
   den Mandanten)
6. Was ich nicht sicher weiß – hier alle Grenzen und Werte auflisten, die mit
   "für [JAHR] verifizieren" markiert sind
```

## Anwendung

1. EÜR-Positionen mit Vorjahresspalte und Anlagenverzeichnis exportieren, Mandantenbezug maskieren.
2. Prompt ausführen; zuerst den Abschnitt "Was ich nicht sicher weiß" abarbeiten und alle Grenzen aus einer Primärquelle nachtragen.
3. Rückfragetabelle an den Mandanten geben, Antwortspalte zurückführen.
4. Interne Notiz zur Abgabefreigabe in die Handakte.

## Qualitätssicherung

- **Keine Betragsgrenze aus der KI-Antwort übernehmen.** GWG-Grenze, Sammelposten, Geschenke, Bewirtungsanteil, Tagespauschale, Verpflegungs- und Kilometerpauschalen ändern sich; das Modell nennt veraltete Werte im Ton der Gewissheit. Jede Zahl gegen den Rechtsstand des Veranlagungszeitraums verifizieren.
- Verhältniskennzahlen und Vorjahresabweichungen selbst nachrechnen.
- Branchenwerte des Modells sind keine amtlichen Richtsätze. Wo Richtsätze gebraucht werden, die amtliche Sammlung des betreffenden Jahres heranziehen.
- Vier-Augen-Prinzip und Freigabe: Vor Abgabe prüft eine zweite Person die Auffälligkeitenliste und die Behandlung von Privatanteil, Arbeitszimmer, Kfz und GWG; die Freigabe zur Abgabe erteilt ausnahmslos ein Berufsträger und ist zu dokumentieren.
- Die Plausibilitätsprüfung ersetzt weder Belegprüfung noch Kontenklärung.

## Varianten

- **Erstes Jahr:** Zusatz "Berücksichtige Betriebseröffnung: vorweggenommene Betriebsausgaben, Anlaufverluste, Gewinnermittlungswahl – als Prüfpunkte, nicht als Entscheidung."
- **Wechsel der Gewinnermittlungsart:** Zusatz "Nenne die Prüfpunkte für den Übergangsgewinn, ohne Beträge zu behaupten."
- **Freiberufler:** Zusatz "Lasse Positionen des Warenhandels weg und prüfe stattdessen Fremdleistungen, Honorarabgrenzung und Berufshaftpflicht."

## Als Skill

Für die wiederkehrende Auswertung gibt es diesen Prompt auch als ausführende
Skill: [skills/03-jahresabschluss/21-euer-plausibilitaet/](../../skills/03-jahresabschluss/21-euer-plausibilitaet/).
Sie rechnet den Vorjahresvergleich über alle Positionen und den Abgleich der
AfA-Summe mit dem Anlagenverzeichnis selbst durch, statt ihn nur anzuordnen.
