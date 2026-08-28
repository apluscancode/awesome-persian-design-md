---
version: alpha
name: CafeBazaar-Inspired-design-analysis
description: >
  An inspired interpretation of Cafe Bazaar's design language — Iran's primary
  Android app store whose surface is a clean white canvas ruled by a single
  emerald-green brand accent (#0ea960), YekanBakh typography at comfortable
  line-heights (1.9–2.15), and a component library built on Bootstrap-like
  utilities with 8px-radius cards and subtle shadows. The system reads as
  pragmatic, developer-friendly, and strictly RTL.
colors:
  primary: "#0ea960"
  primary-dark: "#1e7e34"
  primary-light: "#e5e7f0"
  primary-tonal: "#e5e7f0"
  success: "#28a745"
  success-bg: "#e5e7f0"
  danger: "#dc3545"
  danger-bg: "#fff0f0"
  warning: "#ffc107"
  warning-bg: "#fff3ed"
  info: "#17a2b8"
  info-bg: "#ebf6ff"
  canvas: "#ffffff"
  canvas-app: "#f9fafd"
  surface-sunken: "#e5e7f0"
  ink-strongest: "#212529"
  ink-strong: "#2a2a2a"
  ink-body: "#2a2a2a"
  ink-body-md: "#495057"
  ink-secondary: "#4e4e4e"
  ink-muted: "#6c757d"
  ink-faint: "#8f8f8f"
  hairline: "#dee2e6"
  hairline-soft: "#eaedf8"
  white: "#ffffff"
typography:
  font-family-primary: "YekanBakh, sans-serif"
  font-family-icon: "cafebazaar-icon, Material Icons"
  display-hero:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "3rem"
    fontWeight: 800
    lineHeight: "1.4"
  display-lg:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "2.125rem"
    fontWeight: 700
    lineHeight: "1.4"
  heading-lg:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "2.125rem"
    fontWeight: 700
    lineHeight: "1.4"
  heading-md:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 700
    lineHeight: "1.5"
  heading-sm:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 700
    lineHeight: "1.5"
  body-lg:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 400
    lineHeight: "2.15"
  body-md:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "1.4rem"
    fontWeight: 400
    lineHeight: "2.15"
  body-md-2:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 400
    lineHeight: "2.1"
  body-sm:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: "2.1"
  body-xs:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: "2.1"
  caption:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: "2.1"
  button-label:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "1rem"
    fontWeight: 700
    lineHeight: "1.6"
  button-sm:
    fontFamily: "YekanBakh, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 600
    lineHeight: "1.5"
rounded:
  sm: "4px"
  md: "8px"
  lg: "12px"
  xl: "16px"
  xxl: "22px"
  pill: "9999px"
  circle: "50%"
spacing:
  xxs: "2px"
  xs: "4px"
  sm: "4px"
  md: "8px"
  lg: "16px"
  xl: "20px"
  xxl: "24px"
  xxxl: "32px"
  section: "48px"
  hero-y: "48px"
components:
  nav-bar:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink-strongest}"
    height: "64px desktop / 56px mobile"
    sticky: true
  search-bar:
    backgroundColor: "{colors.surface-sunken}"
    textColor: "{colors.ink-body}"
    placeholderColor: "{colors.ink-muted}"
    rounded: "{rounded.sm}"
    padding: "12px 16px"
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "#fff"
    rounded: "{rounded.md}"
    typography: "{typography.button-label}"
    padding: "12px 24px"
  button-secondary:
    backgroundColor: "{colors.secondary}"
    textColor: "#fff"
    rounded: "{rounded.md}"
    padding: "12px 24px"
  button-outline:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.primary}"
    borderColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
  button-danger:
    backgroundColor: "{colors.danger}"
    textColor: "#fff"
    rounded: "{rounded.md}"
    padding: "12px 24px"
  card-app:
    backgroundColor: "{colors.canvas}"
    borderColor: "{colors.hairline}"
    rounded: "{rounded.md}"
    padding: "{spacing.sm}"
    hoverShadow: "0 4px 24px #0000001a"
  card-developer:
    backgroundColor: "{colors.canvas}"
    borderColor: "{colors.hairline}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  category-chip:
    backgroundColor: "{colors.surface-sunken}"
    textColor: "{colors.ink-body}"
    rounded: "{rounded.sm}"
    padding: "8px 16px"
  badge-rating:
    backgroundColor: "{colors.warning-bg}"
    textColor: "{colors.warning}"
    rounded: "{rounded.xs}"
    padding: "2px 8px"
  footer:
    backgroundColor: "{colors.surface-sunken}"
    textColor: "{colors.ink-secondary}"
---

## Overview

Cafe Bazaar (کافه‌بازار) is Iran's leading Android app marketplace (~40M+ users) — the de facto Play Store alternative in a Google-less market. Its design system reflects a **pragmatic, developer-first mindset**: clean white canvas, single emerald accent (`#0ea960`), YekanBakh typography at generous line-heights, and a component vocabulary that feels familiar to anyone who's used Bootstrap or Material Design — but with strict RTL discipline.

The brand's visual identity is **monochrome + one accent**: a clean white canvas (`#fff`), slate-scale ink (`#212529` → `#6c757d`), and exactly **one** brand green (`#0ea960` / `#0ea960` → `#1e7e34` for hover). No gradients, no secondary accent hues. This restraint makes the green *mean something* — every primary CTA ("نصب", "دانلود", "خرید") wears the same green, creating a muscle-memory association: **green = action = install/purchase**.

The system is built on **Bootstrap 5-style utility tokens** (spacing, radius, color, shadow) with a thin custom layer (`YekanBakh` font, `cafebazaar-icon` icon font). It feels like a Bootstrap theme customized for Persian/RTL — pragmatic, familiar, zero learning curve for developers.

Typography is **YekanBakh** (4 weights: 300/400/500/700) — the modern successor to IRANSans with better Latin subset and variable-font potential. Body text sits at `1rem` (16px) with **line-height 2.15** — the Persian legibility standard. Headings use 700/800 weights at generous sizes (2.125rem–3rem).

Layout follows a **12-column responsive grid** (Bootstrap-style) with breakpoints at 640/1024/1200/1440px. Container max-width ~1200px. Spacing scale is 4px-based but heavily favors 8px/16px/24px/32px — Bootstrap's 0.5rem/1rem/1.5rem rhythm.

Shadows are subtle and layered: Level 1 `0 4px 24px rgba(0,0,0,.1)` for cards, Level 2 `0 2px 12px rgba(0,0,0,.1)` for dropdowns, Level 3 `0 1rem 3rem` for modals. No heavy shadows — flat-first.

## Colors

### Brand
- **Primary Green** (`#0ea960`): The sole accent. Primary CTAs ("نصب", "دانلود", "خرید"), active nav states, rating stars (filled), download progress, success toasts. Hover → `#1e7e34`.
- **Primary Dark** (`#1e7e34`): Hover/active states on primary buttons.
- **Primary Light / Tonal** (`#e5e7f0`): Success toast backgrounds, subtle badges, hover washes on cards.

### Neutrals
| Token | Hex | Role |
|-------|-----|------|
| Canvas | `#ffffff` | Page background |
| Surface Sunken | `#e5e7f0` | Search bar, inactive tabs, code blocks |
| Ink Strongest | `#212529` | H1, prices, primary labels |
| Body | `#2a2a2a` / `#495057` | Body text (2 tiers) |
| Secondary | `#4e4e4e` / `#6c757d` | Meta, timestamps, secondary text |
| Muted | `#6c757d` / `#8f8f8f` | Placeholders, disabled, captions |
| Hairline | `#dee2e6` | Borders, dividers, input outlines |
| Hairline Soft | `#eaedf8` | Subtle dividers in dense lists |

### Semantic
- **Success** (`#28a745`): "نصب شده", "موجود", success toasts
- **Danger** (`#dc3545`): "حذف", "خطا", form errors
- **Warning** (`#ffc107`): Low stock, pending review
- **Info** (`#17a2b8`): Tips, system notices

### Dark Mode (not implemented in marketing site)
- Not present in current marketing CSS. App/WebView may have separate dark theme.

## Typography

### Font Stack
- **Primary:** `YekanBakh, sans-serif` (weights 100/300/400/700 via self-hosted woff2)
- **Icons:** `Material Icons`, `cafebazaar-icon` (custom icon font)
- **Mono:** `Consolas, Liberation Mono, monospace`

### Hierarchy
| Token | Size | Weight | Line Height | Use |
|-------|------|--------|-------------|-----|
| `{typography.display-hero}` | 3rem (48px) | 800 | 1.4 | Hero H1 |
| `{typography.display-lg}` | 2.125rem (34px) | 700 | 1.4 | Section titles |
| `{typography.heading-lg}` | 2.125rem | 700 | 1.4 | Section titles |
| `{typography.heading-md}` | 1.5rem (24px) | 700 | 1.5 | Card group headers |
| `{typography.heading-sm}` | 1.25rem (20px) | 700 | 1.5 | Card titles, modal headers |
| `{typography.body-lg}` | 1.5rem | 400 | 2.15 | Lead paragraphs |
| `{typography.body-md}` | 1.4rem (22px) | 400 | 2.15 | Default body |
| `{typography.body-sm}` | 1.125rem (18px) | 400 | 2.1 | Secondary text |
| `{typography.body-xs}` | 0.875rem (14px) | 400 | 2.1 | Meta, timestamps |
| `{typography.caption}` | 0.875rem | 400 | 2.1 | Fine print, legal |
| `{typography.button-label}` | 1rem | 700 | 1.6 | Buttons, CTAs |

### Principles
- **Line-height 2.15 for body** — Persian legibility standard (descenders + diacritics).
- **rem-based against 16px root** — `1rem` = 16px, `1.4rem` = 22.4px.
- **Weight ceiling 800** (hero only), 700 for headings, 400/500 for body.
- **No letter-spacing adjustments** — Persian doesn't need it.

## RTL & BiDi Rules ✨

- `<html lang="fa" dir="rtl">` enforced server-side.
- Flex/Grid layouts mirror natively (flex-row runs right→left).
- Search bar: magnifier icon **right** (RTL start), placeholder right-aligned.
- Price format: «۱۲۵٬۰۰۰ تومان» — native Persian digits (YekanBakh FaNum feature), thousands separator «٬».
- Directional icons mirror: chevron-left = forward, chevron-right = back.
- Carousel swipe: left = next (RTL), right = prev.
- Carousels/sliders: `dir="rtl"` on container + `flex-direction: row-reverse` where needed.
- Numbers in prices/counters: native Persian digits via YekanBakh FaNum (no JS conversion).
- Phone numbers stay LTR (`dir="ltr"` span).

## Layout

### Spacing Scale
- Base unit: **4px** → tokens: 4/8/12/16/20/24/32/40/48px.
- Most frequent: 8px (×9), 16px, 4px, 24px, 32px.
- Section rhythm: 48px between bands, 24px between cards.

### Grid & Container
- **Container max-width:** 1200px (Bootstrap `container-xl`).
- Side gutters: 16px mobile, 24px desktop.
- Breakpoints: 640 / 768 / 1024 / 1200 / 1440px.
- Product grid: 4-col ≥1200px, 3-col 992–1199px, 2-col 768–991px, 1-col <640px.

### Responsive Strategy
| Breakpoint | Width | Behavior |
|----------|-------|----------|
| Mobile | < 640px | Single col, hamburger nav, sticky search |
| Tablet | 768–1023px | 2–3 col grids, condensed header |
| Desktop | ≥ 1024px | Full header, 4-col grids, sidebar filters |

## Elevation & Depth

| Level | Treatment | Use |
|-------|-----------|-----|
| Level 0 — Flat | None | Default cards, lists |
| Level 1 — Card Hover | `0 4px 24px rgba(0,0,0,.1)` | App cards, feature cards on hover |
| Level 2 — Dropdown/Tooltip | `0 2px 12px rgba(0,0,0,.1)` | Dropdowns, tooltips, popovers |
| Level 3 — Modal/Modal Sheet | `0 1rem 3rem rgba(0,0,0,.18)` | Modals, bottom sheets, drawers |
| Focus Ring | `0 0 0 .2rem rgba(40,167,69,.25)` | Focus-visible on buttons/inputs |

**Flat-first philosophy** — shadows only for interactivity signals.

## Shapes

| Token | Value | Use |
|-------|-------|-----|
| `{rounded.sm}` | 4px | Inputs, buttons, badges, chips |
| `{rounded.md}` | 8px | **Cards, buttons, inputs, thumbnails** — workhorse |
| `{rounded.lg}` | 12px | Modals, large media containers |
| `{rounded.xl}` | 16px | Hero panels, hero images |
| `{rounded.pill}` | 9999px | Search bar, tags, badges, toggle switches |
| `{rounded.circle}` | 50% | Avatars, icon buttons |

## Components

### Buttons
| Variant | Style | Use |
|---------|-------|-----|
| **Primary** | Bg `#0ea960`, white label, 8px radius, 12px×24px padding | Primary CTAs: "نصب", "دانلود", "خرید" |
| **Secondary** | Bg `#6c757d`, white label | "مشاهده همه", "ادامه مطلب" |
| **Outline** | White bg, `#0ea960` border/text | Secondary actions in cards |
| **Danger** | Bg `#dc3545`, white | "حذف", "خروج از اکانت" |
| **Ghost** | Transparent bg, ink text | Tertiary, low-commitment |

All buttons: **8px radius**, `{typography.button-label}` (1rem, 700), pill-shape *not* used — 8px is the brand.

### Cards & Containers
**`card-app`** — the atomic app tile. White bg, 1px `#dee2e6` border, 8px radius, thumbnail top, title (clamped 2 lines), developer name (muted), rating stars (gold `#ffc107`), price/install button. Hover → Level 1 shadow.

**`card-developer`** — developer dashboard card. White, hairline border, metadata grid.

**`category-chip`** — sunken `#e5e7f0` bg, 4px radius, icon + label, horizontal scroll rail.

### Search & Inputs
**`search-bar`** — sunken `#e5e7f0` fill, 4px radius, magnifier right (RTL), expands to overlay with suggestions on focus.

**`text-input`** — White bg, `#dee2e6` border, 4px radius, focus ring `#28a74540`.

### Navigation
**`nav-bar`** — White sticky, 64px height, logo left (RTL start), search center (expands on focus), user menu right.

**Mobile:** Hamburger → drawer, or bottom tab bar (Home, Categories, Updates, Profile).

### Signature Components

**`price-display`** — Current price in `{typography.body-lg}` 700 weight, original struck in muted, currency «تومان» trailing.

**`rating-stars`** — Gold `#ffc107` filled stars, count in muted caption.

**`install-button`** — The money button. Full-width on mobile, pill-height (44px+), green `#0ea960`, white label "نصب" / "دانلود".

**`skeleton-loader`** — Pulsing `#e5e7f2` → `#fafafa` blocks matching final layout.

**`toast`** — Success green (`#28a745` bg), error red, info blue. Bottom-right, auto-dismiss 4s.

## Agent Prompt Guide

```
Colors:  bg #fff · sunken #e5e7f0 · text #212529/#495057 · accent #0ea960
         border #dee2e6 · success #28a745 · danger #dc3545
Font:    YekanBakh (fallback: Vazirmatn) · body 1rem/2.15 · headings 700/800
Radius:  cards/buttons 8px · inputs 4px · badges pill
Spacing: 8/16/24/32/48px rhythm · 1200px container
RTL:     dir=rtl lang=fa · mirror icons · Persian numerals in prose
Shadow:  card hover 0 4px 24px rgba(0,0,0,.1) · modal 0 1rem 3rem
```

**Sample prompt:**
> "Build an app listing page following Cafe Bazaar DESIGN.md: white canvas, 4-column grid of app cards with hairline borders and 8px radius, green (#0ea960) install buttons, YekanBakh 1rem/2.15 body, sticky white header with sunken search, RTL with Persian digits."

## Do's and Don'ts

### Do
- Keep canvas white; let the single green accent do the work.
- Use YekanBakh at line-height ≥2.0 for Persian body text.
- 8px radius everywhere (cards, buttons, inputs) — consistency = trust.
- Green buttons = primary actions only ("نصب", "دانلود", "خرید").
- Use skeleton loaders shaped like content (not spinners).
- Mirror ALL directional icons in RTL; keep symbolic icons (search, menu) unmirrored.
- 44px minimum tap targets on mobile.

### Don't
- Don't introduce a second accent hue (no blue CTAs, no orange badges).
- Don't use `border-radius: 4px` on cards — 8px is the brand.
- Don't set Persian body line-height below 2.0 — legibility breaks.
- Don't mix Latin digits into Persian prose (use YekanBakh FaNum).
- Don't use heavy shadows on cards — flat + hairline is the aesthetic.
- Don't use `border-radius: 50%` on buttons — 8px only.
- Don't left-align Persian text in RTL layouts.

---

## Appendix: Token Reference (CSS Variables)

```css
:root {
  --primary: #0ea960;
  --primary-dark: #1e7e34;
  --primary-tonal: #e5e7f0;
  --success: #28a745;
  --danger: #dc3545;
  --warning: #ffc107;
  --info: #17a2b8;
  --canvas: #fff;
  --surface-sunken: #e5e7f0;
  --ink-strongest: #212529;
  --ink-body: #2a2a2a;
  --ink-secondary: #4e4e4e;
  --ink-muted: #6c757d;
  --hairline: #dee2e6;
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --spacing-xs: 4px;
  --spacing-md: 8px;
  --spacing-lg: 16px;
  --spacing-xl: 24px;
  --spacing-section: 48px;
}
```

---

*تحلیل بر اساس CSS تولیدی سایت cafebazaar.ir (Next.js, Bootstrap-like utilities, YekanBakh font) — استخراج شده اوت ۲۰۲۶.*