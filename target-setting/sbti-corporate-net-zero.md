# SBTi Corporate Net-Zero Standard

| Field | Value |
|---|---|
| **Initiative** | Science Based Targets initiative (SBTi) |
| **Operative version** | Corporate Net-Zero Standard **v1.2** (April 2024); v2.0 in development — public consultation completed December 2025 |
| **Latest substantive update** | v1.2 (April 2024) — clarifications on residual emissions and beyond-value-chain mitigation (BVCM); v1.1 (April 2023) updated FLAG sector criteria |
| **Next mandatory date** | v2.0 expected publication in late 2026 or early 2027 following the December 2025 consultation; phased adoption to follow |
| **Administered by** | Science Based Targets initiative — a partnership of CDP, the UN Global Compact, World Resources Institute (WRI), and the World Wide Fund for Nature (WWF) |
| **GreenCalculus stack layer** | Layer 5 — Target setting |
| **Last reviewed** | 2026-05-25 |

---

## What this standard does

The SBTi Corporate Net-Zero Standard is the leading global framework for **companies setting science-aligned net-zero targets**. It specifies what a corporate net-zero commitment must include to be consistent with limiting global warming to **1.5°C** above pre-industrial levels, and provides the validation methodology against which SBTi assesses company target submissions.

Where corporate climate frameworks until 2021 generally focused on near-term emission reduction targets (typically 5–10 year horizons), the Net-Zero Standard codified the longer-horizon requirement: a credible net-zero target requires both near-term reductions (≥42% by 2030) *and* long-term reductions (≥90% by 2050, with the remaining ≤10% neutralised via permanent carbon removals).

It is the first standardised, validated framework for corporate net-zero targets aligned with the IPCC's 1.5°C pathways, and as of May 2026 has over 9,000 companies with science-based targets, of which ~7,200 have commitments validated against the Net-Zero Standard specifically.

## Why it matters for GreenCalculus

GreenCalculus calculator outputs are the **primary quantitative input** to an SBTi target-setting and progress-tracking exercise:

1. **Baseline year inventory.** SBTi target validation requires a recent base-year inventory covering Scope 1, 2, and (in most cases) Scope 3 emissions, calculated to the [GHG Protocol Corporate Standard](../ghg-protocol/corporate-standard.md) and [Scope 3 Standard](../ghg-protocol/scope-3-standard.md). Calculator outputs feed this directly.
2. **Annual progress tracking.** Companies with validated SBTi targets must publish annual progress against their targets. Calculator outputs provide the year-by-year emissions trajectory.
3. **Sector-specific pathways.** SBTi maintains 1.5°C-aligned absolute and intensity pathways for several sectors (power, FLAG, buildings, transport, steel, aluminium, cement, financial institutions). GreenCalculus surfaces target trajectories against these where applicable.

For companies committed to SBTi targets — and for those preparing to commit — calculator architecture must align with how SBTi expects emissions to be measured, classified, and tracked.

## The core requirements of v1.2

### Near-term targets (5–10 year horizon)

| Requirement | Detail |
|---|---|
| **Scope 1+2 absolute reduction** | At least **42% absolute reduction by 2030** vs base year (1.5°C-aligned pathway); intensity targets accepted only with simultaneous demonstration of absolute reductions |
| **Scope 3 coverage threshold** | Required where Scope 3 is ≥40% of total Scope 1+2+3 emissions |
| **Scope 3 reduction ambition** | At least **25% absolute reduction** (well-below 2°C-aligned) or supplier engagement target covering most-significant categories |
| **Base year** | Recent (typically within five years of submission); company can update base year following structural changes per the GHG Protocol |
| **Target year** | 5–10 years from submission |

### Long-term targets (net-zero by 2050 at the latest)

| Requirement | Detail |
|---|---|
| **Scope 1+2+3 absolute reduction** | At least **90% absolute reduction by 2050** vs base year, or earlier net-zero target year |
| **Cross-scope coverage** | Net-zero targets must cover all three scopes (with limited exclusions for emissions deemed truly residual) |
| **Residual emissions neutralisation** | The remaining ≤10% must be neutralised via **permanent carbon removals** (geological storage, mineralised, or durable biogenic) — *not* avoided-emissions offsets |
| **Beyond-value-chain mitigation (BVCM)** | Companies are *encouraged but not required* to fund mitigation outside the value chain (e.g. nature-based solutions, frontier removals) to address residual emissions during the transition — this is supplementary to the science-based pathway, not a substitute |

### Forest, Land and Agriculture (FLAG) sector requirements

FLAG sectors (food, agriculture, forestry, and other land-use intensive sectors) face additional requirements under the FLAG Guidance (v1.2 incorporated):

- Separate FLAG vs non-FLAG target submission
- Specific FLAG emission reduction pathway aligned with the Land Sector and Removals Standard
- Removals included on a no-net-deforestation basis from 2025

This sectoral specificity is why [GHG Protocol Land Sector and Removals Standard (2026)](../ghg-protocol/land-sector-removals-2026.md) and SBTi FLAG criteria are operationally interlinked.

## The v2.0 consultation — what's likely changing

The v2.0 public consultation period ran from **March 2025 to 1 December 2025**. The proposed revisions are the most substantive since the Standard's 2021 launch. Headline directions in the consultation draft:

| Area | Proposed direction |
|---|---|
| **Scope 3 coverage thresholds** | Lower thresholds for inclusion; potential category-level rather than aggregate ambition requirements |
| **Beyond-value-chain mitigation (BVCM)** | More explicit role — including possible quantified requirements for high-emitting companies |
| **Residual emissions** | Tighter definition of what counts as "residual"; harder constraint on the size of the residual share |
| **Carbon removals** | Expanded role and clearer hierarchy; potential interim use of high-quality carbon credits for hard-to-abate residuals |
| **Sector-specific pathways** | More sector pathways with mandatory use for in-sector companies |
| **Financial institutions** | Separate evolving framework |
| **Categorisation of company types** | Differentiated requirements for small vs large companies; harder requirements for fossil fuel companies |
| **Net-zero timing flexibility** | Pre-2050 net-zero pathways recognised more formally; later-than-2050 pathways tightened or refused |
| **Insetting** | Clearer position on insetting (in-value-chain interventions credited to specific buyers) |
| **Validation cadence** | Mandatory periodic re-validation cycle for validated targets |

The v2.0 final standard is expected in **late 2026 or early 2027**, with a phased adoption window for companies with v1.x validated targets to transition.

GreenCalculus is tracking the consultation outputs because several v2.0 directions — particularly around Scope 3 category-level ambition, FLAG removals accounting, and residual emissions definitions — will require Master Brain data layer updates and calculator surfacing changes.

## The "Net-Zero" definition — and why it's not interchangeable

SBTi's net-zero definition is more constrained than colloquial usage:

> **A state in which company-wide value-chain emissions have been reduced to a level that is consistent with 1.5°C pathways (at least 90% of base year emissions), with the remaining residual emissions neutralised by permanent removals within the corresponding period.**

Three points worth emphasising:

1. **Net-zero ≠ carbon neutral.** "Carbon neutral" typically allows full reliance on offsets, including avoided-emissions offsets, and does not require deep reductions. SBTi net-zero requires actual emissions to fall by at least 90% before neutralisation.
2. **Removals ≠ offsets.** Permanent carbon removals (geological CO₂ storage, mineralised carbon, durable biochar, long-lived afforestation) physically remove CO₂ from the atmosphere. Most "carbon offsets" historically used are *avoided-emissions* credits (renewable energy, avoided deforestation, methane destruction) — these are not removals and cannot be used to neutralise residual emissions under SBTi.
3. **The 90% / 10% split is hard.** A company cannot claim net-zero by relying more heavily on removals; the 90% reduction floor is the gate.

## SBTi categorisations and exclusions

Not every company can set an SBTi target. Key restrictions:

| Sector / company type | Status |
|---|---|
| Fossil fuel companies | Validation paused since November 2022 pending dedicated framework — Oil, Gas and Integrated Energy framework consulted in 2024/2025; status remains evolving |
| Tobacco | Excluded from SBTi |
| Companies in conflict regions | Case-by-case review |
| Financial institutions | Separate sector framework (Financial Sector Net-Zero Standard) |
| Small companies (under specific thresholds) | Streamlined SME route available |

GreenCalculus does not prevent fossil-fuel or tobacco companies from using its calculators for internal carbon accounting; the SBTi restrictions apply only to *target validation*, not to underlying inventory work.

## How GreenCalculus implements SBTi alignment

**Base year and trajectory tracking.** Calculators support specifying a base year and surfacing year-over-year emissions deltas in absolute and intensity-normalised forms — directly usable for SBTi base-year inventory and annual progress reporting.

**Scope 3 category-level breakdown.** Scope 3 calculators tag results to one of the 15 Scope 3 categories per the [GHG Protocol Scope 3 Standard](../ghg-protocol/scope-3-standard.md). This is the granularity SBTi v2.0 is moving toward.

**FLAG vs non-FLAG separation.** Agriculture and forestry-linked calculators (FLAG sector) are tagged separately from non-FLAG so users with FLAG exposure can submit FLAG-specific targets.

**Residual vs non-residual emissions.** Calculator outputs surface which sources are likely to be reducible (energy, fleet, refrigerants) vs harder-to-abate (process emissions, certain agricultural and aviation sources), aiding the analytical work of defining residual share.

**Sector pathway visualisation.** Where SBTi publishes a sector-specific 1.5°C pathway (power, buildings, transport, FLAG, steel, aluminium, cement), the calculator emissions trajectory can be overlaid for visual progress assessment.

**AR6 GWP-100 throughout.** All CO₂e calculations use [AR6 GWP-100](../ipcc/ar6-gwp-100.md), consistent with [GHG Protocol Corporate Standard (2026 revision)](../ghg-protocol/corporate-standard.md) and SBTi's current GWP basis.

## Relationship with other standards

SBTi target validation depends on multiple upstream standards:

| Upstream standard | Relationship |
|---|---|
| [GHG Protocol Corporate Standard](../ghg-protocol/corporate-standard.md) | Required methodology for base year and progress inventories |
| [GHG Protocol Scope 3 Standard](../ghg-protocol/scope-3-standard.md) | Required methodology for Scope 3 target coverage |
| [GHG Protocol LSR 2026](../ghg-protocol/land-sector-removals-2026.md) | Methodological basis for FLAG sector targets |
| [ISO 14064-1](../iso/14064-1-organisation-ghg-quantification.md) | Verification framework — many SBTi companies have inventories verified to 14064-1 |
| [CSRD / ESRS E1](../eu/csrd-esrs-e1.md) | SBTi-aligned targets satisfy several ESRS E1 transition-plan disclosure points |
| [RE100](./re100-technical-criteria.md) | 100% renewable electricity commitment that supports Scope 2 reduction within SBTi |
| [TCFD / IFRS S2](../disclosure/tcfd-recommendations.md) | SBTi-validated targets disclosed in the Metrics & Targets pillar |

## Important caveats

A few points worth flagging:

**1. SBTi commits the company, not the brand.** A validated target covers the corporate entity's operational and value-chain emissions as a whole. Brand-level or product-level "net-zero" claims that do not cover the parent company at the SBTi-required ambition are not SBTi-validated.

**2. Validation is not certification of achievement.** SBTi validates that a *target* is science-aligned. It does not certify that a company has *met* its target. Annual progress reporting and (under v2.0) periodic re-validation are the accountability mechanism.

**3. The 1.5°C pathway is the only currently accepted ambition.** SBTi retired the "well-below 2°C" pathway for Scope 1+2 in 2022; only 1.5°C-aligned near-term targets are accepted. Scope 3 retains a "well-below 2°C" option for some companies under v1.2 but this is expected to tighten in v2.0.

**4. Avoided-emissions offsets cannot substitute for reductions.** A company cannot claim SBTi compliance by purchasing avoided-emissions credits. The 42% near-term and 90% long-term reduction floors are *absolute*. Removals (and only permanent removals) play a role only in neutralising the residual ≤10%.

**5. SBTi is voluntary.** Unlike CSRD, IFRS S2, or national mandatory disclosure regimes, SBTi is a voluntary commitment scheme. A company may publicly commit, then withdraw — and several have (including Microsoft and Walmart's partial reductions in 2024–2025 from prior SBTi commitments). For external auditors and investors, an SBTi commitment is signal but not enforceable obligation.

**6. GreenCalculus is not an SBTi target validator.** Calculator outputs feed an SBTi submission but do not constitute one. Submission, validation, annual progress, and re-validation are handled directly through the SBTi platform.

## Calculators on greencalculus.com that support SBTi alignment

Every Scope 1, Scope 2, and Scope 3 calculator on the platform produces output usable in an SBTi base-year inventory and annual progress report. Specifically helpful for SBTi work:

- Multi-year emissions trajectory calculators (base year vs current year vs target year)
- Scope 3 category-by-category breakdown calculators (Cat. 1–15)
- FLAG sector-specific calculators (agriculture, forestry, land use)
- Sector pathway visualisation tools (power, buildings, transport, cement, steel, aluminium)
- Removals calculators (afforestation, soil carbon, technological removals) — supporting residual neutralisation modelling
- Intensity-normalised calculators (per unit production, per FTE, per revenue) for SBTi intensity targets

## Official sources

- [Science Based Targets initiative — official site](https://sciencebasedtargets.org/)
- [Corporate Net-Zero Standard v1.2 (April 2024)](https://sciencebasedtargets.org/net-zero)
- [Net-Zero Standard v2.0 — Consultation page](https://sciencebasedtargets.org/standard-development)
- [SBTi FLAG Guidance](https://sciencebasedtargets.org/sectors/forest-land-and-agriculture)
- [SBTi Target Dashboard](https://sciencebasedtargets.org/target-dashboard)
- [Beyond Value Chain Mitigation (BVCM) Position Paper](https://sciencebasedtargets.org/resources)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/sbti-corporate-net-zero-standard/](https://greencalculus.com/standards/sbti-corporate-net-zero-standard/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> Science Based Targets initiative (2024). *Corporate Net-Zero Standard, Version 1.2.* SBTi, April 2024.

For FLAG-specific guidance:

> Science Based Targets initiative (2023). *Forest, Land and Agriculture Science Based Target-Setting Guidance, Version 1.1.* SBTi, April 2023.

For the consultation draft of v2.0:

> Science Based Targets initiative (2025). *Corporate Net-Zero Standard, Version 2.0 — Public Consultation Draft.* SBTi, public consultation period March 2025 – 1 December 2025.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-25
