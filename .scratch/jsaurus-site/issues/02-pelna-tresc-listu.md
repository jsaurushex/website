# 02: Pełna treść listu — What I do, Who you'll work with, How I work, podpis

Spec: `.scratch/jsaurus-redesign/spec.md` — Strony (`/` punkty 3–6), Treść i ton, Komponenty (Section, Signature, placeholder zdjęcia). Pełny szkic treści EN: odpowiedź ticketu „Struktura strony i przekaz” (`.scratch/jsaurus-redesign/issues/06-struktura-strony-i-przekaz.md`).

**What to build:** Klient czytający `/` po otwarciu dostaje cały list: co JSaurus robi (Modernizacja pierwsza, z metaforą „Legacy doesn't have to mean extinct.” przy żółtej kresce; potem aplikacje, strony firmowe, utrzymanie i linijka „Also: …”), z kim będzie pracował (placeholder zdjęcia, bio z 15+ years, dwa ogólne akapity dowodów, uczciwe zdanie o 20-osobowym zespole), na jakich zasadach (trzy zasady + obietnica odpowiedzi w jeden dzień roboczy) — a list kończy się podpisem z e-mailem.

**Blocked by:** 01 — Szkielet listu

**Status:** ready-for-agent

- [ ] Komponenty Section (linia włoskowa + mały nagłówek Oxanium) i Signature istnieją; usługi jako proza z pogrubionym tytułem, bez kart.
- [ ] Sekcje na `/` w kolejności: What I do → Who you'll work with → How I work → podpis; Modernisation jest pierwszą usługą.
- [ ] Treść zgodna ze szkicem EN i regułami tonu (prosty angielski, metafora dinozaura tylko przy Modernizacji, brak emoji, brak cen, brak nazw Klientów); „JSaurus” zawsze z wielkim „JS”.
- [ ] Placeholder zdjęcia: neutralna ramka 4:5 z podpisem „photo”, z alt „Paweł Józefowski”; gotowy do podmiany na prawdziwe zdjęcie przez `astro:assets` (AVIF/WebP) bez zmiany układu.
- [ ] Podpis: „Paweł Józefowski”, „JSaurus, Almere”, e-mail jako link `mailto:`; bez drugiej Pieczątki i drugiego przycisku.
- [ ] Testy: kolejność sekcji; Modernisation pierwsza; trzy zasady obecne; podpis zawiera e-mail; alt zdjęcia/placeholdera; axe bez naruszeń na `/`.
