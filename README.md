# Wytyczne do projektu z przedmiotu Bazy Danych 2020

| Kierunek              | Przedmiot   | Semestr | Rok akademicki |
| :--------------------: | :---------: | :-----: | :------------: |
| Informatyka Stosowana | Bazy danych | 4       | 2019/2020      |

## Informacje wstępne
Projekt z przedmiotu Bazy Danych realizowany jest w grupach dwuosobowych. Celem projektu jest **zaprojektowanie** oraz **implementacja** systemu bazodanowego na wylosowany przez grupę temat. Grupa ma prawo zmienić temat na inny, wybrany przez siebie, jednak nie może się on znajdować na zbiorczej liście.

## Struktura projektu
```bash
.
├── /project/       # Katalog główny projektu
│   ├── /resources/ # Pliki zasobów dołączonych do projektu, np. zrzuty ekranu, rysunki, itp.
│   ├── /sql/       # Zapytania SQL
│   ├── /src/       # Kod źródłowy aplikacji
│   └── /README.md  # Opis projektu w formie pliku markdown
├── /.gitignore     # Pliki i foldery pomijane przy commitowaniu do repozytorium
└── /README.md      # Opis projektu: wytyczne
```
Projekt składa się z dwóch części - projektu bazy danych oraz zaimplementowania funkcjonalności z wykorzystaniem dowolnego języka programowania. Preferowany jest język Python w połączeniu z biblioteką [ _pymysql_](https://pymysql.readthedocs.io/en/latest/).

### Projekt bazy danych
Pierwszym etapem projektu jest stworzenie schematu bazy danych i jego wizualizacja przy pomocy diagramu ERD. Do tego celu należy wykorzystać [DrawIO](https://drawio-app.com/). Diagram należy przechowywać w repozytorium i zaprezentować w [szczegółowym opisie projektu](project/README.md).

Schemat bazy powinien być przemyślany i zawierać niezbędne encje oraz łączące je relacje. Niedopuszczalne jest, aby diagram był niespójny - wszystkie encje powinny być połączone w _jeden spójny system_. Liczba encji na schemacie oraz szczegółowość ich opisu wpływa na ocenę końcową.

W miarę możliwości, encje należy rozstawiać w sposób niwelujący przecięcia lub minimalizujący ich końcową liczbę. Zbyt duża liczba połączeń na schemacie może być przyczyną wystąpienia przecięć. Wówczas należy przeanalizować schemat i w razie konieczności usunąć zbędne powiązania między encjami.

### Implementacja funkcjonalności za pomocą zapytań SQL
tbd...


### Aplikacja
Etapem ostatnim projektu jest zaimplementowanie prostej aplikacji (najlepiej konsolowej) do wizualizacji projektu systemu

### Przykładowy projekt
Przykładowy projekt znajdą Państwo w przygotowanym przeze mnie [repozytorium](#). Proszę, aby Państwo nie kopiowali 1:1 mojej wizji. Podany projekt ma charakter wyłącznie poglądowy i jest niewystarczający do uzyskania pozytywnej oceny.

## Wymagania
tbd...

## Uwagi i wskazówki
1.  Do pracy nad projektem wymagana jest praca na repozytorium gitowym. Informacje na ten temat przekażę Państwu w ramach wykładu z _Administracji Sieciami Komputerowymi_. Nieumiejętna praca z takim repozytorium może nie tylko przysporzyć problemów, ale również doprowadzić to całkowitej _utylizacji_ Waszego projektu.

## Przydatne materiały
1. Poza wykładem z ASK, dołączam tutaj przykładowe źródła:
    1. [Pro Git by Scott Chacon](https://git-scm.com/book/pl/v2);
    2. [Git basics by Academind](https://academind.com/learn/web-dev/git-the-basics/);
    3. Nie jestem zwolennikiem zaczynania nauki od YT, bo często _prowadzący_ popełnia sporo błędów lub wprowadza skróty myślowe, jednak te trzy filmy zasługują na uznanie i mogę je polecić z czystym sumieniem:
        1. [Git - core concepts](https://www.youtube.com/watch?v=uR6G2v_WsRA);
        2. [Git - branching and merging](https://www.youtube.com/watch?v=FyAAIHHClqI);
        3. [Git - remotes](https://www.youtube.com/watch?v=Gg4bLk8cGNo);
2. Projektowanie baz danych:
    1. <https://docs.google.com/presentation/d/1ZLtBj2qpUruyJmJaJmpjUP3DGLLbHKZt3ADerRlyp3U/edit#slide=id.g3ce3f8c6dd_2_492>;
    2. Wykłady od Piotra Macioła;
3. Diagramy ERD:
    1. <https://www.smartdraw.com/entity-relationship-diagram/>;
    2. <https://en.wikipedia.org/wiki/Entity%E2%80%93relationship_model>;
    3. <https://docs.google.com/presentation/d/1-2I78MMznp_8HZytF1YOdsLlTABlRiKasJH9ffriwHg/edit#slide=id.g74303bf83f_0_395>;
4. Język SQL:
    1. [Tech on the Net](https://www.techonthenet.com/mysql/index.php);
    2. [Geeks for Geeks](https://www.geeksforgeeks.org/sql-ddl-dql-dml-dcl-tcl-commands/);
    3. Dokumentacja: [mysql](https://dev.mysql.com/doc/) lub [mariadb](https://mariadb.com/kb/en/documentation/);
    4. Instrukcje na [mojej stronie](http://home.agh.edu.pl/~phajder/2020_IS_BD/).
5. Najlepszym przyjacielem niniejszego projektu powinien być znany wszystkim Internet.