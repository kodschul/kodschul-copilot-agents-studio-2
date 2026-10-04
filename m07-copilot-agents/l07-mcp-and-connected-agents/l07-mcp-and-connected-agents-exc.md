# Lab 7.7 – Übung: MCP-Server und Connected Agent anbinden

**Ändert die Nordwind-Projektbasis?** Ja — der Nordwind Support-Agent erhält eine zusätzliche Tool-Quelle und einen verbundenen Spezialisten-Agenten.

## Ausgangslage

Der Nordwind Support-Agent verfügt bereits über Skills und den Workflow `Support-Ticket anlegen`. Nun kommen zwei neue Integrationspfade hinzu.

Für Teil A wird ein read-only MCP-Server verwendet, den der Trainer vorab auswählt. Die URL bleibt im Material bewusst offen: `<MCP-Server-URL vom Trainer>`.

## Aufgaben

1. Den vom Trainer freigegebenen MCP-Server `<MCP-Server-URL vom Trainer>` anbinden. Klickpfad vor Kursbeginn im Tenant verifizieren.
2. Eine Frage an den Agenten stellen, die sichtbar den MCP-Server braucht, und das Ergebnis dokumentieren.
3. Einen zweiten Agenten mit dem Namen `Nordwind HR-Onboarding-Agent` anlegen. Die Instruktionen kurz halten: HR-nahe Onboarding-Fragen beantworten, personenbezogene Fälle nicht raten, bei Unklarheit an HR eskalieren.
4. Den `Nordwind HR-Onboarding-Agent` mit dem Nordwind Support-Agenten verbinden. Klickpfad vor Kursbeginn im Tenant verifizieren.
5. Den Delegationsfall „Neue Mitarbeiterin braucht Laptop und Zugang“ im Preview testen und notieren, welcher Teil beim Support-Agenten bleibt und welcher Teil an den HR-Agenten geht.
6. Für MCP-Server und Connected Agent je ein Risiko sowie eine passende Governance-Gegenmaßnahme notieren.

## Checkpoint

- Der MCP-Server ist read-only und vorab freigegeben.
- Der zweite Agent trägt exakt den Namen `Nordwind HR-Onboarding-Agent`.
- Im Delegationsfall ist sichtbar, dass nicht alles im Hauptagenten bleibt.

## Abschlusskriterien

- Eine erfolgreiche MCP-gestützte Antwort liegt vor.
- Ein getesteter Delegationsfall zwischen Support- und HR-Agent ist dokumentiert.

## Erweiterung

Eine zweite Frage formulieren, bei der bewusst **kein** MCP und **kein** Connected Agent gebraucht wird, um die Abgrenzung sichtbar zu machen.

## Fallback

Ohne Tenant-Zugriff: der Trainer-Demo folgen und eine Skizze mit drei Kästen erstellen (Support-Agent, MCP-Server, HR-Agent) sowie Datenfluss, Delegation und Risiken beschriften. Einschränkung: kein echter Laufzeitnachweis.
