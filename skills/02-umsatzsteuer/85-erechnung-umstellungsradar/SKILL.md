---
name: erechnung-umstellungsradar
description: Führt den Mandantenstamm profilweise durch das Prüfschema aus Prompt 85
  und segmentiert ihn danach, welcher Zweig der Übergangsregelung des § 27 Abs. 38 UStG
  auf welches Profil zutrifft: Ausstellungspflicht ja oder nein, Ausnahme kraft
  Verordnung, EDI-Fall, Zweifelsfall nahe der Schwelle. Erzeugt eine fortschreibbare
  Übersicht mit Handlungsbedarf je Mandat, den Umstellungsplan je Profil und das
  Dokumentationsraster für die Empfängerseite; sie vergleicht keinen Betrag mit einer
  Schwelle und nennt kein Datum. Use when a Steuerkanzlei wants to sort its client base
  by e-invoicing deadline, plan the changeover, or document why an incoming paper
  invoice was accepted during the transition period.
---

# 85 – E-Rechnungs-Umstellungsradar: Stichtag je Mandant bestimmen

## Zweck

Der Prompt beurteilt ein Mandantenprofil. Die Skill macht daraus ein Radar über den
Stamm: Sie nimmt beliebig viele Profile entgegen, führt **jedes einzeln** durch
dieselben Prüfschritte und verdichtet die Ergebnisse zu einer Segmentierung –
welches Mandat welchem Zweig der Übergangsregelung zuzuordnen ist, wer nur
empfangspflichtig ist, wer über eine EDI-Strecke abrechnet und welche Mandate nahe
an der Schwelle liegen und deshalb ein Mensch ansprechen muss.

Sie ist auf Fortschreibung angelegt. Ein Profil, dessen Vorjahresumsatz noch
vorläufig ist, bleibt in der Zweifelsfallliste und wird beim nächsten Lauf erneut
geführt; der Bestand wächst nicht zu einer Sammlung von Einzelvermerken, sondern
bleibt eine Liste mit einem Stand. Was die Skill dabei ausdrücklich **nicht** tut:
einen Betrag mit einer Schwelle vergleichen und daraus einen Stichtag ableiten. Sie
gibt die Entscheidungsregel mit beiden Zweigen aus; den Abgleich nimmt die Kanzlei
vor, und die Skill hält fest, dass und mit welchem Ergebnis er vorgenommen wurde.

## Wann einsetzen – und wann nicht

**Einsetzen**, wenn der Mandantenstamm nach Umstellungsbedarf sortiert werden soll,
wenn für ein einzelnes Mandat geklärt werden muss, welcher Zweig der
Übergangsregelung greift und was bis dahin zu erledigen ist, oder wenn die
Empfängerseite eine Beweisvorsorge für im Übergangszeitraum erhaltene sonstige
Rechnungen braucht.

**Nicht einsetzen:**

- **Der Mandant soll informiert werden:** Prompt 12. Er arbeitet mit Mandantentyp,
  geschätztem Vorjahresumsatz, heutiger Rechnungspraxis und eingesetzter Software
  und erzeugt daraus ein Serienschreiben. Er informiert; das Radar entscheidet die
  Zuordnung, die dem Schreiben zugrunde liegt.
- **Eine EDI-Strecke ist technisch zu prüfen:** Prompt 115. Er verlangt Format mit
  Versionsstand und Nachrichtentyp, EDI-Dienstleister, bestehende Vereinbarung mit
  Datum, Zustimmungsnachweis des Empfängers und das Ergebnis eines
  Extraktionstests. Hier steht nur, ob EDI-Vereinbarungen bestehen und mit wie
  vielen Partnern.
- **Eine eingegangene E-Rechnung ist fehlerhaft:** Prompt 86. Er arbeitet mit dem
  Wortlaut der Fehlermeldung, Regelkennung, Feldbezeichnung, Schweregrad und
  Versionsstand des Validierungswerkzeugs – ein Beleg, kein Bestand.
- **Anzahlungen, Schlussrechnung oder Berichtigung im strukturierten Format:**
  Prompt 114. Er verlangt je Anzahlung Zeitpunkt, Betrag, Format und die Angabe, ob
  die Rechnung die Pflichtangaben enthielt – eine Rechnungskette, kein Profil.
- **Der Prozess ist zu beschreiben und zu kontrollieren:** Prompt 116. Er fragt
  Eingangskanäle und Formate, Belegzahl im Monat, Systeme je Prozessschritt, wer
  prüft und wer freigibt sowie den Archivweg ab und erzeugt Verfahrensdokumentation
  und Kontrollmatrix.
- **Der Status als Kleinunternehmer ist zu überwachen:** Prompt 88. Er verlangt
  Vorjahresumsatz, aufgelaufenen Umsatz mit Stichtag und den bereits von der Kanzlei
  vorgenommenen Vergleich mit beiden Grenzen. Hier wird die Sonderstellung nur als
  Ausnahmefrage geprüft, nicht der Statuswechsel begleitet.

## Vor dem ersten Arbeitsschritt: Datensparsamkeit

Die Skill bekommt die Profile unmittelbar; niemand maskiert vorher. Deshalb zuerst:

1. Bestätigung einholen, dass Steuernummer, Steuer-Identifikationsnummer,
   Umsatzsteuer-Identifikationsnummer und Aktenzeichen des Finanzamts vollständig
   entfernt sind – nicht teilmaskiert, nicht in Ausschnitten, auch nicht in
   Ausschnitten aus Rechnungen oder Prüfprotokollen.
2. Nur neutrale Kennungen: `Mandant A`, `Lieferant 1`, `Kunde Inland 1`. Anschriften
   und Firmierungen entfallen; für die Einordnung genügen Größenklasse,
   Umsatzstruktur, Empfängerkreis und eingesetzte Software.
3. **Der Betrag selbst wird nicht gebraucht.** Die Skill vergleicht ihn ohnehin
   nicht mit der Schwelle. Es genügt die Angabe, ob die Kanzlei den Abgleich
   vorgenommen hat und mit welchem Ergebnis – darüber, darunter oder nahe daran –
   samt der Herleitung, aus welcher Auswertung sie stammt. Wird der Betrag dennoch
   mitgeliefert, wird er nicht in die Ergebnisdatei übernommen.
4. Taucht Zone-Rot-Material auf, wird angehalten, nicht bereinigt. Die Rückmeldung
   nennt Zeile und Feld und sagt, welche Fassung genügt: Kürzel, Ansässigkeit,
   Rechtsform, Branche, Umsatzsteuerstatus, Anteile nach Empfängerkreis und
   Steuerpflicht, Rechnungsarten, Software, EDI-Lage, Rechnungseingang und Archivweg.
5. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung
   des Anbieters nach § 62a StBerG (sorgfältige Auswahl, Vertrag in Textform mit
   Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das
   Erforderliche) müssen vor dem Einsatz geklärt sein; bei unmittelbarem Einsatz für
   ein konkretes Mandat klärt der Berufsträger vorab § 62a Abs. 5 StBerG.
   Einzelheiten in `DATENSCHUTZ.md`.

## Ablauf

1. **Datensparsamkeit abschließen.** Ohne die Bestätigung wird kein Profil
   aufgenommen.
2. **Lauf einrichten:** Zahl der zu bearbeitenden Profile, Stand des letzten Laufs,
   ob es sich um einen Erstlauf oder eine Fortschreibung handelt. Bei einer
   Fortschreibung wird die Zweifelsfallliste des Vorlaufs vorangestellt und zuerst
   abgearbeitet – sie ist der Grund, warum es einen zweiten Lauf gibt.
3. **Profile formal prüfen.** Fehlt in einem Profil ein Feld des Bogens der
   Prompt-Datei, wird es nachgefordert und nicht ergänzt – mit einer Ausnahme:
   An die Stelle des Betragsfelds tritt hier das Ergebnis des von der Kanzlei
   vorgenommenen Abgleichs samt Herleitung; fehlt dieses, wird es nachgefordert,
   nicht der Betrag. Ist die Umsatzstruktur
   unklar, wird für dieses Profil **nicht** entschieden. Die Zahl der eingegangenen
   Profile wird gegen die angekündigte gehalten; die Differenz gehört in die
   fehlenden Angaben.
4. **Eindeutigkeit je Profil einschätzen** und fehlende Angaben einzeln benennen,
   bevor irgendein Zweig zugeordnet wird.
5. **Profilweise prüfen.** Jedes Profil durchläuft die neun Prüfschritte der
   Prompt-Datei in deren Reihenfolge – von der Unternehmereigenschaft und
   Inlandsansässigkeit über die Frage, ob überhaupt pflichtige Umsätze vorliegen,
   die Ausnahmen kraft Verordnung und die Bemessungsgröße bis zu EDI, Umstellungsplan,
   Empfängerseite und den Folgen für den Vorsteuerabzug. Schema und Fundstellen
   stehen dort und werden hier nicht wiederholt. Kein Profil wird
   zusammengefasst oder übersprungen; nach dem letzten meldet die Skill, wie viele
   sie bearbeitet hat.
6. **Ergebnis je Profil als Entscheidungsregel ausgeben, nicht als Datum.** Beide
   Zweige stehen nebeneinander mit ihren Folgen. Hat die Kanzlei den Abgleich bereits
   vorgenommen, wird der zutreffende Zweig als „von der Kanzlei festgestellt"
   gekennzeichnet und der andere sichtbar gelassen. Die Skill vergleicht selbst
   keinen Betrag, rechnet keine Frist und nennt kein Datum – auch dann nicht, wenn
   die Zahl im Profil steht.
7. **Segmentieren.** Aus den Einzelergebnissen entsteht die Übersicht mit einer
   Zeile je Mandat: Kürzel, zutreffender Zweig oder Zweifelsfall, Handlungsbedarf,
   Ansprechzeitpunkt der Kanzlei, offene Frage. Gleichartige Profile werden zu
   Gruppen zusammengefasst; das Sortierkriterium wird ausdrücklich genannt.
8. **Zweifelsfälle gesondert führen.** Nahe an der Schwelle, vorläufiger
   Vorjahresumsatz, unklare Behandlung von Sondervorgängen, unklare Umsatzstruktur:
   Diese Mandate kommen in eine eigene Liste mit der Angabe, welche Feststellung die
   Entscheidung herbeiführt. Ein Zweig auf vorläufiger Grundlage ist kein Ergebnis,
   sondern eine Vermutung, und wird als solche gekennzeichnet.
9. **Empfangspflicht getrennt ausweisen.** Auch Profile ohne eigene
   Ausstellungspflicht bekommen eine Zeile – die Empfangspflicht besteht unabhängig
   davon und ist der häufigste Irrtum im Mandantengespräch.
10. **Umstellungsplan je Profil oder Profilgruppe:** höchstens zehn Maßnahmen,
    sortiert nach dem spätestmöglichen Beginn, abhakbar mit ☐, ohne alles, was auf
    das Profil nicht passt. Formatnamen, Versionen und ausgeschlossene Profile
    stehen nur als nachzuschlagende Angabe.
11. **Dokumentationsraster für die Empfängerseite erzeugen** – leer, mit den Spalten
    der Prompt-Datei. Es ist die Beweisvorsorge und wird in der Kanzlei laufend
    geführt, nicht bei jedem Lauf neu erzeugt; die Skill weist es deshalb als
    Vorlage zur einmaligen Ablage aus.
12. **Offene Rechtslage, Fristarten und interne Notiz** nach dem Ausgabeformat der
    Prompt-Datei, dann ablegen. Fristarten werden benannt, nicht berechnet, je mit
    dem Hinweis, dass ein Mensch sie berechnet und im Fristenprogramm erfasst.

## Ergebnis

Eine Datei `erechnung-umstellungsradar-<JJJJ-MM>.md` für den stammweiten Lauf, bei
der Beurteilung eines einzelnen Mandats `<Mandatskürzel>-erechnung-stichtag-<JJJJ-MM>.md`.
Jede Fortschreibung ist eine neue Datei mit neuem Monatsstand; die vorige bleibt
stehen, damit nachvollziehbar ist, wann ein Mandat den Zweig gewechselt hat.

Inhalt in der Reihenfolge des Ausgabeformats der Prompt-Datei: Eindeutigkeit und
Datenlage, Prüfprotokoll je Profil mit Rechtsgrundlage, Ergebnis als
Entscheidungsregel, Segmentierungsübersicht mit einer Zeile je Mandat,
Zweifelsfallliste, Umstellungsplan mit ☐, Dokumentationsraster für die
Empfängerseite, Fristarten und Stichtagsarten mit Rechtsgrundlage, offene
Rechtslage, interne Notiz und – als letzter Abschnitt, wie im Ausgabeformat
vorgesehen – was unsicher geblieben ist.
Das Dokumentationsraster wird als Vorlage entnommen; alles Übrige bleibt intern.

## Qualitätssicherung

Das Ergebnis ist ein Entwurf und kennt nur, was in den Profilen stand.

- **Vier-Augen-Prinzip:** Eine zweite fachkundige Person nimmt Bemessungsgröße,
  Zuordnung des Zweiges und EDI-Beurteilung nach, vorrangig bei den Zweifelsfällen.
  Jede Mitteilung an den Mandanten und jede Umstellungszusage gibt ein Berufsträger
  frei (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Die Skill vergleicht nichts und berechnet nichts:** kein Abgleich des Umsatzes
  mit der Schwelle, keine Frist, kein Datum, keine Dauer. Bemessungsgröße, Bezugsjahr
  und Netto- oder Bruttobetrachtung werden am Gesetzestext und an den BMF-Schreiben
  nachgelesen; ein aus dieser Ausgabe übernommener Stichtag ist wertlos.
- **Sondervorgänge im Vorjahresumsatz prüft ein Mensch.** Maßgeblich ist der
  Gesamtumsatz nach der Verweisungsnorm des § 27 Abs. 38 UStG, nicht die Summe der
  Erlöskonten; Verweisung und Absatz haben sich mit der Neufassung verschoben und
  sind am Gesetzestext nachzulesen.
- **Empfangspflicht und Ausstellungspflicht getrennt halten.** Wer keinen eigenen
  Zweig hat, ist trotzdem empfangspflichtig – prüfen, dass die Übersicht das für
  jedes Mandat ausweist.
- **Keine Formatnorm als Inhalt des § 14 UStG.** Welche Norm oder Fundstelle die
  Formatanforderung trägt, wird in der Prompt-Datei nachgeschlagen und nicht aus dem
  Gedächtnis ergänzt; die technische Prüfung einer Strecke ist Prompt 115.
- **Die Empfängerseite ist nicht abschließend geklärt.** Solange die
  Verwaltungsauffassung offen ist, ersetzt die Dokumentation die Sicherheit. Keine
  Aussage gegenüber dem Mandanten, eine Papierrechnung sei „unproblematisch"; keine
  Ausgabe, die eine offene Frage als entschieden darstellt.
- **Vermutungen kennzeichnen:** Jede Aussage zur Umsatzhöhe, die nicht aus einer
  Auswertung folgt, steht ausdrücklich als Vermutung.
- **Zone Rot auch in der Ausgabe kontrollieren:** keine Nummer, kein Aktenzeichen,
  keine Firmierung, auch nicht im Dokumentationsraster.
- **Rechtsstand:** Die Skill führt keine eigene Fundstellensammlung; geprüft wird an
  den in der Prompt-Datei genannten Fundstellen. In der Ausgabe steht gleichwohl zu
  jeder rechtlichen Aussage die Rechtsgrundlage mit Absatz und Satz oder das
  BMF-Schreiben mit Datum und Randziffer, jeweils mit dem Zusatz
  `für [JAHR] verifizieren`; ist eine Fundstelle unsicher, steht dort „Fundstelle
  offen – bitte recherchieren".

## Grundlage

Prüfschema, Normenrahmen und Ausgabeformat stehen in der Prompt-Datei
[prompts/02-umsatzsteuer/85-erechnung-umstellungsradar.md](../../../prompts/02-umsatzsteuer/85-erechnung-umstellungsradar.md);
die Skill folgt ihr und schreibt sie nicht ab.
