# TCDV-PR1
Xavier Sancho-Tello Bayarri i Laura Gandia Barlocci

## Descripció arxius del repositori
### XXX.py
El fitxer XXX és l'script que conté el codi de Python amb el que s'ha generat el dataset. El codi del fitxer XXX realitza webscraping del lloc web https://www.wunderground.com/. 
Concretament, genera un arxiu .csv amb una base de dades amb l'evolució dels indicadors metereològics mensuals per a la ciutat de Barcelona entre l'any 2000 i 2024.

### el-prat-de-llobregat_2000_1.csv 
El dataset conté els valors mitjans (average) d’indicadors meteorològics mensuals a l’aeroport del Barcelona (situat al Prat de Llobregat) entre el gener del 2000 i el març del 2024. El dataset conté 291 registres (corresponents als mesos i anys) i 9 camps (corresponents als indicadors meteorològics). Els indicadors que inclou són: temperatura màxima, temperatura mitjana, temperatura mínima, punt de rosada, precipitació, produnfitat de la neu, velocitat del vent, ratxes de vent, i pressió atmosfèrica a nivell del mar.  
L'arxiu .csv utilitza la coma ',' com a delimitador.

### requirements.txt
Conté el nom de totes les llibreries que cal instal·lar per a executar l'script XXX.py


## Execució de l'script
L'script està pensat per ser executat des de Google Colab. Per a executar l'script és necessari instal·lar les següents llibreries:

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

L'script inclou una funció (scrape_station_weather) que té com a paràmetres d'entrada
- station
- start date
- end date
- out directory

Es pot cridar a la funció modificant els paràmetres d'entrada per a extreure les dades d'altres estacions meteorològiques durant altres períodes de temps i guardar l'arxiu .csv resultant en un directori propi. Per a veure quines dades estan disponibles (a nivell d'estació i periodes temporals), consultar: https://www.wunderground.com/history/monthly
