## Objetivo
Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 56435 -U postgres pico`Password is `postgres`
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ psql -h saturn.picoctf.net -p 56435 -U postgres pico
Password for user postgres:
psql (16.2 (Debian 16.2-1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# help
You are using psql, the command-line interface to PostgreSQL.
Type:  \copyright for distribution terms
       \h for help with SQL commands
       \? for help with psql commands
       \g or terminate with semicolon to execute query
       \q to quit
pico=# \?

[3]+  Stopped                 psql -h saturn.picoctf.net -p 56435 -U postgres pico

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ psql -h saturn.picoctf.net -p 56435 -U postgres pico
Password for user postgres:
psql (16.2 (Debian 16.2-1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico-# \dt
         List of relations
 Schema | Name  | Type  |  Owner
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)
        ^
pico=# select * from flags;
 id | firstname | lastname  |                address
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# exit
```
## Notas adicionales
+ En psql el comando `\dt` muestra las tablas que hay dentro de la base de datos.
## Referencias
