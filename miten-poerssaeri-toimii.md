# ❓ Miten Pörssäri toimii?

Pörssäri ohjaa kodin sähkölaitteita päälle ja pois älyreleiden avustuksella. Palvelinkyselyn perusteella asiakaslaite saa taustapalvelimelta käyttäjäasetusten, sähkön hintatietojen sekä mahdollisen sääennusteen ja aurinkoennusteen perusteella lasketun päällä/pois -ohjaustiedon.

Ohjaustieto lähetetään laitteeseen:

* aina asiakaslaitteen käynnistyessä
* kun käyttäjäasetuksia muutetaan
* mikäli edellisestä ohjaustiedon lähettämisestä on kulunut yli tunti aikaa.

Tavanomaisiin ns. pilvipalveluihin tai muihin Shellyn ohjausskripteihin verrattuna Pörssärin ohjausohjelma ei vaadi jatkuvaa internet-yhteyttä. Ihannetilanteessa ohjaustietoa tallennetaan vastaanottavaan laitteeseen noin 30h eteenpäin kun seuraavan päivän hintatiedot on NordPoolin toimesta julkaistu.

Käyttäjäasetuksia voidaan muuttaa mistä tahansa sijainnista internet-yhteyden välityksellä. Pörssärin kautta ei kuitenkaan ole pääsyä käyttäjän kotiverkkoon, sillä ohjaustieto palautetaan vastauksena ohjauslaitteen suorittamaan kyselyyn. Pörssäri ei tarvitse toimiakseen Shellyn Cloud -ominaisuutta, mutta sen käytölle ei myöskään ole mitään estettä.

<figure><img src=".gitbook/assets/toimintakaavio.png" alt=""><figcaption></figcaption></figure>

Pörssärin etuna on helppokäyttöinen asetusten muokkaus. Käyttäjän ei tarvitse tehdä muutoksia Pörssärin Shelly-ohjelmakirjaston kautta haettuun valmiiseen ohjelmakoodiin. Lisäksi asetukset ovat tallessa taustapalvelimella mikäli ohjausohjelma päivitetään, tai ohjauslaite syystä tai toisesta vioittuu ja joudutaan vaihtamaan uuteen. Mikäli käytössä olisi skriptiohjaus missä asetukset on tallennettuna skriptin joukkoon, tulisi käyttäjäasetukset tehdä päivityksen yhteydessä aina uudelleen.
