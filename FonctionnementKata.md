#Fonctionnement en Kata

## CHAPITRE UN ##

<h1>kata 1</h1>

### 01-
<code>
rvm install 1.9.2
</code>
### 02-
<code>
rails new things_i_bought
</code>
### 03
<code>
bundle install 
rails server
</code>
### 04
Lancer firefox à l'adresse  "localhost:3000"
Vous devez voir page par défaut de rails
### 05
<code>
rails generata scaffold purchase name:string cost:float
</code>
### 06
Verifier existence d'une fichier de migration à
> db/migrate/[date]_create_purchases.rb
Verifier les fonctions sont bien installés

### 07
<code>
rake db:migrate
</code>