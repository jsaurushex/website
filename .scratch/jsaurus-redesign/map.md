Labels: wayfinder:map

# Przebudowa strony JSaurus

**Status: zakończona (2026-10-16)** — wszystkie tickety rozstrzygnięte; następny krok to implementacja.

## Destination

Gotowa do implementacji specyfikacja nowej strony JSaurus: podjęte decyzje o stacku, wypracowany język wizualny oparty na Logo (kolory, typografia, zasady Logo, ruch, komponenty), struktura strony i przekaz ze szkicem treści (EN, architektura gotowa na NL i PL). Mapa kończy się, gdy nie zostaje nic do zdecydowania przed przebudową strony.

## Notes

- Domena: firmowa strona jednoosobowej firmy programistycznej — słownik w [CONTEXT.md](../../CONTEXT.md) (JSaurus, Logo, Sygnet, Logotyp, Język wizualny). Komunikacja osobista, 1. osoba l.poj.
- Stałe ustalenia: stack = Astro 7 + Tailwind v4 (bez daisyUI, bez frameworka UI, bez JS na starcie, fonty przez Fonts API); strona **statyczna**, wdrażana z VPS; repo docelowe `jsaurushex/website`; Logo jest **finalne** (język wizualny buduje się wokół niego); charakter „lekko zabawny, bez przegięcia”.
- Logo: Sygnet w `src/assets/brand/logomark.svg` (płaski) i `logomark-shadow.svg` (z twardym cieniem) — żółty (`#FFE406`) zaokrąglony kwadrat ze śladami pazurów; Logotyp „jsaurus” składany fontem Oxanium SemiBold (brak pliku). Oryginał z Logotypem w historii gita (`5af9680:src/assets/brand/logo.svg`).
- Specyfikacja zawiera przekaz i szkic tekstów; finalne dopracowanie tekstów następuje przy implementacji.
- Skille: `/grilling` + `/domain-modeling` dla grillingów; `/prototype` i `frontend-design:frontend-design` dla prototypów wizualnych; Context7 dla dokumentacji bibliotek.
- Poza mapą (robione osobno): aktualizacja zależności do najnowszych wersji i przeniesienie kodu do `jsaurushex/website`.
- Rozmowa z właścicielem po polsku; treść strony po angielsku.
- **Przed releasem:** usunąć gałąź `prototype/jezyk-wizualny` (warianty języka wizualnego zostawione do wglądu); podmienić placeholder na prawdziwe zdjęcie; uzupełnić btw-id w stopce; opcjonalnie poprosić 2–3 klientów o rekomendacje i zgody na nazwy.

## Decisions so far

<!-- the index — one line per closed ticket -->

- [Architektura i18n pod EN / NL / PL](issues/03-architektura-i18n-pod-en-nl-pl.md) — EN pod `/`, NL/PL później pod `/nl/` `/pl/`; od dnia 1 konfiguracja `i18n` z samym `en`, słownik UI, `hreflang` i sitemap; bez `fallback`/`domains`.
- [Kontakt na stronie statycznej — opcje](issues/04-kontakt-na-stronie-statycznej.md) — `mailto:` wystarcza jako rdzeń; jeśli formularz, to czysty HTML + honeypot na usłudze z UE (Formward); booking tylko jako link; bez reCAPTCHA i Web3Forms. Wybór zapada w strukturze strony.
- [Dla kogo jest strona i co oferujesz](issues/01-dla-kogo-jest-strona-i-co-oferujesz.md) — strona uwiarygadnia i mówi tylko do Klienta (MŚP bez IT, NL/PL); Modernizacja jako wiodąca usługa, potem aplikacje, strony firmowe, utrzymanie; bez cen; główna akcja: wiadomość.
- [Warianty Logo z Affinity](issues/02-warianty-logo-z-affinity.md) — Sygnet jako czyste SVG w dwóch wersjach (płaska do małych rozmiarów, z cieniem do dużych); Logotyp na razie składany fontem Oxanium; w kodzie `logomark`/`wordmark`.
- [Charakter i ton marki](issues/05-charakter-i-ton-marki.md) — konkretny, spokojnie doświadczony, osobisty, uczciwy, z przymrużeniem oka; humor w detalach + jedno mrugnięcie w hero; metafory tylko wokół Modernizacji; prosty angielski; efekt pisania znika, easter egg w stopce zostaje w nowej formie.
- [Język wizualny](issues/07-jezyk-wizualny.md) — kierunek „List + naklejki”: biel, Literata + Oxanium, żółć tylko w przyciskach-naklejkach z twardym cieniem, Sygnecie i kresce metafory; Pieczątka (Sygnet z cieniem, −7°) jako główne Logo w marginesie, bez nagłówka; tylko tryb jasny; pazury na 404.
- [daisyUI i system komponentów](issues/08-daisyui-i-system-komponentow.md) — daisyUI odchodzi; tokeny w `@theme` Tailwind v4; 7 komponentów Astro (BaseLayout, LetterLayout, Stamp, StickerButton, Section, Signature, ClawScratch); zero frameworków i JS; fonty przez Fonts API z Fontsource.
- [Dowody wiarygodności](issues/09-dowody-wiarygodnosci.md) — bez nazw, rekomendacji i profili; dowodem są dwa ogólne akapity (wieloletnia platforma dla branży reklamowej, strony firmowe), liczby „15+ / 10+ years”, trzy zasady „How I work” i prawdziwe zdjęcie; stopka prawna NL z adresem, KvK, btw-id i e-mailem.
- [Struktura strony i przekaz](issues/06-struktura-strony-i-przekaz.md) — jeden list pod `/` + `/privacy` + 404; kontakt tylko `mailto:` (przycisk + widoczny adres); bez analityki; kolejność: otwarcie → What I do → Who you'll work with → How I work → podpis; pełny szkic treści EN w tickecie.
- [Szczegóły techniczne strony: OG, favicony, SEO, dostępność, wydajność](issues/10-szczegoly-techniczne-strony.md) — jeden statyczny OG; favicon.svg + .ico + apple-touch-icon, bez manifestu; JSON-LD `ProfessionalService`; adresy z ukośnikiem, sitemap i robots; WCAG 2.2 AA; Lighthouse 100, zero JS, `/` ≤ ~200 KB.

## Not yet specified

<!-- pusto: mapa zakończona 2026-10-16 — nic nie zostało do zdecydowania przed przebudową -->


## Out of scope

- **Blog / notatki** — świadomie odłożone; architektura nie powinna go blokować, ale go nie projektujemy.
- **Wdrożenie na VPS** (serwer, CI/CD, przepięcie DNS z GitHub Pages) — wykonanie, nie decyzja tej mapy.
- **Finalne dopracowanie tekstów** — dzieje się przy implementacji.
- **Oferta dla Agencji partnerskich na stronie** — agencje są pozyskiwane innymi kanałami ([Dla kogo jest strona i co oferujesz](issues/01-dla-kogo-jest-strona-i-co-oferujesz.md)).
- **Komplet plików Logo** (Logotyp w krzywych, warianty poziomy/pionowy) — praca nad plikami, na którą nie czeka żadna decyzja; do zrobienia kiedykolwiek ([Warianty Logo z Affinity](issues/02-warianty-logo-z-affinity.md)).
- **Nazwy klientów, rekomendacje, LinkedIn/GitHub na stronie** — świadomie nie teraz ([Dowody wiarygodności](issues/09-dowody-wiarygodnosci.md)).
- **Formularz kontaktowy, link do kalendarza, analityka** — świadomie nie na start; struktura pozwala dodać je później ([Struktura strony i przekaz](issues/06-struktura-strony-i-przekaz.md)).
- **Cennik / pakiety cenowe** — świadomie brak cen na stronie, zawsze wycena po rozmowie ([Dla kogo jest strona i co oferujesz](issues/01-dla-kogo-jest-strona-i-co-oferujesz.md)).
- **Tryb ciemny** — świadomie tylko jasny na start ([Język wizualny](issues/07-jezyk-wizualny.md)).
- **Tłumaczenia NL/PL i przełącznik języka** — architektura jest na nie gotowa ([Architektura i18n pod EN / NL / PL](issues/03-architektura-i18n-pod-en-nl-pl.md)), ale start jest tylko po angielsku.
