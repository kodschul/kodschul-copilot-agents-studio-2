# Lab 3.2: Pitchdeck per Human-in-the-Loop

**Leitfragen:**

<details>
<summary>Was gewinnt man dadurch, das Inhaltsverzeichnis vorher mit Copilot zu klären?</summary>

Streichungen und Gewichtung passieren, bevor Text entsteht. Korrekturen an einer Gliederungszeile sind billiger als Korrekturen an ausformulierten Folien.

</details>

<details>
<summary>An welcher Stelle dieses Ablaufs entscheidet der Mensch über die Kernbotschaft?</summary>

Bereits in Lab 2.4, vor jeder Copilot-Anfrage. Hier wird die bereits getroffene Entscheidung genutzt, nicht neu getroffen.

</details>

<details>
<summary>Wo bleibt manuelle Nacharbeit unvermeidbar?</summary>

Bei fehlenden Belegen (siehe die in Lab 2.4 als "nicht belegt" markierten Folien) und bei der visuellen Feinjustierung von Layout und Bildmaterial.

</details>

- Die HITL-Gliederung aus Modul 2 wird jetzt erstmals zu einem echten Artefakt.
- Schritt 4 (Scaffold) arbeitet auf einem bereits geprüften Gerüst, statt bei null zu beginnen.

## Vom Gerüst zur Folie

```
HITL-Gliederung (Lab 2.4)
  → je Folie: Kernaussage + Belegstatus liegen bereits vor
  → Copilot erzeugt Folieninhalt je Abschnitt, nicht das ganze Deck in einem Zug
  → jede Folie einzeln gegen die Kernaussage geprüft
  → nicht belegte Folien bleiben als Platzhalter markiert
```

Der Unterschied zum One-Shot-Ansatz: Es wird nicht "erstelle mir eine Präsentation" verlangt, sondern je Folie ein eng geführter Auftrag mit der bereits feststehenden Kernaussage.

**So findet man den Copilot-Bereich:** in PowerPoint Desktop über das Copilot-Symbol im Menüband, dort den Folienauftrag im Prompt-Feld eingeben.

> **Merksatz:** Ein Scaffold-Auftrag pro Folie ist kein Mehraufwand — er verhindert, dass eine schwache Folie das ganze Deck nach unten zieht.

## Folienauftrag: Aufbau

| Bestandteil | Quelle                                                    |
| ----------- | --------------------------------------------------------- |
| Kernaussage | aus der HITL-Gliederung, unverändert                      |
| Belegstatus | steuert, ob Fakten oder ein Platzhalter entstehen         |
| Format      | Foliendichte: max. 4 Bullet-Points, keine Fließtextblöcke |
| Sprechnotiz | separat anfordern, nicht auf der Folie selbst             |

## Umgang mit unbelegten Folien

| Belegstatus  | Auftrag an Copilot                                                                   |
| ------------ | ------------------------------------------------------------------------------------ |
| belegt       | Folie mit den tatsächlichen Werten aus den Notizen erzeugen                          |
| nicht belegt | Folie als Platzhalter mit Gliederungstitel erzeugen, keine erfundenen Werte einfügen |

Eine nicht belegte Folie erhält ausdrücklich **keinen** plausiblen Fülltext. Ein Platzhalter ist ehrlich, eine erfundene Zahl ist ein Risiko im Kundentermin.

## Grenzen

- Bildmaterial, Diagramme und Layout-Feinschliff bleiben manuelle Aufgabe.
- Sprechnotizen ersetzen keine Vortragsvorbereitung; sie sind ein Gerüst, kein Skript.
- Bei mehr als etwa zehn Folien wird der Folie-für-Folie-Ansatz mühsam; ab dieser Größe lohnt ein zusammenfassender Lauf mit anschließender Einzelprüfung.

## Fazit

- Die Kernaussage aus der HITL-Gliederung steuert jede Folie einzeln, statt einem Gesamtprompt zu vertrauen.
- Unbelegte Folien bleiben Platzhalter, nie ein plausibel klingender Fülltext.
- Sprechnotizen und Layout sind eigene Aufgaben, die Copilot vorbereitet, aber nicht abschließt.

In der Übung entsteht das Pitchdeck aus der eigenen HITL-Gliederung, Folie für Folie geprüft.
