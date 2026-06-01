# STYCZEŃ 2026

Repozytorium zawiera rozwiązania zadań praktycznych egzaminu zawodowego **INF.04 – Projektowanie, programowanie i testowanie aplikacji**.

Stos technologiczny:

- Nazwa środowiska programistycznego: Visual Studio 2022
- Nazwa emulatora dla aplikacji mobilnej: Android Studio Panda 4 | 2025.3.4 Patch 1
- Nazwy języków programowania: C++, Java

---
## ZADANIE 1 - INF.04.2026.01.01

Zadanie polega na wykonaniu **aplikacji konsolowej** (klasa Kosc, która reprezentuje pojedynczą kostkę do gry) z testami jednostkowymi oraz **aplikacji mobilnej** (symulacja rzutu kośćmi).

- [Rozwiązanie egzaminu](https://material.edu.tychy.pl/data/egzaminy/2026/styczen-zadanie-1/Realizacja-inf_04_2026_01_01_SG.zip)
- [Plik do zadania](https://material.edu.tychy.pl/data/egzaminy/2026/styczen-zadanie-1/zad1.7z)

---

### Część 1 – aplikacja konsolowa

Realizacja zadania wymaga stworzenia klasy Kosc, która reprezentuje pojedynczą kostkę do gry. Klasa ma zawierać:

- statyczne pole przechowujące liczbę utworzonych obiektów klasy
- kolekcję nazw plików graficznych:
  - od kosc0.png do kosc6.png
  - liczbę oczek wyrzuconą na kości
  - identyfikator odpowiadającego obrazka
  - informację logiczną określającą dostępność kości

Wymagane są dwa konstruktory:

- Konstruktor jednoargumentowy (przyjmował liczbę oczek):

  - dla wartości 1–6 ustawiał odpowiednie pola
  - dla niepoprawnej wartości ustawiał 0
  - oznaczał kość jako dostępną
  - zwiększał licznik instancji klasy

- Konstruktor bezargumentowy miał:

  - losować liczbę od 1 do 6
  - przypisywać ją jako wynik rzutu
  - ustawiać odpowiedni identyfikator obrazka
  - oznaczać kość jako dostępną
  - zwiększać licznik instancji

### Część 2 – aplikacja mobilna

Należy wykonać aplikację mobilną wykorzystującą dostarczone grafiki kości (kosc0.png – kosc6.png). Program ma realizować logikę rzutu kością i prezentować wynik użytkownikowi poprzez interfejs graficzny.

Wymagane elementy interfejsu:

- obraz przedstawiający aktualną kość
- przycisk wykonania rzutu
- pola lub etykiety prezentujące wyniki
- wykorzystanie dostarczonych plików graficznych

Dodatkowo należy również:

- uruchomić aplikację na emulatorze
- wykonać zrzuty ekranu wszystkich interakcji
- spakować projekt mobilny do folderu mobilna

### Część 3 – testy jednostkowe

Zadanie skupia się na stworzeniu projektu testów sprawdzających poprawność działania klasy Kosc. Testy mają weryfikować m.in.:

- poprawne działanie konstruktora z prawidłową wartością
- reakcję na nieprawidłowe wartości
- poprawne losowanie wartości 1–6
- poprawne ustawianie identyfikatora obrazka
- zliczanie liczby instancji klasy
- poprawne ustawianie pola dostępności

---
## ZADANIE 2 - INF.04.2026.01.02

Zadanie polega na wykonaniu dwóch aplikacji (konsolowej i mobilnej), przeprowadzeniu testów oraz przygotowaniu dokumentacji.

- [Rozwiązanie egzaminu](https://material.edu.tychy.pl/data/egzaminy/2026/styczen-zadanie-2/Realizacja-inf_04_2026_01_02_SG.zip)
- [Plik do zadania](https://material.edu.tychy.pl/data/egzaminy/2026/styczen-zadanie-2/zad2.7z)

---

### Część 1 – aplikacja konsolowa

Należy stworzyć aplikację konsolową realizującą quiz z wykorzystaniem dziedziczenia i klas abstrakcyjnych.

**Klasa Pytanie**

Klasa abstrakcyjna (nie można tworzyć jej obiektów), zawierająca:

Pola chronione:

- treść pytania
- nazwa pliku ze zdjęciem
- informacja logiczna określająca poprawność odpowiedzi

**Konstruktor** (2 argumenty):

- treść pytania
- nazwa pliku graficznego

**Konstruktor**:

- przypisuje wartości pól
- ustawia poprawność odpowiedzi na false

**Metoda abstrakcyjna**:

- przyjmuje odpowiedzi: A, B lub C

**Klasa PytanieZamkniete** dziedziczy po klasie **Pytanie**

Pola prywatne:

- odpowiedź A
- odpowiedź B
- odpowiedź C
- poprawna odpowiedź (A, B lub C)

**Konstruktor** (6 argumentów):

- treść pytania
- nazwa pliku
- odpowiedź A
- odpowiedź B
- odpowiedź C
- poprawna odpowiedź

**Metoda sprawdzająca odpowiedź**:

- porównuje odpowiedź użytkownika z poprawną
- ustawia pole logiczne poprawności
- zwraca wynik (true/false)

### Część 2 – aplikacja mobilna

**Wymagania Git**

Po utworzeniu projektu:

``` 
git init
git config --global user.name "numer_zdajacego"
git config --global user.email egzamin@poczta.pl
```

W trakcie pracy trzeba wykonać minimum 2 commity:

- po wykonaniu widoku
- po wykonaniu logiki aplikacji

**Widok aplikacji**

Elementy początkowe:

- obraz **zad1.jpg**
- pytanie: **Które to schronisko?**
- trzy odpowiedzi:
  - Na Rysiance
  - Na Wielkiej Raczy
  - Na Wielkiej Rycerzowej
- przycisk **DALEJ**

**Wymagania wyglądu**

- tło: #2E7CB8
- biały kolor tekstu
- pytanie większą czcionką
- jednoczesny wybór tylko jednego RadioButtona
- obraz, pytanie i przycisk wyśrodkowane
- odpowiedzi wyrównane do lewej strony

**Logika działania**

Pytania należy przechowywać w kolekcji (lista/tablica). Po kliknięciu **DALEJ**:

- jeśli odpowiedź jest poprawna, to zwiększ liczbę punktów
- wyświetl kolejne pytanie
- gdy skończą się pytania → wróć do pierwszego
- wyczyść zaznaczenie wszystkich odpowiedzi

### Część 3 – testy i dokumentacja

**Test 1 - klasa abstrakcyjna**
- należy spróbować utworzyć obiekt klasy Pytanie. Powinien pojawić się błąd kompilacji (klasa jest abstrakcyjna). Wykonanie zrzutu ekranu błędu oraz zakomentowanie kodu.

**Test 2 - sprawdzenie działania**

- wczytać dane do konstruktora PytanieZamkniete
- utworzyć obiekt
- wczytać odpowiedź użytkownika
- wyświetlić odpowiedź i zrobić zrzut ekranu

## Licencja

Projekt udostępniony wyłącznie w celach edukacyjnych
