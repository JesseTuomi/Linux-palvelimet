# MAAILMA KUULEE

## x)
- Valitse ja vuokraa virtuaalipalvelin haluamaltasi sivustolta
- Tunnistaudu mielummin SSH-avaimilla
- Tarkista luomasi palvelimen IP-osoite
- Asenna apache2 virtuaalipalvelimelle
- Tee palomuuriin reikä SSH-yhteyttä varten ja kytke palomuuri päälle. (sudo ufw allow 22/tcp ja sudo ufw enable)
- Luo uusi käyttäjä ja tee käyttäjästä pääkäyttäjä. (sudo adduser jesse ja sudo aduuser jesse sudo)
- Päivitä virtuaalipalvelin käskyllä sudo apt-get update ja sudo apt-get upgrade
## a)
Käytin pilvipalvelunani DigitalOcean palvelua, koska sen saa ilmaiseksi GitHub Education paketin kautta. Valitsin paketin jossa on tuo 1GB rammia ja 25GB levytilaa. 
En saanut alustavasti SSH yhteyttä toimimaan, palaan asiaan myöhemmin. Suoritin yhteyden salasanan avulla. Muuten yhteys ja serveri toimivat ok nyt.

## b)
Suoritin käskyt sudo ufw allow 22/tcp, sudo ufw enable ja sudo ufw allow 80/tcp. En sulkenut vielä root tunnusta kun en saanut ssh salasanoja vielä toimimaan. Päivitin kaikki ohjelmat asennusten jälkeen sudo apt-get update komennolla

## c)
Asensin apache2 palvelimen virtuaalipalvelimelleni aivan kuten tein omallekkin virtuaali koneelle, vaihdoin index.html tiedoston omaani osoitteessa /var/www/html/index.html micro tekstinkäsittely ohjelmalla.
Kirjauduin virtuaalipalvelimeni URL osoitteeseen 165.22.93.67 ja se avasi sivuni ihan oikeassa netissä.

![image](https://github.com/user-attachments/assets/984e96f5-7699-4624-a897-daa6dfa45291)

# Lähteet

https://terokarvinen.com/linux-palvelimet/
digitalocean.com
github.com/education

