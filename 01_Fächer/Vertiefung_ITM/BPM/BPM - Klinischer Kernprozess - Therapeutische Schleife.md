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

# BPM - Klinischer Kernprozess - Therapeutische Schleife

> [!info] Kurzdefinition
> Die **therapeutische Schleife** ist die zweite Schleife des medizinischen Falls. Sie startet mit der **Identifikation des Therapieschemas** (= passende Leitlinie) und der Therapie­durchführung, prüft den Erfolg über **Kontrolluntersuchungen** und endet mit der **Entlassung** – oder mit einem Neustart der diagnostischen und/oder therapeutischen Schleife.

## Beschreibung

Folie 29. Aufbau:

```
Identifikation Therapieschema (= „passende Leitlinie")
   +
Durchführung Therapie
   ↓
KONTROLLUNTERSUCHUNGEN
   ↓
BEHANDLUNGSZIEL ERREICHT
   ↓
ENTLASSUNG
   ODER
NEUSTART DIAGNOSTISCHE und/oder THERAPEUTISCHE SCHLEIFE
```

### Stationen

| Station | Inhalt |
|---|---|
| **Identifikation Therapieschema** | Auswahl der passenden Leitlinie / SOP / des Therapieschemas auf Basis der gestellten Diagnose |
| **Durchführung Therapie** | Umsetzung – z. B. OP, Medikation, physikalische Therapie |
| **Kontrolluntersuchungen** | Erfolgskontrolle (Labor postop, Bildgebung, Symptom-Score) |
| **Behandlungsziel erreicht** | wenn ja: Entlassung; wenn nein: Reentry |
| **Reentry** | diagnostisch (war die Diagnose falsch?), therapeutisch (war das Schema falsch oder unzureichend?), oder beides |

### Bezug zu Leitlinien

Die Auswahl des Therapieschemas knüpft direkt an die Leitlinien-Welt an (vgl. [[BPM - VL - Erstellung von Leitlinien]] – VL V, [[BPM - Paper - European Hernia Society Guidelines]], [[BPM - Paper - HerniaSurge Update]]). Die Vorlesung referenziert das Therapieschema explizit als „passende Leitlinie".

### Bezug zu Komplikationen

Wenn in der Kontrolluntersuchung ein **Komplikation** ([[BPM - Komplikation - Definition]]) erkannt wird, geht die Schleife in einen Reentry – entweder therapeutisch (Antibiose, Revision-OP) oder diagnostisch (neue Diagnose nötig).

## Bestandteile / Aufbau

- 4 Hauptstationen + 1 Endpunkt + 1 Reentry-Pfad
- Reentry kann sowohl diagnostisch als auch therapeutisch sein (Doppelpfeil)

## Beispiel

Hernien-Therapie laparoskopisch (TAPP):
- Therapieschema: HerniaSurge-Update-Leitlinie empfiehlt TAPP / TEP bei beidseitiger oder Rezidiv-Hernie.
- Durchführung: laparoskopische OP.
- Kontrolluntersuchungen: postop. klinische Untersuchung, ggf. Labor; Schmerzstatus.
- Behandlungsziel erreicht (Bruch verschlossen, keine OP-Komplikation): Entlassung.
- Reentry-Beispiel: postoperatives Hämatom → therapeutische Reentry (Punktion, Kontrolle); Rezidivhernie nach 6 Monaten → diagnostische Reentry (Anamnese, US) + neuer Therapie­zyklus.

## Abgrenzung

- **Therapeutische Schleife ≠ einmalige OP.** Auch eine OP kann mehrere Therapie-Iterationen auslösen, wenn der Erfolg ausbleibt.
- **Kontrolluntersuchung ≠ Routine-Diagnostik.** Kontrolluntersuchung ist *zielgerichtet* (Wirkungsbeleg der Therapie), nicht routinemäßig.
- **Reentry ≠ Wiedervorstellung.** Reentry ist im laufenden Fall; eine spätere Wiedervorstellung mit demselben Problem ist ein neuer Fall.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Beschreiben Sie die therapeutische Schleife des medizinischen Falls."

**Anwendungsfrage:** „In welchen Situationen ist ein Reentry der therapeutischen Schleife angezeigt, und wie modelliert man das im klinischen Pfad?"

**Diskussionsfrage:** Wenn ein Pfad-Modell keinen Reentry vorsieht, wird die Komplikationsbehandlung „außer-Pfad" abgewickelt – mit der Folge, dass sie weder gemessen noch standardisiert wird. Wie verhindert man das? – explizite Reentry-Modellierung mit Trigger­ereignis und Maßnahmen­katalog.

**Mögliche Anschlussfragen:**
- Was triggert eine Reentry?
- Wie hängt Therapieschema mit Leitlinien zusammen?
- Welche Kennzahlen messen das Behandlungsziel?

## Verwandt

- [[BPM - Klinischer Kernprozess - Definition]]
- [[BPM - Klinischer Kernprozess - Diagnostische Schleife]]
- [[BPM - Komplikation - Definition]]
- [[BPM - VL - Erstellung von Leitlinien]]
- [[BPM - Klinischer Pfad - Definition]]
- [[BPM - Paper - HerniaSurge Update]]
- [[BPM - Paper - European Hernia Society Guidelines]]

## Quelle

- Vorlesung: [[BPM - VL - Grundlagen klinischer Kernprozess]]
- Folien/Seitenangabe: Folie 29
