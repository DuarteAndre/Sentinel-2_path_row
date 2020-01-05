# Sentinel-2 Tiles
### Convertion kml Sentinel-2 tiles
For Level-1C and Level-2A, the granules, also called tiles, are 100x100 km2 ortho-images in UTM/WGS84 projection.
- Download kml tiles: https://sentinel.esa.int/web/sentinel/missions/sentinel-2/data-products

### Convertion kml file to shapefile
```
ogr2ogr -f "ESRI Shapefile" -skipfailures -nlt polygon S2Atiles S2A_OPER_GIP_TILPAR_MPC__20151209T095117_V20150622T000000_21000101T000000_B00.kml
```
Features renamed to S2Atiles
```
ogr2ogr -f "ESRI Shapefile" -skipfailures -nlt polygon -nln S2Atiles S2Atiles S2A_OPER_GIP_TILPAR_MPC__20151209T095117_V20150622T000000_21000101T000000_B00.kml
```
### References
- https://forum.step.esa.int/t/convert-and-subset-kml-file-of-tiles/1691
- https://sentinel.esa.int/web/sentinel/missions/sentinel-2/data-products
