# Lab 4.1 – Lösung: Budget-Analyse in Excel

## Aufgaben

### 1. Tabelle übertragen

| Kostenblock         |   Aug 2026 | Sep 2026 (bis 23.) |      Summe |
| ------------------- | ---------: | -----------------: | ---------: |
| Personal (Beratung) |     18.200 |             22.400 |     40.600 |
| Reise & Spesen      |      1.850 |              2.100 |      3.950 |
| Lizenzen & Tools    |      3.200 |              3.200 |      6.400 |
| Fremdleistungen     |      9.500 |              8.900 |     18.400 |
| Sonstiges           |        950 |              1.200 |      2.150 |
| **Summe pro Monat** | **33.700** |         **37.800** | **71.500** |

### 2. Summenformel

```text
=SUMME(B2:C2)
```

Gegen die Kontrollsumme geprüft: 40.600 (Personal) + 3.950 + 6.400 + 18.400 + 2.150 = 71.500 — stimmt mit der Zeile "Summe pro Monat" überein.

### 3. Stärkster Anstieg

| Kostenblock     | Aug 2026 | Sep 2026 | Anstieg |
| --------------- | -------: | -------: | ------: |
| Personal        |   18.200 |   22.400 |  +4.200 |
| Fremdleistungen |    9.500 |    8.900 |    −600 |

Personal (Beratung) ist mit +4.200 € der stärkste Anstieg, nachgerechnet durch einfache Differenz Sep − Aug.

### 4. Diagrammvorschlag

Ein Kreis- oder Balkendiagramm für die Verteilung der Kostenblöcke an der Gesamtsumme (71.500 €), kein Liniendiagramm — es geht um eine Verteilung zu einem Stichtag, nicht um einen Zeitverlauf über viele Perioden.

### 5. Restsumme

```text
=184000-71500
```

Ergebnis: 112.500 € — stimmt mit dem in `nordwind-projektnotizen.md` genannten Wert überein.

## Häufige Fehler

| Fehler                                                 | Korrektur                                                            |
| ------------------------------------------------------ | -------------------------------------------------------------------- |
| Formel ungeprüft aus dem Copilot-Vorschlag übernommen  | Immer gegen eine vorhandene Kontrollsumme oder Handrechnung prüfen   |
| Liniendiagramm für eine Verteilung zu einem Stichtag   | Verteilungsfragen brauchen Kreis-/Balkendiagramm, keinen Zeitverlauf |
| Anstieg absolut statt in Bezug zur Basis interpretiert | Bei stark unterschiedlichen Ausgangswerten zusätzlich Prozent prüfen |

## Checkpoint

- Alle fünf Summenformeln stimmen mit der Kontrollsumme überein.
- Personal (Beratung) ist korrekt als stärkster Anstieg benannt.
- Restsumme 112.500 € ist korrekt berechnet und referenziert.

## Erweiterung

| Kostenblock         | Anteil am Verbrauch |
| ------------------- | ------------------: |
| Personal (Beratung) |              56,8 % |
| Reise & Spesen      |               5,5 % |
| Lizenzen & Tools    |               9,0 % |
| Fremdleistungen     |              25,7 % |
| Sonstiges           |               3,0 % |
| **Summe**           |           **100 %** |

## Fallback

In Copilot Chat eingefügte Tabellen liefern dieselben Formeln und Zahlen als Text, aber kein direkt einsetzbares Excel-Diagramm — nur eine textliche Empfehlung, die anschließend von Hand als Diagramm angelegt werden muss.
