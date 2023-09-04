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

# 💡 Aika- ja hintaohjaus

Aika- ja hintaohjaus on manuaalinen ohjaustila, missä Pörssäri etsii käyttäjäasetusten mukaan joko

* vuorokauden edullisimmat tunnit ja kytkee ne päälle
* vuorokauden kalleimmat tunnit ja jättää ne kytkemättä päälle
* tunnit, mitkä ovat alle tai yli käyttäjän asettaman hintarajan ja ohjaa sen perusteella
* tunnit, mitkä ovat alle tai yli laskennallisen hintarajan, esimerkiksi vuorokauden keskihinta

Ohjaus on mahdollista asettaa vain osaan vuorokautta, eli mikäli on tarve lämmittää esimerkiksi käyttövettä aina yöllä jotta vesi riittää päivän tarpeisiin, voi Pörssäri etsiä edullisimmat tunnit aina väliltä 00-08.

Lisäksi Pörssärissä on mahdollista määrittää joko kaikille päiville yhteiset tai viikonpäivän mukaan määritetyt tunnit, mitkä kytketään aina päälle hinnasta riippumatta.

Releohjaus on mahdollista ohjata myös "käänteisesti", eli kun ohjausehdon mukaan kytketään laitteeseen virta, ohjauslaite kytketään pois päältä.
