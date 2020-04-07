
# Les exercices préparés 

Un exercice préparé est un formulaire permettant de produire un type d'exercice préci.

l'idée est de proposer un fichier de type pp "PrePared" qui fait la liste des balises que l'on doit remplir pour avoir un exercice fonctionnel pour un template donné. Par exemple ici le fichiers proposer devrai "préparer" un exercice qcm. 


la syntaxe pl est utilisé pour exprimer ce fichier:

```pl
# le template de base pour les formulaires d'exercices préparés 
# comme d'habitude avec la syntaxe pl le fichier basic.pp est lu en premier le dictionnaire chargé
# et puis les autres balises sont ajouter dans ce dictionaire 
extends=basic.pp
# balises obligatoire liste str séparé par des virgules 
mandatory=title,text,bad,good
# balise optionnelle 
optional=nb,nbright
# le template à ajouter 
type=/template/qcm.pl 
# le type de chaque balise pour faire du control et 
title={ input_title }
input.title.type=text
input.title.label=Saisissez le titre de votre exercice

text={input_text}
input.text.type=textarea
input.text.label=Saisissez l'énnoncé de votre exercice
bad={ input_bad }
...
nb={ input_nb}
...
```
IL existe des **types** spécifique à pl (non HTML) comme liste de texte, list de numériques etc. 
ou le nombre d'éléments est dynamique


Enfin si l'on veux contraindre un peux plus la saisie il est possible d'ajouter des validateur ou des vérifieurs.


Valideur code javascript qui vérifie dans le navigateur les valeurs saisies.
```pl
# Validator 
input.nb.validator= function f(v){ return v>2 || v==0; }
validator.nb.text= La valeur doit être un entier soit nul soit supérieur à 2. 
validator.title.function= function f(v) { return !(";" in v) ; }
validator.title.text= Pas de ; dans les titres
```


Vérifieurs avec la même syntaxe mais en python sur le serveur
```pl
# verificators 
input.nb.verificator==
def verif(v):
  return v>2 or v==0
==
input.nb.verificatorfeedback= La valeur doit être un entier soit nul soit supérieur à 2. 
input.title.verificator= ...
input.verificator.title.verificatorfeedback= Pas de ; dans les titres
```

il faut que les prémix formulent des validator et des verificators pour les variables sur lesquelles ils sont appliqués.

Le formulaire contient obligatoirement un input nom de fichier qui permet de préciser comment sera sauvegarder.

il est possible de modifier un fichier avec le formulaire dans ce cas la tous les champs sont préremplis avec le contenu du fichier.


Pour finir on peut imaginer que le fichier pp est indiqué dans le template correspondant. 


cela permet en suite que les fichiers "nomdefichier.ext.pl" avec une extension connue "ext" sont interprétés comme des exercices préparés et qu'ils sont ouverts avec le forumalire plustôt que sous forme de fichier text.








