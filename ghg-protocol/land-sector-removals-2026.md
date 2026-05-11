# GHG Protocol Land Sector and Removals Standard

| Field | Value |
|---|---|
| **Initiative** | GHG Protocol (WRI / WBCSD) |
| **Operative version** | Land Sector and Removals Standard v1.0 |
| **Latest substantive update** | Published 30 January 2026 |
| **Next mandatory date** | Effective 1 January 2027 |
| **Administered by** | World Resources Institute (WRI) and World Business Council for Sustainable Development (WBCSD) |
| **GreenCalculus stack layer** | Layer 2 — Calculation |
| **Last reviewed** | 2026-05-13 |

---

## What this standard does

The Land Sector and Removals Standard (LSR Standard, also sometimes abbreviated LSRS) is **the first GHG Protocol standard to provide comprehensive accounting requirements for land-based emissions and carbon dioxide removals**. Published 30 January 2026 after a five-year development process involving more than 300 external reviewers, it closes a long-standing gap in corporate carbon accounting: how to consistently quantify the climate impact of agricultural land management, land use change, and CO₂ removals — both biological (soils, biomass) and technological (direct air capture, bioenergy with carbon capture).

It is a **supplement** to the existing [GHG Protocol Corporate Standard](./corporate-standard.md) and [Scope 3 Standard](./scope-3-standard.md), not a replacement. Companies that report under those standards and have material land-sector activities must apply the LSR Standard for those activities starting **1 January 2027**.

## Why it matters for GreenCalculus

Agriculture and land use change account for roughly **a quarter of global greenhouse gas emissions**. For companies in food, agriculture, fiber, forestry-adjacent industries, apparel, consumer goods, mining rehabilitation, and bioenergy, land-sector emissions can dominate Scope 1 or Scope 3 footprints. Before the LSR Standard, the methodology was fragmented across draft guidance, sector initiatives (SBTi FLAG), and national inventory rules.

The LSR Standard is also the first authoritative framework for reporting **carbon dioxide removals** in a corporate GHG inventory. This includes biological removals (afforestation, soil carbon, perennial cropping) and technological removals with geologic storage (DAC, BECCS, mineralisation). Without a standard, removals reporting was either ignored or claimed loosely; the LSR Standard now defines what is allowed, when, and under which integrity safeguards.

GreenCalculus calculators in agriculture, land use, and removals categories are being aligned to the LSR Standard ahead of its effective date.

## Who it applies to

The LSR Standard applies to any company that:

- **Owns or controls land** with significant GHG emissions or removals (direct activities → Scope 1)
- **Purchases or sells products produced on agricultural land** in its value chain (indirect activities → Scope 3)
- **Chooses to report CO₂ removals** in its inventory — biological or technological — even if otherwise unconnected to the land sector
- **Chooses to report CO₂ capture with geologic storage** (e.g. DAC, CCS-equipped industrial processes)

The third and fourth categories are important: a tech company with no land-sector exposure but a DAC offtake agreement would apply the LSR Standard to that removal reporting.

## What's in scope and what's out

### In scope (v1.0)

| Category | Type | Scope mapping |
|---|---|---|
| Land use change emissions | Direct (Scope 1) or indirect (Scope 3) | Per organisational boundary |
| Land management emissions (cropping, livestock, soils) | Direct (Scope 1) or indirect (Scope 3) | Per organisational boundary |
| Biological CO₂ removals (afforestation, soil C, agroforestry) | Optional reporting | Direct or indirect |
| Technological CO₂ removals (DAC, BECCS, mineralisation) | Optional reporting | Direct or indirect |
| CO₂ capture with geologic storage | Optional reporting | Direct |
| Product carbon storage (HWPs, biochar in soil, biogenic in long-life products) | Optional reporting | Per traceability |

### Out of scope (v1.0)

- **Forest carbon accounting** — explicitly deferred from v1.0. The GHG Protocol Steering Committee decided forestry would not feature in this version to avoid delaying the wider standard. A separate Request for Information will inform a future update.
- **Proximate and adjacent non-productive lands** in Scope 3 — these *may* be included, but implementation detail was not settled in v1.0 and is expected to be clarified in the Q2 2026 Guidance document.

## Key methodological provisions

### Traceability tiers for Scope 3 removals

The LSR Standard requires **physical traceability** for Scope 3 removals. Companies must trace removals to at least one of:

1. **Sourcing region** — the geographic region from which the commodity is sourced
2. **Land management unit** — the farm or operational unit
3. **Harvested area** — the specific land where the harvest occurred

Global average assumptions are explicitly **not sufficient** for Scope 3 removals reporting. This is a significant tightening compared to the 2022 draft guidance, which left traceability open.

### Selective inclusion is prohibited

Companies cannot selectively include beneficial removals while excluding adjacent emitting land. This prevents inflated climate-benefit claims when supply chain traceability is weak.

### Permanence safeguards

For removals to count, the standard requires:

- A reserve approach (buffer pool) to insure against reversal from disturbances or natural disasters
- Disclosure of monitoring methods and reversal handling
- Time-bounded reporting of permanence

This brings corporate GHG inventories closer in line with the integrity standards used in voluntary carbon markets.

### Optional dual inventory reporting

Companies may choose to report **two parallel inventories**:

1. **Physical GHG inventory** — direct measurement, excluding any credits issued or retired
2. **Adjusted inventory** — physical inventory adjusted for credits issued from direct operations and/or value chain activities

This separation allows transparent disclosure for stakeholders who want to see what's happening in the physical world versus what's been monetised through removals issuance.

### Land use change emissions

Land use change (LUC) emissions — typically from conversion of forest, peatland, or grassland to cropping — are required where material. The standard provides accounting periods and amortisation rules consistent with IPCC inventory guidelines.

## How GreenCalculus implements this standard

The LSR Standard takes effect **1 January 2027**. GreenCalculus is aligning the Master Brain data layer (§11 agriculture, §14 removals) and relevant calculators in three phases:

**Phase 1 (now → Q3 2026).** Tag all existing agriculture and land-sector calculators with LSR Standard categories and traceability requirements. No calculation engine changes; metadata only.

**Phase 2 (Q3 2026 → Q1 2027).** Incorporate the LSR Guidance (expected Q2 2026) into worked examples and FAQ content. Add traceability-tier input fields to Scope 3 agricultural calculators.

**Phase 3 (1 January 2027 effective date).** Surface LSR-aligned outputs as the default for affected calculators. Make traceability-tier disclosure visible on all Scope 3 removals calculations.

The Master Brain already maintains separate `fossil` vs `biogenic` methane and N₂O classifications, which the LSR Standard relies on. The structural foundation is therefore in place; the work is calculator-level surfacing and reporting layout.

## Disclosure framework alignment — important caveats

A point widely missed in summary coverage:

- **CSRD / ESRS E1 does not currently reference the LSR Standard.** Companies preparing CSRD disclosures are not required to apply the LSR Standard for ESRS conformance, although they may use it as a useful methodology.
- **IFRS S2 / ISSB does not currently reference the LSR Standard.** Same position.
- **SBTi FLAG targets** are most directly affected. Companies submitting FLAG targets for validation will be expected to align with the LSR Standard, and companies with existing FLAG targets will need to update their inventories to LSR-compliant methodology on their next mandatory five-year review.

If GreenCalculus surfaces an LSR-aligned figure, it does not automatically discharge a CSRD or IFRS S2 disclosure obligation. The relevant disclosure regime mapping remains the user's responsibility, and our [CSRD / ESRS E1 mapping](../eu/csrd-esrs-e1.md) covers this in detail.

## The Q2 2026 Guidance document

The GHG Protocol committed at publication to release an accompanying **Land Sector and Removals Guidance** document in Q2 2026 (April–June 2026). This guidance is expected to include:

- Worked calculation examples
- Case studies by sub-sector (food, fiber, bioenergy, forestry-adjacent)
- Clarification on proximate/adjacent non-productive lands in Scope 3
- Detailed allocation rules for shared land or shared infrastructure
- MRV expectations (monitoring, reporting, verification)

Until the Guidance is published, certain implementation details — particularly around proximate-land Scope 3 inclusion and book-and-claim treatment of land-based removals — remain open. GreenCalculus will update its mapping when the Guidance becomes available.

## Future expansion

The GHG Protocol has flagged two areas for future LSR Standard revisions:

1. **Forest carbon accounting** — currently deferred. A Request for Information will gather stakeholder input. A revised LSR Standard including forestry "may take considerable time" per the GHG Protocol's own communication.
2. **Actions and Markets Instruments** — a parallel workstream is examining how book-and-claim and related mechanisms might be used in inventory accounting. Outcomes will be folded into LSR Standard revisions.

## Calculators on greencalculus.com that use this standard

This list will be populated as each calculator's LSR alignment is verified. Affected categories include:

- All agriculture-sector Scope 1 calculators (livestock, fertiliser, rice cultivation, manure management)
- All land use change calculators (deforestation, conversion of grassland or peatland)
- All Scope 3 Category 1 calculators where the purchased good is agricultural
- Soil carbon and afforestation removals calculators (optional reporting)
- Direct air capture and BECCS removals calculators (optional reporting)

Forestry-specific calculators are excluded pending the future LSR revision incorporating forest carbon accounting.

## Official sources

- [LSR Standard — official page](https://ghgprotocol.org/land-sector-and-removals-standard)
- [LSR Standard: What You Need to Know — GHG Protocol blog](https://ghgprotocol.org/blog/land-sector-and-removals-standard-what-you-need-know)
- [Save the Date announcement (October 2025)](https://ghgprotocol.org/blog/save-date-land-sector-and-removals-standard)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/ghg-protocol-land-sector-removals-2026/](https://greencalculus.com/standards/ghg-protocol-land-sector-removals-2026/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> World Resources Institute and World Business Council for Sustainable Development (2026). *GHG Protocol Land Sector and Removals Standard v1.0.* WRI/WBCSD. Published 30 January 2026; effective 1 January 2027.

For the executive summary:

> GHG Protocol (2026). *Land Sector and Removals Standard — Executive Summary.* WRI/WBCSD, January 2026.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-13
