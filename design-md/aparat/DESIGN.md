---
version: alpha
name: Aparat
description: Iranian video platform with dark theme and minimal design.
colors:
  primary: "#16171a"
  secondary: "#000000"
  neutral: "#ffffff"
typography:
  body-md:
    fontFamily: "Tahoma, Arial, sans-serif"
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.5
rounded:
  sm: 4px
  md: 8px
spacing:
  sm: 8px
  md: 16px
  lg: 24px
components:
  header:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.neutral}"
---

## Overview

Aparat is Iran's leading video sharing platform with a dark-themed interface optimized for video content consumption.

## Colors

- **Primary (#16171a):** Dark background color used throughout the interface
- **Neutral (#ffffff):** Text color on dark backgrounds

## Layout

Mobile-first responsive design with breakpoint at 740px for header styling.

## Components

`header` uses dark background (#16171a) with subtle border for separation.