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

## Conseillers (1 par faction)

- [[Royaume d'Halvorn]] : Maela Briselame (Humaine) - logistique, ravitaillement, sécurité maritime.
- [[Ligue de Veyra]] : Orrin Sable-compte (Halfelin) - contrats, concessions, "rentabilité".
- [[République de Thaldris]] : Daria Kestrel (Naine) - doctrine, avant-postes, contrôle territorial.
- [[Ordre de Myrr]] : Saelwyn Aubeclaire (Elfe) - rites, serments, protection des innocents.

Note : ces conseillers ont l'oreille de leurs membres au Conseil (cf. [[Conseil de la Brèche]]).

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
- [[Ordre de Myrr]] : **bois encadré** (coupes "propres", zones interdites) et forte réserve sur le **fer** ("mémoire dans la pierre", présages, risques sociaux).

---

## Aides MJ (accroches de conversation)

- Halvorn : "combien de semaines avant la prochaine tempête ?" / "combien de barques, combien de fanaux ?" / "si ça tourne mal, comment on évacue ?"
- Veyra : "qui paie quoi, et qui contrôle quoi ?" / "quelles garanties ?" / "quelle contrepartie chiffrable ?"
- Thaldris : "ligne de défense" / "temps de réponse" / "point d'appui et champ de vision"
- Myrr : "qui protège-t-on en premier ?" / "quel serment, quel tabou ?" / "que sacrifie-t-on moralement pour survivre ?"

---

## Conséquences possibles (à cocher)

- [ ] Un site prioritaire est voté pour le village (ouvrir une mission "repérage + négociations + logistique").
- [ ] Une forme de traité kroass est fixée (qui signe, quelles clauses, quelles contreparties).
- [ ] Une priorité ressources est annoncée (bois vs fer) + une mesure d'encadrement (quotas, concessions, garde, tabous).
