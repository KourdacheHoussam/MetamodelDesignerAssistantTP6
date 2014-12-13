

#### 

 Concevoir un m�ta-mod�le conforme � ECore 
------------------------------------------

Le m�ta-mod�le utilis� ici est le m�ta-mod�le de LDP : langage de description de processus.
Les �l�ments m�ta-mod�les utilis�s dans ce mod�le sont :
* EClass pour d�finir une classe   

* EAttribute pour d�finir un attribut d'une classe (un attribut est d'un type primitif entier, bool�en, chaine...)  

* EReference pour d�finir une association entre 2 classes   

* EOperation pour d�finir une op�ration d'une classe   

* EParameter pour d�finir un param�tre d'op�ration   


 
## Un processus 

est une s�quence ordonn�e d'activit�s contenant une date de fin et de d�but.
Le m�ta-�lement processus va nous permettre de d�finir les �lements de nos processus.
Il poss�de deux PseudoState: etat de d�but et de fin.


## PseudoState
une classe abstraite, m�re de deux sous-classes Start et End.
un pseudoState a toujours une r�f�rence vers une Activit�.

## Activity

Une activit� poss�de un nom et une r�f�rence vers l'activit� suivante � condition qu'elle ne soit pas la derni�re activit� 
du processus



