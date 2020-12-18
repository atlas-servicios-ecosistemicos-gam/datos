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

#### Bosque y bosque ribereño
```shell
cd conectividad\cbima\bosque-bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MA.TIF
```

#### Bosque
```shell
cd conectividad\cbima\bosque
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_MA.TIF
```

#### Bosque ribereño
```shell
cd conectividad\cbima\bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MA.TIF
```

#### Migratorias
```shell
cd conectividad\cbima\migratorias
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MA.TIF
```

#### Otras
```shell
cd conectividad\cbima\otras
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_MA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_MA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_OTRAS_MA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_MA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_MA.TIF
```

### CBIRT

#### Bosque y bosque ribereño
```shell
cd conectividad\cbirt\bosque-bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_TORRES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_TORRES_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_TORRES.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_TORRES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_TORRES.TIF
```

#### Bosque
```shell
cd conectividad\cbirt\bosque
gdalwarp -t_srs EPSG:3857 -of vrt ROBABILIDAD_CONECTIVIDAD_BOSQUE_TORRES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ ROBABILIDAD_CONECTIVIDAD_BOSQUE_TORRES_WEB.TIF
del ROBABILIDAD_CONECTIVIDAD_BOSQUE_TORRES.*
gdalwarp -t_srs EPSG:4326 -of vrt ROBABILIDAD_CONECTIVIDAD_BOSQUE_TORRES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ ROBABILIDAD_CONECTIVIDAD_BOSQUE_TORRES.TIF
```

#### Bosque ribereño
```shell
cd conectividad\cbirt\bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_TORRES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_TORRES_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BRIPARIO_TORRES.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_TORRES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_TORRES.TIF
```

#### Migratorias
```shell
cd conectividad\cbirt\migratorias
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_TORRES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_TORRES_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_TORRES.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_TORRES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_TORRES.TIF
```

#### Otras
```shell
cd conectividad\cbirt\otras
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_TORRES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_TORRES_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_OTRAS_TORRES.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_TORRES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_TORRES.TIF
```

### Curridabat

#### Bosque y bosque ribereño
```shell
cd conectividad\curridabat\bosque-bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CURRIDABAT.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CURRIDABAT_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CURRIDABAT.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CURRIDABAT_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CURRIDABAT.TIF
```

#### Bosque
```shell
cd conectividad\curridabat\bosque
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_CURRIDABAT.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_CURRIDABAT_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_CURRIDABAT.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_CURRIDABAT_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_CURRIDABAT.TIF
```

#### Bosque ribereño
```shell
cd conectividad\curridabat\bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CURRIDABAT.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CURRIDABAT_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CURRIDABAT.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CURRIDABAT_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CURRIDABAT.TIF
```

#### Migratorias
```shell
cd conectividad\curridabat\migratorias
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CURRIDABAT.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CURRIDABAT_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CURRIDABAT.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CURRIDABAT_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CURRIDABAT.TIF
```

#### Otras
```shell
cd conectividad\curridabat\otras
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_CURRIDABAT.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_CURRIDABAT_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_OTRAS_CURRIDABAT.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_CURRIDABAT_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_CURRIDABAT.TIF
```

### La Unión

#### Bosque y bosque ribereño
```shell
cd conectividad\launion\bosque-bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_LA_UNION.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_LA_UNION_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_LA_UNION.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_LA_UNION_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_LA_UNION.TIF
```

#### Bosque
```shell
cd conectividad\launion\bosque
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_LA_UNION.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_LA_UNION_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_LA_UNION.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_LA_UNION_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_LA_UNION.TIF
```

#### Bosque ribereño
```shell
cd conectividad\launion\bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_LA_UNION.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_LA_UNION_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BRIPARIO_LA_UNION.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_LA_UNION_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_LA_UNION.TIF
```

#### Migratorias
```shell
cd conectividad\launion\migratorias
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_LA_UNION.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_LA_UNION_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_LA_UNION.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_LA_UNION_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_LA_UNION.TIF
```

#### Otras
```shell
cd conectividad\launion\otras
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_LA_UNION.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_LA_UNION_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_OTRAS_LA_UNION.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_LA_UNION_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_LA_UNION.TIF
```

### Montes de Oca

#### Bosque y bosque ribereño
```shell
cd conectividad\montesdeoca\bosque-bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MONTES_OCA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MONTES_OCA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MONTES_OCA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MONTES_OCA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_MONTES_OCA.TIF
```

#### Bosque
```shell
cd conectividad\montesdeoca\bosque
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_MONTES_OCA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_MONTES_OCA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_MONTES_OCA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_MONTES_OCA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_MONTES_OCA.TIF
```

#### Bosque ribereño
```shell
cd conectividad\montesdeoca\bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MONTES_OCA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MONTES_OCA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MONTES_OCA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MONTES_OCA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_MONTES_OCA.TIF
```

#### Migratorias
```shell
cd conectividad\montesdeoca\migratorias
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MONTES_OCA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MONTES_OCA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MONTES_OCA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MONTES_OCA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_MONTES_OCA.TIF
```

#### Otras
```shell
cd conectividad\montesdeoca\otras
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_MONTES_OCA.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_MONTES_OCA_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_OTRAS_MONTES_OCA.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_MONTES_OCA_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_MONTES_OCA.TIF
```

### San José

#### Bosque y bosque ribereño
```shell
cd conectividad\sanjose\bosque-bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_SAN_JOSE.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_SAN_JOSE_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_SAN_JOSE.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_SAN_JOSE_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_SAN_JOSE.TIF
```

#### Bosque
```shell
cd conectividad\sanjose\bosque
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_SAN_JOSE.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_SAN_JOSE_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_SAN_JOSE.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_SAN_JOSE_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_SAN_JOSE.TIF
```

#### Bosque ribereño
```shell
cd conectividad\sanjose\bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_SAN_JOSE.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_SAN_JOSE_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BRIPARIO_SAN_JOSE.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_SAN_JOSE_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_SAN_JOSE.TIF
```

#### Migratorias
```shell
cd conectividad\sanjose\migratorias
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_SAN_JOSE.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_SAN_JOSE_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_SAN_JOSE.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_SAN_JOSE_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_SAN_JOSE.TIF
```

#### Otras
```shell
cd conectividad\sanjose\otras
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_SAN_JOSE.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_SAN_JOSE_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_OTRAS_SAN_JOSE.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_SAN_JOSE_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_SAN_JOSE.TIF
```

### Corredores

#### Bosque y bosque ribereño
```shell
cd conectividad\corredores\bosque-bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CORREDORES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CORREDORES_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CORREDORES.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CORREDORES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_CORREDORES.TIF
```

#### Bosque
```shell
cd conectividad\corredores\bosque
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_CORREDORES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_CORREDORES_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_CORREDORES.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_CORREDORES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_CORREDORES.TIF
```

#### Bosque ribereño
```shell
cd conectividad\corredores\bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CORREDORES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CORREDORES_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CORREDORES.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CORREDORES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_CORREDORES.TIF
```

#### Migratorias
```shell
cd conectividad\corredores\migratorias
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CORREDORES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CORREDORES_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CORREDORES.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CORREDORES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_CORREDORES.TIF
```

#### Otras
```shell
cd conectividad\corredores\otras
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_CORREDORES.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_CORREDORES_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_OTRAS_CORREDORES.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_CORREDORES_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_CORREDORES.TIF
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
