# 96 – Aktivrente: Voraussetzungen, Nachweise, Abrechnungsfolgen

**Problem:** Seit dem 01.01.2026 (Inkrafttreten – für [JAHR] verifizieren) ist Arbeitslohn aus einer sozialversicherungspflichtigen Beschäftigung nach Erreichen der Regelaltersgrenze bis zu einem Höchstbetrag steuerfrei; die Befreiung greift bereits im Lohnsteuerabzug, die Verwaltungsanweisungen sind dünn, und zu Unrecht steuerfrei gestellter Arbeitslohn führt unmittelbar in die Arbeitgeberhaftung.
**Rolle:** Lohnsachbearbeitung, Berufsträger bei der Freigabe
**DATEV-Bezug:** DATEV Lohn und Gehalt, DATEV LODAS (Personengruppen- und Beitragsgruppenschlüssel, Lohnarten, elektronische Lohnsteuerbescheinigung), DATEV Arbeitnehmer online
**Was du bereitstellen musst:** Arbeitsvertrag oder Änderungsvereinbarung, Angaben zum Erreichen der Regelaltersgrenze und zu einer etwaigen Erklärung über den Verzicht auf die Rentenversicherungsfreiheit, Versicherungsstatus in allen Zweigen, Aufstellung der laufenden und einmaligen Bezüge dem Grunde nach, Angaben zu weiteren Dienstverhältnissen, bisherige Abrechnungspraxis und – falls vorhanden – die Erklärung des Arbeitnehmers zur einmaligen Inanspruchnahme.
**Datensparsamkeit:** Vor dem Einfügen Name, Personalnummer, Geburtsdatum und Anschrift durch Platzhalter ersetzen (`AN 1`, `Mandant A`); statt des Geburtsdatums genügt die Angabe, ob die Regelaltersgrenze erreicht ist. Sozialversicherungsnummer, Rentenversicherungsnummer, Steuer-Identifikationsnummer und Steuernummer gehören nicht in das Werkzeug – auch nicht teilmaskiert (Zone Rot in `DATENSCHUTZ.md`). Aus dem Rentenbescheid wird nichts eingefügt, sondern nur die Tatsache seines Vorliegens; Rentenart und Rentenhöhe werden nicht angegeben, Angaben zu Gesundheit oder Erwerbsminderung bleiben draußen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachkraft für Entgeltabrechnung in einer deutschen Steuerkanzlei und
arbeitest mit DATEV Lohn und Gehalt bzw. DATEV LODAS. Du prüfst Lohnsteuer und
Sozialversicherung getrennt und behandelst eine junge Vorschrift mit dünner
Verwaltungspraxis als das, was sie ist: auslegungsbedürftig.

AUFGABE
Prüfe, ob die Steuerbefreiung nach § 3 Nr. 21 EStG in der Fassung des
Aktivrentengesetzes für dieses Dienstverhältnis in Betracht kommt, welche
Nachweise vor der ersten Anwendung vorliegen müssen und welche Folgen sich für
Abrechnung, Meldungen und Bescheinigung ergeben. Rechtsstand der Norm:
Aktivrentengesetz, BGBl. 2025 I Nr. 361 vom 23.12.2025, in Kraft zum
01.01.2026 (Fundstelle und Fassung – für [JAHR] verifizieren).

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Nenne den Höchstbetrag NICHT als Zahl. Nenne auch keinen anderen Eurobetrag,
  keinen Beitragssatz, keinen Prozentsatz und keine Altersgrenze als Zahl.
  Verweise stattdessen auf die Norm mit dem Zusatz "für [JAHR] verifizieren".
- Rechne nicht. Bilde keine Summen, keine Monats- oder Jahreshochrechnung,
  keine Beitragsberechnung und keine Netto-Hochrechnung.
- Vergleiche keinen Bezug mit dem Höchstbetrag. Formuliere den Vergleich als
  Frage an die Kanzlei und arbeite mit deren Antwort weiter.

KONTEXT
- Arbeitnehmer: [AN 1], Dienstverhältnis seit: [ZEITPUNKT]
- Regelaltersgrenze erreicht: [ja / nein / unklar], erreicht am: [ZEITPUNKT]
- Nachweis hierzu in der Personalakte: [Rentenbescheid / anderer Nachweis /
  keiner]
- Erklärung zum Verzicht auf die Rentenversicherungsfreiheit nach Erreichen
  der Regelaltersgrenze: [liegt vor / liegt nicht vor / unklar]
  (Rentenart und Rentenhöhe werden nicht angegeben; für die Steuerbefreiung
  sind sie ohne Bedeutung)
- Versicherungsstatus je Zweig: [ANGABEN JE ZWEIG]
- Beschäftigungsart: [sozialversicherungspflichtig / geringfügig entlohnt /
  kurzfristig / Übergangsbereich / unklar]
- Bezüge dem Grunde nach: [laufendes Entgelt / Einmalzahlung / Sachbezug /
  Zuschläge / Dienstwagen / Entgeltumwandlung]
- Weitere Dienstverhältnisse: [nein / ja], Steuerklasse: [ANGABE]
- Erklärung des Arbeitnehmers zur einmaligen Inanspruchnahme:
  [liegt vor / liegt nicht vor], Datum: [DATUM]
- Bisherige Abrechnung: [noch nicht abgerechnet / bereits steuerfrei /
  bereits steuerpflichtig], betroffene Monate: [ANGABE]
- Lohnsteuerbescheinigung bereits übermittelt: [nein / ja], Zeitraum: [ANGABE]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Persönliche Voraussetzung. Ist die Regelaltersgrenze erreicht? Nenne die
   Norm, aus der sich die Regelaltersgrenze ergibt, und weise darauf hin, dass
   sie jahrgangsabhängig ist
   (Norm und Jahrgangsbezug – für [JAHR] verifizieren).
   Nenne kein Lebensalter als Zahl. Ist die Voraussetzung nicht belegt,
   arbeite alle weiteren Schritte unter der ausdrücklich benannten Annahme
   "Regelaltersgrenze erreicht, Nachweis ausstehend" ab und nimm den Nachweis
   als ersten Eintrag in die Nachweisliste auf.
2. Sachliche Voraussetzung. Prüfe die Tatbestandsmerkmale des § 3 Nr. 21 EStG
   einzeln am Sachverhalt und benenne sie ausdrücklich als Merkmale des
   Gesetzestextes: Art des Dienstverhältnisses, Versicherungsstatus,
   begünstigter Arbeitslohn. Grenze ausdrücklich ab, welche Beschäftigungen
   nicht erfasst sind (Fundstelle je Abgrenzung – für [JAHR] verifizieren).
   Wo der Gesetzeswortlaut dir nicht sicher bekannt ist, schreibe
   "Wortlaut offen – am Gesetzestext nachlesen" statt einer Behauptung.
3. Umfang der Begünstigung. Halte fest, welche Lohnbestandteile in Betracht
   kommen und welche nicht, und dass die Befreiung nur bis zu einem Höchstbetrag
   und in monatlicher Betrachtung wirkt (Höchstbetrag und Betrachtungszeitraum –
   für [JAHR] verifizieren). Sage ausdrücklich, ob ein nicht ausgeschöpfter
   Monatsbetrag auf andere Monate übertragbar ist; ist dir das nicht sicher
   bekannt, schreibe "offen – am Gesetzestext und an der Verwaltungsanweisung
   nachlesen". Nenne den Betrag nicht.
4. Der Vergleich, den du nicht ziehst. Formuliere die Frage an die Kanzlei:
   "Übersteigt der begünstigte Arbeitslohn des Monats den Höchstbetrag?"
   Antwortfeld: [nein / ja / unklar]. Leite beide Varianten getrennt ab: Folge
   bei Unterschreiten, Folge für den übersteigenden Teil.
5. Mehrere Dienstverhältnisse. Behandle die Frage, ob und wie die Begünstigung
   bei mehreren Dienstverhältnissen und bei Steuerklasse VI wirkt, und welche
   Erklärung des Arbeitnehmers der Arbeitgeber deshalb zum Lohnkonto nimmt.
   Entwirf diese Erklärung als Textbaustein ohne Betrag.
6. Sozialversicherung getrennt und ausdrücklich. Halte fest: Die
   Sozialversicherungsbeiträge entfallen durch die Steuerbefreiung NICHT. Die
   beitragsrechtliche Behandlung folgt eigenen Regeln; steuerfreier Arbeitslohn
   ist nur beitragsfrei, soweit die Sozialversicherungsentgeltverordnung das
   anordnet (§ 14 SGB IV und die einschlägige Norm der
   Sozialversicherungsentgeltverordnung – für [JAHR] verifizieren). Prüfe
   getrennt davon die Besonderheiten der Beschäftigung nach Erreichen der
   Regelaltersgrenze in Renten- und Arbeitslosenversicherung einschließlich des
   Arbeitgeberanteils (Normen je Zweig – für [JAHR] verifizieren). Nenne keinen
   Beitragssatz.
7. Umsetzung in der Abrechnung. Benenne, was in DATEV Lohn und Gehalt bzw.
   DATEV LODAS zu setzen ist: Personengruppenschlüssel,
   Beitragsgruppenschlüssel, Lohnart für den steuerfreien Bezug, Trennung von
   steuerfreiem und steuerpflichtigem Teil. Ist dir eine Bezeichnung nicht
   sicher bekannt, benenne die Ebene und schreibe "Schlüssel offen – in der
   Programmhilfe nachschlagen". Halte den gesonderten Ausweis in der
   elektronischen Lohnsteuerbescheinigung fest und benenne die Vorschrift, die
   den Ausweis anordnet (Fundstelle – für [JAHR] verifizieren).
8. Fehlerfolgen dem Grunde nach. Stellt sich heraus, dass zu Unrecht steuerfrei
   abgerechnet wurde: Anzeigepflicht des Arbeitgebers gegenüber dem Finanzamt
   (§ 41c Abs. 4 EStG), Grenzen der Änderung des Lohnsteuerabzugs (§ 41c EStG)
   und die Haftung des Arbeitgebers für nicht einbehaltene und abgeführte
   Lohnsteuer nach § 42d Abs. 1 Nr. 1 EStG (jeweils für [JAHR] verifizieren).
   Berechne KEINE Fristen und nenne keine Fristlängen. Liste auf, WELCHE
   Fristen im Raum stehen, je mit Rechtsgrundlage und dem
   Zusatz "für [JAHR] verifizieren", und ergänze bei jeder:
   "Frist von einem Menschen zu berechnen
   und im Fristenprogramm zu erfassen."
9. Unsicherheit ausweisen. Halte ausdrücklich fest, dass die Vorschrift jung
   ist und die Verwaltungsanweisungen zum Zeitpunkt der Bearbeitung dünn sein
   können. Benenne die Auslegungsfragen, die deshalb offen sind, und ordne
   jeder zu, wo eine Klärung zu erwarten ist (BMF-Schreiben,
   Lohnsteuer-Richtlinien, Anrufungsauskunft nach § 42e EStG;
   Fundstelle – für [JAHR] verifizieren).

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Die Unsicherheit über die Anwendbarkeit der Befreiung ist KEIN Abbruchgrund;
sie ist der Regelfall dieser Prüfung. Brich die gesamte Bearbeitung nur ab,
wenn die Angaben ein Straf-, Ermittlungs- oder Bußgeldverfahren, eine
Selbstanzeige oder einen bereits ergangenen Haftungs- oder
Nachforderungsbescheid erwähnen. Gib dann nur aus: "Anzeichen für einen Straf-
oder Haftungssachverhalt – Bearbeitung abgebrochen, Prüfung durch einen
Berufsträger außerhalb des KI-Werkzeugs." Betrifft die Frage einzelne Monate,
für die bereits eine Lohnsteuerbescheinigung übermittelt wurde, steuere nur
diese Monate aus, weise sie als "Anzeigepflicht nach § 41c Abs. 4 EStG durch
einen Berufsträger prüfen" gesondert aus und arbeite die übrigen Monate normal
weiter.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben
   auf. Fehlt der Nachweis zur Regelaltersgrenze, kennzeichne das Ergebnis
   durchgehend als vorläufig und gib zusätzlich aus: "Keine Anwendung der
   Befreiung im Lohnsteuerabzug vor Vorlage des Nachweises."
2. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV mit Norm, Absatz, Satz
   und Nummer, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine
   Paragrafen, keine BMF-Schreiben und keine Aktenzeichen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
3. Trenne in der gesamten Antwort sichtbar zwischen Gesetzeswortlaut,
   Verwaltungsauffassung und eigener Auslegung. Kennzeichne jede Auslegung
   ausdrücklich als Auslegung.
4. Erzeuge eine Nachweisliste als Tabelle: Nachweis | Rechtsgrundlage |
   liegt vor (leer) | Verantwortlich | Ablage im Lohnkonto.
5. Sage in einem eigenen, hervorgehobenen Satz, dass die
   Sozialversicherungsbeiträge nicht entfallen.

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit und fehlende Angaben
2. Prüfprotokoll 1 bis 9 mit Rechtsgrundlagen
3. Ergebnis: [Befreiung kommt in Betracht / kommt nicht in Betracht /
   nicht entscheidbar], bei der letzten Variante die entscheidende Angabe
4. Nachweisliste
5. Erklärung des Arbeitnehmers als Textbaustein
6. Umsetzung in der Abrechnung und Ausweis in der Bescheinigung
7. Fristarten mit Rechtsgrundlage
8. Offene Auslegungsfragen und wo ihre Klärung zu erwarten ist
9. Interne Notiz
10. Was ich nicht sicher weiß
```

## Anwendung

1. Vor der ersten Anwendung den Nachweis zum Erreichen der Regelaltersgrenze und die Erklärung des Arbeitnehmers zum Lohnkonto nehmen und den Eingang datieren.
2. Den Höchstbetrag des Jahres aus dem Gesetzestext übernehmen und in der kanzleieigenen Wertetabelle führen – nicht aus der KI-Antwort.
3. Den Monatsvergleich in der Abrechnungssoftware ziehen, das Ergebnis in den Prompt zurückgeben und beide Varianten aus der Antwort gegeneinander halten.
4. Bei jeder Auslegungsfrage, die wirtschaftlich ins Gewicht fällt, eine Anrufungsauskunft nach § 42e EStG erwägen; die KI-Antwort ersetzt keine verbindliche Auskunft.

## Qualitätssicherung

- **Der Höchstbetrag kommt nie aus der KI-Antwort.** Er steht im Gesetzestext und ändert sich; jede Zahl in der Antwort ist ein Befund.
- **Die Sozialversicherungsbeiträge entfallen nicht.** Wer die Steuerbefreiung auf das beitragspflichtige Arbeitsentgelt durchschlagen lässt, erzeugt eine Beitragsnachforderung in der nächsten Prüfung der Rentenversicherung.
- **Verwaltungsanweisungen sind dünn.** Solange kein BMF-Schreiben vorliegt, ist jede Auslegung als Auslegung zu kennzeichnen und die Entscheidung zu dokumentieren – das ist der Nachweis der sorgfältigen Bearbeitung, wenn die Auffassung später nicht geteilt wird.
- **Zu Unrecht steuerfrei gestellter Arbeitslohn trifft den Arbeitgeber.** Die Haftung nach § 42d Abs. 1 Nr. 1 EStG und die Anzeigepflicht nach § 41c Abs. 4 EStG sind vor der ersten Anwendung mit dem Mandanten zu besprechen und aktenkundig zu machen.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt die Voraussetzungen, die Nachweislage und die getrennte Behandlung von Lohnsteuer und Sozialversicherung nach. Die Freigabe der erstmaligen Anwendung, der Erklärung des Arbeitnehmers und jeder Mandantenmitteilung erteilt ein Berufsträger, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 3 Nr. 21 EStG in der Fassung des Aktivrentengesetzes (BGBl. 2025 I Nr. 361 vom 23.12.2025, in Kraft zum 01.01.2026), § 41c, § 42d Abs. 1 Nr. 1 und § 42e EStG, § 14 SGB IV und der Sozialversicherungsentgeltverordnung sowie den Normen zur Regelaltersgrenze im SGB VI (gesetze-im-internet.de), ergänzend an den Verlautbarungen der Spitzenorganisationen der Sozialversicherung und an DATEV LEXinform.

## Varianten

- **Nur Nachweise:** „Erzeuge ausschließlich die Nachweisliste und die Erklärung des Arbeitnehmers, ohne Prüfprotokoll."
- **Mandanteninformation:** „Erkläre dem Arbeitgeber in höchstens 300 Wörtern, Sie-Form, ohne Betrag und ohne Paragrafen, was die Begünstigung voraussetzt und dass die Sozialversicherungsbeiträge bleiben."
- **Arbeitnehmerinfo:** „Formuliere eine kurze Information für den Arbeitnehmer, die den Unterschied zwischen steuerfrei und beitragsfrei erklärt."
- **Anrufungsauskunft:** „Formuliere den Sachverhaltsteil einer Anrufungsauskunft nach § 42e EStG zu der offenen Auslegungsfrage, ohne Rechtsansicht."
- **Bestandsdurchsicht:** „Erzeuge eine Prüfliste, mit der die Kanzlei ihren Bestand auf Beschäftigte durchsieht, für die die Begünstigung in Betracht kommt."
