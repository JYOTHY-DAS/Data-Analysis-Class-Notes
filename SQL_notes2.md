AGGREGATE FUNCTIONS COUNT, MAX, MIN, AVG, SUM

SELECT MIN(year) FROM movies;
SELECT MAX(year) FROM movies;
SELECT COUNT(*) FROM movies;
SELECT COUNT(*) FROM movies where year>2000;
SELECT COUNT(year) FROM movies;


GROUP BY
    - often used with COUNT, MIN, MAX, or SUM
    - if grouping columns contain NULL values, all null values are grouped together

SELECT year, count(year) FROM movies GROUP BY year; # to know #ofmovies released/year

SELECT year, count(year) year_count FROM movies GROUP BY year ORDER BY year_count;
# here year_count is an alias


HAVING
    - Print years which have>1000 movies in our DB
    - Specifiy a condition on groups using HAVING

    - e.g. SELECT year, COUNT(year) year_count FROM movies GROUP BY year HAVING year_count>1000;

    - Order or execusion
        1. GROUP BY to create groups
        2. apply the aggregate functions
        3. apply having condition


    - HAVING is often used with GROUP BY but not mandatory
    - e.g. SELECT name, year FROM movies HAVING year>2000;
    - HAVING without GROUP BY is same as WHERE
    - WHERE is applied on individual rows while HAVING is applied on groups
    - HAVING is applied after grouping while WHERE is used before grouping
    - e.g. SELECT year, COUNT(year) year_count
           FROM movies
           WHERE rankscore>9
           GROUP BY year
           HAVING year_count>20;

Order of KEYWORDS
 - https://dev.mysql.com/doc/refman/8.4/en/select.html

 - SELECT * FROM WHERE G-H-O-L
 - *: ALL (even distinct can be used in this place)
 - G : GROUP BY
 - H : HAVING
 - O : ORDER BY (hav ASC and DESC)
 - L : LIMIT (has OFFSET)



Join and Natural Join
    - combine data in mutiple tables

INNER JOIN Example

SELECT A.ID, A.name, B.course
FROM TableA A
INNER JOIN TableB B
ON A.ID=B.ID


Natural JOIN Example

SELECT *
FROM TableA
NATURAL JOIN TableB;


LEFT JOIN Example

SELECT A.ID, A.name, B.course
FROM TableA A
LEFT JOIN TableB B
ON A.ID=B.ID

RIGHT JOIN Example

SELECT A.ID, A.name, B.course
FROM TableA A
RIGHT JOIN TableB B
ON A.ID=B.ID

FULL OUTER JOIN Example

SELECT A.ID, A.name, B.course
FROM TableA A
FULL OUTER JOIN TableB B
ON A.ID=B.ID





SELECT m.name, g.genre
FROM movies m
JOIN movie_genre g
ON m.id=g.movie_id
LIMIT 20;

    - here m and g are table alises
    - Natural join: a join where the same column-names across two tables
    - T1: C1, C2
    - T2: C1, C3, C4
    - SELECT * FROM T1 JOIN T2;
    - SELCECT * FROM T1 JOIN T2 USING (C1);
    - returns C1, C2, C3, C4
    - no need to use the keyword "ON"

Practice with Hacker Rank

Sub-Queries or Nested Queris or Inner Queries
    - First inner query is executed then outer query is executed

SELECT actor_id FROM roles WHERE movie_id IN
(SELECT id FROM movies where name='Schindler's List')

IN, NOT IN, EXISTS, NOT EXISTS, ANY, ALL, Comparison operators
    - ANY operator retuns TRUE if any of the subquery values meet the condition
    - ALL operator returns TRUE if all of the subquery values meet the condition

    - e.g. SELECT * FROM movies WHERE rankscore>= ALL (SELECT MAX(rankscore) FROM movies);


CREATE, READ, UPDATE, DELETE (CRUD)

CREATE
    - CREATE TABLE table_name (
    col1 col1_dtype,
    col2 col2_dtype,
    );

CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    grade CHAR(1)
);



INSERT

    - INSERT INTO movies(id, name, year, rankscore) VALUES (412321, 'Thor', 2011, 7);

    - INSERT INTO movies(id, name, year, rankscore) VALUES (412321, 'Thor', 2011, 7),
                                                           (412322, 'Iron Man', 2008, 7.9),
                                                           (412323, 'Iron Man 2', 2010, 7);
    - INSERT INTO students (id, name, age, grade) 
      VALUES (1, 'John Doe', 20, 'A');
      
    - INSERT INTO students (id, name, age, grade) 
        VALUES 
            (2, 'Jane Smith', 22, 'B'),
            (3, 'Mark Brown', 19, 'A');


UPDATE

    - UPDATE <TableName> SET col1=val1, col2=val2 WHERE condition;
    - UPDATE movies SET rankscore=9 where id=412321;
    - Can be used to update multiple rows at once

    - UPDATE students 
      SET grade = 'A+' 
      WHERE id = 2;

    - UPDATE students 
      SET age = 21, grade = 'B+' 
      WHERE name = 'Mark Brown';

ALTER: The ALTER TABLE statement is used to modify the structure of the table.
    - Adding new columns
        - ALTER TABLE students 
          ADD email VARCHAR(100);
    - Rename column
        - ALTER TABLE students 
         RENAME COLUMN grade TO final_grade;



DELETE
    - DELETE FROM movies WHERE id=412321


DROP
    - Deletes both tableand all of the data permanently
    - DROP TABLE Tablename;
    - DROP TABLE tablename IF EXISTS;

TRUNCATE
    - TRUNCATE delete the contents of the table but the not the table
    - where as DROP deletes the whole table itself
    - TRUNCATE TABLE tablename;
