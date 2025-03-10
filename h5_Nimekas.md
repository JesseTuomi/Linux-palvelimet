# H5 Nimekäs

## a) NIMI
![image](https://github.com/user-attachments/assets/22b73faf-0b79-4c4d-85dd-03f56df3c686)

Päätin käyttää namecheap palvelua, etusivulla ensin etsitään vapaa nimi minkä voi sitten ottaa käyttöön.

![image](https://github.com/user-attachments/assets/88ac0e27-f6f1-44b9-a084-c766e88a92f2)

Sain nimeni läpi ensimmäisellä yrittämällä ja syötin henkilötietoni järjestelmään.

![image](https://github.com/user-attachments/assets/7c863717-cd3a-461b-acd2-0d21d861f150)

menin namecheap sivuilleni painoin manage

![image](https://github.com/user-attachments/assets/0efd867b-090a-46b3-82d4-6e7ff264bd3b)

sitten advanced DNS

![image](https://github.com/user-attachments/assets/b227558c-20e8-4675-8ba3-d3e243fb9167)

Sen jälkeen poistin vakio arvot kentästä ja lisäsin @ osoitteeni ja www nimisivun

## b) Based

Sitten vain tein jessetuomi.me.conf tiedoston ja sille hakemistopolun ja index.html tiedoston, jonka jälkeen sain oman sivuni näkyviin.

![image](https://github.com/user-attachments/assets/f25618c2-2ab8-4f52-9ceb-7a2126c9405b)

## c) Kotisivu

Tein kolme .html tiedostoa visual studio codella ja kopioin ne palvelimelleni /jessetuomi.me kansioon

![image](https://github.com/user-attachments/assets/ced21151-6953-4819-a127-2bb73baf6ba2)
![image](https://github.com/user-attachments/assets/6a74b1d4-559f-4a73-a647-4c7d77cee860)
![image](https://github.com/user-attachments/assets/44d45f7a-c90b-40e1-b362-387262486514)

Lopputulemana tälle sain toimivan kolmen sivun websivuston aikaiseksi.

![image](https://github.com/user-attachments/assets/57dfb64f-0a55-4266-b73a-6c52db5d253b)

## d) Alidomain

Menin jälleen namecheap sivustolla oman domainin advanced DNS sivulle ja tein sinne kaksi subdomainia

![image](https://github.com/user-attachments/assets/8c736cef-9f27-4bdf-b605-faf0d622d658)

Odotin kunnes muutos meni serverille ja sitten kokeilin löytyykö sivua.

![image](https://github.com/user-attachments/assets/de7a46cd-9768-406e-a6f2-280ee577bd8e)
![image](https://github.com/user-attachments/assets/33b0c051-4298-45d9-b759-0a2e27789928)

Kumpikin toimivat niin kuin pitääkin.

## e) DNS-tiedot

host näyttää URL:in ja liikennettä käsittelevän serverin osoitteen

![image](https://github.com/user-attachments/assets/41f591c2-06f6-41b5-9849-321aa2fcb604)

host namecheap.com antaa eri arvot
jesse@debian-s-1vcpu-1gb-fra1-01:~$ host namecheap.com
namecheap.com has address 198.54.117.250
namecheap.com mail is handled by 5 mx1.jellyfish.systems.

youtube.com antaa myös ip6 osoitteen
jesse@debian-s-1vcpu-1gb-fra1-01:~$ host youtube.com
youtube.com has address 142.250.186.142
youtube.com has IPv6 address 2a00:1450:4001:813::200e
youtube.com mail is handled by 0 smtp.google.com.

host jousiammunnanttv.fi antaa
jousiammunnanttv.fi has address 188.117.28.147
jousiammunnanttv.fi mail is handled by 10 mailserver22.nebula.fi.

dig komentoa ei löytynyt, joten etsin mitä tarvitsen sen toimimiseen ja siten asensin dnsutils ohjelmiston
tämän jälkeen kokeilin uudelleen.

dig jessetuomi.me vastasi

; <<>> DiG 9.18.33-1~deb12u2-Debian <<>> jessetuomi.me
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 8827
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;jessetuomi.me.			IN	A

;; ANSWER SECTION:
jessetuomi.me.		1799	IN	A	165.22.93.67

;; Query time: 20 msec
;; SERVER: 67.207.67.2#53(67.207.67.2) (UDP)
;; WHEN: Sat Feb 22 12:47:53 UTC 2025
;; MSG SIZE  rcvd: 58

namecheap antaa eri tiedot, en näe näissä vertailukohtia
dig jousiammunnanttv.fi antaa

; <<>> DiG 9.18.33-1~deb12u2-Debian <<>> jousiammunnanttv.fi
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 16336
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;jousiammunnanttv.fi.		IN	A

;; ANSWER SECTION:
jousiammunnanttv.fi.	3600	IN	A	188.117.28.147

;; Query time: 40 msec
;; SERVER: 67.207.67.2#53(67.207.67.2) (UDP)
;; WHEN: Sat Feb 22 12:50:53 UTC 2025
;; MSG SIZE  rcvd: 64

ja lopuksi youtube.com antaa dig komenolla

; <<>> DiG 9.18.33-1~deb12u2-Debian <<>> youtube.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 54247
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;youtube.com.			IN	A

;; ANSWER SECTION:
youtube.com.		98	IN	A	142.250.186.174

;; Query time: 0 msec
;; SERVER: 67.207.67.2#53(67.207.67.2) (UDP)
;; WHEN: Sat Feb 22 12:53:04 UTC 2025
;; MSG SIZE  rcvd: 56

Tiedoista ANSWER SECTION tulee nimipalvelimelta ja kertoo sivuston www nimen ja missä URL:ssa se on. 
Numero nimen jälkeen kertoo kuinka kauan tieto on voimassa sekuntteina.

# Lähteet

https://terokarvinen.com/linux-palvelimet/
namecheap.com










