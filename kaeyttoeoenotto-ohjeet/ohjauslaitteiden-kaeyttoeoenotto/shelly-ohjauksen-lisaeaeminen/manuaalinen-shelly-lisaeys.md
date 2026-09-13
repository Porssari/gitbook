# Shelly-laitteen manuaalinen lisääminen

Manuaalinen lisäys on tällä hetkellä oikea tapa lisätä Shelly Pörssäriin. Adoptiokoodi voi näkyä Lisää laite -valikossa, mutta sitä ei ole otettu käyttöön.

Sitä varten tarvitset Shellyn **12-merkkisen laitetunnisteen** ja tiedon käytettävien relekanavien määrästä.

## 1. Tarkista Shellyn laitetunniste

Laitetunnisteen löydät Shelly Smart Control -sovelluksesta laitteen kohdasta **Asetukset → Laitteen tiedot → Device ID**. Gen2- ja Gen3-laitteen paikallisessa rajapinnassa saman tiedon palauttaa `Shelly.GetDeviceInfo`-kutsun `id`-kenttä. Lisätietoa on [Shellyn teknisessä dokumentaatiossa](https://shelly-api-docs.shelly.cloud/gen2/ComponentsAndServices/Shelly/).

Kopioi Pörssäriin vain **12-merkkinen** id-osa, isoilla kirjaimilla ja numeroilla. Älä käytä kentässä laitteen IP-osoitetta tai itse keksittyä nimeä.

{% hint style="warning" %}
Älä syötä mallinimeä laitetunnuksen eteen.

* Väärin: `shellyplus1pm-AABBCCDDEEFF`
* Oikein: `AABBCCDDEEFF`

Shellyn käyttöliittymä tai MQTT-client-id voi näyttää muodon `malli-id`. Pörssäriin kopioidaan vain 12-merkkinen id-osa.
{% endhint %}

## 2. Avaa manuaalinen laitelomake

1. Avaa Pörssärissä oikea käyttöpaikka.
2. Valitse **Laitteet → Lisää laite**.
3. Valitse **Manuaalinen laite**. Vaihtoehdon kuvauksessa mainitaan Shelly, Home Assistant ja mukautettu laite.

Valikossa voi näkyä myös adoptiokoodi; älä käytä sitä.

## 3. Anna laitteen tiedot

Täytä lomake seuraavasti:

- **Laitteen nimi:** kuvaava nimi, esimerkiksi **Shelly Testilaite**.
- **Laitetyyppi:** **Shelly**.
- **Ohjauskanavamäärä:** valitse Pörssärin ohjaukseen käytettävien relekanavien määrä.
- **Laitetunniste:** Shellyn 12-merkkinen Device ID ilman mallinimeä.
- **Luo ohjaukset laitteen kanaville automaattisesti:** pidä valinta käytössä.
- **Valitse rakennus mihin ohjaukset luodaan:** valitse esimerkiksi **Päärakennus**.

![Shelly-laitteen manuaalinen lisäys](../../../.gitbook/assets/app-manual-shelly-add.png)

Kuvan laitetunnus on esimerkki. Korvaa se oman Shelly-laitteesi 12-merkkisellä Device ID -tunnisteella.

Valitse lopuksi **Lisää laite**.

{% hint style="info" %}
Manuaalinen lisäys luo valituille kanaville ohjaukset automaattisesti. Ohjauksia ei luoda erikseen käsin.
{% endhint %}

## 4. Tarkista laite ja ohjaukset

Tarkista **Laitteet**-näkymästä, että Shelly ja sen kanavat näkyvät. Avaa sitten **Ohjaukset** ja varmista, että kanaville syntyneet ohjaukset ovat valitussa rakennuksessa. Nimeä ohjaukset niiden käyttötarkoituksen mukaan, esimerkiksi **Lämminvesivaraaja** tai **Lattialämmitys**.

Jatka tarvittaessa [Pörssäri-skriptin asennusohjeeseen](ohjausskriptin-lisaeaeminen-shelly-laitteeseen/README.md).
