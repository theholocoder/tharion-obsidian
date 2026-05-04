---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 12
code: S012
date_irl: 2026-04-26
fc-date: 16/06/42
fc-end: 16/06/42
resume: Les PJ découvrent un camp de cultistes près d'une grotte où l'on entendait des voix. En fouillant, ils trouvent une caisse doublée destinée à contenir un objet rond, une carte montrant un itinéraire lié à Port Lointain et des robes/chaînes de cérémonie. Déguisés en cultistes/prisonniers, ils infiltrent la grotte ; le rituel d'invocation démarre mais est perturbé par un combat violent où Biscotte et Crunch attaquent, plusieurs cultistes sont tués, Lyra et Yoko sont grièvement blessés (stabilisés/soignés ensuite), et le collier attrapé par Biscotte est jeté dans le bassin (fait progresser le rituel). Grâce aux actions combinées, le rituel échoue et la manifestation (Minotaure/démon) se dissipe ; le groupe récupère équipements et indices laissant des pistes vers Port Lointain et un point côtier.
pjs:
  - "[[Campagnes/EFG/PJ/Voss Vitriox.md|Voss Vitriox]]"
  - "[[Campagnes/EFG/PJ/Yoko.md|Yoko]]"
  - "[[Campagnes/EFG/PJ/Théobald Greyheart.md|Théobald Greyheart]]"
  - "[[Campagnes/EFG/PJ/Lyra.md|Lyra]]"
  - "[[Campagnes/EFG/PJ/Fenn Brindebois.md|Fenn Brindebois]]"
updated: 2026-04-26
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


## Demande des joueurs

> Mes chers compagnons, Nous souhaitons avec [[Fenn Brindebois]] approfondir les recherches dans la forêt au Sud Ouest. Afin de lever le mystère sur cette créature (le minotaure) que vous avez rencontré.
> - [[Yoko]]

La référence est pour la session [[S007 - Piste au sud-ouest]] et ils cherchent à trouver les cultistes de [[Les Chaines d'Ombre]], sans savoir que leur campement n'est pas dans la forêt mais à l'ouest sur la côte à [[Tharumar]].

## Intro

> Les dernières heures de marche ont laissé derrière vous les sentiers praticables et les bruits familiers des éclaireurs de [[Port-Lointain]]. Ici, la forêt du sud-ouest étouffe le vent sous ses branches noires et ses troncs serrés. L'odeur de résine humide se mêle à autre chose : la cendre froide, l'huile brûlée, et ce parfum sec de corde goudronnée qu'on n'attend pas si loin des quais.
> Entre les arbres, une lueur basse filtre par à-coups. Pas un feu de bivouac franc, pas la chaleur d'un camp de chasseurs. Plutôt quelque chose de couvert, de contenu, de volontairement discret.
> Quelques tentes sombres sont dressées. Des caisses, des cordages, des bâches épaisses, un brasero couvert dont la chaleur ne se voit qu'à peine sont éparpillés. Le sol est marqué par des piquets noirs, des chaînes sombres et des traces de cendre. Rien n'a l'air laissé au hasard.
> Au fond, derrière le campement, vous apercevez une paroi rocheuse avec l'entrée d'une grotte. Et surtout, il manque quelque chose. Personne ne bouge. Personne ne parle. Le camp est là, intact, mais vide.

## Beats
### Beat 1 — Le camp désert

**Objectif :** arrivée, lecture du lieu, premiers indices.

Les PJ arrivent devant le campement-relais des cultistes, mais il est désert. Tout indique pourtant une activité récente : le brasero est encore tiède, les tentes sont en place, les chaînes et piquets rituels n'ont pas été démontés, et plusieurs éléments logistiques montrent qu'un départ n'a eu lieu que très récemment.

**Ce que les PJ peuvent inspecter tout de suite :**
- les tentes sombres, austères et montées pour un séjour court ;
- les caisses, bâches et cordages de transport ;
- une caisse vide doublée de feutre ayant contenu un objet rond et précieux ;
- les piquets noirs et chaînes sombres plantés entre le camp et les menhirs ;
- des traces allant vers l'ouverture dans la roche.

> Vous avancez entre les tentes sans croiser âme qui vive. Le camp n'a rien d'abandonné depuis des jours ; au contraire, tout semble avoir été utilisé il y a peu. Les bâches sont encore tendues proprement, une caisse est restée ouverte, le brasero garde une chaleur sourde sous sa cendre, et le sol porte assez de passages pour dire qu'on travaillait ici encore récemment.
> Entre les tentes et les menhirs, les piquets noirs et les chaînes sombres marquent une zone préparée avec soin. Plus loin, au pied de la paroi rocheuse, des traces de bottes, de cendre traînée et de matériel déplacé convergent toutes vers une ouverture sombre dans la pierre.

**Ce que les PJ peuvent comprendre :**
- le camp n'est pas un lieu de vie durable, mais un relais ;
- un objet important a déjà quitté les lieux ;
- le vrai cœur de l'activité n'était probablement pas dans la clairière ;
- les cultistes sont ou étaient retranchés dans la roche derrière le camp.

---

### Beat 2 — La grotte du rituel

**Objectif :** confrontation principale de la soirée, avec possibilité de discussion avant le combat.

Les indices du camp mènent à l'ouverture dans le promontoire rocheux. À l'intérieur, les PJ tombent rapidement sur les premiers cultistes, qui donnent l'alerte. Il n'y a pas de vraie séparation entre première escarmouche et rencontre principale : dès que les PJ pénètrent dans la grotte, tout s'enchaîne vers la salle rituelle.

Les cultistes ne veulent pas interrompre le rituel, mais ils ne cherchent pas non plus à mourir inutilement. S'ils pensent pouvoir gagner du temps, intimider les PJ, négocier un repli ou détourner leur attention, ils essaieront de parler avant d'engager le combat.

**Éléments de décor importants :**
- un couloir de roche humide où la lumière meurt vite ;
- des traces de cendre, de bottes et de chaînes traînées ;
- une cavité principale transformée en salle rituelle ;
- un cercle de cendre noire mélangée à du sang séché ;
- des chaînes tendues entre pitons, piquets ou pierres anciennes ;
- un foyer couvert où rougeoient des braises blanches ;
- des notes, tablettes et matériel rituel.

> Vous entrez dans la grotte. L'air y est plus lourd, chargé de fumée froide et d'une odeur de cendre rance. Plus loin, un éclat rougeâtre danse sur les parois, accompagné d'un cliquetis de chaîne et de voix basses récitant des prières.
> Quand vous débouchez sur la cavité principale, le lieu ne laisse plus de doute. Les cultistes ont installé un rituel au cœur même de la roche : cendres noires au sol, chaînes tendues, braises rougeoiyantes, et au fond une sorte de portail brûlant.

**Ce qui se passe ici :**
- les premiers cultistes rencontrés dans la grotte donnent l'alerte ;
- le timer du rituel peut démarrer à partir de ce moment-là ;
- toute la rencontre se joue sur la même battlemap / même zone de grotte ;
- les cultistes cherchent à **réinvoquer / reforger** le lien démoniaque du [[Le limier d'Ether]].

**Ouverture sociale possible :**
- les cultistes ordonnent d'abord aux PJ de partir ;
- ils peuvent prétendre protéger un lieu sacré, ou n'être que de simples pèlerins ;
- ils peuvent proposer aux PJ de reculer et d'oublier ce qu'ils ont vu ;
- pendant qu'ils parlent, ils cherchent surtout à gagner du temps pour le rituel.

**Intentions des cultistes :**
- gagner du temps si la parole peut suffire ;
- achever le rituel ;
- protéger les notes et les repères de piste ;
- si besoin, fuir avec ce qui reste exploitable vers la côte.

**Actions possibles des PJ :**
- tenter d'ouvrir un dialogue ;
- bluffer, menacer ou diviser les cultistes ;
- foncer sur les officiants ;
- briser le cercle ou les piquets ;
- disperser les cendres ;
- voler les notes ;
- tenter de capturer un survivant.

> Les officiants lèvent enfin la voix. Leurs mots ne ressemblent pas à un chant, mais à une suite d'ordres murmurés à quelque chose qui hésite encore à obéir. Dans le cercle, les cendres s'amassent, retombent, puis se soulèvent à nouveau comme sous un souffle qui n'appartient à personne. Une odeur de métal chauffé et de chair brûlée vous prend à la gorge.
> Au centre, la forme n'est pas encore un corps. Seulement une promesse de cornes, de braise et de colère tenue ensemble par la chaîne, la volonté et la peur.

**Répliques possibles au moment de l'alerte :**
- *"Intrus. Restez où vous êtes."*
- *"Encore un pas et vous mourrez pour une chose que vous ne comprenez pas."*
- *"Terminez le rituel. Je les retiens."*

**Répliques possibles de l'officiant principal :**
- *"Vous n'avez rien vu. Faites demi-tour, et vous sortirez vivants."*
- *"Ce lieu ne vous concerne pas. Partez maintenant."*
- *"Vous croyez interrompre un crime ; vous ne faites que retarder une nécessité."*
- *"Le premier lien a été brisé ; nous le forgeons de nouveau."*
- *"Vous avez retardé l'œuvre, rien de plus."*
- *"Le passage vers [[Tharumar]] est déjà en route. Tenez le lien."*
- *"Sans limier, la piste redevient aveugle. Continuez."*
- *"Tenez-les ! Même incomplet, il suffira !"*

**Déclencheurs de combat évidents :**
- les PJ avancent vers le cercle ;
- les PJ touchent aux cendres, aux notes ou aux piquets ;
- les PJ refusent de reculer après sommation ;
- les cultistes estiment avoir assez gagné de temps.

**Si le rituel dérape ou s'achève partiellement :**
- *"Non… pas ainsi… maintenez-le !"*
- *"Qu'il chasse, même boiteux ! Qu'il morde, même brisé !"*

---

### Beat 3 — Fouille finale / interrogatoire

**Objectif :** révélation finale et crochet vers la suite.

Une fois les cultistes vaincus ou dispersés, les PJ peuvent fouiller le camp, fouiller la grotte, lire les notes, et interroger un survivant. C'est ici qu'ils comprennent que ce site n'était qu'un relais secondaire et que l'élément le plus important a déjà quitté les lieux.

> Quand le vacarme retombe, il ne reste plus que le souffle des braises, l'odeur de pierre humide et de cendre brûlée, et ce léger tintement des chaînes quand quelqu'un bouge encore. Entre le camp vide dehors et la grotte profanée derrière, l'ensemble prend enfin sens : ici, rien n'était fait pour durer. Seulement pour cacher, attendre, puis repartir.
> Et ce qu'ils gardaient vraiment n'est déjà plus là.

**Éléments à mettre sous leurs yeux :**
- une carte ou un croquis côtier incomplet ;
- une caisse vide rembourrée ayant contenu un objet circulaire ;
- un ordre de transit ou une note sur une “troisième borne” ;
- des repères de piste, listes de matériel, comptes de jours ;
- une prière / doctrine sur l'obéissance et le lien.

> Le prisonnier garde le silence tant qu'il le peut, lèvres serrées, regard fixe, comme s'il attendait un ordre qui ne viendra plus. Mais autour de lui, le camp parle déjà presque autant que lui : la caisse vide, les notes tachées, les repères de route, la cendre encore tiède.
> Lorsqu'il cède enfin, ce n'est pas par peur seule. C'est par rage froide d'avoir été interrompu si près du but.

**Répliques possibles du cultiste capturé :**
- *"Ce camp n'est rien. Une halte. Un seuil."*
- *"Vous êtes en retard. Ce qui comptait a déjà pris la route."*
- *"À [[Tharumar]], les pièces seront unies. Ici, nous ne faisions que garder le passage et refaire venir le limier."*
- *"Nous sommes [[Les Chaines d'Ombre]]. Vous ne connaissez encore que nos traces."*

**Cliffhanger conseillé :**
Le prisonnier, la carte, ou l'ordre de transit confirment tous la même chose : un **artefact plus grand** est en cours d'assemblage à [[Tharumar]] à partir de plusieurs composants anciens, et les PJ ne viennent d'interrompre qu'un relais secondaire du plan.

## Indices / Pistes

### Indices trouvables dans le camp

| Indice | Où / comment | Ce que ça révèle | Vers quoi cela mène |
| --- | --- | --- | --- |
| Caisse vide doublée de feutre, marquée par un objet circulaire | Table de travail, tente de stockage | Un objet précieux et fragile a quitté le camp récemment | Qu'un composant important est déjà parti vers [[Tharumar]] |
| Carte sommaire de la forêt et de la côte | Sous une caisse, dans la tente de l'officiant | Le camp est un relais de passage, pas une base | Une prochaine mission vers [[Tharumar]] |
| Ordre de transit mentionnant “troisième borne”, “charge prioritaire”, ou “remise à l'ouest” | Notes de logistique, tablette cirée, parchemin plié | Les cultistes suivent une route structurée | Qu'il existe un trajet organisé entre forêt et côte |
| Piquets noirs gravés reliés par des chaînes | Cercle rituel | Le culte mélange rituel et contrôle démoniaque | Le rôle précis du camp : réinvoquer un garde-piste |
| Cendres épaisses mêlées à des restes d'ossements calcinés | Centre du cercle | Ils essaient de refaire venir le [[Le limier d'Ether]] détruit en [[S007 - Piste au sud-ouest]] | Le lien direct avec la session 7 |
| Litanie ou prière à l'obéissance, au lien et au silence | Autel discret, bande de tissu, tablette | Il s'agit bien d'un culte structuré, pas de simples brigands | Le nom et la doctrine des [[Les Chaines d'Ombre]] |
| Liste de matériel : huile, sel, cordage, couvertures, piquets | Zone logistique | Les séjours sont courts et méthodiques | Le camp fonctionne en relais temporaire |
| Note sur une “lentille” ou une “charge déjà expédiée” | Feuillet de supervision, sac de l'officiant | L'objet n'est plus ici | Qu'un composant d'artefact est en route ou déjà arrivé à [[Tharumar]] |

### Indices obtenus par interrogatoire

| Question / angle | Ce qu'un acolyte peut dire | Ce qu'un officiant ou survivant mieux informé peut dire | Ce vers quoi ça mène |
| --- | --- | --- | --- |
| Qui êtes-vous ? | *"Les [[Les Chaines d'Ombre]]."* | *"Nous lions ce qui doit obéir."* | Identification du culte |
| Que faisiez-vous ici ? | *"Nous gardions le passage."* | *"Nous reforgions le lien du limier."* | Le camp est un relais et un site rituel secondaire |
| Qu'est-ce que vous invoquiez ? | *"Le limier."* | *"Le même lien, le même chasseur, une nouvelle chair si nécessaire."* | Confirmation du retour du [[Le limier d'Ether]] |
| Pourquoi la forêt ? | *"On n'y reste jamais longtemps."* | *"La forêt cache les routes, pas notre œuvre."* | Le vrai centre n'est pas dans les bois |
| Qu'est-ce qui a quitté le camp ? | *"Une charge. Je ne l'ai pas vue de près."* | *"Une lentille gravée. Priorité absolue."* | Un composant majeur a déjà été convoyé |
| Où est partie cette charge ? | *"Vers l'ouest."* | *"Vers [[Tharumar]]."* | Crochet direct vers la prochaine session |
| Pourquoi est-ce si important ? | *"Ordre du Premier Enchaîné."* | *"Les pièces doivent être réunies. Ici, nous ne tenions qu'un maillon."* | Qu'un artefact plus grand est en cours d'assemblage |
| Qui commande ? | *"Un officiant. Je ne sais pas plus."* | *"Le Premier Enchaîné reçoit les pièces."* | Préfigure [[Valdris Nuévite]] sans tout révéler |

## Butin / Récompenses
- Notes du camp des [[Les Chaines d'Ombre]]
- Carte / croquis menant vers la côte et [[Tharumar]]
- Matériel rituel récupérable ou revendable selon ton arbitrage
- Éventuel prisonnier cultiste transférable à [[Port-Lointain]] pour interrogatoire ultérieur

## À reporter / Prépa prochaine
- [[Tharumar]] comme prochaine piste majeure
- Déterminer ce qu'est exactement la “lentille gravée” et son lien avec l'artefact en cours d'assemblage
- Conséquences si un cultiste capturé parle au [[Conseil de la Brèche]] ou au [[Commandant Aelys Tarn]]
- Déterminer si le rituel a été complètement stoppé, partiellement réussi, ou seulement retardé

## Suivi par PJ (rapide)

| PJ                     | Faction                    | Conditions | Notes          |
| ---------------------- | :------------------------- | ---------- | -------------- |
| [[Fenn Brindebois]]    | [[Royaume d'Halvorn]]      | -          | -              |
| [[Lyra]]               | [[République de Thaldris]] | -          | 15pv, blessé 2 |
| [[Théobald Greyheart]] | [[Ligue de Veyra]]         | -          | 15pv           |
| [[Voss Vitriox]]       | [[Ligue de Veyra]]         | -          | 5pv            |
| [[Yoko]]               | [[Royaume d'Halvorn]]      | -          | 5pv, blessé 2  |
