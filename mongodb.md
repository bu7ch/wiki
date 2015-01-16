Mongo db 

Tutoriel de référence pour cette documentation

[TutsPlus](http://code.tutsplus.com/tutorials/getting-started-with-mongodb-part-1--net-22879)

Création d'une base de donnée à la volée.
Taper mongo au niveau du shell

Pour trouver un élément qui correspond

```
db.nomDB.find({gender:'M'}); // va trouver tous les éléments ayant un gender == 'M'

//Recherche multiple

db.nettuts.find({gender: 'm', $or: [{nationality: 'english'}, {nationality: 'american'}]});

//Updater un élément de la base
db.nettuts.update({first: 'james', last: 'caan'}, {$set: {hair_colour: 'brown'}}); // Premiere partie sert à trouver l'élément tandis que le set permet de le modifier
```

Autre article intéressant sur mongoDb du blog Xebia

[Xebia blog post MongoDb](http://blog.xebia.fr/2010/12/15/mongodb-en-pratique/)
