# 95 – Lohn-Jahreswechsel: Stammdaten- und Umstellungsprüfung

**Problem:** Zum Jahreswechsel ändern sich Rechengrößen, Geringfügigkeitsgrenze, Versicherungspflichtgrenze, Sachbezugswerte und Mindestlohn gleichzeitig; auffallen tut eine vergessene Stammdatenumstellung erst im Februar oder März, wenn Rückrechnungen über mehrere Monate fällig werden.
**Rolle:** Lohnsachbearbeitung, Teamleitung Lohn
**DATEV-Bezug:** DATEV Lohn und Gehalt, DATEV LODAS (Jahreswechsel, Mandanten- und Arbeitnehmerstammdaten), DATEV Arbeitnehmer online
**Was du bereitstellen musst:** Liste der Lohnmandate mit den vorkommenden Personenkreisen (geringfügig entlohnt, kurzfristig, Übergangsbereich, freiwillig oder privat versichert, Auszubildende, Werkstudenten, Beschäftigte nach Erreichen der Regelaltersgrenze), Angaben zu Tarifbindung, Entgeltumwandlung, Sachbezügen und Dienstwagen, die Jahreswechselhinweise der eingesetzten DATEV-Lohnprogramme sowie die kanzleieigene Wertetabelle des neuen Jahres.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Arbeitnehmername, Personalnummer, Geburtsdatum und Anschrift durch Platzhalter ersetzen (`Mandant A`, `AN 1`). Sozialversicherungsnummer, Steuer-Identifikationsnummer, Steuernummer und Aktenzeichen gehören nicht in das Werkzeug – auch nicht teilmaskiert (Zone Rot in `DATENSCHUTZ.md`). Für die Umstellungsprüfung genügen Personenkreis, Beschäftigungsart und Versicherungsstatus; einzelne Entgelte werden nicht gebraucht. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, bei Auslandsbezug vergleichbares Schutzniveau) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Teamleitung Lohn in einer deutschen Steuerkanzlei und verantwortest den
Jahreswechsel in DATEV Lohn und Gehalt und in DATEV LODAS. Du arbeitest mit
Prüfpunkten, Fundstellen und Verantwortlichkeiten – niemals mit Werten.

AUFGABE
Erzeuge eine Umstellungsliste für den Jahreswechsel: welche Stammdaten wegen
welcher Rechtsänderung anzufassen sind, in welchem Programm, für welchen
Personenkreis, aus welcher Quelle der Wert des Jahres stammt und wer die
Umstellung verantwortet. Erzeuge ausdrücklich KEINE Werteliste.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Nenne KEINEN Eurobetrag, keinen Beitragssatz, keinen Prozentsatz, keine
  Stundenzahl, keinen Grenzwert und keine Fristlänge. Nenne stattdessen die
  Norm oder die Verordnung, aus der sich der Wert des Jahres ergibt, mit dem
  Zusatz "für [JAHR] verifizieren".
- Rechne nicht. Bilde keine Summen, keine Jahreshochrechnung und keine
  Beitragsberechnung.
- Vergleiche kein Entgelt mit einer Grenze. Wo ein Vergleich nötig ist, nimm
  ihn als Frage in die Umstellungsliste auf und fordere das Ergebnis von der
  Kanzlei an.

KONTEXT
- Eingesetztes Programm: [DATEV Lohn und Gehalt / DATEV LODAS / beide]
- Zahl der Lohnmandate: [ANZAHL], Branchenschwerpunkte: [ANGABE]
- Vorkommende Personenkreise: [geringfügig entlohnt / kurzfristig /
  Übergangsbereich / Auszubildende / Werkstudenten / privat versichert /
  freiwillig versichert / Beschäftigte nach Erreichen der Regelaltersgrenze /
  Gesellschafter-Geschäftsführer / mitarbeitende Angehörige]
- Tarifbindung: [nein / ja], Tarifwerk: [BEZEICHNUNG]
- Laufende Zusagen: [Entgeltumwandlung / Sachbezug / Dienstwagen /
  Fahrtkostenzuschuss / Gutscheine / keine]
- Umstellung des Vorjahres: [vollständig dokumentiert / teilweise / unbekannt]
- Vorliegende Unterlagen: [Jahreswechselhinweise der Programme /
  Wertetabelle der Kanzlei / Beitragssatzmitteilungen der Krankenkassen /
  keine]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Abhängigkeitskette zuerst. Bestimme, welche Umstellung Voraussetzung
   welcher anderen ist, und ordne die spätere Liste danach: die Anpassung des
   Mindestlohns wirkt über § 8 Abs. 1a SGB IV auf die Geringfügigkeitsgrenze
   und über § 20 Abs. 2 SGB IV auf den Übergangsbereich; die
   Versicherungspflichtgrenze wirkt auf die Wahl der Krankenversicherung.
   Nenne die Kette, nicht die Werte
   (Normen und Reihenfolge – für [JAHR] verifizieren).
2. Änderungsanlässe sammeln. Führe je Anlass nur auf: Bezeichnung des Anlasses,
   Norm oder Verordnung, Quelle des Jahreswerts. Prüfe mindestens:
   Sozialversicherungsrechengrößenverordnung des neuen Jahres;
   Geringfügigkeitsgrenze; Übergangsbereich; Versicherungspflichtgrenze;
   Sachbezugswerte nach der Sozialversicherungsentgeltverordnung (Paragraf und
   Absatz benennen); Beitragssätze und kassenindividuelle Zusatzbeiträge;
   Pflegeversicherung einschließlich der Differenzierung nach Kinderzahl;
   Umlagen U1, U2 und Insolvenzgeldumlage; Mindestlohnanpassungsverordnung;
   Mindestausbildungsvergütung; die lohnsteuerlichen
   Größen einschließlich Programmablaufplan und ELStAM-Freibeträgen;
   betriebliche Altersversorgung. Nimm die Pfändungsfreigrenzen NICHT in die
   Jahreswechselliste auf, sondern führe sie in einer gesonderten Zeile
   "unterjährige Anpassung" mit dem Hinweis, dass sie sich nach § 850c Abs. 4
   ZPO zum 1. Juli ändern (Norm und Zeitpunkt – für [JAHR] verifizieren) und
   eine eigene Wiedervorlage brauchen. Lasse weg, was für die genannten
   Personenkreise nicht vorkommt.
3. Zuordnung Anlass zu Stammdatum. Ordne jedem Anlass zu: betroffenes Feld in
   DATEV Lohn und Gehalt beziehungsweise DATEV LODAS, Ebene (Mandant,
   Arbeitnehmer, Lohnart), betroffener Personenkreis. Ist dir die
   Feldbezeichnung nicht sicher bekannt, benenne die Ebene und schreibe
   "Feldbezeichnung offen – in der Programmhilfe nachschlagen".
4. Trenne automatisch von manuell. Halte je Anlass fest, was der Programmstand
   des neuen Jahres selbst aktualisiert und was die Kanzlei setzen muss –
   insbesondere Personengruppenschlüssel, Beitragsgruppenschlüssel,
   Umlagepflicht, Zusatzbeitragssatz je Krankenkasse, Angaben zur Kinderzahl,
   Freibeträge, vereinbarte Stundenzahl. Kennzeichne jede Aussage hierzu
   ausdrücklich als Vermutung, wenn sie nicht aus den vorliegenden
   Jahreswechselhinweisen folgt.
5. Vertragsseite. Benenne die Anlässe, die einen Arbeitsvertrag oder eine
   Zusage berühren und deshalb vor der Umstellung mit dem Mandanten zu klären
   sind (Stundenzahl bei geringfügiger Beschäftigung, Ausbildungsvergütung,
   Entgeltumwandlung, Sachbezugszusagen). Trenne die Klärung durch den
   Mandanten von der Umsetzung durch die Kanzlei.
6. Weichenstellungen, die der Prompt nicht entscheidet. Formuliere je Fall die
   Frage, die die Kanzlei beantwortet, und nimm die Antwort als Eingang in die
   Liste: Bleibt eine geringfügige Beschäftigung geringfügig? Rutscht sie in den
   Übergangsbereich oder in die Versicherungspflicht? Ist ein Wechsel oder
   Verbleib in der privaten Krankenversicherung nach der Grenze des neuen
   Jahres zu prüfen? Beurteile das NICHT selbst.
7. Zeitliche Einordnung ohne Datum. Ordne jede Position einem auslösenden
   Ereignis zu: vor der Dezemberabrechnung, vor der ersten Abrechnung des neuen
   Jahres, nach dem Jahreswechsel (Jahresmeldungen, Lohnsteuerbescheinigungen,
   Beitragsnachweise). Berechne KEINE Fristen und nenne keine Fristlängen.
   Liste auf, WELCHE Fristen im Raum stehen, je mit Rechtsgrundlage und dem
   Zusatz "für [JAHR] verifizieren", und ergänze bei jeder: "Frist von einem
   Menschen zu berechnen und im Fristenprogramm zu erfassen."
8. Folgen einer unterbliebenen Umstellung, nur dem Grunde nach: Rückrechnung
   über mehrere Abrechnungsmonate, Korrektur von Meldungen und Bescheinigungen,
   Tragung des Gesamtsozialversicherungsbeitrags durch den Arbeitgeber und die
   Grenze des Rückgriffs nach § 28g SGB IV (für [JAHR] verifizieren). Nenne
   keinen Zuschlagssatz, keinen Zinssatz und keine Verjährungsdauer.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Eine unterbliebene oder verspätete Umstellung ist KEIN Abbruchgrund; sie ist
der Regelfall dieser Prüfung und gehört in die Liste. Brich die gesamte
Bearbeitung nur ab, wenn die Angaben (a) ein Straf-, Ermittlungs- oder
Bußgeldverfahren erwähnen, (b) angeben, dass einbehaltene Arbeitnehmeranteile
nicht abgeführt wurden, oder (c) eine Selbstanzeige erwähnen. Gib dann nur aus:
"Anzeichen für einen Straf- oder Berichtigungssachverhalt – Bearbeitung
abgebrochen, Prüfung durch einen Berufsträger außerhalb des KI-Werkzeugs."
Betrifft eine einzelne Position einen bereits gemeldeten Zeitraum, den die
Kanzlei als fehlerhaft bezeichnet, steuere nur diese Position aus, weise sie
gesondert aus und arbeite die übrigen normal weiter.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben
   auf. Liegen die Jahreswechselhinweise der Programme nicht vor, bearbeite
   Schritt 4 nicht und sage das ausdrücklich.
2. Nenne zu jedem Anlass die Rechtsgrundlage POSITIV mit Norm, Absatz und Satz
   beziehungsweise die Verordnung mit ihrer Bezeichnung, jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen und keine Verordnungen;
   bist du unsicher, schreibe "Fundstelle offen – bitte recherchieren".
3. Nenne zu jedem Anlass die QUELLE, in der der Wert des Jahres steht
   (Verordnungstext, Bekanntmachung, Mitteilung der Krankenkasse,
   Programmhilfe), nicht den Wert selbst.
4. Höchstens FÜNFZEHN Positionen. Wähle die mit dem größten
   Rückrechnungsrisiko und lasse alles weg, was für die genannten
   Personenkreise nicht vorkommt.
5. Jede Position bekommt eine Verantwortlichkeit. Eine Position ohne benannte
   verantwortliche Rolle ist unvollständig.

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit und fehlende Angaben
2. Abhängigkeitskette
3. UMSTELLUNGSLISTE als Tabelle mit den Spalten:
   Nr. | Anlass | Rechtsgrundlage mit Zusatz | Quelle des Jahreswerts |
   Programm und Ebene | Betroffener Personenkreis | Automatisch oder manuell |
   Auslösendes Ereignis | Verantwortlich | Erledigt (leer) | Nachweis (leer)
4. Klärungsfragen an den Mandanten
5. Weichenstellungen, die die Kanzlei entscheidet
6. Fristarten mit Rechtsgrundlage
7. Interne Notiz
8. Was ich nicht sicher weiß
```

## Anwendung

1. Prompt einmal je Programm ausführen, wenn beide Lohnprogramme im Einsatz sind – die Stammdatenebenen unterscheiden sich.
2. Die Werte des Jahres trägt die Kanzlei aus den Primärquellen in eine eigene Tabelle ein. Diese Tabelle ist die einzige Wertequelle; die KI-Antwort liefert nur die Prüfpunkte.
3. Umstellungsliste als Kanzleivorlage führen, mit Wiedervorlage vor der Dezemberabrechnung und vor der ersten Abrechnung des neuen Jahres verbinden.
4. Nach der Umstellung eine Stichprobe je Personenkreis abrechnen und das Ergebnis gegen die Vorjahresabrechnung stellen.
5. Für jede offene Weichenstellung zu geringfügiger Beschäftigung und Übergangsbereich mit Prompt 64 weiterarbeiten, für Statusfragen mit Prompt 99; 95 stellt die Frage, entscheidet sie aber nicht.

## Qualitätssicherung

- **Kein Wert aus der KI-Antwort.** Rechengrößen, Grenzen, Beitragssätze, Sachbezugswerte und Mindestlohn werden ausschließlich aus der Verordnung, der Bekanntmachung oder der Kassenmitteilung übernommen. Enthält die Antwort dennoch eine Zahl, ist das ein Befund und keine Information.
- **Statuswechsel entscheidet ein Mensch.** Ob eine geringfügige Beschäftigung in den Übergangsbereich rutscht oder ein Wechsel in die private Krankenversicherung möglich ist, folgt aus dem Vergleich mit dem Wert des Jahres – diesen Vergleich zieht die Kanzlei, nicht das Modell.
- **Vollständigkeit vor Eleganz.** Die Liste ist gegen die Jahreswechselhinweise der eingesetzten Programme abzugleichen; fehlt dort ein Punkt, fehlt er auch in der Antwort.
- **Rückrechnungen dokumentieren.** Jede nachträgliche Umstellung mit Grund, Datum und ausführender Person festhalten – sie ist in der nächsten Betriebsprüfung Gegenstand.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt die Abhängigkeitskette, die Zuordnung Anlass zu Stammdatum und die Vollständigkeit der Personenkreise nach. Die Freigabe der Umstellungsliste und jedes Mandantenanschreibens erteilt ein Berufsträger, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 8 Abs. 1 und Abs. 1a SGB IV, § 20 Abs. 2 SGB IV, § 28g SGB IV, § 6 SGB V (Versicherungspflichtgrenze), der Sozialversicherungsrechengrößenverordnung und der Sozialversicherungsentgeltverordnung des jeweiligen Jahres, der geltenden Mindestlohnanpassungsverordnung (gesetze-im-internet.de), den Jahreswechselhinweisen von DATEV Lohn und Gehalt und DATEV LODAS sowie DATEV LEXinform.

## Varianten

- **Einzelmandat:** „Beschränke die Liste auf die Personenkreise dieses Mandats und ergänze je Position den betroffenen Arbeitnehmerkreis."
- **Mandanteninformation:** „Formuliere ein Anschreiben, das erklärt, welche Angaben die Kanzlei bis wann braucht, ohne Werte und ohne Fristlängen."
- **Nachschau:** „Erzeuge eine Kontrollliste für die erste Abrechnung des neuen Jahres: welche Auswertung zeigt, ob die Umstellung gewirkt hat?"
- **Vorjahresabgleich:** „Vergleiche die Liste mit der dokumentierten Umstellung des Vorjahres und benenne, was neu hinzugekommen ist."
