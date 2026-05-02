---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - ITIL Practice - Service Configuration Management

> [!info] Kurzdefinition
> ITIL-4-Practice (Service Management) zur Sicherstellung, dass jederzeit und überall genaue und zuverlässige Informationen über die Konfiguration von Services und der unterstützenden Configuration Items (CIs) verfügbar sind — einschließlich Beziehungen zwischen CIs. Werkzeug: CMDB.

## Beschreibung

Folie 82 (und 139 im Omada-Health-Kontext) definiert Zweck und Begriffe:

**Zweck:**
> „Es sicherzustellen, dass jederzeit und überall genaue und zuverlässige Informationen über die Konfiguration von Services und die unterstützenden CIs verfügbar sind. Dies schließt Informationen dazu ein, wie CIs konfiguriert sind, und über die Beziehungen zwischen diesen."

**Definition Configuration Item (CI):**
> „Alle Komponenten, die gemanagt werden müssen, um einen IT Service bereitstellen zu können."

**Werkzeug** (laut Folie 139): CMDB (Configuration Management Database).

Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Zweck | Genaue, zuverlässige Konfigurationsinformationen verfügbar halten |
| Inhalt | Wie sind CIs konfiguriert? Welche Beziehungen gibt es zwischen CIs? |
| Werkzeug | CMDB |
| Definition CI | Alle Komponenten, die für die Service-Erbringung gemanagt werden müssen |

## Beispiel

Krankenhaus-CMDB: Server „KIS-Prod-01" mit Beziehung zu Service „Krankenhausinformationssystem" und zu Backup-CI „BackupTier-01"; Standort, Hersteller, Patch-Level dokumentiert. Bei Incident kann sofort ermittelt werden, welche Services betroffen sind.

## Abgrenzung

- **CMDB vs. Asset-Management**: Asset-Management fokussiert auf Eigentum, Wert, Lifecycle; CMDB fokussiert auf Konfiguration und Beziehungen. Beide Disziplinen sind komplementär.
- **Service Configuration Management vs. Service Catalogue Management**: SCM verwaltet die CIs *hinter* den Services; Service Catalogue Management verwaltet die *Sicht der Services* (siehe [[SM - IT-Service-Katalog - Sichten und Strukturierung]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Zweck von Service Configuration Management? — Genaue, zuverlässige Konfigurationsinformationen über Services und CIs (mit Beziehungen) jederzeit verfügbar halten.

**Definition CI:** Alle Komponenten, die gemanagt werden müssen, um einen IT Service bereitzustellen.

**Diskussionsfrage:** Warum ist eine aktuelle CMDB so schwer zu pflegen? — Hoher Pflegeaufwand bei dynamischen Umgebungen (Cloud, Container); Tools verändern sich; Disziplin der CI-Aktualisierung erfordert Kultur.

**Mögliche Anschlussfragen:**
- Wie hängt SCM mit Incident und Problem Management zusammen? — CMDB hilft beim schnellen Verstehen der Auswirkungen.
- Welche CI-Typen gibt es? *(im PDF nicht differenziert)*
- Welche Rolle spielt SCM in einer Cloud-Umgebung?

## Verwandt

- [[SM - ITIL Practice - Change Enablement]]
- [[SM - ITIL Practice - Incident Management]]
- [[SM - ITIL 4 - Dimension Informationen und Technologie]]
- [[SM - Fallbeispiel - Omada Health]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 82, 139; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
