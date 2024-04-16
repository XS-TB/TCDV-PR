# TCDV-PR1
Xavier Sancho-Tello Bayarri i Laura Gandia Barlocci

## Descripció arxius del repositori
### source.py
El fitxer source és l'script que conté el codi de Python amb el que s'ha generat el dataset. El codi del fitxer source realitza webscraping del lloc web https://www.wunderground.com/. 
Concretament, genera un arxiu .csv amb una base de dades amb l'evolució dels indicadors metereològics mensuals per a la ciutat de Barcelona entre l'any 2000 i 2024.

### el-prat-de-llobregat_2000_1.csv 
El dataset conté els valors mitjans (average) d’indicadors meteorològics mensuals a l’aeroport del Barcelona (situat al Prat de Llobregat) entre el gener del 2000 i el març del 2024. El dataset conté 291 registres (corresponents als mesos i anys) i 9 camps (corresponents als indicadors meteorològics). Els indicadors que inclou són: temperatura màxima, temperatura mitjana, temperatura mínima, punt de rosada, precipitació, produnfitat de la neu, velocitat del vent, ratxes de vent, i pressió atmosfèrica a nivell del mar.  
L'arxiu .csv utilitza la coma ',' com a delimitador.

### requirements.txt
Conté el nom de totes les llibreries que cal instal·lar per a executar l'script source.py


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
- station: str
- start_date: datetime
- end_date: datetime
- out_directory: str (path)

Es pot cridar a la funció modificant els paràmetres d'entrada per a extreure les dades d'altres estacions meteorològiques durant altres períodes de temps i guardar l'arxiu .csv resultant en un directori propi. Aquesta funció, però, està programada per a executar-se només per a les estacions "station" amb codi 'LEBL', corresponents a l'aeroport de Barcelona. Així, els paràmetres que es poden modificar són la data inicial i final entre les que extreure les dades, i el directori on es guarden.
Si es modifiquen els paràmetres start_date i end_date cal tenir en compte que el dia "day" ha de ser el mateix per start_date i que end_date perquè sinó el bucle no acabarà mai.

Exemples replicables serien:
```
station = 'el-prat-de-llobregat'

#exemple1: dades de l'últim any (de març 2023 a març 2024) en una carpeta amb nom "ultim_any"
start_date_ex1 = datetime(year=2023, month=3, day=1)
end_date_ex1 = datetime(year=2024, month=4, day=1)
out_directory_ex1 = '/content/drive/MyDrive/ultim_any'
scrape_station_weather(station, start_date_ex1, end_date_ex1, out_directory_ex1)

#exemple1: dades entre 2009 i 2011 (al 2010 es van registrar temperatures més baixes) en una carpeta amb nom "2009_2011"
start_date_ex2 = datetime(year=2009, month=1, day=1)
end_date_ex2 = datetime(year=2012, month=1, day=1)
out_directory_ex2 = '/content/drive/2009_2011'
scrape_station_weather(station, start_date_ex1, end_date_ex1, out_directory_ex1)

```
Per a veure quines dades estan disponibles (a nivell d'estació i periodes temporals), consultar: https://www.wunderground.com/history/monthly


## DOI al dataset generat
L’enllaç del DOI del dataset publicat a Zenodo és el següent:
https://doi.org/10.5281/zenodo.10978106
