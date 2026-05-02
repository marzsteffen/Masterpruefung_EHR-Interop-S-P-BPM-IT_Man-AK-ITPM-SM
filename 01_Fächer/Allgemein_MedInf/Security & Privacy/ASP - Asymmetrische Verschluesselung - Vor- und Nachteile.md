---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Verschluesselungsmethoden]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Asymmetrische Verschlüsselung - Vor- und Nachteile

> [!info] Kurzdefinition
> Asymmetrische Verfahren lösen das Schlüsselaustausch-Problem und bieten Authentifizierung per Signatur. Hauptkosten sind Performance (ca. 100.000× langsamer als symmetrisch), große Schlüssellängen und der Mehraufwand bei mehreren Empfängern.

## Beschreibung

Bilanz laut Folie 34 und Folie 52.

**Vorteile (Folie 34):**
- **Hohe Sicherheit** (auch vom Algorithmus abhängig).
- **Geringerer Aufwand der Geheimhaltung → Kein Schlüsselverteilungsproblem.**
- **Bietet Möglichkeit zur Authentifizierung (Signatur).**

**Nachteile (Folie 34):**
- **Viel langsamer als symmetrische Algorithmen (ca. 100 000 Mal langsamer).**
- **Benötigt große Schlüssellänge.**
- **Für jeden Empfänger muss extra verschlüsselt werden.**

**Vertiefung Folie 52 (Performance / mehrere Empfänger):**
- Hoher Aufwand für Ver- und Entschlüsselung (RSA langsamer als ECC).
- Große Schlüsselgröße bei RSA.
- **Asymmetrische Operationen ca. 10 000× langsamer als symmetrische.** *Hinweis: Folie 34 nennt 100 000×, Folie 52 nennt 10 000× – Diskrepanz innerhalb der Vorlesung. Der Größenordnungs-Bereich ist gemeint, nicht eine exakte Zahl.*
- Bei mehreren Empfängern: Nachricht muss für jeden Empfänger individuell verschlüsselt werden (jeweils mit dessen Public Key).

## Bestandteile / Aufbau

| Aspekt | Bewertung |
|---|---|
| Schlüsselverteilung | Sehr einfach (Public Key öffentlich) |
| Performance | Niedrig (10 000–100 000× langsamer als symmetrisch) |
| Authentifizierung (Signatur) | Möglich |
| Schlüsselgröße | Groß (RSA: mind. 2048 Bit; ECC kleiner) |
| Mehrere Empfänger | Pro Empfänger eine eigene Verschlüsselung |
| Skalierung Schlüssel | n Schlüsselpaare bei n Teilnehmern (statt n²) |

## Beispiel

Aus Folie 52: Will Alice eine Nachricht an 5 Empfänger asymmetrisch verschlüsseln, muss sie den Klartext fünfmal mit jeweils einem anderen Public Key verschlüsseln und fünf Ciphertexte versenden – statt einmal symmetrisch und der gleiche Ciphertext für alle.

## Abgrenzung

- **Asymmetrisch vs. [[ASP - Symmetrische Verschluesselung - Vor- und Nachteile]]:** Asymmetrisch löst Schlüsselaustausch und bietet Signatur, ist aber deutlich langsamer und schlechter für Massenverschlüsselung.
- Genau aus dieser Komplementarität ergibt sich [[ASP - Hybride Verschluesselung - Grundlagen]]: Beide werden kombiniert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Vor- und Nachteile hat asymmetrische Verschlüsselung gegenüber symmetrischer?

**Anwendungsfrage:** Warum verwendet man in der Praxis (z. B. TLS) selten reine asymmetrische Verschlüsselung für die Inhalts-Übertragung? (Performance, Skalierung.)

**Diskussionsfrage:** Welcher Vorteil rechtfertigt die schlechtere Performance? (Schlüsselverteilung, Signatur.) Wie löst die hybride Verschlüsselung das Performance-Problem?

**Mögliche Anschlussfragen:**
- Welche typische RSA-Schlüssellänge wird heute empfohlen? (laut Folie 41: 2048 Bit.)
- Warum ist ECC schneller als RSA bei vergleichbarer Sicherheit? (Kürzere Schlüssel, einfachere Operationen – siehe [[ASP - Asymmetrische Verschluesselung - ECC]].)
- Wie skaliert die Schlüsselanzahl bei n Teilnehmern? (asymmetrisch: n Paare; symmetrisch paarweise: n·(n-1)/2.)

## Verwandt

- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Symmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]
- [[ASP - Asymmetrische Verschluesselung - RSA]]
- [[ASP - Asymmetrische Verschluesselung - ECC]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe Kapitel 02: Folien 34, 52
- Wiederholung in Kapitel 03, Folien 14 und 26 – inhaltlich deckungsgleich; auf Folie 14 fehlt der Punkt „Benötigt große Schlüssellänge".

## Ergänzung außerhalb der Vorlesung

Die widersprüchlichen Performance-Angaben (100 000× auf Folie 34 vs. 10 000× auf Folie 52) sind Größenordnungs-Faustformeln; reale Ratios hängen vom Algorithmus, der Schlüssellänge und der Hardware ab. Für die Praxis genügt: asymmetrische Operationen sind um Größenordnungen teurer als symmetrische, weshalb sie typischerweise nur einmal pro Sitzung (für den Schlüsselaustausch und ggf. eine Signatur) verwendet werden.
