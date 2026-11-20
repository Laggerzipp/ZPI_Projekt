# ⛽ FuelRadar

**FuelRadar – porównywarka cen paliw z uwzględnieniem promocji i programów lojalnościowych.**

**Status projektu:** Planowanie i analiza wymagań  
**Wersja:** 0.1 (Planning)  
**Zespół:** 3 osoby  
**Projekt:** ZPI – Zespołowy Projekt Informatyczny

---

## 📖 Opis projektu

FuelRadar to projekt aplikacji internetowej, której celem jest umożliwienie kierowcom wyszukiwania najkorzystniejszych ofert tankowania paliwa.

W przeciwieństwie do tradycyjnych porównywarek cen paliw, FuelRadar będzie uwzględniał nie tylko ceny bazowe, ale również dostępne promocje, programy lojalnościowe oraz warunki wykorzystania rabatów.

Użytkownik będzie mógł określić rodzaj paliwa, planowaną liczbę litrów oraz posiadane programy lojalnościowe. Na podstawie tych informacji system obliczy koszt tankowania na poszczególnych stacjach i przedstawi ranking najkorzystniejszych ofert.

Projekt będzie rozwijany etapowo, począwszy od MVP obejmującego wybrany region.

## 🎯 Problem biznesowy

Obecnie kierowcy chcący znaleźć najkorzystniejszą ofertę tankowania często muszą korzystać z kilku źródeł informacji:

- Porównywarek cen paliw.
- Oficjalnych stron internetowych sieci stacji.
- Aplikacji i programów lojalnościowych.
- Regulaminów aktualnych promocji.

Dodatkowym utrudnieniem są różne zasady przyznawania rabatów, takie jak limity litrów, konieczność posiadania odpowiedniej aplikacji czy ograniczony czas obowiązywania promocji.

**FuelRadar ma uprościć ten proces, prezentując w jednym miejscu obliczony koszt tankowania po uwzględnieniu promocji, z których użytkownik może skorzystać.**

## 🚀 Cel projektu

Głównym celem biznesowym jest osiągnięcie **minimum 500 aktywnych użytkowników miesięcznie w ciągu 3 miesięcy od uruchomienia MVP** w wybranym regionie pilotażowym.

Za aktywnego użytkownika uznajemy osobę, która wykonała przynajmniej jedno kompletne porównanie ofert tankowania w ciągu ostatnich 30 dni.

Realizacja tego celu pozwoli wstępnie zweryfikować zainteresowanie produktem oraz zasadność jego dalszego rozwoju.

## ⚙️ Planowane funkcjonalności MVP

Pierwsza wersja FuelRadar będzie obejmować:

- Wyszukiwanie stacji paliw w wybranym regionie.
- Wybór rodzaju paliwa (np. PB95, PB98, ON, LPG).
- Określanie planowanej liczby litrów paliwa.
- Wyświetlanie cen paliw na dostępnych stacjach.
- Wybór posiadanych programów lojalnościowych.
- Uwzględnianie promocji oraz ich ograniczeń.
- Automatyczne obliczanie kosztu tankowania po zastosowaniu rabatów.
- Sortowanie stacji według całkowitego kosztu tankowania.
- Prezentowanie źródła danych i czasu ich ostatniej aktualizacji.
- Oznaczanie nieaktualnych informacji o cenach.

### Przykład działania

Użytkownik planuje zatankować 50 litrów benzyny PB95.

System porównuje następujące oferty:

| Stacja | Cena bazowa | Promocja | Koszt tankowania |
|---|---|---|---|
| A | 6,20 zł/l | 30 gr/l do 30 litrów | 301,00 zł |
| B | 6,10 zł/l | 20 gr/l do 50 litrów | 295,00 zł |
| C | 6,00 zł/l | Brak promocji | 300,00 zł |

W przedstawionym przykładzie najkorzystniejszą ofertą jest **stacja B**, pod warunkiem spełnienia zasad promocji.

*Przykład wykorzystuje fikcyjne ceny i rabaty. Nie uwzględnia kosztu dojazdu.*

## 📈 Planowany rozwój

W kolejnych etapach planowane jest rozszerzenie systemu o:

- Uwzględnianie kosztów dojazdu do stacji.
- Obsługę kolejnych regionów Polski.
- Powiadomienia o zmianach cen paliw.
- Historię i analizę zmian cen.
- Rozbudowane możliwości personalizacji.
- Konta dla właścicieli stacji paliw.
- Dodatkowe integracje z zewnętrznymi źródłami danych.
- Dedykowaną aplikację mobilną.

Funkcjonalności te nie wchodzą w początkowy zakres MVP.

## 🛠️ Technologie

Wstępnie rozważany stos technologiczny:

| Obszar | Technologia |
|---|---|
| Frontend | React, TypeScript |
| Backend | Node.js lub Python + FastAPI – do ostatecznego uzgodnienia |
| Baza danych | PostgreSQL |
| Usługa bazy danych | Supabase |
| Mapy | OpenStreetMap, Leaflet |
| Hosting frontendu | Cloudflare Pages |
| Kontrola wersji | Git, GitHub |
| Zarządzanie projektem | Jira |

Ostateczny wybór technologii zostanie zatwierdzony przed rozpoczęciem implementacji.

## 🏗️ Architektura systemu

W początkowej wersji planowane jest zastosowanie prostej architektury klient–serwer.

System będzie składał się z trzech podstawowych elementów:

**1. Frontend**

Interfejs aplikacji umożliwiający użytkownikowi wprowadzanie parametrów tankowania, wybór programów lojalnościowych i przeglądanie wyników.

**2. Backend API**

Warstwa odpowiedzialna za przetwarzanie żądań, pobieranie danych, interpretowanie warunków promocji i obliczanie kosztów tankowania.

**3. Baza danych**

Przechowywanie informacji o stacjach paliw, cenach, promocjach oraz źródłach i czasie aktualizacji danych.

W pierwszym etapie planowane jest wykorzystanie pojedynczego backendu oraz jednej bazy danych, aby ograniczyć złożoność i koszty utrzymania.

Architektura będzie projektowana z myślą o możliwości stopniowej rozbudowy systemu.

## 🧪 Proof of Concept (PoC)

Pierwszy planowany sprint zostanie poświęcony przygotowaniu koncepcji Proof of Concept.

**Cel PoC:** Zweryfikowanie możliwości automatycznego obliczania kosztów tankowania z uwzględnieniem rabatów i ograniczeń ilościowych.

Weryfikowane będą między innymi:

- Poprawność obliczania ceny po rabacie.
- Obsługa maksymalnej liczby litrów objętych promocją.
- Poprawność obliczeń bez dostępnego rabatu.
- Walidacja danych wejściowych.
- Poprawność zaokrąglania kwot.

W ramach Zadania 3 PoC będzie opisany na poziomie koncepcji implementacji i planowanego eksperymentu.

## 📅 Plan realizacji

Przewidywany czas realizacji MVP wynosi **12 tygodni**.

Projekt zostanie zaplanowany w oparciu o metodykę Scrum, z wykorzystaniem sześciu dwutygodniowych sprintów.

Główne epiki projektu:

1. **Fuel Station Search** – wyszukiwanie stacji paliw.
2. **Fuel Price Comparison** – porównywanie kosztów tankowania.
3. **Loyalty Programs & Discounts** – obsługa promocji i rabatów.
4. **Offers & Data Management** – zarządzanie danymi i ich aktualnością.
5. **User Interface & System Integration** – interfejs i integracja komponentów.

Roadmapa projektu będzie przedstawiała harmonogram realizacji wyłącznie na poziomie epików.

## 👥 Zespół projektowy

Projekt realizowany jest przez trzyosobowy zespół w ramach przedmiotu ZPI.

Główne obszary odpowiedzialności zespołu obejmują:

- Analizę biznesową i analizę wymagań.
- Projektowanie systemu i architektury oprogramowania.
- Zapewnienie jakości, testowanie i analizę ryzyka.

Szczegółowy podział prac będzie realizowany poprzez zadania przypisywane członkom zespołu w Jira.

## 📂 Dokumentacja

Dokumentacja projektu jest stopniowo rozwijana w katalogu `docs/`.

| Dokument | Status |
|---|---|
| Zadanie 1 – Drivery architektoniczne | Opracowana sekcja 1; pozostałe części w przygotowaniu |
| Zadanie 2 – Specyfikacja wymagań (SRS) | Do opracowania |
| Zadanie 3 – Planowanie projektu i symulacja sprintu | Wstępna wersja przygotowana |
| Diagram architektury | Planowany |
| Dokumentacja implementacji | Planowana |

Dokumenty mogą być aktualizowane wraz z postępem realizacji projektu.

## 📋 Zarządzanie projektem

Do zarządzania projektem wykorzystujemy **Jira**.

Narzędzie służy do organizowania Product Backlogu, epików, historyjek użytkownika, zadań technicznych oraz planowania sprintów.

**Projekt Jira:** link zostanie dodany po przygotowaniu projektu.

## 💰 Koszty i ograniczenia

Na etapie MVP zakładamy wykorzystanie darmowych lub niedrogich usług hostingowych i bazodanowych.

Wstępny cel budżetowy infrastruktury wynosi **0–100 zł miesięcznie**, przy ograniczonym ruchu i korzystaniu z bezpłatnych planów.

Koszt ten nie uwzględnia pracy zespołu, komercyjnego dostępu do danych ani dodatkowych usług zewnętrznych.

Istotnym ograniczeniem projektu jest dostępność aktualnych cen paliw i informacji o promocjach. Przed wykorzystaniem zewnętrznych źródeł danych konieczne będzie zweryfikowanie warunków licencyjnych.

## 📌 Aktualny status projektu

Projekt znajduje się w fazie planowania i analizy wymagań.

Aktualnie prowadzone są prace nad dokumentacją, zakresem MVP, analizą architektury oraz przygotowaniem Product Backlogu.

Implementacja aplikacji i integracja z rzeczywistymi źródłami danych stanowią kolejne etapy projektu.

---

**FuelRadar – znajdź najkorzystniejszą ofertę tankowania, uwzględniając promocje, z których możesz skorzystać.**
