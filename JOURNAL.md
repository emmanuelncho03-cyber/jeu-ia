# Journal de bord

Nom et prénom : Yao N'Cho Emmanuel
Dépôt : https://github.com/emmanuelncho03-cyber/jeu-ia
Outil utilisé (Copilot, modèle affiché) : Copilot

Règle : tu colles ici le texte exact de tes prompts (copier-coller, pas de capture). Une entrée par défi. Ce que tu n'as pas gardé compte autant que ce que tu as gardé.

## Défi 1 - Complétion

- Commentaire ou début de code que j'ai écrit :
// compte les cristaux attrapés dans la variable cristaux
//afficher le nombre de cristaux attrapés sur l'écran de fin dans finScore

- Ce que Copilot a proposé : //Pour compte les cristaux, Copilot a proposé - if (objet.type === CRISTAL) {
    cristaux += 1;
  }

- Ce que j'ai accepté, modifié ou refusé, et pourquoi : J'ai accepté la premiere proposition concernant le comptage des cristaux. J'ai refusé la deuxieme proposé et modifié avec finScore.textContent += " | CRISTAUX : " + cristaux;

- Comment j'ai vérifié que ça marche : J'ai testé sur le jeu, il affiche le nombre de cristaux a la fin

## Défi 2 - Ask
- Mes questions (prompts exacts) :


```
Question 1 :Je suis en Bachelor 1, j'ai fait un peu de Go. Explique jeu.js : comment fonctionnent la boucle du jeu, la chute des objets et la détection de l'objet attrapé ? Une phrase par partie.
Question 2: comment le combo est-il remis à zéro ?
```


- Une affirmation de la réponse que j'ai vérifiée : Le combo est remis à zéro lorsque le joueur perd une vie ou lorsque le chronomètre du combo arrive à zéro.


- Comment je l'ai vérifiée (un changement dans le code, un test dans le jeu) : J'ai recherché les instructions chronoCombo-= dt et combo = 0 dans jeu.js. J'ai ensuite ajouté un console.log() dans la condition concernée, lancé le jeu et observé la console du navigateur après avoir rejoué. Le message ne s'est pas affiché.


- Résultat : exacte, fausse ou incomplète : incomplète.
Les instructions existent bien dans le code, mais je n'ai pas réussi à confirmer leur déclenchement réel pendant mon test.


## Défi 3 - Plan


- Mon prompt en mode Plan (texte exact) :


```
Je veux ajouter un cristal de glace, plus rare que le doré. Quand on l'attrape, tous les objets ralentissent pendant 4 secondes, puis reprennent leur vitesse. Respecte les règles de .github/copilot-instructions.md. Propose un plan sans modifier le code.
```


- Le plan est dans le fichier `PLAN.md`.
- Ce que j'ai changé dans le plan avant de le valider (étape retirée, ajoutée, contrainte) et pourquoi : J'ai retiré l'indicateur du HUD car il n'est pas demandé. J'ai ajouté la contrainte de garder les réglages dans `config.js` et une vérification dans le jeu.


## Défi 4 - Agent


- Mon prompt en mode Agent :


```
Applique PLAN.md. Quand tu as fini, relis tes changements fichier par fichier et vérifie le cristal de glace dans le jeu.
```


- Fichiers que l'agent a modifiés : config.js, dessin.js, jeu.js, index.html et .github/copilot-instructions.md.
- Ce que j'ai relu dans les changements avant d'accepter : J'ai vérifié dans le code que le cristal de glace est plus rare que le doré et ralentit tout pendant 4 secondes; que le bouclier est réinitialisé au début et absorbe la première bombe attrapée; et que le bloc du Défi 1 est resté inchangé.
- Ce que j'ai refusé, corrigé ou fait refaire : J'ai ajouté un flash cyan au bouclier, car le texte seul se voyait peu.
- Mon jeu après l'agent (une phrase) : Le cristal de glace ralentit tous les objets et le bouclier absorbe une bombe par partie.


- Deuxième prompt du Défi 4 : le texte exact n’a pas été conservé dans l’historique disponible. Il demandait un bouclier visible dans le HUD qui absorbe la prochaine bombe attrapée, dans le thème néon.


## Défi 5 - Pull request et revue


- Lien de ma pull request : https://github.com/emmanuelncho03-cyber/jeu-ia/pull/1
- Commentaire de la revue Copilot que j'ai traité (le texte) : le cristal de glace était moins rare que le doré; le titre « PLUIE DE NÉON » avait disparu de l'écran d'accueil.
- Ma décision (corrigé ou refusé) et pourquoi : J'ai corrigé la rareté à 0,02 (contre 0,05 pour le doré) et restauré le titre.
- Lien de mon jeu publié : https://emmanuelncho03-cyber.github.io/jeu-ia/


## Bilan (3 lignes maximum)


- Ce que l'assistant a fait mieux ou plus vite que moi : il m'a aidé à ajouter le cristal de glace et le bouclier.
- Ce qu'il a mal fait ou ce que j'ai dû corriger : la rareté du cristal et le titre de l'écran d'accueil.
- Ce que je ne lui laisserais pas faire : modifier mon Défi 1 sans vérifier avec moi.

