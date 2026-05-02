# Excalidraw – Technische Referenz für Sub-Chats

Diese Datei wird von allen 7 Phase-3-Excalidraw-Sub-Chats als gemeinsame Referenz gelesen (Setup-Phase).

## Excalidraw-MCP Tools

Im Cowork-Chat ist ein Excalidraw-MCP-Server eingebunden. Die Tools heißen `mcp__<UUID>__create_view` und `mcp__<UUID>__read_me` (UUID variiert pro Session).

Wenn die Tools nicht direkt sichtbar sind: per `ToolSearch` mit Query `excalidraw` laden.

**Workflow:**

1. **Erstmalig:** `read_me` aufrufen, um Element-Format und Farb-Palette zu lernen.
2. **Pro Diagramm:** `create_view` mit JSON-Array von Elementen aufrufen → animierte Vorschau im Chat.
3. **Bei „passt":** Elemente in Vault-Format übersetzen (siehe unten) und als `.excalidraw.md` schreiben.

## Vault-Format: `.excalidraw.md`

Die Obsidian-Excalidraw-Plugin-Datei sieht exakt so aus:

````markdown
---
excalidraw-plugin: parsed
tags:
  - excalidraw
  - diagram
  - fach/<fach-tag-pfad>
---

==⚠ Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Excalidraw Data

## Text Elements

## Embedded Files

%%
## Drawing
```json
{
  "type": "excalidraw",
  "version": 2,
  "source": "https://excalidraw.com",
  "elements": [ ... ],
  "appState": {
    "gridSize": null,
    "viewBackgroundColor": "#ffffff"
  },
  "files": {}
}
```
%%
````

Wichtig:
- `excalidraw-plugin: parsed` im Frontmatter ist Pflicht – ohne erkennt das Plugin die Datei nicht.
- Tag `excalidraw` ist Pflicht.
- Der Drawing-JSON-Block wird in `%%`-Obsidian-Kommentare gewickelt, damit er in der Reading-View nicht als roher JSON-Text erscheint.
- Code-Block-Sprache: `json` (uncompressed). Das Plugin akzeptiert auch `compressed-json`, aber `json` ist debuggbar.
- `viewBackgroundColor`: `"#ffffff"` für hell, `"#1e1e2e"` für dunkel.
- Fach-Tag im Frontmatter setzen, damit die Diagramme per Tag-Filter im Fach-Kontext gefunden werden.

## Element-Konvertierung MCP → Excalidraw

Der MCP nutzt ein vereinfachtes Format. Beim Schreiben in das Vault muss in Standard-Excalidraw-Format konvertiert werden.

### Standard-Defaults pro Element

Diese Felder MUSS jedes Element haben (zusätzlich zu den MCP-Feldern):

```json
{
  "seed": <random integer 1..999999>,
  "version": 1,
  "versionNonce": <random integer 1..999999>,
  "isDeleted": false,
  "groupIds": [],
  "frameId": null,
  "roundness": null,
  "boundElements": [],
  "updated": <epoch millis, z.B. 1735000000000>,
  "link": null,
  "locked": false,
  "angle": 0,
  "strokeColor": "#1e1e1e",
  "backgroundColor": "transparent",
  "fillStyle": "solid",
  "strokeWidth": 2,
  "strokeStyle": "solid",
  "roughness": 1,
  "opacity": 100
}
```

Wenn der MCP einen abweichenden Wert gesetzt hat (z.B. `backgroundColor: "#a5d8ff"`), den verwenden.

Für gerundete Rechtecke: `"roundness": {"type": 3}`.

### Text-Element zusätzlich

```json
{
  "type": "text",
  "fontSize": 20,
  "fontFamily": 1,
  "text": "...",
  "textAlign": "center",
  "verticalAlign": "middle",
  "containerId": null,
  "originalText": "...",
  "lineHeight": 1.25,
  "autoResize": true,
  "baseline": <≈ fontSize * 0.85>
}
```

`fontFamily`: 1 = Hand-drawn (Default Excalidraw-Look), 2 = Normal (Helvetica), 3 = Code (Monospace).

### Arrow-Element zusätzlich

```json
{
  "type": "arrow",
  "points": [[0,0], [dx,dy]],
  "lastCommittedPoint": null,
  "startBinding": null,
  "endBinding": null,
  "startArrowhead": null,
  "endArrowhead": "arrow",
  "elbowed": false
}
```

Für Arrow-Bindings:
```json
"startBinding": {"elementId": "<shape-id>", "focus": 0, "gap": 8}
"endBinding": {"elementId": "<shape-id>", "focus": 0, "gap": 8}
```

### Label-Shortcut auflösen

MCP-Format mit `label`:
```json
{ "type": "rectangle", "id": "r1", "x": 100, "y": 100, "width": 200, "height": 80,
  "label": { "text": "Hello", "fontSize": 20 } }
```

Wird im Vault zu **zwei** Elementen:
1. Das Rechteck OHNE `label`-Feld, aber MIT `boundElements`:
   ```json
   { "type": "rectangle", "id": "r1", "x": 100, "y": 100, "width": 200, "height": 80,
     "boundElements": [{"id": "r1_label", "type": "text"}],
     ...standard defaults... }
   ```
2. Ein separates Text-Element mit `containerId`:
   ```json
   { "type": "text", "id": "r1_label", "x": 100, "y": 100, "width": 200, "height": 80,
     "text": "Hello", "fontSize": 20, "containerId": "r1",
     "textAlign": "center", "verticalAlign": "middle", "originalText": "Hello",
     "fontFamily": 1, "lineHeight": 1.25, "autoResize": true,
     ...standard defaults... }
   ```

(Das Plugin zentriert das Text-Element automatisch im Container.)

### `cameraUpdate` und `delete` weglassen

Im Vault-File werden `cameraUpdate` und `delete` Pseudo-Elemente NICHT mitgeschrieben – sie sind nur für die Chat-Animation. Das Vault-File enthält nur die finalen Elemente nach Anwendung aller deletes.

## Naming-Konvention für Excalidraw-Files

`<KÜRZEL> - Diagram - <Spezifischer Titel>.excalidraw.md`

Beispiele:
- `ASP - Diagram - CIA-Triade.excalidraw.md`
- `SM - Diagram - ITIL 4 Service Value System.excalidraw.md`
- `MSI - Diagram - HL7 CDA Aufbau.excalidraw.md`

## Einbettung in andere Notes

Nach Erstellung können die Diagramme in beliebige andere Notes per
`![[ASP - Diagram - CIA-Triade]]`
eingebettet werden – das Plugin rendert dann das Bild inline.

## Quelltreue-Regeln (gleich wie Konzept-Notes)

- Beschriftungen, Labels, Zahlen MÜSSEN aus den Konzept-Notes stammen.
- Keine Spec-/Lehrbuch-Inhalte aus dem Allgemeinwissen ergänzen.
- Wenn die Konzept-Note ein bestimmtes Beispiel nennt, dieses verwenden – nicht erfinden.
- Versionsangaben (FHIR R4, COBIT 2019, ITIL 4, ...) bei Frameworks und Standards mitnehmen, wenn Konzept-Note sie nennt.
