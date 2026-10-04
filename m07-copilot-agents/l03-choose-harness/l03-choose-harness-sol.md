# Lab 7.3 – Lösung: Welchen Weg wählen? Harness-Entscheidung

## Aufgaben

### 1. Entscheidungsmatrix anlegen

| Szenario | Primärer Harness | Kurzbegründung |
| --- | --- | --- |
| FAQ-Antworten aus SharePoint | Copilot-Chat-Harness | Wissensfall mit interner Quelle und geringem Steuerungsbedarf |
| Onboarding-Prozess über mehrere Tools mit generierter Checkliste | GitHub-Copilot-Harness | mehrstufige Aufgabe mit Checkliste, möglicher Tool-Nutzung und wachsendem Skill-Bedarf |
| Rechnungs-gegen-Bestellung-Prüfung mit Dateien | GitHub-Copilot-Harness | genau der reasoning- und dateilastige Fall aus der Faktengrundlage |

### 2. Entscheidungen begründen

- **FAQ aus SharePoint:** passt gut zum Copilot-Chat-Harness, weil Wissen im Vordergrund steht und keine Dateioperation oder Skill-Orchestrierung nötig ist.
- **Onboarding-Prozess mit Checkliste:** passt zum GitHub-Copilot-Harness, weil aus einem offenen Ziel mehrere Schritte und ein Ergebnisartefakt entstehen.
- **Rechnungsprüfung mit Dateien:** passt klar zum GitHub-Copilot-Harness, weil Dateien nativ verarbeitet werden und Fehlerbehandlung Teil des Ablaufs ist.

### 3. Problembehandlung notieren

| Harness | Typischer Umgang mit Problemen |
| --- | --- |
| Copilot-Chat-Harness | Rückfrage oder präzisere Wissensbasis; kein eigener agentic loop hervorgehoben |
| Standard-Harness | Fallbacks und Pfade werden vorab explizit modelliert |
| GitHub-Copilot-Harness | agentic loop: anderer Weg, delegieren oder stoppen |

### 4. Ein-Satz-Empfehlung für den Nordwind Support-Agenten

Empfehlung: **Der Day-2-Ausbau des Nordwind Support-Agenten erfolgt im GitHub-Copilot-Harness, weil Skills, späterer Workflow-/Tool-Ausbau und ein wachsender Aufgabenmix über reines FAQ-Verhalten hinausgehen.**

### 5. Ehrliche Einschränkung ergänzen

Ehrlicher Zusatz: **Der reine FAQ-Teil zu VPN, Standardsoftware und Ersttag-Fragen könnte weiterhin im Copilot-Chat-Harness oder in einem streng geführten Standard-Harness bleiben.**

## Checkpoint

- Alle drei Szenarien sind sauber voneinander abgegrenzt.
- Die Nordwind-Empfehlung benennt bewusst den Ausbaupfad, nicht nur den kleinsten Startfall.
- Die Einschränkung für den FAQ-Anteil ist offen dokumentiert.

## Abschlusskriterien

- Die Entscheidungsmatrix deckt Wissen, Prozess und Dateiarbeit ab.
- Die Empfehlung passt zur späteren Arbeit mit Skills in Lab 7.5.

## Erweiterung

Ein zusätzliches eigenes Szenario ist tragfähig, wenn klar erkennbar bleibt, ob Dateiarbeit, feste Pfade oder reine Wissenssuche den Ausschlag geben.

## Fallback

Auch ohne Live-Tenant bleibt die Architekturentscheidung belastbar, solange die Begründung direkt aus den Kriterien der Faktengrundlage abgeleitet ist.
