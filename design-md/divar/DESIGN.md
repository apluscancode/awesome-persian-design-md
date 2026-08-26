---
version: alpha
name: Divar-Inspired-design-analysis
description: >
  An inspired interpretation of Divar's design language — Iran's largest
  classifieds platform whose surface is a calm zinc-white canvas organized by
  a rigorous three-tier semantic token system (surface/content/border, each in
  6 intensity steps from weakest to strongest). A muted brick-red brand accent
  (#cd6767) marks identity and primary actions without ever shouting; a
  gradient assistive token (violet #5b13f7 → magenta #d80db6) is reserved for
  AI features. Typography is IRANSans at compact 0.875rem body with unitless
  line-height 2.0, radii cluster at 4px, and elevation comes from inset rings
  instead of drop shadows — the whole system reads as engineered restraint:
  a marketplace built like a design-system textbook.
colors:
  brand-default: "#cd6767"
  brand-strong: "#c32e2e"
  brand-stronger: "#8d3131"
  brand-weak: "#e88787"
  brand-weaker: "#fcc9c9"
  brand-weakest: "#fcf8f8"
  on-color: "#ffffff"
  canvas: "#ffffff"
  canvas-app: "#f4f4f5"
  ink-strongest: "#18181b"
  ink-strong: "#2a2a30"
  ink-body: "#52525b"
  ink-secondary: "#71717a"
  ink-weak: "#a1a1aa"
  ink-faint: "#c3c3c9"
  hairline: "#e4e4e7"
  surface-sunken: "#f4f4f5"
  positive-default: "#1d7c4d"
  positive-bg: "#c6f1da"
  negative-default: "#c53434"
  negative-bg: "#fcd9d9"
  warning-default: "#bb681a"
  warning-bg: "#fcdec0"
  informative-default: "#3062d4"
  informative-bg: "#d7e4ff"
  assistive-gradient-from: "#5b13f7"
  assistive-gradient-to: "#9810d7"
  inverted-surface: "#3f3f46"
typography:
  font-family-primary: "IRANSans, tahoma, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif"
  font-family-icon: "sonnat"
  display-lg:
    fontFamily: "IRANSans, sans-serif"
    fontSize: "2rem"
    fontWeight: 700
    lineHeight: "1.75"
  heading-md:
    fontFamily: "IRANSans, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 700
    lineHeight: "1.75"
  heading-sm:
    fontFamily: "IRANSans, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 700
    lineHeight: "2"
  body-lg:
    fontFamily: "IRANSans, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: "2"
  body-md:
    fontFamily: "IRANSans, sans-serif"
    fontSize: ".875rem"
    fontWeight: 400
    lineHeight: "2"
  body-sm:
    fontFamily: "IRANSans, sans-serif"
    fontSize: ".75rem"
    fontWeight: 400
    lineHeight: "2"
  caption-xs:
    fontFamily: "IRANSans, sans-serif"
    fontSize: ".625rem"
    fontWeight: 400
    lineHeight: "1.5"
  button-label:
    fontFamily: "IRANSans, sans-serif"
    fontSize: ".875rem"
    fontWeight: 500
    lineHeight: "1.5"
  price-emphasis:
    fontFamily: "IRANSans, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 700
    lineHeight: "1.5"
rounded:
  xs: "2px"
  sm: "4px"
  md: "8px"
  lg: "12px"
  xl: "16px"
  xxl: "14px"
  pill: "9999px"
  circle: "50%"
spacing:
  xxs: "2px"
  xs: "4px"
  sm: "6px"
  md: "8px"
  lg: "10px"
  xl: "12px"
  xxl: "14px"
  xxxl: "16px"
  huge: "24px"
  band: "32px"
  section: "48px"
components:
  nav-bar:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink-strong}"
    height: "72px desktop / 56px mobile"
    sticky: true
  city-selector:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink-body}"
    borderColor: "{colors.hairline}"
  search-bar:
    backgroundColor: "{colors.surface-sunken}"
    rounded: "{rounded.sm}"
  button-primary:
    backgroundColor: "rgb(var(--surface-brand-strong))"
    textColor: "{colors.on-color}"
    rounded: "{rounded.sm}"
    typography: "{typography.button-label}"
    padding: "10px 16px"
  button-secondary:
    backgroundColor: "{colors.canvas}"
    textColor: "rgb(var(--content-brand-strong))"
    borderColor: "rgb(var(--border-brand-strong))"
    rounded: "{rounded.sm}"
  card-post:
    backgroundColor: "{colors.canvas}"
    borderBottom: "1px solid {colors.hairline}"
    padding: "16px"
    layout: "thumbnail-right (RTL), title + price + meta left"
  chip-category:
    backgroundColor: "{colors.surface-sunken}"
    textColor: "{colors.ink-body}"
    rounded: "{rounded.sm}"
    padding: "8px 12px"
  badge-negotiable:
    backgroundColor: "{colors.positive-bg}"
    textColor: "{colors.positive-default}"
    rounded: "{rounded.xs}"
  chat-fab:
    backgroundColor: "rgb(var(--surface-brand-strong))"
    textColor: "{colors.on-color}"
    shape: "{rounded.circle}"
footer:
  backgroundColor: "{colors.canvas-app}"
---

## Overview

Divar (دیوار) is Iran's dominant classifieds platform (~30M monthly visits) — the Persian Craigslist meets Wallapop. Its design system is the **most disciplined token architecture among Iranian products**: everything routes through a three-axis semantic model (`surface` / `content` / `border`), each axis scaled across six intensity steps (`weakest → weaker → default → strong → stronger → strongest`). No raw hex values appear inside component CSS — only `rgb(var(--token))` references. This makes theming (including full dark mode) trivial and keeps visual consistency mechanical rather than aspirational.

The brand accent is a **muted brick red** (`--content-brand-strong` = `#c32e2e`, default `#cd6767`) — deliberately desaturated compared to Digikala's crimson. It signals Divar's personality: trustworthy utility, not urgency. Red appears on primary buttons ("ثبت آگهی" / post an ad), active states, and the logo — but product cards stay almost monochrome, letting photos carry color.

Its most distinctive token is **assistive**: a violet→magenta gradient (`#5b13f7 → #9810d7`) reserved exclusively for AI-powered features (smart search, auto-descriptions). When you see this gradient, an LLM is behind it — a clever visual contract.

Typography is **IRANSans** (the classic Iranian web face, predecessor to Yekan) with a custom icon face called `sonnat`. Body text sits at compact `.875rem` (14px) with unitless line-height **2.0** — again the Persian legibility rule, but tighter than Digikala's 2.15. Radii are modest (4px workhorse) and elevation uses **inset ring shadows** (`inset 0 0 0 1px …`) rather than drop shadows — borders are simulated with box-shadows to keep hairlines crisp on all DPIs.

## Colors

### Token Architecture (the defining trait)

Every color exists in three parallel axes × six steps. Components never hardcode values:

| Axis | Role |
|------|------|
| `--surface-*` | Backgrounds, fills |
| `--content-*` | Text, icons |
| `--border-*` | Outlines, dividers |

Intensity scale (same for all hues): `weakest → weaker → default → strong → stronger → strongest`.

### Brand

- **Brand Strong** (`rgb(195,46,46)` ≈ `#c32e2e`): Primary buttons, logo mark, active indicators.
- **Brand Default** (`rgb(205,103,103)` ≈ `#cd6767`): Muted rose for secondary emphasis.
- **Brand Weaker/Weakest** (`#fcc9c9` / `#fcf8f8`): Tonal washes for hover states and subtle backgrounds.

### Neutral Scale (zinc family)

| Step | Value | Use |
|------|-------|-----|
| neutral-weaker | #ffffff | Page canvas |
| neutral-weak | #f4f4f5 | Sunken surfaces, chips |
| neutral-default | #e4e4e7 | Hairlines, disabled |
| strong | #c3c3c9 | Borders on interactive |
| stronger | #a1a1aa | Placeholder icons |
| strongest | #52525b | Secondary text |

### Text (Content)

- **Strongest** (`rgb(42,42,48)` ≈ `#2a2a30`): Headlines, prices.
- **Default** (`rgb(113,113,122)` ≈ `#71717a`): Body copy — notably NOT pure black; Divar's body text is mid-gray by default, flipping to stronger for emphasis.
- **Weak** (`rgb(161,161,170)`): Meta info, timestamps.

### Semantic

- **Positive** (`#1d7c47` text on `#c6f1da` bg): "توافقی" (negotiable) tags, available status.
- **Negative** (`#c53434` on `#fcd9d9`): Sold/expired listings, errors.
- **Warning** (`#bb681a` on `#fcdec0`): "در انتظار تأیید" pending states.
- **Informative** (`#3062d4` on `#d7e4ff`): System notices, tips.
- **Assistive** (gradient `#5b13f7→#9810d7`): AI features ONLY — smart filters, auto-reply suggestions.

## Typography

### Font Family

- **IRANSans** (weights 300/400/500/700) — the veteran Persian UI face. Fallback chain includes tahoma then system stack.
- **sonnat** — custom icon font (weight 400 only).
- No Latin-first faces; Latin glyphs render via IRANSans's built-in subset.

### Hierarchy

| Token | Size | Weight | Line Height | Use |
|-------|------|--------|-------------|-----|
| `{typography.display-lg}` | 2rem | 700 | 1.75 | Landing heroes |
| `{typography.heading-md}` | 1.25rem | 700 | 1.75 | Section headers |
| `{typography.heading-sm}` | 1.125rem | 700 | 2.0 | Card titles |
| `{typography.price-emphasis}` | 1.125rem | 700 | 1.5 | Listing prices |
| `{typography.body-lg}` | 1rem | 400 | 2.0 | Descriptions |
| `{typography.body-md}` | .875rem | 400 | 2.0 | Default body — most common size (x77) |
| `{typography.body-sm}` | .75rem | 400 | 2.0 | Meta, timestamps (x75 occurrences) |
| `{typography.caption-xs}` | .625rem | 400 | 1.5 | Fine print |
| `{typography.button-label}` | .875rem | 500 | 1.5 | Buttons |

### Principles

- **Unitless line-height 2.0 dominates** (86 occurrences) — the Persian breathing rule, one notch tighter than Digikala.
- **Compact sizes**: body defaults DOWN to 14px, meta at 12px — density over airiness.
- **Weight range narrow**: 300/400/500/700 only. No black weights anywhere.

## RTL & BiDi Rules ✨

- Document: `<html dir="rtl" lang="fa">`.
- Post-card layout: thumbnail on RIGHT (first in flex order), text flows left.
- Price format: «۱۲٬۵۰۰٬۰۰۰ تومان» — number then currency, Persian thousands separator «٬».
- Negotiability tag («توافقی») replaces price where applicable — never both.
- City/location always precedes title in metadata rows: «تهران، نیاوران».
- Directional icons mirror; the "back" chevron points right.
- Chat bubbles: user messages align LEFT (mirrored from Western right-alignment).

## Layout

### Spacing System

- Base unit: **4px**. Frequency: 8px (×313!) > 16px (×252) > 4px > 24px > 32px.
- The 8px rhythm rules everything — tighter than Digikala's 16px preference.
- List rows: 16px vertical padding; section bands: 32-48px separation.

### Grid & Container

- Desktop container: max-width **1024px** (narrower than e-commerce — classifieds are list-centric).
- Breakpoints: **768px** primary fork (43 queries), 520px mobile refinement, 960/1024px desktop.
- Post lists are single-column rows (not card grids) — scannability over imagery.

### Responsive Strategy

| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | < 768px | Bottom nav FABs, single column, sticky post-button |
| Phablet | 768-959px | Two-column category tiles |
| Desktop | ≥ 960px | Persistent sidebar filters, wider cards |

## Elevation & Depth

Divar's signature move: **inset ring shadows simulate borders** so they render pixel-perfect at any zoom/DPI:

| Level | Treatment | Use |
|-------|-----------|-----|
| Level 0 — Flat | Nothing | Page background |
| Level 1 — Ring | `inset 0 0 0 1px #e4e4e7, inset 0 0 0 1px #fff` | Cards, inputs (double-ring trick) |
| Level 2 — Positive Ring | `inset 0 0 0 1px #1d7c4d…` | Selected/success states |
| Level 3 — Float | `0 8px 16px rgba(0,0,0,.16)` | Modals, dropdowns, sticky bars |

True drop shadows exist ONLY at overlay level — surfaces communicate through rings and fills.

## Shapes

| Token | Value | Use |
|-------|-------|-----|
| `{rounded.xs}` | 2px | Tiny inline tags |
| `{rounded.sm}` | 4px | Buttons, inputs, chips — workhorse |
| `{rounded.md}` | 8px | Image containers, modals |
| `{rounded.lg}` | 12-16px | Hero panels |
| `{rounded.pill}` | 9999px | Status pills |
| `{rounded.circle}` | 50% | Avatars, chat FAB |

## Components

### Buttons

**`button-primary`** — brick red fill (`surface-brand-strong`), white label, 4px radius. Reserved for "ثبت آگهی" and confirmation moments. One per screen maximum.

**`button-secondary`** — outline variant: white bg, brand-red border+text. For "تماس با فروشنده", "چت".

**`button-ghost`** — borderless gray-text for tertiary actions.

### Cards & Containers

**`card-post`** — THE atomic listing unit. Full-width row, white bg, bottom hairline, thumbnail right (RTL-first element), title in heading-sm (single line ellipsis), price in price-emphasis or «توافقی» tag, meta row (city · neighborhood · time-ago) in body-sm weak. No borders between columns — pure typographic hierarchy.

**`chip-category`** — sunken-gray square-ish tile (4px radius) with icon top, label below. Horizontal scroll rail on homepage.

**`badge-status`** — semantic wash pills: توافقی (positive), فروخته شده (negative), در انتظار (warning).

### Inputs & Forms

**`search-bar`** — sunken fill, 4px radius, magnifier icon right. The homepage hero IS the search bar plus city selector — no illustration, no banner.

**`filter-rail`** — persistent checkbox groups with nested categories; selected counts show in informative-blue pills.

### Navigation

**`nav-bar`** — white sticky, logo right, city selector + search center, "ثبت آگهی" primary CTA far left (RTL end).

**Mobile bottom bar** — five items: آگهی‌ها، چت، [＋ ثبت آگهی FAB], نشان‌ها، منو. The center FAB is the revenue action, always thumb-reachable.

### Signature Components

**`chat-intro`** — Divar's moat is anonymous chat; intro bubbles use informative-blue wash with sender avatar circle.

**`ai-assist-pill`** — any AI feature wears the assistive gradient border/text. Instantly distinguishable from human actions.

**`real-estate-specs-row`** — meter²/room/year icons inline with values in body-sm — domain-specific metadata pattern for property listings.

## Agent Prompt Guide

```
Colors:   canvas #fff · sunken #f4f4f5 · text #2a2a30/#71717a/#a1a1aa ·
          brand #c32e2e · success #1d7c4d on #c6f1da · ring #e4e4e7
          AI gradient: linear-gradient(90deg,#5b13f7,#9810d7)
Font:     IRANSans (fallback Vazirmatn) · body 14px/2.0 · headings 700
Radius:   4px everywhere · media/modals 8px · pills 9999px
Spacing:  8px base rhythm · rows 16px · sections 32-48px
RTL:      dir="rtl" lang="fa" · thumbnail-RIGHT cards · Persian numerals
Shadow:   inset rings for borders · real shadow ONLY overlays (0 8px 16px)
Density:  single-column listing rows · compact 14px body · 44px targets
```

**Sample prompt:**
> "Build a classifieds feed following DESIGN.md: single-column white post cards separated by hairlines, thumbnail right side, title + price + city/time meta, brick-red (#c32e2e) primary 'post ad' button, IRANSans 14px/2.0 typography, inset-ring borders, sticky header with city selector, RTL."

## Do's and Don'ts

### Do

- Route every color through the semantic token axes (`surface/content/border` × intensity); never hardcode hex inside components.
- Keep the brand red muted and scarce — it's a trust signal, not a sale siren.
- Use inset ring shadows for borders; they're DPI-proof and dark-mode-ready.
- Reserve the violet-magenta gradient exclusively for AI features — it's a visual contract with users.
- Set Persian body at 14px minimum with line-height 2.0.
- Show «توافقی» INSTEAD of price, never alongside it.
- Keep listing rows single-line-title with ellipsis; scannability beats completeness.

### Don't

- Don't use pure black text — the zinc scale (#18181b ceiling) keeps warmth.
- Don't apply drop shadows to non-overlay elements; rings are the elevation system.
- Don't introduce a second accent hue; semantic colors already cover feedback states.
- Don't use heavy font weights (800+) — IRANSans tops out at 700 and stays elegant.
- Don't place thumbnails on the LEFT in RTL layouts.
- Don't mix Latin digits into Persian prose paragraphs (prices excepted per convention).
- Don't let AI-styled elements (gradient) touch regular CRUD interactions.
