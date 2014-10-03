# Notes livres lus

## Services Web restful, Sam Ruby - Leonard Richardson ed O'Reilly

p154 Démarche de développement

Conceptions et architectures

1. Déterminer le jeu de données
2. Décomposer le jeu de données en ressources

Pour chaque ressources

3. Nommer les ressources par des URI
4. Exposer un sous ensemble de l'interface uniforme
5. Concevoir la ou les représentations accepté par le client
6. Concevoir la ou les représentations fournies par le client
7. Intégrer la ressources dans des ressources existantes en utilisant des liens hypermédias et ou des formulaires
8. Examiner le déroulement typique des évènements. Que doit-il se passer ?
9. Etudier les conditions d'erreurs, que peut il mal se passer ?

Précisions supplémentaires

1. Déterminer le jeu de données
2. Décomposer le jeu de données en ressources
Pour chaque controlleur

a. Ce controlleur expose une ressources ou la frabique ?
b. Expose-t-il en ensemble de ressources objet ?
c. Expose-t-il un formulaire pour créer ou modifier une ressources ?


Faire un diagramme de flux de controle (suggestion du livre)

Existence de ROS.org 

Librairies en C et autres pour tout ce qui est robotique


# Notes discussion avec Yannick

## Différences entre les serveurs ainsi que les objectifs que l'on s'assigne à ceux ci.

1.Serveur d'application

2.Serveur Web

3.Serveur Proxy

4.Serveur Cache


## UDACITY

Le deboggage est important 

Processsus de recherche lent et imprévisible.

Le debuggage coute la moitié du cout d'un logiciel


The devils guide of debugging

Steve McConnel

DO NOT 

1.Scatter output statement everywhere
2.Debug the program into existence
3.Never back up earlier versions
4.Don't try understand what's the program should do
5.Use the most obvious fix

So understand what the program should do and what the problem is and be able to predict future result

Break the cause effect chain)

Methode et modèle scientifique

Observation initiale -> Hypothese -> Prédiction -> Experiment -> Observation ...

Bug like an hyphotesis

input - expected - output

### Explicit debugging 

Mettre dans le commentaires les informations d'hypothèse 

input - expected - output

Format aussi de log - le but est d'éviter de mémoriser

Write things down

Speak to a bear = explicit debugging

Existence dans la STL de la librairie assert.h qui permet de faire des assertions

## Fonctionnement et refining des assertions

1.TESTER L'INPUT
2.PRECONDITIONS
3.POSTCONDITIONS


Concept du TIMEBOMB

Verifier les checkrep - Faire les invariants dans notre code

### RED BLACK TREES

### Tao de la simplification

Get relevant informations

Steve McConnel Code Complete

##Ruby et rails - Le guide ruby des développeurs rails David A Black

1.Décrire et modéliser le domaine de l'application (univers de l'application  ex:Carnet d'adresses - detérmination des modèles)
2.Spécifier ce qui peut se produire au sein du domaine( Ajouter des adresses - Supprimer des adresses... - détermination des actions)
3.Choisir et concevoir les vues du domaine présentées aux utilisateurs(vues du carnet d'adresses)

Modéliser le domaine 

Faire une liste des ensembles, de ce qui le compose
Faire les liens

Cycle de vie d'une application rails

Notion de domaine CGI - Variables CGI à voir et explorer

Helper accès aux autres méthodes par cette syntaxe

```
class MainController < ApplicationController

helper :composer

#Helper de la classe
end

```


