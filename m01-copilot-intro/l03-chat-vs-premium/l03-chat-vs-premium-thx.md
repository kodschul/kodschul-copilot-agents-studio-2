# Lab 1.3: Copilot Chat vs. Microsoft 365 Copilot

**Leitfragen:**

<details>
<summary>Was ist der entscheidende Unterschied in der Datenbasis?</summary>

Copilot Chat kennt das Web und angehängte Dokumente. Microsoft 365 Copilot kennt zusätzlich die eigenen Arbeitsdaten in M365 — Mails, Dateien, Chats, Kalender.

</details>

<details>
<summary>Wann reicht Copilot Chat und wann braucht es wirklich die Volllizenz?</summary>

Chat reicht für allgemeine Formulierungs- und Rechercheaufgaben ohne Bezug zu eigenen Dokumenten. Die Volllizenz braucht es, sobald der eigene Arbeitskontext Teil der Antwort sein soll.

</details>

<details>
<summary>Was darf im freien Chat nicht angehängt werden?</summary>

Alles, was laut interner Richtlinie schützenswert ist — insbesondere personenbezogene Daten, Kundendaten Dritter und Vertrauliches. Die konkrete Liste gibt die eigene Richtlinie vor.

</details>

- Copilot Chat und Microsoft 365 Copilot greifen auf unterschiedliche Daten zu, obwohl beide "Copilot" heißen.
- Sechs Kriterien legen den Unterschied fest und bilden die Grundlage für die Werkzeugwahl im Alltag.

## Web-Modus vs. Arbeit-Modus in Copilot Chat

| Modus  | Datenquelle                                                                    | Verfügbar für                         |
| ------ | ------------------------------------------------------------------------------ | ------------------------------------- |
| Web    | öffentliches Internet plus explizit angehängte Datei                           | alle M365-Lizenzen, ohne Zusatzkosten |
| Arbeit | eigene M365-Arbeitsdaten (Mails, Dateien, Chats, Kalender), zusätzlich zum Web | nur mit Microsoft 365 Copilot-Lizenz  |

> **Merksatz:** Der Umschalter "Web"/"Arbeit" im Chat-Fenster ist die sichtbare Instanz derselben Lizenzfrage.

**So findet man ihn:** oberhalb des Eingabefelds in Copilot Chat. Nur mit Microsoft 365 Copilot-Lizenz sichtbar — ohne Lizenz fehlt er, dann gilt nur der Web-Modus.

## Vergleich entlang von sechs Kriterien

| Kriterium       | Copilot Chat                                               | Microsoft 365 Copilot                                          |
| --------------- | ---------------------------------------------------------- | -------------------------------------------------------------- |
| Beschreibung    | browserbasierte KI-Assistenz, unabhängig von den M365-Apps | KI-Assistenz direkt in Word, Excel, Outlook, Teams             |
| Kosten          | im Rahmen der bestehenden M365-Lizenz, ohne Zusatzkosten   | kostenpflichtige Zusatzlizenz je Nutzer:in und Monat           |
| Integration     | eigenständiger Web-Chat, in Teams/Outlook anheftbar        | direkt in der jeweiligen App, im Dokumentkontext               |
| Datenbasis      | Web plus explizit angehängte Dokumente                     | Web plus eigene Arbeitsdaten (Mails, Dateien, Chats, Kalender) |
| Funktionsumfang | reine Chat-Funktion mit Dateianlage                        | Unterstützung direkt in den Aufgaben der jeweiligen App        |
| Zielgruppe      | alle Mitarbeitenden, besonders gelegentliche Nutzung       | intensive Nutzung: Assistenz, Projektleitung, Beratung         |

> **Prüfpflichtig vor Kursbeginn:** Tier-Bezeichnungen, Funktionsumfang und Listenpreise ändern sich regelmäßig. Aktuelle Werte vor der Durchführung gegen die offizielle Microsoft-Lizenzübersicht abgleichen und Datum notieren.

## Entscheidungsregel

```
Braucht die Antwort meine eigenen Dokumente, Mails oder Termine?
   ja   →  Microsoft 365 Copilot (in der App oder im angemeldeten Chat)
   nein →  Copilot Chat reicht
```

> **Merksatz:** Die Lizenzfrage ist eine Datenfrage. Nicht "was kann das Tool", sondern "auf welche Daten soll es zugreifen".

## Anmeldung als Sicherheitsfaktor

| Zustand                    | Folge                                                                     |
| -------------------------- | ------------------------------------------------------------------------- |
| angemeldet mit Firmenkonto | Unternehmensdatenschutz greift, Eingaben fließen nicht ins Modelltraining |
| nicht angemeldet           | kein Unternehmensdatenschutz; behandelt wie ein öffentlicher Dienst       |

## Grenzen

- Copilot Chat ohne Anmeldung ist kein geeigneter Ort für Arbeitsinhalte.
- Angehängte Dateien im Chat unterliegen einer Größenbeschränkung; sehr große Dokumente müssen gekürzt werden.
- Eine Volllizenz ersetzt keine Berechtigung: Nicht freigegebene Inhalte bleiben unsichtbar.

## Fazit

- Der Unterschied liegt in der Datenbasis, nicht im Sprachmodell.
- Entscheidungsfrage: Sollen eigene Arbeitsdaten Teil der Antwort sein?
- Der Anmeldestatus entscheidet über den Unternehmensdatenschutz, nicht das Tool-Symbol.

In der Übung wird für drei Szenarien das passende Werkzeug gewählt und anhand der sechs Kriterien begründet.
