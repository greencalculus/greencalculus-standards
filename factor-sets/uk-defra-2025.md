# UK DEFRA / DESNZ GHG Conversion Factors — 2025 v1

| Field | Value |
|---|---|
| **Initiative** | UK Government — Department for Energy Security and Net Zero (DESNZ), in partnership with the Department for Environment, Food and Rural Affairs (DEFRA) |
| **Operative version** | **2025 v1** — published June 2025; minor errata patches issued through Q3 2025 |
| **Latest substantive update** | June 2025 — annual refresh covering grid factors, fuels, transport, water, waste, and refrigerants; aligned with the UK national inventory cycle |
| **Next mandatory date** | **2026 set due Q3 2026** — annual refresh expected June–September 2026 |
| **Administered by** | DESNZ (lead from 2023 onward, having absorbed the climate functions of the former BEIS) with DEFRA retaining policy lead for non-energy emission factors |
| **GreenCalculus stack layer** | Layer 3 — Factor data (UK / English / Welsh / Scottish / NI primary factor set) |
| **Last reviewed** | 2026-05-25 |

---

## What this dataset does

The UK Government's annual *Greenhouse Gas Conversion Factors for Company Reporting* is the **canonical UK-specific emission factor set for corporate carbon accounting**. Published every year since 2008 (originally by DEFRA, then BEIS, now DESNZ), it provides emission factors that UK companies are expected — and in some cases legally required — to use for their statutory and voluntary GHG disclosures.

The dataset covers:

| Category | Examples |
|---|---|
| **Fuels (stationary and mobile)** | Natural gas, LPG, diesel, petrol, gas oil, heavy fuel oil, kerosene, coal, biofuels (biodiesel, bioethanol, biomethane), aviation fuels |
| **Electricity** | UK grid (location-based), historical and projected; transmission & distribution losses; well-to-tank fuel components |
| **Heat & steam** | Distributed heat networks, on-site heat |
| **Transport** | Passenger cars (by fuel and size), motorbikes, vans, HGVs (by weight class and Euro standard), buses, rail (UK national and London Underground), domestic flights, international flights (short-, medium-, long-haul; economy/business/first), ferries, taxis |
| **Business travel** | Hotel stays (UK and major international destinations), public transport |
| **Freighting goods** | Road, rail, sea, and air freight — by mode and weight |
| **Water** | Water supply, treatment |
| **Waste** | Recycling, landfill, incineration, composting, anaerobic digestion — by waste type |
| **Refrigerants** | HFC, PFC, and SF₆ — operational basis (with [EU 2024/573](../eu/f-gas-regulation.md) reference for context, though UK rules diverge post-Brexit) |
| **Material use** | Selected materials (paper, cardboard, plastics, glass, metals) — typically for waste/end-of-life calculations |

The factors are published as an Excel workbook accompanied by a methodology document, both freely downloadable from gov.uk.

## Why it matters for GreenCalculus

For UK-based or UK-operating users, the DEFRA/DESNZ conversion factors are the **default emission factor set** that most calculators on the GreenCalculus platform reach for. The reasons are structural:

1. **Regulatory alignment.** UK Streamlined Energy and Carbon Reporting (SECR), the Energy Savings Opportunity Scheme (ESOS), and other UK statutory regimes either explicitly reference DEFRA factors or treat them as the de facto compliance standard.
2. **Annual currency.** Unlike many international factor sets that update on multi-year cycles, the DEFRA/DESNZ refresh is annual — typically published in June each year. This is the most current vintage for any reporting year.
3. **Coverage and granularity.** The dataset covers more activity types than any other publicly available UK-aligned source. Granularity (Euro standard for HGVs, flight class, hotel destination) is unusually fine.
4. **Methodological transparency.** The accompanying methodology document is detailed, auditable, and aligned with the [GHG Protocol Corporate Standard](../ghg-protocol/corporate-standard.md) and underlying [IPCC 2006 Guidelines + 2019 Refinement](../ipcc/2006-guidelines-national-inventories.md).
5. **AR6 GWP basis (from 2024 onward).** The 2024 and 2025 sets adopted [AR6 GWP-100](../ipcc/ar6-gwp-100.md), aligning the factor set with the [GHG Protocol Corporate Standard 2026 revision](../ghg-protocol/corporate-standard.md) and current scientific consensus. Prior years used AR5 or AR4 — GreenCalculus tags vintages so users reporting prior years can use the matching vintage factor.

For non-UK users, DEFRA factors are still relevant: they are widely used as a fallback for European or English-speaking markets where a country-specific equivalent does not exist, and several international corporate reporters use DEFRA as a global default for legacy reasons.

## Structure of the 2025 v1 release

The 2025 v1 set comprises approximately 6,000 individual emission factor rows organised into sheets within the Excel workbook. Headline structure:

| Sheet group | Typical content |
|---|---|
| **Fuels** | kg CO₂e per kWh, per litre, per kg, per tonne — for ~40 fuel types |
| **Bioenergy** | Combustion + supply-chain factors for solid, liquid, and gaseous biofuels |
| **UK electricity** | Location-based grid factor (consumption basis); generation-basis; T&D losses; well-to-tank |
| **UK electricity for EVs** | Distinct factor with charging-loss adjustment |
| **Heat and steam** | Heat-network and on-site factors |
| **Transport — passenger** | Cars by fuel × size; motorbike by size; bus, rail, taxi, etc. |
| **Transport — freight** | Road, rail, sea, air freight by mode and weight |
| **Business travel** | Air (short/medium/long, class), hotel stays |
| **Water** | Supply and treatment |
| **Waste** | By waste type × disposal route |
| **Refrigerants** | By gas, GWP, leak rate assumptions |
| **Material use** | Selected materials, primarily for waste/EoL |
| **WTT vs combustion** | Each fuel split into well-to-tank (upstream supply) and combustion components |
| **Outside scope** | Activities outside GHG Protocol scopes (e.g. biogenic CO₂) — reported separately |

The well-to-tank (WTT) split is methodologically important: it allows users to calculate either combustion-only (Scope 1) emissions or full-fuel-cycle (Scope 1 + Scope 3 Cat. 3) emissions consistently, with no double-counting.

## What changed in the 2025 v1 set vs the 2024 set

The 2025 v1 release continued the trend toward harder grid decarbonisation and methodology cleanups:

| Area | Direction of change |
|---|---|
| **UK grid factor** | Decreased again — UK grid intensity has fallen consistently year-on-year as coal exits and offshore wind expands |
| **Bioenergy** | Tightened sustainability conditions; ineligible biomass routes more explicitly flagged |
| **Aviation** | Updated radiative-forcing index (RFI) treatment; non-CO₂ effects more transparently reported |
| **Refrigerants** | AR6 GWP-100 fully applied (was partial in 2024); R32 and HFO blends gained additional granularity |
| **EV charging** | Distinct factor with explicit charging-loss assumption; aligns better with real-world EV operations |
| **Methodology document** | Restructured for clarity; sources and uncertainty better documented |

## Sub-national disaggregation

A common question: "Is there an England-only, Wales-only, Scotland-only factor?" For most factor types, the answer is *no* — the UK is treated as a single market and most factors apply across all four nations.

Exceptions:

- **Electricity** is published as a UK-wide consumption factor. Sub-national grid intensities exist (Scotland is materially cleaner than the UK average due to high wind and hydro share; Northern Ireland is connected to the Single Electricity Market with Ireland) — but these are *not* in the DEFRA/DESNZ headline dataset. National Grid ESO and the Scottish Government publish supplementary sub-national factors that GreenCalculus surfaces where users need them.
- **Waste** factors vary slightly across the four nations due to different waste-management infrastructure (Scotland's higher recycling rate, NI's distinct landfill regime). The DEFRA dataset is England-weighted; GreenCalculus tags sub-national variants where they materially differ.

## Relationship with the EU and international datasets

The DEFRA/DESNZ factors are methodologically aligned with — but not identical to — major international counterparts:

| Counterpart | Relationship |
|---|---|
| [IPCC 2006 Guidelines + 2019 Refinement](../ipcc/2006-guidelines-national-inventories.md) | DEFRA factors are UK national-inventory implementations of IPCC methodology |
| US EPA emission factors | Different national grid, fuel specifications; methodologically parallel |
| EPA eGRID | US-specific subregional grid; DEFRA UK-aggregate equivalent |
| IEA Global Energy Review | International grid intensities; DEFRA used for UK consumption |
| Inventory of Carbon and Energy (ICE) v3.0 | Embodied carbon factors — complementary, not overlapping |
| ecoinvent / GaBi | Multi-impact LCA databases — methodologically [14040/14044](../iso/14040-14044-lca.md) -aligned |

For multinational corporate reporters operating in UK and US (or EU) jurisdictions, the DEFRA UK factors and EPA US factors are typically used in parallel, applied per the geographic location of the activity.

## How GreenCalculus implements the DEFRA / DESNZ factors

**Default factor for UK activities.** Calculators detecting UK-located activity (UK postcodes, GB/UK-flagged inputs, GBP currency hints) default to DEFRA/DESNZ factors for the relevant vintage.

**Year-vintaged factor selection.** Every Master Brain factor entry carries its DEFRA/DESNZ release year (2023, 2024, 2025). When a user reports for a specific year, the calculator uses the factor vintage current to that reporting year — the methodologically correct choice for inventory work.

**WTT and combustion separation.** Calculators surface combustion-only (Scope 1) and well-to-tank (Scope 3 Cat. 3) components separately, consistent with the DEFRA/DESNZ workbook structure.

**AR6 GWP basis from 2024 onward.** The Master Brain applies AR6 GWP-100 for all CO₂e conversions involving non-CO₂ gases (CH₄, N₂O, refrigerants) consistent with the DEFRA 2024 / 2025 sets. Prior-vintage factors retain their original AR4/AR5 basis where the user is reporting against a prior year.

**Outside-scope and biogenic CO₂ separation.** Following DEFRA convention, biogenic CO₂ from bioenergy is reported separately ("outside scopes") rather than as a Scope 1 emission, in line with the [GHG Protocol](../ghg-protocol/corporate-standard.md) and [ISO 14064-1](../iso/14064-1-organisation-ghg-quantification.md).

**Audit trail.** Every calculator output that uses a DEFRA factor surfaces the source ("DEFRA/DESNZ 2025 v1"), the factor row reference, and the methodological category, supporting verification.

## Regulatory contexts where DEFRA factors are referenced

The DEFRA/DESNZ conversion factors are explicitly or implicitly referenced in:

| Regime | Reference |
|---|---|
| **UK Streamlined Energy and Carbon Reporting (SECR)** | Mandatory for large UK companies; DEFRA factors are the default and most commonly used |
| **Energy Savings Opportunity Scheme (ESOS)** | Phase 3 reporting (2024 cycle); DEFRA factors are the reference for energy-to-CO₂ conversions |
| **UK Companies (Strategic Report) Climate-related Financial Disclosure Regulations 2022** | TCFD-aligned UK disclosure; DEFRA factors used for the Metrics & Targets pillar |
| **UK Emissions Trading Scheme (UK ETS)** | Operates with EU-derived monitoring rules; UK national inventory factors used in compliance calculations |
| **Public Sector Carbon Reporting** | UK Government departments use DEFRA factors for the annual State of the Estate reporting |
| **Voluntary CDP / SBTi reporting** | DEFRA factors widely used by UK-domiciled reporters |

## Important caveats

A few points worth flagging:

**1. The factor set is calendar-year-vintaged.** A factor labelled "2025 v1" is intended for reporting *activity that occurred in 2025*. Using a 2025 factor against 2024 activity is a vintage mismatch and may be flagged by an auditor under [ISO 14064-1](../iso/14064-1-organisation-ghg-quantification.md). GreenCalculus enforces vintage-match where the reporting year is specified.

**2. The UK grid factor is consumption-basis by default.** This includes generation, transmission, and distribution losses, but reflects the location-based method per the [GHG Protocol Scope 2 Guidance](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/). For market-based reporting, supplier-specific or contractual factors must be substituted.

**3. AR6 GWPs are applied from 2024 onward.** Prior-year DEFRA sets used AR5 (2013–2023 vintage range) or earlier. Companies recasting prior-year inventories to AR6 should do so explicitly and disclose the recasting methodology — see [AR6 GWP mapping](../ipcc/ar6-gwp-100.md) for detail.

**4. UK-specific factors don't always extrapolate.** The DEFRA dataset is calibrated for UK fuels, UK vehicle fleets, UK grid, UK waste streams. Using DEFRA factors for non-UK activities (e.g. US road freight, EU electricity) is methodologically inappropriate. GreenCalculus selects geographically-matched factor sets automatically.

**5. Biofuels and bioenergy are sensitive to sustainability conditions.** The DEFRA factors for biofuels assume the biofuel meets UK and EU sustainability criteria (RTFO compliance for road fuels, etc.). Where biofuel sustainability is not verified, the relevant emission factor may not apply.

**6. GreenCalculus is not assurance.** Calculator outputs using DEFRA factors are methodologically aligned but do not discharge any third-party assurance requirement. Companies pursuing SECR limited assurance or ISO 14064-1 verification must engage an accredited body.

## Calculators on greencalculus.com that use this dataset

Every calculator targeting UK activity uses DEFRA/DESNZ factors as the default. Notable categories:

- All Scope 1 stationary combustion calculators (UK fuels)
- All Scope 1 mobile combustion calculators (UK fleet, road, rail)
- All Scope 2 electricity calculators (UK grid, location-based)
- Well-to-tank (Scope 3 Cat. 3) fuel-and-energy-related-activities calculators
- All UK business travel calculators (air, rail, taxi, hotel)
- All UK freighting calculators (road, rail, sea, air)
- UK water and wastewater calculators
- UK waste-disposal calculators (recycling, landfill, incineration)
- UK refrigerant calculators (with vintage-matched GWP basis)
- SECR-aligned reporting bundles

## Official sources

- [UK Government GHG Conversion Factors for Company Reporting (gov.uk)](https://www.gov.uk/government/collections/government-conversion-factors-for-company-reporting)
- [DESNZ — Department for Energy Security and Net Zero](https://www.gov.uk/government/organisations/department-for-energy-security-and-net-zero)
- [SECR statutory guidance](https://www.gov.uk/government/publications/environmental-reporting-guidelines-including-mandatory-greenhouse-gas-emissions-reporting-guidance)
- [UK National Atmospheric Emissions Inventory (NAEI)](https://naei.beis.gov.uk/) — upstream national inventory source
- [Companies (Strategic Report) (Climate-related Financial Disclosure) Regulations 2022](https://www.legislation.gov.uk/uksi/2022/31)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this dataset lives at:

**[greencalculus.com/standards/uk-defra-emission-factors/](https://greencalculus.com/standards/uk-defra-emission-factors/)**

That page is the canonical citation target for this dataset mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> Department for Energy Security and Net Zero / Department for Environment, Food and Rural Affairs (2025). *UK Government Greenhouse Gas Conversion Factors for Company Reporting, 2025 v1.* DESNZ / DEFRA, London, June 2025.

For the methodology paper accompanying the dataset:

> Department for Energy Security and Net Zero (2025). *Government Greenhouse Gas Conversion Factors for Company Reporting — Methodology Paper, 2025 v1.* DESNZ, London.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-25
