# Mini Projekt 1 (MP1): Biblioteka Libre

Projekt zrealizowany w ramach laboratorium **Systemy zarządzania treścią (CMS)** na Collegium Da Vinci w Poznaniu (rok akademicki 2026/2027, prowadzący: mgr inż. Łukasz Grala)[cite: 2, 7, 11].

---

## 1. Karta MP1: opis instytucji, persony i mapa strony (Moduł L1)[cite: 4]

### Charakterystyka projektu
* **Nazwa:** Biblioteka Libre
* **Hasło przewodnie:** *Pobudza wyobraźnię i pozwala oderwać się od rzeczywistości.*[cite: 27]
* **Oferta:** Wypożyczalnia książek tradycyjnych i literatury edukacyjnej, czytelnia stacjonarna z dostępem do Wi-Fi, spotkania autorskie, rekomendacje czytelnicze oraz aktualności kulturalne.
* **Grupa docelowa:** Studenci szukający literatury naukowej i miejsca do nauki, mieszkańcy Poznania czytający beletrystykę, seniorzy oraz rodziny z dziećmi.

### Persony (2 profile użytkowników)[cite: 4]

| Cecha | Persona 1: Anna Kowalska (Studentka) | Persona 2: Marek Nowak (Miłośnik literatury) |
| :--- | :--- | :--- |
| **Wiek i zawód** | 21 lat, studentka informatyki (CDV Poznań) | 44 lata, architekt, mieszkaniec Poznania |
| **Cel** | Szybko sprawdzić dostępność podręczników akademickich i godziny otwarcia czytelni. | Znaleźć nowości wydawnicze, sprawdzić polecane książki i zapisać się do biblioteki. |
| **Problem** | Brak czasu na szukanie informacji w nieczytelnych katalogach i przeładowanych stronach. | Trudność w nawigacji na smartfonie (zbyt małe przyciski i nieczytelny kontrast). |
| **Urządzenie** | Smartfon (ekran 375 px, przeglądanie w drodze na uczelnię) | Laptop (ekran Desktop 1280 px, wieczorne przeglądanie oferty)[cite: 11] |
| **Oczekiwana akcja (CTA)** | Kliknięcie przycisku **„Zobacz więcej”** na stronie głównej i przejście do katalogu **„Książki”**[cite: 27]. | Przejście do zakładki **„Kontakt”** w celu uzyskania karty bibliotecznej. |

### Mapa strony (Sitemap)[cite: 4]
Struktura obejmuje 6 podstron na maksymalnie 2 poziomach zagłębienia[cite: 4]:

* **Strona główna** (`/`) – sekcja Hero (H1 + CTA), polecane książki, zalety biblioteki, zespół, opinie czytelników[cite: 8, 27].
* **O nas** (`/o-nas/`) – historia Biblioteki Libre, misja i godziny otwarcia.
* **Książki** (`/ksiazki/`) – przegląd zbiorów, literatura piękna i edukacyjna (wykorzystuje zapisany wzorzec bloków Hero)[cite: 8, 27].
* **Blog** (`/blog/`) – aktualności biblioteczne, relacje ze spotkań i recenzje (kategorie: *Nowości wydawnicze*, *Wydarzenia*).
* **Kontakt** (`/kontakt/`) – adres, telefon, e-mail, formularz kontaktowy[cite: 4, 14].
* **Polityka prywatności** (`/polityka-prywatnosci/`) – informacje o przetwarzaniu danych osobowych (RODO) i plikach cookies[cite: 4, 12, 13].

### Uzasadnienie wyboru systemu CMS (WordPress)[cite: 4]
Według danych W3Techs (październik 2026) WordPress napędza **40,2%** wszystkich stron w internecie i posiada **58,7%** udziału w rynku systemów CMS, wyprzedzając rozwiązania SaaS takie jak Shopify (7,8%) czy Wix (6,1%) oraz system Drupal (0,6%)[cite: 2]. Wybór WordPressa (model *self-hosted*) daje Bibliotece Libre pełną własność bazy danych i treści bez ryzyka uzależnienia od dostawcy (*vendor lock-in*) oraz stałych opłat abonamentowych[cite: 2, 5]. Dodatkowo wbudowany edytor blokowy (Gutenberg) i Full Site Editing pozwalają bibliotekarzom na łatwą publikację aktualności i zarządzanie wzorcami bloków bez znajomości programowania[cite: 2, 7].

---

## 2. Architektura informacji i projekt interfejsu (Moduł L2)[cite: 7]

### Wireframe strony głównej[cite: 8]
```text
+-------------------------------------------------------------------+
| [LOGO: Biblioteka Libre]   Strona główna | O nas | Książki | ...  |
+-------------------------------------------------------------------+
| [SEKCJA HERO]                                                     |
| H1: Pobudza wyobraźnię i pozwala oderwać się od rzeczywistości.   |
| [Przycisk CTA: Zobacz więcej]            [Zdjęcia książek]        |
+-------------------------------------------------------------------+
| [PASEK KORZYŚCI - 3 KOLUMNY]                                      |
| Gwarancja jakości   |   Łatwy dostęp   |   Poznaj nasz zespół     |
+-------------------------------------------------------------------+
| [POLECANE KSIĄŻKI - SIATKA / KARTY]                               |
| [Książka 1]         |   [Książka 2]    |   [Książka 3]            |
+-------------------------------------------------------------------+
| [OPINIE CZYTELNIKÓW - BLOK CYTAT]                                 |
| „Świetne miejsce do nauki i bogaty księgozbiór.” – Anna K.        |
+-------------------------------------------------------------------+
| [STOPKA]                                                          |
| Biblioteka Libre | Kontakt | Polityka prywatności | © 2026        |
+-------------------------------------------------------------------+
3. Dostępność WCAG 2.2, style i aspekty prawne (Moduł L3)Tabela kontrastu kolorów (WCAG 2.2 AA – min. 4,5:1)Element interfejsuKolor tekstuKolor tłaWspółczynnik kontrastuStatus WCAG AATekst główny na stronie#1A1A1A#FFFFFF17.

4 : 1Spełnia (AAA)Nagłówki sekcji (H1–H3)#1E1E1E#FFFFFF16.5 : 1Spełnia (AAA)Przycisk główny CTA#FFFFFF#B82E2E5.6 : 1Spełnia (AA)Pasek informacyjny w stopce#FFFFFF#22222215.9 : 1Spełnia (AAA)Wdrożone poprawki dostępności (Dodatkowy CSS + audyt)WCAG 2.4.7 (Focus Visible): Dodano wyraźne obramowanie outline: 3px solid #1a1a1a dla elementów nawigowanych klawiaturą (Tab).   WCAG 2.4.11 (Focus Not Obscured): Ustawiono scroll-padding-top: 6rem, aby elementy z fokusem nie chowały się pod nagłówkiem.   WCAG 2.5.8 (Target Size Minimum): Zapewniono minimalny rozmiar celów dotykowych 24x24 px dla linków nawigacji i przycisków[cite: 11, 13].Płynna typografia: Zastosowano funkcję clamp(1.75rem, 1.2rem + 2.5vw, 3rem) dla nagłówka H1.   Wykaz źródeł i licencji materiałów (RODO / Prawa autorskie)System CMS: WordPress (licencja GPLv2+).   Motyw graficzny i zdjęcia demonstracyjne: Motyw biblioteczny z oficjalnego katalogu WordPress.org (licencja GPLv2+).   Wtyczki: Contact Form 7 (licencja GPLv2+).   Fonty: Fonty systemowe / lokalne z Biblioteki fontów WordPress (licencja OFL – hostowane lokalnie bez zewnętrznych zapytań do serwerów Google, zgodnie z RODO).   
