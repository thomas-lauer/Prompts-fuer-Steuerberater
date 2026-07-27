# 09 – Unterlagen-Checkliste Einkommensteuer je Mandantentyp

**Problem:** Mandanten laden in DATEV Meine Steuern nur einen Teil hoch; der Rest fehlt still, und die Erklärung bleibt liegen. Generische Checklisten werden ignoriert, weil 80 % darauf nicht zutreffen.
**Rolle:** Steuerberater, Steuerfachangestellte, Sekretariat
**DATEV-Bezug:** DATEV Meine Steuern, Einkommensteuer, DATEV Upload mobil
**Was du bereitstellen musst:** Lebenssachverhalt des Mandanten, Veranlagungsjahr, was aus dem Vorjahr bekannt ist.
**Datensparsamkeit:** Dieser Prompt sammelt die sensibelsten Angaben aller Prompts (Familie, Immobilien, Auslandsbezug). Namen, Geburtsdaten, Anschriften, Steuernummern, Konto- und Objektbezeichnungen durch Platzhalter ersetzen (`Mandant A`, `Kind 1, 14 Jahre`, `Objekt 1`). Für die Checkliste genügen Sachverhaltstypen, keine Identitäten. Vor dem Einsatz die berufsrechtliche Freigabe der Kanzlei beachten (§ 57 StBerG, § 203 StGB, DSGVO). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Steuerfachwirt in einer deutschen Steuerkanzlei und erstellst
Unterlagenanforderungen, die Mandanten tatsächlich abarbeiten.

AUFGABE
Erstelle eine auf diesen Mandanten zugeschnittene Unterlagen-Checkliste für
die Einkommensteuererklärung [VERANLAGUNGSJAHR].

MANDANTENPROFIL
- Veranlagung: [Einzel / Zusammenveranlagung]
- Einkunftsarten: [z. B. nichtselbständige Arbeit, Vermietung 2 Objekte,
  Kapitalvermögen, Gewerbebetrieb, selbständige Arbeit, Renten]
- Beruflicher Rahmen: [z. B. angestellt mit Homeoffice, doppelte
  Haushaltsführung, Auswärtstätigkeit, Fortbildung]
- Familie: [Kinder mit Alter und Ausbildungsstand, Unterhaltsleistungen]
- Immobilien: [selbstgenutzt / vermietet, Erwerb oder Verkauf im Jahr]
- Kapitalanlagen: [inländisch / ausländisch / Krypto / Beteiligungen]
- Auslandsbezug: [ja/nein, welcher]
- Bekannte Veränderungen gegenüber dem Vorjahr:
  [z. B. Umzug, Heirat, Jobwechsel, Kind geboren, Immobilienkauf, Erbfall]
- Was aus dem Vorjahr bereits vorliegt oder von Amts wegen übermittelt wird:
  [z. B. Lohnsteuerbescheinigung, Beiträge KV/PV, Renten – vorausgefüllte
  Steuererklärung]

ANFORDERUNGEN
1. Gliedere nach Lebensbereichen, nicht nach Anlagen des Formulars.
   Beispiele: "Einnahmen", "Wohnen", "Kinder", "Vorsorge", "Vermietung",
   "Kapitalanlagen", "Sonstiges".
2. Nimm NUR Positionen auf, die zu diesem Profil passen. Lasse alles weg,
   was nicht zutrifft. Eine kurze zutreffende Liste ist besser als eine
   vollständige unzutreffende.
3. Markiere jede Position mit:
   (Pflicht) – ohne das geht die Erklärung nicht
   (wenn vorhanden) – nur falls einschlägig
   (liegt uns vor) – vom Mandanten nicht beizubringen
4. Formuliere jede Position so, dass ein Laie das Dokument erkennt:
   nicht "Nachweis über Vorsorgeaufwendungen", sondern
   "Bescheinigung Ihrer Krankenkasse über die gezahlten Beiträge
   (kommt meist im Februar per Post)".
5. Ergänze je Position – wo hilfreich – einen Hinweis, WO der Mandant
   das Dokument üblicherweise findet.
6. Nimm eine Rubrik "Neu in diesem Jahr" auf, die auf die genannten
   Veränderungen eingeht und die dadurch zusätzlich nötigen Unterlagen nennt.
7. Nimm eine Rubrik "Fragen, die wir nicht aus Unterlagen beantworten können"
   auf – maximal 6 geschlossene Fragen.
8. Schreibe ein Anschreiben von maximal 120 Wörtern mit Frist [DATUM] und
   dem Hinweis auf den Übermittlungsweg [DATEV Meine Steuern / Upload mobil].
9. Erzeuge die Liste so, dass sie ausgedruckt abhakbar ist
   (Kästchen ☐ vor jeder Position).
10. Die Checkliste fordert Unterlagen an, sie berät nicht. Machst du dennoch
    eine rechtliche Aussage – etwa zu einer Nachweispflicht oder einer
    Aufbewahrungsfrist –, nenne die Rechtsgrundlage (Norm mit Absatz und Satz,
    Richtlinie oder BMF-Schreiben mit Datum), jeweils mit dem Zusatz
    "für [JAHR] verifizieren", und stelle sie in die interne Notiz statt in
    den Mandantentext. Erfinde keine Paragrafen; bist du unsicher, schreibe
    "Fundstelle offen – bitte recherchieren".

AUSGABEFORMAT
1. Anschreiben  2. Checkliste nach Lebensbereichen  3. Neu in diesem Jahr
4. Fragen an Sie  5. Interne Notiz für die Kanzlei (was wir selbst beschaffen)
```

## Anwendung

1. Profil aus der Vorjahresakte übernehmen – das ist der Arbeitsschritt, der die Qualität ausmacht.
2. Checkliste als PDF in DATEV Meine Steuern hinterlegen oder per Post versenden.
3. Nach Rücklauf: Zusatzprompt "Vergleiche die eingegangenen Unterlagen mit der Checkliste und erzeuge eine Nachforderung nur über die fehlenden Positionen." (kombinierbar mit Prompt 01)

## Qualitätssicherung

- Liste gegen die tatsächlichen Einkunftsarten der Vorjahresveranlagung prüfen – das Modell kennt den Mandanten nicht.
- Keine Aussagen zur steuerlichen Abzugsfähigkeit in die Checkliste aufnehmen, die nicht geprüft sind; die Liste fordert Unterlagen an, sie berät nicht.
- Prüfen, ob Positionen enthalten sind, die bereits über die vorausgefüllte Steuererklärung vorliegen – doppelte Anforderung wirkt unprofessionell.
- **Vier-Augen-Prinzip und Freigabe:** Die Checkliste ist ein Entwurf. Eine zweite Person muss sie gegen das Mandantenprofil und die Vorjahresveranlagung abgleichen – eine fehlende Pflichtposition fällt erst bei der Bearbeitung auf. Die Freigabe zur Weitergabe an den Mandanten erteilt ein Berufsträger; die Freigabe ist zu dokumentieren.

## Varianten

- **Standardtypen vorbereiten:** Einmal je Mandantentyp erzeugen (Angestellter, Vermieter, Freiberufler, Rentner, Kapitalanleger) und als Kanzleivorlage ablegen; pro Mandat nur noch anpassen.
- **Erstmandat:** Zusatz "Ergänze eine Rubrik 'Unterlagen aus den Vorjahren', die wir für die Erstbearbeitung benötigen."
- **Zweisprachig:** "Erzeuge zusätzlich eine englische Fassung."
