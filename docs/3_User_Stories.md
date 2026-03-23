# User Stories — Historyjki Użytkowników

## Spis Treści

1. [Wprowadzenie i Kontekst MVP](#wprowadzenie-i-kontekst-mvp)
2. [Metryka Dojrzałości User Stories](#metryka-dojrzałości-user-stories)
3. [Aktorzy Systemu](#aktorzy-systemu)
4. [User Stories — Faza MVP](#user-stories--faza-mvp)
5. [User Stories — Plany Rozwoju](#user-stories--plany-rozwoju)
6. [Priorytetyzacja (MoSCoW)](#priorytetyzacja-moscow)
7. [Kryteria Akceptacji](#kryteria-akceptacji)

---

## Wprowadzenie i Kontekst MVP

Niniejszy dokument zawiera zestaw **User Stories** (historyjek użytkowników) dla platformy EduSync. 

**Ważne:** Z uwagi na ograniczenia czasowe (budżet ok. 20 godzin), dokument został wyraźnie podzielony na historyjki realizowane w ramach **MVP** (absolutne minimum do działania aplikacji) oraz rozbudowane historyjki docelowe, zaplanowane na kolejne fazy rozwoju po obronie/zaliczeniu projektu.

Każda historyjka została sformułowana zgodnie z konwencją:
> **Jako** [rola użytkownika], **chcę** [opis akcji], **aby** [korzyść biznesowa].

---

## Metryka Dojrzałości User Stories

| Kryterium | Opis |
|-----------|------|
| **INVEST** | Independent, Negotiable, Valuable, Estimable, Small, Testable |
| **Estymacja**| Story Points (SP) - zakłada się, że 1 SP to ok. 1-2 godziny pracy jednego programisty. |

---

## Aktorzy Systemu

| Aktor | Opis | Status w fazie MVP |
|-------|------|--------------------|
| **Korepetytor** | Osoba prowadząca zajęcia. Zarządza uczniami i grafikiem. | **Główny i jedyny aktor w MVP** |
| **Uczeń** | Osoba uczestnicząca w zajęciach. | Poza zakresem MVP (planowane) |
| **Właściciel szkoły** | Zarządza małą szkołą językową (wielu nauczycieli). | Poza zakresem MVP (planowane) |
| **Administrator** | Osoba zarządzająca całym systemem SaaS. | Poza zakresem MVP (planowane) |

---

## User Stories — Faza MVP

Skupiamy się wyłącznie na fundamentalnych akcjach (CRUD) dla roli Korepetytora w ramach 20 godzin pracy.

### Autoryzacja i Konto (Podstawa)
| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-001** | Jako korepetytor, chcę **zarejestrować się w systemie**, aby utworzyć własne, bezpieczne konto | MUST HAVE | 3 SP |
| **US-002** | Jako korepetytor, chcę **zalogować się i wylogować**, aby nikt inny nie miał dostępu do moich danych | MUST HAVE | 2 SP |

### Zarządzanie Uczniami (Mini-CRM)
| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-010** | Jako korepetytor, chcę **dodać nowego ucznia do bazy** (imię, nazwisko, kontakt), aby prowadzić jego ewidencję | MUST HAVE | 3 SP |
| **US-011** | Jako korepetytor, chcę **widzieć listę wszystkich moich uczniów**, aby szybko ich odszukać | MUST HAVE | 2 SP |
| **US-012** | Jako korepetytor, chcę **usunąć ucznia z bazy**, jeśli zakończymy współpracę | MUST HAVE | 1 SP |

### Harmonogram Zajęć
| ID | User Story | Priorytet | Estymacja |
|----|------------|-----------|-----------|
| **US-020** | Jako korepetytor, chcę **dodać nowe zajęcia**, przypisując do nich konkretnego ucznia i datę | MUST HAVE | 3 SP |
| **US-021** | Jako korepetytor, chcę **widzieć listę moich zaplanowanych zajęć**, aby kontrolować swój grafik | MUST HAVE | 2 SP |
| **US-022** | Jako korepetytor, chcę **anulować/usunąć zajęcia**, jeśli uczeń z nich zrezygnuje | MUST HAVE | 1 SP |

---

## User Stories — Plany Rozwoju

Te historyjki stanowią docelową wizję produktu. **Nie będą realizowane w obecnym sprincie 20-godzinnym.**

* **US-100 (Faktury):** Jako korepetytor, chcę generować faktury w PDF dla moich uczniów.
* **US-101 (Płatności):** Jako korepetytor, chcę zintegrować system ze Stripe/Przelewy24, aby przyjmować płatności online.
* **US-102 (Powiadomienia):** Jako korepetytor, chcę wysyłać automatyczne powiadomienia email/SMS do uczniów.
* **US-200 (Portal Ucznia):** Jako uczeń, chcę mieć własne konto, aby widzieć historię swoich zajęć i płatności.
* **US-300 (Właściciel Szkoły):** Jako właściciel szkoły, chcę widzieć grafik wszystkich zatrudnionych u mnie korepetytorów.

---

## Priorytetyzacja (MoSCoW)

Przy ograniczeniu czasowym (20h dla jednego programisty), pojemność "sprintu" wynosi około **15-20 Story Points**. 

| Kategoria | Opis dla obecnej fazy | Łączna Estymacja |
|-----------|-----------------------|------------------|
| **Must Have** | Logowanie, prosty widok listy uczniów i lekcji (US-001 do US-022). | **17 SP** |
| **Should Have** | --- (Przesunięte do kolejnych iteracji) | 0 SP |
| **Could Have** | --- (Przesunięte do kolejnych iteracji) | 0 SP |
| **Won't Have** | Faktury, panele ucznia, statystyki, płatności, maile. | N/A |

*Wniosek: Zakres Must Have (17 SP) jest realistyczny do wdrożenia przez jedną osobę w czasie 20 godzin przy wykorzystaniu bibliotek Shadcn i bazy Supabase.*

---

## Kryteria Akceptacji

### US-010: Dodawanie ucznia do bazy
**Kryteria akceptacji:**
1. ✅ Użytkownik widzi formularz dodawania ucznia.
2. ✅ Formularz wymaga podania co najmniej Imienia i Nazwiska.
3. ✅ Po kliknięciu "Zapisz", dane lądują w bazie Supabase.
4. ✅ Uczeń pojawia się natychmiast na liście uczniów (widok aktualizuje się).
5. ✅ Jeśli pola obowiązkowe są puste, formularz wyświetla błąd walidacji (np. za pomocą Zod).

### US-020: Dodawanie nowych zajęć
**Kryteria akceptacji:**
1. ✅ Użytkownik widzi formularz tworzenia zajęć.
2. ✅ Użytkownik musi wybrać z listy (dropdown) wcześniej dodanego ucznia.
3. ✅ Użytkownik musi wprowadzić datę i czas trwania lekcji.
4. ✅ Po zapisaniu, lekcja jest widoczna na głównej liście zajęć wraz z przypisanym do niej uczniem.

---

*Status: Scope zredukowany i zatwierdzony dla MVP (20h)*
