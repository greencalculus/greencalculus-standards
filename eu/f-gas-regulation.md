# EU F-Gas Regulation (EU) 2024/573

| Field | Value |
|---|---|
| **Initiative** | European Union Regulation on fluorinated greenhouse gases |
| **Operative version** | Regulation (EU) 2024/573 |
| **Latest substantive update** | Adopted 7 February 2024; in force 11 March 2024; replaces Regulation (EU) 517/2014 |
| **Next mandatory date** | Mandatory Commission review by 1 January 2030; 2040 review of 2050 HFC phase-out feasibility |
| **Administered by** | European Commission (DG Climate Action); enforced by Member State competent authorities via the F-gas Portal |
| **GreenCalculus stack layer** | Layer 3 — Factor data / sectoral regulatory trigger for Scope 1 fugitive emissions |
| **Last reviewed** | 2026-05-16 |

---

## What this regulation does

Regulation (EU) 2024/573 — commonly known as the "new F-Gas Regulation" — is the EU's primary legal instrument for controlling fluorinated greenhouse gas (F-gas) production, placement on the market, use, and emissions. It replaced the previous Regulation (EU) 517/2014 and entered into force on **11 March 2024**.

The regulation covers three groups of fluorinated gases with high global warming potential:

- **Hydrofluorocarbons (HFCs)** — refrigerants, foam blowing agents, propellants, fire suppressants
- **Perfluorocarbons (PFCs)** — semiconductor manufacturing, specialised industrial uses
- **Sulphur hexafluoride (SF₆)** — electrical switchgear, magnesium production

It also brings into scope 23 additional F-gases not previously regulated (including HFOs, HCFOs, fluorinated ethers, ketones, and alcohols), and adds metered dose inhalers (MDIs) to the HFC quota system for the first time.

The regulation's stated objective is an **80% reduction in HFC consumption by 2030** and a **full HFC phase-out by 2050**.

## Why it matters for GreenCalculus

The F-Gas Regulation is unusual in this repository because it is a **regulatory ban** rather than a disclosure standard. It does not tell companies how to report emissions — it tells them which gases they can use, in what quantities, and when each use will be prohibited. But it triggers GHG accounting in three direct ways:

1. **Fugitive Scope 1 emissions.** Refrigerant leaks from refrigeration, air conditioning, heat pumps (RACHP), electrical switchgear, and fire suppression systems are Scope 1 emissions per the [GHG Protocol Corporate Standard](../ghg-protocol/corporate-standard.md). Every kilogram of refrigerant leaked is multiplied by its GWP to produce CO₂e under [IPCC AR6 GWP-100](../ipcc/ar6-gwp-100.md). GreenCalculus refrigerant calculators directly calculate this.
2. **Mandatory leak checks.** The regulation requires regular leak detection by certified personnel for equipment above specific CO₂e thresholds. Leak-check frequency depends on a system's F-gas charge in CO₂e — which means every operator needs to calculate that figure.
3. **Transition planning.** Companies replacing high-GWP equipment with low-GWP alternatives need to model Scope 1 emissions before and after the swap to demonstrate compliance and progress against climate targets.

For users in the EU, UK (which broadly aligns), and other jurisdictions modelled on the EU regulation, F-Gas compliance is the regulatory trigger that makes refrigerant-emissions accounting mandatory.

## HFC quota system — the core mechanism

The regulation phases down HFCs through a **quota system** measured in tonnes of CO₂-equivalent (using AR4 GWP-100 values as the regulatory basis — note this is *not* AR6; the regulation retained AR4 for legal continuity with 517/2014).

The phase-down schedule is steep:

| Period | Maximum HFC quota (MtCO₂e) | Reduction vs 2023 baseline (82.3 MtCO₂e) |
|---|---|---|
| 2025–2026 | ~42.9 | 48% reduction |
| 2027–2029 | ~21.7 (halved again) | ~74% reduction |
| 2030–2032 | ~9.0 (further halved) | ~89% reduction |
| 2036 onwards | Production capped at 15% of 2011–2013 average | Production phase-down |
| 2050 | Full phase-out of HFC consumption | 100% reduction |

The reduced quota applies only to **HFCs placed on the EU market for the first time**. Recycled or reclaimed HFCs already inside the EU are exempt from the quota — which is a major policy lever supporting refrigerant recovery and recycling.

A small **safety-net mechanism** allows the Commission to release limited additional HFC quota in 2025–2029 if shortages threaten the EU's REPowerEU heat pump deployment targets.

## Product and use bans

Beyond the quota system, the regulation introduces application-specific bans on **placing equipment on the market** and on **servicing existing equipment**. Selected key bans most relevant to GreenCalculus users:

### From 1 January 2025

- **Refrigeration and stationary AC servicing** with virgin HFCs of GWP ≥ 2,500 — banned (R404A use becomes severely restricted; recycled/reclaimed allowed until 1 January 2030)
- **Commercial refrigerators and freezers** containing F-gases with GWP ≥ 150 — placement on market prohibited (limited derogations to 30 June 2026 for blast cabinets, gelato makers, ice makers, food trolleys, retarder provers, frozen drinks dispensers)
- **Personal care and skin cooling products** with GWP ≥ 150 — prohibited (medical exceptions)
- **Fire protection equipment** — prohibited except where site safety requires
- **MDI inhalers** with HFCs — now included in the quota system

### From 12 March 2025 (export bans)

- Export of stationary refrigeration, AC, heat pumps, foams, and technical aerosols requiring F-gases with GWP ≥ 1,000 to non-EU countries — prohibited. The intent is to prevent the dumping of obsolete equipment into developing-country markets.

### From 2026

- **Stationary AC and heat pump systems** containing virgin F-gases with GWP ≥ 2,500 — banned for servicing (reclaimed gases allowed until 2032)
- **Domestic refrigerators, standalone refrigeration units, technical aerosols** — further GWP-150 thresholds extended

### From 2027–2028

- **Imports/exports of HFCs** with non-signatories to the Montreal Protocol — prohibited from 1 January 2028
- **Stricter member state certification** — refreshment training required for existing F-gas certificate holders by 12 March 2029

### From 2030–2035

- **Single-split AC and heat pumps**: F-gas use allowed without time limit only if GWP < 750
- **Multi-split, VRV/VRF systems** (<12 kW): GWP < 150 required from 1 January 2035
- **Insulation foams and other technical applications**: further sector-specific bans

### From 2050

- **HFC consumption in the EU** — fully phased out

## How GreenCalculus implements this regulation

**Scope 1 fugitive emissions calculators.** The Master Brain data layer (§10 refrigerants) maintains the complete refrigerant catalogue — R134a, R404A, R410A, R407C, R32, R290 (propane), R744 (CO₂), R717 (ammonia), HFO blends, and others — each tagged with both **AR4 GWP-100** (the regulation's legal basis) and **AR6 GWP-100** (the science basis required by the [GHG Protocol](../ghg-protocol/corporate-standard.md)).

**Why two GWP bases?** Because the F-Gas Regulation uses AR4 for legal compliance (quota calculations, GWP threshold determinations like the 150 / 750 / 2,500 cut-offs, and leak-check thresholds expressed in CO₂e), but corporate emissions reporting uses AR6. A facility manager calculating their CO₂e charge for the legal threshold and their CO₂e leak for Scope 1 reporting will use different multipliers for the same gas. GreenCalculus surfaces both clearly to avoid confusion.

**Leak-rate calculators.** Several calculators compute equipment leak rates against the regulation's mandatory leak-check frequency thresholds (which scale with CO₂e charge).

**Transition planning calculators.** Where companies are modelling a swap from R410A → R32 → R290, GreenCalculus surfaces before-and-after Scope 1 fugitive emissions, capital cost considerations, and compliance with relevant ban deadlines.

## The PFAS overlap — a watch point

A significant emerging issue is the overlap between F-gases and **per- and polyfluoroalkyl substances (PFAS, "forever chemicals")**. Many low-GWP F-gas alternatives — particularly HFOs and HCFOs — are themselves classified as PFAS under the EU's REACH chemicals regulation, and could face separate restrictions on that basis. This is not addressed in Regulation 2024/573 itself but is being considered under parallel REACH proceedings.

For companies planning a transition strategy, the implication is that some HFO-based alternatives that comply with the F-Gas Regulation may face future REACH-driven bans. Natural refrigerants (CO₂, ammonia, hydrocarbons such as propane and isobutane) are PFAS-free and provide the most resilient long-term pathway.

## Relevant implementing regulations

The regulation requires multiple Commission Implementing Regulations to operationalise specific provisions. Most relevant so far:

- **Implementing Regulation (EU) 2024/2215** (September 2024) — Certification and training requirements, including extension to organic Rankine cycles and refrigerated units in mobile equipment. Member States had until September 2025 to implement.
- **Implementing Regulation (EU) 2024/2729** — Four-year derogation (until 31 December 2028) from product ban 4 for specific laboratory equipment (blast cabinets, gelato machines, ice makers, etc. listed above).
- **F-gas Portal** — Centralised system for licensing, quota tracking, and reporting. Mandatory use for all in-scope operators.

## Mandatory reviews

Two scheduled reviews are written into the regulation:

- **By 1 January 2030** — Commission report on the regulation's effects, including evaluation of whether cost-effective, technically feasible, energy-efficient, sufficiently available, and reliable alternatives exist for replacement of F-gases in Annex IV products and equipment.
- **By 1 January 2040** — Commission evaluation of the feasibility of the 2050 HFC consumption phase-out, accounting for technological development and availability of HFC alternatives.

## Important caveats for GreenCalculus users

A few points worth highlighting:

**1. The regulation uses AR4 GWP-100, not AR6.** This is a legal/historical artifact: Regulation 517/2014 used AR4, and 2024/573 retained AR4 for continuity of the quota mechanism. Companies reporting Scope 1 fugitive emissions under GHG Protocol or CSRD must still use AR6 GWP-100 values. GreenCalculus retains both for this reason — see [IPCC AR6 GWP-100 mapping](../ipcc/ar6-gwp-100.md) for the science layer.

**2. GreenCalculus is not legal advice or compliance certification.** A calculator producing F-Gas-aligned figures does not discharge the regulation's certification, leak-check, recovery, or reporting obligations. Operators must engage certified personnel and maintain the records the regulation prescribes.

**3. UK alignment is separate but broadly parallel.** The UK is not subject to EU 2024/573 directly. The UK's equivalent F-Gas regulations (post-Brexit) broadly track EU policy but diverge in specific timelines. UK-based GreenCalculus users should consult [UK DEFRA guidance](https://greencalculus.com/standards/uk-defra-emission-factors/) for UK-specific obligations.

**4. Quota and price volatility.** The HFC quota cuts in 2025–2026 and again in 2027–2029 are steep. Refrigerant prices, particularly for higher-GWP HFCs, are expected to remain volatile. Operators should factor this into both Scope 1 fugitive emissions projections and equipment lifecycle cost planning.

## Calculators on greencalculus.com that use this regulation

This list will be populated as each calculator's F-Gas alignment is verified. Affected categories include:

- All Scope 1 refrigerant leak calculators (commercial refrigeration, supermarket systems, cold chain)
- All Scope 1 stationary AC and heat pump fugitive emissions calculators
- All Scope 1 electrical switchgear SF₆ leak calculators
- Fire suppression system fugitive emissions calculators
- MDI propellant lifecycle calculators
- Equipment transition planning calculators (R410A → R32 → R290 swap modelling)
- Refrigerant CO₂e charge calculators (for leak-check threshold determination)

## Official sources

- [European Commission — Fluorinated Greenhouse Gases (Climate Action)](https://climate.ec.europa.eu/eu-action/fluorinated-greenhouse-gases/f-gas-legislation_en)
- [Regulation (EU) 2024/573 — official EUR-Lex text](https://eur-lex.europa.eu/eli/reg/2024/573/oj)
- [Implementing Regulation (EU) 2024/2215](https://eur-lex.europa.eu/eli/reg_impl/2024/2215/oj)
- [Implementing Regulation (EU) 2024/2729](https://eur-lex.europa.eu/eli/reg_impl/2024/2729/oj)
- [EPEE — New F-gas Regulation Guide for Producers and Users](https://www.epeeglobal.org/)
- [AREA — Practical Guide to the New F-Gas Regulation](https://www.area-eur.be/)
- [European Heat Pump Association — F-Gas Regulation Guidelines](https://www.ehpa.org/)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this regulation lives at:

**[greencalculus.com/standards/f-gas-regulation-eu-2024/](https://greencalculus.com/standards/f-gas-regulation-eu-2024/)**

That page is the canonical citation target for this regulation mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> European Parliament and Council of the European Union (2024). *Regulation (EU) 2024/573 of the European Parliament and of the Council of 7 February 2024 on fluorinated greenhouse gases, amending Directive (EU) 2019/1937 and repealing Regulation (EU) No 517/2014.* Official Journal of the European Union, 20 February 2024.

For the preceding regulation (for historical context):

> European Parliament and Council of the European Union (2014). *Regulation (EU) No 517/2014 of the European Parliament and of the Council of 16 April 2014 on fluorinated greenhouse gases and repealing Regulation (EC) No 842/2006.* Official Journal of the European Union.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-16
