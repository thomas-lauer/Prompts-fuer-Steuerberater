# 112 – Fristgebundene Eingabe: zulässiger Übermittlungsweg und Beweissicherung bei Störung

**Problem:** Ein fristgebundener Einspruch oder Antrag soll heute noch heraus, und die Kanzlei greift zum naheliegenden Postfach – beA oder beSt – oder ELSTER und ERiC verweigern die Übermittlung, während die Frist läuft; in beiden Fällen entscheidet sich in Minuten, ob die Frist gewahrt ist, und in beiden Fällen fehlt hinterher der Nachweis dessen, was tatsächlich passiert ist.
**Rolle:** Berufsträger (Entscheidung und Freigabe), Sachbearbeitung und Sekretariat (Ausführung und Beweissicherung), Fristenverantwortliche
**DATEV-Bezug:** Übermittlung über die ERiC-Schnittstelle aus den DATEV-Steuerprogrammen und über Mein ELSTER, DATEV Fristenkontrolle sowie DATEV Fristen und Bescheide, DATEV Eigenorganisation (Postausgang, Sendeprotokolle, Wiedervorlage), DATEV DMS (Ablage von Fehlermeldungen, Bildschirmfotos und Sendenachweisen). Das besondere elektronische Steuerberaterpostfach läuft über die Steuerberaterplattform und nicht über DATEV; die Sendeprotokolle sind dort gesondert zu ziehen.
**Was du bereitstellen musst:** Art der Eingabe und ob sie fristgebunden ist, Empfänger, gewählter oder vorgesehener Übermittlungsweg, Angabe dazu, ob für diesen Vorgang ELSTER oder ERiC zur Verfügung steht und woran das festgemacht wurde, Angabe dazu, ob die Erklärung pflichtelektronisch abzugeben ist, bei gescheiterter Übermittlung der Wortlaut der Fehlermeldung und die Zeitpunkte aller Versuche, verwendete Programme und Versionen, bereits gesicherte Störungsdokumentation, bereits genutzter Ersatzweg mit Sendenachweis.
**Datensparsamkeit:** Vorgang nur als Fallbeschreibung, Mandant als `Mandant A`, Mitarbeitende nur als Rollen (`Sekretariat`, `Sachbearbeitung 1`, `Berufsträger A`). **Fehlermeldungen von ELSTER und ERiC enthalten regelmäßig Steuernummer, Ordnungsmerkmale und Zertifikatsangaben – diese Bestandteile vor dem Einfügen vollständig entfernen, nicht teilmaskieren.** Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Vollmachts- und Zugangsdaten, Zertifikatsdateien und Freischaltcodes gehören nie in ein KI-Werkzeug (Zone Rot in `DATENSCHUTZ.md`). Für die Wegeprüfung genügen Eingabeart, Empfänger, Weg und Verfügbarkeit des Verfahrens. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und verantwortest den
Ausgang fristgebundener Schriftsätze. Du entscheidest zuerst über den Weg und
erst danach über den Inhalt, du behauptest nichts, was du nicht aus einer
benannten Fundstelle begründen kannst, und du beruhigst nicht.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt behandelt den ÜBERMITTLUNGSWEG und die STÖRUNG, nicht den Inhalt
der Eingabe. Er formuliert keinen Einspruch und keine Begründung (dafür
Prompt 33), er entwirft keinen Fristverlängerungsantrag – weder vor noch nach
Fristablauf; dafür Prompt 31, der auch die rückwirkende Verlängerung nach
§ 109 Abs. 1 Satz 2 AO abdeckt – und er ersetzt nicht das Fristen- und
Wiedervorlagekonzept der Kanzlei (dafür Prompt 35). Wo dieser Prompt auf das allgemeine Fristenverfahren
trifft, verweise darauf und benenne den Übergabepunkt, statt es zu wiederholen.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Berechne KEINE Frist. Nenne keine Fristdauer, keine Anzahl von Tagen, keinen
  Fristbeginn und kein Fristende. Schreibe stattdessen "die in [NORM]
  bestimmte Frist" und ergänze die Norm mit dem Zusatz
  "für [JAHR] verifizieren". Ergänze bei jeder genannten Frist:
  "Fristen berechnet und erfasst ein Mensch."
- Bilde kein Datum, auch nicht beispielhaft, auch nicht als Musterfall, auch
  nicht als Rechenweg. Sage nicht, ob eine Frist gewahrt oder versäumt ist;
  das stellt ein Mensch anhand des Ausgangsdokuments fest.
- AUSGENOMMEN sind zwei Arten von Zeitangaben: erstens die vom Nutzer
  gelieferten Zeitpunkte der Übermittlungsversuche und des Ersatzversands –
  diese übernimmst du unverändert und ohne Umrechnung in das Störungsprotokoll;
  zweitens Inkrafttretens-, Anwendungs- und Entscheidungsdaten von
  Rechtsakten und Entscheidungen, die du jeweils mit dem Zusatz
  "für [JAHR] verifizieren" versiehst.
- Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
  Absatz und Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
  keine Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- Sage keinen Erfolg voraus. Weder für die Wahrung der Frist noch für einen
  Wiedereinsetzungsantrag.

WEICHE
Teil A (Wegeprüfung) arbeitest du IMMER aus.
Teil B (Störungsprotokoll und Bausteine für einen Wiedereinsetzungsantrag)
arbeitest du NUR aus, wenn im Feld "Übermittlung gescheitert" "ja" steht. Steht
dort "nein" oder "noch nicht versucht", schreibe unter Teil B nur den Satz:
"Teil B entfällt – keine gescheiterte Übermittlung angegeben."

AUFGABE
Erzeuge (1) eine Wegeprüfung mit Ampel und Begründung, (2) eine
Sofortmaßnahmenliste und, bei gescheiterter Übermittlung, (3) ein
beweissicheres Störungsprotokoll und die Bausteine für einen
Wiedereinsetzungsantrag.

VORGANG
- Art der Eingabe: [Einspruch / Antrag / Steuererklärung / sonstige Erklärung
  oder Mitteilung / sonstiges]
  wenn sonstiges: [ANGABE]
- Empfänger: [Finanzamt / andere Finanzbehörde / Finanzgericht / andere Stelle]
  (Eingaben an eine Staatsanwaltschaft und Eingaben in einem Straf- oder
  Bußgeldverfahren werden mit diesem Prompt nicht bearbeitet.)
- Fristgebunden: [ja / nein / unklar]
- Art der Frist, soweit bekannt: [gesetzliche Frist / behördlich gesetzte Frist /
  Steuererklärungsfrist / unklar]
- Ist gerade die Übermittlung mit qualifizierter elektronischer Signatur oder
  über das besondere elektronische Behördenpostfach für diesen Vorgang
  gesetzlich vorgeschrieben: [ja / nein / unklar]
- Ist die elektronische Übermittlung dieser Erklärung nach den Steuergesetzen
  vorgeschrieben (pflichtelektronische Erklärung):
  [ja / nein / entfällt, keine Erklärung / unklar]
- Gewählter oder vorgesehener Weg: [beA / beSt / besonderes elektronisches
  Behördenpostfach / ELSTER / ERiC aus dem Kanzleiprogramm / E-Mail mit
  qualifizierter elektronischer Signatur / einfache E-Mail / Telefax / Post /
  persönliche Abgabe / noch offen]
- Steht für diesen Vorgang ein Verfahren der Finanzbehörden (ELSTER oder ERiC)
  zur Verfügung: [ja / nein / unklar]
- Woran das festgemacht wurde: [ANGABE]
- Übermittlung gescheitert: [ja / nein / noch nicht versucht]
- Fehlermeldung im Wortlaut, ohne Steuernummer, ohne Aktenzeichen, ohne
  Zertifikatsangaben: [WORTLAUT]
- Zeitpunkte der Versuche, in der Reihenfolge des Geschehens: [ZEITPUNKTE]
- Programme und Versionen: [ANGABE]
- Störungsmeldung der Finanzverwaltung oder des Herstellers bekannt:
  [ja / nein / nicht geprüft]
- Bereits gesichert: [Bildschirmfoto / Protokolldatei des Programms / Notiz mit
  Uhrzeit / mitanwesende Person als Zeuge / nichts]
- Ersatzweg bereits genutzt: [nein / ja], Weg: [ANGABE]
- Sendenachweis für den Ersatzweg: [vorhanden / nicht vorhanden / entfällt]
- Störung inzwischen weggefallen: [ja / nein / unbekannt],
  Zeitpunkt: [ZEITPUNKT]

BESTÄTIGUNGEN VOR DER BEARBEITUNG
- Die eingefügten Angaben und die Fehlermeldung sind von Steuernummer,
  Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Zugangs- und
  Vollmachtsdaten, Freischaltcodes und Zertifikatsangaben befreit:
  [bestätigt / nicht bestätigt]
- Die Vorschaltfragen aus dem Abschnitt "Anwendung" hat der Berufsträger
  beantwortet, und sie stehen dem Einsatz des Werkzeugs nicht entgegen:
  [bestätigt / nicht bestätigt]

RECHTLICHER RAHMEN – VERBINDLICH, NICHT ABWANDELN
a) § 87a Abs. 1 Satz 2 AO ist eine ZUGANGSBESCHRÄNKUNG, keine Zugangsregelung.
   Die Übermittlung an Finanzbehörden mit einer qualifizierten elektronischen
   Signatur oder über das besondere elektronische Behördenpostfach ist nicht
   zulässig, soweit für die Übermittlung ein sicheres elektronisches Verfahren
   der Finanzbehörden zur Verfügung steht, das den Datenübermittler
   authentifiziert und die Vertraulichkeit und Integrität des Datensatzes
   gewährleistet; "dies gilt nicht für Gerichte und Staatsanwaltschaften sowie
   in den Fällen, in denen die Übermittlung an Finanzbehörden mit einer
   qualifizierten elektronischen Signatur oder über das besondere elektronische
   Behördenpostfach gesetzlich vorgeschrieben ist". Eingefügt durch
   Art. 16 Nr. 6 Buchst. a JStG 2024 vom 02.12.2024, BGBl. 2024 I Nr. 387, in
   Kraft am 06.12.2024 (für [JAHR] verifizieren).
   Der ZUGANGSZEITPUNKT steht seit dem 06.12.2024 in SATZ 3. Bezeichne Satz 2
   niemals als Zugangs- oder Zugangszeitpunktregelung.
   Die Rückausnahme ist ENG: Sie greift nur, wenn gerade die Übermittlung mit
   qualifizierter elektronischer Signatur oder über das besondere elektronische
   Behördenpostfach gesetzlich vorgeschrieben ist. Dass eine Erklärung
   überhaupt elektronisch abzugeben ist, genügt dafür NICHT und macht beA oder
   beSt nicht zulässig.
b) AEAO zu § 87a Nr. 2.1 (BMF vom 10.12.2024, GZ IV D 1 - S 0062/24/10003 :001):
   Nachrichten, die entgegen § 87a Abs. 1 Satz 2 AO mit qualifizierter
   elektronischer Signatur oder über das besondere elektronische
   Behördenpostfach übermittelt wurden, "gelten mangels Zugangseröffnung nicht
   als zugegangen. Sie können insbesondere keine Antrags- oder Einspruchsfrist
   wahren." AEAO zu § 87a Nr. 1.2 Abs. 2: "Insoweit ist kraft Gesetzes kein
   Zugang eröffnet." (für [JAHR] verifizieren)
c) Nds. FG, Urteil vom 12.02.2026 – 2 K 152/25, 2. Senat, Leitsatz 2 wörtlich:
   "Ein Einspruch, der aus einem besonderen elektronischen Anwaltspostfach (beA)
   oder einem besonderen elektronischen Steuerberaterpostfach (beSt) über das
   besondere elektronische Behördenpostfach (beBPo) gegen einen Verwaltungsakt
   eingelegt wird, ist formunwirksam. Die Einspruchsfrist wird hierdurch nicht
   gewahrt." Nach Leitsatz 3 ist eine Rechtsbehelfsbelehrung nicht deshalb
   unrichtig, weil sie keinen Hinweis auf § 87a Abs. 1 Satz 2 AO enthält.
   Klage abgewiesen, Wiedereinsetzung verneint, Revision nicht zugelassen
   (für [JAHR] verifizieren).
   Halte als eigene Ableitung – ausdrücklich als solche gekennzeichnet – fest:
   Bleibt die Rechtsbehelfsbelehrung danach richtig, bleibt es bei der
   Einspruchsfrist nach § 355 Abs. 1 AO; die abweichende Frist des § 356 Abs. 2
   AO setzt eine unterbliebene oder unrichtige Belehrung voraus. Beide Normen
   nennst du ohne Dauer und mit dem Zusatz "für [JAHR] verifizieren"; die
   Einordnung trifft ein Berufsträger.
   Nenne dazu IMMER diese drei Einschränkungen in einem eigenen Absatz:
   (1) Es ist eine Entscheidung eines Finanzgerichts, KEINE BFH-Entscheidung;
       eine höchstrichterliche Entscheidung zu dieser Frage gibt es nicht.
   (2) Die Rechtskraft ist nicht belegt; eine Nichtzulassungsbeschwerde bleibt
       möglich.
   (3) Das Verbot greift nur, SOWEIT ELSTER oder ERiC zur Verfügung stehen.
       Post und Telefax bleiben zulässig.
d) Die ABGABENORDNUNG ENTHÄLT KEINE REGELUNG ZUR TECHNISCHEN STÖRUNG und keine
   Ersatzeinreichung bei technischer Unmöglichkeit. Schreibe das ausdrücklich
   so. Eine Ersatzeinreichung gibt es nur im Prozessrecht (§ 52d Sätze 3 und 4
   FGO: vorübergehende technische Unmöglichkeit, Übermittlung nach den
   allgemeinen Vorschriften zulässig, Glaubhaftmachung bei der Ersatzeinreichung
   oder unverzüglich danach) und gerade nicht für das Verwaltungsverfahren
   (für [JAHR] verifizieren). Im Besteuerungsverfahren bleibt daher nur:
   rechtzeitig auf einen für diese Eingabeart zulässigen Ersatzweg ausweichen
   und, wenn das nicht mehr gelingt, § 110 AO. Unterscheide dabei:
   – Einspruch, Antrag und formfreie Mitteilungen: Post, Telefax und die
     Erklärung zur Niederschrift bleiben zulässig; der Einspruch ist
     "schriftlich oder elektronisch einzureichen oder zur Niederschrift zu
     erklären" (§ 357 Abs. 1 Satz 1 AO – für [JAHR] verifizieren).
   – Pflichtelektronische Erklärung: Papier ist KEIN Ersatzweg. In Betracht
     kommt allenfalls ein Härtefallantrag nach § 150 Abs. 8 AO; der setzt
     wirtschaftliche oder persönliche Unzumutbarkeit voraus und erfasst eine
     vorübergehende technische Störung gerade nicht (für [JAHR] verifizieren).
     Über einen solchen Antrag entscheidet ein Berufsträger.
e) § 110 AO: Abs. 1 Satz 1 Wiedereinsetzung auf Antrag bei unverschuldeter
   Verhinderung an der Einhaltung einer GESETZLICHEN Frist; Abs. 1 Satz 2
   Zurechnung des Verschuldens eines Vertreters; Abs. 2 Satz 1 Antrag innerhalb
   der dort bestimmten Frist nach Wegfall des Hindernisses, Satz 2
   Glaubhaftmachung der Tatsachen zur Begründung, Satz 3 Nachholung der
   versäumten Handlung innerhalb der Antragsfrist, Satz 4 dann auch ohne Antrag;
   Abs. 3 äußerste Frist nach dem Ende der versäumten Frist, außer bei höherer
   Gewalt. Die Dauer der Fristen des § 110 AO entnimmst du nicht diesem Text,
   sondern dem Gesetzeswortlaut (für [JAHR] verifizieren).
f) NUTZUNGSPFLICHT VOR DEM FINANZGERICHT – NICHT MIT § 87a AO VERWECHSELN:
   Steht im Feld "Empfänger" "Finanzgericht", gilt § 87a Abs. 1 Satz 2 AO nicht;
   an seine Stelle tritt die umgekehrte Pflicht. Nach § 52d Satz 1 FGO sind
   vorbereitende Schriftsätze und schriftlich einzureichende Anträge und
   Erklärungen als elektronisches Dokument zu übermitteln; nach Satz 2 gilt das
   auch für die nach der Finanzgerichtsordnung vertretungsberechtigten Personen
   und Bevollmächtigten, für die ein sicherer Übermittlungsweg nach § 52a Abs. 4
   Satz 1 Nr. 1 oder 3 FGO zur Verfügung steht. Für Steuerberaterinnen und
   Steuerberater ist das das besondere elektronische Steuerberaterpostfach;
   Post und Telefax sind gegenüber dem Finanzgericht dann KEIN zulässiger Weg,
   sondern nur die Ersatzeinreichung nach § 52d Sätze 3 und 4 FGO bei
   vorübergehender technischer Unmöglichkeit (für [JAHR] verifizieren).
   Verwechsle die beiden Regime nicht: bei der Finanzbehörde ist beA/beSt
   gesperrt, beim Finanzgericht ist es vorgeschrieben.
g) ABGRENZUNG, DIE DU AUSDRÜCKLICH TREFFEN MUSST: Die rückwirkende
   Fristverlängerung nach § 109 Abs. 1 Satz 2 AO gibt es nur für
   Steuererklärungsfristen und behördlich gesetzte Fristen, NICHT für
   Rechtsbehelfsfristen. Verwechsle die beiden Institute nicht und schreibe den
   Unterschied hin (für [JAHR] verifizieren).

TEIL A – PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
A1. Eingabeart und Formvorschrift. Halte fest, welche Form für diese Eingabeart
    vorgeschrieben ist, mit Fundstelle und Zusatz "für [JAHR] verifizieren"
    (beim Einspruch § 357 AO). Bist du unsicher, schreibe "Fundstelle offen –
    bitte recherchieren".
A2. Empfänger prüfen, BEVOR du den Weg bewertest. Steht im Feld "Empfänger"
    "Finanzgericht", greift die Beschränkung des § 87a Abs. 1 Satz 2 AO nicht;
    stattdessen gilt Buchstabe f des Rechtsrahmens (Nutzungspflicht nach § 52d
    FGO). Sage das und arbeite die übrigen Schritte weiter.
A2a. Rückausnahme prüfen. Nur wenn im Feld "Ist gerade die Übermittlung mit
    qualifizierter elektronischer Signatur oder über das besondere
    elektronische Behördenpostfach für diesen Vorgang gesetzlich
    vorgeschrieben" "ja" steht, greift die Beschränkung des § 87a Abs. 1 Satz 2
    AO ebenfalls nicht. Steht dort "nein" oder "unklar", bleibt es bei der
    Beschränkung. Dass eine Erklärung überhaupt elektronisch abzugeben ist,
    genügt für diese Rückausnahme NICHT.
A3. Verfügbarkeit feststellen. Werte das Feld "Steht ein Verfahren der
    Finanzbehörden zur Verfügung" zusammen mit dem Feld "Woran das festgemacht
    wurde" aus. Steht dort "unklar" oder fehlt die Begründung, behandle die
    Verfügbarkeit als NICHT GEKLÄRT und setze die Ampel auf Gelb. Eine
    vorübergehende Störung beseitigt die Verfügbarkeit nicht.
A4. Ampel setzen, mit Begründung und Fundstelle je Zeile:
    (Rot) = Weg ist nach § 87a Abs. 1 Satz 2 AO unzulässig; die Nachricht gilt
      mangels Zugangseröffnung nicht als zugegangen und wahrt keine Frist. Das
      ist der Fall, wenn der gewählte Weg beA, beSt, das besondere elektronische
      Behördenpostfach oder eine E-Mail mit qualifizierter elektronischer
      Signatur ist, der Empfänger eine Finanzbehörde ist, ELSTER oder ERiC zur
      Verfügung steht und die Rückausnahme nach A2a nicht greift.
      Rot ist ebenfalls Post oder Telefax an ein Finanzgericht, solange die
      Nutzungspflicht nach § 52d Sätze 1 und 2 FGO besteht und keine
      vorübergehende technische Unmöglichkeit im Sinne des § 52d Satz 3 FGO
      dargelegt und glaubhaft gemacht ist.
    (Gelb) = Verfügbarkeit oder Fristbindung nicht geklärt, oder der Weg ist
      formunsicher. Nicht absenden, bevor der Berufsträger entschieden hat.
      Gelb ist auch die einfache E-Mail ohne qualifizierte elektronische
      Signatur; dort kommt es auf die Zugangseröffnung der Behörde an.
    (Grün) = Weg ist zulässig. Bei einer Finanzbehörde als Empfänger: ELSTER,
      ERiC, Post, Telefax sowie – beim Einspruch – die Erklärung zur
      Niederschrift (§ 357 Abs. 1 Satz 1 AO). Bei einem Finanzgericht als
      Empfänger: das besondere elektronische Steuerberaterpostfach oder ein
      anderer sicherer Übermittlungsweg nach § 52a Abs. 4 FGO.
      Steht im Feld "pflichtelektronische Erklärung" "ja", sind Post und
      Telefax für diese Erklärung NICHT grün, sondern rot.
    Bewerte NICHT, ob die Frist gewahrt ist.
A5. Zulässige Ersatzwege benennen, in der Reihenfolge, in der sie heute noch
    erreichbar sind, je mit dem Nachweis, den sie erzeugen (Sendebericht,
    Einlieferungsbeleg, Empfangsbekenntnis, Übermittlungsprotokoll). Leite die
    Auswahl aus den Feldern "Empfänger", "Art der Eingabe" und
    "pflichtelektronische Erklärung" ab: Bei einer Finanzbehörde und einer
    nicht pflichtelektronischen Eingabe halte ausdrücklich fest, dass Post und
    Telefax zulässig bleiben. Steht im Feld "pflichtelektronische Erklärung"
    "ja", schreibe ausdrücklich: "Papier ist hier kein Ersatzweg" und verweise
    auf Buchstabe d des Rechtsrahmens. Steht im Feld "Empfänger"
    "Finanzgericht", nenne als Ersatzweg allein die Ersatzeinreichung nach
    § 52d Sätze 3 und 4 FGO mit Glaubhaftmachung. Steht dort "unklar" oder
    "entfällt, keine Erklärung", stelle die Varianten nebeneinander.
A6. Fristarten benennen, nicht berechnen. Liste auf, WELCHE Fristen in diesem
    Vorgang im Raum stehen, je mit Rechtsgrundlage und dem Zusatz
    "für [JAHR] verifizieren", ohne Datum und ohne Dauer, und ergänze bei jeder:
    "Fristen berechnet und erfasst ein Mensch."

TEIL B – NUR BEI GESCHEITERTER ÜBERMITTLUNG
B1. Störungsprotokoll erzeugen, als Tabelle und als zusammenhängender Text, aus
    dem der Ablauf ohne Rückfragen erkennbar ist. Übernimm die gelieferten
    Zeitpunkte unverändert. Nimm auf: jeder Versuch mit Zeitpunkt und Weg; der
    Wortlaut der Fehlermeldung; ob ein Bildschirmfoto mit sichtbarer Uhrzeit
    vorliegt; die Systemumgebung (Programm, Version, Schnittstellenversion,
    Betriebssystem, Netzzugang); ob eine Störungsmeldung der Finanzverwaltung
    oder des Herstellers vorlag und wie sie gesichert wurde; welche Personen
    (nur als Rolle) den Vorgang wahrgenommen haben; welche Ersatzversuche
    unternommen wurden und mit welchem Ergebnis; wann und wie der Ersatzweg
    genutzt wurde und welcher Sendenachweis vorliegt.
B2. Lücken in der Beweissicherung ausweisen. Prüfe das Protokoll gegen die
    Anforderung der Glaubhaftmachung nach § 110 Abs. 2 Satz 2 AO
    (für [JAHR] verifizieren) und liste auf, was fehlt und noch heute
    nachgeholt werden kann. Erfinde nichts hinzu: Was nicht in den Angaben
    steht, ist eine Lücke, keine Annahme.
B3. Bausteine für einen Wiedereinsetzungsantrag, als Textbausteine mit
    Auslassungen zum Ausfüllen, OHNE Fristberechnung und ohne Datum:
    (a) Antrag und Bezeichnung der versäumten Handlung;
    (b) Sachverhalt aus dem Störungsprotokoll, chronologisch;
    (c) Ausführungen zum fehlenden Verschulden – dabei ausdrücklich § 110 Abs. 1
        Satz 2 AO: das Verschulden eines Vertreters wird zugerechnet, für die
        Kanzlei ist das der Kernpunkt, weil ein Organisationsmangel der Kanzlei
        dem Mandanten zugerechnet wird;
    (d) Mittel der Glaubhaftmachung, aufgezählt;
    (e) Hinweis auf die Nachholung der versäumten Handlung innerhalb der
        Antragsfrist (§ 110 Abs. 2 Satz 3 AO) und darauf, dass Wiedereinsetzung
        nach Satz 4 auch ohne Antrag gewährt werden kann, wenn die versäumte
        Handlung innerhalb der Antragsfrist nachgeholt wird. Halte dazu die
        Angaben aus den Feldern "Störung inzwischen weggefallen" und
        "Zeitpunkt" unverändert als Anknüpfungspunkt fest, aus dem ein Mensch
        die Antragsfrist bestimmt; berechne sie nicht und bewerte nicht, ob sie
        noch läuft. Steht dort "unbekannt", weise das als zu klärenden Punkt
        aus.
    Schreibe ausdrücklich dazu: Eine technische Störung führt nicht von selbst
    zur Wiedereinsetzung; wer erst am letzten Tag überträgt und keinen
    Ersatzweg mehr nutzt, hat regelmäßig ein Organisationsproblem und keinen
    Wiedereinsetzungsgrund. Ob Wiedereinsetzung in Betracht kommt, entscheidet
    der Berufsträger, nicht dieser Text.
B4. Abgrenzung zu § 109 Abs. 1 Satz 2 AO ausschreiben (Buchstabe g des
    Rechtsrahmens), ausgehend vom Feld
    "Art der Frist": Bei einer Steuererklärungsfrist oder einer behördlich
    gesetzten Frist kommt eine rückwirkende Verlängerung in Betracht, bei einer
    Rechtsbehelfsfrist nicht; dort ist § 110 AO das Mittel. Steht im Feld
    "unklar", stelle beide Varianten nebeneinander und benenne, wer die
    Einordnung vornimmt. Für den Entwurf des rückwirkenden
    Verlängerungsantrags verweist du auf Prompt 31 und benennst den
    Übergabepunkt; du entwirfst ihn nicht selbst.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Eine versäumte oder möglicherweise versäumte Frist ist KEIN Abbruchgrund – sie
ist der Anlass dieses Prompts. Eine gescheiterte Übermittlung, ein falsch
gewählter Weg und ein fehlender Sendenachweis sind ebenfalls kein Abbruchgrund.
Brich die gesamte Bearbeitung nur ab, wenn (a) das erste Bestätigungsfeld nicht
auf "bestätigt" steht oder (b) das zweite Bestätigungsfeld nicht auf "bestätigt"
steht – in beiden Fällen auch dann, wenn das Feld unausgefüllt geblieben ist.
Gib dann nur aus: "Abbruchgrund liegt vor (Buchstabe angeben) –
Bearbeitung an dieser Stelle abgebrochen, Prüfung durch einen Berufsträger
außerhalb des KI-Werkzeugs."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben
   auf und arbeite mit klar benannten Annahmen weiter.
2. Formuliere jede Aussage, die nicht aus den Angaben oder aus einer benannten
   Fundstelle folgt, ausdrücklich als Vermutung.
3. Die Sofortmaßnahmen sind abhakbar (Kästchen ☐), höchstens acht Positionen,
   sortiert danach, was zuerst verloren geht.
4. Höchstens 900 Wörter Fließtext; Tabellen und Listen zählen nicht mit.
5. Führe alle genannten Fundstellen am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit
2. (Teil A – Wegeprüfung): Ampel mit einem Satz Ergebnis, danach Tabelle:
   Weg | zulässig / unzulässig / ungeklärt | Begründung | Fundstelle
3. (Einschränkungen zur Rechtsprechung) – die drei Punkte zu Nds. FG
   2 K 152/25 in einem eigenen Absatz
4. (Zulässige Ersatzwege) – in der Reihenfolge der Erreichbarkeit, je mit dem
   erzeugten Nachweis
5. (Sofortmaßnahmen) – abhakbar
6. (Teil B – Störungsprotokoll) – Tabelle:
   Nr. | Zeitpunkt | Weg | Vorgang | Fehlermeldung im Wortlaut | gesicherter
   Nachweis | Rolle
   danach der zusammenhängende Ablauftext
7. (Lücken in der Beweissicherung) – was fehlt, was heute noch nachholbar ist
8. (Bausteine für einen Wiedereinsetzungsantrag) – ohne Datum, ohne Fristdauer
9. (Fristarten, die im Raum stehen) – ohne Datum und ohne Dauer, je mit
   Rechtsgrundlage und dem Satz "Fristen berechnet und erfasst ein Mensch."
10. (Interne Notiz) – was die Kanzlei organisatorisch ändern muss, damit derselbe
    Fall nicht wiederkommt; nicht an den Mandanten
11. (Zu verifizierende Rechtsgrundlagen): Nr. | Fundstelle | wofür sie steht |
    geprüft von (leer)
12. Was ich nicht sicher weiß
```

## Anwendung

1. **Vor dem Werkzeugeinsatz vom Berufsträger beantworten und in der Handakte vermerken (Vorschaltfragen):** (a) Betrifft der Vorgang ein Straf- oder Bußgeldverfahren, eine Selbstanzeige oder einen Sachverhalt mit Beschlagnahmeschutz? (b) Ist wegen dieses Vorgangs ein Haftungs-, Regress- oder Deckungsverfahren gegen die Kanzlei anhängig oder dem Berufshaftpflichtversicherer angezeigt? Ist eine der beiden Fragen mit ja zu beantworten, bleibt der Vorgang vollständig außerhalb des KI-Werkzeugs (Zone Rot in `DATENSCHUTZ.md`), und die Wegeprüfung erfolgt am Gesetzestext. Nur wenn beide Fragen dem Einsatz nicht entgegenstehen, wird das zweite Bestätigungsfeld im Prompt auf „bestätigt" gesetzt.
1a. **Verfügbarkeit vor dem Ausfüllen feststellen** und im Feld „Woran das festgemacht wurde" notieren: Gibt es in Mein ELSTER oder im Kanzleiprogramm ein Formular oder einen Übermittlungsauftrag für genau diese Eingabeart bei genau dieser Behörde? Wurde diese Eingabeart in der Kanzlei bereits über ELSTER oder ERiC übermittelt? Liegt eine Störungsmeldung vor, die die Verfügbarkeit nur vorübergehend aufhebt? Eine vorübergehende Störung beseitigt die Verfügbarkeit nicht – sie ist ein Fall für Teil B, nicht für die Wegeprüfung.
2. Die Wegeprüfung läuft **vor** dem Absenden, nicht danach. Bei Rot wird nicht gesendet, sondern der Ersatzweg gewählt – die unzulässige Übermittlung lässt sich nachträglich nicht heilen, weil sie mangels Zugangseröffnung nicht als zugegangen gilt.
3. Bei einer Störung zuerst sichern, dann probieren: Bildschirmfoto mit sichtbarer Uhrzeit, Fehlermeldung im Wortlaut, Protokolldatei des Programms, Statusmeldung der Finanzverwaltung oder des Herstellers als Bildschirmfoto. Nach dem Neustart ist die Meldung weg, und was nicht gesichert ist, ist für die Glaubhaftmachung verloren.
4. Parallel zum weiteren Versuch den Ersatzweg vorbereiten: Telefax mit Sendebericht, Post mit Einlieferungsbeleg. Wer nur wiederholt auf „Senden" drückt, verliert die Zeit, die für den zulässigen Ersatzweg noch da war.
5. Fehlermeldung vor dem Einfügen von Steuernummer, Ordnungsmerkmalen und Zertifikatsangaben befreien. Diese Bestandteile werden entfernt, nicht durch Sternchen ersetzt.
6. Ergebnis in die Handakte: Störungsprotokoll, Bildschirmfotos und Sendenachweis gehören in dieselbe Ablage wie der Schriftsatz, nicht in ein persönliches Postfach.

## Qualitätssicherung

- **Vier-Augen-Prinzip bei jeder fristwahrenden Eingabe:** Eine Person wählt den Weg und sendet, eine zweite Person prüft anhand des Sendenachweises, dass die Eingabe den richtigen Empfänger auf einem zulässigen Weg erreicht hat, und zeichnet ab. **Die Frist selbst wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten anhand des Ausgangsdokuments nachgeprüft** – bei Rechtsbehelfsfristen ausnahmslos. Kein Datum und keine Fristdauer aus dem Modell übernehmen.
- **Ausgangskontrolle mit Sendenachweis.** Die Frist wird erst gelöscht, wenn der Nachweis vorliegt und geprüft ist – Übermittlungsprotokoll, Sendebericht oder Einlieferungsbeleg, nicht der Bildschirmeindruck „ist raus". Verfahren, Zuständigkeit und Vertretung regelt das Fristen- und Wiedervorlagekonzept (Prompt 35); dieser Prompt liefert nur den Wegenachweis für den Einzelfall.
- **Freigabe durch einen Berufsträger** für die Entscheidung über den Weg, für jeden Wiedereinsetzungsantrag und für jede Erklärung gegenüber der Finanzbehörde (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Prüfen, ob der Text irgendwo § 87a Abs. 1 Satz 2 AO als Zugangsregelung bezeichnet.** Das ist der häufigste Fehler zu dieser Norm: Satz 2 beschränkt den zulässigen Weg, der Zugangszeitpunkt steht seit dem 06.12.2024 in Satz 3 (für [JAHR] verifizieren).
- **Prüfen, ob der Text eine höchstrichterliche Entscheidung behauptet.** Zu dieser Frage liegt nur eine finanzgerichtliche Entscheidung vor (Nds. FG vom 12.02.2026 – 2 K 152/25), deren Rechtskraft nicht belegt ist; eine BFH-Entscheidung gibt es nicht.
- **Prüfen, ob der Text eine Ersatzeinreichung wegen technischer Störung aus der Abgabenordnung ableitet.** Die AO enthält dazu keine Regelung; § 52d Sätze 3 und 4 FGO gilt für das finanzgerichtliche Verfahren, nicht für das Besteuerungsverfahren (für [JAHR] verifizieren).
- **Prüfen, ob die Rückausnahme des § 87a Abs. 1 Satz 2 Halbsatz 2 AO eng geblieben ist.** Sie greift nur, wenn gerade die Übermittlung mit qualifizierter elektronischer Signatur oder über das besondere elektronische Behördenpostfach gesetzlich vorgeschrieben ist – nicht schon deshalb, weil eine Erklärung elektronisch abzugeben ist (für [JAHR] verifizieren).
- **Prüfen, ob die beiden Regime auseinandergehalten sind.** Gegenüber der Finanzbehörde sind beA und beSt gesperrt (§ 87a Abs. 1 Satz 2 AO); gegenüber dem Finanzgericht besteht umgekehrt die Nutzungspflicht nach § 52d Sätze 1 und 2 FGO in Verbindung mit § 52a Abs. 4 Satz 1 Nr. 1 FGO, und Post oder Telefax wahren dort die Frist nicht (für [JAHR] verifizieren). Eine Ausgabe, die Post und Telefax pauschal als zulässig bezeichnet, ist an dieser Stelle falsch.
- **Prüfen, ob Papier als Ersatzweg für eine pflichtelektronische Erklärung angeboten wird.** Das ist falsch; § 150 Abs. 8 AO setzt wirtschaftliche oder persönliche Unzumutbarkeit voraus und erfasst keine vorübergehende Störung (für [JAHR] verifizieren).
- **Prüfen, ob § 109 Abs. 1 Satz 2 AO und § 110 AO auseinandergehalten sind.** Die rückwirkende Verlängerung erfasst Steuererklärungsfristen und behördlich gesetzte Fristen, nicht die Rechtsbehelfsfrist. Diese Verwechslung ist in vergleichbaren Vorlagen bereits vorgekommen.
- **Rechtsstand prüfen an:** § 87a AO, § 110 AO, § 109 AO, § 150 Abs. 8 AO, § 355 AO, § 356 AO und § 357 AO im amtlichen Volltext (gesetze-im-internet.de), am Anwendungserlass zur Abgabenordnung zu § 87a (BMF vom 10.12.2024), am Volltext des Urteils des Nds. FG vom 12.02.2026 – 2 K 152/25 einschließlich der Frage einer Nichtzulassungsbeschwerde sowie an § 52d und § 52a Abs. 4 FGO in Verbindung mit § 62 Abs. 2 FGO.

## Varianten

- **Reine Vorabprüfung:** „Erzeuge nur Teil A als Kurzentscheid: Ampel, ein Satz Begründung, zulässige Ersatzwege. Höchstens 150 Wörter."
- **Kanzleiaushang:** „Verdichte die Wegeprüfung auf eine Seite: welcher Weg für welchen Empfänger, was bei Störung in den ersten fünfzehn Minuten zu tun ist, wer entscheidet."
- **Nachträgliche Aufarbeitung:** „Erzeuge aus dem Störungsprotokoll eine Chronologie für die Handakte, ohne Bewertung und ohne Rechtsausführungen."
- **Postfachbestand prüfen:** „Erzeuge eine Arbeitsliste, mit der die Kanzlei prüft, welche Eingaben in der Vergangenheit über beA oder beSt an Finanzbehörden gegangen sind, gegliedert nach Empfängerart und Fristbindung, mit Spalte für die Vorlage an den Berufsträger."
- **Schulungsfall:** „Formuliere den Sachverhalt als anonymisierten Übungsfall für die Teambesprechung, mit drei Entscheidungspunkten und ohne Lösung."
