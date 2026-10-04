# Lab 4.2 – Übung: Excel-Makros mit Copilot

**Ändert die Nordwind-Projektbasis?** Nein, es entsteht ein wiederverwendbares Werkzeug für den Budget-Report, keine inhaltliche Änderung am Projektstand.

## Ausgangslage

Der Budget-Report aus Lab 4.1 wird wöchentlich neu aufbereitet: Zahlen als Währung formatieren, negative Abweichungen rot markieren. Bisher macht das jemand von Hand.

Bereitgestellt in `output/project/`:

- `nordwind-budget-daten.xlsx` — die zu formatierende Tabelle als echte Excel-Arbeitsmappe (vorab eine Kopie anlegen, siehe Aufgabe 4)
- `nordwind-budget-daten.md` — dieselbe Tabelle als Textreferenz

## Aufgaben

1. Copilot eine konkrete Aufgabenbeschreibung geben: Spalten "Aug 2026", "Sep 2026" und "Summe" als Währung formatieren, Werte unter 0 € rot einfärben.
2. Den generierten VBA-Code Zeile für Zeile lesen und in eigenen Worten zusammenfassen, was er tut.
3. Copilot bitten, den Code für eine einzelne Zeile zu erklären, die unklar ist.
4. Das Makro an einer Kopie der Tabelle testen, nicht am Original.
5. Einen absichtlichen Fehler einbauen (z. B. einen falschen Spaltenbuchstaben) und Copilot bitten, die Fehlerursache zu erklären.

## Checkpoint

- Der generierte Code wurde gelesen und verstanden, nicht nur ausgeführt.
- Das Makro wurde zuerst an einer Kopie getestet.
- Die eingebaute Fehlerursache wurde korrekt identifiziert.

## Abschlusskriterien

- Ein lauffähiges Makro formatiert die Budget-Tabelle wie beschrieben.
- Eine kurze eigene Erklärung des Codes liegt vor.

## Erweiterung

Copilot bitten, dasselbe Makro so zu erweitern, dass es automatisch beim Öffnen der Datei läuft, und die Sicherheitsimplikation dieser Erweiterung benennen.

## Fallback

Ist die Makroausführung im Tenant deaktiviert: Copilot trotzdem den Code generieren und erklären lassen, als reine Lese- und Verständnisübung ohne Ausführung.
