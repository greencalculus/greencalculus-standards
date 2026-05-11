# TCFD Recommendations — Task Force on Climate-related Financial Disclosures

| Field | Value |
|---|---|
| **Initiative** | Task Force on Climate-related Financial Disclosures (TCFD) |
| **Operative version** | 2017 Final Recommendations + 2021 Implementation Guidance (frozen — TCFD disbanded 12 October 2023) |
| **Latest substantive update** | 2023 Status Report (12 October 2023) — final TCFD publication |
| **Next mandatory date** | None — superseded by IFRS S2 for most regulatory uses; some jurisdictions still reference TCFD for pre-2027 reporting |
| **Administered by** | Originally Financial Stability Board (FSB); monitoring responsibilities transferred to IFRS Foundation / ISSB from 1 January 2024 |
| **GreenCalculus stack layer** | Layer 6 — Disclosure |
| **Last reviewed** | 2026-05-15 |

---

## What this framework does

The Task Force on Climate-related Financial Disclosures (TCFD) was established in December 2015 by the Financial Stability Board, chaired initially by Michael Bloomberg. In June 2017, it published a set of voluntary climate-related financial disclosure recommendations structured around four core pillars: **Governance**, **Strategy**, **Risk Management**, and **Metrics and Targets**. These four pillars, together with 11 supporting recommended disclosures, became the de facto global framework for how companies disclose climate-related risks and opportunities in their financial filings.

The TCFD framework is no longer being actively developed. The Task Force published its sixth and final Status Report on 12 October 2023 and disbanded the same day, having "fulfilled its remit." Its work, recommendations, and supporting materials remain available as a public good (with proper attribution required), but the TCFD logo is retired and the supporter list is no longer maintained.

## Why TCFD is still relevant in 2026

Despite its formal disbanding, TCFD remains practically relevant for three reasons:

1. **It is the conceptual foundation of IFRS S2.** The ISSB's *IFRS S2 Climate-related Disclosures* fully incorporates the TCFD recommendations, retaining the same four-pillar structure. Companies preparing IFRS S2 disclosures are effectively meeting TCFD requirements.
2. **Many regulations still reference TCFD directly.** UK FCA listing rules, the UK Companies (Strategic Report) Climate-related Financial Disclosure Regulations 2022, Singapore MAS guidelines, New Zealand's Climate-related Disclosures regime, and Hong Kong Exchange's Climate Disclosure rules all reference TCFD by name. These references will gradually migrate to IFRS S2 as jurisdictions update their rules, but in 2026 many companies still file under TCFD-named rules.
3. **TCFD is the bridge for companies not yet on ISSB.** For organisations beginning their climate disclosure journey, the IFRS Foundation explicitly states that using TCFD recommendations remains "a good entry point" before adopting ISSB Standards.

In short: TCFD is no longer a living standard, but it is not yet a dead reference. It is in a managed sunset.

## Why it matters for GreenCalculus

TCFD disclosures rely heavily on quantitative metrics for Scope 1, 2, and 3 GHG emissions (the Metrics and Targets pillar), and on scenario analysis that requires emission factor data. GreenCalculus calculators directly supply both:

- **Metrics**: every Scope 1, 2, or 3 calculator produces output that can be dropped into a TCFD Metrics & Targets disclosure
- **Scenario analysis**: emission factors from the Master Brain (IEA grid factors, DEFRA, EPA eGRID) underpin transition risk modelling

Companies reporting under TCFD-named rules in the UK, Singapore, NZ, and other jurisdictions continue to use GreenCalculus calculator outputs for their Metrics & Targets section.

## The four pillars and 11 recommended disclosures

| Pillar | # | Recommended disclosure | GreenCalculus relevance |
|---|---|---|---|
| **Governance** | 1 | Board oversight of climate-related risks and opportunities | — |
| **Governance** | 2 | Management's role in assessing and managing climate-related risks | — |
| **Strategy** | 1 | Identified climate-related risks and opportunities (short, medium, long term) | — |
| **Strategy** | 2 | Impact of climate-related risks and opportunities on business, strategy, and financial planning | — |
| **Strategy** | 3 | Resilience of strategy under different climate scenarios (incl. 2°C or lower) | Emission factor data for scenario modelling |
| **Risk Management** | 1 | Processes for identifying and assessing climate-related risks | — |
| **Risk Management** | 2 | Processes for managing climate-related risks | — |
| **Risk Management** | 3 | Integration with overall enterprise risk management | — |
| **Metrics & Targets** | 1 | Metrics used to assess climate-related risks and opportunities | Energy and intensity metrics |
| **Metrics & Targets** | 2 | **Scope 1, 2, and (if appropriate) Scope 3 GHG emissions** | **Primary mapping — most calculators** |
| **Metrics & Targets** | 3 | Targets used to manage climate-related risks and performance against targets | Target tracking and SBTi-aligned tools |

The Metrics & Targets pillar — particularly disclosure 2 — is where GreenCalculus calculators most directly contribute. TCFD requires GHG emissions to be calculated in line with the GHG Protocol Corporate Standard, making the [Corporate Standard mapping](../ghg-protocol/corporate-standard.md) and [Scope 3 Standard mapping](../ghg-protocol/scope-3-standard.md) the upstream methodology references.

## TCFD vs IFRS S2 — the key differences

While IFRS S2 incorporates TCFD's structure wholesale, it is **not** a copy-and-paste. Key differences companies need to be aware of when transitioning:

| Area | TCFD | IFRS S2 |
|---|---|---|
| Status | Voluntary framework; many regulations reference it | Formal standard; basis for jurisdictional regulations |
| Scope 3 emissions | Optional ("if appropriate") | Required where material; financed emissions specifically required for financial institutions |
| Industry-specific metrics | General guidance only | Industry-specific disclosure requirements derived from SASB standards |
| Scenario analysis | Recommended ≥2°C scenario | More detailed requirements on scenario selection, assumptions, and disclosure |
| GHG methodology | GHG Protocol implied | GHG Protocol explicit (with limited jurisdictional flexibility from April 2025 Exposure Draft) |
| Materiality | Investor-focused | Investor-focused but more codified |
| Financial connectivity | Recommended | Required — sustainability disclosures must connect to financial statements |

The IFRS Foundation has published a [TCFD-to-IFRS-S2 comparison document](https://www.ifrs.org/sustainability/tcfd/) for companies mapping the transition.

## Jurisdictional adoption status (as of November 2025)

According to the IFRS Foundation Progress Report 2024 and Persefoni's jurisdictional tracking:

- **17 jurisdictions** have finalised decisions adopting ISSB Standards
- **16 additional jurisdictions** are in the process of developing final regulations
- **Most original TCFD-aligned regulations** are migrating to ISSB-based frameworks on a phased timeline

Notable adoption examples relevant to GreenCalculus users:

| Jurisdiction | Framework | Effective |
|---|---|---|
| United Kingdom | TCFD-aligned mandatory rules for premium listed entities and large private companies | In effect since 2022 |
| Singapore | MAS guidelines (TCFD-aligned) → ISSB-aligned phased | Ongoing migration |
| Hong Kong | HKEX Climate Disclosures based on ISSB Standards | All publicly accountable entities by 2028 |
| Malaysia | National Sustainability Reporting Framework (NSRF) based on ISSB | Phased 2024–2027 by size |
| Mexico | IFRS S1 + S2 mandatory for CNBV-supervised issuers | 2026 reporting (FY 2025 data) |
| New Zealand | Climate-related Disclosures (CRD) regime — TCFD-aligned | In effect since 2023 |
| United States (SEC) | SEC Climate Disclosure Rule | Stayed since April 2024 pending judicial review |
| EU | CSRD / ESRS E1 (covers TCFD areas plus more) | See [CSRD / ESRS E1 mapping](../eu/csrd-esrs-e1.md) |

The US picture remains in flux: the SEC issued an order to stay its Climate Disclosure Rule on 4 April 2024 pending judicial review, and that stay has continued through 2025–2026.

## The April 2025 IFRS S2 Exposure Draft

On 28 April 2025, the ISSB issued an Exposure Draft proposing targeted amendments to IFRS S2 to address practical challenges in disclosing financed emissions (Scope 3 Category 15). Key proposals:

- Relief from the requirement to measure and disclose emissions associated with derivatives and certain financial activities where data is unavailable
- More flexibility in classifying financed emissions by removing the mandatory use of the Global Industry Classification Standard (GICS)
- Permission to use jurisdiction-specific GHG measurement methodologies (and even older AR5 GWP values) where required by local regulations — instead of strict GHG Protocol + AR6 alignment

This is significant for GreenCalculus because it acknowledges that disclosure-layer frameworks cannot always mandate science-layer alignment in all jurisdictions. GreenCalculus retains both AR5 and AR6 GWP values in the Master Brain (§02 GWP) precisely to support this kind of jurisdictional flexibility.

## How GreenCalculus implements TCFD alignment

**Calculator outputs map directly to Metrics & Targets disclosure 2.** Every Scope 1, 2, and 3 calculator produces results in the format TCFD's Metrics & Targets pillar requires: disaggregated by scope, by category (for Scope 3), with disclosed GWP basis (AR6 default) and emission factor source.

**Scope 2 dual reporting.** TCFD references the GHG Protocol's Scope 2 dual reporting requirement (location-based and market-based). GreenCalculus surfaces both in line with the [Scope 2 Guidance](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/).

**Scenario analysis support.** While GreenCalculus does not produce scenario-modelled financial impacts directly, the Master Brain provides the emission factor data, regional grid factors, and intensity benchmarks that feed scenario modelling tools.

**Targets tracking.** Where companies have set TCFD-aligned targets (often SBTi-validated), GreenCalculus calculators surface progress data in formats compatible with TCFD's Metrics & Targets disclosure 3.

## Important caveats

A few points worth flagging:

**1. TCFD is in managed sunset, not abrupt termination.** Companies should not interpret "TCFD disbanded" as "TCFD references in regulation no longer apply." Most TCFD-named regulations will remain in force until they are formally updated to reference ISSB Standards. Companies preparing for FY 2025 or FY 2026 reporting under TCFD-named rules should continue to follow TCFD.

**2. The TCFD supporter list is no longer active.** Companies that previously listed themselves as TCFD supporters should now describe themselves as "aligned with TCFD recommendations" or "preparing for IFRS S2" — the formal supporter designation is no longer maintained.

**3. The 2023 Status Report is the final monitoring publication.** From 2024, monitoring of progress on climate-related disclosures is performed by the IFRS Foundation. The 2024 Progress Report published by IFRS in November 2024 is the successor to TCFD's annual Status Reports.

**4. Many companies in TCFD-named jurisdictions will need both.** A UK-listed company subject to the FCA's TCFD-aligned listing rules *and* preparing for ISSB adoption may need to produce TCFD-formatted disclosures in 2026 while building IFRS S2 capability for 2027 or 2028. GreenCalculus calculator outputs serve both formats without modification.

**5. GreenCalculus is not assurance.** A calculator producing TCFD-aligned figures does not discharge any limited or reasonable assurance obligation. The user remains responsible for documentation, audit trail, and engaging assurance providers as required by the relevant jurisdictional rules.

## Calculators on greencalculus.com that contribute to TCFD disclosures

Every Scope 1, Scope 2, and Scope 3 calculator on the platform produces output usable in a TCFD Metrics & Targets section. Specifically:

- All Scope 1 stationary, mobile, fugitive, and process emissions calculators (Metrics & Targets disclosure 2, row 1)
- All Scope 2 location-based and market-based electricity calculators (Metrics & Targets disclosure 2, row 2)
- All Scope 3 category calculators (Metrics & Targets disclosure 2, row 3, "if appropriate")
- Energy intensity and benchmark calculators (Metrics & Targets disclosure 1)
- SBTi-aligned target tracking tools (Metrics & Targets disclosure 3)

## Official sources

- [IFRS Foundation — ISSB and TCFD page](https://www.ifrs.org/sustainability/tcfd/)
- [IFRS Foundation — Progress on Corporate Climate-related Disclosures 2024 Report](https://www.ifrs.org/content/dam/ifrs/supporting-implementation/issb-standards/progress-climate-related-disclosures-2024.pdf)
- [Financial Stability Board — Climate-related disclosures progress reports](https://www.fsb.org/work-of-the-fsb/financial-innovation-and-structural-change/climate-related-financial-disclosures/)
- [TCFD 2023 Status Report (archival)](https://www.fsb-tcfd.org/publications)
- [IFRS S2 Climate-related Disclosures — official standard page](https://www.ifrs.org/issued-standards/ifrs-sustainability-standards-navigator/ifrs-s2-climate-related-disclosures.html)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this framework lives at:

**[greencalculus.com/standards/tcfd-recommendations/](https://greencalculus.com/standards/tcfd-recommendations/)**

That page is the canonical citation target for this framework mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> Task Force on Climate-related Financial Disclosures (2017). *Final Report: Recommendations of the Task Force on Climate-related Financial Disclosures.* Financial Stability Board, June 2017.

For the implementation guidance:

> Task Force on Climate-related Financial Disclosures (2021). *Implementing the Recommendations of the Task Force on Climate-related Financial Disclosures.* Financial Stability Board, October 2021.

For the final status report:

> Task Force on Climate-related Financial Disclosures (2023). *2023 Status Report.* Financial Stability Board, 12 October 2023.

For the IFRS-led successor framework:

> IFRS Foundation (2023). *IFRS S2 Climate-related Disclosures.* International Sustainability Standards Board, June 2023.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-15
