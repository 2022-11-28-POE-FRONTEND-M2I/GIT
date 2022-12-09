# Exercice 7 en binôme: mise en place de l'intégration continue

## Partie 1 : rédaction du fichier .gitlab-ci.yml

1. Clonez le dépôt suivant [https://github.com/2022-11-28-POE-FRONTEND-M2I/GITLAB-CI.git](https://github.com/2022-11-28-POE-FRONTEND-M2I/GITLAB-CI.git), une fonctionnalité de vérification des données d'un formulaire à l'aide de JavaScript, JQuery et les REGEX.
2. Modifiez le remote (dépôt distant) par le dépôt GitLab que vous avez crée.
3. Mettre en place l'intégration continue à l'aide de la [documentation de gitlab-ci](https://docs.gitlab.com/ee/ci/yaml/). 

Avant le lancement des `scripts` de chaque job (tâche), le `script` suivant doit être exécuté :

- `echo "start continuous integration"`

A la fin de l'exécution des `scripts`de chaque job, le `script` suivant doit être exécuté :

- `echo "end continuous integration"`

Définir les variables suivantes :
- PRODUCTION : `app_frontend.tech`
- DEV : `app_frontend.dev`
- VERSION : `0.0.1`

Les étapes à définir sont :
- `build`
- `test`
- `quality`
- `package`

L'étape `build` possède 2 `jobs` :
- Le premier se nomme `install:production`, la commande à exécuter est `npm install --production` uniquement sur la branche `main`.
- Le second, se nomme `install:dev` dont la commande à exécuter est `npm install`, il doit s'exécuter uniquement sur les branches qui commencent par le `feature`.

Il y a un `job` pour les tests qui se nomme `unit` dont la commande est `npm run test`. Il doit s'exécuter sur toutes les branches sauf la `main`.

Les commandes à exécuter pour le `job` nommé `qa`, associé à la qualité est :
- `npm run standard-fix`

Le script précédent peut échouer, s'il échoue la tâche doit quand même être considéré comme un succès.

La commande à exécuter pour le job de `package` uniquement sur la branche `main` est `tar -cvzf ${PRODUCTION}_${VERSION}.tar.gz --exclude="${CI_PROJECT_DIR}" --exclude="*/node_modules" --exclude="*/.git" ${CI_PROJECT_DIR}`. Le job se nomme `package:production`.


La commande à exécuter pour le job de package sur les autres branches est est `tar -cvzf ${DEV}_${VERSION}.tar.gz  --exclude="${CI_PROJECT_DIR}" --exclude="*/node_modules" --exclude="*/.git" ${CI_PROJECT_DIR}`. Le job se nomme `package:dev`.

## Partie 2

Une fois que votre fichier `.gitlab-ci.yml` est prêt, effectuez des `pushs` sur les branches `main` et `feature/regex`  pour voir le résultat de l'exécution de vos `pipelines`.

En cas d'erreurs, essayez de les corriger.

## Partie 3

Essayez d'optimiser votre fichier `.gitlab-ci.yml` .