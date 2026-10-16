Status: ready-for-agent

# Spec: nowa strona JSaurus

Źródło decyzji: mapa „Przebudowa strony JSaurus” (`.scratch/jsaurus-redesign/map.md`) i jej dziesięć rozstrzygniętych ticketów. Słownik pojęć: `CONTEXT.md` — w tym dokumencie używane są jego terminy (**JSaurus**, **Klient**, **Agencja partnerska**, **Modernizacja**, **Logo**, **Sygnet**, **Pieczątka**, **Logotyp**, **Język wizualny**).

## Problem Statement

JSaurus — jednoosobowa firma programistyczna Pawła Józefowskiego — pozyskuje Klientów głównie z poleceń. Osoba, która dostała nazwisko od znajomego, wchodzi na `jsaur.us`, żeby sprawdzić, czy to poważny wykonawca. Dziś znajduje tam stronę z 2024 roku (Astro 3, GitHub Pages) z tekstem wpisywanym literka po literce, emoji dinozaurów i hasłem o JavaScripcie, które nic nie mówi właścicielowi małej firmy bez IT. Nie widać, co JSaurus konkretnie robi, dla kogo, jak wygląda współpraca ani kto za tym stoi; kontakt pojawia się dopiero po zakończeniu animacji. Firma ma za to nowe Logo, którego strona w ogóle nie używa. Lokalny kod (Astro 7, po aktualizacji zależności) zawiera jeszcze szablon startowy i stary layout.

## Solution

Nowa, statyczna strona w formie **osobistego listu od Paula**: jedna strona główna, która w kilkadziesiąt sekund mówi Klientowi (MŚP bez własnego IT, NL/PL), że JSaurus to „your company's developer — without hiring one”, co robi (z Modernizacją na czele), kim jest człowiek po drugiej stronie, na jakich zasadach pracuje — i daje jedną oczywistą akcję: napisz maila.

Wygląd wynika z Logo: biała „kartka”, spokojny szeryf w treści, Pieczątka (Sygnet z twardym cieniem, obrócony o −7°) z Logotypem w marginesie zamiast nagłówka, żółć tylko w przyciskach-naklejkach z twardym cieniem. Humor marki żyje w detalach: wciskająca się Pieczątka i strona 404 „This page went extinct.” z animacją pazurów. Strona jest szybka (zero JS), dostępna (WCAG 2.2 AA), zgodna z holenderskimi wymogami informacyjnymi i RODO (bez ciasteczek, analityki ani zewnętrznych zasobów), gotowa na późniejsze wersje NL i PL bez zmiany angielskich adresów.

## User Stories

### Klient sprawdzający wykonawcę

1. As a Klient who got Paul's name from a recommendation, I want to understand within seconds what JSaurus does and for whom, so that I know I'm in the right place.
2. As a Klient without an IT department, I want the headline to speak about my situation rather than about technology, so that I feel addressed and not lectured.
3. As a Klient, I want to see that I would work with one real person, so that I trust I won't be passed to a sales team.
4. As a Klient with an old web system nobody wants to touch, I want Modernisation to be the first service I read about, so that I immediately see my problem is the specialty here.
5. As a Klient, I want each service described in one or two plain sentences, so that I understand it without technical knowledge.
6. As a Klient, I want to read that my old system keeps running while its replacement is built, so that I'm not afraid of downtime.
7. As a Klient, I want to see that JSaurus also builds web applications, company websites and handles care & maintenance, so that I know the full range of help available.
8. As a Klient, I want a short mention of integrations and technical advice, so that I know I can ask about those too.
9. As a Klient evaluating credibility, I want to see how long Paul has been doing this (15+ years), so that I can judge experience.
10. As a Klient evaluating credibility, I want to read that Paul has kept one business-critical platform in the advertising industry running for more than ten years, so that I believe in long-term reliability.
11. As a Klient, I want to read that Paul builds company websites for businesses like mine, so that I can picture working together.
12. As a Klient, I want an honest statement about what JSaurus is not (not a 20-person team), so that I trust the rest of the claims.
13. As a Klient, I want to see a real photo of Paul next to the bio, so that I know a real person stands behind the company.
14. As a Klient, I want three clear working principles (free first conversation, fixed quote before work, I own the code), so that I know the rules before I make contact.
15. As a Klient, I want no prices on the page but a clear promise of a quote after a conversation, so that I'm not put off by numbers out of context.
16. As a Klient reading English as a second language (Dutch or Polish), I want short sentences without idioms, so that I understand everything.
17. As a Klient, I want the tone to be calm and competent with only a light wink, so that the site feels professional and still human.

### Kontakt

18. As a Klient ready to act, I want one obvious "Write to me" button right after the headline, so that I can make contact without searching.
19. As a Klient, I want the button to open my email program with the address filled in, so that writing takes one click.
20. As a Klient without a configured email program, I want the email address visible as text next to the button, so that I can copy it.
21. As a Klient who read to the end, I want the letter to close with a signature and the email address, so that I don't have to scroll back up to make contact.
22. As a Klient, I want to read that Paul usually replies within one working day, so that I know what to expect after writing.
23. As a Klient, I want the email address always visible in the margin, so that contact is never more than a glance away.

### Marka i wygląd

24. As a visitor, I want to see the JSaurus Pieczątka with the Logotyp beside the opening of the letter, so that I recognise the brand without a separate header.
25. As a visitor, I want the Pieczątka to press down slightly when I point at it, so that I discover a small playful detail.
26. As a visitor, I want the "Write to me" button to look like a yellow sticker with a hard shadow that presses down when clicked, so that the interaction feels tactile and on-brand.
27. As a visitor, I want the Modernisation metaphor ("Legacy doesn't have to mean extinct.") set apart with a thin yellow bar, so that the one dinosaur wink stands out without shouting.
28. As a visitor on a phone, I want the margin (Pieczątka, Logotyp, note, email) to sit compactly above the letter, so that the layout works on a small screen.
29. As a visitor on a phone, I want no horizontal scrolling and comfortably sized text, so that reading is easy.
30. As a visitor who lands on a missing page, I want a friendly "This page went extinct." page with a claw-scratch animation and a link back, so that the error is clear and on-brand.
31. As a visitor sharing the site in a chat or on social media, I want a clean preview image with the Pieczątka, headline and Logotyp, so that the link looks professional.
32. As a visitor, I want a recognisable favicon (the flat Sygnet) in my browser tab and on my phone's home screen, so that I can find the site again.

### Prawo i prywatność

33. As a Klient, I want company details (JSaurus, Paweł Józefowski, office address, KvK number, btw-id, email) in the footer of every page, so that I can verify the business is registered.
34. As the owner, I want the footer to satisfy Dutch disclosure rules (art. 3:15d BW; details at most one click away), so that the site is legally compliant.
35. As a visitor, I want a short privacy page linked from the footer, so that I know what happens to my data when I write.
36. As a visitor, I want the privacy page to state that the site sets no cookies, uses no analytics and loads nothing from third parties, so that I can trust it.
37. As a visitor, I want the privacy page to name the processors involved (Apple iCloud mail, Hetzner hosting in Germany), my rights and how to complain to the Autoriteit Persoonsgegevens, so that I can exercise them.
38. As a visitor, I want no cookie banner, so that nothing stands between me and the content.

### Dostępność

39. As a keyboard user, I want a clearly visible focus outline on every link and button (including the yellow ones), so that I always know where I am.
40. As a screen-reader user, I want the page language declared, meaningful alt text on the Pieczątka and photo, and decorative claw marks hidden, so that I hear only what matters.
41. As a screen-reader user, I want the margin marked as complementary content and read before the letter, so that the order makes sense.
42. As a visitor sensitive to motion, I want all animations (button press, Pieczątka, 404 claws) disabled when I've asked my system for reduced motion, so that the site is comfortable to use.
43. As any visitor, I want text colours with sufficient contrast (yellow never used for text), so that everything is readable.

### Wydajność i SEO

44. As a visitor on a slow mobile connection, I want the page to load almost instantly (no JavaScript, small fonts and images), so that I don't give up waiting.
45. As a visitor, I want the text to appear immediately even while fonts load, so that I can start reading at once.
46. As the owner, I want search engines to understand JSaurus as a professional service (name, founder, address, area served, KvK/btw-id), so that the company is presented correctly in results.
47. As the owner, I want a sitemap, robots file and canonical URLs with one consistent trailing-slash style, so that the site is indexed cleanly.
48. As the owner, I want the 404 page excluded from indexing, so that it never appears in search results.

### Właściciel i przyszłość

49. As the owner, I want English at `/` and the structure ready for Dutch at `/nl/` and Polish at `/pl/`, so that adding languages later never changes existing English URLs.
50. As the owner, I want all UI strings in one dictionary, so that translations later are a matter of adding entries.
51. As the owner, I want my name shown as "Paul" in the English greeting and as "Paweł Józefowski" where credibility matters (signature, footer, structured data), so that both familiarity and formality are covered.
52. As the owner, I want a neutral photo placeholder in the repository until I provide a real photo, so that no stranger's face is ever published under my name.
53. As the owner, I want fonts self-hosted from my own domain, so that no visitor data goes to Google.
54. As the owner, I want the old starter template, old layout, daisyUI and emoji-based animations removed, so that the codebase contains only the new site.
55. As the owner, I want automated tests that check content, SEO, accessibility, the no-JS/no-third-party rule and reduced motion on the built site, so that future changes don't silently break these promises.
56. As the owner, I want a Lighthouse check against the performance budget, so that the site stays fast as it evolves.

## Implementation Decisions

### Stack

- **Astro 7 + Tailwind CSS v4**, wynik w pełni statyczny (bez adaptera, bez SSR), serwowany jako pliki z własnego VPS. Node ≥ 22.12.
- **daisyUI zostaje usunięte** (zależność i plugin w globalnym CSS). Brak jakiejkolwiek biblioteki komponentów.
- **Brak frameworka UI (React/Svelte/Preact) i brak JS** po stronie przeglądarki. Wszystkie interakcje to CSS.
- **Fonty przez wbudowane Fonts API Astro** (opcja `fonts` w konfiguracji), provider Fontsource, podzbiory `latin` + `latin-ext`, format woff2, `font-display: swap`:
  - **Literata**: 400, 600, kursywa 400 — preload tylko 400.
  - **Oxanium**: 600 (ewentualnie 700).
- **i18n Astro** skonfigurowane od dnia 1 z jednym językiem: `defaultLocale: 'en'`, `locales: ['en']`, `prefixDefaultLocale: false`. Bez `fallback`, bez `domains`. `<html lang>` z `Astro.currentLocale`; linki wewnętrzne przez helpery i18n Astro; teksty interfejsu w jednym słowniku (na razie tylko `en`). Strony jako osobne pliki per język z cienkimi szablonami (bez content collections i bez dynamicznej trasy po locale). Własny komponent `hreflang` (self + `x-default`).
- **SEO/adresy:** `site: https://jsaur.us`; `trailingSlash: 'always'` przy domyślnym `build.format: 'directory'` (np. `/privacy/`); canonical na każdej stronie; `@astrojs/sitemap` z opcją `i18n`; `robots.txt` — allow all + link do sitemap; 404 z `noindex`.

### Tokeny Języka wizualnego (jedno źródło prawdy: blok `@theme` Tailwind v4)

| Token | Wartość | Rola |
|---|---|---|
| `paper` | `#FFFFFF` | tło |
| `ink` | `#000000` | nagłówki, ramki i cień przycisków, fokus |
| `text` | `#2F2F2C` | treść |
| `muted` | `#66665F` | tekst drugorzędny |
| `hair` | `#E3E3DD` | linie włoskowe |
| `signal` | `#FFE406` | wyłącznie powierzchnie (przyciski, Sygnet, kreska metafory) — **nigdy tekst ani cienkie linie na białym** |

- Fonty jako tokeny: `serif` = Literata (nagłówek główny i treść, ~19px / 1,7; nagłówek ~34–52px, 600; podtytuł kursywą), `display` = Oxanium SemiBold (Logotyp z rozstrzeleniem ~0,18em, małe nagłówki sekcji ~17px w sentence case, podpis, przyciski).
- Przycisk-naklejka: tło `signal`, ramka 2px `ink`, twardy cień 5px `ink` (przesunięcie w prawo i w dół, bez rozmycia), promień ~12px; hover — unosi się o 1px (cień rośnie), active — wciska się do zera (przesunięcie o długość cienia, cień znika).
- Pieczątka: Sygnet w wersji z cieniem, obrót −7°; hover — obrót −2° i skala ~0,92 (sprężyste przejście ~160ms).
- Kolumna listu ~40rem; margines po lewej (na desktopie wyrównany do prawej krawędzi, obok listu); na mobile margines w jednym rzędzie nad treścią.
- Tylko tryb jasny.

### Zasady Logo

- Pieczątka (Sygnet z cieniem, −7°) to główna forma Logo na stronie — **jedna**, w marginesie, z Logotypem „jsaurus” (Oxanium) pod spodem.
- Płaski, prosty Sygnet — tylko małe rozmiary (favicony).
- Sygnet nigdy na żółtym tle.
- Logotyp nie ma pliku — składany fontem Oxanium.
- Pliki Sygnetu już są w repo w katalogu marki: wersja płaska i z cieniem, obie czyste wektorowo.

### Komponenty (Astro; klasy Tailwind w markupie, stany przycisku i Pieczątki w lokalnych stylach komponentów)

- **BaseLayout** — `<head>` (title, description, canonical, OG, favicony, hreflang, fonty), `lang`, opcjonalny JSON-LD, opcjonalne `noindex`.
- **LetterLayout** — siatka margines + kolumna listu i cicha stopka prawna; slot na treść listu i na margines.
- **Stamp** — Pieczątka z Logotypem (zestaw w marginesie); alt „JSaurus”.
- **StickerButton** — przycisk-naklejka renderowany jako link (`mailto:` lub URL).
- **Section** — linia włoskowa + mały nagłówek Oxanium + slot.
- **Signature** — podpis kończący list (imię i nazwisko, „JSaurus, Almere”, e-mail).
- **ClawScratch** — animacja pazurów na 404 (pazury jako ozdobnik `aria-hidden`; kształty pazurów wyodrębnione z Sygnetu).
- Prawdopodobnie też mały komponent zdjęcia z placeholderem (ramka 4:5, podpis „photo”) do czasu prawdziwego zdjęcia.

### Strony

- **`/`** — jeden list. Kolejność:
  1. Margines: Pieczątka + Logotyp; notka „Based in Almere. Working remotely across the Netherlands, Poland and the EU.”; e-mail.
  2. Otwarcie: „Hi, I'm Paul.” → hasło *„Your company's developer — without hiring one.”* → podtytuł *„I bring old web systems back to life — and build new ones that last.”* → przycisk „Write to me” + „or write to hello@jsaur.us”.
  3. **What I do**: Modernisation (z metaforą „Legacy doesn't have to mean extinct.” przy żółtej kresce) → Web applications → Company websites → Care & maintenance → linijka „Also: …”. Usługi jako proza z pogrubionym tytułem, bez kart.
  4. **Who you'll work with**: zdjęcie + bio (15+ years, „You'll talk to me, not to a sales team.”), dwa akapity dowodów (platforma w branży reklamowej od 2015; strony firmowe od produkcji żywności po małe studia), zdanie o 20-osobowym zespole.
  5. **How I work**: trzy zasady (bezpłatna, niezobowiązująca pierwsza rozmowa; stała wycena przed pracą; Klient jest właścicielem kodu) + „Tell me what's slowing your company down. I usually reply within one working day.”
  6. Podpis: Paweł Józefowski / JSaurus, Almere / e-mail. Bez drugiej Pieczątki i bez drugiego przycisku.
  7. Stopka: JSaurus, Paweł Józefowski | Randstad 22/46, 1316BZ Almere | KvK 88270793 | btw-id | hello@jsaur.us | Privacy.
- **`/privacy/`** — w tym samym LetterLayout: administrator; dane = tylko to, co ktoś przyśle mailem; cel = odpowiedź i wycena (działania przed umową / prawnie uzasadniony interes); okres = czas rozmowy, u Klientów 7 lat (NL, obowiązek podatkowy); podmioty przetwarzające = Apple iCloud (poczta), Hetzner w Niemczech (hosting); brak ciasteczek, analityki i zasobów zewnętrznych; prawa + skarga do Autoriteit Persoonsgegevens.
- **404** — „This page went extinct.” / „The page you were looking for doesn't exist anymore — or never did.” / link „Back to the start”; ClawScratch; `noindex`; bez OG.
- **Pełny szkic treści EN** (meta, wszystkie sekcje, stopka, 404) jest w odpowiedzi ticketu „Struktura strony i przekaz” — to kierunek; finalne szlify tekstów należą do implementacji, ale bez zmiany przekazu, kolejności i zasad tonu.

### Treść i ton (reguły dla finalnych szlifów)

- Prosty, międzynarodowy angielski (~B2): krótkie zdania, bez idiomów i slangu.
- Cechy: konkretny, spokojnie doświadczony, osobisty, uczciwy, z przymrużeniem oka — humor tylko w detalach + jedno mrugnięcie w otwarciu („back to life”).
- Metafory dinozaura wyłącznie wokół Modernizacji, max jedna na sekcję; bez emoji 🦕🦖 i gier słownych.
- „JSaurus” w tekście zawsze z wielkim „JS”; małe „jsaurus” tylko w Logotypie.
- Brak cen; brak nazw Klientów, rekomendacji i linków do LinkedIn/GitHub.

### Kontakt

- Wyłącznie `mailto:hello@jsaur.us` (przycisk + widoczny adres w otwarciu, marginesie, podpisie i stopce). Bez formularza, bez linku do kalendarza, bez analityki.

### Meta, OG, favicony, dane strukturalne

- title: `JSaurus — web development for companies without an IT team`; description: `JSaurus is Paweł (Paul) Józefowski — a web developer who builds, modernises and maintains web systems for companies without their own IT team.`
- Jeden statyczny obraz OG 1200×630 w repo (biel; Pieczątka po lewej; hasło w Literacie po prawej; Logotyp pod spodem), wspólny dla `/` i `/privacy/`.
- Favicony z płaskiego Sygnetu: SVG; ICO 32×32; `apple-touch-icon` 180×180 (żółty kwadrat z pazurami na całą powierzchnię). Bez web manifestu.
- JSON-LD `ProfessionalService` tylko na `/`: nazwa, `url`, `founder` (Person: Paweł Józefowski), adres (Almere), e-mail, `areaServed` (NL, PL, UE), identyfikatory KvK i btw-id, `logo`.

### Dostępność i ruch

- Cel WCAG 2.2 AA. Fokus: czarna obwódka 2px z odstępem 4px na każdym interaktywnym elemencie. Margines jako `aside`, w kolejności czytania przed listem. Alt: Pieczątka „JSaurus”, zdjęcie „Paweł Józefowski”; pazury `aria-hidden`. Bez skip linka (brak nawigacji).
- `prefers-reduced-motion: reduce` wyłącza animacje przycisku, Pieczątki i 404. Żadnych animacji wejścia ani ruchu bez akcji użytkownika poza 404.

### Wydajność

- Lighthouse 100 na mobile we wszystkich kategoriach; zero JS; zdjęcie przez `astro:assets` (AVIF/WebP, ≤ ~60 KB); cała strona `/` ≤ ~200 KB łącznie z fontami i zdjęciem.

### Sprzątanie

- Usunąć szablon startowy (komponent powitalny i jego grafiki), stary layout z efektem pisania, stopkę z emoji, zastępczy favicon Astro, daisyUI. Treść i dane z `config` przenieść do słownika/stałych nowej strony.
- Zastępcze zdjęcie stockowe istnieje tylko lokalnie w ignorowanym katalogu zasobów deweloperskich i **nie może** trafić do repo ani na produkcję; w repo neutralny placeholder.

## Testing Decisions

- **Jedna warstwa testów, na samej górze: zbudowana strona.** Testy end-to-end w **Playwright** uruchamiane na wyniku `astro build` serwowanym przez `astro preview`. Testy patrzą wyłącznie na to, co dostaje przeglądarka (HTML, odpowiedzi sieciowe, wyrenderowany wygląd), a nie na komponenty — wolno zmieniać implementację, dopóki zachowanie widoczne dla odwiedzającego się nie zmienia.
- Dobry test sprawdza obietnicę wobec odwiedzającego lub właściciela, np. „przycisk w otwarciu prowadzi do `mailto:hello@jsaur.us`”, „żadne żądanie nie wychodzi poza origin strony”, a nie strukturę DOM, nazwy klas czy liczbę elementów.
- Zakres:
  - **Treść i struktura** — sekcje w ustalonej kolejności (What I do → Who you'll work with → How I work → podpis); Modernisation jako pierwsza usługa; przycisk `mailto:`; widoczny adres e-mail; stopka z adresem, KvK, btw-id i e-mailem na każdej stronie; link do `/privacy/`.
  - **Meta i SEO** — title, description, canonical z ukośnikiem, OG (obraz, tytuł), `lang="en"`, JSON-LD `ProfessionalService` z wymaganymi polami na `/`, `noindex` na 404 (i status 404 dla nieistniejącej ścieżki), sitemap zawiera `/` i `/privacy/`, `robots.txt` wskazuje sitemap.
  - **Dostępność** — skan **axe-core** (`@axe-core/playwright`) bez naruszeń na poziomie WCAG 2.2 AA dla `/`, `/privacy/` i 404; alt-teksty Pieczątki i zdjęcia; widoczny fokus na przycisku po nawigacji klawiaturą.
  - **Zero JS i zero zasobów zewnętrznych** — brak elementów `<script>` w wynikowym HTML (poza JSON-LD) i brak żądań sieciowych poza origin strony (fonty lokalne).
  - **Ograniczony ruch** — przy emulacji `prefers-reduced-motion: reduce` animacje/przejścia przycisku, Pieczątki i 404 są wyłączone.
  - **Mobile** — przy szerokości 375px brak poziomego przewijania.
- **Budżet wydajności** — **Lighthouse CI** na tym samym buildzie: wynik 100 (mobile) we wszystkich kategoriach i budżet wagi `/` ≤ ~200 KB.
- Bez testów jednostkowych komponentów — pojedynczy komponent nie ma tu zachowania wartego testowania w izolacji.
- **Prior art:** brak — w repo nie ma jeszcze żadnych testów; to będzie pierwszy zestaw. Skrypt testowy powinien być uruchamialny jednym poleceniem z `package.json`.

## Out of Scope

- Blog / notatki.
- Wdrożenie na VPS (serwer, CI/CD, przepięcie DNS z GitHub Pages) — osobna praca.
- Tłumaczenia NL/PL i przełącznik języka (architektura gotowa, treść tylko EN).
- Tryb ciemny.
- Formularz kontaktowy, link do kalendarza, analityka (struktura pozwala dodać później; analityka tylko bezciasteczkowa i self-hosted).
- Cennik / pakiety cenowe.
- Oferta dla Agencji partnerskich na stronie.
- Nazwy Klientów, logotypy, rekomendacje, linki do LinkedIn/GitHub.
- Komplet plików Logo (Logotyp w krzywych, warianty poziomy/pionowy).

## Further Notes

- **Przed releasem (nie blokuje implementacji):** prawdziwe zdjęcie zamiast placeholdera; numer btw-id w stopce i w JSON-LD; usunięcie gałęzi `prototype/jezyk-wizualny`; opcjonalnie rekomendacje i zgody od 2–3 Klientów.
- **Prototyp Języka wizualnego** (warianty A–D, zwycięzca D „Połączenie”) jest na gałęzi `prototype/jezyk-wizualny` — referencja wizualna dla implementacji, ale kod napisany pod rygorem prototypu: przepisać porządnie, nie kopiować 1:1.
- **Szczegóły decyzji i ich uzasadnienia** — w ticketach mapy: „Dla kogo jest strona i co oferujesz”, „Charakter i ton marki”, „Język wizualny”, „Warianty Logo z Affinity”, „daisyUI i system komponentów”, „Architektura i18n pod EN / NL / PL”, „Kontakt na stronie statycznej — opcje”, „Dowody wiarygodności”, „Struktura strony i przekaz”, „Szczegóły techniczne strony”. Research o i18n i kontakcie na gałęziach `research/i18n` i `research/kontakt`.
- **Wymogi prawne stopki** (NL): art. 3:15d BW, Ondernemersplein i ACM — źródła w ticketcie „Dowody wiarygodności”.
- Strona statyczna oznacza, że status 404 i `trailingSlash` zależą też od konfiguracji serwera na VPS (np. nginx `error_page 404` i obsługa katalogów) — do uwzględnienia przy wdrożeniu.
