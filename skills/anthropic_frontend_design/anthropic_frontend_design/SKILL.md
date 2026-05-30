---
name: anthropic_frontend_design
description: Marker für das offizielle Anthropic frontend-design Plugin (760k Installs, Mai 2026). Triggert AUTOMATISCH bei UI-/Frontend-Build-Requests und zwingt zu BOLDER, distinctiver Aesthetic-Direction vor Code. Operiert als Layer 0 (Direction-Selection / Anti-AI-Slop) — KOMPLEMENTÄR zu huashu_design (Layer 1, Implementation). Verbietet generische Fonts (Inter/Roboto/Arial), purple Gradients auf weiß, predictable layouts. Erzwingt asymmetrische Kompositionen, unexpected font pairings, scroll-triggered Motion. Trigger: build web components, build a page, build an application, design ui, frontend interface.
---

# Anthropic Frontend Design — Layer 0

**Identität:** Offizielles Anthropic Plugin für distinctive Frontend-Builds.
**Quelle:** [anthropics/claude-code (Plugin `frontend-design`)](https://github.com/anthropics/claude-code/tree/main/plugins/frontend-design)
**Stand:** 760.428 Installs (Mai 2026, war März 277k → +180% in 2 Monaten — Plugin-Marketplace #1 Design-Skill).

---

## Layer-Architektur in unserem System

Anthropic frontend-design ist **NICHT redundant** zu unserem `huashu_design` oder `landingpage_agent`. Sie operieren auf **verschiedenen Ebenen**:

```
┌────────────────────────────────────────────────────────────┐
│ LAYER 0 — Direction-Selection (Anthropic frontend-design)  │
│ „WELCHE Aesthetic wählen wir? Avoid AI-Slop."              │
│ → Bold maximalism / refined minimalism / brutalist / etc.   │
└────────────────────────────────────────────────────────────┘
                            ↓
┌────────────────────────────────────────────────────────────┐
│ LAYER 1 — Implementation (huashu_design / landingpage_agent)│
│ „WIE bauen wir es konkret?" Token-Application + HTML-Render │
│ → exakte Hex, Spacing, Easing, Brand-Refs, Asset-Protokoll  │
└────────────────────────────────────────────────────────────┘
                            ↓
┌────────────────────────────────────────────────────────────┐
│ LAYER 2 — Polish (scroll_animation, ui_ux_pro_max, humanizer)│
│ Animation, A11y, Copy-Refinement                            │
└────────────────────────────────────────────────────────────┘
```

---

## Was Anthropic frontend-design erzwingt

**Pflicht-Verhalten vor Code:**
- Commitment auf BOLDE Aesthetic-Direction (brutalist / maximalist / retro-futuristic / editorial / luxury / playful / industrial / etc.)
- Distinctive font choices statt Inter/Roboto/Arial/Space Grotesk
- Dominante Farben mit scharfen Akzenten (nicht timid-evenly-distributed Paletten)
- Asymmetrische Komposition, Grid-Breaking, generous negative space ODER controlled density
- Scroll-triggered Motion, hover surprises, ein orchestrierter Page-Load statt verstreute Micro-Interactions
- Background-Atmosphäre statt solid colors (Gradient-Mesh, Noise, Layered Transparenzen, Grain)

**Hard Bans:**
- Inter, Roboto, Arial, system fonts
- Purple gradients auf white background
- Predictable layouts / cookie-cutter components
- Space Grotesk als Default-Convergence

---

## Wo das Plugin installiert ist

```
Quelle:       ~/.claude/plugins/marketplaces/anthropic-claude-code/plugins/frontend-design/
User-weit:    ~/.claude/skills/frontend-design/    (Symlink)
```

→ Aktiv in **beiden Workspaces** (AI Copywriting System + Unlimited Vibe Coding).

---

## Trigger-Muster

| Saladin sagt | Was triggert |
|--------------|--------------|
| „Bau mir eine LP für Kunde X" | **Layer 0** (Direction) → **Layer 1** huashu_design (Build) → **Layer 2** Polish |
| „Mach mir ein Hi-Fi Mockup" | Layer 0 → huashu_design |
| „Design einen Hero" | Layer 0 erst — danach Implementation |
| „Schreib mir die Tokens" | Direkt Layer 1 (Layer 0 skip, Direction klar) |

---

## Konflikt-Management

**Risiko ohne Klärung:** Beide Skills aktivieren auto bei UI-Requests → konkurrierende System-Prompts möglich.

**Unsere Klärung:**
1. Anthropic frontend-design läuft **zuerst** (Direction wählen / AI-Slop vermeiden)
2. `huashu_design` setzt **darauf auf** (Token-Application für die gewählte Direction)
3. Wenn die Direction explizit aus `VISUAL-DIRECTIONS.md` kommt → Layer 0 wird **skipped** (Direction ist schon gesetzt)

---

## Wann Anthropic frontend-design **skippen**

- ✅ Direction ist schon klar (z.B. bestehender Kunde mit DESIGN.md)
- ✅ Reine Code-Edits (Color-Tweak, Padding-Fix) → kein Direction-Check nötig
- ✅ Asset-Operationen, Datei-Renames → irrelevant

---

## Updates

```bash
cd ~/.claude/plugins/marketplaces/anthropic-claude-code && git pull
```

Symlink zieht automatisch nach.

---

## Verwandte Skills

- **[[huashu_design]]** — Layer 1 Implementation (Hi-Fi HTML, Asset-Protokoll)
- **[[landingpage_agent]]** — Layer 1 Implementation (LP-spezifisch)
- **[[VISUAL-DIRECTIONS]]** — eigene 7 kuratierte Directions (überlappt mit Layer 0 Direction-Selection)
- **[[ui_ux_pro_max]]** — Layer 2 (A11y, Touch-Targets)

---

## Notiz für Wolf

Anthropic frontend-design ist ein **separat installierbares Plugin** (kein Teil des Brain-Repos). Wenn Wolf das auch nutzen will, kann er es bei sich aktivieren:

```bash
cd ~/.claude/plugins/marketplaces
git clone https://github.com/anthropics/claude-code.git anthropic-claude-code
ln -sf ~/.claude/plugins/marketplaces/anthropic-claude-code/plugins/frontend-design/skills/frontend-design ~/.claude/skills/frontend-design
```

Dann ist es bei ihm auch user-weit aktiv.
