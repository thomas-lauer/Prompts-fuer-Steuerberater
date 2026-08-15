---
name: euer-plausibilitaet
description: Prüft die Positionen einer Einnahmen-Überschuss-Rechnung vor der Abgabe
  Zeile für Zeile gegen das Vorjahr, rechnet Abweichungen und Verhältniskennzahlen mit
  Rechenweg, gleicht die AfA-Summe des Anlagenverzeichnisses gegen die AfA-Position ab
  und erzeugt daraus Auffälligkeiten und geschlossene Rückfragen an den Mandanten.
  Fordert Rechtsform und Umsatzsteuerstatus nach, weil sie ganze Prüfschritte schalten.
  Use when a cash-basis profit statement (EÜR) and its fixed-asset schedule have to be
  screened for plausibility and cut-off errors before it is filed.
---

# 21 – Plausibilitätsprüfung EÜR-Zahlen vor Abgabe

## Zweck

Der Prompt beschreibt, worauf bei einer EÜR vor der Abgabe zu achten ist. Diese
Skill arbeitet die Zahlen tatsächlich durch: Sie stellt jede Position neben ihren
Vorjahreswert, rechnet die Abweichung in Betrag und Prozent, bildet die
Verhältniskennzahlen mit sichtbarem Rechenweg, addiert das Anlagenverzeichnis
Zeile für Zeile und stellt die Summe der AfA-Position gegenüber. Der Mengenvorteil
liegt in der Zahl der Positionen und Anlagengüter: Der Vorjahresvergleich über
alle Zeilen und der Verzeichnisabgleich sind Rechenarbeit, die mit dem Textblock
allein von Hand anfällt – und beide Fehlerarten sind erst im Vergleich sichtbar,
nicht in der einzelnen Zeile.

## Wann einsetzen – und wann nicht

Einsetzen, wenn die EÜR-Positionen mit Vorjahresspalte und das Anlagenverzeichnis
vorliegen und die Zahlen vor der Abgabe einen systematischen Plausibilitätsblick
brauchen. Auch geeignet als Zwischenkontrolle vor dem Mandantengespräch: Die
Rückfragetabelle entsteht dabei ohnehin.

Nicht einsetzen bei bilanzierenden Mandanten. Für die Durchsicht des Kontenbilds
vor dem Abschluss ist Prompt 20 einschlägig – er verlangt den SuSa-Export mit
Verkehrszahlen und Vorjahressaldo und prüft Vorzeichen, Verrechnungskonten und
rechtsformwidrige Konten; es gibt ihn auch als Skill. Die periodengerechte
Abgrenzung zum Bilanzstichtag leistet Prompt 51 mit Nachlaufbuchungen,
OPOS-Liste, Dauerschuldverhältnissen und Ereignissen nach dem Stichtag; bei der
EÜR erledigt Prüfschritt 4 der Prompt-Datei die Periodenfrage nach dem Zu- und
Abflussprinzip.

Nicht einsetzen für die Wahlrechte des Anlagevermögens: Nutzungsdauer, Methode
und Gegenüberstellung je Zugang gehören zu Prompt 52, der Anschaffungskosten,
Reparaturaufwand, Gewinnsituation und geplante Investitionen abfragt und
ebenfalls als Skill vorliegt. Diese Skill prüft nur, ob Verzeichnis und
EÜR-Position zusammenpassen, und entscheidet kein Wahlrecht. Gebildete
Abzugsbeträge nach § 7g EStG überwacht Prompt 53 anhand von Bildungsjahr, Betrag,
geplantem Wirtschaftsgut und den Zugängen des laufenden Jahres. Einen einzelnen
Reisekosten- oder Bewirtungsbeleg mit Reiseverlauf, Uhrzeiten und gestellten
Mahlzeiten prüft Prompt 10; hier bleibt es bei der Frage, ob die Position
insgesamt plausibel und der nicht abziehbare Anteil getrennt erfasst ist. Steht
der Kleinunternehmerstatus selbst in Frage – Grenzen, Verzicht, Statuswechsel –,
ist Prompt 88 einschlägig, der Vorjahresumsatz, aufgelaufenen Umsatz und
Verzichtserklärungen abfragt; diese Skill prüft nur die Konsistenz der Erfassung.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Vor dem Einlesen der Zahlen bestätigen lassen:

- dass Steuer-Identifikationsnummer, Steuernummer und Aktenzeichen des
  Finanzamts entfernt sind – auch nicht maskiert, auch nicht gekürzt, auch nicht
  in Kopf- oder Fußzeilen eines Ausdrucks;
- dass der Mandant nur als Mandatskürzel geführt wird und Anschrift sowie Namen
  Dritter – Lieferanten, Kunden, Mitarbeitende, bewirtete Personen – durch
  Platzhalter ersetzt sind (`Lieferant 1`, `Fahrzeug 1`);
- dass aus dem Anlagenverzeichnis Kennzeichen, Seriennummern und Lieferantennamen
  entfernt sind. Für die Prüfung genügen Art des Wirtschaftsguts, Datum, Betrag,
  Nutzungsdauer und Methode;
- dass die Angaben zu Arbeitszimmer, Kfz und Privatanteilen ohne
  Gesundheitsangaben und ohne Angaben zu Angehörigen eingefügt werden. Für den
  Prüfschritt genügt die Position, nicht ihr persönlicher Hintergrund.

Taucht Zone-Rot-Material auf – eine Steuernummer im Kopf des Ausdrucks, ein
Aktenzeichen, eine vollständige IBAN in einer Bemerkung, ein Hinweis auf ein
Steuerstrafverfahren oder eine Selbstanzeige, eine Gesundheitsangabe zur
Begründung einer Position –, sofort abbrechen, den Fundort mit Position und
Spalte benennen und den Anwender bitten, die Aufstellung ohne diese Angabe neu
einzufügen. Nicht selbst überschreiben und mit dem Rest weiterrechnen. Deuten die
Angaben auf ein Strafverfahren oder eine Selbstanzeige, bleibt es beim Abbruch:
Die Bearbeitung gehört dann außerhalb des KI-Werkzeugs zu einem Berufsträger.
Dass eine bereits abgegebene Erklärung zu berichtigen ist, ist für sich genommen
kein Abbruchgrund – Zone Rot erfasst den Straf- und Selbstanzeigesachverhalt,
nicht die Berichtigung als solche.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung
des Anbieters nach § 62a StBerG müssen vor dem Einsatz geklärt sein; § 62a StBerG
geht der DSGVO-Prüfung vor. Maßstab ist `DATENSCHUTZ.md`, Zone Rot.

## Ablauf

1. **Rahmen abfragen, bevor gerechnet wird.** Mandatskürzel und Branche,
   Rechtsform, Veranlagungszeitraum, Kontenrahmen, Belegwesen und die
   Besonderheiten, die eigene Prüfpfade auslösen: Betriebseröffnung,
   Betriebsaufgabe, Wechsel der Gewinnermittlungsart, mehrere Betriebe,
   Nebentätigkeit. Branche und Rechtsform tragen den Vollständigkeitsschritt –
   ohne sie ist nicht sagbar, welche Position erwartbar wäre und fehlt.

2. **Umsatzsteuerstatus ausdrücklich nachfordern.** Regelbesteuerung,
   Kleinunternehmer, steuerfreie Umsätze oder Durchschnittssatzbesteuerung der
   Land- und Forstwirtschaft. Der Status ist ein Schalter: Er entscheidet, ob die
   Prüfung auf Brutto- oder Nettomethode geführt wird und ob der Ansatz von
   Vorsteuer überhaupt zulässig ist. Fehlt er, hier anhalten und fragen – nicht
   aus dem Zahlenbild rückschließen, weil gerade die Mischung beider Methoden der
   häufigste Fehler ist und ein Rückschluss ihn zudeckt.

3. **Schwellen erfragen, nicht setzen.** Prozentsatz und Betragsgrenze, ab denen
   eine Vorjahresabweichung berichtenswert ist, legt die Kanzlei fest. Ohne
   Angabe wird jede Abweichung ausgewiesen und der fehlende Schwellenwert
   vermerkt, statt einen zu wählen.

4. **Vollständigkeit beider Listen klären.** Enthält die Positionsliste eine
   gefüllte Vorjahresspalte, ist das Anlagenverzeichnis vollständig oder ein
   Auszug? Ohne Vorjahresspalte entfällt der Positionsvergleich und wird als
   entfallen vermerkt, nicht durch Schätzwerte ersetzt. Ist das Verzeichnis nur
   ein Auszug, unterbleibt der Summenabgleich, und aus einer Differenz wird kein
   Befund abgeleitet – die übrigen Verzeichnisprüfungen laufen auf dem Auszug
   weiter, jeder Befund trägt dann den Zusatz, dass er an der vollständigen Liste
   zu bestätigen ist.

5. **Positionsweise rechnen.** Jede Position gegen ihren Vorjahreswert stellen,
   Abweichung in Betrag **und** Prozent ausweisen, Rechenweg sichtbar lassen.
   Positionen, die im Vorjahr besetzt und jetzt leer sind, werden gesondert
   geführt – ihr Fehlen fällt in einer nach Größe sortierten Liste sonst heraus.
   Nicht auswertbare Zeilen bleiben aus den Summen heraus und werden benannt.

6. **Verhältnisse bilden.** Die Kennzahlen des Prüfschemas mit Zähler, Nenner und
   Ergebnis ausrechnen, nicht beschreiben. Jeder genannte branchenübliche Bereich
   ist ein unverifizierter Erfahrungswert und wird als solcher gekennzeichnet;
   amtliche Richtsätze werden nicht behauptet und nicht aus dem Gedächtnis
   gebildet.

7. **Anlagenverzeichnis abgleichen.** Die AfA-Beträge des Verzeichnisses zeilenweise
   addieren, der AfA-Position der EÜR gegenüberstellen und eine Differenz beziffern,
   statt sie zu erwähnen. Zusätzlich je Zeile prüfen: Zugang ohne AfA, AfA ohne
   Zugang, Abgang ohne Buchwertabgang, sofort abgezogene Beträge, die
   aktivierungspflichtig sein könnten. Jede dieser Zeilen wandert einzeln in die
   Auffälligkeitenliste.

8. **Übrige Prüfschritte in der Reihenfolge der Prompt-Datei abarbeiten.** Die
   Vollständigkeitsfrage – welche Position wäre bei dieser Branche und
   Rechtsform erwartbar und fehlt, welche ist untypisch, jeweils als Frage und
   nicht als Feststellung –, das Zu- und Abflussprinzip mit seinen Ausnahmen,
   die Umsatzsteuer in der EÜR, die Prüfliste der Zweifelsfälle und die
   formellen Abgabefragen stehen dort vollständig und werden von dort gelesen,
   nicht aus dem Gedächtnis gebildet.
   Jeder Punkt der Prüfliste wird als Frage beantwortet, auch wenn die Angabe
   fehlt – dann lautet die Antwort "Angabe fehlt" und die Frage geht in die
   Rückfragetabelle, statt zu entfallen. Ursachenaussagen sind Vermutungen und
   werden so gekennzeichnet.

9. **Grenzen niemals beziffern.** Für jede Betragsgrenze, Pauschale, Freigrenze
   und jeden Prozentsatz – geringwertige Wirtschaftsgüter, Sammelposten,
   Geschenke, Bewirtungsanteil, Tagespauschale, Verpflegungspauschalen,
   Kilometersatz, AfA-Sätze – steht der Name der Grenze und dahinter "Betrag für
   [JAHR] verifizieren". Das gilt ausnahmslos, auch wenn der Wert sicher
   erscheint. Jede rechtliche Aussage trägt Norm mit Absatz und Satz, Richtlinie
   oder BMF-Schreiben mit Datum und denselben Zusatz; ist die Fundstelle
   unsicher, "Fundstelle offen – bitte recherchieren", ist sie nicht angebbar,
   "ohne Fundstelle – vor Verwendung belegen". Alle so markierten Werte werden am
   Ende noch einmal gesammelt aufgeführt.

10. **Sortieren, begrenzen, schreiben.** Auffälligkeiten nach steuerlicher
    Auswirkung ordnen und auf die Höchstzahl der Prompt-Datei kürzen; was nicht
    zutrifft, wird weggelassen, und die Zahl der gekürzten Positionen genannt.
    Rückfragen an den Mandanten sind geschlossene Fragen in Sie-Form, mit einem
    Wort oder einem Beleg zu beantworten, jeder Fachbegriff kurz erklärt.

## Ergebnis

Eine Markdown-Datei `<Mandatskürzel>-euer-plausibilitaet-<JJJJ>.md` im
Arbeitsordner des Mandats, aufgebaut nach dem Ausgabeformat der Prompt-Datei:
Eindeutigkeit und Datenlage, nach Rang sortierte Auffälligkeiten mit Zahl,
Vermutung, Prüfschritt und steuerlicher Auswirkung, die Prüfliste der
Zweifelsfälle mit Kästchen, die Rückfragetabelle mit leerer Antwortspalte, die
interne Notiz und die Sammlung aller Werte, die vor Verwendung zu verifizieren
sind. Im Kopf stehen Veranlagungszeitraum, Rechtsform, Umsatzsteuerstatus, die
verwendeten Schwellenwerte und die Angabe, ob Vorjahresspalte und
Anlagenverzeichnis vollständig vorlagen – daran ist erkennbar, worauf die Prüfung
beruht. Die Rückfragetabelle wird für den Versand einzeln herausgezogen; die
interne Notiz geht nicht an den Mandanten.

## Qualitätssicherung

Kein Ergebnis verlässt die Kanzlei ohne menschliche Prüfung, und keine Abgabe
folgt der Auswertung ungeprüft. Vor der Freigabe:

- **Keine Betragsgrenze aus der Auswertung übernehmen.** Grenze für geringwertige
  Wirtschaftsgüter, Sammelposten, Geschenke, Bewirtungsanteil, Tagespauschale,
  Verpflegungs- und Kilometerpauschalen ändern sich; jede Zahl wird gegen den
  Rechtsstand des Veranlagungszeitraums aus einer Primärquelle verifiziert.
- Vorjahresabweichungen, Verhältniskennzahlen und die AfA-Summe selbst
  nachrechnen, Gegenprobe in der Tabellenkalkulation. Summenbildung über viele
  Zeilen bleibt die bekannteste Fehlerquelle.
- Branchenwerte der Auswertung sind keine amtlichen Richtsätze. Werden Richtsätze
  gebraucht, ist die amtliche Sammlung des betreffenden Jahres heranzuziehen.
- Vier-Augen-Prinzip: Vor der Abgabe prüft eine zweite Person die
  Auffälligkeitenliste und die Behandlung von Privatanteil, Arbeitszimmer, Kfz
  und geringwertigen Wirtschaftsgütern. Die Freigabe zur Abgabe erteilt
  ausnahmslos ein Berufsträger und ist zu dokumentieren.
- Die Plausibilitätsprüfung ersetzt weder Belegprüfung noch Kontenklärung; eine
  nicht genannte Auffälligkeit ist nicht ausgeschlossen.

Die Skill berechnet keine Fristen: weder Abgabe- und Berichtigungsfristen noch
die Zeiträume der Ausnahmen vom Zu- und Abflussprinzip. Sie benennt sie als
gesondert festzustellen.

## Grundlage

Prüfschema, Sachverhaltsbogen und Ausgabeformat stehen allein in der Prompt-Datei:
[prompts/03-jahresabschluss/21-euer-plausibilitaet.md](../../../prompts/03-jahresabschluss/21-euer-plausibilitaet.md).
