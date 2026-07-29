# 72 – Grundsteuerwert: niedrigeren gemeinen Wert prüfen

**Problem:** Mandanten halten ihren Grundsteuerwert für zu hoch und erwarten von der Kanzlei eine schnelle Antwort; unklar ist aber, ob der Nachweis eines niedrigeren gemeinen Werts überhaupt in Betracht kommt, ab welcher Abweichung er zulässig ist, was als Nachweis genügt, was er kostet und ob ein bereits eingelegter Einspruch nach den Entscheidungen des Bundesfinanzhofs vom 12.11.2025 noch trägt (Rechtsstand – für [JAHR] verifizieren).
**Rolle:** Berufsträger, Sachbearbeiter Steuern; die Entscheidung über Einspruch, Rücknahme und Gutachtenauftrag trifft der Berufsträger gemeinsam mit dem Mandanten
**DATEV-Bezug:** Für die Grundsteuer gibt es kein bestätigtes DATEV-Eigenprodukt; belegbar ist die Marktplatz-Lösung GrundsteuerDigital (Produktstand – für [JAHR] verifizieren). Daneben DATEV DMS (Grundsteuerwertbescheid, Feststellungserklärung, Kaufvertrag, vorhandene Gutachten), DATEV Eigenorganisation (Rechtsbehelfsfristen, Wiedervorlage), DATEV Kanzlei-Rechnungswesen nur, soweit das Grundstück zum Betriebsvermögen gehört.
**Was du bereitstellen musst:** Bundesland der Belegenheit und angewandtes Grundsteuermodell; Grundsteuerwertbescheid mit Feststellungszeitpunkt, festgestelltem Wert, Bescheiddatum und Angabe, ob er unter Vorbehalt der Nachprüfung oder vorläufig ergangen ist; Verfahrensstand (Einspruch eingelegt, Ruhen, Aussetzung der Vollziehung, Bestandskraft); Art und Zustand des Grundstücks mit den Merkmalen, die für einen niedrigeren Wert sprechen (Baujahr, Bauzustand, Denkmalschutz, Belastungen, Baumängel, Erbbaurecht, Immissionen, eingeschränkte Bebaubarkeit, Leerstand); vorhandene Wertangaben (Kaufpreis mit Datum, Verkehrswertgutachten, Beleihungswert, Erbschaft- oder Schenkungsteuerwert); den Grundsteuermessbetrag nur, soweit er für die Größenordnung der jährlichen Auswirkung gebraucht wird – den Hebesatz der Gemeinde nicht, weil er die Gemeinde benennt.
**Datensparsamkeit:** Grundstücke ausschließlich als `Objekt 1`; Beteiligte nur nach Rolle (`Eigentümer 1`, `Erwerber 1`, `Erbbauberechtigter 1`). Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts sowie Grundbuchblatt, Flur- und Flurstücksangaben mit Ortsbezug nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Von der Lage wird nur das Bundesland übernommen; Straße, Hausnummer, Gemeinde, Bodenrichtwertzone und Kartenausschnitte bleiben draußen, weil sie das Objekt identifizieren. Kaufvertragsdaten nur als Betrag und Datum, ohne Vertragsparteien und ohne Urkundennummer. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`, Abschnitte 4 und 7. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und klärst, ob der
Nachweis eines niedrigeren gemeinen Werts gegen einen Grundsteuerwertbescheid in
Betracht kommt und ob sich der Aufwand lohnt. Du arbeitest streng nach
Prüfschema und behauptest keine Rechtslage, die du nicht am Gesetzestext belegen
kannst.

WAS DU NICHT TUST – GILT FÜR DIE GANZE ANTWORT
Du bewertest KEIN Grundstück. Du ermittelst KEINEN gemeinen Wert, KEINEN
Verkehrswert, KEINEN Bodenrichtwert und KEINE Wertminderung. Du rechnest NICHTS
aus – weder die Abweichung zwischen Grundsteuerwert und behauptetem gemeinen
Wert noch die jährliche Grundsteuerwirkung noch die Amortisation eines
Gutachtens. Du berechnest KEINE Frist und KEIN Datum. Du prüfst, ob ein Nachweis
überhaupt in Betracht kommt, welche Anforderungen er erfüllen muss, was er
kosten würde und wie mit einem bereits eingelegten Einspruch umzugehen ist.
Alle Rechengrößen bleiben Leerfelder, die die Kanzlei ausfüllt.

AUFGABE
Erzeuge vier Ergebnisse: (a) die Prüfung, ob der Nachweis dem Grunde nach in
Betracht kommt, (b) den Anforderungskatalog an den Nachweis, (c) eine
Entscheidungstabelle für den Kosten-Nutzen-Vergleich mit Leerfeldern,
(d) eine Empfehlung zum weiteren Vorgehen im Rechtsbehelfsverfahren als
Entscheidungsvorlage.

SACHVERHALT
- Bezeichnung: [OBJEKT 1]
- Bundesland der Belegenheit: [BUNDESLAND]
- Angewandtes Grundsteuermodell: [Bundesmodell / Bundesmodell mit abweichender
  Steuermesszahl / eigenes Landesbewertungsmodell / unbekannt]
- Art der wirtschaftlichen Einheit: [unbebautes Grundstück / Wohngrundstück /
  Nichtwohngrundstück / Betrieb der Land- und Forstwirtschaft]
- Angewandtes Bewertungsverfahren nach dem Bescheid:
  [Ertragswertverfahren / Sachwertverfahren / unbekannt]
- Feststellungszeitpunkt: [DATUM], festgestellter Grundsteuerwert: [BETRAG]
- Bescheiddatum: [DATUM], Bekanntgabe: [DATUM]
- Nebenbestimmungen: [ohne / unter Vorbehalt der Nachprüfung / vorläufig],
  Umfang: [ANGABE]
- Einspruch eingelegt: [nein / ja], Datum: [DATUM]
- Verfahrensstand: [kein Rechtsbehelf / Einspruch anhängig / Ruhen des
  Verfahrens / Aussetzung der Vollziehung gewährt / bestandskräftig / unbekannt]
- Wertangaben, die vorliegen: [Kaufpreis mit Datum / Verkehrswertgutachten mit
  Datum und Wertermittlungsstichtag / Beleihungswert / keine]
- Wertmindernde Merkmale: [Baujahr, Bauzustand, Sanierungsstau, Denkmalschutz,
  Baulasten, Wegerechte, Erbbaurecht, Immissionen, eingeschränkte Bebaubarkeit,
  Leerstand, Kontamination, sonstige]
- Grundsteuermessbetrag: [BETRAG]; der Hebesatz wird nicht übernommen – er
  benennt die Gemeinde. Die jährliche Auswirkung ermittelt die Kanzlei außerhalb
  des Werkzeugs und trägt sie in die Kosten-Nutzen-Tabelle ein.
- Erwartung des Mandanten: [ANGABE]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Modellfrage zuerst – sie trägt alle weiteren Schritte. Die Nachweismöglichkeit
   des Bewertungsgesetzes gilt im Bundesmodell. Fünf Länder wenden ein eigenes
   Bewertungsmodell an; zwei weitere wenden das Bundesmodell mit abweichenden
   Steuermesszahlen an – dort gilt die Nachweismöglichkeit des
   Bewertungsgesetzes uneingeschränkt, eine abweichende Steuermesszahl ist KEIN
   Grund, die Prüfung zu beenden. Nur bei einem eigenen Landesbewertungsmodell
   arbeitest du die folgenden Schritte NICHT ab, sondern gibst aus:
   "Landesbewertungsmodell – ob und unter welchen Voraussetzungen ein niedrigerer
   Wert nachgewiesen werden kann, richtet sich nach dem Landesgrundsteuergesetz
   und ist dort nachzuschlagen", benennst die zu prüfenden Punkte und beendest
   die Prüfung. Bei "unbekannt" kläre das Modell als ersten Punkt der
   Rückfrageliste (Modellzuordnung je Land – für [JAHR] verifizieren).
2. Verfahrensstand – der zweite tragende Schritt. Ohne ihn ist keine Aussage
   möglich, auf welchem Weg ein niedrigerer Wert überhaupt noch berücksichtigt
   werden kann. Ordne zu:
   a) Rechtsbehelfsfrist läuft noch,
   b) Einspruch anhängig,
   c) Bescheid bestandskräftig, aber unter Vorbehalt der Nachprüfung oder
      vorläufig,
   d) Bescheid bestandskräftig und ohne Nebenbestimmung.
   Sage je Fall, welcher Verfahrensweg dem Grunde nach in Betracht kommt –
   Einspruch, Änderungsantrag, Fortschreibung auf einen späteren
   Feststellungszeitpunkt – und benenne je Weg die Norm
   (Verfahrensweg und Fundstelle – für [JAHR] verifizieren). Nenne KEINE Frist
   als Zahl und kein Datum; ergänze: "Frist von einem Menschen zu berechnen und
   im Fristenprogramm zu erfassen."
3. Anwendbarkeit der Nachweismöglichkeit in zeitlicher Hinsicht. Die Vorschrift
   über den Nachweis des niedrigeren gemeinen Werts wurde durch das
   Jahressteuergesetz 2024 eingefügt und ist am 06.12.2024 in Kraft getreten
   (§ 220 Abs. 2 BewG – für [JAHR] verifizieren). Prüfe ausdrücklich, ab welchem
   Feststellungszeitpunkt sie im vorliegenden Fall anzuwenden ist, und benenne
   die Anwendungsvorschrift als die Stelle, aus der sich das ergibt
   (Anwendungsregelung – für [JAHR] verifizieren). Behaupte den
   Anwendungszeitpunkt nicht.
4. Schwelle dem Grunde nach. Der Nachweis kommt nur in Betracht, wenn der
   festgestellte Grundsteuerwert den nachgewiesenen gemeinen Wert um mindestens
   40 Prozent übersteigt (Schwelle – für [JAHR] verifizieren). Rechne die
   Abweichung NICHT aus. Stelle stattdessen dar, welche beiden Größen die
   Kanzlei gegenüberzustellen hat, und gib die Gegenüberstellung als Tabelle mit
   Leerfeldern aus. Sage ausdrücklich, dass die Schwelle eine Zugangsvoraussetzung
   ist und dass eine geringere Abweichung den Nachweis ausschließt.
5. Anhaltspunkte, die für eine erhebliche Abweichung sprechen können. Ordne die
   gelieferten wertmindernden Merkmale danach, ob sie im typisierten
   Bewertungsverfahren bereits berücksichtigt sind oder gerade nicht erfasst
   werden. Kennzeichne jede Aussage ausdrücklich als Vermutung, solange sie nicht
   aus den Angaben folgt, und leite daraus KEINEN Wert ab.
6. Zulässige Nachweismittel. § 220 Abs. 2 Satz 3 BewG erklärt ausschließlich
   § 198 Abs. 1 Satz 2 und Abs. 2 BewG für entsprechend anwendbar;
   § 198 Abs. 3 BewG (Kaufpreis) ist NICHT in Bezug genommen
   (Reichweite der Verweisung – für [JAHR] verifizieren).
   Benenne danach getrennt:
   a) Gutachten des zuständigen Gutachterausschusses,
   b) Gutachten einer Person oder Stelle, die für die Wertermittlung von
      Grundstücken zertifiziert oder öffentlich bestellt und vereidigt ist –
      benenne die Anforderungen an die Qualifikation als eigenen Punkt.
   Ein im gewöhnlichen Geschäftsverkehr zustande gekommener Kaufpreis ist nach
   dem Wortlaut der Verweisung KEIN eigenständiges Nachweismittel; behandle ihn
   nur als Anhaltspunkt und als Unterlage für den Sachverständigen und weise
   ausdrücklich darauf hin, dass seine Anerkennung offen ist
   (Fundstelle offen – bitte recherchieren).
   Sage je Nachweismittel, welche Voraussetzung im Sachverhalt belegt ist und
   welche fehlt.
7. Anforderungen an ein Gutachten. Liste auf, was das Gutachten leisten muss,
   damit es als Nachweis taugt: Wertermittlungsstichtag gleich
   Feststellungszeitpunkt, Bezug auf die richtige wirtschaftliche Einheit,
   Anwendung eines anerkannten Wertermittlungsverfahrens nach der
   Immobilienwertermittlungsverordnung, nachvollziehbare Ableitung der
   Eingangsgrößen, Begründung jeder Abweichung von den typisierten Ansätzen,
   Objektbesichtigung, Qualifikationsnachweis des Sachverständigen
   (Anforderungen im Einzelnen – für [JAHR] verifizieren). Ergänze eine Liste
   der Unterlagen, die dem Sachverständigen zu übergeben sind.
8. Kosten und Nutzen – als Tabelle mit Leerfeldern, ohne eigene Rechnung.
   Spalten: Position | Betrag (leer) | Quelle der Angabe | Bemerkung.
   Zeilen mindestens: Gutachtenkosten, eigener Zeitaufwand der Kanzlei mit
   Honorarhinweis, Kosten des Rechtsbehelfsverfahrens, jährliche
   Grundsteuerwirkung einer Wertminderung, Zahl der Jahre bis zur nächsten
   Hauptfeststellung, Risiko eines für den Mandanten ungünstigen Gutachtens.
   Ergänze den ausdrücklichen Hinweis, dass ein Gutachten auch einen höheren
   Wert ausweisen kann und dass die Kosten dann ohne Nutzen angefallen sind.
9. Umgang mit einem anhängigen Einspruch. Der Bundesfinanzhof hat mit Urteilen
   vom 12.11.2025 – II R 25/24, II R 31/24 und II R 3/25 entschieden, dass das
   Bundesmodell verfassungskonform ist und keine Vorlage an das
   Bundesverfassungsgericht erfolgt
   (Entscheidungen und Reichweite – für [JAHR] verifizieren).
   Ob gegen diese Entscheidungen Verfassungsbeschwerden anhängig
   sind, ist nicht belegt; führe diesen Punkt ausdrücklich als offen und
   behaupte weder, dass Verfahren anhängig sind, noch, dass keine anhängig sind.
   Stelle daraus zwei Wege gegenüber, ohne zu entscheiden:
   a) Einspruch zurücknehmen, wenn er allein auf die Verfassungsfrage gestützt
      war – benenne die Folgen der Rücknahme und die Norm,
   b) Einspruch weiterverfolgen, wenn er auf einen niedrigeren gemeinen Wert
      oder auf einen individuellen Bewertungsfehler gestützt ist oder werden
      kann – benenne, was dafür nachzureichen ist, und die Regelung über das
      Ruhen des Verfahrens
      (Verfahrensvorschriften – für [JAHR] verifizieren).
   Schließe mit dem Satz: "Über Rücknahme oder Fortführung entscheidet der
   Berufsträger gemeinsam mit dem Mandanten."
10. Individuelle Bewertungsfehler. Prüfe getrennt von der Wertfrage, ob der
    Bescheid auf unrichtigen Sachangaben beruht (Fläche, Baujahr, Art der
    Nutzung, Zurechnung, Bewertungsverfahren). Ein solcher Fehler wird nicht
    über ein Gutachten, sondern über die Berichtigung der Angaben geltend
    gemacht; sage das ausdrücklich und benenne den Weg.

WEITERE ERGEBNISSE
11. Rückfrageliste als Tabelle: Nr. | Fehlende Angabe oder Unterlage | Wofür sie
    gebraucht wird | Antwort (leer).
12. Mandantenanschreiben, Sie-Form, höchstens 250 Wörter: was geprüft wurde, was
    der Nachweis voraussetzt, welche Kosten anfallen, dass die Kanzlei den Wert
    nicht selbst ermittelt, und die Bitte um Entscheidung. Keine Zusage eines
    Ergebnisses, keine Erfolgsaussage, keine Zahl ohne Beleg.
13. Interner Vermerk für die Akte, höchstens 250 Wörter, mit dem ausdrücklichen
    Hinweis, welche Fristen im Raum stehen und wer sie erfasst hat.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Benenne fehlende Angaben
   einzeln und arbeite mit ausdrücklich benannten Annahmen.
2. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV, also Norm mit Absatz und
   Satz, Erlass mit Datum oder Entscheidung mit Datum und Aktenzeichen, jeweils
   mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine Absätze, keine
   Erlasse und keine Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Nenne KEINE Prozentschwelle, KEINEN Zeitraum, KEINE Frist, KEINEN Hebesatz
   und KEINEN Betrag als feststehenden Wert. Jede solche Größe nur als
   nachzuschlagende Angabe mit dem Zusatz "für [JAHR] verifizieren".
4. Gib KEINE Erfolgsprognose ab. Sage nicht, ob der Nachweis gelingen wird,
   sondern nur, welche Voraussetzungen erfüllt sein müssen und welche davon nach
   den Angaben belegt sind.
5. Halte durchgehend auseinander: die Frage, ob der Nachweis zulässig ist, die
   Frage, ob er sich lohnt, und die Frage, ob der Bescheid einen individuellen
   Sachfehler enthält.
6. ABBRUCHREGEL: Benennen die Angaben ausdrücklich eine erwogene Selbstanzeige,
   ein laufendes Steuerstrafverfahren oder eine bewusst unrichtig abgegebene
   Feststellungserklärung, arbeite DIESES Objekt nicht weiter ab. Gib für es
   nur aus: "Ausgesteuert – Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs." Unrichtige Sachangaben, die zu einem ZU HOHEN
   Grundsteuerwert geführt haben, sind KEIN Abbruchgrund – sie sind Gegenstand
   von Schritt 10. Weise nur darauf hin, dass eine Berichtigungspflicht nach
   § 153 AO eine mögliche Steuerverkürzung voraussetzt und dass ihre Prüfung dem
   Berufsträger obliegt (§ 153 Abs. 1 Satz 1 Nr. 1 AO – für [JAHR] verifizieren).
   Die übrigen Objekte bearbeitest du normal weiter und weist die ausgesteuerten
   gesondert aus.

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit"
2. "Modell und Verfahrensstand"
3. "Kommt der Nachweis in Betracht?" mit den Schritten 3 bis 5
4. "Nachweismittel und Anforderungen" mit den Schritten 6 und 7
5. "Kosten-Nutzen-Tabelle" mit Leerfeldern
6. "Anhängiger Einspruch: Wege und Folgen"
7. "Individuelle Bewertungsfehler"
8. "Fristarten mit Rechtsgrundlage"
9. "Rückfrageliste"
10. "Mandantenanschreiben (Entwurf)"
11. "Interner Vermerk"
12. "Ausgesteuerte Objekte"
13. "Was ich nicht sicher weiß"
```

## Anwendung

1. Vor dem Prompt Bescheid und Verfahrensstand heraussuchen. Ob die Rechtsbehelfsfrist noch läuft, entscheidet über den ganzen weiteren Weg und wird am Bescheid abgelesen, nicht geschätzt.
2. Bundesland und Modell klären. Im Landesmodell gilt die Nachweismöglichkeit des Bewertungsgesetzes nicht; dort ist das Landesgrundsteuergesetz zu lesen.
3. Die Gegenüberstellung von festgestelltem Grundsteuerwert und behauptetem gemeinen Wert selbst ausfüllen und die Abweichung selbst rechnen. Der Prompt liefert das Raster, nicht die Zahl.
4. Vor der Beauftragung eines Sachverständigen den Anforderungskatalog mit ihm durchgehen, insbesondere Wertermittlungsstichtag und Qualifikationsnachweis. Ein Gutachten auf einen falschen Stichtag ist als Nachweis wertlos.
5. Bei anhängigem Einspruch getrennt entscheiden: Stützt er sich allein auf die Verfassungsfrage, ist nach den Entscheidungen des Bundesfinanzhofs vom 12.11.2025 zu überlegen, ihn zurückzunehmen; stützt er sich auf einen niedrigeren gemeinen Wert oder einen Sachfehler, wird er weiterverfolgt und begründet.
6. Kosten und erwartete jährliche Entlastung dem Mandanten schriftlich gegenüberstellen und die Entscheidung von ihm einholen. Ein Gutachten kann auch einen höheren Wert ausweisen – dieser Hinweis gehört ins Anschreiben.

## Qualitätssicherung

- **Der Prompt bewertet nicht und rechnet nicht.** Jede Zahl in der Antwort, die nicht aus den Eingaben stammt, wird gelöscht. Die Abweichung zwischen Grundsteuerwert und gemeinem Wert rechnet die Kanzlei.
- **Die Schwelle ist eine Zugangsvoraussetzung.** Der Nachweis kommt nur in Betracht, wenn der festgestellte Grundsteuerwert den nachgewiesenen gemeinen Wert um mindestens 40 Prozent übersteigt (§ 220 Abs. 2 BewG, Schwelle – für [JAHR] verifizieren). Liegt die Abweichung darunter, ist der Weg versperrt, und ein Gutachtenauftrag wäre eine vermeidbare Ausgabe.
- **Der Kaufpreis ist kein zugelassenes Nachweismittel.** § 220 Abs. 2 Satz 3 BewG verweist nur auf § 198 Abs. 1 Satz 2 und Abs. 2 BewG; § 198 Abs. 3 BewG, der den im gewöhnlichen Geschäftsverkehr zustande gekommenen Kaufpreis regelt, ist gerade nicht in Bezug genommen (Reichweite der Verweisung – für [JAHR] verifizieren). Ein Einspruch, der allein auf einen Kaufpreis gestützt wird, trägt deshalb nicht; der Kaufpreis gehört als Unterlage zum Sachverständigen.
- **Die Vorschrift ist jung.** § 220 Abs. 2 BewG wurde durch das Jahressteuergesetz 2024 eingefügt und ist am 06.12.2024 in Kraft getreten; ältere Merkblätter und Kanzleivorlagen bilden das nicht ab. Für welchen Feststellungszeitpunkt sie gilt, ist an der Anwendungsvorschrift nachzulesen (Anwendungsregelung – für [JAHR] verifizieren).
- **Der Bundesfinanzhof hat die Verfassungsfrage entschieden.** Mit Urteilen vom 12.11.2025 – II R 25/24, II R 31/24 und II R 3/25 hat er das Bundesmodell für verfassungskonform gehalten und nicht vorgelegt. **Ob dagegen Verfassungsbeschwerden anhängig sind, ist nicht belegt** – dieser Punkt bleibt offen und wird gegenüber dem Mandanten weder in die eine noch in die andere Richtung behauptet.
- **Einsprüche, die allein auf die Verfassungsfrage gestützt sind, sind zu überprüfen.** Ob zurückgenommen oder weiterverfolgt wird, entscheidet der Berufsträger gemeinsam mit dem Mandanten und hält die Entscheidung schriftlich fest.
- **Fristen berechnet und erfasst ein Mensch**, bei Rechtsbehelfsfristen ausnahmslos mit Nachprüfung durch eine zweite Person. Kein Datum und keine Fristlänge aus der KI-Antwort übernehmen.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Verfahrensstand, Fristerfassung und Anforderungskatalog nach. Anschreiben an den Mandanten, Einspruchsrücknahme und jeder Schriftsatz an das Finanzamt werden von einem Berufsträger freigegeben; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 220 Abs. 2 BewG sowie § 198 Abs. 1 Satz 2 und Abs. 2 BewG im amtlichen Volltext (gesetze-im-internet.de) einschließlich der Anwendungsvorschriften; dem Jahressteuergesetz 2024 (Art. 35 Nr. 5, BGBl. 2024 I Nr. 387, in Kraft seit 06.12.2024); den Urteilen des Bundesfinanzhofs vom 12.11.2025 – II R 25/24, II R 31/24 und II R 3/25 im Volltext; dem Landesgrundsteuergesetz des Belegenheitslandes; der Immobilienwertermittlungsverordnung; sowie DATEV LEXinform. Alle Angaben am Original nachlesen (Stand – für [JAHR] verifizieren).

## Varianten

- **Erstauskunft am Telefon:** „Erzeuge nur eine Kurzfassung in höchstens 150 Wörtern, die dem Mandanten sagt, welche drei Angaben die Kanzlei braucht, bevor sie die Frage überhaupt beantworten kann."
- **Mehrere Objekte:** „Bearbeite eine Liste von Objekten, gib je Objekt nur das Ergebnisraster aus – (Nachweis kommt in Betracht), (kommt nicht in Betracht), (nicht entscheidbar) – und ordne sie nach der Höhe der möglichen jährlichen Auswirkung, ohne einen Betrag zu nennen."
- **Auftrag an den Sachverständigen:** „Erzeuge ausschließlich das Anforderungsschreiben an den Sachverständigen mit Wertermittlungsstichtag, Objektabgrenzung, zu berücksichtigenden Merkmalen und der Liste der übergebenen Unterlagen – als Leerformular ohne Objektbezeichnung."
- **Rücknahme des Einspruchs:** „Erzeuge ausschließlich den Entwurf der Rücknahmeerklärung und den Vermerk über die Belehrung des Mandanten zu den Folgen der Rücknahme."
- **Anschluss:** Anzeigepflichten nach einer Änderung Prompt 71, Bescheidabgleich Prompt 32, Einspruchsbegründung Prompt 33, Fristenkonzept Prompt 35.
