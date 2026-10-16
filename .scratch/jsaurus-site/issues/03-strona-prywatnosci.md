# 03: Strona prywatności

Spec: `.scratch/jsaurus-redesign/spec.md` — Strony (`/privacy/`), user stories 35–38.

**What to build:** Odwiedzający klika „Privacy” w stopce dowolnej strony i trafia na `/privacy/` w tym samym układzie listu, gdzie prostym angielskim dowiaduje się: kto jest administratorem, jakie dane są przetwarzane (tylko to, co ktoś przyśle mailem), w jakim celu i na jakiej podstawie, jak długo (czas rozmowy; u Klientów 7 lat — NL obowiązek podatkowy), kto przetwarza (Apple iCloud — poczta; Hetzner w Niemczech — hosting), że strona nie używa ciasteczek, analityki ani zewnętrznych zasobów, oraz jakie ma prawa i jak złożyć skargę do Autoriteit Persoonsgegevens.

**Blocked by:** 01 — Szkielet listu

**Status:** ready-for-agent

- [ ] `/privacy/` renderuje się w LetterLayout z Pieczątką w marginesie i tą samą stopką prawną.
- [ ] Stopka na każdej stronie zawiera link „Privacy” do `/privacy/`.
- [ ] Treść obejmuje wszystkie punkty z opisu powyżej; ton zgodny z regułami (prosty angielski).
- [ ] Testy: link w stopce prowadzi do `/privacy/`; strona zawiera wzmianki o braku ciasteczek, o Apple iCloud, Hetzner i Autoriteit Persoonsgegevens; stopka prawna obecna; axe bez naruszeń.
