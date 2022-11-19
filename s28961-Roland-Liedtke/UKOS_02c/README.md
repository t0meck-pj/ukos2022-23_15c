# Linux - uprawnienia dostępu
---

### Zadania 1
Porcja ćwiczeń (do wykonania na szuflandii)
1. Utworzyć we własnym katalogu domowym niedużą strukturę podkatalogów i plików tekstowych. Przydzielić różne uprawnienia dostępu, następnie spróbować wejść do katalogów domowych innych uczestników zajęć i sprawdzić, które z obiektów są tam dla nas dostępne (i w jakim sensie). Spróbować utworzyć własny plik w cudzym katalogu (`"kukułcze jajko"`) oraz spróbować usunąć cudzy plik we własnym katalogu (co można zaobserwować ?). Wypróbować powyższe operacje:
- w trybie tekstowym;
- przy użyciu programu `Midnight Commander` (mc);
2. W utworzonej na swoim koncie strukturze podkatalogów przeprowadzić eksperymenty:
- usuwając wszelkie uprawnienia dostępu do katalogu bieżącego
- usuwając wszelkie uprawnienia dostępu do katalogu nadrzędnego (nadkatalogu).
- W jakich przypadkach możemy wykonać wtedy polecenie `cd` ? 
- W jakich przypadkach możemy wykonać polecenie `chmod` ? 
- Czy możemy bezpośrednio przeskoczyć do katalogu `ABC/XYZ`, jeśli nie mamy uprawnienia wstępu do `ABC`, ale mamy do `XYZ` ?
- Czy możemy także wrócić korzystając z polecnia `cd -` ?
3. W zespołach 2- lub 3-osobowych (w opisie zadania na githubie proszę umieścić login osób z zespołu) wypróbować możliwość komunikacji przez współdzielony plik: na jednym z kont w zespole utworzyć pusty plik i przydzielić odpowiednie uprawnienia dostępu (do pliku i do katalogu domowego). Wpisywać i odczytywać komunikaty przy użyciu poleceń:
- `echo treść_komunikatu > plik`
- `cat plik`
Sprawdzić, jaki skutek powoduje zamiana operatora `>` na operator `>>` w poleceniu `echo`. Uruchom także drugi terminal i wykonaj w nim komendę `tail -f plik` i powtórz powyższe ćwiczenie w pierwszym terminalu (komunikacja za pomocą pliku).
4. Znaleźć w swoim katalogu domowym podkatalog `public_html` (jeśli go nie ma, to utworzyć; musi się on nazywać DOKŁADNIE tak jak podano, pisane małymi literami z podkreśleniem zamiast spacji pomiędzy słowami). Umieścić w nim plik o nazwie `strona.html` o następującej zawartości:

<pre><code>
<HTML>
<BODY>
<H1>To jest moja strona domowa</H1>
</BODY>
</HTML>
</code></pre>

Sprawdzić, jakie są minimalne uprawnienia dostępu, które trzeba przydzielić do:
- katalogu domowego;
- katalogu public_html;
- pliku strona.html, aby zawartość pliku była widoczna w przeglądarce internetowej pod adresem http://szuflandia.pjwstk.edu.pl/~twój_login/strona.html
5. W opisie bash-a (man) przeczytać opis polecenia wewnętrznego umask i wypróbować jego działanie sprawdzając, a następnie zmieniając swoją maskę trybu pliku i tworząc za każdym razem nowe pliki (przy użyciu polecenia touch plik), a później sprawdzając uzyskane uprawnienia dostępu do nich (polecenie ls -l). Jaka operacja logiczna na bitach domyślnych uprawnień dostępu oraz maski jest wykonywana ? 
