# Setup

Pierwsze uruchomienie ProductBrain. Prowadzisz użytkownika przez 7 kroków.

Zasady prowadzenia:

- Prosty język. Użytkownik to product manager, niekoniecznie techniczny.
- **Jedno pytanie na raz**, czekaj na odpowiedź. Jeśli Twoje narzędzie ma pytania wielokrotnego wyboru - używaj ich przy pytaniach z opcjami.
- Na początku powiedz w 2-3 zdaniach, co się wydarzy i że potrwa to około 10 minut.
- Po każdym kroku jedno zdanie, co zostało zrobione.

Jeśli setup był już zrobiony (brak placeholderów w podwójnych klamrach w `AGENTS.md` i `tematy/o-mnie.md`, wpis `setup` w `log.md`) - zapytaj, co użytkownik chce zmienić: tryb, język, listę tematów czy profil, i wykonaj tylko ten krok.

## Krok 1 - poufność

Powiedz krótko: "Ten folder będzie zawierał informacje o Twojej firmie i ludziach. Zanim wrzucisz tu dokumenty firmowe, sprawdź, czy polityka firmy pozwala używać z nimi narzędzia AI, w którym teraz pracujemy." Zapytaj, czy jest to jasne, i idź dalej. Nie blokuj setupu.

## Krok 2 - język

Zapytaj: "Pracujemy po polsku czy po angielsku?"

- Polski - wpisz `polski` w `AGENTS.md`.
- Angielski - wpisz `angielski` i przetłumacz treść wszystkich plików `.md` (w tym `skills/`, `tematy/`, `README.md`, `AGENTS.md`). Nazwy folderów i plików zostają bez zmian, żeby odwołania działały. Nazwy sekcji w tematach tłumacz konsekwentnie we wszystkich plikach i skillach (np. "Co wiem" -> "What I know", "Kluczowe pytania" -> "Key questions", "Sprzeczności" -> "Contradictions", "Źródła" -> "Sources").

## Krok 3 - tryb i data startu

Zapytaj: "Zaczynasz nową pracę, czy chcesz zmapować to, co wiesz w obecnej?"

- **Nowa praca** - zapytaj o datę startu (już był albo dopiero będzie). Wpisz tryb `nowa praca` i datę `YYYY-MM-DD`.
- **Obecna praca** - zapytaj, od kiedy mniej więcej jest w firmie. Wpisz tryb `obecna praca` i datę (albo `nie dotyczy`).

## Krok 4 - tematy

Pokaż listę tematów z `AGENTS.md` (nazwa + jedno zdanie). Zapytaj: "To domyślne tematy. Chcesz coś dodać, usunąć albo zmienić?"

Podpowiedz typowe dodatki, jeśli pasują do roli: `technologia.md` (dla PM-a technicznego produktu), `dane-i-metryki.md`, `biznes-i-finanse.md`, `regulacje.md`, `procesy-sprzedazy.md`.

- Nowy temat: utwórz plik w `tematy/` w tym samym formacie co pozostałe (nagłówek, "Ostatnia aktualizacja: -", opis w jednym zdaniu, sekcje: Co wiem / Kluczowe pytania / Sprzeczności / Źródła) z 4-5 pytaniami startowymi, które ułożysz razem z użytkownikiem. Dopisz go do listy w `AGENTS.md`.
- Usunięty temat: usuń plik i pozycję z listy w `AGENTS.md`. `o-mnie.md` zostaje zawsze.
- Zapytaj też, czy w którymś temacie brakuje ważnego pytania - dopisz je.

## Krok 5 - o mnie

**Źródła profilu: tylko ten wywiad i materiał wklejony przez użytkownika.** Nie wypełniaj `o-mnie.md` z pamięci narzędzia, z wcześniejszych rozmów ani z innych plików na komputerze - mogą być nieaktualne, dotyczyć innego kontekstu albo zawierać rzeczy, których użytkownik nie chce tu mieć. Jeśli coś z pamięci wydaje się pasować, zapytaj wprost ("Pamiętam, że ... - wpisać to?") i wpisz dopiero po potwierdzeniu.

Najpierw zapytaj: "Masz pod ręką opis siebie - profil LinkedIn, CV, opis stanowiska? Wklej go albo wrzuć plik, wyciągnę z niego, co się da." To skraca wywiad.

Potem dla każdego niewypełnionego placeholdera w `tematy/o-mnie.md` zadaj pytanie z komentarza obok niego, jedno na raz. Możesz łączyć bliskie pytania. Jeśli użytkownik czegoś nie chce podać - wpisz "pominięte".

Wpisuj odpowiedzi zwięźle, pełnymi zdaniami, zastępując placeholder razem z komentarzem. Usuń zdanie o placeholderach z opisu na górze pliku. Ustaw "Ostatnia aktualizacja" na dzisiejszą datę, a w sekcji "Źródła" wpisz `setup YYYY-MM-DD (wywiad)` (plus "wklejony profil / CV", jeśli był).

Pokaż podsumowanie w 4-5 punktach i zapytaj, czy coś poprawić.

## Krok 6 - co wrzucić na start

Usuń z `AGENTS.md` akapit zaczynający się od "Jeśli w tym pliku albo w `tematy/o-mnie.md` są placeholdery". Sprawdź wyszukiwaniem, że w `AGENTS.md` i `tematy/` nie został żaden placeholder (wzorzec: wielkie litery w podwójnych klamrach).

Potem podpowiedz, co warto wrzucić do `inbox/` na początek (zależnie od trybu):

- dokumenty z onboardingu, opis stanowiska, oczekiwania przełożonego
- strategia, roadmapa, OKR-y, prezentacje dla zarządu
- schemat organizacyjny albo lista osób, z którymi będziesz pracować
- notatki z pierwszych spotkań i 1:1 (mogą być surowe, w punktach)
- opis produktu, dokumentacja, wyniki badań, dashboardy (jako zrzut albo opis)

Wyjaśnij, że format nie ma znaczenia: plik `.md`, `.txt`, `.pdf`, wklejony tekst, transkrypcja. Po wrzuceniu wystarczy napisać "review".

## Krok 7 - zapis

1. Dopisz do `log.md`: `YYYY-MM-DD - setup - <tryb>, start <data>, <język>, tematy: <zmiany albo "domyślne">`.
2. Pokaż ściągę:
   - nowy materiał -> wrzuć do `inbox/` i napisz "review"
   - "pokaż luki" -> czego jeszcze nie wiesz i kogo zapytać
   - "przygotuj kontekst" -> folder do podłączania w innych projektach AI
   - dowolne pytanie o firmę, produkt, ludzi
3. Jeśli użytkownik pracuje w Cowork - zaproponuj wpisanie w Instructions projektu zdania "Na początku każdej sesji przeczytaj AGENTS.md."
4. Zapytaj, czy ma już coś do wrzucenia - jeśli tak, od razu przejdź do `skills/review.md`.
