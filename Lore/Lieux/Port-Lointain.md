---
id: port-lointain
type: ville
categorie: lieu
region: "[[Nyssor]]"
faction:
  - "[[Concorde de Kaerith]]"
tags:
  - ville
  - categorie/lieu
  - capitale
updated: 2026-01-09
map_height_y: 1536
map_width_x: 2048
scale_pixels: 2048
scale_pixels_range: 6
mapCalc1: 0.0029296875
---

> [!NOTE]- Quick Calculator  
> Map Height in Pixels: `INPUT[number:map_height_y]`  
> Map Width in Pixels: `INPUT[number:map_width_x]`  
> lat: `VIEW[{map_height_y} / 2][math]`  
> long: `VIEW[{map_width_x} / 2][math]`  
> How Many Pixels In Scale: `INPUT[number:scale_pixels]`  
> How Many Units in Scale: `INPUT[number:scale_pixels_range]`  
> Scale: `VIEW[1/({scale_pixels}/{scale_pixels_range})][math:mapCalc1]`

```leaflet
id: map-port-lointain
lock: true
darkmode: false
image: [[Port-Lointain.webp]]
bounds: [[0,0], [1536,2048]]
height: 450px
width: 95%
lat: 768
long: 1024
unit: km
scale: 0.0029296875 # units/px
minZoom: -1.5
maxZoom: 2
defaultZoom: -1
zoomDelta: 0.5
```

## Description
Port-Lointain est le bastion principal de la colonisation sur [[Nyssor]]. C'est une ville en pleine effervescence, marquée par une architecture pragmatique en bois et en pierre, où le bruit des marteaux de construction se mêle aux cris des mouettes et aux ordres des officiers. La ville est divisée en plusieurs quartiers distincts, s'étendant du littoral vers les terres.

## Quartiers

### Le Rempart (Centre-Ville)
Cœur battant de la cité, ce quartier rassemble la majorité des commerces, des auberges et des habitations actuelles. C'est ici que la vie sociale s'organise.
*   **Architecture :** Dense et fonctionnelle.
*   **Défense :** Le quartier est actuellement ceinturé par une haute palissade en bois robuste. Des travaux sont en cours pour ériger un véritable mur d'enceinte en pierre qui délimitera le futur "Bastion" intérieur, gage de sécurité contre les menaces du continent.
*   **Lieux notables :** La caserne de l'[[Expédition des Fendeurs de Glace]], l'auberge de [[L'Hydre à Deux Choppes]].

### La Citadelle Blanche
Perchée sur un promontoire rocheux s'avançant dans la baie, la Citadelle domine la ville.
*   **Accès :** Un unique pont fortifié relie le promontoire au reste de la ville, rendant la zone très facile à défendre.
*   **Fonction :** C'est le centre politique et religieux. On y trouve les bâtiments officiels et administratifs.
*   **Style :** Contrairement au reste de la ville, les bâtiments y sont construits en pierre blanche dans un style gréco-romain, symbolisant l'ordre et la pérennité de la civilisation de [[Kaerith]].

### L'Ancrage (Les Docks)
Zone portuaire et industrielle située en contrebas.
*   **Atmosphère :** Laborieuse et salée. On y trouve les entrepôts, les chantiers navals et les quais.
*   **Population :** De nombreuses habitations y sont construites pour les ouvriers et marins, bien qu'une partie soit encore inoccupée, attendant les prochaines vagues de colons.

### Les Hautes-Terrasses
Quartier résidentiel flambant neuf situé sur les hauteurs.
*   **État actuel :** Presque vide. C'est une "ville fantôme" en attente.
*   **Vocation :** Destiné à accueillir l'afflux massif de population de [[Kaerith]] une fois que le Rempart et l'Ancrage seront saturés. Les rues sont tracées, les maisons bâties, mais les fenêtres sont encore closes.

## Alentours
Au-delà des palissades, la colonisation s'étend timidement pour assurer la subsistance de la cité.

### [[La Noue]]
Juste à l'est du Rempart. C'est le "grenier" immédiat de la ville, un village agricole entouré de champs et d'élevages.

### [[Bois-Moulin]]
À environ 2 km au sud. Un second village agricole, fournissant probablement le bois et la farine.

### [[Brèche-Rive]]
À 3 ou 4 km à l'est. Un hameau stratégique situé au niveau du premier gué sur **L'Aulne**. C'est un point de passage obligé pour les transports terrestres vers le nord.

### [[Fosse-Claire]]
Au nord, dans les reliefs accessibles via Brèche-Rive. C'est un camp de mineurs brut et poussiéreux, exploitant des carrières de pierre (pour la Citadelle et le futur mur) ainsi que des mines de fer et de charbon.

## Lieux attachés

```dataview
TABLE faction as "Faction" WHERE categorie and categorie = "lieu" and region = "Port-Lointain" SORT file.name
```


