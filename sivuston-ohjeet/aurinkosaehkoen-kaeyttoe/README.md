---
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# 🌞 Aurinkosähkön käyttö

Pörssäri tarjoaa mahdollisuuden aurinkosähkön tuottoennusteen hyödyntämiseen ohjattavien laitteiden ohjauksessa. Ohjauslogiikka pyrkii huolehtimaan siitä, että vuorokauden sisällä sähkön kokonaiskustannus on käyttäjälle mahdollisimman edullinen.

Aurinkosähköennuste haetaan forecast.solar -palvelusta käyttäjän syöttämien koordinaattien mukaisesti. Aurinkoennuste päivitetään kuluvaa vuorokautta seuraavasta päivästä eteenpäin jotta jo toteutettuihin ohjauksiin ei tulisi muutoksia aurinkoennusteen päivittyessä.

Ohjauskuorman asetuksissa halutaan haluttu tuntimäärä vuorokaudessa aurinkosähköä hyödyntävälle ohjaukselle. Kyseinen tuntimäärä kytketään aina vuorokauden sisällä päälle aurinkoennusteesta huolimatta. Mikäli aurinkopaneelit eivät tuota ollenkaan, kytketään vuorokauden edullisimmat tunnit päälle.

Aurinkosähköohjaus vaatii toimiakseen käyttöpaikkaan lisätyt aurinkovoimalat. Lisäksi hintalaskennan onnistumiseksi on tärkeää lisätä käyttöpaikalle mukautetut hinta-asetukset sähkön kokonaishinnan laskemista varten.
