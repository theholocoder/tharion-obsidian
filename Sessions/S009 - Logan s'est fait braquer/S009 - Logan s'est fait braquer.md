---
type: session
campagne: "[[L'Expédition des Fendeurs de Glace]]"
numero: 9
code: S009
date_irl: 2026-04-08
fc-date: 02/05/42
fc-end: 02/05/42
resume: Logan s'est fait braquer ! Quelques jours après être revenu d'aventure dans la forêt, Logan a retrouvé la roulotte de son petit commerce ambulant sans dessus-dessous ! Lui et ses compagnons suivent le voleur qui n'est autre que Aldren Var et finissent par le capturer !
pjs:
  - "[[Campagnes/EFG/PJ/Chiro Kono.md|Chiro Kono]]"
  - "[[Campagnes/EFG/PJ/Fenn Brindebois.md|Fenn Brindebois]]"
  - "[[Campagnes/EFG/PJ/Logan.md|Logan]]"
  - "[[Campagnes/EFG/PJ/Voss Vitriox.md|Voss Vitriox]]"
  - "[[Campagnes/EFG/PJ/Yoko.md|Yoko]]"
updated: 2026-04-08
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

[[Logan]] s'est fait braquer ! Quelques jours après être revenu d'aventure dans la forêt, Logan a retrouvé la roulotte de son petit commerce ambulant sans dessus-dessous !
Vous passiez justement dans le secteur. Aidez le à retrouver le.s coupable.s !

## Scènes

### Braquage

**Scène** : Ecuries
**PNJ** : [[Aldren Var]]

### Poursuite

**Scène** : Poursuite
**PNJ** : Aldren Var

### Combat - Ville

**Scène** : Combat - Ville
**PNJ** : Aldren Var, Aldren Var d'éther

### Combat - Route

**Scène** : Combat - Route
**PNJ** : Aldren Var, Aldren Var d'éther

### Combat - Forêt

**Scène** : Combat - Forêt
**PNJ** : [[Aldren Var]], Aldren Var d'éther, [[Kharza Qalhar]]

## Notes

- **[08/04/2026 09:16:59]** [[Logan]] appelle immédiatement à l'aide ses compagnons proches et se met en chasse du voleur
- **[08/04/2026 09:17:57]** Les PJ passent les 3 obstacles assez vite pour rattraper [[Aldren Var]] à la sortie de la ville
- **[08/04/2026 09:19:31]** Combat expédié rapidement contre les 3 clones. [[Aldren Var]] s'enfuit.
- **[08/04/2026 09:20:29]** Les 3 obstacles suivants sont plus compliqués à passer. Cela laisse le temps à [[Aldren Var]] de tendre une embuscade à un croisement.
- **[08/04/2026 09:23:03]** [[Aldren Var]] tend une embuscade au groupe.
- **[08/04/2026 09:26:13]** Les 3 clones puis Aldren lui même parviennent à mettre [[Logan]], Crunch et [[Yoko]] à terre. Ils sont sauvés par leurs compagnons.
- **[08/04/2026 09:26:28]** Aldren var fuit, gravement blessé.
- **[08/04/2026 09:27:43]** Les 3 derniers obstacles sont plus difficiles que les autres à passer. [[Chiro Kono]] manque de tomber d'un pont plusieurs fois, rattrapé in extremis par [[Logan]]. Ils finissent par les passer en agissant en équipe, mais laissent le temps à Aldren Var de se soigner un peu.
- **[08/04/2026 09:28:25]** Aldren Var, blessé et arrêté pour se soigner, se fait rejoindre par les PJ.
- **[08/04/2026 09:29:09]** Les PJ essaient de l'intimider un peu mais sans succès, ils engagent alors le combat.
- **[08/04/2026 09:29:51]** [[Voss Vitriox]] s'écarte des autres et manque de se faire tuer par les clones. Yoko tombe à terre et est sauvé par Fenn.
- **[08/04/2026 09:30:46]** Un clone est tué avant que Aldren lui-même ne se joigne au combat. Il effectue d'emblée un coup critique sur Logan. Mais il est ensuite rapidement maîtrisé par Logan justement.
- **[08/04/2026 09:31:46]** Les PJ n'obtiennent pas d'informations, ils menottent et attachent Aldren Var et le ramènent à Port-Lointain, dans une geole de la caserne, dans l'espoir que le Conseiller [[Soren Carthain]] obtienne plus d'informations.


## À reporter / Prépa prochaine
- 
