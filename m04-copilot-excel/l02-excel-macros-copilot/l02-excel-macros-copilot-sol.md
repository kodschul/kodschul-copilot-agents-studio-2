# Lab 4.2 – Lösung: Excel-Makros mit Copilot

## Aufgaben

### 1. Aufgabenbeschreibung an Copilot

```text
Schreibe ein VBA-Makro für Excel, das die Spalten B, C und D (Aug 2026, Sep 2026, Summe)
als Währung (€) formatiert und Werte unter 0 rot einfärbt. Bereich: Zeile 2 bis 6.
```

### 2. Generierter Code (Beispiel)

```vba
Sub FormatBudgetReport()
    Dim rng As Range
    Set rng = Range("B2:D6")
    rng.NumberFormat = "#,##0 €"

    Dim cell As Range
    For Each cell In rng
        If cell.Value < 0 Then
            cell.Font.Color = RGB(255, 0, 0)
        Else
            cell.Font.Color = RGB(0, 0, 0)
        End If
    Next cell
End Sub
```

Zeile für Zeile: der Bereich B2:D6 wird als Währung formatiert, danach prüft eine Schleife jede Zelle einzeln und färbt negative Werte rot, positive schwarz.

### 3. Erklärung einer einzelnen Zeile

`rng.NumberFormat = "#,##0 €"` setzt das Zahlenformat auf Tausendertrennzeichen ohne Nachkommastellen plus Euro-Zeichen, unabhängig vom eingestellten Gebietsschema der Datei.

### 4. Test an einer Kopie

Kopie `nordwind-budget-daten-test.xlsx` angelegt, Makro dort ausgeführt: alle fünf Kostenblockzeilen sind korrekt als Währung formatiert, keine negativen Werte vorhanden (also keine rote Einfärbung sichtbar) — erwartungsgemäß, da alle Werte in der Beispieltabelle positiv sind.

### 5. Eingebauter Fehler

Falscher Spaltenbuchstabe `Range("B2:E6")` (Spalte E existiert in der Tabelle nicht) → Copilot-Erklärung: der Bereich greift auf eine leere Spalte zu, das Makro läuft ohne Absturz, formatiert aber eine Spalte, die keine Daten enthält — ein stiller Fehler, kein sichtbarer.

## Häufige Fehler

| Fehler                                                       | Korrektur                                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------------- |
| Code ungelesen direkt auf Echtdaten ausgeführt               | Immer zuerst an einer Kopie testen                                  |
| Bereichsangabe im Code nicht gegen die echte Tabelle geprüft | Zellbereich vor Ausführung mit der tatsächlichen Tabelle abgleichen |
| Stille Fehler übersehen (kein Absturz, falsches Ergebnis)    | Ergebnis immer visuell gegen die Ausgangsdaten prüfen               |

## Checkpoint

- Der Code wurde vor der Ausführung gelesen und in eigenen Worten zusammengefasst.
- Der Test lief zuerst an einer Kopie, nicht am Original.
- Der eingebaute Fehler (falscher Spaltenbuchstabe) wurde korrekt erklärt.

## Erweiterung

Ein `Workbook_Open`-Ereignis würde das Makro automatisch beim Öffnen der Datei ausführen. Sicherheitsimplikation: automatisch ausgeführter Code ist ein bekannter Angriffsvektor (Makroviren) — Tenants blockieren solche Auto-Makros standardmäßig, das ist kein Zufall.

## Fallback

Ohne Ausführungsberechtigung bleibt die Übung eine reine Lese- und Verständnisübung: Code generieren lassen, Zeile für Zeile erklären lassen, aber nicht ausführen.
