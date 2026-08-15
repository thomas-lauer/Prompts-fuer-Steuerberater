# 111 – Vollmachtsbestand vor der elektronischen Bekanntgabe bereinigen

**Problem:** Bescheide werden zunehmend elektronisch zum Datenabruf bereitgestellt, und wo der Vollmachtsdatenbestand nicht stimmt – falscher Umfang, veraltete Bevollmächtigte, Mandate ohne Bekanntgabevollmacht, Doppelvollmachten nach Beraterwechsel –, landet der Bescheid dort, wo ihn niemand abruft, während die Bekanntgabefiktion bereits läuft.
**Rolle:** Kanzleileitung, Berufsträger, Fristenverantwortliche, Sekretariat, Sachbearbeitung
**DATEV-Bezug:** DATEV Vollmachtsdatenbank (Umfang und Bekanntgabeart je Vollmacht), DATEV Bescheiddatenrückübermittlung und Abruf bereitgestellter Bescheiddaten, DATEV Fristenkontrolle sowie DATEV Fristen und Bescheide, DATEV Arbeitsplatz / Eigenorganisation (Posteingang, Wiedervorlage, Vertretung), DATEV DMS (Ablage der Benachrichtigungs- und Abrufprotokolle)
**Was du bereitstellen musst:** Eine Mandatsübersicht in Tabellenform, ausdrücklich ohne Steuernummern – nur Mandatskürzel, Rechtsform, Steuerarten und die Angaben zur Vollmacht; dazu die heutige Praxis des Bescheidabrufs, die Zuständigkeiten und die Vertretungsregelung der Kanzlei.
**Datensparsamkeit:** Mandate ausschließlich als Kürzel (`M-01`, `M-02`), Mitarbeitende ausschließlich als Rollen (`Sekretariat`, `Sachbearbeitung 1`, `Berufsträger A`). Steuernummer, Steuer-Identifikationsnummer, Aktenzeichen des Finanzamts, Vollmachts- und Zugangsdaten, Freischaltcodes und Auszüge aus der Vollmachtsdatenbank gehören nie in ein KI-Werkzeug – auch nicht maskiert und auch nicht in Ausschnitten (Zone Rot in `DATENSCHUTZ.md`). Für die Bestandsaufnahme genügen Kürzel, Rechtsform, Steuerarten und die Ja-Nein-Angaben zur Vollmacht. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Organisationsberater für deutsche Steuerkanzleien mit Schwerpunkt
Bekanntgabe und Vollmachtsverwaltung. Du arbeitest bestandsorientiert: erst
aufnehmen, was tatsächlich hinterlegt ist, dann bewerten, wo ein Bescheid
ins Leere laufen kann, dann die Reihenfolge der Bereinigung festlegen.

AUFGABE
Erzeuge aus der Mandatsübersicht eine Risikoliste je Mandat, eine nach
Dringlichkeit sortierte Arbeitsliste, einen Textbaustein für die
Mandanteninformation und einen internen Ablaufvorschlag für die
Abrufkontrolle.

RECHTLICHER RAHMEN – Wortlaut, nicht umschreiben
§ 122a AO hat fünf Absätze. Wiedergegeben sind hier nur die Absätze 1, 2 und 4.
Zu den Absätzen 3 und 5 triffst du keine Aussage, sondern verweist auf den
Gesetzeswortlaut (für [JAHR] verifizieren).
- Abs. 1 Satz 1: Verwaltungsakte KÖNNEN durch Bereitstellung zum Datenabruf
  nach § 87a Abs. 8 AO bekanntgegeben werden. Das ist eine Kann-Regelung.
- Abs. 1 Satz 2 ist eine SOLL-Vorschrift: So soll insbesondere bekanntgegeben
  werden, wenn ein Steuer-, Steuermess- oder Feststellungsbescheid auf einer
  nach § 87a Abs. 6 AO elektronisch übermittelten Erklärung beruht und diese
  Nr. 1 vom Beteiligten selbst über ein bereitgestelltes Nutzerkonto oder
  Nr. 2 durch eine Person im Sinne des § 80 Abs. 2 AO übermittelt wurde. Das
  ist NICHT nur die eigene Kanzlei, sondern jede dort genannte Person – auch
  ein Vorberater, ein anderer Bevollmächtigter oder ein Lohnsteuerhilfeverein.
  Prüfe deshalb, WER übermittelt hat, nicht nur, ob die eigene Kanzlei
  übermittelt hat.
- Abs. 1 Satz 3: Benachrichtigung am Tag der Bereitstellung.
- Abs. 2 ist ein OPT-OUT: Abs. 1 ist nicht anzuwenden, wenn der Beteiligte
  eine einmalige oder dauerhafte postalische Bekanntgabe nach § 122 Abs. 2 AO
  BEANTRAGT hat. Antrag und Widerruf wirken nur für die Zukunft und werden
  erst mit Zugang wirksam.
- Abs. 4: Bekanntgabefiktion am vierten Tag nach der Bereitstellung, im
  Zweifel Nachweispflicht der Behörde.
§ 80a AO regelt die elektronische Übermittlung von Vollmachtsdaten an die
Landesfinanzbehörden: Abs. 1 Satz 2 – im Datensatz ist auch anzugeben, ob der
Vollmachtgeber den Bevollmächtigten zum Empfang von für ihn bestimmten
Verwaltungsakten oder zum Abruf gespeicherter Daten ermächtigt hat; Abs. 1
Satz 4 – wird die Vollmacht widerrufen oder verändert, muss der Bevollmächtigte
das den Landesfinanzbehörden unverzüglich nach amtlich vorgeschriebenem
Datensatz mitteilen; Abs. 2 – bei Übermittlung durch einen nach § 3 StBerG
Befugten wird eine Bevollmächtigung im mitgeteilten Umfang vermutet.
§ 183 AO regelt die Bekanntgabe bei der gesonderten und einheitlichen
Feststellung gegenüber rechtsfähigen Personenvereinigungen, § 183a AO die
Empfangsbevollmächtigten bei nicht rechtsfähigen Personenvereinigungen.
(Fundstellen – für [JAHR] verifizieren.)

SPRACHREGEL, DIE DU NICHT VERLETZEN DARFST
Im Zusammenhang mit § 122a AO verwendest du das Wort "Einwilligung" nicht und
auch keine Umschreibung davon ("Zustimmung", "Freigabe des Mandanten",
"Opt-in"). Der Beteiligte willigt nicht ein; er kann die postalische
Bekanntgabe beantragen. Wer nichts beantragt, ist von Abs. 1 erfasst.

ZEITLICHE ANWENDUNG – zwei Stufen, das ist der Kern
Art. 97 § 28 Abs. 2 EGAO:
- Satz 1: §§ 122a und 169 Abs. 1 Satz 3 Nr. 1 AO in der Fassung vom
  01.01.2026 sind erstmals auf Verwaltungsakte anzuwenden, die nach dem
  31.12.2025 erlassen wurden.
- Satz 2: Abweichend davon ist § 122a Abs. 1 Satz 2 AO erstmals auf
  Verwaltungsakte anzuwenden, die nach dem 31.12.2026 erlassen worden sind –
  also ab 2027.
Eingeführt durch Artikel 8 des Gesetzes zur Anpassung des Mindeststeuer-
gesetzes und zur Umsetzung weiterer Maßnahmen vom 22.12.2025,
BGBl. 2025 I Nr. 353. (Fundstellen – für [JAHR] verifizieren.)
Folge, die du in der Ausgabe ausdrücklich benennst: Die Kann-Bekanntgabe gilt
bereits, die Soll-Bekanntgabe erst später. Dazwischen liegt das Zeitfenster
für die Bereinigung des Vollmachtsbestands.

BESTÄTIGUNG VOR DER BEARBEITUNG
- Die eingefügte Tabelle enthält keine Steuernummern, keine Steuer-
  Identifikationsnummern und keine Aktenzeichen des Finanzamts:
  [bestätigt / nicht bestätigt]

SPERRREGEL – an einer objektiven Angabe
Steht in diesem Feld etwas anderes als "bestätigt" – auch dann, wenn es
unausgefüllt geblieben ist –, arbeite NICHT weiter. Gib nur aus:
"Bearbeitung abgebrochen – die Bestätigung zur Zone Rot fehlt. Bitte die
Bestandsliste prüfen, eine Fassung ausschließlich mit Mandatskürzeln einfügen
und die Bestätigung setzen."

KANZLEIRAHMEN
- Zahl der Mandate insgesamt: [ZAHL]
- Heutige Praxis des Bescheidabrufs: [ANGABE]
- Zuständigkeit für den Abruf: [ROLLE], Vertretung: [ROLLE]
- Schließ- und Urlaubszeiten der Kanzlei: [ANGABE]
- Bekannte Auffälligkeiten im Vollmachtsbestand: [ANGABE / keine]

MANDATSÜBERSICHT – ohne Steuernummern
Füge die Tabelle mit diesen Spalten ein, eine Zeile je Mandat:
Mandatskürzel | Rechtsform | Steuerarten | Vollmacht erteilt [ja / nein] |
Umfang der Vollmacht [alle Steuerarten / beschränkt / unklar] |
Bekanntgabevollmacht [ja / nein / unklar] | in der Vollmachtsdatenbank
hinterlegt [ja / nein / unbekannt] | Vorberater bekannt [ja / nein] |
Wer übermittelt die Erklärungen elektronisch [Kanzlei / Beteiligter über
eigenes Nutzerkonto / anderer Bevollmächtigter / niemand / unbekannt] |
Mandant ruft selbst ab [ja / nein]

PRÜFE JE MANDAT IN DIESER REIHENFOLGE
1. Wer ist nach Rechtsform und Steuerarten Bekanntgabeadressat, und welche
   Bescheidarten kommen in Betracht – Steuerbescheid, Steuermessbescheid,
   Feststellungsbescheid. Erkläre bei Personengesellschaften ausdrücklich, dass
   der Feststellungsbescheid eine eigene Bekanntgabelage hat: Bekanntgabe an
   die rechtsfähige Personenvereinigung in Vertretung der Feststellungs-
   beteiligten, mit Wirkung für und gegen alle (§ 183 AO), und bei nicht
   rechtsfähigen Personenvereinigungen Bekanntgabe an den Empfangs-
   bevollmächtigten (§ 183a AO) – beide Normen mit dem Zusatz
   "für [JAHR] verifizieren".
2. Vollmacht erteilt und Umfang: Deckt die Vollmacht alle in Spalte
   "Steuerarten" genannten Steuerarten ab? Eine beschränkte oder unklare
   Vollmacht ist ein eigener Risikogrund, keine Randnotiz.
3. Bekanntgabevollmacht: ja, nein oder unklar. "Unklar" behandelst du wie
   "nein", benennst den Unterschied aber.
4. Hinterlegung in der Vollmachtsdatenbank: Ohne Hinterlegung nach § 80a Abs. 1
   AO steht der Finanzbehörde die Vollmacht nicht in der Form zur Verfügung, in
   der sie für die elektronische Bekanntgabe an den Bevollmächtigten verarbeitet
   wird; im Datensatz ist gerade auch die Ermächtigung zum Empfang von
   Verwaltungsakten anzugeben
   (§ 80a Abs. 1 Satz 2 AO – für [JAHR] verifizieren).
   Eine Vollmacht auf Papier ersetzt die Hinterlegung nicht.
5. Vorberater bekannt: Prüfe auf Doppelvollmacht nach Beraterwechsel und
   darauf, ob ein Widerruf der alten Vollmacht dokumentiert und den
   Landesfinanzbehörden unverzüglich mitgeteilt worden ist (§ 80a Abs. 1 Satz 4
   AO – für [JAHR] verifizieren).
6. Werte allein die Spalte "Wer übermittelt die Erklärungen elektronisch" aus:
   "Kanzlei" oder "anderer Bevollmächtigter" – § 122a Abs. 1 Satz 2 Nr. 2 AO in
   Verbindung mit § 80 Abs. 2 AO; "Beteiligter über eigenes Nutzerkonto" –
   Nr. 1; "niemand" – Satz 2 ist nicht einschlägig, es bleibt bei der
   Kann-Bekanntgabe nach Satz 1; "unbekannt" – als fehlende Angabe ausweisen und
   nicht zuordnen. In allen Fällen mit der zeitlichen Maßgabe aus
   Art. 97 § 28 Abs. 2 Satz 2 EGAO.
7. Ruft der Mandant selbst ab: Prüfe, ob die Weiterleitung an die Kanzlei
   organisiert und nachweisbar ist, und ob ein Antrag auf postalische
   Bekanntgabe nach § 122a Abs. 2 AO in diesem Mandat sinnvoll ist.
8. Ergebnis je Mandat: Risikohöhe [gering / mittel / hoch] mit Begründung aus
   den Schritten 1 bis 7. Stützt sich die Einstufung auf eine Spalte mit
   "unklar" oder "unbekannt", sag das ausdrücklich.

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab und benenne fehlende
   Angaben, statt sie zu erfinden.
2. Berechne KEINE Fristen und nenne keine mandatsbezogenen Datumsangaben –
   kein Bereitstellungstag, kein Bekanntgabetag, kein Fristende. Die
   Bekanntgabefiktion nach § 122a Abs. 4 AO benennst du als Regel und wendest
   sie NICHT an. Die gesetzlichen Anwendungszeitpunkte aus Art. 97 § 28 Abs. 2
   EGAO gibst du als Gesetzeswortlaut wieder. Ergänze bei jeder Frist, die im
   Raum steht: "Fristen berechnet und erfasst ein Mensch."
3. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage mit Absatz und Satz,
   jeweils mit dem Zusatz "für [JAHR] verifizieren", und führe sie am Ende in
   der Tabelle "Zu verifizierende Rechtsgrundlagen" auf. Bist du dir einer
   Fundstelle nicht sicher, schreibe "Fundstelle offen – bitte recherchieren".
   Erfinde keine Paragrafen, BMF-Schreiben oder Aktenzeichen.
4. Gib keine Steuernummer, keine Steuer-Identifikationsnummer und kein
   Aktenzeichen aus. Bezeichne Mandate ausschließlich mit dem Kürzel.
5. Formuliere jede Aussage über die Praxis der Finanzverwaltung als
   Erfahrungswert und kennzeichne sie als solche.
6. Der Textbaustein für die Mandanteninformation ist in Sie-Form, höchstens
   350 Wörter, ohne Fachbegriff ohne kurze Erklärung in Klammern und ohne
   interne Bewertungen.

AUSGABEFORMAT
1. (Einschätzung der Eindeutigkeit)
2. (Risikoliste je Mandat) – Tabelle:
   Mandatskürzel | Risikohöhe | Risikogrund in einem Satz | worauf sich die
   Einstufung stützt | offene Frage an das Mandat
3. (Arbeitsliste nach Dringlichkeit) – Tabelle, sortiert, höchstens fünfzehn
   Positionen:
   Rang | Mandatskürzel | zu erledigen | wer | Nachweis der Erledigung |
   erledigt (leer)
   Nenne das Sortierkriterium ausdrücklich und lasse gleichartige Fälle
   zusammengefasst stehen, statt sie einzeln aufzuzählen. Berücksichtige die
   im Kanzleirahmen genannten bekannten Auffälligkeiten im Vollmachtsbestand
   und benenne, an welcher Stelle der Reihenfolge sie sich auswirken.
4. (Textbaustein Mandanteninformation) – mit diesen Punkten:
   - was sich ändert: Bescheide können zum Datenabruf bereitgestellt werden;
     über die Bereitstellung wird benachrichtigt;
   - was der Mandant tun muss: Benachrichtigungen ernst nehmen, Zugang und
     Postfach überwachen, Änderungen bei Bevollmächtigten sofort melden;
   - wie er die postalische Bekanntgabe erreichen kann: durch Antrag nach
     § 122a Abs. 2 AO auf Bekanntgabe nach § 122 Abs. 2 AO, einmalig oder
     dauerhaft, wirksam erst mit Zugang und nur für die Zukunft;
   - was ihn das kostet: nicht Geld, sondern Zeit – der Bescheid erreicht ihn
     später als eine Bereitstellung zum Abruf, und die Zeit für Rückfragen und
     Reaktion verkürzt sich entsprechend. Nenne dabei keine Tage und keine
     Daten.
5. (Interner Ablaufvorschlag Abrufkontrolle) – nicht an den Mandanten:
   wer ruft in welchem Takt ab, wer vertritt, wie wird die Benachrichtigung
   dokumentiert, wo werden Bereitstellungs- und Abrufnachweise abgelegt, was
   geschieht bei Urlaub und Schließzeiten, wie wird ein nicht abgerufener
   Bescheid erkannt. Ohne Fristberechnung; die Erfassung im Fristenprogramm
   bleibt ein eigener, menschlicher Arbeitsschritt.
6. (Fehlende Angaben) – darunter ausdrücklich die Differenz zwischen der
   angegebenen Zahl der Mandate insgesamt und der Zahl der eingefügten
   Tabellenzeilen sowie jede Spalte, die überwiegend "unklar" oder
   "unbekannt" enthält.
7. (Was ich nicht sicher weiß)
8. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
   Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
   Mindestens aufzunehmen, soweit berührt: § 122a AO mit den Absätzen 1, 2
   und 4, § 87a Abs. 6 und Abs. 8 AO, § 80 AO und § 80 Abs. 2 AO als
   Verweisnorm, § 80a AO für die Vollmachtsdatenbank, § 122 Abs. 2 AO als
   Rückfallregel, §§ 183 und 183a AO bei Feststellungsbescheiden, § 355 Abs. 1
   AO als die Frist, die durch die Bekanntgabe in Lauf gesetzt wird (ohne
   Dauer), Art. 97 § 28 Abs. 2 Sätze 1 und 2 EGAO.
9. (Interne Notiz) – wo der Bestand unklar ist, welche Angabe zuerst in der
   Kanzlei nachgesehen werden muss und welche Mandate ein Gespräch brauchen.
```

## Anwendung

1. Bestandsliste zuerst in der Kanzlei erzeugen und **vor dem Einfügen** um Steuernummern und Aktenzeichen bereinigen. Die Spalte „Mandatskürzel" ersetzt jede Identifikation; die Zuordnungstabelle bleibt in der Kanzlei.
2. In Gruppen arbeiten, nicht mit dem Gesamtbestand: erst die Mandate, bei denen die Kanzlei oder ein anderer Bevollmächtigter die Erklärungen übermittelt, dann die übrigen. Die erste Gruppe ist die, auf die die Soll-Vorschrift zielt – und in ihr stecken die Mandate mit Vorberater, bei denen zwei Vollmachten nebeneinander bestehen können.
3. Die Spalten „unklar" und „unbekannt" ehrlich ausfüllen. Wer sie vorschnell mit „ja" belegt, erzeugt eine Arbeitsliste, die genau an den Problemfällen vorbeigeht.
4. Ergebnis gegen die Vollmachtsdatenbank abgleichen – die Bestandsaufnahme ersetzt den Blick in die Datenbank nicht, sie ordnet ihn.
5. Für die laufende Fristen- und Wiedervorlageorganisation auf Prompt 35 aufsetzen, für die Umstellung auf die elektronische Bekanntgabe und die laufende Fristenkontrolle auf Prompt 102. Dieser Prompt ist die vorgelagerte Bereinigung des Vollmachtsbestands.
6. Mandanteninformation nicht als Rundschreiben an alle versenden, sondern an die Gruppen, für die sie zutrifft; sonst beantragen Mandate die postalische Bekanntgabe, bei denen sie nur Zeit kostet.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Umsetzung prüfen: Stimmt je Mandat die Einstufung mit dem tatsächlichen Eintrag in der Vollmachtsdatenbank überein? Die Ausgabe kennt nur, was in der Tabelle stand.
- **Vier-Augen-Prinzip:** Die Arbeitsliste wird von einer Person abgearbeitet und von einer zweiten Person gegen den Datenbankbestand nachgeprüft und abgezeichnet – insbesondere bei Mandaten mit Vorberater, weil dort zwei Vollmachten nebeneinander bestehen können.
- **Freigabe durch einen Berufsträger** für die Mandanteninformation und für jede Änderung am Vollmachtsbestand (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch.** Die Bekanntgabefiktion des § 122a Abs. 4 AO – vierter Tag nach der Bereitstellung, im Zweifel mit Nachweispflicht der Behörde (für [JAHR] verifizieren) – wird nie aus einer KI-Antwort übernommen, sondern von einer Person berechnet, im Fristenprogramm erfasst und von einer zweiten Person anhand der Benachrichtigung nachgeprüft (siehe Prompt 35).
- Prüfen, dass in der Ausgabe an keiner Stelle von einer Einwilligung in die elektronische Bekanntgabe die Rede ist. § 122a Abs. 2 AO ist ein Opt-out über den Antrag auf postalische Bekanntgabe; die Einwilligungslösung war die bis zum 31.12.2025 geltende Fassung (für [JAHR] verifizieren).
- Prüfen, dass die Zweistufigkeit erhalten geblieben ist: Kann-Bekanntgabe nach Abs. 1 Satz 1 bereits anwendbar, Soll-Bekanntgabe nach Abs. 1 Satz 2 erst nach der Maßgabe des Art. 97 § 28 Abs. 2 Satz 2 EGAO (für [JAHR] verifizieren). Wird beides zusammengezogen, ist das Zeitfenster für die Bereinigung falsch dargestellt.
- Kontrollieren, dass die Ausgabe keine Steuernummer, keine Steuer-Identifikationsnummer und kein Aktenzeichen enthält – auch nicht in Beispielzeilen.
- Ein Antrag auf postalische Bekanntgabe wird nur nach Rücksprache mit dem Mandanten gestellt und in der Handakte dokumentiert; er wirkt nur für die Zukunft und erst mit Zugang.
- Interne Notiz und Ablaufvorschlag bleiben intern und gehen nicht an den Mandanten.

## Varianten

- **Nur Beraterwechsel:** „Beschränke die Bearbeitung auf Mandate mit bekanntem Vorberater und ergänze je Mandat, welcher Nachweis über den Widerruf der alten Vollmacht fehlt."
- **Personengesellschaften:** „Beschränke die Bearbeitung auf Mandate mit Feststellungsbescheiden und stelle je Mandat dar, wer Bekanntgabeadressat ist und wer die Benachrichtigung erhält."
- **Kurzfassung für die Teambesprechung:** „Erzeuge zusätzlich eine Kurzfassung mit höchstens 200 Wörtern: was sich ändert, welche drei Gruppen zuerst zu bearbeiten sind, wer zuständig ist."
- **Nachlauf:** „Erzeuge aus der abgearbeiteten Arbeitsliste eine Kontrollübersicht: Mandatskürzel | geändert am (leer) | geprüft von (leer) | verbliebene offene Punkte."

## Als Skill

Für die wiederkehrende Auswertung gibt es diesen Prompt auch als ausführende
Skill: [skills/06-finanzamt-fristen/111-vollmachtsbestand-bekanntgabe/](../../skills/06-finanzamt-fristen/111-vollmachtsbestand-bekanntgabe/).
Sie führt die Mandatstabelle Zeile für Zeile durch das Prüfschema, hält je
Mandat fest, worauf sich die Risikoeinstufung stützt, und verdichtet die
Einzelergebnisse zu einer sortierten Arbeitsliste.
