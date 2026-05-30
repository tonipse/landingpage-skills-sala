---
version: alpha
source: refero
source_id: 131d07b0-f71b-4bd2-8046-f61485ed545c
source_url: https://locomotive.ca
name: Locomotive
description: "This system projects an aura of intellectual rigor and understated luxury, using stark achromatic contrasts and precise typography. The visual mood is serious and art-directed, prioritizing content and a sense of curated exclusivity over overt flair. The absence of traditional buttons, shadows, or rounded corners emphasizes a flat, print-like aesthetic where content is king and interactive elements are subtly integrated into the typographic flow."
theme: light
northStar: "monochrome editorial manifesto \u2013 where stark blocks of content meet fluid, almost invisible interactions."
category: agency
tags: ["minimalist", "editorial", "monochrome", "typographic", "text-heavy", "stark", "art-directed", "flat", "structured", "magazine-like"]

colors:
  pitch-black: "#000000"  # neutral — Primary text, borders, dividers, dark mode backgrounds for specific elements, icon fills.
  canvas-white: "#ffffff"  # neutral — Page backgrounds, card backgrounds, primary surface areas, navigation text in inverted con

typography:
  helveticanowdisplay:
    family: "HelveticaNowDisplay"
    sizes: "15px, 26px"
    weight: "400"
    lineHeight: "1.00, 1.20, 1.30"
    letterSpacing: "normal"
    substitute: "system-ui"
    use: "Body copy (15px), general links, navigation items, descriptive text, and some smaller headings. Its neutrality provides a stable foundation for the more expressive LocomotiveNew."
  locomotivenew:
    family: "LocomotiveNew"
    sizes: "70px, 110px"
    weight: "400"
    lineHeight: "1.00, 1.10"
    letterSpacing: "normal"
    substitute: "Georgia"
    use: "Display headings (70px, 110px). This custom serif font adds a distinctive editorial and somewhat artistic touch, providing gravitas and a unique brand voice at larger sizes, breaking from the Helvetic"
---

# Locomotive — Design System

> monochrome editorial manifesto – where stark blocks of content meet fluid, almost invisible interactions.


This system projects an aura of intellectual rigor and understated luxury, using stark achromatic contrasts and precise typography. The visual mood is serious and art-directed, prioritizing content and a sense of curated exclusivity over overt flair. The absence of traditional buttons, shadows, or rounded corners emphasizes a flat, print-like aesthetic where content is king and interactive elements are subtly integrated into the typographic flow.


## Color Palette


### Neutral
- **Pitch Black** `#000000` — Primary text, borders, dividers, dark mode backgrounds for specific elements, icon fills.
- **Canvas White** `#ffffff` — Page backgrounds, card backgrounds, primary surface areas, navigation text in inverted contexts.

## Layout

The page primarily employs a max-width contained model for most content, implicitly centered. The hero section, however, is full-bleed, using a dramatic background image with centered, large typographic headlines. A strong vertical rhythm is established by generous section gaps (150px). Content is often arranged in large textual blocks or two-column layouts where text is juxtaposed with either negative space or a precisely placed image. Navigation is a simple top bar with a 'Let's talk' link, alongside a minimal footer. The site is text-dominant with key visuals dropped in strategically, giving a very spacious, almost sparse, feel.


## Imagery

The visual language is impactful and sparse. Hero sections feature high-contrast, moody photography with dramatic lighting and often a single muted color cast (e.g., the red-tinted image in the hero). Subsequent sections are text-heavy, with product/object photography (like the ring image) presented as isolated, high-fidelity crops on a black background, emphasizing the object's detail. Visuals are treated as art pieces within the layout, full-bleed at the top, or precisely contained for product showcases, never overlapping or masked with soft edges. Icons are kept to a minimum, likely outlined mono-color for navigational accents. The density is heavily text-dominant, with images serving as focal points rather than decorative elements.


## Spacing

- **radius**: {'all': '0px'}
- **elementGap**: 
- **sectionGap**: 150px
- **cardPadding**: 0px
- **pageMaxWidth**: None

## Do

- Prioritize text content by using HelveticaNowDisplay 400 for all functional text at 15px.
- Use LocomotiveNew 400 at 70px or 110px exclusively for prominent display headings, creating a strong editorial presence.
- Maintain an achromatic palette using only Pitch Black (#000000) and Canvas White (#ffffff) for all UI elements and text.
- Separate major content sections using a generous vertical padding of 150px, establishing a spacious layout.
- Design all interactive elements as text-based, without explicit button containers, borders, or background fills, relying solely on hover states and cursor changes for affordance.

## Don't

- Do not introduce any color other than Pitch Black (#000000) and Canvas White (#ffffff) into the primary UI.
- Avoid using box-shadows or any form of elevation for UI elements; maintain a flat, print-like aesthetic.
- Do not use border-radius; all corners should be sharp and 0px.
- Do not deviate from the specified font families; avoid system fonts or other custom typefaces.
- Never add explicit padding or background colors to buttons; let them exist purely as interactive text.

## Components


### Article List
- **html**: <div style="--color-pitch-black:#000000;--color-canvas-white:#ffffff;--font-helveticanowdisplay:system-ui,sans-serif;--font-locomotivenew:Georgia,serif;width:600px;background:var(--color-canvas-white);font-family:var(--font-helveticanowdisplay);padding:40px 0;box-sizing:border-box;"><div style="border-top:1px solid var(--color-pitch-black);display:grid;grid-template-columns:180px 1fr;"><div style="padding:20px 0 0 0;"><span style="font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);line-height:1.3;">Articles</span></div><div><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">Locomotive x Lightship : Innovation Needs a Companion</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">Locomotive x Chivalry: How We Became More Than Just Collaborators</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">Should I use Locomotive Scroll on my project?</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">Why don't we use front-end frameworks at Locomotive?</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">The revolution of the workspace as we know it</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">A few things your UX designer can learn from your shrink</a></div></div><div style="border-top:1px solid var(--color-pitch-black);display:grid;grid-template-columns:180px 1fr;margin-top:0;"><div style="padding:20px 0 0 0;"><span style="font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);line-height:1.3;">Culture</span></div><div><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">(2024) Locomotive in Jamaica</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">(2023) Locomotive in Samaná</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">(2022) Locomotive in Playa del Carmen</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">(2019) Locomotive in Mexico</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">(2018) Locomotive in Jamaica</a><a href="#" style="display:block;padding:14px 0;border-bottom:1px solid var(--color-pitch-black);font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">(2017) Locomotive in Samaná</a></div></div><div style="border-top:1px solid var(--color-pitch-black);border-bottom:1px solid var(--color-pitch-black);display:grid;grid-template-columns:180px 1fr;margin-top:0;"><div style="padding:20px 0;"><span style="font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);line-height:1.3;">Store</span></div><div style="display:flex;align-items:flex-start;padding:20px 0;"><a href="#" style="font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">Check out our gear</a></div></div></div>

### Work Card — Seven Years
- **html**: <div style="--color-pitch-black:#000000;--color-canvas-white:#ffffff;--font-helveticanowdisplay:system-ui,sans-serif;--font-locomotivenew:Georgia,serif;width:600px;background:var(--color-canvas-white);padding:40px;box-sizing:border-box;font-family:var(--font-helveticanowdisplay);"><div style="font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);margin-bottom:8px;line-height:1.3;">Seven Years</div><div style="display:grid;grid-template-columns:1fr 180px;gap:0;"><div style="background:var(--color-pitch-black);width:100%;height:360px;display:flex;align-items:center;justify-content:center;"><div style="width:130px;height:130px;border-radius:50%;background:linear-gradient(135deg,#c8a84b 0%,#8b6914 40%,#e8c96a 60%,#a07830 100%);box-shadow:inset -10px -10px 20px rgba(0,0,0,0.6),inset 4px 4px 10px rgba(255,220,100,0.3);position:relative;"><div style="position:absolute;top:18px;left:50%;transform:translateX(-50%);width:50px;height:50px;border-radius:50%;background:radial-gradient(circle at 35% 30%,rgba(255,255,255,0.8) 0%,rgba(200,230,255,0.4) 40%,rgba(100,150,200,0.1) 100%);border:3px solid rgba(200,170,80,0.8);"></div></div></div><div style="padding-left:32px;display:flex;flex-direction:column;justify-content:space-between;"><div style="font-family:var(--font-locomotivenew);font-size:26px;font-weight:400;color:var(--color-pitch-black);line-height:1.1;writing-mode:vertical-rl;transform:rotate(180deg);align-self:flex-start;margin-top:0;">Running</div><div><div style="font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);line-height:1.3;margin-bottom:24px;">2018–2024</div><div style="border-top:1px solid var(--color-pitch-black);padding-top:16px;display:flex;justify-content:space-between;align-items:center;"><a href="#" style="font-family:var(--font-helveticanowdisplay);font-size:15px;font-weight:400;color:var(--color-pitch-black);text-decoration:none;line-height:1.3;">The dynasty</a><span style="font-size:15px;color:var(--color-pitch-black);">→</span></div></div></div></div></div>

### Hero Brand Badge
- **html**: <div style="--color-pitch-black:#000000;--color-canvas-white:#ffffff;--font-helveticanowdisplay:system-ui,sans-serif;--font-locomotivenew:Georgia,serif;width:600px;background:#cc1100;padding:48px 40px 48px 40px;box-sizing:border-box;display:flex;flex-direction:column;justify-content:flex-end;min-height:320px;position:relative;"><div style="position:absolute;top:0;left:0;right:0;bottom:0;background:rgba(0,0,0,0.18);"></div><div style="position:relative;z-index:1;"><div style="display:flex;align-items:center;gap:12px;margin-bottom:12px;"><div style="border:1.5px solid #4dd4e8;padding:4px 8px;display:inline-flex;align-items:center;gap:0;"><span style="font-family:var(--font-helveticanowdisplay);font-size:11px;font-weight:400;color:#4dd4e8;letter-spacing:0.03em;line-height:1;">OPS</span><span style="display:inline-block;width:1.5px;height:22px;background:#4dd4e8;margin:0 6px;"></span><div style="display:flex;flex-direction:column;"><span style="font-family:var(--font-helveticanowdisplay);font-size:11px;font-weight:400;color:#4dd4e8;letter-spacing:0.03em;line-height:1;">DES</span><span style="font-family:var(--font-helveticanowdisplay);font-size:11px;font-weight:400;color:#4dd4e8;letter-spacing:0.03em;line-height:1;">DEV</span></div></div><span style="font-family:var(--font-helveticanowdisplay);font-size:22px;font-weight:400;color:#4dd4e8;line-height:1;">Locomotive<sup style="font-size:12px;">®</sup></span></div><div style="display:flex;flex-wrap:wrap;align-items:baseline;gap:0;"><span style="font-family:var(--font-locomotivenew);font-size:52px;font-weight:400;color:#4dd4e8;line-height:1;font-style:italic;">Digital-first</span><span style="font-family:var(--font-locomotivenew);font-size:52px;font-weight:400;color:#4dd4e8;line-height:1;">&nbsp;Design Agency</span><span style="font-family:var(--font-helveticanowdisplay);font-size:36px;font-weight:400;color:#4dd4e8;line-height:1;margin-left:6px;">✳</span><div style="display:inline-flex;align-items:center;margin-left:6px;border-bottom:2px solid #4dd4e8;"><span style="font-family:var(--font-helveticanowdisplay);font-size:13px;font-weight:400;color:#4dd4e8;letter-spacing:0.08em;text-transform:uppercase;padding-bottom:2px;">loco</span></div></div></div></div>

### Navigation Link
- **role**: Interactive text link
- **description**: Appears as plain black text (HelveticaNowDisplay, 400) on a white background. No explicit padding or border, relying on typographic spacing. Interaction implied by context and cursor change, not visual styling.

### Ghost Button
- **role**: Call to action with minimal visual footprint
- **description**: Rendered as text (color: #000000, background: rgba(0, 0, 0, 0)). Features no border, padding, or border-radius, presenting as a clickable typographic element rather than a traditional button shape.

### Text-Only Card
- **role**: Content container for articles or items
- **description**: Completely borderless and shadow-free with rgba(0, 0, 0, 0) background and 0px border-radius. Content stands on its own, flush against the background, emphasizing an editorial layout over distinct UI segmentation.

### Section Divider
- **role**: Visual separation between content blocks
- **description**: A thin horizontal line (implicitly Pitch Black) used to segment content areas, particularly visible in the articles/culture/store listing. Emphasizes structure without visual bulk.

### Headline Section
- **role**: Prominent page titles or section headers
- **description**: Utilizes LocomotiveNew at large sizes (70px or 110px) with Pitch Black text on a Canvas White background. Offers generous vertical padding (150px) above and below, providing significant whitespace.

### Article List Item
- **role**: Entry in a textual list of content
- **description**: HelveticaNowDisplay, 400, Pitch Black text. Each item is typically underlined or bordered lightly (implicitly Pitch Black) and separated by minimal vertical spacing (e.g. 7px padding) to maintain density.

## Agent Prompt Guide

### Quick Color Reference
- Text: #000000 (Pitch Black)
- Background: #ffffff (Canvas White)
- Accent: None (achromatic only)
- Border: #000000 (Pitch Black)
- Interactive Text: #000000 (Pitch Black)

### Example Component Prompts
1. Create a hero section: full-bleed background, centered headline using LocomotiveNew 400, 110px, Pitch Black text. Below it, a line of supporting text using HelveticaNowDisplay 400, 26px, Pitch Black. Max available vertical space between elements as per 150px section gap for surrounding elements.
2. Design a navigation link: Text 'Work' using HelveticaNowDisplay 400, 15px, Pitch Black. No background, no border, no padding. Ensure it is functionally clickable.
3. Build an article list item: Text 'Locomotive x Lightship : Innovation Needs a Companion' using HelveticaNowDisplay 400, 15px, Pitch Black. Include an implied 7px vertical padding for proper line spacing. This item should not have visible borders or background, relying on its text for presence, but able to act as a clickable unit.
4. Produce a section divider: A simple horizontal line, 0px border-radius, Pitch Black, appearing subtly between content blocks like those in the 'Articles' and 'Culture' sections.
5. Create a large display title for a section like 'Featured work': Using LocomotiveNew 400, 70px, Pitch Black text. Ensure it is surrounded by 150px vertical spacing.
