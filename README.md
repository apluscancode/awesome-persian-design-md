# 🇮🇷 Awesome Persian DESIGN.md

**A curated collection of DESIGN.md files for Persian (Farsi) brand design systems.**

Drop a `DESIGN.md` into your project, tell your AI agent *"build me a page that looks like Digikala"* — and generate high-quality, culturally-authentic, **RTL-ready** Persian UI.

Built on the [Stitch DESIGN.md format](https://stitch.withgoogle.com/docs/design-md/overview/) (same as [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md)) — extended for Persian typography, RTL layout systems, and Iranian brand aesthetics.

---

## چرا این ریپو؟ / Why this repo?

Global design-token repos assume LTR, Latin typography, and Western UI conventions. Persian products live in a different reality:

- **RTL is not "mirrored CSS"** — numerals, mixed-direction text, icon direction, and progress metaphors all behave differently
- **Persian web fonts are a real constraint** — Vazirmatn, IRANSans, Yekan Bakh each carry different weights, metrics, and licensing
- **Iranian brands have distinct visual languages** — from Digikala's dense marketplace red to Snapp's friendly green to Divar's utilitarian blue

This repo documents all of it in agent-readable Markdown.

## What is DESIGN.md?

A plain-text design system document that AI agents read to generate consistent UI. No Figma exports. No JSON schemas. Just Markdown:

| File | Who reads it | What it defines |
|------|--------------|-----------------|
| `AGENTS.md` | Coding agents | How to build the project |
| `DESIGN.md` | Design agents | How the project should look and feel |

## Collection

> 🚧 Work in progress — sites are added as they are analyzed.

| Brand | Category | DESIGN.md | Status |
|-------|----------|-----------|--------|
| [Digikala (دیجی‌کالا)](https://digikala.com) | E-commerce marketplace | [design-md/digikala/DESIGN.md](design-md/digikala/DESIGN.md) · [preview](design-md/digikala/preview.html) | ✅ v1 |
| [Divar (دیوار)](https://divar.ir) | Classifieds / marketplace | [design-md/divar/DESIGN.md](design-md/divar/DESIGN.md) · [preview](design-md/divar/preview.html) | ✅ v1 |
| [Snapp (اسنپ)](https://snapp.ir) | Super-app / ride-hailing | [design-md/snapp/DESIGN.md](design-md/snapp/DESIGN.md) · [preview](design-md/snapp/preview.html) | ✅ v1 |

### Requested / Roadmap
- Cafe Bazaar (کافه‌بازار) — app store
- Aparat (آپارات) — video platform
- Torob (ترب) — price comparison
- Alibaba.ir (علی‌بابا) — travel

## What's Inside Each DESIGN.md

Every file follows the Stitch DESIGN.md spec with Persian-specific extensions:

| # | Section | What it captures |
|---|---------|------------------|
| 1 | Visual Theme & Atmosphere | Mood, density, design philosophy |
| 2 | Color Palette & Roles | Semantic name + hex + functional role |
| 3 | Typography Rules | **Persian font stack**, full hierarchy table, Latin-fallback pairing |
| 4 | **RTL & BiDi Rules** ✨ | Direction logic, numeral policy (۰۱۲۳ vs 0123), mirrored icons, mixed-content handling |
| 5 | Layout Principles | Spacing scale, grid, whitespace philosophy |
| 6 | Depth & Elevation | Shadow system, surface hierarchy |
| 7 | Do's and Don'ts | Design guardrails and anti-patterns |
| 8 | Agent Prompt Guide | Ready-to-use prompts for coding agents |

✨ = extension beyond the base Stitch spec, required for Persian UI quality

Each site folder includes:
| File | Purpose |
|------|---------|
| `DESIGN.md` | The design system (what agents read) |
| `preview.html` | Visual catalog — RTL, color swatches, type scale, buttons, cards |

## How to Use

1. Copy a site's `DESIGN.md` into your project root
2. Tell your AI agent:
   ```
   Read DESIGN.md and build a product page matching this design system.
   All text in Persian, RTL layout.
   ```

## Contributing

Found a wrong hex value? Missing a token? Analyzed a new Iranian site?

1. Open an issue describing the change
2. Follow the same structure as existing files
3. PRs welcome!

**Analysis method:** computed styles extracted from the live site → semantic tokens → verified against multiple pages of the product.

## License

MIT. Extracted tokens represent publicly visible CSS values; we claim no ownership of any brand's visual identity.
