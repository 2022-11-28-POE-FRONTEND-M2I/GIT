# TP : travail collaboratif avec Git, GitLab et CI

## En équipe

1. Versionnez le TP Banque sur le module `Algorithmie`.
2. Assignez les tâches à chaque développeur en créant des `issues`.
Vous devez avoir au moins 5 branches qu'il faut reconstituer à partir de vos travaux :
- `main` ;
- `feature/create_account` ;
- `feature/withdraw` ;
- `feature/aggios` ;
- `feature/integration`. 

## Individuel

3. Mettre en place l'intégration continue pour chaque branche dédiée.

Vous devez créer les jobs suivants :

- `build`
- `test`
- `QA`
- `package`

Chaque build doit afficher à l'aide de la commande `echo` des variables définies depuis la configuration de votre dépôt.

Par exemple, j'ai une variable que j'ai défini nommée `CI_BUILD`, dans la partie `script`, je dois écrire `echo $CI_BUILD`.

Pour le job `package`, vous pouvez utiliser la commande suivante `tar -cvzf app_bank_v${VERSION}.zip /`.
Le job `package` doit s'exécuter uniquement sur la branche `main`.

4. Faire une demande de `merge request` au propriétaire du dépôt qui aura la responsabilité de `merger` ou non vos travaux. Au moment de la demande, assignez le propriétaire du dépôt et un autre collaborateur pour la partie `Code Review`.

Utilisez la partie commentaire de `GitLab` pour communiquer avec vos collaborateurs.


