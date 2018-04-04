### Podstawy protokołu HTTP

Protokół HTTP to jeden z zestawów zasad według których odbywa się przesyłanie danych w Internecie. Komunikacja opiera się o zapytania (*request*) oraz odpowiedzi (*response*) przesyłane z pomocą adresów URL.

Zapytanie sklada się z nagłówków (*headers*) i treści (*body*).

Zapytanie posiada swój rodzaj (*request type*), który je definiuje, a odpowiedź posiada kod statusu (*status code*).

Protokół HTTP wykorzystuje do komunikacji adresu URL.

Budowa adresu URL:
* protokół
* domena
* ścieżka
* query string: dodatkowe parametry określajce zapytanie

Za każdym razem, kiedy wpisujemy adres w przeglądarce, wykonujemy zapytanie HTTP, serwer, na którym znajduje się strona zwraca odpowiedź, a przeglądarka wyświetla stronę. --> klasyczny przykład zapytania metodą GET.

Zadaniem metod jest wskazanie rodzaju wykonywanej akcji. Np. dane mogą być odczytywane, zapisywane, modyfikowane, edytowane lub usuwane.

`GET` - zapytania typu GET służą do **pobierania danych** i nie posiadają treści (**request body**), w przeciwieństwie do zapytać typu `POST`, które służą do przesyłania danych, które mają zostać przetworzone. <br>
`POST` - zapisywanie nowych danych <br>
`PUT` - przesyłanie i zamiana nowych danych <br>
`PATCH` - aktualizacja istniejących danych<br>
`DELETE` - usunięcie danych

Odpowiedzi posiadają status.

Rolą statusu jest informowanie o tym, czy dane żądanie zostało wykonane pomyślnie, czy też nie oraz zasygnalizowanie podjętego działania.
2** - OK <br>
3** - Redirection: Nastąpiło przekierowanie na innych adres <br>
4** - Client Error: Oddany zasób nie istnieje lub jest niedostępny <br>
5** - Server Error

[Źródło - Overment Youtube - link](https://www.youtube.com/channel/UC_MIaHmSkt9JHNZfQ_gUmrg)
