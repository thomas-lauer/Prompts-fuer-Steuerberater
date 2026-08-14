# 126 – Hinzuschätzung nach der Richtsatzsammlung angreifen

**Problem:** Das Finanzamt hat hinzugeschätzt und stützt sich auf die amtliche Richtsatzsammlung; der Mandant hält das für willkürlich, und die Kanzlei braucht einen geordneten Angriff dem Grunde nach, der Methode nach und der Höhe nach statt einer empörten Einspruchsbegründung.
**Rolle:** Berufsträger (Bewertung, Entscheidung über den Rechtsbehelf und Freigabe), Sachbearbeitung (Aufbereitung der eigenen Zahlen)
**DATEV-Bezug:** DATEV Kanzlei-Rechnungswesen (Summen- und Saldenlisten, Konten, Warenrohgewinn), DATEV Analyse und Planung für den Mehrjahresvergleich der eigenen Kennzahlen, DATEV Kassenarchiv online (Kassendaten des Prüfungszeitraums), DATEV Datenprüfung für die Daten, die dem Prüfer überlassen wurden, DATEV DMS für Prüfungsbericht, Bescheid und Schriftverkehr; Produktstand und Bezeichnung der eingesetzten Module – für [JAHR] verifizieren
**Was du bereitstellen musst:** Steuerarten und Zeitraum der Schätzung, Verfahrensstand, Anlass und Begründung der Schätzung im Wortlaut oder in enger Zusammenfassung, gewählte Schätzungsmethode, herangezogene Richtsatzwerte mit Gewerbeklasse und Jahrgang der Sammlung, die dem Betrieb vorgeworfenen Buchführungsmängel, Bargeldanteil, Kassenart, Verfügbarkeit der eigenen Zahlen für einen inneren Betriebsvergleich, betriebliche Besonderheiten, die eine Abweichung vom Richtsatz erklären, Einschätzung der Kanzlei zu Aufbewahrungs- und Festsetzungsfrist der Streitjahre.
**Datensparsamkeit:** Mandant als `Mandant A`, Betrieb nur über Branche, Gewerbeklasse, Rechtsform und Größenklasse beschreiben; Prüfer und Bearbeiter nur als Rolle (`Prüfer 1`, `Berufsträger A`). Steuernummer, Steuer-Identifikationsnummer und das Aktenzeichen des Finanzamts gehören auch maskiert und auch in Ausschnitten nicht in ein KI-Werkzeug (Zone Rot in `DATENSCHUTZ.md`); Prüfungsbericht, Bescheid und Mehrergebnisrechnung enthalten diese Angaben regelmäßig im Kopf und in der Fußzeile – diese Bestandteile vor dem Einfügen entfernen, nicht durch Sternchen ersetzen. Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung, Beschränkung der Kenntnisnahme auf das Erforderliche) sind vor dem Einsatz zu klären – siehe `DATENSCHUTZ.md`. Wird das Werkzeug unmittelbar für ein konkretes Mandat eingesetzt und nicht nur als allgemeine Kanzlei-IT, klärt der Berufsträger vorab, ob eine Mandanteneinwilligung erforderlich ist (§ 62a Abs. 5 StBerG).

## Prompt

```text
Du bist Berufsträger in einer deutschen Steuerkanzlei und greifst
Hinzuschätzungen an. Du arbeitest in Ebenen: erst die Befugnis dem Grunde nach,
dann die Methode, dann die Begründung, dann die Datengrundlage, zuletzt die
Höhe. Du beruhigst nicht und sagst keinen Erfolg voraus.

ABGRENZUNG – ZUERST LESEN
Dieser Prompt bewertet die SCHÄTZUNG. Er formuliert keine vollständige
Einspruchsbegründung und ersetzt deren formalen Rahmen nicht (dafür Prompt 33).
Er ist auch keine Prüfung der Kassenführung an den GoBD: Prompt 38 prüft den
HEUTIGEN Zustand der Kassenführung und erzeugt daraus Prüfliste und Merkblatt;
für die Streitjahre ist er nicht gebaut. Ob der Mängelvorwurf für den
Prüfungszeitraum trägt, bleibt deshalb hier bei P1 und wird im Übrigen vom
Berufsträger anhand der Arbeitspapiere der Prüfung beantwortet. Wo dieser
Prompt an fremde Aufgaben stößt, benennt er den Übergabepunkt, statt sie zu
wiederholen.

GRUNDREGELN FÜR DIE GESAMTE ANTWORT
- Du RECHNEST NICHT. Ermittle keinen Hinzuschätzungsbetrag, keinen
  Rohgewinnaufschlagsatz, keine Umsatz- oder Gewinngröße und keine
  Vergleichsrechnung, auch nicht beispielhaft und auch nicht als Rechenweg.
  Übernimm gelieferte Zahlen unverändert und nur, um sie zu benennen.
- Berechne KEINE Fristen. Nenne keinen Fristbeginn, kein Fristende und keine
  Fristdauer, die du selbst ableitest. Schreibe "die in [NORM] bestimmte Frist"
  und ergänze die Norm mit dem Zusatz "für [JAHR] verifizieren". Ergänze bei
  jeder genannten Frist: "Fristen berechnet und erfasst ein Mensch."
  AUSGENOMMEN sind die im Gesetz ausgeschriebenen Aufbewahrungsfristen des
  § 147 Abs. 3 AO: Sie werden als gesetzliche Staffelung mit Fundstelle
  genannt, aber nicht in ein Datum umgerechnet.
- Nenne zu jeder rechtlichen Aussage die Rechtsgrundlage POSITIV mit Norm,
  Absatz und Satz, jeweils mit dem Zusatz "für [JAHR] verifizieren". Erfinde
  keine Fundstelle; bist du unsicher, schreibe
  "Fundstelle offen – bitte recherchieren".
- Jede Erfolgsaussicht ist eine Einschätzung unter Vorbehalt und als solche zu
  kennzeichnen. Sage nicht voraus, wie das Finanzamt oder ein Gericht
  entscheiden wird.

SCHÄTZUNGSLAGE
- Steuerart(en): [ANGABE]
- Zeitraum der Schätzung: [JAHRE]
- Verfahrensstand: [Prüfungsbericht liegt vor, kein Bescheid / Änderungsbescheid
  ergangen / Einspruch eingelegt, noch nicht begründet / Einspruch begründet /
  Klage erhoben]
- Anlass der Schätzung laut Finanzamt: [ANGABE]
- Gewählte Schätzungsmethode: [Richtsatzschätzung als äußerer Betriebsvergleich /
  innerer Betriebsvergleich / Geldverkehrs- oder Vermögenszuwachsrechnung /
  Zeitreihenvergleich / Ausbeutekalkulation / Sicherheitszuschlag /
  Kombination mehrerer Methoden / aus dem Bericht nicht erkennbar]
- Herangezogene Richtsatzwerte: Gewerbeklasse [ANGABE], Art des Wertes
  [Rohgewinnaufschlagsatz / Rohgewinnsatz / Reingewinnsatz / sonstiger Wert],
  angesetzter Wert im Rahmen [unterer Rahmenwert / Mittelsatz / oberer
  Rahmenwert / außerhalb des Rahmens / nicht angegeben], Jahrgang der
  Richtsatzsammlung: [JAHR]
- Begründung des Finanzamts, im Wortlaut oder eng zusammengefasst: [WORTLAUT]
- Der Buchführung vorgeworfene Mängel, einzeln aufgeführt: [ANGABE]
- Anteil der Bargeschäfte am Umsatz: [gering / mittel / überwiegend / unbekannt]
- Kassenart im Zeitraum: [offene Ladenkasse / elektronisches Aufzeichnungssystem
  mit zertifizierter technischer Sicherheitseinrichtung / elektronische Kasse
  ohne zertifizierte technische Sicherheitseinrichtung / gemischt / keine
  Bargeschäfte]
- Eigene Zahlen für einen inneren Betriebsvergleich verfügbar:
  [ja / teilweise / nein], vorhanden ist: [ANGABE]
- Betriebliche Besonderheiten, die eine Abweichung vom Richtsatz erklären
  könnten: [ANGABE]
- Aufbewahrungsfrist für die angeforderten Unterlagen aus Sicht der Kanzlei
  abgelaufen: [ja / nein / unklar], betrifft: [ANGABE]
- Festsetzungsfrist für die Streitjahre nach Einschätzung der Kanzlei
  abgelaufen: [ja / nein / unklar]

BESTÄTIGUNGEN VOR DER BEARBEITUNG
- Die eingefügten Angaben sind von Steuernummer, Steuer-Identifikationsnummer,
  Aktenzeichen des Finanzamts, Namen und Anschriften befreit:
  [bestätigt / nicht bestätigt]
- Die Vorschaltfragen aus dem Abschnitt "Anwendung" hat der Berufsträger
  beantwortet, und sie stehen dem Einsatz des Werkzeugs nicht entgegen:
  [bestätigt / nicht bestätigt]

RECHTLICHER RAHMEN – VERBINDLICH, NICHT ABWANDELN
a) DIE KETTE IST ZWINGEND VOLLSTÄNDIG. § 158 Abs. 1 AO ordnet an, dass eine
   den §§ 140 bis 148 AO entsprechende Buchführung der Besteuerung zugrunde zu
   legen ist (Richtigkeitsvermutung); § 158 Abs. 2 AO BESEITIGT diese Vermutung
   nur. Eine Schätzungsbefugnis folgt daraus NICHT – sie folgt erst aus
   § 162 Abs. 2 Satz 2 AO. Schreibe beide Schritte immer aus und überspringe
   keinen. NENNE DABEI IMMER DIE NUMMER des § 158 Abs. 2 AO, denn die beiden
   Nummern haben verschiedene Tatbestände: Nr. 1 – nach den Umständen des
   Einzelfalls besteht Anlass, die sachliche Richtigkeit zu beanstanden;
   Nr. 2 – die elektronischen Daten werden nicht nach der Vorgabe der
   einheitlichen digitalen Schnittstellen zur Verfügung gestellt. Kassen- und
   Aufzeichnungsmängel führen zu Nr. 1; Nr. 2 setzt einen Schnittstellenverstoß
   voraus und ist nicht der Auffangtatbestand (für [JAHR] verifizieren).
   AEAO zu § 158 Nr. 4 und Nr. 5: die Folgen richten sich nach den Umständen
   des Einzelfalls (für [JAHR] verifizieren).
b) § 162 Abs. 1 Satz 1 AO Schätzungspflicht, soweit nicht ermittelt oder
   berechnet werden kann; Satz 2: alle Umstände, die für die Schätzung von
   Bedeutung sind, sind zu berücksichtigen. § 162 Abs. 2 Satz 1 AO: unzureichende
   Aufklärung, Verweigerung der Auskunft, Verletzung der Mitwirkungspflicht nach
   § 90 Abs. 2 AO. § 162 Abs. 2 Satz 2 AO: Nichtvorlage von Büchern oder
   Aufzeichnungen, Nichtzugrundelegung nach § 158 Abs. 2 AO, tatsächliche
   Anhaltspunkte für die Unrichtigkeit oder Unvollständigkeit
   (für [JAHR] verifizieren).
c) BFH, Urteil vom 18.06.2025 – X R 19/21, ECLI:DE:BFH:2025:U.180625.XR19.21.0,
   X. Senat, veröffentlicht am 25.09.2025; Diskothek mit offenen Ladenkassen,
   Streitjahre 2013 und 2014, Vorinstanz FG Hamburg vom 13.10.2020 – 2 K 218/18;
   Vorgeschichte: BFH, Beschluss vom 14.12.2022 – X R 19/21, Beitrittsaufforderung
   an das Bundesministerium der Finanzen nach § 122 Abs. 2 FGO
   (für [JAHR] verifizieren). Tragend ist:
   (1) Bei überwiegenden Bargeschäften können Mängel der Kassenführung der
       gesamten Buchführung die Ordnungsmäßigkeit nehmen.
   (2) und (3) Die Wahl zwischen mehreren möglichen Schätzungsmethoden ist
       Ermessen und durch § 5 AO gebunden; tendenziell ungenauere Methoden sind
       nachrangig, und DER INNERE BETRIEBSVERGLEICH IST IN DER REGEL
       ZUVERLÄSSIGER ALS DER ÄUSSERE.
   (4) Das Schätzungsergebnis muss NACHVOLLZIEHBAR BEGRÜNDET werden; wegen einer
       nicht nachvollziehbaren Begründung der Hinzuschätzung wurde aufgehoben und
       zurückverwiesen.
   (5) Datenbanken der Finanzverwaltung müssen MINDESTANFORDERUNGEN AN DIE
       QUALITÄT DER DATENERFASSUNG erfüllen; Rückfragen, die nicht beantwortet
       werden können, gehen zu Lasten des Beweiswerts.
d) LEITSATZ 6 – PRÄZISION IST HIER ENTSCHEIDEND. Der BFH formuliert "erhebliche
   Zweifel, ob die amtliche Richtsatzsammlung in ihrer bisherigen Form eine
   geeignete Grundlage für einen äußeren Betriebsvergleich darstellt". Diese
   Aussage ist nach den Urteilsgründen AUSDRÜCKLICH ERGÄNZEND UND NICHT TRAGEND.
   Du legst das bei jeder Verwendung offen und leitest daraus KEINE
   Erfolgsaussage ab. Verboten sind die Aussagen, der BFH habe die
   Richtsatzsammlung "gekippt" oder "für unzulässig erklärt", ebenso jede
   sinngleiche Umschreibung. Die Richtsatzschätzung bleibt grundsätzlich
   zulässig; Leitsatz 6 taugt als Argument, nicht als Ergebnis.
e) § 5 AO ist der Maßstab der Methodenwahl: Ermessen entsprechend dem Zweck der
   Ermächtigung und innerhalb der gesetzlichen Grenzen (für [JAHR] verifizieren).
f) §§ 145 und 146 AO für die Ordnungsmäßigkeit; § 147 Abs. 3 Satz 1 AO: für
   Buchungsbelege ACHT Jahre – nicht zehn. DAZU ZWINGEND DIE ABLAUFHEMMUNG:
   Nach § 147 Abs. 3 Satz 5 AO läuft die Aufbewahrungsfrist nicht ab, soweit
   und solange die Unterlagen für Steuern von Bedeutung sind, für welche die
   Festsetzungsfrist noch nicht abgelaufen ist. Solange die Streitjahre offen
   sind, ist der Einwand "Aufbewahrungsfrist abgelaufen" deshalb in der Regel
   unbegründet (für [JAHR] verifizieren).
g) VERFAHRENSRISIKEN DES EINSPRUCHS, die du in jeder Antwort ausdrücklich
   benennst, auch wenn nach dem Sachverhalt viel für einen Angriff spricht:
   § 367 Abs. 2 Satz 2 AO – der Verwaltungsakt kann im Einspruchsverfahren auch
   zum Nachteil des Einspruchsführers geändert werden, wenn zuvor darauf
   hingewiesen und Gelegenheit zur Äußerung gegeben wurde;
   § 364b Abs. 1 AO – das Finanzamt kann dem Einspruchsführer eine Frist zur
   Angabe von Tatsachen, zur Erklärung über klärungsbedürftige Punkte und zur
   Bezeichnung von Beweismitteln oder Vorlage von Urkunden setzen;
   § 364b Abs. 2 AO – danach vorgebrachte Erklärungen und Beweismittel sind
   nicht zu berücksichtigen, § 367 Abs. 2 Satz 2 AO bleibt unberührt und § 110
   AO gilt entsprechend; § 364b Abs. 3 AO – über diese Rechtsfolgen ist mit der
   Fristsetzung zu belehren, weshalb du bei einer Fristsetzung immer prüfen
   lässt, ob die Belehrung erteilt wurde (für [JAHR] verifizieren).

PRÜFE IN DIESER REIHENFOLGE UND HALTE JEDEN SCHRITT GESONDERT FEST
P1. SCHÄTZUNGSBEFUGNIS DEM GRUNDE NACH. Halte zuerst fest, für welche
    Steuerart(en) und welchen Zeitraum geschätzt wurde und welchen Anlass das
    Finanzamt dafür angibt; prüfe dabei, ob der Anlass alle genannten Steuerarten
    trägt oder nur einzelne. Arbeite dann die Kette aus Buchstabe a und b
    vollständig ab: Ist die Buchführung formell ordnungsmäßig (§§ 145, 146 AO)?
    Trägt der Mängelvorwurf die Nichtzugrundelegung nach § 158 Abs. 2 AO, und
    nach WELCHER NUMMER (Nr. 1 oder Nr. 2, siehe Buchstabe a)? Und folgt daraus
    ein Tatbestand des § 162 Abs. 2 Satz 2 AO? Werte dabei die
    Felder "vorgeworfene Mängel", "Anteil der Bargeschäfte" und "Kassenart"
    zusammen aus; Buchstabe c Nummer 1 greift nur bei überwiegenden
    Bargeschäften. Prüfe außerdem anhand der Felder "Zeitraum" und
    "Aufbewahrungsfrist abgelaufen", ob sich ein Mängelvorwurf auf Unterlagen
    stützt, deren Aufbewahrungsfrist abgelaufen sein kann (§ 147 Abs. 3 Satz 1
    AO, für Buchungsbelege acht Jahre). Halte in diesem Punkt IMMER die
    Ablaufhemmung des § 147 Abs. 3 Satz 5 AO dagegen und werte dafür das Feld
    "Festsetzungsfrist für die Streitjahre abgelaufen" aus: Steht dort "nein"
    oder "unklar", trägt der Einwand nicht und du kennzeichnest ihn als nicht
    tragfähig, statt ihn als Angriffspunkt aufzunehmen. Steht in einem der
    beiden Fristfelder "unklar", weise das als zu klärenden Punkt aus; die
    Fristen selbst berechnest du nicht.
P2. METHODENWAHL. Ordne die gewählte Methode ein und miss sie an § 5 AO und an
    Buchstabe c Nummern 2 und 3. Halte ausdrücklich fest, ob ein innerer
    Betriebsvergleich möglich gewesen wäre; werte dazu das Feld "Eigene Zahlen
    für einen inneren Betriebsvergleich verfügbar" aus. Steht dort "ja" oder
    "teilweise" und hat das Finanzamt gleichwohl den äußeren Betriebsvergleich
    gewählt, ist das der stärkste Angriffspunkt dieser Ebene. Steht dort "nein",
    sage das offen und benenne stattdessen, was beschafft werden müsste.
P3. BEGRÜNDUNGSTIEFE. Prüfe die gelieferte Begründung gegen Buchstabe c
    Nummer 4: Sind Ausgangsgrößen, Ansatz innerhalb des Rahmens, Zuordnung zur
    Gewerbeklasse und der Weg zum Ergebnis nachvollziehbar? Benenne jede Lücke
    einzeln. Bewerte nicht die Höhe, sondern die Nachvollziehbarkeit.
P4. DATENGRUNDLAGE. Prüfe die herangezogene Sammlung gegen Buchstabe c Nummer 5
    und stelle die Fragen zusammen, deren Unbeantwortbarkeit den Beweiswert
    mindert: Herkunft und Zahl der ausgewerteten Betriebe, Auswahl und
    Repräsentativität, Behandlung von Ausreißern, Zuordnung zur Gewerbeklasse,
    Aktualität des Jahrgangs. Nimm Buchstabe d hier auf – mit der Offenlegung,
    dass Leitsatz 6 nicht tragend ist.
P5. BETRIEBSINDIVIDUELLE ABWEICHUNGEN – DAS IST DIE EBENE DER HÖHE. Arbeite aus
    dem Feld "Betriebliche Besonderheiten" heraus, was den Betrieb vom
    Durchschnitt der Gewerbeklasse trennt, und ordne jeder Besonderheit den
    Nachweis zu, mit dem sie belegt werden müsste. Ohne Nachweis bleibt sie
    Behauptung; schreibe das dazu. Diese Ebene wird ohne Beträge, ohne Sätze
    und ohne Vergleichsrechnung bearbeitet – du benennst die Abweichung und
    ihren Nachweis, nicht ihre Auswirkung in Zahlen.
P6. VERFAHRENSRISIKEN. Werte das Feld "Verfahrensstand" aus und benenne die
    Risiken aus Buchstabe g. Steht dort "Prüfungsbericht liegt vor, kein
    Bescheid", weise darauf hin, dass die Einwendungen dort noch vor Erlass des
    Bescheids angebracht werden können. Steht dort ein Stand im
    Einspruchsverfahren, ist der Hinweis auf die Verböserungsmöglichkeit
    (§ 367 Abs. 2 Satz 2 AO) Pflichtbestandteil der Antwort. Steht dort "Klage
    erhoben", halte fest, dass dieser Prompt das Einspruchsverfahren abbildet
    und die weitere Bewertung dem Berufsträger obliegt.

ABBRUCHREGEL – an objektiven Angaben, nicht an einer Beurteilung
Eine Hinzuschätzung, ein Mängelvorwurf, eine verworfene Buchführung, eine offene
Ladenkasse und ein hoher Bargeldanteil sind KEIN Abbruchgrund – sie sind der
Anlass dieses Prompts. Brich die Bearbeitung nur ab, wenn (a) das erste
Bestätigungsfeld oder (b) das zweite Bestätigungsfeld nicht auf "bestätigt"
steht, auch dann, wenn das Feld unausgefüllt geblieben ist. Gib dann nur aus:
"Abbruchgrund liegt vor (Buchstabe angeben) – Bearbeitung an dieser Stelle
abgebrochen, Prüfung durch einen Berufsträger außerhalb des KI-Werkzeugs."

ANFORDERUNGEN
1. Gib zuerst eine EINSCHÄTZUNG DER EINDEUTIGKEIT ab: eindeutig / vertretbare
   Varianten / nicht ohne weitere Angaben entscheidbar. Liste fehlende Angaben
   auf und arbeite mit klar benannten Annahmen weiter.
2. Formuliere jede Aussage, die nicht aus den Angaben oder aus einer benannten
   Fundstelle folgt, ausdrücklich als Vermutung.
3. Höchstens zwölf Angriffspunkte, sortiert nach Ebene und innerhalb der Ebene
   nach Tragweite. Eine kurze tragfähige Liste ist besser als eine lange.
4. Höchstens 900 Wörter Fließtext; Tabellen und Listen zählen nicht mit.
5. Führe alle genannten Fundstellen am Ende in der Tabelle
   "Zu verifizierende Rechtsgrundlagen" mit der Spalte "geprüft von (leer)".

AUSGABEFORMAT
1. Einschätzung der Eindeutigkeit
2. (Angriffspunkte nach Ebenen) – Tabelle:
   Ebene (Grund / Methode / Begründung / Datengrundlage / betriebsindividuelle
   Abweichungen) | Angriffspunkt | Fundstelle | was dafür nachzuweisen ist |
   Erfolgsaussicht als Einschätzung mit Vorbehalt (hoch / mittel / gering /
   offen). Die Ebene der betriebsindividuellen Abweichungen ist das Ergebnis
   von P5 und bleibt ohne Zahlen.
3. (Kette dem Grunde nach) – § 158 Abs. 1 AO, § 158 Abs. 2 AO mit der
   einschlägigen Nummer, § 162 Abs. 2 Satz 2 AO, jeder Schritt einzeln mit
   Ergebnis und Fundstelle
4. (Gegenüberstellung der Methoden) – Tabelle:
   Methode | im Fall anwendbar (ja / nein / offen) | erwartete Genauigkeit |
   was sie voraussetzt | Bewertung nach § 5 AO
5. (Eigene Daten für den inneren Betriebsvergleich) – abhakbare Liste (Kästchen ☐)
   der Auswertungen und Unterlagen, die die Kanzlei aufbereiten muss, je mit
   Quelle und Verantwortlichem
6. (Fragenkatalog an das Finanzamt zur Datengrundlage) – nummerierte Fragen,
   sachlich, ohne Vorwurf, je mit dem Zweck der Frage
7. (Einordnung von Leitsatz 6) – eigener Absatz mit dem ausdrücklichen Hinweis,
   dass diese Aussage ergänzend und nicht tragend ist und dass die
   Richtsatzschätzung grundsätzlich zulässig bleibt
8. (Verfahrensrisiken) – Verböserung nach § 367 Abs. 2 Satz 2 AO, Präklusion
   nach § 364b Abs. 2 AO einschließlich der Belehrungspflicht des § 364b
   Abs. 3 AO, jeweils mit einem Satz, was das für diesen Fall bedeutet;
   dazu die Fristarten, die im Raum stehen, ohne Datum und ohne Dauer, je mit
   dem Satz "Fristen berechnet und erfasst ein Mensch."
9. (Textbausteine für die Begründung) – nach Ebenen gegliedert, mit
   Auslassungen zum Ausfüllen, ohne Beträge und ohne Berechnungen
10. (Offene Punkte) – was fehlt, wer es beschafft
11. (Zu verifizierende Rechtsgrundlagen) – Tabelle:
    Nr. | Fundstelle | wofür sie steht | geprüft von (leer)
```

## Anwendung

1. **Vor dem Werkzeugeinsatz vom Berufsträger beantworten und in der Handakte vermerken (Vorschaltfragen):** (a) Ist wegen der Streitjahre ein Steuerstraf- oder Bußgeldverfahren eingeleitet, angekündigt oder eine Selbstanzeige erwogen worden? (b) Werden wegen der Buchführung Haftungs- oder Regressansprüche gegen die Kanzlei geltend gemacht, oder ist der Vorgang dem Berufshaftpflichtversicherer angezeigt? Die bloße Möglichkeit, dass der Mandant die Kanzlei später in Anspruch nimmt, ist kein Hinderungsgrund – sie liegt jeder Hinzuschätzung bei selbst erstellter Buchführung zugrunde. Ist eine der Fragen mit ja zu beantworten, bleibt der Vorgang vollständig außerhalb des KI-Werkzeugs (Zone Rot in `DATENSCHUTZ.md`). Nur wenn beide Fragen dem Einsatz nicht entgegenstehen, wird das zweite Bestätigungsfeld auf „bestätigt" gesetzt.
2. Die Begründung des Finanzamts so wörtlich wie möglich übernehmen, ohne Kopf- und Fußzeilen. Aus der Wortwahl folgt, welche Ebene überhaupt angreifbar ist – eine zusammengefasste Begründung führt zu einer zusammengefassten Antwort.
3. Die Mängelliste ehrlich und einzeln eintragen, auch die berechtigten Punkte. Wer nur die bestrittenen Mängel einträgt, bekommt eine Angriffsliste, die im ersten Schriftwechsel zusammenfällt.
4. Vor dem Einspruch entscheiden, ob der innere Betriebsvergleich tatsächlich aufbereitet wird. Er ist der stärkste Angriff auf die Methodenwahl und zugleich der aufwendigste; wer ihn ankündigt und nicht liefert, verschlechtert die Lage.
5. Ergebnis nicht als Schriftsatz verwenden. Die Textbausteine gehen in die Einspruchsbegründung nach Prompt 33; dort entstehen Rubrum, Antrag und formaler Rahmen.
6. Vor jedem Vorbringen im Einspruchsverfahren die Verböserungsmöglichkeit mit dem Mandanten besprechen und das Gespräch dokumentieren.

## Qualitätssicherung

- **Das Ergebnis ist ein Entwurf.** Vor der Verwendung prüfen: Ist die Kette § 158 Abs. 1 AO – § 158 Abs. 2 AO – § 162 Abs. 2 Satz 2 AO vollständig ausgeschrieben, und wird die Schätzungsbefugnis nirgends allein aus § 158 Abs. 2 AO abgeleitet? Diese Abkürzung ist der häufigste Fehler zu dieser Norm.
- **Prüfen, ob bei § 158 Abs. 2 AO die Nummer genannt ist.** Kassen- und Aufzeichnungsmängel fallen unter Nr. 1 (Anlass, die sachliche Richtigkeit zu beanstanden); Nr. 2 setzt einen Verstoß gegen die einheitlichen digitalen Schnittstellen voraus und passt auf den Kassenfall nur, wenn die Kassendaten nicht schnittstellenkonform bereitgestellt wurden (für [JAHR] verifizieren).
- **Prüfen, ob ein Angriffspunkt auf eine abgelaufene Aufbewahrungsfrist gestützt wird.** Solange die Festsetzungsfrist der Streitjahre nicht abgelaufen ist, läuft auch die Aufbewahrungsfrist nicht ab (§ 147 Abs. 3 Satz 5 AO – für [JAHR] verifizieren). Ein solcher Einwand fällt im ersten Schriftwechsel zusammen und ist zu streichen.
- **Prüfen, ob der Text behauptet, der BFH habe die Richtsatzsammlung gekippt oder für unzulässig erklärt.** Leitsatz 6 des Urteils vom 18.06.2025 – X R 19/21 ist nach den Urteilsgründen ergänzend und nicht tragend; die Richtsatzschätzung bleibt grundsätzlich zulässig (für [JAHR] verifizieren). Eine Ausgabe, die daraus ein Ergebnis macht, ist an dieser Stelle falsch und im Schriftsatz angreifbar.
- **Prüfen, ob gerechnet wurde.** Der Prompt ermittelt keine Hinzuschätzungsbeträge und keine Aufschlagsätze. Jede Zahl in der Ausgabe, die nicht aus den Eingaben stammt, ist zu streichen.
- **Freigabe durch einen Berufsträger** für jede Äußerung gegenüber der Finanzbehörde und für die Entscheidung über den Rechtsbehelf (Freigabestufe 3 in `DATENSCHUTZ.md`).
- **Fristen berechnet und erfasst ein Mensch**, bei der Einspruchsfrist und bei jeder nach § 364b AO gesetzten Frist ausnahmslos mit Nachprüfung durch eine zweite Person anhand des Ausgangsdokuments. Kein Datum aus dem Modell übernehmen (siehe Prompt 35).
- **Prüfen, ob die Verböserungsmöglichkeit nach § 367 Abs. 2 Satz 2 AO im Text steht.** Fehlt sie, ist die Ausgabe unvollständig, weil der Einspruch dann als risikofreies Mittel erscheint.
- **Prüfen, ob Erfolgsaussichten als Prognose formuliert sind.** Zulässig ist eine Einschätzung mit Vorbehalt, nicht die Aussage, das Finanzamt oder ein Gericht werde so entscheiden.
- **Rechtsstand prüfen an:** §§ 5, 145, 146, 147, 158, 162, 364b und 367 AO im amtlichen Volltext (gesetze-im-internet.de), am Anwendungserlass zur Abgabenordnung zu § 158 sowie am Volltext des BFH-Urteils vom 18.06.2025 – X R 19/21 einschließlich der Frage, ob die Finanzverwaltung inzwischen reagiert hat.

## Varianten

- **Vor dem Bescheid:** „Beschränke dich auf Einwendungen gegen den Prüfungsbericht vor Erlass des Änderungsbescheids und benenne, was jetzt noch ohne Rechtsbehelf erreichbar ist."
- **Nur Methodenkritik:** „Erzeuge allein die Gegenüberstellung der Methoden und die Bewertung nach § 5 AO, höchstens 300 Wörter."
- **Aufbereitungsauftrag intern:** „Erzeuge nur die Liste der eigenen Daten für den inneren Betriebsvergleich, mit Quelle, Verantwortlichem und einer Spalte ‚geschätzter Aufwand (von der Kanzlei einzutragen)'."
- **Mandantengespräch:** „Fasse die Lage in Sie-Form für den Mandanten zusammen, höchstens 350 Wörter, ohne interne Bewertungen, mit ausdrücklichem Hinweis auf die Verböserungsmöglichkeit."
- **Schulungsfall:** „Formuliere den Sachverhalt als anonymisierten Übungsfall für die Teambesprechung, mit drei Entscheidungspunkten und ohne Lösung."
