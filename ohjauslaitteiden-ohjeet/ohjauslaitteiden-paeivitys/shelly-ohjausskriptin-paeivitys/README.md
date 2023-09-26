---
description: Oppaan tekstit ja kuvat koonnut Harri Perämäki
---

# Shelly-ohjausskriptin päivitys

Tämän ohjeen avulla saat Shelly-ohjausskriptin päivitettyä uusimpaan tarjolla olevaan ohjelmaversioon. Päivityksen yhteydessä ohjausasetukset säilyvät palvelimella muuttumattomina, ja Shelly jatkaa ohjausten mukaista toimintaa välittömästi päivityksen jälkeen.

Siirry oppaan ensimmäiselle sivulle tästä:

{% content-ref url="1.-vanhan-skriptin-poistaminen.md" %}
[1.-vanhan-skriptin-poistaminen.md](1.-vanhan-skriptin-poistaminen.md)
{% endcontent-ref %}

#### Pikaohje päivitykseen:

1. Poista Shellyn skriptikirjastosta sekä aiempi ohjausskripti sekä valvontaskripti.
2. Päivitä Shellyn laiteohjelmisto uusimpaan tarjolla olevaan versioon. Shelly käynnistyy uudelleen laiteohjelmiston päivityksen yhteyessä.&#x20;
3. Mikäli Shellyssä on jo käytössä uusin laiteohjelmisto, käynnistä Shelly tässä vaiheessa uudelleen.
4. Päivitä tarvittaessa Shellyn ohjelmakirjaston osoite uuden laiteohjelmiston vaatimaan kirjastoon ([https://raw.githubusercontent.com/Porssari/Shelly-client/main/release/porssari-manifest.json](https://raw.githubusercontent.com/Porssari/Shelly-client/main/release/porssari-manifest.json)).
5. Lataa ja tallenna kirjastosta ensin ohjausskripti ja sen jälkeen valvontaskripti.
6. Käynnistä ja aktivoi molemmat kirjastosta haetut skriptit.
