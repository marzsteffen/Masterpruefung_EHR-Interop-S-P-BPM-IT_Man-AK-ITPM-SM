---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - FHIR Grundlagen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - FHIR - 6 Exchange Paradigms

> [!info] Kurzdefinition
> FHIR definiert sechs Austausch-Paradigmen, mit denen Resources ausgetauscht/genutzt werden können: **REST**, **Documents**, **Messaging**, **Services**, **Database/Persistence**, **Subscription**. Jedes adressiert andere Use-Cases.

## Beschreibung

Aus Folie 76:

> „6 exchange paradigms – https://build.fhir.org/exchange-module.html
>
> 1. **Services**: Allows invocation of complex services like decision support or workflow management, suitable for scenarios where simple CRUD actions are insufficient.
> 2. **Database / Persistence**: Uses FHIR resources directly within a database for data storage and retrieval, ensuring compatibility with FHIR-based APIs and other paradigms.
> 3. **Subscription**: Enables real-time notifications by allowing clients to subscribe to specific events or changes in FHIR resources, useful for timely updates like lab results or event detection."

Die übrigen drei (REST, Documents, Messaging) sind vorher bereits eingeführt:

> „FHIR paradigms define how FHIR resources are exchanged.
> Resources should be exchanged and consumed by different systems.
> RESTful, Documents, and Messaging."

## Bestandteile / Aufbau

| # | Paradigma | Use-Case | Mechanismus |
|---|---|---|---|
| 1 | **REST** | CRUD auf einzelne Resources, Search, atomare Updates | HTTP GET/POST/PUT/DELETE auf Resource-URLs |
| 2 | **Documents** | Statische, immutable, signierbare Sammlungen (Entlassungsbriefe, Discharge Summaries) | Bundle vom Typ `document` mit Composition |
| 3 | **Messaging** | Event-driven Kommunikation, Lab-Orders mit Response, Insurance-Transaktionen | Bundle vom Typ `message` mit MessageHeader |
| 4 | **Services** | Komplexe Operationen (CDS, Workflow, Berechnungen), die nicht in CRUD passen | Operation-Endpunkte (`$evaluate`, `$apply` etc.) |
| 5 | **Database / Persistence** | Native Speicherung von FHIR-Resources, kompatibel mit allen FHIR-APIs | FHIR-native Datenbanken (z. B. HAPI mit JPA) |
| 6 | **Subscription** | Real-Time Notifications bei Resource-Events (z. B. neuer Lab-Befund) | Subscription-Resource + Server-side Event-Handling |

## Beispiel

| Use-Case | Paradigma |
|---|---|
| Patient-Stammdaten abrufen | REST |
| Entlassungs­dokument an Hausarzt senden | Documents |
| Lab-Order an externes Labor + Befund-Rückmeldung | Messaging |
| Clinical Decision Support („evaluate this PlanDefinition for this Patient") | Services |
| FHIR-Server speichert intern in PostgreSQL FHIR-JSONB | Database/Persistence |
| Frontend bekommt Push-Notification, sobald neue Observation für Patient X eintrifft | Subscription |

## Abgrenzung

- Die Paradigmen sind **nicht exklusiv** – ein FHIR-Server kann (und tut es typischerweise) mehrere unterstützen.
- **REST + Subscription** ergänzen sich: REST für Pull-Zugriff, Subscription für Push-Notifications.
- **Documents vs. Messaging:** beides Bundles, unterschiedliche Charakteristik (statisch/signiert vs. event-driven).
- **Services** ist FHIR's Antwort auf den klassischen RPC-Bedarf, der in reinem CRUD nicht abbildbar ist.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche sechs Exchange-Paradigmen kennt FHIR? Beschreibe jedes in einem Satz.

**Anwendungsfrage:** Welches Paradigma würdest du wählen für: (a) Echtzeit-Vital-Sign-Monitoring, (b) Discharge-Letter-Übergabe, (c) Drug-Drug-Interaction-Check vor dem Verschreiben? (Antworten: a) Subscription, b) Documents, c) Services)

**Diskussionsfrage:** Warum hat FHIR sechs Paradigmen statt nur einem? Was wäre verloren, wenn nur REST existierte?

**Mögliche Anschlussfragen:**
- Was sind FHIR Operations (Services) konkret – und wie unterscheiden sie sich von einer REST-Resource?
- Wie funktioniert Subscription technisch (Polling, REST-Hook, WebSocket, FHIRcast)?
- Welche Datenbanken sind FHIR-native?
- Wie kombiniert man Documents und REST in einem realen System?

## Verwandt

- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - FHIR - Bundles Document und Message]]
- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Implementation Guides]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 47, 76 (FHIR Paradigms, 6 Exchange Paradigms mit Verweis auf build.fhir.org/exchange-module.html)
