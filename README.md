# Liikenne ja Juna-aikataulut Tampereelle

Kaksi verkkosivua, jotka näyttävät reaaliaikaista tietoa Tampereelle johtavien teiden liikennekameroista sekä Helsingistä Tampereelle suuntautuvien junien aikatauluista.

## Sisältö

- **index.html**: Sivusto pääsivu, josta pääsee navigoimaan liikennekamerat- ja junasivuille.
- **liikennekamera.html**: Näyttää reaaliaikaisen kuvan Tampereelle johtavasta tieliikennekamerasta.
- **junat.html**: Näyttää ajankohtaiset junien aikataulut Helsingistä Tampereelle.

1. **Index-sivu (index.html)**:
   - Tervetuloa-sivu, joka sisältää lyhyen kuvauksen sivuston sisällöstä.
   - Sisältää navigointipainikkeet, joista pääsee liikennekamerat- ja junasivuille.

2. **Liikennekamerat-sivu (liikennekamera.html)**:
   - Näyttää reaaliaikaisen kuvan tieliikennekamerasta (C0450701), joka seuraa tilannetta Tampereelle johtavalla tiellä.
   - Sisältää napin, jolla voi palata takaisin pääsivulle.

3. **Junat-sivu (junat.html)**:
   - Näyttää junien aikataulut Helsingistä Tampereelle. Tiedot haetaan Digitrafficin avoimesta API-rajapinnasta.
   - Näyttää junan numeron, tyypin, lähtöajan Helsingistä sekä saapumisajan Tampereelle.
   - Sisältää napin, jolla voi palata takaisin pääsivulle.

## Käyttöohjeet

1. Avaa `index.html` tiedosto selaimessasi.
2. Käytä navigointipainikkeita päästäksesi liikenne- ja junasivuille.

## Teknologiat

- **HTML5**: Käytetty sivujen rakenteen luomiseen.
- **CSS**: Käytetty sivujen ulkoasun ja tyylin määrittelyyn.
- **JavaScript**: Käytetty junien aikataulutietojen hakemiseen Digitrafficin API-rajapinnasta.

## API

### Digitraffic API

- **Liikennekamerat**: Kelikameroiden kuvat haetaan suoraan URL-osoitteesta `https://weathercam.digitraffic.fi/C0450701.jpg`.
- **Junatiedot**: Junien aikataulutiedot haetaan käyttämällä Digitrafficin API:a osoitteesta `https://rata.digitraffic.fi/api/v1/live-trains/station/HKI?departing_trains=100&include_nonstopping=false`.
