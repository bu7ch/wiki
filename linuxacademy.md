1991 Creation de linux par Linus Torvalds - Idee principale était  dd'avoir un systeme pour lui.

Envoi de ses opérations sur usenet

Utilisation de gcc. Base sur un Kernel simple. Idee Free

Linux licencing - Restrict commercial use.

Licence Gnu => tout ce qui est fait dessus devient Free, nb faire recherche sur les licences (questions de droit)

Copyright different de copyleft.

Pourquoi le pingouin de jeux de mots

Key milestonee

1991 - Base

## Distributions

'One of many member of a larger set of nix like O.S'

Desktop, server, media, scientific, recovery

Organisation of distributions

Manuals

Linux kernel - Free applications - proprietary applications

Manuals and supports maybe paid

Packages are services, libraries or applications complied into a format that can easily distribued and installed

1.yUM
2.RPM
3.Aptitude
4.DEB


[Linux officials](http://www.linux.com)

Plus de 160 distributions

## LINUX SERVER vs Desktop

Desktop = Have a Gui refer to personnal computer

Server = freely LAMP stack Mysql and php. 65% of server publicy and 95% of supercomputer

LAMP stack 

Web server optimized

LDAP User management

Firewall

Proxy server

DNS Server


## Top thing to do after installation

Utility commonly use

1.ubuntu-restricted-extra
2.vlc
3.pidgin
4.chromium
5.Steam


#LINUX DEEP

## Create - Destruct users

useradd pinehead //create a user

passwd pinehead //create a password

etc/sudoers = fichier de modif des personnes ayant des privilèges sudo

usermod -G wheel pinehead // Changement du group utilisateur

groups pinehead // Voir les appartenances au groupe

w //tous les users connectes au systeme

userdel // effacement d'utilisateur


## Vim supplements

%s/chercher/remplacer  =  recherche avec remplacement dans tout le fichier

Ne pas oublier /etc = fichier configuration

/var = dossier dans lequel les fichiers changent enormément



## Options supplémentaires

LESS touche f(forward) B(backward) ? permet de faire la recherche du bas vers le haut


## CRONTAB

Scheduling task

crontab -e // edit scheduling task

crontab -l /:list element

Existence de cron.daily, cron.hourly ... pour faire des taches sur des temps précis


## TOP

Travail sur les process - monitering and manage system resources

Ctrl+N et Shift+N = classement des processus

SHIFT +n

Change priority

r pour renice et entree du Pid avec PId et utilisation du nombre. -20 est le plus elevé


## Architecture

/var contient les infos principales du systemes exemple

/var/log = contient les informations boot run du systeme -> on est dans le systeme

/var/cache gestion

/var/lib => librairie du programme

/sys/ => informations sur le matériel

/sys/devices

/sys/kernel => information kernel

/proc/ => nb dans le fichier est une suite de nombre dont chacun = info sur les processus


### Guide de survie en vim

[Guide de survie en vim](http://www.linux-france.org/prj/support/outils/vi.html)

## SHELL

Commande exec

Ctrl+R = recherche dans le bash

Ctrl+S = recherche forward

Ctrl+X = recherche et modification

Ctrl +K = recherche et modification en avant
