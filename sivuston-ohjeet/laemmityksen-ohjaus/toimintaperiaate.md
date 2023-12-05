# Toimintaperiaate

Pörssäri arvioi kiinteistön päivittäisen lämmitystarpeen talon vuosikulutuksen sekä yr.no -rajapinnasta haetun ulkolämpötilaennusteen perusteella. Koska lämmitys arvioidaan koko kiinteistölle, on tärkeää lisätä järjestelmään myös sellaiset käytössä olevat lämmitysjärjestelmät mitä Pörssäri ei ohjaa. Lisäksi talon energiantarve on tärkeää arvioida mahdollisimman oikein.

{% hint style="info" %}
Mikäli talossa on käytössä lämpöpumppu, ei sähkönkulutus vastaa talon lämmitysenergian tarvetta. Motivan sivuilta löytyy laskuri talon lämmitystarpeen arvioon neliömäärän, huonekorkeuden, henkilömäärän sekä rakennuksen sijainnin perusteella.

[https://lammitysvertailu.eneuvonta.fi](https://lammitysvertailu.eneuvonta.fi) (Kohta 1. Rakennuksen tiedot)
{% endhint %}

### Lämmitystarpeen hienosäätö

Mikäli ohjatut lämmitysjärjestelmät lämmittävät tasaisesti liikaa tai liian vähän, voit hienosäätää lämmitystarvetta lomakevalinnalla "Rakennuksen lämmitystarpeen hienosäätö". Mikäli talo lisääntyy/vähenee liikaa ulkolämpötilan laskiessa mutta on noin 0-asteen ulkolämmössä oikein, voidaan lämmitystarpeen muutosta hienosäätää valinnalla "Lämmitystarpeen muutoksen hienosäätö".

### Erilaiset lämmitysjärjestelmät

Kiinteistöön on mahdollista lisätä tyypiltään kolmea erilaista lämmitysjärjestelmää. Nämä ovat "Päälämmitysjärjestelmä", "Avustava lisälämmitysjärjestelmä" sekä "Mukavuuslämmitysjärjestelmä".&#x20;

#### Päälämmitysjärjestelmä (lasketaan lämmitystarpeen perusteella)

Kiinteistön päälämmitysjärjestelmäksi lisätään lämmityslaite/lämmityslaitteet, joiden halutaan tekevän pääosa lämmityksestä. Tällainen järjestelmä on esimerkiksi kiinteistön vesikiertoisen lämmityksen lämmönlähde, ilmalämpöpumppu tai suoran sähkölämmityksen ollessa kyseessä jokainen lämmityspiiri tai seinäpatteri joko yhteenlaskettuna tai erikseen.

{% hint style="info" %}
Mikäli talossa on vain yksi lämmitysjärjestelmä (seinäpatterit, lämpöpumppu vesikiertoisella lämmönjaolla, sähköinen lattialämmitys), sinun tarvitsee lisätä ainoastaan päälämmitysjärjestelmä. Voit lisätä jokaisen lämmityselementin joko omana yksikkönä tai vaihtoehtoisesti laskea niiden tehon yhteen, ja lisätä kaikki laitteet yhtenä järjestelmänä.
{% endhint %}

#### Avustava lisälämmitysjärjestelmä (lasketaan lämmitystarpeen perusteella)

Mikäli kiinteistön päälämmityslähteenä on esimerkiksi ilmalämpöpumppu, voidaan muut lämmitysjärjestelmät (sähköpatterit/sähköinen lattialämmitys) lisätä Pörssäriin avustavana lisälämmitysjärjestelmänä.

Voit määrittää avustavalle lisälämmitysjärjestelmälle minimäärän lämmitystarpeesta. Tämä tulee kysymykseen tilanteessa, missä halutaan esimerkiksi aina pieni määrä lämmitystä esimerkiksi lattialämmityksellä, mutta ilmalämpöpumppu hoitaa lämmityksestä pääosan.

Mikäli et määritä avustavalle lisälämmitysjärjestelmälle minimimäärää kytketään se päälle ainoastaan tilanteessa, missä päälämmitysjärjestelmän lämmitysteho ei riitä täyttämään lämmitysjakson tarvetta kokonaisuudessaan. Lisälämmitysteho kytketään päälle jakson edullisimpiin tunteihin.

{% hint style="info" %}
Mikäli et ohjaa päälämmönlähteenä olevaa lämpöpumppua Pörssärillä, mutta haluat silti automaattisen ohjauksen lisälämmönlähteisiin, tulee lämpöpumppu kuitenkin lisätä päälämmitysjärjestelmäksi oikean lämmitysmäärän arvioimista varten.
{% endhint %}

#### Mukavuuslämmitysjärjestelmä (ei vaikuta kiinteistön lämmitystarpeen arviointiin)

Mikäli haluat määrittää itse lämmityksen päälläolotunnit 0 ja -10 asteessa, voit lisätä lämmityslaitteen "Mukavuuslämmitysjärjestelmänä". Tällöin päälläoloaika arvioidaan 0- ja -10 -asteen lämmitystarpeen tuntimäärästä arvioiden. Mukavuuslämmitysjärjestelmiä ei oteta huomioon pää- ja avustavan lisälämmitysjärjestelmän päälläolon arvioinnissa.

Voit lisäksi määrittää jakson keskilämpötilan mikä alapuolella mukavuuslämmitysjärjestelmä on aktiivinen.

{% hint style="info" %}
Mukavuuslämmitysjärjestelmän lämmitystarve arvioidaan 0 ja -10 asteen kytkentätuntien perusteella. Mikäli esimerkiksi 0 asteessa tarve on 4h ja -10 asteessa 8h, lasketaan -5 asteessa päälläolotarpeeksi 6h. Mukavuuslämmitys kytketään päälle periodeittain kiinteistön lämmönvarauskyvyn perusteella.
{% endhint %}

