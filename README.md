# ProductBrain

Mapa wiedzy o Twojej firmie, produkcie i ludziach, którą budujesz razem z AI. Najbardziej przydaje się w pierwszych 90 dniach w nowej pracy, ale działa też, jeśli jesteś w firmie od lat i chcesz sprawdzić, co naprawdę wiesz.

## Jak to działa

```
inbox/  ->  review  ->  tematy/  ->  gaps (czego mi brakuje?)
                           |
                           +-> kontekst -> product-context/ (podłączasz do innych projektów AI)
```

1. **Wrzucasz** do `inbox/` wszystko, czego się dowiadujesz: notatki z 1:1, transkrypcje spotkań, dokumenty firmowe, własne przemyślenia. Bez porządkowania - może być surowa notatka.
2. **Mówisz "review".** Agent czyta materiał, pokazuje najważniejsze wnioski i rozpisuje je na tematy: przełożony, zespół, interesariusze, strategia, produkt, użytkownicy, rynek, rytuały, Ty. Odhacza pytania, na które padła odpowiedź, i wyłapuje sprzeczności.
3. **Mówisz "pokaż luki".** Agent pokazuje 5 najważniejszych rzeczy, których jeszcze nie wiesz, i podpowiada, kogo zapytać albo jakie spotkanie umówić.
4. **Mówisz "przygotuj kontekst".** Agent składa z tematów krótki folder `product-context/` - opis Ciebie, firmy, produktu i sposobu pracy. Podłączasz go do innych projektów w Cowork, Cursorze, Claude Code czy Claude Projects, żeby AI w codziennej pracy znało realia Twojej firmy.

Możesz też po prostu pytać: "jak tu się ustala priorytety?", "przygotuj mnie do 1:1 z przełożonym".

## Start

1. Pobierz i rozpakuj folder `ProductBrain`.
2. Otwórz go w swoim narzędziu (instrukcje niżej).
3. Napisz do agenta:

```
Przeczytaj AGENTS.md i zrób setup.
```

Setup trwa około 10 minut: wybierzesz tryb (nowa albo obecna praca), dostosujesz listę tematów i krótko opowiesz o sobie.

### Claude Cowork

W aplikacji Claude przejdź do Cowork -> Projects -> "+" -> "Use an existing folder" i wskaż folder `ProductBrain`. Potem w nowej sesji napisz zdanie startowe.

Wskazówka: w polu Instructions projektu wpisz "Na początku każdej sesji przeczytaj AGENTS.md." - wtedy polecenia "review", "pokaż luki" i "przygotuj kontekst" zadziałają w każdej sesji.

### Claude Code

```
cd ProductBrain
claude
```

Potem zdanie startowe albo `/setup`.

### Cursor

File -> Open Folder -> `ProductBrain`. W czacie agenta zdanie startowe albo `/setup`.

### Codex

```
cd ProductBrain
codex
```

Potem zdanie startowe albo `$setup`.

## Polecenia

| Mówisz | Co się dzieje |
|---|---|
| "review" | agent przetwarza wszystko z `inbox/` |
| "pokaż luki" | 5 najważniejszych luk + kogo zapytać |
| "przygotuj kontekst" | nowa wersja `product-context/` |
| dowolne pytanie | odpowiedź na bazie Twoich tematów |

W Claude Code, Cursorze i Cowork działają też `/inbox-review`, `/gaps`, `/kontekst`, a w Codexie `$inbox-review`, `$gaps`, `$kontekst`. Komenda nazywa się `inbox-review`, bo `/review` jest w tych narzędziach zajęte przez wbudowane code review - samo słowo "review" w zwykłej wiadomości działa normalnie.

## Jak podłączyć product-context/ do innych projektów

`product-context/` powstaje domyślnie obok folderu `ProductBrain`, żeby podłączając go, nie podłączyć przy okazji wszystkich notatek.

- **Cowork** - w ustawieniach projektu, w sekcji Context, dodaj folder `product-context`.
- **Cursor** - File -> Add Folder to Workspace, albo wskaż plik w czacie przez `@`.
- **Claude Code** - `claude --add-dir ../product-context`, albo w `CLAUDE.md` innego projektu dodaj linię `@../product-context/README.md`.
- **Codex** - poproś agenta: "przeczytaj ../product-context/README.md i używaj go jako kontekstu".
- **Claude Projects / Custom GPT / Gemini Gem** - wgraj pliki z `product-context/` jako wiedzę projektu (albo wklej wersję Mini do instrukcji).

Kontekst się nie edytuje ręcznie. Gdy coś się zmieni - zrób review nowych materiałów i powiedz "przygotuj kontekst" jeszcze raz.

## Poufność - przeczytaj przed startem

Ten folder będzie zawierał informacje o Twojej firmie i notatki o ludziach, z którymi pracujesz.

- Sprawdź, jakich narzędzi AI wolno Ci używać z danymi firmy. Jeśli polityka firmy na to nie pozwala - nie wrzucaj tu dokumentów firmowych.
- Nie publikuj tego folderu (np. w publicznym repozytorium) i nie udostępniaj go.
- O ludziach zapisuj fakty i obserwacje, nie oceny. Agent pilnuje tego przy review.

## Co dalej - ProductOS

Gdy onboarding się skończy, a chcesz dalej budować wiedzę i prowadzić projekty z AI, możesz przejść na ProductOS. Jego setup potrafi wczytać Twój `product-context/` (żeby nie odpowiadać drugi raz na te same pytania) i zaimportować tematy z ProductBrain jako materiał do wiki.
