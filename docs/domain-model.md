# Model domeny
## Encje
- Węzły (do tworzenia ścieżek)
- Odcinek drogi
- Drogi (kategoria)
- Trasy
- Pojazdy
- Pojazd (kategoria)
- Znaki drogowe i sygnalizacja świtlna
- Reguły/Zasady ruchu
- Zdarzenia na drodze

## Relacje
* **Odcinek drogi >-< Węzeł**
* **Zasady >- Odcinek drogi**
* **Zasady -- Znaki drogowe**
* **Odcinek drogi -< Drogi (kategoria)**
* **Trasy -< Węzły**
* **Pojazdy -< Trasy**
* **Pojazd (kategoria) -- Pojazdy**
* **Zdarzenie na drodze >- Trasy**
## Uwagi


```mermaid
erDiagram
    ODCINEK_DROGI }|--|{ WEZEL : connects

    ZASADY ||--o{ ODCINEK_DROGI : applies_to
    ZASADY ||--|| ZNAKI_DROGOWE : defines

    ODCINEK_DROGI }o--|| DROGI_KATEGORIA : categorized_as

    TRASY ||--o{ WEZLY : includes
    POJAZDY ||--o{ TRASY : uses

    POJAZD_KATEGORIA ||--o{ POJAZDY : groups

    ZDARZENIE_NA_DRODZE }o--|| TRASY : occurs_on
```
