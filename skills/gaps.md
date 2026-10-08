# Gaps - czego mi brakuje

Pokazuje 5 najważniejszych luk w wiedzy i podpowiada, jak je zamknąć. Celem są konkretne działania (pytanie na 1:1, spotkanie, dokument do znalezienia), nie raport.

## Krok 1 - zbierz stan

1. Z `AGENTS.md` odczytaj tryb i datę startu. W trybie "nowa praca" policz, który to dzień od startu.
2. Przeczytaj wszystkie pliki w `tematy/`. Dla każdego zanotuj:
   - liczbę otwartych pytań (`- [ ]`) i zamkniętych (`- [x]`)
   - czy sekcja "Co wiem" jest pusta albo bardzo cienka
   - datę "Ostatnia aktualizacja" (`-` = jeszcze nigdy)
   - nierozwiązane sprzeczności
3. Sprawdź `inbox/` - jeśli coś tam leży, powiedz, że najpierw warto zrobić review (luki mogą być już zamknięte w nieprzetworzonym materiale).

## Krok 2 - ustal priorytety

**Tryb "nowa praca"** - tematy ważą różnie zależnie od fazy:

| Faza | Najważniejsze tematy | Dlaczego |
|---|---|---|
| dni 0-30 | przełożony, zespół, rytuały, o mnie | najpierw relacje i to, jak tu się pracuje |
| dni 31-60 | produkt, użytkownicy, interesariusze | potem głębokie zrozumienie produktu i ludzi wokół |
| dni 61-90 | strategia, rynek | na końcu szerszy obraz, potrzebny do własnych propozycji |
| po 90 dniach | wszystkie równo | jak w trybie "obecna praca" |

Tematy dodane przez użytkownika w setupie przypisz do fazy, która najbardziej pasuje, i powiedz, jak je przypisałeś.

Luka z tematu z bieżącej fazy jest ważniejsza niż luka z późniejszej. Luka z wcześniejszej fazy, która nadal jest otwarta - najważniejsza (zaległość).

**Tryb "obecna praca"** - wszystkie tematy ważą równo. Priorytet mają tematy najsłabiej pokryte i te, które najbardziej wpływają na codzienne decyzje (zwykle: strategia, użytkownicy, przełożony).

W obu trybach podbij priorytet dla: nierozwiązanych sprzeczności, tematów nieaktualizowanych od ponad 2 tygodni (w trybie "nowa praca") albo 2 miesięcy (w trybie "obecna praca").

## Krok 3 - pokaż wynik

Najpierw jedno zdanie o stanie ("Dzień 24 z 90. Najlepiej pokryte: zespół i rytuały. Najsłabiej: przełożony i strategia.").

Potem **top 5 luk**, każda w formacie:

```
1. <pytanie albo brak> (temat)
   Dlaczego teraz: <jedno zdanie>
   Jak zamknąć: <kogo zapytać / jakie spotkanie umówić / jaki dokument znaleźć>
```

"Jak zamknąć" ma być konkretne: jeśli w tematach jest osoba, która może znać odpowiedź - podaj ją z imienia. Jeśli pasuje kilka luk do jednej rozmowy - zgrupuj je ("na 1:1 z przełożonym zapytaj o 1 i 3").

Na koniec, jeśli dotyczy:

- sprzeczności do wyjaśnienia (krótko, z tematem)
- tematy, które dawno nie były aktualizowane
- jeśli istnieje `product-context/` (ścieżka w `AGENTS.md`), a jego "stan na" jest starszy niż ostatni wpis `review` w `log.md` - przypomnij o "przygotuj kontekst"

## Krok 4 - zapis

1. Zapytaj, czy dopisać do tematów nowe pytania, które wyszły przy analizie (np. brak, którego nie było jeszcze na liście).
2. Dopisz do `log.md`: `YYYY-MM-DD - gaps - <dzień X z 90 albo "obecna praca">, top luki: <3-5 słów na lukę>`.

Nie zapisuj pełnego wyniku w osobnym pliku - za tydzień i tak będzie nieaktualny. Wystarczy wpis w logu.
