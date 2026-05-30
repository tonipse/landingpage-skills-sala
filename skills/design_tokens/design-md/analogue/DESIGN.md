---
version: alpha
source: refero
source_id: 98ab0172-9474-43b5-9055-98cf1a6a2401
source_url: https://analogue.co
name: Analogue
description: "Analogue's design system evokes a sense of understated analog precision, mirroring the brand's focus on classic gaming hardware. It uses a strictly monochromatic grayscale palette with stark black backgrounds and white text, punctuated only by occasional product renders that introduce vivid color. Generous negative space and precise typography create an atmosphere of luxury and meticulous craftsmanship, while deeply rounded pill-shaped elements offer a subtle, almost mechanical softness."
theme: dark
northStar: "Matte black precision instrument. A single focused beam of light highlights intricate details against a deep, absorbing dark."
category: hardware
tags: ["dark-mode", "monochromatic", "high-contrast", "minimalist", "geometric", "precise", "product-focused", "arcade-inspired", "premium"]

colors:
  obsidian: "#000000"  # neutral — Page backgrounds, elevated surfaces, primary button background — the foundational darkness
  glacial-white: "#ffffff"  # neutral — Primary text color, button text, active states. Serves as a crisp counterpoint to Obsidian
  frost-gray: "#e5e7eb"  # neutral — Subtle surface accents, borders on interactive elements. Its near-white value allows for a
  steel-accent: "#bfbfbf"  # neutral — Secondary text in specific contexts, subtle dividers.
  faded-gray: "#999999"  # neutral — Tertiary text, less prominent headings. Offers reduced contrast for hierarchical distincti

typography:
  circularxx:
    family: "circularXx"
    sizes: "13px, 15px, 16px, 18px, 19px, 21px, 26px, 35px, 47px, 53px"
    weight: "400"
    lineHeight: "0.80, 1.00, 1.11, 1.14, 1.15, 1.20, 1.23, 1.50"
    letterSpacing: "-0.39, -0.45, -0.48, -0.54, -0.57, -0.63, -0.78"
    substitute: "Circular Std"
    use: "Body text, navigation, input fields, and smaller headings. The slightly condensed, geometric linearity at weight 400 with subtle letter-spacing creates a technical, precise voice."
  circularxx:
    family: "circularXx"
    sizes: "13px, 15px, 16px, 18px, 19px, 21px, 26px, 35px, 47px, 53px"
    weight: "450"
    lineHeight: "0.80, 1.00, 1.11, 1.14, 1.15, 1.20, 1.23, 1.50"
    letterSpacing: "-0.78, -1.05, -1.41, -1.59"
    substitute: "Circular Std"
    use: "Primary headings and display text. The medium weight with tight, negative letter-spacing for larger sizes gives display headlines a strong, impactful presence while retaining the technical precision."
  circularxx:
    family: "circularXx"
    sizes: "13px, 15px, 16px, 18px, 19px, 21px, 26px, 35px, 47px, 53px"
    weight: "500"
    lineHeight: "0.80, 1.00, 1.11, 1.14, 1.15, 1.20, 1.23, 1.50"
    letterSpacing: "-0.45, -0.54, -0.63, -0.78"
    substitute: "Circular Std"
    use: "Emphasized text, subheadings, and interactive elements where a slightly stronger voice than weight 400 is desired without resorting to bold. Maintains the precise character of the typeface."
---

# Analogue — Design System

> Matte black precision instrument. A single focused beam of light highlights intricate details against a deep, absorbing dark.


Analogue's design system evokes a sense of understated analog precision, mirroring the brand's focus on classic gaming hardware. It uses a strictly monochromatic grayscale palette with stark black backgrounds and white text, punctuated only by occasional product renders that introduce vivid color. Generous negative space and precise typography create an atmosphere of luxury and meticulous craftsmanship, while deeply rounded pill-shaped elements offer a subtle, almost mechanical softness.


## Type Scale

- role: body · size: 15 · lineHeight: 1.2 · letterSpacing: -0.45
- role: subheading · size: 18 · lineHeight: 1.15 · letterSpacing: -0.54
- role: heading · size: 26 · lineHeight: 1.14 · letterSpacing: -0.78
- role: heading-lg · size: 35 · lineHeight: 1.11 · letterSpacing: -1.05
- role: display · size: 53 · lineHeight: 0.8 · letterSpacing: -1.59

## Color Palette


### Neutral
- **Obsidian** `#000000` — Page backgrounds, elevated surfaces, primary button background — the foundational darkness that defines the brand's aesthetic. Provides an ideal canvas for product imagery.
- **Glacial White** `#ffffff` — Primary text color, button text, active states. Serves as a crisp counterpoint to Obsidian, ensuring legibility and drawing attention. Also used for reverse buttons.
- **Frost Gray** `#e5e7eb` — Subtle surface accents, borders on interactive elements. Its near-white value allows for a high contrast with Obsidian while being distinct from pure Glacial White.
- **Steel Accent** `#bfbfbf` — Secondary text in specific contexts, subtle dividers.
- **Faded Gray** `#999999` — Tertiary text, less prominent headings. Offers reduced contrast for hierarchical distinction.

## Layout

The site employs a full-bleed, dark background model that creates an immersive, cinematic feel. Content within sections appears largely horizontally centered, creating a focused presentation. The hero section often features large, centrally placed product photography against the full-bleed dark background with a concise, prominent headline. Sections are defined by generous vertical spacing (41-103px) and occasionally by alternating slight shifts in background color within the neutral palette, but without harsh dividers. Content arrangements vary from centered stacks of text and product images to horizontal grids for elements like review cards. The navigation is a minimalist sticky top bar with subtle Glacial White links on Obsidian.


## Imagery

The visual language focuses on high-fidelity product photography. Products are presented as hero elements, often in tight, studio-like crops, isolated against the deep Obsidian background. The treatment is consistently clean and precise, with products sometimes presented in a slight explosion or deconstructed view to showcase components or accessories (like game cartridges). There's no lifestyle photography, instead a direct, almost reverent focus on the hardware itself. Graphics are minimal, limited to subtle brand logos and UI elements. Icons are typically simple, monochromatic outlines or filled shapes that blend into the UI, serving functional roles rather than decorative ones.


## Spacing

- **radius**: {'cards': '17.6256px', 'buttons': '16777200px'}
- **elementGap**: 3-18px
- **sectionGap**: 41-103px
- **cardPadding**: 26px
- **pageMaxWidth**: None

## Do

- Use Obsidian (#000000) for all main page and card backgrounds to maintain the deep, dark aesthetic.
- Prioritize Glacial White (#ffffff) for primary text and calls to action against dark backgrounds to ensure high contrast and legibility.
- Apply `17.6256px` border radius to all card-like containers, and the maximum `16777200px` (or full pill shape) to buttons and tags.
- Employ circularXx (substitute Circular Std) with precise negative letter-spacing for all typography, specifically targeting `-0.0300em` for body text and tighter for headlines.
- Maintain generous vertical spacing between sections, using `41px` to `103px` as a base, to create visual breathing room and emphasize content blocks.
- Utilize Frost Gray (#e5e7eb) sparingly for borders and subtle element distinctions, reserving it for secondary contrast against Obsidian.
- Ensure all interactive text elements use Glacial White (#ffffff) at circularXx weight 400, size 15px, with subtle letter spacing adjustments.

## Don't

- Avoid using highly saturated or bright colors outside of product photography; the palette is strictly monochromatic.
- Do not use box-shadows for elevation; depth is created through background changes between Obsidian and Frost Gray, or product photography.
- Refrain from using square or lightly rounded corners for buttons or interactive tags; embrace the distinct `16777200px` pill radius.
- Do not vary line-height significantly for body text; aim for the `1.5` ratio for optimal reading comfort against the dark background.
- Avoid breaking compositional elements with hard lines or excessive borders; rely instead on spacing and background color shifts to define areas.
- Do not use generic system fonts; always implement circularXx (or Circular Std) to maintain the brand's precise and modern typographic identity.
- Never use `999999` (Faded Gray) or `bfbfbf` (Steel Accent) for critical text or primary actions, as their lower contrast is reserved for secondary information.

## Components


### CTA Block — Available Now
- **html**: <div style="--color-obsidian:#000000;--color-glacial-white:#ffffff;--color-frost-gray:#e5e7eb;--color-steel-accent:#bfbfbf;--color-faded-gray:#999999;--font-circularxx:'Circular Std',ui-rounded,'Helvetica Neue',Arial,sans-serif; background:var(--color-obsidian);padding:64px 24px;display:flex;flex-direction:column;align-items:center;justify-content:center;min-height:220px;box-sizing:border-box;width:600px;"><p style="font-family:var(--font-circularxx);font-size:15px;font-weight:400;color:var(--color-faded-gray);letter-spacing:-0.45px;line-height:1.2;margin:0 0 10px 0;text-align:center;">Analogue Pocket</p><h1 style="font-family:var(--font-circularxx);font-size:53px;font-weight:450;color:var(--color-glacial-white);letter-spacing:-1.59px;line-height:0.9;margin:0 0 40px 0;text-align:center;">Restock</h1><a href="#" style="display:inline-block;background:var(--color-glacial-white);color:var(--color-obsidian);font-family:var(--font-circularxx);font-size:15px;font-weight:400;letter-spacing:-0.45px;text-decoration:none;padding:11.75px 47px;border-radius:16777200px;border:1px solid var(--color-frost-gray);line-height:1.5;margin-bottom:14px;">Available Now</a><p style="font-family:var(--font-circularxx);font-size:15px;font-weight:400;color:var(--color-faded-gray);letter-spacing:-0.45px;line-height:1.2;margin:0;text-align:center;">Ships in June 2026</p></div>

### Review Cards — Analogue 3D Press
- **html**: <div style="--color-obsidian:#000000;--color-glacial-white:#ffffff;--color-frost-gray:#e5e7eb;--color-steel-accent:#bfbfbf;--color-faded-gray:#999999;--font-circularxx:'Circular Std',ui-rounded,'Helvetica Neue',Arial,sans-serif; background:var(--color-obsidian);padding:48px 20px;box-sizing:border-box;width:600px;"><h2 style="font-family:var(--font-circularxx);font-size:35px;font-weight:450;color:var(--color-glacial-white);letter-spacing:-1.05px;line-height:1.11;text-align:center;margin:0 0 36px 0;">Analogue<sup style="font-size:16px;vertical-align:super;letter-spacing:0;">3D</sup> Reviews</h2><div style="display:grid;grid-template-columns:1fr 1fr;gap:14px;"><div style="background:#111111;border:1px solid #222222;border-radius:17.6256px;padding:26px;box-sizing:border-box;display:flex;flex-direction:column;justify-content:space-between;min-height:200px;"><div style="display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:32px;"><span style="font-family:var(--font-circularxx);font-size:26px;font-weight:450;color:var(--color-glacial-white);letter-spacing:-0.78px;line-height:1;">5/5</span><span style="font-family:var(--font-circularxx);font-size:13px;font-weight:400;color:var(--color-steel-accent);letter-spacing:-0.39px;line-height:1;">gamesradar+</span></div><div><p style="font-family:var(--font-circularxx);font-size:14px;font-weight:400;color:var(--color-glacial-white);letter-spacing:-0.42px;line-height:1.4;margin:0 0 10px 0;">&ldquo;The Analogue<sup style="font-size:10px;">3D</sup> has solved my N64 woes, and it sets a new bar for retro console remakes&rdquo;</p><p style="font-family:var(--font-circularxx);font-size:13px;font-weight:400;color:var(--color-faded-gray);letter-spacing:-0.39px;line-height:1.2;margin:0;">- Gamesradar</p></div></div><div style="background:#111111;border:1px solid #222222;border-radius:17.6256px;padding:26px;box-sizing:border-box;display:flex;flex-direction:column;justify-content:space-between;min-height:200px;"><div style="display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:32px;"><span style="font-family:var(--font-circularxx);font-size:26px;font-weight:450;color:var(--color-glacial-white);letter-spacing:-0.78px;line-height:1;">4.5/5</span><span style="font-family:var(--font-circularxx);font-size:13px;font-weight:400;color:var(--color-steel-accent);letter-spacing:-0.39px;line-height:1;">PC Mag</span></div><div><p style="font-family:var(--font-circularxx);font-size:14px;font-weight:400;color:var(--color-glacial-white);letter-spacing:-0.42px;line-height:1.4;margin:0 0 10px 0;">&ldquo;Editors Choice Award&rdquo;</p><p style="font-family:var(--font-circularxx);font-size:13px;font-weight:400;color:var(--color-faded-gray);letter-spacing:-0.39px;line-height:1.2;margin:0;">- PC Mag</p></div></div><div style="background:#111111;border:1px solid #222222;border-radius:17.6256px;padding:26px;box-sizing:border-box;display:flex;flex-direction:column;justify-content:space-between;min-height:200px;"><div style="display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:32px;"><span style="font-family:var(--font-circularxx);font-size:26px;font-weight:450;color:var(--color-glacial-white);letter-spacing:-0.78px;line-height:1;">9/10</span><span style="font-family:var(--font-circularxx);font-size:13px;font-weight:400;color:var(--color-steel-accent);letter-spacing:-0.39px;line-height:1;">WIRED</span></div><div><p style="font-family:var(--font-circularxx);font-size:14px;font-weight:400;color:var(--color-glacial-white);letter-spacing:-0.42px;line-height:1.4;margin:0 0 10px 0;">&ldquo;This is the best way to play classic N64 games in 2025&rdquo;</p><p style="font-family:var(--font-circularxx);font-size:13px;font-weight:400;color:var(--color-faded-gray);letter-spacing:-0.39px;line-height:1.2;margin:0;">- Wired</p></div></div><div style="background:#111111;border:1px solid #222222;border-radius:17.6256px;padding:26px;box-sizing:border-box;display:flex;flex-direction:column;justify-content:space-between;min-height:200px;"><div style="display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:32px;"><span style="font-family:var(--font-circularxx);font-size:26px;font-weight:450;color:var(--color-glacial-white);letter-spacing:-0.78px;line-height:1;">8.5/10</span><span style="font-family:var(--font-circularxx);font-size:13px;font-weight:400;color:var(--color-steel-accent);letter-spacing:-0.39px;line-height:1;">CNET</span></div><div><p style="font-family:var(--font-circularxx);font-size:14px;font-weight:400;color:var(--color-glacial-white);letter-spacing:-0.42px;line-height:1.4;margin:0 0 10px 0;">&ldquo;The Purest Nintendo 64 Experience You Can Have on a 4K TV&rdquo;</p><p style="font-family:var(--font-circularxx);font-size:13px;font-weight:400;color:var(--color-faded-gray);letter-spacing:-0.39px;line-height:1.2;margin:0;">- CNET</p></div></div></div></div>

### Product Section Header — Analogue 3D Shipping Now
- **html**: <div style="--color-obsidian:#000000;--color-glacial-white:#ffffff;--color-frost-gray:#e5e7eb;--color-steel-accent:#bfbfbf;--color-faded-gray:#999999;--font-circularxx:'Circular Std',ui-rounded,'Helvetica Neue',Arial,sans-serif; background:#f0f0f0;padding:64px 24px 48px;box-sizing:border-box;width:600px;display:flex;flex-direction:column;align-items:center;"><p style="font-family:var(--font-circularxx);font-size:15px;font-weight:400;color:#555555;letter-spacing:-0.45px;line-height:1.2;margin:0 0 8px 0;text-align:center;">Analogue<sup style="font-size:10px;vertical-align:super;">3D</sup></p><h2 style="font-family:var(--font-circularxx);font-size:47px;font-weight:450;color:var(--color-obsidian);letter-spacing:-1.41px;line-height:1.0;margin:0 0 40px 0;text-align:center;">Shipping Now</h2><div style="width:100%;background:#d8d8d8;border-radius:17.6256px;height:280px;display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden;"><div style="width:220px;height:80px;background:#1a1a1a;border-radius:14px;position:relative;display:flex;align-items:center;justify-content:center;"><div style="width:180px;height:60px;background:#2a2a2a;border-radius:10px;display:flex;align-items:flex-end;justify-content:center;padding-bottom:8px;box-sizing:border-box;"><div style="display:flex;gap:14px;"><div style="width:18px;height:18px;background:#111;border-radius:50%;border:2px solid #333;"></div><div style="width:18px;height:18px;background:#111;border-radius:50%;border:2px solid #333;"></div><div style="width:18px;height:18px;background:#111;border-radius:50%;border:2px solid #333;"></div><div style="width:18px;height:18px;background:#111;border-radius:50%;border:2px solid #333;"></div></div></div></div><p style="position:absolute;bottom:18px;left:50%;transform:translateX(-50%);font-family:var(--font-circularxx);font-size:13px;font-weight:400;color:#888888;letter-spacing:-0.39px;white-space:nowrap;">Analogue 3D Console</p></div><div style="margin-top:32px;display:flex;gap:14px;"><a href="#" style="display:inline-block;background:var(--color-obsidian);color:var(--color-glacial-white);font-family:var(--font-circularxx);font-size:15px;font-weight:400;letter-spacing:-0.45px;text-decoration:none;padding:11.75px 47px;border-radius:16777200px;border:1px solid #333333;line-height:1.5;">Shop Now</a><a href="#" style="display:inline-block;background:transparent;color:var(--color-obsidian);font-family:var(--font-circularxx);font-size:15px;font-weight:400;letter-spacing:-0.45px;text-decoration:none;padding:11.75px 47px;border-radius:16777200px;border:1px solid #aaaaaa;line-height:1.5;">Learn More</a></div></div>

### Primary Button
- **role**: Calls to action
- **description**: White background with Obsidian text. Displays a distinctive super-elliptical 'pill' shape. Padding: 11.75px vertical, 47px horizontal. Typography: circularXx, weight 400, size 15px. Border color: Frost Gray.

### Secondary Button
- **role**: Calls to action (dark mode)
- **description**: Obsidian background with Glacial White text. Displays a distinctive super-elliptical 'pill' shape. Padding: 11.75px vertical, 47px horizontal. Typography: circularXx, weight 400, size 15px. Border color: Frost Gray.

### Text Link Button
- **role**: Tertiary action with embedded icon
- **description**: Transparent background with Glacial White text. No padding, no border radius, effectively a text link with button functionality. Typography: circularXx, weight 400, size 15px.

### Header Navigation Item
- **role**: Main site navigation
- **description**: Glacial White text against Obsidian background, typography circularXx weight 400, size 15px. No discernible padding or special states for the items themselves beyond active link color changes.

### Footer Navigation Item
- **role**: Secondary site navigation
- **description**: Glacial White text against Obsidian background, typography circularXx weight 400, size 15px. Appears in columnar lists within the footer.

### Pill Tag
- **role**: Status indicators or labels
- **description**: Examples like 'Available Now' are primary buttons. While no explicit tag component provided, the radical `16777200px` border radius for buttons suggests a consistent 'pill' shape for any small, contained information block would be idiomatic to the design system.

## Agent Prompt Guide

### Quick Color Reference
- Text: #ffffff (Glacial White)
- Background: #000000 (Obsidian)
- CTA Primary: #ffffff (Glacial White)
- CTA Secondary: #000000 (Obsidian)
- Border/Accent: #e5e7eb (Frost Gray)

### Example Component Prompts
1. Create a hero section: Obsidian background. Centered headline 'Restock' at 53px circularXx weight 450, #ffffff, letter-spacing -1.59px, line-height 0.8. Below it, a Primary Button: #ffffff background, #000000 text, 16777200px radius, 11.75px vertical padding, 47px horizontal padding, circularXx weight 400, size 15px. 
2. Create a review card: Background #000000, 17.6256px border-radius, 26px padding. Text '5/5' in #ffffff circularXx weight 450 size 26px, line-height 1.14, letter-spacing -0.78px. Below it, a quote 'The Analogue 3D has solved my N64 woes...' in #ffffff circularXx weight 400 size 15px.
3. Design a dark-themed footer: Obsidian background. Glacial White #ffffff text for links, circularXx weight 400, size 15px, letter-spacing -0.45px. Layout links in columns with a 6px element gap.
4. Create a product feature section: Obsidian background, headline 'Analogue 3D Shipping Now' at 47px circularXx weight 450, #ffffff, letter-spacing -1.41px. Center-align the content. Below it, a Secondary Button: #000000 background, #ffffff text, 16777200px radius, 11.75px vertical padding, 47px horizontal padding, circularXx weight 400, size 15px.
