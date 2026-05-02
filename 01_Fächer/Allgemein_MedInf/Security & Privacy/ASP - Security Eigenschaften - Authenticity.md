---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Einfuehrung und Motivation]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Security Eigenschaften - Authentizität (Authenticity)

> [!info] Kurzdefinition
> Echtheit und Vertrauenswürdigkeit einer Partei (laut Folie 14).

## Beschreibung

Authentizität bedeutet in der Vorlesung wörtlich: „Echtheit und Vertrauenswürdigkeit einer Partei". Eine Partei, die sich als jemand ausgibt, ist tatsächlich diejenige, die sie vorgibt zu sein. Auf der Schutzziel-Grafik (Folie 13) ist Authentizität eines der acht IT-Sicherheits-Schutzziele und in der Vorlesung in einem Atemzug mit Non-repudiation und Accountability genannt – diese drei stehen alle in Bezug zu Identität und Verantwortung.

Authentizität wird in der Vorlesung wiederholt im Angriffs-Kontext zitiert: Bei den Angriffen *Replay*, *Modifikation der unverschlüsselten Nachricht*, *Modifikation der verschlüsselten Nachricht* und *Impersonation* wird die Auswirkung als „Integrität (Authentizität)" angegeben – Authentizität bricht damit zwangsläufig zusammen mit Integrität.

Typische Sicherheitsfunktionen laut Vorlesung: HMACs, digitale Signaturen.

## Bestandteile / Aufbau

Die Vorlesung unterscheidet implizit zwei Aspekte:
- **Datenauthentizität:** Stammen die Daten wirklich von der angegebenen Partei? (HMAC/Signatur)
- **Entitätsauthentizität:** Ist die andere Kommunikations-Partei wirklich diejenige, die sie vorgibt? (Identitätsmanagement-Protokolle, Folge-Vorlesung 05)

Diese explizite Trennung wird allerdings *im PDF nicht definiert*; sie ergibt sich aus den Anwendungsbeispielen.

## Beispiel

Aus Folie 25 (Impersonation): Eve injiziert oder verändert Nachrichten so, dass sie von Bob/Alice zu stammen scheinen. Auswirkung: Integrität (Authentizität). Schutz: HMACs, Signaturen.

## Abgrenzung

- Authentizität ist Voraussetzung für [[ASP - Security Eigenschaften - Non-repudiation]] und [[ASP - Security Eigenschaften - Accountability]] – ohne sichere Identität ist weder Beweisbarkeit noch Zurechenbarkeit möglich.
- Authentizität ist NICHT Vertraulichkeit. Eine signierte Nachricht ist authentisch, kann aber im Klartext öffentlich lesbar sein.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet Authentizität als Schutzziel?

**Anwendungsfrage:** Mit welchen Krypto-Bausteinen wird Authentizität in der Praxis sichergestellt? (HMAC, digitale Signaturen.)

**Diskussionsfrage:** Authentizität, Non-repudiation und Accountability werden oft verwechselt – wie würden Sie sie gegeneinander abgrenzen? Warum impliziert ein erfolgreicher Impersonation-Angriff zwingend einen Authentizitäts-Bruch?

**Mögliche Anschlussfragen:**
- Welcher Krypto-Baustein liefert Authentizität *plus* Non-repudiation, welcher nur Authentizität? (Signatur vs. HMAC.)
- Wann reicht eine HMAC nicht aus?
- Wie hängt Authentizität mit dem Begriff [[ASP - Identitaetsmanagement]] (folgt) zusammen?

## Verwandt

- [[ASP - Security Eigenschaften - Non-repudiation]]
- [[ASP - Security Eigenschaften - Accountability]]
- [[ASP - Angriff - Impersonation]]
- [[ASP - Hash - HMAC]]
- [[ASP - Digitale Signatur - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folien 13, 14, 25
