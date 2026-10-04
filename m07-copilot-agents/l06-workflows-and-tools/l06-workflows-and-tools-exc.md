# Lab 7.6 – Übung: Workflow `Support-Ticket anlegen`

**Ändert die Nordwind-Projektbasis?** Ja — der Nordwind Support-Agent erhält den Workflow `Support-Ticket anlegen` als Tool-Baseline für die weiteren Labs.

## Ausgangslage

Der Agent aus Lab 7.5 kann Standardfragen beantworten und Eskalationen vorbereiten. Jetzt soll daraus ein echter Handlungsschritt entstehen.

Als Ziel ist genau **eine** der freigegebenen Varianten vorgesehen:

- SharePoint-Listenpunkt für den IT-Support, oder
- Teams-Benachrichtigung an den Support-Kanal.

## Aufgaben

1. Vor dem Bauen festlegen, welche Zielvariante im Training freigegeben ist, und die benötigten Felder notieren: Titel, Kategorie, Priorität, anfragende Person, Kurzbeschreibung.
2. Einen Workflow mit dem Namen `Support-Ticket anlegen` erstellen und den Trigger **When an agent calls the flow** wählen.
3. Die Zielaktion ergänzen: entweder einen SharePoint-Listeneintrag anlegen oder eine Teams-Nachricht senden.
4. Einen Human-in-the-loop-Schritt ergänzen, der vor dem finalen Anlegen oder Senden eine Freigabe verlangt.
5. Den Workflow als Tool zum Nordwind Support-Agenten hinzufügen.
6. Im Preview eine Anfrage formulieren, die nicht direkt beantwortet werden darf, sondern ein Ticket auslösen soll, und den Ablauf bis zur Freigabe testen.
7. Dokumentieren, welche Eingaben der Agent an den Workflow übergibt und wo der Ablauf bewusst deterministisch bleibt.

## Checkpoint

- Der Workflow heißt exakt `Support-Ticket anlegen`.
- Der Trigger ist agentengesteuert, nicht manuell oder zeitgesteuert.
- Der Test stoppt vor der finalen Aktion an einer menschlichen Freigabe.

## Abschlusskriterien

- Der Agent kann im Preview eine passende Anfrage an den Workflow übergeben.
- Die Zielaktion ist sichtbar vorbereitet oder ausgeführt, abhängig vom Freigabeschritt.

## Erweiterung

Eine zweite Benachrichtigung ergänzen, etwa Teams **und** SharePoint, ohne den Workflow-Namen oder die Kernfelder zu ändern.

## Fallback

Ohne Tenant-Zugriff: der Trainer-Demo folgen und das Workflow-Designblatt mit Trigger, Feldern, Zielsystem, Freigabepunkt und deterministischen Schritten ausfüllen. Einschränkung: kein echter Tool-Aufruf im Preview.
