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

# 🖥️ Rajapintakuvaus

## Ohjauslaitteen kyselyrajapinta

Nykyisten laiteasiakkaiden yhteensopivuusrajapinta on:

```http
GET /api/v1/controls-legacy
```

Nimestään huolimatta `controls-legacy` on nykyisten laiteskriptien käytössä oleva yhteensopivuuspinta. Se ei käytä käyttäjän Bearer-tunnusta eikä vanhaa `getcontrols.php`-reittiä. Käytä aina `json_version=3`.

### Kyselyparametrit

| Parametri | Pakollinen | Kuvaus |
| --- | --- | --- |
| `device_mac` | kyllä | Laitetunniste; palvelu normalisoi arvon isoiksi kirjaimiksi. |
| `timestamp` | kyllä | Laitetodisteen Unix-aikaleima. |
| `nonce` | kyllä | Kertakäyttöinen 16–64 merkin satunnaisarvo. |
| `signature` | kyllä | Pienillä heksamerkeillä esitetty HMAC-SHA256-todiste. |
| `json_version` | ei | Oletus on `3`. Lähetä arvo `3` eksplisiittisesti; muut arvot hylätään. |
| `last_request` | ei | Edellisen saadun ohjaustiedon Unix-aikaleima; oletus on `0`. |
| `prices` | ei | Pyytää hintatietoja, jos käyttöoikeus sallii ne. |
| `schedule_full_day` | ei | Käyttää koko paikallisen kalenteripäivän ohjausikkunaa. |
| `cut_schedule` | ei | Rajaa palautettavien tulevien tilanvaihtojen enimmäismäärän (1–256). |
| `json_channel_names` | ei | Sisällyttää kanavien nimet, kun ne ovat saatavilla. |
| `timestamp_format` | ei | `unix` (oletus) tai `iso`. |
| `headers` | ei | Palauttaa onnistuneessa status-only-kyselyssä tyhjän rungon. |
| `script_version`, `client_fw`, `client_model` | ei | Asiakkaan versio- ja mallimetatiedot. |

### Allekirjoitettu laitetodiste

Laite saa käyttöönotossa laitekohtaisen salaisuuden. Salaisuutta ei saa lähettää pyynnössä, kirjata lokiin tai julkaista. Jokaiselle kyselylle luodaan uusi aikaleima ja nonce.

Palvelu muodostaa kanonisen kyselymerkkijonon kaikista query-parametreista paitsi `signature`-parametrista. Avain–arvo-parit URL-koodataan RFC 3986 -tyyliin, `device_mac` korvataan normalisoidulla arvolla ja parit järjestetään avaimen sekä arvon mukaan. HMAC-SHA256:n syöte on UTF-8-muodossa seuraavat seitsemän riviä:

```text
GET
/api/v1/controls-legacy
<kanoninen-kysely-ilman-signaturea>
<normalisoitu-device_mac>
<timestamp>
<nonce>
<SHA-256-tyhjästä-pyynnön-rungosta>
```

Allekirjoitus on tämän syötteen HMAC-SHA256 laitteen salaisuudella, esitettynä 64-merkkisenä pienaakkosisena heksamerkkijonona. Aikaleiman pitää olla palveluympäristön sallitun aikapoikkeaman sisällä; oletusraja on viisi minuuttia. Nonce hyväksytään vain kerran, joten samaa allekirjoitettua pyyntöä ei voi toistaa.

Älä käytä toimivaa salaisuutta tai allekirjoitusta dokumentaatioesimerkissä. Asiakas toteuttaa kanonisoinnin ennen allekirjoituksen laskemista; parametreja ei saa muuttaa sen jälkeen.

### Vastaus

Onnistunut `200`-vastaus on suoraan JSON-objekti (ei yleistä response-envelopea):

```json
{
  "metadata": {
    "mac": "ESIMERKKILAITE",
    "channels": [1],
    "fetch_url": "https://example.invalid/api/v1/controls-legacy",
    "timestamp": 1735689600,
    "valid_until": 1735776000,
    "json_version": 3
  },
  "ch_data": [
    {"id": "1", "name": "Lämminvesivaraaja", "updated": 1735689500, "state": "0", "failsafe": []}
  ],
  "controls": [[1735693200, 1, 1], [1735696800, 1, 0]]
}
```

`controls` sisältää rivejä muodossa `[aikaleima, kanava, tila]`. Kun `prices=true` on sallittu ja hintatietoa on saatavana, vastaus voi sisältää lisäksi `prices`-objektin.

### Tila- ja virhekoodit

| Tila | Merkitys |
| --- | --- |
| `200` | Ohjaustiedot palautettiin. `headers=true` voi palauttaa tyhjän rungon. |
| `204` | Laitteelle ei ole ohjausrivejä valitussa ikkunassa. |
| `304` | Laitteella on jo riittävän tuore ohjaustieto `last_request`-arvon perusteella. |
| `401` | Laitetodiste puuttuu. |
| `403` | Laite tai todistus on virheellinen, vanhentunut tai nonce on käytetty aiemmin. |
| `422` | Parametrien muoto tai arvo on virheellinen, esimerkiksi muu JSON-versio kuin 3. |
| `425` | Kyselyväli on liian lyhyt. |
| `429` | Kyselymäärä on ylittänyt rajan; vastaus voi sisältää `Retry-After`-otsakkeen. |
| `503` | Todisteen toistonesto tai nopeusrajoitus ei ole käytettävissä. |

Käsittele `304` ja `204` normaalina tilana, säilytä edellinen kelvollinen ohjaus turvallisesti ja noudata `Retry-After`-otsaketta. Rajapinta on tarkoitettu laiteasiakkaille, ei yleiseksi hintadata- tai käyttäjärajapinnaksi.
