# Nordwind Consulting – Kursprojekt

Ein einziges, anonymisiertes Beispielunternehmen zieht sich durch beide Kurstage: **Nordwind
Consulting**. Alle Daten sind fiktiv.

Dieser Ordner bündelt die Dateien, die mehr als ein Lab wiederverwendet. Einzelne Übungen
referenzieren nur die Dateien, die sie tatsächlich brauchen.

## Wie sich das Projekt aufbaut

| Tag | Nach Modul | Nordwind gewinnt hinzu                                                                  | Datei(en) hier                                                    |
| --- | ---------- | --------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| 1   | vor M01    | Ausgangslage: laufendes Projekt "Hafenmodernisierung", Stand Woche 6                    | `nordwind-projektnotizen.md`, `nordwind-jourfixe-protokoll.md`    |
| 1   | M02        | HITL-Gliederung für das Pitchdeck                                                       | entsteht in Lab 2.4, nicht separat abgelegt                       |
| 1   | M03        | Kundenangebot (Word), Pitchdeck (PowerPoint)                                            | `nordwind-angebotsvorlage.md` (Vorlage), Entwurf entsteht in Lab 3.1 |
| 1   | M04        | Budget-Analyse und generiertes Makro (Excel)                                            | `nordwind-budget-daten.md`                                        |
| 1   | M06        | Kundenmail (Outlook), Kickoff-Recap (Teams)                                             | entsteht in den Labs, referenziert `nordwind-jourfixe-protokoll.md` |
| 1–2 | M07        | Support-Agent: Idee (Lab 7.1), Copilot-Chat-Agent (7.2), Studio-Agent mit Skills, Workflow, MCP und Connected Agent (7.4–7.7), Governance-Blatt (7.9), Aktionsplan (7.10) | `nordwind-it-richtlinie.md`, `nordwind-onboarding-leitfaden.md` |

## Vorhandene Dateien

- `nordwind-projektnotizen.md`/`.docx` — Eckdaten, Arbeitspaketstand, Risiken, offene Punkte; auch als echtes Word-Dokument zum Öffnen/Referenzieren per /-Befehl (M03, Lab 3.1)
- `nordwind-jourfixe-protokoll.md`/`.docx` — Protokoll des letzten Jour fixe, Grundlage für die Outlook-/Teams-Labs in M06, `.docx` zum Anhängen an die Outlook-Mail
- `nordwind-angebotsvorlage.md` — Struktur- und Formatierungsvorgaben für Nordwind-Angebote (M03), textliche Referenzfassung
- `nordwind-angebotsvorlage.docx` — dieselbe Vorlage als echtes Word-Dokument zum Öffnen mit Copilot in Word (M03, Lab 3.1)
- `nordwind-budget-daten.md` — Kostenblöcke nach Monat mit Kontrollsumme, Grundlage für die Excel-Labs (M04), textliche Referenzfassung
- `nordwind-budget-daten.xlsx` — dieselbe Tabelle als echte Excel-Arbeitsmappe inkl. Kontrollsummenformeln, direkt mit Copilot in Excel nutzbar (M04, Lab 4.1/4.2)
- `nordwind-pitchdeck-starter.pptx` — leeres PowerPoint-Grundgerüst (Titelfolie + eine Platzhalterfolie) als Ablagepunkt für die per HITL erzeugten Folien (M03, Lab 3.2)
- `szenarien.md` — fünf Kurzszenarien für die Einordnungsübung in Lab 1.1
- `nordwind-it-richtlinie.md` — VPN, Geräte-/Passwortrichtlinie, IT-Support-Kontakt; Wissensquelle für den Support-Agenten (M07, Lab 7.2/7.4)
- `nordwind-onboarding-leitfaden.md` — Ablauf erster Arbeitstag, erste 30 Tage, häufige Fragen; zweite Wissensquelle für den Support-Agenten (M07, Lab 7.2/7.4/7.7)

Die `.md`-Fassungen sind die versionierte Quelle (für Diffs, Reviews, Slides); die `.docx`/`.xlsx`/`.pptx`-Fassungen
sind die Dateien, die Teilnehmende tatsächlich in Word/Excel/PowerPoint mit Copilot öffnen. Beide Fassungen bleiben
inhaltlich synchron — wird eine Zahl oder Struktur geändert, in beiden Formaten nachziehen.

Von Teilnehmenden erzeugte Zwischenstände (z. B. `nordwind-angebot-entwurf.md` aus Lab 3.1) werden
ebenfalls in diesem Ordner abgelegt, damit spätere Labs darauf zurückgreifen können.

## Für den Trainer

- Alle Zahlen, Namen und Termine sind fiktiv; keine echten Kundendaten verwenden oder ergänzen.
- Die Wissensquellen des Support-Agenten (`nordwind-it-richtlinie.md`, `nordwind-onboarding-leitfaden.md`) vor Tag 2 in einen für die Teilnehmenden zugänglichen SharePoint-Ordner legen.
