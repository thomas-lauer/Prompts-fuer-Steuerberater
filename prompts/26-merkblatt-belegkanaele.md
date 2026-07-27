# 26 – Merkblatt Belegkanäle: verbindliche Regeln für den Mandanten

**Problem:** Derselbe Mandant liefert über Mail, Messenger, Portal und Papier – nichts ist zentral, Belege werden doppelt oder gar nicht erfasst, die Suche nach dem Original kostet mehr Zeit als die Buchung.
**Rolle:** Kanzleileitung, Buchhaltung, Sekretariat, Datenschutzbeauftragte
**DATEV-Bezug:** DATEV Unternehmen online (Belegtransfer, Kassenbuch), DATEV Meine Steuern, Kanzlei-Rechnungswesen, Eigenorganisation (Posteingang)
**Was du bereitstellen musst:** Anfallende Belegarten, heute genutzte Kanäle, die von der Kanzlei angebotenen und freigegebenen Kanäle, Umstellungstermin, technische Möglichkeiten des Mandanten.
**Datensparsamkeit:** Für den Entwurf Mandantenkürzel statt Klarname, keine Zugangsdaten, keine Portal-Links mit Kennungen, keine Mitarbeiternamen. Zugangsdaten nie per Mail und nie im selben Kanal wie das Merkblatt versenden. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du regelst die Zusammenarbeit zwischen einer deutschen Steuerkanzlei und ihren
Mandanten. Du schreibst Merkblätter, die befolgt werden: kurz, genau eine Regel
je Fall, Begründung aus Mandantensicht, Datum ab dem die Regel gilt.

AUFGABE
Erstelle ein verbindliches Merkblatt zu den Belegkanälen für EINEN Mandanten.

AUSGANGSLAGE
- Mandantenkürzel / Branche: [ANGABE]
- Belegarten, die anfallen:
  [LISTE, z. B. Eingangsrechnungen, Ausgangsrechnungen, Kontoauszüge,
   Kassenbelege, Verträge, Lohnunterlagen]
- Heute genutzte Wege: [z. B. Mail an zwei Adressen, Messenger, Portal,
  Papier im Ordner]
- Angebotene und freigegebene Kanäle: [z. B. DATEV Unternehmen online,
  DATEV Meine Steuern, Kanzlei-Mailadresse, Papierabgabe]
- Technische Möglichkeiten: [z. B. Belege-App, Scanner, Papier]
- Gewünschter Umstellungstermin: [DATUM]
- Ansprechpartner in der Kanzlei: [ROLLE]

ANFORDERUNGEN
1. Lege für JEDE Belegart genau EINEN zulässigen Kanal fest. Nie zwei
   gleichwertige Wege – die Wahlmöglichkeit ist die Ursache des Problems.
   Einzige Ausnahme: E-Rechnungen nach Nr. 3a.
2. Begründe jede Festlegung in einem Satz aus Sicht des MANDANTEN
   (weniger Rückfragen, Beleg jederzeit auffindbar), nicht aus Sicht der
   Kanzlei.
3. DATENSCHUTZ UND BERUFSRECHT: Messenger-Dienste (WhatsApp und
   vergleichbare) sind KEIN zulässiger Belegkanal, solange keine
   dokumentierte Freigabe der Kanzlei und keine wirksame Einwilligung
   vorliegen; Verschwiegenheitspflicht und Datenschutz stehen entgegen
   (§ 57 StBerG, § 203 StGB, DSGVO – Fundstellen für [JAHR] verifizieren).
   Formuliere das sachlich als Regel der Kanzlei, nicht als Vorwurf, in
   höchstens zwei Sätzen. Behaupte keine Bußgeldhöhen.
   Nimm zur E-Mail eine eigene Regel auf: Für welche Belegarten sie zulässig
   ist, dass Transportverschlüsselung Voraussetzung ist, dass Lohn- und
   personenbezogene Unterlagen über das Portal und nicht per E-Mail laufen,
   und dass Zugangsdaten nie per E-Mail übermittelt werden. Kennzeichne die
   zugrunde liegenden Anforderungen mit "Fundstelle – für [JAHR] verifizieren".
3a. E-RECHNUNGEN GESONDERT BEHANDELN. Für Eingangsrechnungen ist stets ein
    zweiter Weg vorzusehen: Rechnungen im strukturierten Format (XRechnung,
    ZUGFeRD) werden als Ursprungsdatei weitergeleitet, nicht als Ausdruck, Foto
    oder Scan. Halte fest: aufbewahrungspflichtig ist der strukturierte
    Datensatz (Rechtsstand und Fundstelle – für [JAHR] verifizieren). Diese
    Belegart ist von der Regel "genau ein Kanal" ausdrücklich ausgenommen, weil
    der Rechnungsaussteller das Format bestimmt.
4. Sage ausdrücklich, WAS MIT FALSCH EINGEREICHTEN BELEGEN PASSIERT –
   eine Regel ohne Folge wird nicht befolgt. Nenne eine Folge, die die
   Kanzlei durchhält (z. B. Hinweis auf den richtigen Weg, Erfassung erst
   im Folgemonat, gesonderte Abrechnung des Mehraufwands), und markiere sie
   als (Kanzleientscheidung – bitte bestätigen).
5. Nenne den Umstellungstermin und eine Übergangsregel für Belege, die
   vorher auf altem Weg eingegangen sind.
6. Merkblatt maximal EINE Seite, höchstens 350 Wörter, Sie-Form, jeder
   Fachbegriff in einem Halbsatz erklärt.
7. Nenne keine Aufbewahrungsfristen, Betragsgrenzen oder Paragrafen als
   feststehend, ohne "Stand – für [JAHR] verifizieren" zu ergänzen.
   Erfinde keine Programmfunktionen und keine Menüpfade; Unsicheres
   markierst du als (offen).
8. Nimm nur die angegebenen Belegarten auf. Ergänze nichts aus der Branche.

AUSGABEFORMAT
1. Merkblatt (max. 1 Seite): Überschrift – ein Satz Zweck – Tabelle
   Belegart | Weg | bis wann | warum – "Was nicht geht" (inkl. Messenger) –
   "Wenn ein Beleg anders ankommt" – Umstellungstermin – Ansprechpartner
2. Anschreiben zur Umstellung (max. 150 Wörter): warum jetzt, was sich für
   den Mandanten ändert, was er bis wann tun muss, Angebot einer Einweisung
3. Interne Notiz: welche Kanäle die Kanzlei ab dem Termin schließen muss,
   wer einweist, was bei Nichtbefolgung geschieht, offene Punkte
```

## Anwendung

1. Zuerst intern festlegen, welche Kanäle die Kanzlei anbietet – erst danach den Prompt ausfüllen. Ein Merkblatt, das mehr verspricht als die Kanzlei betreibt, verschärft das Problem.
2. Entwurf mit der betreuenden Sachbearbeitung durchgehen: Sie weiß, was realistisch ist.
3. Umstellungstermin mit Vorlauf setzen und mit einer Einweisung verbinden. Ohne sie fällt der Mandant nach zwei Wochen zurück.
4. Nach dem Termin die alten Kanäle schließen: Postfach umleiten, Messenger im Team einstellen, Papierabgabe nur nach Vereinbarung. Was noch funktioniert, wird benutzt.
5. Merkblatt in die Mandantenakte und ins Onboarding übernehmen.

## Qualitätssicherung

- **Merkblatt und Anschreiben sind Entwürfe und Mandantenkommunikation.** Vier-Augen-Prinzip: eine zweite Person liest gegen, die Freigabe erteilt der zuständige Berufsträger, bevor etwas hinausgeht (Freigabestufe 3 in `DATENSCHUTZ.md`).
- Prüfen, dass die E-Rechnungsregel nicht dazu führt, dass Mandanten Ausdrucke einreichen: aufbewahrungspflichtig ist der strukturierte Datensatz, nicht das Papier. Rechtsstand für [JAHR] verifizieren.
- Die Folge bei falscher Einreichung mandatsvertraglich und berufsrechtlich prüfen; "wir bearbeiten das nicht" kann Haftungsfragen auslösen und braucht die Freigabe des Berufsträgers.
- Prüfen, ob die Kanzlei die Regel selbst einhält – jede interne Ausnahme hebt das Merkblatt auf.
- Datenschutzrechtliche Aussagen durch die Datenschutzbeauftragte oder den Berufsträger gegenlesen lassen; Fundstellen nicht ungeprüft lassen.
- Prüfen, ob für die Kanäle Auftragsverarbeitung, Einwilligungen und Zugänge eingerichtet sind; Aussagen zum Verbleib der Originale fachlich prüfen.
- Bei angespanntem Mandat den Ton des Anschreibens prüfen – die Umstellung darf nicht wie eine Rüge klingen.

## Varianten

- **Kanzleiweite Fassung:** "Erzeuge eine mandantenneutrale Grundfassung, die je Mandant nur um die Belegarten ergänzt wird."
- **Nur Lohn:** "Beschränke das Merkblatt auf Lohnunterlagen mit dem Abrechnungsschluss als Stichtag."
- **Kombination:** Mit Prompt 17 verbinden – Belegkanal (Weg) und Zulieferkalender (Zeitpunkt) auf einem Blatt.
- **Nachfassen:** "Erzeuge eine Erinnerungsmail von höchstens 60 Wörtern für Mandanten beim alten Weg."
