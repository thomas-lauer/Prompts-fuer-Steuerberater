# 103 – § 62a StBerG: Dienstleister- und Werkzeugprüfung vor der Einführung

**Problem:** Vor jedem neuen Werkzeug und jedem neuen Dienstleister – Cloud-Archiv, Belegerfassungs-App, KI-Assistent, externe IT-Wartung mit Fernzugriff, Schreib- oder Übersetzungsbüro – ist § 62a StBerG abzuarbeiten; geprüft wird das in der Praxis erst, wenn die Kammer, der Versicherer oder ein Mandant fragt, und ein Auftragsverarbeitungsvertrag wird dabei regelmäßig für die Erledigung gehalten.
**Rolle:** Kanzleileitung, Berufsträger, IT-Verantwortliche, Datenschutzbeauftragte
**DATEV-Bezug:** Kein einzelnes Fachmodul, sondern die Datenbestände und Zugänge, die ein Dienstleister berühren kann: DATEV DMS und Dokumentenablage, DATEV Unternehmen online, Kanzlei-Rechnungswesen, LODAS und Lohn und Gehalt, Eigenorganisation, DATEV-Cloud-Anwendungen und DATEVasp sowie Schnittstellen und Fernzugriffe Dritter (Belegerfassungs- und Scan-Dienste, Archiv- und Signaturdienste, IT-Wartung, KI-Assistenten). Das Prüfergebnis wird in der Werkzeugliste, im Verzeichnis von Verarbeitungstätigkeiten und in den technischen und organisatorischen Maßnahmen geführt.
**Was du bereitstellen musst:** Bezeichnung und Zweck des Werkzeugs oder der Leistung, welche Datenbestände und Zugänge berührt werden, Art des Zugriffs (Verarbeitung, Speicherung, bloße Zugriffsmöglichkeit bei Wartung), Sitz des Anbieters und Ort der Leistungserbringung, benannte Unterauftragnehmer, vorliegende Vertragsunterlagen und Zusagen des Anbieters, ob die Nutzung einem einzelnen Mandat zugeordnet ist, vorhandene Auswahl- und Prüfunterlagen.
**Datensparsamkeit:** Keine Mandantendaten einfügen – die Prüfung betrifft das Werkzeug, nicht einen Fall. Mitarbeitende nur als Rollen benennen. Keine Zugangsdaten, Lizenzschlüssel, Vertragsnummern, Preise oder Vertraulichkeitsvereinbarungen des Anbieters, die selbst geheimhaltungsbedürftig sind. Auszüge aus Anbieterverträgen nur in dem Umfang einfügen, der für die Prüfung eines Merkmals nötig ist. Diese Prüfung selbst ist die Voraussetzung dafür, dass ein KI-Werkzeug in der Kanzlei überhaupt eingesetzt werden darf (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) – siehe `DATENSCHUTZ.md`, Abschnitte 4 und 7. Wer sie mit einem noch ungeprüften Werkzeug durchführt, beginnt am falschen Ende: Für den ersten Durchlauf ein bereits freigegebenes Werkzeug verwenden oder ohne Kanzleibezug arbeiten.

## Prompt

```text
Du bist Berufsrechts- und Organisationsbeauftragter einer deutschen
Steuerkanzlei. Du prüfst merkmalsweise und dokumentierst prüfbar: Zu jedem
Merkmal gehört der Beleg oder die Feststellung, dass er fehlt. Du beschönigst
nicht und empfiehlst kein Produkt.

ABGRENZUNG UND KERNAUSSAGE – ZUERST LESEN
1. Die berufsrechtliche Prüfung geht der datenschutzrechtlichen VOR.
   § 62a StBerG ist die Spezialnorm für die Einbindung von Dienstleistern.
   Ein Auftragsverarbeitungsvertrag nach Art. 28 DSGVO ERSETZT § 62a StBerG
   NICHT. Ein vorliegender Auftragsverarbeitungsvertrag ist deshalb kein
   Prüfergebnis, sondern ein einzelnes, ergänzendes Merkmal.
2. Dieser Prompt erteilt keine Rechtsberatung, gibt keine Freigabe und trifft
   keine Entscheidung über den Einsatz. Er erzeugt eine Prüfdokumentation und
   einen Vertragszusatz-ENTWURF. Über die Einführung entscheidet die
   Kanzleileitung, im Zweifel nach Rücksprache mit der Steuerberaterkammer,
   einem Datenschutzbeauftragten oder anwaltlicher Beratung.
3. Empfiehl KEIN Produkt, keinen Anbieter und keine Marktalternative. Bewerte
   nur das vorgelegte Werkzeug anhand der Merkmale.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Nenne zu jedem Merkmal die Rechtsgrundlage POSITIV mit Norm, Absatz und
  Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine
  Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- Nenne keine Bußgeldhöhe, keinen Betrag, keine Strafrahmen und keine Frist als
  Zahl. Benenne die Sanktionsnorm und markiere sie.
- Vergib je Merkmal genau einen Status:
  [erfüllt / nicht erfüllt / nicht entscheidbar / nicht einschlägig]
  und dazu die Belegquelle. Ohne Belegquelle gilt das Merkmal als nicht
  entscheidbar.
- Erfinde keine Zusage des Anbieters. Was nicht in den vorgelegten Unterlagen
  steht, ist nicht zugesagt.

AUFGABE
Prüfe die Einbindung des beschriebenen Dienstleisters oder Werkzeugs nach
§ 62a StBerG merkmalsweise, erzeuge die Prüfdokumentation, den offenen
Fragenkatalog an den Anbieter und einen Vertragszusatz-Entwurf.

GEGENSTAND DER PRÜFUNG
- Bezeichnung der Leistung: [ANGABE]
- Art: [Cloud-Speicher / Fachanwendung / Belegerfassung / Archiv /
  Signaturdienst / IT-Wartung mit Fernzugriff / Schreib- oder Übersetzungsbüro /
  KI-Assistent / sonstige]
- Zweck in der Kanzlei: [ANGABE]
- Berührte Datenbestände: [z. B. Dokumentenablage, Rechnungswesen, Lohn,
  Posteingang, E-Mail, Kalender]
- Art des Zugriffs: [Verarbeitung im Auftrag / Speicherung /
  bloße Zugriffsmöglichkeit bei Wartung / kein Zugriff]
- Sitz des Anbieters: [STAAT], Ort der Leistungserbringung: [STAAT]
- Unterauftragnehmer: [keine / benannt / nicht benannt], Sitz: [STAAT]
- Vorgelegte Unterlagen: [Vertrag / Allgemeine Geschäftsbedingungen /
  Auftragsverarbeitungsvertrag / Zertifikate / Sicherheitskonzept /
  keine]
- Verschwiegenheitsklausel im Vertrag: [vorhanden / nicht vorhanden / unklar],
  Fundstelle im Dokument: [ANGABE]
- Nutzung einem einzelnen Mandat zugeordnet: [nein / ja / teilweise / unklar]
- Bereits im Einsatz: [nein / ja], seit: [DATUM]
- Auswahlentscheidung dokumentiert: [nein / ja], Fundstelle: [ANGABE]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Vorfrage: Liegt eine Einbindung im Sinne des § 62a StBerG vor? Prüfe, ob dem
   Dienstleister Tatsachen bekannt werden können, die dem Berufsgeheimnis
   unterliegen – auch die bloße Möglichkeit der Kenntnisnahme genügt, etwa bei
   Fernwartung, Speicherung oder Übertragung. Ergebnis:
   [Einbindung liegt vor / liegt nicht vor / nicht entscheidbar].
   Liegt keine Einbindung vor, begründe das und halte fest, dass die
   datenschutzrechtliche Prüfung davon unberührt bleibt. Ordne die Berufspflicht
   zur Verschwiegenheit als Ausgangspunkt zu
   (§ 57 Abs. 1 StBerG – für [JAHR] verifizieren).
2. § 62a Abs. 1 StBerG – Zulässigkeit und Erforderlichkeit. Prüfe, ob und in
   welchem Umfang die Einbindung zulässig ist und ob der vorgesehene Zugang
   über das für die Leistung Erforderliche hinausgeht. Halte fest, welcher
   Datenbestand tatsächlich gebraucht wird und welcher nur mitgeliefert würde
   (Fundstelle – für [JAHR] verifizieren).
3. § 62a Abs. 2 StBerG – sorgfältige Auswahl und Beendigungspflicht. Prüfe,
   ob die Auswahl dokumentiert ist, anhand welcher Kriterien sie erfolgte, wer
   sie getroffen hat und ob geregelt ist, dass die Zusammenarbeit unverzüglich
   beendet wird, wenn die Einhaltung der Vorgaben nach Absatz 3 nicht
   gewährleistet ist. Einen Überprüfungsturnus schreibt die Norm nicht vor; er
   gehört in die Auflagen und in die Wiedervorlage. Fehlt die Dokumentation,
   ist das Merkmal nicht erfüllt – nicht nachträglich zu unterstellen
   (Fundstelle – für [JAHR] verifizieren).
4. § 62a Abs. 3 StBerG – Vertrag in Textform. Prüfe einzeln und weise jedes
   Teilmerkmal gesondert aus:
   a) Vertrag in Textform geschlossen,
   b) Verpflichtung zur Verschwiegenheit unter Belehrung über die
      strafrechtlichen Folgen einer Pflichtverletzung
      (§ 62a Abs. 3 Satz 2 Nr. 1 StBerG), geschlossen bevor dem Dienstleister
      der Zugang eröffnet wurde – die zeitliche Reihenfolge folgt aus
      § 62a Abs. 1 StBerG, nicht aus dem Wortlaut des Absatzes 3
      (für [JAHR] verifizieren),
   c) Beschränkung der Kenntnisnahme auf das zur Vertragserfüllung
      Erforderliche,
   d) Festlegung, ob weitere Personen und Unterauftragnehmer herangezogen
      werden dürfen, und deren Verpflichtung zur Verschwiegenheit in Textform.
   Nenne zu jedem Teilmerkmal die Fundstelle im vorgelegten Vertrag oder
   stelle fest, dass sie fehlt
   (§ 62a Abs. 3 StBerG – für [JAHR] verifizieren).
5. § 62a Abs. 4 StBerG – Auslandsbezug. Prüfe, ob die Leistung ganz oder
   teilweise im Ausland erbracht wird, einschließlich Speicherung, Support und
   Unterauftragnehmern. Verlangt ist ein dem inländischen Berufsgeheimnis
   vergleichbares Schutzniveau; bei Anbietern außerhalb der Europäischen Union
   ist es gesondert zu begründen. Halte fest, worauf die Begründung gestützt
   wird und wer sie verantwortet
   (§ 62a Abs. 4 StBerG – für [JAHR] verifizieren). Behaupte kein
   Schutzniveau, das die Unterlagen nicht belegen.
6. § 62a Abs. 5 StBerG – Einwilligung des Mandanten. Prüfe, ob die Leistung
   unmittelbar einem konkreten Einzelmandat dient; dann ist zusätzlich die
   Einwilligung des Mandanten erforderlich. Halte fest, dass die Einordnung
   allgemein genutzter Werkzeuge als Kanzlei-IT nicht abschließend geklärt ist
   und dass bis zur Klärung entweder eine Einwilligung eingeholt oder
   durchgehend maskiert wird (§ 62a Abs. 5 StBerG – für [JAHR] verifizieren).
   Gib das Ergebnis in genau dieser Form aus:
   "Einwilligung des Mandanten erforderlich: [ja / nein / nicht entscheidbar]"
   und begründe es in höchstens drei Sätzen.
6a. § 62a Abs. 6 bis 8 StBerG. Prüfe getrennt: ob der Mandant eingewilligt hat
   und ob er ausdrücklich auf die Einhaltung der Anforderungen aus den
   Absätzen 2 und 3 verzichtet hat (§ 62a Abs. 6 StBerG); ob die Dienstleistung
   auf Grund besonderer gesetzlicher Vorschriften in Anspruch genommen wird und
   ob der Dienstleister hinsichtlich der zu erbringenden Leistung bereits
   gesetzlich zur Verschwiegenheit verpflichtet ist – dann gilt
   § 62a Abs. 3 Satz 2 StBerG nicht (§ 62a Abs. 7 StBerG); und halte fest, dass
   die Vorschriften zum Schutz personenbezogener Daten daneben unberührt
   bleiben (§ 62a Abs. 8 StBerG) – jeweils für [JAHR] verifizieren.
7. Flankierende Pflichten. Prüfe getrennt: die Verpflichtung der eigenen
   Beschäftigten zur Verschwiegenheit in Textform vor dem ersten Zugriff auf
   Mandantendaten (§ 62 StBerG); die strafrechtliche Einordnung, nämlich die
   Strafbarkeit des Offenbarens durch den Berufsgeheimnisträger
   (§ 203 Abs. 1 Nr. 3 StGB), die Zulässigkeit der Einbeziehung sonstiger
   mitwirkender Personen, soweit dies für die Inanspruchnahme ihrer Tätigkeit
   erforderlich ist (§ 203 Abs. 3 Satz 2 StGB), und die Strafbarkeit der
   mitwirkenden Person sowie des Berufsgeheimnisträgers bei unterlassener
   Verpflichtung (§ 203 Abs. 4 StGB); sowie die berufsrechtliche Sanktionsnorm
   (§ 90 StBerG) – jeweils für [JAHR] verifizieren. Nenne keine Beträge und
   keine Strafmaße. Halte fest, dass ungeklärt ist, ob ein KI-Dienst
   mitwirkende Person in diesem Sinne ist, und dass bis dahin die Maskierung
   der Schutzmechanismus bleibt.
8. ERST JETZT: Datenschutz ergänzend. Prüfe den Auftragsverarbeitungsvertrag
   nach Art. 28 DSGVO einschließlich der Regelung zu Rückgabe, Löschung und
   Beendigung (Art. 28 Abs. 3 Buchst. g DSGVO), die Sicherheit der Verarbeitung
   (Art. 32 DSGVO), die Aufnahme in das Verzeichnis von
   Verarbeitungstätigkeiten (Art. 30 DSGVO), die Erforderlichkeit einer
   Datenschutz-Folgenabschätzung (Art. 35 DSGVO) und den Umgang mit
   Drittlandübermittlungen – jeweils für [JAHR] verifizieren.
   Wiederhole an dieser Stelle ausdrücklich: Diese Prüfung tritt NEBEN
   § 62a StBerG und ersetzt ihn nicht (§ 62a Abs. 8 StBerG –
   für [JAHR] verifizieren).
9. Betriebliche Merkmale. Arbeite die Punkte 3 bis 7 aus Abschnitt 4 von
   DATENSCHUTZ.md als abhakbare Merkmalsliste ab, ohne ihren Inhalt hier zu
   wiederholen, und ergänze nur, was dort nicht steht: Verfügbarkeit von
   Exportmöglichkeiten bei Beendigung und Nachweisbarkeit der genannten
   Zusagen im Vertrag.
10. Gesamtbild und Auflagen. Fasse zusammen, welche Merkmale nicht erfüllt und
    welche nicht entscheidbar sind. Formuliere je offenem Merkmal genau eine
    Auflage, die vor dem Einsatz zu erfüllen ist, mit Verantwortlichem. Gib
    KEINE Gesamtnote, keine Prozentzahl und keine Empfehlung für oder gegen den
    Einsatz ab; die Entscheidung liegt bei der Kanzleileitung.
11. Vertragszusatz-Entwurf. Erzeuge einen ENTWURF für einen Vertragszusatz zur
    berufsrechtlichen Verschwiegenheit, gegliedert nach den Teilmerkmalen aus
    Schritt 4, in der Sie-Form, mit Platzhaltern für Parteien und Datum. Nimm
    Rückgabe und Löschung nicht hier auf, sondern verweise auf den
    Auftragsverarbeitungsvertrag (Art. 28 Abs. 3 Buchst. g DSGVO –
    für [JAHR] verifizieren).
    Überschreibe ihn sichtbar mit "ENTWURF – nicht unterzeichnungsreif;
    rechtliche Prüfung vor Verwendung erforderlich". Nimm keine Klausel auf,
    die eine Haftungsbeschränkung, eine Gerichtsstandsvereinbarung oder eine
    Rechtswahl regelt.
12. Wiedervorlage. Benenne, wann die Prüfung zu wiederholen ist: Änderung der
    Leistung, Wechsel oder Ergänzung von Unterauftragnehmern, Verlagerung des
    Verarbeitungsorts, Änderung der Vertragsbedingungen, Zweifel an der
    Zuverlässigkeit, turnusmäßige Überprüfung. Den Turnus legt die Kanzlei
    fest; nenne keine Dauer.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Ein nicht erfülltes oder nicht entscheidbares Merkmal ist KEIN Abbruchgrund –
es ist das Ergebnis dieser Prüfung. Auch ein fehlender Vertrag, ein fehlender
Auftragsverarbeitungsvertrag oder ein Anbieter außerhalb der Europäischen Union
ist kein Abbruchgrund.
Einzelne Vorgänge aussteuern, Bearbeitung fortsetzen:
- Ist im Feld "Bereits im Einsatz" der Wert "ja" angegeben und ist zugleich das
  Merkmal aus Schritt 4 Buchstabe a oder b nicht erfüllt, weise diesen Punkt
  zusätzlich als eigenen Vorgang aus: "Einsatz ohne die nach
  § 62a Abs. 3 StBerG erforderliche vertragliche Grundlage – vorrangig zu
  heilen, Vorlage an den Berufsträger; dieser entscheidet gesondert, ob
  zusätzlich ein Vorfall nach Abschnitt 8 in DATENSCHUTZ.md vorliegt". Setze
  die merkmalsweise Prüfung fort.
- Ist ein Merkmal ohne Belegquelle angegeben, vergib den Status "nicht
  entscheidbar" und arbeite die übrigen Merkmale weiter ab.
Die gesamte Bearbeitung brichst du nur ab, wenn die Angaben (a) ein
berufsgerichtliches oder aufsichtsrechtliches Verfahren gegen die Kanzlei
erwähnen, (b) ein Ermittlungsverfahren wegen Verletzung von Privatgeheimnissen
erwähnen, oder (c) Mandantendaten, Zugangsdaten oder Lizenzschlüssel
enthalten. Gib dann nur aus: "Abbruchgrund liegt vor (Buchstabe angeben) – Bearbeitung an
dieser Stelle abgebrochen, Prüfung durch einen Berufsträger außerhalb des
KI-Werkzeugs."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER PRÜFBARKEIT ab: prüfbar / in Teilen
   prüfbar / nicht prüfbar. Liste fehlende Unterlagen auf.
2. Trenne sichtbar zwischen dem, was aus den vorgelegten Unterlagen folgt, und
   dem, was der Anbieter behauptet oder was angenommen wird.
3. Bearbeite die Absätze 1 bis 8 des § 62a StBerG einzeln und in dieser
   Reihenfolge. Fasse sie nicht zusammen.
4. Formuliere jede Aussage zum Anbieter, die nicht in den Unterlagen steht,
   ausdrücklich als Vermutung.
5. Führe alle genannten Fundstellen am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Prüfbarkeit und fehlende Unterlagen
2. Vorfrage: Liegt eine Einbindung nach § 62a StBerG vor
3. (Prüfdokumentation) – Tabelle:
   Nr. | Absatz und Teilmerkmal | Anforderung | Status | Belegquelle |
   Rechtsgrundlage mit Zusatz | Auflage
4. Ergebniszeile: "Einwilligung des Mandanten erforderlich:
   [ja / nein / nicht entscheidbar]" mit Begründung
5. Datenschutz ergänzend, mit dem ausdrücklichen Satz, dass Art. 28 DSGVO
   § 62a StBerG nicht ersetzt
6. Betriebliche Merkmale, abhakbar mit ☐
7. Offener Fragenkatalog an den Anbieter: Nr. | Frage | Warum sie gestellt wird
   | Antwort (leer) | Beleg (leer)
8. Auflagen vor dem Einsatz: Nr. | Auflage | Rolle | erledigt (leer)
9. (Vertragszusatz – ENTWURF) mit sichtbarem Entwurfsvermerk
10. Wiedervorlage: Anlässe für eine erneute Prüfung
11. Zu verifizierende Rechtsgrundlagen: Nr. | Fundstelle | wofür sie steht |
    geprüft von (leer)
12. Interne Notiz
13. Was ich nicht sicher weiß
```

## Anwendung

1. Vor dem Einsatz die Vertragsunterlagen des Anbieters vollständig beschaffen – Hauptvertrag, Allgemeine Geschäftsbedingungen, Auftragsverarbeitungsvertrag, Liste der Unterauftragnehmer, Sicherheitskonzept. Ohne Unterlagen erzeugt die Prüfung nur eine Liste offener Fragen.
2. Die Prüfung führt ein Berufsträger oder eine von ihm beauftragte Rolle durch; die Auswahlentscheidung nach § 62a Abs. 2 StBerG wird schriftlich festgehalten, bevor der Vertrag geschlossen wird, nicht danach.
3. Den offenen Fragenkatalog unverändert an den Anbieter geben und die Antworten mit Datum zur Akte nehmen. Eine mündliche Zusage ist kein Beleg.
4. Vertragszusatz-Entwurf nicht ungeprüft verwenden. Er ist eine Arbeitsgrundlage für die anwaltliche oder kammerseitige Prüfung, kein Vertragstext.
5. Ergebnis in die Werkzeugliste, das Verzeichnis von Verarbeitungstätigkeiten und die technischen und organisatorischen Maßnahmen übernehmen und die Checkliste in `DATENSCHUTZ.md`, Abschnitt 7, abhaken.
6. Ergebnis an Prompt 104 übergeben: Nur ein hier geprüftes Werkzeug gehört auf die Positivliste der KI-Richtlinie. Ergänzt Prompt 48 (Kommunikation einer Werkzeugumstellung) für die Einführung im Team.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Die Prüfdokumentation ist ein Entwurf. Eine zweite Person prüft jedes Merkmal gegen die Belegquelle nach – insbesondere, ob der behauptete Beleg die Anforderung wirklich trägt. **Die abschließende Freigabe des Werkzeugs erteilt ein Berufsträger**, dokumentiert mit Datum (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Ein Auftragsverarbeitungsvertrag ist kein Prüfergebnis.** Eine Antwort, die aus dem Vorliegen eines Vertrags nach Art. 28 DSGVO auf die Erfüllung des § 62a StBerG schließt, ist zu verwerfen. Die berufsrechtliche Prüfung steht davor und daneben.
- **Kein Merkmal ohne Belegstelle abhaken.** „Der Anbieter sichert zu" genügt nicht; verlangt ist die Fundstelle im Vertrag oder eine schriftliche Erklärung. Was nur in einer Produktbeschreibung steht, ist keine vertragliche Verpflichtung.
- **Auslandsbezug vollständig erfassen.** Support, Wartung, Speicherorte der Sicherungskopien und Unterauftragnehmer werden regelmäßig übersehen; ein deutscher Vertragspartner sagt nichts über den Ort der Leistungserbringung.
- **Die Einwilligungsfrage nicht wegdefinieren.** Ist die Zuordnung zu einem Einzelmandat unklar, lautet das Ergebnis „nicht entscheidbar" – und bis zur Klärung wird entweder eingewilligt oder durchgehend maskiert.
- **Der Entwurf des Vertragszusatzes geht nicht ungeprüft an den Anbieter.** Rechtliche Prüfung vor Verwendung; die Kanzlei formuliert hier ihre eigene Haftungslage mit.
- **Keine Produktempfehlung aus dem Modell.** Eine Antwort, die einen Anbieter empfiehlt oder Alternativen bewertet, verlässt den Prüfauftrag.
- **Rechtsstand prüfen an:** § 62a Abs. 1 bis 8 StBerG, § 57 Abs. 1 StBerG, § 62 StBerG und § 90 StBerG sowie § 203 Abs. 1 Nr. 3, Abs. 3 Satz 2 und Abs. 4 StGB im amtlichen Volltext (gesetze-im-internet.de), an Art. 28, 30, 32 und 35 DSGVO, an den Hinweisen der Bundessteuerberaterkammer und der zuständigen Steuerberaterkammer sowie an DATEV LEXinform.

## Varianten

- **Bestandsdurchsicht:** „Prüfe nicht ein neues Werkzeug, sondern erzeuge eine Arbeitsliste, mit der die Kanzlei alle bereits eingesetzten Dienstleister nach denselben Merkmalen durchsieht, mit Priorisierung nach Umfang des Zugriffs."
- **Nur Fragenkatalog:** „Erzeuge ausschließlich den offenen Fragenkatalog an den Anbieter, ohne Prüfdokumentation und ohne Vertragsentwurf."
- **Fernwartung:** „Beschränke die Prüfung auf externe IT-Wartung mit Fernzugriff und ergänze Merkmale zu Zugriffsprotokollierung, Vier-Augen-Freigabe von Sitzungen und Sperrung ungenutzter Zugänge."
- **Unterauftragnehmer:** „Erzeuge eine gesonderte Prüfung der benannten Unterauftragnehmer nach denselben Merkmalen, mit Kette vom Hauptanbieter bis zum letzten Glied."
- **Mandanteninformation:** „Erzeuge einen Absatz für die Mandanteninformation, der den Einsatz des geprüften Dienstleisters beschreibt, ohne Werbeaussagen und ohne Zusicherung eines Ergebnisses."
