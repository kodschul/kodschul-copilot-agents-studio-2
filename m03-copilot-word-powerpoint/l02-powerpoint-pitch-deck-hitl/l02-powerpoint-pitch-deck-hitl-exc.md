# Lab 3.2 – Übung: Pitchdeck aus der HITL-Gliederung bauen

**Ändert die Nordwind-Projektbasis?** Ja — das entstehende Pitchdeck wird in Lab 3.3 weiterverwendet.

## Ausgangslage

`hitl-gliederung.md` aus Lab 2.4 liegt vor: Kernbotschaft, acht bis zehn Folien mit je einer Kernaussage, Belegstatus je Folie.

Bereitgestellt in `output/project/`:

- `nordwind-pitchdeck-starter.pptx` — leeres PowerPoint-Grundgerüst (Titelfolie + eine Platzhalterfolie) als Ablagepunkt für die erzeugten Folien

## Aufgaben

1. Die eigene `hitl-gliederung.md` öffnen und die Folien nach Belegstatus sortieren: belegt zuerst, nicht belegt markiert.
2. Für jede **belegte** Folie einen eigenen Auftrag formulieren, der die Kernaussage unverändert übernimmt und Copilot bittet, sie mit den tatsächlichen Werten aus `nordwind-projektnotizen.md` zu befüllen. Maximal vier Bullet-Points je Folie.
3. Für jede **nicht belegte** Folie einen Auftrag formulieren, der ausdrücklich einen Platzhalter statt erfundener Inhalte verlangt.
4. Alle Folien erzeugen und zu einem Foliensatz zusammenführen (PowerPoint oder gleichwertiges Format).
5. Jede erzeugte Folie gegen ihre Kernaussage aus der Gliederung prüfen: Trifft die Folie die Aussage, oder ist sie abgedriftet?
6. Für mindestens eine Folie eine Sprechnotiz separat anfordern und prüfen, ob sie über die Bullet-Points hinaus etwas Nutzbares ergänzt.

## Checkpoint

- Der Foliensatz enthält so viele Folien wie die Gliederung, keine zusätzliche und keine fehlende.
- Nicht belegte Folien sind im Foliensatz als Platzhalter erkennbar, nicht mit erfundenen Zahlen gefüllt.
- Mindestens eine Folie wurde gegen ihre Kernaussage geprüft und ggf. korrigiert.

## Abschlusskriterien

- Der Foliensatz liegt vollständig vor und ist als Grundlage für einen 20-minütigen Vortrag nutzbar.
- Die Liste der noch zu beschaffenden Belege aus der HITL-Gliederung ist unverändert gültig und wird nicht durch erfundene Werte verdeckt.

## Erweiterung

Eine belegte Folie zusätzlich in einem einzigen Gesamtprompt für das ganze Deck erzeugen lassen (One-Shot-Vergleich) und beide Fassungen dieser einen Folie nebeneinanderlegen.

## Fallback

Ohne PowerPoint-Copilot-Zugriff: Die Folieninhalte in Word oder als Markdown-Gliederung erzeugen und die Struktur anschließend manuell in Folien überführen. Einschränkung: Layout- und Formatübernahme entfallen, der inhaltliche Prüfschritt bleibt unverändert durchführbar.
