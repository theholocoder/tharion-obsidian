---
id: Myca Libre-Spore
type: PJ
campagne: "[[L'Expédition des Fendeurs de Glace]]"
joueur: Adèle
ascendance: Humain
classe: Druide
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
> *Une brève description physique et le concept clé du personnage en une ou deux phrases.*

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
