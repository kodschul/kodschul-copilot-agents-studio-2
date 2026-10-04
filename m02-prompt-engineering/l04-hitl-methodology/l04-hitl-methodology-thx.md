# Lab 2.4: Human-in-the-Loop-Methodik

**Leitfragen:**

<details>
<summary>Warum liefert "erstelle mir eine Präsentation" selten ein brauchbares Ergebnis?</summary>

Weil die eigentlichen Entscheidungen — Kernbotschaft, Gliederung, Gewichtung — mit abgegeben werden. Copilot trifft sie dann nach Plausibilität statt nach Absicht.

</details>

<details>
<summary>An welchen Stellen im Ablauf muss der Mensch zwingend entscheiden?</summary>

Bei der Kernbotschaft, bei der Gliederung und bei der Gewichtung. Das Ausformulieren darf abgegeben werden.

</details>

<details>
<summary>Wo würde sich HITL im eigenen Arbeitsalltag zuerst lohnen?</summary>

Bei längeren Ergebnisdokumenten mit fester Erwartungshaltung: Angebote, Konzepte, Berichte, Pitchdecks.

</details>

- Ein einzelner Prompt wie "Erstelle mir eine Präsentation" liefert zuverlässig ein Ergebnis, das niemand so halten würde.
- Vier Schritte zerlegen die Aufgabe so, dass der Mensch die inhaltlichen Entscheidungen behält.

## Das Problem mit dem One-Shot-Prompt

| Was abgegeben wird | Was passiert                                         |
| ------------------ | ---------------------------------------------------- |
| Kernbotschaft      | Copilot wählt die naheliegendste, nicht die gewollte |
| Gliederung         | Standardaufbau statt Argumentationslinie             |
| Gewichtung         | alle Punkte gleich lang, unabhängig von Wichtigkeit  |
| Ausformulierung    | unproblematisch — das ist die eigentliche Stärke     |

Die ersten drei Zeilen sind die Arbeit. Nur die vierte lässt sich sinnvoll delegieren.

> **Merksatz:** Nicht das Schreiben abgeben, sondern das Tippen. Die Entscheidungen bleiben beim Menschen.

## Die vier Schritte

| Schritt       | Was passiert                                      | Wer entscheidet    | Copilot-Rolle                                      |
| ------------- | ------------------------------------------------- | ------------------ | -------------------------------------------------- |
| 1 Vision      | Kernbotschaft und Adressat in ein bis zwei Sätzen | Mensch             | schärft die Formulierung, schlägt Alternativen vor |
| 2 Gliederung  | Inhaltsverzeichnis gemeinsam klären und kürzen    | Mensch entscheidet | schlägt Struktur vor, Mensch streicht              |
| 3 Kerninhalte | je Abschnitt die Kernaussage festlegen            | Mensch             | fragt nach Lücken, ordnet zu                       |
| 4 Scaffold    | Copilot baut das Gerüst aus Schritt 1–3           | Copilot            | formuliert aus                                     |

Nach Schritt 3 steht die inhaltliche Arbeit. Schritt 4 ist Ausführung.

## Vorher / Nachher

| Ansatz   | Ablauf                                         | Nacharbeit          |
| -------- | ---------------------------------------------- | ------------------- |
| One-Shot | ein Prompt → fertiges Dokument → alles umbauen | hoch, oft Neuanfang |
| HITL     | vier kurze Runden → Gerüst passt → Feinschliff | gering, gezielt     |

Der Gesamtaufwand ist ähnlich. Der Unterschied: Bei HITL fällt der Aufwand vorne an, wo Korrekturen billig sind.

## Verbindung zu den Techniken aus Lab 2.3

| Schritt       | Passende Technik                                    |
| ------------- | --------------------------------------------------- |
| 1 Vision      | Zero-Shot mit Rolle und Adressat                    |
| 2 Gliederung  | Chain-of-Thought — Gliederungslogik sichtbar machen |
| 3 Kerninhalte | ReAct, wenn Quellen herangezogen werden müssen      |
| 4 Scaffold    | Few-Shot, wenn ein Formatmuster existiert           |

HITL ersetzt die Techniken nicht; es ordnet sie einem Arbeitsablauf zu.

## Grenzen

- Für kurze Texte ist der Vier-Schritt-Ablauf Mehraufwand; ab etwa einer Seite lohnt er.
- Wird Schritt 2 nur abgenickt statt geprüft, ist es wieder ein One-Shot mit Zwischenstopps.
- HITL verhindert keine Halluzinationen in den Inhalten; es verbessert Struktur und Zuschnitt.

## Fazit

- Kernbotschaft, Gliederung und Gewichtung bleiben beim Menschen; das Ausformulieren geht an Copilot.
- Die vier Schritte verlagern den Aufwand nach vorne, wo Korrekturen billig sind.
- Eine abgenickte Gliederung ist kein HITL — Schritt 2 lebt vom Streichen.

In der Übung entsteht die HITL-Gliederung für das Nordwind-Pitchdeck, das in Modul 3 tatsächlich gebaut wird.
