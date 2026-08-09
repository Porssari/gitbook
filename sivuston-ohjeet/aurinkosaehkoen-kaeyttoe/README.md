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

Aurinkosähköennuste haetaan forecast.solar-palvelusta käyttäjän syöttämien koordinaattien perusteella. Ennuste päivitetään kuluvaa vuorokautta seuraavasta päivästä alkaen, jotta ennusteen päivitys ei muuta jo toteutettuja ohjauksia.

Ohjauksen asetuksissa määritetään haluttu tuntimäärä vuorokaudessa. Tämä tuntimäärä toteutetaan aurinkoennusteesta riippumatta. Jos paneelit eivät tuota lainkaan, ohjaus käyttää vuorokauden edullisimpia tunteja.

Aurinkosähköohjaus vaatii toimiakseen käyttöpaikalle lisätyt aurinkovoimalat. Lisäksi hintalaskennan onnistumiseksi on tärkeää lisätä käyttöpaikalle mukautetut hinta-asetukset sähkön kokonaishinnan laskemista varten.
