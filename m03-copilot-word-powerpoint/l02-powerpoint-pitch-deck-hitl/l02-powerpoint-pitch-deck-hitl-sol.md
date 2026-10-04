# Lab 3.2 – Lösung: Pitchdeck aus der HITL-Gliederung bauen

## Aufgaben

### 1.–3. Sortierung und Folienaufträge

Referenzfassung basiert auf einer neunteiligen Gliederung mit sechs belegten und drei nicht belegten Folien (Werte aus `l04-hitl-methodology-sol.md`).

Beispiel-Auftrag für eine belegte Folie:

```text
Erstelle eine Folie mit der Kernaussage "Die Ist-Analyse ist abgeschlossen, die
Anforderungserhebung läuft planmäßig". Nutze /nordwind-projektnotizen.md für die
konkreten Werte. Maximal 4 Bullet-Points, keine Fließtextabsätze.
```

Beispiel-Auftrag für eine nicht belegte Folie:

```text
Erstelle eine Platzhalterfolie mit dem Titel "Wirtschaftlichkeitsvergleich" und dem
Hinweis "Werte folgen nach Abstimmung mit dem Fachbereich Finanzen". Keine eigenen
Zahlen einsetzen oder schätzen.
```

### 4.–5. Foliensatz und Prüfung

| Folie                        | Kernaussage getroffen?    | Anmerkung                                                                          |
| ---------------------------- | ------------------------- | ---------------------------------------------------------------------------------- |
| Ausgangslage                 | ja                        | –                                                                                  |
| Projektstand                 | ja                        | Prozentwerte korrekt aus den Notizen übernommen                                    |
| Wirtschaftlichkeitsvergleich | Platzhalter wie gefordert | keine erfundenen Zahlen eingefügt                                                  |
| Zeitplan Anschlussphase      | teilweise                 | Copilot hatte einen Starttermin ergänzt, der nicht in den Notizen steht — entfernt |

### 6. Sprechnotiz

Eine angeforderte Sprechnotiz zur Folie "Projektstand" ergänzt Kontext zur Bedeutung der 70 %-Marke, den die Bullet-Points allein nicht liefern — als Nutzen bestätigt.

## Häufige Fehler

| Fehler                                               | Korrektur                                                                           |
| ---------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Alle Folien in einem Gesamtprompt erzeugt            | Einzelfolien-Prompts einhalten, sonst verwässert eine schwache Folie das ganze Deck |
| Nicht belegte Folie mit plausibler Schätzung gefüllt | Auftrag explizit auf Platzhalter umformulieren                                      |
| Sprechnotiz direkt auf die Folie geschrieben         | Sprechnotiz separat anfordern, Folie bleibt bullet-basiert                          |

## Checkpoint

- Foliensatz enthält exakt so viele Folien wie die Gliederung.
- Platzhalterfolien enthalten keine erfundenen Werte.
- Mindestens eine Folie wurde korrigiert, weil sie von der Kernaussage abwich.

## Erweiterung

Der One-Shot-Vergleich einer Einzelfolie zeigt meist: mehr Text, generischere Formulierungen, keine erkennbare Verbindung zur zuvor festgelegten Kernaussage.

## Fallback

Ohne PowerPoint-Copilot-Zugriff liefert die Markdown-Gliederung dieselbe inhaltliche Prüfung; nur die Layout-Übernahme in echte Folien entfällt und bleibt manuelle Nacharbeit.
