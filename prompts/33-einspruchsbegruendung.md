# 33 – Einspruchsbegründung formulieren

**Problem:** Der Einspruch ist eingelegt, die Begründung bleibt liegen; wenn sie geschrieben wird, vermischen sich Sachverhalt, Meinung und halb erinnerte Rechtsprechung.
**Rolle:** Steuerberater, erfahrene Sachbearbeitung im Entwurf
**DATEV-Bezug:** DATEV Fristen und Bescheide, DATEV DMS, Schriftverkehr aus der Eigenorganisation
**Was du bereitstellen musst:** Bezeichnung des angefochtenen Bescheids, streitige Abweichung mit Beträgen, Sachverhalt, eigene Rechtsauffassung, Beweismittel, Angabe zur Vollstreckung.
**Datensparsamkeit:** Vor dem Einfügen Name, Anschrift, Steuernummer und Aktenzeichen durch Platzhalter ersetzen (`Mandant A`, `Steuernummer ****`). Die echten Kennzeichen setzt die Kanzlei erst in der Reinschrift ein. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und schreibst
Einspruchsbegründungen. Du trennst Sachverhalt und rechtliche Würdigung
strikt und behauptest nichts, was du nicht belegen kannst.

AUFGABE
Entwirf eine Einspruchsbegründung an das Finanzamt.

VORGANG
- Angefochtener Bescheid: [STEUERART], [VERANLAGUNGSZEITRAUM],
  Bescheiddatum [DATUM]
- Einspruch bereits eingelegt am: [DATUM / noch nicht]
- Streitige Position(en): [BEZEICHNUNG], erklärt [BETRAG], veranlagt [BETRAG]
- Begründung des Finanzamts laut Erläuterungstext: [WORTLAUT]
- Sachverhalt: [DARSTELLUNG, chronologisch]
- Eigene Rechtsauffassung: [WAS WIR MEINEN UND WARUM]
- Beweismittel: [VERTRÄGE / RECHNUNGEN / FAHRTENBUCH / ZEUGEN /
  KORRESPONDENZ – jeweils mit Bezeichnung und Datum]
- Vollstreckung / Zahlungsdruck: [Nachzahlung fällig am DATUM / keine /
  unbekannt]
- Aussetzung der Vollziehung gewünscht: [ja / nein / noch offen]
- Antragsziel: [WELCHER BETRAG ODER WELCHE FESTSTELLUNG SOLL GEÄNDERT WERDEN]

ANFORDERUNGEN
0. Ist oben "noch nicht" angegeben, beginne die Ausgabe mit einem hervorgehobenen
   Vorrangsatz: "Vor jeder Begründung ist der fristwahrende Einspruch einzulegen
   (§ 355, § 357 AO – für [JAHR] verifizieren). Die Einspruchsfrist ist von einem
   Menschen zu berechnen und im Fristenprogramm zu erfassen." Erzeuge in diesem
   Fall zuerst einen kurzen fristwahrenden Einspruch ohne Begründung, danach die
   Begründung als getrennten Entwurf.
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab: trägt der gelieferte
   Sachverhalt die Rechtsauffassung? Benenne fehlende Angaben und fehlende
   Beweismittel, statt sie zu ergänzen.
2. Trenne strikt: Im Abschnitt "Sachverhalt" steht nur, was tatsächlich
   geschehen ist. Bewertungen, Schlussfolgerungen und Rechtsansichten gehören
   ausschließlich in die rechtliche Würdigung.
3. Erfinde NICHTS. Insbesondere keine Aktenzeichen, keine BFH- oder
   FG-Entscheidungen, keine BMF-Schreiben, keine Randziffern, keine
   Fundstellen aus Kommentaren. Wenn dir zu einem Punkt keine sichere
   Fundstelle bekannt ist, schreibe: "Fundstelle offen – bitte recherchieren".
4. Nenne zu jedem Prüfungsschritt und zu jeder rechtlichen Aussage die
   einschlägige Rechtsgrundlage. JEDE genannte Fundstelle – auch jeder Paragraf –
   wird im Text mit "(für [JAHR] verifizieren)" markiert UND zusätzlich in der
   Tabelle "Zu verifizierende Rechtsgrundlagen" am Ende mit der Spalte
   "geprüft von (leer)" geführt. Mindestens zu nennen, soweit im Fall berührt:
   § 347 AO, § 355 AO, § 357 AO, § 361 AO, § 240 AO, § 69 FGO. Bist du dir einer
   Fundstelle nicht sicher, schreibe "Fundstelle offen – bitte recherchieren"
   statt einer Angabe.
5. Nenne keine jahresabhängigen Werte ohne die Kennzeichnung
   "Wert – für [JAHR] verifizieren".
6. Berechne KEINE Fristen und nenne kein Fristende. Weise nur darauf hin,
   welche Fristen im Raum stehen und dass sie von einem Menschen zu berechnen
   und im Fristenprogramm zu führen sind.
7. Der Antrag auf Aussetzung der Vollziehung ist ein GETRENNTER Punkt mit
   eigener Überschrift und eigener Begründung. Er wird nicht in die
   Einspruchsbegründung eingeflochten. Wenn oben "noch offen" steht, formuliere
   ihn als Entscheidungsvorlage, nicht als fertigen Antrag.
7a. Weise im Abschnitt zur Aussetzung der Vollziehung ausdrücklich darauf hin,
    dass der Einspruch die Vollziehung nicht hemmt (§ 361 Abs. 1 AO – für [JAHR]
    verifizieren), dass die Nachzahlung ohne Aussetzung fällig bleibt und
    Säumniszuschläge entstehen können (§ 240 AO – für [JAHR] verifizieren).
    Ordne die Zuständigkeit zu: Antrag bei der Finanzbehörde nach § 361 Abs. 2 AO;
    gerichtlicher Antrag erst nachrangig nach § 69 FGO. Behaupte nicht, dass
    Aussetzung gewährt wird.
8. Ton: sachlich, ohne Vorwurf gegenüber dem Finanzamt, ohne Ironie, ohne
   Verstärker ("eindeutig", "offensichtlich", "zweifelsfrei").
9. Höchstens 700 Wörter für den Entwurf. Lass alles weg, was den Streitpunkt
   nicht trägt.

AUSGABEFORMAT
1. (Entwurf) in dieser Gliederung:
   a) Bezeichnung des angefochtenen Bescheids
   b) Antrag – was genau begehrt wird, mit Betrag
   c) Sachverhalt – nur Tatsachen, chronologisch
   d) Rechtliche Würdigung – Argumentation, jede Fundstelle markiert
   e) Beweismittel – nummeriert, mit Bezug zu den Punkten des Sachverhalts
2. (Antrag auf Aussetzung der Vollziehung) – getrennter Abschnitt, nur wenn
   oben angefordert oder offen.
3. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle laut Entwurf | wofür sie im Text steht | geprüft von (leer)
4. (Lücken im Sachverhalt) – was noch belegt werden muss.
5. (Interne Notiz) – nicht ans Finanzamt: Erfolgsaussicht als Einschätzung,
   Risiko der Verböserung, Alternativen zum Einspruch, Wiedervorlage.
```

## Anwendung

1. Sachverhalt aus der Akte zusammenstellen, nicht aus dem Gedächtnis. Was hier ungenau ist, wird im Entwurf glatt formuliert und liest sich dadurch verlässlicher, als es ist.
2. Beweismittel mit Bezeichnung und Datum eintragen; "diverse Belege" erzeugt einen wertlosen Abschnitt.
3. Entwurf gegen Bescheid und Erläuterungstext legen. Fundstellenliste abarbeiten und abgezeichnet zur Akte nehmen.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Ausgangsdokuments nachgeprüft und abgezeichnet** – bei Rechtsbehelfsfristen ausnahmslos, unabhängig davon, ob ein Rechtsbehelf geplant ist. Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Jede Fundstelle wird einzeln nachgeschlagen.** Sprachmodelle erfinden Aktenzeichen und Datumsangaben von Entscheidungen in überzeugender Form. Kein unverifiziertes Zitat verlässt die Kanzlei.
- **Fristen werden von einem Menschen berechnet und geprüft**, insbesondere Einspruchsfrist und die Frist zur Begründung, soweit eine gesetzt wurde. Der Entwurf ersetzt keinen Fristeneintrag.
- **Freigabe durch einen Berufsträger** ist zwingend – die Begründung bindet die Argumentation im weiteren Verfahren.
- Prüfen, ob im Abschnitt "Sachverhalt" Wertungen stehen. Das ist der häufigste Mangel und schwächt die Begründung.
- Risiko der Verböserung vor dem Versand bewerten und dokumentieren.
- Aussetzung der Vollziehung nie stillschweigend mitbeantragen; sie ist eine eigene Entscheidung mit eigenen Folgen.

## Varianten

- **Nur Sachverhalt:** "Erzeuge ausschließlich den Sachverhaltsteil, streng ohne Wertung, und liste getrennt auf, welche Sätze du als Wertung gestrichen hast."
- **Gegenargumente:** "Formuliere die drei stärksten Argumente, die das Finanzamt gegen unsere Auffassung vorbringen wird."
- **Rücknahmeentscheidung:** "Erzeuge eine Entscheidungsvorlage zur Frage, ob der Einspruch aufrechterhalten wird – mit Kriterien statt Empfehlung."
