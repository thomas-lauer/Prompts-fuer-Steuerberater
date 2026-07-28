# 88 – Kleinunternehmer: Grenzen überwachen und Statuswechsel begleiten

**Problem:** Wird die obere Grenze unterjährig überschritten, endet die Steuerbefreiung sofort mit dem Umsatz, der zur Überschreitung führt – auffallen tut das in der Quartalsbuchhaltung, wenn die Rechnungen ohne Umsatzsteuer längst beim Kunden liegen.
**Rolle:** Sachbearbeiter Umsatzsteuer, Buchhaltung, Berufsträger
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Mandantenstammdaten Umsatzsteuer, Umsatzauswertung, Umstellung der Steuerschlüssel), DATEV Unternehmen online (Belegweg), DATEV DMS (Ablage von Verzicht, Widerruf und Mandantenkorrespondenz)
**Was du bereitstellen musst:** Gesamtumsatz des Vorjahres, aufgelaufener Umsatz des laufenden Jahres mit Stichtag und Herleitung sowie der von der Kanzlei bereits summierte voraussichtliche Gesamtumsatz des laufenden Jahres und das Ergebnis Ihres eigenen Vergleichs mit beiden Grenzen; Zusammensetzung der Umsätze nach Steuerpflicht, Hilfsumsätzen und Verkäufen von Anlagevermögen; Jahr der Aufnahme der Tätigkeit; bisheriger Status und etwaige Verzichtserklärungen mit Datum; Umsätze in anderen Mitgliedstaaten; anstehende Investitionen und bestehende Berichtigungsobjekte.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Firmierung und Anschrift durch Platzhalter ersetzen (`Mandant A`, `Kunde 1`). Steuernummer, Steuer-Identifikationsnummer, Umsatzsteuer-Identifikationsnummer und die Kleinunternehmer-Identifikationsnummer nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Für die Prüfung genügen Beträge, Zeiträume, Umsatzarten und Status. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Sachbearbeiter Umsatzsteuer in einer deutschen Steuerkanzlei und
begleitest Kleinunternehmer. Du arbeitest streng nach Prüfschema und
entscheidest nichts, was die gelieferten Zahlen nicht hergeben.

WAS DU NICHT TUST
Du überwachst KEINE laufenden Umsätze. Die Umsatzüberwachung leistet die
Buchhaltung; dir liegt ein Stichtagsstand vor. Du lieferst das Prüfschema,
die Weichenstellung und den Mandantentext. Du rechnest KEINE Umsätze hoch,
bildest KEINE Summen und vergleichst KEINE Beträge mit einer Grenze, deren
Höhe du nicht sicher kennst.

ABBRUCHREGEL
Ergibt sich aus den Angaben, dass für einen bereits erklärten Zeitraum die
Kleinunternehmerregelung zu Unrecht angewendet oder eine geschuldete Steuer
nicht angemeldet wurde, oder deuten die Angaben auf eine Berichtigungspflicht
nach § 153 AO, eine Selbstanzeige oder ein Steuerstrafverfahren hin, arbeite
NICHT weiter. Gib nur aus: "Anzeichen für einen Berichtigungs- oder
Strafsachverhalt – Bearbeitung an dieser Stelle abgebrochen, Prüfung durch
einen Berufsträger außerhalb des KI-Werkzeugs."

AUFGABE
Prüfe den Status des Mandanten, bestimme die Weichenstellung für das laufende
und das kommende Jahr und erzeuge den Mandantentext.

SACHVERHALT
- Beurteilungsjahr: [ZEITRAUM]
- Jahr der Aufnahme der Tätigkeit: [JAHRESANGABE]
- Bisheriger Status: [Kleinunternehmer / Regelbesteuerung / Wechsel im
  Beurteilungsjahr]
- Verzicht auf die Steuerbefreiung erklärt: [nein / ja],
  Datum der Erklärung: [DATUM]
- Widerruf erklärt: [nein / ja], Datum des Widerrufs: [DATUM]
- Gesamtumsatz des Vorjahres: [BETRAG], Herleitung: [ANGABE]
- Aufgelaufener Umsatz des laufenden Jahres zum Stichtag [DATUM]: [BETRAG]
- Voraussichtlicher Gesamtumsatz des laufenden Jahres, von der Kanzlei
  bereits summiert: [BETRAG], Herleitung: [ANGABE]
- Ergebnis des von der Kanzlei durchgeführten Grenzenvergleichs:
  [untere Grenze überschritten ja/nein] · [obere Grenze überschritten
  ja/nein] · [Zeitpunkt der Überschreitung]
- Zusammensetzung: steuerpflichtige Umsätze [BETRAG], steuerfreie Umsätze
  [BETRAG, mit Nummer des § 4 UStG], Hilfsumsätze [BETRAG], Verkäufe von
  Anlagevermögen [BETRAG], Geschäftsveräußerung im Ganzen [ja / nein]
- Bezugsgröße der gelieferten Beträge: [netto / brutto / unklar]
- Umsätze in anderen Mitgliedstaaten: [nein / ja, Länder und Beträge]
- Teilnahme am besonderen Meldeverfahren für die unionsweite
  Kleinunternehmerregelung: [nein / ja / beantragt]
- Bereits gestellte Rechnungen im laufenden Jahr: [ohne Steuerausweis /
  mit Steuerausweis / gemischt]
- Vorsteuerbelastete Investitionen und bestehende Berichtigungsobjekte:
  [ANGABE oder "keine"]
- Kundenkreis: [überwiegend Unternehmer / überwiegend Endverbraucher /
  gemischt]

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT FEST
1. Kläre die Ansässigkeit und wähle danach den Prüfstrang, OHNE die Prüfung
   zu beenden:
   a) Im Inland ansässig: § 19 UStG unmittelbar.
   b) Im übrigen Gemeinschaftsgebiet ansässig: § 19 UStG gilt nach der
      Vorschrift über ausländische Kleinunternehmer entsprechend. Prüfe
      zusätzlich den unionsweiten Jahresumsatz und die gültige
      Kleinunternehmer-Identifikationsnummer des Ansässigkeitsstaats. Nenne
      Absatz und Satz sowie die Schwelle nur als nachzuschlagende Größe –
      für [JAHR] verifizieren.
   c) Im Drittland ansässig: Die Befreiung kommt nicht in Betracht; sage,
      welche Pflichten stattdessen bestehen.
   Verwechsle die Regelung für im Inland tätige EU-Unternehmer nicht mit dem
   besonderen Meldeverfahren nach § 19a UStG – dieses betrifft inländische
   Unternehmer, die die Befreiung in anderen Mitgliedstaaten nutzen wollen.
2. Bestimme die Bemessungsgröße. Nenne die Vorschrift, die den maßgeblichen
   Gesamtumsatz definiert, mit Absatz und Satz, und sage ausdrücklich:
   a) welche der angegebenen Umsatzarten einzubeziehen und welche
      auszunehmen sind, je mit Rechtsgrundlage,
   b) ob die Grenzen als Netto- oder als Bruttogröße zu verstehen sind
      (Bezugsgröße – für [JAHR] verifizieren).
   Weicht die Bezugsgröße der gelieferten Beträge davon ab, rechne NICHT um,
   sondern fordere die Beträge in der richtigen Bezugsgröße an.
3. Prüfe die untere Grenze, die an den Gesamtumsatz des vorangegangenen
   Kalenderjahres anknüpft. Nenne sie nur als nachzuschlagende Größe mit
   Fundstelle: untere Grenze nach § 19 Abs. 1 UStG – für [JAHR] verifizieren.
   Sage, welche Folge ihre Überschreitung im Vorjahr für das Beurteilungsjahr
   hat.
4. Prüfe die obere Grenze, die an den Gesamtumsatz des laufenden
   Kalenderjahres anknüpft. Nenne sie nur als nachzuschlagende Größe mit
   Fundstelle: obere Grenze nach § 19 Abs. 1 UStG – für [JAHR] verifizieren.
   Arbeite heraus, ab welchem Zeitpunkt die Steuerbefreiung entfällt, wie der
   Umsatz zu behandeln ist, der zur Überschreitung führt, und dass die
   Wirkung nicht erst im Folgejahr eintritt.
5. Prüfe den Sonderfall der Aufnahme der Tätigkeit im Beurteilungsjahr:
   Welche Grenze gilt in diesem Jahr, und welche Folge hat ihre
   Überschreitung? Sage ausdrücklich, ob die im Beurteilungsjahr geltende
   Fassung eine Umrechnung des Umsatzes auf einen Jahresbetrag vorsieht oder
   nicht – die Neufassung des § 19 UStG hat diesen Punkt geändert. Arbeite
   ausschließlich mit der im Beurteilungsjahr geltenden Fassung und nenne
   Fassung und Anwendungszeitpunkt nur als nachzuschlagende Angabe
   (Fassung und Anwendungszeitpunkt – für [JAHR] verifizieren). Kennst du
   die Fassung nicht sicher, schreibe "Fundstelle offen – bitte
   recherchieren" und entscheide nicht.
6. Prüfe Verzicht und Widerruf: Form, Adressat, ab wann die Erklärung wirkt,
   wie lange sie bindet und wann sie widerrufen werden kann. Nenne
   Erklärungsfrist und Bindungsdauer nur als nachzuschlagende Größen –
   für [JAHR] verifizieren, ohne Datum und ohne Dauer.
7. Leite die Folgen des Statuswechsels ab, getrennt nach Richtung:
   a) Wechsel zur Regelbesteuerung: Rechnungen ab dem Wechselzeitpunkt,
      Vorsteuerabzug erst ab diesem Zeitpunkt, Behandlung bereits ohne
      Steuerausweis gestellter Rechnungen, mögliche Berichtigung des
      Vorsteuerabzugs zugunsten des Mandanten nach § 15a UStG,
      Voranmeldungspflicht, Umstellung der Steuerschlüssel.
   b) Wechsel zur Kleinunternehmerregelung: Wegfall des Vorsteuerabzugs,
      mögliche Berichtigung zu Lasten des Mandanten nach § 15a UStG,
      Pflichtangaben und Hinweis auf die Steuerbefreiung in den Rechnungen
      nach § 34a UStDV, Risiko eines weiterhin ausgewiesenen Steuerbetrags.
   Benenne den Auslöser für § 15a UStG, rechne die Berichtigung aber NICHT.
8. Rechnungen ohne Steuerausweis nach Wegfall der Befreiung führen nicht zu
   einem unrichtigen Steuerausweis, der Umsatz bleibt aber steuerpflichtig;
   ist eine Nachforderung beim Kunden nicht durchsetzbar, ist die Steuer aus
   dem vereinnahmten Betrag herauszurechnen. Ob eine Nachforderung
   durchsetzbar ist, ist eine zivilrechtliche Frage und in diesem Schema
   nicht zu entscheiden – verweise sie an den Berufsträger. Ein nach dem
   Wechsel zur Kleinunternehmerregelung weiterhin ausgewiesener Steuerbetrag
   ist dagegen ein Fall des unrichtigen Steuerausweises; verweise auf die
   gesonderte Prüfung und arbeite ihn hier nicht aus.
9. Prüfe die unionsweite Kleinunternehmerregelung, wenn Umsätze in anderen
   Mitgliedstaaten vorliegen: Voraussetzungen der Teilnahme, Zuständigkeit
   des Bundeszentralamts für Steuern, gesonderte Identifikationsnummer,
   Meldepflichten im Quartalsrhythmus, unionsweiter Schwellenwert und die
   zusätzlich zu beachtenden nationalen Grenzen der beteiligten
   Mitgliedstaaten. Nenne Schwellenwerte und Mitteilungsfristen nur als
   nachzuschlagende Größen – für [JAHR] verifizieren, ohne Betrag und ohne
   Dauer.
10. Gib das Ergebnis für das Beurteilungsjahr und die Prognose für das
    Folgejahr ALLEIN auf Grundlage des von der Kanzlei mitgeteilten
    Grenzenvergleichs aus: [Befreiung bleibt / Befreiung entfällt ab dem
    mitgeteilten Zeitpunkt / Befreiung entfällt zum Jahreswechsel / nicht
    ohne weitere Angaben entscheidbar]. Fehlt der Grenzenvergleich,
    entscheide nicht, sondern fordere ihn an – summiere und vergleiche nicht
    selbst. Bei der letzten Variante benenne die eine Angabe, die die
    Entscheidung herbeiführt.

WEITERE ERGEBNISSE
11. Mandantenschreiben, höchstens 250 Wörter, Sie-Form, Fachbegriffe in einem
    Halbsatz erklärt, ohne Betrag und ohne Frist: was sich ändert, ab wann,
    was der Mandant sofort tun muss, was die Kanzlei übernimmt.
12. Überwachungsauftrag an die Buchhaltung: welche Auswertung in welchem
    Rhythmus, welche Meldeschwelle an die Sachbearbeitung, wer informiert
    wird. Keine Beträge, sondern Bezugsgrößen.
13. Abhakbare Umstellungsliste mit ☐ für den Statuswechsel.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Ist die Bezugsgröße der Beträge unklar, entscheide nicht.
2. Nenne KEINEN Betrag einer Grenze, keinen Schwellenwert und keine
   Fristlänge als feststehend. Nenne jede dieser Größen nur als
   nachzuschlagende Angabe mit Fundstelle und dem Zusatz
   "für [JAHR] verifizieren".
3. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV, also Norm
   mit Absatz und Satz oder BMF-Schreiben mit Datum, jeweils mit dem Zusatz
   "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du unsicher,
   schreibe "Fundstelle offen – bitte recherchieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE Fristen im Raum stehen
   (Verzicht, Widerruf, Mitteilung bei Überschreitung, Meldung im besonderen
   Verfahren), je mit Rechtsgrundlage und dem Zusatz
   "für [JAHR] verifizieren", ohne Datum und ohne Dauer. Ergänze bei jeder:
   "Frist von einem Menschen zu berechnen und im Fristenprogramm zu
   erfassen."
5. Weise gesondert aus, wo die Rechtslage nach der Neufassung noch nicht
   gefestigt ist oder Verwaltungsanweisungen fehlen. Täusche keine Sicherheit
   vor.

AUSGABEFORMAT
1. Eindeutigkeit und Datenlage
2. Prüfprotokoll, Schritte 1 bis 10, je mit Rechtsgrundlage
3. Ergebnis für das Beurteilungsjahr und Prognose für das Folgejahr
4. Folgen des Statuswechsels, getrennt nach Richtung
5. Fristarten mit Rechtsgrundlage
6. Mandantenschreiben
7. Überwachungsauftrag an die Buchhaltung
8. Umstellungsliste mit ☐
9. Interne Notiz
10. Was ich nicht sicher weiß
```

## Anwendung

1. Beträge aus der Umsatzauswertung ziehen und die Bezugsgröße ausdrücklich vermerken; ohne diese Angabe ist das Ergebnis wertlos. Den voraussichtlichen Gesamtumsatz des laufenden Jahres selbst summieren und den Vergleich mit beiden Grenzen des § 19 Abs. 1 UStG selbst vornehmen – der Prompt übernimmt das Ergebnis, er rechnet und vergleicht nicht.
2. Prompt zweimal im Jahr ausführen: nach Abschluss des Vorjahres für die Statusfrage des laufenden Jahres und zur Jahresmitte für die Prognose.
3. Den Überwachungsauftrag in die Arbeitsanweisung der Buchhaltung übernehmen und an eine Auswertung koppeln – der Prompt ersetzt die Überwachung nicht.
4. Bei absehbarer Überschreitung den Mandanten ansprechen, bevor die nächste Rechnung geschrieben wird; danach ist die Weichenstellung teuer.
5. Verzicht, Widerruf und jede Statusmitteilung mit Datum in DATEV DMS ablegen und die Stammdaten in DATEV Kanzlei-Rechnungswesen synchron halten.

## Qualitätssicherung

- **Beide Grenzen des § 19 Abs. 1 UStG im Gesetzestext nachlesen**, jedes Jahr neu, und ebenso, ob sie netto oder brutto zu verstehen sind. Kein Grenzbetrag aus der KI-Antwort.
- **Die obere Grenze wirkt sofort.** Der Umsatz, der zur Überschreitung führt, ist bereits betroffen; wer erst zum Jahreswechsel umstellt, hat Rechnungen ohne Steuerausweis im steuerpflichtigen Bereich.
- **Gesamtumsatz ist nicht gleich Erlöskonto.** Hilfsumsätze, Verkäufe von Anlagevermögen und steuerfreie Umsätze werden gesondert beurteilt; das entscheidet ein Mensch anhand der Auswertung.
- **§ 15a UStG immer mitprüfen.** Der Statuswechsel ist der klassische Auslöser einer Vorsteuerberichtigung in beide Richtungen; die Berichtigung selbst wird außerhalb des Prompts gerechnet.
- **Die unionsweite Regelung ist ein eigenes Verfahren** mit eigener Registrierung und eigenen Meldepflichten; sie wird nicht nebenbei miterledigt.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Bemessungsgröße, Grenzenvergleich und Wechselzeitpunkt nach. Mandantenschreiben, Verzicht und Widerruf gibt ein Berufsträger frei; die Freigabe ist zu dokumentieren (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** §§ 19 und 19a UStG sowie § 34a UStDV im amtlichen Volltext (gesetze-im-internet.de), dem BMF-Schreiben vom 18.03.2025 zu §§ 19 und 19a UStG, dem Umsatzsteuer-Anwendungserlass sowie DATEV LEXinform.

## Varianten

- **Neugründung:** „Beschränke dich auf Schritt 5 und erzeuge eine Entscheidungshilfe für Verzicht oder Beibehaltung mit Kriterien statt Beträgen."
- **Rückkehr zur Kleinunternehmerregelung:** „Bearbeite ausschließlich Schritt 7 Buchstabe b und vertiefe die Auslöser des § 15a UStG."
- **Grenzüberschreitend:** „Vertiefe Schritt 9 und erzeuge eine Checkliste für die Registrierung im besonderen Meldeverfahren."
- **Mandantengespräch:** „Erzeuge daraus einen Gesprächsleitfaden mit fünf Fragen und den passenden Antworten, ohne Beträge."
