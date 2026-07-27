# 31 – Fristverlängerungsantrag entwerfen

**Problem:** Fristverlängerungsanträge werden unter Zeitdruck mit derselben Standardfloskel gestellt; das Finanzamt lehnt zunehmend ab, und die Kanzlei merkt es zu spät.
**Rolle:** Sekretariat, Sachbearbeitung, Steuerberater (Freigabe)
**DATEV-Bezug:** DATEV Fristenkontrolle / Fristen und Bescheide, DATEV DMS, Schriftverkehr über Kanzlei-Rechnungswesen bzw. Eigenorganisation
**Was du bereitstellen musst:** Steuerart, Veranlagungszeitraum, aktuell notierte Frist mit Herkunft (Gesetz, Verfügung, Vorabanforderung), bisherige Verlängerungen, konkreter Grund, gewünschtes neues Datum.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Steuernummer und Aktenzeichen durch Platzhalter ersetzen (`Mandant A`, `Steuernummer ****`). Für den Entwurf genügen Steuerart, Zeitraum, Datumsangaben und der Sachgrund. Namen von Mitarbeitern oder erkrankten Personen nicht einfügen. Krankheitsbedingte Ausfälle nur neutral als "krankheitsbedingter Ausfall in der Bearbeitung" – ohne Person, ohne Diagnose, ohne Dauer. Die konkreten Angaben setzt die Kanzlei erst in der Reinschrift ein. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist erfahrene Kanzleimitarbeiterin in einer deutschen Steuerkanzlei und
schreibst Anträge an das Finanzamt. Dein Stil: sachlich, kurz, ohne Floskeln,
ohne Rechtfertigungston, mit einem konkreten Datum als Antrag.

AUFGABE
Entwirf einen Antrag auf Verlängerung der Abgabefrist an das Finanzamt.

VORGANG
- Steuerart(en): [z. B. EINKOMMENSTEUER / KÖRPERSCHAFTSTEUER / GEWERBESTEUER /
  UMSATZSTEUER-JAHRESERKLÄRUNG / FESTSTELLUNG]
- Veranlagungszeitraum: [JAHR]
- Bisher notierte Frist: [DATUM]
- Herkunft dieser Frist: [gesetzliche Abgabefrist / allgemeine Verfügung /
  Einzelanordnung des Finanzamts / VORABANFORDERUNG / unklar]
- Bereits verlängert: [nein / ja, bis DATUM, Anzahl: ZAHL]
- Frist bereits abgelaufen: [nein / ja, seit DATUM]
- Grund: [ARBEITSÜBERLASTUNG DER KANZLEI mit konkretem Auslöser /
  FEHLENDE UNTERLAGEN DES MANDANTEN mit Bezeichnung der Unterlagen /
  BESONDERE UMSTÄNDE, z. B. Erbfall, Betriebsprüfung, Systemumstellung]
- Konkretisierung des Grundes: [WAS GENAU FEHLT ODER WAS EINGETRETEN IST]
- Gewünschtes neues Datum: [DATUM]
- Was die Kanzlei bis dahin erledigt hat / erledigen wird: [ANGABE]

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab: Reichen die Angaben für
   einen tragfähigen Antrag? Benenne fehlende Angaben, statt sie zu erfinden.
2. Die Begründung muss sachlich und konkret sein. Verwende KEINE
   Standardformel wie "wegen Arbeitsüberlastung". Benenne den Auslöser, den
   Umfang und warum er gerade diesen Fall betrifft. Wenn der gelieferte Grund
   inhaltsleer ist, sage das und fordere eine Konkretisierung an.
3. Nenne KEINE gesetzlichen Fristen, Fristlängen oder Verlängerungszeiträume
   als feststehend. Jede Datums- oder Fristaussage, die nicht aus meinen
   Angaben stammt, kennzeichnest du als "für [JAHR] verifizieren".
4. Berechne KEINE Fristen. Fristberechnung erfolgt durch einen Menschen.
   Übernimm Datumsangaben ausschließlich so, wie ich sie geliefert habe.
5. Wenn als Herkunft "Vorabanforderung" angegeben ist oder die Angaben darauf
   hindeuten: Behandle das gesondert in einem eigenen Abschnitt. Weise darauf
   hin, dass für eine Vorabanforderung andere Voraussetzungen gelten und der
   Antrag deshalb nicht mit einem Standardantrag gleichgesetzt werden darf.
   Formuliere hier keinen Antragstext ohne ausdrückliche Freigabe.
5a. Ist die Frist nach meinen Angaben bereits abgelaufen, behandle als
    vorrangiges Instrument die RÜCKWIRKENDE Fristverlängerung und nenne dazu die
    Rechtsgrundlage (§ 109 Abs. 1 Satz 2 AO – für [JAHR] verifizieren). Weise
    gesondert darauf hin, dass eine rückwirkende Verlängerung nach
    § 152 Abs. 3 Nr. 1 AO den Verspätungszuschlag ausschließen kann (für [JAHR]
    verifizieren). Die Wiedereinsetzung (§ 110 AO) erwähnst du nur als davon zu
    unterscheidenden, gesondert zu prüfenden Weg, nicht als Regelfall. Ist als
    Herkunft die Frist nach § 149 Abs. 3 AO angegeben (beratene Fälle), weise auf
    die Beschränkung des § 109 Abs. 2 AO hin – dort trägt "Arbeitsüberlastung"
    als Begründung gerade nicht (für [JAHR] verifizieren).
6. Nenne zu jedem Prüfungsschritt die einschlägige Rechtsgrundlage, jeweils mit
   dem Zusatz "für [JAHR] verifizieren", und führe sie am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit Spalte "geprüft von (leer)".
   Mindestens zu nennen, soweit im Fall berührt: § 109 Abs. 1 Satz 2 AO,
   § 109 Abs. 2 AO, § 149 Abs. 3 AO, § 152 Abs. 3 Nr. 1 AO, § 110 AO,
   § 347 AO. Bist du dir einer Fundstelle nicht sicher, schreibe
   "Fundstelle offen – bitte recherchieren" statt einer Angabe.
7. Kein Schuldeingeständnis, keine Zusage, die die Kanzlei nicht halten kann.

AUSGABEFORMAT
1. (Antrag) – Betreffzeile, Antragssatz mit dem gewünschten Datum,
   Begründung in höchstens 6 Sätzen, Schlusssatz.
2. (Variante bei bereits abgelaufener Frist) – nur wenn oben "ja" angegeben
   ist: abweichender Entwurf, gerichtet auf die rückwirkende Fristverlängerung
   nach § 109 Abs. 1 Satz 2 AO (für [JAHR] verifizieren). Der Hinweis auf eine
   mögliche Wiedereinsetzung (§ 110 AO) steht als GETRENNTER Punkt darunter,
   nicht im Antragstext, und ist als "durch Berufsträger zu prüfen"
   gekennzeichnet.
3. (Fehlende Angaben) – was ich nachliefern muss.
4. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | wofür sie im Entwurf steht | geprüft von (leer)
5. (Interne Notiz) – nicht an das Finanzamt: Einschätzung der Erfolgsaussicht,
   Wiedervorlage-Vorschlag, Hinweis auf offene Zulieferung des Mandanten.
```

## Anwendung

1. Herkunft der Frist ehrlich eintragen. "Unklar" ist eine zulässige Antwort und besser als eine geratene.
2. Den Grund vor dem Einfügen konkretisieren: welche Unterlagen fehlen, seit wann, was bereits angemahnt wurde.
3. Antrag mit den Fristen in der DATEV-Fristenüberwachung abgleichen, bevor er das Haus verlässt.
4. Datum des Antrags, Sachbearbeiter und Wiedervorlage sofort im Fristenprogramm eintragen – der Entwurf ersetzt keinen Eintrag.

## Qualitätssicherung

- **Vier-Augen-Prinzip: Die Frist wird von einer Person berechnet und im Fristenprogramm erfasst und von einer zweiten Person anhand des Ausgangsdokuments nachgeprüft und abgezeichnet** – bei Rechtsbehelfsfristen ausnahmslos, unabhängig davon, ob ein Rechtsbehelf geplant ist. Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Fristen werden von einem Menschen berechnet und geprüft.** Kein Datum aus dem Modell übernehmen, ohne es gegen die Akte und das Fristenprogramm zu prüfen.
- **Freigabe durch einen Berufsträger** vor dem Versand – der Antrag hat Rechtsfolgen.
- **Bei abgelaufener Frist zuerst prüfen, ob eine rückwirkende Verlängerung nach § 109 Abs. 1 Satz 2 AO beantragt wird** – sie kann den Verspätungszuschlag nach § 152 Abs. 3 Nr. 1 AO vermeiden. Erst danach und getrennt davon prüft ein Berufsträger die Wiedereinsetzung.
- **Wiedereinsetzung (§ 110 AO) hat eine eigene, kurze Antragsfrist (Monatsfrist ab Wegfall des Hindernisses, § 110 Abs. 2 AO – für [JAHR] verifizieren) und setzt voraus, dass die versäumte Handlung innerhalb dieser Frist nachgeholt wird.** Diese Frist wird sofort und gesondert im Fristenprogramm erfasst. Beachte § 110 Abs. 1 Satz 2 AO: Verschulden der Kanzlei wird dem Mandanten zugerechnet. Deutet die Ursache auf ein Organisationsversagen der Kanzlei hin, ist der Vorgang **kein Antragsfall, sondern ein Haftungsfall** – Vorgehen nach dem Notfallteil des Fristenkonzepts (Prompt 35), Berufsträger unverzüglich einschalten.
- Prüfen, ob die Begründung im Wiederholungsfall noch trägt. Dieselbe Begründung zum dritten Mal ist ein Ablehnungsgrund.
- Aussagen zu Fristlängen und Verlängerungspraxis am aktuellen Rechtsstand verifizieren.

## Varianten

- **Sammelantrag:** "Erzeuge einen Antrag für mehrere Mandate desselben Sachgrunds, mit Anlage als Tabelle: Mandat | Steuerart | Zeitraum | bisherige Frist | beantragtes Datum."
- **Erinnerung an den Mandanten:** "Erzeuge zusätzlich ein kurzes Schreiben an den Mandanten, das die noch fehlenden Unterlagen benennt und die Folgen einer weiteren Verzögerung sachlich beschreibt."
- **Nach Ablehnung:** "Formuliere eine kurze Reaktion auf die Ablehnung – ohne eigene Fristberechnung. Weise gesondert darauf hin, dass die Ablehnung ein anfechtbarer Verwaltungsakt ist (§ 347 AO – für [JAHR] verifizieren), dass dafür eine eigene Frist läuft und dass diese sofort von einem Menschen berechnet und im Fristenprogramm erfasst wird."
