# Kontakt na stronie statycznej — opcje

Type: research
Status: resolved
Blocked by:

## Question

Jakie są realne sposoby przyjmowania kontaktu od potencjalnych klientów na statycznej stronie (bez własnego backendu), serwowanej z VPS, dla firmy w NL (RODO/GDPR)? Porównać: `mailto:` (obecnie `hello@jsaur.us`, poczta na iCloud), usługi formularzy (np. Formspree, Web3Forms, Basin, Netlify-like alternatywy), umawianie rozmowy (Cal.com, Calendly, TidyCal) — pod kątem: kosztu (darmowy próg), ochrony przed spamem (bez CAPTCHA wymagającej zgody cookies, jeśli się da), zgodności z RODO i lokalizacji danych (UE), wymaganego JS, możliwości działania bez zewnętrznej usługi. Zebrać fakty do decyzji podejmowanej w ticketcie o strukturze strony.

## Comments

- Research w toku: gałąź `research/kontakt`, plik `.scratch/jsaurus-redesign/research/04-kontakt.md`.

## Answer

Pełne ustalenia ze źródłami i tabelą porównawczą: gałąź `research/kontakt` (commit `0c7ba57`), plik `.scratch/jsaurus-redesign/research/04-kontakt.md` (`git show research/kontakt:.scratch/jsaurus-redesign/research/04-kontakt.md`).

Fakty kluczowe dla decyzji:

- **`mailto:`** — zero kosztu, JS i podmiotów przetwarzających; adres i tak jest publiczny (zbierany przez boty). Obfuskacja Cloudflare nie działa przy serwowaniu z VPS.
- **Usługi formularzy z USA** — Formspree (50/mies. free, od $10/mies., DPA nieopublikowane), Web3Forms (250/mies. free, brak DPA, sprzeczne deklaracje o przechowywaniu — odradzane). Basin (Kanada, adekwatność UE, DPA w regulaminie; 50/mies., 1 formularz free). Getform → dziś **Forminit**.
- **Opcja UE: Formward** (Szwecja, 2025) — dane i subprocesorzy w UE, DPA w panelu, czysty HTML POST, honeypot + rate-limit bez CAPTCHA, 100/mies. free.
- **Umawianie rozmów** — hostowane opcje trzymają dane w USA; Cal.eu wyłączane 1.11.2026; self-host Cal.com (dziś `cal.diy`) autorzy polecają tylko niekomercyjnie; TidyCal $29 jednorazowo; osadzony Calendly wnosi własny baner cookies → ewentualnie tylko jako link.
- **Antyspam bez banera cookies**: honeypot + filtr po stronie serwera; reCAPTCHA stawia cookie, Turnstile/hCaptcha to zewnętrzny JS.
- **Własny endpoint na VPS** — możliwy, ale oznacza utrzymanie i wysyłkę maili (SMTP iCloud z hasłem aplikacji lub zewnętrzny dostawca) oraz odejście od czystej statyki.

Rekomendacja researchu (decyzja zapada w ticketcie „Struktura strony i przekaz”): `mailto:` jako główny kanał + opcjonalnie formularz w czystym HTML z honeypotem na Formward; rozmowa tylko jako link; unikać Web3Forms i reCAPTCHA.

Niezweryfikowane: DPA Formspree, lokalizacja danych Forminit, dosłowne brzmienie EUR-Lex / EDPB 2/2023.
