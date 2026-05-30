# Hallmark Reference Library (NICHT aktiver Skill)

**Quelle:** github.com/Nutlope/hallmark (Apache 2.0 / MIT)
**Stand:** 2026-05-21 (cherry-picked aus Hallmark v1.0)

---

## ⚠️ WICHTIG — Das ist KEIN aktiver Skill

Diese Files sind **Reference-Material** für selektives Nachschlagen — **NICHT als Claude-Skill aktiviert**, weil sie sonst mit `anthropic_frontend_design`, `huashu_design`, `landingpage_agent` und `ui_ux_pro_max` kollidieren würden.

Hallmark's eigene Description triggert auf „build a new app or landing page" → würde unseren Stack überschreiben.

---

## Was hier wirklich Gold ist (TOP-3 Files)

### 1. `slop-test.md` (30k Bytes, 65 Gates)
**65 Anti-AI-Slop Pre-Ship Gates** in 11 Kategorien:
- Gates 1–8: Visual (Inter/Roboto-Detect, Purple-Blue-Gradients, 3-col-card-grids)
- Gates 9–10: Structural (Hero→3-Features→CTA-Template-Reject)
- Gates 11–20: Microinteractions (`transition: all` ban, `hover:scale-105` ban) — **GOLD**
- Gates 21–23: Variety (Macrostructure-Stamp-Pflicht)
- Gates 24–29: Implementation (OKLCH-zero-chroma ban, accent ≤5% Viewport)
- Gates 30–35: Hero-Enrichment + Diversification
- Gates 36–38: Layout-Safety (320–1920px overflow-x clip)
- Gates 39–40: Typography 2+1-Rule (max 3 Familien)
- Gates 41–45: Input-States — **GOLD**
- Gates 46–50: Contrast (APCA Lc ≥60)
- Gates 51–65: Mobile-Responsiveness

**Use-Case:** Vor jedem LP-Launch manuell durchgehen.

### 2. `anti-patterns.md` (25k Bytes)
Kategorien:
- "Invented metrics"
- "Mid-render token improvisation"
- "Re-drawn UI chrome"
- "Centered hero with min-height 100vh"

**Use-Case:** Cross-Check für Wolf-Premium-Builds.

### 3. `macrostructures/` (21 Layout-Patterns)
Naming-Vokabular für LP-Layouts:
Bento-Grid · Long-Document · Marquee-Hero · Stat-Led · Workbench · Conversational-FAQ · Manifesto · Photographic · Quote-Led · Specimen · Catalogue · Letter · Index-First · Narrative-Workflow · Split-Studio · Feature-Stack · Type-Specimen · Portfolio-Grid · Map-Diagram · Ecosystem-Index · Component-Playground

**Use-Case:** Bessere Briefs schreiben („baue mir eine Marquee-Hero mit Workbench-Body").

---

## Weitere wertvolle Files (selektiv lesen)

- `interaction-and-states.md` — Button/Form/Input-States-Disziplin
- `hero-enrichment.md` — wie Hero-Sections über das Generic hinausgehen
- `microinteractions.md` — Mikro-Animation Anti-Patterns
- `motion.md` — Motion-Discipline (cross-check zu `scroll_animation_agent`)
- `typography.md` — Typo-System
- `color.md` — Farbsystem
- `study.md` — Pipeline für Design-DNA-Extraktion aus URLs

---

## Was NICHT genutzt werden sollte

- `HALLMARK-SKILL-REFERENCE.md` — die original SKILL.md (63k Bytes, Monster). Nur als Read-Reference, NICHT als aktiver Skill installieren.
- `verbs/` — Hallmark's `audit` und `redesign` Commands (würden mit unserem System konfligieren)
- `design-md.md` — Hallmark's design.md-Convention (anders als unsere)

---

## Wie diese Library nutzen

1. **Pre-Launch jedes LP-Builds:** `slop-test.md` manuell durchgehen (15 Min Sanity-Check)
2. **Bei Brand-Briefings:** `macrostructures/` als Vokabular nutzen
3. **Beim Refactoring bestehender LPs:** `anti-patterns.md` als Cross-Check
4. **Wenn ein neuer Brand auditiert werden soll:** `study.md` Pipeline manuell ausführen, Output in `design-md/[brand]/DESIGN.md` einbauen

---

## Beziehung zu anderen Skills

| Frage | Antwort |
|-------|---------|
| Ersetzt es huashu_design? | Nein — huashu bleibt Layer 1 Implementation |
| Ersetzt es anthropic_frontend_design? | Nein — Anthropic bleibt Layer 0 (Direction-Selection) |
| Ergänzt es etwas? | Ja — die 65 Slop-Gates sind detaillierter als alles was wir aktuell haben |

---

**Lizenz:** Siehe `LICENSE` (MIT/Apache 2.0 Mix von Nutlope/Together AI).
