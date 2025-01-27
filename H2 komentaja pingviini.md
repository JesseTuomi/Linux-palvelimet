# H2 Komentaja Pingviini
tehtävä x)
- Opettele liikkumaan kansioissa, yleisimmät komennot ovat pwd/ls/cd/less/ls
- Lataa jokin tekstieditori kuten nano tai micro ja opettele tiedostojen tekemistä ja muokkaamista
- yleisiä komentoja ovat mkdir/mv/cp/rmdir/rm
- etäyhteyden otossa on hyvä käyttää turvattua yhteyttä, tämä tapahtuu avaamalla ssh joku@jokin.com suojattu yhteys
- exit komento on remotecomputer$ exit
- kansion kopiointi onnistuu komennolla scp -r FOLDER joku@jokin.com:public_html
- ohjeet saa komennolla man ls
- Tab näppäimen kaksoispainalluksella saa esiin ehdotuksia mahdollisista komennoista

 ## tehtävä a)
  Kirjoitin komentokehoitteeseen "sudo apt install micro" ja asennus tapahtui.

 ## tehtävä b)
  Kaikki kolme valitsemaani ohjelmaa asentuu kerralla komennolla "sudo apt update && sudo apt install -y htop tree nano" komento update myös varmistaa että saan uusimman pakettiversion.nan

  ![image](https://github.com/user-attachments/assets/1b8bf155-d5ed-4497-8bdd-73539be7ac37)

  tree komento näyttää nykyisen hakemiston puurakenteena
  
![image](https://github.com/user-attachments/assets/5d048f18-c3ff-4b18-8f52-dc03bda72995)

htop komento näyttää järjestelmän tiedot reaaliaikaisesti
![image](https://github.com/user-attachments/assets/206ccac4-0a72-42db-b854-a76927998ce3)

## tehtävä c)

![image](https://github.com/user-attachments/assets/5492c25d-4d64-41c7-85c4-7914f9df762f)

![image](https://github.com/user-attachments/assets/e836cf90-b596-4b3a-bbcf-ffa7a61460b7)

## tehtävä d)
tämä etsii tietyn sanan tiedostosta
![image](https://github.com/user-attachments/assets/4f60ad95-60da-4e7e-92e1-313e83a586f5)

tämä etsii tietyn sanan kaikista hakemiston tiedostoista
![image](https://github.com/user-attachments/assets/37f5a9ac-455d-48d3-9a28-4e73256f4ac7)

## tehtävä e)
tämä komento laskee kuinka monta kertaa jokin sana esiintyy kansiossa
![image](https://github.com/user-attachments/assets/3dd63094-4303-4bf5-8580-d8768961a73b)

## tehtävä f)
![image](https://github.com/user-attachments/assets/e1a0eb4d-1e34-4ec2-9d71-069ec9e232d3)

Tämä listaus näyttää VirtualBox:in käyttämän osuuden tietokoneeni laitteistosta ja perustuvatkin VirtualBox:in asetuksiin ja sen tekemiin laitteiden käyttöihin.
system on siis tuo virtuaali tietokone VirtualBox, jolla on käytössään 128KB BIOS muistia ja 4GB järjestelmän muistia. Prosessori on intel i7-14700KF.
Bridge tiedot kertovat väylien hallilntaan käytettävistä piirisarjoista, jotka ovat emolevyllä. Input tiedot ovat järjestelmään kytkettyjä ulkoisia tai virtuaalisia laitteita, kuten hiiri ja näppäimistö.
Volume tiedot ovat levyjen käytettävissä olevia lohkoja tai koko levyn tilavuuksia, tässä listauksessa on vain sen levyn tiedot jossa VirtualBox sijaitsee.
Bus tiedot tarkoittavat data, ohjaus tai osoiteväyliä ja disk kertoo että käyttettävissä on myös CD-ROM levyasema.
Storage kertoo tallennuslevyn tyypin, nimen ja mihin porttiin se on kytketty. Multimedia on äänilaite, joka on tässä tapauksessa emolevyyn integroitu laite.





