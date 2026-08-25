---
version: alpha
name: Digikala-Inspired-design-analysis
description: >
  An inspired interpretation of Digikala's design language — Iran's largest
  e-commerce marketplace whose surface is a dense, utilitarian white canvas
  ruled by a single crimson-red brand accent (#ef4056), IRANYekan typography
  set at generous 2.1x line-height for Persian legibility, and a component
  library engineered for high-velocity shopping: tight 8px-radius cards,
  hairline dividers, and a semantic color system that color-codes entire
  business verticals (Fresh green, Plus purple, Jet purple-pink, Digipay blue).
colors:
  primary: "#ef4056"
  primary-strong: "#e6123d"
  primary-tonal: "#ffe6eb"
  on-primary: "#ffffff"
  secondary: "#1672dd"
  secondary-deep: "#0d4485"
  canvas: "#ffffff"
  canvas-app: "#f2f2f2"
  canvas-mid: "#fafafa"
  surface-sunken: "#f0f0f1"
  ink: "#0c0c0c"
  ink-body: "#3f4064"
  ink-secondary: "#62666d"
  ink-muted: "#81858b"
  ink-faint: "#a1a3a8"
  hairline: "#e0e0e2"
  hairline-soft: "#f0f0f1"
  success: "#4caf50"
  success-deep: "#2e7b32"
  success-bg: "#e1f9e0"
  error: "#d32f2f"
  error-text: "#b2001a"
  warning: "#f9a825"
  warning-text: "#f57f17"
  rating-low: "#f9bc00"
  rating-mid: "#65aa57"
  rating-high: "#00a049"
  fresh-accent: "#05ba58"
  plus-accent: "#a63489"
  jet-accent: "#a63489"
  digipay-blue: "#0040ff"
  club-cyan: "#0fabc6"
typography:
  font-family-primary: "IRANYekan, sans-serif"
  font-family-var: "var(--font-family)"
  display-hero:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "2.8rem"
    fontWeight: 800
    lineHeight: "1.4"
  display-lg:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "2.2rem"
    fontWeight: 700
    lineHeight: "1.5"
  heading-md:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "1.8rem"
    fontWeight: 700
    lineHeight: "2.1"
  heading-sm:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "1.6rem"
    fontWeight: 700
    lineHeight: "2.1"
  body-lg:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 400
    lineHeight: "2.15"
  body-md:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "1.4rem"
    fontWeight: 400
    lineHeight: "2.15"
  body-sm:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "1.2rem"
    fontWeight: 400
    lineHeight: "2.1"
  caption:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "1.1rem"
    fontWeight: 400
    lineHeight: "1.9"
  price-emphasis:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "1.6rem"
    fontWeight: 800
    lineHeight: "1.5"
  button-label:
    fontFamily: "IRANYekan, sans-serif"
    fontSize: "1.4rem"
    fontWeight: 700
    lineHeight: "1.6"
rounded:
  small: "4px"
  medium: "8px"
  medium-plus: "12px"
  large: "16px"
  pill: "9999px"
  circle: "50%"
spacing:
  xxs: "2px"
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
  xl: "20px"
  xxl: "24px"
  xxxl: "32px"
  xxxxl: "40px"
  hero-y: "48px"
components:
  nav-bar:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    height: "64px desktop / 56px mobile"
    sticky: true
  search-bar:
    backgroundColor: "{colors.surface-sunken}"
    textColor: "{colors.ink}"
    rounded: "{rounded.medium}"
    placeholderColor: "{colors.ink-muted}"
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.medium}"
    typography: "{typography.button-label}"
    padding: "12px 16px"
  button-secondary:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.medium}"
  button-outline:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.primary}"
    borderColor: "{colors.hairline}"
    rounded: "{rounded.medium}"
  card-product:
    backgroundColor: "{colors.canvas}"
    borderColor: "{colors.hairline}"
    rounded: "{rounded.medium}"
    padding: "{spacing.sm}"
    hoverShadow: "0 2px 4px rgba(0,0,0,0.12)"
  category-chip:
    backgroundColor: "{colors.canvas}"
    borderColor: "{colors.hairline}"
    rounded: "{rounded.pill}"
    padding: "8px 16px"
  badge-discount:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.pill}"
    typography: "{typography.caption}"
  badge-fresh:
    backgroundColor: "{colors.fresh-accent}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.small}"
  footer:
    backgroundColor: "{colors.canvas-app}"
    textColor: "{colors.ink-secondary}"
---

## Overview

Digikala is Iran's largest e-commerce marketplace (~40M monthly visits), and its design system is engineered for one job: moving a Persian-speaking shopper from intent to checkout with zero friction. The page is a **dense, utilitarian white canvas** (`{colors.canvas}`) where content — not chrome — carries the visual weight. A single **crimson-red accent** (`{colors.primary}` `#ef4056`) marks every interactive priority: primary CTAs, discount badges, cart icons, active states. There is no decorative color; every hue in the system maps to a business meaning.

The brand's most distinctive decision is its **vertical color-coding**: each business line owns a hue that bleeds into its UI surfaces — Fresh (grocery) gets `#05ba58` green buttons and badges, Plus (membership) gets `#a63489` purple, Digikalajet gets `#ff6200` orange, Digipay uses `#0040ff` blue. A shopper always knows which Digikala product they're inside by color alone.

Typography is **IRANYekan at very generous line-heights** (2.1–2.15 for body text) — nearly double what Latin e-commerce uses. This is not stylistic; Persian script needs the extra vertical air because of descenders, diacritics, and connected letterforms. Font sizes are set in `rem` against an implicit 10px root (so `1.4rem` = 14px), and weights cluster at 400/500/700/800.

Layout follows a **12-column responsive grid** with breakpoints at 320/640/768/1024/1280/1440px (desktop-first at 1024). Cards use `{rounded.medium}` 8px radius, hairline `{colors.hairline}` borders, and shadows are used sparingly — mostly as `0 2px 4px rgba(0,0,0,.12)` hover elevation. Spacing follows a 4px base scale with heavy usage at 16/8/12/24px.

## Colors

### Brand & Accent

- **Crimson Red** (`{colors.primary}` — `#ef4056`): The single dominant accent. Primary CTAs ("افزودن به سبد خرید" / add-to-cart), discount percentage badges, active tab indicators, cart icon fill, logo mark. Reserved exclusively for action + urgency moments.
- **Brand Strong** (`{colors.primary-strong}` — `#e6123d`): Darker red for hover states and the delivery-express indicator.
- **Primary Tonal** (`{colors.primary-tonal}` — `#ffe6eb`): Soft red wash for notification backgrounds and sale banners.
- **Action Blue** (`{colors.secondary}` — `#1672dd`): Secondary CTA color for non-committal actions (login, info links).

### Surface

- **Canvas White** (`{colors.canvas}` — `#ffffff`): Page background. Everything floats on pure white.
- **App Background** (`{colors.canvas-app}` — `#f2f2f2`): Outer frame behind cards, visible on mobile edges.
- **Sunken Surface** (`{colors.surface-sunken}` — `#f0f0f1`): Search bar fill, inactive tabs, skeleton loaders.
- **Hairline** (`{colors.hairline}` — `#e0e0e2`): 1px borders on cards, dividers between list rows, input outlines.

### Text

- **Ink Black** (`{colors.ink}` — `#0c0c0c`): Headlines, prices, product titles.
- **Body Indigo** (`{colors.ink-body}` — `#3f4064`): Long-form paragraphs — slightly blue-tinted dark for reduced glare.
- **Secondary Gray** (`{colors.ink-secondary}` — `#62666d`): Supporting copy, meta information.
- **Muted Gray** (`{colors.ink-muted}` — `#81858b`): Placeholders, disabled states, fine print.

### Semantic

- **Success** (`{colors.success}` — `#4caf50`) with bg (`{colors.success-bg}` — `#e1f9e0`): In-stock indicators, successful order states.
- **Error** (`{colors.error}` — `#d32f2f`): Out-of-stock warnings, form validation failures.
- **Warning** (`{colors.warning}` — `#f9a825`): Low-stock alerts ("تنها ۲ عدد در انبار باقی مانده").
- **Rating Scale** (4 tiers): `{colors.rating-low}` (#f9bc00) for ≤2★ → `{colors.rating-mid}` (#65aa57) for 3-4★ → `{colors.rating-high}` (#00a049) for 4-5★. Rating color IS data.

### Vertical Accents (business-line coding)

| Vertical | Hex | Usage |
|----------|-----|-------|
| Fresh (grocery) | `{colors.fresh-accent}` #05ba58 | Buttons, badges in Fresh section |
| Plus (membership) | `{colors.plus-accent}` #a63489 | Plus-exclusive pricing, member badges |
| Digikalajet | #ff6200 | Express delivery branding |
| Digipay | {colors.digipay-blue} #0040ff | Wallet & payment flows |
| DiDi Club | {colors.club-cyan} #0fabc6 | Loyalty program |

## Typography

### Font Family

Single-face system: **IRANYekan** across all roles (weights 100/300/400/500/700/800/900 loaded via self-hosted woff). No Latin fallback declared beyond generic `sans-serif` — Latin glyphs inside Persian text render via IRANYekan's built-in Latin subset. Icon system uses dedicated `CubeFontIcon` face. Barcode rendering uses "Libre Barcode 128".

### Hierarchy

| Token | Size | Weight | Line Height | Use |
|-------|------|--------|-------------|-----|
| `{typography.display-hero}` | 2.8rem (28px) | 800 | 1.4 | Campaign heroes, mega-sale headlines |
| `{typography.display-lg}` | 2.2rem | 700 | 1.5 | Section titles on landing pages |
| `{typography.heading-md}` | 1.8rem | 700 | 2.1 | Card group headers, modal titles |
| `{typography.heading-sm}` | 1.6rem | 700 | 2.1 | Product titles in lists |
| `{typography.price-emphasis}` | 1.6rem | 800 | 1.5 | Current selling price |
| `{typography.body-lg}` | 1.5rem | 400 | 2.15 | Lead paragraphs, descriptions |
| `{typography.body-md}` | 1.4rem | 400 | 2.15 | Default body text |
| `{typography.body-sm}` | 1.2rem | 400 | 2.1 | Secondary info, specs |
| `{typography.caption}` | 1.1rem | 400 | 1.9 | Meta, timestamps, legal |
| `{typography.button-label}` | 1.4rem | 700 | 1.6 | All button labels |

### Principles

- **Line-height 2.1+ everywhere** — the defining trait. Persian script's connected baseline requires ~2x spacing vs Latin's typical 1.4-1.6.
- **rem-based sizing against 10px root** — `1.4rem` = 14px. Enables user-level zoom scaling.
- **Weight 800 for prices only** — price emphasis is the single heaviest moment on any screen.
- **No italic, no letter-spacing manipulation** — Persian script doesn't support either gracefully.

## RTL & BiDi Rules ✨

- **Document direction:** `<html dir="rtl" lang="fa">`. All layouts mirror natively — flexbox rows run right→left, text-align defaults right.
- **Numerals:** Persian digits (۰۱۲۳۴۵۶۷۸۹) appear in editorial/content contexts; Latin digits (0123) dominate in prices, counts, and phone numbers. Mixed-script lines rely on Unicode BiDi algorithm — never force `direction` inline.
- **Icons:** Directional icons (arrows, chevrons, back buttons) MUST mirror in RTL. Non-directional icons (cart, search, heart) never mirror.
- **Carousels:** Swipe direction inverts; navigation chevrons point left-to-advance (opposite of LTR).
- **Progress/timeline metaphors:** Order-tracking timelines flow right→left.
- **Price formatting:** Currency unit «تومان» follows the number, separated by thin space. Discount percentages render as «٪۲۵» with the percent sign leading.

## Layout

### Spacing System

- Base unit: **4px**. Working tokens: 2/4/6/8/10/12/16/20/24/28/32/36/40/48/56/64/80px.
- Most frequent paddings: 16px (x95 occurrences) > 8px ≈ 4px > 12px > 24px.
- Section rhythm: 24px between sibling cards, 32-40px between section bands.

### Grid & Container

- Desktop container: max-width **1280px**, centered, 16px side gutters.
- Product grids: 6-up at ≥1280px, 4-up at 1024px, 3-up tablet, 2-up mobile.
- Breakpoint hierarchy: **1024px dominates** (258 media queries) as the desktop/mobile fork; secondary at 1280/1440 for wide screens, 640/768 for tablets.

### Responsive Strategy

| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | < 768px | Single column, bottom-nav appears, hero carousels full-bleed |
| Tablet | 768-1023px | 3-up grids, condensed sidebar filters |
| Desktop | ≥ 1024px | Full header nav, 4-6-up grids, persistent filter rail |

Touch targets: minimum 44px tap height on all interactive elements.

## Elevation & Depth

| Level | Treatment | Use |
|-------|-----------|-----|
| Level 0 — Flat | White surface, no shadow | Default cards inside bordered containers |
| Level 1 — Hairline | 1px solid `{colors.hairline}`, no shadow | Product cards, list rows, inputs |
| Level 2 — Soft Lift | `0 2px 4px rgba(0,0,0,.12)` | Hover state on cards, dropdown menus |
| Level 3 — Modal Stack | `0 5px 40px rgba(0,0,0,.16)` | Modals, drawer sheets, sticky headers on scroll |

Depth philosophy: **flat-first**. Shadow appears only to signal interactivity or overlay hierarchy — never as decoration. Skeleton loaders use pulsing `{colors.surface-sunken}` fills instead of spinners.

## Shapes

| Token | Value | Use |
|-------|-------|-----|
| `{rounded.small}` | 4px | Tiny chips, inline tags |
| `{rounded.medium}` | 8px | Cards, buttons, inputs — the workhorse radius |
| `{rounded.medium-plus}` | 12px | Larger media cards, modals |
| `{rounded.large}` | 16px | Hero banners, featured surfaces |
| `{rounded.pill}` | 9999px | Category chips, discount badges, toggle pills |
| `{rounded.circle}` | 50% | Avatars, icon buttons |

## Components

### Buttons

**`button-primary`** — the crimson CTA. Background `{colors.primary}`, white label in `{typography.button-label}`, `{rounded.medium}`, padding 12×16px. Hover darkens toward `{colors.primary-strong}`.

**`button-secondary`** — blue informational action. Background `{colors.secondary}`, white label. Used for "مشاهده" (view), login prompts.

**`button-outline`** — ghost variant. White bg, `{colors.hairline}` border, `{colors.primary}` label. Used in card footers for low-commitment actions.

### Cards & Containers

**`card-product`** — the atomic product tile. White bg, hairline border, `{rounded.medium}`, product image top (square, object-fit cover), title in `{typography.heading-sm}` clamped to 2 lines, rating row (colored star + count), price block with strikethrough original + `{typography.price-emphasis}` current + discount pill. Hover raises to Level 2 shadow.

**`category-chip`** — horizontal-scrollable pill. White bg, hairline border, icon + label, `{rounded.pill}`.

**`badge-discount`** — red pill showing «٪۲۵» in white caption type. Anchored top-left of product images.

### Inputs & Forms

**`search-bar`** — the hero interaction of the header. Sunken `{colors.surface-sunken}` fill, `{rounded.medium}`, magnifier icon right-aligned (RTL), placeholder in `{colors.ink-muted}`. Expands to full-width overlay on focus with recent-searches panel.

### Navigation

**`nav-bar`** — sticky white bar, 64px tall desktop. Right: logo. Center: search (expands to dominate). Left: login/cart/categories. Mobile collapses to bottom tab bar (خانه، دسته‌بندی، سبد، دیجی‌کلاب، پروفایل).

**`footer`** — multi-column link directory on `{colors.canvas-app}` background, trust badges row, app-download QR codes.

### Signature Components

**`price-block`** — the money moment. Original price struck through in `{colors.ink-muted}` caption, current price in `{typography.price-emphasis}`, currency «تومان» trailing in caption size, discount pill adjacent.

**`order-timeline`** — RTL status tracker: right=placed, left=delivered, filled circles in `{colors.success}` for completed steps.

**`skeleton-loader`** — gray shimmer blocks matching final content shape (image square + two text lines).

## Agent Prompt Guide

Quick reference for AI agents building Digikala-style UI:

```
Colors:   bg #fff · frame #f2f2f2 · text #0c0c0c/#62666d · accent #ef4056 ·
          links #1672dd · success #4caf50 · border #e0e0e2
Font:     IRANYekan (fallback: Vazirmatn) · body 14px/2.15 · headings 700-800
Radius:   cards/buttons 8px · chips/badges pill · media 12-16px
Spacing:  4px base · card gap 16-24px · sections 32-40px
RTL:      dir="rtl" lang="fa" · mirror directional icons · Persian numerals in prose
Shadow:   flat default · hover 0 2px 4px rgba(0,0,0,.12) · modal 0 5px 40px
```

**Sample prompt:**
> "Build a product listing page following DESIGN.md: white canvas, 4-column grid of product cards with hairline borders and 8px radius, red (#ef4056) discount pills, IRANYekan typography at 2.15 line-height, sticky white header with sunken search bar, RTL layout with Persian digits."

## Do's and Don'ts

### Do

- Keep the canvas pure white; let `{colors.primary}` red be the only loud voice on the screen.
- Use IRANYekan at line-height ≥2.1 for all Persian body text — cramped Persian text reads broken.
- Color-code verticals consistently: Fresh=green, Plus=purple, Jet=orange. Never mix these accents outside their business context.
- Render prices as the visual anchor: weight 800, larger than surrounding text, with struck-through original when discounted.
- Use skeleton loaders shaped like final content instead of spinners.
- Mirror ALL directional icons in RTL; keep symbolic icons (cart, heart, search) unmirrored.
- Respect the 44px minimum touch target on mobile.

### Don't

- Don't introduce gradients or glassmorphism — Digikala's surfaces are flat and functional.
- Don't use the red `#ef4056` as body text or large decorative fills; it signals action/discount only.
- Don't set Persian body text below 14px or line-height below 2.0 — legibility collapses.
- Don't mix numeral systems inside a single sentence (pick Persian OR Latin per context).
- Don't apply heavy shadows (>Level 3) to nested elements; depth is reserved for true overlays.
- Don't translate the brand voice into formal Arabic-style phrasing — Digikala writes conversational Tehrani Persian («سبد خرید», not «عربة التسوق»).
- Don't left-align Persian text or use LTR progress flows.
