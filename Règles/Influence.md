> [!question]+ Point de règle
>Lorsque les PJ doivent gagner la faveur d'un PNJ ou l'influencer pour atteindre leurs objectifs, parfois un test de [[Duperie]], [[Diplomatie]] ou [[Intimidation]] ne suffit pas. Dans ces cas, vous pouvez implémenter le sous-système d'influence dans une rencontre sociale.
>
>L'influence est un sous-système à court terme dans lequel les PJ accumulent des [[Points d'influence]] durant une rencontre sociale avec un PNJ pour représenter leur influence croissante. Ces rencontres sont une course contre la montre pour atteindre des seuils de [[Points d'influence]] afin d'influencer le PNJ. C'est parfait pour un rassemblement social unique — qu'il s'agisse d'une fête, d'une négociation de traité, ou même d'une tentative de persuader divers membres d'un panel de juges.
>
>En raison de la variété d'options de compétences d'Influence et de la capacité d'utiliser [[Perception]] pour découvrir davantage d'informations, chaque personnage a quelque chose d'important à apporter dans le sous-système d'influence, contrairement aux situations où un seul personnage possède [[Diplomatie]].
>
>Le sous-système d'influence divise une rencontre sociale en rounds, le nombre de rounds représentant la durée de l'événement social. Les rounds durent le temps que vous déterminez, en fonction des besoins du récit, bien qu'entre 15 minutes et une heure soit typique.
>
>Durant chaque round d'une rencontre d'influence, chaque PJ peut agir une fois pour soit [[Influencer]], soit [[Découvrir]].

![[Influencer]]
![[Découvrir]]

## Influence Stat Blocks

> [!question]+ Point de règle
>**Source** [GM Core - Sources - Archives of Nethys: Pathfinder 2nd Edition Database](https://2e.aonprd.com/Sources.aspx?ID=218)
>NPCs in the influence subsystem have little need for many of the statistics you'll find in an ordinary creature stat block. However, it might help you to prepare for the social encounter by creating an influence stat block for each prominent NPC. These are optional; if you can keep most information straight in your head, you might skip this step or just write down the first three categories to keep the numbers straight.  
 > 
>Influence stat blocks are flexible and contain only the stats that you are essential to running the NPC during a social encounter, leaving the rest out. The main stats that matter are the NPC's Perception and Will modifiers.

### Stat Block
```pf2e-stats
# NPC Name
## Niveau 0
---

==Traits==

A succinct description of the NPC, such as “Famous musician” or “Popular baron.”  
**Perception** The NPC's Perception modifier, plus potentially relevant abilities such as scent or truesight.  
**Will** The NPC's Will modifier, plus any special adjustments.  
**Discovery** The Perception DC to Discover information about the NPC, as well as any skill checks to Discover their DCs.  
**Influence Skills** The skills the PCs can use to Influence the NPC are listed here with their DCs, in order from the lowest DC (the skill that works best) to the highest DC. If a skill isn't listed but a player gives a strong narrative explanation for using it, you can add it as an appropriate DC (usually the highest listed DC). Diplomacy should usually be on this list, but should rarely be the best skill to Influence an NPC, in order to encourage and reward using Discover to learn and cater to an NPC's interests.  
**Influence Thresholds** The number of Influence Points required to Influence the PC, and the benefits for meeting them. Some NPCs might have multiple influence thresholds, granting the PCs additional benefits or favors as they cross more thresholds.  
**Resistances** Some NPCs are resistant to certain tactics, biased against certain types of people, or may get defensive when a certain topic comes up. Any of these makes it harder for a PC to convince them. For instance, an NPC might find flattery inane, dislike wizards, or bristle at any mention of their ex-spouse. Typically, an NPC's resistance increases the DC of the associated check to Influence by 2 (or 5 for stronger resistances), but it could have farther-ranging consequences, such as losing Influence Points or angering the NPC enough that attempting to Influence them again is impossible.  
**Weaknesses** Most NPCs have at least one weakness that clever and observant PCs can use to their advantage, whether it's a deep-seated insecurity, a desire for power, a favorite hobby, a bias toward a certain group, or a hidden secret the PCs could threaten to expose. When a PC incorporates an NPC's weakness, it typically decreases the associated Influence check's DC by 2 (or 5 for stronger weaknesses), but it could have farther-ranging effects, such as gaining automatic Influence Points or even automatically influencing the NPC regardless of how many Influence Points the PCs have achieved so far.
```

> [!question]+ Point de règle
> After the influence stat block, you might want to list important information to help you roleplay the NPC and incorporate the NPC into your influence encounter. You can list any of the following details that are relevant to your NPC: their background (a brief bio focusing on information relevant to the encounter), appearance, personality (this can just be a list of adjectives), affiliations, public goals, hidden agendas, or the penalty for antagonizing the NPC (or possibly for failing to Influence the NPC, depending on the way you structure the encounter).

>[!info]- Sample Stat Block
> In this example, the PCs try to convince a grizzled landlord to not evict a theatrical troupe from a dilapidated building he owns. It's a 3rd-level challenge. He is a busy, practical man and gives the PCs only 45 minutes (3 rounds) to make their case.
>
>```pf2e-stats
># Danphy Mollwether
>## Niveau 3
>---
>
>==Unique== ==Medium== ==Human== ==Humanoid==
>
>Penny-pinching landlord
>**Perception** +9
>**Will** +12  
>**Discovery** DC 13 Mercantile Lore, DC 18 Perception, DC 16 Society  
>**Influence Skills** DC 16 Accounting Lore (noting how the theater could be made profitable), DC 16 Crafting (volunteering to repair the building), DC 20 Intimidation, DC 20 Performance, DC 22 Diplomacy, DC 24 Deception  
>**Influence 4** Mr. Mollwether gives the troupe 1 week to get him his back rent, with interest, before evicting them.  
>**Influence 6** Mr. Mollwether gives the troupe 1 month to get him his back rent before evicting them.  
>**Influence 8** Mr. Mollwether allows the troupe to stay, reduces their rent, and forgives half their debt.  
>**Resistances** The landlord thinks in practical terms, with little patience for the “good-for-nothings” of the troupe. Appeals directed at sympathy alone increase the check's DC by 2.  
>**Weaknesses** Mr. Mollwether used to visit the theater often as a small child, and performing one of his favorite old songs or plays brings tears to his eyes and reduces the Performance DC by 2.  
>**Background** Mollwether was raised by wealthy parents who loved the arts and took him to the theater often. A scandal left the family broke, and Danphy clawed his way back up to a decent living. Becoming something of a slumlord, he owns several properties now and still feels he must exploit others to survive.  
>**Appearance** An elderly man in cheap dress clothes, Mr. Mollwether looks like he's never felt a moment of love for anyone in his entire life.  
>**Personality** Impatient, crotchety, skeptical  
>**Penalty** Antagonizing Mr. Mollwether by “sermonizing” or “wasting his time” causes him to cut the meeting short, reducing it to 2 rounds instead of 3.
>```

### Setting DC

> [!question]+ Point de règle
>**Source** [GM Core - Sources - Archives of Nethys: Pathfinder 2nd Edition Database](https://2e.aonprd.com/Sources.aspx?ID=218)
> When setting DCs, it's often good to start with a noncombat level or “social level” for the NPC and set their DCs accordingly. Use the DC adjustments from page 53 just like you normally would. A good starting place is setting the NPC's Will modifier, then taking that DC and adjusting it for skills that are more or less likely to work.  
>
>For instance, for a 3rd-level challenge, you might give an NPC a +12 Will modifier and use 22 as the base DC. You might say that's the DC for Diplomacy but then determine that the NPC is difficult to intimidate, and so you apply the hard DC adjustment to make the Intimidation DC 24. Maybe you also determine that she loves different varieties of wine, resulting in an incredibly easy DC adjustment to get DC 12 for Alcohol Lore.

## Running an influence encounter

> [!question]+ Point de règle
>**Source** [GM Core - Sources - Archives of Nethys: Pathfinder 2nd Edition Database](https://2e.aonprd.com/Sources.aspx?ID=218)
> When running an influence encounter, let the PCs be creative and use a diverse set of skills whenever possible. Be open to improvisation, and change the structure of the encounter if something interesting presents itself. The PCs set the pace and choose with whom they interact. It's up to you to make sure every NPC is distinct, react to the PCs' interactions with the NPCs, and lend overall structure to the encounter by making sure it feels like a living, breathing event rather than just a series of skill checks.  
>
>Think about how the number of rounds of a social encounter relate to the overall event. For instance, if you have a four-course banquet and 6 rounds, you could have 1 round for introductions before the food arrives, 1 round for each of the courses, and 1 last round of conversations after the final course. NPCs might filter in and out or become unavailable for conversations as they are occupied by various tasks, or become particularly eager to engage a PC. That sort of change help makes the NPC feel a bit more real and helps break up any repetition in your encounter.
