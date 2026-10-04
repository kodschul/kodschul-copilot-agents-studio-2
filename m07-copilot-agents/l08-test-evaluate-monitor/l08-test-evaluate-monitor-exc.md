# Lab 7.8 – Übung: Testset anlegen und Evaluation wiederholen

**Ändert die Nordwind-Projektbasis?** Ja — der Nordwind Support-Agent erhält eine erste, dokumentierte Qualitätsbasis für Preview, Evaluate und spätere Monitor-Nutzung.

## Ausgangslage

Der Agent enthält bereits Skills sowie mindestens einen Tool- oder Delegationspfad. Vor einer Freigabe soll die Antwortqualität systematisch geprüft werden.

## Aufgaben

1. Ein Testset mit genau fünf Nordwind-Fragen anlegen: drei Normalfälle und zwei Grenzfälle.
2. Für jede Frage das erwartete Verhalten notieren: direkte Antwort, Skill-Nutzung, Workflow-Aufruf, Delegation oder Eskalation.
3. Die Evaluation ausführen und die schwächste Antwort identifizieren.
4. Nur den kleinsten sinnvollen Hebel anpassen: Skill-Beschreibung, Skill-Body oder globale Instructions.
5. Dieselbe Evaluation erneut ausführen und dokumentieren, ob die schwächste Antwort besser wurde, ohne andere Fälle zu verschlechtern.
6. Notieren, welche Erkenntnis eher in Preview sichtbar wird und welche erst in Evaluate oder später in Monitor.

## Checkpoint

- Das Testset enthält sowohl einen Out-of-Scope-Fall als auch eine Anfrage nach Gehaltsdaten.
- Zwischen Lauf 1 und Lauf 2 wurde genau ein gezielter Hebel verändert.
- Die Verbesserung ist nicht nur behauptet, sondern am Testfall dokumentiert.

## Abschlusskriterien

- Ein vollständiges Fünf-Fragen-Testset mit Erwartung liegt vor.
- Zwei Evaluationsläufe sind dokumentiert und die Anpassung ist begründet.

## Erweiterung

Eine sechste Frage ergänzen, die bewusst einen unnötigen Tool- oder Delegationsaufruf provoziert, und prüfen, ob der Agent trotzdem einfach antwortet.

## Fallback

Ohne Evaluate-Zugang: den Trainer-Demo-Lauf beobachten und die fünf Fragen manuell mit einer kleinen Bewertungsmatrix prüfen. Einschränkung: kein echter Testset-Vergleich im Tool.
