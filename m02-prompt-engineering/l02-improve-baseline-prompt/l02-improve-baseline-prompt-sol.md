# Lab 2.2 – Lösung: Baseline-Prompt in Runden verbessern

## Aufgaben

### 1. Baseline

```text
Schreib was zur Eskalation.
```

Erwartetes Ergebnis: ein allgemeiner Text darüber, wie Eskalationen im Projektmanagement funktionieren — Eskalationsstufen, Kommunikationsregeln, Konfliktvermeidung. Kein Bezug zu AP2, zu den Stadtwerken oder zum Freigabestau.

Diagnose: in sich schlüssig, aber am Bedarf vorbei. Das ist das Muster eines Prompt-Problems, nicht eines Modellproblems.

### 2.–4. Optimierungstabelle

| Runde | Beobachtete Störung                                       | Punkt      | Ergänzte Angabe                                                                                                         | Wirkung                                                          | Prompt oder Quelle |
| ----- | --------------------------------------------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- | ------------------ |
| 1     | Allgemeiner Lehrtext, kein Projektbezug                   | 2 Kontext  | "Projekt Hafenmodernisierung, Kunde Stadtwerke Nordhafen, Freigabe AP2 offen seit 11.09.2026, Projektnotizen beigefügt" | Text nennt jetzt AP2 und den Freigabestau, bleibt aber erzählend | Prompt             |
| 2     | Text beschreibt die Lage, liefert keine Argumentation     | 3 Fokus    | "Ziel: eine Argumentationsgrundlage für das Eskalationsgespräch, die die Konsequenz des Verzugs belegt"                 | Auswirkung auf AP4 und die Rollout-Planung wird benannt          | Prompt             |
| 3     | Einträge uneinheitlich, kein verwendbares Gesprächsgerüst | 4 Struktur | "Drei Abschnitte: Sachstand, Auswirkung, Bitte. Je maximal drei Stichpunkte."                                           | Ergebnis ist als Gesprächsleitfaden direkt nutzbar               | Prompt             |
| —     | Kein Freigabe-Zieltermin nennbar                          | —          | keine Ergänzung möglich                                                                                                 | bleibt offen                                                     | **Quelle**         |

Der Quellenbefund ist der Kernpunkt: Ein konkreter Zieltermin für die Freigabe steht in den Projektnotizen nicht. Jede Prompt-Ergänzung, die einen Termin verlangt, erzeugt einen erfundenen Termin. Das ist nicht durch Optimierung lösbar.

Finaler Prompt:

```text
Als Projektleiterin bei Nordwind Consulting: Erstelle eine Argumentationsgrundlage für das
Eskalationsgespräch mit dem Fachbereich Betrieb der Stadtwerke Nordhafen.

Kontext: Projekt Hafenmodernisierung. Die Freigabe des Anforderungskatalogs (AP2) steht seit
dem 11.09.2026 aus. Grundlage sind die beigefügten Projektnotizen.

Ziel: Die Konsequenz des Verzugs für den weiteren Projektverlauf belegen.

Struktur: drei Abschnitte – Sachstand, Auswirkung, Bitte. Je maximal drei Stichpunkte.
Sachlich, ohne Schuldzuweisung.
```

### 5. Abbruchentscheidung

Abbruch nach Runde 3, begründet mit: _"Die verbliebene Lücke (Zieltermin) ist ein Quellenproblem. Weitere Runden können sie nicht schließen, sondern nur einen Termin erfinden."_

Nicht ausreichend: "Das Ergebnis ist jetzt gut genug." Die Theorie nennt drei verwendbare Kriterien: zwei Runden ohne Verbesserung, Information nicht in der Quelle, Nacharbeit schneller als Iteration.

Manuelle Nacharbeit: Der Zieltermin wird von der Projektleitung eingesetzt, nicht von Copilot.

## Gültige Alternativen

Die Reihenfolge der Runden ist nicht festgelegt. Wer in Runde 1 zuerst den Fokus (Punkt 3) statt des Kontexts (Punkt 2) ergänzt, kommt zu einem vergleichbaren Ergebnis. Entscheidend ist:

- pro Runde genau eine Angabe,
- jede Änderung ist einem Checklistenpunkt zugeordnet,
- die Wirkung ist beobachtet und notiert.

## Häufige Fehler

| Fehler                                                 | Korrektur                                                                     |
| ------------------------------------------------------ | ----------------------------------------------------------------------------- |
| Runde 1 ergänzt Kontext, Fokus und Format gleichzeitig | Wirkung ist dann nicht zuzuordnen; das Schema verliert seinen Zweck           |
| Erfundener Freigabetermin wird übersehen               | Jede Datumsangabe gegen die Projektnotizen prüfen                             |
| Fehlender Termin wird als Prompt-Problem behandelt     | Prüfen, ob die Information in der Quelle steht, bevor der Prompt ergänzt wird |
| Abbruch ohne Kriterium                                 | Eines der drei Abbruchkriterien benennen                                      |

## Checkpoint

- Drei Runden, je genau eine Angabe, vollständig dokumentiert.
- Mindestens eine Störung ist als Quellenproblem klassifiziert (erwartet: der Zieltermin).
- Die Abbruchentscheidung nennt ein Kriterium aus der Theorie.

## Erweiterung

Erwartete Beobachtung beim Partnerdurchlauf:

| Bleibt gleich                                   | Weicht ab                                      |
| ----------------------------------------------- | ---------------------------------------------- |
| Drei Abschnitte, Stichpunktzahl, sachlicher Ton | Wortwahl, Reihenfolge innerhalb der Abschnitte |
| Benannte Auswirkung auf AP4                     | Gewichtung der drei Sachstandspunkte           |

Zusätzlich möglich: Hat die Partnerin oder der Partner Zugriff auf andere Dokumente zum Projekt, können zusätzliche Details auftauchen. Das ist kein Fehler, sondern der Grounding-Effekt aus Modul 1 — jede Person sieht einen anderen Kontext.
