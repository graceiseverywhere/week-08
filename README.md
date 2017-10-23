# week-08
week 8 assignment
# data-structures
This includes: 
   1.  an articulation of my data model
   2.  the SQL code I used to create your table(s) and insert a row of values into the table(s)
   
   
   
   

An articulation of my data model


![alt text](https://github.com/graceiseverywhere/data-structures/blob/master/MSDV_DataStructures_grace_sensors_mockdesign.png
 "Initial Mockup design")





The SQL code you used to create your table(s) and insert a row of values into the table(s)

\\\create connection to AWS hosted db in cloud9 terminal

psql --host=datastructures.cqg9canqxxtt.us-east-2.rds.amazonaws.com --port=5432 --username=grace --password --dbname=sensors

\\\create table in cloud9 terminal 

CREATE TABLE gracesensors 
(
FSRSENSOR int, 
POTENTSENSOR varchar(20), 
sensortime timestamp DEFAULT current_timestamp);

CREATE TABLE gracesensors (FSRSENSOR int, POTENTSENSOR varchar(20), sensortime timestamp DEFAULT current_timestamp);

\\\insert statements into gracesensors 
sensors=> INSERT INTO gracesensors VALUES (1, 'motivated', DEFAULT);
sensors=> INSERT INTO gracesensors VALUES (5, 'unmotivated', DEFAULT);
sensors=> INSERT INTO gracesensors VALUES (8, 'motivated', DEFAULT);
sensors=> INSERT INTO gracesensors VALUES (9, 'motivated', DEFAULT);

\\\verifying table is there 
sensors=> \d
           List of relations
 Schema |     Name     | Type  | Owner 
--------+--------------+-------+-------
 public | gracesensors | table | grace
(1 row)


\\\select statement
sensors=> SELECT * from gracesensors;
 fsrsensor | potentsensor |         sensortime         
-----------+--------------+----------------------------
         1 | motivated    | 2017-10-23 17:23:51.702079
         5 | unmotivated  | 2017-10-23 17:24:53.893031
         8 | motivated    | 2017-10-23 17:25:01.295956
         9 | motivated    | 2017-10-23 17:25:07.760505
(4 rows)
