---
version: alpha
source: refero
source_id: 597355de-6167-4f37-8f14-b3897919a94c
source_url: https://exhibition-magazine.com
name: Exhibition Magazine
description: "Exhibition Magazine embraces a high-contrast editorial aesthetic: stark black and white punctuated by strong photographic imagery. Content is presented on clean, unadorned surfaces with minimal elevation, emphasizing typography and photography. Subtle linear borders provide structure without visual weight. The overall impression is one of confident, minimalist sophistication, focusing reader attention on the curated content."
theme: light
northStar: "monochrome editorial canvas"

colors:
  canvas-white: "#ffffff"  # neutral — Page backgrounds, header, card backgrounds. Provides a clean, bright stage for content
  ink-black: "#000000"  # neutral — Primary text, headings, navigational elements. Establishes a bold and authoritative textua
  divider-gray: "#e5e7eb"  # neutral — Subtle borders for cards, navigation items, and other structural dividers. Provides soft v
  muted-surface: "#a9a9a9"  # neutral — Secondary card backgrounds, subtly differentiating content blocks or for specific sections
  blush-card-back: "#fff5fa"  # neutral — Accent background for specific featured cards or content areas, adding a hint of warmth
  swiper-accent: "#007aff"  # accent — Supporting palette color for small decorative accents when the core palette needs contrast

typography:
  cochin:
    family: "Cochin"
    sizes: "16px, 46px"
    weight: "400"
    lineHeight: "1.20, 1.50"
    substitute: "Georgia"
    use: "Primary body text and descriptive links. Its humanist serifs provide a classic, editorial feel against the modern sans-serifs, a deliberate contrast for readability and character."
  din:
    family: "DIN"
    sizes: "25px, 36px, 40px, 50px, 52px, 90px, 100px"
    weight: "400"
    lineHeight: "0.75, 0.80, 1.00, 1.20"
    letterSpacing: "-0.0080em, -0.0060em, -0.0040em"
    substitute: "Inter"
    use: "Dominant display typography for headings, titles, and calls to action. Its condensed, strong sans-serif form exudes a bold, confident voice, with tight letter-spacing enhancing its impact."
  forma-djr-display:
    family: "forma-djr-display"
    sizes: "13px"
    weight: "500"
    lineHeight: "1.60"
    letterSpacing: "0.0620em"
    substitute: "Roboto Mono"
    use: "Small, highly tracked uppercase text for descriptors and meta-information. The wide letter-spacing adds a contemporary, functional touch for annotation."
---

# Exhibition Magazine — Design System

> monochrome editorial canvas


Exhibition Magazine embraces a high-contrast editorial aesthetic: stark black and white punctuated by strong photographic imagery. Content is presented on clean, unadorned surfaces with minimal elevation, emphasizing typography and photography. Subtle linear borders provide structure without visual weight. The overall impression is one of confident, minimalist sophistication, focusing reader attention on the curated content.


## Type Scale

- role: caption · size: 13 · lineHeight: 1.6 · letterSpacing: 0.79
- role: body · size: 16 · lineHeight: 1.5
- role: subheading · size: 25 · lineHeight: 1.2 · letterSpacing: -0.2
- role: heading · size: 36 · lineHeight: 1.2 · letterSpacing: -0.2
- role: heading-lg · size: 40 · lineHeight: 1 · letterSpacing: -0.2
- role: display-sm · size: 46 · lineHeight: 1.2
- role: display · size: 90 · lineHeight: 0.8 · letterSpacing: -0.36

## Color Palette


### Neutral
- **Canvas White** `#ffffff` — Page backgrounds, header, card backgrounds. Provides a clean, bright stage for content
- **Ink Black** `#000000` — Primary text, headings, navigational elements. Establishes a bold and authoritative textual presence against light backgrounds
- **Divider Gray** `#e5e7eb` — Subtle borders for cards, navigation items, and other structural dividers. Provides soft visual separation without being intrusive
- **Muted Surface** `#a9a9a9` — Secondary card backgrounds, subtly differentiating content blocks or for specific sections
- **Blush Card Back** `#fff5fa` — Accent background for specific featured cards or content areas, adding a hint of warmth

### Accent
- **Swiper Accent** `#007aff` — Supporting palette color for small decorative accents when the core palette needs contrast. Do not promote it to the primary CTA color

## Layout

The page primarily uses a full-bleed layout for hero sections, filling the viewport horizontally. Content sections then generally narrow to a contained maximum width, centered on the page. The hero features a large full-bleed image with centered overlaid text. Sections follow a consistent vertical rhythm with a 60px gap. Content is arranged in alternating patterns, often with large image cards followed by text blocks. There's a clear 4-column implied grid for card layouts, though some sections use a single dominant image. Navigation is a minimalist top bar, sticky or otherwise. The overall density is comfortable, allowing for strong visual impact from images and typography.


## Imagery

This design system primarily utilizes photography, which is often full-bleed and serves as the dominant visual element. Images are usually high-contrast and often moody, presented with raw, un-masked edges and no rounding. Product shots are contained within image cards, and lifestyle photography in hero sections is used to set the tone rather than provide explicit information. Icons are minimal, likely outlined and monochromatic, acting as functional cues rather than decorative elements. Image density is high, with visuals often taking precedence over text in content blocks.


## Spacing

- **radius**: {'cards': '0px', 'buttons': '100%'}
- **elementGap**: 12px
- **sectionGap**: 60px
- **cardPadding**: 24px
- **pageMaxWidth**: None

## Do

- Prioritize Ink Black (#000000) for all primary text and headings against Canvas White (#ffffff) backgrounds for maximum contrast.
- Use DIN font exclusively for all headings and significant display text, with its characteristic tight letter-spacing.
- Structure content using Divider Gray (#e5e7eb) for subtle linear borders and dividers, rather than heavy backgrounds or shadows.
- Treat images as full-bleed within their content containers, adhering to the 0px border-radius for a stark, unconstrained look.
- Reserve the Swiper Accent (#007aff) for minimal interactive cues, avoiding its use for primary calls to action or decorative elements.
- Maintain generous section gaps of 60px to provide ample white space and visual breathing room between content blocks.
- Utilize forma-djr-display for small supporting text, always uppercase and highly tracked (0.0620em) to differentiate it.

## Don't

- Avoid using drop shadows or complex gradients; the design relies on flat surfaces and high contrast.
- Do not introduce new saturated colors; the palette is intentionally monochromatic with a single, highly controlled accent.
- Do not apply rounded corners to cards or main content blocks; maintain sharp, crisp edges (0px radius).
- Avoid decorative background patterns or textures; surfaces should remain clean and uncluttered.
- Do not use Cochin for headlines or large display text; its role is specifically for body copy and descriptive links.
- Do not place buttons or interactive elements on Muted Surface (#a9a9a9) or Blush Card Back (#fff5fa) backgrounds without sufficient contrast for text and interaction states.
- Do not create dense, information-heavy blocks without substantial white space; content should be spaced out to maintain clarity.

## Components


### Carousel Navigation Button
- **role**: Interactive element to navigate image carousels
- **description**: Ghost button with an Ink Black border on hover, 100% border-radius for a circular shape, with its primary text also in Ink Black. No explicit padding, relying on content for size.

### Load More Button
- **role**: Expands content using a prominent call to action.
- **description**: Ink Black text, sans background, underlined with Ink Black for emphasis. Utilizes the DIN font for its commanding presence.

### Image Card Default
- **role**: Displays articles or features prominently with large imagery.
- **description**: Transparent background with no shadow or border-radius, images are typically full-bleed within the card area. Text overlays are in Ink Black, featuring Cochin for descriptive text and DIN for titles.

### Blush Content Card
- **role**: Highlights specific curated content or editorial picks.
- **description**: Uses Blush Card Back (#fff5fa) as its background color, with 24px padding on all sides. No border-radius or shadow, maintaining the flat aesthetic.

### Hero Section Header
- **role**: Primary visual for articles, featuring a large image and overlaid title.
- **description**: Full-bleed image background with overlaid Ink Black text using the DIN font for headlines. Associated descriptive text uses Cochin. The layout is centered, minimalist.

### Navigation Link
- **role**: Top-level navigation items
- **description**: Ink Black text in DIN font, with a Divider Gray underline on hover, contributing to the stark, functional header.

## Agent Prompt Guide

Quick Color Reference:
text: #000000
background: #ffffff
border: #e5e7eb
accent: #007aff
primary action: no distinct CTA color

Example Component Prompts:
Create a navigation link: 'FASHION' text, #000000 color, DIN font weight 400, size 16px, with a #e5e7eb underline on hover.
Create a hero section title: 'EXHIBITION MAGAZINE' text, #000000 color, DIN font weight 400, size 90px, letter-spacing -0.0040em. Image background.
Create an image card: Transparent background, 0px border-radius, an image filling the card, with a text overlay using Cochin 16px weight 400 for description and DIN 25px weight 400 for title, both in #000000.
