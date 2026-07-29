# 77 – Auskunftsersuchen nach Art. 15 DSGVO beantworten

**Problem:** Ein Auskunftsersuchen trifft die Kanzlei an der empfindlichsten Stelle: Sie ist auskunftspflichtig und zugleich zur Verschwiegenheit verpflichtet, die Frist läuft ab Eingang des Antrags (Fristbeginn und Fristlänge – für [JAHR] verifizieren), und wer pauschal alles herausgibt oder pauschal alles verweigert, macht denselben Fehler in zwei Richtungen.
**Rolle:** Zusammenstellung der Datenbestände und Entwurf durch Kanzleiorganisation oder Datenschutzkoordination; die Entscheidung über Umfang und Beschränkung der Auskunft sowie die Freigabe des Schreibens ausnahmslos durch einen Berufsträger.
**DATEV-Bezug:** Kein einzelnes Fachmodul, sondern sämtliche Bestände, in denen Daten der betroffenen Person liegen können: LODAS und Lohn und Gehalt einschließlich Bescheinigungs- und Meldewesen, Kanzlei-Rechnungswesen, DATEV Unternehmen online und Belegtransfer, DATEV Arbeitnehmer online, DATEV DMS und Dokumentenablage, DATEV Eigenorganisation mit Fristen, Notizen und Postbuch, E-Mail-Archiv und Telefonnotizen, DATEV-Cloud-Anwendungen und DATEVasp sowie Sicherungskopien. Die Vollständigkeit der Recherche entscheidet über die Qualität der Auskunft, nicht das Schreiben.
**Was du bereitstellen musst:** Wortlaut oder Zusammenfassung des Ersuchens, Eingangsdatum und Eingangsweg, wer es stellt und in welcher Rolle, Stand der Identitätsprüfung, betroffene Datenbestände und Systeme, Art des Mandats (laufend, beendet, Lohnmandat), getrennt voneinander: ob ein Honorarstreit anhängig ist, ob ein Kündigungs- oder Mandatsbeendigungsstreit anhängig ist und ob gegen die Kanzlei ein Schadensersatz- oder Haftungsanspruch angekündigt oder beziffert geltend gemacht ist, ob zugleich Unterlagen herausverlangt werden, ob Daten Dritter in den betroffenen Beständen liegen.
**Datensparsamkeit:** Den Inhalt der Datenbestände nicht einfügen – für die Bearbeitung genügt, WELCHE Bestände es gibt, nicht was darin steht. Antragsteller nur als Rolle (`Antragsteller`, `ehemaliger Mandant`, `Beschäftigter des Lohnmandanten`), Mandant als `Mandant A`. Keine Lohnwerte, keine Personalnummern, keine Ausweisdaten aus der Identitätsprüfung. Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). **Vorschaltfrage vor dem Ausfüllen, außerhalb des Werkzeugs vom Berufsträger zu beantworten und in der Handakte zu vermerken:** Steht das Ersuchen im Zusammenhang mit einem Straf-, Steuerstraf- oder Ermittlungsverfahren, wird dieser Prompt **nicht** verwendet und der Sachverhalt **nicht** eingegeben (Zone Rot in `DATENSCHUTZ.md`); der Vorgang geht unmittelbar an den Berufsträger. Die Angabe wird auch nicht als „ja/nein" in den Sachverhaltsbogen aufgenommen. Der Einsatz setzt die berufsrechtliche Einbindung des Anbieters nach § 62a StBerG voraus (sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) – siehe `DATENSCHUTZ.md`, Abschnitte 4 und 7.

## Prompt

```text
Du bist Datenschutzkoordinator einer deutschen Steuerkanzlei. Du arbeitest
bestandsweise: erst wer fragt, dann welche Bestände es gibt, dann was aus jedem
Bestand herausgehen darf. Du gibst nichts frei und du verweigerst nichts pauschal.

ABGRENZUNG – GILT FÜR DIE GANZE ANTWORT
1. Du entscheidest nicht über die Auskunft. Du bereitest die Entscheidung vor
   und legst sie einem Berufsträger vor. Die Abwägung zwischen Auskunftsanspruch
   und Verschwiegenheit trifft ein Mensch.
2. Du BERECHNEST KEINE FRIST. Nenne kein Datum, keine Dauer und keinen
   Wochentag. Benenne nur, welches Ereignis den Fristlauf auslöst, dass ein
   Fristende zu bestimmen ist und wer es im Fristenprogramm erfasst.
3. Trenne den Auskunftsanspruch von der Herausgabe von Unterlagen. Die Frage,
   welche Unterlagen der Mandant nach Beendigung des Auftrags herausverlangen
   kann, richtet sich nach den Vorschriften über die Handakte (§ 66 StBerG –
   für [JAHR] verifizieren) und nicht nach Art. 15 DSGVO. Vermenge beides nicht
   und erzeuge keine Aussage zu einem Zurückbehaltungsrecht.
4. Unterstelle dem Antragsteller kein Motiv. Dass ein Ersuchen in einem Honorar-
   oder Kündigungsstreit als Druckmittel eingesetzt werden kann, ändert nichts
   an der Pflicht, es ordnungsgemäß zu bearbeiten. Vermerke den Zusammenhang
   ausschließlich in der internen Notiz und nie im Schreiben an den
   Antragsteller.
5. Du beschreibst ausschließlich die Rechtsposition und die Verarbeitung der
   Kanzlei. Du bewertest nicht die datenschutzrechtlichen Pflichten des
   Mandanten, seines Arbeitgebers oder eines Dritten und gibst ihnen keine
   Handlungsempfehlung – das wäre Rechtsberatung außerhalb der Befugnis nach
   § 33 StBerG und nur als Nebenleistung nach § 5 Abs. 1 RDG denkbar
   (§ 33 StBerG, § 5 Abs. 1 RDG – für [JAHR] verifizieren). Verlangt das
   Ersuchen eine solche Bewertung, gib nur aus: "Frage betrifft die Rechtslage
   des Anfragenden – Vorlage an den Berufsträger, kein Schreiben erzeugt."

VERBINDLICHE RECHTSGRUNDLAGEN – GENAU SO VERWENDEN
a) Frist: Art. 12 Abs. 3 DSGVO regelt die Grundfrist ab Eingang des Antrags,
   die Möglichkeit der Verlängerung und die Pflicht, den Antragsteller über die
   Verlängerung samt Gründen noch innerhalb der Grundfrist zu unterrichten
   (Art. 12 Abs. 3 DSGVO – für [JAHR] verifizieren). Nenne die Dauer nicht als
   Zahl; sie wird am Normtext abgelesen.
b) Art. 15 Abs. 4 DSGVO beschränkt nach seinem Wortlaut nur das Recht auf
   Erhalt einer KOPIE nach Art. 15 Abs. 3 DSGVO, nicht das Auskunftsrecht
   insgesamt. Formuliere das genau so und leite daraus keine allgemeine
   Verweigerung ab (Art. 15 Abs. 3 und 4 DSGVO – für [JAHR] verifizieren).
c) Die für Berufsgeheimnisträger einschlägige Schranke ist
   § 29 Abs. 1 Satz 2 BDSG: Das Auskunftsrecht besteht nicht, soweit durch die
   Auskunft Informationen offenbart würden, die nach einer Rechtsvorschrift oder
   ihrem Wesen nach geheim gehalten werden müssen; flankierend gilt § 34 BDSG
   (§ 29 Abs. 1 Satz 2 BDSG, § 34 BDSG – für [JAHR] verifizieren). Prüfe die
   Schranke bestandsweise, nicht pauschal.
   Gegenüber dem Mandanten als Träger des eigenen Geheimnisses trägt die
   berufliche Verschwiegenheit keine Beschränkung. § 29 Abs. 1 Satz 2 BDSG
   greift nur, soweit durch die Auskunft Informationen offenbart würden, die
   Dritte betreffen – andere Mandate, andere Beschäftigte, Angaben Dritter in
   der Akte. Prüfe je Bestand ausdrücklich, wessen Geheimnis betroffen ist, und
   stütze eine Beschränkung nie darauf, dass die Daten des Antragstellers selbst
   dem Berufsgeheimnis unterliegen
   (§ 29 Abs. 1 Satz 2 BDSG – für [JAHR] verifizieren).
d) § 32c AO gilt nur gegenüber Finanzbehörden und ist gegenüber dem
   Steuerberater NICHT einschlägig. Nenne die Norm ausschließlich zur
   Abgrenzung und stütze keine Verweigerung darauf
   (§ 32c AO – für [JAHR] verifizieren).
e) Höchstrichterliche Rechtsprechung speziell zum Auskunftsanspruch gegenüber
   Steuerberatern ist nicht bekannt. Behaupte keine. Willst du auf
   EuGH 26.10.2023 – C-307/22 oder BGH 15.06.2021 – VI ZR 576/19 verweisen,
   kennzeichne beide ausdrücklich als nicht zu Steuerberatern ergangen –
   die eine betrifft einen Arzt, die andere einen Versicherer – und als
   allenfalls analogiefähig (für [JAHR] verifizieren). Zitiere keinen Leitsatz
   wörtlich.

AUFGABE
Erzeuge fünf Ergebnisse: (a) die Zuordnung des Antragstellers, (b) eine
bestandsweise Prüftabelle, (c) einen Entwurf des Antwortschreibens, (d) einen
Vorschlag, was nach dem Entwurf nicht herausgehen soll, mit Begründung, zur
Entscheidung durch den Berufsträger, (e) eine interne Notiz.

SACHVERHALT
- Antragsteller: [laufender Mandant / ehemaliger Mandant /
  Beschäftigter eines Lohnmandanten / Gesellschafter oder Organ eines Mandanten /
  Dritter / unklar]
- Eingang am: [ZEITPUNKT], Eingangsweg: [Brief / E-Mail / Telefon /
  über Rechtsanwalt / Portal]
- Wortlaut oder Kern des Ersuchens: [ANGABE]
- Umfang des Verlangens: [Auskunft / Kopie / beides / unklar]
- Identität geprüft: [ja / nein / Zweifel bestehen]
- Mandat: [laufend / beendet / nie bestanden]
  wenn beendet, beendet am: [ZEITPUNKT]
- Bei Lohnmandat – Arbeitgeber ist: [MANDANT A], Kanzlei führt:
  [Abrechnung / Meldewesen / Bescheinigungen / mehreres]
- Betroffene Bestände: [ANGABEN, nur Bezeichnung der Systeme und Ablagen]
- Daten Dritter in den Beständen: [nein / ja / unklar]
  wenn ja, nämlich: [ANGABE]
- Zugleich Herausgabe von Unterlagen verlangt: [nein / ja]
- Honorarstreit anhängig: [nein / ja / unbekannt]
- Kündigungs- oder Mandatsbeendigungsstreit anhängig: [nein / ja / unbekannt]
- Gegen die Kanzlei geltend gemachter Schadensersatz- oder Haftungsanspruch:
  [nein / angekündigt / beziffert geltend gemacht / unbekannt]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Identität und Rolle. Ohne gesicherte Identität keine Auskunft; benenne, was
   zur Feststellung fehlt, und dass eine Nachforderung von Nachweisen die
   Bearbeitung nicht beliebig aufschiebt. Bestehen begründete Zweifel an der
   Identität, können zusätzliche Informationen zur Bestätigung angefordert
   werden; bloße Bequemlichkeit trägt die Nachforderung nicht
   (Art. 12 Abs. 6 DSGVO – für [JAHR] verifizieren). Ordne den Antragsteller einer der
   Rollen zu und halte fest, welche Daten in dieser Rolle überhaupt bei der
   Kanzlei anfallen.
2. Sonderfall Beschäftigter eines Lohnmandanten. Die Kanzlei verarbeitet die
   Daten nicht im Auftrag des Mandanten, sondern weisungsfrei als
   Verantwortliche (§ 11 Abs. 2 StBerG – für [JAHR] verifizieren; Einordnung
   siehe Prompt 76). Halte fest, dass daneben eine eigene Auskunftspflicht des
   Arbeitgebers besteht und dass die Abgrenzung beider Ansprüche sowie die Frage,
   in welchem Umfang die Kanzlei gegenüber Beschäftigten ihres Mandanten
   auskunftspflichtig ist, vom Berufsträger zu klären ist
   ("Fundstelle offen – bitte recherchieren"). Entscheide sie nicht selbst und
   verweise den Antragsteller nicht einfach an den Arbeitgeber weiter.
3. Bestandsaufnahme. Liste jeden Bestand einzeln auf, in dem Daten der
   betroffenen Person liegen können, einschließlich E-Mail, Notizen, Postbuch,
   Fristenverwaltung und Sicherungskopien. Ergänze je Bestand, wer ihn
   durchsucht. Erfinde keinen Bestand und unterstelle keinen, der nicht genannt
   wurde; benenne stattdessen die Bestände, nach denen zu fragen ist.
4. Bestandsweise Prüfung. Ordne je Bestand zu:
   (Auskunft möglich), (Auskunft beschränkt) oder (nicht entscheidbar).
   Begründe jede Beschränkung einzeln mit der Rechtsgrundlage aus Buchstabe c
   und benenne, welche Information konkret geheim zu halten ist. Eine
   Beschränkung ohne benannten Grund ist unzulässig. Halte getrennt fest, ob
   sich eine Beschränkung nur auf die Kopie oder auf die Auskunft selbst
   bezieht (Buchstabe b).
5. Rechte Dritter. Prüfe gesondert, ob Daten anderer Mandanten, anderer
   Beschäftigter oder sonstiger Dritter betroffen sind, und benenne, welche
   Teile deshalb zu schwärzen oder herauszunehmen sind. Eine vollständige
   Verweigerung wegen Drittdaten ist zu begründen, nicht zu behaupten.
6. Pflichtinhalte der Auskunft. Gehe die in Art. 15 Abs. 1 und 2 DSGVO
   genannten Angaben durch und ordne jeder zu, ob sie die Kanzlei liefern kann
   und aus welcher Quelle (Art. 15 Abs. 1 und 2 DSGVO – für [JAHR] verifizieren).
   Erfinde keine Angabe; was nicht bekannt ist, wird als offen ausgewiesen.
7. Fristbehandlung. Benenne den Fristbeginn dem Grunde nach (Eingang des
   Antrags), das Erfordernis eines bestimmten Fristendes, die Möglichkeit der
   Verlängerung und die Pflicht zur Unterrichtung innerhalb der Grundfrist, je
   mit Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   ohne Dauer. Ergänze wörtlich: "Frist von einem Menschen zu berechnen und im
   Fristenprogramm zu erfassen." Benenne die Rolle, die das tut.
8. Antwortschreiben. Sie-Form, höchstens 350 Wörter, sachlich, ohne Vorwurf und
   ohne Rechtfertigung. Es bestätigt den Eingang, benennt den Umfang der
   Auskunft, weist Beschränkungen aus und begründet sie in einem Satz je
   Beschränkung, weist auf das Beschwerderecht bei der Aufsichtsbehörde hin
   (Art. 77 DSGVO – für [JAHR] verifizieren), enthält ein Datum als Leerfeld und
   einen Ansprechpartner als Leerfeld. Es enthält KEINE Aussage zum Honorar, zur
   Mandatsbeendigung, zur Handakte und keine Bewertung des Ersuchens. Wird
   zugleich Herausgabe verlangt, nimm dazu nur den Satz auf, dass dieser Punkt
   gesondert beantwortet wird.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar, und liste fehlende
   Angaben auf.
2. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
   Absatz und Satz und dem Zusatz "für [JAHR] verifizieren". Erfinde keine
   Fundstelle und kein Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Verweigere nichts pauschal und gib nichts pauschal frei. Beides ist ein
   Fehler; die Prüfung erfolgt bestandsweise.
4. Nenne keine Bußgeldhöhe, keinen Schadensersatzbetrag und keine Zahl als
   Frist.
5. Formuliere jede Annahme über den Antragsteller als Vermutung und kennzeichne
   sie als solche.

ABBRUCHREGEL – an den Feldern des Sachverhaltsbogens, nicht an einer Beurteilung
Ein anhängiger Honorar- oder Kündigungsstreit, ein angekündigter
Haftungsanspruch, ein anwaltlich formuliertes Ersuchen, ein knapp gesetzter
Termin oder ein ehemaliger Mandant sind KEIN Abbruchgrund – das ist der
Normalfall dieses Prompts. Brich nur ab, wenn (a) die Angaben gleichwohl ein
Straf- oder Ermittlungsverfahren erkennen lassen, (b) die Angaben einen bereits
eingetretenen Datenschutzvorfall in den betroffenen Beständen erwähnen,
(c) im Feld "Gegen die Kanzlei geltend gemachter Schadensersatz- oder
Haftungsanspruch" der Wert "beziffert geltend gemacht" steht oder (d) die
Angaben ein laufendes Verfahren einer Aufsichtsbehörde erwähnen. Gib dann nur
aus: "Abbruchgrund liegt vor (Buchstabe angeben) – Bearbeitung an dieser Stelle
abgebrochen, Prüfung durch einen Berufsträger außerhalb des KI-Werkzeugs."

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit und fehlende Angaben"
2. "Zuordnung des Antragstellers" mit Ergebnis der Identitätsprüfung
3. "Bestandsweise Prüfung": Nr. | Bestand | System oder Ablage | Einordnung |
   Grund der Beschränkung | Rechtsgrundlage mit Zusatz | wer durchsucht |
   erledigt (leer)
4. "Pflichtinhalte nach Art. 15 DSGVO": Angabe | lieferbar | Quelle | offen
5. "Rechte Dritter und Schwärzungen"
6. "Fristarten und Fristbeginn" – ohne Datum und ohne Dauer
7. "Antwortschreiben (Entwurf)"
8. "Vorschlag: Was nach dem Entwurf nicht herausgehen soll – Entscheidung durch
   den Berufsträger" – je Position mit Begründung und Rechtsgrundlage
9. "Interne Notiz": Abgrenzung zur Handakte, möglicher Zusammenhang mit einem
   Streit, offene Punkte, Vorlage an den Berufsträger
10. "Was ich nicht sicher weiß"
```

## Anwendung

1. Eingang sofort mit Datum und Eingangsweg festhalten und die Frist im Fristenprogramm erfassen, bevor die inhaltliche Arbeit beginnt. Die häufigste Ursache für einen Fehler ist nicht die falsche Antwort, sondern die vergessene Frist.
2. Identität prüfen, bevor recherchiert wird. Bei Zweifeln Nachweise anfordern und die Anforderung dokumentieren; die Bearbeitung ruht dadurch nicht unbegrenzt.
3. Die Bestandsliste einmal als Kanzleistandard erstellen – alle Systeme, Ablagen, Postfächer und Sicherungen mit zuständiger Rolle. Ohne diese Liste ist jede Auskunft unvollständig, und die Vollständigkeit ist der eigentliche Aufwand.
4. Beschränkungen einzeln begründen und die Begründung zur Akte nehmen. Eine pauschale Berufung auf die Verschwiegenheit trägt nicht; ebenso wenig trägt Art. 15 Abs. 4 DSGVO eine Verweigerung der Auskunft insgesamt.
5. Wird zugleich die Handakte verlangt, den Punkt gesondert und in einem eigenen Schreiben beantworten (§ 66 StBerG – für [JAHR] verifizieren); für das zweite Schreiben Prompt 69 verwenden. Zwei Ansprüche, zwei Antworten.
6. Auskunft, Anlagen und Versandnachweis im DMS ablegen. Die Dokumentation der erteilten Auskunft ist im Streitfall der einzige Beleg dafür, was herausgegeben wurde.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Prüftabelle und Schreiben sind Entwürfe. Eine zweite Person geht die Bestandsliste auf Vollständigkeit durch und prüft jede Beschränkung gegen ihre Begründung. **Die Entscheidung über Umfang und Beschränkung sowie die Freigabe des Schreibens erteilt ausnahmslos ein Berufsträger**, dokumentiert mit Datum (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum und keine Dauer aus der KI-Antwort übernehmen; die Verlängerung setzt eine Unterrichtung innerhalb der Grundfrist voraus und ist ihrerseits fristgebunden (Art. 12 Abs. 3 DSGVO – für [JAHR] verifizieren).
- **Art. 15 Abs. 4 DSGVO nicht überdehnen.** Eine Antwort, die daraus eine Beschränkung des Auskunftsrechts insgesamt ableitet, ist zu verwerfen; der Wortlaut betrifft das Recht auf Erhalt einer Kopie.
- **§ 32c AO nicht als Schranke verwenden.** Die Norm gilt gegenüber Finanzbehörden. Steht sie in der Antwort als Verweigerungsgrund, ist die Stelle zu streichen.
- **Verschwiegenheit ist keine Schranke gegenüber dem Geheimnisherrn.** Eine Beschränkung, die damit begründet wird, dass die Daten des Antragstellers selbst dem Berufsgeheimnis unterliegen, ist zu streichen. § 29 Abs. 1 Satz 2 BDSG greift nur, soweit Informationen offenbart würden, die Dritte betreffen.
- **Keine Bewertung fremder Rechtslage.** Die Antwort beschreibt die Verarbeitung der Kanzlei. Bewertet sie die datenschutzrechtlichen Pflichten des Arbeitgebers oder eines Dritten, ist die Stelle zu streichen (§ 33 StBerG, § 5 Abs. 1 RDG).
- **Keine erfundene Rechtsprechung.** Zu Steuerberatern ist keine höchstrichterliche Entscheidung bekannt; die Entscheidungen zum Arzt und zum Versicherer sind allenfalls analogiefähig und als solche zu kennzeichnen. Wörtliche Zitate löschen.
- **Auskunft und Handakte getrennt halten.** Vermischt das Schreiben beide Ansprüche, entsteht ein Anerkenntnis oder eine Ablehnung, die niemand gewollt hat.
- **Kein Wort zum Streit im Schreiben.** Hinweise auf Honorar, Kündigung oder Motive gehören ausschließlich in die interne Notiz.
- **Rechtsstand prüfen an:** Art. 12 Abs. 3, 5 und 6, Art. 15 und Art. 77 DSGVO, § 29 Abs. 1 Satz 2 BDSG und § 34 BDSG, § 11 Abs. 2 StBerG, § 33 StBerG, § 57 Abs. 1 StBerG und § 66 StBerG, § 5 Abs. 1 RDG sowie § 203 Abs. 1 Nr. 3 StGB im amtlichen Volltext (gesetze-im-internet.de); zur Abgrenzung § 32c AO; ergänzend die Hinweise der Bundessteuerberaterkammer zum Datenschutz, die Orientierungshilfen der Datenschutzkonferenz und DATEV LEXinform.

## Varianten

- **Nur Bestandsliste:** „Erzeuge ausschließlich die kanzleiweite Bestandsliste als Vorlage, ohne Bezug zu einem Ersuchen, mit Spalten für System, Ablage, zuständige Rolle und Suchweg."
- **Verlängerung:** „Erzeuge ausschließlich die Unterrichtung über die Verlängerung mit Begründung, ohne Datum, und benenne, wer das Datum einsetzt."
- **Zweites Ersuchen:** „Der Antragsteller wiederholt sein Ersuchen kurz nach der Beantwortung. Prüfe, welche Angaben zur Wiederholung fehlen, und entwirf eine Antwort ohne Bewertung des Verhaltens. Prüfe dabei die Voraussetzungen des Art. 12 Abs. 5 DSGVO und weise darauf hin, dass die Kanzlei den offenkundig unbegründeten oder exzessiven Charakter nachzuweisen hat; entscheide nicht selbst (Art. 12 Abs. 5 DSGVO – für [JAHR] verifizieren)."
- **Ehemaliger Mandant mit Herausgabeverlangen:** „Trenne die beiden Ansprüche in zwei Schreiben und nimm in das erste keine Aussage zur Handakte auf."
- **Lohnmandat:** „Beschränke die Prüfung auf die Bestände der Lohnabrechnung und benenne, welche Angaben der Arbeitgeber selbst zu beauskunften hat."
- **Löschungsverlangen:** „Der Antragsteller verlangt zugleich Löschung. Benenne nur, welche Aufbewahrungspflichten dem entgegenstehen können, je mit Rechtsgrundlage und dem Zusatz, ohne zu entscheiden."
- **AVV-Anfrage:** Prompt 76. **Dienstleisterprüfung:** Prompt 103. **Herausgabe der Handakte:** Prompt 69.
