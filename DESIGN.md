---
# ============================================================
# DESIGN TOKENS — Studio 23 TTL
# Premium photography studio. Dark, editorial, cinematic.
# ============================================================

colors:
  background: "#0A0A0A"
  surface: "#141414"
  surface-raised: "#1E1E1E"
  border: "#2A2A2A"
  border-subtle: "#1A1A1A"

  text-primary: "#F5F5F5"
  text-secondary: "#A0A0A0"
  text-muted: "#5A5A5A"
  text-inverse: "#0A0A0A"

  primary: "#C8A96E"
  primary-hover: "#B8955A"
  secondary: "#E8E8E8"
  tertiary: "#3A3A3A"

  success: "#4CAF50"
  warning: "#FF9800"
  error: "#F44336"
  info: "#2196F3"

typography:
  fontFamily:
    heading: "Playfair Display, Georgia, serif"
    body: "Inter, system-ui, sans-serif"
    mono: "JetBrains Mono, monospace"

  display:
    fontSize: "72px"
    fontWeight: "700"
    lineHeight: "1.1"
    letterSpacing: "-0.02em"
    fontFamily: "{typography.fontFamily.heading}"

  h1:
    fontSize: "56px"
    fontWeight: "700"
    lineHeight: "1.15"
    letterSpacing: "-0.02em"
    fontFamily: "{typography.fontFamily.heading}"

  h2:
    fontSize: "40px"
    fontWeight: "600"
    lineHeight: "1.2"
    letterSpacing: "-0.01em"

  h3:
    fontSize: "28px"
    fontWeight: "600"
    lineHeight: "1.3"

  h4:
    fontSize: "20px"
    fontWeight: "600"
    lineHeight: "1.4"

  body-lg:
    fontSize: "18px"
    fontWeight: "400"
    lineHeight: "1.7"

  body-md:
    fontSize: "16px"
    fontWeight: "400"
    lineHeight: "1.6"

  body-sm:
    fontSize: "14px"
    fontWeight: "400"
    lineHeight: "1.5"

  label:
    fontSize: "13px"
    fontWeight: "600"
    letterSpacing: "0.1em"
    textTransform: "uppercase"

  caption:
    fontSize: "12px"
    fontWeight: "400"
    lineHeight: "1.5"

  mono:
    fontSize: "14px"
    fontFamily: "{typography.fontFamily.mono}"

spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
  2xl: "48px"
  3xl: "64px"
  4xl: "96px"

rounded:
  none: "0px"
  sm: "4px"
  md: "6px"
  lg: "12px"
  xl: "20px"
  full: "9999px"

elevation:
  0: "none"
  1: "0 1px 3px rgba(0,0,0,0.5), 0 1px 2px rgba(0,0,0,0.4)"
  2: "0 4px 16px rgba(0,0,0,0.6)"
  3: "0 12px 40px rgba(0,0,0,0.8)"

components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.text-inverse}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "14px 32px"
    height: "48px"

  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    border: "1px solid {colors.primary}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    height: "48px"

  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.text-secondary}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"

  card:
    backgroundColor: "{colors.surface}"
    border: "1px solid {colors.border}"
    rounded: "{rounded.none}"
    padding: "{spacing.xl}"
    elevation: "{elevation.1}"

  input:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text-primary}"
    border: "1px solid {colors.border}"
    rounded: "{rounded.none}"
    height: "48px"
    padding: "12px {spacing.md}"

  badge:
    backgroundColor: "{colors.surface-raised}"
    textColor: "{colors.primary}"
    typography: "{typography.caption}"
    rounded: "{rounded.full}"
    padding: "4px 12px"

  nav:
    backgroundColor: "transparent"
    height: "80px"
    border: "none"
---

## Overview

Studio 23 TTL is a premium photography and videography studio based in Houston, TX. The UI should feel like entering a high-end gallery — dark, cinematic, editorial. Every frame deliberate. Every pixel earning its place.

**Personality:** cinematic, premium, editorial, disciplined, high-contrast
**Mode:** Dark-first
**Audience:** Premium clients, nightclub operators, businesses seeking professional photography

## Colors

The palette is built around near-black backgrounds with warm gold accents — evoking the feeling of a photography darkroom coming to life. The gold (`#C8A96E`) signals quality and exclusivity without screaming luxury.

- **Background `#0A0A0A`** — near-black canvas, lets photography breathe
- **Surface `#141414`** — cards and panels, subtly lifted from background
- **Primary `#C8A96E`** — warm gold for CTAs, highlights, and accents
- **Text hierarchy** — three tiers: bright white for headings, mid-gray for body, dark gray for muted/metadata

## Typography

Playfair Display for headings brings editorial weight and a print-magazine feel. Inter handles body text with clean legibility. The contrast between serif headings and sans body is intentional — it creates visual rhythm without feeling chaotic.

- **Display/H1**: 72–56px, weight 700 — hero statements and page titles
- **H2/H3**: 40–28px — section headers
- **Body**: 16–18px Inter — clean, readable prose
- **Label**: 13px uppercase, tracked — used for nav links, buttons, category tags

## Layout

Based on an 8px grid with generous breathing room.

- **Max content width:** 1280px
- **Page margins:** 64px on desktop, 24px on mobile
- **Section spacing:** `{spacing.4xl}` (96px) between major sections
- **Column grid:** 12-column

Photography-forward layouts — let images dominate. Text supports the visual, not the other way around.

## Elevation & Depth

Minimal shadow use. Depth is created through contrast and layering, not heavy shadows. Cards sit slightly above the background via color difference. Hover states use subtle gold borders rather than shadows.

## Shapes

Sharp edges throughout. No pill buttons. No heavy rounding.

- **Buttons:** Square (`{rounded.none}`) — deliberate, confident
- **Cards:** Square (`{rounded.none}`) — gallery-wall feel
- **Inputs:** Square (`{rounded.none}`)
- **Badges:** Pill (`{rounded.full}`) — only exception, for category tags

## Components

**Buttons:**
- Primary: gold fill, black text, uppercase label font — one per section max
- Secondary: transparent with gold border — supporting actions
- Ghost: for nav links and text-level actions

**Cards:**
- Square edges, dark surface, subtle border
- Hover: border upgrades to gold (`{colors.primary}`)
- Photography cards: image-first, minimal text below

**Navigation:**
- Transparent on load, transitions to dark semi-transparent on scroll
- Backdrop blur on scroll
- Logo left, links right, CTA button far right

## Do's and Don'ts

### ✅ Do
- Let photography dominate — give images full-bleed treatment whenever possible
- Use gold sparingly — it's the accent, not the base
- Use Playfair Display for every headline — it's the brand voice
- Keep whitespace generous — premium brands don't crowd
- Use uppercase labels for all navigation, buttons, and category tags

### ❌ Don't
- Don't use rounded buttons — sharp edges are the brand signature
- Don't put text over busy photographs without a dark overlay
- Don't use more than one primary CTA per section
- Don't use bright colors outside the palette
- Don't use body font for headlines — Playfair is non-negotiable
- Don't use colors outside the defined palette
- Don't mix font families beyond heading/body/mono
- Don't override component border-radius — shape language is intentional
