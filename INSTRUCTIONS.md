# INSTRUCTIONS für Cowork – Vault-Befüllung

**Diese Datei MUSS in jedem Cowork-Chat als Erstes gelesen werden, bevor mit der Bearbeitung eines PDFs begonnen wird.**

## Rolle und Ziel

Du befüllst einen bestehenden Obsidian-Vault zur Vorbereitung auf die mündliche Masterprüfung im Studiengang eHealth (FH JOANNEUM). Dein Output dient als Lerngrundlage für eine 15–20-minütige mündliche Prüfung pro Fachgebiet.

**Du erfindest keine eigenen Strukturen.** Du befüllst das vorhandene Skelett (Ordner, Templates, Tag-Schema, Naming-Konvention).

## Fächer und Ordnerzuordnung

| Kürzel | Fach | Ordner |
|---|---|---|
| ASP | Advanced Security and Privacy | `01_Fächer/Allgemein_MedInf/Security & Privacy/` |
| MSI | Medizinische Standards und Semantische Interoperabilität | `01_Fächer/Allgemein_MedInf/Interop/` |
| EHR | Electronic Health Records | `01_Fächer/Allgemein_MedInf/EHR/` |
| ITPM | IT-Projektmanagement | `01_Fächer/Vertiefung_ITM/IT-Projektmanagement/` |
| ITM-AK | IT-Management ausgewählte Kapitel | `01_Fächer/Vertiefung_ITM/IT-Management_AK/` |
| SM | Servicemanagement | `01_Fächer/Vertiefung_ITM/Servicemanagement/` |
| BPM | Business Process Management | `01_Fächer/Vertiefung_ITM/BPM/` |

**Quelle der Vorlesungs-PDFs:** Alle Folien liegen unter `Folien/` im Vault-Root, sortiert nach Fach (Folder-Namen sind die ausgeschriebenen Fachbezeichnungen, z. B. `Folien/Advanced Security and Privacy/`, `Folien/Medizinische Standards und Semantische Interop/`).

## Workflow pro PDF

1. Lies zuerst diese `INSTRUCTIONS.md`, dann die Templates in `_Templates/`.
2. Lies das angegebene PDF aus `_Attachments/` oder dem vom Nutzer angegebenen Pfad.
3. Bestimme das Fach-Kürzel (Nutzer gibt es vor; im Zweifel nachfragen).
4. Erzeuge **eine Vorlesungs-Note** (Template: `_Templates/Vorlesung.md`) im jeweiligen Fach-Ordner. Sie ist die Übersicht über den PDF-Inhalt und verlinkt auf alle daraus abgeleiteten Konzept-Notes.
5. Erzeuge **atomare Konzept-Notes** (Template: `_Templates/Konzept.md`) – eine Note pro klar abgrenzbarem Konzept. Faustregel: Wenn du das Konzept später isoliert abprüfen können willst, ist es eine eigene Note wert. Lieber zu granular als zu grob.
6. Aktualisiere das passende Fach-MOC (`00_MOCs/<Fach> - MOC.md`): Füge Wiki-Links zur neuen Vorlesung und zu allen neuen Konzept-Notes hinzu, ordne sie thematisch ein.
7. **Keine Karteikarten und keine Prüfungsfragen erzeugen.** Das passiert in Phase 2 in einem separaten Workflow.

## Naming-Konvention

**Pflicht-Format für alle Notes:**

```
<KÜRZEL> - <Thema> - <Spezifikation>.md
```

Beispiele:
- `MSI - HL7 FHIR - Bundle.md`
- `MSI - HL7 FHIR - Resource.md`
- `ASP - Authentifizierung - OAuth2.md`
- `EHR - ELGA - Architektur.md`
- `ITPM - PMBOK - Wissensgebiete.md`

**Vorlesungs-Notes:**
```
<KÜRZEL> - VL - <Vorlesungstitel oder Datum>.md
```
Beispiel: `MSI - VL - HL7 FHIR Grundlagen.md`

**Regeln:**
- Bindestriche als Trenner, keine Unterstriche, keine Slashes im Dateinamen.
- Keine Umlaute in Pfaden, falls vermeidbar (Ausnahme: bestehende Ordner wie `01_Fächer` und `03_Prüfungsfragen` sind okay – Obsidian kommt damit klar, externe Skripte teils nicht).
- Englische Fachbegriffe bleiben englisch (FHIR, OAuth2, RBAC, …).
- Bei Mehrdeutigkeit: erst Oberkategorie, dann Spezifikation (`HL7 FHIR - Bundle`, nicht `Bundle - HL7 FHIR`). Das hält verwandte Notes in der Dateiliste beieinander.

**Ausnahme – atomare Konzepte (2-Segment-Format):**
Bei Begriffen, für die ein erzwungenes drittes Segment künstlich wäre (Eigennamen, Modelle, einzelne Methoden), darf das 2-Segment-Format `<KÜRZEL> - <Thema>.md` verwendet werden. Beispiele: `ITPM - Wasserfallmodell.md`, `ITPM - Brooks's Law.md`, `ITM-AK - BCG-Matrix.md`, `ITM-AK - Bilanz.md`, `BPM - PDCA-Zyklus.md`. Faustregel: wenn das dritte Segment den Titel nur künstlich verlängern würde, weglassen. Wenn das Konzept Teil eines Clusters ist (mehrere verwandte Notes), das 3-Segment-Format bevorzugen, um die Notes in der Dateiliste beieinander zu halten.

## Tag-Schema

Jede Note bekommt im Frontmatter mindestens:

- **Fach-Tag** (genau einer):
  `#fach/allgemein/asp` · `#fach/allgemein/msi` · `#fach/allgemein/ehr` · `#fach/vertiefung/itpm` · `#fach/vertiefung/itm-ak` · `#fach/vertiefung/sm` · `#fach/vertiefung/bpm`
- **Typ-Tag** (genau einer):
  `#typ/konzept` · `#typ/vorlesung` · `#typ/moc` · `#typ/pruefungsfrage`
- **Status-Tag** (genau einer):
  `#status/offen` (Standard für neu erzeugte Notes – signalisiert: vom Nutzer noch nicht inhaltlich geprüft) · `#status/geprüft`

Cross-Fach-Konzepte in `02_Konzepte/` bekommen mehrere Fach-Tags.

## Verlinkung

- **Wiki-Links** verwenden: `[[MSI - HL7 FHIR - Bundle]]` (ohne `.md`, ohne Pfad).
- Jede Konzept-Note verlinkt **nach oben** auf ihre Vorlesungs-Note (Feld „Quelle" im Template).
- Jede Konzept-Note verlinkt **seitwärts** auf inhaltlich verwandte Konzepte (Sektion „Verwandt"). Wenn du die verwandte Note kennst (existiert im Vault) → echter Wiki-Link. Wenn sie noch nicht existiert, aber existieren sollte → trotzdem Wiki-Link setzen (wird zu „unresolved link", ist gewollt – signalisiert offene Stellen).
- **Keine Backlinks manuell pflegen.** Obsidian erzeugt sie automatisch.

## Inhaltliche Regeln

**Quelltreue:**
- Jede inhaltliche Aussage in einer Konzept-Note muss aus dem PDF stammen oder als externes Wissen klar gekennzeichnet sein (Sektion „Ergänzung außerhalb der Vorlesung" – nur verwenden, wenn unverzichtbar).
- Bei Standards (HL7, IHE, FHIR-Versionen, ITIL, ISO-Normen) **Versionsnummer/Edition mitgeben**, wenn im PDF angegeben.
- **Nicht halluzinieren.** Wenn ein Begriff im PDF nur erwähnt, aber nicht erklärt wird: in der Note als „im PDF nicht definiert" markieren, nicht aus dem Allgemeinwissen ergänzen.

**Granularität:**
- Eine Konzept-Note = ein Konzept. „HL7 FHIR" ist zu groß für eine Note. „FHIR Bundle", „FHIR Resource", „FHIR Profile" sind je eine eigene Note.
- Faustregel: Wenn die Note länger als ~400 Wörter im Hauptteil wird, prüfe, ob sie aufgeteilt werden sollte.

**Mündliche-Prüfungs-Perspektive:**
- Die Prüfung dauert 15–20 Minuten pro Fach und ist diskursiv. Reine Definitionen reichen nicht.
- Jede Konzept-Note enthält eine Sektion „Prüfungsrelevanz", die festhält: typische Anschlussfragen, Vergleichsachsen zu anderen Konzepten, kritische Diskussionspunkte. Diese Sektion ist die wichtigste Sektion der Note.

## Sprache

**Notes auf Deutsch.** Fachbegriffe und Standardnamen bleiben englisch (FHIR, ITIL, OAuth2, RBAC, ABAC, SMART on FHIR, …). Bei Erstnennung in einer Note: kurze deutsche Erklärung in Klammern.

## Was du NICHT tust

- Keine Karteikarten generieren (Phase 2).
- Keine Prüfungsfragen generieren (Phase 2).
- Keine Inhalte aus dem Vault löschen oder überschreiben ohne expliziten Auftrag.
- Keine Templates oder diese `INSTRUCTIONS.md` modifizieren.
- Keine eigene Ordnerstruktur erfinden.
- Keine Inhalte erfinden, die nicht im PDF stehen (Ausnahme: explizit gekennzeichnete Ergänzungen).

## Output-Bestätigung

Am Ende jedes PDF-Bearbeitungs-Chats kurze Zusammenfassung an den Nutzer:
- Verarbeitetes PDF (Dateiname)
- Erzeugte Vorlesungs-Note (1)
- Erzeugte Konzept-Notes (Liste mit Anzahl)
- Aktualisiertes MOC
- Hinweise auf unklare Stellen im PDF, die der Nutzer prüfen sollte
