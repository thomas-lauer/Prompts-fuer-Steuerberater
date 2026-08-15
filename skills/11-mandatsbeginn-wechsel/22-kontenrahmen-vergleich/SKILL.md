---
name: kontenrahmen-vergleich
description: Arbeitet den Kontenplan oder die Summen- und Saldenliste des Vorberaters
  Zeile für Zeile durch, ordnet jedes Konto über seine Funktion einem Bilanz- oder
  GuV-Posten des Zielkontenrahmens zu, gleicht eine vorliegende Überleitungsliste als
  Mengenvergleich dagegen ab und rechnet die Summenprobe über alle Salden. Prüft vorab,
  ob Anlass und Umstellungszeitpunkt zusammenpassen, und fordert Rechtsform,
  Gewinnermittlung und Zielkontenrahmen nach, weil ohne sie kein Zielposten benennbar
  ist. Use when a predecessor's chart of accounts has to be mapped to SKR03 or SKR04
  after taking over a client or before switching the chart of accounts.
---

# 22 – Kontenrahmen-Vergleich SKR03 ↔ SKR04 bei Mandatsübernahme

## Zweck

Der Prompt beschreibt die Zuordnungslogik. Diese Skill wendet sie auf den
vorliegenden Kontenplan an: Sie geht jede Kontenzeile durch, leitet die Funktion
aus Bezeichnung und Saldo ab, benennt den Ziel-Bilanz- oder GuV-Posten und
kennzeichnet, wie sicher die Zuordnung ist. Der Mengenvorteil liegt in der
Zeilenzahl eines Kontenplans und darin, dass zwei Listen gegeneinander zu halten
sind: Erst der Abgleich aller Altkonten gegen alle Ziele der vorliegenden
Überleitungsliste zeigt Konten ohne Ziel, Ziele ohne Quelle und
Zusammenfassungen, die Information vernichten. Dazu kommt die Summenprobe über
sämtliche Salden, die von Hand niemand für jede Zwischenfassung neu rechnet.

## Wann einsetzen – und wann nicht

Einsetzen, wenn ein Kontenplan oder eine SuSa des Vorberaters vorliegt und
entweder in den eigenen Kontenrahmen überführt oder auf Kontierungsgewohnheiten
durchgesehen werden soll – bei Mandatsübernahme, bei Kontenrahmenwechsel oder
bei beidem. Auch geeignet, wenn eine Überleitungsliste bereits existiert und
geprüft werden soll, bevor Eröffnungswerte übernommen werden.

Nicht einsetzen, wenn nicht die Zuordnung das Problem ist, sondern die
Herausgabe: Wer welche Bestände, Nachweise und Verzeichnisse vom Vorberater
verlangen kann, wie der Stand der Vollmachten und offener Verfahren aufzunehmen
ist und was die Kanzlei beim eigenen Mandatsende herausgeben muss, steht in
Prompt 69, der Übernahmezeitpunkt, betroffene Bereiche, gelieferte Bestände und
Honorarforderungen des Vorberaters abfragt. Bei einer Neugründung ohne
Vorberater gibt es keinen Altkontenplan – dort führt Prompt 68 durch die
Weichenstellungen des Fragebogens zur steuerlichen Erfassung. Bleibt der
Kontenrahmen unverändert und soll nur der laufende Bestand auf Auffälligkeiten
durchgesehen werden, ist Prompt 20 der Einstieg, der Verkehrszahlen und
Vorjahreswerte verlangt; für die Plausibilität der EÜR-Positionen mit
Anlagenverzeichnis, Kfz und Privatanteilen Prompt 21. Diese Skill ersetzt weder
die Kontenklärung noch die Prüfung der Eröffnungsbilanzwerte.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Vor dem Einlesen des Kontenplans bestätigen lassen:

- dass Steuer-Identifikationsnummer, Steuernummer und Aktenzeichen des
  Finanzamts entfernt sind – auch nicht maskiert, auch nicht in Kopf- oder
  Fußzeilen des Exports und auch nicht in Ausschnitten;
- dass Mandantenname und Beraternummer entfernt sind und der Mandant nur als
  Mandatskürzel geführt wird, ebenso der bisherige Berater nur als
  `Vorberater`;
- dass Personenkonten maskiert sind (`Debitor 1`, `Kreditor 1`) oder als eine
  Zeile je Kontengruppe zusammengefasst eingefügt werden. Beides ist zulässig,
  solange der Saldo enthalten bleibt – ohne ihn bricht die Summenprobe in
  Schritt 7. Maskierung konsistent über alle Zeilen hinweg.

Für die Zuordnung genügen Kontobezeichnung, Kontengruppe und Saldo. Häufiger
Fund in genau diesen Exporten: Bankkonten tragen die vollständige IBAN in der
Kontobezeichnung – die gehört nicht hinein, `Konto ****1234` genügt. Erscheint
Zone-Rot-Material – eine Steuernummer in der Exportkopfzeile, ein Aktenzeichen
in einer Bemerkungsspalte, eine vollständige IBAN in einer Kontobezeichnung, ein
Hinweis auf ein Steuerstrafverfahren oder eine Selbstanzeige in einer Notizspalte
–, sofort abbrechen, den Fundort mit Zeile und Spalte nennen und den Anwender
bitten, den Export ohne Kopfzeile und ohne diese Spalte neu zu ziehen. Nicht
selbst entfernen und weiterarbeiten.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung
des Anbieters nach § 62a StBerG müssen vor dem Einsatz geklärt sein; § 62a StBerG
geht der DSGVO-Prüfung vor. Maßstab ist `DATENSCHUTZ.md`, Zone Rot.

## Ablauf

1. **Anlass und Umstellungszeitpunkt zusammen prüfen – vor jeder Zuordnung.**
   Anlass, Umstellungsdatum und Wirtschaftsjahr abfragen und gegeneinander
   halten, nach dem Hinweis im Abschnitt RAHMEN der Prompt-Datei. Passt beides
   nicht zusammen, ist das der erste Befund, und die Arbeit wird in zwei
   getrennte Ergebnisteile geteilt – unterjährige Übernahme im bisherigen
   Kontenrahmen einerseits, Kontenrahmenwechsel zum nächsten Wirtschaftsjahr
   andererseits. Fehlt Umstellungsdatum oder Wirtschaftsjahr, anhalten und
   nachfragen; kein Datum aus dem Auftragsdatum oder aus Saldenständen ableiten.

2. **Rahmen abfragen.** Branche, Rechtsform, Gewinnermittlung (Bilanz oder EÜR),
   Ausgangskontenrahmen, Zielkontenrahmen und Besonderheiten wie individuelle
   Konten des Vorberaters, mehrere Betriebsstätten, Betriebsaufspaltung oder
   Anlagenbuchführung im Vorsystem. Rechtsform und Gewinnermittlung schalten die
   Zielposten frei: Ohne sie ist nicht entscheidbar, welche Eigenkapital- und
   Privatkonten überhaupt geführt werden dürfen und gegen welche Gliederung
   zugeordnet wird. Fehlt eines der beiden oder der Zielkontenrahmen, anhalten
   und nachfragen – nicht aus dem Kontenbild rückschließen. Ist der
   Ausgangskontenrahmen kein Standardkontenrahmen, wird die Funktion jedes
   Kontos allein aus Bezeichnung und Saldo abgeleitet, und das gilt für den
   gesamten Lauf.

3. **Vollständigkeit der Liste klären.** Ausdrücklich fragen: Enthält der Export
   alle Konten mit Saldo, oder ist er ausschnittweise oder verdichtet eingefügt?
   Die Frage steht am Anfang und wird nicht aus der Zeilenzahl geraten. Ist die
   Liste unvollständig, unterbleibt die Summenprobe in Schritt 7, und aus dem
   Fehlen eines Kontos wird kein Befund abgeleitet – weder "Konto ohne Ziel" noch
   "Ziel ohne Quelle" in Schritt 6. Die übrigen Schritte laufen normal weiter,
   jeder Befund trägt dann den Zusatz "auf Ausschnitt festgestellt – an der
   vollständigen Liste im Programm zu bestätigen".

4. **Gliederungsprinzip schreiben.** Zuerst den Fließtext nach Anforderung 1 der
   Prompt-Datei, ohne Kontonummern und innerhalb des dort gesetzten
   Wortumfangs. Er steht vor der Tabelle, weil die Begründungen der einzelnen
   Zuordnungen darauf zurückgreifen.

5. **Zeilenweise zuordnen.** Jede Kontenzeile durch dasselbe Raster: Funktion aus
   Bezeichnung und Saldo, Ziel-Bilanz- oder GuV-Posten, Sicherheitsgrad der
   Zuordnung in der dreistufigen Kennzeichnung des Prompts, Begründung, und was
   im Programm nachzuschlagen ist. Kontonummern werden nie als gesichert
   ausgegeben; wird eine genannt, steht der wörtliche Zusatz aus Anforderung 2
   der Prompt-Datei dahinter. Die Tabelle ist auf die dort genannte Höchstzahl
   von Positionen begrenzt: nach Saldenhöhe und Fehlerrisiko auswählen und
   danach ausdrücklich festhalten, wie viele Konten nicht aufgenommen wurden und
   welchen Anteil an der Summe der Salden sie ausmachen. Eine Zeile, die ohne
   weitere Angaben nicht entscheidbar ist, wird so gekennzeichnet und wandert in
   die Fragenliste an den Vorberater – sie wird nicht geraten.

6. **Vorliegende Überleitungsliste gegenhalten.** Nur wenn eine Liste eingefügt
   wurde. Beide Listen als Mengen vergleichen: jedes Altkonto ohne Ziel, jedes
   Ziel ohne Quelle, jede Zusammenfassung mehrerer Altkonten auf ein Ziel. Dazu
   je Position die Prüfpunkte aus Anforderung 3 der Prompt-Datei –
   funktionsfremde Zuordnung, Vorzeichenverwechslung, Auswirkung auf
   Vorjahresvergleich und bestehende Auswertungen. Liegt keine Überleitungsliste
   vor, entfällt dieser Teil, und das wird im Ergebnis ausdrücklich vermerkt: Die
   eigene Zuordnung aus Schritt 5 ist ein Vorschlag und wird nicht als geprüfte
   Überleitung ausgegeben.

7. **Summenprobe rechnen.** Nur bei vollständiger Liste: Soll- und Habensumme der
   Ausgangssalden gegen die Summe der zugeordneten Salden, getrennt und mit
   sichtbarem Rechenweg. Gerechnet wird über alle in Schritt 5 zugeordneten
   Zeilen, nicht über die auf die Höchstzahl gekürzte Tabelle – sonst entsteht
   eine Differenz, die allein aus der Kürzung stammt. Zeilen, deren Zuordnung
   offen geblieben ist, gehen mit ihrem Saldo als eigener Posten in die Probe
   ein, damit sie aufgeht und die offene Summe zugleich sichtbar bleibt. Eine
   Abweichung ist der wichtigste Befund und vor der Übernahme der
   Eröffnungswerte zu klären. Diese Rechnung erfolgt auf der
   eingefügten Liste und ersetzt die Summenprobe im Programm nach Anlage der
   Überleitung nicht – das steht als Satz im Ergebnis.

8. **Unübliche Kontierungen sammeln.** Nach dem Raster von Anforderung 4 der
   Prompt-Datei, begrenzt auf die dort genannte Höchstzahl, nach Risiko sortiert.
   Jede Bewertung als gekennzeichnete Vermutung mit dem zugehörigen Prüfschritt,
   nie als Feststellung.

9. **Zwei Fragelisten trennen.** Systematikfragen an den Vorberater,
   Sachverhaltsfragen an den Mandanten, beide geschlossen formuliert. Jede in
   Schritt 5 als nicht entscheidbar gekennzeichnete Zeile muss sich in einer der
   beiden Listen wiederfinden. Im Ergebnis der Hinweis, dass die Fragen an den
   Vorberater zeitnah zu stellen sind – nach Mandatsende sind Antworten schwer zu
   bekommen.

10. **Ergebnis schreiben.** Aufbau nach dem Ausgabeformat der Prompt-Datei. Jede
    rechtliche Aussage trägt ihre Fundstelle mit dem Zusatz "für [JAHR]
    verifizieren"; ist sie unsicher, "Fundstelle offen – bitte recherchieren",
    ist sie nicht angebbar, "ohne Fundstelle – vor Verwendung belegen". Jeder
    genannte Jahreswert, Grenzbetrag und Steuersatz erhält den Zusatz "Wert für
    [JAHR] verifizieren".

## Ergebnis

Eine Markdown-Datei `<Mandatskürzel>-kontenueberleitung-<JJJJ-MM-TT>.md` im
Arbeitsordner des Mandats, mit dem Umstellungsdatum im Dateinamen. Aufbau nach
dem Ausgabeformat der Prompt-Datei: Gliederungsprinzip, Überleitungstabelle,
Befunde zur vorliegenden Überleitungsliste, unübliche Kontierungen, Fragen an den
Vorberater, Fragen an den Mandanten, interne Notiz und die unsicheren Punkte. Im
Kopf stehen Anlass, Ausgangs- und Zielkontenrahmen, Rechtsform,
Gewinnermittlung, Umstellungszeitpunkt und Wirtschaftsjahr, die beantwortete
Vollständigkeitsfrage, das Ergebnis der Summenprobe oder der Grund ihres
Unterbleibens sowie die Angabe, ob eine Überleitungsliste vorlag.

Die Überleitungstabelle bekommt je Zeile eine Spalte für Erledigungsvermerk und
Handzeichen. Sie ist das Arbeitspapier der Umstellung und wird fortgeschrieben:
Wird eine Zuordnung nach Antwort des Vorberaters geändert, wird die Zeile
ergänzt, nicht überschrieben, damit nachvollziehbar bleibt, worauf die Änderung
beruht.

## Qualitätssicherung

Kein Ergebnis verlässt die Kanzlei ohne menschliche Prüfung. Vor der Freigabe:

- Keine Kontonummer aus der Auswertung übernehmen. Jede Nummer aus dem
  Standardkontenrahmen in der eingesetzten Version und aus dem individuellen
  Kontenplan des Mandanten ziehen; das Modell erzeugt hier plausible, aber
  falsche Nummern, und das ist die häufigste Fehlerart dieser Auswertung.
- Die Zuordnung am Bilanz- und GuV-Posten prüfen, nicht an der Nummer – die
  Zuordnungslogik ist die eigentliche Leistung.
- Die Summenprobe im Programm wiederholen, nachdem die Überleitung angelegt ist,
  getrennt nach Soll und Haben, und mit einem Probemonat testen. Abweichungen
  vor der Übernahme der Eröffnungswerte klären.
- Vorjahresvergleich, BWA-Zuordnung, Kostenstellen und Anlagenspiegel nach der
  Umstellung gegenprüfen; sie hängen an der Zuordnung und brechen still.
- Vier-Augen-Prinzip: Eine zweite Person prüft die Überleitungsliste, der
  Berufsträger gibt sie frei, bevor Eröffnungswerte übernommen werden. Die
  Freigabe ist zu dokumentieren.

Die Skill entscheidet nicht über den Umstellungszeitpunkt und berechnet keine
Fristen – weder Abgabe- noch Berichtigungsfristen und keine Aussage dazu, bis
wann eine Umstellung vollzogen sein muss. Sie stellt nur fest, ob der angegebene
Zeitpunkt zum angegebenen Anlass passt, und benennt eine Unstimmigkeit als
Befund. Über Bilanzansätze und Wahlrechte des Vorberaters entscheidet sie
ebenfalls nicht; sie macht sie sichtbar und stellt die Frage.

## Grundlage

Zuordnungslogik, Sachverhaltsbogen und Ausgabeformat stehen allein in der
Prompt-Datei:
[prompts/11-mandatsbeginn-wechsel/22-kontenrahmen-vergleich.md](../../../prompts/11-mandatsbeginn-wechsel/22-kontenrahmen-vergleich.md).
