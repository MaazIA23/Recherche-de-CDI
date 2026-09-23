# Recherche de CDI

Tableau de bord de suivi de ma recherche d'emploi (janvier → septembre 2026) : candidatures, entretiens, refus et prochaines échéances.

- Page : `index.html` (HTML statique, aucune dépendance à installer)
- Données : `data/candidatures.json` (une entrée par candidature)

## Mise à jour

- **Automatique** : chaque soir, une routine lit Gmail et met à jour `data/candidatures.json`. Voir [AUTOMATISATION.md](AUTOMATISATION.md).
- **À la main** : ajouter ou modifier une entrée dans `data/candidatures.json`, par exemple :

```json
{"date": "2026-09-23", "entreprise": "Limagrain", "poste": "AI Transformation Lead", "canal": "SITE", "issue": "", "retour": "", "note": "", "entretiens": 0}
```

`canal` vaut `LI`, `SITE`, `IND`, `DIR` ou `INT`. `issue` vaut `entretien`, `refus`, `attente` ou `sans`. Si `issue` reste vide, elle est calculée automatiquement : « En attente » pendant 3 semaines, puis « Sans réponse ».

## Publication

Netlify : le site est publié depuis `main` (voir `netlify.toml`, aucune étape de build). Chaque push déclenche un redéploiement.

Pour tester en local : `python3 -m http.server`, puis ouvrir http://localhost:8000. La page charge le fichier JSON, elle ne fonctionne donc pas si on l'ouvre directement depuis le disque.
