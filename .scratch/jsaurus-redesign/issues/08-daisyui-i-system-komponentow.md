# daisyUI i system komponentów

Type: grilling
Status: resolved
Blocked by: 07

## Question

Czy przy ustalonym Języku wizualnym daisyUI zostaje (z własnym motywem), zostaje zastąpione inną biblioteką, czy komponenty powstają na czystym Tailwind? Jak tokeny z Języka wizualnego trafiają do Tailwind (`@theme`), jaki jest minimalny zestaw komponentów strony i czy potrzebny jest jakikolwiek framework UI (islands) poza Astro. Wejście z „Język wizualny”: tokeny kolorów i typografii, przycisk-naklejka z twardym cieniem, brak kart, układ list + margines, jeden motyw jasny — patrz odpowiedź w tym tickecie.

## Answer

Rozstrzygnięte w grillingu z właścicielem (2026-10-02). Wszystkie rekomendacje przyjęte.

- **daisyUI odchodzi.** Czysty Tailwind v4; jedyne dotychczasowe użycie (`btn` w starym `Layout.astro`) i tak znika. Do tematu bibliotek wracamy dopiero, gdy dojdzie złożony UI (np. formularze).
- **Tokeny w `@theme` Tailwind v4** — kolory (`paper`, `ink`, `text`, `muted`, `hair`, `signal`), fonty, promień i cień przycisku z „Język wizualny”; dostępne i jako klasy (`bg-signal`, `font-display`…), i jako zmienne CSS. Jedno źródło prawdy.
- **Style:** komponenty pisane klasami Tailwind w markupie; stany przycisku-naklejki i Pieczątki (hover/active, obrót −7°) w małych lokalnych `<style>` komponentów.
- **Minimalny zestaw komponentów** (może urosnąć po „Struktura strony i przekaz”):
  - `BaseLayout` — `<head>`, fonty, meta, `lang`
  - `LetterLayout` — siatka margines + kolumna listu, cicha stopka
  - `Stamp` — Pieczątka z Logotypem (zestaw w marginesie)
  - `StickerButton` — przycisk-naklejka (link `mailto:` / zewnętrzny)
  - `Section` — linia włoskowa + mały nagłówek Oxanium
  - `Signature` — podpis kończący list
  - `ClawScratch` — animacja pazurów na stronie 404
- **Bez frameworka UI i bez JS na starcie** — wszystkie interakcje to CSS; ewentualny formularz kontaktowy jako czysty HTML.
- **Fonty przez Fonts API Astro** (`fonts` w `astro.config`, stabilne w Astro 7), provider Fontsource, podzbiory `latin` + `latin-ext`: Literata 400, 600, kursywa 400; Oxanium 600 (ew. 700). Pobierane przy buildzie i serwowane z `jsaur.us`.
