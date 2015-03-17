## RAILS ##
-----
<h1>Modele MVC </h1>

<h1>Rails Conventions</h1>

> Dry - Don't repeat yourself
> Convention over configuration
> Models must be in singular 
> Controller must be in plural

Deux phrases qui résume la philosophie Rails. Rails est un framework de développement d'applications orienté web.<br>
Sites intéressant et références sur rails <br>

[Railscasts.com](http://railscasts.com)

[JumpstartLabs tutoriels](http://tutorials.jumpstartlab.com/)

<h2>Créer une nouvelle application</h2>
```
rails new <nomApplication>
```
Cette commande génere un nouveau dossier  blog dans lequel nous construirons notre application.<br>
Il existe une option -T qui empeche la génération du dossier test de rails. Nb le test par défaut sous rails est effectué par test :: unit.
Ce dossier est composé d'une architecture de dossier qu'il convient de voir.

 - App => contient les fichiers principaux de notre applications. Nous avons ainsi au sein de ce fichier les modèles, controllers. Le gros du travail sera sur ce dossier.
 - views => qui contient tout ce qui concerne l'affichage de notre application
 - bin => Isolation de commandes et invocation de commandes précises par rapport à des conflits de versions.
 - public => qui contient toutes les ressources publiques de notre application
 - Config => qui contient les fichiers de configuration de notre application
 - db => acronyme de database qui contient tout ce qui concerne les bases de données au sein de notre application
 - log => il s'agit du fichier log qui recueille les erreurs au sein de notre application
 - Rakefile => fichier de routage de l'application
 - tmp => dossier temporaire de l'application
 - helpers => petites fonctions qui ne sont pas du domaine l'application.

Nb existence dossier assets = feuilles de styles css, javascript etc...<br>

Possibilité d'avoir des options dans la génération de l'application rails.
```
rails new NomApplication --skip-test-unit #crée l'application sans les test unifaires
rails new NomApplication -f #réecrit sur l'application.
```

<h2>Lancer le serveur </h2>
Si l'ensemble de l'application est en bon fonctionnement et qu'aucune erreur de compilation ou manque de fichier de dépendance ne se déclare alors lancer le serveur rails. 
La commande est la suivante:
```
rails server # Un raccourci est rails s
```
Cette commande est lancée au sein du dossier comprenant notre application.

<h2>Générer un controller</h2>
Pour faire simple le controller est ce qui controlera notre application. Il déterminera le comportement de celle ci.
Pour générer un controller on use:
```
rails generate controller <nomController> <NomPageGestionController> # Possibilité de faire rails g
```
Les controllers sont dans le dossier 
/app/controllers 
Ce sont des fichier de code Ruby.
La gestion des controllers est stocké au sein du dossier /config/routes.rb
Il est possible de décommenter certaines des lignes pour modifications.
Note bien que le mot clé root signifie je suppose la base du site ou de l'application internet.
Index un mot clé pour le "main" d'un site internet.

<h2>Création d'une ressources </h2>

En rails une ressources est une collection d'objets similaires. D'après ce que j'ai compris un ressources est en fait un mot clé qui est en lien avec les bases de données et leur utilisation via le CRUD(Create Read Update Delete).<br>

<h2>Controllers</h2>
Le controlleur est le conteneur de pages web dynamiques ayant des liens entre elles.<br>
```
rails generate controller <Conteneur> <pagesWeb1> <pagesWeb2>
```
La convention ruby exige que les controlleurs soient au pluriel et les modeles au singulier<br>
PagesWeb1 et pagesWeb2 sont les actions qu'effectuera ce controlleur.<br>

Les actions effectués sont aussi des conventions Ruby. index qui affiche la page par défaut.
Création de page web en statique.

<h2>Models</h2>
Les modeles sont la base statiques de notre application, une forme de ressources.
```
rails generate model <nomModele == NomController>
```
Le nom du modele doit être au singulier et le nom du controlleur au pluriel (convention Ruby)


<h2>Echaffaudage</h2>
Existence d'une commande en rails qui "crée" l'échaffaudage de notre application.<br>
```
rails generate scaffold <NomClasse> <attribut1:type> <attribut2:type> 
```
La commande génère un controller, une view, une base de donnée ainsi qu'un modèle.

<h2>Destruction des objets</h2>
La destruction des controllers, modeles et autres s'effectue par l'utilisation de la commande destroy.

```
rails destroy model <nomModele>
rails destroy controller <nomController>
````

Le moyen de voir la liste des controllers et les routes associés est de passer par la commande rake routes.

<h2>Rails console </h2>
Permet de tester le modèle de notre base de donnée, c'est la console rails.

```
rails console # possibilité de faire rails c
rails c --sandbox # aucune valeur est sauvegardé tmp
```
Console irb pour la manipulation de rails. Nous avons ainsi les points suivant par rapport à la base de données qui sont les suivant:

```
post = Post.new #nouvel objet post
post.title ="bonjour le monde" #accès à l'attribut title
post.save #sauvegarde du post dans la base de données
post.destroy #détruit le post
post.all #affiche tous les posts de la base de données
post.update_attribute(:content,"contenu") #mise a jour de la base de donne sur objet post et sur le champ content
post.find(:id) #Affiche le post avec l'id concerné
```
Possibilité de transformer une application rails en plugin, il suffit visiblement de lancer la commande:
```
rails new plugin <nomplugin> #Visiblement transforme en plugin l'app
```

<h2>Link</h2>
Les directions au sein de Ruby sont particulières soit nous avons:<br>

```
action_controllerName_path
```

Dans le cas par exemple de l'édition d'une page, il s'agit de générer le path par l'intermédiaire de l' :id soit 

```
edit_post_path(:id)
```

L'action est la définition présente au sein du controlleur. Ainsi pour faire un nouveau lien vers nous avons toujours la syntaxe : <br>

```
link_to "NomLienClick",action_controllerName_path
```

qui amènera à la view defini par l'action.
Plusieurs voies sont possibles une des plus intéressantes est la suivante:

```
link_to "NomLienClick" controller: "NomController" , action:"ActionController", id: "id"
```

<h2>Création de formulaire sous rails</h2>

Exemple de formulaire

```
<%= form_for @post do |f|  %>
	<p>
		<%= f.label :title %><br>    
		<%= f.text_field :title %><br> 
	</p>
	<p>
		<%= f.label :content %><br>
		<%= f.text_area :content %><br>
	</p>
	<%= f.submit "add a new post" %><br>
<% end %>
```

<h2>RAKE</h2>

La commande rake est en rapport avec le routage dans l'application et ce qui concerne la base de donnée dans l'application.<br>
Soit différentes fonctionnalités:<br>

```
rake test #effectue le test des routes
rake routes #Trace les routes du fichiers
rake db:create #cree une base de données en fonction d'un modèle prédéfinie
rake db:migrate #fait la migration de données
rake db:rollback #vide le cache de la base de données
rake doc:app #genere documentation application
rake assets:precompile #compilation des assets en vue de leur utilisation 
```

Il faut créer une base de données puis la migrer.<br>
Existence de la **gem debugger** pour tout ce qui est du débuggage en rails.<br>
Existence d'une **gem view_mapper** pour l'affichage et gestion des views à partir d'un model et controller.
<h1>Commandes Rails en invite de commande</h1>
Ctrl+Z ou stop = arrêt de l'application
bg = mise en arrière plan de l'application
fg = foreground - mise en avant l'application 

L'idée est de jouer sur ces deux mise en arrière et avant pour faire ses codes et relancer celui ci.<br>
Rails et terminal au même endroit.

<h1>Structure application Rails </h1>

Mode en rails

```
RAILS_ENV=production rails s #passage en mode production
```

Rails Prompt utile
```
Rails.logger.debug("message")
Rails.logger.warn("message")
```

Dans sqlite3 possibilité de faire des requêtes en ligne de commandes de manière directe. 
```
"select * from users"

```

```
remote :true // permet d'effectuer des requetes ajax
```

RakeCors gem qui en ruby gère les problèmes de CORS

RAILS POUR AJAX tutoriel a explorer

[Rails ajax](http://www.codebeerstartups.com/2012/12/ajaxify-your-site-with-remote-true)

Rails pour verifier des infos

raise(params)

Mailman tutorial 

[dansowter](http://dansowter.com/mailman-guide/)

Possibilité d'écrire en rails une notation en tableau pour avoir des données d'une varible d'instance 

Dans views

```
@user[:name]
```

Possibilité de faire passer des champs cachés (formulaire qui possèdent des champs noté bien avant le forms)

```
f.hidden_field :champ => :value => ...

```

En rails possibilité existence de la garberish technique qui permet de charger du code javascript séléctif en prenant en compte des éléments du DOM.

Article intéressant sur le sujet.

[Viget Garberish techinque](http://viget.com/inspire/extending-paul-irishs-comprehensive-dom-ready-execution)


Envoi de mail en rails 

[Handling mail in rails](http://www.gotealeaf.com/blog/handling-emails-in-rails)

Livre ressource sur la création d'application en rails

[API ON rails ](http://apionrails.icalialabs.com/book/chapter_one#cid3)

Existence d'une gem pour la gestion et le filtrage de base de données

[Filterrific](http://filterrific.clearcove.ca/)

Exitence de la gem sabisu pour rails avec une fonctionnalité semblabe a postman
