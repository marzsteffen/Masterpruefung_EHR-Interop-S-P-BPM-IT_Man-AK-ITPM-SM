---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - Paper - Why Digital Medicine Depends on Interoperability]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Interoperabilitätsebenen - Syntaktisch

> [!info] Kurzdefinition
> Syntaktische Interoperabilität spezifiziert Format und Struktur der ausgetauschten Daten (z. B. in einem XML-Dokument). Sie ist die Voraussetzung dafür, dass die Daten überhaupt geparst werden können – ohne sie zu „verstehen".

## Beschreibung

Wörtlich aus Lehne et al. (2019), Sektion „Syntactic interoperability":

> „Syntactic interoperability specifies the format and structure of the data (for example, in an XML document). The structured exchange of health data is supported by international standards development organizations (SDOs) such as Health Level Seven International (HL7) or Integrating the Healthcare Enterprise (IHE)."

Konkret nennt das Paper als syntaktische Standards:
- **HL7 FHIR** als „emerging standard for the communication of health data … defines around 140 common healthcare concepts, so-called resources, which can be accessed and exchanged using modern web technologies." Wird zunehmend für mobile Health-Apps eingesetzt.
- **openEHR** als alternative Initiative: erlaubt klinischen Fachpersonen und IT-Experten, klinische Inhalte über sogenannte **Archetypes** zu definieren, basierend auf einem Reference Model. openEHR enthält außerdem die **Archetype Querying Language (AQL)** zum portablen Abfragen sowie Tools zum Definieren und Publizieren der Archetypes.

## Bestandteile / Aufbau

Syntaktische Interoperabilität betrifft (laut Paper):
- Format (z. B. XML, JSON)
- Struktur (Felder, Hierarchie)
- Standardisierungs-Gremien als Träger (HL7, IHE)
- Konkrete Spezifikationen: FHIR, openEHR

## Beispiel

Aus dem Paper: HL7 FHIR mit etwa 140 Resources, modern Web-API-tauglich. Eine FHIR-Resource hat ein definiertes JSON-Schema – das ist syntaktische Festlegung. Was ein Code wie `8867-4` *bedeutet*, regelt erst die semantische Schicht (LOINC).

## Abgrenzung

- **Syntaktisch ≠ technisch.** Technisch sichert die Übertragung A→B, syntaktisch sichert das Format der übertragenen Bytes.
- **Syntaktisch ≠ semantisch.** Ein FHIR-Patient kann syntaktisch valide sein und trotzdem unbrauchbare Daten enthalten, wenn die Codes/Werte nicht bedeutungsvoll sind.
- **Syntaktisch ≠ Profilierung.** Profile (z. B. ELGA-FHIR-Profile) schränken den Standard für einen Use Case ein – sie sind eine spezialisierte Anwendung von syntaktischen Spezifikationen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was regelt syntaktische Interoperabilität, und wodurch grenzt sie sich von technischer und semantischer ab?

**Anwendungsfrage:** Ein FHIR-Server liefert ein wohlgeformtes JSON, aber die `code`-Felder sind frei vergebene Texte. Welche Ebene fehlt – syntaktisch oder semantisch?

**Diskussionsfrage:** Argument: „FHIR macht Syntax und Semantik gleichzeitig". Stimmt das? (Antwort des Papers: nein – FHIR liefert die Hülle, die Bedeutung kommt aus Terminologien.)

**Mögliche Anschlussfragen:**
- Welche SDOs sind für syntaktische Standards verantwortlich?
- Warum ist openEHR ein alternativer syntaktischer Ansatz zu FHIR?
- Wie verhält sich HL7 CDA zu syntaktischer Interoperabilität?

## Verwandt

- [[MSI - Interoperabilitätsebenen - Vier-Ebenen-Modell Lehne]]
- [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]
- [[MSI - openEHR - Archetypes]]
- [[MSI - HL7 FHIR - Resource]] (Querverweis Vorlesung 06)
- [[MSI - HL7 CDA - Header]] (Querverweis Vorlesung 04)

## Quelle

- Vorlesung: [[MSI - Paper - Why Digital Medicine Depends on Interoperability]]
- Folien/Seitenangabe: Sektion „Syntactic interoperability", S. 2 des Papers
