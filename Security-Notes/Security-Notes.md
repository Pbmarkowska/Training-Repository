### Basics of Security Testing

OWASP - Open Web Application Security Project

ASVC - Application Security Verification Standard

Standard weryfikowania bezpieczeństwa aplikacji

**Poziomy weryfikacji bezpieczeństwa aplikacji:**

0 Pobieżny <br>
1 Oportunistyczny - przeznaczony dla wszystkich programów <br>
2 Standardowy - przeznaczony dla aplikacji, które zawierają dane wymagające ochrony <br>
3 Zaawansowany - przeznaczony dla najbardziej krytycznych aplikacji - takich, które wykonują transakcje znacznej wartości, zawierają wrażliwe dane, a także innych aplikacji, które wymagają najwyższego poziomu zaufania.

**Poziom 1: Oportunistyczny**

Aplikacja osiąga poziom 1 ASVS, jeśli odpowiednio chroni przed lukami w zabezpieczeniach aplikacji, które są łatwe do odkrycia oraz są zaware w OWASP Top 10 i innych podobnych listach kontrolnych.

Poziom 1 jest zwykle odpowiedni dla aplikacji, dla których wystarczający jest niski poziom zaufania dla prawidłowego stosowania mechanizmów bezpieczeństwa.  

**Poziom 2: Standardowy**

Aplikacja osiąga poziom 2 ASVS w przypadku, gdy właściwie chroni przed większością obecnych ryzyk dotyczących oprogramowania.

Poziom 2 zapewnia, że mechanizmy bezpieczeństwa są wdrożone, skuteczne, oraz są wykorzystywane wewnątrz aplikacji. Poziom 2 jest zazwyczaj właściwy dla aplikacji, które obsługują istotne transakcje biznesowe - włączając w to przetwarzanie informacji medycznych, informacji, które realizują funkcje wrażliwe lub krytyczne dla biznesu, a także takie, które przetwarzają inne zasoby wymagające ochrony.

**Poziom 3: Zaawansowany**

Poziom 3 jest najwyższym poziomem weryfikacji w ramach ASVSC. Jest zarezerwowany dla aplikacji, które wymagają szczególnego poziomu weryfikacji mechanizmów bezpieczenstwa, takich jak te, które można znaleźć w zastosowaniach wojskowych, ochronie zdrowia i bezpieczeństwa publicznego, ochronie infrastruktury krytycznej itp.

Aplikacja znajdująca się na Poziomie 3 ASVS wymaga bardziej dogłębnej analizy, architektury, kodowania i testowania niż na pozostałych poziomach.

**Jaka jest bezpieczna aplikacja?**
* **Składa się z modułów** (w celu ułatwienia jej elastyczności, skalowalności, a przede wszytskim stosowania kolejnych warstw zabezpieczeń).
  * **Każdy moduł** (wydzielony w sposób fizyczny i/lub wykorzystując połączenia siecowe) **dba o poprawność własnych wymagań bezpieczeństwa** (tzw. wielowartstwowa ochronę - *defence in depth*), **które muszą być następnie właściwie udokumentowane**.
* Wymagania obejmują zabezpieczenia zapewniające **poufność (np. szyfrowanie)**, **integralność** (np. transakcje, walidacja wejścia), **dostępność** (np. sprawna obsługa obciążeń - *handling load gracefully*), **uwierzytelnianie** (w tym między systemami), **niezaprzeczalność**, **autoryzację** i **audyt**. 
