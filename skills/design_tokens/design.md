---
name: Design Inspiration Library
description: Kuratierte Dribbble Design-Referenzen + Studio Knowledge für High-End LP und Presentation Builds. Anti-AI-Slop. Kategorisiert nach Stil und Use Case.
type: reference
---

# Design Inspiration Library
> Basis für alle LP-, Presentation- und Creative-Builds. Immer aus dieser Library wählen — nie AI-Slop Defaults halluzinieren.
> Quellen: Live Dribbble Scrape (März 2026) + dokumentierte Studio-Systeme.

**📁 REFERENZ-SCREENSHOTS:** `Brain/skills/design_tokens/references/`
→ Saladin legt hier Screenshots von LPs/Pages ab die ihm gefallen
→ VOR jedem LP-Build prüfen ob neue Referenzen vorhanden sind → Patterns extrahieren

---

## AI-SLOP BLACKLIST (niemals verwenden)

| Element | Verboten |
|---------|----------|
| **Fonts** | Inter als Headline, Roboto, System-UI als Display, Poppins für alles |
| **Farben** | Purple Gradient #7B2FF7→#2196F3, Teal+Navy Kombo, Coral+Turquoise, Electric Blue+Purple |
| **Effekte** | Radial Glow hinter Hero Text, Glassmorphism Cards (overused), FadeUp auf jedem Element, Blur Overlay auf Hero Image |
| **Layouts** | Centered Everything, identische Card-Grid Heights, 3-Column Feature Grid mit Icon+Title+Text, Testimonial Carousel |
| **Kombinationen** | Dark bg + Teal CTA + Inter Headline = AI-Slop. Dark bg + Purple Gradient + Icon Grid = AI-Slop. |

---

## CSS TOOLBOX — Copy-Paste Patterns (Produktionserprobt)

> Diese Patterns sind live-erprobt (SMS Karriere-LP, GODIA Präsentation). Direkt verwenden — kein Neuerfinden.

---

### FARBPALETTEN (Hex-Werte, sofort einsetzbar)

```css
/* --- DARK AGENCY / B2B (universal, conversion-focused) --- */
--bg:          #0d0d0d;
--bg-card:     #141414;
--bg-elevated: #1a1a1a;
--border:      rgba(255,255,255,0.07);
--text-primary: #f0f0f0;
--text-muted:  rgba(240,240,240,0.45);
--accent:      #ffffff;

/* --- DARK FINANCE / FINTECH --- */
--bg:          #080C12;
--bg-card:     #0D1117;
--accent:      #2E6FF3;
--accent-glow: rgba(46,111,243,0.25);
--text:        #F8F9FA;

/* --- DARK LUXURY / TAX / LAW (Cormorant-Stil) --- */
--bg:          #111111;
--bg-warm:     #1a1814;
--cream:       #F5F0E8;
--gold:        #C9A96E;
--gold-light:  #E8D5A3;
--text:        #F5F0E8;

/* --- KARRIERE DARK (SMS-Stil, grün) --- */
--bg:          #0d0d0d;
--bg-section:  #111111;
--green:       #1a7a4a;
--green-bright:#22c55e;
--green-glow:  rgba(34,197,94,0.15);
--text:        #f0f0f0;

/* --- DIAMOND / LUXURY PRODUCT (GODIA-Stil) --- */
--bg:          #0a0a0a;
--bg-card:     #111111;
--gold:        #C9A96E;
--gold-shine:  #E8D5A3;
--gold-dark:   #8B6914;
--text:        #F5F0E8;
--border:      rgba(201,169,110,0.2);

/* --- LIGHT EDITORIAL (wenn hell gewünscht) --- */
--bg:          #FAFAF8;
--bg-dark:     #1a1a1a;
--text:        #111111;
--text-muted:  #666666;
--accent:      #111111;
--border:      rgba(0,0,0,0.08);
```

---

### FONT PAIRS (Google Fonts Import-ready)

```html
<!-- EDITORIAL LUXURY — Cormorant + Source Sans -->
<!-- Für: Steuerberatung, Law, Finance, Immobilien, Luxury Products -->
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Source+Sans+3:wght@300;400;600&display=swap" rel="stylesheet">
/* Headline: Cormorant Garamond 300–600 | Body: Source Sans 3 400 */

<!-- MODERN AGENCY — Space Grotesk + DM Sans -->
<!-- Für: Agenturen, SaaS, Tech, Karriere, B2B -->
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">
/* Headline: Space Grotesk 600–700 | Body: DM Sans 400 */

<!-- BOLD EDITORIAL — Plus Jakarta Sans -->
<!-- Für: Bold B2B, Coaching, Performance Marketing -->
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300&display=swap" rel="stylesheet">
/* Alles: Plus Jakarta Sans — skaliert von 300 bis 800 */

<!-- NEWSPAPER EDITORIAL — Playfair + Source Sans -->
<!-- Für: Newspaper-Split Layouts, Editorial Blogs, Brand-Storytelling -->
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400;1,700&family=Source+Sans+3:wght@300;400;600&display=swap" rel="stylesheet">
/* Headline: Playfair Display | Body: Source Sans 3 */

<!-- DARK TECH — Space Grotesk + JetBrains Mono -->
<!-- Für: Dev Tools, FinTech, AI Platforms, Data -->
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
/* Headline: Space Grotesk | Code/Data: JetBrains Mono */
```

---

### CSS PATTERNS — Grain Texture

```css
/* Grain Overlay — alle dunklen Sektionen */
/* Als SVG Data-URI, kein externes Asset nötig */
.grain-section {
  position: relative;
}
.grain-section::after {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='1'/%3E%3C/svg%3E");
  opacity: 0.045;
  pointer-events: none;
  z-index: 1;
}
```

---

### CSS PATTERNS — 3D Card (Hero, produkterprobt)

```css
/* Static 3D Tilt — Mobile & kein JS */
.card-3d-static {
  transform: perspective(1400px) rotateX(3deg) rotateY(-14deg) scale(1.01);
  box-shadow:
    0 40px 80px rgba(0,0,0,0.6),
    0 0 0 1px rgba(255,255,255,0.07),
    0 0 60px rgba(34,197,94,0.08);
  border-radius: 20px;
  transition: transform 0.1s ease, box-shadow 0.1s ease;
}

/* Dynamic Mouse-Tracking 3D — Desktop */
/* JS: mousemove → rotateX/Y via CSS custom properties */
.card-3d-dynamic {
  transform: perspective(1400px)
    rotateX(var(--rx, 3deg))
    rotateY(var(--ry, -14deg))
    scale(var(--sc, 1.01));
  transition: transform 0.08s ease, box-shadow 0.08s ease;
}
```

---

### CSS PATTERNS — Card Fall + Float (Einflug-Animation)

```css
/* Keyframes — einmal definieren, überall renutzen */
@keyframes card-fall {
  from { opacity: 0; transform: perspective(1400px) rotateX(3deg) rotateY(-14deg) translateY(-60px) scale(0.96); }
  to   { opacity: 1; transform: perspective(1400px) rotateX(3deg) rotateY(-14deg) translateY(0) scale(1.01); }
}
@keyframes card-float {
  0%, 100% { transform: perspective(1400px) rotateX(3deg) rotateY(-14deg) translateY(0) scale(1.01); }
  50%       { transform: perspective(1400px) rotateX(4deg) rotateY(-12deg) translateY(-12px) scale(1.01); }
}
@keyframes orb-float {
  0%, 100% { transform: translateX(-50%) scale(1); opacity: 0.5; }
  50%       { transform: translateX(-50%) scale(1.15); opacity: 0.7; }
}

/* Usage */
.hero-card {
  animation:
    card-fall 1.5s cubic-bezier(.22,1,.36,1) both,
    card-float 4.5s ease-in-out 1.6s infinite;
}
```

---

### CSS PATTERNS — Spotlight Sweep

```css
@keyframes spotlight-sweep {
  0%   { left: -80%; opacity: 0; }
  10%  { opacity: 1; }
  90%  { opacity: 1; }
  100% { left: 130%; opacity: 0; }
}
@keyframes green-hit {
  0%, 100% { opacity: 0; }
  50%       { opacity: 0.55; }
}

/* Element das den Sweep trägt */
.spotlight-beam {
  position: absolute;
  inset: 0;
  overflow: hidden;
  border-radius: inherit;
  pointer-events: none;
}
.spotlight-beam::before {
  content: '';
  position: absolute;
  top: 0; left: -80%;
  width: 60%; height: 100%;
  background: linear-gradient(105deg, transparent 30%, rgba(255,255,255,0.09) 50%, transparent 70%);
  animation: spotlight-sweep 8s ease-in-out 2s infinite;
}
.spotlight-beam::after {
  content: '';
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse at 50% 30%, rgba(34,197,94,0.18) 0%, transparent 65%);
  animation: green-hit 8s ease-in-out 2s infinite;
}
```

---

### CSS PATTERNS — Ambient Glow Orb

```css
/* Pulsierender Glow-Orb hinter Hero-Element */
.ambient-orb {
  position: absolute;
  bottom: -40px;
  left: 50%;
  transform: translateX(-50%);
  width: 280px;
  height: 40px;
  background: radial-gradient(ellipse, rgba(34,197,94,0.35) 0%, transparent 70%);
  filter: blur(20px);
  animation: orb-float 4.5s ease-in-out 1.6s infinite;
  pointer-events: none;
}
/* Farbe je nach Palette anpassen: rgba(46,111,243,...) für Finance, rgba(201,169,110,...) für Luxury */
```

---

### CSS PATTERNS — Newspaper Split Hero

```css
/* 50/50 Split — links dark, rechts cream/light */
.newspaper-hero {
  display: grid;
  grid-template-columns: 1fr 1fr;
  min-height: 100vh;
}
.newspaper-hero .side-dark {
  background: var(--bg);
  padding: clamp(60px, 8vw, 120px);
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.newspaper-hero .side-light {
  background: var(--cream, #F5F0E8);
  position: relative;
  overflow: hidden;
  border-left: 1px solid rgba(0,0,0,0.08);
}
/* Mobile: stack */
@media (max-width: 768px) {
  .newspaper-hero { grid-template-columns: 1fr; }
  .newspaper-hero .side-light { min-height: 50vh; }
}
```

---

### CSS PATTERNS — Counter Animation

```css
/* Zählt von 0 auf Zielwert — reines CSS + minimal JS */
/* JS-Snippet: */
/*
document.querySelectorAll('[data-count]').forEach(el => {
  const target = +el.dataset.count;
  const duration = 2000;
  const start = performance.now();
  const tick = now => {
    const p = Math.min((now - start) / duration, 1);
    el.textContent = Math.floor(p * target).toLocaleString('de-DE');
    if (p < 1) requestAnimationFrame(tick);
  };
  requestAnimationFrame(tick);
});
*/
/* Usage: <span data-count="1234">0</span> */
```

---

### SPACING SYSTEM

```css
/* Konsistente Vertical Rhythm Werte */
--space-xs:  clamp(16px, 2vw, 24px);
--space-sm:  clamp(32px, 4vw, 48px);
--space-md:  clamp(60px, 7vw, 96px);
--space-lg:  clamp(96px, 10vw, 140px);
--space-xl:  clamp(120px, 14vw, 200px);

/* Section Padding (Standard) */
section { padding: var(--space-lg) clamp(20px, 5vw, 80px); }

/* Hero Headline Responsive */
.hero-h1 {
  font-size: clamp(48px, 8vw, 96px);
  line-height: 0.93;
  letter-spacing: -0.03em;
}
/* Mobile */
@media (max-width: 768px) {
  .hero-h1 { font-size: clamp(52px, 14vw, 72px); line-height: 0.94; }
}
```

---

### SHADOW ELEVATION SYSTEM (5 Levels)

```css
/* Level 0 — Flat (kein Shadow) */
--shadow-0: none;

/* Level 1 — Subtle Lift (Hover States, kleine Karten) */
--shadow-1: 0 1px 3px rgba(0,0,0,0.18), 0 1px 2px rgba(0,0,0,0.24);

/* Level 2 — Card (Standard Karten, Dropdowns) */
--shadow-2: 0 4px 12px rgba(0,0,0,0.22), 0 2px 4px rgba(0,0,0,0.14);

/* Level 3 — Floating (Modals, Featured Cards) */
--shadow-3: 0 10px 28px rgba(0,0,0,0.25), 0 4px 10px rgba(0,0,0,0.15);

/* Level 4 — Hero Card (3D Perspective Cards) */
--shadow-4: 0 40px 80px rgba(0,0,0,0.60), 0 0 0 1px rgba(255,255,255,0.07);

/* Level 5 — Glow Shadow (CTA Buttons mit Farb-Glow) */
/* Farbe je nach Accent anpassen: */
--shadow-5-green:  0 20px 50px rgba(34,197,94,0.35),  0 4px 15px rgba(0,0,0,0.3);
--shadow-5-blue:   0 20px 50px rgba(46,111,243,0.35),  0 4px 15px rgba(0,0,0,0.3);
--shadow-5-gold:   0 20px 50px rgba(201,169,110,0.30), 0 4px 15px rgba(0,0,0,0.3);
--shadow-5-white:  0 20px 50px rgba(255,255,255,0.12), 0 4px 15px rgba(0,0,0,0.3);
```

---

### BORDER RADIUS TOKEN-SCALE

```css
--radius-xs:   4px;    /* Subtle — Badges, Tags, Code-Blöcke */
--radius-sm:   8px;    /* Small — Inputs, kleine Buttons */
--radius-md:   12px;   /* Default — Standard Cards, Dropdowns */
--radius-lg:   16px;   /* Large — Featured Cards, Modals */
--radius-xl:   20px;   /* Hero Cards, prominente Elemente */
--radius-2xl:  28px;   /* Oversized Karten, Bento Cells */
--radius-pill: 9999px; /* CTA Buttons, Tags, Pills */
```

---

### BUTTON SYSTEM (Primary, Secondary, Ghost)

```css
/* === PRIMARY BUTTON (Haupt-CTA) === */
.btn-primary {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 14px 32px;
  border-radius: var(--radius-pill);
  background: var(--accent);
  color: var(--bg);
  font-weight: 600;
  font-size: 15px;
  letter-spacing: -0.01em;
  border: none;
  cursor: pointer;
  transition: transform 0.25s cubic-bezier(0.34,1.56,0.64,1),
              box-shadow 0.25s ease,
              background 0.2s ease;
}
.btn-primary:hover {
  transform: translateY(-2px) scale(1.02);
  box-shadow: var(--shadow-5-white); /* Farbe je Palette anpassen */
}
.btn-primary:active {
  transform: translateY(0) scale(0.99);
}

/* === SECONDARY BUTTON (Ghost mit Border) === */
.btn-secondary {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 13px 30px;
  border-radius: var(--radius-pill);
  background: transparent;
  color: var(--text-primary);
  font-weight: 500;
  font-size: 15px;
  border: 1px solid rgba(255,255,255,0.2);
  cursor: pointer;
  transition: border-color 0.2s ease, background 0.2s ease, transform 0.25s cubic-bezier(0.34,1.56,0.64,1);
}
.btn-secondary:hover {
  border-color: rgba(255,255,255,0.5);
  background: rgba(255,255,255,0.06);
  transform: translateY(-1px);
}

/* === GHOST BUTTON (Minimal, Tertiary) === */
.btn-ghost {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 10px 20px;
  background: transparent;
  color: rgba(240,240,240,0.6);
  font-size: 14px;
  font-weight: 400;
  border: none;
  cursor: pointer;
  text-decoration: underline;
  text-underline-offset: 4px;
  transition: color 0.2s ease;
}
.btn-ghost:hover { color: rgba(240,240,240,1); }

/* Mindest-Touch-Target Mobile: immer min-height 44px sicherstellen */
@media (max-width: 768px) {
  .btn-primary, .btn-secondary { min-height: 48px; padding: 14px 28px; }
}
```

---

### ANIMATION TIMING CURVES (Named System)

```css
/* Spring — für Einflug-Animationen, Hover-Transforms, Card-Fall */
/* Leichtes Überschießen → fühlt sich lebendig an */
--ease-spring:   cubic-bezier(0.34, 1.56, 0.64, 1);

/* Smooth Out — für Scroll-Reveals, Fade-Ins */
/* Schnell rein, sanft stoppen */
--ease-out:      cubic-bezier(0, 0, 0.2, 1);

/* Smooth In-Out — für Float-Loops, Orb-Pulse */
/* Gleichmäßig, keine harten Kanten */
--ease-inout:    cubic-bezier(0.42, 0, 0.58, 1);

/* Snappy — für Micro-Interactions, Buttons, Tooltips */
/* Sehr schnell, direkt */
--ease-snappy:   cubic-bezier(0.25, 0.46, 0.45, 0.94);

/* Decelerate — für Elemente die "landen" */
/* Kommt schnell, bremst vor dem Ziel */
--ease-land:     cubic-bezier(0.0, 0.0, 0.2, 1.0);

/* USAGE GUIDE:
   Card Fall/Fly-In:   1.5s var(--ease-spring)
   Hover Transform:    0.25s var(--ease-spring)
   Scroll Reveal:      0.6s var(--ease-out)
   Float Loop:         4.5s var(--ease-inout) infinite
   Button Hover:       0.2s var(--ease-snappy)
   Modal Open:         0.35s var(--ease-land)
*/
```

---

### TRANSITION DURATION TOKENS

```css
--duration-instant: 100ms;  /* Tooltips, Highlights — kaum wahrnehmbar */
--duration-fast:    200ms;  /* Hover States, Farb-Wechsel */
--duration-normal:  300ms;  /* Standard Transitions (Cards, Dropdowns) */
--duration-slow:    500ms;  /* Scroll Reveals, Öffnen/Schließen */
--duration-xslow:   800ms;  /* Große Einflüge, Hero Animationen */

/* REGEL: Nur transform + opacity animieren — nie width/height/margin */
/* GPU-beschleunigt: transform, opacity, filter */
/* Layout-Thrashing (vermeiden): width, height, margin, padding, top, left */
```

---

### Z-INDEX LAYERING MAP

```css
--z-base:        0;     /* Standard Content */
--z-raised:      10;    /* Cards im hover-State, kleine Overlays */
--z-sticky:      100;   /* Sticky Nav */
--z-dropdown:    200;   /* Dropdown-Menüs */
--z-overlay:     300;   /* Backdrop-Dimmer */
--z-modal:       400;   /* Modals, Dialoge */
--z-toast:       500;   /* Notifications, Toasts */
--z-tooltip:     600;   /* Tooltips */
--z-cursor:      9999;  /* Custom Cursor */
```

---

### GRADIENT RECIPES

```css
/* Dark Hero Overlay — Photo dahinter noch sichtbar */
.overlay-dark {
  background: linear-gradient(180deg, transparent 0%, rgba(0,0,0,0.7) 100%);
}

/* Section Fade — nahtloser Übergang von Section zu Section */
.fade-to-bg {
  background: linear-gradient(180deg, transparent 0%, var(--bg) 100%);
}

/* Mesh Gradient (2025 Trend) — Hero Hintergründe, Abstract Backgrounds */
.mesh-hero {
  background:
    radial-gradient(circle at 20% 50%, rgba(34,197,94,0.15) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, rgba(46,111,243,0.12) 0%, transparent 50%),
    radial-gradient(circle at 60% 80%, rgba(201,169,110,0.10) 0%, transparent 50%),
    var(--bg);
}
/* Farben je nach Palette anpassen */

/* Glow Accent — hinter CTA Buttons, Hero Cards */
.glow-accent {
  background: radial-gradient(ellipse at center,
    rgba(34,197,94,0.20) 0%,
    transparent 65%);
  filter: blur(40px);
}

/* Text Gradient (für Display Headlines) */
.text-gradient {
  background: linear-gradient(135deg, #ffffff 0%, rgba(255,255,255,0.6) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* === KINETIC GRADIENTS (2026 Trend — Lando Norris / Awwwards SOTY) === */
/* Pflicht-Trigger: Direction 6 KINETIC/LIQUID aus VISUAL-DIRECTIONS.md */
/* Pure-CSS, performance-safer als WebGL, prefers-reduced-motion-respektiert */

/* Kinetic Hero — langsam rotierender Conic-Gradient mit Multi-Hue */
.kinetic-hero {
  background:
    radial-gradient(ellipse at 30% 40%, rgba(124,92,255,0.35) 0%, transparent 50%),
    radial-gradient(ellipse at 70% 60%, rgba(255,122,181,0.30) 0%, transparent 50%),
    conic-gradient(from 0deg at 50% 50%, rgba(124,92,255,0.15), rgba(255,122,181,0.12), rgba(62,255,208,0.10), rgba(124,92,255,0.15));
  background-size: 100% 100%, 100% 100%, 200% 200%;
  animation: kinetic-rotate 18s linear infinite;
}
@keyframes kinetic-rotate {
  0%   { background-position: 0% 0%, 100% 100%, 0% 50%; }
  50%  { background-position: 50% 100%, 50% 0%, 100% 50%; }
  100% { background-position: 0% 0%, 100% 100%, 200% 50%; }
}

/* Liquid Morph — viscose Übergang, ideal für Section-Backgrounds */
.liquid-morph {
  background:
    radial-gradient(circle at var(--mx, 50%) var(--my, 50%), rgba(124,92,255,0.4) 0%, transparent 35%),
    radial-gradient(circle at calc(100% - var(--mx, 50%)) calc(100% - var(--my, 50%)), rgba(62,255,208,0.3) 0%, transparent 40%),
    #0a0a0f;
  transition: background 1.6s cubic-bezier(0.16, 1, 0.3, 1);
  /* JS-Hook: --mx/--my werden via mousemove gesetzt (Lenis kompatibel) */
}

/* Aurora Sweep — für CTA-Sections, Trust-Pills, Premium-Boxen */
.aurora-sweep {
  background: linear-gradient(110deg,
    #7c5cff 0%,
    #ff7ab5 25%,
    #3effd0 50%,
    #ff7ab5 75%,
    #7c5cff 100%);
  background-size: 300% 100%;
  animation: aurora-shift 8s ease-in-out infinite;
}
@keyframes aurora-shift {
  0%, 100% { background-position: 0% 50%; }
  50%      { background-position: 100% 50%; }
}

/* Performance: ALWAYS Fallback für Reduced-Motion */
@media (prefers-reduced-motion: reduce) {
  .kinetic-hero,
  .liquid-morph,
  .aurora-sweep {
    animation: none !important;
    transition: none !important;
  }
}
```

**Wann Kinetic-Gradients nutzen:**
- Direction 6 (KINETIC/LIQUID) aktiv → Pflicht für Hero/Hero-adjacent Sections
- AI-Tool-Launch, Performance-Brand, Innovation-Story
- **NIE** für Direction 1 (Editorial), Direction 5 (Soft Warm), Direction 7 (Anti-AI Tactile)
- **NIE** für Conversion-kritische Above-The-Fold ohne A/B-Test (Bewegung kann Bounce-Rate erhöhen)

**Anti-Patterns:**
- ❌ Statische Stops als "Kinetic" deklarieren — Bewegung muss IMMER sichtbar sein
- ❌ Mehr als 1 Kinetic-Gradient pro Section — Konflikte zw. Easing
- ❌ ohne `prefers-reduced-motion` Fallback (A11y-Killer)

---

### CLIP-PATH DIAGONAL (2025 Trend — Section Divider)

```css
/* Diagonaler Schnitt — Section von Section trennen ohne geraden Rand */
.section-diagonal-bottom {
  clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
  margin-bottom: -5vw;
}
.section-diagonal-top {
  clip-path: polygon(0 5vw, 100% 0, 100% 100%, 0 100%);
  margin-top: -5vw;
}

/* Angled CTA Banner */
.banner-angled {
  clip-path: polygon(2% 0%, 100% 0%, 98% 100%, 0% 100%);
}
```

---

### 2025 NEUE FONT PAIRS (Ergänzung zu bestehenden)

```html
<!-- BOLD IMPACT — Bebas Neue + Heebo -->
<!-- Für: Performance Marketing, Coaching, Bold Startups -->
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Heebo:wght@300;400;500&display=swap" rel="stylesheet">
/* Headline: Bebas Neue (ALL CAPS, tight tracking) | Body: Heebo 400 */

<!-- MINIMALIST ELEGANCE — Prata + Manrope -->
<!-- Für: Luxury SaaS, Premium Coaching, High-End Brands -->
<link href="https://fonts.googleapis.com/css2?family=Prata&family=Manrope:wght@300;400;500&display=swap" rel="stylesheet">
/* Headline: Prata 400 | Body: Manrope 300-400 (sehr leicht, sehr elegant) */

<!-- BOLD EDITORIAL — Montserrat + Merriweather -->
<!-- Für: Professional SaaS, Content-heavy, Trust-first -->
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@600;700;800;900&family=Merriweather:ital,wght@0,400;1,300&display=swap" rel="stylesheet">
/* Headline: Montserrat 700-900 | Body: Merriweather 400 */
```

---

### 2025 NEUE FARBPALETTEN (Warm Trend + New Combos)

```css
/* WARM MODERN (2025 dominant — schlägt kühle Paletten) */
--bg:         #F2F0EA;   /* Warm Off-White — kein reines Weiß */
--bg-card:    #E8E5DE;
--text:       #1A1814;   /* Warm Black — kein #000 */
--accent:     #2D5A27;   /* Deep Forest Green */
--accent-warm:#C8401A;   /* Terracotta als Alternative */

/* BOLD TECH (Startup Energy — Neon auf Dunkel) */
--bg:         #0F0F0F;
--accent-1:   #6366F1;   /* Neon Indigo */
--accent-2:   #CCFF00;   /* Cyber Lime — sparsam einsetzen */
--text:       #FAFAFA;

/* E-COMMERCE PRODUCT (Desire-driven, Clean) */
--bg:         #FFFFFF;
--bg-alt:     #F8F7F4;
--text:       #111111;
--accent:     #D4A853;   /* Warm Gold */
--accent-dark:#8B6914;
--border:     #E5E2DC;
```

---

### AI-SLOP BLACKLIST — UPDATES (2025)

| Neu verboten | Warum |
|-------------|-------|
| Parallax auf JEDEM Element | Causes motion sickness, clichéd seit 2022 |
| Autoplay Video mit Sound | Conversion-Killer, User verlässt sofort |
| 3-Column Icon-Grid als Feature-Section | Seit 2020 überall — kein Differenzierungsmerkmal |
| Bounce/Spin Loader Animationen | Billig, unprofessionell |
| Gradient Text überall | Wird 2025 zu AI-Slop degradiert — nur für Display Headlines |
| Centered Everything auf Desktop | Kein visuelles Gewicht, kein Narrativ |

---

## 1. DARK EDITORIAL / DARK LUXURY

### Event Organizer — Dark Editorial Experience
- **Designer:** 10am Space (@10amspace)
- **URL:** dribbble.com/shots/26843407
- **Farben:** Near-black bg, Neon Yellow accent (~#F5FF00), weiß text
- **Mood:** Electric, punchy, event-energy
- **Non-Slop-Element:** Neon Yellow auf schwarz — gewagt, sofort distinctive. Kein Teal, kein Purple.

### Fine Dine Club — Website Design
- **Designer:** Dwipo Prawiro
- **URL:** dribbble.com/shots/26906627
- **Farben:** Deep charcoal bg (~#1A1714), warm cream text (#F5F0E8), gold accent
- **Fonts:** Serif Display (Cormorant oder Playfair) + leichte Sans
- **Mood:** Culinary luxury, cinematic, intimate
- **Non-Slop-Element:** Warme Charcoal statt kaltem #000 — Photography zentriert, Typographie dient dem Bild

### Boutique Law Firm — Premium Legal Services
- **Designer:** Mike Taylor (@designwithmikey) — 23 Likes, 5.3k Views
- **URL:** dribbble.com/shots/26909555
- **Farben:** Very dark navy/charcoal bg, off-white text, subtle warm gold accent
- **Fonts:** Serif Headlines, clean grotesk Body
- **Mood:** Trustworthy, premium, authoritative
- **Non-Slop-Element:** Typ-fokussiert, keine Icon-Arrays, klare Hierarchie. Minimal aber nicht leer.

### Luxury Real Estate — Modern Property Landing Page
- **Designer:** Peno Lab — 24 Likes, 5.5k Views
- **URL:** dribbble.com/shots/26853330
- **Farben:** Dark architectural palette (~#0F0F0F bg), warm beige accent, weiß
- **Mood:** Architecture, precision, modern luxury
- **Non-Slop-Element:** Architektur-Fotografie als Design-Element. Text-Overlay ohne Glassmorphism.

### The Culinary Atelier — Luxury Dining Website
- **Designer:** Jia M — 3 Likes, 1.6k Views
- **URL:** dribbble.com/shots/26839232
- **Farben:** Dark bg, warm cream, muted gold, Photography-getrieben
- **Fonts:** High-contrast Serif Display + leichter Sans
- **Mood:** Cinematic, tactile, gastronomic
- **Non-Slop-Element:** Split-Layout mit massivem Food Photography. Kein White-Space-Missbrauch.

### Vintage Camera Landing Page UI
- **Designer:** Mike Taylor (@designwithmikey) — 50 Likes, 25.6k Views
- **URL:** dribbble.com/shots/26302344
- **Farben:** Dark warm bg (~#1C1A17), amber/gold accent, cream white
- **Fonts:** Bold retro serif + mono body
- **Mood:** Nostalgic luxury, collector's edition
- **Non-Slop-Element:** Retro-Ästhetik ohne Kitsch — warme Dunkelheit, Vintage Photography, übergroße Typographie

### Book Author Landing Page
- **Designer:** Sophy Inasaridze — 24 Likes, 6.3k Views
- **URL:** dribbble.com/shots/26818648
- **Farben:** Dark earthy bg, warm off-white, muted terracotta accent
- **Fonts:** Editorial Serif (Display) + grotesk
- **Mood:** Literary, intellectual, quiet authority
- **Non-Slop-Element:** Buchcover als Hero-Element. Keine Icons. Reine Typographie-Hierarchie.

### Shift Studio — Digital Agency Hero Animation
- **Designer:** Elux Space — 41 Likes, 3.9k Views
- **URL:** dribbble.com/shots/27104940
- **Farben:** Deep dark bg, gradient hero, clean white text
- **Mood:** Motion-first, agency energy, dark premium
- **Non-Slop-Element:** Hero Animation als USP — kein statisches Hero Image. Gradient dient Bewegung, nicht Dekoration.

### Verba — Dark Hero UI for Athletes & Artists
- **Designer:** Konrad Makowski — 3 Likes, 1k Views
- **URL:** dribbble.com/shots/27172490
- **Farben:** Near-black bg, Yellow (~#F5D000), Grid-Layout
- **Fonts:** Bold grotesque, sehr groß, tight tracking
- **Mood:** Bold, athletic, editorial
- **Non-Slop-Element:** Yellow Accent auf schwarz — mutig. Fotografische Textur. Grid-Overlay sichtbar.

### AI & Digital Art Platform
- **Designer:** Buraq Lab — 75 Likes, 7.1k Views
- **URL:** dribbble.com/shots/26936563
- **Farben:** Dark bg, editorial collage-Stil, nature-Elemente, minimal color
- **Fonts:** Serif + sans, editorial balance
- **Mood:** Surreal, artistic, editorial
- **Non-Slop-Element:** Collage-Ästhetik — surreale Bildsprache statt generischer AI-Illustrationen

### Constellation — AI SaaS Startup Website
- **Designer:** LAIN — 114 Likes, 30.9k Views
- **URL:** dribbble.com/shots/26481057
- **Farben:** Very dark bg (~#050505), elegant off-white, subtle blue accent sehr dezent
- **Fonts:** Elegant serif Display + clean sans Body
- **Mood:** Minimal luxury, futuristic editorial, refined
- **Non-Slop-Element:** Wenig Elemente, maximale Wirkung. Kein Icon-Grid. Text als primäres Design-Element.

### Alyra — Web Experience
- **Designer:** Serhii Uzkyi — 17 Likes, 541 Views
- **URL:** dribbble.com/shots/27111488
- **Mood:** B2B editorial, clean dark, SaaS-meets-agency
- **Non-Slop-Element:** Dark editorial für B2B Kontext — nicht alles muss hellblau sein

### Portfolio — Magazine Style Website
- **Designer:** Ali Qadri — 15 Likes, 5.1k Views
- **URL:** dribbble.com/shots/26609616
- **Farben:** Dark bg, magazine layout, editorial grid
- **Fonts:** Strong sans + serif mix, magazine-Tradition
- **Mood:** Editorial, curated, intellectual
- **Non-Slop-Element:** Magazine-Grid auf Web — unerwartete Spaltensetzung, keine Cards

### Less.bureau — Editorial Brand Experiences
- **Designer:** Beka Kvaratskhelia
- **URL:** dribbble.com/shots/26793941
- **Farben:** Dark bg, grotesk-heavy, newspaper grid
- **Fonts:** Grotesk (helvetica-feeling), groß und bold
- **Mood:** Newspaper, dark fashion, post-modern
- **Non-Slop-Element:** Zeitungs-Ästhetik im Dark Mode — raw und intentional

### No-Code SaaS Feature Section
- **Designer:** Mike Taylor — 29 Likes, 9.4k Views
- **URL:** dribbble.com/shots/26910311
- **Mood:** Dark fintech feature, conversion-focused
- **Non-Slop-Element:** Feature-Section ohne Feature-Grid-Monotonie

### AI Advisory Firm Website
- **Designer:** Mike Taylor — 36 Likes, 6.7k Views
- **URL:** dribbble.com/shots/26909644
- **Farben:** Dark, enterprise, futuristic
- **Mood:** AI enterprise, consulting, authority
- **Non-Slop-Element:** AI-Consulting ohne Robot-Klischee

### Isaiah Rashad — Newsletter Sign Up Hero
- **Designer:** Felpis — 2 Likes, 2.9k Views
- **URL:** dribbble.com/shots/26853948
- **Farben:** Artist dark, editorial, serif, minimal
- **Mood:** Artist brand, dark editorial, lead-gen
- **Non-Slop-Element:** Lead-Gen Form als editorial Design-Element, nicht als Klotz

---

## 2. FINANCE / TAX / FINTECH

### Fintech Website Landing Page | Dark theme
- **Designer:** Akshay Hooda — 119 Likes, 29.2k Views
- **URL:** dribbble.com/shots/25983619
- **Farben:** Very dark bg (~#080C12), accent blue (~#2E6FF3), weiß
- **Mood:** Dark finance, 3D elements, trading energy
- **Non-Slop-Element:** 3D Animation statt flaches Hero. Finance-Dramatik ohne Klischee-Gold.

### Cryptfy — Crypto Trading Platform
- **Designer:** Kris Anfalova — 227 Likes, 36.7k Views
- **URL:** dribbble.com/shots/26480081
- **Farben:** Deep dark (#0A0D14), electric blue/cyan accent, white
- **Fonts:** Clean sans, stark + technical
- **Mood:** Trading precision, dark tech, professional crypto
- **Non-Slop-Element:** Technical precision statt Blockchain-Klischee. Data als Design-Element.

### Real-Time Fintech Landing Page Design
- **Designer:** Ofspace UX/UI — 114 Likes, 22.7k Views
- **URL:** dribbble.com/shots/26209801
- **Farben:** Dark corporate (#0D1117), subtle blue accent, data visualization colors
- **Mood:** Data-driven, corporate dark, real-time
- **Non-Slop-Element:** Echtzeit-Daten als visuelles Narrativ. Charts als Design-Elemente.

### Smart Banking & Fintech SaaS Website
- **Designer:** Confidency — 153 Likes, 20.4k Views
- **URL:** dribbble.com/shots/26961171
- **Mood:** Trustworthy, modern banking, SaaS-precision
- **Non-Slop-Element:** Banking ohne konservative Langeweile — modern aber seriös

### Fintech Landing Page UI — Smart Finance Platform
- **Designer:** Mike Taylor — 66 Likes, 13.1k Views
- **URL:** dribbble.com/shots/26910071
- **Farben:** Dark bg, clean blue accent, AI-dashboard feel
- **Mood:** AI-Finance, precision, enterprise
- **Non-Slop-Element:** AI-Element ohne Roboter-Klischee. Platform-Focus, conversion-orientiert.

### Finance Landing Page — Dark Mode
- **Designer:** Orizon — 89 Likes, 20.1k Views
- **URL:** dribbble.com/shots/26542480
- **Mood:** Bold finance, conversion-focused, dark mode done right
- **Non-Slop-Element:** Finance dark ohne Crypto-Ästhetik — seriöse Unternehmen

### SaaS Website — Fintech Landing Page
- **Designer:** Oripio — 123 Likes, 10k Views
- **URL:** dribbble.com/shots/26971928
- **Mood:** Modern banking SaaS, clean dark
- **Non-Slop-Element:** SaaS-meets-Finance — nicht tech-bro, aber auch nicht legacy bank

### B2B Revenue Generation — Fintech Landing Page
- **Designer:** Mike Taylor — 71 Likes, 20.9k Views
- **URL:** dribbble.com/shots/25897539
- **Mood:** B2B sales, revenue-focus, enterprise
- **Non-Slop-Element:** Sales-orientiertes Design — Hero kommuniziert ROI, kein Feature-Dump

### SwiftFunds: SaaS Fintech Landing Page
- **Designer:** Keitoto — 156 Likes, 14.4k Views
- **URL:** dribbble.com/shots/25360178
- **Farben:** Dark bg, linear.app-feeling palette, clean bento
- **Mood:** Modern SaaS, linear, dark premium
- **Non-Slop-Element:** Bento-Grid sinnvoll eingesetzt — Feature-Kommunikation ohne Grid-Monotonie

### Features Bento Grids for SaaS Fintech
- **Designer:** Keitoto — 220 Likes, 74.9k Views
- **URL:** dribbble.com/shots/24733072
- **Mood:** Data visualization, SaaS features, dark precision
- **Non-Slop-Element:** Bento als Kompositions-Tool, nicht als Trend. Jede Card hat eigene Funktion.

### Credly — Fintech Landing Page
- **Designer:** RARE LAB — 127 Likes, 36.1k Views
- **URL:** dribbble.com/shots/25685937
- **Farben:** Dark finance (~#090D15), accent blue, data-visualization colors
- **Mood:** Investments, stocks, professional trading
- **Non-Slop-Element:** Financial data als Hero-Element. Hero kommuniziert sofort den Core Value.

### Fintech Landing Page (Ofspace)
- **Designer:** Ofspace UX/UI — 77 Likes, 17.3k Views
- **URL:** dribbble.com/shots/24087689
- **Mood:** Dark finance, payment UI, clean
- **Non-Slop-Element:** Payment-Interface ohne Wallet-App-Kitsch

### Fintech Landing Page — 3D Website Animation
- **Designer:** Akshay Hooda — 74 Likes, 15k Views
- **URL:** dribbble.com/shots/26793957
- **Mood:** 3D dark fintech, organic sphere animation, voice AI
- **Non-Slop-Element:** 3D Sphere als Brand-Element statt generischem Hero Gradient

### Fintech Landing Page UI Design for Cash Management
- **Designer:** Ofspace UX/UI — 70 Likes, 17.1k Views
- **URL:** dribbble.com/shots/26947765
- **Mood:** Cash management, dark animated, finance SaaS
- **Non-Slop-Element:** Animation als strukturierendes Element, nicht Dekoration

### Accounting services & FinTech Landing Page
- **URL:** dribbble.com/shots/27191031 — 7 Likes, 1.6k Views
- **Mood:** Accounting + Fintech hybrid (relevant für SMS Steuerberatung)
- **Non-Slop-Element:** Accounting-Kontext ohne Taschenrechner-Klischee

### Modern Fintech Landing Page — Smart Investment
- **Designer:** Peno Lab — 15 Likes, 6.6k Views
- **URL:** dribbble.com/shots/26743897
- **Mood:** Dark SaaS fintech, investment platform, modern
- **Non-Slop-Element:** Investment Platform ohne Wall-Street-Klischee

### NectPay — Fintech Landing Page
- **Designer:** MultiQoS — 25 Likes, 2.1k Views
- **URL:** dribbble.com/shots/27067290
- **Mood:** Personal finance, dark, modern banking
- **Non-Slop-Element:** Personal Finance mit eigenem Character, nicht generisch

---

## 3. RECRUITMENT / KARRIERE

### Career and Recruitment — Landing Page
- **Designer:** Perevoz Design — 127 Likes, 36.2k Views
- **URL:** dribbble.com/shots/25427454
- **Mood:** Modern HR, AI-powered, professional
- **Non-Slop-Element:** HR-Platform ohne Stock-Photo-Menschen. Data-driven Visualisierung.

### dev.io — HR Webflow Design, Careers
- **Designer:** DesignUp — 438 Likes, 90.1k Views
- **URL:** dribbble.com/shots/20001396
- **Farben:** Clean minimal, light bg, professional
- **Fonts:** Strong sans, clean hierarchy
- **Mood:** Modern jobs platform, minimal, conversion-focused
- **Non-Slop-Element:** Job-Board ohne Job-Board-Klischee. Webflow-clean, keine Icon-Arrays.

### TalentBridge — Recruitment Website UI/UX
- **Designer:** Phenomenon Studio — 391 Likes, 102k Views
- **URL:** dribbble.com/shots/26530663
- **Mood:** Enterprise HR, modern talent management
- **Non-Slop-Element:** Vollständiges Design-System für Recruitment — kein Single-Page-Trick

### Career and Job Landing
- **Designer:** QClay — 683 Likes, 229k Views
- **URL:** dribbble.com/shots/24257471
- **Mood:** Aspirational career, growth journey, modern
- **Non-Slop-Element:** Karriere als Aspiration kommuniziert — nicht nur "Jobs finden"

### Job Portal Website Landing Page
- **Designer:** Suhayel Ahmed Nasim — 365 Likes, 251k Views
- **URL:** dribbble.com/shots/16022853
- **Mood:** Clean professional, functional job portal
- **Non-Slop-Element:** Bewährt durch 251k Views — funktionales Design das konvertiert

### LokerGan — Job Board Landing Page
- **Designer:** Elux Space — 306 Likes, 106k Views
- **URL:** dribbble.com/shots/18538816
- **Mood:** Modern job board, clean, employer + candidate
- **Non-Slop-Element:** Doppelte Zielgruppe elegant gelöst

### Teamora — Hiring Platform Landing Pages
- **Designer:** Vektora — 100 Likes, 6.4k Views
- **URL:** dribbble.com/shots/26830921
- **Mood:** Clean B2B hiring, SaaS-feel, modern HR
- **Non-Slop-Element:** HR-SaaS ohne Dashboard-Overload im Hero

### Olvera — HR Platform Landing Page
- **Designer:** Cansaas — 58 Likes, 7.9k Views
- **URL:** dribbble.com/shots/26567815
- **Mood:** Minimalist HR platform, B2B clean
- **Non-Slop-Element:** Responsives Design als Feature kommuniziert

### HireFlow — Responsive Landing Page
- **Designer:** Kretya Studio — 76 Likes, 15.4k Views
- **URL:** dribbble.com/shots/25370965
- **Mood:** Clean, modern, applicant-focused
- **Non-Slop-Element:** AI-Recruiting ohne AI-Buzzword-Overkill

### Clinicare — HR Recruitment in Healthcare
- **Designer:** Elux Space — 191 Likes, 17.2k Views
- **URL:** dribbble.com/shots/26341761
- **Farben:** Healthcare-appropriate palette, vertrauenswürdig
- **Mood:** Healthcare-meets-Recruitment, trust-first
- **Non-Slop-Element:** Nischen-Recruitment mit eigenem Design-Gefühl

### MedHire — Medical Recruitment Animation
- **Designer:** Elux Space — 63 Likes, 4.6k Views
- **URL:** dribbble.com/shots/27034922
- **Mood:** Medical, precision, modern animation
- **Non-Slop-Element:** Animated Hero im B2B Recruitment — selten, sofort distinctive

### Landing Page — Job Finder Jobsync
- **Designer:** Enver Studio — 123 Likes, 32.2k Views
- **URL:** dribbble.com/shots/23315835
- **Mood:** Minimalist job finder, conversion-focused
- **Non-Slop-Element:** Minimalism die konvertiert — kein Feature-Dump

### HireMind — AI Recruitment Platform
- **Designer:** Fahim Faysal — 41 Likes, 4.3k Views
- **URL:** dribbble.com/shots/27211593
- **Mood:** AI-powered Talent, modern SaaS
- **Non-Slop-Element:** AI-Feature für Recruitment ohne Roboter-Imagery

### Workora — Employee Management
- **Designer:** Tusher Sardar — 113 Likes, 6k Views
- **URL:** dribbble.com/shots/26601194
- **Mood:** HR Management, SaaS, professional
- **Non-Slop-Element:** Employee Management als Produkt mit eigenem Character

### HirePath — Job Recruitment Landing Page
- **Designer:** Shahriar Durjoy — 3 Likes, 2.2k Views
- **URL:** dribbble.com/shots/26952824
- **Mood:** Clean minimal recruitment, modern
- **Non-Slop-Element:** Recruitment ohne Bewerbungsformular-Feeling

### Qareer — AI-Powered Job Board
- **Designer:** Lumeburg Studio — 17 Likes, 3.6k Views
- **URL:** dribbble.com/shots/26989031
- **Mood:** AI job matching, clean, modern
- **Non-Slop-Element:** AI + Recruitment ohne Buzzword-Overkill

---

## 4. SAAS / B2B LANDING PAGES

### Marketing Automation Website
- **Designer:** Turja Sen Das Partho — 30 Likes, 12.1k Views
- **URL:** dribbble.com/shots/26052511
- **Mood:** Dark SaaS, CRM, Marketing Automation
- **Non-Slop-Element:** Marketing-Tool mit Dark-UI — selten, very distinctive

### SaaS Company Dark Futuristic — Framer
- **Designer:** Stylin Studio — 27 Likes, 29.2k Views
- **URL:** dribbble.com/shots/25758027
- **Mood:** Futuristic SaaS, dark premium, AI-assistant
- **Non-Slop-Element:** Framer-Quality Dark — animation-ready, sehr clean

### PlugCRM — Modern CRM SaaS Landing Page
- **Designer:** Nexila Agency — 24 Likes, 23.6k Views
- **URL:** dribbble.com/shots/26233059
- **Mood:** CRM, B2B software, sales-focused
- **Non-Slop-Element:** CRM landing ohne Salesforce-Langeweile — dark und modern

### Server Rental Service — Landing Page
- **Designer:** Stacy More — 118 Likes, 1.7k Views
- **URL:** dribbble.com/shots/27000360
- **Mood:** Technical, infrastructure, dark precision
- **Non-Slop-Element:** Technical Product mit dark editorial Design — nicht generisch IT

### Dark Social Tracking Platform — SaaS
- **Designer:** Mike Taylor — 35 Likes, 6k Views
- **URL:** dribbble.com/shots/27015042
- **Mood:** Analytics SaaS, attribution, enterprise dark
- **Non-Slop-Element:** Attribution/Analytics ohne Dashboard-Screenshot-Hero

### Clean B2B Website Concept
- **Designer:** Mike Taylor — 40 Likes, 7.3k Views
- **URL:** dribbble.com/shots/27015051
- **Mood:** Minimal B2B, conversion-focused, dark
- **Non-Slop-Element:** B2B Minimal — kein Feature-Grid, reines Value Proposition

### Managed Accounts — Enterprise Account Management
- **Designer:** Keitoto — 59 Likes, 10.3k Views
- **URL:** dribbble.com/shots/26806438
- **Mood:** Enterprise SaaS, account management, dark
- **Non-Slop-Element:** Enterprise-Kontext mit modernem Design

### Workflow Automation SaaS Landing Page
- **Designer:** Meo Studio — 33 Likes, 1.1k Views
- **URL:** dribbble.com/shots/27165356
- **Mood:** Automation, productivity, dark SaaS
- **Non-Slop-Element:** Automation als visuelles Narrativ — nicht nur "Features"

### Landing Page Design with Bento Grid & Icon System
- **Designer:** Synergy Codes — 20 Likes, 19.3k Views
- **URL:** dribbble.com/shots/26106840
- **Mood:** Dark SaaS, icon-system, bento layout
- **Non-Slop-Element:** Bento Grid mit eigenem Icon-System — kein Font Awesome

### Social Media Analytics SaaS — Landing Page
- **Designer:** Ajendra Sutariya — 30 Likes, 9.9k Views
- **URL:** dribbble.com/shots/26165101
- **Mood:** Analytics, dark SaaS, marketing tools
- **Non-Slop-Element:** Analytics Dashboard als überzeugender Hero

---

## 5. HIGH-END GENERAL LANDING PAGES (Megahits)

### ChronoTask — Landing Page
- **Designer:** Outcrowd — 2.9k Likes, 1.1M Views
- **URL:** dribbble.com/shots/25000009
- **Mood:** SaaS platform, motion-forward, bento hero
- **Non-Slop-Element:** Eines der meistgesehenen LP-Designs überhaupt — studierenswert

### Finpay — Fintech Landing Page
- **Designer:** Dipa Inhouse — 2.7k Likes, 1.3M Views
- **URL:** dribbble.com/shots/24820686
- **Mood:** Finance, animated sections, b2b clean
- **Non-Slop-Element:** Animation als strukturierendes Element, nicht Dekoration

### Trading Landing Page — Engaging Motion
- **Designer:** Roobinium — 833 Likes, 170k Views
- **URL:** dribbble.com/shots/25492218
- **Mood:** Trading energy, dark finance, motion-forward
- **Non-Slop-Element:** Motion Graphics als Hero-Storyline

### Landing Page — Travel Website
- **Designer:** Dstudio Agency — 3.3k Likes, 728k Views
- **URL:** dribbble.com/shots/12063590
- **Mood:** Premium travel, photography-first
- **Non-Slop-Element:** Photography als Layout-Struktur, nicht Background-Filler

### B2B SaaS Landing Page — HackerRank
- **Designer:** Ramotion — 1k Likes, 295k Views
- **URL:** dribbble.com/shots/26414267
- **Mood:** B2B tech, developer-focused, professional
- **Non-Slop-Element:** Ramotion's precision — kein wasted Space, pure Function

### Landing Page for Construction Company
- **Designer:** HALO LAB — 1.5k Likes, 702k Views
- **URL:** dribbble.com/shots/24175820
- **Mood:** Industrial premium, construction, bold dark
- **Non-Slop-Element:** Industrial Ästhetik mit High-End Feel — kein Bauhelm-Stock-Photo

### Sleek Landing Page — CoreShift
- **Designer:** Outcrowd — 1k Likes, 429k Views
- **URL:** dribbble.com/shots/25869450
- **Mood:** HR/SaaS, animated, bento, clean
- **Non-Slop-Element:** HR-Plattform mit Animation-First Approach

### Prodmast — Manufacturing Landing Page
- **Designer:** Dipa Inhouse — 2k Likes, 1.2M Views
- **URL:** dribbble.com/shots/24788574
- **Mood:** Industrial B2B, manufacturing, dark/light hybrid
- **Non-Slop-Element:** Manufacturing nicht langweilig — motion + clean design

### Clause — Contract Management Landing Page
- **Designer:** Dipa Inhouse — 1.7k Likes, 825k Views
- **URL:** dribbble.com/shots/23713828
- **Mood:** Legal tech, SaaS, clean animated
- **Non-Slop-Element:** Legal/Contract ohne graue Tristesse

### AI Sales — Landing Page Design
- **Designer:** Dstudio — 890 Likes, 236k Views
- **URL:** dribbble.com/shots/26404910
- **Mood:** AI-Sales, commerce, modern
- **Non-Slop-Element:** AI ohne Roboter-Metaphern

### Landing Page for AI-Powered Design System
- **Designer:** Zajno — 536 Likes, 397k Views
- **URL:** dribbble.com/shots/26057663
- **Mood:** Agency AI, dark animated, branded
- **Non-Slop-Element:** Agency Quality — Bewegung als Brand-Ausdruck

### Landing Page Design for DeepSeek AI
- **Designer:** Shakuro — 810 Likes, 619k Views
- **URL:** dribbble.com/shots/25881029
- **Mood:** AI Company, dark, minimal, powerful
- **Non-Slop-Element:** AI-Company ohne AI-Slop — sehr clean, dark editorial

### Landing Page Marketing Agency
- **Designer:** Nixtio — 1.2k Likes, 670k Views
- **URL:** dribbble.com/shots/25618155
- **Mood:** B2B Agency, dark sections + light contrast
- **Non-Slop-Element:** Agency LP die tatsächlich zeigt was Agency kann

### Modern Art Museum — Exhibition Landing Page
- **Designer:** Nixtio — 385 Likes, 82.7k Views
- **URL:** dribbble.com/shots/27001570
- **Mood:** Cultural, editorial, bold typography
- **Non-Slop-Element:** Museum-Ästhetik auf Web — schmal, typografisch, keine Icons

### Ascone — Finance Landing Page
- **Designer:** Dipa Inhouse — 1.8k Likes, 848k Views
- **URL:** dribbble.com/shots/23286378
- **Mood:** Finance B2B, animated, clean SaaS
- **Non-Slop-Element:** Finance Animation done right — kein Dashboard Screenshot als Hero

### Lattice — HR Management Landing Page
- **Designer:** Awsmd — 1.3k Likes, 561k Views
- **URL:** dribbble.com/shots/24496936
- **Mood:** HR SaaS, professional, conversion-optimized
- **Non-Slop-Element:** HR mit Character — nicht generisch grau

### Logistics Company Web Design
- **Designer:** Ronas IT — 985 Likes, 390k Views
- **URL:** dribbble.com/shots/25708252
- **Mood:** B2B Logistics, industrial, trust-first
- **Non-Slop-Element:** Logistics ohne Truck-Bilder-Klischee

### Steel Industrial Company Landing Page
- **Designer:** tubik — 369 Likes, 107k Views
- **URL:** dribbble.com/shots/26575677
- **Mood:** Industrial heritage, craft, strong material
- **Non-Slop-Element:** Industrial Material Ästhetik — Steel als Design-Sprache

### Crypto Landing Page
- **Designer:** Awsmd — 1.2k Likes, 617k Views
- **URL:** dribbble.com/shots/24753967
- **Mood:** Modern crypto, banking-crossover, dark animated
- **Non-Slop-Element:** Crypto ohne NFT-Chaos — banking-grade Design

### Football Player Landing Page
- **Designer:** Nixtio — 372 Likes, 117k Views
- **URL:** dribbble.com/shots/26940773
- **Mood:** Sports, dark, athlete-hero, bold
- **Non-Slop-Element:** Personal Brand LP für Athleten — Fotografie als Struktur

### Landing page for Social Media Management Platform
- **Designer:** Outcrowd — 727 Likes, 226k Views
- **URL:** dribbble.com/shots/26366091
- **Mood:** SaaS SMM, animated, minimal, clean
- **Non-Slop-Element:** Animation als Feature-Demonstration

### Landing Page for Mobile Banking App
- **Designer:** Conceptzilla — 737 Likes, 541k Views
- **URL:** dribbble.com/shots/25472342
- **Mood:** Mobile banking, light/clean, conversion-optimized
- **Non-Slop-Element:** Banking App LP ohne Smartphone-Mockup-Overkill

### AI Startup — SaaS Landing Page
- **Designer:** Dstudio Agency — 412 Likes, 111k Views
- **URL:** dribbble.com/shots/26470661
- **Mood:** AI Startup, community, modern SaaS
- **Non-Slop-Element:** AI Startup ohne Hype-Klischee

### Landing Page Design for Yoga Platform
- **Designer:** Paperpillar — 2.3k Likes, 1.3M Views
- **URL:** dribbble.com/shots/24325045
- **Mood:** Wellness, photography-first, clean light
- **Non-Slop-Element:** Wellness ohne Hippie-Klischee — editorial Ästhetik auf Wellness

---

## 6. BEKANNTE STUDIOS — DOKUMENTIERTE DESIGN-SYSTEME

> Exakte Farbwerte aus dokumentierten Design-Systemen. Zuverlässiger als Dribbble-Schätzungen.

### Basement Studio (Buenos Aires)
- **Signature:** Dark Brutalism, Typography-first
- **Farben:** `#0D0D0D` (bg), `#F2F0EB` (warm off-white), `#FF3B00` (red-orange accent)
- **Fonts:** Editorial New (display) + Neue Montreal oder Helvetica Now (body)
- **Layout:** Kein rounded border-radius, Marquee Text, Split-Layouts, Oversized Type
- **Non-Slop-Element:** Raw intentionality — jede Entscheidung begründbar, kein Decoration
- **Referenz:** basement.studio

### Linear
- **Signature:** Premium Dark SaaS, pixel-perfect
- **Farben:** `#050505` (bg), `#FFFFFF` (primary), `#5E6AD2` (brand purple — sehr dezent)
- **Fonts:** Inter — so eng getrackt und gewichtet, dass es nicht AI-Slop wirkt
- **Layout:** Maximum negative space, subtle glow effects, sharp cards ohne Glassmorphism
- **Non-Slop-Element:** Inter ist nicht das Problem — die execution ist das Problem. Linear beweist das.
- **Referenz:** linear.app

### Vercel
- **Signature:** Minimal high-contrast, terminal-aesthetic
- **Farben:** `#000000` (bg), `#FFFFFF` (text), `#888888` (muted gray), `#EDEDED` (light)
- **Fonts:** Geist (Vercel's eigener Font, ähnlich Inter aber eigenständig)
- **Layout:** Maximum whitespace, terminal-inspired components, sharp everything
- **Non-Slop-Element:** Schwarz/Weiß als vollständige Design-Sprache — keine Farbe als Krücke
- **Referenz:** vercel.com

### Stripe
- **Signature:** Editorial premium, colorful-but-controlled
- **Farben:** `#635BFF` (brand purple-blue), `#0A2540` (dark navy), `#00D4FF` (aqua accent), `#FFFFFF`
- **Fonts:** Sohne (ähnlich Aktiv Grotesk) — sehr clean, nicht generisch
- **Layout:** Card-based mit echtem Depth, Gradient als Information nicht Dekoration
- **Non-Slop-Element:** Farbige Gradienten die funktionieren — weil jede Farbe dem Content dient
- **Referenz:** stripe.com

### Lusion
- **Signature:** Interactive dark 3D, cinematic
- **Farben:** `#0A0A0A` (bg), project-specific accents, sehr wenig Farbe
- **Fonts:** Custom wordmarks, display serif für Projekte
- **Layout:** WebGL 3D Hero, dark backgrounds, fullscreen sections, cinematic Transitions
- **Non-Slop-Element:** 3D als Brand-Strategie, nicht als Trend — technisch und visuell überlegen
- **Referenz:** lusion.co

### Active Theory
- **Signature:** Immersive dark interactive
- **Farben:** Very dark (#080808), neon accent projekt-spezifisch, minimale Farbigkeit
- **Layout:** Heavy interaction design, 3D transitions, cursor-based interactions
- **Non-Slop-Element:** Interface als Experience — nicht als Information-Container
- **Referenz:** activetheory.net

### Studio Freight
- **Signature:** Dark editorial, strong typography, open source
- **Farben:** `#000000`, `#FFFFFF`, warme Töne projektabhängig
- **Fonts:** Editorial New (flagship), starke Serif-Tradition
- **Layout:** Large bold text, intentional whitespace, no superfluous decoration
- **Non-Slop-Element:** Open-source Design-Ethik — jede Entscheidung dokumentiert und begründet

### Rauno Freiberg (Vercel Designer)
- **Signature:** Clean functional minimalism, extreme restraint
- **Farben:** Monochromatic, black/white/gray, keine unnötige Farbe
- **Layout:** Extreme Reduktion — nur was funktional notwendig ist, bleibt
- **Non-Slop-Element:** "If in doubt, remove it" — weniger als Linear, noch funktionaler
- **Referenz:** rauno.me

### Koto Studio
- **Signature:** Brand identity + editorial, warm tones, strong typography
- **Farben:** Warm palettes, brand-specific (oft Erdtöne + starke Akzentfarbe)
- **Fonts:** Custom brand fonts, immer mit starker Persönlichkeit
- **Non-Slop-Element:** Brand als Design-Treiber — nicht UI-Patterns als Treiber
- **Referenz:** koto.studio

---

## 7. FONT-PAIRING LIBRARY (Anti-AI-Slop)

### Pair 1: Editorial Luxury (Dark) — EMPFOHLEN FÜR SUBSTRACORE / SMS
- **Display:** Cormorant Garamond (Italic für emphasis)
- **Body:** DM Mono
- **Feeling:** Intellectual authority, precision, editorial

### Pair 2: Dark Brutalist — EMPFOHLEN FÜR AGENCY / GODIA
- **Display:** Editorial New (alternativ: Neue Montreal Bold 700+)
- **Body:** Neue Montreal Regular
- **Feeling:** Raw, intentional, post-modern

### Pair 3: Modern SaaS Premium
- **Display:** Geist oder custom sans, very tight tracking
- **Body:** Geist Mono oder DM Sans
- **Feeling:** Technical precision, no decoration

### Pair 4: Finance Authority — EMPFOHLEN FÜR FINTECH
- **Display:** Freight Display Pro (Serif)
- **Body:** Aktiv Grotesk oder Sohne
- **Feeling:** Trustworthy authority, institutional credibility

### Pair 5: Warm Editorial (Hell) — EMPFOHLEN FÜR SMS KARRIERE
- **Display:** DM Serif Display
- **Body:** Plus Jakarta Sans
- **Feeling:** Approachable premium, warm but professional

### Pair 6: Minimal High-Contrast
- **Display:** Space Grotesk (bold, 700+)
- **Body:** Space Grotesk (400)
- **Feeling:** Direct, modern, no-nonsense

### Pair 7: Neo-Grotesque Power
- **Display:** Neue Haas Grotesk Display
- **Body:** Neue Haas Grotesk Text
- **Feeling:** Swiss precision, timeless, establishment

---

## 8. FARB-PALETTEN LIBRARY (Konkrete Hex-Werte)

### Palette 01: Ink on Paper (Consulting/Tax) — SMS KARRIERE OPTION
```
bg:      #F7F5F0  (warm off-white)
text:    #0D1B2A  (deep ink blue)
accent:  #0038D4  (electric blue)
muted:   #6B7280  (cool gray)
```

### Palette 02: Midnight Finance (Dark Finance)
```
bg:      #080C12
text:    #E8E4DE
accent:  #2E6FF3
muted:   #4A5568
border:  #1A2035
```

### Palette 03: Charcoal + Gold (Premium Dark)
```
bg:      #141210
text:    #F5F0E8
accent:  #C9A84C  (muted gold)
muted:   #6B6458
```

### Palette 04: Near-Black Editorial (Basement-Inspired)
```
bg:      #0D0D0D
text:    #F2F0EB
accent:  #FF3B00  (Basement-Signature)
muted:   #888888
```

### Palette 05: Terminal (Vercel-Inspired)
```
bg:      #000000
text:    #FFFFFF
muted:   #888888
border:  #333333
accent:  #EDEDED
```

### Palette 06: Warm Dark Recruitment — SMS KARRIERE DARK OPTION
```
bg:      #0A0A0A
text:    #F0EDE6
accent:  #2ECC71  (green / growth)
accent2: #D4A843  (gold / achievement)
muted:   #666666
card:    #1A1A1A
```

### Palette 07: Corporate Premium (Hell)
```
bg:      #FFFFFF
text:    #0A0A0A
accent:  #0038D4
muted:   #6B7280
border:  #E5E7EB
section: #F9FAFB
```

### Palette 08: Stripe Purple (SaaS Authority)
```
bg:      #0A2540
text:    #FFFFFF
accent:  #635BFF
accent2: #00D4FF
muted:   #8892A4
```

### Palette 09: Amber on Black (Luxury Tech)
```
bg:      #0A0806
text:    #F5F0E8
accent:  #F59E0B  (warm amber)
muted:   #6B5C44
border:  #1F1A13
```

### Palette 10: Deep Navy Editorial (Finance/Legal)
```
bg:      #0F172A
text:    #E2E8F0
accent:  #3B82F6
muted:   #64748B
border:  #1E293B
```

---

## 9. LAYOUT-PATTERN LIBRARY

### Pattern 01: Split Hero (55/45)
- Links: Headline + Sub + CTA
- Rechts: Produkt-Screenshot oder visuelle Metapher
- **Use for:** SaaS, Finance, B2B

### Pattern 02: Full-Bleed Typography Hero
- 100vw Headline (100px+), keine Bilder
- Sub-Text klein darunter, CTA links
- **Use for:** Agency, Studio, Editorial Brand

### Pattern 03: Bento Feature Grid
- Irregular Grid: 2 große + 4 kleine Cards
- Jede Card hat eigene Funktion und Visualisierung
- **Use for:** SaaS Features, Finance Dashboard, Product

### Pattern 04: Centered Minimal Hero
- Centered Headline + kurzer Sub + 2 CTAs
- Sehr viel Whitespace, minimalistische Visualisierung dahinter
- **Use for:** Linear/Vercel-Stil, Developer Tools

### Pattern 05: Scroll Narrative
- Jede Section erzählt nächsten Story-Schritt
- Sections sind thematisch sequenziell, nicht Feature-Listen
- **Use for:** Storytelling LPs, Coaching, High-Ticket Services, SMS

### Pattern 06: Photo-First Editorial
- Massives Full-Bleed Foto als Struktur
- Text ist Overlay oder daneben, nicht darüber mit Blur
- **Use for:** Restaurant, Luxury, Lifestyle, Real Estate

---

## QUICK-REFERENCE: WAS PASST WOHIN

| Use Case | Palette | Font Pair | Pattern | Referenz-Designs |
|----------|---------|-----------|---------|-----------------|
| SMS Steuerberatung Karriere | 06 (dark) oder 01 (hell) | Pair 5 (DM Serif+Jakarta) | 05 Scroll Narrative | Career&Job QClay, TalentBridge |
| Substracore Health B2B | 01 oder 10 | Pair 1 (Cormorant+DM Mono) | 01 Split Hero | Boutique Law Firm, Constellation |
| GODIA / Agency Dark | 04 | Pair 2 (Editorial New) | 02 Full-Bleed Type | Basement Studio, Verba Dark Hero |
| Finance / Tax Dark | 02 | Pair 4 (Freight+Aktiv) | 03 Bento | SwiftFunds, Credly, Ofspace |
| Recruitment / HR | 07 (hell) oder 06 | Pair 5 | 05 Scroll | TalentBridge, dev.io, LokerGan |
| SaaS Minimal | 05 | Pair 3 (Geist) | 04 Centered | Linear, Clean B2B Mike Taylor |
| Industrial / B2B Heavy | 04 oder 09 | Pair 7 (Neue Haas) | 01 Split | Steel Tubik, Construction HALO LAB |

---

## 10. DESIGN.MD BRAND LIBRARY (Production-grade Tokens)

> **106 echte Brand-Design-Systems** im DESIGN.md Format (Google Stitch Open-Source Spec) — direkt nutzbar als präzise Token-Quelle.
> Pfad: `Brain/skills/design_tokens/design-md/`
> Master-Index: `Brain/skills/design_tokens/design-md/_INDEX.md`

**Quellen:**
- VoltAgent/awesome-design-md (71 Brands, Apache 2.0)
- kwakseongjae/oh-my-design (20 zusätzliche Brands, MIT)
- Refero API (15 Editorial-Brands)

**Wann nutzen:**
- IMMER bei LP-Build → 2–3 passende Brands aus _INDEX.md picken als Token-Quelle (Hex, Typo, Spacing)
- Nicht 1:1 klauen — als Referenz für eigene Kunden-Identität nutzen
- Editorial-Look (Ute Wagner) → `monocle`, `kinfolk`, `hyperstudio`, `analogue`, `locomotive`
- SaaS/Finance → `stripe`, `linear.app`, `vercel`, `wise`, `revolut`
- Luxury/Premium → `bugatti`, `ferrari`, `lamborghini`, `apple`
- Tech-Magazine → `wired`, `theverge`, `itsnicethat`, `typewolf`

**Workflow:**
```
1. _INDEX.md scannen → 2–3 Brand-Slugs picken passend zum Kunden
2. Brain/skills/design_tokens/design-md/[slug]/DESIGN.md lesen
3. Color Tokens + Typography Stack als Inspiration in eigenes Design System übersetzen
4. AI-Slop Blacklist (Section 1) und Anti-Tropes weiterhin pflichtig
```

**Format pro Brand:**
- YAML-Frontmatter: name, description, theme, colors (Hex+Role), typography (family, sizes, weight, line-height, letter-spacing)
- Markdown-Body: Layout-Beschreibung, Imagery-Stil, Spacing, Do/Don't-Listen, Component-Specs

---

## 11. DESIGN.md STANDARD-KONVENTION (Google Labs Format, 2026+)

> **Quelle:** [google-labs-code/design.md](https://github.com/google-labs-code/design.md) — Industry-Standard für AI-Agent-readable Design-Systems (v0.1.0, April 2026, 13.8k Stars)
>
> **Zweck:** Konsistentes maschinenlesbares Format für künftige Brand-DESIGN.md Files. Bestehende 106 Files bleiben wie sie sind — nur NEUE Brand-Files folgen ab jetzt dem Standard.

### Struktur (zwei Schichten)

1. **YAML Front Matter** (maschinenlesbare Tokens, oben)
2. **Markdown Body** (menschenlesbare Rationale in `##`-Sections)

### Kanonische Sections (Reihenfolge)

```
1. Overview
2. Colors
3. Typography
4. Layout
5. Elevation & Depth
6. Shapes
7. Components
8. Do's and Don'ts
```

### Pflicht-Felder im YAML Front Matter

```yaml
---
name: BrandName
description: "Brand-Beschreibung in 1-2 Sätzen"
theme: light | dark | auto

colors:
  primary: "#1A1C1E"        # Pflicht: Hex sRGB
  secondary: "#7D8487"
  accent: "#C9A87A"
  background: "#F5F2EC"
  text-primary: "#1A1A1A"
  text-light: "#6B6B6B"

typography:
  display:
    family: "Fraunces"
    weights: [300, 400, 700]
  body:
    family: "DM Sans"
    weights: [400, 500, 700]

spacing:
  unit: 8px                  # Base unit
  scale: [4, 8, 16, 24, 32, 48, 64, 96, 128, 160]

radius:
  sm: 4px
  md: 8px
  lg: 16px
  pill: 999px

shadows:
  level-1: "0 1px 2px rgba(0,0,0,0.05)"
  level-2: "0 4px 8px rgba(0,0,0,0.08)"
  level-3: "0 8px 24px rgba(0,0,0,0.12)"
---
```

### Token-Referenzen (für DRY)

Im Markdown Body können YAML-Tokens referenziert werden:
```markdown
Primary CTA-Buttons verwenden `{colors.primary}` mit `{shadows.level-2}`.
Border-Radius: `{radius.md}`.
```

### Pflicht-Validierung pro Brand

- ✅ **WCAG AA:** Text-on-Background ≥ 4.5:1 (Body), ≥ 3:1 (Large-Display)
- ✅ **Token-Referenzen aufgelöst:** Keine ungültigen `{token}`-Verweise
- ✅ **Hex-Format:** sRGB (`#RRGGBB`), nicht HSL/HWB/OKLch (außer explizit)
- ✅ **Einheiten:** `px`, `em`, `rem` — kein `pt`, `vw` (außer typography)

### Wann das Standard-Format verwenden

- ✅ Bei **NEUEN Brand-DESIGN.md** Files ab 2026-05-15
- ✅ Bei **Discovery-Form Output** → wenn Brand-Tokens nach Discovery festgelegt werden
- ✅ Bei **Visual-Direction-Customization** → Tokens aus `VISUAL-DIRECTIONS.md` in dieses Format gießen

### Wann NICHT migrieren

- ❌ Bestehende 106 Brand-Files in `design-md/` → bleiben prose-format, keine Migration nötig
- ❌ Schnelle Mockups / Konzepte → nicht überengineering
- ❌ Single-Use-Decks ohne Brand-Wiederverwendung

### Cross-Reference

- **Visual-Directions:** `VISUAL-DIRECTIONS.md` (5 Default-Directions als Startpunkt für Tokens)
- **Discovery-Form:** `_universal/DISCOVERY-FORM.md` (Dimension 4 → liefert Brand-Inputs)
- **Use-Case-Index:** `USE-CASE-INDEX.md` (welche Tokens pro Section-Typ)

→ Diese Library ergänzt die obigen 10 Paletten + 6 Patterns — nicht ersetzt. Erst eigene Paletten/Patterns prüfen, dann Brand-Library als Präzisions-Ergänzung.
