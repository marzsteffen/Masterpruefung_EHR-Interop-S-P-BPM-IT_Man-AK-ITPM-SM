---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 CDA und e-Befunde]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 CDA - Eigenschaften

> [!info] Kurzdefinition
> Sechs definierende Eigenschaften eines CDA-Dokuments laut Folie 11: **Persistenz, Verwaltung (stewardship), Kontext, Authentisierung (potential für authentication), Ganzheit (wholeness), Lesbarkeit (human readability)**. Diese Eigenschaften sind Voraussetzung dafür, dass ein Dokument als „medizinisches Dokument" im Sinne von CDA gilt.

## Beschreibung

Wörtlich aus Folie 11:

- **Persistenz**: Medizinische Dokumente sind durch Persistenz, also dauerhafte Existenz in den sendenden oder empfangenden Systemen gekennzeichnet, wo sie für einen bestimmten Zeitraum in einem unveränderten Zustand bleiben. Dieser Zeitraum wird durch lokale Regelungen definiert.
- **Verwaltung** (engl. „stewardship"): Für die Verwaltung des Dokuments ist eine bestimmte Organisation verantwortlich (der „Custodian").
- **Kontext**: Medizinische Dokumente etablieren den Standard-Kontext für die in ihnen gespeicherten Inhalte (z. B. den „Entlassungsbrief").
- **Authentisierung** (engl. „potential für authentication"): Medizinische Dokumente werden authentisiert. Im medizinischen Alltag entspricht das der Signierung, Vidierung oder Validierung.
- **Ganzheit** (engl. „wholeness"): Die Authentisierung eines medizinischen Dokumentes bezieht sich auf das Dokument als Ganzes und nicht nur auf einzelne aus dem Kontext gelöste Teile.
- **Lesbarkeit** (engl. „human readability"): Medizinische Dokumente sind für Menschen lesbar. Zusätzlich:
  - Es muss einen eindeutig festgelegten Weg für einen Empfänger geben, den authentifizierten Inhalt sichtbar zu machen.
  - Es ist nicht zulässig, dass die Darstellung im Browser nur mithilfe eines bestimmten Stylesheets bewerkstelligt werden kann, das zusammen mit dem CDA-Dokument gesendet werden muss. Es muss möglich sein, den Inhalt mit einem beliebigen Stylesheet und marktüblichen Browsern darzustellen.
  - Lesbarkeit bezieht sich auf den authentifizierten Inhalt. Zusätzlich kann weitere Information im Dokument vorhanden sein („CDA Level 3"), die auf Auswertbarkeit durch Anwendungssysteme abzielt, die aber nicht authentifiziert oder lesbar dargestellt werden muss.

## Bestandteile / Aufbau

Sechs orthogonale Eigenschafts-Achsen:

| Eigenschaft | Englisch | Bedeutung |
|---|---|---|
| Persistenz | persistence | dauerhafte Existenz, unverändert |
| Verwaltung | stewardship | verantwortlicher Custodian |
| Kontext | context | Standard-Kontext für Inhalte |
| Authentisierung | potential for authentication | Signatur/Vidierung/Validierung |
| Ganzheit | wholeness | Auth bezieht sich auf das Ganze |
| Lesbarkeit | human readability | für Menschen lesbar, ohne mitgeliefertes Stylesheet |

## Beispiel

Aus Folie 10: Der `<legalAuthenticator>` mit `<signatureCode code="S"/>` und einer assignedEntity (Dr. Cardiologist) instanziiert das **Authentisierungs-Potenzial**. Die enthaltenen Daten beziehen sich auf das gesamte Dokument (**Ganzheit**). Der Custodian-Eintrag adressiert die **Verwaltung**.

## Abgrenzung

- **Lesbarkeit ≠ Stylesheet-abhängig**: Eine Lesedarstellung muss auch ohne das mitgesendete Stylesheet möglich sein. Stylesheets sind Empfehlung, keine Pflicht.
- **Authentisierung ≠ Verschlüsselung**: Authentisierung sichert Urheber/Inhalt; Verschlüsselung ist eine Transport-/Speicherungs-Schicht und nicht Teil der CDA-Eigenschaften.
- **Persistenz ≠ Versionierung**: Persistenz heißt „unveränderter Zustand"; eine neue Version ist ein neues Dokument.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche sechs Eigenschaften definieren ein CDA-Dokument?

**Anwendungsfrage:** Welcher CDA-Header-Eintrag adressiert welche Eigenschaft?

**Diskussionsfrage:** Warum wird verlangt, dass ein CDA-Dokument auch ohne mitgeliefertes Stylesheet lesbar ist? Was wäre die Konsequenz, wenn das nicht so wäre?

**Mögliche Anschlussfragen:**
- Was ist ein „Custodian"?
- Was bedeutet „signatureCode"?
- Wie verhält sich „Ganzheit" zur Versionierung eines CDA-Dokuments?
- Welche Cimino-Desiderata adressieren ähnliche Themen wie Persistenz und Wholeness? → [[MSI - Terminologie - Cimino Desiderata]]

## Verwandt

- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 CDA - Header]]
- [[MSI - HL7 CDA - Stylesheet und Validierung]]
- [[ASP - MOC]] (Authentifizierung-Querbezug)

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 11
