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


