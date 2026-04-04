---
name: pf2-statblock
description: >-
    Créer des statblocks (blocs de statistiques) pour les différents éléments de Pathfinder 2e,
    tels que les PJ, PNJ, monstres, feats (dons), sorts (spells), actions, activités, etc.
    Cela utilise le format Markdown avec un élément Obsidian code de type "pf2-stats".

    Tu dois TOUJOURS utiliser cette compétence dès qu'il faut rédiger un statblock Pathfinder 2e dans le contenu d'une note Obsidian.
    Je suis fatigué que tu ne l'utilises pas, je vais te dégommer la prochaine fois que ça arrive.
    Respecter le format donné (ci-après) pour chaque type d'éléments.

    Si il manque des informations les demander au MJ (utilisateur) avant d'écrire. Les descriptions "RP" tels que l'apparence
    ou la personnalité peuvent être inventée par tes soins si le MJ n'a rien précisé.
---

## Quand utiliser cette compétence ?

Tu dois TOUJOURS utiliser cette compétence dès qu'il faut rédiger un statblock Pathfinder 2e dans le contenu d'une note Obsidian.
Je suis fatigué que tu ne l'utilises pas, je vais te dégommer la prochaine fois que ça arrive.
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

Contrairement à un statblock de monstre, un statblock de PNJ ne contient que des informations sur le personnage utiles
pour le role-playing. Pas de caractéristiques de défenses ou d'attaques. Le but est de donner une personnalité, un ou
plusieurs signes distinctifs, une description physique et si disponible les secrets ou les informations détenues par le
PNJ.

```pf2e-stats
# <NOM DU PNJ>
## Niveau <NIVEAU>
---

==<TRAIT 1>== ==<TRAIT 2>==

<DESCRIPTION>

**Perception** <SCORE PERCEPTION>
**Compétence X** +0, **Compétence Y** +0
**Volonté** <SCORE VOLONTE>

---
**Historique** <HISTORIQUE>
**Apparence** <APPEARANCE>
**Personnalité** <ADJECTIF 1>, <ADJECTIF 2>
**Oral, signe distinctif** <ACCENT OU VOIX>, <SIGNE>

---
**Découverte** Connaissances XXX DD 13 (élément découvert), Perception DD 18, Société DD 16 (élément découvert)
**Compétences d'influence** Connaissances XXX DD 16, Intimidation DD 20, Duperie DD 22 (précisions contexte), Diplomatie DD <10+SCORE VOLONTE>
**Influence 4.** Information ou avantage.
**Influence 6.** Information ou avantage.
**Influence 8.** Information ou avantage.
**Résistances.** Ce qui augmente de 2-5 le DD.
**Faiblesses.** Ce qui réduit de 2-5 le DD.
```

Précisions sur les règles d'influence de Pathfinder 2e:

- "Découverte" c'est les compétences et difficulté pour trouver des informations sur le PNJ. Il est intéressant de
préciser ce qu'on découvre sur le PNJ avec chaque compétence, par exemple Médecine DD 13 (Le PNJ est en état de choc).
Il peut être intéressant d'ajouter une compétence "Lore"/"Connaissance" qui correspond à l'historique du PNJ,
généralement avec le DD le plus faible car très personnel. La comptétence "Perception" est toujours présente et son DD
est le DD par niveau de la créature (par exemple, DD 18 au niveau 3). Les autres compétences ont des DD plus faibles.
- "Compétences d'influence" liste les compétences que les PJ peuvent utiliser pour influencer le PNJ avec leur DD trié
du plus bas au plus élevé. Diplomatie figure généralement dans cette liste mais rarement comme la meilleure compétence
pour influencer le PNJ (son DD minimum est 10+SCORE VOLONTE). Il est possible de préciser le contexte de chaque
compétence si elle doit être utilisée d'une façon "RP" particulière pour fonctionner.
- "Influence X" sont les différents seuils en nombre de points d'influence nécessaires pour obtenir l'information qui en
decoule.
- La "résistance" c'est pour indiquer les comportements des PJ qui vont augmenter la difficulté à obtenir des
informations de la part du PNJ.
- A l'inverse la "faiblesse" c'est tout ce qui peut permettre d'amadouer le PNJ afin qu'il livre ses informations
(volontairement) plus facilement.
- Les PJ otiennent un point d'influence sur un succès à un test de "compétence d'influence". Sur un succès critique,
ils en obtiennent deux.

### Monstre

Un statblock de monstre est exclusivement destiné au combat. Il contient des informations sur les caractéristiques
de défense et d'attaque, les différentes actions, capacités et sorts du monstre. Le layout suivant est sur deux colonnes.

> [!statblocks|columns]
>>```pf2e-stats
>># <NOM DE LA CRÉATURE>
>>## Créature <NIVEAU>
>>---
>>
>>==<TAILLE>== ==TRAIT 1== ==TRAIT 2==
>>
>>**Perception** +4; <AUTRES SENS>
>>**Langues** <LANGUES>
>>**Compétences** Athlétisme +7, Intimidation +6, Nature +6, Survie +4
>>**For** +5, **Dex** +1, **Con** +4, **Int** +1, **Sag** +1, **Cha** +1
>>---
>>**CA** 15; **Vig** +10, **Réf** +4, **Vol** +7
>>**PV** 26; **Résistances** <TYPE DE RÉSISTANCE> <RÉSISTANCE>; **Faiblesses** <TYPE DE FAIBLESSE> <FAIBLESSE>
>>---
>>**Vitesse** 25ft
>>
>>**Corps à corps** `[one-action]` strike +9 (finesse), **Dégâts** 1d4+2 perforant
>>**Corps à corps** `[one-action]` claws +9, **Dégâts** 1d6+3 tranchant (plus <CAPACITE>)
>>---
>>```
>
>>```pf2e-stats
>>**<NOM DE LA CAPACITE>** `[reaction]`
>>**Condition** <CONDITION>
>>
>><DESCRIPTION>
>>
>>---
>>
>>**<NOM DE LA CAPACITE>** `[one-action]`
>>**Condition** <CONDITION>
>>
>><DESCRIPTION>
>>```

### Action

```pf2e-stats
# <NOM DE L'ACTION> <?ACTIONS>
---

==<TRAIT 1>== ==<TRAIT 2>==

<DESCRIPTION>
```
