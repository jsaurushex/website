Labels: wayfinder:map

# Przebudowa strony JSaurus

## Destination

Gotowa do implementacji specyfikacja nowej strony JSaurus: podjęte decyzje o stacku, wypracowany język wizualny oparty na Logo (kolory, typografia, zasady Logo, ruch, komponenty), struktura strony i przekaz ze szkicem treści (EN, architektura gotowa na NL i PL). Mapa kończy się, gdy nie zostaje nic do zdecydowania przed przebudową strony.

## Notes

- Domena: firmowa strona jednoosobowej firmy programistycznej — słownik w [CONTEXT.md](../../CONTEXT.md) (JSaurus, Logo, Sygnet, Logotyp, Język wizualny). Komunikacja osobista, 1. osoba l.poj.
- Stałe ustalenia: Astro + Tailwind zostają (reszta stacku do dyskusji); strona **statyczna**, wdrażana z VPS; repo docelowe `jsaurushex/website`; Logo jest **finalne** (język wizualny buduje się wokół niego); charakter „lekko zabawny, bez przegięcia”.
- Logo: `src/assets/brand/logo.svg` — żółty (`#FFE406`) zaokrąglony kwadrat z twardym czarnym cieniem i śladami pazurów + logotyp „jsaurus” w Oxanium SemiBold.
- Specyfikacja zawiera przekaz i szkic tekstów; finalne dopracowanie tekstów następuje przy implementacji.
- Skille: `/grilling` + `/domain-modeling` dla grillingów; `/prototype` i `frontend-design:frontend-design` dla prototypów wizualnych; Context7 dla dokumentacji bibliotek.
- Poza mapą (robione osobno): aktualizacja zależności do najnowszych wersji i przeniesienie kodu do `jsaurushex/website`.
- Rozmowa z właścicielem po polsku; treść strony po angielsku.

## Decisions so far

<!-- the index — one line per closed ticket -->

- [Architektura i18n pod EN / NL / PL](issues/03-architektura-i18n-pod-en-nl-pl.md) — EN pod `/`, NL/PL później pod `/nl/` `/pl/`; od dnia 1 konfiguracja `i18n` z samym `en`, słownik UI, `hreflang` i sitemap; bez `fallback`/`domains`.

## Not yet specified

- **Szczegóły techniczne strony**: tryb ciemny (czy i jak Sygnet działa na ciemnym tle), obraz OG/social, favicony i ikony aplikacji z Sygnetu, podstawy SEO (sitemap, meta, dane strukturalne firmy), dostępność (kontrast żółci `#FFE406` na bieli!), budżet wydajności. Do rozbicia, gdy znany będzie język wizualny i struktura.
- **Losy obecnych animacji**: efekt pisania intro i pasek dinozaurów w stopce — zależą od charakteru marki i języka wizualnego; pewnie wpadną do ticketu o języku wizualnym albo osobnego o ruchu.
- **Dowody wiarygodności**: czy i jakie referencje, case studies, logotypy klientów, opinie — wyjaśni się po ustaleniu grupy docelowej i struktury.

## Out of scope

- **Blog / notatki** — świadomie odłożone; architektura nie powinna go blokować, ale go nie projektujemy.
- **Wdrożenie na VPS** (serwer, CI/CD, przepięcie DNS z GitHub Pages) — wykonanie, nie decyzja tej mapy.
- **Finalne dopracowanie tekstów** — dzieje się przy implementacji.
- **Tłumaczenia NL/PL i przełącznik języka** — architektura jest na nie gotowa ([Architektura i18n pod EN / NL / PL](issues/03-architektura-i18n-pod-en-nl-pl.md)), ale start jest tylko po angielsku.
