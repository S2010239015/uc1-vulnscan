# UC1 - Vulnerability Scanning

Use Case 1 für die Masterarbeit: Vergleich von Vulnerability Scannern in einer kontrollierten Umgebung.

## Topologie

- **target** (192.168.20.5) — Ubuntu mit absichtlichen Schwachstellen (CVEs, schwache Konfigs, unsichere Services)
- **scanner** (192.168.20.10) — Ubuntu mit vorinstallierten Open-Source Scannern (OpenVAS, Nuclei)
- **router** — verbindet beide Netze

## Zu vergleichende Scanner

| Scanner | Typ | Installation |
|---------|-----|--------------|
| OpenVAS | Open Source, klassisch | automatisch |
| Nuclei | Open Source, template-basiert | automatisch |
| Nessus Essentials | kommerziell | manuell (siehe README auf Scanner-Host) |

## Eingebaute Schwachstellen

Verschiedene Kategorien:
- Schwache Authentisierung (Passwörter, anonymous FTP)
- Unsichere Dienste (Telnet, RSH, TFTP)
- Apache Fehlkonfigurationen
- Verwundbare Webanwendung (SQLi, RCE, Path Traversal)
- Unsichere Samba/NFS Shares
- Sudo Fehlkonfigurationen
- Schwache SSH Konfiguration
