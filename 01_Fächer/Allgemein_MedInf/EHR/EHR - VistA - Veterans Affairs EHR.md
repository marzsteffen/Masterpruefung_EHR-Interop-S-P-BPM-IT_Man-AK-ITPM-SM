---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Meaningful Use]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - VistA - Veterans Affairs EHR

> [!info] Kurzdefinition
> **VistA** (Veterans Health Information Systems and Technology Architecture) ist das EHR-System des **US Department of Veterans Affairs (VA)**. Es war vor 2009 das einzige große, voll integrierte EHR-System der USA und ist als Public Domain verfügbar – auch international eingesetzt.

## Beschreibung

Vor 2009 war die Nutzung von EHRs in den USA sehr limitiert. Größtes integriertes EHR-System war **VistA** der Veterans Affairs Administration. Diese US-Behörde versorgt Kriegsveteranen und ihre Familien.

## Bestandteile / Aufbau

### VA-Zahlen (laut Folie, Stand 2016):
- **8,7 Millionen Patienten**
- **1.700 Sites**: Medical Centers, Outpatient Clinics, Community Service Programs, Community-Based Outpatient Clinics

### Geschichte (laut Folie):

| Zeitraum | Ereignis |
|---|---|
| Ende 1970er | Programmierer in VA-Krankenhäusern entwickeln heimlich („underground") ein System zum Austausch medizinischer Informationen zwischen verschiedenen VA-Standorten. Bezeichnung: „Hardhats". |
| Ursprünglich | „Decentralized Hospital Computer Program (DHCP)" |
| 1981–1982 | Offizielle „Legalisierung" des Systems |
| Später | Umbenennung in **VistA** |
| Ab dann | **Public Domain**-Verfügbarkeit, Einsatz auch in anderen Ländern |

## Beispiel

VistA gilt als Lehrbuch-Beispiel dafür, wie ein **bottom-up** entstandenes IT-System in einer großen Versorgungsorganisation langfristig erfolgreich werden kann – im Gegensatz zu vielen top-down-mandatierten EHR-Roll-outs.

## Abgrenzung

- VistA ≠ private US-EHRs (Cerner, Epic, Allscripts) – letztere sind kommerziell, VistA ist Public Domain.
- VistA ≠ Tricare (Health-Insurance-Programm des Department of Defense) – verschiedene US-Behörden.
- Public Domain bedeutet: Quellcode öffentlich, jeder darf nutzen/anpassen – wurde z. B. in Mexiko, Jordanien, Indien adaptiert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist VistA und welche Rolle spielte es vor Beginn des Meaningful Use Programms?

**Anwendungsfrage:** Warum konnte sich VistA in den 1980ern als großes EHR durchsetzen, während die zivile US-Versorgung erst nach 2009 mit Meaningful Use folgte?

**Diskussionsfrage:** Public-Domain-Software in der Gesundheitsversorgung – welche Vorteile, welche Risiken? Lässt sich das auf europäische Kontexte übertragen?

**Mögliche Anschlussfragen:**
- Was ist die „Hardhats"-Geschichte und welche Lessons Learned ergeben sich daraus?
- Welche Auslandseinsätze von VistA sind dokumentiert?
- Wie verhält sich VistA zur aktuellen Modernisierung der VA mit Cerner Millennium / Oracle Health?
- Welche Rolle spielt der MUMPS-/M-Programmiersprachen-Kontext für VistA? (im PDF nicht erwähnt)

## Ergänzung außerhalb der Vorlesung

VistA basiert technisch auf der Programmiersprache **MUMPS (M)**, die auch viele andere Healthcare-IT-Systeme (Epic, Meditech) prägt. Seit 2017 läuft beim VA eine schrittweise Modernisierung: VistA wird sukzessive durch **Cerner Millennium** (jetzt Oracle Health) ersetzt – ein Großprojekt, das bisher mit erheblichen Verzögerungen und Kostensteigerungen kämpft.

## Verwandt

- [[EHR - VL - Meaningful Use]]
- [[EHR - HITECH Act und ARRA 2009]]
- [[EHR - Beispiel - Cerner PowerChart Office]]

## Quelle

- Vorlesung: [[EHR - VL - Meaningful Use]]
- Folien/Seitenangabe: Folien 3–6 (Geschichte, Numbers, History of VistA)
