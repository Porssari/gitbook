# ❓ Miten Pörssäri toimii?

Pörssäri muodostaa kodin sähkölaitteille ohjausaikatauluja käyttäjän asetusten, sähkön hintatietojen sekä tarvittaessa sää- ja aurinkoennusteiden perusteella. Käyttäjä lisää käyttöpaikan, rakennuksen ja laitteen sovelluksessa; laitteen kanaville voidaan luoda ohjaukset automaattisesti.

Laite tai laiteasiakas hakee ohjaustiedon Pörssärin rajapinnasta ja käyttää sitä paikallisesti. Ohjaus voidaan säilyttää laitteessa, joten yksittäinen lyhyt verkkokatko ei välttämättä keskeytä jo haettua aikataulua. Tarkka toiminta riippuu käytettävästä laiteasiakkaasta ja sen asetuksista.

Ulkoisten pilvipalveluiden ohjaus toimii reaaliajassa, eli ohjauslaitteella täytyy olla jatkuva internet-yhteys. Pörssäri varmistaa jokaisen käskyn perillemenon.

Käyttäjä muokkaa asetuksia sovelluksessa. Pörssäri ei muodosta suoraa yhteyttä käyttäjän kotiverkkoon, vaan laite tai laiteasiakas aloittaa yhteyden palveluun. Pörssäri ei tarvitse Shelly Cloud -ominaisuutta, mutta sen käytölle ei ole estettä.

Pörssärin etuna on helppokäyttöinen asetusten muokkaus. Käyttäjän ei tarvitse tehdä muutoksia Pörssärin Shelly-ohjelmakirjaston kautta haettuun valmiiseen ohjelmakoodiin. Lisäksi asetukset ovat tallessa taustapalvelimella, jos ohjausohjelma päivitetään tai ohjauslaite vaihdetaan uuteen.
