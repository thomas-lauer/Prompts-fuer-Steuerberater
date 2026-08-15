---
name: dublettenpruefung
description: Vergleicht einen Buchungs- oder Stammdatenexport zeilenübergreifend auf
  doppelte Belege und doppelt angelegte Personenkonten, hält je Treffer das erfüllte
  Kriterium und einen Sicherheitsgrad fest und schlägt je Fund eine Zusammenführung
  mit Vorprüfungen vor. Klärt vorab den Modus und die Güte der Pseudonymisierung,
  weil ein verkürztes Bankmerkmal die Prüfung wertlos macht.
  Use when a booking export or a customer/vendor master data export has to be
  screened for duplicate documents or duplicate accounts before a close, a payment
  run or a data migration.
---

# 19 – Dublettenprüfung auf Buchungs- und Stammdatenexporten

## Zweck

Der Prompt beschreibt die Kriterien, an denen eine Dublette erkennbar ist. Diese
Skill wendet sie auf den Export an: Sie stellt die Zeilen einander gegenüber,
prüft jedes Paar in der Kriterienreihenfolge, hält das erste erfüllte Kriterium
fest, vergibt den Sicherheitsgrad und schreibt die Fundliste samt
Zusammenführungsvorschlag. Der Mengenvorteil liegt nicht in der Zeilenzahl,
sondern in der Zahl der Paare: Ein Befund entsteht erst aus dem Vergleich zweier
Zeilen, die im Export weit auseinanderstehen können, und diesen Vergleich hält
von Hand niemand über einen Jahresstapel oder einen Personenkontenbestand durch.

## Wann einsetzen – und wann nicht

Einsetzen, wenn ein Buchungsexport (Modus A) oder ein Personenkonten-Stammsatz
(Modus B) auf Doppelerfassungen durchzusehen ist – vor dem Abschluss, vor einem
Zahlungslauf, nach einer Phase mit mehreren Belegkanälen oder bei der Übernahme
zweier Bestände in ein System. Wiederholt sich der Lauf, wird die Fundliste des
Vorlaufs mit eingelesen: Ausgewiesen werden dann nur neue Funde und die
Positionen, deren Erledigungsvermerk noch offen ist.

Nicht einsetzen, um Dubletten künftig zu verhindern – dafür ist Prompt 25
einschlägig, der Kontenrahmen, Nummernkreise, anlegende Rollen und die bekannten
Problemfälle des Bestands abfragt und daraus ein Regelwerk für Schreibweise,
Suchpflichten vor der Anlage und Nummernvergabe erzeugt. Der Weg ist
19 → 25: erst finden, dann die Regel setzen. Fehler, die schon bei der
Belegerfassung entstehen – falscher Kreditor, Bruttobetrag im Nettofeld,
Zahlendreher –, gehören zu Prompt 28, der Belegkreis, Belegmenge, Erfassungsweg
und Fehlerbilder abfragt und daraus eine Vier-Augen-Prüfroutine baut. Altersstruktur
und Ausfallrisiko der offenen Forderungen sind Sache von Prompt 18 und seiner
Skill; allgemeine Auffälligkeiten des Kontenbilds prüft Prompt 20 und seine Skill
am SuSa-Export. Umsätze, deren Zuordnung unklar ist und die beim Mandanten
erfragt werden müssen, gehören nicht in die Fundliste, sondern zu Prompt 02, der
aus Datum, Betrag, Verwendungszweck und Gegenseite eine gebündelte Rückfrage
erzeugt.

Diese Skill entscheidet nichts. Sie löscht, storniert und führt nichts zusammen,
sondern legt die Entscheidungsgrundlage vor.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Vor dem Einlesen des Exports bestätigen lassen:

- dass Steuer-Identifikationsnummer, Steuernummer und Aktenzeichen des
  Finanzamts entfernt sind – auch nicht maskiert, auch nicht in Kopfzeilen,
  auch nicht in einzelnen Ausschnitten. Für den Mandanten gilt das ausnahmslos;
  bei Geschäftspartnern tritt an die Stelle der Steuernummer das Kürzel nach
  dem übernächsten Punkt, der Originalwert kommt auch dort nicht mit;
- dass der Mandant nur als Mandatskürzel geführt wird und Klarnamen durch
  fortlaufende Platzhalter ersetzt sind (`Kreditor 1`, `Debitor 1`);
- dass Bank- und Steuermerkmale **pseudonymisiert, nicht verkürzt** sind: An
  die Stelle von IBAN, Umsatzsteuer-Identifikationsnummer und der Steuernummer
  eines Geschäftspartners tritt ein Kürzel, das allein die Gleichheit abbildet
  (`IBAN-A`, `IBAN-B`, `USTID-A`, `STNR-A`) – gleiche Werte durchgehend
  dasselbe Kürzel, verschiedene Werte verschiedene. Der
  Originalwert kommt nicht mit; die Zuordnungstabelle bleibt in der Kanzlei.
  Eine verkürzte Angabe (`****1234`) ist hier unbrauchbar, weil verschiedene
  Konten in den letzten Stellen übereinstimmen können – aus ihr entsteht ein
  falscher Treffer, kein gefundener;
- dass Buchungstexte und Verwendungszwecke ohne Angaben zu einzelnen Personen
  eingefügt werden. Lohn-, Unterhalts- und Gesundheitsbezüge werden vorher
  aussortiert, nicht überschrieben.

Taucht Zone-Rot-Material auf – eine vollständige IBAN in einer Stammdatenspalte,
eine echte Steuernummer im Feld für das Steuermerkmal, ein Aktenzeichen oder ein
Hinweis auf ein Steuerstrafverfahren oder eine Selbstanzeige in einer Bemerkung
–, sofort abbrechen, den Fundort mit Zeile und Spalte benennen und den Anwender
bitten, den Export mit pseudonymisierten Merkmalen und ohne diese Spalte neu zu
ziehen und erneut einzufügen. Nicht selbst überschreiben, nicht selbst
pseudonymisieren und mit dem Rest weiterarbeiten: Ein nachträglich in der
Auswertung vergebenes Kürzel bildet die Gleichheit der Originalwerte nicht ab.

Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung
des Anbieters nach § 62a StBerG müssen vor dem Einsatz geklärt sein; § 62a StBerG
geht der DSGVO-Prüfung vor. Maßstab ist `DATENSCHUTZ.md`, Zone Rot.

## Ablauf

1. **Modus festlegen – vor jedem Vergleich.** Ausdrücklich fragen, ob Modus A
   (Buchungsdubletten) oder Modus B (Stammdatendubletten) gearbeitet wird.
   Bearbeitet wird genau einer. Enthält der Export beides – Buchungszeilen mit
   angehängten Stammdatenfeldern –, wird nicht gemischt geprüft, sondern der
   Modus erfragt und nur dessen Felder ausgewertet; die gemischte Auswertung
   erzeugt Scheintreffer, weil dieselbe Rechnungsnummer bei mehreren Konten
   auftaucht.

2. **Güte der Pseudonymisierung klären.** Fragen, ob die Merkmale wertgleich
   ersetzt wurden und ob dies über den gesamten Export in einem Durchgang
   geschah. Wurde je Datei oder je Abschnitt getrennt ersetzt, sind die Kürzel
   nicht vergleichbar: Dann entfallen die Kriterien, die auf Bank- und
   Steuermerkmalen beruhen, das wird im Kopf der Ergebnisdatei vermerkt, und
   gearbeitet wird nur mit den übrigen Kriterien.

3. **Rahmen abfragen.** Mandatskürzel und Branche, Zeitraum oder Stichtag,
   Kontenrahmen, genutzte Belegkanäle und die Besonderheiten, die den
   Ausschlussteil steuern: Dauerbuchungen, Ratenzahlungen, wiederkehrende
   gleiche Beträge, mehrere Standorte mit demselben Lieferanten. Ohne diese
   Angaben ist ein gleicher Betrag am gleichen Tag nicht von einem Abschlag zu
   unterscheiden – nachfordern, nicht unterstellen. Für Modus A zusätzlich die
   beiden Werte des Rundungskriteriums erfragen: zulässige Betragsabweichung und
   Zeitfenster in Tagen. Beide setzt die Kanzlei fest, nicht die Skill. Bleiben
   sie offen, wird das darauf beruhende Kriterium nicht mit selbst gewählten
   Werten geprüft, sondern wie ein fehlendes Feld als "nicht prüfbar"
   ausgewiesen.

4. **Datenqualität je Spalte prüfen und die Kriterien freischalten.** Für jedes
   Kriterium der gewählten Modusliste festhalten, ob die dafür nötigen Felder
   vorhanden und gefüllt sind. Fehlt ein Feld – kein Erfassungsdatum, keine
   Belegquelle, kein Anlagedatum –, wird das Kriterium nicht ersatzweise über ein
   anderes Feld geprüft, sondern ausdrücklich als "nicht prüfbar" ausgewiesen.
   Zeilen ohne Betrag oder ohne Datum werden gesondert gelistet und aus dem
   Vergleich herausgehalten, damit sie nicht als leere Treffer erscheinen.

5. **Paarweise durch die Kriterienliste.** Die Kriterien des gewählten Modus
   stehen vollständig in der Prompt-Datei und werden von dort gelesen, nicht aus
   dem Gedächtnis gebildet. Sie werden in ihrer Reihenfolge abgearbeitet: Jede
   Zeile wird gegen die übrigen gestellt, das erste erfüllte Kriterium wird
   festgehalten und der Vergleich für dieses Paar beendet. Kein Treffer ohne
   benanntes Kriterium – eine Ähnlichkeit, die sich an keinem Kriterium
   festmachen lässt, wird nicht behauptet, sondern weggelassen. Zusammenhängende
   Ketten (drei Zeilen zum selben Vorgang) werden als ein Fund geführt.

6. **Gegenprobe gegen den Ausschlussteil.** Jeder Treffer des Modus A läuft
   anschließend gegen die Liste dessen, was die Prompt-Datei ausdrücklich als
   keine Dublette abgrenzt – wiederkehrende Zahlungen, Raten, Sammelrechnungen,
   Storno plus Neubuchung. Was daran hängenbleibt, wandert nicht aus der Datei,
   sondern in den eigenen Abschnitt "ausdrücklich keine Dublette" mit der
   Begründung. Diese Liste ist der Nachweis, dass geprüft und nicht übersehen
   wurde. Gleicher Name bei abweichendem Ort ist im Modus B kein Ausschluss,
   sondern das letzte Kriterium der Modusliste: Solche Paare bleiben in der
   Fundliste und tragen den ausdrücklichen Vermerk, dass hier ein echter
   Unterschied vorliegen kann (Filialen, Namensgleichheit), samt dem Prüfschritt,
   mit dem sich das in der Kanzlei entscheiden lässt.

7. **Sicherheitsgrad vergeben.** Nach den Vorgaben der Prompt-Datei
   (Anforderung 2) und ohne Aufrundung: Beruht ein Treffer nur auf
   Namensähnlichkeit oder auf pseudonymisierten Bank- und Steuermerkmalen, ist
   der höchste zulässige Grad "wahrscheinlich", und als Prüfschritt wird der
   Abgleich der vollständigen Werte in der Kanzlei genannt.

8. **Zusammenführung vorschlagen.** Je Fund: welcher Datensatz führend bleibt,
   mit Begründung aus den Daten (ältestes Anlagedatum, vollständigste Felder,
   bebucht), was mit dem anderen geschieht und was vorher zu prüfen ist – offene
   Posten, laufende Zahlungsläufe, Mahnstufen, Vorjahresbezug. Lässt sich der
   führende Satz aus den Daten nicht bestimmen, wird das als offene Frage
   ausgewiesen, statt einen zu wählen.

9. **Begrenzen, sortieren, schreiben.** Auf die Höchstzahl der Prompt-Datei
   kürzen, nach Sicherheitsgrad und dann nach Betrag sortieren und die Zahl der
   nicht in die Liste aufgenommenen Kandidaten nennen, damit erkennbar bleibt,
   dass gekürzt wurde. Kontonummern gelten nicht als gesichert; Jahreswerte und
   Betragsgrenzen tragen den Zusatz "für [JAHR] verifizieren". Jede rechtliche
   Aussage trägt Norm mit Absatz und Satz, Richtlinie oder BMF-Schreiben mit
   Datum und denselben Zusatz; ist die Fundstelle unsicher, "Fundstelle offen –
   bitte recherchieren", ist sie nicht angebbar, "ohne Fundstelle – vor
   Verwendung belegen".

## Ergebnis

Eine Markdown-Datei `<Mandatskürzel>-dubletten-modus-<a|b>-<JJJJ-MM>.md` im
Arbeitsordner des Mandats, aufgebaut nach dem Ausgabeformat der Prompt-Datei:
Datenqualität, Fundliste, ausdrücklich keine Dublette, interne Notiz mit
Bereinigungsreihenfolge und Risiken, unsichere Punkte. Im Kopf stehen Modus,
Zeitraum oder Stichtag, Kontenrahmen, die Angabe zur Güte der Pseudonymisierung,
die Zahl der verglichenen und der nicht auswertbaren Zeilen und die Kriterien,
die mangels Feld nicht geprüft werden konnten – daran ist erkennbar, worauf sich
das Ergebnis stützt. Jede Zeile der Fundliste hat die Spalten "geprüft von / am"
und "erledigt", damit die Liste die Bereinigung begleitet und im nächsten Lauf
fortgeschrieben werden kann. Die interne Notiz geht nicht an den Mandanten.

## Qualitätssicherung

Kein Ergebnis verlässt die Kanzlei ohne menschliche Prüfung, und keine
Bereinigung folgt der Fundliste ungeprüft. Vor der Umsetzung:

- **Niemals löschen.** Weder eine Buchung noch ein Personenkonto wird aufgrund
  dieser Auswertung gelöscht. Buchungen werden storniert oder umgebucht, Konten
  gesperrt und erst danach zusammengeführt, jeweils mit Beleg über den Vorgang.
  Ein festgeschriebener Stapel wird nicht nachträglich verändert – die
  Unveränderbarkeits- und Aufbewahrungspflichten der GoBD gelten unberührt.
- Auch jeden Fund mit dem Grad "sicher" am Originalbeleg prüfen. Gleicher Betrag
  am gleichen Tag ist bei Abschlägen, Filialen und Raten der Normalfall.
- Vor jeder Zusammenführung von Personenkonten offene Posten, laufende
  Mahnungen, Zahlungsläufe, Vorjahresbestände und Bezüge in Anlagen- oder
  Vertragsverwaltung prüfen. Eine Zusammenführung im laufenden Jahr kann
  Vorjahresvergleiche zerstören.
- Treffer, die auf Pseudonymen beruhen, gegen die vollständigen Werte in der
  Kanzlei abgleichen, bevor sie als gesichert gelten.
- Vier-Augen-Prinzip: Die Bereinigung führt eine andere Person durch als die,
  die die Fundliste erstellt hat; die Freigabe zeichnet ein Berufsträger ab und
  wird dokumentiert.

Die Skill berechnet keine Fristen: weder Aufbewahrungs- noch Berichtigungs- oder
Festschreibungsfristen. Sie benennt den Prüfschritt, nicht den Termin.

## Grundlage

Kriterien, Sachverhaltsbogen und Ausgabeformat stehen allein in der Prompt-Datei:
[prompts/01-finanzbuchhaltung/19-dublettenpruefung.md](../../../prompts/01-finanzbuchhaltung/19-dublettenpruefung.md).
