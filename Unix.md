Filtrer un processus

```
ps -aux | grep firefox

```

Astuce Unix pour trouver des elements précis 
```
/*mot_a_trouver*/
```

## Linux - shell ##

at [heure minutes ...]
>Instructions
>Ctrl + D

Crontab 

```
crontab -l
crontab -e 
crontab -r

```

Grep 

```
//Utilisation du grep
$ grep ’197.$’ fichier.dat
Jimi Hendrix 1970
Jim Morrison 1971
$
 $ grep ’^Ji’ fichier.dat
Jimi Hendrix 1970
Jim Morrison 1971
$
$ grep ’^J.*1970’ fichier.dat
Jimi Hendrix 1970
$
$ grep -E ’Jimi?’ fichier.dat
Jimi Hendrix 1970
Jim Morrison 1971
$
$ grep -i jimi fichier.dat
Jimi Hendrix 1970
$

```

Nb pour faire le set up d'une variable d'environnement.<br>
```
echo 'export CHROME_BIN="/usr/bin/chromium-browser"' >> ~/.bashrc && source ~/.bashrc

```

Travail sur le shell et l'execution de scripts shell permet d'accélerer le processus de développement.
Rappel sur le shell

```
basehtml='Bonjour le monde'

echo " $basehtml"

```

Changer le mode du fichier par chmod +x exemple.sh

Execution du fichier par ./exemple.sh

Création de dossier parenté.

```
mkdir -p app/views
```

#### VI commands in your shell

```
set -o vi
```

##  Grep and filtres

cat pour concaténation

wc = word count + number of lines

split -l 2 file2

cat *x affichage d'un tout




Recherche et grep de fichier

```

find --name "*android*"

grep ri dependencies

```

Ultimate installation from Okhin

```
#!/bin/sh
 
apt-get install -y tmux zsh python3 git build-essential htop iotop saidar iftop lolcat grc moc ncmpcpp \
 sysv-rc-conf ncurses-term locate dcfldd nmap tree netcat acpitool bastet apt-file ntpdate libssl-dev python3-pip\
 python-virtualenv virtualenvwrapper mosh ffmpeg2theora pastebinit curl tsocks libncurses5-dev nmap 

```

Trucs et astuces en linux (interessant)

[Tech bar ](http://www.techbar.me/linux-shell-tips/)

[Linux mag astuces](http://www.linuxjournal.com/article/7385)

[Linux academy](https://linuxacademy.com/blog/linux/tutorial-the-best-tips-tricks-for-bash-explained/)

`̀ `
mv nomfichier (,{.conf})

```

Commande Watch pour avoir des informations

```
watch -d ip r 
watch -d ip a  s wlan0
watch -d ip n 

```

Existence de mrt pour les recherches et watch

OLPC pc couleur verte 100$

Searxks meta moteur en python 

m.al-f.net

mtr-tiny

tanenbaum les réseaux

Tink - Utilisation d'un VPN 

Note-X - batterie portable vente sur paris 

[Note-x](http://www.note-x.com/index.php)

Pour connexion à un serveur 

```
ssh remote_user@adresse_ip

```

Outil pour le transfert de fichier. Utilisation possible de Samba mais aussi d'outils tiers tels que scp 

[University of indiana knowledge base](https://kb.iu.edu/d/agye)

[Blog guillerm Garon](http://www.garron.me/en/articles/scp.html)

[Linux Academy](https://linuxacademy.com/blog/linux/ssh-and-scp-howto-tips-tricks/)

[Faq Forge](http://www.faqforge.com/linux/how-to-copy-files-with-scp-between-linux-servers/)

sudo fdisk -l => liste des medias connectés
sudo apt-cache search | less 

nb mori difference
sudo apt-get update
sudo apt-get upgrade


Prise de notes d'un livre sur unix 
Script Shell Entrainez vous a programmer sous Unix, Linux  Jean Marc Baranger Theo Schomaker

Commandes importantes
tee
du (disk usage)
df (disk file)
find 
locate (deux commandes précédentes pour trouver ses fichiers)

alias 
history 

Nb possibilité de créer plusieurs dossier à la suite

```

mkdir  -p bonjour/{mori,benoit,mohammed}

```

Variables d'environnement obligatoires en Unix
PATH
PS1
PS2
PWD
HOME
LOGNAME
TERM
TMOUT

Options du shell
set -o 

possibilité de les aciver en usant de set -o option ou set +o option

Creation alias et suppression alias
alias nomAlias=""
unalias nomAlias

Possibilité d'associer commandes et alias a des combinaisons de touches

alias nomAlias= Ctrl+p

Les test en bash s'effectuent par l'intermédiaire de la commande test 

Syntaxe

test [[condition][option]]

Faire de l'arithmétique en Unix on use de expr

possibilité d'user des doubles paranthèses en unix pour faire du bash

mettre des infos de debug au niveau du shell utilisation de set 

set -x ou set +x a l'intérieur du script ou exterieur du script de cette manières

```

$ksh -x affiche.sh

```

existence de la commande pr


Site internet d'un codeur avec des références nombreuses au C et à VIm 

[Site internet Derek Wyatt](http://derekwyatt.org/vim/tutorials/intermediate/#vimrc)

Possibilité avec le shell de faire des commandes plus evolués tel que 

pv (pipeviewer)

nc (netcat)

Sachant que l'on peut faire tourner un serveur avec netcat
[Tutorial to try](http://www.catonmat.net/blog/unix-utilities-netcat/)
