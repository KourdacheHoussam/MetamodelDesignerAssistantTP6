

#### 

 Concevoir un méta-modèle conforme à ECore 
------------------------------------------

Le méta-modèle utilisé ici est le méta-modèle de LDP : langage de description de processus.
Les éléments méta-modèles utilisés dans ce modèle sont :
* EClass pour définir une classe   

* EAttribute pour définir un attribut d'une classe (un attribut est d'un type primitif entier, booléen, chaine...)  

* EReference pour définir une association entre 2 classes   

* EOperation pour définir une opération d'une classe   

* EParameter pour définir un paramètre d'opération   


 
## Un processus 

est une séquence ordonnée d'activités contenant une date de fin et de début.
Le méta-élement processus va nous permettre de définir les élements de nos processus.
Il possède deux PseudoState: etat de début et de fin.


## PseudoState
une classe abstraite, mère de deux sous-classes Start et End.
un pseudoState a toujours une référence vers une Activité.

## Activity

Une activité possède un nom et une référence vers l'activité suivante à condition qu'elle ne soit pas la dernière activité 
du processus



