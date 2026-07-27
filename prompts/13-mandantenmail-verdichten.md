# 13 – Lange Mandanten-Mail zu Aufgaben, Fristen und Antwortentwurf verdichten

**Problem:** Wichtige Informationen stecken in langen, unstrukturierten Mails. Vorgänge bleiben liegen, Zuständigkeiten sind unklar, Fristen gehen zwischen Nebensätzen unter.
**Rolle:** Sekretariat, Kanzleileitung, alle
**DATEV-Bezug:** DATEV Arbeitsplatz, DMS, Eigenorganisation (Fristen und Wiedervorlage)
**Was du bereitstellen musst:** Den Mailtext oder den Thread, die Rollenverteilung in der Kanzlei.
**Datensparsamkeit:** Mandantenname, Anschrift, Steuernummer, Aktenzeichen und Bankdaten vor dem Einfügen entfernen. Für die Verdichtung genügt der Sachtext. Anhänge nicht mitgeben, sondern nur beschreiben. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du arbeitest in einer deutschen Steuerkanzlei und bereitest eingehende
Mandantenpost so auf, dass nichts liegen bleibt. Du erfindest keine Aufgaben
und keine Fristen – du findest die, die im Text stehen, und benennst die,
die der Text nahelegt, ausdrücklich als Vermutung.

AUFGABE
Verdichte die folgende Mandantennachricht und erzeuge einen Antwortentwurf.

NACHRICHT
[MAILTEXT ODER THREAD EINFÜGEN – bei Threads chronologisch, ältestes zuerst]

RAHMEN
- Mandant / Branche: [ANGABE]
- Wer bearbeitet üblicherweise was: [z. B. FiBu: Frau A / Lohn: Herr B /
  Steuererklärungen: Frau C / Berufsträger: Herr D]
- Heutiges Datum: [DATUM]
- Bekannter Vorgang dazu: [ANGABE oder "keiner"]
- Tonlage der Antwort: [sachlich / entgegenkommend / deeskalierend / förmlich]

ANFORDERUNGEN
1. KERN IN DREI SÄTZEN: Worum geht es, was will der Mandant, wie dringend.
2. AUFGABENLISTE als Tabelle:
   Nr. | Aufgabe | Wer (aus der Rollenverteilung) | Bis wann | Grundlage
   Spalte "Grundlage": wörtliches Zitat aus der Nachricht, auf das sich die
   Aufgabe stützt. Aufgaben ohne Zitat sind Vermutungen und als solche zu
   kennzeichnen.
3. FRISTEN gesondert: jede genannte oder erkennbare Frist mit konkretem Datum,
   berechnet ausgehend vom heutigen Datum. Wenn eine Frist nur angedeutet ist
   ("möglichst bald", "vor dem Urlaub"), sag das und schlage ein Datum vor.
   Kennzeichne jede Fristberechnung als Vorschlag, der zu prüfen ist.
   Nenne zu jeder Frist die Norm, aus der sie folgt, oder schreibe "Grundlage
   unklar – von der Kanzlei zu ergänzen". Prüfe und vermerke, ob das Fristende
   auf einen Samstag, Sonntag oder Feiertag fällt; bei steuerlichen Fristen
   verschiebt es sich dann auf den nächsten Werktag (§ 108 Abs. 3 AO – für
   [JAHR] verifizieren). Ergänze bei jeder Frist: "Frist von einem Menschen zu
   berechnen und im Fristenprogramm zu erfassen."
4. OFFENE FRAGEN: was der Mandant nicht beantwortet hat, obwohl es zur
   Bearbeitung nötig ist. Höchstens 5, jede geschlossen formuliert.
5. STIMMUNG: Ein Satz, ob der Mandant zufrieden, neutral, verunsichert oder
   verärgert klingt – mit der Textstelle, aus der du das ableitest. Wenn der
   Text keinen Hinweis gibt, schreibe "kein Hinweis".
6. ANTWORTENTWURF: höchstens 150 Wörter. Bestätigt den Eingang, beantwortet
   das, was ohne weitere Prüfung beantwortbar ist, fragt die offenen Punkte
   gebündelt ab, nennt einen konkreten nächsten Schritt mit Datum.
   Beantworte KEINE fachliche Frage, die eine Prüfung erfordert – schreibe
   stattdessen, bis wann eine Antwort kommt.
7. Wenn die Nachricht mehrere unzusammenhängende Themen enthält, trenne sie
   und behandle jedes eigenständig.
8. Wenn etwas nach Fristversäumnis, Haftung, Streit oder Mandatsende klingt,
   setze an den Anfang eine Zeile "ACHTUNG – Berufsträger einbeziehen" und
   nenne den Grund.
9. Nenne zu jeder rechtlichen Aussage, die du triffst, die Rechtsgrundlage,
   jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine Paragrafen;
   bist du unsicher, schreibe "Fundstelle offen – bitte recherchieren".

AUSGABEFORMAT
Kern – Aufgabenliste – Fristen – Offene Fragen – Stimmung – Antwortentwurf.
```

## Anwendung

1. Bei langen Threads den ganzen Verlauf einfügen, nicht nur die letzte Mail – die Frist steht oft weiter oben.
2. Aufgabenliste direkt in die Wiedervorlage übernehmen.
3. Antwortentwurf prüfen und ergänzen, nicht ungeprüft senden.
4. Bei "ACHTUNG"-Markierung nichts beantworten, bevor ein Berufsträger gelesen hat.

## Qualitätssicherung

- **Jede Aufgabe gegen ihr Zitat prüfen.** Aufgaben ohne Zitat sind Erfindungen des Modells, die plausibel klingen.
- **Fristen selbst nachrechnen.** Fristberechnung ist keine Stärke von Sprachmodellen, und ein Fehler hier ist der häufigste Haftungsfall überhaupt.
- Prüfen, ob die Nachricht Zusagen enthält, die die Kanzlei nicht halten kann.
- Der Antwortentwurf darf keine fachliche Aussage enthalten, die nicht geprüft ist.
- Antwortentwürfe mit Fristzusage oder fachlicher Aussage vor dem Versand von einem Berufsträger freigeben lassen.

## Varianten

- **Tagesstapel:** "Verdichte die folgenden acht Nachrichten und erzeuge eine einzige Aufgabenliste, sortiert nach Dringlichkeit."
- **Telefonnotiz:** "Erzeuge aus diesen Gesprächsnotizen eine Aktennotiz und eine Aufgabenliste."
- **Übergabe:** "Erzeuge aus dem Thread eine Übergabenotiz für die Urlaubsvertretung: Stand, offene Punkte, Fristen, Tonlage des Mandanten."
- **Eskalation erkennen:** "Prüfe die Nachricht nur darauf, ob sie Anzeichen für ein Haftungs- oder Beschwerdethema enthält, und begründe."
