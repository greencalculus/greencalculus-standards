# GHG Protocol Scope 2 Guidance

| Field | Value |
|---|---|
| **Initiative** | GHG Protocol (WRI / WBCSD) — amendment to the [Corporate Standard](./corporate-standard.md) |
| **Operative version** | Scope 2 Guidance (2015) — still in effect as of May 2026 |
| **Latest substantive update** | Public consultation period closed 31 January 2026; ISB approval of revisions for consultation 14 July 2025 |
| **Next mandatory date** | Final revised Scope 2 Guidance targeted late 2027, with multiyear phased implementation thereafter |
| **Administered by** | World Resources Institute (WRI) and World Business Council for Sustainable Development (WBCSD), via the Scope 2 Technical Working Group |
| **GreenCalculus stack layer** | Layer 2 — Calculation (electricity / purchased energy) |
| **Last reviewed** | 2026-05-20 |

---

## What this guidance does

The GHG Protocol Scope 2 Guidance, published in January 2015 as an amendment to the [Corporate Standard](./corporate-standard.md), is the global framework for how companies measure and report greenhouse gas emissions from **purchased electricity, steam, heat, and cooling**. It introduced the **dual reporting requirement** — that companies must report Scope 2 emissions using both the **location-based method** (LBM, regional grid average) *and* the **market-based method** (MBM, contractual instruments like renewable energy certificates, power purchase agreements, and supplier-specific factors).

The Scope 2 Guidance is the basis for how virtually every major reporting framework treats purchased energy emissions — CSRD, ISSB IFRS S2, TCFD, CDP, SBTi, and California SB 253 all reference it. When a company claims "100% renewable electricity" or "carbon-free energy", that claim is being made under the rules this guidance defines.

It is currently in the most consequential revision of its history.

## Why it matters for GreenCalculus

Electricity is typically the largest single category of corporate emissions outside Scope 1 fuel combustion. For technology, financial services, retail, and most office-based industries, Scope 2 dominates the reporting picture. The methodology used — location-based vs market-based — can change a reported number by 80% or more, particularly for companies with significant renewable energy procurement.

Every GreenCalculus electricity calculator surfaces both LBM and MBM results because the Scope 2 Guidance requires dual reporting. The Master Brain data layer maintains regional grid emission factors (from IEA Global Energy Review 2026, EPA eGRID, and equivalent national datasets) for the location-based method, and supports user-provided contractual factors for the market-based method.

The forthcoming revision — which would require hourly matching for many voluntary clean energy claims — would substantially change how those calculations are performed and presented. GreenCalculus is tracking the revision closely because it will require structural changes to how MBM calculators handle temporal granularity.

## The two methods — current (2015) framework

### Location-based method (LBM)

Reports emissions using the **average emissions intensity of the grid** where the electricity is consumed. The factor is regional (or national) and reflects what was actually generated and consumed on that grid in the reporting year.

| Method | Data source | Typical use |
|---|---|---|
| **Subregional grid factors** | EPA eGRID (US), national grid operators (EU), provincial datasets (China, India) | Most accurate available |
| **National grid factors** | IEA Global Energy Review, national inventories | Used where subregional unavailable |
| **Continental / generic factors** | IEA, IPCC defaults | Fallback only |

LBM tells you what the *physical electricity system* actually emitted to serve your demand. It does not credit your renewable procurement.

### Market-based method (MBM)

Reports emissions using **contractual instruments** that document the supplier-specific or contracted emissions associated with the electricity. The market-based method allows companies to receive accounting credit for renewable energy procurement.

Acceptable contractual instruments (in the 2015 hierarchy):

1. **Energy attribute certificates (EACs)** — RECs (US), Guarantees of Origin (EU), GO-equivalent national schemes
2. **Contracts** — power purchase agreements (PPAs), green tariffs
3. **Supplier-specific emission rates** — disclosed by the utility
4. **Residual mix factors** — what's left in the grid after EACs and other instruments are subtracted
5. **Other grid-average factors** — fallback only

A company that purchases 100% renewable EACs can report **zero MBM Scope 2 emissions** from electricity — even if the physical grid serving that company is still 50% coal. This is the core of the LBM/MBM divergence and the source of most current controversy.

## Dual reporting — why both are required

The 2015 Scope 2 Guidance mandates that companies report **both methods** when they are operating in a market with contractual instruments. This is not optional: a company cannot simply report MBM (which often looks better) and omit LBM. The reasoning is that:

- **LBM** tells stakeholders what the company's electricity demand actually drove in physical emissions
- **MBM** tells stakeholders what climate-related contractual choices the company made

Both are valuable; neither alone is complete. Most disclosure frameworks (CSRD, IFRS S2, TCFD, CDP) require both.

## The 2025–2026 revision — what's changing

The Scope 2 Guidance has been substantively unchanged since 2015. After more than a decade of practitioner feedback — particularly around the integrity of unbundled REC claims, the rise of corporate PPAs, and the growing concern that annual matching obscures the real climate impact of clean energy procurement — the GHG Protocol convened a Scope 2 Technical Working Group to draft revisions.

Process status as of May 2026:

- **14 July 2025** — ISB voted to approve proposed revisions for public consultation (10 yes, 1 no on both LBM and MBM revisions)
- **20 October 2025** — 60-day public consultation period opened
- **31 January 2026** — Public consultation period closed (extended from original 19 December 2025 deadline)
- **Late 2027** — Final revised Scope 2 Guidance targeted for publication
- **Multiyear phased implementation** anticipated thereafter

### Proposed changes to the location-based method

| Change | What it does |
|---|---|
| **New emission factor hierarchy** | Prioritises the most accurate available factor — typically subregional > national > continental |
| **Accessibility requirement** | The detailed factor must be free and publicly accessible to be required — companies aren't forced to pay for commercial datasets |
| **"Accessible data" defined** | A formal definition replaces ambiguity about what counts as available |
| **Temporal precision** | Hourly or sub-annual factors required only where the underlying data is publicly available |

### Proposed changes to the market-based method

This is where the substantive controversy lives.

| Change | What it does |
|---|---|
| **Hourly matching requirement** | EACs must be matched to electricity consumption **on an hourly basis** — but only when the company is making a voluntary clean energy claim |
| **Deliverability requirement** | EACs must come from a generator on a grid that physically delivers power to the consumption location |
| **New emission factor hierarchy** | Tightens the order: supplier-specific → contracts → EACs → residual mix → fossil-only defaults |
| **Residual mix more prescriptive** | Where unclaimed energy exists, it must default to residual mix or fossil-only — closing some current loopholes |
| **Estimated hourly data permitted** | Companies don't need real-time meters; they can use load profiles applied to monthly/annual consumption |

### Feasibility measures (the "softening" provisions)

The revision includes several measures intended to reduce implementation burden, all of which are politically important:

| Provision | What it does |
|---|---|
| **Hourly matching exemption threshold** | Smaller organisations exempted from hourly matching requirements |
| **Legacy clause** | Existing long-term contracts (PPAs signed before revision adoption) can continue under annual matching for their original term |
| **Load profiles permitted** | Companies can use estimated hourly profiles where real-time data unavailable |
| **Phased multi-year implementation** | Compliance phased over multiple years rather than abrupt switch |

### Parallel consultation — avoided emissions

Alongside the Scope 2 revision, the GHG Protocol consulted on **consequential accounting methods for estimating avoided emissions** from electricity-sector actions. This is separate from Scope 2 inventory accounting (which is attributional). Avoided emissions accounting will inform subsequent work under the Actions and Markets Instruments (AMI) workstream.

## The hourly matching debate

The proposed hourly matching requirement is the single most contested element of the revision. The debate splits broadly:

**In favour of hourly matching:**

- Closes the gap between *claimed* and *delivered* clean energy — a company can claim 100% renewable on an annual basis while still drawing fossil power at night
- Drives investment in batteries, demand response, and 24/7 carbon-free energy
- Aligns corporate claims with physical grid reality
- Supports the growing 24/7 CFE (Carbon-Free Energy) movement

**Against (or cautioning):**

- Implementation burden — most companies don't have hourly consumption data
- EAC market structure not yet capable of supporting hourly matching at scale
- Could devalue existing renewable investments matched annually
- Disproportionate burden on data centres, manufacturing, and other high-consumption operations
- Uptime Institute and major data centre operators have flagged the approach as "beyond the resources of most operators"

The compromise in the proposed revision is that hourly matching is **required only when companies make voluntary clean energy claims** (like "100% renewable", "100% carbon-free", or "24/7 CFE"). A company that simply reports its dual LBM/MBM Scope 2 figures without making a clean energy claim does not need to match hourly. This is a meaningful narrowing that addresses much of the feasibility concern.

## Implications for corporate PPAs

If the revision is adopted as proposed, the **corporate Power Purchase Agreement (PPA)** market would benefit substantially relative to unbundled EAC purchases. Corporate PPAs typically deliver EACs on an hourly or sub-hourly basis (matched to actual generation profiles), while unbundled REC/GO purchases are typically annual. Hourly matching requirements would make PPAs the operationally simpler path for companies wanting to make 24/7 or hourly-matched clean energy claims.

This is one reason the revision has drawn substantial corporate attention beyond the GHG accounting community — it directly affects multi-billion-euro renewable procurement strategies.

## How GreenCalculus implements Scope 2 alignment

GreenCalculus electricity calculators implement the 2015 Scope 2 Guidance methodology as follows:

**Dual reporting by default.** Every electricity calculator surfaces both LBM and MBM results, never one or the other in isolation. Users see both figures side-by-side, in line with the dual reporting requirement.

**Location-based method.** The Master Brain data layer (§04 grid) maintains location-based factors at the highest available granularity:
- Subregional factors where available (EPA eGRID for US, national grid operators for EU)
- National factors from IEA Global Energy Review 2026 as fallback
- Year-specific factors with explicit data vintage
- Marginal vs average factors clearly labelled where both exist

**Market-based method.** GreenCalculus accepts user inputs for:
- Supplier-specific emission rates
- Bundled EAC instruments (RECs, GOs, I-RECs, regional certificates)
- PPA contracted volumes and emissions factors
- Residual mix factors where applicable
- Fossil-only defaults for unclaimed portion

**Residual mix support.** Where a country publishes residual mix factors (e.g. AIB European Residual Mixes), GreenCalculus surfaces them for the unclaimed portion of consumption.

**Audit-trail metadata.** Every Scope 2 output carries the LBM and MBM factor sources, dates, methodology hierarchy step, and any user-provided contractual basis — supporting [ISO 14064-1](../iso/14064-1-organisation-ghg-quantification.md) verification.

## How GreenCalculus is preparing for the revision

The revision is not final and not in effect. But GreenCalculus is preparing the Master Brain data layer and calculator architecture for several likely changes:

- **Hourly factor support.** Where hourly LBM factors become available (ENTSO-E in Europe, several US ISOs), the Master Brain will tag them and surface them in calculators. Load-profile-based estimation is being scoped for users without hourly consumption data.
- **Deliverability tagging.** Each EAC and contractual instrument input is being tagged with its source grid, supporting future deliverability checks.
- **Clean energy claim flagging.** Users explicitly indicating they want to make a "100% renewable" or "24/7 CFE" claim are routed to stricter calculation paths anticipating revised requirements.
- **Phased rollout planning.** Calculator outputs will continue to follow the 2015 guidance until the final revised Scope 2 is published. When it is, a phased migration plan will be documented here.

## Important caveats

A few points worth flagging:

**1. The revision is not yet final.** Companies should continue to follow the 2015 Scope 2 Guidance for all current reporting. Anticipating revision-aligned practices is sensible for forward planning but is not a current requirement.

**2. The 2015 methodology remains in effect for CSRD, IFRS S2, CDP, and SBTi reporting** until those frameworks update to reference the revised Scope 2 Guidance — which will typically lag publication by 1–2 years.

**3. Hourly matching is conditional.** The proposed requirement applies only to voluntary clean energy claims, not to baseline Scope 2 reporting. This is widely misreported in commercial summaries.

**4. AR6 GWP basis applies.** All Scope 2 CO₂e conversions use [IPCC AR6 GWP-100](../ipcc/ar6-gwp-100.md) values, consistent with the GHG Protocol Corporate Standard.

**5. GreenCalculus is not verification.** A Scope 2 number from a calculator is methodologically aligned but is not assurance. Companies pursuing CSRD limited assurance, [ISO 14064-1](../iso/14064-1-organisation-ghg-quantification.md) verification, or voluntary third-party verification must engage an accredited body.

## Calculators on greencalculus.com that use this guidance

All electricity, steam, heat, and cooling calculators implement dual Scope 2 reporting. Specifically:

- All location-based electricity calculators (regional, national, and subregional factor support)
- All market-based electricity calculators (REC, GO, I-REC, PPA, supplier-specific factor support)
- Residual mix calculators (European AIB, US Green-e residual)
- Steam, heat, and chilled water purchased-energy calculators
- Data centre electricity calculators (high-resolution factor support)
- Manufacturing electricity calculators (industrial subregional factors)
- Combined facility Scope 1 + Scope 2 calculators (fuel + electricity)

## Official sources

- [GHG Protocol Scope 2 Guidance — official page](https://ghgprotocol.org/scope-2-guidance)
- [Scope 2 Standard Advances — ISB Approval for Consultation (July 2025)](https://ghgprotocol.org/blog/scope-2-standard-advances-isb-approves-consultation-market-and-location-based-revisions)
- [Upcoming Scope 2 Public Consultation: Overview of Revisions](https://ghgprotocol.org/blog/upcoming-scope-2-public-consultation-overview-revisions)
- [Upcoming Scope 2 Public Consultation: Hourly Matching and Deliverability](https://ghgprotocol.org/blog/upcoming-scope-2-public-consultation-hourly-matching-and-deliverability)
- [GHG Protocol Standard Development and Revision Procedure](https://ghgprotocol.org/ghg-protocol-corporate-suite-standards-and-guidance-update-process)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this guidance lives at:

**[greencalculus.com/standards/ghg-protocol-scope-2-guidance/](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/)**

That page is the canonical citation target for this guidance mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> World Resources Institute and World Business Council for Sustainable Development (2015). *GHG Protocol Scope 2 Guidance: An Amendment to the GHG Protocol Corporate Standard.* WRI/WBCSD, January 2015.

For the revision process documents:

> GHG Protocol Scope 2 Technical Working Group (2025). *Scope 2 Public Consultation Documents.* WRI/WBCSD, public consultation period 20 October 2025 – 31 January 2026.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-20
