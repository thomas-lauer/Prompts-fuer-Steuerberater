---
name: wirtschafts-identifikationsnummer
description: Geht den Mandantenbestand zeilenweise durch, ordnet jedes Mandat
  einer Vergabestufe der Wirtschafts-Identifikationsnummer-Verordnung zu,
  begründet die Einstufung aus dem jeweiligen Feld und leitet daraus die
  anzupassenden Stammdatenfelder, die berührten Verfahren und eine
  Mandanteninformation ab. Sie arbeitet durchgehend mit
  „vorhanden ja / nein / unbekannt" und fragt keine Nummer ab. Use when a
  Steuerkanzlei wants to know which Mandate are affected by the
  Wirtschafts-Identifikationsnummer, which Stammdatenfelder are missing, or how to
  inform Mandanten about it.
---

# 113 – Wirtschafts-Identifikationsnummer im Mandantenbestand

## Zweck

Die Skill wertet den Mandantenbestand aus: Sie prüft **jede Zeile einzeln**,
ordnet das Mandat einer Vergabestufe nach § 1 WIdV zu, benennt das Feld, aus dem
sich die Zuordnung ergibt, gleicht die Stufe gegen den mitgeteilten Stand ab und
leitet daraus die Feldliste für die Stammdaten ab. Der Prompt liefert Rechtsrahmen
und Prüfreihenfolge für einen Durchlauf; bei einigen hundert Mandaten ist die
eigentliche Arbeit die gleichförmige Zuordnung Zeile für Zeile und ihre
Verdichtung zu einer Arbeitsliste ohne überflüssige Rückfragen.

## Wann einsetzen – und wann nicht

**Einsetzen** für die bestandsweite Betroffenheitsprüfung: Welche Mandate sind
wirtschaftlich tätig, in welcher Vergabestufe stehen sie, bei welchen ist die
Nummer mitgeteilt, welche haben voraussichtlich mehrere Unterscheidungsmerkmale,
welche Stammdatenfelder und Verfahren sind zu ergänzen.

**Nicht einsetzen** für die Namenskonvention der Personenkonten: Wie Debitoren und
Kreditoren heißen, welche Nummernkreise und welcher Kontenrahmen gelten, regelt
Prompt 25 – dort endet diese Skill mit einem Übergabepunkt. Umgekehrt gilt: Für
die Benennung von Mandanten-Stammdatenfeldern zu steuerlichen Ordnungsmerkmalen
hat Prompt 25 kein Eingabefeld und trägt den Fall nicht; diese Feldnamen schlägt
die Skill selbst vor und übergibt sie zur Angleichung an die vorhandene
Konvention. Ebenso wenig einsetzen für die Erstanmeldung eines einzelnen Mandats: Der
Fragebogen zur steuerlichen Erfassung mit den Angaben zu Tätigkeit, Beginn,
Rechtsform, geschätzten Umsätzen und Vollmachten ist Prompt 68. Diese Skill
behandelt den Bestand, nicht den Zugang.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

**Die Wirtschafts-Identifikationsnummer ist selbst ein steuerliches
Ordnungsmerkmal und wird wie die Steuernummer behandelt.** Sie kommt nicht in das
Werkzeug – auch nicht teilmaskiert, auch nicht in Ausschnitten, auch nicht als
Beispiel. Die Skill arbeitet ausnahmslos mit `vorhanden ja / nein / unbekannt`
und fragt die Nummer an keiner Stelle ab. Dasselbe gilt für Steuernummer,
Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts (Zone Rot in
`DATENSCHUTZ.md`) sowie – aus Datensparsamkeit – für USt-IdNr., Register- und
Handelsregisternummern. Mandate erscheinen nur als fortlaufende Kürzel (`M-01`),
Mitarbeitende nur als Rollen; keine Firmennamen, keine Anschriften, keine Namen
von Beteiligten.

**Taucht eine Nummer während der Bearbeitung dennoch auf, wird abgebrochen, nicht
überlesen und nicht bereinigt.** Rückmeldung: in welcher Zeile und welcher Spalte
die Angabe steht, dass der begonnene Durchlauf verworfen ist und dass der Bestand
vor dem erneuten Einsatz ohne diese Spalte einzufügen ist. Ein Weiterarbeiten
„ohne die Nummer" gibt es nicht – die Angabe ist dann bereits im Werkzeug.

Vor der ersten Zeile fordert die Skill die Bestätigung aus der Prompt-Datei an,
dass alle Nummernspalten vor dem Einfügen gelöscht wurden. Steht dort etwas
anderes als `bestätigt` – auch dann, wenn das Feld unausgefüllt geblieben ist –,
wird keine Zeile bearbeitet; die Skill gibt nur die Rückmeldung nach der
Abbruchregel der Prompt-Datei aus und sagt, welche Fassung sie stattdessen
braucht. Ein unvollständig bekannter Bestand ist dagegen **kein** Abbruchgrund:
`unbekannt` in einer Zeile, auch in mehreren oder allen Feldern einer Zeile, ist
der Anlass dieser Auswertung.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche
Einbindung des Anbieters nach § 62a StBerG (sorgfältige Auswahl, Vertrag in
Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf
das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Ablauf

1. **Kanzleirahmen aufnehmen.** Heute gepflegte Stammdatenfelder, Programme,
   Rolle für die Stammdatenpflege, Ort, an dem Mitteilungen des Bundeszentralamts
   für Steuern auflaufen, und ob dieser Ort überwacht ist. Was fehlt, wird
   nachgefordert und nicht unterstellt; ist für die Übertragung in die Stammdaten
   keine Rolle benannt, wird das als Lücke ausgewiesen.
2. **Tabelle formal prüfen.** Die Spalten der Prompt-Datei müssen vollständig
   vorhanden sein – einschließlich der Anzahl der Betriebe und Betriebstätten als
   eigener Spalte neben der Ja-Nein-Angabe; eine fehlende wird nachgefordert und
   nicht ergänzt. Enthält die Tabelle noch eine Nummernspalte, wird sie
   zurückgewiesen. Bei großen Beständen mit einem Ausschnitt beginnen – etwa den
   Mandaten mit Betriebstätten.
3. **Vollständigkeit der Angaben einschätzen:** ausreichend / in Teilen lückenhaft /
   für eine Bestandsaussage noch nicht tragfähig, mit Aufzählung der fehlenden
   Angaben. Die Einstufung steht am Anfang der Ergebnisdatei. Ein Bestand, der
   überwiegend `unbekannt` trägt, führt zu „für eine Bestandsaussage noch nicht
   tragfähig" – **und trotzdem zur vollständigen Auswertung**, denn er ist der
   Arbeitsvorrat, nicht der Abbruchgrund.
4. **Zeilenweise zuordnen.** Jede Zeile durchläuft die Prüfschritte der
   Prompt-Datei in deren Reihenfolge, von der wirtschaftlichen Tätigkeit über die
   Stufe nach § 1 WIdV und die voraussichtliche Zahl der Unterscheidungsmerkmale
   aus den Feldern „Mehrere Betriebe oder Betriebstätten" und „Anzahl" bis zu den
   berührten Verfahren; Rechtsrahmen und
   Fundstellen stehen dort und werden hier nicht wiederholt. **Keine Zuordnung
   ohne Feldbezug:** Zu jeder Einstufung wird das Feld genannt, aus dem sie
   folgt. Widersprechen sich die Felder oder steht überall `unbekannt`, läuft das
   Mandat als „Zuordnung offen" weiter und wird nicht weggelassen; steht ein für
   die Stufe entscheidendes Feld auf `unbekannt`, lautet das Ergebnis „Stufe
   nicht bestimmbar" mit der fehlenden Angabe in der Arbeitsliste. Es wird nicht
   geraten. Nach der letzten Zeile meldet die Skill, wie viele sie bearbeitet
   hat.
5. **Die Gruppe mit vorhandener USt-IdNr. getrennt führen.** Bei Mandaten der
   Stufe § 1 Abs. 2 WIdV ist die Wirtschafts-Identifikationsnummer mit der schon
   vorhandenen Umsatzsteuer-Identifikationsnummer identisch. `unbekannt` heißt in
   diesen Zeilen deshalb **nicht** Rückfrage beim Mandanten, sondern Abgleich in
   der eigenen Akte: Sie gehören in die Gruppe „im eigenen Bestand zu klären",
   nicht in die Gruppe „nach der Stufe zu erwarten, aber nicht mitgeteilt". Die
   Skill führt beide Gruppen sichtbar getrennt und mit unterschiedlichen nächsten
   Schritten – sonst entsteht eine Arbeitsliste voller überflüssiger Rückfragen.
   Die Gruppe „unbekannt" insgesamt ist der Regelfall und der eigentliche
   Arbeitsvorrat, kein Versäumnis des Mandanten.
6. **Stammdatenfelder ableiten.** Aus den Einzelzuordnungen entsteht die
   Feldliste: Merkmal der wirtschaftlichen Tätigkeit, Stufe, Status der
   Mitteilung, Zahl der Betriebe und Betriebstätten, Zuordnung der
   Unterscheidungsmerkmale, Quelle, Eingangsweg, zuständige Rolle. Je Feld wird
   festgehalten, ob es die Nummer selbst enthält; diese Felder werden nur im
   Kanzleisystem geführt und in kein weiteres Werkzeug übernommen. Für Benennung
   und Schreibweise der Felder liefert Prompt 25 die Systematik – Nummernkreise,
   Kontenrahmen, Schreibweise –, ist aber auf **Personenkonten** zugeschnitten und
   kennt keine Felder für steuerliche Ordnungsmerkmale eines Mandats. Diesen Teil
   trägt Prompt 25 also nicht: Die Skill schlägt die Feldnamen selbst vor und
   übergibt sie mit dem Vermerk „an die vorhandene Stammdatenkonvention
   anzugleichen" an die Kanzlei.
7. **Die Termindivergenz offen weitertragen.** Die Verordnung, das
   Bundeszentralamt für Steuern und das FAQ des Bundesfinanzministeriums nennen
   für die weiteren Unterscheidungsmerkmale unterschiedliche Zeitpunkte. Die
   Skill stellt die drei Angaben nebeneinander, kennzeichnet sie als offen,
   **entscheidet sich für keine** und fordert zur Prüfung am aktuellen Stand bei
   BZSt und BMF auf; alle drei Zeitangaben tragen den Zusatz
   `für [JAHR] verifizieren`.
   Der Punkt steht an erster Stelle der offenen Punkte und bleibt dort stehen,
   auch wenn ein Anwender nach dem „richtigen" Termin fragt.
8. **Mandanteninformation und offene Punkte erzeugen, dann ablegen.** Die
   Mandanteninformation bleibt ohne Rechtsgrundlagen im Fließtext, ohne Nummer
   und ohne die offenen Termine, und umfasst höchstens 200 Wörter. Sie wird
   ausdrücklich als versandgesperrt gekennzeichnet: Versand erst, wenn die
   Termindivergenz am aktuellen Stand bei BZSt und BMF geprüft und vom
   Berufsträger freigegeben ist – ein Anschreiben mit einem Datum, das sich als
   nicht belegt erweist, erzeugt mehr Rückfragen, als es beantwortet. Fristen
   werden nur dem Grunde nach benannt.

## Ergebnis

Eine Markdown-Datei, Vorschlag: `widnr-bestandsauswertung-<JJJJ-MM-TT>.md`.

Inhalt in der Reihenfolge des Ausgabeformats der Prompt-Datei: Einschätzung der
Vollständigkeit, Betroffenheitsliste je Mandat mit Stufe, Feldbezug und Gruppe,
Mandate mit voraussichtlich mehreren Unterscheidungsmerkmalen, Tabelle der
anzupassenden Stammdatenfelder und Formulare mit den Spalten `enthält die Nummer
selbst` und `erledigt`, offene Punkte mit der Termindivergenz an erster Stelle,
Mandanteninformation, Fristen nur dem Grunde nach, interne Notiz, Fundstellen mit
leerer Spalte `geprüft von`. Nur die Mandanteninformation wird für den Versand
entnommen; alles Übrige bleibt in der Kanzlei.

## Qualitätssicherung

Das Ergebnis ist ein Entwurf und kennt nur, was in der Tabelle stand.

- **Prüfen, ob im Ergebnis irgendwo eine Nummer steht.**
  Wirtschafts-Identifikationsnummer, Steuernummer, Steuer-Identifikationsnummer
  und USt-IdNr. gehören nicht in ein KI-Werkzeug, auch nicht als erfundenes
  Beispiel. Findet sich eine, wird die Bearbeitung abgebrochen, der Durchlauf
  verworfen und der Bestand vor dem erneuten Einsatz bereinigt – die Datei wird
  nicht um die Nummer bereinigt und weiterverwendet.
- **Vier-Augen-Prinzip:** Eine zweite Person prüft die Stufenzuordnung
  stichprobenweise gegen die Stammdaten, vor allem die Abgrenzung der Gruppe „im
  eigenen Bestand zu klären" von der Gruppe „zu erwarten, aber nicht mitgeteilt".
  **Freigabe durch einen Berufsträger** für die Mandanteninformation und für jede
  Aussage zu Terminen und Pflichten (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Prüfen, ob die Termindivergenz offen geblieben ist.** Ein Ergebnis, das sich
  für einen der drei Zeitpunkte entscheidet, ist an dieser Stelle falsch.
- Die Prompt-Datei stellt vier Verbote auf; jedes ist am Ergebnis nachzuprüfen:
  kein Bezug zur Sozialversicherung, zum Sozialgesetzbuch oder zur Betriebsnummer;
  kein Termin, der in keiner amtlichen Quelle belegt ist; keine Behauptung, das
  Digitale-Dienste-Gesetz verlange die W-IdNr. im Impressum – anzugeben ist die
  USt-IdNr. **oder** die W-IdNr., und nur, wenn eine solche besessen wird, ohne
  Beschaffungspflicht; und die neunstellige Ziffernfolge ist auf die Verordnung zu
  stützen, nicht auf die Abgabenordnung. Zusätzlich prüfen, ob für die W-IdNr. eine
  Norm zitiert wird, die ausschließlich natürliche Personen betrifft.
- **Formgrenzen einhalten:** höchstens 800 Wörter Fließtext (Tabellen und Listen
  zählen nicht mit); die Mandanteninformation höchstens 200 Wörter. Jede Aussage,
  die weder aus den Angaben noch aus einer benannten Fundstelle folgt, steht
  ausdrücklich als Vermutung.
- **Die Skill berechnet keine Frist** und nennt keine Fristdauer. Anzeige- und
  Mitteilungspflichten werden nur dem Grunde nach mit Rechtsgrundlage benannt:
  Fristen berechnet und erfasst ein Mensch.
- **Rechtsstand:** Die Skill führt keine eigene Fundstellensammlung; geprüft wird
  an den in der Prompt-Datei genannten Fundstellen. In der Ausgabe steht
  gleichwohl zu jeder rechtlichen Aussage die Rechtsgrundlage mit Absatz und Satz
  und dem Zusatz `für [JAHR] verifizieren`; ist eine Fundstelle unsicher, steht
  dort „Fundstelle offen – bitte recherchieren".

## Grundlage

Rechtsrahmen, Prüfreihenfolge und Ausgabeformat stehen in der Prompt-Datei
[prompts/10-kanzleiorganisation/113-wirtschafts-identifikationsnummer.md](../../../prompts/10-kanzleiorganisation/113-wirtschafts-identifikationsnummer.md);
die Skill folgt ihr und schreibt sie nicht ab.
