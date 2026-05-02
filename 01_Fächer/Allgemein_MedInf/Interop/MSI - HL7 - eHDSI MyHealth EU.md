---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Terminologien Anwendung]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 - eHDSI MyHealth EU

> [!info] Kurzdefinition
> eHDSI (*eHealth Digital Service Infrastructure*) ist die EU-Infrastruktur für den grenzüberschreitenden Austausch von Gesundheitsdaten (z. B. ePrescription, Patient Summary). Sie nutzt eine **NCP-zu-NCP-Architektur** (National Contact Point) mit harmonisierten Value Sets. Die Folge­bezeichnung lautet **My health @ EU**.

## Beschreibung

Folie 33 stellt die NCP-zu-NCP-Architektur vor:

> „eHDSI (eHealth Digital Service Infrastructure): Kommunikation über Staats- und Sprachengrenzen hinweg
> eHDSI Value Sets auf https://termgit.elga.gv.at/ einsehbar"

Schema (Folie 33):
```
NCP COUNTRY A                                  NCP COUNTRY B
Prescription Provider  ───── Prescription ────► Dispense Provider
Patient ↔ Prescriber                           Dispense Provider ↔ Patient
                       ◄── Dispensed medicine
                            datasets
```

Folie 34 zeigt das Folge-Branding:

> „My health @ EU – eHealth Digital Service Infrastructure – A service provided by the European Union"

Verlinkt: „Elektronische grenzüberschreitende Gesundheitsdienste (europa.eu)".

## Bestandteile / Aufbau

| Komponente | Funktion |
|---|---|
| **NCP** (National Contact Point) | nationaler Übergabepunkt pro Mitgliedstaat |
| Prescription Provider | erstellt Verschreibung im Heimatland |
| Dispense Provider | gibt Arzneimittel im Aufenthaltsland ab |
| Datasets | ePrescription, Dispensed medicine, Patient Summary |
| Harmonisierte Value Sets | über `termgit.elga.gv.at/` einsehbar (für AT) |
| Branding | „My health @ EU" (Nachfolger von eHDSI) |

## Beispiel

Aus dem Folien-Schema: Patient bekommt in Land A ein Rezept; reist in Land B; dort wird das Rezept über NCP A → NCP B abgerufen, im Land B dispensiert; das Dispensed-medicine-Dataset fließt zurück. Beides läuft über harmonisierte Value Sets, damit die Codes in beiden Ländern verständlich sind.

## Abgrenzung

- **eHDSI ≠ ELGA**. ELGA ist ein nationales eHealth-System; eHDSI/MyHealth@EU ist die EU-übergreifende Brücke.
- **NCP ≠ Endpoint des Health Providers**. Der NCP ist der nationale Hub – Health Provider haben Zugang über ihre eigenen Systeme, die mit dem NCP integriert sind.
- **eHDSI ≠ International Patient Summary**. IPS ist eine Spezifikation (HL7 + CEN), eHDSI ist die Infrastruktur, die u. a. IPS-Dokumente austauscht.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eHDSI / MyHealth@EU? Welche Architektur nutzt es?

**Anwendungsfrage:** Sie sind Österreicher und brauchen ein Rezept in Italien. Wie läuft der Datenaustausch über eHDSI?

**Diskussionsfrage:** Welche Hürden bleiben trotz harmonisierter Value Sets? (organisatorische Interoperabilität, gesetzliche Rahmen, Sprache.)

**Mögliche Anschlussfragen:**
- Welche Datasets unterstützt eHDSI aktuell?
- Wie verhalten sich nationale Code Systeme zu eHDSI Value Sets?
- Wie verhalten sich eHDSI und IPS zueinander? → [[MSI - HL7 - International Patient Summary]]

## Verwandt

- [[MSI - HL7 - International Patient Summary]]
- [[MSI - Interoperabilität - Anwendungsbereiche Lehne]] (International Cooperation)
- [[MSI - Value Set - Eigenschaften und Wartung]]
- [[EHR - ELGA - Architektur]] (nationaler Counterpart)

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 33, 34 (Quelle Schema: Europäische Kommission)
