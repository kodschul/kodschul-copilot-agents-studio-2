# Nordwind Consulting – IT-Richtlinie (Auszug)

Wissensquelle für den internen Support-Agenten aus Lab 7.2/7.3. Alle Angaben sind fiktiv und anonymisiert.

## Geltungsbereich

Diese Richtlinie gilt für alle Mitarbeitenden der Nordwind Consulting GmbH mit einem Firmengerät oder Zugriff auf Nordwind-IT-Systeme.

## VPN und Remote-Zugriff

| Feld                 | Wert                                                                     |
| -------------------- | ------------------------------------------------------------------------ |
| VPN-Client           | Cisco Secure Client (AnyConnect)                                         |
| Verbindungsziel      | vpn.nordwind-consulting.example                                          |
| Authentifizierung    | Firmen-Login + Multi-Faktor-Authentifizierung (Authenticator-App)        |
| Zuständig für Zugang | IT-Support (it-support@nordwind-consulting.example)                      |
| Gültigkeitsdauer     | VPN-Zertifikat läuft automatisch nach 12 Monaten ab, Erneuerung durch IT |

**Kurzanleitung:** Cisco Secure Client installieren (Standard-Image auf allen Firmengeräten vorinstalliert) → Verbindungsziel eingeben → mit Firmen-Login und MFA anmelden.

## Geräte- und Passwortrichtlinie

- Firmengeräte müssen vollverschlüsselt sein (BitLocker bzw. FileVault) und aktuelle Sicherheitsupdates installiert haben.
- Passwörter: mindestens 12 Zeichen, alle 180 Tage Wechsel, kein Wiederverwenden der letzten 5 Passwörter.
- Multi-Faktor-Authentifizierung ist für alle Microsoft-365-Konten verpflichtend.
- Private Geräte dürfen nur über die mobile Outlook-/Teams-App mit App-Schutzrichtlinie genutzt werden, nicht über VPN.

## IT-Support-Kontakt

| Kanal           | Erreichbarkeit                         |
| --------------- | -------------------------------------- |
| Ticket-Portal   | it-support.nordwind-consulting.example |
| E-Mail          | it-support@nordwind-consulting.example |
| Telefon-Hotline | werktags 08:00–18:00 Uhr               |

## Eskalation

Fragen, die nicht durch diese Richtlinie oder den Onboarding-Leitfaden abgedeckt sind (z. B. individuelle Sonderberechtigungen, Gehaltsfragen, personenbezogene Ausnahmen), werden nicht durch den Support-Agenten beantwortet, sondern an das IT-Support-Ticket-Portal bzw. an HR eskaliert.

## Grenzen dieser Richtlinie

Diese Richtlinie deckt Standardfragen ab. Sie ersetzt keine individuelle Sicherheitsfreigabe und keine rechtliche Beratung.
