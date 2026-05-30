# Lessons Learned

> Diese Datei wird nach jeder abgeschlossenen Task automatisch gepflegt.
> Format: Datum | Task | Was fehlte | Fix eingetragen

| Datum | Task | Was hat gefehlt | Fix |
|-------|------|-----------------|-----|
| 2026-03-31 | SMS Karriere-LP v3 — Mobile Responsive | Skill wurde nicht getriggert: Prompts ("mobile fix", "responsive", "card") matchen kein LP-Keyword im skill_router → skill_router.py Keywords ergänzen | "responsive\|mobile fix\|karriere.?lp\|seite optimieren" → landingpage_agent |
| 2026-03-31 | SMS Karriere-LP v3 — Mobile Responsive | SKILL.md beschreibt Copy-Prozess, nicht HTML/CSS-Build → bei LP-Build komplett falsch | SKILL.md: zweite Section "LP BUILD" anlegen mit Animations-Stack, design.md Pflicht, Responsive-Checklist |
| 2026-03-31 | SMS Karriere-LP v3 — Mobile Hero Card | Mobile-Card ohne 3D startend → hatte nur statisches Bild | Fix: `card-fall` + `card-float` Keyframes (bereits global definiert) direkt auf `.mobile-mo-float-wrap` referenzieren — kein neues JS nötig |
| 2026-03-31 | SMS Karriere-LP v3 — Job Card Toggle | Toggle-Button overflow: `grid-template-columns:1fr auto` + langer Titel → `min-width:auto` auf Grid-Item überschreibt Track-Breite | Fix: `min-width:0` auf `.job-header > div:first-child` — zwingt Text-Spalte in Grid-Spur |
| 2026-03-31 | SMS Karriere-LP v3 — Preload | `<link rel="preload">` zeigte auf `mo-v3-nobg.png` (alte Datei) statt `IMG_8181.JPG` (tatsächliches Hero-Bild) | Immer Preload-Asset nach Bild-Wechsel prüfen |
| 2026-03-31 | SMS Karriere-LP v3 — Timeline Bar Mobile | `steps-bar` ist `position:absolute` im 4-Spalten-Grid → bei 2×2-Spalten-Layout auf Mobile verbindet Bar nur Zeile 1 | Fix: `display:none` bei ≤768px — Bar funktioniert strukturell nur bei 4-spaltigem Grid |
