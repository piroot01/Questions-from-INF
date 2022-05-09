## 21. Databáze - deklarativní paradigma

### 1. Dekalarativní paradigma

- základní myšlenka tohoto přístupu je *co se má udělat*, to jak se to provede nás nezajímá
- specifikuje cíl a algoritmizaci ponechává na dané implementaci
- jejich výhoda třeba spočívá v tom, že redukují horizont pro vytvoření potenciálních chyb, nedeklarují se datové typy
- v deklarativních jazycích se využívají už rozhranní, pracujeme s již vytvořenými funkcemi, proměnné se víceméně nepoužívají
- nepoužívají se cykly (for, while), vše je řešeno pomocí rekurze
- jako všechno jde, ale to už není deklarativní paradigma, takže třeba v SQL jdou vytvořit jak proměnné, tak cykly
- high-level programovací jazyk
- nenabývá postranních účinků, což může být problém v objektových či imperativních paradigmatech
	- neboli jedná se o referenčně transparentní paradigma, výraz, který může být nahrazen jeho odpovídající hodnotou nenaruší chod programu
- čistě koresponduje k matematické logice (Boolean logic)
- k deklarativním jazykům mážeme přistupovat dvojím způsobem:
	- funkcionální, logické programovací jazyky, definuje se v nich množina funkčních závislostí nebo pravidel, kód není zpracováván lineárné, kompozice a high-level, Heskell, což je čistý funkcionální jazyk, žádné vedlejší účinky funkce, změny stavu jsou reprezentovány funkcemi, které transformují svůj stav, explicitně definovány objekty v programu
	- hybridní přístup spočívá v tom, že použijeme imperativní jazyk v kombinaci s knihovnami pro deklarativní programování, makefiles, C
	- doménově specifické jazyky jsou takové, které řeší konkrétní problém, typickým příkladem je SQL, manipulace s databázemi


### 2. SQL - příkazy

- SQL = Structured Query Language
- příkazy se dělí na čtyři základní skupiny:
	1. **data definition language**: příkazy pro definici dat
		- *CREATE*, *DROP*, *ALTER* (změna datového typu např. tabulky)
	2. **data manipulation language**: příkazy pro manipulaci s daty
		- *SELECT*, *INSERT*, *UPDATE*, *DELETE*
	3. **data control language**: příkazy pro řízení transakcí
		- *COMMIT*, *GRANT*, *ROLLBACK*