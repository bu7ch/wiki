## Notes sur NODEJS ##

Node est un technologie qui permet au javascript de s'executer du coté serveur et non plus client.
Nous créons un serveur dans lequel nous pouvons faire nos pages html.
Le code pour créer un serveur minimal nodejs est le suivant.

```
//Chargement de modules a la maniere d'un ruby
var http = require("http");
var url = require("url");
var fs = require("fs");
var event = require("events");
var querystring = require("querystring");
//Creation du serveur et actions associes

var server = http.createServer(function(req,res){

    res.writeHead(200);
    res.write("bonjour");
    res.end();
});
```
server.listen(8808); //Ecoute le port localhost:8808

Nb astuce pour le javascript et sa lecture.
Faire une bonne indentation et regarder le code par les closures sur les plus fréquentes. En l'occurence celle ci : });

Le node est orienté gestion évenements soit 
1. Ecoute du systeme en attente d'un evenement
2. Un évènement se produit
3. Le code agit sur cet évènement



```


```
Manipulation des querystring
```
var http = require('http');
var url = require('url');
var querystring = require('querystring');

var server = http.createServer(function(req, res) {
        var params = querystring.parse(url.parse(req.url).query);
            res.writeHead(200, {"Content-Type": "text/plain"});
                if ('prenom' in params && 'nom' in params) {
                            res.write('Vous vous appelez ' + params['prenom'] + ' ' + params['nom']);
                                }
                                    else {
                                                res.write('Vous devez bien avoir un prénom et un nom, non ?');
                                                    }
                                                        res.end();
});
server.listen(8080);

```

Pour require un fichier sans le chemin absolu et ou relatif => mettre notre module dans le dossier node_modules.
C'est une convention.

Equivalent en ruby du gemspec est le package.json.

```
{
    "name": "mon-app",
        "version": "0.1.0",
            "dependencies": {
                    "markdown": "~0.4"
                        }
                        }
            }
}
```

Routes statiques en nodejs

```
var express = require("express");
var app = express();

app.get('/', function(req, res) {
    res.setHeader('Content-Type', 'text/plain');
        res.end('Vous êtes à l\'accueil, que puis-je pour vous ?');
        });

        app.get('/sous-sol', function(req, res) {
            res.setHeader('Content-Type', 'text/plain');
                res.end('Vous êtes dans la cave à vins, ces bouteilles sont à moi !');
                });

                app.get('/etage/1/chambre', function(req, res) {
                    res.setHeader('Content-Type', 'text/plain');
                        res.end('Hé ho, c\'est privé ici !');
                        });
                })
        })
})
```

Routes dynamiques


```
var express = require("express");
var app = express();

app.get('/etage/:etagenum/chambre', function(req, res) {
    res.setHeader('Content-Type', 'text/plain');
    res.end('Vous êtes à la chambre de l\'étage n°' + req.params.etagenum);
});
```
Possibilite de faire du javascript embedded avec EJS a ranger dans un dossier nommé views
Nb express n'est pas le seul framework node, il en existe d'autre tels que fab.js

CALLBACK PATTERN

```
var fs= require("fs");

function callback(err, results){
	if (err) return handleError(err);
	console.log('File content:', results);
}

var result = fs.readFile('/etc/passwd',callback);
```

Callback last

Callback err 


Node js have specials emitter and listeners called streams


Node Async in order to make or callback simpler

[Node Asyn](http://www.befundoo.com/blog/different-uses-node-async-library/)

Concept d'application MEAN (Mongoose, Express, Angular et Node ) 

Ce sont des applications ultra-reactives qui ne se base que sur le javascript, d'ailleurs un site d'entreprise sur le sujet.

[sCOTCH.io](http://scotch.io/tutorials/javascript/creating-a-single-page-todo-app-with-node-and-angular)

[BrianFord Blog](http://briantford.com/blog/angular-express.html?utm_source=javascriptweekly&utm_medium=email)

D'ailleurs tester MEAN.io pour être au point et voir ce que peut faire Node*.js
