# Plan : cristal de glace

## Plan validé

1. Ajouter `GLACE`, sa rareté, la durée de 4 secondes et le facteur de ralentissement dans `config.js`.
2. Créer le cristal de glace avec une probabilité plus faible que celle du cristal doré.
3. Le dessiner avec une couleur distincte et démarrer le ralentissement quand le joueur l'attrape.
4. Appliquer le facteur aux objets qui tombent pendant 4 secondes, puis reprendre leur vitesse normale.

## Ajustements avant validation

- Retirer l'ajout d'un indicateur dans le HUD : il n'est pas demandé et rendrait le changement plus long.
- Garder rareté, durée et facteur dans `config.js` pour faciliter les réglages.

## Comment vérifier dans le jeu

Augmenter temporairement la rareté de la glace dans `config.js`, lancer une partie et attraper la glace. Vérifier que les objets ralentissent, puis reprennent leur vitesse après 4 secondes. Remettre ensuite la rareté à sa valeur normale.