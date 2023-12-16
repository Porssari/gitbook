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

# Rajapintakuvaus

Lähtökohtaisesti Pörssärin rajapinta on HTTP GET osoitteeseen *https://api.porssari.fi/getcontrols.php*, kahdella parametrillä:

* device_mac: laitteen MAC-osoite isoilla kirjaimilla ja ilman muita merkkejä, esim A1B2C3D4E5F6
* client: käyttäjön skriptin nimi ja versio

Eli esimerkiksi: https://api.porssari.fi/getcontrols.php?device_mac=A1B2C3D4E5F6&client=documentation-example-1

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

Kellonajat ovan suomen aikaa paitsi Timestamp joka UTC ja johon voi lisätä Timestamp_offset että on suomen ajassa.
