# Lab 7.5 – Übung: Skills für den Nordwind Support-Agenten

**Ändert die Nordwind-Projektbasis?** Ja — der Nordwind Support-Agent erhält drei Skills als Baseline für die Labs 7.6 bis 7.9.

## Ausgangslage

Der Nordwind Support-Agent aus Lab 7.4 ist angelegt und nutzt bereits `nordwind-it-richtlinie.md` sowie `nordwind-onboarding-leitfaden.md` als Wissensquellen.

Ziel dieses Labs ist nicht mehr ein besserer System-Prompt, sondern ein modularer Agent mit drei getrennten Skills.

## Aufgaben

1. Im Bereich **Skills** den Entwurf aus Lab 7.2 als `SKILL.md` hochladen. Falls der Name noch nicht normgerecht ist, auf `vpn-zugang-erklaeren` anpassen.
2. Mit **Generate with AI** den Skill `onboarding-checkliste-erstellen` erzeugen. Die Rückfragen von Copilot vollständig beantworten und den erzeugten Entwurf prüfen.
3. Mit **Create from blank** den Skill `ticket-eskalation-vorbereiten` von Hand anlegen. Beschreibung, Schritte, Ausgabeformat und Sonderfälle vollständig eintragen.
4. Im Preview pro Skill drei Prompts testen: einen Standardfall, eine anders formulierte Variante und einen Fall, der den Skill nicht auslösen sollte.
5. Nach jedem Test die `description` gezielt nachschärfen, bis der passende Skill zuverlässig aktiviert wird und unpassende Fälle beim Agenten oder einer Eskalation bleiben.
6. Die drei finalen Skill-Beschreibungen sowie je ein beobachtetes Fehltrigger-Beispiel notieren.

## Checkpoint

- Alle drei Skill-Namen folgen der Regel `lowercase + numbers + hyphens only`.
- Für jeden Skill liegen drei Preview-Tests mit Beobachtung vor.
- Mindestens eine Beschreibung wurde nach einem Fehltrigger sichtbar verbessert.

## Abschlusskriterien

- Der Agent enthält die drei Skills `vpn-zugang-erklaeren`, `onboarding-checkliste-erstellen` und `ticket-eskalation-vorbereiten`.
- Pro Skill ist dokumentiert, wann er auslösen soll und wann ausdrücklich nicht.

## Erweiterung

Eine optionale Ressource ergänzen, etwa eine kleine Vorlage oder ein Beispieldokument, und prüfen, ob der Skill dadurch klarer oder nur schwerer wird.

## Fallback

Ohne Tenant-Zugriff: der Trainer-Demo folgen und auf Papier oder in einem Dokument pro Skill Name, Beschreibung, Schritte, Nicht-Auslöser und ein Fehltrigger-Beispiel festhalten. Einschränkung: kein echter Preview-Nachweis.
