# 56 – Offenlegung im Unternehmensregister: Fristenplan und Ordnungsgeldabwehr

**Problem:** Die Offenlegung läuft über das Unternehmensregister, Mandanten reagieren erst auf die Androhung des Bundesamts für Justiz – dann muss es sofort gehen, und niemand weiß, was jetzt noch hilft.
**Rolle:** Kanzleiorganisation, Sekretariat, Berufsträger (Freigabe)
**DATEV-Bezug:** DATEV Bilanzbericht (Offenlegungsdatensatz), DATEV Eigenorganisation comfort (Fristenkontrolle), DATEV DMS
**Was du bereitstellen musst:** Rechtsform, Geschäftsjahr, Bilanzsumme, Umsatzerlöse und Arbeitnehmerzahl der drei Jahre; Stand der Feststellung; Offenlegungshistorie; bei einer Androhung das Schreiben des Bundesamts für Justiz mit Datum, Adressat und Zugangsnachweis.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Steuernummer, Registernummer und Namen der Organmitglieder durch Platzhalter ersetzen (`Gesellschaft A`, `Organmitglied 1`); Aktenzeichen vollständig entfernen und nur mit `Aktenzeichen liegt vor` kennzeichnen. Für die Prüfung genügen Kennzahlen und Zeitpunkte. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist erfahrene Kanzleimitarbeiterin und organisierst Offenlegungen. Du
arbeitest nach Prüfschema, berechnest nichts und beruhigst nicht.

AUFGABE
Teil A: Fristen- und Zuständigkeitsmatrix. Teil B: Prüfschema und Entwürfe zur
Reaktion auf eine Androhung des Bundesamts für Justiz.

MANDANTENRAHMEN
- Rechtsform: [GmbH / UG / AG / GmbH & Co. KG / eG / e. K. / …]
- Größenklasse: [kleinst / klein / mittelgroß / groß]
- Geschäftsjahr: [VON BIS]
- Bilanzsumme, Umsatzerlöse, Arbeitnehmerzahl, drei Jahre: [WERTE]
- Abschluss festgestellt: [ja mit DATUM / nein / unklar]
- Offenlegung dieses Jahres: [erfolgt / teilweise / nicht erfolgt]
- Anlass: [Regelfall / Androhung / Ordnungsgeld festgesetzt]

DATEN, SOWEIT VORHANDEN
1. Schreiben des Bundesamts für Justiz: [WORTLAUT ODER ZUSAMMENFASSUNG]
2. Adressat, Zugangsart, Zugangsnachweis: [ANGABEN]
3. Offenlegungshistorie: [ANGABEN]

TEIL A – FRISTEN- UND ZUSTÄNDIGKEITSMATRIX
Tabelle mit den Spalten: Rechtsform | Größenklasse | offenlegungspflichtig |
Umfang der offenzulegenden oder hinterzulegenden Unterlagen | Fristart ohne
Datum und Dauer | Übermittlungsweg | verantwortlich | Rechtsgrundlage.
Behandle getrennt: Kleinstgesellschaften (Hinterlegung), kleine, mittelgroße,
große Gesellschaften, haftungsbeschränkte Personengesellschaften. Prüfe Befreiungs- und Erleichterungstatbestände mit
Rechtsgrundlage. Halte fest: Die Offenlegung verantworten die gesetzlichen
Vertreter; die Kanzlei übermittelt nur, soweit beauftragt.

TEIL B – REAKTION AUF EINE ANDROHUNG
PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Ist das Schreiben zugegangen? Wann, wie, an welche Adresse?
2. Wem gegenüber ergeht die Androhung: der Gesellschaft, den Organmitgliedern,
   beiden? Ist die Kanzlei Adressat?
3. Welche Frist setzt das Schreiben? Entnimm Fristbeginn und Fristende
   ausschließlich dem Schreiben, rechne nichts nach und kennzeichne die Angabe
   als übernommen und von einem Menschen zu prüfen. Stelle getrennt dar, welche
   Wirkung eine Nachholung innerhalb dieser Frist auf die Festsetzung des
   Ordnungsgeldes hat und welche sie auf die Verfahrenskosten hat, je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren".
4. Ist die Offenlegung inzwischen nachgeholt – welches Geschäftsjahr, welcher
   Umfang, welcher Weg, welcher Nachweis?
5. Welcher Betrag ist angedroht oder festgesetzt? Nenne ihn nur als
   nachzuschlagende Größe (Ordnungsgeldrahmen – für [JAHR] verifizieren).
6. Welche Handlungsmöglichkeiten bestehen: Nachholung, Stellungnahme,
   Rechtsbehelf, Antrag zur Kostenfolge? Je mit Rechtsgrundlage.

VOR DEN ENTWÜRFEN
Benenne zuerst, welcher Rechtsbehelf gegen welche Maßnahme statthaft ist, an
welche Stelle er zu richten ist und wer über ihn entscheidet, je mit
Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren". Erst danach der
Entwurf. Ist die statthafte Rechtsbehelfsart nicht sicher bestimmbar, gib den
Entwurf nicht aus, sondern nur die offene Frage.

ENTWÜRFE, GETRENNT UND ALS ENTWURF GEKENNZEICHNET
7. Stellungnahme an das Bundesamt für Justiz: sachlich, ohne Schuldzuweisung,
   mit nachgeholter Handlung und Nachweisen.
8. Rechtsbehelf mit Wiedereinsetzungsargumentation – GETRENNTER PUNKT.
   Unterscheide die Nachholung von der Wiedereinsetzung in den vorigen Stand.
   Behaupte weder Verschulden noch fehlendes Verschulden; liste auf, welche
   Tatsachen vorzutragen und zu belegen wären, mit Rechtsgrundlage. Setze
   darüber: "Wiedereinsetzung ist Berufsträgersache – Vortrag, Begründung und
   Einlegung verantwortet ein Berufsträger."
9. Mandanteneskalationsschreiben: Sie-Form, höchstens 200 Wörter, benennt
   Mitwirkung, Zuständigkeit der Vertreter und nächsten Schritt, ohne Frist
   und Betrag.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben.
2. Berechne KEINE Fristen und keine Fristenden. Fristbeginn und Fristende
   übernimm nur, soweit sie im Schreiben stehen, gekennzeichnet als übernommen
   und von einem Menschen zu prüfen. Liste im Übrigen auf, WELCHE Fristen im
   Raum stehen, je mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren",
   ohne Datum und ohne Dauer. Ergänze bei jeder: "Frist von einem Menschen zu
   berechnen und im Fristenprogramm zu erfassen." Die Wirkung einer Nachholung
   und die Folgen einer Versäumnis unterdrücke NICHT, sondern benenne sie je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren" – ohne sie als
   feststehend zu behaupten.
3. Nenne Ordnungsgeldbeträge, Kosten und Fristlängen nur als nachzuschlagende
   Größen mit dem Zusatz "für [JAHR] verifizieren".
4. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
   Satz oder Verlautbarung mit Datum) mit dem Zusatz "für [JAHR] verifizieren".
   Erfinde keine Paragrafen und keine Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
5. Formuliere jede Aussage zu Zugang und Ursache der Verspätung als Vermutung,
   solange sie nicht aus den Angaben folgt.
6. ABBRUCHREGEL: Deutet das Material auf ein Organisationsversagen der Kanzlei
   hin, arbeite NICHT weiter. Gib nur aus: "Anzeichen für einen Haftungsfall –
   Bearbeitung abgebrochen, Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs."

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Matrix aus Teil A
3. Liste der Fristarten mit Rechtsgrundlage
4. Prüfprotokoll Teil B, Schritte 1 bis 6
5. Statthafter Rechtsbehelf, Adressat und entscheidende Stelle, je mit
   Rechtsgrundlage – oder die offene Frage, wenn nicht sicher bestimmbar
6. Entwurf Stellungnahme
7. Entwurf Rechtsbehelf mit Wiedereinsetzungsargumentation
8. Entwurf Mandantenschreiben
9. Interne Notiz, abhakbar mit ☐
10. Was ich nicht sicher weiß
```

## Anwendung

1. Kennzahlen der drei Jahre und die Offenlegungshistorie bereitlegen – sonst ist der Umfang nicht bestimmbar.
2. Teil A je Rechtsformgruppe ausführen, als Kanzleimatrix sichern, die Fristarten in DATEV Eigenorganisation comfort anlegen und von einem Menschen terminieren.
3. Im Androhungsfall zuerst die Nachholung prüfen – sie steht vor jeder Argumentation.
4. Offenlegungsdatensatz aus DATEV Bilanzbericht erzeugen, Übermittlungsprotokoll in DATEV DMS ablegen – ohne Protokoll ist die Nachholung nicht nachweisbar.
5. Entwürfe dem Berufsträger vorlegen, nicht versenden.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Verwendung prüfen: Adressat und Zugang, Geschäftsjahr, Umfang der Unterlagen, Nachweise.
- **Fristen berechnet und erfasst ein Mensch**, bei Rechtsbehelfsfristen ausnahmslos eine zweite Person zur Nachprüfung. Kein Datum aus der KI-Antwort übernehmen – auch nicht das aus dem Schreiben übernommene; es ist am Original abzulesen.
- **Rechtsbehelfsart und Zuständigkeit vor dem Entwurf klären.** Gegen welche Maßnahme welcher Rechtsbehelf statthaft ist, an welche Stelle er zu richten ist und wer entscheidet, prüft ein Berufsträger am Gesetzestext; ist das unklar, geht kein Entwurf hinaus.
- **Wiedereinsetzung ist Berufsträgersache.** Über Rechtsbehelf und Begründung entscheidet ein Berufsträger; der KI-Entwurf ist Materialsammlung.
- **Vier-Augen-Prinzip und Freigabe:** Eine zweite Person prüft Umfang und Übermittlungsnachweis; jedes Schreiben nach außen gibt ein Berufsträger frei, die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** §§ 325, 325a, 326, 327, 328, 329, 335, 335a HGB sowie § 264 Abs. 1 Satz 4 und 5 und § 267a HGB im amtlichen Volltext (gesetze-im-internet.de), den Hinweisen des Bundesamts für Justiz zum Ordnungsgeldverfahren, DATEV LEXinform.

## Varianten

- **Kleinstgesellschaft:** Zusatz "Prüfe die Hinterlegung als Alternative."
- **Mehrere Jahre offen:** Zusatz "Behandle jedes offene Geschäftsjahr als eigenen Fall, geordnet nach Dringlichkeit, ohne Fristen zu berechnen."
- **Kanzleiorganisation:** Zusatz "Leite eine Arbeitsanweisung ab, die den Offenlegungslauf jährlich auslöst." Ergänzt Prompt 23.
