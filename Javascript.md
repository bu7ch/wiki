# JAVASCRIPT BASIS

## VARIABLES

### Variables de bases

```
var maVariable = 5;
```

### Types avancés

## FONCTIONS

## STRUCTURE DECISIONNELLES

### if

### case

## BOUCLES

### FOR 

### FOR IN

## CLASSES

### DECLARATION D'UN OBJET

### CREATION D'UN OBJET

### HERITAGE

### METHODES

## METHODES





Cours sur le javascript

http://code.tutsplus.com/articles/17-hours-of-javascript-from-the-masters--net-7615

http://code.tutsplus.com/tutorials/javascript-fundamentals-new-premium-course--net-24631

http://code.tutsplus.com/tutorials/using-createjs-easeljs--net-34840

http://www.jslint.com/

http://boardreader.com/

http://code.tutsplus.com/tutorials/using-createjs-easeljs--net-34840

http://code.tutsplus.com/tutorials/24-javascript-best-practices-for-beginners--net-5399

http://pivotal.github.io/jasmine/

http://www.xul.fr/ecmascript/frameworks.html

http://www.xul.fr/ecmascript/frameworks.html 

http://www.createjs.com/#!/EaselJS

http://melonjs.org/

http://www.lafermeduweb.net/billet/melonjs-un-moteur-de-jeux-2d-melant-javascript-et-html5-1159.html

## SUPERHEROJS - articles sur le javascript

[superherojs](http://superherojs.com/)

[javascript is sexy](http://javascriptissexy.com/how-to-learn-javascript-properly/)

[Learning ressources yauh for javascript](http://yauh.de/best-learning-resources-for-meteorjs/)



Code School javascript
https://github.com/glejeune/Ruby-Graphviz/

Demander metaprogrammation Ruby et Python

NOTES 
Javascript is a misunderstood and unloved langaguage
Javascript include plus and minus of programmation language 
Language of many constrast

From computer scientist to simple people

Don't have the choice in web, javascript is the super
browser programming experience is awful = prob = DOM model
Not fast enough why = DOM search and try to find faster models
Pile of mistakes
	Javascript has good parts
cf java applets


YEOMAN
http://code.tutsplus.com/tutorials/say-yo-to-yeoman--net-27167

java inheritance
SELF 
SCHEME
JAVA 
PERL

CRSF = provient du javascript

Prob = with et eval == probleme
Phony arrays
Arrays = essentiellement hash tables
Probleme = les opérateurs logiques
Utiliser le ===

2 types d'héritages = prototype et class

Javascript

MODULE PARTTERN
```
var simpleton = function(){
  var privateVariable;
  function privateFunction(x) {
	privateVar;
  }
    return {
       firstMethod: function(a,b){
	  privateVariable
       },
       secondMethod: function(c) {
  	   privateFunction
        }
    };
}();
```
ECMASCRIPT = futur du javascript
Mettre le strict mode tag en javascript

Secure 


FUNCTION SCOOPE ARE RULES IN JAVASCRIPT
Implied global


Javascript and the DOM
http://code.tutsplus.com/tutorials/javascript-and-the-dom-series-lesson-1--net-3134

Livre assez intéressant de tim wright sur la programmation

[Learning js ](http://learningjsbook.com/)

Possibilité d'utiliser en Jquery le script $getScript pour charger un script présent sur le serveur, plusieurs solution à l'ancienne était de créer une balise script via le javascript et de l'évaluer. 

Utilisation aussi de callbacks

[Unix papa](http://unixpapa.com/js/dyna.html)

Existence des instruction import et export en javascript pour importer objet et fonctions

[Stack overflow include javascript in other javascript file](http://stackoverflow.com/questions/950087/how-to-include-a-javascript-file-in-another-javascript-file)

JQUERY et utilisateion des requetes ajax 

[Tuts plus requete ajax](http://code.tutsplus.com/tutorials/5-ways-to-make-ajax-calls-with-jquery--net-6289)

Ressource quotidienne sur le javascript

[Daily js](www.dailyjs.com)


Clever solution to map an object// parcourir un objet

```

function solution(pairs){
  return Object.keys(pairs)
    .map(function(k) { return k + ' = ' + pairs[k] })
    .join(',');
}

```

Utilisation du mot clé let pour bien spécifier au javascript de laisser la portée d'une variable à sa fonction. 

### Recettes sur le javascript

Nb existence d'une balise noscript qui dans le temps permettait au navigateur d'executer cette partie si le javascript était désactivé
Gestion des erreurs

Utilisation de try catch et finally pour gestion des erreurs pour erreurs courantes
Initier des erreurs manageables par l'utilisation du mot clé throw

```
if typeof value == "number"
    sum += number
else
    throw "Not a number"
//possibilité de l'envoyer en objet
```

