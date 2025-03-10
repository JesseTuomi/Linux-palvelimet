# h1 Oma Linux

## Raportin kirjoittaminen
- Kerro täsmällisesti mitä teit ja mitä sitten tapahtui
- Raportin tulee olla toistettava samassa ympäristössä jonkun muun toimesta
- Kirjoita raporttiin myös laitteisto ja softa jolla harjoitus on tehty
- Ole täsmällinen ja käytä kelloaikoja eri työvaiheiden seurantaa varten
- Tee raportista helppolukuinen ja tarkista kieliasun oikeellisuus
- Viittaa käytettyihin lähteisiin ohjeistuksen mukaisesti
- Älä kopioi muiden töitä ja ole tarkkana kuvien käyttöoikeuksien kanssa

## FSF Free Software Definition
- Free software ei ole käsitteenä ilmainen ohjelma
- Se antaa käyttälleen oikeuden käyttää, kopioida, jakaa muille ja opetella ohjelman koodia, muuttaa ja parannella koodia vapaasti
- Free software voi olla kaupallinen ohjelmisto
- Ohjelman jakamisessa voi olla rajoitteita pakkaustavan ja jakamisväylien suhteen, myös jakaminen tiettyihin maihin voi olla rajoitettua
- Säännöissä voi olla tulkinnan varaa
- kun ohjelmistoa muutetaan, tulee kirjata tarkat käyttöohjeet ja kaikki muutokset mitkä uuteen versioon on tehty

## Linuxin asennus virtuaalikoneeseen
Laitteisto: Itse rakennettu pöytäkone / intel Core i7-14700KF / 32GB ram /  käyttölevy 500GB ssd / GUI NVIDIA GeForce RTX 3060 Ti
- to 14:30 asensin Oracle VirtualBox Manager ohjelman koneelleni 
- asennusvaiheessa valitti python core pack ja win32 api bindings puuttetta
- Asensin python core pack:in jonka jälkeen asennus sujui ongelmitta ohjeiden mukaisesti
- to 16:50 latasin debian 12.9 live .iso tiedoston
- su 13:40 aloitin virtualboxin valmistelun debian asennusta varten ohjeiden mukaisesti
- su 13:50 boottasin virtualboxin debian live virtuaali cd:llä ja testasin kaikkia toimintoja
- su 14:15 aloitin debian asennuksen, asennus sujui ongelmitta ohjeita noudattaen
- su 14:30 ensimmäinen login, kaikki yhä sujui ongelmitta, kaikki toimii debianissa niin kuin pitääkin.
- su 14:45 suoritin ohjeen mukaiset päivitykset komentokehotteen kautta ja asensin sekä käyttöönotin palomuurin, boottasin uudelleen ja kaikki edelleen toimi.
- su 15:00 Aloitin guest addition for good resolution asennuksen, ohjeet toimivat hyvin, eikä ongelmia ollut tässäkään vaiheessa
- su 15:20 boottasin järjestelmän uudelleen ja sitten tuli black screen vastaan, ruudussa vilahti error: host log in failed.
- su 15:30 googlasin virheilmoitusta ja löysin debian user forums -sivuilta ohjeen vaihtaa virtualboxin graphics controller VMSVGA asetuksen toiseen optioon, tein näin ja buuttasin uudelleen, nyt toimi.
- su 15:45 nyt ruutu oli hyvän kokoinen ja testasin, että kaikki toimii niinkuin pitää. 






![Näyttökuva 2025-01-19 163025](https://github.com/user-attachments/assets/75a0ae0e-c5eb-48ed-87ac-98a014e3878d)

# Lähteet

https://terokarvinen.com/linux-palvelimet/
