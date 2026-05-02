---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - Paper - Lin 2013 SOAP vs APSO Provider Satisfaction]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Studie - APSO Adoption Lin 2013

> [!info] Kurzdefinition
> Erste publizierte Studie zur Adoption und Satisfaction des APSO-Formats in EHR-Progress-Notes (Lin et al., JAMA Intern Med 2013). 13 ambulante Kliniken, 100 % Adoption bei Mandate, 51 % bei Voluntary; hohe subjektive Präferenz, aber kein messbarer Zeit-/Genauigkeitsvorteil.

## Beschreibung

Die Studie hatte das Ziel, drei Hypothesen zu prüfen:
1. APSO verbessert die Lesbarkeit (readability)
2. APSO erhöht die Provider-Satisfaction
3. APSO verkürzt die Zeit, klinische Fragen zu beantworten

Die ersten beiden wurden bestätigt (subjektiv), die dritte konnte **nicht** belegt werden.

## Bestandteile / Aufbau

### Setting und Methodik

| Aspekt | Wert |
|---|---|
| Setting | 13 ambulante Kliniken eines großen akademischen Medical Centers |
| EHR-System | Allscripts Enterprise EHR V10.2 |
| Adoption gemessen nach | 2 Monaten |
| Statistik | Paired t-test (Zeit), lineare Regression (Reihenfolgeneffekt), P < 0.05 |
| Studientyp | Prospektive observationelle Studie + Online-Survey |
| Ethik | IRB-approved |

### Adoption (nach 2 Monaten)

| Klinik-Typ | Anzahl Kliniken | Provider | Adoption |
|---|---|---|---|
| Mandatory APSO | 8 (6 Primary Care + 2 Spezialisten) | 47 | 100 % (47/47) |
| Voluntary APSO | 5 (3 Primary Care + 2 Spezialisten) | 73 | 51 % (37/73) |
| **Gesamt** | 13 | 120 | 84 (70 %) |

### Satisfaction-Survey (n = 64, Response 76 %)

| Frage | Pro APSO | Neutral | Pro SOAP |
|---|---|---|---|
| Transition to APSO was: | 72 % easy/very easy | 19 % | 9 % difficult |
| Writing in APSO is: | 74 % easy | 18 % | 8 % difficult |
| Time to write notes: | 27 % APSO faster | 60 % | 13 % SOAP faster |
| Skipping around in note: | 28 % more with APSO | 34 % | 38 % more with SOAP |
| Forgetting segments: | 28 % more with APSO | 61 % | 11 % more with SOAP |
| Reflects how I think: | 31 % APSO | 49 % | 20 % SOAP |
| Finding clinically relevant data: | **81 % easier with APSO** | 19 % | **0 % easier with SOAP** |
| Browsing through notes: | **82 % faster with APSO** | 18 % | **0 % faster with SOAP** |
| Preferred reading format: | **75 % prefer APSO** | 17 % | 8 % prefer SOAP |
| Following flow across notes: | 54 % easy with APSO | 41 % | 5 % difficult with APSO |
| Author satisfaction: | 73 % satisfied | 22 % | 5 % dissatisfied |
| Reader satisfaction: | 83 % satisfied | 15 % | 2 % dissatisfied |

### Objektiver Zeitvergleich

- 14 Provider beantworteten klinische Fragen aus 10 APSO + 10 SOAP Notes (gleicher Inhalt)
- Reihenfolge cross-over: 7 Provider zuerst APSO, 7 zuerst SOAP
- **Ergebnis:** Kein statistisch signifikanter Zeitunterschied (P = 0.37)
- **Genauigkeit:** SOAP 4/120 falsch, APSO 3/120 falsch (P = 0.54) – kein signifikanter Unterschied

## Beispiel

Der scheinbare Widerspruch der Studie: Provider berichten subjektiv (82 %), dass APSO **schneller** sei – aber im objektiven Test ist kein Zeitunterschied messbar. Mögliche Erklärungen:
- Die getestete Aufgabe (klinische Fragen beantworten) misst nicht das, was Provider als „faster browsing" wahrnehmen.
- Ergonomische Erleichterung führt zu subjektivem Zeitgefühl, ohne objektive Beschleunigung.
- Sample-Größe (n = 14) zu klein für signifikanten Effekt.

## Abgrenzung

- Single-Center-Studie – Generalisierbarkeit beschränkt.
- Setting: ambulant, **nicht** inpatient/ED/Radiologie/Pathologie.
- EHR-spezifisch: Allscripts; andere EHRs könnten andere Ergebnisse zeigen.
- Prospektiv-observationell, nicht randomisiert kontrolliert.
- Das Paper ist ein **Research Letter** (kurz, knapp), kein vollständiger Studienartikel.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was hat die Lin-2013-Studie zur APSO-Adoption gezeigt?

**Anwendungsfrage:** Warum war die Adoption bei Mandate-Kliniken 100 % und bei Voluntary-Kliniken nur 51 %? Welche Implikationen hat das für Change Management bei EHR-Roll-outs?

**Diskussionsfrage:** Die Studie zeigt subjektiv klare Präferenz, objektiv aber keinen Zeit- oder Genauigkeitsvorteil. Wie ist das zu bewerten – ist „subjektive Satisfaction" alleine bereits Grund für eine Format-Umstellung?

**Mögliche Anschlussfragen:**
- Welche Limitationen hat die Studie?
- Wie unterscheidet sich Adoption von Satisfaction methodisch?
- Welche statistischen Tests wurden verwendet, und warum diese?
- Welche Folgestudien wären sinnvoll? (Antwort: inpatient/ED, randomisierte kontrollierte Designs, andere EHR-Systeme)
- Wo liegt der Unterschied zwischen subjektiver „faster browsing" und objektiv messbarer Zeit?

## Verwandt

- [[EHR - SOAP - APSO Variante]]
- [[EHR - SOAP - Schwächen und Kritik]]
- [[EHR - Progress Notes - EHR Lesbarkeitsproblem]]
- [[EHR - Paper - SOAP Notes StatPearls]]

## Quelle

- Vorlesung: [[EHR - Paper - Lin 2013 SOAP vs APSO Provider Satisfaction]]
- Folien/Seitenangabe: gesamter Letter (S. 160–161), insbesondere Tabelle „Health Care Provider Satisfaction With APSO Format"
