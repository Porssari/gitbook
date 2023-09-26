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

Pörssäri on helppokäyttöinen ohjauspalvelu kodin sähkölaitteiden hintaohjaukseen pörssisähkön hinnan sekä tarvittaessa myös aurinkopaneeleiden tuotannon perusteella. Lokakuun 2023 aikana julkaistaan lisäksi ulkolämpötilaan perustuva lämmityksen ohjausmahdollisuus. Sivuston ohjaus on mahdollista välittää useiden eri ohjauslaitteiden kautta. Pörssäri automatisoi sähkön käytön käyttäjän tekemien asetusten perusteella vuorokauden edullisimmille tunneille.

Pörssärin käyttöönotto onnistuu helpoiten Shelly-älyreleen avulla. Yhteensopivia malleja ovat Shelly Plus -mallin releet (1, 1PM, 2PM, mielellään ei PM-malleja kontaktoriohjaukseen) sekä Pro-mallin releet (mieluiten Pro1, Pro2 tai Pro3, myös Pro4PM, mutta mielellään ei PM-malleja kontaktoriohjaukseen). Lisäksi tarvitset sähköasentajan kytkemään Shellyn paikalleen.&#x20;

Nimestään huolimatta yksi luotettava verkkokauppa Shellyn hankkimiseksi on [Nurkan Takaa -verkkokauppa.](https://verkkokauppa.nurkantakaa.fi/) Kaupan omistaja Teemu Räikkönen on tunnettu Facebookin suomenkielisen Shelly -tukiryhmän ylläpitämisestä.

Shellyn lisäksi tällä hetkellä tuettuna on Home Assistant sekä Raspberry Pico W -releohjaus Micropython-pohjaisella järjestelmällä. Pörssärin ohjaustieto lähetetään asiakaslaitteeseen taustapalvelimelta JSON-muodossa siten, että laitteen ohjauskanavalle kerrotaan senhetkinen ohjaustila sekä aikataulu tilanmuutoksista niin pitkään kuin hintatietoa on saatavilla. Mikäli haluat käyttää omaa ohjauslaitetta Pörssärin ohjaustiedon välittämiseen sähkölaitteille, tutustu ohjesivuston "Kehittäjille" -osioon.
