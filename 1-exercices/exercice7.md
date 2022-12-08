# Exercice 7 : mise en place de l'intégration continue

Mettre en place l'intégration continue des éléments suivants : 

Définir les variables suivants :
- PRODUCTION_DOMAIN : `app_frontend.tech`
- DEMO_DOMAIN : `app_frontend.demo`
- DEV_DOMAIN : `app_frontend.dev`
- VERSION : `2.4.3`

Les étapes à définir sont :
- `build`
- `unit_test`
- `quality`
- `package`
- `deploy`

Le build possède 2 `jobs` :
- Le premier se nomme `install`, la commande à exécuté est `npm install --production`
- Le second, se nomme `tsc` dont la commande est `rm -r dist && tsc`
- Le dernier, se nomme `compile` dont la commande est `npm run build`, elle doit être effectuée uniquement en demo.

La commande à exécuter pour le `job` lié aux tests unitaires est `jest --color --coverage`

La commande à exécuter pour le job concernant la qualité est `standard --fix`

La commande à exécuter pour le job de package sur la branche master est `tar -cvzf app_frontend_prod_v${VERSION}.zip --exclude="*/cache" --exclude="*.exe" --exclude="*/node_modules" /`


La commande à exécuter pour le job de package sur la branche demo est `tar -cvzf app_frontend_demo_v${VERSION}.zip --exclude="*/cache" --exclude="*.exe" --exclude="*/node_modules" /`

