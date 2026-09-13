---
cover: .gitbook/assets/banneri3.jpg
coverY: 0
---

# 🔌 Pörssärin ohjesivusto

Pörssäri on kodin sähkölaitteiden ohjauspalvelu. Se muodostaa ohjauksia sähkön hinnan, käyttäjän asetusten sekä tarvittaessa sää- ja aurinkoennusteiden perusteella. Käyttö tapahtuu [Pörssäri-sovelluksessa](https://porssari.fi/app/).

Pörssärin käyttö on helppoa aloittaa rekisteröitymällä palveluun joko sähköpostiosoitteella tai Google-kirjautumista käyttäen. Lisää sen jälkeen sähkön käyttöpaikka, jolloin sille luodaan automaattisesti **Päärakennus**. Lisää seuraavaksi laite ja tarkista sen kanaville syntyneet ohjaukset. Tarkemmat vaiheet ovat [aloitusohjeessa](sivuston-ohjeet/aika-ja-hintaohjaus/README.md) ja [laitteiden käyttöönotossa](kaeyttoeoenotto-ohjeet/ohjauslaitteiden-kaeyttoeoenotto/).

Sähkön day-ahead-hintatiedot ovat Nord Poolin omistamaa lisenssinalaista dataa, ja niiden uudelleenjakaminen ilman asianmukaista lisenssiä on kielletty. Pörssäri on selvittänyt yhdessä Nord Poolin kanssa, että palvelu nykymuodossaan on vaatimusten mukainen ja sitä voidaan tarjota ilmaispalveluna ilman hintatietojen uudelleenjakamislisenssiä.

Pörssärin käyttöönotto onnistuu helpoiten Shelly-älyreleen avulla. Shellyn voi hankkia esimerkiksi [Nurkan Takaa -verkkokaupasta](https://verkkokauppa.nurkantakaa.fi/) tai [Shellykauppa.fi-verkkokaupasta](https://shellykauppa.fi). Kauppiailta voi pyytää apua oikean releen valintaan.

Pörssärin kanssa yhteensopivia ovat Shelly Plus-, Shelly Pro-, Shelly Pro 3EM + Add-on-, Shelly Gen3- ja Shelly Gen4 -sarjojen releet, joissa on skriptiohjauksen tuki. Kontaktoriohjaukseen PM-mallit eivät ole suositeltavia.

Teetä Shellyn kiinteään sähköasennukseen liittyvät kytkennät sähköalan ammattilaisella. Lisätietoa sallituista sähkötöistä on [Tukesin ohjeessa](https://tukes.fi/kodin-sahkoturvallisuus/mita-sahkotoita-saan-tehda-itse).

Shellyn lisäksi tuettuina ovat Home Assistant, Raspberry Pico W -releohjaus Micropython-pohjaisella järjestelmällä sekä mukautettu laite. Pilvipalveluista julkisesti tuettuina ovat Sensibo ja Themo. Muita pilvipalveluita voi olla saatavilla esikatseluominaisuuksina.
