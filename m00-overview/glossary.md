# Glossar

| Begriff                      | Bedeutung                                                                                                                           |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Copilot Chat                 | Konversationelle Copilot-Oberfläche, webbasiert oder in Teams/Microsoft 365, ohne App-Integration                                   |
| Copilot in Word/Excel/…      | App-integrierte Copilot-Funktion, arbeitet direkt am geöffneten Dokument                                                            |
| /-Befehl                     | Slash-Befehl in Word/Excel-Copilot, um ein konkretes Dokument als Kontext zu referenzieren                                          |
| Human-in-the-Loop (HITL)     | Prinzip, nach dem KI-generierte Zwischenergebnisse vor der finalen Nutzung von einem Menschen geprüft werden                        |
| RAG / Grounding              | Das System sucht vor der Antwort relevante Informationen in externen Quellen (bei Copilot: Microsoft Graph) und legt sie zugrunde   |
| Custom Agent                 | Eigener Agent mit Ziel, Anweisungen, Wissen, Tools und Skills — kein gespeicherter Prompt, sondern ein System, das Schritte wählt   |
| No-Code Agent Builder        | Vereinfachtes Werkzeug zum Anlegen eines Agenten direkt in Copilot Chat (Copilot-Chat-Harness)                                      |
| Copilot Studio               | Microsoft-Plattform zum Bauen, Testen, Veröffentlichen und Überwachen eigener Agenten und Workflows                                 |
| Harness                      | Laufzeitschicht zwischen Modell und Agent-Konfiguration: steuert, wann das Modell aufgerufen wird, welche Komponenten es bekommt, wie Tools aufgerufen werden |
| GitHub-Copilot-Harness       | Copilot-Studio-Harness für schlussfolgernde, mehrstufige Agenten und Workflows mit Skills und Memory; **nicht** der GitHub-Copilot-Dienst; Abrechnung über Copilot Credits |
| Standard-Harness             | Copilot-Studio-Harness für regelbasierte Agenten (Topics, feste Pfade) mit vorhersagbarem Verhalten                                 |
| Copilot-Chat-Harness         | Harness zum Erweitern von Microsoft Copilot Chat um Unternehmenswissen; nur interne Veröffentlichung                                |
| Skill                        | Portables Paket aus Name, Beschreibung und Markdown-Anweisungen (`SKILL.md`), das der Agent nur lädt, wenn die Anfrage zur Beschreibung passt |
| `SKILL.md`                   | Datei im offenen Skill-Format: Name (Kleinbuchstaben, Zahlen, Bindestriche) und Beschreibung im Kopf, danach die Anweisungen         |
| Progressive Disclosure       | Der Agent lädt nur den Kontext, den er für die aktuelle Anfrage braucht — nicht alle Skills auf einmal                              |
| Build / Preview / Evaluate / Monitor | Die vier Tabs eines Agenten im GitHub-Copilot-Harness: konfigurieren, interaktiv testen, Testsets messen, Betrieb überwachen |
| Workflow                     | Deterministischer Ablauf aus Trigger und Aktionen (inkl. KI-Aktionen und menschlicher Freigabe); als Tool für Agenten nutzbar       |
| Automatisierung              | Regelbasierter Ablauf ohne KI-Entscheidung: fester Trigger, feste Aktionskette                                                      |
| MCP (Model Context Protocol) | Offener Standard, über den sich ein Agent mit externen Tools und Datenquellen verbindet                                             |
| Connected Agent              | Spezialisierter Agent, an den ein anderer Agent Teilaufgaben delegiert (Sub-Agent-Muster)                                           |
| Agentic Loop                 | Der Agent bewertet seinen Fortschritt und entscheidet, ob er weitermacht, einen anderen Weg versucht, delegiert oder stoppt         |
| Copilot Credits              | Nutzungsbasierte Abrechnungseinheit für Agenten im GitHub-Copilot-Harness (Bauen, Testen, Evaluieren, Betrieb)                      |
| Power-Platform-Umgebung      | Container, in dem Agenten und Flows leben und der Governance (z. B. Dev/Test/Prod, DLP) ermöglicht                                  |
| Microsoft Graph Connector    | Anbindung externer Line-of-Business-Datenquellen, damit Copilot sie durchsuchbar einbeziehen kann                                   |
| Oversharing                  | Zu breite Freigabe eines Dokuments oder einer Wissensquelle (z. B. "gesamte Organisation"), oft unbeabsichtigt                      |
| The Nextise Agentic Way      | Methodik: KI nutzen, um KI zu bauen; Problem verstehen → Lösung konzipieren → bauen; Mensch bleibt in jedem Schritt "in the loop"   |
