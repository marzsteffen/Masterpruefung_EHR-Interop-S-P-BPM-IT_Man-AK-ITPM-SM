---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 CDA und e-Befunde]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 CDA - II Instance Identifier

> [!info] Kurzdefinition
> Datentyp **II** (*Instance Identifier*) erlaubt die global eindeutige Identifikation einer Instanz durch Verwendung von OIDs (ISO/IEC 9834-1). Zwei Methoden: (1) OID direkt als `root`-Attribut, (2) OID einer ID-Liste in `root` + eigentliche ID in `extension`.

## Beschreibung

Folie 18 erklärt:

> „Identifikationselemente (II Instance Identifier) erlauben die global eindeutige Identifikation durch Verwendung von Objektidentifikatoren (kurz ‚OID')
> – ISO/IEC 9834-1 Standard
> – OID-Portal für das Österreichische Gesundheitswesen: OIDs registriert und veröffentlicht"

Zwei Methoden im Beispiel der Folie:

**Methode 1**: Angabe einer OID als direkten Identifikator
```xml
<id root="1.2.40.0.34.99.111.0.1" assigningAuthorityName="KH Eisenstadt"/>
```

**Methode 2**: Angabe der OID der ID-Liste in `@root` sowie der eigentlichen ID in `@extension`
```xml
<id root="1.2.40.0.34.99.111.1.1" extension="134F989"
    assigningAuthorityName="KH Eisenstadt"/>
```

**Methode 3** (impliziert via codeSystem-Attribut bei codierten Elementen):
```xml
<code code="3333" displayName="Zithromax"
      codeSystem="1.2.40.0.34.4.16"
      codeSystemName="Pharmazentralnummer"/>
```

Folie 19 vertieft das **OID-Konzept**:
- OIDs sind **persistente, wohl definierte Identifikatoren** von Objekten der realen Welt: Institutionen, Personen, Klassifikationen, Nachrichten, Dokumente oder Tabellen.
- OIDs weisen eine **Baumstruktur** auf.
- Zusammensetzung in **Dot-Notation**: Beginnend bei der Wurzel kann entlang der Kanten für jeden Knoten im Baum die jeweilige OID als Abfolge der Zwischen­knoten abgelesen werden.
- **Weltweite Eindeutigkeit** wird gewährleistet durch Registrierungsstellen und Verantwortliche für den jeweiligen Unterbaum.
- Der OID-Baum ist **weder als inhaltliche Hierarchie noch als Klassifikation** von Objekten zu verstehen. Er dient lediglich zur Verwaltung und Organisation der Identifikatoren nach pragmatischen Gesichtspunkten.
- Detail-Quelle: `https://www.gesundheit.gv.at/OID_Frontend/OID_Konzept_1-1-0.pdf`

Folie 20 ergänzt für die österreichische eHealth-Landschaft:
- Für jede OID sind die entsprechenden Metadaten gespeichert.
- Alle Value Sets, Code Systeme, GDA, CDA-Templates haben eingetragene OID.
- Der GDA-I vergibt automatisch eine OID für alle GDA.
- „Meldepflicht" – wichtige OIDs müssen eingetragen werden.
- Österreichisches OID-Portal: `https://www.gesundheit.gv.at/OID_Frontend/`

## Bestandteile / Aufbau

| Komponente | Erklärung |
|---|---|
| `root` | OID, identifiziert entweder das Objekt selbst (Methode 1) oder die ID-Liste, aus der `extension` stammt (Methode 2) |
| `extension` | Konkrete ID innerhalb der ID-Liste |
| `assigningAuthorityName` | Klartext-Name der vergebenden Stelle |

## Beispiel

Aus Folie 18 (Methoden 1+2). Aus Folie 25:
```xml
<id extension="OBS-1-1" root="2.16.840.1.113883.2.16.1.99.3.1"/>
```
hier ist `root` die OID-Wurzel der Lab-Observation-IDs, `extension` der konkrete ID-Wert.

OID-Baum-Auszug aus Folie 19:
- `0` ITU-T
- `1` ISO
  - `2` member-body
    - `840` US (ANSI)
    - `40` AT (ÖNORM Institut)
      - `0` gv (Stabsstelle IKT)
        - `10` verwaltung
          - `1` organisation
          - `2` dienste
  - `3` Identified organization
- `2` Joint ISO/ITU-T
  - `16` Country assignments

Die HL7-Wurzel `2.16.840.1.113883` ist Joint ISO/ITU-T → 16 Country assignments → 840 USA → 1 US Org. → 113883 HL7 inc.

## Abgrenzung

- **II ≠ OID**: II ist der CDA-Datentyp; OID ist der Identifikator-Inhalt.
- **`root` Methode 1 vs. Methode 2**: Methode 1 hat keinen `extension`, weil die OID selbst der Identifikator ist. Methode 2 verwendet `root` als Namespace-Pointer für `extension`.
- **OID-Baum ≠ inhaltliche Hierarchie**: explizit auf Folie 19 hervorgehoben. Der Baum ist organisatorisch.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Was ist ein II Instance Identifier? Welche Methoden gibt es?

**Anwendungsfrage:** Erklären Sie die Bedeutung der `root`- und `extension`-Attribute in einem konkreten II-Element.

**Diskussionsfrage:** Warum ist der OID-Baum *nicht* als inhaltliche Hierarchie zu verstehen?

**Mögliche Anschlussfragen:**
- Welche Standardisierungsorganisation steht hinter OIDs?
- Wie wird die Eindeutigkeit garantiert?
- Welche Art von Objekten werden in Österreich mit OIDs identifiziert? (siehe Folie 20)

## Verwandt

- [[MSI - Identifikator - OID]]
- [[MSI - Identifikator - Übersicht eHealth]]
- [[MSI - HL7 CDA - Datentypen]]
- [[MSI - Terminologie - Code System]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 18, 19, 20
