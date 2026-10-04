---
theme: default
layout: default
---

# Lab 6.2: Meeting-Recap in Teams

**Leitfragen:**

<details>
<summary>Was muss aktiviert sein, damit Copilot ein Meeting zusammenfassen kann?</summary>

Aufzeichnung bzw. Transkription muss für das Meeting aktiviert und von allen Teilnehmenden zugelassen worden sein — ohne Transkript hat Copilot keine Grundlage für eine Zusammenfassung.

</details>

<details>
<summary>Wie zuverlässig sind die erkannten Aktionspunkte?</summary>

Sie sind ein guter erster Entwurf, aber keine verlässliche Vollständigkeitsgarantie — implizit vereinbarte oder nebenbei erwähnte Aufgaben werden leicht übersehen und müssen gegengeprüft werden.

</details>

<details>
<summary>Was ist bei Transkription rechtlich/organisatorisch zu beachten?</summary>

Alle Teilnehmenden müssen vorab informiert werden bzw. zustimmen; bei Kundenmeetings ist das explizit anzukündigen, nicht stillschweigend zu aktivieren.

</details>

- Copilot in Teams fasst ein Meeting aus dem Transkript zusammen, wenn Aufzeichnung/Transkription aktiviert war.
- Erkannte Aktionspunkte sind ein Entwurf, keine geprüfte Aufgabenliste.

## Was Copilot in Teams-Meetings kann

| Funktion             | Voraussetzung                       | Ergebnis                                        |
| -------------------- | ----------------------------------- | ----------------------------------------------- |
| Live-Zusammenfassung | laufende Aufzeichnung/Transkription | Kernpunkte während oder direkt nach dem Meeting |
| Aktionspunkte        | laufende Aufzeichnung/Transkription | Liste vorgeschlagener Aufgaben mit Zuordnung    |
| Nacharbeitung        | vorhandene Aufzeichnung             | Zusammenfassung auch für nicht Anwesende        |

## Aktivierung und Voraussetzung

- Aufzeichnung/Transkription muss vor oder zu Beginn des Meetings gestartet werden.
- Alle Teilnehmenden werden auf die Aktivierung hingewiesen (Hinweisbanner in Teams reicht nicht als alleinige Information bei externen Kundenmeetings).
- Ohne Transkript keine Zusammenfassung — eine nachträgliche Aktivierung wirkt nicht rückwirkend.

> **Merksatz:** Copilot fasst zusammen, was aufgezeichnet wurde — nicht, was im Meeting eigentlich gemeint war.

## Zuverlässigkeit der Aktionspunkte

- Explizit ausgesprochene Zusagen ("ich kümmere mich darum") werden meist korrekt erkannt.
- Implizite oder beiläufig erwähnte Aufgaben werden häufig übersehen.
- Jede erkannte Aktion braucht eine kurze Gegenprüfung durch eine Person, die im Meeting war.

## Rechtliche/organisatorische Aspekte

- Zustimmung aller Teilnehmenden zur Aufzeichnung, insbesondere bei Kundenmeetings, vorab einholen.
- Aufbewahrungsdauer und Zugriff auf Transkript/Aufzeichnung nach den Vorgaben des Unternehmens klären.
- Bei sensiblen Themen (z. B. Konflikten, personenbezogenen Bewertungen) Aufzeichnung bewusst nicht aktivieren.

## Grenzen

- Eine Zusammenfassung ersetzt keine Protokollpflicht mit rechtlicher Verbindlichkeit.
- Sprecherzuordnung und Aktionspunkte können bei überlappendem Sprechen fehlerhaft sein.

## Fazit

- Ohne aktivierte Aufzeichnung/Transkription gibt es keine Zusammenfassung.
- Aktionspunkte sind ein Entwurf und werden von einer im Meeting anwesenden Person geprüft.
- Zustimmung zur Aufzeichnung wird vorab eingeholt, nicht stillschweigend vorausgesetzt.

Die Übung bereitet das Kickoff-Meeting mit den Stadtwerken Nordhafen vor und fasst es zusammen.

## Ausblick: Microsoft Graph Connectors

Outlook und Teams liefern Copilot Inhalte aus M365-eigenen Quellen (Mails, Dateien, Meetings). Für Wissen aus **externen** Line-of-Business-Systemen (z. B. ein CRM oder Ticketsystem außerhalb von M365) bindet man stattdessen einen **Microsoft Graph Connector** an — er indiziert externe Inhalte, sodass Copilot sie durchsuchbar in seine Antworten einbeziehen kann. Einrichtung und Berechtigungsmodell eines Graph Connectors sind Admin-Aufgaben (Microsoft 365 Admin Center) und werden in diesem Kurs nicht praktisch konfiguriert, nur eingeordnet.
