# Juwelier Achim Weidmann (V3)

**Slug:** juwelier-weidmann-v3
**Branche:** Juwelier · Goldschmied
**Build-Datum:** 2026-05-11
**Live-URL:** https://adamanm780-dotcom.github.io/juwelier-weidmann-v3/
**Repo:** https://github.com/adamanm780-dotcom/juwelier-weidmann-v3
**Lokal:** C:\Users\Adria\claude-discord-projects\allgemein\juwelier-weidmann-3

## Kontakt
- Adresse: Burgstraße 3, 65183 Wiesbaden
- Telefon: +49 611 374 280
- E-Mail: n/a
- Öffnungszeiten: Di–Fr 10:00–18:30 · Sa 10:00–16:00 · So + Mo geschlossen
- Website (Original): n/a
- Instagram: n/a

## Design
- Palette: #fbf8f3 #ffffff #f5ede1 #ebe0cf #231711 #2f6e5b #5b3f2c
- Fonts: Cormorant Garamond + Inter + Italiana
- Style-Richtung: hell + dunkles Holz + jade, editorial-luxury, scroll-driven (Bilder leiten beim Scrollen in die Website hinein), durchgängiges Parallax

## Assets
- Hero: assets/hero.webp (übernommen aus v1 — Nano Banana 21:9 → Real-ESRGAN 4K)
- Maps-Fotos: n/a (kein reichhaltiges GBP)
- Insta-Posts: n/a (kein Handle)
- Zusatz-Assets: texture.webp, detail-01…06.webp, about.webp

## Build-Stats
- Build-Zeit: ~6m (Assets-Reuse aus v1)
- Sections im HTML: 11 (Topbar · Header · Hero · Marquee · Intro · Categories · Featured · Atelier · Parallax-Band · Detail-Grid · Testimonial · Kontakt · Footer)

## Scroll-Mechanics (V3-spezifisch)
- Hero ist 140vh hoch mit sticky inner-frame — beim Scrollen scaled das Bild leicht hoch, Content fliegt schneller weg, Hairline-Border öffnet sich nach außen → Bild "öffnet" sich in die Site
- Atelier-Section: 2-Spalten-Grid mit sticky Image links und scrollendem Text rechts (Slow-Drift-Parallax am Bild)
- Parallax-Band zwischen Detail-Sections: Hintergrund bewegt sich 30% relativ zur Section
- Marquee-Band in Walnuss zwischen Hero und Intro
- Reveal-on-Scroll mit IntersectionObserver (Stagger) auf Grid-Items
- Cursor-Glow nur im Hero (Desktop-only)

## Updates
- 2026-05-11: Initial Build V3 (light + dark wood + scroll-driven hero reveal + parallax band + sticky atelier)
- 2026-05-11: Scroll-Frame-Animation eingebaut (50 Frames, Seedance 1.0-Pro + Nano-Banana-Greenscreen, Platinring rotiert beim Scrollen von Front- zur Aufsicht). Asset-Ordner: assets/scroll/frames-clean/ (1.5MB, WebP-alpha via ffmpeg colorkey)
- 2026-05-11: Scroll-Animation neu generiert — Jade-Ring durch Diamant-Solitärring ersetzt. Alte Frames hatten Greenscreen-Artefakte (grüner Saum, Geister-Reflexion), weil das Jade-Grün mit Chromakey #00b140 verschmolzen ist. Neuer Pipeline-Wechsel: Nano Banana auf reinem Weiß-BG → Seedance 1.0-Pro → ffmpeg-Extraktion → AI-Background-Remover `lucataco/remove-bg` pro Frame (statt Chromakey) → libwebp Q82 mit Alpha. Resultat: 1.9MB, kein grüner Saum, Diamant und Metall sauber freigestellt. Caption/Alt-Text angepasst auf „Platin · Brillant".
- 2026-05-11: Scroll-Frames 006–050 (45 Stk.) einzeln re-cleaned. Vorherige Cleanup-Runde hatte ab Frame ~10 noch Geister-/Grünreste am Ring-Band (Metall mit Greenscreen-Reflexion verschluckte vereinzelte Chromakey-Defekte). Pipeline: für jeden Frame Upload zu Replicate Files → `851-labs/background-remover` (rgba, threshold 0) → libwebp Q80 mit Alpha. Frames 001–005 belassen (waren bereits sauber). Backup der alten frames-clean wurde nach Verifikation entfernt — Original-PNGs bleiben in `assets/scroll/frames/` als Quelle erhalten.
