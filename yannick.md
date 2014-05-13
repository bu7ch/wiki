# Test après implémentation

Utilisation de Selenium IDE pour faire du test d'acceptance



Dans sqlite3 possibilité de faire des requêtes en ligne de commandes de manière directe. 
```
$ sqlite development/db "select * from users"

```

Test d'acceptance 

Utilisation des outils Sélénium et/ou CasperJS


Différences fixtures et seed.

Fixtures =  jeu de données bidon pour le test
Seed = jeu de données pour le developpement et potentiellement production

Utilisation de frabiques pour créer des données à la volée.

Idée est de se sentir bien dans le code que l'on fait.

```
grep ri pseudo test/developpement
grep "test" .
```

```
bundle show gem //affiche le dossier d'installation de la gem
```

Vim copier une ligne 

yt$

```
git add -p // Option patch
```

YAF

Aller plus lentement


# Workflow

Trois branche de travail

Branches à faire

1.Demo
2.Dev
3.Production

Eviter au mieux les git rebase

Trois serveurs pour le travail de l'application

Commiter le README

Utiliser les Gist pour faire des stocks de code prêt à l'utilisation.

Démarrage d'un serveur sur son ordinateur.

```
git add -p //options patch

git commit --amend // Ajout des autres fichiers modifié

bdelete // Effacer le buffer

```

Ctrl+Alt droite gauche => Utilisation des bureaux pour organiser son travail

Raccourcir les boucles de feedback, deux branches demo et production => livrer le plus vite possible.

Bitbucket 


dotenv => Attention aux variables environnements

```

gem 'dotenv'

require 'dotenv'

Dotenv.load

user = ENV[USER_NAME]


config:set KEY // config:set REMI_PASSWORD=postantRack


Chapeau pour faire Tabulation Vim
```

[CSS font stack](http://cssfontstack.com/) Css et ensemble

Pas plus de 2,3 fontes par pages,
Sérif plus sympa à lire

[CSS tricks](http://css-tricks.com/), faire des listes pour au cas ou une est absente

Utilisation de font-family, par défaut utiliser Sérif

```
apt-cache search paquet

```

Text to speech gem

```
gem 'speechtotext'

```
Pocket sphinx  => logiciel linux pour synthèse vocale

