# TP3- Fullstack

Le but de ce TP était d'apporter des améliorations ainsi que de résoudre des bugs sur un projet existant (projet de l'année passée). **Ce TP a été réalisé par Sébastien GUERRIER et Jordan ELIE**.

Voici les travaux qui étaient à réaliser :

- Mise à jour des frameworks et librairies à la version LTS.
- Résolution d'un bug de gestion des conflits horaires des boutiques.
- Ajout d'une recherche fulltext avec Elastic Search.

## Mise à jour des frameworks et librairies à la version LTS

Deux frameworks (ou librairies) majeurs ont été utilisées au sein de ce projet :

- Spring Boot pour l'API.
- React pour le client.

Les dernières versions LTS de ces technologies sont respectivement les suivantes : 3.2.x, 18.2.x

De manière générale la mise à jour de ces technologies ainsi que l'adaptation des autres dépendances n'a pas été trop pénible, étant donné que du côté de Spring seule l'intégration du Swagger a été à modifier et que la documentation de Spring Boot propose un guide de migration. Ainsi que du côté de React seul un composant (DateTimePicker) de React MUI nécessitait des changements.

## Résolution d'un bug de gestion des conflits horaires des boutiques

La résolution du bug consistait à ajouter de la logique au niveau de la classe `ShopService` lors de la création ainsi que de la mise à jour (qui ne nécessitait pas de changement car celle-ci utilise la création). Deux méthodes privées ont donc été ajoutées :

- **shopHaveOpeningHoursConflict** : Vérifie qu'une boutique ne contient pas de conflit d'horaire.
- **hourHaveConflictWith** : Vérifie que deux horaires d'ouverture n'entrent pas en conflit (utilisée par la méthode shopHaveOpeningHoursConflict).

## Ajout d'une recherche fulltext avec Elastic Search

Par manque de temps mais aussi de compétence sur ce domaine, cette fonctionnalité n'a pas pu être implémentée.
