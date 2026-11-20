# 1. Wizja i zakres projektu

## 1.1. Problem biznesowy i szanse rynkowe

### Problem biznesowy

Ceny paliw stanowią istotny element kosztów użytkowania samochodu, zarówno dla kierowców indywidualnych, jak i osób wykorzystujących pojazdy w pracy zawodowej. Kierowcy często poszukują możliwości ograniczenia wydatków na tankowanie poprzez wybór stacji oferujących najkorzystniejsze ceny.

Na rynku funkcjonują serwisy umożliwiające porównywanie cen paliw, takie jak PaliwoMapa, BenzynaMAPA czy Fuelio. Dostępne są również aplikacje lojalnościowe poszczególnych sieci paliwowych, oferujące rabaty, kupony oraz promocje okresowe.

Pomimo dostępności takich rozwiązań, porównanie rzeczywistego kosztu tankowania może być dla kierowcy czasochłonne. Wynika to z kilku problemów:

- **Rozproszenie informacji** – ceny paliw i informacje o promocjach mogą znajdować się w różnych serwisach oraz aplikacjach poszczególnych sieci.
- **Zróżnicowane warunki promocji** – rabaty mogą wymagać posiadania określonej aplikacji, aktywowania kuponu, spełnienia minimalnej wartości zakupów lub tankowania określonej ilości paliwa.
- **Ograniczenia rabatów** – promocje mogą obejmować maksymalną liczbę litrów, wybrane rodzaje paliw lub określone dni tygodnia.
- **Nieaktualne informacje** – prezentowane ceny i oferty mogą różnić się od aktualnych warunków obowiązujących na stacji.
- **Brak indywidualnego porównania** – najniższa cena bazowa paliwa nie musi oznaczać najniższego kosztu tankowania po uwzględnieniu promocji dostępnych dla konkretnego kierowcy.

Przykładowo stacja oferująca benzynę w cenie 6,20 zł/l może okazać się korzystniejsza od stacji z ceną 6,05 zł/l, jeżeli kierowca posiada uprawnienie do rabatu 30 groszy na litrze i spełnia jego warunki.

Problemem, który zamierza rozwiązać FuelRadar, jest zatem nie tylko wyszukiwanie najniższych cen paliw, ale przede wszystkim automatyczne ustalanie najkorzystniejszej oferty tankowania na podstawie indywidualnych możliwości skorzystania z promocji.

### Proponowane rozwiązanie

FuelRadar będzie aplikacją internetową umożliwiającą porównywanie kosztów tankowania na stacjach paliw w wybranym obszarze.

Użytkownik będzie mógł określić rodzaj paliwa, planowaną liczbę litrów, lokalizację oraz posiadane programy lojalnościowe. Na podstawie tych informacji system przeanalizuje ceny i dostępne rabaty, a następnie przedstawi ranking stacji według obliczonego kosztu tankowania.

Aplikacja będzie uwzględniała warunki promocji możliwe do jednoznacznego zweryfikowania, np. maksymalną liczbę litrów objętych rabatem czy konieczność posiadania określonego programu lojalnościowego.

Dla zwiększenia przejrzystości każda oferta będzie zawierała informację o źródle danych, dacie ostatniej aktualizacji oraz warunkach zastosowania promocji.

Początkowo system nie będzie uwzględniał dodatkowego kosztu dojazdu do stacji. Funkcjonalność ta zostanie przewidziana jako jeden z przyszłych kierunków rozwoju.

### Szanse rynkowe i przewaga konkurencyjna

FuelRadar będzie konkurować z istniejącymi porównywarkami cen paliw oraz aplikacjami lojalnościowymi sieci stacji.

Serwisy takie jak PaliwoMapa udostępniają informacje o cenach paliw i promocjach, natomiast BenzynaMAPA umożliwia przeglądanie cen stacji oraz oferuje dostęp do danych przez API. Fuelio dodatkowo wspiera monitorowanie kosztów użytkowania pojazdu.

Z tego względu przewagą FuelRadar nie będzie samo wyświetlanie cen lub zbieranie informacji o promocjach, lecz **automatyczne przeliczanie dostępnych ofert na rzeczywisty koszt tankowania dostosowany do sytuacji konkretnego użytkownika**.

Projekt ma szansę usprawnić istniejący proces porównywania ofert poprzez:

- Połączenie informacji o cenach i promocjach w jednym interfejsie.
- Automatyczne obliczanie kosztu tankowania z uwzględnieniem ograniczeń rabatowych.
- Personalizację wyników na podstawie posiadanych programów lojalnościowych.
- Ograniczenie czasu potrzebnego na porównywanie ofert.
- Prezentowanie aktualności danych i warunków promocji, aby użytkownik mógł świadomie ocenić wiarygodność rekomendacji.

Główną grupą docelową będą kierowcy indywidualni, szczególnie osoby regularnie korzystające z samochodu i poszukujące oszczędności.

W dalszych etapach rozwoju potencjalnymi odbiorcami mogą stać się również kierowcy zawodowi, przedsiębiorstwa posiadające floty pojazdów oraz stacje paliw zainteresowane promocją swoich ofert.

Zakładamy, że istnieje zapotrzebowanie na narzędzie upraszczające porównywanie indywidualnych kosztów tankowania. Jest to jednak hipoteza biznesowa, którą należy zweryfikować poprzez analizę konkurencji, testy z potencjalnymi użytkownikami i uruchomienie MVP.

### Wartość biznesowa i społeczna

Podstawową wartością FuelRadar będzie umożliwienie kierowcom podejmowania bardziej świadomych decyzji zakupowych.

**Korzyści dla użytkowników:**
- Potencjalne zmniejszenie wydatków na paliwo.
- Oszczędność czasu dzięki automatycznemu porównywaniu ofert.
- Łatwiejsze korzystanie z dostępnych promocji.
- Większa przejrzystość warunków rabatowych.

**Korzyści dla stacji paliw:**
- Możliwość dotarcia do kierowców poszukujących korzystnych ofert.
- Potencjalne zwiększenie zainteresowania aktualnymi promocjami.
- W przyszłości możliwość publikowania i aktualizowania ofert bezpośrednio w systemie.

**Korzyści dla operatora platformy:**

Rozwój bazy aktywnych użytkowników może w przyszłości umożliwić wprowadzenie modelu biznesowego opartego na wyraźnie oznaczonych ofertach sponsorowanych lub płatnych narzędziach dla stacji paliw.

Ewentualne treści sponsorowane powinny być prezentowane niezależnie od organicznego rankingu opłacalności tankowania, aby zachować wiarygodność rekomendacji.

---

## 1.2. Wizja produktu

**Wizją FuelRadar jest umożliwienie każdemu kierowcy szybkiego i świadomego wyboru najkorzystniejszego miejsca do tankowania poprzez połączenie cen paliw, promocji i indywidualnych uprawnień do rabatów w jednym przejrzystym serwisie.**

Docelowo FuelRadar ma stać się niezależnym narzędziem wspierającym ograniczanie kosztów tankowania, rozwijanym wraz z potrzebami użytkowników i dostępnością wiarygodnych źródeł danych.

---

## 1.3. Główny cel biznesowy zgodny z metodą SMART

### Główny cel biznesowy

**W ciągu 3 miesięcy od uruchomienia MVP aplikacji FuelRadar osiągnąć co najmniej 500 aktywnych użytkowników miesięcznie w wybranym regionie pilotażowym, którzy korzystają z funkcji porównywania kosztów tankowania z uwzględnieniem promocji, w celu zweryfikowania zainteresowania produktem oraz zasadności jego dalszego rozwoju.**

Za aktywnego użytkownika przyjmujemy unikalnego użytkownika, który w ciągu ostatnich 30 dni wykonał przynajmniej jedno kompletne porównanie ofert tankowania.

Region pilotażowy oraz sposób identyfikowania unikalnych użytkowników zostaną ustalone przed uruchomieniem MVP.

### Analiza celu według SMART

| Kryterium | Uzasadnienie |
|---|---|
| **S – Specific (Konkretny)** | Cel dotyczy pozyskania użytkowników aktywnie korzystających z porównywarki FuelRadar w regionie pilotażowym. |
| **M – Measurable (Mierzalny)** | Sukces będzie mierzony liczbą minimum 500 aktywnych użytkowników miesięcznie. |
| **A – Achievable (Osiągalny)** | Ograniczenie zasięgu do jednego regionu, niewielkiego MVP i promocji w lokalnych społecznościach umożliwia podjęcie próby pozyskania takiej liczby użytkowników przez czteroosobowy zespół. |
| **R – Relevant/Realistic (Istotny i realistyczny)** | Pozyskanie użytkowników pozwoli zweryfikować wartość produktu, zanim zespół poniesie większe koszty jego rozwoju. |
| **T – Time-bound (Określony w czasie)** | Cel powinien zostać osiągnięty do końca trzeciego pełnego miesiąca po publicznym uruchomieniu MVP. |

### Uzasadnienie wyboru celu

Na początkowym etapie rozwoju FuelRadar priorytetem nie będzie generowanie przychodów, lecz sprawdzenie, czy proponowane rozwiązanie odpowiada na rzeczywiste potrzeby kierowców.

Osiągnięcie 500 aktywnych użytkowników miesięcznie będzie wstępnym sygnałem zainteresowania produktem. Pozwoli także zebrać dane o sposobie korzystania z aplikacji oraz wskazać funkcjonalności wymagające poprawy.

Cel jest powiązany z koncepcją MVP, ponieważ nie wymaga wdrażania całego planowanego systemu. Skupia się na najważniejszej wartości biznesowej, czyli porównywaniu cen paliw po uwzględnieniu dostępnych rabatów.

Liczba 500 użytkowników stanowi przyjęte założenie projektowe, a jej osiągalność będzie weryfikowana podczas pilotażu.

---

## 1.4. Kluczowe metryki sukcesu (KPI)

Do oceny realizacji głównego celu biznesowego wybrano trzy wskaźniki.

### KPI 1 – Liczba aktywnych użytkowników miesięcznie (MAU)

**Cel: minimum 500 aktywnych użytkowników w trzecim miesiącu od uruchomienia MVP.**

Wskaźnik określa liczbę unikalnych użytkowników, którzy wykonali przynajmniej jedno kompletne porównanie ofert tankowania w ciągu 30 dni.

Pomiar będzie prowadzony za pomocą narzędzia analitycznego rejestrującego zakończone porównania oraz unikalnych użytkowników, z uwzględnieniem wymogów ochrony prywatności.

KPI pozwoli ocenić zainteresowanie główną funkcjonalnością produktu oraz stopień realizacji celu SMART.

### KPI 2 – Wskaźnik powracających użytkowników

**Cel: co najmniej 20% aktywnych użytkowników z drugiego miesiąca ponownie skorzysta z porównywarki w trzecim miesiącu.**

Wskaźnik będzie obliczany jako stosunek liczby użytkowników aktywnych zarówno w drugim, jak i trzecim miesiącu do liczby aktywnych użytkowników w drugim miesiącu, pomnożony przez 100%.

Jego zadaniem będzie sprawdzenie, czy FuelRadar oferuje powtarzalną wartość, a nie jedynie wzbudza jednorazowe zainteresowanie.

### KPI 3 – Skuteczność dostarczania porównywalnych ofert

**Cel: co najmniej 70% zapytań o porównanie tankowania powinno zakończyć się przedstawieniem minimum dwóch stacji z aktualnymi danymi cenowymi i możliwymi do oceny warunkami promocji.**

Na potrzeby MVP za aktualną uznajemy cenę potwierdzoną lub zaktualizowaną w ciągu ostatnich 48 godzin. Jeżeli nie można potwierdzić aktualności danych, system powinien odpowiednio je oznaczyć, a nie przedstawiać jako pewne.

Wskaźnik będzie liczony jako stosunek liczby zapytań spełniających powyższe warunki do wszystkich zakończonych zapytań o porównanie ofert, pomnożony przez 100%.

KPI pozwoli ocenić, czy aplikacja posiada wystarczająco wiarygodne dane, aby użytkownicy mogli regularnie korzystać z jej głównej funkcjonalności.

### Podsumowanie KPI

| Wskaźnik | Wartość docelowa | Termin |
|---|---|---|
| Aktywni użytkownicy miesięcznie (MAU) | ≥ 500 | Koniec 3. miesiąca |
| Powracający użytkownicy | ≥ 20% | Porównanie 2. i 3. miesiąca |
| Skuteczność porównywania ofert | ≥ 70% | Koniec 3. miesiąca |

Przedstawione wartości są założeniami i celami dla pilotażu, a nie wynikami rzeczywistego działania aplikacji.

---

## 1.5. Główne klasy użytkowników i interesariusze

### Klasy użytkowników

W systemie FuelRadar wyróżniono trzy podstawowe klasy użytkowników.

**1. Kierowcy indywidualni**

Stanowią główną grupę docelową aplikacji. Korzystają z samochodów na potrzeby codziennych dojazdów, zakupów i podróży prywatnych.

Ich podstawowym celem jest ograniczenie wydatków na paliwo i szybkie znalezienie korzystnej oferty tankowania bez konieczności przeszukiwania wielu aplikacji.

**2. Kierowcy często korzystający z samochodu**

Są to między innymi przedstawiciele handlowi, kierowcy wykonujący regularne podróże oraz osoby dojeżdżające na duże odległości.

Ze względu na częstotliwość tankowania mogą być szczególnie zainteresowani aktualnością cen, możliwością porównywania różnych lokalizacji oraz przyszłą funkcją uwzględniającą koszt dojazdu.

**3. Administratorzy platformy**

Odpowiadają za jakość i poprawność danych prezentowanych w serwisie.

Do ich zadań należy weryfikowanie promocji, zarządzanie informacjami o stacjach, kontrolowanie nieaktualnych ofert oraz reagowanie na błędy zgłaszane w systemie.

W wersji MVP dostęp do funkcji administracyjnych będzie ograniczony do członków zespołu zarządzającego platformą.

### Interesariusze projektu

| Interesariusz | Oczekiwania i interesy |
|---|---|
| Kierowcy indywidualni | Niskie koszty tankowania, szybkie porównanie ofert, prostota obsługi |
| Kierowcy często tankujący | Aktualność cen, wiarygodne informacje, oszczędność czasu |
| Właściciele i operatorzy stacji paliw | Zwiększenie zainteresowania ofertami i możliwość promowania rabatów |
| Dostawcy danych o cenach paliw | Przestrzeganie warunków licencji, poprawna atrybucja danych i odpowiedzialne korzystanie z API |
| Administratorzy FuelRadar | Utrzymanie jakości danych, bezpieczeństwa i prawidłowego działania systemu |
| Zespół projektowy | Zbudowanie działającego MVP w ograniczonym czasie i budżecie |
| Opiekun projektu / uczelnia | Poprawne zastosowanie metod inżynierii wymagań oraz uzasadnionych decyzji architektonicznych |

Właściciele stacji paliw będą początkowo interesariuszami zewnętrznymi. Możliwość samodzielnego zarządzania promocjami przez stacje zostanie rozważona na późniejszym etapie rozwoju.

---

## 1.6. Persony użytkowników

### Persona 1 – Michał, kierowca indywidualny

**Wiek:** 24 lata

**Zawód:** Student, pracujący dorywczo

**Charakterystyka:**

Michał codziennie korzysta z samochodu, dojeżdżając na uczelnię i do pracy. Dysponuje ograniczonym budżetem, dlatego zwraca uwagę na ceny paliw i chętnie korzysta z promocji oferowanych przez stacje.

Posiada konta w kilku programach lojalnościowych, ale nie zawsze pamięta, jakie rabaty są aktualnie dostępne.

**Cele:**
- Znalezienie najtańszej dostępnej oferty tankowania w okolicy.
- Ograniczenie miesięcznych wydatków na paliwo.
- Wykorzystanie posiadanych programów lojalnościowych.
- Porównanie ofert w krótkim czasie.

**Frustracje:**
- Konieczność otwierania kilku aplikacji w celu sprawdzenia promocji.
- Niejasne warunki niektórych rabatów.
- Brak pewności, czy promocja rzeczywiście się opłaca.
- Nieaktualne ceny wyświetlane w serwisach internetowych.

**Potrzeby wobec systemu:**

Michał oczekuje prostego interfejsu, w którym będzie mógł określić rodzaj paliwa, liczbę litrów i posiadane programy lojalnościowe. Aplikacja powinna automatycznie przedstawić najkorzystniejsze oferty wraz z ostateczną ceną tankowania.

### Persona 2 – Tomasz, kierowca często podróżujący

**Wiek:** 42 lata

**Zawód:** Przedstawiciel handlowy

**Charakterystyka:**

Tomasz regularnie podróżuje samochodem między miastami w ramach obowiązków zawodowych. Tankuje kilka razy w miesiącu, a koszty paliwa stanowią istotny element jego wydatków związanych z eksploatacją pojazdu.

Nie chce poświęcać dużo czasu na analizowanie promocji, ale zależy mu na uzyskiwaniu sprawdzonych informacji.

**Cele:**
- Szybkie znalezienie korzystnej cenowo stacji paliw.
- Unikanie niepotrzebnych wydatków podczas częstych tankowań.
- Korzystanie z aktualnych promocji.
- W przyszłości uwzględnianie kosztu dojazdu do stacji.

**Frustracje:**
- Nieaktualne dane cenowe.
- Oferty, których warunki okazują się trudne do spełnienia.
- Konieczność samodzielnego przeliczania rabatów.
- Trudności w porównywaniu cen w nieznanych lokalizacjach.

**Potrzeby wobec systemu:**

Tomasz oczekuje szybkich wyników wyszukiwania, aktualnych cen oraz jasnej informacji o warunkach promocji. Szczególnie istotna jest dla niego wiarygodność danych, ponieważ błędna rekomendacja może spowodować stratę czasu i dodatkowe koszty.

### Persona 3 – Karolina, administrator platformy

**Wiek:** 31 lat

**Zawód:** Administrator systemu internetowego

**Charakterystyka:**

Karolina odpowiada za kontrolowanie jakości informacji prezentowanych użytkownikom. Jej zadaniem jest dbanie o to, aby ceny paliw i promocje były poprawnie opisane, aktualne oraz zgodne z dostępnymi źródłami.

Korzysta z panelu administracyjnego i monitoruje dane pochodzące z zewnętrznych serwisów.

**Cele:**
- Zapewnienie możliwie wysokiej wiarygodności prezentowanych cen.
- Szybkie wykrywanie nieaktualnych promocji.
- Ograniczenie liczby błędnych rekomendacji.
- Sprawne zarządzanie danymi stacji i ofert.

**Frustracje:**
- Brak informacji o źródle i czasie aktualizacji danych.
- Promocje z niejasnymi warunkami.
- Konieczność ręcznego poprawiania wielu rekordów.
- Problemy z dostępnością zewnętrznych źródeł danych.

**Potrzeby wobec systemu:**

Karolina potrzebuje panelu umożliwiającego przeglądanie ofert, sprawdzanie ich aktualności, edycję danych i wyłączanie nieprawidłowych promocji. System powinien wspierać identyfikowanie potencjalnych błędów oraz ograniczać ryzyko publikowania niezweryfikowanych informacji.

---

## 1.7. Podsumowanie wizji i zakresu projektu

FuelRadar odpowiada na problem rozproszenia informacji o cenach paliw i promocjach oraz trudności w określeniu rzeczywistego kosztu tankowania.

Projekt koncentruje się na dostarczeniu kierowcom narzędzia, które automatycznie porównuje dostępne oferty i przedstawia ich koszt po zastosowaniu możliwych rabatów.

Pierwsza wersja zostanie ograniczona do wybranego regionu i podstawowych funkcjonalności, aby zmniejszyć koszty oraz ryzyko związane z realizacją projektu.

Najważniejszym celem biznesowym będzie zdobycie 500 aktywnych użytkowników miesięcznie w ciągu trzech miesięcy od uruchomienia MVP.

Dalszy rozwój będzie zależeć od zainteresowania użytkowników, jakości dostępnych danych i wyników pilotażu.

Takie podejście umożliwi stopniową rozbudowę FuelRadar bez konieczności projektowania rozbudowanej infrastruktury już na pierwszym etapie.

### Źródła do analizy rynku

- [PaliwoMapa – opis aplikacji](https://play.google.com/store/apps/details?id=pl.paliwomapa.app)
- [BenzynaMAPA – dokumentacja API](https://benzynamapa.pl/api-docs/)
- [Fuelio – funkcje aplikacji](https://www.fuel.io/en-US/features/)

