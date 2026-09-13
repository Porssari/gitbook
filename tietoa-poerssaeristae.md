---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: false
  pagination:
    visible: false
---

# 📖 Muita kysymyksiä ja vastauksia

### Onko Pörssäri luotettava palvelu?

Pörssäri on harrastepohjalta rakennettu palvelu, joka on ensisijaisesti tehty omiin käyttötarpeisiin. Emme lupaa suoraa asiakastukea, mutta ongelmatilanteita pyritään mahdollisuuksien mukaan ratkaisemaan yhteistyössä käyttäjien kanssa. Ongelmatilanteiden varalle sivustolta löytyy yhteydenottolomake, ja lisäksi tukea voi pyytää sähköpostitse osoitteesta info(at)porssari.fi.

Pörssäri on käyttäjälle maksuton kaikkien käytettävissä olevien ominaisuuksien osalta nyt ja aina tulevaisuudessa.

### Mistä sähkön hintatiedot haetaan?

Pörssäri hakee Spot-hintatiedot ensisijaisesti ENTSO-E-rajapinnasta. Varapalveluna käytetään Eleringin rajapintaa.

### Miksi Pörssärissä ei näytetä sähkön hintatietoja kaikille?

Sähkön hintatietojen uudelleenjulkaisu on Nord Poolin lisenssiehdoilla rajoitettua. Hintojen näkyvyys sovelluksessa riippuu käyttäjätilin oikeuksista. Emme pystyisi tarjoamaan ilmaispalvelua ilman Nord Poolin hyväksyntää lisenssittömälle hintatietojen käytölle.

### Miten aloitan käytön?

Rekisteröidy ja kirjaudu [Pörssäri-sovellukseen](https://porssari.fi/app/) sähköpostiosoitteella tai Google-tilillä. Lisää ensin käyttöpaikka; Pörssäri luo sille automaattisesti Päärakennuksen. Lisää sitten laite. Laitteen kanaville luodaan ohjaukset laitelisäyksen yhteydessä. Katso [aloitusohje](sivuston-ohjeet/aika-ja-hintaohjaus/README.md).

### Miksi Pörssäriin täytyy rekisteröityä?

Haluamme tarjota varmatoimisen ohjausratkaisun kaikille käyttäjille. Rekisteröinnin avulla saamme sekä tallennettua käyttäjäkohtaiset asetukset että hallittua Pörssärin palvelinkuormaa. Lisäksi rekisteröitymisen yhteydessä annettu sähköpostiosoite toimii tiedotuskanavana palveluun liittyvistä asioista.

Rekisteröityminen on maksutonta, sen voi tehdä halutessaan myös anonyymisti ja rekisteröityneiden käyttäjien tietoja ei luovuteta eteenpäin eikä käytetä mainontaan tai muihinkaan Pörssärin toimintaan liittymättömiin tarkoituksiin.

### Mitä kirjautumistapoja voin käyttää?

Käyttäjäprofiilin **Kirjautumistavat**-välilehti näyttää omalle tilillesi käytettävissä olevat vaihtoehdot. Niitä voivat olla salasana, sähköpostin tai tekstiviestin kertakäyttökoodi ja autentikointisovelluksen TOTP-koodi. Tarjolla olevat menetelmät riippuvat tilistä ja palvelun asetuksista. Käytä vain profiilissa näkyviä vaihtoehtoja.

### Voinko testata palvelun käyttöä?

Rekisteröityminen osoitteessa [https://porssari.fi/app/](https://porssari.fi/app/) on maksutonta. Voit vapaasti kokeilla Pörssäri-palvelua haluamasi ajan. Mikäli et halua jatkaa palvelun käyttöä, voit pyytää käyttäjätilisi poistamista sivuston palautelomakkeen kautta.

### Tarvitseeko minun käyttää Shelly Cloud -palvelua?

Ei. Pörssäri ei tarvitse käyttöoikeutta Shelly Cloud -tiliisi Shelly-ohjauksen käyttöönottoa varten.

### Voinko käyttää Shelly-relettä muuhun kuin Pörssäriin?

Kyllä. Ota Pörssärin ohjaukseen vain ne kanavat, joita haluat palvelun ohjaavan. Tarkista kanavien ja ohjausten asetukset ennen käyttöönottoa.

### Onko Pörssärin käyttö maksullista?

Pörssärin käyttö on nyt ja tulevaisuudessa maksutonta. Kyseessä on harrastepohjalta ylläpidettävä palvelu, ja mikäli palvelinkapasiteetti alkaisi loppumaan, rajoitamme uusien käyttäjien määrää.

### Onko Pörssärin käyttö turvallista?

Laite muodostaa itse tarvitsemansa yhteydet palveluun; Pörssäri ei avaa suoraa yhteyttä käyttäjän kotiverkkoon. Pilvipalvelun tunnukset syötetään vain yhteyden muodostamiseen tarkoitettuun lomakkeeseen. Käytä vahvaa, yksilöllistä salasanaa ja pidä myös laitteiden ohjelmistot ajan tasalla.

Sivuston ja laitetietokannan hallinnassa käytetään hyviä tietoturvakäytäntöjä. Ylläpitäjien käyttäjätilit on suojattu monivaiheisella tunnistautumisella. Käyttäjä voi ottaa tilillään käyttöön esimerkiksi salasanan, kertakäyttökoodin, Google-kirjautumisen, TOTP-sovelluksen tai WebAuthn-/passkey-tunnistautumisen sen mukaan, mitä tilille on otettu käyttöön.

### Mitä tietoja palvelu tarvitsee?

Palvelu tarvitsee käyttäjätilin ja ohjausten asetukset. Rekisteröityessä pakollisena tietona kerätään sähköpostiosoite; käyttäjä voi lisäksi lisätä nimensä. Käyttöpaikan sijaintitietoja voidaan tarvita sää- tai aurinkoennustetta käyttäville ohjauksille. Käyttäjätiedot ja ohjaustiedot sijaitsevat toisistaan erillisissä tietokannoissa, eikä ohjaustietokannassa säilytetä käyttäjän tunnistetietoja.

Älä julkaise laitetunnisteita, adoptiokoodeja tai pilvipalvelujen tunnuksia. Kyselyn suorittavan laitteen julkinen IP-osoite voidaan tallentaa tietokantaan palvelinkyselyiden määrän hallinnassa.

### Saako palvelua käyttää VPN-yhteyden tai välityspalvelimen kautta?

Käyttöehdoissamme ei kielletä palvelun käyttöä VPN-yhteyden tai välityspalvelimen välityksellä. Palvelinyhteyksien sallimisessa saattaa olla maakohtaisia rajoituksia ja samasta IP-osoitteesta tulevia kyselyitä rajoitetaan aikakohtaisesti. Huomioithan tämän, mikäli käytät julkista VPN-osoitetta.

### Ylläpidetäänkö Pörssäriä pitkäaikaisesti?

Pörssäri-palvelu tulee olemaan käytettävissä pitkäaikaisesti sivuston omistajien omien laitteiden hallinnan vuoksi. Mikäli tulevaisuudessa Pörssärin aktiivinen ylläpito päättyisi, tultaisiin sekä ohjauslogiikkaan liittyvät palvelintiedostot että kattava dokumentaatio ohjauslogiikasta mukaan lukien tietokantaparametrien käyttö jakamaan julkisesti saataville.

### Mistä saan apua?

Ongelmatilanteissa voit ottaa yhteyttä Pörssärin palautekanavan kautta tai sähköpostitse osoitteeseen info(at)porssari.fi.
