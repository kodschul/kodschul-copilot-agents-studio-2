---
theme: default
layout: default
---

# Lab 7.1: Was ist ein Custom Agent? Anwendungsfälle

Custom Agents bearbeiten einen klaren Auftrag mit konfiguriertem Verhalten, Wissen, Tools und Skills. Dieses Lab grenzt passende Anwendungsfälle ab und bereitet den Nordwind Support-Agenten für Tag 2 vor.

**Leitfragen:**

<details>
<summary>Was macht einen Agenten mehr als einen gespeicherten Prompt?</summary>

Ein Agent verbindet Ziel, Regeln und angebundene Bausteine zu einem wiederverwendbaren Verhalten. Ein gespeicherter Prompt bleibt dagegen nur eine Textvorlage ohne eigene Laufzeitlogik.

</details>

<details>
<summary>Woran erkennt man einen lohnenden Anwendungsfall?</summary>

Die Aufgabe wiederholt sich, die Wissenslage ist ausreichend stabil und der Nutzen ist für mehrere Personen sichtbar. Dann lohnt sich Pflege- und Bauaufwand eher.

</details>

<details>
<summary>Welche Aufgaben gehören bewusst nicht an einen Agenten?</summary>

Einmalige Sonderfälle, heikle Einzelfallentscheidungen und Arbeit ohne belastbare Datenbasis bleiben besser beim Menschen. Ein Agent verstärkt sonst Unsicherheit statt Nutzen.

</details>

## Vier Bausteine eines Agenten

| Baustein | Rolle | Nordwind-Beispiel |
| --- | --- | --- |
| Instruktionen | beschreiben Zweck, Stil, Grenzen und Eskalationsregeln | „Antworte nur auf Basis der Nordwind-Quellen und eskaliere Gehaltsfragen an HR.“ |
| Wissen | liefert die fachliche Grundlage | IT-Richtlinie und Onboarding-Leitfaden |
| Tools | führen Aktionen oder Systemzugriffe aus | später z. B. Ticket-Workflow oder Tool-Aufruf |
| Skills | kapseln wiederverwendbares Aufgaben-Know-how | VPN erklären, Checkliste erstellen, Eskalation vorbereiten |

## Prompt, Chat und Agent sauber trennen

| Form | Wofür geeignet | Grenze |
| --- | --- | --- |
| Einzelprompt | einmalige Anfrage oder Entwurf | keine dauerhafte Struktur |
| Chat mit Verlauf | Nachfragen und Verfeinerung im Gespräch | bleibt an den Verlauf gebunden |
| Custom Agent | wiederkehrende Aufgabe mit festen Regeln und Quellen | braucht Pflege, Tests und klare Grenzen |

## Drei Harnesses im Kurzüberblick

| Harness | Kurzidee | Typische Stärke |
| --- | --- | --- |
| Copilot-Chat-Harness | erweitert Microsoft Copilot Chat um Unternehmenswissen | schneller interner Wissensagent |
| Standard-Harness | arbeitet regelbasiert mit Topics und Pfaden | vorhersagbarer Helpdesk- oder FAQ-Ablauf |
| GitHub-Copilot-Harness | plant mehrstufige Schritte dynamisch aus einem Ziel heraus | reasoning-starke Prozesse mit Dateien, Skills und Memory |

Die Detailentscheidung folgt in Lab 7.3. Für dieses Lab reicht die Orientierung: Nicht jeder Anwendungsfall braucht den stärksten Harness.

## The Nextise Agentic Way im Kurs

Nordwind Consulting sammelt wiederkehrende IT- und Onboarding-Fragen bisher verteilt über E-Mail, Chat und Zuruf. Tag 2 baut daraus einen Support-Agenten, aber erst nach einer sauberen Problemklärung.

| Schritt | Assistent | Ergebnis |
| --- | --- | --- |
| 1 | Problem-Solver | Use-Case-Canvas und Top-1-Empfehlung |
| 2 | Solution Architect | Kurzkonzept, Ablauf und Skill-Kandidaten |
| 3 | Skill-/System-Prompt-Generator | System-Prompt und Skill-Entwürfe |

> **Merksatz:** Ein guter Agent beginnt nicht mit einem Tool, sondern mit einem klaren Problem und vier sauber getrennten Bausteinen.

## Grenzen und Stolpersteine

- Eine unklare oder ständig wechselnde Datenlage erzeugt Pflegeaufwand statt Entlastung.
- Ein Agent ohne Eskalationsregel antwortet schnell, aber nicht automatisch verantwortbar.
- Der stärkste Harness ist nicht automatisch der beste; zu viel Orchestrierung erhöht Aufwand, Latenz und später auch Credits.

## Fazit

- Ein Agent kombiniert Instruktionen, Wissen, Tools und Skills zu einem klaren Auftrag.
- Lohnend sind wiederkehrende Aufgaben mit stabiler Wissensbasis und sichtbarem Nutzen.
- Der Nordwind Support-Agent ist ein guter Kandidat, weil IT- und Onboarding-Fragen häufig auftreten und abgrenzbare Quellen haben.

Die Übung klassifiziert Anwendungsfälle und erarbeitet mit Assistent 1 die Top-1-Empfehlung für Nordwind.
