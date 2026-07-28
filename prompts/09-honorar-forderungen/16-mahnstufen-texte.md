# 16 – Mahnstufen: Zahlungserinnerung, erste und zweite Mahnung, Ratenzahlung

**Problem:** Offene Honorare bleiben liegen, weil niemand gern mahnt. Wenn dann gemahnt wird, ist der Ton entweder zu weich oder zu scharf, und der Mandant reagiert nicht oder verärgert.
**Rolle:** Sekretariat, Kanzleileitung, Buchhaltung
**DATEV-Bezug:** DATEV Eigenorganisation comfort (Rechnungsschreibung, Mahnwesen)
**Was du bereitstellen musst:** Rechnungsdaten, bisherige Kontakte, Art des Mandanten, ob eine Ratenzahlung in Frage kommt.
**Datensparsamkeit:** Mandantenname, Anschrift, Steuernummer und Bankdaten weglassen. Für den Entwurf genügen Rechnungsdatum, Betrag, Fälligkeit und der bisherige Verlauf. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe DATENSCHUTZ.md.

## Prompt

```text
Du schreibst das Mahnwesen einer deutschen Steuerkanzlei. Du weißt, dass eine
Kanzlei ihren Mandanten anders mahnt als ein Versandhändler: Die Beziehung soll
das Mahnverfahren überleben, und berufsrechtliche Grenzen sind zu beachten.

AUFGABE
Schreibe eine vierstufige Mahnstrecke plus eine Ratenzahlungsvereinbarung.

VORGANG
- Rechnungsdatum: [DATUM] · Rechnungsnummer: [NR]
- Betrag: [BETRAG] · Fällig seit: [DATUM]
- Leistung: [z. B. Jahresabschluss 2025, laufende Buchführung 01–06/2026]
- Mandantenart: [Unternehmer / Verbraucher]
- Mandatsstatus: [läuft weiter / beendet / in Kündigung]
- Bisherige Kontakte: [z. B. Rechnung am …, telefonisch erinnert am …]
- Reaktion bisher: [keine / Zahlungszusage nicht eingehalten /
  Einwand gegen die Höhe / Liquiditätsproblem geschildert]
- Beziehung: [langjährig und gut / neutral / angespannt]
- Ratenzahlung möglich: [ja, bis … Raten / nein]
- Heutiges Datum: [DATUM]

ANFORDERUNGEN
0. Setze an den Anfang eine Prüffrage: Liegt dem Mandanten eine Berechnung in
   Textform vor, die alle Angaben des § 9 Abs. 2 StBVV enthält? Wenn nicht oder
   unklar, gib die Zeile "ACHTUNG – vor jeder Mahnung Berechnung nach § 9 StBVV
   prüfen" aus und begründe.
1. Erzeuge fünf Texte, jeder als sofort versendbares Schreiben mit Betreff:
   Stufe 1 – Zahlungserinnerung: unterstellt Versehen, freundlich, kurz.
   Stufe 2 – Erste Mahnung: sachlich, neue Frist mit Datum, Hinweis auf
     die Folgen bei weiterem Ausbleiben.
   Stufe 3 – Zweite und letzte Mahnung: förmlich, letzte Frist, benennt die
     nächsten Schritte sachlich (gerichtliches Mahnverfahren, Übergabe zur
     Rechtsverfolgung), bietet weiterhin ein Gespräch an.
   Stufe 4 – Ankündigung der Rechtsverfolgung: knapp, ohne Wiederholung,
     mit Fristsetzung.
   Zusatz – Ratenzahlungsvereinbarung: Text zum Gegenzeichnen mit
     Ratenhöhe, Fälligkeiten und Verfallklausel.
2. Höchstens 150 Wörter je Schreiben. Keine Wiederholung des gesamten
   Verlaufs – ab Stufe 2 genügt ein Satz zur Vorgeschichte.
3. Nenne in jedem Schreiben: Rechnungsnummer, Datum, Betrag, neue Frist mit
   konkretem Datum, Zahlungsweg.
4. Verzug (§ 286 BGB – für [JAHR] verifizieren):
   - Grundfall: Verzug tritt durch Mahnung nach Eintritt der Fälligkeit ein
     (§ 286 Abs. 1 BGB) – bei Unternehmern wie Verbrauchern gleichermaßen.
     Die Zahlungserinnerung der Stufe 1 ist bereits eine Mahnung.
   - Zusätzlich tritt Verzug spätestens 30 Tage nach FÄLLIGKEIT UND Zugang
     der Rechnung ein (§ 286 Abs. 3 BGB); gegenüber Verbrauchern nur, wenn
     in der Rechnung auf diese Folge besonders hingewiesen wurde.
   - Die Fälligkeit richtet sich nach § 7 StBVV, nicht nach dem
     Rechnungsdatum; einforderbar ist die Vergütung erst nach Mitteilung der
     Berechnung in Textform (§ 9 Abs. 1 StBVV).
   Formuliere den Hinweis entsprechend der Mandantenart.
5. Verzugszinsen und Mahnkosten: Nenne KEINE konkreten Zinssätze oder Beträge.
   Setze stattdessen die Platzhalter [ZINSSATZ] und [MAHNKOSTEN]
   (von der Kanzlei einzusetzen und zu prüfen).
6. Zurückbehaltungsrecht an Unterlagen: Erwähne es NICHT in den Stufen 1 bis 4.
   Erzeuge stattdessen einen gesonderten internen Abschnitt mit den
   Voraussetzungen (§ 66 Abs. 3 StBerG – für [JAHR] verifizieren):
   - Die Vergütung muss fällig (§ 7 StBVV) und einforderbar sein; einforderbar
     erst nach Mitteilung einer Berechnung in Textform mit allen Angaben des
     § 9 Abs. 2 StBVV.
   - Konnexität: Forderung und Unterlagen aus demselben Auftragsverhältnis.
   - Erfasst sind nur Dokumente, die die Kanzlei VON oder FÜR den Auftraggeber
     erhalten hat (§ 66 Abs. 2 Satz 1 StBerG). NICHT erfasst: Korrespondenz
     zwischen Kanzlei und Mandant, Dokumente, die der Mandant bereits besitzt,
     interne Arbeitspapiere.
   - Unangemessenheit: nicht ausüben, wenn der Mandant die Unterlagen dringend
     für die Fortführung seines Betriebs oder eigene Fristen braucht, wenn es
     als Druckmittel für eine Honorarerhöhung wirkt oder wenn die Forderung
     im Verhältnis zur Bedeutung der Unterlagen geringfügig ist.
   - Es wirkt gegenüber dem Auftraggeber. Es entbindet den Mandanten nicht von
     seinen Erklärungspflichten gegenüber dem Finanzamt und rechtfertigt keine
     Fristversäumnis.
   Kennzeichne alles davon als prüfbedürftig.
7. Passe den Ton an die Beziehung an. Bei einem langjährigen Mandat beginnt
   Stufe 1 mit einer persönlichen Zeile, bei einem angespannten nicht.
8. Wenn ein Einwand gegen die Höhe vorliegt: Setze an den Anfang eine Zeile
   "ACHTUNG – erst den Einwand klären, dann mahnen" und begründe.
9. Erzeuge einen Zeitplan: welche Stufe wann versendet wird, ausgehend vom
   heutigen Datum.
10. Erzeuge eine INTERNE NOTIZ mit den Punkten, die vor dem Versand zu prüfen
    sind, einschließlich der Frage, ob die Verjährung des Honoraranspruchs
    droht – eine Mahnung hemmt die Verjährung nicht.
11. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage, jeweils mit dem
    Zusatz "für [JAHR] verifizieren". Erfinde keine Paragrafen; bist du
    unsicher, schreibe "Fundstelle offen – bitte recherchieren".

AUSGABEFORMAT
Prüffrage Berechnung nach § 9 StBVV – Zeitplan – Stufe 1 bis 4 –
Ratenzahlungsvereinbarung – Hinweis Zurückbehaltungsrecht (intern) –
Interne Notiz.
```

## Anwendung

1. Einmal als Kanzleivorlage erzeugen, danach nur noch Rechnungsdaten austauschen.
2. Zeitplan als Wiedervorlage hinterlegen – der häufigste Fehler ist, dass Stufe 2 nie versendet wird.
3. Bei Einwänden gegen die Höhe zuerst Prompt 15 verwenden.
4. Ratenzahlungsvereinbarung nur nach Freigabe verwenden; sie berührt Fälligkeit und Durchsetzbarkeit.

## Qualitätssicherung

- **Zinssätze, Mahnkosten und Verzugsfolgen selbst einsetzen und prüfen.** Der Prompt lässt sie bewusst offen.
- **Verjährung im Blick behalten:** Honoraransprüche verjähren in der Regelfrist; maßgeblich ist die Fälligkeit, nicht die Rechnungsstellung. Eine Mahnung hemmt die Verjährung nicht – dafür braucht es Mahnbescheid oder Klage. Laufende Verhandlungen über die Forderung hemmen die Verjährung dagegen (§ 203 BGB – für [JAHR] verifizieren); Beginn und Ende der Verhandlungen dokumentieren. Bei drohendem Fristablauf sofort einen Berufsträger einschalten.
- **Zurückbehaltungsrecht nie ohne Prüfung ausüben.** Es setzt eine fällige und einforderbare Vergütung voraus – einforderbar erst nach mitgeteilter Berechnung nach § 9 StBVV – und wirkt nicht gegenüber jedem und nicht an allem (§ 66 Abs. 2 und 3 StBerG – für [JAHR] verifizieren). Fehlgriffe können Schadensersatzpflichten auslösen.
- Prüfen, ob eine Lastschrift läuft und ob sie noch zurückgegeben werden kann.
- **Freigabe durch einen Berufsträger für alle Stufen.** Bereits die Zahlungserinnerung ist eine Mahnung im Sinne des § 286 Abs. 1 BGB und begründet Verzug. Die Ratenzahlungsvereinbarung ist ein Vertrag und geht nie ohne Berufsträger hinaus; sie berührt Fälligkeit, Durchsetzbarkeit und den Beginn der Verjährung.

## Varianten

- **Beendetes Mandat:** "Passe die Stufen an ein bereits beendetes Mandat an – ohne Angebote zur weiteren Zusammenarbeit."
- **Liquiditätsproblem:** "Der Mandant hat ein Liquiditätsproblem geschildert. Erzeuge stattdessen ein Schreiben, das eine Ratenzahlung anbietet und den Kontakt hält."
- **Telefonleitfaden:** "Erzeuge einen Gesprächsleitfaden für das Mahntelefonat: Einstieg, drei mögliche Reaktionen des Mandanten, Antwort darauf, Gesprächsziel."
- **Mandantenmahnwesen:** "Erzeuge dieselbe Mahnstrecke für unseren Mandanten gegenüber seinen eigenen Kunden – ohne berufsrechtliche Besonderheiten."
