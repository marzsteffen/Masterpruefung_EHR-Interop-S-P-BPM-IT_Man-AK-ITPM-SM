---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Informationssicherheits-Risikomanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Risikomanagement - Asset-basierte Risikoidentifikation (6 Schritte)

> [!info] Kurzdefinition
> Bottom-up-Methode in 6 Schritten nach BSI-IT-Grundschutz: Strukturanalyse + Schutzbedarfsfeststellung, IT-Grundschutz-Modellierung, Gefährdungsübersicht, Anforderungsübersicht, Schwachstellenanalyse, Risikoliste.

## Beschreibung

Die Vorlesung führt den asset-basierten Ansatz in **sechs Schritten** durch (Folien 19–29). Der Ablauf folgt der **BSI 200-2 IT-Grundschutz-Methodik**.

### Schritt 1: Strukturanalyse und Schutzbedarfsfeststellung (Folien 20–22)
- Detaillierte Auflistung aller Assets und ihrer Abhängigkeiten.
- Beginnt bei Geschäftsprozessen und Informationen.
- **Top-Down-Approach** innerhalb dieses Schritts: von Prozess-Ebene über Anwendungs-Ebene zur IT-System-Ebene.
- Erleichtert die Schutzbedarfsfeststellung durch **Vererbung** des Schutzbedarfs.
- Pro Asset wird der Schutzbedarf für die drei CIA-Schutzziele festgelegt (Beispiel Folie 22 – Active Directory: Vertraulichkeit 5, Integrität 5, Verfügbarkeit 5).

### Schritt 2: IT-Grundschutz-Modellierung gemäß BSI 200-2 (Folien 24–26)
Siehe [[ASP - Risikomanagement - IT-Grundschutz BSI 200-2]] für Details.
Das IT-Grundschutz-Kompendium enthält:
- IT-Grundschutz-Bausteine.
- Gefährdungskataloge.
- Maßnahmenkataloge.

### Schritt 3: Gefährdungsübersicht (Folien 28–29)
Pro Zielobjekt werden drei Klassen von Gefährdungen gesammelt:
- **Elementare Gefährdungen** (z. B. G 0.18 Fehlplanung, G 0.21 Manipulation Hard-/Software).
- **Spezifische Gefährdungen** (z. B. „Fehlerhafte Konfiguration der Virtualisierung").
- **Zusätzliche Gefährdungen** durch Workshops/Brainstorming, wenn IT-Grundschutz-Baustein fehlt oder Einsatzszenario nicht abgedeckt ist.

### Schritt 4: Anforderungsübersicht (Folie 31)
**Soll-Ist-Vergleich** bestehender und erforderlicher Schutzmaßnahmen pro Baustein.
Beispiel-Baustein NET.1.1 (Netzarchitektur und -design):
- Basis-Anforderungen (z. B. Sicherheitsrichtlinie für das Netz).
- Standard-Anforderungen (z. B. Spezifikation der Netzarchitektur).
- Anforderungen für erhöhten Schutzbedarf (z. B. hochverfügbare Netz- und Sicherheitskomponenten).
Pro Anforderung wird eingetragen: erfüllt? ja/nein.

### Schritt 5: Schwachstellenanalyse (Folie 33)
Aus dem Soll-Ist-Vergleich werden die nicht erfüllten Anforderungen als **Schwachstellen** identifiziert. Beispiel-Baustein OPS.1.1.4 (Schutz vor Schadprogrammen): Schutzmechanismen aktiv (✔), aber Konzept fehlt (✘) → Schwachstelle.

### Schritt 6: Risikoliste (Folie 35)
Pro Risiko werden die **Mindestfaktoren** dokumentiert:
- **Wer** (Angreifer / Gefahrenquelle).
- **Tut Was** (Schwachstelle, Angriff, Bedrohung).
- **Gegen Wen** (Asset, Wert, Ziel, Opfer).
- **Mit welcher Auswirkung** (Schaden, welches Interesse des Unternehmens wird verletzt?).

## Bestandteile / Aufbau

| Schritt | Hauptaktivität | Ergebnis |
|---|---|---|
| 1 | Strukturanalyse + Schutzbedarf | Asset-Liste mit Schutzbedarfsklassen |
| 2 | IT-Grundschutz-Modellierung | Bausteine pro Asset |
| 3 | Gefährdungsübersicht | Liste relevanter Gefährdungen |
| 4 | Anforderungsübersicht | Soll-Ist je Baustein-Anforderung |
| 5 | Schwachstellenanalyse | Nicht erfüllte Anforderungen |
| 6 | Risikoliste | strukturierte Risiken |

## Beispiel

Aus Folien 22, 27, 29, 31, 33, 35:
- **Schritt 1:** Asset Active Directory; Schutzbedarf C/I/A jeweils 5.
- **Schritt 2:** Baustein SYS.1.5 Virtualisierung anwendbar.
- **Schritt 3:** Gefährdungen wie „Fehlerhafte Planung", „Kompromittierung der Virtualisierungssoftware".
- **Schritt 4:** Soll-Ist je Anforderung: „Einspielen von Updates" erfüllt; „Härtung des Virtualisierungsservers" nicht erfüllt.
- **Schritt 5:** Schwachstelle: fehlende Härtung.
- **Schritt 6:** Risiko: Angreifer (Wer) nutzt Schwachstelle der nicht-gehärteten Virtualisierung (Tut Was) gegen das Active Directory (Gegen Wen) → Verlust der Vertraulichkeit von Mitarbeiterdaten (Auswirkung).

## Abgrenzung

- **Asset-basiert ≠ Ereignis-basiert** (siehe [[ASP - Risikomanagement - Risikoidentifikation Ansaetze]]).
- **6 Schritte ≠ 7 Schritte des Big Picture:** Diese 6 Schritte sind nur die Risikoidentifikation (Schritt 2 im Big Picture).
- **BSI 200-2 vs. ISO 27005:** ISO ist Rahmen, BSI ist Methode für die konkrete Durchführung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche sechs Schritte umfasst die asset-basierte Risikoidentifikation? Was passiert in jedem Schritt?

**Anwendungsfrage:** Wenden Sie die Methode auf ein konkretes eHealth-Asset (z. B. Patientenakten-Server) an. Welche Bausteine sind relevant, welche Gefährdungen erwarten Sie?

**Diskussionsfrage:** Welcher Schritt ist in der Praxis am aufwändigsten? (Schritt 1 – Strukturanalyse und Schutzbedarfsfeststellung; oft mehrere Personenwochen.) Welche Vor- und Nachteile bringt die strikte Bindung an BSI 200-2?

**Mögliche Anschlussfragen:**
- Was sind elementare vs. spezifische Gefährdungen?
- Wie wird der Schutzbedarf eines Assets vererbt?
- Welche vier Mindestfaktoren beschreibt ein Risiko-Eintrag?

## Verwandt

- [[ASP - Risikomanagement - Risikoidentifikation Ansaetze]]
- [[ASP - Risikomanagement - Strukturanalyse und Schutzbedarf]]
- [[ASP - Risikomanagement - IT-Grundschutz BSI 200-2]]
- [[ASP - Risikomanagement - Grundvoraussetzungen]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 19–35
