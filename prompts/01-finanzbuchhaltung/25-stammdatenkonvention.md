# 25 – Namens- und Stammdatenkonvention für Personenkonten festlegen

**Problem:** Debitoren und Kreditoren werden doppelt und uneinheitlich angelegt; Auswertungen, OP-Listen und Zahlungsläufe werden dadurch unbrauchbar.
**Rolle:** Stammdatenpflege, Buchhaltung, Teamleitung, Kanzleileitung
**DATEV-Bezug:** Kanzlei-Rechnungswesen (Personenkonten, Nummernkreise im Kontenrahmen SKR03/SKR04), DATEV Unternehmen online (Belegerkennung und Kontovorschlag), Auswertungen und Zahlungsverkehr
**Was du bereitstellen musst:** Kontenrahmen, genutzte Nummernkreise, Zahl und Art der Mandate, bekannte Problemfälle aus dem Bestand, eingesetzte Belegerkennung.
**Datensparsamkeit:** Für die Erarbeitung der Regeln genügen anonymisierte Beispielnamen (`Muster Handels GmbH`, `Kreditor 1`). Keine echten Namen, keine IBAN, keine USt-IdNr., keine Steuernummern einfügen. Ergänzt Prompt 19: Dieser Prompt verhindert Dubletten bei der Anlage, Prompt 19 findet die bereits entstandenen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist verantwortlich für Datenqualität und Stammdaten in einer deutschen
Steuerkanzlei. Du schreibst Regeln ohne Auslegungsspielraum: für jeden Fall
genau eine zulässige Schreibweise, entscheidbar in unter zehn Sekunden.

AUFGABE
Erstelle ein Regelwerk für die Anlage und Pflege von Personenkonten
(Debitoren und Kreditoren).

RAHMEN
- Kontenrahmen: [SKR03 / SKR04]
- Genutzte Nummernkreise heute: [z. B. Debitoren 10000–69999,
  Kreditoren 70000–99999]
- Anzahl Mandate / Kanzleigröße: [ANGABE]
- Wer legt Personenkonten an: [ROLLEN]
- Belegerkennung im Einsatz: [ja, welche / nein]
- Bekannte Problemfälle im Bestand: [z. B. "GmbH" mal ausgeschrieben, mal
  abgekürzt; Umlaute mal als ae, mal als ä; Privatpersonen mal Nachname
  zuerst, mal Vorname zuerst]
- Vorhandene Regeln, die gelten sollen: [ANGABE oder "keine"]

REGELUNGSBEDARF – behandle jeden Punkt einzeln
1. Firmenname: Grundform, Reihenfolge der Bestandteile.
2. Rechtsformzusatz: ausgeschrieben oder abgekürzt, mit oder ohne Komma,
   Position, Umgang mit "& Co. KG", "e. K.", ausländischen Formen.
3. Umlaute und ß: beibehalten oder umschreiben – EINE Regel, keine Wahl.
4. Sonderzeichen: kaufmännisches Und, Bindestrich, Punkt, Apostroph,
   Anführungszeichen, Klammern.
5. Abkürzungen im Firmennamen, Groß-/Kleinschreibung reiner Versalnamen.
6. Artikel am Namensanfang.
7. Privatpersonen: Reihenfolge Nachname/Vorname, Titel, Namenszusätze,
   Ehepaare, gleichnamige Personen.
8. Nummernkreise: Systematik, Vergabeverfahren, was NICHT in die Nummer
   hineincodiert werden darf.
9. Pflichtfelder bei Anlage und optionale Felder.
10. Suchbegriff / Kurzbezeichnung: Ableitungsregel aus dem Namen.
11. Namensänderung, Rechtsformwechsel, Verschmelzung, Insolvenz: Konto umbenennen
    oder neu anlegen – mit Kriterium, wann was gilt, und mit der Vorgabe, dass
    die Bedeutung des Kontos für zurückliegende Buchungen erhalten bleiben muss
    (Historisierung mit Gültigkeitsangabe statt stiller Umbenennung; Nummern
    werden nicht wiederverwendet). Kennzeichne die zugrunde liegende Anforderung
    als "Fundstelle – für [JAHR] verifizieren".
12. Dublettenvermeidung: welche Suchen VOR der Anlage zwingend sind und in
    welcher Reihenfolge.

ANFORDERUNGEN
1. Formuliere jede Regel im Imperativ, ohne "sollte" und "in der Regel".
   Wo zwei Lösungen vertretbar sind, entscheide dich für eine, begründe sie
   in einem Halbsatz und markiere sie als
   (Kanzleientscheidung – bitte bestätigen).
2. Gib zu jeder Regel mindestens ein Beispielpaar richtig/falsch mit
   erfundenen Namen. Keine echten Firmen.
3. Personenkonten werden sortiert ausgewertet und in Zahlungsläufen
   maschinell abgeglichen: Nenne zu jeder Regel in einem Halbsatz, welchen
   Folgefehler sie verhindert.
4. Nenne keine DATEV-Feldlängen, Nummernkreisgrenzen oder Programmvorgaben
   als feststehend, ohne sie als "Vorgabe im eingesetzten Programmstand –
   für [JAHR] verifizieren" zu kennzeichnen. Erfinde keine Menüpfade.
5. Nenne keine handels- oder steuerrechtlichen Vorgaben zur Firmierung als
   feststehend, ohne "Fundstelle – für [JAHR] verifizieren" zu ergänzen.
6. Höchstens 25 Regeln. Streiche, was in der Praxis nie strittig ist.
7. Was der Rahmen nicht hergibt, markierst du als (offen) und nimmst es in
   die Klärungsliste auf.

AUSGABEFORMAT
1. Regelwerk (nummeriert, gegliedert nach den zwölf Punkten oben)
2. Beispieltabelle: Fall | richtig | falsch | verhinderter Folgefehler
3. Prüfliste Neuanlage (abhakbar, Kästchen ☐, in der Reihenfolge des
   tatsächlichen Anlagevorgangs, Dublettensuche VOR der Vergabe der Nummer)
4. Was zu entscheiden ist (Kanzleientscheidungen und offene Punkte)
5. Interne Notiz: Auswirkungen auf den Altbestand
```

## Anwendung

1. Rahmen ausfüllen und die Problemfälle des eigenen Bestands ehrlich benennen – daran entscheidet sich, ob die Regeln die echten Streitfälle treffen.
2. Ergebnis im Team durchgehen und die markierten Kanzleientscheidungen beschließen. Regeln, die niemand beschlossen hat, werden nicht befolgt.
3. Prüfliste Neuanlage an den Arbeitsplatz, nicht ins Intranet.
4. Altbestand nicht sofort umstellen: erst die Neuanlage regeln, dann mit Prompt 19 die Dubletten aufarbeiten.
5. Regelwerk mit Version und Datum versehen und in die Einarbeitung aufnehmen.

## Qualitätssicherung

- **Das Regelwerk ist ein Entwurf.** Vor Inkraftsetzung von einer zweiten Person gegenlesen lassen (Vier-Augen-Prinzip); die Freigabe erteilt die Kanzleileitung, bei Auswirkungen auf Firmierung, Zahlungsträger und Mandantenkorrespondenz ein Berufsträger (Freigabestufe 3 in `DATENSCHUTZ.md`).
- Nummernkreise gegen den eingesetzten Kontenrahmen und die Stammdaten prüfen; eine Konvention, die vergebene Bereiche überschreibt, schadet mehr als die Uneinheitlichkeit.
- Feldlängen und zulässige Zeichen im Programm nachsehen, bevor eine Schreibweise verbindlich wird.
- Prüfen, ob die Belegerkennung mit der gewählten Schreibweise noch zuordnet – wer Umlaute umschreibt, verschlechtert womöglich die automatische Kontozuordnung.
- Auswirkungen auf Zahlungsträger und Mahnwesen prüfen: Der Name im Personenkonto wandert nach außen.
- Vor Inkraftsetzung an zwanzig Bestandskonten testen: Jeder Zweifelsfall zeigt eine fehlende Regel.

## Varianten

- **Sachkonten:** "Erweitere das Regelwerk um Bezeichnungen individueller Sachkonten und um die Frage, wann ein eigenes Konto statt eines Buchungstextes angelegt wird."
- **Bestandsbereinigung:** "Erzeuge aus dem Regelwerk eine Prüfregel-Liste, mit der ein Stammdatenexport auf Regelverstöße durchsucht wird."
- **Kurzfassung:** "Erzeuge eine Fassung mit höchstens zehn Regeln für Auszubildende."
