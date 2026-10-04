---
theme: default
layout: default
---

# Lab 7.8: Testen, Evaluieren, Überwachen

Ein gebauter Agent ist noch kein belastbarer Agent. Dieses Lab trennt manuelle Preview-Tests, wiederholbare Evaluationsläufe und laufende Beobachtung nach der Veröffentlichung.

**Leitfragen:**

<details>
<summary>Was misst ein Testset, was Preview nicht misst?</summary>

Ein Testset macht Antworten über mehrere feste Fälle vergleichbar und wiederholbar. Preview ist stark für Exploration, aber nicht für systematische Qualitätstrends.

</details>

<details>
<summary>Woran erkennt man Credit-Verschwendung?</summary>

Wenn aufwendige Skills, Tools oder Delegationen für einfache Fragen anspringen oder eine zweite Runde keinen messbaren Qualitätsgewinn bringt.

</details>

<details>
<summary>Was zeigt Monitor erst nach der Veröffentlichung?</summary>

Sessions, Ergebnisse und Credit-Nutzung aus echter Nutzung des veröffentlichten Agenten, nicht nur aus dem Bau- oder Preview-Kontext.

</details>

- Preview ist der schnelle Dialogtest.
- Evaluate macht Qualität über feste Testfälle vergleichbar.
- Monitor zeigt laufende Nutzung und Ergebnisse erst nach der Veröffentlichung.

## Drei Prüfmodi im Vergleich

| Modus | Zweck | Gute Frage |
| --- | --- | --- |
| Preview | Verhalten explorativ prüfen | „Wie reagiert der Agent auf diese Formulierung?“ |
| Evaluate | Testset wiederholt ausführen | „Wird derselbe Qualitätsstandard über mehrere Fälle erreicht?“ |
| Monitor | produktive Sessions und Outcomes beobachten | „Was passiert nach der Veröffentlichung in echten Anfragen?“ |

## Was in ein Testset gehört

| Falltyp | Beispiel |
| --- | --- |
| Normalfall | VPN-Frage aus der IT-Richtlinie |
| Variantenfall | gleiche Absicht, andere Formulierung |
| Grenzfall | außerhalb des Zwecks |
| Schutzfall | personenbezogene oder sensible Daten |

## Verbesserungshebel nach einer Evaluation

| Hebel | Wann sinnvoll |
| --- | --- |
| Skill-Beschreibung schärfen | falscher Trigger oder Fehltrigger |
| Instructions präzisieren | Ton, Grenzen oder Eskalationsregel unklar |
| Skill-Body nachschärfen | korrekter Trigger, aber schwache Arbeitslogik |
| Tool-Beschreibung prüfen | unnötiger Workflow- oder MCP-Aufruf |

> **Merksatz:** Preview findet Ideen. Evaluate vergleicht Qualität. Monitor zeigt das echte Leben.

## Nordwind-Szenario

Der Agent verfügt jetzt über Skills, Workflow und optionale Delegation. Vor einer Freigabe muss sichtbar werden, ob einfache Fragen leicht bleiben und kritische Fälle zuverlässig eskalieren.

## Grenzen

- Ein Testset ersetzt keine echte Produktion, sondern reduziert Überraschungen vor der Veröffentlichung.
- Monitor zeigt Produktionsdaten erst nach Nutzung des veröffentlichten Agenten.
- Bauen, Testen und Evaluieren verbrauchen Copilot Credits.

## Fazit

- Preview, Evaluate und Monitor lösen unterschiedliche Qualitätsfragen.
- Ein gutes Testset mischt Normal-, Varianten-, Grenz- und Schutzfälle.
- Verbesserungen sollten am kleinsten wirksamen Hebel ansetzen.

Die Übung legt ein Testset mit fünf Nordwind-Fragen an, verbessert die schwächste Antwort und vergleicht zwei Evaluationsläufe.
