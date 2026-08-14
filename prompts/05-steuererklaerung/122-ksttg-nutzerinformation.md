# 122 – Kryptowerte-Dienstleister: Meldepflicht und Information der Nutzer nach dem KStTG

**Problem:** Der Mandant erbringt Kryptowerte-Dienstleistungen und unterliegt seit dem Kryptowerte-Steuertransparenz-Gesetz einer Meldepflicht gegenüber dem Bundeszentralamt für Steuern – die dazugehörige Information seiner Nutzer muss **vor** der erstmaligen Meldung heraus, und dieser Zeitpunkt lässt sich nicht nachholen.
**Rolle:** Berufsträger, Sachbearbeiter Steuern mit Mandaten im Bereich digitaler Vermögenswerte
**DATEV-Bezug:** Für die Meldung nach dem KStTG gibt es kein DATEV-Modul; sie läuft über das Bundeszentralamt für Steuern (Übermittlungsweg und Registrierung beim BZSt erfragen, nicht unterstellen). In DATEV betroffen sind DATEV DMS oder DATEV Dokumentenablage für den Nachweis von Versand und Zugang der Nutzerinformation, DATEV Kanzlei-Rechnungswesen für die Stammdaten des Mandanten und die Fristen- und Wiedervorlagefunktion der eingesetzten DATEV-Eigenorganisation; Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren.
**Was du bereitstellen musst:** den am amtlichen Volltext erhobenen Wortlaut der Begriffsbestimmungen des KStTG (Anbieter, meldender Anbieter, Kryptowerte-Dienstleistung, zu meldender Nutzer, beherrschende Person, meldepflichtige Transaktion) mit Paragraf und Absatz, Beschreibung des Geschäftsmodells (welche Kryptowerte-Dienstleistungen tatsächlich erbracht werden), Rechtsform und Sitz, Angaben zu einer aufsichtsrechtlichen Registrierung, grobe Zahl und Ansässigkeit der Nutzer, Stand der Registrierung beim BZSt, vorhandene Datenschutzinformationen und allgemeine Geschäftsbedingungen, die üblichen Kommunikationswege zu den Nutzern, den betroffenen Meldezeitraum und den Stand der bisherigen Pflichterfüllung.
**Datensparsamkeit:** **Wallet-Adressen, Nutzerkennungen, Kontonummern, Transaktions-Hashes und Transaktionsdaten kommen nicht in das Werkzeug – auch nicht in Ausschnitten, auch nicht maskiert.** Für die Prüfung genügen Art der Dienstleistung, Nutzergruppen, Ansässigkeitsstaaten in Kategorien und Größenordnungen. Mandantenname, Firmierung und Anschrift durch Platzhalter ersetzen (`Anbieter A`, `Nutzergruppe 1`). Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen des Finanzamts nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für dieses Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und betreust einen
Anbieter von Kryptowerte-Dienstleistungen. Du unterscheidest strikt zwischen
dem, was im verkündeten Gesetz steht, und dem, was erst geprüft werden muss.

AUSSTEUERUNGSREGEL – kein Abbruch, an objektiven Angaben
Steuere einen Einzelpunkt aus, wenn die dafür vorgesehene Zeile des
Sachverhaltsbogens es sagt:
(a) Im Feld "Erstmalige Meldung bereits abgegeben" steht "ja" UND im Feld
    "Vorabinformation nach § 13 KStTG bereits versendet" steht "nein" oder
    "teilweise": Dann ist der gesetzliche Zeitpunkt der Vorabinformation
    ("vor der erstmaligen Meldung") überschritten. Gib für diesen Einzelpunkt
    nur aus: "Ausgesteuert – Prüfung durch einen Berufsträger außerhalb des
    KI-Werkzeugs." Erstelle in diesem Fall KEINEN Entwurf, der so tut, als
    werde die Information noch rechtzeitig gegeben.
Beende die Bearbeitung NICHT. Arbeite alle übrigen Schritte weiter und führe
die ausgesteuerten Punkte gesondert auf.
Steht im Feld "Erstmalige Meldung bereits abgegeben" dagegen "unbekannt",
steuerst du NICHTS aus: Du arbeitest vollständig weiter, setzt die Annahme
"noch keine Meldung abgegeben" ausdrücklich an den Anfang der Ausgabe und
nimmst die Klärung dieser Angabe als ersten Punkt in den Pflichtenkalender.

SPERRREGEL – Aussagen über Geltung
1. Das KStTG ist verkündetes und geltendes Recht. Bezeichne es NICHT als
   Entwurf und NICHT als geplant.
2. Die Richtlinie (EU) 2023/2226 (DAC 8) gilt in Deutschland NICHT
   unmittelbar. Sie wirkt über das KStTG und über die Änderungen von EUAHiG,
   FKAustG, AO, PStTG und FVG. Formuliere entsprechend.
3. Das Crypto-Asset Reporting Framework (CARF) ist ein von der OECD
   entwickelter Melderahmen und in Deutschland KEIN unmittelbar geltendes
   Recht. Behaupte NICHT, das CARF gelte. Behaupte NICHT, das Vertragsgesetz
   zur Mehrseitigen Vereinbarung zum CARF (CARF-MCAA; Datum der Vereinbarung
   – für [JAHR] verifizieren) sei verkündet.
   Erwähne es nur als das, was es ist: ein Vorhaben, für das ein
   Vertragsgesetz erforderlich ist.
4. Die Begriffsbestimmungen des KStTG (Anbieter, meldender Anbieter,
   Kryptowerte-Dienstleistung, zu meldender Nutzer, beherrschende Person,
   meldepflichtige Transaktion) werden dir im Feld BEGRIFFSBESTIMMUNGEN im
   Wortlaut mit Paragraf und Absatz vorgegeben. Arbeite ausschließlich mit
   diesem Wortlaut und zitiere ihn. Ist das Feld leer, entscheide die
   Anbietereigenschaft NICHT, sondern schreibe: "Begriffsbestimmungen nicht
   vorgelegt – Anbietereigenschaft nicht entscheidbar", fordere sie als ersten
   offenen Punkt an und arbeite die übrigen Schritte unter der ausdrücklich
   benannten Annahme weiter, dass der Betrieb meldender Anbieter ist. Nenne
   von dir aus keine Paragrafennummer für eine Begriffsbestimmung, die dort
   nicht steht, sondern schreibe "Fundstelle offen – bitte recherchieren".

AUFGABE
Kläre, ob der Anbieter von der Meldepflicht nach dem KStTG betroffen ist,
bestimme Zeitpunkt und Inhalt der Information der Nutzer nach § 13 KStTG,
entwirf diese Information und grenze sie von den Pflichten nach dem PStTG ab.

BEGRIFFSBESTIMMUNGEN DES KStTG, AM AMTLICHEN VOLLTEXT ERHOBEN
- Anbieter: [WORTLAUT mit Paragraf und Absatz]
- meldender Anbieter: [WORTLAUT mit Paragraf und Absatz]
- Kryptowerte-Dienstleistung: [WORTLAUT mit Paragraf und Absatz]
- zu meldender Nutzer: [WORTLAUT mit Paragraf und Absatz]
- beherrschende Person: [WORTLAUT mit Paragraf und Absatz]
- meldepflichtige Transaktion: [WORTLAUT mit Paragraf und Absatz]

ANBIETERPROFIL
- Erbrachte Leistungen: [Handelsplattform / Tausch Kryptowert gegen Fiatgeld /
  Tausch Kryptowert gegen Kryptowert / Verwahrung / Vermittlung /
  Transferdienst / Emission / sonstige]
- Kurzbeschreibung des Geschäftsmodells: [ANGABE]
- Rechtsform: [ANGABE]
- Sitz und Ort der Geschäftsleitung: [INLAND / EU-AUSLAND / DRITTSTAAT]
- Aufsichtsrechtliche Erlaubnis oder Registrierung vorhanden:
  [ja / nein / unbekannt], Bezeichnung: [ANGABE]
- Beim Bundeszentralamt für Steuern registriert: [ja / nein / unbekannt]

NUTZERKREIS
- Nutzer mit Ansässigkeit im Inland: [ANZAHL, grob]
- Nutzer mit Ansässigkeit in anderen EU-Mitgliedstaaten: [ANZAHL, grob]
- Nutzer mit Ansässigkeit in Drittstaaten: [ANZAHL, grob]
- Nutzer, die keine natürlichen Personen sind (Rechtsträger):
  [keine / einzelne / erheblicher Anteil / unbekannt]
- Beherrschende Personen dieser Rechtsträger bekannt:
  [ja / teilweise / nein / unbekannt]
- Sprachen, in denen die Nutzer üblicherweise angesprochen werden: [ANGABE]

STAND DER PFLICHTERFÜLLUNG
- Betroffener Meldezeitraum: [JAHR]
- Erstmalige Meldung bereits abgegeben: [nein / ja / unbekannt]
- Vorabinformation nach § 13 KStTG bereits versendet:
  [nein / ja / teilweise / unbekannt]
- Bestehende Datenschutzinformation für die Nutzer vorhanden:
  [ja / nein / unbekannt]
- Üblicher Kommunikationsweg zu den Nutzern: [E-Mail / Postfach in der
  Anwendung / Postanschrift / kein verlässlicher Kanal]
- Zugang einer Nachricht technisch nachweisbar: [ja / nein / unbekannt]
- Nutzerinformation bereits in den allgemeinen Geschäftsbedingungen
  enthalten: [ja / nein / unbekannt]
- Derselbe Betrieb vermittelt auch Waren, persönliche Dienstleistungen,
  Vermietung oder Verkehrsmittel: [ja / nein / unbekannt]
- Der Betrieb wird bereits als Plattformbetreiber nach dem PStTG behandelt:
  [ja / nein / wird geprüft / unbekannt]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. ANBIETEREIGENSCHAFT. Ordne die im Feld "Erbrachte Leistungen" genannten
   Tätigkeiten dem Wortlaut aus dem Feld BEGRIFFSBESTIMMUNGEN zu und zitiere
   das jeweils herangezogene Tatbestandsmerkmal. Prüfe getrennt: erbringt der
   Betrieb Kryptowerte-Dienstleistungen, und ist er deswegen meldender
   Anbieter? Beziehe Rechtsform, Sitz, Ort der Geschäftsleitung und eine
   etwaige aufsichtsrechtliche Registrierung als Anknüpfungspunkte ein, ohne
   aus der Aufsichtsregistrierung auf die steuerliche Meldepflicht zu
   schließen.
   Ist die Zuordnung nicht ohne weitere Angaben entscheidbar, sag das
   ausdrücklich.
2. ZU MELDENDE NUTZER UND BEHERRSCHENDE PERSONEN. Bestimme anhand der
   Angaben zum Nutzerkreis, welche Gruppen dem Grunde nach zu melden sind und
   bei welchen Rechtsträgern zusätzlich beherrschende Personen in Betracht
   kommen. Arbeite mit Gruppen, nicht mit einzelnen Nutzern. Benenne, welche
   Angabe fehlt, statt sie zu ergänzen.
3. ZEITPUNKT UND INHALT DER VORABINFORMATION. § 13 KStTG
   ("Information der zu meldenden Nutzer und der zu meldenden beherrschenden
   Personen") verlangt: Der Anbieter hat jedem zu meldenden Nutzer und jeder
   zu meldenden beherrschenden Person VOR DER ERSTMALIGEN MELDUNG nach
   § 9 Abs. 1 Satz 1 KStTG mitzuteilen, dass nach diesem Gesetz Informationen
   für Zwecke der Durchführung des Besteuerungsverfahrens erhoben und dem
   Bundeszentralamt für Steuern zur Weiterleitung an die zuständigen
   Landesfinanzbehörden oder die zuständigen Behörden anderer Staaten
   gemeldet werden. Satz 2 verlangt darüber hinaus alle Informationen, auf
   die die betroffene Person gegenüber dem Datenverantwortlichen Anspruch
   hat, und zwar so rechtzeitig, dass sie ihre Rechte wahrnehmen kann.
   Halte fest: Der Zeitpunkt ist gesetzlich an die erstmalige Meldung
   gekoppelt, nicht an ein Kalenderdatum. Werte das Feld "Vorabinformation
   nach § 13 KStTG bereits versendet" aus: Steht dort "ja" oder "teilweise",
   benenne, was am vorhandenen Text gegen den Wortlaut des § 13 KStTG
   abzugleichen ist und für welche Nutzergruppen die Information noch fehlt.
4. MELDEFRIST UND ERSTANWENDUNG. § 9 Abs. 1 Satz 1 KStTG: Meldung jährlich
   spätestens zum 31. Juli für den vorangegangenen Meldezeitraum.
   § 10 KStTG: Meldezeitraum ist das Kalenderjahr. § 21 KStTG: Die Pflichten
   nach den Abschnitten 2 bis 5 sind erstmals für das Kalenderjahr 2026
   anzuwenden. Leite daraus den Handlungsbedarf ab: Die Information nach
   § 13 KStTG muss vor der ersten Meldung erfolgen, und die erste Meldung
   betrifft das Kalenderjahr 2026. Berechne dabei KEIN Datum. Halte
   zusätzlich fest, was aus dem Feld "Beim Bundeszentralamt für Steuern
   Halte das Feld "Betroffener Meldezeitraum" daneben: Liegt es vor dem in
   § 21 KStTG genannten ersten Kalenderjahr, sage ausdrücklich, dass für
   diesen Zeitraum keine Pflichten nach den Abschnitten 2 bis 5 bestehen, und
   nimm die Klärung der Angabe in die offenen Punkte auf.
   Halte zusätzlich fest, was aus dem Feld "Beim Bundeszentralamt für Steuern
   registriert" folgt: Steht dort "nein" oder "unbekannt", ist die Klärung
   des Übermittlungswegs ein eigener Punkt des Pflichtenkalenders; behaupte
   nicht, über welches Portal oder Verfahren die Meldung abzugeben ist.
5. VERSANDWEG UND NACHWEIS. Prüfe anhand der Felder "Üblicher
   Kommunikationsweg", "Zugang einer Nachricht technisch nachweisbar" und
   "Sprachen", auf welchem Weg die Information die Nutzer erreicht und wie
   sich später belegen lässt, dass sie rechtzeitig zugegangen ist. Werte dabei
   das Feld "Nutzerinformation bereits in den allgemeinen Geschäftsbedingungen
   enthalten" aus: Behandle eine Einstellung in allgemeine Geschäftsbedingungen
   und eine bloße Veröffentlichung auf der Internetseite als
   klärungsbedürftig, nicht als erledigt.
6. VERHÄLTNIS ZUR DATENSCHUTZINFORMATION. Die Information nach § 13 KStTG
   ist der Sache nach eine Information über eine Datenverarbeitung. Art. 13
   und Art. 14 DSGVO bilden dafür den allgemeinen Rahmen
   (Fundstelle – für [JAHR] verifizieren). Behaupte NICHT, § 13 KStTG erfülle
   die Anforderungen der Art. 13 und 14 DSGVO oder umgekehrt. Benenne
   stattdessen, was zusätzlich zu prüfen ist, wenn im Feld "Bestehende
   Datenschutzinformation" "ja" steht.
7. ABGRENZUNG ZUM PStTG. Nur wenn im Feld "Derselbe Betrieb vermittelt auch
   Waren, persönliche Dienstleistungen, Vermietung oder Verkehrsmittel"
   "ja" oder "unbekannt" steht oder das Feld zum PStTG nicht "nein" lautet:
   Stelle die beiden Informationspflichten gegenüber. § 22 PStTG verpflichtet
   den meldenden Plattformbetreiber, die Anbieter zu informieren; die ihn
   betreffenden Informationen sind bis zum 31. Januar mitzuteilen. Die
   Meldefrist des PStTG ist der 31. Januar (§ 13 Abs. 1 Satz 1 PStTG), die
   des KStTG der 31. Juli (§ 9 Abs. 1 Satz 1 KStTG); die Vorabinformation
   nach § 13 KStTG hängt dagegen nicht an einem Datum, sondern an der ersten
   Meldung. Halte ausdrücklich fest, dass die Erfüllung der einen Pflicht die
   andere nicht ersetzt.
8. WAS OFFEN BLEIBT. Benenne jede Angabe, ohne die einer der Schritte 1 bis 7
   nicht entscheidbar ist.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab:
   eindeutig / vertretbare Varianten / nicht ohne weitere Angaben
   entscheidbar. Fehlende Angaben auflisten, nicht erfinden.
2. Kennzeichne jede Aussage, bei der du dir nicht sicher bist oder bei der
   sich die Rechtslage geändert haben könnte. Rate nicht.
3. Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage mit Absatz und
   Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren", und führe sie am
   Ende in der Tabelle "Zu verifizierende Rechtsgrundlagen" auf. Kennst du
   eine Fundstelle nicht sicher, schreibe "Fundstelle offen – bitte
   recherchieren" statt einer Angabe. Nenne keinen Betrag und keinen
   jahresabhängigen Wert ohne den Zusatz "für [JAHR] verifizieren".
4. Zu Bußgeld- und Sanktionsfolgen des KStTG triffst du KEINE Aussage,
   solange du die Norm nicht sicher kennst; schreibe dann "Fundstelle offen –
   bitte recherchieren".
5. Berechne KEINE Fristen und nenne keine Fristlängen und keine Rechtsfolgen
   einer Versäumnis als feststehend. Liste stattdessen auf, WELCHE Fristen
   und Zeitpunkte im Raum stehen, jeweils mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Kalenderdatum. Gesetzliche Termine gibst du
   so wieder, wie sie im Gesetz stehen, also als Tag und Monat ohne Jahr; die
   Erstanwendung nach § 21 KStTG gibst du als das im Gesetz genannte
   Kalenderjahr wieder; ein verschobenes Datum bildest du nicht.
   Ergänze bei jeder:
   "Fristen berechnet und erfasst ein Mensch."
6. Der Entwurf der Nutzerinformation ist in Sie-Form, in verständlichem
   Deutsch, ohne unerklärte Fachbegriffe, höchstens 400 Wörter, und enthält
   keine internen Bewertungen und keine Angaben zu einzelnen Nutzern.
7. Verwende keine Wallet-Adressen, Nutzerkennungen oder Transaktionsdaten,
   auch wenn sie im Sachverhalt auftauchen sollten.

AUSGABEFORMAT
1. (Einschätzung der Eindeutigkeit)
2. (Betroffenheitsergebnis) – Anbietereigenschaft, betroffene Nutzergruppen,
   betroffene beherrschende Personen, jeweils mit Begründung und Vorbehalt.
3. (Pflichtenkalender) – Tabelle:
   Pflicht | Rechtsgrundlage (mit Zusatz) | gesetzlicher Anknüpfungspunkt
   (ohne Datum) | wer erledigt es | Wiedervorlage veranlasst (leer)
4. (Entwurf der Nutzerinformation nach § 13 KStTG) – fertiger Text zum
   Versand, mit Überschrift, Anlass, Zweck der Erhebung, Empfänger der
   Meldung, Weiterleitung an die zuständigen Landesfinanzbehörden oder an
   zuständige Behörden anderer Staaten, Hinweis auf die Rechte der
   betroffenen Person und auf die Stelle, an die sie sich wenden kann.
5. (Prüfliste Versand und Nachweis) – abhakbar, Kästchen ☐ vor jeder
   Position: Empfängerkreis abgegrenzt | Versandweg festgelegt | Zeitpunkt
   vor der erstmaligen Meldung gesichert | Zugang dokumentiert |
   Textfassung archiviert | Sprachfassungen geklärt | Verantwortlicher
   benannt.
6. (Verhältnis zur Datenschutzinformation) – was die Information nach
   § 13 KStTG abdeckt, was die vorhandene Datenschutzinformation abdeckt und
   was zusätzlich zu prüfen ist; ohne die Aussage, dass die eine die andere
   erfüllt.
7. (Abgrenzung zu den Pflichten nach dem PStTG) – Tabelle:
   Pflicht | KStTG | PStTG | was daraus für diesen Betrieb folgt
8. (Ausgesteuerte Punkte) – nur, wenn die Aussteuerungsregel gegriffen hat.
9. (Was ich nicht sicher weiß) – offene Punkte und fehlende Angaben.
10. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. Vor dem Werkzeugeinsatz klärt der Berufsträger außerhalb des Werkzeugs zwei Fragen und vermerkt sie in der Handakte: Liegt ein Anhaltspunkt für eine unrichtige abgegebene Erklärung, eine Selbstanzeige oder ein Steuerstrafverfahren vor, und laufen Ermittlungen einer Aufsichtsbehörde? Beides gehört nach `DATENSCHUTZ.md` in die Zone Rot und damit nicht in das Werkzeug – auch nicht als Ja-Nein-Angabe.
2. Das Geschäftsmodell in eigenen Worten beschreiben, nicht die Marketingsprache der Internetseite übernehmen. Die Anbietereigenschaft entscheidet sich an der tatsächlich erbrachten Leistung.
3. Die beiden Felder zum Stand der Pflichterfüllung („Erstmalige Meldung bereits abgegeben", „Vorabinformation bereits versendet") vor dem Absenden mit dem Mandanten abgleichen und nicht schätzen – an ihnen hängt die Aussteuerungsregel.
4. Den Entwurf der Nutzerinformation nicht ungeprüft versenden: Er ist eine Textgrundlage. Die Fassung, die tatsächlich hinausgeht, wird gegen den Gesetzeswortlaut des § 13 KStTG und gegen die vorhandene Datenschutzinformation abgeglichen.
5. Den Versand so organisieren, dass sich der Zugang später belegen lässt, und den Nachweis zusammen mit der versendeten Textfassung ablegen.
6. Ergibt der Prompt, dass auch das PStTG greift, den dortigen Pflichtenkreis gesondert bearbeiten – die Fristen laufen unterschiedlich.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Verwendung prüfen: Stimmt die Zuordnung der tatsächlich erbrachten Leistungen zu den Begriffen des KStTG, ist der Empfängerkreis der Information richtig abgegrenzt, und deckt der Text alles ab, was § 13 KStTG verlangt?
- **Freigabe durch einen Berufsträger** für die Nutzerinformation und für jede Kommunikation mit dem Bundeszentralamt für Steuern (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Vier-Augen-Prinzip: Der Empfängerkreis der Information und der Zeitpunkt des Versands werden von einer Person festgelegt und von einer zweiten Person anhand des Gesetzeswortlauts und der Meldevorbereitung nachgeprüft und abgezeichnet** – der Zeitpunkt ist nicht nachholbar, und ein Versand nach der ersten Meldung erfüllt § 13 KStTG nicht mehr.
- **Fristen berechnet und erfasst ein Mensch.** Kein Datum aus der KI-Antwort übernehmen. Der Zeitpunkt der Vorabinformation ist an die erstmalige Meldung gekoppelt und deshalb im Fristenprogramm mit der Meldevorbereitung zu verknüpfen, nicht mit einem Kalendertag.
- **Prüfen, dass die Ausgabe das KStTG nicht als Entwurf bezeichnet.** Das Gesetz ist Art. 1 des Gesetzes zur Umsetzung der Richtlinie (EU) 2023/2226 vom 22.12.2025, BGBl. 2025 I Nr. 352, ausgegeben am 23.12.2025, in Kraft seit 24.12.2025 (für [JAHR] verifizieren).
- **Prüfen, dass die Ausgabe nicht behauptet, das CARF gelte in Deutschland oder das Vertragsgesetz zum CARF-MCAA sei verkündet.** Der Melderahmen stammt von der OECD; verbindlich wird er unionsrechtlich über DAC 8 und völkerrechtlich über die Mehrseitige Vereinbarung vom 26.11.2024, für die ein Vertragsgesetz erforderlich ist. Zum Stand 24.03.2026 lag dazu ein Referentenentwurf vor (für [JAHR] verifizieren).
- **Prüfen, dass DAC 8 nicht als unmittelbar geltendes Recht dargestellt wird.** Die Richtlinie (EU) 2023/2226 des Rates vom 17.10.2023 (ABl. L, 2023/2226, 24.10.2023) wirkt in Deutschland über das KStTG und die Änderungen von EUAHiG, FKAustG, AO, PStTG und FVG.
- Angaben zu Bußgeldern nur übernehmen, wenn die Norm am Gesetzestext nachgeschlagen wurde. Eine Bußgeldnorm des PStTG ist § 25 PStTG, nicht § 24 PStTG – diese Verwechslung ist in Vorlagen verbreitet.
- Der versendete Text und der Zugangsnachweis gehören in die Akte des Mandanten; die interne Einschätzung zur Betroffenheit bleibt intern.

## Varianten

- **Nur Betroffenheitsprüfung:** „Beschränke dich auf die Schritte 1 und 2 und gib statt des Entwurfs eine Liste der Angaben aus, die für die Entscheidung über die Anbietereigenschaft noch fehlen."
- **Anbieter mit Sitz im Ausland:** „Ergänze einen Schritt, in dem du prüfst, welche Anknüpfungspunkte des Sachverhalts eine Meldepflicht in Deutschland begründen könnten und welche Angaben dafür fehlen; triff keine Aussage über ausländisches Recht."
- **Doppelte Betroffenheit KStTG und PStTG:** „Erzeuge zusätzlich einen gemeinsamen Pflichtenkalender beider Gesetze mit Spalte ‚gilt für welchen Teil des Geschäftsmodells'."
- **Interne Verfahrensbeschreibung:** „Leite aus dem Ergebnis eine Arbeitsanweisung ab, die festlegt, wer die Vorabinformation auslöst, wer sie freigibt und wer den Zugang dokumentiert."
