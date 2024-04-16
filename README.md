# TCDV-PR1

El codi del fitxer XXX realitza webscraping del lloc web https://www.wunderground.com/. 
Concretament, genera un arxiu .csv amb una base de dades amb l'evolució dels indicadors metereològics mensuals per a la ciutat de Barcelona entre l'any 2000 i 2024.

L'script està pensat per ser executat des de Google Colab. Per a executar l'script és necessari instal·lar les següents biblioteques:

```
!pip install requests
!pip install beautifulsoup4
!pip install selenium
!pip install python-whois
!pip install builtwith
!pip install selenium
!pip install python-dateutil
!apt install chromium-chromedriver
```

Actualment, l'script extreu els valors mitjans (average) mensuals de: temperatura màxima, temperatura mitjana, temperatura mínima, punt de rosada, precipitació, produnfitat de la neu, velocitat del vent, ratxes de vent, i pressió atmosfèrica a nivell del mar.

L'script inclou una funció (scrape_station_weather2) que té com a paràmetres d'entrada
- station
- start date
- end date
- out directory

Es pot cridar a la funció modificant els paràmetres d'entrada per a extreure les dades d'altres estacions meteorològiques durant altres períodes de temps i guardar l'arxiu .csv resultant en un directori propi. Per a veure quines dades estan disponibles (a nivell d'estació i periodes temporals), consultar: https://www.wunderground.com/history/monthly
