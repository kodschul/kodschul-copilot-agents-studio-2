# Lab 7.7 – Lösung: MCP-Server und Connected Agent anbinden

**Ändert die Nordwind-Projektbasis?** Ja — der Nordwind Support-Agent erhält eine zusätzliche Tool-Quelle und einen verbundenen Spezialisten-Agenten.

## Ausgangslage

Der Agent soll externe Dokumentation nutzen und HR-nahe Spezialfälle delegieren können.

## Aufgaben

### 1. MCP-Server anbinden

| Feld | Beispiel |
| --- | --- |
| Typ | read-only Dokumentations-MCP |
| URL | `<MCP-Server-URL vom Trainer>` |
| Zweck | offizielle Dokumentation als Tool-Quelle |
| Prüfung | Betreiber bekannt, keine Schreibaktion, vorab freigegeben |

Hinweis: Der konkrete Klickpfad bleibt tenantabhängig und ist vor Kursbeginn zu verifizieren.

### 2. MCP-gestützte Frage

**Beispiel für einen gültigen Test:** eine Frage, deren Antwort aus der freigegebenen Dokumentation stammen muss.

**Erwartetes Verhalten:**

- der Agent nutzt den MCP-Server sichtbar als Quelle,
- die Antwort bleibt auf den Dokumentationsinhalt begrenzt,
- keine Schreibaktion wird angeboten.

### 3. `Nordwind HR-Onboarding-Agent` anlegen

**Kurz-Instruktion:**

> Rolle: HR-naher Onboarding-Agent für Nordwind. Beantworte nur Onboarding-Fragen mit HR-Bezug. Rate nicht bei personenbezogenen Fällen. Wenn Angaben fehlen oder die Antwort nicht sicher ist, formuliere eine HR-Eskalation.

### 4. Verbindung zum Hauptagenten

Ziel der Verbindung: Der Nordwind Support-Agent bleibt erste Anlaufstelle und delegiert nur, wenn die Anfrage erkennbar HR-nah oder personenbezogen ist.

### 5. Delegationsfall testen

**Testanfrage:** „Neue Mitarbeiterin braucht Laptop und Zugang.“

**Sinnvolle Aufteilung:**

| Teil der Anfrage | Zuständigkeit |
| --- | --- |
| Laptop, VPN, IT-Zugang | Nordwind Support-Agent |
| Onboarding-Ablauf, erste Woche, Buddy/Patin | Nordwind HR-Onboarding-Agent |
| Vertrags- oder Personaldetails | HR-Eskalation statt Antwort |

### 6. Risiken und Gegenmaßnahmen

| Erweiterung | Risiko | Gegenmaßnahme |
| --- | --- | --- |
| MCP-Server | externer Betreiber stellt unerwartete Tools bereit | nur read-only, Betreiber und Aktionsumfang vorab freigeben |
| Connected Agent | Spezialist nutzt zu breite Wissensquellen | eigene Review-Freigabe und klarer Rollenfokus |

## Checkpoint

- Der MCP-Server ist read-only und freigegeben.
- Der Agentname stimmt exakt.
- Die Delegation teilt den Fall sichtbar auf.

## Abschlusskriterien

- Eine MCP-gestützte Antwort ist dokumentiert.
- Ein Delegationsfall zwischen Haupt- und Spezialisten-Agent wurde nachvollziehbar beschrieben.

## Erweiterung

Ein Gegenbeispiel ohne Delegation oder MCP ist sinnvoll, wenn die Frage direkt aus den Nordwind-Wissensquellen beantwortbar ist, etwa „Welches VPN nutzen wir?“

## Fallback

Ohne Live-Umgebung bleibt die Lösung eine Architektur- und Governance-Skizze. Die tatsächlichen Klickpfade und Laufzeitsignale sind vor dem Kurs im Tenant zu verifizieren.
