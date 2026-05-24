# RE100 — Technical Criteria

| Field | Value |
|---|---|
| **Initiative** | RE100 — global corporate renewable electricity initiative |
| **Operative version** | RE100 Technical Criteria — **September 2024 revision** (latest substantive update) |
| **Latest substantive update** | September 2024 — tightened market boundary, vintage, and additionality provisions; new geographic granularity rules |
| **Next mandatory date** | Aligned with the GHG Protocol [Scope 2 Guidance revision](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/) (targeted late 2027) — RE100 will issue an updated criteria revision after the Scope 2 final is published |
| **Administered by** | Climate Group, in partnership with CDP |
| **GreenCalculus stack layer** | Layer 5 — Target setting (renewable-electricity-specific) |
| **Last reviewed** | 2026-05-25 |

---

## What this initiative does

RE100 is the global corporate initiative under which member companies publicly commit to **sourcing 100% of their electricity from renewable sources by 2050 at the latest**. Launched in 2014 by The Climate Group in partnership with CDP, RE100 has grown to over 430 member companies as of 2025–2026, collectively representing over 380 TWh of annual electricity demand — more than the total annual electricity consumption of countries such as Poland or the Netherlands.

The **RE100 Technical Criteria** is the operational document that defines what counts as a "renewable electricity" claim eligible for RE100 reporting purposes. It is structurally an extension of, and aligned with, the [GHG Protocol Scope 2 Guidance](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/) market-based method — but it adds RE100-specific rules around eligible technologies, market boundaries, vintage, and reporting.

The Technical Criteria has undergone multiple revisions since 2014, with the most consequential being the September 2024 update which tightened market boundary requirements and aligned more closely with the in-progress GHG Protocol Scope 2 revision.

## Why it matters for GreenCalculus

For companies pursuing or already committed to RE100, the Technical Criteria defines:

1. **What renewable electricity counts** — which technologies, vintages, and contractual instruments qualify.
2. **Geographic boundaries** — where the generation must be located relative to the consumption.
3. **Market-based reporting** — how the company calculates and reports its progress toward 100%.

GreenCalculus Scope 2 calculators directly support RE100 reporting by surfacing:

- The location-based vs market-based Scope 2 split required by the underlying GHG Protocol Scope 2 Guidance
- Renewable share calculation under both methods
- Eligibility flags for the principal contractual instruments (PPAs, EACs, green tariffs) that the Technical Criteria treats differently

For companies *considering* an RE100 commitment, the GreenCalculus calculator output also serves as the baseline against which the 100% pathway is planned.

## The four headline requirements

| Requirement | Detail |
|---|---|
| **100% renewable electricity by 2050 at the latest** | Public, dated commitment to reach 100% by a specified year ≤ 2050 |
| **Interim milestones** | 60% by 2030, 90% by 2040 (or earlier — many members commit to faster trajectories) |
| **Annual disclosure** | Annual reporting via CDP, including renewable electricity volumes, instruments used, and progress against the commitment |
| **RE100 Technical Criteria conformance** | All claimed renewable electricity must conform to the Technical Criteria's eligibility, market boundary, vintage, and instrument rules |

## What counts as renewable — eligible technologies

The Technical Criteria covers the following generation types:

| Technology | Eligible | Notes |
|---|---|---|
| **Solar PV** (utility-scale, distributed, building-integrated) | Yes | Standard inclusion |
| **Onshore wind** | Yes | Standard inclusion |
| **Offshore wind** | Yes | Standard inclusion |
| **Geothermal** | Yes | Standard inclusion |
| **Sustainably-sourced biomass** | Yes (with conditions) | Must meet sustainability criteria; cofiring constraints |
| **Sustainably-sourced biogas** | Yes (with conditions) | Sustainability criteria; agricultural and waste-derived feedstocks |
| **Sustainably-sourced hydropower** | Yes (with conditions) | Subject to size and location sustainability tests |
| **Marine / wave / tidal** | Yes | Standard inclusion |
| **Green hydrogen / power-to-gas-to-power** | Case-by-case | Emerging technology pathway |
| **Nuclear** | **No** | Not currently eligible under RE100; this is a frequently misunderstood point |
| **Fossil with CCS** | **No** | Not eligible regardless of CO₂ capture |

The nuclear exclusion has been controversial — particularly given some carbon-neutral or 24/7 carbon-free energy frameworks (e.g. Google's 24/7 CFE) treat nuclear as on-par with renewables. The RE100 position is that nuclear is *carbon-free* but not *renewable*, and the initiative is explicitly about renewable energy.

## Market boundary rules — September 2024 update

The most consequential element of the 2024 revision was the tightening of **market boundary rules** — where the claimed renewable generation must be located relative to the consumption.

The principle is that a renewable claim should reflect a meaningful market connection between the generation and the consumption. Generation in a market with no physical or commercial link to the consumption point cannot credibly be claimed by that consumer.

| Market boundary level | Detail |
|---|---|
| **Same physical electricity grid** | Generation must be connected to the same grid as the consumption (e.g. for the EU, the European synchronous grid) |
| **Same country or sub-national region** | Preferred where the grid covers multiple regulatory jurisdictions |
| **Cross-border within market region** | Permitted where there is a recognised market mechanism (e.g. EU AIB system for cross-border GO trading) |
| **Across continents** | **Not permitted** for new claims — closes the "globally sourced REC" loophole that historically allowed e.g. US companies to buy Indian or Brazilian RECs against US consumption |

The 2024 revision phased out previously-permitted cross-continental EAC purchases for new claims. Existing long-term contracts signed before the revision are subject to a transitional period (typically until 2030) but new claims must comply with the tighter boundary rules.

This change matters for GreenCalculus users planning a renewable procurement strategy: I-REC purchases from India or Brazil, for instance, cannot be applied against North American or European consumption under the 2024 criteria.

## Vintage rules

Renewable energy attribute certificates (EACs) — RECs in the US, GOs in the EU, I-RECs in many emerging markets — represent generation in a specific time period. The vintage rule sets how recent that generation must be relative to the claim:

| Vintage rule | Application |
|---|---|
| **EACs issued in the consumption year** | Strongly preferred |
| **EACs from prior 6 months or following 3 months** | Permitted under a 12-month window centred on the consumption period |
| **EACs older than 12 months from consumption** | Not eligible — vintage gap too wide |

This contrasts with some EAC markets historically operating on a 24-month or even open-ended basis. The vintage tightening prevents companies from "banking" pre-existing surplus certificates against future consumption claims.

## Geographic granularity and 24/7 carbon-free energy

The 2024 Technical Criteria revision moved toward greater geographic granularity. While RE100 has not yet mandated hourly matching (this is a future direction as the [Scope 2 Guidance revision](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/) progresses), the September 2024 update encouraged members to disclose:

- Annual matching status (current standard)
- Sub-annual matching where data permits (monthly, weekly)
- Hourly or sub-hourly matching for advanced members

This positions RE100 as a transitional standard between purely annual matching (the historical norm) and the hourly matching paradigm associated with the broader 24/7 Carbon-Free Energy (CFE) movement.

GreenCalculus tracks 24/7 CFE-aligned calculators separately because the methodology (hourly matching against hourly grid factors) differs structurally from the RE100 annual matching framework — but the platform supports both.

## Eligible contractual instruments

The Technical Criteria recognises four broad categories of contractual instrument:

| Instrument | Detail | Typical use |
|---|---|---|
| **Self-generation** | Renewable electricity generated on-site or directly behind-the-meter | Rooftop solar, wind, on-site biomass |
| **Power Purchase Agreements (PPAs)** | Direct, virtual, or sleeved PPAs with renewable generators | Corporate PPAs (largest single growth area) |
| **Green tariffs** | Supplier-provided renewable-electricity tariffs backed by EACs | Utility green-power programmes |
| **Unbundled EACs** | Renewable Energy Certificates (RECs), Guarantees of Origin (GOs), I-RECs, and equivalent | Standalone EAC purchases not linked to physical energy delivery |

The hierarchy in practice tracks the GHG Protocol Scope 2 quality hierarchy: self-generation > PPAs > green tariffs > unbundled EACs. The 2024 revision did not change the relative quality ordering but did tighten the eligibility tests for unbundled EACs.

## How GreenCalculus implements RE100 alignment

**Scope 2 dual reporting.** Every electricity calculator surfaces location-based and market-based results per the [Scope 2 Guidance](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/). The market-based result is the basis for RE100 progress reporting.

**Renewable share calculation.** Calculators that accept contractual-instrument inputs (PPAs, green tariffs, EACs) produce both a Scope 2 MBM emissions number *and* a renewable percentage in the underlying electricity mix — directly usable as RE100 progress data.

**Market boundary tagging.** Every EAC and PPA contract input carries a market region tag (country, grid region) so the calculator can flag whether the contractual instrument is within the RE100 market boundary for the consumption location.

**Vintage tagging.** Contractual instruments are tagged with their generation vintage, supporting compliance with the 12-month window rule.

**Eligibility flags.** Where a user inputs a contractual instrument that does not meet RE100 eligibility (cross-continental, wrong vintage, ineligible technology like nuclear), the calculator surfaces a non-blocking warning.

**Trajectory modelling.** Calculators support modelling a company's renewable trajectory against the RE100 interim milestones (60% by 2030, 90% by 2040, 100% by 2050).

## Relationship with other standards

RE100 sits within the broader Scope 2 standards stack:

| Related standard | Relationship |
|---|---|
| [GHG Protocol Scope 2 Guidance](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/) | Upstream methodology — RE100 builds on the market-based method |
| [GHG Protocol Corporate Standard](../ghg-protocol/corporate-standard.md) | Overall corporate inventory frame |
| [SBTi Corporate Net-Zero](./sbti-corporate-net-zero.md) | RE100 commitment supports Scope 2 reduction under SBTi |
| [CSRD / ESRS E1](../eu/csrd-esrs-e1.md) | Renewable electricity sourcing is an ESRS E1 mandatory disclosure point |
| [TCFD / IFRS S2](../disclosure/tcfd-recommendations.md) | RE100 progress disclosed in the Metrics & Targets pillar |
| 24/7 Carbon-Free Energy Compact | RE100 is annual-matching today; 24/7 CFE is hourly — distinct but compatible |

## Important caveats

A few points worth flagging:

**1. RE100 is electricity-only.** The commitment covers purchased electricity (Scope 2). It does not cover heat, cooling, steam, or any fuel-based energy. Companies seeking renewable thermal energy targets should consider the related EP100 initiative or set separate thermal-energy targets.

**2. Renewable ≠ zero emissions in physical terms.** A 100% RE100 company still draws power from a grid that may be partially fossil-generated at any given hour. The 100% claim is a *market-based* accounting outcome, not a physical statement about the kilowatt-hours that flowed through the meter. This is the same LBM/MBM tension that drives the broader Scope 2 debate.

**3. The 2024 market boundary tightening is consequential.** Companies that historically met their RE100 commitment via cross-continental I-REC purchases may need to re-source. The transitional grace period for existing contracts is generous but not indefinite. GreenCalculus surfaces market-boundary status to support re-sourcing planning.

**4. Nuclear exclusion is firm.** Companies seeking 24/7 carbon-free energy frameworks that include nuclear (e.g. Google's CFE programme, several US utility tariffs) cannot directly claim those volumes against RE100. RE100 and CFE are complementary but distinct.

**5. RE100 is voluntary.** Like SBTi, RE100 is a voluntary corporate initiative. Membership can be withdrawn (Microsoft, Walmart, and several others have publicly revisited prior renewable commitments in 2024–2025). Validation is via annual CDP disclosure; there is no third-party assurance requirement built into the framework, though many members pursue [ISO 14064-3 verification](../iso/14064-1-organisation-ghg-quantification.md) voluntarily.

**6. GreenCalculus is not RE100 certification.** Calculator outputs methodologically support RE100 reporting but do not substitute for the annual CDP disclosure that constitutes RE100 reporting itself.

## Calculators on greencalculus.com that support RE100

Every Scope 2 electricity calculator on the platform supports RE100 progress reporting. Specifically helpful:

- All location-based and market-based Scope 2 electricity calculators
- PPA modelling calculators (corporate PPA, virtual PPA, sleeved PPA)
- Renewable share / RE100 progress trackers
- EAC purchase calculators (REC, GO, I-REC)
- Self-generation Scope 2 calculators (rooftop solar, on-site wind)
- Green tariff Scope 2 calculators
- Multi-year RE100 trajectory tools (60% / 90% / 100% milestone tracking)

## Official sources

- [RE100 — official site](https://www.there100.org/)
- [RE100 Technical Criteria (September 2024 revision)](https://www.there100.org/re100-technical-criteria)
- [RE100 Annual Report and member list](https://www.there100.org/our-work/publications)
- [Climate Group — RE100 page](https://www.theclimategroup.org/re100)
- [CDP disclosure platform](https://www.cdp.net/) (annual RE100 reporting channel)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this initiative lives at:

**[greencalculus.com/standards/re100-technical-criteria/](https://greencalculus.com/standards/re100-technical-criteria/)**

That page is the canonical citation target for this initiative mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> Climate Group and CDP (2024). *RE100 Technical Criteria, September 2024 Revision.* The Climate Group, London.

For the annual disclosure context:

> Climate Group and CDP (2024). *RE100 Annual Disclosure Report 2024.* The Climate Group, London.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-25
