<%*
// Tente de récupérer le nom de la session parente si on est dans un dossier de session
const currentFolder = tp.file.folder(true);
let sessionLink = "";
if (currentFolder.match(/^S\d{3}\s-\s/)) {
    sessionLink = `[[${currentFolder}/${currentFolder}.md|${currentFolder}]]`;
}
-%>
---
type: combat
parent: "<% sessionLink %>"
difficulte: Modérée
xp: 
---
# <% tp.file.title %>

## Enjeu
*Pourquoi ce combat a-t-il lieu ?*

## Terrain
- **Taille** : 
- **Couvert** : 
- **Dangers** : 

## Forces en présence

| Nom | Nombre | Initiative | PV | Notes |
|---|---|---|---|---|
| Ennemi A | | | | |
| Ennemi B | | | | |

## Tactiques
- **Round 1** :
- **Si difficulté** : 

## Butin
- 
