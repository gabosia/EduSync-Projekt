# Założenia Biznesowe

## Spis Treści

1. [Wprowadzenie](#1-wprowadzenie)
2. [Analiza Problemu](#2-analiza-problemu)
3. [Rynek i Oportunita](#3-rynek-i-oportunita)
4. [Proponowane Rozwiązanie (MVP a Wizja)](#4-proponowane-rozwiązanie-mvp-a-wizja)
5. [Model Monetizacji](#5-model-monetizacji)
6. [Analiza Konkurencji](#6-analiza-konkurencji)
7. [Podsumowanie i Rekomendacje](#7-podsumowanie-i-rekomendacje)

---

## 1. Wprowadzenie

### Kontekst Projektu

Niniejszy dokument stanowi fundament strategiczny dla projektu **EduSync** — platformy SaaS dedykowanej korepetytorom indywidualnym oraz małym szkołom językowym. Dokument przedstawia docelową wizję produktu oraz określa zakres pierwszej, testowej wersji aplikacji **(MVP - Minimum Viable Product)**, która powstanie w ramach ok. 20-godzinnego nakładu pracy.

Współczesny rynek edukacji prywatnej przeżywa rozkwit. Miliony korepetytorów zmuszeni są zarządzać swoją działalnością w sposób, który często przekracza ich kompetencje organizacyjne. Celem EduSync jest rozwiązanie tego problemu.

---

## 2. Analiza Problemu

### 2.1. Charakterystyka Grupy Docelowej
Polski rynek korepetycji to ponad 150 000 działalności. Typowy korepetytor obsługuje od 10 do 50 uczniów, a jego priorytetem jest nauczanie, nie administracja. 

### 2.2. Manifestacja Chaosu Organizacyjnego
* **Excel jako "System CRM":** Nauczyciele toną w arkuszach kalkulacyjnych, co generuje błędy i brak mobilnego dostępu.
* **Odwołane Zajęcia i Brak Śledzenia:** Brak systemowego podejścia do odwołań to strata czasu i zarobku.
* **Rozproszona komunikacja:** Ustalenia na Messengerze, SMS i mailach giną w chaosie.
* **Brak Statystyk:** Korepetytor nie wie, ilu ma dokładnie aktywnych uczniów i jakie są jego realne przychody.

**Podsumowując**: Chaos organizacyjny może kosztować korepetytora nawet 30-40% potencjalnego przychodu rocznie.

---

## 3. Rynek i Oportunita

* **Rynek Globalny (TAM):** Rynek narzędzi do zarządzania praktyką nauczycielską to ok. USD 3.5 miliarda.
* **Rynek Docelowy w Polsce (SOM):** Szacowany na PLN 500-800 milionów rocznie.
* **Trendy:** Praca zdalna, rosnące zapotrzebowanie na języki obce, profesjonalizacja sektora edukacji prywatnej.

**Profil Idealnego Klienta (ICP):**
Korepetytor (1-15 lat doświadczenia), obsługujący 15-100 uczniów, tracący czas na ręczną administrację, gotowy zapłacić za automatyzację.

---

## 4. Proponowane Rozwiązanie (MVP a Wizja)

Z uwagi na budżet czasowy (ok. 20 godzin na pierwszą fazę techniczną), rozwój EduSync został podzielony na fazę weryfikacji pomysłu (MVP) oraz docelową rozbudowę.

### 4.1. Zakres MVP (Obecna faza realizacji - ok. 20h)
Wersja MVP to absolutne fundamenty, które pozwolą korepetytorowi odejść od notatnika/Excela:
1. **Moduł Autoryzacji:** Rejestracja i logowanie użytkowników (korepetytorów).
2. **Baza Uczniów (Mini-CRM):** Dodawanie, edycja i usuwanie profili uczniów wraz z notatkami.
3. **Harmonogram Zajęć:** Proste planowanie lekcji, przypisywanie uczniów do konkretnych terminów i oznaczanie statusu zajęć (np. "zaplanowane", "zrealizowane").

### 4.2. Plany Rozwoju (Docelowa Wizja - poza zakresem MVP)
W kolejnych etapach rozwoju, projekt zakłada wdrożenie następujących modułów:
* **Moduł Billingowy:** Automatyczne faktury i integracja z bramkami płatności (Przelewy24, Stripe).
* **Zaawansowany Kalendarz:** Synchronizacja z Google Calendar i Apple.
* **Automatyczna Komunikacja:** Powiadomienia SMS/Email dla uczniów o zbliżających się zajęciach.
* **Zaawansowana Analityka:** Wykresy przychodów i wskaźniki rezygnacji (churn rate).
* **Materiały Dydaktyczne:** Chmurowe udostępnianie plików uczniom.

---

## 5. Model Monetizacji

Aplikacja w fazie MVP będzie udostępniana darmowo pierwszym testerom. Docelowo model biznesowy zakłada subskrypcję SaaS:
* **Starter (Darmowy):** Do 5 uczniów, funkcje podstawowe.
* **Pro (79 PLN/msc):** Bez limitu uczniów, pełen kalendarz i fakturowanie.
* **Team (199 PLN/msc):** Dla małych szkół językowych (do 10 nauczycieli).

---

## 6. Analiza Konkurencji

* **Calendly / Acuity Scheduling:** Silne w planowaniu, ale brak pełnego CRM ucznia.
* **Platformy kursowe (Teachable):** Stworzone do gotowych kursów wideo, nie do zajęć 1:1 na żywo.
* **Przewaga EduSync:** Stworzone specjalnie i wyłącznie dla korepetytorów, łączące bazę uczniów z harmonogramem.

---

## 7. Podsumowanie i Rekomendacje

### 7.1. Kluczowe Wnioski
Problem chaosu organizacyjnego wśród korepetytorów jest realny i kosztowny. Chmura i nowoczesne frameworki (React, Supabase) pozwalają na szybkie zbudowanie narzędzia, które go rozwiąże.

### 7.2. Najbliższe Kroki (Roadmapa)
1. **Rozwój MVP:** Zbudowanie bazowego modułu autoryzacji, zarządzania uczniami i lekcjami (Zasób czasowy: ok. 20h).
2. **Beta-Testy:** Udostępnienie MVP grupie 10 zaprzyjaźnionych korepetytorów w celu zebrania opinii.
3. **Faza 2 (Przyszłość):** Planowanie i wdrożenie integracji płatniczych oraz automatycznych powiadomień.

---

*Status: Zaktualizowano dla fazy MVP*
