---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 5
code: S005
date_irl: 2026-03-15
fc-date: 2942-05-25
fc-end: 2942-05-27
resume: "Korvax, parti seul en reconnaissance de la grotte, n'est pas revenu. Les autres membres de l'Expédition ont donc une double mission : retrouver Korvax et explorer la grotte repérée lors d'une mission précédente. Cette grotte est occupée par des Gobeliés. Elle contient également le \"Fer Trompeur\", un minerai magique qui laisse apparaître des échos du passé..."
pjs:
  - "[[Campagnes/EFG/PJ/Chiro Kono.md|Chiro Kono]]"
  - "[[Campagnes/EFG/PJ/Fenn Brindebois.md|Fenn Brindebois]]"
  - "[[Campagnes/EFG/PJ/Voss Vitriox.md|Voss Vitriox]]"
  - "[[Campagnes/EFG/PJ/Korvax Oeil-de-fer.md|Korvax Oeil-de-fer]]"
updated: 2026-03-14
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

## TODO

- [x] Battlemap grotte (5 pièces)
- [x] Statblocks Gobeliés (maille + big boss) + araignées
- [x] Dangers : descente falaise, toiles/cocons, traversées du rift, chaleur/lave, échos du Fer Trompeur
- [x] Handouts : carte des territoires (Gobeliés/Cisarelles) + message + miroir (vision d'Aethelgard)
- [x] Butin/récompenses (échantillons de Fer Trompeur, fragments d'artefacts)

## Intro

> Nyssor... 
> Au-delà de la Couronne Blanche, s'étendent des terres sans cartes et des ruines sans noms.
> Bienvenue, **éclaireur** de l'Expédition des Fendeurs de Glace. On vous envoie là ou les palissades s'arrêtent : explorer l'inconnu, découvrir des ressources, repousser les menaces ou nouer des alliances quand c'est possible. Et ramener à Port-Lointain ce que l'on ne peut pas cultiver : des réponses.

## Aperçu de la session
- Double objectif : retrouver [[Korvax Oeil-de-fer]] et explorer la grotte de l'hex [[0413]] (rumeur : [[Le Fer Trompeur]]).
- La grotte est occupée par une maille de [[Gobeliés]] (Maille « Reflet-Suie »), qui exploite des veines de Fer Trompeur.
- Exploration en « 5 room dungeon » (pièces, pas scènes) : vie de la Trame, nid, rift/lave, bureau du Tisse-Chef, grand gisement.

> [!gm] Noms
> **Maille :** Reflet-Suie (soie grise/noire, motif de vagues concentriques comme un miroir trouble).
> **Big boss :** Tisse-Chef Nirkz « Carto-Fil » (pragmatique, curieux du monde de surface, araignée-jumelle : « Dagueuse »).

## Pièces (5-room dungeon)

### Pièce 1 - La grande cavité (centre de vie)

> Le tunnel s'ouvre sur un vide soudain. En contrebas, une grande cavité respire d'un souffle tiède, humide, chargé d'une odeur de laine et de fumée froide.
> Vous êtes sur un chemin en surplomb ; à gauche, une falaise d'environ trois mètres plonge vers le sol de la salle. Plus loin, le même chemin continue en pente et rejoint l'ouest de la cavité.
> En bas, la vie gobeline est exposée sans pudeur : un enclos de fortune où des moutons se serrent, une « cuisine » faite de pierres noircies et de broches, des tables basses, des couchettes de soie tendue.
> Partout, des fils de toile vibrent à la moindre goutte. Dans les parois, des veines d'un métal noir luisent par endroits, comme si la roche avait gardé une mémoire.
> Près de l'enclos, une cage circulaire est suspendue au plafond par des cordes de soie ; à l'intérieur, un corps bouge à peine.

> [!gm] Notes
> - Korvax est dans la cage suspendue (clef sur le big boss; sinon corde/soie a couper).
> - Les veines de Fer Trompeur ici sont fines : chuchotements faibles, sensation de « reflet » dans la vision périphérique.

### Pièce 2 - Le nid des araignées

> Une ouverture sur la droite donne sur une alcôve étouffée, comme si la grotte retenait son souffle.
> La lumière se casse dans des couches de toiles superposées. Des cocons pendent du plafond et des parois, certains à taille d'animal, d'autres plus petits, serrant ce qu'ils contiennent comme des poings.
> Au fond, un nid : un amoncellement d'œufs laiteux, luisants, à moitié enfouis dans la soie. Chaque pas colle un peu au sol.
> Dans la roche, le métal noir affleure sous les toiles, comme une cicatrice.

> [!gm] Notes
> - Si les PJ s'approchent trop près des oeufs sans faire attention, ils éclosent et font pop une "nuée d'araignées"

### Pièce 3 - Le puits de lave (rift + dépotoir)

> La galerie débouche dans une salle coupée net par un rift profond.
> Tout en bas, une lueur orange pulse lentement ; de la lave coule comme un sang lourd, et l'air porte une chaleur sèche qui racle la gorge.
> Du côté proche de la grande cavité, un tas d'ossements, de peau salée et de crasse gobeline forme un dépotoir. Une odeur nauséabonde s'en dégage.

### Pièce 4 - Le bureau du big boss (quartiers du Tisse-Chef)

> L'air change. Un écoulement d'eau naturel chante sur la pierre, régulier, presque rassurant.
> La caverne est organisée : un bureau fabriqué à partir de planches récupérées, un siège étonnamment confortable, et un lit de soie tendue et de peaux.
> Des cordes de toile forment des étagères, des suspensions, des petits paquets noués ; ici, chaque nœud a un sens.
> Près du mur, un espace à l'écart est réservé à une araignée : une zone de toile tendue, propre, avec des restes de nourriture soigneusement rangés.
> Dans la paroi, le métal noir trace des lignes fines, comme des runes sans langue.

> [!gm] Contenu trouve
> - **Carte** : territoire des [[Gobeliés]] + zone revendiquée par les [[Cisarelles]].
> - **Message** : *« Fouille la forêt pour chercher la Sorcière. Ramène-la vivante. Si elle parle, coupe-lui la langue. »*

### Pièce 5 - Le gisement de Fer Trompeur (la mémoire dans la pierre)

> Au-delà du rift, la grotte s'élargit en une grande cavité brisée par des éboulis.
> Les parois sont rayées de veines noires, nombreuses, épaisses.
> Des fragments d'artefacts sont pris dans la roche : une arête de métal aux angles trop parfaits, une plaque fissurée couverte de motifs presque géométriques, un anneau tordu que la pierre n'a pas réussi à avaler.
> Plus vous avancez, plus l'air semble « charger » vos pensées. Les ombres ne suivent pas vos mouvements. Vous avez la sensation absurde qu'il y a des silhouettes juste derrière vous.

> [!gm] Le miroir (recompense / indice)
> **Effet de narration :** dans son reflet, on voit des habitants d'une ancienne ville d'[[Hégémonie Aethelgard|Aethelgard]] au moment du cataclysme (silhouettes, rues, peur).
> **Interprétation (option) :** Occultisme (16) -> un détail utile (symbole, nom, direction) ; critique -> deux détails.

## Indices / Pistes
- Carte des territoires (Gobeliés vs Cisarelles) -> préparation de futures rencontres.
- Message sur la « sorcière » en forêt -> [[La Sorcière Gentille]]


## À reporter / Prépa prochaine
- Les PJ ont **sauvé [[Korvax Oeil-de-fer]]** et l’ont ramené vivant.
- La **grotte des Gobe’liés est presque vidée** : Crux est le dernier survivant du groupe local.
- Les PJ ont **négocié une coopération avec [[Krux]]** plutôt que de le tuer.
- Krux a accepté :
    - de **construire une passerelle** au-dessus du gouffre,
    - de **prévenir les autres Gobe’liés** que les PJ peuvent être des alliés.
- Les PJ connaissent maintenant le **code secret gobelin** :
    - « Il n’y a que maille qui maille. »
- Les PJ ont promis de **revenir aider contre les “fantômes”** (fumées noires volantes) qui hantent la zone.
- Les PJ ont découvert :
    - une **zone au-delà du gouffre** encore inexplorée,
    - une **grande araignée** qui vit plus loin dans la grotte.

