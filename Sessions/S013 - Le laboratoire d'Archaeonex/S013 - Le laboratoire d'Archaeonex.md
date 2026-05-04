---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 13
code: S013
date_irl: 2026-05-04
fc-date: ""
fc-end: ""
resume: ""
pjs: []
updated: 2026-05-04
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

- [ ] Définir la composition exacte de la patrouille cisarelle pour 3 PJ de niveau 3.
- [ ] Mettre à jour la map de la grotte / mine d'[[Archaeonex]] avec l'avancée des prospecteurs et le début d'exploitation du fer.
- [ ] Définir la recette alchimique anti-communication cisarelle trouvée dans le laboratoire.
- [ ] Définir le détail mécanique du composant rare : champignon poussant sur les troncs calcinés du territoire cisarelle.
- [ ] Définir une piste / récompense spécifique pour le psychiste afin de sentir ou perturber les communications cisarelles.
- [ ] Rédiger la description du laboratoire d'[[Archaeonex]].
- [ ] Rédiger le passage narratif des visions du cristal d'éther au retour chez [[Archaeonex]].
- [ ] Préparer le timer visible de patrouille cisarelle et ses conséquences à chaque passage.
- [ ] Créer dans Foundry VTT les objets, recettes, indices et éléments interactifs utiles à la session.

## Intro

> Les PJ repartent vers l'ancien refuge d'[[Archaeonex]], en plein territoire des [[Cisarelles]], pour récupérer son [[Fil-Mémoire]] laissé derrière lors du raid qui a ravagé sa couvée. La mission doit rester courte et tendue : infiltration légère, pression du territoire, peu de combat, mais un vrai risque si les PJ traînent ou se font repérer.
>
> L'objectif apparent est simple : entrer, récupérer le fil, sortir. Mais dans les profondeurs du refuge se cache un laboratoire organique secret où [[Archaeonex]] menait des expériences sur l'isolement d'une Cisarelle hors du [[Psylith]]. Les PJ peuvent y découvrir un protocole de brouillage local des communications cisarelles… et, s'ils ramènent le fil à [[Archaeonex]], obtenir ensuite la vérité sur l'identité de cette captive : la future [[Golgotha, la Mère des Chairs]].

## Beats
- ### Scène 1 — Approche du territoire calciné
  > Les arbres ne sont plus que des colonnes noires, fendues par la chaleur ancienne. La cendre étouffe les pas, accroche les bottes, et le silence ici n'est jamais complet : il est traversé de cliquetis lointains, de froissements secs, comme si quelque chose passait d'un tronc calciné à l'autre juste hors de vue. Sur certains bois brûlés poussent des excroissances fongiques sombres, en couronnes irrégulières, comme si la terre elle-même avait appris à vivre dans la brûlure.

  **Description prête à lire — trouver l'entrée**
  > Plus vous progressez dans la cendre, plus la piste cesse d'en être une. Ce ne sont plus des traces franches, mais une série de détails ténus : un filament gris coincé dans l'écorce noire d'un tronc, une rainure trop nette sur une pierre brûlée, une zone où la cendre a été remuée à plusieurs reprises puis laissée retomber. En suivant ces indices, vous finissez par distinguer une faille sombre entre deux parois fendues, à moitié masquée par des lambeaux de soie morte et par l'ombre des roches calcinées. L'entrée n'a rien d'évident. Sans savoir quoi chercher, vous seriez passés devant.

  **But de la scène**
  - Poser l'ambiance du territoire cisarelle.
  - Installer le timer de patrouille.
  - Laisser les PJ choisir leur approche : prudente, rapide, guidée, ou improvisée.

  **Informations que les PJ peuvent trouver**
  - Le territoire est régulièrement parcouru par des patrouilles cisarelles.
  - Les troncs calcinés portent les champignons liés à la future recette alchimique, mais cette session n'est pas une mission de récolte.
  - Le psychiste peut percevoir une impulsion télépathique diffuse, signe qu'ils pénètrent dans une zone sous surveillance du [[Psylith]].
  - L'entrée du refuge n'est pas visible de loin ; elle est cachée dans une faille rocheuse noircie, à demi bouchée par de la soie morte et des débris brûlés.
  - Pour la trouver, les PJ doivent remonter une combinaison d'indices : ancienne soie arachnomorphe accrochée aux troncs, traces du raid initial, passages cisarelles plus récents, et zones de cendre troublée menant vers une paroi fendue.

  **Jets possibles**
  - **Survie** : choisir une approche plus discrète, lire les traces, éviter un axe de patrouille, remonter la piste jusqu'à la bonne zone.
  - **Perception** : repérer un passage récent de Cisarelles, une zone moins exposée, un bon couvert avant l'entrée, distinguer la faille noire des autres fractures de la roche.
  - **Nature** : remarquer les champignons sur bois brûlé et comprendre qu'ils ne sont pas ordinaires.
  - **Diplomatie / Société / Connaissance locale** si les PJ ont pensé à solliciter [[Tisse-Chef Krux]] avant le départ.
  - Si les PJ ont une indication préalable de [[Tisse-Chef Krux]] ou d'[[Archaeonex]], ils savent aussi chercher les indices suivants : vieille soie grisâtre, rainures de griffes sur la pierre, et cendre plus souvent remuée que le reste du secteur.

  **Complication / relance**
  - Le timer visible démarre ici.
  - Si les PJ traînent ou ratent leurs approches, la première patrouille passe plus près de la grotte, rendant la suite plus tendue.
  - En cas d'échec, les PJ trouvent quand même la bonne zone, mais au prix de temps perdu, d'une arrivée plus exposée, ou d'un premier passage de patrouille au mauvais moment.

- ### Scène 2 — Le refuge ravagé
  > L'entrée de la grotte semble avoir été éventrée puis abandonnée à moitié. Des pans entiers de soie pendent encore entre la roche et les racines brûlées. Plus loin, la chambre de ponte est un charnier silencieux : œufs brisés, membranes déchirées, traces nettes de lutte et de prélèvements. Quelque chose ici a été défendu jusqu'au bout, puis arraché.

  **Description prête à lire — contact avec le [[Fil-Mémoire]]**
  > Au contact de la soie, quelque chose vous traverse sans passer par les mots. Une secousse de peur, d'abord. Puis l'urgence nue, animale, absolue : protéger, couvrir, retenir, gagner quelques instants de plus. Vous sentez la rupture d'un fil, puis d'un autre, les vibrations de pas trop nombreux, trop rapides, trop proches. Pendant une respiration, vous n'êtes plus dans une couvée détruite depuis longtemps ; vous êtes au cœur de la panique qui l'a vue mourir.

  **But de la scène**
  - Faire trouver le [[Fil-Mémoire]].
  - Montrer le coût émotionnel du raid.
  - Semer les premiers indices qu'il existe une partie cachée du refuge.

  **Informations que les PJ peuvent trouver**
  - Le raid a été violent, rapide et ciblé.
  - Le [[Fil-Mémoire]] se trouve dans la couvée, et uniquement là.
  - Les Cisarelles sont revenues après le raid : il y a des traces plus récentes, surtout près d'une paroi ou d'une membrane suspecte, comme si elles savaient qu'il y avait quelque chose derrière sans avoir réussi à y accéder.
  - Le contact avec le fil peut transmettre une impression brève : panique, instinct de protection, urgence, rupture.

  **Jets possibles**
  - **Perception** : retrouver le [[Fil-Mémoire]] parmi les débris de couvée ; remarquer les zones trop piétinées près du futur passage.
  - **Médecine** ou **Nature** : distinguer les dégâts du raid initial des fouilles plus récentes.
  - **Occultisme** : interpréter l'empreinte sensorielle laissée dans le [[Fil-Mémoire]].
  - **Discrétion** : se cacher si la patrouille repasse pendant la fouille.

  **Complication / relance**
  - Un passage de patrouille peut survenir pendant cette scène selon le timer.
  - Les PJ doivent choisir : continuer à fouiller, se cacher, ou interrompre leurs recherches quelques instants.

- ### Scène 3 — Le laboratoire caché
  > Derrière une membrane presque confondue avec la paroi, l'air change. Le lieu n'a pas l'aspect d'un simple nid : ici, tout évoque l'étude. Des cristaux d'éther sont enchâssés dans la roche et la soie durcie. Des résidus alchimiques, des instruments adaptés à des manipulations fines, des fils tirés en réseaux précis, et surtout une zone de confinement montrent qu'une Cisarelle a été retenue ici pour être observée, isolée, étudiée.

  **Description prête à lire — Cristal 1 : chambre d'isolement**
  > Le cristal s'allume de l'intérieur et une scène se forme, non comme une image nette, mais comme une pensée ordonnée. Le laboratoire est intact. Les fils tendus dessinent un motif précis entre la roche, la soie durcie et les cristaux enchâssés. Au centre, derrière une membrane renforcée, une Cisarelle captive heurte les parois, coupe son mouvement, recommence. Les gestes d'[[Archaeonex]] sont méthodiques, presque cliniques. Ce qu'elle observe ici n'est pas seulement un corps retenu, mais un lien qu'elle cherche à affaiblir. Quelque chose dans cette chambre a été conçu pour brouiller la connexion entre la captive et le [[Psylith]].

  **Description prête à lire — Cristal 2 : formule incomplète**
  > Cette vision se fragmente en détails techniques : coupelles où sèchent des résidus sombres, spores, poussières minérales, fils traités, fluides filtrés dans de fines poches de soie, cristaux accordés les uns aux autres. Puis tout converge vers une absence. Vous comprenez qu'[[Archaeonex]] ne cherchait pas seulement à maintenir une prison ; elle tentait de reproduire l'effet de brouillage sous une forme exploitable. Mais un composant manque, toujours le même, comme une pièce autour de laquelle tout le reste a été construit : un champignon ayant poussé longtemps sur les troncs calcinés du territoire cisarelle, imprégné des résonances du [[Psylith]]. Sans lui, la formule reste incomplète, instable, dangereuse.

  **Description prête à lire — Cristal 3 : la captive change**
  > Dans ce souvenir, la captive ne se jette plus contre les parois comme au début. Elle bouge plus lentement, plus précisément. Elle touche les fils, la membrane, les pierres, puis s'immobilise, comme si elle apprenait le lieu autant qu'elle le subissait. Le silence imposé par l'isolement ne l'a pas simplement privée de quelque chose ; il a laissé de la place à autre chose. Là où vous attendriez l'épuisement ou la confusion, vous percevez l'ébauche d'une volonté plus nette, plus singulière, plus dure. Une pensée commence à prendre forme dans la coupure.

  **But de la scène**
  - Faire découvrir le cœur caché du refuge.
  - Donner le protocole de brouillage local des communications cisarelles.
  - Révéler qu'[[Archaeonex]] expérimentait sur une Cisarelle sans dévoiler encore l'identité de la captive.

  **Informations que les PJ peuvent trouver**
  - [[Archaeonex]] menait ici des expériences sur l'isolement d'une Cisarelle hors du [[Psylith]].
  - Le brouillage local des communications cisarelles est possible.
  - Il faut un composant rare pour stabiliser la formule : un champignon poussant sur les troncs calcinés du territoire cisarelle.
  - Les cristaux d'éther du laboratoire servent de mémoire de recherche.
  - Le lieu suffit à pointer les PJ vers les bons éléments : zone d'expérimentation, matériel alchimique, traces de confinement, mais sans tout expliquer à leur place.

  **Jets possibles**
  - **Perception** : trouver le mécanisme d'ouverture de la membrane si ce n'est pas encore fait ; repérer les éléments importants du laboratoire.
  - **Arcane** ou **Occultisme** : comprendre le rôle des cristaux d'éther et le principe général du brouillage.
  - **Alchimie / Artisanat** : identifier la formule, ses éléments utiles, et la nécessité d'un composant stabilisateur.
  - **Nature** : relier le composant rare au champignon du territoire calciné.

  **Complication / relance**
  - Les PJ n'ont pas de sortie secondaire ; ils devront repartir par le même chemin.
  - Le timer continue : plus ils étudient le lieu, plus la sortie devient risquée.

  **Détails supplémentaires en cas de bons jets**
  - **Succès en Arcane / Occultisme sur le cristal 1** : les PJ comprennent que le brouillage agit localement sur le relais entre une Cisarelle et le [[Psylith]], pas sur tout le réseau d'un seul coup.
  - **Succès en Artisanat / Alchimie sur le cristal 2** : les PJ identifient clairement qu'il est possible de transformer ce principe en ressource alchimique utilisable plus tard.
  - **Succès en Arcane / Occultisme sur le cristal 3** : les PJ comprennent que l'isolement n'a pas seulement privé la captive d'un lien ; il a favorisé l'émergence d'une pensée plus individuelle.

- ### Scène 4 — Sortie du territoire
  > Le refuge est derrière vous, mais pas encore la sécurité. La cendre garde les traces, les troncs morts découpent les lignes de vue, et chaque minute passée de plus dans cette zone laisse le temps à la patrouille de repasser. Le silence revient, mais ce n'est pas celui d'un lieu vide : c'est celui d'un territoire qui écoute.

  **But de la scène**
  - Transformer la sortie en vraie décision de rythme.
  - Faire peser les conséquences du temps perdu dans la grotte.
  - Ramener les PJ en zone sûre pour respecter le format Westmarch.

  **Informations que les PJ peuvent trouver**
  - Les Cisarelles surveillent cette zone par passages réguliers plutôt que par présence constante dans le refuge.
  - Le psychiste peut ressentir une nouvelle impulsion mentale à l'approche d'une patrouille ou d'un balayage local.

  **Jets possibles**
  - **Discrétion** : quitter la zone sans attirer l'attention.
  - **Survie** : choisir un itinéraire de retour moins exposé.
  - **Perception** : entendre ou voir la patrouille avant qu'elle n'arrive à portée dangereuse.
  - **Athlétisme** ou **Acrobaties** : franchir vite un passage encombré si la fuite devient nécessaire.

  **Complication / relance**
  - Selon l'état du timer, cette scène peut se résoudre dans la tension pure, la cachette, ou un affrontement bref si les PJ ont accumulé trop de retard ou de bruit.

- ### Scène 5 — Retour chez [[Archaeonex]]
  > De retour auprès d'[[Archaeonex]], l'atmosphère change. La peur du territoire laisse place à quelque chose de plus lourd, plus ancien. Lorsque le [[Fil-Mémoire]] lui est rendu, la soie semble presque se tendre d'elle-même entre ses pattes. Puis les cristaux d'éther répondent, l'un après l'autre, comme si une pensée oubliée trouvait enfin le chemin du retour.

  **Description prête à lire — cristal final**
  > Lorsque le dernier cristal répond enfin au [[Fil-Mémoire]], la vision vous saisit avec une netteté presque douloureuse. Le laboratoire est le même, mais l'équilibre a disparu. Les fils vibrent hors rythme. Les cristaux répondent à contretemps. La captive, presque immobile, semble pourtant remplir toute la pièce de sa présence. Puis vient l'instant précis où quelque chose force un passage. Ce n'est ni une voix ni un cri. C'est une volonté froide, aiguë, obstinée, qui refuse le silence qu'on lui impose. Vous sentez cette pensée heurter le brouillage, insister, trouver une faille, puis franchir la barrière.
  >
  > La suite déferle immédiatement : mouvement au-dehors, retour de présences cisarelles, rupture du refuge, panique d'[[Archaeonex]], défense désespérée de la couvée. Tout se mêle dans l'urgence, jusqu'au moment où une identité se fixe avec une clarté insupportable. La captive n'est plus seulement un sujet d'étude. Le nom qui reste, comme une écharde plantée dans la mémoire, est **Golgotha**.

  **But de la scène**
  - Offrir le climax narratif de la session.
  - Révéler l'identité de la captive du laboratoire.
  - Donner aux PJ la vérité sur l'attaque du refuge et sur le lien avec [[Golgotha, la Mère des Chairs]].

  **Informations que les PJ peuvent trouver**
  - Les visions du cristal sont automatiques dès qu'[[Archaeonex]] restaure la continuité de ses souvenirs.
  - Elles montrent les expériences d'isolement sur une jeune Cisarelle, les effets partiels du brouillage, l'émergence d'une volonté plus individuelle, puis les tentatives de communication au-delà du blocage.
  - La dernière séquence montre la percée mentale qui permet d'alerter l'extérieur et entraîne l'attaque du refuge.
  - Le nom de **Golgotha** n'apparaît qu'à la fin, liant rétrospectivement la captive du laboratoire à la future [[Golgotha, la Mère des Chairs]].

  **Jets possibles**
  - **Arcane** ou **Occultisme** : clarifier les séquences, mieux comprendre l'ordre des expériences et ce qui s'est joué dans le laboratoire.
  - **Psychisme / compétence appropriée du PJ psychiste** : ressentir plus finement la nature de la percée mentale ou du signal envoyé.
  - **Diplomatie** ou **Nature** : calmer [[Archaeonex]] ou guider l'échange si la restitution du souvenir la bouleverse.

  **Détails supplémentaires en cas de bons jets**
  - **Succès en Arcane / Occultisme** : les PJ comprennent que la percée mentale de Golgotha n'a pas été propre ni stable, mais qu'elle a été suffisante pour alerter l'extérieur malgré le brouillage.

  **Conséquence**
  - Les PJ terminent la session avec le [[Fil-Mémoire]] rendu, une avancée concrète contre les [[Cisarelles]], et une nouvelle compréhension du rôle de [[Golgotha, la Mère des Chairs]] dans l'arc en cours.


## Événements / Décisions
- Les PJ décident ou non de chercher l'aide de [[Tisse-Chef Krux]] avant l'expédition.
- Les PJ gèrent leur temps face au timer de patrouille : vitesse, discrétion, fouille approfondie ou repli.
- Les PJ récupèrent le [[Fil-Mémoire]] d'[[Archaeonex]].
- Les PJ découvrent ou non le passage vers le laboratoire caché.
- Les PJ récupèrent ou non les éléments utiles du laboratoire avant de repartir.
- Les PJ choisissent s'ils retournent voir [[Archaeonex]] dans la même session pour lui rendre le fil.

## Indices / Pistes
- Les [[Cisarelles]] communiquent par télépathie de proximité plutôt que par un lien uniforme et instantané partout.
- Des relais locaux spécialisés permettent de transmettre ou relayer les communications vers le [[Psylith]].
- Une Cisarelle isolée localement du réseau devient plus difficile à coordonner et peut être perturbée.
- [[Archaeonex]] avait déjà découvert un moyen partiel de brouiller cette communication.
- Le laboratoire prouve qu'[[Archaeonex]] expérimentait sur une Cisarelle captive.
- Le protocole trouvé exige un champignon rare poussant sur les troncs calcinés du territoire cisarelle.
- Le retour chez [[Archaeonex]] révèle que la captive du laboratoire deviendra plus tard [[Golgotha, la Mère des Chairs]].

## Butin / Récompenses
- [[Fil-Mémoire]] d'[[Archaeonex]].
- Accès au laboratoire caché d'[[Archaeonex]].
- Cristaux d'éther contenant ou permettant d'activer des souvenirs de recherche.
- Recette / protocole alchimique de brouillage local des communications cisarelles.
- Identification d'un composant rare nécessaire : champignon des troncs calcinés du territoire cisarelle.
- Révélation narrative sur l'origine de la déviation de [[Golgotha, la Mère des Chairs]].

## À reporter / Prépa prochaine
- Préparer mécaniquement la patrouille cisarelle adaptée au groupe réel.
- Déterminer les PJ présents et vérifier les synergies particulières (psychiste, alchimiste).
- Préparer la version exacte de la recette alchimique et ses limites.
- Définir la future exploitation du champignon rare : récolte, rareté, risques, culture éventuelle.
- Écrire la scène de restitution du [[Fil-Mémoire]] à [[Archaeonex]].
- Mettre à jour les cartes liées à la grotte, à la mine et au camp des prospecteurs.
