<%*
/**
 * Session template
 * - campagne: [[L'Expédition des Fendeurs de Glace]]
 * - numéro auto (max numero + 1) parmi Sessions/ de cette campagne
 * - nom final: "S### - <titre>"
 */
const CAMP = "[[L'Expédition des Fendeurs de Glace]]";
const sessionsFolder = "Sessions/";

// calcule prochain numéro
// getMarkdownFiles renvoie TOUS les fichiers du vault, on filtre ceux qui sont dans Sessions/ (y compris sous-dossiers)
const files = app.vault.getMarkdownFiles().filter(f => f.path.startsWith(sessionsFolder));

let maxNum = 0;
for (const f of files) {
  const fm = app.metadataCache.getFileCache(f)?.frontmatter;
  if (!fm) continue;
  if (fm.type !== "session") continue;
  // On nettoie les guillemets éventuels autour du nom de campagne pour la comparaison
  const fmCampagne = fm.campagne ? fm.campagne.replace(/^"|"$/g, '') : "";
  const targetCamp = CAMP.replace(/^"|"$/g, '');
  
  if (fmCampagne !== targetCamp) continue;
  
  const n = Number(fm.numero);
  if (!Number.isNaN(n)) maxNum = Math.max(maxNum, n);
}
const numero = maxNum + 1;
const code = "S" + String(numero).padStart(3, "0");

// titre demandé une seule fois, stable
const titre = await tp.system.prompt("Titre de la session (court, stable)", "");
const safeTitre = (titre && titre.trim().length) ? titre.trim() : "Sans titre";

const baseName = `${code} - ${safeTitre}`;
const newFolderPath = `${sessionsFolder}${baseName}`;

// Création du dossier s'il n'existe pas
if (!app.vault.getAbstractFileByPath(newFolderPath)) {
    await app.vault.createFolder(newFolderPath);
}

// Déplacement du fichier courant dans le nouveau dossier
await tp.file.move(`${newFolderPath}/${baseName}`);
-%>
---
type: session
campagne: [[L'Expédition des Fendeurs de Glace]]
numero: <% numero %>
code: <% code %>
date_irl: <% tp.date.now("YYYY-MM-DD") %>
fc-date: ""
fc-end: ""
resume: ""
pjs: []
updated: <% tp.date.now("YYYY-MM-DD") %>
termine: false
timelines: ["session"]
aat-render-enabled: true
---

## Informations sur la session

**Date IRL :** `INPUT[datePicker:date_irl]` | **Début IG :** `INPUT[text(placeholder('08/11/42')):fc-date]` | **Fin IG :** `INPUT[text(placeholder('10/11/42 / vide')):fc-end]` | **Terminée ?** `INPUT[toggle:termine]`

```meta-bind
INPUT[textArea(title('Résumé de la session en 2-5 phrases max. ')):resume]
```

```meta-bind
INPUT[listSuggester(title('Personnages'), optionQuery("Campagnes/EFG/PJ")):pjs]
```

---

## Précédemment

```dataview
TABLE choice(length(resume) > 0, resume, "*Aucun résumé renseigné pour la session précédente.*") AS "Résumé"
FROM "Sessions"
WHERE type = "session"
  AND numero = this.numero - 1
LIMIT 1
```

---

## TODO

- [ ] item

## Intro

> Todo

## Aperçu de la session
- 

### Scènes
```dataview
TABLE WHERE type = "scene" AND contains(file.folder, this.file.folder) SORT file.name
```

## Événements / Décisions
- 

## Indices / Pistes
- 

## Butin / Récompenses
- 

## À reporter / Prépa prochaine
- 
