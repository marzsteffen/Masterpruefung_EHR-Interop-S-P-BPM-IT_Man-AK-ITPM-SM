---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Identitaetsmanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Berechtigungsmodelle - Übersicht (RBAC, ABAC, IBAC, MAC, DAC, CBAC)

> [!info] Kurzdefinition
> Sechs Modelle zur Vergabe von Zugriffsrechten in Systemen: RBAC (Rollen), ABAC (Attribute), IBAC (Identitäten), MAC (zentrale Sicherheitsregeln), DAC (Eigentümer entscheidet), CBAC (Kontext).

## Beschreibung

Folien 13–14 stellen die sechs Modelle vor. Folie 16 vergleicht sie tabellarisch.

### Role Based Access Control (RBAC)
- Zugriff wird basierend auf **Rollen** gewährt, die Benutzern zugeordnet sind.
- Eine Rolle definiert Berechtigungen und Aufgaben für bestimmte Benutzergruppen (z. B. „Arzt", „Krankenschwester", „Patient").
- **Vorteile:** Einfaches Management, klare Zuweisung von Rechten; ideal für Organisationen mit klar definierten Hierarchien.
- **Nachteile:** Eingeschränkt flexibel, Berechtigungen starr an Rollen gebunden.

### Attribute-Based Access Control (ABAC)
- Zugriff wird auf Basis von **Attributen** des Benutzers, der Ressource oder des Umfelds gewährt.
- Attribute können z. B. Abteilung des Mitarbeiters, Firmenstandort oder ein spezifisches Gerät (Client) sein.
- **Vorteile:** Sehr flexibel, dynamisch; ideal für feingranulare Zugriffssteuerungen.
- **Nachteile:** Komplex in der Verwaltung – viele Attribute müssen konfiguriert und gepflegt werden.

### Identity Based Access Control (IBAC)
- Zugriffsentscheidungen basieren direkt auf der **Identität** eines Benutzers oder Geräts, unabhängig von Rollen oder Attributen.
- **Vorteile:** Direkte Kontrolle über spezifische Identitäten; Zugriff kann für einzelne Personen explizit gewährt werden.
- **Nachteile:** Schwer skalierbar, pflegeintensiv – für jede Identität müssen Rechte einzeln festgelegt werden.

### Context-based Access Control (CBAC)
- Berücksichtigt zusätzlich zur Identität, Rolle oder Attributen **kontextbezogene Informationen** wie Tageszeit, Standort oder Netzwerkbedingungen.
- **Vorteile:** Geeignet für Zero-Trust-Umgebungen, Zugriffsentscheidungen können kontinuierlich angepasst werden.
- **Nachteile:** Erfordert komplexe Infrastruktur, kann hohe Rechenlast verursachen.

### Mandatory Access Control (MAC)
- Zugriff auf Ressourcen wird durch eine **zentrale Autorität** nach definierten Sicherheitsregeln festgelegt.
- Berechtigungen richten sich nach der Identität der Person, des Informationsobjekts und zusätzlichen Regeln.
- **Vorteile:** Sehr hohe Sicherheit und Kontrolle; ideal für sicherheitskritische Domänen wie Gesundheitswesen, öffentliche Verwaltung.
- **Nachteile:** Schwierig zu verwalten, eingeschränkt anpassbar für dynamische Umgebungen.

### Discretionary Access Control (DAC)
- Der **Ressourcenbesitzer** entscheidet, wer Zugriff erhält und welche Berechtigungen er vergibt.
- **Vorteile:** Flexibel, benutzerfreundlich – Berechtigungen direkt von den Eigentümern.
- **Nachteile:** Benutzer treffen möglicherweise unsichere Entscheidungen; Informationsfluss schwer zu überwachen.

## Bestandteile / Aufbau – Vergleichstabelle (Folie 16)

| Modell | Vorteil (Kern) | Nachteil (Kern) |
|---|---|---|
| RBAC | klare Rollen, einfaches Management | starr |
| ABAC | feingranular, flexibel | komplexe Verwaltung |
| IBAC | direkte Personen-Kontrolle | schlecht skalierbar |
| MAC | sehr hohe Sicherheit, zentrale Kontrolle | schwer dynamisch anpassbar |
| DAC | flexibel, benutzerfreundlich | unsichere Entscheidungen möglich |
| CBAC | dynamisch, Zero-Trust-tauglich | komplex, rechenintensiv |

## Beispiel

eHealth-Krankenhaus: typische Praxis-Kombination ist **RBAC** (Rollen Arzt/Pflege/Patient) plus **ABAC**-Zusätze (Stationsbindung, „nur eigene Station") plus **MAC** (zentrale gesetzliche Vorgaben, z. B. ELGA-Patientenverfügungs-Sperren) plus **CBAC** (z. B. Notfall-Modus außerhalb regulärer Zeiten).

## Abgrenzung

- **RBAC ↔ ABAC:** Rollen sind eine Form von Attribut, aber nicht alle Attribute sind Rollen. ABAC ist allgemeiner.
- **MAC ↔ DAC:** MAC ist top-down (zentrale Regel), DAC ist bottom-up (Eigentümer entscheidet). Beide schließen einander nicht aus, werden aber selten gleichzeitig verwendet.
- **IBAC** wird oft als spezifischste Form von ABAC interpretiert, in der das einzige Attribut die Identität ist.
- **CBAC** wird häufig als Erweiterung anderer Modelle implementiert, nicht als eigenständige Lösung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Berechtigungsmodelle kennt die Vorlesung, und worin unterscheiden sie sich kurz?

**Anwendungsfrage:** Welches Modell würden Sie für einen regionalen Gesundheitsdienstleister wie HealthNet (siehe Übungsaufgabe Folie 15) wählen, und warum? Welche Vor- und Nachteile gegen die anderen?

**Diskussionsfrage:** RBAC ist in eHealth weitverbreitet, hat aber bekannte Schwächen – welche, und wie löst man sie? (Antwort: Rollen-Explosion bei feinen Granularitäten; Lösung: Kombination mit ABAC, oder hierarchische Rollen.) Wann braucht man wirklich MAC?

**Mögliche Anschlussfragen:**
- Wie hängt RBAC mit dem österreichischen ELGA-Rollenkonzept zusammen?
- Was ist der Unterschied zwischen DAC und „Sharing" in modernen Cloud-Tools?
- Welche Schwierigkeit hat ABAC bei der Audit-Nachvollziehbarkeit?

## Verwandt

- [[ASP - Identitaetsmanagement - Autorisierung]]
- [[ASP - Identitaetsmanagement - Definition]]
- [[ASP - Security Eigenschaften - Accountability]]
- [[ASP - DSGVO - Grundsaetze]]
- [[EHR - Berechtigungssteuerung]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folien 13, 14, 16
