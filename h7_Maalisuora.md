## H7 MAALISUORA

# Hei maailma a)

Avasin virtuaalikoneen ja päivitin tuttuun tapaan. 
Avasin micron ja kirjoitin hello world kolmella kielella ohjelmaksi. 

![image](https://github.com/user-attachments/assets/26e010ef-131c-4fbd-82c2-aac215965007)

Tallensin scriptin ja ajoin sen.

![image](https://github.com/user-attachments/assets/aef2feaa-e598-42e0-89a3-e4cca8d0f758)

# b.) Lisäsin puuttuvat lähdeviitteet aikaisempiin tehtäviini.

# c.) Uusi komento kaikille

Tein microlla ohjelman joka kysyy käyttäjän syntymäajan ja kertoo sen perusteella käyttäjän iän. Käytin ohjelman tekemiseen visual studion co pilot assistanttia.

![image](https://github.com/user-attachments/assets/775a331d-46f0-464d-99e7-8c6fdef30f0b)

Sitten siirsin ohjelman /usr/local/bin/ -hakemistoon ja samalla nimesin komennon age.sh pelkäksi age komennoksi 
Tähän käytin komentoa: sudo mv age.sh /usr/local/bin/age
Sitten annoin kaikille käyttäjille execute oikeudet komennolla: sudo chmod +x /usr/local/bin/age.
Testasin ohjelmaa 

![image](https://github.com/user-attachments/assets/78d49e6e-839f-41c4-af9b-664b9f63cff6)

# e) Uuden linuxin asennus

Latasin debian 12.9. gnomen .iso liven ja laitoin sen virtuaali asemaan.
Laitoin muisti ja prossu asetukset sopiviksi

![image](https://github.com/user-attachments/assets/21ce13c5-ed95-4827-8b1b-71a9d3a63c03)

Asetin virtuaali kovalevyn asetukset kohdalleen

![image](https://github.com/user-attachments/assets/0d046fe1-8f40-4203-8827-a1c3f47dd995)

Sitten hyväksyin tiedot ja loin uuden virtuaalikoneen debianin asennusta varten.

![image](https://github.com/user-attachments/assets/ebebe98a-f187-46b1-961e-a3823e3e9765)

boottasin virtuaali koneen ja valitsin käynnistykseen Live vaihtoehdon, kokeilin että kaikki toimii ja aloitin asennuksen.
Asennuksen jälkeen testasin jälleen, että järjestelmä toimii ja sitten ajoin päivitykset komentokehoitteen kautta.
Sitten asensin firewallin ja laitoin sen päälle. 
$ sudo apt-get -y install ufw
$ sudo ufw enable
Sitten uusi virtuaali linux onkin valmis lopputehtävään.

# Lähteet
https://terokarvinen.com/linux-palvelimet/




