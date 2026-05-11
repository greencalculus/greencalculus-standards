# GHG Protocol Corporate Value Chain (Scope 3) Standard

| Field | Value |
|---|---|
| **Initiative** | GHG Protocol (WRI / WBCSD) |
| **Operative version** | 2011 edition (still in effect) |
| **Latest substantive update** | 31 March 2026 — Phase 1 Progress Update (draft) |
| **Next mandatory date** | Final revised standard targeted late 2027, effective 2028 or later |
| **Administered by** | World Resources Institute (WRI) and World Business Council for Sustainable Development (WBCSD) |
| **GreenCalculus stack layer** | Layer 2 — Calculation |
| **Last reviewed** | 2026-05-11 |

---

## What this standard does

The Corporate Value Chain (Scope 3) Accounting and Reporting Standard, published in 2011, is the global framework for how companies measure and report indirect emissions across their value chain. It defines the **15 Scope 3 categories** — from purchased goods and services (Category 1) through to investments (Category 15) — that together typically account for the majority of a company's total carbon footprint.

The Scope 3 Standard supplements the [GHG Protocol Corporate Standard](./corporate-standard.md) and is normatively referenced by virtually every corporate climate framework: SBTi target-setting, CSRD / ESRS E1 disclosure, CDP reporting, IFRS S2 / ISSB, California SB 253, and SEC climate disclosure rules.

## Why it matters for GreenCalculus

Scope 3 is where most companies' real emissions live — often 70% or more of total footprint. It is also where calculation methodology is hardest and most contested, because data is rarely primary and methods range from highly granular activity-based calculations down to spend-based proxies.

The Scope 3 Standard defines which categories are mandatory, what data hierarchies are acceptable, and how to disclose exclusions. Every Scope 3 calculator on GreenCalculus is mapped to a specific category number and follows the calculation methods this standard prescribes.

## The 15 Scope 3 categories

| # | Category | CSRD-mandatory | GreenCalculus Master Brain sections |
|---|---|---|---|
| 1 | Purchased goods and services | Yes | supply_chain |
| 2 | Capital goods | Yes | supply_chain, buildings |
| 3 | Fuel- and energy-related activities | Yes | fuels, grid |
| 4 | Upstream transportation and distribution | Yes | freight |
| 5 | Waste generated in operations | Yes | waste, water |
| 6 | Business travel | Yes | business_travel |
| 7 | Employee commuting | Yes | commuting |
| 8 | Upstream leased assets | No | fuels, grid |
| 9 | Downstream transportation and distribution | No | freight |
| 10 | Processing of sold products | No | fuels, grid |
| 11 | Use of sold products | Yes | fuels, grid |
| 12 | End-of-life treatment of sold products | Yes | waste |
| 13 | Downstream leased assets | No | fuels, grid |
| 14 | Franchises | No | fuels, grid |
| 15 | Investments | No | (financed emissions module, in development) |

The CSRD-mandatory column reflects ESRS E1-6 disclosure requirements for in-scope EU companies.

## How GreenCalculus implements this standard

**Category tagging.** Every calculator and every emission factor in the Master Brain data layer (§15 commuting, §07 freight, §06 business_travel, §13 supply_chain, etc.) carries an explicit Scope 3 category designation. Audit-ready outputs include the category number on every line item.

**Data hierarchy.** Where GreenCalculus offers multiple calculation paths for the same activity (for example, distance-based vs spend-based for freight), the higher-quality path is presented first and clearly labelled. This anticipates the proposed data-tier disaggregation requirement in the 2026 revision (see below).

**Worked example alignment.** Where the Scope 3 Standard provides worked examples in its Chapter 5–10 annexes, GreenCalculus calculators reproduce those calculations as test cases to verify mathematical alignment.

## The 2026 revision — what's changing

The first major revision of the Scope 3 Standard since 2011 is currently in progress. The **Phase 1 Progress Update was published 31 March 2026** by the GHG Protocol Technical Working Group. The document is **draft material, not a final standard**, and a full public consultation draft is forthcoming. Final approval is targeted for **late 2027**, with effective adoption in **2028 or later**.

The most consequential proposed changes:

**1. 95% coverage floor (Revision B1).** Companies reporting in conformance with the revised standard would need to account for at least 95% of total required Scope 3 emissions. Exclusions could not exceed 5% and must be quantified, disclosed, and justified — replacing the current soft "disclose and justify" language. This aligns with SBTi and CDP's existing 5% thresholds.

**2. Mandatory data-tier disaggregation (Revision A1).** Reported Scope 3 emissions would need to be broken down by data type for each category — distinguishing primary supplier data, secondary data, and spend-based proxies. The intent is to make data quality visible and put public pressure on spend-based estimates.

**3. Verification disclosure (Revision A2).** Companies would need to label each Scope 3 figure as verified, partially verified, or not verified by a third party.

**4. Category 16 — facilitated emissions (proposed new).** A new optional category covering insurance underwriting, capital markets facilitation, and other value-chain activities that don't fit cleanly into Category 15 (investments). This would move insurance-associated emissions out of Category 15, narrowing it to investments proper and financed emissions.

**5. Allocation method restrictions (Revision A8).** Corporate-level emissions allocation would be restricted to single-industry suppliers only. Diversified suppliers would require product- or site-level data.

**6. Tightened Category 15 scope.** Investments category would explicitly apply to all companies (not only investment managers), but its scope would be narrower with insurance moved to Category 16.

## What GreenCalculus is doing about the revision

The 2026 Phase 1 Update is draft; no GreenCalculus calculator currently implements proposed revisions as binding. However, our Master Brain data layer already supports the disaggregation patterns the revision proposes — every factor carries explicit metadata for source, calculation method, and data tier. When the final revised standard is approved (targeted late 2027), GreenCalculus calculators will be updated to surface this disaggregation as a default output column, in line with the proposed Revision A1.

Companies with SBTi-validated targets will face the most direct exposure to the revised standard, because SBTi mandates GHG Protocol methodology and the new SBTi Corporate Net-Zero Standard v2 is being written to reference the revised Scope 3 Standard. See our [SBTi Net-Zero Standard mapping](../targets/sbti-net-zero.md) for the implications.

## Calculators on greencalculus.com that use this standard

This list will be populated as each Scope 3 calculator's mapping is verified.

- All Category 1 (Purchased Goods and Services) calculators — spend-based and supplier-specific
- All Category 4 (Upstream Transportation and Distribution) calculators
- All Category 5 (Waste in Operations) calculators
- All Category 6 (Business Travel) calculators — flights, rail, road, hotels
- All Category 7 (Employee Commuting) calculators
- All Category 11 (Use of Sold Products) calculators
- All Category 12 (End-of-Life Treatment of Sold Products) calculators

## Official sources

- [Scope 3 Standard — official page](https://ghgprotocol.org/standards/scope-3-standard)
- [Scope 3 Calculation Guidance (2013)](https://ghgprotocol.org/scope-3-calculation-guidance-2)
- [Scope 3 Phase 1 Progress Update — March 2026](https://ghgprotocol.org/scope-3-standard-revisions-phase-1-progress-update)
- [Standard Development Plan (Scope 3)](https://ghgprotocol.org/sites/default/files/2025-01/S3-SDP-20241220.pdf)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/ghg-protocol-scope-3-standard/](https://greencalculus.com/standards/ghg-protocol-scope-3-standard/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> World Resources Institute and World Business Council for Sustainable Development (2011). *Corporate Value Chain (Scope 3) Accounting and Reporting Standard.* WRI/WBCSD.

For the in-progress revision:

> GHG Protocol (2026). *Scope 3 Standard Revisions: Phase 1 Progress Update.* GHG Protocol Technical Working Group, 31 March 2026.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-11
