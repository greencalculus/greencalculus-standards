# IPCC 2006 Guidelines for National Greenhouse Gas Inventories

| Field | Value |
|---|---|
| **Initiative** | IPCC Task Force on National Greenhouse Gas Inventories (TFI) |
| **Operative version** | 2006 IPCC Guidelines, augmented by the **2019 Refinement** |
| **Latest substantive update** | 2019 Refinement to the 2006 IPCC Guidelines (May 2019) — methodological updates across all five volumes |
| **Next mandatory date** | None — these guidelines are mandatory under the UNFCCC Enhanced Transparency Framework (ETF) from the first Biennial Transparency Reports (BTRs) due 31 December 2024 |
| **Administered by** | Intergovernmental Panel on Climate Change (IPCC), via the TFI Bureau and the Technical Support Unit hosted at the Institute for Global Environmental Strategies (IGES), Japan |
| **GreenCalculus stack layer** | Layer 2 — Calculation (sectoral methodology) |
| **Last reviewed** | 2026-05-25 |

---

## What this standard does

The 2006 IPCC Guidelines for National Greenhouse Gas Inventories — formally adopted at the IPCC Plenary in April 2006 — are the global methodological reference for **how countries compile and report their national greenhouse gas inventories under the United Nations Framework Convention on Climate Change (UNFCCC)**. They define, sector by sector and gas by gas, the activity data, emission factors, calculation tiers, and quality-control procedures that produce a country's annual emissions total.

The 2019 Refinement, published in May 2019, did not replace the 2006 Guidelines — it supplemented them. Where the 2019 Refinement provides updated default emission factors or new methodological elaboration (notably for fugitive coal methane, F-gases, and afforestation/reforestation), countries are expected to use the refined values; the underlying 2006 structure remains in force.

The guidelines are organised into five volumes:

| Volume | Sector |
|---|---|
| **Volume 1** | General Guidance and Reporting |
| **Volume 2** | Energy |
| **Volume 3** | Industrial Processes and Product Use (IPPU) |
| **Volume 4** | Agriculture, Forestry and Other Land Use (AFOLU) |
| **Volume 5** | Waste |

Each volume specifies methodologies at three tiers of increasing complexity — Tier 1 (default emission factors and simple activity-data approaches), Tier 2 (country-specific factors), and Tier 3 (process models and direct measurement). Countries select the appropriate tier per source category based on whether the category is a *key category* contributing significantly to total emissions or trend.

## Why it matters for GreenCalculus

The 2006 IPCC Guidelines are the **upstream methodological source for almost every national-level emission factor a corporate inventory will ever touch**. When a GreenCalculus calculator uses a default emission factor for diesel combustion, fugitive methane from coal mining, N₂O from synthetic fertiliser, or CH₄ from solid waste decomposition, that value almost certainly traces back — directly or via a national-inventory cascade — to the 2006 Guidelines or the 2019 Refinement.

The guidelines matter to GreenCalculus in three direct ways:

1. **Default emission factors.** The Master Brain data layer's Tier 1 emission factors for stationary combustion, mobile combustion, fugitive emissions, agricultural soils, livestock enteric fermentation, manure management, solid waste disposal, and wastewater treatment are sourced from the 2006 Guidelines (with 2019 Refinement updates applied where relevant).
2. **Methodological hierarchy.** Where a calculator allows users to substitute country-specific or facility-specific factors (Tier 2 / Tier 3), the data hierarchy is structured per Volume 1 Chapter 2 of the 2006 Guidelines: prefer facility-measured → country-specific → IPCC default.
3. **Compatibility with national reporting.** Companies operating in jurisdictions where national-inventory factors are referenced in corporate disclosure rules (notably the UK's [DEFRA conversion factors](../factor-sets/uk-defra-2025.md), which derive heavily from the 2006 Guidelines + 2019 Refinement) can rely on GreenCalculus outputs being methodologically consistent with the underlying national inventory.

## The tier structure — and why it matters for corporate calculators

A single source category (say, diesel-fuelled stationary combustion) can be calculated at any of three tiers:

| Tier | Approach | Typical use in GreenCalculus |
|---|---|---|
| **Tier 1** | Default emission factor from the IPCC Guidelines × activity data | Default in most calculators where no facility-specific data is available |
| **Tier 2** | Country-specific or technology-specific emission factor × activity data | Used where DEFRA, EPA, or equivalent national factors are available |
| **Tier 3** | Process model, direct measurement, or facility-specific stoichiometric calculation | Available in advanced calculators (e.g. mass-balance for landfill CH₄, model-based N₂O for fertilised soils) |

Corporate inventories using IPCC defaults are explicitly Tier 1. This is methodologically sound for most facility-level reporting where higher-tier data is unavailable, but the limitation should be acknowledged in disclosure documentation.

## Key methodological elements GreenCalculus relies on

**Energy (Volume 2).** Default emission factors for stationary combustion (Chapter 2), mobile combustion (Chapter 3), and fugitive emissions from coal mining and oil & gas systems (Chapter 4, materially updated in the 2019 Refinement). The carbon-content-of-fuel approach used in many Scope 1 stationary calculators is the Volume 2 Chapter 1 default.

**IPPU (Volume 3).** Emission factors for cement clinker production, lime production, ammonia, nitric acid, adipic acid, aluminium smelting (PFC byproducts), magnesium production (SF₆ cover gas), and semiconductor manufacturing (NF₃, PFCs). Refrigerant emissions methodologies are also Volume 3 (Chapter 7), though for the EU these are now operationalised through [Regulation 2024/573](../eu/f-gas-regulation.md).

**AFOLU (Volume 4).** Methodologies for livestock enteric fermentation, manure management, agricultural soils (direct and indirect N₂O), rice cultivation, prescribed burning, and land-use change. This volume is the upstream source for many Scope 3 Category 1 (purchased goods) agricultural emission factors and is the methodological anchor for the [GHG Protocol Land Sector and Removals Standard](../ghg-protocol/land-sector-removals-2026.md).

**Waste (Volume 5).** First-Order Decay (FOD) model for landfill methane (Chapter 3), biological treatment of solid waste (Chapter 4), incineration and open burning (Chapter 5), wastewater treatment and discharge (Chapter 6). The FOD model in particular underpins almost every commercial landfill CH₄ calculator.

**General Guidance (Volume 1).** Time series consistency, uncertainty assessment (the propagation approach Tier 1 / Monte Carlo Tier 2), key category analysis, QA/QC procedures, and reporting tables. Volume 1 is the methodological glue that allows the four sectoral volumes to combine into a coherent national inventory.

## The 2019 Refinement — what changed

The 2019 Refinement updated specific methodologies and emission factors where post-2006 science warranted revision. The most consequential updates for corporate inventories:

| Area | 2006 default | 2019 Refinement | GreenCalculus implementation |
|---|---|---|---|
| **Fugitive coal mine CH₄** | Generic factors by mining type | Refined factors with depth, basin, and gas-content sensitivity | Used in fugitive coal calculators (Volume 2 Chapter 4 updated) |
| **F-gas emission factors** | Limited coverage | Expanded coverage, updated lifecycle factors | Used alongside [EU 2024/573](../eu/f-gas-regulation.md) and [AR6 GWPs](./ar6-gwp-100.md) |
| **Forest and other land-use** | Default biomass and soil carbon factors | Refined biomass densities, soil carbon stock-change factors | Used in [LSR 2026](../ghg-protocol/land-sector-removals-2026.md) -aligned removals calculators |
| **N₂O from soils** | Generic emission factors | Disaggregated factors by climate, crop, and management | Used in agricultural soils calculators (Tier 2 path) |
| **Wastewater** | Updated population-equivalent factors and protein-intake updates | Region-specific methane correction factors | Used in industrial wastewater calculators |

Throughout, the 2019 Refinement retains the 2006 Guidelines' tier structure and overall format. Countries adopting the Refinement do so on a category-by-category basis as part of their inventory cycle.

## The UNFCCC Enhanced Transparency Framework — why these guidelines are mandatory

Under the Paris Agreement's Enhanced Transparency Framework (ETF), all Parties — developed and developing — are required to submit **Biennial Transparency Reports (BTRs)** with their national GHG inventories. The first BTRs were due 31 December 2024. The 2006 IPCC Guidelines (with the 2019 Refinement) are the **mandatory methodological basis** for these reports — Decision 18/CMA.1 (Katowice, 2018) explicitly so requires.

This is a step up from the pre-Paris regime, under which only Annex I (developed) countries used the 2006 Guidelines mandatorily and developing countries could use earlier (1996 Revised) guidelines. Under ETF, the same methodological floor applies globally.

The first BTR review cycle is underway through 2025–2026. The Technical Expert Review Teams (ERTs) coordinated by the UNFCCC Secretariat are reviewing submitted inventories for methodological consistency with the 2006 Guidelines + 2019 Refinement.

## How GreenCalculus implements the 2006 Guidelines

**Default factors traced to source.** Every Tier 1 emission factor in the Master Brain data layer carries a citation back to its IPCC volume, chapter, and table number where applicable. The 2019 Refinement values are tagged explicitly as such.

**Tier hierarchy surfaced in calculators.** Where users can substitute country-specific or facility-specific data, the calculator surfaces the methodological tier (Tier 1 default → Tier 2 country → Tier 3 facility) so the user can document their data hierarchy choice for verification under [ISO 14064-1](../iso/14064-1-organisation-ghg-quantification.md).

**Volume-aligned categorisation.** Calculator scope tags map cleanly to IPCC source categories: 1A1 (Energy: Stationary Combustion — Energy Industries), 1A2 (Manufacturing), 1A3 (Transport), 1A4 (Other Sectors), 1B1 (Fugitive Coal), 1B2 (Fugitive Oil & Gas), and so on through the IPPU, AFOLU, and Waste codes.

**AR6 GWP application.** The 2006 Guidelines originally referenced 1995 (SAR) GWPs; the 2019 Refinement did not mandate AR6. Corporate users following GHG Protocol must apply [AR6 GWP-100](./ar6-gwp-100.md) regardless of the IPCC vintage of the underlying emission factor — GreenCalculus enforces this consistently, with AR5 retained for legacy comparison only.

**Uncertainty propagation.** Volume 1 Chapter 3 of the 2006 Guidelines specifies how to combine uncertainties across categories. GreenCalculus calculators surface the qualitative or quantitative uncertainty range from the underlying factor, and aggregate calculators apply the Tier 1 propagation approach (error propagation with default correlations).

## Relationship with other standards

The 2006 IPCC Guidelines sit at the methodological base of the standards stack:

| Downstream standard | Relationship |
|---|---|
| [GHG Protocol Corporate Standard](../ghg-protocol/corporate-standard.md) | Cites IPCC Guidelines as the upstream science / methodology source for default factors |
| [GHG Protocol Scope 3 Standard](../ghg-protocol/scope-3-standard.md) | Category-specific methodologies (Cat. 1, 4, 5, 11) draw on IPCC AFOLU, Energy, and Waste volumes |
| [GHG Protocol LSR 2026](../ghg-protocol/land-sector-removals-2026.md) | AFOLU methodology heavily aligned with IPCC Volume 4; LSR refines for corporate use |
| [ISO 14064-1](../iso/14064-1-organisation-ghg-quantification.md) | Compatible — 14064-1 inventories can be built using IPCC methodologies + corporate scopes mapping |
| [UK DEFRA conversion factors](../factor-sets/uk-defra-2025.md) | UK national inventory methodology derives from IPCC 2006 + 2019 Refinement |
| EPA eGRID, IEA factors | National/regional implementations of IPCC methodology with country-specific data |

## Important caveats

A few points worth flagging:

**1. The Guidelines are designed for national inventories, not corporate inventories.** Methodologies translate well but not always cleanly. National inventories aggregate across all activities in a territory; corporate inventories aggregate across organisational boundaries. The factor values are usually directly usable; the categorisation and reporting structure must be re-applied through GHG Protocol or ISO 14064-1.

**2. The 2019 Refinement is not a full revision.** It supplements rather than replaces the 2006 Guidelines. Countries (and corporate calculators) use the 2006 Guidelines as the base and apply 2019 Refinement updates where available. The next full IPCC inventory methodology revision is not yet scheduled.

**3. Tier 1 defaults are often conservative.** IPCC default factors are designed to apply broadly across countries with limited data. Where country-specific or facility-specific values are available, they almost always produce more accurate (and frequently lower) estimates. Where regulatory compliance permits Tier 2/3, users should pursue them.

**4. AR6 GWPs are not part of the 2006 Guidelines themselves.** The 2006 Guidelines use 1995 (SAR) GWPs in their original text. Corporate users must overlay [AR6 GWP-100](./ar6-gwp-100.md) per the [GHG Protocol Corporate Standard 2026 revision](../ghg-protocol/corporate-standard.md).

**5. GreenCalculus is not a national-inventory tool.** The calculators are designed for corporate (and increasingly product- and site-level) inventory work. National inventory compilers should use national inventory software (e.g. the IPCC Inventory Software) and the original Guidelines documentation directly.

## Calculators on greencalculus.com that use this standard

The 2006 IPCC Guidelines are upstream of virtually every default emission factor on the platform. Most directly visible in:

- All Scope 1 stationary combustion calculators (Volume 2, Chapter 2 — combustion factors by fuel type)
- All Scope 1 mobile combustion calculators (Volume 2, Chapter 3 — road, rail, aviation, marine)
- All Scope 1 fugitive coal methane calculators (Volume 2, Chapter 4 — 2019 Refinement basin factors)
- All Scope 1 fugitive oil & gas calculators (Volume 2, Chapter 4 — venting, flaring, leakage)
- All Scope 1 industrial process calculators (Volume 3 — cement, lime, ammonia, aluminium, semiconductor)
- All Scope 1 agriculture calculators (Volume 4 — enteric, manure, soils, rice, prescribed burning)
- All Scope 3 Category 5 waste calculators (Volume 5 — landfill FOD, wastewater, biological treatment)
- Land-use and removals calculators (Volume 4 — also via [LSR 2026 mapping](../ghg-protocol/land-sector-removals-2026.md))

## Official sources

- [IPCC Task Force on National Greenhouse Gas Inventories — official site](https://www.ipcc-nggip.iges.or.jp/)
- [2006 IPCC Guidelines for National Greenhouse Gas Inventories — full text](https://www.ipcc-nggip.iges.or.jp/public/2006gl/)
- [2019 Refinement to the 2006 IPCC Guidelines — full text](https://www.ipcc-nggip.iges.or.jp/public/2019rf/index.html)
- [Emission Factor Database (EFDB)](https://www.ipcc-nggip.iges.or.jp/EFDB/main.php)
- [UNFCCC Enhanced Transparency Framework — modalities, procedures and guidelines (Decision 18/CMA.1)](https://unfccc.int/sites/default/files/resource/cma2018_3_add2_new_advance.pdf)
- [IPCC Inventory Software](https://www.ipcc-nggip.iges.or.jp/software/index.html)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/ipcc-2006-guidelines-national-inventories/](https://greencalculus.com/standards/ipcc-2006-guidelines-national-inventories/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> IPCC (2006). *2006 IPCC Guidelines for National Greenhouse Gas Inventories* [Eggleston H.S., Buendia L., Miwa K., Ngara T. and Tanabe K. (eds.)]. Prepared by the National Greenhouse Gas Inventories Programme. IGES, Japan.

For the 2019 Refinement:

> IPCC (2019). *2019 Refinement to the 2006 IPCC Guidelines for National Greenhouse Gas Inventories* [Calvo Buendia, E., Tanabe, K., Kranjc, A., Baasansuren, J., Fukuda, M., Ngarize, S., Osako, A., Pyrozhenko, Y., Shermanau, P. and Federici, S. (eds.)]. Published: IPCC, Switzerland.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-25
