## Objetivo
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/237/atbash.jpg).
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/HideTooSee]
└─$ steghide extract -sf atbash.jpg
Enter passphrase:
wrote extracted data to "encrypted.txt".

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/HideTooSee]
└─$ ls
atbash.jpg  encrypted.txt

┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoctf/HideTooSee]
└─$ cat encrypted.txt
krxlXGU{zgyzhs_xizxp_05y2z65z}
```
Después de obtener el formato de la bandera utilizamos un decodificador Atbash online para saber lo que dice y obtenemos lo siguiente: `picoCTF{atbash_crack_05b2a65a}`
## Notas adicionales

## Referencias
+ [Atbash - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Atbash)