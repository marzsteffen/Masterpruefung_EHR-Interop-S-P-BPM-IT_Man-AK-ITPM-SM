---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Einfuehrung und Motivation]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Informationssicherheit - IT-Sicherheit vs Informationssicherheit

> [!info] Kurzdefinition
> IT-Sicherheit ist der technische Teil der Informationssicherheit. Informationssicherheit umfasst zusätzlich nicht-technische Informationsträger (Papier, gesprochenes Wort, Wissen) und betriebliche Strukturen.

## Beschreibung

Die Vorlesung positioniert IT-Sicherheit als echte Teilmenge der Informationssicherheit:

- **IT-Sicherheit:**
  - Schutz von technischen Systemen vor Bedrohungen und Schäden
  - Mittel: Zugriffskontrollen, Kryptographie
  - Ist Teil der Informationssicherheit

- **Informationssicherheit:**
  - Schutz von Informationen unabhängig vom Trägermedium
  - Umfasst auch nicht-technische Systeme (Papierarchive, Betriebsgelände usw.)
  - Berücksichtigt betriebliche Strukturen (Kommunikationswege, Richtlinien usw.)

Auf Folie 8 zeigt die Vorlesung vier Informationsarten: elektronische Daten, Wissen, gesprochenes Wort, Dokumente in Papierform. Folie 10 ordnet jeder dieser Arten Schutzmaßnahmen für die drei CIA-Schutzziele zu. Damit wird die Aussage „Informationssicherheit ≠ nur Daten in Computern" konkret.

## Bestandteile / Aufbau

| Aspekt | IT-Sicherheit | Informationssicherheit |
|---|---|---|
| Schutzobjekt | Technische Systeme | Informationen jeder Art |
| Reichweite | Hardware, Software, Netze | + Papier, Wissen, gesprochenes Wort |
| Maßnahmen | Zugriffskontrollen, Krypto | + Richtlinien, Betriebsabläufe, Schulung |
| Verhältnis | Teilmenge | Obermenge |

## Beispiel

Aus der Vorlesung (Folie 10): Vertraulichkeit von **Wissen** wird über *Vertraulichkeitsvereinbarungen* (NDAs) geschützt – das ist eine organisatorische Maßnahme der Informationssicherheit, keine IT-Sicherheits-Maßnahme. Vertraulichkeit von **elektronischen Daten** wird über Verschlüsselung geschützt – klassische IT-Sicherheit.

## Abgrenzung

- Wird häufig synonym verwendet, ist aber laut Vorlesung explizit nicht synonym.
- Cybersecurity (in der Folie nicht erwähnt – im PDF nicht definiert) ist umgangssprachlich oft mit IT-Sicherheit gleichgesetzt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worin unterscheiden sich IT-Sicherheit und Informationssicherheit?

**Anwendungsfrage:** Ordne konkrete Maßnahmen ein – z. B. abschließbarer Aktenschrank, NDA, TLS-Verschlüsselung, Onboarding-Schulung. Welche fallen unter IT-Sicherheit, welche „nur" unter Informationssicherheit?

**Diskussionsfrage:** Warum reicht reine IT-Sicherheit nicht aus, um den Datenschutz im Krankenhaus sicherzustellen? Welche Rolle spielen organisatorische Maßnahmen?

**Mögliche Anschlussfragen:**
- Wie schützt man die Verfügbarkeit von Wissen, wenn ein Mitarbeiter ausscheidet? (Antwort laut Folie 10: Wissenstransfer, Vertretungen.)
- Welche Schutzziele aus der CIA-Triade adressiert eine Vertraulichkeitsvereinbarung?

## Verwandt

- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - Security Eigenschaften - Uebersicht]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folien 8, 10, 11
