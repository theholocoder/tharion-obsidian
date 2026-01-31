---
type: scene
parent: "[[S001 - Port-Lointain]]"
tags:
  - scene
  - lieu
---

# Scène 3c - Entrepôt des docks

`BUTTON[btn-001-scene2]` `BUTTON[btn-001-home]` `BUTTON[btn-001-scene3,btn-001-scene3b,btn-001-scene3c]`
```meta-bind-button
style: primary
label: < Scène 2 - Commandant Aelys Tarn
id: btn-001-scene2
hidden: true
actions:
  - type: open
    link: "Scène 2 - Commandant Aelys Tarn"
```
```meta-bind-button
style: primary
label: Scène 3a - La Porte de la Noue >
id: btn-001-scene3
hidden: true
actions:
  - type: open
    link: "Scène 3a - La Porte de la Noue"
```
```meta-bind-button
style: primary
label: Scène 3b - Rue Gelevrod >
id: btn-001-scene3b
hidden: true
actions:
  - type: open
    link: "Scène 3b - Rue Gelevrod"
```
```meta-bind-button
style: primary
label: Scène 3c - Entrepôt des docks >
id: btn-001-scene3c
hidden: true
actions:
  - type: open
    link: "Scène 3c - Entrepôt des docks"
```
```meta-bind-button
style: primary
label: S001 - Port-Lointain
id: btn-001-home
hidden: true
actions:
  - type: open
    link: "../S001 - Port-Lointain"
```

## Description

>Un entrepôt massif en bois sombre, aux poutres robustes et au sol en terre battue. L'air est épais d'odeurs de sel, de viande séchée et de poisson fumé. La lumière des lampes à huile vacille sur des rangées immenses de caisses et de barils.
>Les caisses et les étagères de l'entrepôt ont été pillées ou saccagées. La poussière soulevée et les copeaux de bois jonchant le sol forment des empreintes insectoïdes au sol. Dans un coin de l'entrepôt, un tissus immense, probablement une voile à moitié dépliée, est soulevée légèrement par le vent. 

## Points d'intérêt

### Adaptation temporelle selon le timer

| Tours écoulés | Phase                       | État de la scène                                                                                                                                           | Nouveaux éléments                                                                                                                                                 |
| ------------- | --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **X+ tours**  | **L'Assaut en cours**       | Les Cisarelles sont encore en train de prélever la nourriture. Les PJ arrivent au milieu de l'action.                                                      | Combat possible, communication visible en temps réel, témoin en danger immédiat.                                                                                  |
| **X+ tours**  | **La Retraite coordonnée**  | Au moment où les PJ entrent, toutes les Cisarelles gèlent simultanément pendant 3-4 secondes, puis partent en parfaite synchronisation vers le nord-ouest. | Observation du signal de retraite, témoin sauvé mais traumatisé, indices encore "chauds".                                                                         |
| **X+ tours**  | **Le Silence post-attaque** | L'entrepôt est vide et silencieux. Le témoin s'est enfui.                                                                                                  | **Mue complète découverte** : une exuvie entière, encore flexible - révélation biologique majeure. Indices "froids" mais plus détaillés possibles pour l'analyse. |

### **A** : Les caisses de salaison violées

**Tests possibles :**
- **Médecine/Nature DC 15** : Identifier une sélection alimentaire ciblée, suggérant des besoins nutritionnels spécifiques
- **Perception/Survie DC 15** : Remarquer de fines entailles sur les bords des caisses, comme si des pinces acérées les avaient découpées
- **Perception DC 17** : Remarquer une seule caisse non endommagée, mais avec un sceau de la [[Ligue de Veyra]] à moitié dissimulé sous la poussière, rumeur [[Le Marché Secret]]
- **Détection de la Magie** : Senser une faible aura d'illusion sur cette caisse spécifique, comme si un sort la rendait "invisible à l'attention", rumeur [[Le Marché Secret]]

**Indices visibles :**
- Certaines caisses sont complètement vidées, d'autres ne présentent que des morceaux très spécifiques manquants
- Les morceaux prélevés sont principalement des abats riches en protéines, des parties grasses et des organes internes
- Les morceaux maigres sont systématiquement laissés sur place, comme s'ils étaient sans intérêt
- Une caisse discrètement marquée du sceau de la [[Ligue de Veyra]], intacte mais protégée par magie

**Révélation :** Intelligence et organisation dans la collecte de nourriture, mais aussi présence suspecte d'une cargaison protégée de la Ligue de Veyra

### **B** : Les traînées synchronisées 

**Tests possibles :**
- **Survie DC 16** : Comprendre le mode de déplacement coordonné et estimer le nombre de créatures (3-4 individus)
- **Perception/Nature DC 14** : Identifier les fragments d'exuvie comme des mues d'insectes géants
- **Arcanes/Occultisme DC 17** : Senser une étrange résonance dans l'air, comme un "écho" de communication psionique

**Indices visibles :**
- Pas de traces désordonnées, de glissades ou de bousculades
- Les traînées forment des motifs géométriques, suggérant un déplacement coordonné
- Fragments brillants d'exuvie (mue) parsemés le long du chemin

**Révélation :** Mouvement synchronisé, coordination parfaite, biologie insectoïde évoluée

### **C** : Le témoin caché

**Dialogue potentiel :**
> *"Elles... elles se sont arrêtées toutes en même temps ! Comme si quelqu'un avait sifflé, mais sans aucun son. Leurs antennes... elles ont vibré ensemble, puis... elles sont parties. Dans la même direction. Sans se regarder, sans rien se dire. C'était... terrifiant."*

**Révélation :** Communication non-verbale, hiérarchie, signal de retraite coordonné

> [!statblocks|columns]
>>```pf2e-stats
>># Eliror Thruwin Stromo
>>## Niveau 0
>>---
>>
>>==Petite== ==Gnome==
>>
>>Un employé des entrepôts de Port-Lointain, terrifié mais témoin oculaire direct de la coordination des Cisarelles.
>>
>>**Perception** +3
>>**Artisanat** +4, **Intimidation** +2
>>**Volonté** +6
>>
>>---
>>**Historique** Employé des entrepôts depuis l'arrivée à Port-Lointain, spécialisé dans le tri et la conservation des denrées. A vu plusieurs attaques de créatures mais jamais rien d'aussi organisé. Vit seul dans le quartier du Rempart.
>>**Apparence** Petit et nerveux (1m10), doigts fins et habiles marqués par le travail de triage. Porte des lunettes de protection et une tunique de bureau adaptée aux entrepôts. Cheveux en bataille, regard perçant mais fatigué.
>>**Personnalité** Meticuleux, anxieux, observateur.
>>**Oral, signe distinctif** Voix aiguë qui tremble quand il est stressé. Cligne des yeux fréquemment, joue avec un petit outil de tri quand il réfléchit.
>>```
>
>> ```pf2e-stats
>>**Découverte** Perception DD 15 (remarquer sa présence), Médecine DD 13 (état de choc), Connaissances (Entrepôts/Docks) DD 11/Artisanat DD 14 (vêtements et outils d'un spécialiste du tri et conservation)
>>**Compétences d'influence** Duperie DD 14 (se faire passer pour un secouriste ou une autorité médicale), Intimidation DD 16, Diplomatie DD 16 (l'approcher calmement, valider sa peur ou reconnaître son expertise professionnelle),  Persuasion DD 18 (le convaincre que son témoignage est vital pour la sécurité de Port-Lointain et que les autorités ont besoin de son aide)
>>**Influence 2.** Description précise du comportement des Cisarelles (coordination, sélection ciblée des aliments).
>>**Influence 4.** Révélation qu'il a vu une créature plus grande diriger les autres depuis l'ombre d'une poutre, **ET** il mentionne nerveusement une caisse "spéciale" marquée de la Ligue de Veyra qui n'a pas été touchée par les Cisarelles ([[Le Marché Secret]]).
>>**Influence 6.** Information détaillée sur la substance résineuse laissée sur les caisses et sa propre expérience des marquages territoriaux d'insectes géants. **ET** il avoue, en regardant autour de lui, avoir déjà vu des représentants de la Ligue de Veyra récupérer discrètement des caisses similaires ces dernières semaines. Il a trop peur pour en dire plus. ([[Le Marché Secret]]).
>>**Résistances.** Approche agressive (+3 au DD), langage militaire/technique (+2 au DD), ignorer son expertise professionnelle (+2 au DD)
>>**Faiblesses.** Approche médicale (-3 au DD), valider son travail d'expert (-2 au DD), protection promise (-2 au DD)
>>```

## Butin / Indices
- **Fragments d'exuvie** : Matériau biologique rare (1 unité, worth 10po)
- **Marquage phéromonal** : Substance résineuse sur les caisses
- **Indices alimentaires** : Comprendre le régime ciblé des Cisarelles
- **Témoignage direct** : Observation du hive mind en action
- **Piste Ligue de Veyra** : Caisse suspecte avec sceau de la Ligue et protection magique, activités suspectes de récupération discrète

---

> [!gm] Note pour le MJ
> Chaque phase offre une expérience différente mais mène à la même conclusion : les Cisarelles sont organisées, intelligentes et coordonnées par une entité centrale. L'ordre des scènes influence la manière dont les PJ découvrent cette vérité, mais pas la vérité elle-même.
