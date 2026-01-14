---
type: session
campagne: EFG
numero: 1
code: S001
date_irl: 2026-02-01
date_ig_debut: 08/11/42
date_ig_fin: 08/11/42
persos: []
resume: ""
updated: 2026-01-09
termine: true
---
## Informations sur la session

**Date IRL :** `INPUT[datePicker:date_irl]` | **Début IG :** `INPUT[text(placeholder('2942-11-08')):date_ig_debut]` | **Fin IG :** `INPUT[text(placeholder('2941-11-10 / vide')):date_ig_fin]` | **Terminée ?** `INPUT[toggle:termine]`

```meta-bind
INPUT[textArea(title('Résumé de la session en 2-5 phrases max. ')):resume]
```

```meta-bind
INPUT[listSuggester(title('Personnages'), useLinks(partial), allowOther):persos]
```

---

## Précédemment
> (dynamique) Affiche le `resume` de la session précédente dès qu’il est rempli.

```dataview
TABLE WITHOUT ID resume
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
