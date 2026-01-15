---
map_height_y: 2048
map_width_x: 1642
scale_pixels: 268
scale_pixels_range: 30
mapCalc1: 0
---
<% await tp.file.move("Lore/Lieux/" + tp.file.title) %>

> [!NOTE]- Quick Calculator  
> Map Height in Pixels: `INPUT[number:map_height_y]`  
> Map Width in Pixels: `INPUT[number:map_width_x]`  
> lat: `VIEW[{map_height_y} / 2][math]`  
> long: `VIEW[{map_width_x} / 2][math]`  
> How Many Pixels In Scale: `INPUT[number:scale_pixels]`  
> How Many Units in Scale: `INPUT[number:scale_pixels_range]`  
> Scale: `VIEW[1/({scale_pixels}/{scale_pixels_range})][math:mapCalc1]`

```leaflet  
id: MapExample  
image: [[Nyssor.webp]]
bounds: [[0,0], [4096,4096]]
height: 850px
width: 95%
lat: 2280
long: 1700
unit: km
scale: 0.03 # units/px
minZoom: -2
maxZoom: 1
defaultZoom: -2
zoomDelta: 1
```

## Lieux attachés

```dataview
TABLE faction as "Faction" WHERE categorie and categorie = "lieu" and region = "<% tp.file.title %>" SORT file.name
```


