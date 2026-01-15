---
id: Noctis
type: PJ
campagne: "[[L'Expédition des Fendeurs de Glace]]"
joueur: Gilles
ascendance: Elfe
classe: Bretteur
niveau: 1
statut: Vivant
faction: "[[République de Thaldris]]"
tags:
  - pj
updated: 2026-01-15
---

> [!infobox]
> **Joueur** :: `VIEW[{joueur}]`
> **Ascendance** :: `VIEW[{ascendance}]`
> **Classe** :: `VIEW[{classe}]`
> **Niveau** :: `VIEW[{niveau}]`

> [!abstract]+ Concept & Apparence
> Noctis est un elfe grand et élancé, avec une silhouette nerveuse faite pour la vitesse plutôt que la force brute. Chaque mouvement chez lui semble calculé, comme s’il était toujours à un souffle de dégainer ou d’esquiver. 
>Sa peau est pâle, presque froide, contrastant avec ses cheveux argentés qu’il porte longs et légèrement en bataille. Ils encadrent un visage anguleux aux traits fins mais durs, marqué par une vie passée à survivre plutôt qu’à vivre.
>Ses yeux sont sa caractéristique la plus troublante : d’un vert éclatant ils semblent parfois refléter une lueur rougeâtre quand des créatures infernales sont proches.
> Il porte un long manteau de cuir sombre, usé et griffé, souvent entrouvert pour lui permettre de bouger librement. En dessous, des vêtements de bretteur pratiques, renforcés mais légers. À sa ceinture pendent plusieurs dagues, tandis que sa rapière — fine, élégante, mortelle — est toujours à portée de main. Son corps porte quelques cicatrices, discrètes mais nombreuses, souvenirs de combats qu’il n’aurait pas dû survivre.
>Et pourtant, quand Noctis sourit, on y devine quelque chose de dangereux : un mélange de défi, de fatigue et de mépris pour la mort. On dirait quelqu’un qui a déjà tout perdu… et qui n’a plus rien à craindre.

> [!note]- Background
> *Résumé de l'histoire du personnage avant l'aventure. Origines, événements marquants.*

## Relations Clés
- **[[PNJ ou PJ]]** : Nature de la relation.
- **[[Organisation]]** : Affiliation ou conflit.

## Accomplissements
*Titres gagnés, hauts faits héroïques ou réputation acquise.*

## Secrets & Notes du MJ
> [!private] Réservé au MJ
> Ici, notez les secrets liés au background que le joueur ignore peut-être, ou les intrigues futures qui le concernent spécifiquement.
> - [ ] Idée d'arc narratif : ...

## Évolution & Choix Marquants
*Notes sur les choix mécaniques ayant un impact narratif ou les objets iconiques.*
- **Dons d'Héritage/Ascendance** :
- **Archétypes** :
- **Objets Uniques/Reliques** :

## Historique des Sessions
*Sessions où le personnage est présent ou mentionné.*

```dataview
TABLE date_irl as "Date", resume as "Résumé"
FROM "Sessions"
WHERE contains(persos, this.file.link) OR contains(file.outlinks, this.file.link)
SORT date_irl DESC
```
