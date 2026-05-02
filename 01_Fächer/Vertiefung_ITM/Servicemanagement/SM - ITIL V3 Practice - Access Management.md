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

# SM - ITIL V3 Practice - Access Management

> [!info] Kurzdefinition
> Access Management gewährt autorisierten Anwendern den Zugriff auf einen Service und beschränkt den Zugriff für nicht autorisierte Anwender. Es umfasst Verifizierung, Zuweisung von Rechten, Überwachung des ID-Status, Aufzeichnung der Zugriffe sowie Entziehung und Einschränkung von Rechten.

## Beschreibung

Folie 41 listet Ziele und Ablauf:

**Ziele:**
- Gewährung des Zugriffs auf einen Service
- Zugriffsbeschränkung für nicht autorisierte Anwender
- Zugriffsgewährleistung

**Ablauf (5 Schritte):**
1. Verifizierung
2. Zuweisung von Rechten
3. Überwachung des ID-Status
4. Aufzeichnung und Verfolgung der Zugriffe
5. Entziehung und Einschränkung von Rechten

Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008).

Access Management ist im V3-Diagramm sowohl in **Service Transition** als auch in **Service Operation** verortet (siehe [[SM - ITIL V3 - Servicelebenszyklus]]) — Setup während Transition, Tagesgeschäft während Operation.

## Bestandteile / Aufbau

| Schritt | Inhalt |
|---|---|
| Verifizierung | Identität des Anfragenden prüfen |
| Zuweisung von Rechten | Berechtigungen entsprechend Rolle vergeben |
| Überwachung des ID-Status | Account aktiv? Gültigkeit? Sperrungen? |
| Aufzeichnung und Verfolgung der Zugriffe | Log, Audit-Trail |
| Entziehung und Einschränkung | Bei Rollenwechsel, Austritt, Verstoß |

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Krankenhaus-Beispiele:
- Neuaufnahme einer Pflegekraft → Account-Anlage mit Stationsrechten (Verifizierung über HR, Zuweisung Rolle „Pflege Station 3").
- Pflegekraft wechselt Station → Berechtigung passt nicht mehr → Entziehung alter Rechte, Neuzuweisung.
- Audit zeigt unberechtigte Zugriffe → Aufzeichnung erlaubt Nachvollzug, ID-Status wird gesperrt.

## Abgrenzung

- **Access Management vs. Information Security Management**: Access Management ist der operative Vollzug; Information Security Management legt Richtlinien und Sicherheitsstrategie fest. ITIL 4 ordnet Access Management in der Praxis dem Information Security Management zu.
- **Access Management vs. IAM (Identity and Access Management)**: IAM ist der branchenübliche Sammelbegriff (Identitäten + Zugriff); ITIL Access Management fokussiert auf Zugriff. Identity Lifecycle ist im V3-Modell *nicht explizit benannt*.
- **Access Management vs. Privacy by Design** (siehe [[SM - Privacy by Design - DSGVO]]): Privacy by Design ist eine Designpflicht bei Service-Konzeption (Datensparsamkeit etc.); Access Management ist der Betriebsprozess.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind die Ziele von Access Management? — Zugriff gewähren, Beschränkung für nicht autorisierte Anwender, Zugriffsgewährleistung.

**Anwendungsfrage:** Welche Schritte umfasst Access Management bei Eintritt einer neuen Pflegekraft? — Verifizierung (HR-Daten) → Zuweisung Rolle → Status-Überwachung → Logging → ggf. Entziehung beim Austritt.

**Diskussionsfrage:** Warum ist Access Management im Krankenhaus besonders kritisch? — Patientendaten, DSGVO, Berufsgeheimnis, Mehrschicht-Betrieb mit häufigem Personalwechsel. Gleichzeitig: Im Notfall müssen Zugriffe schnell möglich sein („Break-the-glass" — *im PDF nicht thematisiert*).

**Mögliche Anschlussfragen:**
- Wie unterscheiden sich Access Management und Information Security Management?
- Welche Rolle spielt Access Management im Kontext DSGVO und Patientenrechte?
- Was passiert, wenn Schritt 5 (Entziehung) vergessen wird? — Sicherheitslücken durch verwaiste Accounts mit weiterhin gültigen Berechtigungen.

## Verwandt

- [[SM - ITIL V3 - Service Operation]]
- [[SM - Privacy by Design - DSGVO]]
- [[SM - Compliance - Definition]]
- [[ASP - Authentifizierung - OAuth2]] *(Cross-Fach)*

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 41; Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
