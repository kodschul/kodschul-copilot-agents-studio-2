# Wie Microsoft 365 Copilot funktioniert

Hintergrundmaterial zu Modul 1. Erklärt, woher Copilot seine Antworten nimmt und warum dieselbe Frage unterschiedliche Antworten liefern kann.

## Der Weg einer Anfrage

```
Prompt
  → Copilot sucht relevanten Kontext in Microsoft 365 (Grounding)
  → nur Inhalte, für die die anfragende Person berechtigt ist
  → Prompt + gefundener Kontext gehen an das Sprachmodell
  → Antwort wird erzeugt und zurück in die App gegeben
```

## Grounding: die Datengrundlage

| Aspekt         | Verhalten                                                                          |
| -------------- | ---------------------------------------------------------------------------------- |
| Quelle         | Inhalte in Microsoft 365: E-Mails, Dateien, Chats, Kalender, ggf. Web              |
| Berechtigungen | ausschließlich Inhalte, die die anfragende Person ohnehin sehen darf               |
| Suchverfahren  | semantisch, nicht nur Stichwort — inhaltlich passende Treffer statt Wortgleichheit |
| Relevanz       | Sortierung u. a. nach Zusammenarbeit, Aktualität und Dateityp                      |

Copilot vergibt keine neuen Berechtigungen. Es macht bestehende Berechtigungen nur sichtbarer und schneller nutzbar — der Grund, warum Berechtigungen und Wissensquellen bei Agenten (Lab 7.9) sorgfältig geprüft werden müssen.

## Warum derselbe Prompt unterschiedliche Antworten liefert

| Ursache               | Wirkung                                                                   |
| --------------------- | ------------------------------------------------------------------------- |
| Kontextabhängigkeit   | Jede Person hat andere Dateien, Mails und Rollen im Zugriff               |
| Stochastisches Modell | Die Antwort wird über Wahrscheinlichkeiten erzeugt, nicht deterministisch |
| Personalisierung      | Benutzerdefinierte Anweisungen und gespeicherte Präferenzen wirken mit    |
| Zeitpunkt             | Neue Dokumente und Mails verändern den verfügbaren Kontext                |

> **Merksatz:** Zwei identische Prompts können zwei unterschiedliche Antworten liefern. Wer reproduzierbare Ergebnisse braucht, prüft das Ergebnis, nicht den Prompt.

## Konsequenzen für die Praxis

- Ergebnisse vergleichen, wenn mehrere Personen an derselben Aufgabe arbeiten.
- Zahlen, Namen und Fristen immer gegen die Quelle prüfen.
- Ein gutes Ergebnis ist kein Beweis, dass derselbe Prompt morgen dasselbe liefert.
- Fehlender Kontext erzeugt generische Antworten, keine Fehlermeldung.

Angewendet in Lab 1.3 (Chat vs. Premium) und Lab 1.4 (erster Prompt); vertieft in Lab 7.9 (Agent-Governance und Oversharing).
