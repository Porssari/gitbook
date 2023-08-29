# 📪 Aurinkosähkön käyttö

Pörssäri tarjoaa mahdollisuuden aurinkosähkön tuottoennusteen hyödyntämiseen ohjattavien laitteiden ohjauksessa. Älykäs taustalogiikka huolehtii siitä, että vuorokauden sisällä sähkön kokonaiskustannus on käyttäjälle mahdollisimman edullinen.

Aurinkosähköennuste haetaan forecast.solar -palvelusta käyttäjän syöttämien koordinaattien mukaisesti. Aurinkoennuste päivitetään kuluvaa vuorokautta seuraavasta päivästä eteenpäin jotta jo toteutettuihin ohjauksiin ei tulisi muutoksia aurinkoennusteen päivittyessä.

Laitehallinnan asetuksissa valitaan tuntimäärä mikä aurinkosähköä hyödyntävän laitteen halutaan olevan kytkettynä. Kyseinen tuntimäärä kytketään aina vuorokauden sisällä päälle aurinkoennusteesta huolimatta. Mikäli aurinkopaneelit eivät tuota ollenkaan, kytketään vuorokauden edullisimmat tunnit päälle.

Aurinkosähköennusteen käyttö edellyttää hinta-asetusten tekemistä sivustolle. Huomioithan siirtotariffissa myös sähköveron osuuden!
