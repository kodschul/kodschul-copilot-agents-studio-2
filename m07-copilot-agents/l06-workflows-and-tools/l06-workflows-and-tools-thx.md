---
theme: default
layout: default
---

# Lab 7.6: Workflows & Tools: der Agent handelt

Der Nordwind Support-Agent soll nicht nur antworten, sondern handeln. Dieses Lab zeigt, wann ein Workflow das richtige Werkzeug ist und wie daraus ein Tool für den Agenten wird.

**Leitfragen:**

<details>
<summary>Was unterscheidet eine Automatisierung von einem Agenten?</summary>

Eine Automatisierung führt einen festen Ablauf aus. Ein Agent bewertet variierende Anfragen und entscheidet, ob und wann eine Automatisierung gebraucht wird.

</details>

<details>
<summary>Woran erkennt der Agent, wann er einen Workflow aufruft?</summary>

Der Workflow ist als Tool beschrieben. Der Agent entscheidet anhand der Anfrage und der Tool-Beschreibung, ob genau dieser Ablauf gebraucht wird.

</details>

<details>
<summary>Wo gehört eine menschliche Freigabe hin?</summary>

Vor sensible, irreversible oder kostenrelevante Schritte, nicht erst danach.

</details>

- Workflows sind der deterministische Teil im GitHub-Copilot-Harness.
- Der Agent bleibt adaptiv und ruft Workflows nur dann auf, wenn der feste Ablauf wirklich passt.

## Begriffe im Vergleich

| Begriff | Kerngedanke | Typischer Einsatz |
| --- | --- | --- |
| Automatisierung | gleicher Trigger, gleiche Aktionskette | Ticket anlegen, Nachricht versenden, Datensatz schreiben |
| Workflow | Trigger + Aktionen + Ergebnis | Cloud-Flow, Genehmigung, strukturierter Übergabeschritt |
| Agent | interpretiert die Anfrage und wählt den passenden nächsten Schritt | Support-Agent, der antwortet oder einen Workflow als Tool nutzt |

**Faustregel:** Bleibt der Ablauf immer gleich, gehört er in einen Workflow. Variieren Anfragen, entscheidet ein Agent und ruft bei Bedarf den Workflow als Tool auf.

## Workflow-Anatomie

| Baustein | Rolle |
| --- | --- |
| Trigger | startet den Ablauf |
| Aktionen | erzeugen Daten, rufen Dienste auf oder fragen Menschen um Freigabe |
| KI-Aktionen | generieren, klassifizieren oder formulieren Inhalte |
| Human in the loop | holt Bestätigung oder fehlende Angaben ein |
| Konnektoren / Built-in Tools | verbinden Dienste oder steuern Datenlogik |

## Wann ein Workflow zum Tool wird

Ein Workflow mit dem Trigger **„When an agent calls the flow“** kann dem Agenten als Tool hinzugefügt werden. Damit bleibt der Ablauf deterministisch, während der Agent nur den Aufruf entscheidet.

> **Merksatz:** Der Agent entscheidet **ob**, der Workflow definiert **wie**.

## Nordwind-Szenario

Eine unbeantwortbare Support-Anfrage soll nicht in einer Textantwort enden. Der Agent soll ein strukturiertes Support-Ticket anlegen und das Team benachrichtigen.

## Zwei Automatisierungswelten kurz eingeordnet

- **Power Automate Cloud Flows:** Cloud-zu-Cloud-Abläufe zwischen Microsoft-365-Diensten, Datenspeichern und Konnektoren.
- **Power Automate Desktop:** RPA für Altsysteme oder Desktop-Oberflächen ohne API; im Kurs nur zur Einordnung, nicht als Bauziel.

## Kapazität und Kosten

Jede Workflow-Aktion verbraucht Copilot-Studio-Kapazität. Ist die vorausbezahlte Kapazität einer Umgebung aufgebraucht, werden neue Runs blockiert; laufende Runs enden regulär.

## Grenzen

- Ein Workflow ersetzt keine unklare Agentenlogik; schlechte Tool-Beschreibungen führen zu falschen Aufrufen.
- Sensible Schritte bleiben freigabepflichtig, auch wenn der Ablauf technisch automatisierbar ist.
- Teams- oder SharePoint-Ziele hängen von der freigegebenen Umgebung ab.

## Fazit

- Workflows bilden feste Abläufe mit Trigger und Aktionen ab.
- Der Trigger „When an agent calls the flow“ macht einen Workflow für den Agenten nutzbar.
- Human in the loop gehört vor riskante Schritte, nicht als nachträgliche Kontrolle.

Die Übung baut den Workflow `Support-Ticket anlegen` und bindet ihn als Tool an den Nordwind Support-Agenten.
