# Reference — UTE Wagner Karriere-Sales-Page

> **Use-Case:** Wiederverwendbare Vorlage für Sales-Karriere-LPs (Recruiting: Setter/Closer für Coaching/Mentoring-Businesses)

**Live-Beispiel:** https://utewagner.de/karriere-vertrieb/
**Original-Quelle:** `Agency/UTE Wagner/Website & Funnels/Karriereseite/`
**Stand:** 14. Mai 2026

---

## Wann diese Referenz nehmen?

Wenn ein Kunde Setter / Closer / Sales-Talente recruiten will und eine **eigene Karriere-LP** braucht. Funktioniert besonders gut für:

- Coaching- / Mentoring-Businesses mit klarem Hochpreis-Offer
- Praxis-Unternehmer:innen / Therapeut:innen-Zielgruppe (B2B)
- Personenmarken mit starkem Founder-Story-Component
- Wenn Vertrauen + Substanz > Pushy Sales gefragt sind

---

## Design-System

### Farben
```css
--cream:        #f5f2ec   /* Background */
--cream-soft:   #efebe2   /* Section-Splits */
--teal:         #2a6b6e   /* Primary CTA / Buttons */
--teal-deeper:  #133539   /* Dark Sections */
--gold:         #c9a87a   /* Akzent / Apply-CTA-Background */
--gold-deep:    #b08a5d   /* Hover-State Gold */
--text:         #1a1a1a
--text-light:   #6b6b6b
```

### Fonts
- **Display:** Fraunces (Variable Serif, italic-friendly für Akzente)
- **Body:** DM Sans

### Stil
Editorial / Magazine — hochwertig, ruhig, viel Whitespace, kein AI-Slop. Italic-Serif für emotionale Akzente, Sans für Klarheit.

---

## Wiederverwendbare Patterns

### 1. Hero mit Foto-Right-Layout
- Linke Spalte: Eyebrow + Headline (Fraunces + Italic em-Tag) + Sub + 2 CTAs + Pills
- Rechte Spalte: Foto vom Founder (Speaker-Pose / authentisch, kein Stockfoto)
- Animation: fadeUp-Sequenz mit gestaffelten Delays

### 2. Stellen-Cards (Setter + Closer Split)
- Zwei nebeneinander: Light-Card + Dark-Card (visueller Kontrast)
- Pro Card: Position-Label, Titel, Sub, Aufgaben-Liste mit Pfeilen, Earning-Block, eigener CTA
- Wirkung: "Du kannst wählen — beide sind ernst gemeint"

### 3. Verdienst-Transparency-Block
- Innerhalb jeder Card: klarer Grundgehalt-Range, klare Provisions-Logik
- Top-Performer-Beispiel ("erreichbar in 6-12 Monaten")
- Kein vages Marketing — konkrete Zahlen + Realismus

### 4. Karriere-Timeline (3-Phasen)
- Visual Timeline mit Phasen-Bodies (Onboarding → Eigenständigkeit → Senior)
- Konkrete Meilensteine pro Phase ("Erste eigene Calls in Woche 4")

### 5. Match-Section ("Für dich / Nicht für dich")
- Zwei-Spalten-Layout: ✕-Liste links, →-Liste rechts
- Disqualifikation = Selbst-Selektion → bessere Conversion-Qualität

### 6. FAQ-Accordion
- 5-6 echte Einwand-Fragen (Verdienst, Remote, Team-Größe, Erfahrung)
- Button + Icon-Toggle (CSS-only Accordion möglich)

### 7. Apply-CTA mit Gold-Background
- Eigene Section, Goldgrund mit SVG-Noise-Overlay
- Headline + Italic-Akzent + Sub + Single-Button → externe Bewerbungs-URL
- Apply-Meta-Pills unter Button (Position · Standort · Start)

### 8. Floating Section-Indicator
- Rechte Seite, fixiert, scrollt mit
- Zeigt aktive Section auf einen Blick
- Dezent, aber Orientierung auf langer Page

### 9. Sticky-Nav mit CTA
- Logo links, Section-Links Mitte, Apply-CTA rechts
- Mobile-Burger mit Vollbild-Menu
- Backdrop-Blur für premium Feel

---

## Tech-Setup (Coolify-Hosting-Pattern)

```
Karriereseite/
├── karriere.html          # Index-HTML (in nginx.conf gesetzt)
├── Dockerfile             # nginx:alpine Buildpack
├── nginx.conf             # try_files routing
└── assets/                # Bilder, Logos, Favicons
```

**Key Lesson — Subpath-Hosting:** Bei einer LP unter `/karriere-vertrieb/` (kein Root) **immer `<base href="/karriere-vertrieb/">`** im `<head>`. Sonst brechen relative Asset-Pfade ohne Trailing-Slash.

---

## Performance-Notes

- WebP + JPG Fallback via `<picture>` für Hero-Bilder
- Google Fonts async geladen (kein Render-Blocking)
- Explizite `width`/`height` auf allen Bildern (Layout-Stability)
- Inline-CSS für Above-the-fold (kein externes CSS, kein FOUC)
- GSAP/Lenis-frei — pure CSS-Animations (`fadeUp` via Keyframes)

---

## Copy-Prinzipien (für ähnliche Funnels)

- **Konkrete Zahlen statt Marketing-Phrasen:** "2.300-2.500 € Grundgehalt" statt "attraktives Gehalt"
- **Founder-Story als Anker:** Echte Geschichte > Corporate-Speak
- **Disqualifikation einbauen:** "Nicht für dich wenn ..." — wirkt stärker als Inklusion alleine
- **Externe Bewerbung > Inline-Form:** Weniger Reibung, kein Webhook-Setup nötig, sauberer Tracking-Übergang in ATS/CRM
- **Italic-Em-Tag für emotionale Momente:** `<em>` mit Serif-Italic = Magazin-Feeling

---

## Files in diesem Ordner

| Datei | Zweck |
|-------|-------|
| `karriere.html` | Komplette HTML mit allen Sections (vollständig referenzierbar) |
| `assets/` | Bilder + Logos + Favicons |
| `Dockerfile` | Coolify Docker-Buildpack-Vorlage |
| `nginx.conf` | nginx-Config mit korrektem `try_files` für SPA-ähnliches Routing |
| `README.md` | Diese Datei |
