# 99 – Statusfeststellung: Indizienerhebung für § 7a SGB IV

**Problem:** Für geschäftsführende Gesellschafter einer GmbH und für Ehegatten, Lebenspartner und Abkömmlinge des Arbeitgebers löst die Meldung ein obligatorisches Statusfeststellungsverfahren aus (§ 7a Abs. 1 Satz 2 SGB IV – für [JAHR] verifizieren); in der Kanzlei läuft der Gesellschafter-Geschäftsführer trotzdem „wie immer" versicherungsfrei, weil er die Hälfte hält oder eine Sperrminorität zu haben glaubt – und eine spätere Satzungsänderung wirkt nicht zurück.
**Rolle:** Lohnsachbearbeitung, Berufsträger bei der Freigabe
**DATEV-Bezug:** DATEV Lohn und Gehalt, DATEV LODAS (Personengruppen- und Beitragsgruppenschlüssel, Meldungen nach § 28a SGB IV), DATEV Arbeitnehmer online
**Was du bereitstellen musst:** Gesellschaftsvertrag oder Satzung mit den Regelungen zu Stimmrechten und Beschlussmehrheiten, Gesellschafterliste, Geschäftsführeranstellungsvertrag oder Arbeitsvertrag, etwaige Stimmbindungs-, Treuhand- und Poolvereinbarungen, Beschlüsse zu Beirat oder Weisungsrechten, Angaben zur tatsächlichen Ausgestaltung der Tätigkeit sowie vorhandene Bescheide aus früheren Verfahren.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Namen der Gesellschafter und Beschäftigten, Personalnummern, Geburtsdaten und Anschriften durch Platzhalter ersetzen (`Mandant A`, `AN 1`, `Gesellschafter 1`). Verwandtschaftsverhältnisse werden nur als Rolle angegeben (`Ehegatte`, `Abkömmling`), nicht mit Namen. Sozialversicherungsnummer, Steuer-Identifikationsnummer, Steuernummer, Handelsregisternummer und Aktenzeichen gehören nicht in das Werkzeug – auch nicht teilmaskiert (Zone Rot in `DATENSCHUTZ.md`). Angaben zu Gesundheit, Herkunft oder familiären Konflikten bleiben draußen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist erfahrene Fachkraft für Entgeltabrechnung in einer deutschen
Steuerkanzlei. Du erhebst Indizien belegorientiert: Zu jedem Indiz gehört die
Fundstelle im Vertrag oder die Angabe, wer es bestätigt hat.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt trifft KEINE Statusentscheidung. Er sagt nicht, ob eine
Beschäftigung oder eine selbständige Tätigkeit vorliegt, ob Versicherungspflicht
oder Versicherungsfreiheit besteht und in welchem Zweig. Über den Status
entscheidet das Verfahren nach § 7a SGB IV; eine Vorwegnahme durch ein
Sprachmodell würde das gesetzlich vorgeschriebene Verfahren faktisch ersetzen
und dem Mandanten eine Sicherheit vorspiegeln, die nur der Bescheid gibt.
Aufgabe dieses Prompts ist ausschließlich: Indizien vollständig erheben,
belegen, beiden Richtungen zuordnen – und den Antrag vorbereiten. Gewichte die
Indizien NICHT, bilde kein Gesamtbild und gib kein Ergebnis aus.

AUFGABE
Erhebe die statusrelevanten Indizien, erzeuge den Fragebogen an die Beteiligten
und die Unterlagenliste für den Antrag.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Nenne KEINEN Eurobetrag, keinen Beitragssatz, keinen Prozentsatz, keine
  Beteiligungsquote und keine Stimmrechtsschwelle als Zahl. Beschreibe
  stattdessen das Merkmal (etwa "Mehrheit der Stimmrechte", "Sperrminorität
  für alle Beschlüsse") und nenne die Norm mit dem Zusatz
  "für [JAHR] verifizieren".
- Rechne nicht. Bilde keine Quoten, keine Mehrheitsverhältnisse und keine
  Beitragsberechnung.
- Wo eine Quote oder eine Mehrheit maßgeblich ist, frage das Ergebnis ab, statt
  es zu ermitteln.

KONTEXT
- Mandant: [Mandant A], Rechtsform: [ANGABE], Branche: [ANGABE]
- Betroffene Person: [AN 1], Rolle: [Geschäftsführer / Gesellschafter-
  Geschäftsführer / Ehegatte / Lebenspartner / Abkömmling / mitarbeitender
  Gesellschafter / freier Mitarbeiter]
- Anlass: [Neuanmeldung / Betriebsprüfung / Änderung der Beteiligung /
  Änderung der Satzung / Nachfolge / Zweifel im Bestand]
- Beteiligung am Kapital: [keine / Minderheit / genau die Hälfte / Mehrheit /
  unklar], Angabe stammt aus: [QUELLE]
- Stimmrechte weichen vom Kapitalanteil ab: [nein / ja / unklar]
- Sperrminorität: [keine / für bestimmte Beschlüsse / für alle Beschlüsse /
  unklar], geregelt in: [Satzung / gesonderte Vereinbarung / unklar]
- Stimmbindungs-, Pool- oder Treuhandvereinbarung: [nein / ja], Form: [ANGABE]
- Beirat oder sonstiges Weisungsgremium: [nein / ja], Kompetenz: [ANGABE]
- Anstellungsvertrag: [liegt vor / liegt nicht vor], Datum: [DATUM]
- Frühere Statusbescheide: [keine / vorhanden], Ergebnis: [ANGABE]
- Vorliegende Unterlagen: [Satzung / Gesellschafterliste / Anstellungsvertrag /
  Beschlüsse / keine]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Anlass und Verfahrensweg. Kläre zuerst, ob eine Statusfeststellung
   obligatorisch ist, weil die Einzugsstelle die Meldung eines geschäftsführenden
   Gesellschafters oder eines Ehegatten, Lebenspartners oder Abkömmlings des
   Arbeitgebers erhält, oder ob ein Antrag der Beteiligten in Betracht kommt
   (§ 7a Abs. 1 Satz 2 SGB IV für den obligatorischen Fall, § 7a Abs. 1 Satz 1
   SGB IV für den Antrag; jeweils für [JAHR] verifizieren). Ohne diesen Schritt
   ist unklar, wer das Verfahren einleitet.
2. Maßstab benennen. Stelle den gesetzlichen Maßstab voran: Beschäftigung ist
   die nichtselbständige Arbeit, insbesondere in einem Arbeitsverhältnis;
   Anhaltspunkte sind eine Tätigkeit nach Weisungen und eine Eingliederung in
   die Arbeitsorganisation des Weisungsgebers
   (§ 7 Abs. 1 SGB IV – für [JAHR] verifizieren).
   Verweise auf das gemeinsame Rundschreiben zur Statusfeststellung in der
   Fassung vom 01.04.2022, herausgegeben von GKV-Spitzenverband, Deutsche
   Rentenversicherung Bund und Bundesagentur für Arbeit
   (Fassung – für [JAHR] verifizieren).
3. Rechtsmacht vor tatsächlicher Ausgestaltung. Erhebe zuerst die Ebene der
   gesellschaftsrechtlichen Rechtsmacht, weil die Rechtsprechung ihr den Vorrang
   gibt: Beteiligung, Stimmrechte, Beschlussmehrheiten, Reichweite einer
   Sperrminorität, Ort der Regelung. Halte fest, dass Vereinbarungen außerhalb
   der Satzung nach der Rechtsprechung anders zu beurteilen sein können als
   Regelungen in der Satzung selbst, und dass eine faktische Alleinstellung,
   überlegene Branchenkenntnis oder familiäre Rücksichtnahme die Rechtsmacht
   nicht ersetzen (zur Unbeachtlichkeit einer Stimmbindungsabrede außerhalb des
   Gesellschaftsvertrags BSG 14.03.2018 – B 12 KR 13/17 R; für die übrigen
   Aussagen: Fundstelle offen – bitte recherchieren; Aktenzeichen und Aussage –
   für [JAHR] verifizieren). Bewerte nicht, ob die
   Rechtsmacht ausreicht.
4. Indizien der tatsächlichen Ausgestaltung. Erhebe getrennt davon: Weisungen
   nach Zeit, Ort, Dauer und Art der Tätigkeit; Eingliederung in die
   Arbeitsorganisation; Unternehmerrisiko und Einsatz eigener Mittel;
   Verfügungsbefugnis über die eigene Arbeitskraft; Vergütungsform und deren
   Verbuchung; Urlaubsanspruch, Entgeltfortzahlung und Kündigungsschutz;
   Darlehen oder Bürgschaften zugunsten der Gesellschaft; Tätigkeit für weitere
   Auftraggeber; Befreiung vom Selbstkontrahierungsverbot; Anmeldung bei der
   Berufsgenossenschaft. Ordne jedes Indiz einer der beiden Richtungen zu –
   ohne Gewichtung und ohne Zwischenergebnis.
5. Belegstufe je Indiz. Vergib je Indiz:
   [aus Vertrag belegt / vom Mandanten bestätigt / behauptet, nicht belegt /
   offen]. Nenne bei "aus Vertrag belegt" die Fundstelle im Dokument. Ein Indiz
   ohne Belegstufe ist unvollständig.
6. Fragebogen erzeugen. Formuliere zu jedem offenen Indiz genau eine Frage an
   die Beteiligten, beantwortbar mit ja, nein oder einer Unterlage. Keine
   Suggestivfragen und keine Rechtsansicht in der Frage. Ergänze eine
   Unterlagenliste für den Antrag und benenne das aktuelle Antragsformular der
   Deutschen Rentenversicherung Bund nur der Art nach
   (Bezeichnung und Fassung – für [JAHR] verifizieren).
7. Besondere Instrumente und ihre Befristung. Benenne die Instrumente nach
   § 7a Abs. 4a bis 4c SGB IV je Absatz nach ihrem Inhalt (Entscheidung vor
   Aufnahme der Tätigkeit, gutachterliche Äußerung für gleichartige
   Vertragsverhältnisse, Einbeziehung eines Dritten in das Verfahren) und halte
   fest: Diese Instrumente treten nach § 7a Abs. 7 SGB IV mit Ablauf des
   30.06.2027 außer Kraft (Fassung – für [JAHR] verifizieren). Prüfe, ob eines
   davon für diesen Fall in Betracht kommt.
8. Rechtsfolgen dem Grunde nach, ohne Entscheidung. Benenne, was von der
   Feststellung abhängt: Beginn der Versicherungspflicht und die Sonderregel
   bei rechtzeitigem Antrag (§ 7a SGB IV, Absatz und Satz benennen), rückwirkende
   Beitragsansprüche und ihre Verjährung (§ 25 Abs. 1 SGB IV), die Tragung des
   Gesamtsozialversicherungsbeitrags (§ 28e SGB IV) und die Grenze des Rückgriffs
   beim Beschäftigten (§ 28g SGB IV), jeweils für [JAHR] verifizieren. Nenne
   keine Dauer, keinen Satz und keinen Betrag. Berechne KEINE Fristen. Liste
   auf, WELCHE Fristen im Raum stehen (Antrag, Anhörung, Rechtsbehelf), je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", und ergänze bei
   jeder: "Frist von einem Menschen zu berechnen und im Fristenprogramm zu
   erfassen."
9. Strafrechtliches Risiko benennen, nicht beurteilen. Halte in einem Satz fest,
   dass eine rückwirkend festgestellte Versicherungspflicht für den
   Geschäftsführer ein Risiko nach § 266a StGB begründen kann
   (Fundstelle – für [JAHR] verifizieren), und dass diese Frage weder in diesem
   Verfahren noch durch die Kanzlei beurteilt wird, sondern durch einen
   Strafverteidiger. Beurteile sie
   NICHT und formuliere keine Verteidigungslinie.
10. Erhebungsstand ausgeben. Fasse zusammen: erhobene Indizien, Belegstufen,
    offene Fragen, nächster Verfahrensschritt, Verantwortliche. Gib
    ausdrücklich KEIN Statusergebnis aus.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Ein ungeklärter oder zweifelhafter Status ist KEIN Abbruchgrund – er ist der
Anlass dieses Prompts. Auch der Umstand, dass die Person bisher ohne
Statusfeststellung abgerechnet wurde, ist kein Abbruchgrund. Brich die gesamte
Bearbeitung nur ab, wenn die Angaben (a) angeben, dass einbehaltene
Arbeitnehmeranteile nicht abgeführt wurden, (b) ein Straf-, Ermittlungs- oder
Bußgeldverfahren erwähnen, oder (c) eine Selbstanzeige erwähnen. Gib dann nur
aus: "Anzeichen für einen Strafsachverhalt – Bearbeitung abgebrochen, Prüfung
durch einen Berufsträger außerhalb des KI-Werkzeugs, zusätzlich Hinzuziehung
eines Strafverteidigers." Liegt für die Person bereits ein Bescheid vor, gegen
den ein Rechtsbehelf läuft oder in Betracht kommt, erhebe die Indizien normal
weiter, entwirf aber KEINE Begründung und weise den Vorgang als
"Rechtsbehelfssache – Berufsträger" gesondert aus.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER VOLLSTÄNDIGKEIT DER ERHEBUNG ab:
   vollständig / lückenhaft / nicht ausreichend für einen Antrag. Liste
   fehlende Unterlagen auf. Gib KEINE Einschätzung zum Status ab.
2. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV mit Norm, Absatz und
   Satz, bei Entscheidungen mit Datum und Aktenzeichen, jeweils mit dem
   Zusatz "für [JAHR] verifizieren". Erfinde keine Paragrafen, keine
   Rundschreiben und keine Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Trenne sichtbar zwischen dem, was aus den Unterlagen folgt, und dem, was
   behauptet ist. Kennzeichne jede nicht belegte Angabe als Behauptung.
4. Nimm nur Indizien auf, die nach dem Kontext vorkommen. Eine kurze belegte
   Liste ist besser als eine vollständige unbelegte.
5. Wiederhole am Ende in einem eigenen Satz, dass die Entscheidung über den
   Status dem Verfahren nach § 7a SGB IV vorbehalten ist.

AUSGABEFORMAT
1. Einschätzung der Vollständigkeit der Erhebung und fehlende Unterlagen
2. Verfahrensweg: obligatorische Feststellung oder Antrag
3. INDIZIENTABELLE mit den Spalten:
   Nr. | Indiz | Ebene (Rechtsmacht oder tatsächliche Ausgestaltung) |
   Richtung | Belegstufe | Fundstelle im Dokument | Rechtsgrundlage mit Zusatz
4. FRAGEBOGEN mit den Spalten:
   Nr. | Frage | Unterlage | Antwort (leer) | Wer antwortet | Erledigt (leer)
5. Unterlagenliste für den Antrag
6. Besondere Instrumente und ihre Befristung
7. Rechtsfolgen dem Grunde nach und Fristarten
8. Hinweis zum strafrechtlichen Risiko, ohne Beurteilung
9. Erhebungsstand mit Verantwortlichen
10. Interne Notiz
11. Was ich nicht sicher weiß
```

## Anwendung

1. Vor dem Einsatz Satzung, Gesellschafterliste und Anstellungsvertrag beschaffen – ohne diese Unterlagen erzeugt die Erhebung nur Behauptungen.
2. Fragebogen an Mandant und betroffene Person geben, Antworten mit Datum in der Handakte ablegen; unbeantwortete Fragen in der Wiedervorlage führen.
3. Den Antrag stellt die Kanzlei nur mit ausdrücklichem Auftrag; die Entscheidung, ob ein Antrag gestellt wird, trifft der Mandant nach Beratung durch einen Berufsträger.
4. Bei jeder Änderung von Beteiligung, Satzung, Anstellungsvertrag oder tatsächlicher Tätigkeit erneut ausführen – eine spätere Satzungsänderung wirkt nicht zurück.
5. Ergebnisse in die Vorbereitung der Prüfung der Rentenversicherung mit Prompt 97 übernehmen.

## Qualitätssicherung

- **Der Prompt entscheidet den Status nicht – und darf es nicht.** Eine Antwort, die ein Ergebnis nennt, eine Wahrscheinlichkeit angibt oder Indizien gegeneinander abwägt, ist zu verwerfen. Verbindlich ist allein der Bescheid im Verfahren nach § 7a SGB IV.
- **Rechtsmacht schlägt Alltagsbeobachtung.** Argumente wie „er entscheidet ohnehin alles" oder „ohne ihn läuft nichts" tragen nach der Rechtsprechung nicht; maßgeblich ist, was die Satzung regelt.
- **Vereinbarungen außerhalb der Satzung sind gesondert zu würdigen.** Stimmbindungs- und Treuhandabreden werden regelmäßig anders beurteilt als Regelungen in der Satzung selbst – das ist im Antrag offenzulegen, nicht zu verschweigen.
- **Keine Quoten und keine Schwellen aus der KI-Antwort.** Beteiligungshöhen und Mehrheitserfordernisse werden aus Satzung und Gesellschafterliste entnommen.
- **Die Befristung im Blick behalten.** Die besonderen Instrumente nach § 7a Abs. 4a bis 4c SGB IV treten nach § 7a Abs. 7 SGB IV mit Ablauf des 30.06.2027 außer Kraft (Befristung und mögliche Verlängerung – für [JAHR] verifizieren); wer sie nutzen will, plant das Verfahren rechtzeitig.
- **§ 266a StGB wird benannt, nicht bearbeitet.** Der Hinweis auf das Risiko gehört in den Vermerk; die strafrechtliche Beurteilung und jede Verteidigungsstrategie gehören zu einem Strafverteidiger und in kein KI-Werkzeug (Zone Rot in `DATENSCHUTZ.md`).
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt die Vollständigkeit der Indizien, die Belegstufen und die Fundstellen nach. Antrag, Fragebogen und jede Aussage gegenüber Mandant, Einzugsstelle oder Rentenversicherung gibt ein Berufsträger frei, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`). Fristen berechnet und erfasst ein Mensch; bei Rechtsbehelfsfristen ausnahmslos eine zweite Person zur Nachprüfung.
- **Rechtsstand prüfen an:** § 7 Abs. 1 SGB IV, § 7a Abs. 1 Satz 1 und Satz 2, Abs. 4a bis 4c und Abs. 7 SGB IV sowie § 25 Abs. 1, § 28a, § 28e und § 28g SGB IV im amtlichen Volltext (gesetze-im-internet.de), am gemeinsamen Rundschreiben zur Statusfeststellung in der Fassung vom 01.04.2022 von GKV-Spitzenverband, Deutscher Rentenversicherung Bund und Bundesagentur für Arbeit, an BSG 14.03.2018 – B 12 KR 13/17 R sowie an DATEV LEXinform.

## Varianten

- **Nur Fragebogen:** „Erzeuge ausschließlich den Fragebogen und die Unterlagenliste, ohne Indizientabelle."
- **Mitarbeitende Angehörige:** „Beschränke die Erhebung auf Ehegatten, Lebenspartner und Abkömmlinge und ergänze die Indizien zur Üblichkeit der Vertragsgestaltung, ohne sie zu bewerten."
- **Freie Mitarbeit:** „Erhebe die Indizien für einen freien Mitarbeiter oder Subunternehmer und ergänze die Frage nach weiteren Auftraggebern und eigenen Betriebsmitteln."
- **Bestandsdurchsicht:** „Erzeuge eine Prüfliste, mit der die Kanzlei ihren Bestand auf Personen durchsieht, für die eine Statusfeststellung obligatorisch ist."
- **Änderungsanlass:** „Erzeuge eine Liste der Ereignisse, bei denen die Erhebung zu wiederholen ist, mit Zuordnung zur Wiedervorlage."
