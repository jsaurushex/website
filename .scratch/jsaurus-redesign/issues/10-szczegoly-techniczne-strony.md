# Szczegóły techniczne strony: OG, favicony, SEO, dostępność, wydajność

Type: grilling
Status: open
Blocked by:

## Question

Jakie są ustalenia techniczne „wokół” strony, których implementacja nie powinna zgadywać — przy znanej już strukturze (`/`, `/privacy`, 404; patrz „Struktura strony i przekaz”) i języku wizualnym („Język wizualny”)? Do rozstrzygnięcia:

- **Obraz OG/social** — jak wygląda w języku „List + Pieczątka” (statyczny jeden obraz vs generowany per strona), jaki tekst.
- **Favicony i ikony** — z płaskiego Sygnetu: zestaw (SVG favicon, `apple-touch-icon`, manifest?), tło, maskable.
- **SEO** — dane strukturalne (`Organization` / `Person` / `ProfessionalService` w JSON-LD?), sitemap i `hreflang` (już ustalone w i18n), `robots.txt`, canonical, trailing slash.
- **Dostępność poza kolorem** — poziom docelowy (WCAG 2.2 AA?), styl fokusu, kolejność czytania marginesu i listu na mobile, alt-teksty Pieczątki i zdjęcia, `prefers-reduced-motion`.
- **Budżet wydajności** — cele (np. Lighthouse 100, waga strony, fonty: podzbiory i `font-display`), obrazy (format, `astro:assets`).
