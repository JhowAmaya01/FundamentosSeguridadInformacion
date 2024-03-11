## Objetivo
Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ strings pico_img.png | grep "pico"
picoCTF{s0_m3ta_d8944929}K
```
## Notas adicionales
+ Este reto también pudo resolverse utilizando la herramienta exiftool la cual muestra los metadatos de la imagen.
## Referencias
+ [Metadatos - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Metadatos) 