## Objetivo
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Solución
Para este reto tuvimos que cambiar la extensión del archivo por lo que se hizo lo siguiente.
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ ls
capture.pcap  flag.txt

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ file flag.txt
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ mv flag.txt flag.png

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ ls
capture.pcap  flag.png
```
Después abrimos la imagen y es ahí donde encontramos la bandera, la cual es la siguiente:
`picoCTF{now_you_know_about_extensions}`
## Notas adicionales
+ Debemos de saber que además de mover un archivo de un directorio a otro el comando `mv` también sirve para cambiar la extensión de los archivos, siempre y cuando nos encontremos en el directorio donde se encuentra el archivo al cual queremos cambiarle la extensión.
## Referencias
+ [Cómo renombrar archivos en Linux con los comandos mv y rename (hostinger.mx)](https://www.hostinger.mx/tutoriales/renombrar-archivos-linux)