# ansibel
## Eesmärk
Skript instaleerib wordpressi Apache2 peale ja lisab juurde weel mysql serveri ja phpmyadmini
#### github paigaldus
##### Paigaldamine
```
apt install git
```
##### Seadistamine
```
git config --global user.name "Eesnimi Perenimi"
git config --global user.email email@domeen.com
git config --global core.editor nano
```

#### Skriptid [Skriptid on väljatoodud käivitamise järjekorras]
##### apache.yml
Paigaldab Apache2 paketi

##### php7.yml
Paigalda php7.0 ja sellega kaasa tulevad paketi moodulid

##### mysql-server5.7.yml
MySQL serveri paigaldus ja root kasutaja loomine.
Root login fail asub kaustas /root/.my.cnf
###### mysql server
Kasutaja: root
Kasutaja parool: qwerty

#####  pma.yml
Instaleerbi phpmyadmini, mida on võimalk kätte saada lehelt: http://local-host/phpmyadmin

##### wordpress_paigaldus.sh
Skript tõmbab uusima wordpressi versiooni, pakib selle lahti ja muudab wp-config-sample.php faili
Tekkitab wordpressis uue kasutaja ja andmebaasi mida wordpress hakkab kasutama
###### mysql server
andmebaas:                  "wordpress"
andmebaasi kasutaja:        "wordpressuser"
andmebaasi kasutaja parool: "qwerty"

### Ligipääsemine
- Wordpressile saab ligi kirjutades url {serveri IP}/wordpress
- Myphpadminile saab ligi kirjutades url {serveri IP}/myphpadmin
