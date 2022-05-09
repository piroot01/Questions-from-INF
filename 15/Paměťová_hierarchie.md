## 15. Paměťová hierarchie

- trvalé či dočasné uložení dat v binární podobě

### 1. Druhy pamětí

- **dělení podle typu úložního média**
	- *polovodičové*: většina dnešních pamětí, tvořené tranzistory, aktivní, SSD, FLASH
	- *plotnové*: HDD
	- *laserové*: CD, DVD
	- *analogové*: vinyl, děrové pásky
- **volatilní**: po přerušení elektrického proudu data na uložišti zmizí
	- RAM: random acces memory, krátkodobé uložení dat, vysokorychlostní sběrnice s CPU
	- SRAM: vyrovnávací paměť, statická
	- DRAM: dynamická RAM, používá se jako vysokorychlostní dočasné uložiště
- **nevolatilní**: nezávislé na napájení, trvalé, HDD
	- ROM, PROM - programovatelná, EPROM - mazatelná UV, EEPROM - elektrickým nábojem mazatelná
	- FLASH: libovolný přístup, rozdělena na bloky
- **vnitřní paměť**: RAM či ROM, pro komponenty počítače, nikoliv pro uživatele, BIOS
- **vnější paměť**: pro uložení dat, nabízejí velkou kapacitu
- **virtuální paměť**: třeba SWAP, jedná se o typ vnitřní paměti, ale nachází se na uložištích vnější paměti
- **chráněná paměť**: paměť přidělená pouze jednomu procesu, zvyšuje spolehlivost a bezpečnost
- **operační paměť**: paměť, kterou využívá typycky CPU, normy DDR

### 2. Metody správy

- **monolitická paměť**: FAP (fyzicky adresovaný prostor) je dělen na dva bloky (rutiny jádra, kernel memory a druhý app memory), statická alokace paměti, aplikaci je přidělen celý blok na určitou periodu, dnes se už nevyužívá
- **statické bloky paměti**: aplikační blok je dělen na subbloky, ty se dají alokovat zvlášť, nutnost chránit přidělené bloky, aby nedošlo k overflow, jeden proces si může zabrat více bloků
- **dynamické bloky paměti**: velikost bloků, které jsou alokovány, se mění - dynamická alokace paměti, sklon k fragmentaci - jeden proces vyžaduje souvislý blok, který prostě neni, s tím souvisí endianita
- **trimming**: proces, při kterém se mažou označené bloky, jde o to, že zápis na volné sektory SSD je rychlejší, než přepisování, takže nová data se ukládají na nové sektory, a při TRIMu se mažou obsazené sektory, dochází tedy k rovnoměrnému opotřebení paměti, na to je SSD citlivé, kolik read-write cyklů je schopna vykonat

### 3. Využití

- operační paměť CPU
	- paměť určená jako sada instrukcí
	- cache, vysokorychlostní paměť, dočasné odkladiště CPU
		- L1, L2, L3  dělení podle rychlosti, vyšší číslo nižší rychlost rw, ale vyšší kapacita
- NAS uložiště, serverová multiclusterová pole
- cloudová uložiště
- personální uložiště

### 4. Hardwarová realizace

- **SSD**
	- realizace pomocí NAND hradel
	- skládá se z jednotlivých FLAH bloků a lepší obsahují DRAM pro rychlý přístup k datům
	- využití stackování tranzistorů, aby byla živostnost paměti prodloužena
	- vyšší cena než HDD
	- mechanicky odolnější než HDD
	- menší spotřeba než HDD
	- rychlé v read-write
	- kratší životnost
	- znatelně nižší kapacita
- **HDD**
	- skládají se z diskové hlavy (slouží ke čtení z ploten), plotny (2.5 a 3.5 palcové, povrch je oxid železitý), ROM (firmware disku), řadič (přenos dat na plotny)
	- data se ukládají v následující posloupnosti: *sektor* (část jedné stopy, značky začátku a konce, 512 bitů) $\rightarrow$ *stopa* (oblast pro konkrétní uložení dat) $\rightarrow$ $\rightarrow$ *cylindr* (sada několika stop), *cluster* (obsahuje n sektorů)
