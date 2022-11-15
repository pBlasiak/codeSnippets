Code snippets for LaTeX and Bash
========================================


Bash
------------

- [Usuniecie wszystkich linii w pliku zawierajacych znaki "step"](#usuniecie-wszystkich-linii-w-pliku-zawierajacych-znaki-step)

- [Usuniecie wyrazu "Wyraz" z pliku](#usuniecie-wyrazu-wyraz-z-pliku)

- [Usunięcie N-tej linii w pliku](#usuniecie-n-tej-linii-w-pliku)

- [Grepowanie następnego wyrazu po "RASModel"](#grepowanie-nastepnego-wyrazu-po-rasmodel)

- [Grepowanie następnego wyrazu po zadanym i zakończenie grepowania
](#grepowanie-nastepnego-wyrazu-po-zadanym-i-zakonczenie-grepowania)

- [Grepowanie ostatniej linii zawierającej "Wyraz"](#grepowanie-ostatniej-linii-zawierajacej-wyraz)

- [Grepowanie liczb wliczając zapis naukowy](#grepowanie-liczb-wliczajac-zapis-naukowy)

- [Grepowanie linii w pliku zawierających "Wyraz"](#grepowanie-linii-w-pliku-zawierajacych-wyraz)

- [Wyświetlenie N-tej kolumny pliku](#wyswietlenie-n-tej-kolumny-pliku)

- [Wyświetlenie kolumn o stałej szerokości w terminalu](#wyswietlenie-kolumn-o-stalej-szerokosci-w-terminalu)

- [Wyświetlenie ostatniej linii w pliku](#wyswietlenie-ostatniej-linii-w-pliku)

- [Zmiana części nazwy pliku rekursywnie w podfolderach](#zmiana-czesci-nazwy-pliku-rekursywnie-w-podfolderach)



## Usuniecie wszystkich linii w pliku zawierajacych znaki "step" 

	sed -i '/step/d' nazwaPliku

## Usuniecie wyrazu "Wyraz" z pliku

	sed -i 's/Wyraz//' plik

## Usunięcie N-tej linii w pliku

	sed 'Nd' plik
	sed '1d;3d;4d' plik

## Grepowanie następnego wyrazu po "RASModel"

	grep -Po '(?<=RASModel\s)\w+' plik

## Grepowanie następnego wyrazu po zadanym i zakończenie grepowania

	grep -A 1 -m 1 Wyraz plik

## Grepowanie ostatniej linii zawierajacej "Wyraz"

	grep "Wyraz" plik | tail -1 

## Grepowanie liczb wliczając zapis naukowy

	grep -Eo '[-+]?[0-9]*\.?[0-9]+([eE][-+]?[0-9]+)?.' plik

## Grepowanie linii w pliku zawierających "Wyraz"

	grep -i "Wyraz" plik

## Wyświetlenie N-tej kolumny pliku

	awk '{ print $2 }' plik

## Wyświetlenie kolumn o stałej szerokości w terminalu

	printf '\t%-15s %-15s %-15s %-15s %-15s %-15s %-15s %-15s\n' $CD $turbMod "mesh =" $mesh "y+ =" $yPlus "dp =" $dp

## Wyświetlenie ostatniej linii w pliku

	tail -1 plik

## Zmiana części nazwy pliku rekursywnie w podfolderach

	find /the/path -depth -name "*.abc" -exec sh -c 'mv "$1" "${1%.abc}.edefg"' _ {} \;
