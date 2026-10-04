# Lab 7.4 – Lösung: Support-Agent in Copilot Studio (GitHub-Copilot-Harness)

## Aufgaben

### 1. Agent auf dem GitHub-Copilot-Harness anlegen

Beispielname: **Nordwind Support-Agent (Studio)**. Falls kein eigener Zugang vorliegt, genügt eine vollständige Protokollnotiz der Trainer-Demo mit Harness, sichtbaren Tabs und gewählter Umgebung.

### 2. Instructions und Knowledge übernehmen

| Bereich | Inhalt |
| --- | --- |
| Instructions | System-Prompt aus Lab 7.2 mit klarer Eskalationsregel |
| Knowledge | `../../project/nordwind-it-richtlinie.md`, `../../project/nordwind-onboarding-leitfaden.md` |

### 3. Modellwahl dokumentieren

Die Modellwahl hängt vom Tenant ab. Tragfähig ist eine Notiz wie: „Verfügbare Modelle im Tenant gesichtet, eines für den ersten Test gewählt; genaue Namen und Verfügbarkeit vor Kursbeginn prüfen.“

### 4. Preview mit drei Fragen testen

| Testfrage | Erwartetes Verhalten | Beispielbeobachtung |
| --- | --- | --- |
| „Welches VPN nutzen wir bei Nordwind?“ | Cisco Secure Client nennen | korrekt beantwortet |
| „Was passiert am ersten Arbeitstag?“ | Erstlogin, Passwortwechsel, MFA und Standardsoftware nennen | korrekt beantwortet |
| „Wie hoch ist die Gehaltsbandbreite meiner Position?“ | an HR eskalieren | korrekt eskaliert |

Beim Dokumentbezug reicht als Beobachtung, ob die Antwort erkennbar auf die Nordwind-Quellen zurückgeht oder ob der Tenant zusätzlich eine Quellenanzeige sichtbar macht.

### 5. Studio-Agent mit Chat-Agent vergleichen

| Kriterium | Chat-Agent aus Lab 7.2 | Studio-Agent aus Lab 7.4 |
| --- | --- | --- |
| Antwortqualität | für reine Wissensfragen bereits gut | ähnlich gut, mit stärkerem Ausbaupfad |
| Quellenangabe | Dokumentbezug eher indirekt | Dokumentbezug beziehungsweise Quellenansicht im Preview genauer beobachtbar, tenantabhängig |
| Steuerbarkeit | schneller erster Start | mehr Bausteine und klarerer Ausbau für Skills/Tools |
| Aufwand | geringer | höher wegen zusätzlicher Konfiguration |
| Credits | nicht der Fokus dieses Lab-Schritts | Credits schon beim Bauen und Testen relevant |

### 6. Fehlende Bausteine für den nächsten Schritt festhalten

Noch offen für den Ausbau:

- Skills hinzufügen,
- Skill-Auslösung testen,
- weitere Tool-/Workflow-Bausteine in späteren Labs ergänzen.

## Checkpoint

- System-Prompt und Knowledge stimmen mit Lab 7.2 überein.
- Alle drei Testfälle wurden nachvollziehbar dokumentiert.
- Die Vergleichstabelle zeigt nicht nur Vorteile, sondern auch Credits und Zusatzaufwand.

## Abschlusskriterien

- Die Studio-Variante des Nordwind Support-Agenten ist als Basis für Skills vorbereitet.
- Der Vergleich mit dem Chat-Agenten ist entscheidungsrelevant dokumentiert.
- Lab 7.5 kann direkt mit den Skill-Entwürfen aus Lab 7.2 anschließen.

## Erweiterung

Eine kombinierte Frage ist hilfreich, um zu prüfen, ob der Studio-Agent schon jetzt strukturierter wirkt oder ob der Mehrwert erst mit den späteren Skills sichtbar wird.

## Fallback

Im Fallback ist die Lösung tragfähig, wenn die Beobachtungen aus der Demo sauber auf die fünf Vergleichskriterien abgebildet wurden. Ein eigener Credit-Verbrauch oder ein eigener Preview-Lauf lässt sich damit jedoch nicht belegen.
