# GHG Protocol Corporate Accounting and Reporting Standard

| Field | Value |
|---|---|
| **Initiative** | GHG Protocol (WRI / WBCSD) |
| **Operative version** | 2026 revision |
| **Latest substantive update** | 2026 |
| **Next mandatory date** | Aligned with annual reporting cycles |
| **Administered by** | World Resources Institute (WRI) and World Business Council for Sustainable Development (WBCSD) |
| **GreenCalculus stack layer** | Layer 2 — Calculation |
| **Last reviewed** | 2026-05-10 |

---

## What this standard does

The GHG Protocol Corporate Accounting and Reporting Standard ("Corporate Standard") is the foundational global framework for how companies account for and report greenhouse gas emissions. It defines the three scopes — Scope 1 (direct emissions), Scope 2 (indirect emissions from purchased energy), and Scope 3 (other indirect emissions) — that virtually every other corporate climate framework, from CSRD to SBTi to ISO 14064-1, builds on.

Originally published in 2001 with a 2004 revised edition, the Corporate Standard underwent a 2026 revision to incorporate methodology updates, alignment with newer disclosure regimes, and clarifications around market-based accounting for Scope 2.

## Why it matters for GreenCalculus

Every calculator on the GreenCalculus platform classifies its output against the GHG Protocol scope boundaries. This is the backbone of our scope tagging system — when a calculator returns a result tagged "Scope 1 — Stationary Combustion", that classification is sourced directly from this standard.

## How GreenCalculus implements this standard

**Scope mapping.** The Master Brain data layer (§16) maps every calculator and every emission factor to a Scope 1, 2, or 3 designation, with Scope 3 further broken down into the 15 categories defined in the [Scope 3 Standard](./scope-3-standard.md).

**Dual reporting for Scope 2.** Per the Corporate Standard's amended Scope 2 Guidance, GreenCalculus electricity calculators present both location-based and market-based results where applicable. Location-based uses regional grid factors from the IEA 2026 dataset; market-based applies contractual instruments (RECs, GOs, PPAs) where the user provides them.

**AR6 GWPs.** The 2026 revision aligns with IPCC AR6 (2021) for global warming potentials. GreenCalculus uses AR6 GWP-100 as the default basis for all CO₂-equivalent calculations. AR5 values are retained in the Master Brain for legacy comparison only.

## Calculators on greencalculus.com that use this standard

This list will be populated as each calculator's mapping is verified.

- All Scope 1 stationary combustion calculators
- All Scope 1 mobile combustion (fleet) calculators
- All Scope 2 electricity calculators (location-based and market-based)
- All Scope 3 category-specific calculators (1–15)

## Official sources

- [GHG Protocol Corporate Standard — official page](https://ghgprotocol.org/corporate-standard)
- [GHG Protocol Scope 2 Guidance](https://ghgprotocol.org/scope-2-guidance)

## Canonical GreenCalculus reference

The fully-styled, version-tracked, schema-marked-up reference page for this standard lives at:

**[greencalculus.com/standards/ghg-protocol-corporate-standard/](https://greencalculus.com/standards/ghg-protocol-corporate-standard/)**

That page is the canonical citation target for this standard mapping. This GitHub document is the open-methodology mirror, distributed under CC-BY-4.0 for verification and reuse.

## Citation

> World Resources Institute and World Business Council for Sustainable Development (2026). *The Greenhouse Gas Protocol: A Corporate Accounting and Reporting Standard, Revised Edition.* WRI/WBCSD.

---

**Authored by** Jeremiah Say · **Verified by** GreenCalculus Engineering · **Last reviewed** 2026-05-10
