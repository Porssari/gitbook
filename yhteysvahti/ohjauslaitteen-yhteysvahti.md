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

# ✅ Ohjauslaitteen yhteysvahti

Pörssäri-sivustolla on mahdollista ottaa käyttöön yhteysvahti, mikä ilmoittaa käyttäjälle mikäli ohjauslaite ei ole yhteydessä palvelimelle käyttäjän määrittelemän ajan sisällä. Normaalitilanteessa laite on yhteydessä palvelimelle noin kahden minuutin välein.

Ohjauslaitetta ole välttämätöntä uudelleenkäynnistää heti yhteyskatkoilmoituksen saatuaan mikäli on todennettavissa, että ongelma on laitteen verkkoyhteydessä. Ohjaustieto tallennetaan paikallisesti yleensä niin pitkälle kun hintatietoa on NordPoolista saatavilla, ja Pörssärin laiteohjelma uudelleenkäynnistää laitteen automaattisesti kun ohjaustietoa tulevaisuuteen ei ole enää paikallisesti tallennettuna.&#x20;

Oletusasetus yhteysvahdin reagointiin on 30 minuuttia, mutta se on käyttäjän toimesta muutettavissa välille 5-120 minuuttia.

[telegram-yhteysvahdin-kaeyttoeoenotto](telegram-yhteysvahdin-kaeyttoeoenotto/ "mention")
