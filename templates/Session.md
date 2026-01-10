<%*
/**
 * Session template
 * - campagne: EFG
 * - numéro auto (max numero + 1) parmi Sessions/ de cette campagne
 * - nom final: "S### - <titre>"
 */
const CAMP = "EFG";
const sessionsFolder = "Sessions/";

// calcule prochain numéro
const files = app.vault.getMarkdownFiles().filter(f => f.path.startsWith(sessionsFolder));

let maxNum = 0;
for (const f of files) {
  const fm = app.metadataCache.getFileCache(f)?.frontmatter;
  if (!fm) continue;
  if (fm.type !== "session") continue;
  if (fm.campagne !== CAMP) continue;
  const n = Number(fm.numero);
  if (!Number.isNaN(n)) maxNum = Math.max(maxNum, n);
}
const numero = maxNum + 1;
const code = "S" + String(numero).padStart(3, "0");

// titre demandé une seule fois, stable
const titre = await tp.system.prompt("Titre de la session (court, stable)", "");
const safeTitre = (titre && titre.trim().length) ? titre.trim() : "Sans titre";

// rename
await tp.file.rename(`${code} - ${safeTitre}`);
-%>
---
type: session
campagne: EFG
numero: <% numero %>
code: <% code %>
date_irl: <% tp.date.now("YYYY-MM-DD") %>
date_ig_debut: ""
date_ig_fin: ""
joueurs: []
persos: []
resume: ""
updated: <% tp.date.now("YYYY-MM-DD") %>
termine: false
---

## Informations sur la session

**Date IRL :** `INPUT[datePicker:date_irl]` | **Début IG :** `INPUT[text(placeholder('08/11/42')):date_ig_debut]` | **Fin IG :** `INPUT[text(placeholder('10/11/42 / vide')):date_ig_fin]` | **Terminée ?** `INPUT[toggle:termine]`

```meta-bind
INPUT[textArea(title('Résumé de la session en 2-5 phrases max. ')):resume]
```

```meta-bind
INPUT[listSuggester(title('Personnages'), useLinks(partial), allowOther):persos]
```

---

## Précédemment

```dataview
TABLE choice(length(resume) > 0, resume, "*Aucun résumé renseigné pour la session précédente.*") AS "Résumé"
FROM "Sessions"
WHERE type = "session"
  AND campagne = "EFG"
  AND numero = this.numero - 1
LIMIT 1
```

---

## Scènes (notes MJ)
- 

## Événements / Décisions
- 

## Indices / Pistes
- 

## Butin / Récompenses
- 

## À reporter / Prépa prochaine
- 
