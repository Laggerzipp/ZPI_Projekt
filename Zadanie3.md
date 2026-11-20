# ZADANIE 3: PLANOWANIE PROJEKTU I SYMULACJA SPRINTU

## Projekt: FuelRadar

**Skład zespołu:**
- Uczestnik 1
- Denys Liashenko
- Uczestnik 3

**Technologie:**
- Frontend: React
- Backend: Node.js
- Narzędzie do zarządzania projektem: Jira
- Planowana długość sprintu: 2 tygodnie
- Planowany czas realizacji MVP: 12 tygodni

---

# CZĘŚĆ A. PRODUCT BACKLOG I ROADMAPA

## 1. Zakres MVP

Celem pierwszej wersji systemu FuelRadar jest umożliwienie kierowcom porównywania rzeczywistych kosztów tankowania na podstawie cen paliw i dostępnych rabatów.

MVP będzie obejmować następujące funkcjonalności:

1. Wybór rodzaju paliwa.
2. Określenie planowanej liczby litrów.
3. Wyszukiwanie stacji paliw w wybranym regionie.
4. Przeglądanie cen paliw.
5. Wprowadzanie posiadanych programów lojalnościowych.
6. Automatyczne obliczanie kosztu tankowania z uwzględnieniem warunków rabatowych.
7. Sortowanie ofert według rzeczywistego kosztu tankowania.
8. Wyświetlanie źródła danych i daty ostatniej aktualizacji.

MVP będzie początkowo ograniczone do jednego regionu pilotażowego.

### Funkcjonalności wyłączone z MVP

Ze względu na ograniczony czas realizacji następujące funkcjonalności zostaną odłożone na późniejsze etapy:

- Aplikacja mobilna na Android i iOS.
- Uwzględnianie kosztów dojazdu do stacji.
- Zaawansowane rekomendacje oparte na sztucznej inteligencji.
- Konta dla właścicieli stacji paliw.
- Rozbudowany system zarządzania flotą pojazdów.
- Powiadomienia o zmianach cen.
- Obsługa wielu regionów jednocześnie.

## 2. Epiki Product Backlog

### EPIC 1 – Fuel Station Search

**Cel:** Umożliwienie użytkownikom wyszukiwania stacji paliw w wybranym regionie.

Zakres:
- Wybór lokalizacji.
- Wybór rodzaju paliwa.
- Określenie liczby litrów.
- Wyświetlanie listy dostępnych stacji.

### EPIC 2 – Fuel Price Comparison

**Cel:** Umożliwienie porównywania kosztów tankowania na różnych stacjach.

Zakres:
- Pobieranie cen paliw.
- Obliczanie kosztu tankowania.
- Sortowanie ofert według ceny końcowej.
- Wyświetlanie szczegółów cenowych.

### EPIC 3 – Loyalty Programs & Discounts

**Cel:** Uwzględnianie indywidualnych programów lojalnościowych i rabatów użytkowników.

Zakres:
- Wybór posiadanych programów lojalnościowych.
- Odczytywanie warunków promocji.
- Uwzględnianie limitów rabatowych.
- Obliczanie rzeczywistej wartości rabatu.

### EPIC 4 – Offers & Data Management

**Cel:** Zapewnienie poprawności i aktualności danych prezentowanych w aplikacji.

Zakres:
- Pobieranie danych z zewnętrznych źródeł.
- Przechowywanie informacji o cenach.
- Przechowywanie informacji o promocjach.
- Rejestrowanie źródeł i dat aktualizacji.
- Oznaczanie nieaktualnych danych.

### EPIC 5 – User Interface & System Integration

**Cel:** Zapewnienie przejrzystego interfejsu oraz prawidłowej komunikacji między frontendem i backendem.

Zakres:
- Implementacja interfejsu React.
- Implementacja API w Node.js.
- Integracja modułów systemu.
- Obsługa błędów.
- Testowanie i poprawa użyteczności.

## 3. Szczegółowe Historyjki Użytkownika

Każdy z trzech członków zespołu przygotowuje dwie szczegółowe historyjki użytkownika.

### UCZESTNIK 1 – Wyszukiwanie stacji paliw

#### US-01 – Wyszukiwanie stacji według lokalizacji

**Epic:** EPIC 1 – Fuel Station Search

**Opis:**

System powinien umożliwiać użytkownikowi wyszukiwanie stacji paliw na podstawie wybranej lokalizacji. Użytkownik powinien otrzymać listę stacji znajdujących się w obsługiwanym obszarze.

**User Story:**

Jako kierowca chcę wyszukiwać stacje paliw według lokalizacji, aby znaleźć dostępne miejsca tankowania w interesującym mnie obszarze.

**Kryteria akceptacji:**

1. Użytkownik może wskazać lokalizację wyszukiwania.
2. System zwraca listę stacji znajdujących się w obsługiwanym regionie.
3. Każda stacja posiada nazwę oraz informację o lokalizacji.
4. W przypadku braku wyników system wyświetla odpowiedni komunikat.
5. System informuje użytkownika, jeżeli lokalizacja nie jest obsługiwana.

**Priorytet:** High

**Story Points:** 5

**Refinement:**

- Przygotowanie struktury danych stacji paliw.
- Zaprojektowanie endpointu API w Node.js.
- Implementacja formularza wyszukiwania w React.
- Przygotowanie przykładowych danych testowych.
- Obsługa pustych wyników i błędów API.

#### US-02 – Wybór rodzaju paliwa i liczby litrów

**Epic:** EPIC 1 – Fuel Station Search

**Opis:**

System powinien umożliwiać określenie rodzaju paliwa oraz planowanej ilości litrów, aby porównanie ofert odpowiadało potrzebom konkretnego tankowania.

**User Story:**

Jako kierowca chcę wybrać rodzaj paliwa i planowaną liczbę litrów, aby otrzymać porównanie ofert odpowiadające mojemu zapotrzebowaniu.

**Kryteria akceptacji:**

1. Użytkownik może wybrać rodzaj paliwa spośród rodzajów obsługiwanych przez system.
2. Użytkownik może wprowadzić planowaną liczbę litrów.
3. System nie akceptuje wartości mniejszych lub równych zero.
4. System nie akceptuje niepoprawnych danych liczbowych.
5. Wybrane parametry są przekazywane do modułu porównywania ofert.

**Priorytet:** High

**Story Points:** 3

**Refinement:**

- Przygotowanie formularza w React.
- Walidacja danych wejściowych.
- Określenie obsługiwanych rodzajów paliwa.
- Przekazanie parametrów do backendu.
- Testowanie poprawnych i niepoprawnych wartości.

### Denys Liashenko – Obliczanie kosztów i rabatów

#### US-03 – Obliczanie rzeczywistego kosztu tankowania

**Epic:** EPIC 2 – Fuel Price Comparison

**Opis:**

System powinien obliczać całkowity koszt tankowania na podstawie ceny jednostkowej paliwa, planowanej liczby litrów oraz dostępnych rabatów.

**User Story:**

Jako kierowca chcę automatycznie obliczać rzeczywisty koszt tankowania, aby wiedzieć, ile faktycznie zapłacę na wybranej stacji.

**Kryteria akceptacji:**

1. System pobiera cenę jednostkową paliwa.
2. System uwzględnia planowaną liczbę litrów.
3. System uwzględnia rabat, jeżeli użytkownik spełnia warunki promocji.
4. System respektuje maksymalną liczbę litrów objętych rabatem.
5. System oblicza całkowity koszt tankowania.
6. System wyświetla koszt przed zastosowaniem rabatu i po jego zastosowaniu.
7. Wynik obliczeń jest przedstawiany w złotych z dokładnością do dwóch miejsc po przecinku.

**Priorytet:** Highest

**Story Points:** 8

**Refinement:**

- Opracowanie algorytmu obliczania kosztu tankowania.
- Implementacja logiki biznesowej w Node.js.
- Obsługa rabatów procentowych i kwotowych, jeżeli będą obsługiwane przez dane promocji.
- Uwzględnianie limitów ilościowych rabatu.
- Przygotowanie testów jednostkowych.
- Weryfikacja poprawności wyników na przykładach obliczeniowych.

#### US-04 – Sortowanie ofert według rzeczywistego kosztu

**Epic:** EPIC 2 – Fuel Price Comparison

**Opis:**

System powinien umożliwiać sortowanie dostępnych stacji według całkowitego kosztu planowanego tankowania po uwzględnieniu dostępnych rabatów.

**User Story:**

Jako kierowca chcę zobaczyć ranking stacji według rzeczywistego kosztu tankowania, aby szybko wybrać najbardziej opłacalną ofertę.

**Kryteria akceptacji:**

1. System wyświetla listę porównywanych stacji.
2. Każda oferta zawiera obliczony koszt tankowania.
3. Oferty są domyślnie sortowane od najniższego kosztu do najwyższego.
4. System poprawnie uwzględnia rabaty w rankingu.
5. Oferty bez wystarczających danych do obliczenia kosztu nie są prezentowane jako zweryfikowane rekomendacje.
6. W przypadku jednakowego kosztu system prezentuje obie oferty.

**Priorytet:** High

**Story Points:** 5

**Refinement:**

- Przygotowanie struktury wyników porównania.
- Implementacja sortowania po stronie backendu.
- Wyświetlanie rankingu w React.
- Obsługa braku danych.
- Testy poprawności kolejności wyników.

### UCZESTNIK 3 – Programy lojalnościowe i aktualność danych

#### US-05 – Wybór posiadanych programów lojalnościowych

**Epic:** EPIC 3 – Loyalty Programs & Discounts

**Opis:**

System powinien umożliwiać użytkownikowi wskazanie programów lojalnościowych, z których może korzystać podczas tankowania.

**User Story:**

Jako kierowca chcę wskazać posiadane programy lojalnościowe, aby system uwzględniał tylko promocje dostępne dla mnie.

**Kryteria akceptacji:**

1. System wyświetla listę obsługiwanych programów lojalnościowych.
2. Użytkownik może wybrać jeden lub więcej programów.
3. Użytkownik może zmienić wcześniej dokonany wybór.
4. System uwzględnia wyłącznie promocje powiązane z wybranymi programami.
5. W przypadku braku wybranych programów system uwzględnia tylko promocje ogólnodostępne.
6. System nie wymaga podawania haseł do zewnętrznych aplikacji lojalnościowych.

**Priorytet:** High

**Story Points:** 5

**Refinement:**

- Przygotowanie listy obsługiwanych programów.
- Opracowanie modelu danych programów lojalnościowych.
- Implementacja wyboru programów w React.
- Przekazywanie informacji do backendu.
- Testowanie różnych kombinacji programów.

#### US-06 – Wyświetlanie aktualności cen i promocji

**Epic:** EPIC 4 – Offers & Data Management

**Opis:**

System powinien prezentować źródło informacji o cenach paliw oraz datę ostatniej aktualizacji danych.

**User Story:**

Jako kierowca chcę sprawdzić źródło i datę aktualizacji ceny paliwa, aby ocenić wiarygodność prezentowanej oferty.

**Kryteria akceptacji:**

1. Każda oferta zawiera informację o źródle danych.
2. System przechowuje datę i godzinę ostatniej aktualizacji ceny.
3. Ceny starsze niż 48 godzin są oznaczane jako nieaktualne.
4. System nie przedstawia nieaktualnych cen jako potwierdzonych aktualnych danych.
5. Użytkownik może rozpoznać, które oferty mają potwierdzoną aktualność danych.

**Priorytet:** High

**Story Points:** 5

**Refinement:**

- Przygotowanie modelu danych cen i promocji.
- Dodanie pól źródła i czasu aktualizacji.
- Implementacja logiki sprawdzania aktualności.
- Wyświetlanie odpowiednich oznaczeń w React.
- Testowanie danych aktualnych i starszych niż 48 godzin.

## 4. Pozostałe elementy Product Backlog

Poniższe zadania będą znajdować się w Jira jako dodatkowe historyjki lub zadania techniczne. Nie wymagają pełnego opisu na obecnym etapie.

| ID | Nazwa zadania | Typ | Priorytet |
|---|---|---|---|
| US-07 | Wyświetlanie szczegółów stacji paliw | Story | Medium |
| US-08 | Wyświetlanie warunków promocji | Story | High |
| US-09 | Obsługa błędów podczas pobierania danych | Story | High |
| US-10 | Panel administracyjny ofert | Story | Medium |
| US-11 | Filtrowanie ofert według rodzaju paliwa | Story | Medium |
| US-12 | Zgłaszanie nieprawidłowych danych | Story | Low |
| TASK-01 | Konfiguracja projektu React | Task | High |
| TASK-02 | Konfiguracja serwera Node.js | Task | High |
| TASK-03 | Przygotowanie bazy danych | Task | High |
| TASK-04 | Przygotowanie dokumentacji API | Task | Medium |
| TASK-05 | Testy bezpieczeństwa API | Task | High |
| TASK-06 | Testy integracyjne systemu | Task | High |
| TASK-07 | Przygotowanie środowiska wdrożeniowego | Task | Medium |

---

## 5. Roadmapa projektu

Planowana realizacja MVP potrwa 12 tygodni, czyli około 3 miesięcy.

Przyjmujemy sześć sprintów, z których każdy trwa dwa tygodnie.

### Harmonogram Epików

| Epic | Sprinty | Okres | Cel |
|---|---|---|---|
| EPIC 5 – User Interface & System Integration | Sprint 1–2 | Tyg. 1–4 | Przygotowanie środowiska i podstawowej architektury |
| EPIC 1 – Fuel Station Search | Sprint 2–3 | Tyg. 3–6 | Wyszukiwanie stacji i parametry tankowania |
| EPIC 3 – Loyalty Programs & Discounts | Sprint 2–4 | Tyg. 3–8 | Obsługa programów i rabatów |
| EPIC 2 – Fuel Price Comparison | Sprint 1–4 | Tyg. 1–8 | Obliczanie i porównywanie kosztów |
| EPIC 4 – Offers & Data Management | Sprint 3–5 | Tyg. 5–10 | Integracja i kontrola danych |
| EPIC 5 – User Interface & System Integration | Sprint 5–6 | Tyg. 9–12 | Integracja końcowa, testy i przygotowanie MVP |

### Wykres Gantta – wyłącznie Epiki

| Epic | 1–2 tydz. | 3–4 tydz. | 5–6 tydz. | 7–8 tydz. | 9–10 tydz. | 11–12 tydz. |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| EPIC 1 – Search | | █ | █ | | | |
| EPIC 2 – Comparison | █ | █ | █ | █ | | |
| EPIC 3 – Loyalty | | █ | █ | █ | | |
| EPIC 4 – Data Management | | | █ | █ | █ | |
| EPIC 5 – UI & Integration | █ | █ | | | █ | █ |

Harmonogram ma charakter planistyczny. Nie oznacza, że poszczególne Epiki będą realizowane całkowicie niezależnie. Niektóre prace będą prowadzone równolegle.

---

# CZĘŚĆ B. PLANOWANIE SPRINTU 1

## 1. Cel Sprintu

Sprint 1 potrwa dwa tygodnie.

**Cel Sprintu:**

W ciągu dwóch tygodni zespół FuelRadar opracuje koncepcję i zweryfikuje techniczną wykonalność algorytmu obliczającego rzeczywisty koszt tankowania z uwzględnieniem rabatów i limitów ilościowych. Rezultatem będzie opisany PoC, zestaw scenariuszy testowych oraz decyzja dotycząca dalszej implementacji algorytmu w systemie.

Cel jest konkretny, mierzalny, osiągalny, istotny biznesowo i określony w czasie.

### Kryteria osiągnięcia celu Sprintu

- Opracowanie algorytmu obliczania kosztu tankowania.
- Uwzględnienie limitu litrów objętych rabatem.
- Przygotowanie minimum 5 przypadków testowych.
- Uzyskanie poprawnych wyników dla wszystkich przypadków testowych.
- Udokumentowanie wyników eksperymentu.
- Przygotowanie rekomendacji dotyczącej dalszej implementacji.

## 2. Proof of Concept (PoC)

### 2.1. Nazwa PoC

Weryfikacja algorytmu obliczania rzeczywistego kosztu tankowania z uwzględnieniem rabatów i ich ograniczeń.

### 2.2. Hipoteza

Zakładamy, że możliwe jest opracowanie algorytmu, który na podstawie ceny paliwa, ilości litrów oraz warunków promocji automatycznie obliczy rzeczywisty koszt tankowania i prawidłowo uwzględni ograniczenia rabatowe.

### 2.3. Parametry eksperymentu

Przykładowe dane wejściowe:

| Parametr | Wartość |
|---|---:|
| Cena bazowa paliwa | 6,20 zł/l |
| Rabat | 0,30 zł/l |
| Planowana ilość paliwa | 50 l |
| Maksymalna ilość objęta rabatem | 30 l |

### 2.4. Oczekiwany wynik

Koszt 30 litrów z rabatem:

30 × (6,20 − 0,30) = 177,00 zł

Koszt pozostałych 20 litrów bez rabatu:

20 × 6,20 = 124,00 zł

Całkowity koszt:

177,00 + 124,00 = 301,00 zł

Koszt bez rabatu:

50 × 6,20 = 310,00 zł

Oszczędność:

310,00 − 301,00 = 9,00 zł

### 2.5. Kryteria sukcesu PoC

PoC zostanie uznany za udany, jeżeli:

1. Algorytm poprawnie obliczy koszt tankowania z rabatem.
2. Algorytm prawidłowo uwzględni maksymalną liczbę litrów objętych promocją.
3. Algorytm nie zastosuje rabatu do litrów przekraczających limit.
4. Wyniki będą zgodne z niezależnymi obliczeniami kontrolnymi.
5. Wszystkie przygotowane scenariusze testowe zakończą się oczekiwanym wynikiem.

Przyjmujemy minimum pięć scenariuszy testowych i 100% poprawnych wyników dla tych scenariuszy.

### 2.6. Koncepcja implementacji

Planowane rozwiązanie będzie oparte na technologii Node.js.

Moduł obliczeniowy otrzyma następujące dane:

- cenę bazową paliwa,
- planowaną liczbę litrów,
- wysokość rabatu,
- maksymalną liczbę litrów objętych rabatem.

Następnie algorytm obliczy liczbę litrów objętych rabatem i liczbę litrów rozliczanych według ceny bazowej.

Wynik zostanie zwrócony w postaci całkowitego kosztu tankowania, kosztu bez rabatu oraz wartości oszczędności.

W kolejnych etapach rezultat będzie przekazywany do frontendowej aplikacji React poprzez API Node.js.

### 2.7. Opis eksperymentu

Zespół przygotuje zestaw przykładowych danych reprezentujących różne warunki promocji.

Następnie dla każdego przypadku zostanie ręcznie obliczony oczekiwany wynik. Rezultat ten zostanie porównany z wynikiem uzyskanym przez przygotowany prototyp algorytmu.

Eksperyment będzie obejmował:

- tankowanie w całości objęte rabatem,
- tankowanie częściowo objęte rabatem,
- tankowanie przekraczające limit rabatowy,
- tankowanie bez dostępnego rabatu,
- niepoprawne wartości wejściowe.

W ramach tego zadania przedstawiamy koncepcję eksperymentu i planowane testy. Nie deklarujemy wykonania działającego prototypu ani uzyskania rzeczywistych wyników implementacji.

### 2.8. Możliwe scenariusze decyzji

**Scenariusz 1 – PoC zakończony sukcesem**

Algorytm prawidłowo oblicza koszty dla wszystkich scenariuszy.

Decyzja: przejście do pełnej implementacji modułu obliczeniowego w backendzie Node.js.

**Scenariusz 2 – PoC zakończony częściowym sukcesem**

Algorytm działa dla podstawowych przypadków, ale występują problemy z bardziej złożonymi warunkami promocji.

Decyzja: uproszczenie obsługiwanych reguł rabatowych w MVP i zaplanowanie dodatkowych testów.

**Scenariusz 3 – PoC zakończony niepowodzeniem**

Algorytm nie zapewnia prawidłowych wyników dla przyjętych scenariuszy.

Decyzja: ponowna analiza modelu danych i logiki obliczeniowej, a następnie przygotowanie alternatywnego rozwiązania przed rozpoczęciem pełnej implementacji.

## 3. Sprint Backlog i szacowanie

Do pierwszego sprintu wybieramy zadania związane z przygotowaniem i weryfikacją PoC.

| ID | Zadanie | Odpowiedzialny | Story Points |
|---|---|---|---:|
| S1-01 | Analiza warunków rabatowych i ograniczeń | Uczestnik 1 | 3 |
| S1-02 | Opracowanie algorytmu obliczania kosztu | Denys Liashenko | 5 |
| S1-03 | Przygotowanie koncepcji modułu Node.js | Denys Liashenko | 3 |
| S1-04 | Przygotowanie scenariuszy testowych | Uczestnik 3 | 3 |
| S1-05 | Opracowanie modelu danych promocji | Uczestnik 1 | 2 |
| S1-06 | Analiza wyników i dokumentacja PoC | Cały zespół | 2 |

**Łączna estymacja: 18 Story Points.**

Estymacja jest wstępnym założeniem zespołu. Po pierwszym sprincie zostanie zweryfikowana na podstawie rzeczywistego postępu prac.

## 4. Definition of Done (DoD)

Definition of Done określa wspólne kryteria jakościowe, które muszą zostać spełnione, aby zadanie w backlogu mogło zostać uznane za ukończone.

W projekcie FuelRadar przyjmujemy następujące kryteria:

1. Zadanie zostało wykonane zgodnie z opisem i wymaganiami.
2. Wszystkie kryteria akceptacji zostały spełnione.
3. Kod jest zgodny z przyjętymi standardami projektu.
4. Kod został sprawdzony przez innego członka zespołu, jeżeli dotyczy zadania programistycznego.
5. Wykonano odpowiednie testy jednostkowe lub funkcjonalne.
6. Nie występują błędy blokujące działanie realizowanej funkcjonalności.
7. Nie są ujawniane hasła, tokeny ani inne dane poufne.
8. Dokumentacja techniczna została zaktualizowana, jeżeli była wymagana.
9. Zmiany zostały zapisane w repozytorium projektu.
10. Zadanie zostało zaktualizowane w Jira i zaakceptowane przez zespół.

W przypadku zadań analitycznych i dokumentacyjnych odpowiednie kryteria jakościowe dotyczą kompletności, poprawności i możliwości weryfikacji przygotowanych materiałów.

---

# 5. ANALIZA PRE-MORTEM

## 5.1. Założenie

Zespół wyobraża sobie sytuację, w której implementacja algorytmu obliczającego rzeczywisty koszt tankowania zakończyła się niepowodzeniem.

Przyczyną może być nieprawidłowe działanie algorytmu, błędna interpretacja warunków promocji, problemy z danymi wejściowymi lub podatności bezpieczeństwa.

Analiza dotyczy wyłącznie PoC, a nie całego projektu FuelRadar.

## 5.2. Możliwe przyczyny niepowodzenia

| ID | Zagrożenie | Prawdopodobieństwo | Skutek |
|---|---|---|---|
| R1 | Nieprawidłowe obliczanie rabatów | Średnie | Wysokie |
| R2 | Błędna interpretacja limitu litrów | Wysokie | Wysokie |
| R3 | Niepoprawne lub brakujące dane wejściowe | Średnie | Średnie |
| R4 | Nieaktualne warunki promocji | Wysokie | Wysokie |
| R5 | Manipulacja parametrami zapytania API | Niskie | Wysokie |
| R6 | Nieprawidłowe zaokrąglanie wyników | Średnie | Średnie |

## 5.3. Szczegółowa analiza ryzyka

### R1 – Nieprawidłowe obliczanie rabatów

**Problem:** Algorytm może nieprawidłowo obliczać koszt tankowania po zastosowaniu rabatu.

**Konsekwencje:** Użytkownik może otrzymać błędną informację o rzeczywistym koszcie tankowania.

**Działania zapobiegawcze:**
- Przygotowanie niezależnych obliczeń kontrolnych.
- Testowanie różnych wartości rabatów.
- Wykonanie testów jednostkowych.
- Weryfikacja wyników przez drugiego członka zespołu.

### R2 – Błędna interpretacja limitu litrów

**Problem:** System może zastosować rabat do większej liczby litrów, niż przewiduje promocja.

**Konsekwencje:** Ranking stacji może przedstawiać nieprawidłowe rekomendacje.

**Działania zapobiegawcze:**
- Jednoznaczne określenie limitów w modelu danych.
- Przygotowanie osobnych przypadków testowych.
- Weryfikacja sytuacji, w której ilość tankowanego paliwa przekracza limit promocji.

### R3 – Niepoprawne dane wejściowe

**Problem:** Użytkownik lub zewnętrzny system może przekazać nieprawidłową cenę, liczbę litrów albo wartość rabatu.

**Konsekwencje:** Algorytm może wygenerować błędny wynik lub zakończyć działanie błędem.

**Działania zapobiegawcze:**
- Walidacja danych po stronie backendu.
- Odrzucanie wartości ujemnych i nieprawidłowych.
- Obsługa wyjątków.
- Testowanie niepoprawnych danych wejściowych.

### R4 – Nieaktualne warunki promocji

**Problem:** System może korzystać z promocji, która została zakończona lub zmieniła warunki.

**Konsekwencje:** Użytkownik może otrzymać rekomendację oferty, z której nie będzie mógł skorzystać.

**Działania zapobiegawcze:**
- Przechowywanie dat obowiązywania promocji.
- Kontrolowanie aktualności danych.
- Oznaczanie niezweryfikowanych ofert.
- Nieprzedstawianie nieaktualnych promocji jako dostępnych.

### R5 – Zagrożenia bezpieczeństwa API

**Problem:** Osoba nieuprawniona może próbować manipulować parametrami przesyłanymi do modułu obliczeniowego.

**Konsekwencje:** Możliwe jest uzyskanie nieprawidłowych wyników, przeciążenie API lub wykorzystanie podatności aplikacji.

**Działania zapobiegawcze:**
- Walidacja danych po stronie serwera.
- Ograniczenie dopuszczalnych wartości parametrów.
- Obsługa błędów bez ujawniania szczegółów wewnętrznych.
- Stosowanie bezpiecznej konfiguracji API.
- Ograniczenie dostępu do funkcji administracyjnych.

### R6 – Nieprawidłowe zaokrąglanie wyników

**Problem:** Operacje na liczbach zmiennoprzecinkowych mogą prowadzić do niedokładności obliczeń finansowych.

**Konsekwencje:** Wynik może różnić się od oczekiwanej kwoty o kilka groszy.

**Działania zapobiegawcze:**
- Stosowanie odpowiedniej reprezentacji wartości pieniężnych.
- Przechowywanie cen w ustalonych jednostkach.
- Zaokrąglanie wyników zgodnie z przyjętymi zasadami.
- Testowanie przypadków z wartościami dziesiętnymi.

## 5.4. Konsekwencje niedostarczenia PoC

Jeżeli zespół nie potwierdzi możliwości prawidłowego obliczania kosztów tankowania, podstawowa wartość biznesowa FuelRadar nie zostanie zrealizowana.

Użytkownicy mogą otrzymywać błędne rekomendacje, co spowoduje utratę zaufania do aplikacji.

W takiej sytuacji zespół powinien ograniczyć zakres obsługiwanych promocji, poprawić model danych lub przeanalizować alternatywną metodę obliczeń.

Nie należy wdrażać niezweryfikowanego algorytmu jako podstawy rankingu ofert.

---

# 6. PODSUMOWANIE

Projekt FuelRadar będzie realizowany w oparciu o metodykę Scrum i narzędzie Jira.

W ramach Product Backlog zdefiniowano pięć Epików oraz szczegółowe historyjki użytkownika odpowiadające głównym funkcjonalnościom systemu.

Każdy członek trzyosobowego zespołu otrzymał odpowiedzialność za przygotowanie dwóch szczegółowych User Stories.

Zakres MVP został ograniczony do funkcjonalności umożliwiających wyszukiwanie stacji paliw, porównywanie cen oraz obliczanie rzeczywistych kosztów tankowania z uwzględnieniem promocji.

Realizacja projektu została zaplanowana na sześć dwutygodniowych sprintów.

Pierwszy sprint będzie poświęcony przygotowaniu i weryfikacji koncepcji PoC, którego celem jest sprawdzenie technicznej wykonalności algorytmu obliczającego rzeczywisty koszt tankowania.

Przeprowadzona analiza Pre-Mortem pozwoliła zidentyfikować najważniejsze zagrożenia związane z poprawnością obliczeń, aktualnością danych i bezpieczeństwem API.

Przyjęty plan umożliwi stopniową realizację MVP oraz ograniczenie ryzyka projektowego.
