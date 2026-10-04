# Lab 5.2 – Lösung: Personalisierungsprofil & Copilot-Speicher

## Aufgaben

### 1. Profil anlegen

Beispielprofil:

```text
Rolle: Projektleitung bei Nordwind Consulting
Tonfall: sachlich-knapp, keine Werbesprache
Zielgruppe: Kund:innen und interne Führungskräfte
```

### 2. Vergleich vor/nach Profil

| Ohne Profil                                           | Mit Profil                                                              |
| ----------------------------------------------------- | ----------------------------------------------------------------------- |
| allgemeiner Ton, unklare Zielgruppe, wechselnde Länge | durchgehend sachlich-knapp, konsistent auf die Zielgruppe zugeschnitten |

Erwarteter Unterschied: Tonfall und Zielgruppenbezug sind mit Profil stabiler, ohne dass sie im Prompt wiederholt werden müssen.

### 3. Speicher-Eintrag anlegen

```text
Merke dir, dass ich bei Nordwind Consulting für die Kundenkommunikation zuständig bin.
```

### 4. Prüfung im neuen Chat

Prompt im neuen Chat: "Wer sollte die nächste Kundenmail an die Stadtwerke Nordhafen schreiben?" Erwartetes Verhalten: Copilot bezieht die gespeicherte Zuständigkeit ohne erneute Nennung ein.

### 5. Eintrag prüfen und löschen

Der Eintrag erscheint in der Speicherverwaltung im Wortlaut nahe der ursprünglichen Formulierung. Nach dem Löschen ist er dort nicht mehr aufgeführt und wird in neuen Chats nicht mehr berücksichtigt.

## Checkpoint

- Der Unterschied zwischen den beiden Zusammenfassungen ist an Tonfall oder Zielgruppenbezug festgemacht.
- Aufgabe 4 bestätigt die automatische Verwendung des gespeicherten Fakts.
- Der Eintrag ist nachweislich gelöscht.

## Erweiterung

Ein Profil mit nur "freundlich" liefert kaum unterscheidbare Ergebnisse gegenüber gar keinem Profil — der Effekt entsteht erst durch konkrete, rollenbezogene Angaben, nicht durch allgemeine Stimmungswörter.
