---
id: synode-mechanis
type: organisation
categorie: faction
region: "[[Nyssor]]"
faction:
aliases:
  - Synode
tags:
  - organisation
  - categorie/faction
updated: 2026-02-10
reputation: 0
---

```meta-bind
INPUT[progressBar(title('Réputation de la Concorde'), minValue(-100), maxValue(100), defaultValue(0), stepSize(1)):reputation]
```

> *« Si cela ne peut pas être réparé, cela n’a pas été compris. »*

![[Image.webp|banner]]

## Résumé

![[Image.webp|loc left profile medium]]

| Type de faction | Cohésion | Méthodes |
| --- | --- | --- |
| faction | Forte | ingénierie, contrats, prototypes, forge par résonance |

Le **Synode Mechanis** est une alliance de bâtisseurs et de maîtres-artisans souterrains, unis par une valeur centrale : l’**EFFORT** (Endurance, Force, Façonnage, Œuvre, Résilience, Transmission). Ils ont maîtrisé le **Vitrosol** (verre noir ébène) et arraché aux profondeurs un métal né d’une météorite : le **Siderium**, insensible à la magie et façonnable uniquement par **résonance**.

### Origines — Vitrosol, impact et Siderium
Avant la Saison du Feu, des tribus artisanes vivaient dispersées dans les dunes de **Qal’Rhaz**. Une campagne de fouilles révéla le **Vitrosol**, matériau résistant et isolant, permettant de bâtir des structures souterraines capables d’endurer des chaleurs extrêmes.

Lorsque la surface devint inhabitable, ces cités enfouies tinrent bon… jusqu’à l’**impact** : une masse céleste frappa les profondeurs vitrifiées, fissurant et ensevelissant des galeries entières. Les survivants stabilisèrent leur monde par calcul et acharnement, puis explorèrent le cratère : ils y découvrirent le **Siderium**, métal sombre né de la fusion du Vitrosol et de la météorite.

De la maîtrise du Vitrosol et de l’écoute du Siderium naquit le Synode.

### Valeurs
La magie et la religion sont tolérées mais non centrales : *« La Magie contourne, la Foi espère, l’Effort bâtit. »* La valeur d’un individu se mesure à ce qu’il produit, maintient et transmet.

### Coutumes majeures
- **Manuscriptum** : grand registre consignant individus, projets, lois, décisions (gardé par la guilde du **Registre**).
- **Assignation** : épreuve fondatrice ; les adolescents doivent réaliser une œuvre en autonomie (résultats consignés).
- **Poids de l’Œuvre** : célébration d’un projet majeur ; décorations de guilde, démonstrations, offrandes versées dans une “balance” géante.

### Communication & société
Réseaux de **tubes acoustiques** en métal dans les galeries ; à la surface, signaux de fumée minérale et éclats au miroir de Vitrosol. Culture bruyante et conviviale : le vacarme est la preuve que “tout fonctionne”.

### Guerre
Le champ de bataille est un atelier : armures massives renforcées de Vitrosol, armes mécaniques (et prototypes), signaux visuels/mécaniques, formations compactes. Après chaque combat : analyse technique, collecte de données, itération.

L’élite peut être équipée d’éléments en **Siderium** : soldats anti-magie, lourds et redoutables.

### Habitat & apparence
Ville souterraine taillée dans le Vitrosol, divisée en quartiers de guildes ; centre industriel : **le Cratère** (Siderium). Cœur social : **la Confluence** (réfectoires, halles, annonces, démonstrations). Tenues utilitaires, modulaires, marquées par l’outil ; prothèses et cicatrices sont normales.

### Étrangers
Les étrangers sont acceptés s’ils ont une utilité claire. Commerce encouragé mais encadré : contrats consignés par le Registre. Le **Vitrosol** peut s’exporter sous contrôle ; le **Siderium** n’est **jamais** vendu.

## Buts & méthodes

|  |  |
| --- | --- |
| **Court terme** | - Protéger le **Manuscriptum** et les ateliers (brevets, méthodes).<br>- Stabiliser les zones fragilisées et sécuriser le **Cratère** (Siderium).<br>- Identifier l’origine des vols de brevets. |
| **Long terme** | - Perfectionner la forge par **résonance** et les infrastructures en Vitrosol.<br>- Préserver l’indépendance technique (contrats, secrets, contrôle des matériaux). |
| **Tabous / lignes rouges** | - Sabotage d’infrastructure (galeries, ventilation, Cratère).<br>- Vol/altération du **Manuscriptum** ou de plans majeurs.<br>- Tentative d’exportation ou d’accès non autorisé au **Siderium**. |

## Territoire & influence

```leaflet
id: synode-mechanis-map
lock: true
darkMode: false
image: [[Nyssor.webp]]
bounds: [[0,0], [4096,4096]]
height: 400px
width: 95%
lat: 2048
long: 2048
unit: km
scale: 1
minZoom: -2
maxZoom: 2
defaultZoom: 0
zoomDelta: 0.5
```

Le Synode est un bastion souterrain : son influence se manifeste par le contrôle de matériaux (Vitrosol) et par des contrats d’ingénierie… mais ses accès profonds restent verrouillés.

## Organisation interne

Les membres du Synode sont les **Qalhars** (habitants de Qal’Rhaz). L’organisation est guildée : chaque guilde occupe/optimise une partie de la cité.

### Guildes
- **Porte-Piliers** : tunneliers et bâtisseurs
- **Résonants** : forgerons (résonance)
- **Façonneurs** : autres artisans
- **Vigie** : protection et justice
- **Négoce** : commerce
- **Registre** : archives, lois, décisions

### Gouvernance
L’ensemble des chefs de guildes forme le **Rouage**. Le dirigeant suprême, le **Premier Artifex**, est élu par le **Registre** (membres choisis par les autres guildes, au nom de la neutralité).

### Hiérarchie (au sein d’une guilde)
| Caste / Rang | Rôle | Description | Particularité |
| --- | --- | --- | --- |
| **Premier Artifex** | Dirigeant | Coordonne le Synode au nom du Rouage. | Destituable par vote exceptionnel. |
| **Chefs de Guilde (Rouage)** | Gouvernance | Représentent et arbitrent les fonctions majeures. | Pouvoir collectif. |
| **Maître Compagnon** | Rang suprême | Artisan d’exception, valide méthodes, représente la guilde. | Juge l’excellence. |
| **Scelleur d’Œuvre** | Chef de projet | Compagnon dévoué à une œuvre ambitieuse. | Signe une œuvre. |
| **Régulateur** | Encadrement | Responsable d’ateliers/chantier ; qualité et sécurité. | Garant des méthodes. |
| **Mécano** | Opérationnel | Exécute et maintient ; peut encadrer des Main-Neuves. | Autonomie sur tâches définies. |
| **Main-Neuve** | Apprenti | Observe et assiste sous supervision stricte. | Ne signe aucune œuvre. |

## Relations
- **Alliés :**
- **Rivaux :**
  - [[Sceau Arcanique]] (catalyseur vendu puis refus de fournir davantage ; tension)
- **Neutres / opportunistes :**

## Notes MJ
> [!gm] Secrets, leviers, plans
> - Le Synode a vendu un **catalyseur** au [[Sceau Arcanique]] contre une somme astronomique ; depuis, il rechigne à en fournir d’autres.
> - [[Kaelen, l'Architecte de Fer]] est un **ex-ingénieur du Synode**, banni pour ses expériences non-éthiques ; il œuvre désormais pour [[Varkesh, le Héraut du Silence]] (Acte 2) et cherche à obtenir des [[Cristaux d’Ether]] pour son chantier.
> - Rumeurs : **fragilisation** de zones profondes et **créatures gigantesques** sous les dunes.
> - Vols de brevets : paranoïa, purges, fausses accusations… ou infiltration réelle.
