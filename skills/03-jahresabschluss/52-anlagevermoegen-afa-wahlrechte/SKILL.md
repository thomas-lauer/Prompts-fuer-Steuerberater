---
name: anlagevermoegen-afa-wahlrechte
description: Prüft die Zugänge eines Wirtschaftsjahres einzeln durch das Entscheidungsschema zum
  Anlagevermögen, stellt je Zugang die Wahlrechte gegenüber und stimmt die Anlagenbuchführung
  gegen die Konten des Rechnungswesens ab. Sie rechnet keine AfA und übt kein Wahlrecht aus.
  Use when an Anlagenliste has to be plausibilised before closing the books, when Methodenwahl
  und Wahlrechte je Zugang zu dokumentieren sind, or when Reparaturkonten auf nachträgliche
  Anschaffungskosten durchzusehen sind.
---

# 52 – Anlagevermögen und AfA-Wahlrechte plausibilisieren

## Zweck

Die Skill nimmt Anlagenliste, Kontensalden und Reparaturaufwand einmal entgegen und führt danach
jeden Zugang des Jahres einzeln durch das achtstufige Entscheidungsschema der Prompt-Datei.
Darin liegt der Mengenvorteil: Der Textblock allein müsste je Zugang neu ausgefüllt werden, samt
Mandantenrahmen; die Skill hält den Rahmen fest, arbeitet die Zugangsliste zeilenweise ab und
sammelt die Rückfragen gebündelt. Über den Bestand laufen zusätzlich Ausreißersuche und
Abstimmung gegen die Anlagen- und Abschreibungskonten. Die Skill **rechnet keine AfA** und übt
kein Wahlrecht aus – sie legt die Entscheidungsgrundlage vor.

## Wann einsetzen – und wann nicht

Einsetzen, wenn die Zugänge eines Wirtschaftsjahres vor dem Abschluss plausibilisiert werden
sollen: Methodenwahl je Zugang, Bindungswirkung der Wahlrechte, Ausreißer im Bestand,
Differenzen zwischen Anlagenbuchführung und Rechnungswesen. Nicht einsetzen für:

- **Anschaffungsnahe Herstellungskosten bei Gebäuden:** Prompt 89. Er verlangt Angaben, die eine
  Anlagenliste nicht enthält – Kaufvertrag, Kaufpreisaufteilung, Zustand und Ausstattung des
  Gebäudes vor und nach der Maßnahme, sämtliche Rechnungen als Einzelpositionen und den Stand der
  Bescheide. Die maßgebliche Liste steht dort unter "Was du bereitstellen musst" und wird von dort
  angefordert, nicht von hier – sie ist länger und in den Einzelheiten strenger, als sich hier
  wiedergeben lässt. Fehlen die Angaben, werden sie angefordert; der Verweis ersetzt sie nicht.
  Auch Prompt 89 bildet keine Summen und rechnet keine Prozentgrenze.
- **Überwachung von Investitionsabzugsbeträgen über mehrere Jahre:** Prompt 53. Er verlangt die
  Übersicht der Abzugsbeträge mit Jahr der Bildung, Betrag, geplantem Wirtschaftsgut,
  verwendetem Teilbetrag und Rest.
- **Im Nachlauf gebuchte Zugänge und die Periodenabgrenzung:** Prompt 51 mit der Buchungsliste
  des Nachlaufzeitraums.

Ebenso wenig einsetzen, um AfA-Beträge, Restbuchwerte oder Bemessungsgrundlagen zu ermitteln
oder ein Wahlrecht zu entscheiden.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Vor dem ersten Zugang ist zu bestätigen, dass **Steuer-Identifikationsnummer, Steuernummer und
Aktenzeichen des Finanzamts entfernt** sind – nicht maskiert, sondern entfernt, auch in
Ausschnitten und in Kopfzeilen exportierter Auswertungen. Sie sind Zone Rot nach
`DATENSCHUTZ.md`.

Gearbeitet wird ausschließlich mit Mandatskürzeln und Platzhaltern: `Mandant A`, `Lieferant 1`,
`Fahrzeug 1`, `Objekt 1`. Amtliche Kennzeichen, Seriennummern, Fahrgestellnummern und
Lieferantennamen werden ersetzt, nicht gekürzt; für die Prüfung genügen Wirtschaftsgutart,
Datum, Betrag, Nutzungsdauer und Methode. Betreffen Positionen ein Gebäude, bleibt die Anschrift
des Objekts draußen, die Lage wird nur als Kategorie angegeben.

Taucht Zone-Rot-Material auf, wird abgebrochen und konkret zurückgemeldet, was stattdessen
einzureichen ist – etwa: Spalte "Steuernummer" aus dem Export löschen; Bezeichnungen mit
Kennzeichen und Fahrgestellnummer durch `Fahrzeug 1`, `Fahrzeug 2` ersetzen; Lieferantennamen auf
`Lieferant 1` vereinheitlichen. Danach die Liste erneut einreichen.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters
nach § 62a StBerG (sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung)
müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Ablauf

1. **Mandantenrahmen einmal aufnehmen:** Rechtsform, Gewinnermittlung, Wirtschaftsjahr,
   Gewinnsituation und erwartete Entwicklung, geplante Investitionen, vorhandene Abzugsbeträge
   nach § 7g EStG, Besonderheiten. Die **Gewinnermittlungsart ist Pflichtangabe** – sie
   entscheidet, welche außerplanmäßige Wertkorrektur überhaupt zulässig ist. Fehlt sie, wird
   nachgefragt und nicht unterstellt.
2. **Unterlagen entgegennehmen und auf denselben Stichtag prüfen:** Anlagenliste, Salden der
   Anlagen- und Abschreibungskonten, Reparatur- und Instandhaltungsaufwand. Weichen die Stichtage
   ab oder fehlt einer, wird nachgefragt, bevor abgestimmt wird – sonst entstehen
   Scheindifferenzen.
3. **Zugänge des Jahres vom Bestand trennen** und aus den Zugängen eine Arbeitsliste bilden.
   Jeder Zugang läuft einzeln und in der Reihenfolge der Prompt-Datei durch alle acht Schritte des
   Abschnitts "ENTSCHEIDUNGSSCHEMA JE ZUGANG"; jedes Schrittergebnis wird festgehalten, auch wenn
   es "nicht entscheidbar" lautet. Jede Ursachenaussage wird als Vermutung gekennzeichnet, gleich
   in welchem Teil des Ergebnisses sie steht – Wahlrechtsgegenüberstellung, Empfehlungsraster,
   Ausreißerliste oder Abstimmung.
4. **Die Weiche nachträgliche Anschaffungs- oder Herstellungskosten gegen Erhaltungsaufwand**
   (Schritt 7 des Entscheidungsschemas) wird für jede auffällige Position der Reparatur- und
   Instandhaltungskonten gestellt und zusätzlich für jeden Zugang, der an ein bereits vorhandenes
   Wirtschaftsgut anknüpft – Umbau, Erweiterung, Ersatz von Bestandteilen, Maßnahme am Gebäude.
   Erstanschaffungen ohne Bezug zu vorhandenem Anlagevermögen durchlaufen die Weiche nicht; das
   wird je Zugang mit "Erstzugang – Weiche nicht einschlägig" protokolliert und hält den Zugang
   nicht auf. Wo die Weiche greift, entscheidet sie über die gesamte Folgebehandlung:
   Bemessungsgrundlage, Nutzungsdauer, Methodenwahl und Sofortabzug hängen daran. Ergebnis je
   Position ist "nachträgliche Anschaffungs- oder Herstellungskosten", "Erhaltungsaufwand" oder
   "nicht entscheidbar".
5. **Greift die Weiche und fehlen Angaben zum Zustand, wird nachgefragt, nicht geschätzt.** Ohne
   Angabe zum Zustand des Wirtschaftsguts vor und nach der Maßnahme, zu deren Umfang und dazu, ob
   das Wirtschaftsgut vorher funktionsfähig und betriebsbereit war, wird nicht zugeordnet; aus
   Kontobezeichnung, Betrag oder Lieferant wird nichts geschlossen. Die übrigen Schritte des
   Entscheidungsschemas laufen für diese Position weiter. Betrifft die Maßnahme ein Gebäude in
   zeitlicher Nähe zum Erwerb, geht die Position mit der in Prompt 89 verlangten Unterlagenliste
   dorthin.
6. **Wahlrechte je Zugang gegenüberstellen** nach den Spalten des Ausgabeformats der Prompt-Datei.
   Zu jedem Wahlrecht wird ausdrücklich gesagt, ob es nach Ausübung gebunden ist, ob es mehrjährig
   wirkt und ob es sich später noch ändern lässt – ist das unklar, wird es als unklar ausgewiesen.
   Prozentsätze, Höchstbeträge, Betragsgrenzen, Nutzungsdauern und Anwendungszeiträume werden
   nicht als feststehend genannt, sondern als nachzuschlagende Größe benannt, jeweils mit dem
   wörtlichen Zusatz "für [JAHR] verifizieren". Jede rechtliche Aussage – auch in Ausreißerliste,
   Abstimmung und interner Notiz – trägt ihre Rechtsgrundlage mit Absatz und Satz und denselben
   Zusatz; ist sie unsicher, steht dort "Fundstelle offen – bitte recherchieren", ist sie nicht
   angebbar, "ohne Fundstelle – vor Verwendung belegen". Zu jedem Wahlrecht steht: Ausübung
   entscheidet ein Berufsträger.
7. **Bestand durchsehen und abstimmen:** höchstens zehn Ausreißer, sortiert nach steuerlicher
   Auswirkung, jede Beobachtung mit Zahl, jede Vermutung als solche gekennzeichnet, je mit
   Prüfschritt. Danach die Anlagenbuchführung gegen die Kontensalden stellen: Die Zugangs-,
   Abgangs- und AfA-Spalten der Anlagenliste werden dafür summiert und den Kontensalden
   gegenübergestellt, jede Differenz wird mit Betrag benannt, der Rechenweg bleibt sichtbar.
   Darüber hinaus wird nichts gerechnet: AfA-Beträge, Restbuchwerte und Bemessungsgrundlagen
   werden nicht ermittelt und nicht nachgerechnet.
8. **Offene Punkte gebündelt zurückfragen:** eine Rückfrage über alle markierten Positionen, je
   Position mit der genau fehlenden Angabe. Bleibt sie unbeantwortet, gilt die Position als nicht
   entscheidbar und erscheint mit ihrer Lücke im Ergebnis.
9. **Ergebnisdatei schreiben** in der Gliederung des Ausgabeformats der Prompt-Datei.

## Ergebnis

Eine Datei `<Mandatskürzel>-anlagevermoegen-<JJJJ>.md` mit dem Wirtschaftsjahr im Namen. Inhalt
und Reihenfolge richten sich nach dem Ausgabeformat der Prompt-Datei: Eindeutigkeit und Datenlage;
Wahlrechtsgegenüberstellung je Zugang mit den dort genannten Spalten; Empfehlungsraster als
Abwägung ohne Entscheidung; Ausreißerliste; Abstimmung der Anlagenbuchführung gegen das
Rechnungswesen mit Differenzen; interne Notiz; "Was ich nicht sicher weiß". Die
Zuordnungsentscheidung aus Schritt 4 steht je Zugang sichtbar im Protokoll – auch als "Erstzugang
– Weiche nicht einschlägig" –, einschließlich der mangels Zustandsangaben offen gebliebenen
Positionen.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Eine zweite fachkundige Person prüft je Zugang
  Anschaffungszeitpunkt, Zulässigkeit der Methode zu genau diesem Zeitpunkt, Nutzungsdauer und
  Bindungswirkung; die Freigabe erteilt ein Berufsträger und dokumentiert sie (Freigabestufe 3 in
  `DATENSCHUTZ.md`).
- **Die Skill rechnet keine AfA.** Weder AfA-Beträge noch Restbuchwerte, Bemessungsgrundlagen
  oder Sonderabschreibungen werden ermittelt; gerechnet wird außerhalb, und die Ergebnisse sind
  nachzurechnen. Kein Prozentsatz, Höchstbetrag, Grenzwert und kein Anwendungszeitraum wird aus
  der Ausgabe übernommen – diese Werte haben sich mehrfach geändert und sind an den Quellen zu
  prüfen, die der Abschnitt `## Qualitätssicherung` der Prompt-Datei nennt.
- **Die Summen der Abstimmung sind gegenzurechnen.** Die Verdichtung der Zugangs-, Abgangs- und
  AfA-Spalten und jede genannte Differenz werden in der Tabellenkalkulation nachgerechnet;
  Summenbildung über viele Zeilen ist eine bekannte Fehlerquelle.
- **Die Zuordnung nachträgliche Anschaffungskosten gegen Erhaltungsaufwand ist vor der Freigabe
  einzeln zu prüfen** – sie wirkt über die gesamte Abschreibungsdauer und wird in der Prüfung
  zuerst angegriffen. Als "nicht entscheidbar" geführte Positionen sind vor dem Abschluss zu
  klären, nicht zu buchen.
- **Wahlrechte sind teils nicht rückholbar und wirken mehrjährig.** Die Ausübung entscheidet ein
  Berufsträger; mehrjährig wirkende Entscheidungen gehören in die Dauerakte, auch die bewusst
  nicht gewählte Alternative.

## Grundlage

Entscheidungsschema, Sachverhaltsbogen und Ausgabeformat stehen in der Prompt-Datei; die Skill
folgt ihr und schreibt sie nicht ab:
[prompts/03-jahresabschluss/52-anlagevermoegen-afa-wahlrechte.md](../../../prompts/03-jahresabschluss/52-anlagevermoegen-afa-wahlrechte.md).
