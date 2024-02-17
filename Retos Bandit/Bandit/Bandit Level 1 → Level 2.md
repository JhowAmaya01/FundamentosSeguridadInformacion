## Objetivo
The password for the next level is stored in a file called **-** located in the home directory

## Datos de acceso al nivel
bandit1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
## Solución
```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ 

```
## Notas adicionales
+ Al utilizar el comando cat seguido de un guion (cat -) la consola se queda esperando alguna instrucción.
+ Para solucionar el problema anterior con simbolos especiales se anteponen ./ para permitir abrir el archivo.
## Referencias
[linux - How to open a "-" dashed filename using terminal? - Stack Overflow](https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal)