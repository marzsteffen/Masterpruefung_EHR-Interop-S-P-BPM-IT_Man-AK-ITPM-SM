---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Business Continuity Management]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - BCM - Soll-Ist-Vergleich (RTA, RPA gegen RTO, RPO)

> [!info] Kurzdefinition
> Vergleich der geforderten Wiederanlauf- und Datenverlustwerte (RTO, RPO als SOLL) mit den tatsächlich mit den vorhandenen Maßnahmen erreichten Werten (RTA, RPA als IST). Zeigt, ob die BC-Strategie ausreicht.

## Beschreibung

Folie 19:

**Ziel:** Beurteilung, ob die geforderte Wiederanlaufzeit mit vorhandenen technischen und organisatorischen Maßnahmen erreicht werden kann.

**Relevante Ergebnisse aus der Business Impact Analyse:**
- Geforderte Wiederanlaufzeit aller zeitkritischen Ressourcen (**RTO**)
- Maximal zulässiger Datenverlust (**RPO**)
- → RTO & RPO sind **SOLL-WERTE**

**Tatsächliche Werte:**
- Tatsächliche Wiederanlaufzeit – **Recovery Time Actual (RTA)**
- Tatsächlicher Datenverlust – **Recovery Point Actual (RPA)**
- → RTA & RPA sind **IST-WERTE**

**Logik:**
- Wenn RTA ≤ RTO und RPA ≤ RPO: Anforderungen erfüllt.
- Wenn RTA > RTO oder RPA > RPO: Lücke aufgedeckt; zusätzliche Maßnahmen nötig (z. B. häufigere Backups, schnellerer Recovery-Prozess, Hot-Standby).

## Bestandteile / Aufbau

| Kenngröße | Was? | Quelle | Status |
|---|---|---|---|
| RTO | geforderte Wiederanlaufzeit | BIA | SOLL |
| RPO | maximal zulässiger Datenverlust | BIA | SOLL |
| RTA | tatsächliche Wiederanlaufzeit | Test/Übung/Realfall | IST |
| RPA | tatsächlicher Datenverlust | Test/Übung/Realfall | IST |

## Beispiel

Geschäftsprozess „Patientenakten-Zugriff": RTO = 4 Stunden, RPO = 1 Stunde. Übung ergibt RTA = 8 Stunden, RPA = 6 Stunden. → Beide IST-Werte überschreiten die SOLL-Werte. Konsequenz: Backup-Frequenz erhöhen (auf z. B. stündlich) und Recovery-Prozess optimieren (Hot-Standby statt Cold-Restore).

## Abgrenzung

- **Soll-Ist-Vergleich ≠ Audit:** Audit prüft Compliance gegen Standards; Soll-Ist-Vergleich prüft die Eigenfähigkeit gegen die in der BIA selbst gesetzten Ziele.
- **RTA/RPA werden nicht in der BIA, sondern erst in CHECK-Phase / Übungen / Realfällen ermittelt.** Folie 19 macht das implizit klar.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Soll-Ist-Vergleich im BCM, und welche vier Kennwerte werden gegenübergestellt?

**Anwendungsfrage:** RTA = 8 h, RTO = 4 h. Was bedeutet das für den BCM-Verantwortlichen? Welche Maßnahmen kommen in Betracht?

**Diskussionsfrage:** Warum ist es wichtig, RTA und RPA regelmäßig durch Übungen zu validieren statt sie nur theoretisch zu schätzen? Welche systematischen Fehler treten ohne Realtests auf? (Optimismus-Bias; vergessene Abhängigkeiten; nicht funktionierende Wiederherstellungs-Skripte.)

**Mögliche Anschlussfragen:**
- Wie kann ein Soll-Ist-Vergleich in einem Krankenhaus konkret durchgeführt werden? (Übung mit simuliertem Stromausfall; Restore-Test einer Datenbank.)
- Was tut man, wenn die SOLL-Werte unrealistisch sind? (Diskussion mit der Institutionsleitung; entweder mehr Investition oder MTPD/RTO anpassen.)
- Welcher Zusammenhang zur PDCA-CHECK-Phase besteht?

## Verwandt

- [[ASP - BCM - BIA Kenngroessen]]
- [[ASP - BCM - Business Impact Analyse]]
- [[ASP - BCM - Risikoanalyse]]
- [[ASP - BCM - Managementsystem]]

## Quelle

- Vorlesung: [[ASP - VL - Business Continuity Management]]
- Folien/Seitenangabe: Folie 19
