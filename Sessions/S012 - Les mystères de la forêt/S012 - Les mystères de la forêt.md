---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 12
code: S012
date_irl: 2026-04-26
fc-date: 16/06/42
fc-end: 16/06/42
resume: ""
pjs:
  - "[[Campagnes/EFG/PJ/Voss Vitriox.md|Voss Vitriox]]"
  - "[[Campagnes/EFG/PJ/Yoko.md|Yoko]]"
  - "[[Campagnes/EFG/PJ/Théobald Greyheart.md|Théobald Greyheart]]"
  - "[[Campagnes/EFG/PJ/Lyra.md|Lyra]]"
  - "[[Campagnes/EFG/PJ/Fenn Brindebois.md|Fenn Brindebois]]"
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


## Demande des joueurs

> Mes chers compagnons, Nous souhaitons avec [[Fenn Brindebois]] approfondir les recherches dans la forêt au Sud Ouest. Afin de lever le mystère sur cette créature (le minotaure) que vous avez rencontré.
> - [[Yoko]]

La référence est pour la session [[S007 - Piste au sud-ouest]] et ils cherchent à trouver les cultistes de [[Les Chaines d'Ombre]], sans savoir que leur campement n'est pas dans la forêt mais à l'ouest sur la côte à [[Tharumar]].

## TODO

- [ ] Préparer carte/battlemap du campement-relais
- [ ] Préparer rencontre 1 : sentinelles / occultistes de lisière
- [ ] Préparer rencontre 2 : rituel de réinvocation du [[Le limier d'Ether]]
- [ ] Préparer notes, carte et ordre de transit vers [[Tharumar]]
- [ ] Préparer questions/réponses si un cultiste est capturé
- [ ] Préparer les statblocks PF2e des cultistes retenus
- [ ] Préparer un statblock PNG d'influence

Idées statblocks :
- https://2e.aonprd.com/NPCs.aspx?ID=3532
- https://2e.aonprd.com/NPCs.aspx?ID=3537
- https://2e.aonprd.com/NPCs.aspx?ID=3535
- https://2e.aonprd.com/NPCs.aspx?ID=3534

## Beats

## Intro

> Les dernières heures de marche ont laissé derrière vous les sentiers praticables et les bruits familiers des éclaireurs de [[Port-Lointain]]. Ici, la forêt du sud-ouest étouffe le vent sous ses branches noires et ses troncs serrés. L'odeur de résine humide se mêle à autre chose : la cendre froide, l'huile brûlée, et ce parfum sec de corde goudronnée qu'on n'attend pas si loin des quais.
> Entre les arbres, une lueur basse filtre par à-coups. Pas un feu de bivouac franc, pas la chaleur d'un camp de chasseurs. Plutôt quelque chose de couvert, de contenu, de volontairement discret.
> En avançant encore, vous distinguez enfin le camp : quelques tentes sombres, des caisses, des piquets noirs plantés en cercle, et des silhouettes en robe qui bougent sans parler plus haut qu'un murmure. Ce n'est pas un repaire de fortune. C'est un relais. Et quoi qu'ils fassent ici, ils ont déjà commencé.

### Beat 1 — La lisière du camp

**Objectif :** ouvrir vite, identifier le culte, lancer l'alerte.

À l'entrée du campement, les PJ tombent sur une petite cellule avancée : sentinelles ou occultistes occupés à décharger du matériel, surveiller le couvert, ou transporter des seaux de cendres noires vers l'intérieur du camp.

**Ce que les PJ voient tout de suite :**
- des robes sombres sans emblème visible de loin ;
- des chaînes noires portées comme marque de dévotion ;
- des caisses légères, des cordages huilés, des couvertures épaisses pour emballer des objets fragiles ;
- un calme discipliné, presque religieux.

> Vous écartez les dernières branches basses et tombez sur une clairière étroite, artificiellement dégagée. Deux silhouettes encapuchonnées se tiennent près d'un tronc abattu, une troisième va et vient entre une caisse ouverte et un petit brasero couvert. Des chaînes noires pendent à leurs poignets et à leur ceinture, ternes, sans éclat. Tout ici semble pensé pour être démonté vite et sans laisser grand-chose derrière soi.

**Dialogue possible si les cultistes repèrent les PJ :**
- *"Qui va là ?"*
- *"Reculez. Ce lieu n'est pas pour vous."*

**Cri d'alerte si le combat tourne mal :**
- *"Intrus ! Vite — terminez le rituel !"*
- *"Achevez le lien ! Qu'il revienne avant qu'ils n'entrent !"*

**Transition :** ce cri lance la pression. Les PJ entendent ensuite, plus loin dans le camp, des voix qui montent enfin au-dessus du murmure.

---

### Beat 2 — Le cœur du camp révélé

**Objectif :** montrer clairement l'enjeu avant la grande rencontre.

Après la première escarmouche, les PJ débouchent sur le vrai centre du relais : une zone rituelle semi-cachée au fond de la clairière, à l'abri d'un surplomb rocheux ou de grands pins.

**Éléments de décor importants :**
- un cercle de cendre noire mélangée à du sang séché ;
- des chaînes tendues entre des piquets noirs gravés ;
- un foyer couvert où rougeoient des braises blanches ;
- des caisses déjà refermées ou vides, dont l'une porte encore l'empreinte d'un objet circulaire retiré récemment ;
- des feuillets, tablettes ou planches de notes techniques et cultuelles.

> Le fond du camp s'ouvre sous un rideau de branches taillées. Là, le silence discipliné de la lisière laisse place à une tension plus nue. Un cercle de cendre a été tracé au sol, épais comme une tombe remuée. Des chaînes noires relient des piquets gravés à un brasero couvert, et dans la chaleur étouffée qui s'en dégage, la cendre semble parfois respirer.
> Une caisse doublée de feutre repose ouverte sur une table basse. Son intérieur garde la marque nette d'un objet rond, lourd, déjà retiré. Tout autour, des silhouettes en robe noire s'activent enfin avec urgence.

**Ce que les PJ peuvent comprendre avant d'agir :**
- le camp n'est pas une base durable mais un relais temporaire ;
- un objet important a déjà quitté les lieux ;
- les cultistes sont en train de tenter de refaire venir quelque chose à partir des cendres.

**Dialogue possible des officiants :**
- *"Le passage vers [[Tharumar]] est déjà en route. Tenez le lien."*
- *"Sans limier, la piste redevient aveugle. Continuez."*
- *"Ne laissez pas les cendres refroidir."*

---

### Beat 3 — Rencontre principale : le rituel du limier

**Objectif :** affrontement central de la soirée.

Les PJ interviennent pendant que les officiants cherchent à **réinvoquer / reforger** le lien démoniaque du [[Le limier d'Ether]].

**Intentions des cultistes :**
- achever le rituel ;
- protéger les notes et les repères de piste ;
- si besoin, fuir avec ce qui reste exploitable vers la côte.

**Actions possibles des PJ :**
- foncer sur les officiants ;
- briser le cercle ou les piquets ;
- disperser les cendres ;
- voler les notes ;
- tenter de capturer un survivant.

> Les officiants lèvent enfin la voix. Leurs mots ne ressemblent pas à un chant, mais à une suite d'ordres murmurés à quelque chose qui hésite encore à obéir. Dans le cercle, les cendres s'amassent, retombent, puis se soulèvent à nouveau comme sous un souffle qui n'appartient à personne. Une odeur de métal chauffé et de chair brûlée vous prend à la gorge.
> Au centre, la forme n'est pas encore un corps. Seulement une promesse de cornes, de braise et de colère tenue ensemble par la chaîne, la volonté et la peur.

**Répliques possibles de l'officiant principal :**
- *"Le premier lien a été brisé ; nous le forgeons de nouveau."*
- *"Vous avez retardé l'œuvre, rien de plus."*
- *"Tenez-les ! Même incomplet, il suffira !"*

**Si le rituel dérape ou s'achève partiellement :**
- *"Non… pas ainsi… maintenez-le !"*
- *"Qu'il chasse, même boiteux ! Qu'il morde, même brisé !"*

---

### Beat 4 — Le camp après le sang

**Objectif :** laisser souffler, fouiller, comprendre.

Une fois le combat terminé ou le rituel interrompu, le camp devient une scène d'investigation rapide. Les PJ peuvent fouiller, lire, comparer les éléments, et éventuellement sécuriser un prisonnier.

> Quand les derniers cris retombent, il ne reste plus dans la clairière que le grésillement du brasero couvert, le tintement léger des chaînes agitées par le vent, et cette odeur de cendre mouillée qui colle aux vêtements. Maintenant que plus personne ne protège l'ordre du camp, son sens apparaît mieux : rien ici n'était fait pour durer, tout était fait pour passer, transporter, réveiller, puis disparaître.

**Éléments à mettre sous leurs yeux :**
- une carte ou un croquis côtier incomplet ;
- une caisse vide rembourrée ayant contenu un objet circulaire ;
- un ordre de transit ou une note sur une “troisième borne” ;
- des repères de piste, listes de matériel, comptes de jours ;
- une prière / doctrine sur l'obéissance et le lien.

---

### Beat 5 — Interrogatoire et cliffhanger vers [[Tharumar]]

**Objectif :** finir la soirée sur une révélation exploitable pour une prochaine session.

Si les PJ capturent un cultiste vivant, ils peuvent obtenir le nom du culte, la nature du relais, et surtout l'information que l'objet important a déjà été expédié vers [[Tharumar]], où plusieurs pièces anciennes sont en cours d'assemblage.

> Le prisonnier garde le silence tant qu'il le peut, lèvres serrées, regard fixe, comme s'il attendait un ordre qui ne viendra plus. Mais autour de lui, le camp parle déjà presque autant que lui : la caisse vide, les notes tachées, les repères de route, la cendre encore tiède.
> Lorsqu'il cède enfin, ce n'est pas par peur seule. C'est par rage froide d'avoir été interrompu si près du but.

**Répliques possibles du cultiste capturé :**
- *"Ce camp n'est rien. Une halte. Un seuil."*
- *"Vous êtes en retard. Ce qui comptait a déjà pris la route."*
- *"À [[Tharumar]], les pièces seront unies. Ici, nous ne faisions que garder le passage et refaire venir le limier."*
- *"Nous sommes les [[Les Chaines d'Ombre]]. Vous ne connaissez encore que nos traces."*

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
