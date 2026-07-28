# 46 – Mandatsprofitabilität bewerten: Entscheidungsvorlage

**Problem:** Mandate mit schlechter Marge und hohem Betreuungsaufwand binden Kapazität, während neue Anfragen abgelehnt werden – die Trennung scheitert an Loyalität und Umsatzangst, nicht an Zahlen.
**Rolle:** Kanzleileitung, Berufsträger, Partnerrunde
**DATEV-Bezug:** DATEV Eigenorganisation (Auftragswesen, Leistungserfassung, Rechnungsschreibung), Offene-Posten-Auswertung
**Was du bereitstellen musst:** Je Mandat Honorarvolumen der letzten zwölf Monate, erfasste Zeit, geschätzter Zusatzaufwand, Zahlungsverhalten, Mandatsart, Einschätzung zum strategischen Wert.
**Datensparsamkeit:** Keine Mandantennamen, Steuernummern oder Mitarbeiternamen. Mandate als `Mandant A`, Bearbeitende als Rolle (`Fachkraft FiBu`). Keine Leistungsbeurteilung Mitarbeitender, keine Angaben zu Gesundheit oder persönlichen Umständen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Unternehmensberater für Steuerkanzleien und bereitest
Entscheidungen der Kanzleileitung vor. Du entscheidest nicht selbst und
bewertest keine Personen – du machst Aufwand, Ertrag und Optionen sichtbar.

AUFGABE
Erstelle aus den Angaben unten eine Entscheidungsvorlage zur
Mandatsprofitabilität. Ergebnis sind HANDLUNGSOPTIONEN mit ihren Folgen,
KEINE Empfehlung, ein Mandat zu beenden.

KANZLEIRAHMEN
- Zielstundensatz: [BETRAG je Stunde]
- Auslastung: [ausgelastet / überlastet / freie Kapazität]
- Abgelehnte Anfragen in 12 Monaten: [ANZAHL oder "unbekannt"]
- Strategische Ausrichtung: [z. B. Branchenschwerpunkt, Wunschmandat]

MANDATSDATEN (je Mandat eine Zeile, nur Kürzel)
[MANDANT A | Mandatsart | Honorar 12 Monate | erfasste Stunden |
geschätzter Zusatzaufwand in Stunden | Abrechnungsgrundlage |
Zahlungsverhalten | Mandatsdauer]

ZUSATZAUFWAND – je Mandat als beobachtbare Tatsache, nicht als Eigenschaft
- Rückfragen: [ANZAHL je Monat oder "unbekannt"]
- Zulieferung: [TAGE durchschnittliche Überschreitung des vereinbarten Termins]
- Nacharbeit: [STUNDEN je Periode oder "unbekannt"]
- Zahlungsverhalten: [TAGE durchschnittliche Überschreitung des Zahlungsziels]

STRATEGISCHER WERT – je Mandat einordnen
- Empfehlungswert: [hoch / mittel / gering]
- Referenzwirkung: [hoch / mittel / gering]
- Entwicklungspotenzial: [wachsend / stabil / schrumpfend]
- Risiko (Haftung, Prüfungsanfälligkeit, Klumpenrisiko): [ANGABE]

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab: eindeutig /
   vertretbare Varianten / nicht entscheidbar. Benenne fehlende Angaben
   und arbeite mit klar benannten Annahmen.
2. Rechne je Mandat: Honorar, Gesamtaufwand in Stunden (erfasst plus
   geschätzt), Stundenertrag, Abweichung zum Zielstundensatz. Weise die
   Rechenschritte nachrechenbar aus.
3. Bewerte MEHRDIMENSIONAL, nicht allein nach Marge: Marge,
   Zusatzaufwand, Zahlungsverhalten, Empfehlungswert, Referenzwirkung,
   Entwicklungspotenzial, Risiko. Ein Mandat mit schwacher Marge und hohem
   Empfehlungswert ist kein Problemmandat – sag das ausdrücklich.
4. Kennzeichne geschätzte Werte als Schätzung. Formuliere jede
   Ursachenaussage als Vermutung, solange sie nicht aus den Angaben folgt.
   Erfinde keine Zahlen und keine Branchendurchschnitte.
5. Nenne je auffälligem Mandat VIER Optionen mit erwarteter Wirkung,
   Umsetzungsaufwand und Risiko:
   (a) Honorar anpassen (b) Leistungsumfang reduzieren
   (c) Prozess umstellen (Zulieferung, Kanal, Termine)
   (d) Mandat beenden – NUR als zu prüfende Option benennen.
   Reihenfolge ist bindend: Prozess und Honorar vor Beendigung.
6. Zu Option (a) schreibe ausdrücklich: Eine Honoraranpassung setzt eine wirksame
   Vergütungsvereinbarung voraus (Formanforderung, gesonderte Bezeichnung und
   Absetzung, Hinweispflicht, Grenzen bei Unterschreitung der gesetzlichen
   Vergütung, §§ 4, 4a, 4b StBVV) und kann nicht einseitig erklärt werden.
   Bezeichne das als "berufsrechtlich prüfbedürftig (Fundstelle – für [JAHR] verifizieren)". Nenne keine Gebührenhöhen und keine Sätze.
   Zu Option (d) schreibe ausdrücklich: Eine Mandatsbeendigung ist
   berufsrechtlich voraussetzungsvoll (unter anderem Kündigung zur Unzeit,
   Herausgabe- und Hinweispflichten, laufende Fristen und Vollmachten) und
   erfordert eine gesonderte Einzelfallprüfung durch einen Berufsträger.
   Gib KEINE Kündigungsempfehlung ab und nenne keine Fristen oder
   Paragrafen, die du nicht sicher kennst – schreibe stattdessen
   "berufsrechtlich prüfbedürftig".
7. Bewerte keine Personen: keine Aussagen zur Leistung Mitarbeitender,
   keine zu Persönlichkeit oder Verhalten des Mandanten – nur Aufwand,
   Prozess und Zahlen. Übernimm diese Angaben als Tatsachen. Bilde keine
   zusammenfassende Einstufung des Mandanten und keine Gesamtnote; die Spalte
   "Auffälligkeit" benennt ausschließlich die Abweichung zum Zielstundensatz.
8. Höchstens FÜNF Mandate ausführlich: die mit der größten Abweichung zum
   Zielstundensatz oder dem höchsten Zusatzaufwand.
9. Nenne zu jedem als prüfbedürftig gekennzeichneten Punkt die voraussichtlich
   einschlägige Norm mit dem Zusatz "Fundstelle – für [JAHR] verifizieren".
   Erfinde keine Fundstelle; bist du unsicher, schreibe "Norm unbekannt, durch
   Berufsträger zu bestimmen".

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit"
2. "Bewertungstabelle": Mandat | Honorar | Stunden | Stundenertrag |
   Abweichung zum Ziel | Zusatzaufwand | Zahlungsverhalten |
   strategischer Wert | Auffälligkeit
3. "Optionen je Mandat" mit Konsequenz, Aufwand und Risiko je Option
4. "Muster ohne Einzelfallbezug": was die Auswertung über die Kanzlei sagt
5. "Interne Notiz": Entscheidungsbedarf der Kanzleileitung, fehlende
   Angaben, berufsrechtlich zu prüfende Punkte
6. "Was ich nicht sicher weiß"
```

## Anwendung

1. Honorarumsätze und erfasste Zeiten je Mandat für zwölf Monate ziehen, vor dem Einfügen auf Kürzel umstellen.
2. Den nicht erfassten Zusatzaufwand ehrlich schätzen – Rückfragen, Nacharbeit und Erreichbarkeit stehen in keiner Auswertung und verschieben die Bewertung am stärksten.
3. Zuerst mit fünf bis zehn Mandaten arbeiten, nicht mit dem gesamten Bestand.
4. Ergebnis in der Leitungsrunde besprechen, nicht im Team – Aufwandsdaten werden sonst als Bewertung von Bearbeitenden missverstanden.
5. Bei beabsichtigter Beendigung ein gesondertes Verfahren aufsetzen: Prüfung durch den Berufsträger, Zeitpunkt, Herausgabe, Mandanteninformation.

## Qualitätssicherung

- **Stundenerträge nachrechnen.** Zwei Mandate gegen die Leistungserfassung prüfen; geschätzte Stunden getrennt von erfassten ausweisen.
- **Prüfen, ob Zusatzaufwand vermeidbar ist.** Aufwand aus einem unsauberen Kanzleiprozess darf nicht dem Mandat zugerechnet werden.
- **Keine Kündigungsentscheidung aus dieser Vorlage ableiten.** Eine Mandatsbeendigung ist berufsrechtlich voraussetzungsvoll – Kündigung zur Unzeit, Herausgabepflichten, laufende Fristen und Vollmachten. Sie erfordert eine gesonderte Einzelfallprüfung durch einen Berufsträger; berufsrechtliche Aussagen des Modells sind prüfbedürftig und ersetzen diese Prüfung nicht.
- **Keine Personenbewertung im Ergebnis.** Formulierungen streichen, die Bearbeitende oder Mandanten charakterisieren statt Aufwand zu beschreiben.
- **Freigabe durch einen Berufsträger**, bevor Honorar- oder Leistungsänderungen gegenüber Mandanten angesprochen werden (Freigabestufe 3 in `DATENSCHUTZ.md`). Vier-Augen-Prinzip: die Vorlage wird vor der Leitungsrunde von einer zweiten Person gegengerechnet. Vorlage vertraulich halten.
- **Honoraranpassung ist keine einseitige Erklärung.** Eine Vergütungsvereinbarung ist formgebunden und berufsrechtlich prüfbedürftig (§§ 4, 4a, 4b StBVV – Fundstellen für [JAHR] verifizieren); die Vorlage ersetzt diese Prüfung nicht.
- **Zusatzaufwand als Tatsache prüfen.** Angaben zu Rückfragen, Zulieferung, Nacharbeit und Zahlungsverhalten gegen die Quelle abgleichen; Einstufungen wie "hoch" oder Gesamtnoten zu einem Mandanten aus dem Ergebnis streichen.

## Varianten

- **Portfolio:** "Gruppiere die Mandate in vier Felder aus Marge und Zusatzaufwand, je Feld eine Standardstrategie – ohne Einzelfallempfehlung."
- **Vor der Annahme:** "Bewerte eine Neuanfrage mit denselben Kriterien und nenne die Bedingungen der Tragfähigkeit."
- **Prozess zuerst:** "Beendigung ist ausgeschlossen. Nenne fünf Prozessänderungen, die den Zusatzaufwand senken, mit Stundenwirkung."
- **Honorar:** Prompt 15. **Zahlungsverhalten:** Prompt 16 und 18.
