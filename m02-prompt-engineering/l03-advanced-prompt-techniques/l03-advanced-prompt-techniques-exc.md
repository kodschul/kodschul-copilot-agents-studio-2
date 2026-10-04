# Lab 2.3 – Übung: Zero-Shot gegen Chain-of-Thought und ReAct

**Ändert die Nordwind-Projektbasis?** Nein — Technikvergleich auf bereitgestellten Projektdaten.

## Ausgangslage

Der Lenkungsausschuss fragt: _Welche zwei Arbeitspakete gefährden den Projekterfolg am stärksten, und welches Budgetrisiko ergibt sich daraus?_

Die Antwort erfordert mehrere Zwischenschritte: Status der Arbeitspakete lesen, Abhängigkeiten erkennen, mit der Risikoliste abgleichen, Budgetverbrauch gegen Fortschritt halten.

Bereitgestellt: `nordwind-projektnotizen.md` in `output/project/`.

## Aufgaben

1. Die Frage Zero-Shot stellen — ohne Vorgehenshinweis, ohne Beispiel. Das Ergebnis speichern.
2. Das Zero-Shot-Ergebnis auf Nachvollziehbarkeit prüfen: Ist erkennbar, **woraus** die Einschätzung abgeleitet wurde? Notieren, an welcher Stelle die Herleitung fehlt.
3. Dieselbe Frage mit Chain-of-Thought stellen (Vorgehen schrittweise darlegen lassen, Zwischenschritte vor dem Ergebnis). Das Ergebnis speichern.
4. Die Zwischenschritte aus Aufgabe 3 einzeln gegen die Projektnotizen prüfen. Jeden Schritt als "belegt" oder "nicht belegt" markieren.
5. Dieselbe Frage im ReAct-Muster stellen: das Modell anweisen, abwechselnd zu überlegen und gezielt in den Notizen nachzusehen, und beides sichtbar zu machen.
6. Die drei Ergebnisse in einer Tabelle vergleichen: Ergebnisqualität, Prüfbarkeit, Länge, Aufwand.
7. Entscheiden und begründen, welche Technik für diese Frage die passende ist.

## Checkpoint

- Drei Ergebnisse liegen vor und sind den drei Techniken eindeutig zugeordnet.
- Aus Aufgabe 4 liegt eine Schritt-für-Schritt-Bewertung vor, in der mindestens ein Schritt einzeln geprüft wurde.
- Die Vergleichstabelle aus Aufgabe 6 ist in allen vier Spalten gefüllt.

## Abschlusskriterien

- Die Entscheidung aus Aufgabe 7 ist an Prüfbarkeit oder Aufwand festgemacht, nicht an "las sich besser".
- Falls ein Zwischenschritt als "nicht belegt" markiert wurde: benannt, welche Angabe fehlt oder erfunden ist.

## Erweiterung

Die Frage ein viertes Mal stellen, diesmal Few-Shot: zwei Beispiele für das gewünschte Antwortformat mitgeben (Arbeitspaket – Gefährdung – Budgetwirkung). Festhalten, was sich gegenüber Chain-of-Thought an Form und Inhalt ändert.

## Fallback

Ohne Copilot-Zugriff: Die drei Prompts ausformulieren und je Technik vorhersagen, wie das Ergebnis strukturiert sein wird. Der Abgleich erfolgt an der Trainer-Demo. Einschränkung: Die Prüfung einzelner Zwischenschritte (Aufgabe 4) entfällt.
