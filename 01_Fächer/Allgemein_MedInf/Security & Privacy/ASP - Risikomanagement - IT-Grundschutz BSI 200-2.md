---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Informationssicherheits-Risikomanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Risikomanagement - IT-Grundschutz BSI 200-2 (Bausteine)

> [!info] Kurzdefinition
> BSI-Standard 200-2 IT-Grundschutz-Methodik. Strukturiert IT-Sicherheit über das IT-Grundschutz-Kompendium mit Bausteinen, Gefährdungs- und Maßnahmenkatalogen. Bausteine sind in zwei Klassen organisiert: Prozess-Bausteine (ISMS, ORP, CON, OPS) und System-Bausteine (APP, SYS, IND, NET, INF).

## Beschreibung

Folien 24–27 stellen die IT-Grundschutz-Methodik vor.

### IT-Grundschutz-Kompendium (Folie 25)
Beinhaltet:
- **IT-Grundschutz-Bausteine.**
- **Gefährdungskataloge.**
- **Maßnahmenkataloge.**

### Prozess-Bausteine (Folie 26)
Decken organisatorische und prozessuale Themen ab:
- **ISMS:** Sicherheitsmanagement.
- **ORP:** Organisation und Personal.
- **CON:** Konzeption und Vorgehensweisen.
- **OPS:** Betrieb.

### System-Bausteine (Folie 26)
Decken technische Themen ab:
- **APP:** Anwendungen.
- **SYS:** IT-Systeme.
- **IND:** Industrielle IT.
- **NET:** Netze und Kommunikation.
- **INF:** Infrastruktur.

### Aufbau eines Bausteins (Folie 27, Beispiel SYS.1.5 Virtualisierung)
Pro Baustein gibt es:
- **Spezifische Gefährdungen** (z. B. „Fehlerhafte Planung der Virtualisierung", „Unzureichende Ressourcen für virtuelle IT-Systeme").
- **Elementare Gefährdungen** (z. B. G 0.18 Fehlplanung, G 0.21 Manipulation von Hard- oder Software).
- **Anforderungen in drei Stufen:**
  - **Basis-Anforderungen** (z. B. Einspielen von Aktualisierungen und Sicherheitsupdates).
  - **Standard-Anforderungen** (z. B. Netzplanung für virtuelle Infrastrukturen).
  - **Anforderungen bei erhöhtem Schutzbedarf** (z. B. Verwendung von hochverfügbaren Architekturen, Härtung des Virtualisierungsservers).

## Bestandteile / Aufbau

| Kategorie | Bausteine | Inhalt |
|---|---|---|
| Prozess | ISMS, ORP, CON, OPS | Management, Organisation/Personal, Konzeption, Betrieb |
| System | APP, SYS, IND, NET, INF | Anwendungen, IT-Systeme, Industrielle IT, Netze, Infrastruktur |

Pro Baustein: spezifische + elementare Gefährdungen, Anforderungen in 3 Stufen.

## Beispiel

Direkt aus Folie 27, Baustein **SYS.1.5 Virtualisierung**: spezifische Gefährdungen wie „Fehlerhafte Planung der Virtualisierung"; Basis-Anforderungen wie „Einspielen von Aktualisierungen"; Standard-Anforderungen wie „Netzplanung für virtuelle Infrastrukturen"; Anforderungen bei erhöhtem Schutzbedarf wie „Härtung des Virtualisierungsservers".

## Abgrenzung

- **BSI 200-2 ≠ BSI 200-4:** 200-2 ist allgemeine IT-Grundschutz-Methodik; 200-4 ist BCM-spezifisch (siehe [[ASP - BCM - Normen]]).
- **BSI vs. ISO 27001:** ISO 27001 ist abstrakter Rahmen; BSI 200-2 ist konkrete Methodik mit dicker Bausteinsammlung.
- **Bausteine sind keine Risiken**, sondern Strukturierungsansätze. Sie werden in der Risikoidentifikation als Vorlagen genutzt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist BSI 200-2? Welche zwei Klassen von Bausteinen gibt es, und welche Bausteine fallen in jede Klasse?

**Anwendungsfrage:** Welcher Baustein passt auf welches Asset? (KIS-Anwendung → APP; Server → SYS; Netzwerk → NET; Serverraum → INF; Backup-Prozess → OPS.)

**Diskussionsfrage:** Welche Vor- und Nachteile hat die Bindung der Risikoanalyse an einen vordefinierten Baustein-Katalog? (Vorteil: Vollständigkeit, vergleichbare Ergebnisse. Nachteil: Bürokratie, kann Innovation und seltenere Szenarien übersehen.)

**Mögliche Anschlussfragen:**
- Was sind elementare Gefährdungen? (Generische Gefahren-Klassen, mit „G 0.x"-IDs.)
- Was unterscheidet Basis-, Standard- und „erhöhter Schutzbedarf"-Anforderungen?
- Welcher Baustein ist relevant für eine medizinische Industrieanlage? (IND – Industrielle IT.)

## Verwandt

- [[ASP - Risikomanagement - Asset-basierte Identifikation]]
- [[ASP - Risikomanagement - Strukturanalyse und Schutzbedarf]]
- [[ASP - BCM - Normen]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 24–27
- Standard: BSI 200-2 IT-Grundschutz-Methodik
