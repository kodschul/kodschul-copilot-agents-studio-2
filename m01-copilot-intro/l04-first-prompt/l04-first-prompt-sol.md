# Lab 1.4 – Lösung: Erster Prompt für den Nordwind-Status

## Aufgaben

### 1. Knapper Prompt

```text
Schreib einen Statusbericht.
```

Erwartetes Ergebnis: ein Fließtext von etwa 150–300 Wörtern, allgemein gehalten, mit Platzhaltern oder erfundenen Projektdetails. Ohne Kontext kennt Copilot weder Projekt noch Adressat.

### 2. Ausgebauter Prompt

```text
Als Projektleiterin bei Nordwind Consulting: Verfasse einen Statusbericht zum Projekt
"Hafenmodernisierung" für den Lenkungsausschuss der Stadtwerke.

Grundlage sind die beigefügten Projektnotizen. Das Projekt läuft seit sechs Wochen.

Format: fünf Stichpunkte, maximal 100 Wörter insgesamt, sachlich, ohne Floskeln.
Der letzte Stichpunkt benennt die offenen Risiken.
```

Zuordnung der Bausteine:

| Baustein | Textstelle                                                             |
| -------- | ---------------------------------------------------------------------- |
| Rolle    | "Als Projektleiterin bei Nordwind Consulting"                          |
| Kontext  | Projektname, Adressat, Laufzeit, beigefügte Notizen                    |
| Aufgabe  | "Verfasse einen Statusbericht"                                         |
| Format   | fünf Stichpunkte, max. 100 Wörter, sachlich, Risiken als letzter Punkt |

Gültige Varianten: Rolle als "Projektleiter" oder "Beraterin"; Format als Tabelle statt Stichpunkten; Risiken als eigener Abschnitt statt letztem Punkt. Entscheidend ist, dass alle vier Bausteine besetzt sind.

### 3.–4. Unterschiede und Zuordnung

| Beobachteter Unterschied                                        | Baustein |
| --------------------------------------------------------------- | -------- |
| Ton ist sachlich statt werblich; keine Selbstlob-Formulierungen | Rolle    |
| Projektname, Kunde und Laufzeit sind korrekt statt Platzhalter  | Kontext  |
| Ergebnis ist ein Bericht, kein allgemeiner Text über Berichte   | Aufgabe  |
| Fünf Punkte statt Fließtext; Länge direkt passend               | Format   |
| Risiken sind enthalten statt zu fehlen                          | Format   |

Drei Unterschiede genügen. Nicht ausreichend: "besser", "professioneller" ohne Zuordnung.

### 5. Faktenprüfung

Prüfschritte gegen `nordwind-projektnotizen.md`:

| Prüfpunkt               | Typischer Befund                                                     |
| ----------------------- | -------------------------------------------------------------------- |
| Projektname und Kunde   | korrekt, weil im Prompt genannt                                      |
| Anzahl offener Punkte   | korrekt, wenn in den Notizen eindeutig; sonst zusammengefasst        |
| Zahlen und Prozentwerte | **häufigste Fehlerquelle** — gerundet, kombiniert oder frei ergänzt  |
| Namen von Beteiligten   | korrekt, sofern in den Notizen enthalten; sonst erfunden             |
| Termine und Fristen     | prüfpflichtig, besonders wenn in den Notizen mehrere Daten vorkommen |

Erwartetes Ergebnis: mindestens eine Abweichung bei Zahlen oder Formulierungsschärfe. Auch ein sauberer Durchlauf ohne Abweichung ist ein gültiges, dokumentiertes Prüfergebnis.

Versandfähigkeit: Nein, nicht ohne Durchsicht. Der Bericht ist ein Entwurf auf Vorlage-Niveau; Zahlen und Risikoformulierungen verantwortet die Projektleitung.

## Checkpoint

- Beide Prompts liegen im Wortlaut vor.
- Drei Unterschiede sind je einem Baustein zugeordnet.
- Die Faktenprüfung ist dokumentiert, mit oder ohne gefundene Abweichung.

## Erweiterung

Zweiter Durchlauf desselben Prompts:

| Bleibt gleich                                  | Ändert sich                                |
| ---------------------------------------------- | ------------------------------------------ |
| Struktur (fünf Punkte), Länge, Ton             | Wortwahl, Reihenfolge innerhalb der Punkte |
| enthaltene Fakten, sofern im Kontext vorhanden | Gewichtung und Formulierung der Risiken    |

Schlussfolgerung: Das Format ist steuerbar und stabil, der genaue Wortlaut nicht. Deshalb wird das Ergebnis geprüft, nicht der Prompt erneut optimiert.

## Fallback

Ohne Copilot-Zugriff: Die schriftliche Vorhersage je Variante wird mit der Trainer-Demo abgeglichen. Bewertungsmaßstab bleibt die Zuordnung der Unterschiede zu den vier Bausteinen.
