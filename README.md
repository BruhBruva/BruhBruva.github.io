W folderze "próba" znajduje się kod, plik GeoJSON jak i plik HTML.
Ta strona nie jest ukończona gdyż z niewiadomej mi przyczyny, po wielu dniach/godzinach prób nie mogłem się uporać z błędem, który uniemożliwiał wyświetlanie obiektów z pliku GeoJSON.
Kod i pliki zostawiam do wglądu aby ocenić z czym sobie poradziłem, a z czym niekoniecznie.

Dane do próby:
  - Rozmieszczenie rezerwatów pozyskałem z serwisu OpenForestData - https://gis.openforestdata.pl/layers/geonode_data:geonode:Rezerwaty_wgs84

  - Natomiast dane na temat rezerwatów pozyskałem z Centralnego Rejestru Form Ochrony Przyrody (CRFOP) - https://crfop.gdos.gov.pl/CRFOP/

  - Podkład z OSM

  - Podkład z ukształtowaniem powierzchni

Poniżej znajduje się link do mapy interaktywnej, którą wykonałem na stronie "MapHub" - (https://maphub.net)
https://maphub.net/Maciej_Wisniewski/mapa-rezerwatow-przyrody-w-polsce

Tworząc "próbę" jak i wyżej wymienioną mapę zamysł był ten sam, czyli zaprezentować mapę rezerwatów przyrody w Polsce z podziałem na ich rodzaje.
Każdy rodzaj ma mieć możliwość odznaczania i zaznaczania do wyświetlania (po części ze względu na to, że część rezerwatów znajduje się na bardzo zbliżonych terenach co inne).
Do wyboru mają być różne rodzaje podkładów, by użytkownik wybrał dogodny dla siebie (zawarta miała być również opcja braku podkładu by można było się skupić wyłącznie na rezerwatach).
W planach było stworzenie bardziej zaawansowanego paska bocznego dzięki, któremu mógłbym zawrzeć tam informacje na temat rezerwatów przyrody i informacji dla każego rodzaju z osobna.
Obiekty na mapie (rezerwaty) po kliknięciu na nie mają wyświetlać najbardziej podstawowe informacje na ich temat.

(lokalizacja rezerwatów jak i dane na ich temat pochodziły z tych samych źródeł co w "próbie")

mapshaper.org okazał się być pomocny w obejrzeniu mapy w wersji poglądowej

Zrzuty ekranu z obu "wersji" projektu zawarte są w folderze głównym (screenshot).

PRÓBA - objaśnienie działań

Kod wykonałem w Notepad++ korzystając z HTML przy użyciu bibliotek JS/Leaflet.

- utworzenie i przystosowanie paska bocznego
- dodanie podkładów i możliwości przełączania między nimi
- dodanie pliku GeoJSON
- przydzielenie różnych kolorów dla różnych rodzajów rezerwatów
- ograniczenie zasięgu mapy do Polski (działa to połowicznie ze względu na to, że po przybliżeniu do Polski nie można się przesuwać poza jej granice, ale podczas oddalania obrazu już można zobaczyć resztę)
- dodanie braku podkładu jako domyślną "pozycję startową"



WERSJA Z MAP HUB - objaśnienie działań
- wstępne podzielenie pliku GeoJSON na osobne rodzaje rezerwatów
- dodanie plików do MapHub
- Ustalenie odpowiedniej kolorystyki rezerwatów
- Ustalenie tytułu i krótkiego opisu

(MapHub pozwala na osadzenie interaktywnej mapy na własnej stronie)

Projekt znajduje się na GitHubie głównie dlatego, że chciałem aby stworzona przeze mnie mapa była ogólnie dostępna za pomocą linku na GitHub Sites.
Dodatkowo dzięki temu można mieć łatwy dostęp/wgląd do plików celem ich sprawdzenia.

Owy projekt w najbliższych miesiącach będzie przeze mnie naprawiany i ulepszany gdyż zamierzam włączyć go w moją pracę inżynierską.
Dlatego w finalnym projekcie mam w planie zawrzeć:
  - dodanie i możliwość wyboru aktywnych pasm (i ich kombinacji) obrazów satelitarnych (Sentinel)
  - przycięcie pasm do obszarów rezerwatów celem analizy róznic pomiędzy rodzajami rezerwatów
  - wyszukiwarka pojedyńczych rezerwatów po np. nazwie
  - dodatkowe informacje na temat każdego rezerwatu (powierzchnia itp.)
  - osobna zakładka z opisem analiz różnic między rezerwatami, bądź umieszczenie tego na własnej stronie do której zostanie włączona mapa
