---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - Grundlagen klinischer Kernprozess]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - Klinischer Kernprozess - Diagnostische Schleife

> [!info] Kurzdefinition
> Die **diagnostische Schleife** ist die erste der beiden Schleifen des medizinischen Falls. Sie führt von **Anamnese + Status** über eine **Verdachtsdiagnose** und gezielte **Untersuchungen** zu einer **Diagnose** – oder, falls die Untersuchungen die Verdachtsdiagnose nicht bestätigen, zurück zum Neustart der Schleife.

## Beschreibung

Folie 28 des VL-I-PDFs. Die diagnostische Schleife wird als zyklisch dargestellt:

```
ANAMNESE
   +
STATUS
   ↓
VERDACHTSDIAGNOSE
   ↓
UNTERSUCHUNGEN
   ↓
DIAGNOSE
   ODER
NEUSTART DIAGNOSTISCHE SCHLEIFE
```

### Stationen der Schleife

| Station | Inhalt |
|---|---|
| **Anamnese + Status** | strukturiertes Patientengespräch + körperliche Untersuchung; Ausgangspunkt jeder Diagnostik (siehe [[BPM - VL - Anamnese Status Differentialdiagnose]] in VL III) |
| **Verdachtsdiagnose** | erste Hypothese auf Basis von Anamnese und Status |
| **Untersuchungen** | gezielte Tests zur Bestätigung oder Verwerfung der Verdachtsdiagnose (Labor, Bildgebung, Funktionsdiagnostik) |
| **Diagnose** | bestätigte Diagnose mit hinreichender Sicherheit |
| **Neustart** | wenn die Untersuchungen die Verdachtsdiagnose nicht bestätigen, Rücksprung zur erneuten Anamnese / Status / neue Verdachtsdiagnose |

### Grundsätzlich gilt: Untersuchungen sind hypothesengeleitet

Die Schleife setzt voraus, dass Untersuchungen zur Bestätigung/Verwerfung einer **konkreten Hypothese** angeordnet werden. Routine-Untersuchungen ohne Hypothese sind eine Form von Verschwendung (vgl. [[BPM - Waste - Sechs Domaenen]] – „Overtreatment / Low-Value Care") und werden in den Vorlesungen zu Choosing Wisely kritisiert (vgl. [[BPM - Paper - Choosing Wisely]]).

## Bestandteile / Aufbau

- 4 Stationen (Anamnese+Status, Verdachtsdiagnose, Untersuchungen, Diagnose)
- 1 Reentry (Neustart, wenn Diagnose nicht bestätigt)

## Beispiel

Hernien-Diagnostik:
- Anamnese: Leistenschmerz beim Heben, Schwellung in der Leiste.
- Status: tastbarer Bruchsack, Valsalva-Test positiv.
- Verdachtsdiagnose: Inguinalhernie.
- Untersuchungen: Sonografie mit Valsalva-Manöver bei Unklarheit (CT/MRI nur falls Klinik + US inkonklusiv – siehe SOP Hernie).
- Diagnose: K40.x ICD-10.

Falls die Sonografie die Diagnose ausschließt: Neustart mit erweiterter Differentialdiagnose (Lymphknoten, Lipom, Femoralhernie, …).

## Abgrenzung

- **Diagnostische Schleife ≠ therapeutische Schleife.** Diagnostisch klärt *was ist*; therapeutisch klärt *was tun*. Vgl. [[BPM - Klinischer Kernprozess - Therapeutische Schleife]].
- **Verdachtsdiagnose ≠ Diagnose.** Verdachtsdiagnose ist Hypothese, Diagnose ist bestätigt. Falsche Gleichsetzung führt zu unnötigen Therapien.
- **Untersuchung ≠ Screening.** Untersuchungen in dieser Schleife sind hypothesengeleitet; Screening ist populationsbasiert ohne konkrete Verdachtsdiagnose.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Beschreiben Sie die diagnostische Schleife des medizinischen Falls."

**Anwendungsfrage:** „Wann startet die diagnostische Schleife neu, und welche Konsequenzen hat das für die Pfadmodellierung?" – Modellierung muss explizit Loops vorsehen (vgl. BPMN-Gateway-Modellierung).

**Diskussionsfrage:** Welche Verschwendung entsteht, wenn die Schleife *nicht* als Schleife, sondern als linearer Pfad modelliert ist? – Zwangs-Folge: erweiterte Diagnostik wird umgangen oder Neustart wird intransparent durchgeführt; die Komplikationsrate steigt. Bezug zu „Variation in Medical Practice" und „Choosing Wisely".

**Mögliche Anschlussfragen:**
- Welche Stationen umfasst die Schleife?
- Wann ist eine Untersuchung wertschöpfend, wann nicht?
- Wie hängt das mit Differentialdiagnose zusammen?

## Verwandt

- [[BPM - Klinischer Kernprozess - Definition]]
- [[BPM - Klinischer Kernprozess - Therapeutische Schleife]]
- [[BPM - VL - Anamnese Status Differentialdiagnose]]
- [[BPM - Waste - Sechs Domaenen]]
- [[BPM - Paper - Choosing Wisely]]
- [[BPM - Klinischer Pfad - Definition]]

## Quelle

- Vorlesung: [[BPM - VL - Grundlagen klinischer Kernprozess]]
- Folien/Seitenangabe: Folie 28
