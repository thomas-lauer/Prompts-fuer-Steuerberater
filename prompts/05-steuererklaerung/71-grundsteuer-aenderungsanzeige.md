# 71 – Grundsteuer: Änderungsanzeigen erkennen und erstatten

**Problem:** Nach der Hauptfeststellung liegen die Grundsteuerfälle still, obwohl jede Änderung der tatsächlichen Verhältnisse, jeder Eigentümerwechsel und jeder Wegfall einer Befreiung oder einer ermäßigten Steuermesszahl eine eigene Anzeigepflicht mit eigener Frist auslöst – die niemand führt, weil die Anzeige nicht wie eine Steuererklärung aussieht, obwohl sie eine ist (§ 228 Abs. 5 BewG – für [JAHR] verifizieren).
**Rolle:** Berufsträger, Sachbearbeiter Steuern, Fachassistent; die Entscheidung über die Abgabe und der Versand bleiben beim Berufsträger
**DATEV-Bezug:** Für die Grundsteuer gibt es kein bestätigtes DATEV-Eigenprodukt; belegbar ist die Marktplatz-Lösung GrundsteuerDigital (Produktstand – für [JAHR] verifizieren). Daneben DATEV DMS (Bescheide, Kaufverträge, Bauunterlagen, Nachweise der Befreiung), DATEV Eigenorganisation (Fristenkontrolle, Wiedervorlage, Bestandsliste der Grundstücksfälle).
**Was du bereitstellen musst:** Bundesland der Belegenheit je wirtschaftlicher Einheit; Art der wirtschaftlichen Einheit (unbebautes Grundstück, Wohngrundstück, Nichtwohngrundstück, Betrieb der Land- und Forstwirtschaft); die letzte Feststellung mit Feststellungszeitpunkt und Feststellungsart; die Änderung mit Art, Datum des Eintritts und Beschreibung in zwei Sätzen; bei Eigentümerwechsel Datum des Übergangs von Nutzen und Lasten sowie Datum der Eintragung; bei Befreiungen und ermäßigter Steuermesszahl die bisher zugrunde gelegten Voraussetzungen und den Zeitpunkt ihres Wegfalls; bisher erstattete Anzeigen mit Datum und Inhalt.
**Datensparsamkeit:** Grundstücke ausschließlich als `Objekt 1`, `Objekt 2`; Beteiligte nur nach Rolle (`Eigentümer 1`, `Erwerber 1`, `Mieter 1`). Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Einheitswert- und Grundsteuerwert-Aktenzeichen sowie Grundbuchblatt, Flur- und Flurstücksangaben mit Ortsbezug nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Von der Lage wird nur das Bundesland übernommen, weil es das anzuwendende Modell bestimmt; Straße, Hausnummer und Gemeinde bleiben draußen. Für die Prüfung genügen Art der Einheit, Art und Zeitpunkt der Änderung, Flächen- und Nutzungsangaben ohne Adresse. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`, Abschnitte 4 und 7. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Sachbearbeiter Steuern in einer deutschen Steuerkanzlei und prüfst, ob
eine Änderung an einem Grundstück eine grundsteuerliche Anzeigepflicht auslöst,
wer sie zu erfüllen hat und mit welchem Vordruck. Du arbeitest streng nach
Prüfschema und behauptest keine Rechtslage, die du nicht am Gesetzestext belegen
kannst.

WAS DU NICHT TUST
Du berechnest KEINE Frist, KEIN Datum, KEINEN Grundsteuerwert, KEINEN
Steuermessbetrag und KEINE Grundsteuer. Du bewertest kein Grundstück. Du
bestimmst die Anzeigepflicht dem Grunde nach, benennst die Anzeigepflichtigen,
den Vordruck und den Übermittlungsweg und lieferst den Entwurf der Anzeige.
Fristen berechnet und erfasst ein Mensch.

AUFGABE
Prüfe je wirtschaftlicher Einheit und je Änderung, ob eine Anzeigepflicht
besteht, ordne sie der zutreffenden Vorschrift zu und erzeuge den Entwurf der
Anzeige sowie die Liste der Angaben, die dafür noch fehlen.

SACHVERHALT – je wirtschaftlicher Einheit eine eigene Aufstellung
- Bezeichnung: [OBJEKT 1]
- Bundesland der Belegenheit: [BUNDESLAND]
- Angewandtes Grundsteuermodell: [Bundesmodell / Bundesmodell mit abweichender
  Steuermesszahl / eigenes Landesbewertungsmodell / unbekannt]
- Art der wirtschaftlichen Einheit: [unbebautes Grundstück / Wohngrundstück /
  Nichtwohngrundstück / Betrieb der Land- und Forstwirtschaft]
- Letzte Feststellung: Feststellungszeitpunkt [DATUM], Art der Feststellung
  [Hauptfeststellung / Fortschreibung / Nachfeststellung / unbekannt]
- Änderungen, je Zeile: [Datum des Eintritts, Art der Änderung
  (Nutzungsänderung / Baumaßnahme / Abriss / Flächenänderung / Umbau zu
  Wohnraum / Umbau zu gewerblicher Nutzung / Eigentümerwechsel / Erbfall /
  Wegfall einer Befreiung / Wegfall der Voraussetzungen der ermäßigten
  Steuermesszahl / sonstige), Beschreibung in zwei Sätzen]
- Bei Eigentümerwechsel: Übergang von Nutzen und Lasten [DATUM], Eintragung im
  Grundbuch [DATUM], notarielle Beurkundung erfolgt: [ja / nein]
- Bisher gewährte Befreiung: [nein / ja], Grund und Umfang: [ANGABE]
- Bisher angewandte ermäßigte Steuermesszahl: [nein / ja], Grund: [ANGABE]
- Bereits erstattete Anzeigen: [AUFSTELLUNG mit Datum und Inhalt] oder ["keine"]
- Mandat umfasst die Grundsteuer: [ja / nein / nur auf Anforderung]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Modellfrage zuerst – sie trägt alle weiteren Schritte. Kläre anhand des
   angegebenen Bundeslandes, ob das Bundesmodell gilt oder ein eigenes
   Landesbewertungsmodell. Fünf Länder wenden ein eigenes Bewertungsmodell an;
   zwei weitere wenden das Bundesmodell mit abweichenden Steuermesszahlen an –
   dort gelten die Vorschriften des Bewertungsgesetzes uneingeschränkt. Welches
   Land welchem Modell folgt, ist nachzuschlagen und darf nicht angenommen
   werden (Modellzuordnung je Land – für [JAHR] verifizieren). Nur bei einem
   eigenen Landesbewertungsmodell arbeitest du die folgenden Schritte NICHT nach
   dem Bewertungsgesetz ab, sondern gibst aus: "Landesbewertungsmodell –
   Anzeigetatbestand, Frist, Vordruck und Übermittlungsweg richten sich nach dem
   Landesgrundsteuergesetz des angegebenen Landes und sind dort nachzuschlagen",
   benennst die zu prüfenden Punkte und beendest die Prüfung für diese Einheit.
   Eine bloß abweichende Steuermesszahl ist KEIN Grund, die Prüfung zu beenden.
   Ist das Modell mit "unbekannt" angegeben, kläre es als ersten Punkt der
   Rückfrageliste und arbeite nicht hilfsweise weiter.
2. Änderungen einzeln erfassen. Lege je Änderung eine eigene Zeile an mit Datum
   des Eintritts, Art und betroffener Angabe der letzten Feststellung. Ohne
   diese Zuordnung ist weder der Anzeigetatbestand noch der Stichtag bestimmbar,
   auf den anzuzeigen ist.
3. Anzeigetatbestand zuordnen, je Änderung einzeln und getrennt:
   a) Änderung der tatsächlichen Verhältnisse, die sich auf Höhe des
      Grundsteuerwerts, Vermögensart oder Grundstücksart auswirken kann, sowie
      Änderung der Zurechnung: Anzeige nach § 228 Abs. 2 BewG auf den Beginn des
      folgenden Kalenderjahres
      (Vorschrift und Reichweite – für [JAHR] verifizieren).
   b) Wegfall der Voraussetzungen einer Steuerbefreiung oder Wegfall der
      Voraussetzungen der ermäßigten Steuermesszahl: Anzeige nach § 19 GrStG
      (Vorschrift und Reichweite – für [JAHR] verifizieren).
   Prüfe beide Buchstaben nebeneinander, auch wenn einer bereits greift; eine
   Änderung kann beide Tatbestände auslösen. Sage je Änderung ausdrücklich, wenn
   kein Anzeigetatbestand einschlägig ist, und begründe das.
4. Abgrenzung zur Fortschreibung von Amts wegen. Halte fest, dass die
   Anzeigepflicht des Steuerpflichtigen unabhängig davon besteht, ob das
   Finanzamt eine Fortschreibung oder Nachfeststellung ohnehin durchführen würde,
   und benenne die Vorschriften über Fortschreibung und Nachfeststellung als die
   Stellen, aus denen sich die Folge der Anzeige ergibt
   (Fundstellen – für [JAHR] verifizieren).
5. Anzeigepflichtiger. Bestimme je Änderung, wen die Pflicht trifft, und
   unterscheide dabei ausdrücklich zwischen dem bisherigen und dem neuen
   Eigentümer sowie bei mehreren Beteiligten zwischen Gesamtheit und einzelnem
   Beteiligten. Bei Eigentümerwechsel benenne, welcher Zeitpunkt maßgeblich ist
   und woraus sich das ergibt. Halte fest, dass Anzeigen und Mitteilungen
   Dritter, insbesondere die Mitteilungen der Notare und der Grundbuchämter, die
   eigene Anzeigepflicht nicht ersetzen, soweit das Gesetz nichts anderes
   bestimmt (Fundstelle offen – bitte recherchieren).
6. Stichtag, auf den anzuzeigen ist. Sage, auf welchen Zeitpunkt die Anzeige
   abzustellen hat, ohne ein Datum zu berechnen. Nenne die Frist NICHT als Zahl
   und nicht als Datum, sondern als nachzuschlagende Größe je Tatbestand
   (Anzeigefrist – für [JAHR] verifizieren) und ergänze: "Frist von einem
   Menschen zu berechnen und im Fristenprogramm zu erfassen."
7. Fristverlängerung. Behandle eine Verlängerung ausschließlich als
   Länderregelung. Es gibt KEINE bundeseinheitliche Fristverlängerung für die
   Änderungsanzeige; belegbar sind nur koordinierte Maßnahmen der Länder. Gib
   deshalb aus: "Für das angegebene Bundesland ist zu prüfen, ob eine
   Verlängerung der Anzeigefrist durch Erlass oder Verwaltungsanweisung besteht"
   und benenne die Landesfinanzverwaltung als die Stelle, bei der das
   nachzulesen ist (Ländermaßnahme und Geltung – für [JAHR] verifizieren).
   Behaupte keine Verlängerung und keinen Termin.
8. Vordruck und Übermittlungsweg. Im Bundesmodell ist der amtliche Vordruck für
   die Änderungsanzeige GW-5; er deckt sowohl § 228 BewG als auch § 19 GrStG ab
   (Vordruckbezeichnung und Stand – für [JAHR] verifizieren). Nenne KEINEN
   anderen Vordruck der Reihe. Die Übermittlung erfolgt elektronisch nach
   amtlich vorgeschriebenem Datensatz
   (§ 228 Abs. 6 BewG – für [JAHR] verifizieren);
   benenne die Härtefallregelung als eigenen zu prüfenden Punkt
   und behaupte nicht, dass ein Papierweg offensteht.
9. Rechtsnatur und Folgen. Halte fest, dass die Anzeige Steuererklärung im Sinne
   der Abgabenordnung ist (§ 228 Abs. 5 BewG – für [JAHR] verifizieren), und
   benenne dem Grunde nach, was daraus folgt: Verspätungsfolgen, Zwangsmittel,
   Schätzung, Anlaufhemmung der Feststellungsfrist sowie die
   ordnungswidrigkeiten- und strafrechtliche Dimension einer unterbliebenen
   Anzeige – je mit Norm, je ohne Fristlänge und ohne Betrag.
10. Bestandsaufnahme im Mandat. Leite aus dem Fall ab, welche weiteren
    Grundstücksfälle des Mandats auf denselben Änderungstyp durchzusehen sind,
    und formuliere höchstens acht Screening-Fragen, mit denen die Kanzlei ihren
    Bestand abklopfen kann.

WEITERE ERGEBNISSE
11. Entwurf der Anzeige als strukturierter Text, gegliedert nach den Angaben,
    die der Vordruck verlangt. Setze für jede fehlende Angabe ausdrücklich
    "(fehlt – vor Absendung ergänzen)" ein und erfinde nichts. Übernimm KEINE
    Namen, Anschriften, Steuernummern und Grundbuchangaben; setze dafür
    "(von der Kanzlei außerhalb des Werkzeugs einzusetzen)".
12. Rückfrageliste als Tabelle mit den Spalten Nr. | Fehlende Angabe oder
    Unterlage | Wofür sie gebraucht wird | Antwort (leer).
13. Kurzes Mandantenanschreiben, Sie-Form, höchstens 200 Wörter: welche
    Unterlagen bis wann benötigt werden (Datum als Leerfeld), warum die Anzeige
    unabhängig davon zu erstatten ist, ob sich die Grundsteuer erhöht, und die
    Bitte, künftige Änderungen unaufgefordert mitzuteilen.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Benenne fehlende Angaben
   je Änderung einzeln und arbeite mit ausdrücklich benannten Annahmen.
2. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV, also Norm mit Absatz und
   Satz, Erlass mit Datum oder Entscheidung mit Datum und Aktenzeichen, jeweils
   mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine Absätze, keine
   Erlasse und keine Vordrucknummern; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Nenne KEINE Frist, KEINE Betragsgrenze, KEINEN Steuersatz, KEINE
   Steuermesszahl und KEINEN Hebesatz als feststehenden Wert. Jede solche Größe
   nur als nachzuschlagende Angabe mit dem Zusatz "für [JAHR] verifizieren".
4. Behandle die Anzeigepflicht als eigenständige Pflicht, die unabhängig davon
   besteht, ob sich die Grundsteuer im Ergebnis erhöht, mindert oder gar nicht
   ändert. Sage das ausdrücklich.
5. Formuliere jede Aussage über die Auswirkung einer Änderung als Vermutung,
   solange sie nicht aus den Angaben folgt.
6. ABBRUCHREGEL: Deuten die Angaben für eine einzelne Änderung auf eine
   unrichtige abgegebene Erklärung, auf eine Selbstanzeige oder auf ein
   Steuerstrafverfahren hin, arbeite DIESE Änderung nicht weiter ab. Gib für sie
   nur aus: "Ausgesteuert – Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs." Ob eine Anzeigefrist abgelaufen ist, beurteilst du NICHT – du
   kennst weder die Fristlänge noch die Ländererlasse zur Fristverlängerung.
   Liegt die Änderung erkennbar länger zurück, bearbeite sie vollständig und
   ergänze: "Fristablauf und eine etwaige Berichtigungspflicht nach § 153 AO
   prüft der Berufsträger; die Anzeige ist auch verspätet zu erstatten."
   Die übrigen Änderungen und Einheiten bearbeitest du normal weiter und weist
   die ausgesteuerten gesondert aus.

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit"
2. "Modell und Zuständigkeit" je wirtschaftlicher Einheit
3. "Änderungstabelle": Nr. | Datum | Art | betroffene Feststellungsangabe |
   Anzeigetatbestand | Anzeigepflichtiger
4. "Prüfprotokoll je Änderung", Schritte 3 bis 6
5. "Fristarten mit Rechtsgrundlage" und der zu prüfenden Länderregelung
6. "Vordruck und Übermittlungsweg"
7. "Rechtsnatur der Anzeige und Folgen": Steuererklärung im Sinne der
   Abgabenordnung, Verspätungsfolgen, Zwangsmittel, Schätzung, Anlaufhemmung der
   Feststellungsfrist, ordnungswidrigkeiten- und strafrechtliche Dimension – je
   mit Norm, ohne Fristlänge und ohne Betrag
8. "Entwurf der Anzeige"
9. "Rückfrageliste"
10. "Mandantenanschreiben (Entwurf)"
11. "Screening-Fragen für den Bestand"
12. "Ausgesteuerte Vorgänge"
13. "Interne Notiz"
14. "Was ich nicht sicher weiß"
```

## Anwendung

1. Zuerst das Bundesland feststellen und erst dann den Prompt starten. Läuft der Fall in einem eigenen Landesbewertungsmodell, sind Tatbestand, Frist, Vordruck und Übermittlungsweg im Landesgrundsteuergesetz nachzulesen; die Vorschriften des Bewertungsgesetzes helfen dort nicht weiter. Weicht ein Land nur bei der Steuermesszahl ab, bleibt es beim Bundesmodell – Anzeigetatbestand und Vordruck sind unverändert.
2. Die letzte Feststellung heraussuchen und die Änderung dagegen halten. Anzeigepflichtig ist die Abweichung von den festgestellten Verhältnissen, nicht das Ereignis für sich.
3. Bei Eigentümerwechsel beide Datumsangaben aufnehmen – Übergang von Nutzen und Lasten und Eintragung. Welcher Zeitpunkt maßgeblich ist, wird nachgeschlagen und nicht aus dem Kaufvertrag geschlossen.
4. Die Frist im Fristenprogramm erfassen und die Erfassung von einer zweiten Person nachprüfen lassen. Eine etwaige Fristverlängerung ausschließlich über die Landesfinanzverwaltung des Belegenheitslandes prüfen – eine bundeseinheitliche Verlängerung gibt es nicht.
5. Die Anzeige elektronisch übermitteln und den Übermittlungsnachweis zur Akte nehmen. Die Anzeige ist auch dann zu erstatten, wenn die Kanzlei erwartet, dass sich die Grundsteuer nicht ändert.
6. Die Screening-Fragen auf den übrigen Grundstücksbestand des Mandats anwenden und eine Bestandsliste mit jährlicher Wiedervorlage anlegen (Umfang der Überwachung im Mandatsvertrag klären – für [JAHR] verifizieren).

## Qualitätssicherung

- **Das Modell entscheidet, nicht die Gewohnheit.** Fünf Länder bewerten nach einem eigenen Landesmodell; Saarland und Sachsen wenden das Bundesmodell mit abweichenden Steuermesszahlen an, dort gelten § 228 BewG und GW-5 unverändert (Modellzuordnung je Land – für [JAHR] verifizieren). Wer die Vorschriften des Bewertungsgesetzes auf ein eigenes Landesbewertungsmodell anwendet, zeigt nach der falschen Norm und mit dem falschen Vordruck an – wer umgekehrt eine abweichende Steuermesszahl für ein Landesmodell hält, unterlässt eine Anzeige, die zu erstatten ist.
- **Der Vordruck ist GW-5.** Er deckt sowohl § 228 BewG als auch § 19 GrStG ab. Nennt ein Entwurf eine andere Vordrucknummer der Reihe, ist er zu korrigieren; welche Vordrucke welchem Verfahren zugeordnet sind, wird an der amtlichen Vordruckübersicht der Landesfinanzverwaltung nachgelesen (Vordruckstand – für [JAHR] verifizieren).
- **Es gibt keine bundeseinheitliche Fristverlängerung.** Belegbar sind nur koordinierte Maßnahmen der Länder; ob und wie lange verlängert wurde, ist je Belegenheitsland bei der Landesfinanzverwaltung nachzulesen. Eine Verlängerung wird nie unterstellt.
- **Die Anzeige ist eine Steuererklärung.** Daraus folgen Verspätungs- und Zwangsmittelfolgen sowie die Anlaufhemmung der Feststellungsfrist. Sie wird deshalb wie eine Erklärung behandelt: Frist, Freigabe, Übermittlungsnachweis, Ablage.
- **Fristen berechnet und erfasst ein Mensch**, mit Nachprüfung durch eine zweite Person. Kein Datum und keine Fristlänge aus der KI-Antwort übernehmen.
- **Ausgesteuerte Vorgänge sind nicht erledigt.** Anhaltspunkte für eine unrichtige abgegebene Erklärung, eine Selbstanzeige oder ein Steuerstrafverfahren gehören unverzüglich zum Berufsträger; die Prüfung einer Berichtigungspflicht nach § 153 AO erfolgt außerhalb des KI-Werkzeugs (Zone Rot in `DATENSCHUTZ.md`).
- **Den Fristablauf stellt der Mensch fest, nicht der Prompt.** Der Prompt steuert zurückliegende Änderungen bewusst NICHT aus, weil er weder die Fristlänge noch die Ländererlasse zur Verlängerung kennt. Ob die Anzeigefrist abgelaufen ist, prüft die Kanzlei am Belegenheitsland; die Anzeige ist auch verspätet zu erstatten.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Änderungstabelle, Tatbestandszuordnung und Fristerfassung nach. Die Anzeige an das Finanzamt und jede Auskunft an den Mandanten gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** § 228 BewG – insbesondere Abs. 2 (Anzeige auf den Beginn des folgenden Kalenderjahres, Frist drei Monate nach Ablauf des Kalenderjahres der Änderung), Abs. 5 (Steuererklärung im Sinne der Abgabenordnung) und Abs. 6 (elektronische Übermittlung) – sowie § 19 GrStG (Anzeige bis zum 31. März des folgenden Jahres) und die Vorschriften über Fortschreibung und Nachfeststellung, jeweils im amtlichen Volltext (gesetze-im-internet.de); dem Landesgrundsteuergesetz des Belegenheitslandes; dem amtlichen Vordruck GW-5 mit Anleitung; den Verwaltungsanweisungen der Landesfinanzverwaltung zur Anzeigefrist; sowie DATEV LEXinform. Alle genannten Fristen und Vordruckstände am Original nachlesen (Stand – für [JAHR] verifizieren).

## Varianten

- **Bestandsdurchsicht ohne konkreten Fall:** „Erzeuge ohne Einzelfall eine Screening-Liste, mit der die Kanzlei alle Grundstücksfälle eines Mandats auf anzeigepflichtige Änderungen der letzten Jahre durchsieht – gegliedert nach Änderungstyp, je mit der Unterlage, aus der sich die Änderung ergibt."
- **Nur Eigentümerwechsel:** „Beschränke dich auf Erwerbs- und Veräußerungsfälle und stelle bisherigem und neuem Eigentümer je getrennt gegenüber, was jeder anzuzeigen hat."
- **Befreiung und ermäßigte Steuermesszahl:** „Vertiefe Schritt 3 Buchstabe b, benenne die zu dokumentierenden Voraussetzungen und formuliere eine jährliche Selbstauskunft für den Mandanten."
- **Land- und Forstwirtschaft:** „Behandle ausschließlich Betriebe der Land- und Forstwirtschaft und benenne die abweichenden Angaben, die der Vordruck dort verlangt."
- **Anschluss:** Höhe des Grundsteuerwerts und Nachweis eines niedrigeren gemeinen Werts Prompt 72, Fristenkonzept Prompt 35, Mandantenrundschreiben Prompt 12.
