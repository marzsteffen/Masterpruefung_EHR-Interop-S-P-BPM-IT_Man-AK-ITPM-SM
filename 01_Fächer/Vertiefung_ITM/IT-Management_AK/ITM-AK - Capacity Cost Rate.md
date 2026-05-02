---
fach: itm-ak
typ: konzept
status: offen
quelle: "[[ITM-AK - Paper - Porter-Kaplan 2011 - TDABC]]"
tags:
  - fach/vertiefung/itm-ak
  - typ/konzept
  - status/offen
---

# ITM-AK - Capacity Cost Rate

> [!info] Kurzdefinition
> Der Capacity Cost Rate ist der Kostensatz pro Zeiteinheit (€/h oder €/min), zu dem eine Ressource für patientenrelevante Tätigkeit verfügbar ist. Er ist das Herzstück von TDABC und wird berechnet als „Expenses Attributable to Resource / Available Capacity of Resource".

## Beschreibung

Im Zähler stehen alle Kosten, die zur Bereitstellung einer Ressource anfallen: Vergütung der Person inklusive Lohnnebenkosten, Sozialleistungen (z. B. Krankenversicherung, Pension), plus pro-rata-Anteile an Supervision, Raum (Büro inkl. Patientenzonen), Equipment, IT/Telekom. Die Ressource „kostet" also nicht nur ihr Gehalt – sie schleppt einen Anteil aller unterstützenden Strukturen mit sich.

Im Nenner steht die **praktische Kapazität**: tatsächlich für patientennahe Arbeit verfügbare Stunden pro Periode. Die Berechnung startet mit Brutto-Arbeitszeit (z. B. 365 Tage/Jahr) und subtrahiert Wochenenden, Urlaub, Feiertage, Krankheit, Pausen, Schulung, Verwaltung.

## Bestandteile / Aufbau

Grundgleichung:

```
Capacity Cost Rate (Resource_i) = Expenses Attributable to Resource_i  /  Available Capacity of Resource_i
```

### Beispiel Nurse White (Paper, S. 52)

**Zähler – Annual Total Cost:**

| Position | Wert |
|---|---|
| Annual compensation (inkl. Fringe Benefits) | $65.000 |
| Supervision Cost (10 % der Vorgesetztenkosten) | $9.000 |
| Occupancy (9 m² × $1.200/m²/Jahr) | $10.800 |
| Technology and Support | $2.560 |
| **Annual total cost** | **$87.360** |
| **Monthly total cost** | **$7.280** |

**Nenner – Verfügbare Kapazität:**

| Position | Wert |
|---|---|
| Start | 365 Tage/Jahr |
| − Wochenenden | 104 |
| − Urlaub | 20 |
| − Feiertage | 12 |
| − Krankheit | 5 |
| **= Verfügbare Tage** | **224 (≈ 18,7/Monat)** |
| Start | 7,5 h pro verfügbarem Tag |
| − Pausen | 0,5 h |
| − Meetings, Schulung, Verwaltung | 1,0 h |
| **= Verfügbare klinische Stunden** | **6 h/Tag** |

**Praktische Kapazität:** 18,7 Tage × 6 h = 112 h/Monat.

**Capacity Cost Rate:** $7.280 / 112 h = **$65/h**.

Für Equipment-Ressourcen analog: praktische Kapazität = max. mögliche Nutzung in Tagen × Stunden pro Tag, korrigiert um Spitzenlasten und Wachstumsreserve.

## Beispiel

Im Patient-Jones-Beispiel (Paper) ergeben sich:

| Ressource | Capacity Cost Rate |
|---|---|
| Administrator Allen | $45/h |
| Nurse White | $65/h |
| Physician Green | $300/h |

Equipment-Beispiel im Paper (S. 57): Bluttest-Gerät, das 10.000 Tests/Monat durchführen könnte, aber nur 6.000 abdeckt. Ohne Korrektur würden Kosten auf 6.000 Tests verteilt → Test wirkt um Faktor 10/6 zu teuer. TDABC verlangt, die volle Kapazität (10.000) als Nenner zu nehmen, damit ungenutzte Kapazität als eigener Kostenposten sichtbar wird.

## Abgrenzung

- **Capacity Cost Rate ≠ Stundenlohn:** Stundenlohn = Brutto-Compensation/Brutto-Stunden. Capacity Cost Rate = Vollkosten/praktische Kapazität – inklusive Overhead, abzüglich nicht-klinischer Zeiten.
- **Praktische Kapazität ≠ theoretische Kapazität:** Praktische Kapazität liegt typischerweise bei 80–85 % der theoretischen (nach Sweet Spot in Operations Management). Im Paper als „rule of thumb" nicht explizit benannt.
- **Capacity Cost Rate ≠ Verrechnungssatz/Tarif:** Verrechnungssatz ist verhandelbar (Tarifvertrag, interne Verrechnung); Capacity Cost Rate basiert auf realen Kosten und realer Kapazität.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Was ist der Capacity Cost Rate und wie wird er berechnet?"

**Anwendungsfrage:** „Berechnen Sie den Capacity Cost Rate einer Pflegekraft mit Jahresgesamtkosten $87.360 und 1.344 verfügbaren klinischen Stunden pro Jahr." Antwort: 87.360 / 1.344 = **$65/h**.

**Diskussionsfrage:** Warum ist die Wahl des Nenners (praktische statt theoretische Kapazität) so wichtig? Diskussion:
- Bei voller theoretischer Kapazität würden die Kosten unrealistisch tief erscheinen, weil sie selten erreicht wird.
- Bei tatsächlicher Auslastung würden alle Kostendifferenzen aus Auslastungs-Schwankungen direkt in den Cost Rate fließen → Vergleichbarkeit zerstört.
- Praktische Kapazität ist ein Mittelweg – stabil, realistisch erreichbar, transparent.
- Differenz zwischen praktischer Kapazität und tatsächlichem Verbrauch wird als „Cost of Unused Capacity" ausgewiesen → wird zur Steuerungsgröße.

**Mögliche Anschlussfragen:**
- Wie geht TDABC mit Spitzenlast-Kapazitäten um (z. B. Notaufnahme)?
- Wie wirkt sich Forschung/Lehre eines Arztes auf den Capacity Cost Rate aus? (Subtraktion nicht-klinischer Zeit, Restkosten klinisch zugeordnet.)
- Wie behandelt man „Rule of 1" – Ressourcen mit nur einer Person/Einheit (z. B. einzelner Lehrlogopäde)?

## Verwandt

- [[ITM-AK - TDABC - Time Driven Activity Based Costing]]
- [[ITM-AK - TDABC - Sieben Schritte der Kostenmessung]]
- [[ITM-AK - Costing Myth - Hospital Overhead too complex]]
- [[ITM-AK - Costing Myth - Healthcare Costs are fixed]]

## Quelle

- Vorlesung: [[ITM-AK - Paper - Porter-Kaplan 2011 - TDABC]]
- Folien/Seitenangabe: HBR-Paginierung 51 (Formel + Beispiel Patient Jones), 52 (Nurse-White-Berechnung), 57 (Equipment-Beispiel, Rule of 1).
