# Exercice bonus

**PS : Avec le jargon technique**

## Partie 1

1. Créer un nouveau dossier
2. Initialisez un dépôt git
3. Faites la liaison vers votre dépôt distant Github
4. Créez un fichier *.gitignore* dont le contenu doit exclure le sous-dossier *img*.
5. Faites votre premier commit
6. Renommez le nom de la branche *master* en *main* 
7. Créez et (dé)placez-vous dans une branche nommée *feature/ex-bonus/part1-3*
8. Créez un sous-dossier *img*
9. Ajouter le fichier *.gitkeep* dans *img*.
10. Commitez.

## Partie 2

1. Créez le fichier *README.md* dont le contenu correspond à l’énoncé de cet exercice de la partie 1 à la 3.
2. Faites une capture d’écran de l’état de votre dépôt et enregistrez le fichier dans le sous-dossier *img*.
3. Commitez votre travail en respectant les bonnes pratiques de commit [voir l'annexe partie commits](./../annexe.md).
4. Faites à nouveau une capture d’écran de votre dépôt et enregistrez le fichier dans le sous-dossier *img*.
5. Retirez la ligne contenant *img* dans le *.gitignore*.

## Partie 3

1. Commitez votre travail sans écrire un nouveau message de commit ou en modifiant le message du commit précédent.

## Aide

1. Commitez sans modifier le dernier message de commit : `git commit --amend --no-edit`
2. Commitez en modifiant le dernier message de commit (sans en créer un nouveau) : `git commit --amend`
- Votre éditeur (celui configuré à l'installation) s'ouvre et vous pouvez éditer votre message puis l'enregistrer.

### Cas particulier éditeur VIM

1. Tapez sur la touche *Echap* puis sur la lettre `i` pour passer en mode édition.
2. Modifier votre message de commit
3. Tapez sur le bouton `Echap` pour quitter le mode d'édition.
4. Tapez sur les touches `:x` pour enregistrer les modifications et quitter l'éditeur.

## Partie 4

1. Fusionnez la branche *feature/ex-bonus/part1-3* dans la branche *main*.
2. Créez une nouvelle branche *feature/ex-bonus/part-4* à partir de la branche *main*.
3. Modifiez le fichier *README.md* en ajoutant le contenu de l’énoncé actuel (Partie 4).
4. Commitez votre travail en respectant les bonnes pratiques.
5. Fusionnez la branche *feature/ex-bonus/part4* dans la branche *main*.
6. Envoyez toutes vos modifications (branches *feature/ex-bonus/part1-3*, *feature/ex-bonus/part-4* et *main*) vers votre dépôt distant GitHub.

## Partie 5

Depuis votre compte GitHub, à partir du dépôt où vous avez envoyé précédemment votre travail.
1. Créez une nouvelle branche *feature/ex-bonus/part-5* à partir de la branche *main*.
2. Modifiez le fichier *README.md* en ajoutant le contenu de l’énoncé actuel (Partie 5).
3. Commitez votre travail en respectant les bonnes pratiques.

En local

4. Récupérez les modifications du dépôt distant (aide commande à effectuer `git checkout -b feature/ex-bonus/part-5 --track origin/feature/ex-bonus/part-5`).
5. Fusionnez la branche *feature/ex-bonus/part-5* dans la branche *main*.

### Partie 6

1. Créez une nouvelle branche nommée *feature/ex-bonus/part-6* à partir de la branche *main*.
2. Modifiez le fichier *README.md* en ajoutant l’énoncé actuel (Partie 6)
3. Mettez votre travail de côté (aide commande à effectuer `git stash`)

### Partie 7

1. Créez une nouvelle branche nommée *feature/ex-bonus/part-7* à partir de votre branche *main*.
2. Modifiez le fichier *README.md* en ajoutez l’énoncé actuel (Partie 7).
3. Commitez votre travail en respectant les bonnes pratiques
4. Basculez sur la branche *feature/ex-bonus/part-6*.
5. Récupérez le travail mis de côté (`git stash apply`) et commitez
6. Fusionnez la branche *feature/ex-bonus/part-6* dans votre branche *feature/ex-bonus/part-7*.
7. Résolvez le conflit
8. Fusionnez la branche *feature/ex-bonus/part-7* dans la branche *main*.
9. Ajoutez une version(tag) au dernier commit (`git tag v1.0.0`)
10. Analysez l'état de votre dépôt à l'aide de la commande `git log`
11. Envoyez vers votre dépôt distant GitHub toutes vos branches locales
12. En local, supprimez toutes les branches sauf la branche *main* (pour supprimer une branche `git branch -d branch_to_delete`)

PS : avec l'option `-d`, s'il y a des travaux qui n'ont pas été mergé sur la branche principale, *Git* empêchera la suppression. 
Avec l'option `-D`, la suppression est immédiate peu importe l'état de la branche.