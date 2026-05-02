---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - Implementation Guide

> [!info] Kurzdefinition
> Ein Implementation Guide (IG) ist eine Sammlung von FHIR-Profilen, Value Sets, CodeSystems und weiteren Artefakten, die gemeinsam einen klinischen oder technischen Anwendungsfall spezifizieren. IGs sind das Hauptmittel, um aus dem generischen FHIR-Standard eine interoperable Lösung zu machen.

## Beschreibung

Seite 4 verweist auf folgende Referenz-IGs als Beispiele:

- **International Patient Summary (IPS):** `https://hl7.org/fhir/uv/ips/`
- **AT Core Profile (Österreich, R5):** `https://fhir.hl7.at/r5-core-main/index.html`
- **FHIR Profiling Spezifikation:** `https://hl7.org/fhir/profiling.html`

Die Vorlesung stellt drei Fragen, die das Selbststudium der IG-Dokumentation strukturieren:

1. Unter welchem Tab findet man die Profile der Ressourcen?
2. Was ist der Unterschied zwischen dem **Differential Table** und dem **Snapshot Table**?
3. Wie dürfen Kardinalitäten eingeschränkt werden?

Diese Fragen werden im PDF nicht beantwortet – sie verweisen auf die externe Dokumentation. Die Inhalte sind im PDF nicht definiert.

## Bestandteile / Aufbau

Im PDF nicht ausgeführt. Folgende Begriffe werden erwähnt (ohne Definition):

| Begriff | Kontext |
|---|---|
| Differential Table | Zeigt nur die Änderungen gegenüber dem Basisprofil |
| Snapshot Table | Zeigt alle Elemente inkl. geerbter Felder vollständig |
| Kardinalität | Einschränkung der Multiplizität eines Elements im Profil |

> **Hinweis:** Differential Table vs. Snapshot Table ist im PDF nur als Frage gestellt, nicht erklärt. Antwort im Selbststudium über `https://hl7.org/fhir/profiling.html` erarbeiten.

## Beispiel

- IPS als internationaler IG: definiert, welche Ressourcen und Value Sets in einer Patienten-Kurzakte verpflichtend sind.
- AT Core Profile als nationaler IG für Österreich auf Basis von FHIR R5.

## Abgrenzung

- **Implementation Guide ≠ Profil**: Ein Profil (StructureDefinition) ist ein einzelnes Artefakt; ein IG ist ein Paket, das viele Profile + andere Artefakte bündelt.
- **Differential Table ≠ Snapshot Table**: Differential zeigt nur Abweichungen vom Basisprofil; Snapshot zeigt das vollständige Bild inklusive aller geerbten Elemente. (Im PDF nicht erklärt – Ergänzung aus FHIR-Spezifikation.)
- **IG ≠ Standard**: Ein IG ist eine Anwendung des FHIR-Standards auf einen Kontext, kein Standard selbst.

## Prüfungsrelevanz

**Hoch** (insbesondere Differential vs. Snapshot Table ist ein klassisches Prüfungsthema).

**Typische Definitionsfrage:** Was ist ein FHIR Implementation Guide?

**Anwendungsfrage:** Wo findet man in der IG-Dokumentation, welche Elemente ein Profil gegenüber der Basisressource einschränkt?

**Diskussionsfrage:** Warum reicht der FHIR-Standard allein nicht für Interoperabilität? Was leisten Implementation Guides zusätzlich?

**Mögliche Anschlussfragen:**
- Was zeigt der Differential Table, was der Snapshot Table? (→ im PDF als Frage gestellt, Details in externer Spec)
- Welche Kardinalitätsseinschränkungen sind in FHIR-Profilen erlaubt? (→ 0..* → 1..*, aber nie Erweiterung)
- Welche österreichischen IGs kennen Sie? (→ AT Core Profile, ELGA-Leitfäden)

## Verwandt

- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - FHIR Shorthand (FSH) und SUSHI]]
- [[MSI - HL7 FHIR - Versionen]]
- [[MSI - HL7 - International Patient Summary]]

## Quelle

- Vorlesung: [[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]
- Folien/Seitenangabe: Seite 4
