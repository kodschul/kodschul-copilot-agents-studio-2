# The Nextise Agentic Way — das große Ziel dieses Kurses

Kickoff-Material für die Vorstellungsrunde am Morgen von Tag 1, vor dem ersten Copilot-Klick.
Zum Zeigen auf dem Board: die drei Blöcke unten (Ziel, Prinzip, Drei-Assistenten-Kette) einzeln
aufdecken und mit dem eigenen Beispiel aus Modul 7 verknüpfen.

- Dieser Kurs ist keine Klick-Schulung für einzelne Copilot-Funktionen.
- Das eigentliche Ziel: KI nutzen, um KI zu bauen — statt Aufgaben weiter selbst zu lösen und
  KI nur am Rand einzusetzen.
- Angewendet wird das konkret in Modul 7: Tag 1 endet mit der Frage "Was ist ein Custom Agent?", an Tag 2 entsteht daraus ein eigener Support-Agent in Copilot Studio — gebaut mit Skills.

## Der Denkwechsel (fürs Board)

```
KI kann bereits fast alles.
  → Die eigene Rolle ist nicht mehr: ihr beibringen, WIE eine Aufgabe zu lösen ist.
  → Die eigene Rolle ist: sie führen, damit sie das RICHTIGE tut.
```

- Wer KI direkt eine Lösung beschreibt ("bau mir ein Tool, das X macht"), überträgt ein oft
  noch unausgereiftes eigenes Lösungsbild.
- Ist das Problemverständnis an dieser Stelle falsch, baut die KI zuverlässig die falsche
  Lösung für das falsche Problem.

## Prinzip: Problem vor Lösung trennen

```
1. Problem verstehen   →   2. Lösung konzipieren   →   3. Lösung bauen
   (unabhängig von            (Konzept, Bausteine)         (konkrete Umsetzung)
    jeder Lösungsidee)
```

- **1. Problem verstehen** — Was ist das eigentliche Problem, unabhängig von jeder
  Lösungsidee? Zeitpunkt: bevor über eine Lösung gesprochen wird.
- **2. Lösung konzipieren** — Welches Konzept, welche Bausteine lösen dieses
  Problem? Zeitpunkt: erst wenn das Problem klar ist.
- **3. Lösung bauen** — Wie wird das Konzept konkret umgesetzt? Zeitpunkt: erst
  wenn Konzept und Bausteine feststehen.

> **Merksatz (fürs Board):** Der Mensch bleibt in jedem Schritt "in the loop" — er entscheidet,
> welches Problem gelöst wird, welches Konzept überzeugt und welcher Baustein gebraucht wird.
> Genau das unterscheidet Agentic Thinking von "KI, bau mir einen Agenten".

## Die Drei-Assistenten-Kette (fürs Board)

Statt eines einzigen Chat-Verlaufs für alles: drei spezialisierte Assistenten, jeder übernimmt
nur einen Schritt der Kette. Jeder Assistent bekommt den Output des vorherigen als Eingabe.

```
Problem
  →  [1] Problem-Solver              →  Use-Case-Canvas, Top-1-Empfehlung
  →  [2] Solution Architect          →  Kurzkonzept, Bausteine
  →  [3] Skill-/System-Prompt-Generator  →  System-Prompt + SKILL.md
```

- **1. Problem-Solver** — nimmt ein Problem entgegen und liefert Ideen, wie ein
  Agent es lösen könnte, inkl. Bewertung von Nutzen, Datenlage und Risiko.
  Eingabe: eine frei formulierte Problembeschreibung.
  Ausgabe: Use-Case-Canvas, Scoring, Top-1-Empfehlung.
- **2. Solution Architect** — leitet aus Problem und gewählter Idee die
  Bausteine ab: Skills, Tools, Ablauf.
  Eingabe: Problem + gewählte Idee.
  Ausgabe: Kurzkonzept, Bausteine, Übergabepaket.
- **3. Skill-/System-Prompt-Generator** — erzeugt aus Problem,
  Architektur-Übergabepaket und gewähltem Skill den fertigen System-Prompt,
  testet und verbessert iterativ.
  Eingabe: Problem + Architektur-Output + gewählter Skill.
  Ausgabe: fertiger, getesteter System-Prompt und `SKILL.md`, die in Copilot Studio
  hochgeladen werden kann (Lab 7.5).

> **Merksatz:** Jeder Assistent kennt bereits den Kontext der vorherigen Schritte und liefert
> deshalb genau das, was in diesem Moment gebraucht wird — statt eines generischen
> "baue mir alles"-Ergebnisses.

## Fazit

- Das große Ziel des Kurses: KI nutzen, um KI zu bauen, mit dem Menschen als Entscheider in
  jedem Schritt.
- Problem und Lösung werden konsequent getrennt, bevor irgendetwas gebaut wird.
- Die Drei-Assistenten-Kette (Problem-Solver → Solution Architect → Skill-Generator) ist das
  konkrete Werkzeug dafür — angewendet in Modul 7 beim Bau des Nordwind-Support-Agenten.
