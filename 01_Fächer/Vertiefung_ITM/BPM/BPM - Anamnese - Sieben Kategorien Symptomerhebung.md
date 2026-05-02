---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - Anamnese Status Differentialdiagnose]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - Anamnese - Sieben Kategorien strukturierter Symptomerhebung

> [!info] Kurzdefinition
> **Sieben Befragungs­kategorien** zur strukturierten Symptom-Anamnese. Sie systematisieren das Patientengespräch und stellen sicher, dass kein wichtiger Aspekt eines Beschwerdebildes vergessen wird. Die Vorlesung führt sie am Beispiel „Beinschwellung" vor.

## Beschreibung

Folien 7–13. Die sieben Kategorien sind:

| # | Kategorie | Beispiel-Fragen (Beinschwellung) |
|---|---|---|
| 1 | **Lokalisation und Ausbreitung** | Wie sehen die Schwellungen aus? Beide Beine? Gleich stark? Wo genau? Knöchel/Fußrücken/höher? |
| 2 | **Qualität** | Wie fühlen sich die Schwellungen an? Beschwerden? Schmerzhaft? Ausstrahlung? Druckgefühl? Weich oder derb? |
| 3 | **Schweregrad** | Sichtbar? Sehr ausgeprägt? Nur bei Druck? Socken-Einkerbungen? Schuhe zu eng? |
| 4 | **Zeitliches Auftreten** | Wann zum ersten Mal bemerkt? Konstante Beschwerden? Phasen ohne Schwellungen? Gründe? Frühere Episoden? |
| 5 | **Verstärkung / Abschwächung** | Tageszeitliche Schwankungen? Stehender Beruf? Nahrung/Trinken? Liegen/Hochlagern? Medikamente? |
| 6 | **Begleitsymptomatik** | Weitere Beschwerden? Gewichtszunahme? Wadenkrämpfe? Atemnot? Herzbeschwerden? Nykturie? Veränderter Urin? |
| 7 | **Grad der Behinderung** | Wie stark beeinträchtigt? Beruf ungehindert ausübbar? Probleme am Arbeitsplatz, zu Hause, im Bekanntenkreis? |

### Bedeutung

- Reduziert das Risiko, eine wichtige Symptomdimension zu übersehen.
- Macht die Anamnese **dokumentierbar und reproduzierbar** (Voraussetzung für Pfad-Modellierung und Datenqualität).
- Erleichtert die **Differentialdiagnose** (siehe [[BPM - Differentialdiagnose - Definition]]) – die Abgrenzung ähnlicher Krankheitsbilder gelingt nur mit ausreichend feiner Symptom­charakterisierung.
- Bildet die Grundlage für die **Anamnese-Bausteine** in einem klinischen Pfad (vgl. [[BPM - VL - Erstellung klinischer Pfade]]).

## Bestandteile / Aufbau

```
Symptom (z. B. Beinschwellung)
   ├── 1. Lokalisation/Ausbreitung
   ├── 2. Qualität
   ├── 3. Schweregrad
   ├── 4. Zeitliches Auftreten
   ├── 5. Verstärkung/Abschwächung
   ├── 6. Begleitsymptomatik
   └── 7. Grad der Behinderung
```

## Beispiel

Übertragung auf Symptom „Leistenschmerz" (Hernien-Verdacht):
1. **Lokalisation**: rechts/links/beidseitig? Im Leistenbogen? Ausstrahlung in Skrotum/Labium?
2. **Qualität**: ziehend, brennend, stechend?
3. **Schweregrad**: Schmerzskala 0–10? Tagesarbeit beeinträchtigt?
4. **Zeitliches Auftreten**: seit wann? Plötzlich/schleichend? Konstant?
5. **Verstärkung**: bei Husten, Pressen, schwerem Heben? Linderung beim Liegen?
6. **Begleitsymptomatik**: Schwellung, Übelkeit, Stuhlveränderungen (Inkarzerations­zeichen)?
7. **Grad der Behinderung**: Berufsausübung möglich? Sport? Schlaf?

## Abgrenzung

- **Sieben Kategorien ≠ Vorlesungserfindung.** Diese Struktur ist klinischer Standard (z. B. SOCRATES-Schema im Englischen: Site, Onset, Character, Radiation, Associations, Time course, Exacerbating/relieving factors, Severity – ähnlich, aber mit teilweise abweichender Gruppierung); im PDF nicht als SOCRATES bezeichnet.
- **Symptomerhebung ≠ Eigen-/Fremdanamnese.** Eigen vs. Fremd ist die Quelle; Symptomerhebung ist die *Struktur*.
- **Sieben Kategorien ≠ Familien-/Sozialanamnese.** Diese sind eigenständige Anamnese­bausteine, die *zusätzlich* zur Symptomerhebung erfragt werden.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche sieben Kategorien einer strukturierten Symptomerhebung lehrt die Vorlesung?"

**Anwendungsfrage:** „Erstellen Sie eine strukturierte Symptomerhebung für einen Patienten mit Leistenschmerz." – konkrete Fragen pro Kategorie aufzählen.

**Diskussionsfrage:** Warum ist die strukturierte Erhebung in einem klinischen Pfad wichtig? – sie macht die Information *reproduzierbar* und damit *digitalisierbar* (KIS-Eingabemasken, FHIR-Resources). Ohne Struktur sind Anamnesen Freitext-Romane, die nicht maschinell auswertbar sind. Bezug zu [[MSI - MOC]] (HL7 FHIR) später.

**Mögliche Anschlussfragen:**
- Welche Kategorie umfasst „Berufstätigkeit als stehender Beruf"? (5: Verstärkung/Abschwächung)
- Wie hängt die strukturierte Anamnese mit der Pfad-Modellierung zusammen?
- Warum ist „Grad der Behinderung" eine eigene Kategorie?

## Verwandt

- [[BPM - Anamnese - Definition]]
- [[BPM - Status - Definition]]
- [[BPM - Symptom und Krankheitsbild]]
- [[BPM - Differentialdiagnose - Definition]]
- [[BPM - Klinischer Kernprozess - Diagnostische Schleife]]
- [[MSI - MOC]]

## Quelle

- Vorlesung: [[BPM - VL - Anamnese Status Differentialdiagnose]]
- Folien/Seitenangabe: Folien 7–13
