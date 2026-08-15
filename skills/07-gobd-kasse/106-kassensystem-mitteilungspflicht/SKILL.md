---
name: kassensystem-mitteilungspflicht
description: Arbeitet eine Systeminventur elektronischer Aufzeichnungssysteme Zeile
  für Zeile ab: erfasst § 146a Abs. 1 AO das System, welcher Vorgang löst eine
  Mitteilung aus, welche Angabe des Datensatzes nach § 146a Abs. 4 AO fehlt. Erzeugt
  daraus Bestandsübersicht je Betriebsstätte, Vorgangsliste, Lückenliste und ein
  Mandantenanschreiben. Use when a client has bought, rented, taken over or retired
  cash register systems and the notification to the tax office must be prepared or
  checked for completeness.
---

# 106 – Mitteilungspflicht für elektronische Kassensysteme

## Zweck

Die Skill führt die Inventur aus, die der Prompt beschreibt. Sie bedient kein
Portal, füllt keinen amtlichen Datensatz aus und übermittelt nichts: Die Mitteilung
setzt ein Mensch in Mein ELSTER oder über die ERiC-Schnittstelle der eingesetzten
Software ab; die Skill erzeugt ausschließlich die Vorarbeit dafür.

Sie nimmt die Systemaufstellung je Betriebsstätte entgegen und arbeitet sie
positionsweise ab: je Zeile die Systemabgrenzung, je erfasster Zeile die
Vorgangsermittlung, je Vorgang die acht Angaben des Datensatzes einzeln. Vor der
ersten Zeile lässt sie sich bestätigen, dass die Inventur beim Mandanten erhoben und
nicht aus der Anlagenbuchhaltung abgeleitet wurde; ist sie abgeleitet, steht das als
Vollständigkeitsvorbehalt im Ergebnis, weil geleaste und gemietete Geräte,
Zweitkassen, mobile Kassen im Außendienst und Filialsysteme dort erfahrungsgemäß
fehlen. Der Mengenvorteil liegt in der Zahl der
Zeilen – ein Filialbetrieb mit Zweitkassen, mobilen Kassen und geleasten Geräten
kommt schnell auf dreistellige Zeilenzahlen, und genau dort entstehen die
unvollständigen Mitteilungen. Die Skill hält je Zeile dasselbe Raster durch und
erzeugt daraus Bestandsübersicht, Vorgangsliste, Lückenliste und
Mandantenanschreiben in einem Lauf.

## Wann einsetzen – und wann nicht

Einsetzen, wenn der Meldebestand elektronischer Aufzeichnungssysteme aufgenommen,
auf Vollständigkeit geprüft oder nach einer Anschaffung, Miete, Übernahme oder
Außerbetriebnahme fortgeschrieben werden soll.

Nicht einsetzen:

- **Laufende Kassenführung nach GoBD** – Tagesabschluss, Kassenbericht, Stornos,
  Belegausgabe, Einzelaufzeichnung: Prompt 38. Er fragt Kassenart, Anzahl, System,
  Vorhandensein einer technischen Sicherheitseinrichtung und die Art der
  Kassenbuchführung ab und baut daraus eine Mandantencheckliste, nicht den
  Meldebestand.
- **Einführung eines neuen Kassensystems mit einem Dienstleister:** Prompt 107. Er
  verlangt Vorhaben, Standorte, Termin für den Echtbetrieb und die
  Leistungsbeschreibung des Angebots – Anforderungen an ein künftiges System, keine
  Inventur eines vorhandenen.
- **Berichtigung nach § 153 AO, Selbstanzeige, laufendes Straf- oder
  Bußgeldverfahren:** Der Sachverhalt gehört nach `DATENSCHUTZ.md` (Zone Rot) in kein
  KI-Werkzeug. Diese Vorschaltfrage klärt der Berufsträger vorab und vermerkt sie in
  der Handakte.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Die Skill bekommt die Inventur unmittelbar; niemand maskiert vorher. Deshalb zuerst:

1. Bestätigung einholen, dass Steuer-Identifikationsnummer, Steuernummer,
   Bezeichnung des Finanzamts und Aktenzeichen vollständig entfernt sind – nicht
   teilmaskiert, nicht in Ausschnitten, auch nicht in Auszügen aus Kauf-, Miet- oder
   Leasingverträgen und Herstellerunterlagen.
2. **Seriennummern werden nicht eingefügt**, erfasst wird nur `vorhanden ja/nein/
   unbekannt`. Dasselbe gilt für die Steuernummer: Sie ist Nr. 2 des Datensatzes nach
   § 146a Abs. 4 AO, wird hier aber weder abgefragt noch ausgegeben, sondern nur als
   „(nicht im Werkzeug – in der Kanzlei einzusetzen)" geführt – auch dann, wenn die
   Lückenliste sonst vollständig wäre.
3. Nur neutrale Kennungen: `Mandant A`, `Betriebsstätte 1`, `System 1`. Kein
   Finanzamt wird benannt.
4. Taucht Zone-Rot-Material auf, wird abgebrochen, nicht bereinigt. Rückmeldung:
   welche Angabe in welcher Zeile steht und die Bitte, die Inventur ohne diese Spalte
   erneut einzufügen – Systemart, Hersteller und Bezeichnung, Anzahl gleichartiger
   Systeme, Seriennummer vorhanden (ja/nein/unbekannt, ohne die Nummer selbst), Art
   der Sicherheitseinrichtung, Vorgang mit Monat und Jahr, Beschaffungsform,
   ersetztes Vorgängersystem und Meldestand genügen. Das ersetzte Vorgängersystem
   ist keine Nebenspalte: Ohne sie lässt sich ein Systemwechsel nicht als zwei
   Vorgänge führen.
5. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung
   des Anbieters nach § 62a StBerG müssen vor dem Einsatz geklärt sein; bei
   unmittelbarem Einsatz für ein konkretes Mandat klärt der Berufsträger vorab
   § 62a Abs. 5 StBerG. Einzelheiten in `DATENSCHUTZ.md`.

## Ablauf

1. **Datensparsamkeit abschließen** und die Vorschaltfrage des Berufsträgers zu
   § 153 AO, Selbstanzeige und laufendem Verfahren als beantwortet bestätigen lassen.
2. **Rahmen aufnehmen:** Zahl der Betriebsstätten, Zahl der beiliegenden Inventuren,
   Stand der Zuständigkeitsfeststellung, ob eine Kassen-Nachschau oder Außenprüfung
   anhängig oder angekündigt ist. Weichen die beiden Zahlen ab, wird das sofort
   festgehalten – für Betriebsstätten ohne Inventur ist keine Mitteilung vorbereitbar.
3. **Eindeutigkeit einschätzen:** eindeutig / vertretbare Varianten / nicht ohne
   weitere Angaben entscheidbar, mit Aufzählung der fehlenden Angaben. „Unbekannt"
   ist ein Ergebnis, kein Anlass zum Raten – und kein Abbruchgrund. Auch eine
   Inventur, deren Spalten überwiegend „unbekannt" tragen, wird vollständig
   abgearbeitet; die betroffenen Spalten werden als überwiegend unbekannt gemeldet
   und ihre Zeilen in die Lückenliste übernommen.
4. **Systemabgrenzung je Zeile:** Ist das System von § 146a Abs. 1 AO erfasst? Die
   Skill folgt dem Prüfschema der Prompt-Datei, Schritt 2, und entscheidet nicht aus
   dem Gedächtnis. Zeilen mit „unklar" gehen unbewertet in die Lückenliste.
5. **Vorgangsermittlung je erfasster Zeile** nach Schritt 3 der Prompt-Datei. Ein
   Systemwechsel wird als zwei Vorgänge geführt; gemietete und geleaste Systeme
   werden nicht weggelassen; „nein" oder „unbekannt" im Meldestand wird als
   möglicherweise bereits versäumte Mitteilung behandelt, nicht als offener Termin.
6. **Datensatzvollständigkeit je Vorgang** nach Schritt 4 der Prompt-Datei: Die acht
   Angaben werden einzeln mit „liegt vor" oder „fehlt" abgehakt. Für Steuernummer und
   Seriennummer wird kein Wert ausgegeben, sondern der Vermerk „in der Kanzlei
   einzusetzen"; sie erscheinen in der Lückenliste als Beschaffungsposition mit
   Zuständigkeit, nicht als abzufragende Angabe. Steht die Art der zertifizierten
   technischen Sicherheitseinrichtung auf „keine" oder „unbekannt", ist das nicht nur
   eine Datensatzlücke: Die Skill vermerkt zusätzlich „Systemfrage – gehört in die
   Prüfung der laufenden Kassenführung (Prompt 38)" und bewertet sie hier nicht.
7. **Vollständigkeit je Betriebsstätte prüfen – der Kern dieser Skill.** Bei jeder
   Mitteilung sind stets **alle** Systeme der betroffenen Betriebsstätte zu
   übermitteln, auch die bereits gemeldeten und die unverändert im Bestand
   befindlichen; eine Einzelmeldung des neuen oder des abgemeldeten Systems genügt
   nie. Die Skill prüft deshalb je Betriebsstätte, ob die Inventur vollständig ist,
   und benennt jede Lücke ausdrücklich, statt einen einzelnen Vorgang als meldefertig
   auszuweisen. In der Vorgangsliste steht je Vorgang, welche Systeme der
   Betriebsstätte er umfasst.
8. **Zuständigkeit, Fristarten, Sanktionslage und Anlass** nach den Schritten 6 bis 9
   der Prompt-Datei. Kein Finanzamt benennen, kein Fristende berechnen, kein Bußgeld
   für die unterbliebene Mitteilung nennen.
9. **Aussteuerung beachten – kein Abbruch.** Steht im Rahmenfeld zur Kassen-Nachschau
   oder Außenprüfung ein „ja", entstehen Bestandsübersicht, Vorgangsliste und
   Lückenliste unverändert, und alle übrigen Abschnitte werden vollständig
   abgearbeitet. Auch das Mandantenanschreiben wird ausgegeben, beschränkt auf die
   reine Anforderung der fehlenden Angaben. Zur Reihenfolge und zum Zeitpunkt des
   Nachholens unterbliebener Mitteilungen steht ausschließlich der Aussteuerungssatz
   aus der Prompt-Datei.
10. **Mandantenanschreiben erzeugen** – Sie-Form, höchstens 300 Wörter, ohne Vorwurf
    und ohne Sanktionshinweis, je fehlende Angabe mit dem Hinweis, wo der Mandant sie
    findet.
11. **Ergebnis ablegen.** Die Abschnittsreihenfolge folgt dem Ausgabeformat der
    Prompt-Datei; der Lückenliste wird ein Kopfsatz mit der Zahl der offenen
    Positionen vorangestellt, damit sie beim Öffnen der Datei zuerst ins Auge fällt.

## Ergebnis

Eine Datei `<Mandatskürzel>-kassensysteme-meldebestand-<JJJJ-MM>.md`, bei
Fortschreibung eine neue Datei mit neuem Monatsstand. Inhalt und Reihenfolge folgen
dem Ausgabeformat der Prompt-Datei, von der Bestandsübersicht je Betriebsstätte über
Vorgangsliste, Lückenliste, Fristarten und Mandantenanschreiben bis zur Tabelle der
zu prüfenden Rechtsgrundlagen. Die Lückenliste bleibt auch dann bestehen, wenn nur
Steuernummer, Seriennummer oder die Art der zertifizierten technischen
Sicherheitseinrichtung fehlen – ohne diese Angaben ist keine Übermittlung möglich,
gleich wie klar der Vorgang ist.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Bestandsübersicht und Vorgangsliste werden von einer
  zweiten Person gegen die Inventur des Mandanten nachgeprüft; die Freigabe der
  Mitteilung und des Anschreibens erteilt ein Berufsträger (Freigabestufe 3 in
  `DATENSCHUTZ.md`).
- **Die Skill berechnet keine Fristen.** Sie benennt nur die Fristarten mit ihrer
  Fundstelle; das Fristende bestimmt ein Mensch und erfasst es im Fristenprogramm.
- **Vollständigkeit je Betriebsstätte kontrollieren, bevor übermittelt wird.** Eine
  Mitteilung, die nur den neuen Vorgang enthält, ist der häufigste Fehler.
- **Keine Sanktionsdrohung stehen lassen:** Die Mitteilungspflicht nach
  § 146a Abs. 4 AO ist selbst nicht bußgeldbewehrt; ein entsprechender Hinweis im
  Entwurf wird gestrichen.
- **Zone Rot kontrollieren – auch in der Ausgabe.** Steuernummer, Seriennummern,
  Bezeichnung des Finanzamts und Aktenzeichen stehen weder in der Eingabe noch im
  Ergebnis; sie setzt ein Mensch erst in Mein ELSTER oder in der Kanzleisoftware ein.
- **„Unklar" entscheidet ein Berufsträger** anhand des Wortlauts und der
  Herstellerunterlagen, nicht das Modell.
- **Vermutungen kennzeichnen:** Jede Aussage über den Sachverhalt, die nicht aus der
  Inventur folgt, steht im Ergebnis ausdrücklich als Vermutung.
- **Ergebnis in der Mandantenakte dokumentieren**, einschließlich der Systeme und
  Betriebsstätten, für die der Mandant keine Angaben liefern konnte.
- **Rechtsstand:** Die Skill führt keine eigene Fundstellensammlung; geprüft wird an
  den in der Prompt-Datei genannten Fundstellen. In der Ausgabe steht gleichwohl zu
  jeder rechtlichen Aussage die Rechtsgrundlage mit Absatz und Satz und dem Zusatz
  `für [JAHR] verifizieren`; ist eine Fundstelle unsicher, steht dort „Fundstelle
  offen – bitte recherchieren".

## Grundlage

Diese Skill führt den Prompt
[prompts/07-gobd-kasse/106-kassensystem-mitteilungspflicht.md](../../../prompts/07-gobd-kasse/106-kassensystem-mitteilungspflicht.md)
aus; Prüfschema, Abgrenzung und Fundstellen stehen dort und gelten unverändert.
