## Objetivo
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF]
└─$ nc jupiter.challenges.picoctf.org 4427 | grep picoCTF
picoCTF{digital_plumb3r_5ea1fbd7}
```
## Notas adicionales
+ Para resolver este reto utilice los conocimientos adquiridos en los retos de `First Grep`, `what's a net cat?` y `Nice netcat...`
## Referencias
