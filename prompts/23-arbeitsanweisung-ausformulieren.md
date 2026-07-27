# 23 – Arbeitsanweisung aus Stichworten ausformulieren

**Problem:** Dieselbe Aufgabe wird je nach Bearbeiter anders erledigt, weil der Ablauf nie aufgeschrieben wurde – bei Urlaub und Krankheit bricht die Vertretung ein.
**Rolle:** Kanzleileitung, Teamleitung, erfahrene Sachbearbeitung, Qualitätsbeauftragte
**DATEV-Bezug:** Eigenorganisation (Arbeitsablauf, Wiedervorlage), Kanzlei-Rechnungswesen, LODAS/Lohn und Gehalt, DATEV Unternehmen online – je nachdem, welchen Ablauf die Anweisung beschreibt
**Was du bereitstellen musst:** Stichwortartige Notizen der Kraft, die den Ablauf heute macht (Reihenfolge grob genügt), Auslöser der Aufgabe, beteiligte Rollen, betroffene Programme, bekannte Fehlerfälle.
**Datensparsamkeit:** Mandantennamen, Steuernummern und Namen von Mitarbeitern durch Rollen und Platzhalter ersetzen (`Mandant A`, `Sachbearbeitung FiBu`, `Berufsträger`). Eine Arbeitsanweisung beschreibt Rollen, nicht Personen – das ist zugleich datensparsam und länger haltbar. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du dokumentierst Arbeitsabläufe in einer deutschen Steuerkanzlei. Du schreibst
so, dass eine eingearbeitete Vertretung den Ablauf allein durchführen kann,
ohne nachzufragen. Du erfindest nichts: Was in den Stichworten fehlt, wird zur
offenen Frage, nicht zu einer plausiblen Behauptung.

AUFGABE
Formuliere aus den folgenden Stichworten eine Arbeitsanweisung aus.

VORGANG
- Bezeichnung: [WIE DER ABLAUF IN DER KANZLEI GENANNT WIRD]
- Häufigkeit: [täglich / monatlich / quartalsweise / jährlich / anlassbezogen]
- Betroffene Programme: [z. B. DATEV Kanzlei-Rechnungswesen, DATEV Unternehmen
  online, LODAS, Eigenorganisation, Outlook, Dokumentenablage]
- Beteiligte Rollen: [z. B. Sekretariat, Sachbearbeitung, Berufsträger]
- Stichworte der erfahrenen Kraft:
  [NOTIZEN, eine Zeile je Gedanke, Reihenfolge grob, unvollständig erlaubt]
- Bekannte Fehlerfälle: [WAS SCHON SCHIEFGEGANGEN IST]

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER VOLLSTÄNDIGKEIT ab:
   vollständig / in Teilen lückenhaft / als Anweisung noch nicht tragfähig.
2. Gliedere die Anweisung genau so:
   Zweck – Auslöser – Voraussetzungen – Schritte – Entscheidungspunkte –
   Ausnahmen – Fehlerquellen – Freigabe.
3. Jeder Schritt: fortlaufende Nummer, ein Satz im Imperativ, dahinter der
   Verantwortliche als ROLLE (nie als Personenname) und, falls einschlägig,
   Programm und Menüpfad.
4. Jeder Entscheidungspunkt bekommt ein nachprüfbares KRITERIUM
   ("wenn Betrag über [BETRAG]" statt "wenn größer"), beide Zweige und die
   Angabe, wer entscheidet.
5. Trenne Ausnahmen (seltene, aber vorgesehene Fälle) von Fehlerquellen
   (was typischerweise falsch gemacht wird und woran man es erkennt).
6. Unter "Freigabe": wer den Vorgang abschließend prüft, woran, und was ohne
   diese Freigabe nicht hinausgeht.
7. WICHTIGSTE REGEL: Ergänze KEINE Schritte aus allgemeiner Plausibilität.
   Wo die Stichworte eine Lücke lassen, setze an die Stelle im Ablauf den
   Marker (offen) und nimm die Lücke in die Liste der offenen Fragen auf.
   Lieber eine Anweisung mit zwölf offenen Fragen als eine glatte Anweisung,
   die an drei Stellen falsch ist.
8. Nenne keine Fristen, keine Betragsgrenzen und keine Paragrafen, die nicht
   in den Stichworten stehen. Ist eine Frist erkennbar gemeint, aber nicht
   genannt, schreibe "Frist offen – für [JAHR] verifizieren und von einem
   Menschen im Fristenprogramm erfassen".
9. Höchstens 15 Schritte. Ist der Ablauf länger, schlage eine Teilung in zwei
   Anweisungen vor und nenne die Schnittstelle.

AUSGABEFORMAT
1. Einschätzung der Vollständigkeit
2. Arbeitsanweisung (Gliederung nach Nr. 2, Schritte als Tabelle:
   Nr. | Schritt | Rolle | Programm/Pfad | Ergebnis)
   Kopfzeile der Anweisung: Bezeichnung | Version | Stand (Datum) |
   freigegeben durch (Rolle) | nächste Prüfung | Anzahl noch offener Marker.
3. Offene Fragen (Tabelle: Nr. | Stelle im Ablauf | Was fehlt |
   Wen fragen | Antwort (leer))
4. Interne Notiz: was vor Inkraftsetzung noch zu klären ist
```

## Anwendung

1. Die erfahrene Kraft schreibt ihre Stichworte in zehn Minuten herunter – ungeordnet, unvollständig, das reicht. Nicht schön formulieren lassen, das ist die Arbeit des Prompts.
2. Prompt ausführen, Ergebnis mit derselben Kraft durchgehen und nur die offenen Fragen abarbeiten. Die Lückenliste zeigt genau das, was bisher nur im Kopf einer Person lag.
3. Zweite Runde mit den ergänzten Antworten, dann Version und Datum vergeben.
4. Anweisung von jemandem testen lassen, der den Ablauf nicht kennt. Jede Rückfrage im Test ist eine verbliebene Lücke.

## Qualitätssicherung

- **Die Anweisung ist ein Entwurf.** Vier-Augen-Prinzip: Vor Inkraftsetzung liest eine zweite Person gegen, die den Ablauf nicht beschrieben hat. Die Freigabe erteilt ein Berufsträger, sobald die Anweisung Mandantenkommunikation, Fristen oder Vorbehaltsaufgaben berührt (Freigabestufe 3 in `DATENSCHUTZ.md`). Kopfzeile mit Version, Stand und Freigeber ausfüllen.
- Jeden Menüpfad und jede Programmbezeichnung am lebenden System nachsehen; das Modell kennt die Oberfläche der eingesetzten Version nicht.
- Alle Marker (offen) müssen vor Inkraftsetzung verschwunden sein – ein Marker in einer freigegebenen Anweisung ist eine Falle für die Vertretung.
- Fristen, Betragsgrenzen und Rechtsgrundlagen durch den Berufsträger bestätigen lassen.
- Prüfen, ob der Freigabeschritt berufsrechtlich richtig verortet ist: Was dem Berufsträger vorbehalten ist, darf die Anweisung nicht an die Sachbearbeitung delegieren.
- Verantwortliche als Rolle prüfen, nicht als Name – sonst ist die Anweisung beim nächsten Personalwechsel wertlos.

## Varianten

- **Einarbeitung:** "Erzeuge zusätzlich eine Kurzfassung für den ersten Tag: nur die Schritte, die eine neue Kraft ohne Rückfrage ausführen darf."
- **Mehrere Beschreiber:** Stichworte von zwei Bearbeitern getrennt einfügen und ergänzen: "Stelle Abweichungen zwischen beiden Beschreibungen gegenüber und markiere sie als zu entscheiden."
- **Prüfliste statt Fließtext:** "Erzeuge aus der Anweisung eine abhakbare Prüfliste (Kästchen ☐ vor jedem Schritt) für den laufenden Betrieb."
