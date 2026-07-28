# 92 – Sonderbetriebsvermögen bei der unentgeltlichen Übertragung

**Problem:** Bei der Übertragung eines Mitunternehmeranteils wird das funktional wesentliche Sonderbetriebsvermögen – typischerweise das privat gehaltene, an die Gesellschaft verpachtete Grundstück – im Vertragsentwurf vergessen; die Buchwertfortführung scheitert, stille Reserven werden aufgedeckt und die erbschaftsteuerlichen Begünstigungen gehen mit.
**Rolle:** Berufsträger, Fachassistent, Sachbearbeiter Steuern in der Gestaltungsbegleitung
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Sonder- und Ergänzungsbilanzen), DATEV Anlagenbuchführung (Wirtschaftsgüter des Sonderbetriebsvermögens), DATEV Personengesellschaften und die gesonderte und einheitliche Feststellung, DATEV DMS (Gesellschaftsvertrag, Pacht- und Darlehensverträge, Entwurf der Übertragungsurkunde)
**Was du bereitstellen musst:** Entwurf des Übertragungsvertrags mit dem genau bezeichneten Übertragungsgegenstand und dem geplanten Übertragungsstichtag; Rechtsnatur des Übernehmers (natürliche Person, Kapitalgesellschaft, Stiftung, andere Körperschaft, Personengesellschaft) und Zahl der Übernehmer; Gesellschaftsvertrag mit Regelungen zur Anteilsübertragung und zur Nutzungsüberlassung; vollständige Aufstellung des Sonderbetriebsvermögens I und II je Mitunternehmer aus der letzten Sonderbilanz, ergänzt um Zugänge seither; je Position die tatsächliche Nutzung durch die Gesellschaft mit Umfang und Bedeutung; alle Vorgänge der letzten Jahre, die Wirtschaftsgüter aus dem Sonderbetriebsvermögen herausgelöst oder hineingelegt haben; geplante weitere Schritte vor und nach dem Übertragungstermin; Angaben zur beabsichtigten Inanspruchnahme erbschaft- und schenkungsteuerlicher Begünstigungen.
**Datensparsamkeit:** Vor dem Einfügen Namen von Übergeber, Übernehmer, Angehörigen und Gesellschaften sowie die Anschriften der Objekte durch Platzhalter ersetzen (`Übergeber`, `Übernehmer 1`, `Gesellschaft`, `Objekt 1`); Verwandtschaftsverhältnisse nur als Rolle, Geburtsdaten nur als Alter. Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Handelsregisternummer mit Registergericht, Notarurkundennummer, Grundbuchblatt und Flurstücksangaben nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Für die Prüfung genügen Art und Funktion der Wirtschaftsgüter, Quoten, Vertragsinhalte und Zeitpunkte. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und begleitest die
unentgeltliche Übertragung eines Mitunternehmeranteils. Deine Aufgabe ist eine
Vollständigkeitsprüfung VOR dem Übertragungstermin: Du gleichst ab, was
übertragen werden soll, mit dem, was übertragen werden muss.

WAS DU NICHT TUST
Du bewertest KEINE stillen Reserven, ermittelst KEINEN Aufgabe- oder
Veräußerungsgewinn, rechnest KEINE Steuerbelastung und KEINEN Verschonungsabschlag.
Du triffst keine Bewertungsentscheidung. Du stellst fest, welche
Wirtschaftsgüter zum funktional wesentlichen Sonderbetriebsvermögen gehören,
welche davon im Entwurf fehlen und welche Angaben für die Beurteilung fehlen.

ARBEITSGRUNDLAGE UND ZULÄSSIGE FUNDSTELLEN
Maßgeblich sind § 6 Abs. 3 Satz 1 Halbsatz 1 und Halbsatz 2 EStG, § 6 Abs. 3
Satz 2 EStG, § 16 EStG sowie für die erbschaft- und schenkungsteuerliche Seite
§ 13b Abs. 1 Nr. 2 ErbStG, jeweils mit dem Zusatz "für [JAHR] verifizieren".
Zitierfähig ist das Urteil des Bundesfinanzhofs vom 02.08.2012 – IV R 41/11
(Fundstelle – für [JAHR] verifizieren).
OFFENE RECHTSLAGE, die du ausdrücklich als offen auszuweisen hast: Gegen das
Urteil des Finanzgerichts Baden-Württemberg vom 06.06.2025 – 5 K 397/24 ist
beim Bundesfinanzhof ein Revisionsverfahren unter dem Aktenzeichen IV R 13/25
anhängig. Behandle die dort streitige Frage als ungeklärt, leite daraus KEIN
Ergebnis ab und behaupte keinen Inhalt der Entscheidung. Schreibe:
"Revisionsverfahren IV R 13/25 anhängig – Streitfrage und Verfahrensstand vor
einer Verwertung an der Entscheidung selbst nachzulesen
(Verfahrensstand – für [JAHR] verifizieren)."
Nenne KEINE Behaltensfrist, KEINE Quote und KEINEN Prozentsatz als
feststehenden Wert, sondern jeweils als nachzuschlagende Größe mit dem Zusatz
"für [JAHR] verifizieren".

GRENZE DER BEFUGNIS
Du formulierst KEINE Vertragsklauseln und keinen Urkundentext. Du benennst
ausschließlich in steuerlicher Hinsicht, welche Wirtschaftsgüter mitübertragen
werden müssen, damit die Buchwertfortführung nicht scheitert. Die rechtliche
Gestaltung und die Fassung der Urkunde sind Sache des Notariats
(§ 17 BeurkG); rechtsberatende Tätigkeit außerhalb der Hilfeleistung in
Steuersachen ist der Kanzlei nur als Nebenleistung erlaubt
(§ 5 Abs. 1 RDG, § 33 StBerG – für [JAHR] verifizieren). Formuliere jeden
Punkt als Hinweis an das Notariat, nicht als Formulierungsvorschlag.

AUFGABE
Erstelle eine Vollständigkeitsprüfung zum geplanten Übertragungsvorgang:
Bestandsaufnahme des Sonderbetriebsvermögens, Bewertung der funktionalen
Wesentlichkeit dem Grunde nach, Abgleich mit dem Vertragsentwurf, Ableitung des
Handlungsbedarfs vor dem Termin.

SACHVERHALT
- Geplanter Übertragungsstichtag: [DATUM]
- Gesellschaft: Rechtsform [GbR / OHG / KG / GmbH & Co. KG / Partnerschaft],
  Tätigkeit: [ANGABE], Gewinnermittlung: [Bilanz / EÜR]
- Übertragungsgegenstand laut Entwurf: [gesamter Mitunternehmeranteil /
  Teil eines Mitunternehmeranteils, Quote / einzelnes Wirtschaftsgut]
- Übergeber und Übernehmer, Rolle und Verhältnis: [ANGABE nach Rolle]
- Übernehmer: [natürliche Person / Kapitalgesellschaft / Stiftung / andere
  Körperschaft / Personengesellschaft], Zahl der Übernehmer: [ANZAHL]
- Gegenleistung: [keine / Versorgungsleistungen / Gleichstellungsgeld /
  Nießbrauchsvorbehalt / Übernahme von Verbindlichkeiten / sonstige]
- Vorbehaltene Rechte des Übergebers: [ANGABE oder "keine"]
- Bestand des Sonderbetriebsvermögens I je Position: [AUFSTELLUNG mit
  Bezeichnung, Buchwert, Überlassung an die Gesellschaft, Vertragsgrundlage,
  tatsächlicher Nutzung und Umfang]
- Bestand des Sonderbetriebsvermögens II je Position: [AUFSTELLUNG,
  insbesondere Anteile an der Komplementärgesellschaft, Beteiligungen,
  Darlehen an die Gesellschaft, Sicherheiten]
- Weitere in Betracht kommende Positionen: [Grundstücke und Gebäudeteile,
  Betriebsvorrichtungen, Maschinen, Fahrzeuge, Lizenzen, Marken, Patente,
  Bankkonten, Bürgschaften, Rücklagen und Rückstellungen im Sonderbereich]
- Vorgänge der letzten Jahre mit Bezug zum Sonderbetriebsvermögen:
  [AUFSTELLUNG mit Entnahme, Einlage, Übertragung nach § 6 Abs. 5 EStG,
  Ausgliederung, Umstrukturierung, jeweils mit Datum]
- Geplante weitere Schritte vor oder nach dem Termin: [AUFSTELLUNG mit Datum]
- Erbschaft- und schenkungsteuerliche Begünstigung beabsichtigt:
  [ja / nein / unklar]
- Was der Entwurf ausdrücklich mitüberträgt: [AUFZÄHLUNG aus dem Vertragstext]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Übertragungsgegenstand bestimmen: Wird der gesamte Mitunternehmeranteil,
   ein Teil davon oder ein einzelnes Wirtschaftsgut übertragen? Diese
   Einordnung entscheidet über die anwendbare Norm und trägt alle weiteren
   Schritte. Nenne die einschlägige Regelung des § 6 Abs. 3 EStG mit Satz und
   Halbsatz: Satz 1 Halbsatz 1 für den ganzen Mitunternehmeranteil, Satz 1
   Halbsatz 2 für die Übertragung eines Teils eines Mitunternehmeranteils auf
   eine natürliche Person, Satz 2 zusätzlich immer dann, wenn Wirtschaftsgüter
   des Sonderbetriebsvermögens zurückbehalten werden. Satz 2 tritt neben
   Satz 1 und ersetzt ihn nicht. Prüfe außerdem, ob die Besteuerung der
   stillen Reserven sichergestellt ist
   (§ 6 Abs. 3 Satz 1 Halbsatz 1 EStG – für [JAHR] verifizieren).
   Ist der Übernehmer keine natürliche Person und wird nur ein Teil eines
   Mitunternehmeranteils übertragen, ist die Buchwertfortführung nach
   § 6 Abs. 3 Satz 1 Halbsatz 2 EStG streitig; weise das als offen aus und
   verweise auf das Revisionsverfahren IV R 13/25. Ist der Übernehmer eine
   natürliche Person, ist das Verfahren für diesen Fall ohne Bedeutung – sage
   das ebenfalls ausdrücklich.
   Ist die Einordnung nach dem Entwurf nicht eindeutig, sage das und arbeite
   die Varianten getrennt ab.
2. Unentgeltlichkeit prüfen: Liegt eine voll unentgeltliche Übertragung vor?
   Prüfe Gleichstellungsgeld, Übernahme von Verbindlichkeiten,
   Versorgungsleistungen und Nießbrauchsvorbehalt einzeln daraufhin, ob sie
   die Unentgeltlichkeit berühren, je mit Rechtsgrundlage. Bei teilentgeltlicher
   Übertragung benenne die Folge dem Grunde nach und weise darauf hin, dass die
   Aufteilung außerhalb dieses Prompts vorzunehmen ist.
3. Bestandsaufnahme: Lege für JEDE gelieferte Position des
   Sonderbetriebsvermögens I und II eine eigene Zeile an. Ergänze eine
   Suchliste der Positionen, die typischerweise nicht in der Sonderbilanz
   stehen und trotzdem dazugehören können, und frage sie ab, wenn Angaben
   fehlen: an die Gesellschaft überlassene Grundstücke und Gebäudeteile,
   Betriebsvorrichtungen, an die Gesellschaft überlassene Fahrzeuge und
   Maschinen, Lizenzen, Marken und Patente, Anteile an der
   Komplementärgesellschaft, Darlehen an die Gesellschaft und deren
   Sicherheiten, Bürgschaften, Guthaben auf Gesellschafterkonten, Ansprüche
   aus Rückdeckungsversicherungen.
4. Funktionale Wesentlichkeit je Position, dem Grunde nach: Benenne den
   Maßstab und woraus er folgt, und ordne dann jede Position zu
   [funktional wesentlich / nicht wesentlich / unklar], mit Begründung in
   höchstens drei Sätzen. Sage ausdrücklich, welche Bedeutung stille Reserven
   für diese Zuordnung haben und welche nicht, mit Fundstelle. Bewerte KEINE
   stillen Reserven.
5. Abgleich mit dem Entwurf – der Kern dieser Prüfung: Stelle jede als
   wesentlich oder unklar eingestufte Position dem gegenüber, was der Entwurf
   ausdrücklich mitüberträgt. Ergebnis je Position:
   (im Entwurf erfasst), (im Entwurf nicht erfasst – Handlungsbedarf vor dem
   Termin), (Zuordnung offen – Angabe fehlt). Zähle die Positionen mit
   Handlungsbedarf am Ende auf, ohne Betrag.
6. Zeitliche Zusammenhänge: Prüfe jeden gelieferten Vorgang der letzten Jahre
   und jeden geplanten weiteren Schritt darauf, ob er die Buchwertfortführung
   berührt. Behandle getrennt: Ausgliederung oder Entnahme wesentlicher
   Positionen vor der Übertragung, taggleiche Vorgänge, Übertragungen nach
   § 6 Abs. 5 EStG, die Behaltensregelung des § 6 Abs. 3 Satz 2 EStG
   (Zeitraum – für [JAHR] verifizieren) und die Frage eines einheitlichen
   Plans. Nenne je Fall die Rechtsgrundlage und sage, wenn die Beurteilung
   streitig ist.
7. Erbschaft- und schenkungsteuerliche Seite, dem Grunde nach: Benenne, welche
   Bedeutung die Mitübertragung des Sonderbetriebsvermögens für das
   begünstigungsfähige Vermögen nach § 13b Abs. 1 Nr. 2 ErbStG hat, und welche
   weiteren Voraussetzungen und Nachbehaltensregelungen im Raum stehen
   (Quoten, Fristen und Lohnsummenregelung – für [JAHR] verifizieren). Rechne
   nichts und nenne keine Werte. Weise darauf hin, dass die
   ertragsteuerliche und die erbschaftsteuerliche Beurteilung getrennt zu
   führen sind und auseinanderfallen können.
8. Handlungsbedarf vor dem Termin: Welche Positionen müssen aus steuerlicher
   Sicht in den Übertragungsvorgang einbezogen werden, welche Zustimmungen und
   Beschlüsse fehlen, welche Unterlagen sind zu beschaffen, wer entscheidet?
   Formuliere jeden Punkt als Hinweis an das Notariat, nicht als
   Vertragsklausel, und ordne ihn einer Verantwortlichkeit zu:
   [Kanzlei / Notariat / Mandant / offen]. Ob und wie eine Position gesondert
   zu beurkunden ist, entscheidet das Notariat; benenne die Frage, beantworte
   sie nicht.

WEITERE ERGEBNISSE
9. Rückfrageliste, Tabelle mit den Spalten Nr. | Fehlende Angabe oder
   Unterlage | Wofür sie gebraucht wird | Antwort (leer).
10. Terminliste bis zum geplanten Übertragungsstichtag: die Punkte aus
    Schritt 8 in sinnvoller Reihenfolge, ohne Datum und ohne Fristangabe, je
    mit dem Ereignis, das den Punkt auslöst.
11. Prüfvermerk für die Akte, höchstens 250 Wörter: Übertragungsgegenstand,
    Zahl der Positionen mit Handlungsbedarf, offene Rechtsfragen, ausdrücklicher
    Hinweis auf das anhängige Revisionsverfahren, nächster Schritt.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben je Position einzeln. Reicht eine Angabe für die Zuordnung nicht aus,
   ordne NICHT zu, sondern nimm die Position in die Rückfrageliste.
2. Nenne KEINEN Betrag, KEINE Quote, KEINEN Prozentsatz und KEINE Fristlänge
   als feststehenden Wert. Jede solche Größe nur als nachzuschlagende Angabe
   mit dem Zusatz "für [JAHR] verifizieren".
3. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV, also Norm mit Absatz und
   Satz, Richtlinie oder BMF-Schreiben mit Datum oder Entscheidung mit Datum
   und Aktenzeichen, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
   keine Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE Fristen und Behaltenszeiträume im
   Raum stehen, je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und ohne Dauer. Ergänze bei jeder:
   "Frist von einem Menschen zu berechnen und im Fristenprogramm zu erfassen."
5. Weise jede Frage, die höchstrichterlich nicht geklärt oder Gegenstand eines
   anhängigen Verfahrens ist, ausdrücklich als offen aus. Täusche keine
   Sicherheit vor, auch nicht durch die Wortwahl.
6. Formuliere jede Aussage zur tatsächlichen Nutzung eines Wirtschaftsguts als
   Vermutung, solange sie nicht aus den Angaben folgt.
7. Bewerte die Vollständigkeit der Unterlagen als [tragfähig / dünn /
   nicht tragfähig] und sage in einem Satz, was fehlt.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Übertragungsgegenstand und Unentgeltlichkeit
3. Bestandstabelle Sonderbetriebsvermögen (Position | Art | Nutzung durch die
   Gesellschaft | Vertragsgrundlage | funktional wesentlich | Begründung)
4. Abgleichstabelle mit dem Entwurf (Position | im Entwurf erfasst |
   Handlungsbedarf | offene Angabe)
5. Zeitliche Zusammenhänge
6. Erbschaft- und schenkungsteuerliche Seite, dem Grunde nach
7. Offene Rechtsfragen einschließlich des anhängigen Revisionsverfahrens
8. Fristarten mit Rechtsgrundlage
9. Handlungsbedarf mit Verantwortlichkeit
10. Rückfrageliste
11. Terminliste
12. Prüfvermerk
13. Interne Notiz
14. Was ich nicht sicher weiß
```

## Anwendung

1. Den Prompt einsetzen, sobald ein Entwurf vorliegt und nicht erst nach dem Notartermin – nach der Beurkundung ist die Vollständigkeitsprüfung nur noch eine Schadensfeststellung.
2. Die Sonderbilanz als Ausgangspunkt nehmen, aber nicht als abschließende Liste. Positionen, die nie in die Sonderbilanz gelangt sind – überlassene Fahrzeuge, Lizenzen, Anteile an der Komplementärgesellschaft, Bürgschaften –, sind der eigentliche Risikobereich.
3. Den Wortlaut des Übertragungsgegenstands aus dem Entwurf einfügen, nicht dessen Zusammenfassung. Der Abgleich in Schritt 5 lebt vom Vertragstext.
4. Die Positionen mit Handlungsbedarf vor dem Termin mit dem Notariat abstimmen und den Abstimmungsstand in der Akte festhalten.
5. Ergebnis und offene Rechtsfragen dem Mandanten schriftlich mitteilen, bevor beurkundet wird; der Hinweis auf das anhängige Revisionsverfahren gehört in die Akte.

## Qualitätssicherung

- **Die Prüfung ist eine Vollständigkeitsprüfung, keine Bewertung.** Wer aus dem Ergebnis eine Aussage über die Höhe stiller Reserven oder über eine Steuerbelastung ableitet, verwendet den Prompt außerhalb seines Zwecks.
- **Die Sonderbilanz ist nicht die Bestandsliste.** Jede Position, die tatsächlich der Gesellschaft dient, ist unabhängig davon zu prüfen, ob sie bilanziert wurde.
- **Ertragsteuer und Erbschaftsteuer getrennt beurteilen.** Die Buchwertfortführung kann gelingen und die Begünstigung dennoch scheitern – und umgekehrt.
- **Kein Vertragsentwurf aus dem Werkzeug.** Enthält die Antwort Klauseltext, ist er zu streichen; die Kanzlei liefert dem Notariat den steuerlichen Befund, nicht die Urkunde.
- **Satz und Halbsatz des § 6 Abs. 3 EStG nachlesen.** Die Übertragung eines Teils eines Mitunternehmeranteils auf eine natürliche Person steht in Satz 1 Halbsatz 2; Satz 2 betrifft die Zurückbehaltung von Wirtschaftsgütern mit Behaltensregelung und tritt neben Satz 1. Eine KI-Antwort, die Satz 2 mit der Teilanteilsübertragung gleichsetzt, ist falsch.
- **Das Revisionsverfahren IV R 13/25 ist offen.** Weder das Urteil des Finanzgerichts Baden-Württemberg vom 06.06.2025 – 5 K 397/24 noch eine daraus abgeleitete Erwartung trägt eine Gestaltungsempfehlung. Der Verfahrensstand ist vor jeder Verwertung selbst nachzulesen.
- **Zeitliche Zusammenhänge sind der zweite Fallstrick.** Vorgeschaltete Ausgliederungen und taggleiche Übertragungen können die Buchwertfortführung berühren; sie gehören vollständig auf den Tisch, bevor beurkundet wird.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Bestandstabelle und Abgleich mit dem Vertragsentwurf Position für Position nach. Die Gestaltungsempfehlung, jede Mitteilung an Mandant oder Notariat und die Freigabe des Vertragsentwurfs verantwortet ein Berufsträger; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 6 Abs. 3 und Abs. 5 EStG sowie § 16 EStG im amtlichen Volltext (gesetze-im-internet.de) – bei § 6 Abs. 3 EStG satz- und halbsatzgenau –, §§ 13a und 13b ErbStG, den einschlägigen BMF-Schreiben zu § 6 Abs. 3 EStG über die Datenbank des Bundesfinanzministeriums, dem Urteil des Bundesfinanzhofs vom 02.08.2012 – IV R 41/11, dem Verfahrensstand zu BFH IV R 13/25 sowie DATEV LEXinform.

## Varianten

- **Teilanteilsübertragung:** „Beschränke dich auf § 6 Abs. 3 Satz 1 Halbsatz 2 EStG und, soweit Sonderbetriebsvermögen zurückbehalten wird, zusätzlich auf § 6 Abs. 3 Satz 2 EStG. Arbeite die Behaltensregelung als nachzuschlagende Größe ab und benenne, welche Angaben zur Quote, zur Person des Übernehmers und zum Verbleib des Sonderbetriebsvermögens fehlen."
- **Nur Bestandsaufnahme:** „Führe ausschließlich die Schritte 3 und 4 aus und erzeuge eine abhakbare Liste (Kästchen ☐ vor jeder Position) für die Durchsicht mit dem Mandanten."
- **Nach der Beurkundung:** „Prüfe, welche wesentlichen Positionen nicht mitübertragen wurden, benenne die Folge dem Grunde nach ohne Bewertung und erstelle eine Unterlagenliste für die Prüfung durch den Berufsträger."
- **Erbfall statt Schenkung:** „Stelle dar, welche Schritte bei einem Erwerb von Todes wegen abweichen, insbesondere zur Zuordnung des Sonderbetriebsvermögens bei Erbengemeinschaft und Auseinandersetzung, je mit Rechtsgrundlage."
