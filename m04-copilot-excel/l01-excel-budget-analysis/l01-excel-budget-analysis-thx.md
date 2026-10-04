# Lab 4.1: Budget-Analyse in Excel

**Leitfragen:**

<details>
<summary>Welche Datenstruktur braucht Copilot in Excel, damit es überhaupt sinnvoll arbeiten kann?</summary>

Eine Tabelle mit klaren Spaltenüberschriften und einem Wert pro Zelle. Verbundene Zellen, mehrere Werte pro Zelle oder freie Kommentarspalten erschweren die Auswertung erheblich.

</details>

<details>
<summary>Wie prüft man eine von Copilot vorgeschlagene Formel?</summary>

Gegen eine bekannte Kontrollsumme rechnen (z. B. eine bereits vorhandene Zeilen- oder Spaltensumme) und die Formel selbst lesen, nicht nur das Ergebnis übernehmen.

</details>

- Copilot in Excel arbeitet auf einer sauberen Tabellenstruktur, nicht auf freiem Text.
- Formeln erklären und Diagramme vorschlagen ja, komplexe Automatisierung nein.

## Was Copilot in Excel kann

| Fähigkeit                | Beispiel                                                |
| ------------------------ | ------------------------------------------------------- |
| Formeln erklären         | "Was macht diese SUMMEWENN-Formel in Zelle D5?"         |
| Formeln vorschlagen      | "Berechne die Summe je Kostenblock über beide Monate."  |
| Muster in Daten erkennen | "Welcher Kostenblock ist am stärksten gestiegen?"       |
| Diagrammvorschläge       | "Schlage ein passendes Diagramm für diese Tabelle vor." |

## Was Copilot in Excel nicht kann

- Komplexe Automatisierung wiederkehrender Abläufe ohne Makro/VBA-Unterstützung (siehe Lab 4.2).
- Verlässliche Aussagen über Daten außerhalb der geöffneten Tabelle.
- Fehlerfreie Formeln bei uneinheitlicher oder unsauberer Tabellenstruktur.

## Von der Frage zur Formel

```
Frage in Worten formulieren
   →  Copilot schlägt Formel vor
   →  Formel gegen eine Kontrollsumme prüfen
   →  erst dann übernehmen
```

![Screenshot of Copilot Chat in Excel](https://support.microsoft.com/en-us/microsoft-365-copilot/media/copilot-excel-chat.png)

_Quelle: Microsoft Support, "How Copilot Chat works in Microsoft 365 apps" (https://support.microsoft.com/en-us/microsoft-365-copilot/how-copilot-chat-works-in-microsoft-365-apps), abgerufen am 25.09.2026._

> **Merksatz:** Eine plausible Formel ist nicht automatisch eine korrekte Formel.

## Grenzen

- Copilot sieht nur die geöffnete Tabelle, keine verknüpften externen Dateien.
- Bei großen Tabellen werden nicht immer alle Zeilen einbezogen; das Ergebnis muss gegen die tatsächliche Zeilenzahl geprüft werden.
- Diagrammvorschläge sind Vorschläge, keine automatische Auswahl des einzig richtigen Diagrammtyps.

## Fazit

- Eine saubere Tabellenstruktur ist die Voraussetzung, nicht optional.
- Jede vorgeschlagene Formel wird gegen eine bekannte Kontrollsumme geprüft.
- Copilot liefert Analyse und Vorschläge, die Entscheidung über Darstellung bleibt beim Menschen.

In der Übung wird die Budget-Tabelle des Nordwind-Angebots mit Copilot analysiert.
