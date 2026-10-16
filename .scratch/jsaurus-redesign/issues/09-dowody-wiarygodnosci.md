# Dowody wiarygodności

Type: grilling
Status: resolved
Blocked by:

## Question

Skoro główną rolą strony jest uwiarygadnianie (patrz „Dla kogo jest strona i co oferujesz”), czym konkretnie JSaurus to udowadnia? Co istnieje i co wolno pokazać: nazwy/logotypy Klientów (zgody?), opisy projektów lub case studies (także zanonimizowane — np. wieloletnia Modernizacja i rozwój systemu dla firmy medialnej), opinie/rekomendacje, lata współpracy i liczby, profil LinkedIn/GitHub, dane rejestrowe (KvK), zdjęcie i bio właściciela (imię: „Paul” w EN/NL, „Paweł” w PL, pełne „Paweł Józefowski” tam, gdzie liczy się wiarygodność — z „Charakter i ton marki”). Co przy projektach objętych NDA lub white-label? Wynik: lista dowodów do użycia na stronie z ich źródłem i statusem zgody.

## Answer

Rozstrzygnięte w grillingu z właścicielem (2026-10-16).

**Nie pokazujemy (na razie):** nazw klientów i projektów, logotypów, linków do realizacji, rekomendacji, profili LinkedIn i GitHub (publiczny GitHub jest prawie pusty). Projekty white-label i objęte NDA nie pojawiają się nawet anonimowo.

**Pokazujemy:**

1. **Dwa ogólne akapity prozą** (bez nazw; „advertising industry” zamiast „OOH”, bo to mniej identyfikujące):
   - *„Since 2015 I've kept a business-critical platform for a company in the advertising industry running — and growing.”*
   - *„Company websites for businesses from food production to small creative studios.”*
2. **Dwie liczby w treści:** „15+ years” i „10+ years with one client”.
3. **Zasady współpracy („How I work”)** — dowód przez przejrzystość, potwierdzone przez właściciela:
   - *„The first conversation is free and without obligation.”*
   - *„You get a fixed quote before any work starts.”*
   - *„You own the code and everything I build for you.”*
   Miejsce na stronie ustala „Struktura strony i przekaz”.
4. **Zdjęcie:** jedno prawdziwe, przy sekcji „Who you'll work with”. Do tego czasu w repo neutralny placeholder (ramka 4:5, podpis „photo”); na dev lokalny stockowy portret w `src/assets/dev-only/` (w `.gitignore`, nigdy nie commitowany — nieznana licencja, publiczne repo, ryzyko cudzej twarzy na produkcji).
5. **Stopka prawna** (wymóg NL, dostępna z każdej strony, max jedno kliknięcie): JSaurus, Paweł Józefowski · Randstad 22/46, 1316BZ Almere (adres biurowy) · KvK 88270793 · btw-id (uzupełnić przy implementacji) · `hello@jsaur.us`. **Bez telefonu** — e-mail spełnia wymóg „danych do szybkiego kontaktu”.

Źródła wymogów stopki:
- [Ondernemersplein — regels voor bedrijfscorrespondentie](https://ondernemersplein.overheid.nl/wetten-en-regels/regels-voor-bedrijfscorrespondentie/): na stronie nazwa, bezoekadres (chyba że zastrzeżony w Handelsregister), e-mail i telefon; przy usługach online także KvK i btw-id.
- [Art. 3:15d BW (komentarz SDU)](https://www.sdu.nl/content/commentaar-op-burgerlijk-wetboek-boek-3-art-15d-vermogensrecht): tożsamość, adres siedziby, dane do szybkiego kontaktu łącznie z e-mailem, numer rejestru.
- [ACM — bedrijfsgegevens vermelden](https://www.acm.nl/nl/verkoop-aan-consumenten/consumenten-informeren/bedrijfsgegevens-vermelden): ACM egzekwuje łatwą dostępność tych danych.

Uwaga: Ondernemersplein wymienia telefon, ustawa wymaga „danych do szybkiego kontaktu, w tym e-maila” — przyjęto interpretację, że sam e-mail wystarcza.
