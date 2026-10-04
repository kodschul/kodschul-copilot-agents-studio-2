# Lab 2.2: Prompt-Optimierung nach Vorgehensschema

**Leitfragen:**

<details>
<summary>Wie merkt man, dass der Prompt und nicht das Modell das Problem ist?</summary>

Wenn das Ergebnis in sich schlüssig, aber am Bedarf vorbei ist. Modellprobleme äußern sich als falsche Fakten, Promptprobleme als falscher Zuschnitt.

</details>

<details>
<summary>Wann hört man mit dem Optimieren auf?</summary>

Wenn die nächste Iteration länger dauert als die manuelle Nacharbeit, oder wenn die fehlende Information in der Quelle gar nicht vorhanden ist.

</details>

- Ein unbrauchbares Ergebnis ist selten ein Modellfehler, sondern meist eine fehlende Angabe im Prompt.
- Ein wiederholbares Schema hilft, diese Lücke gezielt zu finden.

## Das Vorgehensschema

```
1. Ergebnis gegen den Bedarf halten  →  was genau stört?
2. Störung einem Checklistenpunkt zuordnen (1–6)
3. Genau eine Angabe ergänzen
4. Erneut ausführen und vergleichen
5. Abbrechen, wenn keine Verbesserung mehr eintritt
```

Nur **eine** Angabe pro Runde ändern. Werden drei Dinge gleichzeitig ergänzt, bleibt unklar, welche gewirkt hat.

> **Merksatz:** Ein schlechtes Ergebnis ist eine Diagnosefrage, keine Wiederholungsfrage. Erst benennen, was fehlt, dann ergänzen.

## Störung → Checklistenpunkt

| Beobachtete Störung                              | Fehlender Punkt         |
| ------------------------------------------------ | ----------------------- |
| Ton passt nicht zum Adressaten                   | 2 Kontext, 5 Sprachstil |
| Antwort ist richtig, aber unbrauchbar lang       | 4 Struktur              |
| Text kreist um das Thema, ohne zu liefern        | 1 Klarheit, 3 Fokus     |
| Einträge sind uneinheitlich aufgebaut            | 6 Beispiele             |
| Inhalte sind allgemein statt projektbezogen      | 2 Kontext               |
| Wichtiges fehlt, Nebensächliches ist ausführlich | 3 Fokus                 |

## Prompt-Problem oder Quellenproblem?

| Symptom                                     | Ursache         | Reaktion                                       |
| ------------------------------------------- | --------------- | ---------------------------------------------- |
| Zuschnitt, Ton, Format passen nicht         | Prompt          | Angabe ergänzen                                |
| Erfundene Namen, Zahlen, Termine            | fehlende Quelle | Quelle mitgeben oder Angabe streichen          |
| Inhalt fehlt vollständig, obwohl gefordert  | Quelle          | prüfen, ob die Information überhaupt existiert |
| Ergebnis schwankt bei gleichem Prompt stark | Modellverhalten | akzeptieren, Ergebnis prüfen statt optimieren  |

## Abbruchkriterien

- Zwei Runden ohne erkennbare Verbesserung.
- Die fehlende Information steht nicht in der bereitgestellten Quelle.
- Die Nacharbeit von Hand dauert kürzer als die nächste Iteration.

## Fazit

- Erst diagnostizieren, welcher Checklistenpunkt fehlt, dann ergänzen.
- Pro Runde genau eine Angabe ändern, sonst ist die Wirkung nicht zuzuordnen.
- Prompt-Probleme sind lösbar, Quellenprobleme nicht — die Unterscheidung spart die meiste Zeit.

In der Übung wird ein schwacher Baseline-Prompt am Nordwind-Fall in dokumentierten Runden verbessert.
