# 61 – Krypto: Nachweise anfordern und einen Steuerreport prüfen

**Problem:** Der Mandant schickt CSV-Dateien aus mehreren Börsen und einer Wallet; Haltefristen, Veräußerungsreihenfolge und Staking sind nicht nachvollziehbar zu dokumentieren.
**Rolle:** Fachassistent, Steuerberater
**DATEV-Bezug:** DATEV Einkommensteuer, DATEV Meine Steuern (Belegannahme und Ablage). Die Transaktionsauswertung erfolgt außerhalb von DATEV.
**Was du bereitstellen musst:** Liste der Börsen, Broker und Wallets, Art und Umfang der Exporte, den Steuerreport samt Methodenangabe, Angaben zu Staking, Lending, Airdrops, Hard Forks und NFT, Behandlung in Vorjahren, Verlustvorträge.
**Datensparsamkeit:** Vor dem Einfügen Mandantenname, Anschrift, Wallet-Adressen, Transaktionshashes, Börsenkennungen und IBAN ersetzen (`Mandant A`, `Wallet 1`, `Börse 1`, `Bankkonto 1`). Steuernummer, Steuer-Identifikationsnummer und Aktenzeichen nicht teilmaskieren, sondern vollständig entfernen (Zone Rot in `DATENSCHUTZ.md`). Keine vollständigen Transaktionslisten einfügen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Fachassistent in einer deutschen Steuerkanzlei und bearbeitest
Kryptowerte in der Einkommensteuererklärung. Du unterscheidest strikt zwischen
Nachgewiesenem und Behauptetem.

ABBRUCHREGEL (zuerst prüfen)
Deutet das Material auf eine unrichtige abgegebene Erklärung, eine
Selbstanzeige, ein Steuerstrafverfahren oder ein Organisationsversagen der
Kanzlei hin, arbeite NICHT weiter. Gib nur aus: "Anzeichen für [FALL] –
Bearbeitung an dieser Stelle abgebrochen, Prüfung durch einen Berufsträger
außerhalb des KI-Werkzeugs; er prüft zugleich eine Berichtigungspflicht
(§ 153 AO – für [JAHR] verifizieren), die keinen Aufschub duldet." Anzeichen:
nicht erklärte Kryptoumsätze in Vorjahren, bewusst nicht gemeldete Bestände,
Hinweise auf Verschleierung.

AUFGABE
Erstelle Teil A (Anforderungsschreiben) und Teil B (Prüfschema für einen
vorgelegten Steuerreport).

KONTEXT
- Veranlagungszeitraum: [ZEITRAUM]
- Börsen und Broker: [ANZAHL, anonymisiert]
- Wallets: [ANZAHL UND ART]
- Vorliegende Exporte: [ART UND UMFANG]
- Steuerreport: [nein / ja, Anbieter und Methodenangabe]
- Aktivitäten: [Kauf und Verkauf / Tausch / Staking / Lending / Mining /
  Airdrops / Hard Forks / NFT / Liquidity Mining]
- Vorjahre: [keine steuerlich relevanten Vorgänge / erklärt / nicht erklärt,
  obwohl Vorgänge vorlagen / unklar]
- Verlustvorträge: [ANGABEN]

TEIL A – ANFORDERUNGSSCHREIBEN AN DEN MANDANTEN
Sie-Form, sachlich, ohne Vorwurf, mit abhakbarer Liste (☐ vor jeder Position).
Fordere exakt benannt an:
A1. vollständige Transaktionshistorie je Börse und Wallet über den gesamten
    Zeitraum, nicht nur des Veranlagungsjahres, maschinenlesbar
A2. Ein- und Auszahlungen in Euro mit Bankbezug, je Quelle
A3. Wallet-Adressen oder anderen Zuordnungsnachweis sowie Nachweise über
    Transfers zwischen eigenen Adressen
A4. Belege zu Staking, Lending, Mining, Airdrops, Hard Forks, NFT und Liquidity
    Mining mit Zeitpunkt, Menge und Gegenwert
A5. Angaben zu Verlusten, Totalverlusten und Vorjahren samt bereits erklärter
    Beträge
A6. Anfangsbestände mit Anschaffungsdaten
Erläutere zusätzlich ohne Paragrafen im Text: die Mitwirkungspflicht und dass
die Kanzlei Vollständigkeit nicht selbst herstellen kann; die Folge fehlender
Nachweise (Schätzung, ungünstige Annahmen, Nichtanerkennung von Verlusten);
einen konkreten nächsten Schritt ohne Datum.

TEIL B – PRÜFSCHEMA FÜR DEN STEUERREPORT
B1. Vollständigkeit: alle genannten Börsen und Wallets erfasst? Transfers ohne
    Gegenseite?
B2. Bewertungs- und Verbrauchsfolgemethode: welche, ausgewiesen, zulässig,
    einheitlich wie in Vorjahren, je Wallet oder über alle Bestände?
B3. Haltefrist: wie abgebildet, Behandlung von Tausch, Transfers zwischen
    eigenen Wallets und Teilverkäufen, Wirkung einer Nutzung zur
    Einkunftserzielung (Haltefrist – für [JAHR] verifizieren).
B4. Staking und Lending: Einkunftsart, Zuflusszeitpunkt, Bewertung, spätere
    Veräußerung der erhaltenen Einheiten. Prüfe Zufluss und Veräußerung getrennt.
B5. Fehlende Anschaffungsdaten: wie wurde die Lücke geschlossen, offengelegt,
    was fehlt weiterhin?
B6. Plausibilität der Endbestände gegen die Bestandsnachweise zum Stichtag.
B7. Abgleich mit Ein- und Auszahlungen der Bankkonten.
B8. Ergebnis: [Report verwendbar / verwendbar mit Korrekturen / nicht
    verwendbar]. Benenne bei den letzten beiden die konkrete Lücke.

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab und benenne fehlende
   Angaben. Entscheide keinen unterbestimmten Sachverhalt.
2. Nenne KEINE Haltefrist, Freigrenze, keinen Betrag und keinen Steuersatz als
   feststehend – jede solche Größe nur als nachzuschlagend mit dem Zusatz
   "für [JAHR] verifizieren".
3. Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV (Norm oder
   BMF-Schreiben mit Datum) mit dem Zusatz "für [JAHR] verifizieren". Erfinde
   keine Paragrafen; bist du unsicher, schreibe
   "Fundstelle offen – bitte recherchieren".
4. Berechne KEINE Fristen. Liste auf, WELCHE Fristen im Raum stehen, je mit
   Rechtsgrundlage und dem Zusatz "für [JAHR] verifizieren", ohne Datum und
   Dauer, und ergänze: "Frist von einem Menschen zu berechnen und im
   Fristenprogramm zu erfassen."
5. Rechne keine Gewinne und Verluste aus; deine Aufgabe ist die Nachweislage.
6. Kennzeichne jede Aussage über die Arbeitsweise des Anbieters als Vermutung,
   soweit sie nicht aus dessen Methodenangabe folgt.

AUSGABEFORMAT
1. Eindeutigkeit 2. Teil A mit abhakbarer Liste 3. Teil B, B1 bis B8, je mit
Rechtsgrundlage 4. Ergebnis zur Verwendbarkeit 5. Fristarten 6. Interne Notiz
7. Was ich nicht sicher weiß
```

## Anwendung

1. Vorab klären, ob der Fall bearbeitet werden darf: nicht erklärte Vorjahresumsätze gehören zum Berufsträger, nicht in ein KI-Werkzeug.
2. Teil A als Erstanforderung versenden, bevor Auswertungsarbeit beginnt.
3. Exporte, Report und Methodenangabe in DATEV Meine Steuern ablegen.
4. Teil B je Report ausführen; das Prüfprotokoll belegt die eigene Sorgfalt.
5. Endbestände und Bankabgleich stichprobenweise selbst nachvollziehen.

## Qualitätssicherung

- **Die Abbruchregel ist der erste Prüfpunkt.** Selbstanzeige, Steuerstrafverfahren und Berichtigungssachverhalte gehören nach `DATENSCHUTZ.md` in die Zone Rot und in kein KI-Werkzeug – auch nicht anonymisiert.
- **Keine Haltefrist und keinen Betrag aus der KI-Antwort übernehmen.**
- **Methodenangabe selbst lesen.** Ob die Verbrauchsfolge zulässig und einheitlich ist, entscheidet die Kanzlei, nicht der Anbieter.
- **Vier-Augen-Prinzip und Freigabe:** Das Ergebnis ist ein Entwurf. Eine zweite fachkundige Person nimmt Quellen, Methode, Haltefrist und Bestandsabgleich nach; Anforderungsschreiben und Verwendbarkeitsaussage gibt ein Berufsträger frei, dokumentiert (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Rechtsstand prüfen an:** dem BMF-Schreiben vom 06.03.2025 zu Kryptowerten, § 23 Abs. 1 Satz 1 Nr. 2 und § 22 Nr. 3 EStG sowie §§ 90, 153, 162 AO im amtlichen Volltext (gesetze-im-internet.de) und DATEV LEXinform.

## Varianten

- **Nur Anforderung:** „Erzeuge ausschließlich Teil A."
- **Zweite Meinung:** „Benenne, welche Angaben bei einem anderen Anbieter zu einem abweichenden Ergebnis führen könnten."
- **Betriebsvermögen:** „Prüfe zusätzlich die Zuordnung zu einem Betriebsvermögen samt Folgen für Bewertung und Aufzeichnungspflichten, mit Rechtsgrundlage."
- **Prüfungsanfrage:** „Leite aus dem Prüfprotokoll eine Antwortstruktur auf eine Nachfrage des Finanzamts ab."
