---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - PRINCE2 4 Projektablauf]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - PRINCE2 - Qualitätskontrollpfad

> [!info] Kurzdefinition
> Der Qualitätskontrollpfad ist der Lebenszyklus der Qualität von Projektbeginn bis -ende. Zwei Hauptblöcke: **Qualitätsplanung** (Kundenqualitätserwartungen → Projektabnahmekriterien → PEP → QM-Strategie → Produktbeschreibungen mit Qualitätskriterien/-toleranzen/-prüfmethode/-verantwortlichkeiten) und **Qualitätssteuerung** (Qualitätsregister → Spezialistenprodukt → Qualitäts- und Produktabnahmedokumentation → Projektabnahmedokumentation).

## Beschreibung

Aus PRINCE-Buch Folien 6–11 (Kapitel 4.2.1):

> „Der Qualitätskontrollpfad spiegelt eine Art Lebenszyklus wider, welcher hilft, den Überblick über die Anforderung zu erlangen. Einen Lebenszyklus deshalb, weil von der ersten Kundenanforderung bis zur Erstellung des Endprodukts jeder Zwischenschritt aufgezeigt wird."

## Bestandteile / Aufbau

### Block 1: Qualitätsplanung

| # | Schritt | Inhalt |
|---|---|---|
| **1** | **Kundenqualitätserwartungen** | Erste Wünsche des Kunden, in der PEP niedergeschrieben. Meist „weich" / nicht messbar formuliert. Im SU. |
| **2** | **Projektabnahmekriterien** | Kundenqualitätserwartungen so messbar wie möglich formulieren. Je messbarer, desto weniger Diskussion am Ende. |
| **3** | **PEP** | Produktbeschreibung des Projektendprodukts; bündelt Erwartungen + Kriterien. |
| **4** | **Qualitätsmanagementstrategie** | Policy mit Standards, Techniken, Verantwortlichkeiten. Im IP. |
| **5** | **Produktbeschreibungen** | Pro Produkt detailliert: enthalten **Qualitätskriterien**, **Qualitätstoleranzen**, **Qualitätsprüfmethode**, **Qualitätsverantwortlichkeiten**. |
| **5.1** | Qualitätskriterien | z. B. Lautstärke des Eröffnungsfeuerwerks |
| **5.2** | Qualitätstoleranzen | z. B. 10–15 dB |
| **5.3** | Qualitätsprüfungsmethode | z. B. Testfeuerwerk 48 h vorher |
| **5.4** | Qualitätsverantwortlichkeiten | z. B. Firefighter Smith + PM |

### Block 2: Qualitätssteuerung

| # | Schritt | Inhalt |
|---|---|---|
| **6** | **Qualitätsregister** | Sammeldokument aller Qualitätsdaten; ständig aktualisiert. |
| **7** | **Spezialistenprodukt** | Wird auf Basis der Produktbeschreibungen entwickelt. |
| **8** | **Qualitäts- und Produktabnahmedokumentation** | Prüfung der Eigenschaften gegen die in der Produktbeschreibung genannten Anforderungen + Prüfmethode. Vermerk im Qualitätsregister. |
| **9** | **Projektabnahmedokumentation** | Finale Abnahme nach iterativer Durchläufung der Schritte 5–8 für alle Produkte; Übergabe des Endprodukts. |

> Die Schritte 5–8 wiederholen sich pro Produkt, bis das letzte Produkt final abgenommen wurde.

## Beispiel

Olympiade London (Buch):

- Kundenqualitätserwartung: „Großartige Olympiade".
- Projektabnahmekriterium: „6000-Raketen-Feuerwerk, 150 m Höhe, Lautstärke 110±5 dB".
- Produktbeschreibung Eröffnungsfeuerwerk mit Kriterium 110±5 dB; Toleranz 10–15 dB; Prüfmethode = Testfeuerwerk 48 h vorher.
- Verantwortlich: Firefighter Smith (Firefighter Headquarter London) + PM.

## Abgrenzung

- Der Qualitätskontrollpfad **kombiniert** Elemente aus mehreren Prozessen (SU für PEP/Erwartungen, IP für QM-Strategie, CS/MP für Produktbeschreibungen, SB für Abnahmen).
- Strukturell vergleichbar mit klassischem [[ITPM - QM - Hierarchische Anforderungsdoku]] (Business Vision → Stakeholder Req → System/SW Req → Component Req).
- Verbindung zur **Verifikation/Validierung** ([[ITPM - QS - Testen Verifikation Validierung]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche zwei Hauptblöcke umfasst der Qualitätskontrollpfad, und welche Schritte gehören zu jedem?

**Anwendungsfrage:** Durchlaufen Sie den Pfad für die Anforderung „Patientenportal soll datenschutzkonform sein" – konkret bis zu Qualitätskriterien.

**Diskussionsfrage:** Wann wird ein Pfad-Schritt übersprungen, und welche Risiken birgt das?

**Mögliche Anschlussfragen:**
- Welche vier Bestandteile hat eine Produktbeschreibung qualitativ?
- Wie verhält sich das Qualitätsregister zum Risikoregister?
- Welche Verbindung zur PEP aus SU?

## Verwandt

- [[ITPM - PRINCE2 - Thema Qualität]]
- [[ITPM - PRINCE2 - Qualitätsregister]]
- [[ITPM - PRINCE2 - Qualitätsprüfungstechnik]]
- [[ITPM - PRINCE2 - PEP]]
- [[ITPM - PRINCE2 - Managementstrategien]]
- [[ITPM - QM - Hierarchische Anforderungsdoku]]

## Quelle

- Vorlesung: [[ITPM - VL - PRINCE2 4 Projektablauf]]
- Buch-Kapitel: 4.2.1 (Folien 6–11)
