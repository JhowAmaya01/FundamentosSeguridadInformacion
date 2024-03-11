## Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.
## Solución
Para este reto utilice el comando `strings` el cuál muestra una cadena de caracteres ascii dentro de archivos binarios e imágenes.
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ strings garden.jpg | grep "pico"
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"
```
## Notas adicionales
+ Otra forma de resolver el reto es utilizar un editor hexadecimal para poder localizar la bandera. Una vez dentro del editor puede usarse `ctrl+w` para buscar una cadena de caracteres, en distintos formatos
## Referencias
