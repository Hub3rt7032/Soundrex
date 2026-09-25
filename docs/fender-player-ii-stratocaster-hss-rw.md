### Udało się przenieść:

* nazwę produktu
* zdjęcia (osobno per wariant koloru)
* cenę
* SKU
* opis (specyfikacja wpisana ręcznie w opis) (Patrz "obejscie")
* warianty (kolor, podstrunnica)
* dane dostawy (wymiary, waga)
* kategorię
* status Published — produkt widoczny na froncie

### Nie udało się przenieść:

* podmiany zdjęcia przy zmianie wariantu na froncie — dane są poprawnie zapisane w panelu, ale galeria produktu ma atrybut `wire:ignore`, więc Livewire nie ma prawa jej zaktualizować (blokada wynika z konfliktu z biblioteką Swiper, która zarządza karuzelą); cena i SKU aktualizują się poprawnie, zdjęcie nie
* szczegółowej tabeli specyfikacji technicznej (brak dedykowanych pól, wpisane ręcznie w opis)
* próbek dźwiękowych i widoku 360°
* opinii i ocen z zewnętrznych platform
* informacji o gwarancji
* EAN — nie było dostępne w źródle (Thomann go nie pokazuje, mimo że Milio ma to pole)

### Co uproszczono:

* tylko 3 z 7 kolorów oryginału (3-Color Sunburst, Black, Aquatone Blue)
* dla wariantów Black i Aquatone Blue brak pełnych, osobno zweryfikowanych danych producenta (cena i SKU oparte na wariancie głównym, nie pobrane indywidualnie z Thomanna)


### Co zrobiono obejściem:

* szczegółowa specyfikacja techniczna (korpus, szyjka, podstrunnica, przetworniki, mostek itd.) wpisana ręcznie jako tekst w polu Description, zamiast w osobne pola atrybutów — bo Milio nie ma dla tej kategorii dedykowanych pól na taką specyfikację