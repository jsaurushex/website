Labels: wayfinder:map

# Przebudowa strony JSaurus

## Destination

Gotowa do implementacji specyfikacja nowej strony JSaurus: podjęte decyzje o stacku, wypracowany język wizualny oparty na Logo (kolory, typografia, zasady Logo, ruch, komponenty), struktura strony i przekaz ze szkicem treści (EN, architektura gotowa na NL i PL). Mapa kończy się, gdy nie zostaje nic do zdecydowania przed przebudową strony.

## Notes

- Domena: firmowa strona jednoosobowej firmy programistycznej — słownik w [CONTEXT.md](../../CONTEXT.md) (JSaurus, Logo, Sygnet, Logotyp, Język wizualny). Komunikacja osobista, 1. osoba l.poj.
- Stałe ustalenia: Astro + Tailwind zostają (reszta stacku do dyskusji); strona **statyczna**, wdrażana z VPS; repo docelowe `jsaurushex/website`; Logo jest **finalne** (język wizualny buduje się wokół niego); charakter „lekko zabawny, bez przegięcia”.
- Logo: Sygnet w `src/assets/brand/logomark.svg` (płaski) i `logomark-shadow.svg` (z twardym cieniem) — żółty (`#FFE406`) zaokrąglony kwadrat ze śladami pazurów; Logotyp „jsaurus” składany fontem Oxanium SemiBold (brak pliku). Oryginał z Logotypem w historii gita (`5af9680:src/assets/brand/logo.svg`).
- Specyfikacja zawiera przekaz i szkic tekstów; finalne dopracowanie tekstów następuje przy implementacji.
- Skille: `/grilling` + `/domain-modeling` dla grillingów; `/prototype` i `frontend-design:frontend-design` dla prototypów wizualnych; Context7 dla dokumentacji bibliotek.
- Poza mapą (robione osobno): aktualizacja zależności do najnowszych wersji i przeniesienie kodu do `jsaurushex/website`.
- Rozmowa z właścicielem po polsku; treść strony po angielsku.

## Decisions so far

<!-- the index — one line per closed ticket -->

- [Architektura i18n pod EN / NL / PL](issues/03-architektura-i18n-pod-en-nl-pl.md) — EN pod `/`, NL/PL później pod `/nl/` `/pl/`; od dnia 1 konfiguracja `i18n` z samym `en`, słownik UI, `hreflang` i sitemap; bez `fallback`/`domains`.
- [Kontakt na stronie statycznej — opcje](issues/04-kontakt-na-stronie-statycznej.md) — `mailto:` wystarcza jako rdzeń; jeśli formularz, to czysty HTML + honeypot na usłudze z UE (Formward); booking tylko jako link; bez reCAPTCHA i Web3Forms. Wybór zapada w strukturze strony.
- [Dla kogo jest strona i co oferujesz](issues/01-dla-kogo-jest-strona-i-co-oferujesz.md) — strona uwiarygadnia i mówi tylko do Klienta (MŚP bez IT, NL/PL); Modernizacja jako wiodąca usługa, potem aplikacje, strony firmowe, utrzymanie; bez cen; główna akcja: wiadomość.
- [Warianty Logo z Affinity](issues/02-warianty-logo-z-affinity.md) — Sygnet jako czyste SVG w dwóch wersjach (płaska do małych rozmiarów, z cieniem do dużych); Logotyp na razie składany fontem Oxanium; w kodzie `logomark`/`wordmark`.
- [Charakter i ton marki](issues/05-charakter-i-ton-marki.md) — konkretny, spokojnie doświadczony, osobisty, uczciwy, z przymrużeniem oka; humor w detalach + jedno mrugnięcie w hero; metafory tylko wokół Modernizacji; prosty angielski; efekt pisania znika, easter egg w stopce zostaje w nowej formie.

## Not yet specified

- **Szczegóły techniczne strony**: tryb ciemny (czy i jak Sygnet działa na ciemnym tle), obraz OG/social, favicony i ikony aplikacji z Sygnetu, podstawy SEO (sitemap, meta, dane strukturalne firmy), dostępność (kontrast żółci `#FFE406` na bieli!), budżet wydajności. Do rozbicia, gdy znany będzie język wizualny i struktura.

## Out of scope

- **Blog / notatki** — świadomie odłożone; architektura nie powinna go blokować, ale go nie projektujemy.
- **Wdrożenie na VPS** (serwer, CI/CD, przepięcie DNS z GitHub Pages) — wykonanie, nie decyzja tej mapy.
- **Finalne dopracowanie tekstów** — dzieje się przy implementacji.
- **Oferta dla Agencji partnerskich na stronie** — agencje są pozyskiwane innymi kanałami ([Dla kogo jest strona i co oferujesz](issues/01-dla-kogo-jest-strona-i-co-oferujesz.md)).
- **Komplet plików Logo** (Logotyp w krzywych, warianty poziomy/pionowy) — praca nad plikami, na którą nie czeka żadna decyzja; do zrobienia kiedykolwiek ([Warianty Logo z Affinity](issues/02-warianty-logo-z-affinity.md)).
- **Cennik / pakiety cenowe** — świadomie brak cen na stronie, zawsze wycena po rozmowie ([Dla kogo jest strona i co oferujesz](issues/01-dla-kogo-jest-strona-i-co-oferujesz.md)).
- **Tłumaczenia NL/PL i przełącznik języka** — architektura jest na nie gotowa ([Architektura i18n pod EN / NL / PL](issues/03-architektura-i18n-pod-en-nl-pl.md)), ale start jest tylko po angielsku.
