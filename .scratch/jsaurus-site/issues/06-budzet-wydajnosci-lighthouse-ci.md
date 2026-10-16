# 06: Budżet wydajności — Lighthouse CI

Spec: `.scratch/jsaurus-redesign/spec.md` — Wydajność, Testing Decisions (budżet).

**What to build:** Właściciel ma jednopoleceniową kontrolę, która na zbudowanej stronie potwierdza, że strona jest i zostanie szybka: Lighthouse 100 na mobile we wszystkich kategoriach i `/` do ~200 KB łącznie z fontami i zdjęciem — a strona faktycznie ten budżet spełnia.

**Blocked by:** 02 — Pełna treść listu; 03 — Strona prywatności; 04 — Strona 404; 05 — SEO i udostępnianie

**Status:** ready-for-agent

- [ ] Lighthouse CI uruchamiany jednym poleceniem z `package.json` na wyniku `astro build` dla `/` i `/privacy/` (profil mobile).
- [ ] Asercje: 100 w Performance, Accessibility, Best Practices i SEO; budżet wagi `/` ≤ ~200 KB.
- [ ] Strona spełnia budżet: preload tylko Literaty 400, fonty woff2 w podzbiorach, obrazy przez `astro:assets` (AVIF/WebP), zero JS.
- [ ] Wyniki i ewentualne świadome odstępstwa opisane w komentarzu zamykającym ticket.
