---
fach: itm-ak
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/vertiefung/itm-ak
---

# ITM-AK - PF - Finanzwesen

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Diese PF-Note deckt den Finanzmanagement-Block aus ITM-AK ab: Jahresabschluss-Elemente, Bilanz, GuV, Kapitalflussrechnung, Eigenkapitalveränderungsrechnung, alle Kennzahlen (Bilanz-, GuV-, Cashflow-Kennzahlen), GAAP/IFRS, Rechnungswesen intern vs. extern, Finanzierungsformen und Shareholder vs. Stakeholder Value. Quellvorlesung: VL „IT-Management Einführung und Finance". Reale Beispiele aus der VL: Mediclinic-Bilanz 2021, Moderna-GuV und -Cashflow 2021.

## Verlinkte Konzepte

- [[ITM-AK - Jahresabschluss - Elemente]]
- [[ITM-AK - Bilanz]]
- [[ITM-AK - Gewinn- und Verlustrechnung]]
- [[ITM-AK - Kapitalflussrechnung]]
- [[ITM-AK - Eigenkapitalveränderungsrechnung]]
- [[ITM-AK - Bilanzanalyse - Kennzahlen]]
- [[ITM-AK - GuV-Analyse - Kennzahlen]]
- [[ITM-AK - Cashflow-Analyse - Kennzahlen]]
- [[ITM-AK - GAAP und IFRS]]
- [[ITM-AK - Rechnungswesen - Externes vs Internes]]
- [[ITM-AK - Finanzierung - Eigen- vs Fremd- intern vs extern]]
- [[ITM-AK - Finanzierung - Phasen der Unternehmensfinanzierung]]
- [[ITM-AK - Shareholder vs Stakeholder Value]]
- [[ITM-AK - Finanzmanagement - Definition und Aufgaben]]

---

## Karten

### Definition

Welche sechs Elemente enthält ein Jahresabschluss nach IFRS-Logik?

?

| Element | Englisch | Funktion |
|---|---|---|
| **Bilanz** | balance sheet | Status quo zum Stichtag (Vermögen, Schulden, Eigenkapital) |
| **Gewinn- und Verlustrechnung** | income statement | Erfolg über eine Periode (Erträge − Aufwendungen → Net Income) |
| **Kapitalflussrechnung** | cash-flow statement | Zahlungsmittelbewegungen der Periode |
| **Aufstellung Eigenkapitalveränderung** | statement of changes in equity | Entwicklung jeder Eigenkapitalkomponente |
| **Anmerkungen** | notes | Methodenbeschreibung, Erläuterungen zu Positionen |
| **Lagebericht** | — | Nach österreichischem Recht verpflichtend; Zukunftsaussichten, Risiken |

Wichtige Verknüpfungen: GuV → Bilanz (einbehaltene Gewinne ins Eigenkapital); GuV → Cashflow (Net Income als Startwert); Bilanz → Cashflow (Veränderungen in Bilanzpositionen = Adjustments).

---

Was ist die Bilanz und wie lautet die Bilanzgleichung? Beschreiben Sie Aktiva und Passiva.

?

Die Bilanz (balance sheet) stellt Vermögenswerte, Verbindlichkeiten und Eigenkapital eines Unternehmens zu einem **Stichtag** (in der Regel Jahresende) dar.

**Bilanzgleichung:**
```
Aktiva (Vermögen) = Passiva (Schulden) + Eigenkapital
→ Eigenkapital = Aktiva − Passiva
```

**Aktiva:**
- Umlaufvermögen: Bargeld/Wertpapiere, Forderungen (Debitoren), Vorräte, sonstiges UV
- Anlagevermögen: Sachanlagen (Immobilien, Ausrüstung, Fahrzeuge), immaterielle Vermögenswerte

**Passiva + Eigenkapital:**
- Kurzfristige Verbindlichkeiten (z. B. Lieferantenkredite)
- Langfristige Verbindlichkeiten (Schulden, Leasing, gestundete Steuern)
- Eigenkapital: Stammkapital, Rücklagen, einbehaltene Gewinne

Leitfragen laut VL: „Was gehört dem Unternehmen?" / „Was ist es schuldig?" / „Was haben die Anteilseigner?"

---

Beschreiben Sie den schematischen Aufbau der Gewinn- und Verlustrechnung von oben nach unten.

?

Die GuV (income statement) beginnt mit den Umsatzerlösen und berechnet schrittweise das Nettoeinkommen:

```
Total Revenue (Gesamtumsatz)
− COGS (Cost of Goods Sold)
                              = Bruttoergebnis
− Betriebliche Aufwendungen (R&D, SG&A)
                              = EBITDA  (vor Abschreibungen, Zinsen, Steuern)
− Abschreibungen / Amortisationen (D&A)
                              = EBIT    (Operatives Ergebnis)
− Zinsen
                              = EBT     (Ergebnis vor Steuern)
− Steuern
                              = Net Income (Nettoeinkommen)
```

**Links:** Net Income → einbehaltene Gewinne (Bilanz); Net Income → Startwert der Kapitalflussrechnung.

---

Beschreiben Sie die drei Bereiche der Kapitalflussrechnung.

?

Die Kapitalflussrechnung (cash-flow statement) beginnt mit dem **Nettoeinkommen** aus der GuV und gliedert Zahlungsmittelbewegungen in drei Bereiche:

| Bereich | Inhalte |
|---|---|
| **Cashflow aus operativer Tätigkeit (CFO)** | Reingewinn; Abschreibung/Amortisation; Veränderung Forderungen/Verbindlichkeiten; Vorräte |
| **Cashflow aus Investitionstätigkeit (CFI)** | Übernahmen, Kapitalinvestitionen (Kauf/Verkauf Sachanlagen) |
| **Cashflow aus Finanzierungstätigkeit (CFF)** | Dividenden; Kauf/Verkauf eigener Aktien; kurz- und langfristige Kreditaufnahme/-tilgung |

**Endergebnis:** CFO + CFI + CFF = Nettoveränderung Cash → + Cash zu Periodenbeginn = **Cash zu Periodenende** (erscheint in der Bilanz).

---

Was ist der Unterschied zwischen GAAP und IFRS und warum gibt es IFRS?

?

| Merkmal | GAAP | IFRS |
|---|---|---|
| Gültigkeitsbereich | National (z. B. Österreich-GAAP, UK-GAAP, US-GAAP) | International, über 140 Staaten |
| Einheitlichkeit | Kein einheitlicher Standard – jedes Land eigene Regeln | Einheitlicher Rahmen |
| Fokus | Nationale Gesetze, lokale Steuerregeln | Vergleichbarkeit, Investorenschutz |

**Warum IFRS?** (laut VL, Folie 45):
- Internationale Normen
- Objektivität
- Ähnliche Bewertung von Vermögenswerten (Lehre aus Finanzskandalen)
- International anerkannter Rahmen

[Ergänzung] Für kapitalmarktorientierte Unternehmen in der EU seit 2005 für konsolidierte Abschlüsse verpflichtend (EU-Verordnung 1606/2002) – nicht im PDF angegeben.

---

Was ist der Unterschied zwischen Shareholder Value und Stakeholder Value?

?

| Aspekt | Shareholder Value | Stakeholder Value |
|---|---|---|
| Adressat | Aktionäre / Eigentümer | Alle Interessengruppen |
| Maßstab | Aktienkurs, Dividenden, Gewinn | Breiter Wertbegriff (auch nicht-monetär) |
| Frage | „Wie viel ist das Unternehmen in Geld wert?" | „Welchen Wert schafft es für Gesellschaft, Umwelt, Mitarbeiter, Kunden?" |
| Perspektive | Finanziell, kurzfristig möglich | Breiter, inkl. soziale und ökologische Aspekte |

Laut VL: „viel diskutiertes Thema" – beide Sichtweisen sind nicht per se unvereinbar.

---

### Anwendung

Nennen Sie alle fünf Bilanzkennzahlen mit Formel und ordnen Sie sie in Liquiditäts- und Strukturkennzahlen ein.

?

**Liquiditätskennzahlen** (Fähigkeit, kurzfristige Verbindlichkeiten zu bedienen):

| Kennzahl | Formel |
|---|---|
| **Current ratio** | current assets / current liabilities |
| **Quick ratio** | (current assets − inventory) / current liabilities |
| **Cash ratio** | (cash + cash equivalents) / current liabilities |

**Strukturkennzahl:**

| Kennzahl | Formel |
|---|---|
| **Debt-equity ratio** | debt / shareholder's equity |

**Absolutbetragskennzahl:**

| Kennzahl | Formel |
|---|---|
| **Working capital** | current assets − current liabilities |

Merkhilfe: Current → Quick → Cash = immer strenger (Vorräte raus → nur noch Cash).

---

Nennen Sie alle GuV-Kennzahlen mit Formel.

?

| Kennzahl | Formel |
|---|---|
| **Net Profit Margin** | net income / total sales |
| **RoE** (Return on Equity) | net income / shareholder's equity |
| **RoA** (Return on Assets) | net income / total assets |
| **RoI** (Return on Investment) | net return of investment / cost of investment |
| **EBITDA / EBIT / EBT** | absolute Erfolgsgrößen aus der GuV-Kaskade |

Hinweis laut VL: Return-Ratios × 100 = Prozentangabe.

---

Nennen Sie die zwei Cashflow-Kennzahlen mit Formel und Aussage.

?

| Kennzahl | Formel | Aussage |
|---|---|---|
| **Cash Flow Margin Ratio** | CFO / revenue | Cash-Profitabilität: Wie viel operativer Cashflow pro Umsatz-Euro? |
| **Cash Flow Coverage Ratio** | CFO / debt | Schuldendienstfähigkeit: Wie gut deckt der operative Cashflow die Verschuldung? |

Beide nutzen **Cashflow aus operativer Tätigkeit (CFO)** als Zähler.
Beispiel: Coverage Ratio = 0,1 → CFO deckt nur 10 % der Schulden – kritisch.

---

Wie sind Bilanz, GuV und Kapitalflussrechnung miteinander verknüpft? Skizzieren Sie die Schnittstellen.

?

```
GuV (income statement)
  └─ Net Income ──────────────────────→ Startwert Kapitalflussrechnung
  └─ Net Income → Retained Earnings ──→ Eigenkapital in der Bilanz

Bilanz (balance sheet)
  └─ Veränderungen Forderungen, Verbindlichkeiten, Vorräte ──→ Adjustments im CFO
  └─ Cash-Endbestand ←─────────────────── Kapitalflussrechnung (Ende)

Kapitalflussrechnung
  └─ CFO + CFI + CFF = Δ Cash ──────→ Cash in der Bilanz (Stichtag)
```

Prüfungsrelevante Formel: Nur alle drei Instrumente zusammen geben ein vollständiges Bild – Bilanz zeigt Strukturen, GuV Profitabilität, Cashflow Liquidität.

---

Ein Krankenhaus kauft ein neues MRT-Gerät für 2 Mio. € per Bankkredit. Wie wirkt sich das auf Bilanz, GuV und Cashflow aus?

?

**Bilanz:**
- Aktiva: Sachanlagen ↑ +2 Mio. €
- Passiva: langfristige Verbindlichkeiten ↑ +2 Mio. €

**GuV (Folgeperioden):**
- Abschreibungen auf das Gerät ↓ senken EBIT und Net Income

**Kapitalflussrechnung:**
- CFI: Kauf von Sachanlagen → Abfluss −2 Mio. €
- CFF: Kreditaufnahme → Zufluss +2 Mio. €
- CFO: keine direkte Wirkung im Kaufjahr (Abschreibungen erscheinen als Add-back im CFO)

---

### Diskussion

Warum gilt der operative Cashflow (CFO) als „ehrlichere" Kennzahl als das Net Income der GuV?

?

- **Net Income** folgt dem Periodenprinzip – Erträge/Aufwendungen werden periodengerecht zugeordnet, unabhängig vom tatsächlichen Geldeingang. Abschreibungspolitik und Bewertungsspielräume (IFRS Fair Value) können das Ergebnis erheblich beeinflussen.
- **CFO** basiert auf tatsächlichen Zahlungsströmen – näher am realen Geldfluss, schwerer zu „gestalten".
- **Einschränkung** (aus Konzept-Note): Auch CFO kann durch Working-Capital-Management gesteuert werden (Forderungen verzögert eintreiben, Zahlungen aufschieben).

Fazit: CFO ist robuster, aber nicht manipulationssicher. Erst die Kombination aller drei Instrumente ergibt das vollständige Bild.

---

Warum gilt EBITDA als bevorzugte Kennzahl für Unternehmensvergleiche – und was kritisiert man daran?

?

**Argumente für EBITDA:**
- Neutralisiert Effekte aus unterschiedlicher Abschreibungspolitik (D&A), Zinsstruktur und Steuerregime.
- Macht Unternehmen mit verschiedener Kapitalstruktur vergleichbarer.
- Zeigt operativen Cash-nahen Ergebnisbeitrag.

**Kritik** (aus Konzept-Note):
- EBITDA blendet reale Investitionsbedarfe aus – ein Asset-intensives Krankenhaus braucht hohe Abschreibungen (und damit Reinvestitionen), die EBITDA ignoriert.
- Kann als Schönrechnerei wirken: ein Unternehmen mit negativem Net Income kann ein positives EBITDA ausweisen.
- [Ergänzung] Charlie Munger nannte EBITDA einmal „bullshit earnings" – nicht im PDF, aber bekannter Kontext.

---

Worin unterscheiden sich externes und internes Rechnungswesen?

?

| Aspekt | Externes Rechnungswesen | Internes Rechnungswesen |
|---|---|---|
| Adressat | Dritte: Investoren, Behörden, Banken, Börse | Management |
| Pflicht | Gesetzlich vorgeschrieben | Freiwillig, intern definiert |
| Standards | GAAP, IFRS, nationales Recht | Frei wählbar |
| Inhalt | Bilanz, GuV, Cashflow, Anhang | Kostenrechnung, Deckungsbeitrag, Break-even, Budgetierung |
| Zeithorizont | Rückblickend (abgeschlossene Periode) | Vergangenheit + Zukunft (Plan, Budget) |

Laut VL (Folie 44): Aus den Daten des externen Rechnungswesens werden für den internen Gebrauch berechnet: **Kosten, Preise, Deckungsbeitrag, Break-even-Punkt**.

---

Welche Vor- und Nachteile haben Eigen- vs. Fremdfinanzierung?

?

| Aspekt | Eigenfinanzierung | Fremdfinanzierung |
|---|---|---|
| Rückzahlungspflicht | Keine | Ja (Tilgung + Zinsen) |
| Einfluss Kapitalgeber | Verwässerung der Eigentumsrechte | Keine Eigentümerrechte, aber Covenants möglich |
| Kosten | Renditeanforderungen der Aktionäre (i. d. R. höher als Fremdkapitalzinsen) | Zinslast, steuerlich abziehbar |
| Risikoprofil | Niedriger für das Unternehmen (kein Insolvenzrisiko durch Zinsen) | Bonitätsrisiko, Verschuldungsgrad steigt |

Laut VL: Die Wahl bestimmt, ob Kapitalgeber **Eigentümer** (Aktionäre) oder **Gläubiger** (Kreditgeber) sind. [Ergänzung] Optimaler Kapitalmix → Stichwort WACC.

### Vergleich

Grenzen Sie Current ratio, Quick ratio und Cash ratio voneinander ab – wann ist welche aussagekräftiger?

?

Alle drei messen **Liquidität** (Fähigkeit, kurzfristige Verbindlichkeiten zu bedienen), unterscheiden sich aber im Grad der Konservativität:

| Kennzahl | Formel | Strenge | Sinn |
|---|---|---|---|
| **Current ratio** | current assets / current liabilities | niedrig | Breite Sicht: alle UV zählen |
| **Quick ratio** | (current assets − inventory) / current liabilities | mittel | Ohne Vorräte: nicht immer schnell liquidierbar |
| **Cash ratio** | (cash + cash equivalents) / current liabilities | hoch | Nur sofort verfügbares Geld |

Wann: Current ratio für allgemeine Liquiditätseinschätzung; Quick ratio wenn Vorräte nicht schnell verkaufbar (z. B. Krankenhaus-Medizintechnik); Cash ratio in Liquiditätskrisen oder für kurzfristige Zahlungsfähigkeit.

---

Vergleichen Sie RoE und RoA: Was messen sie, wo liegen die Unterschiede?

?

| Kennzahl | Formel | Bezugsgröße | Perspektive |
|---|---|---|---|
| **RoE** (Return on Equity) | net income / shareholder's equity | Eigenkapital | Aktionärsperspektive: Effizienz des eingesetzten Eigenkapitals |
| **RoA** (Return on Assets) | net income / total assets | Gesamtvermögen | Managementperspektive: Effizienz aller Ressourcen |

**Kritischer Unterschied**: Ein hoher RoE kann auch durch hohe Verschuldung entstehen (Leverage-Effekt) – mehr Fremdkapital → weniger Eigenkapital → höherer RoE bei gleichem Net Income. RoA ist deshalb „neutraler", weil er die Kapitalstruktur herausrechnet.

Aus GuV-Konzept-Note: „Kein einzelner Königsweg – je nach Frage die passende Kennzahl."

---

Können Shareholder Value und Stakeholder Value im Konflikt stehen? Zeigen Sie an Beispielen aus dem Gesundheitswesen.

?

**Konfliktbeispiele** (aus Konzept-Note):
- Investitionen in Mitarbeiter-Weiterbildung erhöhen Stakeholder Value, kosten kurzfristig Shareholder Value.
- Aggressive Kostenreduktion (z. B. weniger Pflegepersonal) erhöht kurzfristigen Shareholder Value, kann aber Patientensicherheit (Stakeholder) gefährden.
- Schließung einer defizitären Abteilung: Shareholder-rational, Stakeholder-schädlich (Versorgungslücke).

**Mögliche Vereinbarkeit**: Long-term Shareholder Value lässt sich oft mit Stakeholder Value vereinbaren – ein Krankenhaus mit hoher Patientenzufriedenheit und guter Mitarbeiterkultur erzielt langfristig bessere Ergebnisse.

Laut VL: Öffentlich-finanzierte Krankenhäuser sind primär Stakeholder-orientiert (Versorgungsauftrag); private Konzerne stehen zusätzlich unter Shareholder-Druck.

---

## Mögliche Anschlussfragen des Prüfers

- Welche Bilanzposition verändert sich, wenn ein Krankenhaus eine Immobilie kauft – und finanziert sie sich über Eigenkapital vs. Kredit?
- Welche Aussagekraft haben Bilanzanalyse-Kennzahlen für ein Non-Profit-Krankenhaus?
- Wie hängen Finanzmanagement und PDCA-Zyklus zusammen (laut VL)?
- Welche Finanzierungsmethoden sind in frühen Unternehmensphasen typisch?
- Warum reicht die Bilanz allein nicht für eine Unternehmensbeurteilung?
- Wie wirkt sich eine IFRS-Umstellung auf die Bilanzpolitik aus?
- Welche Schnittstelle hat Finanzmanagement zum IT-Management?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
