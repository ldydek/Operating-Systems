W zadaniach 1-2 proszę skorzystać z obu wariantów implementacji:
- lib - przy użyciu funkcji biblioteki C: fread() i fwrite()
- sys - przy użyciu funkcji systemowych: read() i write()

<h1> Zadanie 1 (25%) </h1>
Napisz program, który kopiuje zawartość jednego pliku do drugiego z usuwaniem pustych linii (zawierających tylko "whitespace characters"). Jeśli argumentów nie podano, wówczas nazwy plików mają być pobrane od użytkownika.

<h1> Zadanie 2 (25%) </h1>
Napisz program, który przyjmuje 2 argumenty wiersza poleceń. Pierwszy z argumentów jest znakiem, drugi nazwą pliku. Program powinien policzyć ile razy występuje podany znak oraz liczbę wierszy pliku wejściowego, które zawierają dany znak. Zakładamy, że każdy wiersz w pliku kończy się znakiem przejścia do nowej linii. Przyjmujemy, że żaden wiersz nie przekracza długości 256 znaków.

<h6> Dla obu wariantów implementacji należy przeprowadzić pomiar czasu wykonywania obu wariantów programów. Wyniki należy przedstawić w formie pliku pomiar_zad_x.txt </h6>

<h1> Zadanie 3 (50%) </h1>
Napisz program, który będzie przeglądał katalog podany jako argument i kolejno wszystkie jego podkatalogi. 
Program ma wypisać na standardowe wyjście następujące informacje o znalezionych plikach:
 ścieżka bezwzględna pliku,
-liczbę dowiązań,
- rodzaj pliku (zwykły plik - file, katalog - dir, urządzenie znakowe - char dev, urządzenie blokowe - block dev, potok nazwany - fifo, link symboliczny - slink, soket - sock),
- rozmiar w bajtach,
- datę ostatniego dostępu,
- datę ostatniej modyfikacji.

Na koniec ma wypisać na standardowe wyjście informacje o liczbach plików poszczególnych rodzajów, zawartych w tym katalogu i wszystkich jego podkatalogach. Powinny zostać zliczone: zwykłe pliki, katalogi, pliki specjalne znakowe, pliki specjalne blokowe, potoki/kolejki FIFO, linki symboliczne i sokety. 

Ścieżka podana jako argument wywołania może być względna lub bezwzględna. Program nie powinien podążać za dowiązaniami symbolicznymi do katalogów.

Program należy zaimplementować w dwóch wariantach:
- korzystając z funkcji opendir(), readdir() oraz funkcji z rodziny stat (25%)
- korzystając z funkcji nftw() (25%)