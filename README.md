---
cover: .gitbook/assets/banneri3.jpg
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: false
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# 🔌 Pörssärin ohjesivusto

Pörssäri on helppokäyttöinen ohjauspalvelu kodin sähkölaitteiden ohjaukseen pörssisähkön hinnan, ulkolämpötilaennusteen sekä aurinkopaneeleiden tuotantoennusteen perusteella.

Sähkön day-ahead -hintatiedot ovat NordPoolin omistamaa lisenssinalaista dataa, ja niiden uudelleenjakaminen ilman asianmukaista lisenssiä on kielletty. Pörssäri on selvittänyt yhdessä NordPoolin kanssa, että palvelu nykymuodossaan on vaatimusten mukainen, ja sitä voidaan ilmaispalveluna tarjota ilman hintatietojen uudelleenjakamislisenssiä.

Pörssärin käyttöönotto onnistuu helpoiten Shelly-älyreleen avulla. Luotettavia suomalaisia verkkokauppoja Shellyn hankintaan ovat esimerkiksi [Nurkan Takaa -verkkokauppa](https://verkkokauppa.nurkantakaa.fi/) sekä [Shellykauppa.fi](https://shellykauppa.fi).

Yhteensopivia malleja Pörssärin kanssa ovat kaikki Shelly Plus- ja Shelly Pro -sarjan releet mistä löytyy tuki skriptiohjaukselle. Tuki Shelly AddOn-switch -lisälaitteille on mahdollista saada toistaiseksi yksinkertaisella skriptimuutoksella, virallinen tuki tuodaan uudelle ohjaussivustolle 2024 ensimmäisen vuosineljänneksen aikana. Kontaktoriohjaukseen PM-mallit eivät ole suositeltavia.&#x20;

Lisäksi tarvitset sähköasentajan kytkemään Shellyn paikalleen.&#x20;

Shellyn lisäksi tällä hetkellä tuettuna on Home Assistant sekä Raspberry Pico W -releohjaus Micropython-pohjaisella järjestelmällä. Testikäytössä on ilmalämpöpumpun ohjaus Sensibo-ohjauslaitetta hyödyntäen sekä Themo-lattialämmitystermostaattien ohjaus. Nämä tuodaan viralliseen käyttöön uudelle ohjaussivustolle, mutta mahdollisuus niiden käyttöön on saatavilla sivuston palautelomakkeella sitä pyytäen.
