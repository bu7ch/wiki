#Fonctionnement en Kata

## CHAPITRE UN ##

<h1>kata 1</h1>

###

#### 0-
>Terminal 

<code>
rvm install 1.9.2
</code>
#### 0-
<code>
gem install rails -v 3.1.0
</code>
#### 0-
<code>
rails new things_i_bought
</code>
#### 0
<code>
bundle install 
rails server
</code>
#### 0
Lancer firefox à l'adresse  "localhost:3000"
Vous devez voir page par défaut de rails
#### 0
<code>
rails generata scaffold purchase name:string cost:float
</code>
#### 0
Verifier existence d'une fichier de migration à
> db/migrate/[date]_create_purchases.rb
Verifier les fonctions sont bien installés

#### 0
<code>
rake db:migrate
</code>

#### 0

Verifier le code a 
>app/models/purchase.rb

Procéder à sa modification

<code>
class Purchase < ActiveRecord::Base
	validates_presence_of :name
	validates_numericality_of :cost, :greater_than => 0
end
</code>


### FIN


