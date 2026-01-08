<%*
// Template Lore interactif (Templater)
let title = tp.file.title;

// Si la note vient d’être créée avec un nom par défaut, on demande un vrai titre
// (sinon l'id + le H1 restent "Untitled").
const isUntitled = /^(untitled|nouvelle note|new note)( \d+)?$/i.test(title);
if (isUntitled) {
  const wishedTitle = await tp.system.prompt("Titre de la note", "");
  if (wishedTitle && wishedTitle.trim().length) {
    title = wishedTitle.trim();
    await tp.file.rename(title);
  }
}

const slugify = (s) => s
  .normalize("NFD")
  .replace(/[\u0300-\u036f]/g, "") // retire les accents
  .toLowerCase()
  .replace(/[’']/g, " ")
  .replace(/[^a-z0-9]+/g, "-")
  .replace(/-+/g, "-")
  .replace(/^-|-$/g, "");

const id = slugify(title);
const region = await tp.system.prompt("Région", "Tharion");
const faction = await tp.system.prompt("Faction (ou ~)", "~");
const mainTagsRaw = await tp.system.prompt(
  "Tags (séparés par des virgules)\nEx: geographie, cosmologie, mystere",
  "geographie, mystere"
);
const tags = mainTagsRaw
  .split(",")
  .map(t => t.trim())
  .filter(Boolean);

const updated = tp.date.now("YYYY-MM-DD");

tR += `---\n`;
tR += `id: ${id}\n`;
tR += `aliases: []\n`;
tR += `type: lore\n`;
tR += `region: ${region}\n`;
tR += `faction: ${faction}\n`;
tR += `tags:\n`;
for (const t of tags) tR += `  - ${t}\n`;
tR += `updated: ${updated}\n`;
tR += `---\n\n`;
%>
# <% title %>

> *Pitch en 1 phrase (ce que c'est, en quoi c'est important).*  
> *Ex : \"Une barrière de glace permanente séparant Kaerith et Nyssor.\"*

## Description
Décris ce que les PJ peuvent constater (sensoriel, concret, observable).

## Ce que "tout le monde" sait
- 
- 

## Ce qui est vrai (Notes MJ)
> [!gm] Vérité / explication
> - Ce qui se passe réellement.
> - Pourquoi c’est mal compris.
> - Ce que cela implique si les PJ enquêtent.
