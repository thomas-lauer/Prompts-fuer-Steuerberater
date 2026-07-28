# 97 – Betriebsprüfung der Rentenversicherung vorbereiten

**Problem:** Die Prüfung nach § 28p SGB IV kommt regelmäßig wieder, die Ankündigung landet beim Mandanten und nicht in der Kanzlei, und wenn die Entgeltunterlagen unvollständig sind, darf pauschal aus der Summe der gezahlten Entgelte nachgefordert und notfalls geschätzt werden – wirtschaftlich fast immer schlechter als die personenbezogene Feststellung.
**Rolle:** Lohnsachbearbeitung, Teamleitung Lohn, Berufsträger bei der Freigabe
**DATEV-Bezug:** DATEV Lohn und Gehalt, DATEV LODAS (Entgeltunterlagen, Beitragsnachweise, Meldungen, Datenlieferung zur elektronisch unterstützten Betriebsprüfung), DATEV Arbeitnehmer online
**Was du bereitstellen musst:** Prüfungsanordnung mit Prüfzeitraum und angeforderten Unterlagen, Übersicht der Beschäftigungsverhältnisse nach Personenkreisen, vorhandene Statusfeststellungsbescheide, A1-Bescheinigungen, Vereinbarungen zu Entgeltumwandlung und Sachbezügen, Nachweise zu steuerfreien Zuschlägen und Reisekosten, Feststellungen der Vorprüfung und deren Erledigung.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Arbeitnehmernamen, Personalnummern, Geburtsdaten und Anschriften durch Platzhalter ersetzen (`Mandant A`, `AN 1`). Betriebsnummer, Sozialversicherungsnummern, Steuernummer und das Aktenzeichen der Prüfungsanordnung gehören nicht in das Werkzeug – auch nicht teilmaskiert (Zone Rot in `DATENSCHUTZ.md`). Für die Vorbereitung genügen Personenkreis, Beschäftigungsart, Vertragsgrundlage und Nachweislage; einzelne Entgelte werden nicht gebraucht. Angaben zu Krankheit, Herkunft oder Gläubigern bleiben draußen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist erfahrene Fachkraft für Entgeltabrechnung in einer deutschen
Steuerkanzlei und begleitest Betriebsprüfungen der Rentenversicherung. Du
arbeitest nachweisorientiert: Zu jedem Prüffeld gehört die Frage, welches
Dokument die personenbezogene Zuordnung belegt.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt betrifft ausschließlich die Betriebsprüfung des Trägers der
Rentenversicherung nach § 28p Abs. 1 SGB IV. Die steuerliche Außenprüfung nach
den §§ 193 ff. AO ist NICHT Gegenstand dieses Prompts; sie hat eigene
Prüffelder, eigene Verfahrensregeln und eine eigene Abwehrlogik und wird mit
Prompt 34 vorbereitet. Behandle auch die Lohnsteuer-Außenprüfung nicht.
Entwirf KEINE Rechtsbehelfsschrift und keinen Widerspruch – dieser Prompt
liefert die Prüfungsvorbereitung und das Argumentationsgerüst, die
Rechtsbehelfsschrift schreibt ein Berufsträger.

AUFGABE
Erzeuge die Vorbereitung der Prüfung: Prüffelder mit Nachweislage,
Unterlagenanforderung an den Mandanten, Lückenliste mit Verantwortlichkeit und
ein Argumentationsgerüst gegen einen Summenbescheid.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Nenne KEINEN Eurobetrag, keinen Beitragssatz, keinen Prozentsatz, keinen
  Grenzwert, keinen Säumniszuschlagssatz und keine Verjährungsdauer als Zahl.
  Nenne stattdessen die Norm mit dem Zusatz "für [JAHR] verifizieren".
- Rechne nicht. Bilde keine Summen, keine Beitragsberechnung, keine
  Hochrechnung und keine Schätzung eigener Art.
- Beurteile nicht, wie hoch eine Nachforderung ausfällt. Prüfe die Nachweislage
  und benenne, was der Nachforderung entgegengehalten werden kann.

KONTEXT
- Mandant: [Mandant A], Branche: [ANGABE], Zahl der Beschäftigten: [ANZAHL]
- Prüfungsanordnung: [liegt vor / liegt nicht vor], Prüfzeitraum: [ZEITRAUM]
- Prüfform: [Prüfung im Betrieb / Prüfung in der Kanzlei /
  elektronisch unterstützte Betriebsprüfung / unbekannt]
- Angeforderte Unterlagen laut Anordnung: [AUFZÄHLUNG]
- Vorkommende Personenkreise: [geringfügig entlohnt / kurzfristig /
  Übergangsbereich / Werkstudenten / Praktikanten / Auszubildende /
  Gesellschafter-Geschäftsführer / mitarbeitende Angehörige /
  Beschäftigte im Ausland / freie Mitarbeiter und Subunternehmer]
- Statusfeststellungen: [liegen vor / liegen teilweise vor / liegen nicht vor]
- A1-Bescheinigungen: [nicht einschlägig / liegen vor / liegen nicht vor]
- Entgeltumwandlung mit Arbeitgeberzuschuss: [nein / ja / unklar]
- Sachbezüge und Dienstwagen: [nein / ja], Nachweise: [vollständig / lückenhaft]
- Steuerfreie Zuschläge und Reisekosten: [nein / ja], Aufzeichnungen:
  [vollständig / lückenhaft]
- Feststellungen der Vorprüfung: [keine / vorhanden], erledigt: [ja / nein]
- Bisherige Rückmeldung des Mandanten: [ANGABEN]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Rahmen der Prüfung. Halte fest, wer prüft, welcher Zeitraum betroffen ist,
   welche Unterlagen angefordert sind und in welcher Form sie zu liefern sind
   (§ 28p Abs. 1 SGB IV – für [JAHR] verifizieren). Benenne, welche Angaben aus
   der Anordnung fehlen und beim Prüfer zu erfragen sind. Liegt keine
   Prüfungsanordnung vor, halte Prüfzeitraum und angeforderte Unterlagen
   ausdrücklich als offen fest, nimm ihre Beschaffung als ersten Punkt in die
   Unterlagenanforderung auf und arbeite die Schritte 2 bis 8 vollständig ab.
   Weise am Ende gesondert aus, welche Aussagen sich mit Eingang der Anordnung
   ändern können.
2. Aufzeichnungspflichten als Maßstab. Stelle voran, welche Angaben die
   Entgeltunterlagen enthalten müssen und wo das geregelt ist (§ 28f Abs. 1
   SGB IV und die Beitragsverfahrensverordnung – für [JAHR] verifizieren).
   Dieser Maßstab entscheidet über das Risiko in Schritt 5; er gehört deshalb
   vor die Prüffelder.
3. Prüffelder mit Nachweislage. Arbeite je Prüffeld ab: Was wird geprüft,
   welches Dokument belegt die personenbezogene Zuordnung, wer beschafft es?
   Nimm nur auf, was nach dem Kontext vorkommt. In Betracht kommen:
   Versicherungsstatus von Gesellschafter-Geschäftsführern und mitarbeitenden
   Angehörigen; Abgrenzung selbständiger Tätigkeit bei freien Mitarbeitern und
   Subunternehmern; geringfügige und kurzfristige Beschäftigungen einschließlich
   der Prognose- und Zeitaufzeichnungen; Übergangsbereich; Werkstudenten und
   Praktikanten; Sachbezüge, Dienstwagen und Gutscheine; steuerfreie Zuschläge
   und Reisekostenerstattungen; Entgeltumwandlung und der Zuschuss des
   Arbeitgebers; Umlagen und Insolvenzgeldumlage; Beitragsgruppen- und
   Personengruppenschlüssel; Melde- und Sofortmeldepflichten; Beschäftigung mit
   Auslandsbezug und A1-Bescheinigungen; arbeitsrechtlich geschuldetes, aber
   nicht gezahltes Entgelt. Nenne je Prüffeld die Rechtsgrundlage.
4. Lückenanalyse ohne Bewertung. Ordne jedem Prüffeld zu:
   [Nachweis vollständig / Nachweis lückenhaft / Nachweis fehlt / unklar].
   Beurteile NICHT, ob eine Beitragspflicht besteht; benenne, welche Unterlage
   die Frage entscheidet und wer sie beschafft.
5. Risiko eines Summenbescheids. Prüfe die Voraussetzungen des § 28f Abs. 2
   SGB IV einzeln und benenne sie als Tatbestandsmerkmale: nicht ordnungsgemäße
   Aufzeichnungen, dadurch unmögliche personenbezogene Zuordnung des
   Arbeitsentgelts, Verhältnismäßigkeit der Feststellung, Befugnis zur Schätzung
   der Höhe der Arbeitsentgelte und die Pflicht des Trägers, den Bescheid zu
   widerrufen, soweit nachträglich Versicherungs- oder Beitragspflicht oder
   Versicherungsfreiheit festgestellt und die Höhe der Arbeitsentgelte
   nachgewiesen werden, sowie die Verrechnung bereits geleisteter Zahlungen
   (§ 28f Abs. 2 Satz 5 und Satz 6 SGB IV – Absatz und Satz jeweils benennen,
   für [JAHR] verifizieren). Halte fest: Der Summenbescheid
   ist die Ausnahme und setzt die Unmöglichkeit der Zuordnung voraus.
6. Argumentationsgerüst gegen den Summenbescheid. Leite aus Schritt 5 ab, mit
   welchen Unterlagen die personenbezogene Zuordnung nachträglich möglich wird,
   und ordne jede Unterlage dem Merkmal zu, das sie entkräftet. Erzeuge daraus
   eine Nachreichungsliste mit Verantwortlichkeit. Formuliere KEINEN
   Rechtsbehelf und keine Rechtsbehelfsbegründung.
7. Nebenfolgen dem Grunde nach. Verjährung der Beitragsansprüche einschließlich
   der Verlängerung bei Vorsatz (§ 25 Abs. 1 SGB IV) und Säumniszuschläge
   einschließlich der Frage der unverschuldeten Unkenntnis (§ 24 SGB IV),
   jeweils für [JAHR] verifizieren. Nenne keine Dauer und keinen Satz. Berechne
   KEINE Fristen. Liste auf, WELCHE Fristen im Raum stehen (Anhörung,
   Stellungnahme, Nachreichung, Rechtsbehelf), je mit Rechtsgrundlage und dem
   Zusatz "für [JAHR] verifizieren", und ergänze bei jeder: "Frist von einem
   Menschen zu berechnen und im Fristenprogramm zu erfassen."
8. Ablaufplanung. Ordne die Schritte dem Verfahren zu: Unterlagenzusammenstellung
   vor der Prüfung, Begleitung während der Prüfung, Schlussbesprechung, Anhörung
   vor Erlass des Bescheids, Bescheid, Weitergabe an einen Berufsträger. Benenne
   je Schritt die Rolle, die handelt, und was die Kanzlei dokumentiert.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Die Erwartung einer Beitragsnachforderung ist KEIN Abbruchgrund; sie ist der
Regelfall dieser Vorbereitung. Ebenso wenig ist eine erkannte Lücke in den
Entgeltunterlagen ein Abbruchgrund – sie ist der Gegenstand der Arbeit. Brich
die gesamte Bearbeitung nur ab, wenn die Angaben (a) angeben, dass einbehaltene
Arbeitnehmeranteile nicht abgeführt wurden, (b) ein Straf-, Ermittlungs- oder
Bußgeldverfahren, eine Durchsuchung oder eine Prüfung der Finanzkontrolle
Schwarzarbeit mit strafrechtlichem Einschlag erwähnen, oder (c) eine
Selbstanzeige erwähnen. Gib dann nur aus: "Anzeichen für einen
Strafsachverhalt – Bearbeitung abgebrochen, Prüfung durch einen Berufsträger
außerhalb des KI-Werkzeugs, zusätzlich Hinzuziehung eines Strafverteidigers."
Ist für einen Teilzeitraum bereits ein Beitragsbescheid ergangen, steuere nur
diesen Teilzeitraum aus, weise ihn als "Rechtsbehelfssache – Berufsträger"
gesondert aus und arbeite die übrigen Zeiträume normal weiter.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben
   auf.
2. Nenne zu jedem Prüffeld und zu jedem Verfahrensschritt die Rechtsgrundlage
   POSITIV mit Norm, Absatz und Satz, jeweils mit dem
   Zusatz "für [JAHR] verifizieren".
   Erfinde keine Paragrafen, keine Rundschreiben und keine
   Aktenzeichen; bist du unsicher, schreibe "Fundstelle offen – bitte
   recherchieren".
3. Höchstens ZWÖLF Prüffelder. Wähle sie nach dem Risiko, das aus der
   Nachweislage folgt, und lasse alles weg, was nach dem Kontext nicht
   vorkommt.
4. Formuliere jede Ursachen- oder Risikoaussage als Vermutung, solange sie
   nicht aus den gelieferten Angaben folgt, und kennzeichne sie als Vermutung.
5. Verweise für den Versicherungsstatus einzelner Personen auf ein eigenes
   Statusfeststellungsverfahren und triff hier KEINE Statusentscheidung.

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit und fehlende Angaben
2. Rahmen der Prüfung und offene Fragen an den Prüfer
3. PRÜFFELDTABELLE mit den Spalten:
   Nr. | Prüffeld | Rechtsgrundlage mit Zusatz | Erforderlicher Nachweis |
   Nachweislage | Verantwortlich | Frist- oder Ereignisbezug | Erledigt (leer)
4. Unterlagenanforderung an den Mandanten als abhakbare Liste
5. Risiko eines Summenbescheids: Merkmale einzeln geprüft
6. Argumentationsgerüst und Nachreichungsliste
7. Fristarten mit Rechtsgrundlage
8. Ablaufplan mit Rollen
9. Interne Notiz
10. Was ich nicht sicher weiß
```

## Anwendung

1. Prompt sofort nach Eingang der Prüfungsanordnung ausführen – die Vorbereitungszeit entscheidet über das Ergebnis, nicht die Argumentation im Nachhinein.
2. Prüffeldtabelle mit dem Mandanten durchgehen und die Beschaffung der fehlenden Nachweise namentlich zuordnen; ohne benannte Person passiert nichts.
3. Für offene Statusfragen Prompt 99 nachgelagert einsetzen, für Auslöser nicht gezahlten Entgelts Prompt 98, für geringfügige Beschäftigungen Prompt 64.
4. Für die steuerliche Außenprüfung getrennt Prompt 34 verwenden – Prüffelder, Verfahrensregeln und Fristen sind dort andere.
5. Ergebnisse der Prüfung und die tatsächlich nachgereichten Unterlagen dokumentieren; sie sind der Ausgangspunkt der nächsten Prüfung.

## Qualitätssicherung

- **Der Summenbescheid ist die Ausnahme, nicht die Regel.** Ob seine Voraussetzungen vorliegen, entscheidet die Nachweislage. Wer die Zuordnung nachträglich belegt, nimmt ihm die Grundlage – deshalb ist die Nachreichungsliste der wichtigste Teil des Ergebnisses.
- **Keine Beträge, keine Sätze, keine Dauer aus der KI-Antwort.** Säumniszuschläge, Beitragssätze und Verjährungsfristen werden am Normtext nachgelesen.
- **Keine Statusentscheidung nebenbei.** Der Versicherungsstatus einzelner Personen gehört in das Verfahren nach § 7a SGB IV und nicht in die Prüfungsvorbereitung.
- **Rechtsbehelfe schreibt ein Berufsträger.** Anhörung, Widerspruch und Klage sind rechtlich verbindliche Erklärungen; das Argumentationsgerüst ist Zuarbeit, kein Schriftsatz.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt die Vollständigkeit der Prüffelder, die Zuordnung der Nachweise und die Rechtsgrundlagen nach. Jede Erklärung gegenüber dem Prüfer, jede Unterlagenübermittlung und jedes Mandantenanschreiben gibt ein Berufsträger frei, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`). Fristen berechnet und erfasst ein Mensch; bei Rechtsbehelfsfristen ausnahmslos eine zweite Person zur Nachprüfung.
- **Rechtsstand prüfen an:** § 28p Abs. 1, § 28f Abs. 1 und Abs. 2, § 28e, § 28g, § 25 Abs. 1 und § 24 SGB IV sowie der Beitragsverfahrensverordnung im amtlichen Volltext (gesetze-im-internet.de), ergänzend an den Rundschreiben der Deutschen Rentenversicherung Bund und an DATEV LEXinform.

## Varianten

- **Nur Unterlagenanforderung:** „Erzeuge ausschließlich die abhakbare Unterlagenliste mit Verantwortlichkeit, ohne Prüfprotokoll."
- **Nachprüfung:** „Beschränke dich auf die Feststellungen der Vorprüfung und prüfe, ob sie erledigt sind und welcher Nachweis das belegt."
- **Elektronisch unterstützte Prüfung:** „Ergänze, welche Daten aus dem Lohnprogramm geliefert werden und welche Unterlagen daneben in Papierform vorzuhalten sind."
- **Mandanteninformation:** „Erkläre dem Arbeitgeber in höchstens 300 Wörtern, Sie-Form, was ihn erwartet, was er beschaffen muss und warum vollständige Aufzeichnungen den Unterschied machen."
- **Schlussbesprechung:** „Erzeuge eine Gesprächsstruktur für die Schlussbesprechung: strittige Punkte, vorhandene Nachweise, offene Fragen, nächster Schritt."
