# libgsidem2el

 - get elevation in GSI-Dem tile layer 
 - in japanese : http://computational-sediment-hyd.hatenablog.jp/entry/2018/12/26/214934

## Usage

### import module

```python
import libgsidem2el as gsi
``` 

### constructor

 - It's possible to select one of DEM5A, DEM5B, DEM10B and DEMGM
 - see https://maps.gsi.go.jp/help/pdf/demapi.pdf

```python
dem = gsi.libgsidem2el('DEM5A')
``` 

### get elevation data

 - arguments of function getEL is longitude, latitude and zoom level
 - zoom level is DEM5A,B:15, DEM10B:0-14, DEMGM:0-8

```python
el = dem.getEL(lon, lat, zoom = 15)
``` 

 - it's possible to get rapidly data in the same tile layer as the last time, because this object holds tile layer data until destructor runs.

## Licence

[MIT](/LICENCE)

## Author

[computational-sediment-hyd](https://github.com/computational-sediment-hyd)
