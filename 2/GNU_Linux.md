## 2. GNU/Linux

### 1. Vznik

- GNU:
	- 1985, GNU manifest
	- Richard Stallman
	- rekurzivní struktura
	- MIT, laboratoř AI
	- userspace pro Linuxí kernel
- Linux:
	- napsán jako svobodná alternativa k UNIX kernelu
	- 1991
	- inspirace MINIXEM (nejpoužívanější OS)
	- nedokonalé Linusovo jádro se vyvíjelo za pomocí tisíce programátorů z celého světa
	- kernel.org
	- licence GPLv2
	
### 2. Souborová struktura
	
- jedním ze základních stavebních kamenů je, že vše je soubor
- / začíná stromový adresář, poté jsou další součásti Linuxu děleny do podružných souborů
	- /proc - system info, kernel files
	- /dev - zařízení, disky, komunikace - UART, serial
	- /bin - spustitelné binárky
	- /boot - kernel, iniciální obraz systému, GRUB
	- /etc - konfigurace systému
	- /home - uživatelský adresář
	- /lib - knihovny
	- /mnt - mount media
	- /run - dočasný file systém
	- /srv - service data
	- /sbin - systémové binárky
	- /tmp - dočasné soubory, po resetu nejsou
	- /usr - uživatelské binárky
	- /var - konstantně se měnící obsah, logy

### 3. Práce s shellem

### 4. Principy

0. Každý program by měl dělat jednu věc a pořádně
1. Vše je soubor
2. Jeden výstup programu může být vstup jiného
3. Vše je open-source