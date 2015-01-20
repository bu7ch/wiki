Twisted - librairie Python pour faire de l'asynchrone


##BOUCLES 

Les boucles généralement sont des for .. in  qui existent aussi en javascript et en ruby.
exception faite de énumerate.

```
choices = ['pizza', 'pasta', 'salad', 'nachos']

print 'Your choices are:'
for index, item in enumerate(choices):
    index += 1
    print index , item

# Nous aurons ainsi une variable index qui sera index de notre tableau.

```

Nous avons aussi zip - fonction qui permet le parcours de deux tableaux à la fois:

```
list_a = [3, 9, 17, 15, 19]
list_b = [2, 4, 8, 10, 30, 40, 50, 60, 70, 80, 90]

for a, b in zip(list_a, list_b):
    # Add your code here!
    if a > b: 
        print a 
    else:
        print b

```
La méthode .items() permet d'avoir les élémnents composant un dictionnaire
Méthode .keys() pour avoir les clés
Méthode .values() pour avoir les valeurs

in permet de voir des informations sur les mots

```

#examples de for .. in 

for number in range(5):
    print number,

d = { "name": "Eric", "age": 26 }
for key in d:
    print key, d[key],

for letter in "Eric":
    print letter,  # note the comma!


```

[Oreilly ressources](http://programming.oreilly.com/2013/04/twisted-python-the-engine-of-your-internet.html)

[Stack overflow informations](http://twistedmatrix.com/documents/12.3.0/core/examples/)

[pyenv installation](http://davebehnke.com/python-pyenv-ubuntu.html)

[Notes sur le python](http://jcalderone.livejournal.com/tag/sixty%20seconds)

[Python.org twisted ressources](https://wiki.python.org/moin/Twisted-Examples)

[Stack overflow question et ressources](http://stackoverflow.com/questions/1888139/python-twisted-where-to-start)

[Krondo](http://krondo.com/?p=1209)

