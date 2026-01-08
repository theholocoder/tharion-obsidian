<%*
// Template Événement Calendrier interactif (Templater)
let title = tp.file.title;

// Si la note vient d'être créée avec un nom par défaut, on demande un vrai titre
const isUntitled = /^(untitled|nouvelle note|new note)( \d+)?$/i.test(title);
if (isUntitled) {
  const wishedTitle = await tp.system.prompt("Nom de l'événement", "");
  if (wishedTitle && wishedTitle.trim().length) {
    title = wishedTitle.trim();
    await tp.file.rename(title);
  }
}

const slugify = (s) => s
  .normalize("NFD")
  .replace(/[\u0300-\u036f]/g, "") // retire les accents
  .toLowerCase()
  .replace(/['']/g, " ")
  .replace(/[^a-z0-9]+/g, "-")
  .replace(/-+/g, "-")
  .replace(/^-|-$/g, "");

const id = slugify(title);

// Demande des informations spécifiques aux événements
const dateDebut = await tp.system.prompt("Date de début (YYYY-MM-DD)", "0001-01-01");
const dateFin = await tp.system.prompt("Date de fin (YYYY-MM-DD)", "0001-15-35");
const categorie = await tp.system.suggester(
  ["Historique", "Campagne", "Fêtes"],
  ["Historique", "Campagne", "Fêtes"],
  false,
  "Catégorie de l'événement"
);

const region = await tp.system.prompt("Région", "Tharion");
const faction = await tp.system.prompt("Faction (ou vide)", "");

const mainTagsRaw = await tp.system.prompt(
  "Tags supplémentaires (séparés par des virgules)\nPar défaut: evenement, calendrier",
  ""
);
const customTags = mainTagsRaw
  .split(",")
  .map(t => t.trim())
  .filter(Boolean);

// Tags par défaut + tags personnalisés
const tags = ["evenement", "calendrier", ...customTags];

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
tR += `fc-date: ${dateDebut}\n`;
tR += `fc-end: ${dateFin}\n`;
tR += `fc-category: ${categorie}\n`;
tR += `fc-display-name: ${title}\n`;
tR += `timelines:\n`;
tR += `  - timeline\n`;
tR += `aat-render-enabled: true\n`;
tR += `aat-event-picture: "[[foundry-thumbnail.webp]]"\n`;
tR += `---\n`;
%>
