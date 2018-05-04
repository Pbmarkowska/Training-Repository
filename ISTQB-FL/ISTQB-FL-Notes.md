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

**Debagowanie** to czynność programistyczna, która znajduje, anazliuje i umożliwia usunięcie przyczyny awarii. Późniejsze testy potwierdzające (retesty) wykonywane przez testera gwarantują, że poprawka rzeczywiście usunęła usterkę.

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

ogólne cele testowania przekształcane są w konkretne warunki testowe i przypadki testowanego

Główne zadania analizy i projektowania testów:

* przeglądanie podstawy testów
* ocena testowalności podstawy testów i przedmiotu testów <br>
* identyfikacja i priorytetyzacja warunków testowych na podstawie analizy elementów testowych, specyfikacji, zachowania i struktury oprogramowania
* projektowanie i priorytetyzacja przypadków testowych wysokiego poziomu
* ustalanie jakie dane testowe są potrzebne dla warunków testowych oraz przypadków testowych
* projektowanie środowiska testowego oraz identyfikacja potrzebnej infrastruktury

* **tworzenie dwukierunkowego śledzenia pomiędzy podstawą testów oraz przypadkami testowymi**

* **implementacja i wykonanie testów**
to czynność, podczas której specyfikowane są procedury i skrypty testowe przez ustawienie przypadków testowych w konkretnej kolejności oraz dolączenie innych informacji potrzebnych do wykonania tstów, konfigurowane jest środowisko testowe oraz są wykonywane testy.

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
* oceninie, czy potrzeba więcej testów lub czy nie powinny zostać zmienione kryteria zakończenia
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

Modele iteracyjno-przyrostowe
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
Polegają na wyszukiwaniu błędów i weryfikacji funkcjonalności oprogramowania, które można **testować oddzielnie**. Można podczas nich użyć zaślepek, sterowników testowych oraz symulatorów.

Testy modułowe mogą zawierać testy funkcjonalności oraz niektórych atrybutów niefunkcjonalnych, takich jak stopień wykorzystania zasobów (np. wycieków pamięci) lub odporności, jak również testy strukturalne (np. pokrycia decyzji).

Testy modułowe zwykle wykonuje się mając dostęp do kodu źródłowego i przy wsparciu środowiska rozwojowego, zwykle angażują prgramistę. Usterki są usuwane jak tylko zostaną wykryte.

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
