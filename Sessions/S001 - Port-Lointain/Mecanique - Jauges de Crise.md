---
type: mechanic
session: "[[S001 - Port-Lointain]]"
tags:
  - règle-maison
  - foundry
updated: 2026-01-20
---

# Mécanique : Jauges de Crise

Pour cette session, deux barres de progression sont affichées aux joueurs sur FoundryVTT pour représenter l'état de la ville en temps réel.

## 1. Les Jauges

### 📦 Ressources de la Colonie
- **Valeur :** Démarre à **100** (Intact) et descend vers **0** (Ruine).
- **Représente :** L'intégrité matérielle de Port-Lointain (vivres, outils, bâtiments, armes).
- **Conséquence :** Narrative. Détermine l'état de la ville à la fin de la session (Ressources disponibles pour la suite de la campagne).

### 👥 Habitants Capturés
- **Valeur :** Démarre à **0** (Aucun) et monte vers **100** (Population décimée).
- **Représente :** Le nombre de colons enlevés par les Cisarelles.
- **Conséquence :** **Mécanique.** Détermine la difficulté du combat final (voir plus bas).

---

## 2. Évolution des Jauges

Le principe est que les Cisarelles sont des ouvrières : si elles finissent leur tâche, elles rejoignent leur cheffe.

### Le Coût du Temps (Gestion du rythme)
À chaque transition de scène ou repos de 10 min (Soins/Refocalisation) :
- **Ressources :** `-5` (Le pillage continue).
- **Capturés :** `+5` (Les enlèvements continuent).
- *Note : Un repos de 1h coûte `-20` / `+20`.*

### Le Coût des Actions (Résultat des scènes)
- **Scène réussie** (Civils sauvés / Porte fermée) :
  - **Capturés :** `+0` (Hémorragie stoppée localement).
  - **Ressources :** `+0` (Pillage stoppé).
- **Scène échouée** (Civils emportés / Pillage réussi) :
  - **Capturés :** `+10` à `+15` (Un groupe entier est pris).
  - **Ressources :** `-10` à `-15` (Un entrepôt est vidé/brûlé).

---

## 3. Impact sur le Boss Final (La Mutalide)

Le niveau de la jauge **Habitants Capturés** au moment d'entrer dans la **Room 5** détermine les renforts présents.

| % Capturés | État de l'Essaim | Renforts (en plus du Boss) |
| :--- | :--- | :--- |
| **0 - 25%** | **Désorganisé** | Le Boss est quasi seul. Les Cisarelles sont encore occupées en ville.<br>*(Combat Facile)* |
| **26 - 50%** | **Standard** | Quelques ouvrières ont fini et ont rejoint le Boss.<br>*(Combat Moyen - Standard)* |
| **51 - 75%** | **Regroupé** | Le gros de l'essaim a réussi sa récolte et forme un mur défensif.<br>*(Combat Difficile - Ajout d'ennemis)* |
| **76 - 100%** | **Invincible** | La ville est vidée. Toutes les Cisarelles sont sur la place.<br>*(Combat Extrême - Fuite probable)* |
