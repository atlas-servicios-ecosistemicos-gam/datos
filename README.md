# Datos

## Biodiversidad

### Registros de presencia de especies

#### Mammalia, Amphibia, Reptilia, Aves y Plantae
Para obtener los registros de presencia en la GAM de estos grupos biológicos, se realizó una consulta al portal de GBIF, la cual se encuentra en la dirección:  
[https://www.gbif.org/occurrence/download/0002762-200127171203522](https://www.gbif.org/occurrence/download/0002762-200127171203522)

El archivo resultante se separó en otros cinco archivos GeoJSON, correspondientes a cada uno de los grupos (Mammalia, Amphibia, Reptilia, Aves y Plantae).

Seguidamente se presentan los comandos utilizados para generar los cinco archivos y la ubicación en donde está almacenado cada uno. En los comandos, el archivo renombrado como _mammalia-amphibia-reptilia-aves-plantae.csv_ corresponde al que se descargó de GBIF.

#### Registros de presencia de Mammalia
```terminal
ogr2ogr -f GeoJSON mammalia.geojson mammalia-amphibia-reptilia-aves-plantae.csv -select "kingdom, scientificName" -where "class='Mammalia'" -oo X_POSSIBLE_NAMES=decimalLongitude -oo Y_POSSIBLE_NAMES=decimalLatitude
```
Archivo para visualizar:  
[https://github.com/atlas-servicios-ecosistemicos-gam/datos/blob/master/biodiversidad/presencia/mammalia.geojson](https://github.com/atlas-servicios-ecosistemicos-gam/datos/blob/master/biodiversidad/presencia/mammalia.geojson)
[https://raw.githubusercontent.com/atlas-servicios-ecosistemicos-gam/datos/master/biodiversidad/presencia/mammalia.geojson](https://raw.githubusercontent.com/atlas-servicios-ecosistemicos-gam/datos/master/biodiversidad/presencia/mammalia.geojson)
