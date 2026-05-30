---
version: alpha
source: refero
source_id: 8eb9c53e-d69c-497a-b640-610856cf3a60
source_url: https://hyperstudio.org
name: Hyperstudio
description: "This design system evokes a sparse, high-contrast digital workspace, reminiscent of a command line interface or early internet text modes but with a refined typographic sensibility. The stark black backgrounds (#101010, #080808) are punctuated by crisp white text (#F3F3F3, #FFFFFF), creating a sense of technical precision and directness. Minimal chromatic accents (#E7C59A, #00AC5C) are used sparingly, like status lights, ensuring they immediately draw the eye and signify interactive elements or states without overwhelming the monochrome base. Custom Aeonik and Input fonts lend a distinctive, somewhat retro-futuristic feel, reinforcing the tech-focused brand identity."
theme: dark
northStar: "Monochrome terminal with amber accents. The design feels like a precisely coded interface, where every element serves a distinct, functional purpose against a dark, featureless backdrop."
category: agency
tags: ["dark mode", "monochrome", "high contrast", "minimalist", "tech-focused", "futuristic", "typographic", "precise", "command-line", "controlled accent"]

colors:
  midnight-void: "#101010"  # neutral — Primary page background, deepest dark surface.
  deep-space: "#080808"  # neutral — Secondary background, slightly darker than Midnight Void, used for subtle depth.
  polar-white: "#F3F3F3"  # neutral — Primary text color, hero headlines, clear contrast against dark backgrounds.
  absolute-zero: "#FFFFFF"  # neutral — Accent text and background for interactive elements like buttons, header text.
  ash-gray: "#949494"  # neutral — Secondary text, subtle borders, slightly toned down from main text.
  dark-carbon: "#333333"  # neutral — Border colors, muted backgrounds for secondary elements.
  slate: "#C1C1C1"  # neutral — Subtle borders, outlines, dividers.
  light-gradients: "#B5B5B5"  # neutral — Subtle background gradient for UI elements, providing a soft, almost imperceptible texture
  amber-glow: "#E7C59A"  # accent — Key accent color for interactive elements, 'NEW' tags, drawing attention in a restrained w
  neon-green: "#00AC5C"  # semantic — Small status indicators, 'spots left' tags, indicating positive status or availability.

typography:
  aeonik:
    family: "Aeonik"
    sizes: "13px, 14px, 16px, 17px, 18px, 21px, 23px, 34px, 44px, 63px"
    weight: "400, 700"
    lineHeight: "0.95, 1.03, 1.05, 1.07, 1.11, 1.22, 1.28, 1.29, 1.34, 1.35, 1.38, 1.43, 2.69"
    letterSpacing: "-0.011, -0.007"
    substitute: "Inter"
    use: "Primary typeface for all headlines, body text, and UI elements. Its confident, geometric forms convey technical modernity and clarity consistently across sizes."
  input:
    family: "Input"
    sizes: "13px, 14px, 16px, 17px, 18px"
    weight: "400"
    lineHeight: "1.20, 1.21, 1.25, 1.31, 1.48, 1.50, 1.54"
    letterSpacing: "-0.037, -0.022"
    substitute: "IBM Plex Mono"
    use: "Secondary typeface used for specific data points and code-like elements, adding a monospaced, technical contrast to Aeonik for specialized information. The tighter letter spacing enhances its code-lik"
---

# Hyperstudio — Design System

> Monochrome terminal with amber accents. The design feels like a precisely coded interface, where every element serves a distinct, functional purpose against a dark, featureless backdrop.


This design system evokes a sparse, high-contrast digital workspace, reminiscent of a command line interface or early internet text modes but with a refined typographic sensibility. The stark black backgrounds (#101010, #080808) are punctuated by crisp white text (#F3F3F3, #FFFFFF), creating a sense of technical precision and directness. Minimal chromatic accents (#E7C59A, #00AC5C) are used sparingly, like status lights, ensuring they immediately draw the eye and signify interactive elements or states without overwhelming the monochrome base. Custom Aeonik and Input fonts lend a distinctive, somewhat retro-futuristic feel, reinforcing the tech-focused brand identity.


## Type Scale

- role: caption · size: 13 · lineHeight: 1.43 · letterSpacing: -0.007
- role: subheading · size: 18 · lineHeight: 1.28
- role: heading-sm · size: 21 · lineHeight: 1.22
- role: heading · size: 23 · lineHeight: 1.11
- role: heading-lg · size: 34 · lineHeight: 1.07
- role: display · size: 44 · lineHeight: 1.03
- role: display-lg · size: 63 · lineHeight: 0.95 · letterSpacing: -0.011

## Color Palette


### Neutral
- **Midnight Void** `#101010` — Primary page background, deepest dark surface.
- **Deep Space** `#080808` — Secondary background, slightly darker than Midnight Void, used for subtle depth.
- **Polar White** `#F3F3F3` — Primary text color, hero headlines, clear contrast against dark backgrounds.
- **Absolute Zero** `#FFFFFF` — Accent text and background for interactive elements like buttons, header text.
- **Ash Gray** `#949494` — Secondary text, subtle borders, slightly toned down from main text.
- **Dark Carbon** `#333333` — Border colors, muted backgrounds for secondary elements.
- **Slate** `#C1C1C1` — Subtle borders, outlines, dividers.
- **Light Gradients** `#B5B5B5` — Subtle background gradient for UI elements, providing a soft, almost imperceptible texture.

### Accent
- **Amber Glow** `#E7C59A` — Key accent color for interactive elements, 'NEW' tags, drawing attention in a restrained way appropriate for a tech brand.

### Semantic
- **Neon Green** `#00AC5C` — Small status indicators, 'spots left' tags, indicating positive status or availability.

## Layout

The page primarily uses a full-bleed, dark-themed model with content centered within an implied maximum width, though no explicit max-width is strictly enforced visually. The hero section is full-viewport, featuring a prominent centered headline over an abstract pixelated graphic on a deep black background. Sections are delineated by consistent vertical spacing of approximately 64px, with subtle shifts in background darkness creating a sense of depth rather than sharp dividers. Content arrangement leans towards centered stacks or clear two-column grid layouts for textual features and service descriptions. The density is comfortable, with generous breathing room around content blocks. Navigation is a sticky top bar with a left-aligned logo and right-aligned links and a prominent 'LET'S CHAT' button.


## Imagery

The visual language is characterized by abstract, pixelated graphics, specifically 'hands' composed of stark white dots on a black background, which adds a digitized, almost retro-tech aesthetic. There are no traditional photographs or realistic illustrations. Icons are simple, outlined, and monochromatic, matching the overall dark theme's precision. These graphics appear to be decorative, creating atmosphere and visual interest without being literal product showcases. The density of imagery is low; large areas of the screen are dominated by text and UI elements, with graphics serving as large-scale background motifs. Treatment is full-bleed for the abstract graphics, often low-opacity or subtle, allowing them to complement rather than compete with text.


## Spacing

- **radius**: {'tags': '20px', 'buttons': '8px', 'default': '8px', 'statusIcons': '99px'}
- **elementGap**: 10px
- **sectionGap**: 64px
- **cardPadding**: 24px
- **pageMaxWidth**: None

## Do

- Prioritize high contrast between text and background, typically Polar White (#F3F3F3) on Midnight Void (#101010) or Absolute Zero (#FFFFFF) on Dark Carbon (#333333).
- Use Aeonik at size 63px, weight 700, and lineHeight 0.95 for primary display headlines to maintain a commanding yet compact presence.
- Employ Amber Glow (#E7C59A) exclusively for key attention-grabbing elements, such as 'NEW' labels or critical status indicators.
- Maintain a default border radius of 8px for most interactive elements and cards, using 99px only for circular or pill-shaped tags.
- Utilize Input font for any content that benefits from a monospace, data-like presentation, especially at -0.037em letter spacing for specific technical details.
- Structure layouts with ample section-gap (64px) to create a spacious, breathable feel between content blocks despite the dark theme.
- Employ Neon Green (#00AC5C) to denote positive status, availability, or success, ensuring it stands out as an unambiguous indicator.

## Don't

- Do not introduce additional vibrant colors; stick to Amber Glow (#E7C59A) and Neon Green (#00AC5C) as the only chromatic accents.
- Avoid using drop shadows for elevation; rely on varied shades of dark neutrals like Midnight Void (#101010) and Deep Space (#080808) for depth perception.
- Do not deviate from the specified tight line-heights for headlines, as they are crucial for the dense, impactful typographic style.
- Do not use generic system fonts; Aeonik and Input are essential to the brand's distinctive technical aesthetic.
- Avoid excessive rounding; maintain sharp or subtly rounded corners (8px) for most UI elements, reserving pill shapes for specific tags.
- Do not use full-width background images that break the defined dark background color palette; visual interest comes from typographic treatment and data visualization.

## Components


### Availability Status Pill + CTA Button Group
- **html**: <div style="
  --color-midnight-void: #101010;
  --color-deep-space: #080808;
  --color-polar-white: #F3F3F3;
  --color-absolute-zero: #FFFFFF;
  --color-ash-gray: #949494;
  --color-dark-carbon: #333333;
  --color-slate: #C1C1C1;
  --color-amber-glow: #E7C59A;
  --color-neon-green: #00AC5C;
  --font-aeonik: 'Inter', sans-serif;
  --font-input: 'IBM Plex Mono', monospace;
  background: var(--color-midnight-void);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 32px;
  padding: 48px 24px;
  font-family: var(--font-aeonik);
  width: 600px;
  box-sizing: border-box;
">
  <!-- Status pill -->
  <div style="
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(0,172,92,0.15);
    border: 1px solid rgba(0,172,92,0.35);
    border-radius: 99px;
    padding: 6px 14px;
  ">
    <span style="
      width: 8px;
      height: 8px;
      background: var(--color-neon-green);
      border-radius: 99px;
      display: inline-block;
      flex-shrink: 0;
      box-shadow: 0 0 6px var(--color-neon-green);
    "></span>
    <span style="
      font-family: var(--font-aeonik);
      font-size: 13px;
      font-weight: 400;
      color: var(--color-polar-white);
      letter-spacing: 0.06em;
      text-transform: uppercase;
    ">2/5 SPOTS LEFT FOR APRIL</span>
  </div>

  <!-- Headline -->
  <div style="text-align: center;">
    <h1 style="
      font-family: var(--font-aeonik);
      font-size: 52px;
      font-weight: 700;
      line-height: 0.95;
      color: var(--color-polar-white);
      margin: 0;
      letter-spacing: -0.011em;
    ">World-class branding<br>and websites<br>for startups.</h1>
  </div>

  <!-- Button group -->
  <div style="display: flex; gap: 12px; align-items: center; flex-wrap: wrap; justify-content: center;">
    <!-- Primary CTA -->
    <a href="#" style="
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--color-polar-white);
      color: var(--color-midnight-void);
      font-family: var(--font-aeonik);
      font-size: 14px;
      font-weight: 400;
      letter-spacing: 0.05em;
      text-transform: uppercase;
      text-decoration: none;
      padding: 12px 22px;
      border-radius: 8px;
      border: none;
      cursor: pointer;
    ">START NOW
      <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M2 12L12 2M12 2H4M12 2V10" stroke="#101010" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </a>
    <!-- Secondary CTA -->
    <a href="#" style="
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--color-dark-carbon);
      color: var(--color-ash-gray);
      font-family: var(--font-aeonik);
      font-size: 14px;
      font-weight: 400;
      letter-spacing: 0.05em;
      text-transform: uppercase;
      text-decoration: none;
      padding: 12px 22px;
      border-radius: 8px;
      border: none;
      cursor: pointer;
    ">VIEW WORK
      <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M7 2V12M7 12L3 8M7 12L11 8" stroke="#949494" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </a>
  </div>
</div>

### Service Feature Cards Grid
- **html**: <div style="
  --color-midnight-void: #101010;
  --color-deep-space: #080808;
  --color-polar-white: #F3F3F3;
  --color-absolute-zero: #FFFFFF;
  --color-ash-gray: #949494;
  --color-dark-carbon: #333333;
  --color-slate: #C1C1C1;
  --color-amber-glow: #E7C59A;
  --color-neon-green: #00AC5C;
  --font-aeonik: 'Inter', sans-serif;
  --font-input: 'IBM Plex Mono', monospace;
  background: var(--color-midnight-void);
  padding: 40px 0;
  width: 600px;
  box-sizing: border-box;
  font-family: var(--font-aeonik);
">
  <!-- Section header -->
  <div style="padding: 0 32px 32px; border-bottom: 1px solid var(--color-dark-carbon);">
    <h2 style="
      font-family: var(--font-aeonik);
      font-size: 34px;
      font-weight: 700;
      line-height: 1.07;
      color: var(--color-polar-white);
      margin: 0 0 10px 0;
    ">Invest Today, Stand Out Tomorrow</h2>
    <p style="
      font-family: var(--font-aeonik);
      font-size: 16px;
      font-weight: 400;
      color: var(--color-ash-gray);
      margin: 0;
      line-height: 1.5;
    ">We're currently working across next-gen sectors, including AI, Web3, and biopharma.</p>
  </div>

  <!-- 2x2 grid -->
  <div style="display: grid; grid-template-columns: 1fr 1fr; border-bottom: 1px solid var(--color-dark-carbon);">
    
    <!-- Card 1 -->
    <div style="
      padding: 28px 28px;
      border-right: 1px solid var(--color-dark-carbon);
      border-bottom: 1px solid var(--color-dark-carbon);
    ">
      <div style="margin-bottom: 20px;">
        <svg width="26" height="26" viewBox="0 0 26 26" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M5 21L10 13L15 17L20 9" stroke="#E7C59A" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M16 5H21V10" stroke="#E7C59A" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          <circle cx="5" cy="21" r="1.5" fill="#E7C59A"/>
        </svg>
      </div>
      <h3 style="
        font-family: var(--font-aeonik);
        font-size: 14px;
        font-weight: 700;
        color: var(--color-polar-white);
        margin: 0 0 12px 0;
        letter-spacing: 0.07em;
        text-transform: uppercase;
      ">AWARD-WINNING LOGOS</h3>
      <p style="
        font-family: var(--font-aeonik);
        font-size: 15px;
        font-weight: 400;
        color: var(--color-ash-gray);
        margin: 0;
        line-height: 1.5;
      ">Easy to remember and distinctive logos, giving your brand a unique identity.</p>
    </div>

    <!-- Card 2 -->
    <div style="
      padding: 28px 28px;
      border-bottom: 1px solid var(--color-dark-carbon);
    ">
      <div style="margin-bottom: 20px;">
        <svg width="26" height="26" viewBox="0 0 26 26" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect x="4" y="5" width="18" height="14" rx="1" stroke="#E7C59A" stroke-width="1.5"/>
          <path d="M4 9H22" stroke="#E7C59A" stroke-width="1.5"/>
          <path d="M9 5V19" stroke="#E7C59A" stroke-width="1.5"/>
        </svg>
      </div>
      <h3 style="
        font-family: var(--font-aeonik);
        font-size: 14px;
        font-weight: 700;
        color: var(--color-polar-white);
        margin: 0 0 12px 0;
        letter-spacing: 0.07em;
        text-transform: uppercase;
      ">TIMELESS BRANDING</h3>
      <p style="
        font-family: var(--font-aeonik);
        font-size: 15px;
        font-weight: 400;
        color: var(--color-ash-gray);
        margin: 0;
        line-height: 1.5;
      ">Brand identities that drive sales and create lasting connections.</p>
    </div>

    <!-- Card 3 -->
    <div style="
      padding: 28px 28px;
      border-right: 1px solid var(--color-dark-carbon);
    ">
      <div style="margin-bottom: 20px;">
        <svg width="26" height="26" viewBox="0 0 26 26" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect x="3" y="3" width="9" height="9" rx="1" stroke="#E7C59A" stroke-width="1.5"/>
          <rect x="14" y="3" width="9" height="9" rx="1" stroke="#E7C59A" stroke-width="1.5"/>
          <rect x="3" y="14" width="9" height="9" rx="1" stroke="#E7C59A" stroke-width="1.5"/>
          <rect x="14" y="14" width="9" height="9" rx="1" stroke="#E7C59A" stroke-width="1.5"/>
        </svg>
      </div>
      <h3 style="
        font-family: var(--font-aeonik);
        font-size: 14px;
        font-weight: 700;
        color: var(--color-polar-white);
        margin: 0 0 12px 0;
        letter-spacing: 0.07em;
        text-transform: uppercase;
      ">WEBSITES THAT CONVERT</h3>
      <p style="
        font-family: var(--font-aeonik);
        font-size: 15px;
        font-weight: 400;
        color: var(--color-ash-gray);
        margin: 0;
        line-height: 1.5;
      ">World-class UX/UI and development for high-impact websites.</p>
    </div>

    <!-- Card 4 -->
    <div style="padding: 28px 28px;">
      <div style="margin-bottom: 20px;">
        <svg width="26" height="26" viewBox="0 0 26 26" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M3 13H8L11 6L15 20L18 13H23" stroke="#E7C59A" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <h3 style="
        font-family: var(--font-aeonik);
        font-size: 14px;
        font-weight: 700;
        color: var(--color-polar-white);
        margin: 0 0 12px 0;
        letter-spacing: 0.07em;
        text-transform: uppercase;
      ">3D &amp; ANIMATIONS</h3>
      <p style="
        font-family: var(--font-aeonik);
        font-size: 15px;
        font-weight: 400;
        color: var(--color-ash-gray);
        margin: 0;
        line-height: 1.5;
      ">Dynamic 3D designs and animations to bring your brand to life.</p>
    </div>
  </div>
</div>

### Why Hyperstudio Manifesto Block
- **html**: <div style="
  --color-midnight-void: #101010;
  --color-deep-space: #080808;
  --color-polar-white: #F3F3F3;
  --color-absolute-zero: #FFFFFF;
  --color-ash-gray: #949494;
  --color-dark-carbon: #333333;
  --color-slate: #C1C1C1;
  --color-amber-glow: #E7C59A;
  --color-neon-green: #00AC5C;
  --font-aeonik: 'Inter', sans-serif;
  --font-input: 'IBM Plex Mono', monospace;
  background: var(--color-midnight-void);
  padding: 56px 40px;
  width: 600px;
  box-sizing: border-box;
  font-family: var(--font-aeonik);
  border-left: 1px solid var(--color-dark-carbon);
  border-right: 1px solid var(--color-dark-carbon);
">
  <!-- Heading -->
  <h2 style="
    font-family: var(--font-aeonik);
    font-size: 34px;
    font-weight: 700;
    color: var(--color-polar-white);
    text-align: center;
    margin: 0 0 28px 0;
    line-height: 1.07;
  ">Why Hyperstudio?</h2>

  <!-- First paragraph (bright) -->
  <p style="
    font-family: var(--font-aeonik);
    font-size: 16px;
    font-weight: 400;
    color: var(--color-polar-white);
    text-align: left;
    line-height: 1.65;
    margin: 0 0 20px 0;
  ">We started Hyperstudio because most design agencies aren't built for technology companies. They produce good work, but they rarely understand the product, the market, or the pace at which these companies operate. We thought there should be a studio that actually gets it, so we built one.</p>

  <!-- Second paragraph (muted / fading) -->
  <p style="
    font-family: var(--font-aeonik);
    font-size: 16px;
    font-weight: 400;
    color: var(--color-ash-gray);
    text-align: left;
    line-height: 1.65;
    margin: 0 0 36px 0;
  ">Before this, we built companies ourselves. We've sat on the other side of the table, hiring agencies, raising capital, shipping products. That changes how you think about design. You stop treating it as decoration and start asking what the brand needs to do.</p>

  <!-- Read Manifesto button -->
  <div style="display: flex; justify-content: center;">
    <a href="#" style="
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--color-dark-carbon);
      background-image: linear-gradient(180deg, rgba(80,80,80,0.18) 0%, rgba(0,0,0,0) 100%);
      color: var(--color-absolute-zero);
      font-family: var(--font-aeonik);
      font-size: 13px;
      font-weight: 400;
      letter-spacing: 0.07em;
      text-transform: uppercase;
      text-decoration: none;
      padding: 12px 24px;
      border-radius: 6px;
      border: 1px solid rgba(255,255,255,0.08);
      cursor: pointer;
    ">READ MANIFESTO
      <svg width="13" height="13" viewBox="0 0 13 13" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M6.5 1V12M6.5 12L2.5 8M6.5 12L10.5 8" stroke="#FFFFFF" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </a>
  </div>
</div>

### Primary Ghost Button
- **role**: Call to action button for primary actions
- **description**: Transparent background, Polar White text (#F3F3F3), no visible border, 8px radius. Text uses Aeonik, weight 400, size 16px. Example: 'START NOW'.

### Secondary Ghost Button
- **role**: Call to action button for secondary actions
- **description**: Transparent background, Ash Gray text (#949494), no visible border, 8px radius. Text uses Aeonik, weight 400, size 16px. Example: 'VIEW WORK'.

### Small Status Pill Tag
- **role**: Indicates status or limited availability
- **description**: Pill-shaped (99px radius) background in Neon Green (#00AC5C) with Polar White (#F3F3F3) text. Text uses Aeonik, weight 400, size 13px. Example: '2/5 SPOTS LEFT FOR APRIL'.

### Header Navigation Link
- **role**: Navigation items in the primary header
- **description**: Polar White text (#F3F3F3), Aeonik, weight 400, size 16px. Underline on hover. Example: 'SERVICES'.

### Header Navigation Tag
- **role**: Highlighted new navigation items
- **description**: Navigation link with an Amber Glow (#E7C59A) 'NEW' tag appended. Text uses Aeonik, weight 400, size 13px. Example: 'PORTFOLIO NEW'.

### Chat Button
- **role**: Persistent contact CTA in the header
- **description**: Black button with Absolute Zero (#FFFFFF) text (Aeonik, weight 400, size 14px), 8px radius, with small icon. No border. Example: 'LET'S CHAT'.

### Service Feature Card
- **role**: Used to highlight key service offerings
- **description**: Implied dark background on Deep Space (#080808), with Polar White (#F3F3F3) headline (Aeonik, weight 700, size 23px) and Ash Gray (#949494) body text (Aeonik, weight 400, size 16px). No explicit border or shadow, but clear visual separation through composition.

### Manifesto Button
- **role**: Secondary call to action button, typically for more information.
- **description**: Dark Carbon (#333333) background, Absolute Zero (#FFFFFF) text (Aeonik, weight 400), with a 4.5px radius. Subtle light gradient suggests a slight emboss. Example: 'READ MANIFESTO'.

## Agent Prompt Guide

### Quick Color Reference
- Text: #F3F3F3
- Background: #101010
- CTA: #333333 (background), #FFFFFF (text)
- Border: #333333
- Accent: #E7C59A

### 3-5 Example Component Prompts
1. **Create a hero section:** background #101010. Headline 'World-class branding and websites for startups.' using Aeonik, size 63px, weight 700, #F3F3F3, letterSpacing -0.011em, lineHeight 0.95. Below, add a 'START NOW' button: transparent background, Aeonik, size 16px, weight 400, #F3F3F3, 8px border-radius. Next to it, a 'VIEW WORK' button: transparent background, Aeonik, size 16px, weight 400, #949494, 8px border-radius.
2. **Generate a service feature block:** background #080808. Title 'AWARD-WINNING LOGOS' using Aeonik, size 23px, weight 700, #F3F3F3. Body text 'Easy to remember and distinctive logos, giving your brand a unique identity.' using Aeonik, size 16px, weight 400, #949494. Ensure consistent 24px padding within the block, and the block is visually separated by 64px from other content.
3. **Design a persistent header bar:** background #101010. Logo 'Hyperstudio' using Aeonik, size 18px, weight 700, #F3F3F3. Navigation links 'SERVICES', 'PROCESS' using Aeonik, size 16px, weight 400, #F3F3F3. Add a 'PORTFOLIO NEW' link: 'PORTFOLIO' using Aeonik, size 16px, weight 400, #F3F3F3; 'NEW' tag appending it with background #E7C59A, text #F3F3F3, Aeonik, size 13px, weight 400. Include a 'LET'S CHAT' button on the right: background #000000, text #FFFFFF, Aeonik, size 14px, weight 400, 8px border-radius, with an icon.
4. **Create a 'Why Hyperstudio?' section:** background #101010. Main heading 'Why Hyperstudio?' using Aeonik, size 44px, weight 700, #F3F3F3. Body text paragraph using Aeonik, size 18px, weight 400, #F3F3F3, with lineHeight 1.31. Below, add a 'READ MANIFESTO' button: background #333333, text #FFFFFF, Aeonik, size 16px, weight 400, 4.5px border-radius.
