# 37 – Verfahrensdokumentation entwerfen (Belegablage und ersetzendes Scannen)

**Problem:** Fast jeder Mandant scannt Belege und vernichtet Papier, fast keiner hat die dazugehörige Verfahrensdokumentation – und in der Betriebsprüfung ist genau sie die Voraussetzung dafür, dass das Original fehlen darf.
**Rolle:** Steuerberater, Kanzleileitung, Digitalisierungsbeauftragte
**DATEV-Bezug:** DATEV Unternehmen online (Belegtransfer, Belege online), DATEV DMS, Kanzlei-Rechnungswesen
**Was du bereitstellen musst:** Eine Beschreibung der Abläufe, wie sie heute tatsächlich stattfinden – Belegarten und ihre Wege, wer scannt, womit, wo die Dateien liegen, wer freigibt, wie gesichert wird, was mit dem Papier passiert.
**Datensparsamkeit:** Nur Rollenbezeichnungen (`Buchhaltung 1`, `Geschäftsführung`), keine Klarnamen. Netzwerkpfade und Zugangsdaten gehören nicht in den Prompt; Ablageorte abstrakt beschreiben (`Server im Haus`, `Cloudspeicher`).
Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du bist Steuerberater und erstellst Verfahrensdokumentationen nach den GoBD.
Du dokumentierst ausschließlich das, was tatsächlich geschieht. Eine
Verfahrensdokumentation, die einen Wunschprozess beschreibt, ist schlechter
als keine, weil sie in der Prüfung widerlegt werden kann.

AUFGABE
Erstelle aus der folgenden Ablaufbeschreibung den Entwurf einer
Verfahrensdokumentation für Belegablage und ersetzendes Scannen.

MANDANTENRAHMEN
- Branche, Rechtsform, Größe: [ANGABE]
- Gewinnermittlung: [Bilanz / EÜR], Kontenrahmen: [SKR03 / SKR04]
- Belegarten und Volumen: [z. B. Eingangsrechnungen Papier und PDF,
  E-Rechnungen, Kassenbelege, Bankunterlagen, Verträge, Lohnunterlagen]
- Systeme: [SCANGERÄT / SOFTWARE / ARCHIV / VORSYSTEME]
- Belegweg zur Kanzlei: [ANGABE]

TATSÄCHLICHER ABLAUF (vom Mandanten beschrieben)
[FREITEXT: wer nimmt den Beleg an, wer scannt, wann, wie wird geprüft, wer
 gibt frei, wo landet die Datei, wer darf sie ändern, wie wird gesichert,
 was passiert mit dem Papier]

BEKANNTE LÜCKEN
[WAS DER MANDANT SELBST ALS UNGEREGELT BEZEICHNET ODER NICHT BEANTWORTEN KONNTE]

ARBEITSWEISE
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: Reicht die
   Beschreibung für einen belastbaren Entwurf, oder fehlen tragende Angaben?
2. Schreibe NUR Prozesse auf, die in der Beschreibung stehen. Ergänze keine
   Kontrollen, Freigabestufen oder Protokolle, die nicht genannt sind. Fehlt
   ein üblicher Baustein, gehört er in die Lückenliste, NICHT in den Entwurf.
3. Markiere jede Stelle, an der du interpretiert hast, mit (Annahme).
4. Präsens, Wir-Form des Mandanten.

GLIEDERUNG
A. ALLGEMEINE BESCHREIBUNG – Zweck, Geltungsbereich, Belegarten,
   Verantwortliche (Rollen), Stand, Versionierung, Änderungshistorie.
B. ANWENDERDOKUMENTATION – der Prozess aus Sicht der Beschäftigten:
   Annahme, Vorbereitung, Scannen, Sichtprüfung, Indexierung, Freigabe,
   Weitergabe an die Kanzlei, Fehler und Nachzügler, Vertretung.
C. TECHNISCHE SYSTEMDOKUMENTATION – Hard- und Software mit Versionsständen,
   Schnittstellen und Datenflüsse vom Vorsystem bis zur Buchführung,
   Formate, Auflösung, Speicherorte, Berechtigungskonzept,
   Unveränderbarkeit, Protokollierung, Migrationen.
C2. E-RECHNUNGEN UND ELEKTRONISCHE EINGANGSBELEGE – Empfangswege, welcher
    Bestandteil als aufbewahrungspflichtiges Original behandelt wird
    (strukturierter Datenteil), wie die bildhafte Darstellung behandelt wird,
    wie die maschinelle Auswertbarkeit ohne Konvertierung sichergestellt ist,
    wo Ergänzungen zum Beleg festgehalten werden, wenn auf dem Beleg selbst
    nicht geschrieben werden kann. Fundstelle und Anforderungen – für [JAHR]
    verifizieren.
D. BETRIEBSDOKUMENTATION – Datensicherung und Wiederherstellung, Notfall-
   und Ausfallregelung, internes Kontrollsystem (welche Kontrolle, durch
   wen, wie oft, wie nachweisbar), Zugriffsschutz, Lesbarmachung, Löschung.
E. SCANRICHTLINIE (ersetzendes Scannen) – wer scannt (Rolle), wann, welche
   Belege ausdrücklich NICHT ersetzend gescannt werden, wie die bildliche
   Übereinstimmung geprüft und protokolliert wird, wie nachgescannt wird.
   Formuliere KEINE eigenen Voraussetzungen für die Vernichtung des
   Papieroriginals. Gib stattdessen als Leerstelle aus:
   "Vernichtung erst nach schriftlicher Freigabe durch [ROLLE]; die
   Voraussetzungen legt die Kanzlei fest (Fundstelle und Frist – für [JAHR]
   verifizieren)." Führe die Unterlagen, die NICHT ersetzend gescannt werden
   dürfen, als eigene Positivliste mit zwei getrennten Gründen:
   (1) steuerliche Original-Aufbewahrungspflicht – Jahresabschlüsse,
   Eröffnungsbilanz sowie bestimmte Zoll- und Präferenzunterlagen
   (§ 147 Abs. 2 AO – Umfang und Fundstelle für [JAHR] verifizieren);
   (2) nichtsteuerliche Gründe – Urkunden und Dokumente mit Beweisfunktion.
   Beides als Prüfpunkt, nicht als Abschlussliste.
F. AUFBEWAHRUNG – Ordne den Belegarten die Fristen zu. Behandle
   Buchungsbelege und die übrigen aufbewahrungspflichtigen Unterlagen
   getrennt, weil die Fristen unterschiedlich sein können, und markiere
   JEDE Fristangabe als "Frist und Anwendungsbereich für [JAHR]
   verifizieren". Nenne keine Frist ohne diese Kennzeichnung.

ANFORDERUNGEN
- Kennzeichne jede Aussage, bei der du dir nicht sicher bist. Rate nicht.
- Nenne zu JEDER rechtlichen Aussage die Rechtsgrundlage (Norm mit Absatz und
  Satz, Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
  "für [JAHR] verifizieren". Kannst du sie nicht angeben, kennzeichne die Aussage
  als "ohne Fundstelle – vor Verwendung belegen". Erfinde keine Paragrafen,
  BMF-Schreiben oder Dokumentnummern; unsichere: "Fundstelle offen – bitte
  recherchieren".
- Der Entwurf muss ohne die Lückenliste unvollständig WIRKEN.
  Schreibe keine Lücke schön.

AUSGABEFORMAT
1. Verfahrensdokumentation (Entwurf), Abschnitte A–F einschließlich C2
2. Lückenliste: Nr. | Lücke | Risiko | wer klärt | Antwort des Mandanten (leer)
3. Interne Notiz: was die Kanzlei vor Freigabe prüfen muss, welche Aussagen
   zu plausibilisieren sind, was ohne Besichtigung vor Ort offenbleibt
4. "Was ich nicht sicher weiß"
```

## Anwendung

1. Die Ablaufbeschreibung vom Mandanten schreiben lassen, idealerweise von der Person, die tatsächlich scannt. Formulierungen der Kanzlei erzeugen genau den Wunschprozess, den der Prompt vermeiden soll.
2. Entwurf und Lückenliste getrennt übergeben; die Lückenliste ist der Arbeitsauftrag.
3. Nach Rücklauf den Prompt mit ergänzter Beschreibung erneut laufen lassen, statt den Text von Hand zu flicken.
4. Stand, Version und Verantwortliche eintragen und bei jeder Systemänderung fortschreiben.

## Qualitätssicherung

- **Rechtsstand prüfen an:** GoBD, BMF-Schreiben vom 28.11.2019, zuletzt geändert durch BMF-Schreiben vom 14.07.2025 (Fassung und Änderungsstand für [JAHR] verifizieren – die GoBD wurden bereits zweimal geändert). Ergänzend an der Muster-Verfahrensdokumentation zum ersetzenden Scannen von BStBK und DStV sowie an der BSI-Richtlinie TR-03138 (RESISCAN).
- **Aufbewahrungsfristen selbst nachschlagen.** Die Verkürzung durch das Vierte Bürokratieentlastungsgesetz betrifft nicht alle aufbewahrungspflichtigen Unterlagen gleichermaßen; für einzelne Branchen gelten abweichende Regelungen.
- Eine Stichprobe Belege durch den dokumentierten Prozess zurückverfolgen. Weicht die Praxis ab, ist der Entwurf zu ändern – nicht die Praxis auf dem Papier.
- Klären, wer beim Mandanten die Dokumentation verantwortet und unterschreibt. Sie ist eine Erklärung des Mandanten, nicht der Kanzlei.
- Vier-Augen-Prinzip: Freigabe durch einen Berufsträger, weil der Entwurf in der Prüfung gegen den Mandanten verwendet werden kann.

## Varianten

- **Kurzfassung:** "Erzeuge eine zweiseitige Fassung für einen Betrieb mit unter fünf Beschäftigten – ohne Abschnitte ohne Anwendungsfall."
- **Nur Scanrichtlinie:** "Erzeuge ausschließlich Abschnitt E als Arbeitsanweisung zum Aushang am Scanplatz, höchstens eine Seite."
- **Fragebogen vorab:** "Erzeuge aus der Gliederung einen Fragebogen für den Mandanten, je Abschnitt höchstens fünf Fragen in Alltagssprache."
- **Fortschreibung:** "Vergleiche die vorliegende Fassung mit der neuen Ablaufbeschreibung und liste nur die zu ändernden Abschnitte auf."
