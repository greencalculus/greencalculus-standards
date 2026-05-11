# IPCC AR6 — 100-Year Global Warming Potentials

| Field | Value |
|---|---|
| **Initiative** | IPCC Sixth Assessment Report (AR6) — Working Group I |
| **Operative version** | AR6 WGI (2021) |
| **Latest substantive update** | None since publication (2021) |
| **Next mandatory date** | Superseded when IPCC AR7 WGI is published — targeted mid-to-late 2028, timeline still disputed at IPCC-63 (April 2026) |
| **Administered by** | Intergovernmental Panel on Climate Change (IPCC) — a body of the United Nations |
| **GreenCalculus stack layer** | Layer 1 — Science |
| **Last reviewed** | 2026-05-12 |

---

## What this standard does

The IPCC Sixth Assessment Report Working Group I (WGI) — *Climate Change 2021: The Physical Science Basis* — provides the current global scientific consensus on the radiative forcing of greenhouse gases, expressed as 100-year Global Warming Potentials (GWP-100). These values are the multipliers used to convert emissions of any greenhouse gas into a common unit of CO₂-equivalent (CO₂e), enabling like-for-like aggregation across scopes, sectors, and inventories.

The specific values used in corporate GHG accounting are drawn from **AR6 WGI Chapter 7, Supplementary Material Table 7.SM.7**.

## Why it matters for GreenCalculus

GWP values are the multiplicative bridge between *physical emissions* (kilograms of methane, nitrous oxide, refrigerants) and *reportable carbon equivalence* (kilograms of CO₂e). Every calculator on the GreenCalculus platform that handles a non-CO₂ gas — methane from fugitive emissions, nitrous oxide from agriculture, HFCs from refrigeration, SF₆ from electrical equipment — performs this conversion using AR6 GWP-100 values.

A single GWP value change between assessment cycles can shift reported emissions by 10–30% for non-CO₂-dominant inventories. This is why the science basis layer is not optional: every CO₂e number on the site is only as accurate as the GWP basis behind it.

## Why GHG Protocol mandates AR6

The [GHG Protocol Corporate Standard (2026 revision)](../ghg-protocol/corporate-standard.md) requires the use of AR6 GWP-100 values. This replaces the AR5 (2013) values that were operative under the previous revision. GreenCalculus retains AR5 values in the Master Brain data layer for legacy comparison only — they are not used for current-period reporting.

The choice of GWP basis is not a methodological preference. It is a scientific update: AR6 incorporates substantial refinements in radiative forcing science, particularly for methane, where the inclusion of climate-carbon feedbacks moved fossil CH₄ from a GWP-100 of 28 (AR5) to 29.8 (AR6) and biogenic CH₄ to 27.9.

## Key AR6 GWP-100 values used by GreenCalculus

The full set is maintained in the Master Brain data layer (§02 GWP). Most-cited values:

| Gas | AR6 GWP-100 | AR5 GWP-100 (legacy) | Notes |
|---|---|---|---|
| CO₂ | 1 | 1 | Reference gas |
| Methane (fossil) | 29.8 | 28 | Combustion, oil & gas fugitives |
| Methane (biogenic) | 27.9 | 28 | Landfill, livestock, rice cultivation |
| Nitrous oxide (N₂O) | 273 | 265 | Fertiliser, combustion |
| HFC-134a | 1,530 | 1,300 | Common refrigerant |
| HFC-23 | 14,600 | 12,400 | Byproduct of HCFC-22 production |
| SF₆ | 25,200 | 23,500 | Electrical switchgear |
| NF₃ | 17,400 | 16,100 | Semiconductor manufacturing |
| PFC-14 (CF₄) | 7,380 | 6,630 | Aluminium smelting |

All values are 100-year horizon, without climate-carbon feedbacks unless otherwise noted in the Master Brain entry. For sources that report values *with* climate-carbon feedbacks, GreenCalculus retains both forms and labels them explicitly.

## How GreenCalculus implements AR6

**Default basis is AR6 GWP-100.** Every CO₂e calculation on the live site uses AR6 values from Master Brain §02 unless explicitly stated otherwise (some legacy regulatory contexts — e.g. certain national inventory reporting — still mandate AR5; those calculators are flagged).

**AR5 retained for legacy comparison only.** Each GWP entry in the Master Brain carries both `ar6_100` and `ar5_100` fields. Calculators can surface either, but the default and the schema-published value is always AR6.

**Methane is disambiguated.** Most public emission factor sources publish a single CH₄ value. AR6 distinguishes fossil CH₄ (29.8) from biogenic CH₄ (27.9). GreenCalculus enforces this distinction throughout the Master Brain — combustion and oil & gas fugitives use fossil; landfill, livestock, and rice cultivation use biogenic.

**Sources of fugitive emissions follow IPCC 2019 Refinement.** For fugitive coal methane in particular, GreenCalculus uses the 2019 Refinement to the 2006 IPCC Guidelines for National Greenhouse Gas Inventories (Volume 2 Energy, Chapter 4), applied with AR6 GWPs.

## When AR6 will be superseded — AR7 status as of May 2026

AR6 GWP values will remain the operative scientific basis until IPCC AR7 Working Group I is published. The AR7 timeline is currently **unresolved**.

As of the 63rd IPCC Plenary Session held in Lima, Peru, in April 2026, governments have failed to agree the AR7 publication timeline for the **fifth consecutive session**. Two broad camps remain:

- Countries favouring a faster cycle (US, EU, small island states) want all three Working Group reports published in 2028 to inform the UN's Second Global Stocktake at COP33.
- Countries favouring a longer cycle (Saudi Arabia, India, China, several African delegations) cite developing-country review capacity and scientific literature gaps, and would push WG2 to late 2028, WG3 to 2029.

The current best estimate based on IPCC Bureau planning:

- **WG1 (Physical Science Basis)** — targeted mid-2028. *This is the report that will publish updated GWP values.*
- **WG2 (Impacts, Adaptation, Vulnerability)** — 2028 or early 2029
- **WG3 (Mitigation of Climate Change)** — late 2028 or 2029
- **AR7 Synthesis Report** — late 2029

GreenCalculus will publish a transition plan as soon as the IPCC confirms the WGI publication date. Until AR7 WGI is published, **AR6 remains the operative basis** and any commercial or marketing claim to "AR7-ready" methodology should be treated with scepticism.

## Calculators on greencalculus.com that use this standard

Every non-CO₂-only calculator on the platform uses AR6 GWP-100 values. Notable categories:

- All Scope 1 fugitive refrigerant calculators (HFC leak emissions)
- All Scope 1 fugitive coal methane calculators (using IPCC 2019 Refinement)
- All Scope 1 agriculture calculators (N₂O from fertiliser, CH₄ from livestock)
- All Scope 3 Category 5 waste calculators (landfill CH₄)
- All electrical infrastructure calculators (SF₆ in switchgear)
- All semiconductor sector calculators (NF₃, PFCs)

## Official sources

- [IPCC AR6 WGI — Climate Change 2021: The Physical Science Basis](https://www.ipcc.ch/report/ar6/wg1/)
- [AR6 WGI Chapter 7 — The Earth's Energy Budget, Climate Feedbacks, and Climate Sensitivity](https://www.ipcc.ch/report/ar6/wg1/chapter/chapter-7/)
- [AR6 WGI Chapter 7 Supplementary Material (contains Table 7.SM.7)](https://www.ipcc.ch/report/ar6/wg1/downloads/report/IPCC_AR6_WGI_Chapter07_SM.pdf)
- [IPCC AR7 — official assessment cycle page](https://www.ipcc.ch/assessment-report/ar7/)
- [IPCC 2019 Refinement to the 2006 Guidelines](https://www.ipcc-nggip.iges.or.jp/public/2019rf/index.html)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/ipcc-ar6/](https://greencalculus.com/standards/ipcc-ar6/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> IPCC (2021). *Climate Change 2021: The Physical Science Basis. Contribution of Working Group I to the Sixth Assessment Report of the Intergovernmental Panel on Climate Change* [Masson-Delmotte, V., P. Zhai, A. Pirani, S.L. Connors, C. Péan, S. Berger, N. Caud, Y. Chen, L. Goldfarb, M.I. Gomis, M. Huang, K. Leitzell, E. Lonnoy, J.B.R. Matthews, T.K. Maycock, T. Waterfield, O. Yelekçi, R. Yu, and B. Zhou (eds.)]. Cambridge University Press, Cambridge, United Kingdom and New York, NY, USA. https://doi.org/10.1017/9781009157896

For the specific GWP table:

> Forster, P., T. Storelvmo, K. Armour, W. Collins, J.-L. Dufresne, D. Frame, D.J. Lunt, T. Mauritsen, M.D. Palmer, M. Watanabe, M. Wild, and H. Zhang, 2021: *The Earth's Energy Budget, Climate Feedbacks, and Climate Sensitivity*. In: Climate Change 2021: The Physical Science Basis. Contribution of Working Group I to the Sixth Assessment Report of the IPCC. Table 7.SM.7.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-12
