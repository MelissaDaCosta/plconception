# Créateur

Le créateur produit des exercices, des feuilles, des templates ... réutilisables sur la plate forme.
La distinction du rôle vient de l'action "**n'importe qui peut créer des élements PL**".
Par contre tout élément pl doit subir un **[processus éditorial](../concept/edition.md)** ce processus éditorial validant l'élément et structurant l'intégration de l'exercice dans la base d'exercice PL.


## Fonctionnalités demandées.

Le créateur peut éditer et créer :
* [Un exercice](../concept/exercice.md)
* [Une feuille](../concept/feuille.md)
* [Un grain](../concept/grain.md)
* [Une ressource](../concept/ressource.md)

Il lui faut un tutoriel pour chaque type de création.

Son besoin est d'éditer rapidement et simplement de nouveaux exercices.

Pour chaque type de création (exercice ou feuille ou ...), l'enseignant peut gagner un [badge](../concept/badge.md). Il peut obtenir un badge à partir d'un certain palier.
Par exemple, lorsqu'il a créé 10 exercices, il remporte un badge.
Il en gagne un 2ème lorsqu'il en aura créé 50, puis un 3ème lorsqu'il en aura créé 100.
Il en est de même pour les feuilles, les grains et les ressources ...

Chaque création rapporte de la réputation au créateur.
Il gagne :
* x points pour la création d'un exercice.
* x points pour la création d'une feuille.
* x points pour la création d'un grain.
* x points pour la création d'une ressource.

Il a besoin de validation, de tests, de framework de tests. Il veut des retours sur ses exercices (combien de ses exercices sont utilisés et lesquels).

Il faut un mécanisme (organisation) pour faire passer du code de l'exercice vers le template et du template vers la librairie promotion.


# [Les Cercles](../concept/cercle.md)

Acteur secondaire

Les cercles sont des **communautés** de créateurs et d'utilisateurs où l'on est accepté comme membre par les administrateurs et propriétaires du cercle.
Les critères du cercle variant d'un cercle à l'autre.
Le cercle le plus grand est le cercle créateur piloté par DR. Le cercle le plus exigeant est à ce jour le cercle mythique piloté par DR.

### Données primaires

login, mot de passe

### Données secondaires

Organisation (UPEM, UPMC ...)

### Données générées

* [tag](../concept/tag.md)
* [feuille](../concept/feuille.md)
* [grain](../concept/grain.md)
* [ressource](../concept/ressource.md)

## Cas d'utilisation associées

[créer un exercice](../casutilisation/createur/createexercice.md)

[éditer un exercice](../casutilisation/createur/editerexercice.md)

[éditer une feuille](../casutilisation/createur/editerfeuille.md)

[éditer un grain](../casutilisation/createur/editergrain.md)


<!--- 
Author : Hugo 
Validator : Raphael 
-->

