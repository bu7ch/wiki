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

## Le Zen des CSS, Dave Shea et Molly Holzschlag

Conseils pour l'utilisation des css 
 
1.Utiliser un bon balisage
2.Eviter l'excès de div
3.Limiter le volume de code
4.Exploiter les attributs class et id

Possibilité de mettre un id a un body

Metrre d'abord les id ensuite les classes sachant que les id sont les éléments fixes de notre page.

Attention au jeu de caractères

cf [Alist apart - article sur les carctères spéciaux du web](www.alistapart.com/articles/emen)

Tester sous plusieurs navigateurs => browser Stack


Structure Visuelle

Flexibilité 

Exemple de style css

Exemple basé sur le minimalisme

Idée principale est que le css doit être guidé sur 1 thème et ce "theme" est le design. Suivre tout le long du css cette idée et développer ne conséquence.

Phénomène de fusion des marges en css

Débordement du contenu
Utiliser clear et overflown property

Css est création d'environnements

####Css Processus

#####Fixer des frontières

Mise en place d'un container et body avec les specs du design pricipale

#####Construire des colonnes

Mais aussi des rows composant ces colonnes

#####Créer les illusions d'optiques

Stylisation des éléments - la structure effectuée => travail sur les éléments de style

Exemple de la radio zen garden

Conseils

1.Si vous utilisez des éléments flottants, assurez vous que le dégagement se fait correctement
2.Problème de marge : appliquez un padding ou une bordure pour les éviter
3.Eviter d'appliquer un padding ou des bordures à un élément dont on a spécifié la largeur et la hauteur
4.Ne pas se fier a min-width et min-height
5.En cas de doute diminuez les valeurs en pourcentage
6.Verifier que les effets que vous voulez produire existent réelement
7.Souvenez vous de LoVe/HAte (Link, Visited, Hover, Active -> et LVHFA (Link, Visited, Hover, Focus, Active)
8.Mesures TRouBles - padding et margin ordre dans le sens des aiguilles d'une montre.
9.Spécifiez des unités pour des valeurs non nulles - Le css aime le 0
10.Essayer différentes taille de police
11.Attention différence de casse html css
12.CSS interne pour les test ; CSS externe pour la production
13.Ajouter des bordures visibles pour aider à la correction des problèmes de mise en page.
14.N'utiliser pas les guillements simple autour des chemins d'accès au images
15.Attention au style des liens si on use des ancres

Autres liens et ressources

CSS discuss
[Css discuss mailing list sur le css](www.css-discuss.org)

CSS Max design
[css max design](www.css.maxdesign.com.au)

Andy budd  Références Css
[Andy Budd](www.andybudd.com)

Molly CSS Zeldman - Ressources css
[Molly Css Zeldman](www.dezwozhere.com)

Position is everything
[Position is everything](www.positioniseverything.com)

Magazine veteran designer web css
[A list apart](www.alistapart.com)

Digital Web
[Digital web magazine](www.digital-web.com)

WEB STANDARD BUZZ
[WEB STANDARD BUZZ](www.webstandards.org/buzz)


##Javascript le guide Complet, Olivier Hondermarck

Nb faire des Règles de nommage

Existence de l'opérateur with qui permet accès au propriétés et méthodes d'un objet:

```
with(document){
   write("title =", title, "<br />");
   write("locuste =", locuste, "<br />");
}
```

Tableaux Spéciaux par adressage associatif

```
var tableau = new Array();
tableau['un'] = "Chaine de caractères" ;
tableau['deux'] = 2 ; 

document.write(tableau["deux"] + "<br />");

```

Méthodes tableau
1.concat
2.push
3.pop
4.join
5.reverse
6.shift
7.unshift
8.sort
9.splice

Méthodes String(Regexp avancées)
1.test (Verifier une regexp)
2.exec
3.match (extraire des données)
4.split
5.replace


Popup en javascript autre que alert

```
var winPopup = window.open(txtUrl, txtName, txtOptions);

<a href="javascript:openPopup("popup.html")>Cliquez ici</a>

Nb sur txtOptions
propriete1 = valeur1, propriete2 = valeur2

```

Existence propriété windows.onerror


##Jquery Simplifiez vos développements Javascript, J Chaffer K SwedBerg ed Pearson 

Annexe sur le test en jQuery avec Qunit
Possibilité de faire des tests asynchrones en utilisant deux fonction asyncTest et start

Lecture sur les fermetures en javascript

```
//Fonctions internes algorithmes récursif et Apis

function outerFn(){
  console.log('Fonction externe');
  function innerFn() {
    console.log('Fonction interne')
  }
  innerFn();
};
console.log("OuterFn:\n");
outerFn();

//Appel d'une fonction interne de manière globale

var globalVar ; 

function outerFn(){
  console.log('Fonction externe');
  function innerFn() {
    console.log('Fonction interne')
  }
  globalVar = innerFn;
};
console.log("OuterFn:\n");
globalVar();

//Ecriture par référence "Meilleur pour le ramasse miettes" prise intérieur de innerFn

function outerFn(){
  console.log('Fonction externe');
  function innerFn() {
    console.log('Fonction interne')
  }
  return innerFn;
};
console.log("var fnRef = outerFn():\n");
var fnRef = outerFn();
console.log('fnRef():');
fnRef();
```

Portée des variables

```

function outerFn(){
  console.log('Fonction externe');
  function innerFn() {
    var innerVar = 0;
    innerVar++;
    console.log('InnerVar = ' + innerVar)
  }
  return innerFn;
};
console.log("OuterFn:\n");
var fnRef = outerFn();
fnRef();
fnRef();
var fnRef2 = outerFn();
fnRef2();
fnRef2();
```

Les variables renverons toujours 1
Tandis que dans ce cas on a un compteur

```
var globaVar ;
function outerFn(){
  console.log('Fonction externe');
  function innerFn() {
    globalVar++;
    console.log('globalVar = ' + globalVar)
  }
  return innerFn;
};
console.log("OuterFn:\n");
var fnRef = outerFn();
fnRef();
fnRef();
var fnRef2 = outerFn();
fnRef2();
fnRef2();
```
Nous avons la variable globalVar qui enregistrera les appels de cette fonction et ce qu'importe l'objet

Dans cet exemple nous avons un mélange.

``` 
function outerFn(){
  var outerVar = 0;
  console.log('Fonction externe');
  function innerFn() {
    outerVar++;
    console.log('outerVar = ' + outerVar)
  }
  return innerFn;
};
console.log("OuterFn:\n");
var fnRef = outerFn();
fnRef();
fnRef();
var fnRef2 = outerFn();
fnRef2();
fnRef2();
```
on obtient 1,2 1,2 en résultat - Il y a un scope.

Interactions entre les fermetures

```
function outerFn(){
  var outerVar = 0;
  console.log('Fonction externe');
  function innerFn1() {
    outerVar++;
    console.log('outerVar = ' + outerVar)
  }
  function innerFn2(){
    outerVar += 2;
    console.log('outerVar= ' + outerVar)
  }
  return {'fn1': innerFn1 , 'fn2': innerFn2 };
};
console.log("OuterFn:\n");
var fnRef = outerFn();
fnRef.fn1();
fnRef.fn2();
var fnRef2 = outerFn();
fnRef2.fn1();
fnRef2.fn2();
```

Utilisation de json a but d'affichage

```

$(document).ready(function(){
  $("#letter-b a").click(function(event){
      event.preventDefault();
      $.getJSON('b.json', function(data){
         var html='';
         $.each(data, function(entryIndex, entry) {
           html += 'div class="entry">';
           html += '<h3>'+entry.term+'</h3>';
         });
       $('#dictionnary').html(html);
      });
  });
});

```


Ajout de fonctionnalités à jQuery

```
(function($){
  $.sum = function(){
    var total  = 0;
    $.each(array, function(index, value){ value = $.trim(value) ; value = parseFlaot(value)||0 ; total += value;
    });
    return total;
  };
  $.average =  function(){
     if $.isArray(array)) {
        return $.sum(array) /array.length;
     }
     return '';
  };
})(jQuery);


// Avec l'utilisation d'un espace de nom on opère de la même manière mais en faisant attention a commencer par un objet global.

(function($){
  $.mathUtils = {
    sum: function(array) {
      //fonction jquery sera dans le futur utilisé de cette manière
      // $.mathUtils.sum(array); 
    },
    average: function(average){
       //fonction jquery qui sera utilisée de cette manière
       // $.mathUtils.average(average);
    }
  };
})();

//Methodes ajoutées a l'objet général jQuery

jQuery.fn.maMethode = function(){
   alert('Rien à signaler');
};

//En jquery il existe le mot clé extend pour aussi effectuer ses opération pour agrandir l'espace de nom.
```


##Lecons inaugurales du college de france Gérard Berry, Penser Modéliser et maîtriser le calcul informatique

