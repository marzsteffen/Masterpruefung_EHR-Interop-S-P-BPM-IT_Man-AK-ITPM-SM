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

# ASP - Security Eigenschaften - Rückverfolgbarkeit (Non-repudiation)

> [!info] Kurzdefinition
> Erfolgte Tätigkeiten müssen nachweisbar und nicht-abstreitbar sein (laut Folie 14).

## Beschreibung

Rückverfolgbarkeit (Non-repudiation) ist die Eigenschaft, dass eine Partei eine durchgeführte Handlung im Nachhinein nicht plausibel abstreiten kann. Im engeren Sinne bedeutet das: Es existiert ein Beweismittel, das die Tätigkeit zweifelsfrei der Partei zuordnet und gegenüber Dritten (z. B. einem Gericht) standhält.

Die Vorlesung führt Non-repudiation als eines der acht Schutzziele auf der Security-Grafik (Folie 13) ein und definiert sie auf Folie 14 mit einer Zeile.

Konkrete Mechanismen werden in der Einführung *nicht* benannt – das gehört zur Folge-Vorlesung Hash/MAC/Signaturen. **Im PDF nicht definiert:** welche kryptografische Primitive Non-repudiation liefern (typischerweise digitale Signaturen mit asymmetrischer Krypto, weil nur der Inhaber des privaten Schlüssels signieren kann; HMAC reicht *nicht*, weil beide Parteien den geteilten Schlüssel kennen).

## Beispiel

*Im PDF nicht explizit als Beispiel ausgewiesen.* Naheliegender Anwendungsfall ist die Signatur eines Arztbriefs: Der Arzt kann später nicht abstreiten, den Befund unterschrieben zu haben.

## Abgrenzung

- **Non-repudiation vs. Authenticity:** Authentizität sagt aus „die Nachricht stammt von Alice"; Non-repudiation sagt zusätzlich aus „Alice kann das nicht gegenüber Dritten abstreiten". Beide Eigenschaften können auseinanderfallen: HMAC liefert Authentizität, aber keine Non-repudiation, weil auch der Empfänger den Schlüssel hat und die Nachricht hätte erzeugen können.
- **Non-repudiation vs. Accountability:** Accountability adressiert primär die Zurechenbarkeit innerhalb einer Organisation (intern); Non-repudiation adressiert die Beweisbarkeit auch gegenüber Dritten (extern, ggf. juristisch). Diese Abgrenzung ist allerdings *im PDF nicht explizit* gezogen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet Non-repudiation als Schutzziel?

**Anwendungsfrage:** Welcher Krypto-Baustein liefert Non-repudiation, welcher nicht – und warum?

**Diskussionsfrage:** Non-repudiation und Accountability klingen ähnlich – worin unterscheiden sie sich? Warum kann eine reine HMAC-Konstruktion Non-repudiation nicht erfüllen?

**Mögliche Anschlussfragen:**
- Welche Schlüsselart ist nötig, damit Non-repudiation kryptografisch garantiert ist? (Privater Schlüssel mit asymmetrischem Verfahren.)
- Wie wirkt eine kompromittierte CA auf die Non-repudiation digitaler Signaturen?
- Warum ist Non-repudiation für eHealth-Workflows (z. B. Verordnungen) besonders relevant?

## Verwandt

- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Security Eigenschaften - Accountability]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Hash - HMAC]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folien 13, 14
