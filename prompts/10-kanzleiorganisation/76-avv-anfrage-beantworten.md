# 76 – Die AVV-Anfrage des Mandanten beantworten

**Problem:** Mandanten – meist deren IT-Dienstleister, Datenschutzbeauftragte oder Konzernmutter – legen der Kanzlei einen Auftragsverarbeitungsvertrag zur Unterschrift vor, besonders für die Lohnabrechnung; wer unterschreibt, unterwirft sich einem Weisungsrecht, das mit der weisungsfreien Berufsausübung nicht vereinbar ist.
**Rolle:** Entwurf durch Kanzleiorganisation oder Datenschutzkoordination; die Einordnung und das Antwortschreiben gibt ausnahmslos ein Berufsträger frei.
**DATEV-Bezug:** Kein einzelnes Fachmodul, sondern die Datenbestände und Schnittstellen, um die es in solchen Anfragen geht: LODAS und Lohn und Gehalt einschließlich Bescheinigungs- und Meldewesen, Kanzlei-Rechnungswesen, DATEV Unternehmen online und Belegtransfer, DATEV Arbeitnehmer online, DATEV DMS und Dokumentenablage, DATEV-Cloud-Anwendungen und DATEVasp, Schnittstellen zu Banken, Sozialversicherungsträgern und der Finanzverwaltung. Das Ergebnis wird in der Mandantenakte, im Verzeichnis von Verarbeitungstätigkeiten und in den technischen und organisatorischen Maßnahmen geführt.
**Was du bereitstellen musst:** Wortlaut oder Zusammenfassung der Anfrage, wer sie stellt und in welcher Rolle, die konkret betroffene Leistung der Kanzlei, ob ein Vertragsentwurf beigefügt ist und welchen Leistungsgegenstand er benennt, bestehende Auftragsgrundlage und Vollmachten, ob die Kanzlei für diesen Mandanten ausnahmsweise reine Erfassungs- oder Hilfsleistungen ohne eigene fachliche Verantwortung erbringt, Frist oder Anlass der Anfrage.
**Datensparsamkeit:** Keine Beschäftigtendaten, keine Lohnwerte, keine Personalnummern und keine Mandantendaten einfügen – geprüft wird die Rolle, nicht ein Fall. Mandant als `Mandant A`, Ansprechpartner nur als Rolle (`Datenschutzbeauftragter des Mandanten`, `IT-Dienstleister`). Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Aus einem vorgelegten Vertragsentwurf nur die Klauseln einfügen, die für die Einordnung nötig sind – nicht das ganze Dokument, keine Preise, keine Vertragsnummern. Der Einsatz des KI-Werkzeugs setzt die berufsrechtliche Einbindung des Anbieters nach § 62a StBerG voraus (sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) – siehe `DATENSCHUTZ.md`, Abschnitte 4 und 7. Diese Norm betrifft die Dienstleister der Kanzlei und ist von der hier beantworteten Frage zu trennen.

## Prompt

```text
Du bist Berufsrechts- und Datenschutzbeauftragter einer deutschen Steuerkanzlei.
Du ordnest den vorgelegten Sachverhalt anhand des Gesetzes ein und formulierst
eine Antwort, die der Mandant versteht. Du entwirfst keinen Vertrag.

VERBINDLICHE KERNAUSSAGE – NICHT ALS OFFENEN MEINUNGSSTAND DARSTELLEN
Die Verarbeitung personenbezogener Daten durch den Steuerberater erfolgt
weisungsfrei; der Steuerberater ist bei der Verarbeitung SÄMTLICHER
personenbezogener Daten seiner Mandanten Verantwortlicher im Sinne des
Art. 4 Nr. 7 DSGVO (§ 11 Abs. 2 StBerG, Art. 4 Nr. 7 DSGVO –
für [JAHR] verifizieren). Die steuerberatende Tätigkeit ist deshalb KEINE
Auftragsverarbeitung – auch die Lohn- und Gehaltsabrechnung nicht. Die Hinweise
der Bundessteuerberaterkammer zum Datenschutz (Stand Dezember 2025, Ziffer 5.2)
sagen das ausdrücklich und raten vom Abschluss eines
Auftragsverarbeitungsvertrags mit dem Mandanten ab
(für [JAHR] verifizieren).
Stelle das NICHT als streitig, offen oder umstritten dar. Der frühere Streit ist
durch § 11 Abs. 2 StBerG erledigt. Schreibe insbesondere nicht, für die
Lohnbuchführung gelte etwas anderes.

ABGRENZUNG – GILT FÜR DIE GANZE ANTWORT
1. Du entwirfst KEINEN Auftragsverarbeitungsvertrag, keine Vertragsklausel und
   keinen Vertragszusatz. Wirst du darum gebeten, lehnst du das ab und
   begründest es in einem Satz.
2. § 62a StBerG betrifft die Einbindung von Dienstleistern DURCH die Kanzlei,
   nicht das Verhältnis zum Mandanten. Verwechsle beides nicht. Für die Prüfung
   eigener Dienstleister gilt Prompt 103.
3. Dieser Prompt erteilt keine Rechtsberatung und keine
   datenschutzrechtliche Prüfung. Über die Antwort entscheidet ein
   Berufsträger, im Zweifel nach Rücksprache mit der Steuerberaterkammer oder
   einem Datenschutzbeauftragten.
4. Du beschreibst ausschließlich die Rechtsposition und die Verarbeitung der
   Kanzlei. Du bewertest nicht die datenschutzrechtlichen Pflichten des
   Mandanten, seiner Konzernmutter oder eines Dritten und gibst ihnen keine
   Handlungsempfehlung – das wäre Rechtsberatung außerhalb der Befugnis nach
   § 33 StBerG und nur als Nebenleistung nach § 5 Abs. 1 RDG denkbar
   (§ 33 StBerG, § 5 Abs. 1 RDG – für [JAHR] verifizieren). Verlangt die
   Anfrage eine solche Bewertung, gib nur aus: "Frage betrifft die Rechtslage
   des Anfragenden – Vorlage an den Berufsträger, kein Schreiben erzeugt."

AUFGABE
Erzeuge drei Ergebnisse: (a) die Einordnung des konkret angefragten
Sachverhalts, (b) ein Antwortschreiben an den Mandanten in dessen Sprache,
(c) eine Liste dessen, was anstelle eines Auftragsverarbeitungsvertrags sinnvoll
und richtig ist.

SACHVERHALT
- Mandant: [MANDANT A], Rechtsform: [ANGABE], Branche: [ANGABE]
- Anfrage gestellt von: [Mandant selbst / Datenschutzbeauftragter des Mandanten /
  IT-Dienstleister des Mandanten / Konzernmutter / Wirtschaftsprüfer / unbekannt]
- Form der Anfrage: [Vertragsentwurf zur Unterschrift / Fragebogen /
  E-Mail-Anfrage / Anforderung im Rahmen einer Zertifizierung / mündlich]
- Betroffene Leistung der Kanzlei: [Finanzbuchführung / Lohn- und
  Gehaltsabrechnung / Jahresabschluss / Steuererklärungen /
  betriebswirtschaftliche Auswertungen / Beratung / mehrere]
- Leistungsgegenstand laut vorgelegtem Entwurf: [ANGABE oder "kein Entwurf"]
- Auftragsgrundlage: [Steuerberatungsvertrag / Einzelauftrag /
  Allgemeine Auftragsbedingungen / unklar]
- Erbringt die Kanzlei für diesen Mandanten reine Erfassungs-, Schreib- oder
  IT-Leistungen ohne eigene fachliche Verantwortung:
  [nein / ja / unklar]
  wenn ja, nämlich: [ANGABE]
- Anlass oder Frist der Anfrage: [ANGABE]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Gegenstand der Anfrage bestimmen. Halte fest, welche Leistung gemeint ist und
   ob die Anfrage überhaupt einen Auftragsverarbeitungsvertrag verlangt oder nur
   Auskunft für das Verarbeitungsverzeichnis des Mandanten. Beides wird häufig
   verwechselt und führt zu unterschiedlichen Antworten.
2. Regeleinordnung. Ordne die angefragte Leistung als steuerberatende Tätigkeit
   ein und leite daraus die Verantwortlichenstellung der Kanzlei ab
   (§ 11 Abs. 2 StBerG, Art. 4 Nr. 7 DSGVO – für [JAHR] verifizieren). Ergebnis
   in genau dieser Form:
   "Auftragsverarbeitung: [nein / ausnahmsweise ja / nicht entscheidbar]".
3. Ausnahmeprüfung – der einzige Prüfpfad, der von der Regel wegführt. Prüfe, ob
   die angefragte Leistung ausnahmsweise eine reine Hilfstätigkeit ohne eigene
   fachliche Verantwortung ist, die die Kanzlei nach Weisung des Mandanten
   erbringt und die nicht zur steuerberatenden Tätigkeit gehört – etwa reines
   Erfassen oder Digitalisieren vorgegebener Daten, ein reiner Schreibauftrag,
   die bloße Bereitstellung von IT oder Speicherplatz für den Mandanten. Prüfe
   dazu: Wer bestimmt Zweck und Mittel der Verarbeitung? Trifft die Kanzlei eine
   eigene fachliche Entscheidung? Haftet sie für das fachliche Ergebnis?
   Erbringt die Kanzlei die Leistung nur, weil und soweit ein steuerliches
   Mandat besteht, bleibt es bei der Regel. Erzwinge keine Ausnahme; ist die
   Antwort unklar, lautet das Ergebnis "nicht entscheidbar" und der Vorgang geht
   an den Berufsträger.
4. Wirkung eines gleichwohl geschlossenen Vertrags. Halte in der internen Notiz
   fest, welche Folgen ein unterzeichneter Auftragsverarbeitungsvertrag hätte:
   Er würde ein Weisungsrecht des Mandanten begründen, das der weisungsfreien
   Verarbeitung nach § 11 Abs. 2 StBerG widerspricht, und die Rollenverteilung
   gegenüber der Aufsichtsbehörde unzutreffend abbilden
   (§ 11 Abs. 2 StBerG, Art. 28 DSGVO – für [JAHR] verifizieren). Nenne keine
   Bußgeldhöhe und keinen Betrag.
5. Antwortschreiben. Sie-Form, höchstens 350 Wörter, sachlich und ohne
   Belehrung. Es
   a) nimmt die Anfrage ernst und benennt sie,
   b) erklärt in einem Satz ohne Fachbegriff, warum die Kanzlei
      Verantwortliche ist und nicht Auftragsverarbeiterin,
   c) nennt die Rechtsgrundlage einmal, mit Absatz, im Klammerzusatz,
   d) sagt ausdrücklich, dass die Kanzlei den vorgelegten Vertrag nicht
      unterzeichnet, und dass darin keine Ablehnung des Datenschutzes liegt,
   e) bietet an, was stattdessen möglich ist – Angaben für das
      Verarbeitungsverzeichnis des Mandanten, Auskunft über technische und
      organisatorische Maßnahmen, Bestätigung der Verschwiegenheit,
   f) nennt einen Ansprechpartner als Leerfeld und ein Datum als Leerfeld.
   Wird das Ergebnis "ausnahmsweise ja" oder "nicht entscheidbar" ermittelt,
   erzeuge KEIN Antwortschreiben, sondern den Satz: "Einordnung nicht im
   Regelfall – Vorlage an den Berufsträger, kein Schreiben erzeugt."
6. Was stattdessen sinnvoll ist. Erzeuge eine Liste von höchstens acht Punkten,
   je mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren". Nimm auf:
   die berufsrechtliche Verschwiegenheit als eigenständige und weitergehende
   Bindung (§ 57 Abs. 1 StBerG, § 203 Abs. 1 Nr. 3 StGB); die Verpflichtung der
   Beschäftigten der Kanzlei in Textform (§ 62 StBerG); die berufsrechtliche
   Einbindung eigener Dienstleister der Kanzlei, für die im Verhältnis zu diesen
   sehr wohl Verträge zu schließen sind (§ 62a StBerG); technische und
   organisatorische Maßnahmen und ihre Darstellbarkeit gegenüber dem Mandanten
   (Art. 32 DSGVO); die wechselseitigen Angaben für die
   Verarbeitungsverzeichnisse (Art. 30 DSGVO); die Information des Mandanten
   über die Datenverarbeitung der Kanzlei (Art. 13 und 14 DSGVO). Lasse weg, was
   im geschilderten Sachverhalt nicht passt.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar, und benenne fehlende
   Angaben.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
   Absatz und Satz und dem Zusatz "für [JAHR] verifizieren". Erfinde keine
   Fundstelle; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Erzeuge keinen Vertragstext, keine Klausel und keine Vertragsanlage.
4. Nenne keine Bußgeldhöhe, keinen Betrag und keine Frist als Zahl.
5. Trenne sichtbar zwischen dem, was an den Mandanten geht, und der internen
   Notiz.

ABBRUCHREGEL
Ein Streit über den Vertrag, eine gesetzte Frist oder der Hinweis des Mandanten,
er werde das Mandat sonst beenden, sind KEIN Abbruchgrund – das ist der
Normalfall dieser Anfrage. Brich nur ab, wenn die Angaben (a) ein laufendes
Verfahren einer Datenschutzaufsichtsbehörde GEGEN DIE KANZLEI, (b) einen
Datenschutzvorfall IN DER SPHÄRE DER KANZLEI, (c) einen gegen die Kanzlei
geltend gemachten Schadensersatzanspruch oder (d) ein Straf- oder
Ermittlungsverfahren gegen die Kanzlei oder eine Person in der Kanzlei
erwähnen. Ein Vorfall, eine Prüfung oder eine Zertifizierung beim Mandanten ist
der typische Anlass dieser Anfrage und kein Abbruchgrund; vermerke ihn in der
internen Notiz. Gib im Abbruchfall nur aus: "Abbruchgrund liegt vor (Buchstabe
angeben) – Bearbeitung an dieser Stelle abgebrochen, Prüfung durch einen
Berufsträger außerhalb des KI-Werkzeugs."

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit und fehlende Angaben"
2. "Gegenstand der Anfrage" – Vertrag oder bloße Auskunft
3. Ergebniszeile: "Auftragsverarbeitung:
   [nein / ausnahmsweise ja / nicht entscheidbar]" mit Begründung in höchstens
   drei Sätzen
4. "Ausnahmeprüfung": Kriterium | Feststellung | Folge
5. "Antwortschreiben (Entwurf)"
6. "Was stattdessen sinnvoll ist": Nr. | Maßnahme | Rechtsgrundlage mit Zusatz |
   zuständig | erledigt (leer)
7. "Interne Notiz": Wirkung eines gleichwohl geschlossenen Vertrags,
   Abgrenzung zu § 62a StBerG und Prompt 103, offene Punkte
8. "Was ich nicht sicher weiß"
```

## Anwendung

1. Zuerst klären, was der Absender tatsächlich braucht. Sehr häufig will er nur Angaben für sein eigenes Verarbeitungsverzeichnis oder die Bestätigung, dass die Kanzlei die Daten schützt – dafür genügt eine Auskunft, und der Vertragsentwurf erledigt sich.
2. Den vorgelegten Entwurf nicht überarbeiten und nicht „entschärfen". Wer Klauseln verhandelt, akzeptiert die Rollenverteilung, die er gerade bestreitet.
3. Antwortschreiben von einem Berufsträger zeichnen lassen. Es geht regelmäßig an den Datenschutzbeauftragten des Mandanten, nicht an den Mandanten selbst – Ton und Adressat entsprechend prüfen.
4. Die Kernaussage einmal als Kanzleistandard hinterlegen, damit nicht jede Anfrage neu entschieden wird. Danach ist dieser Prompt nur noch für Zweifelsfälle nötig.
5. Erbringt die Kanzlei für einen Mandanten tatsächlich reine Hilfsleistungen ohne fachliche Verantwortung, gehört diese Leistung ohnehin gesondert beauftragt und gesondert dokumentiert; der Berufsträger entscheidet dann getrennt über die datenschutzrechtliche Rolle.
6. Ergebnis in der Mandantenakte ablegen und im Verarbeitungsverzeichnis vermerken. Für die eigenen Dienstleister der Kanzlei gilt Prompt 103.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Einordnung und Antwortschreiben sind Entwürfe. Eine zweite Person prüft, ob die Ergebniszeile zur Begründung passt und ob das Schreiben keine Zusage enthält, die die Kanzlei nicht einhalten kann. **Die Freigabe erteilt ausnahmslos ein Berufsträger** (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Keine Weichzeichnung der Kernaussage.** Formulierungen wie „umstritten", „nach überwiegender Auffassung" oder „für die Lohnabrechnung wird teilweise anderes vertreten" sind zu streichen. § 11 Abs. 2 StBerG erfasst sämtliche Mandantendaten.
- **Kein Vertragstext im Ergebnis.** Enthält die Antwort eine Klausel, einen Vertragszusatz oder eine überarbeitete Fassung des vorgelegten Entwurfs, ist sie zu verwerfen – auch dann, wenn sie inhaltlich gut aussieht.
- **Ausnahme nicht großzügig annehmen.** Eine Leistung, die die Kanzlei nur erbringt, weil ein steuerliches Mandat besteht, ist keine reine Hilfstätigkeit. Bleibt die Zuordnung unklar, lautet das Ergebnis „nicht entscheidbar", und es geht kein Schreiben hinaus.
- **§ 62a StBerG nicht verwechseln.** Er verpflichtet die Kanzlei gegenüber ihren eigenen Dienstleistern. Eine Antwort, die daraus eine Pflicht gegenüber dem Mandanten ableitet, ist falsch.
- **Keine Bewertung fremder Rechtslage.** Die Antwort beschreibt die Rolle der Kanzlei. Bewertet sie die datenschutzrechtlichen Pflichten des Mandanten, seiner Konzernmutter oder eines Dritten, ist die Stelle zu streichen: Das ist Rechtsberatung außerhalb der Befugnis nach § 33 StBerG und allenfalls Nebenleistung nach § 5 Abs. 1 RDG.
- **Rechtsstand prüfen an:** § 11 Abs. 2 StBerG, § 33 StBerG, § 57 Abs. 1 StBerG, § 62 StBerG und § 62a StBerG, § 5 Abs. 1 RDG sowie § 203 Abs. 1 Nr. 3 StGB im amtlichen Volltext (gesetze-im-internet.de), an Art. 4 Nr. 7, Art. 13, 14, 28, 30 und 32 DSGVO, an den Hinweisen der Bundessteuerberaterkammer zum Datenschutz in ihrer jeweils aktuellen Fassung sowie an DATEV LEXinform.

## Varianten

- **Nur Auskunft:** „Der Mandant braucht keine Vertragsunterschrift, sondern Angaben für sein Verarbeitungsverzeichnis. Erzeuge ausschließlich diese Angaben nach Art. 30 DSGVO, ohne Antwortschreiben."
- **Fragebogen:** „Beantworte den beigefügten Fragebogen des Mandanten Frage für Frage, mit dem Hinweis auf die Verantwortlichenstellung dort, wo die Frage von einer Auftragsverarbeitung ausgeht. Beantworte nur die Fragen, die die Kanzlei betreffen; Fragen zur Rechtslage des Mandanten bleiben unbeantwortet und werden als solche gekennzeichnet."
- **Konzernmandat:** „Der Fragebogen kommt von der Konzernmutter des Mandanten. Ergänze einen Absatz, dass die Kanzlei nur gegenüber ihrem Mandanten auskunftspflichtig ist, und formuliere den Weg über den Mandanten."
- **Zweitschreiben:** „Der Mandant besteht nach der ersten Antwort weiter auf der Unterschrift. Entwirf ein zweites Schreiben, das den Standpunkt ohne neue Begründung bekräftigt und ein Gespräch anbietet."
- **Mandanteninformation:** „Erzeuge einen Absatz für die allgemeine Mandanteninformation, der die Rollenverteilung vorab erklärt, ohne Werbeaussage."
- **Eigene Dienstleister:** Prompt 103. **Auskunftsersuchen:** Prompt 77.
