# 02 – Gebündelte Rückfrageliste zu unklaren Bankumsätzen

**Problem:** Zu jedem unklaren Bankumsatz geht eine einzelne Mail an den Mandanten; pro Monat entstehen Dutzende Mikro-Nachrichten und ebenso viele Antworten.
**Rolle:** Buchhaltung
**DATEV-Bezug:** Kanzlei-Rechnungswesen (Bankbuchungen, offene Posten), DATEV Unternehmen online
**Was du bereitstellen musst:** Export oder Abschrift der unklaren Umsätze (Datum, Betrag, Verwendungszweck, Gegenseite).
**Datensparsamkeit:** Mandantenname, IBAN und Klarnamen Dritter durch Platzhalter ersetzen (`Mandant A`, `Konto ****1234`, `Zahlungsempfänger 1`). Für die Klärung genügen Datum, Betrag, Verwendungszweck und Art der Gegenseite. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Buchhalterin in einer deutschen Steuerkanzlei. Du bereitest die
Rückfragen an einen Mandanten so auf, dass er sie in einem Durchgang
beantworten kann.

AUFGABE
Erzeuge aus der folgenden Liste unklarer Bankumsätze EINE gebündelte
Rückfrage an den Mandanten.

KONTEXT
- Mandant: [MANDANT / BRANCHE]
- Zeitraum: [ZEITRAUM]
- Konto: [BEZEICHNUNG, z. B. Geschäftskonto 1]
- Unklare Umsätze (Datum | Betrag | S/H | Verwendungszweck | Gegenseite):
  [LISTE EINFÜGEN]

ANFORDERUNGEN
1. Gruppiere die Umsätze nach Rückfrage-Typ, z. B.
   A) Beleg fehlt vollständig
   B) Betrieblich oder privat? (Zuordnung unklar)
   C) Zahlung ohne erkennbaren Bezug (Vorschuss, Verrechnung, Storno?)
   D) Wiederkehrende Zahlung – bitte einmalig grundsätzlich klären
   Nimm nur Gruppen auf, die tatsächlich vorkommen.
2. Formuliere je Position EINE geschlossene Frage, die mit einem Wort oder
   einem Beleg beantwortbar ist. Keine offenen Fragen wie "Was war das?",
   sondern z. B. "Handelt es sich um die Anzahlung für <erkennbarer Bezug>?
   Falls ja, bitte die Rechnung nachreichen."
3. Nutze den Verwendungszweck, um eine begründete Vermutung anzubieten.
   Kennzeichne jede Vermutung ausdrücklich als Vermutung.
4. Erzeuge eine Tabelle mit den Spalten:
   Nr. | Datum | Betrag | Verwendungszweck (gekürzt) | Unsere Frage | Antwort des Mandanten (leer)
5. Schreibe darüber ein Anschreiben von höchstens 120 Wörtern mit
   Frist [DATUM] und einem Satz, warum die Klärung nötig ist.
6. Erzeuge zusätzlich eine interne Kurzliste: welche Positionen bei
   ausbleibender Antwort wie vorläufig gebucht werden können
   (z. B. Verrechnungskonto, Privatentnahme) – als Vorschlag zur Prüfung,
   nicht als Entscheidung.
7. Wenn eine Position aus dem Verwendungszweck eindeutig zuzuordnen ist,
   nimm sie NICHT in die Mandantenliste auf, sondern in eine separate
   Rubrik "Von uns geklärt – keine Rückfrage nötig" mit Begründung.
8. Nenne zu jeder rechtlichen Aussage – etwa zur Behandlung einer
   Privatentnahme oder eines Verrechnungsvorgangs – die Rechtsgrundlage
   (Norm mit Absatz und Satz), jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Solche Aussagen gehören ausschließlich in die
   interne Kurzliste, nicht in den Mandantentext. Erfinde keine Paragrafen;
   bist du unsicher, schreibe "Fundstelle offen – bitte recherchieren".

AUSGABEFORMAT
1. Anschreiben  2. Rückfragetabelle  3. Von uns geklärt  4. Interne Kurzliste
```

## Anwendung

1. Unklare Umsätze aus dem Buchungsstapel oder der Bankdatei zusammenstellen (CSV-Export reicht).
2. Kontonummern und Namen Dritter maskieren.
3. Prompt ausführen, Tabelle als Anlage (PDF oder Excel) an den Mandanten geben.
4. Antwortspalte zurück in die Buchung übernehmen.

## Qualitätssicherung

- Jede vom Modell angebotene Vermutung gegen den tatsächlichen Verwendungszweck prüfen – Modelle raten hier plausibel, aber nicht immer richtig.
- Die interne Kurzliste ist ein Vorschlag; die Buchungsentscheidung trifft die Kanzlei.
- Stichprobe: mindestens drei Positionen selbst nachvollziehen, bevor die Liste rausgeht.
- **Vier-Augen-Prinzip und Freigabe:** Die Liste ist ein Entwurf. Vor dem Versand muss eine zweite Person die Rückfragetabelle und die Rubrik "Von uns geklärt" gegenlesen – eine als geklärt eingestufte, tatsächlich offene Position ist der teuerste Fehler dieser Auswertung. Die Freigabe zur Weitergabe an den Mandanten erteilt ein Berufsträger; die Freigabe ist zu dokumentieren.

## Varianten

- **Kreditkarte:** Gruppen um "Privatnutzung?" und "Beleg auf Fremdwährung" ergänzen.
- **Jahresarbeit:** Zusatzanweisung "Fasse gleichartige Positionen zu einer einzigen Grundsatzfrage zusammen und liste die betroffenen Datumsangaben nur als Anhang."
- **Kassenumsätze:** Spalte "Kassenbericht vorhanden (ja/nein)" ergänzen lassen.
