---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 11
code: S011
date_irl: 2026-04-26
fc-date: 14/06/42
fc-end: 14/06/42
resume: ""
pjs:
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Noctis.md|Noctis]]"
  - "[[Campagnes/EFG/PJ/Yoko.md|Yoko]]"
  - "[[Campagnes/EFG/PJ/Théobald Greyheart.md|Théobald Greyheart]]"
  - "[[Campagnes/EFG/PJ/Sylis et Sylorn.md|Sylis et Sylorn]]"
updated: 2026-04-26
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

Cette session a été gérée par un autre MJ (Maxime).