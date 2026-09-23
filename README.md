# Recherche de CDI

Tableau de bord de suivi de ma recherche d'emploi (janvier → septembre 2026) : candidatures, entretiens, refus et prochaines échéances.

- Page : `index.html` (HTML statique, aucune dépendance à installer)
- Données : tableau `A` dans le script en bas de `index.html` (une ligne par candidature)

## Mise à jour

Ajouter ou modifier une ligne dans le tableau `A` :

```js
["AAAA-MM-JJ", "Entreprise", "Poste", "LI|SITE|IND|DIR|INT", "entretien|refus|attente|sans", "date du dernier retour", "note"]
```

Laisser l'issue vide pour qu'elle soit calculée automatiquement (« En attente » pendant 3 semaines, puis « Sans réponse »).

## Publication

GitHub Pages : Settings → Pages → Deploy from a branch → `main` / `(root)`.
