# Linux - Procesy i Strumienie
---

### Zadania 0
Przypuśćmy, że nie możesz utworzyć żadnego pliku na swoim koncie uczelnianym np. na szuflandii.
Co się mogło stać? (wymień co najmniej 2 opcje)
Zakładamy, że możesz zalogować się w konsoli i nie masz zaległości w opłatach.

### Zadania 1
Jest dane takie drzewo katalogów:
<pre>
.
├── ala
│   ├── i
│   │   └── as
│   └── ma
│       └── kota
└── kot
    └── ma
        └── ale
</pre>
Znajdujesz się w katalogu `kota`. Katalog `ala`, jest w katalogu `/tmp/ukos`.
Jak przejść do katalogu `ala` ale za pomocą:
- `ścieżki względnej (relatywnej)`
- `ścieżki bezwzględnej (absolutnej)`

### Zadania 2
Masz taki układ katalogów, jak wyżej i ciągle jesteś w katalogu `kota`. Jak utworzyć poddrzewo katalogów `jan/kowalski` w katalogu ale za pomocą jednej komendy?

### Zadania 3
Masz taki układ katalogów, jak wyżej i ciągle jesteś w katalogu `kota`. Jak przenieść katalog `ale` do katalogu `i` używając:
- źródło (ścieżka względna), miejsce docelowe (ścieżka absolutna)
- źródło (ścieżka absolutna), miejsce docelowe (ścieżka względna)

### Zadania 4
Jak zamknąć program, który nie reaguje na `ctrl+c` ?

### Zadania 5
Jak wypisać wszystkie pliki w bieżącym katalogu, których nazwa zaczyna się od `al`?
Tu będzie trochę opisu ode mnie na temat wyrażeń regularnych.
Materiały:
<a href="http://www.robelle.com/smugbook/regexpr.html">Link 1</a>
<a href="https://www.regular-expressions.info/">Link 2</a>

Narzędzia do testowania wyrażeń regularnych w przyzwoity sposób:
<a href="https://regex101.com/">Link 3</a>
<a href="https://regexr.com/">Link 4</a>

### Zadania 6
Nadaj uprawnienia do katalogu `ala` tak aby:
- każdy mógł do niego wejść
- tylko grupa mogła wyświetlić co w nim jest
- właściciel ma pełne prawa

Przygotuj 3 wariacje rozwiązania tego zadania używając różnych notacji: 
- oktalnej/ósemkowej/cyfrowej
- literowej ze znakiem równości
- literowej z plusami i minusami

Wszystkie wersje powinny być zapisane w jednym poleceniu (bez używania `&&` czy `|` )

### Zadania 7
Jak utworzyć plik z listą plików w bieżącym katalogu?

### Zadania 8
Jak przyspieszyć wpisywanie komend w terminalu? Jaki klawisz pozwala na uzupełnianie komend?

### Zadania 9
Jak uruchomić program by nie blokował terminala. Są 2 sposoby. Jakie?
