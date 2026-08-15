# 106 – Elektronische Kassensysteme: Mitteilungspflicht nach § 146a Abs. 4 AO

**Problem:** Ein Kassensystem wurde angeschafft, gemietet, geleast, übernommen oder außer Betrieb genommen, und die Mitteilung an das Finanzamt fehlt oder ist unvollständig, weil niemand einen Überblick über den Systembestand je Betriebsstätte hat.
**Rolle:** Steuerberater, Sachbearbeitung Finanzbuchhaltung, Mandantenbetreuung
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen, DATEV Kassenarchiv online und DATEV Datenprüfung (Kassendaten), DATEV Unternehmen online (Kassenbuch online) – jeweils als Quelle für den Systembestand. Die Mitteilung selbst wird in Mein ELSTER oder über die ERiC-Schnittstelle der eingesetzten Software abgesetzt, nicht aus einer DATEV-Auswertung heraus.
**Was du bereitstellen musst:** Je Betriebsstätte eine Aufstellung aller elektronischen Aufzeichnungssysteme mit Systemart, Hersteller und Bezeichnung, Anzahl gleichartiger Geräte, Art der zertifizierten technischen Sicherheitseinrichtung, Monat und Jahr von Anschaffung oder Außerbetriebnahme, Beschaffungsform (Eigentum, Miete, Leasing), ersetztem Vorgängersystem und der Angabe, ob und wann bereits eine Mitteilung abgesetzt wurde. Kauf-, Miet- und Leasingverträge sowie Herstellerunterlagen nur als Auszug ohne Nummern.
**Datensparsamkeit:** Betriebsstätten und Systeme nur mit neutralen Kennungen bezeichnen (`Betriebsstätte 1`, `System 1`), Mandantenname durch `Mandant A` ersetzen. **Die Steuernummer gehört zum Datensatz nach § 146a Abs. 4 Satz 1 Nr. 2 AO, darf aber nach `DATENSCHUTZ.md` (Zone Rot) auch nicht in Auszügen in ein KI-Werkzeug** – ebenso wenig die Bezeichnung des Finanzamts oder ein Aktenzeichen. Seriennummern der Systeme und der Sicherheitseinrichtungen werden nicht eingefügt, sondern nur mit `vorhanden ja/nein` erfasst. Vor dem Einsatz müssen Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters geklärt sein – § 62a StBerG verlangt die dokumentierte sorgfältige Auswahl und einen Vertrag in Textform, der den Anbieter zur Verschwiegenheit verpflichtet; Einzelheiten in `DATENSCHUTZ.md`. Dient der Einsatz unmittelbar einem einzelnen Mandat, klärt der Berufsträger vorab die Frage der Mandanteneinwilligung (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Steuerberater in einer deutschen Steuerkanzlei und führst den
Meldebestand elektronischer Aufzeichnungssysteme. Du arbeitest inventarisch:
erst feststellen, welche Systeme je Betriebsstätte vorhanden sind, dann
welcher Vorgang eine Mitteilung auslöst, dann welche Angabe dafür fehlt.

AUFGABE
Erzeuge aus der Systeminventur eine Bestandsübersicht je Betriebsstätte, eine
Vorgangsliste mit Mitteilungsbedarf, eine Lückenliste und ein Anschreiben an
den Mandanten, mit dem die fehlenden Angaben angefordert werden.

ABGRENZUNG – so wird dieser Prompt gelesen
Geprüft wird ausschließlich der Melde- und Systembestand. Die laufende
Kassenführung nach GoBD – Tagesabschluss, Kassenbericht, Stornos,
Bedienerverwaltung, Belegausgabe, Einzelaufzeichnung – ist NICHT Gegenstand;
sie gehört in die Prüfung der laufenden Kassenführung (Prompt 38). Du bedienst
kein Portal, füllst keinen amtlichen Datensatz aus und übermittelst nichts:
die Mitteilung erfolgt nach § 146a Abs. 4 Satz 1 AO nach amtlich
vorgeschriebenem Datensatz durch Datenfernübertragung und wird von einem
Menschen in Mein ELSTER oder über die ERiC-Schnittstelle der eingesetzten
Software abgesetzt. Das BMF-Schreiben vom 28.06.2024 hat die zuvor bestehende
Aussetzung der Mitteilungspflicht aufgehoben; das Verfahren steht ab dem
01.01.2025 zur Verfügung (für [JAHR] verifizieren).

RAHMEN
- Betriebsstätten insgesamt: [ZAHL]
- Betriebsstätten, für die eine Inventur beiliegt: [ZAHL]
- Zuständigkeit je Betriebsstätte nach §§ 18 bis 20 AO in der Kanzlei
  festgestellt: [ja / nein / offen]
- Kassen-Nachschau oder Außenprüfung zu diesem Betrieb anhängig oder
  angekündigt: [nein / ja]

SYSTEMINVENTUR – je Betriebsstätte eine eigene Tabelle, eine Zeile je System
Betriebsstätte: [BETRIEBSSTAETTE] (neutrale Kennung)
Spalten und zulässige Angaben je Zeile:
1. Lfd. Nr.: [NUMMER]
2. Systemart: [elektronisches oder computergestütztes Kassensystem /
   Registrierkasse / Taxameter / Wegstreckenzähler / Waren- oder
   Dienstleistungsautomat / Geldspielgerät / elektronisches
   Buchhaltungsprogramm / offene Ladenkasse / unklar]
3. Hersteller und Bezeichnung: [ANGABE / unbekannt]
4. Anzahl gleichartiger Systeme: [ZAHL]
5. Seriennummer vorhanden: [ja / nein / unbekannt] – Nummer NICHT eintragen
6. Art der zertifizierten technischen Sicherheitseinrichtung:
   [Hardware / Cloud / keine / unbekannt]
7. Vorgang: [Anschaffung / Miete oder Leasing begonnen / Übernahme aus einem
   anderen Betrieb / Außerbetriebnahme / unverändert im Bestand],
   Monat und Jahr: [MONAT UND JAHR]
8. Beschaffungsform: [Eigentum / Miete / Leasing / unbekannt]
9. Ersetztes Vorgängersystem: [keines / lfd. Nr. / unbekannt]
10. Bereits mitgeteilt: [nein / unbekannt / ja]

AUSSTEUERUNGSREGEL – kein Abbruch, an einer objektiven Angabe.
Steht im Feld "Kassen-Nachschau oder Außenprüfung anhängig oder angekündigt"
ein "ja", erstelle Bestandsübersicht, Vorgangsliste und Lückenliste
unverändert weiter. Gib das Mandantenanschreiben aus, beschränke es aber auf
die reine Anforderung der fehlenden Angaben. Mache KEINE Aussage dazu, in
welcher Reihenfolge oder zu welchem Zeitpunkt unterbliebene Mitteilungen
nachgeholt werden sollten; schreibe an dieser Stelle nur:
"Ausgesteuert – Entscheidung durch einen Berufsträger außerhalb des
KI-Werkzeugs." Arbeite alle übrigen Abschnitte vollständig ab.

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Eindeutigkeit: eindeutig / vertretbare Varianten / nicht ohne weitere
   Angaben entscheidbar. Benenne fehlende Angaben, statt sie zu erfinden.
   "Unbekannt" ist ein Ergebnis, kein Anlass zum Raten.
2. Systemabgrenzung je Zeile: Ist das System von § 146a Abs. 1 AO erfasst?
   Welche Systeme erfasst sind und welche ausgenommen, bestimmt
   § 1 KassenSichV; zu den Ausnahmen zählen unter anderem elektronische
   Buchhaltungsprogramme sowie Waren- und Dienstleistungsautomaten. Gib
   weder den Ausnahmekatalog noch die Absatz- oder Satzgliederung aus dem
   Gedächtnis wieder und gib die Liste nicht als abschließend aus; markiere
   die Zuordnung jeder Zeile mit "Wortlaut des § 1 KassenSichV am amtlichen
   Volltext prüfen – für [JAHR] verifizieren".
   Eine offene Ladenkasse ist kein elektronisches Aufzeichnungssystem und
   löst keine Mitteilung nach § 146a Abs. 4 AO aus. Bei "unklar" trage die
   Zeile in die Lückenliste ein und entscheide nicht.
   Behaupte KEINE Pflicht, ein elektronisches Aufzeichnungssystem
   einzusetzen: § 146a Abs. 1 Satz 1 AO knüpft an die tatsächliche
   Verwendung an (für [JAHR] verifizieren).
3. Vorgangsermittlung je erfasster Zeile: Welcher Vorgang löst welche
   Mitteilung aus? Anschaffung und Außerbetriebnahme sind eigene Vorgänge;
   ein Systemwechsel ist deshalb regelmäßig ZWEI Vorgänge (Außerbetriebnahme
   des Vorgängersystems und Anschaffung des neuen Systems). Gemietete und
   geleaste Systeme stehen angeschafften gleich (AEAO zu § 146a Nr. 1.16.2.6 –
   für [JAHR] verifizieren); "gemietet" ist deshalb kein Grund, eine Zeile
   wegzulassen. Steht in Spalte 10 "nein" oder "unbekannt", behandle die Zeile
   als möglicherweise BEREITS VERSÄUMTE Mitteilung, nicht als offenen Termin.
4. Datensatzvollständigkeit je Vorgang: Prüfe die acht Angaben des
   § 146a Abs. 4 Satz 1 AO einzeln und vermerke je Angabe
   "liegt vor" oder "fehlt":
   Nr. 1 Name des Steuerpflichtigen
   Nr. 2 Steuernummer des Steuerpflichtigen
   Nr. 3 Art der zertifizierten technischen Sicherheitseinrichtung
   Nr. 4 Art des verwendeten elektronischen Aufzeichnungssystems – prüfe,
         ob Systemart (Spalte 2) sowie Hersteller und Bezeichnung
         (Spalte 3) dafür ausreichen; steht in Spalte 3 "unbekannt", ist
         das eine Lücke
   Nr. 5 Anzahl der verwendeten elektronischen Aufzeichnungssysteme
   Nr. 6 Seriennummer des verwendeten elektronischen Aufzeichnungssystems
   Nr. 7 Datum der Anschaffung des Systems
   Nr. 8 Datum der Außerbetriebnahme des Systems
   (Wortlaut und Nummerierung – für [JAHR] verifizieren.)
   Zu Nr. 2 und Nr. 6 gibst du KEINE Werte aus, auch wenn sie im Material
   stehen sollten, sondern ausschließlich:
   "(nicht im Werkzeug – in der Kanzlei einzusetzen)".
   Steht in Spalte 6 "keine" oder "unbekannt", ist das nicht nur eine Lücke im
   Datensatz, sondern eine Systemfrage nach § 146a Abs. 1 Sätze 2 und 3 AO
   (zertifizierte technische Sicherheitseinrichtung, einheitliche digitale
   Schnittstelle – für [JAHR] verifizieren). Vermerke sie als
   "Systemfrage – gehört in die Prüfung der laufenden Kassenführung",
   und bewerte sie hier nicht.
5. Bestandsvollständigkeit je Betriebsstätte: Bei jeder Mitteilung sind stets
   ALLE Systeme der betroffenen Betriebsstätte zu übermitteln, auch die
   bereits gemeldeten und die unverändert im Bestand befindlichen
   (AEAO zu § 146a Nr. 1.16.1.4 – für [JAHR] verifizieren). Eine Mitteilung,
   die nur das neue oder nur das abgemeldete System enthält, genügt nie.
   Prüfe deshalb je Betriebsstätte ausdrücklich, ob die Inventur vollständig
   ist, und vergleiche die Zahl der beiliegenden Inventuren mit der Zahl der
   Betriebsstätten im Rahmen. Fehlt eine Inventur, ist für diese
   Betriebsstätte keine Mitteilung vorbereitbar – sag das ausdrücklich.
6. Zuständigkeit: Die Mitteilung geht an das nach §§ 18 bis 20 AO zuständige
   Finanzamt (für [JAHR] verifizieren). Steht im Rahmenfeld "nein" oder
   "offen", nimm die Feststellung der Zuständigkeit als eigene Position in
   die Lückenliste auf. Nenne kein Finanzamt.
7. Fristen: Benenne die Fristen, die im Raum stehen, mit Rechtsgrundlage.
   Gesetzliche und im BMF-Schreiben genannte Stichtage darfst du im Wortlaut
   wiedergeben; ein Fristende für ein konkretes System berechnest du NICHT,
   und ein Datum aus den Angaben der Inventur leitest du NICHT ab:
   - Mitteilung innerhalb eines Monats nach Anschaffung oder
     Außerbetriebnahme (§ 146a Abs. 4 Satz 2 AO – für [JAHR] verifizieren)
   - Frist für Systeme i. S. d. § 1 Abs. 1 Satz 1 KassenSichV, die vor dem
     01.07.2025 angeschafft wurden: 31.07.2025 nach dem BMF-Schreiben vom
     28.06.2024. Für alle übrigen Systemarten gilt diese Frist nicht; prüfe
     sie dort nicht mit. Weise ausdrücklich darauf hin, dass dieser Termin
     aus dem BMF-Schreiben stammt und nicht aus dem Gesetz
     (für [JAHR] verifizieren).
   Ergänze in jedem Fall: "Fristen berechnet und erfasst ein Mensch."
8. Sanktionslage – ohne zu drohen: § 379 Abs. 1 Satz 1 Nr. 4 bis 6 AO erfasst
   die Verwendung, den Schutz und das Bewerben oder Inverkehrbringen
   elektronischer Aufzeichnungssysteme; der Rahmen folgt aus § 379 Abs. 6 AO
   und beträgt bis 25.000 € (für [JAHR] verifizieren).
   Stelle ausdrücklich klar: Die MITTEILUNGSPFLICHT nach § 146a Abs. 4 AO ist
   selbst NICHT bußgeldbewehrt. Nenne kein Bußgeld für eine unterbliebene oder
   verspätete Mitteilung und leite daraus keinen Handlungsdruck ab. Die Frage,
   welche Folgen eine unterbliebene oder verspätete Mitteilung im konkreten
   Fall hat, beantwortest du nicht, sondern verweist sie an den Berufsträger.
9. Anlass: Erkläre in höchstens drei Sätzen, warum der Bestand stimmen muss –
   die Kassen-Nachschau nach § 146b Abs. 1 AO findet ohne vorherige
   Ankündigung statt und kann ohne Prüfungsanordnung in eine Außenprüfung
   übergehen; dafür ist ein schriftlicher Hinweis erforderlich
   (§ 146b Abs. 3 AO – für [JAHR] verifizieren).

ANFORDERUNGEN
- Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
  Satz, Verwaltungsanweisung mit Datum), jeweils mit dem Zusatz
  "für [JAHR] verifizieren", und führe sie am Ende in der Tabelle
  "Zu verifizierende Rechtsgrundlagen" auf. Erfinde keine Paragrafen,
  BMF-Schreiben oder Aktenzeichen; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren" statt einer Angabe.
- Die DSFinV-K ist eine Verwaltungsvorgabe des Bundeszentralamts für Steuern
  und keine Rechtsnorm. Erwähne sie nur so und nenne eine Version nur mit
  Quelle und dem Zusatz "Stand für [JAHR] verifizieren".
- Formuliere jede Aussage über den Sachverhalt, die nicht aus der Inventur
  folgt, als Vermutung und kennzeichne sie als solche.
- Das Mandantenanschreiben ist in Sie-Form, höchstens 300 Wörter, sachlich,
  ohne Vorwurf und ohne Sanktionshinweis. Es fordert nur die fehlenden
  Angaben an und nennt je Angabe, wo der Mandant sie findet.

AUSGABEFORMAT
1. (Einschätzung der Eindeutigkeit)
2. (Bestandsübersicht) – je Betriebsstätte eine Tabelle:
   Lfd. Nr. | Systemart | von § 146a Abs. 1 AO erfasst (ja/nein/unklar) |
   Beschaffungsform | Vorgang | bereits mitgeteilt
3. (Vorgangsliste mit Mitteilungsbedarf) – Tabelle:
   Nr. | Betriebsstätte | Vorgang | Mitteilung erforderlich (ja/nein/unklar) |
   Begründung mit Fundstelle | umfasst welche Systeme der Betriebsstätte
4. (Lückenliste) – was fehlt, um übermitteln zu können. Tabelle:
   Nr. | Betriebsstätte | fehlende Angabe | Nummer im Datensatz |
   woher sie zu beschaffen ist | wer beschafft | erledigt (leer)
5. (Fristen im Raum) – ohne berechnetes Fristende, mit Fundstelle
6. (Sanktionslage und Anlass) – Ergebnis der Schritte 8 und 9, höchstens
   sechs Sätze, jede Aussage mit Fundstelle; ausdrücklich mit dem Satz, dass
   die Mitteilungspflicht nach § 146a Abs. 4 AO selbst nicht bußgeldbewehrt
   ist
7. (Mandantenanschreiben) – Datenanforderung, Sie-Form
8. (Interne Notiz) – nicht an den Mandanten: was der Berufsträger vorab
   entscheiden muss, welche Punkte an die Prüfung der laufenden Kassenführung
   abzugeben sind, was in die Handakte gehört
9. (Was ich nicht sicher weiß)
10. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. **Vorschaltfrage durch den Berufsträger, vor dem Werkzeugeinsatz:** Steht im Raum, dass Kassenaufzeichnungen unrichtig sind, ist eine Berichtigung nach § 153 AO oder eine Selbstanzeige im Gespräch oder läuft ein Steuerstraf- oder Bußgeldverfahren? Dann gehört der Sachverhalt nach `DATENSCHUTZ.md` (Zone Rot) nicht in ein KI-Werkzeug. Die Antwort wird in der Handakte vermerkt, nicht im Prompt.
2. Systeminventur zuerst beim Mandanten erheben, nicht aus der Buchhaltung ableiten. Geleaste und gemietete Geräte, Zweitkassen, mobile Kassen im Außendienst und Systeme in Filialen fehlen erfahrungsgemäß in der Anlagenbuchhaltung.
3. Eine Tabelle je Betriebsstätte, auch wenn dieselbe Kasse zweimal vorkommt. Die Mitteilung ist betriebsstättenbezogen; eine über alle Standorte gemischte Liste lässt sich nicht in eine Mitteilung überführen.
4. Ergebnis mit der Lückenliste beginnen: Ohne Seriennummer und ohne Art der zertifizierten technischen Sicherheitseinrichtung ist keine Übermittlung möglich, gleich wie klar der Vorgang ist.
5. Übermittlung selbst in Mein ELSTER oder in der Kanzleisoftware durch einen Menschen. Steuernummer und Seriennummern werden erst dort eingesetzt – nie im Werkzeug.
6. Der Prompt ersetzt Prompt 38 nicht. Wer den Meldebestand geordnet hat, hat noch keine ordnungsmäßige Kassenführung.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Bestandsübersicht und Vorgangsliste werden von einer zweiten Person gegen die Inventur des Mandanten nachgeprüft; die Freigabe der Mitteilung und des Mandantenanschreibens erfolgt durch einen Berufsträger (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum aus der KI-Antwort übernehmen; die Monatsfrist nach § 146a Abs. 4 Satz 2 AO wird im Fristenprogramm erfasst und von einer zweiten Person nachgeprüft.
- **Vollständigkeit je Betriebsstätte prüfen, bevor übermittelt wird.** Bei jeder Mitteilung sind alle Systeme der Betriebsstätte zu übermitteln (AEAO zu § 146a Nr. 1.16.1.4 – für [JAHR] verifizieren). Eine Mitteilung, die nur den neuen Vorgang enthält, ist der häufigste Fehler und macht die Meldung unvollständig.
- **Rechtsstand prüfen an:** § 146a AO, § 146b AO, § 379 AO, KassenSichV, Anwendungserlass zur AO zu § 146a und BMF-Schreiben vom 28.06.2024 (Fassung und Nachfolgeschreiben für [JAHR] verifizieren).
- **Keine Sanktionsdrohung stehen lassen.** Enthält der Entwurf einen Hinweis auf ein Bußgeld für die unterbliebene Mitteilung, ist er zu streichen: § 379 AO erfasst die Mitteilungspflicht nicht.
- **Zone Rot kontrollieren:** Steuernummer, Bezeichnung des Finanzamts, Aktenzeichen und Seriennummern dürfen weder in der Eingabe noch in der Ausgabe stehen. Findet sich eine solche Angabe, ist der Vorgang nach Abschnitt 8 der `DATENSCHUTZ.md` zu behandeln.
- Bei Systemen, die als "unklar" eingestuft bleiben, entscheidet ein Berufsträger anhand des Wortlauts des § 1 KassenSichV und der Herstellerunterlagen, nicht das Modell.
- Ergebnis in der Mandantenakte dokumentieren, einschließlich der Systeme, für die der Mandant keine Angaben liefern konnte.

## Varianten

- **Betriebsübernahme:** "Ergänze eine Spalte, aus welchem Vorbetrieb das System stammt, und prüfe je System, ob der Vorgang beim Übernehmer eine Anschaffung und beim Übergeber eine Außerbetriebnahme auslöst."
- **Filialbetrieb:** "Erzeuge je Betriebsstätte einen eigenen Übermittlungsbogen und zusätzlich eine Übersicht, welche Betriebsstätte noch keine vollständige Inventur geliefert hat."
- **Jahresarbeit:** "Leite aus dem Ergebnis eine Arbeitsanweisung ab, die sicherstellt, dass jede Anschaffung und jede Außerbetriebnahme eines Kassensystems der Kanzlei gemeldet wird, mit Auslöser, Zuständigkeit und Wiedervorlage."
- **Mandantenmerkblatt:** "Erzeuge eine Kurzfassung mit höchstens zehn Punkten, die erklärt, welche Vorgänge der Mandant der Kanzlei künftig unaufgefordert mitteilt."

## Als Skill

Für die wiederkehrende Auswertung gibt es diesen Prompt auch als ausführende
Skill: [skills/07-gobd-kasse/106-kassensystem-mitteilungspflicht/](../../skills/07-gobd-kasse/106-kassensystem-mitteilungspflicht/).
Sie arbeitet die Systeminventur zeilenweise ab und prüft je Betriebsstätte, ob der
Bestand für eine Mitteilung vollständig ist.
