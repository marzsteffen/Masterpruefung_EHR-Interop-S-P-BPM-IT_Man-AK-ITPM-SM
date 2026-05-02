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

# MSI - LOINC - Sechs-Achsen-Struktur

> [!info] Kurzdefinition
> Jeder LOINC-Code beschreibt ein Konzept entlang von sechs Achsen: Component (Analyt/Substrat), Property (Messgröße), Time (Zeitbezug), System (Probe/Material), Scale (Skalen-Typ) und Method (Methode). Diese Achsen werden im Fully Specified Name als `Component:Property:Time:System:Scale:Method` geschrieben.

## Beschreibung

Folie 23 zeigt die sechs Achsen mit Beispielen:

| Achse | Bedeutung | Beispiele aus Folie 23 |
|---|---|---|
| **Component (Analyte)** | Was wird gemessen? | Glukose, Kalium, Hämoglobin |
| **Property** | Welche physikalische/chemische Eigenschaft? | Massenkonzentration, Enzym-Aktivität, Druck, Fläche; zusätzlich: Doc, Email, Finding |
| **Time** | Zeitbezug | einmalig, in 24 Stunden, Beobachtungs­dauer |
| **System (Specimen)** | Untersuchungs­material/Probe | Serum, Urin |
| **Scale** | Skalen-Typ | quantitativ, qualitativ, beschreibend (Text/Diktat) |
| **Method** | Mit welcher Methode? | – |

Die Folie stellt zwei Diskussions­fragen:
- „Was bedeuten die einzelnen Stellen (Ziffern) des LOINC-Codes?" – Antwort: nichts. Der Zifferncode (z. B. `26464-8`) ist semantisch *nicht* zerlegbar; die Bedeutung kommt aus dem zugeordneten 6-Achsen-Namen, nicht aus den Ziffern. Damit erfüllt LOINC Cimino's Desideratum „Nonsemantic Concept Identifier" → [[MSI - Terminologie - Cimino Desiderata]].
- „Sind LOINC-Codes post- oder präkoordiniert?" – Antwort: präkoordiniert. Jeder Code repräsentiert die fertige Kombination der sechs Achsen-Werte; Postkoordination findet in LOINC nicht statt.

## Bestandteile / Aufbau

Sechs Achsen ergeben den Fully Specified Name (FSN):
```
Component:Property:Time:System:Scale:Method
```
Beispiel aus Folie 23: `Leukocytes : NCnc : Pt : Bld : Qn : :` für Code `26464-8`.

Der FSN wird ergänzt durch einen „long common name", der besser lesbar ist (siehe [[MSI - LOINC - Fully Specified Name]]).

## Beispiel

Aus Folie 23 (Code `26464-8` „Leukozyten"):
- Component: `Leukocytes (white blood cells)`
- Property: `NCnc (Number concentration)`
- Time: `Pt (Point in time)`
- System: `CSF (Cerebral spinal fluid)` – im Folien-Bild zeigt das System `Bld` für Blut; das CSF-Beispiel ist im Folientext nur als Vergleichswert genannt
- Scale: `Qn (Quantitative)`
- Method: `Manual Count`

> Hinweis: Auf Folie 23 zeigt die linke Hälfte die Werte für den klassischen LOINC `26464-8` (Bld/Pt/Qn). Die Method ist beim Standard-Code offen. Method `Manual Count` ist im Folien-Bild als zusätzliche Method-Achse abgebildet.

## Abgrenzung

- **6-Achsen ≠ mehrachsige Klassifikation à la APPC.** Der LOINC-Code enthält keine Bedeutung in den Ziffern; APPC hingegen ist semantisch im Code (`2.0.2-3-7.4-2-3` = CT.undefiniert.virtuelle-endoskopie.colon).
- **Achsen ≠ Postkoordination.** Die Achsen werden vom LOINC-Pfleger in einem präkoordinierten Code zusammen­gefasst, nicht zur Laufzeit kombiniert.

## Prüfungsrelevanz

**Sehr hoch.** Klassische LOINC-Verständnis-Frage.

**Typische Definitionsfrage:** Welche sechs Achsen hat ein LOINC-Code?

**Anwendungsfrage:** Zerlegen Sie einen LOINC-Code (z. B. `26464-8`) in seine sechs Achsen und geben Sie die Werte an.

**Diskussionsfrage:** Warum sind LOINC-Codes präkoordiniert? Welche Trade-offs hat das gegenüber Postkoordination?

**Mögliche Anschlussfragen:**
- Erfüllt LOINC Cimino's „Nonsemantic Concept Identifier"-Desideratum?
- Was ist der Unterschied zwischen Component und Property?
- Warum gibt es eine Method-Achse, obwohl viele Codes diese leer lassen?

## Verwandt

- [[MSI - LOINC - Definition]]
- [[MSI - LOINC - Fully Specified Name]]
- [[MSI - Terminologie - Cimino Desiderata]] (Nonsemantic Concept Identifier)
- [[MSI - Terminologie - Präkoordination vs Postkoordination]]
- [[MSI - Terminologie - Mehrachsigkeit]] (Vergleich zu APPC)

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 23
