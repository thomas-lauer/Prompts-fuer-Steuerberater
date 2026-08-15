---
name: liquiditaetsplanung-13-wochen
description: Baut aus OPOS-Listen, Fixkosten, Tilgungsplan und Kreditlinien eine
  rollierende Wochentabelle über 13 Wochen, weist je Zeile die Herkunft des Werts
  aus und rechnet die drei Szenarien durch. Schreibt eine vorhandene Planung Woche
  für Woche fort und stellt Plan und Ist gegenüber. Use when a client's cash
  position over the next quarter must be planned or an existing 13-week plan needs
  to be rolled forward by one week.
---

# 66 – Rollierende 13-Wochen-Liquiditätsplanung

## Zweck

Die Skill führt die Arbeit aus, die der Prompt beschreibt: Sie liest die
exportierten Listen zeilenweise ein, verteilt jede Position auf die Kalenderwoche,
in der sie zahlungswirksam wird, und rechnet Anfangsbestand, Endbestand und freien
Rahmen über 13 Wochen durch – für die Basis und für die beiden abweichenden
Szenarien. Der Mengenvorteil liegt doppelt: in der Datenauswertung, weil eine
OPOS-Liste mit dreistelliger Zeilenzahl von Hand nicht in Wochen zerlegt wird, und
in der Fortschreibung, weil die Skill beim nächsten Aufruf die vorhandene Datei
einliest, die abgelaufene Woche gegen das Ist schließt und eine neue 13. Woche
anhängt. Erst diese Rückschau macht die Planung belastbar.

## Wann einsetzen – und wann nicht

Einsetzen für den Aufbau eines Planungsgerüsts über 13 Wochen, für die wöchentliche
Fortschreibung einer bereits angelegten Planung und für die Gegenüberstellung von
Plan und Ist der abgelaufenen Wochen.

Nicht einsetzen:

- **Krisenindikatoren und Hinweisschreiben:** Prompt 65. Er ist dem Berufsträger
  vorbehalten und fragt anderes ab – Abschlusszahlen mehrerer Jahre, Kapitaldienst
  gegen erwirtschafteten Überschuss, Lieferantenlaufzeiten, Datum und Inhalt des
  Gesprächs. Diese Angaben erhebt die Skill nicht.
- **Zahlungsunfähigkeit, Statusgerüst für den Insolvenzrechtler:** Prompt 74. Er
  verlangt einen Stichtag, fällige Verbindlichkeiten mit Datum der Fälligstellung,
  Rückstände bei der Sozialversicherung als Gesamtbetrag und als Pflichtangabe die
  Bestätigung, dass die Beitragsrückstände dem Berufsträger vorgelegen haben. Ohne
  diese Felder ist ein Status nicht aufzubauen – die Skill baut ihn deshalb nicht,
  auch nicht ansatzweise, und trifft **keine insolvenzrechtliche Beurteilung**.
- **Sanierungs- und Finanzierungsberatung:** dafür gibt es in dieser Sammlung
  keinen Prompt und keine Skill, und es soll auch keine geben. Beides ist
  Rechtsdienstleistung und für den Steuerberater allenfalls als Nebenleistung
  denkbar; die Abgrenzung und ihre Fundstellen stehen in der Prompt-Datei. Nach
  einer Finanzierungsempfehlung, einem Sanierungsvorschlag oder einer Aussage zur
  Fortführungsfähigkeit gefragt, gibt die Skill sie nicht ab, sondern verweist an
  den Berufsträger und an einen Insolvenz- oder Sanierungsrechtler.
- **Vorlage bei einer Bank:** Prompt 67 – er fragt den Wortlaut der Bankanforderung
  und den Stand der dokumentierten Einwilligung ab.
- **Reine Auswertung offener Forderungen** nach Altersstruktur und Risiko, ohne
  Wochenbezug: Prompt 18. Er wertet den OPOS-Export der **Debitoren** aus – die
  Forderungen des Mandanten gegen seine Kunden – und hat kein Eingabefeld für
  Kreditoren. Für die Verbindlichkeitenseite gibt es kein eigenes Ziel; sie bleibt
  in dieser Skill und wird hier wochenweise verteilt.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Die Skill bekommt den Sachverhalt unmittelbar; niemand maskiert vorher. Deshalb
zuerst:

1. Bestätigung einholen, dass Steuer-Identifikationsnummer, Steuernummer und
   Aktenzeichen des Finanzamts vollständig entfernt sind – nicht teilmaskiert,
   nicht in Ausschnitten, nicht in Anlagen.
2. Nur mit Kürzeln arbeiten: `Mandant A`, `Kunde 1`, `Lieferant 1`, Beschäftigte
   ausschließlich als Rolle, Konten als `Konto ****1234`. Die vollständige IBAN
   bleibt draußen, ebenso die Zuordnungstabelle der Kürzel.
3. Taucht Zone-Rot-Material auf, wird die Bearbeitung abgebrochen, nicht bereinigt.
   Rückmeldung: welche Angabe gefunden wurde, in welcher Zeile, und die Bitte, den
   Export ohne diese Spalte erneut einzufügen – Betrag, Fälligkeit, Kürzel,
   Mahnstufe und die mittlere Zahlungsverzögerung je Kunde genügen für die Planung.
4. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche
   Einbindung des Anbieters nach § 62a StBerG müssen vor dem Einsatz geklärt sein;
   bei unmittelbarem Einsatz für ein konkretes Mandat klärt der Berufsträger vorab
   § 62a Abs. 5 StBerG. Einzelheiten in `DATENSCHUTZ.md`.

## Ablauf

1. **Datensparsamkeit abschließen.** Ohne die Bestätigung aus Punkt 1 des
   Datensparsamkeitsabschnitts wird nicht begonnen.
2. **Rahmen aufnehmen:** Startwoche, Kontostände zum Start, Limit und Ausnutzung
   der Kreditlinien, Angaben zur Umsatzsteuer. Fehlt ein Feld, wird es als „fehlt"
   geführt und nicht geschätzt.
3. **Exporte zeilenweise einlesen:** OPOS Debitoren und Kreditoren Zeile für Zeile,
   das historische Zahlungsverhalten je Kunde (mittlere Überschreitung in Tagen),
   dazu Fixkosten, Personalkosten samt Abführungen, Tilgungsplan, Sondereffekte,
   Umsatzhistorie. Zeilen ohne Fälligkeit oder ohne Betrag wandern unverändert in
   die Lückenliste und werden nicht eingeplant. Fehlt das Zahlungsverhalten, wird
   es nachgefordert und bis dahin als Lücke geführt – ohne diese Angabe fällt die
   Planung zu optimistisch aus; eine Zahlungsquote wird nicht ersatzweise
   unterstellt.
4. **Vorwochendatei einlesen, falls vorhanden** – vor dem Rechnen, nicht danach.
   Die abgelaufene Woche wird mit den Ist-Werten geschlossen, die Abweichung je
   Position vermerkt, der Endbestand der Vorwoche als Anfangsbestand der neuen
   Startwoche übernommen und eine neue 13. Woche angehängt. Abweichungen, die sich
   wiederholen, werden als geänderte Annahme mit neuem Herkunftskennzeichen
   geführt, nicht stillschweigend eingerechnet. Der Abschnitt „Plan und Ist der
   abgelaufenen Woche" entsteht hier und bleibt auch dann in der Datei, wenn die
   Bearbeitung später nach Schritt 8 endet.
5. **Herkunft je Zeile kennzeichnen** – die tragende Regel dieser Skill. Jede Zeile
   der Wochentabelle und jeder Eintrag der Annahmenliste trägt eines von drei
   Kennzeichen: `Export` (Wert stammt aus einer gelieferten Datei), `Mandant`
   (vom Mandanten genannt oder geschätzt) oder `Annahme` (aus der gelieferten
   Historie abgeleitet, mit offengelegtem Ableitungsweg). Ein Wert ohne Kennzeichen
   kommt nicht in die Tabelle; lässt sich die Herkunft nicht klären, wird die
   Position zur Lücke. Zahlungsquoten, Zinssätze und Saisonverläufe werden nicht
   erfunden.
6. **Wochentabelle rechnen** nach dem Vorgehen in der Prompt-Datei, Schritte 1 bis 6,
   in dieser Reihenfolge. Steuer- und Beitragszahlungen bekommen eine eigene Zeile
   mit leerer Wochenspalte; die Skill bestimmt keinen Zahlungstermin.
7. **Szenarien rechnen:** Basis, vorsichtig, angespannt. Geändert werden
   ausschließlich Annahmen, nie Zahlen; je Szenario werden die geänderten Annahmen
   offen aufgelistet.
8. **Punkt der ersten Unterdeckung bestimmen** – ohne Bewertung. Ergibt ein Szenario
   einen Endbestand zuzüglich freier Linie unter Null oder eine vollständig
   ausgenutzte Linie, endet die Bearbeitung hier: Erläuterungstext für den Mandanten
   und Frühindikatoren werden **nicht** erzeugt, ausgegeben werden nur Wochentabelle,
   Annahmenliste und der Weiterleitungssatz aus der Prompt-Datei mit Woche und
   Szenario. Die Weiterleitung an den Berufsträger und das Verfahren aus Prompt 65
   werden nicht abgeschwächt, nicht relativiert und nicht durch eine eigene
   Einschätzung ersetzt.
9. **Erläuterungstext und Frühindikatoren erzeugen** – nur, wenn Schritt 8 nicht
   gegriffen hat. Der Erläuterungstext ist in Sie-Form, höchstens 350 Wörter, löst
   jeden Fachbegriff in einem Halbsatz auf und enthält den Vorbehalt aus der
   Abgrenzung der Prompt-Datei: Die Planung ist eine Fortschreibung von Annahmen,
   keine Zusage, keine Finanzierungsempfehlung und keine Fortbestehensprognose.
   Dieser Vorbehalt ist Pflichtbestandteil des Mandantentextes, nicht bloß ein
   Verbot. Dazu höchstens sieben Frühindikatoren, je mit Quelle in DATEV und
   Beobachtungsanlass.
10. **Ergebnis ablegen.** An den Anfang kommt die Einschätzung der Eindeutigkeit –
    eindeutig / vertretbare Varianten / nicht entscheidbar – und unmittelbar
    darunter die Lückenliste mit allen als „fehlt" geführten Angaben. Lücken werden
    weder eingeplant noch geschätzt.

## Ergebnis

Eine Datei `<Mandatskürzel>-liquiditaet-13w-<JJJJ-KWnn>.md`, je Fortschreibung eine
neue Datei mit der Kalenderwoche im Namen, damit der Verlauf nachvollziehbar bleibt.
Inhalt und Reihenfolge folgen dem Ausgabeformat der Prompt-Datei; die Wochentabelle
wird um eine Spalte „Herkunft" ergänzt, bei einer Fortschreibung kommt ein Abschnitt
„Plan und Ist der abgelaufenen Woche" davor. Endet der Lauf nach Schritt 8, enthält
die Datei die Einschätzung der Eindeutigkeit, die Lückenliste, den Abschnitt „Plan
und Ist der abgelaufenen Woche" aus Schritt 4, Wochentabelle, Annahmenliste und den
Weiterleitungssatz – und einen Vermerk, dass die Mandantenkommunikation bewusst
unterblieben ist.

Die Datei ist das Übertragungsgerüst, nicht das führende System: Wochentabelle und
Annahmen werden nach der Freigabe in DATEV Analyse und Planung (Liquiditätsplanung)
übernommen und dort fortgeschrieben. Eine dauerhaft danebenlaufende Einzeltabelle
wird nicht angelegt.

## Qualitätssicherung

- **Vier-Augen-Prinzip:** Das Ergebnis ist ein Entwurf. Eine zweite Person rechnet
  Wochentabelle und Annahmenliste nach; die Freigabe erteilt ein Berufsträger
  (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Die Skill berechnet keine Fristen und keine Steuertermine.** Sie benennt nur,
  welche Terminarten im Raum stehen. Die Woche setzt ein Mensch ein und erfasst den
  Termin im Fristenprogramm; solange eine Zeile keine Woche trägt, ist die Tabelle
  ausdrücklich unvollständig.
- **Jede Annahme auf ihre Quelle prüfen.** Zeilen mit dem Kennzeichen `Annahme`
  werden gegen den ausgewiesenen Ableitungsweg gehalten; was sich nicht zurückführen
  lässt, wird gestrichen und bleibt Lücke.
- **Keine Zusage im Text – und der Vorbehalt muss darin stehen.** Formulierungen
  streichen, die Zahlungsfähigkeit oder Fortführung zusichern, und positiv prüfen,
  dass der Erläuterungstext den Vorbehalt trägt: Fortschreibung von Annahmen, keine
  Zusage, keine Finanzierungsempfehlung, keine Fortbestehensprognose. Fehlt der
  Vorbehalt, geht der Text nicht hinaus.
- **Verwendungszweck prüfen, bevor etwas das Haus verlässt:** Weitergabe an eine
  Bank nur nach Prompt 67, bei Krisenindikatoren Prompt 65, bei der Frage der
  Zahlungsunfähigkeit Prompt 74 – jeweils mit gesonderter Beurteilung durch einen
  Berufsträger.
- **Rechtsstand:** Die Skill übernimmt keine eigene Fundstellensammlung in diese
  Datei – maßgeblich sind die Fundstellen der Prompt-Datei. In der Ausgabe steht
  gleichwohl zu jeder rechtlichen Aussage die Rechtsgrundlage positiv mit Absatz und
  Satz, jeweils mit dem Zusatz `für [JAHR] verifizieren`; ist eine Fundstelle
  unsicher, steht dort „Fundstelle offen – bitte recherchieren". Ein Verbot ersetzt
  hier keine Pflicht: Ohne benannte Fundstelle weiß der Berufsträger nicht, was er
  nachschlagen soll.

## Grundlage

Diese Skill führt den Prompt
[prompts/12-krise-liquiditaet-bank/66-liquiditaetsplanung-13-wochen.md](../../../prompts/12-krise-liquiditaet-bank/66-liquiditaetsplanung-13-wochen.md)
aus; Prüfschema, Abgrenzung und Fundstellen stehen dort und gelten unverändert.
