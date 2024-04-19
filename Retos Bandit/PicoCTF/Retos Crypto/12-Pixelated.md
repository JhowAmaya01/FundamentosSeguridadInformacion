## Objetivo
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/1594c3f1980e3fb93df09a6d02f53904/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/1594c3f1980e3fb93df09a6d02f53904/scrambled2.png)
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf]
└─$ cd pixelated

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/pixelated]
└─$ convert scrambled1.png scrambled2.png -compose Add -composite flag.png

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/pixelated]
└─$ ls
flag.png  scrambled1.png  scrambled2.png
```
Una vez hecho esto abrimos la imagen y observamos la bandera
## Notas adicionales

## Referencias
+ [Visual cryptography - Wikipedia](https://en.wikipedia.org/wiki/Visual_cryptography)
+ [ImageMagick – Create, Edit, Compose, or Convert Digital Images](https://imagemagick.org/index.php)