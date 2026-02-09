---
type: campagne
campagne: EFG
tags: [campagne, hub]
updated: 2026-01-09
---
# EFG — Hub

```leaflet  
id: nyssor-map  
lock: true
darkMode: false
image: [[Nyssor.webp]]
bounds: [[0,0], [4096,4096]]
height: 850px
width: 95%
lat: 2280
long: 1700
unit: km
scale: 0.16853932584269662
minZoom: -2
maxZoom: 2
defaultZoom: -2
zoomDelta: 0.5
```
## Accès rapide
- Intro joueurs : [[EFG Intro]]
- Rumeurs : [[Liste des rumeurs]]

## Sessions `BUTTON[button-new-session]`
```dataview
TABLE
  code AS "Code",
  dateformat(date(date_irl), "dd/LL/yy") AS "Date IRL",
  date_ig_debut AS "IG début",
  date_ig_fin AS "IG fin",
  joueurs AS "Joueurs",
  resume AS "Résumé",
  choice(termine, "☑", "☐") as "Terminée?"
FROM "Sessions"
WHERE type = "session" AND campagne = [[L'Expédition des Fendeurs de Glace]]
SORT numero DESC
```
colonne1;colonne2
test;csv
peut;marcher
## Joueurs `BUTTON[button-new-pj]`
```dataview
TABLE
  joueur AS "Joueur",
  classe AS "Classe",
  ascendance AS "Ascendance"
FROM "Campagnes/EFG/PJ"
WHERE type = "PJ"
SORT file.name ASC
```



```meta-bind-button
id: button-new-session
hidden: true
style: primary
label: Nouvelle Session (EFG)
actions:
  - type: templaterCreateNote
    templateFile: "templates/Session.md"
    folderPath: "Sessions"
    fileName: "Nouvelle session - RENAME ME"
    openNote: true
    openIfAlreadyExists: false
```

```meta-bind-button
id: button-new-pj
hidden: true
style: primary
label: Nouveau PJ (EFG)
actions:
  - type: templaterCreateNote
    templateFile: "templates/PJ.md"
    folderPath: "Campagnes/EFG/PJ"
    fileName: "Nouveau PJ - RENAME ME"
    openNote: true
    openIfAlreadyExists: false
```