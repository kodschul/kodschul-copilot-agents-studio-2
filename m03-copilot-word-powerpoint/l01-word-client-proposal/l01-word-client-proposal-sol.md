# Lab 3.1 – Lösung: Kundenangebot in Word

## Aufgaben

### 1. Prompt mit /-Befehl

```text
Als Projektleiterin bei Nordwind Consulting GmbH: Entwirf ein Angebot für die Stadtwerke
Nordhafen über die Anschlussphase "Betrieb und Weiterentwicklung Leitstand" (24 Monate).

Referenziere /nordwind-angebotsvorlage.docx für Struktur und Formatvorgaben.
Referenziere /nordwind-projektnotizen.docx für Ausgangslage und Projektstand.

Ton: sachlich-zurückhaltend, förmlich, ohne Werbesprache.
```

### 2. Abgleich mit der Vorlage

| Pflichtabschnitt | Im Entwurf vorhanden?            |
| ---------------- | -------------------------------- |
| Anschreiben      | ja                               |
| Ausgangslage     | ja                               |
| Leistungsumfang  | ja                               |
| Zeitplan         | ja                               |
| Kommerzielles    | ja, ohne Zahlen (wie vorgegeben) |
| Nächste Schritte | ja                               |

### 3. Faktenprüfung

| Geprüfte Angabe                                        | Beleg in den Notizen                       | Bewertung      |
| ------------------------------------------------------ | ------------------------------------------ | -------------- |
| "Projektstart im August 2026"                          | 12.08.2026                                 | korrekt        |
| "Die Ist-Analyse ist vollständig abgeschlossen"        | AP1: 100 %                                 | korrekt        |
| "Der Anforderungskatalog ist bereits final abgestimmt" | AP2: 70 %, Freigabe seit 11.09. ausstehend | **abweichend** |

Typisches drittes Prüfergebnis "erfunden": ein im Entwurf genannter konkreter Startzeitpunkt der Anschlussphase, der in den Notizen nicht steht.

### 4. Korrektur

| Textstelle                 | Korrektur                                                                             |
| -------------------------- | ------------------------------------------------------------------------------------- |
| "bereits final abgestimmt" | ersetzt durch "zu 70 % erarbeitet, Freigabe durch den Fachbereich ausstehend"         |
| erfundener Startzeitpunkt  | gestrichen, durch "Beginn nach Abschluss der laufenden Digitalisierungsphase" ersetzt |

### 5. Ablage

`nordwind-angebot-entwurf.md` enthält den korrigierten Entwurf mit allen sechs Pflichtabschnitten, ohne verbliebene erfundene oder abweichende Angaben.

## Häufige Fehler

| Fehler                                                       | Korrektur                                                                   |
| ------------------------------------------------------------ | --------------------------------------------------------------------------- |
| Vorlage nur beschrieben statt referenziert                   | Ohne /-Befehl übernimmt Copilot eine eigene, abweichende Gliederung         |
| Kommerzieller Abschnitt mit erfundenen Zahlen befüllt        | Die Vorlage schließt Zahlen an dieser Stelle ausdrücklich aus               |
| Prüfung nur "überflogen" statt gegen die Notizen abgeglichen | Mindestens eine Zahl oder ein Termin muss tatsächlich nachgeschlagen werden |

## Checkpoint

- Alle sechs Pflichtabschnitte sind im finalen Entwurf vorhanden.
- Drei geprüfte Angaben liegen vor, mindestens eine als "abweichend" oder "erfunden" korrigiert.
- Der finale Entwurf enthält keine unkorrigierte Falschangabe mehr.

## Erweiterung

| Variante                     | Beobachtung                                                            |
| ---------------------------- | ---------------------------------------------------------------------- |
| mit /-Befehl                 | Struktur folgt der Vorlage, Fakten stammen überwiegend aus den Notizen |
| nur mit Freitextbeschreibung | eigene Gliederung, mehr plausibel klingende, aber unbelegte Details    |

## Fallback

Ohne /-Befehl-Funktion: Vorlage und Notizen als Volltext einfügen. Die Struktur muss danach von Hand mit der Vorlage abgeglichen werden, da Copilot ohne Dateireferenz keine feste Formatzuordnung übernimmt.
