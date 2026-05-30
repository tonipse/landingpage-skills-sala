---
version: alpha
source: refero
source_id: 9e2dceb8-0c87-45db-8830-9df961b02b32
source_url: https://dezeen.com
name: Dezeen
description: "The Dezeen design system presents an editorial aesthetic, blending classic serif typography with a modern sans-serif for a distinctive voice. Dominant black text on bright white surfaces creates crisp readability, while the signature 'Indigo Accent' (#556e9b) injects a cool, authoritative hue across key interactive elements and titles. The layout emphasizes content separation and clear hierarchy, utilizing subtle borders and generous vertical spacing to frame articles and navigation."
theme: light
northStar: "Architectural Blueprint on Crisp White. This metaphor evokes the precision and clarity of architectural drawings and the pristine nature of a fresh page."
category: editorial
tags: ["monochromatic", "editorial", "high-contrast", "sharp-edges", "classic-modern", "text-heavy", "content-focused", "architectural"]

colors:
  pitch-black: "#000000"  # neutral — Primary text, core UI elements, bold borders — forms the backbone of the typographic hiera
  pure-white: "#ffffff"  # neutral — Page backgrounds, card surfaces, input fields — provides expansive canvas for content and 
  fog-gray: "#f0f0f0"  # neutral — Subtle background for UI sections, list backgrounds — offers a soft visual break from pure
  silver-ash: "#d8d8d8"  # neutral — Secondary backgrounds, subtle borders, inactive link states — provides subdued contrast fo
  concrete-gray: "#757575"  # neutral — Subtle text, secondary links — used for less prominent textual information, such as timest
  soft-stone: "#eaeaea"  # neutral — Navigation backgrounds, dividers — a slightly darker off-white for structural elements.
  indigo-accent: "#556e9b"  # brand — Key headings, interactive links, active navigation, subtle button borders — establishes br
  sunset-orange: "#ff7617"  # accent — Accent for certain links, potentially call-to-action highlights — adds a vibrant, warm con

typography:
  standardct:
    family: "StandardCT"
    sizes: "19px, 27px, 40px"
    weight: "700"
    lineHeight: "0.95, 1.00, 1.10, 1.20, 1.25, 1.37, 1.38"
    substitute: "Open Sans, Montserrat"
    use: "Display and primary headings. The bold, all-caps presentation at larger sizes commands attention, while the specific font-feature-settings ensure stylistic consistency with the brand's custom type, pr"
  chronicle-text-g1-a:
    family: "Chronicle Text G1 A"
    sizes: "14px, 16px"
    weight: "400, 700"
    lineHeight: "1.23, 1.25, 1.29, 1.50"
    substitute: "Georgia, Merriweather"
    use: "Body copy, article content, secondary headings, and general UI text. This serif font provides a classic, readable foundation for lengthy editorial content, distinguishing it from the sans-serif headin"
  arial:
    family: "Arial"
    sizes: "13px, 14px, 16px"
    weight: "400, 700"
    lineHeight: "1.00, 1.20, 1.29"
    substitute: "Helvetica Neue"
    use: "System fallback for UI elements, labels, and minor interactive components where a clean, straightforward sans-serif is required."
---

# Dezeen — Design System

> Architectural Blueprint on Crisp White. This metaphor evokes the precision and clarity of architectural drawings and the pristine nature of a fresh page.


The Dezeen design system presents an editorial aesthetic, blending classic serif typography with a modern sans-serif for a distinctive voice. Dominant black text on bright white surfaces creates crisp readability, while the signature 'Indigo Accent' (#556e9b) injects a cool, authoritative hue across key interactive elements and titles. The layout emphasizes content separation and clear hierarchy, utilizing subtle borders and generous vertical spacing to frame articles and navigation.


## Type Scale

- role: body · size: 14 · lineHeight: 1.29
- role: body-lg · size: 16 · lineHeight: 1.25
- role: subheading · size: 19 · lineHeight: 1.38
- role: heading · size: 27 · lineHeight: 1.2
- role: display · size: 40 · lineHeight: 1.1

## Color Palette


### Neutral
- **Pitch Black** `#000000` — Primary text, core UI elements, bold borders — forms the backbone of the typographic hierarchy and defines structure.
- **Pure White** `#ffffff` — Page backgrounds, card surfaces, input fields — provides expansive canvas for content and ensures high contrast.
- **Fog Gray** `#f0f0f0` — Subtle background for UI sections, list backgrounds — offers a soft visual break from pure white without introducing chromatic noise.
- **Silver Ash** `#d8d8d8` — Secondary backgrounds, subtle borders, inactive link states — provides subdued contrast for secondary content.
- **Concrete Gray** `#757575` — Subtle text, secondary links — used for less prominent textual information, such as timestamps or meta-information.
- **Soft Stone** `#eaeaea` — Navigation backgrounds, dividers — a slightly darker off-white for structural elements.

### Brand
- **Indigo Accent** `#556e9b` — Key headings, interactive links, active navigation, subtle button borders — establishes brand identity and guides user attention.

### Accent
- **Sunset Orange** `#ff7617` — Accent for certain links, potentially call-to-action highlights — adds a vibrant, warm contrast.

## Layout

The page maintains a centered max-width of 1212px for its core content, providing a contained reading experience. The hero section often presents a split layout, with a prominent image juxtaposed against a large headline. Content sections follow a vertical rhythm, with consistent spacing of 9px to 11px between elements and an implied 48px between major sections. Articles typically arrange text and images in alternating left-right or stacked configurations. Navigation consists of a sticky top bar with a search utility and prominent category links, supplemented by a left sidebar for 'Highlights' and 'Most Popular' sections creating a multi-column editorial structure. The layout prioritizes clear content separation and readability.


## Imagery

This site prominently features photography within article cards and hero sections, often displayed full-bleed within its content blocks (0px padding, no radius). The photography style is varied, encompassing product shots, architectural exteriors and interiors, and landscape vistas, but generally leans towards high-quality, professional imagery that serves to illustrate content more than set a specific mood. Photos are contained, not overlapping, and appear without masks or special treatments. Density is moderate, balancing visual interest with text-dominant article layouts. Icons are minimal, typically monochrome, and integrated subtly for navigation or interaction.


## Spacing

- **radius**: {'cards': '0px', 'inputs': '0px', 'buttons': '0px', 'accentCircular': '100%'}
- **elementGap**: 9px
- **sectionGap**: 48px
- **cardPadding**: 0px
- **pageMaxWidth**: 1212px

## Do

- Use 'Pitch Black' (#000000) for all primary body text and 'Pure White' (#ffffff) for all main backgrounds to ensure high contrast and readability.
- Apply 'Indigo Accent' (#556e9b) exclusively to key interactive elements like links, active navigation items, and prominent headings to guide user focus.
- Reserve the 'Circular Play Button' style for media controls, emphasizing its unique shape against the otherwise angular design.
- Maintain 0px border-radius for all cards and input fields to uphold the sharp, architectural aesthetic.
- Utilize 'Chronicle Text G1 A' for all long-form editorial content at 14px or 16px with appropriate line heights (1.23-1.50) for optimal legibility.
- Employ 'StandardCT' (weight 700) for all main headings and titles, leveraging its strong editorial presence.
- Ensure generous vertical spacing, typically in multiples of 9px or 11px, between content blocks to create a comfortable density and clear content hierarchy.

## Don't

- Do not use shadow for card elevation; rely on clear borders or background color shifts where visible.
- Avoid decorative rounded corners on any elements other than specific circular buttons, as it contradicts the sharp, precise aesthetic.
- Do not introduce new chromatic colors unless explicitly defined as an accent; the palette is tightly controlled.
- Never use 'Arial' for main headings or body text; reserve it for minor UI elements or as a system fallback.
- Do not use excessive letter-spacing; all specified fonts use 'normal' letter-spacing to maintain typographic integrity.

## Components


### Newsletter Signup Modal
- **html**: <style>
  :root {
    --color-pitch-black: #000000;
    --color-pure-white: #ffffff;
    --color-fog-gray: #f0f0f0;
    --color-silver-ash: #d8d8d8;
    --color-concrete-gray: #757575;
    --color-soft-stone: #eaeaea;
    --color-indigo-accent: #556e9b;
    --color-sunset-orange: #ff7617;
    --font-standardct: 'Open Sans', Montserrat, sans-serif;
    --font-chronicle-text-g1-a: Georgia, Merriweather, serif;
    --font-arial: Arial, 'Helvetica Neue', sans-serif;
  }
</style>
<div style="width:600px;background:var(--color-pure-white);font-family:var(--font-arial);box-sizing:border-box;">
  <!-- Image banner -->
  <div style="width:100%;height:230px;background:linear-gradient(180deg,#7baac4 0%,#4a6a8a 30%,#2c3a2e 70%,#1a1a1a 100%);position:relative;overflow:hidden;">
    <!-- Dezeen logo -->
    <div style="position:absolute;top:20px;left:24px;">
      <span style="font-family:var(--font-standardct);font-weight:700;font-size:22px;color:var(--color-pure-white);letter-spacing:-0.5px;line-height:1;">de<br>zeen</span>
    </div>
    <!-- Airstream trailer placeholder -->
    <div style="position:absolute;bottom:30px;left:50%;transform:translateX(-50%);width:180px;height:80px;background:rgba(200,200,200,0.85);border-radius:40px 40px 6px 6px;">
      <div style="position:absolute;bottom:0;left:10px;width:30px;height:30px;background:#888;border-radius:50%;"></div>
      <div style="position:absolute;bottom:0;right:10px;width:30px;height:30px;background:#888;border-radius:50%;"></div>
    </div>
    <!-- Headline overlay -->
    <div style="position:absolute;bottom:0;left:0;right:0;padding:18px 24px;">
      <p style="font-family:var(--font-standardct);font-weight:700;font-size:27px;color:var(--color-pure-white);margin:0;line-height:1.2;text-align:center;">Sign up to a Dezeen newsletter today</p>
    </div>
  </div>
  <!-- Form area -->
  <div style="background:var(--color-fog-gray);padding:24px 24px 28px 24px;display:flex;align-items:center;gap:16px;">
    <input
      type="email"
      placeholder="Email"
      style="flex:1;height:44px;background:var(--color-pure-white);color:var(--color-pitch-black);border:1.5px solid var(--color-indigo-accent);border-radius:0;font-family:var(--font-arial);font-size:16px;padding:0 10px;outline:none;box-sizing:border-box;"
    />
    <button style="background:transparent;border:none;cursor:pointer;font-family:var(--font-standardct);font-weight:700;font-size:22px;color:var(--color-pitch-black);padding:0;white-space:nowrap;">Next</button>
  </div>
</div>

### Article Card List
- **html**: <style>
  :root {
    --color-pitch-black: #000000;
    --color-pure-white: #ffffff;
    --color-fog-gray: #f0f0f0;
    --color-silver-ash: #d8d8d8;
    --color-concrete-gray: #757575;
    --color-soft-stone: #eaeaea;
    --color-indigo-accent: #556e9b;
    --color-sunset-orange: #ff7617;
    --font-standardct: 'Open Sans', Montserrat, sans-serif;
    --font-chronicle-text-g1-a: Georgia, Merriweather, serif;
    --font-arial: Arial, 'Helvetica Neue', sans-serif;
  }
</style>
<div style="width:600px;background:var(--color-pure-white);padding:0;font-family:var(--font-chronicle-text-g1-a);box-sizing:border-box;">
  <!-- Article 1 -->
  <div style="display:flex;gap:16px;padding:20px 0;border-bottom:1px solid var(--color-soft-stone);">
    <div style="flex:1;min-width:0;">
      <h2 style="font-family:var(--font-chronicle-text-g1-a);font-weight:700;font-size:19px;color:var(--color-pitch-black);margin:0 0 8px 0;line-height:1.25;">DSDHA prioritises "elegant frugality" in Henry Moore Studios gallery revamp</h2>
      <p style="font-family:var(--font-chronicle-text-g1-a);font-size:14px;color:var(--color-pitch-black);margin:0 0 10px 0;line-height:1.5;">London studio <a href="#" style="color:var(--color-indigo-accent);text-decoration:none;">DSDHA</a> has renovated Sheep Field Barn, a <a href="#" style="color:var(--color-indigo-accent);text-decoration:none;">gallery</a> at Henry Moore Studios &amp; Gardens in Hertfordshire, UK, updating exhibitions while introducing workshop spaces.</p>
      <p style="font-family:var(--font-arial);font-size:13px;color:var(--color-concrete-gray);margin:0;"><a href="#" style="color:var(--color-indigo-accent);text-decoration:none;">Lizzie Crook</a> | 1 hour ago | 3 comments</p>
    </div>
    <div style="width:140px;flex-shrink:0;">
      <div style="width:140px;height:105px;background:var(--color-silver-ash);"></div>
    </div>
  </div>
  <!-- Article 2 -->
  <div style="display:flex;gap:16px;padding:20px 0;border-bottom:1px solid var(--color-soft-stone);">
    <div style="flex:1;min-width:0;">
      <h2 style="font-family:var(--font-chronicle-text-g1-a);font-weight:700;font-size:19px;color:var(--color-pitch-black);margin:0 0 8px 0;line-height:1.25;">Brutalist Korea presents "nu-bru" buildings from Seoul to Jeju Island</h2>
      <p style="font-family:var(--font-chronicle-text-g1-a);font-size:14px;color:var(--color-pitch-black);margin:0 0 10px 0;line-height:1.5;">New <a href="#" style="color:var(--color-indigo-accent);text-decoration:none;">book</a> Brutalist Korea showcases designs ranging from a blocky <a href="#" style="color:var(--color-indigo-accent);text-decoration:none;">kindergarten</a> to a building designed to "conjure the image of a cloud in the sky."</p>
      <p style="font-family:var(--font-arial);font-size:13px;color:var(--color-concrete-gray);margin:0;"><a href="#" style="color:var(--color-indigo-accent);text-decoration:none;">Ellen Eberhardt</a> | 15 hours ago | <a href="#" style="color:var(--color-indigo-accent);text-decoration:none;">17 comments</a></p>
    </div>
    <div style="width:140px;flex-shrink:0;">
      <div style="width:140px;height:105px;background:var(--color-silver-ash);"></div>
    </div>
  </div>
  <!-- Article 3 -->
  <div style="display:flex;gap:16px;padding:20px 0;">
    <div style="flex:1;min-width:0;">
      <h2 style="font-family:var(--font-chronicle-text-g1-a);font-weight:700;font-size:19px;color:var(--color-pitch-black);margin:0 0 8px 0;line-height:1.25;">This week BIG revealed dramatic rammed-earth villas in Japan</h2>
      <p style="font-family:var(--font-chronicle-text-g1-a);font-size:14px;color:var(--color-pitch-black);margin:0 0 10px 0;line-height:1.5;"><a href="#" style="color:var(--color-indigo-accent);text-decoration:none;">This week on Dezeen</a>, Danish studio BIG unveiled sweeping rammed-earth villas on the shores of Japan, a project which marks the studio's first built work in Asia.</p>
      <p style="font-family:var(--font-arial);font-size:13px;color:var(--color-concrete-gray);margin:0;"><a href="#" style="color:var(--color-indigo-accent);text-decoration:none;">Cajsa Carlson</a> | 6 hours ago | 9 comments</p>
    </div>
    <div style="width:140px;flex-shrink:0;">
      <div style="width:140px;height:105px;background:var(--color-silver-ash);"></div>
    </div>
  </div>
</div>

### Most Commented Sidebar Block
- **html**: <style>
  :root {
    --color-pitch-black: #000000;
    --color-pure-white: #ffffff;
    --color-fog-gray: #f0f0f0;
    --color-silver-ash: #d8d8d8;
    --color-concrete-gray: #757575;
    --color-soft-stone: #eaeaea;
    --color-indigo-accent: #556e9b;
    --color-sunset-orange: #ff7617;
    --font-standardct: 'Open Sans', Montserrat, sans-serif;
    --font-chronicle-text-g1-a: Georgia, Merriweather, serif;
    --font-arial: Arial, 'Helvetica Neue', sans-serif;
  }
</style>
<div style="width:600px;background:var(--color-pure-white);font-family:var(--font-chronicle-text-g1-a);box-sizing:border-box;padding:0;">
  <!-- Section header -->
  <div style="display:flex;align-items:center;justify-content:space-between;padding:10px 0 12px 0;border-bottom:2px solid var(--color-pitch-black);margin-bottom:0;">
    <h2 style="font-family:var(--font-standardct);font-weight:700;font-size:19px;color:var(--color-pitch-black);margin:0;text-transform:uppercase;letter-spacing:0;">Most commented</h2>
  </div>
  <!-- Item 1 -->
  <div style="display:flex;align-items:flex-start;gap:14px;padding:14px 0;border-bottom:1px solid var(--color-soft-stone);">
    <span style="font-family:var(--font-standardct);font-weight:700;font-size:27px;color:var(--color-silver-ash);line-height:1;min-width:28px;">1</span>
    <div style="flex:1;">
      <a href="#" style="font-family:var(--font-chronicle-text-g1-a);font-weight:700;font-size:15px;color:var(--color-pitch-black);text-decoration:none;line-height:1.4;display:block;">Toronto completes one of largest North American underground rail lines in decades</a>
    </div>
    <div style="width:72px;flex-shrink:0;">
      <div style="width:72px;height:54px;background:var(--color-silver-ash);"></div>
    </div>
  </div>
  <!-- Item 2 -->
  <div style="display:flex;align-items:flex-start;gap:14px;padding:14px 0;border-bottom:1px solid var(--color-soft-stone);">
    <span style="font-family:var(--font-standardct);font-weight:700;font-size:27px;color:var(--color-silver-ash);line-height:1;min-width:28px;">2</span>
    <div style="flex:1;">
      <a href="#" style="font-family:var(--font-chronicle-text-g1-a);font-weight:700;font-size:15px;color:var(--color-pitch-black);text-decoration:none;line-height:1.4;display:block;">Nine European houses that reinterpret local architecture</a>
    </div>
    <div style="width:72px;flex-shrink:0;">
      <div style="width:72px;height:54px;background:var(--color-silver-ash);"></div>
    </div>
  </div>
  <!-- Item 3 -->
  <div style="display:flex;align-items:flex-start;gap:14px;padding:14px 0;border-bottom:1px solid var(--color-soft-stone);">
    <span style="font-family:var(--font-standardct);font-weight:700;font-size:27px;color:var(--color-silver-ash);line-height:1;min-width:28px;">3</span>
    <div style="flex:1;">
      <a href="#" style="font-family:var(--font-chronicle-text-g1-a);font-weight:700;font-size:15px;color:var(--color-pitch-black);text-decoration:none;line-height:1.4;display:block;">Omar Gandhi Architects carve cedar lake house into Canadian hillside</a>
    </div>
    <div style="width:72px;flex-shrink:0;">
      <div style="width:72px;height:54px;background:var(--color-silver-ash);"></div>
    </div>
  </div>
  <!-- Item 4 -->
  <div style="display:flex;align-items:flex-start;gap:14px;padding:14px 0;border-bottom:1px solid var(--color-soft-stone);">
    <span style="font-family:var(--font-standardct);font-weight:700;font-size:27px;color:var(--color-silver-ash);line-height:1;min-width:28px;">4</span>
    <div style="flex:1;">
      <a href="#" style="font-family:var(--font-chronicle-text-g1-a);font-weight:700;font-size:15px;color:var(--color-pitch-black);text-decoration:none;line-height:1.4;display:block;">Goldstein Heather doubles home's footprint with four-storey extension</a>
    </div>
    <div style="width:72px;flex-shrink:0;">
      <div style="width:72px;height:54px;background:var(--color-silver-ash);"></div>
    </div>
  </div>
  <!-- Item 5 -->
  <div style="display:flex;align-items:flex-start;gap:14px;padding:14px 0;">
    <span style="font-family:var(--font-standardct);font-weight:700;font-size:27px;color:var(--color-silver-ash);line-height:1;min-width:28px;">5</span>
    <div style="flex:1;">
      <a href="#" style="font-family:var(--font-chronicle-text-g1-a);font-weight:700;font-size:15px;color:var(--color-pitch-black);text-decoration:none;line-height:1.4;display:block;">Marc Joseph develops mop with integrated water-suction mechanism</a>
    </div>
    <div style="width:72px;flex-shrink:0;">
      <div style="width:72px;height:54px;background:var(--color-silver-ash);"></div>
    </div>
  </div>
</div>

### Circular Play Button
- **role**: Interaction
- **description**: Small, circular button with a black background (#000000) and an 'Indigo Accent' (#556e9b) border and text. Fully rounded (borderRadius: 50%) with no padding specified, implying a contained icon. This button is used for media playback, distinguished by its unique circular shape against a predominantly angular UI.

### Underlined Text Button
- **role**: Navigation/Action
- **description**: Transparent background (rgba(0,0,0,0)) with 'Pitch Black' (#000000) text and border color. No border-radius. Minimal vertical padding (1px top/bottom, 6px sides). Used for text-based actions or links within content, maintaining a subtle presence.

### Circular Highlight Button
- **role**: Accent/Icon
- **description**: Small, circular button with 'Silver Ash' (#dddddd) background and 'Pure White' (#ffffff) text. Fully rounded (borderRadius: 100%) with 5px padding on all sides. Used for prominent, small interactive elements or icons.

### Article Card
- **role**: Content Display
- **description**: Transparent background with no border-radius or box-shadow, relying on text and image content for definition. No padding, implying content extends to edges. Used for displaying articles in lists or grids, maintaining a clean, unadorned presentation.

### Newsletter Input Field
- **role**: Form Input
- **description**: Pure White (#ffffff) background with 'Pitch Black' (#000000) text and border. No border-radius, presenting a sharp, functional appearance. Features 0px top/bottom padding and 5px horizontal padding. Used for email subscription forms.

## Agent Prompt Guide

### Quick Color Reference
- Text: #000000
- Background: #ffffff
- CTA: #556e9b
- Border: #000000 (primary), #556e9b (accent)
- Accent: #ff7617

### 3-5 Example Component Prompts
1. Create a primary headline: Text 'Milan design week must-sees', font 'StandardCT', weight 700, size 40px, lineHeight 1.1, color #000000, fontFeatureSettings '"calt" 0, "kern", "liga" 0'.
2. Design an article body paragraph: Text 'London studio about DSDHA prioritises "elegant frugality" in Henry Moore Studios gallery revamp', font 'Chronicle Text G1 A', weight 400, size 16px, lineHeight 1.25, color #000000.
3. Make an interactive text link: Text 'Highlights', font 'Chronicle Text G1 A', weight 400, size 14px, color #556e9b, with a subtle 1px #556e9b border on hover.
4. Build a newsletter input field: 'Pure White' (#ffffff) background, 'Pitch Black' (#000000) text and 1px border. No border-radius. Padding 0px top/bottom, 5px left/right. Placeholder text 'Email' in #000000 color.
5. Assemble an Article Card: Transparent background, no border-radius. Contains an image at the top (no corner radius), followed by a 'subheading' in 'StandardCT' and a 'body' text in 'Chronicle Text G1 A'. No internal padding for the card container.
