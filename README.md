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

Pörssäri on helppokäyttöinen ohjauspalvelu kodin sähkölaitteiden hintaohjaukseen pörssisähkön hinnan sekä tarvittaessa myös aurinkopaneeleiden tuotannon perusteella. Lokakuun 2023 aikana julkaistaan lisäksi ulkolämpötilaan perustuva lämmityksen ohjausmahdollisuus. Loppuvuoden aikana tuodaan tarjolle mahdollisuus ohjata Themon älytermostaattia web-rajapinnan kautta sekä Sensibo-tuki ilmalämpöpumpun ohjaukseen.

Sähkön day-ahead -hintatiedot ovat NordPoolin omistamaa lisenssinalaista dataa, ja niiden uudelleenjakaminen ilman asianmukaista lisenssiä on kielletty. Pörssäri on selvittänyt yhdessä NordPoolin kanssa, että palvelu nykymuodossaan on vaatimusten mukainen, ja sitä voidaan ilmaispalveluna tarjota ilman hintatietojen uudelleenjakamislisenssiä.

Pörssärin käyttöönotto onnistuu helpoiten Shelly-älyreleen avulla. Luotettavia suomalaisia verkkokauppoja Shellyn hankintaan ovat sekä [Shellykauppa.fi](https://shellykauppa.fi) että [Nurkan Takaa -verkkokauppa.](https://verkkokauppa.nurkantakaa.fi/)

Yhteensopivia malleja Pörssärin kanssa ovat kaikki Shelly Plus- ja Shelly Pro -sarjan releet mistä löytyy tuki skriptiohjaukselle. Tuki Shelly ProEM 50 -releelle sekä AddOn-switch -lisälaitteille tuodaan lähiaikoina. Kontaktoriohjaukseen PM-mallit eivät ole suositeltavia.&#x20;

Lisäksi tarvitset sähköasentajan kytkemään Shellyn paikalleen.&#x20;

Shellyn lisäksi tällä hetkellä tuettuna on Home Assistant sekä Raspberry Pico W -releohjaus Micropython-pohjaisella järjestelmällä. Pörssärin ohjaustieto lähetetään asiakaslaitteeseen taustapalvelimelta JSON-muodossa siten, että laitteen ohjauskanavalle kerrotaan senhetkinen ohjaustila sekä aikataulu tilanmuutoksista niin pitkään kuin hintatietoa osaatavilla. Mikäli haluat käyttää omaa ohjauslaitetta Pörssärin ohjaustiedon välittämiseen sähkölaitteille, tutustu ohjesivuston "Kehittäjille" -osioon.
