# 10 – Reisekosten- und Bewirtungsbeleg prüfen

**Problem:** Frühstückskürzung, Business-Package, Achtstundengrenze, fehlende Pflichtangaben auf Bewirtungsbelegen – die immer gleichen Fehler kosten in jeder Buchungsperiode Zeit und gefährden den Betriebsausgaben- und Vorsteuerabzug.
**Rolle:** Buchhaltung, Lohnsachbearbeitung, Steuerberater
**DATEV-Bezug:** Kanzlei-Rechnungswesen, DATEV Unternehmen online, Lohn und Gehalt (steuerfreie Erstattungen)
**Was du bereitstellen musst:** Reisedaten, Belegangaben, was der Arbeitgeber erstattet hat.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Personalnummern und die Namen der bewirteten Personen durch Platzhalter ersetzen (`Mandant A`, `AN 1`, `Teilnehmer 1–4`, `Geschäftspartner 1`). Für die Prüfung genügen Rolle, Anlass, Orte, Uhrzeiten und Beträge. Die namentliche Teilnehmerliste bleibt auf dem Beleg in der Kanzlei.

## Prompt

```text
Du prüfst Reisekosten- und Bewirtungsabrechnungen in einer deutschen
Steuerkanzlei. Du arbeitest strikt nach Prüfschema und gibst nie einen Wert
an, den du nicht als aktuellen Rechtsstand verifizieren kannst, ohne ihn
als prüfbedürftig zu kennzeichnen.

AUFGABE
Prüfe die folgende Abrechnung auf steuerliche Richtigkeit und benenne
Korrekturbedarf.

REISE / VORGANG
- Reisender: [ROLLE, z. B. Arbeitnehmer / Unternehmer]
- Erste Tätigkeitsstätte: [ORT / keine / arbeitsvertraglich zugeordnet ja-nein]
- Reisegrund: [ANLASS]
- Reiseverlauf: [ABFAHRT DATUM UHRZEIT ORT → ANKUNFT … je Etappe]
- Land/Länder: [ANGABEN]
- Übernachtungen: [ANZAHL, Hotelrechnung liegt vor ja/nein]
- Verpflegung gestellt: [Frühstück / Mittag / Abend – an welchen Tagen,
  auch wenn nicht in Anspruch genommen]
- Dauer der Auswärtstätigkeit an derselben Stätte bisher: [ANGABE, wegen
  Dreimonatsfrist]

BELEGE
[JE BELEG: Art | Datum | Aussteller | Netto/USt/Brutto | Besonderheiten,
 z. B. "Hotelrechnung mit Business-Package 25 €",
 "Bewirtungsbeleg 186 € brutto, handschriftlicher Eigenbeleg",
 "Taxiquittung ohne USt-Ausweis"]

ERSTATTUNG DURCH DEN ARBEITGEBER
[WAS WURDE IN WELCHER HÖHE ERSTATTET]

PRÜFE UND DOKUMENTIERE
A. VERPFLEGUNGSMEHRAUFWAND
   1. Liegt eine Auswärtstätigkeit vor? Erste Tätigkeitsstätte geklärt?
   2. Abwesenheitsdauer je Kalendertag; An- und Abreisetag gesondert.
   3. Anzuwendender Pauschbetrag je Tag (Inland/Ausland) – nenne den
      Wert und markiere ihn als "für [JAHR] verifizieren".
   4. Kürzung wegen gestellter Mahlzeiten: Nenne die Kürzungslogik
      (Prozentsatz bezogen auf den vollen Tagessatz, unabhängig davon,
      ob die Mahlzeit in Anspruch genommen wurde) und rechne sie je Tag vor.
   5. Dreimonatsfrist: greift sie? Wurde sie durch Unterbrechung neu ausgelöst?
B. ÜBERNACHTUNG
   6. Aufteilung der Hotelrechnung: Übernachtung, Frühstück, sonstige
      Leistungen; Behandlung eines pauschalen "Business-Package".
   7. Umsatzsteuerliche Aufteilung und Vorsteuerabzug.
C. FAHRTKOSTEN
   8. Tatsächliche Kosten oder pauschaler Kilometersatz für
      Auswärtstätigkeiten (§ 9 Abs. 1 Satz 3 Nr. 4a EStG – NICHT die
      Entfernungspauschale, die nur für Fahrten zur ersten
      Tätigkeitsstätte gilt); Nachweise.
      Satz bitte für [JAHR] verifizieren.
D. BEWIRTUNG
   9. Prüfe die Pflichtangaben einzeln: Ort, Tag, Teilnehmer namentlich
      (auf dem Eigenbeleg, nicht in der Rechnungsanschrift),
      konkreter Anlass (allgemeine Angaben wie "Arbeitsessen" genügen
      nicht), Höhe, Unterschrift des bewirtenden Steuerpflichtigen;
      bei Bewirtung in einem Bewirtungsbetrieb eine maschinell erstellte,
      elektronisch aufgezeichnete und mit einer zertifizierten
      technischen Sicherheitseinrichtung abgesicherte Rechnung mit den
      Angaben nach § 6 KassenSichV;
      ab der Kleinbetragsgrenze zusätzlich Name und Anschrift des
      bewirtenden Unternehmers als Rechnungsempfänger (nicht der
      bewirteten Gäste) sowie Steuernummer/USt-ID des Ausstellers –
      eine handschriftliche Ergänzung des Rechnungsempfängers genügt nicht.
   10. Abzugsumfang: Geschäftsfreunde vs. reine Arbeitnehmerbewirtung;
       Behandlung des Trinkgelds; Vorsteuerabzug.
E. ERSTATTUNG UND LOHNSTEUER
   11. Ist die Erstattung steuerfrei, pauschalierbar oder steuerpflichtiger
       Arbeitslohn? Prüfe Auslagenersatz vs. durchlaufende Gelder.
   12. Welcher Betrag ist ggf. dem Lohn hinzuzurechnen?
   13. Bescheinigungspflichten: Ist der Großbuchstabe "M" in der
       Lohnsteuerbescheinigung einzutragen (§ 41b Abs. 1 Satz 2 Nr. 8 EStG)?
       Sind Mahlzeitengestellungen oberhalb der Grenze für Belohnungsessen
       als Arbeitslohn zu erfassen (Grenzwert bitte für [JAHR] verifizieren)?

ANFORDERUNGEN
- Erstelle eine Korrekturtabelle: Position | abgerechnet | richtig |
  Differenz | Grund | Rechtsgrundlage.
- Liste getrennt auf: "Beleg unbrauchbar – neu anfordern" und
  "Beleg heilbar – was ergänzt werden muss".
- Formuliere einen Kurztext an den Mandanten, der die Beanstandungen
  ohne Vorwurf erklärt und sagt, was künftig anders laufen soll.
- Markiere ALLE Pauschbeträge, Freigrenzen und Prozentsätze ausdrücklich
  als "Wert für [JAHR] bitte verifizieren". Erfinde keine Auslandssätze.

AUSGABEFORMAT
A–E als Prüfabschnitte – Korrekturtabelle – Belegstatus –
Mandantentext – "Werte bitte verifizieren".
```

## Anwendung

1. Reiseverlauf mit Uhrzeiten eingeben – ohne Uhrzeiten ist der Verpflegungsmehraufwand nicht prüfbar.
2. Gestellte Mahlzeiten immer angeben, auch wenn der Reisende sie nicht genutzt hat.
3. Korrekturtabelle als Grundlage für die Buchung und für die Rückmeldung an den Mandanten nutzen.

## Qualitätssicherung

- **Pauschbeträge und Auslandssätze immer selbst nachschlagen** (BMF-Schreiben zu den Auslandstagegeldern des jeweiligen Jahres). Sprachmodelle geben hier häufig veraltete oder erfundene Werte an – das ist die größte Fehlerquelle dieses Prompts.
- Kürzungsbeträge nachrechnen: Der Prozentsatz bezieht sich auf den vollen Tagessatz, auch an Tagen mit reduziertem Pauschbetrag.
- **Rechtsstand Bewirtung:** Maßgeblich ist das jeweils aktuelle BMF-Schreiben zur Anerkennung von Bewirtungsaufwendungen (zuletzt 19.11.2025, ersetzt das Schreiben vom 30.06.2021). Fassung vor Anwendung prüfen.
- Bewirtungsbelege im Original ansehen; die KI beurteilt nur, was in der Beschreibung steht.
- Bei lohnsteuerlicher Nachversteuerung Freigabe durch die Lohnsachbearbeitung einholen.

## Varianten

- **Mandantenmerkblatt:** "Leite aus den Beanstandungen ein einseitiges Merkblatt ab: was auf einen Bewirtungsbeleg gehört und wie eine Reisekostenabrechnung eingereicht wird."
- **Massenprüfung:** "Prüfe die folgenden 20 Abrechnungen und liste nur die auf, bei denen ein Korrekturbedarf besteht – mit Kurzbegründung."
- **Reiserichtlinie:** "Erstelle aus den wiederkehrenden Fehlern einen Entwurf für eine Reisekostenrichtlinie des Mandanten."
