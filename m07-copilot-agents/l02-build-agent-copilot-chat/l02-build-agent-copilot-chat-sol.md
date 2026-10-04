# Lab 7.2 – Lösung: Agent in Copilot Chat bauen

## Aufgaben

### 1. Kurzkonzept mit Assistent 2

Mögliche Skill-Kandidaten aus dem Architektur-Entwurf:

| Kandidat | Zweck |
| --- | --- |
| `frage-klassifizieren` | erkennt Standardfrage, Grenzfall oder Eskalation |
| `vpn-zugang-erklaeren` | erklärt VPN-Zugang aus der IT-Richtlinie |
| `onboarding-checkliste-erstellen` | bündelt erste Schritte aus dem Leitfaden |
| `ticket-eskalation-vorbereiten` | bereitet Übergabe an IT oder HR vor |
| `antwort-knapp-formatieren` | hält Stil und Struktur konsistent |

Ablauf: Anfrage einordnen → passende Quelle nutzen → knapp antworten oder an IT/HR eskalieren.

### 2. System-Prompt und drei Skill-Entwürfe

Beispiel für den finalen Kern des System-Prompts:

```text
Rolle: interner Nordwind Support-Agent für IT- und Onboarding-Standardfragen.
Nutze nur die hinterlegte IT-Richtlinie und den Onboarding-Leitfaden.
Antworte kurz, sachlich und ohne Vermutungen.
Wenn eine Frage Gehalt, individuelle Ausnahmen oder nicht belegte Sonderfälle betrifft,
verweise an IT oder HR und erfinde keine Antwort.
```

Die drei konsistent benannten Skill-Entwürfe:

| Skill-Name | Deutsche Beschreibung |
| --- | --- |
| `vpn-zugang-erklaeren` | Erklärt den VPN-Zugang bei Nordwind auf Basis der IT-Richtlinie. |
| `onboarding-checkliste-erstellen` | Erstellt aus dem Onboarding-Leitfaden eine kurze Checkliste für die ersten Schritte. |
| `ticket-eskalation-vorbereiten` | Bereitet eine saubere Eskalation an IT oder HR vor, wenn die Quellen nicht ausreichen. |

### 3. System-Prompt testen und nachschärfen

| Testfrage | Erwartetes Verhalten | Ergebnis |
| --- | --- | --- |
| „Welches VPN nutzen wir bei Nordwind?“ | nennt Cisco Secure Client | korrekt |
| „Was passiert am ersten Arbeitstag?“ | nennt Erstlogin, Passwortwechsel, MFA und vorbereitete Software | korrekt |
| „Wie hoch ist die Gehaltsbandbreite meiner Position?“ | eskaliert an HR | korrekt nach Ergänzung der Eskalationsregel |

Nachschärfung: Eskalationsregel für HR-Themen ausdrücklich ergänzt.

### 4. Agent im Copilot-Chat-Harness anlegen

| Feld | Beispielwert |
| --- | --- |
| Name | Nordwind Support-Agent |
| Instruktionen | finaler System-Prompt aus Aufgabe 2/3 |
| Wissen | `../../project/nordwind-it-richtlinie.md`, `../../project/nordwind-onboarding-leitfaden.md` |
| Harness | Copilot-Chat-Harness |

### 5. Erneut testen und für Lab 7.5 dokumentieren

Dokumentiert werden sollten:

- finaler System-Prompt,
- drei Skill-Entwürfe mit konsistenten Namen,
- kurze Testergebnisse zu VPN, Onboarding und Eskalation,
- Hinweis: Workflow-/Tool-Anbindung folgt erst in Lab 7.6.

## Checkpoint

- Das Architekturpaket bleibt schlank und überschreitet die 5–6 Skill-Kandidaten nicht.
- Genau drei Skill-Entwürfe sind für Lab 7.5 vorbereitet.
- Die Eskalation für Gehaltsfragen ist explizit und nicht nur implizit angenommen.

## Abschlusskriterien

- Der Nordwind Support-Agent ist für den Vergleich mit Lab 7.4 verfügbar.
- Die drei Skill-Entwürfe sind uploadfähig vorbereitet und konsistent benannt.
- Die Testnotizen zeigen mindestens eine gezielte Prompt-Korrektur.

## Erweiterung

Eine kombinierte Frage wie „Wie komme ich am ersten Tag per VPN ins Firmennetz?“ deckt gut auf, ob der Prompt mehrere Quellen knapp zusammenführen kann.

## Fallback

Im Fallback bleibt das Ergebnis tragfähig, wenn Prompt, Skill-Entwürfe und Konfiguration vollständig dokumentiert sind. Die reale Antwortqualität des Harness kann dabei nur über Trainer-Demo oder Vergleichsnotizen bewertet werden.
