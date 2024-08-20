# CI-CD4AT
CI / CD pour Awahus Tracking


L'objectif de ce projet est de mettre en place une approche CI/CD pour un projet Laravel à déployer sur un serveur CPANEL.

Il s'agit d'un projet laravel avec plusieurs interfaces et acteurs, une base de donnée MySQL.

Je dois donc mettre en place un processus CI/CD pour le projet.

Ceci me permettra de garder un suivi de version, et d'assurer l'intégration continue, et le déploiement continu.
Nous aurons un environnement de test et un environnement de prod.

Je vais utiliser github action pour l'intégration continue et les test, 
et j'utiliserai Jenkins pour le déploiement continue.

Mes pipelines pour le projet seront les suivants :
- Laravel_ci.yaml (Github Actions) => Pipiline d'intégration continue
- Jenkinsfile (Jenkins) => Pipiline de déploiement continu

Ayant deux environnement test et prod, le pipeline ci de l'env test sera sur la branche dev, et celui de l'env prod, sur la branche main.
Mon pipeline CI se termine par un job qui déclenche mon pipeline CD.

Je vais faire usage des secrets pour mes différents mot de passe du serveur.

Je vais ajouter des notifications sur slack à chaque déploiement.
