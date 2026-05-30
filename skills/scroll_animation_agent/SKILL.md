---
name: Scroll Animation Agent (Agency X)
description: Mobile-safe Scroll-Animationen für Landing Pages + Dashboards. Immer aktiv wenn eine LP gebaut wird. GSAP (komplett frei seit April 2025) + Lenis Smooth Scroll + Motion (ex Framer Motion). Mit CSS Native Scroll-Driven Animations für simple Cases. KEIN 3D — dafür web_animation_3d_agent nutzen.
version: 2.0
updated: 2026-05-20
---

# Scroll Animation Agent

## Identität
Du bist der Scroll-Animations-Spezialist für Agency X. Dieser Skill feuert **immer** wenn eine Landing Page oder Dashboard gebaut wird — unabhängig vom Kunden, der Nische oder dem Funnel. Dein Output ist immer **mobile-safe, performant und zugänglich.**

**WICHTIG:** Dieser Skill enthält KEIN R3F, KEIN Spline, KEIN Three.js. Für 3D → `web_animation_3d_agent` nutzen, aber NUR wenn explizit danach gefragt wird.

---

## 🆕 2026 BIG NEWS (kritisches Update vs. 2025)

### GSAP ist seit April 2025 100% FREI für alle Use-Cases
**Webflow hat GSAP übernommen (Herbst 2024) und Stand April 2025 alle Premium-Plugins kostenlos freigegeben.** Keine Club-Greensock-Subscription mehr nötig.

**Plugins die JETZT frei nutzbar sind:**
- `SplitText` (neu geschrieben, performance-optimiert) — Text-Reveal pro Zeichen/Wort/Zeile
- `ScrollSmoother` — Alternative zu Lenis bei reinem GSAP-Setup
- `MorphSVG` — SVG-Path-Morphing
- `DrawSVG` — Stroke-Reveal-Animationen
- `Physics2D`, `InertiaPlugin`, `MotionPathPlugin`, `Flip`

Quelle: https://webflow.com/blog/gsap-becomes-free

### Motion (ex Framer Motion) — REBRAND
- Paket heißt jetzt `motion`, nicht mehr `framer-motion`
- Import: `import { motion } from "motion/react"` (nicht mehr `framer-motion`)
- Funktioniert mit React Server Components / Next.js 15+
- Vanilla-API verfügbar (Vue, vanilla JS)

### CSS Native Scroll-Driven Animations (Game-Changer)
**Safari 26.5 + Chrome/Edge 135+ supportieren jetzt `animation-timeline: scroll() / view()`.**

Was pure CSS jetzt kann (was vorher nur GSAP konnte):
- Parallax (subtil)
- Reveal-on-scroll
- Sticky-Scrub
- View-based Animations
- Scroll-driven Carousels ohne JS

**Performance:** läuft auf Compositor-Thread, 60fps, KEINE scroll-listener nötig.

**Regel:** Für SIMPLE Cases → CSS Native. Für KOMPLEXE Cases (pin, snap, timeline-orchestration) → GSAP.

---

## PAKETE & VERSIONEN (2026-05-20)

```json
{
  "lenis": "^1.x.x",
  "gsap": "^3.15.x",
  "@gsap/react": "^2.1.x",
  "motion": "^12.x.x"
}
```

**Migrations-Hinweise:**
- Alt: `"framer-motion": "^11.x.x"` → Neu: `"motion": "^11.x.x"`
- Alt: `import { motion } from "framer-motion"` → Neu: `import { motion } from "motion/react"`
- Alt: `"@studio-freight/lenis"` → schon länger: `"lenis"`

---

## LENIS — Smooth Scroll (Mobile-Safe Setup)

```tsx
// providers/LenisProvider.tsx
'use client'
import { ReactLenis } from 'lenis/react'

export function LenisProvider({ children }: { children: React.ReactNode }) {
  return (
    <ReactLenis
      root
      options={{
        duration: 1.2,
        smoothWheel: true,
        syncTouch: false,        // KRITISCH: false — iOS/Android nativ scroll, kein Lenis-Touch
        touchMultiplier: 2,
        infinite: false,
      }}
    >
      {children}
    </ReactLenis>
  )
}
```

**Wichtiger Update-Hinweis 2026:**
- ❌ `smoothTouch` ist DEPRECATED (entfernt aus Lenis)
- ✅ Nur noch `syncTouch: false` setzen — Native Touch-Scroll auf Mobile

**Lenis-Alternative:** Bei reinem GSAP-Setup → `ScrollSmoother` (jetzt frei) statt Lenis.

---

## GSAP ScrollTrigger — Mobile-Safe Config (PFLICHT)

```tsx
'use client'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import { useGSAP } from '@gsap/react'

gsap.registerPlugin(ScrollTrigger, useGSAP)

// MOBILE CONFIG — immer beim Setup einbinden
ScrollTrigger.normalizeScroll(true)         // Fixiert iOS Safari Address-Bar Jitter
ScrollTrigger.config({ ignoreMobileResize: true })
```

**Lenis + GSAP ScrollTrigger synchronisieren:**
```tsx
// providers/LenisGSAPSync.tsx
'use client'
import { useEffect } from 'react'
import { useLenis } from 'lenis/react'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

export function LenisGSAPSync() {
  const lenis = useLenis()

  useEffect(() => {
    if (!lenis) return
    lenis.on('scroll', ScrollTrigger.update)
    const update = (time: number) => lenis.raf(time * 1000)
    gsap.ticker.add(update)
    gsap.ticker.lagSmoothing(0)
    return () => {
      lenis.off('scroll', ScrollTrigger.update)
      gsap.ticker.remove(update)
    }
  }, [lenis])

  return null
}
```

---

## CSS NATIVE SCROLL-DRIVEN ANIMATIONS (2026 Bevorzugt für simple Cases)

### Parallax mit pure CSS
```css
@keyframes parallax-up {
  from { transform: translateY(0); }
  to { transform: translateY(-20%); }
}

.parallax-image {
  animation: parallax-up linear;
  animation-timeline: scroll(root block);
  animation-range: entry exit;
}
```

### Reveal-on-Scroll (Compositor-Thread)
```css
@keyframes reveal {
  from { opacity: 0; transform: translateY(40px); }
  to   { opacity: 1; transform: translateY(0); }
}

.reveal-section {
  animation: reveal linear both;
  animation-timeline: view();
  animation-range: entry 0% entry 80%;
}
```

### Sticky-Scrub Progress-Indicator
```css
@keyframes progress {
  from { width: 0%; }
  to { width: 100%; }
}

.scroll-progress {
  animation: progress linear;
  animation-timeline: scroll(root block);
  position: fixed; top: 0;
}
```

**Browser-Fallback (Safari < 26.5 / alte Browser):**
```css
@supports not (animation-timeline: scroll()) {
  /* GSAP-Fallback per JS einsetzen */
}
```

**Wann CSS Native nutzen:**
- ✅ Simple Parallax (1-2 Layer)
- ✅ Single-Element Reveal-on-Scroll
- ✅ Sticky-Progress-Bars
- ❌ NICHT bei: pinned sections, scroll-triggered timelines, snap-points → da bleibt GSAP überlegen

---

## PREFERS-REDUCED-MOTION (PFLICHT — Accessibility)

```tsx
// hooks/useReducedMotion.ts
'use client'
import { useEffect, useState } from 'react'

export function useReducedMotion() {
  const [prefersReduced, setPrefersReduced] = useState(false)

  useEffect(() => {
    const mq = window.matchMedia('(prefers-reduced-motion: reduce)')
    setPrefersReduced(mq.matches)
    const handler = (e: MediaQueryListEvent) => setPrefersReduced(e.matches)
    mq.addEventListener('change', handler)
    return () => mq.removeEventListener('change', handler)
  }, [])

  return prefersReduced
}
```

**In allen Animations-Komponenten nutzen:**
```tsx
const prefersReduced = useReducedMotion()

useGSAP(() => {
  if (prefersReduced) return
  // ... Animations-Code
}, { scope: containerRef })
```

**CSS-Pendant:**
```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## SCROLL-ANIMATION PATTERNS (Mobile-Safe, GSAP-basiert)

### 1. Fade-In beim Scrollen (bestes Performance/Effekt Verhältnis)
```tsx
'use client'
import { useRef } from 'react'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import { useGSAP } from '@gsap/react'
import { useReducedMotion } from '@/hooks/useReducedMotion'

gsap.registerPlugin(ScrollTrigger, useGSAP)

export function FadeInSection({ children }: { children: React.ReactNode }) {
  const ref = useRef<HTMLDivElement>(null)
  const prefersReduced = useReducedMotion()

  useGSAP(() => {
    if (prefersReduced) return
    gsap.from(ref.current, {
      opacity: 0,
      y: 40,
      duration: 0.8,
      ease: 'power3.out',
      scrollTrigger: {
        trigger: ref.current,
        start: 'top 85%',
        end: 'bottom 20%',
      }
    })
  }, { scope: ref })

  return <div ref={ref}>{children}</div>
}
```

### 2. Staggered Cards (Feature-Sektion)
```tsx
useGSAP(() => {
  if (prefersReduced) return
  gsap.from('.feature-card', {
    opacity: 0,
    y: 60,
    duration: 0.7,
    stagger: 0.15,
    ease: 'power3.out',
    scrollTrigger: {
      trigger: '.features-grid',
      start: 'top 80%',
    }
  })
}, { scope: containerRef })
```

### 3. SplitText Reveal (JETZT FREI — 2026 Premium-Feature)
```tsx
import SplitText from 'gsap/SplitText'
gsap.registerPlugin(SplitText)

useGSAP(() => {
  if (prefersReduced) return
  const split = new SplitText('.headline', { type: 'words,chars' })
  gsap.from(split.chars, {
    opacity: 0,
    y: 80,
    rotateX: -90,
    duration: 0.8,
    stagger: 0.02,
    ease: 'power3.out',
    scrollTrigger: { trigger: '.headline', start: 'top 75%' }
  })
}, { scope: heroRef })
```

### 4. Text Reveal (Clip-Path — GPU-accelerated)
```tsx
useGSAP(() => {
  if (prefersReduced) return
  gsap.from('.reveal-text', {
    clipPath: 'inset(0 100% 0 0)',
    duration: 1.2,
    stagger: 0.2,
    ease: 'power4.inOut',
    scrollTrigger: {
      trigger: '.reveal-text',
      start: 'top 75%',
    }
  })
}, { scope: containerRef })
```

### 5. Hero Load Timeline
```tsx
useGSAP(() => {
  if (prefersReduced) return
  const tl = gsap.timeline({ delay: 0.2 })
  tl.from('.hero-eyebrow', { y: 20, opacity: 0, duration: 0.6, ease: 'power3.out' })
    .from('.hero-headline', { y: 60, opacity: 0, duration: 0.9, stagger: 0.08, ease: 'power4.out' }, '-=0.3')
    .from('.hero-sub', { y: 30, opacity: 0, duration: 0.7, ease: 'power3.out' }, '-=0.5')
    .from('.hero-cta', { scale: 0.9, opacity: 0, duration: 0.5, ease: 'back.out(1.7)' }, '-=0.3')
}, { scope: heroRef })
```

### 6. Parallax (Mobile-Safe — NUR mit transform, NIEMALS background-attachment: fixed)
```tsx
useGSAP(() => {
  if (prefersReduced) return
  gsap.to('.parallax-img', {
    yPercent: -20,
    ease: 'none',
    scrollTrigger: {
      trigger: '.parallax-section',
      start: 'top bottom',
      end: 'bottom top',
      scrub: true,
    }
  })
}, { scope: containerRef })
```

### 7. Horizontal Scroll (Pinned Section)
```tsx
useGSAP(() => {
  if (prefersReduced) return
  const panels = gsap.utils.toArray<HTMLElement>('.h-panel')
  gsap.to(panels, {
    xPercent: -100 * (panels.length - 1),
    ease: 'none',
    scrollTrigger: {
      trigger: '.h-scroll-container',
      pin: true,
      scrub: 1,
      snap: 1 / (panels.length - 1),
      end: () => '+=' + (document.querySelector('.h-scroll-container') as HTMLElement).offsetWidth
    }
  })
}, { scope: containerRef })
```

### 8. Counter Animation
```tsx
useGSAP(() => {
  if (prefersReduced) return
  const counters = gsap.utils.toArray<HTMLElement>('.counter')
  counters.forEach(counter => {
    const target = parseInt(counter.dataset.target || '0')
    gsap.from({ value: 0 }, {
      value: target,
      duration: 2,
      ease: 'power2.out',
      snap: { value: 1 },
      scrollTrigger: { trigger: counter, start: 'top 80%' },
      onUpdate: function() { counter.textContent = Math.round(this.targets()[0].value).toString() }
    })
  })
}, { scope: containerRef })
```

---

## MOTION (ex Framer Motion) — Micro-Interactions

### Magnetic Button (CTA Buttons)
```tsx
'use client'
import { useRef } from 'react'
import { motion, useSpring } from 'motion/react'

export function MagneticButton({ children, className }: { children: React.ReactNode; className?: string }) {
  const ref = useRef<HTMLButtonElement>(null)
  const x = useSpring(0, { stiffness: 150, damping: 15 })
  const y = useSpring(0, { stiffness: 150, damping: 15 })

  const onMove = (e: React.MouseEvent) => {
    const rect = ref.current?.getBoundingClientRect()
    if (!rect) return
    x.set((e.clientX - rect.left - rect.width / 2) * 0.35)
    y.set((e.clientY - rect.top - rect.height / 2) * 0.35)
  }

  return (
    <motion.button
      ref={ref}
      style={{ x, y }}
      onMouseMove={onMove}
      onMouseLeave={() => { x.set(0); y.set(0) }}
      whileTap={{ scale: 0.95 }}
      className={className}
    >
      {children}
    </motion.button>
  )
}
```

### Infinite Marquee (Social Proof / Logo Ticker)
```tsx
'use client'
import { motion } from 'motion/react'

export function Marquee({ items, speed = 20 }: { items: string[]; speed?: number }) {
  return (
    <div className="overflow-hidden flex" aria-hidden="true">
      {[0, 1].map((i) => (
        <motion.div
          key={i}
          animate={{ x: ['0%', '-100%'] }}
          transition={{ duration: speed, repeat: Infinity, ease: 'linear' }}
          className="flex gap-8 pr-8 shrink-0"
        >
          {items.map((item, j) => <span key={j}>{item}</span>)}
        </motion.div>
      ))}
    </div>
  )
}
```

### Hover Card Lift
```tsx
<motion.div
  whileHover={{ y: -8, boxShadow: '0 20px 60px rgba(0,0,0,0.15)' }}
  transition={{ duration: 0.3, ease: [0.22, 1, 0.36, 1] }}
>
  {/* Card Content */}
</motion.div>
```

---

## DASHBOARD-SPEZIFISCHE PATTERNS (2026 Best Practices)

### Chart-Animations (Recharts v3 mit WAAPI)
Recharts v3 nutzt jetzt **WAAPI** statt CSS-Transitions → signifikant smoother auf Low-End-Devices. Tremor (gebaut auf Recharts + Radix) profitiert automatisch.

```tsx
// Tremor + Recharts v3 — automatisch smooth via WAAPI
import { AreaChart } from '@tremor/react'

<AreaChart
  data={data}
  index="date"
  categories={['Revenue']}
  showAnimation={true}
  animationDuration={900}
/>
```

### Skeleton-Loader 2026 — Shimmer From Structure
**NEU 2026:** `shimmer-from-structure` scannt Runtime-DOM und generiert passende Skeletons automatisch. Game-Changer gegen Layout-Duplikation.

→ Repo: `darula-hpp/shimmer-from-structure` (React/Vue/Svelte)

```tsx
import { ShimmerFromStructure } from 'shimmer-from-structure'

<ShimmerFromStructure isLoading={!data}>
  <DashboardCard data={data} />
</ShimmerFromStructure>
```

### Live-Indikator (Pulse + Glow)
```tsx
// motion/react — Live-Status
<motion.div
  animate={{ opacity: [1, 0.5, 1] }}
  transition={{ duration: 1.5, repeat: Infinity, ease: 'easeInOut' }}
  className="w-2 h-2 rounded-full bg-emerald-500"
/>
```

---

## OPTIONALE PLUGINS / MCP-SERVER (2026)

### GSAP Master MCP Server (Empfehlung)
**Repo:** `bruzethegreat/gsap-master-mcp-server`
Most comprehensive GSAP MCP Server, AI-Intent-Analysis, alle Plugins.

Install (user-weit):
```bash
cd ~/.claude/plugins/marketplaces
git clone https://github.com/bruzethegreat/gsap-master-mcp-server.git
```

### Offizieller GSAP Skills Plugin
**Repo:** `greensock/gsap-skills`
Direkt von GreenSock maintained.

```bash
/plugin marketplace add greensock/gsap-skills
/plugin install gsap-skills@greensock
```

### Niche-Alternatives (Performance-kritisch)
- **Trig.js** (4KB CSS-first scroll-observer) — für Performance-kritische LPs
- **locomotive-scroll v5** (Lenis-Wrapper mit Parallax-Bonus) — wenn Lenis nicht reicht
- **anime.js v4** (66k⭐, TypeScript-nativ, tree-shakeable) — für leichtgewichtige UI-Animations

### Vorsicht
- **Theatre.js** — privates Repo seit Mitte 2024, eventuell sterbend. **NICHT für Production** bis 1.0 public.

---

## 🆕 VIEW TRANSITIONS API (2026 Standard für Page-Übergänge)

Seit Chrome 111 (SPA-Variante), Safari 18+, Firefox 144 verfügbar. Für LP-Funnels mit Sub-Pages, Step-Funnels oder Modal-Transitions **deutlich performanter** als JS-Framework-Routing.

**Vorteile:**
- Native — kein zusätzliches Bundle
- INP-Impact <70ms bei `transform`+`opacity` only
- Pairing mit Speculation Rules → "essentially nothing to wait for"
- Funktioniert mit Next.js 15 App Router

### Basic-Setup (CSS)

```css
::view-transition-old(root),
::view-transition-new(root) {
  animation-duration: 0.3s;          /* MAX 300ms — sonst Sluggish */
  animation-timing-function: cubic-bezier(0.22, 1, 0.36, 1);
}

/* Named-Transition pro Section */
.hero-image {
  view-transition-name: hero-image;
  contain: layout;
}
```

### Trigger via JS (SPA-Style)

```tsx
function navigate(url: string) {
  if (!document.startViewTransition) {
    window.location.href = url
    return
  }
  document.startViewTransition(() => {
    // DOM-Updates hier
    window.location.href = url
  })
}
```

**Wann nutzen:**
- ✅ Multi-Page-Funnels (LP → Calendly → Thank-You)
- ✅ Modal-Open/Close mit Content-Switch
- ✅ Tab-Switches mit Content-Animation
- ❌ NICHT für komplexe scroll-driven Animations (da bleibt GSAP überlegen)

---

## 🆕 CONTENT-VISIBILITY für lange LPs (Performance-Boost)

`content-visibility: auto` lässt Browser Off-Screen-Sections skippen — **LCP/INP-Boost** bei langen LPs.

```css
.lp-section {
  content-visibility: auto;
  contain-intrinsic-size: 0 800px;   /* Platzhalter-Höhe für Scroll-Stabilität */
}
```

**Wann nutzen:**
- ✅ LPs mit 8+ Sections
- ✅ Long-Form-Content (Sales-Pages)
- ❌ NICHT bei Hero-Section (immer above-the-fold)
- ❌ NICHT wenn `contain-intrinsic-size` nicht bekannt ist (verursacht CLS)

---

## INTERAKTIVE MIKRO-ANIMATIONEN: Rive vs Lottie 2026

### Rive (empfohlen für interaktive Elements)
- 10-100× kleiner als unkomprimiertes JSON-Lottie
- 15-50KB für komplexe interaktive Animations
- State-Machine-basiert (Hover → Click → Active)
- Mobile: ~60fps

**Use-Cases:** CTAs, Mascots, Trust-Badges, Onboarding-Flows

### Lottie 2026 — hat Lücke geschlossen
- **dotLottie** (40-70% kleiner als JSON-Lottie)
- **dotLottie State Machines** (seit Ende 2025) — interaktive Animations mit Triggern
- **iOS ThorVG Renderer** (nativer Multithreading-Renderer, deutlich performanter als Legacy)
- Mobile mit dotLottie: spürbar smoother als JSON-Lottie

**Verdict:** Für KOMPLEXE interaktive Animations → Rive. Für Marketing-Animations aus After Effects → dotLottie.

---

## MOBILE DON'TS (Strikte Regeln)

```
❌ background-attachment: fixed → kaputt auf iOS Safari, NIEMALS nutzen
❌ Blur/Filter bei Scroll → zu teuer, nur bei Hover erlaubt
❌ Mehr als 3 Parallax-Layer → laggt auf Mobile
❌ Lenis smoothTouch: true → DEPRECATED, entfernt
❌ will-change auf vielen Elementen → erhöht Memory
❌ CSS scroll-snap mit Lenis mischen → Konflikte
❌ Animationen ohne prefers-reduced-motion Check
❌ JSON-Lottie ohne dotLottie-Compression auf Mobile
```

## PERFORMANCE REGELN

```
✅ Nur transform + opacity animieren (GPU-Pfad)
✅ will-change: transform sparsam (max 3-5 Elemente, danach auf 'auto' zurück)
✅ gsap.ticker statt requestAnimationFrame direkt
✅ ScrollTrigger.normalizeScroll(true) für iOS
✅ ScrollTrigger.config({ ignoreMobileResize: true })
✅ useGSAP mit scope — verhindert Memory Leaks
✅ Suspense für schwere Komponenten
✅ prefers-reduced-motion immer prüfen
✅ CSS Native scroll-driven für simple Cases (Compositor-Thread)
✅ Trigger-Anzahl < 30 pro Seite (INP-Penalty bei mehr)
```

---

## VOLLSTÄNDIGE LAYOUT-ARCHITEKTUR (LP)

```
layout.tsx
└── LenisProvider                    ← Smooth Scroll Root
    ├── LenisGSAPSync                ← Ticker Sync (einmalig)
    └── page.tsx
        ├── HeroSection
        │   ├── HeroLoadTimeline     ← GSAP (kein Scroll nötig)
        │   ├── SplitText Reveal     ← GSAP (jetzt FREI)
        │   └── MagneticButton       ← Motion CTA
        ├── FeaturesSection
        │   ├── FadeInSection        ← GSAP ScrollTrigger ODER CSS Native
        │   └── StaggeredCards       ← GSAP ScrollTrigger
        ├── SocialProofSection
        │   ├── CounterAnimation     ← GSAP ScrollTrigger
        │   └── Marquee              ← Motion
        ├── ParallaxSection          ← CSS Native (simple) ODER GSAP Scrub (komplex)
        └── CTASection
            └── FadeInSection        ← CSS Native (animation-timeline: view())
```

## VOLLSTÄNDIGE LAYOUT-ARCHITEKTUR (Dashboard)

```
DashboardLayout
├── Header
│   └── LiveIndicator           ← Motion (pulse)
├── ChartGrid
│   ├── Recharts v3 / Tremor    ← WAAPI automatisch (smooth)
│   └── ShimmerFromStructure    ← Auto-Skeleton beim Loading
└── DataTables
    └── Motion list-animations
```

---

## CROSS-REFERENCES

- **3D-Animationen** (R3F, Spline, WebGPU): `web_animation_3d_agent/SKILL.md`
- **Design Tokens**: `design_tokens/design.md` (Animation Timing Curves, Easing-System)
- **UI/UX Best Practices**: `ui_ux_pro_max/SKILL.md`
- **Visual Directions**: `design_tokens/VISUAL-DIRECTIONS.md` (Direction 6 KINETIC/LIQUID nutzt diesen Skill)
