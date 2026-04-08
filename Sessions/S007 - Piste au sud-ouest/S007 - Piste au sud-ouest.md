---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 7
code: S007
date_irl: 2026-04-07
fc-date: 30/05/42
fc-end: 30/05/42
resume: Les joueurs explorent la forêt au sud-ouest de Port-Lointain sur une mission proposée par Logan suite à un aperçu d'une carte lors de la session S002. Dans cette forêt se cache le Have des Sans-Visages, qui est aussi Le Marché Secret.
pjs:
  - "[[Campagnes/EFG/PJ/Chiro Kono.md|Chiro Kono]]"
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Lyra.md|Lyra]]"
  - "[[Campagnes/EFG/PJ/Théobald Greyheart.md|Théobald Greyheart]]"
  - "[[Campagnes/EFG/PJ/Noctis.md|Noctis]]"
updated: 2026-04-07
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

## Aperçu de la session
- Les joueurs explorent la forêt au sud-ouest de [[Port-Lointain]] sur une mission proposée par [[Logan]] suite à un aperçu d'une carte lors de la session [[S002 - Le Parapheur de Platine]].
- Dans cette forêt se cache le [[Have des Sans-Visages]], qui est aussi [[Le Marché Secret]]. [[Maera Voile-Court]], une Sans-Passé, les y accueille en disant aux PJ qu'il n'y a pas de grabuge ici et que tout le monde est bienvenu.
- Les PJ vont pouvoir commercer avec des marchands [[Kroass-Goll]], [[Gobeliés]] et même certains venant de [[Port-Lointain]] !
- Dans les ruines qui constituent le [[Havre des Sans-Visage]], il y a une grotte avec des ruines souterraines. Dans cette grotte sont exploités des [[Cristaux d’Ether]] et ils y sont vendus aussi.
- [[Aldren Var]], qui est l'homme habillé de vert et en capuche vu par [[Eliror Thruwin Stromo]] dans [[S001 - Notes]], se trouve précisément dans la grotte. Il échange avec un membre du [[Synode Mechanis]] : [[Kharza Qalhar]].

## Scènes
- 


## Événements / Décisions
- Avant d'arriver au [[Havre des Sans-Visage]], les PJ suivent des traces dans la forêt qui les mènent dans une embuscade du [[Le limier d'Ether|Limier d'ether]] une sorte de minotaure de feu. Ils parviennent à le tuer, le démon tombe en cendres. Trouvés dans les cendres : fragments d'un collier magique (cassé) + 3–4 maillons d'une chaîne noire — la chaîne prise en charge pour étude.
- Après le combat, exploration du site et déplacement rapide vers le camp/market de la grotte le même jour. [[Logan]] parvient à acheter un lingot de fer froid pour quasi rien auprès du marchand [[Kroass-Goll]] ([[Zong'Sel]]). [[Chiro Kono]] vole un sac au marchand [[Gobeliés]] ([[Tchak'Fil]]) : un sac magique contenant une code de soie d'araignée magique elle aussi.
- Ils finissent par se rendre dans la grotte, gardes de la grotte : gardes mécaniques (au moins 3 repérés) + gardes humains ; l'un s'appelle Quen'tin (plaisanteries/échos).
- Personnage en capuche verte aperçu discutant avec l'homme en armure cuivrée. 
- Marchands de la grotte : vendent cristaux (usage/valeur magique), négociation possible en objets/valeurs alternatives.
- Les PJ ayant été repérés par [[Aldren Var]] et [[Kharza Qalhar]], [[Aldren Var]] s'enfuit de la grotte sans laisser de traces.

## Indices / Pistes
- Une carte locale montre un tracé menant loin au sud‑est (le désert du [[Synode Mechanis]]).
- [[Maera Voile-Court]] indique aux PJ que son peuple est là depuis bien plus longtemps qu'eux. Ils ne viennent pas de quelque part, ils sont nés ici.

## Butin / Récompenses
- Transactions et récupérations : Logan acquiert un lingot de "fer froid" (lingot ajouté), Chiro vole une sacoche (succès), Jester prend la chaîne noire pour étude, Chiro récupère le fragment cassé du collier de domination du limier d'ether cassé pour réparation.

## À reporter / Prépa prochaine
- Chaîne noire et collier cassé
- La carte et la direction sud‑est
    - Les PJ ont vu un tracé menant loin au sud‑est sur la carte de la grotte : le désert du [[Synode Mechanis|Synode]].
- Synode Mécanis / Kharza
    - Kharza (ou figure équivalente) s'est montré intéressé par un petit tube métallique (10 cm) : définir qui est Kharza, ses objectifs (armes/tech/marchandage), et si le tube appartient à une technologie précise.
- Grotte aux cristaux
    - Les cristaux sont extraits de la paroi via nacelles/cordages : préparer une Faille/Piège d’extraction, règles de récupération, et le type d’usage (alchimie, énergie pour armes, composant magique).
    - Valeurs/échanges : exemple observé — gros cristal ~125 po ; définir taux d’échange, demandes non-monétaires (objets magiques, matériel d’ingénierie) pour négociations.
- Marchands & contacts
    - Si les PJ reviennent, préparer réactions selon leurs actes (pickpocket, achats, aveux de violence contre le démon) — ex : garde mécanique vigilant, réputation modulable.
- Objets et valeurs d'importance à noter pour la suite
    - Cristal (ex. 125 po aperçu), lingot de fer-froid (valeur réelle 300–400 po), sacoche (contenu à déclarer), collier fragmenté (objet magique possible), maillons de chaîne noire (3–4 maillons).
    - Note explicite : la chaîne ne peut pas être identifiée sur le coup → nécessite Religion/Occultisme/Artisanat pour diagnostic.
