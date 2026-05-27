# Model domeny
## Encje
- **Węzły (do tworzenia ścieżek)** - punkty kontrolne wykorzystywane do tworzenia oraz łączenia odcinków dróg i tras przejazdu.
- **Odcinek drogi** - fragment drogi pomiędzy węzłami, posiadający określone parametry i zasady ruchu.
- **Typ Drogi** - definicja rodzaju drogi określająca jej kształt oraz właściwości wizualne i funkcjonalne.
- **Trasy** - wyznaczone ścieżki przejazdu pojazdów składające się z połączonych węzłów i odcinków dróg.
- **Pojazdy** - obiekty uczestniczące w symulacji ruchu, poruszające się po wyznaczonych trasach.
- **Typ pojazdu** - definicja parametrów i właściwości danego rodzaju pojazdu, np. prędkości czy masy.
- **Znaki drogowe i sygnalizacja świtlna** - elementy infrastruktury drogowej sterujące ruchem pojazdów i pieszych.
- **Reguły/Zasady ruchu** - zestaw zasad obowiązujących na danym odcinku drogi lub wynikających ze znaków drogowych.
- **Zdarzenia na drodze** - sytuacje występujące podczas symulacji, np. kolizje, korki lub zatrzymania ruchu.

## Relacje
* **Odcinek drogi 🡢 Węzeł** (1:N) *Odcinek drogi* jest zbudowany z *węzłów* 
* **Odcinek drogi 🡢 Zasady** (1:N) *Odcinek drogi* posiada *zasady*
* **Odcinek drogi 🡢 Typ Drogi** (1:1) *Odcinek drogi* jest *typu*
* **Znaki drogowe 🡢 Zasady** (1:1) *Znak* dyktuje *zasady*
* **Trasy 🡢 Węzły** (1:N) *Trasa* przechodzi przez *Węzły*
* **Pojazdy 🡢 Trasy** (1:1) *Pojazd* jedzie *trasą*
* **Pojazdy 🡢 Typ pojazdu** (1:1) *Pojazd* jest *typu*
* **Trasy 🡢 Zdarzenie na drodze** (0..1:N) Na *trasie* występuje wiele *zdarzeń na drodze*
## Uwagi

```mermaid
erDiagram

    ZNAKI_DROGOWE {
        int id
        string nazwa
        string typ
        string opis
        string stan
    }

    ZASADY {
        int id
        string typ_zasady
        string wartosc
        string opis
    }

    ODCINEK_DROGI {
        int id
        string nazwa
        float dlugosc
        int liczba_pasow
        string kierunek
        float ograniczenie_predkosci
    }

    TYP_DROGI {
        int id
        string nazwa
        string ksztalt
        string tekstura
        float domyslny_promien
    }

    WEZEL {
        int id
        float pozycja_x
        float pozycja_y
        string typ
    }

    TRASY {
        int id
        string nazwa
        float dlugosc
        string status
    }

    POJAZDY {
        int id
        string model
        float aktualna_predkosc
        float przyspieszenie
        string stan
    }

    TYP_POJAZDU {
        int id
        string nazwa
        float maksymalna_predkosc
        float masa
        float dlugosc
    }

    ZDARZENIE_NA_DRODZE {
        int id
        string typ
        string opis
        datetime czas_wystapienia
        string priorytet
    }

    %% Relacje
    ZNAKI_DROGOWE ||--|| ZASADY : "dyktuje"

    ODCINEK_DROGI ||--o{ ZASADY : "posiada"
    ODCINEK_DROGI ||--|| TYP_DROGI : "jest_typu"
    ODCINEK_DROGI ||--o{ WEZEL : "zbudowany_z"

    TRASY ||--o{ WEZEL : "przechodzi_przez"

    POJAZDY ||--|| TRASY : "jedzie"
    POJAZDY ||--|| TYP_POJAZDU : "jest_typu"

    TRASY o|--o{ ZDARZENIE_NA_DRODZE : "wystepuje"
```
