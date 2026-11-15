# Karta projektu MP1: Palarnia Kawy Ziarno & Pasja

## 1. Opis firmy
* **Nazwa:** Palarnia Kawy Ziarno & Pasja
* **Oferta:** Rzemieślnicza kawa ziarnista i mielona świeżo wypalana na zamówienie, zestawy degustacyjne, akcesoria do parzenia (drip, chemex) oraz subskrypcja kawowa dla klientów indywidualnych i biur.
* **Grupa docelowa:** Miłośnicy kawy specialty (25–45 lat) parzący kawę w domu oraz właściciele małych biur i kawiarni szukający stałego dostawcy.

## 2. Persony
* **Persona 1: Marek (32 lata, programista pracujący zdalnie)**
  * **Cel:** Chce szybko zamówić świeżo paloną kawę pod ekspres przelewowy z dostawą do domu.
  * **Problem:** Trudno mu dobrać profil smakowy ziaren bez czytania długich opisów.
  * **Urządzenie:** Smartfon (przegląda w przerwie od pracy).
  * **Oczekiwana akcja (CTA):** Przejście do zakładki *Oferta* i wybór konkretnego rodzaju kawy.

* **Persona 2: Anna (41 lat, Office Manager w firmie IT)**
  * **Cel:** Szuka stałego dostawcy dobrej kawy do ekspresu biurowego na fakturę VAT.
  * **Problem:** Brak jasnej informacji o rabatach hurtowych i warunkach współpracy B2B.
  * **Urządzenie:** Laptop / komputer stacjonarny.
  * **Oczekiwana akcja (CTA):** Wypełnienie formularza zapytania ofertowego w zakładce *Kontakt*.

## 3. Mapa strony (Sitemap)
* **Strona główna**
  * **O nas** (historia palarni, proces wypalania)
  * **Oferta**
    * *Kawy jednorodne (Single Origin)*
    * *Mieszanki (Blendy) i zestawy*
  * **Dla firm (B2B)** (współpraca dla biur i gastronomii)
  * **Blog / Poradnik** (przepisy na parzenie kawy)
  * **Kontakt** (formularz kontaktowy, dane firmy)
  * **Polityka prywatności** (wymogi RODO)

## 4. Uzasadnienie wyboru systemu CMS
Wybieram system **WordPress**, ponieważ według danych W3Techs (październik 2026) napędza on 40,2% wszystkich stron w internecie i posiada 58,7% udziału w rynku CMS, co gwarantuje ogromne wsparcie społeczności oraz bezpieczeństwo rozwoju. W przeciwieństwie do rozwiązań SaaS (takich jak Wix czy Shopify), model self-hosted daje pełną własność danych oraz brak uzależnienia od abonamentu dostawcy (vendor lock-in). Z kolei względem systemu Drupal (0,6% rynku), który jest dedykowany dużym portalom korporacyjnym, WordPress zapewnia znacznie niższy koszt wdrożenia i intuicyjny panel edycji treści dla małej palarni kawy.

## 5. Użycie AI
* **Narzędzie:** Gemini
* **Zakres użycia:** Pomoc w wygenerowaniu struktury pliku `docker-compose.yml`, szkicu opisów person oraz propozycji treści na stronę „O nas”.
* **Poprawki ręczne:** Samodzielnie zweryfikowałem poprawność wcięć w pliku YAML, dostosowałem hasła bazy danych, skonfigurowałem środowisko w Playground i Codespaces oraz dopasowałem strukturę podstron do wymagań zadania.