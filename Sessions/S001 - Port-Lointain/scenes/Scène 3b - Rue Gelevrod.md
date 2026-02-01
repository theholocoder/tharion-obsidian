---
type: scene
parent: "[[S001 - Port-Lointain]]"
tags:
  - scene
  - lieu
---

# Scène 3b - Rue Gelevrod

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

> Une troupe d'insectoïdes de taille humaine a coincé un couple avec un enfant dans la rue. Jet d'initiative.

En fonction de l'avancement/timer, faire jeter `1d3` et l'un des membres de la famille se fait enlever en fonction du résultat.

>[!columns]
>>### 5 joueurs
>> 2 [[Arracheuse Cisarelle]], 2 [[Chasseur Cisarelle]], 1 [[Brute Cisarelle]] (élite)
>
>> ### 6 joueurs
>> 2 [[Arracheuse Cisarelle]], 2 [[Chasseur Cisarelle]], 2 [[Brute Cisarelle]]

## Rumeurs
- Si l'enfant a été kidnappé, [[L'enfant Arraché]]

## PNJ

```pf2e-stats
# Maela Verdan
## Niveau 1
---

==Moyenne== ==Humaine==

Apothicaire de campagne affectée à Port-Lointain, Maela fait partie des premiers civils venus soutenir l’[[Expédition des Fendeurs de Glace]].

**Perception** +5
**Médecine** +8, **Artisanat (Apothicaire)** +7, **Connaissances (Herboristerie)** +6
**Volonté** +6

---
**Historique** Ancienne soigneuse de campagne pour la [[République de Thaldris]], Maela a suivi les convois vers [[Nyssor]] pour offrir ses compétences en premiers secours et en préparation de remèdes. Elle tient un petit cabinet improvisé près de la Rue Gelevrod.
**Apparence** Quarantaine, traits tirés mais regard vif. Tablier taché de sang séché et de teintures, sacoche de cuir pleine de fioles et de bandages. Odeur d’alcool fort et de plantes.
**Personnalité** Calme, pragmatique, protectrice.
**Oral, signe distinctif** Voix douce mais ferme, donne des ordres médicaux courts. Se frotte systématiquement les mains comme si elle les désinfectait, même sans eau ni alcool.

---
**Découverte**  
- **Perception DD 13** : Remarquer qu’elle cache sa propre peur pour rassurer son enfant.  
- **Médecine DD 12** : Noter sa gestuelle professionnelle, celle d’une soignante aguerrie.  
- **Connaissances (Herboristerie ou Médecine) DD 11** : Identifier l’origine militaire de ses techniques (protocoles de triage).

**Compétences d'influence**  
- **Diplomatie DD 15** : Gagner sa confiance en montrant un réel souci pour la vie des civils.  
- **Médecine DD 13** : Discuter de méthodes de soins ou proposer une meilleure approche médicale.  
- **Connaissances (Maladies/Bestioles) DD 14** : Échanger sur les risques biologiques à Nyssor.  
- **Intimidation DD 18** : Tenter de la presser brutalement (fortement déconseillé).

**Influence 4.** Elle accepte de soigner gratuitement les PJ blessés après l’attaque et de leur parler franchement de la situation sanitaire à Port-Lointain.  
**Influence 6.** Elle propose d’analyser tout fragment de mue ou substance inconnue rapporté par les PJ (dont la mue de [[Cisarelles]]), et de leur fournir un rapport écrit utilisable comme avantage lors de futures missions.  
**Influence 8.** Elle devient une alliée fiable : accepte de servir de contact médical régulier, de stocker temporairement des objets ou documents sensibles et de transmettre discrètement des messages aux forces locales.

**Résistances.** Menaces envers Jon (+3 au DD), critiques sur sa compétence médicale (+2 au DD).  
**Faiblesses.** Respect explicite pour son rôle de soignante (-2 au DD), aide concrète apportée à sa famille (-3 au DD).
```

```pf2e-stats
# Tomas Verdan
## Niveau 0
---

==Moyenne== ==Humain==

Charpentier et manutentionnaire, Tomas tente de garder la tête froide alors que sa famille est prise au piège.

**Perception** +4
**Athlétisme** +5, **Artisanat (Construction navale)** +4
**Volonté** +4

---
**Historique** Ancien ouvrier des chantiers navals d’[[Halvorn]], il a suivi Maela par amour plus que par conviction. Il travaille désormais à la réparation des palissades et des toitures de [[Port-Lointain]].
**Apparence** Corpulent, épaules larges, mains calleuses. Porte une chemise rêche, un pantalon de toile épaisse et une ceinture d’outils. Une arme improvisée (maillet de charpentier) ne le quitte jamais.
**Personnalité** Protecteur, méfiant, rancunier.
**Oral, signe distinctif** Parle bas, mâchoire serrée. Garde toujours un œil sur Jon quand il parle à quelqu’un.

---
**Découverte**  
- **Perception DD 12** : Voir qu’il se place instinctivement entre les PJ et sa famille.  
- **Société DD 13** : Deviner son origine halvornienne à son accent et à ses expressions maritimes.  
- **Artisanat (Construction) DD 12** : Reconnaître en lui un ouvrier expérimenté habitué aux structures défensives.

**Compétences d'influence**  
- **Diplomatie DD 16** : Le convaincre que les PJ ne sont pas une menace pour sa famille.  
- **Intimidation DD 17** : Le forcer à coopérer (il obéit mais gardera une dent contre les PJ).  
- **Société DD 14** : Se placer sur le terrain des “petits gens pris entre les décisions du Conseil”.  
- **Athlétisme DD 13 (preuve de force amicale)** : Gagner son respect par une démonstration physique non agressive.

**Influence 4.** Il accepte de témoigner sur ce qu’il a vu dans la rue avant l’arrivée des PJ (mouvements des Cisarelles, direction de retraite).  
**Influence 6.** Il propose d’aider à renforcer ou réparer un point défensif indiqué par les PJ (barricade, porte, ponton), donnant un bonus circonstanciel lors d’un futur siège local.  
**Influence 8.** Il devient un relais fiable dans le quartier : transmet rumeurs, mouvements de troupes, humeurs populaires concernant le [[Conseil de la Brèche]].

**Résistances.** Menaces directes contre Maela ou Jon (+3 au DD), mépris des “civils” (+2 au DD).  
**Faiblesses.** Aide physique offerte à sa famille (soins, transport, protection) (-3 au DD), partage d’alcool fort + discussion franche (-2 au DD).
```

```pf2e-stats
# Jon Verdan
## Niveau 0
---

==Petite== ==Humain==

Jeune garçon curieux ayant grandi trop vite à cause des dangers de Port-Lointain.

**Perception** +5
**Discrétion** +5, **Société** +3
**Volonté** +3

---
**Historique** Fils unique de Maela et Tomas, Jon a suivi ses parents à [[Nyssor]] sans réellement comprendre l’ampleur du changement. Il passe son temps à explorer les ruelles, à écouter les soldats parler et à se fabriquer des jouets avec les chutes de bois de son père.
**Apparence** 9–10 ans, cheveux bruns en bataille, vêtements trop grands raccommodés plusieurs fois. Garde souvent un petit jouet de bois (animal ou soldat) serré dans sa main.
**Personnalité** Curieux, impressionnable, courageux malgré lui.
**Oral, signe distinctif** Parle vite quand il est excité, mais bute sur les mots quand il a peur. Regarde souvent vers les toits et les ombres au-dessus des bâtiments.

---
**Découverte**  
- **Perception DD 11** : Noter qu’il observe tout, même quand il fait semblant de regarder ailleurs.  
- **Psychologie (ou Intuition via Perception) DD 12** : Comprendre qu’il minimise ce qu’il a vu pour ne pas inquiéter ses parents.  
- **Société DD 11** : Deviner qu’il écoute souvent les conversations des soldats et des dockers.

**Compétences d'influence**  
- **Diplomatie DD 13** : Le rassurer et le traiter comme un “grand” pour qu’il s’ouvre.  
- **Duperie DD 14** : Se présenter comme des héros invincibles pour gagner son admiration.  
- **Intimidation DD 18** : Le faire parler par la peur (forte chance de l’endurcir contre les PJ ensuite).  
- **Représentation (Histoires, tours, magie mineure) DD 12** : Le captiver assez pour qu’il parle librement.

**Influence 2.** Jon décrit la scène telle qu’il l’a vue : où étaient les Cisarelles, comment elles ont bougé, qui elles ont pris pour cible en premier.  
**Influence 4.** Il révèle avoir déjà vu “des ombres d’insectes” sur les toits avant l’attaque, et peut indiquer des ruelles ou toits qu’il connaît bien comme chemins rapides.  
**Influence 6.** Il devient un petit éclaireur officieux : promet de prévenir les PJ s’il “revoit des choses bizarres en hauteur”, fournissant un prétexte pour relier plus tard à la rumeur [[L'enfant Arraché]].

**Résistances.** Présence d’armes dégainées (+2 au DD), ton sec ou autoritaire (+2 au DD).  
**Faiblesses.** Promesse de protéger ses parents (-3 au DD), cadeaux simples (jouet, sucrerie, talisman de “protection”) (-2 au DD).
```
