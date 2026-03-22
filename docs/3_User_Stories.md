# User Stories — Historyjki Użytkowników

## Spis Treści

1. [Wprowadzenie](#wprowadzenie)
2. [Metryka Dojrzałości User Stories](#metryka-dojrzałości-user-stories)
3. [Actorzy Systemu](#actorzy-systemu)
4. [User Stories — Korepetytor / Trener](#user-stories--korepetytor--trener)
5. [User Stories — Uczeń](#user-stories--uczeń)
6. [User Stories — Właściciel Szkoły Językowej](#user-stories--właściciel-szkoły-językowej)
7. [User Stories — Administrator Systemu](#user-stories--administrator-systemu)
8. [Priorytetyzacja (MoSCoW)](#priorytetyzacja-moscow)
9. [Kryteria Akceptacji — Przykłady](#kryteria-akceptacji---przykłady)

---

## Wprowadzenie

Niniejszy dokument zawiera kompletny zestaw **User Stories** (historyjek użytkowników) dla platformy EduSync. Każda historyjka została sformułowana zgodnie z konwencją:

> **Jako** [rola użytkownika], **chcę** [opis akcji], **aby** [korzyść biznesowa].

Dodatkowo każda historia zawiera:

- **Identyfikator** (np. US-001)
- **Priorytet** (Must Have / Should Have / Could Have / Won't Have)
- **Estymację** (story points)
- **Kryteria akceptacji**
- **Powiązania** z innymi historiami

---

## Metryka Dojrzałości User Stories

| Kryterium | Opis |
|-----------|------|
| **INVEST** | Independent (Niezależna), Negotiable (Negocjowalna), Valuable (Wartościowa), Estimable (Oszacowalna), Small (Mała), Testable (Testowalna) |
| **3C** | Card (Karta), Conversation (Rozmowa), Confirmation (Potwierdzenie) |
| **Dodatkowe** | Definition of Done, Acceptance Criteria |

---

## Actorzy Systemu

| Actor | Opis | Uprawnienia |
|-------|------|-------------|
| **Korepetytor** | Osoba prowadząca indywidualne zajęcia edukacyjne | Pełny dostęp do własnego konta |
| **Właściciel szkoły** | Osoba zarządzająca małą szkołą językową | Dostęp do konta szkoły + konta nauczycieli |
| **Uczenniak / Uczeń** | Osoba uczestnicząca w zajęciach | Ograniczony dostęp (portal ucznia) |
| **Administrator** | Osoba zarządzająca systemem | Pełny dostęp do wszystkich danych |

---

## User Stories — Korepetytor / Trener

### 1. Zarządzanie Kalendarzem

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-001** | Jako korepetytor, chcę **dodawać terminy zajęć do kalendarza**, aby uczniowie mogli je zobaczyć i zarezerwować | MUST HAVE | 3 SP |
| **US-002** | Jako korepetytor, chcę **zmieniać i odwoływać zajęcia**, aby elastycznie zarządzać grafikiem | MUST HAVE | 2 SP |
| **US-003** | Jako korepetytor, chcę **ustawiać powtarzające się zajęcia** (cykliczne), aby nie dodawać ręcznie każdego tygodnia | SHOULD HAVE | 5 SP |
| **US-004** | Jako korepetytor, chcę **wysyłać automatyczne przypomnienia** o zbliżających się zajęciach, aby zmniejszyć liczbę nieobecności | SHOULD HAVE | 3 SP |
| **US-005** | Jako korepetytor, chcę **blokować terminy niedostępne** (urlop, przerwa świąteczna), aby uczniie wiedzieli, kiedy nie ma zajęć | COULD HAVE | 2 SP |
| **US-006** | Jako korepetytor, chcę **widzieć konflikty w grafiku** (nakładające się rezerwacje), aby ich uniknąć | MUST HAVE | 3 SP |
| **US-007** | Jako korepetytor, chcę **eksportować kalendarz do Google Calendar / Outlook**, aby mieć wszystko w jednym miejscu | COULD HAVE | 5 SP |

### 2. Zarządzanie Uczniami (CRM)

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-010** | Jako korepetytor, chcę **dodawać nowych uczniów do bazy** z danymi kontaktowymi, aby móc zarządzać moimi klientami | MUST HAVE | 2 SP |
| **US-011** | Jako korepetytor, chcę **edycować i usuwać uczniów** z bazy, aby utrzymywać ją aktualną | MUST HAVE | 1 SP |
| **US-012** | Jako korepetytor, chcę **wyszukiwać uczniów po imieniu, nazwisku, języku**, aby szybko znaleźć właściwą osobę | MUST HAVE | 2 SP |
| **US-013** | Jako korepetytor, chcę **tagować uczniów** (np. "egzamin maturalny", "biznesowy", "dziecko"), aby ich kategoryzować | SHOULD HAVE | 3 SP |
| **US-014** | Jako korepetytor, chcę **dodawać notatki o uczniach** (postępy, uwagi, preferencje), aby personalizować nauczanie | SHOULD HAVE | 3 SP |
| **US-015** | Jako korepetytor, chcę **widzieć historię zajęć z każdym uczniem**, aby śledzić postępy | MUST HAVE | 3 SP |
| **US-016** | Jako korepetytor, chcę **oceniać obecność uczniów** na zajęciach, aby mieć statystyki | SHOULD HAVE | 2 SP |
| **US-017** | Jako korepetytor, chcę **archiwizować nieaktywnych uczniów**, aby nie zaśmiecać aktywnej bazy | COULD HAVE | 1 SP |

### 3. Billing i Fakturowanie

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-020** | Jako korepetytor, chcę **wystawiać faktury VAT** z danymi mojej firmy, aby rozliczać się z uczniami | MUST HAVE | 5 SP |
| **US-021** | Jako korepetytor, chcę **wystawiać faktury bez VAT** (dla osób prywatnych), aby dostosować do sytuacji | MUST HAVE | 3 SP |
| **US-022** | Jako korepetytor, chcę **śledzić status płatności** (oczekująca, opłacona, przeterminowana), aby wiedzieć, kto zalega | MUST HAVE | 3 SP |
| **US-023** | Jako korepetytor, chcę **wysyłać automatyczne przypomnienia** o nieopłaconych fakturach, aby zmniejszyć zaległości | SHOULD HAVE | 3 SP |
| **US-024** | Jako korepetytor, chcę **generować faktury automatycznie** na podstawie odbytych zajęć, aby oszczędzić czas | SHOULD HAVE | 5 SP |
| **US-025** | Jako korepetytor, chcę **eksportować faktury do PDF**, aby je archiwizować i wysyłać | MUST HAVE | 2 SP |
| **US-026** | Jako korepetytor, chcę **tworzyć własne szablony faktur**, aby dostosować wygląd do mojej marki | COULD HAVE | 3 SP |
| **US-027** | Jako korepetytor, chcę **przyjmować płatności online** (Przelewy24, Stripe), aby uczniowie mogli płacić jednym kliknięciem | SHOULD HAVE | 8 SP |

### 4. Komunikacja

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-030** | Jako korepetytor, chcę **wysyłać wiadomości do uczniów** bezpośrednio z systemu, aby mieć historię komunikacji | MUST HAVE | 3 SP |
| **US-031** | Jako korepetytor, chcę **używać szablonów wiadomości** (przypomnienie, potwierdzenie), aby oszczędzać czas | SHOULD HAVE | 2 SP |
| **US-032** | Jako korepetytor, chcę **wysyłać maile/SMS z systemu**, aby mieć pewność, że dotrą | COULD HAVE | 5 SP |
| **US-033** | Jako korepetytor, chcę **udostępniać uczniom portal**, gdzie mogą sprawdzić swój grafik i faktury, aby odciążyć mnie od pytań | SHOULD HAVE | 5 SP |
| **US-034** | Jako korepetytor, chcę **zbierać feedback od uczniów** po zajęciach, aby poprawiać jakość | COULD HAVE | 3 SP |

### 5. Analityka i Raporty

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-040** | Jako korepetytor, chcę **widzieć dashboard z przychodami**, aby wiedzieć, ile zarobiłem w danym okresie | MUST HAVE | 3 SP |
| **US-041** | Jako korepetytor, chcę **generować raporty frekwencji**, aby widzieć, ilu uczniów regularnie przychodzi | SHOULD HAVE | 3 SP |
| **US-042** | Jako korepetytor, chcę **widzieć statystyki najpopularniejszych języków/poziomów**, aby planować ofertę | COULD HAVE | 2 SP |
| **US-043** | Jako korepetytor, chcę **eksportować raporty do Excel/PDF**, aby przekazywać je księgowemu | SHOULD HAVE | 2 SP |
| **US-044** | Jako korepetytor, chcę **prognozować przychody** na podstawie historii, aby planować budżet | WON'T HAVE | - |

### 6. Materiały Dydaktyczne

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-050** | Jako korepetytor, chcę **przechowywać materiały w jednym miejscu**, aby łatwo je znaleźć | SHOULD HAVE | 3 SP |
| **US-051** | Jako korepetytor, chcę **udostępniać materiały uczniom** bezpośrednio z systemu, aby nie wysyłać ręcznie plików | SHOULD HAVE | 3 SP |
| **US-052** | Jako korepetytor, chcę **tworzyć listy materiałów dla poszczególnych poziomów**, aby systematyzować nauczanie | COULD HAVE | 5 SP |

---

## User Stories — Uczeń

### 1. Rezerwacja i Kalendarz

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-100** | Jako uczeń, chcę **widzieć dostępne terminy korepetytora**, aby zarezerwować dogodny slot | MUST HAVE | 3 SP |
| **US-101** | Jako uczeń, chcę **rezerwować zajęcia jednym kliknięciem**, aby szybko umówić się na lekcję | MUST HAVE | 3 SP |
| **US-102** | Jako uczeń, chcę **odwoływać lub przenosić zajęcia** z wyprzedzeniem, aby zarządzać moim czasem | MUST HAVE | 2 SP |
| **US-103** | Jako uczeń, chcę **dostawać przypomnienia o zbliżających się zajęciach**, aby nie zapomnieć | SHOULD HAVE | 2 SP |
| **US-104** | Jako uczeń, chcę **widzieć mój kalendarz zajęć**, aby wiedzieć, kiedy mam lekcje | MUST HAVE | 2 SP |

### 2. Płatności

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-110** | Jako uczeń, chcę **widzieć moje faktury i historię płatności**, aby wiedzieć, co zapłaciłem | MUST HAVE | 2 SP |
| **US-111** | Jako uczeń, chcę **opłacać faktury online** (karta, BLIK), aby nie musieć robić przelewów ręcznie | SHOULD HAVE | 3 SP |
| **US-112** | Jako uczeń, chcę **pobierać faktury w PDF**, aby je archiwizować | MUST HAVE | 1 SP |

### 3. Komunikacja

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-120** | Jako uczeń, chcę **wysyłać wiadomości do korepetytora** przez system, aby mieć historię kontaktów | MUST HAVE | 2 SP |
| **US-121** | Jako uczeń, chcę **dostawać odpowiedzi na moje wiadomości**, aby komunikacja była sprawna | MUST HAVE | 1 SP |
| **US-122** | Jako uczeń, chcę **oceniać zajęcia po ich zakończeniu**, aby dać feedback korepetytorowi | COULD HAVE | 2 SP |

### 4. Materiały

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-130** | Jako uczeń, chcę **mieć dostęp do materiałów od korepetytora**, aby móc się uczyć | SHOULD HAVE | 2 SP |
| **US-131** | Jako uczeń, chcę **śledzić postępy w nauce** (odbyte lekcje, tematy), aby widzieć efekty | COULD HAVE | 3 SP |

---

## User Stories — Właściciel Szkoły Językowej

### 1. Zarządzanie Zespołem

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-200** | Jako właściciel szkoły, chcę **dodawać nauczycieli do systemu**, aby mogli prowadzić zajęcia | MUST HAVE | 3 SP |
| **US-201** | Jako właściciel szkoły, chcę **zarządzać uprawnieniami nauczycieli**, aby kontrolować dostęp do danych | MUST HAVE | 3 SP |
| **US-202** | Jako właściciel szkoły, chcę **widzieć grafik wszystkich nauczycieli**, aby koordynować pracę szkoły | MUST HAVE | 3 SP |
| **US-203** | Jako właściciel szkoły, chcę **przydzielać uczniów do nauczycieli**, aby automatycznie planować zajęcia | SHOULD HAVE | 5 SP |
| **US-204** | Jako właściciel szkoły, chcę **wystawiać faktury w imieniu szkoły** (z NIP), aby rozliczać się korporacyjnie | MUST HAVE | 5 SP |

### 2. Raporty i Analityka

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-210** | Jako właściciel szkoły, chcę **widzieć przychody całej szkoły**, aby znać sytuację finansową | MUST HAVE | 3 SP |
| **US-211** | Jako właściciel szkoły, chcę **porównywać wyniki nauczycieli**, aby ocenić efektywność zespołu | SHOULD HAVE | 3 SP |
| **US-212** | Jako właściciel szkoły, chcę **widzieć obłożenie sal/komitek**, aby optymalizować wykorzystanie zasobów | COULD HAVE | 3 SP |
| **US-213** | Jako właściciel szkoły, chcę **generować raporty dla księgowości**, aby ułatwić rozliczenia | MUST HAVE | 3 SP |

---

## User Stories — Administrator Systemu

### 1. Zarządzanie Użytkownikami

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-300** | Jako administrator, chcę **tworzyć i zarządzać kontami użytkowników**, aby utrzymywać porządek w systemie | MUST HAVE | 3 SP |
| **US-301** | Jako administrator, chcę **resetować hasła użytkowników**, aby pomagać w awariach logowania | MUST HAVE | 1 SP |
| **US-302** | Jako administrator, chcę **blokować konta naruszające regulamin**, aby chronić system | SHOULD HAVE | 2 SP |

### 2. Konfiguracja Systemu

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-310** | Jako administrator, chcę **konfigurować ustawienia systemu** (stawki VAT, waluta, strefa czasowa), aby dostosować do rynku | MUST HAVE | 3 SP |
| **US-311** | Jako administrator, chcę **zarządzać szablonami email/SMS**, aby personalizować komunikację | SHOULD HAVE | 3 SP |
| **US-312** | Jako administrator, chcę **włączać/wyłączać funkcje** dla poszczególnych planów cenowych, aby kontrolować dostęp | MUST HAVE | 5 SP |

### 3. Monitorowanie i Bezpieczeństwo

| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-320** | Jako administrator, chcę **monitorować logi systemu**, aby wykrywać problemy i ataki | MUST HAVE | 3 SP |
| **US-321** | Jako administrator, chcę **tworzyć kopie zapasowe danych**, aby zabezpieczyć się przed utratą | MUST HAVE | 5 SP |
| **US-322** | Jako administrator, chcę **wymuszać zmianę haseł** po określonym czasie, aby zwiększyć bezpieczeństwo | COULD HAVE | 2 SP |
| **US-323** | Jako administrator, chcę **wygaszać sesje po nieaktywności**, aby chronić konta | SHOULD HAVE | 2 SP |

---

## Priorytetyzacja (MoSCoW)

### Must Have (Krytyczne)

Łączna estymacja: **47 SP**

| ID | User Story | Estymacja |
|----|------------|-----------|
| US-001 | Dodawanie terminów do kalendarza | 3 SP |
| US-002 | Zmienianie i odwoływanie zajęć | 2 SP |
| US-006 | Wykrywanie konfliktów w grafiku | 3 SP |
| US-010 | Dodawanie uczniów do bazy | 2 SP |
| US-011 | Edycja i usuwanie uczniów | 1 SP |
| US-012 | Wyszukiwanie uczniów | 2 SP |
| US-015 | Historia zajęć z uczniem | 3 SP |
| US-020 | Wystawianie faktur VAT | 5 SP |
| US-021 | Wystawianie faktur bez VAT | 3 SP |
| US-022 | Śledzenie statusu płatności | 3 SP |
| US-025 | Eksport faktur do PDF | 2 SP |
| US-030 | Wysyłanie wiadomości do uczniów | 3 SP |
| US-040 | Dashboard z przychodami | 3 SP |
| US-100 | Widok dostępnych terminów | 3 SP |
| US-101 | Rezerwacja zajęć jednym kliknięciem | 3 SP |
| US-102 | Odwoływanie/przenoszenie zajęć | 2 SP |
| US-104 | Widok kalendarza ucznia | 2 SP |
| US-110 | Widok faktur i historii płatności | 2 SP |
| US-112 | Pobieranie faktur w PDF | 1 SP |
| US-120 | Wysyłanie wiadomości przez system | 2 SP |

### Should Have (Ważne)

Łączna estymacja: **38 SP**

| ID | User Story | Estymacja |
|----|------------|-----------|
| US-003 | Ustawianie powtarzających się zajęć | 5 SP |
| US-004 | Automatyczne przypomnienia o zajęciach | 3 SP |
| US-013 | Tagowanie uczniów | 3 SP |
| US-014 | Dodawanie notatek o uczniach | 3 SP |
| US-016 | Ocena obecności uczniów | 2 SP |
| US-023 | Przypomnienia o nieopłaconych fakturach | 3 SP |
| US-024 | Automatyczne generowanie faktur | 5 SP |
| US-027 | Przyjmowanie płatności online | 8 SP |
| US-031 | Szablony wiadomości | 2 SP |
| US-033 | Portal ucznia | 5 SP |
| US-041 | Raporty frekwencji | 3 SP |
| US-050 | Przechowywanie materiałów | 3 SP |
| US-051 | Udostępnianie materiałów uczniom | 3 SP |

### Could Have (Pożądane)

Łączna estymacja: **28 SP**

| ID | User Story | Estymacja |
|----|------------|-----------|
| US-005 | Blokowanie terminów | 2 SP |
| US-007 | Eksport kalendarza | 5 SP |
| US-017 | Archiwizacja uczniów | 1 SP |
| US-026 | Własne szablony faktur | 3 SP |
| US-032 | Wysyłanie email/SMS z systemu | 5 SP |
| US-034 | Zbieranie feedbacku | 3 SP |
| US-042 | Statystyki popularnych języków | 2 SP |
| US-052 | Listy materiałów dla poziomów | 5 SP |
| US-103 | Przypomnienia o zajęciach | 2 SP |
| US-111 | Płatności online | 3 SP |
| US-122 | Ocena zajęć | 2 SP |
| US-130 | Dostęp do materiałów | 2 SP |
| US-131 | Śledzenie postępów | 3 SP |

### Won't Have (Nie w tej iteracji)

| ID | User Story | Uzasadnienie |
|----|------------|--------------|
| US-044 | Prognozowanie przychodów | Wymaga zaawansowanych algorytmów ML, niska wartość MVP |
| US-323 | Wygaszanie sesji | Można dodać w późniejszej iteracji |

---

## Kryteria Akceptacji — Przykłady

### US-001: Dodawanie terminów do kalendarza

**Kryteria akceptacji:**

1. ✅ Użytkownik może wybrać datę z kalendarza
2. ✅ Użytkownik może wybrać godzinę rozpoczęcia i zakończenia
3. ✅ Użytkownik może przypisać ucznia do zajęć
4. ✅ System sprawdza dostępność i nie pozwala na konflikty
5. ✅ Po zapisaniu zajęcia widoczne w kalendarzu
6. ✅ Użytkownik otrzymuje potwierdzenie zapisu

**Scenariusze testowe:**

- Dodanie zajęcia na wolny termin → sukces
- Dodanie zajęcia na zajęty termin → błąd z komunikatem
- Dodanie zajęcia bez przypisania ucznia → ostrzeżenie (możliwe)

---

### US-020: Wystawianie faktur VAT

**Kryteria akceptacji:**

1. ✅ System pobiera dane firmy z profilu użytkownika
2. ✅ System pobiera dane ucznia z bazy
3. ✅ Użytkownik może edytować dane przed wystawieniem
4. ✅ Faktura zawiera: NIP sprzedawcy, dane nabywcy, datę, kwotę, VAT
5. ✅ Faktura otrzymuje unikalny numer (FV/2025/001)
6. ✅ Faktura jest generowana jako PDF
7. ✅ Faktura jest zapisywana w historii

**Scenariusze testowe:**

- Wystawienie faktury na osobę fizyczną → wymagany PESEL
- Wystawienie faktury na firmę → wymagany NIP
- Wystawienie faktury z 0% VAT → możliwe (np. zwolnienie)

---

### US-101: Rezerwacja zajęć jednym kliknięciem

**Kryteria akceptacji:**

1. ✅ Uczeń widzi listę dostępnych terminów
2. ✅ Kliknięcie w termin automatycznie tworzy rezerwację
3. ✅ System wysyła potwierdzenie do ucznia i korepetytora
4. ✅ Zajęcia pojawiają się w kalendarzu obu stron
5. ✅ Przy próbie rezerwacji zajętego terminu → błąd

---

## Podsumowanie

| Kategoria | Liczba User Stories | Łączna Estymacja |
|-----------|--------------------|--------------------|
| Must Have | 20 | 47 SP |
| Should Have | 13 | 38 SP |
| Could Have | 13 | 28 SP |
| Won't Have | 2 | 0 SP |
| **RAZEM** | **48** | **113 SP** |

**Uwagi:**

- Zakładamy sprint 2-tygodniowy z pojemnością ~30-40 SP
- MVP powinno zawierać wszystkie Must Have (47 SP = ~2 sprinty)
- Should Have to cel na kolejne 2-3 sprinty

---

*Document Version: 1.0*  
*Last Updated: 2025*  
*Author: Product Team*  
*Status: Ready for Development*
