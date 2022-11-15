Code snippets for LaTeX and Bash
========================================


Bash
------------

- [Usuniecie wszystkich linii w pliku zawierajacych znaki "step"](#usuniecie-wszystkich-linii-w-pliku-zawierajacych-znaki-step)
- [Grepowanie następnego wyrazu po "RASModel"](#grepowanie-nastepnego-wyrazu-po-rasmodel)


## Usuniecie wszystkich linii w pliku zawierajacych znaki "step"


	sed -i '/step/d' nazwaPliku

## Grepowanie następnego wyrazu po "RASModel"

	grep -Po '(?<=RASModel\s)\w+' path/to/file
