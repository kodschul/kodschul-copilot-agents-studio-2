# Lab 1.3 – Lösung: Das passende Werkzeug wählen

## Aufgaben

### 1. Entscheidung je Szenario

| #   | Szenario                                  | Werkzeug              | Tragende Kriterien                                                                     |
| --- | ----------------------------------------- | --------------------- | -------------------------------------------------------------------------------------- |
| 1   | Branchenübliche Vertragslaufzeiten        | Copilot Chat          | **Datenbasis** (allgemeines Webwissen genügt), **Kosten** (keine Zusatzlizenz nötig)   |
| 2   | Kundenkommunikation "Hafenmodernisierung" | Microsoft 365 Copilot | **Datenbasis** (eigene Mails/Chats nötig), **Integration** (Kontext liegt in M365)     |
| 3   | Externes Ausschreibungs-PDF verdichten    | Copilot Chat          | **Funktionsumfang** (Dateianlage reicht), **Datenbasis** (Quelle liegt als Anhang bei) |

Szenario 3 ist der lehrreiche Fall: Das Dokument ist extern und wird mitgeliefert. Es muss nicht in M365 gefunden werden, also genügt der Chat mit Anhang. Eine Volllizenz brächte hier keinen zusätzlichen Nutzen.

### 2. Szenario 1 in Copilot Chat

Erwartetes Ergebnis: eine brauchbare, allgemeine Übersicht. Typische Antwort nennt übliche Spannen und Einflussfaktoren wie Projektgröße und Leistungsart.

Bewertung: brauchbar für ein internes Briefing. Die genannten Zahlen sind Orientierungswerte ohne belastbare Quelle und müssen für eine Kundenaussage belegt werden.

### 3. Szenario 2 im Vergleich

| Variante                           | Erwartetes Ergebnis                                                                                                         |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Copilot Chat ohne Anhang           | allgemeine Aussagen darüber, wie man Kundenkommunikation zusammenfasst; keine konkreten Inhalte, keine Namen, keine Termine |
| Mit Zugriff auf den Arbeitskontext | konkrete Zusammenfassung mit den tatsächlichen Themen, Beteiligten und offenen Punkten                                      |

Die erste Variante scheitert nicht mit einer Fehlermeldung. Sie liefert eine plausibel klingende, aber leere Antwort — genau das Verhalten aus dem Hintergrundmaterial "Wie Copilot funktioniert".

### 4. Der Unterschied in einem Satz

Beispielformulierung: "Ohne Zugriff auf die eigenen Mails beschreibt Copilot nur, wie man zusammenfasst, statt tatsächlich zusammenzufassen — den Unterschied macht die **Datenbasis**."

Nicht ausreichend: "Die zweite Antwort war besser." Ohne Rückführung auf ein Kriterium fehlt die übertragbare Regel.

### 5. Anmeldestatus

| Beobachtung                       | Bewertung                                                                     |
| --------------------------------- | ----------------------------------------------------------------------------- |
| angemeldet mit dem Firmenkonto    | Unternehmensdatenschutz greift; Arbeitsinhalte sind in diesem Rahmen zulässig |
| nicht angemeldet / privates Konto | kein Unternehmensdatenschutz; keine Arbeitsinhalte eingeben                   |

Prüfweg: Kontoanzeige im Chat-Fenster öffnen und Kontoname bzw. Organisationszugehörigkeit ablesen.

## Häufige Fehler

| Fehler                                               | Korrektur                                                                     |
| ---------------------------------------------------- | ----------------------------------------------------------------------------- |
| Szenario 3 wird der Volllizenz zugeordnet            | Das Dokument wird mitgeliefert; Zugriff auf M365-Daten ist nicht erforderlich |
| Entscheidung allein über "Kosten"                    | Kosten sind ein Kriterium, entscheidend ist die Datenbasis                    |
| Leere Antwort in Szenario 2 als Tool-Fehler gedeutet | Fehlender Kontext erzeugt generische Antworten, keine Fehlermeldung           |

## Checkpoint

- Drei Entscheidungen mit je zwei benannten Kriterien liegen vor.
- Zwei tatsächlich erzeugte Antworten zu Szenario 2 liegen nebeneinander.
- Der Anmeldestatus ist geprüft und dokumentiert.

## Fallback

Ohne Volllizenz entfällt die zweite Variante in Aufgabe 3. Die Trainer-Demo zeigt den Unterschied; die Beobachtung aus Aufgabe 4 wird dann anhand der Demo formuliert.

## Erweiterung

Für den eigenen Vergleichsfall gilt dieselbe Regel: Sobald eigene Dokumente, Mails oder Termine Teil der Antwort sein sollen, führt kein Weg an der Volllizenz vorbei. Lässt sich die Quelle als Datei anhängen, genügt der Chat.
