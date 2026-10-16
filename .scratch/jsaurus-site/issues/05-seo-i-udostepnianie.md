# 05: SEO i udostępnianie — meta, adresy, sitemap, dane strukturalne, OG i favicony

Spec: `.scratch/jsaurus-redesign/spec.md` — Stack (i18n, SEO/adresy), Meta, OG, favicony, dane strukturalne.

**What to build:** Link do `jsaur.us` wklejony w komunikator lub wyszukany w Google wygląda profesjonalnie: poprawny tytuł i opis, czysty obraz podglądu (biel, Pieczątka, hasło w Literacie, Logotyp), rozpoznawalny favicon (płaski Sygnet) w karcie i na ekranie telefonu, a wyszukiwarki rozumieją JSaurus jako firmę usługową. Adresy mają jeden styl (z ukośnikiem na końcu), są w sitemapie i są gotowe na przyszłe `/nl/` i `/pl/`.

**Blocked by:** 01 — Szkielet listu; 03 — Strona prywatności

**Status:** ready-for-agent

- [ ] `site: https://jsaur.us`, `trailingSlash: 'always'` przy formacie katalogów; canonical z ukośnikiem na `/` i `/privacy/`.
- [ ] Meta: title `JSaurus — web development for companies without an IT team` i description ze spec na `/`; sensowny title/description na `/privacy/`.
- [ ] Komponent `hreflang` (self + `x-default`), linki wewnętrzne przez helpery i18n Astro.
- [ ] `@astrojs/sitemap` z opcją `i18n` — sitemap zawiera `/` i `/privacy/`, nie zawiera 404; `robots.txt` pozwala na wszystko i wskazuje sitemap.
- [ ] JSON-LD `ProfessionalService` tylko na `/`: nazwa, `url`, `founder` (Person: Paweł Józefowski), adres (Almere), e-mail, `areaServed` (NL, PL, UE), identyfikatory KvK i btw-id (placeholder), `logo`.
- [ ] Statyczny obraz OG 1200×630 w repo, zgodny z opisem w spec, podpięty na `/` i `/privacy/` (`og:image`, `og:title`, `og:description`, `twitter:card`).
- [ ] Favicony z płaskiego Sygnetu: SVG, ICO 32×32, `apple-touch-icon` 180×180 (żółty kwadrat z pazurami na całą powierzchnię); bez web manifestu.
- [ ] Testy: title/description/canonical; obecność i poprawność OG; JSON-LD parsuje się i ma wymagane pola; sitemap i `robots.txt` jak wyżej; linki faviconów zwracają 200.
