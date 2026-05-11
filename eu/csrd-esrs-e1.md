# CSRD / ESRS E1 — Corporate Sustainability Reporting Directive, Climate Change Standard

| Field | Value |
|---|---|
| **Initiative** | EU Corporate Sustainability Reporting Directive (CSRD) — Climate change standard ESRS E1 |
| **Operative version** | ESRS Set 1 (Delegated Regulation EU 2023/2772), as modified by Quick Fix Delegated Regulation (Nov 2025) and Omnibus I Directive (EU) 2026/470 |
| **Latest substantive update** | Omnibus I Directive (EU) 2026/470, in force 18 March 2026 |
| **Next mandatory date** | Simplified ESRS Delegated Act due by 18 September 2026, applying from FY 2027 (reporting in 2028) |
| **Administered by** | European Commission; technical standards developed by EFRAG |
| **GreenCalculus stack layer** | Layer 6 — Disclosure |
| **Last reviewed** | 2026-05-14 |

---

## What this standard does

The Corporate Sustainability Reporting Directive (CSRD) is the European Union's mandatory sustainability disclosure regime. Within CSRD, the European Sustainability Reporting Standards (ESRS) define the specific information companies must disclose. **ESRS E1 — Climate Change** is the most substantive topical standard in the set, covering GHG emissions disclosure, transition plans, climate targets, anticipated financial effects of climate-related risks, and the alignment of operations and CapEx with EU Taxonomy and Paris Agreement goals.

ESRS E1 retains a special status in the simplified ESRS framework: while data points across other topical standards have been reduced, ESRS E1 keeps its own dedicated anticipated financial effects requirement (E1-11) because regulators want companies to continue distinguishing between physical and transition climate risks.

## Why it matters for GreenCalculus

For in-scope companies, CSRD/ESRS E1 is the regulation that *forces* GHG accounting from a voluntary exercise into a mandatory, audited disclosure. ESRS E1 explicitly requires GHG inventories prepared "in accordance with" the GHG Protocol — making GreenCalculus calculators directly relevant for the underlying data, and making the upstream standards (Corporate Standard, Scope 3 Standard, IPCC AR6 GWPs) part of the CSRD audit trail.

A CSRD reviewer or auditor reading a GreenCalculus output should be able to trace every number back to: a GHG Protocol scope, a published emission factor source, and an AR6 GWP basis. That traceability is the entire point of mapping CSRD onto our calculator outputs.

## The Omnibus I reform — what changed in 2026

The CSRD landscape shifted dramatically in 2025–2026. Three legislative instruments are now operative:

### Stop-the-Clock Directive (EU 2025/794)

**Published 16 April 2025; in force 17 April 2025.** Defers by two years the application of CSRD requirements for Wave 2 (large non-Wave-1 companies) and Wave 3 (listed SMEs and certain credit/insurance entities). Wave 1 timetable was unchanged. Wave 4 (non-EU enterprise reporting) was also unchanged.

### Quick Fix Delegated Regulation

**Adopted 11 July 2025; published in OJEU 10 November 2025; in force 13 November 2025.** Provides Wave 1 companies with extended transitional reliefs and additional reporting flexibility for FY 2025 and FY 2026 reporting, effectively freezing the additional reporting requirements that would have phased in. Wave 1 still reports — but the level of reporting in 2026 and 2027 (covering FY 2025 and FY 2026) is closer to what was filed for FY 2024.

### Omnibus I Directive (EU 2026/470)

**Published in OJEU 26 February 2026; in force 18 March 2026.** This is the substantive scope-narrowing directive. Key provisions:

- **New permanent thresholds.** From fiscal years beginning on or after 1 January 2027, CSRD applies only where a company exceeds **both** 1,000 employees and €450 million net turnover. The original thresholds were considerably lower (250 employees / €50M turnover or €25M balance sheet), so the new rules remove a substantial number of mid-size European companies from mandatory direct scope.
- **Listed SMEs are no longer in scope.**
- **Non-EU threshold revised.** For non-EU companies, the new threshold is €450 million in net EU turnover (up from €150M) plus an EU subsidiary or branch with at least €200M in EU revenue.
- **Limited assurance retained.** The planned progression from limited to reasonable assurance has been cancelled.
- **Sector-specific ESRS dropped.** Development of sector-specific standards has been discontinued.
- **Value chain cap.** Companies in scope cannot require companies outside CSRD scope (in their value chain) to provide more data than is set out in the voluntary VSME standard. Voluntary sharing is unaffected.
- **Member state transitional options.** Wave 1 companies that would fall below the new thresholds can be exempted from FY 2025 and FY 2026 reporting at member state discretion — but only where the relevant member state has transposed the directive accordingly. Most have not yet done so.

### Wave 1 — what reporting is still required

Wave 1 companies (those already reporting under the original CSRD) continue to report through the 2026 reporting year and 2027 reporting year — covering FY 2025 and FY 2026 data — *unless* they fall under a member state exemption. From FY 2027 onwards, only companies meeting the new permanent thresholds remain in scope.

### Simplified ESRS — the next deadline

Omnibus I requires the European Commission to adopt a revised, simplified ESRS Delegated Act **by 18 September 2026**. EFRAG submitted its technical advice in December 2025; the Commission can modify the text within the Omnibus mandate. The simplified ESRS will apply from FY 2027 reporting, with optional early adoption for FY 2026.

### N-ESRS — paused

The separate set of standards for non-EU groups (N-ESRS) — originally intended for FY 2028 reporting — has been paused. Work is expected to resume after the main simplified ESRS are final.

## ESRS E1 disclosure requirements

ESRS E1 covers ten disclosure requirements plus two policy-level ones. The core for any GHG calculator output is **E1-6 (Gross Scopes 1, 2, 3 and total GHG emissions)** — which is what GreenCalculus is most directly mapped to.

| Disclosure | Scope | Where GreenCalculus contributes |
|---|---|---|
| E1-1 Transition plan for climate change mitigation | Strategy | Decarbonisation roadmap tools |
| E1-2 Policies related to climate change mitigation and adaptation | Policy | — |
| E1-3 Actions and resources in relation to climate change policies | Actions | — |
| E1-4 Targets related to climate change mitigation and adaptation | Targets | SBTi-aligned target tools |
| E1-5 Energy consumption and mix | Activity data | Energy use calculators |
| **E1-6 Gross Scopes 1, 2, 3 and total GHG emissions** | **GHG accounting** | **Primary mapping — most calculators** |
| E1-7 GHG removals and GHG mitigation projects | Removals | LSR-aligned removals calculators |
| E1-8 Internal carbon pricing | Strategy | — |
| E1-9 Anticipated financial effects from material physical and transition risks | Financial | — |
| E1-11 Anticipated financial effects retained | Financial | — |

GHG emissions disclosed under E1-6 must be calculated in accordance with the **GHG Protocol Corporate Standard** and disaggregated by scope. Scope 3 disclosure requires the 15 GHG Protocol categories. AR6 GWP-100 values are required for the CO₂e conversion.

## How GreenCalculus implements ESRS E1 alignment

**Calculator output → ESRS E1-6 line item mapping.** Every Scope 1, 2, or 3 calculator on the platform produces output that can be dropped directly into the ESRS E1-6 disaggregation table. The Master Brain data layer tags every factor with its GHG Protocol scope, Scope 3 category number, and AR6 GWP basis — the three audit-trail elements ESRS E1 requires.

**Scope 2 dual reporting.** Per the GHG Protocol Scope 2 Guidance and ESRS E1-6 requirements, GreenCalculus electricity calculators present both location-based and market-based results.

**Scope 3 category disaggregation.** CSRD-mandatory Scope 3 categories (1, 2, 3, 4, 5, 6, 7, 11, 12 per current ESRS E1) are surfaced explicitly. Optional categories are clearly labelled.

**AR6 GWP basis.** All CO₂e conversions use IPCC AR6 GWP-100 values, in line with ESRS E1 expectations.

## Important caveats for CSRD reporters

A few points often unclear in commercial summaries:

**1. GreenCalculus is not assurance.** A calculator producing an ESRS E1-aligned number does not discharge the limited assurance obligation. The user remains responsible for engaging a statutory auditor or independent assurance services provider, and for assembling supporting documentation (activity data sources, calculation logs, control evidence).

**2. ESRS E1 changes are still in flight.** The simplified ESRS Delegated Act has not yet been finalised at the time of this writing (May 2026). GreenCalculus calculator mappings reflect ESRS Set 1 (2023/2772) as modified by Quick Fix; further alignment updates will follow when the simplified ESRS is published in Q3 2026.

**3. The LSR Standard is not yet referenced by ESRS.** Companies with material land-sector emissions are not required to apply the [GHG Protocol Land Sector and Removals Standard](../ghg-protocol/land-sector-removals-2026.md) for ESRS E1 conformance, although applying it is best practice and is being increasingly expected by assurance providers. See the LSR Standard mapping for detail.

**4. Member state transposition matters.** Whether a Wave 1 company falling below the new Omnibus thresholds is exempted from FY 2025 / FY 2026 reporting depends on the relevant member state's transposition choices. National transposition is incomplete in most member states as of May 2026.

## Calculators on greencalculus.com that contribute to ESRS E1

This list will be populated as each calculator's ESRS mapping is verified. Essentially every Scope 1, Scope 2, and CSRD-mandatory Scope 3 calculator contributes:

- All Scope 1 stationary combustion calculators (E1-6 row 1)
- All Scope 1 mobile combustion calculators (E1-6 row 1)
- All Scope 1 fugitive emissions calculators including F-gas under [EU 2024/573](https://greencalculus.com/standards/f-gas-regulation-eu-2024/) (E1-6 row 1)
- All Scope 1 agriculture and land-sector calculators (E1-6 row 1; cross-references LSR Standard from 2027)
- All Scope 2 location-based electricity calculators (E1-6 row 2a)
- All Scope 2 market-based electricity calculators (E1-6 row 2b)
- All CSRD-mandatory Scope 3 category calculators 1, 2, 3, 4, 5, 6, 7, 11, 12 (E1-6 row 3)
- Energy consumption calculators (E1-5)
- Removals calculators (E1-7; LSR-aligned)

## Official sources

- [Corporate Sustainability Reporting Directive (CSRD) — official Commission page](https://finance.ec.europa.eu/capital-markets-union-and-financial-markets/company-reporting-and-auditing/company-reporting/corporate-sustainability-reporting_en)
- [Commission Delegated Regulation (EU) 2023/2772 — ESRS Set 1](https://eur-lex.europa.eu/eli/reg_del/2023/2772/oj)
- [Stop-the-Clock Directive (EU) 2025/794](https://eur-lex.europa.eu/eli/dir/2025/794/oj)
- [Omnibus I Directive (EU) 2026/470](https://eur-lex.europa.eu/eli/dir/2026/470/oj)
- [Quick Fix Delegated Regulation — November 2025](https://eur-lex.europa.eu/oj/direct-access.html)
- [EFRAG ESRS Technical Advice on simplification — December 2025](https://www.efrag.org/)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/csrd-esrs-e1/](https://greencalculus.com/standards/csrd-esrs-e1/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> European Commission (2023). *Commission Delegated Regulation (EU) 2023/2772 of 31 July 2023 supplementing Directive 2013/34/EU as regards sustainability reporting standards.* Official Journal of the European Union.

For the Omnibus I revision:

> European Parliament and Council of the European Union (2026). *Directive (EU) 2026/470 amending Directives 2006/43/EC, 2013/34/EU, (EU) 2022/2464 and (EU) 2024/1760 as regards corporate sustainability reporting and due diligence requirements.* Official Journal of the European Union, 26 February 2026.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-14
