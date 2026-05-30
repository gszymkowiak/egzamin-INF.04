# STYCZEŃ 2026

Repozytorium zawiera rozwiązania zadań praktycznych egzaminu zawodowego **INF.04 – Projektowanie, programowanie i testowanie aplikacji**.

---
## ZADANIE 1 - INF.04.2026.01.01

Zadanie polega na wykonaniu **aplikacji konsolowej** (klasa Kosc, która reprezentuje pojedynczą kostkę do gry) oraz **aplikacji mobilnej** (symulacja rzutu kośćmi).

- [Rozwiązanie egzaminu](https://material.edu.tychy.pl/data/egzaminy/2026/styczen-zadanie-1/Realizacja-inf_04_2026_01_01_SG.zip)
- [Plik do zadania](https://material.edu.tychy.pl/data/egzaminy/2026/styczen-zadanie-1/zad1.7z)

---

### Część 1 – aplikacja konsolowa

Należało zaprogramować klasę Kosc, która reprezentuje pojedynczą kostkę do gry. Klasa miała zawierać:

- statyczne pole przechowujące liczbę utworzonych obiektów klasy
- kolekcję nazw plików graficznych:
  - od kosc0.png do kosc6.png
  - liczbę oczek wyrzuconą na kości
  - identyfikator odpowiadającego obrazka
  - informację logiczną określającą dostępność kości

Wymagane były dwa konstruktory:

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

Należało wykonać aplikację mobilną wykorzystującą dostarczone grafiki kości (kosc0.png–kosc6.png). Aplikacja miała realizować mechanikę rzutu kością i prezentować wynik użytkownikowi poprzez interfejs graficzny.

Typowe elementy interfejsu obejmowały:

- obraz przedstawiający aktualną kość
- przycisk wykonania rzutu
- pola lub etykiety prezentujące wyniki
- wykorzystanie dostarczonych plików graficznych

Należało również:

- uruchomić aplikację na emulatorze
- wykonać zrzuty ekranu wszystkich interakcji
- spakować projekt mobilny do folderu mobilna

### Część 3 – testy jednostkowe

Należało utworzyć projekt testów sprawdzających poprawność działania klasy Kosc. Testy powinny weryfikować m.in.:

- poprawne działanie konstruktora z prawidłową wartością
- reakcję na nieprawidłowe wartości
- poprawne losowanie wartości 1–6
- poprawne ustawianie identyfikatora obrazka
- zliczanie liczby instancji klasy
- poprawne ustawianie pola dostępności

## Licencja

Projekt udostępniony wyłącznie w celach edukacyjnych
