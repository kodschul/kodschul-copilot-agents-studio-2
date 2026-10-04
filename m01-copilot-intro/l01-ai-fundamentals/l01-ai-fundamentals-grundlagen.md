# Lab 1.0 – Grundlagen: Wie KI-Systeme lernen und funktionieren

Erster, produktunabhängiger Theorie-Teil von Lab 1.0. Klärt, was KI überhaupt ist und was sie technisch tut, bevor in Lab 1.0 (zweiter Teil, `l01-ai-fundamentals-thx.md`) Prompting und Copilot dazukommen.

## Was ist künstliche Intelligenz überhaupt?

- **Künstliche Intelligenz (KI)** ist der Oberbegriff für Maschinen, die Aufgaben lösen, für die sonst menschliche Intelligenz nötig wäre.
- Den Begriff gibt es bereits seit 1956 (Dartmouth-Konferenz) — der aktuelle Boom ist keine neue Erfindung, sondern ein technischer Durchbruch seit etwa 2012.
- Eine KI ist **nicht** dasselbe wie ein Roboter: Ein Roboter ist Hardware, KI ist die Software/Logik dahinter — oft ganz ohne Körper, zum Beispiel als Chat.

## Starke vs. schwache KI

| Begriff          | Bedeutung                                                                                |
| ---------------- | ---------------------------------------------------------------------------------------- |
| Schwache/enge KI | auf eine Aufgabe spezialisiert — das haben wir heute, auch Copilot.                      |
| Starke KI        | hypothetische KI mit genereller, menschenähnlicher Intelligenz — existiert bisher nicht. |

> **Merksatz:** Alles, was in diesem Kurs vorkommt, ist schwache/enge KI — spezialisiert auf Sprache, Bilder oder einzelne Aufgaben, nicht auf "alles wie ein Mensch".

## Die Teilbereiche der KI

| Teilbereich                       | Kurzbeschreibung                                          |
| --------------------------------- | --------------------------------------------------------- |
| Machine Learning                  | lernt Muster aus Daten, statt fest programmierter Regeln. |
| NLP (Natural Language Processing) | Sprache verstehen und erzeugen — Basis für Copilot Chat.  |
| Computer Vision                   | Bilder und Videos interpretieren.                         |
| Robotics                          | KI steuert physische Maschinen/Roboter.                   |

## KI ist nicht gleich LLM

- KI ist der große Oberbegriff — ein **LLM** (Large Language Model, die Technik hinter Copilot) ist nur **ein** Teilbereich davon.
- Es gibt ganz unterschiedliche KI-Anwendungsfälle: von Spam-Filtern über Bilderkennung bis zu Chatbots.
- Wichtige Unterscheidung dabei: **generative KI** vs. **nicht-generative KI**.

## Generative KI vs. nicht-generative KI

|          | Generative KI                           | Nicht-generative KI                                |
| -------- | --------------------------------------- | -------------------------------------------------- |
| Aufgabe  | erzeugt neue Inhalte (Text, Bild, Code) | klassifiziert, erkennt oder entscheidet nur        |
| Beispiel | ChatGPT, Copilot, Bildgeneratoren       | Spam-Filter, Gesichtserkennung, Empfehlungssysteme |
| Ausgabe  | jedes Mal leicht anders                 | im Kern immer dieselbe Kategorie/Entscheidung      |

## Deterministisch vs. flexibel

Je determinierter ein System, desto unflexibler, aber zuverlässiger. Je flexibler, desto kreativer, aber weniger vorhersagbar — die richtige Balance für den Anwendungsfall zu finden, ist die eigentliche Kunst.

|                   | Deterministisch                          | Generative KI (flexibel)                |
| ----------------- | ---------------------------------------- | --------------------------------------- |
| Eingabe → Ausgabe | gleiche Eingabe → immer dieselbe Ausgabe | gleiche Eingabe → kann leicht variieren |
| Vorhersagbarkeit  | hoch                                     | geringer                                |
| Beispiel          | Regel-Systeme, Taschenrechner            | Copilot, ChatGPT                        |

```
deterministisch, vorhersagbar  <───────────────────────────>  flexibel, kreativ
```

## Warum ist Generative KI gerade jetzt so relevant?

- Das Thema KI gibt es schon seit den 1950ern — warum also gerade jetzt der Hype?
- Früher trainierte jede Firma ihr eigenes, kleines Modell selbst — aufwändig, teuer, nur für Großkonzerne machbar.
- Heute nutzen alle wenige große, vortrainierte **Foundation-Modelle** (z. B. von OpenAI) und passen sie nur noch an.
- Der ChatGPT-Moment (November 2022) machte generative KI erstmals massentauglich — genau das macht diesen Kurs relevant: **nutzen statt selbst trainieren**.

## Wie KI-Systeme lernen

| Lernart                | Funktionsweise                                                            | Beispiel                                                |
| ---------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------- |
| Supervised Learning    | lernt aus großen Mengen strukturierter, bereits gekennzeichneter Daten    | Spam-Erkennung anhand markierter E-Mails                |
| Unsupervised Learning  | findet selbstständig Strukturen/Gruppierungen in ungekennzeichneten Daten | Kund:innen anhand von Kaufverhalten clustern            |
| Reinforcement Learning | lernt durch Trial-and-Error, erhält für Handlungen Belohnung oder Strafe  | ein Spielprogramm, das durch Wiederholen gewinnen lernt |

> **Merksatz:** Alle drei Lernarten laufen einmalig beim Training. Ein fertiges Modell wie das hinter Copilot lernt im laufenden Betrieb nichts dazu — es wendet nur an, was es beim Training gelernt hat.

## Deep Learning und künstliche neuronale Netze

Deep Learning setzt auf **künstlichen neuronalen Netzen** auf: einzelne "Neuronen", lose am Vorbild des menschlichen Gehirns orientiert, sind in Schichten verbunden und geben gewichtete Signale weiter.

![Colored diagram of a multi-layer artificial neural network with input, hidden and output layers](https://commons.wikimedia.org/wiki/Special:FilePath/Colored_neural_network.svg)

Large-Language-Modelle wie die hinter Copilot sind genau solche neuronalen Netze — trainiert auf riesigen Textmengen, um Sprachmuster zu lernen.

> **Merksatz:** "Neuronales Netz" ist eine Analogie, keine Kopie des Gehirns. Ein künstliches Neuron berechnet nur eine gewichtete Summe — es denkt nicht.

## Tokenisierung: wie Text in Häppchen zerlegt wird

Bevor ein Sprachmodell irgendetwas berechnet, zerlegt es den Eingabetext in **Token** — kleine Einheiten, oft ein kurzes Wort, eine Silbe oder ein Satzzeichen. "Anforderungserhebung" wird zum Beispiel zu mehreren Token, nicht zu einem. Das Modell arbeitet ausschließlich auf dieser Token-Ebene, nie auf ganzen Sätzen.

## Vektorisierung: wie aus Token Zahlen werden

Token allein sind für eine Rechenmaschine bedeutungslos. Deshalb wird jedes Token in einen **Vektor** (auch Embedding genannt) übersetzt — eine lange Liste von Zahlen, die die Bedeutung des Tokens im gelernten Sprachraum codiert. Token mit ähnlicher Bedeutung liegen im Vektorraum nah beieinander ("Angebot" und "Offerte" liegen näher zusammen als "Angebot" und "Regenschirm").

![Diagram comparing a localist one-hot representation with a distributed vector representation](https://commons.wikimedia.org/wiki/Special:FilePath/Distributed_representation.svg)

Genau dieses Prinzip steckt hinter der **semantischen Suche**, die Copilot beim Grounding nutzt (siehe `01-copilot-funktionsweise.md`): Copilot vergleicht nicht Wort für Wort, sondern die Nähe von Vektoren — deshalb findet es auch passende Inhalte, die die gesuchten Wörter gar nicht wörtlich enthalten.

> **Merksatz:** Token = die Häppchen, Vektor/Embedding = die Zahlen, die deren Bedeutung ausdrücken. Ohne Vektorisierung gäbe es keine semantische Suche.

## Nur Wahrscheinlichkeitsrechnung

Ein Sprachmodell "denkt" nicht wie ein Mensch. Es sagt Token für Token den statistisch wahrscheinlichsten nächsten Token voraus, basierend auf den Mustern, die es beim Training in Milliarden von Textbeispielen gesehen hat — reine Wahrscheinlichkeitsrechnung, keine Faktenprüfung.

```
Prompt  →  Zerlegung in Token  →  Vektorisierung
        →  Modell berechnet wahrscheinlichsten nächsten Token
        →  Token für Token bis zum Ende
        →  Antworttext
```

Das Modell prüft dabei nichts nach. Es gibt keine Faktenprüfung im Ablauf — genau daraus entsteht das Halluzinationsrisiko.

## Wie "rechnet" eine KI, ohne eigentlich Mathe zu können?

Wenn das Sprachmodell nur den wahrscheinlichsten nächsten Token vorhersagt — wie löst es dann eine komplexe Berechnung, etwa eine Tabellen-Auswertung oder ein Diagramm in Copilot?

Gar nicht direkt im neuronalen Netz. Die KI agiert eher wie ein "Projektmanager": sie lässt rechnen, statt selbst zu rechnen.

```
Codegenerierung  →  Sandbox (isoliert)  →  Output-Interpretation
```

Die KI schreibt ein Skript für die Aufgabe, lässt es sicher in einer isolierten Umgebung ausführen und erklärt anschließend das Ergebnis. Gerechnet wird also nicht im neuronalen Netz, sondern im ausgeführten Code.

## Wie wird "Wissen" im Modell gespeichert?

- Gelerntes Wissen wird in **Parametern** gespeichert — Zahlen, die die Stärke der Verbindungen im neuronalen Netz beschreiben.
- Die Modellgröße wird deshalb in Milliarden Parametern angegeben (z. B. "70B" = 70 Milliarden Parameter).
- Faustregel: 1 Milliarde Parameter entspricht grob 0,5 Gigabyte Modellgröße.

| Modell                          | Parameter                                   | offiziell bestätigt? |
| ------------------------------- | ------------------------------------------- | -------------------- |
| GPT-3 (2020)                    | 175 Milliarden                              | ja                   |
| GPT-4 / GPT-5                   | nicht veröffentlicht, Schätzungen kursieren | nein                 |
| Llama 3 (Meta, offene Gewichte) | Varianten mit 8, 70 oder 405 Milliarden     | ja                   |

> **Merksatz:** OpenAI veröffentlicht die Parameterzahl der aktuellen GPT-Modelle nicht mehr offiziell — nur Schätzungen kursieren. Bekannt bestätigt ist nur die Vorgänger-Generation (GPT-3).

## Open-Source vs. Open-Weights vs. Closed

| Begriff             | Bedeutung                                                                                                                     |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Open-Source-Modell  | Trainingscode ist öffentlich einsehbar.                                                                                       |
| Open-Weights-Modell | zusätzlich sind die trainierten Parameter frei verfügbar — z. B. Llama. Das gelernte Wissen selbst steht zum Download bereit. |
| Closed-Modell       | weder Code noch Parameter offen — z. B. GPT-4/5, nur per API nutzbar (wie hinter Copilot/ChatGPT).                            |

## "Shit in, shit out": Datenqualität entscheidet

- Daten sind die Basis — ein Modell ist immer nur so gut wie die Daten, aus denen es gelernt hat.
- Beim Training speichert das Modell dieses Wissen als Parameter; Fehler, Lücken und Verzerrungen in den Trainingsdaten werden mit gespeichert.
- Ein neuer Hype-Begriff macht aus schlechten Daten kein besseres Ergebnis — im schlimmsten Fall skaliert er nur den Fehler.

> **Merksatz:** Bevor über ein neues Modell oder eine neue Technik nachgedacht wird, lohnt sich immer zuerst die Frage nach der Datenqualität.

## RAG: warum man einem Sprachmodell nicht blind vertraut

Ein Sprachmodell allein kennt nur das, was beim Training gesehen wurde, und liefert die wahrscheinlichste Fortsetzung — nicht garantiert korrekte Fakten. **RAG (Retrieval-Augmented Generation)** wirkt dem entgegen:

```
Anfrage  →  RAG sucht relevante Informationen in externen Quellen
         →  (Datenbanken, Dokumente, APIs)
         →  Sprachmodell erzeugt Antwort gestützt auf diese Quellen
         →  weniger Halluzination, nachvollziehbarere Antwort
```

Copilot nutzt genau dieses Prinzip als "Grounding" über Microsoft Graph — vertieft in Lab 1.2 (`01-copilot-funktionsweise.md`).

## Begriffe

| Begriff           | Bedeutung                                                                                                                                     |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Foundation-Modell | großes, vortrainiertes Basismodell (z. B. von OpenAI), das viele nutzen statt selbst zu trainieren                                            |
| Token             | kleinste Verarbeitungseinheit eines Sprachmodells, etwa eine Silbe oder ein kurzes Wort                                                       |
| Vektor/Embedding  | numerische Darstellung eines Tokens, codiert dessen Bedeutung im Sprachraum                                                                   |
| Neuronales Netz   | Schichten künstlicher "Neuronen", die gewichtete Signale weitergeben                                                                          |
| Parameter         | im Training gelernte Zahl, die die Stärke einer Verbindung im neuronalen Netz beschreibt; Modellgröße wird in Milliarden Parametern angegeben |
| Open-Weights      | Modellvariante, bei der die trainierten Parameter frei verfügbar sind (z. B. Llama)                                                           |
| LLM               | Large Language Model, ein neuronales Netz, trainiert auf riesigen Textmengen                                                                  |
| RAG               | Retrieval-Augmented Generation: Antwort gestützt auf gezielt gesuchte externe Quellen                                                         |
| Halluzination     | plausibel klingende, aber faktisch falsche Ausgabe                                                                                            |

## Fazit

- KI ist der Oberbegriff; ein LLM ist nur ein Teilbereich davon — generative und nicht-generative KI unterscheiden sich in Aufgabe, Beispiel und Ausgabe.
- Je determinierter ein System, desto zuverlässiger, aber unflexibler; die richtige Balance ist die eigentliche Kunst.
- Foundation-Modelle machen generative KI gerade jetzt relevant: nutzen statt selbst trainieren.
- KI-Systeme lernen auf drei Grundarten: Supervised, Unsupervised und Reinforcement Learning — danach lernt ein fertiges Modell im Betrieb nichts mehr dazu.
- Text wird zuerst in Token, dann in Vektoren zerlegt; Vektor-Nähe ist die Basis für semantische Suche.
- Ein Sprachmodell sagt Token für Token die wahrscheinlichste Fortsetzung voraus — reine Wahrscheinlichkeitsrechnung, keine Faktenprüfung; komplexe Berechnungen löst es per generiertem Code in einer Sandbox, nicht im neuronalen Netz.
- Gelerntes Wissen steckt in Milliarden Parametern (1B ≈ 0,5 GB); Open-Source, Open-Weights und Closed unterscheiden sich darin, was davon offen zugänglich ist.
- "Shit in, shit out": ein Modell ist immer nur so gut wie seine Trainingsdaten — das lösen auch neue Hype-Begriffe nicht.
- RAG stützt die Vorhersage auf externe, aktuelle Quellen statt nur auf gelerntes Wissen.

Weiter geht es in `l01-ai-fundamentals-thx.md` mit Prompting, Modell-Aktivierung und der Frage, wann ein Agent gebraucht wird.
