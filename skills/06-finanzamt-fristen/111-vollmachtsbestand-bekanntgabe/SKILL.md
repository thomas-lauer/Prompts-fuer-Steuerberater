---
name: vollmachtsbestand-bekanntgabe
description: Arbeitet eine Mandatstabelle zum Vollmachtsbestand Zeile für Zeile
  durch, stuft je Mandat das Risiko für die elektronische Bekanntgabe ein und
  erzeugt daraus eine nach Dringlichkeit sortierte Arbeitsliste, einen
  Textbaustein für die Mandanteninformation und einen internen Ablaufvorschlag
  für die Abrufkontrolle. Sie folgt dem Prüfschema aus Prompt 111, berechnet
  keine Frist und bricht ab, wenn die Bestätigung zur Zone Rot fehlt. Use when a
  Steuerkanzlei wants to clean up its Vollmachtsbestand before Bescheide are
  bereitgestellt zum Datenabruf, or asks which Mandate are at risk under § 122a AO.
---

# 111 – Vollmachtsbestand vor der elektronischen Bekanntgabe bereinigen

## Zweck

Die Skill wertet den Mandantenbestand aus: Sie prüft **jede Zeile einzeln** nach
dem Schema der Prompt-Datei, stuft das Risiko je Mandat ein und verdichtet die
Einstufungen zu einer sortierten Arbeitsliste. Der Prompt liefert das Prüfschema
für einen Durchlauf; bei einigen hundert Mandaten ist die eigentliche Arbeit die
gleichförmige Anwendung dieses Schemas auf jede Zeile und das anschließende
Sortieren – genau die nimmt die Skill ab. Sie hält fest, worauf sich jede
Einstufung stützt, damit eine zweite Person sie gegen die Vollmachtsdatenbank
nachprüfen kann.

## Wann einsetzen – und wann nicht

**Einsetzen**, wenn eine Bestandsliste mit einer Zeile je Mandat vorliegt und
geklärt werden soll, bei welchen Mandaten ein zum Abruf bereitgestellter Bescheid
ins Leere laufen kann: fehlende oder beschränkte Vollmacht, fehlende
Bekanntgabevollmacht, fehlende Hinterlegung in der Vollmachtsdatenbank,
Doppelvollmacht nach Beraterwechsel oder Selbstabruf durch den Mandanten.

**Nicht einsetzen** für die kanzleiweite Umstellung auf die elektronische
Bekanntgabe und die dauerhafte Fristenkontrolle: Prompt 102 arbeitet mit einem
Mengengerüst je Fallgruppe, nicht mit einer Zeile je Mandat, und fragt die
heutige Praxis der Fristerfassung, die eingesetzten Programme und die
Auffälligkeiten nach der Umstellung der Vollmachtsdatenbank ab. Das Fristen- und
Wiedervorlagekonzept der Kanzlei mit Rollen, Programmen und bisheriger
Erfassungspraxis steht in Prompt 35.

Den internen Ablaufvorschlag zur Abrufkontrolle erzeugt diese Skill gleichwohl –
er ist Bestandteil des Ausgabeformats der Prompt-Datei und beschreibt die
Abrufkontrolle für den soeben bereinigten Bestand, nicht das kanzleiweite
Verfahren. Wird daraus eine Dauerorganisation, ist ab dort Prompt 102 zuständig
und für die Fristerfassung Prompt 35.

Die Fristenlage eines einzelnen Bescheids trägt keines der drei Ziele: Diese
Skill rechnet nicht, sie ordnet den Bestand; Prompt 102 kennt keine Einzelmandate
und Prompt 35 kein Bescheiddatum. Ist ein Mandat bekannt, bei dem eine
Bereitstellung dokumentiert und kein Abruf vermerkt ist, gehört es sofort dem
Berufsträger vorgelegt.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Vor der ersten Tabellenzeile fordert die Skill die Bestätigung aus der
Prompt-Datei an: dass die Übersicht **keine Steuernummern, keine
Steuer-Identifikationsnummern und keine Aktenzeichen des Finanzamts** enthält –
auch nicht maskiert, auch nicht in Ausschnitten.

Steht dort etwas anderes als `bestätigt` – auch dann, wenn das Feld unausgefüllt
geblieben ist oder die Tabelle kommentarlos eingefügt wurde –, wird **keine
einzige Zeile** bearbeitet. Die Skill gibt nur die Rückmeldung nach der
Sperrregel der Prompt-Datei aus und sagt konkret, was stattdessen einzufügen ist:
eine Fassung ausschließlich mit Mandatskürzeln (`M-01`), Rechtsform, Steuerarten
und den Ja-Nein-Angaben zur Vollmacht. Die Zuordnungstabelle bleibt in der
Kanzlei.

Ebenfalls Zone Rot in diesem Fall (`DATENSCHUTZ.md`): Vollmachts- und
Zugangsdaten, Freischaltcodes und Auszüge aus der Vollmachtsdatenbank.
Mitarbeitende erscheinen nur als Rollen (`Sekretariat`, `Berufsträger A`).
Taucht solches Material erst während der Bearbeitung auf – etwa im Feld zu den
bekannten Auffälligkeiten –, hält die Skill an, verarbeitet die Angabe nicht und
benennt, welche Fassung sie braucht. Die Ausgabe enthält nie eine Nummer oder ein
Aktenzeichen, auch nicht in Beispielzeilen.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche
Einbindung des Anbieters nach § 62a StBerG (sorgfältige Auswahl, Vertrag in
Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf
das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Ablauf

1. **Datensparsamkeit abschließen.** Ohne die Bestätigung zur Zone Rot wird nichts
   aufgenommen – auch nicht der Kanzleirahmen, dessen Feld zu den bekannten
   Auffälligkeiten erfahrungsgemäß Zone-Rot-Material anzieht.
2. **Kanzleirahmen aufnehmen.** Zahl der Mandate insgesamt, heutige Praxis des
   Bescheidabrufs, Zuständigkeit und Vertretung als Rollen, Schließ- und
   Urlaubszeiten, bekannte Auffälligkeiten. Was fehlt, wird nachgefordert und
   nicht unterstellt; ohne benannte Zuständigkeit und Vertretung entsteht kein
   Ablaufvorschlag, sondern eine offene Frage.
3. **Tabelle formal prüfen.** Die zehn Spalten der Prompt-Datei müssen vorhanden
   sein; eine fehlende wird nachgefordert und nicht ergänzt. Die Zeilenzahl wird
   gegen die genannte Zahl der Mandate gehalten, die Differenz gehört in die
   fehlenden Angaben. Bei großen Beständen in Gruppen arbeiten: zuerst die
   Mandate, bei denen die Kanzlei oder ein anderer Bevollmächtigter
   elektronisch übermittelt, danach die übrigen.
4. **Zeitfenster ausdrücklich benennen.** Die Ausgabe sagt in eigenen Worten, dass
   die Kann-Bekanntgabe bereits gilt, die Soll-Bekanntgabe erst später anwendbar
   wird und dass dazwischen das Zeitfenster für die Bereinigung des
   Vollmachtsbestands liegt. Die gesetzlichen Anwendungszeitpunkte werden dabei als
   Gesetzeswortlaut der Prompt-Datei wiedergegeben, nicht umgerechnet und nicht zu
   einer Frist verarbeitet.
5. **Zeilenweise prüfen.** Jede Zeile durchläuft die acht Prüfschritte der
   Prompt-Datei in deren Reihenfolge, von der Bekanntgabelage nach Rechtsform bis
   zur Risikohöhe mit Begründung; Schema und Fundstellen stehen dort und werden
   hier nicht wiederholt. Keine Zeile wird zusammengefasst oder übersprungen;
   nach der letzten meldet die Skill, wie viele Zeilen sie bearbeitet hat.
6. **„unklar" und „unbekannt" als eigenen Zweig führen.** Diese Werte sind keine
   fehlenden Angaben, die man auffüllen dürfte, und keine stillen Neins. Für die
   Risikohöhe wirkt „unklar" bei der Bekanntgabevollmacht so vorsichtig wie
   „nein" – aber die Skill schreibt den Wert nie in „nein" um, nennt den
   Unterschied in der Begründung und leitet daraus eine **andere** Aufgabe ab:
   bei „nein" die Beschaffung der fehlenden Vollmacht, bei „unklar" zuerst die
   Klärung des Bestands in der Kanzlei. In der Spalte zum Übermittler bleibt
   „unbekannt" ohne Zuordnung und wird als fehlende Angabe ausgewiesen. Jede
   Einstufung, die darauf beruht, sagt das ausdrücklich; eine Spalte, die
   überwiegend so ausgefüllt ist, wird als solche gemeldet.
7. **Arbeitsliste bilden.** Die Einzeleinstufungen werden nach Dringlichkeit
   sortiert, auf höchstens fünfzehn Positionen verdichtet, gleichartige Fälle
   zusammengefasst statt einzeln aufgezählt. Das Sortierkriterium wird
   ausdrücklich genannt; die bekannten Auffälligkeiten aus Schritt 2 werden
   eingeordnet, mit Angabe, an welcher Stelle sie wirken.
8. **Mandanteninformation und internen Ablaufvorschlag erzeugen, dann ablegen.**
   Beides nach den Vorgaben der Prompt-Datei und sauber getrennt: Der
   Textbaustein ist für den Mandanten – höchstens 350 Wörter in Sie-Form, jeder
   Fachbegriff in Klammern erklärt, ohne interne Bewertungen –, Ablaufvorschlag und
   interne Notiz sind es nicht. Keine Tage, keine Datumsangaben, kein Wort von einer
   Einwilligung. Jede Aussage über die Praxis der Finanzverwaltung wird ausdrücklich
   als Erfahrungswert gekennzeichnet. Zum Textbaustein gehört die Angabe, für welche
   Gruppe er bestimmt ist: Er geht nicht als Rundschreiben an den gesamten Bestand,
   sondern nur an die Mandate, für die er zutrifft – sonst beantragen Mandate die
   postalische Bekanntgabe, bei denen sie nur Zeit kostet. Fehlende Angaben, offene
   Fragen und die Fundstellentabelle kommen mit in die Ergebnisdatei.

## Ergebnis

Eine Markdown-Datei, Vorschlag: `vollmachtsbestand-bekanntgabe-<JJJJ-MM-TT>.md`.

Inhalt in der Reihenfolge des Ausgabeformats der Prompt-Datei: Einschätzung der
Eindeutigkeit, Risikoliste je Mandat (Kürzel, Risikohöhe, Risikogrund, worauf
sich die Einstufung stützt, offene Frage), Arbeitsliste nach Dringlichkeit mit
den leeren Spalten `Nachweis der Erledigung` und `erledigt`, Textbaustein für die
Mandanteninformation, interner Ablaufvorschlag, fehlende Angaben, Tabelle der zu
verifizierenden Rechtsgrundlagen mit leerer Spalte `geprüft von`, interne Notiz.
Nur der Textbaustein wird für den Versand entnommen – und auch er nur an die
Gruppe, für die er gilt; alles Übrige bleibt intern.

## Qualitätssicherung

Das Ergebnis ist ein Entwurf und kennt nur, was in der Tabelle stand.

- **Vier-Augen-Prinzip:** Eine Person arbeitet die Liste ab, eine zweite prüft
  die Einstufungen gegen den Bestand der Vollmachtsdatenbank und zeichnet ab –
  vorrangig bei Mandaten mit Vorberater, weil dort zwei Vollmachten nebeneinander
  bestehen können.
- **Freigabe durch einen Berufsträger** für die Mandanteninformation und für
  jede Änderung am Vollmachtsbestand (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Die Skill berechnet keine Frist:** kein Bereitstellungstag, kein
  Bekanntgabetag, kein Fristende. Die Bekanntgabefiktion wird als Regel benannt
  und nicht angewendet – Fristen berechnet, erfasst und kontrolliert ein Mensch
  (Prompt 35).
- **Rechtsstand:** Die Skill führt keine eigene Fundstellensammlung; geprüft wird
  an den in der Prompt-Datei genannten Fundstellen. In der Ausgabe steht
  gleichwohl zu jeder rechtlichen Aussage die Rechtsgrundlage mit Absatz und Satz
  und dem Zusatz `für [JAHR] verifizieren`; ist eine Fundstelle unsicher, steht
  dort „Fundstelle offen – bitte recherchieren".
- Prüfen, dass nirgends von einer Einwilligung in die elektronische Bekanntgabe
  die Rede ist, dass die Zweistufigkeit erhalten geblieben ist – Kann- und
  spätere Soll-Bekanntgabe nicht zusammenziehen, sonst ist das Zeitfenster für
  die Bereinigung falsch dargestellt – und dass in der Ausgabe keine Nummer und
  kein Aktenzeichen steht.
- Ein Antrag auf postalische Bekanntgabe wird nur nach Rücksprache mit dem
  Mandanten gestellt und in der Handakte dokumentiert; er wirkt nur für die
  Zukunft und erst mit Zugang – eine bereits erfolgte Bereitstellung erreicht er
  nicht mehr.

## Grundlage

Fachliches Prüfschema, Rechtsrahmen und Ausgabeformat stehen in der Prompt-Datei
[prompts/06-finanzamt-fristen/111-vollmachtsbestand-bekanntgabe.md](../../../prompts/06-finanzamt-fristen/111-vollmachtsbestand-bekanntgabe.md);
die Skill folgt ihr und schreibt sie nicht ab.
