---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 3
code: S003
date_irl: 2026-02-15
fc-date: 2942-05-12
fc-end: ""
resume: ""
updated: 2026-02-15
termine: false
timelines:
  - session
aat-render-enabled: true
pjs:
  - "[[Campagnes/EFG/PJ/Korvax Oeil-de-fer.md|Korvax Oeil-de-fer]]"
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Voss Vitriox.md|Voss Vitriox]]"
  - "[[Campagnes/EFG/PJ/Théobald Greyheart.md|Théobald Greyheart]]"
  - "[[Campagnes/EFG/PJ/Citolin.md|Citolin]]"
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

- [x] Visuel des ruines
- [ ] Visuel du gardien
- [x] Visuel de Sachant
- [ ] Statblock Gardien
- [ ] Statblock Kroass ?
- [ ] Battlemap des ruines
- [ ] Battlemap terrain rivière avec les kroass-goll
- [ ] Conversations avec portraits dans Foundry
- [ ] Rencontre aléatoire
- [ ] Ajouter les journaux sur l'hexmap dans Foundry
- [ ] Prep. downtime activities
- [x] Portrait + handout de Gruk'Vase
- [ ] Pour l'intermède de Maxime regarder le sous système de recherche
- [ ] Items récompenses

## Intro

> Nyssor... 
> Au-delà de la Couronne Blanche, s'étendent des terres sans cartes et des ruines sans noms.
> Bienvenue, **éclaireur** de l'Expédition des Fendeurs de Glace. On vous envoie là ou les palissades s'arrêtent : explorer l'inconnu, découvrir des ressources, repousser les menaces ou nouer des alliances quand c'est possible. Et ramener à Port-Lointain ce que l'on ne peut pas cultiver : des réponses.

## Aperçu de la session
- Les PJ atteignent des ruines d’irrigation de [[Mnesitheos]], une ancienne ville de l’[[Hégémonie Aethelgard]], noyées dans une **brume humide** anormale ; une délégation [[Kroass-Goll]] menée par un **Sachant** veut récupérer une **Statue-Chaman** coincée dans le mécanisme irrigation, mais un **gardien** antique la maintient en place.

## Scènes

### Scène 1 : Hexploration (plaines)

> Vous quittez les palissades de [[Port-Lointain]] et, très vite, le monde se vide. Des plaines hautes, un ciel immense, vous avancez dans des territoires que peu de personnes ont foulé.
> Les points d’eau deviennent des repères plus que des ressources : mares temporaires, ruisseaux timides, et cette rivière au nord-est que vous suivez de loin comme une ligne de vie.
> Au second matin, l’air change : plus frais, plus lourd. Il y a cette odeur de terre mouillée… alors même que la pluie n’est pas tombée.

Entrée en mode Hexploration, sur la carte de Nyssor.

**Rencontres possibles (0 combat, 5–10 min chacune, au choix)**
- "Au milieu des hautes herbes, trois piquets grossiers forment un petit triangle. Le vent fait claquer un ruban de tissu sombre qui maintien les piquets ensemble. À quelques pas, une pierre plate a est posé au sol"
	Un trésor est caché sous la pierre, si les PJ soulèvent la pierre un item de récompense est trouvé. 
- "Une nappe de brume glisse entre les touffes d’herbe… mais elle ne suit pas le vent. Elle “cherche” les creux, s’accroche aux bottes, puis s’étire en filaments vers le nord-est, comme tirée par une respiration lointaine. Quand vous vous arrêtez, le silence est trop net : même les insectes semblent attendre."
	Foreshadowing de la brume des Kroass-goll
- "Vous tombez nez-à-nez avec une créature de la taille d'un enfant, ressemblant à une grenouille se tenant debout sur ses pattes arrières. Elle est aussi surprise que vous en vous voyant. D'une voix peu sûre, elle dit : Peau-sèche a pitié de ce Kroass, pas faire de mal".
	C'est un membre du groupe Kroass des ruines qui s'est perdu, il s'appelle : Gruk’Vase

### Scène 2 : Système d'irrigation

> Vous suivez la rivière jusqu'à un creux où l'atmosphère est empli d'une brume lourde et humide.
> Entre les hautes herbes, des murs bas émergent par fragments : blocs taillés, angles trop nets, dalles disjointes qui tracent encore un ancien canal peu profond. Plus loin, à travers la brume, vous devinez les ruines dont on vous a parlé : une ligne de façades effondrées et d’arches cassées.
> Le canal principal file vers un bâtiment qui ne ressemble pas à une maison : un ouvrage. Un long volume de pierre recouvert de toute sortes de mousses et de lichens, renforcé de bandes de métal riveté et rouillé, partiellement enfoncé dans la berge. Là où il devrait y avoir des fenêtres, il y a des ouvertures techniques : grilles épaisses, volets de maintenance, anneaux d’arrimage, et une grande porte cintrée à demi tordue.
> Autour de certains canaux, des bandes de terre sont dénuées de hautes herbes, comme si la friche avait évité ces endroits.

**Indices à distribuer**

1) **Traces Kroass-Goll**
- **Survie** DD 15 (pister) ou **Perception** DD 16
  - **Succès** : empreintes de bipèdes lourds, peau humide, pas “humains” → piste vers les roseaux (entrée Scène 3).
  - **Succès critique** : + détail : ils se sont arrêtés plusieurs fois comme pour “écouter” les vannes.

2) **Culture récente**
- **Nature** DD 14 (sol, plantation) ou **Société** DD 15 (outils/gestes)
  - **Succès** : parcelle irriguée *très récemment* (semis, rigoles reprises, outil de bois oublié).
  - **Succès critique** : + routine (réparations régulières) : ce n’est pas un coup unique.

3) **La rivière n’alimente pas le système**
- **Survie** DD 13 (lire les écoulements) ou **Perception** DD 13 (trop-pleins)
  - **Succès** : la rivière reçoit l’excédent ; le canal est plus humide en allant *vers* les ruines.
  - **Succès critique** : retour d’eau “propre” (condensation/filtration).

**Complication douce (si besoin de tension sans combat)**
- Bord de bassin **glissant** : **Acrobaties** DD 15
  - **Échec** : chute (1d6 contondant), équipement mouillé ; un objet non-sécurisé glisse vers une grille.

### Scène 3 : Les Kroass-goll

> Des yeux luisants apparaissent d’abord, bas, au ras des roseaux. Puis des silhouettes amphibiennes se dessinent : peau lisse et brillante, bijoux ternis par la tourbe, mains ouvertes en signe d’arrêt.
> L’un d’eux avance avec lenteur et gravité. Sa peau est plus terne, mais ses ornements sont plus riches ; il porte des morceaux d’argile séchée comme des reliques. Il incline la tête, inspire profondément la brume, puis “parle” autant avec la gorge qu’avec les mains.
> *« Brume-bonne, peaux-sèches. Ce Kroass… a besoin grand boutou. Vase-vrai : pas piège. Juste Statue. Suivez ce Kroass, venez ! »*

**À jouer**
- Vocatif : **« peau-sèches »**.
- Serment exigé : **« Vase-vrai : pas profaner Statue-Chaman. »**
- Ils éludent le “pourquoi” : *survie du Marais*.

**Répliques prêtes (Uuroch)**
- *« Ce Kroass dit vase-vrai : la Statue doit rentrer. Pas pour l’or. Pour le souffle du Marais. »*
- *« Peau-sèche… tu portes corde et fer. Bon. Grand boutou. »*
- *« Ne touche pas la Statue comme trophée. On la porte comme ancêtre. »*

**Dès qu'Uuroch est prêt à parler aux PJ ou si les PJ leur demande ce qu'ils font ici :**
> L'homme-grenouille s’accroupit, paume contre la boue, puis trace dans la vase un petit cercle, un autre, et une ligne entre les deux. Il inspire longuement la brume, comme on écoute une voix lointaine. Derrière lui, deux Kroass-Goll portent un grand panier tressé de roseaux, vide, mais tenu avec le même respect qu’un berceau.
> *« Ce Kroass… vient pour Ancêtre. Statue-Chaman. »* Il tapote le panier, puis pose ses doigts sur sa gorge, et secoue la tête : *« Sans Statue… chant cassé. Brume faible. Marais… saigne. »*
> Il pointe vers les ruines, puis fait un geste d’arrêt net, les deux mains ouvertes. Sa voix baisse, plus grave. *« Dans pierre-fer… y a Gardien. Pas chair. Pas esprit. Pas bête. »* Il mime quelque chose de haut, immobile, puis des bras qui se déploient avec des angles trop droits. *« Fer-dur qui marche. Œils-verre. Il écoute l’eau. Il compte les gouttes. »*
> *« Il dit : “pas prendre”. Il frappe les Kroass. »* Puis il relève la tête vers vous, l’air solennel. *« Nous-Kroass pas assez grand boutou pour reprendre Ancêtre. Peau-sèches ont corde et fer, savent parler fort. Peau-sèches grand boutou. Peau-sèche reprendre Ancêtre sans casser. »*
> Il pose une main sur son cœur, l’autre vers vous : *« Vase-vrai : si vous aidez, peau-sèches bienvenue au Marais. »*

```pf2e-stats
# Uuroch « Brume-Sûre », Sachant Kroass-Goll
## Niveau 2
---

==Kroass-Goll== ==Humanoïde==

Chaman gardien des chants ; venu loin du Marais (≈ 6 jours au sud) pour rapatrier une Statue-Chaman “exilée”.

**Perception** +8
**Nature** +9, **Religion** +8, **Diplomatie** +7, **Survie** +8
**Volonté** +9

---
**Historique** Uuroch a reçu ses visions au “Chant Sans Voix”. Il a juré de ramener la statue, car chaque gardien perdu affaiblit les rites et la brume.
**Apparence** Peau terne, bijoux et argile séchée ; mains tachées de tourbe ; regard fixe.
**Personnalité** Prudent, Solennel, Intransigeant sur la vérité
**Oral, signe distinctif** 3e personne (« ce Kroass… »), serments (« Vase-vrai »), signes des mains.

---
**Découverte** Société DD 14 (chef religieux), Nature DD 13 (liés à la brume), Perception DD 18 (il “mesure” les mensonges), Survie DD 13 (voyage léger/efficace)
**Compétences d'influence** Diplomatie DD 19 (10 + Volonté), Nature DD 16, Religion DD 16, Société DD 18, Intimidation DD 20 (seulement si on prouve qu’on peut protéger : « grand boutou »)
**Influence 2.** *Rumeur — « Le Marais saigne »* : raids de [[Cisarelles]] (piste : **sud**, brume persistante).
**Influence 4.** Détail concret : un **passage vital** (pont/pilotis) harcelé ; ils cherchent **escorte** ou **réparation** (cordes, clous, haches, sel).
**Influence 6.** *Rumeur — « D’autres peaux-sèches »* : [[Gobe'liés]] (sud/sud-ouest) ; **gens sous la terre** : [[Loge des Sans-Passé]] (craie puis disparition).
**Influence 8.** Contact : Uuroch accepte d’être un relais si les PJ restent “Vase-vrai”.
**Résistances.** Mensonge, plaisanteries sur les rites, profanation Statue-Chaman : +3 DD.
**Faiblesses.** Serment clair, respect physique, offrir **sel** ou **outils** : −2 DD.
```

### Scène 4 : Les Ruines de Mnesitheos

Les PJ entrent directement dans la partie des ruines/ville qui gère le système irrigation. Le reste de la ville semble enseveli sous terre, ou complètement détruit.

> Les murs de pierre sombre sont pris dans une ossature de métal : plaques rivetées, nervures de cuivre vert-rouille, anneaux et charnières qui n’ont rien à faire dans une maçonnerie classique. Il y a des grilles, des évents, des trappes d’accès ; là où l’on attendrait des fresques, on trouve des conduites et des boîtiers scellés.
> Par endroits, de minuscules perles d’eau naissent sur le métal puis roulent vers des rainures, guidées vers le bas — un système pensé pour capter, filtrer, redistribuer. Même en ruine, tout ici donne l’impression d’une fonction : rien n’est décoratif, tout est conçu.
> Le sol est instable et recouvert de boue et de racines. A droite et à gauche, de nombreux couloirs semblent s'être effondrés, le sol ayant disparu au profit de la terre ou de rochers. Sous la boue qui jonche le chemin, vous distinguez des lignes qui rident le sol… Parallèles parfois, divergentes d'autres fois. Certaines lignes semblent s'arrêter nette alors que le sol a disparu, d'autres se dirigent droit vers un passage éboulé et les dernières guident vos pas en direction d'une salle d'où émane le son constant de l'eau qui ruisselle.

Les PJ arrivent dans la salle de contrôle du système d'approvisionnement en eau. Il y a des mécanismes au murs et des centaines de conduites qui partent dans toutes les directions. Quelques conduites semblent être celles qui forment le système irrigation. Au coeur de ce complexe mécanisme, la statue des Kroass-goll suintante et dégoulinante, les gouttes d'eau tombant de la statue semblent remplir un réservoir situé dessous.
Devant ce réservoir ce tient un grand "golem" mécanique de [[Technomagie]] : le gardien.

> Vous débouchez dans une vaste salle dont le plafond s’est affaissé par endroits, mais où le cœur du dispositif tient encore. Les murs sont couverts de mécanismes : roues dentées figées, leviers sans poignée, cadrans opaques, et surtout des centaines de conduites qui entrent et sortent comme des veines. Certaines sont ouvertes, mangées par l’oxydation ; d’autres sont intactes, froides au toucher, et vibrent à peine — comme si un débit minuscule persistait encore.
> Au centre, une masse de pierre et d’argile attire immédiatement le regard : la Statue, saturée d’humidité, suintante, presque vivante dans cette brume. Des gouttes s’en détachent avec régularité et tombent dans un réservoir.
> Puis vous entendez le bruit : pas un grondement, plutôt une série de petits sons précis — cliquetis, souffles, un “tac”. Quelque chose, derrière un coffrage, vient de reprendre une routine. Une silhouette lourde se redresse lentement, couverte de dépôts calcaires comme d’une croûte de sel. Deux lentilles laiteuses s’allument d’un éclat faible et vous passent au crible, outil par outil, arme par arme… puis s’arrêtent sur la Statue.
> « DÉFAUT : MODULE D’HUMIDIFICATION. REMPLACEMENT INSTALLÉ. STATUT : STABLE. »

**Si les PJ tentent de retirer la statue**
> *« AVERTISSEMENT. RETRAIT D’ÉLÉMENT CRITIQUE INTERDIT. »*

**Lignes du gardien**
- *« AVERTISSEMENT. RETRAIT D’ÉLÉMENT CRITIQUE INTERDIT. »*
- *« PARAMÈTRES BIOLOGIQUES INCONNUS. LES VISITEURS NE SONT PAS ADMIS DANS LA SALLE DE CONTRÔLE. »*
- *« PRÉSENTEZ PLAN DE CONTINUITÉ. TEST DE DÉBIT REQUIS. »*
- *« PARAMÈTRES DU MONDE : INCONNUS. FOURNIR PREUVES. »*

---

**Jets — comprendre le site**
- **Perception** DD 16 : le réservoir alimente les conduites.
- **Artisanat** DD 15 : réservoir interne/puits → chambre de pression → distribution.
- **Survie** DD 15 : certaines conduites forment le système d'irrigation, certaines partent dans l'autre direction à travers les murs ou vers le sol, suggérant une alimentation possible en eau d'autres systèmes/lieux.

**Indice Sans-Passé (récent)**
> Dans une alcôve sèche, des os, des lambeaux de vêtement sombre, une ceinture utilitaire… et une poussière blanche (craie) comme un marquage.

- **Médecine** DD 15 : mort récente.
- **Perception** DD 16 : craie = signe menant vers un interstice sous dalle (à garder pour plus tard).

---

**3 voies de résolution**
1) **Convaincre (Influence)** : proposer une continuité de service.
2) **Désactiver** : **Artisanat DD 20** (DD 18 si panneau de purge trouvé : Artisanat DD 15 / Perception DD 16). Option : tâche complexe 3 succès avant 2 échecs.
3) **Combat** (1 seul maximum) : si forçage/attaque/échec critique.

**Écho de la Statue-Chaman (option, ambiance)**
- À jouer en chuchotements dans la condensation, pas en dialogue.
- *« …brume… brume… »*
- *« …ne me porte pas comme un trophée… porte-moi comme une mémoire… »*
- *« …l’eau se souvient… mais la pierre oublie… »*

```pf2e-stats
# Gardien des Écluses — « Unité de Maintenance 7 »
## Niveau 2
---

==Construit== ==Aethelgard==

Automate de maintenance chargé de préserver l’irrigation. La **Statue-Chaman** sert de remplacement au module d’humidification.

**Perception** +7
**Artisanat** +10, **Société** +6, **Arcana** +8
**Volonté** +8

---
**Historique** Mission non révoquée : « maintenir débit, pression, humidité ».
**Apparence** Métal couvert de dépôts calcaires ; joints sifflants ; lentilles laiteuses.
**Personnalité** Littéral, inflexible, peut re-prioriser si on démontre une nouvelle réalité.
**Oral, signe distinctif** Voix de protocole : “PARAMÈTRES”, “DÉFAUT”, “TEST DE DÉBIT”.

---
**Découverte** Artisanat DD 14 (hydraulique), Arcana DD 16 (brume non-standard), Perception DD 18 (scan outils/statue)
**Compétences d'influence** Artisanat DD 18 (pièce de rechange), Société DD 18 (prouver l’effondrement), Diplomatie DD 18 (10 + Volonté), Arcana DD 19 (brume/statue)
**Influence 2.** Mission : maintenir l’irrigation, empêcher retrait d’élément critique.
**Influence 4.** Pièce d’origine brisée ; statue = “remplacement”.
**Influence 6.** Extraction autorisée si **remplacement** installé + test de débit.
**Influence 8.** Mode archive : plan simplifié des vannes ; PJ consignés comme “techniciens externes”.
**Influence 10.** « MÉMOIRE CRÉATEURS : PERDUE ». Dérive des horloges / archives effacées : plus de référence sur ses “créateurs” ; il ne sait plus *à qui* transmettre la maintenance.
**Résistances.** Menaces/vandalisme/arrachement : +3 DD, déclenche défense.
**Faiblesses.** Montrer une pièce + démonstration : −2 DD.
```

**Speech (Gardien)**
- *« DÉFAUT : MODULE D’HUMIDIFICATION. REMPLACEMENT INSTALLÉ. STATUT : STABLE. »*
- *« PRÉSENTEZ PLAN DE CONTINUITÉ. TEST DE DÉBIT REQUIS. »*

**Test de débit (si Influence ≥ 6)**
- **Artisanat** DD 15 (10 min) pour poser un remplacement temporaire et lancer le test.
  - **Succès** : le Gardien valide la continuité → extraction autorisée.
  - **Échec** : fuite / pression instable → le Gardien exige une correction (+1 DD cumulé sur Influence/Désactivation, max +3).
  - **Échec critique** : procédure de défense (à n’utiliser que si tu veux *vraiment* le combat).

> [!statblocks|columns]
>>```pf2e-stats
>># Gardien des Écluses (mode Défense)
>>## Créature 3
>>---
>>
>>==Moyen== ==Construit== ==Aethelgard==
>>
>>**Perception** +9; vision dans la brume (ignore dissimulation due à brume non-magique)
>>**Langues** —
>>**Compétences** Artisanat +10, Athlétisme +9
>>**For** +5, **Dex** +1, **Con** +5, **Int** +0, **Sag** +2, **Cha** −2
>>---
>>**CA** 20; **Vig** +12, **Réf** +8, **Vol** +10
>>**PV** 70; **Résistances** physique 3 (sauf adamantine)
>>---
>>**Vitesse** 20ft
>>
>>**Corps à corps** `[one-action]` poing-piston +13, **Dégâts** 2d6+5 contondant
>>
>>**Jet de vanne (pression interne)** `[two-actions]` (eau) Ligne 30 ft ; **DD 19 Réflexes**.
>>**Succès critique** aucune
>>**Succès** 1d6 contondant et repoussée 5 ft
>>**Échec** 3d6 contondant, repoussée 10 ft et **à terre**
>>**Échec critique** 3d6+5 contondant, repoussée 15 ft et **à terre**
>>---
>>```
>
>>```pf2e-stats
>>**Brumisation de maintenance** `[one-action]`
>>Le gardien libère une brume épaisse (burst 10 ft). La zone devient **dissimulée** jusqu’au début de son prochain tour.
>>
>>---
>>
>>**Priorité : Élément critique** `[reaction]`
>>**Déclencheur** une créature interagit avec la Statue-Chaman ou tente de l’extraire.
>>
>>Le gardien effectue immédiatement un **poing-piston**. En cas de **succès**, la créature lâche l’objet.
>>```

### Scène 5 : Remerciements Kroass-goll

> Quand la Statue-Chaman est enfin libérée, la brume change. Elle ne disparaît pas — elle se **réorganise**.
> Uuroch s’agenouille, pose ses paumes sur l’argile sombre, et murmure un chant presque inaudible. Autour, les Kroass-Goll répondent en cadence.
> *« Vase-vrai… peau-sèches. Ce Kroass… n’oublie pas. »*
> Uuroch tend une amulette aux PJ.

**Clôture**
- Rituel bref ; Uuroch repart vite.
- Donner **2 rumeurs** + 1–2 récompenses.

## Rumeurs possibles

- **« Le Marais saigne »** : des [[Cisarelles]] harcèlent les routes d’eau Kroass-Goll (piste : **sud**).
- **« D’autres peaux-sèches »** : [[Gobe'liés]] (sud/sud-ouest) ; [[Loge des Sans-Passé]] (craie puis disparition).

## Butin / Récompenses

- **Yeux de la Brume (lunettes)** — *Niv. 3* : +1 bonus d’objet à la **Perception** (repérage dans brume/obscurité légère).
- **Bottes de Roseau** — *Niv. 3* : 1/j, 10 min, ignorer terrain difficile dû à boue/eaux peu profondes.
- **Amulette « Vase-vrai »** — *Niv. 4* : +1 bonus d’objet à **Déceler un mensonge** ; 1/j, réaction quand on te ment directement → sensation brève de “saveur de vase”.

## À reporter / Prépa prochaine

- Réactions de [[Port-Lointain]] à un premier contact Kroass-Goll (outils/sel ? pacte ?).
- Exploiter l’indice **Sans-Passé** : marquage à la craie + interstice sous dalle.
- Si combat : noter l’état du système d’irrigation (stable / dégradé) et les conséquences locales.
