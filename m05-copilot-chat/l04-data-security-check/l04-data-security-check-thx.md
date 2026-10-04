---
theme: default
layout: default
---

# Lab 5.4: Datensicherheit im Chat

**Leitfragen:**

<details>
<summary>Welche Daten dürfen Sie anhängen und welche nicht?</summary>

Interne Arbeitsdaten mit eigener Berechtigung dürfen im angemeldeten Arbeit-Modus verwendet werden. Kundendaten Dritter, Geheimhaltungspflichtiges und Daten ohne eigene Berechtigung gehören nicht in den Chat.

</details>

<details>
<summary>Was ändert sich sicherheitstechnisch zwischen angemeldetem und nicht angemeldetem Chat?</summary>

Angemeldet greift der Unternehmensdatenschutz: Eingaben fließen nicht ins Modelltraining und bleiben in der eigenen Umgebung. Nicht angemeldet gilt der Chat wie ein öffentlicher Dienst.

</details>

<details>
<summary>An wen eskalieren Sie im Zweifelsfall?</summary>

An die interne Datenschutz- oder IT-Sicherheitsstelle, bevor eine unklare Angabe angehängt oder eingegeben wird.

</details>

- Nicht jede Information gehört in einen Prompt, unabhängig davon, wie hilfreich die Antwort wäre.
- Der Anmeldestatus (Modul 1) und der Web-/Arbeit-Modus entscheiden zusätzlich, wie ein angehängter Inhalt behandelt wird.

## Datenkategorien bei Nordwind

| Kategorie                            | Chat-tauglich?                       |
| ------------------------------------ | ------------------------------------ |
| eigene Arbeitsdokumente (berechtigt) | ja, im angemeldeten Arbeit-Modus     |
| Kundendaten Dritter                  | nein                                 |
| vertrauliche Vertragsinhalte         | nein, außer ausdrücklich freigegeben |
| öffentlich verfügbare Informationen  | ja, auch im Web-Modus                |

> **[SCREENSHOT-PLATZHALTER – Quelle erforderlich]** UI-Pfad: Copilot Chat → Anmeldestatus-Anzeige und Web-/Arbeit-Umschalter mit Hinweis auf Unternehmensdatenschutz. Ersetzen durch eigene anonymisierte Sandbox-Aufnahme (mit Aufnahmedatum) oder offizielle Microsoft-Learn-Abbildung (mit Quelle und Datum).

> **Merksatz:** Berechtigung plus Anmeldestatus entscheidet, nicht die Nützlichkeit der Antwort.

## Ablauf eines Datensicherheits-Checks

1. Datenkategorie der geplanten Eingabe bestimmen (siehe Tabelle).
2. Anmeldestatus und Modus (Web/Arbeit) prüfen.
3. Bei Unsicherheit: nicht eingeben, sondern eskalieren.

## Grenzen

- Eine Lizenz allein erlaubt keinen Zugriff auf nicht berechtigte Inhalte (siehe Modul 1, Lab 1.2).
- Eine einmal eingegebene, unzulässige Angabe lässt sich nicht rückwirkend "zurückholen".

## Fazit

- Datenkategorie und Anmeldestatus entscheiden gemeinsam, nicht die Nützlichkeit der Antwort.
- Im Zweifel gilt: nicht eingeben, sondern eskalieren.
- Ein Datensicherheits-Check läuft in drei festen Schritten ab.

Die Übung wendet diesen Check auf das eigene Szenario aus Lab 5.1 an.
