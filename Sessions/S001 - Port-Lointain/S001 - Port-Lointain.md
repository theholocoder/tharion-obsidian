---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 1
code: S001
date_irl: 2026-02-01
date_ig_debut: 08/11/42
date_ig_fin: 08/11/42
pjs:
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Chiro Kono.md|Chiro Kono]]"
  - "[[Campagnes/EFG/PJ/Théobald Greyheart.md|Théobald Greyheart]]"
  - "[[Campagnes/EFG/PJ/Voss Vitriox.md|Voss Vitriox]]"
  - "[[Campagnes/EFG/PJ/Yoko.md|Yoko]]"
  - "[[Campagnes/EFG/PJ/Lyra.md|Lyra]]"
  - "[[Campagnes/EFG/PJ/Noctis.md|Noctis]]"
  - "[[Myca Libre-Spore]]"
  - "[[Campagnes/EFG/PJ/Fenn Brindebois.md|Fenn Brindebois]]"
  - "[[Campagnes/EFG/PJ/Korvax Oeil-de-fer.md|Korvax Oeil-de-fer]]"
resume: ""
updated: 2026-01-09
termine: false
---
## Informations sur la session

**Date IRL :** `INPUT[datePicker:date_irl]` | **Début IG :** `INPUT[text(placeholder('2942-11-08')):date_ig_debut]` | **Fin IG :** `INPUT[text(placeholder('2941-11-10 / vide')):date_ig_fin]` | **Terminée ?** `INPUT[toggle:termine]`

```meta-bind
INPUT[textArea(title('Résumé de la session en 2-5 phrases max. ')):resume]
```

```meta-bind
INPUT[listSuggester(title('Personnages'), optionQuery("Campagnes/EFG/PJ")):pjs]
```

---

## Précédemment
> (dynamique) Affiche le `resume` de la session précédente dès qu’il est rempli.

```dataview
TABLE WITHOUT ID resume
FROM "Sessions"
WHERE type = "session"
  AND campagne = "EFG"
  AND numero = this.numero - 1
LIMIT 1
```

---

## TODO

- [ ] Audio bourdonnements + cloches d'alarme
- [ ] Battlemaps
- [ ] Intro + musique d'intro pour la campagne
- [ ] Handout: document du [[Conseil de la Brèche]] indiquant que si le PJ permet la destruction des Mantes Géantes, le conseil lui accordera un droit de propriété sur la parcelle de son choix dans le quartier des Hautes-Terrasses ou le terrain de son choix au delà des murs de la ville. Ils gagneront également le rang d'Eclaireur

## Intro

> TODO



## Aperçu de la session
Les joueurs sont arrivés depuis peu à [[Port-Lointain]], ils sont réunis dans la taverne [[L'Hydre à Deux Choppes]]. Ils sociabilisent et découvrent l'abondance de [[Nyssor]] lorsqu'ils sont interrompus par un bourdonnement et les cloches d'alarmes : les [[Cisarelles]] attaquent la ville.

### Scènes
```dataview
TABLE WHERE type = "scene" AND contains(file.folder, this.file.folder) SORT file.name
```

![[Scène 1 - L'Hydre à Deux Choppes]]

![[Scène 2 - Commandant Aelys Tarn]]



---

### Room 1 — L’Hydre à Deux Choppes (Intro & RP)
- Décrire odeurs (viande rôtie, pain), bruit, optimisme des colons.
- Laisser les PJ se présenter.
- Déclencheur : bourdonnement grave, cloches du port, cri coupé net.

### Sortie & Ordres — [[Commandant Aelys Tarn]]
- Aelys est dehors, entourée de soldats. Elle **ordonne**, ne harangue pas.
- Elle donne l’objectif : tenir la ville et traiter **trois points de crise**.

**Principe : le temps passe vraiment.** Si les PJ laissent une room “pour plus tard”, ils y arrivent quand la situation a empiré.

**Règle pratique (impro)** : après chaque room résolue, fais avancer les autres rooms d’un cran sur **Léger → Grave → Catastrophe**. À *Catastrophe*, l’objectif n’est plus “sauvable” : seulement limiter la casse + récolter des indices.

### Room 2 — Carrefour des quais (tenir une ligne)
- Enjeu : empêcher l’essaim d’entrer dans les habitations.
- Terrain : passerelles glissantes, chariots renversés, filets.
- Indice : une Cisarelle neutralisée **vibre** ; des Cisarelles plus loin changent de cap comme sur un ordre muet.
- **Si les PJ arrivent en dernier** : patrouille en retraite, quais perdus, **civils enlevés**, pertes matérielles.

### Room 3 — Dilemme : vivres ou vies
Deux sous-sites, au choix (ou les PJ essaient de tout faire, au prix du temps) :
- **Option A : feu aux vivres** (dépôt temporaire)
  - Indice : comportement de **collecte** (morceaux précis, réserves).
  - Si en dernier : dépôt brûlé, rations perdues, tensions dans la population.
- **Option B : civils piégés** (baraque barricadée)
  - Indice : micro-pause collective + repositionnement simultané (hive mind).
  - Si en dernier : adultes probablement morts, au moins une personne **enlevée**.

### Room 4 — Point d’attraction : entrepôt des salaisons
- Enjeu : comprendre *pourquoi ici* (sans révéler le Rituel).
- Indice : l’essaim lâche des proies faciles pour converger sur un point précis : **collecte/logistique**.
- Si en dernier : entrepôt “vidé”, traînées parallèles, témoin décrivant un arrêt synchronisé.

### Room 5 — Place du marché : climax & révélation implicite
- Une “cheffe” coordonne l’essaim via antennes/vibrations/stridulations.
- **Révélation hive mind** : au moment où elle est repoussée, arrêt net de l’essaim, une seconde de silence, puis retrait à l’unisson vers le nord-ouest.
- La corne du fort retentit *après* : signal humain tardif.
- Aelys fait un débrief : « des faits, pas des impressions ».

### Notes combat (à faire plus tard)
- Difficulté visée : **Modérée**.

#### Snatchers
1 [[Arracheuse Cisarelle]], 2 [[Chasseur Cisarelle]] et 1 [[Brute Cisarelle]]

#### Mutalide


## Événements / Décisions
- Les PJ choisissent l’ordre de résolution des crises (Room 2/3/4).
- Selon l’ordre : pertes de vivres, morts/enlèvements, dégâts logistiques aux quais.

## Indices / Pistes
- [[Cisarelles]] = faction (page à créer/importer).
- Indices “hive mind” : micro-pauses collectives, repositionnements simultanés, vibrations/antennes comme signaux.
- Indice “collecte/logistique” : elles privilégient nourriture/abats/salaisons plutôt que des cibles faciles.
- Piste long terme : enlèvements possibles → où emmènent-elles les vivants ?
## Butin / Récompenses
- 

## À reporter / Prépa prochaine
- Créer/importer la page [[Cisarelles]] (faction) + éléments sur le [[Rituel de Transmission]] (secret MJ).
- Finaliser rencontres/terrains + statblocks (inclure poison léthargique).
- Compléter [[Port-Lointain]] (note actuellement vide) avec quartiers/lieux utiles (quais, marché, entrepôts, palissade).

>D'abord, c'est juste une vibration lointaine, un murmure presque imperceptible sous les conversations animées de la taverne. Quelques missionnaires lèvent tête un instant, cherchant la source de cette vibration dans l'air, puis retournent à leurs choppes. Mais le son grandit, s'amplifie, devient un bourdonnement sourd et continu qui fait trembler les verres sur les tables. Le sol commence à vibrer sous vos pieds, le plafond en bois grince dans une plainte inconfortable. Les conversations toutes simultanément, remplacées par un silence de plus en plus lourd.
>Puis le bourdonnement explose en un assaut sonore déchirant, comme des milliers d'ailes de géant qui lacèrent le ciel simultanément. C'est un bruit qui éveille des terreur anciennes au fond de vos tripes. Les vitres des fenêtres se mettent à vibrer dangereusement, des objets tombent des étagères, et vous sentez la pression changer dans vos tympans. C'est à ce moment que la première cloche d'alarme se met à retentir depuis la Caserne, immédiatement rejoint par une deuxième, puis une troisième.
>Le bruit est partout maintenant, un vacarme qui semble venir de toutes les directions à la fois. Olgar a déjà disparu sous le comptoir pour attraper son marteau de guerre, tandis que Bruna se fige au milieu de la salle, son visage tourné vers l'extérieur comme si elle pouvait voir l'invisible apocalypse qui s'abat sur Port-Lointain. Les cloches continuent leur appel désespéré. C'est alors que les premiers cris commencent à percer les mur de la taverne - des cris de surprise, puis de terreur, venant de la rue dehors. Quelque chose est arrivé. Et le bourdonnement continue.

*Lorsque les joueurs sortent de la taverne, ils tombent nez à nez avec une [[Cisarelles|Cisarelle]] immense, Aelys Tarn la découpe en deux*

>En poussant la porte de la taverne, le PJ qui sort en premier se retrouve nez à nez avec l'horreur : un insecte, une mante religieuse géante, haute de trois mètres, sa carapace verte et noire brillant sous le soleil. Ses multiples yeux composés fixent leur nouvelle cible avec une curiosité glaciale, et ses faucilles tranchantes, longues comme des épées, se lèvent dans un mouvement sinistre, sur le point de s'abattre sur le PJ.
>Vous n'avez même pas le temps de sortir une arme qu'une silhouette déchire l'air sur votre gauche. Une épée bâtarde dessine un arc d'argent dans le dos de la créature, la lame s'enfonçant dans l'articulation entre le thorax et l'abdomen avec un bruit déchirant de carapace brisée. L'insecte pousse un cri strident. Le vacarme de mandibules frottantes s'arrête net quand l'épée achève sa rotation, découpant la créature en deux avec une puissance incroyable. Les deux moitiés du monstre s'effondrent sur le pavé dans un fracas glissant de fluides et de viscères, révélant votre [[Commandant Aelys Tarn]] debout, son visage impassible, son épée dégoulinante de sang verdâtre. Son regard se tourne vers vous.
>*"La ville est attaquée, vous êtes réquisitionnés"*