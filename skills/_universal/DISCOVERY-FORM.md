---
name: DISCOVERY-FORM
description: Strukturierter Fragebogen VOR jedem visuellen Build. Verhindert ~80% Revisionen indem alle 5 Pflicht-Dimensionen vorab abgeklärt werden. Inspiriert von nexu-io/open-design's Interactive Discovery Form.
type: pre-build-form
version: 1.0
created: 2026-05-15
trigger: Vor jedem neuen Brand-Build, neuen Page-Build, neuem Funnel-Konzept
---

# DISCOVERY-FORM — Strukturierter Vor-Build-Fragebogen

> **Zweck:** Statt sich durch unstrukturierte Fragen zu hangeln → systematisch alle 5 kritischen Dimensionen abklären. Verhindert 80% der späteren Revisionen.
>
> **Verbindlich für:** Neue Brand-Builds, neue Landing-Pages, neue Funnel-Konzepte, neue Email-Sequenzen, neue Decks.
>
> **Skippbar für:** Kleine Edits, Datei-Operationen, Direkt-Follow-ups innerhalb desselben Tasks.

---

## Wie nutzen

1. **Vor dem ersten Build-Schritt** → Form mit User durchgehen
2. **Alle 5 Sektionen abdecken** — nicht überspringen weil "klar ist"
3. **Antworten dokumentieren** in `Agency/[Kunde]/Sources/Discovery.md` (falls neuer Kunde) ODER in `Sources/[Funnel-Name]-Discovery.md` (für funnel-spezifisch)
4. **Erst nach kompletter Form → Plan zeigen → Go abwarten**

---

## DIMENSION 1: SURFACE (Was wird gebaut?)

### Pflicht-Fragen
- **Format?** Landing Page · VSL · E-Mail-Sequenz · Slide-Deck · Ad-Creative · Other
- **Single oder Multi-Page?** Falls Multi → wie viele Pages, welche Reihenfolge?
- **Tech-Stack-Constraints?** Coolify · Vercel · Framer · Webflow · WordPress · Static HTML?
- **Subpath oder Root-Domain?** (Falls Subpath → `<base href>` einplanen)
- **Bestehende Page die wir ersetzen oder neu?**

### Sekundär-Fragen (wenn relevant)
- Deadline / Launch-Datum?
- Mobile-First oder Desktop-First?
- Performance-Critical? (z.B. Ads-Landing mit Load <2s?)
- Multi-Sprache nötig?

---

## DIMENSION 2: AUDIENCE (Für wen wird gebaut?)

### Pflicht-Fragen
- **Primär-Avatar:** Existiert `Kunden-Avatar.md`? Wenn nein → STOP, erst Avatar erstellen
- **Konkrete Persona:** Alter, Beruf, Lebenssituation, Schmerzen, Wünsche
- **Sprach-Form:** Du/Sie? Tonalität (warm/direkt/business/casual)?
- **Awareness-Level:** Cold Traffic · Warm Lead · Hot Buyer? (verschiedene Copy-Strategien)
- **Bestehende Kundenstimmen vorhanden?** → Quotes verwenden statt frei erfinden

### Sekundär
- Demografische Daten (Region, Bildungsstand)?
- Psychografische Trigger (Werte, Ängste, Aspirationen)?
- Wettbewerbs-Konsum (was sehen sie sonst noch)?

---

## DIMENSION 3: TONE (Wie soll es sich anfühlen?)

### Pflicht-Fragen
- **Brand-Tonalität:** Editorial · SaaS · Luxury · Casual · Authoritative · Healing/Therapeutic?
- **Direktheit vs. Sanft:** Konfrontativ (Belief-Busting) oder einladend (Wellness)?
- **Humor-Level:** Trocken/sachlich · Zwinker-Humor · Komplett ernsthaft?
- **Emotionale Trigger:** Welche Gefühle soll der Leser haben? (Hoffnung, Dringlichkeit, Sicherheit, Erleichterung)
- **No-Gos im Wording:** Wörter/Phrasen die NIE vorkommen dürfen?

### Sekundär
- Referenz-Pages die genau diesen Tone treffen?
- Kontra-Referenzen (so wollen wir NICHT klingen)?

---

## DIMENSION 4: BRAND (Wie sieht es aus?)

### Pflicht-Fragen
- **Bestehende Brand-Assets?**
  - Logo (Variants?) ✅/❌
  - Farbpalette (Hex-Werte!) ✅/❌
  - Font-Pair (mit Google Fonts Names!) ✅/❌
  - Foto-Library (Founder/Product) ✅/❌
- **Visual-Direction:** Welche der 5 Default-Directions passt? (siehe `VISUAL-DIRECTIONS.md`)
- **Brand-Akzent-Element:** Gibt es ein Logo-Detail das wiederkehrend genutzt werden kann? (z.B. Stern, Pfeil, Ornament)
- **Reference-Brands (max 3):** Welche bestehenden Sites/Brands feedbackten als Match?

### Sekundär
- Bestehende Style-Guide oder Brand-Spec.md vorhanden?
- Was DARF NICHT vorkommen visuell? (z.B. Stockfotos, Glassmorphism, Bouncy-Animations)

---

## DIMENSION 5: SCALE (Wie groß / wie schnell / wie viel?)

### Pflicht-Fragen
- **Section-Count:** Wie viele Sections (LP)? Wie viele Slides (Deck)? Wie viele Mails (Sequenz)?
- **Copy-Länge pro Section:** Punchy 1-2 Sätze oder Editorial-Long-Form (5-10 Sätze)?
- **Animations-Komplexität:** Statisch · subtle Reveal · komplex GSAP-Choreography?
- **Interaktivität-Level:** Pure Display · Hover-States · Click-Effects · Full-App?

### Sekundär
- A/B-Test-Varianten gewünscht? (z.B. 2 Hero-Headlines)
- Personalisierung nötig? (z.B. Name-Token in Mails)
- CTA-Ziel: Anrufe · Buchung · Kauf · Lead-Magnet · Newsletter-Signup?

---

## OUTPUT — Discovery-Summary

Nach Form-Komplettierung → diese Summary erstellen (in `Sources/Discovery.md` oder Chat):

```markdown
# DISCOVERY — [Kunde] / [Funnel-Name]

**Datum:** YYYY-MM-DD

## Surface
- Format: [X]
- Pages: [N]
- Tech: [Stack]

## Audience
- Avatar: [Link zu Avatar.md]
- Sprache: [Du/Sie]
- Awareness: [Cold/Warm/Hot]

## Tone
- Brand-Vibe: [Editorial / SaaS / Luxury / etc.]
- Direktheit: [Konfrontativ / Sanft]
- No-Gos: [Liste]

## Brand
- Visual-Direction: [aus VISUAL-DIRECTIONS.md]
- Reference-Brands: [3 max]
- Assets-Status: Logo [✅/❌] · Palette [✅/❌] · Fonts [✅/❌] · Fotos [✅/❌]

## Scale
- Sections: [N]
- Copy-Länge: [Punchy / Long-Form]
- Animation: [Static / Subtle / Complex]
- Interaktivität: [Display / Hover / Click / App]

## Decisions
- [Konkrete Picks aus den Fragen]
```

---

## Red-Flag-Stops während der Form

Wenn beim Durchgehen der Form auffällt:

🚩 **Avatar fehlt** → STOP, erst Avatar erstellen (siehe `Brain/skills/new_client_blueprint/`)
🚩 **Marketing-Thesis fehlt** → STOP, erst Thesis erstellen
🚩 **Brand-Assets unklar** → STOP, Asset-Protokoll aus `huashu_design/SKILL.md` durchlaufen
🚩 **Visual-Direction unklar** → 5 Default-Directions aus `VISUAL-DIRECTIONS.md` zur Auswahl präsentieren
🚩 **Awareness-Level unklar** → ist der Lead Cold/Warm/Hot? Bestimmt Copy-Strategie

---

## Cross-References

- **Avatar erstellen:** `Brain/skills/new_client_blueprint/`
- **Visual-Directions:** `Brain/skills/design_tokens/VISUAL-DIRECTIONS.md`
- **Asset-Protokoll:** `Brain/skills/huashu_design/SKILL.md`
- **Workflow nach Discovery:** `Brain/skills/_universal/SECTION-BUILD-WORKFLOW.md`
- **CLAUDE.md REGEL 0.5:** Universal Onboarding (Pflicht bei JEDER Task)
