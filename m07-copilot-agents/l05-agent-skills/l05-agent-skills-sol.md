# Lab 7.5 – Lösung: Skills für den Nordwind Support-Agenten

**Ändert die Nordwind-Projektbasis?** Ja — der Nordwind Support-Agent erhält drei Skills als Baseline für die Labs 7.6 bis 7.9.

## Ausgangslage

Der Nordwind Support-Agent nutzt die Wissensquellen `nordwind-it-richtlinie.md` und `nordwind-onboarding-leitfaden.md`. Drei häufige Teilaufgaben werden als Skills ausgelagert.

## Aufgaben

### 1. Upload-Skill `vpn-zugang-erklaeren`

```md
---
name: vpn-zugang-erklaeren
description: Erklärt den Nordwind-VPN-Zugang Schritt für Schritt auf Basis der IT-Richtlinie. Nutze diesen Skill bei Fragen zu VPN, Remote-Zugriff, Cisco Secure Client, Verbindungsziel, MFA oder Zertifikatslaufzeit. Nutze ihn nicht für Gehalt, Vertragsfragen, Sonderberechtigungen oder private Geräte außerhalb der Standardregel.
---

# Zweck

Eine präzise, kurze VPN-Anleitung für Nordwind liefern.

# Ressourcen

- Knowledge: `nordwind-it-richtlinie.md`

# Vorgehen

1. Prüfen, ob die Anfrage wirklich VPN, Remote-Zugriff oder Anmeldung von außen betrifft.
2. Relevante Fakten aus der IT-Richtlinie extrahieren: Client, Verbindungsziel, Authentifizierung, Zuständigkeit.
3. Die Schritte in sinnvoller Reihenfolge ausgeben.
4. Wenn die Frage nach individuellen Ausnahmen, privaten Geräten oder Sonderrechten fragt, nicht raten, sondern an den IT-Support verweisen.

# Ausgabeformat

- Kurzantwort in 3 bis 5 Stichpunkten.
- Konkrete Produktnamen und das Verbindungsziel nennen.
- Am Ende bei Sonderfällen den Kontaktkanal angeben.

# Sonderfälle

- Private Geräte: nur die Standardregel nennen, keine Umgehung vorschlagen.
- Zertifikat abgelaufen: an IT-Support verweisen.
- Fehlende MFA: auf verpflichtende MFA hinweisen und Eskalation nennen.

# Tool-Hinweise

- Kein externer Tool-Aufruf nötig.
- Falls ein Ticket-Workflow verfügbar ist, nur auf ausdrücklichen Nutzerwunsch an die Eskalation übergeben.
```

### 2. Generate-with-AI-Skill `onboarding-checkliste-erstellen`

**Sinnvolle Antworten auf Copilot-Rückfragen:**

| Rückfrage | Beispielantwort |
| --- | --- |
| Für wen ist die Checkliste gedacht? | Für neue Mitarbeitende oder für den Buddy in den ersten 30 Tagen. |
| Welche Quellen gelten? | Nur `nordwind-onboarding-leitfaden.md` und bei VPN-Themen zusätzlich die IT-Richtlinie. |
| Wie soll das Ergebnis aussehen? | Als kompakte Checkliste nach „vor dem ersten Arbeitstag“, „erster Arbeitstag“ und „erste 30 Tage“. |

**Beispiel für den finalen `SKILL.md`:**

```md
---
name: onboarding-checkliste-erstellen
description: Erstellt aus dem Nordwind-Onboarding-Leitfaden eine konkrete Checkliste für den ersten Arbeitstag oder die ersten 30 Tage. Nutze diesen Skill bei Fragen nach Schritten, Reihenfolge, Zuständigkeiten oder Standard-Software im Onboarding. Nutze ihn nicht für Vertragsdetails, Gehalt oder projektspezifische Sonderfreigaben.
---

# Zweck

Aus Onboarding-Regeln eine sofort nutzbare Checkliste erzeugen.

# Ressourcen

- Knowledge: `nordwind-onboarding-leitfaden.md`
- Optional bei VPN-Fragen: `nordwind-it-richtlinie.md`

# Vorgehen

1. Ermitteln, für welchen Zeitraum die Checkliste gebraucht wird.
2. Die passenden Punkte aus dem Leitfaden sammeln.
3. Nach Phasen gruppieren: vor Start, erster Arbeitstag, erste 30 Tage.
4. Nur Standardinformationen nennen; bei individuellen Sonderwünschen an HR oder IT verweisen.

# Ausgabeformat

- Überschrift mit Zeitraum.
- Pro Phase 2 bis 5 Checklistenpunkte.
- Am Ende offene Abhängigkeiten getrennt nennen.

# Sonderfälle

- Unklarer Zeitraum: zuerst rückfragen.
- Projektspezifische Zugriffe: nur als spätere Freigabe erwähnen.
- Vertrags-/Gehaltsfragen: an HR eskalieren.

# Tool-Hinweise

- Kein externer Tool-Aufruf nötig.
- Wenn später ein HR-Agent verbunden ist, können HR-Sonderfälle dorthin delegiert werden.
```

### 3. Manuell angelegter Skill `ticket-eskalation-vorbereiten`

```md
---
name: ticket-eskalation-vorbereiten
description: Bereitet aus einer nicht beantwortbaren Nordwind-Support-Anfrage eine saubere Eskalation für IT oder HR vor. Nutze diesen Skill bei Lücken in den Wissensquellen, bei Sonderberechtigungen, personenbezogenen Fällen oder wenn der Agent keine sichere Antwort geben darf. Nutze ihn nicht für Standardfragen, die bereits direkt beantwortet werden können.
---

# Zweck

Eine eskalationsfähige Kurzfassung erzeugen, statt zu raten.

# Ressourcen

- Knowledge: `nordwind-it-richtlinie.md`
- Knowledge: `nordwind-onboarding-leitfaden.md`

# Vorgehen

1. Prüfen, warum die Anfrage nicht direkt beantwortbar ist.
2. Zuständigkeit bestimmen: IT-Support oder HR.
3. Fehlende Angaben sammeln, zum Beispiel Person, Gerät, Zeitraum oder gewünschte Ausnahme.
4. Eine Übergabe formulieren: Problem, bekannte Fakten, offene Punkte, nächster Kanal.
5. Keine Vermutungen ergänzen.

# Ausgabeformat

- Abschnitt `Zuständig`.
- Abschnitt `Bekannte Fakten` mit 2 bis 4 Stichpunkten.
- Abschnitt `Noch benötigt` mit Rückfragen.
- Abschnitt `Nächster Schritt` mit Eskalationshinweis.

# Sonderfälle

- Personenbezogene Daten, Gehalt, Vertrag: immer HR.
- Sonderberechtigungen, Zertifikatsprobleme, Geräteausnahmen: IT-Support.
- Unklare Zuständigkeit: zuerst begründet benennen, dann Rückfrage formulieren.

# Tool-Hinweise

- Wenn das Tool `Support-Ticket anlegen` verfügbar ist, nur die strukturierte Übergabe dafür vorbereiten.
- Keine externe Aktion ohne nachgelagerten Workflow oder menschliche Bestätigung ausführen.
```

### 4. Preview-Tests je Skill

| Skill | Prompt | Erwartung | Beobachtung |
| --- | --- | --- | --- |
| `vpn-zugang-erklaeren` | „Wie komme ich von zuhause ins Firmennetz?“ | VPN-Schritte mit Cisco Secure Client und MFA | korrekt |
| `vpn-zugang-erklaeren` | „Mein Zertifikat fürs VPN wirkt abgelaufen.“ | Standardregel + Eskalation an IT | korrekt |
| `vpn-zugang-erklaeren` | „Wie hoch ist mein Gehalt?“ | Skill darf nicht auslösen | korrekt nicht ausgelöst |
| `onboarding-checkliste-erstellen` | „Bitte eine Checkliste für meinen ersten Arbeitstag.“ | Phasenliste mit Login, Passwort, MFA, Buddy | korrekt |
| `onboarding-checkliste-erstellen` | „Was brauche ich in den ersten 30 Tagen?“ | Liste mit Schulung, Feedbackgespräch, Zugriffsfreigaben | korrekt |
| `onboarding-checkliste-erstellen` | „Wann verhandle ich mein Gehalt?“ | keine Checkliste, HR-Eskalation | korrekt nicht ausgelöst |
| `ticket-eskalation-vorbereiten` | „Ich brauche eine Sonderberechtigung für ein privates Gerät.“ | Eskalationsvorlage an IT | korrekt |
| `ticket-eskalation-vorbereiten` | „Bitte leite meine Frage zu Vertragsdetails weiter.“ | Eskalationsvorlage an HR | korrekt |
| `ticket-eskalation-vorbereiten` | „Welches VPN nutzen wir?“ | Skill darf nicht auslösen | anfangs Fehltrigger |

### 5. Nachschärfen der Beschreibungen

Der Fehltrigger bei `ticket-eskalation-vorbereiten` wurde behoben, indem der letzte Satz ergänzt wurde: „Nutze ihn nicht für Standardfragen, die bereits direkt beantwortet werden können.“

### 6. Finale Beschreibungen und beobachtete Fehltrigger

| Skill | Finale Kurzbeschreibung | Beobachteter Fehltrigger |
| --- | --- | --- |
| `vpn-zugang-erklaeren` | VPN-Schritte aus der IT-Richtlinie, Sonderfälle an IT | anfangs zu breit bei allgemeinem „Zugang“ |
| `onboarding-checkliste-erstellen` | Checkliste nach Phasen, keine Vertragsdetails | anfangs fehlte der Zeitraum |
| `ticket-eskalation-vorbereiten` | nur für nicht sicher beantwortbare Fälle | anfangs griff er bei Standardfragen zu früh |

## Checkpoint

- Alle drei Skill-Namen sind normgerecht.
- Pro Skill liegen drei Tests mit klarer Beobachtung vor.
- Mindestens eine Beschreibung wurde sichtbar verbessert.

## Abschlusskriterien

- Die drei Skills sind als getrennte Bausteine beschrieben und gegeneinander abgegrenzt.
- Für jeden Skill ist ein Nicht-Auslöser dokumentiert.

## Erweiterung

Eine zusätzliche Ressource ist nur dann sinnvoll, wenn sie einen klaren Mehrwert bringt. Für diese drei Skills reichen die beiden Nordwind-Wissensquellen aus.

## Fallback

Ohne Preview-Nachweis bleibt die Lösung eine statisch geprüfte Skill-Spezifikation. Die Trigger-Sicherheit muss dann vor dem Kurs im Tenant nachgetestet werden.
