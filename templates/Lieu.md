---
map_height_y: 2048  
map_width_x: 1642  
scale_pixels: 268  
scale_pixels_range: 25  
mapCalc1: 0  
---
<% await tp.file.move("Lore/Lieux/" + tp.file.title) %>
```leaflet  
id: MapExample  
image: [[Nyssor.webp]]
height: 850px
width: 95%
lat: 45
long: 35
unit: km
scale: 0.03 # units/px
defaultZoom: 7
```

## Lieux attachés

```dataview
TABLE faction as "Faction" WHERE categorie and categorie = "lieu" and region = "<% tp.file.title %>" SORT file.name
```


