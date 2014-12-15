

####Concevoir un m�ta-mod�le conforme � ECore : utilisation du plugin Grimm pour g�n�rer un mod�le conforme au m�ta-mod�le ecore pass� en param�tre.

------------------------------------------------------------



# M�ta-Mod�le d'un r�seau de Petri: 

* EClass pour d�finir une classe   

* EAttribute pour d�finir un attribut d'une classe (un attribut est d'un type primitif entier, bool�en, chaine...)  

* EReference pour d�finir une association entre 2 classes   

* EOperation pour d�finir une op�ration d'une classe   

* EParameter pour d�finir un param�tre d'op�ration   


## D�finition de l'outil (plugin) Grimm:
Outil permettant de g�n�rer des models depuis des m�ta-mod�les conforme Ecore.


###### Exemple d'utilisation : java -jar grimm.jar metamodel.ecore Compo root lb ub rb sys **

- grimm.jar : outil � utiliser pour g�n�rer le model : [t�l�chargment](http://www2.lirmm.fr/~ferdjoukh/english/research.html "t�l�chargment") 
- metamodel.ecore : le m�ta-mod�le pour lequel vous voulez g�n�rer le mod�le.
- Compo : le r�pertoire dans lequel sera stock� le mod�le g�n�r�. _Vous pouvez visualiser l'instance du mod�le g�n�r� en installant GraphViZ, le lien de t�l�achargemet_ [Download](http://www.graphviz.org/Download..php "title") 
- root : la classe racine du m�ta-mod�le mm.
- lb : la borne inf�rieure du nombre d�instances par classe. Ex : 2
- ub : la borne sup�rieure du nombre d�instances par classe. Ex : 2
- rb : la borne sup�rieure du nombre d�instances par r�f�rence.  Ex : 4
- sym : Casser ou non les symm�tries entre les variables des r�f�rences : O ou 1.  Ex: 1


###### Exemple :  java -jar grimm.jar metamodel.ecore Compo 2 2 2 4 1


##### Remarques:

 - Il est imp�ratif d'utiliser le m�me nom de r�pertoire, avec la premi�re lettre en majuscule : Compo
 - Dans le m�ta-mod�le que vous allez cr�er, veillez � rajouter la EClass Compo avec un association de composition vers la racine 
 	de votre mod�le.
 - L'instance du mod�le g�n�r� peut �tre exporter dans differents formats(pdf, png, jpg...etc).
 

## Premier exemple

Dans le r�pertoire model, vous trouverez un fichier .ecore sur lequel vous pourrez faire le premier test:
Le fichier g�n�r� ressemblerai � ceci:

![test](img/test.jpeg "title")  

#M�ta-mod�le 


### Version 1 du M�ta-Mod�le et l'instance du mod�le g�n�r�:
![mm-v1](img/mm-v1.PNG "title")
  


------------------------------------------------------------

![n1](img/m-v1.jpeg "title")


### Version 2 du M�ta-Mod�le et l'instance du mod�le g�n�r�:

Apr�s l'ajout d'une EClass Jeton et la l'agr�gation entre la class "Place" et la class "Jeton".
![mm-v2](img/mm-v2.PNG "title")


------------------------------------------------------------

![n1](img/m-v2.jpeg "title")


### Version 3 du M�ta-Mod�le et l'instance du mod�le g�n�r�:

Apr�s avoir met la class "Transition" en abstract et avoir ajout� les deux classes filles   
TransitionSource et TransitionPuit.
![mm-v2](img/mm-v3.PNG "title")


------------------------------------------------------------

![n1](img/m-v3.jpeg "title")


### Version 4 du M�ta-Mod�le et l'instance du mod�le g�n�r�:

Ajout de la classe Domaine : un r�seau de petri peut �tre appliqu� � plusieurs domaines .
![mm-v2](img/mm-v4.PNG "title")


------------------------------------------------------------

![n1](img/m-v4.jpeg "title")


### Version 5 du M�ta-Mod�le et l'instance du mod�le g�n�r�:

Ajout de la classe Resource et l'association( poids[0..*]) :
Remarque: Dans certain domaine on r�sonne plus en nombre de ressources   

![mm-v5](img/mm-v5.PNG "title")


------------------------------------------------------------

![n1](img/m-v5.jpeg "title")



### Version 6 du M�ta-Mod�le et l'instance du mod�le g�n�r�:

Ajout de  ElementLiaison impl�mentant un Arc du r�seau de Petri;   
Ajout de  ElementNoeud impl�mentant un Noeud qui peut �tre une place ou transition;   
Ajout de AInhibiteur, un arc de type inhibiteur et un arc normal h�ritant de la classe Arc;   
 
Remarque: Dans certain domaine on r�sonne plus en nombre de ressources   

![mm-v6](img/mm-v6.PNG "title")


------------------------------------------------------------

![n1](img/m-v6.jpeg "title")


### Version 7 du M�ta-Mod�le et l'instance du mod�le g�n�r�:
 
Remarque: Dans certain domaine on r�sonne plus en nombre de ressources   

![mm-v7](img/mm-v7.PNG "title")


------------------------------------------------------------

![n1](img/m-v7.jpeg "title")


------------------------------------------------------------


------------------------------------------------------------

 
&copy; 2014 Houssam KOURDACHE