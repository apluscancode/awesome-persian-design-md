---
version: alpha
name: Snapp-Inspired-design-analysis
description: >
  An inspired interpretation of Snapp's design language — Iran's super-app
  (ride-hailing, food delivery, fintech and 15+ verticals) whose defining
  trait is a runtime theme-switching architecture: one obfuscated-token
  system, fifteen brand palettes. Setting data-panda-theme="taxi" repaints
  the entire UI in Snapp green (#06d170); "food" turns hot pink (#ff00a6);
  "express" turns orange (#ff661f). Light mode is a clean white canvas with
  slate-ink text; dark mode (`.dark` class, 194 tokens) flips to deep navy
  surfaces (#070814). Typography is IRANSansX FaNum — the modern successor
  to IRANSans with built-in Persian digits — at compact 14px body. Radii are
  fully rounded pills for actions, shadows use layered cool-gray tints, and
  spacing follows an 8px rhythm. The system reads as a Figma-compiled design
  pipeline: machine-generated token names, human-designed semantics.
colors:
  brand-taxi: "#06d170"
  brand-taxi-dark: "#9fb2ff"
  brand-food: "#ff00a6"
  brand-express: "#ff661f"
  brand-trip: "#ff4340"
  brand-club: "#ffce00"
  brand-insurance: "#028ef9"
  brand-doctor: "#58c0f9"
  brand-market-primary: "#ff661f"
  brand-market-deep: "#0a2cdc"
  brand-pay: "#008efa"
  brand-shop: "#b400ae"
  brand-pro: "#00a399"
  brand-ticket: "#6e1ec3"
  brand-wallet: "#000000"
  brand-investment: "#edb727"
  default-primary: "#575eff"
  default-green: "#21aa58"
  canvas-light: "#ffffff"
  canvas-dark: "#070814"
  surface-dark-raised: "#232631"
  surface-sunken-light: "#ebecf2"
  ink-strongest: "#252a3c"
  ink-body: "#686c79"
  ink-on-dark: "#fafafa"
  hairline-light: "#ebecf2"
  hairline-dark: "#ebecf21f"
typography:
  font-family: "IRANSansXFaNum, IRANSansX, sans-serif"
  display-hero:
    fontFamily: "IRANSansXFaNum, sans-serif"
    fontSize: "32px"
    fontWeight: 700
    lineHeight: "1.6"
  heading-lg:
    fontFamily: "IRANSansXFaNum, sans-serif"
    fontSize: "22px"
    fontWeight: 700
    lineHeight: "1.6"
  heading-md:
    fontFamily: "IRANSansXFaNum, sans-serif"
    fontSize: "20px"
    fontWeight: 700
    lineHeight: "1.7"
  heading-sm:
    fontFamily: "IRANSansXFaNum, sans-serif"
    fontSize: "17px"
    fontWeight: 700
    lineHeight: "1.7"
  body-md:
    fontFamily: "IRANSansXFaNum, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: "1.9"
  body-sm:
    fontFamily: "IRANSansXFaNum, sans-serif"
    fontSize: "12px"
    fontWeight: 400
    lineHeight: "1.8"
  button-label:
    fontFamily: "IRANSansXFaNum, sans-serif"
    fontSize: "14px"
    fontWeight: 600
    lineHeight: "1.5"
  price-fanum:
    fontFamily: "IRANSansXFaNum, sans-serif"
    fontSize: "17px"
    fontWeight: 700
    lineHeight: "1.5"
rounded:
  pill-button: "9999px"
  md: "8px"
  lg: "12px"
  circle: "50%"
spacing:
  xs: "4px"
  sm: "6px"
  md: "8px"
  lg: "12px"
  xl: "16px"
  xxl: "24px"
  xxxl: "32px"
  section: "40px"
components:
  nav-bar:
    backgroundColor: "{canvas-light}"
    textColor: "{ink-strongest}"
    height: "64px desktop / sticky"
  theme-root:
    attribute: "data-panda-theme"
    values: "taxi | food | express | trip | club | insurance | doctor | market | pay | shop | pro | ticket | wallet | investment | default"
  dark-mode:
    classTrigger: ".dark on <html>"
    canvasDark: "{canvas-dark}"
  button-pill-primary:
    backgroundColor: "theme primary (--fNluSm)"
    textColor: "#ffffff"
    rounded: "{rounded.pill-button}"
    padding: "10px 24px"
  card-service:
    backgroundColor: "{canvas-light}"
    rounded: "{rounded.md}"
    shadow: "0 2px 2px rgba(97,100,117,.06), 0 3px 1px rgba(97,100,117,.04), 0 1px 5px rgba(97,100,117,.12)"
---

## Overview

Snapp is Iran's super-app: ride-hailing at its core, wrapped around food delivery (Snappfood), express courier, fintech (SnappPay), investment, insurance, and a dozen more verticals. Its design system answers a hard question — *how does one product wear fifteen brand identities without becoming incoherent?* — with a **runtime theme engine**: a single set of semantic component styles reads from CSS custom properties whose values swap based on a `data-panda-theme` attribute. Set it to `taxi` and every accent becomes Snapp's signature green `#06d170`; switch to `food` and the same UI renders hot pink `#ff00a6`; `express` goes orange `#ff661f`; `wallet` goes pure black.

The implementation is unmistakably **Figma Tokens → compiled CSS**: token names are build-minified (`--fNluSm`, `--hFZWLg`, `--bZcRGw`) via Panda CSS, each theme ships exactly **40 parallel slots** (primary/strong/stronger + tonal washes + alpha variants like `#06d17014`), and dark mode arrives as a separate `.dark` class flipping all 194 tokens to deep-navy surfaces (`#070814`) with softened accents (`#06d170` becomes periwinkle `#9fb2ff` in dark taxi).

Light mode is a calm white canvas with slate ink (`#252a3c` strongest, `#686c79` body). Actions are **fully-rounded pills**; cards float on layered cool-gray shadows (`#616475` tinted, three stacked layers each). Typography moved from legacy IRANSans to **IRANSansX FaNum** — Persian digits baked into the font itself, no JS digit-conversion needed. Body text sits at 14px/1.9, headings bold at 17–32px.

## Colors

### Theme Matrix (the core innovation)

Fifteen themes × identical slot structure. Primary color per theme:

| Theme | data-panda-theme | Primary | Darkened |
|-------|------------------|---------|----------|
| Taxi (core) | `taxi` | `#06d170` green | `#04924e` |
| Food | `food` | `#ff00a6` pink | `#b30074` |
| Express | `express` | `#ff661f` orange | `#b34716` |
| Trip | `trip` | `#ff4340` red | `#b32f2d` |
| Club (loyalty) | `club` | `#ffce00` yellow | `#b39000` |
| Insurance | `insurance` | `#028ef9` blue | `#0163ae` |
| Doctor | `doctor` | `#58c0f9` sky | `#3e86ae` |
| Market (super app store) | `market` | `#ff661f` + deep blue `#0a2cdc` dual | `#071f9a` |
| Pay (fintech) | `pay` | `#008efa` blue | `#0063af` |
| Shop | `shop` | `#b400ae` magenta | `#7e007a` |
| Pro (drivers) | `pro` | `#00a399` teal | `#00726b` |
| Ticket | `ticket` | `#6e1ec3` violet | `#4d1588` |
| Wallet | `wallet` | `#000000` black | `#000000` |
| Investment | `investment` | `#edb727` gold | `#a6801b` |
| Default (marketing site) | `default` | `#575eff` indigo + `#21aa58` green dual | `#3d42b3` |

Each theme also defines: hover-stronger, disabled-alpha (`14` hex alpha), focus-ring (`1f` alpha), tonal washes (`e6faf1` family), and border variants — 40 slots total, perfectly parallel across all 15 themes.

### Neutrals

- **Light canvas:** `#ffffff`, sunken `#ebecf2`
- **Ink:** strongest `#252a3c` (slate), body `#686c79`, faint `#a0a2aa`
- **Dark canvas** (`.dark`): page `#070814`, raised `#232631`, elevated `#262934`
- **Dark ink:** text flips to `#fafafa`, secondary `#a0a2aa`

### Dark Mode

Toggled by `.dark` class on `<html>`. Not simple inversion — a curated navy-tinted palette: backgrounds lean blue-black (`#070814`, `#0a0b1f`), greens soften (`#06d170` → `#9fb2ff` for taxi links), and every alpha token re-derives against the dark base.

## Typography

### Font Family

**IRANSansXFaNum** (4 weights loaded) — the X generation of Iran's standard face with **FaNum feature: Persian numerals (۰۱۲۳) render natively**, eliminating client-side digit conversion. Fallbacks: `ui-sans-serif, system-ui`.

### Hierarchy

| Token | Size | Weight | Line Height | Use |
|-------|------|--------|-------------|-----|
| `{typography.display-hero}` | 32px | 700 | 1.6 | Homepage H1 ("تجربه‌ی زندگی راحت‌تر…") |
| `{typography.heading-lg}` | 22px | 700 | 1.6 | Section headlines |
| `{typography.heading-md}` | 20px | 700 | 1.7 | Card group titles |
| `{typography.heading-sm}` | 17px | 700 | 1.7 | Service card titles |
| `{typography.price-fanum}` | 17px | 700 | 1.5 | Prices (native Persian digits) |
| `{typography.body-md}` | 14px | 400 | 1.9 | Default body |
| `{typography.body-sm}` | 12px | 400 | 1.8 | Meta, captions |
| `{typography.button-label}` | 14px | 600 | 1.5 | Pill buttons |

### Principles

- **Line-height ~1.6–1.9** — tighter than Digikala/Divar because IRANSansX has shorter descenders and the product leans modern-tech, not document-style.
- **Native FaNum digits everywhere** — prices, counters, timestamps never need `toLocaleString('fa')`.
- Weight ceiling is 700; hierarchy comes from size steps, not heaviness.

## RTL & BiDi Rules ✨

- `<html lang="fa" dir="rtl">` set server-side.
- Super-app service tiles flow right→left in carousels.
- Ride-tracking maps keep LTR geography but RTL chrome (buttons, sheets).
- Price format: «۱۲۵٬۰۰۰ تومان» with native FaNum digits.
- Phone numbers stay LTR inside RTL sentences (`dir="ltr"` spans).
- Directional chevrons mirror; brand glyphs (Snapp logo, category icons) never mirror.

## Layout

### Spacing System

- Base: 8px rhythm. Frequency: 12px > 8px > 24px ≈ 6px ≈ 40px > 4px.
- Section bands: 40px vertical; card internals: 12–16px.

### Grid & Container

- Marketing container ~1200px centered.
- Service grids: 4-up desktop, 2-up mobile.
- Breakpoints minimal: single formal breakpoint at **600px** (mobile-first elsewhere via fluid layout).

### Responsive Strategy

| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | < 600px | Single column, full-width pill buttons, bottom-sheet patterns |
| Desktop | ≥ 600px | Multi-column service grid, side-by-side hero panels |

## Elevation & Depth

Layered three-stack cool-gray shadows — a Material-3-inspired recipe:

| Level | Treatment | Use |
|-------|-----------|-----|
| Level 0 | None | Flat lists |
| Level 1 | `0 2px 2px #6164750f, 0 3px 1px #6164750a, 0 1px 5px #6164751f` | Service cards, chips |
| Level 2 | `0 4px 5px #6164750f, 0 1px 10px #6164750a, 0 2px 4px #6164751f` | Hovered cards, small popovers |
| Level 3 | `0 12px 17px #6164750f, 0 5px 22px #0000000a, 0 7px 8px #6164751f` | Modals, map sheets |

The `#616475` (cool slate) tint keeps shadows soft-blue rather than muddy gray — subtle but deliberate.

## Shapes

| Token | Value | Use |
|-------|-------|-----|
| `{rounded.pill-button}` | 9999px | ALL buttons, search bars, toggle chips |
| `{rounded.md}` | 8px | Cards, inputs, thumbnails |
| `{rounded.lg}` | 12px | Map containers, hero media |
| `{rounded.circle}` | 50% | Avatars, driver photo rings |

Pill-shape buttons are Snapp's most recognizable silhouette — friendlier than Divar's squares, softer than Digikala's 8px rectangles.

## Components

### Buttons

**`button-pill-primary`** — theme-colored fully-rounded CTA. Background reads `var(--fNluSm)` so the SAME component renders green in taxi context, pink in food context. White label, 10×24px padding.

**`button-pill-outline`** — white bg, theme-color border/text.

### Cards & Containers

**`card-service`** — the super-app tile: white bg, 8px radius, icon top (theme-tinted), label below, Level-1 shadow. Grid of these IS the Snapp homepage identity.

**`card-ride-summary`** — map thumbnail + driver info + price row; uses informative tokens for trip states.

**`banner-promo`** — tonal wash background (`--ewxSWa` family, e.g. `#e6faf1` for taxi) with theme-colored headline — never the raw saturated accent as fill.

### Inputs

**`search-pill`** — fully rounded, sunken `#ebecf2` fill, magnifier right (RTL), expands into overlay with recent + suggested queries.

### Navigation

**`nav-bar`** — white sticky header: logo right, services dropdown center, login/pill CTA left.

**Mobile tab bar** — five slots with the center action highlighted in theme color; switches hue per active vertical.

### Signature Components

**`theme-demo-switcher`** — marketing homepage includes a live vertical picker that flips `data-panda-theme` in real-time, demonstrating the whole system in one interaction.

**`price-fanum`** — prices always render in native Persian digits via font feature, weight 700, currency «تومان» trailing.

**`dark-map-sheet`** — ride screens combine LTR map tiles with RTL info sheets using the dark navy palette regardless of system theme.

## Agent Prompt Guide

```
Theme:   set data-panda-theme=<vertical>; primary auto-resolves
         taxi #06d170 · food #ff00a6 · express #ff661f · pay #008efa
Canvas:  light #fff · dark (.dark class) #070814 · sunken #ebecf2
Ink:     light #252a3c/#686c79 · dark #fafafa/#a0a2aa
Font:    IRANSansXFaNum · body 14px/1.9 · headings 700 · native ۰۱۲۳ digits
Shape:   pill buttons (9999px) · cards 8px · avatars circle
Shadow:  layered #616475 stacks (see levels) · flat otherwise
Spacing: 8px base · sections 40px · cards 12-16px
RTL:     dir=rtl lang=fa · mirrored icons · phone numbers dir=ltr
```

**Sample prompt:**
> "Build a service landing page following DESIGN.md with data-panda-theme='taxi': white canvas, green (#06d170) pill CTAs, 4-column service card grid with soft slate shadows, IRANSansXFaNum 14px body, native Persian digits, sticky white nav with rounded search bar, RTL layout."

## Do's and Don'ts

### Do

- Always scope components to `data-panda-theme` — never hardcode a vertical's hex into shared components.
- Use IRANSansXFaNum's native Persian digits for ALL numbers; no JS conversion layers.
- Keep buttons fully pill-shaped (9999px) — this is Snapp's silhouette.
- Layer shadows from the `#616475` recipe; never plain black shadows.
- In dark mode, use the SOFTENED accent set (`#9fb2ff` etc.), not the saturated light-mode values.
- Let each vertical own its hue completely while on that vertical — mixing taxi-green and food-pink in one view breaks the mental model.

### Don't

- Don't introduce a sixteenth accent color outside the theme matrix.
- Don't use square (≤4px radius) buttons anywhere; pills only.
- Don't set body text above 15px or below 12px — the scale is deliberately compact.
- Don't apply the AI/assistive gradient concept here (that's Divar); Snapp expresses verticals through solid hues.
- Don't mix two theme hues in a single screen outside the marketing homepage's showcase section.
- Don't forget `.dark` overrides — every new component needs its 194-token dark story.
