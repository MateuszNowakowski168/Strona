# Living Spec — Aplikacja Sprawdzacz Ważności

## 1. Co i dla kogo
* **Produkt:** Prosta aplikacja webowa do zapisywania dat ważności produktów spożywczych/kosmetycznych i wysyłania przypomnień o kończącym się terminie.
* **Użytkownik:** Każdy, kto chce przestać marnować jedzenie i pieniądze z powodu przegapienia daty ważności w domowej spiżarni lub lodówce.

## 2. Ekrany i dane
### Ekrany:
* **Ekran główny (Dashboard):** Lista wszystkich dodanych produktów posortowana od tych, które psują się najszybciej, z wizualnym oznaczeniem (np. kolor czerwony dla pilnych).
* **Formularz dodawania/edycji:** Prosty widok z polami do wprowadzenia nowego produktu.

### Dane (Pola w bazie/stanie):
* `id` (unikalny identyfikator)
* `nazwa_produktu` (tekst, np. "Mleko", "Krem do twarzy")
* `data_waznosci` (data RRRR-MM-DD)
* `kategoria` (opcjonalnie: jedzenie, kosmetyki, leki)
* `status` (w normie / kończy się termin / przeterminowane)

## 3. Definicja „gotowe” (MVP)
1. Użytkownik może dodać produkt z nazwą oraz datą ważności i zobaczyć go na liście ułożonej chronologicznie.
2. System automatycznie wylicza pozostałe dni i oznacza produkty bliskie przeterminowania (np. mniej niż 3 dni).
3. System wysyła proste powiadomienie (np. alert na stronie, e-mail lub powiadomienie push) o produktach wymagających uwagi.

## 4. Czego nie robimy (Poza zakresem MVP)
* Nie robimy systemu kont i logowania użytkowników (na razie aplikacja działa lokalnie dla jednego użytkownika).
* Nie robimy skanowania kodów kreskowych ani rozpoznawania produktów ze zdjęć paragonów.
* Nie robimy zaawansowanych statystyk ani wykresów ile jedzenia zmarnowano w skali miesiąca.
* Nie robimy integracji z kalendarzami zewnętrznymi (Google Calendar, Outlook).
