# ISO 14067:2018 — Product Carbon Footprint

| Field | Value |
|---|---|
| **Initiative** | International Organization for Standardization (ISO) Technical Committee 207 — Environmental management |
| **Operative version** | ISO 14067:2018 (first edition) — reviewed and confirmed 2024, remains current |
| **Latest substantive update** | Replaced ISO/TS 14067:2013 (technical specification) on first publication in 2018 |
| **Next mandatory date** | None mandatory; revision in progress (ISO/WD 14067, registered 14 October 2024) |
| **Administered by** | ISO/TC 207/SC 7 — Greenhouse gas management and related activities |
| **GreenCalculus stack layer** | Layer 2 — Calculation (product level) |
| **Last reviewed** | 2026-05-17 |

---

## What this standard does

ISO 14067:2018 — formally titled *Greenhouse gases — Carbon footprint of products — Requirements and guidelines for quantification* — is the international standard for quantifying and reporting the **carbon footprint of a product (CFP)**. It applies to a single product or service across its entire life cycle, from raw material extraction through manufacturing, distribution, use, and end-of-life treatment.

It is the *product-level* counterpart to organisational standards like [ISO 14064-1](https://greencalculus.com/standards/iso-14064-1/) (organisation-level) and the [GHG Protocol Corporate Standard](../ghg-protocol/corporate-standard.md). Where those standards ask "what is my company's footprint?", ISO 14067 asks "what is *this product's* footprint?"

The standard is built directly on the LCA framework defined in [ISO 14040 and ISO 14044](https://greencalculus.com/standards/iso-14040-14044-lca/). It does not replace those standards — it applies their principles specifically to the climate-change impact category.

A note on scope discipline: ISO 14067 addresses **only one impact category — climate change**. It does not cover water footprint, land use, biodiversity, or any other environmental dimension. It also explicitly excludes carbon offsetting and the communication of CFP results (the latter is covered by ISO 14026:2017).

## Why it matters for GreenCalculus

ISO 14067 is gaining material importance in 2026 for three converging reasons:

1. **EU Green Claims Directive** and broader anti-greenwashing rules across major jurisdictions require companies that claim "carbon neutral" or "low carbon" for specific products to support those claims with recognised quantification methodology. ISO 14067 is the most credible internationally-accepted framework for doing so.

2. **Digital Product Passports** are being introduced for batteries (already in force), textiles, electronics, and other categories. ISO 14067 outputs are a primary input for the climate-impact section of these passports.

3. **CSRD value chain data requirements** ([see CSRD / ESRS E1 mapping](../eu/csrd-esrs-e1.md)) push large companies to request product-level carbon data from suppliers. ISO 14067 provides the supplier-side framework for producing that data consistently.

For GreenCalculus, this means product-level calculators (rather than the organisational Scope 1/2/3 calculators that dominate the platform) need their own methodological lineage. ISO 14067 is that lineage.

## Full CFP vs partial CFP — the two scope levels

ISO 14067 explicitly allows two calculation boundaries:

| Boundary | Term | What's included |
|---|---|---|
| **Cradle-to-grave** | Full CFP | Raw material acquisition → production → distribution → use → end-of-life |
| **Cradle-to-gate** | Partial CFP | Raw material acquisition → production → factory gate (excludes downstream use and end-of-life) |

Partial CFPs are common for B2B intermediate products where downstream use depends on the customer (e.g. steel sold to multiple industries cannot have a meaningful "use phase"). The standard requires partial CFP results to be clearly labelled as such and not compared to full CFP values without adjustment.

## Core methodological requirements

ISO 14067 derives its methodology from ISO 14040/14044 LCA principles, with carbon-footprint-specific refinements. The four LCA phases apply:

| LCA phase | ISO 14067 application |
|---|---|
| **Goal and scope definition** | Define product system, functional unit, system boundary (cradle-to-grave or cradle-to-gate), time boundaries, allocation rules |
| **Life cycle inventory (LCI)** | Collect activity data for all unit processes in the system boundary |
| **Life cycle impact assessment (LCIA)** | Apply emission factors and GWP values to compute CO₂e for each unit process; aggregate to product total |
| **Interpretation** | Sensitivity, uncertainty, and completeness analysis; conclusions and limitations |

**The functional unit is critical.** ISO 14067 requires the CFP to be expressed against a defined functional unit (per kilogram, per kWh, per use, per square metre, etc.). Comparisons between products are only valid if functional units match. A "kg CO₂e per kg of steel" CFP cannot be compared with "kg CO₂e per tonne of steel" without conversion, and cannot be compared with "kg CO₂e per car body" at all without redefining the functional unit.

**Biogenic carbon and electricity** treatment was specifically clarified versus the 2013 technical specification. Biogenic CO₂ uptake and release must be reported separately from fossil emissions. Electricity may use either location-based or market-based factors, with the choice and rationale disclosed.

**Product Category Rules (PCRs)** are not part of ISO 14067 itself but are widely used alongside it. PCRs define system boundaries, data requirements, and calculation methods for specific product categories — ensuring that two manufacturers calculating the CFP of (for example) a 500ml glass bottle do so on a comparable basis. PCRs from organisations like EPD International, Bionova, and the International EPD® System are commonly referenced.

## How GreenCalculus implements ISO 14067 alignment

Product-level CFP work is a different operational mode than organisational reporting. GreenCalculus product carbon footprint calculators implement ISO 14067 alignment through:

**Cradle-to-gate and cradle-to-grave boundary options.** Each PCF calculator allows users to select the boundary explicitly, with the output clearly labelled and the unincluded life cycle phases listed.

**Functional unit input.** Calculators require the functional unit to be set before output is generated. This prevents the common error of producing a CFP that cannot be meaningfully compared.

**Master Brain factor sourcing.** All emission factors used in product-level calculations are drawn from the Master Brain data layer with full source attribution (DEFRA 2025, IEA 2026, ICE database, ecoinvent-compatible mappings where applicable). Each factor's source, date, GWP basis, and unit is exposed in the calculator output.

**Biogenic carbon disaggregation.** For products containing biogenic carbon (wood, paper, bio-based polymers), biogenic and fossil CO₂ are tracked and reported separately in line with ISO 14067 requirements.

**Electricity dual reporting.** Where electricity is a significant unit process, both location-based and market-based factors are surfaced, mirroring the [GHG Protocol Scope 2 Guidance](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/) treatment.

**AR6 GWP-100 default.** CO₂e calculations use [IPCC AR6 GWP-100](../ipcc/ar6-gwp-100.md) values by default, with AR5 retained for legacy comparison or when a specific PCR mandates an older basis.

## The relationship between ISO 14067 and other standards

ISO 14067 does not exist in isolation. It sits at the intersection of several standard families:

| Standard | Relationship |
|---|---|
| **ISO 14040 / 14044** (LCA) | Foundational methodology — ISO 14067 is an application-specific extension |
| **ISO 14064 series** (organisational GHG) | Definitions aligned for terminology consistency |
| **ISO 14025** (EPDs) | EPDs typically reference ISO 14067 for the climate-change impact category |
| **ISO 14026** (footprint communication) | Covers the *communication* of CFP results — explicitly out of ISO 14067 scope |
| **EN 15804** (construction EPDs) | Sector-specific PCR for construction products; references ISO 14067 methodology |
| **PAS 2050** (BSI, UK) | Predecessor and parallel UK national standard; broadly aligned but distinct |
| **GHG Protocol Product Standard** | Parallel framework with different governance; results often similar but not identical |

For most companies, the choice between ISO 14067 and the GHG Protocol Product Standard is a matter of organisational preference and audit context. The two produce comparable results for most well-defined products, but the documentation conventions differ.

## The revision in progress — ISO/WD 14067

A revision is underway. Key milestones to date:

- **14 October 2024** — New project registered in TC/SC work programme
- **21 June 2025** — Working draft (WD) study initiated
- **26 August 2025** — Close of comment period for WD
- **Status as of May 2026** — WD approved for registration as Committee Draft (CD); subsequent stages will be CD → Draft International Standard (DIS) → Final Draft International Standard (FDIS) → publication

Publication of the revised ISO 14067 is targeted for 2027 or 2028, depending on the ballot and review cycle. The revision is not expected to fundamentally change the methodology — the standard was already a refinement of ISO/TS 14067:2013 with substantial methodological maturity. Expected changes include alignment with newer ISO 14064 series amendments, clearer guidance on biogenic carbon and removals (cross-referencing the GHG Protocol [Land Sector and Removals Standard](../ghg-protocol/land-sector-removals-2026.md) where appropriate), and updated electricity accounting consistent with current Scope 2 best practice.

GreenCalculus will track the revision and update calculator alignment when the final standard is published.

## Important caveats

A few points to flag:

**1. ISO 14067 covers only climate change.** It is not a full environmental footprint standard. Companies wanting a broader environmental performance picture need to apply ISO 14040/14044 fully and report multiple impact categories (acidification, eutrophication, ozone depletion, etc.) — ISO 14067 alone is insufficient.

**2. ISO 14067 does not cover offsetting.** Carbon offsets, removal credits, and "carbon neutral" claims are out of scope. A product cannot be made ISO-14067-compliant *by* offsetting — the standard quantifies emissions, it does not endorse netting them against credits.

**3. ISO 14067 does not cover communication.** Labelling, marketing claims, and how CFP results are communicated to consumers fall under ISO 14026:2017 (footprint communication) and emerging regulations like the EU Green Claims Directive. An ISO 14067-compliant CFP gives you the *number*; communicating it responsibly is a separate compliance exercise.

**4. PCRs are recommended but not mandated.** ISO 14067 itself does not require Product Category Rules. But for any product where comparability with peer products matters (and that is most B2B use cases), using a PCR is effectively necessary to avoid producing results that cannot be meaningfully compared.

**5. GreenCalculus is not third-party verification.** ISO 14067 results are typically verified by an accredited body (SGS, TÜV, DNV, Bureau Veritas, etc.) to be useful for external claims, EPDs, or regulated disclosures. GreenCalculus produces the calculation; verification is a separate engagement.

## Calculators on greencalculus.com that use this standard

This list will be populated as each product-level calculator's ISO 14067 alignment is verified. Affected categories include:

- All product carbon footprint calculators (cradle-to-gate and cradle-to-grave)
- Building material PCF calculators (cross-references [BS EN 15978](https://greencalculus.com/standards/bs-en-15978-embodied-carbon-buildings/))
- Food and agricultural product CFP calculators
- Packaging CFP calculators
- Industrial intermediate product CFP calculators (steel, aluminium, plastics, glass)
- Textile and apparel CFP calculators

## Official sources

- [ISO 14067:2018 — official standard page](https://www.iso.org/standard/71206.html)
- [ISO/WD 14067 — revision in progress](https://www.iso.org/standard/90578.html)
- [ISO 14040:2006 — LCA principles and framework](https://www.iso.org/standard/37456.html)
- [ISO 14044:2006 — LCA requirements and guidelines](https://www.iso.org/standard/38498.html)
- [ISO/TC 207/SC 7 — committee page](https://www.iso.org/committee/54854.html)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/iso-14067-product-carbon-footprint/](https://greencalculus.com/standards/iso-14067-product-carbon-footprint/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> International Organization for Standardization (2018). *ISO 14067:2018 — Greenhouse gases — Carbon footprint of products — Requirements and guidelines for quantification.* ISO, Geneva. First edition. Reviewed and confirmed 2024.

For the European harmonised version:

> European Committee for Standardization (2018). *EN ISO 14067:2018 — Greenhouse gases — Carbon footprint of products — Requirements and guidelines for quantification.* CEN, Brussels.

For the predecessor technical specification (historical reference):

> International Organization for Standardization (2013). *ISO/TS 14067:2013 — Greenhouse gases — Carbon footprint of products — Requirements and guidelines for quantification and communication.* ISO, Geneva. *Cancelled and replaced by ISO 14067:2018.*

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-17
