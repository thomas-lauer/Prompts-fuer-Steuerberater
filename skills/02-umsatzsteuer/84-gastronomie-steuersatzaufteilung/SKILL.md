---
name: gastronomie-steuersatzaufteilung
description: Gleicht Speise- und Getränkekarte, Paketbeschreibungen und den Artikelstamm
  der Kasse gegeneinander ab und ordnet jedes Angebot Zeile für Zeile nach dem Prüfschema
  aus Prompt 84 zu: erst die Art der Leistung, dann der Steuersatz je Bestandteil, dann
  die Aufteilungsfrage beim Pauschalpreis. Erzeugt daraus die vollständige Artikelmatrix,
  die Änderungsaufträge für das Kassensystem, Rückfrageliste, Aufgabenliste,
  Mandantenschreiben und Prüfvermerk; sie rechnet keine Aufteilung aus und nennt keinen
  Steuersatz als Zahl. Use when a gastronomy or hotel client has combination offers,
  buffets, conference or all-inclusive packages at one flat price and the cash register
  article master has to be split by tax rate.
---

# 84 – Gastronomie: Steuersatzaufteilung bei Kombiangeboten

## Zweck

Die Skill führt die Zuordnung aus, die der Prompt beschreibt, und nimmt dabei die
Mengenarbeit ab: Karte, Paketbeschreibungen und Artikelstamm der Kasse werden
gegeneinander abgeglichen und **jede Position einzeln** durch dasselbe Raster
geführt. Ein Betrieb mit Mittagskarte, Abendkarte, Getränkekarte, Tagungspauschalen
und Aktionsangeboten kommt schnell auf mehrere hundert Zeilen, und der Fehler
entsteht nicht bei der schwierigen, sondern bei der übersehenen Zeile – bei dem
Kombiartikel, den niemand für einen Aufteilungsfall gehalten hat.

Sie rechnet nichts. Sie ordnet zu, hält je Zeile fest, worauf die Zuordnung sich
stützt und was zu ihrer Bestätigung fehlt, und liefert die Artikelmatrix so, dass
der Betrieb nur noch die Spalte mit dem Kassenschlüssel füllt. Die ausführliche
Begründung bleibt auf fünf Angebotstypen beschränkt – die Skill benennt, nach
welchem Kriterium sie diese fünf gewählt hat, damit nachvollziehbar bleibt, welche
Zeilen nur in der Matrix stehen.

## Wann einsetzen – und wann nicht

**Einsetzen**, wenn Angebote mit einem Pauschalpreis über mehrere Bestandteile
umsatzsteuerlich zuzuordnen sind – Buffets, Menüpauschalen, Tagungs- und
Business-Packages, Übernachtungspakete, All-inclusive-Angebote, Cateringpakete –
oder wenn nach einer Umstellung kontrolliert werden soll, ob der Artikelstamm der
Kasse die Zuordnung tatsächlich abbildet.

**Nicht einsetzen:**

- **Belege mit unrichtigem Steuerausweis liegen bereits vor:** Prompt 87. Er
  verlangt den Wortlaut des Steuerausweises, den Rechnungstyp, die Zusammensetzung
  des Empfängerkreises mit Nachweisquelle sowie Anzahl und Volumen der betroffenen
  Rechnungen – Angaben zur Berichtigung, nicht zur Zuordnung. Diese Skill ordnet zu
  und übergibt dorthin.
- **Die Gutscheinsystematik selbst ist zu klären:** Prompt 117. Er fragt Wortlaut
  und Bedingungen des Gutscheins, Einlösestellen, Einlöseraum, Ausgabe im eigenen
  oder fremden Namen, Übertragbarkeit und Restwertregelung ab. Hier steht nur
  Gutscheinart und Ausgabezeitpunkt im Bogen; steht dort „unklar", wird die Zeile
  nicht eingeordnet, sondern übergeben.
- **Laufende Kassenführung nach GoBD** – Tagesabschluss, Kassenbericht, Stornos,
  Belegausgabe, Einzelaufzeichnung: Prompt 38. Er fragt Kassenart und Anzahl,
  eingesetztes System, Vorhandensein einer technischen Sicherheitseinrichtung, Stand
  der Mitteilung an das Finanzamt und die Art der Kassenbuchführung ab und erzeugt
  eine Mandantencheckliste, keine Artikelzuordnung.
- **Die Verfahrensdokumentation soll geschrieben werden:** Prompt 37. Er verlangt
  die Beschreibung der tatsächlichen Abläufe – Belegarten und ihre Wege, wer scannt,
  womit, wer freigibt, wie gesichert wird. Diese Skill benennt nur, was aus der
  Umstellung heraus zu dokumentieren und fortzuschreiben ist.
- **Erwogene Selbstanzeige oder laufendes Steuerstrafverfahren:** Diese Angaben
  gehören nach `DATENSCHUTZ.md` (Zone Rot) in kein KI-Werkzeug. Zusammen mit einem
  erkennbaren Organisationsversagen der Kanzlei lösen sie die Abbruchregel der
  Prompt-Datei aus; sie steuern den betroffenen Zeitraum aus, nicht den ganzen
  Lauf – siehe Schritt 3.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Die Skill bekommt Karte und Artikelstamm unmittelbar; niemand maskiert vorher.
Deshalb zuerst:

1. Bestätigung einholen, dass Steuernummer, Steuer-Identifikationsnummer,
   Umsatzsteuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Seriennummer der
   technischen Sicherheitseinrichtung und Zertifikatsangaben der Kasse vollständig
   entfernt sind – nicht teilmaskiert, nicht in Ausschnitten, auch nicht in
   Auszügen aus Kassen- oder Herstellerunterlagen.
2. **Personenbezogene Kassendaten bleiben draußen:** Bedienernamen und
   Bedienerkennungen, Personalnummern, Trinkgeldzuordnungen, Kundenkonten und
   Namen von Veranstaltungskunden. Artikelstammexporte führen diese Spalten
   erfahrungsgemäß mit, ohne dass jemand sie erwartet – sie werden vor dem Einfügen
   gelöscht, nicht ausgeblendet.
3. Nur neutrale Kennungen: `Mandant A`, `Betrieb 1`, `Veranstaltungskunde 1`.
   Anschriften der Betriebsstätten entfallen ersatzlos.
4. Taucht Zone-Rot-Material auf, wird angehalten, nicht bereinigt. Die Rückmeldung
   nennt Spalte und Zeile und sagt, was stattdessen genügt: Artikelbezeichnung,
   enthaltene Bestandteile, Preis, Verzehrart, Anlass und der derzeit hinterlegte
   Steuerschlüssel. Mehr braucht die Zuordnung nicht.
5. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung
   des Anbieters nach § 62a StBerG (sorgfältige Auswahl, Vertrag in Textform mit
   Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das
   Erforderliche) müssen vor dem Einsatz geklärt sein; bei unmittelbarem Einsatz für
   ein konkretes Mandat klärt der Berufsträger vorab § 62a Abs. 5 StBerG.
   Einzelheiten in `DATENSCHUTZ.md`.

## Ablauf

1. **Datensparsamkeit abschließen.** Ohne die Bestätigung wird keine Zeile
   aufgenommen.
2. **Rahmen aufnehmen:** Betriebsart, betrachteter Zeitraum, Kontenrahmen,
   Kassensystem mit der Angabe, ob Set- oder Kombiartikel und die Umschaltung der
   Verzehrart möglich sind, Stand der Verfahrensdokumentation, Stand der bereits
   abgegebenen Voranmeldungen. Was fehlt, wird nachgefordert und nicht unterstellt:
   Ohne die Angaben zur Leistungsfähigkeit der Kasse entsteht kein Änderungsauftrag,
   sondern eine offene Frage.
3. **Aussteuern, bevor zugeordnet wird.** Noch vor dem ersten Abgleich wird
   geprüft, ob die Angaben eine erwogene Selbstanzeige, ein laufendes
   Steuerstrafverfahren oder ein Organisationsversagen der Kanzlei benennen. Ist
   das für einen Zeitraum der Fall, wird für ihn nicht weitergearbeitet; dafür
   steht ausschließlich der Aussteuerungssatz der Prompt-Datei, und weder
   Artikelmatrix noch Änderungsauftrag noch Mandantenschreiben nehmen diesen
   Zeitraum auf. Die übrigen Zeiträume laufen vollständig weiter, und die Skill
   sagt ausdrücklich, welchen sie ausgesteuert hat. Diese Prüfung steht hier und
   nicht am Ende: Eine Aussteuerung nach abgeschlossener Zuordnung hätte die
   Bearbeitung nicht verhindert. Bereits abgegebene Voranmeldungen mit
   unzutreffender Zuordnung sind **kein** Abbruchgrund: Sie gehören unter die
   Übergabepunkte, die Prüfung einer Berichtigung nach § 153 AO ist Aufgabe des
   Berufsträgers.
4. **Karte und Artikelstamm gegeneinander abgleichen – der eigentliche Mengenschritt.**
   Beide Quellen führen selten dieselben Bezeichnungen. Die Skill bildet drei
   Zeilengruppen: Positionen in beiden Quellen, Kartenposition ohne Artikel im
   Stamm, Artikel im Stamm ohne Kartenposition. Sie führt nichts stillschweigend
   zusammen; jede Zuordnung zweier abweichender Bezeichnungen wird als solche
   ausgewiesen. Am Ende meldet sie, wie viele Zeilen je Gruppe entstanden sind.
5. **Eindeutigkeit einschätzen** und fehlende Angaben je Angebot einzeln benennen.
   Fehlt die Beschreibung der Dienstleistungselemente, wird die Art der Leistung
   **nicht** entschieden, sondern angefordert – auch dann, wenn das Ergebnis
   naheliegt.
6. **Art der Leistung je Zeile bestimmen, vor jeder Steuersatzfrage.** Die Skill
   folgt dem Prüfschema der Prompt-Datei, Schritt 1, und entscheidet nicht aus dem
   Gedächtnis. Die Reihenfolge wird nicht umgedreht; Ergebnis je Zeile ist auch
   „nicht entscheidbar", und diese Zeilen gehen unbewertet in die Rückfrageliste.
   Derselbe Artikel kann am Tisch und über die Theke unterschiedlich ausfallen –
   dann entstehen zwei Zeilen, nicht eine.
7. **Zeitliche Anwendung je Umsatz** nach Schritt 2 der Prompt-Datei. Gesondert
   geführt werden Anzahlungen und Vorausrechnungen über den Jahreswechsel,
   Gutscheine nach ihrer Art und Veranstaltungen, die über den Jahreswechsel laufen.
   Steht bei einem Gutschein „unklar", wird er nicht eingeordnet, sondern an
   Prompt 117 übergeben.
8. **Steuersatz je Bestandteil und Prüfung auf einheitliche Leistung** nach den
   Schritten 3 und 4 der Prompt-Datei, Bestandteil für Bestandteil: Speisen,
   Getränke, Übernachtung und die damit verbundenen Leistungen, Raumnutzung,
   Technik, Betreuung, Eintritt, Transport. Jede Pauschale, die Getränke enthält,
   wird als Aufteilungsfall markiert, auch wenn die Karte nur einen Preis kennt.
   Kein Steuersatz und kein Prozentsatz als Zahl – nur ermäßigter oder allgemeiner
   Steuersatz mit dem Zusatz `für [JAHR] verifizieren`.
9. **Aufteilung des Pauschalpreises darstellen, nicht rechnen** (Schritt 5 der
   Prompt-Datei): Maßstab, in Betracht kommende Nichtbeanstandungsregelung mit ihren
   Voraussetzungen, Prozentsatz ausschließlich als nachzuschlagende Größe, bestehende
   Wahlrechte und was ihre Ausübung dokumentarisch voraussetzt. Die Rechengrößen
   werden so aufbereitet, dass ein Mensch die Aufteilung im Fachprogramm vornimmt.
10. **Artikelmatrix vollständig erzeugen.** Jede Zeile aus Schritt 4 wird
    aufgenommen, auch die eindeutigen und die aus der Gruppe „Artikel ohne
    Kartenposition". Die Spalte Kassenschlüssel bleibt leer. Die ausführliche
    Begründung erhalten höchstens fünf Angebotstypen; die Skill nennt das
    Auswahlkriterium und listet auf, welche Zeilen nur zugeordnet und nicht
    erläutert wurden.
11. **Änderungsaufträge für das Kassensystem und Dokumentationspflichten** nach den
    Schritten 7 und 8 der Prompt-Datei, je Auftrag mit Rolle und Nachweis. Keine
    Aufbewahrungsdauer als Zahl, keine Frist.
12. **Übrige Ergebnisse erzeugen und ablegen:** Übergabepunkte, Rückfrageliste,
    Aufgabenliste mit ☐, Mandantenschreiben von höchstens 250 Wörtern in Sie-Form
    ohne Steuersatz als Zahl und ohne Ergebniszusage, Prüfvermerk für die Akte. Die
    Abschnittsreihenfolge folgt dem Ausgabeformat der Prompt-Datei.

## Ergebnis

Eine Datei `<Mandatskürzel>-steuersatzmatrix-<JJJJ-MM>.md`; bei der
Umstellungskontrolle nach einigen Wochen eine neue Datei mit neuem Monatsstand,
damit der Vorher-Nachher-Vergleich möglich bleibt.

Inhalt und Reihenfolge folgen dem Ausgabeformat der Prompt-Datei: Eindeutigkeit und
Datenlage, Art der Leistung je Angebot, zeitliche Anwendung, Steuersatzzuordnung je
Bestandteil, einheitliche oder mehrere Leistungen, Aufteilung mit
Nichtbeanstandungsregelung und Rechengrößen, Artikelmatrix, Änderungen im
Kassensystem mit Rollen, Aufzeichnungs- und Dokumentationspflichten, Übergabepunkte,
Rückfrageliste, Aufgabenliste, Mandantenschreiben, Prüfvermerk, interne Notiz und –
als letzter Abschnitt, wie im Ausgabeformat vorgesehen – was unsicher geblieben
ist. Nur das Mandantenschreiben wird für den Versand entnommen; alles Übrige
bleibt intern.

## Qualitätssicherung

Das Ergebnis ist ein Entwurf und kennt nur, was in Karte und Artikelstamm stand.

- **Vier-Augen-Prinzip:** Eine zweite fachkundige Person nimmt die Artikelmatrix
  Zeile für Zeile gegen Karte und Artikelstamm nach, vorrangig die Zeilengruppe mit
  abweichenden Bezeichnungen. Mandantenschreiben und jede Auskunft zur
  Steuersatzzuordnung gibt ein Berufsträger frei (Freigabestufe 3 in
  `DATENSCHUTZ.md`).
- **Die Skill rechnet nicht:** keine Aufteilung eines Pauschalpreises, kein
  Entgeltanteil, kein Steuerbetrag, keine Frist. Die Rechenarbeit erledigt ein
  Mensch im Fachprogramm.
- **Kein Prozentsatz aus der Antwort.** Der Prozentsatz einer
  Nichtbeanstandungsregelung wird am BMF-Schreiben abgelesen und die Inanspruchnahme
  dokumentiert; ein aus dieser Ausgabe übernommener Wert ist kein Beleg.
- **Rechtsgrundlage ist das Steueränderungsgesetz 2025.** Eine Ausgabe, die
  § 12 Abs. 2 Nr. 15 UStG dem Investitionssofortprogramm zuschreibt, wird verworfen
  und der Lauf wiederholt.
- **Erst die Art der Leistung, dann der Steuersatz.** Ist die Reihenfolge in der
  Ausgabe vertauscht, ist das Ergebnis unbrauchbar, auch wenn die Zuordnung zufällig
  stimmt.
- **Vor der Umstellung einen Testbon je Angebotstyp** erzeugen und gegen die
  Artikelmatrix halten; ein falsch hinterlegter Setartikel produziert den Fehler
  tausendfach. Änderungen am Artikelstamm und an den Steuerschlüsseln mit Datum
  protokollieren und die Verfahrensdokumentation zur Kasse fortschreiben.
- **Zuordnen und Berichtigen trennen.** Liegen Belege mit unrichtigem Steuerausweis
  vor, wird an Prompt 87 übergeben, bevor weitere Belege ausgegeben werden; dort
  hängt schon die Frage, ob die Steuer entsteht, vom Empfängerkreis ab.
- **Vermutungen kennzeichnen:** Jede Zuordnung, die von der tatsächlichen
  Ausgestaltung im Betrieb abhängt, steht ausdrücklich als Vermutung mit der
  Feststellung, die sie bestätigen würde.
- **Zone Rot auch in der Ausgabe kontrollieren:** keine Nummer, kein Aktenzeichen,
  keine Bedienerkennung, auch nicht in Beispielzeilen.
- **Rechtsstand:** Die Skill führt keine eigene Fundstellensammlung; geprüft wird an
  den in der Prompt-Datei genannten Fundstellen. In der Ausgabe steht gleichwohl zu
  jeder rechtlichen Aussage die Rechtsgrundlage mit Absatz, Satz und Nummer und dem
  Zusatz `für [JAHR] verifizieren`; ist eine Fundstelle unsicher, steht dort
  „Fundstelle offen – bitte recherchieren".

## Grundlage

Prüfschema, Rechtsrahmen und Ausgabeformat stehen in der Prompt-Datei
[prompts/02-umsatzsteuer/84-gastronomie-steuersatzaufteilung.md](../../../prompts/02-umsatzsteuer/84-gastronomie-steuersatzaufteilung.md);
die Skill folgt ihr und schreibt sie nicht ab.
