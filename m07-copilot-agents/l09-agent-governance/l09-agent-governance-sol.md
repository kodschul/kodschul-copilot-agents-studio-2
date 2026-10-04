# Lab 7.9 – Lösung: Governance-Blatt für den Nordwind Support-Agenten

**Ändert die Nordwind-Projektbasis?** Nein — es entsteht die Freigabe- und Betriebsdokumentation für den bestehenden Agenten.

## Ausgangslage

Der Agent soll nicht nur funktionieren, sondern kontrolliert gebaut, freigegeben und betrieben werden.

## Aufgaben

### 1. Governance-Blatt anlegen

| Zeile | Eintrag für Nordwind |
| --- | --- |
| Zielgruppe | neue Mitarbeitende sowie interne Standard-Support-Anfragende |
| Wissensquellen | `nordwind-it-richtlinie.md`, `nordwind-onboarding-leitfaden.md` |
| Skills | `vpn-zugang-erklaeren`, `onboarding-checkliste-erstellen`, `ticket-eskalation-vorbereiten` |
| Workflow/Tools | `Support-Ticket anlegen` |
| MCP-Server | optional, nur read-only Dokumentationsserver `<MCP-Server-URL vom Trainer>` |
| Connected Agents | `Nordwind HR-Onboarding-Agent` |
| Freigeber | IT-Leitung gemeinsam mit HR-Verantwortung für den Onboarding-Teil |
| Review-Turnus | monatlich im Pilot, danach quartalsweise |
| Abschaltkriterium | Wissensquellen veraltet, Owner nicht benannt oder Credit-Limit überschritten |
| Umgebung/Solution | getrennte Test-/Pilot-Umgebung, Agent und Flow gemeinsam versioniert |
| Credit-Limit | pro Pilotumgebung festgelegt, mit benannter Verbrauchsverantwortung |

### 2. Offen markieren statt raten

Beispiel für einen sauber offenen Punkt:

- MCP-Server bleibt „noch offen“, solange Betreiber, URL und Tool-Umfang nicht freigegeben sind.

### 3. Zusätzliche Review-Fragen notieren

| Erweiterung | Review-Frage |
| --- | --- |
| Skills | Löst der Skill nur in den vorgesehenen Fällen aus? |
| MCP-Server | Welche Tools und Daten stellt der Server konkret bereit? |
| Connected Agents | Welche eigenen Wissensquellen und Tools bringt der Spezialisten-Agent mit? |

### 4. Wer darf bauen, veröffentlichen, teilen?

| Tätigkeit | Rolle |
| --- | --- |
| bauen | Pilotteam im geschützten Testkontext |
| veröffentlichen | benannte Freigeber nach Review |
| teilen | nur an die freigegebene Zielgruppe |

### 5. Review-Turnus und Abschaltkriterium

- **Review-Turnus:** monatlicher Pilot-Review auf Wissensquellen, Fehltrigger und Credit-Verbrauch
- **Abschaltkriterium:** veraltete Richtlinien, fehlender Owner oder wiederholte Eskalationsfehler

### 6. Credit-Limit und Verantwortung

- Limit wird vor dem Pilot pro Umgebung festgelegt.
- Verantwortung liegt bei der Rolle, die Pilot und Evaluation freigibt.
- Evaluate ist vor Produktion Pflicht, damit Credits nicht in vermeidbare Fehlpfade laufen.

## Checkpoint

- Alle Zusatzzeilen sind enthalten.
- Offene Punkte wurden sichtbar offen gelassen.
- Build, Publish und Share sind rollensepariert.

## Abschlusskriterien

- Das Governance-Blatt ist vollständig genug für einen Pilotentscheid.
- Review-Turnus, Abschaltkriterium und Credit-Verantwortung sind explizit festgehalten.

## Erweiterung

Für Produktion würden strengere DLP-, Freigabe- und Monitoring-Regeln ergänzt. Im Pilot reicht eine schlankere, aber dokumentierte Variante.

## Fallback

Ohne Live-Umgebung bleibt die Lösung ein statisch ausgefülltes Governance-Artefakt. Rollen, Umgebungen und Limits müssen dann vor dem Kurs im Tenant abgeglichen werden.
