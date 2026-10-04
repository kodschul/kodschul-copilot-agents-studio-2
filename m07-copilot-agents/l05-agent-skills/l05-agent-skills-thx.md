---
theme: default
layout: default
---

# Lab 7.5: Skills: Agentenwissen als Baustein

Skills kapseln wiederverwendbares Agentenverhalten. Dieses Lab zeigt, wie der Nordwind Support-Agent drei kleine, klar auslösbare Skills erhält.

**Leitfragen:**

<details>
<summary>Woran entscheidet der Agent, einen Skill zu laden?</summary>

Vor allem an der Beschreibung und daran, ob die Nutzeranfrage genau zu Zweck, Grenzen und Format des Skills passt.

</details>

<details>
<summary>Wann ist ein Skill passender als eine allgemeine Instruktion?</summary>

Wenn ein wiederholbarer Teilauftrag eigene Schritte, Sonderfälle oder ein eigenes Ausgabeformat braucht, ohne die Kerninstruktionen aufzublähen.

</details>

<details>
<summary>Warum bleiben gute Skills klein und fokussiert?</summary>

Kleine Skills triggern zuverlässiger, lassen sich leichter testen und erzeugen weniger Nebeneffekte als ein Sammel-Skill für alles.

</details>

- Ein Skill besteht aus `name`, `description`, Markdown-Anweisungen und optionalen Ressourcen.
- Der GitHub-Copilot-Harness lädt nur den gerade benötigten Skill-Kontext nach; das ist der Kern von Progressive Disclosure.

## Skill-Anatomie

| Baustein | Aufgabe | Gute Ausprägung |
| --- | --- | --- |
| `name` | technische Kennung | kurz, eindeutig, nur Kleinbuchstaben/Zahlen/Bindestriche |
| `description` | Aktivierungssignal | beschreibt Anlass, Zweck, Grenzen und Zielausgabe |
| Markdown-Anweisungen | Arbeitslogik | nummerierte Schritte, Format, Fehlerfälle |
| Ressourcen | Zusatzkontext | Richtlinie, Vorlage, Beispiele, nur wenn wirklich nötig |

## Komponenten sauber trennen

| Komponente | Wofür gedacht | Typische Frage |
| --- | --- | --- |
| Instructions | Grundrolle, Stil, Eskalationsregeln | „Wie verhält sich der Agent immer?“ |
| Knowledge | Faktenbasis und Dokumente | „Worauf grounded die Antwort?“ |
| Tools | Aktionen über Flows, Konnektoren oder MCP | „Was darf der Agent ausführen?“ |
| Skills | wiederverwendbarer Teilauftrag | „Welcher abgegrenzte Job wird gerade gelöst?“ |

## Progressive Disclosure in der Praxis

Die Nordwind-Wissensquellen enthalten viele Details zu VPN, Onboarding und Eskalation. Ein Skill zieht nur den Teil heran, der zur Anfrage passt, statt jede Regel immer in die globalen Instructions zu kopieren.

> **Merksatz:** Nicht mehr globale Instruktionen schreiben, sondern wiederkehrende Teilaufgaben als kleine Skills paketieren.

## Gute und schlechte Skill-Beschreibungen

| Variante | Beispiel | Wirkung |
| --- | --- | --- |
| zu breit | „Hilft bei Supportfragen.“ | triggert unklar, konkurriert mit fast jeder Anfrage |
| zu technisch | „Antwortet mit Markdown über Netzwerkanbindung.“ | beschreibt Form, aber nicht den fachlichen Anlass |
| gut | „Erklärt den Nordwind-VPN-Zugang Schritt für Schritt auf Basis der IT-Richtlinie und eskaliert Sonderfälle an den IT-Support.“ | nennt Anlass, Quelle, Ergebnis und Grenze |

## Drei Wege im Lab

| Weg | Zweck im Lab | Typischer Nutzen |
| --- | --- | --- |
| Upload a Skill | vorhandenen Entwurf übernehmen | schnelles Reuse eines bereits erarbeiteten `SKILL.md` |
| Generate with AI | aus einer Beschreibung starten | gute Wahl für die erste Fassung plus Rückfragen |
| Create from blank | Verhalten bewusst von Hand bauen | maximale Kontrolle über Beschreibung und Schritte |

## Mini-Demo: Trigger absichern

1. Anfrage: „Wie richte ich VPN auf dem Firmenlaptop ein?“
2. Erwartung: `vpn-zugang-erklaeren` wird aktiv, nennt Cisco Secure Client, Verbindungsziel und MFA.
3. Gegenprobe: „Wie hoch ist mein Gehalt?“ darf den Skill nicht laden, sondern muss eskalieren.

## Nordwind-Szenario

Der Support-Agent aus Lab 7.4 beantwortet schon Standardfragen. Jetzt werden drei Teilaufgaben sauber ausgelagert: VPN erklären, Onboarding-Checkliste erstellen und Eskalation vorbereiten.

## Grenzen

- Eine schwache `description` wird durch gute Schritte im Body nicht kompensiert; der Skill muss zuerst zuverlässig triggern.
- Zu große Skills werden schwer testbar und konkurrieren mit den globalen Instructions.
- UI-Beschriftungen können im Tenant leicht abweichen; Produktfakten stammen aus Microsoft Learn, Stand 04.10.2026.

## Fazit

- Skills sind wiederverwendbare, markdownbasierte Fähigkeitsbausteine.
- Die Beschreibung steuert die Aktivierung, nicht nur der Dateiname.
- Kleine Skills mit klarer Grenze sind leichter zu testen und zu pflegen.

Die Übung ergänzt den Nordwind Support-Agenten um drei Skills und schärft deren Beschreibungen im Preview-Test nach.
