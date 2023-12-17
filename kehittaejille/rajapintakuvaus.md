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

# 🖥 Rajapintakuvaus

## Versio 2 (current)

Pörssärin rajapinta on HTTP GET osoitteeseen _https://api.porssari.fi/getcontrols.php_, neljällä pakollisella parametrillä:

* device\_mac: laitteen MAC-osoite isoilla kirjaimilla ja ilman muita merkkejä, esim A1B2C3D4E5F6
* last\_request: edellisen JSON-ohjaustiedon aikaleima (UNIX-timestamp -muodossa, 0 mikäli ohjaustietoa ei ole tallennettu laitteeseen)
* client: käyttäjön skriptin nimi ja versio
* json\_version=2 : käytä API versio 2:ta

Eli esimerkiksi: https://api.porssari.fi/getcontrols.php?device\_mac=A1B2C3D4E5F6\&last\_request=1702815000\&client=documentation-example-1\&json\_version=2

* Mikäli last\_request -parametri on alle tunti nykyhetkestä taaksepäin, palvelin vastaa http-koodilla 304
* Mikäli device\_mac -parametrin mukaista laitetta ei löydy tietokannasta, palvelin vastaa http-koodilla 400
* Mikäli samalla device\_mac -parametrilla kysytään alle 10 sekunnin kuluessa edellisestä kyselystä, palvelin vastaa http-koodilla 425
* Mikäli samalla device\_mac -parametrilla kysytään yli 60 kertaa tunnin kuluessa, palvelin vastaa http-koodilla 429

Muussa tapauksessa palvelin vastaa JSON-objektilla:

```json
{
"metadata": {
    "mac": "A1B2C3D4E5F6",
    "channels": "1",
    "fetch_url": "https://api.porssari.fi/getcontrols.php",
    "timestamp": "1702821684",
    "timestamp_offset": "7200",
    "valid_until": "1702940100"
  },
  "controls": [
    {
      "id": "1",
      "name": "examplename",
      "updated": "1702708849",
      "state": "0",
      "schedules": [
        { "timestamp": "1702850368", "state": "1" },
        { "timestamp": "1702853976", "state": "0" },
        { "timestamp": "1702857522", "state": "1" },
        { "timestamp": "1702875674", "state": "0" },
        { "timestamp": "1702936868", "state": "1" }
      ]
    }
  ]
}
```

##

## Versio 1 (legacy)

Legacy-rajapinta vastaa ohjaustilan tuntitasolla. Mikäli käytössä on ohjaustila mikä annetaan 15min resoluutiolla (esimerkiksi lämmitysohjaus), rajapinta palauttaa tunnin arvoksi kyseisen tunnint ensimmäisen 15 minuutin ajanjakson ohjaustilan.

Lähtökohtaisesti Pörssärin rajapinta on HTTP GET osoitteeseen _https://api.porssari.fi/getcontrols.php_, kolmella pakollisella parametrillä:

* device\_mac: laitteen MAC-osoite isoilla kirjaimilla ja ilman muita merkkejä, esim A1B2C3D4E5F6
* last\_request: edellisen JSON-ohjaustiedon aikaleima (UNIX-timestamp -muodossa, 0 mikäli ohjaustietoa ei ole tallennettuna laitteeseen)
* client: käyttäjön skriptin nimi ja versio

Eli esimerkiksi: https://api.porssari.fi/getcontrols.php?device\_mac=A1B2C3D4E5F6\&last\_request=1702815000\&client=documentation-example-1

* Mikäli last\_request -parametri on alle tunti nykyhetkestä taaksepäin, palvelin vastaa http-koodilla 304
* Mikäli device\_mac -parametrin mukaista laitetta ei löydy tietokannasta, palvelin vastaa http-koodilla 400
* Mikäli samalla device\_mac -parametrilla kysytään alle 10 sekunnin kuluessa edellisestä kyselystä, palvelin vastaa http-koodilla 425
* Mikäli samalla device\_mac -parametrilla kysytään yli 60 kertaa tunnin kuluessa, palvelin vastaa http-koodilla 429

Palvelin vastaa tavallisesti JSON objektilla:

```json
{
    "Metadata": {
        "Mac": "A1B2C3D4E5F6",
        "Channels": "1",
        "Fetch_url": "https://api.porssari.fi/getcontrols.php",
        "Date": "2023-12-16",
        "Time": "21:26:00",
        "Timestamp": "1702754760",
        "Timestamp_offset": "7200",
        "Hours_count": 24,
    },
    "Channel1": {
        "21": "1",
        "22": "1",
        "23": "1",
        "0": "0",
        "1": "1",
        "2": "1",
        "3": "1",
        "4": "1",
        "5": "1",
        "6": "1",
        "7": "0",
        "8": "0",
        "9": "0",
        "10": "0",
        "11": "0",
        "12": "0",
        "13": "0",
        "14": "0",
        "15": "0",
        "16": "0",
        "17": "0",
        "18": "0",
        "19": "0",
        "20": "0",
    },
}
```

Tässä esimerkissä kanavien lukumäärä on yksi.

Kellonajat ovan suomen aikaa paitsi Timestamp joka UTC ja johon voi lisätä Timestamp\_offset että on suomen ajassa.

