---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 8
code: S008
date_irl: 2026-03-17
fc-date: 29/05/42
fc-end: 29/05/42
resume: Logan et Théobald rendent compte à Soren Carthain concernant les fioles et l'épave.
pjs:
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Théobald Greyheart.md|Théobald Greyheart]]"
updated: 2026-03-17
termine: true
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

## Indices / Pistes
- [[Le Marché Secret]] la piste de l'homme à la capuche a été remontée jusque dans la forêt au Sud
- [[Les Moutons Merveilleux]] Hodert Ferdo Gedge leur dit que les moutons grandissent un peu vite...
- [[Les Murmures des Racines]] un bruit de couloir, "des murmures dans les arbres".


## Notes
- Ils vont voir Hodert Ferdo Gedge le garde halfelin sur la place de la citadelle.
- Ils vont voir [[Soren Carthain]] rende les tubes mais pas le codex.
- Ils posent des questions sur [[Lyra]]. Balancent [[Commandant Aelys Tarn]] comme son supérieur. Ils suivent [[Lyra]], [[Soren Carthain]] va se renseigner sur le [[Commandant Aelys Tarn]] et la [[République de Thaldris]].
- [[Korran Vraxx]] pense que [[Théobald Greyheart]] le drague et qu'il a un coup.
- [[Logan]] a fait une copie des 7 dernières pages du Codex retrouvé dans l'épave avant de le rendre à [[Korran Vraxx]].
- Puis, [[Logan]] fait encore 5 copies des 7 pages.

## À reporter / Prépa prochaine
- changer la léchi sur la salle de balle
- 
