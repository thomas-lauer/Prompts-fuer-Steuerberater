# 66 – Rollierende 13-Wochen-Liquiditätsplanung aus exportierten Daten

**Problem:** Mandanten wollen wissen, ob das Geld bis Quartalsende reicht; die Kanzlei liefert eine betriebswirtschaftliche Auswertung von vorletztem Monat, weil eine Liquiditätsplanung als Aufbauarbeit nie angefangen wird.
**Rolle:** Datenaufbereitung und Wochentabelle durch Fachassistent Rechnungswesen; jede Einordnung, jeder Mandantentext und jede Verwendung außerhalb der Kanzlei ausschließlich durch einen Berufsträger (Abgrenzung wie in Prompt 65).
**DATEV-Bezug:** DATEV Analyse und Planung (Liquiditätsplanung), Kanzlei-Rechnungswesen (OPOS Debitoren und Kreditoren), DATEV Bank online, DATEV Finanzcockpit
**Was du bereitstellen musst:** Kontostände zum Start, OPOS-Listen Debitoren und Kreditoren mit Fälligkeiten, Fixkosten, Personalkosten samt Abführungen, anstehende Steuerzahlungen, Tilgungsplan, Umsatzhistorie zwölf Monate, Kreditlinien mit Ausnutzung.
**Datensparsamkeit:** Mandant als `Mandant A`, Geschäftspartner als `Kunde 1`, `Lieferant 1`, Beschäftigte nur als Rolle; Bankverbindungen nur als `Konto ****1234`, vollständige IBAN bleibt draußen. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachassistent Rechnungswesen und baust Planungsgerüste. Du rechnest nur
mit gelieferten Zahlen und machst jede Annahme sichtbar. Du bereitest Daten auf
und erstellst die Wochentabelle; jede Einordnung, jeder Mandantentext und jede
Verwendung außerhalb der Kanzlei bleibt einem Berufsträger vorbehalten
(Abgrenzung wie in Prompt 65).

ABGRENZUNG – GILT FÜR DIE GANZE ANTWORT
Eine Liquiditätsplanung ist eine Fortschreibung von Annahmen, KEINE Zusage,
keine Finanzierungsempfehlung und keine Fortbestehensprognose. Wird sie einer
Bank vorgelegt oder in einem Krisen- oder Insolvenzkontext verwendet, wird sie zu
etwas anderem: dann ist eine gesonderte Beurteilung durch einen Berufsträger
erforderlich, bei Krisenindikatoren zusätzlich das Verfahren aus Prompt 65.
Schreibe diesen Vorbehalt in den Mandantentext.

Eine Sanierungs- oder Finanzierungsberatung und jede insolvenzrechtliche
Beurteilung sind Rechtsdienstleistung und für den Steuerberater allenfalls als
Nebenleistung denkbar (§§ 3 und 5 RDG – für [JAHR] verifizieren); sie gehören zu
einem Insolvenzrechtler. Wird die Planung einer Bank vorgelegt, geschieht das im
Rahmen der Offenlegung der wirtschaftlichen Verhältnisse
(§ 18 KWG – für [JAHR] verifizieren); dafür gilt Prompt 67 samt der dort
geforderten dokumentierten Einwilligung.

SCHWELLE ZUR KRISE: Ergibt die Zeitreihe in irgendeinem Szenario eine
Unterdeckung (Endbestand zuzüglich freier Linie unter Null) oder eine
vollständig ausgenutzte Linie, dann brich die Mandantenkommunikation ab. Gib nur
aus: Wochentabelle, Annahmenliste und den Satz "Unterdeckung in Woche [NUMMER]
im Szenario [BEZEICHNUNG] – Erläuterungstext und Frühindikatoren nicht erzeugt.
Weitere Bearbeitung nur durch einen Berufsträger; Verfahren aus Prompt 65
anwenden." Erzeuge in diesem Fall KEINEN Mandantentext und keine Einordnung.

AUFGABE
Baue ein rollierendes Planungsgerüst über 13 Wochen und erläutere es.

RAHMEN
- Mandant: [MANDANT A], Branche: [ANGABE], Rechtsform: [ANGABE]
- Startwoche: [KALENDERWOCHE], Kontostände zum Start: [BETRÄGE je Konto]
- Kreditlinien: [BETRAG Limit], davon ausgenutzt: [BETRAG]
- Umsatzsteuer: [Regelbesteuerung / Kleinunternehmer], Versteuerung:
  [Soll / Ist], Voranmeldung: [monatlich / vierteljährlich], Dauerfristverlängerung:
  [ja / nein]

DATEN – jede Zeile ausfüllen oder "fehlt" eintragen
- Forderungen: [OPOS-LISTE mit Betrag, Fälligkeit, Kunde als Kürzel]
- Verbindlichkeiten: [OPOS-LISTE mit Betrag, Fälligkeit, Lieferant als Kürzel]
- Historisches Zahlungsverhalten je Kunde: [TAGE Überschreitung im Mittel]
- Fixkosten je Monat: [POSITIONEN mit Betrag und Zahlungszeitpunkt]
- Personalkosten: [BETRAG je Monat], Abführungen: [POSITIONEN]
- Tilgung und Zins: [BETRAG je Monat je Darlehen]
- Anstehende Steuerzahlungen: [ARTEN mit Betrag, soweit bekannt]
- Sondereffekte: [z. B. Investition, Nachzahlung, Saisonspitze, Großauftrag]
- Umsatzhistorie: [MONATSWERTE der letzten zwölf Monate]

VORGEHEN – IN DIESER REIHENFOLGE, JEDEN SCHRITT AUSWEISEN
1. Zeitreihe: 13 Wochen ab Startwoche, Anfangsbestand je Woche, Endbestand,
   kumulierter Verlauf, verfügbarer Rahmen aus Kontostand plus freier Linie.
2. Einzahlungen aus Forderungen: nach Fälligkeit einplanen, um das historische
   Zahlungsverhalten verschieben, die Verschiebung je Kunde als Annahme
   benennen. Erfinde KEINE Zahlungsquote.
3. Einzahlungen aus künftigen Umsätzen: nur aus der gelieferten Historie
   ableiten, Ableitungsweg offenlegen, Saisonalität als Annahme benennen.
4. Auszahlungen: Verbindlichkeiten nach Fälligkeit, wiederkehrende Zahlungen
   (Personal, Miete, Leasing, Versicherungen, Tilgung) mit ihrem Zahlungsmuster,
   Sondereffekte gesondert.
5. Steuer- und Beitragszahlungen: Plane nur die vom Mandanten gelieferten
   Beträge ein. Bestimme KEINE Zahlungstermine selbst. Lege je Zahlungsart eine
   eigene Zeile mit leerer Wochenspalte an ("Woche vom Menschen einzusetzen") und
   benenne, welche Angabe den Termin bestimmt (Voranmeldungszeitraum,
   Dauerfristverlängerung, Abrechnungsstichtag der Sozialversicherung), je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren". Weise am Ende der
   Wochentabelle aus, welche Zeilen noch keine Woche tragen, und sage, dass die
   Tabelle bis dahin unvollständig ist.
6. Kreditlinien: Ausnutzung im Verlauf zeigen, den Punkt der ersten
   Unterdeckung benennen, ohne Bewertung.
7. Szenarien: Basis, vorsichtig, angespannt. Je Szenario die geänderten
   Annahmen offen auflisten – nur Annahmen ändern, keine Zahlen.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht entscheidbar. Liste alle mit "fehlt" gekennzeichneten
   Angaben als LÜCKE auf und plane sie nicht ein. Erfinde keine Annahme, keinen
   Wert und keine Position.
2. Nenne KEINE Zahlungsquote, keinen Zinssatz, keinen Steuersatz und keinen
   Steuertermin als feststehend – nur nachzuschlagend mit dem Zusatz
   "für [JAHR] verifizieren".
3. Berechne KEINE Fristen und keine Steuertermine. Liste auf, WELCHE Termine und
   Fristen im Raum stehen (Voranmeldung, Lohnsteuer, Beitragsnachweis,
   Vorauszahlung), je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und Dauer, und ergänze: "Termin von
   einem Menschen zu bestimmen und im Fristenprogramm zu erfassen."
4. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV (Norm MIT
   ABSATZ UND SATZ, Richtlinie oder BMF-Schreiben MIT DATUM) mit dem Zusatz
   "für [JAHR] verifizieren"; bist du unsicher:
   "Fundstelle offen – bitte recherchieren".
5. Erläuterungstext für den Mandanten: Sie-Form, höchstens 350 Wörter, jede
   Annahme erklärt, Fachbegriffe in einem Halbsatz aufgelöst, mit dem
   Vorbehaltssatz aus der Abgrenzung.
6. Frühindikatoren: höchstens sieben beobachtbare Größen für die monatliche
   Beobachtung, je mit Quelle in DATEV und Beobachtungsanlass.

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit und Lücken"
2. "Wochentabelle": Woche | Anfangsbestand | Einzahlungen | Auszahlungen |
   Endbestand | freie Linie
3. "Annahmenliste" – je Annahme Quelle und Wirkung
4. "Szenarien" mit den geänderten Annahmen
5. "Erläuterung für den Mandanten" 6. "Termine und Fristarten"
7. "Frühindikatoren" 8. "Interne Notiz" 9. "Was ich nicht sicher weiß"
```

## Anwendung

1. OPOS-Listen mit Fälligkeiten, Kontostände und Tilgungsplan exportieren, auf Kürzel umstellen.
2. Zahlungsverhalten je Kunde aus der Historie ermitteln – ohne diese Angabe wird die Planung zu optimistisch.
3. Ergebnis in DATEV Analyse und Planung übertragen, nicht in eine Einzeltabelle.
4. Wöchentlich rollieren: Woche schließen, neue 13. Woche anhängen, Abweichung vermerken. Erst diese Rückschau macht die Planung belastbar.
5. Lücken mit dem Mandanten klären, nicht selbst füllen.

## Qualitätssicherung

- **Jede Annahme auf Herkunft prüfen.** Annahmen ohne Quelle streichen; als Lücke gekennzeichnete Positionen bleiben Lücke.
- **Keine Zusage im Text.** Formulierungen streichen, die Zahlungsfähigkeit oder Fortführung zusichern. Die Planung ist keine Fortbestehensprognose.
- **Verwendungszweck prüfen.** Vor Weitergabe an eine Bank Prompt 67, bei Krisenindikatoren Prompt 65 – beides mit gesonderter Beurteilung durch einen Berufsträger.
- **Freigabe und Vier-Augen:** Das Ergebnis ist ein Entwurf. Eine zweite Person rechnet Wochentabelle und Annahmenliste nach; die Freigabe erteilt ein Berufsträger (Freigabestufe 3 in `DATENSCHUTZ.md`). Termine bestimmt ein Mensch, kein Datum aus der KI-Antwort übernehmen.
- **Unterdeckung beendet die Mandantenkommunikation.** Zeigt ein Szenario eine Unterdeckung oder eine vollständig ausgenutzte Linie, gehen weder Erläuterungstext noch Frühindikatoren hinaus; dann gilt Prompt 65 und die Bearbeitung liegt beim Berufsträger.
- **Rechtsstand prüfen an:** § 18 UStG, § 41a EStG, § 37 EStG (gesetze-im-internet.de), § 57 StBerG zum Umfang der zulässigen Tätigkeit, §§ 3 und 5 RDG zur Abgrenzung der Rechtsdienstleistung, § 18 KWG zur Offenlegung, § 1 StaRUG zur Krisenfrüherkennung sowie DATEV LEXinform und der DATEV-Hilfe zu Analyse und Planung.

## Varianten

- **Vier Wochen:** „Verkürze auf vier Wochen mit Tagesauflösung."
- **Nur Annahmen:** „Erzeuge ausschließlich die Annahmenliste als Fragebogen."
- **Abweichungsanalyse:** „Vergleiche Plan und Ist der abgelaufenen Wochen und benenne die drei größten Abweichungen mit Vermutung zur Ursache."
- **BWA-Kommentar:** Prompt 06. **Offene Posten:** Prompt 18.
