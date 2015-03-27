Meteor est un framework javascript en devenir a regarder de très près.


Extension meteor pour le debug: meteor Console

[meteor Console](https://github.com/gandev/meteor-server-console)

Possibilité d'user du node inspector pour aider au débuggage.

[Node inspector and debug](http://stackoverflow.com/questions/14909610/how-to-debug-server-side-code-in-a-meteor-app)

Existence de bootswatch pour faire des modifications et themes bootstrap


Meteor Livres

[Meteor livres](https://leanpub.com/meteortutorial)

[Youtube specialiste meteor](http://www.youtube.com/channel/UC4-DIsbr23Z-rPe_F4JAH9w)


Meteor Cheatsheet

[Meteor cheat sheet](http://journal.gentlenode.com/meteor-5-cheatsheet/)


Meteor with Matt Debergalis = screencast youtube a consulter

Meteor Cookbook - Outil pour la cuisine de programme

[Meteor Cookbook](https://github.com/awatson1978)

Meteor tips - Site internet d'un passioné de meteor qui en a même fait un livre

[Meteor tips](http://meteortips.com/book/)

Paquets intéressants pour la conceptions d'applications meteor 

aldeed:collection2  => génération de schema pour bases de données mongo
aldeed:autoform => gestion des formulaires

possibilité de prendre la base de données Mongo en meteor par l'intermédiaire de la commande

```

$ meteor mongo --url

```


meteor reset pour effacer la base de données avant il faut arreter le serveur.

Formation dossier lib/router.js

client/application/layout.html
client/posts/post_index.html

Cheatsheet Geniale sur meteor a consulter

[Meteor Cheatsheet](https://gentlenode.com/journal/meteor-11-iron-router-cheatsheet/18)

Analyse de l'application Téléscope - Prise de note sur ce qui est observé.

L'application a son routeur qui se trouve au niveau de lib - On peut en déduire que dès le lancement de l'applicationle routeur est chargé en premier.
Les dossiers principaux server client public lib et tests sont presents.
On peut noter la présence de fichiers particuliers qui sont de la documentation pour l'utilisation de l'application sous d'autres plateformes.
Point IMPORTANT est le dossier package - Ce dossier comporte de nombreux fichier et dossier. Je suppose qu'il est important pour l'application.

Le dossier collection comporte l'ensemble de la base - de nombreux fichiers.

Point à noter est la présence d'un dossier helpers au sein du client.
Le fichier est client/helpers/handlebars.js
Il s'agit de fonctions crées par le developpeur dans un objectif de faciliter l'affichage de ses données.

Les helpers s'organisent de cette manière

UI.registerHelper('nomHelper', function(){
    //Effectue quelqueChose
});

Il faut noter que UI est remplacé a ce qu'il me semble par Blaze

Nb Blaze est le module qui permet la manipulation des templates au sein de meteor

Utilisation de simpleSchema pour créer des modèles qui vont ensuite servir pour les bases de données.

Utilisation dans le code de checks pour vérifier les valeurs

Après observation des collection, j'ai remarqué qu'il y a possibilité de faire Meteor.isClient au niveau de la déclaration des propriétés de la base

NB retour au niveau de javascript de variables ou de constantes système en Majuscule

Pour ce qui concerne l'internationalisation les paquets i18n il s'agit de l'édition de fichier de traduction au format JSON

Une grande partie de l'application est axée sur les paquets -> Exploration de la création d'un paquet Meteor

Le cas de l'application téléscope est que celle ci est divisée en sous modules  ou packages

Meteor permet la création de packages, sorte de mini applications meteor

Afin de lancer le process de création des packages

```

meteor create  --package nomUser:nomPaquet

```

Utiliser dans le nomUser le nom que vous avez usé sur la plateforme meteor

Le code du paquet s'organise autour d'une description du paquets situé dans package.js et du dossier lib qui concentre l'essentiel du code source du module.

package.js comprend:
Description du paquet
Dépendances Npm
Package.onUser
api.use
api.add_files
api.exports // objet global pour utiliser les fonctions au sein du paquet

Utilisation tableau

Le point important à creuser sera de voir comment faire pour aller mettre l'infrastructure sur un serveur ou autre.

NB Analyse de libreboard et comparaison pour voir les différences:

Différence entre routage client et serveur à creuser


Existence de l'application MeteorKitchen qui permet la création d'application meteor par l'intermédiaire du json

[MeteorKitchen](http://www.meteorkitchen.com/)

Existence du paquet <<b>Mongol</b> qui permet une  meilleure édition de meteor en incluant une fenêtre pour le test de javascript

Meteor paquet pour faire des recherches en base de données => user du paquet easy-search
