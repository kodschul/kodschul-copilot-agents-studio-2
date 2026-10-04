# Lab 7.6 – Lösung: Workflow `Support-Ticket anlegen`

**Ändert die Nordwind-Projektbasis?** Ja — der Nordwind Support-Agent erhält den Workflow `Support-Ticket anlegen` als Tool-Baseline für die weiteren Labs.

## Ausgangslage

Der Agent soll Eskalationen nicht nur formulieren, sondern in einen deterministischen Ablauf übergeben.

## Aufgaben

### 1. Zielfelder festlegen

| Feld | Zweck |
| --- | --- |
| Titel | kurze Beschreibung des Vorfalls |
| Kategorie | z. B. VPN, Onboarding, Sonderberechtigung |
| Priorität | niedrig, mittel, hoch |
| Anfragende Person | Rückruf- oder Kontaktbezug |
| Kurzbeschreibung | strukturierte Eskalationszusammenfassung |

### 2. Workflow anlegen

Name: `Support-Ticket anlegen`

Trigger: **When an agent calls the flow**

Erwartete Eingaben aus dem Agenten:

- `titel`
- `kategorie`
- `prioritaet`
- `anfragende_person`
- `kurzbeschreibung`

### 3. Zielaktion ergänzen

**Variante A – SharePoint als Baseline:**

- Aktion: neuen Listeneintrag im Support-Backlog anlegen
- Zuordnung: Titel → Spalte Titel, Priorität → Spalte Priorität, Kurzbeschreibung → Beschreibung

**Variante B – Teams als gültige Alternative:**

- Aktion: Nachricht im Support-Kanal senden
- Nachricht enthält Titel, Priorität, anfragende Person und Eskalationszusammenfassung

### 4. Human-in-the-loop ergänzen

Vor der Zielaktion liegt ein Freigabeschritt, der mindestens diese Angaben zeigt:

- Zusammenfassung des Tickets
- Zielsystem der Aktion
- verantwortliche Zielgruppe

Erst nach Bestätigung läuft die Zielaktion weiter.

### 5. Workflow als Tool hinzufügen

Tool-Beschreibung, die den Agenten gut steuert:

> Nutze `Support-Ticket anlegen`, wenn eine Nordwind-Anfrage nicht sicher direkt beantwortet werden darf und stattdessen strukturiert an IT oder HR übergeben werden muss.

### 6. Preview-Test

**Testanfrage:** „Ich brauche für mein privates Tablet Zugriff auf das Firmennetz und eine Ausnahme von der Standardregel.“

**Erwartetes Verhalten:**

1. Standardantwort reicht nicht aus.
2. Eskalationsdaten werden gesammelt.
3. Workflow `Support-Ticket anlegen` wird aufgerufen.
4. Freigabeschritt stoppt vor der finalen Aktion.

### 7. Deterministische und adaptive Teile dokumentieren

| Teil | Art | Begründung |
| --- | --- | --- |
| Anfrage bewerten | adaptiv | Agent entscheidet, ob Standardantwort reicht |
| Ticketfelder füllen | adaptiv | Felder werden aus der Anfrage abgeleitet |
| Ticket anlegen / Nachricht senden | deterministisch | gleicher Ablauf, gleiche Zielaktion |
| Freigabe vor finaler Aktion | deterministisch | feste Kontrollstelle |

## Checkpoint

- Der Workflow-Name stimmt exakt.
- Der Trigger ist agentengesteuert.
- Der Test stoppt vor der finalen Aktion an einer Freigabe.

## Abschlusskriterien

- Der Agent kann eine Eskalation als Tool-Aufruf übergeben.
- Die Zielaktion ist reproduzierbar beschrieben und klar kontrolliert.

## Erweiterung

Eine zweite Benachrichtigung ist möglich, solange die Baseline unverändert bleibt: gleicher Trigger, gleiche Eingabefelder, gleicher Freigabepunkt.

## Fallback

Ohne Live-Umgebung bleibt die Lösung ein statisch geprüfter Ablauf mit vollständigem Designblatt. Der echte Tool-Aufruf muss dann vor dem Kurs im Tenant verifiziert werden.
