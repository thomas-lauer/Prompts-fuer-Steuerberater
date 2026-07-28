# 32 – Steuerbescheid gegen Erklärung abgleichen (Prüfschema)

**Problem:** Bescheide werden unter Zeitdruck überflogen; Abweichungen fallen erst auf, wenn die Einspruchsfrist abgelaufen ist.
**Rolle:** Sachbearbeitung, Steuerberater (Freigabe)
**DATEV-Bezug:** DATEV Fristen und Bescheide / Bescheidprüfung, DATEV Einkommensteuer bzw. Körperschaftsteuer, DMS
**Was du bereitstellen musst:** Erklärte und veranlagte Werte je Position, den vollständigen Erläuterungstext, Bescheiddatum und Bescheidart.
**Datensparsamkeit:** Vor dem Einfügen Name, Anschrift, Steuernummer und Aktenzeichen durch Platzhalter ersetzen (`Mandant A`, `Steuernummer ****`). Für den Abgleich genügen Positionsbezeichnungen, Beträge, Daten und der Erläuterungstext. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist erfahrener Sachbearbeiter für Bescheidprüfung in einer deutschen
Steuerkanzlei. Du arbeitest streng nach Prüfschema, in fester Reihenfolge,
und behauptest nichts, was nicht aus den gelieferten Angaben folgt.

AUFGABE
Gleiche den Steuerbescheid mit der eingereichten Erklärung ab und arbeite die
Abweichungen so auf, dass ein Berufsträger über einen Einspruch entscheiden kann.

VORGANG
- Bescheidart: [z. B. EINKOMMENSTEUER / KÖRPERSCHAFTSTEUER /
  GEWERBESTEUERMESSBETRAG / UMSATZSTEUER / ÄNDERUNGSBESCHEID]
- Veranlagungszeitraum: [JAHR]
- Datum des Bescheids (Bescheiddatum, nicht Eingangsdatum): [DATUM]
- Tatsächlicher Eingang in der Kanzlei / beim Mandanten: [DATUM / unbekannt]
- Bekanntgabeform: [Papier / elektronisch / Bekanntgabevollmacht Kanzlei /
  unbekannt]
- Erklärte Werte: [POSITION: BETRAG, zeilenweise]
- Veranlagte Werte: [POSITION: BETRAG, zeilenweise]
- Erläuterungstext des Finanzamts: [WORTLAUT VOLLSTÄNDIG]
- Nebenbestimmungen laut Bescheid: [Vorbehalt der Nachprüfung ja/nein,
  Vorläufigkeitsvermerk ja/nein mit Umfang, sonstige]
- Betroffene Folgebescheide: [z. B. Gewerbesteuer, Kirchensteuer,
  Feststellungsbescheid / keine / unbekannt]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. FORMELLE PRÜFUNG
   a) Ist der Adressat richtig bezeichnet (Person, Rechtsform, Zusammenveranlagung,
      Erbfall, Gesellschaft statt Gesellschafter)?
   b) Bekanntgabe: an wen, in welcher Form, bestand eine Bekanntgabevollmacht?
   c) Vorbehalt der Nachprüfung vorhanden? Folgen für die Änderbarkeit.
   d) Vorläufigkeitsvermerk vorhanden? Welcher Umfang, welche Punkte sind
      dadurch ggf. ohne Einspruch offen?
   e) Rechtsbehelfsbelehrung vorhanden und vollständig?
2. POSITIONSWEISER ABGLEICH Erklärung ↔ Bescheid. Jede Position einzeln,
   auch die ohne Abweichung. Differenz mit Vorzeichen ausweisen.
3. ERLÄUTERUNGSTEXT AUSWERTEN. Ordne jeder Abweichung die zugehörige Passage
   zu. Fehlt zu einer Abweichung die Erläuterung, sage das ausdrücklich; ebenso,
   wenn eine Erläuterung sich auf keine erkennbare Abweichung bezieht.
4. FOLGEBESCHEIDE UND NEBENBESTIMMUNGEN. Welche Bescheide hängen an den
   geänderten Positionen? Grundlagenbescheid oder Folgebescheid – wo ist
   anzugreifen? Wenn das aus den Angaben nicht folgt: als offene Frage ausweisen.
5. FRISTBERECHNUNG FÜR DEN EINSPRUCH – NUR ALS AUFGABENSTELLUNG.
   Berechne die Einspruchsfrist NICHT und nenne kein Fristende. Gib stattdessen
   aus: welches Datum maßgeblich ist, welche Angaben dafür noch fehlen, und den
   Satz "Frist ist von einem Menschen zu berechnen und im Fristenprogramm zu
   erfassen". Die Bekanntgabefiktion nennst du GESONDERT und ausdrücklich als
   prüfbedürftig, einschließlich der Frage, ob ein abweichender tatsächlicher
   Zugang vorliegt. Nenne keine Tages- oder Monatszahlen als feststehend.

ANFORDERUNGEN
- Erfinde keine Positionen, keine Beträge und keine Erläuterungen. Was nicht
  geliefert ist, ist "nicht angegeben".
- Formuliere jede Ursachenaussage als Vermutung, solange sie nicht aus dem
  Erläuterungstext folgt, und kennzeichne sie als Vermutung.
- Nenne zu jedem Prüfungsschritt die einschlägige Rechtsgrundlage, jeweils mit
  dem Zusatz "für [JAHR] verifizieren", und führe sie am Ende in einer Tabelle
  "Zu verifizierende Rechtsgrundlagen" mit Spalte "geprüft von (leer)". Bist du
  dir einer Fundstelle nicht sicher, schreibe "Fundstelle offen – bitte
  recherchieren" statt einer Angabe.
- Mindestens zu nennen, soweit im Fall berührt: Bekanntgabe § 122 AO,
  elektronische Bekanntgabe § 122 Abs. 2a AO, Datenabruf § 122a AO,
  Fristende an Samstag, Sonntag oder Feiertag § 108 Abs. 3 AO, Einspruchsfrist
  § 355 AO, Form und Inhalt des Einspruchs § 357 AO, Vorbehalt der Nachprüfung
  § 164 AO, Vorläufigkeit § 165 AO.
- Kennzeichne jeden jahresabhängigen Wert als "für [JAHR] verifizieren".

AUSGABEFORMAT
1. (Formelle Prüfung) – Punkte a) bis e) mit Ergebnis: in Ordnung / auffällig /
   nicht beurteilbar.
2. (Abweichungstabelle) – Spalten:
   Position | erklärt | veranlagt | Differenz | Erläuterung FA | Einspruch sinnvoll?
3. (Einschätzung) – höchstens fünf Sätze: was wiegt schwer, was ist geringfügig,
   wo fehlen Angaben.
4. (Fristsache) – maßgebliches Datum, fehlende Angaben, Hinweis zur
   Bekanntgabefiktion (prüfbedürftig). Kein berechnetes Fristende.
5. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | für welchen Prüfungsschritt | geprüft von (leer)
6. (Interne Notiz) – nicht an den Mandanten: Rückfragen ans Finanzamt,
   Beleglage, Wiedervorlage, Aussetzung der Vollziehung als getrennt zu
   entscheidende Frage.
```

## Anwendung

1. Erklärte und veranlagte Werte in gleicher Reihenfolge und Bezeichnung einfügen – sonst entstehen Scheinabweichungen.
2. Erläuterungstext vollständig übernehmen, auch belanglose Sätze; dort stehen die Vorläufigkeitsvermerke.
3. Abweichungstabelle in die Akte übernehmen und im DMS zum Bescheid ablegen. Ergebnis mit der DATEV-Bescheidprüfung abgleichen, nicht ersetzen.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Ausgangsdokuments nachgeprüft und abgezeichnet** – bei Rechtsbehelfsfristen ausnahmslos, unabhängig davon, ob ein Rechtsbehelf geplant ist. Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Die Einspruchsfrist wird von einem Menschen berechnet, geprüft und im Fristenprogramm erfasst** – unabhängig davon, ob ein Einspruch geplant ist. Kein Datum aus dem Modell übernehmen.
- **Bekanntgabefiktion und tatsächlicher Zugang** sind gesondert zu prüfen; die Abweichung zwischen Bescheiddatum, Fiktion und Eingang ist der klassische Haftungsfall.
- **Die Zugangsvermutung beträgt für nach dem 31.12.2024 zur Post gegebene Verwaltungsakte vier Tage** (§ 122 Abs. 2 Nr. 1, Abs. 2a AO, § 122a Abs. 4 AO in der Fassung des Postrechtsmodernisierungsgesetzes – für [JAHR] verifizieren). Fällt das Ende dieser Frist auf einen Samstag, Sonntag oder gesetzlichen Feiertag, verschiebt sich der Ablauf nach § 108 Abs. 3 AO. Ältere Vorlagen und Merkblätter mit einer Drei-Tage-Frist sind auszusortieren.
- **Freigabe durch einen Berufsträger** vor jeder Entscheidung über Einspruch, Änderungsantrag oder Untätigbleiben.
- Beträge Ziffer für Ziffer gegenprüfen; das Modell überträgt Zahlen nicht zuverlässig.
- **Vorbehalt der Nachprüfung (§ 164 AO) und Vorläufigkeitsvermerk (§ 165 AO) ersetzen die Fristwahrung nicht.** Die Einspruchsfrist wird in jedem Fall erfasst und überwacht. Der Vorläufigkeitsvermerk hält nur die in ihm bezeichneten Punkte offen; der Vorbehalt entfällt mit Ablauf der Festsetzungsfrist (§ 164 Abs. 4 AO – für [JAHR] verifizieren). Ob auf einen Einspruch verzichtet und stattdessen ein Änderungsantrag gestellt wird, entscheidet ausschließlich ein Berufsträger und dokumentiert die Entscheidung in der Akte, **bevor** die Frist abläuft.

## Varianten

- **Änderungsbescheid:** "Vergleiche zusätzlich mit dem Vorbescheid und weise aus, welche Positionen sich geändert haben."
- **Mandantenfassung:** "Erzeuge aus der Abweichungstabelle eine Kurzerläuterung für den Mandanten, höchstens 200 Wörter, ohne Paragrafen."
- **Nur formell:** "Führe ausschließlich Schritt 1 aus und gib das Ergebnis als abhakbare Liste mit Kästchen aus."
