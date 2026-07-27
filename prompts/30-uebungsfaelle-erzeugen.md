# 30 – Übungsfälle mit Musterlösung für die Einarbeitung erzeugen

**Problem:** Einarbeitung bindet die Zeit erfahrener Kräfte; es fehlen Übungsfälle, an denen neue Mitarbeitende gefahrlos lernen können, ohne an einem echten Mandat auszuprobieren.
**Rolle:** Ausbildungsbeauftragte, Teamleitung, Kanzleileitung
**DATEV-Bezug:** Kanzlei-Rechnungswesen (Kontierung, EÜR), LODAS / Lohn und Gehalt, Umsatzsteuer-Voranmeldung, DATEV Reisekostenabrechnung, Übungsmandant im Testsystem
**Was du bereitstellen musst:** Themengebiet, Schwierigkeitsgrad, Vorkenntnisse der lernenden Person, Kontenrahmen, typische Mandantenstruktur.
**Datensparsamkeit:** Übungsfälle werden frei erfunden. Keine echten Mandantendaten, keine abgewandelten Echtfälle mit erkennbaren Merkmalen (Branche, Ort und Betragshöhe zusammen machen ein Mandat identifizierbar). Firmen als `Muster GmbH`, Personen als `AN 1`. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Ausbildungsbeauftragte in einer deutschen Steuerkanzlei und
schreibst Übungsfälle. Du schreibst Fälle so, dass genau EIN fachlicher
Kern geübt wird und der Rest des Sachverhalts unauffällig bleibt.

AUFGABE
Erzeuge [ANZAHL] anonyme Übungsfälle mit getrennter Musterlösung.

RAHMEN
- Themengebiet: [KONTIERUNG / UMSATZSTEUER / LOHNSONDERFÄLLE / EÜR / REISEKOSTEN]
- Schwerpunkt innerhalb des Themas: [z. B. § 13b, Bewirtung, Firmenwagen,
  Einmalzahlungen, Anzahlungen]
- Schwierigkeitsgrad: [EINSTIEG / MITTEL / FORTGESCHRITTEN]
- Zielgruppe: [AUSZUBILDENDE 1. JAHR / QUEREINSTEIGER / STEUERFACHANGESTELLTE]
- Kontenrahmen: [SKR03 / SKR04]
- Rechtsform des fiktiven Mandanten: [RECHTSFORM], Gewinnermittlung: [BILANZ / EÜR]
- Bearbeitungszeit je Fall: [MINUTEN]

ANFORDERUNGEN
1. Jeder Fall enthält: kurzen Sachverhalt (max. 120 Wörter), die
   Belegangaben als Feldliste (Daten, Beträge, Hinweise auf dem Beleg)
   und eine klar formulierte Arbeitsanweisung.
2. Baue in jeden Fall genau EINE Stolperstelle ein, die zum Schwerpunkt
   passt. Bei [EINSTIEG] ist die Stolperstelle im Sachverhalt erkennbar,
   bei [FORTGESCHRITTEN] ergibt sie sich erst aus einem Detail.
3. Erfinde alle Namen, Orte und Beträge. Verwende ausschließlich
   Platzhalternamen (Muster GmbH, AN 1). Keine realen Unternehmen.
4. Die MUSTERLÖSUNG enthält je Fall:
   - Ergebnis (Buchungssatz / Beurteilung / Abrechnung)
   - Begründung in maximal 6 Sätzen mit Nennung der einschlägigen Norm
   - die typischen Fehler, die Lernende hier machen, und WARUM der jeweilige
     Fehler naheliegt
   - zwei Kontrollfragen zum Verständnis, mit Antwort
5. WICHTIG – Verifikationspflicht: Markiere in der Musterlösung JEDE
   Kontonummer, jede Betragsgrenze, jeden Steuersatz, jede Pauschale und
   jede Fundstelle ausdrücklich mit (für [JAHR] verifizieren). Behaupte keine
   Kontonummer als gesichert; Kontonummern sind der unzuverlässigste Teil
   deiner Antwort. Erfinde keine Paragrafen und keine BMF-Schreiben.
   Kennzeichne jede Aussage, bei der sich die Rechtslage geändert haben
   könnte, als "Rechtsstand – für [JAHR] verifizieren".
   Gib zusätzlich je Fall eine Zeile "Sicherheit der Beurteilung: gesichert /
   vertretbar, aber prüfbedürftig / unsicher" mit einem Halbsatz Begründung. Bei
   "unsicher" schreibe ausdrücklich, dass der Fall ohne fachliche Prüfung nicht
   eingesetzt werden darf.
6. Erzeuge am Ende einen Abschnitt PRÜFHINWEISE FÜR DIE AUSBILDENDE PERSON:
   welche Angaben vor dem Einsatz fachlich zu prüfen sind, an welchen
   Stellen der Fall bei abweichender Rechtslage nicht mehr aufgeht, und
   welche Stellen bewusst mehrdeutig sind.
7. Fall und Musterlösung strikt trennen. In den Fallteil gehört KEIN
   Hinweis auf die Lösung, kein Vorgriff, keine Andeutung.
8. Setze in jeden Teil eine Kopfzeile: "Rechtsstand: für [JAHR] verifizieren |
   Status: ENTWURF, nicht freigegeben | Freigabe durch: (offen) | Datum: (offen)".
   Der Status bleibt "ENTWURF", bis die ausbildende Person ihn ersetzt. Teil A
   trägt diese Kopfzeile ebenfalls.

AUSGABEFORMAT
TEIL A – ÜBUNGSFÄLLE (allein ausgebbar, ohne Lösungshinweise)
TEIL B – MUSTERLÖSUNGEN (je Fall: Ergebnis, Begründung, typische Fehler,
         Kontrollfragen mit Antwort)
TEIL C – PRÜFHINWEISE FÜR DIE AUSBILDENDE PERSON
TEIL D – Was ich nicht sicher weiß
```

## Anwendung

1. Erst Teil C lesen, dann Teil B fachlich prüfen, dann Teil A ausgeben. Nie in umgekehrter Reihenfolge.
2. Alle mit (für [JAHR] verifizieren) markierten Werte gegen Kontenrahmen, Steuerschlüsseltabelle und aktuellen Rechtsstand abgleichen und die Markierung erst danach entfernen. Erst danach den Status in der Kopfzeile von "ENTWURF" auf freigegeben ändern, mit Freigeber und Datum.
3. Teil A getrennt speichern; die Musterlösung erst nach der eigenen Bearbeitung herausgeben.
4. Geprüfte Fälle in einer Kanzlei-Fallsammlung ablegen, sortiert nach Thema und Schwierigkeitsgrad – die Prüfung fällt so nur einmal an.
5. Fälle mit Prompt 29 verknüpfen: je überprüfbarer Fertigkeit mindestens ein Fall.

## Qualitätssicherung

- **Ein fehlerhafter Übungsfall lehrt den Fehler.** Vier-Augen-Prinzip: Die Musterlösung wird vor dem ersten Einsatz von einer fachlich qualifizierten Person geprüft, die den Fall nicht erzeugt hat, bei Fällen mit Rechtsanwendungsspielraum von einem Berufsträger freigegeben. Das ist keine Empfehlung, sondern Voraussetzung des Einsatzes.
- Kontonummern grundsätzlich selbst nachschlagen. Sprachmodelle geben sie plausibel und häufig falsch an.
- Prüfen, ob der Sachverhalt vollständig ist: Ein Fall, der ohne zusätzliche Annahmen nicht lösbar ist, erzeugt Frustration statt Lernerfolg – entweder Angaben ergänzen oder die Mehrdeutigkeit zum Lernziel machen.
- Prüfen, ob wirklich nur eine Stolperstelle enthalten ist. Häufen sich Sonderfälle, prüft der Fall Ausdauer statt Verständnis.
- Bezug zu echten Mandaten ausschließen. Auch abgewandelte Echtfälle können identifizierbar bleiben; im Zweifel Branche oder Größenordnung ändern.
- Rechtsstand mit Datum auf jeden Fall schreiben. Fälle veralten still. Die Kopfzeile aus Anforderung 8 gehört auf Teil A, B und C; solange dort "ENTWURF" steht, ist der Fall nicht einsetzbar.
- Die Zeile "Sicherheit der Beurteilung" gegenlesen: Fälle mit "unsicher" werden nicht ausgegeben, sondern fachlich geklärt oder gestrichen. Das Modell schätzt seine eigene Sicherheit nur grob – eine Selbsteinschätzung "gesichert" entbindet nicht von der Prüfung.

## Varianten

- **Fallserie mit Steigerung:** "Erzeuge drei aufeinander aufbauende Fälle: Grundfall, Variante mit Änderung, Fehlerfall zum Aufdecken."
- **Fehlersuchfall:** "Gib den Fall bereits gebucht aus, mit zwei eingebauten Fehlern; Aufgabe ist, sie zu finden und zu begründen."
- **Mandantengespräch:** "Formuliere den Sachverhalt als Mandantenanruf mit unvollständigen Angaben; die Aufgabe ist, die fehlenden Angaben zu erfragen."
- **Selbstlernpaket:** Teil A und Teil B zeitversetzt bereitstellen, dazu ein Kurzprotokoll, in dem die lernende Person ihre Abweichungen selbst einträgt.
