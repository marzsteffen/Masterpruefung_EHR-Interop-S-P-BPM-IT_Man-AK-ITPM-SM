---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - Paper - SOAP Notes StatPearls]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - SOAP - Schwächen und Kritik

> [!info] Kurzdefinition
> Drei zentrale Kritikpunkte am SOAP-Schema: fehlende explizite Zeitdimension, ungeeignete Lese-Reihenfolge bei chronischen Visiten (siehe APSO) und das EMR-Risiko, SOAP-Notes mit klinisch irrelevanten Daten zu überfrachten.

## Beschreibung

StatPearls führt zwei Kritikbereiche aus, die sich zu drei Hauptpunkten zusammenfassen lassen.

### 1. Fehlende Zeitdimension

> „A weakness of the SOAP note is the inability to document changes over time. In many clinical situations, evidence changes over time, requiring providers to reconsider diagnoses and treatments. An important gap in the SOAP model is that it does not explicitly integrate time into its cognitive framework."

→ Adressiert durch SOAPE-Erweiterung ([[EHR - SOAP - SOAPE Erweiterung]]).

### 2. Lese-Reihenfolge unpassend für chronische Visiten

> „The order in which a medical note is written has been a topic of discussion. While a SOAP note follows the order Subjective, Objective, Assessment, and Plan, it is possible, and often beneficial, to rearrange the order. (...) One study found that the APSO order was better than the typical SOAP note order in terms of speed, task success (accuracy), and usability for physician users acquiring information needed for a typical chronic disease visit in primary care."

→ Adressiert durch APSO-Variante ([[EHR - SOAP - APSO Variante]]) – studiengestützt.

### 3. EMR-Datenüberfrachtung („data-filled notes")

> „An unintended consequence of electronic documentation is the ability to incorporate large volumes of data easily. These data-filled notes risk burdening a busy clinician if the data are not useful. As importantly, the patient may be harmed if the information is inaccurate. It is essential to make the most clinically relevant data in the medical record easier to find and more immediately available."

→ Trade-off: SOAP soll Information **strukturieren und auffindbar machen**, aber EMRs verleiten zum unselektiven Anhängen großer Datenmengen.

## Bestandteile / Aufbau

| Schwäche | Adressiert durch |
|---|---|
| Keine explizite Zeitdimension | SOAPE-Erweiterung (E = Evaluate) |
| Lese-Reihenfolge ineffizient | APSO-Variante (Assessment/Plan vorne) |
| EMR-Datenüberfrachtung | Sorgfältige Selektion klinisch relevanter Daten; Templates mit Fokus statt Vollständigkeit |

## Beispiel

**Problem:** Ein EMR-System fügt automatisch alle Vital Signs der letzten 30 Tage in die Objective-Sektion ein. Klinisch relevant ist nur der heutige Wert plus 2 Vergleichs­zeitpunkte.

**Konsequenz:** Lesende Ärzte scrollen durch irrelevante Daten, übersehen ggf. den klinisch entscheidenden Trend.

**Mitigationsstrategie:** Strukturierte EMR-Templates mit klinisch motivierter Auswahl; APSO-Anzeige; ggf. Zusammenfassungen via Summary-Algorithmen oder LLMs.

## Abgrenzung

- Diese Kritik ist **nicht** ein generelles Argument gegen SOAP – SOAP bleibt der dominante Standard. Es geht um zu adressierende Schwachstellen, nicht um Ersatz.
- Die Kritik richtet sich teils an SOAP selbst (fehlende Zeitdimension), teils an seine **EMR-Implementierung** (Datenüberfrachtung).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Schwächen hat das SOAP-Schema und welche Erweiterungen/Varianten adressieren sie?

**Anwendungsfrage:** Wie würdest du eine EMR-Implementierung gestalten, die SOAP-Schwächen adressiert? Nenne 3 konkrete Maßnahmen.

**Diskussionsfrage:** Ist die fehlende Zeitdimension wirklich eine Schwäche des Schemas oder eine Stärke (klare Trennung von Zustands­dokumentation pro Visite vs. Verlauf)? Argumente in beide Richtungen.

**Mögliche Anschlussfragen:**
- Welche modernen Konzepte (FHIR Bundles mit zeitlichen Querverbindungen, Trend-Visualisierungen, LLM-Zusammenfassungen) adressieren diese Schwächen heute?
- Wie verhält sich die EMR-Datenüberfrachtung zu Burnout-Forschung bei Ärzten?
- Welche EMR-Hersteller setzen auf „dynamic notes"?

## Verwandt

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - SOAPE Erweiterung]]
- [[EHR - SOAP - APSO Variante]]
- [[EHR - SOAP - Templates]]

## Quelle

- Vorlesung: [[EHR - Paper - SOAP Notes StatPearls]]
- Folien/Seitenangabe: Sektion „Issues of Concern" + Sektion „Clinical Significance"
