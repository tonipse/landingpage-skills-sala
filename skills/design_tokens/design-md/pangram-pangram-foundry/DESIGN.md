---
version: alpha
source: refero
source_id: 6d64a4da-ef40-453e-86f7-4bfabc0c9051
source_url: https://pangrampangram.com
name: Pangram Pangram Foundry
description: "Pangram Pangram champions a stark, high-contrast aesthetic with functional color accents. The UI features a bright, almost white canvas, broken by dark header sections and image-heavy content blocks. Typography is the primary visual element, bold and expansive, with interactions generally expressed through subtle changes in neutral buttons or vivid, distinct status badges. Surfaces are largely flat with soft, large corner radii, avoiding heavy shadows."
theme: light
northStar: "Type foundry's bold canvas: white pages, dark headers, expressive typography, and soft, rounded containers."

colors:
  ink: "#000000"  # neutral — Primary text, headers, icon strokes, borders, and some button fills. This is the dominant 
  canvas: "#fafafa"  # neutral — Page backgrounds, card surfaces, and some light text
  paper: "#ededed"  # neutral — Secondary surface backgrounds, used for cards and some buttons, providing a subtle visual 
  slate: "#666666"  # neutral — Muted text, secondary link color, and card text details
  alert-red: "#ff2f00"  # brand — Orange action color for filled buttons, selected navigation states, and focused conversion
  update-yellow: "#ffb700"  # accent — Yellow state accent for badges, validation surfaces, and short status labels.
  early-access-blue: "#bfe0ff"  # accent — Blue state accent for badges, validation surfaces, and short status labels.

typography:
  neue-montreal:
    family: "Neue Montreal"
    sizes: "12px, 14px, 16px, 18px, 20px, 22px, 24px, 36px, 48px, 121px, 145px"
    weight: "400, 530, 600"
    lineHeight: "1.00, 1.10, 1.17, 1.20, 1.30"
    substitute: "Inter"
    use: "The primary typeface for headings, body text, navigation, and interface elements. Its wide range of weights and sizes forms the core expressive character of the brand. Default letter spacing is normal"
  neue-montreal-semibold:
    family: "neue-montreal-semibold"
    sizes: "103px, 121px"
    weight: "600"
    lineHeight: "1.00"
    substitute: "Inter"
    use: "A specific variant of Neue Montreal used for large, impactful display headings."
  neue-york-normal-bold:
    family: "neue-york-normal-bold"
    sizes: "103px"
    weight: "700"
    lineHeight: "1.00"
    substitute: "Inter"
    use: "A bold variant for display headings, adding weight and presence to feature titles."
  neue-york-normal-normal-bold:
    family: "neue-york-normal-normal-bold"
    sizes: "121px"
    weight: "400"
    lineHeight: "1.00"
    substitute: "Inter"
    use: "A normal weight variant for very large headings, providing a softer impact than its bold counterpart."
  frama-semibold:
    family: "frama-semibold"
    sizes: "103px"
    weight: "580"
    lineHeight: "1.00"
    substitute: "Figtree"
    use: "A unique semibold display font used for specific font showcase headings, reflecting individual font identities."
  kyoto-semibold:
    family: "kyoto-semibold"
    sizes: "103px"
    weight: "600"
    lineHeight: "1.00"
    substitute: "DM Sans"
    use: "Another distinctive semibold display font chosen for font showcase headings, adding character diversity."
  neue-gstaad-normal-bold:
    family: "neue-gstaad-normal-bold"
    sizes: "103px"
    weight: "700"
    lineHeight: "1.00"
    substitute: "Poppins"
    use: "A bold display font for font showcase headings, conveying strength and impact."
  palma-fizzy-heavy:
    family: "palma-fizzy-heavy"
    sizes: "103px"
    weight: "800"
    lineHeight: "1.00"
    substitute: "Montserrat"
    use: "An extra-bold display font for font showcase headings, used for maximum visual punch."
  mori-bold:
    family: "mori-bold"
    sizes: "103px"
    weight: "700"
    lineHeight: "1.00"
    substitute: "Roboto"
    use: "A bold display font for font showcase headings, sharp and clear."
  museum-light:
    family: "museum-light"
    sizes: "103px"
    weight: "300"
    lineHeight: "1.00"
    substitute: "Open Sans Light"
    use: "A light display font for specific font showcase headings, offering a delicate and refined touch."
  neue-corp-normal-semibold:
    family: "neue-corp-normal-semibold"
    sizes: "103px"
    weight: "500"
    lineHeight: "1.00"
    substitute: "Titillium Web"
    use: "A medium-semibold display font for font showcase headings, balancing authority with approachability."
  watch-medium:
    family: "watch-medium"
    sizes: "103px"
    weight: "485"
    lineHeight: "1.00"
    substitute: "Lexend"
    use: "A unique medium weight display font for font showcase headings, providing a distinct stylistic flair."
  monument-narrow-medium:
    family: "monument-narrow-medium"
    sizes: "103px"
    weight: "525"
    lineHeight: "1.00"
    substitute: "IBM Plex Sans Condensed"
    use: "A medium weight, narrow display font for font showcase headings, maintaining legibility while conserving horizontal space."
  model-plastic-regular:
    family: "model-plastic-regular"
    sizes: "103px"
    weight: "500"
    lineHeight: "1.00"
    substitute: "Inter"
    use: "A regular weight display font for font showcase headings, offering a clean, contemporary appearance."
---

# Pangram Pangram Foundry — Design System

> Type foundry's bold canvas: white pages, dark headers, expressive typography, and soft, rounded containers.


Pangram Pangram champions a stark, high-contrast aesthetic with functional color accents. The UI features a bright, almost white canvas, broken by dark header sections and image-heavy content blocks. Typography is the primary visual element, bold and expansive, with interactions generally expressed through subtle changes in neutral buttons or vivid, distinct status badges. Surfaces are largely flat with soft, large corner radii, avoiding heavy shadows.


## Type Scale

- role: caption · size: 12 · lineHeight: 1.2
- role: body-sm · size: 14 · lineHeight: 1.2
- role: body · size: 16 · lineHeight: 1.2
- role: subheading-sm · size: 18 · lineHeight: 1.2
- role: subheading · size: 20 · lineHeight: 1.2
- role: heading-sm · size: 24 · lineHeight: 1.17
- role: heading · size: 36 · lineHeight: 1.1
- role: heading-lg · size: 48 · lineHeight: 1.1
- role: display-sm · size: 121 · lineHeight: 1
- role: display · size: 145 · lineHeight: 1

## Color Palette


### Neutral
- **Ink** `#000000` — Primary text, headers, icon strokes, borders, and some button fills. This is the dominant dark neutral, grounding the bright canvas
- **Canvas** `#fafafa` — Page backgrounds, card surfaces, and some light text
- **Paper** `#ededed` — Secondary surface backgrounds, used for cards and some buttons, providing a subtle visual distinction from the main canvas
- **Slate** `#666666` — Muted text, secondary link color, and card text details

### Brand
- **Alert Red** `#ff2f00` — Orange action color for filled buttons, selected navigation states, and focused conversion moments.

### Accent
- **Update Yellow** `#ffb700` — Yellow state accent for badges, validation surfaces, and short status labels.
- **Early Access Blue** `#bfe0ff` — Blue state accent for badges, validation surfaces, and short status labels.

## Layout

The page primarily uses a full-bleed layout for hero sections and large image blocks, with content centered within these expansive areas. Subsequent sections typically maintain a maximum content width, creating a spacious, readable flow. The hero pattern features large, centered headlines and calls-to-action over an image background. Vertical rhythm is established by section gaps around 92px. Content often alternates between large textual displays and visual blocks. There are instances of 4-column card grids for features, particularly for font showcases. Navigation is a sticky top bar, minimalist and un-intrusive.


## Imagery

The visual language for imagery varies: hero sections feature large, atmospheric photography or blurred, abstract product shots, often with a dark overlay to provide contrast for white text. Other sections use product-focused imagery (e.g., food items relevant to font names) which are often full-bleed or large-scale background elements. Icons are minimal, typically outlined and black on light backgrounds, or white on dark sections, keeping focus on typography. Imagery serves as evocative atmosphere or direct content showcase rather than decorative flourishes.


## Spacing

- **radius**: {'cards': '20px', 'badges': '999px', 'inputs': '20px', 'buttons': '20px'}
- **elementGap**: 8px
- **sectionGap**: 92px
- **cardPadding**: 26px
- **pageMaxWidth**: None

## Do

- Use Neue Montreal for all textual content, adjusting weights and sizes from the defined typescale for hierarchy.
- Apply a 20px border radius to all interactive elements like buttons and input fields, and all elevated cards.
- Utilize Alert Red (#ff2f00) solely for accenting new features, primary calls-to-action, or important status indicators.
- Maintain a clear distinction between backgrounds: use Canvas (#fafafa) for general pages and Paper (#ededed) for subtly differentiated card surfaces.
- Ensure headings use Ink (#000000) for high contrast against light backgrounds, emphasizing typographic expression.
- Prioritize text and button padding of 7.65px vertical and 22.95px horizontal for a consistent comfortable density.
- Employ the 999px radius for all badges to achieve a distinct pill-shaped visual for status indicators.

## Don't

- Do not use shadows; rely on background color changes, borders, and rounded corners for visual separation and depth.
- Avoid using Alert Red (#ff2f00) for general body text or non-actionable elements, reserving its impact for specific functions.
- Do not deviate from the defined 20px or 999px border radii; inconsistent rounding undermines the soft, approachable aesthetic.
- Do not introduce additional chromatic colors beyond Alert Red, Update Yellow, and Early Access Blue for UI elements.
- Avoid dense, information-heavy blocks of text without ample vertical spacing, as readability is key with the expansive type.
- Do not use very thin strokes for borders; a 1px solid stroke in Ink (#000000) or Canvas (#fafafa) is typical for emphasis or separation.
- Do not use letter-spacing values other than 'normal' for Neue Montreal, as this typeface relies on its natural spacing.

## Components


### Filled Button - Dark
- **role**: Primary action button.
- **description**: Background: Ink (#000000), Text: Canvas (#fafafa). Padding: 7.65px vertical, 22.95px horizontal. Radius: 20px.

### Filled Button - Light
- **role**: Secondary action button.
- **description**: Background: Paper (#ededed) or Canvas (#fafafa), Text: Ink (#000000). Padding: 7.65px vertical, 22.95px horizontal. Radius: 20px.

### Outlined Button - Light
- **role**: Tertiary action button or alternative action.
- **description**: Background: transparent, Text: Canvas (#fafafa), Border: 1px solid Canvas (#fafafa). Padding: 7.65px vertical, 22.95px horizontal. Radius: 20px.

### Outlined Button - Accent
- **role**: Call-to-action with strong visual emphasis.
- **description**: Background: transparent, Text: Alert Red (#ff2f00), Border: 1px Alert Red (#ff2f00). Padding: 7.65px vertical, 22.95px horizontal. Radius: 20px.

### Font Showcase Card - Filled
- **role**: Displays font information within a contained content block.
- **description**: Background: Paper (#ededed), Radius: 20px. Padding: 25.72px on all sides. No shadow.

### Font Showcase Card - Transparent
- **role**: Showcases font information directly on a contrasting background, usually within a themed section.
- **description**: Background: transparent, Radius: 20px. Padding: 25.72px on all sides. No shadow.

### Text Input
- **role**: Form input field.
- **description**: Background: Canvas (#fafafa), Text: Ink (#000000), Border: 1px Ink (#000000). Radius: 20px. Padding: 24px vertical, 45.9px right, 24px left.

### Status Badge - Alert Red
- **role**: Indicates 'New' status or a primary highlight.
- **description**: Background: Alert Red (#ff2f00), Text: Ink (#000000). Radius: 999px (pill shape). Padding: 4px vertical, 11.65px horizontal.

### Status Badge - Update Yellow
- **role**: Indicates 'Update' status.
- **description**: Background: Update Yellow (#ffb700), Text: Ink (#000000). Radius: 999px. Padding: 4px vertical, 11.65px horizontal.

### Status Badge - Early Access Blue
- **role**: Indicates 'Early Access' status.
- **description**: Background: Early Access Blue (#bfe0ff), Text: Ink (#000000). Radius: 999px. Padding: 4px vertical, 11.65px horizontal.

## Agent Prompt Guide

Quick Color Reference:
text: #000000
background: #fafafa
border: #000000
accent: #ff2f00
primary action: #ff2f00 (filled action)

Example Component Prompts:
1. Create a large hero section: full-width dark image background, centered display text 'Neue Montreal' in Neue Montreal weight 600 size 145px (#fafafa). Below it, add caption text 'Version 3 is here!' in Neue Montreal weight 400 size 24px (#fafafa). Include two buttons: 'Explore font' (outlined, transparent background, #fafafa text, #fafafa border, 20px radius, 7.65px vertical 22.95px horizontal padding) and 'Try for Free' (filled, #000000 background, #fafafa text, 20px radius, 7.65px vertical 22.95px horizontal padding).
2. Create a 'Font Showcase Card' for 'Neue York Collection': background #ededed, 20px radius, 25.72px padding. Inside, display font title 'Neue York Collection' in Neue Montreal weight 600 size 18px (#000000). Below that, add descriptive text '48 styles + Variable cuts' in Neue Montreal weight 400 size 14px (#666666). In the top right, place an 'Update' badge: background #ffb700, #000000 text, 999px radius, 4px vertical 11.65px horizontal padding.
3. Design a header with site navigation: background #fafafa, with 'Pangram Pangram Foundry' logo in Neue Montreal weight 600 size 18px (#000000). Navigation links 'All fonts', 'Font starter pack', 'Font in use', 'Academy', 'Support' in Neue Montreal weight 400 size 16px (#000000). Include a search icon and a hamburger menu icon, both in #000000.
