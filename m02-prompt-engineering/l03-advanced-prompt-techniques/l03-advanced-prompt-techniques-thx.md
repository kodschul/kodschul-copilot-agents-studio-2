# Lab 2.3: Fortgeschrittene Prompt-Techniken

**Leitfragen:**

<details>
<summary>Wann lohnt sich Few-Shot gegenüber einer reinen Beschreibung?</summary>

Wenn das gewünschte Format schwer zu beschreiben, aber leicht zu zeigen ist — etwa bei einer festen Eintragsstruktur oder einem bestimmten Tonfall.

</details>

<details>
<summary>Bei welcher Art von Aufgabe bringt Chain-of-Thought spürbar bessere Ergebnisse?</summary>

Bei mehrstufigen Aufgaben mit Zwischenergebnissen: Berechnungen, Vergleiche mit mehreren Kriterien, Ursachenanalysen.

</details>

<details>
<summary>Was unterscheidet ReAct von Chain-of-Thought?</summary>

Chain-of-Thought denkt in einem Zug durch. ReAct wechselt zwischen Überlegen und Handeln: nachsehen, Ergebnis bewerten, nächsten Schritt entscheiden.

</details>

- Die Checkliste aus Lab 2.1 macht einen Prompt vollständig; die hier behandelten Techniken bestimmen, **wie** das Modell an die Aufgabe herangeht.
- Zero-/One-/Few-Shot, Chain-of-Thought und ReAct lassen sich nach Einsatzfall ordnen.

## Die Techniken im Überblick

| Technik              | Prinzip                                              | Passt bei                                       |
| -------------------- | ---------------------------------------------------- | ----------------------------------------------- |
| Zero-Shot            | reine Anweisung, kein Beispiel                       | klaren Standardaufgaben                         |
| One-Shot             | ein Beispiel mitgeben                                | einem festen Format, das gezeigt werden soll    |
| Few-Shot             | zwei bis fünf Beispiele mitgeben                     | Mustern mit Varianten, Tonfall, Kategorisierung |
| Chain-of-Thought     | Lösungsweg Schritt für Schritt darlegen lassen       | mehrstufigen Analysen mit Zwischenergebnissen   |
| ReAct (Reason + Act) | abwechselnd überlegen und Informationen holen/prüfen | Aufgaben mit Recherche- oder Prüfschritten      |

> **Merksatz:** Few-Shot steuert, wie das Ergebnis **aussieht**. Chain-of-Thought steuert, wie das Modell **vorgeht**.

## Zero-Shot: reine Anweisung, kein Beispiel

| Prompt                                                           | Typisches Ergebnis                                                                                                                                                  |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "Kategorisiere diese Kundenanfrage: 'Wo bleibt meine Rechnung?'" | "Kategorie: Buchhaltung" — im nächsten Durchlauf, gleiche Anfrage: "Kategorie: Rechnungswesen". Das Modell erfindet Kategorien neu, statt sie konsistent zu halten. |

| Vorteile                           | Nachteile                                     |
| ---------------------------------- | --------------------------------------------- |
| Kein Aufwand für Beispiele         | Modell entscheidet Format & Kategorien selbst |
| Schnell getippt, sofort einsetzbar | Ergebnis schwankt zwischen Durchläufen        |

**Wann ja:** bei klaren Standardaufgaben, bei denen jedes plausible Format passt.
**Wann nicht:** sobald ein festes Format oder Tonfall eingehalten werden muss.

## One-Shot: ein Beispiel mitgeben

| Prompt                                                                                                                                         | Typisches Ergebnis                                                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "Kategorisiere diese Kundenanfragen. Beispiel: 'Rechnung unklar' → Kategorie: Abrechnung. Neu: 'Login geht nicht'; 'Handyvertrag verlängern?'" | "Login geht nicht" → Abrechnung (falsch übernommen, da nur ein Beispiel als Vorlage diente). "Handyvertrag verlängern?" → Vertrag (zufällig richtig geraten). |

| Vorteile                              | Nachteile                                          |
| ------------------------------------- | -------------------------------------------------- |
| Format wird grob vorgegeben           | Ein Beispiel deckt Varianten nicht ab              |
| Wenig Mehraufwand gegenüber Zero-Shot | Modell übergeneralisiert leicht aus dem einen Fall |

**Wann ja:** wenn ein festes Format gezeigt werden soll, aber Varianz kein Thema ist.
**Wann nicht:** bei Aufgaben mit vielen unterschiedlichen Fallgruppen — hier reicht ein Beispiel nicht.

## Few-Shot: zwei bis fünf Beispiele mitgeben

| Prompt                                                                                                                                                                         | Typisches Ergebnis                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| "Kategorisiere diese Kundenanfragen. Beispiele: 'Rechnung unklar' → Abrechnung; 'Login geht nicht' → Technik; 'Vertrag kündigen' → Vertrag. Neu: 'Handy kaputt, Ersatz nötig'" | "Handy kaputt, Ersatz nötig" → Technik (passt ins gelernte Muster, bleibt über mehrere Durchläufe konsistent bei „Technik“). |

| Vorteile                                           | Nachteile                                          |
| -------------------------------------------------- | -------------------------------------------------- |
| Deckt mehrere Varianten/Kategorien gleichzeitig ab | Längerer Prompt, mehr Pflegeaufwand                |
| Stabileres, wiederholbares Ergebnis                | Schlecht gewählte Beispiele verzerren das Ergebnis |

**Wann ja:** bei Mustern mit Varianten, Tonfall- oder Kategorisierungsaufgaben.
**Wann nicht:** bei einmaligen Aufgaben ohne wiederkehrendes Muster — der Mehraufwand lohnt sich nicht.

Drei Beispiele reichen fast immer. Mehr als fünf verlängern den Prompt ohne Zusatznutzen.

## Chain-of-Thought: Lösungsweg Schritt für Schritt

Auslösende Formulierung: _"Gehe schrittweise vor und zeige die Zwischenschritte, bevor du das Ergebnis nennst."_

Beispielfrage: Kann Projekt X wie geplant starten? (AP2: 70 %, AP4: 0 %, AP4 hängt von AP2 ab)

| Ohne CoT                     | Mit CoT                                                                                                                                                 |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "Nein, Start ist gefährdet." | "1. AP2 ist zu 70 % fertig. 2. AP4 hängt von AP2 ab und liegt noch bei 0 %. 3. Ohne AP4 kann der Rollout nicht starten. Ergebnis: Start ist gefährdet." |

| Vorteile                                            | Nachteile                                                    |
| --------------------------------------------------- | ------------------------------------------------------------ |
| Zwischenschritte sind prüfbar, Fehler lokalisierbar | Längere, langsamere Antworten                                |
| Bessere Ergebnisse bei mehrstufigen Analysen        | Zwischenschritte können selbst falsch sein — trotzdem prüfen |

**Wann ja:** bei mehrstufigen Analysen mit Zwischenergebnissen (z. B. Risikobewertung).
**Wann nicht:** bei simplen Ein-Schritt-Aufgaben — unnötig lang und langsamer ohne Mehrwert.

Der eigentliche Gewinn ist nicht nur ein besseres Ergebnis, sondern ein **prüfbares** Ergebnis.

## ReAct: abwechselnd überlegen und nachschlagen/prüfen

Muster: _Überlegen → Nachsehen → Bewerten → nächster Schritt._

```
Gedanke:  Um die Verzugsfolge zu beurteilen, brauche ich den Status von AP2 und AP4.
Handlung: Projektnotizen nach AP2 und AP4 durchsuchen.
Ergebnis: AP2 bei 70 %, AP4 bei 0 %, AP4 hängt an AP2.
Gedanke:  Damit ist der Rollout-Start direkt blockiert.
```

| Vorteile                                                | Nachteile                                                     |
| ------------------------------------------------------- | ------------------------------------------------------------- |
| Überlegen und Nachsehen sind beide sichtbar und prüfbar | Aufwändigster Prompt-Stil, mehrere Runden nötig               |
| Reduziert Halluzinationen bei Recherche-Aufgaben        | Ohne echte Datenquelle (RAG) bleibt „Nachsehen“ nur simuliert |

**Wann ja:** bei Aufgaben mit Recherche- oder Prüfschritten gegen eine echte Quelle.
**Wann nicht:** ohne verfügbare Quelle zum Nachschlagen — dann bleibt es reines Chain-of-Thought.

Passt, wenn die Antwort aus mehreren Quellenstellen zusammengesetzt werden muss.

## Grenzen

- Chain-of-Thought macht die Antwort länger; bei einfachen Aufgaben ist das reiner Mehraufwand.
- Sichtbare Zwischenschritte sind kein Beweis für Korrektheit — auch ein falscher Weg wird flüssig dargestellt.
- Few-Shot-Beispiele wirken stark: schiefe Beispiele erzeugen zuverlässig schiefe Ergebnisse.
- ReAct hängt davon ab, dass die nachgeschlagene Quelle tatsächlich verfügbar ist.

## Fazit

- Zero → One → Few-Shot: steigende Formatkontrolle und Konsistenz durch Beispiele statt Beschreibung.
- Chain-of-Thought macht mehrstufige Aufgaben prüfbar, nicht automatisch richtig.
- ReAct passt, wenn zwischen Überlegen und Nachsehen gewechselt werden muss.
- Jede Technik hat einen klaren Vorteil, einen klaren Nachteil und einen Punkt, ab dem sie nicht mehr passt — die Wahl richtet sich nach Aufgabe, nicht nach Vorliebe.

In der Übung wird dieselbe mehrstufige Nordwind-Analyse einmal Zero-Shot und einmal mit Chain-of-Thought bzw. ReAct gelöst und die Ergebnisqualität verglichen.
