---
id: rumeurs-campagne
type: resource
tags: [hexploration, rumeurs, indices, campaign-tools]
updated: 2026-01-08
---
# Liste des Rumeurs

```dataview
TABLE
	arc as "Acte",
	hex as "Hex",
	resume as "Résumé",
	organisations as "Liens",
	choice(revelee, "☑", "☐") as "Révélée?",
	choice(exploree, "☑", "☐") as "Explorée?",
	sessions as "Sessions"
FROM "Rumeurs"
SORT arc, hex, revelee, exploree
```

## Idées

- [ ] 