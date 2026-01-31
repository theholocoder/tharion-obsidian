---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 1
code: S001
date_irl: 2026-02-01
date_ig_debut: 08/11/42
date_ig_fin: 08/11/42
pjs:
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Chiro Kono.md|Chiro Kono]]"
  - "[[Campagnes/EFG/PJ/Théobald Greyheart.md|Théobald Greyheart]]"
  - "[[Campagnes/EFG/PJ/Voss Vitriox.md|Voss Vitriox]]"
  - "[[Campagnes/EFG/PJ/Yoko.md|Yoko]]"
  - "[[Campagnes/EFG/PJ/Lyra.md|Lyra]]"
  - "[[Campagnes/EFG/PJ/Noctis.md|Noctis]]"
  - "[[Myca Libre-Spore]]"
  - "[[Campagnes/EFG/PJ/Fenn Brindebois.md|Fenn Brindebois]]"
  - "[[Campagnes/EFG/PJ/Korvax Oeil-de-fer.md|Korvax Oeil-de-fer]]"
resume: ""
updated: 2026-01-09
termine: false
---
## Informations sur la session

**Date IRL :** `INPUT[datePicker:date_irl]` | **Début IG :** `INPUT[text(placeholder('2942-11-08')):date_ig_debut]` | **Fin IG :** `INPUT[text(placeholder('2941-11-10 / vide')):date_ig_fin]` | **Terminée ?** `INPUT[toggle:termine]`

```meta-bind
INPUT[textArea(title('Résumé de la session en 2-5 phrases max. ')):resume]
```

```meta-bind
INPUT[listSuggester(title('Personnages'), optionQuery("Campagnes/EFG/PJ")):pjs]
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

## TODO

- [ ] Audio bourdonnements + cloches d'alarme
- [ ] Intro + musique d'intro pour la campagne
- [ ] Handout: document du [[Conseil de la Brèche]] indiquant que si le PJ permet la destruction des Mantes Géantes, le conseil lui accordera un droit de propriété sur la parcelle de son choix dans le quartier des Hautes-Terrasses ou le terrain de son choix au delà des murs de la ville. Ils gagneront également le rang d'Eclaireur
- [ ] FoundryVTT: configurer un timer ou un resource bar pour la limite de temps après Aelys Tarn
- [ ] FoundryVTT: battlemap rue Gelevrod
- [ ] FoundryVTT: battlemap combat à la porte
- [ ] FoundryVTT: battlemap combat boss
- [ ] FoundryVTT: objet "Fragment d'exuvie" et "Marquage phéromonal"
- [x] Scène 4: dialogue du boss en une fois avant le combat

## Intro

> TODO



## Aperçu de la session
Les joueurs sont arrivés depuis peu à [[Port-Lointain]], ils sont réunis dans la taverne [[L'Hydre à Deux Choppes]]. Ils sociabilisent et découvrent l'abondance de [[Nyssor]] lorsqu'ils sont interrompus par un bourdonnement et les cloches d'alarmes : les [[Cisarelles]] attaquent la ville.

### Scènes
```dataview
TABLE WHERE type = "scene" AND contains(file.folder, this.file.folder) SORT file.name
```

![[Scène 1 - L'Hydre à Deux Choppes]]

![[Scène 2 - Commandant Aelys Tarn]]

![[Scène 3a - La Porte de la Noue]]

![[Scène 3b - Rue Gelevrod]]

![[Scène 3c - Entrepôt des docks]]

![[Scène 4 - la Citadelle Blanche]]




---

## À reporter / Prépa prochaine

- Reporter les rumeurs et POI sur FoundryVTT