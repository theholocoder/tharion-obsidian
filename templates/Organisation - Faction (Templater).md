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

tR += `---\n\n`;
%>
# <% title %>

> *Pitch en 1 phrase : ce que c’est + pourquoi c’est important pour l’Expédition.*

## Identité
- **Catégorie :** `<% categorie %>`
- **Symbole / couleurs :** 
- **Devise :** 

## Buts & méthodes
- **Objectifs (publics) :**
- **Objectifs (réels) :**
- **Méthodes :**
- **Lignes rouges :**

## Territoire & influence
- **Base / siège :**
- **Zone d’influence :**
- **Ressources clés :**

## Organisation interne
- **Dirigeant(e) :**
- **Figures importantes :**
- **Rangs / titres :**

## Relations
- **Alliés :**
- **Rivaux :**
- **Neutres / opportunistes :**

## Accroches (prêtes à jouer)
- 
- 

## Notes MJ
> [!gm] Secrets, leviers, plans
> - 
