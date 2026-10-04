# Lab 1.1 – Lösung: Eigene Anwendungsfälle einordnen

Diese Übung hat individuelle Ergebnisse. Die Lösung liefert den Bewertungsmaßstab und ein durchgerechnetes Referenzbeispiel.

## Aufgaben

### 1.–2. Aufgaben sammeln und Muster zuordnen

Referenzbeispiel aus dem Beratungsalltag:

| Aufgabe                                   | Heutige Dauer | Nutzenmuster  |
| ----------------------------------------- | ------------: | ------------- |
| Wöchentlicher Projektstatus an den Kunden |        45 min | Verdichten    |
| Angebotsentwurf für eine Standardleistung |        90 min | Entwerfen     |
| Interne Notiz kundentauglich machen       |        20 min | Umformulieren |
| Workshop-Notizen in eine Agenda bringen   |        30 min | Strukturieren |
| Terminbestätigung an einen Kunden         |         3 min | kein Muster   |

### 3. Prüfdauer schätzen

| Aufgabe                     |  Heute | Copilot-Entwurf | Prüfen |  Summe | Ergebnis        |
| --------------------------- | -----: | --------------: | -----: | -----: | --------------- |
| Projektstatus               | 45 min |           5 min | 15 min | 20 min | deutlich besser |
| Angebotsentwurf             | 90 min |          10 min | 35 min | 45 min | deutlich besser |
| Notiz kundentauglich machen | 20 min |           3 min |  8 min | 11 min | besser          |
| Workshop-Notizen            | 30 min |           5 min | 10 min | 15 min | besser          |
| Terminbestätigung           |  3 min |           2 min |  2 min |  4 min | schlechter      |

### 4. Sortierung

| Gruppe           | Aufgaben                                                              |
| ---------------- | --------------------------------------------------------------------- |
| lohnt sich       | Projektstatus, Angebotsentwurf, Notiz umformulieren, Workshop-Notizen |
| lohnt sich nicht | Terminbestätigung                                                     |

Entscheidungsregel: Lohnend ist eine Aufgabe, wenn **Entwurf + Prüfung** zusammen deutlich unter der heutigen Dauer liegen. Bei kurzen Texten ist das nie der Fall, weil die Prüfung eine Mindestdauer hat.

### 5. Vergleichsfall markieren

Tragfähig ist ein Vergleichsfall, wenn er wiederkehrend ist, Textcharakter hat und der Zeitvorteil aus Aufgabe 3 klar erkennbar war. Im Referenzbeispiel: der wöchentliche Projektstatus.

## Häufige Fehleinschätzungen

| Einschätzung                                 | Korrektur                                                                  |
| -------------------------------------------- | -------------------------------------------------------------------------- |
| Prüfdauer mit 0 angesetzt                    | Jedes Ergebnis wird gelesen; unter 20 % der Entwurfszeit ist unrealistisch |
| "Lohnt sich immer, es geht ja schneller"     | Bei kurzen Texten überwiegt der Prompt- und Prüfaufwand                    |
| Exakte Zahlenberichte als lohnend eingestuft | Zahlen müssen vollständig nachgerechnet werden, der Zeitvorteil entfällt   |

## Checkpoint

- Fünf Zeilen mit heutiger Dauer und geschätzter Prüfdauer liegen vor.
- Mindestens eine Aufgabe ist begründet in "lohnt sich nicht" eingeordnet.
- Der markierte Vergleichsfall ist wiederkehrend und textbasiert.

## Erweiterung

Für die Terminbestätigung: Sie wird lohnend, wenn statt einer einzelnen Bestätigung zwanzig Terminmails mit identischer Struktur anfallen. Dann kippt das Muster von "kein Muster" zu "Entwerfen" — und ab wöchentlicher Wiederholung mit fester Vorlage wird daraus der Agenten-Fall aus Lab 1.0.
