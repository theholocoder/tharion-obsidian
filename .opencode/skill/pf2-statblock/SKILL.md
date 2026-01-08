---
name: pf2-statblock
description: >-
    Créer des statblocks (blocs de statistiques) pour les différents éléments de Pathfinder 2e,
    tels que les PJ, PNJ, monstres, feats (dons), sorts (spells), actions, activités, etc.
    Cela utilise le format Markdown avec un élément Obsidian code de type "pf2-stats".
---

## Quand utiliser cette compétence ?

Utiliser cette compétence dès qu'il faut rédiger un statblock Pathfinder 2e dans le contenu d'une note Obsidian.
Respecter le format donné (ci-après) pour chaque type d'éléments.

Si il manque des informations les demander au MJ (utilisateur) avant d'écrire. Les descriptions "RP" tels que l'apparence
ou la personnalité peuvent être inventée par tes soins si le MJ n'a rien précisé.

**Attention** : lorsque tu inventes des informations, prends en compte le lore du dossier @Lore/ pour éviter les incohérences.

## Types de statblocks

Choisi le statblock approprié en fonction du type d'élément. Remplace ce qui se trouve entre les chevrons `<EXEMPLE>`
par l'information appropriée.

Un token spécial peut être utilisé pour représenter le nombre d'action ou le type:

- 1 action : ``[one-action]``
- 2 actions : ``[two-actions]``
- 3 actions : ``[three-actions]``
- Action libre : ``[free-action]``
- Réaction : ``[reaction]``

Dans les descriptions, on utilise le gras pour les actions ou spécificités, par exemple:

```
**Corps à corps** [two-actions] charge
ou
**Succès critique** effet
**Succes** effet
```


### PNJ

```pf2e-stats
# <NOM DU PNJ>
## Niveau <NIVEAU>
---

==<TRAIT 1>== ==<TRAIT 2>==

<DESCRIPTION>
**Perception** <SCORE PERCEPTION>
**Volonté** <SCORE VOLONTE>
**Historique** <HISTORIQUE>
**Apparence** <APPEARANCE>
**Personnalité** <ADJECTIF 1>, <ADJECTIF 2>
**Oral, signe distinctif** <ACCENT OU VOIX>, <SIGNE>
```

### Action

```pf2e-stats
# <NOM DE L'ACTION> <?ACTIONS>
---

==<TRAIT 1>== ==<TRAIT 2>==

<DESCRIPTION>
```
