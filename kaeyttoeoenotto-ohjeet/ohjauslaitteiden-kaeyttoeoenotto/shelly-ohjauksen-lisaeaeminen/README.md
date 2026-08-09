# Shelly-ohjauksen lisääminen

Tämän oppaan avulla lisäät Shellyn Pörssäriin adoptiokoodilla. Yhdistä Shelly ensin kotiverkkoosi valmistajan ohjeen mukaan.

Pörssärissä et tarvitse Shellyn IP-osoitetta tai laitetunnusta manuaalista lomaketta varten. Luo adoptiokoodi ja lisää se Shellyn Pörssäri-skriptiin. Kun Shelly ottaa yhteyden, laite ja sen kanavat löytyvät käyttöpaikallesi.

{% hint style="info" %}
Adoptiokoodi edellyttää Pörssäri-skriptiversiota, jossa Shellyn käyttöliittymässä näkyy kenttä **porssari_adoption_code**. Jos kenttää ei näy, päivitä skripti käyttöympäristöllesi julkaistuun adoptiokoodia tukevaan versioon ennen jatkamista. Älä lisää koodia muokkaamalla skriptin lähdekoodia.
{% endhint %}

Jos käyttöpaikallesi löytyy laite ennen adoptiokoodin luontia, voit valita **Laitteet → Lisää laite → Tälle käyttöpaikalle löydetyt laitteet**, nimetä laitteen ja viimeistellä lisäyksen. Tämä on vaihtoehtoinen polku; adoptiokoodi on ensisijainen tapa.

Kun laite on adoptoitu, Pörssäri luo sen rekisteröidyille kanaville ohjaukset automaattisesti.

{% content-ref url="laitteen-lisaeaeminen-poerssaeri-sivustolle/" %}
[laitteen-lisaeaeminen-poerssaeri-sivustolle](laitteen-lisaeaeminen-poerssaeri-sivustolle/)
{% endcontent-ref %}

{% content-ref url="ohjausskriptin-lisaeaeminen-shelly-laitteeseen/" %}
[ohjausskriptin-lisaeaeminen-shelly-laitteeseen](ohjausskriptin-lisaeaeminen-shelly-laitteeseen/)
{% endcontent-ref %}
