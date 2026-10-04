# Lab 5.1 – Lösung: Komplexes Chat-Szenario

## Aufgaben

### 1. Einordnung

```text
Ich hänge unsere Projektnotizen zu "Hafenmodernisierung" an. Die Stadtwerke Nordhafen fragen an,
ob eine Team-Schulung Teil des laufenden Projekts sein könnte oder ein separates Angebot bräuchte.
Ordne das anhand von Leistungsumfang und Laufzeit aus den Notizen ein.
```

Erwartetes Ergebnis: eine Einschätzung, die zwischen "im Rahmen" und "separates Angebot" unterscheidet, mit Verweis auf den in den Notizen definierten Leistungsumfang.

### 2. Zeit- und Kostenrahmen

```text
Basierend auf der vorigen Einschätzung: Skizziere einen groben Zeit- und Kostenrahmen für die
Schulung, unter Berücksichtigung der verbleibenden Restsumme aus der Budget-Tabelle (Anhang).
```

Erwartetes Ergebnis: eine grobe Spanne, die explizit auf die Restsumme (112.500 €) Bezug nimmt, keine erfundene Festzahl ohne Verankerung an den Daten.

### 3. Argumentation für den Jour fixe

```text
Formuliere daraus eine sachliche Drei-Satz-Argumentation für den Jour fixe: Passt die Schulung
ins Projekt, was würde sie ungefähr kosten, was ist der nächste Schritt?
```

Beispielergebnis: "Die Schulung liegt inhaltlich außerhalb des aktuellen Leistungsumfangs und würde als Zusatzangebot laufen. Angesichts der verbleibenden Restsumme ist ein kleiner, zeitlich begrenzter Rahmen realistisch. Ein separates Kurzangebot wird bis zum nächsten Jour fixe vorbereitet."

### 4.–5. Vergleich mit neu gestartetem Verlauf

Derselbe Prompt aus Aufgabe 3 ohne vorherigen Verlauf liefert typischerweise eine generische Argumentation ohne Bezug zu Projektnamen, Restsumme oder Leistungsumfang, da diese Fakten nicht mehr im Kontext stehen.

| Fortgeführter Verlauf                       | Neu gestarteter Verlauf                        |
| ------------------------------------------- | ---------------------------------------------- |
| nennt Restsumme und Leistungsumfang konkret | bleibt allgemein, ohne Zahlenbezug             |
| Argumentation passt zum realen Projektstand | Argumentation ist plausibel, aber austauschbar |

Der fehlende Kontext zeigt sich als fehlender Zahlen- und Sachbezug, nicht als offensichtlicher Fehler — das macht den Effekt im Alltag leicht übersehbar.

## Checkpoint

- Alle drei Prompts liegen im selben Verlauf vor.
- Der Unterschied ist am fehlenden Zahlen-/Sachbezug im neuen Verlauf festgemacht.
- Die Kostenaussage wurde gegen 112.500 € geprüft.

## Erweiterung

Ein einziger langer Prompt mit allen drei Anforderungen liefert meist ein brauchbares, aber weniger präzises Ergebnis: einzelne Teilfragen werden knapper beantwortet, weil Copilot alle Anforderungen gleichzeitig gewichten muss. Schrittweises Vorgehen erlaubt, jede Teilantwort einzeln zu prüfen, bevor die nächste darauf aufbaut.
