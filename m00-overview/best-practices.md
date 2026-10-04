# Best Practices

Übergreifende Merksätze aus den Modulen, gebündelt für den schnellen Rückblick.

## Prompting & Human-in-the-Loop

- Ein Prompt ohne Rolle, Ziel, Kontext und Format liefert einen plausiblen, aber oft nicht
  passenden Entwurf — nicht die endgültige Antwort.
- Jedes KI-generierte Zwischenergebnis wird vor der finalen Nutzung von einem Menschen geprüft,
  besonders bei Zahlen, Namen und Fristen.
- Referenziere vorhandene Dokumente per /-Befehl (Word/Excel), statt ihren Inhalt im Prompt neu zu beschreiben.

## Agenten bauen (The Nextise Agentic Way)

- Erst das Problem verstehen, dann die Lösung konzipieren, erst dann bauen — nicht "KI, bau mir einen Agenten".
- Wähle den kleinsten Harness, der die Aufgabe trägt: ein mächtigerer Harness kann ein einfaches
  Problem "überarbeiten" und kostet dann nur mehr Credits und Zeit.
- Der Harness wird beim Anlegen des Agenten gewählt und lässt sich später nicht wechseln.
- Skills klein und fokussiert halten (max. 5–6 prozessabhängige Skills pro Agent); die
  **Beschreibung** entscheidet, ob der Skill zur richtigen Zeit geladen wird.
- Ein Skill gehört in die Skill-Datei, allgemeines Verhalten in die Instruktionen, Daten in Knowledge, Aktionen in Tools.
- Ein System-Prompt braucht eine klare Eskalationsregel für Fragen außerhalb der Wissensquelle.
- Workflows für alles, was immer gleich ablaufen muss; der Agent entscheidet, *wann* er den Workflow aufruft.
- Bei irreversiblen Aktionen eine menschliche Freigabe in den Workflow einbauen.

## Testen & Betrieb

- Nach jedem neuen Skill, Tool oder Connected Agent im Preview-Tab testen, bevor man weiterbaut.
- Vor Veröffentlichung ein Testset (Evaluate) mit normalen Fragen **und** Grenzfällen laufen lassen.
- Bauen, Testen und Evaluieren verbrauchen Copilot Credits — Limit und Verantwortliche vorab festlegen.

## Governance

- Jeder Skill, jede MCP-Verbindung und jeder Connected Agent ist zusätzliche Verhaltens- bzw. Zugriffsfläche
  und braucht dieselbe Freigabeprüfung wie ein Konnektor.
- Vor Veröffentlichung: Freigabeprozess und Berechtigungsprüfung, nicht nur ein einzelner erfolgreicher Test.
- Jeder Agent hat einen Verantwortlichen, einen Review-Turnus und ein Abschaltkriterium.
