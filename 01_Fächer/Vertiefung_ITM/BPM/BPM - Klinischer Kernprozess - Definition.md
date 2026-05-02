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

# BPM - Klinischer Kernprozess - Definition

> [!info] Kurzdefinition
> Der **klinische Kernprozess** ist die End-to-End-Behandlung eines Patienten / einer Patientin in einer Versorgungseinheit. Er besteht aus zwei verkoppelten Schleifen – der **diagnostischen** und der **therapeutischen** – die zusammen den **„medizinischen Fall"** bilden.

## Beschreibung

Erste Vorlesungseinheit, eingeführt unter dem Titel „Der klinische Kernprozess" (Folie 1) und konkretisiert in den Folien zum „medizinischen Fall" (Folien 28–32 des PDF).

Der klinische Kernprozess ist die Übertragung des allgemeinen BPM-Begriffs **Kernprozess** ([[BPM - Prozesslandkarte - Prozesskategorien]]) auf das Krankenhaus: Er steht direkt mit dem/der Patient:in in Verbindung, schafft den eigentlichen Wert der Klinik und ist die Kernkompetenz des Hauses.

### Aufbau des „medizinischen Falls"

Der medizinische Fall besteht aus zwei Schleifen, die sequenziell und iterativ durchlaufen werden:

1. **Diagnostische Schleife** ([[BPM - Klinischer Kernprozess - Diagnostische Schleife]]) – Anamnese + Status → Verdachtsdiagnose → Untersuchungen → Diagnose oder Neustart.
2. **Therapeutische Schleife** ([[BPM - Klinischer Kernprozess - Therapeutische Schleife]]) – Identifikation Therapieschema (Leitlinie) → Therapie → Kontrolluntersuchungen → Ziel erreicht (Entlassung) oder Neustart.

Beide Schleifen können *erneut starten*, wenn das Ergebnis nicht ausreicht – die Architektur ist explizit zyklisch, nicht linear.

### Bezug zur Steuerung (Value-Based Care)

Folie 32 stellt explizit her, dass die Steuerung einer Klinik über **Prozesse + Outcomes + Kosten** zu Value-Based Care führt (siehe [[BPM - Value-Based Care]]). Der klinische Kernprozess ist die Steuerungseinheit auf der Prozessseite.

### Komplikationen als Outcome-Maß

In den Folien 30–31 wird **Komplikation** ([[BPM - Komplikation - Definition]]) als zentraler Outcome-Indikator des klinischen Kernprozesses eingeführt. Insbesondere Davenport et al. (2005, NSQIP-Daten) zeigen, dass präoperative Risikofaktoren und chirurgische Komplexität die Kostenstruktur dominieren – nicht die postoperativen Komplikationen.

## Bestandteile / Aufbau

```
Klinischer Kernprozess (= medizinischer Fall)
├── Diagnostische Schleife
│      Anamnese + Status → Verdachtsdiagnose → Untersuchungen → Diagnose
│      └─ Neustart (falls Diagnose nicht plausibel)
└── Therapeutische Schleife
       Therapieschema (Leitlinie) → Therapie → Kontrolluntersuchungen → Behandlungsziel erreicht
       └─ Entlassung
       └─ Neustart (diagnostisch und/oder therapeutisch, falls Ziel nicht erreicht)
```

## Beispiel

Hernien-Pfad als klinischer Kernprozess:
- Diagnostische Schleife: Anamnese (Schmerz in der Leiste) + körperliche Untersuchung (Bruchsackpalpation, Valsalva) → Verdachtsdiagnose Inguinalhernie → ggf. Sonografie/CT → Diagnose K40.x ICD-10.
- Therapeutische Schleife: OP-Indikation (Leitlinie HerniaSurge) → laparoskopische TAPP → postoperative Kontrolle → Entlassung. Bei Komplikation (z. B. Hämatom) Neustart der therap. Schleife.

## Abgrenzung

- **Klinischer Kernprozess ≠ einzelne medizinische Tätigkeit.** Eine OP allein ist nicht der Kernprozess; der Kernprozess ist der gesamte Fall vom Trigger (Aufnahme/Indikation) bis zum Outcome (Entlassung mit erreichtem Behandlungsziel).
- **Klinischer Kernprozess ≠ klinischer Pfad.** Pfad ist die *standardisierte SOLL-Beschreibung* eines wiederkehrenden Kernprozess-Typs (z. B. Hernie); der Kernprozess ist die *individuelle Durchführung* an einem Patienten. Ein Pfad ist ein Schablonen-Modell für viele Kernprozesse derselben Diagnose. Vgl. [[BPM - Klinischer Pfad - Definition]] (folgt aus VL VI).
- **Diagnostische und therapeutische Schleife ≠ getrennte Prozesse.** Sie sind gekoppelt: die Diagnose triggert die Therapieschema-Auswahl; die therap. Schleife kann die diagn. Schleife reaktivieren (Neustart bei ausbleibender Therapie-Wirkung).

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Was ist der klinische Kernprozess, und aus welchen Bestandteilen setzt er sich zusammen?"

**Anwendungsfrage:** „Modellieren Sie den klinischen Kernprozess für eine Cholezystektomie." – Trigger (Indikation Cholezystolithiasis), diagn. Schleife abschließen, therap. Schleife durchlaufen, Komplikations-Reentry.

**Diskussionsfrage:** Warum ist die zyklische Struktur (Neustart-Möglichkeit) wichtiger als die Linearität? – Patientenrealität ist zyklisch; ein lineares Modell verschleiert die häufigsten Probleme (falsche Verdachtsdiagnose, Therapieversagen). Vergleich zur Autoindustrie (Folien 14–15) ist explizit gewollt: Auto wird einmal gebaut, Patient wird oft mehrfach evaluiert.

**Mögliche Anschlussfragen:**
- Was unterscheidet diagnostische und therapeutische Schleife?
- Wann startet eine Schleife neu?
- Wie hängt der Kernprozess mit Komplikationen und Value-Based Care zusammen?

## Verwandt

- [[BPM - Klinischer Kernprozess - Diagnostische Schleife]]
- [[BPM - Klinischer Kernprozess - Therapeutische Schleife]]
- [[BPM - Komplikation - Definition]]
- [[BPM - Value-Based Care]]
- [[BPM - Prozesslandkarte - Prozesskategorien]]
- [[BPM - Klinischer Pfad - Definition]]
- [[EHR - MOC]]

## Quelle

- Vorlesung: [[BPM - VL - Grundlagen klinischer Kernprozess]]
- Folien/Seitenangabe: Folien 1, 27–32 (medizinischer Fall, klinische Kernprozesse, Value-Based Care)
