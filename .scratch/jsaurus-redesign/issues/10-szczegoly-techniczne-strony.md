# Szczegóły techniczne strony: OG, favicony, SEO, dostępność, wydajność

Type: grilling
Status: resolved
Blocked by:

## Question

Jakie są ustalenia techniczne „wokół” strony, których implementacja nie powinna zgadywać — przy znanej już strukturze (`/`, `/privacy`, 404; patrz „Struktura strony i przekaz”) i języku wizualnym („Język wizualny”)? Do rozstrzygnięcia:

- **Obraz OG/social** — jak wygląda w języku „List + Pieczątka” (statyczny jeden obraz vs generowany per strona), jaki tekst.
- **Favicony i ikony** — z płaskiego Sygnetu: zestaw (SVG favicon, `apple-touch-icon`, manifest?), tło, maskable.
- **SEO** — dane strukturalne (`Organization` / `Person` / `ProfessionalService` w JSON-LD?), sitemap i `hreflang` (już ustalone w i18n), `robots.txt`, canonical, trailing slash.
- **Dostępność poza kolorem** — poziom docelowy (WCAG 2.2 AA?), styl fokusu, kolejność czytania marginesu i listu na mobile, alt-teksty Pieczątki i zdjęcia, `prefers-reduced-motion`.
- **Budżet wydajności** — cele (np. Lighthouse 100, waga strony, fonty: podzbiory i `font-display`), obrazy (format, `astro:assets`).

## Answer

Rozstrzygnięte w grillingu z właścicielem (2026-10-16). Wszystkie rekomendacje przyjęte.

- **Obraz OG:** jeden statyczny `og.png` 1200×630 w repo, wspólny dla `/` i `/privacy` (404 bez OG). Biała „kartka”: Pieczątka po lewej, po prawej hasło *„Your company's developer — without hiring one.”* w Literacie, pod nim Logotyp „jsaurus” w Oxanium.
- **Favicony** (z płaskiego Sygnetu): `favicon.svg`; `favicon.ico` 32×32; `apple-touch-icon.png` 180×180 — żółty kwadrat z pazurami na całą powierzchnię, bez białej ramki. **Bez** `manifest.webmanifest`.
- **Dane strukturalne:** JSON-LD `ProfessionalService` tylko na `/` — nazwa JSaurus, `url`, `founder` (Person: Paweł Józefowski), adres (Almere), e-mail, `areaServed` NL/PL/UE, identyfikatory KvK i btw-id, `logo` (Sygnet).
- **SEO / adresy:** `site: https://jsaur.us`; `trailingSlash: 'always'` przy domyślnym `build.format: 'directory'` (`/privacy/`); canonical na każdej stronie; `@astrojs/sitemap` z opcją `i18n`; `robots.txt` — allow all + link do sitemap; 404 z `noindex`.
- **Dostępność — cel WCAG 2.2 AA:** fokus = czarna obwódka 2px z odstępem 4px (także na żółtych przyciskach); `<html lang="en">`; margines jako `aside`, w kolejności czytania przed listem; alt: Pieczątka „JSaurus”, zdjęcie „Paweł Józefowski”, pazury `aria-hidden`; `prefers-reduced-motion` wyłącza animacje przycisków, Pieczątki i 404; bez skip linka (brak nawigacji).
- **Budżet wydajności:** Lighthouse 100 na mobile we wszystkich kategoriach; zero JS; fonty woff2, podzbiory `latin` + `latin-ext`, `font-display: swap`, `preload` tylko Literaty 400; zdjęcie przez `astro:assets` (AVIF/WebP, ≤ ~60 KB); cała strona `/` ≤ ~200 KB łącznie z fontami i zdjęciem.
