# Datos

### Registros de presencia de Mammalia, Amphibia, Reptilia, Aves, Plantae
La consulta al portal de GBIF se encuentra en la dirección:  
[https://www.gbif.org/occurrence/download/0002762-200127171203522](https://www.gbif.org/occurrence/download/0002762-200127171203522)

Para procesarlo en los comandos que se presentan seguidamente, el archivo CSV producto de la consulta se renombró como **mammalia-amphibia-reptilia-aves-plantae.csv**.

El archivo anterior se separó de la siguiente forma:

#### Registros de presencia de Mammalia
```terminal
ogr2ogr -f GeoJSON mammalia.geojson occurrences.csv -select "kingdom, scientificName" -where "class='Mammalia'" -oo X_POSSIBLE_NAMES=decimalLongitude -oo Y_POSSIBLE_NAMES=decimalLatitude
```
El archivo está almacenado en
