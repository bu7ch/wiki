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

[TutorielSurGitFlow](http://yakiloo.com/getting-started-git-flow/)

[TutorielInteressant sur le gitFlow](http://labs.grupow.com/blog/2011/07/05/getting-started-with-git-flow)

[ATLASSIAN GIT Tutoriel](https://www.atlassian.com/fr/git/workflows#!workflow-gitflow)

Autres commandes destinées dans git.

```
git diff --cached // Affichage des differences en lignes
```

Indiquer parfois la commande pour le commit exemple
```
git commit -m "$rails g controller welcome"
```
Faire des commits selectionnés

```
--patch
```

Commande git a revoir 

```
git checkout -f 'Sha1 ou tag'
```

Force le retour a une modification locale
NB Dans un commit possibilité de faire plusieurs saut à la ligne.

```
git instaweb
git flow
```
Git instaweb affiche les informations des commits sur un navigateur
Git flow permet de faire la gestion des commits
Tutoriel git flow [GIt flow tutorial](http://danielkummer.github.io/git-flow-cheatsheet/)

La possibilité de faire des pages projets dans github.

[Créer des pages projets manuellement](https://help.github.com/articles/creating-project-pages-manually)

Nouvelle fonctionnalité apprise

```
git checkout --orphan gh-pages
git rm -rf
```
Création de branche orphelines (sans lien avec d'autres branche)
Suppression en git

Astuces cool en git et github

[Timgreen github cool features](https://github.com/tiimgreen/github-cheat-sheet)