# Linux - Procesy i Strumienie
---

### Zadania 0
1. Przejdź do swojego katalogu domowego
2. Wydaj komendę: ls -a
3. Zobacz ile plików wypisało.
4. Teraz wydaj komendę: ls -a | grep D
HINT: Jeśli nie masz żadnego pliku czy katalogu z literką D to wybierz inną literkę, która już będzie w nazwie jakiegoś pliku czy katalogu.
5. Zobacz ile teraz jest wyników. Co się stało?
Otóż program grep służy do wyszukiwania wierszy w pliku lub strumieniu wejściowym, które pasują do wzorca. Tu podano wzorzec jako "D".
6.A teraz wykonaj komendę: ls -a | grep D > lista_plikow_z_literka_d.txt
7. Zobacz czy utworzył sie jakiś plik?
Jaka jest jego treść?
Co znaczy | oraz co znaczy > ?
8. A teraz wykonaj komendę: ls -a | grep D | tee lista_plikow_z_literka_d_2.txt
9. Zobacz czy plik się utworzył?
Jaka jest treść względem poprzedniej próby bez programu tee?
Co robi program tee?

### Zadania 1
Program ps służy do wyświetlania listy procesów. 
Zadania:
A: Zobacz co się stanie jeśli wpiszemy w terminalu:

ps

ps -a

ps x

ps axu
INFO: tu kolejność parametrów a, x, u nie ma znaczenie a jedynie fakt, że są podane. Dowolna kolejność powinna dać ten sam wynik.

Jak myślisz, co oznacza znak zapytania w kolumnie 2?
Nie wiesz? A gdzie może być wyjaśnienie?

B: Jak wykonasz poniższe 2 zadania?

Wyświetl wszystkie procesy bash

Wyświetl wszystkei procesy należące do użytkownika root

### Zadania 2
INFO: Zadanie do wykonania na linuxie z dostępnym środowiskiem graficznym.

PID jest to indentyfikator procesu ([P]rocess [ID]entificator). Za jego pomocą możesz odwołać się do danego procesu za pomocą różnych mechanizmów systemu. Jednym z takich mechanizmów jest wysłanie sygnału (na przykład zakończenia) do procesu. Do tego można użyć komendy kill (może brzmi ona dość brutalnie, ale cóż, informatyka nie jest dla mięczaków). Komenda ta domyślnie wysyła sygnał zakończenia procesu do zadanego procesu.

Zadanie:

Uruchom wybrany przez Ciebie graficzny edytor tekstowy (np. gedit, gvim, Visual Studio Code, atom, itd...)

Zobacz jaki ma on PID - przyda się do tego komenda ps

Wydaj komendę kill w taki sposób, aby ten edytor się wyłączył. Zobacz czy to działa.
UWAGA: Niektóre programy przechwytują sygnały i mogą je częściowo blokować. 
			Jeśli program nie wyłącza się, to zobacz jaka jest jego reakcja.
			Zobacz czy możesz wysłać do niego SIGKILL (gdzie sprawdzisz jak to zrobić?)

Zobacz działanie komendy killall bash

Zobacz czy kill zadziała dla dowolnego procesu.

### Zadania 3
W terminalu jest kilka przydatnych skrótów klawiszowych. Jednym z nich jest CTRL+C lub jak to jest często podawane C-c lub ^C. Niektórzy z Państwa już go mieli okazję przetestować. Jest to sposób na wyłączenie aktywnego programu w terminalu. Proszę go przetestować w taki sposób, że:

Uruchom komendę cat be parametrów

Wciśnij CTRL+C i zobacz co się stanie

Kolejnym fajnym (zależy dla kogo :) ) skrótem klawiszowym jest CTRL+D. Służy on do zakończenia strumienia wejściowego. Działa to trochę inaczej niż poprzednie rozwiązanie, mimo że na pierwszy rzut oknawygląda tak samo. Tym razem nie wysyła sygnału zakończenia, a jedynia zamyka strumień wejściowy. Jest to bardzo przydatne, jeśli chcemy zakończyć działanie jakiegoś programu korzystającego ze standardowego wejścia (stdin), ale w sposób możliwie bezpieczny.

Zobacz co się stanie:

Wydaj komendę cat > wynik3_1.txt

Wpisz tekst witaj bez wciskania klawisza Enter

Wciśnij CTRL+C

Zobacz co się znalazło w pliku wynik3_1.txt



Wydaj komendę cat > wynik3_2.txt

Wpisz tekst witaj bez wciskania klawisza Enter

Wciśnij CTRL+D (możliwe, że będzie trzeba wcisnąć go 2x)

Zobacz co się znalazło w pliku wynik3_2.txt

W opisie rozwiązania zadania umieść:

jak rozumiesz co się stało?

czym oba te przykłady się różnią?

DLACZEGO się różnią?

### Zadania 4
INFO: Zadanie do wykonania na linuxie z dostępnym środowiskiem graficznym.

CTRL+Z służy do wstrzymania bieżącego procesu i przeniesienia go do tła. To znaczy, że program jest w pamięci, ale nie wykonuje żadnych operacji. Jest wstrzymany.

Zobacz co się stanie:

Wpisz komendę gimp (lub np. edytor tekstowy gedit)

W terminalu w którym sie to uruchomiło wciśnij CTRL+Z

Spróbuj coś wyklikać w gimpie / gedicie

Otwórz dowolne inne okno i przesuń je tak by częściowo nachodziło na okno gimpa / gedita i potem je odsuń by odsłonić w pełni okno gimpa / gedita

Co się stało? Wstrzymaliśmy program gimp/gedit. Program wstrzymany za pomocą kombinacji CTRL+Z jest przenoszony w tło (background). Efekt jest taki, że taki program przestaje odpowiadać na cokolwiek.

Komenda bg służy do wznowienia w tle wstrzymanego programu. Zobacz:

Wpisz komendę: bg

Jak widać gimp/gedit ożył (jeśli nie, to zapytaj prowadzącego)

Komenda fg służy do wznowienia na pierwszym planie wstrzymanego wcześniej procesu. Zobacz co się stanie:

Wpisz komendę: fg

Jak widać proces wrócił i można wcisnąć na przykład CTRL+C aby go zakończyć.

W momencie uruchamiania programu, możemy od razu nakazać wykonanie go w tle. Służy do tego znak & umieszczony na końcu instrukcji.

Zobacz:
INFO: Jeśli jakiegoś programu nie ma to zastąp go innym, który znasz.

Wykonaj komendę gimp &

Wykonaj komendę gedit &

Wykonaj komendę geany &

Zobacz co się stało (domyślam się, że uruchomiły się 3 programy, a na terminalu ciągle można coś pisać.



Kolejna komenda to jobs. Służy ona do wyświetlania listy zadań (jobów; nie mylić z procesami) przeniesionych do tła.

Przywróć program gedit (lub gimp, w każdym razie nie uruchomiony jako ostatni program) z tła na pierwszy plan. Skorzystaj z jobs aby dowiedzieć się jakie mają numery poszczególne zadania działające w tle.
składnia: fg %(numer jobu)