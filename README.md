# GreenCalculus — Standards Alignment

> Open methodology mapping for the global greenhouse gas accounting standards that GreenCalculus calculators implement.

[![GHG Protocol Corporate](https://img.shields.io/badge/GHG_Protocol-Corporate-1D3215?style=flat-square)](./ghg-protocol/corporate-standard.md)
[![GHG Protocol Scope 3](https://img.shields.io/badge/GHG_Protocol-Scope_3-1D3215?style=flat-square)](./ghg-protocol/scope-3-standard.md)
[![LSR 2026](https://img.shields.io/badge/GHG_Protocol-LSR_2026-1D3215?style=flat-square)](./ghg-protocol/land-sector-removals-2026.md)
[![IPCC AR6](https://img.shields.io/badge/IPCC-AR6_GWP--100-1D3215?style=flat-square)](./ipcc/ar6-gwp-100.md)
[![ISO 14064-1](https://img.shields.io/badge/ISO-14064--1-1D3215?style=flat-square)](./iso/iso-14064-1.md)
[![CSRD ESRS E1](https://img.shields.io/badge/CSRD-ESRS_E1-04BF62?style=flat-square)](./eu/csrd-esrs-e1.md)
[![SBTi Net-Zero](https://img.shields.io/badge/SBTi-Net--Zero-04BF62?style=flat-square)](./targets/sbti-net-zero.md)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-04BF62?style=flat-square)](./LICENSE)

---

## What this repository is

This repository documents **how GreenCalculus calculators align with the global standards governing corporate greenhouse gas accounting**. Every calculator on [greencalculus.com](https://greencalculus.com) is built on top of one or more of the standards mapped here.

The intent is simple: a sustainability officer, auditor, or CSRD reviewer should be able to read these documents alongside any GreenCalculus output and verify, line by line, that the methodology is sound.

This is not a substitute for the official standards. It is a **navigation layer** — telling you which standard governs which calculation, which version is operative, and where each emission factor in our Master Brain is sourced.

---

## The standards we map

| Layer | Standard | Operative version | Status |
|---|---|---|---|
| Calculation | [GHG Protocol Corporate Standard](./ghg-protocol/corporate-standard.md) | 2026 revision | In effect |
| Calculation | [GHG Protocol Scope 3 Standard](./ghg-protocol/scope-3-standard.md) | 2011 (revisions in progress) | In effect |
| Calculation | [GHG Protocol Land Sector & Removals Standard](./ghg-protocol/land-sector-removals-2026.md) | v1.0 — 30 Jan 2026 | Effective 1 Jan 2027 |
| Science | [IPCC AR6 — 100-year GWPs](./ipcc/ar6-gwp-100.md) | AR6 (2021) | In effect; AR7 due ~2028 |
| Verification | [ISO 14064-1](./iso/iso-14064-1.md) | 2018 revision | In effect |
| Disclosure | [CSRD / ESRS E1](./eu/csrd-esrs-e1.md) | ESRS E1 (Climate change) | Phased rollout 2024–2028 |
| Targets | [SBTi Corporate Net-Zero Standard](./targets/sbti-net-zero.md) | v1.2 | In effect |
| Factor data | [UK DEFRA / DESNZ GHG Conversion Factors](./factor-sets/uk-defra-2025.md) | 2025 v1 | In effect; 2026 set due Q3 2026 |

See [INDEX.md](./INDEX.md) for the full registry, including standards we monitor but do not yet implement.

---

## How to use this repository

**If you are a sustainability officer or auditor** — open the standard you care about and read the "How GreenCalculus implements this" section. Each document tells you which calculators on the live site use this standard, which factors are drawn from it, and which sections of our Master Brain data layer correspond.

**If you are a researcher or journalist** — every standard document includes a citation block. You may cite this repository under CC-BY-4.0 (see [LICENSE](./LICENSE)).

**If you are a developer building your own carbon tools** — the structured fields at the top of each standard document (operative version, scope, effective date, citation) are stable and machine-readable. You may copy them, fork them, or use them as a template.

---

## Citation

If you cite this repository in academic work, ESG disclosures, or methodology documents, please use:

> GreenCalculus (2026). *GreenCalculus Standards Alignment.* Version 1.0. https://github.com/greencalculus/greencalculus-standards

A formal `CITATION.cff` file is included so GitHub renders a "Cite this repository" button in the sidebar.

---

## Governance

- **Authored by** Jeremiah Say, Lead Systems Architect, GreenCalculus
- **Verified by** GreenCalculus Engineering — all standard mappings are reviewed against the official source documents before publication and on every material amendment
- **Corrections** welcomed via [GitHub Issues](https://github.com/greencalculus/greencalculus-standards/issues) or email to `jeremiah@greencalculus.com`. All accepted corrections are credited in the next changelog entry.
- **Changelog** at [CHANGELOG.md](./CHANGELOG.md) (added with first amendment)

---

## License

Content in this repository is licensed under [Creative Commons Attribution 4.0 International (CC-BY-4.0)](./LICENSE).

You may share and adapt the material for any purpose, including commercially, provided you give appropriate credit, link to the licence, and indicate if changes were made.

The full GreenCalculus calculator platform is available at [greencalculus.com](https://greencalculus.com).
