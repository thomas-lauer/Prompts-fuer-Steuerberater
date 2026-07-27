# 11 – Fachtext in Mandantensprache übersetzen

**Problem:** Schreiben der Kanzlei sind juristisch korrekt und für den Mandanten unverständlich. Er ruft an, fragt nach oder – schlimmer – fragt nicht nach und handelt falsch.
**Rolle:** alle
**DATEV-Bezug:** übergreifend (DMS, Mandantenkorrespondenz, DATEV Meine Steuern)
**Was du bereitstellen musst:** Den Ausgangstext, den Adressaten und das, was der Mandant nach dem Lesen tun soll.
**Datensparsamkeit:** Mandantenname, Anschrift, Steuernummer und Aktenzeichen vor dem Einfügen entfernen oder durch `Mandant A` ersetzen. Für die Übersetzung genügt der Sachtext. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du übersetzt Fachtexte einer deutschen Steuerkanzlei in eine Sprache, die
Unternehmer und Privatpersonen ohne steuerliche Vorbildung verstehen.
Du vereinfachst die Sprache, nicht den Inhalt. Du lässt nichts weg, was
rechtlich wirkt, und du fügst nichts hinzu, was nicht im Ausgangstext steht.

AUFGABE
Erzeuge aus dem folgenden Fachtext eine Fassung für den Mandanten.

AUSGANGSTEXT
[TEXT EINFÜGEN – z. B. Auszug aus einem Bescheid, ein Gesetzestext,
 eine Verfügung, ein Beratungsvermerk, ein Prüfungsbericht]

ADRESSAT
- Wer liest das: [z. B. Handwerksmeister ohne kaufmännische Ausbildung /
  Geschäftsführerin einer GmbH / Privatperson / Erbengemeinschaft]
- Vorwissen: [keines / Grundkenntnisse / kaufmännisch versiert]
- Verhältnis: [Sie-Form förmlich / Sie-Form vertraut / Du-Form]

ZWECK
- Was soll der Mandant nach dem Lesen TUN: [z. B. Unterlagen nachreichen,
  einer Fristverlängerung zustimmen, eine Entscheidung treffen, nichts –
  nur informiert sein]
- Wie eilig ist es: [ANGABE]
- Was auf keinen Fall missverstanden werden darf: [ANGABE]

ANFORDERUNGEN
1. Erzeuge ZWEI Fassungen:
   A) KURZFASSUNG – höchstens 5 Sätze. Was ist passiert, was bedeutet es für
      Sie, was ist zu tun. Muss allein für sich verständlich sein.
   B) ERLÄUTERUNG – höchstens 300 Wörter, gegliedert mit Zwischenüberschriften.
2. Ersetze Fachbegriffe durch Alltagssprache. Wo ein Fachbegriff stehen
   bleiben MUSS, weil der Mandant ihm wieder begegnen wird, nenne ihn einmal
   und erkläre ihn in einem Halbsatz in Klammern.
3. Löse jede Abkürzung beim ersten Vorkommen auf.
4. Zitiere keine Paragrafen im Fließtext. Wenn eine Rechtsgrundlage genannt
   werden muss, setze sie ans Ende in eine Zeile "Rechtsgrundlage: …".
   Nenne dort zu jeder rechtlichen Aussage, die die Fassung übernimmt, die
   Rechtsgrundlage, jeweils mit dem Zusatz "für [JAHR] verifizieren".
   Übernimm dort ausschließlich Fundstellen, die im Ausgangstext stehen.
   Ergänze keine eigenen. Wenn der Ausgangstext keine nennt, lasse die Zeile
   weg. Erfinde keine Paragrafen; bist du bei einer im Ausgangstext genannten
   Fundstelle unsicher, schreibe "Fundstelle offen – bitte recherchieren".
5. Formuliere aktiv und in kurzen Sätzen. Vermeide Passiv, Nominalstil
   ("die Inanspruchnahme der Möglichkeit der …") und Schachtelsätze.
6. Wandle Bedingungen in Wenn-dann-Sätze um.
7. Wenn der Ausgangstext eine Frist enthält, muss sie in BEIDEN Fassungen
   mit Datum stehen.
8. Schließe mit einem Abschnitt "Was jetzt zu tun ist" als nummerierte Liste
   mit höchstens drei Punkten. Wenn nichts zu tun ist, schreibe das ausdrücklich.
9. Verändere die Aussage nicht. Wenn der Ausgangstext eine Einschränkung,
   einen Vorbehalt oder eine Bedingung enthält, muss sie erhalten bleiben –
   auch wenn sie die Botschaft komplizierter macht.
10. Liste am Ende gesondert unter "Prüfen vor dem Versand" auf:
    a) welche Vereinfachungen inhaltlich heikel sind,
    b) welche Aussagen des Ausgangstexts du nicht sicher verstanden hast,
    c) welche Angaben aus dem Ausgangstext du bewusst weggelassen hast.

AUSGABEFORMAT
A Kurzfassung – B Erläuterung – Was jetzt zu tun ist – Rechtsgrundlage –
Prüfen vor dem Versand (nicht an den Mandanten).
```

## Anwendung

1. Ausgangstext vollständig einfügen, nicht gekürzt – Kürzungen erzeugen genau die Auslassungen, die später Ärger machen.
2. Den Zweck ehrlich angeben. "Nur informieren" ergibt einen anderen Text als "muss zustimmen".
3. Abschnitt "Prüfen vor dem Versand" durchgehen und danach löschen.
4. Bewährte Übersetzungen als Textbausteine sammeln – dieselben Bescheidarten kommen wieder.

## Qualitätssicherung

- **Ausgangstext und Übersetzung nebeneinander legen.** Der typische Fehler ist nicht die falsche Formulierung, sondern die verlorene Einschränkung.
- Fristen und Beträge Ziffer für Ziffer abgleichen.
- Prüfen, ob die Kurzfassung allein stehen kann – viele Mandanten lesen nur sie.
- **Die Übersetzung ist ein Entwurf, keine freigegebene Mandantenkorrespondenz.** Vor dem Versand von einem Berufsträger freigeben lassen – zwingend bei Bescheiden, Einsprüchen und allem mit Rechtsfolge (Freigabestufe 3 in `DATENSCHUTZ.md`). Vier-Augen-Prinzip: Ausgangstext und Übersetzung werden von einer zweiten Person verglichen.
- **Fristen und Daten prüft und erfasst ein Mensch.** Kein Datum aus der KI-Antwort übernehmen; bei Rechtsbehelfsfristen ausnahmslos eine zweite Person zur Nachprüfung.
- Keine Verbindlichkeit erzeugen, die der Ausgangstext nicht hat. Aus "kann" wird leicht "wird".

## Varianten

- **Rückrichtung:** "Formuliere aus dieser Mandantenschilderung eine fachlich präzise Sachverhaltsdarstellung für die Akte."
- **Vorlesefassung:** "Erzeuge eine Fassung, die man am Telefon vorlesen kann, ohne zu stocken."
- **Einfache Sprache:** "Erzeuge zusätzlich eine Fassung in einfacher Sprache, Sätze mit höchstens 12 Wörtern."
- **Fremdsprache:** "Erzeuge zusätzlich eine englische Fassung – fachlich gleichwertig, nicht wörtlich übersetzt."
