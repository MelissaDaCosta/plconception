# Suivre un élève

Objectif :  Permet à un enseignant de suivre un élève de son cours.

Résumé général: L'enseignant choisit un élève, le tableau de bord de l'élève apparait, il peut modifier le tableau de bord, dans les différents indicateurs il peut choisir d'afficher précisément les informations de l'élève. Ce qui lui permet d'avoir des détails sur un élève en particulier.

# Données :

Acteur Principal : Enseignant

Acteurs secondaires : Admin

Concurrence : Oui

Déclencheur : Se déclenche lorsqu'un enseignant clique sur l'un de ses étudiants.

## Pré-conditions :

### Données d'entrées :

	Avoir un compte enseignant dans la base de donnée.
	
	Etre relié à un cours.

	Avoir des étudiants qui suivent ce cours.


## Post Conditions :

### Données sortie :
	login de l'élève

	Cours dans lequel l'enseignant veux suivre l'élève

	Cours que suit l'étudiant


En cas de succès : L'enseignant voit le [tableau de bord](../utilisateur/tableaudebord.md) de l'élève (les exercices qu'il a effectué, ce qu'il a fait, raté ou commencé), ainsi que son niveau dans les autres cours de manières très générale.

En cas d'échec : L'élève ne suis pas son cours, ou il n'a rien fait, dans ce cas la on signale à l'élève qu'il faut travailler.

# Navigation / IHM  :

Principe de navigation du scénario principal, organisation de l'IHM.

Dès que l'enseignant voit le login ou nom prénom de l'étudiant il peut cliquer dessus et voir tout ce qui concerne l'élève.

## Scénarios :

# MAIN SUCCESS SCENARIO

Step    Action

S	L'enseignant voit le nom d'un étudiant et peut le suivre.

1	Ce cas d'utilisation commence quand l'enseignant clique sur le nom de l'étudiant qu'il veut suivre ou quand on entre l'url de suivie de l'élève dans un navigateur.

2	On affiche le tableau de bord de l'étudiant.

3	L'enseignant peut voir absolument tout ce que l'étudiant à effectué dans les exercices.

4	L'enseignant peut voir en detail ce que l'étudiant a fait dans ses feuilles d'exercices.

5	Il peut lui [donner des indications](../../concept/editeurdechamps.md) afin de l'aider a réussir un exercice en particulier.

6	Ce cas d'utilisation se finit lorsque l'enseignant change de page internet et arrête le suivie.

EXTENSION 

Step    Branching Condition

1	 Si l'étudiant ne suit aucun cours de l'enseignant. Etape 4

na.  Action causing branching:

1 : L'enseignant pourra alors voir son niveau global dans les cours que suit l'étudiant.


# RELATED INFORMATION

Concurrency    Quand plusieurs enseignants suivent en même temps un même étudiant, un seul enseignant à la fois peut donner des indications sur un même exercice.

Include Use Cases    [Editeur](../../concept/editeurdechamps.md) [Tableau de bord](../utilisateur/tableaudebord.md)
 
<!---
Author : Jordan
Validator : Raphael
-->
