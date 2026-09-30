# Warianty Logo z Affinity

Type: task (HITL)
Status: open
Blocked by:

## Question

Przygotować czyste, produkcyjne pliki Logo z oryginalnego projektu w Affinity, żeby decyzje o języku wizualnym, faviconach i trybie ciemnym opierały się na realnych wariantach. Obecny `src/assets/brand/logo.svg` ma pazury i cień jako osadzone bitmapy PNG, Logotyp jako żywy tekst zależny od fontu Oxanium i wypieczone białe tło.

Checklista dla właściciela (eksport do `src/assets/brand/`):

- [ ] Pazury i cień jako **wektory** (nie bitmapy); przy eksporcie SVG w Affinity: „Rasterise: Nothing”
- [ ] Logotyp **zamieniony na krzywe** (Convert to Curves)
- [ ] **Bez tła** (usunąć biały prostokąt), przycięte do zawartości (bez pustego marginesu 1500×1500)
- [ ] `sygnet.svg` — sam Sygnet
- [ ] `logo-horizontal.svg` — Sygnet + Logotyp obok siebie
- [ ] `logo-vertical.svg` — Sygnet nad Logotypem (jak obecnie)
- [ ] Wersje na **ciemne tło** dla powyższych (np. Logotyp biały; decyzja: czy cień Sygnetu zostaje czarny, znika, czy zmienia kolor)
- [ ] (opcjonalnie) `logotyp.svg` — sam napis
- [ ] Informacja: czy font Oxanium ma licencję pozwalającą na użycie go na stronie (Oxanium jest na Google Fonts, OFL — do potwierdzenia, jeśli użyto innej wersji)

Odpowiedź: lista wyeksportowanych plików + ewentualne ustalenia co do wersji ciemnej.
