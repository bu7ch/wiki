#Fonctionnement en Kata

## CHAPITRE UN ##


### KATA DEBUT Rails Scaffolding

#### 01
>Terminal 

<code>
rvm install 1.9.2
</code>
#### 02-
<code>
gem install rails -v 3.1.0
</code>
#### 03-
<code>
rails new things_i_bought
</code>
#### 04
<code>
bundle install 
rails server
</code>
#### 05
Lancer firefox à l'adresse  "localhost:3000"
Vous devez voir page par défaut de rails
#### 06
<code>
rails generata scaffold purchase name:string cost:float
</code>
#### 07
Verifier existence d'une fichier de migration à

> db/migrate/[date]_create_purchases.rb

Verifier les fonctions sont bien installés

#### 08
<code>
rake db:migrate
</code>

#### 09

Verifier le code a 
>app/models/purchase.rb

Procéder à sa modification

<code>
class Purchase < ActiveRecord::Base
	validates_presence_of :name
	validates_numericality_of :cost, :greater_than => 0
end
</code>


### FIN KATA

## CHAPITRE DEUX ##

### DEBUT KATA Rails Save your bacon -Test Unit 

#### 0
Créer un dossier
<code>
mkdir example
</code>

#### 0
Entrer dans dossier ; Créer un fichier example_test.rb
<code>
cd example
touch example_test.rb
</code>

#### 0
Coder

>example/example_test.rb

<code>
require 'test/unit'

class ExampleTest < Test::Unit::TestCase
	def test_truth
		assert true
	end
end

</code>

#### 0
Runner le test

<code>
ruby example_test.rb
</code>

### FIN KATA Rails Save your bacon -Test Unit

### DEBUT KATA Rails Save your bacon -Rspec

#### 0
Créer un dossier work ; Aller a l'intérieur du dossier ; Créer un dossier spec ; Installer la gem 

<code>
mkdir work
cd work 
mkdir spec
gem install rspec
</code>

#### 0
Aller a l'intérieur du dossier spec ; Créer un fichier spec_helper.rb ; Créer un fichier book_spec.rb

<code>
cd spec
touch spec_helper.rb book_spec.rb
</code>

#### 0
Coder 

>spec/spec_helper.rb

<code>
require_relative "../book"
</code>

>spec/book_spec.rb

<code>
require_relative '../book.rb'

describe Book do

end
</code>

#### 0
Retour dans le fichier arriere ; Coder book.rb

<code>
cd .. 
</code>

>work/book.rb

<code>
class Book

end
</code>

#### 0
Lancer rspec

<code>
rspec spec
</code>

### FIN KATA Rails Save your bacon -Rspec

### DEBUT KATA Rails Save your bacon -Cucumber

#### 0
Installation gem cucumber

<code>
gem install cucumber
</code>

#### 0
Création du dossier account ; création du dossier account/features ; création du fichier account.feature dans account/features;

<code>
mkdir accounts; mkdir accounts/features ; touch accounts/features/account.features
</code>


#### 0
Coder 

>accounts/features/account.feature

<code>
Feature: My Account
	In order to manage my account
	As a money minder
	I want to ensure my money doesn't get lost

	Scenario: Taking out money
		Given I have an account
		And it has a balance of 100
		When I take out 10
		Then my balance should be 90

</code>

#### 0

Retourner en arrière ; Lancer cucumber features

<code>
cd ..
cucumber features
</code>

#### 0

Copier le messages pour le pending ; 
Créer dossier step_definitions
Créer le fichier features/step_definitions/account_steps.rb


#### 0

Créer le dossier lib à partir de la racine de accounts
créer un fichier account.rb

#### 0
Coder dans account.rb 

<code>
class Account
end
</code>

#### 0
Coder dans step_definitions le code copié de cucumber features à  savoir.
<code>

</code>

#### 0

Créer un dossier features/support/env.rb;
coder 

<code>
$LOAD_PATH << File.expand_path('../../../lib', __FILE__)
require 'account'
</code>


###FIN KATA Rails Save your bacon -Cucumber


## CHAPITRE 3

### Kata developing a real rais app

#### 0
<code>
rvm use 1.9.3
gem install rails
</code>

#### 0
<code>
rails new ticketee
</code>


#### 0
Entrer dans l'application 
 
#### 0

 Coder le Gemfile

<code>

	source 'http://rubygems.org'
gem 'rails', '3.1.0'
gem 'sqlite3'
group
gem
gem
gem
end
:assets do
'sass-rails', " ~> 3.1.0"
'coffee-rails', "~> 3.1.0"
'uglifier'
gem 'jquery-rails'
group :test do
# Pretty printed test output
gem 'turn', :require => false
end


</code>

#### 0
Ajouter dans le Gemfile

<code>
gem 'cucumber-rails'
gem 'rspec-rails'
</code>

#### 0
Installer le profil des gems

<code>

group :test do 	
rails g cucumber:install
rails g rspec:install
end
</code>

## Kata sur la création de gems

#### 0
Créer un dossier gem_perso ; 
Entrer dans ce dossier 

#### 0
Lancer la commande 
rvm use 2.0.0

#### 0
Creer la configuration pour la creation de la gem 
bundle gem <nomDeGem>

#### 0
Créer le Gemfile pour édition de la gem
bundle init




###KATA rails begin

$ rails new blog

$ cd blog

$ rails generate model Article

$ rake db:create

$ rake db:migrate


$ rails g scaffold Article title:string body:text published_at:datetime --skip-migration

$ rails s

Ajout d'un champ supplémentaire

$ rails generate migration add_excerpt_and_location_to_articles
excerpt:string location:string

Coder 

db/migrate/

class AddExcerptAndLocationToArticles < ActiveRecord::Migration
	def change
		add_column :articles, :excerpt, :string
		add_column :articles, :location, :string
	end
end


Coder dans la vue app/views/article/_forms.html.erb


Ajouter des validations
coder

class Article < ActiveRecord::Base
	validates_presence_of :title, :body
end


$ rake db:migrate



Possibilité de faire du graphviz avec la gem ruby-graphviz
Kata sur la création blog 15minutes
http://www.reinteractive.net/posts/32-ruby-on-rails-3-2-blog-in-15-minutes-step-by-step
http://12devs.co.uk/articles/writing-a-web-application-with-ruby-on-rails/
http://code.tutsplus.com/tutorials/zero-to-sixty-creating-and-deploying-a-rails-app-in-under-an-hour--net-8252
http://www.webmonkey.com/2010/02/ruby_on_rails_for_beginners/
http://www.codelearn.org/ruby-on-rails-tutorial
http://guides.railsgirls.com/devise/
http://www.softwaredeveloper.com/features/best-ruby-on-rails-061307/
http://pothibo.com/2013/07/responsive-javascript-in-rails/
http://guides.railsgirls.com/app/
https://gitorious.org/rails-app-examples
https://devblog.toopher.com/2013/11/19/toopher-on-rails-example/
http://railsgirlsberlin.de/apptutorial/
http://www.sean.co.uk/a/webdesign/javascript_gamelib/javascript_gamelib.shtm
http://blog.artenet.fr/2011/09/16/javascript-les-frameworks-de-jeux-videos/
