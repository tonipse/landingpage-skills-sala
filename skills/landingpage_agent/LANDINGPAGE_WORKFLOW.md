---
name: Landing Page Workflow (Agency X Master)
description: Universeller Master-Workflow für Landing Pages. Jeder Kunde, jede Nische, jeder Funnel. Aktiviert automatisch alle relevanten Skills in der richtigen Reihenfolge.
---

# Landing Page Master-Workflow

## Wann dieser Workflow aktiv ist
Immer wenn der User sagt:
- "Bau eine Landing Page für..."
- "Erstelle eine LP für..."
- "Ich brauche eine Seite für..."
- "Funnel / Opt-In / Sales Page für..."

---

## SCHRITT 1 — Kundendaten lesen (IMMER ZUERST)

```
Lese: AGENCY X /Agency/[Kundenname]/Sources/Marketing-Thesis.md
Lese: AGENCY X /Agency/[Kundenname]/Sources/Kunden-Avatar.md
```

**Wenn kein Kundenordner vorhanden:** Frage den User nach:
1. Zielgruppe (Wer ist der ideale Kunde?)
2. Hauptproblem (Was hält ihn nachts wach?)
3. Angebot (Was wird verkauft?)
4. USP (Warum dieses Angebot, nicht ein anderes?)
5. Beweis (Testimonials, Zahlen, Cases)

---

## SCHRITT 2 — Design System generieren (ui_ux_pro_max)

```bash
python3 Brain/skills/ui_ux_pro_max/scripts/search.py "[Produkt-Typ] [Nische] [Keywords]" --design-system -p "[Kundenname]"
```

Ergebnis bestimmt:
- Farbpalette (Primär, Akzent, Hintergrund, Text)
- Font-Pairing (Display + Body)
- UI-Stil (Glassmorphism, Bento Grid, Dark Luxury, etc.)
- Anti-Patterns (was NICHT nutzen)

**Dann in `globals.css` eintragen:**
```css
:root {
  --primary: [Farbe aus Design System];
  --accent: [Farbe aus Design System];
  --bg: [Hintergrund];
  --text: [Textfarbe];
}
```

---

## SCHRITT 3 — Copy-Struktur aufbauen (landingpage_agent)

Basierend auf Kundendaten aus Schritt 1 und Design-System aus Schritt 2:

```
1. Hero (Above the Fold)
   - Eyebrow / Kicker
   - Main Headline (stärkstes Versprechen)
   - Subheadline (der Mechanismus)
   - CTA (Reibungslos, Verb zuerst)

2. Problem-Phase ("Ugly Truth")
   - Frustrations aus Kunden-Avatar.md
   - Format: "Klingt das nach dir?" oder Bullet-Points

3. Solution-Phase (Paradigmenwechsel)
   - USP aus Marketing-Thesis.md
   - Features → Benefits übersetzen

4. Social Proof
   - Konkrete Zahlen, keine Hyperbeln
   - Echte Testimonials aus Sources/

5. CTA-Sektion (Repeat)
   - Gleicher CTA wie Hero, andere Formulierung
```

---

## SCHRITT 4 — Komponenten bauen (shadcn_agent)

- Shadcn/ui für alle Basis-Komponenten
- Semantische Farb-Tokens nutzen (bg-primary, text-muted-foreground)
- 8pt Grid System (p-4, p-8, gap-8 — KEIN p-5 oder gap-3)
- Mobile-First Breakpoints
- Touch-Targets min. 44×44px

---

## SCHRITT 5 — Scroll-Animationen einbauen (scroll_animation_agent)

**IMMER aktiv — für JEDE Landing Page:**

```
Layout-Setup:
├── LenisProvider (root in layout.tsx)
├── LenisGSAPSync (Ticker Sync)
└── Animations:
    ├── HeroLoadTimeline (Hero-Bereich beim Load)
    ├── FadeInSection (alle weiteren Sektionen)
    ├── StaggeredCards (Features/Benefits)
    ├── CounterAnimation (wenn Zahlen vorhanden)
    └── MagneticButton (alle CTAs)
```

**Mobile Config immer setzen:**
```tsx
ScrollTrigger.normalizeScroll(true)
ScrollTrigger.config({ ignoreMobileResize: true })
// Lenis: smoothTouch: false
```

**prefers-reduced-motion immer prüfen** vor jeder Animation.

---

## SCHRITT 6 — 3D Effekte (web_animation_3d_agent)

⚠️ **NUR wenn der User explizit erwähnt:**
- "mit 3D Effekten"
- "3D Animationen"
- "3D in der Hero Sektion"
- "Spline"
- "React Three Fiber"

**Wenn 3D gewünscht:**
- Spline für fertige 3D Objekte → `@splinetool/react-spline/next`
- R3F für Custom 3D → `@react-three/fiber@^9.5.0`
- Immer mit `Suspense` wrappen
- `dpr={[1, 2]}` für Mobile Performance
- `transpilePackages` in `next.config.js` setzen

**Wenn NICHT erwähnt → KEIN 3D.**

---

## SCHRITT 7 — Mobile-Check (PFLICHT vor Fertigstellung)

```
[ ] Alle Animationen nutzen transform + opacity (nicht margin/height/width)
[ ] background-attachment: fixed NIRGENDWO verwendet
[ ] Lenis smoothTouch: false
[ ] ScrollTrigger.normalizeScroll(true) gesetzt
[ ] ScrollTrigger.config({ ignoreMobileResize: true }) gesetzt
[ ] prefers-reduced-motion in allen Animations-Komponenten
[ ] Touch-Targets min. 44×44px
[ ] Keine horizontalen Scrollbars
[ ] Breakpoints: 375px, 768px, 1024px, 1440px
[ ] Bilder mit next/image (automatische Optimierung)
[ ] Fonts via next/font (kein FOUT)
[ ] will-change max auf 3-5 Elementen gleichzeitig
```

---

## TECHNISCHER STACK (Standard für jede LP)

```json
{
  "framework": "Next.js 15 (App Router)",
  "styling": "Tailwind CSS v4 + shadcn/ui",
  "animations": "GSAP 3.12 + Framer Motion 11",
  "scroll": "lenis ^1.x",
  "fonts": "next/font/google",
  "images": "next/image",
  "icons": "lucide-react (SVG, keine Emojis)"
}
```

**next.config.js Standard:**
```js
const nextConfig = {
  transpilePackages: [], // Nur bei 3D: ['three', '@react-three/fiber', '@react-three/drei']
}
module.exports = nextConfig
```

---

## SKILL-REIHENFOLGE (immer in dieser Sequenz)

```
1. [Daten]    → Marketing-Thesis.md + Kunden-Avatar.md lesen
2. [Design]   → ui_ux_pro_max (Design System generieren)
3. [Copy]     → landingpage_agent (Texte schreiben)
4. [Code]     → shadcn_agent (Komponenten bauen)
5. [Motion]   → scroll_animation_agent (immer aktiv)
6. [3D]       → web_animation_3d_agent (NUR auf explizite Anfrage)
7. [Check]    → Mobile-Checklist durchgehen
```

---

## UNIVERSALITÄT — funktioniert für jeden Use-Case

| Nische | Anpassung |
|--------|-----------|
| B2B Coaching/Agentur | Dark Luxury oder Clean Authority Stil, Authority Social Proof |
| SaaS / Tech | Modern Dark oder Clean Light, Feature Bento Grid |
| E-Commerce | Produkt-Hero, Lifestyle Bilder, Review Marquee |
| Health / Wellness | Warm Tones, Soft UI, Trust-Signale |
| Finance / Legal | Seriös, Minimal, Zahlen-fokussiert |
| Creative / Agency | Bold, Scroll-Heavy, Awwwards-Level |

**Das Design-System (Schritt 2) passt den Stil automatisch an — kein manuelles Entscheiden nötig.**
