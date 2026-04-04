---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 6
code: S006
date_irl:
fc-date:
fc-end:
resume:
updated: 2026-03-15
termine: false
timelines:
  - session
aat-render-enabled: true
pjs: []
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

## Pitch joueurs (a envoyer)

Vous êtes conviés à **La Nuit des Sceaux**, une soirée officielle dans la [[Citadelle Blanche]] de [[Port-Lointain]].
Ce n'est pas un banquet : c'est un champ de bataille poli.

Quatre tables, quatre factions, et des conseillers dont la parole pèse sur les décisions du [[Conseil de la Brèche]]. Vous aurez quelques tours pour gagner leur faveur, comprendre leurs lignes rouges, et pousser la colonie vers des choix qui engageront les prochains mois.

---

## Format (Influence PF2e)

- 100% roleplay, structuré par "tours" d'influence.
- 4 tables (une par faction). À chaque tour, un PJ choisit une table (ou reste) et fait une approche (discussion, argumentaire, promesse, concession, etc.).
- Les PJ peuvent repartir avec des "engagements" : appuis, vétos levés, contreparties, rumeurs exploitables.

Suggestion pratique : afficher les 3 sujets (ci-dessous) comme "ordre du jour" ; chaque table a une position de départ et 1-2 conditions non négociables.

---

## Règles à lire aux joueurs (version courte)

Cadre : on utilise le sous-système **Influence** (GM Core). La soirée est découpée en rounds.

- **Initiative** : on joue à l'initiative ; à ton tour, tu as **3 minutes** (timer Foundry) pour ton "moment".
- **1 action par tour** : tu choisis une table (un conseiller) et tu fais **1 action** parmi :
  - **Influencer** : faire un jet adapté ; **succès = +1** point d'Influence, **succès critique = +2**, **échec = +0**, **échec critique = -1**.
  - **Découvrir** : observer / discuter pour comprendre ses leviers (jet de Perception ou autre compétence) ; tu obtiens une info utile (faiblesse, résistance, meilleure compétence...). Permet également de connaître gratuitement la position du conseiller à propos de l'un des points à l'ordre du jour.
- **RP libre** : entre les actions, tu peux parler et jouer ton rôle ; seuls les "moments d'action" comptent mécaniquement.
- **Changer de table** : gratuit, mais **au début de ton tour** (sinon tu restes à la même table).

### Seuils d'Influence (par conseiller)

- **Influence 2** : posture mineure (le conseiller s'ouvre, révèle un vrai enjeu / une condition).
- **Influence 4** : soutien conditionnel (compromis possible, contrepartie explicite).
- **Influence 6** : *sway* possible (engagement officiel sur **1** des 3 points).

### Cachets de faction (réputation)

Votre faction dispose d'un petit nombre de **Cachets** (réserve commune). Un Cachet représente un appui officiel (lettre scellée, recommandation, faveur, crédit, bénédiction...).

- **Dépense (1 Cachet)** : uniquement quand tu fais l'action **Influencer**, **après avoir vu ton résultat**.
  - Sur un **échec**, traite-le comme un **succès** (tu gagnes **+1** point d'Influence).
  - Sur un **échec critique**, traite-le comme un **échec** (tu ne perds pas de point).
- **Garde-fou** : un Cachet **ne peut pas** être le point qui fait franchir le seuil de *sway* (il peut t'amener à 5, mais pas à 6).

### Plaidoirie finale (déclenchement du *sway*)

Atteindre **Influence 6** rend le conseiller "prêt à basculer", mais la décision finale se joue en **plaidoirie**.

- **Éligibles** : tout PJ ayant déjà gagné **au moins 1 point d'Influence** sur ce conseiller pendant la soirée.
- **Moment** : en général au **Round 6 (dessert + toasts)** (ou dès que le MJ annonce que le sujet se fige).
- **Action** : chaque PJ éligible peut utiliser son action **Influencer** pour une plaidoirie (30–60 s) et annoncer :
  - quel **point de l'ordre du jour** il veut faire basculer ;
  - vers quelle **position** (sa version / son compromis).
- **Jet** : jet d'Influence cohérent (compétence du conseiller, ou Diplomatie si justifiée).
- **Départage** : le meilleur résultat **fixe le sway**.
- **Bonus "travail en amont"** : +1 circonstance au jet de plaidoirie finale par succès d'Influence précédent obtenu personnellement sur ce conseiller (max +2).

---

## Conseillers (1 par faction)

- [[Royaume d'Halvorn]] : Rosa Copperkettle (Halfeline) - logistique, ravitaillement, sécurité maritime.
- [[Ligue de Veyra]] : [[Soren Carthain]] (Tengu) - contrats, cadres, "vérités écrites".
- [[République de Thaldris]] : Lorrata (Léchi) - doctrine, avant-postes, contrôle territorial.
- [[Ordre de Myrr]] : Erevan Moonblade (Elfe) - rites, serments, protection des innocents.

Note : ces conseillers ont l'oreille de leurs membres au Conseil (cf. [[Conseil de la Brèche]]).

Invité : un ambassadeur **[[Kroass-Goll]]** est présent pour entendre les débats concernant le traité et porter une parole "Vase-vrai".

---

## PNJ — Statblocks d'influence

```pf2e-stats
# Rosa Copperkettle
## Niveau 3
---

==Petite== ==Halfeline==

Conseillère d'Halvorn au sourire rare et au regard de contremaître : elle pense en rations, en marées, et en vies à sauver.

**Perception** +12
**Connaissances (Ravitaillement & Convois)** +10, **Performance** +9, **Athlétisme** +9, **Société** +9
**Volonté** +9

---
**Historique** Fille de cambuse devenue intendante de convoi, Rosa s'est faite un nom en tenant des équipages debout quand le sel manquait et que les hommes râlaient. À Port-Lointain, elle surveille tout ce qui nourrit, chauffe, et évacue.
**Apparence** Habit de laine sombre impeccablement reprisé, gants fins tachés de cire, petite bouilloire de cuivre cabossée en porte-bonheur. Odeur de sel et d'infusion amère.
**Personnalité** Pragmatique, protectrice, intransigeante.
**Oral, signe distinctif** Pose des questions "simples" qui enferment les vagues promesses ; compte sur ses doigts (rations, jours, hommes).

---
**Découverte** Connaissances (Cuisine) DD 12 (son plat "simple mais parfait" et l'infusion amère), Connaissances (Convois) DD 12 (son désastre de ravitaillement), Société DD 18 (son vrai levier : rations et navires), Perception DD 22 (elle déteste le gaspillage; la bouilloire-talisman)
**Compétences d'influence** Connaissances (Cuisine de bord) DD 12, Connaissances (Ravitaillement & Convois) DD 14, Performance DD 16 (chant de halage / l'inviter à danser), Athlétisme DD 17 (prouver qu'on tiendra), Artisanat DD 18 (solutions de quai/palissade), Diplomatie DD 19, Intimidation DD 21 (capitaine à capitaine; risqué)
**Influence 2.** Neutralité : elle ne s'opposera pas à votre demande, mais ne mettra pas son poids logistique dessus.
**Influence 4.** Alliée conditionnelle : elle appuie si vous intégrez un cadre de survie concret (évacuation, ravitaillement, protection des civils, pas de gaspillage) et une contrepartie immédiate réaliste.
**Influence 6.** *Sway* : porteuse active : elle s'engage publiquement et promet de mobiliser ses leviers (rations, convois, priorités de quai) pour faire passer la décision.
**Influence 8.** Faveur logistique : priorité sur un transport, un entreposage, ou une escorte maritime limitée (selon les besoins de la colonie).
**Résistances.** Discours "on verra" (+2), minimiser les pertes civiles (+2), promesses vagues sans échéancier (+2).
**Faiblesses.** Corriger un gaspillage en public / faire servir "juste" (−2) ; lancer un chant de halage ou l'inviter à danser (−2) ; priorité aux réfugiés et aux blessés (−2).
```

```pf2e-stats
# Soren Carthain
## Niveau 3
---

==Unique== ==Tengu== ==Humanoïde==

Commissaire aux contrats de la Main de Platine : Carthain n'achète pas la vérité, il achète une vérité **écrivable**.

**Perception** +12
**Connaissances (Contrats & Droit commercial)** +10, **Société** +9, **Diplomatie** +9, **Duperie** +9, **Performance** +9
**Volonté** +9

---
**Historique** Affecté à [[Port-Lointain]] pour transformer les crises en clauses et les rumeurs en preuves, Soren sert de filtre : il écoute, encadre, scelle, puis laisse le temps travailler.
**Apparence** Plumage noir aux reflets ternes, tenue sombre impeccable, gants fins, chaîne de platine discrète, parapheur épais et stylet.
**Personnalité** Froid, méthodique, implacable.
**Oral, signe distinctif** Phrases courtes. N'élève presque jamais la voix. Répète : « Sans écrit, il n'y a pas de vérité. »

---
**Découverte** Connaissances (Contrats & Droit commercial) DD 12 (ce qu'il respecte: formulation courte; "sceau de courtoisie"), Société DD 18 (son rôle de filtre et ce qu'il bloque), Perception DD 22 (quand il "ouvre" son parapheur; ce qui l'agace en public)
**Compétences d'influence** Connaissances (Contrats & Droit commercial) DD 12, Performance DD 15 (toast bref, oratoire net), Société DD 16 (cadre acceptable par toutes les factions), Duperie DD 18 ("bonne" omission, dangereux), Diplomatie DD 19, Intimidation DD 22 (menace ses réseaux; très risqué)
**Influence 2.** Neutralité : il ne s'opposera pas à votre demande (il ne bloquera pas), mais ne la soutiendra pas.
**Influence 4.** Allié conditionnel : il prendra la parole pour défendre votre position si la proposition reste dans un cadre simple (3-5 clauses max, réciprocité, garde-fous clairs).
**Influence 6.** *Sway* : il devient porteur actif : il tranche en faveur de votre formulation et s'engage à la défendre comme "la seule version qui tiendra" devant le [[Conseil de la Brèche]].
**Influence 8.** Il ouvre une faveur de Veyra : accélérer un dossier, offrir une ligne de crédit officieuse, ou protéger une information derrière un sceau (au prix d'une dette RP).
**Résistances.** Tenter de l'émouvoir (+3), discours moraliste anti-argent (+3), contradictions sans preuve (+2).
**Faiblesses.** Offrir (ou faire apporter) un petit nécessaire d'écriture de qualité / demander un "sceau de courtoisie" sur un billet d'intention (−2) ; porter un toast bref et élégant à l'ordre, à la stabilité et aux "vérités écrites" (−2).
```

```pf2e-stats
# Lorrata
## Niveau 3
---

==Petite== ==Léchi==

Conseillère de Thaldris : une plante en uniforme, patiente et implacable, qui voit chaque décision comme une ligne de défense à faire pousser.

**Perception** +12
**Connaissances (Stratégie & Fortifications)** +10, **Performance** +9, **Nature** +9, **Société** +9, **Survie** +9
**Volonté** +9

---
**Historique** Lorrata a été "cultivée" (selon ses mots) dans l'ombre d'arsenaux thaldrissiens. Elle a appris à fortifier avant d'étendre, et à étendre avant d'être engloutie.
**Apparence** Corps de fibre et d'écorce, feuilles sombres taillées net ; harnais militaire ajusté ; petites plaques de métal rivetées comme une armure de parade.
**Personnalité** Disciplinée, calme, méfiante.
**Oral, signe distinctif** Voix basse, rythmée ; utilise des métaphores de croissance ("racines", "nœuds", "tailler").

---
**Découverte** Connaissances (Fortifications) DD 12 (ce qu'elle appelle un "avant-poste" viable), Performance DD 12 (elle adore danser; la musique la rend accessible), Nature DD 18 (elle lit le terrain), Perception DD 22 (elle repère les angles morts et jauge les gens au placement)
**Compétences d'influence** Connaissances (Fortifications) DD 12, Performance DD 15 (l'inviter à danser), Nature DD 16 (terrain, couverts, obstacles), Survie DD 17 (itinéraires, patrouilles), Société DD 18 (chaîne de commandement), Diplomatie DD 19, Intimidation DD 22 (pression frontale; très risqué)
**Influence 2.** Neutralité : elle ne s'opposera pas, mais ne détournera pas de moyens militaires pour vous.
**Influence 4.** Alliée conditionnelle : elle appuie si le plan renforce la posture défensive (ligne de vue, signal d'alerte, responsabilité claire) et si on ne "découvre" pas la colonie au nom du commerce.
**Influence 6.** *Sway* : porteuse active : elle s'engage publiquement, plaide la décision au Conseil, et promet d'affecter encadrement/planification pour la rendre opérationnelle.
**Influence 8.** Elle offre un avantage tactique : carte, plan de poste, ou détachement d'encadrement (selon l'état des forces).
**Résistances.** Pacifisme naïf (+2), acheter sa loyauté (+3), contester sans données (+2), menacer la forêt sans nécessité (+2), approcher avec flammes/fumée ou menaces "terre brûlée" (+2).
**Faiblesses.** L'inviter à danser (−2) ; tracer un croquis d'avant-poste sur une serviette (angles, lignes de vue, signal d'alerte) (−2) ; engagement clair contre les [[Cisarelles]] (−2).
```

```pf2e-stats
# Erevan Moonblade
## Niveau 3
---

==Moyenne== ==Elfe==

Conseiller de Myrr : calme, tranchant dans ses principes, attentif aux serments que l'on prononce sans y penser.

**Perception** +12
**Religion** +10, **Occultisme** +9, **Médecine** +9, **Diplomatie** +9, **Performance** +9
**Volonté** +9

---
**Historique** Attaché aux rites et à la médiation, Erevan a vu trop de colonies "réussir" en se damnant. Sa mission est d'empêcher Port-Lointain de devenir un autre sacrifice.
**Apparence** Robes claires brodées de motifs d'astres et de flammes, parfum d'encens, regard qui "écoute".
**Personnalité** Bienveillant, inflexible, lucide.
**Oral, signe distinctif** Parle en images simples ; marque les silences comme des parenthèses de jugement.

---
**Découverte** Connaissances (Rites de Myrr) DD 12 (ce qui est acceptable en public; comment demander une bénédiction), Performance DD 18 (il préfère la musique sobre; un chant bien choisi le touche), Religion DD 18 (ce qu'il considère sacré/intouchable), Perception DD 22 (il se place près des fenêtres et observe la lune; il jauge les intentions)
**Compétences d'influence** Connaissances (Rites de Myrr) DD 12, Performance DD 16 (chant sobre / accompagner les musiciens), Médecine DD 17 (protéger les civils, soins), Religion DD 18, Occultisme DD 18 (présages, prudence), Société DD 18 (équilibres de la Concorde), Diplomatie DD 19, Duperie DD 22 (très risqué)
**Influence 2.** Neutralité : il ne s'opposera pas à votre demande, mais ne la bénira pas ni ne la défendra.
**Influence 4.** Allié conditionnel : il appuie si la proposition respecte un cadre moral et rituel (protection des innocents, réparation en cas d'offense, pas de profanation) et si le ton reste digne.
**Influence 6.** *Sway* : porteur actif : il s'engage publiquement, prend le rôle de garant/médiateur, et pousse la décision au Conseil comme "nécessaire et juste".
**Influence 8.** Il accorde une faveur de Myrr : médiation formelle, sanctuaire, ou divination limitée liée aux conséquences d'une décision.
**Résistances.** Cynisme sur la foi (+2), instrumentaliser la religion (+2), moquerie des rites (+3).
**Faiblesses.** Proposer un toast rituel bref "pour les vivants et les absents" et lui demander une bénédiction symbolique (−2) ; offrir une lumière (bougie/lanterne) dédiée aux civils et éclaireurs (−2) ; intervenir quand quelqu'un ridiculise un rite ou humilie un innocent (−2).
```

```pf2e-stats
# Drim’Roseau, « Porte-Brume » — Ambassadeur Kroass-Goll
## Niveau 3
---

==Kroass-Goll== ==Humanoïde==

Émissaire du Goll-Tout à Port-Lointain, Drim’Roseau vient “mettre des mots sur la brume” : obtenir un traité court, respectueux, et surtout utile contre les [[Cisarelles]].

**Perception** +12
**Nature** +10, **Religion** +9, **Diplomatie** +9, **Société** +9, **Survie** +9, **Performance** +9, **Connaissances (Kroass-Goll)** +9
**Volonté** +9

---
**Historique** Désigné par les Sachants du Vase-Goll pour porter une parole "Vase-vrai" auprès des peaux-sèches. A déjà négocié sel, clous et cordages contre guidage et pilotis, et a vu des étrangers profaner par ignorance.
**Apparence** Amphibien à peau lisse vert sombre, terne aux épaules, luisante aux mains. Bijoux de tourbe et d’os poli, petites plaques d’argile séchée gravées de motifs de roseaux. Porte un paquet de sel scellé et un chapelet de perles de vase.
**Personnalité** Patient, méfiant, cérémonieux.
**Oral, signe distinctif** Parle à la 3e personne ("Ce Kroass…"), ponctue ses phrases de serments ("Vase-vrai") et de gestes codés (paume ouverte = paix, doigts vers la gorge = vérité).

---
**Découverte** Connaissances (Kroass-Goll) DD 12 (3 tabous immédiats + le sens des plaques d'argile), Performance DD 18 (le refrain simple + gestes corrects), Nature DD 18 (ce qu'il considère "utile" ce soir: outils, sel, cordage, jarres sèches), Perception DD 22 (il se ferme quand on parle d'exclusivité/propriété; il s'apaise à l'odeur du sel)
**Compétences d'influence** Connaissances (Kroass-Goll) DD 12 (tabou + réparation), Performance DD 15 (refrain + gestes; sans moquerie), Nature DD 16 (pilotis, passages, brume; pas de "possession" du marais), Survie DD 17 (itinéraires, signaux, campements secs; montrer un kit), Société DD 18 (traité court, 3-5 clauses max), Diplomatie DD 19, Intimidation DD 22 (uniquement contre les [[Cisarelles]] + preuve crédible)

**Influence 2.** Il donne une liste claire de besoins (2-3 objets + 1 service) et ce qu'il offre en échange. Besoins typiques : **sel**, **cordage**, **clous/rivets**, **lames (hache/serpe)**, **huile de lampe**, **couvertures sèches**, **jarres étanches**.
**Influence 4.** Il livre une information exploitable sur les [[Cisarelles]] (signe de raid, zone de chasse sur les rivières, comment éviter une embuscade), et propose un échange immédiat (guidage/pilotis contre livraison datée de matériel).
**Influence 6.** *Sway* : il endosse publiquement une forme de traité et promet un acte visible : un **guide désigné** + ouverture d'un **passage sur pilotis** + un **signal d'alerte**. Il exige un mini-rite de sceau (chorus + geste + sel ou lumière).
**Influence 8.** Avantage majeur anti-[[Cisarelles]] : enseignement de signaux kroass pour patrouilles OU une cache sûre sur pilotis OU un écran de brume tactique (une fois) sur une mission, contre un engagement explicite de protection.

**Résistances.** Mensonge ou "demi-vérité" (+5 au DD); contrat long/jargon (+2); exclusivité/monopole "sur le marais" (+2); moquerie des rites (+3);
**Faiblesses.** Poser du **sel/cordage/clous/outils** sur la table (−2); accepter un mini-rite public de sceau (−2); promesse datée d'action contre les [[Cisarelles]] (−2); reproduire correctement refrain/gestes (−2).
```

---

## Ordre du jour (3 items)

### 1) Implantation du premier village (hors de l'hex de [[Port-Lointain]])

Contexte : [[La Noue]], [[Bois-Moulin]], [[Brèche-Rive]] et [[Fosse-Claire]] restent des dépendances du même hex ; la question porte sur une implantation permanente au-delà.

- [[Royaume d'Halvorn]] : village **côtier** (pêche, relais de fanaux, appui naval, évacuation facile).
- [[République de Thaldris]] : village **vers le territoire des [[Cisarelles]]** (avant-poste, profondeur défensive, contrôle des mouvements).
- [[Ligue de Veyra]] : village sur un **nœud économique** (carrefour naturel/vallée/point d'eau) avec **marché + entrepôts**, idéalement sous forme de concession.
- [[Ordre de Myrr]] : village **refuge** loin des zones de conflit (sanctuaire, soins, rites ; neutralité affichée).

### 2) Traité avec les [[Kroass-Goll]]

Contexte : contact établi lors de `S003` ; le Sachant Uuroch a promis l'envoi d'ambassadeurs à [[Port-Lointain]].

- [[Royaume d'Halvorn]] : **pacte de passage et de secours** (guides, balises, sauvetage ; pas d'engagement profond).
- [[République de Thaldris]] : **accord militaire limité** (renseignements sur les [[Cisarelles]], patrouilles conjointes, signaux d'alerte ; clauses strictes).
- [[Ligue de Veyra]] : **traité commercial** (sel/outils contre guide, ressources de marais, droits de comptoir ; exclusivités "raisonnables").
- [[Ordre de Myrr]] : **pacte rituel** (serments "Vase-vrai", protection des sites/ancêtres ; médiation ; interdire la profanation).

### 3) Priorité ressources (6 mois) : bois au sud vs fer noir à l'ouest

Contexte :
- Bois : forêt au sud (construction, chauffage, palissades, chantiers).
- Fer noir : collines à l'ouest (outils, clous, armement). Risque associé aux histoires autour de [[Le Fer Trompeur]] et aux [[Gobeliés]].

- [[Royaume d'Halvorn]] : **bois** d'abord (quais, chantiers navals, palissades ; impact immédiat).
- [[République de Thaldris]] : **fer** d'abord (autonomie militaire, outillage, production).
- [[Ligue de Veyra]] : **fer** si exploitable via contrats/contrôle ; sinon **bois** (liquidité rapide ; maîtrise des flux).
- [[Ordre de Myrr]] : **pierre**.

---

## Aides MJ (accroches de conversation)

- Halvorn : "combien de semaines avant la prochaine tempête ?" / "combien de barques, combien de fanaux ?" / "si ça tourne mal, comment on évacue ?"
- Veyra : "qui paie quoi, et qui contrôle quoi ?" / "quelles garanties ?" / "quelle contrepartie chiffrable ?"
- Thaldris : "ligne de défense" / "temps de réponse" / "point d'appui et champ de vision"
- Myrr : "qui protège-t-on en premier ?" / "quel serment, quel tabou ?" / "que sacrifie-t-on moralement pour survivre ?"

---

## Intermède de Théobald
Tu reçois une convocation à la Citadelle Blanche où l'on te guide jusqu'à l'ambassadeur Kroass-Goll qui a demandé ta présence. Il se présente: Porte-Brume Drim'Roseau. Il te montre le papier que vous aviez remis au Sachant Uuroch. Vous discutez pendant quelques heures et tu obtiens les informations suivantes : 
- Les Kroass-Goll ont besoin de sel, de haches/serpes/lames utiles aussi bien en tant qu'outils qu'arme, tissus/couvertures sèches. Il est aussi très intrigué par le concept de lampe à huile.
- Les Kroass-Goll peuvent offrir des guides pour les régions plus au sud, construire des ponts/pilotis, partager des informations sur les Cisarelles (Mantes).

---
Concernant les Conseillers tu obtiens les informations suivantes :
- Lorrata (léchi) : elle aime danser et discuter stratégie militaire. Elle n'aime pas que l'on envisage un pacifisme naïf face aux menaces. Ses positions sur l'ordre du jour sont de placer un avant-poste au sud pour faire tampon entre le territoire Cisarelle et Port-Lointain.
- Rosa Copperkettle (halfeline) : aucune information actionnable ne circule actuellement.
- Erevan Moonblade (elfe) : il est attaché aux rites et à la médecine. Il aime aussi une bonne chanson ou un toast bien porté. Il déteste le cynisme. Ses positions sur l'ordre du jour sont de pousser pour une plus grande exploitation des carrières de pierre, pour ériger des temples ou solidifier les défenses.

## Conséquences possibles (à cocher)

- [ ] Un site prioritaire est voté pour le village (ouvrir une mission "repérage + négociations + logistique").
- [ ] Une forme de traité kroass est fixée (qui signe, quelles clauses, quelles contreparties).
- [ ] Une priorité ressources est annoncée (bois vs fer) + une mesure d'encadrement (quotas, concessions, garde, tabous).
