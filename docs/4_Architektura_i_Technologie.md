# Architektura i Technologie

## Spis Treści

1. [Wprowadzenie](#wprowadzenie)
2. [Przegląd Architektury](#przegląd-architektury)
3. [Technologie Frontendowe](#technologie-frontendowe)
4. [Technologie Backendowe](#technologie-backendowe)

---

## 1. Wprowadzenie

Niniejszy dokument przedstawia przegląd architektury technologicznej platformy EduSync. 
**Ważne:** Z uwagi na ograniczenia czasowe (ok. 20 godzin na realizację), projekt jest realizowany w formie MVP (Minimum Viable Product). Skupiamy się wyłącznie na kluczowych funkcjonalnościach (CRUD dla zajęć i uczniów), odkładając zaawansowane moduły na późniejsze etapy.

**Zasady przewodnie:**
- **Prostota** — wybieramy sprawdzone, popularne technologie pozwalające na szybki development.
- **Szybkość wdrożenia** — korzystamy z gotowych komponentów UI i rozwiązań BaaS.

---

## 2. Przegląd Architektury

### Model Aplikacji

EduSync jest aplikacją **SPA (Single Page Application)** z backend-as-a-service (BaaS), co oznacza:
- Cały interfejs użytkownika ładuje się jednorazowo w przeglądarce.
- Komunikacja z serwerem odbywa się przez API.
- Backend oparty na usługach chmurowych (Supabase).

### Wzorce Architektoniczne

| Wzorzec | Zastosowanie |
|---------|--------------|
| **Client-Server** | Frontend (React) ↔ Backend (Supabase) |
| **RESTful API** | Komunikacja z bazą danych przez wygenerowane API Supabase |

---

## 3. Technologie Frontendowe

### 3.1. React & Vite
Aplikacja bazuje na React 18+ (język: TypeScript) uruchamianym za pomocą Vite dla błyskawicznego środowiska deweloperskiego. Wybór ten gwarantuje popularny, komponentowy model pracy i ogromny ekosystem.

### 3.2. Styling & UI (Tailwind CSS + Shadcn)
Aby maksymalnie skrócić czas budowania interfejsu (ograniczenie 20h), zrezygnowano z pisania czystego CSS na rzecz:
- **Tailwind CSS:** Do szybkiego stylowania za pomocą klas narzędziowych.
- **Shadcn UI:** Zestaw gotowych, dostępnych (WCAG) i profesjonalnie wyglądających komponentów (przyciski, formularze, tabele), które można łatwo skopiować do projektu.

### 3.3. Dodatkowe Biblioteki Frontendowe

| Biblioteka | Zastosowanie |
|------------|--------------|
| **React Router** | Nawigacja i routing aplikacji (ochrona tras logowania) |
| **React Hook Form** | Obsługa formularzy (dodawanie uczniów/zajęć) |
| **Zod** | Walidacja danych w formularzach |
| **date-fns** | Proste operacje na datach przy planowaniu zajęć |

---

## 4. Technologie Backendowe

### 4.1. Supabase

Wybrano Supabase jako Backend-as-a-Service, aby uniknąć czasochłonnego pisania własnego serwera. Oferuje on gotową bazę PostgreSQL.

**Wykorzystane Moduły Supabase (MVP):**
- **PostgreSQL:** Główna relacyjna baza danych.
- **Auth:** Uwierzytelnianie użytkowników (logowanie/rejestracja za pomocą e-mail/hasło).
- **Row Level Security (RLS):** Zabezpieczenie bazy, aby użytkownik widział tylko swoje dane.

### 4.2. Uproszczony Schema Bazy Danych (MVP)

Wersja MVP posiada zredukowaną strukturę tabel, skupiającą się wyłącznie na obsłudze uczniów i zajęć.

```sql
-- Profile użytkowników (powiązane z Sup
