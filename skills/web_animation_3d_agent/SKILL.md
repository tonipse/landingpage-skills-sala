---
name: 3D Animation Agent (Agency X)
description: NUR für echtes 3D — React Three Fiber v9 stable und Spline. Wird AUSSCHLIESSLICH aktiviert wenn der User explizit "3D" oder "3D Effekte" oder "3D Animationen" erwähnt. Für Scroll-Effekte → scroll_animation_agent nutzen. Für interaktive Mikro-Animations (CTAs, Mascots) → Rive in scroll_animation_agent.
version: 2.0
updated: 2026-05-20
---

# 3D Animation & Web Motion Agent

## Identität
Du bist ein preisgekrönter Creative Developer für Agency X. Awwwards-Level ist dein Standard.
Deine Werkzeuge: **GSAP 3.15+ (komplett frei seit April 2025)**, **Motion (ex Framer Motion)**, **React Three Fiber v9 stable**, **Lenis**, **Spline**.

---

## 🆕 2026 BIG NEWS

### React Three Fiber v10 ist in ALPHA — Production: bleibt bei v9
- **v9.5+ ist current stable** — KEIN Wechsel zu v10 vor Stable-Release
- v10 Alpha bringt: WebGPURenderer + WebGLRenderer parallel, neuer Scheduler, TSL first-class
- Drei 11 alpha läuft parallel

### Three.js r184 (Mai 2026 current)
- **WebGPU production-ready in current Three.js** mit automatischem WebGL2-Fallback
- **TSL (Three Shading Language)** — Node-basierter Shader-Graph, renderer-agnostic (kompiliert zu WGSL und GLSL)
- Safari 26+ unterstützt WebGPU — alle major Browser jetzt abgedeckt
- r182 ESLint 9 flat config, r183 deprecated code removal — Migration-Notes checken bei Updates

### Motion (ex Framer Motion) — REBRAND
- Paket: `motion`, Import: `motion/react`
- Funktioniert mit React Server Components / Next.js 15+

---

## KRITISCH: Pakete & Versionen (Next.js 15 + React 19, Stand 2026-05-20)

```json
{
  "@react-three/fiber": "^9.5.0",
  "@react-three/drei": "^10.7.7",
  "three": "^0.184.0",
  "gsap": "^3.15.x",
  "@gsap/react": "^2.1.x",
  "lenis": "^1.x.x",
  "@splinetool/react-spline": "^4.1.0",
  "motion": "^12.x.x"
}
```

**Migrations-Hinweise:**
- Alt: `"framer-motion": "^11.x.x"` → Neu: `"motion": "^11.x.x"`
- Alt: `import { motion } from "framer-motion"` → Neu: `import { motion } from "motion/react"`

**next.config.js — PFLICHT für R3F:**
```js
const nextConfig = {
  transpilePackages: ['three', '@react-three/fiber', '@react-three/drei']
}
module.exports = nextConfig
```

**WICHTIG:**
- `@studio-freight/lenis` ist DEPRECATED → immer das neue `lenis` Package
- R3F v8 ist NICHT kompatibel mit React 19 / Next.js 15 → immer v9
- R3F v10 alpha NICHT in Production verwenden
- GSAP 3.15+ ist komplett FREI (Webflow-Acquisition, alle Premium-Plugins inklusive)

---

## LENIS — Smooth Scroll (2025 korrekt)

```tsx
// providers/LenisProvider.tsx
'use client'
import { ReactLenis } from 'lenis/react'

export function LenisProvider({ children }: { children: React.ReactNode }) {
  return (
    <ReactLenis root options={{ duration: 1.2, smoothWheel: true }}>
      {children}
    </ReactLenis>
  )
}
// In layout.tsx: <LenisProvider><App /></LenisProvider>
```

**Lenis + GSAP ScrollTrigger synchronisieren:**
```tsx
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
    const update = (time: number) => lenis.raf(time * 1000)
    gsap.ticker.add(update)
    gsap.ticker.lagSmoothing(0)
    return () => gsap.ticker.remove(update)
  }, [lenis])
  return null
}
```

---

## GSAP — ScrollTrigger (ohne Hydration-Fehler)

```tsx
'use client'
import { useRef } from 'react'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import { useGSAP } from '@gsap/react'

gsap.registerPlugin(ScrollTrigger, useGSAP)

export function ScrollSection() {
  const containerRef = useRef<HTMLDivElement>(null)

  useGSAP(() => {
    gsap.from('.reveal-text', {
      y: 80, opacity: 0, duration: 1, stagger: 0.15, ease: 'power4.out',
      scrollTrigger: { trigger: '.reveal-text', start: 'top 80%' }
    })
  }, { scope: containerRef }) // scope = Memory Leak Schutz

  return <div ref={containerRef}><h2 className="reveal-text">Headline</h2></div>
}
```

### Hero Reveal (Page Load Timeline):
```tsx
'use client'
import { useRef } from 'react'
import gsap from 'gsap'
import { useGSAP } from '@gsap/react'

gsap.registerPlugin(useGSAP)

export function HeroReveal() {
  const ref = useRef<HTMLDivElement>(null)

  useGSAP(() => {
    const tl = gsap.timeline()
    tl.from('.hero-eyebrow', { y: 20, opacity: 0, duration: 0.6, ease: 'power3.out' })
      .from('.hero-headline', { y: 80, opacity: 0, duration: 1, stagger: 0.1, ease: 'power4.out' }, '-=0.3')
      .from('.hero-sub', { y: 40, opacity: 0, duration: 0.8, ease: 'power3.out' }, '-=0.5')
      .from('.hero-cta', { scale: 0.8, opacity: 0, duration: 0.6, ease: 'back.out(1.7)' }, '-=0.4')
  }, { scope: ref })

  return (
    <div ref={ref}>
      <span className="hero-eyebrow">Eyebrow Text</span>
      <h1 className="hero-headline">Main Headline</h1>
      <p className="hero-sub">Subtext</p>
      <button className="hero-cta">CTA</button>
    </div>
  )
}
```

### Clip-Path Reveal:
```tsx
useGSAP(() => {
  gsap.from('.clip-reveal', {
    clipPath: 'inset(0 100% 0 0)',
    duration: 1.2, stagger: 0.2, ease: 'power4.inOut',
    scrollTrigger: { trigger: '.clip-reveal', start: 'top 75%' }
  })
}, { scope: containerRef })
```

### Horizontaler Scroll (Pinned):
```tsx
useGSAP(() => {
  const panels = gsap.utils.toArray<HTMLElement>('.panel')
  gsap.to(panels, {
    xPercent: -100 * (panels.length - 1),
    ease: 'none',
    scrollTrigger: {
      trigger: '.horizontal-scroll',
      pin: true, scrub: 1,
      snap: 1 / (panels.length - 1),
      end: () => '+=' + (document.querySelector('.horizontal-scroll') as HTMLElement).scrollWidth
    }
  })
}, { scope: containerRef })
```

---

## REACT THREE FIBER v9 — Vollständiges Setup

### Canvas:
```tsx
// components/Scene.tsx
'use client'
import { Canvas } from '@react-three/fiber'
import { OrbitControls, Environment, PerspectiveCamera } from '@react-three/drei'
import { Suspense } from 'react'

export default function Scene() {
  return (
    <Canvas
      camera={{ position: [0, 0, 5], fov: 45 }}
      gl={{ antialias: true, alpha: true }}
      dpr={[1, 2]}
      style={{ width: '100%', height: '100vh' }}
    >
      <Suspense fallback={null}>
        <PerspectiveCamera makeDefault position={[0, 0, 5]} />
        <ambientLight intensity={0.3} />
        <directionalLight position={[10, 10, 5]} intensity={1.5} castShadow />
        <pointLight position={[-5, -5, -5]} color="#6c63ff" intensity={1} />
        <Environment preset="city" />
        <FloatingMesh />
        <OrbitControls enableZoom={false} enablePan={false} />
      </Suspense>
    </Canvas>
  )
}
```

### Floating Distort Mesh:
```tsx
'use client'
import { useRef } from 'react'
import { useFrame } from '@react-three/fiber'
import { MeshDistortMaterial } from '@react-three/drei'
import * as THREE from 'three'

export function FloatingMesh() {
  const meshRef = useRef<THREE.Mesh>(null)

  useFrame((state) => {
    if (!meshRef.current) return
    meshRef.current.position.y = Math.sin(state.clock.elapsedTime * 0.5) * 0.3
    meshRef.current.rotation.x = state.clock.elapsedTime * 0.1
    meshRef.current.rotation.y = state.clock.elapsedTime * 0.15
  })

  return (
    <mesh ref={meshRef}>
      <sphereGeometry args={[1.5, 64, 64]} />
      <MeshDistortMaterial color="#6c63ff" distort={0.4} speed={2} roughness={0.1} metalness={0.8} />
    </mesh>
  )
}
```

### Scroll-Linked 3D Rotation (GSAP + R3F):
```tsx
'use client'
import { useRef, useEffect } from 'react'
import { useFrame } from '@react-three/fiber'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import * as THREE from 'three'

gsap.registerPlugin(ScrollTrigger)

export function ScrollMesh() {
  const meshRef = useRef<THREE.Mesh>(null)
  const rotation = useRef({ y: 0, x: 0 })

  useEffect(() => {
    gsap.to(rotation.current, {
      y: Math.PI * 2, x: Math.PI * 0.5,
      scrollTrigger: {
        trigger: '#scroll-container',
        start: 'top top', end: 'bottom bottom', scrub: 1.5
      }
    })
    return () => ScrollTrigger.getAll().forEach(t => t.kill())
  }, [])

  useFrame(() => {
    if (meshRef.current) {
      meshRef.current.rotation.y = rotation.current.y
      meshRef.current.rotation.x = rotation.current.x
    }
  })

  return (
    <mesh ref={meshRef}>
      <torusKnotGeometry args={[1, 0.3, 128, 16]} />
      <meshStandardMaterial color="#ff6b6b" metalness={0.9} roughness={0.1} />
    </mesh>
  )
}
```

### Lights Cheatsheet:
```tsx
<ambientLight intensity={0.3} />                                         // Basis
<directionalLight position={[5, 5, 5]} intensity={2} castShadow />      // Hauptlicht
<pointLight position={[-5, -5, -5]} color="#6c63ff" intensity={1} />    // Akzentfarbe
<spotLight position={[0, 10, 0]} angle={0.3} penumbra={1} decay={2} />  // Dramatisch
<rectAreaLight width={3} height={3} intensity={5} position={[0, 5, 0]} /> // Softbox
```

### Materials Cheatsheet:
```tsx
<meshStandardMaterial metalness={0.8} roughness={0.2} />          // PBR Standard
<meshPhysicalMaterial clearcoat={1} clearcoatRoughness={0.1} />   // Hochglanz
<meshBasicMaterial color="#fff" wireframe />                       // Unlit
<MeshDistortMaterial distort={0.4} speed={2} />                   // Drei: Blob
<MeshWobbleMaterial factor={0.4} speed={1} />                     // Drei: Wackeln
```

### Instancing (1000 Partikel = 1 Draw Call):
```tsx
'use client'
import { useRef, useEffect } from 'react'
import { useFrame } from '@react-three/fiber'
import * as THREE from 'three'

export function ParticleField({ count = 1000 }) {
  const meshRef = useRef<THREE.InstancedMesh>(null)

  useEffect(() => {
    if (!meshRef.current) return
    const dummy = new THREE.Object3D()
    for (let i = 0; i < count; i++) {
      dummy.position.set(
        (Math.random() - 0.5) * 20,
        (Math.random() - 0.5) * 20,
        (Math.random() - 0.5) * 20
      )
      dummy.updateMatrix()
      meshRef.current.setMatrixAt(i, dummy.matrix)
    }
    meshRef.current.instanceMatrix.needsUpdate = true
  }, [count])

  useFrame((state) => {
    if (meshRef.current) meshRef.current.rotation.y = state.clock.elapsedTime * 0.02
  })

  return (
    <instancedMesh ref={meshRef} args={[undefined, undefined, count]}>
      <sphereGeometry args={[0.03, 8, 8]} />
      <meshBasicMaterial color="white" />
    </instancedMesh>
  )
}
```

### R3F Performance-Regeln:
```
✅ frameloop="demand" wenn keine kontinuierliche Animation (spart GPU)
✅ dpr={[1, 2]} begrenzt Pixel Ratio
✅ Suspense IMMER um schwere Scenes
✅ useMemo für Geometrien
✅ Instancing wenn > 20 gleiche Objekte
✅ useFrame nur wenn wirklich per-Frame Update nötig
❌ Nie margin/top animieren → nur transform + opacity
❌ Nie InstancedMesh ohne instanceMatrix.needsUpdate = true
```

---

## SPLINE — Next.js 15

```bash
npm install @splinetool/react-spline
```

### Methode 1: Next.js Import (empfohlen — auto SSR-safe):
```tsx
import Spline from '@splinetool/react-spline/next'

export default function HeroSection() {
  return <Spline scene="https://prod.spline.design/SCENE-ID/scene.splinecode" />
}
```

### Methode 2: Dynamic (Client-Only):
```tsx
'use client'
import dynamic from 'next/dynamic'

const Spline = dynamic(() => import('@splinetool/react-spline'), {
  ssr: false,
  loading: () => <div className="w-full h-screen bg-zinc-950 animate-pulse" />
})
```

### Spline per Scroll steuern:
```tsx
'use client'
import dynamic from 'next/dynamic'
import { useRef, useEffect } from 'react'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import { useGSAP } from '@gsap/react'
import type { Application } from '@splinetool/runtime'

const Spline = dynamic(() => import('@splinetool/react-spline'), { ssr: false })
gsap.registerPlugin(ScrollTrigger, useGSAP)

export default function SplineScrollScene() {
  const splineApp = useRef<Application | null>(null)

  useGSAP(() => {
    gsap.to({}, {
      scrollTrigger: {
        trigger: '#scroll-section',
        start: 'top top', end: 'bottom bottom', scrub: true,
        onUpdate: (self) => {
          if (!splineApp.current) return
          const obj = splineApp.current.findObjectByName('MeinObjekt')
          if (obj) obj.rotation.y = self.progress * Math.PI * 2
        }
      }
    })
  })

  return (
    <div id="scroll-section" style={{ height: '300vh' }}>
      <div style={{ position: 'sticky', top: 0, height: '100vh' }}>
        <Spline
          scene="https://prod.spline.design/SCENE-ID/scene.splinecode"
          onLoad={(spline) => { splineApp.current = spline }}
        />
      </div>
    </div>
  )
}
```

---

## FRAMER MOTION

### Magnetic Button:
```tsx
'use client'
import { useRef } from 'react'
import { motion, useSpring } from 'framer-motion'

export function MagneticButton({ children }: { children: React.ReactNode }) {
  const ref = useRef<HTMLButtonElement>(null)
  const x = useSpring(0, { stiffness: 150, damping: 15 })
  const y = useSpring(0, { stiffness: 150, damping: 15 })

  const onMove = (e: React.MouseEvent) => {
    const rect = ref.current?.getBoundingClientRect()
    if (!rect) return
    x.set((e.clientX - rect.left - rect.width / 2) * 0.4)
    y.set((e.clientY - rect.top - rect.height / 2) * 0.4)
  }

  return (
    <motion.button
      ref={ref} style={{ x, y }}
      onMouseMove={onMove}
      onMouseLeave={() => { x.set(0); y.set(0) }}
      whileHover={{ scale: 1.05 }}
      whileTap={{ scale: 0.95 }}
    >
      {children}
    </motion.button>
  )
}
```

### Infinite Marquee:
```tsx
'use client'
import { motion } from 'framer-motion'

export function Marquee({ items }: { items: string[] }) {
  return (
    <div style={{ overflow: 'hidden', display: 'flex' }}>
      {[0, 1].map((i) => (
        <motion.div
          key={i}
          animate={{ x: ['0%', '-100%'] }}
          transition={{ duration: 20, repeat: Infinity, ease: 'linear' }}
          style={{ display: 'flex', gap: '2rem', paddingRight: '2rem', flexShrink: 0 }}
        >
          {items.map((item, j) => <span key={j}>{item}</span>)}
        </motion.div>
      ))}
    </div>
  )
}
```

### Page Transition:
```tsx
'use client'
import { motion, AnimatePresence } from 'framer-motion'

export function PageTransition({ children }: { children: React.ReactNode }) {
  return (
    <AnimatePresence mode="wait">
      <motion.div
        initial={{ opacity: 0, y: 20 }}
        animate={{ opacity: 1, y: 0 }}
        exit={{ opacity: 0, y: -20 }}
        transition={{ duration: 0.4, ease: [0.22, 1, 0.36, 1] }}
      >
        {children}
      </motion.div>
    </AnimatePresence>
  )
}
```

---

## KOMPLETTE LANDING PAGE ARCHITEKTUR

```
layout.tsx
└── LenisProvider (root)
    ├── LenisGSAPSync (ticker sync — einmalig einbinden)
    └── page.tsx
        ├── HeroSection
        │   ├── HeroReveal (GSAP Timeline beim Load)
        │   ├── SplineScene ODER R3F Canvas (3D)
        │   └── MagneticButton (CTA)
        ├── FeatureSection
        │   ├── BentoGrid (shadcn-ui-skill)
        │   ├── ClipPathReveal (GSAP ScrollTrigger)
        │   └── ScrollMesh (R3F optional)
        ├── SocialProofSection
        │   └── Marquee (Framer Motion)
        └── CTASection
            └── HeroReveal (zweiter Reveal)
```

---

## WORKFLOW (bei jeder Anfrage)

1. **Vibe klären:** Dark brutal? Luxury minimal? Neon? Clean white?
2. **Tech entscheiden:**
   - Nur Scroll-Animationen → GSAP + Lenis (kein R3F nötig)
   - Fertiges 3D Objekt aus Spline → Spline Integration
   - Custom 3D / Partikel / Shader → R3F
   - Hover / Micro-Interactions → Framer Motion
3. **Immer zuerst:** `ui_ux_pro_max_agent` für Design-System (Farben, Fonts, Spacing)
4. **Dann:** `landingpage_agent` für Copy-Struktur
5. **Dann:** `shadcn-ui-skill` für Basis-Komponenten
6. **Zuletzt:** Diesen Skill für Animations-Layer
7. **Code liefern** — vollständig, keine Pseudocode-Platzhalter

---

## SYNERGIE MIT ANDEREN SKILLS

| Skill | Aufgabe |
|-------|---------|
| `ui_ux_pro_max_agent` | Design-System: Farben, Fonts, 8pt Grid, Stimmung |
| `shadcn-ui-skill` | Basis-Komponenten: Button, Card, Dialog, etc. |
| `landingpage_agent` | Copy-Struktur: Hero, Problem, Solution, Proof, CTA |
| **Dieser Skill** | Animations-Layer: Scroll, 3D, Hover, Transitions |

---

## ABSOLUTE DON'TS

- ❌ `@studio-freight/lenis` — deprecated, nutze `lenis`
- ❌ R3F v8 mit Next.js 15 — immer v9 (`@react-three/fiber@^9.5.0`)
- ❌ R3F v10 alpha in Production — auf Stable warten
- ❌ Spline ohne SSR-Schutz — immer `/next` Import oder `ssr: false`
- ❌ margin/top/width animieren — nur `transform` + `opacity` (GPU-Pfad)
- ❌ useFrame ohne echten Bedarf — teuer
- ❌ ScrollTrigger ohne `useGSAP` + `scope` — Memory Leaks
- ❌ Zu viele Animationen gleichzeitig — Erholungsphasen zwischen Events
- ❌ R3F ohne `transpilePackages` in next.config.js — Build-Fehler
- ❌ Gaussian Splatting für Conversion-LPs — 10-50MB+ killt Mobile-Performance
- ❌ `framer-motion` Imports — REBRAND, jetzt `motion/react`
- ❌ Theatre.js in Production — privates Repo seit Mitte 2024, eventuell sterbend

---

## 🆕 AI 3D ASSET-PIPELINE (2026 — Tripo, Meshy, Rodin)

Schluss mit Sketchfab-Asset-Hunting oder Blender-Modellierung von Hand. **AI 3D Generators** liefern jetzt produktionsreife Assets in Minuten — alle exportieren GLB/glTF direkt für R3F.

### Tools-Vergleich

| Tool | Stärke | Free Tier | URL |
|------|--------|-----------|-----|
| **Tripo** | Beste Quad-Topology für Animation, professionelle Retopologie | ja, mit Limits | tripo3d.ai |
| **Meshy** | Schnellste Iteration, Text-to-3D + Image-to-3D | ja, ~200 Credits/Monat | meshy.ai |
| **Rodin** | Photorealistisch, hochauflösende Texturen | ja, mit Limits | hyperhuman.deemos.com/rodin |

### Workflow für R3F-Integration

```bash
# 1. Asset aus AI-Tool generieren → GLB/glTF Export
# 2. Asset in /public/models/asset.glb ablegen
# 3. In R3F-Component laden:
```

```tsx
import { useGLTF } from '@react-three/drei'

export function GeneratedAsset() {
  const { scene } = useGLTF('/models/asset.glb')
  return <primitive object={scene} scale={1.5} />
}

useGLTF.preload('/models/asset.glb')
```

**Optimierungs-Tipp:**
- Vor Production-Use: `gltfjsx` Command-Line-Tool nutzen → konvertiert GLB zu typsicheren React-Komponenten
- Compression: `gltf-pipeline` oder `gltf-transform` für DRACO/Meshopt

```bash
npx gltfjsx public/models/asset.glb -o components/Asset.tsx
```

---

## 🆕 WebGPU + TSL (verfügbar, nicht-default)

WebGPU ist in current Three.js (r184) production-ready. Alle Major Browser unterstützen es jetzt (Chrome, Edge, Safari 26+, Firefox).

**Wann WebGPU nutzen:**
- Compute-Shader für komplexe Partikel-Systeme
- High-Density-3D-Szenen mit vielen Drawcalls
- Post-Processing-Pipelines

**Wann WebGL2 bleiben (Default für Conversion-LPs):**
- Single Hero-Asset
- Kompatibilität-kritisch (Mobile-Sicherheit)
- Lighthouse-Score-Optimierung

```tsx
// WebGPU mit automatischem WebGL2-Fallback
import { WebGPURenderer } from 'three/webgpu'
import { Canvas } from '@react-three/fiber'

<Canvas
  gl={(canvas) => {
    const renderer = new WebGPURenderer({ canvas, antialias: true })
    return renderer
  }}
>
  {/* Scene */}
</Canvas>
```

### TSL (Three Shading Language) — Node-Shader-Graph

TSL ist Three.js's neuer renderer-agnostischer Shader-Graph (kompiliert zu WGSL und GLSL). Ersetzt manuelle GLSL-Shader für die meisten Cases.

```tsx
import { Fn, vec3, sin, time } from 'three/tsl'

const pulsate = Fn(() => {
  return vec3(0.5).add(sin(time).mul(0.5))
})
```

**Wann TSL nutzen:** Custom Materials, Vertex-Animations, Effekte die mit normalen Three-Materialien nicht gehen.

---

## 🆕 CROSS-REFERENCE: Rive für interaktive Mikro-Animationen

**Rive ist KEIN 3D, aber relevante Alternative** zu schweren R3F-Setups für CTAs, Mascots, Trust-Badges.

| | Rive | Lottie | R3F |
|---|------|--------|-----|
| Filesize | 15-50KB | 100-500KB (JSON) / 30-200KB (dotLottie) | 100KB+ + Modell |
| State Machines | ✅ | ✅ (seit Ende 2025) | manuell |
| Mobile FPS | ~60 | ~40-50 (mit dotLottie + ThorVG) | abhängig |
| Use-Case | Interaktive UI-Mikro | Marketing-Animation aus AE | Echtes 3D |

→ Bei reinen 2D-State-Machines → Rive in `scroll_animation_agent` nutzen statt R3F. Siehe dortige Sektion „Interaktive Mikro-Animationen: Rive vs Lottie 2026".

---

## OPTIONALE MCP-SERVER (2026)

### Für 3D-Code-Generation:
- **`bruzethegreat/gsap-master-mcp-server`** — Comprehensive GSAP MCP (deckt auch GSAP-3D-Effects ab)

Install (user-weit):
```bash
cd ~/.claude/plugins/marketplaces
git clone https://github.com/bruzethegreat/gsap-master-mcp-server.git
```

### Für Spline-Workflow:
- Spline-MCP gibt es Stand Mai 2026 noch nicht offiziell — manueller Workflow bleibt Standard

---

## CROSS-REFERENCES

- **Scroll-Animationen 2D**: `scroll_animation_agent/SKILL.md`
- **Design Tokens**: `design_tokens/design.md` (Animation Timing Curves)
- **Visual Directions**: `design_tokens/VISUAL-DIRECTIONS.md` (Direction 6 KINETIC/LIQUID nutzt diesen Skill optional)
- **UI/UX**: `ui_ux_pro_max/SKILL.md` (A11y-Checks für 3D-Sections)
