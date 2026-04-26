---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 10
code: S010
date_irl: 2026-04-09
fc-date: 04/06/42
fc-end: ""
resume: ""
pjs:
  - "[[Campagnes/EFG/PJ/Chiro Kono.md|Chiro Kono]]"
  - "[[Campagnes/EFG/PJ/Fenn Brindebois.md|Fenn Brindebois]]"
  - "[[Campagnes/EFG/PJ/Korvax Oeil-de-fer.md|Korvax Oeil-de-fer]]"
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Voss Vitriox.md|Voss Vitriox]]"
  - "[[Campagnes/EFG/PJ/Lyra.md|Lyra]]"
updated: 2026-04-09
termine: false
timelines:
  - session
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

## Scènes
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
