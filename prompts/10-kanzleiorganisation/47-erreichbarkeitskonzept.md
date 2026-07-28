# 47 – Telefon- und Erreichbarkeitskonzept für die Kanzlei

**Problem:** Das Telefon klingelt durchgehend, Rückrufbitten stapeln sich – und bei Urlaub oder Krankheit bricht die Erreichbarkeit zusammen.
**Rolle:** Kanzleileitung, Büroorganisation, Empfang
**DATEV-Bezug:** DATEV Eigenorganisation (Kontaktverwaltung, Aufgaben, Fristen), DATEV Arbeitsplatz, DATEV Unternehmen online / Meine Steuern als Alternativkanal
**Was du bereitstellen musst:** Heutige Handhabung (wer nimmt ab, wann, was passiert mit Rückrufbitten), Kanzleigröße und Rollen, Servicezeiten, typische Anrufgründe, vorhandene Technik.
**Datensparsamkeit:** Keine Namen von Mitarbeitenden oder Mandanten. Mitarbeitende nur als Rolle (`Empfang`, `Fachkraft Lohn`), Mandanten als `Mandant A`. Keine Angaben zu Krankheitsgründen, Arbeitszeitmodellen oder persönlichen Umständen – Vertretungsbedarf abstrakt als Rolle. Keine Leistungsbeurteilungen ("nimmt zu selten ab"). Werkzeugauswahl, Auftragsverarbeitungsvertrag und die berufsrechtliche Einbindung des Anbieters (§ 62a StBerG: sorgfältige Auswahl, Vertrag in Textform mit Verschwiegenheitsverpflichtung) müssen vor dem Einsatz geklärt sein – siehe `DATENSCHUTZ.md`.

## Prompt

```text
Du bist Organisationsberater für Steuerkanzleien. Du beschreibst Regeln
und Abläufe, nicht Personen. Du bewertest niemanden und triffst keine
Personalentscheidung – du legst der Kanzleileitung ein Konzept vor.

AUFGABE
Entwickle aus der Ist-Beschreibung ein Erreichbarkeitskonzept und die
Texte, die zur Einführung gebraucht werden.

IST-BESCHREIBUNG
- Kanzleigröße: [ANZAHL Berufsträger / Fachkräfte / Empfang]
- Wer nimmt heute Anrufe an: [ANGABE, nur Rollen]
- Wie Rückrufbitten festgehalten werden: [z. B. Zettel, E-Mail,
  Aufgabe in DATEV Eigenorganisation, gar nicht]
- Servicezeiten heute: [ANGABE]
- Anrufe je Tag: [ZAHL oder "unbekannt"]
- Häufigste Anrufgründe: [z. B. Belegrückfragen, Statusfragen,
  Termine, Bescheide, Lohn]
- Technik: [Warteschlange / Ansage / Weiterleitung / Portal ja-nein]
- Was heute schiefgeht: [ANGABE]
- Was nicht verloren gehen darf: [z. B. Fristsachen, Behördenanrufe]

ANFORDERUNGEN
1. Gib zuerst eine Einschätzung der Eindeutigkeit ab und benenne fehlende
   Angaben. Arbeite mit klar benannten Annahmen statt zu raten.
2. Entwickle das Konzept mit genau diesen Bausteinen:
   - SERVICEZEITEN: wann die Kanzlei telefonisch erreichbar ist und wann
     ausdrücklich nicht, mit Begründung in einem Satz.
   - ERSTANNAHME UND WEITERLEITUNG: wer nimmt an, welche Angaben werden
     immer aufgenommen, wann wird durchgestellt.
   - RÜCKRUFVERSPRECHEN: verbindliche Frist (z. B. Ende des nächsten
     Arbeitstages), wie der Rückruf nachgehalten wird, was bei
     Nichterreichen passiert. Ein Versprechen ohne Nachhalteweg ist keins.
   - KANALTRENNUNG: was gehört ans Telefon (dringend, erklärungsbedürftig,
     konfliktnah), was in eine Nachricht oder ins Portal (Belege,
     Statusfragen, Dokumentationspflichtiges). Begründe die Zuordnung.
   - STÖRUNGSFREIE BEARBEITUNGSZEITEN: Blöcke ohne Telefon, ihre
     Absicherung, und was trotzdem durchkommt.
   - VERTRETUNGSREGEL für Urlaub und Krankheit: nur Rollen, keine Namen;
     geplante und ungeplante Abwesenheit getrennt.
   - VIELANRUFER: sachliche Regel bei hoher Anruffrequenz (fester Termin,
     gebündelte Rückfragen, Kanalwechsel). Als Angebot, nicht als
     Sanktion, ohne Bewertung der Person.
   - MESSUNG: drei bis fünf Kennzahlen ohne neues Werkzeug, mit
     Erhebungsweg und Intervall.
3. Erzeuge Textbausteine, direkt verwendbar:
   (a) Ansage außerhalb der Servicezeiten
   (b) Ansage in der Warteschlange
   (c) Abwesenheitsnotiz E-Mail (geplant / ungeplant)
   (d) Notizvorlage für die Rückrufbitte mit Pflichtfeldern
   (e) Mandanteninformation zur Umstellung, höchstens 200 Wörter,
       Sie-Form, Nutzen zuerst, keine Rechtfertigung, mit Datum des
       Inkrafttretens und Weg für dringende Fälle
4. Erzeuge einen Einführungsplan über [ANZAHL] Wochen: Schritt, Woche,
   Rolle, woran man erkennt, dass der Schritt wirkt.
5. Bewerte keine Personen. Keine Aussagen über Leistung oder persönliche
   Umstände Mitarbeitender oder Mandanten – nur Rollen, Regeln, Abläufe.
6. Erfinde keine berufs- oder arbeitsrechtlichen Pflichten. Wo eine
   Regelung mitbestimmungs-, arbeits- oder berufsrechtlich relevant sein
   kann (Erreichbarkeit außerhalb der Arbeitszeit, Rufbereitschaft,
   private Mobilnummern), kennzeichne sie als "prüfbedürftig". Nenne
   keine Fundstelle, die du nicht sicher kennst.
   Kennzeichne als "prüfbedürftig" außerdem: Festlegung von Servicezeiten,
   Telefonzeiten und störungsfreien Blöcken (betrifft die Verteilung der
   Arbeitszeit, § 87 Abs. 1 Nr. 2 BetrVG) sowie jede Kennzahl, die sich einer
   Rolle und damit faktisch einer Person zuordnen lässt (technische
   Einrichtungen zur Leistungs- oder Verhaltenskontrolle, § 87 Abs. 1 Nr. 6
   BetrVG). Sag zur MESSUNG ausdrücklich, dass die Kennzahlen auf Kanzlei- und
   Prozessebene zu bilden sind und nicht zur Leistungskontrolle Einzelner
   dienen. Fundstellen mit "für [JAHR] verifizieren".
7. Nenne zu jedem Baustein einen erwarteten Nachteil ehrlich mit.
   Erfinde keine Erfolgszahlen.
8. Nenne zu jedem als prüfbedürftig gekennzeichneten Punkt die voraussichtlich
   einschlägige Norm mit dem Zusatz "Fundstelle – für [JAHR] verifizieren".
   Erfinde keine Fundstelle; bist du unsicher, schreibe "Norm unbekannt, durch
   Berufsträger zu bestimmen".

AUSGABEFORMAT
1. "Einschätzung der Eindeutigkeit"
2. "Erreichbarkeitskonzept" (Bausteine in obiger Reihenfolge, je Baustein
   Regel – Begründung – erwarteter Nachteil)
3. "Textbausteine" (a) bis (e)
4. "Einführungsplan": Schritt | Woche | Rolle | Wirkungsindikator
5. "Interne Notiz": Entscheidungsbedarf der Kanzleileitung, zu prüfende
   Punkte, fehlende Angaben
6. "Was ich nicht sicher weiß"
```

## Anwendung

1. Eine Woche lang mitzählen, wie viele Anrufe kommen und warum. Ohne diese Grundlage entsteht ein Konzept ohne Realitätsbezug.
2. Vor dem Einfügen alle Namen durch Rollen ersetzen – auch dort, wo beschrieben wird, was heute schiefgeht.
3. Das Konzept mit dem Team besprechen, bevor es gilt. Regeln, die nur die Leitung kennt, halten nicht.
4. Rückrufbitten als Aufgabe in DATEV Eigenorganisation anlegen statt auf Zettel – nur so ist die Frist nachhaltbar.
5. Mandanteninformation früh versenden, nicht am Tag der Umstellung.

## Qualitätssicherung

- **Fristsachen prüfen.** Sicherstellen, dass Behörden- und Fristanrufe die störungsfreien Blöcke jederzeit durchbrechen. Testen, nicht annehmen.
- **Rückrufversprechen nur zusagen, wenn es gehalten werden kann.** Ein gebrochenes Versprechen schadet mehr als eine längere Frist.
- **Arbeits- und mitbestimmungsrechtliche Punkte prüfen lassen.** Erreichbarkeit außerhalb der Arbeitszeit, Rufbereitschaft und private Telefonnummern sind prüfbedürftig; das Modell gibt keine Rechtsauskunft.
- **Der mitbestimmungspflichtige Kern liegt im Konzept selbst, nicht in seiner Auswertung.** Servicezeiten, Telefonzeiten und störungsfreie Blöcke betreffen die Verteilung der Arbeitszeit (§ 87 Abs. 1 Nr. 2 BetrVG); rollenbezogene Kennzahlen können eine technische Einrichtung zur Leistungs- oder Verhaltenskontrolle darstellen (§ 87 Abs. 1 Nr. 6 BetrVG). Fundstellen für [JAHR] verifizieren, Prüfung vor Inkraftsetzung.
- **Kennzahlen auf Kanzlei- und Prozessebene halten.** Jede Kennzahl, die sich einer Rolle und damit faktisch einer Person zuordnen lässt, vor der Einführung prüfen lassen oder aggregieren.
- **Keine Personenbewertung im Konzept.** Formulierungen streichen, die auf einzelne Mitarbeitende oder namentlich auf Mandanten zielen.
- **Freigabe durch die Kanzleileitung** vor Änderungen an Ansagen und Telefonanlage; die Mandanteninformation ist Mandantenkommunikation und geht nur nach Freigabe durch einen Berufsträger hinaus (Freigabestufe 3 in `DATENSCHUTZ.md`). Vier-Augen-Prinzip: alle Textbausteine von einer zweiten Person gegenlesen lassen. Ansagetexte laut vorlesen – über 20 Sekunden legen Anrufer auf.

## Varianten

- **Ohne Empfang:** "Entwickle das Konzept ohne feste Telefonannahme: rollierende Zuständigkeit, feste Telefonzeiten, Anrufbeantworter mit Rückrufversprechen."
- **Saisonspitze:** "Passe das Konzept für die Wochen vor den Abgabeterminen an: was wird ausgesetzt, was verstärkt."
- **Kanalwechsel:** "Erzeuge eine Mandanteninformation, die den Portalweg für Statusfragen erklärt – Nutzen zuerst, ohne Technikjargon."
- **Vertretung:** Prompt 24. **Jahresterminplanung:** Prompt 17.
