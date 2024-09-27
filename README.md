# Liikenne ja Juna-aikataulut Tampereelle

Tämä projekti koostuu kahdesta verkkosivusta, jotka näyttävät reaaliaikaista tietoa Tampereelle johtavien teiden liikennekameroista sekä Helsingistä Tampereelle suuntautuvien junien aikatauluista.

## Sisältö

- **index.html**: Sivuston pääsivu, josta pääsee navigoimaan liikennekamerat- ja junasivuille.
- **liikennekamera.html**: Näyttää reaaliaikaisen kuvan Tampereelle johtavien teiden viidestä liikennekamerasta sekä kuvien aikaleimat.
- **junat.html**: Näyttää ajankohtaiset junien aikataulut Helsingistä Tampereelle.

### 1. **Index-sivu (index.html)**
   - Tervetulosivu, joka sisältää lyhyen kuvauksen sivuston sisällöstä.
   - Sisältää navigointipainikkeet, joilla voi siirtyä liikennekamera- ja junasivuille.

### 2. **Liikennekamerat-sivu (liikennekamera.html)**
   - Näyttää reaaliaikaiset kuvat viidestä Tampereelle johtavasta tieliikennekamerasta.
   - Jokaisen kameran kuvien yhteydessä näytetään myös mitattu aikaleima, joka haetaan Digitrafficin rajapinnasta.
   - Seuraavat kamerakuvat näytetään:
     - [C0450701](https://weathercam.digitraffic.fi/C0450701.jpg)
     - [C0450702](https://weathercam.digitraffic.fi/C0450702.jpg)
     - [C0450703](https://weathercam.digitraffic.fi/C0450703.jpg)
     - [C0450704](https://weathercam.digitraffic.fi/C0450704.jpg)
     - [C0450709](https://weathercam.digitraffic.fi/C0450709.jpg)
   - Sisältää napin, jolla voi palata takaisin pääsivulle.

### 3. **Junat-sivu (junat.html)**
   - Näyttää ajankohtaiset junien aikataulut Helsingistä Tampereelle.
   - Tiedot haetaan Digitrafficin avoimesta API-rajapinnasta, ja ne sisältävät junan numeron, tyypin, lähtöajan Helsingistä sekä saapumisajan Tampereelle.
   - Sisältää napin, jolla voi palata takaisin pääsivulle.

## Käyttöohjeet

1. Avaa `index.html` tiedosto selaimessasi.
2. Valitse navigointipainikkeista, haluatko nähdä liikennekamerakuvia vai junien aikataulut.
3. Palaa pääsivulle käyttämällä "Takaisin"-painiketta.

## Teknologiat

- **HTML5**: Sivurakenteen luomiseen.
- **CSS**: Sivujen ulkoasun ja tyylin määrittelyyn.
- **JavaScript**: Tietojen hakemiseen Digitrafficin API-rajapinnasta sekä liikennekamerakuvien ja aikaleimojen dynaamiseen näyttämiseen.

## API

### Digitraffic API

- **Liikennekamerat**: Liikennekamerakuvat (5 kpl) haetaan suoraan Digitrafficin kelikamera-URL:eista:
  - [C0450701](https://weathercam.digitraffic.fi/C0450701.jpg)
  - [C0450702](https://weathercam.digitraffic.fi/C0450702.jpg)
  - [C0450703](https://weathercam.digitraffic.fi/C0450703.jpg)
  - [C0450704](https://weathercam.digitraffic.fi/C0450704.jpg)
  - [C0450709](https://weathercam.digitraffic.fi/C0450709.jpg)
  
  - Kamerakuvien aikaleimat ja muut tiedot haetaan API-datasta, joka löytyy osoitteesta:
    [https://tie.digitraffic.fi/api/weathercam/v1/stations](https://tie.digitraffic.fi/api/weathercam/v1/stations)
  
- **Junatiedot**: Junien aikataulutiedot haetaan käyttämällä Digitrafficin [junaliikenteen API:a](https://rata.digitraffic.fi/api/v1/live-trains/station/HKI?departing_trains=100&include_nonstopping=false).
