# Struktura strony i przekaz

Type: grilling
Status: resolved
Blocked by: 01, 04, 09

## Question

Jaka jest struktura informacji nowej strony: one-pager czy podstrony, jakie sekcje w jakiej kolejności, co mówi każda z nich (przekaz + szkic treści w EN), i jak odbywa się kontakt (wybór spośród opcji z ticketu „Kontakt na stronie statycznej — opcje”)? Uwzględnić gotowość na NL/PL i to, że blog jest poza zakresem. Wejście z ticketu „Dla kogo jest strona i co oferujesz”: strona uwiarygadnia, mówi tylko do Klienta (bez sekcji dla agencji), eksponuje usługi w ustalonej kolejności (Modernizacja pierwsza), bez cen, główne działanie to wiadomość + opcjonalny link do rozmowy. Wejście z „Dowody wiarygodności”: które dowody i gdzie je pokazać. Wejście z „Język wizualny”: strona nie ma nagłówka — Pieczątka, Logotyp i e-mail stoją w marginesie obok listu; jeśli struktura wymaga podstron, nawigacja musi zmieścić się w tym marginesie (albo trzeba wrócić do decyzji o nagłówku). Strona 404 istnieje (animacja pazurów, „This page went extinct.”). Wejście z „Dowody wiarygodności”: dwa ogólne akapity o doświadczeniu, liczby „15+ / 10+ years”, trzy zasady „How I work” (do umiejscowienia), zdjęcie przy „Who you'll work with”, stopka prawna z adresem, KvK, btw-id i e-mailem.

## Answer

Rozstrzygnięte w grillingu z właścicielem (2026-10-16). Wszystkie rekomendacje i szkic treści przyjęte.

### Strony

- **`/`** — jeden list; bez podstron usług / about / contact, bez nawigacji (zgodnie z brakiem nagłówka).
- **`/privacy`** — krótkie oświadczenie o prywatności (RODO: przetwarzanie danych z maili); link w stopce.
- **404** — „This page went extinct.” + animacja pazurów (`ClawScratch`) + link do strony głównej.
- Ścieżki gotowe na `/nl/…` i `/pl/…` bez zmiany angielskich adresów (patrz „Architektura i18n pod EN / NL / PL”).

### Kontakt

Tylko **`mailto:hello@jsaur.us`**: główny przycisk-naklejka „Write to me” + widoczny adres do skopiowania obok. Bez formularza i bez linku do kalendarza na start (obie rzeczy da się dodać później bez zmiany struktury). Obietnica odpowiedzi „within one working day” potwierdzona przez właściciela.

### Analityka

**Brak** na start. Jeśli kiedyś — tylko bezciasteczkowa, self-hosted na VPS (np. Umami/Plausible), opisana w `/privacy`. Nigdy Google Analytics.

### Układ `/`

```
margines                 │ list
─────────────────────────┼──────────────────────────────────────────
Pieczątka + jsaurus      │ Hi, I'm Paul. / hasło / podtytuł
notka o pracy zdalnej    │ [Write to me]  hello@jsaur.us
hello@jsaur.us           │ What I do
                         │ Who you'll work with (zdjęcie + bio + dowody)
                         │ How I work (3 zasady + zachęta do kontaktu)
                         │ Podpis
─────────────────────────┴──────────────────────────────────────────
stopka: dane prawne | Privacy
```

Dowody nie mają osobnej sekcji — są w „Who you'll work with”. „How I work” tuż przed podpisem, bo prowadzi do kontaktu.

### Szkic treści (EN) — kierunek; finalne szlify przy implementacji

**Meta**
- title: `JSaurus — web development for companies without an IT team`
- description: `JSaurus is Paweł (Paul) Józefowski — a web developer who builds, modernises and maintains web systems for companies without their own IT team.`

**Margines**
> Based in Almere. Working remotely across the Netherlands, Poland and the EU.
> hello@jsaur.us

**Otwarcie**
> Hi, I'm Paul.
> # Your company's developer — without hiring one.
> *I bring old web systems back to life — and build new ones that last.*
> **[Write to me]** or write to hello@jsaur.us

**What I do**
> **Modernisation.** Your old system keeps running while I build its replacement. Many companies depend on a web system that nobody wants to touch anymore. I take it over, keep it working, and move it step by step to technology that will last another ten years.
> ▎*Legacy doesn't have to mean extinct.*
>
> **Web applications.** Custom tools built around how your company actually works — not the other way round.
> **Company websites.** Fast, clear websites you can update yourself.
> **Care & maintenance.** Updates, fixes and small improvements, so your system stays healthy without the drama.
> Also: connecting your systems with each other, and honest technical advice when you need a second opinion.

**Who you'll work with**
> [photo]
> I've built for the web for more than 15 years — from early JavaScript to today's frameworks, on both the front end and the back end. You'll talk to me, not to a sales team.
> Since 2015 I've kept a business-critical platform for a company in the advertising industry running — and growing. More than ten years with one client taught me that good software is mostly about being there when it matters.
> I also build company websites for businesses from food production to small creative studios.
> If you need a 20-person team, I'm not your guy — I'll tell you who is.

**How I work**
> - The first conversation is free and without obligation.
> - You get a fixed quote before any work starts.
> - You own the code and everything I build for you.
>
> Tell me what's slowing your company down. I usually reply within one working day.

**Podpis**
> **Paweł Józefowski** / JSaurus, Almere / hello@jsaur.us

**Stopka**
> JSaurus, Paweł Józefowski | Randstad 22/46, 1316BZ Almere | KvK 88270793 | btw-id … | hello@jsaur.us | Privacy

**404**
> # This page went extinct.
> The page you were looking for doesn't exist anymore — or never did. [Back to the start]

### `/privacy` — zawartość

- Administrator: JSaurus (Paweł Józefowski), adres i e-mail jak w stopce.
- Dane: tylko to, co ktoś sam przyśle mailem (imię, adres e-mail, treść wiadomości).
- Cel i podstawa: odpowiedź i przygotowanie wyceny (działania przed zawarciem umowy / prawnie uzasadniony interes).
- Okres: przez czas rozmowy; u Klientów — 7 lat (holenderski obowiązek przechowywania dokumentów podatkowych).
- Podmioty przetwarzające: Apple (poczta iCloud dla `jsaur.us`); hosting strony na własnym VPS u **Hetzner w Niemczech**.
- Strona: bez ciasteczek, bez analityki, bez zewnętrznych zasobów (fonty hostowane lokalnie).
- Prawa: dostęp, sprostowanie, usunięcie, sprzeciw; skarga do Autoriteit Persoonsgegevens.
