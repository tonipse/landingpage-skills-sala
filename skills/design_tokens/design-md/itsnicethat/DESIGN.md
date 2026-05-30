---
version: alpha
source: refero
source_id: 3e70af05-a07f-4c11-98ca-6ecb4765e967
source_url: https://itsnicethat.com
name: Itsnicethat
description: "This design system feels like a carefully curated art zine, balancing disciplined, editorial typography with unexpected splashes of vivid, almost childlike color. The overall impression is one of approachable creativity and intellectual curiosity. Sharp corners dominate the UI, making the few instances of extreme roundedness (75px) feel like deliberate, playful exceptions. This tension between strict layout and spontaneous color creates a dynamic, engaging experience."
theme: light
northStar: "Artist's sketchbook, bursting with vibrant scraps and precise typography."
category: editorial
tags: ["editorial", "art", "colorful", "sharp-corners", "typographic", "vibrant-accents", "eclectic", "magazine-like", "creative", "design-focused"]

colors:
  black-ink: "#2b2b2b"  # neutral — Primary text, main headings, icons, borders – creates a sharp, authoritative presence agai
  pure-white: "#ffffff"  # neutral — Page backgrounds, card surfaces, button text – the dominant canvas for content.
  frost-gray: "#f0efef"  # neutral — Subtle background for badges and secondary elements, offering a softer lift than Pure Whit
  medium-gray: "#676767"  # neutral — Secondary text, less prominent borders and icons, receding slightly from Black Ink.
  muted-taupe: "#faead9"  # neutral — Background for specific content blocks, providing a warm, subtle shift.
  electric-purple: "#8147ff"  # brand — Primary brand accent, used for prominent interactive elements like call-to-action buttons 
  sunshine-yellow: "#ffd519"  # accent — Secondary accent for interactive elements and highlighted content – adds a warm, optimisti
  deep-indigo: "#6219ff"  # accent — Prominent links, suggesting interactivity - a slightly darker, more saturated version of E
  risograph-gradient: "#ffffff"  # neutral — Subtle background gradient for specific sections, adding a textural feel.

typography:
  bradford:
    family: "Bradford"
    sizes: "11px, 15px, 17px"
    weight: "400, 500"
    lineHeight: "1.15, 1.47, 1.53, 2.27"
    letterSpacing: "-0.005em at 11px, 0.008em at 15px, 0.027em at 17px"
    substitute: "Georgia"
    use: "Body text, article content, component labels — its slightly condensed, serif form reinforces the editorial, artistic feel, making long-form content engaging."
  labilvariable:
    family: "LabilVariable"
    sizes: "11px, 13px, 15px, 18px, 25px, 40px"
    weight: "400"
    lineHeight: "1.20, 1.28, 1.40, 1.45, 1.46, 1.73"
    letterSpacing: "0.025em at 11px, 0.032em at 13px, 0.056em at 15px, 0.067em at 18px, 0.077em at 25px, 0.091em at 40px"
    substitute: "Open Sans"
    use: "Prominent headings, titles, and key UI elements — its variable nature and wider letter spacing provides a distinct, modern counterbalance to Bradford's classic feel, adding visual breathing room to la"
  labil:
    family: "Labil"
    sizes: "11px, 13px, 17px"
    weight: "400, 500"
    lineHeight: "1.40, 1.45, 1.47"
    letterSpacing: "0.005em at 11px, 0.091em at 13px"
    substitute: "Open Sans"
    use: "Secondary headings, metadata, and smaller UI labels — a more compact, structured sans-serif that aids readability in informational contexts."
---

# Itsnicethat — Design System

> Artist's sketchbook, bursting with vibrant scraps and precise typography.


This design system feels like a carefully curated art zine, balancing disciplined, editorial typography with unexpected splashes of vivid, almost childlike color. The overall impression is one of approachable creativity and intellectual curiosity. Sharp corners dominate the UI, making the few instances of extreme roundedness (75px) feel like deliberate, playful exceptions. This tension between strict layout and spontaneous color creates a dynamic, engaging experience.


## Type Scale

- role: caption · size: 11 · lineHeight: 1.4 · letterSpacing: 0.005
- role: body · size: 15 · lineHeight: 1.47 · letterSpacing: 0.008
- role: heading · size: 25 · lineHeight: 1.46 · letterSpacing: 0.077
- role: display · size: 40 · lineHeight: 1.73 · letterSpacing: 0.091

## Color Palette


### Neutral
- **Black Ink** `#2b2b2b` — Primary text, main headings, icons, borders – creates a sharp, authoritative presence against the light background.
- **Pure White** `#ffffff` — Page backgrounds, card surfaces, button text – the dominant canvas for content.
- **Frost Gray** `#f0efef` — Subtle background for badges and secondary elements, offering a softer lift than Pure White.
- **Medium Gray** `#676767` — Secondary text, less prominent borders and icons, receding slightly from Black Ink.
- **Muted Taupe** `#faead9` — Background for specific content blocks, providing a warm, subtle shift.
- **Risograph Gradient** `#ffffff` — Subtle background gradient for specific sections, adding a textural feel.

### Brand
- **Electric Purple** `#8147ff` — Primary brand accent, used for prominent interactive elements like call-to-action buttons – vibrant and energetic.

### Accent
- **Sunshine Yellow** `#ffd519` — Secondary accent for interactive elements and highlighted content – adds a warm, optimistic pop.
- **Deep Indigo** `#6219ff` — Prominent links, suggesting interactivity - a slightly darker, more saturated version of Electric Purple.

## Layout

The page adheres to a max-width, center-aligned model of 1200px, providing structured content presentation. The hero section often features a large headline centered over a background or a split layout with prominent text. Content sections maintain a consistent vertical rhythm, with generous section spacing of 40px. The main content flows in a series of stacked, full-width blocks, often alternating between text-dominant sections and grid-like arrangements of images/cards. Feature sections frequently exhibit a three-column grid for articles. Navigation is a combination of a fixed top bar and a floating pill-shaped menu at the bottom, offering both persistent and contextual navigation.


## Imagery

The site primarily uses diverse, high-quality photography and static illustrations to showcase creative work. Imagery is mostly contained within distinct blocks, without significant masks or overlaps, maintaining a structured presentation. Photographs are often bright and product-focused, displaying artworks or designs clearly. Illustrations are varied in style, ranging from whimsical and organic to geometric and flat, always serving to represent artistic content. There's a high density of imagery, particularly within content listings, making the site visually rich and appealing to a creative audience. Icons are minimal, subtle, and outline-based, mostly functional.


## Spacing

- **radius**: {'buttons': '75px', 'default': '0px'}
- **elementGap**: 10px
- **sectionGap**: 40px
- **cardPadding**: 0px
- **pageMaxWidth**: 1200px

## Do

- Use Electric Purple (#8147ff) for primary interactive elements to ensure visual magnetism.
- Maintain 0px border-radius for all structural elements and standard buttons to reinforce the sharp, editorial aesthetic.
- Employ a 75px border-radius exclusively for navigation pill buttons to highlight their distinctive interactive role.
- Utilize LabilVariable font at larger sizes for headlines, coupled with its generous letter spacing (e.g., 0.091em at 40px), to create impactful, breathable titles.
- Integrate the Muted Taupe (#faead9) background for selected content sections to provide subtle visual differentiation and warmth.
- Leverage the Bradford font for body text and descriptive elements, ensuring readability and an editorial tone.
- Apply 10px element gap as a default for horizontal and vertical spacing between most inline content elements.

## Don't

- Avoid using shadows for elevation; rely on color and spacing hierarchy instead.
- Do not deviate from the 0px border-radius for anything other than specific navigation pill buttons.
- Refrain from using highly saturated colors for large background areas or extensive text blocks; reserve them for accents.
- Do not introduce additional font families; the current mix of Bradford, LabilVariable, and Labil is deliberate.
- Avoid generic 'modern' or 'sleek' visual tropes; the system's character is in its eclectic editorial feel.
- Do not introduce gradients unless they mirror the subtle 'Risograph Gradient' pattern; avoid complex, multi-stop gradients.

## Components


### The Nice Feed — Article Feed Strip
- **html**: <div style="--color-black-ink:#2b2b2b;--color-pure-white:#ffffff;--color-frost-gray:#f0efef;--color-medium-gray:#676767;--color-muted-taupe:#faead9;--color-electric-purple:#8147ff;--color-sunshine-yellow:#ffd519;--font-bradford:Georgia,serif;--font-labilvariable:'Open Sans',sans-serif;--font-labil:'Open Sans',sans-serif; box-sizing:border-box; width:600px; background:var(--color-pure-white); border:1px solid #e0e0e0; font-family:var(--font-bradford);"> <div style="display:flex; align-items:center; justify-content:space-between; padding:12px 16px; border-bottom:1px solid var(--color-black-ink);"> <div style="display:flex; align-items:center; gap:12px;"> <span style="font-family:var(--font-labilvariable); font-size:13px; font-weight:400; letter-spacing:0.032em; color:var(--color-black-ink);">The Nice Feed</span> <span style="font-family:var(--font-bradford); font-size:11px; color:var(--color-medium-gray); letter-spacing:0.005em;">Refreshed 23h ago</span> </div> <a href="#" style="display:flex; align-items:center; gap:6px; font-family:var(--font-labilvariable); font-size:13px; letter-spacing:0.032em; color:var(--color-black-ink); text-decoration:none;">Explore All <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="16" height="16" rx="0" fill="var(--color-black-ink)"/><path d="M5 8h6M8 5l3 3-3 3" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></a> </div> <div style="display:grid; grid-template-columns:1fr 1fr 1fr; border-top:none;"> <div style="display:flex; flex-direction:column; border-right:1px solid #e8e8e8; padding:0;"> <div style="width:100%; height:110px; background:#7a6fa0; overflow:hidden;"><div style="width:100%;height:100%;background:linear-gradient(135deg,#5a3e8a 0%,#8a6aad 100%); display:flex; align-items:center; justify-content:center;"><span style="color:white;font-family:var(--font-labilvariable);font-size:10px;letter-spacing:0.05em;text-align:center;padding:8px;">NICER TUESDAYS</span></div></div> <div style="padding:10px 12px; flex:1;"> <p style="margin:0 0 8px 0; font-family:var(--font-bradford); font-size:14px; line-height:1.4; color:var(--color-black-ink); font-weight:400;">Get tickets for April's Nicer Tuesdays in LA!</p> <div style="display:flex; justify-content:space-between; align-items:center;"> <span style="font-family:var(--font-labil); font-size:11px; color:var(--color-medium-gray); letter-spacing:0.005em;">It's Nice That</span> <span style="font-family:var(--font-labil); font-size:11px; color:var(--color-medium-gray);">23h</span> </div> </div> </div> <div style="display:flex; flex-direction:column; border-right:1px solid #e8e8e8;"> <div style="width:100%; height:110px; background:#1a1a2e; overflow:hidden;"><div style="width:100%;height:100%;background:linear-gradient(135deg,#1a1a2e 0%,#2d2d4e 100%); display:flex; align-items:center; justify-content:center;"><span style="color:#e0c070;font-family:var(--font-labilvariable);font-size:9px;letter-spacing:0.04em;text-align:center;padding:8px;">I WAS HIRED BY HBO</span></div></div> <div style="padding:10px 12px; flex:1;"> <p style="margin:0 0 8px 0; font-family:var(--font-bradford); font-size:14px; line-height:1.4; color:var(--color-black-ink);">Heated Rivalry fan-editor on landing HBO job</p> <div style="display:flex; justify-content:space-between; align-items:center;"> <span style="font-family:var(--font-labil); font-size:11px; color:var(--color-medium-gray);">Impact</span> <span style="font-family:var(--font-labil); font-size:11px; color:var(--color-medium-gray);">1d</span> </div> </div> </div> <div style="display:flex; flex-direction:column;"> <div style="width:100%; height:110px; background:#d4c9b0; overflow:hidden;"><div style="width:100%;height:100%;background:linear-gradient(135deg,#c8bca0 0%,#e0d4b8 100%); display:flex; align-items:center; justify-content:center;"><span style="color:#3a3020;font-family:var(--font-labilvariable);font-size:8px;letter-spacing:0.04em;text-align:center;padding:8px;">ICELANDAIR CAMPAIGN</span></div></div> <div style="padding:10px 12px; flex:1;"> <p style="margin:0 0 8px 0; font-family:var(--font-bradford); font-size:14px; line-height:1.4; color:var(--color-black-ink);">Icelandair is looking for a really, really bad photographer</p> <div style="display:flex; justify-content:space-between; align-items:center;"> <span style="font-family:var(--font-labil); font-size:11px; color:var(--color-medium-gray);">Famous Campaigns</span> <span style="font-family:var(--font-labil); font-size:11px; color:var(--color-medium-gray);">1d</span> </div> </div> </div> </div> </div>

### Article Card with Tags
- **html**: <div style="--color-black-ink:#2b2b2b;--color-pure-white:#ffffff;--color-frost-gray:#f0efef;--color-medium-gray:#676767;--color-muted-taupe:#faead9;--color-electric-purple:#8147ff;--color-sunshine-yellow:#ffd519;--font-bradford:Georgia,serif;--font-labilvariable:'Open Sans',sans-serif;--font-labil:'Open Sans',sans-serif; box-sizing:border-box; width:600px; background:var(--color-pure-white); padding:0; font-family:var(--font-bradford);"> <div style="width:100%; height:320px; background:linear-gradient(135deg,#7c5cbf 0%,#4a90d9 50%,#6b8c3a 100%); position:relative; overflow:hidden;"> <div style="position:absolute; inset:0; display:grid; grid-template-columns:1fr 1fr 1fr; gap:0;"> <div style="background:#7c5cbf; display:flex; align-items:center; justify-content:center;"><div style="width:120px;height:160px;background:rgba(255,255,255,0.12);border-radius:2px;"></div></div> <div style="background:#4a90d9; display:flex; align-items:center; justify-content:center;"><div style="width:120px;height:160px;background:rgba(255,255,255,0.12);border-radius:2px;"></div></div> <div style="background:#7a8c3a; display:flex; align-items:center; justify-content:center;"><div style="width:120px;height:160px;background:rgba(255,255,255,0.12);border-radius:2px;"></div></div> </div> </div> <div style="display:grid; grid-template-columns:1fr 1fr; gap:30px; padding:30px 0 0 0;"> <div> <h2 style="margin:0; font-family:var(--font-labilvariable); font-size:28px; font-weight:400; line-height:1.28; letter-spacing:0.05em; color:var(--color-black-ink);">The joy and power of Risograph: Risotto showcases 400 printed postcards from artists across the globe</h2> </div> <div style="display:flex; flex-direction:column; justify-content:space-between;"> <p style="margin:0 0 16px 0; font-family:var(--font-bradford); font-size:15px; line-height:1.53; letter-spacing:0.008em; color:var(--color-black-ink);">Print and design studio Risotto is marking 100 months of artist postcards, all printed by hand and posted worldwide, with an exhibition that puts the beauty and breadth of Risograph on show.</p> <div> <p style="margin:0 0 12px 0; font-family:var(--font-labil); font-size:11px; color:var(--color-medium-gray); letter-spacing:0.005em;">4 days ago</p> <div style="display:flex; gap:6px; flex-wrap:wrap;"> <span style="display:inline-block; font-family:var(--font-bradford); font-size:11px; color:var(--color-black-ink); background:var(--color-frost-gray); padding:5px 10px; letter-spacing:0.005em;">Features</span> <span style="display:inline-block; font-family:var(--font-bradford); font-size:11px; color:var(--color-black-ink); background:var(--color-frost-gray); padding:5px 10px; letter-spacing:0.005em;">Event</span> <span style="display:inline-block; font-family:var(--font-bradford); font-size:11px; color:var(--color-black-ink); background:var(--color-frost-gray); padding:5px 10px; letter-spacing:0.005em;">...</span> </div> </div> </div> </div> </div>

### Floating Navigation Bar
- **html**: <div style="--color-black-ink:#2b2b2b;--color-pure-white:#ffffff;--color-frost-gray:#f0efef;--color-medium-gray:#676767;--color-muted-taupe:#faead9;--color-electric-purple:#8147ff;--color-sunshine-yellow:#ffd519;--font-bradford:Georgia,serif;--font-labilvariable:'Open Sans',sans-serif;--font-labil:'Open Sans',sans-serif; box-sizing:border-box; width:600px; background:#f5f5f5; padding:40px 20px; display:flex; justify-content:center;"> <div style="display:flex; align-items:center; gap:0; background:var(--color-pure-white); border-radius:75px; box-shadow:0 4px 24px rgba(0,0,0,0.13); padding:6px 6px 6px 16px; width:100%; max-width:560px;"> <div style="display:flex; align-items:center; justify-content:center; width:36px; height:36px; border-radius:50%; background:var(--color-black-ink); flex-shrink:0; margin-right:8px;"> <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg"><circle cx="10" cy="10" r="8" stroke="white" stroke-width="1.5"/><path d="M7 10c0-1.657 1.343-3 3-3s3 1.343 3 3-1.343 3-3 3-3-1.343-3-3z" fill="white"/></svg> </div> <nav style="display:flex; align-items:center; flex:1; gap:0;"> <a href="#" style="font-family:var(--font-labilvariable); font-size:13px; font-weight:400; letter-spacing:0.032em; color:var(--color-black-ink); text-decoration:none; white-space:nowrap; padding:8px 12px;">Projects + Creatives</a> <a href="#" style="font-family:var(--font-labilvariable); font-size:13px; font-weight:400; letter-spacing:0.032em; color:var(--color-black-ink); text-decoration:none; white-space:nowrap; padding:8px 12px;">Insights + Opinion</a> <a href="#" style="font-family:var(--font-labilvariable); font-size:13px; font-weight:400; letter-spacing:0.032em; color:var(--color-black-ink); text-decoration:none; white-space:nowrap; padding:8px 10px;">Resources + Advice</a> </nav> <button style="display:flex; align-items:center; gap:8px; background:var(--color-electric-purple); color:var(--color-pure-white); border:none; border-radius:75px; padding:10px 20px; font-family:var(--font-labilvariable); font-size:13px; font-weight:400; letter-spacing:0.032em; cursor:pointer; flex-shrink:0; white-space:nowrap;"> <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg"><circle cx="6" cy="6" r="4.5" stroke="white" stroke-width="1.5"/><path d="M9.5 9.5L12.5 12.5" stroke="white" stroke-width="1.5" stroke-linecap="round"/></svg> Search </button> </div> </div>

### Primary Ghost Button
- **role**: Call to action, navigation
- **description**: Transparent background, Black Ink text (#2b2b2b), Black Ink border (#2b2b2b). Text uses Bradford font, weight 400. No border radius. Padding 12.5px vertically, 12.5px horizontally.

### Category Label Button
- **role**: Informational grouping, filtering
- **description**: Muted Taupe background (#faead9), Black Ink text (#2b2b2b), Black Ink border (#2b2b2b). Text uses Bradford font, weight 400. No border radius. Padding 12.5px vertically, 12.5px horizontally.

### Pill Accent Button
- **role**: Primary call to action (floating nav)
- **description**: Electric Purple background (#8147ff), Pure White text (#ffffff), Pure White border (#ffffff). Text uses LabilVariable font, weight 400. Border radius 75px. Padding 0px vertically, 20px horizontally.

### Highlighted Button
- **role**: Prominent action
- **description**: Transparent background, Sunshine Yellow text (#ffd519), Sunshine Yellow border (#ffd519). Text uses LabilVariable font, weight 400. No border radius. Padding 15px top, 16px bottom, 20px horizontally.

### Badge Tag
- **role**: Content categorization
- **description**: Transparent background, Frost Gray text (#f0efef). Text uses Bradford font, weight 400. No border radius. Padding 5px vertically, 10px horizontally.

### Article Card
- **role**: Content listing
- **description**: Transparent background, no shadow, no border radius. Padded at 0px. Content is structured within this transparent bounding box, images are essential for visual interest.

### Search Input Field
- **role**: User input
- **description**: Pure White background (#ffffff), Black Ink text (#000000), Black Ink border (#000000). No border radius. Text uses LabilVariable font, weight 400. Padding 15px top, 16px bottom, 20px horizontally.

## Agent Prompt Guide

### Quick Color Reference
Text: #2b2b2b
Background: #ffffff
CTA: #8147ff
Border: #2b2b2b
Accent: #ffd519

### 3-5 Example Component Prompts
1.  **Create a main article headline**: Text 'The joy and power of Risograph: Risotto showcases 400 printed postcards from artists across the globe'. Font LabilVariable, weight 400, size 40px, lineHeight 1.73, letterSpacing 0.091em. Color Black Ink (#2b2b2b).
2.  **Generate a primary call-to-action button for a sticky footer**: Text 'Search'. Background Electric Purple (#8147ff), text Pure White (#ffffff), border Pure White (#ffffff), borderRadius 75px, padding 0px 20px. Font LabilVariable, weight 400, size 17px.
3.  **Produce a category badge**: Text 'Advertising'. Background transparent, text Frost Gray (#f0efef), borderRadius 0px, padding 5px 10px. Font Bradford, weight 400, size 11px.
4.  **Design a hero section with a main title and a subtitle**: Main title: 'It's Nice That' - LabilVariable, weight 400, size 40px, lineHeight 1.73, letterSpacing 0.091em, color Black Ink (#2b2b2b). Subtitle: 'Inspiring Creativity Since 2007' - Bradford, weight 400, size 17px, lineHeight 1.53, letterSpacing 0.027em, color Medium Gray (#676767). Default page background Pure White (#ffffff).
5.  **Create a text input field**: Placeholder text 'Type your search...'. Background Pure White (#ffffff), text Black Ink (#000000), border Black Ink (#000000), borderRadius 0px, padding 15px top, 16px bottom, 20px horiz. Font LabilVariable, weight 400, size 15px.
