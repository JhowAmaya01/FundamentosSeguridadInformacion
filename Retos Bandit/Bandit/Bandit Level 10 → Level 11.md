## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de acceso al nivel
bandit10
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
## Solución
```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt 
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

```
## Notas adicionales
El comando base64 se utiliza bastante para convertir en una imagen

## Referencias
+ Ayuda del comando base64
+ [Base64 - Wikipedia](https://en.wikipedia.org/wiki/Base64)