# Lab 4.1 – Übung: Budget-Analyse in Excel

**Ändert die Nordwind-Projektbasis?** Ja, die Analyseergebnisse dienen als Kostenübersicht für das Nordwind-Angebot.

## Ausgangslage

Die Budget-Tabelle des laufenden Nordwind-Projekts liegt vor: Auftragsvolumen 184.000 €, bisher verbraucht 71.500 € über fünf Kostenblöcke und zwei Monate.

Bereitgestellt in `output/project/`:

- `nordwind-budget-daten.xlsx` — die Tabelle als echte Excel-Arbeitsmappe (Kostenblock, Aug 2026, Sep 2026, Summe), direkt mit Copilot in Excel öffnen
- `nordwind-budget-daten.md` — dieselbe Tabelle als Textreferenz
- `nordwind-projektnotizen.md` — Auftragsvolumen und Gesamtverbrauch als Referenzwerte

## Aufgaben

1. `nordwind-budget-daten.xlsx` öffnen und die vorhandene Struktur prüfen (Kostenblock, Aug 2026, Sep 2026, Summe).
2. Copilot bitten, für jeden Kostenblock die Summe über beide Monate zu berechnen, und die vorgeschlagene Formel gegen die bereits vorhandene Kontrollsumme prüfen.
3. Copilot fragen, welcher Kostenblock am stärksten gestiegen ist, und das Ergebnis von Hand gegen die Rohdaten gegenrechnen.
4. Copilot um einen Diagrammvorschlag für die Verteilung der Kostenblöcke bitten.
5. Die verbleibende Restsumme (Auftragsvolumen minus Gesamtverbrauch) berechnen lassen und gegen den in `nordwind-projektnotizen.md` genannten Wert (112.500 €) prüfen.

## Checkpoint

- Jede Formel wurde vor der Übernahme gegen eine Kontrollsumme geprüft, nicht nur das Ergebnis übernommen.
- Die berechnete Restsumme stimmt mit dem Referenzwert überein.
- Der vorgeschlagene Diagrammtyp passt zur Fragestellung (Verteilung, nicht Zeitverlauf).

## Abschlusskriterien

- Alle fünf Kostenblöcke sind mit korrekter Summenformel hinterlegt.
- Der stärkste Kostenanstieg ist benannt und begründet.
- Ein Diagramm zur Kostenverteilung liegt vor.

## Erweiterung

Copilot bitten, den Anteil jedes Kostenblocks am Gesamtverbrauch in Prozent auszurechnen, und prüfen, ob sich die Prozentwerte zu 100 % summieren.

## Fallback

Steht kein Excel mit aktiviertem Copilot zur Verfügung: die Tabelle in Copilot Chat als Text einfügen und dieselben Fragen dort stellen. Einschränkung: kein direkt einsetzbares Diagramm, nur eine textliche Diagrammempfehlung.
