### 1.1 Dlaczego testowanie jest niezbędne?
*pluskwa, defekt, błąd, awaria, pomyłka, ryzyko*

##### Przyczyny usterek w oprogramowaniu

Człowiek może popełnić **błąd (pomyłkę)** w kodzie programu lub dokumencie.
Jeżeli kod zawierający defekt zostaje wykonany, system nie zrobi tego, co powinien (lub wykona to czego nie powinien) powodując **awarię**.
Usterki w oprogramowaniu, systemach lub dokumentach mogą prowadzić do wystąpienia awarii, ale nie wszystkie usterki powodują awarie.

##### Rola testowania w rozwoju, utrzymaniu i użytkowaniu oprogramowania.

Testy systemów i dokumentacji mogą pomóc w zmniejszeniu ryzyka wystąpienia problemów podczas użytkowania oprogramowania i przyczynić się do podniesienia jakości systemu, **jeśli znalezione usterki zostaną poprawione przed wdrożeniem systemu do użytkowania**.

##### Testowanie a jakość

Testowanie może budować zaufanie do jakości oprogramowania, jeżeli osoby testujące znajdują mało usterek. **Poprawnie zaprojektowany test, który jest zaliczony obniża ogólny poziom ryzyka w systemie**.

Kiedy testowanie wykrywa usterki, jakoś systemu podnosi się wraz z ich naprawieniem. Samo testowanie nie podnosi jakości oprogramowania i dokumentacji.

### 1.2 Co to jest testowanie?
*debagowanie, wymaganie, przegląd, przypadek testowy, testowanie, cel testu*

Czynności testowania:
* planowanie i nadzór
* wybór warunków testowych
* projektowanie i wykonywanie przypadków testowych
* sprawdzanie wyników
* ocena spełnienia kryteriów zakończenia
* raportowanie procesu testowania i testowanego systemu
* kończenie i zamykanie testów (po zakończeniu fazy testów)
* przeglądy dokumentacji i kodu źródłowego
* analiza statyczna

Cele testowania:
* znajdowanie usterek
* nabieranie zaufania do poziomu jakości
* dostarczanie informacji potrzebnych do podejmowania decyzji
* zapobieganie defektom

**Debagowanie** to czynność programistyczna, która znajduje, analizuje i umożliwia usunięcie przyczyny awarii. Późniejsze testy potwierdzające (retesty) wykonywane przez testera gwarantują, że poprawka rzeczywiście usunęła usterkę.

**Testerzy testują, a programiści debagują**

### 1.3 Zasady testowania

1. **Testowanie ujawnia usterki** (jeśli ne zostały znalezione żadne usterki, nie stanowi to dowodu poprawności oprogramowania)
2. **Testowanie gruntowne jest niewykonalne.** Przetestowanie wszystkiego jest wykonalne tylko w trywialnych przypadkach. Zamiast testowania gruntownego, do kierowania testami należy wykorzystać analizę ryzyka i priorytetyzację.
3. **Wczesne testowanie**
4. **Kumulowanie się błędów**
5. **Paradoks pestycydów**. Jeżeli te same testy są powtarzane bez zmian, to w końcu przestaną znajdować nowe usterki. Żeby przezwyciężyć 'paradoks pestycydów', testy muszą być regularnie przeglądane i uaktualniane.
6. **Testowanie zależy od kontekstu**.
7. **Mylne przekonanie o braku błędów**. Znajdowanie i naprawa usterek nie pomoże, jeżeli produkowany system nie nadaje się do użytkowania lub nie spełnia wymagań i oczekiwań użytkownika.

### 1.4 Podstawowy proces testowy

Podstawowy proces testowy składa się z następujących części:
* **planowanie i nadzór nad testami**

polega na zdefiniowaniu celów testowania i określeniu czynności testowych potrzebnych do wypełnienia misji i celów testowania
* **analiza i projektowanie testów**

ogólne cele testowania przekształcane są w konkretne warunki testowe i przypadki testowe

Główne zadania analizy i projektowania testów:

* przeglądanie podstawy testów
* ocena testowalności podstawy testów i przedmiotu testów <br>
* identyfikacja i priorytetyzacja warunków testowych na podstawie analizy elementów testowych, specyfikacji, zachowania i struktury oprogramowania
* projektowanie i priorytetyzacja przypadków testowych wysokiego poziomu
* ustalanie jakie dane testowe są potrzebne dla warunków testowych oraz przypadków testowych
* projektowanie środowiska testowego oraz identyfikacja potrzebnej infrastruktury

* **tworzenie dwukierunkowego śledzenia pomiędzy podstawą testów oraz przypadkami testowymi**

* **implementacja i wykonanie testów**
to czynność, podczas której specyfikowane są procedury i skrypty testowe przez ustawienie przypadków testowych w konkretnej kolejności oraz dołączenie innych informacji potrzebnych do wykonania testów, konfigurowane jest środowisko testowe oraz są wykonywane testy.

Główne zadania implementacji i wykonania testów:
* dokończenie, implementacja i priorytetyzacja przypadków testowych
* przygotowanie i priorytetyzacja procedur testowych, tworzenie danych testowych oraz (opcjonalnie) przygotowanie jarzm testowych i pisanie automatycznych skryptów testowych
* tworzenie zestawów testów z procedur testowych w celu efektywniejszego wykonania testów
* sprawdzenie czy środowisko testowe zostało poprawnie skonfigurowanie
* weryfikacja oraz uaktualnienie dwukierunkowego śledzenia pomiędzy podstawą testów oraz przypadkami testowymi
* wykonanie procedur testowych w zaplanowanej kolejności, ręcznie lub przy pomocy narzędzi do wykonywania testów
* zapisywanie wyników wykonania testów oraz zapisanie identyfikatorow i wersji testowanego oprogramowania, narzędzi testowych oraz testaliów
* porównywanie wyników rzeczywistych z wynikami oczekiwanymi
* raportowanie rozbieżności jako incydentów oraz ich analiza w celu ustalenia ich przyczyny
* powtarzanie czynności testowych jako rezultt akcji podjętych po stwierdzeniu rozbieżności: retesty (testy potwierdzające), testy regresywne


* **ocena kryteriów zakończenia i raportowanie** polega na ocenie wykonania testów zgodnie z przyjętymi celami testowania. Powinna być wykonywana dla każdego poziomu testowania.

Główne zadania oceny spełnienia kryteriów zakończenia:
* sprawdzenie w logach testów czy zostały spełnione kryteria zakończenia testów określone podczas planowania
* ocenienie, czy potrzeba więcej testów lub czy nie powinny zostać zmienione kryteria zakończenia
* napisanie raportu podsumowującego testy dla interesariuszy

* **czynności zamykąjące test**
W ramach czynności zamykających testy zbierane są dane z zakończonych czynności testowych, żeby utrwalić doświadczenie, testalia, fakty i liczby. Czynności zamykające testy wykonywane są przy kamieniach milowych projektu takich jak: wydanie systemu, zakończenie (lub anulowanie) projektu testowego, osięgnięcie kamienia milowego, lub zakończenie wydania serwisowego.

Główne zadania wykonywania w ramach czynności zamykąjących testy są:
* sprawdzenie, które planowane produkty zostały dostarczone
* zamknięcie raportów incydentów lub utworzenie zgłoszeń zmian, dla tych, które pozostały otwarte
* udokumentowanie akceptacji systemu
* dokończenie i zarchiwizowanie testaliów, środowiska testowego i infrastruktury testowej do ponownego użycia w późniejszym terminie
* przekazanie testaliów do zespołu serwisowego
* przenalizowanie doświadczeń by ustalić jakie zmiany są potrzebne w przyszłych wydaniach i projektach
* wykorzystanie zebranych informacji do podniesienia dojrzałości testowania.

## 2.1 Modele wytwarzania oprogramowania

Model V (sekwencyjny): MISA
* testy modułowe (jednostkowe)
* testy integracyjne
* testy systemowe
* testy akceptacyjne

Modele iteracyjno-przyrostowe <br>
Iteracyjno-przyrosotwe wytwarzanie oprogramowania to proces zbierania wymagań projektowania, budowania oraz testowania systemu zorganizowany w krótsze cykle rozwojowe np. prototypowanie, RAD, RUP oraz metodyki zwinne.

**Testowanie regresywne jest bardzo ważne w każdej iteracji oprócz pierwszej. Każdy przyrost może podlegać zarówno weryfikacji, jak i walidacji. **

#### Testowanie w cyklu życia oprogramowania
W każdy modelu rozwoju oprogramowania dobre testowanie posiada kilka niezmiennych cech:
* dla każdej czynności związanej z wytworzeniem oprogramowania istnieją odpowiadające jej czynności związane z testowaniem
* każdy poziom testowania ma zdefiniowane cele
* analiza i projektowanie testów dla danego poziomu powinny rozpoczynać się już podczas odpowiadającej im fazy wytwarzania
* testerzy powinni uczestniczyć w przeglądach już od wczesnych wersji dokumentacji

### 2.2 Poziomy testów

#### Testy modułowe
Polegają na wyszukiwaniu błędów i weryfikacji funkcjonalności oprogramowania, które można **testować oddzielnie**. Można podczas nich użyć **zaślepek, sterowników testowych oraz symulatorów.**

Testy modułowe mogą zawierać testy funkcjonalności oraz niektórych atrybutów niefunkcjonalnych, takich jak stopień wykorzystania zasobów (np. wycieków pamięci) lub odporności, jak również testy strukturalne (np. pokrycia decyzji).

Testy modułowe zwykle wykonuje się mając dostęp do kodu źródłowego i przy wsparciu środowiska rozwojowego, zwykle angażują programistę. Usterki są usuwane jak tylko zostaną wykryte.

Podejście 'Najpierw testuj' (TDD - Test Driven Development - Wytwarzanie sterowane testowaniem) - jednym z podejść do testów modułowych jest przygotowanie i zautomatyzowanie przypadków testowych przed kodowaniem.  

Typowe obiekty testów:
* moduły
* programy
* programy do konwersji lub migracji danych
* moduły bazodanowe   

#### Testy integracyjne

Testy integracyjne sprawdzają interfejsy pomiędzy modułami, interakcje z innymi częściami systemu oraz interfejsy pomiędzy systemami.

Testowanie integracji modułów sprawdza intrakcje między modułami oprogramowania i jest wykonywane po testach modułowch.

Testowanie integracji systemów sprawdza interakcje pomiędzy różnymi systemami lub pomiędzy sprzętem a oprogramowaniem i może być wykonywane po testach systemowych.

Na każdym etapie integracji testerzy koncentrują się wyłącznie na samej integracji.

Systematyczne strategie integracji mogą bazować na architekturze systemu (np. strategie wstępująca i zstępująca), zadaniach funkcjonalnych, sekwencjach przetwarzania transakcji albo na innym aspekcie systemu lub modułu.

Typowe obiekty testów:
* implementacja baz danych podsystemów
* infrastruktura
* interfejsy
* konfiguracja systemu i dane konfiguracyjne

Na każdym etapie integracji testerzy koncentrują się wylącznei na samej integracji (a nie na funkcjonalności).

Systematyczne strategie integracji mogą bazować na architekturze systemu (np. strategie wstępująca i zstępująca), zadaniach funkcjonalnych, sekwencjach przetwarznia transakcji albo na innym aspekcie systemu lub modułu.

#### Testy systemowe

Testy systemowe zajmują się zachowaniem systemu/produktu. Środowisko testowe, podczas testów systemowych, powinno być zgodne ze środowiskiem docelowym/produkcyjnym w jak najwyższym możliwym stopniu, żeby zminimalizować ryzyko wystąpienia awarii spowodowanych przez środowisko.

Testy systemowe powinny sprawdzać funkcjonalne, jak i niefunkcjonalne **wymagania** na system oraz jakość danych.

Testy systemowe są często wykonywane przez niezależny zespół testowy.

Typowe obiekty testów:
* podręczniki systemowe, użytkownika i operacyjne
* konfiguracja systemu i dane konfiguracyjne

#### Testy akceptacyjne

Odpowiedzialnóść za testy akceptacyjne leży często po stronie klientów lub użytkowników systemu.

Celem testów akceptacyjnych jest nabranie zaufania do systemu (nie szukam bugów, tylko potwierdzam, że działa)

Typowe formy testów akceptacyjnych:
* testowanie akceptacyjne użytkownika (sprawdza przydatkość systemu dla użytkowników)
* akceptacja systemu przez administratorów
* testy akceptacyjne zgodności z umową i testy zgodności legislacynej
* testy alfa i beta

Testy alfa - są wykonywane u producenta, a nie przez zespół projektowy.

Testy beta - są wykonywane przez klientów lub potencjalnych klientów w ich własnych lokalizacjach.

## 2.3 Typy testów

Cele testów:
* przetestowanie jakiejś funkcji wykonywanej przez oprogramowaniem - **TESTY FUNKCJONALNE**
* przetestowanie jakiegoś niefunkcjonalnego atrybutu jakościowego (takiego jak niezawodność lub użyteczność) - **TESTY NIEFUNKCJONALNE**
* przetestowanie struktury lub architektury systemu - **TESTY STRUKTURALNE**
* testy związane ze zmianami, to jest **potwierdzeniem, że usterki zostały naprawione (testy potwierdzające == retesty) i szukaniem niezamierzonych zmian (testowanie regresywne)** - **RETESTY LUB TESTOWANIE REGRESYWNE**

#### Testowanie funkcjonalne (testowanie funkcji)

Funkcje są tym, "co" system robi.

Testy funkcjonalne zajmują się zewnętrznym zachowaniem oprogramowania (testy czarnoskrzynkowe).

Testy funkcjonalne można wykonywać na wszystkich poziomach.

**Typy testów funkcjonalnych:**
* testowanie zabezpieczeń
* testowanie współdziałania (ocenia zdolność oprogramowania do współpracy z jednym lub większą liczbą wskazanych modułów lub systemów)


#### Testowanie niefunkcjonalne (testowanie atrybutów niefunkcjonalnych)

Testowanie niefunkcjonalne polega na sprawdzeniu "jak" system działa.

Testy niefunkcjonalne mogą być wykonywane na wszystkich poziomach testów.

Testy niefunkcjonalne zajmują się zewnętrznym zachowaniem oprogramowania i w większości wypadków wykorzystują techniki czarnoskrzynkowe.

**Typy testów niefunkcjonalnych:**
* testowanie wydajnościowe
* testowanie obciążeniowe
* testowanie przeciążeniowe
* testowanie użyteczności
* testowanie pielęgnowalności
* testowanie niezawodności
* testowanie przenaszalności (RWD)

#### Testowanie strukturalne (testowanie struktury/architektury systemu)

Testy strukturalne (białoskrzynkowe) można wykonywać na każdym poziomie testowania.

**Pokrycie** to stopień, w  jakim struktura została przetstowana przez zestaw testów wyrażony jako odsetek pokrytych elementów. **Pokrycie mozna mierzyć za pomocą narzędzi. **

#### Testowanie związane ze zmianami: testowanie potwierdzające oraz regresywne

Testy, które mają być stosowane w testowaniu potwierdzającym i regresywnym muszą być powtarzalne.

<br>
**TESTY POTWIERDZAJĄCE (RETESTY)** - Po wykryciu i naprawieniu defektu, powinien zostać wykonany retest, żeby potwierdzić usunięcie usterki.

**TESTY REGRESYWNE** to powtórzenie testow na już przetestowanym programie wykonywane po modyfikacjach, żeby wykryć nowe usterki lub usterki odsłonięte na skutek wykonanych zmian. Testy regresywne wykonuje się po zmianach w oprogramowaniu. Są dobrymi kandydatami do automatyzacji.

Testy regresywne można wykonywać na wszystkich poziomach testów i dla wszystkich typów testów: funkcjonalnych, niefunkcjonalnych i strukturalnych.

#### Testowanie pielęgnacyjne

Testowanie pielęgnacyjne wykonuje się na działającym systemie na skutek modyfikacji, migracji lub złomowania oprogramowania lub systemu.

Modyfikacjami mogą być:
* planowane ulepszenia
* poprawki lub naprawy awaryjne
* zmiany środowiska (planowanie podniesienie wersji systemu operacyjnego, bazy danych lub oprogramowania z półki albo łaty zabezpieczeń systemu operacyjnego)


**Analiza wpływu** - określenie jaki wpływ na istniejący system mogą mieć zmiany, nazywamy analizą wpływu. Stosuje się ja, aby ustalić zakres testów regresywnych. Analiza wpływu może zostać użyta do wybrania zestawu testów regresyjnych.

### Statyczne techniki testowania

**Typy technik testowania**
1. Przeglądy
2. Analiza statyczna
3. Testy dynamiczne

**Techniki statyczne** polegają na sprawdzeniu ręcznym (przeglądy) lub analizie automatycznej (analiza statyczna) kodu lub innych dokumentów projektowych bez uruchamiania kodu. Wykrywają usterki, nie awarie.

#### Przeglądy

**Przeglądy**: mogą im podlegać wszystkie produkty procesu wytwarzania oprogramowania: specyfikacja wymagań, projekt, kod, plany testów, specyfikacja testów, przypadki testowe, skrypty testowe, podręcznik użytkownika oraz strony webowe.

**Główne korzyści z wykonywania przeglądów**:
* wczesne wykrycie i naprawa usterek
* zwiększenie produktywności produkcji oprogramowania
* redukcja czasu produkcji oprogramowania
* zmniejszenie kosztów i czasu testowania
* ogólne zmniejszenie kosztu wytwarzania i użytkowania oprogramowania
* zmniejszenie liczby usterek
* usprawnienie komunikacji

**Typowe usterki, które łatwo wykryć w testach statycznych:**
* odchylenia od standardów
* usterki w wymaganiach
* usterki w projekcie
* niedostateczna pielęgnowalność
* nieprawidłowe specyfikacje interfejsów


**Kroki przeglądu formalnego**
  1. planowanie
  2. rozpoczęcie
  3. przygotowanie indywidualne
  4. kontrola/ocena/zapisanie wyników (spotkanie przeglądowe)
  5. poprawki
  6. zakończenie


  **Role uczestników przeglądów**
  * Kierownik
  * Moderator
  * Autor
  * Przeglądajacy
  * Protokólant


  **Typy przeglądów**
* Przegląd nieformalny
* Przejrzenie
* Przegląd techniczny
* Inspekcja

#### Analiza statyczna przy pomocy narzędzi

Cel analizy statycznej: wykrycie usterek w kodzie programu lub w modelach bez uruchamiania oprogramowania.

**Analiza statyczna zwykle wykrywa następujące typy usterek:**
* odwołanie do niezainicjalizowanej zmiennej
* niespójne interfejsy między modułami
* niewykorzystane lub niepoprawnie zadeklarowane zmiennej
* martwy kod
* brakująca albo błędna logka (pętle potencjalnie nieskończone)
* zbyt skomplikowane konstrukcje
* naruszenie standardów kodowania
* słabe punkty zabezpieczeń
* naruszenie reguł składni kodu i modeli programowania

### Proces rozwoju testów


1. **Analiza testów**: przegląd dokumentacji podstawy testów
2. **Wybór technik projektowania testów**
3. **Projektowanie testów**: tworzenie i opisanie przypadków testowych i danych testowych.
4. **Stworzenie procedór testowych**: priorytetyzacja wykonania przypadków testowych
5. **Stworzenie harmonogramu testowego**: porządek wykonania procedur testowych

**Podczas analizy testów**, przeglądana jest dokumentacja podstawy testów w celu określenia co należy przetestować, czyli warunków testowych.

Aby wybrać techniki projektowania testów, które zostaną użyte, podczas analizy stosowane jest szczegółowe podejście do testów oparte między innymi na analizie ryzyka.

**Podczas projektowania testów** tworzy się i opisuje przypadki testowe i dane testowe.

**Przypadek testowy** składa się ze:
* zbioru wartości wejściowych
* warunków wstępnych
* oczekiwanych wyników (od strony klienta), powinnym być zdefiniowane przed wykonaniem testów
* warunków zakończenia (od strony systemu) utworzonych, aby pokryć pewne cele twstów lub warunki testowe

**Procedura testowa** zawiera kolejność działań podczas wykonania testu. Jest to poukładany, spriorytetyzowany zbiór przypadków testowych.

Procedury testowe i automatyczne skrypty testowe są następnie układane w **harmonogram wykonania testów**.


### Kategorie technik projektowania testów

**Klasyczny podział**:
1. **Techniki czarnoskrzynkowe** (oparte na specyfikacji). Z definicji nie wykorzystują żadnych informacji o strukturze wewnętrznej testowanego modułu lub systemu.
2. **Techniki białoskrzynkowe** (strukturalne, oparte na strukturze)
3. Techniki operate na doświadczeniu


Cechy wspólne technik projektowania testów opartych na specyfikacji:
* w specyfikacji problemu do rozwiązania, oprogramowania lub jego komponentów używane są modele
* z tych modelu można, w sposób usystematyzowany, wywodzić przypadki testowe

Cechy wspólne technik projektowania testów opartych na strukturze:
* do tworzenia przypadków testowych, wykorzystywana jest wiedza o tym jak oprogramowanie jest skonstruowane, np. kod źródłowy
* można mierzyć stopień pokrycia istniejących przypadków testowych, można w sposób usystematyzowany
 tworzyć nowe przypadki testowe w celu zwiększenia pokrycia

Cechy wspólne technik projektowania testów opartych na doświadczeniu
* do tworzenia przypadków testowych wykorzystywne jest doświadczenie ludzi

#### Techniki oparte na specyfikacji lub czarnoskrzynkowe
<br>
**Techniki czarnoskrzynkowe:**
* podział na klasy równoważności
* analiza wartości brzegowych
* testowanie w oparciu o tablicę decyzyjną
* testowanie przejść pomiędzy stanami
* testowanie w oparciu o przypadki użycia

**Podział na klasy równoważności** <br>
W technice podziału na klasy równoważności wejścia do programu lub systemu są dzielone na grupy, które powodują podobne zachowanie oprograowania. Klasy równoważności można znaleźć dla **danych poprawnych** (wartości, które powinny zostać zaakceptowane) oraz **niepoprawnych** (wartości, które powinny zostać odrzucone). Klasy równoważności można znaleźć również dla **wyjść, wartości wewnętrznych, wartości zależnych od czasu oraz parametrów interfejsów.**

**Minimum i maksimum klasy równoważności to jej wartości brzegowe**

Wartość brzegowa to wartość znajdująca się wewnątrz, pomiędzy lub tuż przy granicy danej klasy równoważnośc

Przykład:
    - rejestracja dziecka w przedziale wiekowym 0 – 18:
testowane wartości brzegowe: {-1, 0, 1, 17, 18, 19}

**Testowanie w oparciu o tablicę decyzyjną** <br>
Tablice decyyzyjne są dobrym sposobem na uchwycenie wymagań na system, które zawierają zależności logiczne, oraz na udokumentowanie wewnętrznej budowy systemu. Mogą być używane do zapisywanie złożonych reguł biznesowych.

Warunki wejściowe oraz zachowanie systemu często muszą być zapisane jako prawda lub fałsz (boolean).

**Testowanie przejść między stanami**

Tabela stanów pokazuje zależności pomiędzy stanami oraz wejściami i może uwypuklić przejscia nieprawidłowe.

Przejścia 0-przełącznikowe (bez pośrednich stanów) <br>
Przejścia 1-przełącznikowe (1 pośredni stan)

Testowanie przejść między stanami jest często używane w testowaniu oprogramowania wbudowanego oraz ogólnie w automatyce.

**Testowanie w oparciu o przypadki użycia**

Testy można zaprojektować na podstawie przypadków użycia.

 **Przypadek użycia** opisuje interakcje pomiędzy aktorami (użytkownikami lub systemami), które powodują powstanie wyniku wartościowego z punktu widzenia użytkownika lub klienta.

Przypadki użycia zwykle posiadają **scenariusz główny** (tj. najbardziej prawdopodobny) oraz czasami **scenariusze poboczne**.

Każdy przypadek użycia zaczyna się warunkami wstępnymi i kończy warunkami końcowymi.

#### Techniki oparte na strukturze lub białoskrzynkowe

Testowanie oparte na strukturze (białoskrzybkowe) bazuje na rozpoznanej strukturze oprogramowania lub systemu.

Strukturą może być:
* w testach modułowych jest to kod, jego instrukcje, decyzje, rozgałęzienia lub nawet rozróżnialne ścieżki
* w testach integracyjnych strukturą może być hierarchia wywołań (diagram, który pokazuje jak moduły wywołują inne moduły)
* w testach systemowych strukturą może być budowa menu, proces biznesowyy lub struktura strony webowej


3 strukturalne techniki projektowania testów związane z pokryciem kodu, bazujące na instrukcjach, decyzjach i rozgałęzieniach:
1. Testowanie i pokrycie instrukcji
2. Testowanie i pokrycie decyzji

Pokrycie decyzji:
liczba wyników decyzji pokrytych/zaprojektowane lub wykonane przypadki testowe/liczba wszystkich wyników decyzji, znajdujących się w testowanym kodzie

Testowanie decyzji jest jedną z form testowania przepływu sterowania, ponieważ podąża za konkretnym przepłuywem sterowania przez punkty decyzyjne.

100% pokrycia decyzji gwarantuje 100% pokrycia instrukcji, ale nie na odwrót.

3. Inne techniki oparte na strukturze: pokrycie warunków lub wielokrotne pokrycie warunków


### 5.1 Organizacja testów

**Plusy i minusy niezależnego testowania** <br>
Plusy: brak uprzedzeń, widzą inne usterki <br>

Minusy: izolacja od deweloperów, mogą być postrzegani jako wąskie gardło

Tester a lider (kierownik testów)

#### 5.2 Planowanie i szacowanie testów

**Czynności związane z planowaniem testów**:

**Kryteria wejścia**

Kryteria wejścia definiują warunki pozwalające na rozpoczęcie testów na początku poziomu testów lub, gdy zbiór testów jest gotowy do wykonania.

Kryteria wejścia zwykle mogą zawierać następujące zagadnienia:
* dostępność i gotowość środowiska testowego
* gotowość narzędzi testowych w środowisku testowym
* dostępność testowalnego kodu
* dostępność danych testowych

#### Ryzyko a testowanie

** Obszary ryzyka projektowego**
* czynniki organizacyjne:
  * braki w umiejętnościach, szkoleniach lub personelu
  * problemy kadrowe
  * problemy polityczne: problemy z testerami komunikującymi swoje potrzeby oraz wyniki testów
  * brak reakcji zespołu w związku z informacjami pozyskanymi podczas testów i przeglądów
  * nieprawidłowe nastawienie i oczekiwanie od testowania
* problemy techniczne
  * problemy ze zdefiniowaniem poprawnych wymagań
  * stopień, w jakim wymagania mogą zostać spełnione przy istniejących ograniczeniach
  * środowisko testowe niegotowe na czas
  * spóźniona konwersja danych, planowanie migracji oraz rozwój i testowanie narzędzi do migracji i konwersji danych
  * niska jakość projektu, kodu, danych konfiguracyjnych, danych testowych i testów
* problemy z dostawcami
  * niewywiązywanie się dostawców ze zobowiązań
  * problemy z kontraktami
