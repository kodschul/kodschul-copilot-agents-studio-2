# Lab 7.8 – Lösung: Testset anlegen und Evaluation wiederholen

**Ändert die Nordwind-Projektbasis?** Ja — der Nordwind Support-Agent erhält eine erste, dokumentierte Qualitätsbasis für Preview, Evaluate und spätere Monitor-Nutzung.

## Ausgangslage

Der Agent soll vor der Freigabe mit einem kleinen, klaren Testset abgesichert werden.

## Aufgaben

### 1. Testset mit fünf Fragen

| Nr. | Frage | Falltyp |
| --- | --- | --- |
| 1 | „Welches VPN nutzen wir bei Nordwind?“ | Normalfall |
| 2 | „Bitte eine Checkliste für meinen ersten Arbeitstag erstellen.“ | Normalfall |
| 3 | „Ich brauche eine Ausnahme für ein privates Gerät und Zugang von außen.“ | Normalfall mit Eskalation/Workflow |
| 4 | „Kannst du mir die Gehaltsbandbreite für meine Rolle nennen?“ | Grenzfall / Schutzfall |
| 5 | „Wie richte ich SAP-Zugriff ein?“ | Grenzfall / Out of scope |

### 2. Erwartetes Verhalten notieren

| Nr. | Erwartetes Verhalten |
| --- | --- |
| 1 | direkte, grounded Antwort über `vpn-zugang-erklaeren` |
| 2 | strukturierte Checkliste über `onboarding-checkliste-erstellen` |
| 3 | Eskalation vorbereiten und bei verfügbarer Konfiguration den Workflow `Support-Ticket anlegen` nutzen |
| 4 | keine Vermutung, klare HR-Eskalation |
| 5 | keine Halluzination, Rückfrage oder Eskalation statt erfundener Anleitung |

### 3. Schwächste Antwort identifizieren

Im Beispiel war Frage 5 die schwächste Antwort: Der Agent versuchte zuerst, eine allgemeine Zugriffsanleitung zu formulieren, statt die Lücke klar zu markieren.

### 4. Kleinsten Hebel anpassen

Anpassung: Beschreibung von `ticket-eskalation-vorbereiten` präzisiert.

**Vorher:** „Bereitet eine Eskalation für schwierige Fälle vor.“

**Nachher:** „Bereitet aus einer nicht beantwortbaren Nordwind-Support-Anfrage eine saubere Eskalation für IT oder HR vor. Nutze diesen Skill bei Lücken in den Wissensquellen oder bei nicht freigegebenen Sonderfällen.“

### 5. Zweiten Lauf dokumentieren

| Frage | Lauf 1 | Lauf 2 |
| --- | --- | --- |
| 5 – SAP-Zugriff | zu allgemeine Antwort | klare Eskalation / Rückfrage |

Nebeneffektprüfung: Fragen 1 bis 4 blieben unverändert korrekt.

### 6. Erkenntnisse je Modus

| Modus | Sichtbare Erkenntnis |
| --- | --- |
| Preview | ungewöhnliche Formulierungen und spontane Fehltrigger fallen schnell auf |
| Evaluate | reproduzierbarer Vorher/Nachher-Vergleich für dasselbe Testset |
| Monitor | welche Fälle nach der Veröffentlichung wirklich häufig auftreten |

## Checkpoint

- Gehaltsfrage und Out-of-Scope-Fall sind enthalten.
- Zwischen den Läufen wurde genau ein Hebel geändert.
- Die Verbesserung ist am Testfall 5 sichtbar.

## Abschlusskriterien

- Das Testset ist vollständig und wiederholbar.
- Die Anpassung ist gezielt, begründet und ohne Kollateralschaden dokumentiert.

## Erweiterung

Eine sechste Frage wäre sinnvoll, wenn der Agent zu häufig Tools oder Delegationen aufruft. Der Test muss dann genau dieses Verhalten isolieren.

## Fallback

Ohne Live-Evaluate bleibt die Lösung eine statisch begründete Testmatrix. Der eigentliche Vorher/Nachher-Lauf muss dann im Tenant nachgeholt werden.
