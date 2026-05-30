---
name: VISUAL-DIRECTIONS
description: 7 kuratierte Default-Visual-Directions als Auswahl-Vorlage. Schneller Kickoff für neue Brand-Builds wenn Visual-Identity noch unklar ist. Inspiriert von nexu-io/open-design's "5 Visual Directions"-Pattern + 2026 Markt-Trends (Kinetic/Liquid, Anti-AI Tactile).
type: visual-template-library
version: 1.1
created: 2026-05-15
updated: 2026-05-19
trigger: Wenn neuer Kunde Brand-Vibe nicht klar definiert hat
---

# VISUAL-DIRECTIONS — 7 Default-Directions zur Auswahl

> **Zweck:** Statt "irgendwas Schönes" bauen → 5 kuratierte, battle-tested Directions. User wählt eine → klarer Kickoff-Punkt.
>
> **Wann nutzen:**
> - Neuer Kunde, Brand-Identity nicht festgelegt
> - Mehrere Konzept-Varianten zur Auswahl gewünscht
> - "Probier mal ein paar Stile aus"-Briefing
>
> **Wann NICHT nutzen:**
> - Bestehende Brand mit klarer Visual-Identity → diese verwenden
> - Asset-Protokoll aus `huashu_design/SKILL.md` existiert bereits

---

## DIRECTION 1 — EDITORIAL MAGAZINE

**Vibe:** Hochwertig, ruhig, viel Whitespace, italic-Akzente. Wirkt wie ein Premium-Lifestyle-Magazin.

**Ideal für:** Personenmarken, Coaches/Mentor:innen, Therapy/Health, Healing, Hochpreis-Consulting.

**Reference-Brands (aus `design-md/`):**
- kinfolk, monocle, charlie-le-maignan, hyperstudio, wallpaper-projects

**Beispiel-Implementation in unserem System:**
- UTE Wagner Startseite v2 (Cream + Teal + Gold)
- UTE Karriere-Page (`utewagner.de/karriere-vertrieb/`)

### Tokens

```yaml
colors:
  background: "#f5f2ec"     # Cream
  background-soft: "#efebe2"
  text-primary: "#1a1a1a"
  text-light: "#6b6b6b"
  brand-primary: "#2a6b6e"  # Teal
  brand-deeper: "#133539"
  accent: "#c9a87a"          # Gold

fonts:
  display: "Fraunces"        # Variable Serif, italic-friendly
  body: "DM Sans"

spacing:
  section-y: 120px
  section-y-mobile: 72px

animation:
  ease: "cubic-bezier(0.22, 1, 0.36, 1)"
  hover-duration: 0.5s
  reveal-duration: 0.8s
```

### Pattern-Hinweise
- **Headlines:** Display-Serif mit `<em>` Italic-Akzent (z.B. *„Mehr Freizeit."*)
- **Section-Padding:** großzügig (120px Y Desktop)
- **Numbers:** Big decorative italic numbers als visueller Anker
- **Hover:** subtle rotate (-4° to -8°) + lift 4-6px
- **KEINE Bouncy-Eases**
- **Bilder:** Editorial-Portraits, kein Stock

### Wann NICHT verwenden
- B2B-SaaS-Produkte (zu warm/personal)
- Mass-Market mit niedrigem Trust-Need

---

## DIRECTION 2 — MODERN MINIMAL

**Vibe:** Strict, clean, monochrom mit 1-2 Akzentfarben. Wirkt premium-tech, restraint, Apple-esque.

**Ideal für:** Tech-Brands, Premium-Products, Pure-Service-Businesses, Professional-Consulting.

**Reference-Brands (aus `design-md/`):**
- apple, notion, linear.app, framer, cal

**Beispiel-Use:** Coaches mit Tech-Background, Premium-Services, Architecten/Design-Studios

### Tokens

```yaml
colors:
  background: "#ffffff"
  background-soft: "#f5f5f7"
  text-primary: "#000000"
  text-light: "#86868b"
  brand-primary: "#0066cc"   # accent (or any single accent)
  border: "#d2d2d7"

fonts:
  display: "Inter"           # or SF Pro Display
  body: "Inter"

spacing:
  section-y: 96px
  section-y-mobile: 56px

animation:
  ease: "cubic-bezier(0.4, 0, 0.2, 1)"  # Material-style
  hover-duration: 0.3s
  reveal-duration: 0.6s
```

### Pattern-Hinweise
- **Layout:** strict Grid (12-col), generous Gutters
- **Typography:** primarily Sans, viel Hierarchy via Size/Weight (nicht Color)
- **Color:** monochromatic + 1 Akzent — kein Rainbow
- **Hover:** subtle scale (1.02) + opacity change, kein Rotate
- **Shadows:** sehr dezent (kein blur >20px)
- **Spacing:** strict 8px-Grid

### Wann NICHT verwenden
- Emotionale Brands (Therapy, Coaching, Healing)
- Bunte/Lifestyle-Brands

---

## DIRECTION 3 — TECH UTILITY

**Vibe:** Dark Mode default, Gradient-Akzente, Monospace-Touches, Dev-First. Wirkt wie ein Tool für Developer/Power-User.

**Ideal für:** SaaS-Tools, Developer-Products, API-Services, B2B-Tech, AI-Tools.

**Reference-Brands (aus `design-md/`):**
- stripe, vercel, linear.app, supabase, clickhouse, cohere

**Beispiel-Use:** Internal-Tools, Developer-Marketing-Sites, AI-Product-LPs

### Tokens

```yaml
colors:
  background: "#0a0a0a"      # Dark base
  background-soft: "#1a1a1a"
  text-primary: "#ffffff"
  text-light: "#a1a1aa"
  brand-primary: "#7c3aed"   # vibrant accent
  gradient: "linear-gradient(135deg, #7c3aed, #06b6d4)"
  border: "rgba(255,255,255,0.1)"

fonts:
  display: "Inter"
  body: "Inter"
  mono: "JetBrains Mono"     # for code blocks, tech-akzente

spacing:
  section-y: 80px
  section-y-mobile: 48px

animation:
  ease: "cubic-bezier(0.16, 1, 0.3, 1)"  # snappy
  hover-duration: 0.2s
  reveal-duration: 0.5s
```

### Pattern-Hinweise
- **Background:** Dark base mit subtle Gradient-Overlay
- **Gradients:** als Akzent in Headlines, Buttons, Borders
- **Glow-Effects:** auf Buttons/Cards (z.B. `box-shadow: 0 0 40px purple/30`)
- **Code-Blocks:** Monospace mit Syntax-Highlighting
- **Animations:** snappy (0.2-0.3s)
- **Cards:** subtle border (1px solid rgba(255,255,255,0.08))

### Wann NICHT verwenden
- Therapy/Health/Wellness (zu cold)
- Senior-Zielgruppen (Dark-Mode-Aversion)

---

## DIRECTION 4 — BRUTALIST EDITORIAL

**Vibe:** Bold, contrasting, oversized typography, asymmetric Layout, raw. Wirkt mutig, polarisierend, statement-making.

**Ideal für:** Creative-Agencies, Provokateur-Brands, Limited-Editions, Avant-Garde-Products.

**Reference-Brands (aus `design-md/`):**
- analogue, hyperstudio, pangram-pangram-foundry, logoarchive, exhibition-magazine

**Beispiel-Use:** Design-Agentur-Self-Marketing, Fashion-Brands, Art-Galleries

### Tokens

```yaml
colors:
  background: "#fff8e7"      # Cream + 1 bold contrast color
  contrast-primary: "#000000"
  contrast-accent: "#ff3b30"  # or another bold color
  text-primary: "#000000"

fonts:
  display: "Fraunces"        # or any bold Display-Serif
  body: "DM Sans"
  optional: "Space Grotesk"  # for variation

spacing:
  asymmetric: true            # break Grid intentionally
  section-y: 64-160px        # variable

animation:
  ease: "cubic-bezier(0.65, 0, 0.35, 1)"
  hover-duration: 0.4s
  reveal-duration: 0.7s
```

### Pattern-Hinweise
- **Typography:** Display-Sizes EXTREM (200px+ Headlines), tight letter-spacing
- **Layout:** asymmetrisch, Elements können "rausragen" (negative margins, overflow-visible)
- **Colors:** 2-3 bold Farben, hoher Contrast
- **Hover:** dramatisch (rotate 8-15°, scale 1.1+)
- **Borders:** thick (3-6px) statt subtle
- **Bilder:** entweder bold cropped oder komplett textuell

### Wann NICHT verwenden
- Conservative-Zielgruppen
- Health/Trust-Critical-Businesses

---

## DIRECTION 5 — SOFT WARM

**Vibe:** Warm Beige-Tones, weiche Schatten, Hand-drawn Akzente, friendly. Wirkt einladend, sicher, beruhigend.

**Ideal für:** Wellness, Healing, Children-Brands, Lifestyle, Beauty, Food, Soft-Sell-Coaching.

**Reference-Brands (aus `design-md/`):**
- airbnb, headspace (concept), notion, clay, baemin

**Beispiel-Use:** Yoga-Studios, Wellness-Coaches, Family-Brands, Lifestyle-Products

### Tokens

```yaml
colors:
  background: "#fdf6e3"      # Warm cream
  background-soft: "#f5ecd9"
  text-primary: "#3d2e1f"    # Warm dark brown
  text-light: "#8a7560"
  brand-primary: "#e07856"   # Terracotta
  brand-soft: "#f4c4a9"      # Peach
  accent: "#7d9d68"          # Sage green

fonts:
  display: "Fraunces"        # or "Recoleta"
  body: "DM Sans"            # or "Outfit"

spacing:
  section-y: 96px
  section-y-mobile: 56px
  border-radius: 16-24px     # generous rounded corners

animation:
  ease: "cubic-bezier(0.34, 1.56, 0.64, 1)"  # gentle bounce OK
  hover-duration: 0.4s
  reveal-duration: 0.8s
```

### Pattern-Hinweise
- **Border-Radius:** generös (16-24px) auf Cards, Buttons, Images
- **Shadows:** soft + warm (z.B. `box-shadow: 0 8px 24px rgba(160,100,60,0.15)`)
- **Illustrations:** Hand-drawn-Stil > Stock-Photos
- **Hover:** gentle bounce (subtle scale 1.04 + slight rotate ±2°)
- **Background:** keine harten Übergänge, soft Gradients

### Wann NICHT verwenden
- Tech-/Developer-Brands (zu fluffy)
- High-Stakes-Sales (zu zart)

---

## DIRECTION 6 — KINETIC / LIQUID

**Vibe:** Motion-as-aesthetic. Fließende Verläufe, WebGL-Atmosphäre, scroll-triggered Liquid-Animationen. Wirkt zukunftsorientiert, kinetisch, experimentell. **2026 Awwwards-SOTY-Trend** (Lando Norris, OFF+BRAND).

**Ideal für:** Premium-Tech, AI-Plattformen, Performance-Brands (Sport/Auto), Innovation-Stories, Brand-Experience-Sites.

**Reference-Brands (aus `design-md/`):**
- runway, tavus, cohere, framer, locomotive, ferrari, lamborghini

**Beispiel-Use:** AI-Tool-Launch, Performance-Auto-Brand, Brand-Experience für Tech-Konferenz, Sport-Marken-Hero

### Tokens

```yaml
colors:
  background: "#0a0a0f"          # Deep abyss
  background-soft: "#13131a"
  text-primary: "#f5f5f7"
  text-light: "#8a8a92"
  brand-primary: "#7c5cff"       # Electric violet (or custom hot accent)
  brand-deep: "#3d1d99"
  accent-warm: "#ff7ab5"          # Liquid pink/magenta
  accent-cool: "#3effd0"          # Aurora teal

gradients:
  hero-kinetic: "radial-gradient(ellipse at 30% 40%, #7c5cff 0%, transparent 50%), radial-gradient(ellipse at 70% 60%, #ff7ab5 0%, transparent 50%), #0a0a0f"
  liquid-overlay: "conic-gradient(from 0deg, #7c5cff, #ff7ab5, #3effd0, #7c5cff)"

fonts:
  display: "PP Editorial New" or "Migra"   # Editorial-meets-Tech
  body: "Inter Tight" or custom
  mono: "JetBrains Mono"                    # für Code-Akzente

spacing:
  section-y: 140px
  section-y-mobile: 80px
  border-radius: 0-4px                       # sharp, kein soft

animation:
  ease: "cubic-bezier(0.16, 1, 0.3, 1)"      # smooth out, no bounce
  hero-duration: 1.6s                        # längere, atmende Loops
  scroll-trigger-stagger: 80ms
```

### Pattern-Hinweise
- **Hero:** WebGL-Shader oder CSS-Conic-Gradient als bewegter Hintergrund
- **Gradients:** **Kinetic** (siehe `design.md` Kinetic-Gradient-Spec) — radial + conic kombiniert, langsam rotierend
- **Scroll:** liquid-morphing Sections via GSAP ScrollTrigger, NICHT statisch
- **Typography:** XL-Display (140-200px) mit `font-variation-settings` für Variable-Font-Morphing
- **Cursor:** Custom-Cursor mit Trail-Effekt (Lenis + Framer Motion `mouseFollower`)
- **NO:** flache Gradients, statische Hero-Images, Stock-Photos
- **Performance:** `prefers-reduced-motion` MUSS Fallback haben (reduced animations + statischer Gradient)

### Wann NICHT verwenden
- Trust-Heavy B2B (zu experimentell, kein Steuerberater-Vibe)
- Performance-kritische SEO-Sites (WebGL killt Lighthouse)
- Conservative Industries (Finance, Legal, Health-Care)

---

## DIRECTION 7 — ANTI-AI TACTILE WARMTH

**Vibe:** Backlash gegen AI-Slop. Texture-first, handwritten elements, paper-feel, intentional imperfection. Wirkt menschlich, krafted, anti-perfekt — bewusst gegen den "AI-generated"-Look. **2026 Counter-Trend** (Creative Bloq, "Tactile Rebellion").

**Ideal für:** Coaching/Therapy mit Soul-Touch, Premium-Craft-Brands, Editorial-Healing, Personal-Brand mit Wärme, Slow-Living-Audiences.

**Reference-Brands (aus `design-md/`):**
- granola, mercury, analogue, kinfolk, charlie-le-maignan, hyperstudio (texture-heavy variants)

**Beispiel-Use:** Therapeut:innen-Page mit Vertrauens-Vibe, Slow-Coaching-Brand, Editorial-Newsletter-LP, Premium-Handcraft-E-Commerce

### Tokens

```yaml
colors:
  background: "#f4ede2"               # Warm paper cream (NICHT pure white)
  background-texture: "#ede4d3"        # Slightly darker for layered cards
  text-primary: "#2a1f15"              # Deep coffee brown
  text-warm: "#5c4630"
  brand-primary: "#a8553c"             # Brick / Terracotta
  brand-deep: "#6b3724"
  accent-handwritten: "#1a1a1a"        # Ink-black für handgeschriebene Akzente

textures:
  paper: "url('/textures/paper-grain.png')"        # 8-12% opacity overlay
  fabric: "url('/textures/canvas-fibers.png')"     # subtle 5% opacity
  noise: "Generated via CSS filter or SVG"          # always present, low opacity

fonts:
  display: "Recoleta" or "Apoc"        # warm Serif mit Charakter
  body: "Söhne" or "Inter"
  handwritten: "Caveat" or "Permanent Marker"  # für annotative Akzente (10-15% der Texte)

spacing:
  section-y: 96px
  section-y-mobile: 56px
  border-radius: 2-6px                  # bewusst minimal, fast cantons
  card-padding: asymmetrisch             # z.B. padding: 32px 24px 48px 36px

animation:
  ease: "cubic-bezier(0.34, 1.56, 0.64, 1)"   # subtle bounce für Wärme
  hover-duration: 0.5s
  reveal-duration: 0.9s
```

### Pattern-Hinweise
- **Background:** IMMER mit Paper-Grain-Overlay (8-12% opacity SVG-noise oder PNG-texture)
- **Card-Borders:** unregelmäßig — z.B. via SVG mit leicht wackeliger Linie statt `border: 1px solid`
- **Handwritten-Accents:** 10-15 % der Section-Text als handgeschrieben (Caveat, Permanent Marker) — als Akzent, NIE als Body
- **Imperfection:** Bilder mit Mini-Rotation (-2° bis +2°), nie perfekt aligned
- **Shadows:** SOFT + WARM, niemals scharf — `0 8px 32px rgba(140,80,40,0.18)`
- **Sticky-Notes / Tape:** als Decorative Elements für Testimonials, Annotations
- **Pull-Quotes:** als Polaroid oder "handgeschriebener Zettel" gerahmt
- **NO:** perfekte Symmetry, harte Gradients, Glasmorphism, Neon-Akzente
- **Bilder:** Editorial-Portraits mit Filmkorn, NIE Stock, ggf. selbst-fotografiert / illustriert

### Wann NICHT verwenden
- B2B-SaaS / Developer-Tools (zu warm)
- Performance/Auto/Sport-Brands (zu gemütlich)
- High-Tech-Innovation (Direction 6 ist passender)

---

## Wie diese Library nutzen

### Bei neuem Kunden (Visual-Direction unklar)

**Workflow:**
1. Im Discovery-Form Dimension 4 (Brand) → User fragt "welche Direction?"
2. Diese 5 als Auswahl präsentieren mit Kurz-Vibe + Reference-Brand-Beispielen
3. User wählt 1 → diese Direction's Tokens als Startpunkt für Brand-Spec
4. **Brand-Spec.md anlegen** (siehe `huashu_design/SKILL.md`) mit angepassten Tokens
5. Erst dann Build starten

### Bei Hybrid-Anforderung (z.B. "Editorial mit etwas Tech")

→ Eine als Basis (z.B. EDITORIAL MAGAZINE) + 1-2 spezifische Elements aus anderer Direction (z.B. Gradient-Akzent aus TECH UTILITY)
→ NICHT mehr als 2 Directions mischen (sonst inkonsistent)

### Bei bestehender Brand (Tokens schon definiert)

→ Diese File **nicht verwenden**. Stattdessen die bestehende Brand-Spec.md / Visual-Tokens-File nutzen.
→ Optional: Direction als Reference im Kopf behalten ("ist im Stil von X").

---

## Cross-References

- **Discovery-Form:** `Brain/skills/_universal/DISCOVERY-FORM.md` (Dimension 4)
- **Asset-Protokoll:** `Brain/skills/huashu_design/SKILL.md` (Brand-Spec.md erstellen)
- **Brand-Library:** `Brain/skills/design_tokens/design-md/_INDEX.md` (106 echte Brands als tiefere Referenz)
- **Use-Case-Routing:** `Brain/skills/design_tokens/USE-CASE-INDEX.md` (Pattern pro Section-Typ)
- **CSS-Patterns:** `Brain/skills/design_tokens/design.md` (Spacing, Animations, Shadows)

---

## Update-Mechanismus

**Wenn eine 6. Direction entsteht** (z.B. "Sci-Fi Cyberpunk"):
- Hier als Direction 6 anhängen
- Mit Tokens + Reference-Brands + Pattern-Hinweisen

**Wenn eine Direction battle-tested ist** (= 3+ erfolgreiche Builds):
- Mit `✅ proven N×` markieren
- Beispiel-Build-Links auflisten

**Wenn eine Direction nie genutzt wird** (= 6 Monate dead):
- Hinterfragen ob sie sinnvoll ist
- Eventuell entfernen oder durch passendere ersetzen
