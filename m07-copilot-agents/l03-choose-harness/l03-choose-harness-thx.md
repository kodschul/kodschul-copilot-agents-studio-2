---
theme: default
layout: default
---

# Lab 7.3: Welchen Weg wählen? Harness-Entscheidung

Die Harness-Wahl bestimmt, wie ein Agent denkt, welche Bausteine er nutzen kann und wie Kosten entstehen. Dieses Lab vergleicht Copilot-Chat-, Standard- und GitHub-Copilot-Harness anhand von Nordwind-Szenarien.

**Leitfragen:**

<details>
<summary>Wann reicht der Copilot-Chat-Harness aus?</summary>

Wenn ein interner Wissensfall mit klaren Quellen im Vordergrund steht und kein aufwendiger mehrstufiger Ablauf nötig ist. Dann bleibt der Aufbau schlank.

</details>

<details>
<summary>Wann lohnt sich der GitHub-Copilot-Harness trotz Credits?</summary>

Wenn ein offenes Ziel, mehrere Schritte, Dateien, Skills oder Laufzeitentscheidungen gefragt sind. Dann kompensiert die höhere Leistungsfähigkeit den Zusatzaufwand.

</details>

<details>
<summary>Was passiert bei einer falschen Harness-Wahl?</summary>

Ein zu einfacher Harness begrenzt den Anwendungsfall, ein zu mächtiger Harness überarbeitet eine eigentlich einfache Aufgabe. Beides erzeugt unnötigen Umbau, Kosten oder Friktion.

</details>

## Drei Harnesses im Vergleich

| Kriterium | Copilot-Chat-Harness | Standard-Harness | GitHub-Copilot-Harness |
| --- | --- | --- | --- |
| **Best for** | interner Wissensagent mit Unternehmensquellen | regelbasierte, vorhersagbare Abläufe | reasoning-starke, mehrstufige Aufgaben |
| **How it works** | erweitert Microsoft Copilot Chat um Wissen | Topics, Prompts und feste Pfade | nimmt ein Ziel in Prosa und plant Schritte dynamisch |
| **Recovers from problems** | kein eigener Recovery-Mechanismus hervorgehoben; primär Chat-Verhalten | Fallbacks und Pfade werden explizit modelliert | Agentic Loop: anderer Weg, delegieren oder stoppen |
| **Files** | in dieser Faktengrundlage nicht als natives Dateiarbeiten hervorgehoben | in dieser Faktengrundlage nicht als natives Dateiarbeiten hervorgehoben | erzeugt/bearbeitet Word-, Excel-, PowerPoint- und PDF-Dateien |
| **Skills & Memory** | Wissensquellen stehen im Vordergrund | Skills/Memory sind nicht der Fokus | Skills und Memory werden explizit unterstützt |
| **Publishing** | intern für Teams | vor Kursbeginn im Tenant prüfen | intern oder extern |
| **Billing** | verbrauchsbasiert oder im M365-Copilot-Lizenzumfang | bisheriges Lizenzmodell | Copilot Credits, auch beim Bauen, Testen und Evaluieren |

## Faustregel nach Aufgabengewicht

| Aufgabentyp | Passender Weg |
| --- | --- |
| eine klar abgrenzbare Wissensfrage mit stabiler Quelle | Copilot-Chat-Harness |
| wiederholbarer Prozess mit bewusst modellierten Pfaden | Standard-Harness |
| offenes Ziel mit mehreren Schritten, Dateien oder delegierten Teilaufgaben | GitHub-Copilot-Harness |

Ein mächtigerer Harness kann ein einfaches Problem überarbeiten. Das zeigt sich in mehr Latenz, mehr Credits und mehr Konfigurationsaufwand ohne echten Mehrwert.

## Agentic Loop und Nicht-Wechselbarkeit

| Begriff | Bedeutung |
| --- | --- |
| Agentic Loop | Der Agent bewertet Zwischenergebnisse und entscheidet, ob er weitermacht, einen anderen Weg versucht, delegiert oder stoppt. |
| Harness-Wahl | Der Harness wird beim Anlegen des Agenten festgelegt. Ein späterer Wechsel zwischen Standard- und GitHub-Copilot-Harness ist nicht vorgesehen. |
| Datenversprechen | Der GitHub-Copilot-Harness ist nicht der GitHub-Copilot-Dienst; Daten bleiben unter den Copilot-Studio-Zusagen zu Datenschutz, Sicherheit, Compliance und Datenresidenz. |

> **Merksatz:** Nicht der stärkste, sondern der passendste Harness gewinnt — gemessen an Problem, Aufwand, Credits und gewünschter Steuerbarkeit.

## Grenzen und Prüfpunkte

- Preview-Status, verfügbare Modelle und Kanäle vor Kursbeginn im Tenant prüfen.
- Eine FAQ kann im Chat-Harness bleiben; ein reiner Workflow-Fall kann im Standard-Harness klarer werden.
- Der GitHub-Copilot-Harness lohnt sich erst, wenn dynamische Orchestrierung, Dateien, Skills oder Memory im Szenario wirklich gebraucht werden.

## Fazit

- Die Harness-Wahl ist eine Architekturentscheidung, keine reine Geschmacksfrage.
- Task Weight hilft: kleine Wissensfälle leicht halten, offene Mehrschrittaufgaben stärker orchestrieren.
- Für Nordwind ist wichtig, ob nur FAQ beantwortet oder später auch Checklisten, Eskalationen und weitere Bausteine aufgebaut werden sollen.

Die Übung entscheidet drei Nordwind-Szenarien und leitet daraus die Empfehlung für den Nordwind Support-Agenten ab.
