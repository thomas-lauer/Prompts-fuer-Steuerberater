# 102 – Elektronische Bekanntgabe nach § 122a AO: Umstellung und Fristenkontrolle

**Problem:** Bescheide dürfen zum Datenabruf bereitgestellt werden, und die Bekanntgabe gilt nach Ablauf der gesetzlichen Frist als bewirkt – auch wenn niemand abgerufen hat; Urlaub, Krankheit oder ein nicht überwachtes Postfach lassen die Einspruchsfrist damit lautlos ablaufen, und bei einem Teil der Bestandsvollmachten wurde die Bekanntgabeart mit der Umstellung der Vollmachtsdatenbank zurückgesetzt.
**Rolle:** Kanzleileitung, Berufsträger, Fristenverantwortliche, Sekretariat, Sachbearbeitung
**DATEV-Bezug:** DATEV Vollmachtsdatenbank (§ 80a AO, Bekanntgabeart je Vollmacht), DATEV Bescheiddatenrückübermittlung und Abruf bereitgestellter Bescheiddaten, DATEV Fristenkontrolle sowie DATEV Fristen und Bescheide, DATEV Arbeitsplatz und Eigenorganisation (Posteingang, Wiedervorlage, Vertretung), DATEV DMS (Ablage der Bereitstellungs- und Abrufprotokolle)
**Was du bereitstellen musst:** Mengengerüst je Fallgruppe – Anzahl der Mandate nach hinterlegter Bekanntgabeart und Vollmachtsart, ohne Namen, ohne Steuernummern und ohne Auszug aus der Vollmachtsdatenbank; heutige Praxis des Bescheidabrufs und der Fristerfassung, eingesetzte Programme, Zuständigkeiten und Vertretungsregelung, Urlaubs- und Schließzeiten der Kanzlei, bereits bekannte Auffälligkeiten nach der Umstellung der Vollmachtsdatenbank.
**Datensparsamkeit:** Keine Mandantendaten einfügen. Mandate nur als Fallgruppen oder als `Mandat A`, Mitarbeitende nur als Rollen (`Sekretariat`, `Sachbearbeitung 1`, `Berufsträger A`). Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Vollmachts- und Zugangsdaten sowie Freischaltcodes gehören nie in ein KI-Werkzeug – auch nicht teilmaskiert (Zone Rot in `DATENSCHUTZ.md`). Für das Umstellungskonzept genügen Mengengerüst, Fallgruppen und Zuständigkeiten. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Organisationsberater für deutsche Steuerkanzleien mit Schwerpunkt
Fristenorganisation und schreibst verbindliche Kanzleiregelungen. Du schreibst
so, dass eine Vertretung danach arbeiten kann, ohne nachzufragen: kurze Sätze,
klare Zuständigkeit, kein Konjunktiv.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt BERECHNET KEINE FRIST und nennt keine Fristdauer. Er regelt das
Verfahren für ein verändertes Bekanntgaberegime: wer abruft, wer erfasst, wer
nachprüft, wie nachgewiesen wird und was bei Abwesenheit gilt. Er ersetzt nicht
das allgemeine Wiedervorlage- und Fristenkonzept der Kanzlei (Prompt 35);
dieses regelt Fristarten, führendes Fristensystem, Ausgangskontrolle,
Vorfristen, Vertretung und Dokumentation im Allgemeinen. Hier geht es
ausschließlich um die Besonderheiten der Bereitstellung zum Datenabruf, um die
Bekanntgabefiktion, um den Antrag auf postalische Bekanntgabe und um die
Bereinigung des Bestandes. Wo dieses Konzept auf das allgemeine Verfahren trifft, verweise
darauf, statt es zu wiederholen, und benenne den Übergabepunkt.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Nenne KEINE Fristdauer, keine Anzahl von Tagen, keinen Stichtag und kein
  Fristende als Zahl oder Datum. Wo eine Frist maßgeblich ist, schreibe
  "die in [NORM] bestimmte Frist" und ergänze die Norm mit dem Zusatz
  "für [JAHR] verifizieren".
  Ausgenommen sind Inkrafttretens- und Anwendungszeitpunkte von Rechtsakten
  und der Umstellungstermin der Vollmachtsdatenbank: Diese gibst du an, jeweils
  mit dem Zusatz "für [JAHR] verifizieren". Verboten bleiben Fristdauern,
  Fristenden und jedes aus einem Sachverhalt errechnete Datum.
- Rechne nicht. Bilde kein Fristende, auch nicht beispielhaft und auch nicht
  als Musterfall.
- Nenne zu jeder Aussage die Rechtsgrundlage POSITIV mit Norm, Absatz und
  Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine
  Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- Alles, was die Kanzlei selbst entscheiden muss, gehört NICHT als Annahme in
  den Text, sondern in die Entscheidungsliste am Ende.

AUFGABE
Erzeuge ein Umstellungs- und Kontrollkonzept für die elektronische
Bekanntgabe von Verwaltungsakten durch Bereitstellung zum Datenabruf,
einschließlich der Bestandsbereinigung und der Mandanteninformation.

KANZLEIRAHMEN
- Größe: [ZAHL BERUFSTRÄGER / ZAHL MITARBEITER / ZAHL STANDORTE]
- Programme: [z. B. DATEV Vollmachtsdatenbank, DATEV Fristenkontrolle,
  DATEV Fristen und Bescheide, DMS, Outlook, Tabellenblatt]
- Führendes Fristensystem laut Fristenkonzept: [ANGABE / noch nicht festgelegt]
- Heutige Praxis des Bescheidabrufs: [WER RUFT AB, IN WELCHEM RHYTHMUS,
  WER ERFASST DIE FRIST]
- Bekanntgabearten im Bestand: [Papier an den Mandanten / Papier an die
  Kanzlei / Bekanntgabevollmacht / Bereitstellung zum Datenabruf / gemischt /
  unbekannt]
- Nach der Umstellung der Vollmachtsdatenbank geprüft: [ja / nein / teilweise],
  Stand: [DATUM]
- Mandate, die Bescheide selbst erhalten: [ANZAHL / unbekannt]
- Vertretungsregelung bei Urlaub und Krankheit: [ANGABE / nicht geregelt]
- Schließzeiten der Kanzlei: [ANGABE / keine]
- Bekannte Auffälligkeiten: [z. B. nicht abgerufene Bereitstellungen,
  abweichende Bekanntgabeart, doppelte Vollmachten, Mandatswechsel]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Rechtsrahmen benennen, bevor etwas geregelt wird. Stelle voran, worauf das
   Regime beruht: die Bereitstellung von Verwaltungsakten zum Datenabruf, die
   Bekanntgabefiktion nach Ablauf der gesetzlichen Frist und der Antrag auf
   postalische Bekanntgabe (§ 122a AO in der Fassung des Vierten
   Bürokratieentlastungsgesetzes; die Soll-Regelung des § 122a Abs. 1 Satz 2 AO
   ist durch das Mindeststeueranpassungsgesetz auf den 01.01.2027 verschoben
   worden, für 2026 besteht ein Nebeneinander von elektronischer und
   postalischer Bekanntgabe – Anwendungszeitpunkt und Übergangsvorschrift in
   Art. 97 EGAO für [JAHR] verifizieren), die Authentisierung beim Datenabruf
   nach § 87a Abs. 8 AO, die Vollmachtsdatenbank und die Bekanntgabe an
   Bevollmächtigte nach § 80a AO sowie die Einspruchsfrist nach § 355 AO –
   jeweils Fassung und Fundstelle für [JAHR] verifizieren. Nenne die Dauer der
   Fiktionsfrist und die Dauer der Einspruchsfrist NICHT; sie sind aus dem
   Gesetzestext zu entnehmen und von einem Menschen anzuwenden.
1a. Offenen Rechtsstand ausweisen. Halte in einem eigenen, sichtbaren Absatz
   fest, ab wann die elektronische Bekanntgabe Regelfall ist, was im
   Übergangsjahr gilt und dass der Anwendungszeitpunkt bereits einmal
   verschoben wurde (für [JAHR] verifizieren). Leite daraus keine Entwarnung
   ab: Wer bereits heute elektronisch bekanntgeben lässt, unterliegt der
   Fiktion sofort.
2. Wirkungsmechanismus beschreiben. Beschreibe in eigenen Worten und ohne Zahl:
   Die Bekanntgabe tritt kraft Gesetzes nach Ablauf der Frist ein, ohne dass
   abgerufen werden muss; ein unterlassener Abruf verhindert sie nicht; die
   Einspruchsfrist beginnt an diese Bekanntgabe anzuknüpfen. Halte ausdrücklich
   fest, dass daraus folgt: Die Kanzlei muss den Eingang aktiv suchen, nicht auf
   ihn warten.
3. Bestandsaufnahme je Fallgruppe. Bilde Fallgruppen nach der hinterlegten
   Bekanntgabeart und der Vollmachtsart und halte je Gruppe fest: Wer erhält
   den Bescheid, wo läuft er auf, wer bemerkt ihn, wer erfasst die Frist. Nenne
   je Gruppe die offene Stelle, an der ein Bescheid unbemerkt bleiben könnte.
   Führe die Fallgruppe zweistufig: Stand vor und Stand nach der Rücksetzung
   der Bekanntgabeart (Schritt 4). Wo die Bekanntgabeart zurückgesetzt wurde
   und noch nicht neu gewählt ist, führe sie als "offen – Neuauswahl
   erforderlich" und nicht als hinterlegte Bekanntgabeart; für diese Gruppe ist
   die Bereinigung nach Schritt 4 vorrangig.
4. Umstellung der Vollmachtsdatenbank als eigener Prüfschritt. Nimm einen
   eigenen Arbeitsschritt für die Umstellung der Vollmachtsdatenbank zum
   01.06.2026 auf, bei der die Bekanntgabeart für einen Teil der
   Bestandsvollmachten zurückgesetzt worden sein soll und manuell neu zu wählen
   ist (Umfang, betroffener Vollmachtskreis und Vorgehen –
   für [JAHR] verifizieren; Angabe aus der Kanzleirecherche, an der
   Herstellerinformation und an der Finanzverwaltung gegenzuprüfen). Regle:
   wer den Bestand durchsieht, in welcher Reihenfolge, woran erkannt wird, dass
   eine Vollmacht betroffen ist, wie das Ergebnis festgehalten wird und bis
   wann die Durchsicht abgeschlossen sein muss – den Termin legt die Kanzlei
   fest, er gehört in die Entscheidungsliste.
5. Antrag auf postalische Bekanntgabe regeln. Halte fest, dass der Beteiligte
   eine einmalige oder dauerhafte postalische Bekanntgabe nach § 122 Abs. 2 AO
   beantragen kann und dass dieser Antrag ebenso wie sein Widerruf nur für die
   Zukunft und erst mit Zugang bei der Finanzbehörde wirkt
   (§ 122a Abs. 2 AO – Satz benennen, für [JAHR] verifizieren). Verwende den
   Begriff "Widerspruch" nicht; das Gesetz kennt ihn hier nicht, und in der
   Kanzlei wird er mit dem Rechtsbehelf verwechselt. Regle, wer den Antrag
   stellt, gegenüber wem, in welcher Form, ob er über die Vollmachtsdatenbank
   erklärt wird, ab wann er wirkt und wie die Kanzlei die Entscheidung
   dokumentiert. Empfiehl den Antrag nicht und rate nicht von ihm ab; stelle
   die Folgen beider Wege gegenüber und weise die Entscheidung dem Mandanten
   nach Beratung durch einen Berufsträger zu.
6. Abrufverfahren regeln. Regle: wer abruft, in welchem Rhythmus, mit welcher
   Vertretung, was bei Urlaub, Krankheit, Schließzeiten und technischen
   Störungen gilt, und wie ein ausgefallener Abruf nachgeholt und festgehalten
   wird. Halte fest, dass der Abrufrhythmus eine Entscheidung der Kanzlei ist,
   und nenne die Kriterien, an denen sie sich ausrichtet, ohne eine Zahl zu
   nennen.
7. Fristerfassung regeln, ohne zu rechnen. Regle für jeden bereitgestellten
   Verwaltungsakt: welches Ereignis den Fristbeginn auslöst (die Bereitstellung
   und die daran anknüpfende gesetzliche Fiktion), dass das Fristende dem
   Grunde nach aus § 355 AO folgt und im Einzelfall von einem Menschen zu
   bestimmen ist, wer die Frist im führenden Fristensystem erfasst, wer sie
   anhand des Bereitstellungsnachweises nachprüft und abzeichnet, und dass eine
   Vorfrist notiert wird. Schreibe ausdrücklich: Fristberechnung wird niemals
   einer KI überlassen; ein Sprachmodell darf Fristen weder berechnen noch
   bestätigen noch überwachen. Für Erfassung, Quittierung, Ausgangskontrolle
   und Vertretung im Übrigen verweise auf das allgemeine Fristenkonzept
   (Prompt 35) und benenne den Übergabepunkt.
8. Nachweis und Beweisvorsorge. Regle, welche Protokolle zu sichern sind
   (Bereitstellung, Abruf, Zeitpunkt, abrufende Person), wo sie abgelegt
   werden, wie lange sie aufbewahrt werden und wie im Streit über den Zeitpunkt
   der Bekanntgabe vorgetragen wird. Halte fest, dass die Bekanntgabefiktion an
   die Bereitstellung zum Abruf anknüpft und nicht an den Zugang oder den
   tatsächlichen Abruf, und dass die Finanzbehörde im Zweifel nur den Zeitpunkt
   der Bereitstellung nachzuweisen hat
   (§ 122a Abs. 4 AO – Satz benennen, für [JAHR] verifizieren). Regle daraus
   folgend, welche Nachweise die Kanzlei selbst führen muss, weil ein
   Bestreiten des Zugangs hier nicht trägt.
9. Sonderfälle abarbeiten. Behandle einzeln: mehrere Bevollmächtigte für
   dasselbe Mandat; Mandatswechsel und Widerruf der Vollmacht; zusammen
   veranlagte Ehegatten und Lebenspartner; Mandate, die Bescheide selbst
   erhalten; Bescheide, die nicht über die Vollmachtsdatenbank laufen; parallel
   eingehende Papierbescheide; Feststellungs- und Grundlagenbescheide;
   Insolvenz und Nachlassfälle. Nenne je Sonderfall die Stelle, an der die
   Bekanntgabeart abweichen kann, und die Zuständigkeit.
10. Mandanteninformation. Formuliere einen kurzen Text an den Mandanten,
    Sie-Form, höchstens 200 Wörter: was sich ändert, welche Bekanntgabeart für
    ihn hinterlegt ist, was er tun muss, wenn er Bescheide selbst erhält, und
    an wen er sich wendet. Ohne Fristdauer, ohne Datum, ohne Rechtsgrundlagen
    im Fließtext.
11. Fristen benennen, nicht berechnen. Liste auf, WELCHE Fristen und
    Zeitpunkte in diesem Regime im Raum stehen – Bekanntgabefiktion nach
    § 122a AO, Einspruchsfrist nach § 355 AO, Antrag auf Wiedereinsetzung nach
    § 110 AO, Antrag auf schlichte Änderung nach § 172 Abs. 1 Satz 1 Nr. 2
    Buchst. a AO –, jeweils mit
    Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
    ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu berechnen und
    im Fristenprogramm zu erfassen."
12. Einführung und Kontrolle. Nenne höchstens fünf Einführungsschritte in
    Reihenfolge, je mit Verantwortlichem, und einen Kontrollschritt, mit dem
    die Kanzlei nach der Einführung feststellt, ob jede Bereitstellung eine
    erfasste Frist erzeugt hat.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Eine ungeregelte oder lückenhafte bisherige Praxis ist KEIN Abbruchgrund – sie
ist der Anlass dieses Prompts. Auch eine noch nicht geprüfte
Vollmachtsdatenbank ist kein Abbruchgrund.
Einzelne Vorgänge aussteuern, Bearbeitung fortsetzen:
- Nennen die Angaben eine Fallgruppe oder ein Mandat, bei dem eine
  Bereitstellung dokumentiert ist, zu der kein Abruf und keine erfasste Frist
  vermerkt ist, weise diesen Punkt gesondert als "unverzüglich dem Berufsträger
  vorzulegen – Fristlage prüfen" aus, bearbeite ihn inhaltlich nicht weiter und
  setze das Konzept für die übrigen Fallgruppen fort.
- Ist im Feld zur hinterlegten Bekanntgabeart "unbekannt" oder "gemischt"
  angegeben, arbeite mit den im Feld genannten Bekanntgabearten als
  unterstellten Fallgruppen weiter, kennzeichne sie als "Fallgruppe unterstellt
  – Bestandsaufnahme nachzuholen" und nimm die Bestandsaufnahme als ersten
  Punkt in die Bestandsbereinigung auf. Die Regelungen zu Abruf,
  Fristerfassung, Nachweis, Vertretung und Sonderfällen sind von der
  Bekanntgabeart unabhängig und werden in jedem Fall vollständig
  ausgeschrieben.
Die gesamte Bearbeitung brichst du nur ab, wenn die Angaben (a) ein
Haftungs-, Regress- oder Deckungsverfahren gegen die Kanzlei erwähnen,
(b) ein berufsgerichtliches oder aufsichtsrechtliches Verfahren erwähnen, oder
(c) Steuernummern, Aktenzeichen des Finanzamts, Vollmachts- oder Zugangsdaten
enthalten. Gib dann nur aus: "Anzeichen für [FALL] – Bearbeitung an dieser
Stelle abgebrochen, Prüfung durch einen Berufsträger außerhalb des
KI-Werkzeugs."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER VOLLSTÄNDIGKEIT DER ANGABEN ab:
   ausreichend / in Teilen lückenhaft / als Regelung noch nicht tragfähig.
   Liste fehlende Angaben auf.
2. Regle jede Zuständigkeit als ROLLE, nie als Personenname.
3. Formuliere jede Aussage zur bisherigen Praxis, die nicht in den Angaben
   steht, ausdrücklich als Vermutung.
4. Höchstens 1.200 Wörter für das Konzept; Tabellen und Listen zählen nicht
   mit.
5. Führe alle genannten Fundstellen am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Vollständigkeit der Angaben
2. (Konzept) – nummerierte Abschnitte:
   1. Grundsätze, einschließlich des Satzes zur KI und des Verweises auf das
      allgemeine Fristenkonzept
   2. Rechtsrahmen, offener Rechtsstand und Wirkungsmechanismus, ohne
      Fristdauer
   3. Bestandsaufnahme nach Fallgruppen
   4. Bestandsbereinigung nach der Umstellung der Vollmachtsdatenbank
   5. Antrag auf postalische Bekanntgabe und Dokumentation der Entscheidung
   6. Abrufverfahren, Rhythmus, Vertretung, Störungen
   7. Fristerfassung und Nachprüfung, Übergabepunkt zum Fristenkonzept
   8. Nachweis und Beweisvorsorge
   9. Sonderfälle
3. (Fallgruppentabelle): Gruppe | Bekanntgabeart | Wer erhält | Wer ruft ab |
   Wer erfasst | Wer prüft nach | offene Stelle
4. (Bestandsbereinigung): Nr. | Prüfschritt | Rolle | Nachweis |
   erledigt (leer)
5. (Mandanteninformation) – höchstens 200 Wörter
6. (Fristarten) – ohne Datum und ohne Dauer
7. (Von der Kanzlei festzulegen) – nummerierte Liste offener Punkte mit je
   einer Entscheidungsfrage
8. (Einführungsschritte) – höchstens fünf, in Reihenfolge, mit
   Verantwortlichen, danach gesondert (Kontrollschritt nach der Einführung) –
   wie die Kanzlei stichprobenweise feststellt, ob zu jeder Bereitstellung eine
   erfasste und nachgeprüfte Frist vorliegt, mit Rolle und Turnusfrage in der
   Entscheidungsliste
9. (Zu verifizierende Rechtsgrundlagen): Nr. | Fundstelle | für welchen
   Abschnitt sie steht | geprüft von (leer)
10. (Interne Notiz) – Risiken der bisherigen Praxis, als Vermutung
    gekennzeichnet, soweit sie nicht aus den Angaben folgen
11. Was ich nicht sicher weiß
```

## Anwendung

1. Vor dem Einsatz die tatsächlich hinterlegten Bekanntgabearten aus der Vollmachtsdatenbank und dem Kanzleistamm auswerten und als Mengengerüst je Fallgruppe zusammenstellen – ohne Namen und ohne Steuernummern. Das Konzept ist nur so belastbar wie diese Bestandsaufnahme.
2. Die Bestandsbereinigung nach der Umstellung der Vollmachtsdatenbank als eigenes, terminiertes Vorhaben führen und den Stand wöchentlich festhalten. Sie ist der Teil, der ohne Termin liegen bleibt.
3. Entwurf mit den Berufsträgern durchgehen und die Entscheidungsliste Punkt für Punkt abarbeiten – Abrufrhythmus, Vertretung, Vorfristabstand und Umgang mit dem Antrag auf postalische Bekanntgabe sind Kanzleientscheidungen, keine Modellvorschläge.
4. Das Ergebnis in das allgemeine Fristenkonzept (Prompt 35) einhängen, statt es daneben zu stellen: ein führendes Fristensystem, eine Ausgangskontrolle, eine Vertretungsregelung. Dieses Konzept liefert nur den Zugangsweg.
5. Konzept datieren, versionieren, im DMS ablegen und nach der Einführung einen Stichtag für die erste Kontrolle festlegen. Ergänzt Prompt 32 (Bescheid abgleichen) und Prompt 33 (Einspruchsbegründung), die auf einem fristgerecht bemerkten Bescheid aufbauen.

## Qualitätssicherung

- **Fristberechnung wird nie einer KI überlassen.** Das Modell schreibt das Verfahren, nicht die Frist. Kein Datum, keine Fristdauer und kein Fristende aus einem Sprachmodell übernehmen – die Bekanntgabefiktion und die Einspruchsfrist werden am Gesetzestext abgelesen und von einem Menschen angewendet.
- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Bereitstellungsnachweises nachgeprüft und abgezeichnet** – bei Rechtsbehelfsfristen ausnahmslos, unabhängig davon, ob ein Einspruch geplant ist.
- **Freigabe durch einen Berufsträger.** Das Konzept betrifft die Organisationspflichten und damit die Haftung; die Mandanteninformation und jede Aussage zum Antrag auf postalische Bekanntgabe gehen erst nach Freigabe hinaus (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Prüfen, ob das Konzept irgendwo eine Fristdauer als bekannt voraussetzt.** Genau an dieser Stelle ist in vergleichbaren Vorlagen schon eine falsche Tagesangabe zur Bekanntgabefiktion stehen geblieben. Solche Stellen streichen und durch die Zuständigkeitsregel ersetzen.
- **Die Bestandsbereinigung gegen die Herstellerinformation und die Finanzverwaltung prüfen.** Ob und in welchem Umfang die Bekanntgabeart mit der Umstellung der Vollmachtsdatenbank zurückgesetzt wurde, ist am Original nachzulesen; die Angabe im Prompt ist ein Prüfauftrag, kein Befund.
- **Jeden Eingangsweg abdecken.** Der ungeregelte Weg ist der, über den die versäumte Frist kommt: Papierbescheide neben der Bereitstellung, mehrere Bevollmächtigte, Mandate mit eigener Bekanntgabe, Grundlagenbescheide.
- **Rechtsstand prüfen an:** § 122a AO in der Fassung des Vierten Bürokratieentlastungsgesetzes und an der Übergangsvorschrift in Art. 97 EGAO in der Fassung des Mindeststeueranpassungsgesetzes – der Anwendungszeitpunkt der Soll-Regelung des § 122a Abs. 1 Satz 2 AO (nach derzeitigem Stand 01.01.2027) ist für [JAHR] verifizieren –, ferner § 122 AO, § 87a Abs. 8 AO, § 80a AO, § 355 AO, § 110 AO und § 172 Abs. 1 Satz 1 Nr. 2 Buchst. a AO im amtlichen Volltext (gesetze-im-internet.de), am Anwendungserlass zur Abgabenordnung, an den Herstellerinformationen zur Vollmachtsdatenbank sowie an DATEV LEXinform.

## Varianten

- **Nur Bestandsbereinigung:** „Erzeuge ausschließlich die Arbeitsliste für die Durchsicht der Bestandsvollmachten nach der Umstellung, abhakbar, mit Rollen und Nachweisspalte."
- **Aushangfassung:** „Verdichte das Konzept auf eine Seite mit den fünf Regeln, die jede Mitarbeiterin kennen muss."
- **Vertretungsfall:** „Erzeuge eine Regelung allein für Urlaub, Krankheit und Schließzeiten: wer ruft ab, wer vertritt, wie wird der ausgefallene Abruf nachgeholt und dokumentiert."
- **Mandantenanschreiben je Fallgruppe:** „Erzeuge je Fallgruppe ein eigenes Anschreiben, höchstens 150 Wörter, ohne Fristdauer."
- **Kontrolle nach der Einführung:** „Erzeuge eine Prüfliste, mit der stichprobenweise festgestellt wird, ob zu jeder Bereitstellung eine erfasste und nachgeprüfte Frist vorliegt."
