---
name: SECTION-BUILD-WORKFLOW
description: Verbindliche Checklisten für jeden Section-Build, Section-Polish und Page-Final-Audit. Garantiert Design-System-Nutzung statt Halluzination.
type: workflow-checklist
version: 1.0
created: 2026-05-15
---

# SECTION-BUILD-WORKFLOW

> **Zweck:** Niemals improvisieren. Immer auf System bauen. Jede Section folgt einer dieser drei Checklisten.
>
> **Verbindlich für:** Jeden visuellen Build (LP, VSL-Slides, Decks, Email-Templates, Creatives mit HTML).
>
> **Im Chat sichtbar machen:** Schritte 1-3 explizit ankündigen ("Lese System-Files: X, Y, Z"). Keine stille Annahme.

---

## 🏗️ CHECKLIST A — SECTION-BUILD (initial, neue Section)

**Zweck:** Eine neue Section bauen mit System statt aus Erinnerung.

### Vor dem ersten Pixel

1. **Kundendaten lesen** (CLAUDE.md REGEL 1)
   - `Agency/[Kunde]/Sources/Marketing-Thesis.md` ✅
   - `Agency/[Kunde]/Sources/Kunden-Avatar.md` ✅
   - Falls vorhanden: `Kundenstimmen-Raw.md` / Transkripte ✅
   - `Agency/Playbook.md` (Funnel-Logik) ✅

2. **Use-Case identifizieren** (Hero / Belief / Process / Testimonial / FAQ / CTA / Stats / Footer / Divider)

3. **USE-CASE-INDEX abfragen** (`Brain/skills/design_tokens/USE-CASE-INDEX.md`)
   - Welche Patterns aus `design.md`?
   - Welche 2-3 Brand-Refs aus `design-md/`?
   - Welche A11y-Critical-Punkte?
   - → **Im Chat zeigen:** "Für diese Section nutze ich Pattern X (Zeile Y), Brand-Ref Z."

4. **Design-DNA der Page checken**
   - Editorial Premium? → Easing `cubic-bezier(0.22, 1, 0.36, 1)`, KEINE Bounce
   - SaaS Snappy? → Easing `cubic-bezier(0.4, 0, 0.2, 1)`, 0.2-0.3s
   - Luxury Dark? → Ambient Glow + Gradient Recipes
   - → DNA bleibt konsistent durch ALLE Sections der Page

5. **Avatar-Match prüfen**
   - Sprache: Du/Sie? Du-Form fast immer (außer hochpreis-luxus)
   - Tonalität: Direkt/sanft/konfrontativ? Aus Avatar ableiten
   - Pain-Points: 1-2 Top-Pains pro Section vorkommen lassen

### Während des Builds

6. **Mobile-First HTML-Order**
   - Text vor Bild im HTML (außer explizit anders gewollt)
   - Kein `order: -1` auf Image-Container (Mobile-Lesefluss)
   - Container `max-width` setzen, nicht fixed width

7. **CSS-Patterns aus `design.md` kopieren, nicht aus Erinnerung schreiben**
   - Animation-Curves: aus L457-491 ziehen
   - Spacing: aus L312-338 ziehen (`--space-1` bis `--space-12`)
   - Shadows: aus L339-366 ziehen (5 Levels)
   - Border-Radius: aus L367-380 (Token-Scale)

8. **AI-Slop Blacklist live-check** (`design.md` L17-28)
   - Keine `margin/top/width` Animationen → nur `transform` + `opacity`
   - Kein `background-attachment: fixed` (iOS broken)
   - Keine Emojis als Icons → lucide oder SVG
   - Keine Bouncy-Eases auf Editorial-Brands
   - Keine Drop-Shadows auf Cream/Light Backgrounds (nicht sichtbar)
   - Keine Gedankenstriche (—) als Stilmittel im Copy

9. **A11y CRITICAL (Priorität 1-2 aus `ui_ux_pro_max`)**
   - Touch-Target ≥44px (Buttons, Links, FAQ-Header)
   - Contrast ≥4.5:1 für Body-Text, ≥3:1 für Large-Display
   - `:focus-visible` Styling sichtbar
   - Semantic HTML (`<button>` statt `<div onclick>`, `<details><summary>` für FAQ)
   - Alt-Text auf allen `<img>` (descriptive, nicht "image")

10. **`prefers-reduced-motion` einbauen**
    - CSS-Block: `@media (prefers-reduced-motion: reduce) { animation: none !important; }`
    - GSAP-Check am Anfang: `if (matchMedia('(prefers-reduced-motion: reduce)').matches) { gsap.set(...endstate...); return; }`
    - → Endzustand zeigen, nicht ausblenden

### Nach dem Build

11. **Self-Review** (sichtbar im Chat ankündigen)
    - Gegen Avatar prüfen: Klingt der Text nach dieser Zielgruppe?
    - Gegen Marketing-Thesis prüfen: Kommuniziert die Section die Kernbotschaft?
    - Konkrete Zahlen statt vage Versprechen?
    - Du-Form durchgängig?

12. **Mobile-Check (3 Breakpoints minimum)**
    - 375px (iPhone SE)
    - 768px (Tablet)
    - 1024px (Desktop-Small)

---

## 🔍 CHECKLIST B — SECTION-POLISH (Tiefenanalyse / Optimieren)

**Trigger:** User sagt "Tiefenanalyse", "optimieren", "perfektionieren", "Section X nochmal".

**Zweck:** Bestehende Section auf nächstes Level — auf System-Basis, nicht aus Erinnerung.

### Vor dem ersten Edit

1. **System-Files frisch lesen (NICHT aus Erinnerung)**
   - `design_tokens/design.md` (relevante Sections nach Use-Case)
   - `design_tokens/USE-CASE-INDEX.md` (Use-Case-Mapping)
   - `ui_ux_pro_max/SKILL.md` (Prioritäten 1-2)
   - `huashu_design/SKILL.md` (Anti-AI-Slop Clearlist)
   - → **Im Chat zeigen:** "Lese System-Files: [...] für [Section-Typ]"

2. **Aktuellen Stand der Section dokumentieren**
   - Was hat sie schon? (Animations, CSS-Patterns, Copy)
   - Was funktioniert? Was nicht?
   - Was sagt der Avatar? Stimmt Copy zu Zielgruppe?

3. **Backup anlegen**
   - `cp file.html file.html.backup-before-[section-name]-polish`
   - Sichtbar im Chat erwähnen → Rollback jederzeit möglich

### Tiefenanalyse — die 8 Prüfsteine

4. **Visual Hierarchy**
   - Ist klar was zuerst gelesen wird? (Headline → Sub → CTA → Trust)
   - Größenkontrast: H2 mind. 2.5x Body-Größe?
   - Whitespace: lieber mehr als zu wenig

5. **Animation-Audit**
   - `transform` + `opacity` only? (siehe AI-Slop Blacklist)
   - Editorial-Easing oder SaaS-Easing — konsistent zum Page-Vibe?
   - Reveal-Sequenz max 3 staggered Elements (sonst Cognitive Load)
   - Hover-States definiert? Click-Feedback?

6. **Interaktion-Tiefe**
   - Hover-Effekte vorhanden auf Desktop? Editorial: subtle (rotate ±5°, lift 4-6px)
   - Click-Feedback auf Touch-Devices? (Stempel-Press, Scale-Bounce)
   - `cursor: pointer` auf allen klickbaren Elements?

7. **Copy-Punch**
   - Konkrete Zahlen statt vager Versprechen ("15-30k €" statt "Tausende")
   - Du-Form durchgängig
   - `<strong>` semantisch für die WICHTIGEN Wörter (nicht dekorativ)
   - Closing-Frage vor CTA: konfrontativ statt höflich

8. **Brand-Recall**
   - Brand-Element wiederkehrend? (Logo-Akzent, Color, Font)
   - Zu viel? → Max 3 Touchpoints pro Page für Brand-Akzent
   - Zu wenig? → Mindestens 1 Brand-Akzent pro Hero + 1 pro Closing

9. **A11y-Re-Check (Priorität 1-2)**
   - Touch-Target ≥44px alle interaktiven Elemente
   - Contrast ≥4.5:1 (mit Chrome DevTools / Stark-Plugin checken)
   - Keyboard-Navigation funktioniert (Tab + Enter)
   - Screen-Reader: macht semantische HTML-Struktur Sinn?

10. **Mobile-Spezifika**
    - Touch-Hover entfällt → Click-Pattern für Mobile-Mirror?
    - Stacking-Order der Sub-Elements: Text vor Image
    - Spacing reduziert (40px → 24px Section-Padding)

11. **`prefers-reduced-motion` — Endzustand korrekt?**
    - Bei reduced-motion: zeigt es den korrekten End-State (nicht ausgeblendet)?
    - Alle Klassen die normalerweise via Animation gesetzt werden: direkt setzen

### Nach den Edits

12. **Vercel-Deploy + Manual-Check**
    - Hard-Refresh-Hinweis im Chat (`Cmd+Shift+R`)
    - User Daumen-rauf abwarten
    - Bei Daumen-runter: Backup restore ist 1-Befehl

---

## 🎯 CHECKLIST C — PAGE-FINAL (vor öffentlichem Launch)

**Trigger:** Page ist visuell + copy-mäßig fertig. Vor finalem Deploy/Push.

**Zweck:** Alles muss konsistent, accessible, performant sein. Keine Überraschungen für User.

### Konsistenz-Check

1. **Design-DNA Page-übergreifend konsistent**
   - Easing-Curves: gleich in allen Sections?
   - Spacing: System-Tokens durchgängig?
   - Colors: nur Custom-Properties, keine raw Hex?
   - Font-Pairs: max 2 Schriften (sonst inkonsistent)

2. **Headline-Rhythmus**
   - Keine zwei aufeinanderfolgenden H2 mit gleichem Pattern ("Drei X" → "Drei Y")
   - Variation in Phrasing-Patterns
   - Italic-Akzente nicht in jeder H2 (sonst entwertet)

3. **CTA-Konsistenz**
   - Alle "Durchblick-Call" / Primary-CTAs gleiche Beschriftung?
   - Gleiches Button-System (Gold = Primary, Teal = Secondary)?
   - Brand-Akzente (z.B. Logo-Stern) konsistent platziert?

### Performance-Check

4. **Image-Optimization**
   - WebP + JPG-Fallback via `<picture>` für alle größeren Bilder
   - `loading="lazy"` für Below-the-Fold Images
   - `loading="eager"` für Hero-Image
   - Explizite `width`/`height` Attribute (verhindert Layout-Shift)

5. **Font-Loading**
   - Google Fonts mit `&display=swap`
   - Preconnect für `fonts.googleapis.com` + `fonts.gstatic.com`
   - Max 2 Schriften, max 4 Weights

6. **CSS/JS-Bundle-Size**
   - Inline-CSS für Above-the-Fold (kein FOUC)
   - GSAP nur die genutzten Plugins (ScrollTrigger separat geladen)

### A11y-Final-Check (alle Priorität 1-2 aus `ui_ux_pro_max`)

7. **Keyboard-Navigation**
   - Tab geht durch alle interaktiven Elemente in logischer Reihenfolge?
   - Skip-to-Content Link am Page-Start?
   - Mobile-Menu mit Esc-Key schließbar?

8. **Screen-Reader-Test (semantic HTML)**
   - `<button>` statt `<div onclick>`
   - `<nav>` für Navigation, `<main>` für Content, `<footer>` für Footer
   - `<details><summary>` für FAQ (native + accessible)
   - `<figure><figcaption>` für Bilder mit Caption

9. **Color-Contrast (alle Text-Elemente)**
   - Body-Text: ≥4.5:1
   - Large-Display (H1, H2): ≥3:1
   - Tools: Chrome DevTools, axe DevTools, Stark Plugin

### Cross-Device-Test

10. **Breakpoints prüfen**
    - 320px (Mini-Mobile)
    - 375px (iPhone SE)
    - 768px (Tablet Portrait)
    - 1024px (Tablet Landscape / Small Desktop)
    - 1440px (Desktop)
    - 1920px (Large Desktop)

11. **Browser-Test**
    - Safari (iOS + macOS) — Edge cases mit `-webkit-` prefixes
    - Chrome (Android + Desktop) — Standard
    - Firefox — Edge cases mit Flexbox/Grid

12. **Animation Cross-Device**
    - Smooth auf 60fps? (Chrome DevTools Performance-Tab)
    - Mobile: keine Janks beim Scroll?
    - `prefers-reduced-motion` final-test (DevTools → Rendering → Emulate)

### Copy-Final-Check

13. **Humanizer-Pass**
    - Keine "—" Gedankenstriche als Stilmittel
    - Keine AI-Tells ("It's important to note...", "Let me explain...")
    - Tonalität konsistent mit Avatar
    - Konkrete Zahlen, keine vagen Phrasen

14. **Self-Review gegen Marketing-Thesis**
    - Page kommuniziert die Kernbotschaft klar?
    - Funnel-Logik durchgängig (Awareness → Interest → Decision → Action)?
    - Avatar fühlt sich verstanden?

### Deploy

15. **Backup vor Push**
    - Live-Version ist im Git getracked
    - `git tag` setzen falls große Page-Version (z.B. `v1.0-launch`)

16. **Deploy-Check**
    - Live-URL antwortet HTTP 200
    - Bilder laden (curl Logo + Hero)
    - Critical CSS lädt
    - Console-Errors checken (Chrome DevTools)

---

## 🚨 RED-FLAG-Sofort-Stop

**WENN du eines dieser Symptome bei dir bemerkst — STOP und re-route durch System-Files:**

- 🚩 Du baust ein Pattern aus der Erinnerung statt aus `design.md` zu lesen
- 🚩 Du wählst eine Animation-Curve ohne zu wissen ob sie der Page-DNA entspricht
- 🚩 Du schreibst Copy ohne Avatar/Thesis frisch gelesen zu haben
- 🚩 Du editierst ohne Backup
- 🚩 Du pushst ohne explizites User-"Go"
- 🚩 Du machst eine Section "perfekt" ohne System-Files zu konsultieren

→ **Sofort:** Files lesen, Plan zeigen, neu starten.

---

## Lessons-Lock-In (nach JEDER Section)

Am Ende eines Section-Builds / Polish-Cycles → 1 Eintrag in passende `LESSONS.md`:

**Template:**
```markdown
## [Datum] — [Kunde] [Section-Name]
- **Verwendet aus System:** [Pattern-Liste mit Zeilennummern]
- **Was funktionierte:** [konkrete Wins]
- **Was fehlte:** [Pattern-Gaps die wir hatten]
- **Neue Patterns dazu:** [falls etwas erfunden wurde → in design.md ergänzen]
```

→ System wächst **organisch durch echte Arbeit**, nicht durch akademische Theorie.

---

## Cross-References

- **System-Files:** `Brain/skills/design_tokens/design.md` + `USE-CASE-INDEX.md` + `design-md/`
- **UI/UX Rules:** `Brain/skills/ui_ux_pro_max/SKILL.md`
- **Design-Philosophy:** `Brain/skills/huashu_design/SKILL.md`
- **Onboarding:** `Brain/skills/_universal/ONBOARDING.md`
- **CLAUDE.md REGEL 1.5:** Pflichtlektüre vor visuellem Build (mit dieser Workflow-Datei jetzt verschärft)
