# Język wizualny

Type: prototype
Status: resolved
Blocked by: 05

## Question

Jak wygląda Język wizualny JSaurus wyprowadzony z Logo? Paleta (żółć `#FFE406`, czerń, neutralne; role kolorów i kontrast — żółć na bieli nie przejdzie jako tekst), typografia (czy Oxanium z Logotypu jako nagłówki + krój do treści), zasady użycia Logo i Sygnetu, charakter kształtów (zaokrąglenia, twardy przesunięty cień z Sygnetu jako motyw?), ikonografia/ilustracje (pazury), ruch i animacje, tryb ciemny. Wejście z „Charakter i ton marki”: pazury jako rzadki akcent (maks. 2–3 razy na stronie), bez ilustracji dinozaurów i emoji; efekt pisania intro odpada, a ruchomy easter egg w stopce potrzebuje nowej formy zgodnej z Sygnetem (np. przemykające ślady pazurów). Wejście z „Warianty Logo z Affinity”: Sygnet płaski i z twardym cieniem — czy twardy cień staje się motywem interfejsu. Rozstrzygnąć na podstawie 2–3 szybkich prototypów kierunków do porównania; wynik: tokeny + zasady.

## Answer

Rozstrzygnięte z właścicielem na prototypie (2026-10-01). Prototyp: gałąź **`prototype/jezyk-wizualny`** (commit `df20b31`) — `pnpm dev`, potem `/?variant=A|B|C|D` (←/→ przełącza). Warianty: A „Naklejka”, B „Sygnał”, C „List”, D „Połączenie” (zwycięzca). Gałąź zostaje do ewentualnego wglądu; **usunąć przed releasem**.

**Kierunek: D** — układ i typografia „Listu” (C) + przyciski-naklejki z twardym cieniem z „Naklejki” (A) + Pieczątka jako główna forma Logo. „Sygnał” (B) odrzucony w całości (żółte tła, czarne sekcje, wielkie pazury).

**Kolory (tokeny):**

| Token | Hex | Rola |
|---|---|---|
| `paper` | `#FFFFFF` | tło |
| `ink` | `#000000` | nagłówki, ramki i cień przycisków |
| `text` | `#2F2F2C` | treść |
| `muted` | `#66665F` | drugorzędny tekst (kontrast ~5,9:1) |
| `hair` | `#E3E3DD` | linie włoskowe |
| `signal` | `#FFE406` | wyłącznie powierzchnie — nigdy tekst ani cienkie linie na białym (1,3:1) |

**Typografia:** Literata (szeryf) — nagłówek główny i treść, 19px / 1,7, nagłówek ~34–52px, waga 600; podtytuł kursywą. Oxanium SemiBold — Logotyp (rozstrzelenie 0,18em), małe nagłówki sekcji (~17px, sentence case), podpis, przyciski. Fonty **hostowane samodzielnie** (OFL; bez Google Fonts CDN — RODO).

**Żółć tylko w trzech miejscach:** przyciski-naklejki (żółte tło, ramka 2px `ink`, twardy cień 5px `ink`, radius 12px; hover lekko unosi, kliknięcie wciska do zera); Sygnet / Pieczątka; pionowa kreska 3px przy metaforze.

**Zasady Logo:**
- **Pieczątka** (Sygnet z cieniem, −7°) = główna forma Logo na stronie — jedna, w marginesie, w zestawie z Logotypem pod spodem.
- Płaski prosty Sygnet — małe rozmiary (favicon, ikony).
- Sygnet nigdy na żółtym tle (znika).
- Zmiana samego Logo (obrót wszędzie) — nie teraz; ewentualnie osobno w przyszłości.

**Układ:** brak nagłówka strony; siatka: margines (Pieczątka + Logotyp + notka o pracy zdalnej + e-mail; na mobile w jednym rzędzie nad treścią) | kolumna listu ~40rem; bez kart — sekcje oddzielone linią włoskową i małym nagłówkiem Oxanium; usługi jako proza z pogrubionym tytułem; list kończy się podpisem (imię i nazwisko, „JSaurus, Almere”, e-mail) — bez powtórzonej Pieczątki i przycisku; cicha stopka z danymi firmy.

**Ruch:** przyciski wciskają się; Pieczątka wciska się po najechaniu (jedyny easter egg); **stopka cicha** — to zmienia ustalenie z „Charakter i ton marki” (ruchomy easter egg w stopce); animacja rozdrapania pazurami trafia na **stronę 404** („This page went extinct.”); żadnych animacji wejścia; `prefers-reduced-motion` respektowane.

**Tryb ciemny:** tylko jasny na start (koncepcja „list na papierze”); Sygnet działa na ciemnym, więc dodanie później nie dotyka Logo.
