---
layout:
  title:
    visible: true
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

Pörssäri on helppokäyttöinen ohjauspalvelu kodin sähkölaitteiden hintaohjaukseen pörssisähkön hinnan sekä aurinkopaneeleiden tuotannon perusteella. Sivuston ohjaus on mahdollista välittää useiden eri ohjauslaitteiden kautta. Pörssäri automatisoi sähkön käytön käyttäjän tekemien asetusten perusteella vuorokauden edullisimmille tunneille.

Pörssärin käyttöönotto onnistuu helpoiten Shelly-älyreleen avulla. Yhteensopivia malleja ovat Shelly Plus -mallin releet (1, 1PM, 2PM, ei PM-mallit kontaktorin kanssa) sekä Pro-mallin releet (mieluiten Pro1, Pro2 tai Pro3, ei PM-mallit kontaktorien kanssa). Lisäksi tarvitset sähköasentajan kytkemään Shellyn paikalleen. Luotettava verkkokauppa Shellyn hankkimiseksi on [Nurkan Takaa -verkkokauppa.](https://verkkokauppa.nurkantakaa.fi/)

Shellyn lisäksi tällä hetkellä tuettuna on Home Assistant sekä Raspberry Pico W -releohjaus Micropython-pohjaisella järjestelmällä. Pörssärin ohjaustieto lähetetään asiakaslaitteeseen taustapalvelimelta JSON-muodossa siten, että laitteen ohjauskanavalle kerrotaan senhetkinen ohjaustila sekä aikataulu tilanmuutoksista niin pitkään kuin hintatietoa on saatavilla. Mikäli haluat käyttää omaa ohjauslaitetta Pörssärin ohjaustiedon välittämiseen sähkölaitteille, tutustu ohjesivuston "Kehittäjille" -osioon.
