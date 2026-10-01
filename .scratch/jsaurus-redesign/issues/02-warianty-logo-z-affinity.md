# Warianty Logo z Affinity

Type: task (HITL)
Status: resolved
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

## Answer

Zrobione (2026-10-01), częściowo przez właściciela (eksport z Affinity), częściowo przez agenta (wersja z cieniem, porządki).

Pliki w `src/assets/brand/`:

- **`logomark.svg`** — Sygnet płaski: czyste wektory (bez bitmap), bez tła, przycięty do zawartości (`viewBox="34.55 26.82 1430.9 1446.36"`), zdublowany żółty kształt usunięty. Eksport właściciela (pierwotnie `logo_trademark.svg`).
- **`logomark-shadow.svg`** — Sygnet z twardym czarnym cieniem: ten sam kształt co kwadrat, przesunięty o **2,56% szerokości** w prawo i w dół (45°) — proporcja zmierzona z bitmapy cienia oryginalnego `logo.svg` (22 / 860,6 j.), więc wierne odtworzenie, nie przybliżenie.
- Oryginalny `logo.svg` (z bitmapami i Logotypem) usunięty z dysku; zostaje w historii gita (commit `5af9680`) jako wzorzec.

Decyzje:

- **Dwie wersje Sygnetu:** płaska do małych rozmiarów (favicon, ikony), z cieniem do większych ekspozycji. Czy twardy cień staje się też motywem interfejsu — rozstrzyga „Język wizualny”.
- **Logotyp na razie bez plików:** na stronie „jsaurus” składane fontem Oxanium (SemiBold, rozstrzelenie; OFL). Komplet plików Logo z Logotypem w krzywych — później, poza mapą.
- **Ciemne tło:** Sygnet działa bez zmian; szczegóły w „Języku wizualnym”.
- **Nazewnictwo:** w kodzie i plikach angielskie odpowiedniki — Sygnet = `logomark`, Logotyp = `wordmark` (zapisane w CONTEXT.md).
