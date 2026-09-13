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
    visible: true
---

# ➡️ Kuinka pääsen alkuun?

Pörssärissä käyttöönoton järjestys on **käyttöpaikka ja rakennus → laite → ohjaukset → ohjausasetukset**. Esimerkeissä käyttöpaikka on **Testikiinteistö**, rakennus **Päärakennus**, laite **Testilaite** ja ohjaus **Lämminvesivaraaja**.

1. Avaa käyttäjävalikko ja valitse **Käyttöpaikat**-osiosta **Lisää käyttöpaikka**. Luo esimerkiksi Testikiinteistö. Pörssäri luo sille automaattisesti Päärakennuksen.
2. Avaa **Laitteet** ja valitse **Lisää laite**. Valitse laitteellesi sopiva käyttöönotto-ohje: [Shelly](../../kaeyttoeoenotto-ohjeet/ohjauslaitteiden-kaeyttoeoenotto/shelly-ohjauksen-lisaeaeminen/), [Home Assistant](../../kaeyttoeoenotto-ohjeet/ohjauslaitteiden-kaeyttoeoenotto/home-assistant-ohjauksen-lisaeaeminen/) tai [pilvilaite](../../kaeyttoeoenotto-ohjeet/ohjauslaitteiden-kaeyttoeoenotto/pilvilaitteen-lisaeaeminen.md).
3. Kun lisäät Shellyn, Home Assistantin tai mukautetun laitteen, valitse **Luo ohjaukset laitteen kanaville automaattisesti** ja kohderakennus. Shelly lisätään manuaalisena laitteena; adoptiokoodi ei ole tällä hetkellä käytössä. Pilvituonnissa rakennus valitaan laitekohtaisesti.
4. Avaa **Ohjaukset**, valitse esimerkiksi Lämminvesivaraaja ja säädä sen **Ohjausasetukset**.

Ohjausta ei tarvitse luoda erikseen ennen laitteen lisäämistä.

![Päärakennuksen ohjaukset Testikiinteistössä](../../.gitbook/assets/app-controls.png)



