# Architektura i Technologie

## Spis Treści

1. [Wprowadzenie](#wprowadzenie)
2. [Przegląd Architektury](#przegląd-architektury)
3. [Technologie Frontendowe](#technologie-frontendowe)
4. [Technologie Backendowe](#technologie-backendowe)


---

## Wprowadzenie

Niniejszy dokument przedstawia szczegółowy przegląd architektury technologicznej platformy EduSync. Dokument opisuje wybór technologii, uzasadnienie decyzji architektonicznych oraz integracje z usługami zewnętrznymi.

**Zasady przewodnie:**

- **Prostota** — wybieramy sprawdzone, popularne technologie
- **Skalowalność** — architektura musi obsłużyć wzrost liczby użytkowników
- **Bezpieczeństwo** — ochrona danych użytkowników jest priorytetem
- **Koszt-efektywność** — optymalizacja kosztów przy zachowaniu jakości

---

## Przegląd Architektury

### Model Aplikacji

EduSync jest aplikacją **SPA (Single Page Application)** z backend-as-a-service (BaaS), co oznacza:

- Cały interfejs użytkownika ładuje się jednorazowo
- Komunikacja z serwerem odbywa się przez API
- Stan aplikacji zarządzany lokalnie (client-side)
- Backend oparty na usługach chmurowych (Supabase)

### Wzorce Architektoniczne

| Wzorzec | Zastosowanie |
|---------|--------------|
| **Client-Server** | Frontend (React) ↔ Backend (Supabase) |
| **RESTful API** | Komunikacja przez REST/GraphQL |
| **Serverless** | Edge Functions dla logiki biznesowej |
| **Event-Driven** | Webhooks dla powiadomień |

---

## Technologie Frontendowe

### 3.1. React

| Aspekt | Opis |
|--------|------|
| **Wersja** | React 18+ (z Concurrent Mode) |
| **Język** | TypeScript |
| **Dlaczego?** | Najpopularniejszy framework, ogromna społeczność, bogaty ekosystem |
| **Korzyści** | Komponentowy model, wirtualny DOM, hooks API |

**Struktura projektu:**

```
src/
├── components/       # Komponenty React
├── pages/           # Strony aplikacji
├── hooks/           # Custom hooks
├── services/        # Serwisy API
├── store/           # Stan aplikacji (Zustand/Redux)
├── utils/           # Funkcje pomocnicze
└── types/           # Definicje TypeScript
```

### 3.2. Tailwind CSS

| Aspekt | Opis |
|--------|------|
| **Wersja** | Tailwind CSS 3.x |
| **Dlaczego?** | Szybki rozwój, brak konfliktu klas, mały rozmiar bundle |
| **Korzyści** | Spójny design system, responsywność out-of-the-box |

**Konfiguracja:**

- Customowy config z design tokens (kolory, fonty, spacing)
- Komponenty zgodne z WCAG (dostępność)
- Dark mode support

### 3.3. Vite

| Aspekt | Opis |
|--------|------|
| **Wersja** | Vite 5.x |
| **Dlaczego?** | Błyskawiczny dev server, szybki build |
| **Korzyści** | HMR (Hot Module Replacement), optymalizacje produkcyjne |

### 3.4. Dodatkowe Biblioteki Frontendowe

| Biblioteka | Zastosowanie |
|------------|--------------|
| **React Router** | Routing aplikacji |
| **React Query** | Zarządzanie stanem serwerowym (caching, synchronizacja) |
| **Zustand** | Globalny stan aplikacji (lokalny) |
| **React Hook Form** | Formularze z walidacją |
| **Zod** | Walidacja schematów danych |
| **date-fns** | Operacje na datach |
| **React Calendar** | Komponent kalendarza |
| **Recharts** | Wykresy i wykresy |
| **React Email** | Szablony email |

---

## Technologie Backendowe

### 4.1. Supabase

| Aspekt | Opis |
|--------|------|
| **Usługa** | Backend-as-a-Service (BaaS) |
| **Baza danych** | PostgreSQL |
| **Dlaczego?** | Open-source'owy Firebase alternative, silny PostgreSQL |
| **Korzyści** | Auth, Database, Storage, Edge Functions, Realtime |

**Moduły Supabase:**

| Moduł | Zastosowanie |
|-------|--------------|
| **PostgreSQL** | Główna baza danych |
| **Auth** | Uwierzytelnianie użytkowników (JWT) |
| **Storage** | Przechowywanie plików (avatars, materials) |
| **Edge Functions** | Serverless functions (logika biznesowa) |
| **Realtime** | Live aktualizacje (chat, kalendarz) |
| **Row Level Security** | Bezpieczeństwo na poziomie wierszy |

### 4.2. Schema Bazy Danych

#### Główne tabele:

```sql
-- Użytkownicy (rozszerzenie auth.users)
profiles (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES auth.users,
  email VARCHAR,
  first_name VARCHAR,
  last_name VARCHAR,
  phone VARCHAR,
  avatar_url TEXT,
  role ENUM('tutor', 'student', 'owner', 'admin'),
  created_at TIMESTAMP,
  updated_at TIMESTAMP
)

-- Szkoły (dla właścicieli)
organizations (
  id UUID PRIMARY KEY,
  name VARCHAR,
  nip VARCHAR,
  address TEXT,
  owner_id UUID REFERENCES profiles,
  created_at TIMESTAMP
)

-- Uczniowie
students (
  id UUID PRIMARY KEY,
  organization_id UUID REFERENCES organizations,
  first_name VARCHAR,
  last_name VARCHAR,
  email VARCHAR,
  phone VARCHAR,
  notes TEXT,
  created_at TIMESTAMP
)

-- Zajęcia
lessons (
  id UUID PRIMARY KEY,
  organization_id UUID REFERENCES organizations,
  tutor_id UUID REFERENCES profiles,
  student_id UUID REFERENCES students,
  scheduled_at TIMESTAMP,
  duration_minutes INTEGER,
  status ENUM('scheduled', 'completed', 'cancelled'),
  topic VARCHAR,
  notes TEXT,
  created_at TIMESTAMP
)

-- Faktury
invoices (
  id UUID PRIMARY KEY,
  organization_id UUID REFERENCES organizations,
  student_id UUID REFERENCES students,
  invoice_number VARCHAR,
  amount DECIMAL,
  vat_amount DECIMAL,
  status ENUM('pending', 'paid', 'overdue', 'cancelled'),
  due_date DATE,
  paid_at TIMESTAMP,
  created_at TIMESTAMP
)

-- Płatności
payments (
  id UUID PRIMARY KEY,
  invoice_id UUID REFERENCES invoices,
  amount DECIMAL,
  payment_method VARCHAR,
  stripe_payment_id VARCHAR,
  status VARCHAR,
  created_at TIMESTAMP
)
```

---




## Następne Kroki

1. [ ] Konfiguracja projektu React z Vite
2. [ ] Setup Supabase (baza, auth, storage)
3. [ ] Połączenie Stripe
4. [ ] Implementacja pierwszych User Stories
5. [ ] Deployment produkcyjny

---

*Document Version: 1.0*  
*Last Updated: 2025*  
*Author: Technical Architecture Team*  
*Status: Approved for Implementation*
