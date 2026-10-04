# Lab 3.1 – Übung: Kundenangebot in Word

**Ändert die Nordwind-Projektbasis?** Ja — der Angebotsentwurf ist Grundlage für die Kundenkommunikation in Modul 6.

## Ausgangslage

Für die Stadtwerke Nordhafen soll ein Angebot für die Anschlussphase "Betrieb und Weiterentwicklung Leitstand" entstehen (24 Monate Laufzeit).

Bereitgestellt in `output/project/`:

- `nordwind-angebotsvorlage.docx` — die Vorlage als echtes Word-Dokument, in Word mit Copilot öffnen
- `nordwind-angebotsvorlage.md` — dieselbe Struktur als Textreferenz
- `nordwind-projektnotizen.docx` — Projektstand, Risiken, offene Punkte als echtes Word-Dokument, per /-Befehl referenzierbar
- `nordwind-projektnotizen.md` — dieselbe Notizen als Textreferenz

## Aufgaben

1. Einen Prompt formulieren, der die Angebotsvorlage **und** die Projektnotizen per /-Befehl referenziert (`/nordwind-angebotsvorlage.docx`, `/nordwind-projektnotizen.docx`), statt deren Inhalt zu beschreiben. Rolle, Adressat und Tonfall ("sachlich-zurückhaltend") ergänzen.
2. Den Entwurf erzeugen und mit der Vorlage abgleichen: Sind alle Pflichtabschnitte aus `nordwind-angebotsvorlage.md` vorhanden?
3. Drei konkrete Angaben im Entwurf (Zahl, Frist oder Name) gegen `nordwind-projektnotizen.md` prüfen und das Ergebnis je Angabe als "korrekt", "abweichend" oder "erfunden" festhalten.
4. Für jede als "abweichend" oder "erfunden" markierte Angabe: die Textstelle korrigieren oder streichen.
5. Den finalen, geprüften Entwurf als `nordwind-angebot-entwurf.md` in `output/project/` ablegen.

## Checkpoint

- Der erzeugte Entwurf enthält alle Pflichtabschnitte aus der Vorlage.
- Drei geprüfte Angaben liegen mit Bewertung vor, mindestens eine Prüfung ist tatsächlich gegen die Notizen erfolgt (nicht nur plausibel angenommen).
- Der finale Entwurf enthält keine als "erfunden" markierte Angabe mehr.

## Abschlusskriterien

- `nordwind-angebot-entwurf.md` liegt vor, referenziert die Vorlage strukturell und ist inhaltlich mit den Projektnotizen konsistent.
- Der verwendete Prompt ist im Wortlaut dokumentiert.

## Erweiterung

Denselben Entwurf ein zweites Mal ohne /-Befehl erzeugen, nur mit einer Freitextbeschreibung der Projektlage. Die beiden Fassungen auf erfundene Details vergleichen.

## Fallback

Steht keine /-Befehl-Funktion zur Verfügung oder liegen die Dateien nicht in OneDrive/SharePoint: Vorlage und Notizen als Volltext in den Prompt einfügen. Einschränkung: Formatierung und Struktur der Vorlage werden dann nicht automatisch übernommen und müssen von Hand nachgezogen werden.
