# ProductBrain - instrukcja dla agenta

Ten plik czytasz na początku każdej sesji. Działa w Cowork, Claude Code (przez `CLAUDE.md`), Cursorze i Codexie.

**Jeśli w tym pliku albo w `tematy/o-mnie.md` są placeholdery w podwójnych klamrach (np. `{{TRYB}}`), vault nie przeszedł setupu.** Zanim zrobisz cokolwiek innego, zaproponuj setup: przeczytaj `skills/setup.md` i postępuj według niego.

## Czym jest ten vault

Mapa wiedzy product managera o jego firmie, produkcie i ludziach, budowana razem z agentem. Użytkownik wrzuca materiały do `inbox/`, agent przetwarza je w review i zapisuje wiedzę w plikach tematów. Skill `gaps` pokazuje, czego jeszcze brakuje, a skill `kontekst` składa z tematów przenośny folder `product-context/` do podłączania w innych projektach AI.

## Ustawienia (wypełnia setup)

- Tryb: {{TRYB}} <!-- "nowa praca" (onboarding, priorytety według dni od startu) albo "obecna praca" (bez faz) -->
- Data startu w firmie: {{DATA_STARTU}} <!-- YYYY-MM-DD; w trybie "obecna praca" - przybliżona albo "nie dotyczy" -->
- Język: {{JĘZYK}} <!-- polski albo angielski -->
- Ścieżka do product-context: `../product-context/` (domyślnie obok vaulta; skill `kontekst` pyta o nią przy pierwszym uruchomieniu i tu ją aktualizuje)

## Struktura

- `inbox/` - wszystko nowe: notatki z 1:1, transkrypcje spotkań, dokumenty firmowe, zrzuty ze Slacka, własne przemyślenia. Coś leży = jest do przetworzenia.
- `tematy/` - jeden plik na temat, żywe dokumenty pisane przez agenta (lista niżej).
- `archiwum/` - materiały po review, nazwane `YYYY-MM-DD-opis.md`. Nie edytujesz ich po przeniesieniu.
- `skills/` - procedury: `setup.md`, `review.md`, `gaps.md`, `kontekst.md`. To jedyne miejsce z pełnym opisem kroków.
- `log.md` - historia: setup, review, reject, gaps, kontekst.

## Tematy

Lista ustawiana w setupie. Dodając albo usuwając temat, zaktualizuj tę listę.

- `tematy/o-mnie.md` - mój styl, kontekst i sposób pracy
- `tematy/przelozony.md` - przełożony: oczekiwania, styl, jak mierzy sukces
- `tematy/zespol.md` - mój zespół: ludzie, role, mocne strony, dynamika
- `tematy/interesariusze.md` - kto poza zespołem wpływa na produkt i czego chce
- `tematy/strategia.md` - strategia firmy i produktu, cele, zakłady
- `tematy/produkt.md` - co robi produkt, jak działa, metryki, dług
- `tematy/uzytkownicy.md` - użytkownicy i klienci: segmenty, problemy, wiedza z badań
- `tematy/rynek.md` - konkurencja, trendy, pozycja firmy
- `tematy/rytualy.md` - jak tu się pracuje: strategia, priorytety, współpraca z zespołem, spotkania cykliczne

## Polecenia

Użytkownik może wywołać skill przez `/nazwa` (Claude Code, Cursor), `$nazwa` (Codex) albo słowami. Rozpoznawaj słowa:

- "setup", "skonfiguruj" -> `skills/setup.md`
- "review", "inbox-review", "przetwórz inbox", "wrzuciłem notatkę" -> `skills/review.md` (komenda nazywa się `inbox-review`, bo `/review` jest w wielu narzędziach wbudowane - jeśli użytkownik napisze samo "review", chodzi o tę procedurę, nie o code review)
- "luki", "czego mi brakuje", "gaps", "co dalej" -> `skills/gaps.md`
- "kontekst", "przygotuj kontekst", "zrób product context" -> `skills/kontekst.md`

Zawsze przeczytaj odpowiedni plik w `skills/` przed wykonaniem procedury.

**Pytania o firmę, produkt, ludzi** (np. "jak tu się ustala priorytety?", "przygotuj mnie do 1:1 z przełożonym") - odpowiadaj na bazie plików w `tematy/`, z odnośnikiem do tematu. Jeśli tematy nie mają odpowiedzi - powiedz to wprost i zaproponuj dopisanie pytania do sekcji "Kluczowe pytania" właściwego tematu.

## Zasady

1. **Wrzucaj szeroko, odsiewaj przy review.** Do `inbox/` trafia wszystko, co może się przydać - koszt jest zerowy. Selekcja dzieje się przy review.
2. **O ludziach - fakty i obserwacje, nie oceny.** "Na spotkaniu dwa razy wrócił do terminu Q2" zamiast "jest nerwowy". Te notatki mogą kiedyś zobaczyć inne osoby.
3. **Zawsze źródło.** Każdy fakt w temacie ma odnośnik do pliku w `archiwum/`. Wiedza bez źródła to przypuszczenie - zapisuj ją jako pytanie, nie fakt.
4. **Sprzeczności się zapisuje, nie rozstrzyga po cichu.** Jeśli dwa źródła mówią co innego - sekcja "Sprzeczności" w temacie.
5. **`product-context/` tylko się regeneruje.** Poprawki wprowadzasz w tematach, potem skill `kontekst` ponownie.
6. **Poufność.** Vault zawiera informacje o firmie i ludziach. Nie proponuj wysyłania go dalej ani publikowania.

## Styl pisania

- "-" zamiast długiego myślnika
- prosty, konkretny język, pełne zdania
- bez dramatyzowania i zdań kontrastowych w stylu "To nie X. To Y."
- własne preferencje użytkownika - `tematy/o-mnie.md`, sekcja "Jak piszę"
