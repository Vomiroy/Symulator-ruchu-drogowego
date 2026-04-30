Uworzenie odcinka drogi
połącząnego z istniejeącą drogą lub nie
problem wielu pasów 



```mermaid
flowchart TD
    A((Start
Uruchomienie programu)) --> B[Wybranie typu drogi]

    B --> B1{Czy odcinek drogi znajduje się na mapie?}
    B1 -- Nie --> C[Wybranie początku drogi przez kliknięcie punktu na mapie]
    B1 -- Tak --> B2[Edycja rodzaju odcinka drogi istniejącego odcinka drogi]
    B2 --> E
    C --> D[Wybranie końca drogi przez kliknięcie punktu na mapie]
    D --> E{Czy odcinek drogi odzwiercielda rzeczywisty kształt?}
    E -- Tak --> F((Koniec))
    E -- Nie/Usunięcie --> G[Usunięcie utworzonego odcinka drogi]
    E -- Nie/Edycja --> B2 
    G --> B  
```
flowchart TD
    A[User visits website] --> B{Is user logged in?}

    B -- No --> C[Show login/signup page]
    C --> D[User enters credentials]
    D --> E{Valid credentials?}

    E -- No --> F[Show error message]
    F --> C

    E -- Yes --> G[Redirect to dashboard]

    B -- Yes --> G

    G --> H[User browses content]
    H --> I{User performs action?}

    I -- View item --> J[Display item details]
    I -- Logout --> K[Log out user]

    J --> H
    K --> A
