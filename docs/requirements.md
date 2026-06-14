**US1** 

Jako użytkownik chcę stworzyć odcinek drogi przez dodanie nowych węzłów lub połączenie ich z istniejącymi, aby budować sieć drogową z zachowaniem ciągłości zasad ruchu.

**AC1**

* Użytkownik może stworzyć odcinek między dwoma nowymi węzłami lub kliknąć istniejący węzeł, aby dołączyć do niego nową drogę.
* Połączenie nowego odcinka jako kontynuacji drogi automatycznie przenosi (dziedziczy) reguły ruchu z elementu poprzedzającego (np. domyślną prędkość, kierunkowość pasów).
* System poprawnie aktualizuje strukturę grafu, łącząc węzły tak, aby pojazdy mogły płynnie przejechać z jednego elementu na drugi.
* System waliduje poprawność położenia (np. zapobiega nakładaniu się dróg na siebie w niedozwolony sposób).

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US2** 

Jako użytkownik chcę utworzyć własny element drogowy z grupy połączonych węzłów, aby móc łatwo powtarzać i wstawiać złożone układy dróg.

**AC2**

* Użytkownik może zaznaczyć zestaw węzłów i połączeń, a następnie zapisać go w pamięci aplikacji jako własny szablon (np. rondo, specyficzne skrzyżowanie).
* Zapisany element posiada zdefiniowane zewnętrzne węzły (punkty wlotowe i wylotowe), które umożliwiają wpinanie go w istniejącą siatkę dróg.
* Element pojawia się w menu wyboru jako gotowy komponent do wielokrotnego użycia na mapie.
* Wstawienie elementu z menu na mapę wiernie kopiuje całą jego wewnętrzną strukturę węzłów oraz przypisane do nich reguły ruchu.

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US3** 

Jako użytkownik chcę dodać przejście dla pieszych na odcinku drogi, aby umożliwić pieszym przekraczanie jezdni.

**AC3**

* Użytkownik może wskazać miejsce na istniejącym odcinku drogi, aby umieścić na nim przejście dla pieszych.
* Dodanie przejścia tworzy w strukturze grafu dedykowany węzeł przecięcia dla ruchu kołowego i pieszego.
* Pojazdy zbliżające się do tego węzła sprawdzają obecność pieszych i automatycznie ustępują im pierwszeństwa (zatrzymują się przed węzłem).

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US4** 

Jako użytkownik chcę wstawić przejazd pod mostem z określoną wysokością, aby wprowadzić ograniczenia gabarytowe dla poruszających się pojazdów.

**AC4**

* Użytkownik może wskazać odcinek drogi i zdefiniować na nim parametr maksymalnej wysokości przejazdu pod mostem (np. w metrach).
* Odcinek drogi pod mostem otrzymuje regułę ograniczającą ruch dla pojazdów przekraczających tę wysokość.
* Algorytm automatycznego wyznaczania trasy unika tego odcinka, jeśli gabaryty pojazdu (np. ciężarówki) są większe niż dopuszczalna wysokość.

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US5** 

Jako użytkownik chcę dodać przejazd kolejowy, aby umożliwić bezpieczne przecinanie się tras kolejowych i drogowych.

**AC5**

* Użytkownik może umieścić przejazd kolejowy w miejscu przecięcia torów z odcinkiem drogi.
* System tworzy w tym miejscu specjalny węzeł kolizyjny, który automatycznie nadaje bezwzględne pierwszeństwo pojazdom szynowym.
* Gdy pociąg zbliża się do węzła, ruch drogowy na połączonych pasach zostaje zablokowany, zmuszając samochody do zatrzymania się.
* Po opuszczeniu węzła przez pociąg, blokada zostaje automatycznie zdjęta i ruch kołowy zostaje wznowiony.

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US6** 

Jako użytkownik chcę dodać regułę ruchu do odcinka drogi lub węzła, aby kontrolować zachowanie pojazdów na poziomie logicznym.

**AC6**

* Użytkownik może wybrać konkretne połączenie (pas) lub węzeł i przypisać mu regułę (np. ograniczenie prędkości, zakaz wjazdu, nakaz jazdy prosto).
* Przypisana reguła zmienia właściwości logiczne elementu w grafie bez generowania obiektów wizualnych na mapie.
* Algorytmy pojazdów natychmiast odczytują nową regułę i dostosowują do niej swoje zachowanie (np. zwalniają lub zmieniają trasę).

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US7** 

Jako użytkownik chcę dodać znak drogowy do odcinka drogi, aby wizualnie oznaczyć i automatycznie wymusić powiązaną z nim regułę.

**AC7**

* Użytkownik może wybrać znak drogowy i umieścić go w konkretnym miejscu na odcinku drogi.
* Postawienie znaku automatycznie aktywuje przypisaną do niego regułę na danym połączeniu między węzłami.
* Wpływ znaku (reguła) zaczyna obowiązywać pojazdy automatycznie i natychmiast od punktu, w którym fizycznie się on rozpoczyna (od miejsca jego postawienia).
* Znak wyświetla się poprawnie jako element graficzny na mapie.

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US8** 

Jako użytkownik chcę utworzyć nowy znak drogowy w bazie danych, aby móc rozszerzyć bibliotekę dostępnych znaków w aplikacji.

**AC8**

* Użytkownik może zdefiniować wygląd graficzny nowego znaku (np. wgrać ikonę lub wybrać szablon).
* Użytkownik może przypisać do nowego znaku logiczną regułę ruchu (lub zestaw reguł), którą ten znak ma reprezentować.
* Po zapisaniu, nowy znak pojawia się w menu wyboru i jest gotowy do umieszczenia na makiecie drogi.

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US9** 

Jako użytkownik chcę kontrolować sygnalizację świetlną na skrzyżowaniach (węzłach), aby móc zarządzać cyklami ruchu i przepustowością.

**AC9**

* Użytkownik może przypisać sygnalizację świetlną do wybranego węzła, który łączy wiele odcinków dróg.
* Użytkownik może zdefiniować fazy świateł (zielone, żółte, czerwone) oraz czas ich trwania dla poszczególnych kierunków (wlotów do węzła).
* Pojazdy docierające do węzła odczytują aktualny stan sygnalizacji dla swojego pasa i zatrzymują się na czerwonym świetle lub płynnie przejeżdżają na zielonym.

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US10** 

Jako użytkownik chcę stworzyć nowy pojazd, aby zdefiniować jego parametry i typ w bazie danych symulacji.

**AC10**

* Użytkownik może określić typ pojazdu (np. samochód, ciężarówka, tramwaj, rower).
* Użytkownik może zdefiniować parametry fizyczne pojazdu, takie jak maksymalna prędkość, przyspieszenie oraz gabaryty (długość, szerokość i wysokość).
* Nowo stworzony pojazd pojawia się na liście gotowych agentów do umieszczenia w symulacji.
* Użytkownik może także wczytać własny plik modelu pojazdu służący do jego reprezentacji, w przypadku jeśli tego nie zrobi zostanie mu przydzielony domyślny wygląd.

**US11** 

Jako użytkownik chcę stworzyć nową trasę z sekwencji połączonych węzłów, aby zdefiniować ścieżkę, po której mogą poruszać się pojazdy.

**AC11**

* Użytkownik może wyznaczyć trasę, wskazując kolejno połączone ze sobą węzły lub przystanki.
* System waliduje ciągłość i kierunkowość połączeń, uniemożliwiając stworzenie nieprzejezdnej trasy (np. jazdy pod prąd).
* Nowo utworzona trasa zostaje zapisana w systemie i jest gotowa do przypisania pojazdom.

[Makieta](Makiety/MakietaAI_Tworzenie_trasy.png)

**US12** 

Jako użytkownik chcę dodać przystanki oraz trasy komunikacji publicznej, aby zasymulować regularny ruch autobusów lub tramwajów.

**AC12**

* Użytkownik może wskazać miejsce na odcinku drogi (lub torowiska), aby utworzyć tam przystanek.
* Tworzenie trasy komunikacji publicznej pozwala na połączenie sekwencji węzłów oraz wskazanie, na których przystankach pojazd ma się zatrzymywać.
* Pojazdy przypisane do komunikacji publicznej zatrzymują się na przystankach na określony czas (np. czas wymiany pasażerów), po czym wznawiają jazdę.
  
[Makieta](Makiety/MakietaAI_Tworzenie_lini_komunikacyjnej.png)

**US13**

Jako użytkownik chcę stworzyć przystanek i przypisać go do wielu linii komunikacji publicznej, aby odzwierciedlić realne współdzielenie infrastruktury.

**AC13**

* Użytkownik może umieścić element „przystanek” w wybranym miejscu na odcinku drogi lub węźle.
* Podczas tworzenia linii komunikacji publicznej (na bazie istniejącej trasy) użytkownik wskazuje, na których przystankach pojazdy mają się zatrzymywać i zdefiniować czasy przyjazdu.
* Ten sam przystanek może być współdzielony i obsługiwany przez wiele różnych linii komunikacji publicznej.
* Pojazdy linii publicznej zatrzymują się na przystankach, a system generuje opóźnienia (np. wynikające z ruchu drogowego lub oczekiwania na zwolnienie współdzielonego przystanku przez inny pojazd).

[Makieta](Makiety/MakietaAI_Tworzenie_lini_komunikacyjnej.png)

**US14**

Jako użytkownik chcę dodać element blokady drogi, aby tymczasowo wyłączyć wybrany odcinek lub węzeł z ruchu.

**AC14**

* Użytkownik może umieścić element blokady (np. remont, wypadek) na konkretnym pasie ruchu (połączeniu między węzłami) lub na całym węźle.
* Dodanie blokady zmienia status logiczny elementu grafu na „nieprzejezdny”.
* Pojazdy generowane w symulacji dynamicznie reagują na blokadę – jeśli to możliwe, zmieniają trasę, aby ją ominąć, a jeśli nie mają alternatywy, zatrzymują się przed zablokowanym obszarem.
* Blokada jest wyświetlana na mapie w czytelny sposób za pomocą dedykowanej grafiki.

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png)

**US15**

Jako użytkownik chcę wyznaczyć obszar ze specjalnymi warunkami środowiskowymi (np. lód, zalanie drogi), aby dynamicznie wpływać na zachowanie różnych typów pojazdów, parametry fizyczne tras oraz wywoływać zdarzenia awaryjne.

**AC15**

* Użytkownik może zaznaczyć fragment sieci dróg i nałożyć na niego stan środowiskowy: **„Lód”** lub **„Zalanie”** (z określeniem poziomu wody).
* Stan **„Lód”** automatycznie zmniejsza przyczepność nawierzchni, co wydłuża drogę hamowania pojazdów i wymusza wolniejszą, bezpieczniejszą jazdę.
* Stan **„Zalanie”** wprowadza progi tolerancji w zależności od typu i gabarytów pojazdu:
* Pojazdy mogą podjąć próbę przejazdu, ale ich prędkość spada.
* Wyznaczony obszar jest wyróżniony na mapie odpowiednią nakładką graficzną (np. błękitną dla lodu, jasnoniebieską dla zalania).

**US16** 

Jako użytkownik chcę zmieniać globalną pogodę, aby wpłynąć na fizykę jazdy, widoczność i zachowanie pojazdów w całej symulacji.

**AC16**

* Użytkownik może wybrać stan pogody: **Słonecznie**, **Deszcz**, **Śnieg** lub **Mgła** (co zmienia też warstwę wizualną).
* Deszcz / Śnieg:** Zmniejszają przyczepność nawierzchni – pojazdy wydłużają drogę hamowania i zwiększają bezpieczny odstęp.
* Mgła:** Ogranicza widoczność – pojazdy wolniej wykrywają przeszkody i automatycznie redukują prędkość maksymalną.
* Trudne warunki generują losowe opóźnienia, wpływając m.in. na punktualność autobusów.
* Warunki lokalne mają wyższy priorytet i nadpisują pogodę globalną w danym miejscu.

**US17** 

Jako użytkownik chcę konfigurować intensywność ruchu dla różnych przedziałów czasowych bezpośrednio z poziomu węzła, aby zasymulować zmienne w czasie obciążenie sieci przez pojazdy i pieszych.

**AC17**

* Kliknięcie na węzeł otwiera dedykowane menu kontekstowe dla tego konkretnego punktu.
* W menu kontekstowym użytkownik może zdefiniować listę różnych przedziałów czasowych (np. od 15:30 do 16:09 ).
* Dla każdego zdefiniowanego przedziału czasowego użytkownik może za pomocą suwaków lub pól numerycznych określić osobną intensywność pojawiania się np. pojazdów lub pieszych rozpoczynających ruch z tego węzła.
* W trakcie trwania symulacji system automatycznie śledzi upływający czas i w momencie przekroczenia granicy przedziału dynamicznie zmienia tempo automatycznego generowania obiektów z danego węzła.
* Harmonogram intensywności w menu kontekstowym można modyfikować także w czasie rzeczywistym podczas działającej symulacji, co natychmiast wpływa na bieżący strumień ruchu.

[Makieta](Makiety/MakietaAI_Tworzenie_odcinków_drogi.png) Obrazek 10

**US18**

Jako użytkownik chcę, aby system automatycznie i dynamicznie wyznaczał optymalne trasy dla wszystkich typów uczestników ruchu (pojazdów, pieszych, rowerów, tramwajów), wykorzystując algorytmy wyszukiwania ścieżek.

**AC18**

* System automatycznie kalkuluje trasę od punktu początkowego (Źródła) do docelowego (Ujścia) przy użyciu algorytmu grafowego.
* Rozróżnienie sieci poruszania się: Algorytm ściśle respektuje infrastrukturę dedykowaną dla danej klasy agenta.
* Dynamiczne przeliczanie tras: Agenci reagują na bieżące zmiany na mapie. Jeśli na ich trasie pojawi się nagła blokada lub strefa niedostępna z powodu zalania, pojazdy w najbliższym węźle automatycznie przeliczają alternatywną ścieżkę.
* Wagi odcinków: Koszt przejścia danego odcinka drogi w algorytmie nie wynika tylko z jego fizycznej długości, ale uwzględnia również:
    * Aktualne ograniczenia prędkości,
    * Obecność sygnalizacji świetlnej,
    * Narastające natężenie ruchu.
 
**US19**

Jako użytkownik chcę widzieć zagęszczenie ruchu w postaci kolorowego gradientu, aby szybko i intuicyjnie zlokalizować korki na mapie.

**AC19**

* System nakłada na drogi dynamiczną warstwę wizualną w postaci płynnego gradientu kolorów (od zielonego, przez żółty, aż do intensywnej czerwieni).
* Kolor odcinka zmienia się automatycznie w czasie rzeczywistym na podstawie bieżącej płynności i liczby stojących pojazdów.
* Czysty zielony oznacza całkowity brak zatorów, a ciemnoczerwony – pełny paraliż drogi (korek).
* Widok gradientu natężenia ruchu można w każdej chwili włączyć lub wyłączyć jednym kliknięciem w interfejsie.

**US20** 

Jako użytkownik chcę kontrolować stan oraz prędkość działania całej symulacji, aby móc swobodnie uruchamiać, zatrzymywać i przyspieszać ruch na mapie.

**AC20**

* Interfejs zawiera główny panel kontrolny z przyciskami: **Start/Odtwarzaj**, **Pauza** oraz **Reset**.
* Przycisk **Pauza** natychmiast zamraża ruch wszystkich pojazdów, pieszych, sygnalizacji oraz licznik czasu, zachowując pełną interaktywność UI (możliwość klikania w węzły).
* Użytkownik może płynnie zmieniać **prędkość symulacji** za pomocą suwaka lub poprzez wpisanie wartości w pole po kliknieciu na mnożnik, co przyspiesza fizykę ruchu i logikę agentów.
* Opcja **Reset** natychmiast usuwa z mapy wszystkie dynamicznie wygenerowane obiekty i przywraca zegar symulacji do startowej wartości.
* Na ekranie głównym wyświetlany jest aktualny, ciągły czas trwania symulacji.
* Użytkownik ma możliwość wpisania czasu startowego symulacji gdy jest ona zatrzymana.

**US21** 

Jako użytkownik chcę zapisać zaznaczony schemat infrastruktury, aby móc wielokrotnie wykorzystywać ten sam układ sieci do różnych scenariuszy ruchu.

**AC21**

* Opcja **„Zapisz schemat”** eksportuje do pliku wyłącznie statyczną strukturę mapy: siatkę dróg, węzły, znaki, reguły oraz cykle sygnalizacji świetlnej.
* Plik **nie zawiera** informacji o aktualnie poruszających się pojazdach, pieszych ani stanie licznika symulacji.
* Dane są zapisywane w lekkim, ustrukturyzowanym formacie (np. JSON).
* Użytkownik może wybrać folder docelowy oraz nadać plikowi własną nazwę poprzez standardowe okno systemowe.


**US21** 

Jako użytkownik chcę zaznaczyć ramką określone elementy infrastruktury, aby zapisać je jako schemat (blueprint) do późniejszego skopiowania lub eksportu.

**AC21**

* Użytkownik może aktywować narzędzie selekcji (np. przeciągając prostokątną ramkę) i wybrać fragment infrastruktury (węzły, odcinki, znaki, sygnalizację).
* System podświetla wybrane elementy i pozwala zapisać ten konkretny fragment jako osobny plik schematu (np. "Rondo_turbinowe.json").
* Zapisywane są wyłącznie statyczne elementy i ich wzajemna logika, dynamiczne pojazdy wewnątrz ramki są ignorowane.
* Zapisany w ten sposób schemat trafia na listę podręcznych szablonów użytkownika, gotowych do ponownego "wklejenia" w dowolnym miejscu na makiecie.

**US22** 

Jako użytkownik chcę wybrać zapisany schemat (blueprint) i go wstawić, aby szybko replikować złożone układy skrzyżowań i dróg.

**AC22**

* Użytkownik może wybrać zapisany wcześniej schemat z listy podręcznej lub wczytać go z pliku JSON.
* Po wyborze schematu, pod kursorem myszy pojawia się półprzezroczysty podgląd wklejanej infrastruktury.
* Użytkownik może obracać podgląd schematu i sostosować jego pozycję przed jego ostatecznym umieszczeniem na mapie.
* Kliknięcie przycisku potwierdzenia lub klawisza "enter" myszy potwierdza, automatycznie łącząc drogi ze schematu z istniejącą już siecią, jeśli ich punkty stykowe się pokrywają.
* Wklejona infrastruktura zachowuje całą swoją oryginalną konfigurację (przypisane znaki, reguły pierwszeństwa oraz cykle sygnalizacji świetlnej).

**US23** 

Jako użytkownik chcę zapisać pełny stan symulacji do pliku, aby móc później wznowić pracę dokładnie w tym samym momencie, z zachowaniem wszystkich poruszających się pojazdów.

**AC23**

* Opcja **Zapisz** eksportuje do pliku (JSON lub dedykowany format) kompletny stan całej makiety.
* Zapis obejmuje:
  * Całą infrastrukturę drogową, znaki i reguły.
  * Aktualną pozycję, prędkość, przypisaną trasę i typ każdego aktywnego pojazdu, pieszego czy pociągu na mapie.
  * Bieżący czas symulacji, stan sygnalizacji świetlnej oraz aktywne blokady.
  * Ustawienia pogody: lokalne i globalne
* Użytkownik zapisuje plik poprzez standardowe okno systemowe, wybierając dowolną nazwę i lokalizację na dysku.

**US24**

Jako użytkownik chcę wczytać pełny stan symulacji z pliku, aby wznowić zapisaną wcześniej sesję wraz ze wszystkimi poruszającymi się obiektami.

**AC24**

* Użytkownik wybiera plik zapisu z poziomu okna systemowego.
* Wczytanie pliku całkowicie zastępuje bieżący stan makiety, odtwarzając pełną infrastrukturę oraz dokładne pozycje, prędkości i trasy wszystkich pojazdów, pieszych i pociągów.
* System przywraca dokładny czas zegara symulacji oraz aktualne fazy sygnalizacji świetlnej z momentu zapisu.
* Po pomyślnym wczytaniu symulacja domyślnie uruchamia się w trybie **Pauzy**, pozwalając użytkownikowi na rozejrzenie się po mapie przed wznowieniem ruchu.
