# 01 – Belegnachforderung beim Mandanten in drei Eskalationsstufen

**Problem:** Mandanten liefern Belege zu spät oder unvollständig; die Kanzlei schreibt immer wieder neue Erinnerungen von Hand.
**Rolle:** Buchhaltung, Sekretariat, Lohnsachbearbeitung
**DATEV-Bezug:** DATEV Unternehmen online (Belegtransfer), Kanzlei-Rechnungswesen, LODAS/Lohn und Gehalt
**Was du bereitstellen musst:** Liste der fehlenden Unterlagen, Zeitraum, bisherige Kontakte, gewünschte Frist, Verhältnis zum Mandanten.
**Datensparsamkeit:** Mandantenname, Anschrift, Steuernummer und den Namen des Ansprechpartners durch Platzhalter ersetzen (`Mandant A`, `Frau M.`). Namen erst beim Versand aus der Kanzleivorlage einsetzen.

## Prompt

```text
Du bist erfahrene Kanzleimitarbeiterin in einer deutschen Steuerkanzlei und
schreibst Mandantenkorrespondenz. Dein Stil: höflich, klar, kurze Sätze,
keine Floskeln, keine Vorwürfe, immer mit konkretem nächsten Schritt.

AUFGABE
Schreibe DREI aufeinander aufbauende Anschreiben zur Nachforderung fehlender
Unterlagen – Stufe 1 freundliche Erinnerung, Stufe 2 verbindliche Nachfassung
mit Fristsetzung, Stufe 3 letzte Aufforderung mit Konsequenzenhinweis.

KONTEXT
- Mandant: [MANDANTENKÜRZEL / BRANCHE / ANREDE DES ANSPRECHPARTNERS]
- Zeitraum / Vorgang: [ZEITRAUM, z. B. Buchhaltung Juni 2026 oder Lohnabrechnung 07/2026]
- Übermittlungsweg: [DATEV Unternehmen online / DATEV Meine Steuern / E-Mail]
- Fehlende Unterlagen:
  [LISTE, eine Position je Zeile, z. B.
   - Eingangsrechnungen Juni: 7 von 23 fehlen
   - Kontoauszüge Bank XY Nr. 6–8
   - Kassenbericht Juni mit Zählprotokoll]
- Bisherige Kontakte: [z. B. Erinnerung am 03.07., Telefonat am 10.07.]
- Gewünschte Frist: [DATUM]
- Beziehung: [langjährig und gut / neu / bereits angespannt]
- Konsequenz bei Nichtlieferung: [z. B. Übermittlung einer auf Schätzwerten
  beruhenden Voranmeldung mit anschließender Berichtigung, verspätete Abgabe
  mit Verspätungszuschlag, Verschiebung des Abschlusses, gesonderte
  Abrechnung des Mehraufwands]

ANFORDERUNGEN
1. Jede Stufe als eigenständige, sofort versendbare E-Mail mit Betreffzeile.
2. Die fehlenden Unterlagen als nummerierte Liste – der Mandant muss sie
   abhaken können, ohne zurückzufragen.
3. Nenne in jeder Stufe genau EINEN Übermittlungsweg und wie er funktioniert.
4. Stufe 1: freundlich, unterstellt Vergessen, bietet Hilfe an.
   Stufe 2: sachlich verbindlich, klare Frist mit Datum, benennt die Folge
   für die Kanzleiarbeit.
   Stufe 3: förmlich, letzte Frist, benennt die konkrete Konsequenz
   sachlich und ohne Drohton, bietet ein Gespräch an.
5. Maximal 180 Wörter je Mail. Keine Rechtsbelehrung, kein Paragrafenzitat,
   außer es ist für die Konsequenz zwingend.
6. Passe die Anrede an: [Sie-Form förmlich / Sie-Form vertraut / Du-Form].

AUSGABEFORMAT
Für jede Stufe: Überschrift "Stufe N – <Zweck>", Betreff, Mailtext,
darunter eine Zeile "Versenden ab: <Zeitpunkt relativ zur Vorstufe>".
```

## Anwendung

1. Fehlende Positionen aus der Belegübersicht in DATEV Unternehmen online bzw. aus deiner Nachfrageliste kopieren.
2. Prompt ausfüllen, Ergebnis erzeugen lassen.
3. Stufe 1 sofort versenden, Stufen 2 und 3 als Wiedervorlage hinterlegen.
4. Die drei Texte einmalig als Kanzleivorlage speichern – ab dem zweiten Mal reicht Austauschen der Liste.

## Qualitätssicherung

- Prüfe, ob die genannte Konsequenz mandatsvertraglich und berufsrechtlich tragfähig ist. Formulierungen wie "wir stellen die Arbeit ein" nie ungeprüft versenden.
- Frist muss zur tatsächlichen Bearbeitungszeit der Kanzlei passen, nicht nur zur gesetzlichen Frist.
- Bei angespanntem Mandat: Stufe 3 vor Versand vom verantwortlichen Berufsträger freigeben lassen.

## Varianten

- **Lohn:** Stichtagsbezogen umformulieren ("Abrechnungsschluss ist der 5. des Monats"), Positionen = Stundenzettel, Krankmeldungen, Ein-/Austritte.
- **Jahresabschluss:** Stufe 2 um Hinweis auf Offenlegungsfrist ergänzen.
- **Kurzfassung für Messenger/SMS:** Zusatzanweisung "Erzeuge zusätzlich je Stufe eine Kurzfassung mit maximal 300 Zeichen." Nur über einen von der Kanzlei berufsrechtlich freigegebenen Kanal versenden; WhatsApp und vergleichbare Dienste sind ohne dokumentierte Freigabe und Einwilligung nicht geeignet (§ 57 StBerG, § 203 StGB, DSGVO). Keine Mandatsinhalte in die Kurzfassung aufnehmen, nur die Aufforderung zur Rückmeldung.
