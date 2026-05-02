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

# MSI - HL7 - IPS Allergie-Codierung

> [!info] Kurzdefinition
> Konkretes Beispiel für Value-Set-Architektur im International Patient Summary (IPS): Eine Allergie wird über mehrere Dimensionen kodiert (Art, Allergie/Intoleranz, Auslösende Substanz, Manifestation, Kritikalität, Sicherheit der Diagnose, Zeitbereich), jede mit eigenem Value Set. Auf termgit.elga.gv.at sind die ELGA-IPS-Value-Sets einsehbar; spezielle „No-Info-Codes" decken absentOrUnknownAllergies ab.

## Beschreibung

Folie 35 zeigt die Codierungs-Dimensionen einer Allergie/Intoleranz im IPS-Kontext:

| Dimension | Inhalt | Value-Set-Kategorie |
|---|---|---|
| **Art** | Allergie oder Intoleranz | allergyOrIntollerance |
| **Allergie** | Keine Information / Allergie auf eine Substanz | IPSNoAllergiesInfo / IPSAllergiesToSubstances |
| **Auslösende Substanz** („Allergen") | Allergen / Nicht-Arzneimittel oder Allergen / Arzneimittel | IPSReactionAgent |
| **Manifestation** | Art des Problems / Reaktion / Schweregrad | IPSProblemType / IPSAllergyReaction / IPSProblemSeverity |
| **Kritikalität** | – | CriticalityObservationValue |
| **Sicherheit der Diagnose** | – | IPSConditionVerificationStatus |
| **Zeitbereich** | erstes / letztes Auftreten | – |

ELGA-Value-Sets für Allergie-Codierung (Folie 35 mit URLs):
- `https://termgit.elga.gv.at/ValueSet-elga-allergyorintolerancetype.html`
- `https://termgit.elga.gv.at/ValueSet-elga-allergyorintoleranceagent.html`
- `https://termgit.elga.gv.at/ValueSet-elga-allergyreaction.html`
- `https://termgit.elga.gv.at/ValueSet-elga-allergystatuscode.html`

**„No-Info-Codes"**: für Patienten ohne bekannte Allergien:
- `https://termgit.elga.gv.at/ValueSet-elga-absentorunknownallergies.html`

Diskussionsfrage der Folie: „Kennen Sie andere Strategien, diese Informationen anzugeben?" – Alternativen wären z. B. Marker auf Resource-Ebene (FHIR `AllergyIntolerance.code` mit explizitem `no-allergy-info`-Konzept) oder Section-Level-NullFlavors.

Alle Infos zum IPS: `https://international-patient-summary.net`.

## Bestandteile / Aufbau

Eine vollständige Allergie-Aussage in IPS besteht also aus mehreren Codierungs-Schichten – jede Dimension hat ihr eigenes Value Set. Das ist ein Beispiel für **Value-Set-Decomposition**: statt einem mega-präkoordinierten Code wird ein Profil aus mehreren Code-Slots gebildet.

## Beispiel

Patient hat Allergie auf Penicillin mit Manifestation Hautausschlag, mittlere Kritikalität:
- allergyOrIntolerancetype → „Allergie"
- allergyorIntoleranceAgent → Penicillin (Arzneimittel-Substanz)
- allergyReaction → Hautausschlag
- ProblemSeverity → mittel
- CriticalityObservationValue → low/moderate/high

Alle Dimensionen werden über ihre jeweiligen Value Sets validiert.

## Abgrenzung

- **IPS ≠ ELGA**. IPS ist eine internationale Spezifikation (HL7 + CEN); ELGA-Value-Sets profilieren IPS für Österreich.
- **No-Info-Codes ≠ NullFlavor.** Ein No-Info-Code ist ein expliziter Code, der „keine Allergien bekannt" als positive Aussage codiert; ein NullFlavor ist eine Abwesenheits-Markierung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Dimensionen werden bei der Allergie-Codierung im IPS erfasst?

**Anwendungsfrage:** Wie codieren Sie „Patient hat keine bekannten Allergien"? Welche Value-Set-Strategie greift hier?

**Diskussionsfrage:** Warum mehrere Value Sets statt eines präkoordinierten „Allergie-Codes"? (Antwort: Multiple Granularities + Multiple Consistent Views – siehe Cimino-Desiderata.)

**Mögliche Anschlussfragen:**
- Wo finde ich die ELGA-Value-Sets für Allergien? (termgit.elga.gv.at)
- Welche Beziehung haben IPS und FHIR? (IPS ist als FHIR Implementation Guide spezifiziert.)
- Welche Vorteile hat ein expliziter „No-Info"-Code gegenüber NullFlavor?

## Verwandt

- [[MSI - HL7 - International Patient Summary]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Terminologie - Cimino Desiderata]] (Multiple Granularities)
- [[MSI - HL7 - eHDSI MyHealth EU]]

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 35
