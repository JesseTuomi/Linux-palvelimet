# Hello Web Server

## tehtävä x)

- Name based virtual host tarkoittaa sitä, että serverillä on Http serverillä nimen käyttöön perustuva hostname, näin monet eri hostit voivat käyttää samaa IP osoitetta
- IP-based virtual host käyttää IP-osoitetta yhteyden muodostamiseen, jolloin jokaisella eri hostilla pitää olla eri IP-osoite
- Palvelin valitsee nimipalvelimen, rajaamalla ensin vaihtoehtoja IP-osoitteen perusteella ja vasta sitten valitsee parhaiten sopivan nimen haun perusteella
- Jos haussa käytetään * hakua IP-osoitehaku on irrelevantti
- Jos hakuehtoja vastaavaa serverin nimi tai serverin aliasta, joka täsmäisi haun IP-osoitteen ja portin kombinaation kanssa ei löydy, silloin ensimmäinen virtuaali hosti listalla joka sopii hakuun tulee valituksi
- Kun luodaan uusi virtual host block, tarvitaan vähintään ServerName ja DocumentRoot direktiivit, jotta järjestelmä löytää tarvittavat tiedot.
- Tyypillisesti yhdellä IP-osoitteella on monta verkkosivua hostattavana
- Apachea käytettäessä sinulla voi olla monia domain nimiä

## tehtävä a)

![image](https://github.com/user-attachments/assets/77218541-a153-46da-953c-885303c2e32d)

## tehtävä b)

![image](https://github.com/user-attachments/assets/49548738-31bc-476c-a59f-4e7ecddc1599)

Tätä en ymmärtänyt

## tehtävä c)

![image](https://github.com/user-attachments/assets/8dd6941c-208c-4305-8afb-2b5a89dc6b10)

## tehtävä d)


![image](https://github.com/user-attachments/assets/64d27837-2905-4959-82d7-183d448547f1)

## tehtävä f)

curl komento näyttää jonkin verkkosivun koodin esim.


![image](https://github.com/user-attachments/assets/90d750a1-c0b4-450e-aae6-138e5ad1cc56)

curl -I komento näyttää vain HTTP otsikot, esim:

![image](https://github.com/user-attachments/assets/851e9f16-d723-4f4b-b4fe-1dbba6887fac)

HTTP/1.1 200 OK Palvelin vastasi HTTP/1.1:lla, ja 200 OK tarkoittaa, että pyyntö onnistui.
date: on vain Palvelimen antama tarkka aika, jolloin vastaus luotiin.
server: kertoo mitä apache versiota käytetään ja Linux version.
Last Modified: kertoo koska tiedostoa on viimeksi muokattu
ETag: Uniikki tunniste tiedoston versiolle, jota käytetään välimuistin hallintaan.
Accept-Ranges: Tämä tarkoittaa, että palvelin tukee byte-tason osittaisia latauksia. Kun asiakas pyytää vain osan tiedostosta, palvelin pystyy palauttamaan sen pyydetyn osan ilman,
että koko tiedosto ladataan alusta alkaen.
Content-Lenght: on HTTP-otsake, joka kertoo vastauksen sisällön koon tavuina eli kuinka monta tavua vastausdataa on.
Vary: Tässä luetellaan pyynnön osa-alueet, joiden perusteella palvelin valitsee, mitä dataa se lähettää.
Content-Type: Missä tiedostomuodossa tiedoston sisältö on






