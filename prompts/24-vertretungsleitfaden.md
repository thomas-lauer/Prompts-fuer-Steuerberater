# 24 – Vertretungsleitfaden je Mandant für Urlaub und Krankheit

**Problem:** Fällt der zuständige Bearbeiter aus, weiß die Vertretung nicht, was bei diesem Mandanten anders läuft – und erfährt es erst, wenn etwas schiefgegangen ist.
**Rolle:** Sachbearbeitung (schreibt für die eigene Vertretung), Teamleitung, Kanzleileitung
**DATEV-Bezug:** Eigenorganisation (Wiedervorlage, Fristen, Mandantenstammdaten), Kanzlei-Rechnungswesen, LODAS/Lohn und Gehalt, DATEV Unternehmen online
**Was du bereitstellen musst:** Leistungsumfang für diesen Mandanten, laufende und anstehende Termine, Kontierungsbesonderheiten, offene Punkte, Ansprechpartner beim Mandanten und in der Kanzlei, Abwesenheitszeitraum.
**Datensparsamkeit:** Für den Entwurf Mandantenkürzel statt Klarname, keine Steuernummer, keine Bankverbindung, keine Namen Dritter. Einschätzungen zum Verhalten des Mandanten sachlich formulieren. Der Steckbrief ist ein internes Arbeitspapier und unterliegt nicht der Herausgabepflicht für Mandantenunterlagen (§ 66 Abs. 2 StBerG nimmt Arbeitspapiere aus); über die darin enthaltenen personenbezogenen Daten kann der Mandant jedoch Auskunft verlangen (Art. 15 DSGVO – Fundstelle für [JAHR] verifizieren). Schreibe jeden Satz so, dass er in einer Auskunft bestehen kann. Klarnamen und Kontaktdaten erst beim Ausdruck ergänzen.
Zum Bearbeiter und zur Vertretung nur die ROLLE, kein Kürzel und kein Name. Kein Abwesenheitsgrund: nie "krank", "Kur", "Elternzeit" – nur "Abwesenheit von … bis …" oder "ungeplante Abwesenheit". Der Grund einer Abwesenheit ist ein Gesundheits- bzw. Beschäftigtendatum und gehört nach `DATENSCHUTZ.md` in Zone Rot; er kommt auch nicht in Kürzelform in das KI-Werkzeug.
Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du organisierst Vertretungsregelungen in einer deutschen Steuerkanzlei. Du
schreibst für eine Kollegin, die den Mandanten nicht kennt und in fünf Minuten
handlungsfähig sein muss. Du schreibst sachlich und wertfrei; Eigenheiten des
Mandanten beschreibst du als beobachtetes Verhalten, nicht als Urteil.

AUFGABE
Erstelle einen Vertretungs-Steckbrief für EINEN Mandanten.

MANDAT
- Mandantenkürzel / Branche / Rechtsform: [ANGABE]
- Betreute Leistungen: [z. B. FiBu monatlich, UStVA monatlich mit
  Dauerfristverlängerung, Lohn für [ZAHL] AN, Jahresabschluss, Erklärungen]
- Kontenrahmen: [SKR03 / SKR04]
- Abwesenheit: [VON] bis [BIS] (Grund nicht angeben), Vertretung: [ROLLE]

LAUFENDE AUFGABEN IM ZEITRAUM
[Je Zeile: Aufgabe – Termin – Stand heute]

KONTIERUNGSBESONDERHEITEN
[Je Zeile: Sachverhalt – wie wir ihn buchen – warum, z. B. Sonderkonten,
wiederkehrende Abgrenzungen, gemischte Nutzung, Ist-Versteuerung,
Verrechnungskonto mit verbundenem Unternehmen]

EIGENHEITEN DES MANDANTEN
- Bevorzugter Kommunikationsweg: [ANGABE]
- Übliche Reaktionszeit: [ANGABE]
- Empfindliche Themen: [z. B. Honorar, Nachfragen zu Privatentnahmen]
- Was schon einmal Ärger verursacht hat: [ANGABE]

OFFENE PUNKTE
[Je Zeile: Punkt – seit wann – wer ist am Zug]

ANSPRECHPARTNER
- Beim Mandanten: [FUNKTION, z. B. Geschäftsführung, Buchhaltungskraft]
- In der Kanzlei bei Rückfragen: [ROLLE]

ANFORDERUNGEN
1. Maximal EINE Seite, höchstens 450 Wörter. Was nicht auf die Seite passt,
   gehört nicht in den Steckbrief, sondern in die Akte. Nenne am Ende, was du
   aus Platzgründen weggelassen hast.
2. Reihenfolge: zuerst was im Abwesenheitszeitraum zu TUN ist, dann was man
   WISSEN muss. Nicht umgekehrt.
3. Erzeuge einen eigenen Abschnitt "Nicht ohne Rücksprache entscheiden" mit
   höchstens fünf Punkten – jeweils mit der Angabe, wen die Vertretung
   stattdessen fragt.
4. Formuliere Eigenheiten des Mandanten als beobachtetes Verhalten und als
   Handlungshinweis ("meldet sich erfahrungsgemäß nach zwei bis drei Tagen –
   nicht früher nachfassen"). Keine Charakterurteile, keine Zuschreibungen
   zu Gesundheit, Herkunft oder persönlichen Verhältnissen.
5. Kontierungsbesonderheiten nur übernehmen, wenn sie angegeben sind. Leite
   keine Buchungsregeln aus der Branche ab und nenne keine konkreten
   Kontonummern, die nicht angegeben wurden.
6. Nenne keine Fristen als feststehend, ohne sie als "Termin – für [JAHR]
   verifizieren" zu kennzeichnen. Erfinde keine Paragrafen.
7. Was in den Angaben fehlt, markierst du als (offen) und nimmst es in die
   Klärungsliste auf – nicht ergänzen, nicht plausibel raten.

AUSGABEFORMAT
1. Steckbrief (max. 1 Seite):
   Kopfzeile Mandat/Zeitraum/Vertretung – Was ansteht (Tabelle:
   Aufgabe | Termin | Stand | Was zu tun ist) – Besonderheiten Kontierung –
   Umgang mit dem Mandanten – Offene Punkte – Nicht ohne Rücksprache
   entscheiden – Ansprechpartner
2. "Was der Bearbeiter vor dem Urlaub noch klären muss"
   (Tabelle: Nr. | Punkt | Bis wann | Mit wem | erledigt ☐)
3. Interne Notiz: weggelassene Punkte und was die Teamleitung wissen sollte
```

## Anwendung

1. Spätestens zwei Wochen vor der Abwesenheit ausfüllen – nur dann ist die Liste "vor dem Urlaub klären" noch abarbeitbar.
2. Steckbrief mit der Vertretung persönlich durchgehen, nicht nur ablegen. Das Gespräch dauert fünf Minuten und deckt die letzten Lücken auf.
3. Für ungeplante Abwesenheiten: Steckbriefe laufend gepflegt für das Team zugänglich halten. Ein Leitfaden, der erst bei Ausfall des Bearbeiters geschrieben wird, existiert nicht. Der Grund der Abwesenheit wird dabei nirgends festgehalten – es genügt, dass der Bearbeiter ausfällt.
4. Nach der Rückkehr aktualisieren: Was hat die Vertretung gefragt? Genau das fehlte.

## Qualitätssicherung

- Alle Termine gegen Wiedervorlage und Fristenkalender abgleichen; der Steckbrief ersetzt die Fristenüberwachung nicht.
- Kontierungsbesonderheiten stichprobenweise gegen die Buchungen des Vorjahres prüfen – überliefertes Wissen ist oft veraltet.
- Abschnitt "Nicht ohne Rücksprache" durch den Berufsträger bestätigen lassen, besonders bei Vollmachten, Zahlungsfreigaben und Auskünften an Dritte.
- Formulierungen zu Eigenheiten des Mandanten gegenlesen: Würden Sie den Satz dem Mandanten zeigen wollen? Wenn nein, umformulieren.
- Prüfen, ob die Vertretung die nötigen Rechte in DATEV hat – fehlende Berechtigungen sind der häufigste stille Blocker.
- Prüfen, dass im Steckbrief kein Abwesenheitsgrund und kein Personenname des Bearbeiters steht – nur Rolle und Zeitraum. Ein Grund im Text ist ein Beschäftigtendatum und dort zu löschen.
- Das Mandantenanschreiben ist Mandantenkommunikation und geht nur nach Freigabe durch den zuständigen Berufsträger hinaus (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Der Steckbrief ist ein Entwurf.** Vor der Weitergabe an die Vertretung von einer zweiten Person gegenlesen lassen (Vier-Augen-Prinzip); Termine, Vollmachten und Zahlungsfreigaben gibt ein Berufsträger frei.

## Varianten

- **Team statt Einzelperson:** "Erzeuge einen Sammelsteckbrief für alle [ZAHL] Mandate dieses Bearbeiters, je Mandat höchstens acht Zeilen, sortiert nach Termindruck."
- **Ungeplante Abwesenheit ohne Vorlauf:** "Lasse den Abschnitt 'vor dem Urlaub klären' weg und ergänze stattdessen 'Was die Vertretung in den ersten zwei Stunden tun muss'."
- **Mandantenanschreiben:** "Erzeuge zusätzlich eine Mail von höchstens 80 Wörtern an den Mandanten: Zeitraum, Vertretung, Kontaktweg."
