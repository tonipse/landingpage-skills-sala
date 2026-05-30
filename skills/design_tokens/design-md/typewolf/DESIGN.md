---
version: alpha
source: refero
source_id: c46ecd77-9c92-4a85-9162-c6d4afd99d95
source_url: https://typewolf.com
name: Typewolf
description: "This design system evokes the tactile quality of a letterpress studio, balancing classic elegance with a distinct, almost academic feel. A highly restrained palette of mauves and desaturated grays, anchored by a creamy off-white background, defines its sophisticated, understated mood. The interplay of custom serif and sans-serif fonts, particularly a heavy sans-serif with subtle negative letter-spacing for accents, establishes an intellectual yet approachable tone, akin to a well-curated typographic journal."
theme: light
northStar: "Letterpress on aged paper. This design feels like pages from an expertly printed, well-loved typography textbook."
category: editorial
tags: ["editorial", "typography-focused", "muted-palette", "classic-modern", "text-heavy", "sophisticated", "clean-layout", "serene", "informational", "monochromatic"]

colors:
  cream-canvas: "#f8f5f5"  # neutral — Page backgrounds, subtle card outlines, content separators.
  cloud-white: "#ffffff"  # neutral — Card backgrounds, input fields, highlighted content blocks.
  dusty-mauve: "#cfc6c7"  # neutral — Input and button borders, subtle dividers.
  inkwell-gray: "#443235"  # neutral — Primary body text, link default state, subtle decorative elements, badge text.
  charcoal-text: "#2e2c2c"  # neutral — Headings, prominent text, high-contrast elements.
  plum-accent: "#654a4"  # brand — Hover state for links and navigation, secondary buttons, subtle background for selected it
  rosewood-cta: "#916a70"  # brand — Primary call-to-action buttons, active navigation items — a warm, inviting accent without 

typography:
  domainetext:
    family: "DomaineText"
    sizes: "14px, 16px, 18px, 24px, 28px"
    weight: "400"
    lineHeight: "1.20, 1.25, 1.30, 1.40, 1.45, 1.50"
    letterSpacing: "normal"
    substitute: "Source Serif Pro"
    use: "Primary display serif font for subtle headings, body text, badges, and general content. Its distinct character shapes define the site's classic, editorial feel. Sizes 14-18px at weight 400 are common "
  dia:
    family: "Dia"
    sizes: "12px, 13px, 14px, 15px"
    weight: "900"
    lineHeight: "1.20, 1.30, 2.20"
    letterSpacing: "-0.0300em"
    substitute: "Inter"
    use: "Distinctive sans-serif used for navigation items, secondary headings, and interactive elements. Its extreme weight (900) at small sizes (12-15px) with negative letter-spacing (-0.03em) creates a conde"
  domainedisplaynarrow:
    family: "DomaineDisplayNarrow"
    sizes: "26px, 42px, 46px"
    weight: "700"
    lineHeight: "1.20"
    letterSpacing: "normal"
    substitute: "Playfair Display"
    use: "Primary serif font for prominent headings. Used at larger sizes (26-46px) and a bold weight (700) for impactful titles, maintaining an elegant, authoritative presence."
---

# Typewolf — Design System

> Letterpress on aged paper. This design feels like pages from an expertly printed, well-loved typography textbook.


This design system evokes the tactile quality of a letterpress studio, balancing classic elegance with a distinct, almost academic feel. A highly restrained palette of mauves and desaturated grays, anchored by a creamy off-white background, defines its sophisticated, understated mood. The interplay of custom serif and sans-serif fonts, particularly a heavy sans-serif with subtle negative letter-spacing for accents, establishes an intellectual yet approachable tone, akin to a well-curated typographic journal.


## Type Scale

- role: caption · size: 12 · lineHeight: 1.3 · letterSpacing: -0.48
- role: body-sm · size: 14 · lineHeight: 1.5
- role: body · size: 16 · lineHeight: 1.4
- role: subheading · size: 18 · lineHeight: 1.25
- role: heading-sm · size: 24 · lineHeight: 1.2
- role: heading · size: 26 · lineHeight: 1.2
- role: heading-lg · size: 42 · lineHeight: 1.2
- role: display · size: 46 · lineHeight: 1.2

## Color Palette


### Neutral
- **Cream Canvas** `#f8f5f5` — Page backgrounds, subtle card outlines, content separators.
- **Cloud White** `#ffffff` — Card backgrounds, input fields, highlighted content blocks.
- **Dusty Mauve** `#cfc6c7` — Input and button borders, subtle dividers.
- **Inkwell Gray** `#443235` — Primary body text, link default state, subtle decorative elements, badge text.
- **Charcoal Text** `#2e2c2c` — Headings, prominent text, high-contrast elements.

### Brand
- **Plum Accent** `#654a4` — Hover state for links and navigation, secondary buttons, subtle background for selected items — providing depth and interaction feedback.
- **Rosewood CTA** `#916a70` — Primary call-to-action buttons, active navigation items — a warm, inviting accent without overt vibrancy.

## Layout

The page primarily uses a max-width contained model, with content centered. The hero section features a centered headline and subtitle over the Cream Canvas background. Content sections generally consist of a grid of cards, often two columns wide, each card presenting a distinct article or resource. Each card is a self-contained unit with its own content and visual treatment. There's a consistent vertical rhythm of spacing between elements and sections, contributing to an organized, readable flow. Navigation is a minimalist top-bar with horizontally listed links, and a prominent header introducing the brand. The layout is information-dense yet visually uncluttered.


## Imagery

This site features illustrations and product screenshots, all contained within specific sections or cards. Illustrations are line-art based, often black or brand-colored on a solid, muted background (like the orange card background). Photography, when present, appears to be product-focused (e.g., large letterforms, type specimens). The overall treatment is contained and isolated, with no full-bleed or overlapping imagery. Images serve an explanatory or decorative role within their content blocks, enhancing the editorial feel rather than dominating the layout. Icons are minimal, likely line-art to match the illustrations.


## Spacing

- **radius**: {'small': '4px', 'default': '0px'}
- **elementGap**: 
- **sectionGap**: 64px
- **cardPadding**: 12px
- **pageMaxWidth**: None

## Do

- Use Cream Canvas (#f8f5f5) as the default page background to establish the site's light, subtle aesthetic.
- Apply Charcoal Text (#2e2c2c) for primary headlines and Inkwell Gray (#443235) for body text, maintaining contrast and readability.
- Emphasize interactive elements and calls to action with Rosewood CTA (#916a70) as the background color for primary buttons.
- Utilize Dia 900 font with -0.03em letter-spacing for all navigation items and concise, impactful labels.
- Maintain a default border radius of 0px for most elements to reinforce the crisp, structured aesthetic, only deviating to 4px for specific components where a subtle break is required.
- Apply the shadow rgba(145, 106, 112, 0.15) 0px 6px 24px 0px for elevated content cards, ensuring subtle depth without harshness.
- Employ DomaineText at 14-18px for body and descriptive text to maintain the editorial and inviting tone.

## Don't

- Avoid using highly saturated, vibrant colors; stick to the muted, near-gray, and earthy tones defined in the palette.
- Do not introduce rounded corners arbitrarily; reserve the 4px radius only where explicitly defined for small, functional elements.
- Refrain from using excessively bold weights for body text; DomaineText 400 is sufficient for paragraphs.
- Do not deviate from the specified letter-spacing for Dia font; the -0.03em is integral to its distinctive appearance.
- Do not use dark backgrounds for main content areas; the design is firmly built on a light theme with Cream Canvas and Cloud White surfaces.
- Avoid generic, system fonts; prioritize DomaineText, Dia, and DomaineDisplayNarrow to preserve the site's unique typographic identity.
- Do not use box-shadows on individual text elements; reserve them for content containers like cards for subtle elevation.

## Components


### Content Card Grid
- **html**: <style>:root{--color-cream-canvas:#f8f5f5;--color-cloud-white:#ffffff;--color-dusty-mauve:#cfc6c7;--color-inkwell-gray:#443235;--color-charcoal-text:#2e2c2c;--color-plum-accent:#654a4e;--color-rosewood-cta:#916a70;--font-domainetext:'Source Serif Pro',Georgia,serif;--font-dia:'Inter',sans-serif;--font-domainedisplaynarrow:'Playfair Display',Georgia,serif;--shadow-lg:rgba(145,106,112,0.15) 0px 6px 24px 0px;}</style><div style="background:var(--color-cream-canvas);padding:32px;font-family:var(--font-domainetext);width:600px;box-sizing:border-box;"><div style="display:grid;grid-template-columns:1fr 1fr;gap:20px;"><div style="background:var(--color-cloud-white);box-shadow:var(--shadow-lg);border-radius:0px;"><div style="width:100%;height:160px;background:#e8b86d;display:flex;align-items:center;justify-content:center;overflow:hidden;"><div style="text-align:center;padding:16px;"><div style="font-family:var(--font-domainedisplaynarrow);font-size:28px;font-weight:700;color:var(--color-charcoal-text);line-height:1.2;">By the Numbers</div><div style="font-family:var(--font-domainetext);font-size:12px;color:var(--color-charcoal-text);margin-top:8px;line-height:1.4;">Proven care, powerful results.</div></div></div><div style="padding:12px;"><div style="display:flex;justify-content:space-between;align-items:baseline;margin-bottom:4px;"><a href="#" style="font-family:var(--font-domainedisplaynarrow);font-size:15px;font-weight:700;color:var(--color-rosewood-cta);text-decoration:none;">Daylight</a><span style="font-family:var(--font-dia);font-size:11px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);text-transform:uppercase;">Dec 14, 2025</span></div><div style="font-family:var(--font-dia);font-size:11px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);"><span style="text-transform:uppercase;">Fonts</span> <span style="font-weight:400;font-family:var(--font-domainetext);font-size:13px;letter-spacing:normal;">— Grenette, Styrene</span></div></div></div><div style="background:var(--color-cloud-white);box-shadow:var(--shadow-lg);border-radius:0px;"><div style="width:100%;height:160px;background:#2d3d1e;display:flex;align-items:center;justify-content:center;overflow:hidden;"><div style="text-align:center;padding:16px;"><div style="font-family:var(--font-domainedisplaynarrow);font-size:32px;font-weight:700;color:var(--color-cloud-white);line-height:1.25;">Spring</div><div style="font-family:var(--font-domainedisplaynarrow);font-size:32px;font-weight:700;color:var(--color-cloud-white);line-height:1.25;">Summer</div></div></div><div style="padding:12px;"><div style="display:flex;justify-content:space-between;align-items:baseline;margin-bottom:4px;"><a href="#" style="font-family:var(--font-domainedisplaynarrow);font-size:15px;font-weight:700;color:var(--color-rosewood-cta);text-decoration:none;">Heart &amp; Soil</a><span style="font-family:var(--font-dia);font-size:11px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);text-transform:uppercase;">Dec 13, 2025</span></div><div style="font-family:var(--font-dia);font-size:11px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);"><span style="text-transform:uppercase;">Fonts</span> <span style="font-weight:400;font-family:var(--font-domainetext);font-size:13px;letter-spacing:normal;">— Cardinal, Sweet Sans, Baskerville</span></div></div></div><div style="background:var(--color-cloud-white);box-shadow:var(--shadow-lg);border-radius:0px;"><div style="width:100%;height:160px;background:#d4e09a;display:flex;align-items:center;justify-content:center;overflow:hidden;"><div style="font-family:var(--font-domainedisplaynarrow);font-size:26px;font-weight:700;color:#2a4a1a;line-height:1.2;padding:16px;">Natural wines are additive-free</div></div><div style="padding:12px;"><div style="display:flex;justify-content:space-between;align-items:baseline;margin-bottom:4px;"><a href="#" style="font-family:var(--font-domainedisplaynarrow);font-size:15px;font-weight:700;color:var(--color-rosewood-cta);text-decoration:none;">Dirty Vine</a><span style="font-family:var(--font-dia);font-size:11px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);text-transform:uppercase;">Dec 12, 2025</span></div><div style="font-family:var(--font-dia);font-size:11px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);"><span style="text-transform:uppercase;">Fonts</span> <span style="font-weight:400;font-family:var(--font-domainetext);font-size:13px;letter-spacing:normal;">— Swear, DM Mono</span></div></div></div><div style="background:var(--color-cloud-white);box-shadow:var(--shadow-lg);border-radius:0px;"><div style="width:100%;height:160px;background:#c9b99a;display:flex;align-items:center;justify-content:center;overflow:hidden;"><div style="font-family:var(--font-domainedisplaynarrow);font-size:42px;font-weight:700;color:var(--color-cloud-white);line-height:1.1;padding:16px;">Gather round</div></div><div style="padding:12px;"><div style="display:flex;justify-content:space-between;align-items:baseline;margin-bottom:4px;"><a href="#" style="font-family:var(--font-domainedisplaynarrow);font-size:15px;font-weight:700;color:var(--color-rosewood-cta);text-decoration:none;">Board</a><span style="font-family:var(--font-dia);font-size:11px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);text-transform:uppercase;">Dec 10, 2025</span></div><div style="font-family:var(--font-dia);font-size:11px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);"><span style="text-transform:uppercase;">Fonts</span> <span style="font-weight:400;font-family:var(--font-domainetext);font-size:13px;letter-spacing:normal;">— Kabel, Neue Haas Grotesk</span></div></div></div></div></div>

### Navigation Bar
- **html**: <style>:root{--color-cream-canvas:#f8f5f5;--color-cloud-white:#ffffff;--color-dusty-mauve:#cfc6c7;--color-inkwell-gray:#443235;--color-charcoal-text:#2e2c2c;--color-plum-accent:#654a4e;--color-rosewood-cta:#916a70;--font-domainetext:'Source Serif Pro',Georgia,serif;--font-dia:'Inter',sans-serif;--font-domainedisplaynarrow:'Playfair Display',Georgia,serif;}</style><div style="background:var(--color-cream-canvas);width:600px;box-sizing:border-box;font-family:var(--font-domainetext);"><div style="text-align:center;padding:40px 32px 20px;"><div style="font-family:var(--font-domainedisplaynarrow);font-size:56px;font-weight:700;color:var(--color-cloud-white);background:var(--color-inkwell-gray);display:inline-block;padding:8px 28px;letter-spacing:-1px;line-height:1.1;">Typewolf</div><div style="font-family:var(--font-domainetext);font-size:18px;color:var(--color-inkwell-gray);margin-top:14px;letter-spacing:0.01em;">What's Trending in Type</div></div><div style="border-top:1px solid var(--color-dusty-mauve);margin:0 32px;"></div><nav style="display:flex;justify-content:center;align-items:center;gap:32px;padding:18px 32px;"><a href="#" style="font-family:var(--font-dia);font-size:13px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);text-decoration:none;text-transform:uppercase;">Font Lists</a><a href="#" style="font-family:var(--font-dia);font-size:13px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);text-decoration:none;text-transform:uppercase;">Lookbooks</a><a href="#" style="font-family:var(--font-dia);font-size:13px;font-weight:900;letter-spacing:-0.03em;color:var(--color-rosewood-cta);text-decoration:none;text-transform:uppercase;">Checklist</a><a href="#" style="font-family:var(--font-dia);font-size:13px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);text-decoration:none;text-transform:uppercase;">Free Fonts</a><a href="#" style="font-family:var(--font-dia);font-size:13px;font-weight:900;letter-spacing:-0.03em;color:var(--color-inkwell-gray);text-decoration:none;text-transform:uppercase;">Learning Resources</a></nav><div style="border-top:1px solid var(--color-dusty-mauve);margin:0 32px;"></div></div>

### Promo Card — Definitive Guide
- **html**: <style>:root{--color-cream-canvas:#f8f5f5;--color-cloud-white:#ffffff;--color-dusty-mauve:#cfc6c7;--color-inkwell-gray:#443235;--color-charcoal-text:#2e2c2c;--color-plum-accent:#654a4e;--color-rosewood-cta:#916a70;--font-domainetext:'Source Serif Pro',Georgia,serif;--font-dia:'Inter',sans-serif;--font-domainedisplaynarrow:'Playfair Display',Georgia,serif;--shadow-lg:rgba(145,106,112,0.15) 0px 6px 24px 0px;}</style><div style="background:var(--color-cream-canvas);padding:32px;width:600px;box-sizing:border-box;"><div style="background:var(--color-cloud-white);box-shadow:var(--shadow-lg);display:flex;flex-direction:column;"><div style="background:#f0ebe8;height:220px;display:flex;align-items:center;justify-content:center;padding:32px;"><div style="font-family:var(--font-domainedisplaynarrow);font-size:38px;font-weight:700;color:var(--color-charcoal-text);line-height:1.2;text-align:center;">The Closest Free Alternative to Every Font on Typewolf</div></div><div style="padding:20px 20px 24px;"><div style="display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:12px;"><div><div style="font-family:var(--font-domainedisplaynarrow);font-size:18px;font-weight:700;color:var(--color-rosewood-cta);margin-bottom:6px;">The Definitive Guide to Free Fonts</div><div style="font-family:var(--font-domainetext);font-size:14px;color:var(--color-inkwell-gray);line-height:1.5;max-width:380px;">An expertly curated resource identifying the best free alternatives to premium fonts — perfect for designers working on any budget.</div></div><div style="font-family:var(--font-dia);font-size:18px;font-weight:900;letter-spacing:-0.03em;color:var(--color-rosewood-cta);white-space:nowrap;margin-left:20px;">$39</div></div><div style="display:flex;gap:12px;margin-top:16px;"><a href="#" style="display:inline-block;background:var(--color-rosewood-cta);color:var(--color-cloud-white);font-family:var(--font-dia);font-size:13px;font-weight:900;letter-spacing:-0.03em;text-transform:uppercase;text-decoration:none;padding:15px 20px 12px;border-radius:0;border:none;">Get the Guide</a><a href="#" style="display:inline-block;background:var(--color-plum-accent);color:var(--color-cloud-white);font-family:var(--font-dia);font-size:13px;font-weight:900;letter-spacing:-0.03em;text-transform:uppercase;text-decoration:none;padding:15px 20px 12px;border-radius:0;border:none;">Learn More</a></div></div></div></div>

### Primary Call to Action Button
- **role**: Interactive element
- **description**: Filled button with Rosewood CTA background (#916a70), Cloud White text (#ffffff). No border radius, borders are 0px. Padding is top: 15px, right: 11px, bottom: 12px, left: 11px.

### Secondary Button
- **role**: Interactive element
- **description**: Filled button with Plum Accent background (#654a4e), Cloud White text (#ffffff). No border radius, borders are 0px. Padding is top: 18px, right: 20px, bottom: 16px, left: 20px.

### Default Input Field
- **role**: Data input
- **description**: Cloud White background (#ffffff), Inkwell Gray text (#443235). Border is 1px solid Dusty Mauve (#cfc6c7). No border radius, borders are 0px. Padding is 10.5px on all sides.

### Flat Badge
- **role**: Categorization/metadata
- **description**: Transparent background (rgba(0,0,0,0)), Inkwell Gray text (#443235). No border, no border radius. No explicit padding (0px on all sides), relying on text spacing.

### Content Card
- **role**: Content container
- **description**: Cloud White background (#ffffff) with a subtle shadow: rgba(145, 106, 112, 0.15) 0px 6px 24px 0px. No explicit border radius other than 0px. Internal padding varies; content areas often have 12px vertical spacing with elements. Headlines use DomaineDisplayNarrow 46px/1.2 at #2e2c2c.

### Navigation Link
- **role**: Navigation element
- **description**: Dia 900, 14px/-0.03em letter-spacing, Inkwell Gray (#443235). On hover, color changes to Plum Accent (#654a4e). No explicit background or radius.

### Hero Section Title
- **role**: Page headline
- **description**: DomaineDisplayNarrow 700 with size 46px and lineHeight 1.2, in Charcoal Text (#2e2c2c). Subtitle uses DomaineText 18px 400.

## Agent Prompt Guide

### Quick Color Reference
- Text (body): #443235
- Text (headline): #2e2c2c
- Background (page): #f8f5f5
- Background (card): #ffffff
- CTA (button): #916a70
- Primary Accent: #654a4e

### 3-5 Example Component Prompts
1.  **Create a Primary Call to Action Button:** text 'Learn More →', background #916a70, text color #ffffff, border-radius 0px, padding 15px 11px 12px 11px. Font is Dia 900, 14px, lineHeight 1.2, letterSpacing -0.03em.
2.  **Generate a Content Card:** white background #ffffff, with shadow rgba(145, 106, 112, 0.15) 0px 6px 24px 0px. Headline 'My Favorite Fonts' in DomaineDisplayNarrow 700, 26px, #2e2c2c. Body text 'A curated list...' in DomaineText 400, 16px, #443235. Internal padding around content of 12px.
3.  **Design a Navigation Link:** text 'Font Lists', color #443235. On hover, color changes to #654a4e. Font is Dia 900, 14px, lineHeight 1.2, letterSpacing -0.03em. No background, no padding.
4.  **Compose a Default Input Field:**  background #ffffff, text color #443235, border 1px solid #cfc6c7, border-radius 0px, padding 10.5px. Placeholder text is DomaineText 400, 16px, #443235 with 50% opacity.
