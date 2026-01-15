<%*
// Tente de récupérer le nom de la session parente si on est dans un dossier de session
const currentFolder = tp.file.folder(true);
let sessionLink = "";
// Si le dossier ressemble à "S00X - Titre", on peut supposer que c'est la session
if (currentFolder.match(/^S\d{3}\s-\s/)) {
    sessionLink = `[[${currentFolder}/${currentFolder}.md|${currentFolder}]]`;
} else {
    // Sinon on laisse vide ou on demande
    sessionLink = ""; 
}
-%>
---
type: scene
parent: "<% sessionLink %>"
tags: [scene, lieu]
---
# <% tp.file.title %>

## Description
*Lumière, odeurs, sons...*

## Points d'intérêt
- **A** : 
- **B** : 

## Créatures / PNJ
- 

## Butin / Indices
- 
