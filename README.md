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
Projekt składa się z trzech części - projektu bazy danych, zaimplementowania funkcjonalności za pomocą języka SQL oraz wykorzystaniem napisanych zapytań w aplikacji.

### Projekt bazy danych
Pierwszym etapem projektu jest stworzenie schematu bazy danych i jego wizualizacja przy pomocy diagramu ERD. Diagram należy przechowywać w repozytorium i zaprezentować w [szczegółowym opisie projektu](project/README.md)

Schemat bazy powinien być przemyślany i zawierać niezbędne encje oraz łączące je relacje. Niedopuszczalne jest, aby diagram był niespójny - wszystkie encje powinny być połączone w _jeden spójny system_. Liczba encji na schemacie oraz szczegółowość ich opisu wpływa na ocenę końcową.

W miarę możliwości, encje należy rozstawiać w sposób niwelujący przecięcia lub minimalizujący ich końcową liczbę. Zbyt duża liczba połączeń na schemacie może być przyczyną wystąpienia przecięć. Wówczas należy przeanalizować schemat i w razie konieczności usunąć zbędne powiązania między encjami.

### Implementacja funkcjonalności za pomocą zapytań SQL
Przygotowany schemat bazy danych ma służyć, by przechowywać stan aplikacji, co pozwala na realizowanie wielu z jej funkcjonalności. tbd...


### Aplikacja
Etapem ostatnim projektu jest zaimplementowanie prostej aplikacji (najlepiej konsolowej) do wizualizacji projektu systemu. Preferowany jest język Python w połączeniu z biblioteką [ _pymysql_](https://pymysql.readthedocs.io/en/latest/). tbd...

### Przykładowy projekt
Przykładowy projekt znajdą Państwo w przygotowanym przeze mnie [repozytorium](#). Proszę, aby Państwo nie kopiowali 1:1 mojej wizji. Podany projekt ma charakter wyłącznie poglądowy i jest niewystarczający do uzyskania pozytywnej oceny.

## Wymagania
tbd...

## Narzędzia
1. _Projekt bazy danych_: diagram powinien być czytelny, więc należy go wyeksportować do formatu wektorowego, najlepiej SVG. Do tego celu można wykorzystać następujące narzędzia:
    1. [DrawIO](https://drawio-app.com/). Przykład dołączenia diagramów DrawIO do pliku markdown znajdą Państwo w [wiki DrawIO](https://github.com/jgraph/drawio/wiki/Embed-Diagrams) oraz na [ich repo](https://github.com/jgraph/drawio-github).
    2. [Visual Paradigm](https://www.visual-paradigm.com/tutorials/how-to-model-relational-database-with-erd.jsp). Plik projektu VP nie musi znajdować się na repo, wystarczy tylko wyeksportowana grafika.
    3. Niektóre IDE do pracy z BD mają wbudowane narzędzia do generacji takich diagramów, np. [SQL Server Management Studio](https://stackoverflow.com/questions/32379038/how-to-generate-entity-relationship-er-diagram-of-a-database-using-microsoft-s) dla MSSQL czy [DataGrip](https://www.jetbrains.com/help/datagrip/creating-diagrams.html).
2. _Implementacja funkcjonalności w formie zapytań SQL_: do pisania zapytań SQL można wykorzystać dowolne IDE, pozwalające na pracę z bazami danych:
    1. [Squirrel SQL](http://squirrel-sql.sourceforge.net/) jest lekkim Javowym klientem do obsługi połączeń z bazami danych.
    2. [DataGrip](https://www.jetbrains.com/datagrip/) multiplatformowy klient do połączeń z bazami danych. Wymagana jest licencja, by z niego korzystać, jednak studenci i pracownicy uczelni mają ją za darmo. Trzeba tylko zarejestrować się z mailem w domenie edu.
    3. [Narzędzia JetBrains'a](https://www.jetbrains.com/help/pycharm/managing-data-sources.html) mają dostępny plugin do obsługi baz danych, więc można połączyć pracę z bazą i implementację w Pythonie w PyCharm'ie.
    4. **Uwaga**: do połączenia z bazą danych wymagany jest odpowiedni sterownik. [Czym jest sterownik?](https://www.jdatalab.com/information_system/2017/02/16/database-driver.html) W DataGrip'ie to jeden przycisk, w Squirrelu trzeba dodać go w [odpowiedni sposób](http://home.agh.edu.pl/~phajder/2020_IS_BD/extra/SquirrelConfig.pdf).
3. _Aplikacja_: do implementacji aplikacji zalecam wykorzystanie języka Python w połączeniu z biblioteką do bazy mysql - [_pymysql_](https://pymysql.readthedocs.io/en/latest/). Do pracy można wykorzystać następujace IDE:
    1. [PyCharm](https://www.jetbrains.com/pycharm/) od JetBrainsa. Wersja community powinna być wystarczająca. Znacząco uprości to też pracę z gitem.
    2. [Visual Studio Code](https://code.visualstudio.com/). Małe IDE, które można rozbudować pod własne potrzeby. Konieczne będzie zainstalowanie [pluginu do Pythona](https://github.com/Microsoft/vscode-python) przez menedżer pluginów. Dostępne są też narzędzia do pracy z SQLem.
    3. Dopuszczalne jest wykorzystanie innego języka programowania, np. Java, C#, js, przy czym prosiłbym o indywidualny kontakt w takiej sytuacji. Nie wolno wykorzystywać frameworków typu ORM, gdyż projekt polega na pisaniu zapytań SQL.

## Uwagi i wskazówki
1.  Do pracy nad projektem wymagana jest praca na repozytorium gitowym. Informacje na ten temat przekażę Państwu w ramach wykładu z _Administracji Sieciami Komputerowymi_. Nieumiejętna praca z takim repozytorium może nie tylko przysporzyć problemów, ale również doprowadzić to całkowitej _utylizacji_ Waszego projektu.
2. Celem napisania aplikacji do obsługi bazy danych jest zrozumienie sensu wykorzystywania baz danych. Taka aplikacja może Państwu pomóc w ocenie, czy dane zapytanie zostało poprawnie napisane. Powinna również ocenę poprawności schematu.
3. tbd...

## Przydatne materiały
1. Poza wykładem z ASK, dołączam tutaj przykładowe źródła:
    1. [Pro Git by Scott Chacon](https://git-scm.com/book/pl/v2);
    2. [Git basics by Academind](https://academind.com/learn/web-dev/git-the-basics/);
    3. Nie jestem zwolennikiem zaczynania nauki od YT, bo często _prowadzący_ popełnia sporo błędów lub wprowadza skróty myślowe, jednak te trzy filmy zasługują na uznanie i mogę je polecić z czystym sumieniem:
        1. [Git - core concepts](https://www.youtube.com/watch?v=uR6G2v_WsRA);
        2. [Git - branching and merging](https://www.youtube.com/watch?v=FyAAIHHClqI);
        3. [Git - remotes](https://www.youtube.com/watch?v=Gg4bLk8cGNo);
2. Projektowanie baz danych:
    1. [Wykład o projektowaniu BD](https://docs.google.com/presentation/d/1ZLtBj2qpUruyJmJaJmpjUP3DGLLbHKZt3ADerRlyp3U) z kursu CS145 na Stanford;
    2. Wykłady od Piotra Macioła;
3. Diagramy ERD:
    1. [Entiti Relationship Diagram](https://www.smartdraw.com/entity-relationship-diagram/) w Internecie;
    2. [Model ER wiki](https://en.wikipedia.org/wiki/Entity%E2%80%93relationship_model);
    3. [Wykład o modelach ER](https://docs.google.com/presentation/d/1-2I78MMznp_8HZytF1YOdsLlTABlRiKasJH9ffriwHg) z kursu CS145 na Stanford;
4. Język SQL:
    1. [Tech on the Net](https://www.techonthenet.com/mysql/index.php);
    2. [Geeks for Geeks](https://www.geeksforgeeks.org/sql-ddl-dql-dml-dcl-tcl-commands/);
    3. Dokumentacja: [mysql](https://dev.mysql.com/doc/) lub [mariadb](https://mariadb.com/kb/en/documentation/);
    4. Instrukcje na [mojej stronie](http://home.agh.edu.pl/~phajder/2020_IS_BD/).
5. Najlepszym przyjacielem niniejszego projektu powinien być znany wszystkim Internet.