# Architektura i18n pod EN / NL / PL

Type: research
Status: resolved
Blocked by:

## Question

Jak w najnowszym Astro (statyczny build, bez SSR) zbudować stronę, która startuje wyłącznie po angielsku, ale jest gotowa na dodanie NL i PL bez przebudowy? Do ustalenia z dokumentacji źródłowej: wbudowany routing i18n Astro (konfiguracja `i18n`, strategie prefiksów, domyślny język bez prefiksu, fallback), organizacja treści i tłumaczeń (content collections vs pliki słowników), generowanie `hreflang`/alternates i sitemap, przełącznik języka, oraz koszt „uśpionej” gotowości (co trzeba mieć od dnia 1, a co da się dodać później bez zmiany URL-i angielskich).

## Comments

- Research w toku: gałąź `research/i18n`, plik `.scratch/jsaurus-redesign/research/03-i18n.md`.

## Answer

Pełne ustalenia ze źródłami: gałąź `research/i18n` (commit `8e3291e`), plik `.scratch/jsaurus-redesign/research/03-i18n.md` (`git show research/i18n:.scratch/jsaurus-redesign/research/03-i18n.md`).

- **EN pod `/`** (`i18n.routing.prefixDefaultLocale: false`), NL/PL później pod `/nl/` i `/pl/` — dodanie języka to nowe pliki, angielskie URL-e nigdy się nie zmieniają.
- **Od dnia 1:** konfiguracja `i18n` z samym `en`; te same angielskie slugi we wszystkich językach; `site` i jedna zasada trailing slash; `<html lang>` z `Astro.currentLocale`; linki przez `getRelativeLocaleUrl`; słownik UI `src/i18n/ui.ts` tylko z `en`; własny komponent `hreflang` (self + `x-default`) i opcja `i18n` w `@astrojs/sitemap`.
- **Struktura treści:** osobne pliki stron per język z cienkimi szablonami; bez content collections i bez dynamicznej trasy `[...locale]` na start.
- **Nie używać:** `i18n.fallback` (w statyce generuje meta-refresh stronki trafiające do sitemap lub EN treść pod złym `lang`), `domains` i `preferredLocale` (wymagają SSR).
- **Później:** dopisanie `nl`/`pl`, tłumaczenia słownika, przełącznik języka jako zwykłe linki tylko do istniejących tłumaczeń (listy z `get*LocaleUrlList` trzeba filtrować), bez auto-przekierowań.
- Fakt: najnowsze Astro 7.3.5 (v7 nic nie zmienia w i18n względem v6).
