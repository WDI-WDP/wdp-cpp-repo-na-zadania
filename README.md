# Wprowadzenie do programowania z wykorzystaniem języka C++

Repozytorium jest przeznaczone do pracy podczas kursu **„Wprowadzenie do programowania z wykorzystaniem języka C++”**.

Służy ono do:

* przechowywania rozwiązań zadań wykonywanych podczas zajęć,
* przechowywania zadań wykonywanych samodzielnie,
* tworzenia własnych notatek,
* śledzenia historii zmian za pomocą systemu kontroli wersji Git,
* przekazywania rozwiązań do sprawdzenia za pomocą GitHub Classroom.

## Materiały do kursu

Podstawowym materiałem wykorzystywanym podczas zajęć jest prezentacja:

**[Prezentacja – Wprowadzenie do programowania z wykorzystaniem języka C++](https://wdi-wdp.github.io/prezentacja-cpp/#/0/0)**

Prezentacja zawiera materiał omawiany podczas kolejnych lekcji, przykłady oraz treści zadań.

---

# Struktura repozytorium

Repozytorium jest podzielone na katalogi odpowiadające kolejnym lekcjom.

Przykładowa struktura pojedynczej lekcji:

```text
04-Lekcja/
├── 00-Notatki-wlasne/
├── 01-Zadanie/
├── 02-Zadanie/
└── 03-Zadanie/
```

Numer lekcji odpowiada numerowi materiału omawianego podczas zajęć.

Wewnątrz katalogu lekcji znajdują się:

* `00-Notatki-wlasne/` – miejsce na własne notatki, przykłady lub dodatkowy kod,
* `01-Zadanie/` – rozwiązanie pierwszego zadania,
* `02-Zadanie/` – rozwiązanie drugiego zadania,
* `03-Zadanie/` – rozwiązanie trzeciego zadania,
* kolejne katalogi z zadaniami, jeżeli dana lekcja zawiera ich więcej.

Liczba zadań może różnić się pomiędzy lekcjami.

Nie należy zmieniać nazw ani numeracji istniejących katalogów.

---

# Rozwiązywanie zadań

Każde zadanie powinno zostać rozwiązane w **odpowiadającym mu katalogu**.

Przykładowo rozwiązanie pierwszego zadania z lekcji 4 powinno znajdować się w:

```text
04-Lekcja/01-Zadanie/
```

## Minimalna struktura rozwiązania

Najprostszym sposobem zapisania rozwiązania jest umieszczenie pliku:

```text
main.cpp
```

bezpośrednio w katalogu zadania.

Przykład:

```text
04-Lekcja/
└── 01-Zadanie/
    └── main.cpp
```

Plik `main.cpp` powinien zawierać kod źródłowy programu rozwiązującego dane zadanie.

Jeżeli zadanie wymaga dodatkowych plików, mogą one znajdować się w tym samym katalogu.

Przykład:

```text
04-Lekcja/
└── 03-Zadanie/
    ├── main.cpp
    ├── dane.txt
    └── wynik.txt
```

---

# Korzystanie z IDE

Do rozwiązywania zadań można używać dowolnego środowiska programistycznego obsługującego język C++, np.:

* Visual Studio Code,
* CLion,
* Code::Blocks,
* Visual Studio,
* innego edytora lub IDE wybranego przez studenta.

## Pojedynczy plik `main.cpp`

Preferowaną i najprostszą strukturą rozwiązania jest umieszczenie pliku `main.cpp` bezpośrednio w katalogu zadania:

```text
04-Lekcja/
└── 01-Zadanie/
    └── main.cpp
```

## Cały projekt IDE

Dopuszczalne jest również utworzenie całego projektu IDE wewnątrz katalogu konkretnego zadania.

Przykładowo projekt CLion może wyglądać następująco:

```text
04-Lekcja/
└── 01-Zadanie/
    ├── CMakeLists.txt
    └── main.cpp
```

Projekt Code::Blocks może wyglądać przykładowo:

```text
04-Lekcja/
└── 01-Zadanie/
    ├── Zadanie.cbp
    └── main.cpp
```

Najważniejsze jest, aby **cały projekt dotyczący danego zadania znajdował się we właściwym katalogu zadania** oraz aby możliwe było łatwe odnalezienie kodu źródłowego programu.

Nie należy tworzyć jednego wspólnego projektu obejmującego rozwiązania wielu niezależnych zadań, chyba że prowadzący wyraźnie zaznaczy inaczej.

---

# Pliki generowane przez kompilator i IDE

Do repozytorium należy dodawać przede wszystkim **kod źródłowy oraz pliki potrzebne do zbudowania projektu**.

Nie należy umieszczać w repozytorium plików generowanych automatycznie podczas kompilacji, takich jak:

```text
*.exe
*.o
*.obj
```

oraz katalogów zawierających wyniki kompilacji, np.:

```text
build/
cmake-build-debug/
cmake-build-release/
bin/
obj/
```

Pliki te mogą być generowane ponownie na podstawie kodu źródłowego i nie stanowią rozwiązania zadania.

Jeżeli korzystasz z projektu utworzonego przez IDE, możesz umieścić w repozytorium pliki opisujące projekt, np.:

```text
CMakeLists.txt
*.cbp
*.sln
*.vcxproj
```

Nie ma natomiast potrzeby przesyłania plików tymczasowych, pamięci podręcznej IDE ani skompilowanych programów.

W repozytorium znajduje się plik `.gitignore`, który standardowo wyklucza z kontroli wersji typowe pliki generowane przez kompilator, IDE oraz system operacyjny. W zależności od używanego środowiska pliki te mogą być wizualnie oznaczone jako ignorowane — przykładowo w Visual Studio Code są zazwyczaj wyświetlane na szaro i nie są uwzględniane przy dodawaniu zmian do commita.


---

# Własne notatki

Każda lekcja zawiera katalog:

```text
00-Notatki-wlasne/
```

Można w nim umieszczać między innymi:

* notatki w formacie `.md` lub `.txt`,
* własne przykłady kodu,
* eksperymenty wykonywane podczas zajęć,
* fragmenty kodu pomagające zrozumieć omawiane zagadnienia.

Przykład:

```text
04-Lekcja/
└── 00-Notatki-wlasne/
    ├── notatki.md
    └── przyklad.cpp
```

Zawartość tego katalogu nie musi stanowić kompletnego rozwiązania konkretnego zadania.

---

# Przygotowanie rozwiązania do sprawdzenia

Przed zakończeniem pracy należy upewnić się, że:

* rozwiązanie znajduje się w katalogu właściwego zadania,
* kod źródłowy został zapisany,
* program można skompilować,
* program został przetestowany dla przykładowych danych,
* wszystkie potrzebne pliki zostały dodane do repozytorium,
* zmiany zostały zatwierdzone za pomocą `git commit`,
* commity zostały wysłane do GitHuba za pomocą `git push`.

Samo zapisanie pliku na komputerze **nie powoduje przesłania rozwiązania do GitHuba**.

Samo wykonanie `git commit` również nie wystarcza – commit jest wtedy zapisany jedynie w lokalnym repozytorium.

Rozwiązanie znajdujące się na komputerze należy jeszcze wysłać do zdalnego repozytorium GitHub za pomocą `git push`.

---

# Kontrola wersji – Git i GitHub

**Git** jest systemem kontroli wersji pozwalającym zapisywać kolejne wersje projektu.

**GitHub** jest usługą przechowującą zdalną kopię repozytorium Git.

Podczas pracy wykorzystywane są więc dwa repozytoria:

* **repozytorium lokalne** – znajdujące się na komputerze,
* **repozytorium zdalne** – znajdujące się na GitHubie.

Najczęstszy schemat pracy wygląda następująco:

```text
edycja plików
     ↓
git add
     ↓
git commit
     ↓
git push
     ↓
GitHub
```

---

## Pobranie repozytorium

Po otrzymaniu repozytorium poprzez GitHub Classroom można pobrać je na komputer za pomocą:

```bash
git clone <adres-repozytorium>
```

Następnie należy przejść do pobranego katalogu:

```bash
cd <nazwa-repozytorium>
```

Jeżeli repozytorium zostało już otwarte np. poprzez GitHub Codespaces albo funkcję klonowania dostępną bezpośrednio w IDE, ręczne wykonywanie `git clone` nie jest potrzebne.

---

## Sprawdzanie zmian

Do sprawdzania aktualnego stanu repozytorium służy:

```bash
git status
```

Polecenie pokazuje między innymi:

* zmodyfikowane pliki,
* nowe pliki,
* zmiany przygotowane do commita,
* zmiany nieprzygotowane do commita,
* stan lokalnej gałęzi względem repozytorium zdalnego.

Przykład:

```text
/workspaces/repo-name (main) $ git status

On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)

        modified:   04-Lekcja/01-Zadanie/main.cpp

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        04-Lekcja/00-Notatki-wlasne/notatki.md

no changes added to commit
```

W powyższym przykładzie:

```text
modified: 04-Lekcja/01-Zadanie/main.cpp
```

oznacza, że plik był już wcześniej śledzony przez Git, ale został zmodyfikowany od czasu ostatniego commita.

Natomiast:

```text
Untracked files
```

oznacza nowe pliki, które nie były wcześniej śledzone przez Git.

W przykładzie jest to:

```text
04-Lekcja/00-Notatki-wlasne/notatki.md
```

---

## Przygotowanie zmian do commita – `git add`

Przed utworzeniem commita należy wskazać, które zmiany mają się w nim znaleźć.

Służy do tego polecenie:

```bash
git add
```

Przykładowo, aby przygotować konkretny plik:

```bash
git add 04-Lekcja/01-Zadanie/main.cpp
```

Można również przygotować wszystkie zmiany znajdujące się w bieżącym katalogu i jego podkatalogach:

```bash
git add .
```

Po wykonaniu:

```bash
git add .
```

ponowne wywołanie:

```bash
git status
```

może zwrócić:

```text
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)

        modified:   04-Lekcja/01-Zadanie/main.cpp
        new file:   04-Lekcja/00-Notatki-wlasne/notatki.md
```

Sekcja:

```text
Changes to be committed
```

oznacza, że pokazane zmiany zostały **przygotowane do zapisania w następnym commicie**.

Operacja ta jest nazywana również **stagingiem zmian**.

> Przed wykonaniem `git add .` warto sprawdzić, czy w katalogu nie znajdują się niepotrzebne pliki, np. skompilowane programy lub katalogi `build`.

---

## Utworzenie commita – `git commit`

Commit zapisuje przygotowany zestaw zmian jako kolejną wersję projektu w **lokalnym repozytorium Git**.

Commit można utworzyć poleceniem:

```bash
git commit -m "opis zmian"
```

Przykład:

```bash
git commit -m "Rozwiązanie zadań 2 i 3"
```

Przykładowy rezultat:

```text
[main 8058e5b] Rozwiązanie zadań 2 i 3
 3 files changed, 45 insertions(+), 4 deletions(-)
```

Opis commita powinien krótko informować, czego dotyczą zapisane zmiany.

Dobre przykłady:

```text
Rozwiązanie zadania 1
```

```text
Rozwiązanie zadań 2 i 3
```

```text
Poprawa zadania 4
```

```text
Dodanie notatek z lekcji 5
```

Należy unikać opisów, które nie przekazują żadnej informacji, np.:

```text
test
```

```text
zmiany
```

```text
aaa
```

---

## Sprawdzenie commita

Po utworzeniu commita można ponownie wykonać:

```bash
git status
```

Przykładowy rezultat:

```text
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

Komunikat:

```text
Your branch is ahead of 'origin/main' by 1 commit.
```

oznacza, że commit znajduje się już w lokalnym repozytorium, ale **nie został jeszcze wysłany do GitHuba**.

---

## Wysłanie zmian do GitHuba – `git push`

Aby przesłać lokalne commity do repozytorium znajdującego się na GitHubie, należy wykonać:

```bash
git push
```

Przykład:

```text
/workspaces/repo-name (main) $ git push

Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), done.
Total 5 (delta 1), reused 0 (delta 0)
To https://github.com/WDI-WDP/repo-name
   a0d9727..8058e5b  main -> main
```

Po poprawnym wykonaniu `git push` rozwiązanie powinno być widoczne w repozytorium na stronie GitHub.

Warto otworzyć repozytorium w przeglądarce i upewnić się, że znajdują się tam odpowiednie pliki.

---

## Pobieranie zmian – `git pull`

Jeżeli repozytorium jest używane na więcej niż jednym komputerze albo jego zawartość została wcześniej zmieniona na GitHubie, przed rozpoczęciem pracy warto pobrać najnowszą wersję:

```bash
git pull
```

Polecenie pobiera zmiany ze zdalnego repozytorium i aktualizuje lokalną kopię.

Przykładowy schemat rozpoczęcia pracy:

```bash
git pull
git status
```

Następnie można rozpocząć edycję plików.

---

## Udostępnianie zmian za pomocą Visual Studio Code

Git można obsługiwać również bez wpisywania poleceń w terminalu.

W Visual Studio Code należy otworzyć panel:

**Source Control / Kontrola źródła**

znajdujący się na lewym pasku aplikacji.

### 1. Sprawdzenie zmian

W panelu widoczne będą zmodyfikowane oraz nowe pliki.

Po wybraniu pliku można zobaczyć różnice pomiędzy aktualną wersją a wersją zapisaną w ostatnim commicie.

### 2. Przygotowanie zmian do commita

Przy pliku należy nacisnąć ikonę:

```text
+
```

czyli **Stage Changes / Przygotuj zmiany**.

Można również przygotować wszystkie zmiany jednocześnie za pomocą:

```text
Stage All Changes
```

### 3. Utworzenie commita

W polu wiadomości należy wpisać opis zmian, np.:

```text
Rozwiązanie zadań 2 i 3
```

Następnie należy wybrać:

```text
Commit
```

Jeżeli zmiany nie zostały wcześniej przygotowane, Visual Studio Code może zapytać, czy przygotować wszystkie zmiany i utworzyć commit.

Można wtedy wybrać:

```text
Yes / Tak
```

### 4. Wysłanie zmian do GitHuba

Po utworzeniu commita należy wybrać:

```text
Sync Changes
```

lub, zależnie od wersji Visual Studio Code:

```text
Push
```

`Push` wysyła lokalne commity do GitHuba.

Opcja `Sync Changes` może dodatkowo pobrać zmiany ze zdalnego repozytorium, a następnie wysłać lokalne commity.

Po zakończeniu synchronizacji należy sprawdzić repozytorium na stronie GitHub.

---

## Najczęstsze błędy

### Plik został zapisany, ale nie jest widoczny na GitHubie

Sprawdź:

```bash
git status
```

Następnie wykonaj:

```bash
git add .
git commit -m "Rozwiązanie zadania"
git push
```

### Commit został wykonany, ale rozwiązania nadal nie ma na GitHubie

Najprawdopodobniej commit istnieje tylko lokalnie.

Wykonaj:

```bash
git push
```

### Zadanie znajduje się w niewłaściwym katalogu

Przenieś pliki do katalogu odpowiadającego numerowi lekcji i zadania.

Przykładowo:

```text
04-Lekcja/02-Zadanie/main.cpp
```

oznacza rozwiązanie **zadania 2 z lekcji 4**.

Po przeniesieniu pliku ponownie wykonaj:

```bash
git add .
git commit -m "Poprawa struktury zadania"
git push
```

---

## Git – podsumowanie

Sprawdzenie aktualnego stanu repozytorium:

```bash
git status
```

Przygotowanie wszystkich zmian do następnego commita:

```bash
git add .
```

Utworzenie commita w lokalnym repozytorium:

```bash
git commit -m "Opis zmian"
```

Wysłanie commitów do repozytorium na GitHubie:

```bash
git push
```

Pobranie najnowszych zmian z GitHuba:

```bash
git pull
```

Podstawowy cykl pracy wygląda więc następująco:

```bash
git status
git add .
git commit -m "Rozwiązanie zadania"
git push
```

Po wykonaniu `git push` należy upewnić się, że rozwiązanie jest widoczne w repozytorium GitHub.
