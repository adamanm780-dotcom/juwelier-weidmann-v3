# Inspo — Juwelier Weidmann V3 (Scroll-Reveal Edition)

## Übergeordnete Richtung
Editorial-Luxus auf hellem Boden, dunkles Walnuss als geerdetes Gegengewicht, Jade als Akzent. **Neu in v3**: die Site arbeitet erzählerisch über Scroll-Driven-Imagery — der Hero "öffnet sich" beim Scrollen, Bilder rahmen sich neu, Sections reveal via Parallax. Aus Dribbble adaptierte Patterns (luxury-jewelry-website, scroll-driven-storytelling, editorial-fashion-website).

## Konkrete Anpassungen für Phase 6

- **Font-Pair**: Cormorant Garamond (Serif Headlines) + Inter (Sans Body) + Italiana (Logo/Display) — bleibt aus V1/V2.
- **Hero-Treatment**:
  - Vollformatiges Hero-Image mit Parallax-Speed 0.4 (Hintergrund scrollt langsamer als Foreground)
  - Beim Scrollen schrumpft der Hero auf eine inset-gerahmte Galerie-Ansicht zusammen (clip-path + transform-Animation getriggert via scroll progress)
  - Headline und Tagline fliegen in unterschiedlichen Geschwindigkeiten weg → tiefenwirkung
- **Section-Flourishes**:
  - **Sticky-Image-Reveal**: in der Atelier-Section bleibt das Bild gepinnt, Text-Blöcke wandern darüber durch
  - **Image-Lead-In**: Detail-Grid baut sich Bild-für-Bild aus dem Boden auf (translateY + opacity, gestaffelt via IntersectionObserver mit Stagger)
  - **Marquee-Band** zwischen Sections — horizontaler Streifen mit Material-Tags (Gold, Platin, Diamant, Jade, Smaragd)
  - **Diagonal-Cuts** zwischen Sections über `clip-path: polygon()` für sanften Walnuss-Übergang
- **Mikro-Interaktionen**:
  - Parallax-Layer auf Hero (2 Tiefenebenen)
  - Background-attachment fixed auf Atelier-Section
  - Hover-Tilt (3D) auf Kategorie-Karten
  - Magnetic Underline auf Nav
  - Cursor-Glow im Hero (subtil, jade-tinted)
- **Farb-Mood-Hinweis**: Body weiß/cream, Bands in Walnuss-Espresso, Jade als Akzent-Highlights — exakt nach V1/V2 Palette, aber dramatischere Hell-Dunkel-Wechsel zwischen Sections für Scroll-Drama.

## Limited Inspo
Direkter Dribbble-Browse aus Zeitgründen übersprungen — V3 baut auf bewährter V1/V2 Stilrichtung auf, fügt nur Scroll-Mechanics hinzu.
