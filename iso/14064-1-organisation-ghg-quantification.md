# ISO 14064-1 — Organisation-Level GHG Quantification and Reporting

| Field | Value |
|---|---|
| **Initiative** | International Organization for Standardization (ISO) Technical Committee 207 — Environmental management |
| **Operative version** | ISO 14064-1:2018 (second edition) — reviewed and confirmed 2024, remains current |
| **Latest substantive update** | Published 18 December 2018; replaced ISO 14064-1:2006 with substantial methodological changes |
| **Next mandatory date** | None mandatory; revision in progress (ISO/WD 14064-1.2, new project registered 14 October 2024) |
| **Administered by** | ISO/TC 207/SC 7 — Greenhouse gas management and related activities |
| **GreenCalculus stack layer** | Layer 2 — Calculation (organisation level, verification-focused) |
| **Last reviewed** | 2026-05-19 |

---

## What this standard does

ISO 14064-1:2018 — formally titled *Greenhouse gases — Part 1: Specification with guidance at the organization level for quantification and reporting of greenhouse gas emissions and removals* — is the international standard for **quantifying and reporting an organisation's GHG inventory in a manner that supports independent third-party verification**.

It is the *organisation-level* sister standard to:

- **ISO 14064-2:2019** — Project-level GHG quantification (offset projects, emission reduction initiatives)
- **ISO 14064-3:2019** — Validation and verification of GHG assertions (the standard verifiers use to audit 14064-1 reports)

Where the [GHG Protocol Corporate Standard](../ghg-protocol/corporate-standard.md) defines the dominant *methodology* for corporate carbon accounting, ISO 14064-1 defines the dominant *verification framework* for that same accounting. The two standards are explicitly compatible — most companies that follow GHG Protocol can have their inventory verified to ISO 14064-1 without methodology change — but the documentation conventions, terminology, and reporting boundaries differ in important ways.

A key positioning point: ISO 14064-1 is **GHG programme neutral**. If a specific GHG programme (CDP, SBTi, EU ETS, CBAM, California Cap-and-Trade, CSRD) applies, that programme's requirements are *additional* to ISO 14064-1 — they don't replace it. This makes 14064-1 the underlying assurance framework that programme-specific reporting sits on top of.

## Why it matters for GreenCalculus

For organisations seeking **third-party assurance** of their GHG inventory — for CSRD limited assurance, voluntary verification to support customer trust, regulatory compliance (EU ETS, CBAM), or internal governance — ISO 14064-1 is the standard that defines what they must document, how they must structure their inventory, and what an auditor will check against.

GreenCalculus calculator outputs that comply with the GHG Protocol Corporate Standard methodology are *also* compatible with ISO 14064-1 — but only if the user understands which terminology to use, which categories to map to, and what additional documentation is needed for verification readiness. This mapping document is the bridge.

In practice, every GreenCalculus user pursuing ISO 14064-1 verification needs to know:

- Their calculator outputs are methodologically aligned but use GHG Protocol terminology (Scope 1/2/3)
- ISO 14064-1 uses six categories, not three scopes — they map directly but differently
- Verification readiness requires audit-trail documentation that the calculator output is a *component* of, not the entirety of

## The six emission categories — ISO 14064-1's structural departure from "scopes"

The single most important conceptual difference between ISO 14064-1:2018 and the GHG Protocol is the **replacement of the three-scope model with a six-category model**. The 2006 edition of ISO 14064-1 used three scopes aligned with GHG Protocol. The 2018 edition revised this to better reflect the structure of indirect emissions across the value chain.

| ISO 14064-1 Category | Description | GHG Protocol equivalent |
|---|---|---|
| **Category 1** | Direct GHG emissions and removals | Scope 1 |
| **Category 2** | Indirect GHG emissions from imported energy | Scope 2 |
| **Category 3** | Indirect GHG emissions from transportation | Scope 3 — Categories 4, 6, 7, 9 (parts) |
| **Category 4** | Indirect GHG emissions from products used by organisation | Scope 3 — Categories 1, 2, 3, 5, 8 |
| **Category 5** | Indirect GHG emissions associated with the use of products from the organisation | Scope 3 — Categories 10, 11, 12, 13 |
| **Category 6** | Indirect GHG emissions from other sources | Scope 3 — Category 14, 15, and others not elsewhere classified |

This reorganisation is **functionally equivalent** to the GHG Protocol scopes — every emission source maps to one (and only one) ISO 14064-1 category, and the totals match. But the documentation and reporting structure differs. Organisations following GHG Protocol can present the same data in ISO 14064-1 format by re-aggregating, with no recalculation required.

The 2018 edition also renamed "other indirect GHG emissions" (the 2006 term for Scope 3) to simply **"indirect GHG emissions"**, eliminating a conceptual hierarchy that confused users.

## Required content of a 14064-1-compliant report

A 14064-1-compliant GHG inventory report must include:

| Requirement | Detail |
|---|---|
| **Organisational boundary** | Defined by either *control approach* (financial or operational) or *equity share* approach |
| **Reporting boundary** | All six emission categories, with significance assessment for each |
| **Quantified GHG emissions and removals** | By category, in tonnes of CO₂ equivalent (tCO₂e) |
| **Base year** | Selected base year inventory and recalculation policy for structural changes |
| **GHG inventory quality management** | Procedures for ensuring accuracy, completeness, consistency, transparency |
| **Uncertainty assessment** | Qualitative or quantitative |
| **Biogenic CO₂** | Reported separately from fossil emissions |
| **Seven Kyoto gases** | CO₂, CH₄, N₂O, HFCs, PFCs, SF₆, NF₃ — all must be considered |
| **GWP basis** | Time horizon and source (typically AR6 GWP-100); consistently applied |
| **Methodology** | Calculation methods, emission factors, and activity data sources |
| **Significant changes** | Disclosure of significant changes from prior year |
| **Internal verification** | Description of internal QA/QC process |

This is more prescriptive than the GHG Protocol Corporate Standard, which is intentional — 14064-1 was designed to be verifiable, so it specifies exactly what needs to be documented for a third party to check.

## Verification under ISO 14064-3 — limited vs reasonable assurance

Verification is performed by an accredited third party against ISO 14064-3:2019. Two levels of assurance are possible:

| Assurance level | Auditor's opinion form | Effort required | Common use |
|---|---|---|---|
| **Limited assurance** | "Nothing has come to our attention that the GHG statement is materially misstated" (negative opinion) | Lower — sample-based testing | CSRD initial years; voluntary disclosure |
| **Reasonable assurance** | "In our opinion, the GHG statement is presented fairly" (positive opinion) | Higher — substantive testing of controls and data | Regulated emissions trading; high-stakes regulated disclosure; CSRD planned progression (now cancelled under Omnibus I) |

The CSRD originally planned a progression from limited to reasonable assurance over time. Under Omnibus I (Feb 2026), this progression has been cancelled — limited assurance is now retained as the permanent CSRD requirement. See the [CSRD / ESRS E1 mapping](../eu/csrd-esrs-e1.md) for detail.

For organisations not subject to CSRD, voluntary 14064-1 verification at limited or reasonable assurance level is increasingly common as a market signal — particularly in jurisdictions with weaker mandatory regimes.

## How GreenCalculus implements ISO 14064-1 alignment

GreenCalculus calculator outputs are methodologically compatible with ISO 14064-1 because both standards use the same underlying calculation principles (activity data × emission factor, AR6 GWP conversion, mass-balance accounting). The alignment is operationalised through:

**Dual category/scope tagging.** The Master Brain data layer tags every emission factor with both its GHG Protocol scope (1/2/3) and its ISO 14064-1 category (1–6). Calculator outputs surface both, so users pursuing verification can re-aggregate into 14064-1 format without recalculation.

**Documentation export.** Each calculator output includes a methodological statement covering activity data source, emission factor source and date, GWP basis (AR6), uncertainty range (qualitative), and any allocation or aggregation rules applied. This is the calculator-side contribution to the inventory documentation a 14064-1 verifier will review.

**Biogenic CO₂ separation.** Biogenic and fossil CO₂ are tracked and reported separately throughout the Master Brain (§02 GWP, §11 agriculture, §14 removals) in line with 14064-1 requirements.

**Seven Kyoto gases coverage.** The Master Brain covers all seven Kyoto gases (CO₂, CH₄, N₂O, HFCs, PFCs, SF₆, NF₃) with both AR6 and AR5 GWP values. NF₃ — added to Kyoto in 2012 — is included.

**Base year support.** Calculators support specifying a base year inventory and surfacing year-over-year changes. The user remains responsible for documenting their recalculation policy.

## The relationship between ISO 14064-1 and the GHG Protocol

A common source of confusion is whether ISO 14064-1 and the GHG Protocol Corporate Standard are alternatives or complements. The accurate framing is:

- **The GHG Protocol Corporate Standard is a methodology** — it tells you *how* to calculate
- **ISO 14064-1 is a verification framework** — it tells you *how to document and report* in a way that supports third-party verification

In practice, most companies follow the GHG Protocol Corporate Standard for methodology and then present the same data structured according to ISO 14064-1 for verification purposes. This is explicitly anticipated by both standards. Annex H of ISO 14064-1 even provides a mapping between the six categories and GHG Protocol scopes.

The two standards have not historically been in tension — but with the [GHG Protocol Scope 3 revision in progress](../ghg-protocol/scope-3-standard.md) (Phase 1 Update March 2026), the ISO 14064-1 revision (ISO/WD 14064-1.2 underway), and the [GHG Protocol Land Sector and Removals Standard](../ghg-protocol/land-sector-removals-2026.md) now in effect, alignment is being actively maintained by both standards bodies through cross-referencing in the respective drafting committees.

## Programme recognition

ISO 14064-1 is explicitly recognised or referenced by:

| Programme | Recognition status |
|---|---|
| **EU ETS** (Emissions Trading System) | Monitoring, Reporting and Verification (MRV) requirements broadly align; some sector-specific differences |
| **EU CBAM** (Carbon Border Adjustment Mechanism) | Verification of embedded emissions in imported goods accepts 14064-1 / 14064-3 verification |
| **CSRD / ESRS E1** | 14064-1 verification supports the limited assurance requirement; widely used in CSRD preparation |
| **CDP** | 14064-1 verification recognised as a credible verification standard |
| **California Cap-and-Trade** | Mandatory reporting verification follows analogous principles |
| **TCFD Recommendations** | 14064-1 verification supports the Metrics & Targets pillar |
| **SBTi** | 14064-1 verification recognised for target validation |
| **ISO 14064-3** verifier accreditation through ANAB (US), UKAS (UK), and equivalent national accreditation bodies | Standard accreditation route |

## The revision in progress — ISO/WD 14064-1.2

A revision is underway. Key facts:

- **14 October 2024** — New project registered in TC 207/SC 7 work programme
- **Status as of May 2026** — Working draft (WD) at stage 20.20; will progress through WD → CD → DIS → FDIS → publication
- **Expected publication** — 2027 or 2028, depending on the ballot cycle

The revision is not expected to be as substantive as the 2006-to-2018 transition. Likely changes include:

- Updated alignment with the in-progress [GHG Protocol Scope 3 revision](../ghg-protocol/scope-3-standard.md)
- Cross-referencing with the [GHG Protocol Land Sector and Removals Standard](../ghg-protocol/land-sector-removals-2026.md)
- Clarifications on Category 5 (use of sold products) reflecting practitioner feedback
- Updated electricity accounting consistent with current [Scope 2 Guidance](https://greencalculus.com/standards/ghg-protocol-scope-2-guidance/) best practice
- Possible addition of explicit removals reporting (mirroring the LSR Standard direction)

GreenCalculus will track the revision and update calculator alignment when the final standard is published.

## Important caveats

A few points worth flagging:

**1. ISO 14064-1 does not require verification.** The standard specifies the *requirements* for an inventory that *can* be verified. Verification itself is governed by ISO 14064-3 and is a separate engagement with an accredited body. An organisation can produce a 14064-1-compliant report without ever undergoing verification — but the standard's design assumes verification is on the table.

**2. ISO 14064-1 is methodologically broader than the GHG Protocol Scope 3 Standard.** The Scope 3 Standard requires categorisation into 15 specific categories. ISO 14064-1's six categories are higher-level — a single ISO 14064-1 category may aggregate multiple Scope 3 categories. This means an inventory verified to ISO 14064-1 is not automatically presented in Scope 3 Standard-compliant format; an explicit mapping is needed.

**3. Significance thresholds are organisation-defined.** ISO 14064-1 requires the organisation to identify significant emission sources but doesn't prescribe a numerical threshold. Common practice is 5% of total or other proportional rules, but the organisation must justify its threshold to the verifier.

**4. The control vs equity share choice is consequential.** Operational control, financial control, and equity share approaches can produce materially different organisational boundaries — particularly for organisations with joint ventures, minority stakes, or franchise networks. The choice must be documented and applied consistently.

**5. GreenCalculus is not verification.** Calculator outputs methodologically aligned with 14064-1 are an input to a verification process — not a substitute for it. Organisations pursuing assurance must engage an accredited verification body under ISO 14064-3 (or analogous national accreditation).

## Calculators on greencalculus.com that contribute to ISO 14064-1 inventories

Every Scope 1, Scope 2, and Scope 3 calculator on the platform produces output compatible with ISO 14064-1 categorisation. Specifically:

- All Scope 1 stationary, mobile, fugitive, and process emissions calculators → Category 1
- All Scope 2 location-based and market-based electricity calculators → Category 2
- All Scope 3 transportation-related calculators (business travel, commuting, upstream/downstream freight) → Category 3
- All Scope 3 purchased goods, capital goods, fuel-and-energy-related activities, waste, leased assets (upstream) → Category 4
- All Scope 3 processing, use, end-of-life of sold products, leased assets (downstream) → Category 5
- Scope 3 franchises, investments, and other-categorised emissions → Category 6
- Removals calculators (soil carbon, afforestation, technological removals) → Reported separately in line with both 14064-1 and the LSR Standard

## Official sources

- [ISO 14064-1:2018 — official standard page](https://www.iso.org/standard/66453.html)
- [ISO/WD 14064-1.2 — revision in progress](https://www.iso.org/standard/90575.html)
- [ISO 14064-2:2019 — project level](https://www.iso.org/standard/66454.html)
- [ISO 14064-3:2019 — validation and verification](https://www.iso.org/standard/66455.html)
- [ISO/TC 207/SC 7 — committee page](https://www.iso.org/committee/54854.html)
- [ANAB GHG Validation/Verification Bodies Accreditation Program](https://anab.ansi.org/ghg-vvb-accreditation)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/iso-14064-1/](https://greencalculus.com/standards/iso-14064-1/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> International Organization for Standardization (2018). *ISO 14064-1:2018 — Greenhouse gases — Part 1: Specification with guidance at the organization level for quantification and reporting of greenhouse gas emissions and removals.* ISO, Geneva. Second edition. Reviewed and confirmed 2024.

For the verification companion standard:

> International Organization for Standardization (2019). *ISO 14064-3:2019 — Greenhouse gases — Part 3: Specification with guidance for the verification and validation of greenhouse gas statements.* ISO, Geneva.

For the predecessor edition (historical reference):

> International Organization for Standardization (2006). *ISO 14064-1:2006 — Greenhouse gases — Part 1: Specification with guidance at the organization level for quantification and reporting of greenhouse gas emissions and removals.* ISO, Geneva. *Cancelled and replaced by ISO 14064-1:2018.*

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-19
