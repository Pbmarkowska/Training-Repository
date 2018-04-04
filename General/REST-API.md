### API

Application Programming Interface

Interfejs to rodzaj połączenia umożliwiający komunikację.

* Interfejs użytkownika (UI)
* Interfejs programistyczny (API)
* Interfejs fizyczny w postaci układu, umożliwiającego połączenie np. urządzen

API to po prostu sposób komunikacji pomiędzy rożnymi elementami oprogramowania. Web API to zestaw odpowiednio przygotowanych metod, zwykle dostępnych w postaci adresów URI (endpointów)

#### Czym jest API i REST?

REST - Representational State Transfer

Standard określający zasady projektowania API. W przypadku Web API opiera się o metody HTTP. Np. popularne akcje, jak CRUD (Create, Read, Update, Delete) odpowiadają metodom `POST`, `GET`, `PUT` i `DELETE`.

`GET` - zwraca listę <br>
`POST` - zapisuje nowy obiekt <br>
`PUT` - aktualizuje obiekt <br>
`DELETE`  - usuwa obiekt

##### Zasady:
1. **Uniform Interface**: interfejs powinien zapewniać ustandaryzowaną komunikację pomiędzy klientem a serwerem
2. **Client-Server**: wyraźnie zaznaczony podział pomiędzy aplikacją działającą po stronie klienta i serwera, aplikacje mogą się rozwijać niezależnie, a my zyskujemy elastyczność
3. **Stateless**: każde zapytanie musi zawierać komplet informacji niezbędnych do jego poprawnego zakończenia, np. serwer nie może przechowywać informacji o stanie klienta. Klient za każdym razem gdy wysyła zapytanie dostarcza zestaw informacji, który umożliwia serwerowi określenie czy klient ma dostęp do danych zasobów, czy też nie.
4. **Cacheable**: API powinno wspierać cache'owanie danych w celu zwiększenia wydajności. Serwer może być obciążony dużą ilością zapytań pochodzących z API, dobrą praktyką jest przechowywanie informacji w pamięci podręcznej.  
5. **Layered System**: System powinien być zaprojektowany w taki sposób aby klient wysyłający zapytanie mógł uzyskać odpowiedź bez konieczności posiadania wiedzy o tym, co się dzieje po stronie serwera.
6. **Code on demand**: opcjonalna, przewiduje możliwość wysyłania fragmentów kodu (np.JS), który może być wykonany po stronie klienta.

[Źródło - Overment Youtube - link](https://www.youtube.com/channel/UC_MIaHmSkt9JHNZfQ_gUmrg)
