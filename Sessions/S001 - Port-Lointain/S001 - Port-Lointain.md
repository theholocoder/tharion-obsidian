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

## Scènes (notes MJ)
- **Pitch** : première soirée à [[Port-Lointain]]. Les PJ découvrent l’abondance (comparée à [[Kaerith]]), puis la ville passe en mode survie : attaque des [[Cisarelles]].
- **Structure** : “five-room dungeon” urbain.
  - **Room 1** (intro) : taverne **L’Hydre à Deux Choppes**.
  - **Room 2/3/4** (semi-ouvert) : trois crises à résoudre **dans l’ordre voulu**.
  - **Room 5** : convergence sur la place du marché, climax et retrait coordonné.

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
