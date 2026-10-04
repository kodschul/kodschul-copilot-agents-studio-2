# Lab 7.2 – Übung: Agent in Copilot Chat bauen

**Ändert die Nordwind-Projektbasis?** Ja — der Nordwind Support-Agent bildet die Baseline für Lab 7.4 und liefert die Skill-Entwürfe für Lab 7.5.

## Ausgangslage

Die Top-1-Empfehlung aus Lab 7.1 liegt vor: ein interner Support-Agent für IT- und Onboarding-Standardfragen bei Nordwind. Als Wissensquellen stehen bereit:

- `../../project/nordwind-it-richtlinie.md`
- `../../project/nordwind-onboarding-leitfaden.md`

## Aufgaben

1. Die Top-1-Empfehlung an **Assistent 2 „Solution Architect“** aus dem [Anhang: Assistenten-Prompts](../anhang-assistenten-prompts.md) übergeben und das Kurzkonzept mit maximal 5–6 Skill-Kandidaten, Ablauf und Risiken erzeugen.
2. Aus diesem Übergabepaket mit **Assistent 3 „Skill-/System-Prompt-Generator“** einen finalen System-Prompt sowie genau drei Skill-Entwürfe mit diesen Namen erzeugen: `vpn-zugang-erklaeren`, `onboarding-checkliste-erstellen`, `ticket-eskalation-vorbereiten`. Die Beschreibungen der Skills bleiben auf Deutsch.
3. Den System-Prompt mit mindestens drei Fragen testen: VPN-Frage, Onboarding-Frage und Grenzfall außerhalb des Zwecks. Den Prompt nur dort nachschärfen, wo die Tests einen Fehler zeigen.
4. Den Agenten **Nordwind Support-Agent** im Copilot-Chat-Harness anlegen, die zwei Nordwind-Dokumente als Wissen ergänzen und den finalen System-Prompt als Instruktionsbasis übernehmen.
5. Den Agenten erneut mit den drei Testfragen prüfen und die drei Skill-Entwürfe so dokumentieren, dass sie in Lab 7.5 hochgeladen werden können. Workflows und externe Tools bleiben in diesem Lab bewusst außen vor; dazu folgt nur der Vorgriff auf Lab 7.6.

## Checkpoint

- Das Kurzkonzept aus Assistent 2 bleibt bei höchstens 5–6 Skill-Kandidaten.
- Aus Assistent 3 liegen ein System-Prompt und genau drei Skill-Entwürfe mit den geforderten Namen vor.
- Der angelegte Agent beantwortet mindestens eine Wissensfrage belastbar aus den Nordwind-Quellen und eskaliert die Grenzfrage sauber.

## Abschlusskriterien

- Der **Nordwind Support-Agent** ist im Copilot-Chat-Harness angelegt oder vollständig dokumentiert.
- Die drei Skill-Entwürfe liegen konsistent benannt für Lab 7.5 bereit.
- Die Testnotizen zeigen, welche Prompt-Anpassung aus realen Beobachtungen entstanden ist.

## Erweiterung

Eine vierte Testfrage formulieren, die mehrere Informationsstücke kombiniert, etwa VPN plus Erstlogin, und die Grenzen des ersten Prompt-Entwurfs dokumentieren.

## Fallback

Ohne eigenen Builder- oder Tenant-Zugang: der Trainer-Demo folgen, System-Prompt und Skill-Entwürfe trotzdem erzeugen und die spätere Agent-Konfiguration in einer Tabelle dokumentieren. Einschränkung: kein eigener Lauf im Harness und kein eigener Preview-Test.
