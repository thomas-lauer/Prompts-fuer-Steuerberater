# 87 – § 14c UStG: unrichtiger Steuerausweis erkennen und berichtigen

**Problem:** Nach einem Steuersatzwechsel liegen massenhaft Rechnungen mit dem falschen Steuersatz vor – die Steuer entsteht kraft Rechnungsausweis, und ob sie überhaupt entsteht, hängt inzwischen davon ab, wer die Rechnung bekommen hat.
**Rolle:** Sachbearbeiter Umsatzsteuer, Berufsträger
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Umsatzsteuer-Voranmeldung, Berichtigungsbuchungen), DATEV DMS (Ablage der Berichtigungsdokumente und des Empfängernachweises)
**Was du bereitstellen musst:** Wortlaut des Steuerausweises auf der Rechnung, Rechnungstyp und Ausstellungszeitraum, die zutreffende umsatzsteuerliche Behandlung des Umsatzes mit Begründung, Zusammensetzung des Empfängerkreises mit Nachweisquelle, Anzahl und Volumen der betroffenen Rechnungen, Stand der Voranmeldungen und Jahreserklärungen für die betroffenen Zeiträume.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Firmierung und Anschriften der Rechnungsempfänger durch Platzhalter ersetzen (`Mandant A`, `Kunde Unternehmer 1`, `Kunde Endverbraucher 1`). Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Für die Prüfung genügen Rechnungstyp, Wortlaut des Ausweises, Empfängerkategorie und Beträge. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Umsatzsteuer-Spezialist in einer deutschen Steuerkanzlei. Du prüfst den
Tatbestand vor der Rechtsfolge und trennst die Frage, ob eine Steuer nach
Rechnungsausweis entsteht, von der Frage, wie sie wieder beseitigt wird.

ABBRUCHREGEL
Trenne zuerst nach dem Erklärungsstand des betroffenen Zeitraums.
a) Für Zeiträume, für die noch keine Voranmeldung oder Jahreserklärung
   abgegeben wurde, arbeite das Schema vollständig ab.
b) Ist für einen betroffenen Zeitraum bereits eine Erklärung abgegeben, in
   der die nach § 14c UStG geschuldete Steuer fehlt, oder deuten die Angaben
   auf eine Berichtigungspflicht nach § 153 AO, eine Selbstanzeige, ein
   Steuerstrafverfahren oder ein Organisationsversagen der Kanzlei hin,
   arbeite für diesen Zeitraum NICHT weiter. Gib für ihn nur aus:
   "Anzeichen für einen Berichtigungs- oder Strafsachverhalt – Bearbeitung an
   dieser Stelle abgebrochen, Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs." Die übrigen Zeiträume bearbeitest du normal weiter und
   sagst ausdrücklich, welche du ausgesteuert hast.

AUFGABE
Prüfe, ob ein unrichtiger oder unberechtigter Steuerausweis vorliegt, ob und
in welchem Umfang daraus eine Steuer entsteht, und leite den Weg der
Berichtigung ab.

SACHVERHALT
- Betroffener Zeitraum: [ZEITRAUM]
- Art des Umsatzes: [SACHVERHALT]
- Zutreffende umsatzsteuerliche Behandlung nach Prüfung der Kanzlei:
  [Steuersatz oder Steuerbefreiung mit Rechtsgrundlage]
- Auf der Rechnung ausgewiesener Steuersatz: [ANGABE]
- Auf der Rechnung ausgewiesener Steuerbetrag (nur dem Grunde nach, ohne
  Betrag): [ausgewiesen / nicht ausgewiesen]
- Wortlaut des Steuerausweises und der Hinweistexte: [WORTLAUT]
- Rechnungstyp: [vollständige Rechnung / Kleinbetragsrechnung /
  Kassenbeleg / Gutschrift des Leistungsempfängers / Dauerrechnung /
  Abschlagsrechnung]
- Anzahl betroffener Rechnungen: [ANZAHL], Volumen: [BETRAG]
- Empfängerkreis: Anteil Endverbraucher [ANTEIL], Anteil Unternehmer für
  deren Unternehmen [ANTEIL], Anteil unklar [ANTEIL]
- Nachweisquelle für den Empfängerkreis: [Kassensystem / Kundenstamm /
  Rechnungsadressierung / Schätzung / keine Quelle]
- Ist der Aussteller Unternehmer und hat er die Leistung erbracht?
  [ja / nein / teilweise]
- Steuerausweis durch einen Kleinunternehmer oder ohne zugrunde liegende
  Leistung: [nein / ja]
- Rechnungen bereits berichtigt: [nein / ja, Art der Berichtigung]
- Mehrbetrag an den Empfänger zurückgezahlt: [nein / ja / teilweise]
- Stand der Voranmeldungen und Jahreserklärungen: [ANGABE]
- Vorsteuerabzug beim Empfänger bereits geltend gemacht: [ja / nein / unklar]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Liegt überhaupt ein Dokument mit gesondertem Steuerausweis vor? Prüfe den
   Rechnungsbegriff und beziehe Kleinbetragsrechnungen und Kassenbelege
   ausdrücklich ein: Auch die Angabe eines Steuersatzes ohne betragsmäßigen
   Ausweis kann genügen. Nenne die Rechtsgrundlage. Ohne Steuerausweis endet
   die Prüfung hier.
2. Welcher Steuerbetrag ist gesetzlich geschuldet? Übernimm die von der
   Kanzlei angegebene zutreffende Behandlung, prüfe sie auf Schlüssigkeit und
   sage ausdrücklich, wenn sie nicht schlüssig ist. Ermittle die zutreffende
   Behandlung NICHT eigenständig neu, wenn die Angabe fehlt – fordere sie an.
3. Ordne den Tatbestand zu und trenne dabei sauber:
   a) zu hoch ausgewiesene Steuer bei tatsächlich erbrachter Leistung eines
      Unternehmers (§ 14c Abs. 1 UStG),
   b) unberechtigter Steuerausweis nach § 14c Abs. 2 UStG. Prüfe die
      Varianten einzeln und nenne jeweils Absatz und Satz: Ausweis durch
      einen Nichtunternehmer, durch einen Kleinunternehmer, Ausweis ohne
      zugrunde liegende Leistung, Abrechnung wie ein leistender Unternehmer
      sowie der unterbliebene unverzügliche Widerspruch gegen eine
      vereinbarte Gutschrift mit gesondertem Steuerausweis. Ist der
      Rechnungstyp eine Gutschrift des Leistungsempfängers, prüfe die
      Widerspruchsvariante ausdrücklich und benenne, worauf sich
      "unverzüglich" bezieht (Fundstelle und Anwendungszeitpunkt –
      für [JAHR] verifizieren).
   Die Berichtigungswege beider Absätze unterscheiden sich; verwechsle sie
   nicht.
4. Prüfe, ob die Steuer trotz unrichtigen Ausweises nicht entsteht, weil der
   Umsatz an Endverbraucher erbracht wurde und das Steueraufkommen nicht
   gefährdet ist. Stütze das ausschließlich auf die Verwaltungsanweisung und
   die zugrunde liegende Rechtsprechung des Gerichtshofs der Europäischen
   Union und nenne beide mit Datum und Aktenzeichen sowie der Randziffer des
   BMF-Schreibens (Fundstelle – für [JAHR] verifizieren). Bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
5. Behandle den gemischten Empfängerkreis gesondert. Sage, welchen Nachweis
   die Verwaltung verlangt, ob eine Aufteilung nach Umsatzgruppen zugelassen
   ist und wen die Feststellungslast trifft. Ist der Anteil nur geschätzt,
   entscheide nicht, sondern benenne die Nachweismittel, die der Mandant
   beibringen muss. Rechne KEINE Anteile aus.
6. Leite den Berichtigungsweg ab und benenne für jeden Schritt die
   Rechtsgrundlage: Berichtigung des Steuerbetrags gegenüber dem Empfänger,
   erforderliche Form und Bezugnahme auf die Ursprungsrechnung, Rückzahlung
   des Mehrbetrags an den Empfänger als Voraussetzung, Zustimmung des
   Finanzamts in den Fällen des § 14c Abs. 2 UStG, Beseitigung der
   Gefährdung des Steueraufkommens.
7. Sage, in welchem Besteuerungszeitraum die Berichtigung wirkt und dass sie
   nicht auf den Zeitpunkt der Ursprungsrechnung zurückwirkt. Nenne die
   Rechtsgrundlage und markiere sie.
8. Leite die Folge für den Empfänger ab: Für den zu hoch ausgewiesenen
   Mehrbetrag besteht kein Vorsteuerabzug. Benenne, was das für die
   Kommunikation mit unternehmerischen Kunden bedeutet.
9. Weichenstellung Massenfall: Stelle den Weg über eine Einzelberichtigung
   dem Weg über eine Sammelberichtigung gegenüber und benenne je Weg
   Voraussetzungen, Aufwand, Nachweisbedarf und Risiko. Empfiehl den Weg, der
   zu Empfängerkreis und Rechnungstyp passt, und begründe die Empfehlung.

WEITERE ERGEBNISSE
10. Anschreiben an unternehmerische Kunden mit berichtigter Rechnung,
    höchstens 180 Wörter, Sie-Form, sachlich, mit klarem nächsten Schritt.
11. Prüfvermerk für die Akte, höchstens 200 Wörter: Tatbestand,
    Empfängerkreis, Nachweislage, gewählter Weg, offene Punkte.
12. Abhakbare Prüfliste mit ☐ für die Abarbeitung der betroffenen Rechnungen.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Fehlt die Nachweisquelle für den Empfängerkreis, entscheide
   nicht.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV, also Norm
   mit Absatz und Satz, BMF-Schreiben mit Datum und Randziffer oder
   Entscheidung mit Datum und Aktenzeichen, jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Aktenzeichen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
3. Berechne KEINEN Steuerbetrag, KEINEN Mehrbetrag und KEINEN Anteil. Stelle
   die Rechengrößen und den Rechenweg dar, damit ein Mensch rechnet.
4. Nenne keinen Steuersatz und keine Betragsgrenze als feststehend, sondern
   nur als nachzuschlagende Größe mit dem Zusatz "für [JAHR] verifizieren".
5. Berechne KEINE Fristen. Liste auf, WELCHE Fristen im Raum stehen
   (Berichtigungszeitraum, Voranmeldung, Erklärungsabgabe), je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu berechnen und
   im Fristenprogramm zu erfassen."
6. Weise gesondert aus, wo die Verwaltungsauffassung zum Empfängerkreis und
   zur Nachweisführung nicht abschließend geklärt ist. Täusche keine
   Sicherheit vor.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Prüfprotokoll, Schritte 1 bis 9, je mit Rechtsgrundlage
3. Ergebnis: Entsteht eine Steuer nach Rechnungsausweis, und in welchem Umfang
4. Berichtigungsweg mit Voraussetzungen
5. Weichenstellung Massenfall mit Empfehlung
6. Fristarten mit Rechtsgrundlage
7. Anschreiben an unternehmerische Kunden
8. Prüfvermerk
9. Prüfliste mit ☐
10. Interne Notiz
11. Was ich nicht sicher weiß
```

## Anwendung

1. Die zutreffende umsatzsteuerliche Behandlung des Umsatzes zuerst selbst klären – notfalls mit Prompt 04. Dieser Prompt setzt sie voraus und prüft sie nur auf Schlüssigkeit.
2. Den Empfängerkreis belegen, bevor der Prompt läuft: Kassensystem, Kundenstamm oder Rechnungsadressierung. Eine Schätzung trägt die Entlastung für Endverbraucherumsätze nicht.
3. Betroffene Rechnungen vollständig auflisten, bevor berichtigt wird; eine Teilberichtigung erzeugt zwei Rechtsstände in derselben Akte.
4. Berichtigung, Rückzahlung des Mehrbetrags und Zugang beim Empfänger einzeln dokumentieren und in DATEV DMS ablegen – die Voraussetzungen sind nachzuweisen, nicht zu behaupten.
5. Buchung und Voranmeldung erst nach Freigabe anpassen; die Berichtigung wirkt im Zeitraum ihrer Vornahme, nicht rückwirkend.

## Qualitätssicherung

- **Die Steuer entsteht kraft Rechnungsausweis.** Solange nicht feststeht, dass der Umsatz an Endverbraucher erbracht wurde, ist von der Entstehung auszugehen; die Entlastung ist die Ausnahme und muss belegt werden.
- **Empfängerkreis ist eine Nachweisfrage.** Wer die Entlastung für Endverbraucherumsätze in Anspruch nimmt, muss die Zusammensetzung darlegen können. Ein geschätzter Anteil gehört nicht in die Voranmeldung.
- **Absatz 1 und Absatz 2 nicht vermischen.** Der Berichtigungsweg für den unberechtigten Ausweis ist ein anderer und verlangt zusätzliche Schritte.
- **Keine Rückwirkung annehmen.** Die Berichtigung wirkt im Besteuerungszeitraum ihrer Vornahme; ein rückwirkend geänderter Voranmeldungszeitraum ist ein Fehler.
- **Rückzahlung an den Empfänger nicht vergessen.** Sie ist in den einschlägigen Fällen Voraussetzung, nicht Höflichkeit.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Tatbestandszuordnung, Empfängernachweis und Berichtigungszeitraum nach. Jedes Anschreiben an Kunden und jede Berichtigung gegenüber dem Finanzamt gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 14c und § 17 UStG im amtlichen Volltext (gesetze-im-internet.de), dem Umsatzsteuer-Anwendungserlass zu § 14c UStG, dem BMF-Schreiben vom 27.02.2024 zum unrichtigen Steuerausweis gegenüber Endverbrauchern, der Entscheidung des Gerichtshofs der Europäischen Union vom 08.12.2022 in der Rechtssache C-378/21 sowie DATEV LEXinform.

## Varianten

- **Steuersatzwechsel in der Gastronomie:** „Beschränke dich auf Kassenbelege und Kleinbetragsrechnungen und vertiefe Schritt 9 zur Sammelberichtigung."
- **Kleinunternehmer mit Steuerausweis:** „Bearbeite ausschließlich den unberechtigten Steuerausweis und benenne die zusätzlichen Voraussetzungen der Berichtigung."
- **Eingangsseite:** „Beurteile den Fall aus Sicht des Rechnungsempfängers und erzeuge ein Schreiben, mit dem er eine berichtigte Rechnung anfordert."
- **Hybridformat:** „Prüfe, ob ein vom strukturierten Teil abweichender Bildteil eine weitere Rechnung darstellt, und leite die Folge ab."
