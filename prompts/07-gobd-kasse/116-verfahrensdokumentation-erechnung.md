# 116 – Verfahrensdokumentation und Kontrollmatrix für den E-Rechnungsprozess

**Problem:** Seit der Umstellung auf die E-Rechnung ist der aufbewahrungspflichtige Gegenstand nicht mehr das Bild der Rechnung, sondern der strukturierte Datensatz – Eingang, Prüfung, Freigabe, Verbuchung und Archivierung laufen über mehrere Systeme, und niemand hat beschrieben, wer an welcher Stelle was kontrolliert.
**Rolle:** Steuerberater, Kanzleileitung, Digitalisierungsbeauftragte, Sachbearbeitung Finanzbuchführung
**DATEV-Bezug:** DATEV Unternehmen online (Belegeingang, Belegtransfer, Belegweg), DATEV Kanzlei-Rechnungswesen (Buchung, Belegverknüpfung, Datenprüfung / Datenzugriff Z1–Z3), DATEV DMS (Ablage der Verfahrensdokumentation und der Kontrollnachweise); Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Eine Beschreibung des Ablaufs, wie er heute tatsächlich stattfindet – Eingangskanäle und Formate, Belegzahl im Monat, eingesetzte Systeme je Prozessschritt und deren Schnittstellen, wer prüft und wer freigibt, was archiviert wird (strukturierter Datensatz oder Bildansicht), ob gegen die Norm validiert wird, Umgang mit hybriden Formaten und mit Rechnungen im nicht vereinbarten Format, Regelungen zu Unveränderbarkeit, Wiederauffindbarkeit, Datensicherung, Notfall- und Ausfallregelung, Zugriffsschutz und Löschung nach Fristablauf; bei eigenen E-Rechnungen zusätzlich Erstellungssystem, Format und Archivweg des Ausgangsdatensatzes.
**Datensparsamkeit:** Nur Rollenbezeichnungen (`Buchhaltung 1`, `Geschäftsführung`, `Einkauf 1`), keine Klarnamen. Netzwerkpfade, Serveradressen, Postfachadressen, Zugangsdaten, Zertifikate und EDI-Schlüssel gehören nicht in den Prompt; Ablageorte abstrakt beschreiben (`Server im Haus`, `Cloudspeicher`, `Archivsystem des Herstellers`). Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Einzelne Rechnungsdaten werden nicht gebraucht – der Prompt beschreibt den Prozess, nicht den Beleg. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug für ein konkretes Mandat und nicht nur als allgemeine Kanzlei-IT eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und erstellst
Verfahrensdokumentationen nach den GoBD. Du dokumentierst ausschließlich den
Ablauf, der tatsächlich gelebt wird. Was nur geplant, gewünscht oder üblich
ist, gehört in die Lückenliste, nicht in die Dokumentation.

AUFGABE
Erstelle für den Umgang mit elektronischen Rechnungen die Prozessbeschreibung
und die Kontrollmatrix. Aufbewahrungspflichtiger Gegenstand ist der
STRUKTURIERTE DATENSATZ, nicht seine Bildansicht. Der Prozess umfasst Empfang,
Validierung, Zuordnung, Freigabe, Verbuchung, Archivierung und
Wiederauffindbarkeit.

ABGRENZUNG – hier NICHT behandeln, sondern auf den genannten Prompt verweisen
- Ersetzendes Scannen von Papierbelegen, Scanrichtlinie, Vernichtung von
  Papieroriginalen: Prompt 37.
- Ab welchem Stichtag dieser Mandant selbst E-Rechnungen ausstellen muss:
  Prompt 85.
- Einordnung und Behandlung einzelner fehlerhafter Rechnungen: Prompt 86.

UNTERNEHMENSRAHMEN
- Branche, Rechtsform, Größe: [ANGABE]
- Gewinnermittlung: [Bilanz / EÜR], Kontenrahmen: [SKR03 / SKR04]
- Ausstellung eigener E-Rechnungen: [nein / ja]
- Papierbelege oder Papierrechnungen daneben im Umlauf: [nein / ja]

STAND UND GELTUNG
- Stand der Dokumentation (Tag der Erstellung): [DATUM]
- Der beschriebene Ablauf wird tatsächlich so gelebt seit: [DATUM]
- Die Dokumentation trägt als Stand den Tag der Erstellung: [ja / nein]

EINGANGSKANÄLE UND VOLUMEN
- Kanäle: [z. B. zentrales Postfach, Lieferantenportal, EDI-Verbindung, Upload
  durch den Lieferanten, Papierpost]
- Belege im Monat je Kanal: [ANZAHL]
- Formate im Eingang: [z. B. normkonformes Format, hybrides Format,
  EDI-Format, PDF ohne strukturierte Daten, Papier]
- Zugriff auf das Eingangspostfach haben: [ROLLEN]

SYSTEME JE PROZESSSCHRITT
- Empfang: [SYSTEM] – Validierung: [SYSTEM / keine Validierung]
- Zuordnung und sachliche Prüfung: [SYSTEM] – Freigabe: [SYSTEM]
- Verbuchung: [SYSTEM] – Archivierung: [SYSTEM]
- Versionsstand der genannten Systeme: [ANGABE / nicht bekannt]
- Übergaben und Schnittstellen zwischen diesen Systemen: [ANGABE]
- Nur wenn eigene E-Rechnungen ausgestellt werden: Erstellung [SYSTEM],
  erstellende Rolle [ROLLE], Format [ANGABE], Archivierung des
  Ausgangsdatensatzes [SYSTEM]

MENSCHEN UND KONTROLLEN
- Sachliche Prüfung durch: [ROLLE]
- Freigabe durch: [ROLLE], Wertgrenzen: [ANGABE]
- Vertretung geregelt: [nein / ja]
- Freigabe und Zahlungsauslösung in getrennten Händen: [nein / ja]

BEHANDLUNG DES DATENSATZES
- Aufbewahrt wird: [nur strukturierter Datensatz / nur Bildansicht / beides]
- Validierung gegen die Norm: [nein / ja], womit: [ANGABE]
- Verhalten bei fehlgeschlagener Validierung: [ANGABE]
- Hybride Formate, führender Bestandteil: [strukturierter Teil / Bildteil /
  nicht geregelt]
- Umgang mit Rechnungen im nicht vereinbarten oder nicht zulässigen Format:
  [ANGABE]
- Ergänzungen zum Beleg (Kontierung, Prüf- und Freigabevermerk) werden
  festgehalten in: [ANGABE]
- Unveränderbarkeit gesichert durch: [ANGABE]
- Wiederauffindbarkeit: Suchkriterien [ANGABE], Verknüpfung zwischen Datensatz
  und Buchung: [ANGABE]
- Datensicherung und Wiederherstellung: [ANGABE]
- Notfall- und Ausfallregelung: [ANGABE / nicht geregelt]
- Zugriffsschutz und Berechtigungskonzept: [ANGABE / nicht geregelt]
- Löschung nach Fristablauf, wer entscheidet: [ANGABE / nicht geregelt]
- Bereitstellung der Daten für den Datenzugriff des Finanzamts durch: [ROLLE],
  aus: [SYSTEM]

BEKANNTE LÜCKEN
[WAS DER MANDANT SELBST ALS UNGEREGELT BEZEICHNET ODER NICHT BEANTWORTEN KONNTE]

ABBRUCH- UND AUSSTEUERUNGSREGELN – an objektiven Angaben, nicht an Bewertungen
1. ABBRUCHREGEL: Steht im Feld "Die Dokumentation trägt als Stand den Tag der
   Erstellung" ein "nein", arbeite NICHT weiter. Gib nur aus:
   "Abbruchgrund liegt vor (Stand weicht vom Tag der Erstellung ab) –
   Bearbeitung an dieser Stelle abgebrochen, Entscheidung durch einen
   Berufsträger außerhalb des KI-Werkzeugs."
2. AUSSTEUERUNGSREGEL – kein Abbruch: Steht im Feld "Papierbelege oder
   Papierrechnungen daneben im Umlauf" ein "ja", gib für Scanvorgang,
   Scanrichtlinie und Vernichtung der Papieroriginale nur aus: "Ausgesteuert –
   ersetzendes Scannen nach Prompt 37, hier nicht beschrieben." Nimm die
   Papierbelege gleichwohl in die Aufbewahrungsübersicht und mit einer eigenen
   Zeile in die Kontrollmatrix auf und weise in der Lückenliste aus, dass
   beide Dokumentationen aufeinander abzustimmen sind. Arbeite alle übrigen
   Schritte weiter.

ARBEITSWEISE
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: Reicht die Beschreibung
   für einen belastbaren Entwurf, oder fehlen tragende Angaben?
2. Schreibe NUR auf, was in den Angaben steht. Ergänze keine Kontrolle, keine
   Freigabestufe und kein Protokoll, das nicht genannt ist. Fehlt ein üblicher
   Baustein, gehört er in die Lückenliste, NICHT in den Entwurf.
3. Markiere jede Stelle, an der du interpretiert hast, mit (Annahme).
4. Arbeite jeden Prozessschritt nach demselben Raster ab: was geschieht |
   welches System | wer (Rolle) | welche Kontrolle | welcher Nachweis der
   Durchführung | welches Risiko bei Ausfall dieses Schritts. Prozessschritte:
   Empfang, Validierung, Zuordnung und sachliche Prüfung, Freigabe, Verbuchung,
   Archivierung, Wiederauffindbarkeit und Datenzugriff; zusätzlich Ausstellung
   und Archivierung eigener E-Rechnungen, wenn das entsprechende Feld "ja" sagt.
   Ziehe die Belegzahl je Kanal in die Einschätzung des Ausfallrisikos ein.
5. Beschreibe im Schritt Validierung ausdrücklich, was mit einer Rechnung
   geschieht, die im nicht vereinbarten oder nicht zulässigen Format eingeht,
   und wer entscheidet, ob eine berichtigte Rechnung angefordert wird
   (Einordnung des Einzelfalls: Prompt 86).
6. Präsens, Wir-Form des Mandanten.

ANFORDERUNGEN
1. Kennzeichne jede Aussage, bei der du dir nicht sicher bist. Rate nicht.
2. Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz, Verwaltungsanweisung mit Datum), jeweils mit dem Zusatz
   "für [JAHR] verifizieren", und führe sie am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" auf. Erfinde keine Paragrafen,
   BMF-Schreiben oder Dokumentnummern; bist du dir nicht sicher, schreibe "Fundstelle offen –
   bitte recherchieren". Mindestens zu nennen, soweit im Fall berührt:
   - § 14 Abs. 1 Satz 3 UStG (elektronische Rechnung), Satz 4 (sonstige
     Rechnung), Satz 6 (Format).
   - Die europäische Normenreihe EN 16931 steht NICHT im Gesetz. Belege den
     Bezug auf die Norm mit UStAE Abschnitt 14.1 Abs. 11 Satz 1 Nr. 1 und
     nicht mit § 14 UStG.
   - § 14 Abs. 2 Satz 2 Nr. 1 Halbsatz 2 und Satz 3 UStG sowie § 27 Abs. 38
     UStG für die Frage, welche Belege bereits pflichtig sind. Die
     Umsatzgrenze steht in § 27 Abs. 38 Satz 1 Nr. 2 UStG, nicht in Nr. 3;
     Nr. 3 (elektronischer Datenaustausch) gilt ohne Umsatzgrenze. Nenne
     keinen Betrag und keinen Stichtag ohne den Zusatz
     "für [JAHR] verifizieren"; die Einordnung des Mandanten leistet
     Prompt 85.
   - § 145 Abs. 1 AO: Die Buchführung muss einem sachverständigen Dritten
     innerhalb angemessener Zeit einen Überblick ermöglichen. Das ist der
     Maßstab für die Verfahrensdokumentation selbst – schreibe sie so, dass
     ein Dritter den Weg eines Belegs ohne Rückfragen nachvollziehen kann.
   - § 146 Abs. 4 AO (Unveränderbarkeit) und § 146 Abs. 5 Satz 2 AO: Die Daten
     müssen während der Aufbewahrungsfrist jederzeit verfügbar und
     unverzüglich lesbar sein. Das ist der Kern des Archivierungskapitels.
   - § 147 Abs. 1 Nr. 2 und Nr. 4 AO (Kategorien), § 147 Abs. 3 Satz 1 AO
     (Dauer), § 147 Abs. 4 AO (Fristbeginn), § 147 Abs. 6 AO (Datenzugriff).
   - § 14b Abs. 1 UStG für die Aufbewahrung der empfangenen Rechnungen und der
     Doppel der selbst ausgestellten Rechnungen; Satz 2 verlangt, dass die
     Rechnungen für den gesamten Zeitraum die Anforderungen des § 14 Abs. 3
     Satz 1 UStG erfüllen, Satz 3 regelt den Fristbeginn und stellt klar, dass
     § 147 Abs. 3 AO unberührt bleibt.
     Dauer und Anwendungsbereich – für [JAHR] verifizieren.
   - § 15 Abs. 1 Satz 1 Nr. 1 UStG für die Verknüpfung von Rechnungsprüfung
     und Vorsteuerabzug.
   - GoBD: BMF-Schreiben vom 28.11.2019, BStBl I 2019, 1269, geändert durch
     BMF-Schreiben vom 11.03.2024, BStBl I 2024, 374, und durch BMF-Schreiben
     vom 14.07.2025, GZ IV D 2 - S 0316/00128/005/088, BStBl I 2025, 1502,
     anzuwenden mit Wirkung vom 14.07.2025. Nenne das Schreiben, aber ZITIERE
     KEINE EINZELNE RANDZIFFER – Randziffern gelten hier als nicht belegt.
3. Aufbewahrung: Ordne jeder Belegart die Kategorie des § 147 Abs. 1 AO zu und
   daraus die Dauer nach § 147 Abs. 3 Satz 1 AO – zehn Jahre für Nr. 1 und
   Nr. 4a, ACHT Jahre für Buchungsbelege (Nr. 4), sechs Jahre für die übrigen
   Unterlagen. Behaupte für Buchungsbelege NIE zehn Jahre. Ist ein Beleg
   zugleich Buchungsbeleg (Nr. 4) und empfangener Geschäftsbrief (Nr. 2), gib
   beide Zuordnungen aus und kennzeichne die maßgebliche Dauer als von der
   Kanzlei zu entscheiden. Jede Dauerangabe trägt den Zusatz "Dauer und
   Anwendungsbereich – für [JAHR] verifizieren".
4. Berechne KEINE Fristen und kein Ablaufdatum. Nenne den Fristbeginn nur
   abstrakt nach § 147 Abs. 4 AO (Schluss des Kalenderjahres, in dem das
   maßgebliche Ereignis liegt) und ergänze: "Fristen berechnet und erfasst ein
   Mensch."
5. Der Entwurf muss ohne die Lückenliste unvollständig WIRKEN. Schreibe keine
   Lücke schön und formuliere keine Kontrolle als vorhanden, für die kein
   Nachweis genannt ist.

AUSGABEFORMAT
1. (Einschätzung der Eindeutigkeit)
2. (Prozessbeschreibung) in vier Abschnitten:
   A ALLGEMEINE BESCHREIBUNG – Zweck, Unternehmensrahmen mit Gewinnermittlung
     und Kontenrahmen, Geltungsbereich und Geltungsbeginn, erfasste Belegarten
     und Formate, Rollen, Stand, Version.
   B ANWENDERDOKUMENTATION – der Ablauf aus Sicht der Beschäftigten, Schritt
     für Schritt, einschließlich Fehlerfällen, Nachzüglern und Vertretung.
   C TECHNISCHE SYSTEMDOKUMENTATION – Systeme mit Versionsständen,
     Schnittstellen und Datenflüsse, Speicherorte, Berechtigungskonzept,
     Behandlung des strukturierten Datensatzes und der Bildansicht, Umgang mit
     hybriden Formaten, Ort der Ergänzungen zum Beleg (Kontierung, Prüf- und
     Freigabevermerk), Unveränderbarkeit, Protokollierung.
   D BETRIEBSDOKUMENTATION – Datensicherung und Wiederherstellung, Notfall-
     und Ausfallregelung, Lesbarmachung, Zugriffsschutz, Bereitstellung für
     den Datenzugriff, Löschung nach Fristablauf.
3. (Kontrollmatrix) – Tabelle, eine Zeile je Prozessschritt, bei mehreren
   Kontrollen je Schritt mehrere Zeilen:
   Prozessschritt | Risiko | Kontrolle | präventiv oder detektiv |
   Verantwortlicher (Rolle) | Nachweis der Durchführung
   Nimm in jedem Fall eine Zeile auf, die zeigt, an welcher Stelle die
   Voraussetzungen des Vorsteuerabzugs geprüft werden (§ 15 Abs. 1 Satz 1
   Nr. 1 UStG – für [JAHR] verifizieren), eine Zeile für die Kontrolle, dass
   der strukturierte Datensatz und nicht nur die Bildansicht ins Archiv
   gelangt, und eine Zeile zur Trennung von Freigabe und Zahlungsauslösung.
   Ist eine dieser Kontrollen nach den Angaben nicht eingerichtet, schreibe
   "nicht eingerichtet" in die Spalte Kontrolle und nimm sie in die
   Lückenliste auf.
4. (Aufbewahrungsübersicht) – Tabelle:
   Belegart | Kategorie nach § 147 Abs. 1 AO | Dauer nach § 147 Abs. 3 Satz 1
   AO | Fristbeginn nach § 147 Abs. 4 AO | Aufbewahrung nach § 14b Abs. 1 UStG
   (ja/nein) | aufbewahrender Ort | Verantwortlicher
5. (Lückenliste) – Tabelle:
   Nr. | Lücke | Risiko | wer klärt | Antwort des Mandanten (leer)
6. (Änderungshistorie) – Vorlage als leere Tabelle: Version | Datum | geänderter
   Abschnitt | Grund der Änderung | erstellt von | freigegeben von
7. (Interne Notiz) – was die Kanzlei vor der Freigabe prüfen muss und was ohne
   Besichtigung des Ablaufs vor Ort offenbleibt.
8. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. **Vorschaltfrage durch den Berufsträger, vor dem Werkzeugeinsatz und außerhalb des Werkzeugs:** Soll die Dokumentation einen Zeitraum abdecken, in dem der beschriebene Ablauf noch nicht gelebt wurde, oder gibt es Anhaltspunkte für eine Berichtigungspflicht nach § 153 AO, eine Selbstanzeige oder ein Steuerstrafverfahren? Wenn ja, wird dieser Prompt nicht eingesetzt; die Antwort wird in der Handakte vermerkt (Zone Rot in `DATENSCHUTZ.md`). Die Frage wird nicht im Werkzeug gestellt.
2. Die Ablaufbeschreibung von den Personen erheben lassen, die den Beleg tatsächlich anfassen – Rechnungseingang, Einkauf, Buchhaltung, IT. Eine Beschreibung, die allein aus der Kanzlei stammt, erzeugt genau den Wunschprozess, den der Prompt vermeiden soll.
3. Vor dem Lauf klären, welcher Bestandteil bei hybriden Formaten heute tatsächlich gebucht und archiviert wird. Antwortet niemand darauf, ist das die erste Lücke – nicht eine Annahme.
4. Entwurf, Kontrollmatrix und Lückenliste getrennt übergeben; die Lückenliste ist der Arbeitsauftrag an den Mandanten. Nach Rücklauf den Prompt mit ergänzter Beschreibung erneut laufen lassen, statt den Text von Hand zu flicken.
5. Kontrollmatrix mit den benannten Verantwortlichen durchsprechen und je Kontrolle festhalten, wo der Nachweis der Durchführung liegt. Eine Kontrolle ohne Nachweis ist in der Prüfung keine.
6. Stand, Version und Verantwortliche eintragen und bei jeder System- oder Prozessänderung fortschreiben.
7. Läuft neben dem elektronischen Beleglauf weiter Papier, gehören beide Dokumentationen zusammen: Dieser Prompt beschreibt den E-Rechnungsprozess, Prompt 37 den Scan- und Papierweg. Vor der Freigabe prüfen, dass keine Belegart in beiden Dokumenten fehlt.

## Qualitätssicherung

- **Die Verfahrensdokumentation beschreibt den tatsächlichen, nicht den gewünschten Prozess.** Eine Dokumentation, die vom gelebten Ablauf abweicht, ist schlechter als keine: Sie ist in der Prüfung widerlegbar und liefert die Abweichung gleich mit. Vor der Freigabe eine Stichprobe von Rechnungen durch den beschriebenen Ablauf zurückverfolgen – vom Eingangskanal über Validierung, Freigabe und Buchung bis ins Archiv. Weicht die Praxis ab, wird der Entwurf geändert, nicht die Praxis auf dem Papier.
- **Keine Rückdatierung.** Der Stand ist der Tag der Erstellung. Wer eine Dokumentation mit älterem Stand versieht, um eine Lücke zu schließen, schafft ein neues Problem; die Entscheidung darüber trifft ausschließlich ein Berufsträger.
- **Archivierungstest statt Zusage:** Aus dem Archiv einen strukturierten Datensatz zurückholen, ihn lesbar machen und mit der Buchung verknüpfen. Erst das belegt, was § 146 Abs. 5 Satz 2 AO verlangt – jederzeit verfügbar und unverzüglich lesbar (für [JAHR] verifizieren).
- **Umsatzsteuerliche Aufbewahrung nicht vergessen.** Neben § 147 AO gilt für Rechnungen und Rechnungsdoppel § 14b Abs. 1 UStG; die Anforderungen des § 14 Abs. 3 Satz 1 UStG müssen über den gesamten Zeitraum erfüllt bleiben. Dauer und Fassung im amtlichen Volltext nachlesen (für [JAHR] verifizieren).
- **Aufbewahrungsdauern selbst nachschlagen.** Für Buchungsbelege gilt nach § 147 Abs. 3 Satz 1 AO nicht dieselbe Dauer wie für Jahresabschlüsse; die Verkürzung durch das Vierte Bürokratieentlastungsgesetz betrifft nicht alle Unterlagen gleichermaßen, und für einzelne Branchen gelten abweichende Regelungen (für [JAHR] verifizieren).
- **GoBD-Fassung prüfen:** BMF vom 28.11.2019, zuletzt geändert durch BMF vom 14.07.2025 (Fassung und Änderungsstand für [JAHR] verifizieren). Aussagen, die das Modell einer Randziffer zuschreibt, werden gestrichen – Randziffern sind in diesem Projekt nicht belegt.
- **Fristen berechnet und erfasst ein Mensch.** Aus dieser Dokumentation folgt kein Vernichtungsdatum; die Freigabe zur Vernichtung erteilt ein Berufsträger.
- **Vier-Augen-Prinzip:** Prozessbeschreibung und Kontrollmatrix werden von einer zweiten Person gegen die Ablaufbeschreibung gelesen und von einem Berufsträger freigegeben (Freigabestufe 3 in `DATENSCHUTZ.md`) – der Entwurf kann in der Prüfung gegen den Mandanten verwendet werden. Klären, wer beim Mandanten die Dokumentation verantwortet und unterschreibt: Sie ist eine Erklärung des Mandanten, nicht der Kanzlei.

## Varianten

- **Nur Kontrollmatrix:** "Erzeuge ausschließlich die Kontrollmatrix, ergänzt um eine Spalte 'Häufigkeit der Kontrolle', als Arbeitsgrundlage für das interne Kontrollsystem."
- **Kleiner Betrieb:** "Erzeuge eine Kurzfassung für einen Betrieb mit unter fünf Beschäftigten, in dem eine Person empfängt, prüft, freigibt und bucht – benenne die dadurch entfallende Funktionstrennung ausdrücklich als Risiko und schlage kompensierende Kontrollen vor."
- **Fortschreibung:** "Vergleiche die vorliegende Fassung mit der neuen Ablaufbeschreibung und gib nur die zu ändernden Abschnitte und die betroffenen Zeilen der Kontrollmatrix aus."
- **Vorbereitung auf die Betriebsprüfung:** "Erzeuge aus der Kontrollmatrix eine Liste der Nachweise, die bei einem Datenzugriff nach § 147 Abs. 6 AO kurzfristig vorzulegen sind (für [JAHR] verifizieren) – siehe auch Prompt 34."
