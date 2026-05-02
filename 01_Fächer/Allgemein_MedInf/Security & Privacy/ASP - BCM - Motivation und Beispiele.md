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

# ASP - BCM - Motivation und Beispiele (Gesundheitswesen)

> [!info] Kurzdefinition
> Das Gesundheitswesen ist hochgradig abhängig von ununterbrochenen Abläufen für Patientenversorgung und -sicherheit. Vier Gründe für BCM, illustriert an zwei realen Beispielen: WannaCry-Cyberangriff auf NHS 2017 und COVID-19-Pandemie 2022.

## Beschreibung

### Herausforderungen im Gesundheitswesen (Folie 2)
- **Kritische Abhängigkeit:** Hochgradige Abhängigkeit von ununterbrochenen Abläufen für Patientenversorgung und -sicherheit.
- **Risikoexposition:** Exposition gegenüber Naturkatastrophen, Pandemien, Cyberangriffen und technischen Ausfällen.

Typische Risikoquellen visualisiert in einem BCM-Kreis (Folie 2): Elementargefahren, Pandemien, Internet-Blackouts, Cyber-Vorfälle, Stromausfall, Server-Ausfall.

### Vier Gründe für BCM im Gesundheitswesen (Folie 2)
1. **Patientenversorgung:** Gewährleistung der kontinuierlichen und zuverlässigen Versorgung von Patienten in Krisen.
2. **Reputations- und Vertrauensschutz:** Bewahrung des Vertrauens von Patienten und der Öffentlichkeit durch kontinuierliche Qualität und Zuverlässigkeit.
3. **Compliance-Anforderungen:** Einhaltung gesetzlicher Vorschriften und regulatorischer Standards.
4. **Risikomanagement:** Proaktive Minimierung von Risiken, um unerwünschte Auswirkungen auf die Gesundheitsdienste zu vermeiden.

### Beispiel 1: WannaCry-Cyberangriff auf NHS (2017, Folie 3)
- **Malware-Angriff** traf den britischen National Health Service: Krankenhäuser und Praxen betroffen.
- **Absage von Operationen** und **Schließung von Notfallzentren**.
- Einschränkungen in **digitaler Bildgebung und Patientenaktenzugriff**.

**Ursachen und Risiken:**
- Veraltete Betriebssysteme und gekürzter Sicherheitssupport aufgrund Finanzierungsmangel.
- Gefährdung der Patientensicherheit bei IT-Angriffen in unterfinanzierten Gesundheitssystemen.

**Notwendigkeit neuer Maßnahmen:**
- Ärzte betonen Verantwortung für aktuelle Software und Schulungen zu IT-Sicherheit.
- Digitale Medizin hat Vorteile, erfordert jedoch verstärkte IT-Sicherheitsüberlegungen und angemessene Finanzierung.

### Beispiel 2: COVID-19-Pandemie 2022 (Folie 4)
- Pandemie stellte das Gesundheitswesen vor enorme Herausforderungen.
- Belastung der Krankenhäuser durch hohe Patientenanzahl und begrenzte Ressourcen.

**Auswirkungen auf die Gesundheitssysteme:**
- Überlastung der Intensivstationen und Herausforderungen bei der Ressourcenallokation.
- Notwendigkeit schneller Anpassungen von Gesundheitsrichtlinien und Behandlungsprotokollen.

**Langfristige Lehren und Veränderungen:**
- Betonung der Bedeutung von Vorsorge, Resilienz und besserer Vorbereitung auf Pandemien.
- Notwendigkeit von Investitionen in die Gesundheitssysteme und Digitalisierung für Krisensituationen.

## Bestandteile / Aufbau

| Risikoquelle | Beispiel-Auswirkung |
|---|---|
| Cyberangriff | Operationen abgesagt (NHS WannaCry) |
| Pandemie | Intensivstation überlastet (COVID 2022) |
| Stromausfall | Geräte fallen aus |
| Naturkatastrophe | Standort nicht erreichbar |
| Server-Ausfall | Patientenakten unzugänglich |

## Beispiel

NHS WannaCry und COVID, je ausführlich in den Folien 3 und 4. Beide zeigen: Wenn das Gesundheitssystem nicht resilient ist, sind Operationen, Akten-Zugriffe und Behandlungs-Kapazität direkt betroffen – mit unmittelbaren Folgen für die Patientensicherheit.

## Abgrenzung

- **Motivation ≠ Methode.** Diese Note begründet nur, *warum* BCM nötig ist; das *wie* folgt im BCMS und in der BIA.
- **Cyberangriff vs. Pandemie:** Beide BCM-relevant, aber sehr unterschiedliche Antwort-Maßnahmen (technisch-organisatorisch vs. Personal/Ressourcen-Skalierung).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Warum ist BCM im Gesundheitswesen besonders wichtig? Welche vier Gründe nennt die Vorlesung?

**Anwendungsfrage:** Erläutere am Beispiel WannaCry NHS, welche BCM-Aspekte unzureichend waren und welche Maßnahmen das verhindert hätten.

**Diskussionsfrage:** Welche Lehren aus der COVID-19-Pandemie sollten Eingang in das BCM-Konzept eines Krankenhauses finden? Welche Trade-offs entstehen zwischen Vorsorge-Investitionen und laufenden Kosten?

**Mögliche Anschlussfragen:**
- Welche IT-Maßnahmen hätten WannaCry verhindert? (Patch-Management, Netzwerksegmentierung, Awareness-Schulungen.)
- Welche der vier Gründe sind eHealth-spezifisch, welche universell?
- Wie hängt BCM mit dem Schutzziel Verfügbarkeit aus der CIA-Triade zusammen?

## Verwandt

- [[ASP - BCM - Managementsystem]]
- [[ASP - BCM - Business Impact Analyse]]
- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - Angriff - Denial-of-Service]]
- [[ASP - Security Eigenschaften - Reliability]]

## Quelle

- Vorlesung: [[ASP - VL - Business Continuity Management]]
- Folien/Seitenangabe: Folien 2, 3, 4
