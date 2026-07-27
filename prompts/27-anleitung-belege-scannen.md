# 27 – Kurzanleitung: So reichen Sie Belege richtig ein

**Problem:** Mandanten fotografieren Belege schief, unscharf und mit Schatten, Thermopapier ist beim Eintreffen verblasst; die Belegerkennung scheitert und jeder Beleg muss von Hand nachgearbeitet werden.
**Rolle:** Sekretariat, Buchhaltung, Kanzleileitung (Mandantenkommunikation)
**DATEV-Bezug:** DATEV Unternehmen online, Belegtransfer, DATEV Upload mobil / Upload online, Belegbilderservice
**Was du bereitstellen musst:** Übermittlungsweg des Mandanten, Mandantentyp und Belegaufkommen, kanzleieigene Vorgaben zu Dateibenennung und Ordnerstruktur, bekannte Fehlerbilder aus der bisherigen Zusammenarbeit.
**Datensparsamkeit:** Keine echten Belege in den Prompt geben. Für die Anleitung genügen Beschreibungen der Fehlerbilder ("Foto schräg, rechter Rand fehlt"). Mandantenname und Ansprechpartner erst im fertigen Dokument einsetzen, nicht im Prompt (`Mandant A`). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist erfahrene Kanzleimitarbeiterin und schreibst Mandantenanleitungen.
Dein Stil: Sie-Form, kurze Sätze, keine Vorwürfe, jeder Punkt sagt, was zu
tun ist – nicht, was falsch war.

AUFGABE
Schreibe eine Kurzanleitung "So reichen Sie Ihre Belege richtig ein" für
[MANDANT]. Umfang: maximal eine DIN-A4-Seite.

RAHMEN
- Übermittlungsweg: [DATEV Unternehmen online / Upload mobil / Belegtransfer /
  E-Mail an Kanzlei-Postfach]
- Erfassungsgerät des Mandanten: [Smartphone / Dokumentenscanner / beides]
- Belegarten: [z. B. Kassenbons, Eingangsrechnungen, Tankquittungen, Bewirtung]
- Belegaufkommen pro Monat: [ZAHL]
- Bisher aufgetretene Fehlerbilder: [FEHLERBILDER]
- Kanzleivorgabe Dateibenennung: [SCHEMA ODER "keine"]

INHALT – DIESE ABSCHNITTE SIND PFLICHT
1. Aufnahme: einfarbiger, kontrastierender Untergrund; gleichmäßiges Licht
   ohne Schatten und ohne Blitzreflexe; Kamera parallel über dem Beleg,
   nicht schräg; alle vier Ecken und Ränder im Bild; ein Beleg je Bild.
2. Thermopapier (Kassenbons, Tankquittungen): Erfassen Sie diese Belege am Tag
   des Erhalts. Die Schrift verblasst, und der Beleg muss über die gesamte
   Aufbewahrungsfrist lesbar bleiben – deshalb ist die lesbare Zweitausfertigung
   (Scan oder Kopie) der Beleg, auf den es ankommt. Nicht knicken, nicht in die
   Sonne, nicht ins heiße Auto. Ob das Papieroriginal danach vernichtet werden
   darf, richtet sich nach der Verfahrensdokumentation der Kanzlei; markiere
   diese Aussage mit (VON DER KANZLEI ZU PRÜFEN).
2a. Elektronische Rechnungen: Leiten Sie eine Rechnung, die Sie als Datei
    erhalten (PDF, XML, ZUGFeRD, XRechnung), immer als Originaldatei weiter –
    nie als Ausdruck, nie als Foto des Ausdrucks, nie als Screenshot. Beim
    Ausdrucken geht der Teil verloren, der aufbewahrt werden muss.
    (Rechtsstand – für [JAHR] verifizieren)
3. Mehrseitige Rechnungen: alle Seiten, in richtiger Reihenfolge, als EIN
   Dokument – nicht als mehrere Einzelbilder.
3a. Angaben, die Sie VOR dem Fotografieren auf oder zum Beleg ergänzen: Nenne je
    angegebener Belegart, was ergänzt werden muss (bei Bewirtung Anlass und
    Teilnehmer, bei Fahrtkosten Zweck und Strecke, bei Barbelegen der
    Zahlungsweg). Nenne KEINE Betragsgrenzen und keine Paragrafen ohne den Zusatz
    "für [JAHR] verifizieren". Weise darauf hin, dass ergänzende Angaben zum
    Beleg gehören und nicht per Nachricht hinterhergeschickt werden.
4. Dateiformat und Benennung: [FORMATVORGABE], Benennungsschema
   [SCHEMA], keine Sonderzeichen.
5. Was Sie NICHT schicken sollten – mit je einem Halbsatz Begründung:
   Screenshots von E-Mails statt der angehängten Rechnung, abfotografierte
   Bildschirme, Sammelfotos mit mehreren Belegen, Belege in Schutzhüllen.
6. Aufbewahrung: Formuliere einen Absatz, der DREI Punkte trennt:
   (a) welche Unterlagen nach dem Scannen vernichtet werden dürfen,
   (b) dass die Vernichtung eine Verfahrensdokumentation zum ersetzenden Scannen
       voraussetzt,
   (c) welche Unterlagen im Original bleiben müssen, weil eine andere Vorschrift
       das verlangt – u. a. Eröffnungsbilanz und Jahresabschluss (§ 257 HGB,
       § 147 Abs. 2 AO), Zollpapiere, notarielle Urkunden, Wertpapiere.
   Nenne die Fundstellen mit dem Zusatz "für [JAHR] verifizieren". Markiere den
   gesamten Absatz mit (VON DER KANZLEI ZU PRÜFEN) und nenne, was die Kanzlei
   vor dem Versand festlegen muss.

ANFORDERUNGEN
1. Erkläre jeden Fachbegriff in einem Halbsatz in Klammern.
2. Formuliere handlungsorientiert: "Legen Sie den Beleg auf ...",
   nicht "Belege sollten ... werden".
3. Nenne KEINE konkreten Fristen, Betragsgrenzen oder Rechtsstände, ohne
   sie als "für [JAHR] verifizieren" zu kennzeichnen. Erfinde keine
   Paragrafen und keine BMF-Schreiben; unsichere Fundstellen kennzeichnest
   du mit "Fundstelle – für [JAHR] verifizieren".
4. Kennzeichne jede Aussage zur technischen Funktionsweise des genannten
   Übermittlungswegs, bei der du dir nicht sicher bist.

AUSGABEFORMAT
1. Anleitung (max. 1 Seite, nummerierte Abschnitte)
2. Kurzfassung "Die 5 Regeln" – fünf Zeilen zum Aushängen an der Kasse
   oder im Lager, je Zeile maximal 12 Wörter
3. Interne Notiz für die Kanzlei: was vor dem Versand zu prüfen oder zu
   ergänzen ist, welche Angaben gefehlt haben
4. Was ich nicht sicher weiß
```

## Anwendung

1. Fehlerbilder aus den letzten Monaten sammeln, bevor der Prompt läuft – die Anleitung wirkt nur, wenn sie die tatsächlichen Fehler dieses Mandanten adressiert.
2. Ergebnis auf eine Seite kürzen. Alles, was auf Seite 2 rutscht, wird nicht gelesen.
3. Die 5-Regeln-Kurzfassung getrennt ausdrucken und dem Mandanten laminiert oder als Bild fürs Smartphone mitgeben.
4. Beim nächsten Belegeingang stichprobenartig kontrollieren und die Anleitung nach drei Monaten nachschärfen.

## Qualitätssicherung

- **Die Anleitung ist ein Entwurf und Mandantenkommunikation.** Vier-Augen-Prinzip: eine zweite Person liest gegen, die Freigabe erteilt der zuständige Berufsträger, bevor die Anleitung hinausgeht (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Der Aufbewahrungsabsatz geht nicht ungeprüft raus.** Vor dem Versand festlegen: ob eine Verfahrensdokumentation zum ersetzenden Scannen vorliegt, für welche Belegarten Vernichtung danach zugelassen wird und welche Unterlagen im Original bleiben, weil eine andere Vorschrift das verlangt. Fundstellen für [JAHR] verifizieren. Freigabe durch einen Berufsträger.
- **Thermopapier:** Prüfen, dass die Anleitung nicht pauschal die Aufbewahrung des Papieroriginals verlangt. Maßgeblich ist die lesbare Zweitausfertigung; über das Papier entscheidet die Verfahrensdokumentation.
- **E-Rechnung:** Prüfen, dass die Anleitung den Mandanten nicht zum Ausdrucken elektronischer Rechnungen anleitet. Aufbewahrungspflichtig ist der strukturierte Datensatz.
- Technische Angaben zum Übermittlungsweg gegen die aktuelle DATEV-Hilfe prüfen; Bezeichnungen und Bedienschritte ändern sich mit Programmversionen.
- Formatvorgaben (Dateityp, Auflösung, maximale Dateigröße) aus den Kanzleivorgaben übernehmen, nicht aus der KI-Antwort.
- Anleitung von einer Person gegenlesen lassen, die den Übermittlungsweg nicht kennt.

## Varianten

- **Branchenfassung:** Zusatz "Ergänze Beispiele aus der Branche [BRANCHE] (z. B. Handwerk: Materialbelege von der Baustelle, Gastronomie: Wareneingang)."
- **Bilderanleitung:** "Erzeuge zusätzlich eine Liste von 6 Bildmotiven, die wir für eine bebilderte Fassung fotografieren sollten – je Motiv ein Satz Bildunterschrift."
- **Onboarding:** Anleitung fest in die Mandatsaufnahme aufnehmen, gemeinsam mit Prompt 26 zur Einrichtung des digitalen Belegwegs.
- **Mitarbeiterfassung:** "Formuliere dieselben Regeln als interne Arbeitsanweisung für Mitarbeitende, die Belege beim Mandanten vor Ort erfassen."
