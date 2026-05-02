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

# ASP - Risikomanagement - Grundvoraussetzungen (Asset, Bedrohung, Schwachstelle)

> [!info] Kurzdefinition
> Ein Informationssicherheits-Risiko entsteht nur, wenn drei Voraussetzungen gleichzeitig erfüllt sind: ein schützenswertes **Asset**, eine **Bedrohung** und eine ausnutzbare **Schwachstelle**. Fehlt eines, gibt es kein Risiko.

## Beschreibung

Folie 3 zeigt die Trias als Venn-Diagramm: Asset, Bedrohung, Schwachstelle – die Schnittmenge ist das Risiko. Folie 4 gibt Beispiele.

### Asset
Schützenswerter Wert: Server, Anwendung, Daten, Gebäude, Mitarbeiter, Reputation usw.

### Bedrohung
Mögliche Ursache eines unerwünschten Ereignisses: Feuer, Stromausfall, Malware, Hacking, ehemaliger Mitarbeiter mit Insiderwissen, Naturereignis usw.

### Schwachstelle
Verwundbarkeit, die eine Bedrohung zur Schädigung des Assets nutzen kann: fehlende Brandschutzmaßnahmen, fehlendes USV, veraltete Systeme ohne Patches, schwache Login-Verfahren, fehlender Rechteentzug.

### Beispiele aus Folie 4

| Asset | Bedrohung | Schwachstelle |
|---|---|---|
| Unternehmensgebäude, Büroräume, Fertigungshalle, Serverraum | Feuer | Fehlende Brandschutzmaßnahmen |
| Serverraum, Server | Ausfall der Stromversorgung | Keine redundante Stromversorgung, keine USV |
| Server, Applikationen | Malware | Unzureichende Wartung, fehlendes Patchmanagement, veraltete Systeme |
| File Server, Laufwerke | Fehler bei Datenspeicherung, korrupte Daten, mutwillige Zerstörung | Fehlende Datensicherung, fehlende Restore-Tests |
| Server, Applikationen, Netzwerke | Hacking | Software-Schwachstellen, Software-Fehler, ungeschützte Netzwerke, fehlendes Logging, schwache Login-Verfahren |
| ERP-System, SAP, Laufwerke | Mutwillige Zerstörung von Daten durch ehemalige Mitarbeiter | Fehlende Prozesse zum Rechteentzug, fehlendes Logging, fehlende Backups |

### Übungs-Beispiele zur Begriffstrennung (Folie 5)

Aus dem PDF (Übungsaufgabe für die Studierenden – nicht direkt aufgelöst):
1. „Der Reifen hat kaum noch Profil." → Schwachstelle.
2. „Die Tür zum Warenlager steht häufig offen." → Schwachstelle.
3. „Die Aktivität von Cyberterroristen hat zugenommen." → Bedrohung (allgemein).
4. „Der entlassene Mitarbeiter hat gedroht, geheime Finanzdaten zu veröffentlichen, indem er die ihm bekannten technischen Schwachstellen ausnützt." → Risiko (Asset = Finanzdaten, Bedrohung = entlassener Mitarbeiter, Schwachstelle = bekannte technische Schwachstellen).
5. „Ein erfolgreicher Cyberangriff hat unsere Webseite für mehrere Stunden lahmgelegt." → Schadensereignis (kein Risiko mehr; Risiko hat sich realisiert).
6. „Der unter Punkt 5 genannte Angriff könnte zukünftig wieder passieren." → Risiko.
7. „Ein Anrufer könnte mittels Social Engineering Kennworte erfahren und somit Remotezugang zu den Buchhaltungsdaten gewinnen." → Risiko.

## Bestandteile / Aufbau

| Element | Frage | Beispiel |
|---|---|---|
| Asset | Was schützen wir? | Patientenakten |
| Bedrohung | Wer/was kann schaden? | Ransomware-Angriff |
| Schwachstelle | Wo greift es an? | nicht gepatchtes Betriebssystem |
| → Risiko | Schnittmenge der drei | mögliche Datenverschlüsselung mit Schaden |

## Beispiel

Patientendaten in einem Krankenhaus-System (Asset). Mögliche Ransomware-Welle (Bedrohung). Veralteter Windows-Server ohne aktuelle Patches (Schwachstelle). → Risiko = Verschlüsselung der Patientendaten mit Lösegeld-Forderung und ggf. Abbruch lebenswichtiger Prozesse.

## Abgrenzung

- **Bedrohung ≠ Risiko:** Eine Bedrohung allein ist noch kein Risiko (Beispiel 3: „Cyberterroristen" – ohne Asset und Schwachstelle keine Risikobewertung).
- **Schwachstelle ≠ Risiko:** Auch eine Schwachstelle allein erzeugt kein Risiko (Beispiel 1: abgefahrene Reifen sind erst dann ein Risiko, wenn man auch fährt).
- **Schadensereignis ≠ Risiko:** Wenn das Ereignis bereits eingetreten ist (Beispiel 5), spricht man von einem Schaden bzw. Vorfall – das Risiko hat sich realisiert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Voraussetzungen müssen für ein Risiko erfüllt sein?

**Anwendungsfrage:** Klassifiziere konkrete Aussagen als Asset, Bedrohung, Schwachstelle, Risiko oder Schadensereignis (siehe Übungs-Beispiele).

**Diskussionsfrage:** Warum genügt eine Bedrohung allein nicht? Warum genügt eine Schwachstelle allein nicht? Welcher Schritt im Risikomanagement-Prozess identifiziert die drei Komponenten? (Risikoidentifikation; siehe [[ASP - Risikomanagement - Asset-basierte Identifikation]].)

**Mögliche Anschlussfragen:**
- Welche Bedrohungen sind in eHealth besonders relevant? (Ransomware, Insider-Bedrohung, Gerätekompromittierung.)
- Welche Schwachstellen sind typisch in Krankenhaus-IT? (Veraltete medizinische Geräte mit Windows XP, fehlende Netzwerksegmentierung.)
- Wie hängt diese Trias mit der ISO-27005-Definition von Risiko zusammen?

## Verwandt

- [[ASP - Risikomanagement - Definition Risiko]]
- [[ASP - Risikomanagement - Risikoidentifikation Ansaetze]]
- [[ASP - Risikomanagement - Asset-basierte Identifikation]]
- [[ASP - Informationssicherheit - CIA-Triade]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 3, 4, 5
