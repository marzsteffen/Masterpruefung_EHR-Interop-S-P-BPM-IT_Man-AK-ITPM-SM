---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - Evidenzbasierte Medizin]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - EBM - Vier mögliche Ursachen einer beobachteten Assoziation

> [!info] Kurzdefinition
> Eine beobachtete Assoziation zwischen zwei Größen kann **vier mögliche Ursachen** haben: **Kausalität**, **Bias**, **Confounding** oder **Zufall**. Nur die Kausalität rechtfertigt eine Behandlungsentscheidung – die anderen drei sind methodische Fallstricke.

## Beschreibung

Folien 7–8. Die Vorlesung formuliert dies als **die zentrale Frage der EBM-Methodik**.

### Die vier Erklärungen

| # | Ursache | Inhalt |
|---|---|---|
| 1 | **Kausalität** | „Echter" Ursache-Wirkungs-Zusammenhang. A bewirkt B. Siehe [[BPM - Kausalitaet vs Korrelation]]. |
| 2 | **Bias** (systematischer Fehler / Verzerrung) | Studie ist methodisch verzerrt; das beobachtete Ergebnis spiegelt eine Wirklichkeit, die so nicht existiert. Siehe [[BPM - Bias - Definition]]. |
| 3 | **Confounding** (Störfaktor) | Eine dritte Variable beeinflusst sowohl Ursache als auch Wirkung; die Assoziation ist *real beobachtet*, aber irreführend interpretiert. Siehe [[BPM - Confounder - Definition]]. |
| 4 | **Zufall** | Das beobachtete Ergebnis ist zufällig entstanden und nicht reproduzierbar. Wird statistisch über p-Werte und Konfidenz­intervalle adressiert. |

### Bias vs. Confounder (Folie 17, wörtlich)

> „BIAS CREATES AN ASSOCIATION THAT IS NOT TRUE BUT CONFOUNDER DESCRIBES AN ASSOCIATION THAT IS TRUE; BUT POTENTIALLY MISLEADING."

→ Bias erzeugt eine *unwahre* Assoziation; Confounder beschreibt eine *wahre*, aber irreführende.

### Methodische Konsequenzen

| Ursache | Gegenmaßnahme |
|---|---|
| Bias | Studiendesign (Randomisierung, Verblindung, klare Definitionen, IR-Reliability) |
| Confounding | [[BPM - Confounder-Kontrolle - Methoden]] (Randomisierung, Restriktion, Matching, Stratifikation, multivariate Analyse) |
| Zufall | ausreichende Fallzahl, statistische Tests mit Signifikanz und Effektgröße |
| Kausalität | übrig, nachdem die anderen drei plausibel ausgeschlossen sind |

## Bestandteile / Aufbau

```
Beobachtete Assoziation A ↔ B
  │
  ├── ist es Kausalität?     ← was wir wissen wollen
  ├── ist es Bias?           ← Studiendesign
  ├── ist es Confounding?    ← dritte Variable
  └── ist es Zufall?         ← Statistik
```

## Beispiel

Beobachtung: Patient:innen, die täglich Vitamin C einnehmen, haben weniger Erkältungen.

- **Kausalität?** Plausibel.
- **Bias?** Hat man Erkältungs­häufigkeit objektiv gemessen oder selbstberichten lassen (Recall-Bias)?
- **Confounding?** Vitamin-C-Nutzer:innen ernähren sich vielleicht insgesamt gesünder (Lebensstil als Confounder).
- **Zufall?** War die Stichprobe groß genug?

Erst wenn die letzten drei kontrolliert sind, lässt sich die Kausalität ableiten.

## Abgrenzung

- **Diese Liste ist exhaustiv für die Vorlesungsperspektive.** Andere Methodologien fügen noch „Reverse Causation" oder „Selection" hinzu; im PDF werden sie nicht separat aufgeführt (Selection ist in vielen Klassifikationen ein Bias-Untertyp).
- **Bias und Confounding sind nicht dasselbe.** Häufige Verwechslung – die Folie 17-Definition ist der knappste Korrektur­satz.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche vier möglichen Ursachen kann eine beobachtete Assoziation haben?"

**Anwendungsfrage:** „Eine retrospektive Studie zeigt: Patient:innen mit Hüft-OP-Verzögerung haben höhere Mortalität. Welche der vier Erklärungen kommen in Frage?" – Kausalität (Verzögerung erhöht Risiko), Confounding (alte/kranke Patient:innen werden eher verzögert; Confounder = Allgemein­zustand; siehe Folie 24 HTEP-Beispiel in [[BPM - Confounder - Definition]]), Bias (Selection?), Zufall (kleine Studie?).

**Diskussionsfrage:** Warum ist die Trennung zwischen Bias und Confounder die schwierigste? – Die Definition unterscheidet sich nur in der Wahrheit der Assoziation. Bias = Beobachtung selbst ist verzerrt; Confounding = Beobachtung stimmt, Interpretation ist irreführend. Das Folie-17-Zitat ist mnemotechnisch das wichtigste der ganzen Vorlesung.

**Mögliche Anschlussfragen:**
- Was unterscheidet Bias von Confounder?
- Wie kontrolliert man Confounding methodisch?
- Welche Rolle spielt der Zufall, und wie wird er adressiert?

## Verwandt

- [[BPM - EBM - Definition]]
- [[BPM - Kausalitaet vs Korrelation]]
- [[BPM - Bias - Definition]]
- [[BPM - Confounder - Definition]]
- [[BPM - Confounder-Kontrolle - Methoden]]
- [[BPM - Studiendesign - RCT Goldstandard]]

## Quelle

- Vorlesung: [[BPM - VL - Evidenzbasierte Medizin]]
- Folien/Seitenangabe: Folien 7–8 (Übersicht), 17 (Bias-vs-Confounder-Abgrenzung)
