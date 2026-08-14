# 124 – Verrechnungspreise: Sachverhaltsaufnahme vor der Dokumentation

**Problem:** Der Mandant hat eine Tochter, eine Mutter oder eine nahestehende Person im Ausland, zwischen ihnen laufen Lieferungen, Dienstleistungen, Darlehen, Lizenzen und Umlagen – und bevor irgendjemand über Dokumentation redet, weiß niemand geordnet, welche Transaktionen es überhaupt gibt, wer welche Funktion ausübt, wer welches Risiko trägt und welche Verträge existieren.
**Rolle:** Steuerberater, Sachbearbeitung mit Auslandsberührung, Berufsträger bei der Übergabe an einen Spezialisten
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Sachkonten und Verrechnungskonten für Leistungsbeziehungen zu verbundenen Unternehmen, Fremdwährungsbuchungen, Debitoren und Kreditoren im Konzernkreis, Datenprüfung und Datenzugriff Z1–Z3, wenn die Aufzeichnungen in der Außenprüfung angefordert werden), DATEV DMS (Verträge, Umlagevereinbarungen, vorhandene Dokumentationsteile), DATEV Fristen und Bescheide (Erfassung der Vorlagefristen), DATEV Arbeitsplatz und Eigenorganisation (Wiedervorlage, Zuständigkeit); Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Beteiligungsstruktur mit Ländern und Beteiligungshöhen, Art und Kurzbeschreibung jeder grenzüberschreitenden Geschäftsbeziehung im Zeitraum, Vorjahresumsatz oberhalb oder unterhalb von 100 Mio. €, die Summen der Entgelte für Lieferungen und der Vergütungen für andere Leistungen aus Geschäftsbeziehungen mit nahestehenden Personen im laufenden Wirtschaftsjahr (für die Erleichterung nach § 6 GAufzV), Angabe zu außergewöhnlichen Geschäftsvorfällen, Liste der vorhandenen Verträge, Stand der vorhandenen Dokumentation, Stand des Verfahrens (Prüfungsanordnung bekanntgegeben, Aufzeichnungen angefordert).
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Firmierungen der verbundenen Unternehmen, Namen von Gesellschaftern und handelnden Personen durch Platzhalter ersetzen (`Mandant A`, `Gesellschaft B`, `Gesellschafter 1`); für die Aufnahme genügen Rechtsform, Land, Beteiligungshöhe und Funktion. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts gehören nie in ein KI-Werkzeug – auch nicht maskiert und auch nicht in Ausschnitten (Zone Rot in `DATENSCHUTZ.md`); Verträge sind vor dem Einfügen um Kopf- und Unterschriftenteil, Anschriften, Bankverbindungen und Registernummern zu kürzen. Kalkulationen und Preislisten verbundener Unternehmen sind Geschäftsgeheimnisse Dritter und werden für diesen Prompt nicht gebraucht. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`; wird das Werkzeug unmittelbar für dieses Einzelmandat eingesetzt, klärt der Berufsträger vorab die Erforderlichkeit einer Mandanteneinwilligung (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und nimmst grenz-
überschreitende Leistungsbeziehungen zwischen nahestehenden Personen auf.
Du arbeitest wie bei einer Erstaufnahme: erst vollständig erfassen, was es
gibt, dann ordnen, dann benennen, was fehlt. Du bewertest nicht.

AUFGABE
Erzeuge aus den Angaben eine geordnete Sachverhaltsaufnahme: Transaktions-
übersicht, Funktions- und Risikoübersicht, Liste der außergewöhnlichen
Geschäftsvorfälle, Fristen- und Sanktionsübersicht, Unterlagenliste und einen
Übergabevermerk für einen Spezialisten.

WAS DIESER PROMPT NICHT TUT – das gehört zur Aufgabe
Er prüft keine Angemessenheit. Er wählt keine Verrechnungspreismethode. Er
ermittelt keine Preise, keine Bandbreiten, keine Margen, keine Kostenaufschläge
und keine Vergleichswerte. Er erstellt weder die Angemessenheitsdokumentation
(§ 90 Abs. 3 Satz 2 Nr. 3 AO – für [JAHR] verifizieren) noch die Stamm-
dokumentation. Er liefert die Grundlage, auf der ein Berufsträger entscheidet,
was selbst erstellt und was an einen Spezialisten übergeben wird.

SPERRE – PREISERMITTLUNG (gilt unabhängig von den Eingaben, kein Abbruch)
Stehen im Eingabeteil Preise, Margen, Kostenaufschläge, Zins- oder Lizenzsätze
oder Umlageschlüssel, übernimmst du sie unverändert in die Spalte "Angabe des
Mandanten" und schreibst in die Hinweisspalte: "Nicht Gegenstand dieses
Durchlaufs – Angemessenheit und Methodenwahl durch einen Spezialisten."
Du gibst dazu keine eigene Zahl, keinen Vergleichswert und keine Einschätzung
aus, auch nicht als Beispiel und auch nicht auf Nachfrage im selben Durchlauf.
Alle übrigen Schritte arbeitest du normal weiter.

MANDANT UND STRUKTUR
- Rechtsform des inländischen Mandanten: [ANGABE]
- Sitz und Ort der Geschäftsleitung, nur als Land und Kategorie:
  [Inland / Land im übrigen Gemeinschaftsgebiet / Drittland]; Ort und
  Anschrift bleiben draußen
- Nahestehende Personen im Ausland, je Zeile Land, Rechtsform,
  Beteiligungshöhe in Prozent, Richtung der Beteiligung: [ANGABE]
- Beteiligung von mindestens einem Viertel bei mindestens einer der genannten
  Personen: [ja / nein / unklar]
- Betriebsstätte im Ausland oder inländische Betriebsstätte eines
  ausländischen Unternehmens: [nein / ja], Land: [LAND]
- Vorjahresumsatz: [über 100 Mio. € / bis 100 Mio. € / unbekannt]
- Summe der Entgelte für Lieferungen von Gütern oder Waren aus Geschäfts-
  beziehungen mit nahestehenden Personen im laufenden Wirtschaftsjahr:
  [über 6.000.000 € / bis 6.000.000 € / unbekannt]
- Summe der Vergütungen für andere Leistungen als Lieferungen aus Geschäfts-
  beziehungen mit nahestehenden Personen im laufenden Wirtschaftsjahr:
  [über 600.000 € / bis 600.000 € / unbekannt]

GESCHÄFTSBEZIEHUNGEN IM ZEITRAUM
- Zeitraum der Aufnahme: [ZEITRAUM]
- Arten: [Warenlieferungen / Dienstleistungen / Darlehen und Sicherheiten /
  Lizenzen und Namensnutzung / Kostenumlagen / Personalentsendung / sonstige]
- Kurzbeschreibung je Geschäftsbeziehung, ohne Preisangaben: [ANGABE]
- Außergewöhnliche Geschäftsvorfälle im Zeitraum, etwa Umstrukturierung,
  Funktionsverlagerung, Übertragung von Wirtschaftsgütern oder wesentliche
  Vertragsänderung: [nein / ja], welche: [ANGABE]

VERTRÄGE UND DOKUMENTATION
- Schriftliche Verträge: [alle / teilweise / keine]
- Vorhandene Dokumentation: [keine / Transaktionsmatrix /
  Sachverhaltsdokumentation / Angemessenheitsdokumentation /
  Stammdokumentation], Stand: [STAND]
- Zeitnahe Aufzeichnungen zu außergewöhnlichen Geschäftsvorfällen:
  [ja / nein / entfällt]

VERFAHRENSSTAND
- Prüfungsanordnung bekanntgegeben: [ja / nein]
- Aufzeichnungen vom Finanzamt angefordert: [ja / nein]
- Qualifiziertes Mitwirkungsverlangen nach § 200a AO eingegangen:
  [ja / nein] – bei "ja" ist Prompt 109 vorrangig zu bearbeiten

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab und benenne fehlende
   Angaben, statt sie zu erfinden. Eine kurze zutreffende Aufnahme ist besser
   als eine vollständige erfundene.
2. Leite jede Zeile der Übersichten AUS DEN ANGABEN ab. Ergänze keine
   Transaktion, die nicht genannt ist; frage sie stattdessen nach.
3. Kennzeichne jede Aussage, bei der du dir nicht sicher bist oder bei der
   sich die Rechtslage geändert haben könnte. Rate nicht.
4. Trenne durchgehend Angabe des Mandanten, Feststellung aus den Unterlagen
   und Vermutung. Jede Vermutung kennzeichnest du als Vermutung.
5. Rechtsgrundlagen nennst du positiv, jeweils mit dem Zusatz
   "für [JAHR] verifizieren", und führst sie am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" auf. Mindestens zu nennen, soweit
   im Fall berührt:
   - § 1 Abs. 1 Satz 1 AStG: Berichtigung von Einkünften nach dem
     Fremdvergleichsgrundsatz, wenn Einkünfte aus einer Geschäftsbeziehung
     zum Ausland mit einer nahestehenden Person durch nicht fremdübliche
     Bedingungen, "insbesondere Preise (Verrechnungspreise)", gemindert sind
   - § 1 Abs. 2 AStG: nahestehende Person, unter anderem bei einer Beteiligung
     von mindestens einem Viertel
   - § 1 Abs. 5 AStG und § 1a AStG, wenn eine Betriebsstätte betroffen ist
   - § 90 Abs. 3 Satz 1 AO: Aufzeichnungspflicht für Geschäftsbeziehungen
     im Sinne des § 1 Abs. 4 AStG
   - § 90 Abs. 3 Satz 2 AO: Nr. 1 Transaktionsmatrix,
     Nr. 2 Sachverhaltsdokumentation, Nr. 3 Angemessenheitsdokumentation
   - § 6 der Gewinnabgrenzungsaufzeichnungs-Verordnung (GAufzV),
     "Anwendungsregelungen für kleinere Unternehmen und für Steuerpflichtige
     mit anderen als Gewinneinkünften": Prüfe und benenne als eigenen offenen
     Punkt, ob die Erleichterung für kleinere Unternehmen in Betracht kommt.
     Kleinere Unternehmen sind nach § 6 Abs. 2 Satz 1 GAufzV solche, bei denen
     im laufenden Wirtschaftsjahr die Summe der Entgelte für die Lieferung von
     Gütern oder Waren aus Geschäftsbeziehungen mit nahestehenden Personen
     6.000.000 € nicht übersteigt (Nr. 1) und die Summe der Vergütungen für
     andere Leistungen 600.000 € nicht übersteigt (Nr. 2)
     (Betragsgrenzen – für [JAHR] verifizieren). Der Bogen erhebt diese
     Summen nicht; fordere sie an und ENTSCHEIDE die Erleichterung nicht.
     Weise zusätzlich darauf hin, dass § 6 GAufzV auf die Satzzählung des
     § 90 Abs. 3 AO in der Fassung VOR dem Vierten Bürokratieentlastungsgesetz
     verweist und das Verhältnis zu § 90 Abs. 4 AO in der geltenden Fassung
     deshalb gesondert am Volltext zu klären ist
     (Fundstelle – für [JAHR] verifizieren)
   - § 90 Abs. 3 Satz 3 AO: Stammdokumentation ab 100 Mio. €
     Vorjahresumsatz (Betragsgrenze – für [JAHR] verifizieren); ordne anhand
     des Feldes "Vorjahresumsatz" zu, ob sie in Betracht kommt, und schreibe
     bei "unbekannt" die Klärung in die offenen Punkte
   - § 90 Abs. 3 Satz 5 AO: zeitnahe Aufzeichnungen zu außergewöhnlichen
     Geschäftsvorfällen
   - § 90 Abs. 4 AO für die Vorlage (siehe Nummer 7)
   - § 162 Abs. 3 und Abs. 4 AO für die Folgen (siehe Nummer 8)
   - Art. 97 § 37 Abs. 5 EGAO: die geänderten §§ 90 und 162 Abs. 4 AO sind ab
     dem 01.01.2025 anzuwenden; die Änderung stammt aus dem Vierten
     Bürokratieentlastungsgesetz vom 23.10.2024, BGBl. 2024 I Nr. 323
   Bist du dir einer Fundstelle nicht sicher, schreibe "Fundstelle offen –
   bitte recherchieren" statt einer Angabe.
6. Stelle klar: Die Aufzeichnungspflichten und ihr Inhalt stehen in § 90
   Abs. 3 AO, die Vorlage und ihre Fristen ausschließlich in § 90 Abs. 4 AO.
7. Berechne KEINE Frist und nenne kein Datum. Benenne die gesetzlichen
   Vorlageregeln, jeweils mit dem Zusatz "für [JAHR] verifizieren":
   - § 90 Abs. 4 Satz 1 AO: Anforderung ist jederzeit möglich
   - § 90 Abs. 4 Satz 2 AO: Vorlage innerhalb von 30 Tagen nach Anforderung
   - § 90 Abs. 4 Satz 3 AO: im Fall einer Außenprüfung sind Transaktions-
     matrix, Stammdokumentation und Aufzeichnungen über außergewöhnliche
     Geschäftsvorfälle OHNE gesondertes Verlangen innerhalb von 30 Tagen nach
     Bekanntgabe der Prüfungsanordnung vorzulegen
   - § 90 Abs. 4 Satz 4 AO: Verlängerung in begründeten Einzelfällen
   Weise ausdrücklich darauf hin, dass Satz 3 in der Praxis der wichtigste
   Punkt ist: die Vorlage kommt ungefragt und hängt an der Prüfungsanordnung,
   nicht an einer Aufforderung. Ergänze: "Fristen berechnet und erfasst ein
   Mensch."
8. Benenne die Folgen einer Pflichtverletzung ohne Prognose, ob sie eintritt,
   jeweils mit dem Zusatz "für [JAHR] verifizieren":
   - § 162 Abs. 3 AO: widerlegbare Vermutung höherer Einkünfte bei Verletzung
     des § 90 Abs. 3 AO; Satz 2 Ausschöpfung des Preisrahmens zu Lasten des
     Steuerpflichtigen
   - § 162 Abs. 4 Satz 1 AO: Zuschlag 5.000 €
   - § 162 Abs. 4 Satz 2 AO: mindestens 5 %, höchstens 10 % des Mehrbetrags
     der Einkünfte, wenn sich danach mehr als 5.000 € ergeben
   - § 162 Abs. 4 Satz 4 AO: bei verspäteter Vorlage verwertbarer
     Aufzeichnungen bis 1.000.000 €, mindestens 100 € je vollem Tag
   - § 162 Abs. 4 Satz 6 AO: Absehen bei entschuldbarer oder nur geringfügig
     schuldhafter Pflichtverletzung
9. OECD-Verrechnungspreisleitlinien und OECD-Musterabkommen darfst du als
   Auslegungshilfe benennen. Schreibe in demselben Satz dazu, dass sie kein
   unmittelbar geltendes Recht sind: anwendbar sind die deutschen Vorschriften
   und das jeweilige Doppelbesteuerungsabkommen (Art. 59 Abs. 2 Satz 1 GG,
   § 2 Abs. 1 AO – für [JAHR] verifizieren). Leite aus ihnen keine Pflicht ab.
10. Steht im Feld "Prüfungsanordnung bekanntgegeben" oder im Feld
   "Aufzeichnungen vom Finanzamt angefordert" ein "ja", stellst du die
   Fristenübersicht als Position 0 VOR die Position 1 und setzt darüber den
   Satz:
   "Sofort dem Berufsträger vorlegen und Frist im Fristenprogramm erfassen."
   Steht im Feld "Qualifiziertes Mitwirkungsverlangen nach § 200a AO" ein
   "ja", setzt du als ersten offenen Punkt: "Prompt 109 vorrangig bearbeiten –
   Erfüllungsfrist und Anfechtungsfrist sofort gesondert erfassen."
11. Höchstens 15 Zeilen in der Transaktionsübersicht. Fasse gleichartige
    Vorgänge zu einer Zeile zusammen und vermerke die Zusammenfassung.

AUSGABEFORMAT
1. (Eindeutigkeit) – wie belastbar die Aufnahme mit den vorliegenden Angaben
   ist, in drei Sätzen.
2. (Transaktionsübersicht) – Tabelle:
   Transaktion | Gegenpartei und Land | Art | Vertrag vorhanden |
   wer übt welche Funktion aus | wer trägt welches Risiko |
   wer stellt welche Wirtschaftsgüter | Dokumentation vorhanden |
   Angabe des Mandanten | Hinweis (nur "Nicht Gegenstand dieses Durchlaufs –
   Angemessenheit und Methodenwahl durch einen Spezialisten" oder "offen: …";
   keine eigene Bewertung)
3. (Funktions- und Risikoübersicht) – je beteiligtem Unternehmen: ausgeübte
   Funktionen, getragene Risiken, eingesetzte Wirtschaftsgüter, jeweils mit
   der Quelle der Angabe (Vertrag, Auskunft, Vermutung). Steht im Feld
   "Betriebsstätte" ein "ja", ergänze eine eigene Zeile für die Betriebsstätte
   und benenne § 1 Abs. 5 AStG und § 1a AStG als gesondert zu prüfende
   Grundlagen (für [JAHR] verifizieren), ohne sie zu prüfen.
4. (Außergewöhnliche Geschäftsvorfälle) – Liste mit Hinweis auf § 90 Abs. 3
   Satz 5 AO und § 90 Abs. 4 Satz 3 AO, je Vorfall mit der Angabe aus dem Feld
   "Zeitnahe Aufzeichnungen"; steht im Bogen "nein", schreibe "keine benannt –
   im Erstgespräch gezielt nachfragen".
5. (Vorlage und Fristen) – Übersicht nach Anforderung 7, ohne Datum, ohne
   Berechnung, mit dem Satz "Fristen berechnet und erfasst ein Mensch."
6. (Folgen einer Pflichtverletzung) – Übersicht nach Anforderung 8.
7. (Anzufordernde Unterlagen) – abhakbar, Kästchen ☐ vor jeder Position,
   gegliedert nach: Verträge | Buchhaltung und Auswertungen |
   Struktur und Beteiligungen | vorhandene Dokumentationsteile |
   Auskünfte von Personen im Unternehmen.
8. (Übergabevermerk an einen Spezialisten) – höchstens eine Seite:
   Struktur in drei Sätzen (Rechtsform, Sitz und Ort der Geschäftsleitung,
   Beteiligungen mit Land und Höhe), Liste der Transaktionen, was dokumentiert
   ist, was fehlt, Verfahrensstand, konkrete Fragestellung an den
   Spezialisten. Keine Bewertung, keine Zahl aus der Sperre.
9. (Offene Punkte) – was für eine belastbare Aufnahme noch fehlt, mit
   Angabe, wer es liefern kann.
10. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. **Vorschaltfrage vor dem Werkzeugeinsatz, vom Berufsträger zu beantworten und in der Handakte zu vermerken:** Gibt es Anhaltspunkte, dass bereits abgegebene Erklärungen wegen der Verrechnungspreise unrichtig sind? Falls ja, wird der Fall außerhalb des KI-Werkzeugs bearbeitet – Berichtigungs-, Selbstanzeige- und Strafsachverhalte gehören nach `DATENSCHUTZ.md` in die Zone Rot und damit auch nicht als Ja-Nein-Feld in den Prompt.
2. Zuerst die Struktur klären, dann die Transaktionen. Wer mit der Transaktionsliste beginnt, übersieht regelmäßig die nahestehende Person ohne Beteiligung.
3. Verträge nur gekürzt einfügen; für die Aufnahme genügen Vertragsgegenstand, Laufzeit, Leistungspflichten und Risikoverteilung.
4. Die Zeile „außergewöhnliche Geschäftsvorfälle" ehrlich ausfüllen. Sie entscheidet über die zeitnahe Aufzeichnung und über die ungefragte Vorlage in der Prüfung.
5. Ergebnis nicht als Dokumentation ablegen, sondern als Aufnahme. Die Dokumentation entsteht danach – in der Kanzlei oder beim Spezialisten.
6. Übergabevermerk vor dem Versand an einen Spezialisten vom Berufsträger freigeben und um die Angaben ergänzen, die nach `DATENSCHUTZ.md` nicht in das Werkzeug durften.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Die Aufnahme wird von einer Person erstellt und von einer zweiten Person anhand der Verträge und der Buchhaltung nachgeprüft und abgezeichnet.** Das Modell liefert einen Entwurf, keine Feststellung.
- **Alle Fristen dieses Verfahrens – Vorlage nach Anforderung und Vorlage nach Bekanntgabe der Prüfungsanordnung – werden von einem Menschen berechnet, geprüft und im Fristenprogramm erfasst.** Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- Prüfen, dass die Ausgabe keine Aussage zur Angemessenheit, keine Methode, keine Bandbreite und keine Marge enthält. Findet sich eine, ist die Sperre verletzt und die Ausgabe zu verwerfen.
- Norm und Absatz gegenprüfen: Aufzeichnungspflicht § 90 Abs. 3 AO, Vorlage und Fristen § 90 Abs. 4 AO. Eine Ausgabe, die die 30 Tage in Abs. 3 verortet, ist falsch.
- Anwendungsvorschrift prüfen: Art. 97 § 37 Abs. 5 EGAO, geänderte Fassung ab 01.01.2025 aus dem Vierten Bürokratieentlastungsgesetz vom 23.10.2024, BGBl. 2024 I Nr. 323 (für [JAHR] verifizieren).
- § 1 AStG ist die Norm zu den Verrechnungspreisen. Nennt die Ausgabe weitere Vorschriften des AStG, ist zu prüfen, ob sie überhaupt Verrechnungspreise betreffen.
- **Erleichterung für kleinere Unternehmen prüfen, bevor der volle Pflichtenkatalog an den Mandanten geht.** § 6 der Gewinnabgrenzungsaufzeichnungs-Verordnung („Anwendungsregelungen für kleinere Unternehmen und für Steuerpflichtige mit anderen als Gewinneinkünften") knüpft an die Summen des § 6 Abs. 2 Satz 1 GAufzV an – 6.000.000 € für Lieferungen, 600.000 € für andere Leistungen (Beträge und Fundstelle – für [JAHR] verifizieren). § 6 GAufzV verweist noch auf die Satzzählung des § 90 Abs. 3 AO vor dem Vierten Bürokratieentlastungsgesetz; das Verhältnis zu § 90 Abs. 4 AO in der geltenden Fassung ist am Volltext zu klären. Eine Ausgabe, die einem kleineren Unternehmen ungeprüft die volle Dokumentation zuschreibt, ist zu korrigieren.
- OECD-Leitlinien und OECD-Musterabkommen sind kein unmittelbar geltendes Recht (Art. 59 Abs. 2 Satz 1 GG, § 2 Abs. 1 AO – für [JAHR] verifizieren). Jede Pflicht muss aus deutschem Recht oder dem konkreten Abkommen folgen.
- Bei Betriebsstättenfällen ist zusätzlich zu klären, ob § 1 Abs. 5 AStG und § 1a AStG einschlägig sind; die Aufnahme allein trägt das nicht.
- Geht in der Prüfung ein qualifiziertes Mitwirkungsverlangen nach § 200a AO ein, hat Prompt 109 Vorrang; Frist und Anfechtungsfrist werden sofort gesondert erfasst.
- Für kleine und mittlere Kanzleien gilt ehrlich: Dieser Prompt dient der Aufnahme und der Weitergabe, nicht der abschließenden Bearbeitung.

## Varianten

- **Nur Darlehen und Finanzierung:** „Beschränke die Aufnahme auf Darlehen, Sicherheiten, Cash-Pooling und Bürgschaften; erfasse je Vorgang Laufzeit, Währung, Besicherung und Vertragslage – ohne jede Aussage zum Zinssatz."
- **Betriebsstättenfall:** „Erweitere die Funktions- und Risikoübersicht um die Zuordnung von Personalfunktionen, Wirtschaftsgütern und Chancen zur Betriebsstätte und nenne § 1 Abs. 5 und § 1a AStG als zu prüfende Grundlagen."
- **Vorbereitung der Außenprüfung:** „Erzeuge zusätzlich eine Gegenüberstellung: nach § 90 Abs. 3 Satz 2 und 3 AO geforderter Bestandteil | vorhanden ja/nein | wer erstellt ihn | bis wann intern fällig." Ergänzend Prompt 34.
- **Angebot an den Mandanten:** „Formuliere aus dem Übergabevermerk ein neutrales Mandantenschreiben, das den Aufnahmestand, den offenen Bedarf und die nächsten Schritte beschreibt – ohne Risikobewertung und ohne Betragsangabe."
