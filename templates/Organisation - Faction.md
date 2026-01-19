<%*
// Template Organisation / Faction (Templater)
// Crée une note dans Lore/Organisations avec frontmatter harmonisé.

let title = tp.file.title;

// 1) Demande le nom + renomme le fichier si besoin
const isUntitled = /^(untitled|nouvelle note|new note)( \d+)?$/i.test(title);
if (isUntitled) {
  const wishedTitle = await tp.system.prompt("Nom de la faction", "");
  if (wishedTitle && wishedTitle.trim().length) {
    title = wishedTitle.trim();
    await tp.file.rename(title);
  }
} else {
  // Même si déjà nommé, on propose de confirmer/ajuster
  const wishedTitle = await tp.system.prompt("Nom de la faction", title);
  if (wishedTitle && wishedTitle.trim().length && wishedTitle.trim() !== title) {
    title = wishedTitle.trim();
    await tp.file.rename(title);
  }
}

// 2) slug -> id
const slugify = (s) => s
  .normalize("NFD")
  .replace(/[\u0300-\u036f]/g, "")
  .toLowerCase()
  .replace(/[’']/g, " ")
  .replace(/[^a-z0-9]+/g, "-")
  .replace(/-+/g, "-")
  .replace(/^-|-$/g, "");

const id = slugify(title);

// 3) Champs
const region = await tp.system.prompt("Région", "Kaerith / Nyssor");

// Catégories proposées (tu peux en ajouter ensuite)
const categories = [
  "faction",
  "guilde-marchande",
  "conseil-dirigeant",
  "ordre",
  "culte",
  "societe-secrete",
  "cartel",
  "compagnie",
  "academie",
  "clan",
  "tribu",
  "milice",
  "bonne-volonte"
];

const categorie = await tp.system.suggester(categories, categories, false, "Catégorie");

// Tags : on pré-remplit avec une base logique
const defaultTags = ["organisation", `categorie/${categorie}`];
const tagsRaw = await tp.system.prompt(
  "Tags (virgules)\nBase conseillée déjà incluse : organisation, categorie/...",
  defaultTags.join(", ")
);
const tags = tagsRaw
  .split(",")
  .map(t => t.trim())
  .filter(Boolean);

const updated = tp.date.now("YYYY-MM-DD");

// 4) Sortie
// NB: pas d'alignement (remaster)

tR += `---\n`;

tR += `id: ${id}\n`;

tR += `type: organisation\n`;

tR += `categorie: ${categorie}\n`;

tR += `region: ${region}\n`;

tR += `faction: ~\n`;

tR += `aliases: []\n`;

tR += `tags:\n`;
for (const t of tags) tR += `  - ${t}\n`;

tR += `updated: ${updated}\n`;
tR += `reputation: 0\n`;

tR += `---\n`;
%>

```meta-bind
INPUT[progressBar(title('Réputation de la Concorde'), minValue(-100), maxValue(100), defaultValue(0), stepSize(1)):reputation]
```

> *« Citation ou rumeur définissant la faction. »*

![[Image.webp|banner]]

## Résumé

![[Image.webp|loc left profile medium]]

| Type de faction   | Cohésion | Méthodes |
| ----------------- | -------- | -------- |
| <% categorie %> | Moyenne  | ...      |
*Description générale de la faction, son apparence et sa "vibe".*

## Buts & méthodes

|                            |                                                                                                  |
| -------------------------- | ------------------------------------------------------------------------------------------------ |
| **Court terme**            | - <br>-                                                                                          |
| **Long terme**             | - <br>-                                                                                          |
| **Tabous / lignes rouges** | -                                                                                                |

## Territoire & influence

```leaflet  
id: <% id %>-map  
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

## Organisation interne

*Description de la structure hiérarchique et du fonctionnement interne.*

| Caste / Rang | Rôle | Description | Particularité |
| ------------ | ---- | ----------- | ------------- |
| **Chef**     | ...  | ...         | ...           |
| **Membre**   | ...  | ...         | ...           |

## Relations
- **Alliés :**
- **Rivaux :**
- **Neutres / opportunistes :**

## Notes MJ
> [!gm] Secrets, leviers, plans
> - 
