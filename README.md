# Metody
Všechny popsané metody jsou nedestruktivní

## Determinant
Na vstupu přečte matici a vrátí None, pokud není čtvercová. Pokud je čtvercová, vrátí její determinant. Metoda matici převede do odstupňovaného tvaru a následně mezi sebou vynásobí všechny prvky na hlavní diagonále. Nakonec výsledek vynásobí -1, pokud byl během odstupňování proveden lichý počet prohození řádků.

## LURozklad
Na vstupu přečte matici a vrátí seznam, kde na nultém indexu je požadovaná dolní trojůhelníková matice, na prvním indexu požadovaná horní trojúhelníková matice a pokud je to nutné, je na druhém indexu permutační matice. Metoda odstupňovává původní matici do horní trojůhelníkové a během toho staví dolní trojůhelníkovou, s tím že pokud je nutné prohodit řádky, upraví příslušným způsobem i permutační matici. Pro zvýšení přesnosti převede na začátku metoda prvky matice na objekty třídy Fraction

## QRRozklad
Na vstupu přečte matici a vrátí seznam, kde na nultém indexu je požadovaná ortogonální matice a na prvním indexu požadovaná horní trojúhelníková matice. Metoda prochází sloupci dané matice a provádí nad nimi Gramovu-Schmidtovu ortogonalizaci, zatímco staví příslušnou horní trojúhelníkovou matici. Pokud jsou sloupce zadané matice lineárně závislé, je příslušný sloupec a řádek ve výsledných maticích vynechán a je upraven iterační seznam, aby nedošlo k přeskočení sloupce.

## Cramer
Na vstupu přečte matici soustavy rovnic a vrátí řešení této soustavy jako seznam hodnot. Metoda využívá Cramerovo pravdidlo a výše zmíněnou metodu Determinant. Pokud není zadaná matice regulární, metoda vrátí None.

## GaussJorEliminace
Na vstupu přečte matici soustavy rovnic a vrátí řešení této soustavy jako seznam hodnot. Metoda využívá Gaussovu-Jordanovu eliminaci. Pokud je matice singulární a nemá řešení, vrátí metoda None. Pokud je matice singulární a má řešení, metoda vrátí to, kde jsou za všechny volné proměnné zvoleny 0.

## LinearniRegrese
Na vstupu přečte seznam dvojic, chápaných jako body a vrátí seznam na jehož nultém indexu je směrnice výsledné přímky a na prvním indexu hodnota, určující posunutí přímky nad, nebo pod počátek souřadnic. Metoda pomocí poznatků z lineární algebry převede seznam bodů na soustavu dvou rovnic, kterou následně vyřeší pomocí výše zmíněné metody Cramer.

# Instalace
Je potřeba mít nainstalovaný správce balíčků pip a do příkazové řádky napsat následující příkaz:

    pip install matoperace
K použití pak stačí v programu použít:

    from matoperace import matfunkce
