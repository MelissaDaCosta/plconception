# Suivre une classe


Objectif :  Permet à un enseignant de suivre une de ses classes. 

Résumé général: L'enseignant choisi une classe, le tableau de bord de la classe apparait, il peut modifier le tableau de bord, dans les différents indicateurs il peut choisir d'accéder aux informations d'un élève. Une fois qu'il a lu suffisement d'informations il peut en déduire certaines informations comme les exercices trop difficiles, trop long, les élèves qui ont le plus de difficultés, des actions qu'il doit mener

# Données :

Acteur Principal : Enseignant

Acteurs secondaires : Admin

Concurrence : Oui

Déclencheur : Se déclenche lorsqu'un enseignant clique sur "Suivre une classe".

## Pré-conditions :

### Données d'entrées :

	Classe

Avoir un compte enseignant dans la base de donnée.

Etre relié à un cours.

Avoir au moins une classe qui suit ce cours.


## Post Conditions :

### Données sortie :

	Tableau de bord pour classe

En cas de succès : L'enseignant voit le [tableau de bord](../utilisateur/tableaudebord.md) d'une classe.
Pour chaque élève de la classe, l'enseignant voit les exercices que l'élève a effectué, ce qu'il a fait, raté ou commencé, ainsi que son niveau dans les autres cours de manières très générale. Tout ceci au moyen de couleur.

Vert veut dire réussi.

Orange veut dire commencé mais pas fini.

Rouge veut dire raté.

Blanc veut dire pas encore fait.

En cas d'échec : Si la classe ne suit pas le cours de l'enseignant, dans ce cas l'enseignant voit quand même le [tableau de bord](../utilisateur/tableaudebord.md) de la classe mais de façon non détaillé.

# Navigation / IHM  :

Principe de navigation du scénario principal, organisation de l'IHM.

Dès que l'enseignant clique sur son cours il voit quelles classes le suit.

## Scénarios :

# MAIN SUCCESS SCENARIO

Step    Action

S    L'enseignant voit le descriptif de la classe (L1 français, M1 mathématique etc...).

1    Ce cas d'utilisation commence quand l'enseignant clique sur le descriptif de la classe ou quand on entre l'url de suivie d'une certaine classe dans un navigateur.

2    On affiche le [tableau de bord](../utilisateur/tableaudebord.md) de la classe (pour chaque élève de la classe on voit son "niveau" dans les feuilles d'exercice du cours).

3    L'enseignant peut voir absolument tout ce que l'étudiant à effectué dans les exercices, ce qui lui permet de [suivre l'étudiant](./suivreeleve.md).

4    Ce cas d'utilisation se finit lorsque l'enseignant change de page internet et arrête le suivie.


EXTENSION 

Step    Branching Condition

1	 Si la classe ne suit aucun cours de l'enseignant. Etape 1

na.  Action causing branching:

1 : L'enseignant pourra alors voir une liste des cours que suit la classe.


# RELATED INFORMATION

Concurrency    Plusieurs enseignants peuvent suivre en même temps une classe.

Include Use Cases    [Suivre l'étudiant](./suivreeleve.md) [Tableau de bord](../utilisateur/tableaudebord.md)
 
<!---
Author : Jordan
Validator : Raphael
-->
