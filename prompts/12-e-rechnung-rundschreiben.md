# 12 – Mandantenrundschreiben E-Rechnungspflicht

**Problem:** Die E-Rechnungspflicht betrifft jeden einzelnen Mandanten, der Erklärungsbedarf ist gleichförmig und riesig, und die Missverständnisse wiederholen sich. Gleichzeitig liest niemand ein fünfseitiges Rundschreiben.
**Rolle:** Steuerberater, Kanzleileitung
**DATEV-Bezug:** DATEV Unternehmen online, E-Rechnung, Kanzlei-Rechnungswesen
**Was du bereitstellen musst:** Mandantentyp, geschätzter Vorjahresumsatz, aktuelle Rechnungspraxis, verwendete Software.
**Datensparsamkeit:** Für ein Serienschreiben genügen Branche und Größenklasse. Namen erst beim Seriendruck aus der Kanzleisoftware einsetzen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du bist Steuerberater und informierst Mandanten über die E-Rechnungspflicht.
Du weißt, dass der häufigste Fehler das fünfseitige Informationsschreiben ist,
das niemand liest. Du schreibst kurz, konkret und handlungsbezogen.

AUFGABE
Erstelle ein Mandantenschreiben zur E-Rechnungspflicht für den folgenden
Mandantentyp.

MANDANTENPROFIL
- Branche: [z. B. Handwerk / Bau / Handel / Industrie / Freiberufler /
  Heilberuf / Vermietung / Gastronomie]
- Größenklasse: [Kleinstbetrieb / bis 800.000 € Vorjahresumsatz /
  über 800.000 € Vorjahresumsatz]
- Umsatzsteuerstatus: [Regelbesteuerung / Kleinunternehmer § 19 UStG /
  überwiegend steuerfreie Umsätze nach § 4 Nr. 8–29 UStG]
- Rechnungsstellung heute: [Papier / PDF per Mail / Fakturasoftware /
  bereits strukturiertes Format]
- Rechnungseingang heute: [Papier / PDF / gemischt / bereits digital]
- Eingesetzte Software: [ANGABE oder "unbekannt"]
- Belegweg zur Kanzlei: [DATEV Unternehmen online / Mail / Papier]

RECHTSSTAND, MIT DEM DU ARBEITEST
- Empfangspflicht: gilt seit 1.1.2025 für ALLE inländischen Unternehmer,
  ohne Übergangsfrist und ohne Ausnahme – auch für Kleinunternehmer,
  Vermieter und Heilberufe (§ 14 Abs. 1 UStG).
- Ausstellungspflicht: § 14 Abs. 2 UStG. Versandpflicht gestaffelt über die
  Übergangsvorschrift des § 27 Abs. 38 UStG: allgemeine Übergangsfrist bis
  31.12.2026; ab 1.1.2027 für Aussteller mit Vorjahresumsatz über 800.000 €;
  ab 1.1.2028 für alle. EDI-Sonderregelung bis 31.12.2027.
- Maßgeblich für den Stichtag 1.1.2027 ist der Gesamtumsatz des Vorjahres;
  die 800.000-€-Schwelle folgt aus § 27 Abs. 38 UStG.
- Kleinunternehmer sind von der AUSSTELLUNG dauerhaft befreit (§ 34a UStDV),
  von der Empfangspflicht nicht.
- Ausgenommen von der Ausstellungspflicht: Kleinbetragsrechnungen bis
  250 € brutto (§ 33 UStDV), Fahrausweise (§ 34 UStDV), steuerfreie Umsätze
  nach § 4 Nr. 8–29 UStG, B2C.
- Zulässige Formate: XRechnung, ZUGFeRD ab 2.0.1 und das inhaltsgleiche
  Factur-X – jeweils ohne die Profile MINIMUM und BASIC-WL –, Peppol BIS.
  Ein einfaches PDF ist KEINE E-Rechnung.
- Bei Hybridformaten ist der strukturierte XML-Teil führend; alle
  umsatzsteuerlichen Pflichtangaben müssen dort stehen. Die
  Leistungsbeschreibung im strukturierten Teil muss die Leistung eindeutig und
  leicht nachprüfbar erkennen lassen. Ergänzende Angaben (Aufmaße,
  Stundennachweise, Leistungsverzeichnisse) dürfen in einem IN der E-Rechnung
  enthaltenen Anhang stehen. Ein bloßer Verweis auf eine externe Anlage oder ein
  Link genügt NICHT.
- Weicht der Bildteil eines Hybridformats inhaltlich vom strukturierten Teil ab,
  kann er eine weitere Rechnung darstellen (§ 14c UStG prüfen). Der
  Vorsteuerabzug richtet sich stets nach dem strukturierten Teil.
- Aufbewahrung (§ 14b Abs. 1 UStG): der XML-Originaldatensatz unverändert und
  maschinell auswertbar, 8 Jahre, gerechnet ab dem Schluss des Kalenderjahrs,
  in dem die Rechnung ausgestellt wurde (für [JAHR] verifizieren). Bei
  Hybridformaten ist zumindest der strukturierte Teil unversehrt in
  ursprünglicher Form aufzubewahren. Ein Ausdruck genügt nicht.
Diese Angaben sind ein Arbeitsstand, kein geprüfter Rechtsstand. Setze hinter
JEDEN Stichtag, jeden Betrag, jede Schwelle und jede Frist, die du in
Anschreiben oder Anlage übernimmst, die Markierung "(für [JAHR] verifizieren)".
Führe in der internen Notiz jeden übernommenen Wert einzeln auf, mit der
Vorschrift, aus der er stammt. Erfinde keine zusätzlichen Fristen, Schwellen
oder Fundstellen.

ANFORDERUNGEN
1. Höchstens EINE Seite, etwa 350 Wörter. Alles Weitere gehört in die Anlage.
2. Beginne mit dem, was für DIESEN Mandanten gilt – nicht mit der Rechtslage
   allgemein. Erster Satz: was er tun muss und bis wann.
3. Trenne Empfangen und Versenden strikt und sichtbar. Das ist der
   Hauptirrtum: viele glauben, sie hätten bis 2028 Zeit, obwohl die
   Empfangspflicht seit Anfang 2025 gilt.
4. Sprich die drei Missverständnisse an, die zu diesem Profil passen.
   Auswahl: "PDF per Mail ist eine E-Rechnung" (falsch) ·
   "Als Kleinunternehmer bin ich raus" (nur vom Versand) ·
   "Ausdrucken und abheften reicht" (nein) ·
   "ZUGFeRD ist immer in Ordnung" (nicht MINIMUM und BASIC-WL) ·
   "Die 800.000 € beziehen sich auf meinen B2B-Umsatz / das laufende Jahr"
   (nein: Gesamtumsatz des Vorjahres).
   Formuliere sie als Klarstellung, nicht als Belehrung.
5. Ergänze branchenspezifisch:
   - Bau/Handwerk: Aufmaß, Abschlags- und Schlussrechnungen. Die
     handschriftliche Kürzung auf der Rechnung endet nicht zu einem festen
     Datum, sondern sobald DIESER Betrieb ausstellungspflichtig wird
     (1.1.2027 bei Gesamtumsatz Vorjahr über 800.000 €, sonst 1.1.2028 –
     für [JAHR] verifizieren). Ab dann gilt: Mindert sich nur die
     Bemessungsgrundlage (Skonto, Nachlass wegen Mängelrüge ohne Änderung
     der Leistung), ist keine Rechnungsberichtigung nötig. Ändert sich der
     Leistungsumfang (relevante Aufmaßänderung), ist zu berichtigen – bei
     vorheriger Vereinbarung auch durch Gutschrift des Auftraggebers mit
     Hinweis auf die Ursprungsrechnung (§ 14 Abs. 2, § 31 Abs. 5 UStDV –
     für [JAHR] verifizieren).
   - Handel/Industrie: bestehende EDI-Verfahren und deren Auslaufen.
   - Heilberufe, Vermieter, Freiberufler mit steuerfreien Umsätzen: Sie
     stellen ggf. keine E-Rechnungen aus, müssen aber empfangen und
     archivieren können.
   - Kleinstbetriebe: das Minimum, mit dem sie die Empfangspflicht erfüllen.
6. Schließe mit "Was wir für Sie tun" (2 Punkte) und "Was Sie tun sollten"
   (höchstens 3 Punkte, jeder mit Frist).
7. Erzeuge zusätzlich eine ANLAGE als Tabelle: Stichtag | Wer ist betroffen |
   Was gilt.
8. Erzeuge zusätzlich eine INTERNE NOTIZ: welche Angaben zu diesem Mandanten
   die Kanzlei vor dem Versand prüfen muss, und welche Rechtsstände seit
   deinem Wissensstand geändert worden sein könnten.
9. Keine Paragrafen im Fließtext. Rechtsgrundlagen nur in der Anlage – dort
   aber vollständig: Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage,
   jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde keine Paragrafen;
   bist du unsicher, schreibe "Fundstelle offen – bitte recherchieren".

AUSGABEFORMAT
Anschreiben – Anlage Stichtagstabelle – Interne Notiz.
```

## Anwendung

1. Einmal je Mandantentyp erzeugen (Bau, Handel, Heilberuf, Kleinunternehmer, Vermietung) und als Serienbrief-Vorlage ablegen.
2. Größenklasse nach dem Gesamtumsatz des **Vorjahres** bestimmen – für den Stichtag 1.1.2027 also nach dem Umsatz 2026.
3. Mandanten, die 2026 knapp über 800.000 € liegen, gesondert kennzeichnen und persönlich ansprechen.
4. Anlage als eigenes Blatt beilegen, nicht in den Fließtext ziehen.

## Qualitätssicherung

- **Rechtsstand vor dem Versand prüfen.** Fristen, die 800.000-€-Schwelle und die Formatvorgaben waren zuletzt stabil, aber ein Serienbrief an den ganzen Mandantenstamm ist der falsche Ort für einen veralteten Stand. Prüfen an: BMF-Schreiben zur obligatorischen E-Rechnung (15.10.2024 und 15.10.2025) sowie am FAQ-Katalog der Bundessteuerberaterkammer.
- Prüfen, ab welchem Stichtag DIESER Baumandant selbst ausstellungspflichtig ist – davon hängt der ganze Absatz ab.
- Prüfen, ob die Kanzlei die unter "Was wir für Sie tun" versprochenen Leistungen auch erbringt – und ob sie im Honorar enthalten sind.
- **Freigabe durch einen Berufsträger vor dem Versand, ausnahmslos** (Freigabestufe 3 in `DATENSCHUTZ.md`). Das Schreiben geht an den gesamten Mandantenstamm; ein Fehler vervielfältigt sich. Vier-Augen-Prinzip: Anschreiben und Anlage werden von einer zweiten Person gegen den geprüften Rechtsstand abgeglichen.
- Jeden mit "(für [JAHR] verifizieren)" markierten Wert einzeln nachschlagen und die Markierung erst dann entfernen. Keine Frist und kein Datum aus der KI-Antwort ungeprüft übernehmen.

## Varianten

- **Persönliches Gespräch statt Rundschreiben:** "Erzeuge daraus einen Gesprächsleitfaden mit fünf Fragen, die ich dem Mandanten stelle, und den passenden Antworten."
- **FAQ für die Kanzleiwebsite:** "Erzeuge daraus 10 Fragen und Antworten, je Antwort höchstens 60 Wörter."
- **Nachfassschreiben:** "Erzeuge ein kurzes Nachfassschreiben an Mandanten, die auf das erste Schreiben nicht reagiert haben."
- **Checkliste zum Abhaken:** "Erzeuge eine einseitige Checkliste, mit der der Mandant seine Bereitschaft selbst prüfen kann."
