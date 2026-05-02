---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Identitaetsmanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Identitätsmanagement - Lebenszyklus

> [!info] Kurzdefinition
> Vier Phasen einer digitalen Identität – Erstellung, Verwendung, Wartung, Löschung – umgeben von der dauerhaft gültigen Phase Governance.

## Beschreibung

Folien 19–21 stellen den Lebenszyklus mit fünf Phasen dar (Folien-Diagramm):

```
        Erstellung → Verwendung → Löschung
                         ↑   ↓
                         Wartung
                         (alles unter Governance)
```

### Erstellung (Folie 19)
- **Registrierungsprozess:** Wie werden Daten zur Erstellung der digitalen Identität erhoben?
- **Erstellung der Anmeldedaten:** Welche Authentifizierungsmittel müssen erstellt werden?
- Wo werden Authentifizierungsmittel gespeichert?
- Prüfung und Verifizierung von Attributen notwendig?

### Verwendung (Folie 19)
- **Verwendungsbereich und Autorisierung:** Auf welche Anwendungen haben die digitalen Identitäten Zugriff?
- **Authentifizierungsprozess:**
  - Wer führt die Authentifizierung durch?
  - Wie läuft der Authentifizierungsprozess ab?
  - Welches Protokoll wird für den Authentifizierungsprozess verwendet? (Identitätsprotokoll)

### Wartung (Folie 20)
- Können Attribute verändert werden? Von wem?
- Welche Attribute müssen unverändert bleiben? (z. B. IDs)
- Haben Attribute selbst eine gewisse Lebensdauer? (z. B. Ablauf von Zertifikaten, Lizenzen)

### Löschung (Folie 20)
- Wie können digitale Identitäten widerrufen werden?
- Werden digitale Identitäten nach einer gewissen Zeit automatisch gelöscht?
- Wie werden betroffene Systeme von der Löschung informiert?
- Wird die Löschung dokumentiert?

### Governance (Folie 21)
- **Erstellung von Richtlinien/Policies für:**
  - Erstellung, Verwendung, Wartung und Löschung
  - Authentifizierung (gefordertes Sicherheitslevel)
  - Autorisierung (Zugriffsregelungen)
  - Rückverfolgbarkeit einzelner Aktivitäten (Monitoring, Logging)
- Überwacht die Einhaltung der Policies.
- Basiert oft auf rechtlichen Vorgaben.

## Bestandteile / Aufbau

| Phase | Kernfragen |
|---|---|
| Erstellung | Datenerhebung, Anmeldedaten, Speicherung, Verifizierung |
| Verwendung | Authentifizierung, Autorisierung, Protokoll |
| Wartung | Attributänderungen, IDs unverändert, Ablaufdaten |
| Löschung | Widerruf, automatische Löschung, Information, Dokumentation |
| Governance | Policies, Überwachung, rechtliche Basis (DSGVO) |

## Beispiel

ELGA-Identität: **Erstellung** durch ID-Austria-Registrierung mit eigener Identitätsprüfung. **Verwendung** beim Zugriff auf die elektronische Gesundheitsakte. **Wartung** bei Namensänderung. **Löschung** bei Tod oder Opt-out. **Governance** durch ELGA-Verordnung und DSGVO.

## Abgrenzung

- Der Lebenszyklus betrifft die **Identität als solche**, nicht einzelne Sitzungen. Eine Sitzung hat ihren eigenen, kürzeren Lebenszyklus.
- Wartung und Löschung greifen oft auf dieselben Mechanismen wie die Zertifikats-Verwaltung zurück (CRL, OCSP – siehe [[ASP - Zertifikate - PKI]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Phasen umfasst der IdM-Lebenszyklus, und was ist Governance?

**Anwendungsfrage:** Beschreiben Sie für ein eHealth-System die typischen Aktivitäten in jeder Phase. Was passiert konkret bei der Wartung, was bei der Löschung?

**Diskussionsfrage:** Welche DSGVO-Pflichten greifen in welchen Phasen? (Datenminimierung in Erstellung; Speicherbegrenzung in Löschung; Integrität & Vertraulichkeit in Wartung; Zweckbindung in Verwendung.) Welche Phase ist in der Praxis am häufigsten unzureichend umgesetzt? (Löschung – „untote Konten" sind ein häufiges Problem.)

**Mögliche Anschlussfragen:**
- Wer übernimmt typischerweise die Governance-Funktion?
- Welche technischen Mechanismen unterstützen die Löschung über Systemgrenzen hinweg?
- Wie hängt der Lebenszyklus mit dem Identitätsprotokoll zusammen?

## Verwandt

- [[ASP - Identitaetsmanagement - Definition]]
- [[ASP - Identitaetsmanagement - Akteure]]
- [[ASP - DSGVO - Grundsaetze]]
- [[ASP - Zertifikate - PKI]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folien 19, 20, 21
