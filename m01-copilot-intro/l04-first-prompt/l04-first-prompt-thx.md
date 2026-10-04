# Lab 1.4: Der erste eigene Prompt

**Leitfragen:**

<details>
<summary>Welche vier Bausteine gehören in jeden brauchbaren Prompt?</summary>

Rolle, Kontext, Aufgabe, Format.

</details>

<details>
<summary>Was passiert, wenn man das Ausgabeformat nicht vorgibt?</summary>

Das Modell wählt selbst — meist Fließtext in mittlerer Länge. Das Ergebnis ist nicht falsch, aber selten direkt verwendbar.

</details>

- Ein Prompt funktioniert wie eine Arbeitsanweisung an eine neue Kollegin, die den Hauskontext nicht kennt.
- Vier Bausteine gehören in jede brauchbare Anweisung.

## Die vier Bausteine

| Baustein | Frage                                | Beispiel                                                |
| -------- | ------------------------------------ | ------------------------------------------------------- |
| Rolle    | Aus wessen Sicht wird geschrieben?   | "als Projektleiterin bei Nordwind Consulting"           |
| Kontext  | Was muss man wissen, um es zu lösen? | "Projekt läuft seit sechs Wochen, Kunde ist Stadtwerke" |
| Aufgabe  | Was genau soll entstehen?            | "Statusbericht für den Lenkungsausschuss"               |
| Format   | Wie soll das Ergebnis aussehen?      | "fünf Stichpunkte, maximal 100 Wörter, ohne Floskeln"   |

## Vorher / Nachher

| Variante | Prompt                                                                                                                                                                                                                           |
| -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Vorher   | "Schreib einen Statusbericht."                                                                                                                                                                                                   |
| Nachher  | "Als Projektleiterin bei Nordwind Consulting: Verfasse einen Statusbericht für den Lenkungsausschuss des Kunden Stadtwerke. Fünf Stichpunkte, maximal 100 Wörter, sachlich, ohne Floskeln. Schließe mit einem Punkt zu Risiken." |

Der zweite Prompt ist länger. Genau das ist der Punkt: Die Zeit, die in die Formulierung fließt, spart Überarbeitungsrunden.

![The visual representation of the prompt framework with examples: goal+context+tone+data](https://support.microsoft.com/en-us/microsoft-365-copilot/media/prompt-framework.png)

> **Merksatz:** Was im Prompt nicht steht, entscheidet das Modell selbst — und zwar ohne Rückfrage.

## Typische Lücken

| Fehlt   | Sichtbare Folge                                     |
| ------- | --------------------------------------------------- |
| Rolle   | unpassender Ton, mal zu locker, mal zu behördlich   |
| Kontext | generische Aussagen ohne Projektbezug               |
| Aufgabe | Thema statt Ergebnis, der Text kreist               |
| Format  | Fließtext mittlerer Länge, muss erst gekürzt werden |

## Grenzen

- Ein guter Prompt erzeugt keine Fakten, die nicht vorliegen — fehlt der Kontext, bleibt die Antwort allgemein.
- Zahlen im Ergebnis stammen aus dem bereitgestellten Material oder sind erfunden; beides sieht gleich aus.
- Auch ein perfekter Prompt liefert bei zwei Durchläufen zwei unterschiedliche Formulierungen.

## Fazit

- Rolle, Kontext, Aufgabe, Format: vier Bausteine, die jede Anweisung tragen.
- Jede fehlende Angabe wird vom Modell stillschweigend selbst entschieden.
- Ein längerer Prompt ist kein Mehraufwand, sondern vorgezogene Überarbeitung.

In der Übung entsteht der erste eigene Prompt für eine Status-Zusammenfassung bei Nordwind Consulting.
