---
version: alpha
source: refero
source_id: 9165ecb1-f068-4093-8783-1f3c98898b8a
source_url: https://monocle.com
name: Monocle
description: "Monocle's design evokes a classic, authoritative editorial feel, grounded in high-contrast typography on a clean white canvas. The system prioritizes crisp lines, clear hierarchy, and restraint over flourish, creating an environment where content takes center stage. Signature elements include the tight letter-spacing on headlines, the use of a custom serif font for primary content, and a sparse accent palette that highlights interactivity and key features without visual noise."
theme: light
northStar: "Ink-on-paper minimalist; a finely printed journal on pristine stock."
category: editorial
tags: ["editorial", "minimalist", "high-contrast", "classic", "serene", "authoritative", "typographic", "newspaper-like"]

colors:
  canvas-white: "#ffffff"  # neutral — Page backgrounds, elevated card surfaces, body text background.
  printer-s-black: "#000000"  # neutral — Primary text, headers, borders, active navigation elements – ensuring maximum contrast and
  sterling-gray: "#6e6e6"  # neutral — Secondary text, metadata, disabled states, subtle borders – providing depth against bright
  zinc-gray: "#d9d9d9"  # neutral — Muted borders, dividers, subtle inactive states – defining structure without visual weight
  cloud-gray: "#e7e7e7"  # neutral — Background for subtle card variants and distinct UI sections.
  parchment-cream: "#fdfcf3"  # neutral — Subtle background for specific UI elements, adding a hint of warmth.
  editorial-yellow: "#ffc500"  # brand — Call-to-action buttons, active navigation indicators, key interactive elements – a vivid p
  sky-blue: "#64d5ff"  # accent — Card backgrounds for specific content categories, offering a cool counterpoint to the neut

typography:
  plantin:
    family: "Plantin"
    sizes: "13px, 16px, 18px, 20px, 24px, 28px, 32px, 34px, 40px"
    weight: "400, 700"
    lineHeight: "1.00, 1.13, 1.15, 1.20, 1.25, 1.30, 1.38, 1.44, 1.50"
    letterSpacing: "-0.0200em, 0.0100em, 0.0500em, 0.0750em"
    substitute: "Georgia"
    use: "Primary content, article headlines, body text, and any long-form narrative. The custom serif embodies the brand's traditional editorial authority."
  helvetica-neue:
    family: "Helvetica Neue"
    sizes: "13px, 14px, 16px, 24px"
    weight: "400, 700"
    lineHeight: "1.00, 1.13, 1.25, 1.29, 1.38, 1.50"
    letterSpacing: "0.0100em"
    substitute: "Arial"
    use: "UI elements, navigation, buttons, and short descriptive text – providing a clean, modern contrast to the serif content."
  chanel:
    family: "Chanel"
    sizes: "9px"
    weight: "700"
    lineHeight: "1.00"
    letterSpacing: "normal"
    substitute: "Playfair Display"
    use: "Distinctive custom display font, likely reserved for branded elements like the main Monocle logo."
---

# Monocle — Design System

> Ink-on-paper minimalist; a finely printed journal on pristine stock.


Monocle's design evokes a classic, authoritative editorial feel, grounded in high-contrast typography on a clean white canvas. The system prioritizes crisp lines, clear hierarchy, and restraint over flourish, creating an environment where content takes center stage. Signature elements include the tight letter-spacing on headlines, the use of a custom serif font for primary content, and a sparse accent palette that highlights interactivity and key features without visual noise.


## Type Scale

- role: caption · size: 13 · lineHeight: 1.5 · letterSpacing: 0.01
- role: body · size: 16 · lineHeight: 1.5 · letterSpacing: 0.01
- role: subheading · size: 24 · lineHeight: 1.25 · letterSpacing: -0.48
- role: heading · size: 32 · lineHeight: 1.15 · letterSpacing: -0.64
- role: display · size: 40 · lineHeight: 1.13 · letterSpacing: -0.8

## Color Palette


### Neutral
- **Canvas White** `#ffffff` — Page backgrounds, elevated card surfaces, body text background.
- **Printer's Black** `#000000` — Primary text, headers, borders, active navigation elements – ensuring maximum contrast and legibility.
- **Sterling Gray** `#6e6e6` — Secondary text, metadata, disabled states, subtle borders – providing depth against brighter neutrals.
- **Zinc Gray** `#d9d9d9` — Muted borders, dividers, subtle inactive states – defining structure without visual weight.
- **Cloud Gray** `#e7e7e7` — Background for subtle card variants and distinct UI sections.
- **Parchment Cream** `#fdfcf3` — Subtle background for specific UI elements, adding a hint of warmth.

### Brand
- **Editorial Yellow** `#ffc500` — Call-to-action buttons, active navigation indicators, key interactive elements – a vivid punctuation mark.

### Accent
- **Sky Blue** `#64d5ff` — Card backgrounds for specific content categories, offering a cool counterpoint to the neutral palette.

## Layout

The page adheres to a max-width 1296px centered layout, creating a contained reading experience. The hero section features a prominent brand marque and headline, often with a large, editorial photograph beneath it, setting an immediate authoritative tone. Content is arranged in a grid-like fashion, employing a combination of single-column article previews and multiple-column card grids for features and related content. The rhythm is established by consistent vertical spacing of 32px between major sections and 16px padding within cards. Navigation is persistent at the top, splitting into a utility bar and a primary category navigation. The layout is information-dense but organized, resembling a structured print publication.


## Imagery

Imagery is primarily editorial photography and stylized illustrations. Photography is typically tightly cropped, showcasing subjects directly in a high-key or natural light. Illustrations are often line-drawn with minimal flat colors, or possess a distinctive, quirky style (like the plane diagram or the Nic Monisse portrait). Images are usually contained within card structures or embedded directly into the content stream, not used as full-bleed hero elements. They serve an explanatory or illustrative role rather than purely decorative, balancing text-heavy layouts.


## Spacing

- **radius**: {'cards': '8px', 'buttons': '0px', 'navBadges': '50%'}
- **elementGap**: 4px
- **sectionGap**: 32px
- **cardPadding**: 16px
- **pageMaxWidth**: 1296px

## Do

- Prioritize Plantin for all article bodies and headlines to maintain editorial voice.
- Use Printer's Black (#000000) on Canvas White (#ffffff) for all primary text and background combinations.
- Apply 8px border-radius for all content cards and UI blocks where a soft edge is needed.
- Reserve Editorial Yellow (#ffc500) exclusively for calls to action and critical interactive states.
- Maintain tight letter-spacing for headlines (e.g., -0.64px for 32px Plantin headings) to enhance visual density.
- Utilize Helvetica Neue for navigation and utility text, setting it at 13px weight 400 for consistency.
- Implement 16px internal padding for all card components to provide sufficient breathing room for content.

## Don't

- Do not introduce additional color accents beyond Editorial Yellow (#ffc500) and Sky Blue (#64d5ff).
- Avoid box shadows or elevations; establish depth through background color changes (Canvas White, Cloud Gray, Sky Blue).
- Do not use rounded corners on primary buttons or navigation elements; maintain sharp, defined edges.
- Never use less than 4px spacing between elements unless for iconography or nested micro-interactions.
- Do not deviate from the specified font families; avoid system defaults for major text blocks.
- Avoid large, impactful hero images; focus on contained, editorial photography or illustrations.
- Do not use highly decorative UI elements; stick to functional and minimal design patterns.

## Components


### Monocle Radio Podcast Player Card
- **html**: <style>:root{--color-canvas-white:#ffffff;--color-printers-black:#000000;--color-sterling-gray:#6e6e6e;--color-zinc-gray:#d9d9d9;--color-cloud-gray:#e7e7e7;--color-parchment-cream:#fdfcf3;--color-editorial-yellow:#ffc500;--color-sky-blue:#64d5ff;--font-plantin:Georgia,serif;--font-helvetica-neue:'Helvetica Neue',Arial,sans-serif;}</style><div style="width:600px;background:var(--color-printers-black);border-radius:8px;padding:20px;box-sizing:border-box;font-family:var(--font-helvetica-neue);"><div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:16px;"><span style="color:var(--color-canvas-white);font-family:var(--font-helvetica-neue);font-size:16px;font-weight:700;letter-spacing:0.05em;">MONOCLE RADIO</span></div><div style="background:#1a1a1a;border-radius:6px;padding:16px;margin-bottom:12px;display:flex;align-items:center;gap:12px;"><div style="display:flex;align-items:center;gap:6px;"><span style="color:var(--color-editorial-yellow);font-family:var(--font-helvetica-neue);font-size:13px;font-weight:700;letter-spacing:0.05em;">ON AIR</span><svg width="18" height="14" viewBox="0 0 18 14" fill="none" xmlns="http://www.w3.org/2000/svg"><rect x="0" y="4" width="3" height="6" fill="#ffc500"/><rect x="5" y="1" width="3" height="12" fill="#ffc500"/><rect x="10" y="3" width="3" height="8" fill="#ffc500"/><rect x="15" y="2" width="3" height="10" fill="#ffc500"/></svg></div><span style="color:var(--color-canvas-white);font-family:var(--font-helvetica-neue);font-size:14px;font-weight:700;letter-spacing:0.05em;">GLOBAL MUSIC</span></div><a href="#" style="display:flex;align-items:center;justify-content:center;gap:10px;background:var(--color-editorial-yellow);color:var(--color-printers-black);font-family:var(--font-helvetica-neue);font-size:14px;font-weight:700;letter-spacing:0.08em;text-decoration:none;padding:14px 24px;border-radius:0;margin-bottom:16px;width:100%;box-sizing:border-box;"><svg width="12" height="14" viewBox="0 0 12 14" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M0 0L12 7L0 14V0Z" fill="#000000"/></svg>LISTEN LIVE</a><div style="display:flex;align-items:center;gap:8px;margin-bottom:20px;"><span style="color:var(--color-sterling-gray);font-family:var(--font-helvetica-neue);font-size:11px;letter-spacing:0.08em;">SPONSORED BY</span><div style="background:var(--color-canvas-white);border-radius:3px;padding:4px 10px;display:flex;align-items:center;justify-content:center;"><span style="font-family:var(--font-helvetica-neue);font-size:13px;font-weight:700;color:var(--color-printers-black);letter-spacing:0.05em;">UBS</span></div></div><div style="border-top:1px solid #2a2a2a;padding-top:12px;display:flex;gap:12px;align-items:flex-start;margin-bottom:12px;"><div style="width:64px;height:64px;background:#222;border-radius:4px;flex-shrink:0;display:flex;align-items:center;justify-content:center;"><span style="color:var(--color-canvas-white);font-family:var(--font-helvetica-neue);font-size:9px;font-weight:700;text-align:center;letter-spacing:0.05em;">MONOCLE<br>RADIO</span></div><div style="flex:1;"><div style="color:var(--color-canvas-white);font-family:var(--font-helvetica-neue);font-size:14px;font-weight:700;letter-spacing:0.01em;margin-bottom:4px;">Top of the Hour</div><div style="color:var(--color-sterling-gray);font-family:var(--font-helvetica-neue);font-size:13px;letter-spacing:0.01em;">Headlines as they happen</div></div></div><div style="border-top:1px solid #2a2a2a;padding-top:12px;display:flex;gap:12px;align-items:flex-start;margin-bottom:20px;"><div style="width:64px;height:64px;background:#3a1a3a;border-radius:4px;flex-shrink:0;display:flex;align-items:center;justify-content:center;"><span style="color:#ff69b4;font-family:var(--font-helvetica-neue);font-size:8px;font-weight:700;text-align:center;">Meet<br>the<br>Writers</span></div><div style="flex:1;"><div style="color:var(--color-canvas-white);font-family:var(--font-helvetica-neue);font-size:14px;font-weight:700;letter-spacing:0.01em;margin-bottom:4px;">Meet the Writers</div><div style="color:var(--color-sterling-gray);font-family:var(--font-helvetica-neue);font-size:13px;letter-spacing:0.01em;">Georgina Godwin chats to your favourite authors</div></div></div><a href="#" style="display:block;text-align:center;background:transparent;color:var(--color-canvas-white);font-family:var(--font-helvetica-neue);font-size:13px;font-weight:700;letter-spacing:0.1em;text-decoration:none;padding:12px 24px;border:1px solid #444;border-radius:0;">VIEW FULL PROGRAMME</a></div>

### Article Feature Card with Category Label and Read Time
- **html**: <style>:root{--color-canvas-white:#ffffff;--color-printers-black:#000000;--color-sterling-gray:#6e6e6e;--color-zinc-gray:#d9d9d9;--color-cloud-gray:#e7e7e7;--color-parchment-cream:#fdfcf3;--color-editorial-yellow:#ffc500;--color-sky-blue:#64d5ff;--font-plantin:Georgia,serif;--font-helvetica-neue:'Helvetica Neue',Arial,sans-serif;}</style><div style="width:600px;box-sizing:border-box;font-family:var(--font-helvetica-neue);background:var(--color-canvas-white);padding:0;"><div style="border-bottom:1px solid var(--color-zinc-gray);padding-bottom:24px;margin-bottom:0;"><div style="display:flex;gap:20px;align-items:flex-start;"><div style="flex:1;"><div style="margin-bottom:10px;"><span style="font-family:var(--font-helvetica-neue);font-size:13px;font-weight:700;letter-spacing:0.08em;color:var(--color-printers-black);">POLITICS</span></div><h2 style="font-family:var(--font-plantin);font-size:28px;font-weight:400;line-height:1.2;letter-spacing:-0.02em;color:var(--color-printers-black);margin:0 0 12px 0;">After 100 days of Zohran Mamdani's New York, is the first-time mayor living up to the hype?</h2><p style="font-family:var(--font-plantin);font-size:16px;line-height:1.5;color:var(--color-printers-black);margin:0 0 16px 0;">As the mayor settles into his first term at the helm of New York, we review his promises on housing, transport, small-business affordability and immigration.</p><div style="display:flex;align-items:center;gap:8px;"><svg width="16" height="14" viewBox="0 0 16 14" fill="none" xmlns="http://www.w3.org/2000/svg"><rect x="0" y="0" width="16" height="10" rx="1" stroke="#000" stroke-width="1.2" fill="none"/><rect x="3" y="10" width="10" height="4" rx="0" stroke="#000" stroke-width="1.2" fill="none"/></svg><span style="color:var(--color-sterling-gray);font-family:var(--font-helvetica-neue);font-size:13px;letter-spacing:0.01em;">|</span><span style="color:var(--color-sterling-gray);font-family:var(--font-helvetica-neue);font-size:13px;letter-spacing:0.05em;">11 MIN READ</span></div></div></div><div style="margin-top:24px;"><div style="width:100%;height:280px;background:var(--color-cloud-gray);border-radius:0;overflow:hidden;position:relative;"><div style="width:100%;height:100%;background:linear-gradient(135deg,#c8b89a 0%,#a89070 50%,#d4b896 100%);display:flex;align-items:center;justify-content:center;"><div style="width:120px;height:160px;background:rgba(0,0,0,0.15);border-radius:2px;display:flex;align-items:center;justify-content:center;"><span style="color:rgba(255,255,255,0.6);font-size:11px;font-family:var(--font-helvetica-neue);">Photo</span></div></div></div></div></div><div style="display:grid;grid-template-columns:1fr 1fr;gap:0;border-bottom:1px solid var(--color-zinc-gray);"><div style="padding:20px 20px 20px 0;border-right:1px solid var(--color-zinc-gray);"><div style="width:100%;height:140px;background:var(--color-cloud-gray);border-radius:0;margin-bottom:12px;overflow:hidden;"><div style="width:100%;height:100%;background:linear-gradient(135deg,#e8d5c0 0%,#c4a882 100%);"></div></div><div style="margin-bottom:8px;"><span style="font-family:var(--font-helvetica-neue);font-size:11px;font-weight:700;letter-spacing:0.08em;color:var(--color-printers-black);">THE WEEKEND OPENER</span></div><h3 style="font-family:var(--font-plantin);font-size:20px;font-weight:400;line-height:1.25;letter-spacing:-0.01em;color:var(--color-printers-black);margin:0 0 12px 0;">Don't wing it. Here's how to behave on a plane</h3><div style="display:flex;align-items:center;gap:8px;"><svg width="14" height="12" viewBox="0 0 14 12" fill="none"><rect x="0" y="0" width="14" height="8" rx="1" stroke="#6e6e6e" stroke-width="1" fill="none"/><rect x="3" y="8" width="8" height="3" stroke="#6e6e6e" stroke-width="1" fill="none"/></svg><span style="color:var(--color-sterling-gray);font-family:var(--font-helvetica-neue);font-size:12px;">|  4 MIN READ</span></div></div><div style="padding:20px 0 20px 20px;"><div style="width:100%;height:140px;background:var(--color-cloud-gray);border-radius:0;margin-bottom:12px;overflow:hidden;"><div style="width:100%;height:100%;background:linear-gradient(135deg,#8a9bb0 0%,#607080 100%);"></div></div><div style="margin-bottom:8px;"><span style="font-family:var(--font-helvetica-neue);font-size:11px;font-weight:700;letter-spacing:0.08em;color:var(--color-printers-black);">AFFAIRS</span></div><h3 style="font-family:var(--font-plantin);font-size:20px;font-weight:400;line-height:1.25;letter-spacing:-0.01em;color:var(--color-printers-black);margin:0 0 12px 0;">What's in a ceasefire? Mixed messages, faultlines and fearing the worst</h3><div style="display:flex;align-items:center;gap:8px;"><svg width="14" height="12" viewBox="0 0 14 12" fill="none"><rect x="0" y="0" width="14" height="8" rx="1" stroke="#6e6e6e" stroke-width="1" fill="none"/><rect x="3" y="8" width="8" height="3" stroke="#6e6e6e" stroke-width="1" fill="none"/></svg><span style="color:var(--color-sterling-gray);font-family:var(--font-helvetica-neue);font-size:12px;">|  5 MIN READ</span></div></div></div></div>

### Podcast Episode Cards Grid
- **html**: <style>:root{--color-canvas-white:#ffffff;--color-printers-black:#000000;--color-sterling-gray:#6e6e6e;--color-zinc-gray:#d9d9d9;--color-cloud-gray:#e7e7e7;--color-parchment-cream:#fdfcf3;--color-editorial-yellow:#ffc500;--color-sky-blue:#64d5ff;--font-plantin:Georgia,serif;--font-helvetica-neue:'Helvetica Neue',Arial,sans-serif;}</style><div style="width:600px;background:var(--color-printers-black);box-sizing:border-box;padding:24px 20px;font-family:var(--font-helvetica-neue);"><div style="display:grid;grid-template-columns:1fr 1fr;gap:16px;"><div style="background:#1c1c1c;border-radius:4px;overflow:hidden;"><div style="position:relative;"><div style="width:100%;height:150px;background:linear-gradient(135deg,#2a1a0a 0%,#5a3a20 50%,#3a2a10 100%);display:flex;align-items:center;justify-content:center;"><div style="position:absolute;top:10px;left:10px;width:32px;height:32px;background:var(--color-editorial-yellow);border-radius:50%;display:flex;align-items:center;justify-content:center;"><svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 2a4 4 0 100 8 4 4 0 000-8zm0 1.5a2.5 2.5 0 110 5 2.5 2.5 0 010-5z" fill="#000"/><path d="M7 6H11" stroke="#000" stroke-width="1.5"/></svg></div></div></div><div style="padding:12px;"><div style="font-family:var(--font-helvetica-neue);font-size:11px;font-weight:700;letter-spacing:0.08em;color:var(--color-sterling-gray);margin-bottom:6px;">AFFAIRS</div><div style="font-family:var(--font-plantin);font-size:15px;font-weight:400;line-height:1.3;color:var(--color-canvas-white);margin-bottom:10px;">Operation Epic Fury: Is that it?</div><div style="display:flex;align-items:center;gap:6px;"><svg width="10" height="12" viewBox="0 0 10 12" fill="none"><circle cx="5" cy="5" r="4" stroke="#6e6e6e" stroke-width="1" fill="none"/><rect x="4" y="9" width="2" height="3" fill="#6e6e6e"/></svg><span style="font-family:var(--font-helvetica-neue);font-size:11px;letter-spacing:0.06em;color:var(--color-sterling-gray);">THE FOREIGN DESK  |  29 MIN</span></div></div></div><div style="background:#1c1c1c;border-radius:4px;overflow:hidden;"><div style="position:relative;"><div style="width:100%;height:150px;background:linear-gradient(135deg,#1a2a3a 0%,#304050 50%,#1a2030 100%);display:flex;align-items:center;justify-content:center;"><div style="position:absolute;top:10px;left:10px;width:32px;height:32px;background:var(--color-editorial-yellow);border-radius:50%;display:flex;align-items:center;justify-content:center;"><svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 2a4 4 0 100 8 4 4 0 000-8zm0 1.5a2.5 2.5 0 110 5 2.5 2.5 0 010-5z" fill="#000"/><path d="M7 6H11" stroke="#000" stroke-width="1.5"/></svg></div></div></div><div style="padding:12px;"><div style="font-family:var(--font-helvetica-neue);font-size:11px;font-weight:700;letter-spacing:0.08em;color:var(--color-sterling-gray);margin-bottom:6px;">AFFAIRS</div><div style="font-family:var(--font-plantin);font-size:15px;font-weight:400;line-height:1.3;color:var(--color-canvas-white);margin-bottom:10px;">Iran talks and Hungary's election. Plus: the ultimate guide to hosting</div><div style="display:flex;align-items:center;gap:6px;"><svg width="10" height="12" viewBox="0 0 10 12" fill="none"><circle cx="5" cy="5" r="4" stroke="#6e6e6e" stroke-width="1" fill="none"/><rect x="4" y="9" width="2" height="3" fill="#6e6e6e"/></svg><span style="font-family:var(--font-helvetica-neue);font-size:11px;letter-spacing:0.06em;color:var(--color-sterling-gray);">MONOCLE ON SATURDAY  |  32 MIN</span></div></div></div><div style="background:#1c1c1c;border-radius:4px;overflow:hidden;"><div style="position:relative;"><div style="width:100%;height:150px;background:linear-gradient(135deg,#2a2a10 0%,#5a5a20 50%,#3a3a10 100%);display:flex;align-items:center;justify-content:center;"><div style="position:absolute;top:10px;left:10px;width:32px;height:32px;background:var(--color-editorial-yellow);border-radius:50%;display:flex;align-items:center;justify-content:center;"><svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 2a4 4 0 100 8 4 4 0 000-8zm0 1.5a2.5 2.5 0 110 5 2.5 2.5 0 010-5z" fill="#000"/><path d="M7 6H11" stroke="#000" stroke-width="1.5"/></svg></div><div style="width:70px;height:70px;background:var(--color-editorial-yellow);border-radius:4px;display:flex;align-items:center;justify-content:center;flex-direction:column;"><span style="font-family:var(--font-helvetica-neue);font-size:9px;font-weight:700;color:#000;text-align:center;line-height:1.2;">The<br>Curator<br>Round-up</span></div></div></div><div style="padding:12px;"><div style="font-family:var(--font-helvetica-neue);font-size:11px;font-weight:700;letter-spacing:0.08em;color:var(--color-sterling-gray);margin-bottom:6px;">AFFAIRS</div><div style="font-family:var(--font-plantin);font-size:15px;font-weight:400;line-height:1.3;color:var(--color-canvas-white);margin-bottom:10px;">What We Learned: The fragile Middle East ceasefire, teleporting to Waffle House</div><div style="display:flex;align-items:center;gap:6px;"><svg width="10" height="12" viewBox="0 0 10 12" fill="none"><circle cx="5" cy="5" r="4" stroke="#6e6e6e" stroke-width="1" fill="none"/><rect x="4" y="9" width="2" height="3" fill="#6e6e6e"/></svg><span style="font-family:var(--font-helvetica-neue);font-size:11px;letter-spacing:0.06em;color:var(--color-sterling-gray);">THE CURATOR  |  6 MIN</span></div></div></div><div style="background:#1c1c1c;border-radius:4px;overflow:hidden;"><div style="position:relative;"><div style="width:100%;height:150px;background:linear-gradient(135deg,#1a1a2a 0%,#252535 50%,#1a1a20 100%);display:flex;align-items:center;justify-content:center;"><div style="position:absolute;top:10px;left:10px;width:32px;height:32px;background:var(--color-editorial-yellow);border-radius:50%;display:flex;align-items:center;justify-content:center;"><svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 2a4 4 0 100 8 4 4 0 000-8zm0 1.5a2.5 2.5 0 110 5 2.5 2.5 0 010-5z" fill="#000"/><path d="M7 6H11" stroke="#000" stroke-width="1.5"/></svg></div></div></div><div style="padding:12px;"><div style="font-family:var(--font-helvetica-neue);font-size:11px;font-weight:700;letter-spacing:0.08em;color:var(--color-sterling-gray);margin-bottom:6px;">AFFAIRS</div><div style="font-family:var(--font-plantin);font-size:15px;font-weight:400;line-height:1.3;color:var(--color-canvas-white);margin-bottom:10px;">Revealed: Monocle's new weekly quiz!</div><div style="display:flex;align-items:center;gap:6px;"><svg width="10" height="12" viewBox="0 0 10 12" fill="none"><circle cx="5" cy="5" r="4" stroke="#6e6e6e" stroke-width="1" fill="none"/><rect x="4" y="9" width="2" height="3" fill="#6e6e6e"/></svg><span style="font-family:var(--font-helvetica-neue);font-size:11px;letter-spacing:0.06em;color:var(--color-sterling-gray);">THE MONOCLE DAILY  |  39 MIN</span></div></div></div></div><div style="display:flex;justify-content:flex-end;margin-top:16px;"><button style="width:36px;height:36px;background:transparent;border:1px solid var(--color-sterling-gray);border-radius:50%;color:var(--color-canvas-white);display:flex;align-items:center;justify-content:center;cursor:pointer;"><svg width="10" height="14" viewBox="0 0 10 14" fill="none"><path d="M2 2l6 5-6 5" stroke="#ffffff" stroke-width="1.5" stroke-linecap="round"/></svg></button></div></div>

### Primary Navigation Link
- **role**: Interactive element
- **description**: Text in Printer's Black (#000000), Helvetica Neue, weight 400. Underlined with a 1px solid Printer's Black (#000000) border when active or hovered. No padding.

### Call-to-Action Button
- **role**: Primary action
- **description**: Background Editorial Yellow (#ffc500), text Printer's Black (#000000), Helvetica Neue, weight 700. No border, no radius. Content based on current context.

### Icon Button (Circular Outline)
- **role**: Secondary action/icon toggle
- **description**: Transparent background, Printer's Black (#000000) text (icon), 1px Printer's Black (#000000) circular border, 50% border-radius. No padding.

### Standard Content Card
- **role**: Content container
- **description**: Background Canvas White (#ffffff), 8px border-radius, no box shadow. Internal padding of 16px around content.

### Category Label Card
- **role**: Thematic content grouping
- **description**: Background Sky Blue (#64d5ff), 8px border-radius, no box shadow. Internal padding of 16px around content.

### Neutral Background Card
- **role**: Subtle content grouping
- **description**: Background Cloud Gray (#e7e7e7), 8px border-radius, no box shadow. Internal padding of 16px around content.

### Podcast Player Card
- **role**: Dynamic audio content display
- **description**: Background Printer's Black (#000000), 8px border-radius, no box shadow. Features an Editorial Yellow (#ffc500) 'Listen Live' button.

### Search Input Field
- **role**: User input
- **description**: Canvas White (#ffffff) background, Printer's Black (#000000) text. No border, no radius. Padding of 16px.

## Agent Prompt Guide

### Quick Color Reference
- Text: #000000 (Printer's Black)
- Background: #ffffff (Canvas White)
- CTA: #ffc500 (Editorial Yellow)
- Border/Divider: #d9d9d9 (Zinc Gray)
- Secondary Text: #6e6e6 (Sterling Gray)

### 3-5 Example Component Prompts
1. Create a `Primary Navigation Link`: text 'Magazine', font Helvetica Neue weight 400, size 16px, color #000000. Underline in #000000 on hover.
2. Design a `Call-to-Action Button`: text 'Subscribe', font Helvetica Neue weight 700, size 16px, background #ffc500, text color #000000, no border, no radius. Padding 6px horizontal, 0px vertical.
3. Build a `Standard Content Card`: background #ffffff, 8px border-radius, no shadow. Internal padding 16px. Add a headline: Plantin weight 700, size 24px, color #000000, letter-spacing -0.48px. Follow with body text: Plantin weight 400, size 16px, color #000000, line-height 1.5.
4. Generate a `Category Label Card`: background #64d5ff, 8px border-radius, 16px padding. Include a title like 'The Weekend Opener' using Plantin weight 700, size 20px, color #000000.
5. Create an `Input Field`: background #ffffff, text color #000000, padding 16px. Placeholder text 'Search' in Sterling Gray #6e6e6e.
