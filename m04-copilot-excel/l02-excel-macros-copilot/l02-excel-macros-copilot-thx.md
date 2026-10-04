# Lab 4.2: Excel-Makros mit Copilot

**Leitfragen:**

<details>
<summary>Was ist ein Makro und wann lohnt es sich überhaupt?</summary>

Ein Makro ist eine aufgezeichnete oder programmierte Befehlsfolge (VBA), die eine wiederkehrende Aufgabe automatisch ausführt. Es lohnt sich ab der zweiten oder dritten identischen Wiederholung, nicht für einen einmaligen Handgriff.

</details>

<details>
<summary>Wie beschreibt man Copilot eine Automatisierungsaufgabe so, dass brauchbarer Code entsteht?</summary>

Konkret: welche Zellen/Bereiche, welcher Auslöser, welches Ergebnis. "Formatiere den Report" ist zu vage; "Formatiere Spalte D als Währung und färbe negative Werte rot" ist konkret genug.

</details>

<details>
<summary>Warum darf man ein generiertes Makro nicht ungeprüft auf Echtdaten laufen lassen?</summary>

Ein Makro verändert Daten automatisch und ohne Rückfrage. Ein Fehler im Code wirkt sich sofort auf alle betroffenen Zellen aus, ein manueller Schritt lässt sich dagegen einzeln stoppen und korrigieren.

</details>

<details>
<summary>Excel hat doch schon einen Makro-Rekorder — wozu dann Copilot?</summary>

Der Rekorder zeichnet nur exakt die geklickten Schritte mit festen Zellbezügen auf, ohne Bedingungen. Sobald eine Bedingung oder ein variabler Bereich gebraucht wird, ist der Prompt an Copilot schneller als Aufzeichnen plus manuelles Nachbearbeiten im Code.

</details>

- Ein Makro automatisiert eine wiederkehrende Aufgabe, ein einmaliger Handgriff braucht keins.
- Copilot kann Makros erstellen, erklären und beim Debuggen helfen, aber nicht ungeprüft auf Echtdaten laufen lassen.

## Vom Prompt zum Makro

```
Aufgabe konkret beschreiben (Bereich, Auslöser, Ergebnis)
   →  Copilot generiert VBA-Code
   →  Code lesen und in einer Kopie der Datei testen
   →  erst danach auf der Originaldatei ausführen
```

## Makro-Rekorder vs. Copilot-generierter Code

Excel bringt einen eingebauten Makro-Rekorder mit: Aufzeichnung starten, die Schritte einmal von Hand ausführen, Aufzeichnung stoppen — daraus entsteht VBA-Code.

| Makro-Rekorder                                                                     | Copilot-generierter Code                                                           |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| zeichnet exakt die geklickten Schritte auf, nichts darüber hinaus                  | entsteht aus einer Beschreibung, ohne die Schritte selbst auszuführen              |
| feste Zellbezüge (z. B. immer `B2:D6`), bricht bei anderer Zeilenzahl              | kann mit Bedingungen und variablen Bereichen umgehen, wenn das mitbeschrieben wird |
| keine Bedingungen ("wenn negativ, dann rot") ohne manuelle Nachbearbeitung im Code | Bedingungen wie "färbe negative Werte rot" direkt im Prompt formulierbar           |
| für einmalige, immer gleich ablaufende Klickfolgen geeignet                        | schneller bei allem, was Logik statt reiner Klickwiederholung braucht              |

Der Rekorder bleibt sinnvoll für sehr einfache, stets identische Klickfolgen ohne jede Bedingung. Sobald eine Bedingung, ein variabler Bereich oder eine Erklärung des Codes gebraucht wird, ist der Prompt an Copilot schneller als Aufzeichnen plus manuelles Nachbearbeiten.

**So findet man den generierten Code:** über Entwicklertools → Visual Basic (VBA-Editor); Copilot liefert den Code direkt im Chat zum Einfügen.

## Was Copilot beim Makro kann

| Aufgabe         | Beispiel                                                        |
| --------------- | --------------------------------------------------------------- |
| Makro erstellen | "Schreibe ein Makro, das Spalte D als Währung formatiert."      |
| Makro erklären  | "Was macht dieses Makro Zeile für Zeile?"                       |
| Makro debuggen  | "Dieses Makro wirft einen Fehler in Zeile 12, woran liegt das?" |

## Grenzen

- Makros/VBA laufen nur in der Excel-Desktop-App, nicht in Excel für das Web.
- Generierter VBA-Code muss vor der Ausführung gelesen und verstanden werden, nicht nur ausgeführt.
- Makros mit Zugriff auf externe Dateien oder das Dateisystem bergen ein höheres Risiko als reine Formatierungsmakros.
- Ohne aktivierte Makrosicherheit im Tenant lässt sich ein Makro gar nicht erst ausführen; das ist Absicht, keine Fehlfunktion.

## Fazit

- Ein Makro lohnt sich erst bei echter Wiederholung.
- Die Aufgabenbeschreibung entscheidet über die Codequalität, nicht das Modell.
- Der Makro-Rekorder reicht für einfache, immer gleiche Klickfolgen; bei Bedingungen oder variablen Bereichen ist Copilot schneller.
- Jedes generierte Makro wird erst an einer Kopie getestet, nie direkt an Echtdaten.

In der Übung erstellt Copilot ein einfaches Makro für eine wiederkehrende Nordwind-Aufgabe.
