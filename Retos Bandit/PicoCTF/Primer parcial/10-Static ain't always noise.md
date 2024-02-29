## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/static)? This [BASH script](https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/ltdis.sh) might help!
## Solución
```
┌──(jhow㉿DESKTOP-Q5FQ7BC)-[/mnt/c/retospicoCTF]
└─$ strings static | grep picoCTF
picoCTF{d15a5m_t34s3r_1e6a7731}
```
## Notas adicionales
+  El comando `strings` sirve para ver lo que hay dentro de un archivo cuando es un archivo binario
## Referencias



