---
theme: default
layout: default
---

# Lab 5.2: Personalisierung & Copilot-Speicher

**Leitfragen:**

<details>
<summary>Was gehört in ein Personalisierungsprofil und was besser nicht?</summary>

Beruflicher Kontext, Arbeitsstil und bevorzugte Tonalität gehören hinein. Vertrauliche oder wechselnde Projektdetails gehören nicht hinein, weil das Profil dauerhaft und global für alle Chats gilt.

</details>

<details>
<summary>Was merkt sich Copilot dauerhaft — und was gerade nicht?</summary>

Nur explizit bestätigte Einzelfakten wie Rolle oder Zuständigkeit. Nicht automatisch gemerkt werden ganze Chatverläufe oder beiläufig erwähnte Details.

</details>

<details>
<summary>Wie löscht oder korrigiert man einen gespeicherten Eintrag?</summary>

Über die Speicherverwaltung in den Copilot-Einstellungen; einzelne Einträge lassen sich dort ansehen, korrigieren oder entfernen.

</details>

- Ein Personalisierungsprofil sagt Copilot, in welcher Rolle, mit welchem Stil und für wen geantwortet werden soll — dauerhaft, ohne es in jedem Prompt zu wiederholen.
- Der Copilot-Speicher merkt sich zusätzlich einzelne, ausdrücklich bestätigte Fakten über mehrere Chats hinweg.

## Zwei unterschiedliche Mechanismen

| Mechanismus             | Was es ist                                                  | Geltungsbereich            |
| ----------------------- | ----------------------------------------------------------- | -------------------------- |
| Personalisierungsprofil | benutzerdefinierte Anweisungen: Rolle, Stil, Zielgruppe     | für jeden neuen Chat aktiv |
| Copilot-Speicher        | einzelne, bestätigte Fakten (z. B. Zuständigkeit, Vorliebe) | über Chats hinweg abrufbar |

> **[SCREENSHOT-PLATZHALTER – Quelle erforderlich]** UI-Pfad: Copilot-Einstellungen → Personalisierung/Speicherverwaltung mit Liste gespeicherter Einträge. Ersetzen durch eigene anonymisierte Sandbox-Aufnahme (mit Aufnahmedatum) oder offizielle Microsoft-Learn-Abbildung (mit Quelle und Datum).

> **Merksatz:** Das Profil beschreibt, _wie_ geantwortet wird; der Speicher merkt sich _was_ über die Person bekannt ist.

## Was der Speicher merkt — und was nicht

- Merkt sich: explizit bestätigte Einzelfakten ("merke dir, dass ich für den Bereich X zuständig bin").
- Merkt sich nicht automatisch: ganze Chatverläufe, beiläufige Erwähnungen, einmalige Projektdetails.
- Jeder gespeicherte Eintrag ist einsehbar und einzeln löschbar — kein unsichtbares Sammeln.

## Grenzen

- Ein zu allgemeines Profil ("freundlich und professionell") verändert Antworten kaum spürbar.
- Vertrauliche oder personenbezogene Daten Dritter gehören nicht ins Profil oder in den Speicher.
- Gespeicherte Fakten gelten global, nicht nur für ein einzelnes Projekt — Einträge entsprechend allgemein halten.

## Fazit

- Profil und Speicher lösen unterschiedliche Probleme: Stil dauerhaft festlegen vs. einzelne Fakten merken.
- Nur ausdrücklich bestätigte Fakten landen im Speicher, kein automatisches Mitschreiben.
- Jeder Eintrag bleibt einsehbar und korrigierbar.

Die Übung legt ein eigenes Profil an und prüft, was Copilot sich davon merkt.
