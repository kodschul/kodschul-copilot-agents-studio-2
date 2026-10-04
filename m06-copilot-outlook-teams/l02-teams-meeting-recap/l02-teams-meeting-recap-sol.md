# Lab 6.2 – Lösung: Meeting-Recap in Teams

## Aufgaben

### 1. Simulierter Gesprächsverlauf (Auszug)

```text
Brandt eröffnet, verweist auf die Mail vom Vortag. Sievers bestätigt, dass die Freigabe von AP2
diese Woche im Fachbereich angesprochen wird, nennt aber weiterhin keinen festen Termin.
Frage zum Testsystemzugang: Sievers sagt zu, den Antrag intern zu beschleunigen, sobald er von
der Nordwind-Seite gestellt ist. Okonkwo bestätigt, dass der Antrag diese Woche rausgeht.
Kurze Diskussion, ob ein fester Termin für die AP2-Freigabe im Protokoll festgehalten werden
sollte — Sievers möchte das noch nicht zusagen. Brandt schlägt vor, in zwei Wochen nachzufragen.
```

### 2. Strukturierte Zusammenfassung (Prompt und Ergebnis)

```text
Fasse diesen Gesprächsverlauf strukturiert zusammen: Teilnehmende, Kernpunkte, Aktionspunkte mit
Verantwortlichkeit.
```

| Aktionspunkt                              | Verantwortlich | Quelle im Verlauf                           |
| ----------------------------------------- | -------------- | ------------------------------------------- |
| Antrag Testsystemzugang stellen           | Okonkwo        | explizit zugesagt ("geht diese Woche raus") |
| AP2-Freigabe im Fachbereich ansprechen    | Sievers        | explizit zugesagt                           |
| Nachfrage zur AP2-Freigabe in zwei Wochen | Brandt         | explizit vorgeschlagen                      |

### 3. Prüfung explizit vs. implizit

Die ersten drei Punkte sind explizit im Verlauf ausgesprochen. Ein möglicher Kandidat für "implizit": Sievers' interne Beschleunigung des Testsystem-Antrags wird oft nur als Nebensatz erkannt, nicht als eigener Aktionspunkt gelistet.

### 4. Ergänzter impliziter Punkt

| Aktionspunkt                                            | Verantwortlich | Kennzeichnung               |
| ------------------------------------------------------- | -------------- | --------------------------- |
| Testsystem-Antrag intern beschleunigen, sobald gestellt | Sievers        | implizit ergänzt (von Hand) |

## Checkpoint

- Drei Aktionspunkte sind als explizit gekennzeichnet, ein vierter als implizit ergänzt.
- Die Ergänzung ist inhaltlich im Gesprächsverlauf begründet, nicht erfunden.

## Erweiterung

Ohne Formatvorgabe liefert Copilot häufig einen zusammenhängenden Fließtext statt einer Tabelle mit klarer Verantwortlichkeit — Aktionspunkte sind dann schwerer auf einen Blick prüfbar.
