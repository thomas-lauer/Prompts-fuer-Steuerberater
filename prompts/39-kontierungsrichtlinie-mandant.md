# 39 – Kontierungsrichtlinie für den Mandanten erstellen

**Problem:** Beim Mandanten sortiert jeder nach eigenem Gefühl, die Kanzlei korrigiert Monat für Monat dieselben Fälle – und fällt die eine Person aus, die "es immer gemacht hat", steht die Belegvorbereitung still.
**Rolle:** Steuerberater, Buchhaltung, Kanzleileitung
**DATEV-Bezug:** DATEV Unternehmen online (Belege online, Belegtransfer, Kassenbuch online), Kanzlei-Rechnungswesen, DATEV Buchungsdatenservice
**Was du bereitstellen musst:** Branche und Geschäftsmodell, die typischen wiederkehrenden Geschäftsvorfälle, die Fälle, die zuletzt korrigiert werden mussten, wer beim Mandanten mit Belegen arbeitet und wer freigibt.
**Datensparsamkeit:** Keine Klarnamen, keine Lieferantennamen mit Preisbezug, keine Kontonummern des Mandanten. Beschäftigte als `Mitarbeiter 1`, `Assistenz`, `Geschäftsführung`. Es genügen Sachverhaltstypen, nicht die Einzelbelege.
Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du bist erfahrene Kanzleimitarbeiterin und schreibst Arbeitsanweisungen für
die Beschäftigten von Mandanten. Du schreibst für Menschen ohne
Buchhaltungsausbildung: kurze Sätze, Alltagssprache, jeder Fachbegriff in
einem Halbsatz erklärt. Eine Richtlinie wird nur befolgt, wenn sie sagt,
was zu TUN ist – nicht, was steuerlich gilt.

AUFGABE
Erstelle eine Kontierungsrichtlinie für die Beschäftigten des Mandanten. Sie
beschreibt, welcher Geschäftsvorfall zu welcher SACHVERHALTSKATEGORIE gehört
und was auf den Beleg geschrieben wird.

WICHTIG: Arbeite bewusst OHNE Kontonummern. Die Richtlinie ordnet
Sachverhalte zu; die Zuordnung zu Konten ergänzt die Kanzlei in einer
eigenen Spalte. Erfinde keine Kontonummern und keine Kontenbezeichnungen,
auch nicht beispielhaft.

MANDANTENRAHMEN
- Branche und Geschäftsmodell: [ANGABE]
- Rechtsform: [ANGABE], Gewinnermittlung: [Bilanz / EÜR]
- Umsatzsteuer: [Regelbesteuerung / Kleinunternehmer § 19 UStG / teilweise
  steuerfreie Umsätze / Ist-Versteuerung]
- Besonderheiten: [z. B. Reverse-Charge-Eingänge, innergemeinschaftliche
  Erwerbe, Bauleistungen, gemischte Nutzung]
- Kontenrahmen (nur zur Information, NICHT verwenden): [SKR03 / SKR04]
- Belegformate: [Papier / PDF / E-Rechnung im strukturierten Format / gemischt],
  Belegsystem mit Notiz- oder Kommentarfunktion: [ja / nein / unbekannt]
- Rollen im Belegprozess: [z. B. Assistenz erfasst, Meister prüft sachlich,
  Geschäftsführung gibt frei], Vertretung geregelt: [ja / nein]

TYPISCHE GESCHÄFTSVORFÄLLE
[LISTE, z. B. Wareneinkauf, Material für Kundenaufträge, Werkzeug,
 Tankbelege, Bewirtung, Reisekosten, Miete, Versicherungen, Leasing,
 Software-Abonnements, Reparaturen, Anschaffungen, Privatentnahmen]

WAS ZULETZT KORRIGIERT WERDEN MUSSTE
[LISTE DER FEHLER DER LETZTEN MONATE – die Richtlinie muss genau diese
 Fälle abdecken]

ARBEITSWEISE
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben.
2. Nimm NUR Sachverhalte auf, die hier vorkommen. Lasse alles Übrige weg.
3. Jede Zeile ist eine Handlungsanweisung, keine Rechtsauskunft.
4. Formuliere Abgrenzungen so, wie sie im Betrieb erkennbar sind (woran
   sieht die Person das am Beleg?), nicht nach Kriterien, die am Beleg
   nicht ablesbar sind.

INHALT
A. ZWECK UND GELTUNG – wofür, für wen, ab wann, wer pflegt sie.
B. GRUNDREGELN FÜR JEDEN BELEG – kein Beleg ohne Sachverhaltskategorie,
   ohne Eingangsdatum, ohne Zuordnung; Original nicht verändern,
   Ergänzungen nur als solche kenntlich.
C. ZUORDNUNGSTABELLE – Spalten: Geschäftsvorfall (Alltagssprache) | Woran
   erkenne ich ihn | Sachverhaltskategorie | Was zusätzlich auf den Beleg
   gehört | Konto (von der Kanzlei auszufüllen).
   Behandle die klassischen Verwechslungen, soweit sie hier vorkommen:
   Material für Kundenaufträge gegen Verbrauchsmaterial des Betriebs;
   Reparatur gegen Anschaffung; Anschaffung gegen geringwertiges
   Wirtschaftsgut (Betragsgrenze NICHT nennen, sondern "Betragsgrenze – für
   [JAHR] verifizieren, von der Kanzlei bestätigen lassen"); Bewirtung von
   Geschäftspartnern gegen Verpflegung eigener Beschäftigter; betrieblich
   gegen privat veranlasst; Anzahlung gegen Schlussrechnung; Kaution gegen
   Aufwand.
D. ANGABEN ZUM BELEG – Anlass, Auftrags- oder Projektbezug, Zahlungsweg,
   bei Bewirtung Teilnehmer und konkreter Anlass, bei Reisen der Reisezweck.
   Ein Beleg ohne diese Angaben ist nicht fertig und wird nicht weitergegeben.
   Gib die Anweisung getrennt für zwei Wege aus:
   (1) Papier und PDF: Angaben auf dem Beleg oder auf einem angehefteten
       Zusatzbeleg, Original nicht verändern.
   (2) Elektronische Rechnungen im strukturierten Format: NICHT im Datensatz
       ändern, keine Angaben auf einem Ausdruck. Die Angaben gehören in die
       Notiz- oder Kommentarfunktion des Belegsystems bzw. auf einen verknüpften
       Zusatzbeleg. Ist keine solche Funktion benannt, gehört dieser Punkt in die
       Lückenliste, nicht in die Richtlinie.
E. ZWEIFELSFÄLLE – DIE WICHTIGSTE REGEL
   Wer unsicher ist, RÄT NICHT. Der Beleg kommt in eine klar benannte
   Sammelposition für ungeklärte Vorgänge und wird der Kanzlei mit einer
   kurzen Frage vorgelegt. Beschreibe: wie die Sammelposition heißt, wo sie
   liegt, was auf den Zettel geschrieben wird, wer wann nachfragt, wie die
   Antwort zurückkommt und wo sie festgehalten wird, damit derselbe Fall
   beim nächsten Mal geklärt ist.
   Nenne Beispiele für "nie selbst entscheiden": alles mit Auslandsbezug,
   Reverse-Charge, Bauleistungen, Zuwendungen an Beschäftigte, Fahrzeuge und
   ihre private Nutzung, Anschaffungen über der Betragsgrenze, Verträge mit
   nahestehenden Personen, alles auf Gesellschafterebene.
F. FREIGABE UND VERTRETUNG – wer prüft sachlich, wer gibt frei, wer vertritt
   wen, was gilt bei Abwesenheit (Rollen, keine Klarnamen).
G. TERMINE – bis wann Belege je Periode bei der Kanzlei sind, was bei
   Nachzüglern gilt.

ANFORDERUNGEN
- Nenne KEINE Kontonummern und keine Betragsgrenzen. Wo eine Grenze relevant
  ist: "Betragsgrenze – für [JAHR] verifizieren, von der Kanzlei bestätigen
  lassen".
- Kennzeichne jede unsichere Aussage. Rate nicht.
- Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
  Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
  "für [JAHR] verifizieren". Kannst du sie nicht angeben, kennzeichne die Aussage
  als "ohne Fundstelle – vor Verwendung belegen". Erfinde keine Paragrafen,
  BMF-Schreiben oder Dokumentnummern; unsichere: "Fundstelle offen – bitte
  recherchieren".
- Höchstens 25 Zeilen in der Zuordnungstabelle. Wähle die Vorfälle mit der
  größten Häufigkeit oder Fehleranfälligkeit. Ignoriere den Rest bewusst.
- Keine Paragrafen im Text der Richtlinie; Rechtsgrundlagen nur intern.

AUSGABEFORMAT
1. Kontierungsrichtlinie, Abschnitte A–G
2. Zweifelsfallliste: Fall | warum zweifelhaft | wer entscheidet | welche
   Angabe die Kanzlei dafür braucht
3. Lückenliste: Nr. | Lücke | warum sie die Richtlinie blockiert | wer klärt |
   Antwort des Mandanten (leer)
4. Interne Notiz einschließlich Fundstellenliste: zu jeder Aussage der
   Richtlinie die Rechtsgrundlage, die die Kanzlei prüft (im Text an den
   Mandanten erscheinen weiterhin keine Paragrafen); außerdem welche Zuordnungen
   die Kanzlei fachlich prüfen und mit Konten hinterlegen muss, welche
   Sachverhalte auf ein ungelöstes steuerliches Thema hindeuten, welche Fehler
   die Richtlinie NICHT verhindern kann
5. "Was ich nicht sicher weiß"
```

## Anwendung

1. Die Liste der zuletzt korrigierten Fälle aus den tatsächlichen Umbuchungen der letzten drei bis sechs Monate ziehen, nicht aus dem Gedächtnis. Ohne sie entsteht eine allgemeine Richtlinie, die nichts verhindert.
2. Die Spalte "Konto" in der Kanzlei ausfüllen und erst die fertige Fassung übergeben. Die Kontenzuordnung ist Kanzleiarbeit.
3. Die Richtlinie mit der Person durchgehen, die die Belege tatsächlich vorbereitet – und mit der Vertretung. Genau dafür existiert sie.
4. Nach zwei bis drei Monaten prüfen, welche Korrekturen weiterhin anfallen, und die Tabelle ergänzen.

## Qualitätssicherung

- **Rechtsstand prüfen an:** den aktuellen DATEV-Unterlagen zu SKR03/SKR04 für die Kontenzuordnung sowie für Belegangaben, Belegsicherung und zeitgerechte Erfassung an: GoBD, BMF-Schreiben vom 28.11.2019, zuletzt geändert durch BMF-Schreiben vom 14.07.2025 (Fassung und Änderungsstand für [JAHR] verifizieren – die GoBD wurden bereits zweimal geändert). Betragsgrenzen – etwa für geringwertige Wirtschaftsgüter – im aktuellen Gesetzestext nachschlagen, nie aus dem Modellergebnis übernehmen.
- Jede Zeile darauf prüfen, ob das Erkennungsmerkmal am Beleg wirklich sichtbar ist. Kriterien, die nur die Kanzlei beurteilen kann, gehören in die Zweifelsfallliste.
- Prüfen, ob die Richtlinie umsatzsteuerliche Sachverhalte dem Mandanten überlässt, die er nicht entscheiden darf – Auslandsbezug, Reverse-Charge und Bauleistungen gehören ausnahmslos in die Sammelposition.
- Kontrollieren, dass keine Kontonummern in den Entwurf gerutscht sind; Modelle ergänzen sie ungefragt und häufig falsch.
- Vier-Augen-Prinzip: Freigabe durch einen Berufsträger, weil die Richtlinie das Verhalten des Mandanten dauerhaft steuert.

## Varianten

- **Kurzfassung:** "Erzeuge eine einseitige Fassung mit den zehn häufigsten Vorfällen zum Aushang am Arbeitsplatz."
- **Einarbeitung:** "Erzeuge eine Einweisung für eine neue Kraft, die noch nie Belege vorbereitet hat – mit fünf Übungsfällen und Musterlösung."
- **Kassenbezug:** "Ergänze einen Abschnitt für Barbelege und die Schnittstelle zum Kassenbuch."
- **Rückmeldeschleife:** "Erzeuge aus den Umbuchungen des letzten Quartals eine Liste der offenbar nicht befolgten Regeln, je mit einer als Vermutung gekennzeichneten Ursache."
