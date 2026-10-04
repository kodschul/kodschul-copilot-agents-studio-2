# Lab 3.1: Kundenangebot in Word

**Leitfragen:**

<details>
<summary>Wie gibt man Copilot in Word ein bestehendes Dokument als Grundlage mit?</summary>

Über den /-Befehl im Prompt-Feld: Datei auswählen, Copilot bezieht deren Inhalt in die Antwort ein.

</details>

<details>
<summary>Was passiert mit Formatierung und Struktur, wenn Copilot umschreibt?</summary>

Formatvorlagen der Vorlage bleiben meist erhalten, wenn im markierten Bereich gearbeitet wird. Bei Neuerstellung ganzer Abschnitte übernimmt Copilot eine eigene, oft abweichende Formatierung.

</details>

- Copilot in Word arbeitet auf dem, was referenziert wird, nicht auf einem leeren Blatt.
- Der /-Befehl macht den Unterschied zwischen einem generischen und einem passenden Entwurf.

## Referenzieren statt beschreiben

| Ansatz                              | Ergebnis                                                  |
| ----------------------------------- | --------------------------------------------------------- |
| Inhalt im Prompt frei beschreiben   | Copilot füllt Lücken mit Plausiblem, nicht mit Fakten     |
| Dokument per /-Befehl referenzieren | Copilot verwendet die tatsächlichen Angaben aus der Datei |

Der /-Befehl öffnet eine Dateiauswahl im Prompt-Feld von Word, Excel und PowerPoint; @-Erwähnungen bleiben Personen und Agenten in Teams/Copilot Chat vorbehalten.

![Screenshot of Copilot Chat in Word](https://support.microsoft.com/en-us/microsoft-365-copilot/media/copilot-word-chat.png)

_Quelle: Microsoft Support, "How Copilot Chat works in Microsoft 365 apps" (https://support.microsoft.com/en-us/microsoft-365-copilot/how-copilot-chat-works-in-microsoft-365-apps), abgerufen am 25.09.2026._

> **Merksatz:** Referenzieren schlägt Beschreiben — jede frei beschriebene Zahl ist eine potenzielle Erfindung.

## Stil- und Tonanpassung

| Steuerung          | Wirkung                                                   |
| ------------------ | --------------------------------------------------------- |
| Tonfall vorgeben   | "förmlich", "werblich", "sachlich-zurückhaltend"          |
| Zielgruppe nennen  | Fachpublikum vs. Entscheidungsebene verändert Detailtiefe |
| Länge begrenzen    | verhindert ausuferende Absätze bei offenen Anfragen       |
| Referenztext geben | ein Absatz im gewünschten Ton liefert das stärkste Signal |

## Ablauf für ein Kundenangebot

```
1. Angebotsvorlage referenzieren (/-Befehl)
2. Projektnotizen referenzieren (/-Befehl)
3. Auftrag mit Rolle, Adressat, Tonfall formulieren
4. Entwurf prüfen: stimmen Zahlen, Leistungsumfang, Fristen?
5. Nur den geprüften Teil in die Vorlage übernehmen
```

## Grenzen

- Der /-Befehl findet nur Dateien, die in OneDrive oder SharePoint liegen; eine lokal gespeicherte Datei muss vorher dorthin hochgeladen werden.
- Der /-Befehl ersetzt keine Faktenprüfung; Copilot kann Angaben aus der referenzierten Datei trotzdem falsch zusammenfassen.
- Sehr lange Referenzdokumente werden gekürzt verarbeitet; wichtige Details am Ende können fehlen.
- Rechtlich bindende Formulierungen (Zahlungsbedingungen, Haftung) bleiben Aufgabe der Fachabteilung.

## Fazit

- Der /-Befehl ist der wirksamste Hebel gegen erfundene Inhalte.
- Ton und Zielgruppe steuern die Wirkung stärker als lange Stilbeschreibungen.
- Der geprüfte Teil, nicht der Rohentwurf, geht in die Vorlage.

In der Übung entsteht ein Kundenangebot für Nordwind Consulting mit referenzierter Vorlage und referenzierten Projektnotizen.
