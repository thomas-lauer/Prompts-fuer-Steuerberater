# 08 – Lohnabrechnung für den Arbeitnehmer verständlich erklären

**Problem:** "Warum ist netto weniger als letzten Monat?" – Arbeitnehmer des Mandanten rufen direkt in der Kanzlei an; jede Erklärung wird neu formuliert.
**Rolle:** Lohnsachbearbeitung, Sekretariat
**DATEV-Bezug:** Lohn und Gehalt, LODAS, DATEV Arbeitnehmer online
**Was du bereitstellen musst:** Die relevanten Positionen beider Abrechnungen, die konkrete Frage des Arbeitnehmers.
**Datensparsamkeit:** Name, Personalnummer und Anschrift des Arbeitnehmers durch `AN 1` ersetzen, den Arbeitgeber durch `Mandant A`. Bei Pfändungen keine Gläubigerdaten und keine Angaben zum Grund der Forderung einfügen.

## Prompt

```text
Du erklärst einem Arbeitnehmer ohne steuerliche Vorkenntnisse seine
Lohnabrechnung. Dein Stil: freundlich, sachlich, in Alltagssprache.
Du erklärst, ohne zu belehren, und du beruhigst nicht durch Verharmlosung,
sondern durch Nachvollziehbarkeit.

AUFGABE
Erkläre die folgende Veränderung in der Lohnabrechnung.

FRAGE DES ARBEITNEHMERS
[WÖRTLICHE FRAGE, z. B. "Warum habe ich diesen Monat 120 € weniger netto?"]

ZAHLEN (anonymisiert)
- Abrechnungsmonat: [MONAT] / Vergleichsmonat: [MONAT]
- Bruttolohn: [WERT] / [WERT]
- Einmalzahlungen, Zuschläge, Sachbezüge: [WERTE mit Bezeichnung]
- Lohnsteuer / Soli / Kirchensteuer: [WERTE] / [WERTE]
- SV-Beiträge (KV/PV/RV/AV): [WERTE] / [WERTE]
- Nettoentgelt: [WERT] / [WERT]
- Bruttoabzüge (z. B. Entgeltumwandlung bAV): [WERTE]
- Bezüge nach Netto (z. B. steuerfreier oder pauschalversteuerter
  Fahrtkostenzuschuss, Auslagenersatz): [WERTE]
- Abzüge nach Netto (z. B. Pfändung, Arbeitgeberdarlehen, AN-Anteil
  vermögenswirksame Leistungen, Kantinen-/Sachbezugsabzug): [WERTE]
- Bekannte Änderungen: [z. B. Steuerklassenwechsel, Kind eingetragen,
  Zusatzbeitrag der Krankenkasse geändert, Einmalzahlung, Elternzeit,
  Firmenwagen neu, Beitragsbemessungsgrenze erreicht]

ANFORDERUNGEN
1. Beginne mit EINEM Satz, der die Hauptursache benennt.
2. Rechne die Veränderung schrittweise vor: welcher Betrag hat sich um
   wie viel verändert und wie wirkt sich das auf das Netto aus.
   Nutze eine kleine Tabelle mit den Spalten:
   Position | Vormonat | aktueller Monat | Veränderung.
   Nimm nur Positionen auf, die sich tatsächlich verändert haben.
3. Erkläre jeden Fachbegriff, den du verwendest, in einem Halbsatz in Klammern.
4. Unterscheide ausdrücklich drei Fälle und ordne die Ursache einem zu:
   (a) gleicht sich im Kalenderjahr aus (z. B. Steuerklassenwechsel,
       Lohnsteuer-Jahresausgleich durch den Arbeitgeber, § 42b EStG),
   (b) gleicht sich erst über die Einkommensteuerveranlagung aus
       (z. B. Mehrsteuer auf eine Einmalzahlung),
   (c) gleicht sich nicht aus, sondern kehrt sich zum Jahreswechsel um
       (z. B. Erreichen der Beitragsbemessungsgrenze im Jahresverlauf).
   Behaupte nie einen Ausgleich, den du nicht einem dieser Fälle zuordnen
   kannst.
5. Wenn aus den Zahlen KEINE eindeutige Ursache hervorgeht: sag das offen,
   nenne die zwei wahrscheinlichsten Ursachen und welche Angabe fehlt.
   Erfinde keine Erklärung.
6. Schließe mit einem Satz, an wen sich der Arbeitnehmer wenden soll und
   wofür – vorrangig an den Arbeitgeber; Krankenkasse oder Finanzamt nur
   bei deren Zuständigkeit; an die Kanzlei nur, wenn dazu eine
   ausdrückliche Vereinbarung mit dem Arbeitgeber besteht.
7. Länge: maximal 250 Wörter. Sie-Form. Keine Paragrafen.

AUSGABEFORMAT
Antwortmail mit Betreff, Text, Tabelle, Schlusssatz.
Darunter separat: "Interne Notiz" – was die Kanzlei ggf. noch prüfen sollte.
```

## Anwendung

1. Nur die veränderten Positionen beider Monate eingeben, Name und Personalnummer weglassen.
2. Antwort prüfen, dann an den Arbeitnehmer oder – je nach Vereinbarung – an den Arbeitgeber zur Weitergabe senden.
3. Wiederkehrende Fälle (Einmalzahlung im November, Beitragsbemessungsgrenze, Steuerklassenwechsel) als feste Textbausteine ablegen.

## Qualitätssicherung

- **Die Rechnung selbst nachvollziehen.** Wenn die vorgerechnete Veränderung nicht exakt aufgeht, den Text nicht versenden.
- Prüfen, ob die Kanzlei gegenüber dem Arbeitnehmer überhaupt auskunftsbefugt ist – Mandant ist der Arbeitgeber. Im Zweifel über den Arbeitgeber kommunizieren.
- Keine Aussagen zur persönlichen Steuersituation des Arbeitnehmers (Erstattung, Veranlagung) ohne Mandat.
- Bei Pfändungen und Abtretungen: Text vor Versand gesondert freigeben, hier sind Datenschutz und Persönlichkeitsrechte berührt.

## Varianten

- **FAQ statt Einzelfall:** "Erzeuge aus den zehn häufigsten Fragen eine FAQ-Seite für die Mitarbeiter unseres Mandanten."
- **Erstabrechnung:** "Erkläre einem neu eingestellten Arbeitnehmer seine erste Abrechnung Position für Position."
- **Jahreswechsel:** "Erkläre, warum sich das Netto zum Januar verändert hat, ohne dass sich das Brutto geändert hat."
