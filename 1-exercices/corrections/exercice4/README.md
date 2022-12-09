# Commandes

## Ajouts des nouveaux fichiers

Depuis votre répertoire de travail en local après avoir effectué des modifications sur les fichiers.

1. `git add hot_dog.md `
2. `git commit -m "feat: hot dog recipe"`
3. `git add jambon_beurre.md `
4. `git commit -m "feat: ham and butter recipe"`

## Commiter

Vous ne pouvez pas commiter sans avoir au préalable ajouté au moins un fichier dans l'index (stage).

1. `git add burger.md `
2. `git commit -m "refactor: update burger recipe"`

#### Etat du dépôt

1. Regardez l’historique de vos commits : `git log`


## Regarder l'historique

1. `git log`
2. `git log --oneline` : commits sur une ligne
3. `git log --graph --pretty=short` : sous forme d'arbre avec les branches et les commits de votre projet