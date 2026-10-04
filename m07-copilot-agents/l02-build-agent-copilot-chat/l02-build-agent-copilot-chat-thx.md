---
theme: default
layout: default
---

# Lab 7.2: Agent in Copilot Chat bauen

Der Copilot-Chat-Harness erweitert Microsoft Copilot Chat um Unternehmenswissen und eignet sich für einen schnellen internen Wissensagenten. Dieses Lab erzeugt den ersten lauffähigen Nordwind Support-Agenten samt wiederverwendbaren Prompt- und Skill-Artefakten.

**Leitfragen:**

<details>
<summary>Welche drei Angaben braucht ein Agent mindestens?</summary>

Ein klarer Zweck, belastbare Instruktionen und mindestens eine Wissensquelle bilden den kleinsten sinnvollen Start. Ohne diese drei Teile bleibt das Verhalten zu beliebig.

</details>

<details>
<summary>Wie lässt sich prüfen, ob der Agent wirklich die Wissensquelle nutzt?</summary>

Die Testfrage muss eine Information verlangen, die nur in den bereitgestellten Nordwind-Dokumenten steht. Korrekt ist die Antwort nur dann, wenn genau diese Information wieder auftaucht oder sauber eskaliert wird.

</details>

<details>
<summary>Was verändert die Assistenten-Kette gegenüber einem One-Shot-Prompt?</summary>

Sie trennt Problem, Architektur und Formulierung in drei Schritte. Dadurch entstehen präzisere Regeln, bessere Testfälle und wiederverwendbare Skill-Entwürfe statt eines pauschalen Textblocks.

</details>

## Copilot-Chat-Harness im Kurskontext

| Aspekt | Bedeutung |
| --- | --- |
| Zweck | Microsoft Copilot Chat um Unternehmenswissen erweitern |
| Stärke | schneller interner Wissensagent mit wenig Aufbauaufwand |
| Veröffentlichung | intern für Teams |
| Abrechnung | verbrauchsbasiert oder im Microsoft-365-Copilot-Lizenzumfang enthalten |

Die konkrete Oberfläche des No-Code Agent Builders ist tenantabhängig. Bezeichnungen und verfügbare Optionen daher **vor Kursbeginn im Tenant prüfen**.

## Aus der Assistenten-Kette werden Bauartefakte

| Artefakt | Vorgabe im Kurs |
| --- | --- |
| Agentenname | **Nordwind Support-Agent** |
| Wissensquellen | `../../project/nordwind-it-richtlinie.md`, `../../project/nordwind-onboarding-leitfaden.md` |
| System-Prompt | finalisierte Fassung aus Assistent 3 |
| Skill-Entwurf 1 | `vpn-zugang-erklaeren` |
| Skill-Entwurf 2 | `onboarding-checkliste-erstellen` |
| Skill-Entwurf 3 | `ticket-eskalation-vorbereiten` |

Die drei Skill-Entwürfe werden in diesem Lab nur erzeugt und dokumentiert. Das eigentliche Hinzufügen als Skills folgt erst in Lab 7.5.

## Minimaler Agentenaufbau

| Baustein | Erwartung für Nordwind |
| --- | --- |
| Zweck | beantwortet IT- und Onboarding-Standardfragen |
| Instruktionen | nutzt nur die Nordwind-Quellen, antwortet knapp, eskaliert Sonderfälle |
| Wissen | IT-Richtlinie und Onboarding-Leitfaden |

## Testfragen vor dem Bauen

| Testfrage | Erwartetes Verhalten |
| --- | --- |
| „Welches VPN nutzen wir bei Nordwind?“ | nennt Cisco Secure Client und verweist auf die IT-Richtlinie |
| „Was passiert am ersten Arbeitstag?“ | greift Schritte aus dem Onboarding-Leitfaden auf |
| „Wie hoch ist die Gehaltsbandbreite meiner Position?“ | verweist an HR statt zu spekulieren |

> **Merksatz:** Erst das Übergabepaket schärfen, dann den Agenten anlegen — sonst wird aus einer Idee nur ein ungetesteter Prompt.

## Grenzen in diesem Lab

- Der Copilot-Chat-Harness löst hier den Wissensfall, nicht die späteren Workflow- oder Tool-Fragen.
- Workflows und externe Tools werden bewusst erst in Lab 7.6 ergänzt.
- Skill-Entwürfe sind in diesem Schritt nur Vorlagen; ihre Auslösung wird erst nach dem Upload in Lab 7.5 sichtbar.

## Fazit

- Für den ersten Nordwind-Prototyp reichen Zweck, Instruktionen und Wissen als Kern aus.
- Die Assistenten-Kette liefert neben dem System-Prompt schon die drei Skill-Entwürfe für den weiteren Ausbau.
- Gute Testfragen trennen echte Grounding-Antworten von plausibel klingenden Vermutungen.

Die Übung erzeugt Konzept, Prompt und Skill-Entwürfe und baut daraus den Nordwind Support-Agenten im Copilot-Chat-Harness.
