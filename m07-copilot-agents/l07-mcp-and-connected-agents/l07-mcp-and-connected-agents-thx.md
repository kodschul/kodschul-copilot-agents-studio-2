---
theme: default
layout: default
---

# Lab 7.7: MCP & Connected Agents: Integration mit anderen Tools

Der Nordwind Support-Agent soll nicht alles selbst wissen. Dieses Lab zeigt zwei Erweiterungen: externe Tool-Quellen über MCP und Delegation an einen zweiten Spezialisten-Agenten.

**Leitfragen:**

<details>
<summary>Was unterscheidet einen Konnektor von einem MCP-Server?</summary>

Ein Konnektor bindet einen bekannten Dienst mit festen Aktionen an. Ein MCP-Server stellt über einen offenen Standard eigene Tools oder Daten bereit und braucht deshalb eine klare Betreiber- und Rechteprüfung.

</details>

<details>
<summary>Wann ist ein Connected Agent sinnvoller als ein Skill?</summary>

Wenn ein zweiter, eigenständig gepflegter Spezialist mit eigenem Fokus gebraucht wird, nicht nur ein kleiner Teilauftrag innerhalb desselben Agenten.

</details>

<details>
<summary>Was ist die zusätzliche Zugriffsfläche?</summary>

Jeder MCP-Server und jeder verbundene Agent erweitert Datenzugriff, Verhalten und Fehlermöglichkeiten des Gesamtsystems und braucht deshalb dieselbe Governance-Aufmerksamkeit wie ein Konnektor.

</details>

- MCP erweitert den Agenten um externe Tools oder Datenquellen.
- Connected Agents erweitern ihn um Delegation an einen zweiten Agenten mit eigenem Spezialgebiet.

## Integrationsformen im Vergleich

| Form | Kernidee | Gute Wahl, wenn ... |
| --- | --- | --- |
| Konnektor | fester Zugriff auf einen Dienst | die Aktion klar ist und der Dienst schon freigegeben ist |
| MCP-Server | offene Standard-Schnittstelle für Tools oder Daten | ein externer Tool-Katalog oder Dokumentationszugriff gebraucht wird |
| Connected Agent | Delegation an einen Spezialisten | ein zweiter Agent mit eigener Rolle und eigenen Regeln besser passt |

## MCP als Tool-Quelle

Ein MCP-Server wird im Kurs als zusätzliche Tool-Quelle verstanden: Der Agent kann darüber externe Funktionen oder Dokumentationswissen erreichen, ohne dass der Skill selbst die Logik nachbildet.

**Klickpfad vor Kursbeginn im Tenant verifizieren.** Die konkrete UI für MCP-Server wurde in der Faktengrundlage nicht im Detail validiert.

## Connected Agents im GitHub-Copilot-Harness

Connected Agents sind Delegationsziele im Build-Bereich. Der GitHub-Copilot-Harness hält dabei den gemeinsamen Kontext zusammen, während der Hauptagent Teilaufgaben an einen Spezialisten übergibt.

> **Merksatz:** Skill = Teilaufgabe im selben Agenten. Connected Agent = eigener Spezialist mit eigener Verantwortung.

## Sub-Agent-Muster für Nordwind

| Rolle | Aufgabe |
| --- | --- |
| Nordwind Support-Agent | triagiert Support- und Onboarding-Anfragen |
| Nordwind HR-Onboarding-Agent | übernimmt HR-nahe Onboarding-Fälle und personenbezogene Weiterleitungen |

## Risikotabelle: zusätzliche Zugriffsflächen

| Erweiterung | Zusätzliche Fläche | Prüffrage |
| --- | --- | --- |
| MCP-Server | externer Betreiber, neue Tools, neue Datenpfade | Wer betreibt den Server und welche Aktionen stellt er bereit? |
| Connected Agent | zweite Agentenlogik, weitere Wissensquellen, weitere Tools | Welche Rolle, welche Daten und welche Freigaben hat der Spezialist? |
| Kombination aus beidem | schwerere Fehlersuche, mehr Credits, mehr Governance-Aufwand | Ist der Mehrwert höher als die zusätzliche Komplexität? |

## Nordwind-Szenario

Der Support-Agent beantwortet Standardfragen. Für Spezialfälle greift er auf externe Dokumentation zurück oder delegiert an einen HR-Agenten, statt alles selbst zu tragen.

## Grenzen

- Ein MCP-Server ersetzt keine Governance-Prüfung; Betreiber, Rechte und Aktionsumfang müssen vorab klar sein.
- Connected Agents sind kein Sammelbecken für ungeklärte Anforderungen; die Rollen müssen klar getrennt bleiben.
- Klickpfade für MCP und Connected Agents vor Kursbeginn verifizieren.

## Fazit

- Konnektoren, MCP und Connected Agents lösen verschiedene Integrationsprobleme.
- MCP liefert externe Tools oder Datenquellen; Connected Agents liefern Delegation.
- Jede zusätzliche Verbindung erweitert die Zugriffsfläche und braucht Review.

Die Übung verbindet einen vorbereiteten MCP-Server mit dem Agenten und testet eine Delegation an den `Nordwind HR-Onboarding-Agent`.
