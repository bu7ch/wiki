## RUBY ##
----

 

L’apprentissage du ruby s’est fait par plusieurs ressources
 
 - [RubyMonk](http://rubymonk.com)
 - [CodeAcademy](http://codeacademy.com)



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

``
precision: 8
scale: 2
``


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
Les hash sont des collections de données de manière non ordonnée, dont chacun des éléments est accessible par un indice.
Les Hash sont à différencier des structures de tableaux. Ils sont fixes et on une syntaxe particulère.

```
Hash
person = { :first_name => 'Brian', :last_name => 'Lobster' ,  :age => 44}
person2 = {fist_name: 'Brisco', last_name: 'Final', age: 44}

```
L'accès aux paramètres des hash se fait de la manière suivante:

```
puts person
puts person[:first_name]
puts person.[] = ("first_name")
person2[:last_name] = 'Moloch'

```


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


Avance Creation et destruction d'objets

[Classes avancées en ruby](http://pleac.sourceforge.net/pleac_ruby/classesetc.html)

Métaprogrammation en Ruby 
[Metaprogramming in ruby exercices](http://ruby-metaprogramming.rubylearning.com/)

## METAPROGRAMMATION

Tout en Ruby est en objet y compris la classe elle même. 
Ainsi quelques point sont a prendre en compte 

La classe suprème en Ruby est ainsi le basic object

Le polymorphisme est inclus en ruby. Le polymorphisme peut s'appliquer au niveau des classes.

Faire la différenciation entre méthodes d'instances, variables d'instances et classes.

Les noms de classes et autres sont des constantes, qui servent d'espaces de noms à Ruby.

```
"hello".class # renvoie String
String.class # renvoie Class
String.instance_methods
```

Possibilité de faire des splat
```
[1,2,3] = 1, *2 # renvoie 1=[1], 2* = [2,3]

```

Travail sur le benchmark 
Rappel fichier bench_calcul.rb
Dans le fichier inclure require 'benchmark'

### RECURSION

```
def test(nombre)
  return 0 if nombre == 0
  test(nombre -1)
end

```

```

Gestion exeptions article

[phrogz - Gestion exeption Ruby](http://phrogz.net/programmingruby/tut_exceptions.html)

[Execption raising](http://rubylearning.com/satishtalim/ruby_exceptions.html)

Gestion des execptions - a creuser par le ruby bastard book

[Ruby bastard book execption handling](http://ruby.bastardsbook.com/chapters/exception-handling/)


Gem pour la genération d'un site en statique 

gem middleman

gem emoji => création de d'émojis

Gestion des regexp site internet

[Regexp - Tutorials pionts](http://www.tutorialspoint.com/ruby/ruby_regular_expressions.htm)

## GESTION DES EXCEPTIONS

```
class KasayaError < StandardError
end

def robe(type)
  ke = KasayaError.new
  begin
    raise ke if type.class != String && type != "Kasaya"
    rescue TypeError => error
      p error.message
    end
  return "Dharmaguptaka's Kasaya Robe"
end

```


Nb un site très utile en ce qui concerne les test et assertions en Ruby 

[MattSears](http://mattsears.com/articles/2011/12/10/minitest-quick-reference)


### PARSING XML ET JSON EN RUBY 

```
require "rexml/document"

file = File.open("pets.txt")
doc = REXML::Document.new file
file.close

doc.elements.each("pets/pet/name") do |element|
  puts element
end
```

```
require 'json'

pets = File.open("pets.txt", "r")

doc = ""
pets.each do |line|
  doc << line
end
pets.close

puts JSON.parse(doc)
```

Possibilité de & en ruby -> transmission de paramètres

gem awesome_print pour l'affichage meilleur des infos
require ap 

[Ruby reloaded](http://rubyreloaded.com/trickshots/)

LIbrary Fiddle pour tout ce qui est d'intégration du c ou ffy

Ripper pour faire evaluation de code

upto()

Ruby expression


RUBY CODE TRICK

```
names= %{fred jones mark}
age =[12,20,54]

name.zip(age)
Hash[name.zip(age)]

```

Possibilite de faire des if suivis en ruby

```

Range in array

[*10..20]

```

```

require 'json'

j hash_variable
jj hash_variables

```

Methods informations
```

p __method__
p __callee__

```

Convention d'écriture et passage par référence

`̀ `
puts "this is a test".scan(/\w+/).map(&:upcase)
                                 .map(&:reverse)
                                 .to_s
```

_ permet dans l'irb d'avoir la dernière valeur

Existence en ruby de parametre pour les proc

```

a = 5 
a -> {}
a.source_location

#Existence de prepend
a = 'world'
a.prepend('hello')

#Fin d'un fichier source ruby

__END__

DATA.read
DATA.rewind

regexp trick

/(?<a>\w+)(?<b>\w+)/ =~ str
```

Possibilité de faire des closures et l'utilisation du & pour faire des références.
Voiçi quelques trucs

```
array.each(&method(:foo))
// equivaut à 
array.each{|element| foo(element)}

// Autre exemple 1
["1", "2", "3"].map{ |string| string.to_i }
=> [1, 2, 3]
["1", "2", "3"].map(&:to_i)
=> [1, 2, 3]

//autre exemple 2 avec X comme element
# when you want to pass an argument to a method
[10, 11, 12].map(&X.to_s(16))
=> ["a", "b", "c"]

# when you want to parse some JSON
owners = [{'name' => 'Fred', 'dog' => 'Fido'},
          {'name' => 'Ron', 'dog' => 'Rex'}];
owners.map(&X['name'])
=> ["Fred", "Ron"]


Existence dans les array de la propriété reject

a = [1,2,3,4,5,6,7,8]
a.reject{|e| e > 5}

```
Les exemples utilisent la gem ampex
Existence de ruby underscore avec les mêmes qualités

[Ruby underscore](https://github.com/danielribeiro/RubyUnderscore)

References
[conrad Irwin](http://cirw.in/blog/ampex)

Ruby weekly 

Application open source
gitlab 
discourse

Différences Ruby avancées


Différences entre require et load!

load peut faire du chargement multiple - actualisation ainsi du code dès qu'il est modifié

Programme CGI 

```
ruby -rdebug nom_programme.rb # debugger
Utilisation de step pour passer au suivant

```

Erb est aussi une commande

```
$ erb erbdemo.rb

```

Méthodes utiles en ruby 

```
# Méthodes utiles en ruby

respond_to?(ARG) #Verifie que l'argument est bien implanté dans l'objet dans lequel la méthode est appellée
object_id        #Indique l'id unique de l'objet
send             #

```

respond_to? est une méthode d'introspection et de réflexion -> examen de l'état d'un programme pendant son éxecution.

####Setter en ruby ancienne mode

```

Class Stupid
   def prix=(x)
     puts "le prix est #{x}"
   end
end

s = Stupide.new
s.prix = 5

Différences entre require et load!

load peut faire du chargement multiple - actualisation ainsi du code dès qu'il est modifié

Programme CGI 

```

En ruby les classes sont également des objets on peut ainsi avoir des structures sympatiques
Exemple simple

```

def Billet.plusonéreux(*billets)
   billets.sort_by {|t| t.prix }.last
end

``̀`
C'est une méthode de classe
Méthode qui s'applique à l'ensemble des objets et non un objet en particulier


Nb pour rajouter des options à une méthodes alors passer par un hash est une meilleure solution.

Lever des exceptions et warnings en ligne de commandes

```
ruby -cw test.rb

```

###Gestion des exceptions

```
# Mettre le code à risque dans un bloc begin rescue end - Possibilité de préciser les exception

def reraise(nomFichier)
  begin
    fichier_handle = Fichier.new(nomFichier)
  rescue Errno::ENOENT => e
    puts "Erreur"
    raise e
  end 
end

```

Utilisation aussi de la syntaxe alternative

``̀`

raise ArgumentError, "Il me faut un chiffre inférieur à 10"
unless x<10

```

###Surdéfinition d'opérateurs

```

#def %(x) travaille sur obj%x
#def []=(x,y) travaille sur obj[x]=y

```
NB possibilité d'avoir des infors en mode pry
```

obj.public_methods
obj.instance_methods(false).sort

```

Possibilité en Ruby de lancer des Process - C'est une commande particulière - exemple de code.<br>
Exemple en sinatra tiré de stackOverflow<br>

```
get '/start_process'
  @@pid = Process.spawn('external_command_to_run')
end
```

Existence de webmock pour gérer les test en requêtes http

Pour la manipulation de fichier Ruby possède quelques methodes qu'il est indispensable de connaître

```

File.join # Joindre des fichier
File.expand_path # Trouve le chemin relatif 
File.dirname # Nom du dossier courant
__FILE__ #Constante pour la gestion des fichier
"./fichier.rb" #Peut renvoyer au dossier précédent

```

Existence en Ruby de ObjectSpace qui permet grace à des routines d'acceder à l'objet en mémoire.

cd [ObjectSpace Ruby](http://ruby-doc.org//core-2.2.0/ObjectSpace.html)

Nb la hierarchie des classes en ruby

class herite de module

Orientation de l'heritage des classes en ruby

Object -> BasicObject 

Existence de Artoo = framework ruby pour ce qui concerne la robotique

Something which seems to be khanacademy
[Leaf academy](http://www.gotealeaf.com/books)
