---
version: alpha
source: refero
source_id: b63cc4ca-52c6-4b70-9a5a-cb04bae15edb
source_url: https://www.logo-archive.org
name: LogoArchive
description: "LogoArchive presents a commanding dark-mode experience, reminiscent of a digital archive or library. Its aesthetic is dominated by deep, muted neutrals, creating a profound backdrop for content. Typography favors compact, confident sans-serifs, reserving a single, vivid yellow for functional accents. Components are lightweight with subtle border treatments and generous curves, balancing utility with a soft, approachable feel against the dark canvas."
theme: dark
northStar: "Deep Digital Archive."

colors:
  midnight-ink: "#000000"  # neutral — Page background (primary), card surfaces, text on bright surfaces
  carbon: "#18181b"  # neutral — Decorative fill for icons and abstract shapes
  steel-gray: "#27272a"  # neutral — Card backgrounds, button backgrounds, secondary surface color
  ash-gray: "#343538"  # neutral — Dark borders and separators for elevated surfaces and inverted UI. Do not promote it to th
  sky-haze: "#a8afb7"  # neutral — Muted secondary text, helper text, subtle borders
  stone: "#8c8c8d"  # neutral — List item backgrounds, tertiary background for subtle differentiation
  porcelain: "#ffffff"  # neutral — Primary text, icon fill, button text, card borders
  polar-mist: "#dadee4"  # neutral — Subtle background tones, light border accents
  amber-glow: "#fde533"  # accent — Yellow outline accent for tags, dividers, and focused UI edges. Do not promote it to the p

typography:
  suisse-international:
    family: "Suisse International"
    sizes: "12px, 14px, 16px, 18px, 19px, 24px, 28px, 65px, 96px"
    weight: "400, 500"
    lineHeight: "0.90, 1.00, 1.20, 1.75"
    letterSpacing: "normal"
    substitute: "Inter"
    use: "Primary content font for all text elements: headings (bold, large), body text, navigation, and button labels. Its wide range of weights and sizes provides clear visual hierarchy within a consistent ae"
  suisse-works-book:
    family: "Suisse Works Book"
    sizes: "65px, 96px"
    weight: "400"
    lineHeight: "1.00, 1.20"
    letterSpacing: "normal"
    substitute: "Lora"
    use: "Used selectively for large, prominent headings, specifically for the main hero statements. Its distinct character provides a stylistic contrast to Suisse International while maintaining legibility."
---

# LogoArchive — Design System

> Deep Digital Archive.


LogoArchive presents a commanding dark-mode experience, reminiscent of a digital archive or library. Its aesthetic is dominated by deep, muted neutrals, creating a profound backdrop for content. Typography favors compact, confident sans-serifs, reserving a single, vivid yellow for functional accents. Components are lightweight with subtle border treatments and generous curves, balancing utility with a soft, approachable feel against the dark canvas.


## Type Scale

- role: caption · size: 12 · lineHeight: 1.75
- role: body-sm · size: 14 · lineHeight: 1.75
- role: body · size: 16 · lineHeight: 1.75
- role: subheading · size: 18 · lineHeight: 1.75
- role: heading-sm · size: 24 · lineHeight: 1.2
- role: heading · size: 28 · lineHeight: 1.2
- role: heading-lg · size: 65 · lineHeight: 1
- role: display · size: 96 · lineHeight: 0.9

## Color Palette


### Neutral
- **Midnight Ink** `#000000` — Page background (primary), card surfaces, text on bright surfaces
- **Carbon** `#18181b` — Decorative fill for icons and abstract shapes
- **Steel Gray** `#27272a` — Card backgrounds, button backgrounds, secondary surface color
- **Ash Gray** `#343538` — Dark borders and separators for elevated surfaces and inverted UI. Do not promote it to the primary CTA color
- **Sky Haze** `#a8afb7` — Muted secondary text, helper text, subtle borders
- **Stone** `#8c8c8d` — List item backgrounds, tertiary background for subtle differentiation
- **Porcelain** `#ffffff` — Primary text, icon fill, button text, card borders
- **Polar Mist** `#dadee4` — Subtle background tones, light border accents

### Accent
- **Amber Glow** `#fde533` — Yellow outline accent for tags, dividers, and focused UI edges. Do not promote it to the primary CTA color

## Layout

The page maintains a centered, max-width contained layout rather than full-bleed, creating a focused experience within the surrounding Midnight Ink canvas. The hero section features large, centered headlines over the dark background, often incorporating a single graphic element. Section rhythm is built on consistent vertical spacing, often with content blocks stacking vertically or arranging in multi-column grids (like the pricing cards). There are no overt visual dividers; sections flow into each other via background changes. Navigation is a minimal top bar with simple text links.


## Imagery

This site prominently features product screenshots and abstract graphics. Product screenshots are typically close-cropped UI elements or full interface views presented on the deep dark background, often showcasing geometric logo arrays. Imagery is contained, never full-bleed, and integrates seamlessly with the surrounding UI. Icons are simple, outlined or filled in monochromatic tones (Porcelain, Carbon), maintaining a clean, utilitarian aesthetic. The focus is on visual content as explanatory rather than decorative, showcasing the product directly.


## Spacing

- **radius**: {'tags': '999px', 'cards': '28px', 'lists': '40px', 'buttons': '20px'}
- **elementGap**: 8px
- **sectionGap**: 24px
- **cardPadding**: 32px
- **pageMaxWidth**: None

## Do

- Use Midnight Ink (#000000) for all primary page backgrounds and main text on Amber Glow surfaces.
- Apply Suisse International for all type, adjusting weight and size to create hierarchy, except for specific large hero headlines.
- Employ Steel Gray (#27272a) for default card backgrounds and subtle interactive elements.
- Prioritize a 28px border radius for most content cards and a 20px radius for buttons.
- Use Amber Glow (#fde533) exclusively for primary calls to action, tags, and small functional highlights.
- Maintain a compact element spacing with 8px as the default gap between components where possible.
- Ensure primary text is Porcelain (#ffffff) on dark backgrounds for optimal contrast.

## Don't

- Avoid using multiple chromatic colors; Amber Glow (#fde533) is the primary accent.
- Do not use box shadows for elevation; rely on background color differences and subtle borders instead.
- Refrain from using thin weights of type on dark backgrounds where legibility could be compromised.
- Do not introduce square or minimally rounded corners; all interface elements should embrace significant corner radii.
- Avoid large empty spaces beyond the pageMaxWidth; the layout should feel dense yet organized.
- Do not use generic system fonts; Suisse International and Suisse Works Book define the brand's typographic voice.
- Do not use generic grey for interactive states; utilize the Amber Glow (#fde533) for hover/active where appropriate for primary actions.

## Components


### Primary Action Button
- **role**: Call to action
- **description**: Filled with Amber Glow (#fde533) with Midnight Ink (#000000) text, 20px border radius, and 4px 10px padding.

### Ghost Secondary Button
- **role**: Secondary action
- **description**: Transparent background with Porcelain (#ffffff) text and 1px Porcelain (#ffffff) border, 20px border radius, and 4px 10px padding.

### Subtle Secondary Button
- **role**: Secondary action on dark backgrounds
- **description**: Filled with Steel Gray (#27272a) background with Porcelain (#ffffff) text, 20px border radius, and 4px 10px padding.

### Standard Content Card
- **role**: Content grouping
- **description**: Steel Gray (#27272a) background, 28px border radius, and 120px 0px 0px 0px padding. No shadow.

### Elevated Content Card
- **role**: Content grouping, slightly more prominent
- **description**: Ash Gray (#343538) background, 22px border radius, and 32px 48px 32px 32px padding. No shadow.

### Minimal Card
- **role**: Basic container
- **description**: Midnight Ink (#000000) background, 28px border radius. No padding.

### Pill Tag
- **role**: Informational tag or filter
- **description**: Porcelain (#ffffff) background with Midnight Ink (#000000) text, 999px border radius for a pill shape.

## Agent Prompt Guide

Quick Color Reference: 
text: #ffffff
background: #000000
border: #ffffff
accent: #fde533
primary action: #27272a (filled action)

Example Component Prompts:
1. Create a Primary Action Button: #27272a background, #ffffff text, 9999px radius, compact pill padding. Use this filled treatment for the main CTA.
2. Build a content card with a title 'Monthly' in Suisse International, weight 500, size 24px, line-height 1.2, color #ffffff. Use a Steel Gray (#27272a) background, 28px border radius, and 120px 0px 0px 0px padding. Inside, include a ghost text button: 'See pricing' with text #ffffff, transparent background, 1px border #ffffff, 20px radius, 4px 10px padding.
3. Design a small informational tag: 'A new format' using Amber Glow (#fde533) background, text #000000, and a 999px border radius with 4px 10px padding. Place it with an 8px element gap from a larger heading.
