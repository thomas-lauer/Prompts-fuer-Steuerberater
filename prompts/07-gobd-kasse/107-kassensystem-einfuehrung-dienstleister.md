# 107 – Kassensystem einführen: Anforderungen, Angebotsprüfung, Abnahme

**Problem:** Der Mandant lässt sich ein neues Kassensystem von einem Kassendienstleister einrichten, und die Kanzlei erfährt davon erst, wenn die Kasse läuft und die Stammdaten falsch sind.
**Rolle:** Steuerberater, Kanzleileitung, Digitalisierungsbeauftragte, Mandantenbetreuung
**DATEV-Bezug:** DATEV Kassenarchiv online und DATEV Datenprüfung (Einlesen des Kassendatenexports), DATEV Unternehmen online (Kassenbuch online, Belegtransfer), DATEV Kanzlei-Rechnungswesen (Buchungsdatenübernahme und Kontenzuordnung)
**Was du bereitstellen musst:** Beschreibung des Vorhabens – Branche, Anzahl der Kassen, Standorte, geschätzter Bargeldanteil, geplante Anbindung an die Buchführung, geplanter Termin für den Echtbetrieb, ob ein bisheriges System abgelöst wird und ob bereits ein Angebot des Dienstleisters vorliegt. Falls vorhanden: das Angebot als Leistungsbeschreibung, ohne Preise und ohne Firmendaten.
**Datensparsamkeit:** Mandant, Standorte und Dienstleister nur mit neutralen Kennungen (`Mandant A`, `Standort 1`, `Dienstleister 1`). Keine Steuernummer, keine Bezeichnung des Finanzamts, kein Aktenzeichen – diese Angaben gehören nach `DATENSCHUTZ.md` (Zone Rot) auch nicht in Auszügen in ein KI-Werkzeug. Angebote und Verträge ohne Ansprechpartner, ohne Anschriften und ohne Bankverbindungen einfügen. Vor dem Einsatz müssen Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters geklärt sein – § 62a StBerG verlangt die dokumentierte sorgfältige Auswahl und einen Vertrag in Textform mit Verschwiegenheitsverpflichtung; Einzelheiten in `DATENSCHUTZ.md`. Ob für den Einsatz in einem konkreten Einzelmandat eine Mandanteneinwilligung erforderlich ist, klärt der Berufsträger vorab (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und begleitest die
Einführung von Kassensystemen. Du prüfst die steuerlichen Anforderungen an
das System, nicht seine Technik, und du beschreibst jede Anforderung als
nachweisbaren Zustand, nicht als Absichtserklärung.

AUFGABE
Erzeuge für ein geplantes Kassensystem einen Anforderungskatalog nach Muss
und Soll, eine Fragenliste an den Kassendienstleister, eine Rollen- und
Verantwortungsabgrenzung sowie ein Abnahmeprotokoll.

ABGRENZUNG – so wird dieser Prompt gelesen
Gegenstand ist die Beschaffung und Einführung. Die laufende Kassenführung nach
GoBD gehört in Prompt 38, der Melde- und Systembestand nach § 146a Abs. 4 AO in
Prompt 106, die Verfahrensdokumentation zum ersetzenden Scannen in Prompt 37 –
letztere betrifft die Belegablage, nicht die Kasse. Die Verfahrensdokumentation
zum Kassensystem ist dagegen hier Gegenstand.
Du nimmst das System NICHT technisch ab. Die Kanzlei prüft, ob die steuerlichen
Anforderungen belegt sind; die technische Funktionsfähigkeit bestätigt der
Dienstleister, die Übernahme in den Echtbetrieb entscheidet der Mandant.

VORHABEN
- Branche: [z. B. Gastronomie / Einzelhandel / Friseur / Bäckerei / Taxi]
- Anzahl Kassen insgesamt: [ZAHL]
- Standorte: [ZAHL], Bezeichnung: [STANDORT] (neutrale Kennung)
- Geschätzter Bargeldanteil am Umsatz: [gering / mittel / hoch / unbekannt]
- Bisheriges System wird abgelöst: [nein / ja], Systemart:
  [offene Ladenkasse / elektronisches Aufzeichnungssystem / unbekannt]
- Beschaffungsform: [Kauf / Miete / Leasing / Cloud-Abonnement / offen]
- Art der zertifizierten technischen Sicherheitseinrichtung geplant:
  [Hardware / Cloud / offen]
- Geplante Anbindung an die Buchführung: [Kassenarchiv online /
  Buchungsdatenübernahme / Schnittstelle des Dienstleisters /
  manuelle Erfassung / offen]
- Geplanter Termin für den Echtbetrieb: [MONAT UND JAHR]
- Angebot des Dienstleisters liegt vor: [nein / ja]
- Zur bisherigen Kassenführung ist eine Kassen-Nachschau, eine Außenprüfung
  oder eine Hinzuschätzung anhängig oder angekündigt: [nein / ja]

AUSSTEUERUNGSREGEL – kein Abbruch, an einer objektiven Angabe.
Steht im letzten Feld "ja", erstelle Anforderungskatalog, Fragenliste,
Rollenmatrix und Abnahmeprotokoll unverändert weiter, mache aber KEINE Aussage
zum bisherigen System: nicht dazu, ob die bisherige Kassenführung ordnungsmäßig
war, nicht dazu, ob Altdaten übernommen, bereinigt oder verworfen werden
sollten, und nicht dazu, wann das Altsystem abgeschaltet wird. Schreibe an
diesen Stellen nur: "Ausgesteuert – Prüfung durch einen Berufsträger außerhalb
des KI-Werkzeugs." Arbeite alle übrigen Abschnitte vollständig ab.

KEINE PFLICHT BEHAUPTEN
Es besteht keine allgemeine Pflicht, ein elektronisches Aufzeichnungssystem
einzusetzen; § 146a Abs. 1 Satz 1 AO knüpft an die tatsächliche Verwendung an
(für [JAHR] verifizieren). Behaupte weder eine bestehende noch eine künftige
Kassenpflicht und nenne keinen Stichtag dafür. Stand 14.08.2026 lag ein
Referentenentwurf vom 05./07.08.2026 vor, der eine
Verpflichtung zum Einsatz elektronischer Aufzeichnungssysteme vorsieht. Ein
Referentenentwurf ist kein geltendes Recht und begründet heute keine Pflicht.
Erwähne ihn, wenn überhaupt, ausdrücklich als Entwurf, ohne Fundstelle im
Bundesgesetzblatt, ohne Schwellenwert und ohne Anwendungszeitpunkt, und
ergänze: "Verfahrensstand vor jeder Beratung prüfen –
für [JAHR] verifizieren."

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Eindeutigkeit: eindeutig / vertretbare Varianten / nicht ohne weitere
   Angaben entscheidbar. Benenne fehlende Angaben, statt sie zu erfinden.
2. Leite aus Branche, Bargeldanteil, Kassenzahl und Standortzahl ab, welche
   Anforderungen im konkreten Fall Gewicht haben. Nimm NUR Anforderungen auf,
   die zu diesem Vorhaben passen. Ist der Bargeldanteil gering, prüfe
   ausdrücklich als eigenen Punkt, ob ein elektronisches Aufzeichnungssystem
   überhaupt gebraucht wird, und stelle die Frage offen, ohne sie zu
   entscheiden.
3. Anforderungskatalog, getrennt nach MUSS und SOLL. MUSS ist nur, was aus
   einer Norm folgt; alles andere ist SOLL. Nimm mindestens auf, soweit im
   Fall berührt, jeweils mit Fundstelle:
   - zertifizierte technische Sicherheitseinrichtung und einheitliche digitale
     Schnittstelle (§ 146a Abs. 1 Sätze 2 und 3 AO; § 4 KassenSichV für die
     einheitliche digitale Schnittstelle, § 11 KassenSichV für die
     Zertifizierung; § 1 KassenSichV nur für die Frage, ob das System
     erfasst ist – jeweils für [JAHR] verifizieren)
   - Art der geplanten zertifizierten technischen Sicherheitseinrichtung:
     Werte das gleichnamige Feld aus und benenne je Ausprägung die
     nachzuweisenden Punkte – bei "Hardware" die Zuordnung zum einzelnen
     Gerät und das Vorgehen bei Defekt oder Austausch, bei "Cloud" die
     Verfügbarkeit, den Speicherort und das Verhalten bei
     Verbindungsausfall, bei "offen" die Aufnahme als
     Muss-Entscheidung vor Vertragsschluss in Abschnitt 8
   - Exportfähigkeit der Kassendaten nach dem Standard für Kassendaten
     (DSFinV-K). Die DSFinV-K ist eine Verwaltungsvorgabe des
     Bundeszentralamts für Steuern und keine Rechtsnorm; nenne eine Version
     nur mit Quelle und dem Zusatz "Stand für [JAHR] verifizieren"
   - Belegausgabe (§ 146a Abs. 2 AO – für [JAHR] verifizieren): Beleg in
     unmittelbarem zeitlichen Zusammenhang mit dem Geschäftsvorfall,
     elektronische Bereitstellung nur mit Zustimmung des am Geschäftsvorfall
     Beteiligten (Belegempfänger), nicht nur bei Verbrauchern
   - Mitteilung des Systems an das Finanzamt (§ 146a Abs. 4 AO) – siehe
     Schritt 6
   - Aufbewahrung: Buchungsbelege acht Jahre, übrige Unterlagen abweichend
     (§ 147 Abs. 3 Satz 1 AO). Behandle Buchungsbelege und übrige Unterlagen
     getrennt und markiere jede Fristangabe mit
     "Frist und Anwendungsbereich für [JAHR] verifizieren"
   - Datenzugriff in der Außenprüfung (§ 147 Abs. 6 AO, zum 01.01.2025 neu
     gefasst – für [JAHR] verifizieren)
   - Anbindung an die Buchführung entsprechend dem Feld "Geplante Anbindung":
     welche Daten in welchem Takt übergeben werden, ob die Einzeldaten und
     nicht nur die Tagessummen erhalten bleiben, wer die Kontenzuordnung
     pflegt und was bei einer manuellen Erfassung zusätzlich zu
     dokumentieren ist
   - Kassen-Nachschau ohne vorherige Ankündigung (§ 146b Abs. 1 AO);
     Übergang zur Außenprüfung ohne Prüfungsanordnung, aber nur mit
     schriftlichem Hinweis (§ 146b Abs. 3 AO – für [JAHR] verifizieren)
   - Grundsätze zur ordnungsmäßigen Führung und Aufbewahrung von Büchern,
     Aufzeichnungen und Unterlagen in elektronischer Form sowie zum
     Datenzugriff (GoBD), BMF-Schreiben vom 28.11.2019, BStBl I 2019, 1269,
     zuletzt geändert durch BMF-Schreiben vom 14.07.2025 (Fassung und
     Änderungsstand für [JAHR] verifizieren)
   - Verfahrensdokumentation zum Kassensystem, Programmier- und
     Stammdatenänderungsprotokolle, Bedienerkennungen, Abgrenzung des
     Trainingsmodus vom Echtbetrieb
   Formuliere jede Anforderung als nachweisbaren Zustand mit der Frage
   "woran erkennen wir das?".
4. Prüfraster für das Angebot: Nur ausgeben, wenn im Feld "Angebot des
   Dienstleisters liegt vor" ein "ja" steht. Gleiche das Angebot Position für
   Position gegen den Anforderungskatalog ab und ordne jede Muss-Anforderung
   ein in: ausdrücklich zugesagt / erwähnt, aber ohne Zusage / nicht erwähnt /
   ausdrücklich ausgeschlossen. Behandle Werbeaussagen wie "GoBD-konform",
   "finanzamtssicher" oder "zertifiziert" NICHT als Zusage; verlange die
   konkrete Angabe, worauf sich die Aussage bezieht. Steht "nein", gib
   stattdessen aus, welche Punkte im einzuholenden Angebot ausdrücklich
   geregelt sein müssen.
5. Fragenliste an den Dienstleister: höchstens 15 Fragen, jede so gestellt,
   dass sie mit einem Dokument oder einer schriftlichen Zusage beantwortet
   werden kann, nicht mit "ja". Nimm auf: Laufzeit und Verlängerung des
   Zertifikats der Sicherheitseinrichtung, Verfahren bei ihrem Ausfall,
   Erzeugung und Prüfung des Kassendatenexports, Umgang mit Stornos und
   Trainingsbuchungen, Bedienerverwaltung, Aufbewahrung und Zugriff auf die
   Daten NACH Vertragsende – bei Miete, Leasing und Cloud-Abonnement
   ausdrücklich –, Lieferung der Verfahrensdokumentation, Meldung von
   Programmänderungen.
6. Mitteilung nach § 146a Abs. 4 AO als Teil der Abnahme: Die Anschaffung
   löst eine Mitteilung aus; gemietete und geleaste Systeme stehen
   angeschafften gleich (AEAO zu § 146a Nr. 1.16.2.6 – für [JAHR] verifizieren).
   Bei jeder Mitteilung sind stets alle Systeme der betroffenen Betriebsstätte
   zu übermitteln (AEAO zu § 146a Nr. 1.16.1.4 – für [JAHR] verifizieren) –
   die Einführung eines einzelnen Systems erfordert deshalb den vollständigen
   Bestand der Betriebsstätte. Erhebe die dafür nötigen Angaben hier NICHT und
   entwirf keinen Datensatz, sondern nimm eine Position in das Abnahme-
   protokoll auf, die auf die Bestandsaufnahme des Meldebestands verweist
   (Prompt 106). Steht im Feld "Bisheriges System wird abgelöst" ein "ja" und
   war das bisherige System ein elektronisches Aufzeichnungssystem, sind es
   ZWEI Vorgänge: Außerbetriebnahme des alten und Anschaffung des neuen
   Systems. Nimm dann zusätzlich eine Position auf, dass die Daten des
   Altsystems über die Aufbewahrungsfrist verfügbar und lesbar bleiben müssen
   (§ 146 Abs. 5 Satz 2 AO, § 147 Abs. 2 Nr. 2 AO – für [JAHR] verifizieren).
7. Verantwortung: Stelle ausdrücklich fest, dass die Verantwortung für die
   Ordnungsmäßigkeit der Aufzeichnungen beim Steuerpflichtigen bleibt
   (§§ 145 bis 147 AO – für [JAHR] verifizieren) und dass Zusicherungen des
   Dienstleisters daran nichts ändern. Ob und wie der Dienstleister dem
   Mandanten zivilrechtlich haftet, beurteilst du NICHT; verweise diese Frage
   an den Berufsträger und, soweit sie über die steuerliche Beratung
   hinausgeht, an anwaltliche Beratung.
8. Fristen: Berechne KEINE Fristen und nenne keine Datumsangaben. Liste
   stattdessen auf, welche Fristen im Raum stehen, jeweils mit Rechtsgrundlage
   und dem Zusatz "für [JAHR] verifizieren": Mitteilung nach § 146a Abs. 4
   Satz 2 AO, Aufbewahrungsfristen nach § 147 Abs. 3 Satz 1 AO. Ergänze bei
   jeder: "Fristen berechnet und erfasst ein Mensch."
   Ordne die offenen Punkte danach, was vor dem im Feld "Geplanter Termin für
   den Echtbetrieb" genannten Zeitpunkt vorliegen muss, und gib dabei kein
   Datum und keine Dauer an.

ANFORDERUNGEN
- Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
  Satz, Verordnung, Verwaltungsanweisung mit Datum), jeweils mit dem Zusatz
  "für [JAHR] verifizieren", und führe sie am Ende in der Tabelle
  "Zu verifizierende Rechtsgrundlagen" auf. Erfinde keine Paragrafen,
  BMF-Schreiben oder Dokumentnummern; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren" statt einer Angabe.
- Markiere ALLE Fristen, Stichtage und Betragsgrenzen als
  "für [JAHR] verifizieren". Lieber keinen Wert als einen unmarkierten.
- Formuliere jede Aussage über die Leistungsfähigkeit eines Systems oder über
  die übliche Praxis von Kassendienstleistern als Vermutung und kennzeichne
  sie als solche. Nenne keine Produkte und keine Hersteller.
- Erkläre jeden Fachbegriff in einem Halbsatz in Klammern.

AUSGABEFORMAT
1. (Einschätzung der Eindeutigkeit)
2. (Vorfrage und Verantwortungsabgrenzung) – Ergebnis der Schritte 2 und 7:
   ob nach den Angaben überhaupt ein elektronisches Aufzeichnungssystem
   gebraucht wird (offen stellen, nicht entscheiden), und die Feststellung,
   dass die Verantwortung für die Ordnungsmäßigkeit der Aufzeichnungen beim
   Steuerpflichtigen bleibt (§§ 145 bis 147 AO – für [JAHR] verifizieren)
3. (Anforderungskatalog) – Tabelle:
   Nr. | Anforderung | Muss oder Soll | Rechtsgrundlage bei Muss |
   woran wir die Erfüllung erkennen | erfüllt (leer)
4. (Angebotsprüfung) – nur bei vorliegendem Angebot, Tabelle:
   Nr. | Muss-Anforderung | Fundstelle im Angebot | Einordnung |
   Nachfrage erforderlich (ja/nein)
5. (Fragenliste an den Dienstleister) – nummeriert, höchstens 15 Fragen,
   je Frage die erwartete Form der Antwort (Dokument, schriftliche Zusage)
6. (Rollenmatrix) – Tabelle:
   Aufgabe | verantwortlich (Mandant / Kanzlei / Dienstleister / offen) |
   wirkt mit
   Je Zeile genau ein Eintrag in der Spalte "verantwortlich"; weitere
   Beteiligte in der Spalte "wirkt mit" benennen. Keine Zeile bleibt ohne
   Eintrag. "Offen" ist ein Ergebnis und wird zusätzlich in Abschnitt 8
   aufgenommen.
7. (Abnahmeprotokoll) – abhakbar, Kästchen ☐ vor jeder Position:
   ☐ | Punkt | Nachweis (Dokument, Testexport, Protokoll) | geprüft von |
   Datum (leer)
   Beginne mit dem Satz, dass die Kanzlei die steuerlichen Anforderungen
   prüft und keine technische Systemabnahme erklärt. Nimm in jedem Fall auf:
   ☐ Testexport der Kassendaten erzeugt und lesbar eingelesen
   ☐ Verfahrensdokumentation zum Kassensystem übergeben
   ☐ Meldebestand der Betriebsstätte aufgenommen, Mitteilung nach
     § 146a Abs. 4 AO vorbereitet (siehe Prompt 106)
8. (Vor dem Echtbetrieb zu klären) – offene Punkte aus Rollenmatrix und
   Angebotsprüfung, mit Verantwortlichem und Reihenfolge, ohne Datumsangaben
9. (Interne Notiz) – nicht an den Mandanten: Risiken, die der Berufsträger
   entscheiden muss, und was in die Handakte gehört
10. (Was ich nicht sicher weiß)
11. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. **Vorschaltfrage durch den Berufsträger, vor dem Werkzeugeinsatz:** Steht im Raum, dass die bisherigen Kassenaufzeichnungen unrichtig sind, ist eine Berichtigung nach § 153 AO oder eine Selbstanzeige im Gespräch oder läuft ein Steuerstraf- oder Bußgeldverfahren? Dann gehört der Sachverhalt nach `DATENSCHUTZ.md` (Zone Rot) nicht in ein KI-Werkzeug; die Antwort wird in der Handakte vermerkt, nicht im Prompt.
2. Den Prompt einsetzen, **bevor** der Mandant unterschreibt. Nach der Installation ist der Anforderungskatalog eine Mängelliste, und Nachbesserungen kosten Geld, das im Angebot nicht vorgesehen war.
3. Anforderungskatalog und Fragenliste ungekürzt an den Mandanten geben, damit er sie an den Dienstleister weiterreicht. Antworten schriftlich einfordern; mündliche Zusagen eines Vertriebsmitarbeiters helfen in der Kassen-Nachschau nicht.
4. Rollenmatrix mit Mandant und Dienstleister gemeinsam durchgehen und jede Zeile besetzen. Die Zeilen, die am Ende bei "offen" stehen, sind der eigentliche Ertrag des Prompts.
5. Abnahmeprotokoll erst abzeichnen, wenn ein Testexport der Kassendaten tatsächlich erzeugt und eingelesen wurde. Ein Export, der erst in der Nachschau erstmals erzeugt wird, funktioniert erfahrungsgemäß nicht.
6. Bei Miete, Leasing und Cloud-Abonnement schriftlich klären, wie der Mandant nach Vertragsende an seine Daten kommt – die Aufbewahrungsfrist läuft weiter, der Vertrag nicht.
7. Nach dem Echtbetrieb: Meldebestand mit Prompt 106 aufnehmen und Mitteilung veranlassen, laufende Kassenführung mit Prompt 38 aufsetzen.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Anforderungskatalog, Fragenliste und Abnahmeprotokoll werden vor der Weitergabe an Mandant oder Dienstleister von einem Berufsträger freigegeben (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Keine Pflicht behaupten, die es nicht gibt.** Enthält der Entwurf eine Aussage über eine bestehende oder künftige Verpflichtung, ein elektronisches Aufzeichnungssystem einzusetzen, ist sie zu streichen oder ausdrücklich als Entwurfsstand zu kennzeichnen; ein Referentenentwurf ist kein geltendes Recht.
- **Keine technische Abnahme durch die Kanzlei.** Prüfen, ob das Abnahmeprotokoll ausschließlich steuerliche Anforderungen enthält. Sätze, die eine Funktionsfähigkeit des Systems bestätigen, gehören nicht in ein Kanzleidokument.
- **Rollenabgrenzung kontrollieren:** Die Verantwortung für die Ordnungsmäßigkeit der Aufzeichnungen bleibt beim Steuerpflichtigen (§§ 145 bis 147 AO – für [JAHR] verifizieren). Formulierungen, nach denen der Dienstleister die Prüfungsfestigkeit schuldet, werden nicht ungeprüft übernommen; die zivilrechtliche Haftung ist hier nicht beurteilt.
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum aus der KI-Antwort übernehmen; die Mitteilungsfrist nach § 146a Abs. 4 Satz 2 AO wird im Fristenprogramm erfasst und von einer zweiten Person nachgeprüft.
- **Rechtsstand prüfen an:** § 146a AO, § 146b AO, §§ 145 bis 147 AO, KassenSichV, Anwendungserlass zur AO zu § 146a, GoBD in der Fassung vom 14.07.2025 sowie am FAQ-Katalog des BMF zur Ordnungsmäßigkeit der Kassenführung (jeweils Fassung für [JAHR] verifizieren).
- Aufbewahrungsfristen nicht pauschal angeben: Buchungsbelege und übrige Unterlagen unterliegen unterschiedlichen Fristen (§ 147 Abs. 3 Satz 1 AO – für [JAHR] verifizieren).
- Prüfen, ob der Anforderungskatalog Pflichten enthält, die das angebotene System technisch nicht erfüllen kann. Dann ist vor der Beschaffung die Systemfrage zu klären, nicht nach der Installation.

## Varianten

- **Mehrere Standorte:** "Ergänze je Standort eine eigene Zeile in der Rollenmatrix und einen Punkt im Abnahmeprotokoll zur Zusammenführung der Kassendaten aus mehreren Systemen."
- **Systemwechsel:** "Ergänze einen Abschnitt zur Stilllegung des Altsystems: Verfügbarkeit und Lesbarkeit der Altdaten über die Aufbewahrungsfrist, Export vor der Abschaltung, Aufbewahrung der Verfahrensdokumentation des Altsystems."
- **Cloud-Kasse:** "Ergänze Fragen zum Speicherort, zum Auftragsverarbeitungsvertrag des Mandanten mit dem Dienstleister und zum Datenzugriff nach Vertragsende."
- **Nach der Einführung:** "Erzeuge aus dem Abnahmeprotokoll eine Mängelliste: Punkt | offen seit | wer | vereinbarte Erledigung | Auswirkung auf die Ordnungsmäßigkeit."
- **Einweisung:** "Erzeuge eine Einweisung für das Kassenpersonal, höchstens 300 Wörter, mit den fünf Bedienfehlern, die den Kassendatenexport unbrauchbar machen."
