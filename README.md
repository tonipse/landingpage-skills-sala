# Landing Page Skills — Design System (von Sala)

Komplettes Design-/Build-Skill-Paket für Claude Code — alles was du brauchst um hochwertige Landing Pages zu bauen. Aus dem Agency-X-System extrahiert (ohne Kundendaten/Copy-IP).

## Installation

```bash
git clone https://github.com/tonipse/landingpage-skills-sala.git
# Skills nach Claude Code ziehen — entweder user-weit oder pro Projekt:
cp -r landingpage-skills-sala/skills/* ~/.claude/skills/
# ODER pro Projekt:
cp -r landingpage-skills-sala/skills/* dein-projekt/.claude/skills/
```

## Die Skills

### 🎨 Design-Foundation
| Skill | Was |
|-------|-----|
| `design_tokens/` | **Das Herzstück.** 120 echte Brand-DESIGN.md Refs (Apple, Stripe, Linear, Kinfolk, Monocle, ...) + USE-CASE-INDEX (Pattern-Routing pro Section-Typ) + VISUAL-DIRECTIONS (7 kuratierte Stile) + design.md (Tokens, Farbpaletten, Font-Pairs, Kinetic-Gradients, AI-Slop-Blacklist) + Hallmark-Refs (65 Anti-Slop-Gates) |
| `anthropic_frontend_design/` | Layer-0 Direction-Selection (Marker fürs offizielle Anthropic-Plugin) |

### 🏗️ Build-Engines
| Skill | Was |
|-------|-----|
| `huashu_design/` | Hi-Fi HTML Design (Claude-Design-Clone). Hauptbasis für LP-Builds |
| `landingpage_agent/` | LP-Struktur + LP Architecture Bible (Section-Taxonomie, Conversion-Flow) |
| `ui_ux_pro_max/` | 161 Paletten, 57 Font-Pairs, 99 UX-Regeln |
| `shadcn_agent/` | shadcn/ui Komponenten (Tailwind v4 + OKLCH + sonner) |

### ✨ Animation
| Skill | Was |
|-------|-----|
| `scroll_animation_agent/` | GSAP (free) + Lenis + Motion + CSS Native Scroll-Driven + View Transitions. Mobile-safe |
| `web_animation_3d_agent/` | R3F + Three.js + Spline + AI-3D-Pipeline. Nur bei explizitem 3D-Bedarf |
| `design_motion_principles/` | Motion-Audit (prüft Animationen auf AI-Slop) |

### ✅ Qualität & Recht
| Skill | Was |
|-------|-----|
| `cro_audit/` | Conversion-Check vor Launch (7 Dimensionen + A/B-Test-Ideen) |
| `dsgvo_consent/` | **DE-Pflicht:** Cookie-Consent + Google Consent Mode v2 für rechtssichere LPs |
| `_universal/` | Discovery-Form (Pre-Build) + Section-Build-Workflow (Checklisten) |

## Empfohlener Build-Flow

```
1. Discovery (_universal/DISCOVERY-FORM.md) — was, für wen, welches Ziel?
2. Direction wählen (anthropic_frontend_design + VISUAL-DIRECTIONS)
3. Brand-Refs scannen (design_tokens/design-md/_INDEX.md → 2-3 passende)
4. Bauen (huashu_design + landingpage_agent + ui_ux_pro_max + shadcn)
5. Animieren (scroll_animation_agent)
6. Auditieren (cro_audit + design_motion_principles + Hallmark slop-test)
7. Rechtssicher machen (dsgvo_consent)
```

## Tech-Stack (Standard)
Next.js 15 · Tailwind v4 · shadcn/ui · GSAP + Motion + Lenis · TypeScript · Mobile-First

## Lizenzen
Skills mit externen Quellen behalten ihre Original-Lizenz (huashu MIT, Hallmark-Refs MIT, CRO aus marketingskills MIT, design_motion_principles MIT). Brand-Refs aus VoltAgent/awesome-design-md (Apache 2.0) + oh-my-design (MIT) + rohitg00 (MIT).

---
Stand: 2026-05-30 · Paket von Sala für Toni
