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

This repository is the **open-methodology mirror**. The canonical, fully-styled standards pages live at [greencalculus.com/standards](https://greencalculus.com/standards/) — each standard below links to both the GitHub markdown summary and the live reference page.

---

## The standards we map

Each row links to the GitHub mapping document and the live reference page on greencalculus.com.

| Layer | Standard | Operative version | Live reference |
|---|---|---|---|
| Calculation | [GHG Protocol Corporate Standard](./ghg-protocol/corporate-standard.md) | 2026 revision | [Live page →](https://greencalculus.com/standards/ghg-protocol-corporate-standard/) |
| Calculation | [GHG Protocol Scope 3 Standard](./ghg-protocol/scope-3-standard.md) | 2011 (revisions in progress) | [Live page →](https://greencalculus.com/standards/ghg-protocol-scope-3-standard/) |
| Calculation | [GHG Protocol Land Sector & Removals](./ghg-protocol/land-sector-removals-2026.md) | v1.0 — 30 Jan 2026 (effective 1 Jan 2027) | Live page pending |
| Science | [IPCC AR6 — 100-year GWPs](./ipcc/ar6-gwp-100.md) | AR6 (2021) | [Live page →](https://greencalculus.com/standards/ipcc-ar6/) |
| Verification | [ISO 14064-1](./iso/iso-14064-1.md) | 2018 revision | [Live page →](https://greencalculus.com/standards/iso-14064-1/) |
| Disclosure | [CSRD / ESRS E1](./eu/csrd-esrs-e1.md) | ESRS E1 (Climate change) | [Live page →](https://greencalculus.com/standards/csrd-esrs-e1/) |
| Targets | [SBTi Corporate Net-Zero](./targets/sbti-net-zero.md) | v1.2 | [Live page →](https://greencalculus.com/standards/sbti-corporate-net-zero-standard/) |
| Factor data | [UK DEFRA / DESNZ Conversion Factors](./factor-sets/uk-defra-2025.md) | 2025 v1 | [Live page →](https://greencalculus.com/standards/uk-defra-emission-factors/) |

See [INDEX.md](./INDEX.md) for the full registry, including standards we monitor but do not yet implement.

---

## How to use this repository

**If you are a sustainability officer or auditor** — open the standard you care about and read the "How GreenCalculus implements this" section. Each document tells you which calculators on the live site use this standard, and links to the canonical reference page at [greencalculus.com/standards](https://greencalculus.com/standards/).

**If you are a researcher or journalist** — every standard document includes a citation block. You may cite this repository under CC-BY-4.0 (see [LICENSE](./LICENSE)). The live reference at [greencalculus.com](https://greencalculus.com) is the canonical version.

**If you are a developer building your own carbon tools** — the structured fields at the top of each standard document (operative version, scope, effective date, citation) are stable and machine-readable. You may copy them, fork them, or use them as a template.

---

## Citation

If you cite this repository in academic work, ESG disclosures, or methodology documents, please use:

> GreenCalculus (2026). *GreenCalculus Standards Alignment.* Version 1.0. https://github.com/greencalculus/greencalculus-standards

The canonical, fully-cited version of each standard mapping is at [greencalculus.com/standards](https://greencalculus.com/standards/).

A formal `CITATION.cff` file is included so GitHub renders a "Cite this repository" button in the sidebar.

---

## Governance

- **Authored by** Jeremiah Say, Lead Systems Architect, GreenCalculus
- **Verified by** GreenCalculus Engineering — all standard mappings are reviewed against the official source documents before publication and on every material amendment
- **Corrections** welcomed via [GitHub Issues](https://github.com/greencalculus/greencalculus-standards/issues) or email to `jeremiah@greencalculus.com`. All accepted corrections are credited in the next changelog entry on [greencalculus.com/changelog](https://greencalculus.com/changelog/).
- **Changelog** — material amendments to standard mappings are recorded at [CHANGELOG.md](./CHANGELOG.md) (created with first amendment) and mirrored to the live changelog.

---

## License

Content in this repository is licensed under [Creative Commons Attribution 4.0 International (CC-BY-4.0)](./LICENSE).

You may share and adapt the material for any purpose, including commercially, provided you give appropriate credit, link to the licence, and indicate if changes were made.

The full GreenCalculus calculator platform is available at [greencalculus.com](https://greencalculus.com).
