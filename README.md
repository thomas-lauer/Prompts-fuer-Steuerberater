# Prompts für Steuerberater

Praxistaugliche KI-Prompts für Steuerkanzleien, die mit DATEV arbeiten.
Zum Kopieren, Ausfüllen, Einsetzen.

---

## Für wen

Für alle, die in einer deutschen Steuerkanzlei arbeiten:

- **Buchhaltung und Steuerfachangestellte** – Kontierung, Belegklärung, Rückfragen an Mandanten
- **Lohnsachbearbeitung** – Sonderfälle einordnen, Abrechnungen erklären, Zulieferungen einfordern
- **Steuerberaterinnen und Steuerberater** – Auswertungen kommentieren, Sachverhalte prüfen, Mandanten verständlich informieren
- **Sekretariat und Kanzleiorganisation** – Fristen, Nachforderungen, wiederkehrende Korrespondenz
- **Kanzleileitung** – Arbeitsanweisungen, Einarbeitung, Prozessdokumentation

Vorkenntnisse in KI-Werkzeugen sind nicht nötig. Wer einen Text in ein
Chatfenster einfügen kann, kann diese Prompts benutzen.

## Wofür

Jeder Prompt löst ein Problem, das im Kanzleialltag regelmäßig wiederkehrt und
jedes Mal von Hand erledigt wird. Die Themen sind nicht erfunden, sondern aus
Foren, Fachdiensten und Kanzleiblogs recherchiert – unter anderem aus der
DATEV-Community.

Abgedeckt sind derzeit:

| Bereich | Was die Prompts leisten |
|---------|-------------------------|
| **Belege und Mandantenzulieferung** | Fehlende Unterlagen in Eskalationsstufen nachfordern; unklare Bankumsätze gebündelt statt einzeln klären |
| **Buchführung** | Buchungssätze in SKR03/SKR04 begründen; Umsatzsteuer-Sonderfälle nach Prüfschema einordnen; UStVA-Abweichungen eingrenzen |
| **Lohn** | Sonderfälle lohnsteuerlich und sozialversicherungsrechtlich prüfen; Abrechnungen für Arbeitnehmer verständlich erklären |
| **Steuererklärung** | Unterlagen-Checklisten, die zum jeweiligen Mandanten passen statt zum Formular |
| **Reisekosten und Bewirtung** | Abrechnungen und Belege systematisch prüfen, Korrekturbedarf benennen |
| **Auswertung und Kommunikation** | BWA so kommentieren, dass der Mandant sie versteht |

## Wofür nicht

Diese Prompts sind **kein Ersatz für steuerliche Beratung** und **keine
verbindliche Auskunft**. Sie erzeugen Entwürfe, Prüfschemata und Textvorlagen.
Die fachliche Verantwortung bleibt vollständig bei der Kanzlei.

Sie können außerdem nicht:

- auf DATEV-Daten zugreifen oder in DATEV buchen
- technische Probleme lösen (Installation, Updates, Bankabruf, Lizenzen)
- Rechtsstände garantieren – Pauschbeträge, Freigrenzen und Beitragsbemessungsgrenzen ändern sich jährlich

## So benutzt du sie

1. Passenden Prompt in `prompts/` öffnen.
2. Den Block unter **## Prompt** vollständig kopieren.
3. Alle Platzhalter in eckigen Klammern ersetzen – `[MANDANT]`, `[ZEITRAUM]`, `[BETRAG]`.
4. In dein KI-Werkzeug einfügen und ausführen.
5. Den Abschnitt **## Qualitätssicherung** durchgehen, bevor das Ergebnis die Kanzlei verlässt.

Jede Datei hat denselben Aufbau: Problem, Rolle, DATEV-Bezug, benötigte Daten,
Datensparsamkeitshinweis, der eigentliche Prompt, Anwendung, Qualitätssicherung,
Varianten.

## Datenschutz und Berufsrecht

**Vor dem Einfügen anonymisieren.** Mandantenname, Anschrift, Steuernummer,
Personalnummern, IBAN und Namen Dritter durch Platzhalter ersetzen
(`Mandant A`, `AN 1`, `Konto ****1234`). Für die fachliche Arbeit genügen
Sachverhalt, Beträge, Konten und Daten.

Der Einsatz von KI-Werkzeugen mit Mandantenbezug berührt die berufsrechtliche
Verschwiegenheitspflicht (§ 57 StBerG, § 203 StGB) und die DSGVO. Ob und mit
welchen Daten ein bestimmtes Werkzeug befüllt werden darf, muss die Kanzlei
entscheiden und dokumentieren. Jeder Prompt enthält dazu einen eigenen Hinweis.

## Zwei Grundregeln, die den Unterschied machen

**Zahlen prüfen, Struktur nutzen.** Die Stärke dieser Prompts liegt in der
Vollständigkeit der Prüfschritte, nicht in den Zahlen. Sprachmodelle geben
Kontonummern, Pauschbeträge und Freigrenzen plausibel, aber häufig falsch an.
Deshalb fordert jeder Prompt das Modell auf, solche Werte als
"für [JAHR] verifizieren" zu markieren – dieser Markierung folgen, immer.

**Vier Augen.** Kein Ergebnis geht ungeprüft an einen Mandanten oder in eine
Buchung. Der Abschnitt Qualitätssicherung sagt in jeder Datei konkret, worauf
zu achten ist.

## Beitragen

Fehler gefunden, Formulierung verbessert, neuen Anwendungsfall? Issue oder
Pull Request. Besonders wertvoll sind Rückmeldungen aus dem echten
Kanzleieinsatz: Was hat funktioniert, was musste umgeschrieben werden.

## Lizenz

Nutzung, Anpassung und Weitergabe innerhalb und außerhalb von Kanzleien
ausdrücklich erwünscht. Ohne Gewähr, ohne Haftung.

---

## Änderungsprotokoll

Änderungen werden hier chronologisch festgehalten, neueste zuerst.

### 2026-07-27 – Veröffentlichung auf GitHub

- Projekt auf zwei Repositorys aufgeteilt: ein privates Entwicklungs-Repository
  mit Charter, Backlog, Recherche und Projektdokumentation, und dieses
  öffentliche Repository mit den Prompts und dieser Beschreibung.
- `README.md` neu geschrieben: von einer internen Konventionsdatei zu einer
  Beschreibung für Anwender – für wen, wofür, wofür ausdrücklich nicht,
  Anwendung, Datenschutz und Berufsrecht.
- Die bisherigen Konventionen für Prompt-Dateien sind in die Projekt-
  dokumentation des privaten Repositorys gewandert.

### 2026-07-27 – Lauf 1: Erstveröffentlichung

- Recherchebasis aufgebaut: 60+ Alltagsprobleme aus DATEV-Community, Circula-Blog,
  IWW, DATEV-Magazin, DStV, Haufe und Kanzleiblogs; gefiltert auf die Fälle, bei
  denen KI ohne DATEV-Systemzugriff tatsächlich hilft.
- Die ersten zehn Prompts erstellt (01–10): Belegnachforderung, Bankumsatz-Rückfragen,
  Buchungssatz SKR03/04, Umsatzsteuer-Sonderfälle, UStVA-Abweichung, BWA-Kommentar,
  Lohn-Sonderfälle, Lohnabrechnung erklären, ESt-Unterlagencheckliste,
  Reisekosten- und Bewirtungsprüfung.
- Zwei Prüfdurchgänge: Strukturprüfung bestanden; adversarische Fachprüfung
  fand 24 Mängel, alle behoben. Unter anderem: zirkuläres Umsatzsteuer-Prüfschema
  neu geordnet, falscher Rechnungsadressat beim Bewirtungsbeleg korrigiert,
  Fahrtkostenzuschuss und bAV in der Lohnabrechnung richtig einsortiert,
  abgekündigtes DATEV-Produkt ersetzt, Datensparsamkeitshinweis in allen Dateien ergänzt.
- Backlog mit 52 Punkten angelegt.
