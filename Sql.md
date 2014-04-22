## SQL ##
```
USE movie1_db

SELECT * FROM movies WHERE year >=2009
SELECT * FROM movies WHERE year BETWEEN 1999 AND 2004
SELECT name FROM actors WHERE name LIKE "%Tom%"
SELECT * FROM movies ORDER BY year ASC, title DESC // peut être mis en DESC


SELECT * FROM movies LIMIT 10 OFFSET 20

//SQL statement which we can create database
CREATE SCHEMA movie_db

CREATE SCHEMA IF NOT EXISTS movie_db
CREATE DATABASE IF NOT EXISTS movie2_db

//SQL statement that's allow database structure
CREATE TABLE actors(name VARCHAR(50))

//Creation d'engines
CREATE TABLE actors(name VARCHAR(50)) ENGINE InnoDb


//CREATE
//Inserer de l'information

INSERT INTO movies (title,year) VALUES ("Aliens",1986);
//Syntaxe alternative
INSERT INTO movies  SET title="Back to future", year=1985;

//UPDATE
SET SQL_SAFE_UPDATES = 0; //eviter les réecritures
UPDATE movies SET year="1985" WHERE title="Avatar 2";

//DELETE
DELETE FROM movies WHERE title="Avatar reloaded" AND year=2016;
SQL_SAFE_UPDATES=1;

//RENAME TABLE
RENAME TABLE movies TO movie_table

//DROP TABLE
DROP TABLE actors

//TRUNCATE 
TRUNCATE actors

//MODIFY COLUMN SCHEMA
//ADD COLUMNS
ALTER TABLE movies ADD genre VARCHAR(25);

//CHANGE COLUMNS
ALTER TABLE movies CHANGE COLUMN year release_year YEAR ;

//REMOVE COLUMN
ALTER TABLE actors DROP place_of_birth


//REMOVE DATABASE
DROP DATABASE movie_db3
//safer
DROP DATABASE IF EXISTS movie_db3
```
Normalization

Type of keys
Primary keys
Unique keys
Foreign keys



```
//primary KEY
CREATE TABLE t_genres (pk_id INTEGER NOT NULL AUTO_INCREMENT PRIMARY KEY , uk_name VARCHAR(4
5) NOT NULL UNIQUE);

//alter key
ALTER TABLE t_movies ADD pk_id INTEGER AUTO_INCREMENT PRIMARY KEY FIRST ;

//alter a foreign key - a creuser
ALTER TABLE t_movies ADD fk_genre_id INTEGER NULL, ADD CONSTRAINT  FOREIGN KEY (t_genres) REFERENCES t_genres(pk_id)

```

Modification 
JOindre des tables 

```
//INNER JOIN
> SELECT * FROM movies INNER JOIN genres ON movies.genre_id = genres.id

//OUTER JOIN LEFT
SELECT * FROM movies LEFT OUTER JOIN genres ON movies.genre_id = genre.id
//un peu mieux
SELECT movies.title, genre.name FROM movies LEFT OUTER JOIN genres ON movies.genre_id = genre.id

Nom b AS Alias b

```