**US1** 

Jako "użytkownik" chcę projektować szlaki dróg, aby mieć wgląd na ruch pojazdów

**AC1**

Użytkownik może tworzyć odcinki dróg na mapie za pomocą edytora.
Użytkownik może łączyć odcinki dróg w skrzyżowania.
Użytkownik może edytować długość, szerokość oraz kierunek drogi.
System wyświetla podgląd utworzonej trasy w czasie rzeczywistym.
Zapisane zmiany są widoczne natychmiast po ich wprowadzeniu.

------------------------------------------------------------------------------------------------

**US2**

Jako "użytkownik" chcę symulować ruch pojazdów, aby ocenić wykonanie dróg

**AC2**

Użytkownik może uruchomić oraz zatrzymać symulację ruchu.
System generuje ruch pojazdów na utworzonych drogach.
Pojazdy poruszają się zgodnie z wyznaczonymi pasami ruchu.
System wyświetla aktualne położenie i ruch pojazdów w czasie rzeczywistym.
Użytkownik może zmieniać parametry symulacji bez konieczności restartu aplikacji.

------------------------------------------------------------------------------------------------

**US3**

Jako "użytkownik" chcę mieć możliwość zapisu utworzonej mapy, aby nie tworzyć jej od nowa

**AC3**

Użytkownik może zapisać mapę lokalnie lub w bazie danych.
System zapisuje wszystkie elementy mapy wraz z konfiguracją.
Użytkownik może nadać nazwę zapisywanej mapie.
Po ponownym uruchomieniu programu użytkownik może otworzyć wcześniej zapisane mapy.
System informuje użytkownika o poprawnym zapisaniu mapy.

------------------------------------------------------------------------------------------------

**US4**
Jako "użytkownik" chcę mieć możliwość udostępnienia swojej mapy w bazie danych, aby inni użytkownicy mogli ją wykorzystać

**AC4**

Użytkownik może oznaczyć mapę jako publiczną.
System zapisuje mapę w centralnej bazie danych.
Inni użytkownicy mogą wyszukiwać udostępnione mapy.
System przechowuje informacje o autorze mapy.
Użytkownik może wycofać udostępnioną mapę.

------------------------------------------------------------------------------------------------

**US5**

Jako "użytkownik" chcę mieć możliwość pobrania mapy z bazy danych udostępnionych przez innych użytkowników, aby móc je wykorzystać

**AC5**

Użytkownik może przeglądać listę publicznych map.
Użytkownik może wyszukiwać mapy po nazwie lub autorze.
Użytkownik może pobrać wybraną mapę do swojej kolekcji.
Pobraną mapę można edytować lokalnie.
System informuje o poprawnym pobraniu mapy.

------------------------------------------------------------------------------------------------

**US6**

Jako "użytkownik" chcę mieć dostęp do gotowych obiektów, aby nie było potrzeby tworzenia ich od podstaw

**AC6**

System udostępnia bibliotekę gotowych obiektów drogowych.
Użytkownik może dodawać gotowe obiekty metodą „przeciągnij i upuść”.
Dostępne obiekty obejmują m.in. drogi, skrzyżowania, ronda i przejścia dla pieszych.
Użytkownik może edytować właściwości dodanych obiektów.
Obiekty są dostępne bez konieczności dodatkowej konfiguracji.

------------------------------------------------------------------------------------------------

**US7**

Jako "użytkownik" chcę importować do programu własne elementy, aby korzystać z obiektów, których nie oferuje sam program

**AC7**

Użytkownik może importować własne modele i tekstury.
System obsługuje określone formaty plików (np. OBJ, FBX, PNG).
Zaimportowane elementy są widoczne w bibliotece użytkownika.
Użytkownik może używać własnych obiektów w projektowanej mapie.
System wyświetla komunikat o błędzie w przypadku nieobsługiwanego formatu.

------------------------------------------------------------------------------------------------

**US8**

Jako "użytkownik" chcę ustawić odpowiednie zasady ruchu dla danego odcinka drogi, aby pojazdy dostosowywały się do nich

**AC8**

Użytkownik może ustawić ograniczenie prędkości dla wybranego odcinka drogi.
Użytkownik może określić kierunek ruchu oraz liczbę pasów.
System umożliwia ustawienie pierwszeństwa przejazdu.
Pojazdy podczas symulacji przestrzegają przypisanych zasad ruchu.
Zmiany zasad ruchu są widoczne natychmiast w symulacji.

------------------------------------------------------------------------------------------------

**US9**

Jako "użytkownik" chcę umieszczać np. znaki drogowe/sygnalizacje świetlne z ustalonymi zasadami, aby pojazdy poruszały się odpowiednio

**AC9**

Użytkownik może dodawać znaki drogowe oraz sygnalizację świetlną na mapie.
Użytkownik może konfigurować działanie sygnalizacji świetlnej.
Pojazdy reagują na znaki oraz sygnalizację zgodnie z przepisami.
System umożliwia usuwanie i edycję dodanych elementów.
Zmiany są uwzględniane podczas aktywnej symulacji.

------------------------------------------------------------------------------------------------

**US10**

Jako "użytkownik" chcę symulować ruch pieszych, aby testować zachowanie pojazdów

**AC10**

System umożliwia generowanie ruchu pieszych.
Piesi mogą poruszać się po chodnikach i przejściach dla pieszych.
Pojazdy reagują na obecność pieszych.
Użytkownik może ustalać natężenie ruchu pieszych.
System wykrywa potencjalne kolizje między pojazdami a pieszymi.

------------------------------------------------------------------------------------------------

**US11**

Jako "użytkownik" chcę mieć możliwość ustalania prędkości z jaką mogą poruszać się pojazdy, aby analizować ich zachowanie na drodze

**AC11**

Użytkownik może ustawić maksymalną prędkość dla pojazdów.
Użytkownik może definiować różne profile prędkości dla różnych typów pojazdów.
Pojazdy dostosowują prędkość do warunków ruchu.
System wyświetla aktualną prędkość pojazdów podczas symulacji.
Zmiana parametrów prędkości wpływa na symulację w czasie rzeczywistym.

------------------------------------------------------------------------------------------------

**US12**

Jako "użytkownik" chcę by program odwzorowywał rzeczywistą fizykę pojazdów, aby analizować ich ruch przy ustalonych zasadach i wykrywać możliwe kolizje między pojazdami

**AC12**

System uwzględnia podstawowe prawa fizyki pojazdów (przyspieszenie, hamowanie, masa).
Pojazdy reagują realistycznie na zakręty i przeszkody.
System wykrywa kolizje między pojazdami.
System wyświetla informacje o wykrytych kolizjach.
Użytkownik może analizować przebieg zdarzeń po zakończeniu symulacji.

------------------------------------------------------------------------------------------------

**US13**

Jako "użytkownik" chcę wybrać odpowiedni typ drogi aby odzwierciedlić jej rzeczywisty kształt.

**AC13**

Użytkownik ma do dyspozycji menu/narzędzie z listą predefiniowanych typów dróg (np. prosta, zakręt, skrzyżowanie, rondo).
Po wybraniu typu drogi i umieszczeniu jej na mapie, jej wizualizacja na ekranie odpowiada wybranemu kształtowi.
System pozwala na łączenie różnych typów dróg ze sobą, weryfikując poprawność połączenia (np. zapobiega nakładaniu się na siebie niekompatybilnych węzłów).
Użytkownik może zdefiniować podstawowe parametry kształtu (np. promień zakrętu, liczba pasów, teksture).

------------------------------------------------------------------------------------------------

**US14**

Jako "użytkownik" chcę ustawić dla określonego odcinku drogi natężenie ruchu w wybranych przediałach czasowych. 

**AC14**

Po kliknięciu na wygenerowany odcinek drogi, pojawia się panel konfiguracji natężenia ruchu.
Użytkownik może dodać wiele przedziałów czasowych w formacie "Od HH:MM do HH:MM".
Dla każdego przedziału użytkownik może zdefiniować wartość natężenia (np. liczba pojazdów na godzinę).
Podczas działania symulacji, system automatycznie zwiększa lub zmniejsza liczbę generowanych pojazdów na danym odcinku, zgodnie z aktualnym czasem symulacji i wprowadzonym harmonogramem.

------------------------------------------------------------------------------------------------

**US15**

Jako "użytkownik" chcę zobaczyć miejsca z wysokim prawdopodobieństwem występowania korków ulicznych.

**AC15**

System analizuje natężenie ruchu na wszystkich odcinkach dróg podczas symulacji.
Odcinki o wysokim zagęszczeniu pojazdów są wyróżniane na mapie odpowiednim kolorem.
Użytkownik może wyświetlić przewidywany poziom korków dla wybranego przedziału czasowego.
System aktualizuje dane o korkach w czasie rzeczywistym podczas działania symulacji.
Użytkownik może wyświetlić statystyki średniego czasu przejazdu dla wybranych tras.

------------------------------------------------------------------------------------------------

**US16**

Jako "użytkownik" chcę wyznaczyć trasę podróży pomiędzy ustawionymi punktami spełniającą wymagania określone w ustawieniach aby dowiedzieć się czy obszar jest niezpotymalizowany pod względem 
ruchu jednego z lub wiecej typu lokomocji (samochody, tramwaje, pieszy, rowery, pociągi).

**AC16**

Użytkownik może wskazać punkt początkowy i końcowy trasy.
Użytkownik może wybrać typ środka transportu (samochód, tramwaj, pieszy, rower, pociąg).
System wyznacza trasę zgodną z obowiązującymi zasadami ruchu.
System uwzględnia aktualne warunki ruchu oraz ograniczenia infrastruktury.
Użytkownik może porównać czas przejazdu dla różnych typów transportu.

------------------------------------------------------------------------------------------------

**US17**

Jako "użytkownik" chcę wyznaczyć obszar terenu do zapisu, aby w przyszłości mięc możliwość ich wczytania. 

**AC17**

Użytkownik może zaznaczyć wybrany obszar mapy za pomocą narzędzia zaznaczania.
System zapisuje wszystkie obiekty znajdujące się w zaznaczonym obszarze.
Użytkownik może nadać nazwę zapisywanemu obszarowi.
Zapisany obszar może zostać ponownie wczytany do projektu.
System informuje użytkownika o poprawnym zapisaniu obszaru.

------------------------------------------------------------------------------------------------

**US18**

Jako "użytkownik" chcę utworzyć scenariusz z możliwością zapisu parametrów dróg dla łatwiejszego testowania obszaru w zróżnicowanych przypadkach.

**AC18**

Użytkownik może utworzyć nowy scenariusz symulacji.
System zapisuje konfigurację dróg, sygnalizacji i parametrów ruchu w scenariuszu.
Użytkownik może przełączać się pomiędzy zapisanymi scenariuszami.
Scenariusze mogą być uruchamiane bez konieczności ponownej konfiguracji mapy.
Użytkownik może edytować oraz usuwać zapisane scenariusze.

------------------------------------------------------------------------------------------------

**US19**

Jako "użytkownik" chcę konfigurować cykle sygnalizacji świetlnej na wybranych skrzyżowaniach, aby analizować ich wpływ na przepustowość ruchu.

**AC19**

Użytkownik może wybrać skrzyżowanie posiadające sygnalizację świetlną.
Użytkownik może ustawić długość trwania świateł zielonych, żółtych i czerwonych.
System umożliwia tworzenie wielu faz sygnalizacji.
Pojazdy reagują na sygnalizację zgodnie z aktualnym stanem świateł.
System prezentuje wpływ zmian sygnalizacji na płynność ruchu i długość korków.

------------------------------------------------------------------------------------------------

**US20**

Jako "użytkownik" chcę zdefiniować trasy, rozkłady jazdy oraz przystanki dla transportu publicznego (np. autobusów i tramwajów), 
aby sprawdzić, jak ich obecność wpływa na płynność ruchu pozostałych pojazdów.

**AC20**

Użytkownik może tworzyć linie komunikacyjne dla autobusów i tramwajów.
Użytkownik może definiować przystanki na trasie przejazdu.
Użytkownik może ustalać godziny odjazdów oraz częstotliwość kursów.
Pojazdy transportu publicznego zatrzymują się na przystankach podczas symulacji.
System analizuje wpływ transportu publicznego na natężenie ruchu.

------------------------------------------------------------------------------------------------

**US21**
Jako "użytkownik" chcę mieć możliwość stworzenia zdarzenia na drodze np. wypadku lub robot drowgowych, w określonym miejscu lub odcinku drogi,
aby zobaczyć ich wpływ na reguralny ruch. 


**AC21**

Użytkownik może wybrać miejsce wystąpienia zdarzenia na mapie.
Użytkownik może określić typ zdarzenia (np. wypadek, remont, zamknięcie pasa).
System ogranicza ruch na wskazanym odcinku zgodnie z typem zdarzenia.
Pojazdy podczas symulacji omijają zablokowane odcinki dróg, jeśli istnieje alternatywna trasa.
System prezentuje wpływ zdarzenia na czas przejazdu i tworzenie się korków.

------------------------------------------------------------------------------------------------

**US22**

Jako "użytkownik" chcę modyfikować globalne warunki pogodowe np. deszcz, śnieg, mgła,
aby zaobserwować, jak zmniejszona prędkość i wydłużona droga hamowania wpływają na ogólny czas podróży i tworzenie się korków.

**AC22**

Użytkownik może wybrać typ warunków pogodowych.
System zmienia parametry ruchu pojazdów zgodnie z wybraną pogodą.
Warunki pogodowe wpływają na prędkość pojazdów oraz drogę hamowania.
System uwzględnia zmniejszoną widoczność podczas mgły.
Użytkownik może obserwować wpływ pogody na czas podróży i poziom korków.

------------------------------------------------------------------------------------------------

**US23**

Jako "użytkownik" chcę wprowadzić do ruchu pojazdy specjalny typ pojazdów takich jak karetki i wozy strażackie, 
aby zweryfikować, czy algorytmy zachowań innych uczestników ruchu poprawnie reagują na konieczność ustąpienia pierwszeństwa.

**AC23**

Użytkownik może dodać pojazdy uprzywilejowane do symulacji.
Pojazdy uprzywilejowane mogą ignorować wybrane zasady ruchu (np. przejazd na czerwonym świetle).
Inne pojazdy ustępują pierwszeństwa pojazdom uprzywilejowanym.
System symuluje użycie sygnałów świetlnych i dźwiękowych.
Użytkownik może analizować wpływ pojazdów uprzywilejowanych na płynność ruchu.

------------------------------------------------------------------------------------------------

**US24**

Jako "użytkownik" chcę zdefiniować przejścia dla pieszych, aby zobaczyć wzajemną interakcje ruchu ludzi oraz pojazdów w celu znalezienia optymalnej konfiguracji.

**AC24**

Użytkownik może dodawać przejścia dla pieszych na wybranych odcinkach drogi.
Użytkownik może określić, czy przejście posiada sygnalizację świetlną.
Piesi korzystają z przejść podczas symulacji.
Pojazdy zatrzymują się przed przejściem zgodnie z obowiązującymi zasadami ruchu.
System umożliwia analizę wpływu przejść dla pieszych na płynność ruchu i bezpieczeństwo.

