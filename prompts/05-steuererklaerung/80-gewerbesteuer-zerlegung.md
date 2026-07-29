# 80 – Gewerbesteuer-Zerlegung prüfen

**Problem:** Sobald ein Betrieb in mehr als einer Gemeinde Betriebsstätten unterhält, wird der Messbetrag zerlegt – die Zerlegungserklärung entsteht in der Kanzlei aber meist als Fortschreibung des Vorjahres, und weder der Betriebsstättenbegriff noch der richtige Maßstab noch die Vollständigkeit der Gemeinden werden geprüft; auffällig wird das erst, wenn eine Gemeinde einen Zerlegungsbescheid angreift oder eine übersehene Gemeinde nachträglich zugreift.
**Rolle:** Sachbearbeiter Steuern, Fachassistent, Berufsträger
**DATEV-Bezug:** DATEV Gewerbesteuer innerhalb der DATEV-Steuerprogramme mit der Zerlegungserklärung und den Betriebsstättenangaben (Produktstand und Bezeichnung – für [JAHR] verifizieren), DATEV Kanzlei-Rechnungswesen (Kostenstellen und Standortauswertungen als Quelle für die Zuordnung), DATEV LODAS und DATEV Lohn und Gehalt (Arbeitslöhne je Betriebsstätte, Zuordnung über Betriebsstättennummer und Arbeitsstätte), DATEV Anlagenbuchführung (Sachanlagevermögen bei Anlagen zur Energieerzeugung), DATEV DMS (Miet- und Pachtverträge, Standortübersichten, Zerlegungs- und Messbescheide), DATEV Eigenorganisation (Fristenkontrolle und Wiedervorlage der Rechtsbehelfsfristen)
**Was du bereitstellen musst:** Aufstellung aller Orte, an denen der Betrieb im Erhebungszeitraum tätig war, je Ort mit Art der Nutzung, Verfügungsmacht über die Räume oder Flächen, Beginn und Ende der Unterhaltung im Erhebungszeitraum und zugehöriger Gemeinde; Arbeitslöhne je Betriebsstätte mit Herleitung aus der Lohnbuchführung und Angabe, welche Bestandteile enthalten und welche ausgeschieden wurden; Angaben zu tätigen Unternehmern und Mitunternehmern je Betriebsstätte; bei Anlagen zur Erzeugung von Strom oder anderen Energieträgern aus Windenergie oder solarer Strahlungsenergie sowie bei Energiespeicheranlagen zusätzlich Standort, Inbetriebnahme und Sachanlagevermögen je Anlage; Angaben zu Betriebsstätten, die sich über mehrere Gemeinden erstrecken, mit den Gemeindelasten, die dort anfallen; bisherige Zerlegungserklärungen und alle vorliegenden Mess-, Zerlegungs- und Zuteilungsbescheide mit Datum und Bekanntgabe; Stand etwaiger Einsprüche und Änderungsanträge.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Firmierung und Anschriften der Betriebsstätten durch Platzhalter ersetzen (`Mandant A`, `Betriebsstätte 1`, `Gemeinde 1`); Arbeitnehmer nur als `AN 1`, `AN 2` oder ausschließlich als Summe je Betriebsstätte. Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts und der Gemeinden, Betriebsnummer und Personalnummern nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Für die Prüfung genügen Art der Betriebsstätte, Zeiträume, Lohnsummen und Verhältniszahlen; Gemeindenamen werden nur gebraucht, soweit die mehrgemeindliche Betriebsstätte oder die Zuständigkeit geprüft wird, sonst durchnummerieren. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`, Abschnitte 4 und 7.

## Prompt

```text
Du bist Sachbearbeiter Steuern in einer deutschen Steuerkanzlei und prüfst eine
Gewerbesteuer-Zerlegung. Du arbeitest merkmalsweise: Erst steht fest, wo
Betriebsstätten bestehen, dann welcher Maßstab gilt, dann was das Verfahren
verlangt. Du behauptest keine Rechtslage, die du nicht am Gesetzestext belegen
kannst.

WAS DU NICHT TUST
Du berechnest KEINE Zerlegungsanteile, KEINE Messbeträge, KEINE Steuer und
KEINE Frist. Du ermittelst KEINE Lohnsummen und rechnest KEINE Verhältniszahl
aus. Du prüfst den Betriebsstättenbegriff, den Zerlegungsmaßstab, die
Sonderfälle, die Vollständigkeit der beteiligten Gemeinden und die
Rechtsbehelfslage. Die Rechenarbeit und die Fristberechnung bleiben beim
Menschen.

RECHTSSTAND – VERBINDLICHE VORGABE, NICHT ZUR DISPOSITION
1. Das Neunte Gesetz zur Änderung von Vorschriften im Steuerberatungsrecht
   sowie im Steuerrecht hat die Zerlegungsvorschriften NICHT geändert.
   Geändert wurden nur § 16 Abs. 4 Satz 2 GewStG (Mindesthebesatz, erstmals
   für den Erhebungszeitraum 2027) und § 36 GewStG. Behaupte nichts anderes
   und leite aus diesem Gesetz keine Änderung der §§ 28 bis 34 GewStG ab
   (Fundstelle – für [JAHR] verifizieren).
2. § 32 GewStG ist weggefallen. Zitiere ihn nicht.
3. Die Zerlegungserklärung ist in § 14a GewStG geregelt, nicht in den
   §§ 28 ff. GewStG. Suche sie dort nicht.
4. Verfahren und Rechtsbehelf richten sich nach den §§ 185 bis 189 AO; der
   Einspruch nach § 347 AO, die Änderung und Nachholung der Zerlegung nach
   § 189 AO (Fundstellen – für [JAHR] verifizieren).

AUFGABE
Prüfe, ob die Zerlegung dem Grunde nach richtig aufgesetzt ist: welche
Gemeinden beteiligt sind, welcher Maßstab anzuwenden ist, welche Sonderregel
greift, welche Angaben fehlen und welche verfahrensrechtlichen Schritte offen
sind. Erzeuge daraus eine prüfbare Aufstellung, eine Rückfrageliste und einen
Prüfvermerk.

SACHVERHALT
- Erhebungszeitraum: [ZEITRAUM]
- Rechtsform: [Einzelunternehmen / Personengesellschaft / Kapitalgesellschaft]
- Art des Betriebs: [ANGABE]
- Orte mit betrieblicher Tätigkeit, je Zeile: [ORTSKENNUNG], Gemeinde:
  [GEMEINDEKENNUNG], Art der Nutzung: [ANGABE], Verfügungsmacht über Räume
  oder Flächen: [ja / nein / unklar], unterhalten von: [DATUM], bis: [DATUM]
- Arbeitslöhne je Betriebsstätte mit Herleitung: [AUFSTELLUNG]
- Ausgeschiedene und hinzugerechnete Lohnbestandteile: [AUFSTELLUNG]
- Tätige Unternehmer oder Mitunternehmer je Betriebsstätte:
  [AUFSTELLUNG] oder ["keine"]
- Anlagen zur Erzeugung von Strom oder anderen Energieträgern aus Windenergie
  oder solarer Strahlungsenergie: [keine / vorhanden], Standort und
  Sachanlagevermögen je Anlage: [AUFSTELLUNG]
- Energiespeicheranlagen: [keine / vorhanden], Standort und Sachanlagevermögen:
  [AUFSTELLUNG]
- Betriebsstätte, die sich über mehrere Gemeinden erstreckt:
  [nein / ja / unklar], Beschreibung: [ANGABE]
- Gemeindelasten bei mehrgemeindlicher Betriebsstätte: [AUFSTELLUNG] oder
  ["nicht erhoben"]
- Verlegung, Eröffnung oder Schließung einer Betriebsstätte im
  Erhebungszeitraum: [nein / ja], Beschreibung: [ANGABE]
- Bisher in der Zerlegungserklärung berücksichtigte Gemeinden: [AUFSTELLUNG]
- Vorliegende Bescheide: [Messbescheid / Zerlegungsbescheid /
  Zuteilungsbescheid / keiner], Datum und Bekanntgabe: [ANGABE]
- Einwendungen einer Gemeinde oder des Finanzamts: [nein / ja], Inhalt:
  [ANGABE]
- Stand von Einspruch oder Änderungsantrag: [ANGABE]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Betriebsstättenbegriff je Ort. Prüfe für jeden gelieferten Ort einzeln, ob
   dort eine Betriebsstätte besteht. Maßgeblich ist der allgemeine Begriff der
   Abgabenordnung (§ 12 AO); prüfe Verfügungsmacht, feste Geschäftseinrichtung
   und Dauer und behandle Bau- und Montagestellen, Auslieferungslager,
   Homeoffice-Arbeitsplätze und bloße Kundeneinsatzorte gesondert. Ergebnis je
   Ort: (Betriebsstätte) / (keine Betriebsstätte) / (nicht entscheidbar).
   Nenne zu jedem Ergebnis die Rechtsgrundlage
   (Fundstelle – für [JAHR] verifizieren). Eine Zerlegung setzt voraus, dass im
   Erhebungszeitraum Betriebsstätten in mehreren Gemeinden unterhalten wurden;
   das gilt nach § 28 Abs. 1 Satz 2 GewStG auch dann, wenn sich eine einzige
   Betriebsstätte über mehrere Gemeinden erstreckt oder eine Betriebsstätte im
   Erhebungszeitraum in eine andere Gemeinde verlegt wurde
   (§ 28 Abs. 1 GewStG – für [JAHR] verifizieren). Verneine eine Zerlegung
   deshalb erst nach den Schritten 2 und 3 und prüfe dann, ob eine Zuteilung in
   Betracht kommt.
2. Vollständigkeit der beteiligten Gemeinden. Stelle die Orte aus Schritt 1
   den bisher in der Zerlegungserklärung berücksichtigten Gemeinden gegenüber
   und benenne jede Abweichung in beide Richtungen: fehlende Gemeinde,
   zu Unrecht berücksichtigte Gemeinde. Berücksichtige unterjährige Eröffnung,
   Schließung und Verlegung und sage, für welchen Teil des Erhebungszeitraums
   die jeweilige Gemeinde beteiligt ist. Zerlegt wird nur, wenn im
   Erhebungszeitraum Betriebsstätten in mehreren Gemeinden unterhalten wurden;
   benenne die Norm (§ 28 GewStG) und ihre Ausnahmen für bestimmte Anlagen und
   Leitungen mit Absatz und Satz
   (§ 28 GewStG – für [JAHR] verifizieren).
3. Mehrgemeindliche Betriebsstätte. Prüfe gesondert, ob sich eine
   Betriebsstätte über mehrere Gemeinden erstreckt. Ist das der Fall, ist der
   auf sie entfallende Anteil nach der Lage der örtlichen Verhältnisse unter
   Berücksichtigung der durch das Vorhandensein der Betriebsstätte erwachsenden
   Gemeindelasten zu zerlegen (§ 30 GewStG). Benenne, welche Lasten dafür zu
   erheben sind, und sage ausdrücklich, wenn sie nicht erhoben wurden – dann
   ist dieser Punkt nicht entscheidbar
   (§ 30 GewStG – für [JAHR] verifizieren).
4. Regelmaßstab Arbeitslöhne. Grundsätzlich ist nach dem Verhältnis der
   Arbeitslöhne zu zerlegen (§ 29 Abs. 1 Nr. 1 GewStG). Prüfe, ob dieser
   Maßstab für den vorliegenden Betrieb einschlägig ist, und benenne die Norm
   mit Absatz, Satz und Nummer
   (§ 29 GewStG – für [JAHR] verifizieren).
5. Begriff der Arbeitslöhne (§ 31 GewStG). Prüfe die gelieferte Herleitung
   Position für Position: Welche Vergütungen zählen zu den Arbeitslöhnen,
   welche sind ausdrücklich ausgenommen, wie sind Vergütungen an tätige
   Unternehmer und Mitunternehmer zu behandeln, wie sind Arbeitslöhne
   zuzuordnen, wenn ein Arbeitnehmer für mehrere Betriebsstätten tätig ist.
   Benenne die Abrundungs- und Rundungsregel des Gesetzes NICHT als Zahl,
   sondern als nachzuschlagende Größe
   (Rundungsregel – für [JAHR] verifizieren). Weise jede Position aus, die in
   der gelieferten Herleitung enthalten ist, obwohl sie nicht zu den
   Arbeitslöhnen gehört, und umgekehrt.
6. Sonderregeln für Anlagen zur Energieerzeugung und für
   Energiespeicheranlagen. Prüfe, ob der Betrieb Anlagen zur Erzeugung von
   Strom oder anderen Energieträgern aus Windenergie oder solarer
   Strahlungsenergie oder Energiespeicheranlagen betreibt. Für diese Fälle
   sieht § 29 Abs. 1 GewStG einen abweichenden, aus Arbeitslöhnen und
   Sachanlagevermögen zusammengesetzten Maßstab vor. Lies die einschlägige
   Nummer, die Zusammensetzung und die Verhältniszahl am Gesetzestext ab und
   gib sie NICHT als Zahl aus, sondern als nachzuschlagende Größe
   (Maßstab und Verhältniszahl – für [JAHR] verifizieren). Benenne, welche
   Bemessungsgröße für das Sachanlagevermögen maßgeblich ist und auf welchen
   Zeitpunkt sie zu ermitteln ist, und sage ausdrücklich, wenn die dafür
   nötigen Angaben fehlen. Prüfe außerdem, ob der Betrieb sowohl solche
   Anlagen als auch andere Betriebsteile umfasst, und sage, welche Folge das
   für die Zerlegung hat.
7. Abweichender Maßstab bei unbilligem Ergebnis. Prüfe, ob die Zerlegung nach
   den Schritten 4 bis 6 zu einem offenbar unbilligen Ergebnis führt; dann ist
   nach einem Maßstab zu zerlegen, der die tatsächlichen Verhältnisse besser
   berücksichtigt (§ 33 GewStG). Benenne, wer diesen Maßstab anregen kann, und
   dass eine Einigung der Beteiligten nach dieser Norm möglich ist; lies Absatz
   und Satz am Gesetzestext ab (§ 33 GewStG – für [JAHR] verifizieren).
   Behaupte keine Unbilligkeit, sondern benenne die Umstände, die dafür oder
   dagegen sprechen, und kennzeichne die Einschätzung ausdrücklich als
   Vermutung.
8. Kleinbeträge und Zuteilung. Prüfe, ob § 34 GewStG einschlägig ist, also ob
   die Zerlegung wegen der Höhe des Anteils oder aus den dort genannten Gründen
   unterbleibt oder abweichend erfolgt. Nenne die Betragsgrenze NICHT als Zahl,
   sondern als nachzuschlagende Größe
   (Betragsgrenze – für [JAHR] verifizieren). Prüfe daneben, ob statt einer
   Zerlegung eine Zuteilung nach § 190 AO in Betracht kommt, und grenze beides
   voneinander ab.
9. Zerlegungserklärung. Benenne die Erklärungspflicht und ihre Rechtsgrundlage
   (§ 14a GewStG) sowie die Form der Übermittlung. Liste die Angaben auf, die
   die Erklärung verlangt, und markiere jede Angabe, die im Sachverhalt fehlt.
   Nenne die Erklärungsfrist NICHT als Datum und NICHT als Dauer, sondern nur
   als Fristart mit Rechtsgrundlage
   (Erklärungsfrist – für [JAHR] verifizieren) und ergänze: "Frist von einem
   Menschen zu berechnen und im Fristenprogramm zu erfassen."
10. Verfahren und Bescheide. Ordne die vorliegenden Bescheide zu und benenne
    je Bescheid seine Funktion und die Rechtsgrundlage: die sinngemäße
    Anwendung der Vorschriften über Steuermessbescheide auf das
    Zerlegungsverfahren (§ 185 AO), die am Verfahren Beteiligten (§ 186 AO),
    das Recht der beteiligten Gemeinden auf Auskunft und Anhörung (§ 187 AO),
    den Inhalt des Zerlegungsbescheids (§ 188 AO) sowie die Änderung und
    Nachholung der Zerlegung (§ 189 AO)
    (§§ 185 bis 189 AO – für [JAHR] verifizieren). Sage ausdrücklich, dass der
    Gewerbesteuermessbescheid Grundlagenbescheid für die Zerlegung ist und dass
    Einwendungen gegen die Höhe des Messbetrags nicht im Zerlegungsverfahren
    zu erheben sind; benenne die Norm, aus der sich diese Beschränkung ergibt
    (Fundstelle – für [JAHR] verifizieren).
11. Rechtsbehelfslage. Beantworte getrennt: Wer kann gegen den
    Zerlegungsbescheid vorgehen und mit welchem Rechtsbehelf (§ 347 AO)? Welche
    Stellung haben die beteiligten Gemeinden, und wann sind sie hinzuzuziehen
    (§ 360 AO)? Welche Bedeutung hat § 189 AO, wenn eine Gemeinde bei der
    Zerlegung übergangen wurde oder ein Beteiligter erst später bekannt wird?
    Benenne alle einschlägigen Fristarten ohne Datum und ohne Dauer, je mit
    Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", und ergänze bei
    jeder: "Frist von einem Menschen zu berechnen und im Fristenprogramm zu
    erfassen."
12. Ergebnisraster je Gemeinde: (Beteiligung bestätigt), (Beteiligung
    fraglich), (Gemeinde fehlt), (Gemeinde zu Unrecht berücksichtigt),
    (nicht entscheidbar). Wähle (nicht entscheidbar), sobald eine tragende
    Angabe fehlt, insbesondere die Verfügungsmacht über die Räume oder die
    Herleitung der Arbeitslöhne.

WEITERE ERGEBNISSE
13. Aufstellung als Arbeitsmittel, Tabelle mit den Spalten:
    Nr. | Ortskennung | Gemeinde | Betriebsstätte ja/nein | Zeitraum im
    Erhebungszeitraum | anzuwendender Maßstab | Belegquelle | offener Punkt.
14. Rückfrageliste an den Mandanten, Tabelle mit den Spalten:
    Nr. | Fehlende Angabe oder Unterlage | Wofür sie gebraucht wird |
    Antwort (leer).
15. Prüfvermerk für die Akte, höchstens 250 Wörter: geprüfte Orte,
    Ergebnisraster, gewählter Maßstab mit Begründung, Abweichungen zur
    bisherigen Erklärung, offene Punkte, benannte Fristarten.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben je Ort einzeln. Fehlt die Angabe zur Verfügungsmacht, entscheide
   den Betriebsstättenbegriff NICHT, sondern fordere sie an.
2. Nenne zu jedem Schritt die Rechtsgrundlage POSITIV, also Norm mit Absatz,
   Satz und Nummer, Richtlinie oder Erlass mit Datum oder Entscheidung mit
   Datum und Aktenzeichen, jeweils mit dem Zusatz "für [JAHR] verifizieren".
   Erfinde keine Paragrafen und keine Aktenzeichen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
3. Berechne KEINEN Zerlegungsanteil, KEINE Quote, KEINEN Messbetrag und KEINEN
   Steuerbetrag. Stelle die Rechengrößen und den Rechenweg so dar, dass ein
   Mensch rechnet.
4. Nenne KEINEN Hebesatz, KEINE Betragsgrenze, KEINE Verhältniszahl und KEINE
   Rundungsregel als feststehenden Wert, sondern nur als nachzuschlagende
   Größe mit dem Zusatz "für [JAHR] verifizieren".
5. Berechne KEINE Fristen. Liste auf, WELCHE Fristen im Raum stehen, je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   ohne Dauer.
6. Formuliere jede Aussage zur Unbilligkeit, zur Zuordnung eines Arbeitnehmers
   und zur Verfügungsmacht ausdrücklich als Vermutung, solange sie nicht aus
   den gelieferten Angaben folgt.
7. ABBRUCHREGEL: Benennen die Angaben ausdrücklich eine erwogene Selbstanzeige,
   ein laufendes Steuerstrafverfahren oder ein Organisationsversagen der
   Kanzlei, arbeite für diesen Erhebungszeitraum NICHT weiter. Gib für ihn nur
   aus: "Anzeichen für einen Berichtigungs- oder Strafsachverhalt – Bearbeitung
   an dieser Stelle abgebrochen, Prüfung durch einen Berufsträger außerhalb des
   KI-Werkzeugs." Eine fehlende oder unrichtige Betriebsstättenaufstellung eines
   abgelaufenen Erhebungszeitraums ist KEIN Abbruchgrund; behandle sie über die
   Änderung und Nachholung der Zerlegung nach § 189 AO
   (für [JAHR] verifizieren) und vermerke: "Ob daneben eine Berichtigung nach
   § 153 AO zu prüfen ist, entscheidet der Berufsträger." Die übrigen
   Erhebungszeiträume bearbeitest du weiter und sagst ausdrücklich, welche du
   ausgesteuert hast.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Betriebsstättenprüfung je Ort, Schritt 1
3. Gemeindeabgleich, Schritt 2, mit Ergebnisraster nach Schritt 12
4. Maßstab: Regelfall, Sonderfälle, mehrgemeindliche Betriebsstätte,
   abweichender Maßstab
5. Kleinbeträge, Unterbleiben der Zerlegung und Abgrenzung zur Zuteilung
   (§ 34 GewStG, § 190 AO), Betragsgrenze nur als nachzuschlagende Größe
6. Prüfung der Arbeitslohnherleitung mit beanstandeten Positionen
7. Verfahren, Bescheide und Rechtsbehelfslage
8. Fristarten mit Rechtsgrundlage
9. Aufstellung als Arbeitsmittel
10. Rückfrageliste
11. Prüfvermerk
12. Interne Notiz
13. Was ich nicht sicher weiß
```

## Anwendung

1. Vor dem Prompt die Standortliste unabhängig von der Vorjahreserklärung neu aufnehmen – aus Mietverträgen, Kostenstellen und der Lohnbuchführung. Die Fortschreibung des Vorjahres ist die häufigste Fehlerquelle, weil sie geschlossene und neu eröffnete Betriebsstätten mitschleppt.
2. Die Arbeitslöhne je Betriebsstätte mit Herleitung liefern, nicht nur als Summe. Der Prompt prüft die Zusammensetzung; ohne Herleitung kann er nur die Vollständigkeit der Gemeinden beurteilen.
3. Bei Wind-, Solar- und Energiespeicheranlagen zusätzlich das Sachanlagevermögen je Anlage bereitstellen und den Standort gemeindescharf angeben. Der abweichende Maßstab läuft ohne diese Angaben leer.
4. Bei einer Betriebsstätte, die sich über mehrere Gemeinden erstreckt, die Gemeindelasten vorab erheben. Ohne sie ist der Maßstab des § 30 GewStG nicht anwendbar, und der Prompt wird den Punkt zu Recht als nicht entscheidbar ausweisen.
5. Zerlegungsanteile im Fachprogramm rechnen, nicht im KI-Werkzeug. Das Ergebnis des Prompts ist die Grundlage für die Erfassung, nicht die Erfassung selbst.
6. Rechtsbehelfsfristen aus dem Bescheid ablesen, im Fristenprogramm erfassen und die Erfassung von einer zweiten Person nachprüfen lassen.

## Qualitätssicherung

- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt die Betriebsstättenliste, den Gemeindeabgleich und die Arbeitslohnherleitung gegen die Belegquellen nach. Die Zerlegungserklärung, jeder Einspruch und jede Stellungnahme gegenüber einer Gemeinde oder dem Finanzamt wird von einem Berufsträger freigegeben; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **§ 32 GewStG ist weggefallen.** Eine Antwort, die ihn zitiert, ist zu verwerfen – ebenso jede Antwort, die die Zerlegungserklärung in den §§ 28 ff. GewStG statt in § 14a GewStG verortet.
- **Keine Änderung der Zerlegungsvorschriften durch das Neunte Gesetz zur Änderung von Vorschriften im Steuerberatungsrecht sowie im Steuerrecht.** Geändert wurden nur § 16 Abs. 4 Satz 2 GewStG (Mindesthebesatz, erstmals für den Erhebungszeitraum 2027 – für [JAHR] verifizieren) und § 36 GewStG. Eine Antwort, die daraus eine Neuerung bei den §§ 28 bis 34 GewStG ableitet, ist falsch.
- **Der Betriebsstättenbegriff steht vor dem Maßstab.** Wer zuerst die Arbeitslöhne verteilt und danach fragt, ob überhaupt eine Betriebsstätte besteht, verteilt auf Orte, die nicht beteiligt sind.
- **Eine einzige Betriebsstätte schließt die Zerlegung nicht aus.** § 28 Abs. 1 Satz 2 GewStG erfasst auch die Betriebsstätte, die sich über mehrere Gemeinden erstreckt, und die Verlegung innerhalb des Erhebungszeitraums (§ 28 Abs. 1 GewStG – für [JAHR] verifizieren). Beide Fälle werden erst nach dem Gemeindeabgleich und der Prüfung der mehrgemeindlichen Betriebsstätte entschieden, nicht schon bei der Standortliste.
- **Eine übersehene Gemeinde erledigt sich nicht.** § 189 AO erlaubt die Änderung und Nachholung der Zerlegung; eine fehlende Gemeinde ist deshalb kein abgeschlossener Vorgang, sondern ein offener.
- **Einwendungen gegen die Höhe des Messbetrags gehören nicht in das Zerlegungsverfahren.** Der Messbescheid ist Grundlagenbescheid; wer ihn im Einspruch gegen den Zerlegungsbescheid angreift, verliert beide Verfahren.
- **Verhältniszahlen und Betragsgrenzen werden nachgeschlagen, nicht erinnert.** Kein Prozentsatz und kein Bruchteil aus der KI-Antwort in die Erklärung übernehmen.
- **Rechtsstand prüfen an:** §§ 14a, 16, 28, 29, 30, 31, 33, 34 und 36 GewStG sowie §§ 12, 153, 185 bis 190, 347 und 360 AO im amtlichen Volltext (gesetze-im-internet.de), den Gewerbesteuer-Richtlinien und -Hinweisen zur Zerlegung, dem Neunten Gesetz zur Änderung von Vorschriften im Steuerberatungsrecht sowie im Steuerrecht im Bundesgesetzblatt sowie DATEV LEXinform. Alle Angaben am Original nachlesen (Stand – für [JAHR] verifizieren).

## Varianten

- **Nur Gemeindeabgleich:** „Beschränke dich auf die Schritte 1, 2 und 12 und erzeuge ausschließlich die Aufstellung und die Rückfrageliste."
- **Wind- und Solaranlagen:** „Vertiefe Schritt 6, behandle je Anlage Standort, Inbetriebnahme und Sachanlagevermögen einzeln und benenne, welche Angaben für den zusammengesetzten Maßstab fehlen."
- **Mehrgemeindliche Betriebsstätte:** „Beschränke dich auf § 30 GewStG, benenne die zu erhebenden Gemeindelasten als Erhebungsauftrag und erzeuge einen Erfassungsbogen für die Lasten."
- **Streit mit einer Gemeinde:** „Beurteile die vorgetragenen Einwendungen der Gemeinde Punkt für Punkt, ordne jeden Einwand einer Norm zu und erzeuge eine Gliederung für die Stellungnahme – ohne Fristangabe und ohne Beträge." Ergänzt den Rechtsbehelfsteil.
- **Vorausschau bei neuem Standort:** „Beurteile einen geplanten Standort vorab: Wann entsteht dort eine Betriebsstätte, ab welchem Zeitpunkt ist die Gemeinde zu beteiligen und welche Angaben sind ab Eröffnung laufend zu erfassen."
