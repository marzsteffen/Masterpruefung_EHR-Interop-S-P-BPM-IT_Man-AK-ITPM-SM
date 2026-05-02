---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Authentifizierung - Level of Assurance (LoA)

> [!info] Kurzdefinition
> Klassifizierung der Vertrauenswürdigkeit einer elektronischen Identifizierung, festgelegt in der eIDAS-Verordnung. Drei Stufen: Low, Medium, High.

## Beschreibung

Folie 32 nennt am Ende der PFS-Diskussion die drei Stufen der Authentifizierungsqualität:

- **Low**
- **Medium**
- **High**

Mit dem Hinweis: „eIDAS regulation: Level of Assurance".

**Kerngedanke laut Folie:** Die Schlüssel-Speicherung beeinflusst direkt die Qualität der Authentifizierung – wer Schlüssel in einer Hardware-Sicherheits-Umgebung erzeugt, kann ein höheres LoA erreichen.

**Im PDF nicht definiert** sind die genauen Kriterien jeder Stufe. Aus dem Kontext und dem eIDAS-Rahmen lässt sich ableiten:

| Stufe | Kerngedanke (Vorlesungs-Kontext + eIDAS) |
|---|---|
| Low | begrenzte Sicherheit, einfache Identifizierung (z. B. nur Username/Passwort) |
| Medium | substanzielle Sicherheit, Mehrfaktorauthentifizierung, oft mit Software-Schlüsseln |
| High | hohe Sicherheit, Schlüssel auf zertifizierter Hardware (SE/HSM), starke Identitätsprüfung |

## Bestandteile / Aufbau

| Stufe | Im PDF angegeben | Detaillierte Anforderungen |
|---|---|---|
| Low | ja (als Stufenname) | im PDF nicht spezifiziert |
| Medium | ja | im PDF nicht spezifiziert |
| High | ja | im PDF nicht spezifiziert; korreliert in der Vorlesung mit Hardware-Sicherheit |

## Beispiel

*Im PDF nicht ausgeführt.* Aus dem österreichischen Kontext: ID Austria mit Smartphone-Signatur und Personenbindung erreicht typischerweise „High"; eine reine Username/Passwort-Anmeldung erreicht „Low".

## Abgrenzung

- **LoA vs. Authentifizierungs-Faktor:** Faktoren sind „etwas wissen / haben / sein" (Wissen, Besitz, Inhärenz). LoA bündelt mehrere Faktoren plus Schlüssel-Sicherheit plus Identitätsprüfung zu einer Stufe.
- **eIDAS-LoA vs. NIST-LoA:** Beide Rahmenwerke definieren Stufen, mit unterschiedlichen Kriterien und Bezeichnungen. *Im PDF nur eIDAS erwähnt.*

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Level of Assurance, in welchem Rahmenwerk ist es geregelt, und welche drei Stufen gibt es?

**Anwendungsfrage:** Wie hängt die LoA-Stufe mit der konkreten Schlüssel-Speicherung zusammen?

**Diskussionsfrage:** Welche eHealth-Anwendungsfälle erfordern aus Ihrer Sicht ein LoA „High", welche reichen mit „Medium" aus? (Beispiele: ärztliche e-Verschreibung, Patientenakten-Zugriff – hohe Anforderungen; Termin-Buchungs-App – ggf. niedriger.)

**Mögliche Anschlussfragen:**
- Welche Faktoren bestimmen das LoA? (Identitätsprüfung, Schlüsselsicherheit, kryptografische Stärke der Authentifizierung – im PDF nicht detailliert.)
- Welche Rolle spielt die Personenbindung (z. B. bPK in Österreich)?
- Wie wird LoA auf der Empfänger-Seite verifiziert? (Über Signaturattribute / Authentifizierungs-Tokens – im PDF nicht behandelt.)

## Verwandt

- [[ASP - Schluesselspeicherung - Hardware Security]]
- [[ASP - Zertifikate - X.509]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Security Eigenschaften - Authenticity]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folie 32

## Ergänzung außerhalb der Vorlesung

eIDAS-Verordnung **(EU) Nr. 910/2014**, ergänzt durch Durchführungsverordnung **(EU) 2015/1502**, definiert die drei LoA-Stufen mit konkreten Anforderungen an Identitätsnachweis, Authentifizierungs-Mechanismus und betriebliche Sicherheit. „Substantial" entspricht hier „Medium". Für qualifizierte elektronische Signaturen ist „High" zwingend; eine qualifizierte Signatur ist juristisch der eigenhändigen Unterschrift gleichgestellt. Die Folge-Verordnung **eIDAS 2.0** (in Kraft seit 2024) führt zusätzlich die Europäische Digitale Identitäts-Brieftasche (EUDI Wallet) ein.
