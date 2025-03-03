## h6 Salataampa

# x) Lue ja tiivistä

# let´s encrypt

- Let`s encrypt tarjoaa ACME protokollan kautta ilmaista salauspalvelua palvelimille
- palvelu tekee sertifikaatin automaattisesti sivustolle
- Palvelu tunnistaa palvelimen adminin julkisen avaimen avulla
- Se muodostaa uuden avain parin palvelimen ja palvelun välille.
- Sertifikaatti uusitaan 90 päivän välein automaattisesti tai käskyllä: sudo certbot renew --dry-run

# Lange 2024: Lego

- Asenna Certbot ja Lego: Varmista, että Certbot ja Lego ovat asennettuina palvelimellasi.
- Pysäytä verkkopalvelin tilapäisesti: Jos mahdollista, sulje Apache/Nginx hetkeksi vapauttaaksesi portin 80.
- Luo hakemisto todentamista varten: Tee hakemisto, johon Let’s Encrypt voi tallentaa vahvistustiedoston (esim. /var/www/html/.well-known/acme-challenge/).
- Käynnistä verkkopalvelin uudelleen: Varmista, että se palvelee tiedostoja tästä hakemistosta.
- Suorita Lego-komento: lego --email="sähköposti@example.com" --domains="example.com" --http --http.webroot="/var/www/html" run
- Sertifikaatti tallentuu hakemistoon: Löydät sen esim. ~/.lego/certificates/.
- Ota käyttöön verkkopalvelimessa: Määritä Apache käyttämään haettua sertifikaattia.

# The apache Software Foundation 2025

- Lataa ja asenna mod_ssl: Varmista, että SSL/TLS-tuki on asennettu Apachelle.
- Ota SSL-moduuli käyttöön: sudo a2enmod ssl / sudo systemctl restart apache2
- Lisää seuraavat asetukset VirtualHost-lohkoon: SSLEngine on / SSLCertificateFile /etc/letsencrypt/live/example.com/fullchain.pem / SSLCertificateKeyFile /etc/letsencrypt/live/example.com/privkey.pem
- Käynnistä Apache uudelleen: sudo systemctl restart apache2
- Testaa HTTPS-yhteys: Avaa https://example.com ja varmista, että SSL toimii.




# a) LET´s

Aloitin asentamalla serverilleni lego ohjelman komennolla: sudo apt-get lego. 
Asensin certbot ohjelman komennolla: sudo apt install certbot python3-certbot-apache
Hankin ja asensin SSL-sertifikaatin komennolla: sudo certbot --apache
Sain asennuksen lopuksi viestin komentokehoitteeseen: 

Successfully received certificate.
Certificate is saved at: /etc/letsencrypt/live/jessetuomi.me/fullchain.pem
Key is saved at:         /etc/letsencrypt/live/jessetuomi.me/privkey.pem
This certificate expires on 2025-06-01.
These files will be updated when the certificate renews.
Certbot has set up a scheduled task to automatically renew this certificate in the background.

Deploying certificate
Successfully deployed certificate for jessetuomi.me to /etc/apache2/sites-available/jessetuomi.me-le-ssl.conf
Successfully deployed certificate for www.jessetuomi.me to /etc/apache2/sites-available/jessetuomi.me-le-ssl.conf
Congratulations! You have successfully enabled HTTPS on https://jessetuomi.me and https://www.jessetuomi.me


Avasin portin 443 komennolla: sudo ufw allow 443/tcp
Potkaisin demonia ja avasin nettisivuni jessetuomi.me

![Näyttökuva 2025-03-03 133514](https://github.com/user-attachments/assets/68f96fe9-e0df-426c-b157-0b384e6d86cf)

Nyt salaus toimii.

# b) A-Rating

Menin ssllabs.com sivustolle ja syötin palvelimeni osoitteen jessetuomi.me
Ohjelmisto testasi sivuni ja sain lopputuloksena seuraavaa:

![image](https://github.com/user-attachments/assets/2122dbb4-9bf9-47b5-877a-60ec5bc9cc45)

![image](https://github.com/user-attachments/assets/742d9331-3ef9-4b1e-bfb8-f157ce7c98d6)

![image](https://github.com/user-attachments/assets/0a22c385-a2ad-40d9-938d-2f649f97346f)

![image](https://github.com/user-attachments/assets/f45bdd89-4fce-4ee4-bd7d-0fa5ff70546b)

![image](https://github.com/user-attachments/assets/b2388cd8-750e-41f5-b932-da98c8990f2d)

![image](https://github.com/user-attachments/assets/d6dbc29f-8c39-4ba0-98f1-5382993fa3aa)



