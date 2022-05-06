## 16. Teorie jazyků a gramatik

### 1. Základní pojmy

- *abecedu* definujeme jako konečnou množinu znaků - značíme $\Sigma$
- jakýkoliv *řetězec* znaků abecedy $\Sigma$ je konečná posloupnost znaků abecedy $\Sigma$
- příkladem abecedy může být $\Sigma = \{0,1\}$, poté řetězce z ní vytvořené jsou například $0010101$ nebo $11010101$ atd.
	- projekt Human Genome Project zkoumající lidský genom bude využívat abecedu $\Sigma = \{A, C, G, T\}$
- pakliže uméstíme tyto řetězce do množiny, budeme jí značit $\Sigma ^+$, poté se hodí zadefinovat $\Sigma^+$ jako množinu neprázdných řetězců, prázdný řetězec budeme označovat $\epsilon$
	- s řetězci potom můžeme provádět různé operace, $x \in \Sigma^+$, potom $x = x\epsilon = \epsilon x$
- definice *formálního jazyka*: opět se jedná o množinu, označíme ji $L$, tato množina bude množinou řetězců nad abecedou $\Sigma$, takže $L \subseteq \Sigma^*$, jinými slovy, formálním jazykem se rozumí soubor všech řetězců, které lze nad danou abecedou vytvořit
	- tato definice nám umožňuje vytvářet formální jazyky, které jsou generované nějakým pravidlem
	- příkad $\Sigma = \{0,1\}$ a $L = \{x \in \Sigma^*; počet 0 a 1 je shodný\}$
- posledním důležitým pojmem jsou 

### 2. Použití
### 3. Klasifikace - Chomského hierarchie
### 4. Výpočetní modely