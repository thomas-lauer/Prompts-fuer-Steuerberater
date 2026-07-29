# Prompt-Baukasten

Wiederverwendbare Bausteine, um eigene Prompts für die Kanzlei zu schreiben oder
die vorhandenen anzupassen. Jeder Baustein ist zum Kopieren gedacht.

Die Reihenfolge unten ist die empfohlene Reihenfolge im Prompt:
**Rolle → Arbeitsweise → Aufgabe → Kontext → Anforderungen → Ausgabeformat.**

---

## 1. Rolle

Nicht nur *wer*, sondern *wie diese Person arbeitet*. Der zweite Satz verändert
das Ergebnis stärker als der erste.

```text
Du bist Bilanzbuchhalter mit langjähriger Erfahrung in einer deutschen
Steuerkanzlei und arbeitest mit DATEV Kanzlei-Rechnungswesen.
```

```text
Du bist Umsatzsteuer-Spezialist. Du arbeitest streng nach Prüfschema und
behauptest nichts, was du nicht begründen kannst.
```

```text
Du bist erfahrene Kanzleimitarbeiterin und schreibst Mandantenkorrespondenz.
Dein Stil: höflich, klar, kurze Sätze, keine Floskeln, keine Vorwürfe,
immer mit konkretem nächsten Schritt.
```

```text
Du prüfst hypothesengeleitet: erst mögliche Ursachen sammeln, dann nach
Wahrscheinlichkeit und Prüfaufwand sortieren, dann konkrete Prüfschritte nennen.
```

## 2. Der Unsicherheitsbaustein

**Der wichtigste Baustein der ganzen Sammlung.** Ohne ihn liefert ein
Sprachmodell falsche Zahlen im Ton der Gewissheit. Immer einbauen, sobald
Rechtsstände, Beträge, Kontonummern oder Fundstellen im Spiel sind.

```text
Kennzeichne ausdrücklich jede Aussage, bei der du dir nicht sicher bist oder
bei der sich die Rechtslage geändert haben könnte. Rate nicht.
Nenne KEINE konkreten Jahreswerte (Pauschbeträge, Freigrenzen,
Beitragsbemessungsgrenzen, Steuersätze), ohne sie als
"für [JAHR] verifizieren" zu markieren.
Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
"für [JAHR] verifizieren". Erfinde keine Paragrafen, BMF-Schreiben oder
Aktenzeichen. Kennst du eine Fundstelle nicht sicher, schreibe
"Fundstelle offen – bitte recherchieren" statt einer Angabe.
```

**Der Markertext lautet wörtlich und ausnahmslos `für [JAHR] verifizieren`.**
Präfixe dürfen davorstehen (`Betragsgrenze – für [JAHR] verifizieren`,
`Fundstelle – für [JAHR] verifizieren`), die Kernzeichenfolge bleibt unverändert.
Abweichende Formulierungen sind Fehler: die Strukturprüfung sucht mechanisch
nach diesem Text, und ein Marker, der nicht gefunden wird, bleibt stehen.

**Das Verbot allein genügt nicht.** "Erfinde keine Paragrafen" verhindert
Halluzinationen, macht aber die Anweisung "am Rechtsstand verifizieren"
unausführbar – der Berufsträger erfährt nicht, was er nachschlagen soll.
Immer beides: Fundstelle einfordern *und* als prüfbedürftig markieren.

Als eigener Ausgabeabschnitt wirkt er stärker als als Nebensatz:

```text
Schließe mit einem Abschnitt "Was ich nicht sicher weiß".
```

Warum das trägt: Eine reine Verbotsformel ("erfinde nichts") ist schwach, weil
sie keine Handlungsalternative anbietet. Die Formel oben gibt eine – das Modell
kann der Anweisung folgen, statt sie zu ignorieren.

## 3. Eindeutigkeitsprüfung vorweg

Verhindert, dass das Modell einen unterbestimmten Sachverhalt entscheidet,
statt nachzufragen.

```text
Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab:
eindeutig / vertretbare Varianten / nicht ohne weitere Angaben entscheidbar.
Wenn Angaben fehlen, liste sie auf und arbeite mit klar benannten Annahmen.
```

## 4. Kontextblock

Immer als ausgefüllte Feldliste, nie als Fließtext. Platzhalter in
GROSSBUCHSTABEN in eckigen Klammern.

```text
MANDANTENRAHMEN
- Kontenrahmen: [SKR03 / SKR04]
- Rechtsform: [z. B. Einzelunternehmen / GmbH / Freiberufler-GbR]
- Gewinnermittlung: [Bilanz / EÜR]
- Umsatzsteuer: [Regelbesteuerung / Kleinunternehmer § 19 / teilweise steuerfrei]
- Besonderheiten: [z. B. Ist-Versteuerung, Vorsteuerabzug eingeschränkt]
```

Faustregel: Jedes Feld, das man weglassen kann, ohne dass sich die Antwort
ändert, gehört nicht in den Prompt. Jedes Feld, dessen Fehlen das Modell zum
Raten zwingt, ist Pflicht.

## 5. Datensparsamkeitszeile

Gehört in den Dateikopf, nicht in den Prompt-Block – sie richtet sich an den
Menschen, nicht an das Modell.

```markdown
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Steuernummer,
Personalnummern und Namen Dritter durch Platzhalter ersetzen
(`Mandant A`, `AN 1`, `Konto ****1234`).
Für die fachliche Prüfung genügen Rolle, Beträge, Konten und Daten.
```

Einzelheiten in `DATENSCHUTZ.md`.

## 6. Weglassen erzwingen

Der Baustein, der über brauchbar und unbrauchbar entscheidet. Vollständige
Listen und Rundum-Kommentare werden nicht gelesen.

```text
Erläutere höchstens FÜNF Positionen. Wähle die mit der größten Abweichung
oder der größten Steuerungsrelevanz. Ignoriere den Rest bewusst.
```

```text
Nimm NUR Positionen auf, die zu diesem Profil passen. Lasse alles weg, was
nicht zutrifft. Eine kurze zutreffende Liste ist besser als eine vollständige
unzutreffende.
```

```text
Wenn eine Position eindeutig geklärt ist, nimm sie NICHT in die Mandantenliste
auf, sondern in eine separate Rubrik "Von uns geklärt – keine Rückfrage nötig".
```

## 7. Tonalität für Mandantentexte

```text
Sprache: Sie-Form, keine Abkürzungen ohne Auflösung, keine Fachbegriffe ohne
kurze Erklärung in Klammern. Maximal [ZAHL] Wörter.
```

```text
Erkläre jeden Fachbegriff, den du verwendest, in einem Halbsatz in Klammern.
```

```text
Du erklärst, ohne zu belehren, und du beruhigst nicht durch Verharmlosung,
sondern durch Nachvollziehbarkeit.
```

```text
Passe die Anrede an: [Sie-Form förmlich / Sie-Form vertraut / Du-Form].
```

## 8. Vermutung als Vermutung kennzeichnen

Gegen die häufigste Fehlerart bei Kommentaren und Analysen: die plausible,
aber erfundene Ursache.

```text
Formuliere jede Ursachenaussage als Vermutung oder Frage, solange sie nicht
aus den gelieferten Angaben eindeutig folgt. Keine erfundenen Gründe.
Kennzeichne jede Vermutung ausdrücklich als Vermutung.
```

## 9. Interne und externe Ausgabe trennen

Kostet nichts und verhindert, dass Vorbehalte in die Mandantenkommunikation
rutschen.

```text
Erzeuge zusätzlich eine "Interne Notiz" mit dem, was die Kanzlei noch prüfen
sollte und was nicht an den Mandanten geht.
```

## 10. Ausgabeformat

Ohne Vorgabe entsteht Fließtext, den niemand weiterverarbeiten kann.

```text
AUSGABEFORMAT
1. Anschreiben  2. Tabelle  3. Interne Notiz
```

Tabellen mit leerer Antwortspalte machen aus einem Text ein Arbeitsmittel:

```text
Erzeuge eine Tabelle mit den Spalten:
Nr. | Datum | Betrag | Unsere Frage | Antwort des Mandanten (leer)
```

Abhakbare Listen:

```text
Erzeuge die Liste so, dass sie ausgedruckt abhakbar ist
(Kästchen ☐ vor jeder Position).
```

## 11. Prüfschema-Baustein

Für alles, was rechtlich geprüft wird. Reihenfolge rückwärts durchgehen und
fragen: Braucht ein Schritt eine Information, die erst später entsteht? Dann
ist das Schema zirkulär.

```text
PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. …
2. …
Gib zu jedem Schritt die Rechtsgrundlage an.
Wenn ein Schritt ohne weitere Angaben nicht entscheidbar ist: sag das
ausdrücklich, benenne die fehlende Angabe und rechne beide Varianten durch.
```

## 12. Anschlussverwendung

```text
Leite aus dem Ergebnis eine wiederverwendbare Checkliste für diesen
Sachverhaltstyp ab.
```

```text
Leite aus der gefundenen Ursache eine Arbeitsanweisung ab, die den Fehler
künftig verhindert.
```

```text
Erzeuge zusätzlich eine Kurzfassung mit maximal [ZAHL] Wörtern.
```

## 13. Freigabe und Vier-Augen

Gehört in den Abschnitt **Qualitätssicherung** der Datei, nicht in den
Prompt-Block – er richtet sich an den Menschen. Fehlt er, ist die Datei
konventionswidrig.

```markdown
- **Das Ergebnis ist ein Entwurf.** Vor dem Versand prüfen: [KONKRETE PRÜFPUNKTE].
- Freigabe durch einen Berufsträger bei allem, was an einen Mandanten oder an
  eine Behörde geht oder rechtlich verbindlich wirkt (Freigabestufe 3 in
  `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch**, bei Rechtsbehelfsfristen
  ausnahmslos eine zweite Person zur Nachprüfung. Kein Datum aus der
  KI-Antwort übernehmen.
```

## 14. Fristen und Rechtsfolgen ausschließen

Sobald ein Prompt in die Nähe von Fristen kommt, gehört dieser Baustein in den
Prompt-Block. Fristversäumnis ist der häufigste Haftungsfall in Steuerkanzleien.

```text
Berechne KEINE Fristen und nenne keine Fristlängen und keine Rechtsfolgen einer
Versäumnis als feststehend. Liste stattdessen auf, WELCHE Fristen im Raum
stehen, jeweils mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren",
ohne Datum und ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu
berechnen und im Fristenprogramm zu erfassen."
```

## 15. Abbruchregel für heikle Sachverhalte

Wenn ein Prompt auf Material trifft, das nach Berichtigungspflicht,
Selbstanzeige, Steuerstrafverfahren oder Haftungsfall aussieht, darf er nicht
weiterarbeiten – solche Sachverhalte gehören nach `DATENSCHUTZ.md` (Zone Rot)
in kein KI-Werkzeug.

```text
ABBRUCHREGEL: Deutet das Material auf eine unrichtige abgegebene Erklärung, eine
Selbstanzeige, ein Steuerstrafverfahren oder ein Organisationsversagen der
Kanzlei hin, arbeite NICHT weiter. Gib nur aus: "Abbruchgrund liegt vor (Grund angeben) –
Bearbeitung an dieser Stelle abgebrochen, Prüfung durch einen Berufsträger
außerhalb des KI-Werkzeugs."
```

**Die Probe aufs Exempel: Fülle den eigenen Sachverhaltsbogen mit dem typischen
Fall aus, für den der Prompt gebaut ist. Feuert die Abbruchregel dabei, ist sie
falsch.** Ein Krisenprompt, dessen Regel bei Beitragsrückständen abbricht, ein
Berichtigungsprompt, dessen Regel bei einer erkannten Unrichtigkeit abbricht,
ein Prüfungsprompt, dessen Regel bei einer Prüfungsanordnung abbricht – jedes
Mal bricht der Prompt in genau dem Fall ab, für den er geschrieben wurde, und
ist damit wertlos. Das ist bis Runde 13 achtmal passiert und war jedes Mal erst
in der Fachprüfung zu sehen, weil die Regel für sich gelesen vernünftig klingt.

Zwei Bedingungen, die eine Abbruchregel deshalb erfüllen muss:

1. **Sie hängt an einem konkreten Feld des Sachverhaltsbogens, nicht an einer
   Beurteilung.** Nicht „die Angaben deuten auf … hin", sondern „im Feld X steht
   ‚ja'". Eine Regel, die das Modell erst beurteilen lässt, ob abzubrechen ist,
   verlangt genau die Beurteilung, die der Prompt sonst verbietet – und feuert
   dann unkontrolliert.
2. **Das auslösende Feld existiert und darf existieren.** Fehlt das Feld, läuft
   die Regel leer. Gehört die Angabe nach `DATENSCHUTZ.md` in die Zone Rot
   (Strafverfahren, Selbstanzeige, nicht abgeführte Arbeitnehmeranteile), darf
   sie auch nicht als „ja/nein" abgefragt werden: Dann ist die Abbruchregel der
   falsche Ort. Die Frage gehört als **Vorschaltfrage in den Abschnitt
   Anwendung**, wird vor dem Werkzeugeinsatz vom Berufsträger beantwortet und in
   der Handakte vermerkt – nicht im Werkzeug.

Trifft ein Grund nur einen Teil der Antwort, ist die Aussteuerung eines
Einzelpunkts das mildere und meist richtige Mittel. Dann heißt die Regel auch
so – eine Überschrift „ABBRUCHREGEL" über einer Anweisung, die den Abbruch
gerade verbietet, liest das Modell zuerst und befolgt sie:

```text
AUSSTEUERUNGSREGEL – kein Abbruch, an objektiven Angaben. Steuere einen
Einzelpunkt aus, wenn die dafür vorgesehene Zeile des Sachverhaltsbogens es
sagt: (a) im Feld "[FELDNAME]" steht "ja". Gib für den ausgesteuerten
Einzelpunkt nur aus: "Ausgesteuert – Prüfung durch einen Berufsträger außerhalb
des KI-Werkzeugs." Beende die Bearbeitung NICHT; arbeite die übrigen Schritte
weiter und führe die ausgesteuerten Punkte gesondert auf.
```

---

## Anti-Muster

Was in Kanzleiprompts regelmäßig schiefgeht:

| Anti-Muster | Warum es schadet | Stattdessen |
|-------------|------------------|-------------|
| "Erstelle einen Text über X" | Ohne Rolle, Format und Länge entsteht Beliebiges | Rolle + Aufgabe + Format + Länge |
| "Sei präzise und korrekt" | Bewertende Adjektive ändern nichts | Konkrete Prüfschritte vorgeben |
| "Beachte die aktuelle Rechtslage" | Das Modell kann das nicht prüfen und behauptet es trotzdem | Unsicherheitsbaustein einsetzen |
| Alle Felder optional | Das Modell füllt Lücken durch Raten | Pflichtfelder benennen, fehlende Angaben einfordern |
| Eine Klammersyntax für zwei Bedeutungen | Anwender versuchen, Ausgabemarker auszufüllen | `[EINGABE]` eckig, `(Ausgabemarker)` rund |
| Freitext als Ausgabe | Nicht weiterverarbeitbar | Tabellen, nummerierte Abschnitte, Kästchen |
| "Fasse alles zusammen" | Erzeugt Vollständigkeit statt Relevanz | Obergrenze setzen, Auswahlkriterium nennen |

---

## Gerüst für einen neuen Prompt

Zum Kopieren als Startpunkt einer neuen Datei in `prompts/<kategorie>/`:

```text
Du bist [ROLLE] in einer deutschen Steuerkanzlei.
[ARBEITSWEISE IN EINEM SATZ]

AUFGABE
[WAS GENAU ENTSTEHEN SOLL]

KONTEXT
- [FELD]: [PLATZHALTER]
- [FELD]: [PLATZHALTER]

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab und benenne fehlende Angaben.
2. [FACHLICHE ANFORDERUNG]
3. [OBERGRENZE / AUSWAHLKRITERIUM]
4. Formuliere jede Ursachenaussage als Vermutung, solange sie nicht belegt ist.
5. Kennzeichne alle Werte, die jährlich wechseln, als "für [JAHR] verifizieren".
6. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen und keine Fundstellen;
   bist du unsicher, schreibe "Fundstelle offen – bitte recherchieren".

AUSGABEFORMAT
[ABSCHNITTE], darunter separat "Interne Notiz" und "Was ich nicht sicher weiß".
```

Danach den Dateikopf nach der Konvention in `CLAUDE.md` ergänzen und die
Abschnitte Anwendung, Qualitätssicherung und Varianten schreiben. In die
Qualitätssicherung gehört zwingend Baustein 13 (Freigabe und Vier-Augen), in den
Dateikopf Baustein 5 (Datensparsamkeit) mit Verweis auf `DATENSCHUTZ.md`. Berührt
der Prompt Fristen, kommt Baustein 14 hinzu; berührt er Berichtigungs- oder
Strafsachverhalte, Baustein 15.
