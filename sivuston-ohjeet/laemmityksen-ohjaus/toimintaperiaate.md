# Toimintaperiaate

Pörssäri arvioi käyttöpaikan päivittäisen lämmitystarpeen rakennuksen vuosikulutuksen sekä yr.no-rajapinnasta haetun ulkolämpötilaennusteen perusteella. Koska lämmitys arvioidaan koko käyttöpaikalle, lisää järjestelmään myös käytössä olevat lämmitysjärjestelmät, joita Pörssäri ei ohjaa. Arvioi lisäksi rakennuksen energiantarve mahdollisimman oikein.

{% hint style="info" %}
Mikäli talossa on käytössä lämpöpumppu, ei sähkönkulutus vastaa talon lämmitysenergian tarvetta. Motivan sivuilta löytyy laskuri talon lämmitystarpeen arvioon neliömäärän, huonekorkeuden, henkilömäärän sekä rakennuksen sijainnin perusteella.

[https://lammitysvertailu.eneuvonta.fi](https://lammitysvertailu.eneuvonta.fi) (Kohta 1. Rakennuksen tiedot)
{% endhint %}

### Lämmitystarpeen hienosäätö

Jos ohjatut lämmitysjärjestelmät lämmittävät tasaisesti liikaa tai liian vähän, voit hienosäätää lämmitystarvetta valinnalla **Rakennuksen lämmitystarpeen hienosäätö**. Jos rakennus lämpenee tai viilenee liikaa ulkolämpötilan laskiessa mutta asetus toimii noin nollan asteen säässä oikein, hienosäädä muutosta valinnalla **Lämmitystarpeen muutoksen hienosäätö**.

### Erilaiset lämmitysjärjestelmät

Käyttöpaikalle voi lisätä kolmenlaisia lämmitysjärjestelmiä: **Päälämmitysjärjestelmä**, **Avustava lisälämmitysjärjestelmä** ja **Mukavuuslämmitysjärjestelmä**.

#### Päälämmitysjärjestelmä (lasketaan lämmitystarpeen perusteella)

Käyttöpaikan päälämmitysjärjestelmäksi lisätään laite tai laitteet, joiden halutaan tuottavan pääosa lämmöstä. Tällainen järjestelmä voi olla esimerkiksi vesikiertoisen lämmityksen lämmönlähde, ilmalämpöpumppu tai suorassa sähkölämmityksessä kukin lämmityspiiri tai seinäpatteri joko erikseen tai yhteen laskettuna.

{% hint style="info" %}
Mikäli talossa on vain yksi lämmitysjärjestelmä (seinäpatterit, lämpöpumppu vesikiertoisella lämmönjaolla, sähköinen lattialämmitys), sinun tarvitsee lisätä ainoastaan päälämmitysjärjestelmä. Voit lisätä jokaisen lämmityselementin joko omana yksikkönä tai vaihtoehtoisesti laskea niiden tehon yhteen, ja lisätä kaikki laitteet yhtenä järjestelmänä.
{% endhint %}

#### Avustava lisälämmitysjärjestelmä (lasketaan lämmitystarpeen perusteella)

Jos käyttöpaikan päälämmityslähteenä on esimerkiksi ilmalämpöpumppu, muut lämmitysjärjestelmät, kuten sähköpatterit tai sähköinen lattialämmitys, voidaan lisätä avustavina lisälämmitysjärjestelminä.

Voit määrittää avustavalle lisälämmitysjärjestelmälle vähimmäisosuuden lämmitystarpeesta. Tätä voi käyttää esimerkiksi silloin, kun lattialämmityksen halutaan olevan hieman päällä, vaikka ilmalämpöpumppu tuottaa pääosan lämmöstä.

Jos vähimmäisosuutta ei määritetä, avustava lämmitys kytketään päälle vain silloin, kun päälämmitysjärjestelmän teho ei riitä täyttämään lämmitysjakson tarvetta. Lisälämmitys ajoitetaan jakson edullisimpiin tunteihin.

{% hint style="info" %}
Mikäli et ohjaa päälämmönlähteenä olevaa lämpöpumppua Pörssärillä, mutta haluat silti automaattisen ohjauksen lisälämmönlähteisiin, tulee lämpöpumppu kuitenkin lisätä päälämmitysjärjestelmäksi oikean lämmitysmäärän arvioimista varten.
{% endhint %}

#### Mukavuuslämmitysjärjestelmä (ei vaikuta käyttöpaikan lämmitystarpeen arviointiin)

Jos haluat määrittää itse lämmityksen päälläolotunnit eri lämpötilapisteissä, lisää lämmityslaite mukavuuslämmitysjärjestelmänä. Tällöin vuorokauden tarvittava lämmitystuntimäärä arvioidaan lämpötilapisteiden tuntimääristä ennustetun keskilämpötilan perusteella.

Lisää lämmitysjärjestelmän asetuksiin vähintään kaksi lämpötilapistettä. Mukavuuslämmitysjärjestelmiä ei oteta huomioon pää- ja avustavan lisälämmitysjärjestelmän päälläolon arvioinnissa.

Voit lisäksi määrittää jakson keskilämpötilan mikä alapuolella mukavuuslämmitysjärjestelmä on aktiivinen.

{% hint style="info" %}
Mukavuuslämmitysjärjestelmän lämmitystarve arvioidaan annettujen pisteiden vuorokauden kytkentätuntien perusteella. Mikäli esimerkiksi 0 asteessa tarve on 4h ja -10 asteessa 8h, lasketaan -5 asteessa päälläolotarpeeksi 6h. Voit valita järjestelmän asetuksissa kuinka monen tunnin jaksoihin päälläolotunnit jaetaan, tuolloin vuorokausitarpeen mukainen lämmitysmäärä jaetaan tasan kyseisiin aikaperiodeihin.
{% endhint %}
