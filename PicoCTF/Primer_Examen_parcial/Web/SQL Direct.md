## Descripción
Connect to this PostgreSQL server and find the flag! `psql -h xebec.cylabacademy.net -p 16170 -U postgres pico`

Password is `postgres`
## Solución
Lo primero que hice fue saber que tablas habia entonces use `\dt` y me salio la tabla flags, ya de ahi consulte lo que habia y pude obtener la bandera la cual es `academy{L3arN_S0m3_5qL_t0d4Y_412c85d9}`
```
pico=# help
You are using psql, the command-line interface to PostgreSQL.
Type:  \copyright for distribution terms
       \h for help with SQL commands
       \? for help with psql commands
       \g or terminate with semicolon to execute query
       \q to quit
pico=# \h
pico=# \?
pico=# \dt
          List of tables
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# SELECT * FROM flags LIMIT 10;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | academy{L3arN_S0m3_5qL_t0d4Y_412c85d9}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

```
## Notas Adicionales 
## Referencias
