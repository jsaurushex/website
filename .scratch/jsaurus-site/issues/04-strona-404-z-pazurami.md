# 04: Strona 404 „This page went extinct.” z animacją pazurów

Spec: `.scratch/jsaurus-redesign/spec.md` — Strony (404), Komponenty (ClawScratch), Dostępność i ruch.

**What to build:** Odwiedzający, który trafi na nieistniejący adres, widzi stronę „This page went extinct.” z krótkim wyjaśnieniem, linkiem „Back to the start” i jednorazową animacją rozdrapania pazurami (kształty pazurów wyodrębnione z Sygnetu). To jedyny ruch na stronie, który nie wynika z akcji użytkownika. Strona nie jest indeksowana.

**Blocked by:** 01 — Szkielet listu

**Status:** ready-for-agent

- [ ] Komponent ClawScratch: pazury jako ozdobnik `aria-hidden`, animacja wyłączona przy `prefers-reduced-motion: reduce` (wtedy pazury widoczne statycznie albo wcale).
- [ ] Strona 404 ma treść ze spec, link do `/`, `noindex`, brak meta OG; stopka prawna obecna.
- [ ] Testy: nieistniejąca ścieżka zwraca status 404 w `astro preview` i pokazuje „This page went extinct.”; `noindex` obecne; link prowadzi do `/`; przy emulacji reduced motion animacja nie działa; axe bez naruszeń.
