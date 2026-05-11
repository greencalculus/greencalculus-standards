# BS EN 15978 — Embodied Carbon in Buildings

| Field | Value |
|---|---|
| **Initiative** | European Committee for Standardization (CEN) — Whole Life Carbon Assessment of buildings |
| **Operative version** | EN 15978:2011 (adopted in UK as BS EN 15978:2011) |
| **Latest substantive update** | EN 15978-1 revision in advanced stages (expected publication 2025–2026); adds modules A0, B8, splits Module D |
| **Next mandatory date** | None mandatory at standard level; embedded in EU EPBD (recast) Annex III and UK / Mayor of London policy |
| **Administered by** | CEN/TC 350 — Sustainability of construction works; adopted nationally by BSI (UK) and equivalent national standards bodies |
| **GreenCalculus stack layer** | Layer 2 — Calculation (built environment) |
| **Last reviewed** | 2026-05-18 |

---

## What this standard does

BS EN 15978 — formally titled *Sustainability of construction works — Assessment of environmental performance of buildings — Calculation method* — is the European calculation framework for **whole life carbon assessment (WLCA)** of buildings. It defines the modules, system boundaries, and calculation rules for evaluating a building's environmental performance across its entire life cycle, from raw material extraction through construction, operation, refurbishment, and end-of-life treatment.

It is the *building-scale* counterpart to:

- **EN 15804** — the product-scale standard governing Environmental Product Declarations (EPDs) for individual construction materials
- **ISO 14040 / 14044** — the foundational LCA framework
- **[ISO 14067](../iso/14067-product-carbon-footprint.md)** — generic product carbon footprint methodology

Where EN 15804 tells a steel manufacturer how to calculate the cradle-to-gate carbon of a tonne of structural steel, EN 15978 tells the architect, engineer, or carbon consultant how to aggregate every product EPD (plus construction, operational, and end-of-life impacts) into a coherent whole-building number expressed as kg CO₂e per square metre per year (or equivalent functional unit).

## Why it matters for GreenCalculus

The built environment is responsible for roughly **40% of global GHG emissions** when operational *and* embodied carbon are counted. Embodied carbon — the emissions from extracting, manufacturing, transporting, installing, and disposing of building materials — accounts for an increasing share of a building's lifetime footprint as operational energy decarbonises. For a high-performing low-energy building, embodied carbon can exceed operational carbon over a 60-year reference study period.

BS EN 15978 is the framework that makes this calculation tractable and comparable. It is referenced by:

- The **EU Energy Performance of Buildings Directive (EPBD recast)** — Annex III mandates EN 15978-based whole-life GWP reporting for new buildings
- The **EU Level(s) framework** — Indicator 1.2 (Life cycle Global Warming Potential)
- The **EU Taxonomy** Technical Screening Criteria for buildings
- The **Mayor of London Whole Life-Cycle Carbon Assessment Policy SI 2** — requires BS EN 15978 + RICS Professional Standard
- **UK Government embodied carbon policy proposals** — Part Z amendment proposal references BS EN 15978 directly
- **Most national green building rating schemes** — BREEAM, LEED, DGNB, HQE, NABERS

For GreenCalculus, EN 15978 is the methodological backbone of every building-scale embodied carbon calculator. It provides the module structure (A1–A5, B1–B7, C1–C4, D) and aggregation rules that make calculator outputs comparable to BREEAM submissions, EU Taxonomy alignment claims, and Mayor of London WLCA filings.

## The life cycle modules — A, B, C, D structure

EN 15978 organises a building's life cycle into four stages, divided into 17 sub-modules. This module structure is the most-cited element of the standard:

### Stage A — Product and Construction (cradle-to-practical-completion)

| Module | Description |
|---|---|
| **A1** | Raw material supply |
| **A2** | Transport (raw materials to manufacturer) |
| **A3** | Manufacturing |
| **A4** | Transport (manufactured products to site) |
| **A5** | Construction / installation processes on site |

**A1–A3** combined is commonly called **"cradle-to-gate" or "upfront embodied carbon"** — the most-quoted figure in construction sustainability discussions. **A1–A5** is "upfront whole-of-construction" and is the figure many policy targets focus on.

### Stage B — Use (in-service life)

| Module | Description |
|---|---|
| **B1** | Use (emissions from installed products in service, e.g. refrigerant leaks from HVAC) |
| **B2** | Maintenance |
| **B3** | Repair |
| **B4** | Replacement |
| **B5** | Refurbishment |
| **B6** | Operational energy use |
| **B7** | Operational water use |

**B6** is operational carbon — historically the dominant share, but declining as electricity grids decarbonise. **B1–B5** is "in-use embodied carbon" (refurbishment cycles).

### Stage C — End of Life (decommissioning)

| Module | Description |
|---|---|
| **C1** | Deconstruction / demolition |
| **C2** | Transport (waste to processing) |
| **C3** | Waste processing |
| **C4** | Disposal |

### Stage D — Beyond the system boundary

| Module | Description |
|---|---|
| **D** | Benefits and loads from reuse, recovery, and recycling beyond the system boundary |

Module D is reported separately from modules A–C, not added to them. It captures the *avoided* emissions from materials that are recycled or reused into other product systems. This is methodologically important — and politically contested — because Module D credits can substantially reduce reported figures for materials with high recycling rates (steel, aluminium, copper).

The Mayor of London Policy SI 2 requires *all of A, B, C, and D* to be reported for compliance, with Module D shown transparently and separately rather than netted against modules A–C.

## The EN 15978-1 revision (in progress)

A substantive revision to EN 15978 is in advanced stages, expected to be published as final in 2025–2026. The revised standard is being numbered **EN 15978-1** (signalling a multi-part standard structure). Key changes:

- **New Module A0 — Preconstruction.** Captures emissions from pre-construction activities including land transformation, site clearance, demolition of existing structures, and preliminary earthworks. Closes a gap that has been widely flagged in the existing standard.
- **New Module B8 — Building-related users' activities not included in B1–B7.** Allows separate reporting of user-driven activities (occupant transportation to the building, occupant-related minor refurbishments, occupant-installed appliances) that the original B1–B7 structure didn't explicitly accommodate.
- **Module D split into D1 and D2.** D1 covers potential net benefits from product-system reuse / recovery / recycling (the current Module D scope). D2 is a new module covering broader societal or environmental net benefits. The split is intended to give clearer disclosure and prevent the previous Module D from being used as a catch-all.
- **Tighter alignment with EN 15804+A2** (the current EPD product standard).
- **Updated terminology** consistent with ISO 14064 and ISO 14067.

GreenCalculus building-scale calculators will track this revision. The current EN 15978:2011 module structure remains valid for compliance with EU EPBD, EU Taxonomy, and Mayor of London policies referring to "EN 15978" — these references will migrate to EN 15978-1 once it is final, typically with a transition period.

## How GreenCalculus implements EN 15978 alignment

**Module-disaggregated outputs.** Every building-scale calculator returns results broken down by module (A1–A3, A4, A5, B1–B5, B6, B7, C1–C4, D), with the modules clearly labelled. This matches the format required by BREEAM, the Mayor of London Policy SI 2, EU Taxonomy alignment statements, and the RICS Professional Standard.

**EPD-aware material inputs.** Where users have specific Environmental Product Declarations (EPDs) from manufacturers, GreenCalculus calculators accept the EPD values directly. Where they don't, the Master Brain falls back to generic background data from the Inventory of Carbon and Energy (ICE) database, ecoinvent-compatible factors, and EPD-derived industry averages — all clearly labelled by source.

**Reference study period.** The default reference study period is 60 years (BRE / RICS convention), with user override available. Functional units are expressed per square metre of gross internal area per year (kgCO₂e/m²/year) or per total over the study period, with both surfaced.

**Module D transparency.** Module D results are computed and displayed separately, never netted against modules A–C. This is critical for compliance with the Mayor of London policy and aligns with the EN 15978-1 revision direction.

**Cross-references to EN 15804 and ISO 14067.** Where a building-scale calculation uses product-level CFP data from EPDs, the calculator surfaces the underlying [EN 15804](https://standards.iteh.ai/catalog/standards/cen/c546e9c4-2c89-4d4a-9d3a-29c9c1f5d6e1/) and [ISO 14067](../iso/14067-product-carbon-footprint.md) lineage of those numbers.

## Related and complementary standards

EN 15978 sits within a dense family of construction-sector environmental standards:

| Standard | Scope | Relationship to EN 15978 |
|---|---|---|
| **EN 15804** | Product-level EPDs for construction products | Provides the underlying product data EN 15978 aggregates |
| **EN 15643** | General framework for sustainability assessment of buildings | The parent framework — environmental, social, economic; EN 15978 is the environmental calculation part |
| **EN 17472** | Civil engineering works (bridges, infrastructure) | Sister standard for non-building structures |
| **ISO 21930** | Sustainability in buildings — environmental declarations of building products (international counterpart to EN 15804) |
| **ISO 21931-1** | Framework for environmental performance assessment of buildings (international counterpart to EN 15978) |
| **RICS Professional Standard** (UK) | UK practitioner methodology built on BS EN 15978 | Adds UK-specific reference values, factors, and reporting conventions |
| **[ISO 14067](../iso/14067-product-carbon-footprint.md)** | Generic product carbon footprint | Methodologically aligned for materials; building-scale aggregation falls to EN 15978 |
| **[ISO 14040 / 14044](https://greencalculus.com/standards/iso-14040-14044-lca/)** | Foundational LCA methodology | EN 15978 is an application-specific extension |

## Important caveats

A few points worth flagging:

**1. EN 15978 is not currently a binding standard on its own.** It is referenced by regulations (EU EPBD, EU Taxonomy, Mayor of London policy, French RE2020, Dutch MPG, Danish BR18 § 297, Finnish Climate Act) but the binding requirements come from the regulation that *cites* EN 15978, not from EN 15978 itself.

**2. Module-coverage inconsistency is widespread.** Many national policies require only A1–A5 (upfront embodied carbon), or only A1–A3, while the standard itself mandates cradle-to-grave. Comparisons between projects in different jurisdictions are only meaningful if the same modules are covered. GreenCalculus calculator outputs make this explicit.

**3. The reference study period matters a lot.** Embodied carbon expressed per m²/year depends on the assumed building lifetime. A 30-year office and a 100-year cultural building will produce very different annualised figures from the same total. The RICS / BRE default of 60 years is widely used but not universal.

**4. EPD data quality varies enormously.** ISO 14067-compliant EPDs from major manufacturers are auditable and well-documented; smaller manufacturers may rely on generic data or product-specific assumptions that are not fully traceable. EN 15978-compliant assessments should disclose the EPD sources for each material and their data quality rating.

**5. GreenCalculus is not third-party WLCA verification.** Building assessments submitted for BREEAM, the EU Taxonomy, the Mayor of London Policy SI 2, or French RE2020 typically require sign-off by a qualified WLCA assessor. GreenCalculus produces the calculation; verification is a separate engagement.

## Calculators on greencalculus.com that use this standard

This list will be populated as each calculator's EN 15978 alignment is verified. Affected categories include:

- All whole life carbon assessment (WLCA) calculators for buildings
- Upfront embodied carbon (A1–A5) calculators for new construction
- Renovation / refurbishment embodied carbon calculators (B5)
- Operational + embodied carbon comparison calculators
- Module D recovery / recycling benefit calculators
- Reference study period analysis tools
- EU Taxonomy alignment indicator 1.2 calculators
- Building material embodied carbon calculators (cross-references EN 15804 EPDs and the ICE database)

## Official sources

- [BS EN 15978:2011 — BSI Shop](https://shop.bsigroup.com/products/sustainability-of-construction-works-assessment-of-environmental-performance-of-buildings-calculation-method)
- [CEN/TC 350 — Sustainability of construction works](https://standards.cencenelec.eu/dyn/www/f?p=205:7:0::::FSP_ORG_ID:481830)
- [EU Level(s) framework — European Commission](https://environment.ec.europa.eu/topics/circular-economy/levels_en)
- [Energy Performance of Buildings Directive (recast)](https://eur-lex.europa.eu/eli/dir/2024/1275/oj)
- [RICS Whole Life Carbon Assessment Professional Standard](https://www.rics.org/profession-standards/rics-standards-and-guidance/sector-standards/building-surveying-standards/whole-life-carbon-assessment)
- [Mayor of London — Whole Life-Cycle Carbon Assessment Guidance](https://www.london.gov.uk/programmes-strategies/planning/implementing-london-plan/london-plan-guidance/whole-life-cycle-carbon-assessment-guidance)
- [ECOS — Calculate Embodied Carbon Recommendations (Feb 2025)](https://ecostandard.org/news_events/calculate-embodied-carbon-lets-do-it-right/)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/bs-en-15978-embodied-carbon-buildings/](https://greencalculus.com/standards/bs-en-15978-embodied-carbon-buildings/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> European Committee for Standardization (2011). *EN 15978:2011 — Sustainability of construction works — Assessment of environmental performance of buildings — Calculation method.* CEN, Brussels.

For the UK national adoption:

> British Standards Institution (2011). *BS EN 15978:2011 — Sustainability of construction works — Assessment of environmental performance of buildings — Calculation method.* BSI, London.

For the revision in progress:

> European Committee for Standardization (forthcoming, 2025–2026). *EN 15978-1 — Sustainability of construction works — Assessment of environmental performance of buildings — Part 1: Calculation method.* CEN, Brussels.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-18
