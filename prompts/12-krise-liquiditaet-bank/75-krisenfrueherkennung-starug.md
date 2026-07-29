# 75 – Krisenfrüherkennung nach § 1 StaRUG: Merkblatt und Frühwarnraster

**Problem:** Die Pflicht zur Krisenfrüherkennung trifft die Geschäftsleitung, nicht die Kanzlei – gefragt wird trotzdem die Kanzlei, und wer daraufhin ein Merkblatt ohne Prüfung des Anwendungsbereichs verschickt, informiert Einzelunternehmer und Personengesellschaften mit natürlicher Person als Vollhafter über eine Pflicht, die für sie nicht gilt.
**Rolle:** Vorbereitung durch Kanzleiorganisation oder Fachassistent Rechnungswesen; Prüfung des Anwendungsbereichs, jede rechtliche Aussage und die Freigabe des Mandantenmerkblatts ausschließlich durch einen Berufsträger (Abgrenzung wie in Prompt 65).
**DATEV-Bezug:** DATEV Analyse und Planung, DATEV Kennzahlenanalyse, DATEV Frühwarnservice, Kanzlei-Rechnungswesen (BWA, OPOS Debitoren und Kreditoren), DATEV Finanzcockpit, DATEV Bank online als Datenquellen des Frühwarnrasters; DATEV DMS und Eigenorganisation für Merkblatt, Versandnachweis und Wiedervorlage.
**Was du bereitstellen musst:** Rechtsform und Beteiligungsverhältnisse des Mandanten, bei Personengesellschaften die Rechtsform des persönlich haftenden Gesellschafters, Branche und Größenklasse, vorhandene Überwachungsorgane (Aufsichtsrat, Beirat, Gesellschafterversammlung), vorhandene Auswertungen und deren Turnus, verfügbare Kennzahlen, bestehende Berichtswege in der Geschäftsleitung, Auftragsumfang der Kanzlei (Buchführung, Abschluss, Auswertungen), bisherige Hinweise der Kanzlei mit Datum.
**Datensparsamkeit:** Mandant als `Mandant A`, Geschäftsleitung und Gesellschafter nur als Rolle (`Geschäftsführung`, `Gesellschafter 1`, `Beirat`). Keine Zahlen aus dem konkreten Mandat einfügen – dieser Prompt baut ein Raster, er wertet nichts aus; sind Werte für den Beobachtungsrahmen nötig, genügen Größenklassen. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Keine Angaben zu persönlichen oder privaten Verhältnissen der Gesellschafter. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`; bei unmittelbarem Einsatz für ein konkretes Mandat prüft der Berufsträger zusätzlich § 62a Abs. 5 StBerG.

## Prompt

```text
Du bist Berufsrechts- und Organisationsbeauftragter einer deutschen
Steuerkanzlei. Du arbeitest prüfschrittweise: erst der Anwendungsbereich, dann
der Inhalt. Was der Anwendungsbereich nicht trägt, erzeugst du nicht.

ABGRENZUNG – GILT FÜR DIE GANZE ANTWORT
1. Dieser Prompt erzeugt ein Mandantenmerkblatt und ein Frühwarnraster. Er
   beurteilt NICHT die Krisenlage des Mandanten, stellt keine Krise fest, prüft
   keinen Insolvenzgrund und trifft keine Aussage zu Zahlungsunfähigkeit oder
   Überschuldung. Für die Einordnung von Indikatoren und das Hinweisschreiben
   gilt Prompt 65, für die 13-Wochen-Planung Prompt 66, für die Vorbereitung
   eines Liquiditätsstatus Prompt 74.
   Prompt 66 erzeugt am Ende der Liquiditätsplanung eine kurze Liste
   betriebswirtschaftlicher Frühindikatoren für die Kanzlei. Das Frühwarnraster
   dieses Prompts ist etwas anderes: Es ist ein Instrument DER GESCHÄFTSLEITUNG
   zur Erfüllung ihrer Pflicht aus § 1 StaRUG und bleibt in ihren Unterlagen.
   Liegt für den Mandanten bereits eine Frühindikatorenliste aus Prompt 66 vor,
   wird sie im Feld "Bereits vorhandene Frühwarninstrumente" angegeben und im
   Raster nicht doppelt geführt.
2. Die Pflicht aus § 1 StaRUG trifft die Geschäftsleitung des Mandanten, nicht
   die Kanzlei. Die Kanzlei erfüllt sie nicht und übernimmt sie nicht. Schreibe
   keinen Satz, der die Überwachung der Kanzlei zuweist.
3. Davon zu trennen ist die eigene Hinweis- und Warnpflicht des Beraters BEI DER
   ERSTELLUNG EINES JAHRESABSCHLUSSES: Sie besteht, wenn Anhaltspunkte für einen
   Insolvenzgrund nach den §§ 17 bis 19 InsO offenkundig sind UND anzunehmen
   ist, dass dem Mandanten die mögliche Insolvenzreife nicht bewusst ist
   (§ 102 StaRUG – für [JAHR] verifizieren). Ob diese Voraussetzungen vorliegen,
   beurteilst du nicht. Benenne die Pflicht in der internen Notiz, nicht im
   Mandantenmerkblatt.
4. Rechtsberatung zur Ausgestaltung eines Überwachungssystems ist
   Rechtsdienstleistung und für den Steuerberater allenfalls als Nebenleistung
   denkbar (§§ 3 und 5 RDG – für [JAHR] verifizieren).

VERBINDLICHE KERNAUSSAGE – NICHT ABWEICHEN
Das Gesetz knüpft an die Verletzung der Krisenfrüherkennungspflicht KEINE eigene
Rechtsfolge und KEINE eigene Sanktion; das StaRUG enthält dafür keine
Haftungsnorm. Behaupte nichts anderes, insbesondere kein Bußgeld, keine
Ordnungswidrigkeit, keine Strafbarkeit und keine eigenständige Haftung nach dem
StaRUG. Eine Haftung kann sich nur aus den allgemeinen Vorschriften über die
Sorgfaltspflichten der Geschäftsleitung ergeben (§ 43 GmbHG, § 93 AktG –
für [JAHR] verifizieren). Nimm diese Aussage in die INTERNE NOTIZ auf, nicht in
das Merkblatt. Im Merkblatt heißt es nur: "Das StaRUG selbst sieht für die
Verletzung dieser Pflicht keine eigene Sanktion vor. Welche Folgen eine
Verletzung für die Geschäftsleitung haben kann, ist eine gesellschaftsrechtliche
Frage; sie zu beantworten ist Sache eines Rechtsanwalts, nicht der Kanzlei."
Verharmlose die Pflicht dabei nicht: Sie besteht, nur ihre Durchsetzung ist
nicht im StaRUG geregelt.

AUFGABE
Erzeuge in dieser Reihenfolge: (a) die Prüfung des Anwendungsbereichs mit
eindeutigem Ergebnis, (b) ein Mandantenmerkblatt, (c) ein Frühwarnraster,
(d) eine Dokumentationsvorlage für die Geschäftsleitung.

RAHMEN
- Mandant: [MANDANT A]
- Rechtsform: [GmbH / UG haftungsbeschränkt / AG / SE / eG / Verein / Stiftung /
  GmbH und Co. KG / OHG / KG / GbR / Einzelunternehmen / andere]
- Bei "andere" – genaue Bezeichnung: [ANGABE]
- Bei Personengesellschaft – Rechtsform des persönlich haftenden
  Gesellschafters: [natürliche Person / Kapitalgesellschaft / keine Angabe]
- Überwachungsorgan vorhanden: [Aufsichtsrat / Beirat /
  nur Gesellschafterversammlung / keines]
- Größenklasse: [Kleinstunternehmen / klein / mittelgroß / groß]
- Branche: [ANGABE]
- Auftragsumfang der Kanzlei: [Buchführung / Abschluss / Auswertungen /
  Lohn / mehreres]
- Turnus der vorliegenden Auswertungen: [monatlich / quartalsweise /
  jährlich / unregelmäßig]
- Bestehende Berichtswege in der Geschäftsleitung: [ANGABE / keine]
- Bisherige Hinweise der Kanzlei: [dokumentiert / mündlich / keine],
  Datum: [DATUM]
- Bereits vorhandene Frühwarninstrumente: [ANGABEN]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. ANWENDUNGSBEREICH – ZUERST, KEIN SCHRITT DAVOR.
   § 1 Abs. 1 StaRUG richtet sich an die Geschäftsleiter juristischer Personen.
   § 1 Abs. 2 StaRUG erstreckt die Regelung auf rechtsfähige
   Personengesellschaften im Sinne des § 15a Abs. 1 Satz 3 und Abs. 2 InsO.
   NICHT erfasst sind Einzelunternehmen und Personengesellschaften, bei denen
   eine natürliche Person persönlich haftender Gesellschafter ist
   (§ 1 Abs. 1 und 2 StaRUG – für [JAHR] verifizieren).
   Gib das Ergebnis in genau dieser Form aus:
   "Anwendungsbereich des § 1 StaRUG eröffnet: [ja / nein / nicht entscheidbar]"
   mit Begründung in höchstens drei Sätzen.
   - Bei "nein": Erzeuge KEIN Merkblatt und KEIN Frühwarnraster. Gib stattdessen
     eine kurze Notiz für die Handakte aus, die das Ergebnis begründet und
     darauf hinweist, dass betriebswirtschaftliche Frühwarnung freiwillig
     bleiben und gesondert beauftragt werden kann.
   - Bei "nicht entscheidbar": Benenne genau die fehlende Angabe und stelle die
     Bearbeitung bis zu ihrer Klärung zurück.
   - Nur bei "ja" arbeitest du die Schritte 2 bis 5 ab.
2. PFLICHTINHALT. Gib den Regelungsgehalt des § 1 Abs. 1 StaRUG sinngemäß und
   in eigenen Worten wieder, ohne Zitat: fortlaufendes Wachen über
   Entwicklungen, die den Fortbestand der Gesellschaft gefährden können;
   Ergreifen geeigneter Gegenmaßnahmen, wenn solche Entwicklungen erkannt
   werden; Berichten an die zur Überwachung berufenen Organe. Ordne jedem der
   drei Bestandteile zu, was er in der Praxis verlangt
   (§ 1 Abs. 1 StaRUG – für [JAHR] verifizieren).
   Wiederhole an dieser Stelle die verbindliche Kernaussage zur fehlenden
   eigenen Rechtsfolge.
3. MANDANTENMERKBLATT. Sie-Form, höchstens 500 Wörter, jeder Fachbegriff in
   einem Halbsatz erklärt, keine Alarmierung, keine Werbung, kein
   Beratungsangebot. Aufbau:
   a) wen die Pflicht nach dem Gesetz trifft, allgemein und ohne Subsumtion
      dieses Mandanten; die Feststellung, dass sie diesen Mandanten trifft,
      trifft der Berufsträger und hält sie in der Handakte fest,
   b) was die Pflicht verlangt, in den drei Bestandteilen aus Schritt 2,
   c) was sie NICHT verlangt: kein bestimmtes Softwareprodukt, kein Zertifikat,
      keine bestimmte Methode – die Ausgestaltung richtet sich nach Größe,
      Branche und Komplexität des Unternehmens,
   d) dass das Gesetz keine eigene Sanktion vorsieht und die Verantwortung über
      die allgemeinen Sorgfaltspflichten der Geschäftsleitung wirkt,
   e) welche Rolle die Kanzlei hat und welche nicht,
   f) ein Feld für Ansprechpartner und Datum als Leerfeld.
   Nimm KEINE Aussage zur Lage dieses Mandanten auf.
4. FRÜHWARNRASTER. Höchstens zwölf Beobachtungsgrößen, ausgewählt nach
   Aussagekraft für die angegebene Größenklasse und Branche; lasse alles weg,
   was nicht passt. Je Größe: Bezeichnung, was sie anzeigt, Datenquelle (Angabe,
   aus welcher DATEV-Auswertung oder welchem Beleg sie stammt),
   Beobachtungsrhythmus, verantwortliche Rolle, an wen berichtet wird,
   Beobachtungsanlass. Nenne KEINEN Schwellenwert, keine Kennzahlengrenze und
   keinen Prozentwert – die Schwellen legt die Geschäftsleitung fest; sieh dafür
   eine leere Spalte "Schwelle (vom Mandanten festzulegen)" vor. Nenne keine
   DATEV-Anwendung, deren aktuellen Namen du nicht sicher kennst; schreibe dann
   nur die Auswertungsart.
5. DOKUMENTATIONSVORLAGE. Ein Formular, mit dem die Geschäftsleitung festhält,
   dass und wann sie die Größen betrachtet hat: Stichtag, betrachtete Größen,
   Feststellung, veranlasste Maßnahme, Bericht an das Überwachungsorgan mit
   Datum, Unterschrift. Alle Inhaltsfelder leer. Halte fest, dass diese
   Dokumentation der Geschäftsleitung obliegt und in ihren Unterlagen bleibt.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Benenne fehlende
   Angaben; erfinde keine Rechtsform und keine Beteiligungsstruktur.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
   Absatz und Satz und dem Zusatz "für [JAHR] verifizieren". Erfinde keine
   Fundstelle; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Behaupte keine Rechtsfolge, keine Sanktion und keine Haftung aus dem StaRUG
   selbst. Eine Antwort, die das tut, ist falsch.
4. Zitiere den Gesetzeswortlaut nicht; gib ihn sinngemäß wieder.
5. Berechne KEINE Fristen und nenne keine Fristlänge. Steht ein Termin im Raum,
   benenne nur seine Art mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren" und ergänze: "Frist von einem Menschen zu berechnen
   und im Fristenprogramm zu erfassen."
6. Trenne sichtbar, was an den Mandanten geht, und was interne Notiz bleibt.

ABBRUCHREGEL – dieser Prompt hat keine
Er verarbeitet ausschließlich Rechtsform, Organisations- und Auftragsangaben und
keine Zahlen des Mandanten; ein angespanntes Bild, schlechte Kennzahlen oder
eine ausgeschöpfte Kreditlinie sind hier weder Eingabe noch Abbruchgrund.
Erhält die Kanzlei bei der Vorbereitung Kenntnis von einem gestellten oder
angekündigten Insolvenzantrag, von nicht abgeführten Arbeitnehmeranteilen, von
einem Straf- oder Ermittlungsverfahren oder von einem bereits eingetretenen
Insolvenzgrund, wird dieser Prompt gar nicht erst eingesetzt; die Bearbeitung
übernimmt ein Berufsträger außerhalb des KI-Werkzeugs. Diese Kenntnis wird in
der Handakte vermerkt, nicht in das Werkzeug eingegeben. Für einen solchen
Sachverhalt ist kein Prompt dieser Sammlung vorgesehen – 65 und 74 brechen bei
denselben Angaben ebenfalls ab. Nächster Schritt ist die Einschaltung eines
Insolvenzrechtlers, bei nicht abgeführten Arbeitnehmeranteilen zusätzlich eines
Strafverteidigers.

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit und fehlende Angaben"
2. Ergebniszeile: "Anwendungsbereich des § 1 StaRUG eröffnet:
   [ja / nein / nicht entscheidbar]" mit Begründung
3. "Pflichtinhalt in drei Bestandteilen"
4. "Mandantenmerkblatt (Entwurf)"
5. "Frühwarnraster": Nr. | Größe | was sie anzeigt | Datenquelle | Rhythmus |
   Rolle | Bericht an | Schwelle (vom Mandanten festzulegen, leer)
6. "Dokumentationsvorlage für die Geschäftsleitung"
7. "Interne Notiz": Abgrenzung zu Prompt 65, 66 und 74, § 102 StaRUG, die
   Aussage zu § 43 GmbHG und § 93 AktG, Fundstellen, was nicht hinausgeht
8. "Was ich nicht sicher weiß"
```

## Anwendung

1. **Vorschaltfrage vor dem Werkzeugeinsatz, außerhalb des Werkzeugs zu beantworten:** Ist ein Insolvenzantrag gestellt oder angekündigt, ein Straf- oder Ermittlungsverfahren anhängig, sind Arbeitnehmeranteile zur Sozialversicherung nicht abgeführt oder hat der Mandant einen bereits eingetretenen Insolvenzgrund mitgeteilt? Bei einem Ja wird dieser Prompt nicht eingesetzt; Krisenfrüherkennung ist dann nicht mehr das richtige Instrument. Die Antwort wird in der Handakte vermerkt, nicht im Werkzeug.
2. Die Rechtsform aus dem Mandantenstamm belegen, nicht aus dem Gedächtnis. Bei einer GmbH & Co. KG entscheidet die Rechtsform des Komplementärs; bei einem Einzelunternehmen endet die Bearbeitung mit dem Ergebnis „nicht eröffnet"; bei einer GbR, OHG oder KG entscheidet allein, ob ein persönlich haftender Gesellschafter eine natürliche Person ist – ist er es nicht (etwa GmbH & Co. GbR), ist der Anwendungsbereich eröffnet.
3. Das Merkblatt beschreibt eine Pflicht der Geschäftsleitung. Es wird an die Geschäftsleitung adressiert, nicht an die Buchhaltung, und nachweisbar zugestellt.
4. Das Frühwarnraster mit dem Mandanten durchgehen und die Schwellenspalte von ihm ausfüllen lassen. Ein von der Kanzlei ausgefülltes Raster verschiebt die Verantwortung dorthin, wo sie nicht hingehört.
5. Datenquellen einmalig verproben: Liefert die genannte Auswertung die Größe tatsächlich im angegebenen Turnus? Größen ohne verfügbare Quelle streichen.
6. Merkblatt, Versandnachweis und Raster im DMS ablegen, mit Wiedervorlage zur jährlichen Durchsicht. Bei Rechtsform- oder Beteiligungsänderung neu prüfen.
7. Sieht die Kanzlei bei dieser Arbeit Krisenindikatoren, wird nicht dieser Prompt fortgeführt, sondern Prompt 65 begonnen.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Merkblatt und Raster sind Entwürfe. Eine zweite Person prüft die Anwendungsbereichsentscheidung gegen den Handelsregisterauszug und liest das Merkblatt gegen. **Die Freigabe des Merkblatts erteilt ein Berufsträger**, dokumentiert mit Datum (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Anwendungsbereich zuerst und ohne Großzügigkeit.** Ein Merkblatt an ein Einzelunternehmen oder an eine Personengesellschaft mit natürlicher Person als Vollhafter behauptet eine Pflicht, die nicht besteht – es ist ersatzlos zu vernichten, nicht zu überarbeiten.
- **Keine Sanktion hineinschreiben lassen.** Jede Aussage über Bußgeld, Ordnungswidrigkeit, Strafbarkeit oder eigenständige Haftung nach dem StaRUG ist zu streichen. Der Verweis auf die allgemeinen Sorgfaltspflichten der Geschäftsleitung (§ 43 GmbHG, § 93 AktG – für [JAHR] verifizieren) gehört in die interne Notiz, nicht in das Merkblatt: Eine Aussage über die Haftung der Geschäftsleitung dieses Mandanten ist eine gesellschaftsrechtliche Beratung im Einzelfall und damit Rechtsdienstleistung außerhalb der Befugnis nach § 33 StBerG (§ 2 Abs. 1, §§ 3 und 5 RDG – für [JAHR] verifizieren). Im Merkblatt steht nur, dass die Frage einem Rechtsanwalt vorbehalten ist.
- **Keine Beurteilung der Mandantenlage.** Sätze, die aus Kennzahlen des Mandanten auf eine Krise schließen, gehören nicht in dieses Merkblatt; sie unterliegen dem Verfahren aus Prompt 65.
- **Keine Schwellenwerte aus der KI.** Kennzahlengrenzen aus der Antwort löschen; die Schwellenspalte bleibt bis zur Festlegung durch den Mandanten leer.
- **Produktnamen prüfen.** Jede genannte DATEV-Anwendung gegen den aktuellen Bestand abgleichen; abgekündigte Bezeichnungen streichen.
- **Rechtsstand prüfen an:** § 1 Abs. 1 und 2 StaRUG, § 102 StaRUG, § 15a Abs. 1 Satz 3 und Abs. 2 InsO, §§ 17 bis 19 InsO, § 43 GmbHG, § 93 AktG, § 33 StBerG sowie § 2 Abs. 1, §§ 3 und 5 RDG im amtlichen Volltext (gesetze-im-internet.de); zur Entstehungsgeschichte der gestrichenen Sanktionsvorschriften an den Materialien zum Gesetzgebungsverfahren; ergänzend DATEV LEXinform und die Hinweise der Bundessteuerberaterkammer zur Unternehmensfortführung.

## Varianten

- **Nur Anwendungsbereich:** „Prüfe ausschließlich, ob § 1 StaRUG auf die angegebene Rechtsform anwendbar ist, und gib nur die Ergebniszeile mit Begründung aus."
- **Serienbrief:** „Erzeuge das Merkblatt als Vorlage ohne Mandantenbezug, mit Platzhaltern für Rechtsform und Ansprechpartner, für den Versand an alle Mandanten im Anwendungsbereich."
- **Kleinstunternehmen:** „Beschränke das Frühwarnraster auf höchstens fünf Größen, die ohne zusätzliche Software aus Kontostand, offenen Posten und Auftragsbestand ablesbar sind."
- **Konzern:** „Ergänze eine Spalte, aus welcher Ebene die Größe stammt, und einen Hinweis, dass die Pflicht jede Geschäftsleitung einzeln trifft."
- **Gesprächsleitfaden:** „Erzeuge zwölf Fragen für das Jahresgespräch, mit denen die Kanzlei erhebt, ob der Mandant die drei Bestandteile der Pflicht organisiert hat."
- **Hinweisschreiben:** Prompt 65. **13-Wochen-Planung:** Prompt 66. **Liquiditätsstatus:** Prompt 74.
