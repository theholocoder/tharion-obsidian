---
type: campagne
campagne: EFG
tags: [campagne, hub]
updated: 2026-01-09
---
# EFG — Hub

```meta-bind-button
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

## Accès rapide
- Intro joueurs : [[EFG Intro]]
- Prépa : [[30 - Prépa prochaine session]]
- Arcs/Fronts : [[10 - Arcs & Fronts]]
- Quêtes : [[11 - Quêtes & Missions]]
- Rumeurs : [[Liste des rumeurs]]

## Sessions (EFG)
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
WHERE type = "session" AND campagne = "EFG"
SORT numero DESC
```
