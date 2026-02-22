---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 4
code: S004
date_irl: 2026-02-21
fc-date: 2942-05-18
fc-end: 2942-05-18
resume: ""
pjs:
  - "[[Campagnes/EFG/PJ/Yoko.md|Yoko]]"
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Lyra.md|Lyra]]"
  - "[[Campagnes/EFG/PJ/Chiro Kono.md|Chiro Kono]]"
  - "[[Campagnes/EFG/PJ/Fenn Brindebois.md|Fenn Brindebois]]"
updated: 2026-02-21
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

- [ ] Visuel des Azarkati
- [ ] Visuel du bernard-l'hermite
- [ ] Statblocks combat 1
- [ ] Statblocks bernard-l'hermite
- [ ] Statblocks Azarkati
- [ ] Rumeurs à trouver
- [ ] Scène/battlemap de la descente
- [ ] Scène de l'épave
- [ ] Battle map upper deck
- [ ] Battle map middle deck
- [ ] Battle map lower deck
- [ ] Prep. downtime activities
- [ ] Récompenses

## Intro

> Nyssor... 
> Au-delà de la Couronne Blanche, s'étendent des terres sans cartes et des ruines sans noms.
> Bienvenue, **éclaireur** de l'Expédition des Fendeurs de Glace. On vous envoie là ou les palissades s'arrêtent : explorer l'inconnu, découvrir des ressources, repousser les menaces ou nouer des alliances quand c'est possible. Et ramener à Port-Lointain ce que l'on ne peut pas cultiver : des réponses.

## Rappel : règles de combat aquatique
Use these rules for battles in water or underwater:

    You're off-guard unless you have a swim Speed.
    You gain resistance 5 to acid and fire.
    You take a –2 circumstance penalty to your attack roll for bludgeoning or slashing attacks that pass through water.
    Ranged attacks made by an underwater creature or against an underwater target have their range increments halved.
    You can't cast fire spells or use actions with the fire trait underwater. As normal for how traits work, any part of the effect that's unrelated to fire still works. For example, an attack with a flaming battle axe could still deal its physical damage, just not its fire damage.
    At the GM's discretion, some ground-based actions might not work underwater or while floating.

## Aperçu de la session
- Les PJ inspectent l'épave de la [[Clef d'Ecume]] avec deux objectifs :
	- Baliser des caisses marquées contenant des défenses pour la ville (armes de siège, munitions).
	- Comprendre comment/pourquoi le navire a coulé.
- Le [[Commandant Aelys Tarn]] équipe les PJ avec une ceinture de plomb et une potion de respiration aquatique (2h)
- Combats "modérés" à "sévère"  (les règles de combat aquatique imposent déjà un certain désavantage), pour 4 PJ de niveau 1 et un PJ de niveau 2.

## Scènes

### Scène 1 - Ordre de mission
Les PJs sont déjà sur un navire qui a jeté l'ancre au dessus de l'endroit estimé du naufrage. Le [[Commandant Aelys Tarn]] fait un briefing sur les objectifs de leur mission et fournit à chaque PJ :
- une ceinture de plomb
- une balise de téléportation
- une potion de respiration aquatique (durée: 2h environ)
- un **charme de voix-bulle** (effet intégré à la potion) : tant que la potion agit, les PJ peuvent **parler et s'entendre sous l'eau** à portée normale ; le son est *étouffé* au-delà de 18 m (60 ft) et ne traverse pas bien les cloisons.

> Le pont du navire roule lentement sur une houle froide. L’air sent le sel et la corde mouillée. Autour de vous, les matelots parlent bas et évitent de regarder trop longtemps l’eau.
> À tribord, une **bouée de repérage** danse au bout d’un cordage tendu ; plus loin, la **chaîne d’ancre** disparaît dans le gris sombre, comme si la mer l’avalait sans effort. Le capitaine a fait mettre le bâtiment à l’arrêt au-dessus d’un point précis, un endroit “vide” sur la carte… mais pas dans les esprits : c’est là, en dessous, que repose la [[Clef d'Ecume]].
> Vos ceintures de plomb attendent sur une bâche, alignées comme des menottes. À côté, les petites balises d’acier et les fioles prêtes à être débouchées. On ne vous a pas amenés ici pour contempler : on vous a amenés pour descendre.

> Aelys Tarn vous jauge un par un, le regard sec et précis. *"Éclaireurs. La **Clef d’Écume** est au fond depuis dix jours. Dix jours que Port-Lointain attend ces caisses — et dix jours que je n’ai que des suppositions pour expliquer pourquoi ce navire a disparu."*
> Elle fait signe à un matelot de pousser une caisse de démonstration. Dans sa main, une balise : une pointe d’acier gravée, coiffée d’une gemme pâle. *"Objectif un : **cinq caisses**, marquées **rouge et blanc**. Vous les localisez, vous plantez la balise dans le bois, et vous activez la gemme."* Elle appuie une fois — *clic*. *"Quand vous appuyez, vous comptez : **cinq secondes**. Pas quatre. Pas six. Et vous gardez vos doigts loin de ce qui se tord ou se met à bouger."* 5 secondes après avoir appuyé sur la gemme, la caisse disparaît et réapparaît cinq mètres plus loin sur le pont du navire. *"Voilà, ça enverra l'équipement directement jusqu'à nous."*
> *"Objectif deux : comprendre **pourquoi** la Clef d’Écume a coulé. Pas une histoire, pas une rumeur. Des faits. Si vous trouvez des signes d’une intervention… vous les notez, vous les décrivez, vous ne les interprétez pas sur place."*
> Elle pointe ensuite votre équipement, comme un inventaire de survie. *"La potion vous donne l’air — et vos voix. La ceinture vous donne le poids. Restez **à portée de main** les uns des autres. Si l’un de vous a un problème, il le dit tout de suite. Si quelqu’un panique et remonte comme une flèche, il ne meurt pas héroïquement : il meurt bêtement."*
> *"Vous descendez, vous travaillez vite, vous remontez proprement. Et vous revenez vivants. C’est un ordre."*

Puis les PJ peuvent sauter dans l'eau. Rappel des règles de nage (10m) et de combat aquatique, application de l'effet sur FoundryVTT.

> La surface se referme au-dessus de vous comme une porte qu’on claque. Pendant quelques secondes, il reste les reflets du ciel, les bulles qui s’échappent de vos vêtements, et la masse sombre de la coque au-dessus de vous.
> Vous luttez tous le plus longtemps possible pour ne pas prendre d'inspiration. C'est naturel. Mais le moment vient où vous n'avez plus le choix : il va vous falloir de l'air ou vous allez mourir ici, maintenant. **Faire faire un jet de volonté** et laisser chaque joueur interpréter son résultat, est-ce qu'il accepte que la potion va faire effet ? Est-ce qu'il se débat jusqu'au dernier moment, à en atteindre presque l’asphyxie ?
> Puis tout devient **vertical**. La ceinture vous tire vers le bas, régulière, implacable. Chaque battement de cœur semble plus lourd. Le froid s’insinue par les poignets, la nuque, sous les sangles. À mesure que vous descendez, la lumière ne baisse pas d’un coup : elle **s’éteint par étages**, comme des lanternes qu’on souffle les unes après les autres.
> La pression serre vos tempes. Vos oreilles protestent. Votre gorge avale de l’air qui n’en est pas vraiment, juste une habitude qu’on refuse de perdre. Vous parlez — et vos mots vous reviennent trop vite, trop proches, comme si l’eau refusait de leur donner de la distance.
> Autour de vous, la mer n’est plus un espace : c’est une **masse**. Un plafond au-dessus, un abîme au-dessous. Au loin, la chaîne de l’ancre descend comme une ligne de pendu dans le noir. Et quand vous regardez vers le haut, le monde d’en surface n’est déjà plus qu’une pièce de monnaie pâle, déformée par les vagues.
> Une dérive de **particules** vous traverse : fibres de cordage, éclats de bois, grains de sable en suspension.

**Combat 1 (extérieur, pendant la descente).** Dès que les PJ traversent la zone de débris en suspension (bois, cordages, sable), un prédateur opportuniste se rapproche.

*Option simple (rapide, létal mais gérable) :* **2 requins récifaux** (ou équivalent) + **banc de poissons carnivores** (swarm) si tu veux mettre la pression sur les lanceurs.

*Tactique :* les prédateurs font des passes, tentent de finir une cible isolée ; si un PJ est déjà blessé ou séparé du groupe, ils le prennent pour cible.

*Sortie propre :* après 3 rounds ou 1 requin tué, les prédateurs se dispersent si les PJ se regroupent et progressent vers l'épave.

### Scène 2 - La timonerie, les quartiers du capitaine et gaillard d'avant (upper deck)

Cette zone est constituée de l'extérieur du navire, de la gaillard d'avant, de la timonerie et des quartiers du capitaine. La gaillard d'avant et la timonerie contiennent également des escaliers qui descendent vers le pont principal (middle).

> L'épave de la **Clef d'Écume** apparaît d'abord comme une ombre couchée. Plus vous approchez, plus le bois se révèle : bordés fendus, cordages tendus comme des nerfs morts, algues accrochées aux bastingages.
> Le navire repose sur un fond de roche et de sable, incliné d'un côté.

#### Gaillard d'avant
Le gaillard d'avant est encombré de :
- un **guindeau** tordu (chaîne d'ancre encore engagée)
- des **râteliers vides** (armes légères emportées)
- une **grande brèche** superficielle sur bâbord (bois éclaté, comme frappé de l'intérieur)

> La proue grince doucement au rythme du courant. Le guindeau est figé, mangé de sel, et la chaîne d'ancre disparaît dans le noir sous la coque, comme si quelqu'un la tenait encore.

#### Timonerie
La timonerie contient :
- la **roue** (bloquée, corde de fortune nouée dessus)
- une **table de carte** renversée (parchemins dissous, compas brisé)
- une **cloche de bord** fêlée

> Derrière les vitres fendillées, la roue du navire est arrêtée en plein tour, ligotée à une corde comme si quelqu'un avait tenté de la retenir. La table de carte n'est plus qu'un chaos de bois et d'encre diluée.

#### Quartiers du capitaine
On trouve ici :
- le **corps du capitaine Odran Hellec**, coincé contre un meuble (mort depuis des jours)
- un **coffre de bord** fermé (effets personnels sans intérêt majeur, sauf si les PJ insistent)
- un **placard haut** (sec), où est rangée une **bouteille scellée** contenant un message
- des traces de **griffures** sur la porte intérieure (panique, lutte contre le manque d'air)

> Les quartiers du capitaine sont étonnamment intacts : un bureau vissé au plancher, une couchette, des cartes gonflées d'eau.
> Un corps flotte en suspension : c'est le **capitaine**, visage cireux, yeux ouverts sur rien. Ses doigts ont laissé des **marques** sur la porte, des ongles cassés sur le bois.
> Au-dessus du bureau, une bouteille bouchonnée attend en suspension.

*"Si quelqu'un lit ceci, c'est que la mer a fini par rendre la Clef d'Écume à la lumière."*
*"Je suis le capitaine **Odran Hellec**. Je n'ai survécu que parce qu'une poche d'air a tenu sous la timonerie. Cinq jours. Après, l'air a eu un goût de rouille et de tombe."*
*"Le jour suivant le naufrage, j'ai vu des silhouettes descendre depuis la surface : **robes sombres**, visages cachés, et surtout ces **chaînes noires** — pas des chaînes de marin. Des chaînes fines, portées comme un signe."*
*"Ils sont descendus droit vers le pont principale ou la cale. N'entendant pas ou ignorant mes appels au secours."*
*"Juste avant que le navire ne cède, pendant l'attaque des Mantes, il y a eu un **fracas** venu de la cale, et une **secousse** si forte que j'ai cru qu'un récif nous avait éventrés. Les robes sombres sont-elles allées voir ce qui a causé le naufrage ? Comment pourraient-elles savoir ? Je commence à me demander si le manque d'air ou si les profondeurs ne me rendent pas fou."*
*"— O. Hellec"*

### Scène 3 - Le pont principal (middle deck)

Cette zone contient des caisses de marchandises, renversées lors du naufrage, ainsi que les quartiers de l'équipage, le tout dans une grande zone ouverte. Une partie de l'équipement à téléporter est ici. Il y a aussi des Azarketi présents, en train de piller ce qu'ils peuvent (harpons, cordes, etc.)

> Le pont principal est une grande nef de bois noyée : des caisses éventrées, des tonneaux roulés contre les cloisons, des hamacs arrachés qui flottent comme des linceuls.
> Ici et là, des **bandes rouge et blanc** sur des caisses plus lourdes. Une caisse massive, éventrée, semblant être faite de bois et de métal, repose au fond du pont. Des corps de marin flottent au plafond et se balancent au gré des remous.
> Le silence est presque complet… sauf pour un cliquetis régulier : du métal qui heurte du métal.

#### Les Azarketi
> Des silhouettes vous observent depuis l'ombre des poutres : peau aux tons d'algues et de nacre, cheveux flottants comme des filaments, yeux immobiles. Ils se déplacent sans hésiter dans l'épave, avec des harpons courts et des filets.
> Ils n'ont pas l'air surpris de vous voir. Ils ont l'air… *agacés*, comme si vous veniez dans une maison dont ils ont déjà commencé à vider les tiroirs.

```pf2e-stats
# Ssaïl « Brise-Écume »
## Niveau 2
---

==Azarketi== ==Humanoïde==

Chef opportuniste d'une petite bande de récupérateurs. Ssaïl ne cherche pas la guerre : il cherche à **finir son pillage vivant**. Il respecte la force calme, déteste la panique et les gestes brusques.

**Perception** +8
**Athlétisme** +9, **Intimidation** +7, **Diplomatie** +6, **Survie** +7, **Larcin** +6
**Volonté** +7

---
**Historique** Né dans des courants côtiers de Nyssor, Ssaïl a appris à lire les épaves comme d'autres lisent les livres : où l'eau passe, où le bois cède, où les humains cachent les choses “importantes”.
**Apparence** Peau vert sombre marbrée, nageoires fines aux avant-bras, cicatrice pâle sur la joue. Porte des cordelettes de coquillages et un harpon court.
**Personnalité** Prudent, territorial.
**Oral, signe distinctif** Parle vite en Aquan (ou elfique archaïque), ponctue ses phrases de claquements de langue; garde toujours un œil sur les issues.

---
**Découverte** Survie DD 14 (c'est un récupérateur expérimenté), Société DD 15 (il a une logique “territoire/partage”), Perception DD 16 (il jauge les balises des PJ plus que leurs armes)
**Compétences d'influence** Diplomatie DD 17 (proposer un accord clair), Intimidation DD 18 (montrer qu'on ne recule pas), Survie DD 18 (parler courants/risques), Larcin DD 19 (parler de butin, cache, partage), Intimidation DD 20 (menacer son groupe)
**Influence 4.** Il laisse les PJ travailler sans interférence et indique les accès sûrs vers la cale.
**Influence 6.** Il décrit ce qu'il a vu après le naufrage : des humains en robes, avec des chaînes noires, venus inspecter la cage et fouiller.
**Influence 8.** Il restitue un petit objet trouvé dans les débris (au choix du MJ : fragment de plaque gravée, cire noire séchée, petit anneau marqué), au prix d'un échange.
**Résistances.** Promesses vagues (+2 DD), gestes agressifs vers son groupe (+3 DD), tentative de confiscation de son butin (+3 DD).
**Faiblesses.** Partage explicite ("vous prenez X, on prend Y") (-2 DD), offrir une corde/harpon/outil utile (-2 DD), démontrer discipline et calme (-2 DD).
```

#### La cage
Une grande cage, contenue dans ce qui reste d'une caisse, semble avoir été explosée de l'intérieur. Elle contenait le démon qui est responsable du naufrage.

> Au milieu de planches éclatées repose une cage d'acier et de bois cerclé, tordue. Le bois est gravé de l'intérieur, alternant runes et symboles mystérieux.

**Jets d'investigation (indices, subtils).**
- **Perception DD 14** : remarquer la cire noire sur les barreaux et des traces de gants (inspection “post-naufrage”).
- **Arcane DD 15** : comprendre que les balises/plaques sont un dispositif de **confinement** (scellement), pas une simple serrure.
- **Occultisme DD 15** : identifier une logique de *contrainte* et de *pacte* (pas un rituel “bienveillant”).
- **Religion DD 16** : associer l'iconographie de **chaîne/obéissance** à un courant dévot/hérétique lié à [[Tharun le Noir]] (sans nommer de cellule).
- **Artisanat DD 17** : voir qu'il manque une **pièce** (plaque/anneau d'ancrage) arrachée volontairement (cohérent avec la fouille des "chaînes noires").
- **Médecine DD 15** (si corps retrouvés ailleurs) : blessures incompatibles avec une noyade/attaque de mante : lacérations + brûlures froides/étranges (au choix).

### Scène 4 - La cale (lower deck)

Si les PJ descendent par l'avant (proue), alors ils tombent directement nez-à-nez avec le corps du bernard-l'hermite géant. Si les PJ descendent par l'arrière, ils peuvent également voir le corps du bernard-l'hermite, mais il y a également les dernières caisses restantes à téléporter ainsi que la caisse spéciale de la [[Ligue de Veyra]] (voir: "Mission spéciale" [[003 - Résultats d'intermède]]) contenant le codex.

**Arrivée par l'avant (proue).**
> L'escalier s'ouvre sur un vide où le navire n'est plus un navire : la cale est **béante**, ouverte sur la mer de part en part. Le courant y entre et en sort comme une respiration.
> Dans cette gorge de bois brisé, une masse pâle est coincée : une créature trop grande pour être là, immobile… puis une patte remue, soulevant un nuage de sable.

**Arrivée par l'arrière (poupe).**
> Ici, le plancher tient encore. De nombreuses caisses lourdes reposent contre une cloison, toutes marquées des différents symboles des factions de la Concorde, certaines marquées **rouge et blanc**. Plus loin, une brèche traverse toute la largeur du navire : un rideau de débris y danse, aspiré puis recraché. Dans cette brèche, une créature trop grande gratte le bois, comme s'il essayait de *s'installer*.

> [!statblocks|columns]
>>```pf2e-stats
>># Bernard-l'hermite des Épaves
>>## Créature 5
>>---
>>
>>==Grand== ==Animal== ==Aquatique==
>>
>>**Perception** +12; vision dans la pénombre
>>**Compétences** Athlétisme +15, Discrétion +10
>>**For** +5, **Dex** +1, **Con** +4, **Int** -4, **Sag** +2, **Cha** -2
>>---
>>**CA** 22; **Vig** +15, **Réf** +10, **Vol** +11
>>**PV** 95
>>---
>>**Vitesse** nage 30 ft, escalade 15 ft
>>
>>**Corps à corps** `[one-action]` Pince +16 (allonge 10 ft), **Dégâts** 2d10+7 contondants plus **Saisie**
>>**Corps à corps** `[one-action]` Patte +16 (agile), **Dégâts** 2d6+7 tranchants
>>---
>>```
>
>>```pf2e-stats
>>**Carapace verrouillée** `[one-action]`
>>Le bernard-l'hermite se cale contre une paroi ou le plancher (épave, roche). Jusqu'au début de son prochain tour, il gagne un **bonus de circonstances +2 à la CA** et une **résistance 5** aux dégâts physiques (sauf contondants). Il ne peut pas utiliser Patte pendant que cet effet est actif.
>>
>>---
>>
>>**Traction vers la brèche** `[reaction]`
>>**Déclencheur** Une créature commence son tour à 10 ft de la brèche (ou y est poussée/traînée).
>>
>>La cible doit réussir un jet de **Réflexes DD 20** ou être déplacée de 10 ft vers la brèche (Succès critique : aucun déplacement; Succès : 5 ft; Échec : 10 ft; Échec critique : 15 ft et tombe à terre/ballottée, à ton choix).
>>```

*Note MJ (terrain) :* dans la cale, ajoute 2 dangers simples :
- **courant/aspiration** (déplacement forcé vers la brèche, géré par la réaction ci-dessus)
- **débris flottants** : à l'entrée en zone de brèche, **Acrobaties ou Athlétisme DD 17** sinon 1d6 dégâts contondants et off-guard 1 round.

### Scène 5 - Retour à la surface

> La remontée est plus longue que la descente. Votre souffle est régulier, mais le corps, lui, comprend : chaque mètre rend la lumière plus vive, et l'eau plus légère.
> Quand la surface vous reprend, l'air est froid et brutal. On vous hisse à bord avec des cordes. Sur le pont, le commandant Tarn vous attend, trempée par les embruns.
> *"Bon travail. Vous venez d'offrir des jours de survie à cette ville."* Elle prend le rapport, les yeux sur vous, pas sur l'horizon. *"Et maintenant dites-moi ce qui a coulé ce navire."*

## A garder sous la main

Créatures aquatiques PF2e (idées de rencontres rapides) :
- Requins (reef shark / shark) : https://2e.aonprd.com/Search.aspx?q=reef%20shark
- Anguille électrique : https://2e.aonprd.com/Search.aspx?q=electric%20eel
- Murène géante : https://2e.aonprd.com/Search.aspx?q=moray
- Poulpe géant : https://2e.aonprd.com/Search.aspx?q=giant%20octopus
- Banc carnivore / essaim : https://2e.aonprd.com/Search.aspx?q=swarm%20fish
- Crabe géant (base à ajuster) : https://2e.aonprd.com/Search.aspx?q=giant%20crab


## Événements / Décisions
- 

## Rumeurs
- **La Maison-Coquillage (NW).** Au nord-ouest, une *maison faite d’une coque géante* servirait de porte d’entrée à des ruines pleines d’un trésor immense ; personne n’en revient sans parler de **Pince-vive**, un crabe géant qui “garde l’escalier”.
- **Le « goulet qui respire ».** Des marins jurent qu’il existe, près de la côte, une faille sous-marine qui aspire puis recrache l’eau par à-coups ; ceux qui s’y font prendre reviennent avec des bleus… ou pas du tout.
- **La cloche sous les vagues.** Par mer calme, certains entendent une cloche lointaine “sonner” sous l’eau au large ; les vieux loups de mer conseillent de ne pas suivre le son, même avec une corde.

## Butin / Récompenses
Propositions :
- **Boulet siffleur** (objet trivial, rigolo) : un boulet percé qui émet un sifflement sinistre quand on le fait tourner/rouler ; sert aussi de presse-papier ou de signal sonore (à toi de voir si tu lui donnes une petite utilité narrative).
- **Boussole du Naufragé** (objet 3) : worn; **+1 bonus d'objet à Survie** pour *S'orienter* / *Ne pas se perdre* et pour Estimer un courant/une météo.
- **Journal du Capitaine Odran Hellec** (objet 2 ou 3) : lecture/feuillet scellé; **+1 bonus d'objet à Connaissances (Lore) Navigation** (ou *Lore Logistique*) et permet de *Recall Knowledge* sur routes/manifestes même sans carte.
- **Potion de nage** (objet 2, officiel) : donne une **vitesse de nage** pendant 1 heure (ou selon la version utilisée) : https://2e.aonprd.com/Search.aspx?q=swimming%20potion

## À reporter / Prépa prochaine
- 
