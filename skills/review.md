# Review

Przetwarza wszystko z `inbox/` i zapisuje wiedzę w plikach w `tematy/`. Pusty `inbox/` (poza `.gitkeep`) = nie ma nic do zrobienia - powiedz to i zaproponuj "pokaż luki".

Przed startem przeczytaj listę tematów w `AGENTS.md`. Jeśli plików w `inbox/` jest więcej niż 5 - zapytaj, czy przetwarzać wszystkie, czy zacząć od kilku najważniejszych.

## Dla każdego pliku w inbox/

1. **Przeczytaj go.** Jeśli to coś nieczytelnego (zły format, pusty plik) - powiedz to i pomiń.
2. **Pokaż wnioski.** 3-5 najważniejszych punktów, krótko. Przy każdym napisz, do którego tematu trafi. Jeden materiał może dotknąć kilku tematów.
3. **Zapytaj o decyzję**: zapisujemy, zapisujemy z poprawkami, czy odrzucamy? Przy oczywistych przypadkach (notatka z 1:1, dokument strategii) możesz zaproponować "zapisuję" i działać, chyba że użytkownik się sprzeciwi.
4. **Zapisz w tematach:**
   - dopisz fakty do sekcji "Co wiem" właściwych tematów, przy każdym odnośnik do źródła, np. `(archiwum/2026-10-14-1on1-anna.md)`
   - osoby zapisuj jako podsekcje `### Imię - rola` w odpowiednim temacie (przełożony, zespół, interesariusze); jeśli osoba już tam jest - dopisz do niej, nie twórz drugiej
   - odhacz w "Kluczowe pytania" te, na które padła odpowiedź: `- [x] pytanie -> "Co wiem" (archiwum/...)`; jeśli odpowiedź jest tylko częściowa - zostaw `- [ ]` i dopisz `(częściowo: ... - archiwum/...)`
   - dopisz nowe pytania, które wynikają z materiału (np. ktoś wspomniał o procesie, którego nie rozumiesz)
   - jeśli coś przeczy temu, co już zapisane - dopisz do sekcji "Sprzeczności" z oboma źródłami i powiedz to użytkownikowi wprost; to samo, gdy jedno źródło pokazuje rozjazd między deklaracją a praktyką (np. "roadmapę ustala zarząd, ale w praktyce sprzedaż dorzuca rzeczy co tydzień")
   - ustaw "Ostatnia aktualizacja" w każdym zmienionym temacie na dzisiejszą datę
   - nie przepisuj całego tematu od nowa; dopisuj i porządkuj, żeby sekcja "Co wiem" była czytelna (łącz powtórzenia, nowsze informacje nad starszymi, jeśli się zmieniły)
5. **Przenieś plik** do `archiwum/` jako `YYYY-MM-DD-krotki-opis.ext` (data materiału albo dzisiejsza). Jeśli materiał był wklejony w czat - zapisz go najpierw jako plik w `archiwum/`.
6. **Albo odrzuć.** Jeśli materiał nic nie wnosi - usuń go z `inbox/` po zgodzie użytkownika.
7. **Wpis w `log.md`**: `review` (które tematy, ile pytań zamkniętych) albo `reject` (co i dlaczego).

## Zasady zapisu

- **O ludziach - fakty i obserwacje, nie oceny.** Zamiast "jest trudna we współpracy" - "na dwóch spotkaniach zakwestionowała termin, prosi o dane przed decyzją". Jeśli użytkownik sam podaje ocenę - zapisz ją jako jego wrażenie ("moje wrażenie: ..."), nie jako fakt.
- **Bez źródła nie ma faktu.** Przypuszczenie użytkownika zapisuj jako pytanie albo z dopiskiem "do sprawdzenia".
- **Opinia to nie fakt.** Gdy ktoś mówi, jak jest (np. "klienci odchodzą, bo nie widzą wartości w pierwszym tygodniu") - zapisz to jako jego zdanie ("wg Marty: ..."), a jeśli to ważne, dopisz pytanie, jak to sprawdzić (dane, rozmowa z klientami).
- **Poufne szczegóły** (wynagrodzenia, sprawy osobiste, dane klientów) - nie zapisuj ich w tematach. Jeśli są w materiale, zapytaj, czy na pewno mają tu trafić.
- Krótko i konkretnie. Temat ma się czytać w 2-3 minuty.

## Na koniec

Podsumuj w 2-3 zdaniach: ile plików przetworzonych, które tematy urosły, ile pytań zamkniętych, czy pojawiły się sprzeczności. Jeśli w trybie "nowa praca" od ostatniego `gaps` w `log.md` minął ponad tydzień - zaproponuj "pokaż luki".
