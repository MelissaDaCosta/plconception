# Modification/ Affichage profil-reglage

Objectif :  Permettre à un utilisateur d'afficher et/ou de modifier les informations le concernant dans la base de données, ou de réglé ses paramètres application (mode daltonien, mode nuit etc..).

Résumé général : Dans l'entête tout les utilisateurs on un bouton "Profil", qui leurs permettent d'afficher et de modifier les informations de leur compte utilisateurs, il y a les réglages application mode nuit mode daltonien etc... c'est modification sont effectif dès que l'utilisateur choisie de les activés. Et pour les informations profils (Nom, Prénom, mail etc...) L'utilisateur dois valider pour que les modifications soient pris en compte et sauvegardé dans la base de données. 

## Pré-conditions
Déclencheur : se déclenche lors d'un clique bouton sur "profil" ou de l'entré de l'URL dans le navigateur.
 
L'utilisateur a accès à la modification de son profil, il peut donc modifier ou juste voir ses informations et régler ses paramètres applicatifs.

## Champs du profile / préférences
* nom (impossibilité de modification)
* prenom (impossibilité de modification)
* genre (homme/femme) (impossibilité de modification)
* date de naissance (pas obligatoire)
* langue (d'affichage des menus)
* mail (celui du lms)
* mot de passe [ modification dans une view spécial]
* mode daltonien 
* mode nuit (ou thèmes)
* notification oui/non (accepter ou refuser les notifications)
* liste des cercles auquels l'utilisateur appartient








