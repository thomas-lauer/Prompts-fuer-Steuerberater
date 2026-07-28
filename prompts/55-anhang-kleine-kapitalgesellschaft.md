# 55 – Anhang kleine Kapitalgesellschaft: Pflichtangaben-Prüfliste

**Problem:** Der Anhang wird jährlich kopiert, obwohl sich Haftungsverhältnisse, Organkredite, Mitarbeiterzahl oder nachträgliche Ereignisse geändert haben.
**Rolle:** Sachbearbeiter Jahresabschluss, Bilanzbuchhalter, Steuerberater
**DATEV-Bezug:** DATEV Bilanzbericht (Anhangtexte und Textbausteine), DATEV Kanzlei-Rechnungswesen (Jahresabschluss, Kontennachweise), DATEV DMS
**Was du bereitstellen musst:** Bilanzsumme, Umsatzerlöse und durchschnittliche Arbeitnehmerzahl des laufenden und der beiden Vorjahre; Vorjahresanhang; Verzeichnis der Haftungsverhältnisse und außerbilanziellen Geschäfte; Restlaufzeiten der Verbindlichkeiten; Organkredite; Gesellschafterliste und Beteiligungen; Ereignisse nach dem Stichtag; angewandte Methoden und Abweichungen zum Vorjahr.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Steuernummer, Registernummer und Namen von Gesellschaftern, Geschäftsführern und Arbeitnehmern durch Platzhalter ersetzen (`Gesellschaft A`, `Gesellschafter 1`, `Organmitglied 1`). Für die Prüfung genügen Beträge, Anteile und Laufzeiten. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Sachbearbeiter Jahresabschluss in einer deutschen Steuerkanzlei und
erstellst den Anhang einer Kapitalgesellschaft. Du prüfst jede Pflichtangabe neu
gegen den Sachverhalt dieses Jahres. Du schreibst im Bewusstsein, dass der Anhang
offengelegt und damit öffentlich einsehbar wird.

AUFGABE
Stelle in drei Stufen die Größenklasse fest, erzeuge die mandantenspezifische
Pflichtangabenliste und formuliere die Anhangtexte.

MANDANTENRAHMEN
- Rechtsform: [GmbH / UG / AG / haftungsbeschränkte Personengesellschaft / …]
- Wirtschaftsjahr: [VON BIS]
- Bilanzsumme, laufendes Jahr und zwei Vorjahre: [WERTE]
- Umsatzerlöse, laufendes Jahr und zwei Vorjahre: [WERTE]
- Arbeitnehmerzahl im Durchschnitt, drei Jahre: [WERTE]
- Erstes Geschäftsjahr oder Umwandlungsjahr: [ja / nein]
- Erleichterungen bisher in Anspruch genommen: [ja / nein / teilweise]

DATEN
1. Anhang des Vorjahres: [VORJAHRESANHANG EINFÜGEN]
2. Haftungsverhältnisse und außerbilanzielle Geschäfte: [ÜBERSICHT EINFÜGEN]
3. Verbindlichkeiten nach Restlaufzeit: [ÜBERSICHT EINFÜGEN]
4. Kredite und Vorschüsse an Organmitglieder: [ÜBERSICHT ODER KEINE]
5. Gesellschafts- und Beteiligungsverhältnisse: [ÜBERSICHT EINFÜGEN]
6. Ereignisse nach dem Stichtag: [EREIGNISSE ODER KEINE]
7. Angewandte Methoden und Abweichungen zum Vorjahr: [ANGABEN EINFÜGEN]

STUFE 1 – GRÖSSENKLASSE
Ordne die Gesellschaft einer Größenklasse zu. Nenne die drei Merkmale, die Regel
über die Überschreitung an zwei aufeinanderfolgenden Stichtagen und die
Besonderheit im ersten Geschäftsjahr, jeweils mit Rechtsgrundlage. Gib die
Schwellenwerte NICHT als feststehend aus, sondern als nachzuschlagen mit dem
Zusatz "für [JAHR] verifizieren" – die Schwellen wurden angehoben. Leite ab,
welche Erleichterungen greifen und welche Angaben entfallen.
Ergibt die Einordnung eine Kleinstkapitalgesellschaft, prüfe VOR Stufe 2, ob
überhaupt ein Anhang aufzustellen ist. Benenne die Voraussetzungen, unter denen
die Aufstellung entfällt, und die Angaben, die dann unter der Bilanz zu machen
sind, je mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren". Entfällt
die Aufstellung, brich Stufe 3 ab und gib stattdessen nur die Liste der unter
der Bilanz zu machenden Angaben aus.

STUFE 2 – PFLICHTANGABENLISTE
Prüfe je Punkt: erforderlich, nicht erforderlich oder Angaben fehlen.
1. Bilanzierungs- und Bewertungsmethoden
2. Abweichungen von den Vorjahresmethoden samt Begründung und Wirkung
3. Restlaufzeiten und Besicherung der Verbindlichkeiten
4. Haftungsverhältnisse, Sicherheiten und außerbilanzielle Geschäfte
   einschließlich der Risikoeinschätzung
5. Durchschnittliche Zahl der Arbeitnehmer und das Ermittlungsverfahren
6. Kredite und Vorschüsse an Organmitglieder
7. Nachtragsangaben zu Ereignissen nach dem Stichtag
8. Angaben zu Gesellschafts- und Beteiligungsverhältnissen
9. Angabe, dass Erleichterungen in Anspruch genommen werden
10. Weitere Angaben, die sich aus dem Sachverhalt ergeben
Begründe jede Einordnung in einem Satz und nenne die Rechtsgrundlage.

STUFE 3 – ANHANGTEXTE
Formuliere je erforderlicher Angabe einen Text: sachlich, knapp, ohne Wertung,
ohne Angabe über die Pflicht hinaus. Wo der Sachverhalt fehlt, setze eine
deutlich gekennzeichnete Leerstelle statt einer Formulierung.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz oder Verlautbarung mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
3. Nenne KEINE Schwellenwerte und Betragsgrenzen als feststehend. Schreibe,
   WELCHER Wert nachzuschlagen ist, mit dem Zusatz "für [JAHR] verifizieren".
4. Übernimm keinen Vorjahrestext unverändert. Kennzeichne jeden Vorjahrestext,
   dessen Grundlage sich verändert haben könnte, als prüfbedürftig und benenne
   die Änderung.
5. Der Anhang wird offengelegt. Weise auf jede Formulierung hin, die mehr
   offenlegt als die Pflicht verlangt, und schlage die knappere Fassung vor.
   Unterscheide freiwillige Zusatzangaben, die entfallen können, von
   Pflichtangaben, die nur unter den Voraussetzungen einer besonderen
   Schutzvorschrift unterbleiben dürfen; nenne diese Vorschrift
   (Fundstelle – für [JAHR] verifizieren).
6. Formuliere keine Risikoeinschätzung, die der Sachverhalt nicht hergibt.
   Fehlt sie, benenne sie als vom Mandanten zu erklären.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Größenklassenfeststellung mit Begründung und nachzuschlagenden Werten
3. Pflichtangabenliste (Nr. | Angabe | Status als erforderlich, nicht
   erforderlich oder Angaben fehlen | Begründung | Rechtsgrundlage)
4. Formulierte Anhangtexte in der Reihenfolge der Liste
5. Hinweise zur Offenlegung: Formulierungen, die zu viel preisgeben
6. Interne Notiz mit den Angaben, die der Mandant liefern muss, abhakbar mit ☐
7. Was ich nicht sicher weiß
```

## Anwendung

1. Kennzahlen der drei Jahre und den Vorjahresanhang bereitlegen; ohne Vorjahreswerte ist die Größenklasse nicht feststellbar.
2. Prompt ausführen; zuerst die Schwellenwerte am Gesetzestext klären, danach die Größenklassenfeststellung prüfen.
3. Interne Notiz als Anforderungsliste an den Mandanten geben, insbesondere zu Haftungsverhältnissen, Organkrediten und Ereignissen nach dem Stichtag – nur die Geschäftsführung kann das erklären.
4. Anhangtexte in DATEV Bilanzbericht übernehmen, Textbausteine fortschreiben.
5. Vor der Offenlegung den Anhang mit dem Blick eines Dritten lesen: Banken, Wettbewerber und Geschäftspartner lesen mit.

## Qualitätssicherung

- **Der Anhang wird offengelegt und ist damit öffentlich sichtbar.** Jede Angabe darauf prüfen, ob sie erforderlich ist; freiwillige Zusatzangaben bewusst entscheiden.
- **Das Ergebnis ist ein Entwurf.** Vor der Verwendung prüfen: Größenklasse, Vollständigkeit der Pflichtangaben, Übereinstimmung der Anhangzahlen mit Bilanz und Erfolgsrechnung.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite fachkundige Person prüft die Pflichtangabenliste Punkt für Punkt; Anhang und Offenlegung gibt ein Berufsträger frei, die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`). Haftungsverhältnisse und Organkredite schriftlich bestätigen lassen.
- **Rechtsstand prüfen an:** §§ 264, 267, 267a, 284, 285, 286, 288 HGB im amtlichen Volltext (gesetze-im-internet.de), die Änderungsgesetze zu den Schwellenwerten über das Bundesgesetzblatt, die Verlautbarungen der Bundessteuerberaterkammer sowie DATEV LEXinform.

## Varianten

- **Kleinstkapitalgesellschaft:** Zusatz "Prüfe, welche Erleichterungen für Kleinstkapitalgesellschaften greifen und welche Angaben verbleiben."
- **Erstes Geschäftsjahr:** Zusatz "Behandle das Wirtschaftsjahr als erstes Geschäftsjahr und benenne die Besonderheiten der Größenklassenfeststellung."
- **Methodenwechsel:** Zusatz "Stelle die Abweichungen von den Vorjahresmethoden gesondert dar."
- **Offenlegung:** Zusatz "Leite die offenzulegenden Unterlagen ab, ohne Fristen zu nennen."
- **Mandantengespräch:** Zusatz "Erzeuge eine Kurzfassung mit maximal 200 Wörtern, die der Geschäftsführung erklärt, was offengelegt wird." Ergänzt Prompt 11.
