---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 2
code: S002
date_irl: 2026-02-07
fc-date: 2942-05-08
fc-end: 2942-05-09
resume: "Mini-session : un émissaire de la Main de Platine reçoit les PJ dans son bureau à la Citadelle Blanche pour cadrer leur loyauté et leur discrétion. Les PJ peuvent révéler l'existence des tubes trouvés à l'entrepôt et, s'ils le souhaitent, signer une clause de confidentialité provisoire. Aucun ordre n'est donné : la Ligue déclenche un audit interne et promet un retour ultérieur."
updated: 2026-02-07
termine: true
pjs:
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Théobald Greyheart.md|Théobald Greyheart]]"
aat-render-enabled: true
timelines:
  - session
---

## Informations sur la session

**Date IRL :** `INPUT[datePicker:date_irl]` | **Début IG :** `INPUT[text(placeholder('08/11/42')):date_ig_debut]` | **Fin IG :** `INPUT[text(placeholder('10/11/42 / vide')):date_ig_fin]` | **Terminée ?** `INPUT[toggle:termine]`

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
WHERE type = "session"
  AND numero = this.numero - 1
LIMIT 1
```

---

## TODO

- [ ] (Optionnel) Ajouter les autres PJ présents (ils étaient 4 côté Veyra lors de la découverte des tubes)
- [ ] Préparer un props : **CCP/PL-01** (Clause de Confidentialité Provisoire)
- [ ] Décider si tu fais une **vérification de routine** à la sortie (tension, sans combat)

## Aperçu de la session

- **But apparent :** obtenir une audience (ou au moins une oreille) côté [[Ligue de Veyra]].
- **But réel :** tester la discrétion/discipline des PJ et, s'ils révèlent les tubes, déclencher un **audit interne** (retour non immédiat).
- **Tonalité :** sèche, contractuelle, tendue.

## Demande des PJ
> [!quote]+ Quote
>"Intendant Valerion, permettez-nous de vous dérober un court instant.
>
>Les remerciements officiels du Conseil pour la défense de la ville nous ont honorés, mais nous ne sommes pas venus chercher de nouveaux lauriers. Au contraire, cet événement nous a fait comprendre que nous pouvions — et devions — faire bien plus pour la Ligue de Veyra.
>
>Nous avons de l'ambition, Intendant. Une ambition qui place les intérêts de la Guilde en priorité absolue. Mais l'ambition sans direction ne vaut rien.
>
>C'est pourquoi nous sollicitons une audience privée avec vous. Courtement.
>
>Nous souhaitons vous exposer comment nous comptons faire fructifier notre récent succès pour le bien de la Ligue, et surtout, vous demander comment nous pouvons, dès aujourd'hui, devenir vos atouts les plus fiables. Nous sommes prêts à faire nos preuves, immédiatement."

## Intro

> Dans le tumulte des remerciements et des rapports d'après-assaut, l'Intendant vous a accordé exactement ce que vous aviez demandé : un court instant. Son sourire était impeccable, sa voix douce — et ses yeux, déjà ailleurs.
> 
> *"Votre zèle vous honore."* Il ajuste calmement ses gants. *"Mais Port-Lointain n'est pas gouvernée à l'émotion. Laissez-moi le temps de mesurer votre… fiabilité."*

> Dans la caserne de l'[[Expédition des Fendeurs de Glace]], un messager en tenue civile demande vos noms, vérifie deux fois, puis vous tend une enveloppe scellée. La cire sombre porte une petite empreinte de clef stylisée.
> 
> *"Présence requise. Citadelle Blanche — Galerie des Archives, bureau du Parapheur de Platine. Demain, 9 heure."*
> 
> Aucun autre mot. Aucun "s'il vous plaît". Juste un rendez-vous, et l'impression que quelqu'un, quelque part, a déjà décidé de la valeur de votre temps.


## Scènes

### Scène 1 — La convocation (caserne)
- Les PJ reçoivent un rendez-vous **pour le lendemain à 9h** à la [[Port-Lointain#La Citadelle Blanche|Citadelle Blanche]].

### Scène 2 — Audience : *Le Parapheur de Platine*
> Le hall d'entrée de la Galerie des Archives est bien protégé, des gardes vous font signe de vous présenter au bureau d'accueil. Le reste de bâtiment se trouve de l'autre côté d'une grille fermée. Une fois présenté, on vous indique que le garde du corps du Parapheur de Platine va vous accompagner jusqu'à son bureau. En effet, un minotaure massif aux cornes épaisses et portant des cicatrices sur le museau ouvre la grille de l'autre côté et vous guide à travers les couloirs.
>
>La pierre blanche renvoie le froid de la glace. Dans ces couloirs, les pas résonnent trop fort et les conversations s'arrêtent lorsque vous approchez. 
>
>Le minotaure frappe deux fois à une porte sur laquelle il est inscrit: "Soren Carthain, Parapheur de Platine". Une voix à l'intérieur ordonne d'entrer.

**À jouer :** rappeler que les PJ sont des recrues (statut), et que tout sujet “sensible” a des oreilles.

**Lieu :** Bureau de [[Soren Carthain]] (Citadelle Blanche)

> Le bureau est étroit, rectangulaire, taillé dans la pierre claire et trop propre pour être confortable. La lumière y tombe d'une seule fenêtre haute, froide, découpant des ombres nettes sur un tapis sombre sans motif. L'air sent le papier sec, la cire à cacheter et le cuir entretenu.
>
> Le mobilier est volontairement minimal : une table de travail lourde, des chaises droites aux accoudoirs lisses, et deux armoires basses fermées par de petites serrures identiques. Rien d'inutile, rien de personnel — pas de bibelot, pas de portrait, pas de tasse oubliée.
>
> Sur le bureau, tout est aligné au doigt : un parapheur épais, des feuillets vierges, un sablier fin, un encrier sombre, un sceau métallique et une petite boîte de cire. À portée, un plateau vide prévu pour recevoir "ce que l'on dépose", et à l'opposé, une simple clochette qui n'appelle pas un serviteur — elle annonce que l'entretien est terminé.
>
> Le détail le plus oppressant n'est pas ce qu'on voit, mais ce qu'on comprend : ici, chaque objet existe pour transformer une parole en trace, et chaque trace en levier.

**Présents :** [[Soren Carthain]] (commissaire aux contrats, **Main de Platine**), une scribe, [[Korran Vraxx]] (garde du corps, sous contrat).

>Un tengu d'âge mûr, tenue sombre impeccable. Plumage noir profond aux reflets ternes, bec parfaitement entretenu, regard fixe. Sa main est posée sur un parapheur épais et un stylet sur le bureau.

> *"L'Intendant Valerion n'accorde pas de temps. Il achète de la certitude."*
> 
> *"Trois choses seulement m'intéressent : ce que vous voulez, ce que vous savez, et ce que vous êtes prêts à signer."*

**Structure (3 questions, ton sec) :**
1) *Ambition* — pourquoi vous, pourquoi maintenant ?
2) *Discrétion* — qui sait que vous êtes ici ? à qui avez-vous parlé ?
3) *Utilité* — qu'avez-vous de concret à déposer dans un parapheur ?

#### Branche : les PJ révèlent les tubes
- Carthain ne montre rien, pose des questions factuelles (combien, où, témoins, divulgation).
- Il propose un **cadre**, pas une mission : **CCP/PL-01** (confidentialité provisoire) + dépôt scellé possible.

> *"Ce n'est pas une faveur. C'est un cadre. Vous voulez servir la Ligue ? Commencez par ne pas lui créer un problème."*

**Choix possibles :**
- **Dépôt scellé (Main de Platine)** : les tubes sont mis sous scellés (reçu daté).
- **Conservation par les PJ** : ils signent qu'ils comprennent le risque et s'interdisent toute divulgation.
- **Refus / temporisation** : Carthain note, clôt, et le dossier devient “incertain” (retour plus lent, plus froid).

#### Branche : les PJ ne révèlent rien
- Carthain conclut qu'ils n'ont **rien de monnayable** pour l'instant.
- Il laisse une porte entrouverte : rapport écrit, dépôt ultérieur.

### Scène 3 — Sortie (le délai)
**Jeton scellé** de la Main de Platine (preuve d'entretien ; utile pour franchir certains filtres administratifs Veyra, sans être un laissez-passer). En réalité un moyen de les contacter en cas de besoin.

> Quand vous ressortez, l'air du dehors a un goût de liberté — et de danger. Derrière vous, la pierre blanche ne promet rien. Elle attend.

- Carthain annonce un **audit interne** : recoupements, vérification des registres, contrôle des sous-traitants.
- Il donne un **jeton scellé** (preuve d'entretien, pas un passe-droit) et renvoie les PJ à leurs missions “officielles”.

> *"Nous recoupons. Nous auditons. Nous décidons. Si vous êtes utiles, vous serez contactés. Pas avant."*

## Indices / Pistes

- Les **tubes** (si révélés) deviennent un “actif” qui déclenche un **audit** de la [[Ligue de Veyra]].
- Le vocabulaire de Carthain (*déni plausible*, *garantie*, *risque politique*) suggère un **flux parallèle**.
- L'existence de scellés/clauses renvoie à l'idée que “le contrat fait loi” (style Veyra).
- (Optionnel) Mention indirecte d'une rumeur au sud sans la nommer : les PJ pourront raccrocher plus tard à [[Le Marché Secret]].

## Butin / Récompenses

- **Jeton scellé** de la Main de Platine (preuve d'entretien ; utile pour franchir certains filtres administratifs Veyra, sans être un laissez-passer).
- (Si dépôt) **Reçu daté** des scellés (Main de Platine).

## À reporter / Prépa prochaine

- Faire jouer une session “normale” : laisser le temps à la Ligue de **mener l'audit**.
- Déterminer le délai de retour : **7–14 jours IG** (ou “après la prochaine mission officielle”).
- Décider si la Ligue recontacte les PJ (sessions privées) ou si l'opportunité leur échappe.
