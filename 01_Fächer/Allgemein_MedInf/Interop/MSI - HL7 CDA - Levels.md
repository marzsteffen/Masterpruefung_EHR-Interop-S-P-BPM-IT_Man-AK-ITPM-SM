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

# MSI - HL7 CDA - Levels

> [!info] Kurzdefinition
> CDA-Levels beschreiben die **Strukturierungsebene des Body**. Level 1 = unstrukturierter Body (NonXMLBody mit eingebettetem PDF, nur lesbar). Level 2 = Section-strukturierter Body (Abschnitte mit Codes). Level 3 = Entry-strukturierter Body (zusätzlich maschinenlesbare Einzelinformationen via Entries).

## Beschreibung

Wörtlich aus Folie 14:

> „Im CDA Body können Inhalte auf mehreren Strukturierungsebenen transportiert werden; diese Ebenen (umgangssprachlich ‚CDA-Levels') erlauben eine flexible Erweiterung der Interoperabilität von CDA Dokumenten.
>
> – ‚Unstrukturierter Body' (**‚CDA-Level 1'**) ist ausschließlich auf die Lesbarkeit durch Menschen ausgelegt. Medizinische Inhalte werden als Text, Bilder oder auch nur als ‚eingebettetes PDF' (als unstrukturierter ‚NonXMLBody') transportiert.
>
> – ‚Section-strukturierter Body' (**‚CDA-Level 2'**) ermöglicht eine Strukturierung der Inhalte nach Abschnitten (‚Sections') mit festgelegter Bedeutung (z. B. ‚Anamnese', ‚Diagnosen'). Die Abschnitte sind mit einem vereinbarten Code versehen, der es ermöglicht, dass EDV-Programme diese eindeutig erkennen und als Block verarbeiten können.
>
> – ‚Entry-strukturierter Body' (**‚CDA-Level 3'**) ist eine Technik zur Anreicherung eines lesbaren Dokuments mit medizinischen Einzelinformationen (z. B. ‚diastolischer Blutdruck', ‚ICD-10 Entlassungsdiagnose', ‚Körpergewicht in kg') durch Anwendung von CDA-Entries, die gemäß einer Vereinbarung maschinenlesbar codiert sind und daher automatisch in medizinische Informationssysteme integriert werden können."

## Bestandteile / Aufbau

| Level | Body-Form | Maschinenlesbarkeit | Typische Anwendung |
|---|---|---|---|
| 1 | NonXMLBody (PDF, Text, Bild) | Nur Header maschinenlesbar | Eingebettetes PDF |
| 2 | structuredBody mit Sections + codes | Section-Block-Ebene | Strukturierter Befund ohne Einzelelement-Codierung |
| 3 | structuredBody mit Sections + Entries | Auch Einzelinformationen codiert | ELGA EIS Full Support |

## Beispiel

Folie 15 zeigt drei Beispiele nebeneinander zur Erkennung:

**Level 1**: `<nonXMLBody>` mit `<text mediaType="application/pdf" representation="B64">JVBERi…` (Base64-PDF).

**Level 3**: `<entry typeCode="DRIV"><organizer>...<observation classCode="OBS" moodCode="EVN"><code code="8867-4" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC" displayName="Heart Beat"/>...<value xsi:type="PQ" value="60" unit="/min"/></observation>...` – Vital Sign mit LOINC-Code und PQ-Wert.

**Level 2**: `<component><section><templateId root="1.2.40.0.34.11.3.2.15" assigningAuthorityName="ELGA"/><code code="PFMED" displayName="Medikamentenverabreichung"…/><title>Medikamentenverabreichung</title><text>Klient nimmt Medikamente selbstständig ein…</text></section></component>` – Section mit Code und Narrative, ohne Entries.

## Abgrenzung

- **CDA-Level ≠ ELGA-EIS-Stufe**! Ein häufiger Verwechslungs­punkt. Siehe [[MSI - ELGA - EIS Stufen]].
- **CDA-Level 3 ≠ vollständig codiert**: auch Level-3-Dokumente können einzelne Sections nur mit Narrative haben.
- **CDA-Level 1 mit eingebettetem PDF ≠ unsicher**: das Dokument ist trotzdem ein gültiges CDA, nur eben mit minimaler Maschinen­lesbarkeit.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Was unterscheidet die drei CDA-Levels?

**Anwendungsfrage:** Erkennen Sie an einem Snippet, welches CDA-Level vorliegt.

**Diskussionsfrage:** Warum gibt es Level 1 überhaupt, wenn Level 3 mehr Funktionalität bietet? Welche Anwendungsfälle bleiben für Level 1?

**Mögliche Anschlussfragen:**
- Welcher EIS-Stufe entspricht ein Level-1-Dokument? (BASIC – siehe [[MSI - ELGA - EIS Stufen]])
- Wie wird die Maschinen­lesbarkeit eines Level-3-Eintrags konkret realisiert? → [[MSI - HL7 CDA - Laborparameter Entry]]
- Was ist ein NonXMLBody?

## Verwandt

- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 CDA - Body und Sections]]
- [[MSI - ELGA - EIS Stufen]]
- [[MSI - HL7 CDA - Laborparameter Entry]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 14, 15
