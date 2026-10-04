# Lab 7.1 – Lösung: Was ist ein Custom Agent? Anwendungsfälle

## Aufgaben

### 1. Drei Fälle klassifizieren

| Fall | Einordnung | Begründung |
| --- | --- | --- |
| VPN- und Onboarding-Fragen | passend | wiederkehrend, klare Wissensquellen, mehrere Betroffene |
| einmalige Sonderfreigabe für einen Vertrag | unpassend | Einzelfall, hohes Ermessen, keine stabile Wiederholung |
| Rückfragen zu Standard-Reisekosten | passend | häufige Standardfrage mit definierbarer Richtlinie |

### 2. Problem-Solver starten

Als Startbeschreibung eignet sich: „Bei Nordwind beantworten IT und HR viele wiederkehrende Fragen zu VPN, Erstlogin, Standardsoftware und Onboarding manuell. Ziel ist ein interner Support-Agent für Standardfragen mit klarer Eskalation bei Sonderfällen.“

### 3. Problem, Nutzen und Datenquellen schildern

Belastbare Eingaben für den Assistenten:

- **Zielgruppe:** neue Mitarbeitende und interne Teams bei Nordwind
- **Ist-Prozess:** Frage per Mail oder Chat, Antwort hängt von der gerade erreichbaren Person ab
- **Nutzen:** schnellere Erstantwort und weniger Unterbrechungen für IT/HR
- **Datenquellen:** `nordwind-it-richtlinie.md`, `nordwind-onboarding-leitfaden.md`

### 4. Use-Case-Canvas und Top-1-Empfehlung

| Feld | Ausfüllung |
| --- | --- |
| Problem | Wiederkehrende IT- und Onboarding-Fragen binden Zeit in IT und HR. |
| Zielgruppe | Neue Mitarbeitende sowie interne Ansprechpartner bei Nordwind. |
| Ist-Prozess | Fragen kommen verteilt per E-Mail, Teams oder Zuruf; Antworten variieren und dauern unterschiedlich lang. |
| Soll-Prozess | Ein Agent beantwortet Standardfragen direkt aus den Quellen und eskaliert Sonderfälle an Menschen. |
| Nutzen | Schnellere Erstantwort, weniger Unterbrechungen, konsistentere Auskünfte. |
| Datenquellen | IT-Richtlinie und Onboarding-Leitfaden. |
| Risiken | Veraltete Dokumente, unklare Zuständigkeiten, sensible Sonderfragen. |

Messbares Erfolgskriterium: „Neue Mitarbeitende erhalten in den ersten 30 Tagen Standardantworten zu VPN, Erstlogin und Standardsoftware ohne Rückfrage an IT oder HR, sofern die Frage in den Nordwind-Quellen enthalten ist.“

Top-1-Empfehlung: **Nordwind Support-Agent für interne IT- und Onboarding-Standardfragen**.

### 5. Klassifizierung prüfen und korrigieren

Die drei Fälle bleiben nach der Prüfung konsistent. Nur der Vertragsfall fällt klar heraus, weil Risiko und Einzelfallcharakter den Nutzen eines Agenten übersteigen.

## Checkpoint

- Alle sieben Canvas-Felder sind ausgefüllt.
- Die Top-1-Empfehlung nennt den Nordwind Support-Agenten ausdrücklich.
- Das Erfolgskriterium ist messbar und an konkrete Fragearten gekoppelt.

## Abschlusskriterien

- Der Support-Agent ist als nächster Bauschritt belastbar begründet.
- Die Problemnotizen reichen aus, um in Lab 7.2 daraus ein Kurzkonzept abzuleiten.

## Erweiterung

Bei einer zu vagen Eingabe fordert der Problem-Solver typischerweise Zielgruppe, Datenquellen und Abgrenzung nach. Genau diese Rückfragen schärfen später Prompt und Skill-Entwürfe.

## Fallback

Auch ohne Live-Dialog bleibt die Top-1-Empfehlung tragfähig, wenn der Canvas vollständig ausgefüllt und das Erfolgskriterium sauber formuliert ist. Die Dialogqualität des Assistenten selbst lässt sich im Fallback jedoch nicht bewerten.
