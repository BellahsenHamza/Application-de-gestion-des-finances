# Application de gestion des finances

## But du projet
Le but de cette application est de proposer aux utilisateurs une gestion simple, efficace et centralisée de leur finance personnelle pour prendre de meilleures décisions financières. Elle permettra donc de gérer les aspects principaux de la finance personnelle, soit la planification budgétaire ainsi que la gestion des investissements. Cette application a donc plusieurs objectifs pour ses utilisateurs:

* Augmenter le taux d’épargne des utilisateurs de la plateforme
  
    * "En 2018, les Québécois ont épargné 15,6 milliards de dollars. Cela
    représente 6,2% du total de leurs revenus personnels disponibles,
    selon les chiffres de Statistique Canada cités par La Presse."
    
* Fournir des outils de calculs pour prendre de meilleures décisions
    financières
  
    * Cette application permettra aussi aux Québécois et Québécoises
    d'avoir des outils de calculs permettant de prendre des décisions
    financières adaptées à leur situation. Par exemple, une calculatrice
    de taux hypothécaire pour permettre une meilleure planification de
    leur investissement immobilier.
    * Fournir des outils pour suivre le progrès de leurs investissements et
    la répartition de leur portefeuille.
    * Suggérer des achats de titres pour respecter la diversification voulue
    par l’utilisateur.
   
## Technologies requises
* [DataGrip: The Cross-Platform IDE for Databases & SQL by JetBrains (executer les scripts .sql)](https://www.jetbrains.com/datagrip/) 
* [Node.Js 14.8.0 ou supérieur](https://nodejs.org/en/download/)
* [MySQL 8.0.23 ou supérieur](https://dev.mysql.com/downloads/installer/) (MySQLRootPassword : localhost)
  * Choisir Use Legacy Authentication Method pour la méthode d'authentification)
  * Le type de setup à séectionner est le Developer Default

## Démarrage du site
* Exécution des scripts de base de données
  * Exécuter le script script_creation.sql en premier
  * Exécuter le script script_data.sql en deuxième
* Rendez vous à la racine du repértoire git et aller sur le répertoire ./client
* Exécuter ces commandes dans le terminal
```
npm install
npm run serve
```
* Rendez vous dans le repertoire server/
* Exécuter cette commandes dans le terminal
```
node ./bin/www
```
* Pour accéder au site, exécuter la commande suivante
```
npm run serve
```
