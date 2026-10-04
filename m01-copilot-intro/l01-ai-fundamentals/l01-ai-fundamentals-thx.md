# Lab 1.0: KI- und Prompting-Grundlagen

In diesem Abschnitt geht es um die praktische Konsequenz aus Teil 1 (`l01-ai-fundamentals-grundlagen.md`): Prompting, Modell-Aktivierung und die Frage, wann ein Agent gebraucht wird.

**Leitfragen:**

<details>
<summary>Was macht ein Sprachmodell eigentlich, wenn es "antwortet"?</summary>

Es sagt Wort für Wort (genauer: Token für Token) die statistisch plausibelste Fortsetzung voraus. Es schlägt nach, versteht aber nicht im menschlichen Sinn.

</details>

<details>
<summary>Warum verändert ein besserer Prompt das Ergebnis so stark?</summary>

Der Prompt ist die einzige Steuerung. Er legt fest, welcher Teil des gelernten Sprachraums aktiviert wird — Rolle, Kontext und Format grenzen die plausiblen Fortsetzungen ein.

</details>

<details>
<summary>Wann reicht ein Prompt nicht mehr und man braucht einen Agenten?</summary>

Wenn dieselbe Aufgabe wiederholt anfällt, eine feste Wissensquelle braucht und von mehreren Personen genutzt werden soll.

</details>

- Ein Sprachmodell sagt Token für Token die plausibelste Fortsetzung voraus.
- Die Formulierung einer Anfrage steuert dieses Ergebnis.
- Ab einem gewissen Punkt reicht ein einzelner Prompt nicht mehr, dann braucht es einen Agenten.

## Begriffe

| Begriff | Bedeutung                                                                     |
| ------- | ----------------------------------------------------------------------------- |
| Prompt  | die Eingabe, die das Modell steuert                                           |
| Kontext | alles, was dem Modell zusätzlich zur Frage vorliegt (Anhänge, Verlauf, Rolle) |
| Agent   | vorkonfigurierter Assistent mit festem Zweck und fester Wissensbasis          |

> **Merksatz:** Ein Sprachmodell liefert die wahrscheinlichste, nicht die richtige Antwort. Die Prüfung bleibt beim Menschen.

## Modell-Aktivierung: warum Präzision wirkt

| Prompt                                      | Aktivierter Sprachraum                        | Ergebnis            |
| ------------------------------------------- | --------------------------------------------- | ------------------- |
| "Schreib was über Projekte"                 | alles, was je über Projekte geschrieben wurde | beliebig, generisch |
| "Schreib als Projektleiterin an den Kunden" | Rolle + Adressat grenzen ein                  | brauchbarer Ton     |
| ... "in fünf Stichpunkten, ohne Floskeln"   | zusätzlich Format und Stil                    | direkt verwendbar   |

![The visual representation of the prompt framework with examples: goal+context+tone+data](https://support.microsoft.com/en-us/microsoft-365-copilot/media/prompt-framework.png)

## Drei Stufen der Automatisierung

| Stufe            | Beschreibung                                    | Beispiel                                    |
| ---------------- | ----------------------------------------------- | ------------------------------------------- |
| Einzelner Prompt | einmalige Aufgabe, Ergebnis wird direkt genutzt | "Fasse dieses Protokoll zusammen"           |
| Besserer Prompt  | dieselbe Aufgabe, aber präzise gesteuert        | Rolle, Format, Umfang und Beispiel mitgeben |
| Agent            | wiederkehrende Aufgabe mit fester Wissensquelle | interner Assistent für Onboarding-Fragen    |

## Grenzen

- Kein Zugriff auf Wissen außerhalb von Training, Prompt und freigegebenen Datenquellen.
- Keine Garantie für Reproduzierbarkeit: gleicher Prompt, leicht andere Antwort.
- Zahlen, Zitate und Quellenangaben sind besonders anfällig für Halluzinationen.

## Fazit

- Ein Sprachmodell sagt Text vorher, es recherchiert und prüft nicht.
- Der Prompt ist die einzige Steuerung; Rolle, Kontext und Format sind die wirksamsten Hebel.
- Ein Agent lohnt sich erst bei Wiederholung plus fester Wissensbasis.

In der Übung werden fünf Alltagsszenarien den drei Stufen zugeordnet.
