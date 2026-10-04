# Lab 2.3 – Lösung: Zero-Shot gegen Chain-of-Thought und ReAct

## Aufgaben

### 1. Zero-Shot

```text
Welche zwei Arbeitspakete gefährden den Projekterfolg am stärksten, und welches
Budgetrisiko ergibt sich daraus? Grundlage sind die beigefügten Projektnotizen.
```

Erwartetes Ergebnis: AP2 und AP3 werden genannt, mit kurzer Begründung. Die Budgetaussage bleibt meist vage ("erhebliches Risiko", "zusätzlicher Aufwand möglich") oder enthält eine nicht hergeleitete Zahl.

### 2. Fehlende Herleitung

| Aussage im Ergebnis      | Herleitung erkennbar?                                    |
| ------------------------ | -------------------------------------------------------- |
| AP2 ist gefährdet        | teilweise — "Freigabe offen" steht in den Notizen        |
| AP3 ist gefährdet        | teilweise — "Testsystemzugang fehlt"                     |
| AP4 hängt von AP2 ab     | **nein** — die Abhängigkeit wird behauptet, nicht belegt |
| Budgetrisiko beträgt X € | **nein** — keine Rechnung sichtbar                       |

Kernbefund: Das Zero-Shot-Ergebnis ist inhaltlich meist nicht falsch, aber nicht prüfbar. Wo die Zahl herkommt, ist nicht erkennbar.

### 3. Chain-of-Thought

```text
Welche zwei Arbeitspakete gefährden den Projekterfolg am stärksten, und welches
Budgetrisiko ergibt sich daraus?

Gehe schrittweise vor und zeige die Zwischenschritte, bevor du das Ergebnis nennst:
1. Status und Fortschritt aller Arbeitspakete auflisten
2. Abhängigkeiten zwischen den Arbeitspaketen benennen
3. Mit der Risikoliste abgleichen
4. Budgetverbrauch gegen Gesamtfortschritt halten
5. Erst dann die zwei kritischen Arbeitspakete und das Budgetrisiko nennen

Grundlage sind ausschließlich die beigefügten Projektnotizen.
```

Erwartetes Ergebnis: fünf sichtbare Zwischenschritte, dann das Ergebnis. Typisch werden AP2 (blockiert AP4) und AP3 (kann nicht abgeschlossen werden) genannt.

### 4. Zwischenschritte einzeln geprüft

| Schritt | Aussage im Ergebnis                                     | Beleg in den Notizen                        | Bewertung         |
| ------- | ------------------------------------------------------- | ------------------------------------------- | ----------------- |
| 1       | AP1 100 %, AP2 70 %, AP3 35 %, AP4 0 %, AP5 0 %         | Tabelle "Stand der Arbeitspakete"           | belegt            |
| 2       | AP4 hängt an der AP2-Freigabe                           | Risiko R1 beschreibt genau das              | belegt            |
| 3       | R1 Eintritt hoch, R2 Eintritt mittel                    | Risikotabelle                               | belegt            |
| 4       | 38,9 % Budget verbraucht bei ca. 41 % Gesamtfortschritt | 71.500 € / 184.000 €; Fortschritt gemittelt | **prüfpflichtig** |
| 5       | konkretes Budgetrisiko in Euro                          | —                                           | **nicht belegt**  |

Der lehrreiche Punkt liegt bei Schritt 4 und 5. Der Gesamtfortschritt ist in den Notizen nicht ausgewiesen; er entsteht erst durch eine Mittelung über fünf Arbeitspakete, die unterschiedlich groß sind. Diese Mittelung ist eine Annahme, keine Tatsache. Ein daraus abgeleiteter Euro-Betrag ist erfunden.

Ohne Chain-of-Thought wäre genau dieser Sprung unsichtbar geblieben.

### 5. ReAct

```text
Beantworte die Frage im folgenden Muster und mache jeden Schritt sichtbar:

Gedanke:  (was als Nächstes geklärt werden muss)
Handlung: (welche Stelle der Projektnotizen dafür herangezogen wird)
Ergebnis: (was dort tatsächlich steht)

Wiederhole das, bis die Frage beantwortet werden kann. Wenn eine benötigte Angabe in
den Notizen fehlt, halte das ausdrücklich als Lücke fest, statt sie zu schätzen.

Frage: Welche zwei Arbeitspakete gefährden den Projekterfolg am stärksten, und welches
Budgetrisiko ergibt sich daraus?
```

Erwarteter Verlauf: drei bis fünf Gedanke/Handlung/Ergebnis-Runden. Der entscheidende Unterschied zu Chain-of-Thought: Die ausdrückliche Lückenanweisung führt dazu, dass die fehlende Budgetgrundlage als Lücke benannt statt geschätzt wird.

### 6. Vergleich

| Kriterium        | Zero-Shot            | Chain-of-Thought                     | ReAct                                         |
| ---------------- | -------------------- | ------------------------------------ | --------------------------------------------- |
| Ergebnisqualität | inhaltlich brauchbar | gleich bis besser                    | gleich, mit benannten Lücken                  |
| Prüfbarkeit      | gering               | hoch — jeder Schritt einzeln prüfbar | hoch, zusätzlich mit Quellenstelle je Schritt |
| Länge            | kurz                 | 2–3× länger                          | 2–4× länger                                   |
| Aufwand          | gering               | mittel (Schrittfolge formulieren)    | höher (Muster und Lückenregel formulieren)    |

### 7. Entscheidung

Für diese Frage passt **Chain-of-Thought**, ergänzt um die Lückenanweisung aus dem ReAct-Prompt.

Begründung: Die Frage ist mehrstufig und die Quelle liegt vollständig vor — es muss nichts zusätzlich nachgeschlagen werden, was ReActs Stärke wäre. Entscheidend ist die Prüfbarkeit, weil das Ergebnis in den Lenkungsausschuss geht. Die sichtbaren Zwischenschritte machen den nicht belegten Budgetsprung erkennbar; genau das leistet Zero-Shot nicht.

Nicht ausreichend: "Chain-of-Thought las sich am besten." Der Maßstab ist Prüfbarkeit gegen Aufwand.

## Häufige Fehler

| Fehler                                                     | Korrektur                                                                         |
| ---------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Sichtbare Zwischenschritte als Korrektheitsbeweis gewertet | Auch ein falscher Weg wird flüssig dargestellt; jeder Schritt braucht einen Beleg |
| Gemittelter Gesamtfortschritt als Tatsache übernommen      | Die Mittelung über ungleich große Arbeitspakete ist eine Annahme                  |
| ReAct und Chain-of-Thought gleichgesetzt                   | CoT denkt durch, ReAct wechselt zwischen Überlegen und Nachsehen                  |
| Zero-Shot als "falsch" bewertet                            | Das Ergebnis ist meist richtig, aber unbelegt — das ist ein anderer Mangel        |

## Checkpoint

- Drei zugeordnete Ergebnisse liegen vor.
- Mindestens ein Zwischenschritt wurde einzeln gegen die Notizen geprüft; erwartet wird "nicht belegt" beim Budgetrisiko.
- Die Vergleichstabelle ist vollständig.

## Erweiterung

Few-Shot mit zwei Beispieleinträgen:

| Verglichen mit Chain-of-Thought | Beobachtung                                                      |
| ------------------------------- | ---------------------------------------------------------------- |
| Form                            | deutlich einheitlicher, alle Einträge im vorgegebenen Dreiteiler |
| Länge                           | kürzer, weil die Zwischenschritte entfallen                      |
| Prüfbarkeit                     | **geringer** — die Herleitung ist wieder unsichtbar              |

Schlussfolgerung: Few-Shot und Chain-of-Thought lösen verschiedene Probleme. Few-Shot vereinheitlicht die Form, Chain-of-Thought macht den Weg prüfbar. Für ein Gremiendokument lassen sie sich kombinieren: erst mit CoT herleiten und prüfen, dann das geprüfte Ergebnis per Few-Shot in die Zielform bringen.
