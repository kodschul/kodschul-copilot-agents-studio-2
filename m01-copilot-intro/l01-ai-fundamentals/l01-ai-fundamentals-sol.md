# Lab 1.0 – Lösung: Prompt, besserer Prompt oder Agent?

## Aufgaben

### 1. Zuordnung der fünf Szenarien

| #   | Szenario                                   | Stufe                         |
| --- | ------------------------------------------ | ----------------------------- |
| 1   | 40-seitiges Ausschreibungsdokument kürzen  | braucht einen besseren Prompt |
| 2   | Wöchentlich dieselben Reisekosten-Fragen   | braucht einen Agenten         |
| 3   | Absage an Bewerber, Ton stimmt nicht       | braucht einen besseren Prompt |
| 4   | Einmalig drei größte Kostenblöcke benennen | braucht nur einen Prompt      |
| 5   | Tägliche Fragen zur IT-Richtlinie          | braucht einen Agenten         |

### 2. Begründungen und tragendes Kriterium

| #   | Begründung                                                                             | Kriterium             |
| --- | -------------------------------------------------------------------------------------- | --------------------- |
| 1   | Einmalige Aufgabe, aber "wichtigste Anforderungen" ist ohne Bewertungsmaßstab beliebig | Qualitätsanspruch     |
| 2   | Immer dieselben Fragen, Antwort steht in einer stabilen Richtlinie                     | Wiederholung + Quelle |
| 3   | Einmalig, aber Ton, Adressat und Härtegrad müssen vorgegeben werden                    | Qualitätsanspruch     |
| 4   | Klar umrissen, einmalig, Ergebnis direkt prüfbar                                       | keine Wiederholung    |
| 5   | Tägliche Wiederholung, feste Wissensquelle, mehrere Fragende                           | Wiederholung + Quelle |

Entscheidungsregel: Agent erst, wenn **Wiederholung** und **stabile Wissensquelle** zusammenkommen. Fehlt eines von beidem, ist ein guter Prompt die richtige Antwort.

### 3. Fehlende Prompt-Angabe

Gültige Antworten für Szenario 1, jeweils konkret statt pauschal:

- der Bewertungsmaßstab: "wichtig" gemessen woran — Vertragsrisiko, Aufwand oder Ausschlusskriterium?
- die Rolle: aus Sicht des Angebotsteams oder der Rechtsabteilung?
- das Format: drei Stichpunkte, Tabelle oder Fließtext, mit oder ohne Seitenverweis?

Für Szenario 3 analog: Tonalität (wertschätzend, formell), Länge, ob ein Feedbackangebot enthalten sein soll.

Nicht ausreichend: "mehr Kontext geben", "präziser formulieren" — das benennt keine konkrete Angabe.

### 4. Eigenes Szenario

Individuelle Lösung. Tragfähig ist die Einordnung, wenn die Begründung auf Wiederholung, Wissensquelle oder Qualitätsanspruch verweist und nicht auf "das klingt kompliziert".

Typische Fehleinordnungen und Korrektur:

| Fehleinordnung                              | Korrektur                                                                     |
| ------------------------------------------- | ----------------------------------------------------------------------------- |
| Komplexe Einmalanalyse → Agent              | Komplexität allein rechtfertigt keinen Agenten; entscheidend ist Wiederholung |
| Häufige Aufgabe ohne stabile Quelle → Agent | Ohne verlässliche Wissensbasis liefert der Agent wiederholt Falsches          |
| Alles außer Trivialem → "besserer Prompt"   | Bei täglicher Wiederholung durch mehrere Personen lohnt der Agent             |

## Checkpoint

- Sechs Zeilen (fünf vorgegebene plus eine eigene) sind zugeordnet und begründet.
- Mindestens eine konkrete fehlende Prompt-Angabe ist benannt, keine Pauschalformulierung.

## Erweiterung

Für ein Reisekosten- oder IT-Richtlinien-Szenario:

| Frage                      | Antwort                                                                        |
| -------------------------- | ------------------------------------------------------------------------------ |
| Welche Wissensquelle?      | die freigegebene, aktuelle Richtlinie als Dokument                             |
| Wer pflegt sie?            | die fachlich verantwortliche Abteilung, nicht die Person, die den Agenten baut |
| Was passiert bei Änderung? | Quelle aktualisieren und Agentenantworten stichprobenartig nachprüfen          |

Dieser Punkt wird in Lab 7.9 (Agent-Governance) systematisch aufgegriffen.
