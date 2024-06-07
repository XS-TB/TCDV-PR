# TCDV-PR2
Xavier Sancho-Tello Bayarri i Laura Gandia Barlocci

## Descripció arxius del repositori
### SourcePR2.py
El fitxer source és l'script que conté el codi de Python amb el que s'ha realitzat la pràctica, on està fet l'analisi i on dins podem veure una explicació més detallada del treball.

### el-prat-de-llobregat_2000_1.csv 
El dataset conté els valors mitjans (average) d’indicadors meteorològics mensuals a l’aeroport del Barcelona (situat al Prat de Llobregat) entre el gener del 2000 i el març del 2024. 
El dataset conté 291 registres (corresponents als mesos i anys) i 9 camps (corresponents als indicadors meteorològics). Els indicadors que inclou són: temperatura màxima, temperatura mitjana, 
temperatura mínima, punt de rosada, precipitació, produnfitat de la neu, velocitat del vent, ratxes de vent, i pressió atmosfèrica a nivell del mar.  
L'arxiu .csv utilitza la coma ',' com a delimitador.

Aquets fitxer es el resultat de la primera pràctica i el que hem modificat per treballar en aquesta segona.

### df.csv
Aquest dataset es la barreja del dataset anterior després d'haver-lo mergeat amb un del nombre de passatgers que van arribar a l'aeroport del prat de llobregat mes a mes. 
Aquest conjunt de dades ha passat per un preprocessament on hem crear noves variables, hem tractat els valors nuls i on hem ajustat els nombres extrems entre altres mesures.

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
