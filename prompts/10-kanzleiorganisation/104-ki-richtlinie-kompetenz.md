# 104 – KI-Richtlinie für Mitarbeitende und KI-Kompetenz nach Art. 4 KI-VO

**Problem:** Die Pflicht zur KI-Kompetenz des eigenen Personals gilt, Mitarbeitende nutzen daneben private Zugänge für Mandantenschriftverkehr, weil es schnell geht – und ohne schriftliche Richtlinie weiß niemand, welches Werkzeug erlaubt ist, was hineingegeben werden darf und wer im Verstoßfall zu informieren ist.
**Rolle:** Kanzleileitung, Berufsträger, IT-Verantwortliche, Datenschutzbeauftragte, Qualitätsbeauftragte
**DATEV-Bezug:** Kein einzelnes Fachmodul, sondern die Datenbestände und Zugänge, auf die sich die Richtlinie bezieht: DATEV DMS und Dokumentenablage, Kanzlei-Rechnungswesen, LODAS und Lohn und Gehalt, DATEV Unternehmen online, Eigenorganisation, DATEV-Cloud-Anwendungen und DATEVasp sowie Assistenz- und Auswertungsfunktionen innerhalb dieser Anwendungen und Schnittstellen zu externen Diensten. Das Werkzeugverzeichnis, die Einweisungsnachweise und die Freigaben werden im DMS geführt und in den technischen und organisatorischen Maßnahmen abgebildet.
**Was du bereitstellen musst:** Kanzleigröße und Rollen, heute tatsächlich genutzte Werkzeuge und Zugänge (auch die geduldeten), bereits nach § 62a StBerG geprüfte und freigegebene Werkzeuge, vorhandene Regelungen und Einweisungen mit Datum, Freigabestufen der Kanzlei, Vorhandensein eines Betriebsrats, bekannte Vorfälle nur als Fallart ohne Mandantenbezug.
**Datensparsamkeit:** Keine Mandantendaten einfügen – die Richtlinie regelt Werkzeuge und Rollen, keinen Fall. Mitarbeitende nur als Rollen benennen (`Sachbearbeitung FiBu`, `Sekretariat`, `Berufsträger A`), keine Namen und keine personenbezogenen Angaben zu Verstößen. Keine Zugangsdaten, Lizenzschlüssel oder Vertragsnummern. Bekannte Vorfälle nur als Fallart beschreiben, nie mit Mandat, Person oder Inhalt. Diese Richtlinie setzt die Prüfung nach § 62a StBerG voraus (sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) – siehe `DATENSCHUTZ.md` und Prompt 103. Für den ersten Durchlauf ein bereits freigegebenes Werkzeug verwenden oder ohne Kanzleibezug arbeiten: Kanzleigröße, Rollen und Werkzeuge nur als Struktur angeben, keine tatsächlich genutzten Produktnamen und keine Vorfallarten, und die Richtlinie anschließend in der Kanzlei ausfüllen.

## Prompt

```text
Du bist Organisationsbeauftragter einer deutschen Steuerkanzlei und schreibst
verbindliche Kanzleiregelungen. Du schreibst so, dass eine neue Mitarbeiterin
danach arbeiten kann, ohne nachzufragen: kurze Sätze, klare Zuständigkeit,
kein Konjunktiv, keine Empfehlung ohne Adressaten.

ABGRENZUNG – ZUERST LESEN
1. Dieser Prompt PRÜFT KEIN WERKZEUG und gibt kein Werkzeug frei. Die
   berufsrechtliche Prüfung eines Dienstleisters oder Werkzeugs nach
   § 62a StBerG erfolgt gesondert (Prompt 103); die Richtlinie setzt deren
   Ergebnis voraus und wiederholt sie nicht. Ein Werkzeug ohne abgeschlossene
   Prüfung steht im Werkzeugverzeichnis mit dem Status "Freigabe offen".
2. Empfiehl KEIN Produkt, keinen Anbieter und keine Marktalternative. Nenne
   Werkzeuge nur, soweit sie in den Angaben vorkommen, und bewerte sie nicht.
3. Dieser Prompt ist keine Rechtsberatung. Die Richtlinie ist ein Entwurf und
   wird von der Kanzleileitung in Kraft gesetzt.

GRUNDREGEL FÜR DIE GESAMTE ANTWORT
- Nenne zu jeder Pflicht die Rechtsgrundlage POSITIV mit Norm oder Artikel,
  Absatz und Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
  keine Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- Nenne keine Bußgeldhöhe, keinen Betrag, keine Schulungsdauer, keinen Turnus
  und keine Frist als Zahl. Wo eine Zeitangabe nötig ist, schreibe
  "unverzüglich" oder verweise die Festlegung in die Entscheidungsliste.
- Wiederhole den Datenschutz- und Freigabeleitfaden der Kanzlei nicht.
  Verweise auf ihn (Zonen und Freigabestufen in `DATENSCHUTZ.md`) und stelle
  nur den Bezug zur Werkzeugnutzung her. Widersprich ihm nicht.
- Alles, was die Kanzlei selbst entscheiden muss, gehört NICHT als Annahme in
  den Text, sondern in die Entscheidungsliste am Ende.

AUFGABE
Erzeuge drei Ergebnisse: eine schriftliche Kanzleirichtlinie zum Einsatz von
KI-Werkzeugen, ein Nachweisraster für die KI-Kompetenz der Beschäftigten und
ein Werkzeugverzeichnis.

KANZLEIRAHMEN
- Größe: [ZAHL BERUFSTRÄGER / ZAHL MITARBEITER / ZAHL STANDORTE]
- Rollen: [z. B. Berufsträger, Sachbearbeitung, Sekretariat, Auszubildende,
  freie Mitarbeit, externe Kräfte]
- Heute tatsächlich genutzte Werkzeuge, auch geduldete: [ANGABE]
- Nach § 62a StBerG geprüft und freigegeben: [vorhanden / keines]
  wenn vorhanden: [ANGABE]
- Vorhandene Regelungen: [Datenschutzleitfaden / Werkzeugliste /
  Arbeitsanweisung / keine], Stand: [DATUM]
- Einweisung zur KI-Kompetenz bisher durchgeführt: [nein / ja], Datum: [DATUM],
  dokumentiert: [nein / ja]
- Verpflichtung der Beschäftigten nach § 62 StBerG in Textform erfolgt:
  [nein / ja / teilweise]
- Freigabestufen der Kanzlei: [übernommen aus DATENSCHUTZ.md / abweichend
  geregelt / nicht geregelt]
- Betriebsrat vorhanden: [nein / ja]
- Bekannte Vorfälle, nur als Fallart: [vorhanden / keine]
  wenn vorhanden: [ANGABE]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Anwendungsbereich und Begriffe klären. Bestimme zuerst, was die Richtlinie
   erfasst: welche Systeme als KI-Systeme gelten, ob die Kanzlei als Betreiber
   handelt, welche Personen erfasst sind (auch Auszubildende, freie Mitarbeit,
   externe Kräfte, Berufsträger selbst) und ob auch Assistenzfunktionen
   innerhalb bereits eingesetzter Fachanwendungen erfasst sind. Ohne diesen
   Schritt regelt die Richtlinie einen unbestimmten Gegenstand.
2. Rechtsrahmen benennen. Ordne zu: die Pflicht des Betreibers, für
   ausreichende KI-Kompetenz der eigenen Beschäftigten zu sorgen
   (Art. 4 VO (EU) 2024/1689, anwendbar seit 02.02.2025), die
   Transparenzpflichten bei bestimmten KI-Systemen und Ausgaben
   (Art. 50 VO (EU) 2024/1689, anwendbar ab 02.08.2026), die Berufspflicht
   zur Verschwiegenheit
   (§ 57 Abs. 1 StBerG), die Verpflichtung der Beschäftigten in Textform
   (§ 62 StBerG), die Einbindung von Dienstleistern (§ 62a StBerG), die
   Strafbarkeit der Verletzung von Privatgeheimnissen (§ 203 StGB) und die
   Sicherheit der Verarbeitung (Art. 32 DSGVO) – jeweils
   für [JAHR] verifizieren. Verweise ergänzend auf die FAQ der
   Bundessteuerberaterkammer "KI im steuerberatenden Berufsstand" in der
   Fassung vom 27.01.2026 (Fassung und Fundstelle – für [JAHR] verifizieren).
3. Offenen Rechtsstand ausweisen. Halte in einem eigenen, sichtbaren Absatz
   fest: Zum Stand dieser Vorlage war der sogenannte Digital Omnibus zur
   KI-Verordnung am 07.05.2026 politisch geeinigt, aber noch nicht förmlich
   verabschiedet; Art. 4 der KI-Verordnung bleibt davon nach dem bekannten
   Stand unberührt. Ob und wie sich weitere Anwendungszeitpunkte verschieben,
   ist offen (Stand des Gesetzgebungsverfahrens und Auswirkung auf die
   Kanzleipflichten – für [JAHR] verifizieren). Leite daraus keine Entwarnung
   ab und stelle die Pflicht aus Art. 4 nicht unter Vorbehalt.
4. Positivliste festlegen. Regle: Es dürfen ausschließlich Werkzeuge genutzt
   werden, die in der Positivliste des Werkzeugverzeichnisses stehen. Die
   Aufnahme setzt die abgeschlossene Prüfung nach § 62a StBerG voraus
   (Prompt 103) und wird von einer benannten Rolle verantwortet. Regle, wie ein
   neues Werkzeug beantragt wird, wer entscheidet, wie die Entscheidung
   dokumentiert wird und was für Werkzeuge gilt, die nicht auf der Liste
   stehen. Nenne keine Produkte, die nicht in den Angaben vorkommen.
5. Eingabeverbot regeln. Regle als ausdrückliches Verbot: In nicht freigegebene
   Systeme werden keine mandats- und keine personenbezogenen Daten eingegeben –
   auch nicht in Ausschnitten, auch nicht maskiert, auch nicht zu Testzwecken.
   Private Zugänge sind für Kanzleiarbeit untersagt. Verweise für die
   Abgrenzung, was in freigegebene Systeme eingegeben werden darf, auf die
   Zonen und Freigabestufen in `DATENSCHUTZ.md`, ohne sie zu wiederholen.
   Regle den Umgang mit Zwischenablage, Datei-Upload, Bildschirmfreigaben,
   Assistenzfunktionen in Browsern und Endgeräten sowie mit privaten
   Endgeräten.
6. Kennzeichnungs- und Prüfpflicht für Ausgaben regeln. Regle: Jeder
   KI-gestützt erstellte Entwurf wird intern als solcher gekennzeichnet;
   Zahlen, Fundstellen, Fristen und Namen werden vor der Verwendung an der
   Quelle geprüft; die Verantwortung für das Ergebnis bleibt bei der Person,
   die es verwendet. Regle, was ohne Freigabe die Kanzlei nicht verlässt, und
   verweise für die Freigabestufen auf `DATENSCHUTZ.md`. Nimm die
   Transparenzpflichten nach Art. 50 VO (EU) 2024/1689 (anwendbar ab
   02.08.2026 – für [JAHR] verifizieren) nur insoweit auf, als die Kanzlei als
   Betreiber erfasst ist; das ist nach dem Wortlaut auf Emotionserkennung und
   biometrische Kategorisierung, auf Deepfakes und auf KI-erzeugte Texte
   beschränkt, die zur Information der Öffentlichkeit über Angelegenheiten von
   öffentlichem Interesse veröffentlicht werden. Regle, wer im Einzelfall
   prüft, ob eine dieser Konstellationen vorliegt, und halte ausdrücklich fest,
   dass sich aus Art. 50 keine allgemeine Pflicht ergibt, KI-Einsatz gegenüber
   Mandanten oder Behörden zu kennzeichnen; die interne Kennzeichnung nach
   Satz 1 bleibt davon unberührt.
7. Meldeweg bei Verstößen regeln. Regle: wer unverzüglich zu informieren ist,
   in welcher Form, was sofort zu veranlassen ist (Nutzung einstellen, Vorgang
   festhalten, Löschung beim Anbieter veranlassen), wer über die Meldepflichten
   entscheidet und wie der Vorfall dokumentiert wird. Verweise für den Ablauf
   auf `DATENSCHUTZ.md`, Abschnitt 8. Regle ausdrücklich, dass eine gemeldete
   Panne besser ist als eine verschwiegene, und dass die Meldung selbst nicht
   sanktioniert wird. Arbeitsrechtliche Folgen benenne nur dem Grunde nach und
   verweise sie in die Entscheidungsliste.
8. Beteiligung und Verpflichtung. Halte fest, dass die Einführung der
   Richtlinie eine Beteiligung des Betriebsrats erfordern kann, soweit ein
   Betriebsrat besteht, und benenne die in Betracht kommenden
   Mitbestimmungstatbestände mit Norm (§ 87 Abs. 1 BetrVG – Nummern benennen,
   für [JAHR] verifizieren). Halte getrennt davon fest, dass Beschäftigte vor
   dem ersten Zugriff auf Mandantendaten nach § 62 StBerG in Textform zur
   Verschwiegenheit zu verpflichten und über die Strafbarkeit zu belehren sind
   (für [JAHR] verifizieren) – das ist keine KI-Frage und wird nicht mit der
   Einweisung vermengt.
9. Nachweisraster für die KI-Kompetenz erzeugen. Erzeuge ein Raster mit:
   Zielgruppen nach Rolle und Nutzungsintensität; Mindestinhalten
   (Funktionsweise und Grenzen von Sprachmodellen, Halluzinationsrisiko bei
   Zahlen und Fundstellen, Berufsrecht und Verschwiegenheit, Datenschutz und
   Maskierung, kanzleiinterne Freigabestufen, Meldeweg); Format der Einweisung;
   Nachweisform mit Datum, Inhalt, Teilnehmerkreis und Bestätigung; Regelung
   für Neueintritte und für Rückkehr nach längerer Abwesenheit; Anlässen für
   eine Auffrischung; Ort der Aufbewahrung. Halte fest, dass ein gelesener
   Leitfaden allein den Nachweis nicht trägt. Nenne keine Dauer und keinen
   Turnus; beides gehört in die Entscheidungsliste.
10. Werkzeugverzeichnis erzeugen. Erzeuge die Struktur mit den Spalten:
    Werkzeug | Zweck | Status nach der Prüfung | Datum der Freigabe |
    verantwortliche Rolle | zugelassene Datenzone | zugelassene Rollen |
    Besonderheiten | nächste Überprüfung. Trage nur ein, was in den Angaben
    vorkommt; alles Übrige bleibt leer.
11. Grenzen der Richtlinie benennen. Halte fest, was die Richtlinie NICHT
    regelt: die Prüfung und Freigabe einzelner Werkzeuge (Prompt 103), die
    Einstufung eines Systems als Hochrisiko-KI, arbeitsrechtliche
    Einzelmaßnahmen, die Bewertung von Anbietern und die datenschutzrechtliche
    Gesamtdokumentation.
12. Entscheidungsliste und Einführung. Sammle alle offenen Festlegungen in
    einer Liste mit je einer Entscheidungsfrage. Nenne höchstens fünf
    Einführungsschritte in Reihenfolge, je mit verantwortlicher Rolle.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Eine fehlende Richtlinie, eine fehlende Einweisung oder die geduldete Nutzung
nicht freigegebener Werkzeuge sind KEIN Abbruchgrund – sie sind der Anlass
dieses Prompts.
Einzelne Vorgänge aussteuern, Bearbeitung fortsetzen:
- Nennen die Angaben ein bestimmtes Werkzeug, trage es in das
  Werkzeugverzeichnis mit dem Status "Freigabe offen – Prüfung nach Prompt 103"
  ein, bewerte es nicht und schreibe die Richtlinie weiter.
- Nennen die Angaben eine Vorfallart, bewerte den einzelnen Vorgang nicht und
  ordne ihm keine Person zu, verwende die Fallart aber als Regelungsanlass:
  Leite daraus in den Abschnitten zum Eingabeverbot und zum Meldeweg mindestens
  eine ausdrückliche Regel ab, die diese Fallart künftig erfasst. Die
  Aufarbeitung des Einzelvorgangs weise gesondert aus: "Aufarbeitung nach
  Abschnitt 8 in DATENSCHUTZ.md, Vorlage an den Berufsträger".
- Ist im Feld zur Verpflichtung nach § 62 StBerG "nein" oder "teilweise"
  angegeben, weise das als eigenen, vorrangig zu erledigenden Punkt aus und
  arbeite weiter.
Die gesamte Bearbeitung brichst du nur ab, wenn die Angaben (a) Mandantendaten,
Klarnamen, Steuernummern oder Zugangsdaten enthalten, (b) ein
berufsgerichtliches, aufsichtsrechtliches oder Ermittlungsverfahren gegen die
Kanzlei oder eine Person erwähnen, oder (c) eine personenbezogene Bewertung
eines Verstoßes verlangen. Gib dann nur aus: "Abbruchgrund liegt vor (Buchstabe angeben) –
Bearbeitung an dieser Stelle abgebrochen, Prüfung durch einen Berufsträger
außerhalb des KI-Werkzeugs."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER VOLLSTÄNDIGKEIT DER ANGABEN ab:
   ausreichend / in Teilen lückenhaft / als Regelung noch nicht tragfähig.
   Liste fehlende Angaben auf.
2. Schreibe jede Regel als Pflicht mit Adressat als ROLLE, nie als
   Personenname und nie als Empfehlung.
3. Formuliere jede Aussage zur bisherigen Praxis, die nicht in den Angaben
   steht, ausdrücklich als Vermutung.
4. Höchstens 1.200 Wörter für die Richtlinie; Raster und Verzeichnis zählen
   nicht mit.
5. Führe alle genannten Fundstellen am Ende in einer Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Vollständigkeit der Angaben
2. (Kanzleirichtlinie) – nummerierte Abschnitte:
   1. Zweck und Anwendungsbereich
   2. Begriffe und erfasste Systeme
   3. Rechtsrahmen und offener Rechtsstand
   4. Positivliste und Beantragung neuer Werkzeuge
   5. Eingabeverbot und Datenzonen, mit Verweis auf DATENSCHUTZ.md
   6. Kennzeichnung, Prüfpflicht und Freigabe von Ausgaben
   7. Meldeweg bei Verstößen
   8. Zuständigkeiten und Inkraftsetzung
3. (Nachweisraster KI-Kompetenz) – Tabelle:
   Zielgruppe | Mindestinhalte | Format | Nachweisform | Anlass | Ablage |
   erledigt (leer)
4. (Werkzeugverzeichnis) – Tabelle nach Schritt 10
5. (Was die Richtlinie nicht regelt)
6. (Von der Kanzlei festzulegen) – nummerierte Liste offener Punkte mit je
   einer Entscheidungsfrage
7. (Einführungsschritte) – höchstens fünf, in Reihenfolge, mit Rollen
8. (Zu verifizierende Rechtsgrundlagen): Nr. | Fundstelle | für welchen
   Abschnitt sie steht | geprüft von (leer)
9. (Interne Notiz)
10. Was ich nicht sicher weiß
```

## Anwendung

1. Vor dem Einsatz ehrlich erheben, was tatsächlich genutzt wird – einschließlich der geduldeten privaten Zugänge. Eine Richtlinie, die den Ist-Zustand beschönigt, regelt einen Betrieb, den es nicht gibt.
2. Die Werkzeugprüfung nach § 62a StBerG mit Prompt 103 zuerst durchführen. Ohne geprüfte Werkzeuge bleibt die Positivliste leer, und die Richtlinie verbietet mehr, als sie erlaubt.
3. Entwurf mit den Berufsträgern durchgehen und die Entscheidungsliste Punkt für Punkt abarbeiten – Turnus der Auffrischung, arbeitsrechtliche Folgen, Zuständigkeit für Werkzeuganträge und Umgang mit privaten Endgeräten sind Kanzleientscheidungen.
4. Besteht ein Betriebsrat, die Beteiligung vor der Inkraftsetzung klären; eine ohne Beteiligung eingeführte Regelung ist angreifbar.
5. Einweisung durchführen und mit Datum, Inhalt, Teilnehmerkreis und Bestätigung dokumentieren. Die Dokumentation ist der Nachweis, nicht die Schulung selbst.
6. Richtlinie datieren, versionieren, im DMS ablegen und in die Einarbeitung neuer Mitarbeitender aufnehmen. Ergänzt Prompt 29 (Onboarding), Prompt 23 (Arbeitsanweisung) und `DATENSCHUTZ.md`, dessen Checkliste in Abschnitt 7 dabei abzuhaken ist.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Die Richtlinie ist ein Entwurf. Vor der Inkraftsetzung liest eine zweite Person gegen, die den Entwurf nicht veranlasst hat, insbesondere auf Widersprüche zu `DATENSCHUTZ.md` und zu bestehenden Arbeitsanweisungen. **Die Inkraftsetzung erteilt ein Berufsträger**, mit Datum und Version (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Die Positivliste ist nur so gut wie die Prüfung dahinter.** Ein Werkzeug gehört erst nach abgeschlossener Prüfung nach § 62a StBerG auf die Liste; ein Auftragsverarbeitungsvertrag allein trägt die Aufnahme nicht (siehe Prompt 103).
- **Keine Produktempfehlung aus dem Modell.** Eine Antwort, die einen Anbieter empfiehlt oder Werkzeuge vergleicht, verlässt den Auftrag und ist zu verwerfen.
- **Den offenen Rechtsstand nicht glätten.** Die Änderungen an der KI-Verordnung waren zum Stand dieser Vorlage nicht förmlich verabschiedet; die Pflicht zur KI-Kompetenz steht davon unabhängig. Vor der Inkraftsetzung den Verfahrensstand nachsehen und den Absatz aktualisieren.
- **Verpflichtung nach § 62 StBerG und KI-Einweisung nicht vermengen.** Das eine ist eine berufsrechtliche Verpflichtung in Textform vor dem ersten Zugriff auf Mandantendaten, das andere eine Kompetenzmaßnahme; wer beides in einem Formular erledigt, hat am Ende keinen von beiden Nachweisen sauber.
- **Nachweise prüfen, nicht behaupten.** Für jede Einweisung müssen Datum, Inhalt, Teilnehmerkreis und Bestätigung vorliegen; ein Verteiler-E-Mail-Nachweis genügt nicht.
- **Prüfen, ob die Richtlinie irgendwo eine Zahl setzt**, die die Kanzlei nicht beschlossen hat – Turnus, Fristen, Schulungsdauer. Solche Stellen streichen und in die Entscheidungsliste verschieben.
- **Rechtsstand prüfen an:** Art. 4 und Art. 50 VO (EU) 2024/1689 im Amtsblatt der Europäischen Union einschließlich der Übergangs- und Anwendungsbestimmungen und des laufenden Änderungsverfahrens, § 57 Abs. 1, § 62 und § 62a StBerG sowie § 203 StGB (gesetze-im-internet.de), Art. 32 DSGVO, § 87 Abs. 1 BetrVG, an den FAQ der Bundessteuerberaterkammer "KI im steuerberatenden Berufsstand" in der jeweils aktuellen Fassung sowie an den Hinweisen der zuständigen Steuerberaterkammer.

## Varianten

- **Aushangfassung:** „Verdichte die Richtlinie auf eine Seite mit den fünf Regeln, die jede Mitarbeiterin kennen muss, ohne Rechtsgrundlagen im Fließtext."
- **Einweisungsunterlage:** „Erzeuge aus dem Nachweisraster eine Ablaufunterlage für die Einweisung mit Lernzielen, Beispielen ohne Mandantenbezug und Bestätigungszeile."
- **Kenntnisnahme:** „Erzeuge ein Bestätigungsformular zur Kenntnisnahme der Richtlinie, das die Verpflichtung nach § 62 StBerG ausdrücklich getrennt ausweist."
- **Kleine Kanzlei:** „Erzeuge eine Fassung für eine Einzelkanzlei mit wenigen Mitarbeitenden: gleiche Pflichten, weniger Rollen, eine verantwortliche Person."
- **Jährliche Überprüfung:** „Erzeuge eine Prüfliste für die jährliche Überprüfung von Richtlinie, Werkzeugverzeichnis und Einweisungsnachweisen, mit Anlässen für eine vorgezogene Überprüfung."
