# Lab 2.1: Prompt-Grundlagen und die 6-Punkte-Checkliste

**Leitfragen:**

<details>
<summary>Warum scheitert der knappe Auftrag, obwohl er scheinbar eindeutig ist?</summary>

Er ist nur für Eingeweihte eindeutig. Die Teamstandards zu Format, Gliederung und Ablage stehen nirgends im Auftrag, sie sind implizites Hauswissen.

</details>

<details>
<summary>Welcher der sechs Punkte fehlt in eigenen Prompts am häufigsten?</summary>

Struktur und Beispiele. Klarheit und Aufgabe werden meist mitgeliefert, Format und Referenzmuster fast nie.

</details>

- Ein knapper Auftrag an einen neuen Kollegen und derselbe Auftrag an Copilot scheitern aus demselben Grund: fehlende Angaben.
- Daraus ergibt sich eine Checkliste, die jeden Prompt prüfbar macht.

## Die Ausgangsgeschichte

Ein neuer Kollege bekommt den Auftrag: _"Fass uns bitte das heutige Meeting zusammen."_

| Was er liefert            | Was das Team erwartet hätte                                      |
| ------------------------- | ---------------------------------------------------------------- |
| dreiseitiger Fließtext    | Stichpunkte mit kurzen Erklärungen                               |
| chronologisch             | nach Kategorien: Entscheidungen, offene Punkte, nächste Schritte |
| als Word-Datei per E-Mail | einheitlich formatiert im gemeinsamen Teams-Ordner               |

Der Auftrag war nicht falsch formuliert. Er war unvollständig — und niemand hat das gemerkt, bis das Ergebnis vorlag.

> **Merksatz:** Genau wie ein neuer Kollege braucht Copilot klare Anweisungen. Implizites Hauswissen ist für beide unsichtbar.

## Die 6-Punkte-Checkliste

| #   | Punkt                | Prüffrage                                                   | Beispiel                                                                      |
| --- | -------------------- | ----------------------------------------------------------- | ----------------------------------------------------------------------------- |
| 1   | Klarheit             | Ist die Aufgabe eindeutig und nachvollziehbar formuliert?   | "Erstelle eine Liste mit fünf Vorteilen von X gegenüber Y"                    |
| 2   | Kontext              | Rolle, Zielgruppe, System, Anwendungsfall genannt?          | "Ich bin Projektmanager und bereite eine Präsentation für Führungskräfte vor" |
| 3   | Fokus                | Was ist das Hauptziel der Anfrage?                          | "Ziel ist es, den Effizienzgewinn im Support aufzuzeigen"                     |
| 4   | Struktur             | Format und Umfang festgelegt?                               | "Tabellenform, drei Spalten, maximal fünf Einträge"                           |
| 5   | Sprachstil           | Ton und Sprachebene vorgegeben?                             | "freundlich und professionell, ohne unnötige Floskeln"                        |
| 6   | Beispiele/Referenzen | Ein Muster für die gewünschte Antwortstruktur mitgeliefert? | "Ich erwarte Einträge wie: _Titel – kurze Erklärung_"                         |

Die Punkte 1–3 sagen, **was** entstehen soll. Die Punkte 4–6 sagen, **wie** es aussehen soll. Die meisten unbrauchbaren Ergebnisse scheitern an 4–6.

## Vom Auftrag zur Anweisung

| Vorher                                         | Nachher                                                                                                                                                                                                                                |
| ---------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "Fass uns bitte das heutige Meeting zusammen." | "Fasse das heutige Meeting zusammen. Verwende Aufzählungspunkte mit kurzen, prägnanten Erklärungen. Gliedere nach: Entscheidungen (fett), offene Punkte (kursiv), nächste Schritte. Sortiere innerhalb der Kategorien nach Priorität." |

## Grenzen

- Die Checkliste macht einen Prompt vollständig, nicht automatisch richtig — falscher Kontext bleibt falsch.
- Nicht jeder Punkt ist in jedem Prompt nötig; bei einer Routineanfrage genügen oft 1, 3 und 4.
- Ein sehr langer Prompt mit widersprüchlichen Angaben ist schlechter als ein kurzer, konsistenter.

## Fazit

- Der Prompt scheitert an dem, was im Kopf bleibt statt im Text zu stehen.
- Punkte 1–3 definieren das Was, Punkte 4–6 das Wie — und 4–6 werden am häufigsten vergessen.
- Ein Muster mitzugeben (Punkt 6) ersetzt drei Sätze Formatbeschreibung.

In der Übung wird der knappe Meeting-Prompt aus der Geschichte anhand der Checkliste ausgebaut und das Ergebnis gegen den Ausgangsprompt gestellt.
