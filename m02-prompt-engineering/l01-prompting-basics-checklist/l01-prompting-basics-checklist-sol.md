# Lab 2.1 – Lösung: Den Meeting-Prompt ausbauen

## Aufgaben

### 1. Knapper Prompt

```text
Fasse das Meeting zusammen.
```

Erwartetes Ergebnis: chronologischer Fließtext, der dem Protokollverlauf folgt. Entscheidungen und offene Punkte stehen vermischt im Text. Länge meist 200–350 Wörter.

### 2. Abweichungen vom Teamstandard

| #   | Abweichung                                                                 |
| --- | -------------------------------------------------------------------------- |
| 1   | Fließtext statt Aufzählungspunkten                                         |
| 2   | Chronologisch statt nach Entscheidungen / offene Punkte / nächste Schritte |
| 3   | Keine Priorisierung innerhalb der Themen                                   |
| 4   | Länge über der halben Seite                                                |
| 5   | Zusagen ohne benannte Verantwortliche übernommen                           |

Drei Abweichungen genügen. Nicht ausreichend: "zu lang und unstrukturiert" ohne konkrete Benennung.

### 3. Checkliste ausgefüllt

| #   | Punkt      | Eintrag                                                                                                                                 |
| --- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Klarheit   | "Fasse das Protokoll des Jour fixe vom 11.09.2026 zusammen"                                                                             |
| 2   | Kontext    | "Als Projektleiterin bei Nordwind Consulting, Adressat ist das interne Projektteam"                                                     |
| 3   | Fokus      | "Ziel: Das Team erkennt in einer Minute, was entschieden ist und was offen bleibt"                                                      |
| 4   | Struktur   | "Aufzählungspunkte, gegliedert nach Entscheidungen / offene Punkte / nächste Schritte; innerhalb nach Priorität; max. eine halbe Seite" |
| 5   | Sprachstil | "sachlich, knapp, ohne Floskeln"                                                                                                        |
| 6   | Beispiele  | "Format je Eintrag: _Thema – Kernaussage in einem Satz – verantwortlich_"                                                               |

Gültige Variante: Punkt 5 als "nicht nötig, weil der Teamstandard den Ton bereits vorgibt" kennzeichnen. Diese begründete Auslassung ist zulässig.

Zusammengesetzter Prompt:

```text
Als Projektleiterin bei Nordwind Consulting: Fasse das beigefügte Protokoll des Jour fixe
vom 11.09.2026 (Projekt Hafenmodernisierung) für das interne Projektteam zusammen.

Ziel: Das Team erkennt in unter einer Minute, was entschieden wurde und was offen ist.

Struktur: Aufzählungspunkte, gegliedert nach
  1. Entscheidungen
  2. Offene Punkte
  3. Nächste Schritte
Innerhalb jeder Kategorie nach Priorität sortieren. Insgesamt maximal eine halbe Seite.

Format je Eintrag: Thema – Kernaussage in einem Satz – verantwortlich.
Sachlich und knapp, ohne Floskeln.
```

### 4. Ergebnis des ausgebauten Prompts

Erwartetes Ergebnis: drei Überschriften mit je zwei bis vier Stichpunkten, jeder im Muster "Thema – Aussage – verantwortlich".

| Standard                      | Erfüllt?                                                               |
| ----------------------------- | ---------------------------------------------------------------------- |
| Stichpunktform                | ja                                                                     |
| Gliederung in drei Kategorien | ja                                                                     |
| Priorisierung                 | meist ja, aber die Reihenfolge ist begründungsbedürftig                |
| Länge                         | ja                                                                     |
| Verantwortliche benannt       | nur wo im Protokoll vorhanden; sonst bleibt das Feld leer oder geraten |

### 5. Gegenüberstellung

| Abweichung aus Aufgabe 2 | Nach dem Ausbau          | Ursache der Restabweichung             |
| ------------------------ | ------------------------ | -------------------------------------- |
| 1 Fließtext              | behoben                  | —                                      |
| 2 Chronologisch          | behoben                  | —                                      |
| 3 Keine Priorisierung    | teilweise behoben        | Prompt (Priorisierungskriterium fehlt) |
| 4 Zu lang                | behoben                  | —                                      |
| 5 Verantwortliche fehlen | besteht teilweise weiter | Rohprotokoll (Zusagen ohne Namen)      |

Die entscheidende Erkenntnis: Abweichung 5 lässt sich nicht durch einen besseren Prompt lösen. Fehlt die Information in der Quelle, erfindet Copilot sie oder lässt sie weg. Abweichung 3 dagegen ist ein Prompt-Problem — "nach Priorität" ohne Maßstab ist genauso unbestimmt wie der Ausgangsauftrag.

## Häufige Fehler

| Fehler                                                  | Korrektur                                                         |
| ------------------------------------------------------- | ----------------------------------------------------------------- |
| Alle sechs Punkte pflichtgemäß befüllt, auch redundante | Begründete Auslassung ist besser als ein widersprüchlicher Zusatz |
| "nach Priorität" ohne Maßstab übernommen                | Maßstab nennen: Risiko, Frist oder Blockadewirkung                |
| Fehlende Verantwortliche dem Prompt angelastet          | Prüfen, ob die Information überhaupt in der Quelle steht          |

## Checkpoint

- Die Abweichungsliste aus Aufgabe 2 enthält mindestens drei konkrete Punkte, keine Pauschalurteile.
- Die Checkliste aus Aufgabe 3 ist für alle sechs Punkte ausgefüllt oder begründet leer.
- Beide erzeugten Zusammenfassungen liegen vor und sind vergleichbar.

## Erweiterung

| Variante             | Beobachtetes Ergebnis                                                            |
| -------------------- | -------------------------------------------------------------------------------- |
| ohne Beispieleintrag | Struktur stimmt, aber die Einträge sind unterschiedlich lang und aufgebaut       |
| mit Beispieleintrag  | alle Einträge folgen demselben Muster, Verantwortliche stehen an gleicher Stelle |

Punkt 6 ersetzt damit mehrere Sätze Formatbeschreibung: Ein Muster wirkt stärker als dessen Beschreibung.
