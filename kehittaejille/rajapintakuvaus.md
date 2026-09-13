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

## Nykyinen laitepollaus (`json_version=3`)

Laitteet hakevat ohjaustiedot allekirjoitetulla HTTP GET -kyselyllä:

`GET https://api.porssari.fi/api/v1/controls-legacy`

Pakollinen tunnisteparametri:

* `device_mac` — laitteen tunniste isoilla kirjaimilla ilman erotinmerkkejä, esimerkiksi `A1B2C3D4E5F6` (12 merkkiä Shellylle; ei mallinimeä edessä)

Laitteen todiste (device proof):

* `timestamp` — HMAC-todisteen aikaleima
* `nonce` — 16–64 merkin nonce
* `signature` — 64 merkin hex-HMAC-allekirjoitus

Muita tärkeitä parametreja:

* `last_request` — edellisen onnistuneen vastauksen Unix-aikaleima (`0` jos ei vielä tallennettu)
* `json_version=3` — ainoa tuettu JSON-versio tällä endpointilla
* `prices` — sisällytä hintatiedot, jos tilillä on oikeus
* `schedule_full_day` — käytä koko paikallisen vuorokauden ohjausikkunaa
* `json_channel_names` — sisällytä kanavien nimet
* `cut_schedule` — rajaa aikataulun pituutta
* `script_version`, `client_fw`, `client_model` — asiakkaan metatiedot
* `schedule_reason` — sisällytä aikataulun syy tarvittaessa
* `headers` — status-only -polku

Esimerkki (fiktiivinen, ilman kelvollista allekirjoitusta):

`https://api.porssari.fi/api/v1/controls-legacy?device_mac=A1B2C3D4E5F6&last_request=0&json_version=3&timestamp=...&nonce=...&signature=...`

### Vastauskoodit

* **200** — ohjausdata (tai tyhjä body, jos `headers=true`)
* **204** — laite löytyy, mutta valitussa ikkunassa ei ole ohjausrivejä
* **304** — laitteella on jo riittävän tuore vastaus
* **401** — todiste puuttuu
* **403** — todiste virheellinen, vanhentunut, uudelleenkäytetty tai väärälle laitteelle
* **404** — tuntematon laite
* **422** — virheelliset parametrit
* **425** — kyselyväli liian lyhyt
* **429** — tuntikohtainen kyselyraja ylitetty
* **503** — rate limiter / replay-suoja ei käytettävissä (tuotannossa fail-closed)

Onnistunut JSON-vastaus palautetaan juurena ilman erillistä success-envelopea. Esimerkkirakenne (yksinkertaistettu):

```json
{
  "metadata": {
    "mac": "A1B2C3D4E5F6",
    "channels": [0],
    "fetch_url": "https://api.porssari.fi/api/v1/controls-legacy",
    "timestamp": 1702821684,
    "valid_until": 1702940100,
    "json_version": 3
  },
  "controls": [
    {
      "id": 1,
      "name": "example",
      "state": 0,
      "schedules": [
        { "timestamp": 1702850368, "state": 1 },
        { "timestamp": 1702853976, "state": 0 }
      ]
    }
  ]
}
```

Älä julkaise käyttökelpoisia heartbeat-salaisuuksia tai allekirjoitettuja pyyntöjä.

## Vanha PHP-rajapinta (legacy)

Vanha `https://api.porssari.fi/getcontrols.php` -kuvaus on korvattu yllä olevalla FastAPI-sopimuksella. Uudet integraatiot tulee tehdä `GET /api/v1/controls-legacy` -rajapintaan `json_version=3` -muodossa.
