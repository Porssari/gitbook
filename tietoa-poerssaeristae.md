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

# 📓 Muita kysymyksiä ja vastauksia

### Onko Pörssäri luotettava palvelu?

Pörssäri on harrastepohjalta rakennettu palvelu, joka on ensisijaisesti tehty omiin käyttötarpeisiin. Emme lupaa suoraa asiakastukea, mutta ongelmatilanteita pyritään mahdollisuuksien mukaan ratkaisemaan yhteistyössä käyttäjien kanssa. Ongelmatilanteiden varalle sivustolta löytyy yhteydenottolomake, ja lisäksi tukea voi pyytää sähköpostitse osoitteesta info(at)porssari.fi.

Pörssäri on käyttäjälle maksuton kaikkien käytettävissä olevien ominaisuuksien osalta nyt ja aina tulevaisuudessa.

### Mistä sähkön hintatiedot haetaan?

Pörssäri hakee sähkön Spot-hintatiedot ensisijaisesti ENTSO-E -rajapinnasta. Varapalveluna käytetään Eleringin tarjoamaa rajapintaa.

### Miksi Pörssärissä ei näytetä sähkön hintatietoja kaikille?

Sähkön hintatietojen uudelleenjulkaisu on Nord Poolin lisenssiehdoilla rajoitettua. Hintojen näkyvyys sovelluksessa riippuu käyttäjätilin oikeuksista. Emme pystyisi tarjoamaan ilmaispalvelua ilman Nord Poolin hyväksyntää lisenssittömälle hintatietojen käytölle.

### Miksi Pörssäriin täytyy rekisteröityä?

Haluamme tarjota varmatoimisen ohjausratkaisun kaikille käyttäjille. Rekisteröinnin avulla saamme sekä tallennettua käyttäjäkohtaiset asetukset että hallittua Pörssärin palvelinkuormaa. Lisäksi rekisteröitymisen yhteydessä annettu sähköpostiosoite toimii tiedotuskanavana palveluun liittyvistä asioista.

Rekisteröityminen on maksutonta, sen voi tehdä halutessaan myös anonyymisti ja rekisteröityneiden käyttäjien tietoja ei luovuteta eteenpäin eikä käytetä mainontaan tai muihinkaan Pörssärin toimintaan liittymättömiin tarkoituksiin.

### Voinko testata palvelun käyttöä?

Rekisteröityminen osoitteessa [https://porssari.fi/app/](https://porssari.fi/app/) on maksutonta. Voit vapaasti kokeilla Pörssäri-palvelua haluamasi ajan. Mikäli et halua jatkaa palvelun käyttöä, voit pyytää käyttäjätilisi poistamista sivuston palautelomakkeen kautta.

### Tarvitseeko minun käyttää Shelly Cloud -palvelua?

Pörssäri ei tarvitse eikä halua saada käyttöoikeutta käyttäjän Shelly Cloud -palveluun. Shelly-relettä ei ole myöskään välttämätöntä lisätä Cloud-palveluun ollenkaan releohjauksen käyttöönottamiseksi.

### Voinko käyttää Shelly-relettä muuhun kuin Pörssäriin?

Pörssärin ohjausohjelma huomioi toiminnassaan ainoastaan ne Shellyn kanavat, joiden tila on Pörssärin asetuksissa jokin muu kuin "ei käytössä". Voit siis käyttää osaa ohjauskanavista Shelly-releessä muihin tarkoituksiin, eikä Pörssärin ohjausohjelma ohjaa näitä kanavia.

Mikäli huomaat lyhyen kokeilun jälkeen, että Pörssäri ei ole sopiva omiin käyttötarpeisiisi, on Shelly-releille tarjolla useita muitakin kolmannen osapuolen pörssisähköohjauspalveluita. Lisäksi Shelly-relettä on mahdollista käyttää esimerkiksi ohjelmoitavana kellokytkimenä sellaisenaan.

### Onko Pörssärin käyttö maksullista?

Pörssärin käyttö on nyt ja tulevaisuudessa maksutonta. Kyseessä on harrastepohjalta ylläpidettävä palvelu, ja mikäli palvelinkapasiteetti alkaisi loppumaan, rajoitamme uusien käyttäjien määrää.

### Onko Pörssärin käyttö turvallista?

Sivuston ja laitetietokannan hallinnassa käytetään hyviä tietoturvakäytäntöjä. Ylläpitäjien käyttäjätilit on suojattu monivaiheisella tunnistautumisella. Käyttäjä voi ottaa tilillään käyttöön esimerkiksi salasanan, kertakäyttökoodin, Google-kirjautumisen, TOTP-sovelluksen tai WebAuthn-/passkey-tunnistautumisen sen mukaan, mitä tilille on otettu käyttöön.

Palvelimelta ei ole yhteyttä käyttäjän kotiverkossa oleviin laitteisiin suoraan, vaan ne hakevat ohjaustiedon REST-JSON -rajapintaa käyttäen.

Ulkoisten ohjauspalvelinten käyttäjätunnukset, salasanat ja api-tunnisteet säilytetään Pörssärin ohjaustietokannassa vahvasti salattuina.

### Mitä tietoja minusta kerätään?

Pörssäri kerää käyttäjältä rekisteröityessä pakollisina tietoina sähköpostiosoitteen, sekä lisäksi käyttäjä voi lisätä oman nimensä palveluun.

Älykkään lämmityslaiteohjauksen ja aurinkosähköennusteen käyttämiseksi käyttäjän tulee syöttää ohjattavan käyttöpaikan sijaintitiedot paikallisen sääennustedatan hakemisen mahdollistamiseksi. Käyttäjätiedot ja ohjaustiedot sijaitsevat toisistaan erillisissä tietokannoissa eikä ohjaustietokannassa säilytetä käyttäjän tunnistetietoja.

Shelly-laitteen tunnisteena käytetään Shellyn 12-merkkistä laitetunnusta. Kyselyn suorittavan laitteen julkinen ip-osoite voidaan tallentaa tietokantaan palvelinkyselyiden määrän hallinnassa.

### Saako palvelua käyttää VPN-yhteyden tai välityspalvelimen kautta?

Käyttöehdoissamme ei kielletä palvelun käyttöä VPN-yhteyden tai välityspalvelimen välityksellä. Palvelinyhteyksien sallimisessa saattaa olla maakohtaisia rajoituksia ja samasta IP-osoitteesta tulevia kyselyitä rajoitetaan aikakohtaisesti. Huomioithan tämän mikäli käytät julkista VPN-osoitetta.

### Ylläpidetäänkö Pörssäriä pitkäaikaisesti?

Pörssäri-palvelu tulee olemaan käytettävissä pitkäaikaisesti sivuston omistajien omien laitteiden hallinnan vuoksi. Mikäli tulevaisuudessa Pörssärin aktiivinen ylläpito päättyisi, tultaisiin sekä ohjauslogiikkaan liittyvät palvelintiedostot että kattava dokumentaatio ohjauslogiikasta mukaanlukien tietokantaparametrien käyttö jakamaan julkisesti saataville.
