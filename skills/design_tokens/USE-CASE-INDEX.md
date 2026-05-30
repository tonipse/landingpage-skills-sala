---
name: USE-CASE-INDEX
description: Pattern-Routing pro Section-Typ. "Wenn du X baust → siehe Y". Indexiert ALLES Bestehende (design.md, design-md/, ui_ux_pro_max, huashu_design). Keine neuen Patterns — nur Zugriff.
type: routing-index
version: 1.0
created: 2026-05-15
---

# USE-CASE-INDEX — Pattern-Routing pro Section-Typ

> **Zweck:** Statt 1.491 Zeilen `design.md` durchsuchen → hier nachschlagen welche Patterns + Brand-Refs für den aktuellen Section-Typ greifen.
>
> **Workflow:**
> 1. Section-Typ identifizieren (Hero, Belief-Busting, Process, Testimonial, etc.)
> 2. Hier nachschlagen → relevante `design.md`-Zeilen + 2-3 Brand-Refs aus `design-md/`
> 3. `ui_ux_pro_max` Prioritäten 1-2 (Accessibility, Touch) ALWAYS checken
> 4. Bauen / Polieren

---

## Tabellen-Übersicht (Quick Scan)

| Section-Typ | Primär-Patterns (design.md) | Brand-Refs (design-md/) | A11y-Critical |
|-------------|------------------------------|--------------------------|---------------|
| **Hero (Editorial)** | 3D-Card L142, Spotlight L196, Newspaper Split L258 | apple, kinfolk, monocle, hyperstudio | Touch-Target ≥44px |
| **Hero (SaaS)** | 3D-Card L142, Gradient L524, Ambient Glow L237 | linear.app, stripe, vercel, framer | Contrast 4.5:1 |
| **Hero (Luxury)** | Ambient Glow Orb L237, Gradient L524 | bugatti, apple, monocle, ferrari | Image alt-text |
| **Belief-Busting / Persuasion** | Counter L289, Card Fall L169, Editorial-Easing L457 | charlie-le-maignan, hyperstudio | Strong-Tags semantisch |
| **Process / Timeline (3-5 Schritte)** | Card Fall L169, Counter L289, Animation Curves L457 | linear.app, stripe, vercel, monocle | Mobile: stack vertikal |
| **Testimonials (Magazine-Stil)** | Newspaper Split L258, Grain L121 | kinfolk, monocle, wallpaper-projects | Citation semantisch |
| **Testimonials (SaaS-Card)** | Card Fall L169, Shadow L339 | stripe, linear.app, supabase | aria-label auf Card |
| **FAQ (Accordion)** | Transition Duration L492, Animation Curves L457 | apple, notion | aria-expanded + keyboard |
| **CTA-Section (Final)** | Spotlight L196, Gradient L524, Button System L381 | stripe, cal, vercel | Button ≥44px + Focus-Ring |
| **CTA-Button (Inline)** | Button System L381 (Primary/Secondary/Ghost) | linear.app, vercel | Hover + Focus States |
| **Stats / Numbers** | Counter L289, Animation Curves L457 | mercari, wise, revolut, mastercard | Format mit `tabular-nums` |
| **Trust-Signals / Pills** | Border Radius L367, Shadow L339 (Low) | stripe, cal, monocle | Visible focus on tab |
| **Pricing-Cards** | 3D-Card L142, Shadow L339, Newspaper Split L258 | stripe, linear.app, vercel | Compare-state aria |
| **Footer** | Spacing L312, Z-Index L508 | apple, vercel, linear.app | Skip-to-Content Link |
| **Section-Divider** | Clip-Path L566, Grain L121 | analogue, hyperstudio | Decoration only — keine Info |

---

## Detailed Routing

### 🦸 HERO — Editorial / Magazine-Style (Use für: Ute Wagner, Praxis-Coaches, Therapy/Health)

**Aus `design.md`:**
- L258 — Newspaper Split Hero (Left/Right Layout, Foto rechts)
- L196 — Spotlight Sweep (subtle Brand-Highlight)
- L457 — Animation Curves: nutze `cubic-bezier(0.22, 1, 0.36, 1)` (Editorial Premium)
- L490 — Transition Duration: `0.5s` für Hover, `0.8s` für Reveal

**Brand-Refs aus `design-md/`:**
- `kinfolk/DESIGN.md` — Pure Editorial, Whitespace, Serif-Display
- `monocle/DESIGN.md` — Magazin-Layout, Premium-Akzente
- `apple/DESIGN.md` — Spacing-System, Restraint
- `hyperstudio/DESIGN.md` — Bold Display + Italic Akzente

**Copy-Pattern:**
- Headline: Display-Serif mit `<em>` Italic-Akzent für emotionalen Punch
- Sub: Sans-Serif, max 3 Zeilen
- Trust-Row unter CTA: Sterne + Ratings + Klienten-Zahl

**Mobile-Critical:**
- Foto und Text in HTML in Lese-Reihenfolge (Text FIRST)
- `order: -1` NICHT auf Foto setzen (sonst kommt's vor Text)
- Hero-Right max-height 420px mobile, 320px small

---

### 🦸 HERO — SaaS / Product (Use für: Tech, B2B, Tools)

**Aus `design.md`:**
- L142 — 3D Card (Hero-Element mit Tiefe)
- L237 — Ambient Glow Orb (Dunkle Backgrounds)
- L524 — Gradient Recipes

**Brand-Refs:**
- `linear.app/DESIGN.md`, `stripe/DESIGN.md`, `vercel/DESIGN.md`, `framer/DESIGN.md`

---

### 💭 BELIEF-BUSTING / PERSUASION (Use für: Coaches, Mentoring, Sales-Pages)

**Aus `design.md`:**
- L289 — Counter Animation (für große dekorative Zahlen 1/2/3)
- L169 — Card Fall + Float (Einflug-Animation)
- L457 — Editorial-Easing für Drop-Animations
- L237 — Ambient Glow Orb (Aura-Pattern)

**Brand-Refs:**
- `charlie-le-maignan/DESIGN.md` — Editorial Dark mit Number-Akzenten
- `hyperstudio/DESIGN.md` — Bold Display + Belief-Quote Pattern

**Copy-Pattern:**
- 3 Beliefs (1/2/3) mit echtem Customer-Voice (aus Avatar/Kundenstimmen)
- Per Belief: Quote (Italic Display) + Rule (Gold Line) + Body (Du-Form, mit `<strong>` für Highlights)
- Closing-Frage direkt vor CTA: "Welchen davon hast du heute schon gedacht?" (konfrontativ)

**Animation-Pattern:**
- Zahl droppt mit `rotateX: -52deg, y: -110` → settle (siehe Section 4 Ute Startseite v2)
- Strikethrough auf Quote nach Drop (CSS `transform: scaleX(0→1)`, transform-origin: left)
- Gold-Underline auf `<strong>` (CSS `background-size: 0%→100% 2px`)
- Hover-Tilt + Click-Stempel-Press auf Zahl

**A11y:**
- `prefers-reduced-motion` PFLICHT — alles statisch + Endzustand zeigen
- Contrast Body-Text: mind. 4.5:1 (cream BG + grey text = checken)

---

### 🛤️ PROCESS / TIMELINE (Use für: 3-5 Schritte-Erklärung)

**Aus `design.md`:**
- L169 — Card Fall (Steps fallen rein beim Scroll)
- L289 — Counter (Numbered Circles oder Roman Numerals)
- L457 — Animation Curves: `power3.out` für settle
- L312 — Spacing System: 96px zwischen Steps Desktop, 52px Mobile

**Brand-Refs:**
- `linear.app/DESIGN.md` — Vertical Timeline mit subtilen Connectors
- `stripe/DESIGN.md` — Numbered Cards mit Side-Connector
- `monocle/DESIGN.md` — Editorial-Numerierung (Roman Numerals als Differentiation)

**Pattern-Varianten:**
- **Numbered Circles** (klassisch SaaS) — 56px solid Teal-Kreis + Number 24px
- **Roman Numerals** (Editorial Premium) — I, II, III ohne Kreis, nur Typografie
- **Connector-Line** zwischen Steps (vertikal links neben Numbers)

**Mobile:**
- Single-Column Stack
- Connector-Line bei 22px (kleiner Margin)
- Step-Padding: 40px → 24px

---

### 💬 TESTIMONIALS

**Aus `design.md`:**
- L258 — Newspaper Split (für Magazine-Stil mit Foto + Quote)
- L169 — Card Fall (für SaaS-Card-Grid)
- L121 — Grain Texture (für Editorial-Background)
- L457 — Animation Curves

**Brand-Refs (Editorial):**
- `kinfolk/DESIGN.md`, `monocle/DESIGN.md`, `wallpaper-projects/DESIGN.md`

**Brand-Refs (SaaS):**
- `stripe/DESIGN.md`, `linear.app/DESIGN.md`

**Pattern:**
- Quote in Display-Serif Italic
- Author-Block: Name (Bold) + Role (Light) + optional: Vorher/Nachher-Zahlen
- Optional Foto: Square 1:1 oder Editorial-Portrait 3:4

---

### ❓ FAQ (Accordion)

**Aus `design.md`:**
- L492 — Transition Duration (0.3s für Open/Close)
- L457 — Animation Curves: `cubic-bezier(0.22, 1, 0.36, 1)` für smooth open

**Brand-Refs:**
- `apple/DESIGN.md` — Cleanest Accordion-Implementation
- `notion/DESIGN.md` — Soft-Edges + Hover-States

**A11y-Pflicht:**
- `<details><summary>` HTML5 verwenden (native + keyboard-accessible)
- ODER: `aria-expanded`, `aria-controls`, Focus-Ring sichtbar
- Touch-Target ganzer Header ≥44px

---

### 🎯 CTA-SECTION (Final, vor Footer)

**Aus `design.md`:**
- L196 — Spotlight Sweep (für Background-Drama)
- L524 — Gradient Recipes (Gold-Background mit SVG-Noise)
- L381 — Button System (Primary = Teal oder Gold)
- L121 — Grain Texture als Overlay

**Brand-Refs:**
- `stripe/DESIGN.md`, `cal/DESIGN.md`, `vercel/DESIGN.md`

**Pattern:**
- Eyebrow ("Bereit?") + Headline (Display-Italic) + Sub + Single-Button + Apply-Meta-Pills
- Background: Gold mit SVG-Filter-Noise (statt langweiliger Solid-Color)

**A11y:**
- Button ≥44px Height
- Focus-Ring sichtbar (`:focus-visible`)
- Click-Area >Button-Visual (besser tap-baroh)

---

### 🔘 CTA-BUTTON (Inline)

**Aus `design.md`:**
- L381 — Button System (3 Varianten dokumentiert)

**Pattern-Varianten:**
- **Primary (Gold) `btn-gold btn-large`** — Wichtigster CTA, Logo-Star vor Text als Brand-Akzent (siehe Ute)
- **Secondary (Teal) `btn-teal`** — Mid-Importance
- **Ghost / Outline `btn-outline`** — Niedrig-Importance (Mehr Info, etc.)

**Hover-Pattern:**
- `transform: translateY(-1px)` + Shadow elevation step up
- `transition: 0.2s ease`

**Mobile:**
- Full-Width unter 480px Single-Column Mobile (vermeidet zu kleine Tap-Areas)

---

### 📊 STATS / NUMBERS

**Aus `design.md`:**
- L289 — Counter Animation (Zahlen zählen hoch beim Scroll-Reveal)
- L457 — Animation Curves

**Brand-Refs:**
- `mercari/DESIGN.md`, `wise/DESIGN.md`, `revolut/DESIGN.md`, `mastercard/DESIGN.md`

**Pattern:**
- Big Number in Display-Serif (oder Sans Bold)
- `font-variant-numeric: tabular-nums` für stabile Breite während Animation
- Label klein darunter (Caps + Letter-Spacing)

**A11y:**
- Wenn Counter animiert: aria-live="polite" auf Container ODER aria-hidden auf der animation + sichtbarer End-Wert für Screenreader

---

### 🛡️ TRUST-SIGNALS / PILLS

**Aus `design.md`:**
- L367 — Border Radius Scale (`pill` = 999px)
- L339 — Shadow Elevation (Low = 1)

**Brand-Refs:**
- `stripe/DESIGN.md`, `cal/DESIGN.md`, `monocle/DESIGN.md`

**Pattern:**
- Pill mit `border-radius: 999px`
- Icon-Pre (z.B. Stern, Check, Logo-Marker) + Text
- Höhe: 32-40px, Padding: 8-12px horizontal

---

### 💰 PRICING-CARDS

**Aus `design.md`:**
- L142 — 3D Card (für Highlight-Tier)
- L339 — Shadow Elevation (Levels 2-3)
- L258 — Newspaper Split (für 2-Tier Vergleich)

**Brand-Refs:**
- `stripe/DESIGN.md`, `linear.app/DESIGN.md`, `vercel/DESIGN.md`

---

### 🦶 FOOTER

**Aus `design.md`:**
- L312 — Spacing System
- L508 — Z-Index Layering

**Brand-Refs:**
- `apple/DESIGN.md`, `vercel/DESIGN.md`, `linear.app/DESIGN.md`

**Pattern:**
- Logo + Tagline links
- Link-Spalten rechts (4-5 Spalten Desktop, 2 Mobile)
- Bottom-Bar: Legal-Links + Copyright + Newsletter (optional)

---

### 🎚️ SECTION-DIVIDER (Übergang zwischen Sections)

**Aus `design.md`:**
- L566 — Clip-Path Diagonal (2025 Trend)
- L121 — Grain Texture (für Editorial-Übergang)

**Brand-Refs:**
- `analogue/DESIGN.md`, `hyperstudio/DESIGN.md`

---

## 🎨 GLOBAL PATTERNS (Section-übergreifend)

### Color-Palette per Vibe
→ `design.md` L35-89 (8 dokumentierte Paletten) + L608-634 (2025 Warm Trends)

| Vibe | Palette aus design.md |
|------|------------------------|
| Editorial Cream (Ute) | "Editorial Cream + Teal + Gold" L35 |
| Dark Luxury (GODIA) | "Dark Editorial" L648+ |
| SaaS Light | "Stripe-style Light" |
| Warm Premium | L608-634 (2025) |

### Font-Pairs per Use-Case
→ `design.md` L90-120 + L587-607 (2025 neue Pairs)

| Vibe | Pair |
|------|------|
| Editorial Magazine | Fraunces + DM Sans |
| SaaS Tech | Inter + Inter |
| Luxury | Cormorant + Inter |
| Bold Editorial | Fraunces Italic + DM Sans |

### Animation-Vokabular (Page-DNA)
→ `design.md` L457-491

**Editorial Premium DNA (Ute, Magazine):**
- Easing: `cubic-bezier(0.22, 1, 0.36, 1)` für Hover/Reveal
- Duration: 0.5s Hover, 0.7-0.85s Reveal, 1.2-1.4s long
- KEINE Bounce-Eases auf hochwertigen Brands

**SaaS Snappy DNA (Linear, Stripe):**
- Easing: `cubic-bezier(0.4, 0, 0.2, 1)` (Material standard)
- Duration: 0.2-0.3s alle Interactions

---

## ❌ AI-Slop Blacklist (NIE verwenden)
→ `design.md` L17-28 (Vollständige Liste)

Kurz-Quick-Check:
- ❌ `background-attachment: fixed` (iOS broken)
- ❌ `margin/top/left` animieren (nur `transform` + `opacity`)
- ❌ Emojis als Icons
- ❌ Generische Glassmorphism ohne Kontext
- ❌ Bouncy Eases auf Editorial-Brands
- ❌ Gedankenstriche (—) als Stilmittel im Copy (AI-Tell #1)
- ❌ Drop-Shadow auf Cream/Light Backgrounds (Glow nicht sichtbar)

---

## 🔗 Cross-References

- **Brand-Library Index:** `design-md/_INDEX.md` (106 Brands, Quick-Pick by Use-Case)
- **UI/UX Rules:** `ui_ux_pro_max/SKILL.md` (10 Prioritäten 1-6 = CRITICAL/HIGH)
- **Design-Philosophy:** `huashu_design/SKILL.md` (Asset-First, Fact-Verification)
- **Onboarding:** `_universal/ONBOARDING.md` (5 Pflicht-Dimensionen vor Build)
- **Workflow:** `_universal/SECTION-BUILD-WORKFLOW.md` (Checklisten)
- **Lessons:** `[skill]/LESSONS.md` per Skill (was wir gelernt haben)

---

## Wie diesen Index aktualisieren

**Beim Section-Build oder -Polish:**
- Neue Patterns entdeckt? → unten an entsprechenden Section-Typ anhängen
- Battle-tested Variante? → mit `✅ proven` markieren
- Funktioniert NICHT? → mit `⚠️ riskant` markieren

**Quartalsweise:**
- Brand-Library `design-md/` Refresh (neue Top-Brands hinzufügen)
- 2025/2026 Trend-Updates in `design.md` einpflegen
