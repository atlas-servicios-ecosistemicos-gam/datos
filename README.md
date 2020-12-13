# Datos
Todos los comandos de esta sección asumen que en cada directorio está copiado el archivo en CR05/CRTM05 (EPSG:5367) disponible en el repositorio datos-fuentes-originales.

Los comandos GDAL realizan las conversiones a Web Mercator (EPSG:3857) y WGS84 (EPSG:4326).
## Infraestructura verde
### CBIMA
```shell
cd infraestructura-verde\cbima
gdalwarp -t_srs EPSG:3857 -of vrt IV_CBI_RIO_MARIA_AGUILAR.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CBI_RIO_MARIA_AGUILAR_WEB.TIF
del IV_CBI_RIO_MARIA_AGUILAR.*
gdalwarp -t_srs EPSG:4326 -of vrt IV_CBI_RIO_MARIA_AGUILAR_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CBI_RIO_MARIA_AGUILAR.TIF
```

### CBIRT
```shell
cd infraestructura-verde\cbirt
gdalwarp -t_srs EPSG:3857 -of vrt IV_CBI_RIO_TORRES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CBI_RIO_TORRES_WEB.TIF
del IV_CBI_RIO_TORRES.*
gdalwarp -t_srs EPSG:4326 -of vrt IV_CBI_RIO_TORRES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CBI_RIO_TORRES.TIF
```

### Curridabat
```shell
cd infraestructura-verde\curridabat
gdalwarp -t_srs EPSG:3857 -of vrt IV_CURRIDABAT.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CURRIDABAT_WEB.TIF
del IV_CURRIDABAT.*
gdalwarp -t_srs EPSG:4326 -of vrt IV_CURRIDABAT_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CURRIDABAT.TIF
```

### La Unión
```shell
cd infraestructura-verde\launion
gdalwarp -t_srs EPSG:3857 -of vrt IV_LA_UNION.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_LA_UNION_WEB.TIF
del IV_LA_UNION.*
gdalwarp -t_srs EPSG:4326 -of vrt IV_LA_UNION_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_LA_UNION.TIF
```

### Montes de Oca
```shell
cd infraestructura-verde\montesdeoca
gdalwarp -t_srs EPSG:3857 -of vrt IV_MONTES_DE_OCA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_MONTES_DE_OCA_WEB.TIF
del IV_MONTES_DE_OCA.*
gdalwarp -t_srs EPSG:4326 -of vrt IV_MONTES_DE_OCA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_MONTES_DE_OCA.TIF
```

### San José
```shell
cd infraestructura-verde\sanjose
gdalwarp -t_srs EPSG:3857 -of vrt IV_SAN_JOSE.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_SAN_JOSE_WEB.TIF
del IV_SAN_JOSE.*
gdalwarp -t_srs EPSG:4326 -of vrt IV_SAN_JOSE_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_SAN_JOSE.TIF
```

### Corredores-cantones
```shell
cd infraestructura-verde\corredores-cantones
gdalwarp -t_srs EPSG:3857 -of vrt IV_CORREDORES_CANTONES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CORREDORES_CANTONES_WEB.TIF
del IV_CORREDORES_CANTONES.*
gdalwarp -t_srs EPSG:4326 -of vrt IV_CORREDORES_CANTONES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CORREDORES_CANTONES.TIF
```

### Corredores
```shell
cd infraestructura-verde\corredores
gdalwarp -t_srs EPSG:3857 -of vrt IV_CORREDORES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CORREDORES_WEB.TIF
del IV_CORREDORES.*
gdalwarp -t_srs EPSG:4326 -of vrt IV_CORREDORES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ IV_CORREDORES.TIF
```

## Conectividad
### CBIMA
#### Bosque
```shell
cd conectividad\cbima\bosque
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA.TIF
```

## Biodiversidad

### Registros de presencia de especies

#### Mammalia, Amphibia, Reptilia, Aves y Plantae
Para obtener los registros de presencia en la GAM de estos grupos biológicos, se realizó una consulta al portal de GBIF, la cual se encuentra en la dirección:  
[https://www.gbif.org/occurrence/download/0002762-200127171203522](https://www.gbif.org/occurrence/download/0002762-200127171203522)

El archivo resultante se separó en otros cinco archivos GeoJSON, correspondientes a cada uno de los grupos (Mammalia, Amphibia, Reptilia, Aves y Plantae).

Seguidamente se presentan los comandos utilizados para generar los cinco archivos y la ubicación en donde está almacenado cada uno. En los comandos, el archivo renombrado como _mammalia-amphibia-reptilia-aves-plantae.csv_ corresponde al que se descargó de GBIF.

#### Registros de presencia de Mammalia
```terminal
ogr2ogr -f GeoJSON mammalia.geojson mammalia-amphibia-reptilia-aves-plantae.csv -select "order, family, genus, species, year" -where "class='Mammalia' AND taxonRank='species'" -oo X_POSSIBLE_NAMES=decimalLongitude -oo Y_POSSIBLE_NAMES=decimalLatitude
```
Visualización:  
[https://github.com/atlas-servicios-ecosistemicos-gam/datos/blob/master/biodiversidad/presencia/mammalia.geojson](https://github.com/atlas-servicios-ecosistemicos-gam/datos/blob/master/biodiversidad/presencia/mammalia.geojson)

Datos:  
[https://raw.githubusercontent.com/atlas-servicios-ecosistemicos-gam/datos/master/biodiversidad/presencia/mammalia.geojson](https://raw.githubusercontent.com/atlas-servicios-ecosistemicos-gam/datos/master/biodiversidad/presencia/mammalia.geojson)
