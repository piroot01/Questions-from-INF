## 19. Počítačové sítě

### 1. Základní prvky sítě

- síťovým zařízením rozumíme jakýkoliv komponent, který je schopný vysílat či přijímat datagramy/pakety
- základní zařízení:
	- *repeater*: zesiluje signál, dosah normy ethernet je 100m
	- *modem*: slouží k modulaci či demodulaci signálu na jiné formy přenosu, GSM, 4G, ...
	- *splitter*: spíše využívaný v DLS (telefonní linky)
	- *hub*: splitter s více porty, niméně se pakety přeposílají neurčeně
	- *switch*: propojuje více segmentů sítě, cílené přepojování, směrové pakety
	- *bridge*: spojuje dvě fyzicky oddělené sítě
	- *gateway*: umožňuje komunikaci dvou odlišných typů sítě
	- *router*: přesměrovává komunikaci na síti
	- *síťová karta*: koncové zařízení na síti, komunikace s počítačem

### 2. Druhy

- **ISO/OSI model**: teoretický model infrastruktury sítě, slouží jako šablona pro ostatní modely TCP/IP
	1. **Fyzická**: navazuje, ukončuje spojení s komunikačním médiem
	2. **Linková**: poskytuje spojení mezi dvěma sousedními systémy
	3. **Síťová**: směřování a adresování paketů, poskytuje spojení systémům, které spolu nesousedí
	4. **Relační**: organizace dialogu mezi spolupracujícími relačními vrstvami obou systémů
	5. **Prezentační**: transformace dat do tvaru, které používají aplikace (šifrování, hashování, komprimace)
	6. **Aplikační**: poskytování aplikacím přístupu ke komunikačnímu systému, protkoly HTTP, FTP, POP3, IMAP, SSH, DHCP, SMTP, ...
- TCP/IP je sada protokolů pro komunikaci v počítačové síti, celosvětová síť internet

### 3. TCP

- transmission control protocol
- obousměrné posílání dat
- garance doručení paketů ve správném pořadí
- umožňuje rozlišovat a rozdělovat data více aplikacím na stejném počítači - web a mail server
- spolehlivé doručení zprávy
- *MTU* je maximální přenosová jednotka, tedy jak májí být jednotlivé segmenty TCP dlouhé
- SSH, WWW, POP3 či IMAP

### 4. UDP

- user datagram protocol
- nedává záruky, proto hovoříme o datagramech
- je oproti TCP rychlejší, jednodušší a je bezstavový
- nezachovává pořadí datagramů
- není tu timeout
- není tu omezení na počet datagramů na síti, o to se stará router, návrh DCCP protokolu
- DNS, LAN, DHCP, RIP

### 5. Principy přenosu

- datagram je základní jednotka, která je přepravovaná v počítačové síti
- paket, to je též základní jednotka, jež se posílá v síti
- rozdíl mezi paketem a datagramem je ten, že u datagramů nás nezajímají záruky doručení, u paketu zajímají, viz dále TCP a UDP protokol
- paket se skládá z metadat a z payloadu (uživatelská data)
- metadata, neboli hlavička paketu, se skládají z IPv4 adresy jak odesilatele, tak příjemce, CRC - checksum, offset fragmentu, TTL - kolik routerů může paket projít, než bude zničen
- *ARP*: protokol slouží k získání linkové adresy síťového rozhranní pomocí IP a MAC adresy, pro IPv4, pro IPv6 je navržen obdobný protokol NDP
- *IPv4*: čtyři osmice bitů
- *IPv6*: osmice po čtyřech hexadecimálních číslech
- *maska*: slouží k směrování, routery, čtyři oktety, někdy IPv4/sum_of_mask_bits