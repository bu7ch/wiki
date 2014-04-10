


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

Astuce Vim <br>
Ouverture de plusieurs fichiers avec une syntaxe intérieure
```
vim $("ARGS".) 
```

Nb recherche a faire s'il n'existe pas une gem qui transforme app rails en html classique
Existence d'une gem kata
Point a creuser "KATAS a faire "


Créer un site internet d'une entreprise
Créer un site recrutement
Créer un site intégrant du javascript
Créer une application téléphone => voir cordova, apache et autre
Internationaliser son site
Faire un système d'authentification
Intégrer du contenu provenant d'autres sources.
Intégrer une api
Envoi de mail et gestion
Faire un jeu navigateur
Site marchand - étude de cas gem Spree
Webcrawler -gem mechanize , nokogiri
Creer un site avec le format haml et slim
Créer un mini réseau social
Faire un site internet d'information en temps réel.
Faire un dashboard intéractif (Web app)
Faire une application qui transforme le contenu youtube et le met en mp3 sur mon bureau
Web sémantique
Créer un site de chat
Créer ub bot de discussion
Créer un wireframe en ligne de commande ???
Faire une application en Sinatra

Recherche du site dannaeu blog sur la frabication d'un blog en sinatra
existence Gem ruby-graphviz pour faire des graphiques.
Creuser un peu plus l'utilisation de sinatra dans les config avancé SPA Single page 
Existence de PythonMonk

## Cours  Erwann 

Faire schéma fonctionnel ( balsamiq )
Faire les specs
    => Travail a faire sur les points
    => mefier sur les fantasmes des gens

Prendre le temps pour la définition de ses specs

Idée est de croire comprendre ce qui est le web
Web comme dernière roue du carrosse

1- Idées
2
3-Préciser le brief visuellement


1-Sentir le client
2-Analyser le brief
3-Présenter le brief visuellement
4-Spécifications exhaustive
    A la fin d'un mail "qu'en pensez vous ?"
    Ne laisser pas la moindre zone d'ombre subsister

Question de la relation de force

Process bien huilé => good

Existence de javascript Monk ==blog
Utiliser Skype pour tout ce qui est du présentiel

5-Spécifications exhaustive à partir des schémas + design
    Selon le budget et la dispo d'un designer
        Préparer au rendu final
        et/ou demander un point de référence clair
        et/ou préparer un moodboard
        Chaque chose que vous faites doit être facturé.
    
    Site internet dribbble qui permet de faire un moodboard

    Design = 2 sens
    Question de l'affordance Nb = a creuser
        Proportions
        Alignements
        Proportions
    Concept clés pour le design

    Communication perpetuelle

    Personne ne s'est fait virer pour avoir choisi une solution Microsofts

    LaCravateSolidaire=location de costumes

    Attirer attention

Ecouter le client

Question du prix qui est sensible. 
    Recadre le besoin
    Estime les délais
   
Postes Unite J/h PrixJourneeHomme Quantity Total

Prévoir les contingences

Question est de la frabication a l'heure

6 - Kickoff 
Idée de l'accompte
Signature du contrat
wireframe exhaustive

7- Reseau et gérer

8- Trello 

9- Livraison et affinages

Zapire = webapp qui gere les taches et outils

Board Reader = site internet de recherche dans forums
Google keyword tools = outil de recherche et prospection

Point a revoir 

Nb les push sur heroku sont toujours aussi enervant il faudra peut être faire un kata

[Krampstudio-listejavascript][87]
[List of useful javascriptLibraries][88]
[ListeLibrairiesUtiles][89]

[CloneFacebook][90]

## BRACKETS ##
A useful editor , besoin d'installer le livereload sur google chrome
[Brackets video tutorial Youtube][100]



## ViM TIPS

mouvements :

- f<caractere> aller sur le caractère
- t<caractere> aller juste avant le caractère
- <C-v> séléction verticale
- <C-v> Séléction verticale + Shift + i + <insertion caractère> + echap = Ajout d'un caractère en début de ligne # utile pour commenter plusieurs lignes

Questions sur le javascript 
Yeoman est générateur de site dans une optique statiques.
Le javascript n'inclue pas la modularisation.
Node permet la mise en console javascript en shell => creuser


## GEM UTILES
Gems utiles au développement 

[Symbioz gem utiles part1][101]
[Symbioz gem utiles part2][102]
[Symbioz créer gem ][103]


<h1>rails g task </h1>
Génération de tache rake en rails

existence de Ultra-Repl en javascript pour gérer son javascript en mode pry
[Ultra-Repl][104]

Probleme des params

[Probleme du parames][105]

Jquery UI = Framework pour les effets javascript Drag'nDrop
jquery-uirails
gem existence act_as_a_list


knowledge graph = Outils Freebase
Existence sous node js d'un paquet freebase
npm install freebase

Sans clé mais avec quota

amazone scrapper paquet qui rcherche sur amazon résultat de recherches

Animate.css


Atelier ANdrei Projet 

Ne pas mettre tout sur la meme page<br>
Donnez des exemples et inviter des personnes à faire de meme.<br>

Question du dialogue par rapport au visiteur
Idée principale est de changer sa landing page meme en cours.

Google Analytic est très importante


Fidéliser par mail
VOir selon comportement et selon le flux.
Avoir le mail des gens est le plus important.

Utilisation d'une clé token

Idee d'être plus parlant
Question des call to actions
Login via email


Ressources utilisé pour le templating en vim

[Symbioz utilistaion de vim][106]


API Webshell qui permet de combiner les API et de créer du JSON et autre. A creuser<br>
[Webshell][107]

Node tutoriel du débutant A faire
[nodeguide.com /beginner][108]

Suckless
Logigiels écrit de manière minimale<br>
[suckless][110]

Utilisation de pry en avancé<br>
[SitePoint -pry][111]

Possibilité de stocker ses données en javascript
[OpenClassroom jstorage][112]


Outils pour mockup site internet 
PERCH

Outils Cms
Azure

Blog Hugeen pour utilisation angular notes de développement
[Hugeen notes de developpement-rails-angular][113]

Creation chat avec node
[tutoriel chat node][114]

Partie 2

[tutorielChatnode2][115]

Possibilité de faire un .build pour faire un ensemble lié
Idée est que le controlleur = naviguation 
Model contient les règles générales impératives.

Sous pry possibilité d'utiliser edit methods pour editer directement sous vim notre code
Possibilité de faire des opérations classiques sur objet active Record

=> travailler manipulation de Pry


VIM 

Utilisation de la commande 'gp'
Paste à un endroit précis

Libv8 = moteur google chrome

Nb Existence de paris api

gem smartcsv qui permet de parser un tableau en csv
gem csv_pirates

Transfo de Xml en json => usage d'un hack
[Stack overflow xml to json][116]

Existence de la gem crack
Existence sur github apotonick/representabele

Existence de la gem chartkick pour faire des graphs

Mots clés = json parsers
Mots clés=chart

Gem pour intelligence artificielle en ruby 
AI4R
berlin AI

Bouger des lignes sous vim swap lines
[Deplacement de ligne et navigation - wikia tip][117]

Rendre l'utilisation de Vim plus agréable
[Petits outils pour Vim et astuces][118]

"Eviter l'évitable"
"Concours de la motivation"
"autonomie, j'appuie sur un bouton et je suis autonome"

Présentation sur les enjeux de santé <br>
Ingénieur, codeur, architecte et parties.<br>
Nouvelle porte en France est celle du numérique. Profession qui est assez négative dans le numérique.<br>
Idée de comment créer de la valeur dans leur métier.<br>
Nous sommes tous des patients.<br>
Dans la vie il suffit d'avoir un porte clé et oser<br>
Applications crées et utilisés pour les projets.<br>

COBTEC

Santé se cache derrière des tas de concepts<br>
Travailler sur la poste et docapost<br>
Travail sur le nouveau domaine de la santé qui est la poste.<br>
Sphère domestique = sujet majeur
Croissance à deux chiffre = allergie + qualité de l'air.<br>

Vitesse de marche = indicateur de l'indice de vie d'une personne

[Rake article test][119]
[Rake example test][120]



La voix est de retour
Série Black mirror

[Ruby on rails et redmine][121]
[Autotest getting started][122]


Voxer applications

Continuer a fonctionner chez soi<br>
Absence de fonctionnement du chez soi => problème futur


Blog intéressant
http://www.mickgenie.com/tag/shell-run/

Codewars
Achieving mastery through challenge
[Codewars][123]

Creation blog en sinatra<br>
[Danneu bLOG][124]

Gem protected_attributes gère problème du require params
Gem nifty-generators qui aide au scaffold de meilleures formes

 TutoUT 
Doctorant informatique qui donne des conseils sur rails
[UT BLOG][127]

Pry show models


```
npm install -g typescript
```
L'option -g semble générer l'executable en plus de l'installation du paquet par node. Cette option peut nécessiter une installation par l'utilisation de sudo.

```
sudo npm install -g typescript

```

Geddy a micro javascript framework same as rails 
Existence de express pour le même travail

[Article about microFramework][128]

http://blog.evantahler.com/

[Blog de programmeur][129]


Cours Vincent
Serveur = Ordinateur distant 
Configuration via Ubuntu serveur.

Heroku s'occupe tout de l'administration systeme
Digital Ocean

HEBERGEMENT 3 GRANDS TYPE
=DEDIE
=VPS
=PATH =par l'issue des vps et dédié il mettre une couche supplémentaire pour gestion.

Apache server = logiciel
	reprend les requêtes et gère les données
Cuma
 
Serveur n'est jamais parfait => si arrêt => plantage

Limité => on veut aller plus loin.
Travail sur la machine distante en ssh.

On est des touristes

Serveur d'applications => fait du Reverse-Proxy
Question du cache
	2 grosses manières
		Reponses au niveau du serveur web. Mettre en ressources tout ce qui est statique.
		Préciser les zones

Avantage = 5$ par mois


REMY
Méthode de classe

```
class Car
  def self.example()
  end
```

Fin de notes

Pousser des gem tutoriels interessant
Gem cutter gem qui s'occupe du push sur rubygems.
Le paquet a utiliser pour faire sa gem est dans le dossier pkg/

gem push nom de la gem

Lien interressnats
[Rails cast sur rubygem][130]
[Ruby learning blog][131]  A observer de plus près

TCP Dump ou utilisaton de la lecture de paquet - tutoriel
[TCP DUMP][132]


Sanitizer = regexp controlle
Open Graph =recherche sur le point

Gem social-stream
gem socialization

minimal Ui
Skeleton

YUI library pour faire css

GEM POUR CONSTRUIRE DES RESEAUX SOCIAUX TUTORIEL
Commencer a construire par les réseaux sociaux
[SocialStream][133]

beautiful-scaffoffold
font awesome
Glipper
Cordova a travailler
Framework app mobiles = stéroids
Framework app mobiles = titanium

XDK a travailler dessus 


Memo Unix =
utiliser !! pour executer la commande précédente


Creation d'applications en meteor 
[Learning ressources javascript meteor][134]

Approche du javascript plus generale

## METEOR ##
Iron-Routes
RouteMapper pour meteor

NB METEOR est un framework en cours de developpement mais prometteur d'un point de vue des fonctionnalités ainsi les points les plus important a retenir sont 
1. Rapidité au niveau du développement par rapport à des frameworks actuels
2. Maintenance simple et gestion des paquets avancés
3. Le point le mis le plus en avant est la capacité de celui ci à faire des applications en real time (temps réel) de manière simplifié.<br>

Point le plus important est la documentation officielle que l'on trouve a 
[Meteor Official documentation][135]
C'est sur elle qu'il faut essentiellement compter le framework étant a un état embryonnaire.

Deuxieme et pas des moindre est la connaissance du javascript et ce de manière étendue et irréprochable. D'après mes recherches 
1. Il faut utiliser Coffeescript pour éviter trop de complexification avec la syntaxe javascript 
2. Utilisation du framework au jour le jour.

Quelques liens que j'ai déniché sur l'apprentissage du javascript, ces limites et ses avantages:

[Conférence sur meteor et principaux aspects][136]

Site intéressant qui regroupe plusieurs dizaines de ressources sur meteor 

[yOH.de][138]

Existence d'un hackpad sur le sujet meteor

[Hackpad meteor][139]


Lecture de la documentation sur meteor 
l'installation se fait par le curl donné sur le site, ensuite pour créer une nouvelle application on effectue 
```
$ meteor create myapp #Creation de l'application
$ cd myapp
$ meteor #Lancement de l'application

$ meteor mongo #equivalent d'un rails console
$ meteor reset #clear la database
```

Possibilité de voir la console a distance

```
meteor mongo myApp #Rails c sur le serveur distant de mongo
meteor logs myApp
```

Fonctionnalités du meteor mongo
```
<Model>.find() # Affichera tous les enregistrements dans la base de données
<Model>.count() #Indique le nombre d'éléments dans la base de données
<Model>.insert() #Permet d'insérer des informations dans la base de données
```
Ajout de fixtures par fixtures.js

```
Template.<Template>.<methodes ou helper> # s'occupe de tout ce qui fonctionne au niveau de la vue
```

```
Meteor.publish(); #Du côté serveur s'occupe de tout le travail de publication
```


Existence de --help

NB en meteor plusieurs dossier 

collections //Regroupe les collections de meteor
server // tout le code coté serveur
client // tout le code côté client
  views //inclut toutes les vues de l'application
    application //Contient tout ce qui concerne l'application
      layout.html //Fichier layout de l'application
    include //Possibilité de mettre des partiels footers, header et autre
  stylesheet //inclus les styles de l'application
  helpers // Fonctions aide de meteor
public // asset pour tout ce qui est image
lib // toutes les librairies javascript sont a placer dans ce fichier, Gestion aussi du routeur visiblement. LE DOSSIER LIB EST CHARGÉ AVANT TOU LE RESTE.
common// Dossier qui contient du javascript qui s'execute tant du côté serveur que client


main.* // fichiers qui sont chargés en dernier

les fichiers en meteor sont chargés de la plus profonde arborescence vers la plus haute.
Autopublish est le diable du meteor, a enlever 

```
meteor remove autopublish
```
Autopublish publie toutes les données. = mauvais car possibilité de la copie de 50go de données dans le navigateur.<br>
Alors utilisation de publish avec la publication de données partielles.<br>

Fonctions a regarder de près:
```
_publishCursor()
.added()
.updated()
```


<h2>ROUTAGE EN METEOR</h2>




NB regle pour gerer l'autorun qui update en temps réel toutes les pages

1. On publie d'abord (coté serveur)
2. On s'abonne ensuite (coté client)

Meteor charge tous les fichiers javascript 
Existence de fichiers spéciaux tels que

Nb le client ne doit jamais avoir un accès direct au serveur!!
<b>Le client devrait n’avoir accès qu’à ce dont il a besoin pour fonctionner à un moment donné, rien de plus.</b>


Notion de publication et abonnement sur meteor

NB creation des fichier en parallèles
server/client.js
client/client.js

A priori les vues du cotés client seront en double 
client/movies.html
client/moviesTemplate.html


Meteor use du template handlebars

mettre des balises templates
Dans le fichier template
<template name ="NomFichier_sansExtension"></template>

Appel dans le fichier html
{{>NomFichier_sansExtension}}


Enlever dans meteor le module insecure 
```
meteor remove insecure
```

Ajout de routeurs en meteor 
```
meteor add router
```
Ajouter Iron-router par l'intermédiare de meteorite pour pouvoir commencer a user de routes
Verifier si la syntaxe est mrt add iron-router


Le manager meteor se place a côté du template avec le même nom mais se terminant par un .js
Il comprend les données qui seront usés par le template

Les collections s'occupe de l'aspect temps réel des données


Avec Handlebars la navigation pour les routeurs est la suivante:
```
href ="{{pathfor '<template>'}}"
```

Package spinner qui permet de créer une animation de transition
inclure dans le code par l'intermédiaire des handlebars
```
{{>spinner}}

̀```

Meteor session
=> stocker des données éphémères qui sont vis a vis de la version courante de l'application.<br>

Les sessions sont toujours en actions pour tester l'entree de variables => user du meteor mongo 
et taper 
̀```
Session.set('<Template>','Variable')

```

Le code a l'intérieur d'un bloc délimité par Deps.autorun va se lancer de manière automatique et gerera la mise a jour automatique.<br>

Lecons a retenir pour les sessions

1. Always store user state in the Session or the URL so that users are minimally disrupted when
a hot code reload happens.
2. Store any state that you want to be shareable between users
within the URL itself

Possibilités de faire des includes dans meteor structure include comporte un layout, header et footer<br>

Fichier de configurations existant en meteor possibilité qu'ils soient propres a chaque dossier
Dans un sous dossier helpers dans client
client/helpers/config.js

Configuration dans ce dossier des conditions pour l'accès au compte.

Les collections font partie du coeur de meteor 
La réactivité sa coquille 

Utilisation de la fonction observe() pour préparer les éventuelles modifications par rapport au champs.
Avec observe() utilisation de trois autres méthodes 
1. added
2. changed
3. removed

Computation peut être aussi utilisé pour le temps réel.

allow() => autorisation faite de la part du serveur
deny() => refus de la part du serveur

Hook => like a postguard that's check before doing any actions or routes, intercept the routing process.

Manipulation des events
```
Template.<"TemplateName>.events(function(e){});
Inserer toujours un e.preventDefault 

Rappel en meteor tout fonctionne par paire
Le formulaire
Le javascript pour execution 
Le routeur et le code coté client et ou serveur pour son execution

Iron-Router

publish est en paire avec subscribe
Existence d'un config.js dans les helpers

Routeur de meteor
[Manuel Schoebel][140]

[DiscoverMeteor][141]


## RAILS APPROCHE ##

Gem utile au developpement par rapport à l'article de nettuts à tester désormais.
[codetuts gem utiles developpement rails][142]


gem 'carrierwave'
=> Solution classique pour tout ce qui est de l'upload en rails

gem kaminari 
=> effectuer de la pagination avec rails, faire plusieur pages d'un même sujet

gem haml
=> Eviter d'utiliser l'HTML

gem Authlogic
=> gère tout ce qui est de l'authentification

gem shoulda 
=> gestion des test unitaire, théoriquement plus léger et efficace que rspec

gem "capybara"
=> navigateur pour test

gem factory-girl
=> Creation de fixtures pour les test

gem Rmagick
=> Utilisation de librairie rmagick pour travail sur l'image

gem Cancan
=> Gestion des authorisation 

gem nokogiri
=> parser html xml css

gem sass 
=> css + super pouvoirs

gem formstatic
=> gestion des formulaires

gem capistrano 
=> execution parallele (a observer de plus près)

gem Omniauth
=> authorisation

gem resque
=> Creation de delayed jobs, background jobs

gem jammit 
=>compression de javascript et css

gem eventmachine
=> Créer serveurs et clients

gem mustache
=> handlebars de ruby on rails

gem chef
=> With Chef, you can manage your servers by writing code, not by running commands.

gem thinking sphinx
=>recherche dans de grandes bases de données

gem passenger 
=>Phusion Passenger™ — a.k.a. mod_rails or mod_rack — makes deployment of Ruby web applications, such as those built on the revolutionary Ruby on Rails web framework, a breeze.

gem paperclip
=> gestion des images

gem wheneverize
=> repetition et cron 

gem clockwork
=> repetiotion et cron

gem devise
=> Authentification

J'ai trouvé d'autres gem intéressantes à creuser soit 
[CodeBeerStartup][143]

gem "frank"
=>Permet de créer des sites staitque a la vitesse elevée.

gem fontawesome
=>Gestion des icones

gem "better_errors"
=> "message d'erreur plus compréhensible"

gem "binding_of_caller"
=>

gem 'annotate'
=>Schema du modele annoté en commentaire

gem 'bullet'
=>Augmenter la vitesse en diminuant le nombre de requêtes

gem 'debugger'
=>"debugger efficace pour rails

gem 'flay'
=>analyse code pour éviter doublons

gem 'hirb'
=>pour rails c un tree, no wrap table etc

gem 'localtunnel'
=>Rendre public un rails s pour le réseau et par internet

gem 'lol_dba'
=>Analyse des models et des id en vue de migration

gem 'mailcatcher'
=>gestion des mails et envoi en local

gem 'meta_request','0.2.1'
=>rails panel in google chrome qui permet de gérer les requetes effectués

gem 'pry'
gem 'pry-doc'
=>gem pour le debuggage

gem 'quiet_assets'
=>mutes asset pipeline messages

gem 'rack-mini-profiler'
=>Speed badges

gem 'railroady'
=>Génération diagramme uml

gem 'rails-footnotes', '>= 3.7.5.rc4'
=>Informations user en bas de chaque rails app

gem 'rails_best_practices'
=>"meilleures pratiques en rails"

gem 'reek'
=>Code smell detector for ruby

gem 'request-log-analyzer'
=>performance log analyzer

gem 'smusher'
=>reduction less of images

gem 'mailchimp'
=>avoir une newsletter

gem 'zeus' # don't add this in your gemfile.
=> permet de generer plus rapidement scaffold et generateurs

gem 'strong_parameters'
gem 'protected-attributes'
=> Gestion autorisation en rails


gem bb-code
=> Markup ??

gem 'faker'
=> generer de la fausse donnee

Autres liste de gem utiles
[10gems to use][144]


Truc pour debugger en rails
Ajout d'une instruction fail
Existence d'une méthode "code HTML" .html_safe
ou content_tag()


  			
Editeur ACE
[Editeur Coffeescript et javascript online plutot bon et marrant][137]


PRY <br>
Information sur le pry, existence des gem pry-rails, pry-doc, jazz_hands qui gère les consoles
[Zone Informations sitepoint pry][145]

FOREM gem pour la gestion de forum

Tutoriel orienté Ruby et ruby on rails
[Ruby on rails tutorial point][146]

Rubinius = > ruby en ruby

Prelang utilitaire ruby on rails pour développement rapide

NE JAMAIS UTILISER LA NOTATION CAMEL CASE EN RUBY 

RAILS 

```
localhost:3000/rails/info
#Affichage des informations essentielles de l'application
localhost:3000/assets/application.js
#Affichage de tout le javascript

```
Dans la console rails c, taper 

```
$ rails c
$ >y _ #liste des dossiers parents et autres
```

Fonction de debuggage rails
```
LienPage/?debug_assets=1

```

Lien javascript et mini librairies à creuser:
[20 minis libraries][147]
[Mini javascript libraries][148]
[Javascript Game libraries][149]


```
def unchange 
	changement de la migration

end

```

gem merit


Ajout de colonne

Technologies javascript supplémentaires
Ember à creuser

Rails Prompt utile
```
Rails.logger.debug("message")
Rails.logger.warn("message")
```

Javascript Bin pour tester code javascript 
```
jsbin a tester

```

bootsnip.com
Element a ré"utiliser

Point a revoir sur les modeles et leur relation

mker.io
reveal.js
mozilla personna


Commande via git pour ignorer des fichiers
```
git update-index --assume-unchanged path/to/file.txt

```


Site internet avec des vidéos et ressources sur meteor
[Eventedmind][150]

Elliot js pour faire des graphiques intéractifs

Liste Github sur les games engines
[Github-game engines][151]

Treehouse cours javascript


```
/\A[\w+\-.]+@[a-z\d\-.]+\.[a-z]+\z/i	full regex
/					start of regex
\A					match start of a string
[\w+\-.]+				at least one word character, plus, hyphen, or dot
@					literal “at sign”
[a-z\d\-.]+				at least one letter, digit, hyphen, or dot
\.					literal dot
[a-z]+					at least one letter
\z					match end of a string
/					end of regex
i					case insensitive
```


NOOWITT
FLIPBOARD

Chatterbots

gem chatterbots en ruby

Muffinlabs - site cool
[muffinlabs][152]
[muffinlabs][153]


Cours ruby 
Methode freeze qui permet de GELER tout objet
flatten = reduction de tableau
store = rajouter element dans le hash
not = existence en ruby 

redo = faire repasse l'itération courante de la boucle = gestion des erreurs
||= eviter les if
&= inverse

```
heroku pg:reset DATABASE

```

module = classes sans variable 
=> possibilité de faire de l'héritage multiple
aJOUT module possibilité de faire le meta programmation


tweetegy


```
ps -aux | grep firefox

```

Gem ffi = ruby en c
Rubinius = autre version de ruby

[Add routing meteor js][153]


Mozilla learning javascript 
[Mozilla learning javascript][154]

+P2PU.org javascript

Cours Erwann
Sautage de verrou et electrochoc

Concept qui permet d'avancer => remuage de plusieurs concepts.
GROSS RAKING

Marketing web
Bootstraper definition => Commencer démarrer entreprise, création de son outil. Création d'un mvp d'abord acquérir des résultats avant de chercher de l'argent.
Création d'un produit qui fait ses preuves.

300 utilisateurs actifs.
Faire la preuve que son produit marche avant les fonds.

Eviter la "vanities", toutes ses victoires qui ne donnent pas de résultats.

Pire des vanities est de réver son projet.

Etat de lieux a faire de ce qu'on sait faire.

=> Idée du super projet. On est pas dans l'entrepreunariat traditionnel.

Valeur lucrative => questionnement et modèle économique. Rare qu'il connaissent leur économie.

FRAMEWORK AARRGH

Aquisition 
Activation
Retention
Refferal 
Revenue

Acquisition = metrics <=>Tous les gens qui viennent sur votre site et votre landing page.

Activation = Nbre de personnes qui vont s'inscrire dans votre service.

Retention = Nbre de personnes qui vont devenir des utilisateurs actifs, Taux de rétention dépend vraiment de votre app

Refferal = Tous les users qui vont devenir ambassadeurs. Utilisateurs qui attire d'autres utilisateurs.

Revenue = Pricing

SEO, SIM, RELATIONS PUBLIQUES, CAMPAGNES
Idée du + tu publies et plus c'est ok

Faire plus de CRM 
Question du vous ne pouvez pas tout gérer
La traction = qd le produit est bon => trop de sollicitations, idée est de faire des sauts.

Important est de gérer les datas.

mesure - learn - refactoring

A/B Testing

Version A et Version B d'un même site pour faire du test 

Ce qui est en jeu est la cognition

Automatiser un max
Rechercher des utilisateurs

podio.com

google recherche utiliser le moins 
-alterné -droit

Gross hacking

growth hacking

Utiliser quora

Thank you economy

ycombinator

spullrocket

producthunt.co 

Algolia hackernews
= Recherche sur hacker news

Cloudflare
= ajout de script analytics

Medium.com

Kissmetrics

EMBER
Existence de EMBER Data pour gestion des Apis
NB pour Ember application

Creation de notre application dans app.js
```
var App= Ember.Application.create({});
//Existence d'options 

var App= Ember.Application.create({
	LOG_TRANSITIONS: true
});
```
Mettre les templates dans des div handlebars

```
  <script type="text/x-handlebars" id="index">
```
Varibles en handlebars

```
<h1>Welcome to {{handlebars}}</h1> // Varible en handlebars

<script type="text/x-handlebars" data-template-name="index"> //nomination nom template

{{outlet}} // Indique ou le template doit être rendu


```


Routeur
<=>Tronc
Travail dans app.js

```
App.Router.map(function(){
	this.route('about');
});

//Aller dans des chemins de chemins

App.Router.map(function(){
	this.route('about',{path: '/aboutus'});
});
```

Créer un modèle en Ember

```
Todos.Todo=DSModel.extend{
	title: DSattr('string'),
	}
```

Emberjs 
Tutoriel intéressant
[Coding smashing][156]
[Ember and rails ][157]
[devomynd][158]
[hashrocket][159]
[blog dxn][160]
[Collective ideas][161]

Existence des embercasts et ember101
https://speakerdeck.com/raycohen/ember-views
https://www.youtube.com/watch?v=1QHrlFlaXdI
A voir

Spinejs autre framework javascript

Test avaec jasmine 
= 2 gems
jasmine 
jasmine-jquery-rails
Gem rb fs-event pour faire les automatismes
friendly id = mettre des noms de modeles dans le browser

trello.com

codetutsplus -rails

Lien sur des screencast interessants
[DevBlogs avdi][162]

Cosy.io 
Cosycloud

si yen a qui veulent jouer avec un cozycloud (cf https://www.cozycloud.cc/ ), on en a installé un sur un PC à simplon => http://192.168.1.95:9104
password: simplonco

cc @emilien

si quelqu'un sait comment lui donner une ip fixe aussi, ça peut m'intéresser :) @yan @andrei 

Notes developpement word mesh ou mashup

SEO Cours
Travail dans le SEO. 
SEO(Fravia search engine optimizer =  spammeur est de travailler sur ces points)
But de tout SEO est de mettre un site bien positionné.

Intérêt = obtenir du traffic de qualité.

Adword vs adsense
Publicité classique vs publicité de masse
Traffic search

Comment avoir du traffic gratuit ?
Traffic du qualité == €€€

Pyramides
Architecture
=> d'abord le rendu final du site, le html, code HTTP. Header HTTP.
Envoyer du 200. eviter les codes d'erreurs.

Notamment les codes erreurs côtés serveurs.



## SQL ##
```
USE movie1_db

SELECT * FROM movies WHERE year >=2009
SELECT * FROM movies WHERE year BETWEEN 1999 AND 2004
SELECT name FROM actors WHERE name LIKE "%Tom%"
SELECT * FROM movies ORDER BY year ASC, title DESC // peut être mis en DESC


SELECT * FROM movies LIMIT 10 OFFSET 20

//SQL statement which we can create database
CREATE SCHEMA movie_db

CREATE SCHEMA IF NOT EXISTS movie_db
CREATE DATABASE IF NOT EXISTS movie2_db

//SQL statement that's allow database structure
CREATE TABLE actors(name VARCHAR(50))

//Creation d'engines
CREATE TABLE actors(name VARCHAR(50)) ENGINE InnoDb


//CREATE
//Inserer de l'information

INSERT INTO movies (title,year) VALUES ("Aliens",1986);
//Syntaxe alternative
INSERT INTO movies  SET title="Back to future", year=1985;

//UPDATE
SET SQL_SAFE_UPDATES = 0; //eviter les réecritures
UPDATE movies SET year="1985" WHERE title="Avatar 2";

//DELETE
DELETE FROM movies WHERE title="Avatar reloaded" AND year=2016;
SQL_SAFE_UPDATES=1;

//RENAME TABLE
RENAME TABLE movies TO movie_table

//DROP TABLE
DROP TABLE actors

//TRUNCATE 
TRUNCATE actors

//MODIFY COLUMN SCHEMA
//ADD COLUMNS
ALTER TABLE movies ADD genre VARCHAR(25);

//CHANGE COLUMNS
ALTER TABLE movies CHANGE COLUMN year release_year YEAR ;

//REMOVE COLUMN
ALTER TABLE actors DROP place_of_birth


//REMOVE DATABASE
DROP DATABASE movie_db3
//safer
DROP DATABASE IF EXISTS movie_db3
```
Normalization

Type of keys
Primary keys
Unique keys
Foreign keys



```
//primary KEY
CREATE TABLE t_genres (pk_id INTEGER NOT NULL AUTO_INCREMENT PRIMARY KEY , uk_name VARCHAR(4
5) NOT NULL UNIQUE);

//alter key
ALTER TABLE t_movies ADD pk_id INTEGER AUTO_INCREMENT PRIMARY KEY FIRST ;

//alter a foreign key - a creuser
ALTER TABLE t_movies ADD fk_genre_id INTEGER NULL, ADD CONSTRAINT  FOREIGN KEY (t_genres) REFERENCES t_genres(pk_id)

```

Modification 
JOindre des tables 

```
//INNER JOIN
> SELECT * FROM movies INNER JOIN genres ON movies.genre_id = genres.id

//OUTER JOIN LEFT
SELECT * FROM movies LEFT OUTER JOIN genres ON movies.genre_id = genre.id
//un peu mieux
SELECT movies.title, genre.name FROM movies LEFT OUTER JOIN genres ON movies.genre_id = genre.id

Nom b AS Alias b

```


## COURS SEO ##

Extension chrome pour verification redirect path, hurl.it
Code d'entête
Regle fondamentale soit 

1Url = 1 contenu et 1 contenu=1url

ht acces => deplacement

Google bot n'a pas de javascript
Prefère des site internet peu gourmand et très rapides
Cache qui est important

Architecture => Contenu de qualité

Navigateur Lynx <=> a ce que voit google
Javascript est en surcouche

Plus proche est plus vu , le plus loin est eloigné.
Fond blanc sur fond blanc

Backlinks = Lien entrants

Thématique moz => Travail sur les backlinks 
Je regarde comment font les autres et j'effectue.
Google webmasters tools.

Communiqués de presse. Echanges de lien

Google + = impact indirect

Aspect porte avion 
Aspect pirate somalien

Unleash the monster 

Verifier son architecture

Google Penguin et Panda

Google Bombing

Page rank 1+>10, 10sup Google pageRank

Utilisateur qui gère leur contenu, le plus possible.

little snitch

Epic

Wildcard DNS

## VIDEO ANDRE ##

UTILISER DES VERSIONS PAR DEFAUT
Outils rails 
=logger

gem 'quiet_assets' 
=> log propre

Affichage dans le logger
```
logger.debug"text logger"
```
Utiliser la rails console
Utiliser cette console le plus souvent possible
Tester des méthodes
Creation de fausses données.

```
# encoding: utf-8

namespace :dev_data do 
	desc "Fill database with sample data"
	task create: :environment do 
		Challenge.delete_all
		Challenge.create!(
			title:"cloche pide",
			description:"Faite 2à fois",
		)
	end
end
```
Faire un rake personnalisé avec des fausses données.
dev data a mettre a jour.

Différents controller pour différents modèles.

Nested routes 
pour les formulaires existence d'un trick

```
<%= form_for [@challenge, @participation] do |f| %>

<% end %>

```

existence de commandes rakes personnalisé et à reflechir 
```
rake db:drop

Rake::Task['db:drop'].invoke 
Rake::Task['db:reset'].invoke
Rake::Task['db:migrate'].invoke  

#Mise en forme   
 strftime("%d %b %Y")
```
Gravatar pour faire des liens
Existence de scope = filtrage des données en statique ma  is aussi en dynamique

Pages dynamiques
```
#Scope statique
scope :high_points , -> {where("points > ?", 50)}

#scope dynamique
scope :above_points, ->(min_points) { where("points > ?",min_poijnts)}

#Travail au niveau des routes

resources :challenges do 
	resources :participations
		collection do 
			get 'running'

	end
end
 
```

HOOKS

```
after_create
before_create
```

Modele lui même doit s'occuper de lui même

Controller a faire le plus minimaliste possible et mettre nos données dans le modèle

[Selenium vs capybara][163]


## Ember js ##

tutoriels
[Lost techies blog Ember][164]
[InfoQ ember][165]
[Ember js missing tutorial][166]
[ArtistTutorialEmber][167]
[Wanna start emberjs][168]
[EMberjs beginner tutorial][169]


Faire un workflow sur sublime plus elaboré
[Sublime ultime workflow ][170]


## Cours Sur le Ruby ++ ##


http://simplon.rocknroot.org/ruby_poo/index.html#/9

self.langage

Monkey patching

## Hackathon Cartoviz ##
Forme de narration et forme de  visualisation => innnover
Numeric facet = distribution de données

Open facet

Datagouv = pages ressources interessantes
Problème d'encodage

Facet et gestion
Utilisation de geocoder pour préparer le creation des points
Toujours traitement à faire

Attention au geocoder
=> être sensible à ce point

Cartoviz - Outils
Sélection d'outils utiles pour les participants au concours
http://cartoviz.lafonderie-idf.fr/
Géocodage, nettoyage et conversion
Visualiseur d'adresses : http://logiciels.ign.fr/?Visualiseur-d-adresses
BatchGeo : http://batchgeo.com/
Batch Geocodeur : http://www.batchgeocodeur.mapjmz.com/
Batch Geocode : http://www.findlatitudeandlongitude.com/batch-geocode/
OpenRefine : http://openrefine.org/
Play With Data : http://jeanabbiateci.fr/play-with-data/
MyGeodata Converter : http://converter.mygeodata.eu/
Géocodeur mondial unitaire et batch: http://www.arcgis.com
GeoDesign
Mapbox : https://www.mapbox.com/
TileMill : https://www.mapbox.com/tilemill/
Map Stack : http://mapstack.stamen.com/
Snazzy Maps : http://snazzymaps.com/
MapStylr : http://www.mapstylr.com/
Tilesets : http://www.pinterest.com/loichay/design-de-tuiles/
ColorBrewer : http://colorbrewer2.org/
Maki : https://www.mapbox.com/maki/
Map Icons : http://mapicons.nicolasmollet.com/
Narration spatialisée
Story Maps : http://storymaps.arcgis.com/
Tour Builder : https://tourbuilder.withgoogle.com/
Geonef : http://www.geonef.fr/
StoryMap JS : http://storymap.knightlab.com/
TimeMapper : http://timemapper.okfnlabs.org/
Searchable Map Template : http://derekeder.com/searchable_map_template/
JEO WP Theme : http://cardume.github.io/jeo/
CartoSet : http://www.vizzuality.com/products/cartoset
Map Tales : http://maptal.es/
Infoviz et graphiques
Datawrapper : https://datawrapper.de/
Google Charts : https://google-developers.appspot.com/chart/
Many Eyes : http://www-958.ibm.com/
Raw : http://raw.densitydesign.org/
Quadrigram : http://www.quadrigram.com/
Infoactive : https://infoactive.co/
Datavisual : http://datavisu.al/
Infogram : http://infogr.am/
The Data Visualisation Catalogue : http://www.datavizcatalogue.com/
Dataviz Tools : http://selection.datavisualization.ch/
Edition cartographique et géovisualisation
ArcGIS Online: http://www.arcgis.com/
QGIS : http://www.qgis.org/
CartoWeb : http://cartoweb.org/
CartoDB : http://cartodb.com/
GeoCommons : http://geocommons.com/
ViziCities : http://vizicities.com/
StatSilk : http://www.statsilk.com/
DataAppeal : http://www.dataappeal.com/
Tableau : http://www.tableausoftware.com/fr-fr
Google Fusion Tables : http://www.google.com/fusiontables/
Google Maps : http://www.google.com/enterprise/mapsearth/
Umap : http://umap.openstreetmap.fr/
Geojson.io : http://geojson.io/
ZeeMaps : http://www.zeemaps.com/
Click2map : http://www.click2map.com/
MangoMap : https://mangomap.com/
MapsData : http://www.mapsdata.co.uk/
Mapline : http://mapline.com/
Librairies de développement et APIs cartographiques
Leaflet : http://leafletjs.com/
OpenLayers : http://openlayers.org/
D3 - Data Driven Documents : http://d3js.org/
Kartograph : http://kartograph.org/
Modest Maps : http://modestmaps.com/
rMaps : http://rmaps.github.io/
Crosslet : http://sztanko.github.io/crosslet/
DataMaps : http://datamaps.github.io/
Unfolding : http://unfoldingmaps.org/
Polymaps : http://polymaps.org/
amMaps : http://www.amcharts.com/javascript-maps/
API Geoportail : http://professionnels.ign.fr/api-web
ArcGIS JavaScript API: https://developers.arcgis.com/javascript/
Bing Maps API : http://www.bing.com/dev/en-us/dev-center
Google Maps API : https://developers.google.com/maps/?hl=FR


Ign a publié pac de données
openDataSoft - bibliothèques qui sont présentes
Grace a google analytics possibilité de faire du json.

data.iledefrance.fr.api

ArcGis online
leafleet
bbotstrap-map
jo - json
rich documentation

3 niv description sous open streetmap


IGN Webservices disponibles

Geoportail javascript qui permet de superposer avec les données de l'iGn - Bibliothèque open source.
Dvelopppement de nombreux outils
114 couches et mise à jour quasi continuelle

Principale fonctionnalités = visualisateur de touche , geometrie
Openlayers

Api standard

Api étendue

Api haut niveau (AHN)

Visualisation des données sur la base nationale

Utilisation en user agent

Developpez.com est partenaire de l'ign

Ubimix
Initiation a Leaflet
Ecosysteme de leaflet

ALTIC
Bi en open source - a creuser
talend
altic search

Youmap 
Bi en open source


Open street map 
Application sur les bancs publics
=> possibilité sociale et autre

Faire un hackhaton interne
Bancs public qui disparaissent

Telephone portable et tout ce qui est mobile .
Les villes devienne de plus en plus lisse

Résistance Theâtre 

Bancs est un enjeu politique 
Commentaire et avis 

Projet roxanna

Question de la réunion

Vraie utilité d'application

Nb lien à faire entre site et application mobile

Travail sur cartodb a faire, qui est la jointure et gère sur l'ensemble

Faire listes des données possibles.
Penser a la mise en forme
Utilisation de différentes couches

Utilisation de tables 
CartoDb = aspire la donnée pour utilisation
Voir comment cartoDb marche

=> comment utiliser votre service

Afficher certain couches

Fond utilisé par MapBox

Attention a la mise en point et des noeuds
=> attention à la quantité de données

Ce que vous voulez afficher et comment 


Journalisme++ = société = mettre de nouvelles manières de faire du journaliste
Utilisation de Datawrapper

Mettre de la donnée rapidement effets +
Kartograph.js et .py

Il est facilement optimisable

Kartograph = librairie qui utilise la visualisation + TECHNIQUE
Pourquoi ? 
A partir d'un Gegfile => remise des points


Geoloc et openStreeMap en ruby = ROSEMARY
gem rosemary
=> gem pour openstreetmap

http://overpass-turbo.eu/

Talend data LOGICIEL OPEN SOURCE analyse données.

Langage programmation clojure

Toro builder
Geonef

gem pour tester deux types de pages d'accueil a essayer


%y et %Y (prise de début et de fin de chiffre)


Probleme avec postgresql = installer libpq-dev en apt-get

Site qui references les framework javascript pour faire des applications mobiles


Idt Intel sdk

Nb subtilité pour l'installation sous ubuntu = 
utiliser install.sh et ensuite recherche de l'application par le home
motclé = xdk

FAIRE INSCRIPTION PAR L'INTERMEDIAIRE DU LOGICIEL
keitamori@gmail.com
@LordOfWar87

Site ressources interessant
[Source forge HTML5 ressources][181]


Outil de mockup Mockingbird
Kinetic js librairie javascript a creuser et étudier sur openclassroom	

Logiciel Ubuntu SoX qui permet la lecture de fichier mp3

Application pour apprentissage des langues sur le chrome store
language immersion



Modele pour le css 
Topcoat[Topcoat][182]

[Nodejs and rails][183]

## Sublime text - Vintage mode ##

```
Choisir une ligne 
Ctrl + l

Choisir occurence d'un mot
Ctrl + d 
Choisir les occurences une a une
Ctrl + d + d
Choisir toutes les occurences
Alt + F3
Sélectionner tout entre les parenthèses/accolades
Ctrl + Shift + M 
Accès au numero par ligne 
Ctrl + G taper numero de ligne

Package pour Sublime K
Pretty task management
Utilisation 
Ctrl + D // tache terminee - done

test

Normal mode 
ci" //Choisir un texte - choose inner ""
Shift+Ctrl+w // chose a word
c2w //choose two word to edit
v5W // visually choose 5words 
vt, //visually choose to ,
V //choisir 1 ligne
y // yank
p // paste
d // delete
vv //select line
vw // select a word
. //repete la derniere instruction connue


```


Notes blog sur serveur
http://blog.mmlac.com/log-transport-with-apache-kafka/


Sublime config
[Developer poland sublime configuration][183]
[Blog developper][184]


## Rails ##
Passing values to javascript from rails.
[Railscast][185]

Firefox
Aller page précédente ou suivante 
Alt + fleche droite ou gauche

gesgse@gesgqs.com



## INTEL GALILEO - Internet of the things ##

Internet des objets
	Smart like a computer
	Intercation Natural interface only.

Why Intelligent Object 
1. Optimiser l'existant. (réduire les frais, rendre la vie plus facile )
2. Difference sur objet connecté et non connecté ex: Médecin. tension 24h/24 vs tension au repos

Objets extremes dans leurs capacités 
=> Concepts bizarres
=> Non adéquation au besoin

Exemples	 
Nike air + iPod
Parrot Flower power
Nest -google
Google glasses
Sen se
jawbone
Basis science
Smokio
Peeble
Motorola montre

-Où vont les données ? 
=> Question de la propriété. 


Probleme n'est pas tant de coder mais de trouver des idées.
Different cultures de développement 
Electronicien 
Developpeur 
Bricoleur

Intel system Studio
Embedded with windriver vxWorks

Yocto - Os Linux

Security with McAfee

Port JTAG = Vie ou de mort


LANGAGE DE PROGRAMMATION METHODE B

2/3 IDEE ET LE RESTE = côté technique



Notes interressantes =
Le cdn est un serveurs qui donne les liens sur les librairies de javascript les plus courantes. L'idée est de ne plus avoir a les inclure au niveau du header
[Cdn-Librairies javascript][186]


Lien videos sur le jSON a creuser 
http://www.youtube.com/watch?v=6LMVOTfp2SI
http://www.youtube.com/watch?v=9xXr2EZfDPQ
http://www.youtube.com/watch?v=_HmtDTWc3iY
http://www.youtube.com/watch?v=pe6keTE9LbE


jQuery permet une meilleure manipulation du jSON
http://json.parser.online.fr/
Json lint pour vérifier le style du json


Site internet a creuser HTML5 rocks
www.html5rocks.com/en/tutorials
codecombat.com


Gem excon 
=> permet de faire des requêtes HTTP

JSONparse()parse =  cconversion en JSON - Présent en javascript autant qu'en Ruby
```
response = Excon.get(url)
JSON.pase responde.body
```
Zeal pour documentation	

vim FX Plugin firefox pour navigation en mode vim

clipit = Logiciel pour buffer et copy paste
ni.com/labview

Prototypage rapide 

http://tenmiles.com/blog/2012/06/25-ruby-on-rails-gems-for-rapid-prototyping/

http://mattsears.com/articles/2011/12/10/minitest-quick-reference

```
git log -p = commit précédents
```

Existence de webrick reload
code and conquer  jeu pour apprendre a coder

Generation d'un rake personnalisé, exemple tiré d'un railscast

```
namespace :pick do
  desc "Pick a random user as the winner"
  task :winner => :environment do
    puts "Winner: #{pick(User).name}"
  end

  desc "Pick a random product as the prize"
  task :prize => :environment do
    puts "Prize: #{pick(Product).name}"
  end
  
  desc "Pick a random prize and winner"
  task :all => [:prize, :winner]
  
  def pick(model_class)
    model_class.find(:first, :order => 'RAND()')
  end
end
```

## Yannick cours sur le responsive design ##

Cours sur le responsive design

responsive.rga.com
alistapart.com
opquast.com/fr
alsacreations.com
css-tricks.com
openweb.eu
pompage.net
w3c
schema.org
pxtoem


Firefox OS simulator // Simulator de telephone portable
Opera Mobile classic Emulator 
Chrome = Outils pour changer la taille

Manipulation du css directement si temps

HTML5 Possibilité de mettre de la sémantique
Google utilisation des éléments sémantiques

Metatags

Sémantique est à mettre a part
Lancer page dans serveur

Responsive => toujours utiliser des em

	rEm => absolu par rapport a em qui est relatif

Peut pas être responsive et pixels perfect

Opera mini

Composant HTML
Contexte vs Controle pixel

Javascript = une surcouche, penser le site sans javascript

=> utiliser sélénium


Wordwrap => utilisation des césures
Gérer des débordements sur css
Raphael Goetter

bookinity


startiorDev.com

Mode Attilla
Travail élément par éléments
=> revoir les balises puis ce qui est en face


Framework javascript => Beaucoup d'actions de la part de l'utilisateur

html moteur de rendu par
block = ht vers bas
autre = gauche vers droite


why the lucky stiff


Javascript ressources a creuser
http://www.alsacreations.com/astuce/lire/1436-console-javascript.html
http://moox.io/blog/coder-en-javascript-dans-une-console/


```
console.dir(variable);
// Affiche les informations de base sur la variable au niveau des consoles

//Calcul de performance
console.time("test1");
//Instructions javascript
console.timeEnd("test1");

//Tout le code javascript entre ses deux instructions sera evalué au niveau du temps

```

Existence balise Html Autorefresh qui permet de recharger la page

redis 


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
  [87]: http://krampstudio.com/blog/2013/02/26/petite-liste-des-outils-javascript/
  [88]: http://www.w3avenue.com/2009/05/25/list-of-really-useful-javascript-libraries/
  [89]: http://allists.com/awl51g9vpb
  [90]: http://vysakh.quora.com/Making-a-Facebook-clone-using-Rails-in-minimum-time
  [100]: http://www.youtube.com/watch?v=HZkrlX7jJcg
  [101]: http://www.synbioz.com/blog/le_kit_du_bon_developpeur_rails_partie_1 
  [102]: http://www.synbioz.com/blog/le_kit_du_bon_developpeur_rails_partie_2
  [103]: http://www.synbioz.com/blog/creer_son_gem_et_le_publier
  [104]: https://github.com/Benvie/Node.js-Ultra-REPL
  [105]: http://stackoverflow.com/questions/17335329/activemodelforbiddenattributeserror-when-creating-new-user
  [106]: http://www.synbioz.com/blog/l_utilisation_de_vim_2
  [107]: http://webshell.io/
  [109]: http://nodeguide.com/beginner.html#frameworks
  [110]: http://tools.suckless.org/
  [111]: http://www.sitepoint.com/pry-friends-rails/ 
  [112]: http://fr.openclassrooms.com/informatique/cours/un-site-web-dynamique-avec-jquery/stockez-vos-donnees-avec-jstorage
  [113]: http://hugeen.com/2013/09/24/quelques-retours-sur-lutilisation-dangularjs/
  [114]: http://www.atinux.fr/2011/08/28/tutoriel-socket-io-debutant/
  [115]: http://www.atinux.fr/2012/10/20/tutoriel-socket-io-intermediaire/
  [116]: http://stackoverflow.com/questions/1530324/ruby-xml-to-json-converter
  [117]: http://vim.wikia.com/wiki/Moving_lines_up_or_down
  [118]: http://www.blogduwebdesign.com/vim/5-hacks-pour-rendre-votre-utilisation-de-vim-plus-agreable/683
  [119]: http://jasonseifer.com/2010/04/06/rake-tutorial
  [120]: http://docs.rubyrake.org/tutorial/chapter01.html
  [121]: http://www.mickgenie.com/tag/shell-run/
  [122]: http://ph7spot.com/musings/getting-started-with-autotest
  [123]: http://www.codewars.com
  [124]: http://www.danneu.com/posts/15-a-simple-blog-with-sinhttp://www.sitepoint.com/rubyists-time-pry-irb/atra-and-active-record-some-useful-tools/
  [125]: http://asanderson.org/
  [126]: http://www.honeybadger.io/blog/page2
  [127]: http://www.schneems.com/ut-rails/
  [128]: http://www.fleegix.org/articles/2010-03-15-geddy-web-framework-for-node-js
  [129]: http://blog.realstuffforabstractpeople.com/post/43558580442/typescript-definitions-package-manager
  [130]: http://help.rubygems.org/kb/gemcutter/publishing-your-own-rubygem
  [131]: http://rubylearning.com/blog/how-do-i-create-and-publish-my-first-ruby-gem/
  [132]: http://www.danielmiessler.com/study/tcpdump/
  [133]: http://social-stream.dit.upm.es/started/
  [134]: http://yauh.de/articles/376/best-learning-resources-for-meteorjs
  [135]: http://docs.meteor.com/
  [136]: http://www.youtube.com/watch?v=vpp-8gkPWVE
  [137]: http://ace.c9.io/build/kitchen-sink.html
  [138]: http://yauh.de/articles/376/best-learning-resources-for-meteorjs
  [139]: https://hackpad.com/Top-Resources-for-learning-MeteorJS-Nrpnr6CHiGs 
  [140]: http://www.manuel-schoebel.com/blog/iron-router-tutorial
  [141]: https://www.discovermeteor.com/blog
  [142]: http://code.tutsplus.com/articles/24-extremely-useful-ruby-gems-for-web-development--net-23863
  [143]: http://www.codebeerstartups.com/2013/04/must-have-gems-for-development-machine-in-ruby-on-rails/#.UxEzqNuRA5Y
  [144]: http://blog.teamtreehouse.com/10-must-have-ruby-gems
  [145]: http://www.sitepoint.com/rubyists-time-pry-irb/
  [146]: http://www.sitepoint.com/learn-ruby-on-rails-1
  [147]: http://codegeekz.com/javascript-libraries/
  [148]: http://microjs.com/#
  [149]: https://github.com/bebraw/jswiki/wiki/Game-Engines
  [150]: https://www.eventedmind.com/tracks/feed-archive/meteor-make-a-reactive-join-in-the-ui
  [151]: https://github.com/bebraw/jswiki/wiki/Game-Engines
  [152]: http://muffinlabs.com/content/chatterbot-ruby-library-twitter-bots/
  [153]: http://muffinlabs.com/chatterbot.html
  [154]: http://sebastiandahlgren.se/2013/07/20/add-routing-to-meteor-js/
  [155]: https://developer.mozilla.org/en-US/learn/javascript
  [156]: http://coding.smashingmagazine.com/2013/11/07/an-in-depth-introduction-to-ember-js/
  [157]: http://www.railsonmaui.com/blog/2013/06/11/emberjs-rails4-tutorial/
  [158]: http://www.devmynd.com/blog/2013-3-rails-ember-js
  [159]: http://hashrocket.com/blog/posts/setting-up-an-ember-app-with-a-rails-backend
  [160]: http://blog.dcxn.com/2013/03/23/getting-started-with-ember-js-on-rails/
  [161]: http://collectiveidea.com/blog/archives/2013/06/13/building-awesome-rails-apis-part-1/
  [162]: http://devblog.avdi.org/2013/06/21/a-list-of-programming-screencast-series/
  [163]: http://www.opinionatedprogrammer.com/2011/02/capybara-and-selenium-with-rspec-and-rails-3/
  [164]: http://lostechies.com/ryanrauh/2013/10/08/emberjs-beyond-the-tutorials/
  [165]: http://www.infoq.com/fr/articles/emberjs
  [166]: https://www.openshift.com/blogs/day-19-ember-the-missing-emberjs-tutorial
  [167]: http://www.toptal.com/javascript/a-step-by-step-guide-to-building-your-first-ember-js-app
  [168]: http://elweb.co/want-to-learn-ember-js-start-here/
  [169]: http://www.williamhart.info/an-emberjs-beginners-tutorial.html
  [170]: https://tutsplus.com/course/improve-workflow-in-sublime-text-2/
  [180]: http://www.webdesignerdepot.com/2012/11/10-javascript-frameworks-to-improve-your-mobile-development/
  [181]: http://html5center.sourceforge.net/blogs/Installing-the-Intel-XDK-on-Linux
  [182]: http://topcoat.io/
  [183]: http://www.perfectline.co/blog/2011/02/optimizing-ruby-on-rails-application-with-nodejs/
  [183]: http://idered.pl/archive/my-sublime-text-setup
  [184]: http://blog.alexmaccaw.com/sublime-text
  [185]: http://railscasts.com/episodes/324-passing-data-to-javascript?view=asciicast
  [186]: http://cdnjs.com/
