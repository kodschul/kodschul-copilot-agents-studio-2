# Hintergrund: Ausblick Makro-Agent

- Ein Makro-Agent nähme eine Aufgabenbeschreibung wie einen Prompt entgegen und baute daraus automatisiert ein passendes Makro.
- Fortgeschrittener, zukünftiger Anwendungsfall mit Bezug zu Modul 7 (Agents) — heute Diskussion, keine Umsetzung.

## Was ein Makro-Agent leisten müsste

| Anforderung                          | Grund                                                        |
| ------------------------------------ | ------------------------------------------------------------ |
| Feste Wissensquelle (z. B. Vorlagen) | wiederkehrende Aufgaben statt einmaliger Prompt-Formulierung |
| Freigabeschritt vor Ausführung       | automatisch generierter Code darf nicht ungeprüft laufen     |
| Protokollierung jeder Änderung       | Nachvollziehbarkeit bei automatisierten Eingriffen           |
| Begrenzter Zugriffsbereich           | kein Zugriff auf Dateien/Bereiche außerhalb der Aufgabe      |

## Leitfragen für die Diskussion

1. Was müsste ein solcher Agent können, damit man ihm wiederkehrende Automatisierungen anvertraut?
2. Welche Freigabe- und Prüfschritte bräuchte er im Unternehmen, bevor ein generiertes Makro auf Echtdaten läuft?

> **Merksatz:** Dieselbe Prüfpflicht wie in Lab 4.2, nur mit einem Agenten statt einem einzelnen Prompt als Auslöser.
