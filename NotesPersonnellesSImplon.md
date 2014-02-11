


> Written with [StackEdit](https://stackedit.io/).

Notes personnelles pour le Ruby et le travail à simplon
C’est une reprise de notes personnelles au propres. L’idée est de réfléchir et de voir l’avancement de ce que j’ai appris.
Apprendre, appliquer, corriger et réapprendre.

## RUBY ##
----

 

L’apprentissage du ruby s’est fait par plusieurs ressources

 - [RubyMonk][1]
 - [CodeAcademy][2]


Notes générales sur Ruby points importants.
Tout est objet dans Ruby.
Convention over configuration.

<h1>Variables</h1>

<h2>Différents types de variables </h2>

Les variables en Ruby sont typées dynamiquement, ainsi il ne faut pas préciser leur type avant de les utiliser.
La déclaration de variables s’effectue ainsi.
```
chaineDeCaractere = ”Bonjour le monde”
Nombre = 8
NombreFlottant=8.67
```
Au niveau des variables ce qui est intéressant est le fait que celle ci sont des objets dès leur création.
Il en résulte que plusieurs méthodes peuvent ainsi s’appliquer à celle ci.

<h2>Précisions variables </h2>
Précision des variables par les attributs suivants:
```
precision: 8
scale: 2
```


<h2>Portée des variables</h2>
Il n’y a aucun gros changement nous avons des variables

 - d'instance
 - locales
 - globales
 - constantes

Les locales sont toujours aussi simples
Les globales commencent par un signe $ ainsi:

```
$MA_VARIABLE_GLOBALE # est une variable globale en Ruby
```

Les constantes sont par contre une autre paire de manche sans oublier le fait que dans Ruby, il existe des variables, ou plutôt constantes avec des valeurs prédéfinies. 
Les variables prédéfinies en Ruby permettent le traitement des exceptions et erreurs.

En ce qui concerne Ruby il existe un constant lookup operator trad: Opérateur de résolution de portée qui permet d'accéder au valeurs des variables.

<h1>Fonctions et méthodes</h1>

<h2>Fonctions et méthodes de base </h2>
TOUJOURS PRECISER LA DEFINITION D’UNE FONCTION  AVANT  SON UTILISATION.
Note bien que les termes de méthodes et de fonctions sont synonymes en Ruby.
La définition d’une fonction et ou méthode suit la démarche suivante.

```ruby
def maFonction
	puts “Bonjour le monde”
end
```
def pour define lance la déclaration de la fonction et se termine par un end. D’après ce que j’ai compris à l’heure où j’écris ces lignes  les blocks sont une part importante dans Ruby.

Pour créer ainsi une fonction avec des arguments on effectue ainsi la démarche suivante

```ruby
def maFonction(argument1, argument2)
	return puts “Bonjour le #{argument1}, et le #{argument2}"
```
Point assez remarquable au niveau du Ruby est qu’au niveau des fonctions le return peut ne pas être noté. Ruby fait des retours de fonction implicites. Il en résulte que cette fonction peut être écrite de cette manière.

```ruby
def maFonction(argument1,argument2)
    "Bonjour le #{argument1}, et le #{argument2}"
end
```
Afin d'effectuer des méthodes chaînées on utilise un retour explicite avec l'objet courant. Retour explicite avec le mot clé return et pour l'objet courant on utilise le mot clé "self".

```Ruby
def cook_egg(quantity)
    puts 'I make an egg'
    return self
end

def make_milkshake(flavor)
    puts 'I made some #{flavor} milkshake'
    return self
end
```
Il est maintenant possible de chaîner les méthodes.
```Ruby
objet.cook_egg(6).make_milkshake("chocolat")
```

<h2>Appel de méthodes</h2>

```
def Bonjour
  puts "bonjour le monde"
end

Bonjour() #Cas fonction simple

class Foo
  def Bonjour
    puts "bonjour le monde"
  end
end

a=Foo.new()
a.Bonjour #Cas methode classe

``` 


<h1>Lambda et Proc </h1>

<h2>Blocks</h2>

<h2>Lambda</h2>

<h2>Proc</h2>


<h1>Structures décisionnelles</h1>

<h2>Opérateurs booléens </h2>
OU = ||<br>
ET = &&<br>
NON = !

<h2>If elsif else</h2>
La structure est classique en ce qui concerne if elsif else soit:
```
if (test==true)
    #Instructions
    elsif
    #instructions
    else
    #instructions
end
```
Une autre variante en Ruby est possible pour les strucures if then else en l'occurence il s'agit:
```
x=10 if (test==true)
```
L'instruction est placée avant l'évaluation de la condition.

<h2>until</h2> 

Modèle de strucutre de décision en until
```
hungry = false

unless hungry
  puts "I'm writing Ruby programs!"
else
  puts "Time to eat!"
end
```
Jusqu'à est une structure de décision assez traître, il faudrait faire attention au boucles infinies. 

<h2>case</h2>

<h2>Opérateurs ternaires</h2>


<h1>Boucles</h1>

Boucle simple avec la méthode times
```Ruby
nb_loop = 5
nb_loop.times do 
    puts "la boucle se déroule"
end
#La boucle se déroulera 5 fois
```
Boucle "Objet" avec la mtéhode each

```
a=14
a.each{|x|, #instructions}
```
<h2>Loop Do </h2>
Existence d'une création de boucle avec le mot loop.
```
i = 20
loop do
  i -= 1
  print "#{i}"
  break if i <= 0
end
```

<h2>for</h2>
Exemple possible de boucle for.
```
for num in 1...10
  puts num
end
```
Le point le plus important je trouve est sur la partie "for num in 1...10" il 1...10 une forme de variable est range.<br>
Nb il est intéressant de voir que cette variable est une forme de tableau abrégé. <br>
(1...10) il est exclusif.<br>
(1..10) est inclusif.<br>


<h2>while</h2>
Exemple de boucle while
```
counter = 1
while counter < 11
  puts counter
  counter = counter + 1
end
```
<h2>Until</h2>
Il existe aussi une possibilité de faire une boucle avec until. La syntaxe est la suivante.
```
counter = 1
until counter > 10
  puts counter
  counter=counter+1
  # Add code to update 'counter' here!
  
end
```

<h2>each</h2>

Il existe la méthode each qui avec une variable permet de parcourir le tableau.

```Ruby
var.each do |x|
    puts "#{x}"
end
```

Deuxième version
```
array.each{|x|puts x}
```
Affiche tous les éléments d'un tableau et ou variable. Le each fait le tour de la variable ci dessus est une version raccourcis. Il existe une version avec une forme 

```
array.each do {|x| puts x}end
```

<h2>times</h2>
Execute une varible n fois.
```
3.times{puts "le texte va s'afficher trois fois"}
```

<h1>Types avancées</h1>

Tableaux
Parcourir un tableau

Hash

Symboles

<h1>Modules</h1>

orp(opérateur de résolution de portée)


<h1>Classes et Objets</h1>

<h2>Déclaration de classe</h2>
Exemple de déclaration de classe
```Ruby
class Car
#variable d'instance et de classe
    @name
    @modele
    @annee
#constructeur
    def initialize(name,modele,annee)
        @name=name
        @modele=modele
        @annee=annee
    end
end
```

Instanciation d’objet

<h2>Méthodes</h2>
<h3>Méthodes rencontrés lors de l'exploration Ruby</h3>



Polymorphisme avec super

Getter et Setter

Attribut self

## Gems ##


## SINATRA ##
-------

Utilisation et bases

ActiveRecord

## RAILS ##
-----
<h1>Modele MVC </h1>

<h1>Rails Conventions</h1>

> Dry - Don't repeat yourself<br>
> Convention over configuration

Deux phrases qui résume la philosophie Rails. Rails est un framework de développement d'applications orienté web.<br>
Sites intéressant et références sur rails <br>
[Railscasts.com][3]
[JumpstartLabs tutoriels][4]

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
```Ruby
rails generate scaffold <NomClasse> <attribut1:type> <attribut2:type> 
```
La commande génère un controller, une view, une base de donnée ainsi qu'un modèle.

<h2>Destruction des objets</h2>
La destruction des controllers, modeles et autres s'effectue par l'utilisation de la commande destroy.
```
rails destroy model <nomModele>
rails destroy controller <nomController>
````
Le moyen de voir la liste des controllers et route est de passer par la commande rake routes.

<h2>Rails console </h2>
Permet de tester le modèle de notre base de donnée, c'est la console rails.<br>
```
rails console # possibilité de faire rails c
rails c --sandbox # aucune valeur est sauvegardé tmp
```
Console irb pour la manipulation de rails. Nous avons ainsi les points suivant par rapport à la base de données qui sont les suivant:<br>
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
```
<h1>Add a new post</h1>

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

## RSPEC ##
Rspec permet le test au niveau des applications.<br>
Rspec travaille sur le dossier des tests.
```
bundle exec rspec <FichierTest> -f documentation #affiche de manière plus précise l'erreur
```
Site internet pour l'utilisation de rspec.
[better Rspec][5]

```
RAILS_ENV=production rails s #passage en mode production
```
<h2>Rails infos </h2>

psql -> connection base de données postgresql.
Utiliser rails c pour consulter la base de données.
Dossier initializer contient des configuration qui sont liés à des gems. Tout ce qui concerne les bases de données.


En rails nb existence de plusieurs méthodes pour gérer les routes.

```
render "index" # équivalent en Sinatra de erb :index
```
Nb pour la récupération paramètres usage d'une méthode post_params
```
def post_params()
		params.require(:post).permit(:title , :content)
	end
```

Réutilisation de post_params par :

```

	def create
		@post=Post.create(post_params)
		render "index"
```

Collections : agit sur l'ensemble de la table 
Member : agit sur une ligne de la table.
namespace :  regroupe un ensemble de routes (Thématiser un ensemble de lients ) Il faut faire évoluer le controller. <br>

## REFLEXIONS ##
----------
<h1>Conflits entre les versions et les gems</h1>
Le problème le plus rencontré est le conflit entre les versions.Visiblement quoi qu'on en dise Ruby n'est pas un langage stable. Les gems qui ne sont rien d'autre que des librairies peuvent entrer en conflits d'ou l'utilisation de gem permettant de gérer ces problèmes tels que : 

 - rvm (ruby version manager)
 - bundle 

L'utilisation de rvm pour ma part passe par la console par :
```
/bin/bash --login
```
 pour passer en mode rvm.
 
 NB Existence d'un framework pour le développement d'applications mobiles qui s'appelle PhoneGap => Walid travaille dessus/.<br>

 Tony nous a fait une démonstration de phoneGap. Il existe visiblement PhoneGap aussi en version open source qui le projet Apache Cordova
 
 

Mickael Hartl Tutoriel video
----------
Travail sur Windows = > installer Cygwin
Installer VIm, GIt, curl, ruby 

 
AUTRES LANGAGES
---------------

## C/C++ ##
<h2>Compilation en ligne de commande </h2>
```
g++ nomFichier.cpp -o nomFichier  #lancer la compilation
./nomFichier  #Lancer l'executable.
```

<h2>Faire un makefile</h2>

Le make est un equivalent d'un idle pour c. Il faut noter que c'est un ensemble d'instruction pour la compilation.<br>
[Makefile Creation gazette linux][6]

## Python ##
## Javascript ##
<h1>Markdown</h1>



  
 Tmux = sorte de terminal pour travail.
 
 Reference Rails <br>
 [Rails Tutoriel Officiel][7]<br>
 [Rails Tutoriel Trad Francais][8]<br>



  

  Database.yml = informations de connexions à la base de données.<br>
  Nb Production, test et développement => environnement de développement qui est différent de la production.<br>
  Différents environnement de développement, le point important est la partie de test.<br>
  Utiliser des test = le point impportant. Idée est d'avoir tout de suite avoir un feedback. <br>
  Deux approches<br>
  <ul>
  <li>Faire le test, ensuite coder </li>
  <li>Coder et faire le test après </li>
  </ul>
  Config.ru = point d'entrée dans l'application.<br>
  En développement par défaut on utilise Sqlite <br>
  Gemfiles = manifeste de tous les gem dans l'applications.<br>
  Gemlock = Locke les version pour permettre interopérabilité.<br>
Test = en synonyme avec dossier app.<br>
vendor = code qui vient d'autre sources<br>
  

## Unix Commands ##

Pour effacer en récursivité. <br>
```
rm -rf dossier1/dossier2
```
Commande sur la méthode make qui permet de générer des éxecutables à partir de fichier
```
$ ./configure && make && sudo make install
```
Nb il est intéressant de voir que la commande && enchaine les commande. Ne pas oublier que | enchaine les commandes en prenant le retour de valeur de la précédente commande.

Existence d'un utilitaire htop qui gère mieux en mode gestionnaire de processus/taches.<br>
En gestionnaire de processus commande = "top"<br>
Chacune des actions que l'on effectue sur un processus est en mode ligne de commande et use de lettres. Voir l'aide "h" et "k" pour kill...

```
pg #Utilitaire de shell en mode ligne de commande. Editeur semblable à vim met pour le shell
```
<h2>Grep</h2>
Utilisation de GREP nous avons :
```
ls -a | grep Tu #Affichera les fichiers commencant par Tu
```
<h2>yum</h2>
Possibilité d'utiliser yum pour installation de programme.
```
yum install <nomProgramme>
```

Nb pour des programmes spécifiques. Tout d'abord trouver les ppa de ces fichiers puis ensuite procéder à l'installation de ce ppa par la commande:
```
sudo add apt-get NomduPPa

```

## Vim ##



## Github/Git commands ##

Create a new repository on the command line
```
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/mosleymos/first_app.git
git push -u origin master
```
Push an existing repository from the command line
```
git remote add origin https://github.com/mosleymos/first_app.git
git push -u origin master
```
Afficher les transferts:
```
gitk #affiche l'historique des commit de manière graphique
tig #affiche l'historique des transferts
git gui # gestionnaire graphique de git
```
Création de branche
```
git branch <nomBranche>
```
Création d'une branche et switch rapide.

```
git checkout -b "NomBrancheNouvelle"
```
Effacement 
```
git branch -d nomBranche
```
Historique de l'application

```
git log
```
 

Merge entre deux branches.
```
git merge <nomBrancheAmerger>
```
Existence d'une possibilité de faire un rebase.<br>
Un commit = 1 chose fait dans notre application. Qqche de complet.<br>

stash est une alternative au tout commit , il permet de mettre de côté et permet de ne pas commiter. Le stash est à soi. Ndt stash = "planque"

```
git stash
```

Modification et déplacement de la head a un point précis

```
git checkout -B master SHA1
```
Le reflog indique tous les endroits ou le HEAD a pointé. Les SHA1 sont ainsi tous présents.<br>
Tout se rajoute dans git, rien ne se détruit.
```
git reflog
```
Dépôt distant <br>
Il s'agit d'une connexion au dépôt.

Effacement de modification et remise à zéro.
```
git reset --hard
```

Connexion a à dépôt distant.

```
git remote add origin git@github.com <nom-utilisateur>/first_app.git
```
Suppression d'une branche distante github
```
git push origin :NomBrancheDist_a_Effacer
```
Existence d'un programme git flow qui gère les branches.<br>
C'est un processus particulier mais intéressant.
[TutorielSurGitFlow][9]<br>
[TutorielInteressant sur le gitFlow][10]<br>
[ATLASSIAN GIT Tutoriel][11]

Autres commandes destinées dans git.

```
git diff --cached // Affichage des differences en lignes
```

Indiquer parfois la commande pour le commit exemple
```
git commit -m "$rails g controller welcome"
```




##HEROKU##

<h1>Commandes Heroku</h1>
Même principe que Github, le but est de mettre une web application en ligne.
```
heroku rename // renommage d'une application
heroku create // Création d'une nouvelle application
git push heroku master //mise de l'application en ligne
heroku status // Affiche le statut actuel d'Heroku
heroku logs // Affichage des logs
```
<h2>Sublime tip</h2>
Utilise le Ctrl+p pour effectuer des recherches
faire subl . pour éditer tout un dossier, marche avec vim.
```
subl .
vim .
```

Lorsque l'on travaille en environnement bundle il est recommandé de faire suivre ses commandes de la commande bundle exec afin de résoudre des problèmes de dépendances dans les gem.<br>
Soit nous avons:
```
bundle exec <commandeAeffectuer>
```



Utiliser arandr pour configurer deux écrans et avoir un environnement de travail optimal.

<h2>Insertion de code dans vim par l'intermédiaire de terminator</h2>
taper :<br>
```
:set paste
```
Insert+Ctrl+Shift+v

<h2>Vim tip</h2>
NERDTREE permet de naviguer dans un fichier.<br>
Nous avons CTRL +p  ou n qui sert à l'autocomplétition.<br>
CTRL + X + F = autocomplétition de chemin<br>
[VimCasts][12]

jackDb lecture de base de données en ligneµ.
Tinder application<br>
possibilité de faire des test et exécutions directement sur Sublime

## Utilisation de Tmux ##

Permet de travailler sur plusieurs écrans à partir de sa ligne de commande.<br>
Tmux utilitaire pour faire deux terminal dans un terminal. : <br> plutoôt cool :Yacisne<br>
Existence d'une application linux intéressante Tmate.<br>
<ul>
    <li>Ctrl+b "attendre qqes secondes" + % "split de l'écran horizontalement</li>
    <li>Ctrl+b +"" split horizontal</li>
    <li>Ctrl+b + n ou p = navigation entre plusieurs vues</li>
    <li>Ctrl+b + c = creation d'une nouvelle vue</li>
    <li>Ctrl+b "maintenir enfoncé" et user des touches directionelles pour faire un resize fenêtre.</li>
    <li>Ctrl+b + ? affichage help</li>
    <li>Ctrl+b + spacebar = mise en vertical ou horizontal </br>
    <li>Ctrl+b +q = affichage des numéros de fenêtres.
    <li>Ctrl+r = rechercher dans un terminal </li>
    <li>Ctrl+r +z = resize de la fenêtre en plus grand. </li>
</ul>
[Tmux bases][13]

<h2> Configuration tmux good </h2>
```
# status bar
set-option -g status-utf8 on


# https://github.com/seebi/tmux-colors-solarized/blob/master/tmuxcolors-256.conf
set-option -g status-bg colour235 #base02
set-option -g status-fg colour136 #yellow
set-option -g status-attr default

# default window title colors
set-window-option -g window-status-fg colour244 #base0
set-window-option -g window-status-bg default
#set-window-option -g window-status-attr dim

# active window title colors
set-window-option -g window-status-current-fg colour166 #orange
set-window-option -g window-status-current-bg default
#set-window-option -g window-status-current-attr bright

# pane border
set-option -g pane-border-fg colour235 #base02
set-option -g pane-active-border-fg colour240 #base01

# message text
set-option -g message-bg colour235 #base02
set-option -g message-fg colour166 #orange

# pane number display
set-option -g display-panes-active-colour colour33 #blue
set-option -g display-panes-colour colour166 #orange
# clock
set-window-option -g clock-mode-colour green #green


set -g status-interval 1
set -g status-justify centre # center align window list
set -g status-left-length 20
set -g status-right-length 140
set -g status-left '#[fg=green]#H #[fg=black]• #[fg=green,bright]#(uname -r | cut -c 1-6)#[default]'
set -g status-right '#[fg=green,bg=default,bright]#(tmux-mem-cpu-load 1) #[fg=red,dim,bg=default]#(uptime | cut -f 4-5 -d " " | cut -f 1 -d ",") #[fg=white,bg=default]%a%l:%M:%S %p#[default] #[fg=blue]%Y-%m-%d'

# C-b is not acceptable -- Vim uses it
set-option -g prefix C-a
bind-key C-a last-window

# Start numbering at 1
set -g base-index 1

# Allows for faster key repetition
set -s escape-time 0

# Rather than constraining window size to the maximum size of any client
# connected to the *session*, constrain window size to the maximum size of any
# client connected to *that window*. Much more reasonable.
setw -g aggressive-resize on

# Allows us to use C-a a <command> to send commands to a TMUX session inside
# another TMUX session
bind-key a send-prefix

# Activity monitoring
setw -g monitor-activity on
set -g visual-activity on

# Highlight active window
#set-window-option -g window-status-current-bg red

# Vi copypaste mode
set-window-option -g mode-keys vi
bind-key -t vi-copy 'v' begin-selection
bind-key -t vi-copy 'y' copy-selection

# hjkl pane traversal
bind h select-pane -L
bind j select-pane -D
bind k select-pane -U
bind l select-pane -R

# reload config
bind r source-file ~/.tmux.conf \; display-message "Config reloaded..."

# auto window rename
set-window-option -g automatic-rename

# rm mouse mode fail
set -g mode-mouse on

# color
set -g default-terminal "screen-256color"
```
TMux et travail en plus
[TMux blog interressant][44]


## Workflow Tmux ##

Workflow intéressant avec Tmux est d'organiser son travail à la manière d'une forle d'IDE soit la configuration suivante.<br>

```
----------------------------------
|   VIM                           |
|                                 |
----------------------------------
|   RACKUP        |   GIT/TIG     |
|                 |               |
```


##PROJET##
Faire un proof of concept = meilleur moyen d'exprimer un projet.<br>
Méthodologie Lean <br>
Dans méthodologie Agile on fonctionne par itération. Chaque itération amène vers notre objectif.<br> 
L'idée est de faire des étapes. Chaque itération est un changement d'étapes. <br>

> Build => Measure => Learn 

Build je fais mon proof of concept
Mesurer, avoir le feedback client.
Learn je tire des enseignement ou je pivote.

Itération = non prend trois mois entre 1 semaine et 1 mois. Faire une liste des tâches à faire. <br>
Série d'article sur la création de bon soft.<br>
Idée principale est cathédrale vs bazar.<br>

 - Tout bon morceau de soft commence par gratter la démengeaison de son problème. (Régler vos propres problèmes)
 
 - Les bons programmeurs savent écrire les meilleurs savent réecrire.
 
 - Prévoyez de jetter une version à la poubelle. Ne pas hésiter à repartir de zéro.
 
 - Si vous ne réinventez pas la roue vous pouvez travailler le détails
 
 - Si un truc vous saoule alors passez la main à quelqu'un d'autre.
 
 - Traitez vos utilisateurs comme des co-developpeurs.
 
 - Sortez souvent des trucs et de manière tôt, et voyez comment ça marche 
 
 - Bien traitez vos utilisateurs.
 
 - Se rendre compte que la valeur n'est pas où l'on pensait.
 
 - La perfection est cd qu'on n'enlève pas. Muda 
 
 - Mesure = soutien de la démarche.
 Question est ce que tout à de l'intérêt dans l'application.

- Se mettre à la place de l'utilisateur

- Quelles sont mes priorités ? <br>
 KISS Keep it simple stupid.

 
 site internet - Design sur le site internet.<br> 
 [37signals][14]<br>
 
 Forum comme zone de prospection et zone d'étude clientèle.
 
 Présentation du projet Lavanya.
 
 Cross matching = essayer de voir des points concordants.
 Faire des schémas <br>
 Etre le plus réactif possible<br>
 Balsamiq et wireframing = Faire le plus près possible.
 
 Présentation Roxana<br>
 Remplacer technologie par les gens. Evènement en cours d'organisation.
 Modification et création d'une application de géolocalisation de vol de vélo. L'idée est de faire une solution antivol.<br>
 Vente par rapport au leboncoin. => problème juridique.<br>
 Découverte du projet et travail en lien. <br>
 
 Copycat = refaire qqchose qui se fait à l'étranger


## Atelier SquareSoft ##
 Aujourd'hui est de comment faire son site vous même et rapidement avec un site qui facilite la création de site internet.<br>
 Atelier avec le groupe saphirlabs.<br>
 Squarespace est fait à la base pour les développeur mais peut être utilisé par les non développeurs.<br>
 Squarespace est essentiellement en anglais et très visuel.<br>
 Fonctionne sur la base de templates et fonctionne avec 8$/mois.<br>
 
 Sélection d'une template prédéfinies selon les styles. <br>
 80% réussite d'un site n'est pas technique mais autre. (visuel, navigation ...) Logique, organisation, esthétique et débrouille.<br>
 Principe du texte à trou.<br>
 guerrilla mail = faux compte mail jettale<br>
 
 Creation d'un compte => relié à la création d'un site internet et avoir des adresses différentes soit redirection.

Tutoriel Sublime sur grafikart<br>
pluralize fonction à chercher<br>
Utilisation d'une extension firefox pour développement bsd

Profil de travail est simple.<br>
Wiswig<br>
A chaque fois que l'on souhaite avoir un apercu du site on utilise l'oeil.<br>
A chaque fois que l'on souhaite avoir une édition du site on utilise le crayon (contenu et structure).<br>
A chaque fois que l'on souhaite avoir un dessin du site on utilise le pinceau.<br><br>

Taille de texte ne doit pas varier. Recommendation globale.<br>
Hauteur des lignes a prendre en compte
Je crée quelqueChose, je le vois et je le maquille 


Logiciel partage en ligne de commande : tmate.io<br>

gtroppee@gmail.com Guillaume Troppee Développeur Ruby.

<br>Travail sur le problème postgresql
Ajout username : nomDe Ma machine
password : nom mot de passe

enlever le slash possibilité d'erreur
Extension en postgesql = absente

NB faire nos commentaires dans un README.md

Faire tourner un processus en tache de fond sous linux
```
NomCommande + esperluette

```
rsp


----------
## Open stack ##

Motivation pour open Stack: Combattre Amazon webservices.<br>
Se liberer de cette domination.<br>

Open Stack = 3 ans seulement.<br>

<h2>A quoi ça sert ?</h2>
Outils pour gérer un cloud, externaliser, optimiser usage du cloud.<br>
exemple pratique : Wikimedia foundation.<br>
Idée d'avoir une copie de wikipedia logiciel et contenu.<br>
Open stack est libre.<br>
Cas d'usage de simplon est de tester application, de produire, faire dépôt git.<br>
Actuellement on est sur des machines locales.<br>
Différence entre heroku et openstack. 
Heroku = Paas <br>
Openstack= Iaas<br>
Dans monde openstack existence de Swift qui gère contenu.<br>
Open shift = alternative rails à openstack.<br>
Possibilité d'augmenter ram, processeur ...<br>

Developpement en cours. <br>
Division en 8 grands projet = chaque projet est sur une couche particulières. Tentative de faire avancer les services. Optimisation.<br>
Dans cloud on demarre depuis un disque (virtuel) qui sont les images.<br>
Projet Nova  = occupe du compute
Glance = stocker des images
Neutron = Networking API, se charge 
Cinder = liaison de block d'images. Gestion de disques et de blocks d'avarices.
Swift = gestion des objets et exposition au public.

Existence d'image que l'on peut configurer, existence d'images présente.<br>
Création d'images pour faire modifications.<br>
Tu peux cuisiner ton image et la mettre sur openstack<br>
FreeOs = creation d'un .iso.<br>
3 à 5 ports réseaux physiques.<br>

pourquoi avoir plusieurs cartes réseaux ?
cloud répartis => gérer les flux. <br>

<h2>Gestion des IP.</h2>
Plages ip et privés 172 ... , 10..., 
différentes des ip publiques.
SI que des Ip privées => non accessible depuis le net.
Dans le cloud utilisation de ip flottantes.

Convention Unix sda, sdb pour physiques et vda, vbd pour virtuel
Quota pour la taille des disques.

Proxy
Proxy inverse

Keystone permet modification et travail sur le point et avoir des urls d'accès pour effectuer les modification. Des permissions sont à utiliser.<br>
Keystone = gestion sécurité.<br>

Python est maître sur openstack.<br>
Ubuntu server = permet la gestion d'OpenStack.<br>

Existence de FreeOs (français)<br>

Dernière étape pour participer au projet openstack => procédures. Développement openstack, remontée des bugs, tester...<br>
How to contribute (doc, webmastering, javascript)<br>

Systeme de notes dans OpenStack.
Système des pull requests.

OpenStack simple pour les nuls
http://redmine.the.re/projects/there/wiki/HOWTO_setup_OpenStack

Existence de CEPH.
Systeme redondants.<br>
Système de fichiers, travail d'un daemon = processus. Plusieurs osd. machines isolés les unes à côtés des autres.
Ceph = comment ça s'installe.

```
ceph-deploy new machine A
ceph-deploy mon machine A
ceph-osd #montre osd 
ceph -s #etat du cluster

```
Ceph gestion espace mémoire par redondance.
Existence des poules pour gestion de groupe de gestion. Gestion de datacenters. <br>
Cartes GIgabits et question de la latence. Latence = 1 ms/100 km soit 60% vitesse de la lumière.<br>

Problème de partage<br>
```
rbd
resize #occupation de l'espace supplémentaire dynamiquement
```
Ceph permet d'augmenter la place.<br>
Ceph forme de système de back up.<br>
Rails turnKey = possede une image iso de rails.<br>

Gestion Web semantique sparkle


----------


json <=> XML pour Ruby géré par la gem json. Définition d'unb mode de communication avec le serveur.

Twilio API recrutement. Codeacademy tutoriel

## Protection des données ##
Ammaelle giton cours sur la protection de données sur internet
Web = environnement hostile en ce qui concerne la protection des données de base car il est basé sur le postulat qu'il faut de l'informations pour échange et le fonctionnement d'internet
amaelle.guiton@technOpolis.net
@micro_ouvert
plz ! 0x77775AF9

Ordi possède des infos.<br>

Informations références<br>

Les spyfiles de wikileaks<br> 
Les ennemis d'internet cf Rsf<br>
La quadrature du net <br>

Idées est de comment sont utilisés ses données.<br>
Grandes pratiques<br>
    Sécurité dépend du maillon faible "PEBKAC" Between keyboard and chair. Sert à rien d'utiliser des outils que l'on ne comprend pas.<br>
    Utilisation outils dont on a confiance et en fonction du contexte.<br>
    
Pour protection => utilisation de logiciels libre ctre exemple ? Porte dérobé solutions microsofts. Idée de la boîte noire.<br>
Se méfier du wifi public.

Test de mots de passe. Question de la structure.
Last pass gestionnaire de mots de passe

=> utiliser des mots de passe qui sont plus des phrases de passe.
=> Ne pas utiliser le même mots de passe pour différents services.

Utiliser la Navigation privée.<br>
Utiliser un chiffrement SSL/TLS<br>
KeePass <br>
Plugin HTTPS everywhere<br>

Tor Browser (Réseau anonymisation en forme d'oignon)<br>
Extension firefox<br>

Boite au lettre morte<br>

True Crypt = création de conteneur chiffré.<br>
Logiciel Lux ligne de commande et cryptage.<br>

Cryptocat = extension navigateur<br>

Chat pidgin qui permet de chiffrer conversation et de gérer authentification<br>

Extension otr permet le chiffrement de la conversation.<br>
Utilisation de Vpn<br>

Smartphones = boites noires<br>
    cf the Guardian project.
    
    rspec tutoriel
[Rspecttuts nets nuts][15]

<h4>Instant id projet intéressant</h4>
jeremy.emsellem@gmail.com
Instant id app

Os orienté sécurité (packagé)<br>   
Outils anonymisation = Tails et Liberté Linux

Principe = courrier papier est beaucoup moins surveillé que le courriel.<br>

Meilleur acteur de votre sécurité c'est vous!!!<br>

Histoire Télécomix
Histoire de la cryptographie 
    Militaire First
    Gros bond = commerciale (banque)
    Aujourd = mouvement technicien vers usager.
    
Documentaire la contre histoire de l'internet.

```
link_to "chaine" "lien"
about_path
```

SHift+entree dans chrome = ouverture lien dans nouvelle fenêtre
Navigation internet via w3m logiciel navigation en ligne de commande.

OUTILS POUR LA PROGRAMMATION DE REGULAR EXPRESSION.

[Rubular][16] Site pour le test des expressions régulières.

Recherches personnelles sur utilisation du temps en rails temps réel sans rafraîchir l'écran

[Stackoverflow SOL01][17]<br>
[StackOverflow Sol 02][18]<br>
[Stack overflow sol 03][19]<br>
[SimoneCarlottiBlog][20]<br>

Existence en HTML 5 d'une balise time qui peut faire il me semble du temps réel.
Voir les nouveautés html5.

Existence en Rails d'une classe ActionHelper qui gère l'affichage à la manire d'un actionController ?

<h2>NERDTree Utilisation </h2>
Raccourcis
```
t: Open the selected file in a new tab
i: Open the selected file in a horizontal split window
s: Open the selected file in a vertical split window
I: Toggle hidden files
m: Show the NERD Tree menu
R: Refresh the tree, useful if files change outside of Vim
?: Toggle NERD Tree's quick help
```

## W3M ##

```
v : affichage de la source du site
o : affichage des options
ESC + v  page suivante
CTRL + v page precedente
q  quitter
Ctrl + T nouvel onglet
Alt +t gestion onglet et navigation
CTRL + r rafraichissement de la page
Esc+e = edition de la page courante

```
[w3m manual][21]

### Frabication Html cours assuré par Tony ###
Site internet Utilitaire <br>
[Easel][22]<br> 
Frabication du stylesheet de votre site internet de manière facile.

Recherche a faire sur le scss

Logiciel CSS3 GENERATOR
[cSS3 GENERATOR][23]
ColorZilla<br>
Layerstyle<br>

//Interessant tuerie<br>
http://cdn.ustwo.co.uk/PPP/PPP2.pdf <br>

Point intéressant: 
Faire des screencast depuis son ordinateur avec shelr.tv:<br>
[CLapico blog][24]

[OVERAPI][25] GOOd Site qui tient api css.
[Google-Fonts][26] Fonts google
[IconMOnster][27]IconMaster<br>
[IconDeposit][28] Icon deposit<br>
[Tutoriel sur les media queries][29] Adaptation de Css en fonction de l'écran<br>
[Fontastic][30] Fontastic

[Coffescript translation javascript][31]  web application

Notes informations sur vim<br>
<ul>
<li>[Clapico][32]</li>
<li>[Usevim][33]</li>
</ul>

Nom clé Informatique
<ul>
<li>Bruce schneir</li>
<li>Paul Graham</li>
<li>[Ycombinator-hacker news][34]</li>
</ul>

BLog sur linux 
[danielRosenKreuz][35]
Blog neolao.com post vim


<h3>Notes sur le ruby</h3>
Problèmes sur les pratiques de Ruby 
Site intéressant:
[PraticingRuby][36]

<h3>Outil git </h4>
git instaweb
git flow
Tutoriel git flow [GIt flow tutorial][37]



<h2>Magazine </h2>
Yess = economie solidaire
[Alliancy magazine web techno][38]


site marrant sur linux
[Funix][39]


Point interressant Plugin spf13.vim <br>
[Spf13][40]
Plugin vim qui est un ensemble de plugin.



<h2>Notes personnelles a propos de reflexions </h2>
Existence des vimcasts<br>
Existences des ascii cast<br>
Ruby quicktips<br>
Blog interessant sur les workflow<br>
[Coderwall][41]
[Ruby rogues][42]
Creuser plus d'informations sur ruby rogues<br>
Article pour augmenter sa productivité en vim<br>
Existence de vimux, sorte de vim + tmux implementé pour le développement - A regarder de plus près<br>
[VImux TreeBrain][43]



<h2>Installation Ruby sur ubuntu </h2>
[Stackoverflow - work][45]
COuiile ruby
[UbuntuFOrum and ask][46]

<h2>Installation de nodejs</h2>
[OpenClassrooms][47]

<h2>Nouvelle collections de gem orientés sur la ligne de commande</h2>

Site internet les répertoriant.
[Blog sur un livre sur la ligne de commande][48]
Gem Commander qui a l'air géniale<br>
Gem Main pour la gestion de la ligne de commande.<br>
Existence de la gem Hightline qui permet le travail en ligne de commande mais aussi d'autre gems telles que le sujet abordé sur stackoverflow<br>
[Stack overflowDiscussion][49]
Existence de la gem 'RubyInline' qui permet d'introduire du code de d'autre langages en ruby<br>

RUby Highline et une autre librairie Junos qui est a tester.<br>
[Junos and a blog][50]
[Ruby-forum][51]
Existence de tmuxinator config déjà prêtes à l'emploi.<br>
gem terminator-table qui permet de génerer des tables en asci

---BASTARD RUBY BOOK ---

A ESSAYER DE TOUTE URGENCE

[BastardRubybOOK][52]

Tutoriel sur le timeout
[Docunext][53]

TUtoriel sur les gemsset
[TUto d'un blog cool][54]
Tutoriel officiel de création de gem
[Officiel Creation GEM][55]

SIte internet sur l'apprendissage de RUby a voir peut être
[Ruby learning][56]

<h1>SPFVIM13</h1>
Spf13 vim est une installation de vim plugin orienté développement déjà toute prête.<br>
[Site officiel Spfvim13][57]
[Site officiel et blog][58]



<h1>JAVASCRIPT</h1>
Les caractères d'echappement pour les guillements sont:
```
string =" Oh my \"delicious "\ darling
```
Méthodes de conversion de types
```
myNumber=parseInt(3.114156)
myNumber=parseFloat(3.1415)
```

Informations sur test Unit a tester
[WhatdoItest][59]
[TestUnitBlog][60]

Interresting rails article to test.
[AndreaPavomani][61]

Wishlist pour les freebies
[Blogs and site ressoureces wish lists][62]

<h1>TODOMVC</h1>
[TODOMVC][63]

mjvc ensemble
[Javascriptmvc][64]


Tutoriel sur javascript
[Angular - tutoriel Graphikart][65]
[Yeoman][66] //outil oiyr travailler en javascript
[LearnToappend -Cours javascript][67]
[Alsacreation-Cours javascript][68]

Organiser code javascript en modules
[Alsacreation modularisation][69]

<h2>Lien interessant</h2>
Enregistrer son code et faire un walktrough<br>
[CodePlayer][70]

Bit Torrent Sync installation <br>
[La vache libre tutoriel Bit Torrent sync][71]
[Ubuntu Forum][72]

Blog interressant sur la creation de Codeplayer et du worflow en cours.<br>
[Tuicool][73]
  

Point intéressant article sur la différence meteor et derby.<br>
Point a revoir
[Derby-blog][74]

Fonctionnalité sur laquelle a faire des recherches<br>

```
script/generate

```

<h3>Teach me to code</h3>
site interressant a creuser
[Teach me to code][75]

<h1>Cours Andrei</h1>
gem autorisation est différentes des gems d'authentification.
Faire une différence.

Devise==Authentification
Gem qui fonctionne avec rails

Notions de filtre:<br>
Devise peut utiliser ses points.<br>
  before action <br>
  before conect<br>
<br>
On regarde les paramètres au niveau du controller et on verifie si tout est ok ou non.<br>
Devise est different de OmniAuth qui fait autre.<br>
<br>
Ruby toolbox<br>
  => voir comment ça s'articule<br>
     voir le dernier commit, l'activité.<br>
     voir le nombre de watchers et stars<br>
           Envoi sur le source code<br>
<br>
README comme pitch de la gem. L'idée est d'évaluer rapidement.<br>
<br>
Onglet > pour gérer Chrome pevent duplicate tab<br>
Faire son shopping de gem<br>
Estimer la taille des commits. Utiliser le pulse.<br>

Helpers dans le cadre des authentification == utile<br>
Exemple utilisation avec gem Monban.<br>
<br>
Exemple gem clearance<br>
CCL:<br>
Testons le - faisons une application minimale<br>

Nb turbolinks = gestion du javascript de manière plus rapide.<br>
Oauth <=> comme standard specification.<br>

Bon point quand il y a un tuto.<br>
Voir nombre de pages sur le wiki de la gem<br>
Authlogic<br>
Wiki sous la forme d'un How to <br>
Possibilité d'utiliser les deux en même temps<br>
Prendre le moins que l'on a besoin.<br>
<br>
Site pour le décryptage des commandes shell
[Explain-Shell][76]<br>
<br>
Token a mettre non en clair<br>
<br>
Workflow in web development a video by Zach Leathermann<br>
[Tool/die][77]<br>

Work about how to code, il utilise un vimrc interressant en ce qui concerne le developpement en javascript<br>
[Rob Levin-howtocode][78] <br>


Hackathon DATAJAM  - Informations recuillies - Impressions diverses et reflexions (Synthèse)<br>

magicbox

design modo

webdesignerdepot.com

urbanexpe


livingtuts.com

sigmajs
les surgissantes

linkurious

MOMA = museum of modern art

atelier iceberg

ateliercartographie.wordpress.com

bakbonejs


techonmap.fr

lefresnoy.net

Linux silex

homengo.com/datajam

home 'n' go

luminosity = jeu  Ressources Erwann

Travail sur les ressources d'andrei a faire
    =recherche sur liv intéractif en javascript 
    =Installation eclipse et autre IDE a envisager.
    =Travail a faire sur le developpement des apps - travail sur tout ce qui est serveur

Version intéressant du site du hackathon
file:///home/simplon/Documents/hackaton/DATAJAM/meltingPost/meltingPost/index.html

Pirate pad hackathon
https://www.piratepad.ca/p/mediaposte

Tutoriel intéressant
http://fr.livingtuts.com/developpement-web/creer-un-site-d%E2%80%99entreprise-de-a-a-z-23-integration-html5-css3/

tip sublime Ctrl+KB = enleve arborescence


## Google chrome webtools ##

[Google Chrome utils][79]
[Group chrome dev tools][80] 
[Page googledev sur chrome developper tools][81]
[Discover School utilities][83]

Brakets a free open editor 
[Webudp8][84]
Cloud9 an ide in cloud 
[Cloud ide][85]

Nide a IDE for mac and others ???
[Nide a open ide][86]


Commande git a revoir 

```
git checkout -f 'Sha1 ou tag'
```

Force le retour a une modification locale<br>
<br>
NB Dans un commit possibilité de faire plusieurs saut à la ligne.<br>

PeerJs qui permet de faire le Webrtc


Angular a Creuser


Nb pour faire le set up d'une variable d'environnement.<br>
```
echo 'export CHROME_BIN="/usr/bin/chromium-browser"' >> ~/.bashrc && source ~/.bashrc

```


  [1]: www.rubymonk.com
  [2]: www.codeacademy.com
  [3]: http://railscasts.com/
  [4]: http://tutorials.jumpstartlab.com/
  [5]: http://betterspecs.org/#short
  [6]: http://ftp.traduc.org/doc-vf/gazette-linux/html/2002/083/lg83-B.html
  [7]: http://ruby.railstutorial.org/ruby-on-rails-tutorial-book
  [8]: http://french.railstutorial.org/chapters/beginning
  [9]: http://yakiloo.com/getting-started-git-flow/
  [10]: http://labs.grupow.com/blog/2011/07/05/getting-started-with-git-flow
  [11]: https://www.atlassian.com/fr/git/workflows#!workflow-gitflow
  [12]: www.vimcasts.org
  [13]: http://lukaszwrobel.pl/blog/tmux-tutorial-split-terminal-windows-easily
  [14]: www.37signals.com
  [15]: http://net.tutsplus.com/tutorials/ruby/ruby-for-newbies-testing-with-rspec/
  [16]: http://rubular.com/
  [17]: http://stackoverflow.com/questions/7465259/ruby-on-rails-reload-current-page
  [18]: http://stackoverflow.com/questions/11236360/using-an-ajax-call-to-update-a-rails-page-without-a-refresh
  [19]: http://stackoverflow.com/questions/3235315/how-to-reload-a-div-using-renderupdate-and-replace-html
  [20]: http://simonecarletti.com/blog/2010/06/unobtrusive-javascript-in-rails-3/
  [21]: http://w3m.sourceforge.net/MANUAL
  [22]: https://www.easel.io/
  [23]: http://css3generator.com/
  [24]: http://www.clapico.com/2012/07/04/shelr-tv/
  [25]: http://overapi.com/css/
  [26]: http://www.google.com/fonts
  [27]: http://iconmonstr.com/random/
  [28]: http://www.icondeposit.com/design:108
  [29]: http://www.youtube.com/watch?v=3p_MZsnUENc
  [30]: http://fontastic.me/
  [31]: http://js2coffee.org/
  [32]: http://www.clapico.com/2012/04/14/w3m/
  [33]: www.usevim.com
  [34]: https://news.ycombinator.com
  [35]: http://denisrosenkranz.com/tuto-introduction-a-tmux-terminal-multiplexer/
  [36]: https://practicingruby.com/articles/ways-to-load-code?u=dc2ab0f9bb
  [37]: http://danielkummer.github.io/git-flow-cheatsheet/
  [38]: www.alliancy.fr
  [39]: www.funix.org
  [40]: https://github.com/spf13/spf13-vim
  [41]: https://coderwall.com/p/_g2vpq
  [42]: http://tuom.as/2013/11/24/my-ruby-on-rails-workflow-with-vim-rspec-and-tmux.html
  [43]: https://www.braintreepayments.com/braintrust/vimux-simple-vim-and-tmux-integration
  [44]: http://projectidealism.com/posts/2013/9/20/my-tmux-configuration-with-tmuxinator
  [45]: http://leonard.io/blog/2012/05/installing-ruby-1-9-3-on-ubuntu-12-04-precise-pengolin/
  [46]: http://askubuntu.com/questions/261329/package-for-ruby-2-0-on-precise
  [47]: http://fr.openclassrooms.com/informatique/cours/des-applications-ultra-rapides-avec-node-js/installation-de-node-js-sous-linux
  [48]: http://www.awesomecommandlineapps.com/gems.html
  [49]: http://stackoverflow.com/questions/1207715/any-good-ruby-console-application-gems-out-there
  [50]: http://workflowsherpas.com/2013/02/06/quickstart-with-ruby/
  [51]: https://www.ruby-forum.com/topic/138405
  [52]: http://ruby.bastardsbook.com/chapters/web-crawling/
  [53]: http://www.docunext.com/blog/2009/08/simple-ruby-timeout-example.html
  [54]: http://robdodson.me/blog/2012/06/14/how-to-write-a-command-line-ruby-gem/
  [55]: http://guides.rubygems.org/make-your-own-gem/
  [56]: http://rubylearning.com/satishtalim/ruby_exceptions.html
  [57]: http://spf13.com/project/spf13-vim/
  [58]: http://vim.spf13.com/
  [59]: https://whatdoitest.com/
  [60]: http://www.hiringthing.com/2012/08/02/rails-testing-demystifying-test-unit.html#sthash.au9QITub.dpbs
  [61]: http://andreapavoni.com/blog/2013/8/a-rails-4-tutorial-application-for-beginners
  [62]: http://www.designyourway.net/blog/resources/25-web-development-blogs-you-should-be-reading/
  [63]: http://todomvc.com/
  [64]: http://javascriptmvc.com/docs/steal.html
  [65]: http://www.youtube.com/watch?v=E1NIJjTYq6U
  [66]: http://yeoman.io/
  [67]: http://learn.appendto.com
  [68]: http://www.alsacreations.com/article/lire/565-JavaScript-organiser-son-code-en-modules.html
  [69]: http://www.alsacreations.com/article/lire/565-JavaScript-organiser-son-code-en-modules.html
  [70]: http://thecodeplayer.com/
  [71]: http://la-vache-libre.org/bittorrent-sync-proprement/
  [72]: http://askubuntu.com/questions/284683/how-to-run-bittorrent-sync
  [73]: http://www.tuicool.com/articles/IBjAfqQ
  [74]: http://blog.derbyjs.com/2012/04/14/our-take-on-derby-vs-meteor/
  [75]: http://teachmetocode.com
  [76]: http://explainshell.com/
  [77]: http://www.youtube.com/watch?v=NkVmhe-vvAo
  [78]: http://www.youtube.com/watch?v=i9MHigUZKEM
  [79]: http://www.html5rocks.com/en/tutorials/developertools/part1/
  [80]: https://code.google.com/p/chromedevtools/
  [83]: http://discover-devtools.codeschool.com/chapters/1?locale=en
  [84]: http://www.webupd8.org/2013/11/install-brackets-in-ubuntu-via-ppa-open.html
  [85]: https://c9.io/
  [86]: http://coreh.github.io/nide
