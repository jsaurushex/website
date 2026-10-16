# 01: Szkielet listu — otwarcie, Pieczątka, kontakt i stopka (z testami od dnia 1)

Spec: `.scratch/jsaurus-redesign/spec.md` — sekcje Stack, Tokeny Języka wizualnego, Zasady Logo, Komponenty, Strony (`/` punkty 1, 2, 7), Kontakt, Dostępność i ruch, Sprzątanie, Testing Decisions.

**What to build:** Odwiedzający wchodzi na `/` i widzi nowy początek strony JSaurus w języku „List + naklejki”: w marginesie Pieczątka z Logotypem „jsaurus”, notka o pracy zdalnej i e-mail; obok otwarcie listu — „Hi, I'm Paul.”, hasło, podtytuł, żółty przycisk-naklejka „Write to me” (`mailto:hello@jsaur.us`) i widoczny adres do skopiowania; na dole cicha stopka prawna. Stara strona (szablon startowy, efekt pisania, emoji dinozaurów, motyw daisyUI) znika z kodu. Od tego ticketu istnieje jednopoleceniowy zestaw testów end-to-end na zbudowanej stronie, który kolejne tickety rozszerzają.

**Blocked by:** None (can start immediately)

**Status:** ready-for-agent

- [ ] Z projektu usunięte: daisyUI (zależność i plugin), komponent powitalny szablonu i jego grafiki, stary layout z efektem pisania, stopka z emoji, zastępczy favicon Astro; dane z dotychczasowego configu przeniesione do słownika/stałych nowej strony.
- [ ] Tokeny kolorów (`paper`, `ink`, `text`, `muted`, `hair`, `signal`), fontów (`serif` = Literata, `display` = Oxanium), promień i cień przycisku zdefiniowane w jednym miejscu (`@theme` Tailwind v4) i używane przez komponenty.
- [ ] Literata (400, 600, kursywa 400) i Oxanium (600) ładowane przez Fonts API Astro z Fontsource, podzbiory `latin` + `latin-ext`, `font-display: swap`; żadne żądanie nie idzie do Google ani innych zewnętrznych hostów.
- [ ] i18n Astro skonfigurowane z jednym językiem (`en`, bez prefiksu, bez `fallback`); `<html lang>` pochodzi z bieżącego locale; teksty interfejsu w jednym słowniku.
- [ ] Komponenty BaseLayout, LetterLayout, Stamp i StickerButton istnieją i składają stronę `/` zgodnie ze spec (margines jako `aside` przed listem; na mobile margines w jednym rzędzie nad treścią).
- [ ] Przycisk-naklejka: żółte tło, ramka i twardy cień w `ink`, unosi się na hover i wciska do zera na active; Pieczątka (Sygnet z cieniem, −7°) wciska się na hover; obie animacje wyłączone przy `prefers-reduced-motion: reduce`.
- [ ] Widoczny fokus (czarna obwódka 2px z odstępem 4px) na każdym linku i przycisku, także żółtym.
- [ ] Stopka na `/`: JSaurus, Paweł Józefowski | Randstad 22/46, 1316BZ Almere | KvK 88270793 | btw-id (placeholder do uzupełnienia) | hello@jsaur.us.
- [ ] Zestaw Playwright (+ `@axe-core/playwright`) uruchamiany jednym poleceniem z `package.json` na wyniku `astro build` serwowanym przez `astro preview`; testy sprawdzają: przycisk w otwarciu prowadzi do `mailto:hello@jsaur.us`; adres e-mail widoczny jako tekst; stopka zawiera adres, KvK i e-mail; `lang="en"`; brak `<script>` (poza ewentualnym JSON-LD) i brak żądań poza origin; animacje przycisku i Pieczątki wyłączone przy emulacji reduced motion; brak poziomego przewijania przy 375px; axe bez naruszeń WCAG 2.2 AA na `/`.
- [ ] Lokalne zdjęcie stockowe z ignorowanego katalogu zasobów deweloperskich nie trafia do repo ani do buildu.
