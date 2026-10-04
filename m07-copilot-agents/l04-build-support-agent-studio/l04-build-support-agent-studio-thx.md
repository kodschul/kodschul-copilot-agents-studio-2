---
theme: default
layout: default
---

# Lab 7.4: Support-Agent in Copilot Studio (GitHub-Copilot-Harness)

Der GitHub-Copilot-Harness baut Agenten natürlichsprachlich und komponentenbasiert statt über fest verdrahtete Topics. Dieses Lab überträgt den Nordwind Support-Agenten aus Lab 7.2 in Copilot Studio und macht Unterschiede bei Steuerbarkeit, Aufwand und Credits sichtbar.

**Leitfragen:**

<details>
<summary>Was ersetzt die Beschreibung in Prosa gegenüber Topics?</summary>

Im GitHub-Copilot-Harness beschreibt Prosa Ziel, Grenzen und gewünschtes Verhalten. Die Laufzeit plant daraus dynamisch Schritte, statt jeden Gesprächspfad als Topic vorzugeben.

</details>

<details>
<summary>Wie lässt sich in Preview erkennen, worauf eine Antwort beruht?</summary>

Entscheidend ist, ob der Antwortbezug auf Instruktionen, Wissensquelle oder Eskalationsregel nachvollziehbar bleibt. Welche Sichtbarkeit der Tenant zeigt, muss vor Kursbeginn geprüft werden.

</details>

<details>
<summary>Was verbraucht Credits?</summary>

Im GitHub-Copilot-Harness entstehen Copilot-Credits nicht nur im späteren Betrieb, sondern bereits beim Bauen, Testen und Evaluieren. Auch deshalb lohnt sich dieser Weg nur für passende Aufgaben.

</details>

## Build-Tab: die Agentenbausteine

| Komponente | Zweck | Nordwind-Bezug |
| --- | --- | --- |
| Instructions | Rolle, Ton, Grenzen, Eskalation | System-Prompt aus Lab 7.2 |
| Knowledge | Quellen und Memory | IT-Richtlinie, Onboarding-Leitfaden |
| Tools | Aktionen und externe Funktionen | in diesem Lab noch leer; Ausbau folgt später |
| Skills | wiederverwendbare Aufgabenpakete | folgen erst in Lab 7.5 |
| Model | wählt das verfügbare Modell für den Agenten | konkrete Optionen vor Kursbeginn im Tenant prüfen |
| Connected agents | Delegation an Spezialisten | in diesem Lab noch nicht genutzt |
| Memory | merkt Details aus Interaktionen | Preview-Status vor Kursbeginn prüfen |

## Die Arbeits-Tabs im Überblick

| Tab | Wofür er dient |
| --- | --- |
| Build | Agent konfigurieren und Bausteine zusammensetzen |
| Preview | Fragen stellen und das Verhalten interaktiv prüfen |
| Evaluate | Testsets und Qualitätsmessung vorbereiten |
| Monitor | Gesundheit, Sessions, Reaktionen und Credit-Nutzung beobachten |

## Natürlichsprachlich statt Topic-first

| Standard-Harness / Topics | GitHub-Copilot-Harness |
| --- | --- |
| Gesprächspfade werden explizit gebaut | Ziel und Grenzen werden in Prosa beschrieben |
| Recovery entsteht über vorab modellierte Fallbacks | Recovery entsteht über agentic loop und Laufzeitentscheidung |
| Fokus auf Vorhersagbarkeit | Fokus auf reasoning-starke, mehrstufige Aufgaben |

Der GitHub-Copilot-Harness ist dabei **nicht** der GitHub-Copilot-Dienst. Daten bleiben unter den Copilot-Studio-Zusagen; dennoch sollten Harness-Zugang, Preview-Status und verfügbare Modelle **vor Kursbeginn im Tenant geprüft** werden.

## Szenariofortsetzung für Nordwind

Der Nordwind Support-Agent kennt bereits Zweck, Eskalationsregel und zwei Wissensquellen. Im Studio-Bau werden jetzt dieselben Inhalte in die Build-Komponenten übersetzt, um die spätere Skill-, Workflow- und Evaluate-Strecke vorzubereiten.

> **Merksatz:** Im GitHub-Copilot-Harness wird nicht jeder Pfad gebaut, sondern Ziel, Grenzen und Bausteine werden so beschrieben, dass der Agent den passenden Weg finden kann.

## Grenzen in diesem Lab

- Skills werden erst im nächsten Lab hinzugefügt, damit Instructions und Knowledge separat beurteilbar bleiben.
- Copilot Credits fallen schon beim Erstellen, Testen und Vergleichen an.
- Die natürliche Erstellung und manche Build-Optionen sind tenant- und preview-abhängig.

## Fazit

- Der GitHub-Copilot-Harness verschiebt die Arbeit von Topics auf Komponenten, Prosa und Tests.
- Preview, Evaluate und Monitor gehören schon zum Bauprozess, nicht erst zum späteren Betrieb.
- Der Vergleich mit dem Chat-Agenten zeigt, ob die höhere Steuerbarkeit den Zusatzaufwand rechtfertigt.

Die Übung baut den Nordwind Support-Agenten im GitHub-Copilot-Harness, testet ihn in Preview und vergleicht ihn mit der Chat-Version aus Lab 7.2.
