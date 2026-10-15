# Panier de saison

Petite appli web statique (GitHub Pages) : chaque jeudi, 10 recettes rapides (30 min max) avec des légumes de saison, et une liste de courses.

- `index.html` : l'appli (aucune dépendance, aucun build).
- `data/config.json` : réglages lus par l'appli et par la tâche du jeudi.
  - `sansLaitJusquau` : date (incluse) jusqu'à laquelle les recettes sont sans protéine de lait. Après cette date, retour aux recettes normales.
  - `personnes`, `tempsMax`.
- `data/semaines/<AAAA-Www>.json` : les 10 recettes d'une semaine.
- `data/semaines/index.json` : liste des semaines disponibles.

Chaque jeudi matin, une tâche programmée Claude ajoute le fichier de la semaine, met à jour `index.json`, pousse sur `main` et envoie une notification.

La liste de courses est enregistrée dans le navigateur de chaque appareil.
